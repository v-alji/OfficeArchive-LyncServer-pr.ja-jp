---
title: 'Lync Server 2013: AppSharingMetricsThreshold テーブル'
description: 'Lync Server 2013: AppSharingMetricsThreshold テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AppSharingMetricsThreshold table
ms:assetid: 782cfab9-01a6-4843-aea1-28f47b0b51f7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205018(v=OCS.15)
ms:contentKeyID: 48184556
ms.date: 12/09/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 092c7d08026e6b736b81043a71b4ecaabc4d5f1b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439873"
---
# <a name="appsharingmetricsthreshold-table-in-lync-server-2013"></a><span data-ttu-id="78eab-103">Lync Server 2013 の AppSharingMetricsThreshold テーブル</span><span class="sxs-lookup"><span data-stu-id="78eab-103">AppSharingMetricsThreshold table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="78eab-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="78eab-104">

<span> </span></span></span>

<span data-ttu-id="78eab-105">_**最終更新日:** 2015-12-08_</span><span class="sxs-lookup"><span data-stu-id="78eab-105">_**Topic Last Modified:** 2015-12-08_</span></span>

<span data-ttu-id="78eab-106">AppSharingMetricsThreshold の表には、アプリケーションの共有で使用されるエクスペリエンスメトリックの品質と受け入れ可能な値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="78eab-106">The AppSharingMetricsThreshold table contains optimal and acceptable values for the Quality of Experience metrics used with application sharing.</span></span> <span data-ttu-id="78eab-107">これらのしきい値は、アプリケーション共有エクスペリエンスが低品質として分類される必要があるかどうかを判断するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="78eab-107">These thresholds are used to determine if the application sharing experience should be classified as poor.</span></span>

