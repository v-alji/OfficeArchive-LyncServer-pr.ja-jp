---
title: 'Lync Server 2013: グループ展開を使用するためのテスト機能'
description: 'Lync Server 2013: グループ展開を使用するためのテスト機能。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing ability to employ group expansion
ms:assetid: 9b0fc954-6f9c-411a-ab32-94ebabc42de2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743836(v=OCS.15)
ms:contentKeyID: 63969634
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6267bc2099fc420c5c57e1ef80f4bf4491334938
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441110"
---
# <a name="testing-ability-to-employ-group-expansion-in-lync-server-2013"></a><span data-ttu-id="84e99-103">Lync Server 2013 でグループ展開を使用するためのテスト機能</span><span class="sxs-lookup"><span data-stu-id="84e99-103">Testing ability to employ group expansion in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="84e99-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="84e99-104">

<span> </span></span></span>

<span data-ttu-id="84e99-105">_**最終更新日:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="84e99-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="84e99-106">確認のスケジュール</span><span class="sxs-lookup"><span data-stu-id="84e99-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="84e99-107">[毎日]</span><span class="sxs-lookup"><span data-stu-id="84e99-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84e99-108">テストツール</span><span class="sxs-lookup"><span data-stu-id="84e99-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="84e99-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="84e99-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84e99-110">必要なアクセス許可</span><span class="sxs-lookup"><span data-stu-id="84e99-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="84e99-111">Lync Server 管理シェルを使用してローカルで実行する場合、ユーザーは RTCUniversalServerAdmins セキュリティグループのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="84e99-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="84e99-112">Windows PowerShell のリモートインスタンスを使って実行する場合は、Test-CsGroupExpansion コマンドレットを実行するためのアクセス許可を持つ RBAC の役割をユーザーに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="84e99-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsGroupExpansion cmdlet.</span></span> <span data-ttu-id="84e99-113">このコマンドレットを使うことができるすべての RBAC ロールの一覧を表示するには、Windows PowerShell プロンプトから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="84e99-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsGroupExpansion&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="84e99-114">説明</span><span class="sxs-lookup"><span data-stu-id="84e99-114">Description</span></span>

<span data-ttu-id="84e99-115">Test-CsGroupExpansion コマンドレットを使用すると、グループの展開が組織内で機能しているかどうかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="84e99-115">The Test-CsGroupExpansion cmdlet lets you determine whether group expansion is working within your organization.</span></span> <span data-ttu-id="84e99-116">グループの拡張が有効になっている場合、ユーザーは配布グループを連絡先として構成します。</span><span class="sxs-lookup"><span data-stu-id="84e99-116">When group expansion is enabled, users configure distribution groups as a contact.</span></span> <span data-ttu-id="84e99-117">つまり、これらのユーザーは、グループの個々のメンバーではなく、グループにメッセージをアドレス指定して、すべてのグループメンバーに同じインスタントメッセージを送信することができます。</span><span class="sxs-lookup"><span data-stu-id="84e99-117">That means that those users can then send the same instant message to all the group members by addressing the message to the group instead of to individual members of that group.</span></span> <span data-ttu-id="84e99-118">グループ展開では、すべてのグループメンバーとその現在の状態をすばやく簡単に表示できます。</span><span class="sxs-lookup"><span data-stu-id="84e99-118">Group expansion enables you to quickly and easily view all the group members and their current status.</span></span>

