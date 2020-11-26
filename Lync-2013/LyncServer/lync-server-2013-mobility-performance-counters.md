---
title: 'Lync Server 2013: モビリティーパフォーマンスカウンター'
description: 'Lync Server 2013: モビリティーパフォーマンスカウンター。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Mobility performance counters
ms:assetid: d18ed85a-673d-4695-aa3f-ac83a38ab90a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690046(v=OCS.15)
ms:contentKeyID: 48185441
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 922288f6c026f088d651dc61afdcb6ba04fed30a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425557"
---
# <a name="mobility-performance-counters-in-lync-server-2013"></a><span data-ttu-id="e9f7a-103">Lync Server 2013 のモバイルパフォーマンスカウンター</span><span class="sxs-lookup"><span data-stu-id="e9f7a-103">Mobility performance counters in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e9f7a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e9f7a-104">

<span> </span></span></span>

<span data-ttu-id="e9f7a-105">_**最終更新日:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="e9f7a-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="e9f7a-106">次の表は、ユニファイドコミュニケーション Web API (UCWA) および Lync Server 2013 Mcx Mobility Service を実行しているサーバーを監視するために使用できるパフォーマンスカウンターの名前と説明を示しています。</span><span class="sxs-lookup"><span data-stu-id="e9f7a-106">The following tables list the names and descriptions of performance counters that you can use to monitor servers running the Unified Communications Web API (UCWA) and the Lync Server 2013 Mcx Mobility Service.</span></span>

<span data-ttu-id="e9f7a-107">UCWA の表のカウンターのカテゴリ名は、**LS:WEB - UCWA** です。</span><span class="sxs-lookup"><span data-stu-id="e9f7a-107">The category name for the counters in the UCWA table is **LS:WEB – UCWA**.</span></span>

<span data-ttu-id="e9f7a-108">Mcx Mobility Service の表のカウンターのカテゴリ名は、**LS:WEB - Mobile Communication Service** です。</span><span class="sxs-lookup"><span data-stu-id="e9f7a-108">The category name for the counters in the Mcx Mobility Service table is **LS:WEB - Mobile Communication Service**.</span></span>

<div>

