---
title: 'Lync Server 2013: ConferenceJoinTimeThresholds テーブル'
description: 'Lync Server 2013: ConferenceJoinTimeThresholds テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ConferenceJoinTimeThresholds table
ms:assetid: 3944d724-bdd8-4d1c-a2af-933ee8141529
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204809(v=OCS.15)
ms:contentKeyID: 48183855
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5e38c8b99f444e16309882b6a8885d166fdceb9b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434460"
---
# <a name="conferencejointimethresholds-table-in-lync-server-2013"></a><span data-ttu-id="8158e-103">Lync Server 2013 の ConferenceJoinTimeThresholds テーブル</span><span class="sxs-lookup"><span data-stu-id="8158e-103">ConferenceJoinTimeThresholds table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8158e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8158e-104">

<span> </span></span></span>

<span data-ttu-id="8158e-105">_**最終更新日:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="8158e-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="8158e-106">ConferenceJoinTimeThresholds テーブルには、電話会議の参加時間のサマリーレポートで使用される分類境界が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8158e-106">The ConferenceJoinTimeThresholds table contains the classification boundaries used by the Conference Join Time Summary Report.</span></span> <span data-ttu-id="8158e-107">[会議参加時間のサマリー] レポートは、ユーザーが会議に参加するのに必要な時間の概要を示します。これらの時間値は、平均として、または次のいずれかのカテゴリに報告されます。</span><span class="sxs-lookup"><span data-stu-id="8158e-107">The Conference Join Time Summary Report summarizes the amount time required for users to successfully join a conference; these time values are reported both as an average and in one of the following categories:</span></span>

  - <span data-ttu-id="8158e-108">2秒未満。</span><span class="sxs-lookup"><span data-stu-id="8158e-108">Less than 2 seconds.</span></span>

  - <span data-ttu-id="8158e-109">2秒と5秒の間。</span><span class="sxs-lookup"><span data-stu-id="8158e-109">Between 2 second and 5 seconds.</span></span>

  - <span data-ttu-id="8158e-110">5 ~ 10 秒の間。</span><span class="sxs-lookup"><span data-stu-id="8158e-110">Between 5 seconds and 10 seconds.</span></span>

  - <span data-ttu-id="8158e-111">10秒以上</span><span class="sxs-lookup"><span data-stu-id="8158e-111">More than 10 seconds.</span></span>

<span data-ttu-id="8158e-112">ConferenceJoinTimeThresholds テーブルには、2秒、5秒、10秒の分類値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8158e-112">The ConferenceJoinTimeThresholds table contains the classification values 2 seconds, 5 seconds, and 10 seconds.</span></span>

<span data-ttu-id="8158e-113">この表は、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="8158e-113">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8158e-114">列</span><span class="sxs-lookup"><span data-stu-id="8158e-114">Column</span></span></th>
<th><span data-ttu-id="8158e-115">データ型</span><span class="sxs-lookup"><span data-stu-id="8158e-115">Data Type</span></span></th>
<th><span data-ttu-id="8158e-116">キー/インデックス</span><span class="sxs-lookup"><span data-stu-id="8158e-116">Key/Index</span></span></th>
<th><span data-ttu-id="8158e-117">詳細</span><span class="sxs-lookup"><span data-stu-id="8158e-117">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8158e-118"><strong>ThresholdId</strong></span><span class="sxs-lookup"><span data-stu-id="8158e-118"><strong>ThresholdId</strong></span></span></p></td>
<td><p><span data-ttu-id="8158e-119">int</span><span class="sxs-lookup"><span data-stu-id="8158e-119">int</span></span></p></td>
<td><p><span data-ttu-id="8158e-120">Primary</span><span class="sxs-lookup"><span data-stu-id="8158e-120">Primary</span></span></p></td>
<td><p><span data-ttu-id="8158e-121">分類の一意の識別子。</span><span class="sxs-lookup"><span data-stu-id="8158e-121">Unique identifier for the classification.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8158e-122"><strong>ThresholdValue</strong></span><span class="sxs-lookup"><span data-stu-id="8158e-122"><strong>ThresholdValue</strong></span></span></p></td>
<td><p><span data-ttu-id="8158e-123">int</span><span class="sxs-lookup"><span data-stu-id="8158e-123">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8158e-124">分類の上限。</span><span class="sxs-lookup"><span data-stu-id="8158e-124">Upper limit for the classification.</span></span> <span data-ttu-id="8158e-125">有効な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="8158e-125">Allowed values are:</span></span></p>
<ol>
<li><p><span data-ttu-id="8158e-126">2</span><span class="sxs-lookup"><span data-stu-id="8158e-126">2</span></span></p></li>
<li><p><span data-ttu-id="8158e-127">5</span><span class="sxs-lookup"><span data-stu-id="8158e-127">5</span></span></p></li>
<li><p><span data-ttu-id="8158e-128">常用</span><span class="sxs-lookup"><span data-stu-id="8158e-128">10</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table><span data-ttu-id="8158e-129">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8158e-129">


</div>

<span> </span>

</div>

</div>

</span></span></div>

