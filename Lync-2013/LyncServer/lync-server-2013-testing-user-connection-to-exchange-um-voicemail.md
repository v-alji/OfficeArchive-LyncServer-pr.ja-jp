---
title: 'Lync Server 2013: Exchange UM ボイスメールへのユーザー接続のテスト'
description: 'Lync Server 2013: Exchange UM ボイスメールへのユーザー接続をテストしています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing user connection to Exchange UM voicemail
ms:assetid: 574da104-8823-4061-9fb6-353639f1884d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727305(v=OCS.15)
ms:contentKeyID: 63969604
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b887b5b0df02a5864e0a39f2b62893d20105a86a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439715"
---
# <a name="testing-user-connection-to-exchange-um-voicemail-in-lync-server-2013"></a><span data-ttu-id="e2a97-103">Lync Server 2013 での Exchange UM ボイスメールへのユーザー接続のテスト</span><span class="sxs-lookup"><span data-stu-id="e2a97-103">Testing user connection to Exchange UM voicemail in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e2a97-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e2a97-104">

<span> </span></span></span>

<span data-ttu-id="e2a97-105">_**最終更新日:** 2014-11-01_</span><span class="sxs-lookup"><span data-stu-id="e2a97-105">_**Topic Last Modified:** 2014-11-01_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e2a97-106">確認のスケジュール</span><span class="sxs-lookup"><span data-stu-id="e2a97-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="e2a97-107">[毎日]</span><span class="sxs-lookup"><span data-stu-id="e2a97-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2a97-108">テストツール</span><span class="sxs-lookup"><span data-stu-id="e2a97-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="e2a97-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="e2a97-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2a97-110">必要なアクセス許可</span><span class="sxs-lookup"><span data-stu-id="e2a97-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="e2a97-111">Lync Server 管理シェルを使用してローカルで実行する場合、ユーザーは RTCUniversalServerAdmins セキュリティグループのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="e2a97-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="e2a97-112">Windows PowerShell のリモートインスタンスを使って実行する場合は、 <strong>テスト-CsExUMVoiceMail メール</strong> コマンドレットを実行する権限を持つ RBAC の役割をユーザーに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="e2a97-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsExUMVoiceMail</strong> cmdlet.</span></span> <span data-ttu-id="e2a97-113">このコマンドレットを使うことができるすべての RBAC ロールの一覧を表示するには、Windows PowerShell プロンプトから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="e2a97-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsExUMVoiceMail&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="e2a97-114">説明</span><span class="sxs-lookup"><span data-stu-id="e2a97-114">Description</span></span>

<span data-ttu-id="e2a97-115">**テスト-CsExUMVoiceMail メール** コマンドレットを使用すると、管理者は、ユーザーが Microsoft Exchange Server 2013 ユニファイドメッセージングサービスにアクセスして使用できることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="e2a97-115">The **Test-CsExUMVoiceMail** cmdlet enables administrators to verify that a user can access and use the Microsoft Exchange Server 2013 unified messaging service.</span></span> <span data-ttu-id="e2a97-116">これを行うために、コマンドレットはユニファイドメッセージングサービスに接続し、指定されたメールボックスにボイスメールを残します。</span><span class="sxs-lookup"><span data-stu-id="e2a97-116">To do this, the cmdlet connects to the unified messaging service and leaves a voice mail in the specified mailbox.</span></span> <span data-ttu-id="e2a97-117">これは、システムによって提供されるボイスメールの場合もあれば、カスタムの場合もあります。自分で録音した WAV ファイル。</span><span class="sxs-lookup"><span data-stu-id="e2a97-117">This can be a system-supplied voice mail, or it can be a custom .WAV file that you have recorded yourself.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="e2a97-118">テストの実行</span><span class="sxs-lookup"><span data-stu-id="e2a97-118">Running the test</span></span>

