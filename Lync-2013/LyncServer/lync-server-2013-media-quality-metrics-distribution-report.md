---
title: 'Lync Server 2013: メディア品質指標配布レポート'
description: 'Lync Server 2013: メディア品質指標の配布レポート。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Media Quality Metrics Distribution Report
ms:assetid: d07996e6-b0a5-4ff8-9512-ab707762b4e2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205262(v=OCS.15)
ms:contentKeyID: 48185409
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: def56580477dadf989268e1fc24fcec7776c00d8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399693"
---
# <a name="the-media-quality-metrics-distribution-report-in-lync-server-2013"></a><span data-ttu-id="e511a-103">Lync Server 2013 でのメディア品質指標の配布レポート</span><span class="sxs-lookup"><span data-stu-id="e511a-103">The Media Quality Metrics Distribution Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e511a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e511a-104">

<span> </span></span></span>

<span data-ttu-id="e511a-105">_**最終更新日:** 2012-06-06_</span><span class="sxs-lookup"><span data-stu-id="e511a-105">_**Topic Last Modified:** 2012-06-06_</span></span>

<span data-ttu-id="e511a-p101">メディア品質メトリック分布レポートでは、ジッターやパケット損失などの QoE (Quality of Experience) 指標の分布値を示すグラフを確認することができます。たとえば、ユーザーが合計で 10 回の通話を行い、この 10 回の通話から以下のようなラウンドトリップ時間が報告されたとします。</span><span class="sxs-lookup"><span data-stu-id="e511a-p101">The Media Quality Metrics Distribution Report enables you to see a graph that shows the distribution values for a Quality of Experience metric such as jitter or packet loss. For example, suppose your users make a total of 10 phone calls; those 10 calls report the following roundtrip times:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e511a-108">通話番号</span><span class="sxs-lookup"><span data-stu-id="e511a-108">Call Number</span></span></th>
<th><span data-ttu-id="e511a-109">往復時間 (ミリ秒)</span><span class="sxs-lookup"><span data-stu-id="e511a-109">Roundtrip Time (milliseconds)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e511a-110">1</span><span class="sxs-lookup"><span data-stu-id="e511a-110">1</span></span></p></td>
<td><p><span data-ttu-id="e511a-111">50</span><span class="sxs-lookup"><span data-stu-id="e511a-111">50</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e511a-112">2</span><span class="sxs-lookup"><span data-stu-id="e511a-112">2</span></span></p></td>
<td><p><span data-ttu-id="e511a-113">50</span><span class="sxs-lookup"><span data-stu-id="e511a-113">50</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e511a-114">3</span><span class="sxs-lookup"><span data-stu-id="e511a-114">3</span></span></p></td>
<td><p><span data-ttu-id="e511a-115">50</span><span class="sxs-lookup"><span data-stu-id="e511a-115">50</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e511a-116">4</span><span class="sxs-lookup"><span data-stu-id="e511a-116">4</span></span></p></td>
<td><p><span data-ttu-id="e511a-117">50</span><span class="sxs-lookup"><span data-stu-id="e511a-117">50</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e511a-118">5</span><span class="sxs-lookup"><span data-stu-id="e511a-118">5</span></span></p></td>
<td><p><span data-ttu-id="e511a-119">50</span><span class="sxs-lookup"><span data-stu-id="e511a-119">50</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e511a-120">6</span><span class="sxs-lookup"><span data-stu-id="e511a-120">6</span></span></p></td>
<td><p><span data-ttu-id="e511a-121">50</span><span class="sxs-lookup"><span data-stu-id="e511a-121">50</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e511a-122">7</span><span class="sxs-lookup"><span data-stu-id="e511a-122">7</span></span></p></td>
<td><p><span data-ttu-id="e511a-123">50</span><span class="sxs-lookup"><span data-stu-id="e511a-123">50</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e511a-124">個</span><span class="sxs-lookup"><span data-stu-id="e511a-124">8</span></span></p></td>
<td><p><span data-ttu-id="e511a-125">4550</span><span class="sxs-lookup"><span data-stu-id="e511a-125">4550</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e511a-126">ファイブ</span><span class="sxs-lookup"><span data-stu-id="e511a-126">9</span></span></p></td>
<td><p><span data-ttu-id="e511a-127">50</span><span class="sxs-lookup"><span data-stu-id="e511a-127">50</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e511a-128">常用</span><span class="sxs-lookup"><span data-stu-id="e511a-128">10</span></span></p></td>
<td><p><span data-ttu-id="e511a-129">50</span><span class="sxs-lookup"><span data-stu-id="e511a-129">50</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e511a-130">これらのラウンドトリップ時間の平均は500ミリ秒 (5000 は10で割る) です。</span><span class="sxs-lookup"><span data-stu-id="e511a-130">The average for those roundtrip times is 500 milliseconds (5000 divided by 10).</span></span> <span data-ttu-id="e511a-131">500ミリ秒は非常に大きなラウンドトリップ時間です。その結果、ネットワークの輻輳に対して重大な問題が発生したと判断される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e511a-131">Five hundred milliseconds is an extremely large roundtrip time; as a result, you might believe that you have a serious problem with network congestion.</span></span> <span data-ttu-id="e511a-132">(ラウンドトリップ時間が長い場合は、通常、ネットワークの過負荷が発生します)。</span><span class="sxs-lookup"><span data-stu-id="e511a-132">(Long roundtrip times are typically the result of overloaded networks.)</span></span>

