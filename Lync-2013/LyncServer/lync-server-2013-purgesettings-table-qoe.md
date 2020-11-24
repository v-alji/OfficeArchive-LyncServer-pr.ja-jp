---
title: 'Lync Server 2013: PurgeSettings table (QoE)'
description: 'Lync Server 2013: PurgeSettings table (QoE)。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: PurgeSettings table (QoE)
ms:assetid: 31b85d1c-3f32-4f67-94bf-9389cdd282c5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204788(v=OCS.15)
ms:contentKeyID: 48183777
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d515d799a7cc442dc6d34f2ece1a968de51cdad6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399015"
---
# <a name="purgesettings-table-qoe-in-lync-server-2013"></a><span data-ttu-id="9d6e8-103">Lync Server 2013 の PurgeSettings テーブル (QoE)</span><span class="sxs-lookup"><span data-stu-id="9d6e8-103">PurgeSettings table (QoE) in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9d6e8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9d6e8-104">

<span> </span></span></span>

<span data-ttu-id="9d6e8-105">_**最終更新日:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="9d6e8-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="9d6e8-106">PurgeSettings テーブルには、古い品質のエクスペリエンスレコードが QoE データベースから自動的に削除されるかどうかを指定する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9d6e8-106">The PurgeSettings table contains information that specifies if (and when) outdated Quality of Experience records will automatically be deleted from the QoE database.</span></span> <span data-ttu-id="9d6e8-107">また、次のコマンドを実行することで、Microsoft Lync Server 2013 管理シェル内からパージに関連する情報を取得することもできます。</span><span class="sxs-lookup"><span data-stu-id="9d6e8-107">Note that purging-related information can also be obtained from within the Microsoft Lync Server 2013 Management Shell by running the following command:</span></span>

    Get-CsQoEConfiguration

