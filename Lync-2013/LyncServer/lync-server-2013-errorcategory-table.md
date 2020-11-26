---
title: 'Lync Server 2013: ErrorCategory テーブル'
description: 'Lync Server 2013: ErrorCategory テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ErrorCategory table
ms:assetid: 0fde3b73-9a2f-44dd-b8dc-6df512303ff1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204675(v=OCS.15)
ms:contentKeyID: 48183425
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8154c73f33b5dad62a338335a960553cfc06ec13
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428567"
---
# <a name="errorcategory-table-in-lync-server-2013"></a><span data-ttu-id="4bd72-103">Lync Server 2013 の ErrorCategory テーブル</span><span class="sxs-lookup"><span data-stu-id="4bd72-103">ErrorCategory table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4bd72-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4bd72-104">

<span> </span></span></span>

<span data-ttu-id="4bd72-105">_**最終更新日:** 2012-08-20_</span><span class="sxs-lookup"><span data-stu-id="4bd72-105">_**Topic Last Modified:** 2012-08-20_</span></span>

<span data-ttu-id="4bd72-106">ErrorCategory テーブルには、Microsoft Lync Server 2013 診断分類ごとのフレンドリ名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4bd72-106">The ErrorCategory table contains the friendly name for each Microsoft Lync Server 2013 diagnostic classification.</span></span> <span data-ttu-id="4bd72-107">既定では、Lync Server 2013 には次のような分類が使用されます。</span><span class="sxs-lookup"><span data-stu-id="4bd72-107">By default, Lync Server 2013 uses the following classifications:</span></span>

  - <span data-ttu-id="4bd72-108">0--成功</span><span class="sxs-lookup"><span data-stu-id="4bd72-108">0 -- Success</span></span>

  - <span data-ttu-id="4bd72-109">1--予期しないエラー</span><span class="sxs-lookup"><span data-stu-id="4bd72-109">1 -- Expected failure</span></span>

  - <span data-ttu-id="4bd72-110">2-予期しないエラー</span><span class="sxs-lookup"><span data-stu-id="4bd72-110">2 – Unexpected failure</span></span>

<span data-ttu-id="4bd72-111">この表は、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="4bd72-111">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4bd72-112">列</span><span class="sxs-lookup"><span data-stu-id="4bd72-112">Column</span></span></th>
<th><span data-ttu-id="4bd72-113">データ型</span><span class="sxs-lookup"><span data-stu-id="4bd72-113">Data Type</span></span></th>
<th><span data-ttu-id="4bd72-114">キー/インデックス</span><span class="sxs-lookup"><span data-stu-id="4bd72-114">Key/Index</span></span></th>
<th><span data-ttu-id="4bd72-115">詳細</span><span class="sxs-lookup"><span data-stu-id="4bd72-115">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4bd72-116"><strong>区分</strong></span><span class="sxs-lookup"><span data-stu-id="4bd72-116"><strong>CategoryId</strong></span></span></p></td>
<td><p><span data-ttu-id="4bd72-117">tinyint</span><span class="sxs-lookup"><span data-stu-id="4bd72-117">tinyint</span></span></p></td>
<td><p><span data-ttu-id="4bd72-118">Primary</span><span class="sxs-lookup"><span data-stu-id="4bd72-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="4bd72-119">分類の一意の識別子。</span><span class="sxs-lookup"><span data-stu-id="4bd72-119">Unique identifier for the classification.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bd72-120"><strong>名前</strong></span><span class="sxs-lookup"><span data-stu-id="4bd72-120"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="4bd72-121">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="4bd72-121">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="4bd72-122">分類に割り当てられている値とフレンドリ名。</span><span class="sxs-lookup"><span data-stu-id="4bd72-122">Value and friendly name assigned to the classification.</span></span> <span data-ttu-id="4bd72-123">有効な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="4bd72-123">Allowed values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="4bd72-124">0--成功</span><span class="sxs-lookup"><span data-stu-id="4bd72-124">0 -- Success</span></span></p></li>
<li><p><span data-ttu-id="4bd72-125">1--予期しないエラー</span><span class="sxs-lookup"><span data-stu-id="4bd72-125">1 -- Expected failure</span></span></p></li>
<li><p><span data-ttu-id="4bd72-126">2-予期しないエラー</span><span class="sxs-lookup"><span data-stu-id="4bd72-126">2 – Unexpected failure</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="4bd72-127">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4bd72-127">


</div>

<span> </span>

</div>

</div>

</span></span></div>

