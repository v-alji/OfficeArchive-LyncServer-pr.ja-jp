---
title: 'Lync Server 2013: ピアツーピアの音声とビデオのレポート'
description: 'Lync Server 2013: ピアツーピアの音声とビデオのレポート。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Peer-to-Peer Voice and Video Report
ms:assetid: e17c36b5-5a2f-4673-9696-3b2d31c2bb2f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615040(v=OCS.15)
ms:contentKeyID: 48185535
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 43041926b3d6b57508b6ee4c53ca9cb055bcb348
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424695"
---
# <a name="peer-to-peer-voice-and-video-report-in-lync-server-2013"></a><span data-ttu-id="be444-103">Lync Server 2013 のピアツーピア音声とビデオレポート</span><span class="sxs-lookup"><span data-stu-id="be444-103">Peer-to-Peer Voice and Video Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="be444-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="be444-104">

<span> </span></span></span>

<span data-ttu-id="be444-105">_**最終更新日:** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="be444-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="be444-p101">ピアツーピア音声およびビデオ レポートは、指定した期間における音声通話やビデオ通話の配信に関する詳細を提供します (たとえば、1 時間あたりの通話回数または 1 日あたりの通話回数)。また、行われたすべての音声通話とビデオ通話を表示したり、正常な通話または失敗した通話のみを表示したりできます。レポートでは、次のグループに分割した通話情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="be444-p101">The Peer-to-Peer Voice and Video Report provides a detailed look at the distribution of voice and video calls over a specified period of time (for example, calls per hour or calls per day). The report also gives you the option of viewing all the voice and video calls that were made, or of viewing only the successful or failed calls. The reports shows call information broken down into the following groupings:</span></span>

  - <span data-ttu-id="be444-109">プール別の通話</span><span class="sxs-lookup"><span data-stu-id="be444-109">Calls per pool</span></span>

  - <span data-ttu-id="be444-110">通話の種類 (Lync から Lync への通話、および PSTN ネットワーク上のユーザーへの Lync 通話など) ごとの通話</span><span class="sxs-lookup"><span data-stu-id="be444-110">Calls per call type (for example, a Lync to Lync call vs. a Lync call to a person on the PSTN network)</span></span>

  - <span data-ttu-id="be444-111">アクセスの種類別の通話 (内部ネットワークにログオンしているユーザー、外部ネットワークにログオンしているユーザー)</span><span class="sxs-lookup"><span data-stu-id="be444-111">Calls per access type (users logged on to the internal network vs. users logged on to the external network)</span></span>

  - <span data-ttu-id="be444-112">仲介サーバーあたりの通話</span><span class="sxs-lookup"><span data-stu-id="be444-112">Calls per Mediation Server</span></span>

<div>

## <a name="to-access-the-peer-to-peer-voice-and-video-report"></a><span data-ttu-id="be444-113">ピアツーピア音声およびビデオ レポートにアクセスするには</span><span class="sxs-lookup"><span data-stu-id="be444-113">To access the peer-to-peer voice and video report</span></span>

<span data-ttu-id="be444-114">ピアツーピア音声およびビデオ レポートにアクセスするには、ピアツーピア アクティビティ概要レポートを開き、次のいずれかの指標をクリックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="be444-114">You can access the Peer-to-Peer Voice and Video Report only by opening the Peer-to-Peer Activity Summary Report and then clicking any of the following metrics:</span></span>

  - <span data-ttu-id="be444-115">ピアツーピア音声セッションの合計数</span><span class="sxs-lookup"><span data-stu-id="be444-115">Total peer-to-peer audio sessions</span></span>

  - <span data-ttu-id="be444-116">ピアツーピア音声セッションの合計時間</span><span class="sxs-lookup"><span data-stu-id="be444-116">Total peer-to-peer audio minutes</span></span>

  - <span data-ttu-id="be444-117">ピアツーピア ビデオ セッションの合計数</span><span class="sxs-lookup"><span data-stu-id="be444-117">Total peer-to-peer video sessions</span></span>

  - <span data-ttu-id="be444-118">ピアツーピア ビデオ セッションの合計時間</span><span class="sxs-lookup"><span data-stu-id="be444-118">Total peer-to-peer video minutes</span></span>

