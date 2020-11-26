---
title: 'Lync Server 2013: 会議アクティビティレポート'
description: 'Lync Server 2013: 会議アクティビティレポート。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conference Activity Report
ms:assetid: 22ddb509-af16-4fc8-9b98-6f58caa6f37e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558627(v=OCS.15)
ms:contentKeyID: 48183618
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b7a2b23a08970defaec62b98d075ad1167527fd7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434551"
---
# <a name="conference-activity-report-in-lync-server-2013"></a><span data-ttu-id="85413-103">Lync Server 2013 での会議アクティビティレポート</span><span class="sxs-lookup"><span data-stu-id="85413-103">Conference Activity Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="85413-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="85413-104">

<span> </span></span></span>

<span data-ttu-id="85413-105">_**最終更新日:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="85413-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="85413-106">電話会議動作状況レポートを使用すると、たとえば 1 日に開催されている電話会議の数や、その時間帯に関する質問に簡単に答えることができます。</span><span class="sxs-lookup"><span data-stu-id="85413-106">The Conference Activity Report makes it easy for you to answer questions like these: how many conferences are being held each day, and when are those conferences being held?</span></span> <span data-ttu-id="85413-107">このような情報はそれ自体が有用であるだけでなく、トラブルシューティング ツールとしても役立ちます。</span><span class="sxs-lookup"><span data-stu-id="85413-107">Information like this is useful not only in its own right, but also as a troubleshooting tool.</span></span> <span data-ttu-id="85413-108">たとえば、昼頃になるとネットワークが著しく遅くなるという苦情がユーザーから寄せられているとします。</span><span class="sxs-lookup"><span data-stu-id="85413-108">For example, suppose users are complaining that the network seems particularly slow in the middle of the day.</span></span> <span data-ttu-id="85413-109">会議アクティビティレポートの概要については、考えられる理由の1つとして、10:00 AM と 2:00 PM の間でスケジュールされている会議の数を確認します。</span><span class="sxs-lookup"><span data-stu-id="85413-109">A quick glance at the Conference Activity reports might suggest one possible reason: far more conferences are being scheduled between the hours of 10:00 AM and 2:00 PM then at any other time.</span></span>

<span data-ttu-id="85413-110">ネットワーク速度が遅いために問題が起きている場合は、一部の電話会議の予定をトラフィックが少ない時間帯にずらしてもらうようにユーザーに働きかけることができます。</span><span class="sxs-lookup"><span data-stu-id="85413-110">If the slow network is causing problems, you can encourage users to reschedule some of their conferences during the less-heavily trafficked times of the day.</span></span>

<div>

## <a name="accessing-the-conference-activity-report"></a><span data-ttu-id="85413-111">電話会議動作状況レポートにアクセスする</span><span class="sxs-lookup"><span data-stu-id="85413-111">Accessing the Conference Activity Report</span></span>

<span data-ttu-id="85413-112">会議アクティビティレポートには、 [Lync Server 2013 の [会議の概要] レポート](lync-server-2013-conference-summary-report.md) からアクセスできます。次のいずれかの指標をクリックします。</span><span class="sxs-lookup"><span data-stu-id="85413-112">The Conference Activity Report is accessed from the [Conference Summary Report in Lync Server 2013](lync-server-2013-conference-summary-report.md) by clicking either one of the following metrics:</span></span>

  - <span data-ttu-id="85413-113">電話会議の合計数</span><span class="sxs-lookup"><span data-stu-id="85413-113">Total conferences</span></span>

  - <span data-ttu-id="85413-114">参加者の合計数</span><span class="sxs-lookup"><span data-stu-id="85413-114">Total participants</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-conference-activity-report"></a><span data-ttu-id="85413-115">電話会議動作状況レポートを最大限に活用する</span><span class="sxs-lookup"><span data-stu-id="85413-115">Making the Best Use of the Conference Activity Report</span></span>

