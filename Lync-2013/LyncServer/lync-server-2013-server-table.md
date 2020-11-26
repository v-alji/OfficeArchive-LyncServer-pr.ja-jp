---
title: 'Lync Server 2013: サーバー テーブル'
description: 'Lync Server 2013: サーバーテーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Server table
ms:assetid: 9af89d08-d35a-48e8-b56d-6df292f973cc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398801(v=OCS.15)
ms:contentKeyID: 48184890
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 00990a91aec64063480d96a16380171990913ad4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441852"
---
# <a name="server-table-in-lync-server-2013"></a><span data-ttu-id="c5cd9-103">Lync Server 2013 のサーバー テーブル</span><span class="sxs-lookup"><span data-stu-id="c5cd9-103">Server table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c5cd9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c5cd9-104">

<span> </span></span></span>

<span data-ttu-id="c5cd9-105">_**最終更新日:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="c5cd9-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="c5cd9-106">サーバーテーブルは、サポートされているテーブルです。</span><span class="sxs-lookup"><span data-stu-id="c5cd9-106">The Server table is a supporting table.</span></span> <span data-ttu-id="c5cd9-107">各レコードは1つのサーバーを表します。</span><span class="sxs-lookup"><span data-stu-id="c5cd9-107">Each record represents one server.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c5cd9-108"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="c5cd9-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="c5cd9-109"><strong>データ型</strong></span><span class="sxs-lookup"><span data-stu-id="c5cd9-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="c5cd9-110"><strong>キー/インデックス</strong></span><span class="sxs-lookup"><span data-stu-id="c5cd9-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="c5cd9-111"><strong>詳細</strong></span><span class="sxs-lookup"><span data-stu-id="c5cd9-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5cd9-112"><strong>ServerKey</strong></span><span class="sxs-lookup"><span data-stu-id="c5cd9-112"><strong>ServerKey</strong></span></span></p></td>
<td><p><span data-ttu-id="c5cd9-113">int</span><span class="sxs-lookup"><span data-stu-id="c5cd9-113">int</span></span></p></td>
<td><p><span data-ttu-id="c5cd9-114">Primary</span><span class="sxs-lookup"><span data-stu-id="c5cd9-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="c5cd9-115">サーバーを識別する一意の番号。</span><span class="sxs-lookup"><span data-stu-id="c5cd9-115">Unique number identifying the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5cd9-116"><strong>同一の Dnorip</strong></span><span class="sxs-lookup"><span data-stu-id="c5cd9-116"><strong>FQDNOrIP</strong></span></span></p></td>
<td><p><span data-ttu-id="c5cd9-117">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="c5cd9-117">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="c5cd9-118">位置</span><span class="sxs-lookup"><span data-stu-id="c5cd9-118">index</span></span></p></td>
<td><p><span data-ttu-id="c5cd9-119">MAC アドレス文字列。</span><span class="sxs-lookup"><span data-stu-id="c5cd9-119">MAC address string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5cd9-120"><strong>ServerType</strong></span><span class="sxs-lookup"><span data-stu-id="c5cd9-120"><strong>ServerType</strong></span></span></p></td>
<td><p><span data-ttu-id="c5cd9-121">int</span><span class="sxs-lookup"><span data-stu-id="c5cd9-121">int</span></span></p></td>
<td><p><span data-ttu-id="c5cd9-122">外部</span><span class="sxs-lookup"><span data-stu-id="c5cd9-122">Foreign</span></span></p></td>
<td><p><span data-ttu-id="c5cd9-123">1: 仲介サーバー</span><span class="sxs-lookup"><span data-stu-id="c5cd9-123">1: Mediation Server</span></span></p>
<p><span data-ttu-id="c5cd9-124">2: a/v 会議 Server16394: A/V Edge service32769: ゲートウェイ</span><span class="sxs-lookup"><span data-stu-id="c5cd9-124">2: A/V Conferencing Server16394: A/V Edge service32769: Gateway</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5cd9-125"><strong>PoolName</strong></span><span class="sxs-lookup"><span data-stu-id="c5cd9-125"><strong>PoolName</strong></span></span></p></td>
<td><p><span data-ttu-id="c5cd9-126">nvarchar (512)</span><span class="sxs-lookup"><span data-stu-id="c5cd9-126">nvarchar(512)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c5cd9-127">サーバーが所属するプール。</span><span class="sxs-lookup"><span data-stu-id="c5cd9-127">Pool the server belongs to.</span></span> <span data-ttu-id="c5cd9-128">A/V 会議サーバーにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="c5cd9-128">Only applicable for the A/V Conferencing Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5cd9-129"><strong>Nextupdatupdat</strong></span><span class="sxs-lookup"><span data-stu-id="c5cd9-129"><strong>NextUpdateTS</strong></span></span></p></td>
<td><p><span data-ttu-id="c5cd9-130">datetime</span><span class="sxs-lookup"><span data-stu-id="c5cd9-130">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c5cd9-131">内部使用のみ。</span><span class="sxs-lookup"><span data-stu-id="c5cd9-131">For internal use only.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="c5cd9-132">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c5cd9-132">


</div>

<span> </span>

</div>

</div>

</span></span></div>

