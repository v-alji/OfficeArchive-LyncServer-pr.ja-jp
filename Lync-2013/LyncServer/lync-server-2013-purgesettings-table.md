---
title: 'Lync Server 2013: PurgeSettings テーブル'
description: 'Lync Server 2013: PurgeSettings テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: PurgeSettings table
ms:assetid: 9ff2c8fc-4ae8-4f22-96a8-1f4d5eecbf2d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205121(v=OCS.15)
ms:contentKeyID: 48184932
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1ec2d1508d8362988bddbab2fe7303a23a8ee2d8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399014"
---
# <a name="purgesettings-table-in-lync-server-2013"></a><span data-ttu-id="b8ac5-103">Lync Server 2013 の PurgeSettings テーブル</span><span class="sxs-lookup"><span data-stu-id="b8ac5-103">PurgeSettings table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b8ac5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b8ac5-104">

<span> </span></span></span>

<span data-ttu-id="b8ac5-105">_**最終更新日:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="b8ac5-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="b8ac5-106">PurgeSettings テーブルには、古い通話の詳細レコードが CDR データベースから自動的に削除されるかどうかを指定する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b8ac5-106">The PurgeSettings table contains information that specifies if (and when) outdated call detail records will automatically be deleted from the CDR database.</span></span> <span data-ttu-id="b8ac5-107">また、次のコマンドを実行することで、Microsoft Lync Server 2013 管理シェル内からパージに関連する情報を取得することもできます。</span><span class="sxs-lookup"><span data-stu-id="b8ac5-107">Note that purging-related information can also be obtained from within the Microsoft Lync Server 2013 Management Shell by running the following command:</span></span>

    Get-CsCdrConfiguration

<span data-ttu-id="b8ac5-108">管理者は、PurgeSettings テーブルを読み取り専用として扱う必要があります。呼び出しの詳細の消去設定への変更は、 [CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsCdrConfiguration) または [CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsCdrConfiguration) コマンドレットを使用して行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8ac5-108">Administrators should treat the PurgeSettings table as read-only: changes to the call detail purge settings should only be made using the [New-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsCdrConfiguration) or [Set-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsCdrConfiguration) cmdlets.</span></span>

