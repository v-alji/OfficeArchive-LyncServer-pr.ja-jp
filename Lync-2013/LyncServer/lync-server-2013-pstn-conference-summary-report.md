---
title: 'Lync Server 2013: PSTN 会議の概要レポート'
description: 'Lync Server 2013: PSTN 会議の概要レポート。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: PSTN Conference Summary Report
ms:assetid: 8e2f0862-4dfa-4c2b-bf8d-ad71419f15d2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615014(v=OCS.15)
ms:contentKeyID: 48184764
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c3bc468e494577c229562a1cb7cfddaf839f946f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436728"
---
# <a name="pstn-conference-summary-report-in-lync-server-2013"></a><span data-ttu-id="a228f-103">Lync Server 2013 の PSTN 会議の概要レポート</span><span class="sxs-lookup"><span data-stu-id="a228f-103">PSTN Conference Summary Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a228f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a228f-104">

<span> </span></span></span>

<span data-ttu-id="a228f-105">_**最終更新日:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="a228f-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="a228f-106">Microsoft Lync Server 2013 の PSTN 会議は、PSTN (公衆交換電話網) 電話を使って、少なくとも1人の参加者がオーディオ部分にダイヤルインする会議です。</span><span class="sxs-lookup"><span data-stu-id="a228f-106">In Microsoft Lync Server 2013, a PSTN conference is any conference in which at least one participant dials in to the audio portion by a using a PSTN (public switched telephone network) phone.</span></span> <span data-ttu-id="a228f-107">(PSTN 電話とは、"固定電話"、携帯電話、またはボイスオーバー IP を使用しないその他の任意の電話のことです)。監視レポートでは PSTN 会議と呼ばれていますが、このような会議は、一般的にダイヤルイン会議と呼ばれることがあります。</span><span class="sxs-lookup"><span data-stu-id="a228f-107">(A PSTN phone is a "landline," a cell phone, or any other phone which does not make use of Voice over IP.) Although referred to as PSTN conferences in the Monitoring Reports, these conferences are perhaps more-commonly known as dial-in conferences.</span></span>

<span data-ttu-id="a228f-p102">PSTN 電話会議の概要レポートは、組織で開催されるすべての PSTN 電話会議 (つまり、少なくとも 1 人のダイヤルイン ユーザーがいたすべての電話会議) に関する情報を提供します。レポートには、PSTN 電話会議の総数、これらの電話会議に参加した人数の合計、およびおそらく最も重要なダイヤルイン ユーザーの総数 (PSTN 参加者の合計数指標) に関する情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a228f-p102">The PSTN Conference Summary Report provides information about all the PSTN conferences held in your organization (that is, all the conferences that had at least one dial-in user). The report includes information about the total number of PSTN conferences, the total number of people who participated in those conferences, and, perhaps, most important, the total number of dial-in users (the Total PSTN participants metric).</span></span>

<div>

## <a name="accessing-the-pstn-conference-summary-report"></a><span data-ttu-id="a228f-110">PSTN 電話会議の概要レポートへのアクセス</span><span class="sxs-lookup"><span data-stu-id="a228f-110">Accessing the PSTN Conference Summary Report</span></span>

<span data-ttu-id="a228f-p103">PSTN 電話会議の概要レポートには、監視レポートのホーム ページからのみアクセスできます。このレポートは、他のどのレポートともリンクされていません。個々のエンドポイントがこの情報の送信を担当することを理由の一部として、PSTN 電話会議の詳細な通話情報は取得できません。PSTN 電話は、通話詳細情報を追跡または送信できません。</span><span class="sxs-lookup"><span data-stu-id="a228f-p103">The PSTN Conference Summary Report can only be accessed from the Monitoring Reports home page. This report is not linked to any other reports. Note that you cannot retrieve detailed call information for a PSTN conference, in part because individual endpoints are responsible for submitting this information. PSTN phones are not capable of tracking or submitting call detail information.</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-pstn-conference-summary-report"></a><span data-ttu-id="a228f-115">PSTN 電話会議の概要レポートの最適な利用</span><span class="sxs-lookup"><span data-stu-id="a228f-115">Making the Best Use of the PSTN Conference Summary Report</span></span>

