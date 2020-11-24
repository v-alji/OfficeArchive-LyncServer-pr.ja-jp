---
title: 'Lync Server 2013: tblScopePrincipal'
description: 'Lync Server 2013: tblScopePrincipal'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblScopePrincipal
ms:assetid: 422d6c7f-7ba7-4dd4-bacc-95ace47959ff
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558639(v=OCS.15)
ms:contentKeyID: 48184009
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 63315f8525e5c2f05fe54a0f9ed9e8a97b9e8bce
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398067"
---
# <a name="tblscopeprincipal-in-lync-server-2013"></a><span data-ttu-id="5c77a-103">Lync Server 2013 の tblScopePrincipal</span><span class="sxs-lookup"><span data-stu-id="5c77a-103">tblScopePrincipal in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5c77a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5c77a-104">

<span> </span></span></span>

<span data-ttu-id="5c77a-105">_**最終更新日:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="5c77a-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="5c77a-106">tblScopePrincipal には、ノードに割り当てられたスコープが含まれます。</span><span class="sxs-lookup"><span data-stu-id="5c77a-106">tblScopePrincipal contains scopes assigned to nodes.</span></span>

### <a name="columns"></a><span data-ttu-id="5c77a-107">行</span><span class="sxs-lookup"><span data-stu-id="5c77a-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5c77a-108">列</span><span class="sxs-lookup"><span data-stu-id="5c77a-108">Column</span></span></th>
<th><span data-ttu-id="5c77a-109">型</span><span class="sxs-lookup"><span data-stu-id="5c77a-109">Type</span></span></th>
<th><span data-ttu-id="5c77a-110">説明</span><span class="sxs-lookup"><span data-stu-id="5c77a-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5c77a-111">scopeNodeID</span><span class="sxs-lookup"><span data-stu-id="5c77a-111">scopeNodeID</span></span></p></td>
<td><p><span data-ttu-id="5c77a-112">int (null ではない)</span><span class="sxs-lookup"><span data-stu-id="5c77a-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="5c77a-113">スコープが適用されるノード ID。</span><span class="sxs-lookup"><span data-stu-id="5c77a-113">Node ID that the scope applies to.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c77a-114">scopePrinID</span><span class="sxs-lookup"><span data-stu-id="5c77a-114">scopePrinID</span></span></p></td>
<td><p><span data-ttu-id="5c77a-115">int (null ではない)</span><span class="sxs-lookup"><span data-stu-id="5c77a-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="5c77a-116">プリンシパル ID。</span><span class="sxs-lookup"><span data-stu-id="5c77a-116">Principal ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c77a-117">scopeIsDenied</span><span class="sxs-lookup"><span data-stu-id="5c77a-117">scopeIsDenied</span></span></p></td>
<td><p><span data-ttu-id="5c77a-118">ビット、null ではない</span><span class="sxs-lookup"><span data-stu-id="5c77a-118">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="5c77a-119">スコープの型が拒否された場合は True。許可する場合は False。</span><span class="sxs-lookup"><span data-stu-id="5c77a-119">True if type of scope is Deny; False if Allow.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c77a-120">スコープ</span><span class="sxs-lookup"><span data-stu-id="5c77a-120">scopeUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="5c77a-121">int (null ではない)</span><span class="sxs-lookup"><span data-stu-id="5c77a-121">int, not null</span></span></p></td>
<td><p><span data-ttu-id="5c77a-122">このエントリを最後に更新したプリンシパルの ID です。</span><span class="sxs-lookup"><span data-stu-id="5c77a-122">ID of the principal that last updated this entry.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="5c77a-123">機能</span><span class="sxs-lookup"><span data-stu-id="5c77a-123">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5c77a-124">列</span><span class="sxs-lookup"><span data-stu-id="5c77a-124">Column</span></span></th>
<th><span data-ttu-id="5c77a-125">説明</span><span class="sxs-lookup"><span data-stu-id="5c77a-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5c77a-126">&lt;scopeNodeID、scopePrinID&gt;</span><span class="sxs-lookup"><span data-stu-id="5c77a-126">&lt;scopeNodeID, scopePrinID&gt;</span></span></p></td>
<td><p><span data-ttu-id="5c77a-127">主キー。</span><span class="sxs-lookup"><span data-stu-id="5c77a-127">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c77a-128">scopeNodeID</span><span class="sxs-lookup"><span data-stu-id="5c77a-128">scopeNodeID</span></span></p></td>
<td><p><span data-ttu-id="5c77a-129">TblNode テーブルで参照される外部キー。</span><span class="sxs-lookup"><span data-stu-id="5c77a-129">Foreign key with lookup in tblNode.nodeID table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c77a-130">scopePrinID</span><span class="sxs-lookup"><span data-stu-id="5c77a-130">scopePrinID</span></span></p></td>
<td><p><span data-ttu-id="5c77a-131">TblPrincipal Id テーブルで参照される外部キー。</span><span class="sxs-lookup"><span data-stu-id="5c77a-131">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="5c77a-132">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5c77a-132">


</div>

<span> </span>

</div>

</div>

</span></span></div>

