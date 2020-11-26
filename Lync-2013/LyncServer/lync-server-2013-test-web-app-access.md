---
title: 'Lync Server 2013: Web アプリへのアクセスのテスト'
description: 'Lync Server 2013: Web アプリへのアクセスをテストします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test Web App access
ms:assetid: 17d67ea3-f74d-4952-ac2b-92c0dacc8014
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn767944(v=OCS.15)
ms:contentKeyID: 63969584
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fc3bbc8008df4fe47fc5a39571356383fe5a6035
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441131"
---
# <a name="test-web-app-access-in-lync-server-2013"></a><span data-ttu-id="074ea-103">Lync Server 2013 で Web アプリへのアクセスをテストする</span><span class="sxs-lookup"><span data-stu-id="074ea-103">Test Web App access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="074ea-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="074ea-104">

<span> </span></span></span>

<span data-ttu-id="074ea-105">_**最終更新日:** 2014-06-07_</span><span class="sxs-lookup"><span data-stu-id="074ea-105">_**Topic Last Modified:** 2014-06-07_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="074ea-106">確認のスケジュール</span><span class="sxs-lookup"><span data-stu-id="074ea-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="074ea-107">毎月</span><span class="sxs-lookup"><span data-stu-id="074ea-107">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="074ea-108">テストツール</span><span class="sxs-lookup"><span data-stu-id="074ea-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="074ea-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="074ea-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="074ea-110">必要なアクセス許可</span><span class="sxs-lookup"><span data-stu-id="074ea-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="074ea-111">Lync Server 管理シェルを使用してローカルで実行する場合、ユーザーは RTCUniversalServerAdmins セキュリティグループのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="074ea-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="074ea-112">Windows PowerShell のリモートインスタンスを使って実行する場合は、Test-CsWebApp コマンドレットを実行するためのアクセス許可を持つ RBAC の役割をユーザーに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="074ea-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsWebApp cmdlet.</span></span> <span data-ttu-id="074ea-113">このコマンドレットを使うことができるすべての RBAC ロールの一覧を表示するには、Windows PowerShell プロンプトから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="074ea-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsWebApp&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="074ea-114">説明</span><span class="sxs-lookup"><span data-stu-id="074ea-114">Description</span></span>

<span data-ttu-id="074ea-115">Test-CsWebApp コマンドレットは、認証されたユーザーが Lync Web App を使って Lync Server 会議に参加できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="074ea-115">The Test-CsWebApp cmdlet verifies that authenticated users can join Lync Server conferences by using the Lync Web App.</span></span> <span data-ttu-id="074ea-116">このコマンドレットを実行すると、Test-CsWebApp Web チケットサービスに接続して、指定されたユーザーの web チケットを取得できます。</span><span class="sxs-lookup"><span data-stu-id="074ea-116">When you run the cmdlet, Test-CsWebApp contacts the Web Ticket service to obtain web tickets for the specified users.</span></span> <span data-ttu-id="074ea-117">これらのチケットは、Lync Server 会議の "受付チケット" として効果的に機能します。</span><span class="sxs-lookup"><span data-stu-id="074ea-117">These tickets effectively act as ‘admission tickets” to the Lync Server conference.</span></span> <span data-ttu-id="074ea-118">チケットを取得でき、ユーザーを認証できる場合は、Test-CsWebApp は Lync Server に連絡して、インスタントメッセージング、アプリケーション共有、データコラボレーション用の個別の会議を確立しようとします。</span><span class="sxs-lookup"><span data-stu-id="074ea-118">If the tickets can be retrieved, and if the users can be authenticated, Test-CsWebApp will then contact Lync Server and attempt to establish separate conferences for instant messaging, application sharing, and data collaboration.</span></span>

<span data-ttu-id="074ea-119">Test-CsWebApp、これらの会議を作成するために使用された Api と接続を確認するだけであることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="074ea-119">Note that Test-CsWebApp just verifies the APIs and connections used to create these conferences.</span></span> <span data-ttu-id="074ea-120">このコマンドレットは、Lync Web App を使用して会議を作成して参加できることを確認するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="074ea-120">The cmdlet is designed to verify that Lync Web App could be used to create and join conferences.</span></span> <span data-ttu-id="074ea-121">ただし、実際には会議を作成して実施するわけではありません。</span><span class="sxs-lookup"><span data-stu-id="074ea-121">However,, it does not actually create and conduct a conference.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="074ea-122">テストの実行</span><span class="sxs-lookup"><span data-stu-id="074ea-122">Running the test</span></span>

<span data-ttu-id="074ea-123">Test-CsWebApp コマンドレットを実行するには、構成済みのテストアカウントのペア、または Lync Server を有効にしている2人のユーザーのアカウントのいずれかを使用します。</span><span class="sxs-lookup"><span data-stu-id="074ea-123">The Test-CsWebApp cmdlet can be run using either a pair of preconfigured test accounts or the accounts of any two users who are enabled for Lync Server.</span></span> <span data-ttu-id="074ea-124">テストアカウントを使用してこのチェックを実行するには、テスト対象の Lync サーバープールの完全修飾ドメイン名を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="074ea-124">To run this check using test accounts, you just have to specify the fully qualified domain name of the Lync Server pool being tested.</span></span> <span data-ttu-id="074ea-125">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="074ea-125">For example:</span></span>

    Test-CsWebApp -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="074ea-126">実際のユーザーアカウントを使用してこのチェックを実行するには、2つの Windows PowerShell credentials オブジェクト (アカウント名とパスワードを含むオブジェクト) を各アカウントに作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="074ea-126">To run this check using actual user accounts, you must create two Windows PowerShell credentials objects (objects that contain the account name and password) for each account.</span></span> <span data-ttu-id="074ea-127">次に、これらの資格情報オブジェクトと、次に記載されている2つのアカウントの SIP アドレスを、テスト用の Webapp の作成時に含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="074ea-127">You must then include those credentials objects and the SIP addresses of the two accounts when you call Test-CsWebApp:</span></span>

    $cred1 = Get-Credential "litwareinc\kenmyer"
    $cred2 = Get-Credential "litwareinc\pilar"
    
    Test-CsWebApp -TargetFqdn atl-cs-001.litwareinc.com -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $cred1 -User2SipAddress "sip:pilar@litwareinc.com" -User2Credential $cred2

