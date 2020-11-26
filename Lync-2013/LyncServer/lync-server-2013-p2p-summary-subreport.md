---
title: 'Lync Server 2013: P2P Summary サブレポート'
description: 'Lync Server 2013: P2P Summary サブレポート。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: P2P Summary Subreport
ms:assetid: fc36185a-3cc5-4167-8c93-8a755fa75ac7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205416(v=OCS.15)
ms:contentKeyID: 48185950
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: eda51e76c4ed7b62535a2a2e4ab52982aa6381f3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424703"
---
# <a name="p2p-summary-subreport-in-lync-server-2013"></a><span data-ttu-id="66999-103">Lync Server 2013 の P2P Summary サブレポート</span><span class="sxs-lookup"><span data-stu-id="66999-103">P2P Summary Subreport in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="66999-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="66999-104">

<span> </span></span></span>

<span data-ttu-id="66999-105">_**最終更新日:** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="66999-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="66999-106">P2P 概要サブレポートは、エラーが発生したピアツーピア セッションの総合的な概要を示します。</span><span class="sxs-lookup"><span data-stu-id="66999-106">The P2P Summary Subreport provides an overall view of your failed peer-to-peer communication sessions.</span></span>

<div>

## <a name="filters"></a><span data-ttu-id="66999-107">フィルター</span><span class="sxs-lookup"><span data-stu-id="66999-107">Filters</span></span>

<span data-ttu-id="66999-p101">フィルターは、細かく絞り込んだデータ セットを返したり、返されたデータをさまざまな方法で表示したりする方法として利用できます。次の表に、P2P 概要サブレポートで使用できるフィルターを示します。</span><span class="sxs-lookup"><span data-stu-id="66999-p101">Filters provide a way for you to return a more finely targeted set of data or to view the returned data in different ways. The following table lists the filters that you can use with the P2P Summary Subreport.</span></span>

### <a name="p2p-summary-subreport-filters"></a><span data-ttu-id="66999-110">P2P 概要サブレポートのフィルター</span><span class="sxs-lookup"><span data-stu-id="66999-110">P2P Summary Subreport Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="66999-111">名前</span><span class="sxs-lookup"><span data-stu-id="66999-111">Name</span></span></th>
<th><span data-ttu-id="66999-112">説明</span><span class="sxs-lookup"><span data-stu-id="66999-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="66999-113"><strong>開始</strong></span><span class="sxs-lookup"><span data-stu-id="66999-113"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="66999-p102">時間範囲の開始日と開始時刻。データを時間単位で表示するには、次のように開始日と開始時刻の両方を入力します。</span><span class="sxs-lookup"><span data-stu-id="66999-p102">Start date and time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="66999-116">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="66999-116">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="66999-p103">開始時刻を入力しないと、レポートは自動的に指定日の午前 12:00 に開始します。データを日単位で表示するには、次のように日付のみを入力します。</span><span class="sxs-lookup"><span data-stu-id="66999-p103">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="66999-119">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="66999-119">7/7/2012</span></span></p>
<p><span data-ttu-id="66999-120">週単位または月単位で表示するには、表示する週または月の任意の日付を入力します (その週または月の最初の日である必要はありません)。</span><span class="sxs-lookup"><span data-stu-id="66999-120">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="66999-121">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="66999-121">7/3/2012</span></span></p>
<p><span data-ttu-id="66999-122">一週間は、日曜日から始まり、土曜日で終わるものとします。</span><span class="sxs-lookup"><span data-stu-id="66999-122">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66999-123"><strong>終了</strong></span><span class="sxs-lookup"><span data-stu-id="66999-123"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="66999-p104">時間範囲の終了日と終了時刻。データを時間単位で表示するには、次のように終了日と終了時刻の両方を入力します。</span><span class="sxs-lookup"><span data-stu-id="66999-p104">End date and time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="66999-126">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="66999-126">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="66999-p105">終了時刻を入力しないと、レポートは自動的に指定日の午前 12:00 に終了します。データを日単位で表示するには、次のように日付のみを入力します。</span><span class="sxs-lookup"><span data-stu-id="66999-p105">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="66999-129">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="66999-129">7/7/2012</span></span></p>
<p><span data-ttu-id="66999-130">週単位または月単位で表示するには、表示する週または月の任意の日付を入力します (その週または月の最初の日である必要はありません)。</span><span class="sxs-lookup"><span data-stu-id="66999-130">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="66999-131">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="66999-131">7/3/2012</span></span></p>
<p><span data-ttu-id="66999-132">一週間は、日曜日から始まり、土曜日で終わるものとします。</span><span class="sxs-lookup"><span data-stu-id="66999-132">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66999-133"><strong>プール</strong></span><span class="sxs-lookup"><span data-stu-id="66999-133"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="66999-p106">レジストラー プールまたはエッジ サーバーの完全修飾ドメイン名 (FQDN)。個別のプールを選択するか、[<strong>すべて</strong>] をクリックしてすべてのプールのデータを表示できます。このドロップダウン リストは、データベース内のレコードに基づいて自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="66999-p106">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server. You can either select an individual pool or click <strong>[All]</strong> to view data for all the pools. This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="66999-137">指標</span><span class="sxs-lookup"><span data-stu-id="66999-137">Metrics</span></span>