<span data-ttu-id="e2a97-119">次の例では、プール atl-cs-001.litwareinc.com の Exchange ユニファイドメッセージングのボイスメール接続をテストします。</span><span class="sxs-lookup"><span data-stu-id="e2a97-119">The following example tests Exchange Unified Messaging voice mail connectivity for the pool atl-cs-001.litwareinc.com.</span></span> <span data-ttu-id="e2a97-120">このコマンドは、テストユーザーがプール atl-cs-001.litwareinc.com に対して定義されている場合にのみ機能します。</span><span class="sxs-lookup"><span data-stu-id="e2a97-120">This command will work only if test users were defined for the pool atl-cs-001.litwareinc.com.</span></span> <span data-ttu-id="e2a97-121">その場合、コマンドは、最初のテストユーザーがユニファイドメッセージングボイスメールを使用できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="e2a97-121">If they have, then the command will determine whether the first test user can use Unified Messaging voice mail.</span></span> <span data-ttu-id="e2a97-122">プールのテストユーザーが構成されていない場合、コマンドは失敗します。</span><span class="sxs-lookup"><span data-stu-id="e2a97-122">If test users were not configured for the pool then the command will fail.</span></span>

    Test-CsExUMVoiceMail -TargetFqdn "atl-cs-001.litwareinc.com" -ReceiverSipAddress "sip:kenmyer@litwareinc.com" 

<span data-ttu-id="e2a97-123">次の例に示すコマンドは、ユーザー litwareinc kenmyer の Exchange ユニファイドメッセージングのボイスメール接続のテスト \\ です。</span><span class="sxs-lookup"><span data-stu-id="e2a97-123">The commands shown in the next example test Exchange Unified Messaging voice mail connectivity for the user litwareinc\\kenmyer.</span></span> <span data-ttu-id="e2a97-124">これを行うには、この例の最初のコマンドでは、 **Credential** コマンドレットを使って、user litwareinc Kenmyer の Windows PowerShell コマンドラインインターフェイスの credentials オブジェクトを作成し \\ ます。</span><span class="sxs-lookup"><span data-stu-id="e2a97-124">To do this, the first command in the example uses the **Get-Credential** cmdlet to create a Windows PowerShell command-line interface credentials object for the user litwareinc\\kenmyer.</span></span> <span data-ttu-id="e2a97-125">このアカウントのパスワードを入力して、有効な資格情報オブジェクトを作成し、 **テスト用の CsExUMVoiceMail メール** コマンドレットでチェックを実行できるようにする必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="e2a97-125">Note that you must supply the password for this account to create a valid credentials object and to ensure that the **Test-CsExUMVoiceMail** cmdlet can run its check.</span></span>

<span data-ttu-id="e2a97-126">この例の2番目のコマンドでは、指定された資格情報オブジェクト ($x) とユーザー litwareinc kenmyer の SIP アドレスを使って、 \\ Exchange ユニファイドメッセージングボイスメールに接続できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="e2a97-126">The second command in the example uses the supplied credentials object ($x) and the SIP address of the user litwareinc\\kenmyer to determine whether or this user can connect to Exchange Unified Messaging voice mail.</span></span>

    $credential = Get-Credential "litwareinc\pilar" 
    
    Test-CsExUMVoiceMail -TargetFqdn "atl-cs-001.litwareinc.com" -ReceiverSipAddress "sip:kenmyer@litwareinc.com" -SenderSipAddress "sip:pilar@litwareinc.com" -SenderCredential $credential 