<span data-ttu-id="b8ac5-109">この表は、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="b8ac5-109">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b8ac5-110">列</span><span class="sxs-lookup"><span data-stu-id="b8ac5-110">Column</span></span></th>
<th><span data-ttu-id="b8ac5-111">データ型</span><span class="sxs-lookup"><span data-stu-id="b8ac5-111">Data Type</span></span></th>
<th><span data-ttu-id="b8ac5-112">キー/インデックス</span><span class="sxs-lookup"><span data-stu-id="b8ac5-112">Key/Index</span></span></th>
<th><span data-ttu-id="b8ac5-113">詳細</span><span class="sxs-lookup"><span data-stu-id="b8ac5-113">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b8ac5-114"><strong>ID</strong></span><span class="sxs-lookup"><span data-stu-id="b8ac5-114"><strong>Id</strong></span></span></p></td>
<td><p><span data-ttu-id="b8ac5-115">int</span><span class="sxs-lookup"><span data-stu-id="b8ac5-115">int</span></span></p></td>
<td><p><span data-ttu-id="b8ac5-116">Primary</span><span class="sxs-lookup"><span data-stu-id="b8ac5-116">Primary</span></span></p></td>
<td><p><span data-ttu-id="b8ac5-117">CDR 消去設定のコレクションの一意の識別子です。</span><span class="sxs-lookup"><span data-stu-id="b8ac5-117">Unique identifier for the collection of CDR purge settings.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8ac5-118"><strong>EnablePurge</strong></span><span class="sxs-lookup"><span data-stu-id="b8ac5-118"><strong>EnablePurge</strong></span></span></p></td>
<td><p><span data-ttu-id="b8ac5-119">bit</span><span class="sxs-lookup"><span data-stu-id="b8ac5-119">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b8ac5-120">True に設定すると (1) Microsoft Lync Server 2013 は、古いレコードを CDR データベースから定期的に削除します。</span><span class="sxs-lookup"><span data-stu-id="b8ac5-120">When set to True (1) Microsoft Lync Server 2013 will periodically purge outdated records from the CDR database.</span></span> <span data-ttu-id="b8ac5-121">パージは、PurgeHour 設定によって指定されたサントメで毎日行われます。</span><span class="sxs-lookup"><span data-stu-id="b8ac5-121">Purging will take place each day at the tome specified by the PurgeHour setting.</span></span> <span data-ttu-id="b8ac5-122">False (0) に設定すると、レコードはデータベースから自動的に削除されません。</span><span class="sxs-lookup"><span data-stu-id="b8ac5-122">If set to False (0) then records will not be automatically purged from the database.</span></span> <span data-ttu-id="b8ac5-123">既定値は True です。</span><span class="sxs-lookup"><span data-stu-id="b8ac5-123">The default value is True.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8ac5-124"><strong>KeepCallDetailForDays</strong></span><span class="sxs-lookup"><span data-stu-id="b8ac5-124"><strong>KeepCallDetailForDays</strong></span></span></p></td>
<td><p><span data-ttu-id="b8ac5-125">int</span><span class="sxs-lookup"><span data-stu-id="b8ac5-125">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b8ac5-126">データベースから削除される CDR レコード (日数) を指定します。 [削除] が有効になっていると、この値よりも古い CDR レコードがデータベースから削除されます。</span><span class="sxs-lookup"><span data-stu-id="b8ac5-126">Specifies the age of CDR records (in days) that will be purged from the database: if purging is enabled, CDR records older than this value will be removed from the database.</span></span> <span data-ttu-id="b8ac5-127">既定値は60日です。</span><span class="sxs-lookup"><span data-stu-id="b8ac5-127">The default value is 60 days.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8ac5-128"><strong>KeepErrorReportForDays</strong></span><span class="sxs-lookup"><span data-stu-id="b8ac5-128"><strong>KeepErrorReportForDays</strong></span></span></p></td>
<td><p><span data-ttu-id="b8ac5-129">int</span><span class="sxs-lookup"><span data-stu-id="b8ac5-129">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b8ac5-130">データベースから削除されるエラーレポートレコード (日数) を指定します。 [削除] を有効にすると、この値よりも古いエラーレポートレコードがデータベースから削除されます。</span><span class="sxs-lookup"><span data-stu-id="b8ac5-130">Specifies the age of error report records (in days) that will be purged from the database: if purging is enabled, error report records older than this value will be removed from the database.</span></span> <span data-ttu-id="b8ac5-131">既定値は60日です。</span><span class="sxs-lookup"><span data-stu-id="b8ac5-131">The default value is 60 days.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8ac5-132"><strong>PurgeHour</strong></span><span class="sxs-lookup"><span data-stu-id="b8ac5-132"><strong>PurgeHour</strong></span></span></p></td>
<td><p><span data-ttu-id="b8ac5-133">int</span><span class="sxs-lookup"><span data-stu-id="b8ac5-133">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b8ac5-134">データベースの消去が行われるローカル時刻を指定します。</span><span class="sxs-lookup"><span data-stu-id="b8ac5-134">Specifies the local time of day when database purging will take place.</span></span> <span data-ttu-id="b8ac5-135">時刻は24時間制を使用して指定します。0は午前0時 (12:00 AM)、23は 11:00 PM を表します。</span><span class="sxs-lookup"><span data-stu-id="b8ac5-135">The time of day is specified using a 24-hour clock, with 0 representing midnight (12:00 AM) and 23 representing 11:00 PM.</span></span> <span data-ttu-id="b8ac5-136">時刻を指定できるのは1日の時間のみです。10の値 (10:00 AM) は許可されていますが、10.5 の 10:30 (10:30 AM を示す) は使用できません。</span><span class="sxs-lookup"><span data-stu-id="b8ac5-136">Note that you can only specify the hour of the day: a value of 10 (indicating 10:00 AM) is allowed, but a value of 10:30 of 10.5 (indicating 10:30 AM) is not allowed.</span></span> <span data-ttu-id="b8ac5-137">既定値は 2 (2:00 AM) です。</span><span class="sxs-lookup"><span data-stu-id="b8ac5-137">The default value is 2 (2:00 AM).</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b8ac5-138">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b8ac5-138">


</div>

<span> </span>

</div>

</div>

</span></span></div>