## <a name="performance-counters-for-ucwa"></a><span data-ttu-id="e9f7a-109">UCWA のパフォーマンス カウンター</span><span class="sxs-lookup"><span data-stu-id="e9f7a-109">Performance Counters for UCWA</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e9f7a-110">カウンター</span><span class="sxs-lookup"><span data-stu-id="e9f7a-110">Counter</span></span></th>
<th><span data-ttu-id="e9f7a-111">説明</span><span class="sxs-lookup"><span data-stu-id="e9f7a-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e9f7a-112">Active Application Count</span><span class="sxs-lookup"><span data-stu-id="e9f7a-112">Active Application Count</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-113">現在のアプリケーション数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-113">The current number of applications</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9f7a-114">Active Application Sharing Modality Count</span><span class="sxs-lookup"><span data-stu-id="e9f7a-114">Active Application Sharing Modality Count</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-115">現在のアプリケーション共有モダリティ数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-115">The current number of Application Sharing modality</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9f7a-116">Active Audio Modality Count</span><span class="sxs-lookup"><span data-stu-id="e9f7a-116">Active Audio Modality Count</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-117">現在の音声モダリティ数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-117">The current number of Audio modality</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9f7a-118">Active Data Collaboration Modality Count</span><span class="sxs-lookup"><span data-stu-id="e9f7a-118">Active Data Collaboration Modality Count</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-119">現在のデータの共同作業モダリティ数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-119">The current number of Data Collaboration modality</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9f7a-120">Active Directory Photo Get Latency (ms)</span><span class="sxs-lookup"><span data-stu-id="e9f7a-120">Active Directory Photo Get Latency (ms)</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-121">このカウンターは、Active Directory から写真を取得する平均時間 (ミリ秒) を示します</span><span class="sxs-lookup"><span data-stu-id="e9f7a-121">This counter shows the average time (in milliseconds) to retrieve a photo from active directory</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9f7a-122">Active Messaging Modality Count</span><span class="sxs-lookup"><span data-stu-id="e9f7a-122">Active Messaging Modality Count</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-123">現在のメッセージング モダリティ数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-123">The current number of Messaging modality</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9f7a-124">Active Panoramic Video Modality Count</span><span class="sxs-lookup"><span data-stu-id="e9f7a-124">Active Panoramic Video Modality Count</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-125">現在のパノラマ ビデオ モダリティ数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-125">The current number of Panoramic Video modality</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9f7a-126">Active Pending Get Count</span><span class="sxs-lookup"><span data-stu-id="e9f7a-126">Active Pending Get Count</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-127">現在アクティブな保留中の取得数。サーバーへの接続は長時間維持されます</span><span class="sxs-lookup"><span data-stu-id="e9f7a-127">The number of currently active pending gets; long-held connections to the server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9f7a-128">Active Session Count</span><span class="sxs-lookup"><span data-stu-id="e9f7a-128">Active Session Count</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-129">アプリケーションごとに UCWA に登録されている現在のエンドポイント数と合計数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-129">The current number of endpoints registered in UCWA per application and total</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9f7a-130">Active User Instance Count</span><span class="sxs-lookup"><span data-stu-id="e9f7a-130">Active User Instance Count</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-131">現在のユーザー インスタンス数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-131">The current number of user instances</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9f7a-132">Active User Instances without Application</span><span class="sxs-lookup"><span data-stu-id="e9f7a-132">Active User Instances without Application</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-133">現在のユーザー インスタンス数 (アプリケーションを含まない)</span><span class="sxs-lookup"><span data-stu-id="e9f7a-133">The current number of user instances without application</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9f7a-134">Active Video Modality Count</span><span class="sxs-lookup"><span data-stu-id="e9f7a-134">Active Video Modality Count</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-135">現在のビデオ モダリティ数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-135">The current number of Video modality</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9f7a-136">Application Creation Requests Received/Second</span><span class="sxs-lookup"><span data-stu-id="e9f7a-136">Application Creation Requests Received/Second</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-137">受信したアプリケーション作成要求の 1 秒あたりの数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-137">The per second rate of received application creation requests</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9f7a-138">AS MCU Join Failures</span><span class="sxs-lookup"><span data-stu-id="e9f7a-138">AS MCU Join Failures</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-139">AS MCU 参加に失敗した数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-139">The number of AS MCU Join Failures</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9f7a-140">AV MCU Join Failures</span><span class="sxs-lookup"><span data-stu-id="e9f7a-140">AV MCU Join Failures</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-141">AV MCU 参加に失敗した数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-141">The number of AV MCU Join Failures</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9f7a-142">Average Application Startup Time (ms)</span><span class="sxs-lookup"><span data-stu-id="e9f7a-142">Average Application Startup Time (ms)</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-143">アプリケーションの平均起動時間 (ミリ秒)</span><span class="sxs-lookup"><span data-stu-id="e9f7a-143">The average application startup time in Milliseconds</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9f7a-144">Average Lifetime for Session (ms)</span><span class="sxs-lookup"><span data-stu-id="e9f7a-144">Average Lifetime for Session (ms)</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-145">セッションの平均存続期間 (ミリ秒)</span><span class="sxs-lookup"><span data-stu-id="e9f7a-145">The average lifetime for a session in milliseconds</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9f7a-146">Data MCU Join Failures</span><span class="sxs-lookup"><span data-stu-id="e9f7a-146">Data MCU Join Failures</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-147">Data MCU 参加に失敗した数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-147">The number of Data MCU Join Failures</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9f7a-148">Exchange Contact Search Latency (ms)</span><span class="sxs-lookup"><span data-stu-id="e9f7a-148">Exchange Contact Search Latency (ms)</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-149">このカウンターは、Exchange 内の連絡先を検索する平均時間 (ミリ秒) を示します</span><span class="sxs-lookup"><span data-stu-id="e9f7a-149">This counter shows the average time (in milliseconds) to search contact in Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9f7a-150">Exchange HD Photo Get Latency (ms)</span><span class="sxs-lookup"><span data-stu-id="e9f7a-150">Exchange HD Photo Get Latency (ms)</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-151">このカウンターは、Exchange から写真を取得する平均時間 (ミリ秒) を示します</span><span class="sxs-lookup"><span data-stu-id="e9f7a-151">This counter shows the average time (in milliseconds) to retrieve a photo from Exchange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9f7a-152">HTTP 4xx Responses/Second</span><span class="sxs-lookup"><span data-stu-id="e9f7a-152">HTTP 4xx Responses/Second</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-153">HTTP 4xx コードでの応答の 1 秒あたりの数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-153">The per second rate of responses with HTTP 4xx code</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9f7a-154">HTTP 5xx Responses/Second</span><span class="sxs-lookup"><span data-stu-id="e9f7a-154">HTTP 5xx Responses/Second</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-155">HTTP 5xx コードでの応答の 1 秒あたりの数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-155">The per second rate of responses with HTTP 5xx code</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9f7a-156">IM MCU Join Failures</span><span class="sxs-lookup"><span data-stu-id="e9f7a-156">IM MCU Join Failures</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-157">IM MCU 参加に失敗した数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-157">The number of IM MCU Join Failures</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9f7a-158">Number of Active Directory Photo Get Failures</span><span class="sxs-lookup"><span data-stu-id="e9f7a-158">Number of Active Directory Photo Get Failures</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-159">Active Directory からの写真の取得に失敗した合計数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-159">The total number of failures to retrieve photos from Active Directory</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9f7a-160">Number of Contact Search failures</span><span class="sxs-lookup"><span data-stu-id="e9f7a-160">Number of Contact Search failures</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-161">Exchange の連絡先の検索に失敗した合計数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-161">The total number of failures to search contacts in Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9f7a-162">Number of Deserialization Failures</span><span class="sxs-lookup"><span data-stu-id="e9f7a-162">Number of Deserialization Failures</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-163">シリアル化解除が失敗した合計数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-163">The total number of deserialization failures</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9f7a-164">HD Photo Get エラーの数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-164">Number of HD Photo Get Failures</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-165">Exchange からの HD 写真の取得に失敗した合計数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-165">The total number of failures to retrieve HD photos from Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9f7a-166">Over The Maximum Subscriptions Per Application</span><span class="sxs-lookup"><span data-stu-id="e9f7a-166">Over The Maximum Subscriptions Per Application</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-167">アプリケーションごとに許可された最大値を超えるサブスクリプション要求の数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-167">The number of Subscription requests over the maximum allowed per application</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9f7a-168">Over The Maximum Subscriptions Per Batch</span><span class="sxs-lookup"><span data-stu-id="e9f7a-168">Over The Maximum Subscriptions Per Batch</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-169">バッチごとに許可された最大値を超えるサブスクリプション要求の数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-169">The number of Subscription requests over the maximum allowed per batch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9f7a-170">Presence Subscription Failures</span><span class="sxs-lookup"><span data-stu-id="e9f7a-170">Presence Subscription Failures</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-171">プレゼンスの登録に失敗した数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-171">The number of failures to subscribe presence</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9f7a-172">Registering Endpoint Failures</span><span class="sxs-lookup"><span data-stu-id="e9f7a-172">Registering Endpoint Failures</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-173">エンドポイントの登録に失敗した数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-173">The number of failures to register endpoints</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9f7a-174">Requests Received/Second</span><span class="sxs-lookup"><span data-stu-id="e9f7a-174">Requests Received/Second</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-175">受信した要求の 1 秒あたりの数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-175">The per second rate of received requests</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9f7a-176">Requests Succeeded/Second</span><span class="sxs-lookup"><span data-stu-id="e9f7a-176">Requests Succeeded/Second</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-177">成功した要求 (HTTP 2xx/3xx 応答コード) の 1 秒あたりの数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-177">The per second rate of successful requests (HTTP 2xx/3xx response codes)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9f7a-178">Succeeded Create Application Requests/Second</span><span class="sxs-lookup"><span data-stu-id="e9f7a-178">Succeeded Create Application Requests/Second</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-179">成功したアプリケーション作成要求の 1 秒あたりの数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-179">The per second rate of successful application creation requests</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9f7a-180">Timed Out Pending Get Count</span><span class="sxs-lookup"><span data-stu-id="e9f7a-180">Timed Out Pending Get Count</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-181">タイムアウトした保留中の取得の数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-181">The number of pending gets that timed out</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9f7a-182">Total Application Creation Requests Received</span><span class="sxs-lookup"><span data-stu-id="e9f7a-182">Total Application Creation Requests Received</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-183">サービスの開始以降に受信したアプリケーション作成要求の合計数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-183">The total number of application creation requests received since the service was started</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9f7a-184">Total HTTP 4xx Responses</span><span class="sxs-lookup"><span data-stu-id="e9f7a-184">Total HTTP 4xx Responses</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-185">HTTP 4xx 応答の合計数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-185">The total number of HTTP 4xx responses</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9f7a-186">Total HTTP 5xx Responses</span><span class="sxs-lookup"><span data-stu-id="e9f7a-186">Total HTTP 5xx Responses</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-187">HTTP 5xx 応答の合計数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-187">The total number of HTTP 5xx responses</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9f7a-188">Total Requests Received on the Command Channel</span><span class="sxs-lookup"><span data-stu-id="e9f7a-188">Total Requests Received on the Command Channel</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-189">コマンド チャネルで受信した要求の合計数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-189">The total number of requests received on the command channel</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9f7a-190">Total Requests Succeeded</span><span class="sxs-lookup"><span data-stu-id="e9f7a-190">Total Requests Succeeded</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-191">成功した要求の合計数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-191">The total number of requests that succeeded</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9f7a-192">Total Sessions Initiated</span><span class="sxs-lookup"><span data-stu-id="e9f7a-192">Total Sessions Initiated</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-193">サービスが開始されてから起動されたセッションの合計数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-193">The total number of sessions that were initiated since the service was started</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9f7a-194">Total Sessions Terminated Because of Idle Timeout</span><span class="sxs-lookup"><span data-stu-id="e9f7a-194">Total Sessions Terminated Because of Idle Timeout</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-195">ユーザーのアイドル タイムアウトが原因で終了したセッションの合計数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-195">The total number of sessions that were terminated because of user idle timeout</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9f7a-196">Total Throttled Applications</span><span class="sxs-lookup"><span data-stu-id="e9f7a-196">Total Throttled Applications</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-197">制限されたアプリケーションの数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-197">The number of throttled applications</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div id="sectionSection1" class="section">

