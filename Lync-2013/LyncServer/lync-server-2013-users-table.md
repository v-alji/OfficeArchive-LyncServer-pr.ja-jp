---
title: 'Lync Server 2013: ユーザー テーブル'
description: 'Lync Server 2013: ユーザーテーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Users table
ms:assetid: a8d71373-4b57-4245-9f02-f7fc0d9fcd3c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412791(v=OCS.15)
ms:contentKeyID: 48185032
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9b1418e162a04e46ee0dfeca082aa66b0665fc77
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436182"
---
# <a name="users-table-in-lync-server-2013"></a><span data-ttu-id="05530-103">Lync Server 2013 のユーザー テーブル</span><span class="sxs-lookup"><span data-stu-id="05530-103">Users table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="05530-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="05530-104">

<span> </span></span></span>

<span data-ttu-id="05530-105">_**最終更新日:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="05530-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="05530-106">ユーザーテーブルは、サポートテーブルです。</span><span class="sxs-lookup"><span data-stu-id="05530-106">The Users table is a supporting table.</span></span> <span data-ttu-id="05530-107">テーブル内の各レコードには、データベース内のレコードが含まれる1人のユーザーに関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="05530-107">Each record in the table stores information about one user involved in calls or sessions that have records in the database.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="05530-108">列</span><span class="sxs-lookup"><span data-stu-id="05530-108">Column</span></span></th>
<th><span data-ttu-id="05530-109">データ型</span><span class="sxs-lookup"><span data-stu-id="05530-109">Data Type</span></span></th>
<th><span data-ttu-id="05530-110">キー/インデックス</span><span class="sxs-lookup"><span data-stu-id="05530-110">Key/Index</span></span></th>
<th><span data-ttu-id="05530-111">詳細</span><span class="sxs-lookup"><span data-stu-id="05530-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="05530-112"><strong>Nextupdatupdat</strong></span><span class="sxs-lookup"><span data-stu-id="05530-112"><strong>NextUpdateTS</strong></span></span></p></td>
<td><p><span data-ttu-id="05530-113">datetime</span><span class="sxs-lookup"><span data-stu-id="05530-113">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="05530-114">内部使用のタイムスタンプ。</span><span class="sxs-lookup"><span data-stu-id="05530-114">Time stamp for internal use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05530-115"><strong>UserId</strong></span><span class="sxs-lookup"><span data-stu-id="05530-115"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="05530-116">int</span><span class="sxs-lookup"><span data-stu-id="05530-116">int</span></span></p></td>
<td><p><span data-ttu-id="05530-117">Primary</span><span class="sxs-lookup"><span data-stu-id="05530-117">Primary</span></span></p></td>
<td><p><span data-ttu-id="05530-118">このユーザーを識別する一意の番号です。</span><span class="sxs-lookup"><span data-stu-id="05530-118">Unique number identifying this user.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="05530-119"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="05530-119"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="05530-120">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="05530-120">nvarchar(450)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="05530-121">ユーザー URI。</span><span class="sxs-lookup"><span data-stu-id="05530-121">User URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05530-122"><strong>テナント</strong></span><span class="sxs-lookup"><span data-stu-id="05530-122"><strong>TenantId</strong></span></span></p></td>
<td><p><span data-ttu-id="05530-123">int</span><span class="sxs-lookup"><span data-stu-id="05530-123">int</span></span></p></td>
<td><p><span data-ttu-id="05530-124">外部</span><span class="sxs-lookup"><span data-stu-id="05530-124">Foreign</span></span></p></td>
<td><p><span data-ttu-id="05530-125">このユーザーのテナント ID。</span><span class="sxs-lookup"><span data-stu-id="05530-125">This user’s Tenant ID.</span></span> <span data-ttu-id="05530-126">詳細については、「 <a href="lync-server-2013-tenants-table.md">Lync Server 2013 のテナントの一覧</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="05530-126">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="05530-127"><strong>UriTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="05530-127"><strong>UriTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="05530-128">int</span><span class="sxs-lookup"><span data-stu-id="05530-128">int</span></span></p></td>
<td><p><span data-ttu-id="05530-129">外部</span><span class="sxs-lookup"><span data-stu-id="05530-129">Foreign</span></span></p></td>
<td><p><span data-ttu-id="05530-130">このユーザーの URI 型。</span><span class="sxs-lookup"><span data-stu-id="05530-130">This user’s URI type.</span></span> <span data-ttu-id="05530-131">詳細については、「 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 の UriTypes テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="05530-131">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="05530-132">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="05530-132">


</div>

<span> </span>

</div>

</div>

</span></span></div>

