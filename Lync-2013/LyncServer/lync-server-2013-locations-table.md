---
title: 'Lync Server 2013: Locations テーブル'
description: 'Lync Server 2013: 場所テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Locations table
ms:assetid: 78dc1b14-5394-4f8e-89d3-4ba593272a04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398596(v=OCS.15)
ms:contentKeyID: 48184579
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9d07b6d3d3820f4efb3310adf0734a7e10c53e6d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399831"
---
# <a name="locations-table-in-lync-server-2013"></a><span data-ttu-id="1a44a-103">Lync Server 2013 の Locations テーブル</span><span class="sxs-lookup"><span data-stu-id="1a44a-103">Locations table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1a44a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1a44a-104">

<span> </span></span></span>

<span data-ttu-id="1a44a-105">_**最終更新日:** 2012-05-25_</span><span class="sxs-lookup"><span data-stu-id="1a44a-105">_**Topic Last Modified:** 2012-05-25_</span></span>

<span data-ttu-id="1a44a-106">各レコードは、E9 通話のような緊急通話での1つの場所参照を表します。</span><span class="sxs-lookup"><span data-stu-id="1a44a-106">Each record represents one location reference in an emergency call, like an E9-1-1 call.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1a44a-107">列</span><span class="sxs-lookup"><span data-stu-id="1a44a-107">Column</span></span></th>
<th><span data-ttu-id="1a44a-108">データ型</span><span class="sxs-lookup"><span data-stu-id="1a44a-108">Data Type</span></span></th>
<th><span data-ttu-id="1a44a-109">キー/インデックス</span><span class="sxs-lookup"><span data-stu-id="1a44a-109">Key/Index</span></span></th>
<th><span data-ttu-id="1a44a-110">詳細</span><span class="sxs-lookup"><span data-stu-id="1a44a-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1a44a-111"><strong>セッション Id</strong></span><span class="sxs-lookup"><span data-stu-id="1a44a-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="1a44a-112">datetime</span><span class="sxs-lookup"><span data-stu-id="1a44a-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="1a44a-113">プライマリ、外部</span><span class="sxs-lookup"><span data-stu-id="1a44a-113">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="1a44a-114">セッション要求の時刻。</span><span class="sxs-lookup"><span data-stu-id="1a44a-114">Time of session request.</span></span> <span data-ttu-id="1a44a-115">セッションを一意に識別するために <strong>Sessionidseq</strong> と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="1a44a-115">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="1a44a-116">詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1a44a-116">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a44a-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="1a44a-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="1a44a-118">int</span><span class="sxs-lookup"><span data-stu-id="1a44a-118">int</span></span></p></td>
<td><p><span data-ttu-id="1a44a-119">プライマリ、外部</span><span class="sxs-lookup"><span data-stu-id="1a44a-119">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="1a44a-120">セッションを識別する ID 番号。</span><span class="sxs-lookup"><span data-stu-id="1a44a-120">ID number to identify the session.</span></span> <span data-ttu-id="1a44a-121">セッションを一意に識別するために <strong>Sessionidtime</strong> と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="1a44a-121">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="1a44a-122">詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1a44a-122">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a44a-123"><strong>場所</strong></span><span class="sxs-lookup"><span data-stu-id="1a44a-123"><strong>Location</strong></span></span></p></td>
<td><p><span data-ttu-id="1a44a-124">nvarchar (max)</span><span class="sxs-lookup"><span data-stu-id="1a44a-124">nvarchar(max)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1a44a-125">緊急通話の場所。</span><span class="sxs-lookup"><span data-stu-id="1a44a-125">Location of emergency call.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="1a44a-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1a44a-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

