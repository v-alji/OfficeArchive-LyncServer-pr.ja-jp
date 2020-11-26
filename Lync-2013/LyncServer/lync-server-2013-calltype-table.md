---
title: 'Lync Server 2013: CallType テーブル'
description: 'Lync Server 2013: CallType テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: CallType table
ms:assetid: a1d7187c-f851-4967-88ea-73922911ee7a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412752(v=OCS.15)
ms:contentKeyID: 48185019
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7af9c40396b993893f5157b89bedff0d80d87eb0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435622"
---
# <a name="calltype-table-in-lync-server-2013"></a><span data-ttu-id="3028c-103">Lync Server 2013 の CallType テーブル</span><span class="sxs-lookup"><span data-stu-id="3028c-103">CallType table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3028c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3028c-104">

<span> </span></span></span>

<span data-ttu-id="3028c-105">_**最終更新日:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="3028c-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="3028c-106">CallType テーブルは、可能な呼び出しの種類の一覧を格納する静的テーブルです。</span><span class="sxs-lookup"><span data-stu-id="3028c-106">The CallType table is a static table that stores the list of possible call types.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3028c-107">列</span><span class="sxs-lookup"><span data-stu-id="3028c-107">Column</span></span></th>
<th><span data-ttu-id="3028c-108">データ型</span><span class="sxs-lookup"><span data-stu-id="3028c-108">Data Type</span></span></th>
<th><span data-ttu-id="3028c-109">キー/インデックス</span><span class="sxs-lookup"><span data-stu-id="3028c-109">Key/Index</span></span></th>
<th><span data-ttu-id="3028c-110">詳細</span><span class="sxs-lookup"><span data-stu-id="3028c-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3028c-111"><strong>発信者の Typeid</strong></span><span class="sxs-lookup"><span data-stu-id="3028c-111"><strong>CallTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="3028c-112">int</span><span class="sxs-lookup"><span data-stu-id="3028c-112">int</span></span></p></td>
<td><p><span data-ttu-id="3028c-113">Primary</span><span class="sxs-lookup"><span data-stu-id="3028c-113">Primary</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3028c-114"><strong>CallType</strong></span><span class="sxs-lookup"><span data-stu-id="3028c-114"><strong>CallType</strong></span></span></p></td>
<td><p><span data-ttu-id="3028c-115">nvarchar</span><span class="sxs-lookup"><span data-stu-id="3028c-115">nvarchar</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="3028c-116">許可される値:</span><span class="sxs-lookup"><span data-stu-id="3028c-116">Allowed values:</span></span></p>
<ul>
<li><p><span data-ttu-id="3028c-117">0--不明</span><span class="sxs-lookup"><span data-stu-id="3028c-117">0 -- Unknown</span></span></p></li>
<li><p><span data-ttu-id="3028c-118">1–インスタントメッセージ (im)</span><span class="sxs-lookup"><span data-stu-id="3028c-118">1 – Instant Messaging</span></span></p></li>
<li><p><span data-ttu-id="3028c-119">2--アプリケーション共有</span><span class="sxs-lookup"><span data-stu-id="3028c-119">2 -- Application Sharing</span></span></p></li>
<li><p><span data-ttu-id="3028c-120">3--オーディオ</span><span class="sxs-lookup"><span data-stu-id="3028c-120">3 -- Audio</span></span></p></li>
<li><p><span data-ttu-id="3028c-121">4-オーディオとビデオ</span><span class="sxs-lookup"><span data-stu-id="3028c-121">4 – Audio and Video</span></span></p></li>
<li><p><span data-ttu-id="3028c-122">5-ファイル送信</span><span class="sxs-lookup"><span data-stu-id="3028c-122">5 – File Transfer</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="3028c-123">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3028c-123">


</div>

<span> </span>

</div>

</div>

</span></span></div>

