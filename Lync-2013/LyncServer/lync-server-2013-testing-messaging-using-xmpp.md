---
title: 'Lync Server 2013: XMPP を使用したメッセージングのテスト'
description: 'Lync Server 2013: XMPP を使ったメッセージングのテスト'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing messaging using XMPP
ms:assetid: ae5305ba-e5fc-4ca0-a805-872b4ebaf981
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727312(v=OCS.15)
ms:contentKeyID: 63969641
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 06faeae0a6104351f9102de31c76b2424a140deb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441005"
---
# <a name="testing-messaging-using-xmpp-in-lync-server-2013"></a><span data-ttu-id="52058-103">Lync Server 2013 での XMPP を使ったメッセージングのテスト</span><span class="sxs-lookup"><span data-stu-id="52058-103">Testing messaging using XMPP in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="52058-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="52058-104">

<span> </span></span></span>

<span data-ttu-id="52058-105">_**最終更新日:** 2014-11-03_</span><span class="sxs-lookup"><span data-stu-id="52058-105">_**Topic Last Modified:** 2014-11-03_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52058-106">確認のスケジュール</span><span class="sxs-lookup"><span data-stu-id="52058-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="52058-107">[毎日]</span><span class="sxs-lookup"><span data-stu-id="52058-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52058-108">テストツール</span><span class="sxs-lookup"><span data-stu-id="52058-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="52058-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="52058-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52058-110">必要なアクセス許可</span><span class="sxs-lookup"><span data-stu-id="52058-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="52058-111">Lync Server 管理シェルを使用してローカルで実行する場合、ユーザーは RTCUniversalServerAdmins セキュリティグループのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="52058-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="52058-112">Windows PowerShell のリモートインスタンスを使用して実行する場合、ユーザーには、 <strong>CsXmppIM</strong> コマンドレットを実行するためのアクセス許可が与えられた RBAC の役割を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="52058-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsXmppIM</strong> cmdlet.</span></span> <span data-ttu-id="52058-113">このコマンドレットを使うことができるすべての RBAC ロールの一覧を表示するには、Windows PowerShell プロンプトから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="52058-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsXmppIM&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="52058-114">説明</span><span class="sxs-lookup"><span data-stu-id="52058-114">Description</span></span>

<span data-ttu-id="52058-115">拡張メッセージングとプレゼンスプロトコル (XMPP) は、インターネット経由でメッセージを送信するために使用される標準の通信プロトコル (XML に基づく) です。</span><span class="sxs-lookup"><span data-stu-id="52058-115">The Extensible Messaging and Presence Protocol (XMPP) is a standard communications protocol (based on XML) used for sending messages across the Internet.</span></span> <span data-ttu-id="52058-116">XMPP は元々 Jabber という名称でしたが、いくつかのインターネットメッセージングやコミュニケーションアプリケーション (Google 通話、Facebook チャットなど) でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="52058-116">XMPP was originally named Jabber, and is supported by several Internet messaging and communication applications, such as Google Talk and Facebook Chat.</span></span> <span data-ttu-id="52058-117">**テスト用の CsXmppIM** コマンドレットは、ユーザーが xmpp ネットワーク上のユーザーとインスタントメッセージをやり取りできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="52058-117">The **Test-CsXmppIM** cmdlet verifies that a user can exchange instant messages with a user on an XMPP network.</span></span> <span data-ttu-id="52058-118">このテストを成功させるには、XMPP ユーザーの有効な SIP アドレスが必要であり、その SIP アドレスが許可されている XMPP パートナーとして構成されたネットワーク上にある必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="52058-118">Note that, for this test to succeed, you must have a valid SIP address for the XMPP user, and that SIP address must be on a network that was configured as an allowed XMPP partner.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="52058-119">テストの実行</span><span class="sxs-lookup"><span data-stu-id="52058-119">Running the test</span></span>

