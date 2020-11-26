---
title: 'Lync Server 2013: ウォッチャーノード構成のテスト'
description: 'Lync Server 2013: ウォッチャーノード構成をテストしています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing watcher node configuration
ms:assetid: f9ecd85c-0ae9-4906-b786-6b002b5a77c6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn751537(v=OCS.15)
ms:contentKeyID: 63969667
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f1eeb141eee011d7e06f5dd49e483e026484d733
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440928"
---
# <a name="testing-watcher-node-configuration-in-lync-server-2013"></a><span data-ttu-id="b8a05-103">Lync Server 2013 でのウォッチャーノード構成のテスト</span><span class="sxs-lookup"><span data-stu-id="b8a05-103">Testing watcher node configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b8a05-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b8a05-104">

<span> </span></span></span>

<span data-ttu-id="b8a05-105">_**最終更新日:** 2014-11-03_</span><span class="sxs-lookup"><span data-stu-id="b8a05-105">_**Topic Last Modified:** 2014-11-03_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b8a05-106">確認のスケジュール</span><span class="sxs-lookup"><span data-stu-id="b8a05-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="b8a05-107">[毎日]</span><span class="sxs-lookup"><span data-stu-id="b8a05-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8a05-108">テストツール</span><span class="sxs-lookup"><span data-stu-id="b8a05-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="b8a05-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="b8a05-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8a05-110">必要なアクセス許可</span><span class="sxs-lookup"><span data-stu-id="b8a05-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="b8a05-111">Lync Server 管理シェルを使用してローカルで実行する場合、ユーザーは RTCUniversalServerAdmins セキュリティグループのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8a05-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="b8a05-112">Windows PowerShell のリモートインスタンスを使って実行する場合は、 <strong>CsWatcherNodeConfiguration</strong> コマンドレットを実行するためのアクセス許可が与えられている RBAC の役割をユーザーに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8a05-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsWatcherNodeConfiguration</strong> cmdlet.</span></span> <span data-ttu-id="b8a05-113">このコマンドレットを使うことができるすべての RBAC ロールの一覧を表示するには、Windows PowerShell プロンプトから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="b8a05-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot; Test-CsWatcherNodeConfiguration&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="b8a05-114">説明</span><span class="sxs-lookup"><span data-stu-id="b8a05-114">Description</span></span>

<span data-ttu-id="b8a05-115">Microsoft System Center Operations Manager を使って Lync Server 2013 を監視している場合は、"ウォッチャーノード" を設定することができます。定期的に自動的に実行されるコンピューターは、Lync Server が予期したとおりに動作していることを確認するために、代理トランザクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="b8a05-115">If you are using Microsoft System Center Operations Manager to monitor Lync Server 2013 then you have the option of setting up "watcher nodes": computers that periodically, and automatically, run synthetic transactions to verify that Lync Server is working as expected.</span></span> <span data-ttu-id="b8a05-116">ウォッチャーノードはプールに割り当てられ、 **CsWatcherNodeConfiguration** コマンドレットを使用して管理されます。</span><span class="sxs-lookup"><span data-stu-id="b8a05-116">Watcher nodes are assigned to pools, and are managed by using the **CsWatcherNodeConfiguration** cmdlets.</span></span> <span data-ttu-id="b8a05-117">System Center Operations Manager を使用している場合は、監視ノードをインストールする必要はないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="b8a05-117">Note that you do not need to install watcher nodes if you are using System Center Operations Manager.</span></span> <span data-ttu-id="b8a05-118">ウォッチャーノードを使用しなくてもシステムを監視することができます。</span><span class="sxs-lookup"><span data-stu-id="b8a05-118">You can still monitor your system without using watcher nodes.</span></span> <span data-ttu-id="b8a05-119">唯一の違いは、実行しようとしている代理トランザクションは、Operations Manager によって自動的に呼び出されるのではなく手動で呼び出す必要がある点です。</span><span class="sxs-lookup"><span data-stu-id="b8a05-119">The only difference is that any synthetic transactions that you want to run must be invoked manually instead of automatically invoked by Operations Manager.</span></span>

<span data-ttu-id="b8a05-120">**CsWatcherNodeConfiguration** コマンドレットを使用すると、ウォッチャーノードが正しく構成されていることを確認し、有効な Lync Server 2013 プールに割り当てられていることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="b8a05-120">The **Test-CsWatcherNodeConfiguration** cmdlet enables you to verify that a watcher node was configured correctly and is assigned to a valid Lync Server 2013 pool.</span></span> <span data-ttu-id="b8a05-121">**CsWatcherNodeConfiguration** コマンドレットは、ウォッチャーノード自体で実行されている必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="b8a05-121">Note that the **Test-CsWatcherNodeConfiguration** cmdlet must be run on the watcher node itself.</span></span> <span data-ttu-id="b8a05-122">リモートコンピューターに対してコマンドレットを実行することはできません。</span><span class="sxs-lookup"><span data-stu-id="b8a05-122">The cmdlet cannot be run against remote computers.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="b8a05-123">テストの実行</span><span class="sxs-lookup"><span data-stu-id="b8a05-123">Running the test</span></span>

