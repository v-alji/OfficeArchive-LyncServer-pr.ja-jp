---
title: 'Lync Server 2013: 通話受付制御レポート'
description: 'Lync Server 2013: 通話受付制御レポート。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call Admission Control Report
ms:assetid: ea4b0c9f-7f93-4b8a-b901-01e1636c44fb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615043(v=OCS.15)
ms:contentKeyID: 48185933
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8764e51603e7097095894bc1230c2a2bb1126b9c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435783"
---
# <a name="call-admission-control-report-in-lync-server-2013"></a><span data-ttu-id="852de-103">Lync Server 2013 での通話受付制御レポート</span><span class="sxs-lookup"><span data-stu-id="852de-103">Call Admission Control Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="852de-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="852de-104">

<span> </span></span></span>

<span data-ttu-id="852de-105">_**最終更新日:** 2012-06-29_</span><span class="sxs-lookup"><span data-stu-id="852de-105">_**Topic Last Modified:** 2012-06-29_</span></span>

<span data-ttu-id="852de-106">通話受付管理レポートは、通話受付管理によって設けられた制限のもとで行われたピアツーピアおよび電話会議セッションに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="852de-106">The Call Admission Control Report provides information about peer-to-peer and conferencing sessions that were conducted under restrictions set in place by Call Admission Control.</span></span> <span data-ttu-id="852de-107">Microsoft Lync Server 2010 で導入された通話受付制御により、管理者は、帯域幅の制約に基づいて通信セッションを許可 (または許可しない) することができます。</span><span class="sxs-lookup"><span data-stu-id="852de-107">Call Admission Control, introduced in Microsoft Lync Server 2010, provides a way for administrators to allow (or not allow) communication sessions based on bandwidth constraints.</span></span> <span data-ttu-id="852de-108">たとえば、管理者は音声通話やビデオ通話に使用可能な帯域幅を制限するポリシーを作成できます。</span><span class="sxs-lookup"><span data-stu-id="852de-108">For example, administrators can create policies that impose a limit on the amount of bandwidth available for voice and video calls.</span></span> <span data-ttu-id="852de-109">帯域幅の制限に達すると、現在の通話のいずれかが終了して必要なネットワーク リソースが解放されるまで、新しい音声通話やビデオ通話を行うことはできません。</span><span class="sxs-lookup"><span data-stu-id="852de-109">If that bandwidth limit has been reached, then no new voice or video calls can be placed until one of the current calls has ended and freed up the required network resources.</span></span>

<div>

## <a name="accessing-the-call-admission-control-report"></a><span data-ttu-id="852de-110">通話受付管理レポートへのアクセス</span><span class="sxs-lookup"><span data-stu-id="852de-110">Accessing the Call Admission Control Report</span></span>

<span data-ttu-id="852de-p102">通話受付管理レポートは、[監視レポート] ホーム ページからアクセスします。通話受付管理レポートから次のいずれかのレポートへドリルダウンできます。</span><span class="sxs-lookup"><span data-stu-id="852de-p102">The Call Admission Control Report is accessed from the Monitoring Reports home page. From the Call Admission Control Report you can drill down to either of the following reports:</span></span>

  - <span data-ttu-id="852de-113">会議詳細レポート - このレポートにアクセスするには、電話会議セッションの [詳細] 指標をクリックします。</span><span class="sxs-lookup"><span data-stu-id="852de-113">Conference Detail Report – To access this report, click the Details metric from a conference session.</span></span>

  - <span data-ttu-id="852de-114">ピアツーピア セッション詳細レポート - このレポートにアクセスするには、ピアツーピア セッションの [詳細] 指標をクリックします。</span><span class="sxs-lookup"><span data-stu-id="852de-114">Peer-to-Peer Session Detail Report – To access this report, click the Details metric for a peer-to-peer session.</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-call-admission-control-report"></a><span data-ttu-id="852de-115">通話受付管理レポートの活用</span><span class="sxs-lookup"><span data-stu-id="852de-115">Making the Best Use of the Call Admission Control Report</span></span>

<span data-ttu-id="852de-p103">帯域幅が十分になかったために失敗した通話の一覧を表示するには、[通話のカテゴリ] ドロップダウン リストから [通話受付管理のため、拒否された通話] を選択します。ほとんどの返信通話は診断 ID が 5 になります。</span><span class="sxs-lookup"><span data-stu-id="852de-p103">To get a list of calls that failed because of insufficient bandwidth, select Calls rejected because of call admission control from the Call category dropdown list. Most of the returned calls will likely have a diagnostic ID of 5:</span></span>

