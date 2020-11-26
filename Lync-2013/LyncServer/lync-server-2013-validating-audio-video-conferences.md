---
title: 'Lync Server 2013: 音声/ビデオ会議を検証する'
description: 'Lync Server 2013: 音声/ビデオ会議を検証しています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Validating audio/video conferences
ms:assetid: 6c8c422a-d501-42cb-820b-b002f9b2250b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720915(v=OCS.15)
ms:contentKeyID: 63969615
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ad12611e928a64b934252ec21c18b98366e0912b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443490"
---
# <a name="validating-audiovideo-conferences-in-lync-server-2013"></a><span data-ttu-id="d7db2-103">Lync Server 2013 での音声/ビデオ会議の検証</span><span class="sxs-lookup"><span data-stu-id="d7db2-103">Validating audio/video conferences in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d7db2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d7db2-104">

<span> </span></span></span>

<span data-ttu-id="d7db2-105">_**最終更新日:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="d7db2-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7db2-106">確認のスケジュール</span><span class="sxs-lookup"><span data-stu-id="d7db2-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="d7db2-107">[毎日]</span><span class="sxs-lookup"><span data-stu-id="d7db2-107">Daily</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7db2-108">テストツール</span><span class="sxs-lookup"><span data-stu-id="d7db2-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="d7db2-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="d7db2-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7db2-110">必要なアクセス許可</span><span class="sxs-lookup"><span data-stu-id="d7db2-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="d7db2-111">Lync Server 管理シェルを使用してローカルで実行する場合、ユーザーは RTCUniversalServerAdmins セキュリティグループのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="d7db2-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="d7db2-112">Windows PowerShell のリモートインスタンスを使って実行する場合は、Test-CsAVConference コマンドレットを実行するためのアクセス許可を持つ RBAC の役割をユーザーに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="d7db2-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsAVConference cmdlet.</span></span> <span data-ttu-id="d7db2-113">このコマンドレットを使うことができるすべての RBAC ロールの一覧を表示するには、Windows PowerShell プロンプトから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="d7db2-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsAVConference&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="d7db2-114">説明</span><span class="sxs-lookup"><span data-stu-id="d7db2-114">Description</span></span>

<span data-ttu-id="d7db2-115">Test-CsAVConference コマンドレットは、2つのテストユーザーが音声/ビデオ (A/V) 会議に参加できるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="d7db2-115">The Test-CsAVConference cmdlet checks whether two test users can participate in an audio/video (A/V) conference.</span></span> <span data-ttu-id="d7db2-116">コマンドレットが実行されると、2人のユーザーがシステムにログオンします。</span><span class="sxs-lookup"><span data-stu-id="d7db2-116">When the cmdlet runs, the two users are logged on to the system.</span></span> <span data-ttu-id="d7db2-117">ログオンが正常に完了したら、最初のユーザーは A/V 会議を作成し、2人目のユーザーがその会議に参加するのを待ちます。</span><span class="sxs-lookup"><span data-stu-id="d7db2-117">After they face successfully logged on, the first user creates an A/V conference, and then waits for the second user to join that conference.</span></span> <span data-ttu-id="d7db2-118">データを簡単に交換した後、会議が削除され、2つのテストユーザーがログオフします。</span><span class="sxs-lookup"><span data-stu-id="d7db2-118">After a brief exchange of data, the conference is deleted and the two tests users are logged off.</span></span>

<span data-ttu-id="d7db2-119">Test-CsAVConference は、2つのテストユーザー間で実際の A/V 会議を実行しないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="d7db2-119">Note that Test-CsAVConference does not conduct an actual A/V conference between the two test users.</span></span> <span data-ttu-id="d7db2-120">代わりに、このコマンドレットは、2人のユーザーが会議の開催に必要なすべての接続を確立できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d7db2-120">Instead, the cmdlet verifies that the two users can make all the connections necessary to conduct such a conference.</span></span>

