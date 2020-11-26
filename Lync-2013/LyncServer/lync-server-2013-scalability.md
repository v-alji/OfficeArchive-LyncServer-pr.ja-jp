---
title: Lync Server 2013 のスケーラビリティ
description: Lync Server 2013 のスケーラビリティ。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Scalability
ms:assetid: 46fa0cb5-1507-4a12-ad3f-ba64585e2dc4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg417160(v=OCS.15)
ms:contentKeyID: 48183995
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 28cd5820755ffd1eb863ed6f2369b5756a7ae3f5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442118"
---
# <a name="scalability-with-lync-server-2013"></a><span data-ttu-id="7f28e-103">Lync Server 2013 のスケーラビリティ</span><span class="sxs-lookup"><span data-stu-id="7f28e-103">Scalability with Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7f28e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7f28e-104">

<span> </span></span></span>

<span data-ttu-id="7f28e-105">_**最終更新日:** 2012-06-25_</span><span class="sxs-lookup"><span data-stu-id="7f28e-105">_**Topic Last Modified:** 2012-06-25_</span></span>

<span data-ttu-id="7f28e-106">Lync Server は、Enterprise Edition と Standard Edition の2つのエディションで提供されています。</span><span class="sxs-lookup"><span data-stu-id="7f28e-106">Lync Server is offered in two editions, Enterprise Edition and Standard Edition.</span></span> <span data-ttu-id="7f28e-107">さまざまなエディションは、主にさまざまな規模の組織向けに設計されています。</span><span class="sxs-lookup"><span data-stu-id="7f28e-107">The different editions are intended primarily for different sizes of organizations.</span></span> <span data-ttu-id="7f28e-108">次の表に示すように、両方のエディションでは、高可用性と障害回復を除き、すべてのワークロードのすべての機能がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="7f28e-108">As shown in the following table, both editions support all functionality in all workloads, except for high availability and disaster recovery.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7f28e-109">機能</span><span class="sxs-lookup"><span data-stu-id="7f28e-109">Feature</span></span></th>
<th><span data-ttu-id="7f28e-110">Enterprise Edition でサポートされていますか?</span><span class="sxs-lookup"><span data-stu-id="7f28e-110">Supported in Enterprise Edition?</span></span></th>
<th><span data-ttu-id="7f28e-111">Standard Edition でサポートされていますか?</span><span class="sxs-lookup"><span data-stu-id="7f28e-111">Supported in Standard Edition?</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7f28e-112">インスタントメッセージング (IM) とプレゼンス</span><span class="sxs-lookup"><span data-stu-id="7f28e-112">Instant messaging (IM) and presence</span></span></p></td>
<td><p><span data-ttu-id="7f28e-113">はい</span><span class="sxs-lookup"><span data-stu-id="7f28e-113">Yes</span></span></p></td>
<td><p><span data-ttu-id="7f28e-114">はい</span><span class="sxs-lookup"><span data-stu-id="7f28e-114">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f28e-115">会議</span><span class="sxs-lookup"><span data-stu-id="7f28e-115">Conferencing</span></span></p></td>
<td><p><span data-ttu-id="7f28e-116">はい</span><span class="sxs-lookup"><span data-stu-id="7f28e-116">Yes</span></span></p></td>
<td><p><span data-ttu-id="7f28e-117">はい</span><span class="sxs-lookup"><span data-stu-id="7f28e-117">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f28e-118">音声ビデオ会議</span><span class="sxs-lookup"><span data-stu-id="7f28e-118">A/V conferencing</span></span></p></td>
<td><p><span data-ttu-id="7f28e-119">はい</span><span class="sxs-lookup"><span data-stu-id="7f28e-119">Yes</span></span></p></td>
<td><p><span data-ttu-id="7f28e-120">はい</span><span class="sxs-lookup"><span data-stu-id="7f28e-120">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f28e-121">ダイヤルイン会議</span><span class="sxs-lookup"><span data-stu-id="7f28e-121">Dial-in conferencing</span></span></p></td>
<td><p><span data-ttu-id="7f28e-122">はい</span><span class="sxs-lookup"><span data-stu-id="7f28e-122">Yes</span></span></p></td>
<td><p><span data-ttu-id="7f28e-123">はい</span><span class="sxs-lookup"><span data-stu-id="7f28e-123">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f28e-124">Enterprise Voice</span><span class="sxs-lookup"><span data-stu-id="7f28e-124">Enterprise Voice</span></span></p></td>
<td><p><span data-ttu-id="7f28e-125">はい</span><span class="sxs-lookup"><span data-stu-id="7f28e-125">Yes</span></span></p></td>
<td><p><span data-ttu-id="7f28e-126">はい</span><span class="sxs-lookup"><span data-stu-id="7f28e-126">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f28e-127">仮想化</span><span class="sxs-lookup"><span data-stu-id="7f28e-127">Virtualization</span></span></p></td>
<td><p><span data-ttu-id="7f28e-128">はい</span><span class="sxs-lookup"><span data-stu-id="7f28e-128">Yes</span></span></p></td>
<td><p><span data-ttu-id="7f28e-129">はい</span><span class="sxs-lookup"><span data-stu-id="7f28e-129">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f28e-130">高可用性、フェールオーバー、および障害回復</span><span class="sxs-lookup"><span data-stu-id="7f28e-130">High availability, failover, and disaster recovery</span></span></p></td>
<td><p><span data-ttu-id="7f28e-131">はい</span><span class="sxs-lookup"><span data-stu-id="7f28e-131">Yes</span></span></p></td>
<td><p><span data-ttu-id="7f28e-132">いいえ</span><span class="sxs-lookup"><span data-stu-id="7f28e-132">No</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="7f28e-133">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7f28e-133">


</div>

<span> </span>

</div>

</div>

</span></span></div>