<span data-ttu-id="074ea-128">詳細については、「 [テスト-CsWebApp](https://docs.microsoft.com/powershell/module/skype/Test-CsWebApp) コマンドレットのヘルプ」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="074ea-128">For more information, see the help topic for the [Test-CsWebApp](https://docs.microsoft.com/powershell/module/skype/Test-CsWebApp) cmdlet.</span></span> <span data-ttu-id="074ea-129">Test-CsWebApp は Lync Server 2013 で使用するためには廃止されたことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="074ea-129">Note that Test-CsWebApp was deprecated for use on Lync Server 2013.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="074ea-130">成功または失敗を確認する</span><span class="sxs-lookup"><span data-stu-id="074ea-130">Determining success or failure</span></span>

<span data-ttu-id="074ea-131">Test-CsWebApp がユーザーを会議に参加できる場合、コマンドレットによってテスト結果の成功が返されます。</span><span class="sxs-lookup"><span data-stu-id="074ea-131">If Test-CsWebApp can join the users to their conferences, the cmdlet will return the test result Success:</span></span>

<span data-ttu-id="074ea-132">ターゲット Fqdn:</span><span class="sxs-lookup"><span data-stu-id="074ea-132">Target Fqdn :</span></span>

<span data-ttu-id="074ea-133">結果: 成功</span><span class="sxs-lookup"><span data-stu-id="074ea-133">Result : Success</span></span>

<span data-ttu-id="074ea-134">待ち時間: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="074ea-134">Latency : 00:00:00</span></span>

<span data-ttu-id="074ea-135">エラーメッセージ:</span><span class="sxs-lookup"><span data-stu-id="074ea-135">Error Message :</span></span>

<span data-ttu-id="074ea-136">診断</span><span class="sxs-lookup"><span data-stu-id="074ea-136">Diagnosis :</span></span>

<span data-ttu-id="074ea-137">ユーザーが必要な会議に参加できない場合、テスト結果は [エラー] としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="074ea-137">If the users cannot join the necessary conferences then the test result will be marked as Failure.</span></span> <span data-ttu-id="074ea-138">通常 Test-CsWebApp は、詳細なエラーメッセージと診断にも報告されます。</span><span class="sxs-lookup"><span data-stu-id="074ea-138">Typically Test-CsWebApp will also report back a detailed error message and diagnosis:</span></span>

<span data-ttu-id="074ea-139">ターゲット Fqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="074ea-139">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="074ea-140">結果: エラー</span><span class="sxs-lookup"><span data-stu-id="074ea-140">Result : Failure</span></span>

<span data-ttu-id="074ea-141">待ち時間: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="074ea-141">Latency : 00:00:00</span></span>

<span data-ttu-id="074ea-142">エラーメッセージ: Web-Ticket サービスの応答が受信されませんでした</span><span class="sxs-lookup"><span data-stu-id="074ea-142">Error Message : No response received for Web-Ticket service</span></span>

<span data-ttu-id="074ea-143">診断: HTTP 要求はクライアントで承認されていません</span><span class="sxs-lookup"><span data-stu-id="074ea-143">Diagnosis : The HTTP request is unauthorized with client</span></span>

<span data-ttu-id="074ea-144">認証スキーム ' Ntlm '。</span><span class="sxs-lookup"><span data-stu-id="074ea-144">authentication scheme 'Ntlm'.</span></span> <span data-ttu-id="074ea-145">認証</span><span class="sxs-lookup"><span data-stu-id="074ea-145">The authentication</span></span>

<span data-ttu-id="074ea-146">サーバーから受信したヘッダーは、"Negotiate、NTLM" でした。</span><span class="sxs-lookup"><span data-stu-id="074ea-146">header received from the server was 'Negotiate,NTLM'.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="074ea-147">テストに失敗した可能性がある理由</span><span class="sxs-lookup"><span data-stu-id="074ea-147">Reasons why the test might have failed</span></span>

<span data-ttu-id="074ea-148">通常、Test-CsWebApp のエラーには、ユーザー認証エラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="074ea-148">Test-CsWebApp failures typically involve user authentication errors.</span></span> <span data-ttu-id="074ea-149">Test-CsWebApp に失敗した場合は、まず、指定したユーザーが有効なユーザーアカウントを持っていて、Lync Server が有効になっていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="074ea-149">If Test-CsWebApp fails, you should first verify that the specified users have valid user accounts and are enabled for Lync Server.</span></span> <span data-ttu-id="074ea-150">次のようなコマンドを使用して、アカウント情報を取得できます。</span><span class="sxs-lookup"><span data-stu-id="074ea-150">You can retrieve account information by using a command similar to this:</span></span>

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object Enabled

<span data-ttu-id="074ea-151">Enabled プロパティが True と等しくない場合、またはコマンドが失敗した場合は、ユーザーが有効な Lync Server アカウントを持っていないことを意味します。また、コマンドレットに指定したパスワードが有効であることも確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="074ea-151">If the Enabled property is not equal to True or if the command fails, that means that the user does not have a valid Lync Server account.You should also verify that the passwords that you supplied to the cmdlet are valid.</span></span>

<span data-ttu-id="074ea-152"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="074ea-152"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

