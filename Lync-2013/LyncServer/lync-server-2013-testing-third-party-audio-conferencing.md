---
title: 'Lync Server 2013: サードパーティの電話会議のテスト'
description: 'Lync Server 2013: サードパーティの電話会議のテスト。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing third-party audio conferencing
ms:assetid: 0428eb2f-a5ce-47e5-9ea4-383965dfc1e4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727299(v=OCS.15)
ms:contentKeyID: 63969576
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f009d95834768d8a4e6619a79ff1f3be0a2b92bd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440956"
---
# <a name="testing-third-party-audio-conferencing-in-lync-server-2013"></a><span data-ttu-id="39189-103">Lync Server 2013 でのサードパーティの電話会議のテスト</span><span class="sxs-lookup"><span data-stu-id="39189-103">Testing third-party audio conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="39189-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="39189-104">

<span> </span></span></span>

<span data-ttu-id="39189-105">_**最終更新日:** 2014-11-01_</span><span class="sxs-lookup"><span data-stu-id="39189-105">_**Topic Last Modified:** 2014-11-01_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39189-106">確認のスケジュール</span><span class="sxs-lookup"><span data-stu-id="39189-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="39189-107">[毎日]</span><span class="sxs-lookup"><span data-stu-id="39189-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39189-108">テストツール</span><span class="sxs-lookup"><span data-stu-id="39189-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="39189-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="39189-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39189-110">必要なアクセス許可</span><span class="sxs-lookup"><span data-stu-id="39189-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="39189-111">Lync Server 管理シェルを使用してローカルで実行する場合、ユーザーは RTCUniversalServerAdmins セキュリティグループのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="39189-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="39189-112">Windows PowerShell のリモートインスタンスを使って実行する場合は、Test-CsAudioConferencingProvider コマンドレットを実行するためのアクセス許可を持つ RBAC の役割をユーザーに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="39189-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsAudioConferencingProvider cmdlet.</span></span> <span data-ttu-id="39189-113">このコマンドレットを使うことができるすべての RBAC ロールの一覧を表示するには、Windows PowerShell プロンプトから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="39189-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsAudioConferencingProvider&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="39189-114">説明</span><span class="sxs-lookup"><span data-stu-id="39189-114">Description</span></span>

<span data-ttu-id="39189-115">電話会議プロバイダーとは、電話会議サービスを組織に提供するサード パーティの企業です。</span><span class="sxs-lookup"><span data-stu-id="39189-115">An audio conferencing provider is a third-party company that provides organizations with conferencing services.</span></span> <span data-ttu-id="39189-116">電話会議プロバイダーの主な機能は、社外にいて企業ネットワークまたはインターネットに接続されていないユーザーが、電話会議または会議のオーディオ部分に参加できるようにすることです。</span><span class="sxs-lookup"><span data-stu-id="39189-116">Among other things, audio conferencing providers enable users located off site, and not connected to the corporate network or the Internet, to participate in the audio portion of a conference or meeting.</span></span> <span data-ttu-id="39189-117">電話会議プロバイダーは、リアルタイムの翻訳、議事録、電話会議などの機能のようなハイエンドサービスを提供します。</span><span class="sxs-lookup"><span data-stu-id="39189-117">Audio conferencing providers often provide high-end services such as live translation, transcription, and live per-conference operator assistance.</span></span>