<span data-ttu-id="a228f-116">ダイヤルインユーザーを含むすべての会議の割合を判断するには、PSTN 会議の合計数と、 [Lync Server 2013 の [会議の概要] レポート](lync-server-2013-conference-summary-report.md)で検出された会議の評価指標の合計の値とを比較します。</span><span class="sxs-lookup"><span data-stu-id="a228f-116">To determine the percentage of all your conferences that include dial-in users, compare the value of the Total PSTN conferences metric with the Total conferences metric found on the [Conference Summary Report in Lync Server 2013](lync-server-2013-conference-summary-report.md).</span></span>

<span data-ttu-id="a228f-117">期待していた数の PSTN 会議が表示されない場合は、ダイヤルインユーザーを許可する会議を開催する機能は、ユーザーに割り当てられている会議ポリシーによって異なることに注意してください。 PSTN 会議の開催が許可されているユーザーの数が多い場合は、PSTN 会議が少なくともあります。</span><span class="sxs-lookup"><span data-stu-id="a228f-117">If you don't see as many PSTN conferences as you might have expected to see, keep in mind that the ability to organize a conference that allows dial-in users depends on the conferencing policy that has been assigned to a user: if very few of your users are allowed to hold PSTN conferences you would obviously see very few PSTN conferences.</span></span> <span data-ttu-id="a228f-118">会議ポリシー (該当する場合) が、Lync Server 管理シェル内から次のコマンドを実行して、PSTN 会議をスケジュールできるかどうかを簡単に確認できます。</span><span class="sxs-lookup"><span data-stu-id="a228f-118">You can quickly verify which of your conferencing policies (if any) allow users to schedule PSTN conferences by running the following command from within the Lync Server Management Shell:</span></span>

    Get-CsConferencingPolicy | Select-Object Identity, EnableDialInConferencing

<span data-ttu-id="a228f-119">この結果、次のようなデータが返されます。</span><span class="sxs-lookup"><span data-stu-id="a228f-119">That will return data similar to this:</span></span>

    Identity                                EnableDialInConferencing
    --------                                ------------------------
    Global                                                      True
    site:Redmond                                               False
    site:Dublin                                                False
    Tag:RedmondDialInUsers                                      True
    Tag:DublinDialInUsers                                       True

<span data-ttu-id="a228f-120">この結果、次のようなデータが返されます。</span><span class="sxs-lookup"><span data-stu-id="a228f-120">That will return data similar to this:</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="a228f-121">フィルター</span><span class="sxs-lookup"><span data-stu-id="a228f-121">Filters</span></span>

<span data-ttu-id="a228f-122">フィルターは、細かく絞り込んだデータ セットを返したり、返されたデータをさまざまな方法で表示したりする方法として利用できます。</span><span class="sxs-lookup"><span data-stu-id="a228f-122">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways.</span></span> <span data-ttu-id="a228f-123">たとえば、PSTN 電話会議の概要レポートでは、データをグループ化する方法を選択できます。</span><span class="sxs-lookup"><span data-stu-id="a228f-123">For example, the PSTN Conference Summary Report enables you to choose how data should be grouped.</span></span> <span data-ttu-id="a228f-124">その場合は、電話会議が時間、日、週、または月の単位でグループ化されます。</span><span class="sxs-lookup"><span data-stu-id="a228f-124">In this case, conferences are grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="a228f-125">次の表に、PSTN 電話会議の概要レポートで使用できるフィルターを示します。</span><span class="sxs-lookup"><span data-stu-id="a228f-125">The following table lists the filters that you can use with the PSTN Conference Summary Report.</span></span>

