---
title: 'Lync Server 2013: サーバーパフォーマンスレポート'
description: 'Lync Server 2013: サーバーパフォーマンスレポート。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Server Performance Report
ms:assetid: 942bb39a-1790-498e-9d99-8f6ce2d155c3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615018(v=OCS.15)
ms:contentKeyID: 48184879
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: aed9b3b9eeec4487dce4d401df0d70ffba89677b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441880"
---
# <a name="server-performance-report-in-lync-server-2013"></a><span data-ttu-id="1034c-103">Lync Server 2013 のサーバーパフォーマンスレポート</span><span class="sxs-lookup"><span data-stu-id="1034c-103">Server Performance Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1034c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1034c-104">

<span> </span></span></span>

<span data-ttu-id="1034c-105">_**最終更新日:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="1034c-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="1034c-106">サーバーパフォーマンスレポートには、高品質の通話が低割合で発生している Microsoft Lync Server 2013 サーバーの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="1034c-106">The Server Performance Report provides a list of Microsoft Lync Server 2013 servers that have experienced the highest-percentage of poor calls.</span></span> <span data-ttu-id="1034c-107">このレポートでは、サーバーが種類ごとに分類され、以下の種類のサーバーの個別の統計情報が報告されます。</span><span class="sxs-lookup"><span data-stu-id="1034c-107">The report breaks down servers by server type, reporting separate statistics for the following types:</span></span>

  - <span data-ttu-id="1034c-108">仲介サーバー</span><span class="sxs-lookup"><span data-stu-id="1034c-108">Mediation Server</span></span>

  - <span data-ttu-id="1034c-109">音声ビデオ会議サーバー</span><span class="sxs-lookup"><span data-stu-id="1034c-109">A/V Conferencing Server</span></span>

  - <span data-ttu-id="1034c-110">音声ビデオ エッジ サーバー</span><span class="sxs-lookup"><span data-stu-id="1034c-110">A/V Edge Server</span></span>

  - <span data-ttu-id="1034c-111">ゲートウェイ (仲介サーバー)</span><span class="sxs-lookup"><span data-stu-id="1034c-111">Gateway (Mediation Server)</span></span>

  - <span data-ttu-id="1034c-112">ゲートウェイ (仲介サーバーのバイパス)</span><span class="sxs-lookup"><span data-stu-id="1034c-112">Gateway (Mediation Server bypass)</span></span>

  - <span data-ttu-id="1034c-113">ビデオ (音声ビデオ会議サーバーと音声ビデオ エッジ サーバーのビデオ指標を含む)</span><span class="sxs-lookup"><span data-stu-id="1034c-113">Video (including video metrics for A/V Conferencing servers and A/V Edge servers)</span></span>

  - <span data-ttu-id="1034c-114">アプリケーション共有 (音声ビデオ会議サーバーと音声ビデオ エッジ サーバーのアプリケーション共有指標を含む)</span><span class="sxs-lookup"><span data-stu-id="1034c-114">Application Sharing (including application sharing metrics for A/V Conferencing servers and A/V Edge servers)</span></span>

<span data-ttu-id="1034c-p102">このレポートに表示されるランク付けは相対的なランク付けであることに注意してください。たとえば、最もパフォーマンスの低いサーバーで発信された 1,000 件の通話のうち、低品質通話が 1 件あったとします。この場合、容認可能な低品質通話のパーセンテージは 0.1% です。しかし、それが最もパフォーマンスの低いサーバーである場合 (つまり、他のすべてのサーバーの低品質通話のパーセンテージが 0.1% 未満の場合)、そのサーバーは引き続きサーバー パフォーマンス レポートに表示されます。</span><span class="sxs-lookup"><span data-stu-id="1034c-p102">It’s important to note that the ranking shown in this report as relative rankings. For example, suppose your worst-performing server had one poor call among its 1,000 placed calls. That's a more-than-acceptable percentage of .1%. However, if that's the worst-performing server you have (that is, if all your other servers have a poor call percentage even lower than .1%), then that server will still appear on the Server Performance Report.</span></span>

<div>

## <a name="accessing-the-server-performance-report"></a><span data-ttu-id="1034c-119">サーバー パフォーマンス レポートへのアクセス</span><span class="sxs-lookup"><span data-stu-id="1034c-119">Accessing the Server Performance Report</span></span>

<span data-ttu-id="1034c-120">サーバー パフォーマンス レポートには、監視レポートのホーム ページからアクセスします。</span><span class="sxs-lookup"><span data-stu-id="1034c-120">The Server Performance Report is accessed from the Monitoring Reports home page.</span></span> <span data-ttu-id="1034c-121">次の指標のいずれかをクリックして、 [Lync Server 2013 の通話リストレポート](lync-server-2013-call-list-report.md) にドリルダウンすることができます。</span><span class="sxs-lookup"><span data-stu-id="1034c-121">You can drill down to the [Call List Report in Lync Server 2013](lync-server-2013-call-list-report.md) by clicking either of the following metrics:</span></span>

  - <span data-ttu-id="1034c-122">通話ボリューム</span><span class="sxs-lookup"><span data-stu-id="1034c-122">Call volume</span></span>

  - <span data-ttu-id="1034c-123">低品質通話のパーセンテージ</span><span class="sxs-lookup"><span data-stu-id="1034c-123">Poor call percentage</span></span>