<span data-ttu-id="852de-p104">セッションを確立するために十分な帯域幅がありません。PSTN 再ルートを試してください。</span><span class="sxs-lookup"><span data-stu-id="852de-p104">Insufficient bandwidth to establish session. Attempt PSTN re-route.</span></span>

<span data-ttu-id="852de-120">通話受付管理の制限によって、VoIP ネットワーク上で通話ができなかったことを示しています。</span><span class="sxs-lookup"><span data-stu-id="852de-120">That indicates that Call Admission Control limitations were preventing the call from being made on the VoIP network.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="852de-121">フィルター</span><span class="sxs-lookup"><span data-stu-id="852de-121">Filters</span></span>

<span data-ttu-id="852de-p105">フィルターは、細かく絞り込んだデータ セットを返したり、返されたデータをさまざまな方法で表示したりする方法として利用できます。たとえば、通話受付管理レポートでは、通話を開始したユーザーや呼び出し先のユーザーに基づいて通話をフィルターできます。また、データをグループ化する方法を選択することもできます。この場合は、時間、日、週、または月を基準に通話がグループ化されます。</span><span class="sxs-lookup"><span data-stu-id="852de-p105">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Call Admission Control Report enables you to filter calls by the user who initiated the call or by the user who was being called. You can also choose how data should be grouped. In this case, calls are grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="852de-126">次の表に、通話受付管理レポートで使用できるフィルターを示します。</span><span class="sxs-lookup"><span data-stu-id="852de-126">The following table lists the filters that you can use with the Call Admission Control Report.</span></span>