<span data-ttu-id="e511a-133">実際には、通話の90% は、非常に優れた往復時間でした。結果全体に対して1つの不正な通話があっただけです。</span><span class="sxs-lookup"><span data-stu-id="e511a-133">In reality, of course, 90% of your calls had excellent round trip times; you merely had one bad call that skewed the overall results.</span></span> <span data-ttu-id="e511a-134">平均ラウンドトリップ時間のみを表示する場合は、問題が発生する可能性が高くなります。</span><span class="sxs-lookup"><span data-stu-id="e511a-134">If you only look at the average roundtrip time you might jump to a very wrong conclusion.</span></span>

<span data-ttu-id="e511a-p104">メディア品質メトリック分布レポートでは、特定の指標 (ラウンドトリップ時間など) の分布をグラフィカルに表示することによって誤った結論に至るのを防ぎます。このようなグラフでは、9 回の通話はとても良好で、1 回の通話だけが良くなかったという事実がはっきりとわかります。当然ながら、その 1 回の通話についてはさらなる調査が必要ですが、10 回のうち 9 回がとても良好だったという結果は、少なくとも現時点では、ネットワークを大きく変更する理由はないことを示唆しています。</span><span class="sxs-lookup"><span data-stu-id="e511a-p104">The Media Quality Metrics Distribution Report helps you avoid jumping to wrong conclusions by showing you a graphical distribution of a specified metric (such as round trip time). These graphs can help make it clear that you had nine very good calls and one very bad call. Admittedly, you might still want to further investigate that one call; however, the fact that 9 out of the 10 calls were very good suggests that there is no reason to make any drastic changes to your network, at least not at this point in time.</span></span>

<div>

## <a name="filters"></a><span data-ttu-id="e511a-138">フィルター</span><span class="sxs-lookup"><span data-stu-id="e511a-138">Filters</span></span>

<span data-ttu-id="e511a-p105">フィルターは、細かく絞り込んだデータ セットを返したり、返されたデータをさまざまな方法で表示したりする方法として利用できます。次の表に、メディア品質メトリック分布レポートで使用できるフィルターを示します。</span><span class="sxs-lookup"><span data-stu-id="e511a-p105">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. The following table lists the filters that you can use with the Media Quality Metrics Distribution Report.</span></span>

