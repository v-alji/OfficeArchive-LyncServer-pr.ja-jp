---
title: 'Lync Server 2013: 会議の概要レポート'
description: 'Lync Server 2013: 会議の概要レポート。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conference Summary Report
ms:assetid: 62f54812-5700-45a3-8526-8f58b0f77fbc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558656(v=OCS.15)
ms:contentKeyID: 48184299
ms.date: 09/03/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2d9c0b8ad7280d2c7336282c14f46e6b5d6a1aec
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434495"
---
# <a name="conference-summary-report-in-lync-server-2013"></a><span data-ttu-id="7336c-103">Lync Server 2013 の会議の概要レポート</span><span class="sxs-lookup"><span data-stu-id="7336c-103">Conference Summary Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7336c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7336c-104">

<span> </span></span></span>

<span data-ttu-id="7336c-105">_**最終更新日:** 2014-09-03_</span><span class="sxs-lookup"><span data-stu-id="7336c-105">_**Topic Last Modified:** 2014-09-03_</span></span>

<span data-ttu-id="7336c-106">電話会議の概要レポートは、オンライン電話会議セッションの全体像を示します。</span><span class="sxs-lookup"><span data-stu-id="7336c-106">The Conference Summary Report provides an overall view of your online conferencing sessions.</span></span> <span data-ttu-id="7336c-107">通常、会議には2人以上のユーザーが関与し、Microsoft Lync Server 2013 会議サービスの使用が必要です。</span><span class="sxs-lookup"><span data-stu-id="7336c-107">A conference typically involves more than 2 users and requires the use of Microsoft Lync Server 2013 conferencing services.</span></span> <span data-ttu-id="7336c-108">これに対して、ピアツーピアセッションでは通常、2人のユーザーのみが必要となり、Lync Server の会議サービスを使う必要はありません。</span><span class="sxs-lookup"><span data-stu-id="7336c-108">By comparison, a peer-to-peer session typically involves just 2 users and does not require the use of Lync Server's conferencing services.</span></span> <span data-ttu-id="7336c-109">ピアツーピアのアクティビティは、 [Lync Server 2013 のピアツーピアアクティビティの概要レポート](lync-server-2013-peer-to-peer-activity-summary-report.md)で報告されます。</span><span class="sxs-lookup"><span data-stu-id="7336c-109">Peer-to-peer activities are reported on the [Peer-to-Peer Activity Summary Report in Lync Server 2013](lync-server-2013-peer-to-peer-activity-summary-report.md).</span></span>

<span data-ttu-id="7336c-110">[会議の概要] レポートには、特定の期間 (時間、日、週、月単位) に開催された会議の数が表示されるだけでなく、それらの会議に参加したユーザーの合計数と、会議の開催者の合計数も通知されます。</span><span class="sxs-lookup"><span data-stu-id="7336c-110">The Conference Summary Report not only tells you how many conferences were held during a given time period (hourly, daily, weekly, monthly) but also tells you the total number of people who took part in those conferences, and the total number of unique conference organizers.</span></span>

