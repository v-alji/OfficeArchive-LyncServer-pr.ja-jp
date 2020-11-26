---
title: 'Lync Server 2013: 失敗の配布レポート'
description: 'Lync Server 2013: 失敗した配布レポート。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failure Distribution Report
ms:assetid: 365c7beb-24d4-40f5-92e7-4978b9688916
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558635(v=OCS.15)
ms:contentKeyID: 48183849
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f5a87f779f87d6b7002fa108f1969c33739eed9b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428217"
---
# <a name="failure-distribution-report-in-lync-server-2013"></a><span data-ttu-id="4b8a4-103">Lync Server 2013 でのエラー配布レポート</span><span class="sxs-lookup"><span data-stu-id="4b8a4-103">Failure Distribution Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4b8a4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4b8a4-104">

<span> </span></span></span>

<span data-ttu-id="4b8a4-105">_**最終更新日:** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="4b8a4-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="4b8a4-106">エラー分布レポートは、問題の発生したセッションを以下のカテゴリに分類します。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-106">The Failure Distribution Report ranks failed sessions in the following categories:</span></span>

  - <span data-ttu-id="4b8a4-107">トップの診断理由</span><span class="sxs-lookup"><span data-stu-id="4b8a4-107">Top diagnostic reasons</span></span>

  - <span data-ttu-id="4b8a4-108">トップのモダリティ</span><span class="sxs-lookup"><span data-stu-id="4b8a4-108">Top modalities</span></span>

  - <span data-ttu-id="4b8a4-109">トップのプール</span><span class="sxs-lookup"><span data-stu-id="4b8a4-109">Top pools</span></span>

  - <span data-ttu-id="4b8a4-110">トップのソース</span><span class="sxs-lookup"><span data-stu-id="4b8a4-110">Top sources</span></span>

  - <span data-ttu-id="4b8a4-111">トップのコンポーネント</span><span class="sxs-lookup"><span data-stu-id="4b8a4-111">Top components</span></span>

  - <span data-ttu-id="4b8a4-112">トップの発信元ユーザー</span><span class="sxs-lookup"><span data-stu-id="4b8a4-112">Top from users</span></span>

  - <span data-ttu-id="4b8a4-113">トップの発信先ユーザー</span><span class="sxs-lookup"><span data-stu-id="4b8a4-113">Top to users</span></span>

  - <span data-ttu-id="4b8a4-114">送信元ユーザー エージェント</span><span class="sxs-lookup"><span data-stu-id="4b8a4-114">Top from user agents</span></span>

<span data-ttu-id="4b8a4-p101">これらのカテゴリを使用して、どこに問題が発生しているか、場合によっては、問題が発生している理由を正確に確認できます。たとえば特定の日に、242 個のオーディオ/ビデオ セッションの障害が記録されたとします。エラー分布レポートを調べてみると、これらの問題の発生したセッションのうち、237 個が Dublin プールで発生しているかもしれません。これらの問題の背後にある原因を調べて診断するには、このような情報が役に立ちます。[**トップのプール**] カテゴリの下の Dublin プールをクリックすると、そのプールのエラー分布レポートのみが表示されます。次に Dublin プールでこれほど多くの問題が発生している理由の分析を開始できます。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-p101">You can use these categories to determine exactly where a problem is occurring and, in some cases, why the problem is occurring. For example, suppose you recorded 242 failed audio/video sessions during a given day. If you look at the Failure Distribution Report, it might show that 237 of those failed sessions took place in your Dublin pool. That gives you a good place to start when it comes to tracking down and diagnosing the causes behind those failures. If you click on the Dublin pool under the **Top pools** category, you will see a Failure Distribution Report just for that pool. You can then begin analyzing why the Dublin pool was experiencing so many difficulties.</span></span>

<div>

## <a name="viewing-the-failure-distribution-report"></a><span data-ttu-id="4b8a4-121">エラー分布レポートを表示する</span><span class="sxs-lookup"><span data-stu-id="4b8a4-121">Viewing the Failure Distribution Report</span></span>

<span data-ttu-id="4b8a4-122">以下の任意のレポートで、[**予期されるエラー ボリューム**] または [**予期しないエラー ボリューム**] の指標をクリックすると、エラー分布レポートにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-122">You can access the Failure Distribution Report from any of the following reports by clicking either the **Expected failure volume** or the **Unexpected failure volume** metric:</span></span>

  - [<span data-ttu-id="4b8a4-123">Lync Server 2013 の上位エラーレポート</span><span class="sxs-lookup"><span data-stu-id="4b8a4-123">Top Failures Report in Lync Server 2013</span></span>](lync-server-2013-top-failures-report.md)

  - [<span data-ttu-id="4b8a4-124">Lync Server 2013 での会議の診断レポート</span><span class="sxs-lookup"><span data-stu-id="4b8a4-124">Conference Diagnostic Report in Lync Server 2013</span></span>](lync-server-2013-conference-diagnostic-report.md)

  - [<span data-ttu-id="4b8a4-125">Lync Server 2013 のピアツーピアアクティビティ診断レポート</span><span class="sxs-lookup"><span data-stu-id="4b8a4-125">Peer-to-Peer Activity Diagnostic Report in Lync Server 2013</span></span>](lync-server-2013-peer-to-peer-activity-diagnostic-report.md)

