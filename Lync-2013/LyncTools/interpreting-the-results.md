---
title: 結果の解釈
description: 結果を解釈します。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Interpreting the Results
ms:assetid: dd7f199f-7075-4d88-bb84-49a7e05eb593
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945608(v=OCS.15)
ms:contentKeyID: 51541433
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b8342a1ec1e15e42852fc5293f87342e98587a60
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443175"
---
# <a name="interpreting-the-results"></a><span data-ttu-id="6dc25-103">結果の解釈</span><span class="sxs-lookup"><span data-stu-id="6dc25-103">Interpreting the Results</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6dc25-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6dc25-104">

<span> </span></span></span>

<span data-ttu-id="6dc25-105">_**最終更新日:** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="6dc25-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<span data-ttu-id="6dc25-106">Lync Server 2013 応力とパフォーマンスツール (LyncPerfTool.exe) には、クライアントの動作を理解するために使用できる多くのカウンターと、問題が発生しているかどうかが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6dc25-106">The Lync Server 2013 Stress and Performance Tool (LyncPerfTool.exe) has many counters that you can use to understand what the client is doing and whether it is encountering issues.</span></span>

<div>

## <a name="client-counters"></a><span data-ttu-id="6dc25-107">クライアントのカウンター</span><span class="sxs-lookup"><span data-stu-id="6dc25-107">Client Counters</span></span>

<span data-ttu-id="6dc25-108">実行されている LyncPerfTool.exe の各インスタンスには、カウンターの個別のインスタンスがあります。</span><span class="sxs-lookup"><span data-stu-id="6dc25-108">Each instance of LyncPerfTool.exe that is running has a separate instance of the counters.</span></span> <span data-ttu-id="6dc25-109">それぞれのインスタンスには、そのプロセス ID による名前が付けられます。</span><span class="sxs-lookup"><span data-stu-id="6dc25-109">Each instance is named by its process ID.</span></span>

<span data-ttu-id="6dc25-110">クライアントが過負荷になっていると、問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6dc25-110">If the clients are overloaded, issues can occur.</span></span> <span data-ttu-id="6dc25-111">これらの問題を回避するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="6dc25-111">To prevent these issues, do the following:</span></span>

1.  <span data-ttu-id="6dc25-112">クライアントコンピューターの CPU とメモリ使用量を監視します。</span><span class="sxs-lookup"><span data-stu-id="6dc25-112">Monitor the CPU and the memory usage on the client computers.</span></span> <span data-ttu-id="6dc25-113">CPU が継続的に 90% 以上になっている場合は、ユーザーの数を減らします。</span><span class="sxs-lookup"><span data-stu-id="6dc25-113">If the CPU is consistently above 90 percent, reduce the number of users.</span></span>

2.  <span data-ttu-id="6dc25-114">メモリフットプリントが高すぎる場合は、ページファイルが十分でない場合に問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6dc25-114">If the memory footprint is high, you could run into issues if the page file is not big enough.</span></span> <span data-ttu-id="6dc25-115">コミット チャージがコンピューターの制限に達していないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="6dc25-115">Verify that the Commit Charge is not hitting the limit on the computer.</span></span> <span data-ttu-id="6dc25-116">メモリの制限を使用している場合は、ページファイルのサイズを大きくするか、ユーザーの数を減らすことを検討してください。</span><span class="sxs-lookup"><span data-stu-id="6dc25-116">If you are running into memory limits, consider increasing the page file size or reducing the number of users</span></span>

<span data-ttu-id="6dc25-117">次の表では、LyncPerfTool のパフォーマンスカウンターの主要な一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="6dc25-117">The following tables list the key LyncPerfTool performance counters.</span></span>

