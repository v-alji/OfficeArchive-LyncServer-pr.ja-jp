---
title: 'Lync Server 2013: SessionCorrelation テーブル'
description: 'Lync Server 2013: セッション相関関係テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: SessionCorrelation table
ms:assetid: 041705e1-7290-464f-95f8-96256cfa2e3e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398091(v=OCS.15)
ms:contentKeyID: 48183267
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 814b7e8539d89f87e7df60ceb03e70800553fb55
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424080"
---
# <a name="sessioncorrelation-table-in-lync-server-2013"></a><span data-ttu-id="00d6e-103">Lync Server 2013 の SessionCorrelation テーブル</span><span class="sxs-lookup"><span data-stu-id="00d6e-103">SessionCorrelation table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="00d6e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="00d6e-104">

<span> </span></span></span>

<span data-ttu-id="00d6e-105">_**最終更新日:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="00d6e-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="00d6e-106">セッション相関関係テーブルは、サポートテーブルです。</span><span class="sxs-lookup"><span data-stu-id="00d6e-106">The SessionCorrelation table is a supporting table.</span></span> <span data-ttu-id="00d6e-107">各レコードは、複数のセッションを関連付けるために使用される1つの CorrelationID を表します。</span><span class="sxs-lookup"><span data-stu-id="00d6e-107">Each record represents one CorrelationID which is used to correlate multiple sessions.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="00d6e-108"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="00d6e-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="00d6e-109"><strong>データ型</strong></span><span class="sxs-lookup"><span data-stu-id="00d6e-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="00d6e-110"><strong>キー/インデックス</strong></span><span class="sxs-lookup"><span data-stu-id="00d6e-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="00d6e-111"><strong>詳細</strong></span><span class="sxs-lookup"><span data-stu-id="00d6e-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="00d6e-112"><strong>サム</strong></span><span class="sxs-lookup"><span data-stu-id="00d6e-112"><strong>Checksum</strong></span></span></p></td>
<td><p><span data-ttu-id="00d6e-113">int</span><span class="sxs-lookup"><span data-stu-id="00d6e-113">int</span></span></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00d6e-114"><strong>CorrelationKey</strong></span><span class="sxs-lookup"><span data-stu-id="00d6e-114"><strong>CorrelationKey</strong></span></span></p></td>
<td><p><span data-ttu-id="00d6e-115">int</span><span class="sxs-lookup"><span data-stu-id="00d6e-115">int</span></span></p></td>
<td><p><span data-ttu-id="00d6e-116">Primary</span><span class="sxs-lookup"><span data-stu-id="00d6e-116">Primary</span></span></p></td>
<td><p><span data-ttu-id="00d6e-117">この A/V 会議サーバーを識別する一意の番号です。</span><span class="sxs-lookup"><span data-stu-id="00d6e-117">Unique number identifying this A/V Conferencing Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00d6e-118"><strong>CorrelationID</strong></span><span class="sxs-lookup"><span data-stu-id="00d6e-118"><strong>CorrelationID</strong></span></span></p></td>
<td><p><span data-ttu-id="00d6e-119">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="00d6e-119">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="00d6e-120">一意</span><span class="sxs-lookup"><span data-stu-id="00d6e-120">Unique</span></span></p></td>
<td><p><span data-ttu-id="00d6e-121">関連付けられているセッションは、関連付け ID が同じになります。</span><span class="sxs-lookup"><span data-stu-id="00d6e-121">Sessions that are correlated will have the same correlation ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00d6e-122"><strong>Nextupdatupdat</strong></span><span class="sxs-lookup"><span data-stu-id="00d6e-122"><strong>NextUpdateTS</strong></span></span></p></td>
<td><p><span data-ttu-id="00d6e-123">datetime</span><span class="sxs-lookup"><span data-stu-id="00d6e-123">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="00d6e-124">内部使用のみ。</span><span class="sxs-lookup"><span data-stu-id="00d6e-124">For internal use only.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="00d6e-125">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="00d6e-125">


</div>

<span> </span>

</div>

</div>

</span></span></div>