<span data-ttu-id="d7db2-121">このコマンドのその他の例については、「テスト用の [CsAVConference 会議](https://docs.microsoft.com/powershell/module/skype/Test-CsAVConference)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d7db2-121">Further examples for this command can be found at [Test-CsAVConference](https://docs.microsoft.com/powershell/module/skype/Test-CsAVConference).</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="d7db2-122">テストの実行</span><span class="sxs-lookup"><span data-stu-id="d7db2-122">Running the test</span></span>

<span data-ttu-id="d7db2-123">Test-CsAVConference コマンドレットを実行するには、定義済みのテストアカウントのペア (「Lync Server テストを実行するためのテストアカウントをセットアップする」を参照) を使用するか、Lync Server を有効にしている2人のユーザーのアカウントを使用します。</span><span class="sxs-lookup"><span data-stu-id="d7db2-123">The Test-CsAVConference cmdlet can be run using either a pair of preconfigured test accounts (see Setting Up Test Accounts for Running Lync Server Tests) or the accounts of any two users who are enabled for Lync Server.</span></span> <span data-ttu-id="d7db2-124">テストアカウントを使用してこの確認を実行するには、テストする Lync Server プールの FQDN を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d7db2-124">To run this check using test accounts, you just have to specify the FQDN of the Lync Server pool being tested.</span></span> <span data-ttu-id="d7db2-125">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="d7db2-125">For example:</span></span>

    Test-CsAVConference -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="d7db2-126">実際のユーザーアカウントを使用してこのチェックを実行するには、2つの Windows PowerShell credentials オブジェクト (アカウント名とパスワードを含むオブジェクト) を各アカウントに作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d7db2-126">To run this check using actual user accounts, you must create two Windows PowerShell credentials objects (objects that contain the account name and password) for each account.</span></span> <span data-ttu-id="d7db2-127">次に、これらの資格情報オブジェクトと、テスト用 Cgi 会議を呼び出すときに2つのアカウントの SIP アドレスを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="d7db2-127">You must then include those credentials objects and the SIP addresses of the two accounts when they call Test-CsAVConference:</span></span>

    $credential1 = Get-Credential "litwareinc\kenmyer"
    $credential2 = Get-Credential "litwareinc\davidlongmire"
    Test-CsAVConference -TargetFqdn "atl-cs-001.litwareinc.com" -SenderSipAddress "sip:kenmyer@litwareinc.com" -SenderCredential $credential1 -ReceiverSipAddress "sip:davidlongmire@litwareinc.com" -ReceiverCredential $credential2

<span data-ttu-id="d7db2-128">詳細については、「 [テスト-CsAVConference](https://docs.microsoft.com/powershell/module/skype/Test-CsAVConference) コマンドレットのヘルプドキュメント」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d7db2-128">For more information, see the Help documentation for the [Test-CsAVConference](https://docs.microsoft.com/powershell/module/skype/Test-CsAVConference) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="d7db2-129">成功または失敗を確認する</span><span class="sxs-lookup"><span data-stu-id="d7db2-129">Determining Success or Failure</span></span>

<span data-ttu-id="d7db2-130">指定したユーザーが A/V 会議を正常に完了できた場合は、次のような結果が返され、Result プロパティは Success とマークされ **ます。**</span><span class="sxs-lookup"><span data-stu-id="d7db2-130">If the specified users can successfully complete an A/V conference, you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="d7db2-131">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="d7db2-131">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="d7db2-132">結果: 成功</span><span class="sxs-lookup"><span data-stu-id="d7db2-132">Result : Success</span></span>

<span data-ttu-id="d7db2-133">待ち時間:00:00: 02.6841765</span><span class="sxs-lookup"><span data-stu-id="d7db2-133">Latency : 00:00:02.6841765</span></span>

<span data-ttu-id="d7db2-134">誤差</span><span class="sxs-lookup"><span data-stu-id="d7db2-134">Error :</span></span>

<span data-ttu-id="d7db2-135">診断</span><span class="sxs-lookup"><span data-stu-id="d7db2-135">Diagnosis :</span></span>

<span data-ttu-id="d7db2-136">ユーザーが会議を完了できなかった場合は、結果がエラーとして表示され、エラーと診断のプロパティに追加情報が記録されます。</span><span class="sxs-lookup"><span data-stu-id="d7db2-136">If the users can not complete the conference, then the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="d7db2-137">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="d7db2-137">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="d7db2-138">結果: エラー</span><span class="sxs-lookup"><span data-stu-id="d7db2-138">Result : Failure</span></span>

<span data-ttu-id="d7db2-139">待ち時間: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="d7db2-139">Latency : 00:00:00</span></span>

<span data-ttu-id="d7db2-140">エラー: 404、見つかりません</span><span class="sxs-lookup"><span data-stu-id="d7db2-140">Error : 404, Not Found</span></span>

<span data-ttu-id="d7db2-141">診断: ErrorCode = 4005、Source = atl-cs-001.litwareinc.com、</span><span class="sxs-lookup"><span data-stu-id="d7db2-141">Diagnosis : ErrorCode=4005,Source=atl-cs-001.litwareinc.com,</span></span>

<span data-ttu-id="d7db2-142">理由 = ターゲット URI が SIP で有効になっていないか、</span><span class="sxs-lookup"><span data-stu-id="d7db2-142">Reason=Destination URI either not enabled for SIP or does not</span></span>

<span data-ttu-id="d7db2-143">残っ.</span><span class="sxs-lookup"><span data-stu-id="d7db2-143">exist.</span></span>

<span data-ttu-id="d7db2-144">DiagnosticHeader の場合</span><span class="sxs-lookup"><span data-stu-id="d7db2-144">Microsoft.Rtc.Signaling.DiagnosticHeader</span></span>

<span data-ttu-id="d7db2-145">たとえば、前回の出力には、アカウントが存在しないか、アカウントが Lync Server に対して有効になっていないために、2つ以上のユーザーアカウントが無効であったためにテストが失敗したことが示されます。</span><span class="sxs-lookup"><span data-stu-id="d7db2-145">For example, the previous output states that the test failed because at least one of the two user accounts was not valid, either because the account does not exist or because the account has not been enabled for Lync Server.</span></span> <span data-ttu-id="d7db2-146">次のようなコマンドを実行することにより、2つのテストアカウントが存在するかどうか、および Lync Server 用に有効になっているかどうかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="d7db2-146">You can verify the existence of the two test accounts, and whether they were enabled for Lync Server, by running a command similar to the following:</span></span>

    "sip:kenmyer@litwareinc.com","sip:davidlongmire@litwareinc.com" | Get-CsUser | Select-Object SipAddress, enabled

<span data-ttu-id="d7db2-147">Test-CsAVConference が失敗した場合は、Verbose パラメーターも含めて、テストを再実行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d7db2-147">If Test-CsAVConference fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsAVConference -TargetFqdn "atl-cs-001.litwareinc.com" -Verbose

<span data-ttu-id="d7db2-148">Verbose パラメーターが含まれている場合 Test-CsAVConference は、指定されたユーザーが AV 会議に参加できるかどうかをチェックしたときに実行される各操作のステップバイステップのアカウントを返します。</span><span class="sxs-lookup"><span data-stu-id="d7db2-148">When the Verbose parameter is included Test-CsAVConference will return a step-by-step account of each action it tried when it checked the ability of the specified users to participate in an AV conference.</span></span> <span data-ttu-id="d7db2-149">たとえば、テストが失敗し、次のような診断が表示されたとします。</span><span class="sxs-lookup"><span data-stu-id="d7db2-149">For example, suppose that your test fails and you receive the following Diagnosis:</span></span>

<span data-ttu-id="d7db2-150">ErrorCode = 1008、Source = accessproxy、Reason = DNS SRV レコードを解決できませんでした</span><span class="sxs-lookup"><span data-stu-id="d7db2-150">ErrorCode=1008,Source=accessproxy.litwareinc.com,Reason=Unable to resolve DNS SRV record</span></span>

<span data-ttu-id="d7db2-151">Verbose パラメーターを使用してテストを再実行する場合、返される手順ごとの情報には、次のような出力が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d7db2-151">If you rerun the test using the Verbose parameter, the step-by-step information returned will include output similar to this:</span></span>

<span data-ttu-id="d7db2-152">VERBOSE: ' Register ' アクティビティが開始されました。</span><span class="sxs-lookup"><span data-stu-id="d7db2-152">VERBOSE: 'Register' activity started.</span></span>

<span data-ttu-id="d7db2-153">登録リクエストの送信:</span><span class="sxs-lookup"><span data-stu-id="d7db2-153">Sending Registration request:</span></span>

<span data-ttu-id="d7db2-154">ターゲット Fqdn = atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="d7db2-154">Target Fqdn = atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="d7db2-155">ユーザー Sip アドレス = sip:davidlongmire@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="d7db2-155">User Sip Address = sip:davidlongmire@litwareinc.com</span></span>

<span data-ttu-id="d7db2-156">レジストラーポート = 5061。</span><span class="sxs-lookup"><span data-stu-id="d7db2-156">Registrar Port = 5061.</span></span>

<span data-ttu-id="d7db2-157">[Authentication Type ' Trusted '] が選択されています。</span><span class="sxs-lookup"><span data-stu-id="d7db2-157">Auth Type 'Trusted' is selected.</span></span>

<span data-ttu-id="d7db2-158">' Register ' アクティビティが開始されました。</span><span class="sxs-lookup"><span data-stu-id="d7db2-158">'Register' activity started.</span></span>

<span data-ttu-id="d7db2-159">登録リクエストの送信:</span><span class="sxs-lookup"><span data-stu-id="d7db2-159">Sending Registration request:</span></span>

<span data-ttu-id="d7db2-160">ターゲット Fqdn = atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="d7db2-160">Target Fqdn = atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="d7db2-161">ユーザー Sip アドレス = sip:kenmyer@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="d7db2-161">User Sip Address = sip:kenmyer@litwareinc.com</span></span>

<span data-ttu-id="d7db2-162">レジストラーポート = 5061。</span><span class="sxs-lookup"><span data-stu-id="d7db2-162">Registrar Port = 5061.</span></span>

<span data-ttu-id="d7db2-163">[Authentication Type ' Trusted '] が選択されています。</span><span class="sxs-lookup"><span data-stu-id="d7db2-163">Auth Type 'Trusted' is selected.</span></span>

<span data-ttu-id="d7db2-164">"エンドポイントを登録できませんでした。" という例外が発生します。</span><span class="sxs-lookup"><span data-stu-id="d7db2-164">An exception 'The endpoint was unable to register.</span></span> <span data-ttu-id="d7db2-165">具体的な理由については、「エラーコード」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="d7db2-165">See the ErrorCode for specific reason.'</span></span> <span data-ttu-id="d7db2-166">ワークフローの実行中に発生</span><span class="sxs-lookup"><span data-stu-id="d7db2-166">occurred during Workflow</span></span>

<span data-ttu-id="d7db2-167">この出力の最後の行は、ユーザー sip:kenmyer@litwareinc.com が Lync Server に登録できなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="d7db2-167">The last line in that output indicates that the user sip:kenmyer@litwareinc.com was unable to register with Lync Server.</span></span> <span data-ttu-id="d7db2-168">つまり、SIP アドレス sip:kenmyer@litwareinc.com が有効であること、および関連付けられたユーザーが Lync Server に対して有効になっていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d7db2-168">That means that you should verify that the SIP address sip:kenmyer@litwareinc.com is valid, and that the associated user is enabled for Lync Server.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="d7db2-169">テストに失敗した可能性がある理由</span><span class="sxs-lookup"><span data-stu-id="d7db2-169">Reasons why the test might have failed</span></span>

<span data-ttu-id="d7db2-170">Test-CsAVConference が失敗する可能性がある一般的な理由を次に示します。</span><span class="sxs-lookup"><span data-stu-id="d7db2-170">Here are some common reasons why Test-CsAVConference might fail:</span></span>

  - <span data-ttu-id="d7db2-171">無効なユーザーアカウントが指定されました。</span><span class="sxs-lookup"><span data-stu-id="d7db2-171">You specified a user account that is not valid.</span></span> <span data-ttu-id="d7db2-172">次のようなコマンドを実行すると、ユーザーアカウントが存在するかどうかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="d7db2-172">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="d7db2-173">ユーザーアカウントは有効ですが、アカウントは現在 Lync Server に対して有効になっていません。</span><span class="sxs-lookup"><span data-stu-id="d7db2-173">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="d7db2-174">Lync Server でユーザーアカウントが有効になっていることを確認するには、次のようなコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="d7db2-174">To verify that a user account is enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="d7db2-175">Enabled プロパティが False に設定されている場合は、ユーザーが現在 Lync Server を有効にしていないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="d7db2-175">If the Enabled property is set to False that means that the user is currently not enabled for Lync Server.</span></span>

<span data-ttu-id="d7db2-176"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d7db2-176"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