<span data-ttu-id="66999-138">次の表に、P2P 概要サブレポートで提供される情報を示します。</span><span class="sxs-lookup"><span data-stu-id="66999-138">The following table lists the information provided in the P2P Summary Subreport.</span></span>

### <a name="p2p-summary-subreport-metrics"></a><span data-ttu-id="66999-139">P2P 概要サブレポートの指標</span><span class="sxs-lookup"><span data-stu-id="66999-139">P2P Summary Subreport Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="66999-140">名前</span><span class="sxs-lookup"><span data-stu-id="66999-140">Name</span></span></th>
<th><span data-ttu-id="66999-141">この項目での並べ替え</span><span class="sxs-lookup"><span data-stu-id="66999-141">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="66999-142">説明</span><span class="sxs-lookup"><span data-stu-id="66999-142">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="66999-143"><strong>セッションの合計数</strong></span><span class="sxs-lookup"><span data-stu-id="66999-143"><strong>Total sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="66999-144">不可</span><span class="sxs-lookup"><span data-stu-id="66999-144">No</span></span></p></td>
<td><p><span data-ttu-id="66999-145">セッションの総数です。成功したセッション、失敗したセッション (予期されるエラーと予期しないエラーの両方)、およびどちらにも分類されないセッションを含みます。</span><span class="sxs-lookup"><span data-stu-id="66999-145">Total number of sessions, including successful sessions, failed sessions (both expected failures and unexpected failures), and uncategorized sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66999-146"><strong>エラー率</strong></span><span class="sxs-lookup"><span data-stu-id="66999-146"><strong>Failure rate</strong></span></span></p></td>
<td><p><span data-ttu-id="66999-147">不可</span><span class="sxs-lookup"><span data-stu-id="66999-147">No</span></span></p></td>
<td><p><span data-ttu-id="66999-148">エラーが発生したピアツーピア セッションの割合です。</span><span class="sxs-lookup"><span data-stu-id="66999-148">Percentage of peer-to-peer sessions that failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66999-149"><strong>セッション (モダリティ別)</strong></span><span class="sxs-lookup"><span data-stu-id="66999-149"><strong>Sessions by Modality</strong></span></span></p></td>
<td><p><span data-ttu-id="66999-150">不可</span><span class="sxs-lookup"><span data-stu-id="66999-150">No</span></span></p></td>
<td><p><span data-ttu-id="66999-151">モダリティによってグループ化されたセッションの合計数 (たとえば、インスタント メッセージング)。</span><span class="sxs-lookup"><span data-stu-id="66999-151">Total number of sessions grouped by modality (for example, instant messaging).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66999-152"><strong>エラー率 (モダリティ別)</strong></span><span class="sxs-lookup"><span data-stu-id="66999-152"><strong>Failure rate by modality</strong></span></span></p></td>
<td><p><span data-ttu-id="66999-153">不可</span><span class="sxs-lookup"><span data-stu-id="66999-153">No</span></span></p></td>
<td><p><span data-ttu-id="66999-154">モダリティによってグループ化された失敗したセッションの合計数 (たとえば、インスタント メッセージング)。</span><span class="sxs-lookup"><span data-stu-id="66999-154">Total number of failed sessions grouped by modality (for example, instant messaging).</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="66999-155">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="66999-155">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