<span data-ttu-id="52058-120">次の例では、pool atl-cs-001.litwareinc.com の XMPP インスタントメッセージング機能を確認します。</span><span class="sxs-lookup"><span data-stu-id="52058-120">The following example verifies the XMPP instant messaging capabilities for the pool atl-cs-001.litwareinc.com.</span></span> <span data-ttu-id="52058-121">このコマンドは、プール atl-cs-001.litwareinc.com に対してテストユーザーが定義されている場合にのみ機能します。</span><span class="sxs-lookup"><span data-stu-id="52058-121">This command will work only if test users are defined for the pool atl-cs-001.litwareinc.com.</span></span> <span data-ttu-id="52058-122">その場合、コマンドは、SIP アドレスが adelaney@contoso.com のユーザーに XMPP のインスタントメッセージを送信するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="52058-122">If they have, then the command will determine whether the first test user can send an XMPP instant message to a user who has the SIP address adelaney@contoso.com.</span></span>

<span data-ttu-id="52058-123">テストユーザーが定義されていない場合は、どのユーザーとしてログオンするかがわからないため、コマンドは失敗します。</span><span class="sxs-lookup"><span data-stu-id="52058-123">If test users are not defined, then the command will fail because it won't know which user to log on as.</span></span> <span data-ttu-id="52058-124">プールのテストユーザーを定義していない場合は、UserSipAddress パラメーターと、ログオンしようとしてコマンドで使用する必要があるユーザーの資格情報を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="52058-124">If you have not defined test users for a pool, then you must include the UserSipAddress parameter and the credentials of the user who the command should use when trying to log on.</span></span>

    Test-CsXmppIM -TargetFqdn "atl-cs-001.litwareinc.com" -Receiver "adelany@contoso.com"

<span data-ttu-id="52058-125">次の例に示すコマンドは、特定のユーザー (litwareinc pilar) がログオンして、 \\ ユーザー adelaney@contoso.com に XMPP インスタントメッセージを送信する機能をテストします。</span><span class="sxs-lookup"><span data-stu-id="52058-125">The commands shown in the next example test the ability of a specific user (litwareinc\\pilar) to log on to send an XMPP instant message to the user adelaney@contoso.com.</span></span> <span data-ttu-id="52058-126">これを行うには、次の例では Get-Credential コマンドレットを使用して、user Pilar Ackerman の名前とパスワードを含む Windows PowerShell コマンドラインインターフェイス資格情報オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="52058-126">To do this, the first command in the example uses the Get-Credential cmdlet to create a Windows PowerShell command-line interface credential object that contains the name and password of the user Pilar Ackerman.</span></span> <span data-ttu-id="52058-127">(Logon name litwareinc \\ pilar がパラメーターとして含まれているため、Windows PowerShell 資格情報の要求ダイアログボックスでは、管理者が Pilar Ackerman アカウントのパスワードを入力する必要があります)。結果として得られた資格情報オブジェクトは、$cred 1 という名前の変数に格納されます。</span><span class="sxs-lookup"><span data-stu-id="52058-127">(Because the logon name litwareinc\\pilar was included as a parameter, the Windows PowerShell Credential Request dialog box only requires the administrator to enter the password for the Pilar Ackerman account.) The resulting credential object is then stored in a variable named $cred1.</span></span>

