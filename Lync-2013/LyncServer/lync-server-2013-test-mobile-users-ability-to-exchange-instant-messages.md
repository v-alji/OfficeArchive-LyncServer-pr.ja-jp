---
title: 'Lync Server 2013: モバイルユーザーがインスタントメッセージをやり取りする機能をテストする'
description: 'Lync Server 2013: モバイルユーザーがインスタントメッセージをやり取りできるかテストします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test mobile users' ability to exchange instant messages
ms:assetid: a78a048f-d413-4bee-8626-d62b8b74f811
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn767950(v=OCS.15)
ms:contentKeyID: 63969638
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 675bbeff93fed374d950b2efbdf15b4ea246f861
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444260"
---
# <a name="test-mobile-users-ability-to-exchange-instant-messages-in-lync-server-2013"></a><span data-ttu-id="bc5d7-103">Lync Server 2013 でモバイルユーザーがインスタントメッセージをやり取りする機能をテストする</span><span class="sxs-lookup"><span data-stu-id="bc5d7-103">Test mobile users' ability to exchange instant messages in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bc5d7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bc5d7-104">

<span> </span></span></span>

<span data-ttu-id="bc5d7-105">_**最終更新日:** 2014-06-07_</span><span class="sxs-lookup"><span data-stu-id="bc5d7-105">_**Topic Last Modified:** 2014-06-07_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bc5d7-106">確認のスケジュール</span><span class="sxs-lookup"><span data-stu-id="bc5d7-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="bc5d7-107">毎月</span><span class="sxs-lookup"><span data-stu-id="bc5d7-107">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc5d7-108">テストツール</span><span class="sxs-lookup"><span data-stu-id="bc5d7-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="bc5d7-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="bc5d7-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc5d7-110">必要なアクセス許可</span><span class="sxs-lookup"><span data-stu-id="bc5d7-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="bc5d7-111">Lync Server 管理シェルを使用してローカルで実行する場合、ユーザーは RTCUniversalServerAdmins セキュリティグループのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="bc5d7-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="bc5d7-112">Windows PowerShell のリモートインスタンスを使って実行する場合は、Test-CsMcxP2PIM コマンドレットを実行するためのアクセス許可を持つ RBAC の役割をユーザーに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="bc5d7-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsMcxP2PIM cmdlet.</span></span> <span data-ttu-id="bc5d7-113">このコマンドレットを使うことができるすべての RBAC ロールの一覧を表示するには、Windows PowerShell プロンプトから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="bc5d7-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsMcxP2PIM&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="bc5d7-114">説明</span><span class="sxs-lookup"><span data-stu-id="bc5d7-114">Description</span></span>

<span data-ttu-id="bc5d7-115">モバイルデバイスユーザーは、次のような操作を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="bc5d7-115">The Mobility Service enables mobile device users to do such things as:</span></span>

1.  <span data-ttu-id="bc5d7-116">インスタントメッセージとプレゼンス情報を交換します。</span><span class="sxs-lookup"><span data-stu-id="bc5d7-116">Exchange instant messages and presence information.</span></span>

2.  <span data-ttu-id="bc5d7-117">ワイヤレスプロバイダーではなく、内部でボイスメールを保存して取得します。</span><span class="sxs-lookup"><span data-stu-id="bc5d7-117">Store and retrieve voice mail internally instead of with their wireless provider.</span></span>

3.  <span data-ttu-id="bc5d7-118">職場やダイヤルアウト会議などの Lync Server 機能を利用できます。</span><span class="sxs-lookup"><span data-stu-id="bc5d7-118">Take advantage of Lync Server capabilities such as Call via Work and dial-out conferencing.</span></span>

<span data-ttu-id="bc5d7-119">Test-CsMxcP2PIM コマンドレットを使うと、ユーザーがモビリティサービスを使用してインスタントメッセージを交換できることを簡単かつ簡単に確認することができます。</span><span class="sxs-lookup"><span data-stu-id="bc5d7-119">The Test-CsMxcP2PIM cmdlet provides a quick and easy way to verify that users can use the Mobility Service to exchange instant messages.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="bc5d7-120">テストの実行</span><span class="sxs-lookup"><span data-stu-id="bc5d7-120">Running the test</span></span>