### <a name="performance-counters-for-mcx-mobility-service"></a><span data-ttu-id="e9f7a-198">Mcx Mobility Service のパフォーマンス カウンター</span><span class="sxs-lookup"><span data-stu-id="e9f7a-198">Performance Counters for Mcx Mobility Service</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e9f7a-199">カウンター</span><span class="sxs-lookup"><span data-stu-id="e9f7a-199">Counter</span></span></th>
<th><span data-ttu-id="e9f7a-200">説明</span><span class="sxs-lookup"><span data-stu-id="e9f7a-200">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e9f7a-201">Average Lifetime for a Session in Milliseconds</span><span class="sxs-lookup"><span data-stu-id="e9f7a-201">Average Lifetime for a Session in Milliseconds</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-202">セッションの平均存続期間 (ミリ秒)</span><span class="sxs-lookup"><span data-stu-id="e9f7a-202">The average lifetime for a session in milliseconds</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9f7a-203">Current Push Notification Subscriptions</span><span class="sxs-lookup"><span data-stu-id="e9f7a-203">Current Push Notification Subscriptions</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-p101">プッシュ通知サブスクリプションの現在の数。この数は、Currently Active Session Count と連携して、Windows Mobile または iPhone のデバイスに登録された現在アクティブなセッションのサブセットを表します。</span><span class="sxs-lookup"><span data-stu-id="e9f7a-p101">The current number of push notification subscriptions. This number, in conjunction with Currently Active Session Count, represents the subset of currently active sessions that are registered for Windows Mobile or iPhone devices.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9f7a-206">Currently Active Network Timeout Poll Count</span><span class="sxs-lookup"><span data-stu-id="e9f7a-206">Currently Active Network Timeout Poll Count</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-207">タイムアウトしたネットワーク ポーリングの数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-207">The number of network polls that timed out</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9f7a-208">Currently Active Poll Count</span><span class="sxs-lookup"><span data-stu-id="e9f7a-208">Currently Active Poll Count</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-209">現在アクティブなポーリングの数 (長時間維持されるサーバーとの接続)</span><span class="sxs-lookup"><span data-stu-id="e9f7a-209">The number of currently active polls (long-held connections to the server)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9f7a-210">Currently Active Session Count</span><span class="sxs-lookup"><span data-stu-id="e9f7a-210">Currently Active Session Count</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-211">Mobility Service に登録されたエンドポイントの現在の数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-211">Current number of endpoints registered in the Mobility Service</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9f7a-212">Currently Active Session Count with Active Presence Subscriptions</span><span class="sxs-lookup"><span data-stu-id="e9f7a-212">Currently Active Session Count with Active Presence Subscriptions</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-213">アクティブなプレゼンス サブスクリプションのある現在アクティブなセッションの数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-213">The number of currently active sessions with active presence subscriptions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9f7a-214">Push Notification Requests Failed/Second</span><span class="sxs-lookup"><span data-stu-id="e9f7a-214">Push Notification Requests Failed/Second</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-215">失敗したプッシュ通知の 1 秒あたりの数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-215">The per second rate of failed push notifications</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9f7a-216">Push Notification Requests Succeeded/Second</span><span class="sxs-lookup"><span data-stu-id="e9f7a-216">Push Notification Requests Succeeded/Second</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-217">成功したプッシュ通知の 1 秒あたりの数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-217">The per second rate of successful push notifications</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9f7a-218">Push Notification Requests Throttled/Second</span><span class="sxs-lookup"><span data-stu-id="e9f7a-218">Push Notification Requests Throttled/Second</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-219">調整済みのプッシュ通知の 1 秒あたりの数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-219">The per second rate of throttled push notifications</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9f7a-220">Push Notification Requests/Second</span><span class="sxs-lookup"><span data-stu-id="e9f7a-220">Push Notification Requests/Second</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-221">送信されたプッシュ通知の 1 秒あたりの数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-221">The per second rate of sent push notifications</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9f7a-222">Requests Failed/Second</span><span class="sxs-lookup"><span data-stu-id="e9f7a-222">Requests Failed/Second</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-223">失敗した要求の 1 秒あたりの数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-223">The per second rate of failed requests</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9f7a-224">Requests Received/Second</span><span class="sxs-lookup"><span data-stu-id="e9f7a-224">Requests Received/Second</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-225">受信した要求の 1 秒あたりの数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-225">The per second rate of received requests</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9f7a-226">Requests Rejected/Second</span><span class="sxs-lookup"><span data-stu-id="e9f7a-226">Requests Rejected/Second</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-227">拒否された要求の 1 秒あたりの数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-227">The per second rate of rejected requests</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9f7a-228">Requests Succeeded/Second</span><span class="sxs-lookup"><span data-stu-id="e9f7a-228">Requests Succeeded/Second</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-229">成功した要求の 1 秒あたりの数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-229">The per second rate of successful requests</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9f7a-230">Succeeded Initiate Session Requests/Second</span><span class="sxs-lookup"><span data-stu-id="e9f7a-230">Succeeded Initiate Session Requests/Second</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-p102">成功した Get Location 要求の 1 秒あたりの数。セッションを開始する要求は、サーバー上の大部分の CPU を消費します。ピーク時にサポートされるロードは 12/秒です。持続可能性は、サーバー上の他のロードによって異なります。セッションの開始は、通常、長時間サインアウトしていたユーザーのサインインを意味します。</span><span class="sxs-lookup"><span data-stu-id="e9f7a-p102">The per second rate of successful Get Location requests. Requests to initiate a session consume the most CPU on the server. Peak supported load is 12/second. Sustainability depends on other loads on the server. Initiate a session typically means a sign-in for a user that has been signed out for an extended period of time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9f7a-236">Total Declined Inbound Voice Calls</span><span class="sxs-lookup"><span data-stu-id="e9f7a-236">Total Declined Inbound Voice Calls</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-237">拒否された着信音声通話の合計数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-237">The total number of inbound voice calls that were declined</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9f7a-238">Total Failed Inbound Voice Calls</span><span class="sxs-lookup"><span data-stu-id="e9f7a-238">Total Failed Inbound Voice Calls</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-239">失敗した着信音声通話の合計数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-239">The total number of inbound voice calls that failed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9f7a-240">Total Failed Outbound Voice Calls</span><span class="sxs-lookup"><span data-stu-id="e9f7a-240">Total Failed Outbound Voice Calls</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-241">失敗した発信音声通話の合計数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-241">The total number of outbound voice calls that failed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9f7a-242">Total number of sessions terminated by user</span><span class="sxs-lookup"><span data-stu-id="e9f7a-242">Total number of sessions terminated by user</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-243">ユーザーが終了したセッションの合計数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-243">The total number of sessions terminated by users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9f7a-244">Total Push Notification Requests</span><span class="sxs-lookup"><span data-stu-id="e9f7a-244">Total Push Notification Requests</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-245">プッシュ通知要求の合計数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-245">The total number of push notification requests</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9f7a-246">Total Push Notification Requests Failed</span><span class="sxs-lookup"><span data-stu-id="e9f7a-246">Total Push Notification Requests Failed</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-247">失敗したプッシュ通知要求の合計数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-247">The total number of push notification requests that failed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9f7a-248">Total Push Notification Requests Succeeded</span><span class="sxs-lookup"><span data-stu-id="e9f7a-248">Total Push Notification Requests Succeeded</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-249">成功したプッシュ通知要求の合計数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-249">The total number of push notification requests that were successful</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9f7a-250">Total Push Notification Requests Throttled</span><span class="sxs-lookup"><span data-stu-id="e9f7a-250">Total Push Notification Requests Throttled</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-251">調整済みのプッシュ通知要求の合計数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-251">The total number of push notification requests that were throttled</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9f7a-252">Total Requests Failed</span><span class="sxs-lookup"><span data-stu-id="e9f7a-252">Total Requests Failed</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-253">失敗した要求の合計数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-253">The total number of requests that failed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9f7a-254">Total Requests received on the Command Channel</span><span class="sxs-lookup"><span data-stu-id="e9f7a-254">Total Requests received on the Command Channel</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-255">コマンド チャネルで受信した要求の合計数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-255">The total number of requests received on the command channel</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9f7a-256">Total Requests Rejected</span><span class="sxs-lookup"><span data-stu-id="e9f7a-256">Total Requests Rejected</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-257">拒否された要求の合計数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-257">The total number of requests that were rejected</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9f7a-258">Total Requests Succeeded</span><span class="sxs-lookup"><span data-stu-id="e9f7a-258">Total Requests Succeeded</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-259">Mobility Service に対する成功した要求の合計数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-259">The total number of requests made to the Mobility Service that succeeded</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9f7a-260">Total Session Initiated Count</span><span class="sxs-lookup"><span data-stu-id="e9f7a-260">Total Session Initiated Count</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-261">Mobility Service が開始されてから起動されたセッションの合計数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-261">The total number of sessions that were initiated since the Mobility Service was started</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9f7a-262">Total Sessions Terminated Because of User Idle Timeout</span><span class="sxs-lookup"><span data-stu-id="e9f7a-262">Total Sessions Terminated Because of User Idle Timeout</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-263">ユーザーのアイドル タイムアウトが原因で終了したセッションの合計数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-263">The total number of sessions that were terminated because of user idle timeout</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9f7a-264">Total Successful Inbound Voice Calls</span><span class="sxs-lookup"><span data-stu-id="e9f7a-264">Total Successful Inbound Voice Calls</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-265">成功した着信音声通話の合計数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-265">The total number of inbound voice calls that were successful</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9f7a-266">Total Successful Outbound Voice Calls</span><span class="sxs-lookup"><span data-stu-id="e9f7a-266">Total Successful Outbound Voice Calls</span></span></p></td>
<td><p><span data-ttu-id="e9f7a-267">成功した発信音声通話の合計数</span><span class="sxs-lookup"><span data-stu-id="e9f7a-267">The total number of outbound voice calls that were successful</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="e9f7a-268">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e9f7a-268">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

