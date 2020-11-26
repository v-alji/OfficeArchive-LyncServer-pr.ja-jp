---
title: 'Lync Server 2013: アドレス帳の web クエリの検証'
description: 'Lync Server 2013: アドレス帳の web クエリを検証しています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Validating address book web query
ms:assetid: e6ae0a5a-e131-4cfe-9a33-6e611831072d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720925(v=OCS.15)
ms:contentKeyID: 63969662
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e73c39fc33f8d1851fc89d277333a94aaa137790
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438905"
---
# <a name="validating-address-book-web-query-in-lync-server-2013"></a><span data-ttu-id="3d02d-103">Lync Server 2013 でのアドレス帳 web クエリの検証</span><span class="sxs-lookup"><span data-stu-id="3d02d-103">Validating address book web query in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3d02d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3d02d-104">

<span> </span></span></span>

<span data-ttu-id="3d02d-105">_**最終更新日:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="3d02d-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3d02d-106">確認のスケジュール</span><span class="sxs-lookup"><span data-stu-id="3d02d-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="3d02d-107">[毎日]</span><span class="sxs-lookup"><span data-stu-id="3d02d-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d02d-108">テストツール</span><span class="sxs-lookup"><span data-stu-id="3d02d-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="3d02d-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="3d02d-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d02d-110">必要なアクセス許可</span><span class="sxs-lookup"><span data-stu-id="3d02d-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="3d02d-111">Lync Server 管理シェルを使用してローカルで実行する場合、ユーザーは RTCUniversalServerAdmins セキュリティグループのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d02d-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="3d02d-112">Windows PowerShell のリモートインスタンスを使って実行する場合は、Test-CsAddressBookWebQuery コマンドレットを実行するためのアクセス許可を持つ RBAC の役割をユーザーに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d02d-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsAddressBookWebQuery cmdlet.</span></span> <span data-ttu-id="3d02d-113">このコマンドレットを使うことができるすべての RBAC ロールの一覧を表示するには、Windows PowerShell プロンプトから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="3d02d-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsAddressBookWebQuery&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="3d02d-114">説明</span><span class="sxs-lookup"><span data-stu-id="3d02d-114">Description</span></span>

