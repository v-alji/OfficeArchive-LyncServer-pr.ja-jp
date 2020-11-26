---
title: 'Lync Server 2013: ピアツーピア音声/ビデオ通話のテスト'
description: 'Lync Server 2013: ピアツーピアの音声/ビデオ通話をテストしています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing peer to peer audio/video call
ms:assetid: 95eb3693-b866-4652-bc45-9b75fdb40b49
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743835(v=OCS.15)
ms:contentKeyID: 63969627
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 03bab69d926a99c091a510ce64b78dbf505d4cbc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439815"
---
# <a name="testing-peer-to-peer-audiovideo-call-in-lync-server-2013"></a><span data-ttu-id="7d374-103">Lync Server 2013 でピアツーピア音声/ビデオ通話をテストする</span><span class="sxs-lookup"><span data-stu-id="7d374-103">Testing peer to peer audio/video call in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7d374-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7d374-104">

<span> </span></span></span>

<span data-ttu-id="7d374-105">_**最終更新日:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="7d374-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7d374-106">確認のスケジュール</span><span class="sxs-lookup"><span data-stu-id="7d374-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="7d374-107">[毎日]</span><span class="sxs-lookup"><span data-stu-id="7d374-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d374-108">テストツール</span><span class="sxs-lookup"><span data-stu-id="7d374-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="7d374-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="7d374-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d374-110">必要なアクセス許可</span><span class="sxs-lookup"><span data-stu-id="7d374-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="7d374-111">Lync Server 管理シェルを使用してローカルで実行する場合、ユーザーは RTCUniversalServerAdmins セキュリティグループのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d374-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="7d374-112">Windows PowerShell のリモートインスタンスを使って実行する場合は、Test-CsP2PAV コマンドレットを実行するためのアクセス許可を持つ RBAC の役割をユーザーに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d374-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsP2PAV cmdlet.</span></span> <span data-ttu-id="7d374-113">このコマンドレットを使うことができるすべての RBAC ロールの一覧を表示するには、Windows PowerShell プロンプトから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="7d374-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsP2PAV&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="7d374-114">説明</span><span class="sxs-lookup"><span data-stu-id="7d374-114">Description</span></span>

<span data-ttu-id="7d374-115">Test-CsP2PAV は、テストユーザーのペアがピアツーピアの A/V の会話に参加できるかどうかを判断するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7d374-115">Test-CsP2PAV is used to determine whether a pair of test users can participate in a peer-to-peer A/V conversation.</span></span> <span data-ttu-id="7d374-116">このシナリオをテストするために、このコマンドレットは、2人のユーザーを Lync Server にログオンして開始します。</span><span class="sxs-lookup"><span data-stu-id="7d374-116">To test this scenario, the cmdlet starts off by logging on the two users to Lync Server.</span></span> <span data-ttu-id="7d374-117">2つのログオンが成功すると、最初のユーザーは、A/V 呼び出しに参加するように2番目のユーザーを招待します。</span><span class="sxs-lookup"><span data-stu-id="7d374-117">Assuming that the two logons succeed, the first user then invites the second user to join an A/V call.</span></span> <span data-ttu-id="7d374-118">2人目のユーザーが通話を受け入れ、2人のユーザー間の接続がテストされた後、通話が終了し、テストユーザーがシステムからログオフされます。</span><span class="sxs-lookup"><span data-stu-id="7d374-118">The second user accepts the call, the connection between the two users is tested, and then the call is ended and the test users are logged off from the system.</span></span>

<span data-ttu-id="7d374-119">Test-CsP2PAV は、実際に A/V 通話を行いません。</span><span class="sxs-lookup"><span data-stu-id="7d374-119">Test-CsP2PAV does not actually conduct an A/V call.</span></span> <span data-ttu-id="7d374-120">マルチメディア情報は、テストユーザー間では交換されません。</span><span class="sxs-lookup"><span data-stu-id="7d374-120">Multimedia information is not exchanged between the test users.</span></span> <span data-ttu-id="7d374-121">代わりに、コマンドレットは、適切な接続を行うことができ、2人のユーザーがそのような呼び出しを実行できることを確認するだけです。</span><span class="sxs-lookup"><span data-stu-id="7d374-121">Instead, the cmdlet merely verifies that the appropriate connections can be made and that the two users can conduct such a call.</span></span>