</div>

<div>

## <a name="to-make-the-best-use-of-the-peer-to-peer-voice-and-video-report"></a><span data-ttu-id="be444-119">ピアツーピア音声およびビデオ レポートを最大限に活用するには</span><span class="sxs-lookup"><span data-stu-id="be444-119">To make the best use of the peer-to-peer voice and video report</span></span>

<span data-ttu-id="be444-p102">ピアツーピア音声およびビデオ レポートをフィルターするさまざまな方法があります。ただし、既定では、これらのフィルター オプションは非表示になっています。使用できるフィルター オプションを表示するには、[レポート] ウィンドウの右上隅にある [**パラメーターの表示/非表示**] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="be444-p102">There are a number of ways you can filter the Peer-to-Peer Voice and Video Report. However, those filtering options are hidden from view by default. To view the filtering options available to you, click **Show/Hide Parameters** button in the upper-right corner of the Report window.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="be444-123">フィルター</span><span class="sxs-lookup"><span data-stu-id="be444-123">Filters</span></span>

<span data-ttu-id="be444-p103">フィルターは、細かく絞り込んだデータ セットを返したり、データをさまざまな方法で表示したりする方法として利用できます。次の表に、ピアツーピア音声およびビデオ レポートで使用できるフィルターを示します。</span><span class="sxs-lookup"><span data-stu-id="be444-p103">Filters provide a way for you to return a more finely targeted set of data or to view the data in different ways. The following table lists the filters that you can use with the Peer-to-Peer Voice and Video Report.</span></span>