<span data-ttu-id="3d02d-115">[Test-CsAddressBookWebQuery コマンドレットを使用すると、管理者は、ユーザーがアドレス帳 Web クエリサービスを使用して特定の連絡先を検索できることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="3d02d-115">The Test-CsAddressBookWebQuery cmdlet enables administrators to verify that users can use the Address Book Web Query service to search for a specific contact.</span></span> <span data-ttu-id="3d02d-116">このコマンドレットを実行すると、Test-CsAddressBookWebQuery は最初に Web チケットサービスに接続して、認証されるようになります。</span><span class="sxs-lookup"><span data-stu-id="3d02d-116">When you run the cmdlet, Test-CsAddressBookWebQuery will first connect to the Web Ticket service to be authenticated.</span></span> <span data-ttu-id="3d02d-117">認証が成功すると、コマンドレットはアドレス帳 Web クエリサービスに接続し、指定された連絡先を検索します。</span><span class="sxs-lookup"><span data-stu-id="3d02d-117">If authentication is successful, the cmdlet will then connect to the Address Book Web Query service and search for the specified contact.</span></span> <span data-ttu-id="3d02d-118">その連絡先が見つかった場合、コマンドレットはローカルコンピューターにその情報を返します。</span><span class="sxs-lookup"><span data-stu-id="3d02d-118">If that contact is found, the cmdlet will attempt to return that information to the local computer.</span></span> <span data-ttu-id="3d02d-119">テストは、すべての手順が完了した場合にのみ成功としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="3d02d-119">The test will be marked a success only if all those steps can be completed.</span></span>

<span data-ttu-id="3d02d-120">詳細については、「 [テスト-CsAddressBookWebQuery](https://docs.microsoft.com/powershell/module/skype/Test-CsAddressBookWebQuery) コマンドレットのヘルプドキュメント」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3d02d-120">For more information, see the Help documentation for the [Test-CsAddressBookWebQuery](https://docs.microsoft.com/powershell/module/skype/Test-CsAddressBookWebQuery) cmdlet.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="3d02d-121">テストの実行</span><span class="sxs-lookup"><span data-stu-id="3d02d-121">Running the test</span></span>

<span data-ttu-id="3d02d-122">Test-CsAddressBookWebQuery コマンドレットを実行するには、事前に定義されたテストアカウント (「Lync Server のテストを実行するためのテストアカウントをセットアップする」を参照) を使用するか、Lync Server を有効にしているユーザーのアカウントを使用します。</span><span class="sxs-lookup"><span data-stu-id="3d02d-122">The Test-CsAddressBookWebQuery cmdlet can be run using either a preconfigured test account (see Setting Up Test Accounts for Running Lync Server Tests) or the account of any user who is enabled for Lync Server.</span></span> <span data-ttu-id="3d02d-123">テストアカウントを使用してこのチェックを実行するには、Lync Server プールの FQDN と、検索のターゲットとして機能しているユーザーの SIP アドレスを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d02d-123">To run this check using a test account, you just have to specify the FQDN of the Lync Server pool and the SIP address of the user acting as the target of the search.</span></span> <span data-ttu-id="3d02d-124">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="3d02d-124">For example:</span></span>

    Test-CsAddressBookWebQuery -TargetFqdn "atl-cs-001.litwareinc.com" -TargetSipAddress "sip:davidlongmire@litwareinc.com"

<span data-ttu-id="3d02d-125">実際のユーザーアカウントを使用してこのチェックを実行するには、有効なユーザー名とパスワードを含む Windows PowerShell 資格情報オブジェクトを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d02d-125">To run this check using an actual user account, you must create a Windows PowerShell credentials object that contains a valid user name and password.</span></span> <span data-ttu-id="3d02d-126">次に、コードが Test-CsAddressBookWebQuery を呼び出したときに、アカウントに割り当てられている資格情報オブジェクトと SIP アドレスを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d02d-126">You must then include that credentials object and the SIP address assigned to the account when the code calls Test-CsAddressBookWebQuery:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsAddressBookWebQuery -TargetFqdn "atl-cs-001.litwareinc.com" -TargetSipAddress "sip:davidlongmire@litwareinc.com" -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

<span data-ttu-id="3d02d-127">詳細については、「 [テスト-CsAddressBookWebQuery](https://docs.microsoft.com/powershell/module/skype/Test-CsAddressBookWebQuery) コマンドレットのヘルプドキュメント」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3d02d-127">For more information, see the Help documentation for the [Test-CsAddressBookWebQuery](https://docs.microsoft.com/powershell/module/skype/Test-CsAddressBookWebQuery) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="3d02d-128">成功または失敗を確認する</span><span class="sxs-lookup"><span data-stu-id="3d02d-128">Determining success or failure</span></span>

<span data-ttu-id="3d02d-129">指定したユーザーがアドレス帳サービスに接続し、ターゲットユーザーアドレスを取得できる場合は、次のような出力が返されます。これは、Success とマークされた Result プロパティによって返されます。</span><span class="sxs-lookup"><span data-stu-id="3d02d-129">If the specified user can connect to the Address Book Service and retrieve the targeted user address, you'll return output similar to this with the Result property marked as Success:</span></span>

<span data-ttu-id="3d02d-130">TargetUri : https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span><span class="sxs-lookup"><span data-stu-id="3d02d-130">TargetUri : https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span></span>

<span data-ttu-id="3d02d-131">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="3d02d-131">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="3d02d-132">結果: 成功</span><span class="sxs-lookup"><span data-stu-id="3d02d-132">Result : Success</span></span>

<span data-ttu-id="3d02d-133">待ち時間:00:00: 06.2611356</span><span class="sxs-lookup"><span data-stu-id="3d02d-133">Latency : 00:00:06.2611356</span></span>

<span data-ttu-id="3d02d-134">誤差</span><span class="sxs-lookup"><span data-stu-id="3d02d-134">Error :</span></span>

<span data-ttu-id="3d02d-135">診断</span><span class="sxs-lookup"><span data-stu-id="3d02d-135">Diagnosis :</span></span>

<span data-ttu-id="3d02d-136">指定したユーザーが接続できない場合、またはターゲットのユーザーアドレスを取得できない場合は、結果がエラーとして表示され、エラーと診断のプロパティに追加情報が記録されます。</span><span class="sxs-lookup"><span data-stu-id="3d02d-136">If the specified user can't connect or if the target user address cannot be retrieved, then the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="3d02d-137">TargetUri : https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span><span class="sxs-lookup"><span data-stu-id="3d02d-137">TargetUri : https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span></span>

<span data-ttu-id="3d02d-138">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="3d02d-138">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="3d02d-139">結果: エラー</span><span class="sxs-lookup"><span data-stu-id="3d02d-139">Result : Failure</span></span>

<span data-ttu-id="3d02d-140">待ち時間: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="3d02d-140">Latency : 00:00:00</span></span>

<span data-ttu-id="3d02d-141">エラー: アドレス帳 Web サービスの要求は応答コードで失敗しました</span><span class="sxs-lookup"><span data-stu-id="3d02d-141">Error : Address Book Web service request has failed with response code</span></span>

<span data-ttu-id="3d02d-142">NoEntryFound。</span><span class="sxs-lookup"><span data-stu-id="3d02d-142">NoEntryFound.</span></span>

<span data-ttu-id="3d02d-143">診断</span><span class="sxs-lookup"><span data-stu-id="3d02d-143">Diagnosis :</span></span>

<span data-ttu-id="3d02d-144">前の出力では、ターゲットユーザーが見つからなかったため、テストが失敗したことが示されます。</span><span class="sxs-lookup"><span data-stu-id="3d02d-144">The previous output states that the test failed because the target user couldn't be found.</span></span> <span data-ttu-id="3d02d-145">次のようなコマンドを実行すると、有効な SIP アドレスが Test-CsAddressBookWebQuery に渡されたかどうかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="3d02d-145">You can determine whether or not a valid SIP address was passed to Test-CsAddressBookWebQuery by running a command similar to the following:</span></span>

    Get-CsUser | Where-Object {$_.SipAddress -eq "sip:davidlongmire@litwareinc.com"

<span data-ttu-id="3d02d-146">Test-CsAddressBookWebQuery が失敗した場合は、Verbose パラメーターも含めて、テストを再実行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="3d02d-146">If Test-CsAddressBookWebQuery fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsAddressBookWebQuery -TargetFqdn "atl-cs-001.litwareinc.com" -TargetSipAddress "sip:davidlongmire@litwareinc.com" -Verbose

<span data-ttu-id="3d02d-147">Verbose パラメーターが含まれている場合、Test-CsAddressBookWebQuery は、指定されたユーザーが Lync Server にログオンする機能を確認するときに、試行した各操作のステップバイステップのアカウントを返します。</span><span class="sxs-lookup"><span data-stu-id="3d02d-147">When the Verbose parameter is included, Test-CsAddressBookWebQuery will return a step-by-step account of each action it tried while checking the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="3d02d-148">たとえば、次の出力は、Test-CsAddressBookWebQuery がアドレス帳サービスに接続できたが、ターゲット SIP アドレスを見つけることができなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="3d02d-148">For example, this output indicates that Test-CsAddressBookWebQuery was able to connect to the Address Book Service, but was not able to locate the target SIP address:</span></span>

<span data-ttu-id="3d02d-149">' QueryAddressBookWebService ' アクティビティが開始されました。</span><span class="sxs-lookup"><span data-stu-id="3d02d-149">'QueryAddressBookWebService' activity started.</span></span>

<span data-ttu-id="3d02d-150">アドレス帳 Web クエリサービスを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3d02d-150">Calling Address Book Web Query Service.</span></span> <span data-ttu-id="3d02d-151">ABWS URL =</span><span class="sxs-lookup"><span data-stu-id="3d02d-151">ABWS URL =</span></span>

https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc

<span data-ttu-id="3d02d-152">アドレス帳のクエリ例外: アドレス帳 Web サービスの要求は、応答コード NoEntryFound で失敗しました。</span><span class="sxs-lookup"><span data-stu-id="3d02d-152">Address book query exception : Address Book Web service request has failed with response code NoEntryFound.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="3d02d-153">テストに失敗した可能性がある理由</span><span class="sxs-lookup"><span data-stu-id="3d02d-153">Reasons Why the Test Might Have Failed</span></span>

<span data-ttu-id="3d02d-154">Test-CsAddressBookWebQuery が失敗する可能性がある一般的な理由を次に示します。</span><span class="sxs-lookup"><span data-stu-id="3d02d-154">Here are some common reasons why Test-CsAddressBookWebQuery might fail:</span></span>

  - <span data-ttu-id="3d02d-155">無効なユーザアカウントを指定しました。</span><span class="sxs-lookup"><span data-stu-id="3d02d-155">You specified an invalid user account.</span></span> <span data-ttu-id="3d02d-156">次のようなコマンドを実行すると、ユーザーアカウントが存在するかどうかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="3d02d-156">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="3d02d-157">ユーザーアカウントは有効ですが、アカウントは現在 Lync Server では有効になっていません。</span><span class="sxs-lookup"><span data-stu-id="3d02d-157">The user account is valid, but the account is not currently enabled for Lync Server.</span></span> <span data-ttu-id="3d02d-158">Lync Server のユーザーアカウントが有効になっていることを確認するには、次のようなコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="3d02d-158">To verify that a user account has been enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="3d02d-159">Enabled プロパティが False に設定されている場合は、ユーザーが現在 Lync Server に対して有効になっていないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="3d02d-159">If the Enabled property is set to False that means that the user is not currently enabled for Lync Server.</span></span>

  - <span data-ttu-id="3d02d-160">ターゲットユーザーがアドレス帳に登録されていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3d02d-160">The target user might not be in the Address Book.</span></span>

  - <span data-ttu-id="3d02d-161">アドレス帳が完全に更新されて複製されていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3d02d-161">The Address Book might not have fully updated and replicated.</span></span> <span data-ttu-id="3d02d-162">次のコマンドを実行して、組織内のすべてのアドレス帳サーバーを強制的に更新することができます。</span><span class="sxs-lookup"><span data-stu-id="3d02d-162">You can force an update of all the Address Book Servers in your organization by running the following command:</span></span>
    
        Update-CsAddressBook

<span data-ttu-id="3d02d-163"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3d02d-163"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

