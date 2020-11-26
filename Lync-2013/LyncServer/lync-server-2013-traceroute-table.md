---
title: 'Lync Server 2013: TraceRoute テーブル'
description: 'Lync Server 2013: TraceRoute テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: TraceRoute table
ms:assetid: b9493cef-6ece-4f13-bf68-dbf132aab4f4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205205(v=OCS.15)
ms:contentKeyID: 48185242
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8af33e572065fbab1eaaaef684997e7f95edaed9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440837"
---
# <a name="traceroute-table-in-lync-server-2013"></a><span data-ttu-id="75d4c-103">Lync Server 2013 の TraceRoute テーブル</span><span class="sxs-lookup"><span data-stu-id="75d4c-103">TraceRoute table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="75d4c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="75d4c-104">

<span> </span></span></span>

<span data-ttu-id="75d4c-105">_**最終更新日:** 2014-02-21_</span><span class="sxs-lookup"><span data-stu-id="75d4c-105">_**Topic Last Modified:** 2014-02-21_</span></span>

<span data-ttu-id="75d4c-106">TraceRoute テーブルには、通話のルーティング情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="75d4c-106">The TraceRoute table contains routing information from calls.</span></span> <span data-ttu-id="75d4c-107">この表は、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="75d4c-107">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="75d4c-108"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="75d4c-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="75d4c-109"><strong>データ型</strong></span><span class="sxs-lookup"><span data-stu-id="75d4c-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="75d4c-110"><strong>キー/インデックス</strong></span><span class="sxs-lookup"><span data-stu-id="75d4c-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="75d4c-111"><strong>詳細</strong></span><span class="sxs-lookup"><span data-stu-id="75d4c-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75d4c-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="75d4c-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="75d4c-113">datetime</span><span class="sxs-lookup"><span data-stu-id="75d4c-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="75d4c-114">プライマリ、外部</span><span class="sxs-lookup"><span data-stu-id="75d4c-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="75d4c-115">通話が開始された日付と時刻。</span><span class="sxs-lookup"><span data-stu-id="75d4c-115">Date and time that the call began.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75d4c-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="75d4c-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="75d4c-117">int</span><span class="sxs-lookup"><span data-stu-id="75d4c-117">int</span></span></p></td>
<td><p><span data-ttu-id="75d4c-118">プライマリ、外部</span><span class="sxs-lookup"><span data-stu-id="75d4c-118">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="75d4c-119">同じ日付と同時に開始された可能性がある複数の通話を区別するために使用される一意の識別子。</span><span class="sxs-lookup"><span data-stu-id="75d4c-119">Unique identifier used to distinguish between multiple calls that might have begun on the same date and at the same time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75d4c-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="75d4c-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="75d4c-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="75d4c-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="75d4c-122">プライマリ、外部</span><span class="sxs-lookup"><span data-stu-id="75d4c-122">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="75d4c-123">通話で使用されるビデオラインの種類を表します。</span><span class="sxs-lookup"><span data-stu-id="75d4c-123">Represents the type of video line used in the call.</span></span> <span data-ttu-id="75d4c-124">有効な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="75d4c-124">Allowed values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="75d4c-125">0–音声</span><span class="sxs-lookup"><span data-stu-id="75d4c-125">0 – Audio</span></span></p></li>
<li><p><span data-ttu-id="75d4c-126">1-ビデオ</span><span class="sxs-lookup"><span data-stu-id="75d4c-126">1 – Video</span></span></p></li>
<li><p><span data-ttu-id="75d4c-127">2-パノラマビデオ</span><span class="sxs-lookup"><span data-stu-id="75d4c-127">2 – Panoramic video</span></span></p></li>
<li><p><span data-ttu-id="75d4c-128">3-アプリケーション/デスクトップ共有</span><span class="sxs-lookup"><span data-stu-id="75d4c-128">3 – Application/Desktop sharing</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75d4c-129"><strong>FromCaller</strong></span><span class="sxs-lookup"><span data-stu-id="75d4c-129"><strong>FromCaller</strong></span></span></p></td>
<td><p><span data-ttu-id="75d4c-130">bit</span><span class="sxs-lookup"><span data-stu-id="75d4c-130">bit</span></span></p></td>
<td><p><span data-ttu-id="75d4c-131">Primary</span><span class="sxs-lookup"><span data-stu-id="75d4c-131">Primary</span></span></p></td>
<td><p><span data-ttu-id="75d4c-132">通話を発信したエンドポイント。</span><span class="sxs-lookup"><span data-stu-id="75d4c-132">Endpoint that placed the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75d4c-133"><strong>ホップ</strong></span><span class="sxs-lookup"><span data-stu-id="75d4c-133"><strong>Hop</strong></span></span></p></td>
<td><p><span data-ttu-id="75d4c-134">int</span><span class="sxs-lookup"><span data-stu-id="75d4c-134">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="75d4c-135">ネットワークホップ/</span><span class="sxs-lookup"><span data-stu-id="75d4c-135">Network hop/</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75d4c-136"><strong>IPAddressKey</strong></span><span class="sxs-lookup"><span data-stu-id="75d4c-136"><strong>IPAddressKey</strong></span></span></p></td>
<td><p><span data-ttu-id="75d4c-137">int</span><span class="sxs-lookup"><span data-stu-id="75d4c-137">int</span></span></p></td>
<td><p><span data-ttu-id="75d4c-138">外部</span><span class="sxs-lookup"><span data-stu-id="75d4c-138">Foreign</span></span></p></td>
<td><p><span data-ttu-id="75d4c-139">IP アドレスの一意の識別子。</span><span class="sxs-lookup"><span data-stu-id="75d4c-139">Unique identifier for the IP address.</span></span> <span data-ttu-id="75d4c-140">IP アドレス情報は、 <a href="lync-server-2013-ipaddress-table.md">Lync Server 2013 の IPAddress テーブル</a>に格納されます。</span><span class="sxs-lookup"><span data-stu-id="75d4c-140">IP address information is stored in the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75d4c-141"><strong>RTT</strong></span><span class="sxs-lookup"><span data-stu-id="75d4c-141"><strong>RTT</strong></span></span></p></td>
<td><p><span data-ttu-id="75d4c-142">int</span><span class="sxs-lookup"><span data-stu-id="75d4c-142">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="75d4c-143">往復時間。</span><span class="sxs-lookup"><span data-stu-id="75d4c-143">Roundtrip time.</span></span> <span data-ttu-id="75d4c-144">往復時間は、ボイスパケットがその宛先に到達し、受信した通知を返信するのにかかる時間を測定します。</span><span class="sxs-lookup"><span data-stu-id="75d4c-144">The roundtrip time measures the amount of time it takes for a voice packet to reach its destination and then send back notification that it was received.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="75d4c-145">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="75d4c-145">


</div>

<span> </span>

</div>

</div>

</span></span></div>