### <a name="peer-to-peer-voice-and-video-report-filters"></a><span data-ttu-id="be444-126">ピアツーピア音声およびビデオ レポートのフィルター</span><span class="sxs-lookup"><span data-stu-id="be444-126">Peer-to-peer voice and video report filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="be444-127">名前</span><span class="sxs-lookup"><span data-stu-id="be444-127">Name</span></span></th>
<th><span data-ttu-id="be444-128">説明</span><span class="sxs-lookup"><span data-stu-id="be444-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be444-129"><strong>開始</strong></span><span class="sxs-lookup"><span data-stu-id="be444-129"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="be444-p104">時間範囲の開始日と開始時刻。データを時間単位で表示するには、次のように開始日と開始時刻の両方を入力します。</span><span class="sxs-lookup"><span data-stu-id="be444-p104">Start date and time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="be444-132">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="be444-132">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="be444-p105">開始時刻を入力しないと、レポートは自動的に指定日の午前 12:00 に開始します。データを日単位で表示するには、次のように日付のみを入力します。</span><span class="sxs-lookup"><span data-stu-id="be444-p105">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="be444-135">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="be444-135">7/7/2012</span></span></p>
<p><span data-ttu-id="be444-136">週単位または月単位で表示するには、表示する週または月の任意の日付を入力します (その週または月の最初の日である必要はありません)。</span><span class="sxs-lookup"><span data-stu-id="be444-136">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="be444-137">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="be444-137">7/3/2012</span></span></p>
<p><span data-ttu-id="be444-138">一週間は、日曜日から始まり、土曜日で終わるものとします。</span><span class="sxs-lookup"><span data-stu-id="be444-138">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be444-139"><strong>終了</strong></span><span class="sxs-lookup"><span data-stu-id="be444-139"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="be444-p106">時間範囲の終了日と終了時刻。データを時間単位で表示するには、次のように終了日と終了時刻の両方を入力します。</span><span class="sxs-lookup"><span data-stu-id="be444-p106">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="be444-142">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="be444-142">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="be444-p107">終了時刻を入力しないと、レポートは自動的に指定日の午前 12:00 に終了します。データを日単位で表示するには、次のように日付のみを入力します。</span><span class="sxs-lookup"><span data-stu-id="be444-p107">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="be444-145">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="be444-145">7/7/2012</span></span></p>
<p><span data-ttu-id="be444-146">週単位または月単位で表示するには、表示する週または月の任意の日付を入力します (その週または月の最初の日である必要はありません)。</span><span class="sxs-lookup"><span data-stu-id="be444-146">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="be444-147">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="be444-147">7/3/2012</span></span></p>
<p><span data-ttu-id="be444-148">一週間は、日曜日から始まり、土曜日で終わるものとします。</span><span class="sxs-lookup"><span data-stu-id="be444-148">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be444-149"><strong>[間隔]</strong></span><span class="sxs-lookup"><span data-stu-id="be444-149"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="be444-p108">時間間隔です。次のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="be444-p108">Time interval. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="be444-152">毎時 (最大 25 時間の表示が可能)</span><span class="sxs-lookup"><span data-stu-id="be444-152">Hourly (a maximum of 25 hours can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="be444-153">毎日 (最大 31 日の表示が可能)</span><span class="sxs-lookup"><span data-stu-id="be444-153">Daily (a maximum of 31 days can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="be444-154">毎週 (最大 12 週の表示が可能)</span><span class="sxs-lookup"><span data-stu-id="be444-154">Weekly (a maximum of 12 weeks can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="be444-155">毎月 (最大 12 か月の表示が可能)</span><span class="sxs-lookup"><span data-stu-id="be444-155">Monthly (a maximum of 12 months can be displayed)</span></span></p></li>
</ul>
<p><span data-ttu-id="be444-156">入力した開始日と終了日が選択した間隔で使用できる値の最大数を超える場合は、最大数の値 (開始日からカウント) のみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="be444-156">If the start and end dates exceed the maximum number of values allowed for the selected interval, only the maximum number of values (starting from the start date) is displayed.</span></span> <span data-ttu-id="be444-157">たとえば、開始日が7/7/2012 で、終了日が2/28/2012 の [日] 間隔を選択した場合は、8/7/2012 12:00 AM から 9/7/2012 12:00 AM (つまり、31日分のデータ) のデータが表示されます。</span><span class="sxs-lookup"><span data-stu-id="be444-157">For example, if you select the Daily interval with a start date of 7/7/2012 and an end date of 2/28/2012, data is displayed for the days 8/7/2012 12:00 AM to 9/7/2012 12:00 AM (that is, a total of 31 days' worth of data).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be444-158"><strong>メディアの種類</strong></span><span class="sxs-lookup"><span data-stu-id="be444-158"><strong>Media type</strong></span></span></p></td>
<td><p><span data-ttu-id="be444-p110">セッションで使用されたメディアの種類を示します。次のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="be444-p110">Indicates the type of media used in the session. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="be444-161">両方</span><span class="sxs-lookup"><span data-stu-id="be444-161">Both</span></span></p></li>
<li><p><span data-ttu-id="be444-162">音声</span><span class="sxs-lookup"><span data-stu-id="be444-162">Audio</span></span></p></li>
<li><p><span data-ttu-id="be444-163">ビデオ</span><span class="sxs-lookup"><span data-stu-id="be444-163">Video</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be444-164"><strong>通話のディスポジション</strong></span><span class="sxs-lookup"><span data-stu-id="be444-164"><strong>Call disposition</strong></span></span></p></td>
<td><p><span data-ttu-id="be444-p111">セッションの成功または失敗を示します。次のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="be444-p111">Indicates the success or failure of the session. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="be444-167">[すべて]</span><span class="sxs-lookup"><span data-stu-id="be444-167">[All]</span></span></p></li>
<li><p><span data-ttu-id="be444-168">成功した通話</span><span class="sxs-lookup"><span data-stu-id="be444-168">Success Calls</span></span></p></li>
<li><p><span data-ttu-id="be444-169">失敗した通話</span><span class="sxs-lookup"><span data-stu-id="be444-169">Failed Calls</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be444-170"><strong>報告元</strong></span><span class="sxs-lookup"><span data-stu-id="be444-170"><strong>Report by</strong></span></span></p></td>
<td><p><span data-ttu-id="be444-p112">レポートで使用する値を指定します。次のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="be444-p112">Indicates the values to be used in the report. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="be444-173">セッション数</span><span class="sxs-lookup"><span data-stu-id="be444-173">Session count</span></span></p></li>
<li><p><span data-ttu-id="be444-174">通話の分数</span><span class="sxs-lookup"><span data-stu-id="be444-174">Call minutes</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-peer-to-peer-voice-and-video-activity-by-pool"></a><span data-ttu-id="be444-175">プール別のピアツーピア音声およびビデオ アクティビティの指標</span><span class="sxs-lookup"><span data-stu-id="be444-175">Metrics for peer-to-peer voice and video activity by Pool</span></span>

<span data-ttu-id="be444-176">次の表に、ピアツーピア音声およびビデオ レポートで各プールについて表示される情報を示します。</span><span class="sxs-lookup"><span data-stu-id="be444-176">The following table lists the information provided in the Peer-to-Peer Voice and Video Report for each pool.</span></span>

### <a name="metrics-for-peer-to-peer-voice-and-video-activity-by-pool"></a><span data-ttu-id="be444-177">プール別のピアツーピア音声およびビデオ アクティビティの指標</span><span class="sxs-lookup"><span data-stu-id="be444-177">Metrics for peer-to-peer voice and video activity by pool</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="be444-178">名前</span><span class="sxs-lookup"><span data-stu-id="be444-178">Name</span></span></th>
<th><span data-ttu-id="be444-179">この項目での並べ替え</span><span class="sxs-lookup"><span data-stu-id="be444-179">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="be444-180">説明</span><span class="sxs-lookup"><span data-stu-id="be444-180">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be444-181"><strong>プール</strong></span><span class="sxs-lookup"><span data-stu-id="be444-181"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="be444-182">不可</span><span class="sxs-lookup"><span data-stu-id="be444-182">No</span></span></p></td>
<td><p><span data-ttu-id="be444-183">通話に使用されるレジストラープールまたはエッジサーバーの名前。</span><span class="sxs-lookup"><span data-stu-id="be444-183">Name of the Registrar pool or Edge Server used for the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be444-184"><strong>日付/時刻</strong></span><span class="sxs-lookup"><span data-stu-id="be444-184"><strong>Date/Time</strong></span></span></p></td>
<td><p><span data-ttu-id="be444-185">不可</span><span class="sxs-lookup"><span data-stu-id="be444-185">No</span></span></p></td>
<td><p><span data-ttu-id="be444-186">通話が行われた日付と時間。</span><span class="sxs-lookup"><span data-stu-id="be444-186">Date and time period in which the call took place.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be444-187"><strong>合計</strong></span><span class="sxs-lookup"><span data-stu-id="be444-187"><strong>Total</strong></span></span></p></td>
<td><p><span data-ttu-id="be444-188">不可</span><span class="sxs-lookup"><span data-stu-id="be444-188">No</span></span></p></td>
<td><p><span data-ttu-id="be444-189">セッション数またはメッセージ数の合計。</span><span class="sxs-lookup"><span data-stu-id="be444-189">Total number of sessions or total message count.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-peer-to-peer-voice-and-video-activity-by-call-type"></a><span data-ttu-id="be444-190">通話の種類別のピアツーピア音声およびビデオ アクティビティの指標</span><span class="sxs-lookup"><span data-stu-id="be444-190">Metrics for peer-to-peer voice and video activity by call type</span></span>

<span data-ttu-id="be444-191">次の表に、ピアツーピア音声およびビデオ レポートで各種類の通話について表示される情報を示します。</span><span class="sxs-lookup"><span data-stu-id="be444-191">The following table lists the information provided in the Peer-to-Peer Voice and Video Report for each type of call that was made.</span></span>

### <a name="metrics-for-peer-to-peer-voice-and-video-activity-by-call-type"></a><span data-ttu-id="be444-192">通話の種類別のピアツーピア音声およびビデオ アクティビティの指標</span><span class="sxs-lookup"><span data-stu-id="be444-192">Metrics for peer-to-peer voice and video activity by call type</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="be444-193">名前</span><span class="sxs-lookup"><span data-stu-id="be444-193">Name</span></span></th>
<th><span data-ttu-id="be444-194">この項目での並べ替え</span><span class="sxs-lookup"><span data-stu-id="be444-194">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="be444-195">説明</span><span class="sxs-lookup"><span data-stu-id="be444-195">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be444-196"><strong>通話の種類</strong></span><span class="sxs-lookup"><span data-stu-id="be444-196"><strong>Call type</strong></span></span></p></td>
<td><p><span data-ttu-id="be444-197">不可</span><span class="sxs-lookup"><span data-stu-id="be444-197">No</span></span></p></td>
<td><p><span data-ttu-id="be444-p113">行われた通話の種類を示します。値は次のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="be444-p113">Indicates the type of call that was made. Values are one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="be444-200">UC 間</span><span class="sxs-lookup"><span data-stu-id="be444-200">UC-to-UC</span></span></p></li>
<li><p><span data-ttu-id="be444-201">UC-PSTN 間</span><span class="sxs-lookup"><span data-stu-id="be444-201">UC-to-PSTN</span></span></p></li>
<li><p><span data-ttu-id="be444-202">PSTN-UC 間</span><span class="sxs-lookup"><span data-stu-id="be444-202">PSTN-to-UC</span></span></p></li>
<li><p><span data-ttu-id="be444-203">PSTN 間</span><span class="sxs-lookup"><span data-stu-id="be444-203">PSTN-to-PSTN</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be444-204"><strong>日付/時刻</strong></span><span class="sxs-lookup"><span data-stu-id="be444-204"><strong>Date/Time</strong></span></span></p></td>
<td><p><span data-ttu-id="be444-205">不可</span><span class="sxs-lookup"><span data-stu-id="be444-205">No</span></span></p></td>
<td><p><span data-ttu-id="be444-206">通話が行われた日付と時間。</span><span class="sxs-lookup"><span data-stu-id="be444-206">Date and time period in which the call took place.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be444-207"><strong>合計</strong></span><span class="sxs-lookup"><span data-stu-id="be444-207"><strong>Total</strong></span></span></p></td>
<td><p><span data-ttu-id="be444-208">不可</span><span class="sxs-lookup"><span data-stu-id="be444-208">No</span></span></p></td>
<td><p><span data-ttu-id="be444-209">セッション数またはメッセージ数の合計。</span><span class="sxs-lookup"><span data-stu-id="be444-209">Total number of sessions or total message count.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-peer-to-peer-voice-and-video-activity-by-access-type"></a><span data-ttu-id="be444-210">アクセスの種類別のピアツーピア音声およびビデオ アクティビティの指標</span><span class="sxs-lookup"><span data-stu-id="be444-210">Metrics for peer-to-peer voice and video activity by access type</span></span>

<span data-ttu-id="be444-211">次の表に、ピアツーピア音声およびビデオ レポートで各種類のアクセスについて表示される情報を示します。</span><span class="sxs-lookup"><span data-stu-id="be444-211">The following table lists the information provided in the Peer-to-Peer Voice and Video Report for each network access type.</span></span>

### <a name="metrics-for-peer-to-peer-voice-and-video-activity-by-access-type"></a><span data-ttu-id="be444-212">アクセスの種類別のピアツーピア音声およびビデオ アクティビティの指標</span><span class="sxs-lookup"><span data-stu-id="be444-212">Metrics for peer-to-peer voice and video activity by access type</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="be444-213">名前</span><span class="sxs-lookup"><span data-stu-id="be444-213">Name</span></span></th>
<th><span data-ttu-id="be444-214">この項目での並べ替え</span><span class="sxs-lookup"><span data-stu-id="be444-214">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="be444-215">説明</span><span class="sxs-lookup"><span data-stu-id="be444-215">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be444-216"><strong>動作状況の種類</strong></span><span class="sxs-lookup"><span data-stu-id="be444-216"><strong>Activity type</strong></span></span></p></td>
<td><p><span data-ttu-id="be444-217">不可</span><span class="sxs-lookup"><span data-stu-id="be444-217">No</span></span></p></td>
<td><p><span data-ttu-id="be444-p114">クライアントが通話時に内部ネットワークにログオンしたか、外部ネットワークにログオンしたかを示します。通常は次のいずれかの値です。</span><span class="sxs-lookup"><span data-stu-id="be444-p114">Indicates whether the clients were logged on to the internal network or the external network when the call was placed. Values are typically one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="be444-220">内部</span><span class="sxs-lookup"><span data-stu-id="be444-220">Internal</span></span></p></li>
<li><p><span data-ttu-id="be444-221">外部</span><span class="sxs-lookup"><span data-stu-id="be444-221">External</span></span></p></li>
<li><p><span data-ttu-id="be444-222">混合</span><span class="sxs-lookup"><span data-stu-id="be444-222">Mixed</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be444-223"><strong>日付/時刻</strong></span><span class="sxs-lookup"><span data-stu-id="be444-223"><strong>Date/Time</strong></span></span></p></td>
<td><p><span data-ttu-id="be444-224">不可</span><span class="sxs-lookup"><span data-stu-id="be444-224">No</span></span></p></td>
<td><p><span data-ttu-id="be444-225">通話が行われた日付と時間。</span><span class="sxs-lookup"><span data-stu-id="be444-225">Date and time period in which the call took place.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be444-226"><strong>合計</strong></span><span class="sxs-lookup"><span data-stu-id="be444-226"><strong>Total</strong></span></span></p></td>
<td><p><span data-ttu-id="be444-227">不可</span><span class="sxs-lookup"><span data-stu-id="be444-227">No</span></span></p></td>
<td><p><span data-ttu-id="be444-228">セッション数またはメッセージ数の合計。</span><span class="sxs-lookup"><span data-stu-id="be444-228">Total number of sessions or total message count.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-peer-to-peer-voice-and-video-activity-by-mediation-server"></a><span data-ttu-id="be444-229">仲介サーバー別のピアツーピア音声およびビデオ アクティビティの指標</span><span class="sxs-lookup"><span data-stu-id="be444-229">Metrics for peer-to-peer voice and video activity by mediation server</span></span>

<span data-ttu-id="be444-230">次の表は、各仲介サーバーのピアツーピア音声およびビデオレポートで提供される情報をまとめたものです。</span><span class="sxs-lookup"><span data-stu-id="be444-230">The following table lists the information provided in the Peer-to-Peer Voice and Video Report for each Mediation Server.</span></span>

### <a name="metrics-for-peer-to-peer-voice-and-video-activity-by-mediation-server"></a><span data-ttu-id="be444-231">仲介サーバー別のピアツーピア音声およびビデオ アクティビティの指標</span><span class="sxs-lookup"><span data-stu-id="be444-231">Metrics for peer-to-peer voice and video activity by mediation server</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="be444-232">名前</span><span class="sxs-lookup"><span data-stu-id="be444-232">Name</span></span></th>
<th><span data-ttu-id="be444-233">この項目での並べ替え</span><span class="sxs-lookup"><span data-stu-id="be444-233">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="be444-234">説明</span><span class="sxs-lookup"><span data-stu-id="be444-234">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be444-235"><strong>仲介サーバー</strong></span><span class="sxs-lookup"><span data-stu-id="be444-235"><strong>Mediation Server</strong></span></span></p></td>
<td><p><span data-ttu-id="be444-236">不可</span><span class="sxs-lookup"><span data-stu-id="be444-236">No</span></span></p></td>
<td><p><span data-ttu-id="be444-237">仲介サーバーの名前。</span><span class="sxs-lookup"><span data-stu-id="be444-237">Name of the Mediation Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be444-238"><strong>日付/時刻</strong></span><span class="sxs-lookup"><span data-stu-id="be444-238"><strong>Date/Time</strong></span></span></p></td>
<td><p><span data-ttu-id="be444-239">不可</span><span class="sxs-lookup"><span data-stu-id="be444-239">No</span></span></p></td>
<td><p><span data-ttu-id="be444-240">通話が行われた日付と時間。</span><span class="sxs-lookup"><span data-stu-id="be444-240">Date and time period in which the call took place.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be444-241"><strong>合計</strong></span><span class="sxs-lookup"><span data-stu-id="be444-241"><strong>Total</strong></span></span></p></td>
<td><p><span data-ttu-id="be444-242">不可</span><span class="sxs-lookup"><span data-stu-id="be444-242">No</span></span></p></td>
<td><p><span data-ttu-id="be444-243">セッション数またはメッセージ数の合計。</span><span class="sxs-lookup"><span data-stu-id="be444-243">Total number of sessions or total message count.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="be444-244">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="be444-244">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