<span data-ttu-id="e2a97-127">次の例に示すコマンドは、例1に示すコマンドの変形です。この例では、OutLoggerVariable パラメーターが含まれており、 **テスト-CsExUMVoiceMail メール** レットによって実行されたすべての手順の詳細なログを生成し、それらの各手順の成功または失敗を生成します。</span><span class="sxs-lookup"><span data-stu-id="e2a97-127">The command shown in the next example is a variation of the command shown in Example 1; in this case, the OutLoggerVariable parameter is included to generate a detailed log of every step done by the **Test-CsExUMVoiceMail** cmdletand the success or failure of each of those steps.</span></span> <span data-ttu-id="e2a97-128">これを行うには、パラメーター値 ExumText と共に OutLoggerVariable パラメーターを追加します。これにより、詳細なログ情報が $ExumTest という名前の変数に格納されます。</span><span class="sxs-lookup"><span data-stu-id="e2a97-128">To do this, the OutLoggerVariable parameter is added alongside the parameter value ExumText; that causes detailed logging information to be stored in a variable named $ExumTest.</span></span> <span data-ttu-id="e2a97-129">この例の最後のコマンドでは、ToXML () メソッドを使ってログ情報を XML 形式に変換しています。</span><span class="sxs-lookup"><span data-stu-id="e2a97-129">In the final command in the example, the ToXML() method is used to convert the log information to XML format.</span></span> <span data-ttu-id="e2a97-130">その XML データは、 \\ \\ Out-File コマンドレットを使用して、VoicemailTest.xml、C: Logs という名前のファイルに書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="e2a97-130">That XML data is then written to a file that is named C:\\Logs\\VoicemailTest.xml by using the Out-File cmdlet.</span></span>

    Test-CsExUMVoiceMail -TargetFqdn "atl-cs-001.litwareinc.com" -ReceiverSipAddress "sip:kenmyer@litwareinc.com" -OutLoggerVariable VoicemailTest 
     
    $VoicemailTest.ToXML() | Out-File C:\Logs\VoicemailTest.xml

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="e2a97-131">成功または失敗を確認する</span><span class="sxs-lookup"><span data-stu-id="e2a97-131">Determining success or failure</span></span>

<span data-ttu-id="e2a97-132">Exchange の統合が適切に構成されている場合は、次のような結果が返され、Result プロパティは **Success** とマークされます。</span><span class="sxs-lookup"><span data-stu-id="e2a97-132">If Exchange integration is correctly configured, you'll receive output similar to this, with the Result property marked as **Success**:</span></span>

<span data-ttu-id="e2a97-133">ターゲット Fqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="e2a97-133">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="e2a97-134">結果: 成功</span><span class="sxs-lookup"><span data-stu-id="e2a97-134">Result : Success</span></span>

<span data-ttu-id="e2a97-135">待ち時間:00:00: 02.9911345</span><span class="sxs-lookup"><span data-stu-id="e2a97-135">Latency : 00:00:02.9911345</span></span>

<span data-ttu-id="e2a97-136">エラーメッセージ:</span><span class="sxs-lookup"><span data-stu-id="e2a97-136">Error Message :</span></span>

<span data-ttu-id="e2a97-137">診断</span><span class="sxs-lookup"><span data-stu-id="e2a97-137">Diagnosis :</span></span>

<span data-ttu-id="e2a97-138">指定したユーザーがボイスメールに接続できない場合、結果はエラーとして表示さ **れ、エラー** と診断のプロパティに追加情報が記録されます。</span><span class="sxs-lookup"><span data-stu-id="e2a97-138">If the specified user can't connect to voicemail, the Result will be shown as **Failure**, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="e2a97-139">警告: 指定した完全修飾のレジストラーポート番号の読み取りに失敗しました</span><span class="sxs-lookup"><span data-stu-id="e2a97-139">WARNING: Failed to read Registrar port number for the given fully qualified</span></span>

<span data-ttu-id="e2a97-140">ドメイン名 (FQDN)。</span><span class="sxs-lookup"><span data-stu-id="e2a97-140">domain name (FQDN).</span></span> <span data-ttu-id="e2a97-141">既定のレジストラーポート番号を使用します。</span><span class="sxs-lookup"><span data-stu-id="e2a97-141">Using default Registrar port number.</span></span> <span data-ttu-id="e2a97-142">エラー</span><span class="sxs-lookup"><span data-stu-id="e2a97-142">Exception:</span></span>

<span data-ttu-id="e2a97-143">InvalidOperationException: トポロジで一致するクラスターが見つかりませんでした。</span><span class="sxs-lookup"><span data-stu-id="e2a97-143">System.InvalidOperationException: No matching cluster found in topology.</span></span>

<span data-ttu-id="e2a97-144">自宅</span><span class="sxs-lookup"><span data-stu-id="e2a97-144">at</span></span>

<span data-ttu-id="e2a97-145">SipSyntheticTransaction-TryRetri の同期を行います。</span><span class="sxs-lookup"><span data-stu-id="e2a97-145">Microsoft.Rtc.Management.SyntheticTransactions.SipSyntheticTransaction.TryRetri</span></span>

