---
title: 'Lync Server 2013: tblRoleType'
description: 'Lync Server 2013: tblRoleType'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblRoleType
ms:assetid: 1eac3a54-656a-40ac-b771-edfc64d6e34b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558623(v=OCS.15)
ms:contentKeyID: 48183577
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f458259acaee7821d5f6a7339b993c70fe65f595
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398078"
---
# <a name="tblroletype-in-lync-server-2013"></a><span data-ttu-id="99422-103">Lync Server 2013 の tblRoleType</span><span class="sxs-lookup"><span data-stu-id="99422-103">tblRoleType in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="99422-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="99422-104">

<span> </span></span></span>

<span data-ttu-id="99422-105">_**最終更新日:** 2012-06-25_</span><span class="sxs-lookup"><span data-stu-id="99422-105">_**Topic Last Modified:** 2012-06-25_</span></span>

<span data-ttu-id="99422-106">tblRoleType は、役割の種類とそれに関連付けられたアクセス許可セットを含む静的参照テーブルです。</span><span class="sxs-lookup"><span data-stu-id="99422-106">tblRoleType is a static lookup table with role types and their associated permission sets.</span></span>

### <a name="columns"></a><span data-ttu-id="99422-107">行</span><span class="sxs-lookup"><span data-stu-id="99422-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="99422-108">列</span><span class="sxs-lookup"><span data-stu-id="99422-108">Column</span></span></th>
<th><span data-ttu-id="99422-109">型</span><span class="sxs-lookup"><span data-stu-id="99422-109">Type</span></span></th>
<th><span data-ttu-id="99422-110">説明</span><span class="sxs-lookup"><span data-stu-id="99422-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="99422-111">rtypeID</span><span class="sxs-lookup"><span data-stu-id="99422-111">rtypeID</span></span></p></td>
<td><p><span data-ttu-id="99422-112">int (null ではない)</span><span class="sxs-lookup"><span data-stu-id="99422-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="99422-113">役割の種類 ID。</span><span class="sxs-lookup"><span data-stu-id="99422-113">Role type ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99422-114">rtypeDesc</span><span class="sxs-lookup"><span data-stu-id="99422-114">rtypeDesc</span></span></p></td>
<td><p><span data-ttu-id="99422-115">nvarchar (256)、null ではない</span><span class="sxs-lookup"><span data-stu-id="99422-115">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="99422-116">役割の種類の説明。</span><span class="sxs-lookup"><span data-stu-id="99422-116">Role type description.</span></span> <span data-ttu-id="99422-117">次の4つの役割を使用できます。</span><span class="sxs-lookup"><span data-stu-id="99422-117">There are four available roles:</span></span></p>
<ul>
<li><p><span data-ttu-id="99422-118">メンバー: チャットルームのメンバー</span><span class="sxs-lookup"><span data-stu-id="99422-118">Member: Chat room member</span></span></p></li>
<li><p><span data-ttu-id="99422-119">管理職: チャットルームマネージャー</span><span class="sxs-lookup"><span data-stu-id="99422-119">Manager: Chat room manager</span></span></p></li>
<li><p><span data-ttu-id="99422-120">読み上げ: 聴衆チャットルームの発表者</span><span class="sxs-lookup"><span data-stu-id="99422-120">Voiced: Presenter for an auditorium chat room</span></span></p></li>
<li><p><span data-ttu-id="99422-121">作成者: チャットルームを作成できる</span><span class="sxs-lookup"><span data-stu-id="99422-121">Creator: Can create chat rooms</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99422-122">rtypeAllowedPermSet</span><span class="sxs-lookup"><span data-stu-id="99422-122">rtypeAllowedPermSet</span></span></p></td>
<td><p><span data-ttu-id="99422-123">bigint (null ではない)</span><span class="sxs-lookup"><span data-stu-id="99422-123">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="99422-124">ロールの権限セット。</span><span class="sxs-lookup"><span data-stu-id="99422-124">Permission set for the role.</span></span> <span data-ttu-id="99422-125">使用されるビットは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="99422-125">The used bits are:</span></span></p>
<ul>
<li><p><span data-ttu-id="99422-126">2: 役割がノードを管理できる場合は True。</span><span class="sxs-lookup"><span data-stu-id="99422-126">2: True if the role can manage nodes.</span></span></p></li>
<li><p><span data-ttu-id="99422-127">4: 役割で子ノードを作成できる場合は True です。</span><span class="sxs-lookup"><span data-stu-id="99422-127">4: True if the role can create children nodes.</span></span></p></li>
<li><p><span data-ttu-id="99422-128">7: 役割がチャットルーム (または、カテゴリの子チャットルーム) に参加できる場合は True。</span><span class="sxs-lookup"><span data-stu-id="99422-128">7: True if the role can join a chat room (or children chat rooms of a category).</span></span></p></li>
<li><p><span data-ttu-id="99422-129">8: 役割がチャットルーム (または、カテゴリの子チャットルーム) でチャットできる場合は True。</span><span class="sxs-lookup"><span data-stu-id="99422-129">8: True if the role can chat in a chat room (or in children chat rooms of a category).</span></span></p></li>
<li><p><span data-ttu-id="99422-130">10: 役割がチャットルームに参加していないときでもチャット履歴を読むことができる場合は True。</span><span class="sxs-lookup"><span data-stu-id="99422-130">10: True if the role can read chat history even when not joined to a chat room.</span></span></p></li>
<li><p><span data-ttu-id="99422-131">11: 役割がチャットルームを表示できる場合は True です。</span><span class="sxs-lookup"><span data-stu-id="99422-131">11: True if the role can see the chat room.</span></span> <span data-ttu-id="99422-132">(これは、スコープや可視性などの要因によってさらに改良されています)。</span><span class="sxs-lookup"><span data-stu-id="99422-132">(This is further refined by factors such as scope and visibility.)</span></span></p></li>
<li><p><span data-ttu-id="99422-133">12: この役割が聴衆チャットルームでチャットできる場合は True です。</span><span class="sxs-lookup"><span data-stu-id="99422-133">12: True if the role can chat in an auditorium chat room.</span></span></p></li>
<li><p><span data-ttu-id="99422-134">13: ノードを表示したときに、役割が可視性規則を無視できる場合は True です。</span><span class="sxs-lookup"><span data-stu-id="99422-134">13: True if the role can bypass visibility rules when viewing nodes.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="99422-135">キー</span><span class="sxs-lookup"><span data-stu-id="99422-135">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="99422-136">列</span><span class="sxs-lookup"><span data-stu-id="99422-136">Column</span></span></th>
<th><span data-ttu-id="99422-137">説明</span><span class="sxs-lookup"><span data-stu-id="99422-137">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="99422-138">rtypeID</span><span class="sxs-lookup"><span data-stu-id="99422-138">rtypeID</span></span></p></td>
<td><p><span data-ttu-id="99422-139">主キー。</span><span class="sxs-lookup"><span data-stu-id="99422-139">Primary key.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="99422-140">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="99422-140">


</div>

<span> </span>

</div>

</div>

</span></span></div>

