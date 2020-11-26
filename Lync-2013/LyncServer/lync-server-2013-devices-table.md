---
title: 'Lync Server 2013: Devices テーブル'
description: 'Lync Server 2013: Devices テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Devices table
ms:assetid: 532e2280-4bbc-4a6c-93da-45d9f80a30a0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398351(v=OCS.15)
ms:contentKeyID: 48184169
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 763e1788e2874f9f9831c089ffe8fa077621b030
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429340"
---
# <a name="devices-table-in-lync-server-2013"></a><span data-ttu-id="2e6d4-103">Lync Server 2013 の Devices テーブル</span><span class="sxs-lookup"><span data-stu-id="2e6d4-103">Devices table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2e6d4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2e6d4-104">

<span> </span></span></span>

<span data-ttu-id="2e6d4-105">_**最終更新日:** 2012-05-25_</span><span class="sxs-lookup"><span data-stu-id="2e6d4-105">_**Topic Last Modified:** 2012-05-25_</span></span>

<span data-ttu-id="2e6d4-106">Devices テーブルは、サポートテーブルです。</span><span class="sxs-lookup"><span data-stu-id="2e6d4-106">The Devices table is a supporting table.</span></span> <span data-ttu-id="2e6d4-107">各レコードには、1つのデバイス (卓上電話) に関する情報が格納されます。</span><span class="sxs-lookup"><span data-stu-id="2e6d4-107">Each record stores information about one device (desk phone).</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2e6d4-108">列</span><span class="sxs-lookup"><span data-stu-id="2e6d4-108">Column</span></span></th>
<th><span data-ttu-id="2e6d4-109">データ型</span><span class="sxs-lookup"><span data-stu-id="2e6d4-109">Data Type</span></span></th>
<th><span data-ttu-id="2e6d4-110">キー/インデックス</span><span class="sxs-lookup"><span data-stu-id="2e6d4-110">Key/Index</span></span></th>
<th><span data-ttu-id="2e6d4-111">詳細</span><span class="sxs-lookup"><span data-stu-id="2e6d4-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2e6d4-112"><strong>DeviceId</strong></span><span class="sxs-lookup"><span data-stu-id="2e6d4-112"><strong>DeviceId</strong></span></span></p></td>
<td><p><span data-ttu-id="2e6d4-113">int</span><span class="sxs-lookup"><span data-stu-id="2e6d4-113">int</span></span></p></td>
<td><p><span data-ttu-id="2e6d4-114">Primary</span><span class="sxs-lookup"><span data-stu-id="2e6d4-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="2e6d4-115">このハードウェアバージョンを識別する一意の番号。</span><span class="sxs-lookup"><span data-stu-id="2e6d4-115">Unique number identifying this hardware version.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e6d4-116"><strong>Manufacturerid]</strong></span><span class="sxs-lookup"><span data-stu-id="2e6d4-116"><strong>ManufacturerId</strong></span></span></p></td>
<td><p><span data-ttu-id="2e6d4-117">int</span><span class="sxs-lookup"><span data-stu-id="2e6d4-117">int</span></span></p></td>
<td><p><span data-ttu-id="2e6d4-118">外部</span><span class="sxs-lookup"><span data-stu-id="2e6d4-118">Foreign</span></span></p></td>
<td><p><span data-ttu-id="2e6d4-119">このデバイスの製造元。</span><span class="sxs-lookup"><span data-stu-id="2e6d4-119">Manufacturer of this device.</span></span> <span data-ttu-id="2e6d4-120">詳細については、「 <a href="lync-server-2013-manufacturers-table.md">Lync Server 2013 の製造元の表</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2e6d4-120">See the <a href="lync-server-2013-manufacturers-table.md">Manufacturers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e6d4-121"><strong>ハードウェアの Versionid</strong></span><span class="sxs-lookup"><span data-stu-id="2e6d4-121"><strong>HardwareVersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="2e6d4-122">int</span><span class="sxs-lookup"><span data-stu-id="2e6d4-122">int</span></span></p></td>
<td><p><span data-ttu-id="2e6d4-123">外部</span><span class="sxs-lookup"><span data-stu-id="2e6d4-123">Foreign</span></span></p></td>
<td><p><span data-ttu-id="2e6d4-124">このデバイスのハードウェアバージョン。</span><span class="sxs-lookup"><span data-stu-id="2e6d4-124">Hardware version of this device.</span></span> <span data-ttu-id="2e6d4-125">詳細については、「 <a href="lync-server-2013-hardwareversions-table.md">Lync Server 2013 のハードウェアバージョンの表</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2e6d4-125">See the <a href="lync-server-2013-hardwareversions-table.md">HardwareVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e6d4-126"><strong>MacAddress</strong></span><span class="sxs-lookup"><span data-stu-id="2e6d4-126"><strong>MacAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="2e6d4-127">bigint</span><span class="sxs-lookup"><span data-stu-id="2e6d4-127">bigint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="2e6d4-128">MAC アドレス</span><span class="sxs-lookup"><span data-stu-id="2e6d4-128">MAC Address</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="2e6d4-129">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2e6d4-129">


</div>

<span> </span>

</div>

</div>

</span></span></div>

