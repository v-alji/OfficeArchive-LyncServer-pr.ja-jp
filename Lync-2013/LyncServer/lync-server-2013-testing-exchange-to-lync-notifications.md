---
title: 'Lync Server 2013: Lync 通知への Exchange のテスト'
description: 'Lync Server 2013: Lync 通知への Exchange のテスト。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing Exchange to Lync notifications
ms:assetid: ed2d6325-3cf5-4450-9951-03092bcb0a7c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727315(v=OCS.15)
ms:contentKeyID: 63969665
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bdf453bfdaab7e7b6bdaae8b67ac7759c0d55af4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398972"
---
# <a name="testing-exchange-to-lync-notifications-in-lync-server-2013"></a><span data-ttu-id="c643f-103">Lync Server 2013 での Lync からの通知への Exchange のテスト</span><span class="sxs-lookup"><span data-stu-id="c643f-103">Testing Exchange to Lync notifications in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c643f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c643f-104">

<span> </span></span></span>

<span data-ttu-id="c643f-105">_**最終更新日:** 2014-11-01_</span><span class="sxs-lookup"><span data-stu-id="c643f-105">_**Topic Last Modified:** 2014-11-01_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c643f-106">確認のスケジュール</span><span class="sxs-lookup"><span data-stu-id="c643f-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="c643f-107">[毎日]</span><span class="sxs-lookup"><span data-stu-id="c643f-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c643f-108">テストツール</span><span class="sxs-lookup"><span data-stu-id="c643f-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="c643f-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c643f-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c643f-110">必要なアクセス許可</span><span class="sxs-lookup"><span data-stu-id="c643f-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="c643f-111">Lync Server 管理シェルを使用してローカルで実行する場合、ユーザーは RTCUniversalServerAdmins セキュリティグループのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="c643f-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="c643f-112">Windows PowerShell のリモートインスタンスを使って実行する場合は、 <strong>CsExStorageNotification</strong> コマンドレットを実行するためのアクセス許可が与えられている RBAC の役割をユーザーに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="c643f-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsExStorageNotification</strong> cmdlet.</span></span> <span data-ttu-id="c643f-113">このコマンドレットを使うことができるすべての RBAC ロールの一覧を表示するには、Windows PowerShell プロンプトから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="c643f-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsExStorageNotification&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="c643f-114">説明</span><span class="sxs-lookup"><span data-stu-id="c643f-114">Description</span></span>

<span data-ttu-id="c643f-115">**CsExStorageNotification** コマンドレットを使用して、ユーザーの連絡先リストが更新されたときに、Microsoft Exchange Server 2013 notification Service が Lync Server 2013 に通知することを確認します。</span><span class="sxs-lookup"><span data-stu-id="c643f-115">The **Test-CsExStorageNotification** cmdlet is used to verify that the Microsoft Exchange Server 2013 notification service can notify Lync Server 2013 any time updates are made to a user's Contact List.</span></span> <span data-ttu-id="c643f-116">このコマンドレットは、ユニファイド連絡先ストアを使用している場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="c643f-116">This cmdlet is valid only if you are using the unified contact store.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="c643f-117">テストの実行</span><span class="sxs-lookup"><span data-stu-id="c643f-117">Running the test</span></span>

<span data-ttu-id="c643f-118">例1に示すコマンドは、Lync Server ストレージサービスが、ユーザー sip:kenmyer@litwareinc.com の Microsoft Exchange Server メールボックス通知サービスに接続できるかどうかを確認するものです。</span><span class="sxs-lookup"><span data-stu-id="c643f-118">The command shown in Example 1 tests to see whether the Lync Server Storage Service can connect to the Microsoft Exchange Server mailbox notification service for the user sip:kenmyer@litwareinc.com.</span></span> <span data-ttu-id="c643f-119">この例では、NetNamedPipe は WCF バインディングとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="c643f-119">In this example, NetNamedPipe is used as the WCF binding.</span></span>

    Test-CsExStorageNotification -SipUri "sip:kenmyer@litwareinc.com" -Binding "NetNamedPipe"

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="c643f-120">成功または失敗を確認する</span><span class="sxs-lookup"><span data-stu-id="c643f-120">Determining success or failure</span></span>

<span data-ttu-id="c643f-121">Exchange の統合が正しく構成されている場合は、次のような結果が返され、Result プロパティは **Success** とマークされます。</span><span class="sxs-lookup"><span data-stu-id="c643f-121">If Exchange integration is configured correctly , you'll receive output similar to this, with the Result property marked as **Success**:</span></span>

<span data-ttu-id="c643f-122">ターゲット Fqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="c643f-122">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="c643f-123">結果: 成功</span><span class="sxs-lookup"><span data-stu-id="c643f-123">Result : Success</span></span>

