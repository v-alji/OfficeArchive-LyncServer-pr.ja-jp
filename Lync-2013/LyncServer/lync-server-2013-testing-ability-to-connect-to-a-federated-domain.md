---
title: 'Lync Server 2013: フェデレーションドメインに接続する機能をテストする'
description: 'Lync Server 2013: フェデレーションドメインに接続する機能をテストしています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing ability to connect to a federated domain
ms:assetid: d8ccfade-ef54-47a4-9f87-36213a635ce5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743840(v=OCS.15)
ms:contentKeyID: 63969653
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bf1f5bdef66d34b9ca2e39797df0b4ad32d9afde
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441138"
---
# <a name="testing-ability-to-connect-to-a-federated-domain-from-lync-server-2013"></a><span data-ttu-id="0b0f0-103">Lync Server 2013 からフェデレーションドメインに接続するためのテスト機能</span><span class="sxs-lookup"><span data-stu-id="0b0f0-103">Testing ability to connect to a federated domain from Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0b0f0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0b0f0-104">

<span> </span></span></span>

<span data-ttu-id="0b0f0-105">_**最終更新日:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="0b0f0-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0b0f0-106">確認のスケジュール</span><span class="sxs-lookup"><span data-stu-id="0b0f0-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="0b0f0-107">[毎日]</span><span class="sxs-lookup"><span data-stu-id="0b0f0-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b0f0-108">テストツール</span><span class="sxs-lookup"><span data-stu-id="0b0f0-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="0b0f0-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="0b0f0-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b0f0-110">必要なアクセス許可</span><span class="sxs-lookup"><span data-stu-id="0b0f0-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="0b0f0-111">Lync Server 管理シェルを使用してローカルで実行する場合、ユーザーは RTCUniversalServerAdmins セキュリティグループのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="0b0f0-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="0b0f0-112">Windows PowerShell のリモートインスタンスを使って実行する場合は、Test-CsFederatedPartner コマンドレットを実行するためのアクセス許可を持つ RBAC の役割をユーザーに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="0b0f0-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsFederatedPartner cmdlet.</span></span> <span data-ttu-id="0b0f0-113">このコマンドレットを使うことができるすべての RBAC ロールの一覧を表示するには、Windows PowerShell プロンプトから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="0b0f0-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsFederatedPartner&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="0b0f0-114">説明</span><span class="sxs-lookup"><span data-stu-id="0b0f0-114">Description</span></span>

<span data-ttu-id="0b0f0-115">Test-CsFederatedPartner は、フェデレーションパートナーのドメインに接続できるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="0b0f0-115">Test-CsFederatedPartner verifies your ability to connect to the domain of a federated partner.</span></span> <span data-ttu-id="0b0f0-116">ドメインへの接続を確認するには、そのドメインが許可された (フェデレーションされた) ドメインのコレクションに表示されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="0b0f0-116">To verify the connectivity to a domain, that domain must be listed in the collection of allowed (federated) domains.</span></span> <span data-ttu-id="0b0f0-117">次のコマンドを使用して、許可ドメインの一覧にあるドメインの一覧を取得できます。</span><span class="sxs-lookup"><span data-stu-id="0b0f0-117">You can retrieve a list of the domains on your allowed domains list by using this command:</span></span>

    Get-CsAllowedDomain

