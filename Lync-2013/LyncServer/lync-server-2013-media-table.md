---
title: 'Lync Server 2013: Media テーブル'
description: 'Lync Server 2013: メディアテーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Media table
ms:assetid: 1e1b427f-59b5-4564-bde5-1002a80439ee
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398268(v=OCS.15)
ms:contentKeyID: 48183568
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 31e30d1f91c59b8e3aa7915fc0d513618d0f709f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425676"
---
# <a name="media-table-in-lync-server-2013"></a><span data-ttu-id="986d9-103">Lync Server 2013 の Media テーブル</span><span class="sxs-lookup"><span data-stu-id="986d9-103">Media table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="986d9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="986d9-104">

<span> </span></span></span>

<span data-ttu-id="986d9-105">_**最終更新日:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="986d9-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="986d9-106">各レコードは、ピアツーピアセッションで使用される1つのメディアの種類を表します。</span><span class="sxs-lookup"><span data-stu-id="986d9-106">Each record represents one media type used in a peer-to-peer session.</span></span> <span data-ttu-id="986d9-107">複数のメディアの種類を使用している場合は、1つのセッションがテーブル内の複数のレコードで表されます。</span><span class="sxs-lookup"><span data-stu-id="986d9-107">One session would be represented by multiple records in the table, if more than one media type is used.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="986d9-108">メディアテーブルを使って、セッションのメディアの再生時間を計算することはできません。</span><span class="sxs-lookup"><span data-stu-id="986d9-108">The Media table should not be used to calculate the media duration for a session.</span></span> <span data-ttu-id="986d9-109">この表には、セッションでのメディア交換の信号の詳細が含まれています。</span><span class="sxs-lookup"><span data-stu-id="986d9-109">This table contains the signaling details of media exchange in a session.</span></span> <span data-ttu-id="986d9-110">メディア交換は INVITE 要求によって実行され、StartTime は招待が送信された時間を示します。この招待は、セッションの開始時刻を意味するわけではありません。これは、セッションを開始した後にのみメディアが開始されるためです。</span><span class="sxs-lookup"><span data-stu-id="986d9-110">Media exchange is done by the INVITE request, and StartTime indicates the time that the INVITE was sent out. The invite time does not necessarily mean the media start time, because media starts only after the sessionee accepts the session.</span></span> <span data-ttu-id="986d9-111">通常、EndTime はこのセッションの終了時刻を示します。</span><span class="sxs-lookup"><span data-stu-id="986d9-111">The EndTime usually means the end time of this session.</span></span>



</div>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="986d9-112">列</span><span class="sxs-lookup"><span data-stu-id="986d9-112">Column</span></span></th>
<th><span data-ttu-id="986d9-113">データ型</span><span class="sxs-lookup"><span data-stu-id="986d9-113">Data Type</span></span></th>
<th><span data-ttu-id="986d9-114">キー/インデックス</span><span class="sxs-lookup"><span data-stu-id="986d9-114">Key/Index</span></span></th>
<th><span data-ttu-id="986d9-115">詳細</span><span class="sxs-lookup"><span data-stu-id="986d9-115">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="986d9-116"><strong>セッション Id</strong></span><span class="sxs-lookup"><span data-stu-id="986d9-116"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="986d9-117">datetime</span><span class="sxs-lookup"><span data-stu-id="986d9-117">datetime</span></span></p></td>
<td><p><span data-ttu-id="986d9-118">プライマリ、外部</span><span class="sxs-lookup"><span data-stu-id="986d9-118">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="986d9-119">セッション要求の時刻。</span><span class="sxs-lookup"><span data-stu-id="986d9-119">Time of session request.</span></span> <span data-ttu-id="986d9-120">セッションを一意に識別するために <strong>Sessionidseq</strong> と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="986d9-120">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="986d9-121">詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="986d9-121">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="986d9-122"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="986d9-122"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="986d9-123">int</span><span class="sxs-lookup"><span data-stu-id="986d9-123">int</span></span></p></td>
<td><p><span data-ttu-id="986d9-124">プライマリ、外部</span><span class="sxs-lookup"><span data-stu-id="986d9-124">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="986d9-125">セッションを識別する ID 番号。</span><span class="sxs-lookup"><span data-stu-id="986d9-125">ID number to identify the session.</span></span> <span data-ttu-id="986d9-126">セッションを一意に識別するために <strong>Sessionidtime</strong> と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="986d9-126">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="986d9-127">詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="986d9-127">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="986d9-128"><strong>MediaId</strong></span><span class="sxs-lookup"><span data-stu-id="986d9-128"><strong>MediaId</strong></span></span></p></td>
<td><p><span data-ttu-id="986d9-129">tinyint</span><span class="sxs-lookup"><span data-stu-id="986d9-129">tinyint</span></span></p></td>
<td><p><span data-ttu-id="986d9-130">プライマリ、外部</span><span class="sxs-lookup"><span data-stu-id="986d9-130">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="986d9-131">このメディアの種類を識別する一意の番号です。</span><span class="sxs-lookup"><span data-stu-id="986d9-131">Unique number identifying this media type.</span></span> <span data-ttu-id="986d9-132">詳細については、「 <a href="lync-server-2013-medialist-table.md">Lync Server 2013 の Medialist の表</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="986d9-132">See the <a href="lync-server-2013-medialist-table.md">MediaList table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="986d9-133"><strong>StartTime</strong></span><span class="sxs-lookup"><span data-stu-id="986d9-133"><strong>StartTime</strong></span></span></p></td>
<td><p><span data-ttu-id="986d9-134">datetime</span><span class="sxs-lookup"><span data-stu-id="986d9-134">datetime</span></span></p></td>
<td><p><span data-ttu-id="986d9-135">Primary</span><span class="sxs-lookup"><span data-stu-id="986d9-135">Primary</span></span></p></td>
<td><p><span data-ttu-id="986d9-136">これは、実際のメディアの開始時刻ではなく、メディア要求が送信された時刻です。</span><span class="sxs-lookup"><span data-stu-id="986d9-136">This is the time that a media request was sent out, not the real media start time.</span></span> <span data-ttu-id="986d9-137"><strong>StartTime</strong> には、セッションのセットアップ時間が含まれます。</span><span class="sxs-lookup"><span data-stu-id="986d9-137"><strong>StartTime</strong> includes the session setup time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="986d9-138"><strong>EndTime</strong></span><span class="sxs-lookup"><span data-stu-id="986d9-138"><strong>EndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="986d9-139">datetime</span><span class="sxs-lookup"><span data-stu-id="986d9-139">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="986d9-140">これはセッションの終了時刻です。</span><span class="sxs-lookup"><span data-stu-id="986d9-140">This is the end time of the session.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="986d9-141">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="986d9-141">


</div>

<span> </span>

</div>

</div>

</span></span></div>

