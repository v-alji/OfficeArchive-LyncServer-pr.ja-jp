---
title: 'Lync Server 2013: Web scheduler のテスト'
description: 'Lync Server 2013: Web scheduler をテストしています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing the Web scheduler
ms:assetid: 58e34058-1afa-42e3-9096-c4ea1954c237
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727304(v=OCS.15)
ms:contentKeyID: 63969603
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6512bf074078005eac66d1e4f5cd3d8ba2dc4bc7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439724"
---
# <a name="testing-the-web-scheduler-in-lync-server-2013"></a><span data-ttu-id="c3cac-103">Lync Server 2013 で Web scheduler をテストする</span><span class="sxs-lookup"><span data-stu-id="c3cac-103">Testing the Web scheduler in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c3cac-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c3cac-104">

<span> </span></span></span>

<span data-ttu-id="c3cac-105">_**最終更新日:** 2014-11-03_</span><span class="sxs-lookup"><span data-stu-id="c3cac-105">_**Topic Last Modified:** 2014-11-03_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c3cac-106">確認のスケジュール</span><span class="sxs-lookup"><span data-stu-id="c3cac-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="c3cac-107">[毎日]</span><span class="sxs-lookup"><span data-stu-id="c3cac-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3cac-108">テストツール</span><span class="sxs-lookup"><span data-stu-id="c3cac-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="c3cac-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c3cac-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3cac-110">必要なアクセス許可</span><span class="sxs-lookup"><span data-stu-id="c3cac-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="c3cac-111">Lync Server 管理シェルを使用してローカルで実行する場合、ユーザーは RTCUniversalServerAdmins セキュリティグループのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3cac-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="c3cac-112">Windows PowerShell のリモートインスタンスを使用して実行する場合、ユーザーには、 <strong>CsWebScheduler</strong> コマンドレットを実行するアクセス許可が与えられた RBAC の役割を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3cac-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsWebScheduler</strong> cmdlet.</span></span> <span data-ttu-id="c3cac-113">このコマンドレットを使うことができるすべての RBAC ロールの一覧を表示するには、Windows PowerShell プロンプトから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="c3cac-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsWebScheduler&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="c3cac-114">説明</span><span class="sxs-lookup"><span data-stu-id="c3cac-114">Description</span></span>

<span data-ttu-id="c3cac-115">**テスト用の webscheduler** コマンドレットを使用すると、特定のユーザーが Web Scheduler を使って会議をスケジュールできるかどうかを判断できます。</span><span class="sxs-lookup"><span data-stu-id="c3cac-115">The **Test-CsWebScheduler** cmdlet enables you to determine whether a specific user can schedule a meeting using the Web Scheduler.</span></span> <span data-ttu-id="c3cac-116">Web Scheduler は、Outlook を実行していないユーザーがオンライン会議をスケジュールすることを可能にします。</span><span class="sxs-lookup"><span data-stu-id="c3cac-116">The Web Scheduler enables users who are not running Outlook to schedule online meetings.</span></span> <span data-ttu-id="c3cac-117">この新機能 (Microsoft Lync Server 2010 リソースキットに含まれていた Web Scheduler ツールに含まれていた機能が組み込まれています) では、ユーザーは次のことを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="c3cac-117">Among other things, this new feature (which incorporates the functionality found in the Web Scheduler tool that was included with the Microsoft Lync Server 2010 resource kit) enables users to:</span></span>

  - <span data-ttu-id="c3cac-118">新しいオンライン会議をスケジュールします。</span><span class="sxs-lookup"><span data-stu-id="c3cac-118">Schedule a new online meeting.</span></span>

  - <span data-ttu-id="c3cac-119">自分がスケジュールしたすべての会議を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="c3cac-119">List all meetings that he or she has scheduled.</span></span>

  - <span data-ttu-id="c3cac-120">既存の会議を表示または変更する。</span><span class="sxs-lookup"><span data-stu-id="c3cac-120">View/modify an existing meeting.</span></span>

  - <span data-ttu-id="c3cac-121">既存の会議を削除します。</span><span class="sxs-lookup"><span data-stu-id="c3cac-121">Delete an existing meeting.</span></span>

  - <span data-ttu-id="c3cac-122">事前に構成された SMTP メールサーバーを使用して、会議の出席者にメール招待状を送信します。</span><span class="sxs-lookup"><span data-stu-id="c3cac-122">Send an email invitation to meeting participants by using a preconfigured SMTP mail server.</span></span>

  - <span data-ttu-id="c3cac-123">既存の会議に参加します。</span><span class="sxs-lookup"><span data-stu-id="c3cac-123">Join an existing conference.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="c3cac-124">テストの実行</span><span class="sxs-lookup"><span data-stu-id="c3cac-124">Running the test</span></span>