<span data-ttu-id="85413-p102">既定では、電話会議動作状況レポートには指定した期間における電話会議の合計数 (たとえば、1 日あたりの電話会議の合計数や、1 日の 1 時間あたりの電話会議の合計数) が表示されます。ただし、その期間における参加者の合計数や、参加者の合計分数を表示することもできます。この操作を行うには、[パラメーターの表示/非表示] ボタンをクリックしてフィルター オプションを表示し、[報告元] ドロップダウン リストから次のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="85413-p102">By default the Conference Activity Report shows you the total number of conferences for the specified time period (for example, the total number of conferences per day, or the total number of conferences per hour of the day). However, you can also choose to display the total number of participants for that time period or the total number of participant minutes. To do that, click the Show/Hide Parameters button to display the filtering options, and then select one of the following from the Report by dropdown list:</span></span>

  - <span data-ttu-id="85413-119">参加者数</span><span class="sxs-lookup"><span data-stu-id="85413-119">Participant count</span></span>

  - <span data-ttu-id="85413-120">参加者の分数</span><span class="sxs-lookup"><span data-stu-id="85413-120">Participant minutes</span></span>

  - <span data-ttu-id="85413-121">電話会議数</span><span class="sxs-lookup"><span data-stu-id="85413-121">Conference count</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="85413-122">フィルター</span><span class="sxs-lookup"><span data-stu-id="85413-122">Filters</span></span>

<span data-ttu-id="85413-p103">フィルターは、細かく絞り込んだデータ セットを返したり、返されたデータをさまざまな方法で表示したりする方法として利用できます。次の表に、電話会議動作状況レポートで使用できるフィルターを示します。</span><span class="sxs-lookup"><span data-stu-id="85413-p103">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. The following table lists the filters that you can use with the Conference Activity Report.</span></span>

