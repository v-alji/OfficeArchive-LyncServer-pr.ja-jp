---
title: 'Lync Server 2013: DeviceDriver テーブル'
description: 'Lync Server 2013: DeviceDriver テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DeviceDriver table
ms:assetid: ca91a0b4-98c0-49f6-af9d-7d0f8ac75f1a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398844(v=OCS.15)
ms:contentKeyID: 48185449
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3d81e2e27ff5196112c6057c429f924e5b1c3e4b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429354"
---
# <a name="devicedriver-table-in-lync-server-2013"></a><span data-ttu-id="4ac86-103">Lync Server 2013 の DeviceDriver テーブル</span><span class="sxs-lookup"><span data-stu-id="4ac86-103">DeviceDriver table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4ac86-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4ac86-104">

<span> </span></span></span>

<span data-ttu-id="4ac86-105">_**最終更新日:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="4ac86-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="4ac86-106">DeviceDriver テーブルはサポートされているテーブルです。</span><span class="sxs-lookup"><span data-stu-id="4ac86-106">The DeviceDriver table is a supporting table.</span></span> <span data-ttu-id="4ac86-107">各レコードは、キャプチャデバイスまたはレンダーデバイスのいずれかで使用されるドライバーを表します。</span><span class="sxs-lookup"><span data-stu-id="4ac86-107">Each record represents a driver used by either a capture device or render device.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4ac86-108"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="4ac86-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="4ac86-109"><strong>データ型</strong></span><span class="sxs-lookup"><span data-stu-id="4ac86-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="4ac86-110"><strong>キー/インデックス</strong></span><span class="sxs-lookup"><span data-stu-id="4ac86-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="4ac86-111"><strong>詳細</strong></span><span class="sxs-lookup"><span data-stu-id="4ac86-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4ac86-112"><strong>DeviceDriverKey</strong></span><span class="sxs-lookup"><span data-stu-id="4ac86-112"><strong>DeviceDriverKey</strong></span></span></p></td>
<td><p><span data-ttu-id="4ac86-113">int</span><span class="sxs-lookup"><span data-stu-id="4ac86-113">int</span></span></p></td>
<td><p><span data-ttu-id="4ac86-114">Primary</span><span class="sxs-lookup"><span data-stu-id="4ac86-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="4ac86-115">このデバイスドライバーレコードを識別する一意の番号です。</span><span class="sxs-lookup"><span data-stu-id="4ac86-115">Unique number identifying this device driver record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ac86-116"><strong>DeviceDriver</strong></span><span class="sxs-lookup"><span data-stu-id="4ac86-116"><strong>DeviceDriver</strong></span></span></p></td>
<td><p><span data-ttu-id="4ac86-117">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="4ac86-117">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="4ac86-118">一意</span><span class="sxs-lookup"><span data-stu-id="4ac86-118">unique</span></span></p></td>
<td><p><span data-ttu-id="4ac86-119">デバイスドライバ名。</span><span class="sxs-lookup"><span data-stu-id="4ac86-119">Device driver name.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="4ac86-120">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4ac86-120">


</div>

<span> </span>

</div>

</div>

</span></span></div>