<span data-ttu-id="78eab-108">この表は、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="78eab-108">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="78eab-109"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="78eab-109"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="78eab-110"><strong>データ型</strong></span><span class="sxs-lookup"><span data-stu-id="78eab-110"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="78eab-111"><strong>キー/インデックス</strong></span><span class="sxs-lookup"><span data-stu-id="78eab-111"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="78eab-112"><strong>詳細</strong></span><span class="sxs-lookup"><span data-stu-id="78eab-112"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="78eab-113"><strong>CallType</strong></span><span class="sxs-lookup"><span data-stu-id="78eab-113"><strong>CallType</strong></span></span></p></td>
<td><p><span data-ttu-id="78eab-114">int</span><span class="sxs-lookup"><span data-stu-id="78eab-114">int</span></span></p></td>
<td><p><span data-ttu-id="78eab-115">Primary</span><span class="sxs-lookup"><span data-stu-id="78eab-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="78eab-116">発信した通話の種類。</span><span class="sxs-lookup"><span data-stu-id="78eab-116">Type of call that was placed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78eab-117"><strong>AppliedBandwidthLimitOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="78eab-117"><strong>AppliedBandwidthLimitOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="78eab-118">int</span><span class="sxs-lookup"><span data-stu-id="78eab-118">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="78eab-119">アプリケーション共有に最適な帯域幅の制限。</span><span class="sxs-lookup"><span data-stu-id="78eab-119">Optimal bandwidth limitation for application sharing.</span></span> <span data-ttu-id="78eab-120">既定値は100万です。</span><span class="sxs-lookup"><span data-stu-id="78eab-120">The default value is 1000000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78eab-121"><strong>AppliedBandwidthLimitAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="78eab-121"><strong>AppliedBandwidthLimitAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="78eab-122">int</span><span class="sxs-lookup"><span data-stu-id="78eab-122">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="78eab-123">アプリケーション共有に対して許容可能な帯域幅制限。</span><span class="sxs-lookup"><span data-stu-id="78eab-123">Acceptable bandwidth limitation for application sharing.</span></span> <span data-ttu-id="78eab-124">既定値は50万です。</span><span class="sxs-lookup"><span data-stu-id="78eab-124">The default value is 500000.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78eab-125"><strong>SpoiledTilePercentTotalOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="78eab-125"><strong>SpoiledTilePercentTotalOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="78eab-126">10進数 (5, 2)</span><span class="sxs-lookup"><span data-stu-id="78eab-126">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="78eab-127">アプリケーション共有の品質を分類するための "損失" タイルの最適な比率。</span><span class="sxs-lookup"><span data-stu-id="78eab-127">Optimal percentage rate for “spoiled” tiles for classifying an Application Sharing quality.</span></span> <span data-ttu-id="78eab-128">この値は、閲覧者に届かなかった、共有先のコンテンツのパーセンテージです。</span><span class="sxs-lookup"><span data-stu-id="78eab-128">This value is the percentage of the content from the sharer that did not reach the viewer.</span></span> <span data-ttu-id="78eab-129">グラフィックスソースまたは ASMCU タイルから共有されているタイルがそれぞれ、共有元のタイルを破棄した場合、コンテンツは破棄 (または損失) されることがあります。</span><span class="sxs-lookup"><span data-stu-id="78eab-129">Content may be discarded (or spoiled) when the sharer discards tiles from the graphics source or the ASMCU tiles discards tiles from Sharer respectively.</span></span> <span data-ttu-id="78eab-130">既定値は11パーセントです。</span><span class="sxs-lookup"><span data-stu-id="78eab-130">The default value is 11 percent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78eab-131"><strong>SpoiledTilePercentTotalAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="78eab-131"><strong>SpoiledTilePercentTotalAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="78eab-132">10進数 (5, 2)</span><span class="sxs-lookup"><span data-stu-id="78eab-132">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="78eab-133">アプリの共有品質を分類するための "損失" タイルの cceptable のパーセンテージ率。</span><span class="sxs-lookup"><span data-stu-id="78eab-133">cceptable percentage rate for “spoiled” tiles for classifying an Application Sharing quality.</span></span> <span data-ttu-id="78eab-134">この値は、閲覧者に届かなかった、共有先のコンテンツのパーセンテージです。</span><span class="sxs-lookup"><span data-stu-id="78eab-134">This value is the percentage of the content from the sharer that did not reach the viewer.</span></span> <span data-ttu-id="78eab-135">グラフィックスソースまたは ASMCU タイルから共有されているタイルがそれぞれ、共有元のタイルを破棄した場合、コンテンツは破棄 (または損失) されることがあります。</span><span class="sxs-lookup"><span data-stu-id="78eab-135">Content may be discarded (or spoiled) when the sharer discards tiles from the graphics source or the ASMCU tiles discards tiles from Sharer respectively.</span></span> <span data-ttu-id="78eab-136">既定値は36パーセントです。</span><span class="sxs-lookup"><span data-stu-id="78eab-136">The default value is 36 percent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78eab-137"><strong>JitterInterArrivalOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="78eab-137"><strong>JitterInterArrivalOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="78eab-138">int</span><span class="sxs-lookup"><span data-stu-id="78eab-138">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="78eab-139">この列は、Microsoft Lync Server 2013 では使用されません。</span><span class="sxs-lookup"><span data-stu-id="78eab-139">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78eab-140"><strong>JitterInterArrivalAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="78eab-140"><strong>JitterInterArrivalAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="78eab-141">int</span><span class="sxs-lookup"><span data-stu-id="78eab-141">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="78eab-142">この列は、Microsoft Lync Server 2013 では使用されません。</span><span class="sxs-lookup"><span data-stu-id="78eab-142">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78eab-143"><strong>RelativeOneWayBurstDensityOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="78eab-143"><strong>RelativeOneWayBurstDensityOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="78eab-144">float</span><span class="sxs-lookup"><span data-stu-id="78eab-144">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="78eab-145">この列は、Microsoft Lync Server 2013 では使用されません。</span><span class="sxs-lookup"><span data-stu-id="78eab-145">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78eab-146"><strong>RelativeOneWayBurstDensityAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="78eab-146"><strong>RelativeOneWayBurstDensityAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="78eab-147">float</span><span class="sxs-lookup"><span data-stu-id="78eab-147">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="78eab-148">この列は、Microsoft Lync Server 2013 では使用されません。</span><span class="sxs-lookup"><span data-stu-id="78eab-148">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78eab-149"><strong>RDPTileProcessingLatencyBurstDensityOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="78eab-149"><strong>RDPTileProcessingLatencyBurstDensityOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="78eab-150">float</span><span class="sxs-lookup"><span data-stu-id="78eab-150">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="78eab-151">この列は、Microsoft Lync Server 2013 では使用されません。</span><span class="sxs-lookup"><span data-stu-id="78eab-151">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78eab-152"><strong>RDPTileProcessingLatencyBurstDensityAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="78eab-152"><strong>RDPTileProcessingLatencyBurstDensityAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="78eab-153">float</span><span class="sxs-lookup"><span data-stu-id="78eab-153">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="78eab-154">この列は、Microsoft Lync Server 2013 では使用されません。</span><span class="sxs-lookup"><span data-stu-id="78eab-154">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78eab-155"><strong>RelativeOneWayAverageOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="78eab-155"><strong>RelativeOneWayAverageOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="78eab-156">float</span><span class="sxs-lookup"><span data-stu-id="78eab-156">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="78eab-157">アプリケーション共有に関連する2つのメディアエンドポイント間の相対的な一方向の遅延の最適値。</span><span class="sxs-lookup"><span data-stu-id="78eab-157">Optimal value for the relative one-way delay between the two media endpoints involved in the application sharing.</span></span> <span data-ttu-id="78eab-158">これは 1 ホップの遅延の測定です。</span><span class="sxs-lookup"><span data-stu-id="78eab-158">This is a single-hop latency measure.</span></span> <span data-ttu-id="78eab-159">既定値は1.0 秒です。</span><span class="sxs-lookup"><span data-stu-id="78eab-159">The default value is 1.0 seconds.</span></span></p>
<p><span data-ttu-id="78eab-160">この列は、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="78eab-160">The column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78eab-161"><strong>RelativeOneWayAverageAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="78eab-161"><strong>RelativeOneWayAverageAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="78eab-162">float</span><span class="sxs-lookup"><span data-stu-id="78eab-162">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="78eab-163">アプリケーション共有に関連する2つのメディアエンドポイント間の相対的な一方向の遅延の最適値。</span><span class="sxs-lookup"><span data-stu-id="78eab-163">Optimal value for the relative one-way delay between the two media endpoints involved in the application sharing.</span></span> <span data-ttu-id="78eab-164">これは 1 ホップの遅延の測定です。</span><span class="sxs-lookup"><span data-stu-id="78eab-164">This is a single-hop latency measure.</span></span> <span data-ttu-id="78eab-165">既定値は1.75 秒です。</span><span class="sxs-lookup"><span data-stu-id="78eab-165">The default value is 1.75 seconds.</span></span></p>
<p><span data-ttu-id="78eab-166">この列は、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="78eab-166">The column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78eab-167"><strong>RDPTileProcessingLatencyAverageOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="78eab-167"><strong>RDPTileProcessingLatencyAverageOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="78eab-168">float</span><span class="sxs-lookup"><span data-stu-id="78eab-168">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="78eab-169">表示セッションの間の会議サーバーとしての平均 RDP タイル処理の待機時間の最適値。</span><span class="sxs-lookup"><span data-stu-id="78eab-169">Optimal value of the average RDP tile processing latency in the AS Conferencing Server over the duration of the viewing session.</span></span> <span data-ttu-id="78eab-170">[待ち時間] は、サーバー (シナリオによっては共有先または MCU) で開始フレームがエンコードされてから、同じ開始フレームが viewer でデコードされるタイミングの差です。</span><span class="sxs-lookup"><span data-stu-id="78eab-170">Latency is the time difference between when the Start Frame is encoded on the server (sharer or MCU depending on the scenario) and the same Start Frame is decoded on the viewer.</span></span></p>
<p><span data-ttu-id="78eab-171">平均値が高いと、表示の際の遅延が大きくなります。</span><span class="sxs-lookup"><span data-stu-id="78eab-171">A high average reflects a longer delay in the viewing experience.</span></span> <span data-ttu-id="78eab-172">過負荷の会議サーバーでは平均遅延が大きくなる場合があります。</span><span class="sxs-lookup"><span data-stu-id="78eab-172">An overloaded conferencing server may experience higher average delays.</span></span> <span data-ttu-id="78eab-173">既定値は200ms です。</span><span class="sxs-lookup"><span data-stu-id="78eab-173">The default value is 200ms.</span></span></p>
<p><span data-ttu-id="78eab-174">この列は、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="78eab-174">The column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78eab-175"><strong>RDPTileProcessingLatencyAverageAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="78eab-175"><strong>RDPTileProcessingLatencyAverageAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="78eab-176">float</span><span class="sxs-lookup"><span data-stu-id="78eab-176">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="78eab-177">表示セッション中の会議サーバーとしての平均 RDP タイル処理待ち時間の値。</span><span class="sxs-lookup"><span data-stu-id="78eab-177">Acceptable value of the average RDP tile processing latency in the AS Conferencing Server over the duration of the viewing session.</span></span> <span data-ttu-id="78eab-178">[待ち時間] は、サーバー (シナリオによっては共有先または MCU) で開始フレームがエンコードされてから、同じ開始フレームが viewer でデコードされるタイミングの差です。</span><span class="sxs-lookup"><span data-stu-id="78eab-178">Latency is the time difference between when the Start Frame is encoded on the server (sharer or MCU depending on the scenario) and the same Start Frame is decoded on the viewer.</span></span></p>
<p><span data-ttu-id="78eab-179">平均値が高いと、表示の際の遅延が大きくなります。</span><span class="sxs-lookup"><span data-stu-id="78eab-179">A high average reflects a longer delay in the viewing experience.</span></span> <span data-ttu-id="78eab-180">過負荷の会議サーバーでは平均遅延が大きくなる場合があります。</span><span class="sxs-lookup"><span data-stu-id="78eab-180">An overloaded conferencing server may experience higher average delays.</span></span> <span data-ttu-id="78eab-181">既定値は200ms です。</span><span class="sxs-lookup"><span data-stu-id="78eab-181">The default value is 200ms.</span></span></p>
<p><span data-ttu-id="78eab-182">この列は、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="78eab-182">The column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="78eab-183">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="78eab-183">


</div>

<span> </span>

</div>

</div>

</span></span></div>

