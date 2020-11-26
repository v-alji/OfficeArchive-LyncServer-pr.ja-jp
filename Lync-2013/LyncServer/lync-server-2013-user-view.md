---
title: 'Lync Server 2013: ユーザービュー'
description: 'Lync Server 2013: ユーザービュー。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: User view
ms:assetid: 796f77e6-1da6-4969-b18b-3537209a1fe4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688100(v=OCS.15)
ms:contentKeyID: 49733699
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: aa606887e8050a51f1e5a87656bb74a7cd58bbc3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439163"
---
# <a name="user-view-in-lync-server-2013"></a><span data-ttu-id="71e86-103">Lync Server 2013 のユーザービュー</span><span class="sxs-lookup"><span data-stu-id="71e86-103">User view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="71e86-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="71e86-104">

<span> </span></span></span>

<span data-ttu-id="71e86-105">_**最終更新日:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="71e86-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="71e86-106">ユーザービューには、データベース内のレコードを持つ通話またはセッションに参加しているユーザーに関する情報が格納されます。</span><span class="sxs-lookup"><span data-stu-id="71e86-106">The User view stores information about users who have been involved in calls or sessions that have records in the database.</span></span> <span data-ttu-id="71e86-107">このビューは、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="71e86-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="71e86-108">列</span><span class="sxs-lookup"><span data-stu-id="71e86-108">Column</span></span></th>
<th><span data-ttu-id="71e86-109">データ型</span><span class="sxs-lookup"><span data-stu-id="71e86-109">Data Type</span></span></th>
<th><span data-ttu-id="71e86-110">詳細</span><span class="sxs-lookup"><span data-stu-id="71e86-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71e86-111">UserId</span><span class="sxs-lookup"><span data-stu-id="71e86-111">UserId</span></span></p></td>
<td><p><span data-ttu-id="71e86-112">int</span><span class="sxs-lookup"><span data-stu-id="71e86-112">int</span></span></p></td>
<td><p><span data-ttu-id="71e86-113">このユーザーを識別する一意の番号です。</span><span class="sxs-lookup"><span data-stu-id="71e86-113">Unique number identifying this user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71e86-114">UserUri</span><span class="sxs-lookup"><span data-stu-id="71e86-114">UserUri</span></span></p></td>
<td><p><span data-ttu-id="71e86-115">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="71e86-115">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="71e86-116">ユーザーの Uri。</span><span class="sxs-lookup"><span data-stu-id="71e86-116">Uri of the user.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71e86-117">TenantKey</span><span class="sxs-lookup"><span data-stu-id="71e86-117">TenantKey</span></span></p></td>
<td><p><span data-ttu-id="71e86-118">長さ</span><span class="sxs-lookup"><span data-stu-id="71e86-118">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="71e86-119">ユーザーのテナント。</span><span class="sxs-lookup"><span data-stu-id="71e86-119">Tenant of user.</span></span> <span data-ttu-id="71e86-120">詳細については、「 <a href="lync-server-2013-tenants-table.md">Lync Server 2013 のテナントの一覧</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="71e86-120">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71e86-121">UriType</span><span class="sxs-lookup"><span data-stu-id="71e86-121">UriType</span></span></p></td>
<td><p><span data-ttu-id="71e86-122">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="71e86-122">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="71e86-123">ユーザー URI の種類。</span><span class="sxs-lookup"><span data-stu-id="71e86-123">Type of user URI.</span></span> <span data-ttu-id="71e86-124">詳細については、「 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 の UriTypes テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="71e86-124">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="71e86-125">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="71e86-125">


</div>

<span> </span>

</div>

</div>

</span></span></div>

