---
title: 'Lync Server 2013: VideoMetricsThreshold テーブル'
description: 'Lync Server 2013: VideoMetricsThreshold テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VideoMetricsThreshold table
ms:assetid: 2e2f4711-35ba-48c6-b15b-5aba61c4eb75
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204778(v=OCS.15)
ms:contentKeyID: 48183736
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 93cdd6fb4c3c54ac1470499490f36fee87ba283d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438870"
---
# <a name="videometricsthreshold-table-in-lync-server-2013"></a><span data-ttu-id="190bf-103">Lync Server 2013 の VideoMetricsThreshold テーブル</span><span class="sxs-lookup"><span data-stu-id="190bf-103">VideoMetricsThreshold table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="190bf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="190bf-104">

<span> </span></span></span>

<span data-ttu-id="190bf-105">_**最終更新日:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="190bf-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="190bf-106">VideoMetricsThreshold テーブルには、ビデオ通話で使用されるエクスペリエンスメトリックの品質と受け入れ可能な値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="190bf-106">The VideoMetricsThreshold table contains optimal and acceptable values for the Quality of Experience metrics used with video calls.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="190bf-107"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="190bf-107"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="190bf-108"><strong>データ型</strong></span><span class="sxs-lookup"><span data-stu-id="190bf-108"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="190bf-109"><strong>キー/インデックス</strong></span><span class="sxs-lookup"><span data-stu-id="190bf-109"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="190bf-110"><strong>詳細</strong></span><span class="sxs-lookup"><span data-stu-id="190bf-110"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="190bf-111"><strong>CallType</strong></span><span class="sxs-lookup"><span data-stu-id="190bf-111"><strong>CallType</strong></span></span></p></td>
<td><p><span data-ttu-id="190bf-112">int</span><span class="sxs-lookup"><span data-stu-id="190bf-112">int</span></span></p></td>
<td><p><span data-ttu-id="190bf-113">Primary</span><span class="sxs-lookup"><span data-stu-id="190bf-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="190bf-114">発信した通話の種類。</span><span class="sxs-lookup"><span data-stu-id="190bf-114">Type of call that was placed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="190bf-115"><strong>VideoPostFECPLROptimal</strong></span><span class="sxs-lookup"><span data-stu-id="190bf-115"><strong>VideoPostFECPLROptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="190bf-116">10進数 (5, 2)</span><span class="sxs-lookup"><span data-stu-id="190bf-116">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="190bf-117">既定値は0.05 です。</span><span class="sxs-lookup"><span data-stu-id="190bf-117">The default value is 0.05.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="190bf-118"><strong>VideoPostFECPLRAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="190bf-118"><strong>VideoPostFECPLRAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="190bf-119">10進数 (5, 2)</span><span class="sxs-lookup"><span data-stu-id="190bf-119">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="190bf-120">既定値は0.10 です。</span><span class="sxs-lookup"><span data-stu-id="190bf-120">The default value is 0.10.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="190bf-121"><strong>VideoLocalFrameLostPercentageAverageOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="190bf-121"><strong>VideoLocalFrameLostPercentageAverageOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="190bf-122">10進数 (5, 2)</span><span class="sxs-lookup"><span data-stu-id="190bf-122">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="190bf-123">既定値は5.0 です。</span><span class="sxs-lookup"><span data-stu-id="190bf-123">The default value is 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="190bf-124"><strong>VideoLocalFrameLostPercentageAverageAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="190bf-124"><strong>VideoLocalFrameLostPercentageAverageAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="190bf-125">10進数 (5, 2)</span><span class="sxs-lookup"><span data-stu-id="190bf-125">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="190bf-126">既定値は10.0 です。</span><span class="sxs-lookup"><span data-stu-id="190bf-126">The default value is 10.0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="190bf-127"><strong>RecvFrameRateAverageOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="190bf-127"><strong>RecvFrameRateAverageOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="190bf-128">10進数 (9, 4)</span><span class="sxs-lookup"><span data-stu-id="190bf-128">decimal(9,4)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="190bf-129">既定値は12.0000 です。</span><span class="sxs-lookup"><span data-stu-id="190bf-129">The default value is 12.0000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="190bf-130"><strong>RecvFramerateAverageAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="190bf-130"><strong>RecvFramerateAverageAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="190bf-131">10進数 (9, 4)</span><span class="sxs-lookup"><span data-stu-id="190bf-131">decimal(9,4)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="190bf-132">既定値は7.0000 です。</span><span class="sxs-lookup"><span data-stu-id="190bf-132">The default value is 7.0000.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="190bf-133"><strong>LowFrameRateCallPercentOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="190bf-133"><strong>LowFrameRateCallPercentOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="190bf-134">10進数 (5, 2)</span><span class="sxs-lookup"><span data-stu-id="190bf-134">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="190bf-135">既定値は5.0 です。</span><span class="sxs-lookup"><span data-stu-id="190bf-135">The default value is 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="190bf-136"><strong>LowFrameRateCallPercentAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="190bf-136"><strong>LowFrameRateCallPercentAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="190bf-137">10進数 (5, 2)</span><span class="sxs-lookup"><span data-stu-id="190bf-137">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="190bf-138">既定値は 10.0/</span><span class="sxs-lookup"><span data-stu-id="190bf-138">The default value is 10.0/</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="190bf-139"><strong>LowResolutionCallPercentOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="190bf-139"><strong>LowResolutionCallPercentOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="190bf-140">10進数 (5, 2)</span><span class="sxs-lookup"><span data-stu-id="190bf-140">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="190bf-141">既定値は5.0 です。</span><span class="sxs-lookup"><span data-stu-id="190bf-141">The default value is 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="190bf-142"><strong>LowResolutionCallPercentAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="190bf-142"><strong>LowResolutionCallPercentAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="190bf-143">10進数 (5, 2)</span><span class="sxs-lookup"><span data-stu-id="190bf-143">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="190bf-144">既定値は10.0 です。</span><span class="sxs-lookup"><span data-stu-id="190bf-144">The default value is 10.0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="190bf-145"><strong>VideoPacketLossRateOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="190bf-145"><strong>VideoPacketLossRateOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="190bf-146">@</span><span class="sxs-lookup"><span data-stu-id="190bf-146">foat</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="190bf-147">既定値は0.05 です。</span><span class="sxs-lookup"><span data-stu-id="190bf-147">The default value is 0.05.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="190bf-148"><strong>VideoPacketLossRateAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="190bf-148"><strong>VideoPacketLossRateAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="190bf-149">float</span><span class="sxs-lookup"><span data-stu-id="190bf-149">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="190bf-150">既定値は0.10 です。</span><span class="sxs-lookup"><span data-stu-id="190bf-150">The default value is 0.10.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="190bf-151"><strong>VideoFrameRateAvgOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="190bf-151"><strong>VideoFrameRateAvgOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="190bf-152">float</span><span class="sxs-lookup"><span data-stu-id="190bf-152">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="190bf-153">既定値は12です。</span><span class="sxs-lookup"><span data-stu-id="190bf-153">The default value is 12.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="190bf-154"><strong>VideoFrameRateAvgAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="190bf-154"><strong>VideoFrameRateAvgAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="190bf-155">float</span><span class="sxs-lookup"><span data-stu-id="190bf-155">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="190bf-156">既定値は7です。</span><span class="sxs-lookup"><span data-stu-id="190bf-156">The default value is 7.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="190bf-157"><strong>DynamicCapabilityPercentOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="190bf-157"><strong>DynamicCapabilityPercentOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="190bf-158">10進数 (5, 2)</span><span class="sxs-lookup"><span data-stu-id="190bf-158">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="190bf-159">既定値は5.00 です。</span><span class="sxs-lookup"><span data-stu-id="190bf-159">The default value is 5.00.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="190bf-160"><strong>DynamicCapabilityPercentAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="190bf-160"><strong>DynamicCapabilityPercentAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="190bf-161">10進数 (5, 2)</span><span class="sxs-lookup"><span data-stu-id="190bf-161">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="190bf-162">既定値は10.00 です。</span><span class="sxs-lookup"><span data-stu-id="190bf-162">The default value is 10.00.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="190bf-163">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="190bf-163">


</div>

<span> </span>

</div>

</div>

</span></span></div>

