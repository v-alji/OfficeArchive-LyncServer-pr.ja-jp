---
title: 'Lync Server 2013: Conference テーブル'
description: 'Lync Server 2013: 会議の表。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conference table
ms:assetid: 2a2c327c-4719-42dc-a3bb-6dbc0864d9af
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425762(v=OCS.15)
ms:contentKeyID: 48183700
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 565725b527399cb3be55c649dfd74d8bcb5f13a2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434467"
---
# <a name="conference-table-in-lync-server-2013"></a><span data-ttu-id="8c6c0-103">Lync Server 2013 の Conference テーブル</span><span class="sxs-lookup"><span data-stu-id="8c6c0-103">Conference table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8c6c0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8c6c0-104">

<span> </span></span></span>

<span data-ttu-id="8c6c0-105">_**最終更新日:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="8c6c0-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="8c6c0-106">会議の表は、サポートされているテーブルです。</span><span class="sxs-lookup"><span data-stu-id="8c6c0-106">The Conference table is a supporting table.</span></span> <span data-ttu-id="8c6c0-107">各レコードは、1つの会議またはピアツーピアセッションを表します。</span><span class="sxs-lookup"><span data-stu-id="8c6c0-107">Each record represents one conference or peer-to-peer session.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8c6c0-108"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="8c6c0-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="8c6c0-109"><strong>データ型</strong></span><span class="sxs-lookup"><span data-stu-id="8c6c0-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="8c6c0-110"><strong>キー/インデックス</strong></span><span class="sxs-lookup"><span data-stu-id="8c6c0-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="8c6c0-111"><strong>詳細</strong></span><span class="sxs-lookup"><span data-stu-id="8c6c0-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8c6c0-112"><strong>ConferenceKey</strong></span><span class="sxs-lookup"><span data-stu-id="8c6c0-112"><strong>ConferenceKey</strong></span></span></p></td>
<td><p><span data-ttu-id="8c6c0-113">int</span><span class="sxs-lookup"><span data-stu-id="8c6c0-113">int</span></span></p></td>
<td><p><span data-ttu-id="8c6c0-114">Primary</span><span class="sxs-lookup"><span data-stu-id="8c6c0-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="8c6c0-115">この会議レコードを識別する一意の番号です。</span><span class="sxs-lookup"><span data-stu-id="8c6c0-115">Unique number identifying this conference record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c6c0-116"><strong>ConfURI</strong></span><span class="sxs-lookup"><span data-stu-id="8c6c0-116"><strong>ConfURI</strong></span></span></p></td>
<td><p><span data-ttu-id="8c6c0-117">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="8c6c0-117">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="8c6c0-118">一意</span><span class="sxs-lookup"><span data-stu-id="8c6c0-118">unique</span></span></p></td>
<td><p><span data-ttu-id="8c6c0-119">会議の URI (会議の場合) または [この Id がピアツーピアセッションの場合] です。</span><span class="sxs-lookup"><span data-stu-id="8c6c0-119">Conference URI if this is a conference, or DialogID if this is a peer-to-peer session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c6c0-120"><strong>サム</strong></span><span class="sxs-lookup"><span data-stu-id="8c6c0-120"><strong>Checksum</strong></span></span></p></td>
<td><p><span data-ttu-id="8c6c0-121">int</span><span class="sxs-lookup"><span data-stu-id="8c6c0-121">int</span></span></p></td>
<td><p><span data-ttu-id="8c6c0-122">位置</span><span class="sxs-lookup"><span data-stu-id="8c6c0-122">index</span></span></p></td>
<td><p><span data-ttu-id="8c6c0-123">会議 URI のチェックサム。</span><span class="sxs-lookup"><span data-stu-id="8c6c0-123">Checksum of the conference URI.</span></span> <span data-ttu-id="8c6c0-124">これは内部的に使用されます。</span><span class="sxs-lookup"><span data-stu-id="8c6c0-124">This is used internally.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c6c0-125"><strong>Nextupdatupdat</strong></span><span class="sxs-lookup"><span data-stu-id="8c6c0-125"><strong>NextUpdateTS</strong></span></span></p></td>
<td><p><span data-ttu-id="8c6c0-126">datetime</span><span class="sxs-lookup"><span data-stu-id="8c6c0-126">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8c6c0-127">内部使用のみ。</span><span class="sxs-lookup"><span data-stu-id="8c6c0-127">For internal use only.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="8c6c0-128">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8c6c0-128">


</div>

<span> </span>

</div>

</div>

</span></span></div>