<span data-ttu-id="6dc25-118">**一般情報**</span><span class="sxs-lookup"><span data-stu-id="6dc25-118">**General Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc25-119"><strong>パフォーマンス カウンター</strong></span><span class="sxs-lookup"><span data-stu-id="6dc25-119"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="6dc25-120"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="6dc25-120"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6dc25-121">Time Spent in Minutes</span><span class="sxs-lookup"><span data-stu-id="6dc25-121">Time Spent in Minutes</span></span></p></td>
<td><p><span data-ttu-id="6dc25-122">プロセスの開始からの経過時間。</span><span class="sxs-lookup"><span data-stu-id="6dc25-122">Time spent since the process was started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dc25-123">Active Endpoints</span><span class="sxs-lookup"><span data-stu-id="6dc25-123">Active Endpoints</span></span></p></td>
<td><p><span data-ttu-id="6dc25-124">現在サーバーに接続しているエンドポイントの数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-124">Number of endpoints currently connected to the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dc25-125">Failed Logons</span><span class="sxs-lookup"><span data-stu-id="6dc25-125">Failed Logons</span></span></p></td>
<td><p><span data-ttu-id="6dc25-126">エンドポイント サインインの合計失敗数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-126">Total number of endpoint sign-in failures.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dc25-127">Logon Attempts</span><span class="sxs-lookup"><span data-stu-id="6dc25-127">Logon Attempts</span></span></p></td>
<td><p><span data-ttu-id="6dc25-128">エンドポイント サインインの合計試行数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-128">Total number of endpoint sign-in attempts.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dc25-129">Endpoints Disconnected</span><span class="sxs-lookup"><span data-stu-id="6dc25-129">Endpoints Disconnected</span></span></p></td>
<td><p><span data-ttu-id="6dc25-130">切断されたエンドポイントの合計数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-130">Total number of endpoints that have been disconnected.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6dc25-131">**プレゼンス情報**</span><span class="sxs-lookup"><span data-stu-id="6dc25-131">**Presence Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc25-132"><strong>パフォーマンス カウンター</strong></span><span class="sxs-lookup"><span data-stu-id="6dc25-132"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="6dc25-133"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="6dc25-133"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6dc25-134">SetPresence Calls</span><span class="sxs-lookup"><span data-stu-id="6dc25-134">SetPresence Calls</span></span></p></td>
<td><p><span data-ttu-id="6dc25-135">プレゼンス変更の合計試行数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-135">Total number of presence change attempts.</span></span> <span data-ttu-id="6dc25-136">プレゼンス変更のさまざまな種類については、SetPresence (プレゼンスの種類) Calls パフォーマンス カウンターを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6dc25-136">For different types of presence changes, see the SetPresence (Presence Type) Calls Performance Counter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dc25-137">NNN Responses for SetPresence</span><span class="sxs-lookup"><span data-stu-id="6dc25-137">NNN Responses for SetPresence</span></span></p></td>
<td><p><span data-ttu-id="6dc25-138">サーバーから受信した nnn 応答コードの合計数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-138">Total number of nnn response codes received from the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dc25-139">GetPresence Calls</span><span class="sxs-lookup"><span data-stu-id="6dc25-139">GetPresence Calls</span></span></p></td>
<td><p><span data-ttu-id="6dc25-140">プレゼンス取得要求の合計試行数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-140">Total number of get presence request attempts.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dc25-141">NNN Responses for GetPresence</span><span class="sxs-lookup"><span data-stu-id="6dc25-141">NNN Responses for GetPresence</span></span></p></td>
<td><p><span data-ttu-id="6dc25-142">サーバーから受信した nnn 応答コードの合計数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-142">Total number of nnn response codes received from the server.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6dc25-143">**アドレス帳サービス情報**</span><span class="sxs-lookup"><span data-stu-id="6dc25-143">**Address Book service Information**</span></span>

