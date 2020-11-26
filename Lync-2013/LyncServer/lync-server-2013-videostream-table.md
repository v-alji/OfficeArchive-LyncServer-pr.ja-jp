---
title: 'Lync Server 2013: VideoStream テーブル'
description: 'Lync Server 2013: VideoStream テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VideoStream table
ms:assetid: 4275ede7-5467-4a97-b8c8-a4b00917bf32
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425928(v=OCS.15)
ms:contentKeyID: 48184014
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0d741478e1f6290685181bff471f143e41ce9ca1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444127"
---
# <a name="videostream-table-in-lync-server-2013"></a><span data-ttu-id="ee530-103">Lync Server 2013 の VideoStream テーブル</span><span class="sxs-lookup"><span data-stu-id="ee530-103">VideoStream table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ee530-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ee530-104">

<span> </span></span></span>

<span data-ttu-id="ee530-105">_**最終更新日:** 2013-12-13_</span><span class="sxs-lookup"><span data-stu-id="ee530-105">_**Topic Last Modified:** 2013-12-13_</span></span>

<span data-ttu-id="ee530-106">各レコードは1つのビデオストリームを表します。</span><span class="sxs-lookup"><span data-stu-id="ee530-106">Each record represents one video stream.</span></span> <span data-ttu-id="ee530-107">1つのビデオメディアラインには通常、2つのビデオストリームが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ee530-107">One video media line usually contains two video streams.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ee530-108"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="ee530-109"><strong>データ型</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="ee530-110"><strong>キー/インデックス</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="ee530-111"><strong>詳細</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee530-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-113">datetime</span><span class="sxs-lookup"><span data-stu-id="ee530-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="ee530-114">Primary</span><span class="sxs-lookup"><span data-stu-id="ee530-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="ee530-115"><a href="lync-server-2013-medialine-table.md">Lync Server 2013 の MediaLine テーブル</a>から参照されている。</span><span class="sxs-lookup"><span data-stu-id="ee530-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee530-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-117">int</span><span class="sxs-lookup"><span data-stu-id="ee530-117">int</span></span></p></td>
<td><p><span data-ttu-id="ee530-118">Primary</span><span class="sxs-lookup"><span data-stu-id="ee530-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="ee530-119">MediaLine は、 <a href="lync-server-2013-medialine-table.md">Lync Server 2013 のテーブル</a>から参照されます。</span><span class="sxs-lookup"><span data-stu-id="ee530-119">R Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee530-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="ee530-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="ee530-122">Primary</span><span class="sxs-lookup"><span data-stu-id="ee530-122">Primary</span></span></p></td>
<td><p><span data-ttu-id="ee530-123"><a href="lync-server-2013-medialine-table.md">Lync Server 2013 の MediaLine テーブル</a>から参照されている。</span><span class="sxs-lookup"><span data-stu-id="ee530-123">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee530-124"><strong>StreamID</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-124"><strong>StreamID</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-125">int</span><span class="sxs-lookup"><span data-stu-id="ee530-125">int</span></span></p></td>
<td><p><span data-ttu-id="ee530-126">Primary</span><span class="sxs-lookup"><span data-stu-id="ee530-126">Primary</span></span></p></td>
<td><p><span data-ttu-id="ee530-127">メディアライン内の一意の ID。</span><span class="sxs-lookup"><span data-stu-id="ee530-127">Unique ID within a media line.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee530-128"><strong>VideoPayloadDescription</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-128"><strong>VideoPayloadDescription</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-129">smallint</span><span class="sxs-lookup"><span data-stu-id="ee530-129">smallint</span></span></p></td>
<td><p><span data-ttu-id="ee530-130">外来、プライマリ</span><span class="sxs-lookup"><span data-stu-id="ee530-130">Foreign, Primary</span></span></p></td>
<td><p><span data-ttu-id="ee530-131">ペイロードの説明。</span><span class="sxs-lookup"><span data-stu-id="ee530-131">Payload description.</span></span> <span data-ttu-id="ee530-132">詳細については、「 <a href="lync-server-2013-payloaddescription-table.md">Lync Server 2013 の PayloadDescription テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee530-132">See the <a href="lync-server-2013-payloaddescription-table.md">PayloadDescription table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee530-133"><strong>JitterInterArrival</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-133"><strong>JitterInterArrival</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-134">int</span><span class="sxs-lookup"><span data-stu-id="ee530-134">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ee530-135">リアルタイム制御プロトコル (RTCP) の統計情報からの平均ネットワークジッター。</span><span class="sxs-lookup"><span data-stu-id="ee530-135">Average network jitter from Real Time Control Protocol (RTCP) statistics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee530-136"><strong>JitterInterArrivalMax</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-136"><strong>JitterInterArrivalMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-137">int</span><span class="sxs-lookup"><span data-stu-id="ee530-137">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ee530-138">ビデオセッション中の最大ネットワークジッター。</span><span class="sxs-lookup"><span data-stu-id="ee530-138">Maximum network jitter during the video session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee530-139"><strong>RoundTrip</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-139"><strong>RoundTrip</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-140">int</span><span class="sxs-lookup"><span data-stu-id="ee530-140">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ee530-141">RTCP の統計情報からのラウンドトリップ時間。</span><span class="sxs-lookup"><span data-stu-id="ee530-141">Round trip time from RTCP statistics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee530-142"><strong>RoundTripMax</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-142"><strong>RoundTripMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-143">int</span><span class="sxs-lookup"><span data-stu-id="ee530-143">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ee530-144">ビデオストリームの最大ラウンドトリップ時間。</span><span class="sxs-lookup"><span data-stu-id="ee530-144">Maximum round trip time for the video stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee530-145"><strong>PacketLossRate</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-145"><strong>PacketLossRate</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-146">10進数 (5, 4)</span><span class="sxs-lookup"><span data-stu-id="ee530-146">decimal(5,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ee530-147">通話中の平均パケット損失率。</span><span class="sxs-lookup"><span data-stu-id="ee530-147">Average packet loss rate during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee530-148"><strong>PacketLossRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-148"><strong>PacketLossRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-149">10進数 (5, 4)</span><span class="sxs-lookup"><span data-stu-id="ee530-149">decimal(5,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ee530-150">通話中に発生したパケット損失の上限。</span><span class="sxs-lookup"><span data-stu-id="ee530-150">Maximum packet loss observed during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee530-151"><strong>PacketUtilization</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-151"><strong>PacketUtilization</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-152">int</span><span class="sxs-lookup"><span data-stu-id="ee530-152">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ee530-153">ビデオストリームのパケット数 (リアルタイムトランスポートプロトコル、RTP)。</span><span class="sxs-lookup"><span data-stu-id="ee530-153">Packet count for the video stream (Real Time Transport Protocol, RTP).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee530-154"><strong>BandwidthEst</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-154"><strong>BandwidthEst</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-155">int</span><span class="sxs-lookup"><span data-stu-id="ee530-155">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ee530-156">ビデオストリームの帯域幅推定。</span><span class="sxs-lookup"><span data-stu-id="ee530-156">Bandwidth estimates for the video stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee530-157"><strong>VideoResolution</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-157"><strong>VideoResolution</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-158">char (9)</span><span class="sxs-lookup"><span data-stu-id="ee530-158">char(9)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ee530-159">ピクセル幅にピクセルの高さを掛けたビデオの解像度。</span><span class="sxs-lookup"><span data-stu-id="ee530-159">Resolution of the video in pixels width multiplied by pixels height.</span></span> <span data-ttu-id="ee530-160">文字列として報告されます。</span><span class="sxs-lookup"><span data-stu-id="ee530-160">Reported as a string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee530-161"><strong>VideoBitRateAvg</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-161"><strong>VideoBitRateAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-162">int</span><span class="sxs-lookup"><span data-stu-id="ee530-162">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ee530-163">ビデオストリームの平均ビットレート。</span><span class="sxs-lookup"><span data-stu-id="ee530-163">Average bit rate of the video stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee530-164"><strong>InboundVideoFrameRateAvg</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-164"><strong>InboundVideoFrameRateAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-165">10進数 (9, 4)</span><span class="sxs-lookup"><span data-stu-id="ee530-165">decimal(9,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ee530-166">ビデオフレームレートが適用されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-166">The video frame rate received.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee530-167"><strong>OutboundVideoFrameRateAvg</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-167"><strong>OutboundVideoFrameRateAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-168">10進数 (9, 4)</span><span class="sxs-lookup"><span data-stu-id="ee530-168">decimal(9,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ee530-169">送信されたビデオフレームレート。</span><span class="sxs-lookup"><span data-stu-id="ee530-169">The video frame rate sent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee530-170"><strong>VideoBitRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-170"><strong>VideoBitRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-171">int</span><span class="sxs-lookup"><span data-stu-id="ee530-171">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ee530-172">ビデオセッション中の最大ビデオビットレート。</span><span class="sxs-lookup"><span data-stu-id="ee530-172">The maximum video bit rate during the video session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee530-173"><strong>VideoFrameLossRate</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-173"><strong>VideoFrameLossRate</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-174">10進数 (9, 4)</span><span class="sxs-lookup"><span data-stu-id="ee530-174">decimal(9,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ee530-175">失われたビデオフレームの合計のパーセンテージ。</span><span class="sxs-lookup"><span data-stu-id="ee530-175">The percentage of total video frames that are lost.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee530-176"><strong>VideoFEC</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-176"><strong>VideoFEC</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-177">bit</span><span class="sxs-lookup"><span data-stu-id="ee530-177">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ee530-178">使用できません。</span><span class="sxs-lookup"><span data-stu-id="ee530-178">Not available.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee530-179"><strong>ビデオ</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-179"><strong>VideoLocalFrameLossPercentageAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-180">10進数 (9, 4)</span><span class="sxs-lookup"><span data-stu-id="ee530-180">decimal(9,4)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-181">失われたビデオフレームの合計のパーセンテージ。</span><span class="sxs-lookup"><span data-stu-id="ee530-181">The percentage of total video frames that are lost.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee530-182"><strong>CIFQualityRatio</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-182"><strong>CIFQualityRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-183">tinyint</span><span class="sxs-lookup"><span data-stu-id="ee530-183">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-184">共通インターチェンジ形式 (CIF) の解像度での通話の割合。</span><span class="sxs-lookup"><span data-stu-id="ee530-184">The percentage of the call that was at the Common Interchange Format (CIF) resolution.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee530-185"><strong>VGAQualityRatio</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-185"><strong>VGAQualityRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-186">tinyint</span><span class="sxs-lookup"><span data-stu-id="ee530-186">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-187">VGA 解像度での通話の割合。</span><span class="sxs-lookup"><span data-stu-id="ee530-187">The percentage of the call that was at VGA resolution.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee530-188"><strong>HD720QualityRatio</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-188"><strong>HD720QualityRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-189">tinyint</span><span class="sxs-lookup"><span data-stu-id="ee530-189">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-190">HD720 の解像度での通話の割合。</span><span class="sxs-lookup"><span data-stu-id="ee530-190">The percentage of the call that was at HD720 resolution.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee530-191"><strong>NoneDropRatio</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-191"><strong>NoneDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-192">tinyint</span><span class="sxs-lookup"><span data-stu-id="ee530-192">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-193">フレームドロップなしの通話時間の割合。</span><span class="sxs-lookup"><span data-stu-id="ee530-193">Percentage of call duration with no frame drop.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee530-194"><strong>Bスペック</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-194"><strong>BDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-195">tinyint</span><span class="sxs-lookup"><span data-stu-id="ee530-195">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-196">B フレームドロップでの通話時間の割合。</span><span class="sxs-lookup"><span data-stu-id="ee530-196">Percentage of call duration with B frame drop.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee530-197"><strong>Bp・スペック</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-197"><strong>BPDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-198">tinyint</span><span class="sxs-lookup"><span data-stu-id="ee530-198">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-199">BP フレームドロップでの通話時間の割合。</span><span class="sxs-lookup"><span data-stu-id="ee530-199">Percentage of call duration with BP frame drop.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee530-200"><strong>Bpsp・ bp</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-200"><strong>BPSPDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-201">tinyint</span><span class="sxs-lookup"><span data-stu-id="ee530-201">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-202">BPSP フレームドロップでの通話時間の割合。</span><span class="sxs-lookup"><span data-stu-id="ee530-202">Percentage of call duration with BPSP frame drop.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee530-203"><strong>BPSPIDropRatio</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-203"><strong>BPSPIDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-204">tinyint</span><span class="sxs-lookup"><span data-stu-id="ee530-204">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-205">BPSPI フレームドロップでの通話時間の割合。</span><span class="sxs-lookup"><span data-stu-id="ee530-205">Percentage of call duration with BPSPI frame drop.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee530-206"><strong>トラフィック</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-206"><strong>Inbound</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-207">bit</span><span class="sxs-lookup"><span data-stu-id="ee530-207">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ee530-208">受信側のストリームデータが受信されます。</span><span class="sxs-lookup"><span data-stu-id="ee530-208">Stream data on receiver side is received.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee530-209"><strong>発信</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-209"><strong>Outbound</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-210">bit</span><span class="sxs-lookup"><span data-stu-id="ee530-210">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ee530-211">送信側のストリームデータが受信されます。</span><span class="sxs-lookup"><span data-stu-id="ee530-211">Stream data on sender side is received.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee530-212"><strong>SenderIsCallerPAI</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-212"><strong>SenderIsCallerPAI</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-213">bit</span><span class="sxs-lookup"><span data-stu-id="ee530-213">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ee530-214">1ストリームの方向は、呼び出し元から呼び出し先へとなります。</span><span class="sxs-lookup"><span data-stu-id="ee530-214">1 means the stream direction is from the caller to callee.</span></span></p>
<p><span data-ttu-id="ee530-215">0は、ストリームの方向を呼び出し元から呼び出し元に転送します。</span><span class="sxs-lookup"><span data-stu-id="ee530-215">0 means the stream direction is from the callee to the caller.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee530-216"><strong>LossCongestionPercent</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-216"><strong>LossCongestionPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-217">float</span><span class="sxs-lookup"><span data-stu-id="ee530-217">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-218">通話が切断された輻輳状態であった時間の割合を示します。</span><span class="sxs-lookup"><span data-stu-id="ee530-218">Indicates the percentage of the time when the call was in a loss congestion state.</span></span></p>
<p><span data-ttu-id="ee530-219">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-219">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee530-220"><strong>DelayCongestionPercent</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-220"><strong>DelayCongestionPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-221">float</span><span class="sxs-lookup"><span data-stu-id="ee530-221">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-222">ネットワークパケットが遅延したために発生した、通話の割合を示します。</span><span class="sxs-lookup"><span data-stu-id="ee530-222">Indicates the percentage of the call during which congestion was caused by the delayed arrival of network packets.</span></span></p>
<p><span data-ttu-id="ee530-223">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-223">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee530-224"><strong>ContentionDetectedPercent</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-224"><strong>ContentionDetectedPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-225">float</span><span class="sxs-lookup"><span data-stu-id="ee530-225">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-226">通話がネットワークリソースに対して競合した時間の割合を示します。</span><span class="sxs-lookup"><span data-stu-id="ee530-226">Indicates the percentage of the time when the call was competing for network resources.</span></span></p>
<p><span data-ttu-id="ee530-227">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-227">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee530-228"><strong>BandwidthEstMin</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-228"><strong>BandwidthEstMin</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-229">int</span><span class="sxs-lookup"><span data-stu-id="ee530-229">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-230">通話中の最小帯域幅推定値。</span><span class="sxs-lookup"><span data-stu-id="ee530-230">Minimum amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="ee530-231">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-231">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee530-232"><strong>BandwidthEstMax</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-232"><strong>BandwidthEstMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-233">int</span><span class="sxs-lookup"><span data-stu-id="ee530-233">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-234">通話中に測定された帯域幅推定の最大量。</span><span class="sxs-lookup"><span data-stu-id="ee530-234">Maximum amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="ee530-235">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-235">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee530-236"><strong>BandwidthEstStdDev</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-236"><strong>BandwidthEstStdDev</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-237">int</span><span class="sxs-lookup"><span data-stu-id="ee530-237">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-238">通話中に測定された帯域幅推定の標準偏差。</span><span class="sxs-lookup"><span data-stu-id="ee530-238">Standard deviation of the bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="ee530-239">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-239">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee530-240"><strong>BandwidthEstAvge</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-240"><strong>BandwidthEstAvge</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-241">int</span><span class="sxs-lookup"><span data-stu-id="ee530-241">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-242">通話中に計測された平均帯域幅推定量。</span><span class="sxs-lookup"><span data-stu-id="ee530-242">Average amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="ee530-243">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-243">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee530-244"><strong>LowBandwidthForMultiview</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-244"><strong>LowBandwidthForMultiview</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-245">float</span><span class="sxs-lookup"><span data-stu-id="ee530-245">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-246">エンドポイントが、ネットワーク接続が multiview ビデオをサポートしていないと判断した通話の割合。</span><span class="sxs-lookup"><span data-stu-id="ee530-246">Percentage of the call where the endpoint determined that the network connection could not support multiview video.</span></span></p>
<p><span data-ttu-id="ee530-247">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-247">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee530-248"><strong>RelativeOneWayTotal</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-248"><strong>RelativeOneWayTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-249">float</span><span class="sxs-lookup"><span data-stu-id="ee530-249">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-250">一方向の待機時間の合計。</span><span class="sxs-lookup"><span data-stu-id="ee530-250">Total amount of one-way latency.</span></span> <span data-ttu-id="ee530-251">相対的な一方向の待ち時間は、クライアントとサーバーの間の遅延を測定します。</span><span class="sxs-lookup"><span data-stu-id="ee530-251">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="ee530-252">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-252">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee530-253"><strong>RelativeOneWayAverage</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-253"><strong>RelativeOneWayAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-254">float</span><span class="sxs-lookup"><span data-stu-id="ee530-254">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-255">一方向の待ち時間の平均値。</span><span class="sxs-lookup"><span data-stu-id="ee530-255">Average amount of one-way latency.</span></span> <span data-ttu-id="ee530-256">相対的な一方向の待ち時間は、クライアントとサーバーの間の遅延を測定します。</span><span class="sxs-lookup"><span data-stu-id="ee530-256">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="ee530-257">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-257">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee530-258"><strong>RelativeOneWayMax</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-258"><strong>RelativeOneWayMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-259">float</span><span class="sxs-lookup"><span data-stu-id="ee530-259">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-260">一方向の待機時間の上限。</span><span class="sxs-lookup"><span data-stu-id="ee530-260">Maximum amount of one-way latency.</span></span> <span data-ttu-id="ee530-261">相対的な一方向の待ち時間は、クライアントとサーバーの間の遅延を測定します。</span><span class="sxs-lookup"><span data-stu-id="ee530-261">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="ee530-262">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-262">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee530-263"><strong>RelativeOneWayBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-263"><strong>RelativeOneWayBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-264">int</span><span class="sxs-lookup"><span data-stu-id="ee530-264">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-265">1方向のバースト発生の合計。</span><span class="sxs-lookup"><span data-stu-id="ee530-265">Total one-way burst occurrences.</span></span> <span data-ttu-id="ee530-266">"Bursty" 伝送とは、安定したストリームと比べて予期しないバーストでデータが流れる伝送です。</span><span class="sxs-lookup"><span data-stu-id="ee530-266">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="ee530-267">このメトリックは、クライアントとサーバー間のデータフローを計測します。</span><span class="sxs-lookup"><span data-stu-id="ee530-267">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="ee530-268">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-268">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee530-269"><strong>RelativeOneWayBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-269"><strong>RelativeOneWayBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-270">int</span><span class="sxs-lookup"><span data-stu-id="ee530-270">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-271">全体的な1方向バースト密度。</span><span class="sxs-lookup"><span data-stu-id="ee530-271">Total one-way burst density.</span></span> <span data-ttu-id="ee530-272">"Bursty" 伝送とは、安定したストリームと比べて予期しないバーストでデータが流れる伝送です。</span><span class="sxs-lookup"><span data-stu-id="ee530-272">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="ee530-273">このメトリックは、クライアントとサーバー間のデータフローを計測します。</span><span class="sxs-lookup"><span data-stu-id="ee530-273">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="ee530-274">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-274">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee530-275"><strong>RelativeOneWayBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-275"><strong>RelativeOneWayBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-276">float</span><span class="sxs-lookup"><span data-stu-id="ee530-276">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-277">一方向のバースト期間の合計。</span><span class="sxs-lookup"><span data-stu-id="ee530-277">Total one-way burst duration.</span></span> <span data-ttu-id="ee530-278">"Bursty" 伝送とは、安定したストリームと比べて予期しないバーストでデータが流れる伝送です。</span><span class="sxs-lookup"><span data-stu-id="ee530-278">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="ee530-279">このメトリックは、クライアントとサーバー間のデータフローを計測します。</span><span class="sxs-lookup"><span data-stu-id="ee530-279">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="ee530-280">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-280">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee530-281"><strong>RelativeOneWayGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-281"><strong>RelativeOneWayGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-282">int</span><span class="sxs-lookup"><span data-stu-id="ee530-282">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-283">一方向のギャップ出現の合計。</span><span class="sxs-lookup"><span data-stu-id="ee530-283">Total one-way gap occurrences.</span></span> <span data-ttu-id="ee530-284">"Bursty" 伝送とは、安定したストリームではなく、予期しないバーストでデータが流れる伝送です。ギャップは、このようなバーストの間の遅延を示します。</span><span class="sxs-lookup"><span data-stu-id="ee530-284">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="ee530-285">このメトリックは、クライアントとサーバー間のデータフローを計測します。</span><span class="sxs-lookup"><span data-stu-id="ee530-285">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="ee530-286">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-286">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee530-287"><strong>RelativeOneWayGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-287"><strong>RelativeOneWayGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-288">float</span><span class="sxs-lookup"><span data-stu-id="ee530-288">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-289">一方向のギャップの密度の合計。</span><span class="sxs-lookup"><span data-stu-id="ee530-289">Total one-way gap density.</span></span> <span data-ttu-id="ee530-290">"Bursty" 伝送とは、安定したストリームではなく、予期しないバーストでデータが流れる伝送です。ギャップは、このようなバーストの間の遅延を示します。</span><span class="sxs-lookup"><span data-stu-id="ee530-290">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="ee530-291">このメトリックは、クライアントとサーバー間のデータフローを計測します。</span><span class="sxs-lookup"><span data-stu-id="ee530-291">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="ee530-292">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-292">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee530-293"><strong>RelativeOneWayGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-293"><strong>RelativeOneWayGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-294">float</span><span class="sxs-lookup"><span data-stu-id="ee530-294">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-295">一方向のギャップ期間の合計。</span><span class="sxs-lookup"><span data-stu-id="ee530-295">Total one-way gap duration.</span></span> <span data-ttu-id="ee530-296">"Bursty" 伝送とは、安定したストリームではなく、予期しないバーストでデータが流れる伝送です。ギャップは、このようなバーストの間の遅延を示します。</span><span class="sxs-lookup"><span data-stu-id="ee530-296">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="ee530-297">このメトリックは、クライアントとサーバー間のデータフローを計測します。</span><span class="sxs-lookup"><span data-stu-id="ee530-297">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="ee530-298">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-298">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee530-299"><strong>パケット損失率</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-299"><strong>VideoPacketLossRate</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-300">10進数 (9, 4)</span><span class="sxs-lookup"><span data-stu-id="ee530-300">decimal(9,4)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-301">ビデオパケットが失われた速度。</span><span class="sxs-lookup"><span data-stu-id="ee530-301">Rate at which video packets were lost.</span></span></p>
<p><span data-ttu-id="ee530-302">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-302">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee530-303"><strong>VideoAllocateBWAvg</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-303"><strong>VideoAllocateBWAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-304">int</span><span class="sxs-lookup"><span data-stu-id="ee530-304">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-305">ビデオに割り当てられている平均帯域幅。</span><span class="sxs-lookup"><span data-stu-id="ee530-305">Average amount of bandwidth allocated for video.</span></span></p>
<p><span data-ttu-id="ee530-306">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-306">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee530-307"><strong>SendCodecTypes</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-307"><strong>SendCodecTypes</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-308">smallint</span><span class="sxs-lookup"><span data-stu-id="ee530-308">smallint</span></span></p></td>
<td><p><span data-ttu-id="ee530-309">外部</span><span class="sxs-lookup"><span data-stu-id="ee530-309">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ee530-310">送信者が使用するビデオコーデックの種類。</span><span class="sxs-lookup"><span data-stu-id="ee530-310">Type of video codecs used by the sender.</span></span> <span data-ttu-id="ee530-311">詳細については、「 <a href="lync-server-2013-codecdescription-table.md">Lync Server 2013 の CodecDescription テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee530-311">See the <a href="lync-server-2013-codecdescription-table.md">CodecDescription table in Lync Server 2013</a> for more information.</span></span></p>
<p><span data-ttu-id="ee530-312">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-312">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee530-313"><strong>Send解像度の幅</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-313"><strong>SendResolutionWidth</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-314">int</span><span class="sxs-lookup"><span data-stu-id="ee530-314">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-315">送信者が使用した解像度の幅。</span><span class="sxs-lookup"><span data-stu-id="ee530-315">Resolution width used by the sender.</span></span></p>
<p><span data-ttu-id="ee530-316">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-316">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee530-317"><strong>Sendの解像度の高さ</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-317"><strong>SendResolutionHeight</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-318">int</span><span class="sxs-lookup"><span data-stu-id="ee530-318">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-319">送信者が使用する解像度の高さ。</span><span class="sxs-lookup"><span data-stu-id="ee530-319">Resolution height used by the sender.</span></span></p>
<p><span data-ttu-id="ee530-320">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-320">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee530-321"><strong>SendFrameRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-321"><strong>SendFrameRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-322">float</span><span class="sxs-lookup"><span data-stu-id="ee530-322">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-323">送信者が使用した平均ビデオフレームレート送信。</span><span class="sxs-lookup"><span data-stu-id="ee530-323">Average video frame rate transmission used by the sender.</span></span></p>
<p><span data-ttu-id="ee530-324">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-324">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee530-325"><strong>SendBitRateMaximum</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-325"><strong>SendBitRateMaximum</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-326">int</span><span class="sxs-lookup"><span data-stu-id="ee530-326">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-327">送信者の最大ビットレート。</span><span class="sxs-lookup"><span data-stu-id="ee530-327">Maximum bit rate for the sender.</span></span></p>
<p><span data-ttu-id="ee530-328">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-328">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee530-329"><strong>SendBitRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-329"><strong>SendBitRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-330">int</span><span class="sxs-lookup"><span data-stu-id="ee530-330">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-331">送信者の平均ビットレート。</span><span class="sxs-lookup"><span data-stu-id="ee530-331">Average bit rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee530-332"><strong>SendVideoStreamsMax</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-332"><strong>SendVideoStreamsMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-333">int</span><span class="sxs-lookup"><span data-stu-id="ee530-333">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-334">送信者が使用したビデオストリームの最大数。</span><span class="sxs-lookup"><span data-stu-id="ee530-334">Maximum number of video streams used by the sender.</span></span></p>
<p><span data-ttu-id="ee530-335">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-335">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee530-336"><strong>RecvCodecTypes</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-336"><strong>RecvCodecTypes</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-337">smallint</span><span class="sxs-lookup"><span data-stu-id="ee530-337">smallint</span></span></p></td>
<td><p><span data-ttu-id="ee530-338">外部</span><span class="sxs-lookup"><span data-stu-id="ee530-338">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ee530-339">受信者が使用するビデオコード。</span><span class="sxs-lookup"><span data-stu-id="ee530-339">Video codes used by the receiver.</span></span> <span data-ttu-id="ee530-340">詳細については、「 <a href="lync-server-2013-codecdescription-table.md">Lync Server 2013 の CodecDescription テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee530-340">See the <a href="lync-server-2013-codecdescription-table.md">CodecDescription table in Lync Server 2013</a> for more information.</span></span></p>
<p><span data-ttu-id="ee530-341">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-341">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee530-342"><strong>RecvResolutionWidth</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-342"><strong>RecvResolutionWidth</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-343">int</span><span class="sxs-lookup"><span data-stu-id="ee530-343">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-344">レシーバーで使用される解像度の幅。</span><span class="sxs-lookup"><span data-stu-id="ee530-344">Resolution width used by the receiver.</span></span></p>
<p><span data-ttu-id="ee530-345">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-345">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee530-346"><strong>RecvResolutionHeight</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-346"><strong>RecvResolutionHeight</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-347">int</span><span class="sxs-lookup"><span data-stu-id="ee530-347">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-348">受信者が使用する解像度の高さ。</span><span class="sxs-lookup"><span data-stu-id="ee530-348">Resolution height used by the receiver.</span></span></p>
<p><span data-ttu-id="ee530-349">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-349">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee530-350"><strong>受信フレームレート</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-350"><strong>RecvFrameRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-351">float</span><span class="sxs-lookup"><span data-stu-id="ee530-351">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-352">受信者が使用した平均ビデオフレームレート。</span><span class="sxs-lookup"><span data-stu-id="ee530-352">Average video frame rate used by the receiver.</span></span></p>
<p><span data-ttu-id="ee530-353">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-353">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee530-354"><strong>RecvBitRateMaximum</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-354"><strong>RecvBitRateMaximum</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-355">int</span><span class="sxs-lookup"><span data-stu-id="ee530-355">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-356">受信者の最大ビットレート。</span><span class="sxs-lookup"><span data-stu-id="ee530-356">Maximum bit rate for the receiver.</span></span></p>
<p><span data-ttu-id="ee530-357">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-357">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee530-358"><strong>RecvBitRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-358"><strong>RecvBitRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-359">int</span><span class="sxs-lookup"><span data-stu-id="ee530-359">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-360">受信者の平均ビットレート。</span><span class="sxs-lookup"><span data-stu-id="ee530-360">Average bit rate for the receiver.</span></span></p>
<p><span data-ttu-id="ee530-361">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-361">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee530-362"><strong>RecvVideoStreamsMax</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-362"><strong>RecvVideoStreamsMax</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-363">int</span><span class="sxs-lookup"><span data-stu-id="ee530-363">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-364">受信者の最大ビデオストリーム。</span><span class="sxs-lookup"><span data-stu-id="ee530-364">Maximum video streams for the receiver.</span></span></p>
<p><span data-ttu-id="ee530-365">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-365">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee530-366"><strong>RecvVideoStreamsMin</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-366"><strong>RecvVideoStreamsMin</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-367">int</span><span class="sxs-lookup"><span data-stu-id="ee530-367">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-368">受信者の最小ビデオストリーム。</span><span class="sxs-lookup"><span data-stu-id="ee530-368">Minimum video streams for the receiver.</span></span></p>
<p><span data-ttu-id="ee530-369">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-369">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee530-370"><strong>RecvVideoStreamsMode</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-370"><strong>RecvVideoStreamsMode</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-371">int</span><span class="sxs-lookup"><span data-stu-id="ee530-371">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-372">受信者のビデオモード (たとえば、ギャラリーや単一ストリーム)。</span><span class="sxs-lookup"><span data-stu-id="ee530-372">Video mode (for example, gallery or single stream) for the receiver.</span></span></p>
<p><span data-ttu-id="ee530-373">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-373">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee530-374"><strong>ビデオ plr</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-374"><strong>VideoPostFECPLR</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-375">float</span><span class="sxs-lookup"><span data-stu-id="ee530-375">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-376">転送後のエラー訂正が適用された後のパケット損失率。</span><span class="sxs-lookup"><span data-stu-id="ee530-376">Packet loss rate after forward error correction has been applied.</span></span></p>
<p><span data-ttu-id="ee530-377">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-377">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee530-378"><strong>動的機能</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-378"><strong>DynamicCapabilityPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-379">float</span><span class="sxs-lookup"><span data-stu-id="ee530-379">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-380">動的機能フラグがアクティブになった時間のパーセンテージ。</span><span class="sxs-lookup"><span data-stu-id="ee530-380">Percentage of time that the dynamic capability flag was active.</span></span></p>
<p><span data-ttu-id="ee530-381">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-381">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee530-382"><strong>解像度分</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-382"><strong>ResolutionMin</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-383">char (9)</span><span class="sxs-lookup"><span data-stu-id="ee530-383">char(9)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-384">通話中に測定された最小解像度。</span><span class="sxs-lookup"><span data-stu-id="ee530-384">Minimum resolution measured during the call.</span></span></p>
<p><span data-ttu-id="ee530-385">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-385">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee530-386"><strong>LowBitRateCallPercent</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-386"><strong>LowBitRateCallPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-387">float</span><span class="sxs-lookup"><span data-stu-id="ee530-387">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-388">低ビットレートのしきい値 (70 kb/秒) 未満の通話のパーセンテージ。</span><span class="sxs-lookup"><span data-stu-id="ee530-388">Percentage of the call below the low bit rate threshold (70 kilobits per second).</span></span></p>
<p><span data-ttu-id="ee530-389">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-389">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee530-390"><strong>LowFrameRateCallPercent</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-390"><strong>LowFrameRateCallPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-391">float</span><span class="sxs-lookup"><span data-stu-id="ee530-391">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-392">低フレームレートのしきい値を下回る通話の割合 (1 秒あたりの7.5 フレーム数)。</span><span class="sxs-lookup"><span data-stu-id="ee530-392">Percentage of the call below the low frame rate threshold (7.5 frames per second, inbound).</span></span></p>
<p><span data-ttu-id="ee530-393">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-393">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee530-394"><strong>低解像度</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-394"><strong>LowResolutionCallPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-395">float</span><span class="sxs-lookup"><span data-stu-id="ee530-395">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-396">最低の解像度で発生した通話の割合。</span><span class="sxs-lookup"><span data-stu-id="ee530-396">Percentage of the call that occurred at the lowest resolution.</span></span></p>
<p><span data-ttu-id="ee530-397">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-397">This column was introduced in Microsoft Lync Server 2013.</span></span></p>
<p><span data-ttu-id="ee530-398">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-398">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee530-399"><strong>DurationSeconds</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-399"><strong>DurationSeconds</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-400">float</span><span class="sxs-lookup"><span data-stu-id="ee530-400">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-401">通話の長さ (秒単位)。</span><span class="sxs-lookup"><span data-stu-id="ee530-401">Length of the call in seconds.</span></span></p>
<p><span data-ttu-id="ee530-402">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-402">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee530-403"><strong>IsAggregatedData</strong></span><span class="sxs-lookup"><span data-stu-id="ee530-403"><strong>IsAggregatedData</strong></span></span></p></td>
<td><p><span data-ttu-id="ee530-404">bit</span><span class="sxs-lookup"><span data-stu-id="ee530-404">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee530-405">複数の通話からデータが集計されたかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="ee530-405">Indicates whether the data has been aggregated from multiple calls.</span></span></p>
<p><span data-ttu-id="ee530-406">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee530-406">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="ee530-407">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ee530-407">


</div>

<span> </span>

</div>

</div>

</span></span></div>