<span data-ttu-id="84e99-119">Test-CsGroupExpansion コマンドレットを使用して、グループのメールアドレスを使用して Active Directory 配布グループを指定します。</span><span class="sxs-lookup"><span data-stu-id="84e99-119">With the Test-CsGroupExpansion cmdlet, you specify an Active Directory distribution group by using the group’s email address.</span></span> <span data-ttu-id="84e99-120">次に、グループの展開を使用してグループメンバーシップを取得し、取得したリストと、指定したグループメールアドレスのメンバーシップを比較します Test-CsGroupExpansion。</span><span class="sxs-lookup"><span data-stu-id="84e99-120">Test-CsGroupExpansion then uses group expansion to retrieve the group membership and compare the retrieved list to the membership of the group email address that you supplied.</span></span> <span data-ttu-id="84e99-121">2つのリストが一致する場合、グループの展開は正常に機能しています。</span><span class="sxs-lookup"><span data-stu-id="84e99-121">If the two lists match, then group expansion is working correctly.</span></span> <span data-ttu-id="84e99-122">グループの展開をテストするには、サービス自体をテストするか、関連付けられた web サービスをテストするという2つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="84e99-122">Note that you can test group expansion in two ways: by testing the service itself or by testing the associated web service.</span></span>

<span data-ttu-id="84e99-123">詳細については、「 [CsGroupExpansion](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupExpansion) コマンドレットのヘルプドキュメント」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="84e99-123">For more information, see the Help documentation for the [Test-CsGroupExpansion](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupExpansion) cmdlet.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="84e99-124">テストの実行</span><span class="sxs-lookup"><span data-stu-id="84e99-124">Running the test</span></span>

<span data-ttu-id="84e99-125">Test-CsGroupExpansion コマンドレットを実行するには、事前に定義されたテストアカウント (「Lync Server のテストを実行するためのテストアカウントをセットアップする」を参照) を使用するか、Lync Server を有効にしているユーザーのアカウントを使用します。</span><span class="sxs-lookup"><span data-stu-id="84e99-125">The Test-CsGroupExpansion cmdlet can be run using either a preconfigured test account (see Setting Up Test Accounts for Running Lync Server Tests) or the account of any user who was enabled for Lync Server.</span></span> <span data-ttu-id="84e99-126">テストアカウントを使用してこのチェックを実行するには、テスト対象の Lync Server プールの FQDN と、有効な配布グループのメールアドレスを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="84e99-126">To run this check using a test account, you just have to specify the FQDN of the Lync Server pool being tested and the email address for a valid distribution group.</span></span> <span data-ttu-id="84e99-127">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="84e99-127">For example:</span></span>

    Test-CsGroupExpansion -TargetFqdn "atl-cs-001.litwareinc.com" -GroupEmailAddress "Sales@litwareinc.com"

<span data-ttu-id="84e99-128">実際のユーザーアカウントを使用してこのチェックを実行するには、まず、アカウント名とパスワードを含む Lync Server 資格情報オブジェクトを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="84e99-128">To run this check using an actual user account, you must first create a Lync Server credentials object that contains the account name and password.</span></span> <span data-ttu-id="84e99-129">次に、資格情報オブジェクトと、システムによってテスト CsGroupExpansion が呼び出されたときにアカウントに割り当てられる SIP アドレスを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="84e99-129">You must then include that credentials object and the SIP address assigned to the account when the system calls Test-CsGroupExpansion:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsGroupExpansion -TargetFqdn "atl-cs-001.litwareinc.com" -GroupEmailAddress "Sales@litwareinc.com" -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

<span data-ttu-id="84e99-130">詳細については、「 [CsGroupExpansion](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupExpansion) コマンドレットのヘルプドキュメント」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="84e99-130">For more information, see the Help documentation for the [Test-CsGroupExpansion](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupExpansion) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="84e99-131">成功または失敗を確認する</span><span class="sxs-lookup"><span data-stu-id="84e99-131">Determining success or failure</span></span>

<span data-ttu-id="84e99-132">指定したユーザーがグループ拡張を使用できる場合は、次のような結果として、Success とマークされた Result プロパティが表示され **ます。**</span><span class="sxs-lookup"><span data-stu-id="84e99-132">If the specified user can use group expansion, you'll receive output similar to this with the Result property marked as **Success:**</span></span>

<span data-ttu-id="84e99-133">TargetUri : https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span><span class="sxs-lookup"><span data-stu-id="84e99-133">TargetUri : https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span></span>

