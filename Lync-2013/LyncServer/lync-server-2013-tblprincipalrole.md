---
title: 'Lync Server 2013: tblPrincipalRole'
description: 'Lync Server 2013: tblPrincipalRole'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalRole
ms:assetid: dcd16dc1-a66c-4720-a48f-ec8b28337383
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615039(v=OCS.15)
ms:contentKeyID: 48185597
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f58ffda3136c254ee77f14d33dcb42af5d172c4a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398085"
---
# <a name="tblprincipalrole-in-lync-server-2013"></a><span data-ttu-id="9f4a2-103">Lync Server 2013 の tblPrincipalRole</span><span class="sxs-lookup"><span data-stu-id="9f4a2-103">tblPrincipalRole in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9f4a2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9f4a2-104">

<span> </span></span></span>

<span data-ttu-id="9f4a2-105">_**最終更新日:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="9f4a2-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="9f4a2-106">tblPrincipalRole には、ノードに割り当てられている明示的な役割が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9f4a2-106">tblPrincipalRole contains explicit roles assigned to nodes.</span></span>

### <a name="columns"></a><span data-ttu-id="9f4a2-107">行</span><span class="sxs-lookup"><span data-stu-id="9f4a2-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9f4a2-108">列</span><span class="sxs-lookup"><span data-stu-id="9f4a2-108">Column</span></span></th>
<th><span data-ttu-id="9f4a2-109">型</span><span class="sxs-lookup"><span data-stu-id="9f4a2-109">Type</span></span></th>
<th><span data-ttu-id="9f4a2-110">説明</span><span class="sxs-lookup"><span data-stu-id="9f4a2-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9f4a2-111">Prinrolid</span><span class="sxs-lookup"><span data-stu-id="9f4a2-111">prinRoleNodeID</span></span></p></td>
<td><p><span data-ttu-id="9f4a2-112">int (null ではない)</span><span class="sxs-lookup"><span data-stu-id="9f4a2-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="9f4a2-113">役割が適用されるノード ID。</span><span class="sxs-lookup"><span data-stu-id="9f4a2-113">Node ID that the role applies to.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f4a2-114">prinRolePrinID</span><span class="sxs-lookup"><span data-stu-id="9f4a2-114">prinRolePrinID</span></span></p></td>
<td><p><span data-ttu-id="9f4a2-115">int (null ではない)</span><span class="sxs-lookup"><span data-stu-id="9f4a2-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="9f4a2-116">プリンシパル ID。</span><span class="sxs-lookup"><span data-stu-id="9f4a2-116">Principal ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f4a2-117">prinRoleTypeID</span><span class="sxs-lookup"><span data-stu-id="9f4a2-117">prinRoleTypeID</span></span></p></td>
<td><p><span data-ttu-id="9f4a2-118">int (null ではない)</span><span class="sxs-lookup"><span data-stu-id="9f4a2-118">int, not null</span></span></p></td>
<td><p><span data-ttu-id="9f4a2-119">役割の種類の ID (tblRoleType から)。</span><span class="sxs-lookup"><span data-stu-id="9f4a2-119">Role type ID (from tblRoleType).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f4a2-120">prinroleupdat</span><span class="sxs-lookup"><span data-stu-id="9f4a2-120">prinRoleUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="9f4a2-121">int (null ではない)</span><span class="sxs-lookup"><span data-stu-id="9f4a2-121">int, not null</span></span></p></td>
<td><p><span data-ttu-id="9f4a2-122">このエントリを最後に更新したプリンシパルの ID です。</span><span class="sxs-lookup"><span data-stu-id="9f4a2-122">ID of the principal that last updated this entry.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="9f4a2-123">機能</span><span class="sxs-lookup"><span data-stu-id="9f4a2-123">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9f4a2-124">列</span><span class="sxs-lookup"><span data-stu-id="9f4a2-124">Column</span></span></th>
<th><span data-ttu-id="9f4a2-125">説明</span><span class="sxs-lookup"><span data-stu-id="9f4a2-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9f4a2-126">&lt;Prinroldeid、prinRolePrinID、prinRoleTypeID&gt;</span><span class="sxs-lookup"><span data-stu-id="9f4a2-126">&lt;prinRoleNodeID, prinRolePrinID, prinRoleTypeID&gt;</span></span></p></td>
<td><p><span data-ttu-id="9f4a2-127">主キー。</span><span class="sxs-lookup"><span data-stu-id="9f4a2-127">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f4a2-128">Prinrolid</span><span class="sxs-lookup"><span data-stu-id="9f4a2-128">prinRoleNodeID</span></span></p></td>
<td><p><span data-ttu-id="9f4a2-129">TblNode テーブルで参照される外部キー。</span><span class="sxs-lookup"><span data-stu-id="9f4a2-129">Foreign key with lookup in tblNode.nodeID table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f4a2-130">prinRolePrinID</span><span class="sxs-lookup"><span data-stu-id="9f4a2-130">prinRolePrinID</span></span></p></td>
<td><p><span data-ttu-id="9f4a2-131">TblPrincipal Id テーブルで参照される外部キー。</span><span class="sxs-lookup"><span data-stu-id="9f4a2-131">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f4a2-132">prinRoleTypeID</span><span class="sxs-lookup"><span data-stu-id="9f4a2-132">prinRoleTypeID</span></span></p></td>
<td><p><span data-ttu-id="9f4a2-133">TblRoleType の Typeid テーブルで参照される外部キー。</span><span class="sxs-lookup"><span data-stu-id="9f4a2-133">Foreign key with lookup in tblRoleType.rtypeID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="9f4a2-134">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9f4a2-134">


</div>

<span> </span>

</div>

</div>

</span></span></div>

