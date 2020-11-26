---
title: 'Lync Server 2013: 会議での共有のテスト'
description: 'Lync Server 2013: 会議での共有をテストしています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing sharing in conferences
ms:assetid: e6021d70-6ed9-414d-954c-06eef397dc1a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727314(v=OCS.15)
ms:contentKeyID: 63969660
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e569a97d102664b64c201af9b60061813df69ef5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439752"
---
# <a name="testing-sharing-in-conferences-in-lync-server-2013"></a><span data-ttu-id="a0141-103">Lync Server 2013 での会議の共有をテストする</span><span class="sxs-lookup"><span data-stu-id="a0141-103">Testing sharing in conferences in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a0141-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a0141-104">

<span> </span></span></span>

<span data-ttu-id="a0141-105">_**最終更新日:** 2014-11-01_</span><span class="sxs-lookup"><span data-stu-id="a0141-105">_**Topic Last Modified:** 2014-11-01_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a0141-106">確認のスケジュール</span><span class="sxs-lookup"><span data-stu-id="a0141-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="a0141-107">[毎日]</span><span class="sxs-lookup"><span data-stu-id="a0141-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0141-108">テストツール</span><span class="sxs-lookup"><span data-stu-id="a0141-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="a0141-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="a0141-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0141-110">必要なアクセス許可</span><span class="sxs-lookup"><span data-stu-id="a0141-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="a0141-111">Lync Server 管理シェルを使用してローカルで実行する場合、ユーザーは RTCUniversalServerAdmins セキュリティグループのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0141-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="a0141-112">Windows PowerShell のリモートインスタンスを使って実行する場合は、 <strong>CsDataConference</strong> コマンドレットを実行するためのアクセス許可が与えられている RBAC の役割をユーザーに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0141-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsDataConference</strong> cmdlet.</span></span> <span data-ttu-id="a0141-113">このコマンドレットを使うことができるすべての RBAC ロールの一覧を表示するには、Windows PowerShell プロンプトから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="a0141-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsDataConference&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="a0141-114">説明</span><span class="sxs-lookup"><span data-stu-id="a0141-114">Description</span></span>

<span data-ttu-id="a0141-115">Lync Server 2013 では、データ会議は、whiteboarding や注釈などのコラボレーションアクティビティを使用する会議です。</span><span class="sxs-lookup"><span data-stu-id="a0141-115">In Lync Server 2013, a data conference is any conference where collaborative activities such as whiteboarding or annotations are used.</span></span> <span data-ttu-id="a0141-116">**CsDataConference** コマンドレットを使用すると、ユーザーのペアがデータ会議に参加できるかどうかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="a0141-116">The **Test-CsDataConference** cmdlet enables you to verify that a pair of users are able to take part in a data conference.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="a0141-117">テストの実行</span><span class="sxs-lookup"><span data-stu-id="a0141-117">Running the test</span></span>

<span data-ttu-id="a0141-118">例1に示すコマンドは、プール atl-cs-001.litwareinc.com でデータ会議を実行できるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0141-118">The command shown in Example 1 verifies that a data conference can be conducted on the pool atl-cs-001.litwareinc.com.</span></span> <span data-ttu-id="a0141-119">このコマンドは、指定されたプールのテストユーザーのペアを構成していることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="a0141-119">This command assumes that you have configured a pair of test users for the specified pool.</span></span> <span data-ttu-id="a0141-120">このようなテストユーザーが存在しない場合、コマンドは失敗します。</span><span class="sxs-lookup"><span data-stu-id="a0141-120">If no such test users exist, the command will fail.</span></span>

    Test-CsDataConference -TargetFqdn "atl-cs-001.litwareinc.com" 

