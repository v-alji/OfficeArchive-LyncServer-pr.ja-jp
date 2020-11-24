---
title: 'Lync Server 2013: Lync クライアント認証のテスト'
description: 'Lync Server 2013: Lync クライアント認証のテスト'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing Lync Client authentication
ms:assetid: e22114cb-4456-4e5f-93ab-51592c4a8209
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn689120(v=OCS.15)
ms:contentKeyID: 63969659
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 03694b7fd56d7847d8d493304b97af335d2a5b4d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398942"
---
# <a name="testing-lync-client-authentication-in-lync-server-2013"></a><span data-ttu-id="305ec-103">Lync Server 2013 での Lync クライアント認証のテスト</span><span class="sxs-lookup"><span data-stu-id="305ec-103">Testing Lync Client authentication in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="305ec-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="305ec-104">

<span> </span></span></span>

<span data-ttu-id="305ec-105">_**最終更新日:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="305ec-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="305ec-106">確認のスケジュール</span><span class="sxs-lookup"><span data-stu-id="305ec-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="305ec-107">[毎日]</span><span class="sxs-lookup"><span data-stu-id="305ec-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="305ec-108">テストツール</span><span class="sxs-lookup"><span data-stu-id="305ec-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="305ec-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="305ec-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="305ec-110">必要なアクセス許可</span><span class="sxs-lookup"><span data-stu-id="305ec-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="305ec-111">Lync Server 管理シェルを使用してローカルで実行する場合、ユーザーは RTCUniversalServerAdmins セキュリティグループのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="305ec-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="305ec-112">Windows PowerShell のリモートインスタンスを使って実行する場合は、Test-CsClientAuth コマンドレットを実行するためのアクセス許可を持つ RBAC の役割をユーザーに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="305ec-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsClientAuth cmdlet.</span></span> <span data-ttu-id="305ec-113">このコマンドレットを使うことができるすべての RBAC ロールの一覧を表示するには、Windows PowerShell プロンプトから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="305ec-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsClientAuth&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="305ec-114">説明</span><span class="sxs-lookup"><span data-stu-id="305ec-114">Description</span></span>

<span data-ttu-id="305ec-115">Test-CsClientAuth コマンドレットを使用すると、ユーザーがクライアント証明書を使って Lync サーバーにログオンできるかどうかを判断できます。また、Test-CsClientAuth コマンドレットを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="305ec-115">The Test-CsClientAuth cmdlet enables you to determine whether a user can log on to the Lync Server by using a client certificate, you can run the Test-CsClientAuth cmdlet.</span></span> <span data-ttu-id="305ec-116">テスト用の CsClientAuth を呼び出すと、コマンドレットは証明書プロビジョニングサービスに問い合わせ、指定されたユーザーのクライアント証明書のコピーをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="305ec-116">After calling Test-CsClientAuth, the cmdlet will contact the certificate provisioning service and download a copy of any client certificates for the specified user.</span></span> <span data-ttu-id="305ec-117">クライアント証明書を見つけてダウンロードできる場合、Test-CsClientAuth はその証明書を使用してログオンしようとします。</span><span class="sxs-lookup"><span data-stu-id="305ec-117">If a client certificate can be found and downloaded, Test-CsClientAuth will then attempt to log on by using that certificate.</span></span> <span data-ttu-id="305ec-118">ログオンが成功すると、Test-CsClientAuth はログオフし、テストが成功したことを報告します。</span><span class="sxs-lookup"><span data-stu-id="305ec-118">If logon succeeds, Test-CsClientAuth will log off and report that the test succeeded.</span></span> <span data-ttu-id="305ec-119">証明書が見つからないか、ダウンロードできない場合、またはコマンドレットがその証明書を使用してログオンできない場合は、テストが失敗したことが Test-CsClientAuth によって報告されます。</span><span class="sxs-lookup"><span data-stu-id="305ec-119">If a certificate cannot be found or downloaded, or if the cmdlet is unable to logon using that certificate, then Test-CsClientAuth will report that the test failed.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="305ec-120">テストの実行</span><span class="sxs-lookup"><span data-stu-id="305ec-120">Running the test</span></span>

