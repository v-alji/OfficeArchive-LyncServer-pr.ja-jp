---
title: 'Lync Server 2013: AudioStream テーブル'
description: 'Lync Server 2013: AudioStream テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AudioStream table
ms:assetid: 49ccbbc3-2f73-45fc-80a6-e612535cbc10
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425961(v=OCS.15)
ms:contentKeyID: 48184077
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8af2e622e14c54fa4f9a6313e1b0dae8f2483132
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438177"
---
# <a name="audiostream-table-in-lync-server-2013"></a><span data-ttu-id="fe00d-103">Lync Server 2013 の AudioStream テーブル</span><span class="sxs-lookup"><span data-stu-id="fe00d-103">AudioStream table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fe00d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fe00d-104">

<span> </span></span></span>

<span data-ttu-id="fe00d-105">_**最終更新日:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="fe00d-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="fe00d-106">各レコードは1つのオーディオストリームを表します。</span><span class="sxs-lookup"><span data-stu-id="fe00d-106">Each record represents one audio stream.</span></span> <span data-ttu-id="fe00d-107">通常、1つのオーディオメディアラインには2つのオーディオストリームが含まれています。</span><span class="sxs-lookup"><span data-stu-id="fe00d-107">One audio media line usually contains two audio streams.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fe00d-108"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="fe00d-109"><strong>データ型</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="fe00d-110"><strong>キー/インデックス</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="fe00d-111"><strong>詳細</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe00d-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-113">datetime</span><span class="sxs-lookup"><span data-stu-id="fe00d-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="fe00d-114">Primary</span><span class="sxs-lookup"><span data-stu-id="fe00d-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="fe00d-115"><a href="lync-server-2013-medialine-table.md">Lync Server 2013 の MediaLine テーブル</a>から参照されている。</span><span class="sxs-lookup"><span data-stu-id="fe00d-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe00d-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-117">int</span><span class="sxs-lookup"><span data-stu-id="fe00d-117">int</span></span></p></td>
<td><p><span data-ttu-id="fe00d-118">Primary</span><span class="sxs-lookup"><span data-stu-id="fe00d-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="fe00d-119"><a href="lync-server-2013-medialine-table.md">Lync Server 2013 の MediaLine テーブル</a>から参照されている。</span><span class="sxs-lookup"><span data-stu-id="fe00d-119">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe00d-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="fe00d-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="fe00d-122">Primary</span><span class="sxs-lookup"><span data-stu-id="fe00d-122">Primary</span></span></p></td>
<td><p><span data-ttu-id="fe00d-123"><a href="lync-server-2013-medialine-table.md">Lync Server 2013 の MediaLine テーブル</a>から参照されている。</span><span class="sxs-lookup"><span data-stu-id="fe00d-123">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe00d-124"><strong>StreamID</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-124"><strong>StreamID</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-125">int</span><span class="sxs-lookup"><span data-stu-id="fe00d-125">int</span></span></p></td>
<td><p><span data-ttu-id="fe00d-126">Primary</span><span class="sxs-lookup"><span data-stu-id="fe00d-126">Primary</span></span></p></td>
<td><p><span data-ttu-id="fe00d-127">メディアライン内の一意の ID。</span><span class="sxs-lookup"><span data-stu-id="fe00d-127">Unique ID within a media line.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe00d-128"><strong>JitterInterArrival</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-128"><strong>JitterInterArrival</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-129">int</span><span class="sxs-lookup"><span data-stu-id="fe00d-129">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="fe00d-130">リアルタイム制御プロトコル (RTCP) の統計情報からの平均ネットワークジッター。</span><span class="sxs-lookup"><span data-stu-id="fe00d-130">Average network jitter from Real Time Control Protocol (RTCP) statistics.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe00d-131"><strong>JitterInterArrivalMax</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-131"><strong>JitterInterArrivalMax</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-132">int</span><span class="sxs-lookup"><span data-stu-id="fe00d-132">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="fe00d-133">通話中の最大ネットワークジッター。</span><span class="sxs-lookup"><span data-stu-id="fe00d-133">Maximum network jitter during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe00d-134"><strong>PacketLossRate</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-134"><strong>PacketLossRate</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-135">10進数 (5, 4)</span><span class="sxs-lookup"><span data-stu-id="fe00d-135">decimal(5,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="fe00d-136">通話中の平均パケット損失率。</span><span class="sxs-lookup"><span data-stu-id="fe00d-136">Average packet loss rate during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe00d-137"><strong>PacketLossRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-137"><strong>PacketLossRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-138">10進数 (5, 4)</span><span class="sxs-lookup"><span data-stu-id="fe00d-138">decimal(5,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="fe00d-139">通話中に発生したパケット損失の上限。</span><span class="sxs-lookup"><span data-stu-id="fe00d-139">Maximum packet loss observed during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe00d-140"><strong>BurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-140"><strong>BurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-141">10進数 (9, 4)</span><span class="sxs-lookup"><span data-stu-id="fe00d-141">decimal(9,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="fe00d-142">通話中に損失が発生した場合のパケット損失の平均密度。</span><span class="sxs-lookup"><span data-stu-id="fe00d-142">Average density of packet Loss during bursts of losses during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe00d-143"><strong>BurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-143"><strong>BurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-144">int</span><span class="sxs-lookup"><span data-stu-id="fe00d-144">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="fe00d-145">通話中に損失が発生したときのパケット損失の平均時間。</span><span class="sxs-lookup"><span data-stu-id="fe00d-145">Average duration of packet loss during bursts of losses during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe00d-146"><strong>BurstGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-146"><strong>BurstGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-147">10進数 (9, 4)</span><span class="sxs-lookup"><span data-stu-id="fe00d-147">decimal(9,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="fe00d-148">パケット損失のバースト間のパケット損失の平均密度。</span><span class="sxs-lookup"><span data-stu-id="fe00d-148">Average density of packet loss during gaps between bursts of packet loss.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe00d-149"><strong>BurstGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-149"><strong>BurstGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-150">int</span><span class="sxs-lookup"><span data-stu-id="fe00d-150">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="fe00d-151">パケット損失のバーストの間の平均時間差。</span><span class="sxs-lookup"><span data-stu-id="fe00d-151">Average duration of gaps between bursts of packet loss.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe00d-152"><strong>PacketUtilization</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-152"><strong>PacketUtilization</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-153">Int</span><span class="sxs-lookup"><span data-stu-id="fe00d-153">Int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="fe00d-154">オーディオストリームのパケット数。</span><span class="sxs-lookup"><span data-stu-id="fe00d-154">Packet count for the audio stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe00d-155"><strong>BandwidthEst</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-155"><strong>BandwidthEst</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-156">Int</span><span class="sxs-lookup"><span data-stu-id="fe00d-156">Int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="fe00d-157">オーディオストリームの帯域幅の推定。</span><span class="sxs-lookup"><span data-stu-id="fe00d-157">Bandwidth estimates for the audio stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe00d-158"><strong>DegradationAvg</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-158"><strong>DegradationAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-159">10進数 (3, 2)</span><span class="sxs-lookup"><span data-stu-id="fe00d-159">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="fe00d-160">電話全体のネットワーク MOS が低下します。</span><span class="sxs-lookup"><span data-stu-id="fe00d-160">Network MOS Degradation for the whole call.</span></span> <span data-ttu-id="fe00d-161">範囲は 0.0 ~ 5.0 です。</span><span class="sxs-lookup"><span data-stu-id="fe00d-161">Range is 0.0 to 5.0.</span></span> <span data-ttu-id="fe00d-162">このメトリックは、ジッタとパケット損失によってネットワーク MOS が削減された量を示します。</span><span class="sxs-lookup"><span data-stu-id="fe00d-162">This metric shows the amount the Network MOS was reduced because of jitter and packet loss.</span></span> <span data-ttu-id="fe00d-163">許容可能な品質には、0.5 未満の値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fe00d-163">For acceptable quality it should less than 0.5.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe00d-164"><strong>DegradationMax</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-164"><strong>DegradationMax</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-165">10進数 (3, 2)</span><span class="sxs-lookup"><span data-stu-id="fe00d-165">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="fe00d-166">通話中の最大ネットワーク MOS の品質低下。</span><span class="sxs-lookup"><span data-stu-id="fe00d-166">Maximum Network MOS degradation during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe00d-167"><strong>DegradationJitterAvg</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-167"><strong>DegradationJitterAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-168">10進数 (3, 2)</span><span class="sxs-lookup"><span data-stu-id="fe00d-168">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="fe00d-169">ジッターによるネットワーク MOS の低下。</span><span class="sxs-lookup"><span data-stu-id="fe00d-169">Network MOS degradation caused by jitter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe00d-170"><strong>DegradationPacketLossAvg</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-170"><strong>DegradationPacketLossAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-171">10進数 (3, 2)</span><span class="sxs-lookup"><span data-stu-id="fe00d-171">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="fe00d-172">パケット損失によるネットワーク MOS の低下。</span><span class="sxs-lookup"><span data-stu-id="fe00d-172">Network MOS degradation caused by packet loss.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe00d-173"><strong>AudioPayloadDescription</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-173"><strong>AudioPayloadDescription</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-174">int</span><span class="sxs-lookup"><span data-stu-id="fe00d-174">int</span></span></p></td>
<td><p><span data-ttu-id="fe00d-175">外部</span><span class="sxs-lookup"><span data-stu-id="fe00d-175">Foreign</span></span></p></td>
<td><p><span data-ttu-id="fe00d-176">PayloadDescription テーブルから参照される、通話に使われるオーディオコーデック。</span><span class="sxs-lookup"><span data-stu-id="fe00d-176">The audio Codec used for the call, referenced from PayloadDescription Table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe00d-177"><strong>AudioSampleRate</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-177"><strong>AudioSampleRate</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-178">int</span><span class="sxs-lookup"><span data-stu-id="fe00d-178">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="fe00d-179">オーディオストリームのサンプリングレート。</span><span class="sxs-lookup"><span data-stu-id="fe00d-179">Sampling rate for the audio stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe00d-180"><strong>RoundTrip</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-180"><strong>RoundTrip</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-181">int</span><span class="sxs-lookup"><span data-stu-id="fe00d-181">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="fe00d-182">RTCP の統計情報からのラウンドトリップ時間。</span><span class="sxs-lookup"><span data-stu-id="fe00d-182">Round trip time from RTCP statistics.</span></span> <span data-ttu-id="fe00d-183">許容可能な品質の場合は、100ms 未満にしてください。</span><span class="sxs-lookup"><span data-stu-id="fe00d-183">For acceptable quality this should be less than 100ms.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe00d-184"><strong>RoundTripMax</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-184"><strong>RoundTripMax</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-185">int</span><span class="sxs-lookup"><span data-stu-id="fe00d-185">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="fe00d-186">オーディオストリームの最大ラウンドトリップ時間。</span><span class="sxs-lookup"><span data-stu-id="fe00d-186">Maximum round trip time for the audio stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe00d-187"><strong>OverallAvgNetworkMOS</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-187"><strong>OverallAvgNetworkMOS</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-188">10進数 (3, 2)</span><span class="sxs-lookup"><span data-stu-id="fe00d-188">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="fe00d-189">通話の平均広帯域ネットワーク MOS。</span><span class="sxs-lookup"><span data-stu-id="fe00d-189">Average wideband Network MOS for the call.</span></span> <span data-ttu-id="fe00d-190">このメトリックは、使用されているパケット損失、ジッタ、およびコーデックによって異なります。</span><span class="sxs-lookup"><span data-stu-id="fe00d-190">This metric depends on the packet loss, jitter, and codec used.</span></span> <span data-ttu-id="fe00d-191">範囲は [1.0 から 5.0] になります。</span><span class="sxs-lookup"><span data-stu-id="fe00d-191">Range is [1.0 to 5.0].</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe00d-192"><strong>OverallMinNetworkMOS</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-192"><strong>OverallMinNetworkMOS</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-193">10進数 (3, 2)</span><span class="sxs-lookup"><span data-stu-id="fe00d-193">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="fe00d-194">通話の最小広帯域ネットワーク MOS。</span><span class="sxs-lookup"><span data-stu-id="fe00d-194">The minimum wideband Network MOS for the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe00d-195"><strong>SendListenMOS</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-195"><strong>SendListenMOS</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-196">10進数 (3, 2)</span><span class="sxs-lookup"><span data-stu-id="fe00d-196">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="fe00d-197">送信された音声の平均予測広帯域 MOS score (音声レベル、ノイズレベル、キャプチャデバイスの特性を含む)。</span><span class="sxs-lookup"><span data-stu-id="fe00d-197">The average predicted wideband Listening MOS score for audio sent, including speech level, noise level and capture device characteristics.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe00d-198"><strong>SendListenMOSMin</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-198"><strong>SendListenMOSMin</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-199">10進数 (3, 2)</span><span class="sxs-lookup"><span data-stu-id="fe00d-199">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="fe00d-200">通話の最小 SendListenMOS。</span><span class="sxs-lookup"><span data-stu-id="fe00d-200">The minimum SendListenMOS for the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe00d-201"><strong>RecvListenMOS</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-201"><strong>RecvListenMOS</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-202">10進数 (3, 2)</span><span class="sxs-lookup"><span data-stu-id="fe00d-202">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="fe00d-203">予測される平均広帯域は、ネットワークから受信した音声の MOS スコア (音声レベル、ノイズレベル、コーデック、ネットワーク条件、キャプチャデバイスの特性など) を対象としています。</span><span class="sxs-lookup"><span data-stu-id="fe00d-203">The average predicted wideband Listening MOS score for audio received from the network including speech level, noise level, codec, network conditions and capture device characteristics.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe00d-204"><strong>RecvListenMOSMin</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-204"><strong>RecvListenMOSMin</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-205">10進数 (3, 2)</span><span class="sxs-lookup"><span data-stu-id="fe00d-205">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="fe00d-206">通話の最小 RecvListenMOS。</span><span class="sxs-lookup"><span data-stu-id="fe00d-206">The minimum RecvListenMOS for the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe00d-207"><strong>AudioFECUsed</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-207"><strong>AudioFECUsed</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-208">bit</span><span class="sxs-lookup"><span data-stu-id="fe00d-208">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fe00d-209">通話にオーディオ FEC が使用されたかどうかを示すフラグ。</span><span class="sxs-lookup"><span data-stu-id="fe00d-209">Flag indicating if audio FEC was used for the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe00d-210"><strong>RatioConcealedSamplesAvg</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-210"><strong>RatioConcealedSamplesAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-211">10進数 (5, 2)</span><span class="sxs-lookup"><span data-stu-id="fe00d-211">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fe00d-212">オーディオの修復によって発生した、一般的なサンプルの平均比率。</span><span class="sxs-lookup"><span data-stu-id="fe00d-212">Average ratio of concealed samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe00d-213"><strong>RatioStretchedSamplesAvg</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-213"><strong>RatioStretchedSamplesAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-214">10進数 (5, 2)</span><span class="sxs-lookup"><span data-stu-id="fe00d-214">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fe00d-215">オーディオ修復によって生成された、一般的なサンプルの平均比率。</span><span class="sxs-lookup"><span data-stu-id="fe00d-215">Average ratio of stretched samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe00d-216"><strong>RatioCompressedSamplesAvg</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-216"><strong>RatioCompressedSamplesAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-217">10進数 (5, 2)</span><span class="sxs-lookup"><span data-stu-id="fe00d-217">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fe00d-218">オーディオの修復によって生成された、一般的なサンプルの圧縮サンプルの平均比率。</span><span class="sxs-lookup"><span data-stu-id="fe00d-218">Average ratio of compressed samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe00d-219"><strong>トラフィック</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-219"><strong>Inbound</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-220">bit</span><span class="sxs-lookup"><span data-stu-id="fe00d-220">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="fe00d-221">受信側のストリームデータが受信されます。</span><span class="sxs-lookup"><span data-stu-id="fe00d-221">Stream data on receiver side is received.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe00d-222"><strong>発信</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-222"><strong>Outbound</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-223">bit</span><span class="sxs-lookup"><span data-stu-id="fe00d-223">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="fe00d-224">送信側のストリームデータが受信されます。</span><span class="sxs-lookup"><span data-stu-id="fe00d-224">Stream data on sender side is received.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe00d-225"><strong>SenderIsCallerPAI</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-225"><strong>SenderIsCallerPAI</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-226">bit</span><span class="sxs-lookup"><span data-stu-id="fe00d-226">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="fe00d-227">1は、ストリームの方向を呼び出し元から呼び出し先に転送することを意味します。</span><span class="sxs-lookup"><span data-stu-id="fe00d-227">1 means the stream direction is from the caller to the callee.</span></span></p>
<p><span data-ttu-id="fe00d-228">0は、ストリームの方向を呼び出し元から呼び出し元に転送します。</span><span class="sxs-lookup"><span data-stu-id="fe00d-228">0 means the stream direction is from the callee to the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe00d-229"><strong>JitterInterArrivalSD</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-229"><strong>JitterInterArrivalSD</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-230">float</span><span class="sxs-lookup"><span data-stu-id="fe00d-230">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fe00d-231">ジッタの到着時刻の標準偏差。</span><span class="sxs-lookup"><span data-stu-id="fe00d-231">Standard deviation for jitter arrival times.</span></span></p>
<p><span data-ttu-id="fe00d-232">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="fe00d-232">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe00d-233"><strong>ConcealRatioMax</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-233"><strong>ConcealRatioMax</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-234">float</span><span class="sxs-lookup"><span data-stu-id="fe00d-234">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fe00d-235">Healer によって隠されているパケットの最大比率。</span><span class="sxs-lookup"><span data-stu-id="fe00d-235">Maximum ratio of packets concealed by the healer.</span></span></p>
<p><span data-ttu-id="fe00d-236">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="fe00d-236">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe00d-237"><strong>ConcealRatioSD</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-237"><strong>ConcealRatioSD</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-238">float</span><span class="sxs-lookup"><span data-stu-id="fe00d-238">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fe00d-239">Healer によって隠されているパケットの比率の標準偏差。</span><span class="sxs-lookup"><span data-stu-id="fe00d-239">Standard deviation for the ratio of packets concealed by the healer.</span></span></p>
<p><span data-ttu-id="fe00d-240">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="fe00d-240">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe00d-241"><strong>HealerPacketDropRatio</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-241"><strong>HealerPacketDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-242">float</span><span class="sxs-lookup"><span data-stu-id="fe00d-242">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fe00d-243">受信したパケットの合計数と比較して、healer によってドロップされたパケットの比率。</span><span class="sxs-lookup"><span data-stu-id="fe00d-243">Ratio of packets dropped by the healer compared to the total number of packets received.</span></span></p>
<p><span data-ttu-id="fe00d-244">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="fe00d-244">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe00d-245"><strong>HealerFECPacketUsedRatio</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-245"><strong>HealerFECPacketUsedRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-246">float</span><span class="sxs-lookup"><span data-stu-id="fe00d-246">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fe00d-247">受信したパケットの合計数と比較した、使用された転送エラー修正パケットの比率。</span><span class="sxs-lookup"><span data-stu-id="fe00d-247">Ratio of used forward error correction packets compared to the total number of packets received.</span></span></p>
<p><span data-ttu-id="fe00d-248">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="fe00d-248">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe00d-249"><strong>MaxCompressedSamples</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-249"><strong>MaxCompressedSamples</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-250">float</span><span class="sxs-lookup"><span data-stu-id="fe00d-250">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fe00d-251">Healer によって圧縮されたオーディオパケットの最大数。</span><span class="sxs-lookup"><span data-stu-id="fe00d-251">Maximum number of audio packets that were compressed by the healer.</span></span></p>
<p><span data-ttu-id="fe00d-252">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="fe00d-252">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe00d-253"><strong>LossCongestionPercent</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-253"><strong>LossCongestionPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-254">float</span><span class="sxs-lookup"><span data-stu-id="fe00d-254">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fe00d-255">通話が切断された輻輳状態であった時間の割合を示します。</span><span class="sxs-lookup"><span data-stu-id="fe00d-255">Indicates the percentage of the time when the call was in a loss congestion state.</span></span></p>
<p><span data-ttu-id="fe00d-256">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="fe00d-256">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe00d-257"><strong>DelayCongestionPercent</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-257"><strong>DelayCongestionPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-258">float</span><span class="sxs-lookup"><span data-stu-id="fe00d-258">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fe00d-259">ネットワークパケットが遅延したために発生した、通話の割合を示します。</span><span class="sxs-lookup"><span data-stu-id="fe00d-259">Indicates the percentage of the call during which congestion was caused by the delayed arrival of network packets.</span></span></p>
<p><span data-ttu-id="fe00d-260">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="fe00d-260">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe00d-261"><strong>ContentionDetectedPercent</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-261"><strong>ContentionDetectedPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-262">float</span><span class="sxs-lookup"><span data-stu-id="fe00d-262">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fe00d-263">通話がネットワークリソースに対して競合した時間の割合を示します。</span><span class="sxs-lookup"><span data-stu-id="fe00d-263">Indicates the percentage of the time when the call was competing for network resources.</span></span></p>
<p><span data-ttu-id="fe00d-264">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="fe00d-264">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe00d-265"><strong>BandwidthEstMin</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-265"><strong>BandwidthEstMin</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-266">int</span><span class="sxs-lookup"><span data-stu-id="fe00d-266">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fe00d-267">通話中の最小帯域幅推定値。</span><span class="sxs-lookup"><span data-stu-id="fe00d-267">Minimum amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="fe00d-268">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="fe00d-268">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe00d-269"><strong>BandwidthEstMax</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-269"><strong>BandwidthEstMax</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-270">int</span><span class="sxs-lookup"><span data-stu-id="fe00d-270">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fe00d-271">通話中に測定された帯域幅推定の最大量。</span><span class="sxs-lookup"><span data-stu-id="fe00d-271">Maximum amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="fe00d-272">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="fe00d-272">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe00d-273"><strong>BandwidthEstStdDev</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-273"><strong>BandwidthEstStdDev</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-274">int</span><span class="sxs-lookup"><span data-stu-id="fe00d-274">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fe00d-275">通話中に測定された帯域幅推定の標準偏差。</span><span class="sxs-lookup"><span data-stu-id="fe00d-275">Standard deviation of the bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="fe00d-276">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="fe00d-276">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe00d-277"><strong>BandwidthEstAvge</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-277"><strong>BandwidthEstAvge</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-278">int</span><span class="sxs-lookup"><span data-stu-id="fe00d-278">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fe00d-279">通話中に計測された平均帯域幅推定量。</span><span class="sxs-lookup"><span data-stu-id="fe00d-279">Average amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="fe00d-280">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="fe00d-280">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe00d-281"><strong>RelativeOneWayTotal</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-281"><strong>RelativeOneWayTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-282">float</span><span class="sxs-lookup"><span data-stu-id="fe00d-282">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fe00d-283">一方向の待機時間の合計。</span><span class="sxs-lookup"><span data-stu-id="fe00d-283">Total amount of one-way latency.</span></span> <span data-ttu-id="fe00d-284">相対的な一方向の待ち時間は、クライアントとサーバーの間の遅延を測定します。</span><span class="sxs-lookup"><span data-stu-id="fe00d-284">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="fe00d-285">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="fe00d-285">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe00d-286"><strong>RelativeOneWayAverage</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-286"><strong>RelativeOneWayAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-287">float</span><span class="sxs-lookup"><span data-stu-id="fe00d-287">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fe00d-288">一方向の待ち時間の平均値。</span><span class="sxs-lookup"><span data-stu-id="fe00d-288">Average amount of one-way latency.</span></span> <span data-ttu-id="fe00d-289">相対的な一方向の待ち時間は、クライアントとサーバーの間の遅延を測定します。</span><span class="sxs-lookup"><span data-stu-id="fe00d-289">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="fe00d-290">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="fe00d-290">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe00d-291"><strong>RelativeOneWayMax</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-291"><strong>RelativeOneWayMax</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-292">float</span><span class="sxs-lookup"><span data-stu-id="fe00d-292">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fe00d-293">一方向の待機時間の上限。</span><span class="sxs-lookup"><span data-stu-id="fe00d-293">Maximum amount of one-way latency.</span></span> <span data-ttu-id="fe00d-294">相対的な一方向の待ち時間は、クライアントとサーバーの間の遅延を測定します。</span><span class="sxs-lookup"><span data-stu-id="fe00d-294">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="fe00d-295">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="fe00d-295">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe00d-296"><strong>RelativeOneWayBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-296"><strong>RelativeOneWayBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-297">int</span><span class="sxs-lookup"><span data-stu-id="fe00d-297">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fe00d-298">1方向のバースト発生の合計。</span><span class="sxs-lookup"><span data-stu-id="fe00d-298">Total one-way burst occurrences.</span></span> <span data-ttu-id="fe00d-299">"Bursty" 伝送とは、安定したストリームと比べて予期しないバーストでデータが流れる伝送です。</span><span class="sxs-lookup"><span data-stu-id="fe00d-299">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="fe00d-300">このメトリックは、クライアントとサーバー間のデータフローを計測します。</span><span class="sxs-lookup"><span data-stu-id="fe00d-300">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="fe00d-301">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="fe00d-301">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe00d-302"><strong>RelativeOneWayBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-302"><strong>RelativeOneWayBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-303">float</span><span class="sxs-lookup"><span data-stu-id="fe00d-303">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fe00d-304">全体的な1方向バースト密度。</span><span class="sxs-lookup"><span data-stu-id="fe00d-304">Total one-way burst density.</span></span> <span data-ttu-id="fe00d-305">"Bursty" 伝送とは、安定したストリームと比べて予期しないバーストでデータが流れる伝送です。</span><span class="sxs-lookup"><span data-stu-id="fe00d-305">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="fe00d-306">このメトリックは、クライアントとサーバー間のデータフローを計測します。</span><span class="sxs-lookup"><span data-stu-id="fe00d-306">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="fe00d-307">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="fe00d-307">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe00d-308"><strong>RelativeOneWayBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-308"><strong>RelativeOneWayBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-309">float</span><span class="sxs-lookup"><span data-stu-id="fe00d-309">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fe00d-310">一方向のバースト期間の合計。</span><span class="sxs-lookup"><span data-stu-id="fe00d-310">Total one-way burst duration.</span></span> <span data-ttu-id="fe00d-311">"Bursty" 伝送とは、安定したストリームと比べて予期しないバーストでデータが流れる伝送です。</span><span class="sxs-lookup"><span data-stu-id="fe00d-311">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="fe00d-312">このメトリックは、クライアントとサーバー間のデータフローを計測します。</span><span class="sxs-lookup"><span data-stu-id="fe00d-312">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="fe00d-313">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="fe00d-313">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe00d-314"><strong>RelativeOneWayGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-314"><strong>RelativeOneWayGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-315">int</span><span class="sxs-lookup"><span data-stu-id="fe00d-315">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fe00d-316">一方向のギャップ出現の合計。</span><span class="sxs-lookup"><span data-stu-id="fe00d-316">Total one-way gap occurrences.</span></span> <span data-ttu-id="fe00d-317">"Bursty" 伝送とは、安定したストリームではなく、予期しないバーストでデータが流れる伝送です。ギャップは、このようなバーストの間の遅延を示します。</span><span class="sxs-lookup"><span data-stu-id="fe00d-317">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="fe00d-318">このメトリックは、クライアントとサーバー間のデータフローを計測します。</span><span class="sxs-lookup"><span data-stu-id="fe00d-318">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="fe00d-319">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="fe00d-319">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe00d-320"><strong>RelativeOneWayGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-320"><strong>RelativeOneWayGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-321">float</span><span class="sxs-lookup"><span data-stu-id="fe00d-321">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fe00d-322">一方向のギャップの密度の合計。</span><span class="sxs-lookup"><span data-stu-id="fe00d-322">Total one-way gap density.</span></span> <span data-ttu-id="fe00d-323">"Bursty" 伝送とは、安定したストリームではなく、予期しないバーストでデータが流れる伝送です。ギャップは、このようなバーストの間の遅延を示します。</span><span class="sxs-lookup"><span data-stu-id="fe00d-323">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="fe00d-324">このメトリックは、クライアントとサーバー間のデータフローを計測します。</span><span class="sxs-lookup"><span data-stu-id="fe00d-324">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="fe00d-325">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="fe00d-325">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe00d-326"><strong>RelativeOneWayGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-326"><strong>RelativeOneWayGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-327">float</span><span class="sxs-lookup"><span data-stu-id="fe00d-327">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fe00d-328">一方向のギャップ期間の合計。</span><span class="sxs-lookup"><span data-stu-id="fe00d-328">Total one-way gap duration.</span></span> <span data-ttu-id="fe00d-329">"Bursty" 伝送とは、安定したストリームではなく、予期しないバーストでデータが流れる伝送です。ギャップは、このようなバーストの間の遅延を示します。</span><span class="sxs-lookup"><span data-stu-id="fe00d-329">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="fe00d-330">このメトリックは、クライアントとサーバー間のデータフローを計測します。</span><span class="sxs-lookup"><span data-stu-id="fe00d-330">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="fe00d-331">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="fe00d-331">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe00d-332"><strong>DecodeStereoPercent</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-332"><strong>DecodeStereoPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-333">float</span><span class="sxs-lookup"><span data-stu-id="fe00d-333">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fe00d-334">ステレオとしてデコードされた通話のパーセンテージ。</span><span class="sxs-lookup"><span data-stu-id="fe00d-334">Percentage of the call decoded as stereo.</span></span></p>
<p><span data-ttu-id="fe00d-335">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="fe00d-335">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe00d-336"><strong>AecRenderStereoPercent</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-336"><strong>AecRenderStereoPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-337">float</span><span class="sxs-lookup"><span data-stu-id="fe00d-337">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fe00d-338">アコースティックエコーキャンセラによってステレオとしてレンダリングされた通話の割合。</span><span class="sxs-lookup"><span data-stu-id="fe00d-338">Percentage of the call rendered as stereo by the acoustic echo canceller.</span></span></p>
<p><span data-ttu-id="fe00d-339">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="fe00d-339">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe00d-340"><strong>AudioPostFECPLR</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-340"><strong>AudioPostFECPLR</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-341">float</span><span class="sxs-lookup"><span data-stu-id="fe00d-341">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fe00d-342">転送後のエラー訂正が適用された後のパケット損失率。</span><span class="sxs-lookup"><span data-stu-id="fe00d-342">Packet loss rate after forward error correction has been applied.</span></span></p>
<p><span data-ttu-id="fe00d-343">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="fe00d-343">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe00d-344"><strong>EncodeStereoPercent</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-344"><strong>EncodeStereoPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-345">float</span><span class="sxs-lookup"><span data-stu-id="fe00d-345">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fe00d-346">ステレオとしてエンコードされた通話の割合。</span><span class="sxs-lookup"><span data-stu-id="fe00d-346">Percentage of the call encoded as stereo.</span></span></p>
<p><span data-ttu-id="fe00d-347">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="fe00d-347">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe00d-348"><strong>AecCaptureStereoPercent</strong></span><span class="sxs-lookup"><span data-stu-id="fe00d-348"><strong>AecCaptureStereoPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="fe00d-349">float</span><span class="sxs-lookup"><span data-stu-id="fe00d-349">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fe00d-350">アコースティックエコーキャンセラでステレオとしてキャプチャされた通話のパーセンテージ。</span><span class="sxs-lookup"><span data-stu-id="fe00d-350">Percentage of the call captured as stereo by the acoustic echo canceller.</span></span></p>
<p><span data-ttu-id="fe00d-351">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="fe00d-351">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="fe00d-352">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fe00d-352">


</div>

<span> </span>

</div>

</div>

</span></span></div>

