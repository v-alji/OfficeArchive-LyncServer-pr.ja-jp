---
title: 'Lync Server 2013: グループ IM の実行機能をテストしています'
description: 'Lync Server 2013: グループ IM の実行機能をテストしています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing ability to do group IM
ms:assetid: ca5545bc-51ac-490f-b96b-917bb742ad04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743839(v=OCS.15)
ms:contentKeyID: 63969652
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f6988a0c1a7ba569f7b4da098ae741beab5e14fa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441103"
---
# <a name="testing-ability-to-do-group-im-in-lync-server-2013"></a><span data-ttu-id="6c03a-103">Lync Server 2013 でグループ IM を実行するためのテスト機能</span><span class="sxs-lookup"><span data-stu-id="6c03a-103">Testing ability to do group IM in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6c03a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6c03a-104">

<span> </span></span></span>

<span data-ttu-id="6c03a-105">_**最終更新日:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="6c03a-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c03a-106">確認のスケジュール</span><span class="sxs-lookup"><span data-stu-id="6c03a-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="6c03a-107">[毎日]</span><span class="sxs-lookup"><span data-stu-id="6c03a-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c03a-108">テストツール</span><span class="sxs-lookup"><span data-stu-id="6c03a-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="6c03a-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="6c03a-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c03a-110">必要なアクセス許可</span><span class="sxs-lookup"><span data-stu-id="6c03a-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="6c03a-111">Lync Server 管理シェルを使用してローカルで実行する場合、ユーザーは RTCUniversalServerAdmins セキュリティグループのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c03a-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="6c03a-112">Windows PowerShell のリモートインスタンスを使って実行する場合は、Test-CsGroupIM コマンドレットを実行するためのアクセス許可を持つ RBAC の役割をユーザーに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c03a-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsGroupIM cmdlet.</span></span> <span data-ttu-id="6c03a-113">このコマンドレットを使うことができるすべての RBAC ロールの一覧を表示するには、Windows PowerShell プロンプトから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="6c03a-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsGroupIM&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="6c03a-114">説明</span><span class="sxs-lookup"><span data-stu-id="6c03a-114">Description</span></span>

<span data-ttu-id="6c03a-115">Test-CsGroupIM コマンドレットは、組織内のユーザーがグループのインスタントメッセージングセッションを実施できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6c03a-115">The Test-CsGroupIM cmdlet verifies that users in your organization can conduct group instant messaging sessions.</span></span> <span data-ttu-id="6c03a-116">テスト用の CsGroupIM を実行すると、コマンドレットによって、テストユーザーのペアを Lync Server にサインインしようとします。</span><span class="sxs-lookup"><span data-stu-id="6c03a-116">When you run Test-CsGroupIM, the cmdlet attempts to sign in a pair of test users to Lync Server.</span></span> <span data-ttu-id="6c03a-117">成功した場合、Test-CsGroupIM は最初のテストユーザーを使用して新しい会議を作成し、その後、2人目のユーザーを会議に参加するように招待します。</span><span class="sxs-lookup"><span data-stu-id="6c03a-117">If successful, Test-CsGroupIM creates a new conference using the first test user, then invites the second user to join the conference.</span></span> <span data-ttu-id="6c03a-118">メッセージの交換後、両方のユーザーがシステムから切断されます。</span><span class="sxs-lookup"><span data-stu-id="6c03a-118">After an exchange of messages, both users are then disconnected from the system.</span></span> <span data-ttu-id="6c03a-119">これは、ユーザーの操作なしで、実際のユーザーには影響を与えずに行われることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="6c03a-119">Note that all of this happens without any user interaction, and without affecting any actual users.</span></span> <span data-ttu-id="6c03a-120">たとえば、テストアカウント sip:kenmyer@litwareinc.com は、実際の Lync Server アカウントを持っている実際のユーザーに対応しているものとします。</span><span class="sxs-lookup"><span data-stu-id="6c03a-120">For example, suppose that the test account sip:kenmyer@litwareinc.com corresponds to a real user who has a real Lync Server account.</span></span> <span data-ttu-id="6c03a-121">その場合は、実際の Ken Myer を中断することなく、テストが行われます。</span><span class="sxs-lookup"><span data-stu-id="6c03a-121">In that case, the test will be conducted without any disruption to the real Ken Myer.</span></span> <span data-ttu-id="6c03a-122">たとえば、Ken Myer のテストアカウントがシステムからログオフした場合でも、Ken Myer はログイン状態を維持します。</span><span class="sxs-lookup"><span data-stu-id="6c03a-122">For example, even when the Ken Myer test account logs off from the system, Ken Myer the person will remain logged on.</span></span> <span data-ttu-id="6c03a-123">同様に、本物の Ken Myer は電話会議に参加するための招待状を受け取りません。</span><span class="sxs-lookup"><span data-stu-id="6c03a-123">Likewise, the real Ken Myer won't receive an invitation to join the conference.</span></span> <span data-ttu-id="6c03a-124">この招待状は、テストアカウントに送信され、承認されます。</span><span class="sxs-lookup"><span data-stu-id="6c03a-124">That invitation will be sent to, and accepted by, the test account.</span></span>