### <a name="pstn-conference-summary-report-filters"></a><span data-ttu-id="a228f-126">PSTN 電話会議の概要レポートのフィルター</span><span class="sxs-lookup"><span data-stu-id="a228f-126">PSTN Conference Summary Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a228f-127">名前</span><span class="sxs-lookup"><span data-stu-id="a228f-127">Name</span></span></th>
<th><span data-ttu-id="a228f-128">説明</span><span class="sxs-lookup"><span data-stu-id="a228f-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a228f-129"><strong>開始</strong></span><span class="sxs-lookup"><span data-stu-id="a228f-129"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="a228f-p106">時間範囲の開始日と開始時刻。データを時間単位で表示するには、次のように開始日と開始時刻の両方を入力します。</span><span class="sxs-lookup"><span data-stu-id="a228f-p106">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="a228f-132">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="a228f-132">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="a228f-p107">開始時刻を入力しないと、レポートは自動的に指定日の午前 12:00 に開始します。データを日単位で表示するには、次のように日付のみを入力します。</span><span class="sxs-lookup"><span data-stu-id="a228f-p107">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="a228f-135">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="a228f-135">7/7/2012</span></span></p>
<p><span data-ttu-id="a228f-136">週単位または月単位で表示するには、表示する週または月の任意の日付を入力します (その週または月の最初の日である必要はありません)。</span><span class="sxs-lookup"><span data-stu-id="a228f-136">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="a228f-137">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="a228f-137">7/3/2012</span></span></p>
<p><span data-ttu-id="a228f-138">一週間は、日曜日から始まり、土曜日で終わるものとします。</span><span class="sxs-lookup"><span data-stu-id="a228f-138">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a228f-139"><strong>終了</strong></span><span class="sxs-lookup"><span data-stu-id="a228f-139"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="a228f-p108">時間範囲の終了日と終了時刻。データを時間単位で表示するには、次のように終了日と終了時刻の両方を入力します。</span><span class="sxs-lookup"><span data-stu-id="a228f-p108">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="a228f-142">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="a228f-142">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="a228f-p109">終了時刻を入力しないと、レポートは自動的に指定日の午前 12:00 に終了します。データを日単位で表示するには、次のように日付のみを入力します。</span><span class="sxs-lookup"><span data-stu-id="a228f-p109">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="a228f-145">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="a228f-145">7/7/2012</span></span></p>
<p><span data-ttu-id="a228f-146">週単位または月単位で表示するには、表示する週または月の任意の日付を入力します (その週または月の最初の日である必要はありません)。</span><span class="sxs-lookup"><span data-stu-id="a228f-146">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="a228f-147">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="a228f-147">7/3/2012</span></span></p>
<p><span data-ttu-id="a228f-148">一週間は、日曜日から始まり、土曜日で終わるものとします。</span><span class="sxs-lookup"><span data-stu-id="a228f-148">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a228f-149"><strong>[間隔]</strong></span><span class="sxs-lookup"><span data-stu-id="a228f-149"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="a228f-p110">時間間隔です。次のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="a228f-p110">Time interval. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="a228f-152">毎時 (最大 25 時間の表示が可能)</span><span class="sxs-lookup"><span data-stu-id="a228f-152">Hourly (a maximum of 25 hours can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="a228f-153">毎日 (最大 31 日の表示が可能)</span><span class="sxs-lookup"><span data-stu-id="a228f-153">Daily (a maximum of 31 days can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="a228f-154">毎週 (最大 12 週の表示が可能)</span><span class="sxs-lookup"><span data-stu-id="a228f-154">Weekly (a maximum of 12 weeks can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="a228f-155">毎月 (最大 12 か月の表示が可能)</span><span class="sxs-lookup"><span data-stu-id="a228f-155">Monthly (a maximum of 12 months can be displayed)</span></span></p></li>
</ul>
<p><span data-ttu-id="a228f-156">入力した開始日と終了日が選択した間隔で使用できる値の最大数を超える場合は、最大数の値 (開始日からカウント) のみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a228f-156">If the start and end dates exceed the maximum number of values allowed for the selected interval, only the maximum number of values (starting from the start date) is displayed.</span></span> <span data-ttu-id="a228f-157">たとえば、開始日が7/7/2012 で、終了日が2/28/2012 の [日] 間隔を選択した場合は、8/7/2012 12:00 AM から 9/7/2012 12:00 AM (つまり、31日分のデータ) のデータが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a228f-157">For example, if you select the Daily interval with a start date of 7/7/2012 and an end date of 2/28/2012, data is displayed for the days 8/7/2012 12:00 AM to 9/7/2012 12:00 AM (that is, a total of 31 days' worth of data).</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="a228f-158">指標</span><span class="sxs-lookup"><span data-stu-id="a228f-158">Metrics</span></span>

<span data-ttu-id="a228f-159">次の表に、PSTN 電話会議の概要レポートの情報を示します。</span><span class="sxs-lookup"><span data-stu-id="a228f-159">The following table lists the information in the PSTN Conference Summary Report.</span></span>

### <a name="pstn-conference-summary-report-metrics"></a><span data-ttu-id="a228f-160">PSTN 電話会議の概要レポートの指標</span><span class="sxs-lookup"><span data-stu-id="a228f-160">PSTN Conference Summary Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a228f-161">名前</span><span class="sxs-lookup"><span data-stu-id="a228f-161">Name</span></span></th>
<th><span data-ttu-id="a228f-162">この項目での並べ替え</span><span class="sxs-lookup"><span data-stu-id="a228f-162">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="a228f-163">説明</span><span class="sxs-lookup"><span data-stu-id="a228f-163">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a228f-164"><strong>[毎時]</strong></span><span class="sxs-lookup"><span data-stu-id="a228f-164"><strong>Hourly</strong></span></span></p>
<p><span data-ttu-id="a228f-165"><strong>[毎日]</strong></span><span class="sxs-lookup"><span data-stu-id="a228f-165"><strong>Daily</strong></span></span></p>
<p><span data-ttu-id="a228f-166"><strong>[毎週]</strong></span><span class="sxs-lookup"><span data-stu-id="a228f-166"><strong>Weekly</strong></span></span></p>
<p><span data-ttu-id="a228f-167"><strong>[毎月]</strong></span><span class="sxs-lookup"><span data-stu-id="a228f-167"><strong>Monthly</strong></span></span></p></td>
<td><p><span data-ttu-id="a228f-168">不可</span><span class="sxs-lookup"><span data-stu-id="a228f-168">No</span></span></p></td>
<td><p><span data-ttu-id="a228f-169">選択されている時間間隔を示します。</span><span class="sxs-lookup"><span data-stu-id="a228f-169">Indicates the selected time interval.</span></span> <span data-ttu-id="a228f-170">必要に応じて、特定の時間間隔をクリックして、その間隔の詳細な情報を表示できます。</span><span class="sxs-lookup"><span data-stu-id="a228f-170">Where applicable, you can click a given time interval to view detailed information for that interval.</span></span> <span data-ttu-id="a228f-171">たとえば、毎日の間隔を使用していて、[7/7/2012] をクリックすると、その日付のユーザー登録アクティビティの時間の内訳が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a228f-171">For example, if you are using the Daily interval and you click 7/7/2012, you see an hourly breakdown of user registration activity for that date.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a228f-172"><strong>[PSTN 電話会議の合計数]</strong></span><span class="sxs-lookup"><span data-stu-id="a228f-172"><strong>Total PSTN conferences</strong></span></span></p></td>
<td><p><span data-ttu-id="a228f-173">不可</span><span class="sxs-lookup"><span data-stu-id="a228f-173">No</span></span></p></td>
<td><p><span data-ttu-id="a228f-174">ダイヤルイン アクセスが許可された電話会議の総数です。</span><span class="sxs-lookup"><span data-stu-id="a228f-174">Total number conferences that allowed dial-in access.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a228f-175"><strong>[参加者の合計数]</strong></span><span class="sxs-lookup"><span data-stu-id="a228f-175"><strong>Total participants</strong></span></span></p></td>
<td><p><span data-ttu-id="a228f-176">不可</span><span class="sxs-lookup"><span data-stu-id="a228f-176">No</span></span></p></td>
<td><p><span data-ttu-id="a228f-177">ダイヤルイン アクセスが許可された電話会議に参加したユーザーの総数です。</span><span class="sxs-lookup"><span data-stu-id="a228f-177">Total number of people who participated in conferences that allowed dial-in access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a228f-178"><strong>[音声ビデオ会議の合計時間 (分)]</strong></span><span class="sxs-lookup"><span data-stu-id="a228f-178"><strong>Total A/V conference minutes</strong></span></span></p></td>
<td><p><span data-ttu-id="a228f-179">不可</span><span class="sxs-lookup"><span data-stu-id="a228f-179">No</span></span></p></td>
<td><p><span data-ttu-id="a228f-180">音声ビデオ会議の合計時間です。</span><span class="sxs-lookup"><span data-stu-id="a228f-180">Total amount of audio/visual conference time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a228f-181"><strong>[音声ビデオ会議参加者の合計時間 (分)]</strong></span><span class="sxs-lookup"><span data-stu-id="a228f-181"><strong>Total A/V conference participant minutes</strong></span></span></p></td>
<td><p><span data-ttu-id="a228f-182">不可</span><span class="sxs-lookup"><span data-stu-id="a228f-182">No</span></span></p></td>
<td><p><span data-ttu-id="a228f-p113">参加者が音声ビデオ会議に費やした合計時間です。たとえば、ある参加者が音声ビデオ会議に 5 分費やし、別の参加者が同じ会議に 3 分費やした場合、音声ビデオ会議参加者の合計時間は 8 分になります。</span><span class="sxs-lookup"><span data-stu-id="a228f-p113">Total amount of audio/visual participant time. For example, if one participant spent five minutes in an A/V conference and another participant spent three minutes in the same conference, the total A/V conference participant time would be eight minutes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a228f-185"><strong>[PSTN 参加者の合計数]</strong></span><span class="sxs-lookup"><span data-stu-id="a228f-185"><strong>Total PSTN participants</strong></span></span></p></td>
<td><p><span data-ttu-id="a228f-186">不可</span><span class="sxs-lookup"><span data-stu-id="a228f-186">No</span></span></p></td>
<td><p><span data-ttu-id="a228f-187">ダイヤルイン アクセスが許可された電話会議にダイヤルインしたユーザーの総数です。</span><span class="sxs-lookup"><span data-stu-id="a228f-187">Total number of users who dialed in to conferences that allowed dial-in access.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a228f-188"><strong>[PSTN 参加者の合計時間 (分)]</strong></span><span class="sxs-lookup"><span data-stu-id="a228f-188"><strong>Total PSTN participant minutes</strong></span></span></p></td>
<td><p><span data-ttu-id="a228f-189">不可</span><span class="sxs-lookup"><span data-stu-id="a228f-189">No</span></span></p></td>
<td><p><span data-ttu-id="a228f-p114">ダイヤルイン ユーザーが電話会議に費やした合計時間です。たとえば、あるダイヤルイン参加者が電話会議に 5 分費やし、別の参加者が同じ電話会議に 3 分費やした場合、PSTN 参加者の合計時間は 8 分になります。</span><span class="sxs-lookup"><span data-stu-id="a228f-p114">Total amount of conference time spent by dial-in users. For example, if one dial-in participant spent five minutes in a conference and another participant spent three minutes in the same conference, the total PSTN participant time would be eight minutes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a228f-192"><strong>[一意の電話会議開催者]</strong></span><span class="sxs-lookup"><span data-stu-id="a228f-192"><strong>Unique conference organizers</strong></span></span></p></td>
<td><p><span data-ttu-id="a228f-193">不可</span><span class="sxs-lookup"><span data-stu-id="a228f-193">No</span></span></p></td>
<td><p><span data-ttu-id="a228f-p115">ダイヤルイン アクセスが許可された電話会議を少なくとも 1 件開催したユーザーの総数です。複数の電話会議を開催したユーザーも、電話会議を 1 件しか開催していないユーザーと同じように、一意の開催者 1 人分としてカウントされます。</span><span class="sxs-lookup"><span data-stu-id="a228f-p115">Total number of users who organized at least one conference that allowed dial-in access. Users who organized more than one conference are counted as one unique organizer, just like users who only organized a single conference.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="a228f-196">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a228f-196">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

