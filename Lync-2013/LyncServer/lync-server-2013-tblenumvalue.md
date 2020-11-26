---
title: 'Lync Server 2013: tblEnumValue'
description: 'Lync Server 2013: tblEnumValue'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblEnumValue
ms:assetid: a33df20c-d19d-4f5c-b012-29dab8fb9200
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615025(v=OCS.15)
ms:contentKeyID: 48185040
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 159f90bb96c367fcb3e11725a582a9993080d3fd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444449"
---
# <a name="tblenumvalue-in-lync-server-2013"></a><span data-ttu-id="ad4b8-103">Lync Server 2013 の tblEnumValue</span><span class="sxs-lookup"><span data-stu-id="ad4b8-103">tblEnumValue in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ad4b8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ad4b8-104">

<span> </span></span></span>

<span data-ttu-id="ad4b8-105">_**最終更新日:** 2012-06-28_</span><span class="sxs-lookup"><span data-stu-id="ad4b8-105">_**Topic Last Modified:** 2012-06-28_</span></span>

<span data-ttu-id="ad4b8-106">tblEnumValue は、ノードテーブルで使用されている属性の可視性と動作の値を含む、ハードコーディングされた表です。</span><span class="sxs-lookup"><span data-stu-id="ad4b8-106">tblEnumValue is a hardcoded table that contains the Visibility and Behavior values of the attributes that are used in the Node table.</span></span>

### <a name="columns"></a><span data-ttu-id="ad4b8-107">行</span><span class="sxs-lookup"><span data-stu-id="ad4b8-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ad4b8-108">列</span><span class="sxs-lookup"><span data-stu-id="ad4b8-108">Column</span></span></th>
<th><span data-ttu-id="ad4b8-109">型</span><span class="sxs-lookup"><span data-stu-id="ad4b8-109">Type</span></span></th>
<th><span data-ttu-id="ad4b8-110">説明</span><span class="sxs-lookup"><span data-stu-id="ad4b8-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ad4b8-111">valueID</span><span class="sxs-lookup"><span data-stu-id="ad4b8-111">valueID</span></span></p></td>
<td><p><span data-ttu-id="ad4b8-112">smallint (null ではない)</span><span class="sxs-lookup"><span data-stu-id="ad4b8-112">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="ad4b8-113">値の ID です。</span><span class="sxs-lookup"><span data-stu-id="ad4b8-113">ID of the value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad4b8-114">attributeID</span><span class="sxs-lookup"><span data-stu-id="ad4b8-114">attributeID</span></span></p></td>
<td><p><span data-ttu-id="ad4b8-115">smallint (null ではない)</span><span class="sxs-lookup"><span data-stu-id="ad4b8-115">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="ad4b8-116">属性の ID です。</span><span class="sxs-lookup"><span data-stu-id="ad4b8-116">ID of the attribute.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad4b8-117">attributeValue</span><span class="sxs-lookup"><span data-stu-id="ad4b8-117">attributeValue</span></span></p></td>
<td><p><span data-ttu-id="ad4b8-118">nvarchar (256)、null ではない</span><span class="sxs-lookup"><span data-stu-id="ad4b8-118">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="ad4b8-119">値の名前。</span><span class="sxs-lookup"><span data-stu-id="ad4b8-119">Name of the value.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="ad4b8-120">機能</span><span class="sxs-lookup"><span data-stu-id="ad4b8-120">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ad4b8-121">列</span><span class="sxs-lookup"><span data-stu-id="ad4b8-121">Column</span></span></th>
<th><span data-ttu-id="ad4b8-122">説明</span><span class="sxs-lookup"><span data-stu-id="ad4b8-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ad4b8-123">valueID</span><span class="sxs-lookup"><span data-stu-id="ad4b8-123">valueID</span></span></p></td>
<td><p><span data-ttu-id="ad4b8-124">主キー。</span><span class="sxs-lookup"><span data-stu-id="ad4b8-124">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad4b8-125">attributeID</span><span class="sxs-lookup"><span data-stu-id="ad4b8-125">attributeID</span></span></p></td>
<td><p><span data-ttu-id="ad4b8-126">TblEnumAttribute テーブルで参照する外部キー</span><span class="sxs-lookup"><span data-stu-id="ad4b8-126">Foreign key with lookup in tblEnumAttribute.attributeID table.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="table-values"></a><span data-ttu-id="ad4b8-127">テーブルの値</span><span class="sxs-lookup"><span data-stu-id="ad4b8-127">Table Values</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ad4b8-128">valueID</span><span class="sxs-lookup"><span data-stu-id="ad4b8-128">valueID</span></span></th>
<th><span data-ttu-id="ad4b8-129">attributeID</span><span class="sxs-lookup"><span data-stu-id="ad4b8-129">attributeID</span></span></th>
<th><span data-ttu-id="ad4b8-130">attributeValue</span><span class="sxs-lookup"><span data-stu-id="ad4b8-130">attributeValue</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ad4b8-131">2</span><span class="sxs-lookup"><span data-stu-id="ad4b8-131">2</span></span></p></td>
<td><p><span data-ttu-id="ad4b8-132">1</span><span class="sxs-lookup"><span data-stu-id="ad4b8-132">1</span></span></p></td>
<td><p><span data-ttu-id="ad4b8-133">private</span><span class="sxs-lookup"><span data-stu-id="ad4b8-133">private</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad4b8-134">3</span><span class="sxs-lookup"><span data-stu-id="ad4b8-134">3</span></span></p></td>
<td><p><span data-ttu-id="ad4b8-135">1</span><span class="sxs-lookup"><span data-stu-id="ad4b8-135">1</span></span></p></td>
<td><p><span data-ttu-id="ad4b8-136">種類</span><span class="sxs-lookup"><span data-stu-id="ad4b8-136">scope</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad4b8-137">4</span><span class="sxs-lookup"><span data-stu-id="ad4b8-137">4</span></span></p></td>
<td><p><span data-ttu-id="ad4b8-138">2</span><span class="sxs-lookup"><span data-stu-id="ad4b8-138">2</span></span></p></td>
<td><p><span data-ttu-id="ad4b8-139">標準</span><span class="sxs-lookup"><span data-stu-id="ad4b8-139">normal</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad4b8-140">5</span><span class="sxs-lookup"><span data-stu-id="ad4b8-140">5</span></span></p></td>
<td><p><span data-ttu-id="ad4b8-141">2</span><span class="sxs-lookup"><span data-stu-id="ad4b8-141">2</span></span></p></td>
<td><p><span data-ttu-id="ad4b8-142">大</span><span class="sxs-lookup"><span data-stu-id="ad4b8-142">auditorium</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad4b8-143">6</span><span class="sxs-lookup"><span data-stu-id="ad4b8-143">6</span></span></p></td>
<td><p><span data-ttu-id="ad4b8-144">1</span><span class="sxs-lookup"><span data-stu-id="ad4b8-144">1</span></span></p></td>
<td><p><span data-ttu-id="ad4b8-145">開こう</span><span class="sxs-lookup"><span data-stu-id="ad4b8-145">open</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="ad4b8-146">関連項目</span><span class="sxs-lookup"><span data-stu-id="ad4b8-146">See Also</span></span>


[<span data-ttu-id="ad4b8-147">Lync Server 2013 の tblNode</span><span class="sxs-lookup"><span data-stu-id="ad4b8-147">tblNode in Lync Server 2013</span></span>](lync-server-2013-tblnode.md)  
  

<span data-ttu-id="ad4b8-148"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ad4b8-148"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