<span data-ttu-id="4b8a4-126">エラー配布レポートでは、次のいずれかの指標をクリックして、 [Lync Server 2013 でエラー一覧レポート](lync-server-2013-failure-list-report.md)を表示できます。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-126">From the Failure Distribution Report, you can click any of the following metrics to view the [Failure List Report in Lync Server 2013](lync-server-2013-failure-list-report.md):</span></span>

  - <span data-ttu-id="4b8a4-127">トップの診断理由 (セッション)</span><span class="sxs-lookup"><span data-stu-id="4b8a4-127">Top diagnostic reasons (sessions)</span></span>

  - <span data-ttu-id="4b8a4-128">トップのモダリティ (セッション)</span><span class="sxs-lookup"><span data-stu-id="4b8a4-128">Top modalities (sessions)</span></span>

  - <span data-ttu-id="4b8a4-129">トップのプール (セッション)</span><span class="sxs-lookup"><span data-stu-id="4b8a4-129">Top pools (sessions)</span></span>

  - <span data-ttu-id="4b8a4-130">トップのソース (セッション)</span><span class="sxs-lookup"><span data-stu-id="4b8a4-130">Top sources (sessions)</span></span>

  - <span data-ttu-id="4b8a4-131">トップのコンポーネント (セッション)</span><span class="sxs-lookup"><span data-stu-id="4b8a4-131">Top components (sessions)</span></span>

  - <span data-ttu-id="4b8a4-132">トップの発信元ユーザー (セッション)</span><span class="sxs-lookup"><span data-stu-id="4b8a4-132">Top from users (sessions)</span></span>

  - <span data-ttu-id="4b8a4-133">トップの発信先ユーザー (セッション)</span><span class="sxs-lookup"><span data-stu-id="4b8a4-133">Top to users (sessions)</span></span>

  - <span data-ttu-id="4b8a4-134">トップの発信元ユーザー エージェント (セッション)</span><span class="sxs-lookup"><span data-stu-id="4b8a4-134">Top from user agents (sessions)</span></span>

</div>

<div>

## <a name="using-the-failure-distribution-report"></a><span data-ttu-id="4b8a4-135">エラー分布レポートを使用する</span><span class="sxs-lookup"><span data-stu-id="4b8a4-135">Using the Failure Distribution Report</span></span>

<span data-ttu-id="4b8a4-p102">モニターの大きさと画面解像度によっては、エラー分布レポートを画面上で表示するとき、表示されるデータの一部が切り捨てられることがあります。これは特に、ユーザー エージェントのような非常に長いラベルを持つことがある指標で発生します。たとえば、"UCCAPI/4.0.7400.0 OC/4.0.7400.0 (Microsoft Lync 2013) " のような名前のユーザー エージェントは、以下のように一部分のみが画面上に表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-p102">Depending on your monitor size and screen resolution, it's possible that some of the data shown in the Failure Distribution Report might be truncated when you view it onscreen. This is especially true for metrics such as user agents, which can have very long labels. For example, a user agent with a name like "UCCAPI/4.0.7400.0 OC/4.0.7400.0 (Microsoft Lync 2013)" might only partially appear onscreen:</span></span>