<span data-ttu-id="52058-128">2番目のコマンドは、このユーザーがプール atl-cs-001.litwareinc.com にログオンして XMPP インスタントメッセージを送信できるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="52058-128">The second command then checks whether this user can log on to the pool atl-cs-001.litwareinc.com and send the XMPP instant message.</span></span> <span data-ttu-id="52058-129">このタスクを実行するために、次の4つのパラメーター (レジストラープールの FQDN) と共に、 **Test-CsXmppIm** コマンドレットが呼び出されます。受け手 (メッセージの宛先となっているユーザの SIP アドレス)。UserCredential (Pilar Ackerman のユーザー資格情報を格納する Windows PowerShell オブジェクト)UserSipAddress (提供されているユーザー資格情報に対応する SIP アドレス) を選びます。</span><span class="sxs-lookup"><span data-stu-id="52058-129">To run this task, the **Test-CsXmppIm** cmdlet is called, together with four parameters: TargetFqdn (the FQDN of the Registrar pool); Receiver (the SIP address of the user the message is being addressed to); UserCredential (the Windows PowerShell object that contains Pilar Ackerman’s user credentials); and UserSipAddress (the SIP address that corresponds to the supplied user credentials).</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    
    Test-CsXmppIM -TargetFqdn "atl-cs-001.litwareinc.com" -Receiver "adelany@contoso.com" -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="52058-130">成功または失敗を確認する</span><span class="sxs-lookup"><span data-stu-id="52058-130">Determining success or failure</span></span>

<span data-ttu-id="52058-131">XMPP のインスタントメッセージングが正しく構成されている場合は、次のような出力が表示され、Result プロパティは Success とマークされ **ます。**</span><span class="sxs-lookup"><span data-stu-id="52058-131">If XMPP instant messaging is correctly configured, you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="52058-132">ターゲット Fqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="52058-132">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="52058-133">結果: 成功</span><span class="sxs-lookup"><span data-stu-id="52058-133">Result : Success</span></span>

<span data-ttu-id="52058-134">待ち時間:00:00: 02.5361946</span><span class="sxs-lookup"><span data-stu-id="52058-134">Latency : 00:00:02.5361946</span></span>

<span data-ttu-id="52058-135">エラーメッセージ:</span><span class="sxs-lookup"><span data-stu-id="52058-135">Error Message :</span></span>

<span data-ttu-id="52058-136">診断</span><span class="sxs-lookup"><span data-stu-id="52058-136">Diagnosis :</span></span>

<span data-ttu-id="52058-137">指定したユーザーが XMPP のインスタントメッセージングを使用できない場合は、結果 **がエラーとして** 表示され、エラーと診断のプロパティに追加情報が記録されます。</span><span class="sxs-lookup"><span data-stu-id="52058-137">If the specified users can't use XMPP instant messaging, the Result will be shown as **Failure**, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="52058-138">警告: 指定した完全修飾のレジストラーポート番号の読み取りに失敗しました</span><span class="sxs-lookup"><span data-stu-id="52058-138">WARNING: Failed to read Registrar port number for the given fully qualified</span></span>

<span data-ttu-id="52058-139">ドメイン名 (FQDN)。</span><span class="sxs-lookup"><span data-stu-id="52058-139">domain name (FQDN).</span></span> <span data-ttu-id="52058-140">既定のレジストラーポート番号を使用します。</span><span class="sxs-lookup"><span data-stu-id="52058-140">Using default Registrar port number.</span></span> <span data-ttu-id="52058-141">エラー</span><span class="sxs-lookup"><span data-stu-id="52058-141">Exception:</span></span>

<span data-ttu-id="52058-142">InvalidOperationException: トポロジで一致するクラスターが見つかりませんでした。</span><span class="sxs-lookup"><span data-stu-id="52058-142">System.InvalidOperationException: No matching cluster found in topology.</span></span>

<span data-ttu-id="52058-143">自宅</span><span class="sxs-lookup"><span data-stu-id="52058-143">at</span></span>

<span data-ttu-id="52058-144">SipSyntheticTransaction-TryRetri の同期を行います。</span><span class="sxs-lookup"><span data-stu-id="52058-144">Microsoft.Rtc.Management.SyntheticTransactions.SipSyntheticTransaction.TryRetri</span></span>

<span data-ttu-id="52058-145">eveRegistrarPortFromTopology (Int32& registrarPortNumber)</span><span class="sxs-lookup"><span data-stu-id="52058-145">eveRegistrarPortFromTopology(Int32& registrarPortNumber)</span></span>