<span data-ttu-id="84e99-134">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="84e99-134">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="84e99-135">結果: 成功</span><span class="sxs-lookup"><span data-stu-id="84e99-135">Result : Success</span></span>

<span data-ttu-id="84e99-136">待ち時間:00:00: 01.1234976</span><span class="sxs-lookup"><span data-stu-id="84e99-136">Latency : 00:00:01.1234976</span></span>

<span data-ttu-id="84e99-137">誤差</span><span class="sxs-lookup"><span data-stu-id="84e99-137">Error :</span></span>

<span data-ttu-id="84e99-138">診断</span><span class="sxs-lookup"><span data-stu-id="84e99-138">Diagnosis :</span></span>

<span data-ttu-id="84e99-139">指定したユーザーがグループの展開を使用できない場合は、結果がエラーとして表示され、エラーと診断のプロパティに追加情報が記録されます。</span><span class="sxs-lookup"><span data-stu-id="84e99-139">If the specified user can't use group expansion, then the Result will be shown as Failure and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="84e99-140">TargetUri : https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span><span class="sxs-lookup"><span data-stu-id="84e99-140">TargetUri : https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span></span>

<span data-ttu-id="84e99-141">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="84e99-141">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="84e99-142">結果: エラー</span><span class="sxs-lookup"><span data-stu-id="84e99-142">Result : Failure</span></span>

<span data-ttu-id="84e99-143">待ち時間: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="84e99-143">Latency : 00:00:00</span></span>

<span data-ttu-id="84e99-144">誤差</span><span class="sxs-lookup"><span data-stu-id="84e99-144">Error :</span></span>

<span data-ttu-id="84e99-145">診断</span><span class="sxs-lookup"><span data-stu-id="84e99-145">Diagnosis :</span></span>

<span data-ttu-id="84e99-146">Test-CsGroupExpansion: エンドポイントは登録できませんでした。</span><span class="sxs-lookup"><span data-stu-id="84e99-146">Test-CsGroupExpansion : The endpoint was unable to register.</span></span> <span data-ttu-id="84e99-147">具体的な理由については、「エラーコード」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="84e99-147">See the ErrorCode for specific reason.</span></span>

<span data-ttu-id="84e99-148">以前の出力では、指定されたユーザーが Lync Server に登録できなかったため、テストが失敗したことが示されます。</span><span class="sxs-lookup"><span data-stu-id="84e99-148">The previous output states that the test failed because the specified user was unable to register with Lync Server.</span></span> <span data-ttu-id="84e99-149">これは通常、テストアカウントが存在しないか、Lync Server に対して有効になっていない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="84e99-149">This will typically occur if the test account does not exist or has not enabled for Lync Server.</span></span> <span data-ttu-id="84e99-150">アカウントが存在するかどうかを確認し、次のようなコマンドを実行して、nm-ocs-14-3 のアカウントが有効になっているかどうかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="84e99-150">You can verify that the account exists, and determine whether or not the account has been enabled for nm-ocs-14-3rd by running a command similar to the following:</span></span>

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object SipAddress, Enabled

<span data-ttu-id="84e99-151">Test-CsGroupExpansion が失敗した場合は、Verbose パラメーターも含めて、テストを再実行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="84e99-151">If Test-CsGroupExpansion fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsGroupExpansion -TargetFqdn "atl-cs-001.litwareinc.com" -GroupEmailAddress "Sales@litwareinc.com" -Verbose

<span data-ttu-id="84e99-152">Verbose パラメーターが含まれている場合 Test-CsGroupExpansion は、指定されたユーザーが Lync Server にログオンする機能を確認したときに実行された各操作のステップバイステップのアカウントを返します。</span><span class="sxs-lookup"><span data-stu-id="84e99-152">When the Verbose parameter is included Test-CsGroupExpansion will return a step-by-step account of each action it tried when it checked the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="84e99-153">たとえば、次の出力は、指定された配布グループが見つからなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="84e99-153">For example, this output indicates that the specified distribution group couldn't be found:</span></span>