<span data-ttu-id="7336c-111">"一意の" 開催者とは、少なくとも 1 件の会議を予定したユーザーです。</span><span class="sxs-lookup"><span data-stu-id="7336c-111">A "unique” organizer is anyone who schedules at least one conference.</span></span> <span data-ttu-id="7336c-112">たとえば、Pilar Ackerman が 1 件の会議を予定した場合、彼女は 1 名の一意の開催者としてカウントされます。</span><span class="sxs-lookup"><span data-stu-id="7336c-112">For example, if Pilar Ackerman schedules one conference she counts as one unique organizer.</span></span> <span data-ttu-id="7336c-113">Ken Myer が 148 件の会議を予定した場合、彼も 1 名の一意の開催者としてカウントされます。</span><span class="sxs-lookup"><span data-stu-id="7336c-113">If Ken Myer schedules 148 conferences he, too counts as one unique organizer.</span></span> <span data-ttu-id="7336c-114">たとえば、次の表では、8回の会議がスケジュールされていますが、固有の開催者 (Ken Myer、Pilar Ackerman、David Ahs) が3つあります。</span><span class="sxs-lookup"><span data-stu-id="7336c-114">For example, the table below shows 8 conferences scheduled, but just three unique organizers (Ken Myer, Pilar Ackerman, and David Ahs).</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7336c-115">会議の開催者</span><span class="sxs-lookup"><span data-stu-id="7336c-115">Conference Organizer</span></span></th>
<th><span data-ttu-id="7336c-116">会議の開催日時</span><span class="sxs-lookup"><span data-stu-id="7336c-116">Conference Date</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7336c-117">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="7336c-117">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="7336c-118">7/7/2012 10:00 AM</span><span class="sxs-lookup"><span data-stu-id="7336c-118">7/7/2012 10:00 AM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7336c-119">David Ahs</span><span class="sxs-lookup"><span data-stu-id="7336c-119">David Ahs</span></span></p></td>
<td><p><span data-ttu-id="7336c-120">7/7/2012 10:00 AM</span><span class="sxs-lookup"><span data-stu-id="7336c-120">7/7/2012 10:00 AM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7336c-121">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="7336c-121">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="7336c-122">7/7/2012 11:00 AM</span><span class="sxs-lookup"><span data-stu-id="7336c-122">7/7/2012 11:00 AM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7336c-123">Pilar Ackerman</span><span class="sxs-lookup"><span data-stu-id="7336c-123">Pilar Ackerman</span></span></p></td>
<td><p><span data-ttu-id="7336c-124">7/7/2012 11:00 AM</span><span class="sxs-lookup"><span data-stu-id="7336c-124">7/7/2012 11:00 AM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7336c-125">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="7336c-125">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="7336c-126">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="7336c-126">7/7/2012 1:00 PM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7336c-127">Pilar Ackerman</span><span class="sxs-lookup"><span data-stu-id="7336c-127">Pilar Ackerman</span></span></p></td>
<td><p><span data-ttu-id="7336c-128">7/7/2012 2:00 PM</span><span class="sxs-lookup"><span data-stu-id="7336c-128">7/7/2012 2:00 PM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7336c-129">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="7336c-129">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="7336c-130">7/2/2012 10:00 AM</span><span class="sxs-lookup"><span data-stu-id="7336c-130">7/2/2012 10:00 AM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7336c-131">Pilar Ackerman</span><span class="sxs-lookup"><span data-stu-id="7336c-131">Pilar Ackerman</span></span></p></td>
<td><p><span data-ttu-id="7336c-132">7/2/2012 10:00 AM</span><span class="sxs-lookup"><span data-stu-id="7336c-132">7/2/2012 10:00 AM</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7336c-133">電話会議の概要レポートは、音声/ビデオを利用した会議の数も示します。</span><span class="sxs-lookup"><span data-stu-id="7336c-133">The Conference Summary Report also indicates how many conferences included audio and/or video.</span></span>

<div>

## <a name="accessing-the-conference-summary-report"></a><span data-ttu-id="7336c-134">電話会議の概要レポートへのアクセス方法</span><span class="sxs-lookup"><span data-stu-id="7336c-134">Accessing the Conference Summary Report</span></span>

<span data-ttu-id="7336c-p103">電話会議の概要レポートには、[監視レポート] ホーム ページからアクセスします。次の指標のどちらかをクリックすることで、電話会議動作状況レポートにドリルダウンできます。</span><span class="sxs-lookup"><span data-stu-id="7336c-p103">The Conference Summary Report is accessed from the Monitoring Reports home page. You can drill down to the Conference Activity report by clicking either of the following metrics:</span></span>

  - <span data-ttu-id="7336c-137">電話会議の合計数</span><span class="sxs-lookup"><span data-stu-id="7336c-137">Total conferences</span></span>

  - <span data-ttu-id="7336c-138">参加者の合計数</span><span class="sxs-lookup"><span data-stu-id="7336c-138">Total participants</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-conference-summary-report"></a><span data-ttu-id="7336c-139">電話会議の概要レポートを最大限に活用する</span><span class="sxs-lookup"><span data-stu-id="7336c-139">Making the Best Use of the Conference Summary Report</span></span>

