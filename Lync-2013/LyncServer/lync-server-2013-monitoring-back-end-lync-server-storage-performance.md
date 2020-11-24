---
title: 'Lync Server 2013: バックエンドの Lync Server 記憶域のパフォーマンスを監視する'
description: 'Lync Server 2013: バックエンドの Lync Server 記憶域のパフォーマンスを監視しています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Monitoring back end Lync Server 2013 storage performance
ms:assetid: 71627c70-1953-4ac2-afbe-f3ad85be0f44
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720917(v=OCS.15)
ms:contentKeyID: 63969619
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e7501418d3589b941b7e92d2b414492c1d27a3ee
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398468"
---
# <a name="monitoring-back-end-lync-server-2013-storage-performance"></a><span data-ttu-id="5ee9f-103">バックエンドの Lync Server 2013 ストレージパフォーマンスの監視</span><span class="sxs-lookup"><span data-stu-id="5ee9f-103">Monitoring back end Lync Server 2013 storage performance</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5ee9f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5ee9f-104">

<span> </span></span></span>

<span data-ttu-id="5ee9f-105">_**最終更新日:** 2014-05-02_</span><span class="sxs-lookup"><span data-stu-id="5ee9f-105">_**Topic Last Modified:** 2014-05-02_</span></span>

<span data-ttu-id="5ee9f-106">Lync Server 2013 バックエンドデータベースは、Lync Server 2013 の展開において非常に重要な部分です。</span><span class="sxs-lookup"><span data-stu-id="5ee9f-106">The Lync Server 2013 back-end databases are a very important part of the Lync Server 2013 deployment.</span></span> <span data-ttu-id="5ee9f-107">Lync Server 2013 のバックエンドが最適に動作していることを確認するために、データベースとそれぞれのトランザクションログを定期的に監視することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="5ee9f-107">We recommend constantly monitoring the databases and respective transaction logs to help to make sure that the Lync Server 2013 back end is performing optimally.</span></span>

<span data-ttu-id="5ee9f-108">次の表は、記憶域のパフォーマンスに関する情報を確認するために監視する必要があるパフォーマンスカウンターを示しています。</span><span class="sxs-lookup"><span data-stu-id="5ee9f-108">The following table identifies performance counters that should be monitored to learn information about Storage Performance.</span></span> <span data-ttu-id="5ee9f-109">これらのカウンターのベースライン値は、システムの負荷が高すぎるときにパフォーマンスの変化を理解するために、最初に決定する必要があります (システムが通常、予想される負荷の場合)。</span><span class="sxs-lookup"><span data-stu-id="5ee9f-109">The baseline values for these counters must be determined first (when system is at its normal, expected load) to understand the performance changes when system is stressed.</span></span>

### <a name="performance-counters-to-be-monitored"></a><span data-ttu-id="5ee9f-110">監視対象のパフォーマンスカウンター</span><span class="sxs-lookup"><span data-stu-id="5ee9f-110">Performance counters to be monitored</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5ee9f-111">パフォーマンス カウンター</span><span class="sxs-lookup"><span data-stu-id="5ee9f-111">Performance Counter</span></span></th>
<th><span data-ttu-id="5ee9f-112">ベースラインのしきい値</span><span class="sxs-lookup"><span data-stu-id="5ee9f-112">Baseline thresholds</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5ee9f-113">トランザクション/秒 (RTC)</span><span class="sxs-lookup"><span data-stu-id="5ee9f-113">Transactions/sec (RTC)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ee9f-114">トランザクション/秒 (rtcdyn)</span><span class="sxs-lookup"><span data-stu-id="5ee9f-114">Transactions/sec (rtcdyn)</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ee9f-115">トランザクション/秒 (tempdb)</span><span class="sxs-lookup"><span data-stu-id="5ee9f-115">Transactions/sec (tempdb)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ee9f-116">ログのフラッシュ回数/秒 (RTC)</span><span class="sxs-lookup"><span data-stu-id="5ee9f-116">Log Flushes/sec (RTC)</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ee9f-117">ログのフラッシュ回数/秒 (rtcdyn)</span><span class="sxs-lookup"><span data-stu-id="5ee9f-117">Log Flushes/sec (rtcdyn)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ee9f-118">ログのフラッシュ回数/秒 (tempdb)</span><span class="sxs-lookup"><span data-stu-id="5ee9f-118">Log Flushes/sec (tempdb)</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ee9f-119">ディスク転送/秒 (読み取り + 書き込み)-RTC db</span><span class="sxs-lookup"><span data-stu-id="5ee9f-119">Disk Transfers/sec (read+write) - RTC db</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ee9f-120">ディスク転送/秒-RTC ログ</span><span class="sxs-lookup"><span data-stu-id="5ee9f-120">Disk Transfers/sec - RTC log</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ee9f-121">Disk 伝送/sec-rtcdyn db</span><span class="sxs-lookup"><span data-stu-id="5ee9f-121">Disk Transfers/sec - rtcdyn db</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ee9f-122">Disk 伝送/sec-rtcdyn ログ</span><span class="sxs-lookup"><span data-stu-id="5ee9f-122">Disk Transfers/sec - rtcdyn log</span></span></p></td>
<td></td>
</tr>
</tbody>
</table><span data-ttu-id="5ee9f-123">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5ee9f-123">


</div>

<span> </span>

</div>

</div>

</span></span></div>

