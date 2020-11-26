---
title: 'Lync Server 2013: メディア品質サマリーレポート'
description: 'Lync Server 2013: メディア品質サマリーレポート。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Media Quality Summary Report
ms:assetid: 8bd59ad6-3087-49c8-b692-5573fe2ffcd8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615012(v=OCS.15)
ms:contentKeyID: 48184776
ms.date: 06/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2616b7e3cdea9df7b004745a5c407188870903c7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446046"
---
# <a name="media-quality-summary-report-in-lync-server-2013"></a><span data-ttu-id="d2170-103">Lync Server 2013 のメディア品質サマリーレポート</span><span class="sxs-lookup"><span data-stu-id="d2170-103">Media Quality Summary Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d2170-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d2170-104">

<span> </span></span></span>

<span data-ttu-id="d2170-105">_**最終更新日:** 2016-06-29_</span><span class="sxs-lookup"><span data-stu-id="d2170-105">_**Topic Last Modified:** 2016-06-29_</span></span>

<span data-ttu-id="d2170-106">メディア品質概要レポートは、組織での通話の品質を解析するのに最良の方法です。このレポートは、次のカテゴリに分類された詳細な QoE (Quality of Experience) 通話指標を提供します。</span><span class="sxs-lookup"><span data-stu-id="d2170-106">The Media Quality Summary Report is perhaps your best bet for analyzing call quality in your organization: this report provides detailed Quality of Experience (QoE) call metrics broken down into the following categories:</span></span>

  - <span data-ttu-id="d2170-107">UC ピアツーピア通話 (Microsoft lync 2013 から Microsoft Lync 2013 通話)</span><span class="sxs-lookup"><span data-stu-id="d2170-107">UC Peer to Peer Calls (such as a Microsoft Lync 2013 to Microsoft Lync 2013 call)</span></span>

  - <span data-ttu-id="d2170-108">UC 電話会議セッション</span><span class="sxs-lookup"><span data-stu-id="d2170-108">UC Conference Sessions</span></span>

  - <span data-ttu-id="d2170-109">PSTN 電話会議セッション</span><span class="sxs-lookup"><span data-stu-id="d2170-109">PSTN Conference Sessions</span></span>

  - <span data-ttu-id="d2170-110">PSTN 通話: メディアのバイパス</span><span class="sxs-lookup"><span data-stu-id="d2170-110">PSTN Calls: Media Bypass</span></span>

  - <span data-ttu-id="d2170-111">PSTN 通話 (非バイパス): UC レグ</span><span class="sxs-lookup"><span data-stu-id="d2170-111">PSTN Calls (Non-Bypass): UC Leg</span></span>

  - <span data-ttu-id="d2170-112">PSTN 通話 (非バイパス): ゲートウェイ レグ</span><span class="sxs-lookup"><span data-stu-id="d2170-112">PSTN Calls (Non-Bypass): Gateway Leg</span></span>

  - <span data-ttu-id="d2170-113">その他の通話の種類</span><span class="sxs-lookup"><span data-stu-id="d2170-113">Other Call Types</span></span>

<span data-ttu-id="d2170-114">レポートを初めて開いたとき、これらの各カテゴリの概要情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d2170-114">When you first open the report, you see summary information for each of these categories.</span></span> <span data-ttu-id="d2170-115">レポートを離れることなく、各カテゴリを展開して、Office Communicator 2007 R2 から Lync 2013 への通話などのサブカテゴリを表示できます。</span><span class="sxs-lookup"><span data-stu-id="d2170-115">Without leaving the report, you can expand each category to look at subcategories such as calls made from Office Communicator 2007 R2 to Lync 2013.</span></span> <span data-ttu-id="d2170-116">また、これらのサブカテゴリにドリルダウンして、そのサブカテゴリ内の発信された各通話の詳細を表示できます。</span><span class="sxs-lookup"><span data-stu-id="d2170-116">In turn, you can then drill down into these subcategories to see details about each call made within that subcategory.</span></span>

<span data-ttu-id="d2170-117">Microsoft Lync Server 2013 の [メディア品質の概要] レポートでは、データが、音声通話、ビデオ通話、アプリケーション共有通話の3種類に分割されます。</span><span class="sxs-lookup"><span data-stu-id="d2170-117">In Microsoft Lync Server 2013 the Media Quality Summary Report further breaks the data down into three call types: audio calls, video calls, and application sharing calls.</span></span> <span data-ttu-id="d2170-118">通話の各種類について、独自のセクションがレポート内に設けられ、通話指標の独自のカスタム セットが用意されています。</span><span class="sxs-lookup"><span data-stu-id="d2170-118">Each call type has its own section in the report, and its own custom set of call metrics.</span></span>

<span data-ttu-id="d2170-119">メディア品質概要レポートでは、有線通話とワイヤレス通話、内部通話と外部通話、VPN 通話と非 VPN 通話を比較できるフィルターも適用できます。</span><span class="sxs-lookup"><span data-stu-id="d2170-119">The Media Quality Summary Report also allows you to apply filters that enable you to compare the call quality of wired calls vs. wireless calls, internal calls vs. external calls, and VPN calls vs. non-VPN calls.</span></span>

<div>

## <a name="accessing-the-media-quality-summary-report"></a><span data-ttu-id="d2170-120">メディア品質概要レポートへのアクセス</span><span class="sxs-lookup"><span data-stu-id="d2170-120">Accessing the Media Quality Summary Report</span></span>