### <a name="media-quality-metrics-distribution-report-filters"></a><span data-ttu-id="e511a-141">メディア品質メトリック分布レポートのフィルター</span><span class="sxs-lookup"><span data-stu-id="e511a-141">Media Quality Metrics Distribution Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e511a-142">名前</span><span class="sxs-lookup"><span data-stu-id="e511a-142">Name</span></span></th>
<th><span data-ttu-id="e511a-143">説明</span><span class="sxs-lookup"><span data-stu-id="e511a-143">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e511a-144"><strong>開始</strong></span><span class="sxs-lookup"><span data-stu-id="e511a-144"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="e511a-p106">時間範囲の開始日と開始時刻。データを時間単位で表示するには、次のように開始日と開始時刻の両方を入力します。</span><span class="sxs-lookup"><span data-stu-id="e511a-p106">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="e511a-147">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="e511a-147">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="e511a-p107">開始時刻を入力しないと、レポートは自動的に指定日の午前 12:00 に開始します。データを日単位で表示するには、次のように日付のみを入力します。</span><span class="sxs-lookup"><span data-stu-id="e511a-p107">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="e511a-150">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="e511a-150">7/7/2012</span></span></p>
<p><span data-ttu-id="e511a-151">週単位または月単位で表示するには、表示する週または月の任意の日付を入力します (その週または月の最初の日である必要はありません)。</span><span class="sxs-lookup"><span data-stu-id="e511a-151">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="e511a-152">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="e511a-152">7/3/2012</span></span></p>
<p><span data-ttu-id="e511a-153">一週間は、日曜日から始まり、土曜日で終わるものとします。</span><span class="sxs-lookup"><span data-stu-id="e511a-153">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e511a-154"><strong>終了</strong></span><span class="sxs-lookup"><span data-stu-id="e511a-154"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="e511a-p108">時間範囲の終了日と終了時刻。データを時間単位で表示するには、次のように終了日と終了時刻の両方を入力します。</span><span class="sxs-lookup"><span data-stu-id="e511a-p108">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="e511a-157">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="e511a-157">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="e511a-p109">終了時刻を入力しないと、レポートは自動的に指定日の午前 12:00 に終了します。データを日単位で表示するには、次のように日付のみを入力します。</span><span class="sxs-lookup"><span data-stu-id="e511a-p109">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="e511a-160">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="e511a-160">7/7/2012</span></span></p>
<p><span data-ttu-id="e511a-161">週単位または月単位で表示するには、表示する週または月の任意の日付を入力します (その週または月の最初の日である必要はありません)。</span><span class="sxs-lookup"><span data-stu-id="e511a-161">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="e511a-162">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="e511a-162">7/3/2012</span></span></p>
<p><span data-ttu-id="e511a-163">一週間は、日曜日から始まり、土曜日で終わるものとします。</span><span class="sxs-lookup"><span data-stu-id="e511a-163">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e511a-164"><strong>x 軸の最小値</strong></span><span class="sxs-lookup"><span data-stu-id="e511a-164"><strong>Minimum in x axis</strong></span></span></p></td>
<td><p><span data-ttu-id="e511a-165">グラフの X 軸に表示される最小の値。</span><span class="sxs-lookup"><span data-stu-id="e511a-165">Lowest value to be displayed on the X axis of the graph.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e511a-166"><strong>x 軸の最大値</strong></span><span class="sxs-lookup"><span data-stu-id="e511a-166"><strong>Maximum in x axis</strong></span></span></p></td>
<td><p><span data-ttu-id="e511a-167">グラフの X 軸に表示される最大の値。</span><span class="sxs-lookup"><span data-stu-id="e511a-167">Highest value to be displayed on the X axis of the graph.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e511a-168"><strong>アクセスの種類</strong></span><span class="sxs-lookup"><span data-stu-id="e511a-168"><strong>Access type</strong></span></span></p></td>
<td><p><span data-ttu-id="e511a-p110">クライアントが通話時に内部ネットワークにログオンしたか、外部ネットワークにログオンしたかを示します。次のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="e511a-p110">Indicates whether the client was logged on to the internal network or the external network when the call was placed. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="e511a-171">[すべて]</span><span class="sxs-lookup"><span data-stu-id="e511a-171">[All]</span></span></p></li>
<li><p><span data-ttu-id="e511a-172">内部</span><span class="sxs-lookup"><span data-stu-id="e511a-172">Internal</span></span></p></li>
<li><p><span data-ttu-id="e511a-173">外部</span><span class="sxs-lookup"><span data-stu-id="e511a-173">External</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e511a-174"><strong>VPN</strong></span><span class="sxs-lookup"><span data-stu-id="e511a-174"><strong>VPN</strong></span></span></p></td>
<td><p><span data-ttu-id="e511a-p111">通話時に外部クライアントが仮想プライベート ネットワーク (VPN) 接続を使用したかどうかを示します。次のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="e511a-p111">Indicates whether an external client was using a virtual private network (VPN) connection when the call was placed. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="e511a-177">[すべて]</span><span class="sxs-lookup"><span data-stu-id="e511a-177">[All]</span></span></p></li>
<li><p><span data-ttu-id="e511a-178">VPN</span><span class="sxs-lookup"><span data-stu-id="e511a-178">VPN</span></span></p></li>
<li><p><span data-ttu-id="e511a-179">非 VPN</span><span class="sxs-lookup"><span data-stu-id="e511a-179">Non-VPN</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e511a-180"><strong>ネットワークの種類</strong></span><span class="sxs-lookup"><span data-stu-id="e511a-180"><strong>Network type</strong></span></span></p></td>
<td><p><span data-ttu-id="e511a-p112">通話時にクライアントが接続したネットワークの種類を示します。次のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="e511a-p112">Indicates the type of network the client was connected to when the call was placed. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="e511a-183">[すべて]</span><span class="sxs-lookup"><span data-stu-id="e511a-183">[All]</span></span></p></li>
<li><p><span data-ttu-id="e511a-184">有線</span><span class="sxs-lookup"><span data-stu-id="e511a-184">Wired</span></span></p></li>
<li><p><span data-ttu-id="e511a-185">ワイヤレス</span><span class="sxs-lookup"><span data-stu-id="e511a-185">Wireless</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="e511a-186">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e511a-186">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