<span data-ttu-id="c3cac-125">次の例では、プール atl-cs-001.litwareinc.com の Web Scheduler を確認します。</span><span class="sxs-lookup"><span data-stu-id="c3cac-125">The following example verifies the Web Scheduler for the pool atl-cs-001.litwareinc.com.</span></span> <span data-ttu-id="c3cac-126">このコマンドは、プール atl-cs-001.litwareinc.com に対してテストユーザーが定義されている場合にのみ機能します。</span><span class="sxs-lookup"><span data-stu-id="c3cac-126">This command will work only if test users are defined for the pool atl-cs-001.litwareinc.com.</span></span> <span data-ttu-id="c3cac-127">その場合、コマンドは、最初のテストユーザーが Web Scheduler を使ってオンライン会議をスケジュールできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="c3cac-127">If they have, then the command will determine whether the first test user can schedule an online meeting using the Web Scheduler.</span></span>

<span data-ttu-id="c3cac-128">テストユーザーが定義されていない場合は、どのユーザーとしてログオンするかがわからないため、コマンドは失敗します。</span><span class="sxs-lookup"><span data-stu-id="c3cac-128">If test users are not defined, then the command will fail because it won't know which user to log on as.</span></span> <span data-ttu-id="c3cac-129">プールのテストユーザーを定義していない場合は、UserSipAddress パラメーターと、ログオンしようとしたときにコマンドによって使用されるユーザーの資格情報を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3cac-129">If you have not defined test users for a pool, then you must include the UserSipAddress parameter and the credentials of the user the command should use when trying to log on.</span></span>

    Test-CsWebScheduler -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="c3cac-130">次の例に示すコマンドは、 \\ Web scheduler を使ってオンライン会議をスケジュールするために、特定のユーザー (litwareinc kenmeyer) の機能をテストします。</span><span class="sxs-lookup"><span data-stu-id="c3cac-130">The commands shown in the next example test the ability of a specific user (litwareinc\\kenmeyer) to schedule an online meeting using the Web scheduler.</span></span> <span data-ttu-id="c3cac-131">これを行うには、この例の最初のコマンドでは、 **Credential** コマンドレットを使用して、ユーザー Ken Meyer の名前とパスワードを含む Windows PowerShell コマンドラインインターフェイスの資格情報オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="c3cac-131">To do this, the first command in the example uses the **Get-Credential** cmdlet to create a Windows PowerShell command-line interface credential object that contains the name and password of the user Ken Meyer.</span></span> <span data-ttu-id="c3cac-132">(Logon name litwareinc \\ kenmeyer はパラメーターとして含まれているため、Windows PowerShell 資格情報の要求ダイアログボックスでは、管理者が Ken Meyer account のパスワードを入力するだけであることになります。)結果として得られた資格情報オブジェクトは、$cred 1 という名前の変数に格納されます。</span><span class="sxs-lookup"><span data-stu-id="c3cac-132">(Because the logon name litwareinc\\kenmeyer is included as a parameter, the Windows PowerShell Credential Request dialog box only requires the administrator to enter the password for the Ken Meyer account.) The resulting credential object is then stored in a variable named $cred1.</span></span>

