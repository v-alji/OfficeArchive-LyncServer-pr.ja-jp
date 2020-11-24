---
title: 'Lync Server 2013: Subnet テーブル'
description: 'Lync Server 2013: サブネットテーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Subnet table
ms:assetid: 76f5c995-96c8-4aa3-bc30-1d74991d7c42
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398582(v=OCS.15)
ms:contentKeyID: 48184544
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d30c04ddf897e0a62551709b30211ba724a75cbf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398126"
---
# <a name="subnet-table-in-lync-server-2013"></a><span data-ttu-id="75b55-103">Lync Server 2013 の Subnet テーブル</span><span class="sxs-lookup"><span data-stu-id="75b55-103">Subnet table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="75b55-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="75b55-104">

<span> </span></span></span>

<span data-ttu-id="75b55-105">_**最終更新日:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="75b55-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="75b55-106">サブネットの表はサポートテーブルです。</span><span class="sxs-lookup"><span data-stu-id="75b55-106">The Subnet table is a supporting table.</span></span> <span data-ttu-id="75b55-107">各レコードは、[ネットワーク構成] の設定で定義された1つのサブネットを表します。</span><span class="sxs-lookup"><span data-stu-id="75b55-107">Each record represents one subnet defined in network configuration setting.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="75b55-108"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="75b55-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="75b55-109"><strong>データ型</strong></span><span class="sxs-lookup"><span data-stu-id="75b55-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="75b55-110"><strong>キー/インデックス</strong></span><span class="sxs-lookup"><span data-stu-id="75b55-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="75b55-111"><strong>詳細</strong></span><span class="sxs-lookup"><span data-stu-id="75b55-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75b55-112"><strong>SubnetIP</strong></span><span class="sxs-lookup"><span data-stu-id="75b55-112"><strong>SubnetIP</strong></span></span></p></td>
<td><p><span data-ttu-id="75b55-113">int</span><span class="sxs-lookup"><span data-stu-id="75b55-113">int</span></span></p></td>
<td><p><span data-ttu-id="75b55-114">プライマリ、外部</span><span class="sxs-lookup"><span data-stu-id="75b55-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="75b55-115">サブネットの IP の整数表現。</span><span class="sxs-lookup"><span data-stu-id="75b55-115">Integer representation for the subnet IP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b55-116"><strong>ネット</strong></span><span class="sxs-lookup"><span data-stu-id="75b55-116"><strong>SubnetMask</strong></span></span></p></td>
<td><p><span data-ttu-id="75b55-117">int</span><span class="sxs-lookup"><span data-stu-id="75b55-117">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="75b55-118">サブネット マスク。</span><span class="sxs-lookup"><span data-stu-id="75b55-118">Subnet mask.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75b55-119"><strong>UserSiteKey</strong></span><span class="sxs-lookup"><span data-stu-id="75b55-119"><strong>UserSiteKey</strong></span></span></p></td>
<td><p><span data-ttu-id="75b55-120">int</span><span class="sxs-lookup"><span data-stu-id="75b55-120">int</span></span></p></td>
<td><p><span data-ttu-id="75b55-121">外部</span><span class="sxs-lookup"><span data-stu-id="75b55-121">Foreign</span></span></p></td>
<td><p><span data-ttu-id="75b55-122"><a href="lync-server-2013-usersite-table.md">Lync Server 2013 の Usersite テーブル</a>から参照されます。</span><span class="sxs-lookup"><span data-stu-id="75b55-122">Referenced from the <a href="lync-server-2013-usersite-table.md">UserSite table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75b55-123"><strong>サブネットの説明</strong></span><span class="sxs-lookup"><span data-stu-id="75b55-123"><strong>SubnetDescription</strong></span></span></p></td>
<td><p><span data-ttu-id="75b55-124">nvarchar (512)</span><span class="sxs-lookup"><span data-stu-id="75b55-124">nvarchar(512)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="75b55-125">サブネットの説明。</span><span class="sxs-lookup"><span data-stu-id="75b55-125">The description for the subnet.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="75b55-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="75b55-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

