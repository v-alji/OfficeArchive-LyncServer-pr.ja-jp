---
title: 'Lync Server 2013: tblPrincipalMemberDifference'
description: 'Lync Server 2013: tblPrincipalMemberDifference'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalMemberDifference
ms:assetid: 0b94f555-6888-4fe0-a048-4660a2513276
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558612(v=OCS.15)
ms:contentKeyID: 48183379
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ce7c770a6fed02dc27d2493816fae58943d391a6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398115"
---
# <a name="tblprincipalmemberdifference-in-lync-server-2013"></a><span data-ttu-id="bd950-103">Lync Server 2013 の tblPrincipalMemberDifference</span><span class="sxs-lookup"><span data-stu-id="bd950-103">tblPrincipalMemberDifference in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bd950-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bd950-104">

<span> </span></span></span>

<span data-ttu-id="bd950-105">_**最終更新日:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="bd950-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="bd950-106">tblPrincipalMemberDifference には、後の Active Directory ドメインサービスの同期手順でまだ処理されていないグループメンバーシップの変更 (メンバーの追加と削除) が含まれています。</span><span class="sxs-lookup"><span data-stu-id="bd950-106">tblPrincipalMemberDifference contains group membership changes (both added and removed members) that have not yet been processed by the later Active Directory Domain Services Sync steps.</span></span>

### <a name="columns"></a><span data-ttu-id="bd950-107">行</span><span class="sxs-lookup"><span data-stu-id="bd950-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bd950-108">列</span><span class="sxs-lookup"><span data-stu-id="bd950-108">Column</span></span></th>
<th><span data-ttu-id="bd950-109">型</span><span class="sxs-lookup"><span data-stu-id="bd950-109">Type</span></span></th>
<th><span data-ttu-id="bd950-110">説明</span><span class="sxs-lookup"><span data-stu-id="bd950-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd950-111">prinGuid</span><span class="sxs-lookup"><span data-stu-id="bd950-111">prinGuid</span></span></p></td>
<td><p><span data-ttu-id="bd950-112">GUID、null ではない</span><span class="sxs-lookup"><span data-stu-id="bd950-112">GUID, not null</span></span></p></td>
<td><p><span data-ttu-id="bd950-113">変更されたグループのプリンシパル GUID。</span><span class="sxs-lookup"><span data-stu-id="bd950-113">Principal GUID of the group that changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd950-114">memberADPath</span><span class="sxs-lookup"><span data-stu-id="bd950-114">memberADPath</span></span></p></td>
<td><p><span data-ttu-id="bd950-115">nvarchar (256)</span><span class="sxs-lookup"><span data-stu-id="bd950-115">nvarchar (256)</span></span></p></td>
<td><p><span data-ttu-id="bd950-116">メンバーの識別名。</span><span class="sxs-lookup"><span data-stu-id="bd950-116">Distinguished name of the member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd950-117">メンバーの削除</span><span class="sxs-lookup"><span data-stu-id="bd950-117">memberRemoved</span></span></p></td>
<td><p><span data-ttu-id="bd950-118">ビット、null ではない</span><span class="sxs-lookup"><span data-stu-id="bd950-118">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="bd950-119">メンバーが追加された場合は False。</span><span class="sxs-lookup"><span data-stu-id="bd950-119">False if the member was added.</span></span> <span data-ttu-id="bd950-120">メンバーが削除された場合は True です。</span><span class="sxs-lookup"><span data-stu-id="bd950-120">True if the member was removed.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="bd950-121">キー</span><span class="sxs-lookup"><span data-stu-id="bd950-121">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bd950-122">列</span><span class="sxs-lookup"><span data-stu-id="bd950-122">Column</span></span></th>
<th><span data-ttu-id="bd950-123">説明</span><span class="sxs-lookup"><span data-stu-id="bd950-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd950-124">&lt;prinGuid、memberADPath&gt;</span><span class="sxs-lookup"><span data-stu-id="bd950-124">&lt;prinGuid, memberADPath&gt;</span></span></p></td>
<td><p><span data-ttu-id="bd950-125">主キー。</span><span class="sxs-lookup"><span data-stu-id="bd950-125">Primary key.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="bd950-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bd950-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