<span data-ttu-id="1034c-124">また、次の指標をクリックして、サーバー メディア品質傾向レポートにドリルダウンすることもできます。</span><span class="sxs-lookup"><span data-stu-id="1034c-124">In addition, you can drill down to the Server Media Quality Trend Report by clicking the following metric:</span></span>

  - <span data-ttu-id="1034c-125">傾向</span><span class="sxs-lookup"><span data-stu-id="1034c-125">Trend</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-server-performance-report"></a><span data-ttu-id="1034c-126">サーバーパフォーマンスレポートを最大限に活用する</span><span class="sxs-lookup"><span data-stu-id="1034c-126">Making the Best Use of the Server Performance Report</span></span>

<span data-ttu-id="1034c-p104">サーバー パフォーマンス レポートには、データをフィルター処理する方法が複数用意されています。たとえば、ネットワークの種類 (有線接続で行われた通話とワイヤレス接続で行われた通話) やアクセスの種類 (ファイヤウォールの内側から行われた通話とファイヤウォールの外側から行われた通話) でフィルター処理することができます。サーバー パフォーマンス レポートを表示するときは、これらのフィルターを利用することをお勧めします。たとえば、低品質通話のパーセンテージが 3.24% の仲介サーバーがあるとします。ワイヤレス通話だけを見ると、同じサーバーの低品質通話のパーセンテージは 20% 近くになっています。つまり、このサーバーのワイヤレス通話には問題がありますが、有線通話に関する問題はなかったため、問題の一部が不明瞭になっていたことがわかります。</span><span class="sxs-lookup"><span data-stu-id="1034c-p104">The Server Performance Report provides a number of ways to filter data; for example, you can filter on network type (calls made from a wired connection vs. calls made from a wireless connection) and access type (calls made from inside the firewall vs. calls made from outside the firewall). It's a good idea when viewing the server performance report to make use of these filters. For example, suppose you have a Mediation Server that has a poor call percentage of 3.24%. If you look solely at wireless calls, that same server might have a poor call percentage approaching 20%. That means that the server was having difficulty with wireless calls, a problem that is partially obscured because the server was not having problems with wired calls.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="1034c-132">フィルター</span><span class="sxs-lookup"><span data-stu-id="1034c-132">Filters</span></span>

<span data-ttu-id="1034c-p105">フィルターは、細かく絞り込んだデータ セットを返したり、返されたデータをさまざまな方法で表示したりする方法として利用できます。たとえば、サーバー パフォーマンス レポートでは、返されたデータをサーバーの種類またはネットワークの種類 (有線またはワイヤレス) 別に表示することができます。また、データをグループ化する方法を選択することもできます。この場合は、データが時間、日、週、または月を基準にグループ化されます。</span><span class="sxs-lookup"><span data-stu-id="1034c-p105">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Server Performance Report enables you to do such things as filter the returned data by server type or by network type (that is, wired or wireless). You can also choose how data should be grouped. In this case, data is grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="1034c-137">次の表に、サーバー パフォーマンス レポートで使用できるフィルターを示します。</span><span class="sxs-lookup"><span data-stu-id="1034c-137">The following table lists the filters that you can use with the Server Performance Report.</span></span>

