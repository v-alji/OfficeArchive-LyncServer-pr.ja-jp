---
title: 'Lync Server 2013: UserSite テーブル'
description: 'Lync Server 2013: UserSite テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: UserSite table
ms:assetid: 1c2a3cf2-dc05-472e-8097-a31f3a1aafcb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398256(v=OCS.15)
ms:contentKeyID: 48183552
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4e0fb3149b9378bbfd3f14da8176eed226e4f57f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436112"
---
# <a name="usersite-table-in-lync-server-2013"></a><span data-ttu-id="23d14-103">Lync Server 2013 の UserSite テーブル</span><span class="sxs-lookup"><span data-stu-id="23d14-103">UserSite table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="23d14-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="23d14-104">

<span> </span></span></span>

<span data-ttu-id="23d14-105">_**最終更新日:** 2010-11-09_</span><span class="sxs-lookup"><span data-stu-id="23d14-105">_**Topic Last Modified:** 2010-11-09_</span></span>

<span data-ttu-id="23d14-106">UserSite テーブルは、サポートされているテーブルです。</span><span class="sxs-lookup"><span data-stu-id="23d14-106">The UserSite table is a supporting table.</span></span> <span data-ttu-id="23d14-107">各レコードは、[ネットワーク構成] の設定で定義された1つのユーザーサイトを表します。</span><span class="sxs-lookup"><span data-stu-id="23d14-107">Each record represents one user site defined in network configuration setting.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="23d14-108"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="23d14-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="23d14-109"><strong>データ型</strong></span><span class="sxs-lookup"><span data-stu-id="23d14-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="23d14-110"><strong>キー/インデックス</strong></span><span class="sxs-lookup"><span data-stu-id="23d14-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="23d14-111"><strong>詳細</strong></span><span class="sxs-lookup"><span data-stu-id="23d14-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="23d14-112"><strong>UserSiteKey</strong></span><span class="sxs-lookup"><span data-stu-id="23d14-112"><strong>UserSiteKey</strong></span></span></p></td>
<td><p><span data-ttu-id="23d14-113">int</span><span class="sxs-lookup"><span data-stu-id="23d14-113">int</span></span></p></td>
<td><p><span data-ttu-id="23d14-114">Primary</span><span class="sxs-lookup"><span data-stu-id="23d14-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="23d14-115">ユーザーサイトを識別する一意の番号です。</span><span class="sxs-lookup"><span data-stu-id="23d14-115">Unique number identifying the user site.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23d14-116"><strong>UserSiteName</strong></span><span class="sxs-lookup"><span data-stu-id="23d14-116"><strong>UserSiteName</strong></span></span></p></td>
<td><p><span data-ttu-id="23d14-117">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="23d14-117">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="23d14-118">一意</span><span class="sxs-lookup"><span data-stu-id="23d14-118">Unique</span></span></p></td>
<td><p><span data-ttu-id="23d14-119">ユーザーサイトの名前。</span><span class="sxs-lookup"><span data-stu-id="23d14-119">User site’s name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23d14-120"><strong>RegionKey</strong></span><span class="sxs-lookup"><span data-stu-id="23d14-120"><strong>RegionKey</strong></span></span></p></td>
<td><p><span data-ttu-id="23d14-121">int</span><span class="sxs-lookup"><span data-stu-id="23d14-121">int</span></span></p></td>
<td><p><span data-ttu-id="23d14-122">外部</span><span class="sxs-lookup"><span data-stu-id="23d14-122">Foreign</span></span></p></td>
<td><p><span data-ttu-id="23d14-123"><a href="lync-server-2013-region-table.md">Lync Server 2013 の地域テーブル</a>から参照されている。</span><span class="sxs-lookup"><span data-stu-id="23d14-123">Referenced from <a href="lync-server-2013-region-table.md">Region table in Lync Server 2013</a>.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="23d14-124">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="23d14-124">


</div>

<span> </span>

</div>

</div>

</span></span></div>