### <a name="call-admission-control-report-filters"></a><span data-ttu-id="852de-127">通話受付管理レポートのフィルター</span><span class="sxs-lookup"><span data-stu-id="852de-127">Call Admission Control Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="852de-128">名前</span><span class="sxs-lookup"><span data-stu-id="852de-128">Name</span></span></th>
<th><span data-ttu-id="852de-129">説明</span><span class="sxs-lookup"><span data-stu-id="852de-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="852de-130"><strong>開始</strong></span><span class="sxs-lookup"><span data-stu-id="852de-130"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="852de-p106">時間範囲の開始日と開始時刻。データを時間単位で表示するには、次のように開始日と開始時刻の両方を入力します。</span><span class="sxs-lookup"><span data-stu-id="852de-p106">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="852de-133">7/17/12012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="852de-133">7/17/12012 1:00 PM</span></span></p>
<p><span data-ttu-id="852de-p107">開始時刻を入力しないと、レポートは自動的に指定日の午前 12:00 に開始します。データを日単位で表示するには、次のように日付のみを入力します。</span><span class="sxs-lookup"><span data-stu-id="852de-p107">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="852de-136">7/17/12012</span><span class="sxs-lookup"><span data-stu-id="852de-136">7/17/12012</span></span></p>
<p><span data-ttu-id="852de-137">週単位または月単位で表示するには、表示する週または月の任意の日付を入力します (その週または月の最初の日である必要はありません)。</span><span class="sxs-lookup"><span data-stu-id="852de-137">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="852de-138">7/13/2012</span><span class="sxs-lookup"><span data-stu-id="852de-138">7/13/2012</span></span></p>
<p><span data-ttu-id="852de-139">一週間は、日曜日から始まり、土曜日で終わるものとします。</span><span class="sxs-lookup"><span data-stu-id="852de-139">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="852de-140"><strong>終了</strong></span><span class="sxs-lookup"><span data-stu-id="852de-140"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="852de-p108">時間範囲の終了日と終了時刻。データを時間単位で表示するには、次のように終了日と終了時刻の両方を入力します。</span><span class="sxs-lookup"><span data-stu-id="852de-p108">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="852de-143">7/17/12012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="852de-143">7/17/12012 1:00 PM</span></span></p>
<p><span data-ttu-id="852de-p109">終了時刻を入力しないと、レポートは自動的に指定日の午前 12:00 に終了します。データを日単位で表示するには、次のように日付のみを入力します。</span><span class="sxs-lookup"><span data-stu-id="852de-p109">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="852de-146">7/17/12012</span><span class="sxs-lookup"><span data-stu-id="852de-146">7/17/12012</span></span></p>
<p><span data-ttu-id="852de-147">週単位または月単位で表示するには、表示する週または月の任意の日付を入力します (その週または月の最初の日である必要はありません)。</span><span class="sxs-lookup"><span data-stu-id="852de-147">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="852de-148">7/13/2012</span><span class="sxs-lookup"><span data-stu-id="852de-148">7/13/2012</span></span></p>
<p><span data-ttu-id="852de-149">一週間は、日曜日から始まり、土曜日で終わるものとします。</span><span class="sxs-lookup"><span data-stu-id="852de-149">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="852de-150"><strong>プール</strong></span><span class="sxs-lookup"><span data-stu-id="852de-150"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="852de-p110">レジストラー プールまたはエッジ サーバーの完全修飾ドメイン名 (FQDN)。個別のプールを選択するか、[<strong>すべて</strong>] をクリックしてすべてのプールのデータを表示できます。このドロップダウン リストは、データベース内のレコードに基づいて自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="852de-p110">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server. You can either select an individual pool or click <strong>[All]</strong> to view data for all the pools. This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="852de-154"><strong>動作状況の種類</strong></span><span class="sxs-lookup"><span data-stu-id="852de-154"><strong>Activity type</strong></span></span></p></td>
<td><p><span data-ttu-id="852de-p111">活動の種類。次のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="852de-p111">Type of activity. Select one of the following activities:</span></span></p>
<ul>
<li><p><span data-ttu-id="852de-157">[すべて]</span><span class="sxs-lookup"><span data-stu-id="852de-157">[All]</span></span></p></li>
<li><p><span data-ttu-id="852de-158">ピアツーピア</span><span class="sxs-lookup"><span data-stu-id="852de-158">Peer-to-Peer</span></span></p></li>
<li><p><span data-ttu-id="852de-159">電話会議</span><span class="sxs-lookup"><span data-stu-id="852de-159">Conference</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="852de-160"><strong>通話のカテゴリ</strong></span><span class="sxs-lookup"><span data-stu-id="852de-160"><strong>Call category</strong></span></span></p></td>
<td><p><span data-ttu-id="852de-p112">通話に CAC が使用された理由を示します。次のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="852de-p112">Indicates the reason that CAC was used for the call. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="852de-163">[すべて]</span><span class="sxs-lookup"><span data-stu-id="852de-163">[All]</span></span></p></li>
<li><p><span data-ttu-id="852de-164">通話受付管理のため、拒否された通話</span><span class="sxs-lookup"><span data-stu-id="852de-164">Call rejected because of call admission control</span></span></p></li>
<li><p><span data-ttu-id="852de-165">通話受付管理のため、PSTN を通じて経路変更された通話</span><span class="sxs-lookup"><span data-stu-id="852de-165">Calls rerouted through PSTN because of call admission control</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-peer-to-peer-sessions"></a><span data-ttu-id="852de-166">ピアツーピア セッションの指標</span><span class="sxs-lookup"><span data-stu-id="852de-166">Metrics for Peer-to-Peer Sessions</span></span>

<span data-ttu-id="852de-167">次の表に、通話受付管理レポートでピアツーピア セッション (2 人の参加者のみが関与するセッション) について提供される情報を示します。</span><span class="sxs-lookup"><span data-stu-id="852de-167">The following table lists the information provided in the Call Admission Control Report for peer-to-peer sessions (that is, sessions involving just two participants).</span></span>

