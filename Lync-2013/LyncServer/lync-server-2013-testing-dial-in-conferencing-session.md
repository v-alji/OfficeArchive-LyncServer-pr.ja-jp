---
title: 'Lync Server 2013: ダイヤルイン会議セッションのテスト'
description: 'Lync Server 2013: ダイヤルイン会議セッションをテストしています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing dial-in conferencing session
ms:assetid: 6c505be5-5af7-450c-b3ca-10d9122bee5c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743834(v=OCS.15)
ms:contentKeyID: 63969613
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4d0c51b16df674dbf8bf7f0a2c6c4c93c2606d95
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398973"
---
# <a name="testing-dial-in-conferencing-session-in-lync-server-2013"></a><span data-ttu-id="73606-103">Lync Server 2013 でのダイヤルイン会議セッションのテスト</span><span class="sxs-lookup"><span data-stu-id="73606-103">Testing dial-in conferencing session in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="73606-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="73606-104">

<span> </span></span></span>

<span data-ttu-id="73606-105">_**最終更新日:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="73606-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73606-106">確認のスケジュール</span><span class="sxs-lookup"><span data-stu-id="73606-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="73606-107">[毎日]</span><span class="sxs-lookup"><span data-stu-id="73606-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73606-108">テストツール</span><span class="sxs-lookup"><span data-stu-id="73606-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="73606-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="73606-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73606-110">必要なアクセス許可</span><span class="sxs-lookup"><span data-stu-id="73606-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="73606-111">Lync Server 管理シェルを使用してローカルで実行する場合、ユーザーは RTCUniversalServerAdmins セキュリティグループのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="73606-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="73606-112">Windows PowerShell のリモートインスタンスを使って実行する場合は、Test-CsDialInConferencing コマンドレットを実行するためのアクセス許可を持つ RBAC の役割をユーザーに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="73606-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsDialInConferencing cmdlet.</span></span> <span data-ttu-id="73606-113">このコマンドレットを使うことができるすべての RBAC ロールの一覧を表示するには、Windows PowerShell プロンプトから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="73606-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsDialInConferencing&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="73606-114">説明</span><span class="sxs-lookup"><span data-stu-id="73606-114">Description</span></span>

<span data-ttu-id="73606-115">Test-CsDialInConferencing コマンドレットは、ユーザーがダイヤルイン会議に参加できるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="73606-115">The Test-CsDialInConferencing cmdlet verifies whether a user can participate in a dial-in conference.</span></span> <span data-ttu-id="73606-116">Test-CsDialInConferencing は、テストユーザーをシステムにログインしようとします。</span><span class="sxs-lookup"><span data-stu-id="73606-116">Test-CsDialInConferencing works by trying to log a test user onto the system.</span></span> <span data-ttu-id="73606-117">ログオンが成功すると、コマンドレットはユーザーの資格情報とアクセス許可を使って、利用可能なダイヤルイン会議アクセス番号をすべて試します。</span><span class="sxs-lookup"><span data-stu-id="73606-117">If the logon succeeds, the cmdlet will then use the user’s credentials and permissions to try all of the available dial-in conferencing access numbers.</span></span> <span data-ttu-id="73606-118">各ダイヤルイン試行の成功または失敗が通知されます。次に、テストユーザーは、Lync Server からログオフされます。テスト-Csdial Inコンファレンスは、適切な接続を確立できることのみを確認します。</span><span class="sxs-lookup"><span data-stu-id="73606-118">The success or failure of each dial-in try will be noted, then the test user will be logged off from Lync Server.Test-CsDialInConferencing only verifies that the appropriate connections can be made.</span></span> <span data-ttu-id="73606-119">このコマンドレットは、実際には電話をかけたり、他のユーザーが参加できるダイヤルイン会議を作成したりすることはありません。</span><span class="sxs-lookup"><span data-stu-id="73606-119">The cmdlet does not actually make any phone calls or create any dial-in conferences that other users can join.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="73606-120">テストの実行</span><span class="sxs-lookup"><span data-stu-id="73606-120">Running the test</span></span>