<span data-ttu-id="e2a97-146">eveRegistrarPortFromTopology (Int32& registrarPortNumber)</span><span class="sxs-lookup"><span data-stu-id="e2a97-146">eveRegistrarPortFromTopology(Int32& registrarPortNumber)</span></span>

<span data-ttu-id="e2a97-147">ターゲット Fqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="e2a97-147">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="e2a97-148">結果: エラー</span><span class="sxs-lookup"><span data-stu-id="e2a97-148">Result : Failure</span></span>

<span data-ttu-id="e2a97-149">待ち時間: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="e2a97-149">Latency : 00:00:00</span></span>

<span data-ttu-id="e2a97-150">エラーメッセージ: 10060、接続されているパーティのため、接続に失敗しました</span><span class="sxs-lookup"><span data-stu-id="e2a97-150">Error Message : 10060, A connection attempt failed because the connected party</span></span>

<span data-ttu-id="e2a97-151">一定の期間が経過した後に正しく応答しなかった場合、または</span><span class="sxs-lookup"><span data-stu-id="e2a97-151">did not properly respond after a period of time, or</span></span>

<span data-ttu-id="e2a97-152">接続されているホストに、接続に失敗しました</span><span class="sxs-lookup"><span data-stu-id="e2a97-152">established connection failed because connected host has</span></span>

<span data-ttu-id="e2a97-153">10.188.116.96 に応答できませんでした: 5061</span><span class="sxs-lookup"><span data-stu-id="e2a97-153">failed to respond 10.188.116.96:5061</span></span>

<span data-ttu-id="e2a97-154">内部例外: 接続の試行が失敗したため、接続できませんでした。</span><span class="sxs-lookup"><span data-stu-id="e2a97-154">Inner Exception:A connection attempt failed because the</span></span>

<span data-ttu-id="e2a97-155">しばらくしても、接続されているパーティが正しく応答しませんでした</span><span class="sxs-lookup"><span data-stu-id="e2a97-155">connected party did not properly respond after a period of</span></span>

<span data-ttu-id="e2a97-156">接続されているホストが原因で、時刻、または接続に失敗しました</span><span class="sxs-lookup"><span data-stu-id="e2a97-156">time, or established connection failed because connected host</span></span>

<span data-ttu-id="e2a97-157">さんが10.188.116.96 に応答できませんでした: 5061</span><span class="sxs-lookup"><span data-stu-id="e2a97-157">has failed to respond 10.188.116.96:5061</span></span>

<span data-ttu-id="e2a97-158">診断</span><span class="sxs-lookup"><span data-stu-id="e2a97-158">Diagnosis :</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="e2a97-159">テストに失敗した可能性がある理由</span><span class="sxs-lookup"><span data-stu-id="e2a97-159">Reasons why the test might have failed</span></span>

<span data-ttu-id="e2a97-160">次に **、テスト-CsExUMVoiceMail メール** が失敗する理由をいくつか示します。</span><span class="sxs-lookup"><span data-stu-id="e2a97-160">Here are some common reasons why **Test-CsExUMVoiceMail** might fail:</span></span>

  - <span data-ttu-id="e2a97-161">指定されたパラメーター値が正しくありません。</span><span class="sxs-lookup"><span data-stu-id="e2a97-161">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="e2a97-162">使用する場合は、オプションのパラメーターが正しく構成されている必要があります。または、テストが失敗します。</span><span class="sxs-lookup"><span data-stu-id="e2a97-162">If used, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="e2a97-163">省略可能なパラメーターを指定せずにコマンドを再実行し、それが成功するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="e2a97-163">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

  - <span data-ttu-id="e2a97-164">このコマンドは、Exchange サーバーが正しく構成されていないか、まだ展開されていない場合に失敗します。</span><span class="sxs-lookup"><span data-stu-id="e2a97-164">This command will fail if the Exchange Server is misconfigured or not yet deployed.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="e2a97-165">関連項目</span><span class="sxs-lookup"><span data-stu-id="e2a97-165">See Also</span></span>


[<span data-ttu-id="e2a97-166">Test-CsExUMConnectivity</span><span class="sxs-lookup"><span data-stu-id="e2a97-166">Test-CsExUMConnectivity</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsExUMConnectivity)  
  

<span data-ttu-id="e2a97-167"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e2a97-167"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