### <a name="metrics-for-peer-to-peer-sessions"></a><span data-ttu-id="852de-168">ピアツーピア セッションの指標</span><span class="sxs-lookup"><span data-stu-id="852de-168">Metrics for Peer-to-Peer Sessions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="852de-169">名前</span><span class="sxs-lookup"><span data-stu-id="852de-169">Name</span></span></th>
<th><span data-ttu-id="852de-170">この項目での並べ替え</span><span class="sxs-lookup"><span data-stu-id="852de-170">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="852de-171">説明</span><span class="sxs-lookup"><span data-stu-id="852de-171">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="852de-172"><strong>[詳細]</strong></span><span class="sxs-lookup"><span data-stu-id="852de-172"><strong>Detail</strong></span></span></p></td>
<td><p><span data-ttu-id="852de-173">不可</span><span class="sxs-lookup"><span data-stu-id="852de-173">No</span></span></p></td>
<td><p><span data-ttu-id="852de-174">この項目をクリックすると、指定したセッションのピアツーピア セッション詳細レポートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="852de-174">When you click this item, the report shows you a Peer-to-Peer Session Detail Report for the specified session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="852de-175"><strong>移動元ユーザー</strong></span><span class="sxs-lookup"><span data-stu-id="852de-175"><strong>From user</strong></span></span></p></td>
<td><p><span data-ttu-id="852de-176">可</span><span class="sxs-lookup"><span data-stu-id="852de-176">Yes</span></span></p></td>
<td><p><span data-ttu-id="852de-177">セッションを開始したユーザーの SIP アドレス。</span><span class="sxs-lookup"><span data-stu-id="852de-177">SIP address of the user who initiated the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="852de-178"><strong>対象ユーザー</strong></span><span class="sxs-lookup"><span data-stu-id="852de-178"><strong>To user</strong></span></span></p></td>
<td><p><span data-ttu-id="852de-179">可</span><span class="sxs-lookup"><span data-stu-id="852de-179">Yes</span></span></p></td>
<td><p><span data-ttu-id="852de-180">セッションへの参加を招待されたユーザーの SIP アドレス。</span><span class="sxs-lookup"><span data-stu-id="852de-180">SIP address of the user who was invited to join the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="852de-181"><strong>モダリティ</strong></span><span class="sxs-lookup"><span data-stu-id="852de-181"><strong>Modalities</strong></span></span></p></td>
<td><p><span data-ttu-id="852de-182">可</span><span class="sxs-lookup"><span data-stu-id="852de-182">Yes</span></span></p></td>
<td><p><span data-ttu-id="852de-183">セッションで使用された通信モダリティ (音声、ビデオなど)。</span><span class="sxs-lookup"><span data-stu-id="852de-183">Communication modalities (such as audio and video) that were used during the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="852de-184"><strong>招待時間</strong></span><span class="sxs-lookup"><span data-stu-id="852de-184"><strong>Invite time</strong></span></span></p></td>
<td><p><span data-ttu-id="852de-185">可</span><span class="sxs-lookup"><span data-stu-id="852de-185">Yes</span></span></p></td>
<td><p><span data-ttu-id="852de-186">セッションへの最初の招待が発信元ユーザーから送信された日時。</span><span class="sxs-lookup"><span data-stu-id="852de-186">Date and time the initial session invitation was sent to the From user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="852de-187"><strong>応答時間</strong></span><span class="sxs-lookup"><span data-stu-id="852de-187"><strong>Response time</strong></span></span></p></td>
<td><p><span data-ttu-id="852de-188">可</span><span class="sxs-lookup"><span data-stu-id="852de-188">Yes</span></span></p></td>
<td><p><span data-ttu-id="852de-189">招待の承諾を受信した日時。</span><span class="sxs-lookup"><span data-stu-id="852de-189">Date and time that the invitation acceptance was received.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="852de-190"><strong>終了時刻</strong></span><span class="sxs-lookup"><span data-stu-id="852de-190"><strong>End time</strong></span></span></p></td>
<td><p><span data-ttu-id="852de-191">可</span><span class="sxs-lookup"><span data-stu-id="852de-191">Yes</span></span></p></td>
<td><p><span data-ttu-id="852de-192">セッションが終了した日時。</span><span class="sxs-lookup"><span data-stu-id="852de-192">Date and time that the session ended.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="852de-193"><strong>診断 ID</strong></span><span class="sxs-lookup"><span data-stu-id="852de-193"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="852de-194">可</span><span class="sxs-lookup"><span data-stu-id="852de-194">Yes</span></span></p></td>
<td><p><span data-ttu-id="852de-p113">SIP メッセージに添付される一意の識別子 (ms-diagnostics ヘッダー形式)。その情報は、多くの場合、エラーのトラブルシューティングに役立ちます。診断ヘッダーはオプションで (このヘッダーを含まない SIP セッションがある可能性もあります)、診断 ID は、何らかの問題が生じたセッションについてのみ報告されます。</span><span class="sxs-lookup"><span data-stu-id="852de-p113">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors. Diagnostics headers are optional (it is possible to have SIP sessions that do not include these headers), and diagnostic IDs are reported only for sessions that experienced problems of some kind.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-conferencing-sessions"></a><span data-ttu-id="852de-197">電話会議セッションの指標</span><span class="sxs-lookup"><span data-stu-id="852de-197">Metrics for Conferencing Sessions</span></span>

