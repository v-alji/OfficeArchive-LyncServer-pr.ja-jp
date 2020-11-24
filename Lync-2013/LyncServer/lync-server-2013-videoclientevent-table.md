---
title: 'Lync Server 2013: VideoClientEvent テーブル'
description: 'Lync Server 2013: VideoClientEvent テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VideoClientEvent table
ms:assetid: e8ab963b-fe1d-45b3-b9bd-66a5f44c1629
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399039(v=OCS.15)
ms:contentKeyID: 48185891
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ae73ac2548e838241febe60a2d31f80983b01de5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399998"
---
# <a name="videoclientevent-table-in-lync-server-2013"></a><span data-ttu-id="13a24-103">Lync Server 2013 の VideoClientEvent テーブル</span><span class="sxs-lookup"><span data-stu-id="13a24-103">VideoClientEvent table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="13a24-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="13a24-104">

<span> </span></span></span>

<span data-ttu-id="13a24-105">_**最終更新日:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="13a24-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="13a24-106">各レコードには、ビデオ通話での1つのエンドポイントのクライアントイベントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="13a24-106">Each record contains client event for one endpoint in a video call.</span></span> <span data-ttu-id="13a24-107">通常、1つの通話には2つのレコードがあります。1つは呼び出し元用、もう1つは呼び出し先用です。</span><span class="sxs-lookup"><span data-stu-id="13a24-107">Usually, one call has two records, one for caller and one for callee.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="13a24-108"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="13a24-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="13a24-109"><strong>データ型</strong></span><span class="sxs-lookup"><span data-stu-id="13a24-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="13a24-110"><strong>キー/インデックス</strong></span><span class="sxs-lookup"><span data-stu-id="13a24-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="13a24-111"><strong>詳細</strong></span><span class="sxs-lookup"><span data-stu-id="13a24-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="13a24-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="13a24-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="13a24-113">datetime</span><span class="sxs-lookup"><span data-stu-id="13a24-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="13a24-114">Primary</span><span class="sxs-lookup"><span data-stu-id="13a24-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="13a24-115"><a href="lync-server-2013-medialine-table.md">Lync Server 2013 の MediaLine テーブル</a>から参照されている。</span><span class="sxs-lookup"><span data-stu-id="13a24-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13a24-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="13a24-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="13a24-117">int</span><span class="sxs-lookup"><span data-stu-id="13a24-117">int</span></span></p></td>
<td><p><span data-ttu-id="13a24-118">Primary</span><span class="sxs-lookup"><span data-stu-id="13a24-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="13a24-119"><a href="lync-server-2013-medialine-table.md">Lync Server 2013 の MediaLine テーブル</a>から参照されている。</span><span class="sxs-lookup"><span data-stu-id="13a24-119">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13a24-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="13a24-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="13a24-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="13a24-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="13a24-122">Primary</span><span class="sxs-lookup"><span data-stu-id="13a24-122">Primary</span></span></p></td>
<td><p><span data-ttu-id="13a24-123"><a href="lync-server-2013-medialine-table.md">Lync Server 2013 の MediaLine テーブル</a>から参照されている。</span><span class="sxs-lookup"><span data-stu-id="13a24-123">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13a24-124"><strong>FromCaller</strong></span><span class="sxs-lookup"><span data-stu-id="13a24-124"><strong>FromCaller</strong></span></span></p></td>
<td><p><span data-ttu-id="13a24-125">bit</span><span class="sxs-lookup"><span data-stu-id="13a24-125">bit</span></span></p></td>
<td><p><span data-ttu-id="13a24-126">Primary</span><span class="sxs-lookup"><span data-stu-id="13a24-126">Primary</span></span></p></td>
<td><p><span data-ttu-id="13a24-127">0: 呼び出し先のデータ</span><span class="sxs-lookup"><span data-stu-id="13a24-127">0: Callee’s data</span></span></p>
<p><span data-ttu-id="13a24-128">1: 発信者のデータ</span><span class="sxs-lookup"><span data-stu-id="13a24-128">1: Caller’s data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13a24-129"><strong>NetworkBandwidthLowEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="13a24-129"><strong>NetworkBandwidthLowEventRatio</strong></span></span></p></td>
<td></td>
<td><p> </p></td>
<td><p><span data-ttu-id="13a24-130">セッションのパーセンテージ低帯域幅イベントが ' Bad ' 状態に対して発生しました。</span><span class="sxs-lookup"><span data-stu-id="13a24-130">Percentage of session the LowBandwidth event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="13a24-131">利用可能な音声エクスペリエンスを実現するには、利用可能な帯域幅が不足しています。</span><span class="sxs-lookup"><span data-stu-id="13a24-131">The available bandwidth is insufficient for an acceptable voice experience.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13a24-132"><strong>NetworkReceiveQualityEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="13a24-132"><strong>NetworkReceiveQualityEventRatio</strong></span></span></p></td>
<td></td>
<td><p> </p></td>
<td><p><span data-ttu-id="13a24-133">セッションのパーセンテージ ReceiveSendQuality イベントが ' Bad ' 状態で発生しました。</span><span class="sxs-lookup"><span data-stu-id="13a24-133">Percentage of session the ReceiveSendQuality event was fired for ‘Bad’ state.</span></span></p>
<p><span data-ttu-id="13a24-134">ネットワーク品質は、ジッタまたはパケット損失の観点では深刻であり、受信中のオーディオの品質に影響します。</span><span class="sxs-lookup"><span data-stu-id="13a24-134">Network quality in terms of jitter or packet loss is severe and impacts the quality of audio being received.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="13a24-135">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="13a24-135">


</div>

<span> </span>

</div>

</div>

</span></span></div>