<span data-ttu-id="d2170-121">メディア品質概要レポートには、監視レポートのホームページからアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="d2170-121">The Media Quality Summary Report is accessed from the Monitoring Reports home page.</span></span> <span data-ttu-id="d2170-122">次の指標のいずれかをクリックして、 [Lync Server 2013 の通話リストレポート](lync-server-2013-call-list-report.md) にドリルダウンすることができます。</span><span class="sxs-lookup"><span data-stu-id="d2170-122">You can drill down to the [Call List Report in Lync Server 2013](lync-server-2013-call-list-report.md) by clicking either of the following metrics:</span></span>

  - <span data-ttu-id="d2170-123">通話ボリューム</span><span class="sxs-lookup"><span data-stu-id="d2170-123">Call volume</span></span>

  - <span data-ttu-id="d2170-124">低品質通話のパーセンテージ</span><span class="sxs-lookup"><span data-stu-id="d2170-124">Poor call percentage</span></span>

<span data-ttu-id="d2170-125">また、次のいずれかの音声通話指標をクリックして、メディア品質メトリック分布レポートにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="d2170-125">In addition, you can access the Media Quality Metrics Distribution Report by clicking any of the following audio call metrics:</span></span>

  - <span data-ttu-id="d2170-126">往復 (ミリ秒)</span><span class="sxs-lookup"><span data-stu-id="d2170-126">Round trip (ms)</span></span>

  - <span data-ttu-id="d2170-127">低下 (MOS)</span><span class="sxs-lookup"><span data-stu-id="d2170-127">Degradation (MOS)</span></span>

  - <span data-ttu-id="d2170-128">パケット損失</span><span class="sxs-lookup"><span data-stu-id="d2170-128">Packet loss</span></span>

  - <span data-ttu-id="d2170-129">ジッター (ミリ秒)</span><span class="sxs-lookup"><span data-stu-id="d2170-129">Jitter (ms)</span></span>

  - <span data-ttu-id="d2170-130">ヒーラー隠し比率</span><span class="sxs-lookup"><span data-stu-id="d2170-130">Healer concealed ratio</span></span>

  - <span data-ttu-id="d2170-131">ヒーラー引き伸ばし比率</span><span class="sxs-lookup"><span data-stu-id="d2170-131">Healer stretched ratio</span></span>

  - <span data-ttu-id="d2170-132">ヒーラー圧縮比率</span><span class="sxs-lookup"><span data-stu-id="d2170-132">Healer compressed ratio</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="d2170-133">フィルター</span><span class="sxs-lookup"><span data-stu-id="d2170-133">Filters</span></span>

<span data-ttu-id="d2170-p104">フィルターは、細かく絞り込んだデータ セットを返したり、返されたデータをさまざまな方法で表示したりする方法として利用できます。たとえば、メディア品質概要レポートでは、返されたデータをアクセスの種類 (内部アクセス、外部アクセスなど) や有線/ワイヤレス ネットワーク接続でフィルターできます。また、データをグループ化する方法を選択することもできます。この場合は、通話が、時間、日、週、または月を基準にグループ化されています。</span><span class="sxs-lookup"><span data-stu-id="d2170-p104">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Media Quality Summary Report enables you to filter the returned data by such things as access type (that is, interval access vs. external access) or by wired/wireless network connection. You can also choose how data should be grouped. In this case, calls are grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="d2170-138">次の表に、メディア品質概要レポートで使用できるフィルターを示します。</span><span class="sxs-lookup"><span data-stu-id="d2170-138">The following table lists the filters that you can use with the Media Quality Summary Report.</span></span>