<span data-ttu-id="6c03a-125">詳細については、「 [テスト-CsGroupIM](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupIM) コマンドレットのヘルプドキュメント」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6c03a-125">For more information, see the Help documentation for the [Test-CsGroupIM](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupIM) cmdlet.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="6c03a-126">テストの実行</span><span class="sxs-lookup"><span data-stu-id="6c03a-126">Running the test</span></span>

<span data-ttu-id="6c03a-127">Test-CsGroupIM コマンドレットを実行するには、定義済みのテストアカウントのペア (「Lync Server テストを実行するためのテストアカウントをセットアップする」を参照) を使用するか、Lync Server を有効にしている2人のユーザーのアカウントを使用します。</span><span class="sxs-lookup"><span data-stu-id="6c03a-127">The Test-CsGroupIM cmdlet can be run using either a pair of preconfigured test accounts (see Setting Up Test Accounts for Running Lync Server Tests) or the accounts of any two users who are enabled for Lync Server.</span></span> <span data-ttu-id="6c03a-128">テストアカウントを使用してこの確認を実行するには、テストする Lync Server プールの FQDN を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c03a-128">To run this check using test accounts, you just have to specify the FQDN of the Lync Server pool being tested.</span></span> <span data-ttu-id="6c03a-129">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="6c03a-129">For example:</span></span>

    Test-CsGroupIM -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="6c03a-130">実際のユーザーアカウントを使用してこのチェックを実行するには、Lync Server 管理シェルの資格情報オブジェクト (アカウント名とパスワードを含むオブジェクト) を各アカウントに作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c03a-130">To run this check using actual user accounts, you must create two Lync Server Management Shell credentials objects (objects that contain the account name and password) for each account.</span></span> <span data-ttu-id="6c03a-131">次に、テストまたは CsGroupIM を呼び出すときに、これらの資格情報オブジェクトと、2つのアカウントの SIP アドレスを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c03a-131">You must then include those credentials objects and the SIP addresses of the two accounts when you call Test-CsGroupIM:</span></span>

    $credential1 = Get-Credential "litwareinc\kenmyer"
    $credential2 = Get-Credential "litwareinc\davidlongmire"
    Test-CsGroupIm -TargetFqdn "atl-cs-001.litwareinc.com" -SenderSipAddress "sip:kenmyer@litwareinc.com" -SenderCredential $credential1 -ReceiverSipAddress "sip:davidlongmire@litwareinc.com" -ReceiverCredential $credential2

<span data-ttu-id="6c03a-132">詳細については、「 [テスト-CsGroupIM](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupIM) コマンドレットのヘルプドキュメント」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6c03a-132">For more information, see the Help documentation for the [Test-CsGroupIM](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupIM) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="6c03a-133">成功または失敗を確認する</span><span class="sxs-lookup"><span data-stu-id="6c03a-133">Determining Success or Failure</span></span>

<span data-ttu-id="6c03a-134">2人のユーザーがグループのインスタントメッセージングセッションを完了できる場合は、次のような結果として、Success とマークされた Result プロパティが表示され **ます。**</span><span class="sxs-lookup"><span data-stu-id="6c03a-134">If the two users can complete a group instant messaging session, you'll receive output similar to this with the Result property marked as **Success:**</span></span>

<span data-ttu-id="6c03a-135">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="6c03a-135">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="6c03a-136">結果: 成功</span><span class="sxs-lookup"><span data-stu-id="6c03a-136">Result : Success</span></span>

<span data-ttu-id="6c03a-137">待ち時間:00:00: 06.3812203</span><span class="sxs-lookup"><span data-stu-id="6c03a-137">Latency : 00:00:06.3812203</span></span>

<span data-ttu-id="6c03a-138">誤差</span><span class="sxs-lookup"><span data-stu-id="6c03a-138">Error :</span></span>

<span data-ttu-id="6c03a-139">診断</span><span class="sxs-lookup"><span data-stu-id="6c03a-139">Diagnosis :</span></span>