### <a name="server-performance-report-filters"></a><span data-ttu-id="1034c-138">サーバー パフォーマンス レポートのフィルター</span><span class="sxs-lookup"><span data-stu-id="1034c-138">Server Performance Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1034c-139">名前</span><span class="sxs-lookup"><span data-stu-id="1034c-139">Name</span></span></th>
<th><span data-ttu-id="1034c-140">説明</span><span class="sxs-lookup"><span data-stu-id="1034c-140">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1034c-141"><strong>開始</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-141"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="1034c-p106">時間範囲の開始日と開始時刻。データを時間単位で表示するには、次のように開始日と開始時刻の両方を入力します。</span><span class="sxs-lookup"><span data-stu-id="1034c-p106">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="1034c-144">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="1034c-144">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="1034c-p107">開始時刻を入力しないと、レポートは自動的に指定日の午前 12:00 に開始します。データを日単位で表示するには、次のように日付のみを入力します。</span><span class="sxs-lookup"><span data-stu-id="1034c-p107">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="1034c-147">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="1034c-147">7/7/2012</span></span></p>
<p><span data-ttu-id="1034c-148">週単位または月単位で表示するには、表示する週または月の任意の日付を入力します (その週または月の最初の日である必要はありません)。</span><span class="sxs-lookup"><span data-stu-id="1034c-148">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="1034c-149">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="1034c-149">7/3/2012</span></span></p>
<p><span data-ttu-id="1034c-150">一週間は、日曜日から始まり、土曜日で終わるものとします。</span><span class="sxs-lookup"><span data-stu-id="1034c-150">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1034c-151"><strong>終了</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-151"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="1034c-p108">時間範囲の終了日と終了時刻。データを時間単位で表示するには、次のように終了日と終了時刻の両方を入力します。</span><span class="sxs-lookup"><span data-stu-id="1034c-p108">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="1034c-154">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="1034c-154">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="1034c-p109">終了時刻を入力しないと、レポートは自動的に指定日の午前 12:00 に終了します。データを日単位で表示するには、次のように日付のみを入力します。</span><span class="sxs-lookup"><span data-stu-id="1034c-p109">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="1034c-157">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="1034c-157">7/7/2012</span></span></p>
<p><span data-ttu-id="1034c-158">週単位または月単位で表示するには、表示する週または月の任意の日付を入力します (その週または月の最初の日である必要はありません)。</span><span class="sxs-lookup"><span data-stu-id="1034c-158">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="1034c-159">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="1034c-159">7/3/2012</span></span></p>
<p><span data-ttu-id="1034c-160">一週間は、日曜日から始まり、土曜日で終わるものとします。</span><span class="sxs-lookup"><span data-stu-id="1034c-160">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1034c-161"><strong>[サーバーの種類]</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-161"><strong>Server type</strong></span></span></p></td>
<td><p><span data-ttu-id="1034c-p110">どのサーバーのパフォーマンスを報告するのか、その対象となるサーバーの種類を示します。次のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="1034c-p110">Indicates the type of server whose performance should be reported. Select one of the following:</span></span></p>
<ol>
<li><p><span data-ttu-id="1034c-164">[すべて]</span><span class="sxs-lookup"><span data-stu-id="1034c-164">[All]</span></span></p></li>
<li><p><span data-ttu-id="1034c-165">仲介サーバー</span><span class="sxs-lookup"><span data-stu-id="1034c-165">Mediation Server</span></span></p></li>
<li><p><span data-ttu-id="1034c-166">音声ビデオ会議サーバー</span><span class="sxs-lookup"><span data-stu-id="1034c-166">A/V Conferencing Server</span></span></p></li>
<li><p><span data-ttu-id="1034c-167">音声ビデオ エッジ サーバー</span><span class="sxs-lookup"><span data-stu-id="1034c-167">A/V Edge Server</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1034c-168"><strong>[トップ N]</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-168"><strong>Top N</strong></span></span></p></td>
<td><p><span data-ttu-id="1034c-p111">カテゴリごとに表示するサーバーの個数 (低品質通話のパーセンテージに基づく) を示します。たとえば、[<strong>5</strong>] を選択すると、特にパフォーマンスの低い 5 個のサーバーが表示されます。次のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="1034c-p111">Indicates the number of servers (based on their poor call percentage) to be displayed in each category. For example, if you select <strong>5</strong> then the five poorest-performing servers are displayed. Select one of the following:</span></span></p>
<ol>
<li><p><span data-ttu-id="1034c-172">[すべて]</span><span class="sxs-lookup"><span data-stu-id="1034c-172">[All]</span></span></p></li>
<li><p><span data-ttu-id="1034c-173">5</span><span class="sxs-lookup"><span data-stu-id="1034c-173">5</span></span></p></li>
<li><p><span data-ttu-id="1034c-174">常用</span><span class="sxs-lookup"><span data-stu-id="1034c-174">10</span></span></p></li>
</ol></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1034c-175"><strong>[アクセスの種類]</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-175"><strong>Access type</strong></span></span></p></td>
<td><p><span data-ttu-id="1034c-p112">クライアントが通話時に内部ネットワークにログオンしたか、外部ネットワークにログオンしたかを示します。次のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="1034c-p112">Indicates whether the client was logged on to the internal network or the external network when the call was placed. Select one of the following:</span></span></p>
<ol>
<li><p><span data-ttu-id="1034c-178">[すべて]</span><span class="sxs-lookup"><span data-stu-id="1034c-178">[All]</span></span></p></li>
<li><p><span data-ttu-id="1034c-179">内部</span><span class="sxs-lookup"><span data-stu-id="1034c-179">Internal</span></span></p></li>
<li><p><span data-ttu-id="1034c-180">外部</span><span class="sxs-lookup"><span data-stu-id="1034c-180">External</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1034c-181"><strong>[ネットワークの種類]</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-181"><strong>Network type</strong></span></span></p></td>
<td><p><span data-ttu-id="1034c-p113">通話時にクライアントが接続したネットワークの種類を示します。次のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="1034c-p113">Indicates the type of network the client was connected to when the call was placed. Select one of the following:</span></span></p>
<ol>
<li><p><span data-ttu-id="1034c-184">[すべて]</span><span class="sxs-lookup"><span data-stu-id="1034c-184">[All]</span></span></p></li>
<li><p><span data-ttu-id="1034c-185">有線</span><span class="sxs-lookup"><span data-stu-id="1034c-185">Wired</span></span></p></li>
<li><p><span data-ttu-id="1034c-186">ワイヤレス</span><span class="sxs-lookup"><span data-stu-id="1034c-186">Wireless</span></span></p></li>
</ol></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1034c-187"><strong>VPN</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-187"><strong>VPN</strong></span></span></p></td>
<td><p><span data-ttu-id="1034c-p114">通話時に外部クライアントが仮想プライベート ネットワーク (VPN) 接続を使用したかどうかを示します。次のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="1034c-p114">Indicates whether an external client was using a virtual private network (VPN) connection when the call was placed. Select one of the following:</span></span></p>
<ol>
<li><p><span data-ttu-id="1034c-190">[すべて]</span><span class="sxs-lookup"><span data-stu-id="1034c-190">[All]</span></span></p></li>
<li><p><span data-ttu-id="1034c-191">VPN</span><span class="sxs-lookup"><span data-stu-id="1034c-191">VPN</span></span></p></li>
<li><p><span data-ttu-id="1034c-192">非 VPN</span><span class="sxs-lookup"><span data-stu-id="1034c-192">Non-VPN</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="1034c-193">指標</span><span class="sxs-lookup"><span data-stu-id="1034c-193">Metrics</span></span>

<span data-ttu-id="1034c-194">次の表に、サーバー パフォーマンス レポートで提供される情報を示します。</span><span class="sxs-lookup"><span data-stu-id="1034c-194">The following table lists the information provided in the Server Performance Report.</span></span>