<span data-ttu-id="7336c-140">会議の概要レポートで使用されるいくつかの指標の合計値は、レポートの下部にあります。下にスクロールして、指定した期間内に開催された会議の合計数、およびそれらの会議に参加したユーザーの合計数などの値を表示します。</span><span class="sxs-lookup"><span data-stu-id="7336c-140">Total values for most of the metrics used on the Conference Summary Report can be found at the bottom of the report; scroll down to see values such as the total number of conferences held during the specified time period, and the total number of people who participated in those conferences.</span></span> <span data-ttu-id="7336c-141">レポートの下部に集計されていない1つのメトリックは、一意の会議開催者の合計数です。</span><span class="sxs-lookup"><span data-stu-id="7336c-141">One metric that is not totaled at the bottom of the report is Total unique conference organizers.</span></span> <span data-ttu-id="7336c-142">なぜでしょうか。</span><span class="sxs-lookup"><span data-stu-id="7336c-142">Why not?</span></span> <span data-ttu-id="7336c-143">1つの理由を次に示します。</span><span class="sxs-lookup"><span data-stu-id="7336c-143">Here’s one reason.</span></span> <span data-ttu-id="7336c-144">1ヶ月分のデータを見ているとします。</span><span class="sxs-lookup"><span data-stu-id="7336c-144">Suppose you are looking at a month's worth of data.</span></span> <span data-ttu-id="7336c-145">1日目に、34固有の会議開催者がいます。2日目には、27の固有の会議開催者がいます。</span><span class="sxs-lookup"><span data-stu-id="7336c-145">On day 1 you had 34 unique conference organizers; on day 2 you had 27 unique conference organizers.</span></span> <span data-ttu-id="7336c-146">2日間、61固有の会議開催者であるということですか?</span><span class="sxs-lookup"><span data-stu-id="7336c-146">Does that mean you had 61 unique conference organizers for those two days?</span></span> <span data-ttu-id="7336c-147">必ずしもそうではありません。</span><span class="sxs-lookup"><span data-stu-id="7336c-147">Not necessarily.</span></span> <span data-ttu-id="7336c-148">結局、2日目に会議を開催した27人全員が、1日目に会議を開催した34人のユーザーである場合があります。</span><span class="sxs-lookup"><span data-stu-id="7336c-148">After all, all 27 people who organized conferences on day 2 might be among the 34 people who organized conferences on day 1.</span></span> <span data-ttu-id="7336c-149">たとえば、この単純なレポートでは、Ken Myer と Pilar Ackermanのスケジュールされた会議は、7/7/2012 と7/2/2012 の両方で使用されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="7336c-149">For example, in this simple report, note that Ken Myer and Pilar Ackerman scheduled conferences both on 7/7/2012 and on 7/2/2012:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7336c-150">会議の開催者</span><span class="sxs-lookup"><span data-stu-id="7336c-150">Conference Organizer</span></span></th>
<th><span data-ttu-id="7336c-151">会議の開催日時</span><span class="sxs-lookup"><span data-stu-id="7336c-151">Conference Date</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7336c-152">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="7336c-152">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="7336c-153">7/7/2012 10:00 AM</span><span class="sxs-lookup"><span data-stu-id="7336c-153">7/7/2012 10:00 AM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7336c-154">David Ahs</span><span class="sxs-lookup"><span data-stu-id="7336c-154">David Ahs</span></span></p></td>
<td><p><span data-ttu-id="7336c-155">7/7/2012 10:00 AM</span><span class="sxs-lookup"><span data-stu-id="7336c-155">7/7/2012 10:00 AM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7336c-156">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="7336c-156">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="7336c-157">7/7/2012 11:00 AM</span><span class="sxs-lookup"><span data-stu-id="7336c-157">7/7/2012 11:00 AM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7336c-158">Pilar Ackerman</span><span class="sxs-lookup"><span data-stu-id="7336c-158">Pilar Ackerman</span></span></p></td>
<td><p><span data-ttu-id="7336c-159">7/7/2012 11:00 AM</span><span class="sxs-lookup"><span data-stu-id="7336c-159">7/7/2012 11:00 AM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7336c-160">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="7336c-160">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="7336c-161">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="7336c-161">7/7/2012 1:00 PM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7336c-162">Pilar Ackerman</span><span class="sxs-lookup"><span data-stu-id="7336c-162">Pilar Ackerman</span></span></p></td>
<td><p><span data-ttu-id="7336c-163">7/7/2012 2:00 PM</span><span class="sxs-lookup"><span data-stu-id="7336c-163">7/7/2012 2:00 PM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7336c-164">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="7336c-164">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="7336c-165">7/2/2012 10:00 AM</span><span class="sxs-lookup"><span data-stu-id="7336c-165">7/2/2012 10:00 AM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7336c-166">Pilar Ackerman</span><span class="sxs-lookup"><span data-stu-id="7336c-166">Pilar Ackerman</span></span></p></td>
<td><p><span data-ttu-id="7336c-167">7/2/2012 10:00 AM</span><span class="sxs-lookup"><span data-stu-id="7336c-167">7/2/2012 10:00 AM</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7336c-168">会議を開催した一意のユーザーの総数を把握するには、期間を変更します。たとえば、日単位ではなく月単位でデータを調べます。</span><span class="sxs-lookup"><span data-stu-id="7336c-168">To get a better idea of the total number of unique users who organized conferences, change your time interval; for example, look at the data by month instead of by day.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="7336c-169">フィルター</span><span class="sxs-lookup"><span data-stu-id="7336c-169">Filters</span></span>