<span data-ttu-id="39189-118">**CsAudioConferencingProvider** コマンドレットを使用して、ユーザーが電話会議プロバイダーへの接続を確立できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="39189-118">The **Test-CsAudioConferencingProvider** cmdlet is used to verify that a user is able to make a connection to his or her audio conferencing provider.</span></span> <span data-ttu-id="39189-119">このコマンドレットは、次の2つの方法のいずれかで実行できます。</span><span class="sxs-lookup"><span data-stu-id="39189-119">Note that this cmdlet can be run in one of two ways.</span></span> <span data-ttu-id="39189-120">多くの管理者は、CsHealthMonitoringConfiguration コマンドレットを使用して、各レジストラープールのテストユーザーをセットアップします。</span><span class="sxs-lookup"><span data-stu-id="39189-120">Many administrators will use the CsHealthMonitoringConfiguration cmdlets to set up test users for each of their Registrar pools.</span></span> <span data-ttu-id="39189-121">これらのテストユーザーは、代理トランザクションで使用するために事前に構成されているユーザーアカウントのペアを表します。</span><span class="sxs-lookup"><span data-stu-id="39189-121">These test users represent a pair of user accounts that have been preconfigured for use with synthetic transactions.</span></span> <span data-ttu-id="39189-122">(通常、テストアカウントであり、実際のユーザーに属するアカウントではありません)。プールに対してテストユーザーが構成されている場合、管理者は、テストに関係しているユーザーアカウントの id を指定せずに、そのプールに対して **CsAudioConferencingProvider** コマンドレットを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="39189-122">(Typically these are test accounts and not accounts that belong to actual users.) If test users are configured for a pool, administrators can run the **Test-CsAudioConferencingProvider** cmdlet against that pool without having to specify the identity of (and supply the credentials for) the user account involved in the test.</span></span>

<span data-ttu-id="39189-123">または、管理者は実際のユーザーアカウントを使用して **CsAudioConferencingProvider** コマンドレットを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="39189-123">Alternatively, administrators can run the **Test-CsAudioConferencingProvider** cmdlet using an actual user account.</span></span> <span data-ttu-id="39189-124">実際のユーザーアカウントを使用してテストを実施する場合は、そのアカウントのログオン名とパスワードを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="39189-124">If you decide to conduct the test using an actual user account you will need to supply the logon name and password for that account.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="39189-125">テストの実行</span><span class="sxs-lookup"><span data-stu-id="39189-125">Running the test</span></span>

<span data-ttu-id="39189-126">例1プール atl-cs-001.litwareinc.com に対して定義されたテストユーザーが、自分の電話会議プロバイダーに接続できるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="39189-126">Example 1 checks to see if a test user defined for the pool atl-cs-001.litwareinc.com is able to connect to his or her audio conferencing provider.</span></span> <span data-ttu-id="39189-127">このコマンドでは、プールに対して少なくとも1つのテストユーザーを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="39189-127">This command requires that at least one test user be defined for the pool.</span></span> <span data-ttu-id="39189-128">Atl-cs-001.litwareinc.com にテストユーザーが定義されていない場合、コマンドは失敗します。これは、 **CsAudioConferencingProvider** コマンドレットでは、どのユーザーがテストで採用するかわからないためです。</span><span class="sxs-lookup"><span data-stu-id="39189-128">If no test users have been defined for atl-cs-001.litwareinc.com, then the command will fail; that's because the **Test-CsAudioConferencingProvider** cmdlet will not know which user to employ in the test.</span></span> <span data-ttu-id="39189-129">プールのテストユーザーを定義していない場合は、電話会議プロバイダーとの接続を確認するときに、コマンドで使用する必要があるユーザーアカウントの UserSipAddress パラメーターと資格情報を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="39189-129">If you have not defined test users for a pool, then you must include the UserSipAddress parameter and the credentials of the user account that the command should employ when verifying the connection with an audio conferencing provider.</span></span>

    Test-CsAudioConferencingProvider -TargetFqdn atl-cs-001.litwareinc.com 

<span data-ttu-id="39189-130">例2に示すコマンドは、特定のユーザー (litwareinc \\ kenmyer) が電話会議プロバイダーに接続できるかどうかをテストします。</span><span class="sxs-lookup"><span data-stu-id="39189-130">The commands shown in Example 2 test the ability of a specific user (litwareinc\\kenmyer) to connect to his audio conferencing provider.</span></span> <span data-ttu-id="39189-131">これを行うには、この例の最初のコマンドレットを Get-Credential 使用して、ユーザー Ken Myer の名前とパスワードを含む Windows PowerShell コマンドラインインターフェイスの資格情報オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="39189-131">To do this, the first command in the example uses the Get-Credential cmdlet to create a Windows PowerShell command-line interface credentials object containing the name and password of the user Ken Myer.</span></span> <span data-ttu-id="39189-132">(ログオン名 litwareinc \\ kenmyer はパラメーターとして含まれているため、Windows PowerShell 資格情報の要求ダイアログボックスでは、管理者が Ken Myer アカウントのパスワードを入力するだけで済みます)。この結果、資格情報オブジェクトは $credential という名前の変数に格納されます。</span><span class="sxs-lookup"><span data-stu-id="39189-132">(Because the logon name litwareinc\\kenmyer has been included as a parameter, the Windows PowerShell Credential Request dialog box only requires the administrator to enter the password for the Ken Myer account.) The resulting credentials object is stored in a variable named $credential.</span></span>