### <a name="server-performance-report-metrics-audio-call-summary"></a><span data-ttu-id="1034c-195">サーバー パフォーマンス レポートの指標: 音声通話の概要</span><span class="sxs-lookup"><span data-stu-id="1034c-195">Server Performance Report Metrics: Audio Call Summary</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1034c-196">名前</span><span class="sxs-lookup"><span data-stu-id="1034c-196">Name</span></span></th>
<th><span data-ttu-id="1034c-197">この項目での並べ替え</span><span class="sxs-lookup"><span data-stu-id="1034c-197">Can Sort On</span></span></th>
<th><span data-ttu-id="1034c-198">説明</span><span class="sxs-lookup"><span data-stu-id="1034c-198">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1034c-199"><strong>[サーバー]</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-199"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1034c-200">不可</span><span class="sxs-lookup"><span data-stu-id="1034c-200">No</span></span></p></td>
<td><p><span data-ttu-id="1034c-201">サーバーの名前/IP アドレス。</span><span class="sxs-lookup"><span data-stu-id="1034c-201">Name/IP address of the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1034c-202"><strong>[通話ボリューム]</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-202"><strong>Call volume</strong></span></span></p></td>
<td><p><span data-ttu-id="1034c-203">不可</span><span class="sxs-lookup"><span data-stu-id="1034c-203">No</span></span></p></td>
<td><p><span data-ttu-id="1034c-204">通話の総数。</span><span class="sxs-lookup"><span data-stu-id="1034c-204">Total number of calls made.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1034c-205"><strong>[低品質通話のパーセンテージ]</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-205"><strong>Poor call percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="1034c-206">不可</span><span class="sxs-lookup"><span data-stu-id="1034c-206">No</span></span></p></td>
<td><p><span data-ttu-id="1034c-p115">低品質として分類される通話の総数。低品質通話とは、少なくとも 1 つの測定指標が許容値を超えている通話 (たとえば、過剰なジッターが発生した通話) のことです。</span><span class="sxs-lookup"><span data-stu-id="1034c-p115">Total number of calls classified as poor. A poor call is any call which at least one of the measured metrics exceeded the allowed value (for example, a call that experienced excessive jitter).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1034c-209"><strong>[往復 (ミリ秒)]</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-209"><strong>Round trip (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="1034c-210">可</span><span class="sxs-lookup"><span data-stu-id="1034c-210">Yes</span></span></p></td>
<td><p><span data-ttu-id="1034c-p116">リアルタイム転送プロトコル (RTP) パケットが別のエンドポイントとの間を往復するのに要する平均時間 (ミリ秒単位)。100 ミリ秒以下の往復時間が許容できる品質と見なされます。</span><span class="sxs-lookup"><span data-stu-id="1034c-p116">Average amount of (in milliseconds) required for a real-time transport protocol (RTP) packet to travel to another endpoint and then back. Round-trip times of 100 milliseconds or less are considered of acceptable quality.</span></span></p>
<p><span data-ttu-id="1034c-p117">この値が高い場合は、国際通話ルーティング、ルーティングの構成ミス、メディア サーバーの過負荷などの原因が考えられます。その結果、双方向のリアルタイムの音声会話が難しくなります。</span><span class="sxs-lookup"><span data-stu-id="1034c-p117">High round-trip values can be caused by international call routing; a routing misconfiguration; or an overloaded media server. High round-trip times result in difficulties with two-way, real-time audio conversations.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1034c-215"><strong>[低下 (MOS)]</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-215"><strong>Degradation (MOS)</strong></span></span></p></td>
<td><p><span data-ttu-id="1034c-216">可</span><span class="sxs-lookup"><span data-stu-id="1034c-216">Yes</span></span></p></td>
<td><p><span data-ttu-id="1034c-217">通話時に発生した平均オピニオン値 (MOS) 低下の平均値。</span><span class="sxs-lookup"><span data-stu-id="1034c-217">Average amount of mean opinion score (MOS) degradation experienced during a call.</span></span> <span data-ttu-id="1034c-218">低下の値範囲は、最低 0.0 から最高 5.0 までとなります。</span><span class="sxs-lookup"><span data-stu-id="1034c-218">Degradation values can range from a low of 0.0 to a high of 5.0.</span></span> <span data-ttu-id="1034c-219">0.5 以下の値は、許容される低下を表します。</span><span class="sxs-lookup"><span data-stu-id="1034c-219">A value of 0.5 or less represents acceptable degradation.</span></span> <span data-ttu-id="1034c-220">従来、平均オピニオン値は、ユーザーが通話の品質を 1 から 5 の範囲で評価することによって計算されていました。</span><span class="sxs-lookup"><span data-stu-id="1034c-220">Historically, mean options scores were calculated by having users rate the quality of a call on a scale of 1-to-5.</span></span> <span data-ttu-id="1034c-221">Lync Server では、監視サーバーは一連のアルゴリズムを使って、ユーザーがどのように通話を評価したかを予測します。</span><span class="sxs-lookup"><span data-stu-id="1034c-221">In Lync Server, the Monitoring Server uses a set of algorithms to predict how users would have rated a call.</span></span></p>
<p><span data-ttu-id="1034c-p119">この値が高い場合は、輻輳、帯域幅の不足、ワイヤレスの輻輳または干渉、メディア サーバーやエンドポイントの過負荷などの原因が考えられます。その結果、音声のひずみや欠落が生じます。</span><span class="sxs-lookup"><span data-stu-id="1034c-p119">High degradation values can be caused by congestion, lack of bandwidth, wireless congestion or interference, or an overloaded media server or endpoint. High degradation results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1034c-224"><strong>パケット損失</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-224"><strong>Packet loss</strong></span></span></p></td>
<td><p><span data-ttu-id="1034c-225">可</span><span class="sxs-lookup"><span data-stu-id="1034c-225">Yes</span></span></p></td>
<td><p><span data-ttu-id="1034c-p120">リアルタイム転送プロトコル (RTP) パケット損失の平均レート (パケット損失は、RTP パケット、つまりインターネット経由で音声とビデオを転送するために使われるプロトコルの一種で、パケットが宛先に到達できなかったときに発生します)。この値が高い場合は、輻輳、帯域幅の不足、ワイヤレスの輻輳または干渉、メディア サーバーの過負荷などの原因が考えられます。パケット損失が発生すると、通常、音声のひずみや欠落が生じます。</span><span class="sxs-lookup"><span data-stu-id="1034c-p120">Average rate of real-time transport protocol (RTP) packet loss. (Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion, lack of bandwidth, wireless congestion or interference, or an overloaded media server. Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1034c-229"><strong>[ジッター (ミリ秒)]</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-229"><strong>Jitter (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="1034c-230">可</span><span class="sxs-lookup"><span data-stu-id="1034c-230">Yes</span></span></p></td>
<td><p><span data-ttu-id="1034c-231">RTP パケットの着信間に検出された平均ジッター (ジッターとは、通話の "揺れ" の測定値です)。</span><span class="sxs-lookup"><span data-stu-id="1034c-231">Average jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="1034c-232">(ジッタは、 &quot; 通話の shakiness の尺度です &quot; )。通常、高ジッターの値は、輻輳または過負荷のメディアサーバーによって発生し、音声が歪むか、失われる原因となります。</span><span class="sxs-lookup"><span data-stu-id="1034c-232">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1034c-233"><strong>ヒーラー隠し比率</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-233"><strong>Healer concealed ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="1034c-234">可</span><span class="sxs-lookup"><span data-stu-id="1034c-234">Yes</span></span></p></td>
<td><p><span data-ttu-id="1034c-p122">サンプルの合計数に対する隠しオーディオ サンプルの平均比率 (隠しオーディオ サンプルとは、突然遷移を取り除くために使用される手法です。突然遷移は、通常、ネットワーク パケットの削除が原因で発生します)。この値が高い場合は、パケット損失やジッターのために高いレベルで損失の隠蔽が適用されています。その結果、音声のひずみや欠落が生じます。</span><span class="sxs-lookup"><span data-stu-id="1034c-p122">Average ratio of concealed audio samples to the total to the total number of samples. (A concealed audio sample is a technique used to smooth out the abrupt transition that would usually be caused by dropped network packets.) High values indicate significant levels of loss concealment applied caused by packet loss or jitter, and results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1034c-237"><strong>ヒーラー引き伸ばし比率</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-237"><strong>Healer stretched ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="1034c-238">可</span><span class="sxs-lookup"><span data-stu-id="1034c-238">Yes</span></span></p></td>
<td><p><span data-ttu-id="1034c-p123">サンプルの合計数に対する引き伸ばされたオーディオ サンプルの平均比率 (引き伸ばされたオーディオとは、ネットワーク パケットの削除が検出されたときに通話の品質を維持できるように拡張されたオーディオのことです)。この値が高い場合は、ジッターのために高いレベルでサンプルの引き伸ばしが行われています。その結果、音声が機械のように聞こえたりひずんで聞こえたりします。</span><span class="sxs-lookup"><span data-stu-id="1034c-p123">Average ratio of stretched audio samples to the total to the total number of samples. (Stretched audio is audio that has been expanded to help maintain call quality when a dropped network packet has been detected.) High values indicate significant levels of sample stretching caused by jitter, and result in audio sounding robotic or distorted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1034c-241"><strong>ヒーラー圧縮比率</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-241"><strong>Healer compressed ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="1034c-242">可</span><span class="sxs-lookup"><span data-stu-id="1034c-242">Yes</span></span></p></td>
<td><p><span data-ttu-id="1034c-p124">サンプルの合計数に対する圧縮オーディオ サンプルの平均比率 (圧縮オーディオとは、ネットワーク パケットの削除が検出されたときに通話の品質を維持できるように圧縮されたオーディオのことです)。この値が高い場合は、ジッターのために高いレベルでサンプルの圧縮が行われています。その結果、音声が早送りされたように聞こえたりひずんで聞こえたりします。</span><span class="sxs-lookup"><span data-stu-id="1034c-p124">Average ratio of compressed audio samples to the total number of samples. (Compressed audio is audio that has been compressed to help maintain call quality when a dropped network packet has been detected.) High values indicate significant levels of sample compression caused by jitter, and result in audio sounding accelerated or distorted.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="server-performance-report-metrics-video-call-summary"></a><span data-ttu-id="1034c-245">サーバー パフォーマンス レポートの指標: ビデオ通話の概要</span><span class="sxs-lookup"><span data-stu-id="1034c-245">Server Performance Report Metrics: Video Call Summary</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1034c-246">名前</span><span class="sxs-lookup"><span data-stu-id="1034c-246">Name</span></span></th>
<th><span data-ttu-id="1034c-247">この項目での並べ替え</span><span class="sxs-lookup"><span data-stu-id="1034c-247">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="1034c-248">説明</span><span class="sxs-lookup"><span data-stu-id="1034c-248">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1034c-249"><strong>[通話の種類/エンドポイントの種類]</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-249"><strong>Call type/Endpoint type</strong></span></span></p></td>
<td><p><span data-ttu-id="1034c-250">不可</span><span class="sxs-lookup"><span data-stu-id="1034c-250">No</span></span></p></td>
<td><p><span data-ttu-id="1034c-p125">この項目をクリックすると、その種類に基づく通話の詳細情報がレポートに表示されます。通話の種類は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="1034c-p125">When you click this item, the report shows detailed information about calls based on that type. Call types include:</span></span></p>
<ul>
<li><p><span data-ttu-id="1034c-253">UC ピアツーピア通話</span><span class="sxs-lookup"><span data-stu-id="1034c-253">UC Peer-to-Peer Calls</span></span></p></li>
<li><p><span data-ttu-id="1034c-254">UC 電話会議セッション</span><span class="sxs-lookup"><span data-stu-id="1034c-254">UC Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="1034c-255">PSTN 電話会議セッション</span><span class="sxs-lookup"><span data-stu-id="1034c-255">PSTN Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="1034c-256">PSTN 通話: メディアのバイパス</span><span class="sxs-lookup"><span data-stu-id="1034c-256">PSTN Calls: Media Bypass</span></span></p></li>
<li><p><span data-ttu-id="1034c-257">PSTN 通話 (非バイパス): UC レグ</span><span class="sxs-lookup"><span data-stu-id="1034c-257">PSTN Calls (Non-Bypass): UC Leg</span></span></p></li>
<li><p><span data-ttu-id="1034c-258">PSTN 通話 (非バイパス): ゲートウェイ レグ</span><span class="sxs-lookup"><span data-stu-id="1034c-258">PSTN Calls (Non-Bypass): Gateway Leg</span></span></p></li>
<li><p><span data-ttu-id="1034c-259">その他の通話の種類</span><span class="sxs-lookup"><span data-stu-id="1034c-259">Other Call Types</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1034c-260"><strong>[通話ボリューム]</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-260"><strong>Call volume</strong></span></span></p></td>
<td><p><span data-ttu-id="1034c-261">不可</span><span class="sxs-lookup"><span data-stu-id="1034c-261">No</span></span></p></td>
<td><p><span data-ttu-id="1034c-262">通話の種類あたりの通話の総数。</span><span class="sxs-lookup"><span data-stu-id="1034c-262">Total number of calls per call type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1034c-263"><strong>[低品質通話のパーセンテージ]</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-263"><strong>Poor call percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="1034c-264">不可</span><span class="sxs-lookup"><span data-stu-id="1034c-264">No</span></span></p></td>
<td><p><span data-ttu-id="1034c-p126">低品質として分類される通話の総数。低品質通話とは、少なくとも 1 つの測定指標が許容値を超えている通話 (たとえば、過剰なジッターが発生した通話) のことです。</span><span class="sxs-lookup"><span data-stu-id="1034c-p126">Total number of calls classified as poor. A poor call is any call which at least one of the measured metrics exceeded the allowed value (for example, a call that experienced excessive jitter).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1034c-267"><strong>[通話ボリューム (ワイヤレス通話)]</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-267"><strong>Call volume (wireless call)</strong></span></span></p></td>
<td><p><span data-ttu-id="1034c-268">不可</span><span class="sxs-lookup"><span data-stu-id="1034c-268">No</span></span></p></td>
<td><p><span data-ttu-id="1034c-269">ワイヤレス接続を使用した通話の数。</span><span class="sxs-lookup"><span data-stu-id="1034c-269">Total number of calls that used a wireless connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1034c-270"><strong>[通話ボリューム (VPN 通話)]</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-270"><strong>Call volume (VPN call)</strong></span></span></p></td>
<td><p><span data-ttu-id="1034c-271">不可</span><span class="sxs-lookup"><span data-stu-id="1034c-271">No</span></span></p></td>
<td><p><span data-ttu-id="1034c-272">VPN 接続を使用した通話の数。</span><span class="sxs-lookup"><span data-stu-id="1034c-272">Total number of calls that used a VPN connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1034c-273"><strong>[通話ボリューム (外部通話)]</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-273"><strong>Call volume (external call)</strong></span></span></p></td>
<td><p><span data-ttu-id="1034c-274">不可</span><span class="sxs-lookup"><span data-stu-id="1034c-274">No</span></span></p></td>
<td><p><span data-ttu-id="1034c-275">外部接続 (つまり、内部ネットワークの外側の接続) を使用した通話の数。</span><span class="sxs-lookup"><span data-stu-id="1034c-275">Number of calls that used an external connection (that is, a connection outside the internal network).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1034c-276"><strong>[平均ビット レート (キロビット/秒)]</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-276"><strong>Avg bit-rate (Kbits/s)</strong></span></span></p></td>
<td><p><span data-ttu-id="1034c-277">不可</span><span class="sxs-lookup"><span data-stu-id="1034c-277">No</span></span></p></td>
<td><p><span data-ttu-id="1034c-278">平均ビデオ ビット レート (kbps)。</span><span class="sxs-lookup"><span data-stu-id="1034c-278">Average video bit rate (in kilobits per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1034c-279"><strong>[低ビット レート (%)]</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-279"><strong>Low bit-rate %</strong></span></span></p></td>
<td><p><span data-ttu-id="1034c-280">不可</span><span class="sxs-lookup"><span data-stu-id="1034c-280">No</span></span></p></td>
<td><p><span data-ttu-id="1034c-281">ビット レートが低い通話のパーセンテージ。</span><span class="sxs-lookup"><span data-stu-id="1034c-281">Percentage of the call where the bit rate was low.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1034c-282"><strong>[送信パケット損失]</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-282"><strong>Outbound packet loss</strong></span></span></p></td>
<td><p><span data-ttu-id="1034c-283">不可</span><span class="sxs-lookup"><span data-stu-id="1034c-283">No</span></span></p></td>
<td><p><span data-ttu-id="1034c-p127">送信パケットのリアルタイム転送プロトコル (RTP) パケット損失 (パケット損失は、RTP パケット、つまりインターネット経由で音声とビデオを転送するために使われるプロトコルの一種で、パケットが宛先に到達できなかったときに発生します)。この値が高い場合は、輻輳、帯域幅の不足、ワイヤレスの輻輳または干渉、メディア サーバーの過負荷などの原因が考えられます。パケット損失が発生すると、通常、音声のひずみや欠落が生じます。</span><span class="sxs-lookup"><span data-stu-id="1034c-p127">Real-Time Transport Protocol (RTP) packet loss for outbound packets. (Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion; lack of bandwidth; wireless congestion or interference; or an overloaded media server. Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1034c-287"><strong>[フリーズ フレーム %]</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-287"><strong>Frozen frame %</strong></span></span></p></td>
<td><p><span data-ttu-id="1034c-288">不可</span><span class="sxs-lookup"><span data-stu-id="1034c-288">No</span></span></p></td>
<td><p><span data-ttu-id="1034c-p128">"フリーズ" フレームのパーセンテージ。フリーズ フレームでは、通話の音声部分が続いていてもビデオの進行が停止します。</span><span class="sxs-lookup"><span data-stu-id="1034c-p128">Percentage of “frozen” frames. In a frozen frame, the video stops advancing while the audio portion of the call continues.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1034c-291"><strong>[送信フレーム率 (平均)]</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-291"><strong>Outbound avg frame rate</strong></span></span></p></td>
<td><p><span data-ttu-id="1034c-292">不可</span><span class="sxs-lookup"><span data-stu-id="1034c-292">No</span></span></p></td>
<td><p><span data-ttu-id="1034c-293">通話時の送信の平均フレーム レート。</span><span class="sxs-lookup"><span data-stu-id="1034c-293">Average frame rate for outbound transmissions during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1034c-294"><strong>[着信フレーム率 (平均)]</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-294"><strong>Inbound avg frame rate</strong></span></span></p></td>
<td><p><span data-ttu-id="1034c-295">不可</span><span class="sxs-lookup"><span data-stu-id="1034c-295">No</span></span></p></td>
<td><p><span data-ttu-id="1034c-296">通話時の受信の平均フレーム レート。</span><span class="sxs-lookup"><span data-stu-id="1034c-296">Average frame rate for incoming transmissions during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1034c-297"><strong>[着信フレーム率 (低) (%)]</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-297"><strong>Inbound low frame rate %</strong></span></span></p></td>
<td><p><span data-ttu-id="1034c-298">不可</span><span class="sxs-lookup"><span data-stu-id="1034c-298">No</span></span></p></td>
<td><p><span data-ttu-id="1034c-299">着信ビデオのビット レートが低い通話のパーセンテージ。</span><span class="sxs-lookup"><span data-stu-id="1034c-299">Percentage of the call where the bit rate for incoming video was low.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1034c-300"><strong>[クライアントの正常性 (%)]</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-300"><strong>Client health %</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1034c-301">通話時のクライアント デバイスの相対的な正常性を示します。</span><span class="sxs-lookup"><span data-stu-id="1034c-301">Indicates the relative health of the client device during the call.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="server-performance-report-metrics-application-sharing-call-summary"></a><span data-ttu-id="1034c-302">サーバー パフォーマンス レポートの指標: アプリケーション共有の通話の概要</span><span class="sxs-lookup"><span data-stu-id="1034c-302">Server Performance Report Metrics: Application Sharing Call Summary</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1034c-303">名前</span><span class="sxs-lookup"><span data-stu-id="1034c-303">Name</span></span></th>
<th><span data-ttu-id="1034c-304">この項目での並べ替え</span><span class="sxs-lookup"><span data-stu-id="1034c-304">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="1034c-305">説明</span><span class="sxs-lookup"><span data-stu-id="1034c-305">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1034c-306"><strong>[通話の種類/エンドポイントの種類]</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-306"><strong>Call type/Endpoint type</strong></span></span></p></td>
<td><p><span data-ttu-id="1034c-307">不可</span><span class="sxs-lookup"><span data-stu-id="1034c-307">No</span></span></p></td>
<td><p><span data-ttu-id="1034c-p129">この項目をクリックすると、その種類に基づく通話の詳細情報がレポートに表示されます。通話の種類は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="1034c-p129">When you click this item, the report shows detailed information about calls based on that type. Call types include:</span></span></p>
<ul>
<li><p><span data-ttu-id="1034c-310">UC ピアツーピア通話</span><span class="sxs-lookup"><span data-stu-id="1034c-310">UC Peer-to-Peer Calls</span></span></p></li>
<li><p><span data-ttu-id="1034c-311">UC 電話会議セッション</span><span class="sxs-lookup"><span data-stu-id="1034c-311">UC Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="1034c-312">PSTN 電話会議セッション</span><span class="sxs-lookup"><span data-stu-id="1034c-312">PSTN Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="1034c-313">PSTN 通話: メディアのバイパス</span><span class="sxs-lookup"><span data-stu-id="1034c-313">PSTN Calls: Media Bypass</span></span></p></li>
<li><p><span data-ttu-id="1034c-314">PSTN 通話 (非バイパス): UC レグ</span><span class="sxs-lookup"><span data-stu-id="1034c-314">PSTN Calls (Non-Bypass): UC Leg</span></span></p></li>
<li><p><span data-ttu-id="1034c-315">PSTN 通話 (非バイパス): ゲートウェイ レグ</span><span class="sxs-lookup"><span data-stu-id="1034c-315">PSTN Calls (Non-Bypass): Gateway Leg</span></span></p></li>
<li><p><span data-ttu-id="1034c-316">その他の通話の種類</span><span class="sxs-lookup"><span data-stu-id="1034c-316">Other Call Types</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1034c-317"><strong>[通話ボリューム]</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-317"><strong>Call volume</strong></span></span></p></td>
<td><p><span data-ttu-id="1034c-318">不可</span><span class="sxs-lookup"><span data-stu-id="1034c-318">No</span></span></p></td>
<td><p><span data-ttu-id="1034c-319">通話の種類あたりの通話の総数。</span><span class="sxs-lookup"><span data-stu-id="1034c-319">Total number of calls per call type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1034c-320"><strong>[低品質通話のパーセンテージ]</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-320"><strong>Poor call percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="1034c-321">不可</span><span class="sxs-lookup"><span data-stu-id="1034c-321">No</span></span></p></td>
<td><p><span data-ttu-id="1034c-p130">低品質として分類される通話の総数。低品質通話とは、少なくとも 1 つの測定指標が許容値を超えている通話 (たとえば、過剰なジッターが発生した通話) のことです。</span><span class="sxs-lookup"><span data-stu-id="1034c-p130">Total number of calls classified as poor. A poor call is any call which at least one of the measured metrics exceeded the allowed value (for example, a call that experienced excessive jitter).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1034c-324"><strong>[通話ボリューム (ワイヤレス通話)]</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-324"><strong>Call volume (wireless call)</strong></span></span></p></td>
<td><p><span data-ttu-id="1034c-325">不可</span><span class="sxs-lookup"><span data-stu-id="1034c-325">No</span></span></p></td>
<td><p><span data-ttu-id="1034c-326">ワイヤレス接続を使用した通話の数。</span><span class="sxs-lookup"><span data-stu-id="1034c-326">Total number of calls that used a wireless connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1034c-327"><strong>[通話ボリューム (VPN 通話)]</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-327"><strong>Call volume (VPN call)</strong></span></span></p></td>
<td><p><span data-ttu-id="1034c-328">不可</span><span class="sxs-lookup"><span data-stu-id="1034c-328">No</span></span></p></td>
<td><p><span data-ttu-id="1034c-329">VPN 接続を使用した通話の数。</span><span class="sxs-lookup"><span data-stu-id="1034c-329">Total number of calls that used a VPN connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1034c-330"><strong>[通話ボリューム (外部通話)]</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-330"><strong>Call volume (external call)</strong></span></span></p></td>
<td><p><span data-ttu-id="1034c-331">不可</span><span class="sxs-lookup"><span data-stu-id="1034c-331">No</span></span></p></td>
<td><p><span data-ttu-id="1034c-332">外部接続 (つまり、内部ネットワークの外側の接続) を使用した通話の数。</span><span class="sxs-lookup"><span data-stu-id="1034c-332">Number of calls that used an external connection (that is, a connection outside the internal network).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1034c-333"><strong>[ジッター (ミリ秒)]</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-333"><strong>Jitter (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="1034c-334">不可</span><span class="sxs-lookup"><span data-stu-id="1034c-334">No</span></span></p></td>
<td><p><span data-ttu-id="1034c-335">RTP パケットの着信間に検出された平均ジッター (ジッターとは、通話の "揺れ" の測定値です)。</span><span class="sxs-lookup"><span data-stu-id="1034c-335">Average jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="1034c-336">(ジッタは、 &quot; 通話の shakiness の尺度です &quot; )。通常、高ジッターの値は、輻輳または過負荷のメディアサーバーによって発生し、音声が歪むか、失われる原因となります。</span><span class="sxs-lookup"><span data-stu-id="1034c-336">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1034c-337"><strong>[平均相対的一方向]</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-337"><strong>Avg. relative one way</strong></span></span></p></td>
<td><p><span data-ttu-id="1034c-338">不可</span><span class="sxs-lookup"><span data-stu-id="1034c-338">No</span></span></p></td>
<td><p><span data-ttu-id="1034c-p132">2 つのメディア エンドポイント間の相対的な一方向の平均遅延。これは 1 ホップの遅延の測定です。</span><span class="sxs-lookup"><span data-stu-id="1034c-p132">Average relative one-way delay between two media endpoints. This is a single-hop latency measure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1034c-341"><strong>[RDP タイル処理の平均待機時間]</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-341"><strong>Avg. RDP tile processing latency</strong></span></span></p></td>
<td><p><span data-ttu-id="1034c-342">不可</span><span class="sxs-lookup"><span data-stu-id="1034c-342">No</span></span></p></td>
<td><p><span data-ttu-id="1034c-p133">表示セッション中の AS 会議サーバーでの RDP タイル処理の平均待機時間。ネットワーク待機時間はこの指標の対象外です。平均値が高いと、表示の際の遅延が大きくなります。過負荷の会議サーバーでは平均遅延が大きくなる場合があります。</span><span class="sxs-lookup"><span data-stu-id="1034c-p133">The average RDP tile processing latency in the AS Conferencing Server over the duration of the viewing session. This metric does not cover network latency. A high average reflects a longer delay in the viewing experience. An overloaded conferencing server may experience higher average delays.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1034c-347"><strong>[損失した合計タイル %]</strong></span><span class="sxs-lookup"><span data-stu-id="1034c-347"><strong>Total spoiled tile %</strong></span></span></p></td>
<td><p><span data-ttu-id="1034c-348">不可</span><span class="sxs-lookup"><span data-stu-id="1034c-348">No</span></span></p></td>
<td><p><span data-ttu-id="1034c-349">損失した RDP タイルのパーセンテージ。</span><span class="sxs-lookup"><span data-stu-id="1034c-349">Total percentage of spoiled RDP tiles.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="1034c-350">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1034c-350">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