<span data-ttu-id="c643f-124">待ち時間: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="c643f-124">Latency : 00:00:00</span></span>

<span data-ttu-id="c643f-125">エラーメッセージ:</span><span class="sxs-lookup"><span data-stu-id="c643f-125">Error Message :</span></span>

<span data-ttu-id="c643f-126">診断</span><span class="sxs-lookup"><span data-stu-id="c643f-126">Diagnosis :</span></span>

<span data-ttu-id="c643f-127">指定したユーザーが通知を受信できない場合、結果はエラーとして表示され、エラーと診断のプロパティに追加情報が記録されます。</span><span class="sxs-lookup"><span data-stu-id="c643f-127">If the specified user can't receive notifications, the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="c643f-128">ターゲット Fqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="c643f-128">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="c643f-129">結果: エラー</span><span class="sxs-lookup"><span data-stu-id="c643f-129">Result : Failure</span></span>

<span data-ttu-id="c643f-130">待ち時間: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="c643f-130">Latency : 00:00:00</span></span>

<span data-ttu-id="c643f-131">エラーメッセージ: 10060、接続されているパーティのため、接続に失敗しました</span><span class="sxs-lookup"><span data-stu-id="c643f-131">Error Message : 10060, A connection attempt failed because the connected party</span></span>

<span data-ttu-id="c643f-132">一定の期間が経過した後に正しく応答しなかった場合、または</span><span class="sxs-lookup"><span data-stu-id="c643f-132">did not properly respond after a period of time, or</span></span>

<span data-ttu-id="c643f-133">接続されているホストに、接続に失敗しました</span><span class="sxs-lookup"><span data-stu-id="c643f-133">established connection failed because connected host has</span></span>

<span data-ttu-id="c643f-134">10.188.116.96 に応答できませんでした: 5061</span><span class="sxs-lookup"><span data-stu-id="c643f-134">failed to respond 10.188.116.96:5061</span></span>

<span data-ttu-id="c643f-135">内部例外: 接続の試行が失敗したため、接続できませんでした。</span><span class="sxs-lookup"><span data-stu-id="c643f-135">Inner Exception:A connection attempt failed because the</span></span>

<span data-ttu-id="c643f-136">しばらくしても、接続されているパーティが正しく応答しませんでした</span><span class="sxs-lookup"><span data-stu-id="c643f-136">connected party did not properly respond after a period of</span></span>

<span data-ttu-id="c643f-137">接続されているホストが原因で、時刻、または接続に失敗しました</span><span class="sxs-lookup"><span data-stu-id="c643f-137">time, or established connection failed because connected host</span></span>

<span data-ttu-id="c643f-138">さんが10.188.116.96 に応答できませんでした: 5061</span><span class="sxs-lookup"><span data-stu-id="c643f-138">has failed to respond 10.188.116.96:5061</span></span>

<span data-ttu-id="c643f-139">診断</span><span class="sxs-lookup"><span data-stu-id="c643f-139">Diagnosis :</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="c643f-140">テストに失敗した可能性がある理由</span><span class="sxs-lookup"><span data-stu-id="c643f-140">Reasons why the test might have failed</span></span>

<span data-ttu-id="c643f-141">次に **、テスト-CsExStorageNotification** が失敗する可能性がある一般的な理由を示します。</span><span class="sxs-lookup"><span data-stu-id="c643f-141">Here are some common reasons why **Test-CsExStorageNotification** might fail:</span></span>

  - <span data-ttu-id="c643f-142">指定されたパラメーター値が正しくありません。</span><span class="sxs-lookup"><span data-stu-id="c643f-142">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="c643f-143">使用する場合は、オプションのパラメーターが正しく構成されている必要があります。または、テストが失敗します。</span><span class="sxs-lookup"><span data-stu-id="c643f-143">If used, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="c643f-144">省略可能なパラメーターを指定せずにコマンドを再実行し、それが成功するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="c643f-144">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

  - <span data-ttu-id="c643f-145">Microsoft Exchange Server が正しく構成されていないか、まだ展開されていない場合、このコマンドは失敗します。</span><span class="sxs-lookup"><span data-stu-id="c643f-145">This command will fail if the Microsoft Exchange Server is misconfigured or not yet deployed.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="c643f-146">関連項目</span><span class="sxs-lookup"><span data-stu-id="c643f-146">See Also</span></span>


[<span data-ttu-id="c643f-147">Test-CsExStorageConnectivity</span><span class="sxs-lookup"><span data-stu-id="c643f-147">Test-CsExStorageConnectivity</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsExStorageConnectivity)  
  

<span data-ttu-id="c643f-148"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c643f-148"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

