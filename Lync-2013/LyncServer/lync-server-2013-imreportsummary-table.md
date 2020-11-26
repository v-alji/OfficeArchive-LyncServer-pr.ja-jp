---
title: 'Lync Server 2013: IMReportSummary テーブル'
description: 'Lync Server 2013: IMReportSummary テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: IMReportSummary table
ms:assetid: 27ff9453-53f2-4fae-b637-70a086c9df96
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204753(v=OCS.15)
ms:contentKeyID: 48183673
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dfafa81d1605845b29a3627321fcbc0f72ca7ac7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427314"
---
# <a name="imreportsummary-table-in-lync-server-2013"></a><span data-ttu-id="a65a6-103">Lync Server 2013 の IMReportSummary テーブル</span><span class="sxs-lookup"><span data-stu-id="a65a6-103">IMReportSummary table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a65a6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a65a6-104">

<span> </span></span></span>

<span data-ttu-id="a65a6-105">_**最終更新日:** 2012-08-20_</span><span class="sxs-lookup"><span data-stu-id="a65a6-105">_**Topic Last Modified:** 2012-08-20_</span></span>

<span data-ttu-id="a65a6-106">Imreportの概要表は、組織内で開催されたインスタントメッセージセッションに関する全体的なレポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="a65a6-106">The IMReportSummaryTable provides an overall report on the instant messaging sessions held in an organization.</span></span> <span data-ttu-id="a65a6-107">この表は、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="a65a6-107">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a65a6-108">列</span><span class="sxs-lookup"><span data-stu-id="a65a6-108">Column</span></span></th>
<th><span data-ttu-id="a65a6-109">データ型</span><span class="sxs-lookup"><span data-stu-id="a65a6-109">Data Type</span></span></th>
<th><span data-ttu-id="a65a6-110">キー/インデックス</span><span class="sxs-lookup"><span data-stu-id="a65a6-110">Key/Index</span></span></th>
<th><span data-ttu-id="a65a6-111">詳細</span><span class="sxs-lookup"><span data-stu-id="a65a6-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a65a6-112"><strong>StartTime</strong></span><span class="sxs-lookup"><span data-stu-id="a65a6-112"><strong>StartTime</strong></span></span></p></td>
<td><p><span data-ttu-id="a65a6-113">datetime</span><span class="sxs-lookup"><span data-stu-id="a65a6-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="a65a6-114">Primary</span><span class="sxs-lookup"><span data-stu-id="a65a6-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="a65a6-115">インスタントメッセージングセッションが開始された日付と時刻。</span><span class="sxs-lookup"><span data-stu-id="a65a6-115">Date and time that the instant messaging session began.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a65a6-116"><strong>期間</strong></span><span class="sxs-lookup"><span data-stu-id="a65a6-116"><strong>TimePeriod</strong></span></span></p></td>
<td><p><span data-ttu-id="a65a6-117">char (1)</span><span class="sxs-lookup"><span data-stu-id="a65a6-117">char(1)</span></span></p></td>
<td><p><span data-ttu-id="a65a6-118">Primary</span><span class="sxs-lookup"><span data-stu-id="a65a6-118">Primary</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a65a6-119"><strong>PoolFQDN</strong></span><span class="sxs-lookup"><span data-stu-id="a65a6-119"><strong>PoolFQDN</strong></span></span></p></td>
<td><p><span data-ttu-id="a65a6-120">nvarchar (257)</span><span class="sxs-lookup"><span data-stu-id="a65a6-120">nvarchar(257)</span></span></p></td>
<td><p><span data-ttu-id="a65a6-121">Primary</span><span class="sxs-lookup"><span data-stu-id="a65a6-121">Primary</span></span></p></td>
<td><p><span data-ttu-id="a65a6-122">セッションをホストしているプールの完全修飾ドメイン名。</span><span class="sxs-lookup"><span data-stu-id="a65a6-122">Fully qualified domain name of the pool hosting the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a65a6-123"><strong>AuthType</strong></span><span class="sxs-lookup"><span data-stu-id="a65a6-123"><strong>AuthType</strong></span></span></p></td>
<td><p><span data-ttu-id="a65a6-124">int</span><span class="sxs-lookup"><span data-stu-id="a65a6-124">int</span></span></p></td>
<td><p><span data-ttu-id="a65a6-125">Primary</span><span class="sxs-lookup"><span data-stu-id="a65a6-125">Primary</span></span></p></td>
<td><p><span data-ttu-id="a65a6-126">通話の優先度 (緊急または不急など)</span><span class="sxs-lookup"><span data-stu-id="a65a6-126">Priority (for example, urgent or non-urgent) of the call.</span></span> <span data-ttu-id="a65a6-127">優先度の情報は、 <a href="lync-server-2013-callpriorities-table.md">Lync Server 2013 の callpriorities テーブル</a>に格納されています。</span><span class="sxs-lookup"><span data-stu-id="a65a6-127">Priority information is stored in the <a href="lync-server-2013-callpriorities-table.md">CallPriorities table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a65a6-128"><strong>SessionCount</strong></span><span class="sxs-lookup"><span data-stu-id="a65a6-128"><strong>SessionCount</strong></span></span></p></td>
<td><p><span data-ttu-id="a65a6-129">bigint</span><span class="sxs-lookup"><span data-stu-id="a65a6-129">bigint</span></span></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a65a6-130"><strong>MsgCount</strong></span><span class="sxs-lookup"><span data-stu-id="a65a6-130"><strong>MsgCount</strong></span></span></p></td>
<td><p><span data-ttu-id="a65a6-131">bigint</span><span class="sxs-lookup"><span data-stu-id="a65a6-131">bigint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a65a6-132">セッション中に交換されたインスタントメッセージの合計数です。</span><span class="sxs-lookup"><span data-stu-id="a65a6-132">Total number of instant messages exchanged during the session.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="a65a6-133">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a65a6-133">


</div>

<span> </span>

</div>

</div>

</span></span></div>

