---
title: 'Lync Server 2013: アドレス帳へのアクセスを検証する'
description: 'Lync Server 2013: アドレス帳へのアクセスを検証しています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Validating address book access
ms:assetid: 630682c6-9262-46c5-9af1-6193db70374b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720916(v=OCS.15)
ms:contentKeyID: 63969611
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6da08e48be24b3325bc1f415b9baa3c9197717c3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438632"
---
# <a name="validating-address-book-access-in-lync-server-2013"></a><span data-ttu-id="f6d27-103">Lync Server 2013 でのアドレス帳へのアクセスを検証する</span><span class="sxs-lookup"><span data-stu-id="f6d27-103">Validating address book access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f6d27-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f6d27-104">

<span> </span></span></span>

<span data-ttu-id="f6d27-105">_**最終更新日:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="f6d27-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f6d27-106">確認のスケジュール</span><span class="sxs-lookup"><span data-stu-id="f6d27-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="f6d27-107">[毎日]</span><span class="sxs-lookup"><span data-stu-id="f6d27-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6d27-108">テストツール</span><span class="sxs-lookup"><span data-stu-id="f6d27-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="f6d27-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="f6d27-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f6d27-110">必要なアクセス許可</span><span class="sxs-lookup"><span data-stu-id="f6d27-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="f6d27-111">Lync Server 管理シェルを使用してローカルで実行する場合、ユーザーは RTCUniversalServerAdmins セキュリティグループのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="f6d27-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="f6d27-112">Windows PowerShell のリモートインスタンスを使って実行する場合は、Test-CsAddressBookService コマンドレットを実行するためのアクセス許可を持つ RBAC の役割をユーザーに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="f6d27-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsAddressBookService cmdlet.</span></span> <span data-ttu-id="f6d27-113">このコマンドレットを使うことができるすべての RBAC ロールの一覧を表示するには、Windows PowerShell プロンプトから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="f6d27-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsAddressBookService&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="f6d27-114">説明</span><span class="sxs-lookup"><span data-stu-id="f6d27-114">Description</span></span>

<span data-ttu-id="f6d27-115">Test-CsAddressBookService コマンドレットを使うと、ユーザーがアドレス帳のダウンロード Web サービスに接続できるかどうかを確認することができます。</span><span class="sxs-lookup"><span data-stu-id="f6d27-115">The Test-CsAddressBookService cmdlet provides a way for you to verify that a user can connect to the Address Book Download Web service.</span></span> <span data-ttu-id="f6d27-116">コマンドレットを実行すると、Test-CsAddressBookService 指定されたプールのアドレス帳のダウンロード Web サービスに接続し、アドレス帳ファイルの場所を要求します。</span><span class="sxs-lookup"><span data-stu-id="f6d27-116">When you run the cmdlet, Test-CsAddressBookService connects to the Address Book Download Web service on the specified pool and requests the location of the Address Book files.</span></span> <span data-ttu-id="f6d27-117">アドレス帳のダウンロード Web サービスがこの場所を提供した場合、テストは成功したと見なされます。</span><span class="sxs-lookup"><span data-stu-id="f6d27-117">If the Address Book Download Web service supplies that location, the test is considered successful.</span></span> <span data-ttu-id="f6d27-118">要求が拒否された場合、テストは失敗したと見なされます。</span><span class="sxs-lookup"><span data-stu-id="f6d27-118">If the request is denied, then the test is considered a failure.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="f6d27-119">テストの実行</span><span class="sxs-lookup"><span data-stu-id="f6d27-119">Running the test</span></span>

<span data-ttu-id="f6d27-120">Test-CsAddressBookService コマンドレットを実行するには、事前に定義されたテストアカウント (「Lync Server テストを実行するためのテストアカウントをセットアップする」を参照)、または Lync Server を有効にしているユーザーのアカウントのいずれかを使用します。</span><span class="sxs-lookup"><span data-stu-id="f6d27-120">The Test-CsAddressBookService cmdlet can be run using either a preconfigured test account (see Setting Up Test Accounts for Running Lync Server Tests) or the account of any user who has been enabled for Lync Server.</span></span> <span data-ttu-id="f6d27-121">テストアカウントを使用してこのチェックを実行するには、テスト対象の Lync サーバープールの完全修飾ドメイン名 (FQDN) を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f6d27-121">To run this check using a test account, all you need to do is specify the fully qualified domain name (FQDN) of the Lync Server pool being tested.</span></span> <span data-ttu-id="f6d27-122">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="f6d27-122">For example:</span></span>

    Test-CsAddressBookService -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="f6d27-123">実際のユーザーアカウントを使用してこのチェックを実行するには、最初に、アカウント名とパスワードを含む Windows PowerShell 資格情報オブジェクトを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f6d27-123">To run this check using an actual user account, you must first create a Windows PowerShell credentials object that contains the account name and password.</span></span> <span data-ttu-id="f6d27-124">次に、ユーザーの資格情報オブジェクトと、CsAddressBookService を呼び出すときにアカウントに割り当てられた SIP アドレスを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="f6d27-124">You must then include that credentials object and the SIP address assigned to the account when calling Test-CsAddressBookService:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsAddressBookService -TargetFqdn "atl-cs-001.litwareinc.com"-UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

