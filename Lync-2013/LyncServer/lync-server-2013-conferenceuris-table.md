---
title: 'Lync Server 2013: ConferenceUris テーブル'
description: 'Lync Server 2013: ConferenceUris テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ConferenceUris table
ms:assetid: b1721d52-3c65-45ea-8997-06af8fef93fc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412854(v=OCS.15)
ms:contentKeyID: 48185160
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a142aa9ad1fe4d3ae92aa3e21aa9eee505457cbe
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434390"
---
# <a name="conferenceuris-table-in-lync-server-2013"></a><span data-ttu-id="83a08-103">Lync Server 2013 の ConferenceUris テーブル</span><span class="sxs-lookup"><span data-stu-id="83a08-103">ConferenceUris table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="83a08-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="83a08-104">

<span> </span></span></span>

<span data-ttu-id="83a08-105">_**最終更新日:** 2012-05-25_</span><span class="sxs-lookup"><span data-stu-id="83a08-105">_**Topic Last Modified:** 2012-05-25_</span></span>

<span data-ttu-id="83a08-106">ConfereneUris テーブルは、データベースに記録された会議セッションに参加しているさまざまな会議の Uri のリストを格納するサポートテーブルです。</span><span class="sxs-lookup"><span data-stu-id="83a08-106">The ConfereneUris table is a supporting table that stores a list of the various conference URIs that have participated in conference sessions recorded in the database.</span></span> <span data-ttu-id="83a08-107">テーブル内の各レコードは、1つの会議 URI を表します。</span><span class="sxs-lookup"><span data-stu-id="83a08-107">Each record in the table represents one conference URI.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="83a08-108">列</span><span class="sxs-lookup"><span data-stu-id="83a08-108">Column</span></span></th>
<th><span data-ttu-id="83a08-109">データ型</span><span class="sxs-lookup"><span data-stu-id="83a08-109">Data Type</span></span></th>
<th><span data-ttu-id="83a08-110">キー/インデックス</span><span class="sxs-lookup"><span data-stu-id="83a08-110">Key/Index</span></span></th>
<th><span data-ttu-id="83a08-111">詳細</span><span class="sxs-lookup"><span data-stu-id="83a08-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="83a08-112"><strong>Nextupdatupdat</strong></span><span class="sxs-lookup"><span data-stu-id="83a08-112"><strong>NextUpdateTS</strong></span></span></p></td>
<td><p><span data-ttu-id="83a08-113">datetime</span><span class="sxs-lookup"><span data-stu-id="83a08-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="83a08-114">Primary</span><span class="sxs-lookup"><span data-stu-id="83a08-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="83a08-115">タイムスタンプ、内部使用。</span><span class="sxs-lookup"><span data-stu-id="83a08-115">Time stamp, Internal used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83a08-116"><strong>ConferenceUriId</strong></span><span class="sxs-lookup"><span data-stu-id="83a08-116"><strong>ConferenceUriId</strong></span></span></p></td>
<td><p><span data-ttu-id="83a08-117">int</span><span class="sxs-lookup"><span data-stu-id="83a08-117">int</span></span></p></td>
<td><p><span data-ttu-id="83a08-118">Primary</span><span class="sxs-lookup"><span data-stu-id="83a08-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="83a08-119">この会議 URI を識別する一意の番号です。</span><span class="sxs-lookup"><span data-stu-id="83a08-119">Unique number identifying this conference URI.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83a08-120"><strong>ConferenceUri</strong></span><span class="sxs-lookup"><span data-stu-id="83a08-120"><strong>ConferenceUri</strong></span></span></p></td>
<td><p><span data-ttu-id="83a08-121">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="83a08-121">nvarchar(450)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="83a08-122">会議の URI。</span><span class="sxs-lookup"><span data-stu-id="83a08-122">Conference URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83a08-123"><strong>サム</strong></span><span class="sxs-lookup"><span data-stu-id="83a08-123"><strong>Checksum</strong></span></span></p></td>
<td><p><span data-ttu-id="83a08-124">int</span><span class="sxs-lookup"><span data-stu-id="83a08-124">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="83a08-125">ConferenceUri のチェックサム。</span><span class="sxs-lookup"><span data-stu-id="83a08-125">Checksum of ConferenceUri.</span></span> <span data-ttu-id="83a08-126">データベースの検索速度を上げるために使われます。</span><span class="sxs-lookup"><span data-stu-id="83a08-126">Used to increases the speed of database searches.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83a08-127"><strong>UriTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="83a08-127"><strong>UriTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="83a08-128">int</span><span class="sxs-lookup"><span data-stu-id="83a08-128">int</span></span></p></td>
<td><p><span data-ttu-id="83a08-129">外部</span><span class="sxs-lookup"><span data-stu-id="83a08-129">Foreign</span></span></p></td>
<td><p><span data-ttu-id="83a08-130">URI の種類 ("conf: IM 会議用チャット" または "conf: 音声/ビデオ会議用のオーディオビデオ" など)。</span><span class="sxs-lookup"><span data-stu-id="83a08-130">URI type, such as conf:chat for IM conference, or conf:audio-video for audio/video conference.</span></span> <span data-ttu-id="83a08-131">詳細については、「 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 テーブルの UriTypes テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="83a08-131">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> table for more information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="83a08-132">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="83a08-132">


</div>

<span> </span>

</div>

</div>

</span></span></div>