<span data-ttu-id="52058-146">ターゲット Fqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="52058-146">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="52058-147">結果: エラー</span><span class="sxs-lookup"><span data-stu-id="52058-147">Result : Failure</span></span>

<span data-ttu-id="52058-148">待ち時間: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="52058-148">Latency : 00:00:00</span></span>

<span data-ttu-id="52058-149">エラーメッセージ: 10060、接続されているパーティのため、接続に失敗しました</span><span class="sxs-lookup"><span data-stu-id="52058-149">Error Message : 10060, A connection attempt failed because the connected party</span></span>

<span data-ttu-id="52058-150">一定の期間が経過した後に正しく応答しなかった場合、または</span><span class="sxs-lookup"><span data-stu-id="52058-150">did not properly respond after a period of time, or</span></span>

<span data-ttu-id="52058-151">接続されているホストに、接続に失敗しました</span><span class="sxs-lookup"><span data-stu-id="52058-151">established connection failed because connected host has</span></span>

<span data-ttu-id="52058-152">10.188.116.96 に応答できませんでした: 5061</span><span class="sxs-lookup"><span data-stu-id="52058-152">failed to respond 10.188.116.96:5061</span></span>

<span data-ttu-id="52058-153">内部例外: 接続の試行が失敗したため、接続できませんでした。</span><span class="sxs-lookup"><span data-stu-id="52058-153">Inner Exception:A connection attempt failed because the</span></span>

<span data-ttu-id="52058-154">しばらくしても、接続されているパーティが正しく応答しませんでした</span><span class="sxs-lookup"><span data-stu-id="52058-154">connected party did not properly respond after a period of</span></span>

<span data-ttu-id="52058-155">接続されているホストが原因で、時刻、または接続に失敗しました</span><span class="sxs-lookup"><span data-stu-id="52058-155">time, or established connection failed because connected host</span></span>

<span data-ttu-id="52058-156">さんが10.188.116.96 に応答できませんでした: 5061</span><span class="sxs-lookup"><span data-stu-id="52058-156">has failed to respond 10.188.116.96:5061</span></span>

<span data-ttu-id="52058-157">診断</span><span class="sxs-lookup"><span data-stu-id="52058-157">Diagnosis :</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="52058-158">テストに失敗した可能性がある理由</span><span class="sxs-lookup"><span data-stu-id="52058-158">Reasons why the test might have failed</span></span>

<span data-ttu-id="52058-159">次に **、テスト用の CsXmppIM** が失敗する一般的な理由をいくつか示します。</span><span class="sxs-lookup"><span data-stu-id="52058-159">Here are some common reasons why **Test-CsXmppIM** might fail:</span></span>

  - <span data-ttu-id="52058-160">指定されたパラメーター値が正しくありません。</span><span class="sxs-lookup"><span data-stu-id="52058-160">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="52058-161">使用する場合は、オプションのパラメーターが正しく構成されている必要があります。または、テストが失敗します。</span><span class="sxs-lookup"><span data-stu-id="52058-161">If used, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="52058-162">省略可能なパラメーターを指定せずにコマンドを再実行し、それが成功するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="52058-162">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

  - <span data-ttu-id="52058-163">XMPP ゲートウェイの構成が正しく設定されていないか、まだ展開されていない場合、このコマンドは失敗します。</span><span class="sxs-lookup"><span data-stu-id="52058-163">This command will fail if XMPP gateway configuration is misconfigured or not yet deployed.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="52058-164">関連項目</span><span class="sxs-lookup"><span data-stu-id="52058-164">See Also</span></span>


[<span data-ttu-id="52058-165">Set-CsXmppGatewayConfiguration</span><span class="sxs-lookup"><span data-stu-id="52058-165">Set-CsXmppGatewayConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsXmppGatewayConfiguration)  
  

<span data-ttu-id="52058-166"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="52058-166"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

