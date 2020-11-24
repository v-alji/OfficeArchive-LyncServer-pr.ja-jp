---
title: 'Lync Server 2013: 通話診断のサマリーレポート'
description: 'Lync Server 2013: 診断サマリーレポートを呼び出します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call Diagnostic Summary Report
ms:assetid: 9091de56-13e6-440e-9353-f57c10c906fe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615016(v=OCS.15)
ms:contentKeyID: 48184789
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b444a176c06974a9eb9827006e078c17b54047a3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49397995"
---
# <a name="call-diagnostic-summary-report-in-lync-server-2013"></a><span data-ttu-id="16764-103">Lync Server 2013 の通話診断サマリーレポート</span><span class="sxs-lookup"><span data-stu-id="16764-103">Call Diagnostic Summary Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="16764-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="16764-104">

<span> </span></span></span>

<span data-ttu-id="16764-105">_**最終更新日:** 2012-06-06_</span><span class="sxs-lookup"><span data-stu-id="16764-105">_**Topic Last Modified:** 2012-06-06_</span></span>

<span data-ttu-id="16764-p101">通話診断の概要レポートでは、失敗したピアツーピア セッションや会議セッションの概要を確認できます。このレポートでは、両方の種類のセッション全体のエラー率が表示され、エラー情報がセッション モダリティごとに分類されます。</span><span class="sxs-lookup"><span data-stu-id="16764-p101">The Call Diagnostic Summary Report provides an overall look at failed peer-to-peer and conferencing sessions. The report shows the overall failure rate for both types of sessions, and further breaks the failure information down by session modality type:</span></span>

  - <span data-ttu-id="16764-108">インスタント メッセージング</span><span class="sxs-lookup"><span data-stu-id="16764-108">Instant messaging</span></span>

  - <span data-ttu-id="16764-109">アプリケーション共有</span><span class="sxs-lookup"><span data-stu-id="16764-109">Application sharing</span></span>

  - <span data-ttu-id="16764-110">ファイル転送</span><span class="sxs-lookup"><span data-stu-id="16764-110">File transfer</span></span>

  - <span data-ttu-id="16764-111">音声</span><span class="sxs-lookup"><span data-stu-id="16764-111">Audio</span></span>

  - <span data-ttu-id="16764-112">ビデオ</span><span class="sxs-lookup"><span data-stu-id="16764-112">Video</span></span>

<div>

## <a name="accessing-the-call-diagnostic-summary-report"></a><span data-ttu-id="16764-113">通話診断の概要レポートへのアクセス</span><span class="sxs-lookup"><span data-stu-id="16764-113">Accessing the Call Diagnostic Summary Report</span></span>

<span data-ttu-id="16764-114">通話診断の概要レポートは、監視レポートのホームページからアクセスされます。</span><span class="sxs-lookup"><span data-stu-id="16764-114">The Call Diagnostic Summary Report is accessed from the Monitoring Reports Home page.</span></span> <span data-ttu-id="16764-115">通話診断の概要レポートでは、レポートの [ピアツーピアセッションの概要] セクションの下にある [エラー率] メトリックをクリックして、 [Lync Server 2013 のピアツーピアアクティビティ診断レポート](lync-server-2013-peer-to-peer-activity-diagnostic-report.md) にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="16764-115">From the Call Diagnostic Summary Report you can access the [Peer-to-Peer Activity Diagnostic Report in Lync Server 2013](lync-server-2013-peer-to-peer-activity-diagnostic-report.md) by clicking the Failure rate metric under the Peer-to-Peer Session Summary section of the report.</span></span> <span data-ttu-id="16764-116">[Lync Server 2013 の会議診断レポート](lync-server-2013-conference-diagnostic-report.md)にアクセスするには、次のいずれかの電話会議の指標をクリックする方法もあります。</span><span class="sxs-lookup"><span data-stu-id="16764-116">You can also access the [Conference Diagnostic Report in Lync Server 2013](lync-server-2013-conference-diagnostic-report.md) by clicking any of the following conference metrics:</span></span>

  - <span data-ttu-id="16764-117">全体的なセッション エラー率</span><span class="sxs-lookup"><span data-stu-id="16764-117">Overall session failure rate</span></span>

  - <span data-ttu-id="16764-118">フォーカス エラー率</span><span class="sxs-lookup"><span data-stu-id="16764-118">Focus failure rate</span></span>

  - <span data-ttu-id="16764-119">MCU エラー率</span><span class="sxs-lookup"><span data-stu-id="16764-119">MCU failure rate</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-call-diagnostic-summary-report"></a><span data-ttu-id="16764-120">通話診断の概要レポートの活用</span><span class="sxs-lookup"><span data-stu-id="16764-120">Making the Best Use of the Call Diagnostic Summary Report</span></span>