<span data-ttu-id="305ec-121">Lync Server を有効にしているユーザーのアカウントを使用して、Test-CsClientAuth コマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="305ec-121">The Test-CsClientAuth cmdlet is run by using the account of any user who is enabled for Lync Server.</span></span> <span data-ttu-id="305ec-122">実際のユーザーアカウントを使用してこのチェックを実行するには、最初に、アカウント名とパスワードを含む Windows PowerShell 資格情報オブジェクトを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="305ec-122">To run this check using an actual user account, you must first create a Windows PowerShell credentials object that contains the account name and password.</span></span> <span data-ttu-id="305ec-123">次に、資格情報オブジェクトと、システムが Test CsClientAuth を呼び出すときにアカウントに割り当てられる SIP アドレスを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="305ec-123">You must then include that credentials object and the SIP address assigned to the account when the system calls Test-CsClientAuth:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsClientAuth -TargetFqdn "atl-cs-001.litwareinc.com"-UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

<span data-ttu-id="305ec-124">詳細については、「 [CsClientAuth のテスト](https://technet.microsoft.com/library/gg398712\(v=ocs.14\).aspx) コマンドレット」のヘルプドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="305ec-124">For more information, see the Help documentation for the [Test-CsClientAuth](https://technet.microsoft.com/library/gg398712\(v=ocs.14\).aspx) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="305ec-125">成功または失敗を確認する</span><span class="sxs-lookup"><span data-stu-id="305ec-125">Determining success or failure</span></span>

<span data-ttu-id="305ec-126">指定したユーザーがクライアント証明書を使って Lync サーバーにログオンできる場合は、次のような出力が返されます。これには、Result プロパティが Success とマークされてい **ます。**</span><span class="sxs-lookup"><span data-stu-id="305ec-126">If the specified user can log on to Lync Server by using a client certificate, you will receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="305ec-127">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="305ec-127">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="305ec-128">結果: 成功</span><span class="sxs-lookup"><span data-stu-id="305ec-128">Result : Success</span></span>

<span data-ttu-id="305ec-129">待ち時間:00:00: 06.8630376</span><span class="sxs-lookup"><span data-stu-id="305ec-129">Latency : 00:00:06.8630376</span></span>

<span data-ttu-id="305ec-130">誤差</span><span class="sxs-lookup"><span data-stu-id="305ec-130">Error :</span></span>

<span data-ttu-id="305ec-131">診断</span><span class="sxs-lookup"><span data-stu-id="305ec-131">Diagnosis :</span></span>

<span data-ttu-id="305ec-132">指定したユーザーがログオンできない場合、結果は失敗として表示され、エラーと診断のプロパティに追加情報が記録されます。</span><span class="sxs-lookup"><span data-stu-id="305ec-132">If the specified user can not log on, the Result will be shown as Failure and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="305ec-133">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="305ec-133">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="305ec-134">結果: エラー</span><span class="sxs-lookup"><span data-stu-id="305ec-134">Result : Failure</span></span>

<span data-ttu-id="305ec-135">待ち時間:00:00: 03.3645259</span><span class="sxs-lookup"><span data-stu-id="305ec-135">Latency : 00:00:03.3645259</span></span>

<span data-ttu-id="305ec-136">エラー: 指定されたユーザーの CS 証明書をダウンロードできませんでした。</span><span class="sxs-lookup"><span data-stu-id="305ec-136">Error : Could not download a CS Certificate for the given user.</span></span> <span data-ttu-id="305ec-137">かどうかを確認</span><span class="sxs-lookup"><span data-stu-id="305ec-137">Check if</span></span>

<span data-ttu-id="305ec-138">指定された uri と資格情報が正しい。</span><span class="sxs-lookup"><span data-stu-id="305ec-138">provided uri and credentials are correct.</span></span>

<span data-ttu-id="305ec-139">診断</span><span class="sxs-lookup"><span data-stu-id="305ec-139">Diagnosis :</span></span>

<span data-ttu-id="305ec-140">たとえば、前回の出力には、指定したユーザーに対して有効なクライアント証明書が見つからなかったため、テストが失敗したことが示されます。</span><span class="sxs-lookup"><span data-stu-id="305ec-140">For example, the previous output states that the test failed because a valid client certificate couldn't be located for the specified user.</span></span> <span data-ttu-id="305ec-141">次のようにコマンドを実行することで、ユーザーに発行されたクライアント証明書の一覧を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="305ec-141">You can return a list of the client certificates issued to a user by running a command as follows:</span></span>

    Get-CsClientCertificate -Identity "sip:kenmyer@litwareinc.com"

<span data-ttu-id="305ec-142">Test-CsClientAuth が失敗した場合は、Verbose パラメーターも含めて、テストを再実行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="305ec-142">If Test-CsClientAuth fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsClientAuth -TargetFqdn "atl-cs-001.litwareinc.com"-UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential -Verbose

<span data-ttu-id="305ec-143">Verbose パラメーターが含まれている場合、Test-CsClientAuth は、指定されたユーザーが Lync Server にログオンする機能を確認したときに実行された各操作のステップバイステップのアカウントを返します。</span><span class="sxs-lookup"><span data-stu-id="305ec-143">When the Verbose parameter is included, Test-CsClientAuth will return a step-by-step account of each action it tried when it checked the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="305ec-144">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="305ec-144">For example:</span></span>

<span data-ttu-id="305ec-145">次のユーザーの CS 証明書をダウンロードしようとしています: kenmyer@litwareinc.com endpoint: STEpid</span><span class="sxs-lookup"><span data-stu-id="305ec-145">Trying to download a CS certificate for User : kenmyer@litwareinc.com endpoint : STEpid</span></span>

<span data-ttu-id="305ec-146">Web サービスの url: https://atl-cs-001.litwareinc.com:443/CertProv/CertprovisioningService.svc</span><span class="sxs-lookup"><span data-stu-id="305ec-146">Web Service url : https://atl-cs-001.litwareinc.com:443/CertProv/CertprovisioningService.svc</span></span>

<span data-ttu-id="305ec-147">Web サービスから CS 証明書をダウンロードできませんでした。</span><span class="sxs-lookup"><span data-stu-id="305ec-147">Could not download a CS certificate from web service.</span></span>

<span data-ttu-id="305ec-148">調べ</span><span class="sxs-lookup"><span data-stu-id="305ec-148">CHECK:</span></span>

<span data-ttu-id="305ec-149">\- Web サービスの url が有効であり、web サービスが機能している</span><span class="sxs-lookup"><span data-stu-id="305ec-149">\- Web service url is valid and the web services are functional</span></span>

<span data-ttu-id="305ec-150">\-認証に PhoneNo Pin を使用している場合は、 \\ \\ ユーザーの uri と一致することを確認します。</span><span class="sxs-lookup"><span data-stu-id="305ec-150">\- If using PhoneNo\\\\Pin to authenticate, make sure they match the user uri</span></span>

<span data-ttu-id="305ec-151">\- NTLM Kerberos 認証を使用している場合は \\ 、有効な資格情報を指定していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="305ec-151">\- If using NTLM\\Kerberos auth, make sure you provided valid credentials</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="305ec-152">テストに失敗した可能性がある理由</span><span class="sxs-lookup"><span data-stu-id="305ec-152">Reasons why the test might have failed</span></span>

<span data-ttu-id="305ec-153">Test-CsClientAuth が失敗する可能性がある一般的な理由を次に示します。</span><span class="sxs-lookup"><span data-stu-id="305ec-153">Here are some common reasons why Test-CsClientAuth might fail:</span></span>

  - <span data-ttu-id="305ec-154">無効なユーザーアカウントが指定されました。</span><span class="sxs-lookup"><span data-stu-id="305ec-154">You specified a user account that was not valid.</span></span> <span data-ttu-id="305ec-155">次のようなコマンドを実行すると、ユーザーアカウントが存在するかどうかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="305ec-155">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="305ec-156">ユーザーアカウントは有効ですが、アカウントは現在 Lync Server に対して有効になっていません。</span><span class="sxs-lookup"><span data-stu-id="305ec-156">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="305ec-157">Lync Server でユーザーアカウントが有効になっていることを確認するには、次のようなコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="305ec-157">To verify that a user account is enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="305ec-158">Enabled プロパティが False に設定されている場合は、ユーザーが現在 Lync Server を有効にしていないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="305ec-158">If the Enabled property is set to False, that means that the user is currently not enabled for Lync Server.</span></span>

  - <span data-ttu-id="305ec-159">テストユーザーは、有効なクライアント証明書を持っていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="305ec-159">The test user might not have a valid client certificate.</span></span> <span data-ttu-id="305ec-160">次のようなコマンドを使用して、ユーザーに割り当てられているクライアント証明書に関する情報を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="305ec-160">You can return information about the client certificates assigned to a user by using a command similar to this:</span></span>
    
        Get-CsClientCertificate -Identity "sip:kenmyer@litwareinc.com"

<span data-ttu-id="305ec-161"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="305ec-161"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

