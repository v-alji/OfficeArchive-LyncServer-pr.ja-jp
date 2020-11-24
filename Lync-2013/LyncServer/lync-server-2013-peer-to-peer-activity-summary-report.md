---
title: 'Lync Server 2013: ピアツーピアアクティビティの概要レポート'
description: 'Lync Server 2013: ピアツーピアアクティビティの概要レポート。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Peer-to-Peer Activity Summary Report
ms:assetid: e829a21e-9dfa-46ba-9b5b-077c175d6586
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615041(v=OCS.15)
ms:contentKeyID: 48185884
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2f081f542a5063ed83be470d3e991c58e458b487
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399542"
---
# <a name="peer-to-peer-activity-summary-report-in-lync-server-2013"></a><span data-ttu-id="16d86-103">Lync Server 2013 のピアツーピアアクティビティの概要レポート</span><span class="sxs-lookup"><span data-stu-id="16d86-103">Peer-to-Peer Activity Summary Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="16d86-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="16d86-104">

<span> </span></span></span>

<span data-ttu-id="16d86-105">_**最終更新日:** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="16d86-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="16d86-106">ピアツーピア アクティビティ概要レポートでは、ピアツーピア通信セッションの概要が示されます。</span><span class="sxs-lookup"><span data-stu-id="16d86-106">The Peer-to-Peer Activity Summary Report provides an overall view of your peer-to-peer communication sessions.</span></span> <span data-ttu-id="16d86-107">ピアツーピアセッションでは通常、2人のユーザーのみが関係し、Lync Server 会議サービスを使う必要はありません。</span><span class="sxs-lookup"><span data-stu-id="16d86-107">A peer-to-peer session typically involves just two users, and does not require the use of the Lync Server conferencing services.</span></span> <span data-ttu-id="16d86-108">これに対して、会議は通常、3人以上のユーザーを対象としており、Microsoft Lync Server 2013 会議サービスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="16d86-108">By comparison, a conference typically involves more than two users and requires the use of Microsoft Lync Server 2013 conferencing services.</span></span> <span data-ttu-id="16d86-109">会議アクティビティは、会議概要レポートで報告されます。</span><span class="sxs-lookup"><span data-stu-id="16d86-109">Conference activity is reported on the Conference Summary Report.</span></span>

<span data-ttu-id="16d86-110">ピアツーピア アクティビティ概要レポートは、次のような質問に答えるときに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="16d86-110">The Peer-to-Peer Activity Summary Report helps you answer questions like the following:</span></span>

  - <span data-ttu-id="16d86-111">通常、ユーザーはピアツーピア インスタント メッセージを 1 日に何通送信しますか?</span><span class="sxs-lookup"><span data-stu-id="16d86-111">How many peer-to-peer instant messages do my users send on a typical day?</span></span>

  - <span data-ttu-id="16d86-112">ユーザーは、実際に Lync Server アプリケーション共有機能とファイル転送機能を利用していますか。</span><span class="sxs-lookup"><span data-stu-id="16d86-112">Are any of my users actually taking advantage of the Lync Server application sharing and file transfer capabilities?</span></span>

  - <span data-ttu-id="16d86-p102">ユーザーが、ネットワークの速度が 1 日の特定の時刻で遅くなるようだと訴えています。これらの時間帯でピアツーピアの音声ビデオセッションに費やされた時間は何分ですか?</span><span class="sxs-lookup"><span data-stu-id="16d86-p102">Users have been complaining that the network seems slow at certain times of the day. How many minutes are devoted to peer-to-peer audio and video sessions during those time periods?</span></span>

<div>

## <a name="accessing-the-peer-to-peer-activity-summary-report"></a><span data-ttu-id="16d86-115">ピアツーピア アクティビティ概要レポートにアクセスする</span><span class="sxs-lookup"><span data-stu-id="16d86-115">Accessing the Peer-to-Peer Activity Summary Report</span></span>