### <a name="media-quality-summary-report-filters"></a><span data-ttu-id="d2170-139">メディア品質概要レポートのフィルター</span><span class="sxs-lookup"><span data-stu-id="d2170-139">Media Quality Summary Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d2170-140">名前</span><span class="sxs-lookup"><span data-stu-id="d2170-140">Name</span></span></th>
<th><span data-ttu-id="d2170-141">説明</span><span class="sxs-lookup"><span data-stu-id="d2170-141">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d2170-142"><strong>開始</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-142"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-p105">時間範囲の開始日と開始時刻。データを時間単位で表示するには、次のように開始日と開始時刻の両方を入力します。</span><span class="sxs-lookup"><span data-stu-id="d2170-p105">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="d2170-145">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="d2170-145">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="d2170-p106">開始時刻を入力しないと、レポートは自動的に指定日の午前 12:00 に開始します。データを日単位で表示するには、次のように日付のみを入力します。</span><span class="sxs-lookup"><span data-stu-id="d2170-p106">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="d2170-148">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="d2170-148">7/7/2012</span></span></p>
<p><span data-ttu-id="d2170-149">週単位または月単位で表示するには、表示する週または月の任意の日付を入力します (その週または月の最初の日である必要はありません)。</span><span class="sxs-lookup"><span data-stu-id="d2170-149">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="d2170-150">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="d2170-150">7/3/2012</span></span></p>
<p><span data-ttu-id="d2170-151">一週間は、日曜日から始まり、土曜日で終わるものとします。</span><span class="sxs-lookup"><span data-stu-id="d2170-151">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2170-152"><strong>終了</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-152"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-p107">時間範囲の終了日と終了時刻。データを時間単位で表示するには、次のように終了日と終了時刻の両方を入力します。</span><span class="sxs-lookup"><span data-stu-id="d2170-p107">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="d2170-155">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="d2170-155">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="d2170-p108">終了時刻を入力しないと、レポートは自動的に指定日の午前 12:00 に終了します。データを日単位で表示するには、次のように日付のみを入力します。</span><span class="sxs-lookup"><span data-stu-id="d2170-p108">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="d2170-158">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="d2170-158">7/7/2012</span></span></p>
<p><span data-ttu-id="d2170-159">週単位または月単位で表示するには、表示する週または月の任意の日付を入力します (その週または月の最初の日である必要はありません)。</span><span class="sxs-lookup"><span data-stu-id="d2170-159">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="d2170-160">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="d2170-160">7/3/2012</span></span></p>
<p><span data-ttu-id="d2170-161">一週間は、日曜日から始まり、土曜日で終わるものとします。</span><span class="sxs-lookup"><span data-stu-id="d2170-161">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2170-162"><strong>[アクセスの種類]</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-162"><strong>Access type</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-p109">クライアントが通話時に内部ネットワークにログオンしたか、外部ネットワークにログオンしたかを示します。次のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="d2170-p109">Indicates whether the client was logged on to the internal network or the external network when the call was placed. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="d2170-165">[すべて]</span><span class="sxs-lookup"><span data-stu-id="d2170-165">[All]</span></span></p></li>
<li><p><span data-ttu-id="d2170-166">内部</span><span class="sxs-lookup"><span data-stu-id="d2170-166">Internal</span></span></p></li>
<li><p><span data-ttu-id="d2170-167">外部</span><span class="sxs-lookup"><span data-stu-id="d2170-167">External</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2170-168"><strong>[ネットワークの種類]</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-168"><strong>Network type</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-p110">通話時にクライアントが接続したネットワークの種類を示します。次のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="d2170-p110">Indicates the type of network the client was connected to when the call was placed. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="d2170-171">[すべて]</span><span class="sxs-lookup"><span data-stu-id="d2170-171">[All]</span></span></p></li>
<li><p><span data-ttu-id="d2170-172">有線</span><span class="sxs-lookup"><span data-stu-id="d2170-172">Wired</span></span></p></li>
<li><p><span data-ttu-id="d2170-173">ワイヤレス</span><span class="sxs-lookup"><span data-stu-id="d2170-173">Wireless</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2170-174"><strong>VPN</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-174"><strong>VPN</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-p111">通話時に外部クライアントが仮想プライベート ネットワーク (VPN) 接続を使用したかどうかを示します。次のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="d2170-p111">Indicates whether an external client was using a virtual private network (VPN) connection when the call was placed. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="d2170-177">[すべて]</span><span class="sxs-lookup"><span data-stu-id="d2170-177">[All]</span></span></p></li>
<li><p><span data-ttu-id="d2170-178">VPN</span><span class="sxs-lookup"><span data-stu-id="d2170-178">VPN</span></span></p></li>
<li><p><span data-ttu-id="d2170-179">非 VPN</span><span class="sxs-lookup"><span data-stu-id="d2170-179">Non-VPN</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="d2170-180">指標</span><span class="sxs-lookup"><span data-stu-id="d2170-180">Metrics</span></span>

<span data-ttu-id="d2170-181">次の表に、メディア品質概要レポートで提供される情報を示します。</span><span class="sxs-lookup"><span data-stu-id="d2170-181">The following table lists the information provided in the Media Quality Summary Report.</span></span>