<span data-ttu-id="c3cac-133">2番目のコマンドは、このユーザーがプール atl-cs-001.litwareinc.com にログオンしてオンライン会議をスケジュールできるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="c3cac-133">The second command then checks whether this user can log on to the pool atl-cs-001.litwareinc.com and schedule an online meeting.</span></span> <span data-ttu-id="c3cac-134">このタスクを実行するために、 **テスト用の Webscheduler** コマンドレットが呼び出され、次の3つのパラメーター (レジストラープールの FQDN) が使用されます。UserCredential (Pilar Ackerman のユーザー資格情報を格納する Windows PowerShell オブジェクト)UserSipAddress (提供されているユーザー資格情報に対応する SIP アドレス) を選びます。</span><span class="sxs-lookup"><span data-stu-id="c3cac-134">To run this task, the **Test-CsWebScheduler** cmdlet is called, together with three parameters: TargetFqdn (the FQDN of the Registrar pool); UserCredential (the Windows PowerShell object that contains Pilar Ackerman’s user credentials); and UserSipAddress (the SIP address that corresponds to the supplied user credentials).</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    
    Test-CsWebScheduler -TargetFqdn "atl-cs-001.litwareinc.com" -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="c3cac-135">成功または失敗を確認する</span><span class="sxs-lookup"><span data-stu-id="c3cac-135">Determining success or failure</span></span>

<span data-ttu-id="c3cac-136">Web scheduler が適切に構成されている場合は、次のような結果が返され、Result プロパティは **Success** とマークされます。</span><span class="sxs-lookup"><span data-stu-id="c3cac-136">If the web scheduler is configured correctly , you'll receive output similar to this, with the Result property marked as **Success**:</span></span>

<span data-ttu-id="c3cac-137">ターゲット Fqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="c3cac-137">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="c3cac-138">ターゲット Uri: https://atl-cs-001.litwareinc.com。</span><span class="sxs-lookup"><span data-stu-id="c3cac-138">Target Uri : https:// atl-cs-001.litwareinc.com.</span></span>

<span data-ttu-id="c3cac-139">litwareinc.com:443/Scheduler</span><span class="sxs-lookup"><span data-stu-id="c3cac-139">litwareinc.com:443/Scheduler</span></span>

<span data-ttu-id="c3cac-140">結果: 成功</span><span class="sxs-lookup"><span data-stu-id="c3cac-140">Result : Success</span></span>

<span data-ttu-id="c3cac-141">待ち時間: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="c3cac-141">Latency : 00:00:00</span></span>

<span data-ttu-id="c3cac-142">エラーメッセージ:</span><span class="sxs-lookup"><span data-stu-id="c3cac-142">Error Message :</span></span>

<span data-ttu-id="c3cac-143">診断</span><span class="sxs-lookup"><span data-stu-id="c3cac-143">Diagnosis :</span></span>

<span data-ttu-id="c3cac-144">Web scheduler が正しく構成されていない場合は、結果が **失敗** として表示され、エラーと診断のプロパティに追加情報が記録されます。</span><span class="sxs-lookup"><span data-stu-id="c3cac-144">If the web scheduler is not configured correctly, the Result will be shown as **Failure**, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="c3cac-145">警告: 指定した完全修飾のレジストラーポート番号の読み取りに失敗しました</span><span class="sxs-lookup"><span data-stu-id="c3cac-145">WARNING: Failed to read Registrar port number for the given fully qualified</span></span>