<span data-ttu-id="7d374-122">詳細については、「 [CsP2PAV](https://docs.microsoft.com/powershell/module/skype/Test-CsP2PAV) コマンドレットのヘルプドキュメント」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7d374-122">For more information, see the Help documentation for the [Test-CsP2PAV](https://docs.microsoft.com/powershell/module/skype/Test-CsP2PAV) cmdlet.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="7d374-123">テストの実行</span><span class="sxs-lookup"><span data-stu-id="7d374-123">Running the test</span></span>

<span data-ttu-id="7d374-124">Test-CsP2PAV コマンドレットを実行するには、定義済みのテストアカウントのペア (「Lync Server テストを実行するためのテストアカウントをセットアップする」を参照) を使用するか、Lync Server を有効にしている2人のユーザーのアカウントを使用します。</span><span class="sxs-lookup"><span data-stu-id="7d374-124">The Test-CsP2PAV cmdlet can be run using either a pair of preconfigured test accounts (see Setting Up Test Accounts for Running Lync Server Tests) or the accounts of any two users who are enabled for Lync Server.</span></span> <span data-ttu-id="7d374-125">テストアカウントを使用してこの確認を実行するには、テストする Lync Server プールの FQDN を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d374-125">To run this check using test accounts, you just have to specify the FQDN of the Lync Server pool being tested.</span></span> <span data-ttu-id="7d374-126">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="7d374-126">For example:</span></span>

    Test-CsP2PAV -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="7d374-127">実際のユーザーアカウントを使用してこのチェックを実行するには、Lync Server credentials オブジェクト (アカウント名とパスワードを含むオブジェクト) をそれぞれのアカウントに作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d374-127">To run this check using actual user accounts, you must create two Lync Server credentials objects (objects that contain the account name and password) for each account.</span></span> <span data-ttu-id="7d374-128">次に、CsP2PAV を呼び出したときに、これらの資格情報オブジェクトと、2つのアカウントの SIP アドレスを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d374-128">You must then include those credentials objects and the SIP addresses of the two accounts when you call Test-CsP2PAV:</span></span>

    $credential1 = Get-Credential "litwareinc\kenmyer"
    $credential2 = Get-Credential "litwareinc\davidlongmire"
    Test-CsP2PAV -TargetFqdn "atl-cs-001.litwareinc.com" -SenderSipAddress "sip:kenmyer@litwareinc.com" -SenderCredential $credential1 -ReceiverSipAddress "sip:davidlongmire@litwareinc.com" -ReceiverCredential $credential2

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="7d374-129">成功または失敗を確認する</span><span class="sxs-lookup"><span data-stu-id="7d374-129">Determining success or failure</span></span>

<span data-ttu-id="7d374-130">2つのテストユーザーがピアツーピアの A/V の呼び出しを完了できる場合は、次のような結果として、Success とマークされた Result プロパティの出力が表示され **ます。**</span><span class="sxs-lookup"><span data-stu-id="7d374-130">If the two test users can complete a peer-to-peer A/V call, then you'll receive output similar to this with the Result property marked as **Success:**</span></span>

<span data-ttu-id="7d374-131">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="7d374-131">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="7d374-132">結果: 成功</span><span class="sxs-lookup"><span data-stu-id="7d374-132">Result : Success</span></span>

<span data-ttu-id="7d374-133">待ち時間:00:00: 06.8630376</span><span class="sxs-lookup"><span data-stu-id="7d374-133">Latency : 00:00:06.8630376</span></span>

<span data-ttu-id="7d374-134">誤差</span><span class="sxs-lookup"><span data-stu-id="7d374-134">Error :</span></span>

<span data-ttu-id="7d374-135">診断</span><span class="sxs-lookup"><span data-stu-id="7d374-135">Diagnosis :</span></span>

<span data-ttu-id="7d374-136">テストユーザーが通話を完了できなかった場合、結果は失敗として表示され、エラーと診断のプロパティに追加情報が記録されます。</span><span class="sxs-lookup"><span data-stu-id="7d374-136">If the test users can't complete the call, then the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="7d374-137">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="7d374-137">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="7d374-138">結果: エラー</span><span class="sxs-lookup"><span data-stu-id="7d374-138">Result : Failure</span></span>

<span data-ttu-id="7d374-139">待ち時間: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="7d374-139">Latency : 00:00:00</span></span>

<span data-ttu-id="7d374-140">エラー: 480、一時的に使用できません</span><span class="sxs-lookup"><span data-stu-id="7d374-140">Error : 480, Temporarily Unavailable</span></span>

<span data-ttu-id="7d374-141">診断: ErrorCode = 15030、Source = atl-litwareinc、Reason = Failed。</span><span class="sxs-lookup"><span data-stu-id="7d374-141">Diagnosis : ErrorCode=15030,Source=atl-cs-001.litwareinc.com,Reason=Failed</span></span>

<span data-ttu-id="7d374-142">Exchange Server にルーティングするには</span><span class="sxs-lookup"><span data-stu-id="7d374-142">to route to Exchange Server</span></span>

<span data-ttu-id="7d374-143">DiagnosticHeader の場合</span><span class="sxs-lookup"><span data-stu-id="7d374-143">Microsoft.Rtc.Signaling.DiagnosticHeader</span></span>

<span data-ttu-id="7d374-144">たとえば、前回の出力では、Microsoft Exchange Server に接続できなかったため、テストが失敗したことが示されます。</span><span class="sxs-lookup"><span data-stu-id="7d374-144">For example, the previous output states that the test failed because the Microsoft Exchange Server couldn't be contacted.</span></span> <span data-ttu-id="7d374-145">このエラーメッセージは、通常、Exchange ユニファイドメッセージングの構成に問題があることを示します。</span><span class="sxs-lookup"><span data-stu-id="7d374-145">This error message typically indicates a problem the configuration of Exchange Unified Messaging.</span></span>

<span data-ttu-id="7d374-146">Test-CsP2PAV が失敗した場合は、Verbose パラメーターも含めて、テストを再実行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="7d374-146">If Test-CsP2PAV fails then you might want to rerun the test, this time including the Verbose parameter:</span></span>

<span data-ttu-id="7d374-147">Test-CsP2PAV-TargetFqdn "atl-cs-001.litwareinc.com"-Verbose</span><span class="sxs-lookup"><span data-stu-id="7d374-147">Test-CsP2PAV -TargetFqdn "atl-cs-001.litwareinc.com" -Verbose</span></span>

<span data-ttu-id="7d374-148">Verbose パラメーターが含まれている場合、Test-CsP2PAV は、指定されたユーザーが Lync Server にログオンする機能をチェックしたときに実行される各操作のステップバイステップのアカウントを返します。</span><span class="sxs-lookup"><span data-stu-id="7d374-148">When the Verbose parameter is included, Test-CsP2PAV will return a step-by-step account of each action it tried as it checked the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="7d374-149">たとえば、次のような診断でテストが失敗したとします。</span><span class="sxs-lookup"><span data-stu-id="7d374-149">For example, suppose that your test failed with the following Diagnosis:</span></span>

<span data-ttu-id="7d374-150">ErrorCode = 6003、Source = atl-litwareinc、Reason = サポートされていないダイアログの要求</span><span class="sxs-lookup"><span data-stu-id="7d374-150">ErrorCode=6003,Source=atl-cs-001.litwareinc.com,Reason=Unsupported out of dialog request</span></span>

<span data-ttu-id="7d374-151">Test-CsP2PAV を再実行し、Verbose パラメーターを含めると、次のような出力が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7d374-151">If you rerun Test-CsP2PAV and include the Verbose parameter, you'll get output similar to this:</span></span>

<span data-ttu-id="7d374-152">VERBOSE: ' Register ' アクティビティが開始されました。</span><span class="sxs-lookup"><span data-stu-id="7d374-152">VERBOSE: 'Register' activity started.</span></span>

<span data-ttu-id="7d374-153">登録リクエストの送信:</span><span class="sxs-lookup"><span data-stu-id="7d374-153">Sending Registration request:</span></span>

<span data-ttu-id="7d374-154">ターゲット Fqdn = atl-cs-011.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="7d374-154">Target Fqdn = atl-cs-011.litwareinc.com</span></span>

<span data-ttu-id="7d374-155">ユーザー Sip アドレス = sip:kenmyer@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="7d374-155">User Sip Address = sip:kenmyer@litwareinc.com</span></span>

<span data-ttu-id="7d374-156">レジストラーポート = 5062。</span><span class="sxs-lookup"><span data-stu-id="7d374-156">Registrar Port = 5062.</span></span>

<span data-ttu-id="7d374-157">認証の種類 ' IWA ' が選択されています。</span><span class="sxs-lookup"><span data-stu-id="7d374-157">Auth Type 'IWA' is selected.</span></span>

<span data-ttu-id="7d374-158">"エンドポイントを登録できませんでした。" という例外が発生します。</span><span class="sxs-lookup"><span data-stu-id="7d374-158">An exception 'The endpoint was unable to register.</span></span> <span data-ttu-id="7d374-159">具体的な理由については、「エラーコード」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="7d374-159">See the ErrorCode for specific reason.'</span></span> <span data-ttu-id="7d374-160">STP2PAVWorkflow の実行中に発生したワークフローのことです。</span><span class="sxs-lookup"><span data-stu-id="7d374-160">occurred during workflow Microsoft.Rtc.SyntheticTransactions.Workflows.STP2PAVWorkflow execution.</span></span>

<span data-ttu-id="7d374-161">あまり明確でない場合もありますが、出力を慎重に確認すると、誤ったレジストラーポート (port 5062) が指定されていることがわかります。</span><span class="sxs-lookup"><span data-stu-id="7d374-161">Although it might not be immediately obvious, if you examine the output carefully you’ll see that an incorrect Registrar port (port 5062) was specified.</span></span> <span data-ttu-id="7d374-162">これにより、テストが失敗する原因となります。</span><span class="sxs-lookup"><span data-stu-id="7d374-162">In turn, that caused the test to fail.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="7d374-163">テストに失敗した可能性がある理由</span><span class="sxs-lookup"><span data-stu-id="7d374-163">Reasons why the test might have failed</span></span>

<span data-ttu-id="7d374-164">Test-CsP2PAV が失敗する可能性がある一般的な理由を次に示します。</span><span class="sxs-lookup"><span data-stu-id="7d374-164">Here are some common reasons why Test-CsP2PAV might fail:</span></span>

  - <span data-ttu-id="7d374-165">無効なユーザーアカウントが指定されました。</span><span class="sxs-lookup"><span data-stu-id="7d374-165">You specified a user account that is not valid.</span></span> <span data-ttu-id="7d374-166">次のようなコマンドを実行すると、ユーザーアカウントが存在するかどうかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="7d374-166">You can verify that a user account exists by running a command similar to this:</span></span>
    
    <span data-ttu-id="7d374-167">Get-CsUser "sip:kenmyer@litwareinc.com"</span><span class="sxs-lookup"><span data-stu-id="7d374-167">Get-CsUser "sip:kenmyer@litwareinc.com"</span></span>

  - <span data-ttu-id="7d374-168">ユーザーアカウントは有効ですが、アカウントは現在 Lync Server に対して有効になっていません。</span><span class="sxs-lookup"><span data-stu-id="7d374-168">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="7d374-169">Lync Server でユーザーアカウントが有効になっていることを確認するには、次のようなコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="7d374-169">To verify that a user account is enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="7d374-170">Enabled プロパティが False に設定されている場合は、ユーザーが現在 Lync Server を有効にしていないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="7d374-170">If the Enabled property is set to False, that means that the user is currently not enabled for Lync Server.</span></span>

<span data-ttu-id="7d374-171"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7d374-171"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

