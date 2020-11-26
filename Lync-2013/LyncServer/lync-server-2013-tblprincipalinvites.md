---
title: 'Lync Server 2013: tblPrincipalInvites'
description: 'Lync Server 2013: tblPrincipalInvites'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalInvites
ms:assetid: 548ec156-4d1a-469d-a804-62cff226e5c2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558650(v=OCS.15)
ms:contentKeyID: 48184141
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d30d741864ed2a3cfbec8329215be33c21b3b262
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423506"
---
# <a name="tblprincipalinvites-in-lync-server-2013"></a><span data-ttu-id="5c808-103">Lync Server 2013 の tblPrincipalInvites</span><span class="sxs-lookup"><span data-stu-id="5c808-103">tblPrincipalInvites in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5c808-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5c808-104">

<span> </span></span></span>

<span data-ttu-id="5c808-105">_**最終更新日:** 2012-06-25_</span><span class="sxs-lookup"><span data-stu-id="5c808-105">_**Topic Last Modified:** 2012-06-25_</span></span>

<span data-ttu-id="5c808-106">tblPrincipalInvites には、自動招待を含むすべてのノードのプロビジョニングされたすべてのユーザーの招待が含まれます。</span><span class="sxs-lookup"><span data-stu-id="5c808-106">tblPrincipalInvites contains invitations for all provisioned users for all nodes with auto-invite on.</span></span>

### <a name="columns"></a><span data-ttu-id="5c808-107">行</span><span class="sxs-lookup"><span data-stu-id="5c808-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5c808-108">列</span><span class="sxs-lookup"><span data-stu-id="5c808-108">Column</span></span></th>
<th><span data-ttu-id="5c808-109">型</span><span class="sxs-lookup"><span data-stu-id="5c808-109">Type</span></span></th>
<th><span data-ttu-id="5c808-110">説明</span><span class="sxs-lookup"><span data-stu-id="5c808-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5c808-111">prinID</span><span class="sxs-lookup"><span data-stu-id="5c808-111">prinID</span></span></p></td>
<td><p><span data-ttu-id="5c808-112">int (null ではない)</span><span class="sxs-lookup"><span data-stu-id="5c808-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="5c808-113">プリンシパル ID。</span><span class="sxs-lookup"><span data-stu-id="5c808-113">Principal ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c808-114">invID</span><span class="sxs-lookup"><span data-stu-id="5c808-114">invID</span></span></p></td>
<td><p><span data-ttu-id="5c808-115">int (null ではない)</span><span class="sxs-lookup"><span data-stu-id="5c808-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="5c808-116">TblLastInviteId テーブルから生成された一意の連続番号 (プリンシパル ID ごと)。</span><span class="sxs-lookup"><span data-stu-id="5c808-116">Unique sequential number (per principal ID) generated from tblLastInviteId table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c808-117">nodeID</span><span class="sxs-lookup"><span data-stu-id="5c808-117">nodeID</span></span></p></td>
<td><p><span data-ttu-id="5c808-118">int (null ではない)</span><span class="sxs-lookup"><span data-stu-id="5c808-118">int, not null</span></span></p></td>
<td><p><span data-ttu-id="5c808-119">ノード ID (チャットルームのみ)。</span><span class="sxs-lookup"><span data-stu-id="5c808-119">Node ID (chat room only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c808-120">createdOn</span><span class="sxs-lookup"><span data-stu-id="5c808-120">createdOn</span></span></p></td>
<td><p><span data-ttu-id="5c808-121">datetime。 null ではありません</span><span class="sxs-lookup"><span data-stu-id="5c808-121">datetime, not null</span></span></p></td>
<td><p><span data-ttu-id="5c808-122">作成時刻。</span><span class="sxs-lookup"><span data-stu-id="5c808-122">Time of creation.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="5c808-123">機能</span><span class="sxs-lookup"><span data-stu-id="5c808-123">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5c808-124">列</span><span class="sxs-lookup"><span data-stu-id="5c808-124">Column</span></span></th>
<th><span data-ttu-id="5c808-125">説明</span><span class="sxs-lookup"><span data-stu-id="5c808-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5c808-126">&lt;prinID、nodeID&gt;</span><span class="sxs-lookup"><span data-stu-id="5c808-126">&lt;prinID, nodeID&gt;</span></span></p></td>
<td><p><span data-ttu-id="5c808-127">主キー。</span><span class="sxs-lookup"><span data-stu-id="5c808-127">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c808-128">prinID</span><span class="sxs-lookup"><span data-stu-id="5c808-128">prinID</span></span></p></td>
<td><p><span data-ttu-id="5c808-129">TblPrincipal Id テーブルで参照される外部キー。</span><span class="sxs-lookup"><span data-stu-id="5c808-129">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c808-130">nodeID</span><span class="sxs-lookup"><span data-stu-id="5c808-130">nodeID</span></span></p></td>
<td><p><span data-ttu-id="5c808-131">TblNode テーブルで参照される外部キー。</span><span class="sxs-lookup"><span data-stu-id="5c808-131">Foreign key with lookup in tblNode.nodeID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="5c808-132">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5c808-132">


</div>

<span> </span>

</div>

</div>

</span></span></div>