<span data-ttu-id="73606-121">Test-CsDialInConferencing コマンドレットを実行するには、事前に定義されたテストアカウント (「Lync Server のテストを実行するためのテストアカウントをセットアップする」を参照) を使用するか、Lync Server を有効にしているユーザーのアカウントを使用します。</span><span class="sxs-lookup"><span data-stu-id="73606-121">The Test-CsDialInConferencing cmdlet can be run using either a preconfigured test account (see Setting Up Test Accounts for Running Lync Server Tests) or the account of any user who is enabled for Lync Server.</span></span> <span data-ttu-id="73606-122">テストアカウントを使用してこのチェックを実行するには、テスト対象の Lync Server プールの FQDN を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="73606-122">To run this check using a test account, you just have to specify the FQDN of the Lync Server pool being tested.</span></span> <span data-ttu-id="73606-123">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="73606-123">For example:</span></span>

    Test-CsDialInConferencing -TargetFqdn "atl-cs-001.litwareinc.com" 

<span data-ttu-id="73606-124">実際のユーザーアカウントを使用してこのチェックを実行するには、アカウント名とパスワードを含む Windows PowerShell 資格情報オブジェクトを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="73606-124">To run this check using an actual user account, you must create a Windows PowerShell credentials object that contains the account name and password.</span></span> <span data-ttu-id="73606-125">次に、その資格情報オブジェクトと、通話テスト用のアカウント SIP アドレスを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="73606-125">You must then include that credentials object and the account SIP address the calling Test-CsDialInConferencing:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsDialInConferencing -TargetFqdn atl-cs-001.litwareinc.com" -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