<span data-ttu-id="f6d27-125">詳細については、「 [テスト-CsAddressBookService](https://docs.microsoft.com/powershell/module/skype/Test-CsAddressBookService) コマンドレットのヘルプドキュメント」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f6d27-125">For more information, see the Help documentation for the [Test-CsAddressBookService](https://docs.microsoft.com/powershell/module/skype/Test-CsAddressBookService) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="f6d27-126">成功または失敗を確認する</span><span class="sxs-lookup"><span data-stu-id="f6d27-126">Determining success or failure</span></span>

<span data-ttu-id="f6d27-127">指定したユーザーがアドレス帳サービスに接続できる場合は、次のような結果が返されます。これには、Result プロパティが **Success** とマークされています。</span><span class="sxs-lookup"><span data-stu-id="f6d27-127">If the specified user is able to connect to the Address Book Service you will get back output similar to this, with the Result property marked as **Success**:</span></span>

<span data-ttu-id="f6d27-128">TargetUri : https://lync-se.fabrikam.com:443/abs/handler</span><span class="sxs-lookup"><span data-stu-id="f6d27-128">TargetUri : https://lync-se.fabrikam.com:443/abs/handler</span></span>

<span data-ttu-id="f6d27-129">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="f6d27-129">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="f6d27-130">結果: 成功</span><span class="sxs-lookup"><span data-stu-id="f6d27-130">Result : Success</span></span>

<span data-ttu-id="f6d27-131">待ち時間:00:00: 06.2260399</span><span class="sxs-lookup"><span data-stu-id="f6d27-131">Latency : 00:00:06.2260399</span></span>

<span data-ttu-id="f6d27-132">誤差</span><span class="sxs-lookup"><span data-stu-id="f6d27-132">Error :</span></span>

<span data-ttu-id="f6d27-133">診断</span><span class="sxs-lookup"><span data-stu-id="f6d27-133">Diagnosis :</span></span>

<span data-ttu-id="f6d27-134">指定したユーザーがこの接続を確立できない場合、結果は失敗として表示され、エラーと診断のプロパティに追加情報が記録されます。</span><span class="sxs-lookup"><span data-stu-id="f6d27-134">If the specified user is not able to make this connection, the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="f6d27-135">TargetUri :</span><span class="sxs-lookup"><span data-stu-id="f6d27-135">TargetUri :</span></span>

<span data-ttu-id="f6d27-136">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="f6d27-136">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="f6d27-137">結果: エラー</span><span class="sxs-lookup"><span data-stu-id="f6d27-137">Result : Failure</span></span>

<span data-ttu-id="f6d27-138">待ち時間: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="f6d27-138">Latency : 00:00:00</span></span>

<span data-ttu-id="f6d27-139">診断: ErrorCode = 4005、Source = atl-cs-001.litwareinc.com、</span><span class="sxs-lookup"><span data-stu-id="f6d27-139">Diagnosis : ErrorCode=4005,Source=atl-cs-001.litwareinc.com,</span></span>

<span data-ttu-id="f6d27-140">理由 = ターゲット URI が SIP で有効になっていないか、</span><span class="sxs-lookup"><span data-stu-id="f6d27-140">Reason=Destination URI either not enabled for SIP or does not</span></span>

<span data-ttu-id="f6d27-141">残っ.</span><span class="sxs-lookup"><span data-stu-id="f6d27-141">exist.</span></span>

<span data-ttu-id="f6d27-142">DiagnosticHeader の場合</span><span class="sxs-lookup"><span data-stu-id="f6d27-142">Microsoft.Rtc.Signaling.DiagnosticHeader</span></span>

<span data-ttu-id="f6d27-143">たとえば、上記の出力では、指定されたユーザー ("送信先 URI") が存在しないか、Lync Server が有効になっていないため、テストが失敗したことが示されます。</span><span class="sxs-lookup"><span data-stu-id="f6d27-143">For example, the preceding output states that the test failed because the specified user (that is, the “Destination URI”) either does not exist or has not been enabled for Lync Server.</span></span> <span data-ttu-id="f6d27-144">次のようなコマンドを実行して、ユーザーアカウントが有効であるかどうかを確認し、正しい SIP アドレスを入力したことを確認できます。</span><span class="sxs-lookup"><span data-stu-id="f6d27-144">You can verify whether or not a user account is valid, and verify that you supplied the correct SIP address, by running a command like this one:</span></span>

<span data-ttu-id="f6d27-145">Get-CsUser-Identity "sip:kenmyer@litwareinc.com" |Select-Object SipAddress、有効</span><span class="sxs-lookup"><span data-stu-id="f6d27-145">Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object SipAddress, Enabled</span></span>

<span data-ttu-id="f6d27-146">Test-CsAddressBookService が失敗した場合は、Verbose パラメーターも含めて、テストを再実行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f6d27-146">If Test-CsAddressBookService fails then you might want to rerun the test, this time including the Verbose parameter:</span></span>

<span data-ttu-id="f6d27-147">Test-CsAddressBookService-TargetFqdn "atl-cs-001.litwareinc.com"-Verbose</span><span class="sxs-lookup"><span data-stu-id="f6d27-147">Test-CsAddressBookService -TargetFqdn "atl-cs-001.litwareinc.com" -Verbose</span></span>

<span data-ttu-id="f6d27-148">Verbose パラメーターが含まれている場合 Test-CsAddressBookService は、指定されたユーザーが Lync Server にログオンする機能を確認したときに実行される各操作のステップバイステップのアカウントを返します。</span><span class="sxs-lookup"><span data-stu-id="f6d27-148">When the Verbose parameter is included Test-CsAddressBookService will return a step-by-step account of each action it attempted when checking the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="f6d27-149">たとえば、次の例の出力では、少なくともこの例で使用されている [テスト-CsAddressBookService] がアドレス帳ファイルをダウンロードできることを示しています。</span><span class="sxs-lookup"><span data-stu-id="f6d27-149">For example, this sample output shows that Test-CsAddressBookService, at least in this example, was able to download the Address Book file:</span></span>

<span data-ttu-id="f6d27-150">Http GET 要求を送信しています。</span><span class="sxs-lookup"><span data-stu-id="f6d27-150">Sending Http GET Request.</span></span>

<span data-ttu-id="f6d27-151">ファイルパス = https://atl-cs-001.litwareinc.com:443/abs/handler/f-1299.lsabs</span><span class="sxs-lookup"><span data-stu-id="f6d27-151">File Path = https://atl-cs-001.litwareinc.com:443/abs/handler/f-1299.lsabs</span></span>

<span data-ttu-id="f6d27-152">試行回数 = 1</span><span class="sxs-lookup"><span data-stu-id="f6d27-152">Attempt Number = 1</span></span>

<span data-ttu-id="f6d27-153">タイムアウト (ミリ秒) = 6万</span><span class="sxs-lookup"><span data-stu-id="f6d27-153">TimeOut (msec) = 60000</span></span>

<span data-ttu-id="f6d27-154">ABS ファイルが正常にダウンロードされました https://atl-cs-001.litwareinc.com:443/abs/handler/f-1299.lsabs</span><span class="sxs-lookup"><span data-stu-id="f6d27-154">Successfully Downloaded the ABS file https://atl-cs-001.litwareinc.com:443/abs/handler/f-1299.lsabs</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="f6d27-155">テストに失敗した可能性がある理由</span><span class="sxs-lookup"><span data-stu-id="f6d27-155">Reasons why the test might have failed</span></span>

<span data-ttu-id="f6d27-156">Test-CsAddressBookService が失敗する可能性がある一般的な理由を次に示します。</span><span class="sxs-lookup"><span data-stu-id="f6d27-156">Here are some common reasons why Test-CsAddressBookService might fail:</span></span>

  - <span data-ttu-id="f6d27-157">無効なユーザアカウントを指定しました。</span><span class="sxs-lookup"><span data-stu-id="f6d27-157">You specified an invalid user account.</span></span> <span data-ttu-id="f6d27-158">次のようなコマンドを実行すると、ユーザーアカウントが存在するかどうかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="f6d27-158">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="f6d27-159">ユーザーアカウントは有効ですが、アカウントは現在 Lync Server では有効になっていません。</span><span class="sxs-lookup"><span data-stu-id="f6d27-159">The user account is valid, but the account is not currently enabled for Lync Server.</span></span> <span data-ttu-id="f6d27-160">Lync Server のユーザーアカウントが有効になっていることを確認するには、次のようなコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="f6d27-160">To verify that a user account has been enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="f6d27-161">Enabled プロパティが False に設定されている場合は、ユーザーが現在 Lync Server に対して有効になっていないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="f6d27-161">If the Enabled property is set to False that means that the user is not currently enabled for Lync Server.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f6d27-162">関連項目</span><span class="sxs-lookup"><span data-stu-id="f6d27-162">See Also</span></span>


[<span data-ttu-id="f6d27-163">Test-CsAddressBookService</span><span class="sxs-lookup"><span data-stu-id="f6d27-163">Test-CsAddressBookService</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsAddressBookService)  
  

<span data-ttu-id="f6d27-164"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f6d27-164"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

