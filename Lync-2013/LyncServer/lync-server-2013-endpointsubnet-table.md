---
title: 'Lync Server 2013: EndpointSubnet テーブル'
description: 'Lync Server 2013: EndpointSubnet テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: EndpointSubnet table
ms:assetid: d62e51d6-2117-4c41-adce-08f8d9d75ce0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398933(v=OCS.15)
ms:contentKeyID: 48185514
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 63e7d3c908a55ae866ed8e330cc8742b9f6a0096
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428665"
---
# <a name="endpointsubnet-table-in-lync-server-2013"></a><span data-ttu-id="c5636-103">Lync Server 2013 の EndpointSubnet テーブル</span><span class="sxs-lookup"><span data-stu-id="c5636-103">EndpointSubnet table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c5636-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c5636-104">

<span> </span></span></span>

<span data-ttu-id="c5636-105">_**最終更新日:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="c5636-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="c5636-106">EndpointSubnet テーブルは、サポートテーブルです。</span><span class="sxs-lookup"><span data-stu-id="c5636-106">The EndpointSubnet table is a supporting table.</span></span> <span data-ttu-id="c5636-107">各レコードは、エンドポイントから取得された1つのサブネットを表します。</span><span class="sxs-lookup"><span data-stu-id="c5636-107">Each record represents one subnet captured from endpoints.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c5636-108"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="c5636-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="c5636-109"><strong>データ型</strong></span><span class="sxs-lookup"><span data-stu-id="c5636-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="c5636-110"><strong>キー/インデックス</strong></span><span class="sxs-lookup"><span data-stu-id="c5636-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="c5636-111"><strong>詳細</strong></span><span class="sxs-lookup"><span data-stu-id="c5636-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5636-112"><strong>SubnetIP</strong></span><span class="sxs-lookup"><span data-stu-id="c5636-112"><strong>SubnetIP</strong></span></span></p></td>
<td><p><span data-ttu-id="c5636-113">int</span><span class="sxs-lookup"><span data-stu-id="c5636-113">int</span></span></p></td>
<td><p><span data-ttu-id="c5636-114">プライマリ、外部</span><span class="sxs-lookup"><span data-stu-id="c5636-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="c5636-115">サブネットの整数表現。</span><span class="sxs-lookup"><span data-stu-id="c5636-115">Integer representation for the subnet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5636-116"><strong>Nextupdatupdat</strong></span><span class="sxs-lookup"><span data-stu-id="c5636-116"><strong>NextUpdateTS</strong></span></span></p></td>
<td><p><span data-ttu-id="c5636-117">datetime</span><span class="sxs-lookup"><span data-stu-id="c5636-117">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c5636-118">内部使用のみ。</span><span class="sxs-lookup"><span data-stu-id="c5636-118">For internal use only.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="c5636-119">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c5636-119">


</div>

<span> </span>

</div>

</div>

</span></span></div>