<span data-ttu-id="16d86-116">監視レポートのホーム ページからピアツーピア アクティビティ概要レポートにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="16d86-116">You access the Peer-to-Peer Activity Summary Report from the Monitoring Reports home page.</span></span> <span data-ttu-id="16d86-117">次のメトリックのいずれかをクリックして、 [Lync Server 2013 でピアツーピア IM レポート](lync-server-2013-peer-to-peer-im-report.md) を開きます。</span><span class="sxs-lookup"><span data-stu-id="16d86-117">You open the [Peer-to-Peer IM Report in Lync Server 2013](lync-server-2013-peer-to-peer-im-report.md) by clicking either of the following metrics:</span></span>

  - <span data-ttu-id="16d86-118">ピアツーピア IM セッションの合計数</span><span class="sxs-lookup"><span data-stu-id="16d86-118">Total peer-to-peer IM sessions</span></span>

  - <span data-ttu-id="16d86-119">ピアツーピア IM メッセージの合計数</span><span class="sxs-lookup"><span data-stu-id="16d86-119">Total peer-to-peer IM messages</span></span>

<span data-ttu-id="16d86-120">同様に、ピアツーピア音声およびビデオ レポートを開くには、次のいずれかの指標をクリックします。</span><span class="sxs-lookup"><span data-stu-id="16d86-120">Likewise, you can open the Peer-to-Peer Voice and Video Report by clicking any of these metrics:</span></span>

  - <span data-ttu-id="16d86-121">ピアツーピア音声セッションの合計数</span><span class="sxs-lookup"><span data-stu-id="16d86-121">Total peer-to-peer audio sessions</span></span>

  - <span data-ttu-id="16d86-122">ピアツーピア音声セッションの合計時間 (分)</span><span class="sxs-lookup"><span data-stu-id="16d86-122">Total peer-to-peer audio session minutes</span></span>

  - <span data-ttu-id="16d86-123">ピアツーピア音声セッションの合計数</span><span class="sxs-lookup"><span data-stu-id="16d86-123">Total peer-to-peer audio sessions</span></span>

  - <span data-ttu-id="16d86-124">ピアツーピア音声セッションの合計時間 (分)</span><span class="sxs-lookup"><span data-stu-id="16d86-124">Total peer-to-peer audio session minutes</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-peer-to-peer-activity-summary-report"></a><span data-ttu-id="16d86-125">ピアツーピア アクティビティ概要レポートを最大限に活用する</span><span class="sxs-lookup"><span data-stu-id="16d86-125">Making the Best Use of the Peer-to-Peer Activity Summary Report</span></span>

<span data-ttu-id="16d86-p104">ピアツーピア アクティビティ概要レポートの下部には、ピアツーピア IM セッションの合計数やピアツーピア IM メッセージの合計数などの、合計の指標が表示されます。これにより、レポート本文にある詳細情報の概要が示されます。</span><span class="sxs-lookup"><span data-stu-id="16d86-p104">At the bottom of the Peer-to-Peer Activity Summary Report you'll find totals for metrics such as Total peer-to-peer IM sessions and Total peer-to-peer IM messages. This provides a quick summary of the detailed information found in the body of the report.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="16d86-128">フィルター</span><span class="sxs-lookup"><span data-stu-id="16d86-128">Filters</span></span>

<span data-ttu-id="16d86-p105">フィルターは、細かく絞り込んだデータ セットを返したり、返されたデータをさまざまな方法で表示したりする方法として利用できます。たとえば、ピアツーピア アクティビティ概要レポートでは、データをグループ化する方法を選択できます。この場合は、時間、日、週、または月を基準にアクティビティがグループ化されます。</span><span class="sxs-lookup"><span data-stu-id="16d86-p105">Filters provide a way for you to return a more finely targeted set of data or to view the returned data in different ways. For example, the Peer-to-Peer Activity Summary Report enables you to choose how data should be grouped. In this case, activity grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="16d86-132">次の表に、ピアツーピア アクティビティ概要レポートで使用できるフィルターを示します。</span><span class="sxs-lookup"><span data-stu-id="16d86-132">The following table lists the filters that you can use with the Peer-to-Peer Activity Summary Report.</span></span>