<span data-ttu-id="4b8a4-139">UCCAPI/4.0.7400.0 OC/4.0.7400.0 (Microsoft Ly...</span><span class="sxs-lookup"><span data-stu-id="4b8a4-139">UCCAPI/4.0.7400.0 OC/4.0.7400.0 (Microsoft Ly...</span></span>

<span data-ttu-id="4b8a4-140">この場合、切り捨てられた値の上にマウス ポインターを置くだけでラベル全体を表示できます。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-140">Fortunately, you can see the entire label simply by holding your mouse over the truncated value.</span></span>

<span data-ttu-id="4b8a4-p103">エラー分布レポートを使用してフィルター処理できる、役立つ指標の 1 つが診断 ID です。さまざまなレポートで同じ診断 ID が表示される場合、エラー分布レポートでその ID をフィルター処理して、問題の発生したセッション中に、その ID が報告された正確な場所と頻度について非常に詳細な情報を得られます。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-p103">One interesting metric that you can filter on by using the Failure Distribution Report is Diagnostic ID. If you see the same Diagnostic ID cropping up in other reports you can filter on that ID in the Failure Distribution Report and get a very detailed look at exactly where, and how often, that ID has been reported during a failed session.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="4b8a4-143">フィルター</span><span class="sxs-lookup"><span data-stu-id="4b8a4-143">Filters</span></span>

<span data-ttu-id="4b8a4-p104">フィルターは、必要なデータのみに絞り込んだデータ セットを取得したり、取得したデータを別の方法で表示したりする方法として利用できます。たとえば、エラー分布レポートを使用すると、動作状況の種類 (ピアツーピア セッションまたは電話会議セッション) などにフィルターを適用できます。また、失敗した各セッションに添付される診断 ID によってフィルターを適用することもできます。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-p104">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Failed Distribution Report enables you to filter on such things as the activity type (peer-to-peer session or conferencing session) or by the diagnostic ID that accompanied each failed session.</span></span>

<span data-ttu-id="4b8a4-146">次の表に、エラー分布レポートで使用できるフィルターを示します。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-146">The following table lists the filters that you can use with the Failure Distribution Report.</span></span>

### <a name="failure-distribution-report-filters"></a><span data-ttu-id="4b8a4-147">エラー分布レポートのフィルター</span><span class="sxs-lookup"><span data-stu-id="4b8a4-147">Failure Distribution Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4b8a4-148">名前</span><span class="sxs-lookup"><span data-stu-id="4b8a4-148">Name</span></span></th>
<th><span data-ttu-id="4b8a4-149">説明</span><span class="sxs-lookup"><span data-stu-id="4b8a4-149">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b8a4-150"><strong>開始</strong></span><span class="sxs-lookup"><span data-stu-id="4b8a4-150"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="4b8a4-p105">時間範囲の開始日と開始時刻。データを時間単位で表示するには、次のように開始日と開始時刻の両方を入力します。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-p105">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="4b8a4-153">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="4b8a4-153">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="4b8a4-p106">開始時刻を入力しないと、レポートは自動的に指定日の午前 12:00 に開始します。データを日単位で表示するには、次のように日付のみを入力します。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-p106">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="4b8a4-156">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="4b8a4-156">7/7/2012</span></span></p>
<p><span data-ttu-id="4b8a4-157">週単位または月単位で表示するには、表示する週または月の任意の日付を入力します (その週または月の最初の日である必要はありません)。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-157">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="4b8a4-158">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="4b8a4-158">7/3/2012</span></span></p>
<p><span data-ttu-id="4b8a4-159">一週間は、日曜日から始まり、土曜日で終わるものとします。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-159">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b8a4-160"><strong>終了</strong></span><span class="sxs-lookup"><span data-stu-id="4b8a4-160"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="4b8a4-p107">時間範囲の終了日と終了時刻。データを時間単位で表示するには、次のように終了日と終了時刻の両方を入力します。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-p107">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="4b8a4-163">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="4b8a4-163">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="4b8a4-p108">終了時刻を入力しないと、レポートは自動的に指定日の午前 12:00 に終了します。データを日単位で表示するには、次のように日付のみを入力します。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-p108">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="4b8a4-166">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="4b8a4-166">7/7/2012</span></span></p>
<p><span data-ttu-id="4b8a4-167">週単位または月単位で表示するには、表示する週または月の任意の日付を入力します (その週または月の最初の日である必要はありません)。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-167">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="4b8a4-168">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="4b8a4-168">7/3/2012</span></span></p>
<p><span data-ttu-id="4b8a4-169">一週間は、日曜日から始まり、土曜日で終わるものとします。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-169">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b8a4-170"><strong>プール</strong></span><span class="sxs-lookup"><span data-stu-id="4b8a4-170"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="4b8a4-p109">レジストラー プールまたはエッジ サーバーの完全修飾ドメイン名 (FQDN)。個別のプールを選択するか、[<strong>すべて</strong>] をクリックしてすべてのプールのデータを表示できます。このドロップダウン リストは、データベース内のレコードに基づいて自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-p109">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server. You can either select an individual pool or click <strong>[All]</strong> to view data for all the pools. This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b8a4-174"><strong>[動作状況の種類]</strong></span><span class="sxs-lookup"><span data-stu-id="4b8a4-174"><strong>Activity type</strong></span></span></p></td>
<td><p><span data-ttu-id="4b8a4-p110">フィルターを適用する動作状況の種類。次のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-p110">Type of activity to filter on. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="4b8a4-177">[すべて]</span><span class="sxs-lookup"><span data-stu-id="4b8a4-177">[All]</span></span></p></li>
<li><p><span data-ttu-id="4b8a4-178">ピアツーピア</span><span class="sxs-lookup"><span data-stu-id="4b8a4-178">Peer-to-peer</span></span></p></li>
<li><p><span data-ttu-id="4b8a4-179">電話会議</span><span class="sxs-lookup"><span data-stu-id="4b8a4-179">Conference</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b8a4-180"><strong>[セッション カテゴリ]</strong></span><span class="sxs-lookup"><span data-stu-id="4b8a4-180"><strong>Session category</strong></span></span></p></td>
<td><p><span data-ttu-id="4b8a4-p111">問題のアクティビティが成功したか失敗したかを示します。次のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-p111">Indicates whether the activity in question succeeded or failed. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="4b8a4-183">[すべて]</span><span class="sxs-lookup"><span data-stu-id="4b8a4-183">[All]</span></span></p></li>
<li><p><span data-ttu-id="4b8a4-184">成功</span><span class="sxs-lookup"><span data-stu-id="4b8a4-184">Success</span></span></p></li>
<li><p><span data-ttu-id="4b8a4-185">予期されたエラー</span><span class="sxs-lookup"><span data-stu-id="4b8a4-185">Expected failure</span></span></p></li>
<li><p><span data-ttu-id="4b8a4-186">予期しないエラー</span><span class="sxs-lookup"><span data-stu-id="4b8a4-186">Unexpected failure</span></span></p></li>
</ul>
<p><span data-ttu-id="4b8a4-187">&quot;予期されるエラー &quot; は、発生する可能性のあるエラーです。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-187">An &quot;expected failure&quot; is a failure that is expected to happen.</span></span> <span data-ttu-id="4b8a4-188">たとえば、ユーザーが応答不可のステータスを設定した場合、そのユーザーへの呼び出しはエラーとなることが予期されます。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-188">For example, if a user has set his or her status to Do Not Disturb you would expect any call to that user to fail.</span></span> <span data-ttu-id="4b8a4-189">&quot;予期しないエラーと &quot; は、正常に動作していると思われるエラーです。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-189">An &quot;unexpected failure&quot; is a failure that occurs in what would appear to be an otherwise healthy system.</span></span> <span data-ttu-id="4b8a4-190">たとえば、発信者が保留にされたときに、通話が終了してはなりません。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-190">For example, a call should not be terminated if the caller is placed on hold.</span></span> <span data-ttu-id="4b8a4-191">そのような状態が発生する場合は、予期しないエラーとしてフラグが設定されます。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-191">If that occurs, that would be flagged as an unexpected failure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b8a4-192"><strong>[診断 ID]</strong></span><span class="sxs-lookup"><span data-stu-id="4b8a4-192"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="4b8a4-p113">SIP メッセージに添付される一意の識別子 (ms-diagnostics ヘッダー形式)。その情報は、多くの場合、エラーのトラブルシューティングに役立ちます。診断ヘッダーはオプションで (このヘッダーを含まない SIP セッションがある可能性もあります)、診断 ID は、何らかの問題が発生したセッションについてのみ報告されます。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-p113">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors. Diagnostics headers are optional (it is possible to have SIP sessions that do not include these headers), and diagnostic IDs are reported only for sessions that experienced problems of some kind.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-diagnostic-reasons"></a><span data-ttu-id="4b8a4-195">トップの診断理由の指標</span><span class="sxs-lookup"><span data-stu-id="4b8a4-195">Metrics for Top Diagnostic Reasons</span></span>

<span data-ttu-id="4b8a4-196">次の表に、最も報告される頻度が高い診断 ID に基づいて、エラー分布レポートで提供される情報を示します。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-196">The following table lists the information provided in the Failure Distribution Report based on the most frequently reported diagnostic ID.</span></span>

### <a name="metrics-for-top-diagnostic-reasons"></a><span data-ttu-id="4b8a4-197">トップの診断理由の指標</span><span class="sxs-lookup"><span data-stu-id="4b8a4-197">Metrics for Top Diagnostic Reasons</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4b8a4-198">名前</span><span class="sxs-lookup"><span data-stu-id="4b8a4-198">Name</span></span></th>
<th><span data-ttu-id="4b8a4-199">この項目での並べ替え</span><span class="sxs-lookup"><span data-stu-id="4b8a4-199">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="4b8a4-200">説明</span><span class="sxs-lookup"><span data-stu-id="4b8a4-200">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b8a4-201"><strong>[ランク]</strong></span><span class="sxs-lookup"><span data-stu-id="4b8a4-201"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="4b8a4-202">不可</span><span class="sxs-lookup"><span data-stu-id="4b8a4-202">No</span></span></p></td>
<td><p><span data-ttu-id="4b8a4-p114">診断 ID に基づく、失敗したセッションの相対的なランク付け。診断 ID は、エラーのトラブルシューティングに役立つ情報の得られることが多い、SIP メッセージに添付された一意の識別子です (ms-diagnostics ヘッダーの形式)。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-p114">Relative ranking of failed sessions based on diagnostic IDs. The diagnostic ID is a unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b8a4-205"><strong>[トップの診断理由]</strong></span><span class="sxs-lookup"><span data-stu-id="4b8a4-205"><strong>Top diagnostic reasons</strong></span></span></p></td>
<td><p><span data-ttu-id="4b8a4-206">不可</span><span class="sxs-lookup"><span data-stu-id="4b8a4-206">No</span></span></p></td>
<td><p><span data-ttu-id="4b8a4-207">セッションで生成される診断 ID。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-207">Diagnostic ID generated in a session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b8a4-208"><strong>[セッション]</strong></span><span class="sxs-lookup"><span data-stu-id="4b8a4-208"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="4b8a4-209">不可</span><span class="sxs-lookup"><span data-stu-id="4b8a4-209">No</span></span></p></td>
<td><p><span data-ttu-id="4b8a4-210">指定された診断 ID が生成された、失敗したセッションの総数。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-210">Total number of failed sessions where the specified diagnostic ID was generated.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-modalities"></a><span data-ttu-id="4b8a4-211">トップのモダリティの指標</span><span class="sxs-lookup"><span data-stu-id="4b8a4-211">Metrics for Top Modalities</span></span>

<span data-ttu-id="4b8a4-212">次の表に、最もエラーが発生したセッション モダリティに基づいて、エラー分布レポートで提供される情報を示します。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-212">The following table lists the information provided in the Failure Distribution Report based on the session modalities that experienced the most failures.</span></span>

### <a name="metrics-for-top-modalities"></a><span data-ttu-id="4b8a4-213">トップのモダリティの指標</span><span class="sxs-lookup"><span data-stu-id="4b8a4-213">Metrics for Top Modalities</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4b8a4-214">名前</span><span class="sxs-lookup"><span data-stu-id="4b8a4-214">Name</span></span></th>
<th><span data-ttu-id="4b8a4-215">この項目での並べ替え</span><span class="sxs-lookup"><span data-stu-id="4b8a4-215">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="4b8a4-216">説明</span><span class="sxs-lookup"><span data-stu-id="4b8a4-216">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b8a4-217"><strong>[ランク]</strong></span><span class="sxs-lookup"><span data-stu-id="4b8a4-217"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="4b8a4-218">不可</span><span class="sxs-lookup"><span data-stu-id="4b8a4-218">No</span></span></p></td>
<td><p><span data-ttu-id="4b8a4-219">セッションの種類 (たとえば、音声ビデオ会議、ピアツーピアのファイル送信セッション) に基づく、失敗したセッションの相対的なランク付け。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-219">Relative ranking based of failed session based on session type (for example, an audio/video conference or a peer-to-peer file transfer session).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b8a4-220"><strong>[トップのモダリティ]</strong></span><span class="sxs-lookup"><span data-stu-id="4b8a4-220"><strong>Top modalities</strong></span></span></p></td>
<td><p><span data-ttu-id="4b8a4-221">不可</span><span class="sxs-lookup"><span data-stu-id="4b8a4-221">No</span></span></p></td>
<td><p><span data-ttu-id="4b8a4-222">セッションの種類。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-222">Session type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b8a4-223"><strong>[セッション]</strong></span><span class="sxs-lookup"><span data-stu-id="4b8a4-223"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="4b8a4-224">不可</span><span class="sxs-lookup"><span data-stu-id="4b8a4-224">No</span></span></p></td>
<td><p><span data-ttu-id="4b8a4-225">指定されたモダリティが含まれる失敗したセッションの総数。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-225">Total number of failed sessions involving the specified modality.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-pools"></a><span data-ttu-id="4b8a4-226">トップのプールの指標</span><span class="sxs-lookup"><span data-stu-id="4b8a4-226">Metrics for Top Pools</span></span>

<span data-ttu-id="4b8a4-227">次の表に、最もエラーが発生したプールに基づいて、エラー分布レポートで提供される情報を示します。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-227">The following table lists the information provided in the Failure Distribution Report based on the pools that experienced the most failures.</span></span>

### <a name="metrics-for-top-pools"></a><span data-ttu-id="4b8a4-228">トップのプールの指標</span><span class="sxs-lookup"><span data-stu-id="4b8a4-228">Metrics for Top Pools</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4b8a4-229">名前</span><span class="sxs-lookup"><span data-stu-id="4b8a4-229">Name</span></span></th>
<th><span data-ttu-id="4b8a4-230">この項目での並べ替え</span><span class="sxs-lookup"><span data-stu-id="4b8a4-230">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="4b8a4-231">説明</span><span class="sxs-lookup"><span data-stu-id="4b8a4-231">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b8a4-232"><strong>[ランク]</strong></span><span class="sxs-lookup"><span data-stu-id="4b8a4-232"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="4b8a4-233">不可</span><span class="sxs-lookup"><span data-stu-id="4b8a4-233">No</span></span></p></td>
<td><p><span data-ttu-id="4b8a4-234">セッションが実行されたレジストラープールまたはエッジサーバーに基づいて、失敗したセッションの相対的なランクを指定します。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-234">Relative ranking of failed sessions based on the Registrar pool or Edge Server where the session was conducted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b8a4-235"><strong>[トップのプール]</strong></span><span class="sxs-lookup"><span data-stu-id="4b8a4-235"><strong>Top pools</strong></span></span></p></td>
<td><p><span data-ttu-id="4b8a4-236">不可</span><span class="sxs-lookup"><span data-stu-id="4b8a4-236">No</span></span></p></td>
<td><p><span data-ttu-id="4b8a4-237">レジストラープールまたはエッジサーバーの名前。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-237">Name of the Registrar pool or Edge Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b8a4-238"><strong>[セッション]</strong></span><span class="sxs-lookup"><span data-stu-id="4b8a4-238"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="4b8a4-239">不可</span><span class="sxs-lookup"><span data-stu-id="4b8a4-239">No</span></span></p></td>
<td><p><span data-ttu-id="4b8a4-240">登録プールまたはエッジサーバーあたりの失敗したセッションの合計数です。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-240">Total number of failed sessions per Registrar pool or Edge Server.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-sources"></a><span data-ttu-id="4b8a4-241">トップのソースの指標</span><span class="sxs-lookup"><span data-stu-id="4b8a4-241">Metrics for Top Sources</span></span>

<span data-ttu-id="4b8a4-242">次の表に、最もエラーが発生したコンピューターに基づいて、エラー分布レポートで提供される情報を示します。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-242">The following table lists the information provided in the Failure Distribution Report based on the computers that experienced the most failures.</span></span>

### <a name="metrics-for-top-sources"></a><span data-ttu-id="4b8a4-243">トップのソースの指標</span><span class="sxs-lookup"><span data-stu-id="4b8a4-243">Metrics for Top Sources</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4b8a4-244">名前</span><span class="sxs-lookup"><span data-stu-id="4b8a4-244">Name</span></span></th>
<th><span data-ttu-id="4b8a4-245">この項目での並べ替え</span><span class="sxs-lookup"><span data-stu-id="4b8a4-245">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="4b8a4-246">説明</span><span class="sxs-lookup"><span data-stu-id="4b8a4-246">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b8a4-247"><strong>[ランク]</strong></span><span class="sxs-lookup"><span data-stu-id="4b8a4-247"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="4b8a4-248">不可</span><span class="sxs-lookup"><span data-stu-id="4b8a4-248">No</span></span></p></td>
<td><p><span data-ttu-id="4b8a4-249">コンピューターごとの失敗したセッションの相対的なランク付け。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-249">Relative ranking failed sessions per computer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b8a4-250"><strong>[トップのソース]</strong></span><span class="sxs-lookup"><span data-stu-id="4b8a4-250"><strong>Top sources</strong></span></span></p></td>
<td><p><span data-ttu-id="4b8a4-251">不可</span><span class="sxs-lookup"><span data-stu-id="4b8a4-251">No</span></span></p></td>
<td><p><span data-ttu-id="4b8a4-252">失敗したセッションに含まれるコンピューターの名前。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-252">Name of the computer involved in the failed session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b8a4-253"><strong>[セッション]</strong></span><span class="sxs-lookup"><span data-stu-id="4b8a4-253"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="4b8a4-254">不可</span><span class="sxs-lookup"><span data-stu-id="4b8a4-254">No</span></span></p></td>
<td><p><span data-ttu-id="4b8a4-255">コンピューターごとの失敗したセッションの総数。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-255">Total number of failed sessions per computer.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-components"></a><span data-ttu-id="4b8a4-256">トップ コンポーネントの指標</span><span class="sxs-lookup"><span data-stu-id="4b8a4-256">Metrics for Top Components</span></span>

<span data-ttu-id="4b8a4-257">次の表に、障害が発生した Microsoft Lync Server 2010 コンポーネントに基づいたエラー分散レポートに記載されている情報を示します。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-257">The following table lists the information provided in the Failure Distribution Report based on the Microsoft Lync Server 2010 components that experienced the most failures.</span></span>

### <a name="metrics-for-top-components"></a><span data-ttu-id="4b8a4-258">トップのコンポーネントの指標</span><span class="sxs-lookup"><span data-stu-id="4b8a4-258">Metrics for Top Components</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4b8a4-259">名前</span><span class="sxs-lookup"><span data-stu-id="4b8a4-259">Name</span></span></th>
<th><span data-ttu-id="4b8a4-260">この項目での並べ替え</span><span class="sxs-lookup"><span data-stu-id="4b8a4-260">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="4b8a4-261">説明</span><span class="sxs-lookup"><span data-stu-id="4b8a4-261">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b8a4-262"><strong>[ランク]</strong></span><span class="sxs-lookup"><span data-stu-id="4b8a4-262"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="4b8a4-263">不可</span><span class="sxs-lookup"><span data-stu-id="4b8a4-263">No</span></span></p></td>
<td><p><span data-ttu-id="4b8a4-264">Lync Server 2010 コンポーネント (ExumRouting、GroupChat、MediationServer など) に基づく、失敗したセッションの相対的なランク。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-264">Relative ranking of failed sessions based on Lync Server 2010 component (for example, ExumRouting, GroupChat, or MediationServer).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b8a4-265"><strong>[トップのコンポーネント]</strong></span><span class="sxs-lookup"><span data-stu-id="4b8a4-265"><strong>Top components</strong></span></span></p></td>
<td><p><span data-ttu-id="4b8a4-266">不可</span><span class="sxs-lookup"><span data-stu-id="4b8a4-266">No</span></span></p></td>
<td><p><span data-ttu-id="4b8a4-267">失敗したセッションに含まれるコンポーネントの名前。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-267">Name of the component involved in the failed session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b8a4-268"><strong>[セッション]</strong></span><span class="sxs-lookup"><span data-stu-id="4b8a4-268"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="4b8a4-269">不可</span><span class="sxs-lookup"><span data-stu-id="4b8a4-269">No</span></span></p></td>
<td><p><span data-ttu-id="4b8a4-270">コンポーネントごとの失敗したセッションの総数。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-270">Total number of failed sessions per component.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-from-users"></a><span data-ttu-id="4b8a4-271">トップの発信元ユーザーの指標</span><span class="sxs-lookup"><span data-stu-id="4b8a4-271">Metrics for Top From Users</span></span>

<span data-ttu-id="4b8a4-272">次の表に、他のユーザーを呼び出したときに最もエラーが発生したユーザー ("発信元" ユーザーと呼ばれる) に基づいて、エラー分布レポートで提供される情報を示します。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-272">The following table lists the information provided in the Failure Distribution Report based on users who experienced the most failures when they tried to call someone else (known as "From" users).</span></span>

### <a name="metrics-for-top-from-users"></a><span data-ttu-id="4b8a4-273">トップの発信元ユーザーの指標</span><span class="sxs-lookup"><span data-stu-id="4b8a4-273">Metrics for Top From Users</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4b8a4-274">名前</span><span class="sxs-lookup"><span data-stu-id="4b8a4-274">Name</span></span></th>
<th><span data-ttu-id="4b8a4-275">この項目での並べ替え</span><span class="sxs-lookup"><span data-stu-id="4b8a4-275">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="4b8a4-276">説明</span><span class="sxs-lookup"><span data-stu-id="4b8a4-276">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b8a4-277"><strong>[ランク]</strong></span><span class="sxs-lookup"><span data-stu-id="4b8a4-277"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="4b8a4-278">不可</span><span class="sxs-lookup"><span data-stu-id="4b8a4-278">No</span></span></p></td>
<td><p><span data-ttu-id="4b8a4-279">セッションに招待されたユーザーに基づく、失敗したセッションの相対的なランク付け。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-279">Relative ranking of failed sessions based on the user who was invited to join the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b8a4-280"><strong>[トップの発信元ユーザー]</strong></span><span class="sxs-lookup"><span data-stu-id="4b8a4-280"><strong>Top from users</strong></span></span></p></td>
<td><p><span data-ttu-id="4b8a4-281">不可</span><span class="sxs-lookup"><span data-stu-id="4b8a4-281">No</span></span></p></td>
<td><p><span data-ttu-id="4b8a4-282">セッションに招待されたユーザーの SIP アドレス。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-282">SIP address of the user invited to join the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b8a4-283"><strong>[セッション]</strong></span><span class="sxs-lookup"><span data-stu-id="4b8a4-283"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="4b8a4-284">不可</span><span class="sxs-lookup"><span data-stu-id="4b8a4-284">No</span></span></p></td>
<td><p><span data-ttu-id="4b8a4-285">ユーザーごとの失敗したセッションの総数。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-285">Total number of failed sessions per user.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-to-users"></a><span data-ttu-id="4b8a4-286">トップの発信先ユーザーの指標</span><span class="sxs-lookup"><span data-stu-id="4b8a4-286">Metrics for Top To Users</span></span>

<span data-ttu-id="4b8a4-287">次の表に、ユーザーが他のユーザーを呼び出したときに最もエラーが発生したユーザー ("発信先" ユーザーと呼ばれる) に基づいて、エラー分布レポートで提供される情報を示します。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-287">The following table lists the information provided in the Failure Distribution Report based on the users who experienced the most failures when another user tried to call them (known as "To" users).</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4b8a4-288">名前</span><span class="sxs-lookup"><span data-stu-id="4b8a4-288">Name</span></span></th>
<th><span data-ttu-id="4b8a4-289">この項目での並べ替え</span><span class="sxs-lookup"><span data-stu-id="4b8a4-289">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="4b8a4-290">説明</span><span class="sxs-lookup"><span data-stu-id="4b8a4-290">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b8a4-291"><strong>[ランク]</strong></span><span class="sxs-lookup"><span data-stu-id="4b8a4-291"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="4b8a4-292">不可</span><span class="sxs-lookup"><span data-stu-id="4b8a4-292">No</span></span></p></td>
<td><p><span data-ttu-id="4b8a4-293">セッションを開始したユーザーに基づく、失敗したセッションの相対的なランク付け。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-293">Relative ranking of failed sessions based on the user who initiated the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b8a4-294"><strong>[トップの発信先ユーザー]</strong></span><span class="sxs-lookup"><span data-stu-id="4b8a4-294"><strong>Top to users</strong></span></span></p></td>
<td><p><span data-ttu-id="4b8a4-295">不可</span><span class="sxs-lookup"><span data-stu-id="4b8a4-295">No</span></span></p></td>
<td><p><span data-ttu-id="4b8a4-296">セッションを開始したユーザーの SIP アドレス。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-296">SIP address of the user who initiated the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b8a4-297"><strong>[セッション]</strong></span><span class="sxs-lookup"><span data-stu-id="4b8a4-297"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="4b8a4-298">不可</span><span class="sxs-lookup"><span data-stu-id="4b8a4-298">No</span></span></p></td>
<td><p><span data-ttu-id="4b8a4-299">ユーザーごとの失敗したセッションの総数。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-299">Total number of failed sessions per user.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-user-agents"></a><span data-ttu-id="4b8a4-300">トップ ユーザー エージェントの指標</span><span class="sxs-lookup"><span data-stu-id="4b8a4-300">Metrics for Top User Agents</span></span>

<span data-ttu-id="4b8a4-301">次の表に、最もエラーが発生したエンドポイント ソフトウェアに基づいて、エラー分布レポートで提供される情報を示します。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-301">The following table lists the information provided in the Failure Distribution Report based on the endpoint software that experienced the most failures.</span></span>

### <a name="metrics-for-top-user-agents"></a><span data-ttu-id="4b8a4-302">トップ ユーザー エージェントの指標</span><span class="sxs-lookup"><span data-stu-id="4b8a4-302">Metrics for Top User Agents</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4b8a4-303">名前</span><span class="sxs-lookup"><span data-stu-id="4b8a4-303">Name</span></span></th>
<th><span data-ttu-id="4b8a4-304">この項目での並べ替え</span><span class="sxs-lookup"><span data-stu-id="4b8a4-304">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="4b8a4-305">説明</span><span class="sxs-lookup"><span data-stu-id="4b8a4-305">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b8a4-306"><strong>[ランク]</strong></span><span class="sxs-lookup"><span data-stu-id="4b8a4-306"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="4b8a4-307">不可</span><span class="sxs-lookup"><span data-stu-id="4b8a4-307">No</span></span></p></td>
<td><p><span data-ttu-id="4b8a4-p115">セッションに含まれるユーザー エージェント (ソフトウェア) に基づく、失敗したセッションの相対的なランク付け。例: RTCC/4.0.0.0 Inbound Routing/4.0.0.0。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-p115">Relative ranking of failed sessions based on the user agent (software) involved in the session. For example: RTCC/4.0.0.0 Inbound Routing/4.0.0.0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b8a4-310"><strong>[トップ ユーザー エージェント]</strong></span><span class="sxs-lookup"><span data-stu-id="4b8a4-310"><strong>Top user agents</strong></span></span></p></td>
<td><p><span data-ttu-id="4b8a4-311">不可</span><span class="sxs-lookup"><span data-stu-id="4b8a4-311">No</span></span></p></td>
<td><p><span data-ttu-id="4b8a4-312">失敗したセッションに含まれるユーザー エージェントの名前。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-312">Name of the user agent involved in the failed session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b8a4-313"><strong>[セッション]</strong></span><span class="sxs-lookup"><span data-stu-id="4b8a4-313"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="4b8a4-314">不可</span><span class="sxs-lookup"><span data-stu-id="4b8a4-314">No</span></span></p></td>
<td><p><span data-ttu-id="4b8a4-315">ユーザー エージェントごとの失敗したセッションの総数。</span><span class="sxs-lookup"><span data-stu-id="4b8a4-315">Total number of failed sessions per user agent.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="4b8a4-316">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4b8a4-316">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