<span data-ttu-id="a0141-121">例2に示すコマンドは、ユーザーのペア (litwareinc \\ pilar と litwareinc \\ kenmyer) が Lync Server 2013 にログオンして、データ会議を開催する機能をテストします。</span><span class="sxs-lookup"><span data-stu-id="a0141-121">The commands shown in Example 2 test the ability of a pair of users (litwareinc\\pilar and litwareinc\\kenmyer) to log on to Lync Server 2013 and then conduct a data conference.</span></span> <span data-ttu-id="a0141-122">これを行うには、この例の最初のコマンドでは、 **Credential** コマンドレットを使用して、User Pilar Ackerman の名前とパスワードを含む Windows PowerShell コマンドラインインターフェイス Credential オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="a0141-122">To do this, the first command in the example uses the **Get-Credential** cmdlet to create a Windows PowerShell command-line interface credential object containing the name and password of the user Pilar Ackerman.</span></span> <span data-ttu-id="a0141-123">(Logon name、litwareinc pilar は \\ パラメーターとして指定されているため、Windows PowerShell 資格情報の要求ダイアログボックスでは、管理者は Pilar Ackerman アカウントのパスワードを入力する必要があります)。結果として得られた資格情報オブジェクトは、$cred 1 という名前の変数に格納されます。</span><span class="sxs-lookup"><span data-stu-id="a0141-123">(Because the logon name, litwareinc\\pilar, has been included as a parameter, the Windows PowerShell Credential Request dialog box only requires the administrator to enter the password for the Pilar Ackerman account.) The resulting credential object is then stored in a variable named $cred1.</span></span> <span data-ttu-id="a0141-124">2番目のコマンドでも同じことが実行されますが、今回は Ken Myer アカウントの credential オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="a0141-124">The second command does the same thing, this time returning a credential object for the Ken Myer account.</span></span>

<span data-ttu-id="a0141-125">資格情報オブジェクトが手元にある場合、3番目のコマンドは、これら2人のユーザーが Lync Server 2013 にログオンして、データ会議を実行できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a0141-125">With the credential objects in hand, the third command determines whether or not these two users can log on to Lync Server 2013 and conduct a data conference.</span></span> <span data-ttu-id="a0141-126">この処理を実行するために、 **CsDataConference** コマンドレットが呼び出され、次のパラメーターが使用されます。 targetfqdn (レジストラープールの FQDN)。SenderSipAddress (最初のテストユーザーの SIP アドレス)SenderCredential (同じユーザーの資格情報が含まれている Windows PowerShell オブジェクト)ReceiverSipAddress (他のテストユーザーの SIP アドレス)ReceiverCredential (他のテストユーザーの資格情報を格納する Windows PowerShell オブジェクト)。</span><span class="sxs-lookup"><span data-stu-id="a0141-126">To carry out this task, the **Test-CsDataConference** cmdlet is called, along with the following parameters: TargetFqdn (the FQDN of the Registrar pool); SenderSipAddress (the SIP address for the first test user); SenderCredential (the Windows PowerShell object containing the credentials for this same user); ReceiverSipAddress (the SIP address for the other test user); and ReceiverCredential (the Windows PowerShell object containing the credentials for the other test user).</span></span>

    $credential1 = Get-Credential "litwareinc\pilar" 
    $credential2 = Get-Credential "litwareinc\kenmyer" 
    Test-CsDataConference -TargetFqdn "atl-cs-001.litwareinc.com" -SenderSipAddress "sip:pilar@litwareinc.com" -SenderCredential $credential1 -ReceiverSipAddress "sip:kenmyer@litwareinc.com" -ReceiverCredential $credential2

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="a0141-127">成功または失敗を確認する</span><span class="sxs-lookup"><span data-stu-id="a0141-127">Determining success or failure</span></span>

<span data-ttu-id="a0141-128">データ会議が正しく構成されている場合は、次のような結果が返され、Result プロパティは Success とマークされ **ます。**</span><span class="sxs-lookup"><span data-stu-id="a0141-128">If data conferencing is correctly configured, you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="a0141-129">ターゲット Fqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="a0141-129">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="a0141-130">結果: 成功</span><span class="sxs-lookup"><span data-stu-id="a0141-130">Result : Success</span></span>

<span data-ttu-id="a0141-131">待ち時間: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="a0141-131">Latency : 00:00:00</span></span>

<span data-ttu-id="a0141-132">エラーメッセージ:</span><span class="sxs-lookup"><span data-stu-id="a0141-132">Error Message :</span></span>

<span data-ttu-id="a0141-133">診断</span><span class="sxs-lookup"><span data-stu-id="a0141-133">Diagnosis :</span></span>

<span data-ttu-id="a0141-134">指定したユーザーがデータ共有を使用できない場合は、結果 **がエラーとして** 表示され、エラーと診断のプロパティに追加情報が記録されます。</span><span class="sxs-lookup"><span data-stu-id="a0141-134">If the specified users can't use data sharing, the Result will be shown as **Failure**, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="a0141-135">ターゲット Fqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="a0141-135">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="a0141-136">結果: エラー</span><span class="sxs-lookup"><span data-stu-id="a0141-136">Result : Failure</span></span>

<span data-ttu-id="a0141-137">待ち時間: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="a0141-137">Latency : 00:00:00</span></span>