<span data-ttu-id="bc5d7-121">このテストを実行するには、2つの Windows PowerShell credentials オブジェクト (アカウント名とパスワードを含むオブジェクト) を各アカウントに作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bc5d7-121">To run this test, you must create two Windows PowerShell credentials objects (objects that contain the account name and password) for each account.</span></span> <span data-ttu-id="bc5d7-122">次に、CsMcxP2PIM を呼び出したときに、これらの資格情報オブジェクトと、2つのアカウントの SIP アドレスを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="bc5d7-122">You must then include those credentials objects and the SIP addresses of the two accounts when you call Test-CsMcxP2PIM:</span></span>

    $credential1 = Get-Credential "litwareinc\kenmyer"
    $credential2 = Get-Credential "litwareinc\pilar"
    
    Test-CsMcxP2PIM -TargetFqdn "atl-cs-001.litwareinc.com" -Authentication Negotiate -SenderSipAddres "sip:kenmyer@litwareinc.com" -SenderCredential $credential1 -ReceiverSipAddress "sip:packerman@litwareinc.com" -ReceiverCredential $credential2

<span data-ttu-id="bc5d7-123">詳細については、 [CsMcxP2PIM](https://docs.microsoft.com/powershell/module/skype/Test-CsMcxP2PIM) コマンドレットのヘルプトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="bc5d7-123">For more information, see the help topic for the [Test-CsMcxP2PIM](https://docs.microsoft.com/powershell/module/skype/Test-CsMcxP2PIM) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="bc5d7-124">成功または失敗を確認する</span><span class="sxs-lookup"><span data-stu-id="bc5d7-124">Determining success or failure</span></span>

<span data-ttu-id="bc5d7-125">2つのテストユーザーがモバイルサービスを使用してインスタントメッセージを交換できる場合、Test-CsMcxP2PIM はテスト結果の成功を返します。</span><span class="sxs-lookup"><span data-stu-id="bc5d7-125">If the two test users can exchange instant messages by using the mobility service then Test-CsMcxP2PIM will return test result Success:</span></span>

<span data-ttu-id="bc5d7-126">ターゲット Fqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="bc5d7-126">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="bc5d7-127">ターゲット Uri: http://atl-cs-001.litwareinc.com:443/mcx</span><span class="sxs-lookup"><span data-stu-id="bc5d7-127">Target Uri : http://atl-cs-001.litwareinc.com:443/mcx</span></span>

<span data-ttu-id="bc5d7-128">結果: 成功</span><span class="sxs-lookup"><span data-stu-id="bc5d7-128">Result : Success</span></span>

<span data-ttu-id="bc5d7-129">待ち時間: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="bc5d7-129">Latency : 00:00:00</span></span>

<span data-ttu-id="bc5d7-130">エラーメッセージ:</span><span class="sxs-lookup"><span data-stu-id="bc5d7-130">Error Message :</span></span>

<span data-ttu-id="bc5d7-131">診断</span><span class="sxs-lookup"><span data-stu-id="bc5d7-131">Diagnosis :</span></span>

<span data-ttu-id="bc5d7-132">テストが失敗した場合、結果は "失敗" に設定され、詳細なエラーメッセージと診断が表示されます。</span><span class="sxs-lookup"><span data-stu-id="bc5d7-132">If the test fails then the Result will be set to Failure and a detailed error message and diagnosis will be displayed:</span></span>

<span data-ttu-id="bc5d7-133">ターゲット Fqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="bc5d7-133">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="bc5d7-134">ターゲット Uri: https://atl-cs-001.litwareinc.com:443/mcx</span><span class="sxs-lookup"><span data-stu-id="bc5d7-134">Target Uri : https://atl-cs-001.litwareinc.com:443/mcx</span></span>

<span data-ttu-id="bc5d7-135">結果: エラー</span><span class="sxs-lookup"><span data-stu-id="bc5d7-135">Result : Failure</span></span>

<span data-ttu-id="bc5d7-136">待ち時間: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="bc5d7-136">Latency : 00:00:00</span></span>

<span data-ttu-id="bc5d7-137">エラーメッセージ: Web-Ticket サービスの応答が受信されませんでした。</span><span class="sxs-lookup"><span data-stu-id="bc5d7-137">Error Message : No response received for Web-Ticket service.</span></span>

<span data-ttu-id="bc5d7-138">内部例外: HHTP 要求は、で許可されていません。</span><span class="sxs-lookup"><span data-stu-id="bc5d7-138">Inner Exception:The HHTP request is unauthorized with</span></span>

<span data-ttu-id="bc5d7-139">クライアントネゴシエーションスキーム ' Ntlm '。</span><span class="sxs-lookup"><span data-stu-id="bc5d7-139">client negotiation scheme 'Ntlm'.</span></span> <span data-ttu-id="bc5d7-140">認証</span><span class="sxs-lookup"><span data-stu-id="bc5d7-140">The authentication</span></span>

<span data-ttu-id="bc5d7-141">サーバーから受信したヘッダーは、"Negotiate、NTLM" でした。</span><span class="sxs-lookup"><span data-stu-id="bc5d7-141">header received from the server was 'Negotiate,NTLM'.</span></span>

<span data-ttu-id="bc5d7-142">内部例外: リモートサーバーからエラーが返されました:</span><span class="sxs-lookup"><span data-stu-id="bc5d7-142">Inner Exception:The remote server returned an error:</span></span>

<span data-ttu-id="bc5d7-143">(401) 承認されていません。</span><span class="sxs-lookup"><span data-stu-id="bc5d7-143">(401) Unauthorized.</span></span>

<span data-ttu-id="bc5d7-144">診断</span><span class="sxs-lookup"><span data-stu-id="bc5d7-144">Diagnosis :</span></span>

<span data-ttu-id="bc5d7-145">内部診断: X-MS---------------------------</span><span class="sxs-lookup"><span data-stu-id="bc5d7-145">Inner Diagnosis:X-MS-server-Fqdb : atl-cs-</span></span>

<span data-ttu-id="bc5d7-146">001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="bc5d7-146">001.litwareinc.com</span></span>

<span data-ttu-id="bc5d7-147">Cache-Control: private</span><span class="sxs-lookup"><span data-stu-id="bc5d7-147">Cache-Control : private</span></span>

<span data-ttu-id="bc5d7-148">Content-type: text/html;charset = utf-8。</span><span class="sxs-lookup"><span data-stu-id="bc5d7-148">Content-Type : text/html; charset=utf-8.</span></span>

<span data-ttu-id="bc5d7-149">サーバー: Microsoft-IIS/8.5</span><span class="sxs-lookup"><span data-stu-id="bc5d7-149">Server : Microsoft-IIS/8.5</span></span>

<span data-ttu-id="bc5d7-150">WWW-Authenticate: Negotiate、NTLM</span><span class="sxs-lookup"><span data-stu-id="bc5d7-150">WWW-Authenticate : Negotiate,NTLM</span></span>

<span data-ttu-id="bc5d7-151">X-電力: ASP.NET</span><span class="sxs-lookup"><span data-stu-id="bc5d7-151">X-Powered-By : ASP.NET</span></span>

<span data-ttu-id="bc5d7-152">X-コンテンツタイプ-オプション: nosniff</span><span class="sxs-lookup"><span data-stu-id="bc5d7-152">X-Content-Type-Options : nosniff</span></span>

<span data-ttu-id="bc5d7-153">日付: 水曜日、28年5月 19:16:05 2014 日</span><span class="sxs-lookup"><span data-stu-id="bc5d7-153">Date : Wed, 28 May 2014 19:16:05 GMT</span></span>

<span data-ttu-id="bc5d7-154">Content-length: 6305</span><span class="sxs-lookup"><span data-stu-id="bc5d7-154">Content-Length : 6305</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="bc5d7-155">テストに失敗した可能性がある理由</span><span class="sxs-lookup"><span data-stu-id="bc5d7-155">Reasons why the test might have failed</span></span>

<span data-ttu-id="bc5d7-156">Test-CsMcxP2PIM が失敗した場合は、まずモビリティサービスが起動して実行されていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bc5d7-156">If Test-CsMcxP2PIM fails your first step should be to verify that the mobility service is up and running.</span></span> <span data-ttu-id="bc5d7-157">この操作を行うには、web ブラウザーを使用して、Lync Server プールのモビリティサービスの URL にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="bc5d7-157">That can be done by using a web browser to verify that the mobility service URL for your Lync Server pool can be accessed.</span></span> <span data-ttu-id="bc5d7-158">たとえば、次のコマンドは、プール atl-cs-001.litwareinc.com の URL を確認します。</span><span class="sxs-lookup"><span data-stu-id="bc5d7-158">For example, this command verifies the URL for the pool atl-cs-001.litwareinc.com:</span></span>

    https://atl-cs-001.litwareinc.com/mcx/mcxservice.svc

<span data-ttu-id="bc5d7-159">モバイルサービスが実行されているように見える場合は、2つのテストユーザーが有効な Lync Server アカウントを持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="bc5d7-159">If the mobility service seems to be running then verify that your two test users have valid Lync Server accounts.</span></span> <span data-ttu-id="bc5d7-160">次のようなコマンドを使用して、アカウント情報を取得できます。</span><span class="sxs-lookup"><span data-stu-id="bc5d7-160">You can retrieve account information by using a command similar to this:</span></span>

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object Enabled

<span data-ttu-id="bc5d7-161">Enabled プロパティが True と等しくない場合、またはコマンドが失敗した場合は、ユーザーが有効な Lync Server アカウントを持っていないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="bc5d7-161">If the Enabled property is not equal to True or if the command fails, that means that the user does not have a valid Lync Server account.</span></span>

<span data-ttu-id="bc5d7-162">また、ユーザーがモビリティを有効にしていることも確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bc5d7-162">You should also verify that the user is enabled for mobility.</span></span> <span data-ttu-id="bc5d7-163">そのためには、まず、アカウントに割り当てられているモビリティポリシーを特定します。</span><span class="sxs-lookup"><span data-stu-id="bc5d7-163">To do that, first determine the mobility policy that is assigned to the account:</span></span>

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object MobilityPolicy

<span data-ttu-id="bc5d7-164">ポリシー名がわかったら、Get-CsMobilityPolicy コマンドレットを使用して、問題のポリシー (たとえば、RedmondMobilityPolicy) に EnableMobility プロパティが True に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="bc5d7-164">After you know the policy name, use the Get-CsMobilityPolicy cmdlet to verify that the policy in question (for example, RedmondMobilityPolicy) has the EnableMobility property set to True:</span></span>

    Get-CsMobilityPolicy -Identity "RedmondMobilityPolicy"

<span data-ttu-id="bc5d7-165">認証ヘッダーを含むエラーメッセージが表示された場合は、それは、有効なユーザーアカウントを指定していないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="bc5d7-165">If you receive an error message with authentication headers, that often means that you have not specified a valid user account.</span></span> <span data-ttu-id="bc5d7-166">ユーザー名とパスワードを確認して、もう一度テストしてみてください。</span><span class="sxs-lookup"><span data-stu-id="bc5d7-166">Verify the user name and password and then try the test again.</span></span> <span data-ttu-id="bc5d7-167">ユーザーアカウントが有効であると確信できる場合は、Get-CsWebServiceConfiguration コマンドレットを使用して、UseWindowsAuth プロパティの値を確認します。</span><span class="sxs-lookup"><span data-stu-id="bc5d7-167">If you are convinced that the user account is valid, then use the Get-CsWebServiceConfiguration cmdlet and check the value of the UseWindowsAuth property.</span></span> <span data-ttu-id="bc5d7-168">これにより、どの認証方法が組織で有効になっているかがわかります。モバイルサービスのトラブルシューティングのヒントについては、「ブログの投稿の [トラブルシューティング外部の Lync モバイル接続の問題のトラブルシューティング](https://blogs.technet.com/b/nexthop/archive/2012/02/21/troubleshooting-external-lync-mobility-connectivity-issues-step-by-step.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bc5d7-168">That will tell you which authentication methods are enabled in your organization.For more tips about how to troubleshoot the mobility service, see the blog post [Troubleshooting External Lync Mobility Connectivity Issues Step-by-Step](https://blogs.technet.com/b/nexthop/archive/2012/02/21/troubleshooting-external-lync-mobility-connectivity-issues-step-by-step.aspx).</span></span>

<span data-ttu-id="bc5d7-169"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bc5d7-169"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