<span data-ttu-id="6dc25-144">このカテゴリには、アドレス帳サービス (ABS) のファイル ダウンロードとアドレス帳 Web クエリ サービスの要求を監視するために使用するカウンターが含まれています。</span><span class="sxs-lookup"><span data-stu-id="6dc25-144">This category includes counters used to monitor Address Book service (ABS) file downloads and Address Book Web Query service requests.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc25-145"><strong>パフォーマンス カウンター</strong></span><span class="sxs-lookup"><span data-stu-id="6dc25-145"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="6dc25-146"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="6dc25-146"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6dc25-147">ABS Full/Delta File Downloads Attempted</span><span class="sxs-lookup"><span data-stu-id="6dc25-147">ABS Full/Delta File Downloads Attempted</span></span></p></td>
<td><p><span data-ttu-id="6dc25-148">試行された完全または差分ファイル ダウンロード要求の合計数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-148">Total number of full or delta file download requests attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dc25-149">ABS Full/Delta File Downloads Succeeded</span><span class="sxs-lookup"><span data-stu-id="6dc25-149">ABS Full/Delta File Downloads Succeeded</span></span></p></td>
<td><p><span data-ttu-id="6dc25-150">試行された完全または差分ファイル ダウンロード要求の合計数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-150">Total number of full or delta file download requests attempted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dc25-151">アドレス帳 Web クエリ サービスに関連するカウンター</span><span class="sxs-lookup"><span data-stu-id="6dc25-151">Address Book Web Query service related counters</span></span></p></td>
<td><p><span data-ttu-id="6dc25-152">アドレス帳ファイルのダウンロードに関連するカウンター。</span><span class="sxs-lookup"><span data-stu-id="6dc25-152">Address book file download related counters.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dc25-153">ABS WS Calls attempted</span><span class="sxs-lookup"><span data-stu-id="6dc25-153">ABS WS Calls attempted</span></span></p></td>
<td><p><span data-ttu-id="6dc25-154">試行したアドレス帳 Web クエリ サービス要求の合計数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-154">Total number of Address Book Web Query service requests attempted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dc25-155">ABS WS Calls Succeeded</span><span class="sxs-lookup"><span data-stu-id="6dc25-155">ABS WS Calls Succeeded</span></span></p></td>
<td><p><span data-ttu-id="6dc25-156">成功応答コードを返したアドレス帳 Web クエリ サービス要求の合計数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-156">Total number of Address Book Web Query service requests that returned a successful response code.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dc25-157">ABS WS Calls Failed</span><span class="sxs-lookup"><span data-stu-id="6dc25-157">ABS WS Calls Failed</span></span></p></td>
<td><p><span data-ttu-id="6dc25-158">エラー応答コードを返したアドレス帳 Web クエリ サービスの合計数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-158">Total number of Address Book Web Query service requests that returned an error response code.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6dc25-159">**配布リスト (DL) の情報**</span><span class="sxs-lookup"><span data-stu-id="6dc25-159">**Distribution List (DL) Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc25-160"><strong>パフォーマンス カウンター</strong></span><span class="sxs-lookup"><span data-stu-id="6dc25-160"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="6dc25-161"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="6dc25-161"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6dc25-162">Calls Attempted</span><span class="sxs-lookup"><span data-stu-id="6dc25-162">Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="6dc25-163">試行した配布リスト展開 (DLX) Web サービス要求の合計数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-163">Total number of distribution list expansion (DLX) web service requests attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dc25-164">Calls Succeeded</span><span class="sxs-lookup"><span data-stu-id="6dc25-164">Calls Succeeded</span></span></p></td>
<td><p><span data-ttu-id="6dc25-165">成功応答コードを返した DLX Web サービス要求の合計数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-165">Total number of DLX web service requests that returned a successful response code.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dc25-166">Calls Failed</span><span class="sxs-lookup"><span data-stu-id="6dc25-166">Calls Failed</span></span></p></td>
<td><p><span data-ttu-id="6dc25-167">エラー応答コードを返した DLX Web サービス要求の合計数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-167">Total number of DLX web service requests that returned an error response code.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6dc25-168">**VoIP の基本情報**</span><span class="sxs-lookup"><span data-stu-id="6dc25-168">**VoIP Basic Information**</span></span>