<span data-ttu-id="6c03a-140">2人のユーザーがインスタントメッセージングセッションを完了できなかった場合、結果はエラーとして表示され、エラーと診断のプロパティに追加情報が記録されます。</span><span class="sxs-lookup"><span data-stu-id="6c03a-140">If the two users can't able to complete the instant messaging session, then the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="6c03a-141">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="6c03a-141">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="6c03a-142">結果: エラー</span><span class="sxs-lookup"><span data-stu-id="6c03a-142">Result : Failure</span></span>

<span data-ttu-id="6c03a-143">待ち時間: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="6c03a-143">Latency : 00:00:00</span></span>

<span data-ttu-id="6c03a-144">エラー: 404、見つかりません</span><span class="sxs-lookup"><span data-stu-id="6c03a-144">Error : 404, Not Found</span></span>

<span data-ttu-id="6c03a-145">診断: ErrorCode = 4005、Source = atl-cs-001.litwareinc.com、</span><span class="sxs-lookup"><span data-stu-id="6c03a-145">Diagnosis : ErrorCode=4005,Source=atl-cs-001.litwareinc.com,</span></span>

<span data-ttu-id="6c03a-146">理由 = ターゲット URI が SIP で有効になっていないか、</span><span class="sxs-lookup"><span data-stu-id="6c03a-146">Reason=Destination URI either not enabled for SIP or does not</span></span>

<span data-ttu-id="6c03a-147">残っ.</span><span class="sxs-lookup"><span data-stu-id="6c03a-147">exist.</span></span>

<span data-ttu-id="6c03a-148">DiagnosticHeader の場合</span><span class="sxs-lookup"><span data-stu-id="6c03a-148">Microsoft.Rtc.Signaling.DiagnosticHeader</span></span>

<span data-ttu-id="6c03a-149">前回の出力では、アカウントが存在しないか、ユーザーが Lync Server を有効にしていないために、少なくとも1つのテストアカウントが無効であったため、テストが失敗したことが示されます。</span><span class="sxs-lookup"><span data-stu-id="6c03a-149">The previous output states that the test failed because at least one of the test accounts was not valid, either because the account does not exist or because the user has not been enabled for Lync Server.</span></span> <span data-ttu-id="6c03a-150">アカウントが存在するかどうかを確認することができます。また、次のようなコマンドを実行することにより、そのアカウントが海里で有効になっているかどうかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="6c03a-150">You can verify the account exists, and whether or not the account has been enabled for nm-ocs-14-3rd by running a command similar to this:</span></span>

    "Ken Myer", "David Longmire" | Get-CsUser | Select-Object SipAddress, Enabled

<span data-ttu-id="6c03a-151">Test-CsGroupIM が失敗した場合は、Verbose パラメーターも含めて、テストを再実行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="6c03a-151">If Test-CsGroupIM fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsGroupIM -TargetFqdn "atl-cs-001.litwareinc.com" -Verbose

<span data-ttu-id="6c03a-152">Verbose パラメーターが含まれている場合、Test-CsGroupIM は、指定されたユーザーがグループのインスタントメッセージングセッションに参加できるかどうかをチェックしたときに実行された各操作のステップバイステップのアカウントを返します。</span><span class="sxs-lookup"><span data-stu-id="6c03a-152">When the Verbose parameter is included, Test-CsGroupIM will return a step-by-step account of each action it tried when it checked the ability of the specified users to participate in a group instant messaging sessions.</span></span> <span data-ttu-id="6c03a-153">たとえば、テストが失敗し、1つ以上のユーザーアカウントが有効でないという通知が表示された場合は、Verbose パラメーターを使用してテストを再実行して、無効なユーザーアカウントを特定することができます。</span><span class="sxs-lookup"><span data-stu-id="6c03a-153">For example, if your test fails and you are told that one or more of the user accounts is not valid, you can rerun the test using the Verbose parameter and determine which user account is not valid:</span></span>

<span data-ttu-id="6c03a-154">登録リクエストの送信:</span><span class="sxs-lookup"><span data-stu-id="6c03a-154">Sending Registration request:</span></span>

 <span data-ttu-id="6c03a-155">ターゲット Fqdn = atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="6c03a-155">Target Fqdn      = atl-cs-001.litwareinc.com</span></span>

 <span data-ttu-id="6c03a-156">ユーザー SIP アドレス = sip:kenmyer@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="6c03a-156">User SIP Address = sip:kenmyer@litwareinc.com</span></span>

 <span data-ttu-id="6c03a-157">登録ポート = 5061</span><span class="sxs-lookup"><span data-stu-id="6c03a-157">Register Port    = 5061</span></span>

<span data-ttu-id="6c03a-158">認証の種類 ' IWA ' が選択されています。</span><span class="sxs-lookup"><span data-stu-id="6c03a-158">Auth type 'IWA' is selected.</span></span>