<span data-ttu-id="852de-198">次の表に、通話受付管理レポートで電話会議セッション (3 人以上の参加者が関与するセッション) について提供される情報を示します。</span><span class="sxs-lookup"><span data-stu-id="852de-198">The following table lists the information provided in the Call Admission Control Report for conferencing sessions (that is, sessions involving three or more participants).</span></span>

### <a name="metrics-for-conferencing-sessions"></a><span data-ttu-id="852de-199">電話会議セッションの指標</span><span class="sxs-lookup"><span data-stu-id="852de-199">Metrics for Conferencing Sessions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="852de-200">名前</span><span class="sxs-lookup"><span data-stu-id="852de-200">Name</span></span></th>
<th><span data-ttu-id="852de-201">この項目での並べ替え</span><span class="sxs-lookup"><span data-stu-id="852de-201">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="852de-202">説明</span><span class="sxs-lookup"><span data-stu-id="852de-202">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="852de-203"><strong>[会議 URI]</strong></span><span class="sxs-lookup"><span data-stu-id="852de-203"><strong>Conference URI</strong></span></span></p></td>
<td><p><span data-ttu-id="852de-204">可</span><span class="sxs-lookup"><span data-stu-id="852de-204">Yes</span></span></p></td>
<td><p><span data-ttu-id="852de-p114">電話会議の一意の識別子。この項目をクリックすると、個別の電話会議参加者が表示されます。</span><span class="sxs-lookup"><span data-stu-id="852de-p114">Unique identifier for the conference. When you click this item, the report shows the individual conference participants.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="852de-207"><strong>開催者</strong></span><span class="sxs-lookup"><span data-stu-id="852de-207"><strong>Organizer</strong></span></span></p></td>
<td><p><span data-ttu-id="852de-208">可</span><span class="sxs-lookup"><span data-stu-id="852de-208">Yes</span></span></p></td>
<td><p><span data-ttu-id="852de-209">会議を開催したユーザーの SIP アドレス。</span><span class="sxs-lookup"><span data-stu-id="852de-209">SIP address of the user who organized the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="852de-210"><strong>プール</strong></span><span class="sxs-lookup"><span data-stu-id="852de-210"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="852de-211">可</span><span class="sxs-lookup"><span data-stu-id="852de-211">Yes</span></span></p></td>
<td><p><span data-ttu-id="852de-212">電話会議で使用されたエッジ サーバー。</span><span class="sxs-lookup"><span data-stu-id="852de-212">Edge Server used in the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="852de-213"><strong>開始時刻</strong></span><span class="sxs-lookup"><span data-stu-id="852de-213"><strong>Start time</strong></span></span></p></td>
<td><p><span data-ttu-id="852de-214">可</span><span class="sxs-lookup"><span data-stu-id="852de-214">Yes</span></span></p></td>
<td><p><span data-ttu-id="852de-215">会議が開始した日時。</span><span class="sxs-lookup"><span data-stu-id="852de-215">Date and time that the conference started.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="852de-216"><strong>終了時刻</strong></span><span class="sxs-lookup"><span data-stu-id="852de-216"><strong>End time</strong></span></span></p></td>
<td><p><span data-ttu-id="852de-217">可</span><span class="sxs-lookup"><span data-stu-id="852de-217">Yes</span></span></p></td>
<td><p><span data-ttu-id="852de-218">会議が終了した日時。</span><span class="sxs-lookup"><span data-stu-id="852de-218">Date and time that the conference ended.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-individual-conference-participants"></a><span data-ttu-id="852de-219">個別の電話会議参加者の指標</span><span class="sxs-lookup"><span data-stu-id="852de-219">Metrics for Individual Conference Participants</span></span>

<span data-ttu-id="852de-220">次の表に、通話受付管理レポートで個別の電話会議参加者について提供される情報を示します。</span><span class="sxs-lookup"><span data-stu-id="852de-220">The following table lists the information provided in the Call Admission Control Report for individual conference participants.</span></span>