<span data-ttu-id="84e99-154">Web チケットを取得しようとしています。</span><span class="sxs-lookup"><span data-stu-id="84e99-154">Trying to get web ticket.</span></span>

<span data-ttu-id="84e99-155">Web サービスの url: https://atl-cs-001.litwareinc.com:443/WebTicket/WebTicketService.svc</span><span class="sxs-lookup"><span data-stu-id="84e99-155">Web Service url : https://atl-cs-001.litwareinc.com:443/WebTicket/WebTicketService.svc</span></span>

<span data-ttu-id="84e99-156">NTLM/Kerb auth を使用しています。</span><span class="sxs-lookup"><span data-stu-id="84e99-156">Using NTLM/Kerb auth.</span></span>

<span data-ttu-id="84e99-157">GetWebTicketActivity が完了しました。</span><span class="sxs-lookup"><span data-stu-id="84e99-157">GetWebTicketActivity completed.</span></span>

<span data-ttu-id="84e99-158">' VerifyDistributionList ' アクティビティが開始されました。</span><span class="sxs-lookup"><span data-stu-id="84e99-158">'VerifyDistributionList' activity started.</span></span>

<span data-ttu-id="84e99-159">DLX Web サービスの応答状態: NotFound。</span><span class="sxs-lookup"><span data-stu-id="84e99-159">DLX Web Service Response Status is: NotFound.</span></span>

<span data-ttu-id="84e99-160">' VerifyDistributionList ' アクティビティは "0.2597923" 秒で完了しました。</span><span class="sxs-lookup"><span data-stu-id="84e99-160">'VerifyDistributionList' activity completed in '0.2597923' secs.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="84e99-161">テストに失敗した可能性がある理由</span><span class="sxs-lookup"><span data-stu-id="84e99-161">Reasons why the test might have failed</span></span>

<span data-ttu-id="84e99-162">Test-CsGroupExpansion が失敗する可能性がある一般的な理由を次に示します。</span><span class="sxs-lookup"><span data-stu-id="84e99-162">Here are some common reasons why Test-CsGroupExpansion might fail:</span></span>

  - <span data-ttu-id="84e99-163">無効なユーザアカウントを指定しました。</span><span class="sxs-lookup"><span data-stu-id="84e99-163">You specified an invalid user account.</span></span> <span data-ttu-id="84e99-164">次のようなコマンドを実行すると、ユーザーアカウントが存在するかどうかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="84e99-164">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="84e99-165">ユーザーアカウントは有効ですが、アカウントは現在 Lync Server に対して有効になっていません。</span><span class="sxs-lookup"><span data-stu-id="84e99-165">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="84e99-166">ユーザーアカウントが Lync Server 用に有効になっていることを確認するには、次のようなコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="84e99-166">To verify that a user account was enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="84e99-167">Enabled プロパティが False に設定されている場合は、ユーザーが現在 Lync Server を有効にしていないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="84e99-167">If the Enabled property is set to False, that means that the user is currently not enabled for Lync Server.</span></span>

  - <span data-ttu-id="84e99-168">グループの拡張が無効になっている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="84e99-168">Group expansion might be disabled.</span></span> <span data-ttu-id="84e99-169">グループの拡張機能をオフにすることができます。</span><span class="sxs-lookup"><span data-stu-id="84e99-169">It is possible to turn off group expansion.</span></span> <span data-ttu-id="84e99-170">グループの拡張が無効になっている場合、Test-CsGroupExpansion コマンドレットは失敗します。</span><span class="sxs-lookup"><span data-stu-id="84e99-170">If group expansion was disabled then the Test-CsGroupExpansion cmdlet will fail.</span></span> <span data-ttu-id="84e99-171">グループの展開が有効であるかどうかを判断するには、次のようなコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="84e99-171">To determine whether group expansion is enabled, use a command similar to this:</span></span>
    
        Get-CsWebServiceConfiguration | Select-Object Identity, EnableGroupExpansion

<span data-ttu-id="84e99-172"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="84e99-172"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