<span data-ttu-id="6c03a-159">例外 ' ログオンは拒否されました。</span><span class="sxs-lookup"><span data-stu-id="6c03a-159">An exception 'The log on was denied.</span></span> <span data-ttu-id="6c03a-160">正しい資格情報が使用されていて、アカウントがアクティブであることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6c03a-160">Check that the correct credentials are being used and the account is active'</span></span>

<span data-ttu-id="6c03a-161">この例では、SIP アドレス sip:kenmyer@litwareinc.com を持っているユーザーがログオンできなかったことを示しています。</span><span class="sxs-lookup"><span data-stu-id="6c03a-161">As you can see, in this example the user who has the SIP address sip:kenmyer@litwareinc.com was not able to log on.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="6c03a-162">テストに失敗した可能性がある理由</span><span class="sxs-lookup"><span data-stu-id="6c03a-162">Reasons why the test might have failed</span></span>

<span data-ttu-id="6c03a-163">Test-CsGroupIM が失敗する可能性がある一般的な理由を次に示します。</span><span class="sxs-lookup"><span data-stu-id="6c03a-163">Here are some common reasons why Test-CsGroupIM might fail:</span></span>

  - <span data-ttu-id="6c03a-164">指定したユーザーアカウントが間違っています。</span><span class="sxs-lookup"><span data-stu-id="6c03a-164">You specified an incorrect user account.</span></span> <span data-ttu-id="6c03a-165">次のようなコマンドを実行すると、ユーザーアカウントが存在するかどうかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="6c03a-165">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="6c03a-166">ユーザーアカウントは有効ですが、アカウントは現在 Lync Server に対して有効になっていません。</span><span class="sxs-lookup"><span data-stu-id="6c03a-166">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="6c03a-167">ユーザーアカウントが Lync Server 用に有効になっていることを確認するには、次のようなコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="6c03a-167">To verify that a user account was enabled for Lync Server, run a command similar to the following:</span></span>
    
    <span data-ttu-id="6c03a-168">Get-CsUser "sip:kenmyer@litwareinc.com" |Select-Object 有効</span><span class="sxs-lookup"><span data-stu-id="6c03a-168">Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled</span></span>
    
    <span data-ttu-id="6c03a-169">Enabled プロパティが False に設定されている場合は、ユーザーが現在 Lync Server を有効にしていないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="6c03a-169">If the Enabled property is set to False, that means that the user is currently not enabled for Lync Server.</span></span>

  - <span data-ttu-id="6c03a-170">インスタントメッセージングサービスを利用できない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6c03a-170">The instant messaging service might not be available.</span></span> <span data-ttu-id="6c03a-171">Lync Server では、アーカイブデータベースにアクセスできない場合にインスタントメッセージングが利用できないようにシステムを構成できます。</span><span class="sxs-lookup"><span data-stu-id="6c03a-171">With Lync Server, you can configure the system so that instant messaging is not available if the archiving database cannot be accessed.</span></span> <span data-ttu-id="6c03a-172">これを確認するには、次のようなコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="6c03a-172">You can verify that by running a command similar to the following:</span></span>
    
        Get-CsArchivingConfiguration -Identity "atl-cs-001.litwareinc.com" | Select-Object BlockOnArchiveFailure
    
    <span data-ttu-id="6c03a-173">Blockonアーカイブエラーが True に設定されている場合は、アーカイブデータベースを使用できるかどうかを判断する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c03a-173">If BlockOnArchiveFailure is set to True, then you should determine whether or not the archiving database is available.</span></span> <span data-ttu-id="6c03a-174">次のコマンドを使用して、アーカイブデータベースの場所を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="6c03a-174">You can return the locations of your archiving databases by using the following command:</span></span>
    
        Get-CsService -ArchivingDatabase

  - <span data-ttu-id="6c03a-175">アーカイブサーバーを利用できない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6c03a-175">The Archiving Server might not be available.</span></span> <span data-ttu-id="6c03a-176">次のコマンドを使用して、アーカイブサーバーの FQDN を取得できます。</span><span class="sxs-lookup"><span data-stu-id="6c03a-176">You can retrieve the FQDN of your Archiving Servers by using this command:</span></span>
    
        Get-CsService -ArchivingServer
    
    <span data-ttu-id="6c03a-177">次に、適切なサーバーに対して ping を実行し、そのサーバーが利用可能であることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="6c03a-177">You can then ping the appropriate server to verify that it is available.</span></span> <span data-ttu-id="6c03a-178">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="6c03a-178">For example:</span></span>
    
        ping atl-archiving-001.litwareinc.com

<span data-ttu-id="6c03a-179"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6c03a-179"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

