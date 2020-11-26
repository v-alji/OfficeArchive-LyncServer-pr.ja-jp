---
title: 'Lync Server 2013: UserAgent テーブル'
description: 'Lync Server 2013: UserAgent テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: UserAgent table
ms:assetid: d6bda1c0-b053-457a-9ffa-2ae859788775
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398939(v=OCS.15)
ms:contentKeyID: 48185582
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b701d8384313d0267dd566e0c32242f6cc077472
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439129"
---
# <a name="useragent-table-in-lync-server-2013"></a><span data-ttu-id="9116d-103">Lync Server 2013 の UserAgent テーブル</span><span class="sxs-lookup"><span data-stu-id="9116d-103">UserAgent table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9116d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9116d-104">

<span> </span></span></span>

<span data-ttu-id="9116d-105">_**最終更新日:** 2012-05-25_</span><span class="sxs-lookup"><span data-stu-id="9116d-105">_**Topic Last Modified:** 2012-05-25_</span></span>

<span data-ttu-id="9116d-106">UserAgent テーブルは、データベースに記録されているセッションに参加しているさまざまなユーザーエージェントのリストを格納するサポートテーブルです。</span><span class="sxs-lookup"><span data-stu-id="9116d-106">The UserAgent table is a supporting table that stores a list of the various user agents that have participated in sessions recorded in the database.</span></span> <span data-ttu-id="9116d-107">テーブル内の各レコードは、1つのユーザーエージェントを表します。</span><span class="sxs-lookup"><span data-stu-id="9116d-107">Each record in the table represents one user agent</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9116d-108"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="9116d-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="9116d-109"><strong>データ型</strong></span><span class="sxs-lookup"><span data-stu-id="9116d-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="9116d-110"><strong>キー/インデックス</strong></span><span class="sxs-lookup"><span data-stu-id="9116d-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="9116d-111"><strong>詳細</strong></span><span class="sxs-lookup"><span data-stu-id="9116d-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9116d-112"><strong>UserAgentKey</strong></span><span class="sxs-lookup"><span data-stu-id="9116d-112"><strong>UserAgentKey</strong></span></span></p></td>
<td><p><span data-ttu-id="9116d-113">int</span><span class="sxs-lookup"><span data-stu-id="9116d-113">int</span></span></p></td>
<td><p><span data-ttu-id="9116d-114">Primary</span><span class="sxs-lookup"><span data-stu-id="9116d-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="9116d-115">このユーザーエージェントを識別する一意の番号です。</span><span class="sxs-lookup"><span data-stu-id="9116d-115">Unique number identifying this user agent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9116d-116"><strong>UserAgent</strong></span><span class="sxs-lookup"><span data-stu-id="9116d-116"><strong>UserAgent</strong></span></span></p></td>
<td><p><span data-ttu-id="9116d-117">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="9116d-117">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="9116d-118">一意</span><span class="sxs-lookup"><span data-stu-id="9116d-118">Unique</span></span></p></td>
<td><p><span data-ttu-id="9116d-119">ユーザーエージェント文字列。</span><span class="sxs-lookup"><span data-stu-id="9116d-119">User Agent string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9116d-120"><strong>UAType</strong></span><span class="sxs-lookup"><span data-stu-id="9116d-120"><strong>UAType</strong></span></span></p></td>
<td><p><span data-ttu-id="9116d-121">smallint</span><span class="sxs-lookup"><span data-stu-id="9116d-121">smallint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="9116d-122">1は仲介サーバーです。</span><span class="sxs-lookup"><span data-stu-id="9116d-122">1 is Mediation Server.</span></span></p>
<p><span data-ttu-id="9116d-123">2は、A/V 会議サーバーです。</span><span class="sxs-lookup"><span data-stu-id="9116d-123">2 is A/V Conferencing Server.</span></span></p>
<p><span data-ttu-id="9116d-124">4は Lync です。</span><span class="sxs-lookup"><span data-stu-id="9116d-124">4 is Lync.</span></span></p>
<p><span data-ttu-id="9116d-125">8は IP 電話です。</span><span class="sxs-lookup"><span data-stu-id="9116d-125">8 is IP Phone.</span></span></p>
<p><span data-ttu-id="9116d-126">16は Live Meeting 本体です。</span><span class="sxs-lookup"><span data-stu-id="9116d-126">16 is Live Meeting Console.</span></span></p>
<p><span data-ttu-id="9116d-127">32は展開検証ツール (DVT) です。</span><span class="sxs-lookup"><span data-stu-id="9116d-127">32 is Deployment Validation Tool (DVT).</span></span></p>
<p><span data-ttu-id="9116d-128">64は、Macintosh コンピューター上の Lync です。</span><span class="sxs-lookup"><span data-stu-id="9116d-128">64 is Lync on Macintosh computers.</span></span></p>
<p><span data-ttu-id="9116d-129">128は、Office Communications Server 2007 R2 アテンダントです。</span><span class="sxs-lookup"><span data-stu-id="9116d-129">128 is Office Communications Server 2007 R2 Attendant.</span></span></p>
<p><span data-ttu-id="9116d-130">256は会議のアナウンスメントサービスです。</span><span class="sxs-lookup"><span data-stu-id="9116d-130">256 is Conferencing Announcement service.</span></span></p>
<p><span data-ttu-id="9116d-131">512は、会議の自動応答です。</span><span class="sxs-lookup"><span data-stu-id="9116d-131">512 is Conferencing Auto Attendant.</span></span></p>
<p><span data-ttu-id="9116d-132">1024は応答グループアプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="9116d-132">1024 is Response Group application.</span></span></p>
<p><span data-ttu-id="9116d-133">2048は外部の音声制御。</span><span class="sxs-lookup"><span data-stu-id="9116d-133">2048 is Outside Voice Control.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="9116d-134">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9116d-134">


</div>

<span> </span>

</div>

</div>

</span></span></div>

