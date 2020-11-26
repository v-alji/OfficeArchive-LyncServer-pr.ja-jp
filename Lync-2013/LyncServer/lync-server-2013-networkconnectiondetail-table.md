---
title: 'Lync Server 2013: NetworkConnectionDetail テーブル'
description: 'Lync Server 2013: NetworkConnectionDetail テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: NetworkConnectionDetail table
ms:assetid: b48cc9a6-5232-48b5-bd20-53b68229336b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205185(v=OCS.15)
ms:contentKeyID: 48185170
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dcd0f429999b6629826a9f9369d154afe3c1af2f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445492"
---
# <a name="networkconnectiondetail-table-in-lync-server-2013"></a><span data-ttu-id="2a110-103">Lync Server 2013 の NetworkConnectionDetail テーブル</span><span class="sxs-lookup"><span data-stu-id="2a110-103">NetworkConnectionDetail table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2a110-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2a110-104">

<span> </span></span></span>

<span data-ttu-id="2a110-105">_**最終更新日:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="2a110-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="2a110-106">NetworkConnectionDetail テーブルは、ネットワーク接続の種類を、エクスペリエンスデータベースの他の場所で使用されていたネットワーク接続識別子にマップします。</span><span class="sxs-lookup"><span data-stu-id="2a110-106">The NetworkConnectionDetail table maps network connection types to the network connection identifiers used elsewhere in the Quality of Experience database.</span></span> <span data-ttu-id="2a110-107">この表は、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="2a110-107">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2a110-108"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="2a110-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="2a110-109"><strong>データ型</strong></span><span class="sxs-lookup"><span data-stu-id="2a110-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="2a110-110"><strong>キー/インデックス</strong></span><span class="sxs-lookup"><span data-stu-id="2a110-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="2a110-111"><strong>詳細</strong></span><span class="sxs-lookup"><span data-stu-id="2a110-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2a110-112"><strong>Networkconnectionのキー</strong></span><span class="sxs-lookup"><span data-stu-id="2a110-112"><strong>NetworkConnectionDetailKey</strong></span></span></p></td>
<td><p><span data-ttu-id="2a110-113">tinyint</span><span class="sxs-lookup"><span data-stu-id="2a110-113">tinyint</span></span></p></td>
<td><p><span data-ttu-id="2a110-114">Primary</span><span class="sxs-lookup"><span data-stu-id="2a110-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="2a110-115">ネットワーク接続の種類を表す一意の識別子です。</span><span class="sxs-lookup"><span data-stu-id="2a110-115">Unique identifier for the network connection type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a110-116"><strong>NetworkConnectionDetail</strong></span><span class="sxs-lookup"><span data-stu-id="2a110-116"><strong>NetworkConnectionDetail</strong></span></span></p></td>
<td><p><span data-ttu-id="2a110-117">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="2a110-117">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="2a110-118">一意</span><span class="sxs-lookup"><span data-stu-id="2a110-118">Unique</span></span></p></td>
<td><p><span data-ttu-id="2a110-119">ネットワーク接続の種類。ネットワーク接続の種類キーに対応しています。</span><span class="sxs-lookup"><span data-stu-id="2a110-119">Network connection type that corresponds to the NetworkConnectionDetailKey.</span></span> <span data-ttu-id="2a110-120">有効な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="2a110-120">Allowed values are:</span></span></p>
<ol>
<li><p><span data-ttu-id="2a110-121">0--有線</span><span class="sxs-lookup"><span data-stu-id="2a110-121">0 -- Wired</span></span></p></li>
<li><p><span data-ttu-id="2a110-122">1--WiFi</span><span class="sxs-lookup"><span data-stu-id="2a110-122">1 -- WiFi</span></span></p></li>
<li><p><span data-ttu-id="2a110-123">2--イーサネット</span><span class="sxs-lookup"><span data-stu-id="2a110-123">2 -- Ethernet</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table><span data-ttu-id="2a110-124">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2a110-124">


</div>

<span> </span>

</div>

</div>

</span></span></div>