<span data-ttu-id="0b0f0-118">詳細については、「 [CsFederatedPartner](https://docs.microsoft.com/powershell/module/skype/Test-CsFederatedPartner) コマンドレットのヘルプドキュメント」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0b0f0-118">For more information, see the Help documentation for the [Test-CsFederatedPartner](https://docs.microsoft.com/powershell/module/skype/Test-CsFederatedPartner) cmdlet.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="0b0f0-119">テストの実行</span><span class="sxs-lookup"><span data-stu-id="0b0f0-119">Running the test</span></span>

<span data-ttu-id="0b0f0-120">Test-FederatedPartner コマンドレットには、エッジサーバーの FQDN とフェデレーションパートナーの FQDN という2つの情報が必要です。</span><span class="sxs-lookup"><span data-stu-id="0b0f0-120">The Test-FederatedPartner cmdlet requires two pieces of information: the FQDN of your Edge Server and the FQDN of the federated partner.</span></span> <span data-ttu-id="0b0f0-121">たとえば、次のコマンドは、ドメイン contoso.com に接続する機能をテストします。</span><span class="sxs-lookup"><span data-stu-id="0b0f0-121">For example, this command tests the ability to connect to the domain contoso.com:</span></span>

    Test-CsFederatedPartner -TargetFqdn "atl-edge-001.litwareinc.com" -Domain "contoso.com"

<span data-ttu-id="0b0f0-122">このコマンドを使用すると、許可ドメインリストに現在あるすべてのドメインへの接続をテストすることができます。</span><span class="sxs-lookup"><span data-stu-id="0b0f0-122">This command enables you to test the connections to all the domains currently on your allowed domains list:</span></span>

    Get-CsAllowedDomain | ForEach-Object {Test-CsFederatedPartner -TargetFqdn "atl-edge-001.litwareinc.com" -Domain $_.Identity}

<span data-ttu-id="0b0f0-123">詳細については、「 [CsFederatedPartner](https://docs.microsoft.com/powershell/module/skype/Test-CsFederatedPartner) コマンドレットのヘルプドキュメント」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0b0f0-123">For more information, see the Help documentation for the [Test-CsFederatedPartner](https://docs.microsoft.com/powershell/module/skype/Test-CsFederatedPartner) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="0b0f0-124">成功または失敗を確認する</span><span class="sxs-lookup"><span data-stu-id="0b0f0-124">Determining success or failure</span></span>

<span data-ttu-id="0b0f0-125">指定したドメインに接続できる場合は、次のような結果として、Success とマークされた Result プロパティが出力され **ます。**</span><span class="sxs-lookup"><span data-stu-id="0b0f0-125">If the specified domain can be contacted, you'll receive output similar to this with the Result property marked as **Success:**</span></span>

<span data-ttu-id="0b0f0-126">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="0b0f0-126">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="0b0f0-127">結果: 成功</span><span class="sxs-lookup"><span data-stu-id="0b0f0-127">Result : Success</span></span>

<span data-ttu-id="0b0f0-128">待ち時間: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="0b0f0-128">Latency : 00:00:00</span></span>

<span data-ttu-id="0b0f0-129">誤差</span><span class="sxs-lookup"><span data-stu-id="0b0f0-129">Error :</span></span>

<span data-ttu-id="0b0f0-130">診断</span><span class="sxs-lookup"><span data-stu-id="0b0f0-130">Diagnosis :</span></span>

<span data-ttu-id="0b0f0-131">指定したドメインに接続できない場合、結果はエラーとして表示され、エラーと診断のプロパティに追加情報が記録されます。</span><span class="sxs-lookup"><span data-stu-id="0b0f0-131">If the specified domain cannot be contacted, then the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="0b0f0-132">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="0b0f0-132">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="0b0f0-133">結果: エラー</span><span class="sxs-lookup"><span data-stu-id="0b0f0-133">Result : Failure</span></span>

<span data-ttu-id="0b0f0-134">待ち時間: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="0b0f0-134">Latency : 00:00:00</span></span>

<span data-ttu-id="0b0f0-135">エラー: 504、サーバーのタイムアウト</span><span class="sxs-lookup"><span data-stu-id="0b0f0-135">Error : 504, Server time-out</span></span>

<span data-ttu-id="0b0f0-136">診断: ErrorCode = 2、Source = litwareinc、Reason = を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0b0f0-136">Diagnosis : ErrorCode=2, Source=atl-cs-001.litwareinc.com,Reason=See</span></span>

<span data-ttu-id="0b0f0-137">応答コードと理由の語句。</span><span class="sxs-lookup"><span data-stu-id="0b0f0-137">response code and reason phrase.</span></span>

<span data-ttu-id="0b0f0-138">DiagnosticHeader の場合</span><span class="sxs-lookup"><span data-stu-id="0b0f0-138">Microsoft.Rtc.Signaling.DiagnosticHeader</span></span>

<span data-ttu-id="0b0f0-139">たとえば、前回の出力では、サーバーのタイムアウトエラーのためにテストが失敗したことが示されます。</span><span class="sxs-lookup"><span data-stu-id="0b0f0-139">For example, the previous output states that the test failed because of a server time-out error.</span></span> <span data-ttu-id="0b0f0-140">これは通常、ネットワーク接続の問題、またはエッジサーバーへの接続の問題を示します。</span><span class="sxs-lookup"><span data-stu-id="0b0f0-140">This typically indicates either network connectivity problems or problems contacting the Edge Server.</span></span>

<span data-ttu-id="0b0f0-141">Test-CsFederatedPartner が失敗した場合は、Verbose パラメーターも含めて、テストを再実行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="0b0f0-141">If Test-CsFederatedPartner fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsFederatedPartner -TargetFqdn "atl-edge-001.litwareinc.com" -Domain "contoso.com" -Verbose

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="0b0f0-142">テストに失敗した可能性がある理由</span><span class="sxs-lookup"><span data-stu-id="0b0f0-142">Reasons why the test might have failed</span></span>

<span data-ttu-id="0b0f0-143">Test-CsFederatedPartner が失敗する可能性がある一般的な理由を次に示します。</span><span class="sxs-lookup"><span data-stu-id="0b0f0-143">Here are some common reasons why Test-CsFederatedPartner might fail:</span></span>

  - <span data-ttu-id="0b0f0-144">エッジサーバーが利用できない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0b0f0-144">The Edge Server might not be available.</span></span> <span data-ttu-id="0b0f0-145">このコマンドを使用して、エッジサーバーの Fqdn を使用できます。</span><span class="sxs-lookup"><span data-stu-id="0b0f0-145">You can the FQDNs of your Edge Servers by using this command:</span></span>
    
        Get-CsService -EdgeServer | Select-Object PoolFqdn
    
    <span data-ttu-id="0b0f0-146">次に、各エッジサーバーに対して ping を実行して、ネットワーク経由でアクセスできることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="0b0f0-146">You can then ping each Edge Server to verify that it can be accessed over the network.</span></span> <span data-ttu-id="0b0f0-147">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="0b0f0-147">For example:</span></span>
    
        ping atl-edge-001.litwareinc.com

  - <span data-ttu-id="0b0f0-148">指定したドメインが [許可したドメイン] リストに表示されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="0b0f0-148">The specified domain might not be listed on the allowed domains list.</span></span> <span data-ttu-id="0b0f0-149">許可ドメインリストに追加されたドメインを確認するには、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="0b0f0-149">To verify the domains that were added to the allowed domains list, use this command:</span></span>
    
        Get-CsAllowedDomain
    
    <span data-ttu-id="0b0f0-150">ユーザーが通信をブロックされたドメインの一覧を表示するには、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="0b0f0-150">If you’d like to see a list of domains that users were blocked from communicating with, then use this command:</span></span>
    
        Get-CsBlockedDomain

<span data-ttu-id="0b0f0-151"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0b0f0-151"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