<span data-ttu-id="b8a05-124">次のコマンドは、組織で使用されている各ウォッチャーノードの構成設定を確認します。</span><span class="sxs-lookup"><span data-stu-id="b8a05-124">The following command verifies the configuration settings for each watcher node that is being used in the organization.</span></span>

    Test-CsWatcherNodeConfiguration

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="b8a05-125">成功または失敗を確認する</span><span class="sxs-lookup"><span data-stu-id="b8a05-125">Determining success or failure</span></span>

<span data-ttu-id="b8a05-126">次の正常なサンプル出力は、4台のエッジサーバーを備えたシステムを示しています。</span><span class="sxs-lookup"><span data-stu-id="b8a05-126">The following successful sample output shows a system with four edge servers.</span></span>

<span data-ttu-id="b8a05-127">トポロジに対するターゲットプールの atl-cs-001.litwareinc.com を検証しています。</span><span class="sxs-lookup"><span data-stu-id="b8a05-127">Validating target pool atl-cs-001.litwareinc.com against topology.</span></span>

<span data-ttu-id="b8a05-128">成功: ターゲットプール atl-cs-001.litwareinc.com はトポロジ内に存在します。</span><span class="sxs-lookup"><span data-stu-id="b8a05-128">Success: Target pool atl-cs-001.litwareinc.com exists in topology.</span></span>

<span data-ttu-id="b8a05-129">成功: ターゲットプールの atl-cs-001.litwareinc.com には、レジストラーの役割がインストールされています。</span><span class="sxs-lookup"><span data-stu-id="b8a05-129">Success: Target pool atl-cs-001.litwareinc.com has Registrar role installed.</span></span>

<span data-ttu-id="b8a05-130">成功: ターゲットプール atl-cs-001.litwareinc.com はサポートされているバージョンです。</span><span class="sxs-lookup"><span data-stu-id="b8a05-130">Success: Target pool atl-cs-001.litwareinc.com is supported version.</span></span>

<span data-ttu-id="b8a05-131">成功: 5061 ターゲットプール atl-cs-001.litwareinc.com のポート番号が正しい。</span><span class="sxs-lookup"><span data-stu-id="b8a05-131">Success: Port number for 5061 Target pool atl-cs-001.litwareinc.com is correct.</span></span>

<span data-ttu-id="b8a05-132">ウォッチャーノード構成で見つからないプールの確認が開始されました。</span><span class="sxs-lookup"><span data-stu-id="b8a05-132">Checking for missing pools in watcher node configuration is started.</span></span> <span data-ttu-id="b8a05-133">エラーが検出された場合は、印刷されます。</span><span class="sxs-lookup"><span data-stu-id="b8a05-133">If any error is detected, it will be printed.</span></span>

<span data-ttu-id="b8a05-134">ウォッチャーノード構成で見つからないプールの確認が完了しました。</span><span class="sxs-lookup"><span data-stu-id="b8a05-134">Checking for missing pools in watcher node configuration is finished.</span></span>

<span data-ttu-id="b8a05-135">ウォッチャーノードのインストールによって作成されたウォッチャーノードレジストリキーの確認が開始されました。</span><span class="sxs-lookup"><span data-stu-id="b8a05-135">Checking for watcher node registry keys created by watcher node installation, is started.</span></span> <span data-ttu-id="b8a05-136">エラーが検出された場合は、印刷されます。</span><span class="sxs-lookup"><span data-stu-id="b8a05-136">If any error is detected, it will be printed.</span></span>

<span data-ttu-id="b8a05-137">ウォッチャーノードのインストールによって作成されたウォッチャーノードレジストリキーの確認は完了しています。</span><span class="sxs-lookup"><span data-stu-id="b8a05-137">Checking for watcher node registry keys created by watcher node installation, is finished.</span></span> <span data-ttu-id="b8a05-138">検出された認証の種類は Negotiate です。</span><span class="sxs-lookup"><span data-stu-id="b8a05-138">Detected authentication type is Negotiate.</span></span>

<span data-ttu-id="b8a05-139">テストユーザーの資格情報 sip の存在が正常に検証されました: user1@ atl-cs-001.litwareinc.com (credential management store)。</span><span class="sxs-lookup"><span data-stu-id="b8a05-139">Successfully validated existence of test user’s credential sip:user1@ atl-cs-001.litwareinc.com in credential management store.</span></span>