<span data-ttu-id="39189-133">2番目のコマンドは、このユーザーが自分の電話会議プロバイダーに接続できるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="39189-133">The second command then checks to see if this user can connect to his audio conferencing provider.</span></span> <span data-ttu-id="39189-134">この処理を実行するために、Test-CsAudioConferencingProvider コマンドレットが呼び出され、次の3つのパラメーター (レジストラープールの FQDN) が示されます。UserCredential (Ken Myer のユーザー資格情報を含む Windows PowerShell オブジェクト)UserSipAddress (提供されているユーザー資格情報に対応する SIP アドレス) を選びます。</span><span class="sxs-lookup"><span data-stu-id="39189-134">To carry out this task, the Test-CsAudioConferencingProvider cmdlet is called, along with three parameters: TargetFqdn (the FQDN of the Registrar pool); UserCredential (the Windows PowerShell object containing Ken Myer's user credentials); and UserSipAddress (the SIP address corresponding to the supplied user credentials).</span></span>

    $credential = Get-Credential "litwareinc\kenmyer" 
    Test-CsAudioConferencingProvider -TargetFqdn atl-cs-001.litwareinc.com -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="39189-135">成功または失敗を確認する</span><span class="sxs-lookup"><span data-stu-id="39189-135">Determining success or failure</span></span>

<span data-ttu-id="39189-136">電話会議プロバイダーが正しく構成されている場合は、次のような出力が表示され、Result プロパティは Success とマークされ **ます。**</span><span class="sxs-lookup"><span data-stu-id="39189-136">If the audio conferencing provider is correctly configured, you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="39189-137">ターゲット Fqdn: atl-sql-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="39189-137">Target Fqdn : atl-sql-001.litwareinc.com</span></span>

<span data-ttu-id="39189-138">結果: 成功</span><span class="sxs-lookup"><span data-stu-id="39189-138">Result : Success</span></span>

<span data-ttu-id="39189-139">待ち時間: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="39189-139">Latency : 00:00:00</span></span>

<span data-ttu-id="39189-140">エラーメッセージ:</span><span class="sxs-lookup"><span data-stu-id="39189-140">Error Message :</span></span>

<span data-ttu-id="39189-141">診断</span><span class="sxs-lookup"><span data-stu-id="39189-141">Diagnosis :</span></span>

<span data-ttu-id="39189-142">指定したユーザーがログオンまたはログオフできない場合は、結果がエラーとして表示さ **れ、エラー** と診断のプロパティに追加情報が記録されます。</span><span class="sxs-lookup"><span data-stu-id="39189-142">If the specified user can't log on or log off, the Result will be shown as a **Failure**, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="39189-143">ターゲット Fqdn: atl-sql-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="39189-143">Target Fqdn : atl-sql-001.litwareinc.com</span></span>

<span data-ttu-id="39189-144">結果: エラー</span><span class="sxs-lookup"><span data-stu-id="39189-144">Result : Failure</span></span>

<span data-ttu-id="39189-145">待ち時間: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="39189-145">Latency : 00:00:00</span></span>

<span data-ttu-id="39189-146">エラーメッセージ: 10060、接続されているパーティのため、接続に失敗しました</span><span class="sxs-lookup"><span data-stu-id="39189-146">Error Message : 10060, A connection attempt failed because the connected party</span></span>

<span data-ttu-id="39189-147">一定の期間が経過した後に正しく応答しなかった場合、または</span><span class="sxs-lookup"><span data-stu-id="39189-147">did not properly respond after a period of time, or</span></span>

<span data-ttu-id="39189-148">接続されているホストに、接続に失敗しました</span><span class="sxs-lookup"><span data-stu-id="39189-148">established connection failed because connected host has</span></span>

<span data-ttu-id="39189-149">\[2001: 4898: f39e: 5c9a: ad83: 81b3: 9944: 5061 を応答できませんでした。 \]</span><span class="sxs-lookup"><span data-stu-id="39189-149">failed to respond \[2001:4898:e8:f39e:5c9a:ad83:81b3:9944\]:5061</span></span>

<span data-ttu-id="39189-150">内部例外: 接続の試行が失敗したため、接続できませんでした。</span><span class="sxs-lookup"><span data-stu-id="39189-150">Inner Exception:A connection attempt failed because the</span></span>

<span data-ttu-id="39189-151">しばらくしても、接続されているパーティが正しく応答しませんでした</span><span class="sxs-lookup"><span data-stu-id="39189-151">connected party did not properly respond after a period of</span></span>

<span data-ttu-id="39189-152">接続されているホストが原因で、時刻、または接続に失敗しました</span><span class="sxs-lookup"><span data-stu-id="39189-152">time, or established connection failed because connected host</span></span>

<span data-ttu-id="39189-153">が応答しませんでした</span><span class="sxs-lookup"><span data-stu-id="39189-153">has failed to respond</span></span>

<span data-ttu-id="39189-154">\[2001: 4898: f39e: 5c9a: ad83: 81b3: 9944 \] : 5061</span><span class="sxs-lookup"><span data-stu-id="39189-154">\[2001:4898:e8:f39e:5c9a:ad83:81b3:9944\]:5061</span></span>

<span data-ttu-id="39189-155">診断</span><span class="sxs-lookup"><span data-stu-id="39189-155">Diagnosis :</span></span>

<span data-ttu-id="39189-156">たとえば、前回の出力には、"接続されているパーティは正しく応答しませんでした" というメモが含まれています。通常、エッジサーバーに問題があることを示します。</span><span class="sxs-lookup"><span data-stu-id="39189-156">For example, the previous output includes the note “the connected party did not properly respond” That typically indicates a problem with the Edge Server.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="39189-157">テストに失敗した可能性がある理由</span><span class="sxs-lookup"><span data-stu-id="39189-157">Reasons why the test might have failed</span></span>

<span data-ttu-id="39189-158">次に **、テスト-CsAudioConferencingProvider** が失敗する可能性がある一般的な理由を示します。</span><span class="sxs-lookup"><span data-stu-id="39189-158">Here are some common reasons why **Test-CsAudioConferencingProvider** might fail:</span></span>

  - <span data-ttu-id="39189-159">指定されたパラメーター値が正しくありません。</span><span class="sxs-lookup"><span data-stu-id="39189-159">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="39189-160">上の例で示したように、オプションのパラメーターは正しく構成されている必要があります。また、テストは失敗します。</span><span class="sxs-lookup"><span data-stu-id="39189-160">As shown in the previous example, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="39189-161">省略可能なパラメーターを指定せずにコマンドを再実行し、それが成功するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="39189-161">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

  - <span data-ttu-id="39189-162">**CsAudioConferencingProvider** コマンドレットによって採用されたユーザーに電話会議プロバイダーが割り当てられていない場合、テストは失敗します。</span><span class="sxs-lookup"><span data-stu-id="39189-162">Note that the test will fail if the user employed by the **Test-CsAudioConferencingProvider** cmdlet has not been assigned an audio conferencing provider.</span></span>

  - <span data-ttu-id="39189-163">エッジサーバーが正しく構成されていないか、まだ展開されていない場合、このコマンドは失敗します。</span><span class="sxs-lookup"><span data-stu-id="39189-163">This command will fail if the Edge Server is misconfigured or not yet deployed.</span></span>

<span data-ttu-id="39189-164"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="39189-164"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