<span data-ttu-id="73606-126">詳細については、「 [テスト](https://docs.microsoft.com/powershell/module/skype/Test-CsDialInConferencing) 用のヘルプ」コマンドレットのヘルプドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="73606-126">For more information, see the Help documentation for the [Test-CsDialInConferencing](https://docs.microsoft.com/powershell/module/skype/Test-CsDialInConferencing) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="73606-127">成功または失敗を確認する</span><span class="sxs-lookup"><span data-stu-id="73606-127">Determining success or failure</span></span>

<span data-ttu-id="73606-128">指定したユーザーが Lync サーバーにログオンして、利用可能なダイヤルイン会議アクセス番号のいずれかを使用して接続すると、次のような出力が表示され、Result プロパティは Success とマークされ **ます。**</span><span class="sxs-lookup"><span data-stu-id="73606-128">If the specified user can log on to Lync Server and then make a connection using one of the available dial-in conferencing access numbers, then you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="73606-129">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="73606-129">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="73606-130">結果: 成功</span><span class="sxs-lookup"><span data-stu-id="73606-130">Result : Success</span></span>

<span data-ttu-id="73606-131">待ち時間:00:00: 06.8630376</span><span class="sxs-lookup"><span data-stu-id="73606-131">Latency : 00:00:06.8630376</span></span>

<span data-ttu-id="73606-132">誤差</span><span class="sxs-lookup"><span data-stu-id="73606-132">Error :</span></span>

<span data-ttu-id="73606-133">診断</span><span class="sxs-lookup"><span data-stu-id="73606-133">Diagnosis :</span></span>

<span data-ttu-id="73606-134">指定したユーザーがこの接続を確立できない場合、結果はエラーとして表示され、エラーと診断のプロパティに追加情報が記録されます。</span><span class="sxs-lookup"><span data-stu-id="73606-134">If the specified user can't make this connection, then the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="73606-135">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="73606-135">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="73606-136">結果: エラー</span><span class="sxs-lookup"><span data-stu-id="73606-136">Result : Failure</span></span>

<span data-ttu-id="73606-137">待ち時間: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="73606-137">Latency : 00:00:00</span></span>

<span data-ttu-id="73606-138">エラー: ログオンは拒否されました。</span><span class="sxs-lookup"><span data-stu-id="73606-138">Error : The log on was denied.</span></span> <span data-ttu-id="73606-139">適切な資格情報があることを確認する</span><span class="sxs-lookup"><span data-stu-id="73606-139">Check that the proper credentials are</span></span>

<span data-ttu-id="73606-140">使用されていて、アカウントが有効になっています。</span><span class="sxs-lookup"><span data-stu-id="73606-140">being used and the account is active.</span></span>

<span data-ttu-id="73606-141">内部例外: NegotiateSecurityAssociation に失敗しました。エラー:-</span><span class="sxs-lookup"><span data-stu-id="73606-141">Inner Exception:NegotiateSecurityAssociation failed, error: -</span></span>

<span data-ttu-id="73606-142">2146893044</span><span class="sxs-lookup"><span data-stu-id="73606-142">2146893044</span></span>

<span data-ttu-id="73606-143">診断</span><span class="sxs-lookup"><span data-stu-id="73606-143">Diagnosis :</span></span>

<span data-ttu-id="73606-144">前回の出力では、テストユーザーが Lync Server 自体へのアクセスを拒否されたことを示しています。</span><span class="sxs-lookup"><span data-stu-id="73606-144">The previous output indicates that the test user was denied access to Lync Server itself.</span></span> <span data-ttu-id="73606-145">これは通常、Test-CsDialInConferencing に渡されたユーザー資格情報が無効であったことを意味します。</span><span class="sxs-lookup"><span data-stu-id="73606-145">This typically means that the user credentials passed to Test-CsDialInConferencing were not valid.</span></span> <span data-ttu-id="73606-146">さらに、Windows PowerShell 資格情報オブジェクトを再作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="73606-146">In turn, you should re-create the Windows PowerShell credentials object.</span></span> <span data-ttu-id="73606-147">ユーザーアカウントのパスワードを取得することはできますが、次のようなコマンドを使用して SIP アドレスを確認できます。</span><span class="sxs-lookup"><span data-stu-id="73606-147">Although you can retrieve the password for the user account, you can verify the SIP address by using a command similar to this:</span></span>

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object SipAddress

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="73606-148">テストに失敗した可能性がある理由</span><span class="sxs-lookup"><span data-stu-id="73606-148">Reasons why the test might have failed</span></span>

<span data-ttu-id="73606-149">Test-CsDialInConferencing が失敗する可能性がある一般的な理由を次に示します。</span><span class="sxs-lookup"><span data-stu-id="73606-149">Here are some common reasons why Test-CsDialInConferencing might fail:</span></span>

  - <span data-ttu-id="73606-150">無効なユーザーアカウントが指定されました。</span><span class="sxs-lookup"><span data-stu-id="73606-150">You specified a user account that is not valid.</span></span> <span data-ttu-id="73606-151">次のようなコマンドを実行すると、ユーザーアカウントが存在するかどうかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="73606-151">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="73606-152">ユーザーアカウントは有効ですが、アカウントは現在 Lync Server に対して有効になっていません。</span><span class="sxs-lookup"><span data-stu-id="73606-152">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="73606-153">Lync Server でユーザーアカウントが有効になっていることを確認するには、次のようなコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="73606-153">To verify that a user account is enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="73606-154">Enabled プロパティが False に設定されている場合は、ユーザーが現在 Lync Server を有効にしていないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="73606-154">If the Enabled property is set to False, that means that the user is currently not enabled for Lync Server.</span></span>

  - <span data-ttu-id="73606-155">ダイヤルイン会議のアクセス番号が間違っている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="73606-155">You might have an incorrect dial-in conferencing access number.</span></span> <span data-ttu-id="73606-156">次のコマンドを使用して、現在構成されているダイヤルイン会議アクセス番号のリストを返すことができます。</span><span class="sxs-lookup"><span data-stu-id="73606-156">You can return your currently-configured list of dial-in conferencing access numbers by using this command:</span></span>
    
        Get-CsDialConferencingAccessNumber

<span data-ttu-id="73606-157"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="73606-157"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