<span data-ttu-id="16764-121">通話診断の概要レポートには、Microsoft Lync Server 2013 で使用されているさまざまなモダリティのエラー率を比較するグラフが含まれています。</span><span class="sxs-lookup"><span data-stu-id="16764-121">The Call Diagnostic Summary Report includes graphs that compare failure rates for the various modalities used in Microsoft Lync Server 2013.</span></span> <span data-ttu-id="16764-122">これらのグラフの列は、実際にはホットリンクです。たとえば、ピアツーピアセッションのインスタントメッセージングの列をクリックすると、 [Lync Server 2013 のピアツーピアアクティビティ診断レポート](lync-server-2013-peer-to-peer-activity-diagnostic-report.md)のインスタンス (通話診断の概要レポートに含まれるすべてのインスタントメッセージングセッションの詳細情報を提供するレポート) が表示されます。</span><span class="sxs-lookup"><span data-stu-id="16764-122">The columns in these graphs are actually hotlinks; for example, if you click the Instant messaging column for peer-to-peer sessions, you'll drill down to an instance of the [Peer-to-Peer Activity Diagnostic Report in Lync Server 2013](lync-server-2013-peer-to-peer-activity-diagnostic-report.md), a report that provides additional details about all the instant messaging sessions included in the Call Diagnostic Summary Report.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="16764-123">フィルター</span><span class="sxs-lookup"><span data-stu-id="16764-123">Filters</span></span>

<span data-ttu-id="16764-p104">フィルターは、細かく絞り込んだデータ セットを返したり、返されたデータをさまざまな方法で表示したりする方法として利用できます。たとえば、通話診断の概要レポートでは、セッションで使用されるレジストラー プールやエッジ プールのような要素をフィルターできます。また、データをグループ化する方法を選択することもできます。この場合は、通話が、時間、日、週、または月の単位でグループ化されます。</span><span class="sxs-lookup"><span data-stu-id="16764-p104">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Call Diagnostic Summary Report enables you to filter on such things as the Registrar pool or Edge Server used in the session. You can also choose how data should be grouped. In this case, calls are grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="16764-128">次の表に、通話診断の概要レポートで使用できるフィルターを示します。</span><span class="sxs-lookup"><span data-stu-id="16764-128">The following table lists the filters that you can use with the Call Diagnostic Summary Report.</span></span>