<span data-ttu-id="9d6e8-108">この表は、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="9d6e8-108">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9d6e8-109"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="9d6e8-109"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="9d6e8-110"><strong>データ型</strong></span><span class="sxs-lookup"><span data-stu-id="9d6e8-110"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="9d6e8-111"><strong>キー/インデックス</strong></span><span class="sxs-lookup"><span data-stu-id="9d6e8-111"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="9d6e8-112"><strong>詳細</strong></span><span class="sxs-lookup"><span data-stu-id="9d6e8-112"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9d6e8-113"><strong>ID</strong></span><span class="sxs-lookup"><span data-stu-id="9d6e8-113"><strong>ID</strong></span></span></p></td>
<td><p><span data-ttu-id="9d6e8-114">int</span><span class="sxs-lookup"><span data-stu-id="9d6e8-114">int</span></span></p></td>
<td><p><span data-ttu-id="9d6e8-115">Primary</span><span class="sxs-lookup"><span data-stu-id="9d6e8-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="9d6e8-116">QoE の消去設定のコレクションの一意の識別子です。</span><span class="sxs-lookup"><span data-stu-id="9d6e8-116">Unique identifier for the collection of QoE purge settings.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d6e8-117"><strong>EnablePurge</strong></span><span class="sxs-lookup"><span data-stu-id="9d6e8-117"><strong>EnablePurge</strong></span></span></p></td>
<td><p><span data-ttu-id="9d6e8-118">bit</span><span class="sxs-lookup"><span data-stu-id="9d6e8-118">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9d6e8-119">True (1) に設定すると、Microsoft Lync Server 2013 は、古いレコードを QoE データベースから定期的に削除します。</span><span class="sxs-lookup"><span data-stu-id="9d6e8-119">When set to True (1) Microsoft Lync Server 2013 will periodically purge outdated records from the QoE database.</span></span> <span data-ttu-id="9d6e8-120">パージは、PurgeHour 設定によって指定されたサントメで毎日行われます。</span><span class="sxs-lookup"><span data-stu-id="9d6e8-120">Purging will take place each day at the tome specified by the PurgeHour setting.</span></span> <span data-ttu-id="9d6e8-121">False (0) に設定すると、レコードはデータベースから自動的に削除されません。</span><span class="sxs-lookup"><span data-stu-id="9d6e8-121">If set to False (0) then records will not be automatically purged from the database.</span></span> <span data-ttu-id="9d6e8-122">既定値は True です。</span><span class="sxs-lookup"><span data-stu-id="9d6e8-122">The default value is True.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d6e8-123"><strong>KeepQoEDataForDays</strong></span><span class="sxs-lookup"><span data-stu-id="9d6e8-123"><strong>KeepQoEDataForDays</strong></span></span></p></td>
<td><p><span data-ttu-id="9d6e8-124">int</span><span class="sxs-lookup"><span data-stu-id="9d6e8-124">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9d6e8-125">データベースから削除される QoE レコード (日数) を指定します。 [削除] が有効になっていると、この値よりも古い QoE レコードはデータベースから削除されます。</span><span class="sxs-lookup"><span data-stu-id="9d6e8-125">Specifies the age of QoE records (in days) that will be purged from the database: if purging is enabled, QoE records older than this value will be removed from the database.</span></span> <span data-ttu-id="9d6e8-126">既定値は60日です。</span><span class="sxs-lookup"><span data-stu-id="9d6e8-126">The default value is 60 days.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d6e8-127"><strong>PurgeHour</strong></span><span class="sxs-lookup"><span data-stu-id="9d6e8-127"><strong>PurgeHour</strong></span></span></p></td>
<td><p><span data-ttu-id="9d6e8-128">int</span><span class="sxs-lookup"><span data-stu-id="9d6e8-128">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9d6e8-129">データベースの消去が行われるローカル時刻を指定します。</span><span class="sxs-lookup"><span data-stu-id="9d6e8-129">Specifies the local time of day when database purging will take place.</span></span> <span data-ttu-id="9d6e8-130">時刻は24時間制を使用して指定します。0は午前0時 (12:00 AM)、23は 11:00 PM を表します。</span><span class="sxs-lookup"><span data-stu-id="9d6e8-130">The time of day is specified using a 24-hour clock, with 0 representing midnight (12:00 AM) and 23 representing 11:00 PM.</span></span> <span data-ttu-id="9d6e8-131">時刻を指定できるのは1日の時間のみです。10の値 (10:00 AM) は許可されていますが、10.5 の 10:30 (10:30 AM を示す) は使用できません。</span><span class="sxs-lookup"><span data-stu-id="9d6e8-131">Note that you can only specify the hour of the day: a value of 10 (indicating 10:00 AM) is allowed, but a value of 10:30 of 10.5 (indicating 10:30 AM) is not allowed.</span></span> <span data-ttu-id="9d6e8-132">既定値は 1 (1:00 AM) です。</span><span class="sxs-lookup"><span data-stu-id="9d6e8-132">The default value is 1 (1:00 AM).</span></span> <span data-ttu-id="9d6e8-133">データベースの消去が行われるローカル時刻を指定します。</span><span class="sxs-lookup"><span data-stu-id="9d6e8-133">Specifies the local time of day when database purging will take place.</span></span> <span data-ttu-id="9d6e8-134">時刻は24時間制を使用して指定します。0は午前0時 (12:00 AM)、23は 11:00 PM を表します。</span><span class="sxs-lookup"><span data-stu-id="9d6e8-134">The time of day is specified using a 24-hour clock, with 0 representing midnight (12:00 AM) and 23 representing 11:00 PM.</span></span> <span data-ttu-id="9d6e8-135">時刻を指定できるのは1日の時間のみです。10の値 (10:00 AM) は許可されていますが、10.5 の 10:30 (10:30 AM を示す) は使用できません。</span><span class="sxs-lookup"><span data-stu-id="9d6e8-135">Note that you can only specify the hour of the day: a value of 10 (indicating 10:00 AM) is allowed, but a value of 10:30 of 10.5 (indicating 10:30 AM) is not allowed.</span></span> <span data-ttu-id="9d6e8-136">既定値は 1 (1:00 AM) です。</span><span class="sxs-lookup"><span data-stu-id="9d6e8-136">The default value is 1 (1:00 AM).</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="9d6e8-137">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9d6e8-137">


</div>

<span> </span>

</div>

</div>

</span></span></div>