### <a name="conference-activity-report-filters"></a><span data-ttu-id="85413-125">電話会議動作状況レポートのフィルター</span><span class="sxs-lookup"><span data-stu-id="85413-125">Conference Activity Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="85413-126">名前</span><span class="sxs-lookup"><span data-stu-id="85413-126">Name</span></span></th>
<th><span data-ttu-id="85413-127">説明</span><span class="sxs-lookup"><span data-stu-id="85413-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="85413-128"><strong>開始</strong></span><span class="sxs-lookup"><span data-stu-id="85413-128"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="85413-p104">時間範囲の開始日と開始時刻。データを時間単位で表示するには、次のように開始日と開始時刻の両方を入力します。</span><span class="sxs-lookup"><span data-stu-id="85413-p104">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="85413-131">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="85413-131">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="85413-p105">開始時刻を入力しないと、レポートは自動的に指定日の午前 12:00 に開始します。データを日単位で表示するには、次のように日付のみを入力します。</span><span class="sxs-lookup"><span data-stu-id="85413-p105">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="85413-134">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="85413-134">7/7/2012</span></span></p>
<p><span data-ttu-id="85413-135">週単位または月単位で表示するには、表示する週または月の任意の日付を入力します (その週または月の最初の日である必要はありません)。</span><span class="sxs-lookup"><span data-stu-id="85413-135">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="85413-136">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="85413-136">7/3/2012</span></span></p>
<p><span data-ttu-id="85413-137">一週間は、日曜日から始まり、土曜日で終わるものとします。</span><span class="sxs-lookup"><span data-stu-id="85413-137">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85413-138"><strong>終了</strong></span><span class="sxs-lookup"><span data-stu-id="85413-138"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="85413-p106">時間範囲の終了日と終了時刻。データを時間単位で表示するには、次のように終了日と終了時刻の両方を入力します。</span><span class="sxs-lookup"><span data-stu-id="85413-p106">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="85413-141">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="85413-141">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="85413-p107">終了時刻を入力しないと、レポートは自動的に指定日の午前 12:00 に終了します。データを日単位で表示するには、次のように日付のみを入力します。</span><span class="sxs-lookup"><span data-stu-id="85413-p107">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="85413-144">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="85413-144">7/7/2012</span></span></p>
<p><span data-ttu-id="85413-145">週単位または月単位で表示するには、表示する週または月の任意の日付を入力します (その週または月の最初の日である必要はありません)。</span><span class="sxs-lookup"><span data-stu-id="85413-145">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="85413-146">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="85413-146">7/3/2012</span></span></p>
<p><span data-ttu-id="85413-147">一週間は、日曜日から始まり、土曜日で終わるものとします。</span><span class="sxs-lookup"><span data-stu-id="85413-147">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85413-148"><strong>[間隔]</strong></span><span class="sxs-lookup"><span data-stu-id="85413-148"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="85413-p108">時間間隔です。次のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="85413-p108">Time interval. Select any of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="85413-151">毎時 (最大 25 時間の表示が可能)</span><span class="sxs-lookup"><span data-stu-id="85413-151">Hourly (a maximum of 25 hours can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="85413-152">毎日 (最大 31 日の表示が可能)</span><span class="sxs-lookup"><span data-stu-id="85413-152">Daily (a maximum of 31 days can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="85413-153">毎週 (最大 12 週の表示が可能)</span><span class="sxs-lookup"><span data-stu-id="85413-153">Weekly (a maximum of 12 weeks can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="85413-154">毎月 (最大 12 か月の表示が可能)</span><span class="sxs-lookup"><span data-stu-id="85413-154">Monthly (a maximum of 12 months can be displayed)</span></span></p></li>
</ul>
<p><span data-ttu-id="85413-155">入力した開始日と終了日が選択した間隔で使用できる値の最大数を超える場合は、最大数の値 (開始日からカウント) のみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="85413-155">If the start and end dates exceed the maximum number of values allowed for the selected interval, only the maximum number of values (starting from the start date) is displayed.</span></span> <span data-ttu-id="85413-156">たとえば、開始日が7/7/2012 で、終了日が2/28/2012 の [日] 間隔を選択した場合は、8/7/2012 12:00 AM から 9/7/2012 12:00 AM (つまり、31日分のデータ) のデータが表示されます。</span><span class="sxs-lookup"><span data-stu-id="85413-156">For example, if you select the Daily interval with a start date of 7/7/2012 and an end date of 2/28/2012, data is displayed for the days 8/7/2012 12:00 AM to 9/7/2012 12:00 AM (that is, a total of 31 days' worth of data).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85413-157"><strong>[報告元]</strong></span><span class="sxs-lookup"><span data-stu-id="85413-157"><strong>Report by</strong></span></span></p></td>
<td><p><span data-ttu-id="85413-p110">レポートで使用する値を指定します。次の中から選択します。</span><span class="sxs-lookup"><span data-stu-id="85413-p110">Indicates the values to be used in the report. You can select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="85413-160">参加者数</span><span class="sxs-lookup"><span data-stu-id="85413-160">Participant Count</span></span></p></li>
<li><p><span data-ttu-id="85413-161">参加者の分数</span><span class="sxs-lookup"><span data-stu-id="85413-161">Participant Minutes</span></span></p></li>
<li><p><span data-ttu-id="85413-162">電話会議数</span><span class="sxs-lookup"><span data-stu-id="85413-162">Conference Count</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-conferences-by-pool"></a><span data-ttu-id="85413-163">電話会議 (プール別) の指標</span><span class="sxs-lookup"><span data-stu-id="85413-163">Metrics for Conferences by Pool</span></span>

<span data-ttu-id="85413-164">次の表に、プールごとの電話会議動作状況レポートでの情報を示します。</span><span class="sxs-lookup"><span data-stu-id="85413-164">The following table lists the information in the Conference Activity Report for each pool.</span></span>

### <a name="metrics-for-conferences-by-pool"></a><span data-ttu-id="85413-165">電話会議 (プール別) の指標</span><span class="sxs-lookup"><span data-stu-id="85413-165">Metrics for Conferences by Pool</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="85413-166">名前</span><span class="sxs-lookup"><span data-stu-id="85413-166">Name</span></span></th>
<th><span data-ttu-id="85413-167">この項目での並べ替え</span><span class="sxs-lookup"><span data-stu-id="85413-167">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="85413-168">説明</span><span class="sxs-lookup"><span data-stu-id="85413-168">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="85413-169"><strong>プール</strong></span><span class="sxs-lookup"><span data-stu-id="85413-169"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="85413-170">不可</span><span class="sxs-lookup"><span data-stu-id="85413-170">No</span></span></p></td>
<td><p><span data-ttu-id="85413-171">電話会議で使用されたレジストラー プールまたはエッジ サーバーの名前。</span><span class="sxs-lookup"><span data-stu-id="85413-171">Name of the Registrar pool or Edge Server used in the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85413-172"><strong>[日付/時刻]</strong></span><span class="sxs-lookup"><span data-stu-id="85413-172"><strong>Date/Time</strong></span></span></p></td>
<td><p><span data-ttu-id="85413-173">不可</span><span class="sxs-lookup"><span data-stu-id="85413-173">No</span></span></p></td>
<td><p><span data-ttu-id="85413-174">電話会議の開始日時。</span><span class="sxs-lookup"><span data-stu-id="85413-174">Date and time when the conference was held.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85413-175"><strong>[合計]</strong></span><span class="sxs-lookup"><span data-stu-id="85413-175"><strong>Total</strong></span></span></p></td>
<td><p><span data-ttu-id="85413-176">不可</span><span class="sxs-lookup"><span data-stu-id="85413-176">No</span></span></p></td>
<td><p><span data-ttu-id="85413-177">参加者総数、参加者総時間 (分)、電話会議総数。</span><span class="sxs-lookup"><span data-stu-id="85413-177">Total participant count, total participant minutes, or total conference count.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-conferences-by-server-type"></a><span data-ttu-id="85413-178">電話会議 (サーバーの種類別) の指標</span><span class="sxs-lookup"><span data-stu-id="85413-178">Metrics for Conferences by Server Type</span></span>

<span data-ttu-id="85413-179">次の表に、サーバーの種類ごとの電話会議動作状況レポートでの情報を示します。</span><span class="sxs-lookup"><span data-stu-id="85413-179">The following table lists the information in the Conference Activity Report for each type of server.</span></span>

### <a name="metrics-for-conferences-by-server-type"></a><span data-ttu-id="85413-180">電話会議 (サーバーの種類別) の指標</span><span class="sxs-lookup"><span data-stu-id="85413-180">Metrics for Conferences by Server Type</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="85413-181">名前</span><span class="sxs-lookup"><span data-stu-id="85413-181">Name</span></span></th>
<th><span data-ttu-id="85413-182">この項目での並べ替え</span><span class="sxs-lookup"><span data-stu-id="85413-182">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="85413-183">説明</span><span class="sxs-lookup"><span data-stu-id="85413-183">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="85413-184"><strong>[会議サーバーの種類]</strong></span><span class="sxs-lookup"><span data-stu-id="85413-184"><strong>Conferencing server type</strong></span></span></p></td>
<td><p><span data-ttu-id="85413-185">不可</span><span class="sxs-lookup"><span data-stu-id="85413-185">No</span></span></p></td>
<td><p><span data-ttu-id="85413-186">電話会議で使用されたサーバーの種類。通常は、次のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="85413-186">Type of server used in the conference, typically one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="85413-187">Web 会議サーバー</span><span class="sxs-lookup"><span data-stu-id="85413-187">Web Conferencing Server</span></span></p></li>
<li><p><span data-ttu-id="85413-188">IM 会議サービス</span><span class="sxs-lookup"><span data-stu-id="85413-188">IM Conferencing Server</span></span></p></li>
<li><p><span data-ttu-id="85413-189">テレフォニー会議サービス</span><span class="sxs-lookup"><span data-stu-id="85413-189">Telephony Conferencing Server</span></span></p></li>
<li><p><span data-ttu-id="85413-190">音声ビデオ会議サーバー</span><span class="sxs-lookup"><span data-stu-id="85413-190">AV Conferencing Server</span></span></p></li>
<li><p><span data-ttu-id="85413-191">アプリケーション共有</span><span class="sxs-lookup"><span data-stu-id="85413-191">Application Sharing</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85413-192"><strong>[日付/時刻]</strong></span><span class="sxs-lookup"><span data-stu-id="85413-192"><strong>Date/Time</strong></span></span></p></td>
<td><p><span data-ttu-id="85413-193">不可</span><span class="sxs-lookup"><span data-stu-id="85413-193">No</span></span></p></td>
<td><p><span data-ttu-id="85413-194">電話会議の開始日時。</span><span class="sxs-lookup"><span data-stu-id="85413-194">Date and time when the conference was held.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85413-195"><strong>[合計]</strong></span><span class="sxs-lookup"><span data-stu-id="85413-195"><strong>Total</strong></span></span></p></td>
<td><p><span data-ttu-id="85413-196">不可</span><span class="sxs-lookup"><span data-stu-id="85413-196">No</span></span></p></td>
<td><p><span data-ttu-id="85413-197">参加者総数、参加者総時間 (分)、電話会議総数。</span><span class="sxs-lookup"><span data-stu-id="85413-197">Total participant count, total participant minutes, or total conference count.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="85413-198">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="85413-198">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