### <a name="call-diagnostic-summary-report-filters"></a><span data-ttu-id="16764-129">通話診断の概要レポートのフィルター</span><span class="sxs-lookup"><span data-stu-id="16764-129">Call Diagnostic Summary Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="16764-130">名前</span><span class="sxs-lookup"><span data-stu-id="16764-130">Name</span></span></th>
<th><span data-ttu-id="16764-131">説明</span><span class="sxs-lookup"><span data-stu-id="16764-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="16764-132"><strong>開始</strong></span><span class="sxs-lookup"><span data-stu-id="16764-132"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="16764-p105">時間範囲の開始日と開始時刻。データを時間単位で表示するには、次のように開始日と開始時刻の両方を入力します。</span><span class="sxs-lookup"><span data-stu-id="16764-p105">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="16764-135">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="16764-135">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="16764-p106">開始時刻を入力しないと、レポートは自動的に指定日の午前 12:00 に開始します。データを日単位で表示するには、次のように日付のみを入力します。</span><span class="sxs-lookup"><span data-stu-id="16764-p106">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="16764-138">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="16764-138">7/7/2012</span></span></p>
<p><span data-ttu-id="16764-139">週単位または月単位で表示するには、表示する週または月の任意の日付を入力します (その週または月の最初の日である必要はありません)。</span><span class="sxs-lookup"><span data-stu-id="16764-139">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="16764-140">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="16764-140">7/3/2012</span></span></p>
<p><span data-ttu-id="16764-141">一週間は、日曜日から始まり、土曜日で終わるものとします。</span><span class="sxs-lookup"><span data-stu-id="16764-141">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16764-142"><strong>終了</strong></span><span class="sxs-lookup"><span data-stu-id="16764-142"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="16764-p107">時間範囲の終了日と終了時刻。データを時間単位で表示するには、次のように終了日と終了時刻の両方を入力します。</span><span class="sxs-lookup"><span data-stu-id="16764-p107">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="16764-145">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="16764-145">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="16764-p108">終了時刻を入力しないと、レポートは自動的に指定日の午前 12:00 に終了します。データを日単位で表示するには、次のように日付のみを入力します。</span><span class="sxs-lookup"><span data-stu-id="16764-p108">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="16764-148">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="16764-148">7/7/2012</span></span></p>
<p><span data-ttu-id="16764-149">週単位または月単位で表示するには、表示する週または月の任意の日付を入力します (その週または月の最初の日である必要はありません)。</span><span class="sxs-lookup"><span data-stu-id="16764-149">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="16764-150">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="16764-150">7/3/2012</span></span></p>
<p><span data-ttu-id="16764-151">一週間は、日曜日から始まり、土曜日で終わるものとします。</span><span class="sxs-lookup"><span data-stu-id="16764-151">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16764-152"><strong>[間隔]</strong></span><span class="sxs-lookup"><span data-stu-id="16764-152"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="16764-p109">時間間隔です。次のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="16764-p109">Time interval. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="16764-155">毎時 (最大 25 時間の表示が可能)</span><span class="sxs-lookup"><span data-stu-id="16764-155">Hourly (a maximum of 25 hours can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="16764-156">毎日 (最大 31 日の表示が可能)</span><span class="sxs-lookup"><span data-stu-id="16764-156">Daily (a maximum of 31 days can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="16764-157">毎週 (最大 12 週の表示が可能)</span><span class="sxs-lookup"><span data-stu-id="16764-157">Weekly (a maximum of 12 weeks can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="16764-158">毎月 (最大 12 か月の表示が可能)</span><span class="sxs-lookup"><span data-stu-id="16764-158">Monthly (a maximum of 12 months can be displayed)</span></span></p></li>
</ul>
<p><span data-ttu-id="16764-159">入力した開始日と終了日が選択した間隔で使用できる値の最大数を超える場合は、最大数の値 (開始日からカウント) のみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="16764-159">If the start and end dates exceed the maximum number of values allowed for the selected interval, only the maximum number of values (starting from the start date) is displayed.</span></span> <span data-ttu-id="16764-160">たとえば、開始日が7/7/2012 で、終了日が2/28/2012 の [日] 間隔を選択した場合は、8/7/2012 12:00 AM から 9/7/2012 12:00 AM (つまり、31日分のデータ) のデータが表示されます。</span><span class="sxs-lookup"><span data-stu-id="16764-160">For example, if you select the Daily interval with a start date of 7/7/2012 and an end date of 2/28/2012, data is displayed for the days 8/7/2012 12:00 AM to 9/7/2012 12:00 AM (that is, a total of 31 days' worth of data).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16764-161"><strong>プール</strong></span><span class="sxs-lookup"><span data-stu-id="16764-161"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="16764-p111">レジストラー プールまたはエッジ サーバーの完全修飾ドメイン名 (FQDN)。個別のプールを選択するか、[<strong>すべて</strong>] をクリックしてすべてのプールのデータを表示できます。このドロップダウン リストは、データベース内のレコードに基づいて自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="16764-p111">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server. You can either select an individual pool or click <strong>[All]</strong> to view data for all the pools. This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-peer-to-peer-sessions"></a><span data-ttu-id="16764-165">ピアツーピア セッションの指標</span><span class="sxs-lookup"><span data-stu-id="16764-165">Metrics for Peer-to-Peer Sessions</span></span>

<span data-ttu-id="16764-166">次の表に、ピアツーピア セッション (参加者が 2 人だけのセッション) の通話診断の概要レポートで提供される情報を示します。</span><span class="sxs-lookup"><span data-stu-id="16764-166">The following table lists the information provided in the Call Diagnostic Summary Report for peer-to-peer sessions (that is, sessions involving just two participants).</span></span>

### <a name="metrics-for-peer-to-peer-sessions"></a><span data-ttu-id="16764-167">ピアツーピア セッションの指標</span><span class="sxs-lookup"><span data-stu-id="16764-167">Metrics for Peer-to-Peer Sessions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="16764-168">名前</span><span class="sxs-lookup"><span data-stu-id="16764-168">Name</span></span></th>
<th><span data-ttu-id="16764-169">この項目での並べ替え</span><span class="sxs-lookup"><span data-stu-id="16764-169">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="16764-170">説明</span><span class="sxs-lookup"><span data-stu-id="16764-170">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="16764-171"><strong>セッションの合計数</strong></span><span class="sxs-lookup"><span data-stu-id="16764-171"><strong>Total sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="16764-172">不可</span><span class="sxs-lookup"><span data-stu-id="16764-172">No</span></span></p></td>
<td><p><span data-ttu-id="16764-173">実施されたピアツーピア セッションの総数です。</span><span class="sxs-lookup"><span data-stu-id="16764-173">Total number of peer-to-peer sessions conducted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16764-174"><strong>[エラー率]</strong></span><span class="sxs-lookup"><span data-stu-id="16764-174"><strong>Failure rate</strong></span></span></p></td>
<td><p><span data-ttu-id="16764-175">不可</span><span class="sxs-lookup"><span data-stu-id="16764-175">No</span></span></p></td>
<td><p><span data-ttu-id="16764-p112">エラーが発生したピアツーピア セッションの割合です。この項目をクリックすると、このレポートでは、エラーが発生したピアツーピア セッションに関する詳細情報を示すピアツーピア アクティビティ診断レポートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="16764-p112">Percentage of peer-to-peer sessions that failed. When you click this item, the report shows the Peer-to-Peer Activity Diagnostic report, which displays more detailed information about the failed peer-to-peer sessions.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-conferencing-sessions"></a><span data-ttu-id="16764-178">電話会議セッションの指標</span><span class="sxs-lookup"><span data-stu-id="16764-178">Metrics for Conferencing Sessions</span></span>

<span data-ttu-id="16764-179">次の表に、電話会議セッション (参加者が 3 人以上のセッション) の通話診断レポートで提供される情報を示します。</span><span class="sxs-lookup"><span data-stu-id="16764-179">The following table lists the information provided in the Call Diagnostic Report for conferencing sessions (that is, sessions involving three or more participants).</span></span>

### <a name="metrics-for-conferencing-sessions"></a><span data-ttu-id="16764-180">電話会議セッションの指標</span><span class="sxs-lookup"><span data-stu-id="16764-180">Metrics for Conferencing Sessions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="16764-181">名前</span><span class="sxs-lookup"><span data-stu-id="16764-181">Name</span></span></th>
<th><span data-ttu-id="16764-182">この項目での並べ替え</span><span class="sxs-lookup"><span data-stu-id="16764-182">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="16764-183">説明</span><span class="sxs-lookup"><span data-stu-id="16764-183">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="16764-184"><strong>[電話会議の合計数]</strong></span><span class="sxs-lookup"><span data-stu-id="16764-184"><strong>Total conferences</strong></span></span></p></td>
<td><p><span data-ttu-id="16764-185">不可</span><span class="sxs-lookup"><span data-stu-id="16764-185">No</span></span></p></td>
<td><p><span data-ttu-id="16764-186">実施された電話会議の総数です。</span><span class="sxs-lookup"><span data-stu-id="16764-186">Total number of conferences conducted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16764-187"><strong>[電話会議セッションの合計数]</strong></span><span class="sxs-lookup"><span data-stu-id="16764-187"><strong>Total conference sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="16764-188">不可</span><span class="sxs-lookup"><span data-stu-id="16764-188">No</span></span></p></td>
<td><p><span data-ttu-id="16764-189">実施された電話会議セッションの総数です。</span><span class="sxs-lookup"><span data-stu-id="16764-189">Total number of conferencing sessions conducted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16764-190"><strong>[全体的なセッション エラー率]</strong></span><span class="sxs-lookup"><span data-stu-id="16764-190"><strong>Overall session failure rate</strong></span></span></p></td>
<td><p><span data-ttu-id="16764-191">不可</span><span class="sxs-lookup"><span data-stu-id="16764-191">No</span></span></p></td>
<td><p><span data-ttu-id="16764-192">エラーが発生した電話会議セッション総数の割合です。</span><span class="sxs-lookup"><span data-stu-id="16764-192">Percentage of the total conferencing sessions that failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16764-193"><strong>[フォーカス セッション]</strong></span><span class="sxs-lookup"><span data-stu-id="16764-193"><strong>Focus sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="16764-194">不可</span><span class="sxs-lookup"><span data-stu-id="16764-194">No</span></span></p></td>
<td><p><span data-ttu-id="16764-195">エラーが発生したフォーカス ベース電話会議セッションの総数です。</span><span class="sxs-lookup"><span data-stu-id="16764-195">Total number of Focus-based conferencing sessions that failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16764-196"><strong>[フォーカス エラー率]</strong></span><span class="sxs-lookup"><span data-stu-id="16764-196"><strong>Focus failure rate</strong></span></span></p></td>
<td><p><span data-ttu-id="16764-197">不可</span><span class="sxs-lookup"><span data-stu-id="16764-197">No</span></span></p></td>
<td><p><span data-ttu-id="16764-198">エラーが発生したフォーカス ベース電話会議セッションの割合です。</span><span class="sxs-lookup"><span data-stu-id="16764-198">Percentage of the Focus-based conferencing sessions that failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16764-199"><strong>[MCU セッション]</strong></span><span class="sxs-lookup"><span data-stu-id="16764-199"><strong>MCU sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="16764-200">不可</span><span class="sxs-lookup"><span data-stu-id="16764-200">No</span></span></p></td>
<td><p><span data-ttu-id="16764-201">エラーが発生した、会議サーバー (以前の Multipoint Control Unit (MCU)) ベースの電話会議の総数です。</span><span class="sxs-lookup"><span data-stu-id="16764-201">Total number of conferencing server-based (formerly known as Multipoint Control Unit or MCU) conferences that failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16764-202"><strong>[MCU エラー率]</strong></span><span class="sxs-lookup"><span data-stu-id="16764-202"><strong>MCU failure rate</strong></span></span></p></td>
<td><p><span data-ttu-id="16764-203">不可</span><span class="sxs-lookup"><span data-stu-id="16764-203">No</span></span></p></td>
<td><p><span data-ttu-id="16764-204">エラーが発生した、会議サーバー (以前の Multipoint Control Unit (MCU)) ベースの電話会議の割合です。</span><span class="sxs-lookup"><span data-stu-id="16764-204">Percentage of the conferencing server-based (formerly known as Multipoint Control Unit or MCU) conferences that failed.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="16764-205">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="16764-205">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