<span data-ttu-id="6dc25-169">次に示す各パフォーマンス カウンターは、すべての Voice over IP (VoIP) の通話数を報告します。これには、仲介サーバー、音声ビデオ会議サーバー、エッジ サーバー、応答グループ アプリケーション、および電話会議自動応答に対する通話が含まれます (これらのシナリオが有効な場合)。</span><span class="sxs-lookup"><span data-stu-id="6dc25-169">The performance counters listed below report numbers for all Voice over IP (VoIP) calls, including calls to Mediation Server, A/V Conferencing Server, Edge Server, Response Group application, and Conference Auto Attendant, when these scenarios are enabled.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc25-170"><strong>パフォーマンス カウンター</strong></span><span class="sxs-lookup"><span data-stu-id="6dc25-170"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="6dc25-171"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="6dc25-171"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6dc25-172">Calls Active</span><span class="sxs-lookup"><span data-stu-id="6dc25-172">Calls Active</span></span></p></td>
<td><p><span data-ttu-id="6dc25-173">現在進行中の着信/発信音声通話の合計数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-173">Total number of incoming/outgoing voice calls ongoing currently.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dc25-174">Calls Terminated</span><span class="sxs-lookup"><span data-stu-id="6dc25-174">Calls Terminated</span></span></p></td>
<td><p><span data-ttu-id="6dc25-175">既に終了している着信/発信音声通話の合計数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-175">Total number of incoming/outgoing voice calls already terminated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dc25-176">Calls Declined</span><span class="sxs-lookup"><span data-stu-id="6dc25-176">Calls Declined</span></span></p></td>
<td><p><span data-ttu-id="6dc25-177">拒否した着信音声通話の合計数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-177">Total number of incoming voice calls declined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dc25-178">Incoming/Outgoing Calls Attempted</span><span class="sxs-lookup"><span data-stu-id="6dc25-178">Incoming/Outgoing Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="6dc25-179">試行した着信/発信音声通話の合計数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-179">Total number of incoming/outgoing voice calls attempted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dc25-180">Incoming/Outgoing Calls Established</span><span class="sxs-lookup"><span data-stu-id="6dc25-180">Incoming/Outgoing Calls Established</span></span></p></td>
<td><p><span data-ttu-id="6dc25-181">成立した着信/発信音声通話の合計数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-181">Total number of incoming/outgoing voice calls established.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dc25-182">Calls Received NNN</span><span class="sxs-lookup"><span data-stu-id="6dc25-182">Calls Received NNN</span></span></p></td>
<td><p><span data-ttu-id="6dc25-183">サーバーから受信した nnn 応答コードの合計数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-183">Total number of nnn response codes received from the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dc25-184">VoIP Pass Rate (%)</span><span class="sxs-lookup"><span data-stu-id="6dc25-184">VoIP Pass Rate (%)</span></span></p></td>
<td><p><span data-ttu-id="6dc25-185">成立した通話の合計/試行した通話の合計。</span><span class="sxs-lookup"><span data-stu-id="6dc25-185">Total calls established/Total calls attempted.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6dc25-186">**応答グループ サービス通話の情報**</span><span class="sxs-lookup"><span data-stu-id="6dc25-186">**Response Group service Call Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc25-187"><strong>パフォーマンス カウンター</strong></span><span class="sxs-lookup"><span data-stu-id="6dc25-187"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="6dc25-188"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="6dc25-188"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6dc25-189">Calls Active</span><span class="sxs-lookup"><span data-stu-id="6dc25-189">Calls Active</span></span></p></td>
<td><p><span data-ttu-id="6dc25-190">応答グループ アプリケーションへのアクティブな通話の合計数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-190">Total number of active calls to the Response Group application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dc25-191">Calls Attempted</span><span class="sxs-lookup"><span data-stu-id="6dc25-191">Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="6dc25-192">試行した通話の合計数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-192">Total number of calls attempted.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6dc25-193">**インスタント メッセージング (IM) 通話の情報**</span><span class="sxs-lookup"><span data-stu-id="6dc25-193">**Instant Messaging (IM) Call Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc25-194"><strong>パフォーマンス カウンター</strong></span><span class="sxs-lookup"><span data-stu-id="6dc25-194"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="6dc25-195"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="6dc25-195"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6dc25-196">Calls Active</span><span class="sxs-lookup"><span data-stu-id="6dc25-196">Calls Active</span></span></p></td>
<td><p><span data-ttu-id="6dc25-197">進行中の着信/発信インスタント メッセージング通話の合計数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-197">Total number of ongoing incoming/outgoing instant messaging calls.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dc25-198">Calls Terminated</span><span class="sxs-lookup"><span data-stu-id="6dc25-198">Calls Terminated</span></span></p></td>
<td><p><span data-ttu-id="6dc25-199">既に終了している着信/発信インスタント メッセージング通話の合計数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-199">Total number of incoming/outgoing instant messaging calls already terminated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dc25-200">Calls Received NNN</span><span class="sxs-lookup"><span data-stu-id="6dc25-200">Calls Received NNN</span></span></p></td>
<td><p><span data-ttu-id="6dc25-201">サーバーから受信した nnn 応答コードの合計数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-201">Total number of nnn response codes received from the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dc25-202">IM Messages Received/Sent</span><span class="sxs-lookup"><span data-stu-id="6dc25-202">IM Messages Received/Sent</span></span></p></td>
<td><p><span data-ttu-id="6dc25-203">すべてのセッションで受信または送信したメッセージの合計数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-203">Total number of messages received or sent for all sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dc25-204">Incoming/Outgoing Calls Attempted</span><span class="sxs-lookup"><span data-stu-id="6dc25-204">Incoming/Outgoing Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="6dc25-205">試行した着信/発信インスタント メッセージング通話の合計数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-205">Total number of incoming/outgoing instant messaging calls attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dc25-206">Incoming/Outgoing Calls Established</span><span class="sxs-lookup"><span data-stu-id="6dc25-206">Incoming/Outgoing Calls Established</span></span></p></td>
<td><p><span data-ttu-id="6dc25-207">成立した着信/発信インスタント メッセージ通話の合計数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-207">Total number of incoming/outgoing instant message calls established.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6dc25-208">**アプリケーション共有通話の情報**</span><span class="sxs-lookup"><span data-stu-id="6dc25-208">**App Sharing Call Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc25-209"><strong>パフォーマンス カウンター</strong></span><span class="sxs-lookup"><span data-stu-id="6dc25-209"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="6dc25-210"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="6dc25-210"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6dc25-211">Calls Active</span><span class="sxs-lookup"><span data-stu-id="6dc25-211">Calls Active</span></span></p></td>
<td><p><span data-ttu-id="6dc25-212">進行中の着信/発信アプリケーション共有通話の合計数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-212">Total number of ongoing incoming/outgoing application sharing calls.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dc25-213">Calls Terminated</span><span class="sxs-lookup"><span data-stu-id="6dc25-213">Calls Terminated</span></span></p></td>
<td><p><span data-ttu-id="6dc25-214">既に終了している着信/発信アプリケーション共有通話の合計数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-214">Total number of incoming/outgoing application sharing calls already terminated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dc25-215">Calls Received NNN</span><span class="sxs-lookup"><span data-stu-id="6dc25-215">Calls Received NNN</span></span></p></td>
<td><p><span data-ttu-id="6dc25-216">サーバーから受信した nnn 応答コードの合計数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-216">Total number of nnn response codes received from the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dc25-217">Incoming/Outgoing Calls Attempted</span><span class="sxs-lookup"><span data-stu-id="6dc25-217">Incoming/Outgoing Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="6dc25-218">試行した着信/発信アプリケーション共有通話の合計数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-218">Total number of incoming/outgoing application sharing calls attempted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dc25-219">Incoming/Outgoing Calls Established</span><span class="sxs-lookup"><span data-stu-id="6dc25-219">Incoming/Outgoing Calls Established</span></span></p></td>
<td><p><span data-ttu-id="6dc25-220">成立した着信/発信アプリケーション共有通話の合計数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-220">Total number of incoming/outgoing application sharing calls established.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6dc25-221">**CAA 通話の情報**</span><span class="sxs-lookup"><span data-stu-id="6dc25-221">**CAA Call Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc25-222"><strong>パフォーマンス カウンター</strong></span><span class="sxs-lookup"><span data-stu-id="6dc25-222"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="6dc25-223"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="6dc25-223"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6dc25-224">Calls Active</span><span class="sxs-lookup"><span data-stu-id="6dc25-224">Calls Active</span></span></p></td>
<td><p><span data-ttu-id="6dc25-225">現在進行中の着信/発信公衆交換電話網 (PSTN) 通話の合計数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-225">Total number of incoming/outgoing public switched telephone network (PSTN) calls ongoing currently.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dc25-226">Calls Terminated</span><span class="sxs-lookup"><span data-stu-id="6dc25-226">Calls Terminated</span></span></p></td>
<td><p><span data-ttu-id="6dc25-227">既に終了している着信/発信 PSTN 通話の合計数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-227">Total number of incoming/outgoing PSTN calls already terminated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dc25-228">Incoming/Outgoing Calls Attempted</span><span class="sxs-lookup"><span data-stu-id="6dc25-228">Incoming/Outgoing Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="6dc25-229">試行した着信/発信 PSTN 通話の合計数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-229">Total number of incoming/outgoing PSTN calls attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dc25-230">Incoming/Outgoing Calls Established</span><span class="sxs-lookup"><span data-stu-id="6dc25-230">Incoming/Outgoing Calls Established</span></span></p></td>
<td><p><span data-ttu-id="6dc25-231">成立した着信/発信 PSTN 通話の合計数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-231">Total number of incoming/outgoing PSTN calls established.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6dc25-232">**会議通話の情報**</span><span class="sxs-lookup"><span data-stu-id="6dc25-232">**Conference Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc25-233"><strong>パフォーマンス カウンター</strong></span><span class="sxs-lookup"><span data-stu-id="6dc25-233"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="6dc25-234"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="6dc25-234"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6dc25-235">Active Instant Messaging Conferences</span><span class="sxs-lookup"><span data-stu-id="6dc25-235">Active Instant Messaging Conferences</span></span></p></td>
<td><p><span data-ttu-id="6dc25-236">進行中のインスタント メッセージング会議通話の合計数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-236">Total number of ongoing instant messaging conferences.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dc25-237">Active Audio/Video Conferences</span><span class="sxs-lookup"><span data-stu-id="6dc25-237">Active Audio/Video Conferences</span></span></p></td>
<td><p><span data-ttu-id="6dc25-238">進行中の音声ビデオ (A/V) 会議通話の合計数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-238">Total number of ongoing audio/video (A/V) conferences.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dc25-239">Active Application Sharing Conferences</span><span class="sxs-lookup"><span data-stu-id="6dc25-239">Active Application Sharing Conferences</span></span></p></td>
<td><p><span data-ttu-id="6dc25-240">進行中のアプリケーション共有会議通話の合計数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-240">Total number of ongoing application sharing conferences.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dc25-241">Number of Participants</span><span class="sxs-lookup"><span data-stu-id="6dc25-241">Number of Participants</span></span></p></td>
<td><p><span data-ttu-id="6dc25-242">会議通話に現在接続している参加者の合計数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-242">Total number of participants currently connected to conferences.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dc25-243">Conference Schedule Failure</span><span class="sxs-lookup"><span data-stu-id="6dc25-243">Conference Schedule Failure</span></span></p></td>
<td><p><span data-ttu-id="6dc25-244">会議通話のスケジュールに失敗した合計回数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-244">Total number of failures while trying to schedule a conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dc25-245">Join Conference Failure</span><span class="sxs-lookup"><span data-stu-id="6dc25-245">Join Conference Failure</span></span></p></td>
<td><p><span data-ttu-id="6dc25-246">会議通話への接続に失敗した合計回数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-246">Total number of failures while trying to connect to a conference.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6dc25-247">**UCWA クライアントのカウンター**</span><span class="sxs-lookup"><span data-stu-id="6dc25-247">**UCWA Client Counters**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc25-248"><strong>パフォーマンス カウンター</strong></span><span class="sxs-lookup"><span data-stu-id="6dc25-248"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="6dc25-249"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="6dc25-249"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6dc25-250">Total Number of IMMCU Joins Succeeded</span><span class="sxs-lookup"><span data-stu-id="6dc25-250">Total Number of IMMCU Joins Succeeded</span></span></p></td>
<td><p><span data-ttu-id="6dc25-251">参加したインスタント メッセージング会議通話の合計数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-251">Total number of instant messaging conferences joined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dc25-252">Total Number of DMCU Joins Succeeded</span><span class="sxs-lookup"><span data-stu-id="6dc25-252">Total Number of DMCU Joins Succeeded</span></span></p></td>
<td><p><span data-ttu-id="6dc25-253">参加した音声ビデオ会議通話の合計数。</span><span class="sxs-lookup"><span data-stu-id="6dc25-253">Total number of A/V conferences joined.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="6dc25-254">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6dc25-254">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