<span data-ttu-id="7336c-p105">フィルターは、細かく絞り込んだデータ セットを返したり、返されたデータをさまざまな方法で表示したりする方法として利用できます。たとえば、電話会議の概要レポートでは、データをグループ化する方法を選択できます。その場合は、電話会議が時間、日、週、または月の単位でグループ化されます。</span><span class="sxs-lookup"><span data-stu-id="7336c-p105">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Conference Summary Report enables you to choose how data should be grouped. In this case, conferences grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="7336c-173">次の表に、電話会議の概要レポートで使用できるフィルターを示します。</span><span class="sxs-lookup"><span data-stu-id="7336c-173">The following table lists the filters that you can use with the Conference Summary Report.</span></span>

### <a name="conference-summary-report-filters"></a><span data-ttu-id="7336c-174">電話会議の概要レポートのフィルター</span><span class="sxs-lookup"><span data-stu-id="7336c-174">Conference Summary Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7336c-175">名前</span><span class="sxs-lookup"><span data-stu-id="7336c-175">Name</span></span></th>
<th><span data-ttu-id="7336c-176">説明</span><span class="sxs-lookup"><span data-stu-id="7336c-176">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7336c-177"><strong>開始</strong></span><span class="sxs-lookup"><span data-stu-id="7336c-177"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="7336c-p106">時間範囲の開始日と開始時刻。データを時間単位で表示するには、次のように開始日と開始時刻の両方を入力します。</span><span class="sxs-lookup"><span data-stu-id="7336c-p106">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="7336c-180">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="7336c-180">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="7336c-p107">開始時刻を入力しないと、レポートは自動的に指定日の午前 12:00 に開始します。データを日単位で表示するには、次のように日付のみを入力します。</span><span class="sxs-lookup"><span data-stu-id="7336c-p107">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="7336c-183">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="7336c-183">7/7/2012</span></span></p>
<p><span data-ttu-id="7336c-184">週単位または月単位で表示するには、表示する週または月の任意の日付を入力します (その週または月の最初の日である必要はありません)。</span><span class="sxs-lookup"><span data-stu-id="7336c-184">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="7336c-185">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="7336c-185">7/3/2012</span></span></p>
<p><span data-ttu-id="7336c-186">一週間は、日曜日から始まり、土曜日で終わるものとします。</span><span class="sxs-lookup"><span data-stu-id="7336c-186">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7336c-187"><strong>終了</strong></span><span class="sxs-lookup"><span data-stu-id="7336c-187"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="7336c-p108">時間範囲の終了日と終了時刻。データを時間単位で表示するには、次のように終了日と終了時刻の両方を入力します。</span><span class="sxs-lookup"><span data-stu-id="7336c-p108">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="7336c-190">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="7336c-190">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="7336c-p109">終了時刻を入力しないと、レポートは自動的に指定日の午前 12:00 に終了します。データを日単位で表示するには、次のように日付のみを入力します。</span><span class="sxs-lookup"><span data-stu-id="7336c-p109">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="7336c-193">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="7336c-193">7/7/2012</span></span></p>
<p><span data-ttu-id="7336c-194">週単位または月単位で表示するには、表示する週または月の任意の日付を入力します (その週または月の最初の日である必要はありません)。</span><span class="sxs-lookup"><span data-stu-id="7336c-194">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="7336c-195">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="7336c-195">7/3/2012</span></span></p>
<p><span data-ttu-id="7336c-196">一週間は、日曜日から始まり、土曜日で終わるものとします。</span><span class="sxs-lookup"><span data-stu-id="7336c-196">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7336c-197"><strong>[間隔]</strong></span><span class="sxs-lookup"><span data-stu-id="7336c-197"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="7336c-p110">時間間隔です。次のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="7336c-p110">Time interval. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="7336c-200">毎時 (最大 25 時間の表示が可能)</span><span class="sxs-lookup"><span data-stu-id="7336c-200">Hourly (a maximum of 25 hours can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="7336c-201">毎日 (最大 31 日の表示が可能)</span><span class="sxs-lookup"><span data-stu-id="7336c-201">Daily (a maximum of 31 days can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="7336c-202">毎週 (最大 12 週の表示が可能)</span><span class="sxs-lookup"><span data-stu-id="7336c-202">Weekly (a maximum of 12 weeks can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="7336c-203">毎月 (最大 12 か月の表示が可能)</span><span class="sxs-lookup"><span data-stu-id="7336c-203">Monthly (a maximum of 12 months can be displayed)</span></span></p></li>
</ul>
<p><span data-ttu-id="7336c-204">開始日と終了日が、選択されている期間内で許容される値の最大数を超えると、(開始日から起算した) 値の最大数のみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7336c-204">If the start and end dates exceed the maximum number of values allowed for the selected interval, only the maximum number of values (starting from the start date) are displayed.</span></span> <span data-ttu-id="7336c-205">たとえば、開始日が7/7/2012 で、終了日が2/28/2012 の [日] 間隔を選択した場合は、8/7/2012 12:00 AM から 9/7/2012 12:00 AM (つまり、31日分のデータ) のデータが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7336c-205">For example, if you select the Daily interval with a start date of 7/7/2012 and an end date of 2/28/2012, data is displayed for the days 8/7/2012 12:00 AM to 9/7/2012 12:00 AM (that is, a total of 31 days' worth of data).</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="7336c-206">指標</span><span class="sxs-lookup"><span data-stu-id="7336c-206">Metrics</span></span>

<span data-ttu-id="7336c-207">次の表に、電話会議の概要レポートで提供される情報を示します。</span><span class="sxs-lookup"><span data-stu-id="7336c-207">The following table the information provided by the Conferences Summary Report.</span></span>

### <a name="conference-summary-report-metrics"></a><span data-ttu-id="7336c-208">電話会議の概要レポートの指標</span><span class="sxs-lookup"><span data-stu-id="7336c-208">Conference Summary Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7336c-209">名前</span><span class="sxs-lookup"><span data-stu-id="7336c-209">Name</span></span></th>
<th><span data-ttu-id="7336c-210">この項目での並べ替え</span><span class="sxs-lookup"><span data-stu-id="7336c-210">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="7336c-211">説明</span><span class="sxs-lookup"><span data-stu-id="7336c-211">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7336c-212"><strong>[毎時]</strong></span><span class="sxs-lookup"><span data-stu-id="7336c-212"><strong>Hourly</strong></span></span></p>
<p><span data-ttu-id="7336c-213"><strong>[毎日]</strong></span><span class="sxs-lookup"><span data-stu-id="7336c-213"><strong>Daily</strong></span></span></p>
<p><span data-ttu-id="7336c-214"><strong>[毎週]</strong></span><span class="sxs-lookup"><span data-stu-id="7336c-214"><strong>Weekly</strong></span></span></p>
<p><span data-ttu-id="7336c-215"><strong>[毎月]</strong></span><span class="sxs-lookup"><span data-stu-id="7336c-215"><strong>Monthly</strong></span></span></p></td>
<td><p><span data-ttu-id="7336c-216">不可</span><span class="sxs-lookup"><span data-stu-id="7336c-216">No</span></span></p></td>
<td><p><span data-ttu-id="7336c-217">フィルター ツール バーで選択した期間を示します。</span><span class="sxs-lookup"><span data-stu-id="7336c-217">Indicates the time interval that you selected on the filter toolbar.</span></span> <span data-ttu-id="7336c-218">場合によっては、特定の期間をクリックして、その期間の詳細情報を表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="7336c-218">Where applicable, you can click a given time interval to view detailed information for that interval.</span></span> <span data-ttu-id="7336c-219">たとえば、毎日の間隔を使用していて、[7/7/2012] をクリックすると、その日付のユーザー登録アクティビティの時間の内訳が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7336c-219">For example, if you are using the Daily interval and you click 7/7/2012, you see an hourly breakdown of user registration activity for that date.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7336c-220"><strong>[電話会議の合計数]</strong></span><span class="sxs-lookup"><span data-stu-id="7336c-220"><strong>Total conferences</strong></span></span></p></td>
<td><p><span data-ttu-id="7336c-221">不可</span><span class="sxs-lookup"><span data-stu-id="7336c-221">No</span></span></p></td>
<td><p><span data-ttu-id="7336c-p113">実施された電話会議の総数です (会議の種類は区別されません)。この項目をクリックすると、選択した期間に対する電話会議動作状況レポートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7336c-p113">Total number of conferences (regardless of conference type) that were held. When you click this item, the report shows you the Conference Activity Report for the selected time period.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7336c-224"><strong>[参加者の合計数]</strong></span><span class="sxs-lookup"><span data-stu-id="7336c-224"><strong>Total participants</strong></span></span></p></td>
<td><p><span data-ttu-id="7336c-225">不可</span><span class="sxs-lookup"><span data-stu-id="7336c-225">No</span></span></p></td>
<td><p><span data-ttu-id="7336c-p114">電話会議に参加したユーザーの総数です。この項目をクリックすると、選択した期間に対する電話会議動作状況レポートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7336c-p114">Total number of people who took part in the conferences. When you click this item, the report shows you the Conference Activity Report for the selected time period.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7336c-228"><strong>[電話会議 1 件あたりの平均参加者数]</strong></span><span class="sxs-lookup"><span data-stu-id="7336c-228"><strong>Average participants per conference</strong></span></span></p></td>
<td><p><span data-ttu-id="7336c-229">不可</span><span class="sxs-lookup"><span data-stu-id="7336c-229">No</span></span></p></td>
<td><p><span data-ttu-id="7336c-p115">1 件の電話会議に参加した平均ユーザー数です。電話会議の合計数を参加者の合計数で割ることで求められます。</span><span class="sxs-lookup"><span data-stu-id="7336c-p115">Average number of people who took part in a given conference. Determined by dividing the total conferences by the total participants.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7336c-232"><strong>[音声ビデオ会議の合計数]</strong></span><span class="sxs-lookup"><span data-stu-id="7336c-232"><strong>Total A/V conferences</strong></span></span></p></td>
<td><p><span data-ttu-id="7336c-233">不可</span><span class="sxs-lookup"><span data-stu-id="7336c-233">No</span></span></p></td>
<td><p><span data-ttu-id="7336c-234">音声またはビデオを利用した会議の総数です。</span><span class="sxs-lookup"><span data-stu-id="7336c-234">Total number of conferences that included audio or video.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7336c-235"><strong>[音声ビデオ会議の合計時間 (分)]</strong></span><span class="sxs-lookup"><span data-stu-id="7336c-235"><strong>Total A/V conference minutes</strong></span></span></p></td>
<td><p><span data-ttu-id="7336c-236">不可</span><span class="sxs-lookup"><span data-stu-id="7336c-236">No</span></span></p></td>
<td><p><span data-ttu-id="7336c-237">音声ビデオ会議に費やされた合計時間を分単位で表したものです。</span><span class="sxs-lookup"><span data-stu-id="7336c-237">Total number of minutes devoted to audio/video conferencing.</span></span></p>
<p><span data-ttu-id="7336c-238">トータル A/V 会議の分単位の料金は、オーディオ/ビジュアル会議の種類 (A/V 会議など) をまとめたものです。IM 会議アプリ共有会議データ会議[PSTN 会議] を選びます。</span><span class="sxs-lookup"><span data-stu-id="7336c-238">The Total A/V conference minutes metric summarizes all the audio/visual conference types, including: A/V conferences; IM conferences; app sharing conferences; data conferences; and PSTN conferences.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7336c-239"><strong>[音声ビデオ会議参加者の合計時間 (分)]</strong></span><span class="sxs-lookup"><span data-stu-id="7336c-239"><strong>Total A/V conference participant minutes</strong></span></span></p></td>
<td><p><span data-ttu-id="7336c-240">不可</span><span class="sxs-lookup"><span data-stu-id="7336c-240">No</span></span></p></td>
<td><p><span data-ttu-id="7336c-p116">参加者が音声ビデオ会議に費やした合計時間を分単位で表したものです。たとえば、あるユーザーが音声ビデオ会議に 5 分費やし、別のユーザーが同じ会議に 3 分費やしたとします。この場合、会議参加者の合計時間は 8 分 (= 5 分 + 3 分) となります。</span><span class="sxs-lookup"><span data-stu-id="7336c-p116">Total number of participant minutes devoted to audio/video conferencing. For example, suppose one user spends 5 minutes in an audio/video conference and a second user spends 3 minutes in that same conference. That makes a total of 8 participant minutes: 5 minutes plus 3 minutes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7336c-244"><strong>[音声ビデオ会議の平均時間 (分)]</strong></span><span class="sxs-lookup"><span data-stu-id="7336c-244"><strong>Average A/V conference minutes</strong></span></span></p></td>
<td><p><span data-ttu-id="7336c-245">不可</span><span class="sxs-lookup"><span data-stu-id="7336c-245">No</span></span></p></td>
<td><p><span data-ttu-id="7336c-246">音声ビデオ会議 1 件あたりの平均時間を分単位で表したものです。</span><span class="sxs-lookup"><span data-stu-id="7336c-246">Average number of minutes per audio/video conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7336c-247"><strong>[電話会議の一意な開催者の合計数]</strong></span><span class="sxs-lookup"><span data-stu-id="7336c-247"><strong>Total number of unique organizers of conferences</strong></span></span></p></td>
<td><p><span data-ttu-id="7336c-248">不可</span><span class="sxs-lookup"><span data-stu-id="7336c-248">No</span></span></p></td>
<td><p><span data-ttu-id="7336c-p117">少なくとも 1 件の電話会議を開催したユーザーの総数です。複数の電話会議を開催したユーザーも、電話会議を 1 件しか開催していないユーザーと同じように、一意の開催者 1 人分としてカウントされます。</span><span class="sxs-lookup"><span data-stu-id="7336c-p117">Total number of users who organized at least one conference. Users who organized more than one conference are counted as one unique organizer, just like users who only organized a single conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7336c-251"><strong>[電話会議メッセージの合計数]</strong></span><span class="sxs-lookup"><span data-stu-id="7336c-251"><strong>Total conference messages</strong></span></span></p></td>
<td><p><span data-ttu-id="7336c-252">不可</span><span class="sxs-lookup"><span data-stu-id="7336c-252">No</span></span></p></td>
<td><p><span data-ttu-id="7336c-253">電話会議中に送信されたインスタント メッセージの総数です。</span><span class="sxs-lookup"><span data-stu-id="7336c-253">Total number of instant messages sent during the conferences.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="7336c-254">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7336c-254">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

