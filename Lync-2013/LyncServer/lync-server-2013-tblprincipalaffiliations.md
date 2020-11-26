---
title: 'Lync Server 2013: tblPrincipalAffiliations'
description: 'Lync Server 2013: tblPrincipalAffiliations'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalAffiliations
ms:assetid: 45fd8484-5837-44d2-85bb-45c83546607c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558642(v=OCS.15)
ms:contentKeyID: 48183993
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 01c373147a58300e64f22e60e989a777c59b2653
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441369"
---
# <a name="tblprincipalaffiliations-in-lync-server-2013"></a><span data-ttu-id="fcd1b-103">Lync Server 2013 の tblPrincipalAffiliations</span><span class="sxs-lookup"><span data-stu-id="fcd1b-103">tblPrincipalAffiliations in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fcd1b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fcd1b-104">

<span> </span></span></span>

<span data-ttu-id="fcd1b-105">_**最終更新日:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="fcd1b-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="fcd1b-106">tblPrincipalAffiliations には、active Directory ドメインサービスセキュリティグループなどの場所のメンバーシップを、ドメインの Active Directory コンテナーで説明するプリンシパルの所属が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fcd1b-106">tblPrincipalAffiliations contains the principal affiliations that describe memberships in locations, including Active Directory Domain Services security groups, in Active Directory containers, in domains.</span></span>

### <a name="columns"></a><span data-ttu-id="fcd1b-107">行</span><span class="sxs-lookup"><span data-stu-id="fcd1b-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fcd1b-108">列</span><span class="sxs-lookup"><span data-stu-id="fcd1b-108">Column</span></span></th>
<th><span data-ttu-id="fcd1b-109">型</span><span class="sxs-lookup"><span data-stu-id="fcd1b-109">Type</span></span></th>
<th><span data-ttu-id="fcd1b-110">説明</span><span class="sxs-lookup"><span data-stu-id="fcd1b-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fcd1b-111">principalID</span><span class="sxs-lookup"><span data-stu-id="fcd1b-111">principalID</span></span></p></td>
<td><p><span data-ttu-id="fcd1b-112">int (null ではない)</span><span class="sxs-lookup"><span data-stu-id="fcd1b-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="fcd1b-113">関連主体の ID です。</span><span class="sxs-lookup"><span data-stu-id="fcd1b-113">ID of the affiliated principal.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcd1b-114">affiliationID</span><span class="sxs-lookup"><span data-stu-id="fcd1b-114">affiliationID</span></span></p></td>
<td><p><span data-ttu-id="fcd1b-115">int (null ではない)</span><span class="sxs-lookup"><span data-stu-id="fcd1b-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="fcd1b-116">所属を表すプリンシパルの ID です。</span><span class="sxs-lookup"><span data-stu-id="fcd1b-116">ID of the principal representing the affiliation.</span></span> <span data-ttu-id="fcd1b-117">各プリンシパル (システムユーザーの種類を除く) には、自己所属も含まれています。</span><span class="sxs-lookup"><span data-stu-id="fcd1b-117">Each principal (except system-user-types) has a self-affiliation as well.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcd1b-118">位置</span><span class="sxs-lookup"><span data-stu-id="fcd1b-118">index</span></span></p></td>
<td><p><span data-ttu-id="fcd1b-119">int (null ではない)</span><span class="sxs-lookup"><span data-stu-id="fcd1b-119">int, not null</span></span></p></td>
<td><p><span data-ttu-id="fcd1b-120">位置.</span><span class="sxs-lookup"><span data-stu-id="fcd1b-120">Index.</span></span> <span data-ttu-id="fcd1b-121">自己所属の値は-1 であり、その他の所属については、principalID の各バケット内の1から順に1が増加し &lt; &gt; ます。</span><span class="sxs-lookup"><span data-stu-id="fcd1b-121">The value for self-affiliations is -1, and for the other affiliations it increases sequentially from 1 within each &lt;principalID, affiliationId&gt; bucket.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcd1b-122">updatedBy</span><span class="sxs-lookup"><span data-stu-id="fcd1b-122">updatedBy</span></span></p></td>
<td><p><span data-ttu-id="fcd1b-123">int (null ではない)</span><span class="sxs-lookup"><span data-stu-id="fcd1b-123">int, not null</span></span></p></td>
<td><p><span data-ttu-id="fcd1b-124">最新の更新プログラムを実行したプリンシパル。</span><span class="sxs-lookup"><span data-stu-id="fcd1b-124">Principal that did the latest update.</span></span> <span data-ttu-id="fcd1b-125">これは通常1で、Active Directory の同期を意味します。</span><span class="sxs-lookup"><span data-stu-id="fcd1b-125">This is usually 1, which means Active Directory Sync.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="fcd1b-126">機能</span><span class="sxs-lookup"><span data-stu-id="fcd1b-126">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fcd1b-127">行</span><span class="sxs-lookup"><span data-stu-id="fcd1b-127">Columns</span></span></th>
<th><span data-ttu-id="fcd1b-128">説明</span><span class="sxs-lookup"><span data-stu-id="fcd1b-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fcd1b-129">&lt;principalID、index、affiliationID&gt;</span><span class="sxs-lookup"><span data-stu-id="fcd1b-129">&lt;principalID, index, affiliationID&gt;</span></span></p></td>
<td><p><span data-ttu-id="fcd1b-130">主キー。</span><span class="sxs-lookup"><span data-stu-id="fcd1b-130">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcd1b-131">principalID</span><span class="sxs-lookup"><span data-stu-id="fcd1b-131">principalID</span></span></p></td>
<td><p><span data-ttu-id="fcd1b-132">TblPrincipal Id テーブルで参照される外部キー。</span><span class="sxs-lookup"><span data-stu-id="fcd1b-132">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcd1b-133">affiliationID</span><span class="sxs-lookup"><span data-stu-id="fcd1b-133">affiliationID</span></span></p></td>
<td><p><span data-ttu-id="fcd1b-134">TblPrincipal Id テーブルで参照される外部キー。</span><span class="sxs-lookup"><span data-stu-id="fcd1b-134">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="fcd1b-135">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fcd1b-135">


</div>

<span> </span>

</div>

</div>

</span></span></div>

