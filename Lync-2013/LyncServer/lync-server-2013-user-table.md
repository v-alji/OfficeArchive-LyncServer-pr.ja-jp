---
title: 'Lync Server 2013: User テーブル'
description: 'Lync Server 2013: ユーザーテーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: User table
ms:assetid: 6b52047e-286d-47ab-b7bc-a9b266f62d82
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398505(v=OCS.15)
ms:contentKeyID: 48184437
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 15d1ac08a229f4afea35a2727ef1105a5f24b826
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444169"
---
# <a name="user-table-in-lync-server-2013"></a><span data-ttu-id="1f0da-103">Lync Server 2013 の User テーブル</span><span class="sxs-lookup"><span data-stu-id="1f0da-103">User table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1f0da-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1f0da-104">

<span> </span></span></span>

<span data-ttu-id="1f0da-105">_**最終更新日:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="1f0da-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="1f0da-106">ユーザーテーブルは、データベースに記録されているセッションに参加しているさまざまなユーザーの一覧を格納するサポートテーブルです。</span><span class="sxs-lookup"><span data-stu-id="1f0da-106">The User table is a supporting table that stores a list of the various users who have participated in sessions recorded in the database.</span></span> <span data-ttu-id="1f0da-107">テーブル内の各レコードは、1人のユーザーを表します。</span><span class="sxs-lookup"><span data-stu-id="1f0da-107">Each record in the table represents one user.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1f0da-108"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="1f0da-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="1f0da-109"><strong>データ型</strong></span><span class="sxs-lookup"><span data-stu-id="1f0da-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="1f0da-110"><strong>キー/インデックス</strong></span><span class="sxs-lookup"><span data-stu-id="1f0da-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="1f0da-111"><strong>詳細</strong></span><span class="sxs-lookup"><span data-stu-id="1f0da-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f0da-112"><strong>UserKey</strong></span><span class="sxs-lookup"><span data-stu-id="1f0da-112"><strong>UserKey</strong></span></span></p></td>
<td><p><span data-ttu-id="1f0da-113">int</span><span class="sxs-lookup"><span data-stu-id="1f0da-113">int</span></span></p></td>
<td><p><span data-ttu-id="1f0da-114">Primary</span><span class="sxs-lookup"><span data-stu-id="1f0da-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="1f0da-115">このユーザーを識別する一意の番号です。</span><span class="sxs-lookup"><span data-stu-id="1f0da-115">Unique number identifying this user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f0da-116"><strong>URI</strong></span><span class="sxs-lookup"><span data-stu-id="1f0da-116"><strong>URI</strong></span></span></p></td>
<td><p><span data-ttu-id="1f0da-117">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="1f0da-117">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="1f0da-118">一意</span><span class="sxs-lookup"><span data-stu-id="1f0da-118">Unique</span></span></p></td>
<td><p><span data-ttu-id="1f0da-119">URI 文字列。</span><span class="sxs-lookup"><span data-stu-id="1f0da-119">URI string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f0da-120"><strong>URIType</strong></span><span class="sxs-lookup"><span data-stu-id="1f0da-120"><strong>URIType</strong></span></span></p></td>
<td><p><span data-ttu-id="1f0da-121">int</span><span class="sxs-lookup"><span data-stu-id="1f0da-121">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1f0da-122">1の URI の型が不明です。</span><span class="sxs-lookup"><span data-stu-id="1f0da-122">1 is unknown URI type.</span></span></p>
<p><span data-ttu-id="1f0da-123">2はユーザー URI です。</span><span class="sxs-lookup"><span data-stu-id="1f0da-123">2 is user URI.</span></span></p>
<p><span data-ttu-id="1f0da-124">4は会議の URI です。</span><span class="sxs-lookup"><span data-stu-id="1f0da-124">4 is conference URI.</span></span></p>
<p><span data-ttu-id="1f0da-125">8は電話の URI です。</span><span class="sxs-lookup"><span data-stu-id="1f0da-125">8 is phone URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f0da-126"><strong>TenantKey</strong></span><span class="sxs-lookup"><span data-stu-id="1f0da-126"><strong>TenantKey</strong></span></span></p></td>
<td><p><span data-ttu-id="1f0da-127">int</span><span class="sxs-lookup"><span data-stu-id="1f0da-127">int</span></span></p></td>
<td><p><span data-ttu-id="1f0da-128">外部</span><span class="sxs-lookup"><span data-stu-id="1f0da-128">Foreign</span></span></p></td>
<td><p><span data-ttu-id="1f0da-129">テナントテーブルから参照されたユーザーのテナント。</span><span class="sxs-lookup"><span data-stu-id="1f0da-129">Tenant of the user, referenced from tenant table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f0da-130"><strong>LastPoorCallTime</strong></span><span class="sxs-lookup"><span data-stu-id="1f0da-130"><strong>LastPoorCallTime</strong></span></span></p></td>
<td><p><span data-ttu-id="1f0da-131">datetime</span><span class="sxs-lookup"><span data-stu-id="1f0da-131">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1f0da-132">ユーザーが低品質の音声通話を行ったときの最新のタイムスタンプ。</span><span class="sxs-lookup"><span data-stu-id="1f0da-132">Latest time stamp when the user had a poor audio call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f0da-133"><strong>Nextupdatupdat</strong></span><span class="sxs-lookup"><span data-stu-id="1f0da-133"><strong>NextUpdateTS</strong></span></span></p></td>
<td><p><span data-ttu-id="1f0da-134">datetime</span><span class="sxs-lookup"><span data-stu-id="1f0da-134">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1f0da-135">内部使用のみ。</span><span class="sxs-lookup"><span data-stu-id="1f0da-135">For internal use only.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="1f0da-136">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1f0da-136">


</div>

<span> </span>

</div>

</div>

</span></span></div>