### <a name="metrics-for-individual-conference-participants"></a><span data-ttu-id="852de-221">個別の電話会議参加者の指標</span><span class="sxs-lookup"><span data-stu-id="852de-221">Metrics for Individual Conference Participants</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="852de-222">名前</span><span class="sxs-lookup"><span data-stu-id="852de-222">Name</span></span></th>
<th><span data-ttu-id="852de-223">この項目での並べ替え</span><span class="sxs-lookup"><span data-stu-id="852de-223">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="852de-224">説明</span><span class="sxs-lookup"><span data-stu-id="852de-224">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="852de-225"><strong>役割</strong></span><span class="sxs-lookup"><span data-stu-id="852de-225"><strong>Role</strong></span></span></p></td>
<td><p><span data-ttu-id="852de-226">不可</span><span class="sxs-lookup"><span data-stu-id="852de-226">No</span></span></p></td>
<td><p><span data-ttu-id="852de-227">電話会議の参加者が担った役割 (発表者など)。</span><span class="sxs-lookup"><span data-stu-id="852de-227">Role (for example, Presenter) played by the conference participant.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="852de-228"><strong>参加者</strong></span><span class="sxs-lookup"><span data-stu-id="852de-228"><strong>Participant</strong></span></span></p></td>
<td><p><span data-ttu-id="852de-229">不可</span><span class="sxs-lookup"><span data-stu-id="852de-229">No</span></span></p></td>
<td><p><span data-ttu-id="852de-230">電話会議の参加者の SIP アドレス。</span><span class="sxs-lookup"><span data-stu-id="852de-230">SIP address of the conference participant.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="852de-231"><strong>接続</strong></span><span class="sxs-lookup"><span data-stu-id="852de-231"><strong>Connectivity</strong></span></span></p></td>
<td><p><span data-ttu-id="852de-232">不可</span><span class="sxs-lookup"><span data-stu-id="852de-232">No</span></span></p></td>
<td><p><span data-ttu-id="852de-233">参加者のネットワーク接続 (一般には内部送信元または外部送信元)。</span><span class="sxs-lookup"><span data-stu-id="852de-233">Network connectivity (typically From Internal or From External) for the participant.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="852de-234"><strong>モダリティ</strong></span><span class="sxs-lookup"><span data-stu-id="852de-234"><strong>Modality</strong></span></span></p></td>
<td><p><span data-ttu-id="852de-235">不可</span><span class="sxs-lookup"><span data-stu-id="852de-235">No</span></span></p></td>
<td><p><span data-ttu-id="852de-236">電話会議の種類 (音声ビデオ会議など)。</span><span class="sxs-lookup"><span data-stu-id="852de-236">Conference type (for example, A/V conferencing).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="852de-237"><strong>参加時間</strong></span><span class="sxs-lookup"><span data-stu-id="852de-237"><strong>Join time</strong></span></span></p></td>
<td><p><span data-ttu-id="852de-238">不可</span><span class="sxs-lookup"><span data-stu-id="852de-238">No</span></span></p></td>
<td><p><span data-ttu-id="852de-239">参加者が電話会議に参加した日時。</span><span class="sxs-lookup"><span data-stu-id="852de-239">Date and time that the participant joined the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="852de-240"><strong>[退場時間]</strong></span><span class="sxs-lookup"><span data-stu-id="852de-240"><strong>Leave time</strong></span></span></p></td>
<td><p><span data-ttu-id="852de-241">不可</span><span class="sxs-lookup"><span data-stu-id="852de-241">No</span></span></p></td>
<td><p><span data-ttu-id="852de-242">参加者が電話会議から退出した日時。</span><span class="sxs-lookup"><span data-stu-id="852de-242">Date and time that the participant left the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="852de-243"><strong>診断 ID</strong></span><span class="sxs-lookup"><span data-stu-id="852de-243"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="852de-244">不可</span><span class="sxs-lookup"><span data-stu-id="852de-244">No</span></span></p></td>
<td><p><span data-ttu-id="852de-p115">SIP メッセージに添付される一意の識別子 (ms-diagnostics ヘッダー形式)。その情報は、多くの場合、エラーのトラブルシューティングに役立ちます。診断ヘッダーはオプションで (このヘッダーを含まない SIP セッションがある可能性もあります)、診断 ID は、何らかの問題が生じたセッションについてのみ報告されます。</span><span class="sxs-lookup"><span data-stu-id="852de-p115">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors. Diagnostics headers are optional (it is possible to have SIP sessions that do not include these headers), and diagnostic IDs are reported only for sessions that experienced problems of some kind.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="852de-247">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="852de-247">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