### <a name="peer-to-peer-activity-summary-report-filters"></a><span data-ttu-id="16d86-133">ピアツーピア アクティビティ概要レポートのフィルター</span><span class="sxs-lookup"><span data-stu-id="16d86-133">Peer-to-Peer Activity Summary Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="16d86-134">名前</span><span class="sxs-lookup"><span data-stu-id="16d86-134">Name</span></span></th>
<th><span data-ttu-id="16d86-135">説明</span><span class="sxs-lookup"><span data-stu-id="16d86-135">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="16d86-136"><strong>開始</strong></span><span class="sxs-lookup"><span data-stu-id="16d86-136"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="16d86-p106">時間範囲の開始日と開始時刻。データを時間単位で表示するには、次のように開始日と開始時刻の両方を入力します。</span><span class="sxs-lookup"><span data-stu-id="16d86-p106">Start date and time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="16d86-139">7/17/12012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="16d86-139">7/17/12012 1:00 PM</span></span></p>
<p><span data-ttu-id="16d86-p107">開始時刻を入力しないと、レポートは自動的に指定日の午前 12:00 に開始します。データを日単位で表示するには、次のように日付のみを入力します。</span><span class="sxs-lookup"><span data-stu-id="16d86-p107">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="16d86-142">7/17/12012</span><span class="sxs-lookup"><span data-stu-id="16d86-142">7/17/12012</span></span></p>
<p><span data-ttu-id="16d86-143">週単位または月単位で表示するには、表示する週または月の任意の日付を入力します (その週または月の最初の日である必要はありません)。</span><span class="sxs-lookup"><span data-stu-id="16d86-143">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="16d86-144">7/13/2012</span><span class="sxs-lookup"><span data-stu-id="16d86-144">7/13/2012</span></span></p>
<p><span data-ttu-id="16d86-145">一週間は、日曜日から始まり、土曜日で終わるものとします。</span><span class="sxs-lookup"><span data-stu-id="16d86-145">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16d86-146"><strong>終了</strong></span><span class="sxs-lookup"><span data-stu-id="16d86-146"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="16d86-p108">時間範囲の終了日と終了時刻。データを時間単位で表示するには、次のように終了日と終了時刻の両方を入力します。</span><span class="sxs-lookup"><span data-stu-id="16d86-p108">End date and time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="16d86-149">7/17/12012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="16d86-149">7/17/12012 1:00 PM</span></span></p>
<p><span data-ttu-id="16d86-p109">終了時刻を入力しないと、レポートは自動的に指定日の午前 12:00 に終了します。データを日単位で表示するには、次のように日付のみを入力します。</span><span class="sxs-lookup"><span data-stu-id="16d86-p109">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="16d86-152">7/17/12012</span><span class="sxs-lookup"><span data-stu-id="16d86-152">7/17/12012</span></span></p>
<p><span data-ttu-id="16d86-153">週単位または月単位で表示するには、表示する週または月の任意の日付を入力します (その週または月の最初の日である必要はありません)。</span><span class="sxs-lookup"><span data-stu-id="16d86-153">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="16d86-154">7/13/2012</span><span class="sxs-lookup"><span data-stu-id="16d86-154">7/13/2012</span></span></p>
<p><span data-ttu-id="16d86-155">一週間は、日曜日から始まり、土曜日で終わるものとします。</span><span class="sxs-lookup"><span data-stu-id="16d86-155">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16d86-156"><strong>[間隔]</strong></span><span class="sxs-lookup"><span data-stu-id="16d86-156"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="16d86-p110">時間間隔です。次のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="16d86-p110">Time interval. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="16d86-159">毎時 (最大 25 時間の表示が可能)</span><span class="sxs-lookup"><span data-stu-id="16d86-159">Hourly (a maximum of 25 hours can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="16d86-160">毎日 (最大 31 日の表示が可能)</span><span class="sxs-lookup"><span data-stu-id="16d86-160">Daily (a maximum of 31 days can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="16d86-161">毎週 (最大 12 週の表示が可能)</span><span class="sxs-lookup"><span data-stu-id="16d86-161">Weekly (a maximum of 12 weeks can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="16d86-162">毎月 (最大 12 か月の表示が可能)</span><span class="sxs-lookup"><span data-stu-id="16d86-162">Monthly (a maximum of 12 months can be displayed)</span></span></p></li>
</ul>
<p><span data-ttu-id="16d86-163">入力した開始日と終了日が選択した間隔で使用できる値の最大数を超える場合は、最大数の値 (開始日からカウント) のみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="16d86-163">If the start and end dates exceed the maximum number of values allowed for the selected interval, only the maximum number of values (starting from the start date) is displayed.</span></span> <span data-ttu-id="16d86-164">たとえば、開始日が7/17/12012 で、終了日が2/28/2012 の [日] 間隔を選択した場合は、8/7/12012 12:00 AM から 9/7/12012 12:00 AM (つまり、31日分のデータ) のデータが表示されます。</span><span class="sxs-lookup"><span data-stu-id="16d86-164">For example, if you select the Daily interval with a start date of 7/17/12012 and an end date of 2/28/2012, data is displayed for the days 8/7/12012 12:00 AM to 9/7/12012 12:00 AM (that is, a total of 31 days' worth of data).</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="16d86-165">指標</span><span class="sxs-lookup"><span data-stu-id="16d86-165">Metrics</span></span>

<span data-ttu-id="16d86-166">次の表に、ピアツーピア アクティビティ概要レポートで提供される情報を示します。</span><span class="sxs-lookup"><span data-stu-id="16d86-166">The following table lists the information provided in the Peer-to-Peer Activity Summary Report.</span></span>

### <a name="peer-to-peer-activity-summary-report-metrics"></a><span data-ttu-id="16d86-167">ピアツーピア アクティビティ概要レポートの指標</span><span class="sxs-lookup"><span data-stu-id="16d86-167">Peer-to-Peer Activity Summary Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="16d86-168">名前</span><span class="sxs-lookup"><span data-stu-id="16d86-168">Name</span></span></th>
<th><span data-ttu-id="16d86-169">この項目での並べ替え</span><span class="sxs-lookup"><span data-stu-id="16d86-169">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="16d86-170">説明</span><span class="sxs-lookup"><span data-stu-id="16d86-170">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="16d86-171"><strong>[毎時]</strong></span><span class="sxs-lookup"><span data-stu-id="16d86-171"><strong>Hourly</strong></span></span></p>
<p><span data-ttu-id="16d86-172"><strong>[毎日]</strong></span><span class="sxs-lookup"><span data-stu-id="16d86-172"><strong>Daily</strong></span></span></p>
<p><span data-ttu-id="16d86-173"><strong>[毎週]</strong></span><span class="sxs-lookup"><span data-stu-id="16d86-173"><strong>Weekly</strong></span></span></p>
<p><span data-ttu-id="16d86-174"><strong>[毎月]</strong></span><span class="sxs-lookup"><span data-stu-id="16d86-174"><strong>Monthly</strong></span></span></p></td>
<td><p><span data-ttu-id="16d86-175">不可</span><span class="sxs-lookup"><span data-stu-id="16d86-175">No</span></span></p></td>
<td><p><span data-ttu-id="16d86-176">フィルター ツール バーで選択した期間を示します。</span><span class="sxs-lookup"><span data-stu-id="16d86-176">Indicates the time interval that you selected on the filter toolbar.</span></span> <span data-ttu-id="16d86-177">場合によっては、特定の期間をクリックして、その期間の詳細情報を表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="16d86-177">Where applicable, you can click a given time interval to view detailed information for that interval.</span></span> <span data-ttu-id="16d86-178">たとえば、毎日の間隔を使用していて、[7/17/12012] をクリックすると、その日付のユーザー登録アクティビティの時間の内訳が表示されます。</span><span class="sxs-lookup"><span data-stu-id="16d86-178">For example, if you are using the Daily interval and you click 7/17/12012, you see an hourly breakdown of user registration activity for that date.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16d86-179"><strong>ピアツーピア セッションの合計数</strong></span><span class="sxs-lookup"><span data-stu-id="16d86-179"><strong>Total peer-to-peer sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="16d86-180">不可</span><span class="sxs-lookup"><span data-stu-id="16d86-180">No</span></span></p></td>
<td><p><span data-ttu-id="16d86-181">実行されたピアツーピア セッションの合計数。セッションの種類は問いません。</span><span class="sxs-lookup"><span data-stu-id="16d86-181">Total number of peer-to-peer sessions conducted, regardless of session type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16d86-182"><strong>ピアツーピア IM セッションの合計数</strong></span><span class="sxs-lookup"><span data-stu-id="16d86-182"><strong>Total peer-to-peer IM sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="16d86-183">不可</span><span class="sxs-lookup"><span data-stu-id="16d86-183">No</span></span></p></td>
<td><p><span data-ttu-id="16d86-p113">ピアツーピア インスタント メッセージング (IM) セッションの合計数。この項目をクリックすると、選択した時間のピアツーピア IM レポートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="16d86-p113">Total number of peer-to-peer instant messaging (IM) sessions. When you click this item, the report shows you the Peer-to-Peer IM Report for the selected time period.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16d86-186"><strong>ピアツーピア IM メッセージの合計数</strong></span><span class="sxs-lookup"><span data-stu-id="16d86-186"><strong>Total peer-to-peer IM messages</strong></span></span></p></td>
<td><p><span data-ttu-id="16d86-187">不可</span><span class="sxs-lookup"><span data-stu-id="16d86-187">No</span></span></p></td>
<td><p><span data-ttu-id="16d86-p114">ピアツーピア セッションで送信されたインスタント メッセージの合計数。この項目をクリックすると、選択した時間のピアツーピア IM レポートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="16d86-p114">Total number of instant messages sent in peer-to-peer sessions. When you click this item, the report shows you the Peer-to-Peer IM Report for the selected time period.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16d86-190"><strong>ピアツーピア音声セッションの合計数</strong></span><span class="sxs-lookup"><span data-stu-id="16d86-190"><strong>Total peer-to-peer audio sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="16d86-191">不可</span><span class="sxs-lookup"><span data-stu-id="16d86-191">No</span></span></p></td>
<td><p><span data-ttu-id="16d86-p115">ピアツーピア音声通話の合計数。このフィールドをクリックすると、選択した時間のピアツーピア音声およびビデオ レポートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="16d86-p115">Total number of peer-to-peer audio calls. When you click this field, the report shows you the Peer-to-Peer Voice and Video Report for the selected time period.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16d86-194"><strong>ピアツーピア音声セッションの合計時間 (分)</strong></span><span class="sxs-lookup"><span data-stu-id="16d86-194"><strong>Total peer-to-peer audio session minutes</strong></span></span></p></td>
<td><p><span data-ttu-id="16d86-195">不可</span><span class="sxs-lookup"><span data-stu-id="16d86-195">No</span></span></p></td>
<td><p><span data-ttu-id="16d86-196">ピアツーピア音声セッションの合計時間。</span><span class="sxs-lookup"><span data-stu-id="16d86-196">Total amount of time spent in peer-to-peer audio sessions.</span></span> <span data-ttu-id="16d86-197">この項目をクリックすると、選択した時間のピアツーピア音声およびビデオ レポートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="16d86-197">When you click this item, the report shows you the Peer-to-Peer Voice and Video Report for the selected time period.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16d86-198"><strong>ピアツーピア音声セッションの平均時間 (分)</strong></span><span class="sxs-lookup"><span data-stu-id="16d86-198"><strong>Average peer-to-peer audio session minutes</strong></span></span></p></td>
<td><p><span data-ttu-id="16d86-199">不可</span><span class="sxs-lookup"><span data-stu-id="16d86-199">No</span></span></p></td>
<td><p><span data-ttu-id="16d86-p117">ピアツーピア音声セッションの平均時間。音声セッションの合計時間を音声セッションの合計数で割ることにより計算されます。</span><span class="sxs-lookup"><span data-stu-id="16d86-p117">Average amount of time spent in peer-to-peer audio sessions. Calculated by dividing the total audio session time by the total number of audio sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16d86-202"><strong>ピアツーピア ビデオ セッションの合計数</strong></span><span class="sxs-lookup"><span data-stu-id="16d86-202"><strong>Total peer-to-peer video sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="16d86-203">不可</span><span class="sxs-lookup"><span data-stu-id="16d86-203">No</span></span></p></td>
<td><p><span data-ttu-id="16d86-p118">ピアツーピア ビデオ通話の合計数。ビデオ セッションは音声セッションとしてもカウントされることに注意してください。各ビデオ セッションは、1 つのビデオ セッションおよび 1 つの音声セッションとしてカウントされます。この項目をクリックすると、選択した時間のピアツーピア音声およびビデオ レポートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="16d86-p118">Total number of peer-to-peer video calls. Note that video sessions are also counted as audio sessions: each video session is counted as one video session and one audio session. When you click this item, the report shows you the Peer-to-Peer Voice and Video Report for the selected time period.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16d86-207"><strong>ピアツーピア ビデオ セッションの合計時間 (分)</strong></span><span class="sxs-lookup"><span data-stu-id="16d86-207"><strong>Total peer-to-peer video session minutes</strong></span></span></p></td>
<td><p><span data-ttu-id="16d86-208">不可</span><span class="sxs-lookup"><span data-stu-id="16d86-208">No</span></span></p></td>
<td><p><span data-ttu-id="16d86-p119">ピアツーピア ビデオ セッションの合計時間。この項目をクリックすると、選択した時間のピアツーピア音声およびビデオ レポートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="16d86-p119">Total amount of time spent in peer-to-peer video sessions. When you click this item, the report shows you the Peer-to-Peer Voice and Video Report for the selected time period.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16d86-211"><strong>ピアツーピア ビデオ セッションの平均時間 (分)</strong></span><span class="sxs-lookup"><span data-stu-id="16d86-211"><strong>Average peer-to-peer video session minutes</strong></span></span></p></td>
<td><p><span data-ttu-id="16d86-212">不可</span><span class="sxs-lookup"><span data-stu-id="16d86-212">No</span></span></p></td>
<td><p><span data-ttu-id="16d86-p120">ピアツーピア ビデオ セッションの平均時間。ビデオ セッションの合計時間をビデオ セッションの合計数で割ることにより計算されます。</span><span class="sxs-lookup"><span data-stu-id="16d86-p120">Average amount of time spent in peer-to-peer video sessions. Calculated by dividing the total video session time by the total number of video sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16d86-215"><strong>ピアツーピア ファイル送信セッションの合計数</strong></span><span class="sxs-lookup"><span data-stu-id="16d86-215"><strong>Total peer-to-peer file transfer sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="16d86-216">不可</span><span class="sxs-lookup"><span data-stu-id="16d86-216">No</span></span></p></td>
<td><p><span data-ttu-id="16d86-217">ファイル送信を行ったピアツーピア セッションの合計数。</span><span class="sxs-lookup"><span data-stu-id="16d86-217">Total number of peer-to-peer sessions that included file transfers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16d86-218"><strong>ピアツーピア アプリケーション共有セッションの合計数</strong></span><span class="sxs-lookup"><span data-stu-id="16d86-218"><strong>Total peer-to-peer application sharing sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="16d86-219">不可</span><span class="sxs-lookup"><span data-stu-id="16d86-219">No</span></span></p></td>
<td><p><span data-ttu-id="16d86-220">アプリケーション共有を行ったピアツーピア セッションの合計数。</span><span class="sxs-lookup"><span data-stu-id="16d86-220">Total number of peer-to-peer sessions that included application sharing.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="16d86-221">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="16d86-221">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

