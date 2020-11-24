---
title: 'Lync Server 2013: tblPrincipalMeta'
description: 'Lync Server 2013: tblPrincipalMeta'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalMeta
ms:assetid: 808490d4-7d6d-47a2-b8af-b5940d47073b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615009(v=OCS.15)
ms:contentKeyID: 48184648
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 899fd1e450dac52afa56c1ee1de86da82b2db309
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398108"
---
# <a name="tblprincipalmeta-in-lync-server-2013"></a><span data-ttu-id="5c4ef-103">Lync Server 2013 の tblPrincipalMeta</span><span class="sxs-lookup"><span data-stu-id="5c4ef-103">tblPrincipalMeta in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5c4ef-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5c4ef-104">

<span> </span></span></span>

<span data-ttu-id="5c4ef-105">_**最終更新日:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="5c4ef-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="5c4ef-106">tblPrincipalMeta には、Active Directory ドメインサービスから更新する必要があるプリンシパルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="5c4ef-106">tblPrincipalMeta contains the principals that have to be refreshed from Active Directory Domain Services.</span></span>

### <a name="columns"></a><span data-ttu-id="5c4ef-107">行</span><span class="sxs-lookup"><span data-stu-id="5c4ef-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5c4ef-108">列</span><span class="sxs-lookup"><span data-stu-id="5c4ef-108">Column</span></span></th>
<th><span data-ttu-id="5c4ef-109">型</span><span class="sxs-lookup"><span data-stu-id="5c4ef-109">Type</span></span></th>
<th><span data-ttu-id="5c4ef-110">説明</span><span class="sxs-lookup"><span data-stu-id="5c4ef-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5c4ef-111">prinID</span><span class="sxs-lookup"><span data-stu-id="5c4ef-111">prinID</span></span></p></td>
<td><p><span data-ttu-id="5c4ef-112">int (null ではない)</span><span class="sxs-lookup"><span data-stu-id="5c4ef-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="5c4ef-113">プリンシパル ID。</span><span class="sxs-lookup"><span data-stu-id="5c4ef-113">Principal ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c4ef-114">prinAffiliationsDirty</span><span class="sxs-lookup"><span data-stu-id="5c4ef-114">prinAffiliationsDirty</span></span></p></td>
<td><p><span data-ttu-id="5c4ef-115">ビット、null ではない</span><span class="sxs-lookup"><span data-stu-id="5c4ef-115">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="5c4ef-116">プリンシパルの所属を更新する必要がある場合は True。</span><span class="sxs-lookup"><span data-stu-id="5c4ef-116">True if principal affiliations have to be refreshed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c4ef-117">Prin属性のダーティ</span><span class="sxs-lookup"><span data-stu-id="5c4ef-117">prinAttributesDirty</span></span></p></td>
<td><p><span data-ttu-id="5c4ef-118">ビット、null ではない</span><span class="sxs-lookup"><span data-stu-id="5c4ef-118">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="5c4ef-119">プリンシパル属性を更新する必要がある場合は True。</span><span class="sxs-lookup"><span data-stu-id="5c4ef-119">True if principal attributes have to be refreshed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c4ef-120">プリントが削除されました</span><span class="sxs-lookup"><span data-stu-id="5c4ef-120">prinDeleted</span></span></p></td>
<td><p><span data-ttu-id="5c4ef-121">ビット、null ではない</span><span class="sxs-lookup"><span data-stu-id="5c4ef-121">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="5c4ef-122">プリンシパルが削除された場合は True。</span><span class="sxs-lookup"><span data-stu-id="5c4ef-122">True if the principal has been deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c4ef-123">tryCount</span><span class="sxs-lookup"><span data-stu-id="5c4ef-123">tryCount</span></span></p></td>
<td><p><span data-ttu-id="5c4ef-124">int</span><span class="sxs-lookup"><span data-stu-id="5c4ef-124">int</span></span></p></td>
<td><p><span data-ttu-id="5c4ef-125">これまでに発生した、AD DS からプリンシパルを更新しようとした回数。</span><span class="sxs-lookup"><span data-stu-id="5c4ef-125">Number of attempts to refresh the principal from AD DS that have happened so far.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c4ef-126">最終試用</span><span class="sxs-lookup"><span data-stu-id="5c4ef-126">lastTry</span></span></p></td>
<td><p><span data-ttu-id="5c4ef-127">datetime</span><span class="sxs-lookup"><span data-stu-id="5c4ef-127">datetime</span></span></p></td>
<td><p><span data-ttu-id="5c4ef-128">プリンシパルを最新の状態に更新しようとしたときのタイムスタンプ。</span><span class="sxs-lookup"><span data-stu-id="5c4ef-128">Time stamp from the latest attempt to refresh the principal.</span></span> <span data-ttu-id="5c4ef-129">更新をまだ実行していない場合は、null を指定できます。</span><span class="sxs-lookup"><span data-stu-id="5c4ef-129">Can be null if no refresh has been attempted yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c4ef-130">nextTry</span><span class="sxs-lookup"><span data-stu-id="5c4ef-130">nextTry</span></span></p></td>
<td><p><span data-ttu-id="5c4ef-131">datetime</span><span class="sxs-lookup"><span data-stu-id="5c4ef-131">datetime</span></span></p></td>
<td><p><span data-ttu-id="5c4ef-132">スケジュールされている次回の更新のタイムスタンプ。</span><span class="sxs-lookup"><span data-stu-id="5c4ef-132">Time stamp for the next scheduled refresh.</span></span> <span data-ttu-id="5c4ef-133">それ以降の更新がスケジュールされていない場合は、null を指定できます。</span><span class="sxs-lookup"><span data-stu-id="5c4ef-133">Can be null if no further refresh has been scheduled.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="5c4ef-134">機能</span><span class="sxs-lookup"><span data-stu-id="5c4ef-134">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5c4ef-135">列</span><span class="sxs-lookup"><span data-stu-id="5c4ef-135">Column</span></span></th>
<th><span data-ttu-id="5c4ef-136">説明</span><span class="sxs-lookup"><span data-stu-id="5c4ef-136">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5c4ef-137">prinID</span><span class="sxs-lookup"><span data-stu-id="5c4ef-137">prinID</span></span></p></td>
<td><p><span data-ttu-id="5c4ef-138">主キー。</span><span class="sxs-lookup"><span data-stu-id="5c4ef-138">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c4ef-139">prinID</span><span class="sxs-lookup"><span data-stu-id="5c4ef-139">prinID</span></span></p></td>
<td><p><span data-ttu-id="5c4ef-140">TblPrincipal Id テーブルで参照される外部キー。</span><span class="sxs-lookup"><span data-stu-id="5c4ef-140">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="5c4ef-141">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5c4ef-141">


</div>

<span> </span>

</div>

</div>

</span></span></div>

