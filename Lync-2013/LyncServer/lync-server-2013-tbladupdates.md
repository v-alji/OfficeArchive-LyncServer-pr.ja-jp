---
title: 'Lync Server 2013: tblADUpdates'
description: 'Lync Server 2013: tblADUpdates'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblADUpdates
ms:assetid: ba19fa16-4d2d-4635-ac32-f93e09469546
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615033(v=OCS.15)
ms:contentKeyID: 48185227
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7ab4418a10eac283d0f39d09b1c1fe15a32b2e68
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444484"
---
# <a name="tbladupdates-in-lync-server-2013"></a><span data-ttu-id="abe5a-103">Lync Server 2013 の tblADUpdates</span><span class="sxs-lookup"><span data-stu-id="abe5a-103">tblADUpdates in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="abe5a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="abe5a-104">

<span> </span></span></span>

<span data-ttu-id="abe5a-105">_**最終更新日:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="abe5a-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="abe5a-106">tblADUpdates には、以降の Active Directory 同期手順でまだ処理されていない Active Directory ドメインサービスの変更が含まれています。</span><span class="sxs-lookup"><span data-stu-id="abe5a-106">tblADUpdates contains Active Directory Domain Services changes that have not yet been processed by the later Active Directory Sync steps.</span></span>

### <a name="columns"></a><span data-ttu-id="abe5a-107">行</span><span class="sxs-lookup"><span data-stu-id="abe5a-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="abe5a-108">列</span><span class="sxs-lookup"><span data-stu-id="abe5a-108">Column</span></span></th>
<th><span data-ttu-id="abe5a-109">型</span><span class="sxs-lookup"><span data-stu-id="abe5a-109">Type</span></span></th>
<th><span data-ttu-id="abe5a-110">説明</span><span class="sxs-lookup"><span data-stu-id="abe5a-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="abe5a-111">prinGuid</span><span class="sxs-lookup"><span data-stu-id="abe5a-111">prinGuid</span></span></p></td>
<td><p><span data-ttu-id="abe5a-112">GUID、null ではない</span><span class="sxs-lookup"><span data-stu-id="abe5a-112">GUID, not null</span></span></p></td>
<td><p><span data-ttu-id="abe5a-113">変更されたオブジェクトのプリンシパル GUID。</span><span class="sxs-lookup"><span data-stu-id="abe5a-113">Principal GUID of the object that changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abe5a-114">prinADPath</span><span class="sxs-lookup"><span data-stu-id="abe5a-114">prinADPath</span></span></p></td>
<td><p><span data-ttu-id="abe5a-115">nvarchar (384)、null ではない</span><span class="sxs-lookup"><span data-stu-id="abe5a-115">nvarchar (384), not null</span></span></p></td>
<td><p><span data-ttu-id="abe5a-116">オブジェクトの識別名。</span><span class="sxs-lookup"><span data-stu-id="abe5a-116">Distinguished name of the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abe5a-117">Prin属性が変更されました</span><span class="sxs-lookup"><span data-stu-id="abe5a-117">prinAttributesChanged</span></span></p></td>
<td><p><span data-ttu-id="abe5a-118">ビット、null ではない</span><span class="sxs-lookup"><span data-stu-id="abe5a-118">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="abe5a-119">オブジェクトの少なくとも1つの属性が変更された場合は True です。</span><span class="sxs-lookup"><span data-stu-id="abe5a-119">True if at least one attribute of the object changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abe5a-120">prinMembersChanged</span><span class="sxs-lookup"><span data-stu-id="abe5a-120">prinMembersChanged</span></span></p></td>
<td><p><span data-ttu-id="abe5a-121">ビット、null ではない</span><span class="sxs-lookup"><span data-stu-id="abe5a-121">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="abe5a-122">メンバーシップが変更された場合は True です。</span><span class="sxs-lookup"><span data-stu-id="abe5a-122">True if the membership changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abe5a-123">prinAffiliationsChanged</span><span class="sxs-lookup"><span data-stu-id="abe5a-123">prinAffiliationsChanged</span></span></p></td>
<td><p><span data-ttu-id="abe5a-124">ビット、null ではない</span><span class="sxs-lookup"><span data-stu-id="abe5a-124">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="abe5a-125">使用されません。</span><span class="sxs-lookup"><span data-stu-id="abe5a-125">Not used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abe5a-126">プリントが削除されました</span><span class="sxs-lookup"><span data-stu-id="abe5a-126">prinDeleted</span></span></p></td>
<td><p><span data-ttu-id="abe5a-127">ビット、null ではない</span><span class="sxs-lookup"><span data-stu-id="abe5a-127">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="abe5a-128">オブジェクトが削除された場合は True。</span><span class="sxs-lookup"><span data-stu-id="abe5a-128">True if the object was deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abe5a-129">最終更新日</span><span class="sxs-lookup"><span data-stu-id="abe5a-129">lastUpdated</span></span></p></td>
<td><p><span data-ttu-id="abe5a-130">datetime。 null ではありません</span><span class="sxs-lookup"><span data-stu-id="abe5a-130">datetime, not null</span></span></p></td>
<td><p><span data-ttu-id="abe5a-131">行が挿入された時刻のタイムスタンプ。</span><span class="sxs-lookup"><span data-stu-id="abe5a-131">Time stamp of when the row was inserted.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="abe5a-132">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="abe5a-132">


</div>

<span> </span>

</div>

</div>

</span></span></div>