<span data-ttu-id="b8a05-140">テストユーザーの資格情報 sip の存在が正常に検証されました: user2@ atl-cs-001.litwareinc.com (credential management store)。</span><span class="sxs-lookup"><span data-stu-id="b8a05-140">Successfully validated existence of test user’s credential sip:user2@ atl-cs-001.litwareinc.com in credential management store.</span></span>

<span data-ttu-id="b8a05-141">ウォッチャーノード構成で見つからないプールの確認が開始されました。</span><span class="sxs-lookup"><span data-stu-id="b8a05-141">Checking for missing pools in watcher node configuration is started.</span></span> <span data-ttu-id="b8a05-142">エラーが検出された場合は、印刷されます。</span><span class="sxs-lookup"><span data-stu-id="b8a05-142">If any error is detected, it will be printed.</span></span>

<span data-ttu-id="b8a05-143">警告: Pool atl-cs-001.litwareinc.com にレジストラーが含まれています</span><span class="sxs-lookup"><span data-stu-id="b8a05-143">WARNING: Pool atl-cs-001.litwareinc.com has Registrar</span></span>

<span data-ttu-id="b8a05-144">ロールはインストールされていますが、テストユーザーが構成されていません。</span><span class="sxs-lookup"><span data-stu-id="b8a05-144">role installed, but there are no test users configured for it.</span></span>

<span data-ttu-id="b8a05-145">ウォッチャーノード構成で見つからないプールの確認が完了しました。</span><span class="sxs-lookup"><span data-stu-id="b8a05-145">Checking for missing pools in watcher node configuration is finished.</span></span>

<span data-ttu-id="b8a05-146">ウォッチャーノードのインストールによって作成されたウォッチャーノードレジストリキーの確認は、</span><span class="sxs-lookup"><span data-stu-id="b8a05-146">Checking for watcher node registry keys created by watcher node installation, is</span></span>

<span data-ttu-id="b8a05-147">さ.</span><span class="sxs-lookup"><span data-stu-id="b8a05-147">started.</span></span> <span data-ttu-id="b8a05-148">エラーが検出された場合は、印刷されます。</span><span class="sxs-lookup"><span data-stu-id="b8a05-148">If any error is detected, it will be printed.</span></span>

<span data-ttu-id="b8a05-149">Test-CsWatcherNodeConfiguration: で正常性レジストリキーが見つかりません</span><span class="sxs-lookup"><span data-stu-id="b8a05-149">Test-CsWatcherNodeConfiguration : Cannot find Health registry key in</span></span>

<span data-ttu-id="b8a05-150">\\Microsoft \\ リアルタイム通信ソフトウェア。</span><span class="sxs-lookup"><span data-stu-id="b8a05-150">Software\\Microsoft\\Real-Time Communications.</span></span> <span data-ttu-id="b8a05-151">Watcher ノードの .msi が</span><span class="sxs-lookup"><span data-stu-id="b8a05-151">Make sure watcher node .msi is</span></span>

<span data-ttu-id="b8a05-152">正しくインストールされている。</span><span class="sxs-lookup"><span data-stu-id="b8a05-152">installed properly.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="b8a05-153">テストに失敗した可能性がある理由</span><span class="sxs-lookup"><span data-stu-id="b8a05-153">Reasons why the test might have failed</span></span>

<span data-ttu-id="b8a05-154">次に **、テスト-CsWatcherNodeConfiguration** が失敗する可能性がある一般的な理由を示します。</span><span class="sxs-lookup"><span data-stu-id="b8a05-154">Here are some common reasons why **Test-CsWatcherNodeConfiguration** might fail:</span></span>

  - <span data-ttu-id="b8a05-155">ウォッチャーノードが正しくインストールされていません。</span><span class="sxs-lookup"><span data-stu-id="b8a05-155">Watcher node is not correctly installed.</span></span>

  - <span data-ttu-id="b8a05-156">テストユーザーが構成されていません。</span><span class="sxs-lookup"><span data-stu-id="b8a05-156">No test users are configured.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="b8a05-157">関連項目</span><span class="sxs-lookup"><span data-stu-id="b8a05-157">See Also</span></span>


[<span data-ttu-id="b8a05-158">Get-CsWatcherNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8a05-158">Get-CsWatcherNodeConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsWatcherNodeConfiguration)  
[<span data-ttu-id="b8a05-159">New-CsWatcherNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8a05-159">New-CsWatcherNodeConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsWatcherNodeConfiguration)  
[<span data-ttu-id="b8a05-160">Remove-CsWatcherNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8a05-160">Remove-CsWatcherNodeConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsWatcherNodeConfiguration)  
[<span data-ttu-id="b8a05-161">Set-CsWatcherNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8a05-161">Set-CsWatcherNodeConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsWatcherNodeConfiguration)  
  

<span data-ttu-id="b8a05-162"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b8a05-162"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