### <a name="media-quality-summary-report-metrics-audio-call-summary"></a><span data-ttu-id="d2170-182">メディア品質概要レポートの指標: 音声通話の概要</span><span class="sxs-lookup"><span data-stu-id="d2170-182">Media Quality Summary Report Metrics: Audio Call Summary</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d2170-183">名前</span><span class="sxs-lookup"><span data-stu-id="d2170-183">Name</span></span></th>
<th><span data-ttu-id="d2170-184">この項目での並べ替え</span><span class="sxs-lookup"><span data-stu-id="d2170-184">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="d2170-185">説明</span><span class="sxs-lookup"><span data-stu-id="d2170-185">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d2170-186"><strong>[通話の種類/エンドポイントの種類]</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-186"><strong>Call type/Endpoint type</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-187">不可</span><span class="sxs-lookup"><span data-stu-id="d2170-187">No</span></span></p></td>
<td><p><span data-ttu-id="d2170-p112">この項目をクリックすると、その種類に基づく通話の詳細情報がレポートに表示されます。通話の種類は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="d2170-p112">When you click this item, the report shows detailed information about calls based on that type. Call types include:</span></span></p>
<ul>
<li><p><span data-ttu-id="d2170-190">UC ピアツーピア通話</span><span class="sxs-lookup"><span data-stu-id="d2170-190">UC Peer-to-Peer Calls</span></span></p></li>
<li><p><span data-ttu-id="d2170-191">UC 電話会議セッション</span><span class="sxs-lookup"><span data-stu-id="d2170-191">UC Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="d2170-192">PSTN 電話会議セッション</span><span class="sxs-lookup"><span data-stu-id="d2170-192">PSTN Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="d2170-193">PSTN 通話: メディアのバイパス</span><span class="sxs-lookup"><span data-stu-id="d2170-193">PSTN Calls: Media Bypass</span></span></p></li>
<li><p><span data-ttu-id="d2170-194">PSTN 通話 (非バイパス): UC レグ</span><span class="sxs-lookup"><span data-stu-id="d2170-194">PSTN Calls (Non-Bypass): UC Leg</span></span></p></li>
<li><p><span data-ttu-id="d2170-195">PSTN 通話 (非バイパス): ゲートウェイ レグ</span><span class="sxs-lookup"><span data-stu-id="d2170-195">PSTN Calls (Non-Bypass): Gateway Leg</span></span></p></li>
<li><p><span data-ttu-id="d2170-196">その他の通話の種類</span><span class="sxs-lookup"><span data-stu-id="d2170-196">Other Call Types</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2170-197"><strong>[通話ボリューム]</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-197"><strong>Call volume</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-198">不可</span><span class="sxs-lookup"><span data-stu-id="d2170-198">No</span></span></p></td>
<td><p><span data-ttu-id="d2170-199">通話の種類あたりの通話の総数。</span><span class="sxs-lookup"><span data-stu-id="d2170-199">Total number of calls per call type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2170-200"><strong>[低品質通話のパーセンテージ]</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-200"><strong>Poor call percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-201">不可</span><span class="sxs-lookup"><span data-stu-id="d2170-201">No</span></span></p></td>
<td><p><span data-ttu-id="d2170-p113">低品質として分類される通話の総数。低品質通話とは、少なくとも 1 つの測定指標が許容値を超えている通話 (たとえば、過剰なジッターが発生した通話) のことです。</span><span class="sxs-lookup"><span data-stu-id="d2170-p113">Total number of calls classified as poor. A poor call is any call which at least one of the measured metrics exceeded the allowed value (for example, a call that experienced excessive jitter).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2170-204"><strong>[通話ボリューム (ワイヤレス通話)]</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-204"><strong>Call volume (wireless call)</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-205">不可</span><span class="sxs-lookup"><span data-stu-id="d2170-205">No</span></span></p></td>
<td><p><span data-ttu-id="d2170-206">ワイヤレス接続を使用した通話の数。</span><span class="sxs-lookup"><span data-stu-id="d2170-206">Total number of calls that used a wireless connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2170-207"><strong>[通話ボリューム (VPN 通話)]</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-207"><strong>Call volume (VPN call)</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-208">不可</span><span class="sxs-lookup"><span data-stu-id="d2170-208">No</span></span></p></td>
<td><p><span data-ttu-id="d2170-209">VPN 接続を使用した通話の数。</span><span class="sxs-lookup"><span data-stu-id="d2170-209">Total number of calls that used a VPN connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2170-210"><strong>[通話ボリューム (外部通話)]</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-210"><strong>Call volume (external call)</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-211">不可</span><span class="sxs-lookup"><span data-stu-id="d2170-211">No</span></span></p></td>
<td><p><span data-ttu-id="d2170-212">外部接続 (つまり、内部ネットワークの外側の接続) を使用した通話の数。</span><span class="sxs-lookup"><span data-stu-id="d2170-212">Number of calls that used an external connection (that is, a connection outside the internal network).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2170-213"><strong>[往復 (ミリ秒)]</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-213"><strong>Round trip (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-214">不可</span><span class="sxs-lookup"><span data-stu-id="d2170-214">No</span></span></p></td>
<td><p><span data-ttu-id="d2170-p114">リアルタイム転送プロトコル (RTP) パケットが別のエンドポイントとの間を往復するのに要する平均時間 (ミリ秒単位)。100 ミリ秒以下の往復時間が許容できる品質と見なされます。</span><span class="sxs-lookup"><span data-stu-id="d2170-p114">Average amount of (in milliseconds) required for a real-time transport protocol (RTP) packet to travel to another endpoint and then back. Round-trip times of 100 milliseconds or less are considered of acceptable quality.</span></span></p>
<p><span data-ttu-id="d2170-p115">この値が高い場合は、国際通話ルーティング、ルーティングの構成ミス、メディア サーバーの過負荷などの原因が考えられます。その結果、双方向のリアルタイムの音声会話が難しくなります。</span><span class="sxs-lookup"><span data-stu-id="d2170-p115">High round-trip values can be caused by international call routing, a routing misconfiguration, or an overloaded media server. High round-trip times result in difficulties with two-way, real-time audio conversations.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2170-219"><strong>低下 (MOS)</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-219"><strong>Degradation (MOS)</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-220">不可</span><span class="sxs-lookup"><span data-stu-id="d2170-220">No</span></span></p></td>
<td><p><span data-ttu-id="d2170-221">通話時に発生した平均オピニオン値 (MOS) 低下の平均値。</span><span class="sxs-lookup"><span data-stu-id="d2170-221">Average amount of mean opinion score (MOS) degradation experienced during a call.</span></span> <span data-ttu-id="d2170-222">低下の値範囲は、最低 0.0 から最高 5.0 までとなります。</span><span class="sxs-lookup"><span data-stu-id="d2170-222">Degradation values can range from a low of 0.0 to a high of 5.0.</span></span> <span data-ttu-id="d2170-223">0.5 以下の値は、許容される低下を表します。</span><span class="sxs-lookup"><span data-stu-id="d2170-223">A value of 0.5 or less represents acceptable degradation.</span></span> <span data-ttu-id="d2170-224">従来、平均オピニオン値は、ユーザーが通話の品質を 1 から 5 の範囲で評価することによって計算されていました。</span><span class="sxs-lookup"><span data-stu-id="d2170-224">Historically, mean options scores were calculated by having users rate the quality of a call on a scale of 1-to-5.</span></span> <span data-ttu-id="d2170-225">Lync server では、Lync Server で一連のアルゴリズムを使って、ユーザーが通話を評価した方法を予測します。</span><span class="sxs-lookup"><span data-stu-id="d2170-225">In Lync Server, Lync Server uses a set of algorithms to predict how users would have rated a call.</span></span></p>
<p><span data-ttu-id="d2170-p117">この値が高い場合は、輻輳、帯域幅の不足、ワイヤレスの輻輳または干渉、メディア サーバーやエンドポイントの過負荷などの原因が考えられます。その結果、音声のひずみや欠落が生じます。</span><span class="sxs-lookup"><span data-stu-id="d2170-p117">High degradation values can be caused by congestion, lack of bandwidth, wireless congestion or interference, or an overloaded media server or endpoint. High degradation results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2170-228"><strong>パケット損失</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-228"><strong>Packet loss</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-229">不可</span><span class="sxs-lookup"><span data-stu-id="d2170-229">No</span></span></p></td>
<td><p><span data-ttu-id="d2170-p118">RTP パケットの平均損失率 (パケット損失は、RTP パケット (音声およびビデオをインターネット上で転送する場合に使用されるプロトコル) が宛先に到達できなかった場合に発生します)。通常、この値が高い場合は、輻輳、帯域幅の不足、ワイヤレスの輻輳または干渉、メディア サーバーの過負荷などの原因が考えられます。その結果、一般に音声のひずみや欠落が生じます。</span><span class="sxs-lookup"><span data-stu-id="d2170-p118">Average rate of RTP packet loss. (Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion, lack of bandwidth, wireless congestion or interference, or an overloaded media server. Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2170-233"><strong>[ジッター (ミリ秒)]</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-233"><strong>Jitter (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-234">不可</span><span class="sxs-lookup"><span data-stu-id="d2170-234">No</span></span></p></td>
<td><p><span data-ttu-id="d2170-235">RTP パケットの着信間に検出された平均ジッター (ジッターとは、通話の "揺れ" の測定値です)。</span><span class="sxs-lookup"><span data-stu-id="d2170-235">Average jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="d2170-236">(ジッタは、 &quot; 通話の shakiness の尺度です &quot; )。通常、高ジッターの値は、輻輳または過負荷のメディアサーバーによって発生し、音声が歪むか、失われる原因となります。</span><span class="sxs-lookup"><span data-stu-id="d2170-236">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2170-237"><strong>ヒーラー隠し比率</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-237"><strong>Healer concealed ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-238">不可</span><span class="sxs-lookup"><span data-stu-id="d2170-238">No</span></span></p></td>
<td><p><span data-ttu-id="d2170-p120">サンプルの合計数に対する隠しオーディオ サンプルの平均比率 (隠しオーディオ サンプルとは、突然遷移を取り除くために使用される手法です。突然遷移は、通常、ネットワーク パケットの削除が原因で発生します)。この値が高い場合は、パケット損失やジッターのために高いレベルで損失の隠蔽が適用されています。その結果、音声のひずみや欠落が生じます。</span><span class="sxs-lookup"><span data-stu-id="d2170-p120">Average ratio of concealed audio samples to the total to the total number of samples. (A concealed audio sample is a technique used to smooth out the abrupt transition that would usually be caused by dropped network packets.) High values indicate significant levels of loss concealment applied caused by packet loss or jitter, and results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2170-241"><strong>ヒーラー引き伸ばし比率</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-241"><strong>Healer stretched ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-242">不可</span><span class="sxs-lookup"><span data-stu-id="d2170-242">No</span></span></p></td>
<td><p><span data-ttu-id="d2170-p121">サンプルの合計数に対する引き伸ばされたオーディオ サンプルの平均比率 (引き伸ばされたオーディオとは、ネットワーク パケットの削除が検出されたときに通話の品質を維持できるように拡張されたオーディオのことです)。この値が高い場合は、ジッターのために高いレベルでサンプルの引き伸ばしが行われています。その結果、音声が機械のように聞こえたりひずんで聞こえたりします。</span><span class="sxs-lookup"><span data-stu-id="d2170-p121">Average ratio of stretched audio samples to the total to the total number of samples. (Stretched audio is audio that has been expanded to help maintain call quality when a dropped network packet has been detected.) High values indicate significant levels of sample stretching caused by jitter, and result in audio sounding robotic or distorted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2170-245"><strong>ヒーラー圧縮比率</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-245"><strong>Healer compressed ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-246">不可</span><span class="sxs-lookup"><span data-stu-id="d2170-246">No</span></span></p></td>
<td><p><span data-ttu-id="d2170-p122">サンプルの合計数に対する圧縮オーディオ サンプルの平均比率 (圧縮オーディオとは、ネットワーク パケットの削除が検出されたときに通話の品質を維持できるように圧縮されたオーディオのことです)。この値が高い場合は、ジッターのために高いレベルでサンプルの圧縮が行われています。その結果、音声が早送りされたように聞こえたりひずんで聞こえたりします。</span><span class="sxs-lookup"><span data-stu-id="d2170-p122">Average ratio of compressed audio samples to the total number of samples. (Compressed audio is audio that has been compressed to help maintain call quality when a dropped network packet has been detected.) High values indicate significant levels of sample compression caused by jitter, and result in audio sounding accelerated or distorted.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="media-quality-summary-report-metrics-video-call-summary"></a><span data-ttu-id="d2170-249">メディア品質概要レポートの指標: ビデオ通話の概要</span><span class="sxs-lookup"><span data-stu-id="d2170-249">Media Quality Summary Report Metrics: Video Call Summary</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d2170-250">名前</span><span class="sxs-lookup"><span data-stu-id="d2170-250">Name</span></span></th>
<th><span data-ttu-id="d2170-251">この項目での並べ替え</span><span class="sxs-lookup"><span data-stu-id="d2170-251">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="d2170-252">説明</span><span class="sxs-lookup"><span data-stu-id="d2170-252">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d2170-253"><strong>[通話の種類/エンドポイントの種類]</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-253"><strong>Call type/Endpoint type</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-254">不可</span><span class="sxs-lookup"><span data-stu-id="d2170-254">No</span></span></p></td>
<td><p><span data-ttu-id="d2170-p123">この項目をクリックすると、その種類に基づく通話の詳細情報がレポートに表示されます。通話の種類は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="d2170-p123">When you click this item, the report shows detailed information about calls based on that type. Call types include:</span></span></p>
<ul>
<li><p><span data-ttu-id="d2170-257">UC ピアツーピア通話</span><span class="sxs-lookup"><span data-stu-id="d2170-257">UC Peer-to-Peer Calls</span></span></p></li>
<li><p><span data-ttu-id="d2170-258">UC 電話会議セッション</span><span class="sxs-lookup"><span data-stu-id="d2170-258">UC Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="d2170-259">PSTN 電話会議セッション</span><span class="sxs-lookup"><span data-stu-id="d2170-259">PSTN Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="d2170-260">PSTN 通話: メディアのバイパス</span><span class="sxs-lookup"><span data-stu-id="d2170-260">PSTN Calls: Media Bypass</span></span></p></li>
<li><p><span data-ttu-id="d2170-261">PSTN 通話 (非バイパス): UC レグ</span><span class="sxs-lookup"><span data-stu-id="d2170-261">PSTN Calls (Non-Bypass): UC Leg</span></span></p></li>
<li><p><span data-ttu-id="d2170-262">PSTN 通話 (非バイパス): ゲートウェイ レグ</span><span class="sxs-lookup"><span data-stu-id="d2170-262">PSTN Calls (Non-Bypass): Gateway Leg</span></span></p></li>
<li><p><span data-ttu-id="d2170-263">その他の通話の種類</span><span class="sxs-lookup"><span data-stu-id="d2170-263">Other Call Types</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2170-264"><strong>[通話ボリューム]</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-264"><strong>Call volume</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-265">不可</span><span class="sxs-lookup"><span data-stu-id="d2170-265">No</span></span></p></td>
<td><p><span data-ttu-id="d2170-266">通話の種類あたりの通話の総数。</span><span class="sxs-lookup"><span data-stu-id="d2170-266">Total number of calls per call type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2170-267"><strong>[低品質通話のパーセンテージ]</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-267"><strong>Poor call percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-268">不可</span><span class="sxs-lookup"><span data-stu-id="d2170-268">No</span></span></p></td>
<td><p><span data-ttu-id="d2170-p124">低品質として分類される通話の総数。低品質通話とは、少なくとも 1 つの測定指標が許容値を超えている通話 (たとえば、過剰なジッターが発生した通話) のことです。</span><span class="sxs-lookup"><span data-stu-id="d2170-p124">Total number of calls classified as poor. A poor call is any call which at least one of the measured metrics exceeded the allowed value (for example, a call that experienced excessive jitter).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2170-271"><strong>[通話ボリューム (ワイヤレス通話)]</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-271"><strong>Call volume (wireless call)</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-272">不可</span><span class="sxs-lookup"><span data-stu-id="d2170-272">No</span></span></p></td>
<td><p><span data-ttu-id="d2170-273">ワイヤレス接続を使用した通話の数。</span><span class="sxs-lookup"><span data-stu-id="d2170-273">Total number of calls that used a wireless connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2170-274"><strong>[通話ボリューム (VPN 通話)]</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-274"><strong>Call volume (VPN call)</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-275">不可</span><span class="sxs-lookup"><span data-stu-id="d2170-275">No</span></span></p></td>
<td><p><span data-ttu-id="d2170-276">VPN 接続を使用した通話の数。</span><span class="sxs-lookup"><span data-stu-id="d2170-276">Total number of calls that used a VPN connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2170-277"><strong>[通話ボリューム (外部通話)]</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-277"><strong>Call volume (external call)</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-278">不可</span><span class="sxs-lookup"><span data-stu-id="d2170-278">No</span></span></p></td>
<td><p><span data-ttu-id="d2170-279">外部接続 (つまり、内部ネットワークの外側の接続) を使用した通話の数。</span><span class="sxs-lookup"><span data-stu-id="d2170-279">Number of calls that used an external connection (that is, a connection outside the internal network).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2170-280"><strong>[平均ビット レート (キロビット/秒)]</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-280"><strong>Avg bit-rate (Kbits/s)</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-281">不可</span><span class="sxs-lookup"><span data-stu-id="d2170-281">No</span></span></p></td>
<td><p><span data-ttu-id="d2170-282">平均ビデオ ビット レート (kbps)。</span><span class="sxs-lookup"><span data-stu-id="d2170-282">Average video bit rate (in kilobits per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2170-283"><strong>[低ビット レート (%)]</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-283"><strong>Low bit-rate %</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-284">不可</span><span class="sxs-lookup"><span data-stu-id="d2170-284">No</span></span></p></td>
<td><p><span data-ttu-id="d2170-285">ビット レートが低い通話のパーセンテージ。</span><span class="sxs-lookup"><span data-stu-id="d2170-285">Percentage of the call where the bit rate was low.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2170-286"><strong>[送信パケット損失]</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-286"><strong>Outbound packet loss</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-287">不可</span><span class="sxs-lookup"><span data-stu-id="d2170-287">No</span></span></p></td>
<td><p><span data-ttu-id="d2170-p125">送信パケットのリアルタイム転送プロトコル (RTP) パケット損失 (パケット損失は、RTP パケット、つまりインターネット経由で音声とビデオを転送するために使われるプロトコルの一種で、パケットが宛先に到達できなかったときに発生します)。この値が高い場合は、輻輳、帯域幅の不足、ワイヤレスの輻輳または干渉、メディア サーバーの過負荷などの原因が考えられます。パケット損失が発生すると、通常、音声のひずみや欠落が生じます。</span><span class="sxs-lookup"><span data-stu-id="d2170-p125">Real-Time Transport Protocol (RTP) packet loss for outbound packets. (Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion, lack of bandwidth, wireless congestion or interference, or an overloaded media server. Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2170-291"><strong>[フリーズ フレーム %]</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-291"><strong>Frozen frame %</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-292">不可</span><span class="sxs-lookup"><span data-stu-id="d2170-292">No</span></span></p></td>
<td><p><span data-ttu-id="d2170-p126">"フリーズ" フレームのパーセンテージ。フリーズ フレームでは、通話の音声部分が続いていてもビデオの進行が停止します。</span><span class="sxs-lookup"><span data-stu-id="d2170-p126">Percentage of “frozen” frames. In a frozen frame, the video stops advancing while the audio portion of the call continues.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2170-295"><strong>[送信フレーム率 (平均)]</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-295"><strong>Outbound avg frame rate</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-296">不可</span><span class="sxs-lookup"><span data-stu-id="d2170-296">No</span></span></p></td>
<td><p><span data-ttu-id="d2170-297">通話時の送信の平均フレーム レート。</span><span class="sxs-lookup"><span data-stu-id="d2170-297">Average frame rate for outbound transmissions during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2170-298"><strong>[着信フレーム率 (平均)]</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-298"><strong>Inbound avg frame rate</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-299">不可</span><span class="sxs-lookup"><span data-stu-id="d2170-299">No</span></span></p></td>
<td><p><span data-ttu-id="d2170-300">通話時の受信の平均フレーム レート。</span><span class="sxs-lookup"><span data-stu-id="d2170-300">Average frame rate for incoming transmissions during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2170-301"><strong>[着信フレーム率 (低) (%)]</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-301"><strong>Inbound low frame rate %</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-302">不可</span><span class="sxs-lookup"><span data-stu-id="d2170-302">No</span></span></p></td>
<td><p><span data-ttu-id="d2170-303">着信ビデオのビット レートが低い通話のパーセンテージ。</span><span class="sxs-lookup"><span data-stu-id="d2170-303">Percentage of the call where the bit rate for incoming video was low.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2170-304"><strong>[クライアントの正常性 (%)]</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-304"><strong>Client health %</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d2170-305">通話時のクライアント デバイスの相対的な正常性を示します。</span><span class="sxs-lookup"><span data-stu-id="d2170-305">Indicates the relative health of the client device during the call.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="media-quality-summary-report-metrics-application-sharing-call-summary"></a><span data-ttu-id="d2170-306">メディア品質概要レポートの指標: アプリケーション共有の通話の概要</span><span class="sxs-lookup"><span data-stu-id="d2170-306">Media Quality Summary Report Metrics: Application Sharing Call Summary</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d2170-307">名前</span><span class="sxs-lookup"><span data-stu-id="d2170-307">Name</span></span></th>
<th><span data-ttu-id="d2170-308">この項目での並べ替え</span><span class="sxs-lookup"><span data-stu-id="d2170-308">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="d2170-309">説明</span><span class="sxs-lookup"><span data-stu-id="d2170-309">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d2170-310"><strong>[通話の種類/エンドポイントの種類]</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-310"><strong>Call type/Endpoint type</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-311">不可</span><span class="sxs-lookup"><span data-stu-id="d2170-311">No</span></span></p></td>
<td><p><span data-ttu-id="d2170-p127">この項目をクリックすると、その種類に基づく通話の詳細情報がレポートに表示されます。通話の種類は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="d2170-p127">When you click this item, the report shows detailed information about calls based on that type. Call types include:</span></span></p>
<ul>
<li><p><span data-ttu-id="d2170-314">UC ピアツーピア通話</span><span class="sxs-lookup"><span data-stu-id="d2170-314">UC Peer-to-Peer Calls</span></span></p></li>
<li><p><span data-ttu-id="d2170-315">UC 電話会議セッション</span><span class="sxs-lookup"><span data-stu-id="d2170-315">UC Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="d2170-316">PSTN 電話会議セッション</span><span class="sxs-lookup"><span data-stu-id="d2170-316">PSTN Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="d2170-317">PSTN 通話: メディアのバイパス</span><span class="sxs-lookup"><span data-stu-id="d2170-317">PSTN Calls: Media Bypass</span></span></p></li>
<li><p><span data-ttu-id="d2170-318">PSTN 通話 (非バイパス): UC レグ</span><span class="sxs-lookup"><span data-stu-id="d2170-318">PSTN Calls (Non-Bypass): UC Leg</span></span></p></li>
<li><p><span data-ttu-id="d2170-319">PSTN 通話 (非バイパス): ゲートウェイ レグ</span><span class="sxs-lookup"><span data-stu-id="d2170-319">PSTN Calls (Non-Bypass): Gateway Leg</span></span></p></li>
<li><p><span data-ttu-id="d2170-320">その他の通話の種類</span><span class="sxs-lookup"><span data-stu-id="d2170-320">Other Call Types</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2170-321"><strong>[通話ボリューム]</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-321"><strong>Call volume</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-322">不可</span><span class="sxs-lookup"><span data-stu-id="d2170-322">No</span></span></p></td>
<td><p><span data-ttu-id="d2170-323">通話の種類あたりの通話の総数。</span><span class="sxs-lookup"><span data-stu-id="d2170-323">Total number of calls per call type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2170-324"><strong>[低品質通話のパーセンテージ]</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-324"><strong>Poor call percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-325">不可</span><span class="sxs-lookup"><span data-stu-id="d2170-325">No</span></span></p></td>
<td><p><span data-ttu-id="d2170-p128">低品質として分類される通話の総数。低品質通話とは、少なくとも 1 つの測定指標が許容値を超えている通話 (たとえば、過剰なジッターが発生した通話) のことです。</span><span class="sxs-lookup"><span data-stu-id="d2170-p128">Total number of calls classified as poor. A poor call is any call which at least one of the measured metrics exceeded the allowed value (for example, a call that experienced excessive jitter).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2170-328"><strong>[通話ボリューム (ワイヤレス通話)]</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-328"><strong>Call volume (wireless call)</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-329">不可</span><span class="sxs-lookup"><span data-stu-id="d2170-329">No</span></span></p></td>
<td><p><span data-ttu-id="d2170-330">ワイヤレス接続を使用した通話の数。</span><span class="sxs-lookup"><span data-stu-id="d2170-330">Total number of calls that used a wireless connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2170-331"><strong>[通話ボリューム (VPN 通話)]</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-331"><strong>Call volume (VPN call)</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-332">不可</span><span class="sxs-lookup"><span data-stu-id="d2170-332">No</span></span></p></td>
<td><p><span data-ttu-id="d2170-333">VPN 接続を使用した通話の数。</span><span class="sxs-lookup"><span data-stu-id="d2170-333">Total number of calls that used a VPN connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2170-334"><strong>[通話ボリューム (外部通話)]</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-334"><strong>Call volume (external call)</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-335">不可</span><span class="sxs-lookup"><span data-stu-id="d2170-335">No</span></span></p></td>
<td><p><span data-ttu-id="d2170-336">外部接続 (つまり、内部ネットワークの外側の接続) を使用した通話の数。</span><span class="sxs-lookup"><span data-stu-id="d2170-336">Number of calls that used an external connection (that is, a connection outside the internal network).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2170-337"><strong>[ジッター (ミリ秒)]</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-337"><strong>Jitter (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-338">不可</span><span class="sxs-lookup"><span data-stu-id="d2170-338">No</span></span></p></td>
<td><p><span data-ttu-id="d2170-339">RTP パケットの着信間に検出された平均ジッター (ジッターとは、通話の "揺れ" の測定値です)。</span><span class="sxs-lookup"><span data-stu-id="d2170-339">Average jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="d2170-340">(ジッタは、 &quot; 通話の shakiness の尺度です &quot; )。通常、高ジッターの値は、輻輳または過負荷のメディアサーバーによって発生し、音声が歪むか、失われる原因となります。</span><span class="sxs-lookup"><span data-stu-id="d2170-340">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2170-341"><strong>[平均相対的一方向]</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-341"><strong>Avg. relative one way</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-342">不可</span><span class="sxs-lookup"><span data-stu-id="d2170-342">No</span></span></p></td>
<td><p><span data-ttu-id="d2170-p130">2 つのメディア エンドポイント間の相対的な一方向の平均遅延。これは 1 ホップの遅延の測定です。</span><span class="sxs-lookup"><span data-stu-id="d2170-p130">Average relative one-way delay between two media endpoints. This is a single-hop latency measure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2170-345"><strong>[RDP タイル処理の平均待機時間]</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-345"><strong>Avg. RDP tile processing latency</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-346">不可</span><span class="sxs-lookup"><span data-stu-id="d2170-346">No</span></span></p></td>
<td><p><span data-ttu-id="d2170-p131">表示セッション中の AS 会議サーバーでの RDP タイル処理の平均遅延。平均値が高いと、表示エクスペリエンスにおける遅延が大きくなり、ネットワーク遅延も生じます。会議サーバーが過負荷になると、平均遅延が大きくなる場合があります。</span><span class="sxs-lookup"><span data-stu-id="d2170-p131">The average RDP tile processing latency in the AS Conferencing Server over the duration of the viewing session. A high average reflects a longer delay in the viewing experience, and includes network latency. An overloaded conferencing server may experience higher average delays.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2170-350"><strong>[損失した合計タイル %]</strong></span><span class="sxs-lookup"><span data-stu-id="d2170-350"><strong>Total spoiled tile %</strong></span></span></p></td>
<td><p><span data-ttu-id="d2170-351">不可</span><span class="sxs-lookup"><span data-stu-id="d2170-351">No</span></span></p></td>
<td><p><span data-ttu-id="d2170-352">損失した RDP タイルのパーセンテージ。</span><span class="sxs-lookup"><span data-stu-id="d2170-352">Total percentage of spoiled RDP tiles.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="d2170-353">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d2170-353">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