<span data-ttu-id="a0141-138">エラーメッセージ: 10060、接続されているパーティのため、接続に失敗しました</span><span class="sxs-lookup"><span data-stu-id="a0141-138">Error Message : 10060, A connection attempt failed because the connected party</span></span>

<span data-ttu-id="a0141-139">一定の期間が経過した後に正しく応答しなかった場合、または</span><span class="sxs-lookup"><span data-stu-id="a0141-139">did not properly respond after a period of time, or</span></span>

<span data-ttu-id="a0141-140">接続されているホストに、接続に失敗しました</span><span class="sxs-lookup"><span data-stu-id="a0141-140">established connection failed because connected host has</span></span>

<span data-ttu-id="a0141-141">\[2001: 4898: f39e: 5c9a: ad83: 81b3: 9944: 5061 を応答できませんでした。 \]</span><span class="sxs-lookup"><span data-stu-id="a0141-141">failed to respond \[2001:4898:e8:f39e:5c9a:ad83:81b3:9944\]:5061</span></span>

<span data-ttu-id="a0141-142">内部例外: 接続の試行が失敗したため、接続できませんでした。</span><span class="sxs-lookup"><span data-stu-id="a0141-142">Inner Exception:A connection attempt failed because the</span></span>

<span data-ttu-id="a0141-143">しばらくしても、接続されているパーティが正しく応答しませんでした</span><span class="sxs-lookup"><span data-stu-id="a0141-143">connected party did not properly respond after a period of</span></span>

<span data-ttu-id="a0141-144">接続されているホストが原因で、時刻、または接続に失敗しました</span><span class="sxs-lookup"><span data-stu-id="a0141-144">time, or established connection failed because connected host</span></span>

<span data-ttu-id="a0141-145">が応答しませんでした</span><span class="sxs-lookup"><span data-stu-id="a0141-145">has failed to respond</span></span>

<span data-ttu-id="a0141-146">\[2001: 4898: f39e: 5c9a: ad83: 81b3: 9944 \] : 5061</span><span class="sxs-lookup"><span data-stu-id="a0141-146">\[2001:4898:e8:f39e:5c9a:ad83:81b3:9944\]:5061</span></span>

<span data-ttu-id="a0141-147">診断</span><span class="sxs-lookup"><span data-stu-id="a0141-147">Diagnosis :</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="a0141-148">テストに失敗した可能性がある理由</span><span class="sxs-lookup"><span data-stu-id="a0141-148">Reasons why the test might have failed</span></span>

<span data-ttu-id="a0141-149">次に **、テスト-CsDataConference** が失敗する可能性がある一般的な理由を示します。</span><span class="sxs-lookup"><span data-stu-id="a0141-149">Here are some common reasons why **Test-CsDataConference** might fail:</span></span>

  - <span data-ttu-id="a0141-150">指定されたパラメーター値が正しくありません。</span><span class="sxs-lookup"><span data-stu-id="a0141-150">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="a0141-151">使用する場合は、オプションのパラメーターが正しく構成されている必要があります。または、テストが失敗します。</span><span class="sxs-lookup"><span data-stu-id="a0141-151">If used, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="a0141-152">省略可能なパラメーターを指定せずにコマンドを再実行し、それが成功するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0141-152">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

  - <span data-ttu-id="a0141-153">データ会議を開催する機能は、会議を開催したユーザーに割り当てられている会議ポリシー ( **CsDataConference** コマンドレットの場合は "送信者") によって異なります。</span><span class="sxs-lookup"><span data-stu-id="a0141-153">The ability to conduct a data conference depends on the conferencing policy that has been assigned to the user who organized the conference (in the case of the **Test-CsDataConference** cmdlet, that is the "sender").</span></span> <span data-ttu-id="a0141-154">開催者が、会議に共同作業のアクティビティを含めることを許可していない場合 (たとえば、自分の会議ポリシーの EnableDataCollaboration プロパティが False に設定されている場合など)、 **CsDataConference** コマンドレットは失敗します。</span><span class="sxs-lookup"><span data-stu-id="a0141-154">If the organizer is not allowed to include collaborative activities in his or her meeting (for example, if his or her conferencing policy has the EnableDataCollaboration property set to False) then the **Test-CsDataConference** cmdlet will fail.</span></span>

  - <span data-ttu-id="a0141-155">エッジサーバーが正しく構成されていないか、まだ展開されていない場合、このコマンドは失敗します。</span><span class="sxs-lookup"><span data-stu-id="a0141-155">This command will fail if the Edge Server is misconfigured or not yet deployed.</span></span>

<span data-ttu-id="a0141-156"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a0141-156"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