<span data-ttu-id="c3cac-146">ドメイン名 (FQDN)。</span><span class="sxs-lookup"><span data-stu-id="c3cac-146">domain name (FQDN).</span></span> <span data-ttu-id="c3cac-147">既定のレジストラーポート番号を使用します。</span><span class="sxs-lookup"><span data-stu-id="c3cac-147">Using default Registrar port number.</span></span> <span data-ttu-id="c3cac-148">エラー</span><span class="sxs-lookup"><span data-stu-id="c3cac-148">Exception:</span></span>

<span data-ttu-id="c3cac-149">InvalidOperationException: トポロジで一致するクラスターが見つかりませんでした。</span><span class="sxs-lookup"><span data-stu-id="c3cac-149">System.InvalidOperationException: No matching cluster found in topology.</span></span>

<span data-ttu-id="c3cac-150">自宅</span><span class="sxs-lookup"><span data-stu-id="c3cac-150">at</span></span>

<span data-ttu-id="c3cac-151">SipSyntheticTransaction-TryRetri の同期を行います。</span><span class="sxs-lookup"><span data-stu-id="c3cac-151">Microsoft.Rtc.Management.SyntheticTransactions.SipSyntheticTransaction.TryRetri</span></span>

<span data-ttu-id="c3cac-152">eveRegistrarPortFromTopology (Int32& registrarPortNumber)</span><span class="sxs-lookup"><span data-stu-id="c3cac-152">eveRegistrarPortFromTopology(Int32& registrarPortNumber)</span></span>

<span data-ttu-id="c3cac-153">ターゲット Fqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="c3cac-153">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="c3cac-154">ターゲット Uri:</span><span class="sxs-lookup"><span data-stu-id="c3cac-154">Target Uri :</span></span>

<span data-ttu-id="c3cac-155">結果: エラー</span><span class="sxs-lookup"><span data-stu-id="c3cac-155">Result : Failure</span></span>

<span data-ttu-id="c3cac-156">待ち時間: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="c3cac-156">Latency : 00:00:00</span></span>

<span data-ttu-id="c3cac-157">エラーメッセージ: 一致するクラスターがトポロジに見つかりませんでした。</span><span class="sxs-lookup"><span data-stu-id="c3cac-157">Error Message : No matching cluster found in topology.</span></span>

<span data-ttu-id="c3cac-158">診断</span><span class="sxs-lookup"><span data-stu-id="c3cac-158">Diagnosis :</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="c3cac-159">テストに失敗した可能性がある理由</span><span class="sxs-lookup"><span data-stu-id="c3cac-159">Reasons why the test might have failed</span></span>

<span data-ttu-id="c3cac-160">次に **、テスト用の Webscheduler スケジューラ** が機能しない場合の一般的な理由を示します。</span><span class="sxs-lookup"><span data-stu-id="c3cac-160">Here are some common reasons why **Test-CsWebScheduler** might fail:</span></span>

  - <span data-ttu-id="c3cac-161">指定されたパラメーター値が正しくありません。</span><span class="sxs-lookup"><span data-stu-id="c3cac-161">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="c3cac-162">使用する場合は、オプションのパラメーターが正しく構成されている必要があります。または、テストが失敗します。</span><span class="sxs-lookup"><span data-stu-id="c3cac-162">If used, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="c3cac-163">省略可能なパラメーターを指定せずにコマンドを再実行し、それが成功するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="c3cac-163">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

  - <span data-ttu-id="c3cac-164">Web Scheduler が正しく構成されていない場合、またはまだ展開されていない場合、このコマンドは失敗します。</span><span class="sxs-lookup"><span data-stu-id="c3cac-164">This command will fail if the Web Scheduler is misconfigured or not yet deployed.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="c3cac-165">関連項目</span><span class="sxs-lookup"><span data-stu-id="c3cac-165">See Also</span></span>


[<span data-ttu-id="c3cac-166">Set-CsWebServer</span><span class="sxs-lookup"><span data-stu-id="c3cac-166">Set-CsWebServer</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsWebServer)  
  

<span data-ttu-id="c3cac-167"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c3cac-167"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

