---
title: 'Lync Server 2013: 通話の詳細レポート'
description: 'Lync Server 2013: 通話の詳細レポート。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call Detail Report
ms:assetid: 38862e35-3fec-41b9-a035-0b301942d446
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558637(v=OCS.15)
ms:contentKeyID: 48183843
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d72ae6c1c1ec869041eee5b0dc35941c33609710
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399417"
---
# <a name="call-detail-report-in-lync-server-2013"></a><span data-ttu-id="c971a-103">Lync Server 2013 の通話詳細レポート</span><span class="sxs-lookup"><span data-stu-id="c971a-103">Call Detail Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c971a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c971a-104">

<span> </span></span></span>

<span data-ttu-id="c971a-105">_**最終更新日:** 2014-02-05_</span><span class="sxs-lookup"><span data-stu-id="c971a-105">_**Topic Last Modified:** 2014-02-05_</span></span>

<span data-ttu-id="c971a-106">通話詳細レポートでは、個々の通話の詳細が表示されます。レポートには、次のようなレポートセクションに分類された、Lync Server によって収集されたエクスペリエンスの測度と統計情報のほぼすべてが含まれます。</span><span class="sxs-lookup"><span data-stu-id="c971a-106">The Call Detail Report provides a detailed look at an individual call; the report includes nearly all the Quality of Experience metrics and statistics collected by Lync Server, divided into report sections such as:</span></span>

  - <span data-ttu-id="c971a-107">通話情報</span><span class="sxs-lookup"><span data-stu-id="c971a-107">Call Information</span></span>

  - <span data-ttu-id="c971a-108">発信者のデバイスおよび信号指標</span><span class="sxs-lookup"><span data-stu-id="c971a-108">Caller Device and Signal Metrics</span></span>

  - <span data-ttu-id="c971a-109">呼び出し先のデバイスおよび信号指標</span><span class="sxs-lookup"><span data-stu-id="c971a-109">Callee Device and Signal metrics</span></span>

  - <span data-ttu-id="c971a-110">発信者クライアント イベント</span><span class="sxs-lookup"><span data-stu-id="c971a-110">Caller Client Event</span></span>

  - <span data-ttu-id="c971a-111">呼び出し先クライアント イベント</span><span class="sxs-lookup"><span data-stu-id="c971a-111">Callee Client Event</span></span>

  - <span data-ttu-id="c971a-112">音声ストリーム (発信者から呼び出し先)</span><span class="sxs-lookup"><span data-stu-id="c971a-112">Audio Stream (Caller to Callee)</span></span>

  - <span data-ttu-id="c971a-113">ビデオ ストリーム (発信者から呼び出し先)</span><span class="sxs-lookup"><span data-stu-id="c971a-113">Video Stream (Caller to Callee)</span></span>

  - <span data-ttu-id="c971a-114">音声ストリーム (呼び出し先から発信者)</span><span class="sxs-lookup"><span data-stu-id="c971a-114">Audio Stream (Callee to Caller)</span></span>

  - <span data-ttu-id="c971a-115">ビデオ ストリーム (呼び出し先から発信者)</span><span class="sxs-lookup"><span data-stu-id="c971a-115">Video Stream (Callee to Caller)</span></span>

<span data-ttu-id="c971a-p101">特定のレポートに表示されるカテゴリと指標は、セッションの種類と、セッションで使用されたエンドポイントの種類に依存します。たとえば、音声のみの通話では、通話にビデオ ストリームがないことにより、ビデオ ストリームの指標は報告されません。同様に、呼び出し先統計はないが、発信者統計を示すレポートがあることがあります。この原因は通常、呼び出し先が SIP 準拠のデバイスを使用していないことです。エンドポイントは通話の終了後に、統計を報告します。しかし、(SIP または SIP 統計を関知しない) 携帯電話は、その種類の情報を報告することはできません。電話の相手先が携帯電話で応答した場合は、通話の終了時に、その携帯電話からのレポートは得られません。</span><span class="sxs-lookup"><span data-stu-id="c971a-p101">Keep in mind that the categories and the metrics you see on a given report depend on two things: the type of session and the type of endpoints used in the session. For example, an audio-only call will not report metrics for video streams; that's because the call didn't have a video stream. Likewise, you might have a report that lists caller statistics but not callee statistics. That's typically because the callee was not using a SIP-compliant device. Endpoints are responsible for reporting statistics at the end of a call; however, a cell phone (which knows nothing about SIP or SIP statistics) is unable to report that kind of information. If you call someone and they answer you on their cell phone, you will not get a report from that cell phone when the call ends.</span></span>

<span data-ttu-id="c971a-122">通話の詳細レポートは、特定の通話でメディアの品質の問題が発生した理由を正確に確認するときに最も役立ちます。</span><span class="sxs-lookup"><span data-stu-id="c971a-122">The Call Detail Report is most useful when you are trying to determine exactly why a given call experienced media quality problems.</span></span>

<div>

## <a name="accessing-the-call-detail-report"></a><span data-ttu-id="c971a-123">通話の詳細レポートを表示する</span><span class="sxs-lookup"><span data-stu-id="c971a-123">Accessing the Call Detail Report</span></span>

<span data-ttu-id="c971a-124">通話の詳細レポートは、以下の任意のレポートから表示できます。</span><span class="sxs-lookup"><span data-stu-id="c971a-124">The Call Detail Report can be accessed from any of the following reports:</span></span>

  - <span data-ttu-id="c971a-125">[Lync Server 2013 の位置情報レポート](lync-server-2013-location-report.md)(通話音量または低品質の通話率のメトリックをクリック)</span><span class="sxs-lookup"><span data-stu-id="c971a-125">The [Location Report in Lync Server 2013](lync-server-2013-location-report.md) (by clicking either the Call volume or the Poor call percentage metric)</span></span>

  - <span data-ttu-id="c971a-126">[Lync Server 2013 の [メディア品質の概要] レポート](lync-server-2013-media-quality-summary-report.md)(通話音量または [低品質通話率] のいずれかをクリック)</span><span class="sxs-lookup"><span data-stu-id="c971a-126">The [Media Quality Summary Report in Lync Server 2013](lync-server-2013-media-quality-summary-report.md) (by clicking either the Call volume or Poor call percentage metric)</span></span>

  - <span data-ttu-id="c971a-127">[Lync server 2013 のメディア品質比較レポート](lync-server-2013-media-quality-comparison-report.md)( [lync Server 2013 の通話リストレポート](lync-server-2013-call-list-report.md)をクリックして、詳細なメトリックをクリックします)。</span><span class="sxs-lookup"><span data-stu-id="c971a-127">The [Media Quality Comparison Report in Lync Server 2013](lync-server-2013-media-quality-comparison-report.md) (by clicking the [Call List Report in Lync Server 2013](lync-server-2013-call-list-report.md) and then clicking the Detail metric).</span></span>

  - <span data-ttu-id="c971a-128">[Lync server 2013 のサーバーパフォーマンスレポート](lync-server-2013-server-performance-report.md)(通話ボリュームまたは低品質通話パーセンテージメトリックをクリック)</span><span class="sxs-lookup"><span data-stu-id="c971a-128">The [Server Performance Report in Lync Server 2013](lync-server-2013-server-performance-report.md) (by clicking either the Call volume or Poor call percentage metric)</span></span>

  - <span data-ttu-id="c971a-129">[Lync Server 2013 の通話リストレポート](lync-server-2013-call-list-report.md)(詳細なメトリックをクリック)</span><span class="sxs-lookup"><span data-stu-id="c971a-129">The [Call List Report in Lync Server 2013](lync-server-2013-call-list-report.md) (by clicking the Detail metric)</span></span>

<span data-ttu-id="c971a-130">通話詳細レポート内から、次のメトリックのいずれかをクリックして、 [Lync Server 2013 のデバイスレポート](lync-server-2013-device-report.md) にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="c971a-130">From within the Call Detail Report you can access the [Device Report in Lync Server 2013](lync-server-2013-device-report.md) by clicking either of the following metrics:</span></span>

  - <span data-ttu-id="c971a-131">キャプチャ デバイス</span><span class="sxs-lookup"><span data-stu-id="c971a-131">Capture device</span></span>

  - <span data-ttu-id="c971a-132">[レンダー デバイス]</span><span class="sxs-lookup"><span data-stu-id="c971a-132">Render device</span></span>

<span data-ttu-id="c971a-133">また、音声ビデオ エッジ サーバー指標をクリックすると、サーバー メディア品質傾向レポートを表示できます。</span><span class="sxs-lookup"><span data-stu-id="c971a-133">You can also access the Server Media Quality Trend Report by clicking the A/V edge server metric.</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-call-detail-report"></a><span data-ttu-id="c971a-134">通話の詳細レポートの活用</span><span class="sxs-lookup"><span data-stu-id="c971a-134">Making the Best Use of the Call Detail Report</span></span>

<span data-ttu-id="c971a-p102">通話の詳細レポートには、一般的には、マイクのタイムスタンプの誤差、低 SNR 時間、および近端エコー時間の項目のような、250 個以上のさまざまな指標が含まれます。これらの指標の詳細が思い出せない場合は、指標のラベル上にマウス ポインターを置きます。多くの場合は、その指標を説明するツール ヒントが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c971a-p102">The Call Detail Report typically includes over 250 different metrics, including such items as Microphone timestamp drift, Low SNR time, and Near end to echo time. If you can't remember what all of these metrics actually measure, try holding your mouse over the metric label; often-times, a tooltip will appear describing that metric.</span></span>

<span data-ttu-id="c971a-137">メトリックの検索で問題が発生した場合は、[検索] ボックスにメトリックラベルの一部を入力し、[検索] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c971a-137">If you have problems locating a metric, type part of the metric label in the search box and then click Find.</span></span> <span data-ttu-id="c971a-138">たとえば、低い SNR 時間メトリックが見つからない場合は、検索ボックスに「SNR」と入力して、[検索] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c971a-138">For example, if you can't find the Low SNR time metric, type SNR in the search box and then click Find.</span></span>

<span data-ttu-id="c971a-p104">レポートは、通話に関する情報を記録するだけです。通話自体は記録されません。</span><span class="sxs-lookup"><span data-stu-id="c971a-p104">Note that the report only tracks information about a call. The call itself is not recorded.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="c971a-141">フィルター</span><span class="sxs-lookup"><span data-stu-id="c971a-141">Filters</span></span>

<span data-ttu-id="c971a-p105">なし。通話の詳細レポートにはフィルターを適用できません。</span><span class="sxs-lookup"><span data-stu-id="c971a-p105">None. You cannot filter the Call Detail Report.</span></span>

</div>

<div>

## <a name="metrics"></a><span data-ttu-id="c971a-144">指標</span><span class="sxs-lookup"><span data-stu-id="c971a-144">Metrics</span></span>

<span data-ttu-id="c971a-145">次の表に、各通話の通話の詳細レポートで提供される情報を示します。</span><span class="sxs-lookup"><span data-stu-id="c971a-145">The following table lists the information provided in the Call Detail Report for each call.</span></span>

### <a name="call-detail-report-metrics"></a><span data-ttu-id="c971a-146">通話の詳細レポートの指標</span><span class="sxs-lookup"><span data-stu-id="c971a-146">Call Detail Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c971a-147">名前</span><span class="sxs-lookup"><span data-stu-id="c971a-147">Name</span></span></th>
<th><span data-ttu-id="c971a-148">この項目での並べ替え</span><span class="sxs-lookup"><span data-stu-id="c971a-148">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="c971a-149">説明</span><span class="sxs-lookup"><span data-stu-id="c971a-149">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c971a-150"><strong>[発信者 PAI]</strong></span><span class="sxs-lookup"><span data-stu-id="c971a-150"><strong>Caller PAI</strong></span></span></p></td>
<td><p><span data-ttu-id="c971a-151">不可</span><span class="sxs-lookup"><span data-stu-id="c971a-151">No</span></span></p></td>
<td><p><span data-ttu-id="c971a-p106">呼び出しを開始したユーザーの P-Asserted-Identity。P-Asserted-Identity は、信頼されたネットワーク内でユーザーの証明済み ID を送信するのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="c971a-p106">P-Asserted-Identity of the user who initiated the call. The P-Asserted-Identity is used to convey the proven identity of a user within a trusted network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c971a-154"><strong>[発信者 URI]</strong></span><span class="sxs-lookup"><span data-stu-id="c971a-154"><strong>Caller URI</strong></span></span></p></td>
<td><p><span data-ttu-id="c971a-155">不可</span><span class="sxs-lookup"><span data-stu-id="c971a-155">No</span></span></p></td>
<td><p><span data-ttu-id="c971a-156">呼び出しを開始したユーザーの SIP アドレス。</span><span class="sxs-lookup"><span data-stu-id="c971a-156">SIP address of the user who initiated the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c971a-157"><strong>[発信者エンドポイント]</strong></span><span class="sxs-lookup"><span data-stu-id="c971a-157"><strong>Caller endpoint</strong></span></span></p></td>
<td><p><span data-ttu-id="c971a-158">不可</span><span class="sxs-lookup"><span data-stu-id="c971a-158">No</span></span></p></td>
<td><p><span data-ttu-id="c971a-159">呼び出しを実行したデバイス。</span><span class="sxs-lookup"><span data-stu-id="c971a-159">Device used to make the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c971a-160"><strong>[発信者ユーザー エージェント]</strong></span><span class="sxs-lookup"><span data-stu-id="c971a-160"><strong>Caller user agent</strong></span></span></p></td>
<td><p><span data-ttu-id="c971a-161">不可</span><span class="sxs-lookup"><span data-stu-id="c971a-161">No</span></span></p></td>
<td><p><span data-ttu-id="c971a-162">呼び出しを実行したデバイスで使用されるソフトウェア。</span><span class="sxs-lookup"><span data-stu-id="c971a-162">Software used on the device that made the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c971a-163"><strong>[通話の開始]</strong></span><span class="sxs-lookup"><span data-stu-id="c971a-163"><strong>Call start</strong></span></span></p></td>
<td><p><span data-ttu-id="c971a-164">不可</span><span class="sxs-lookup"><span data-stu-id="c971a-164">No</span></span></p></td>
<td><p><span data-ttu-id="c971a-165">呼び出しが最初に開始された日時。</span><span class="sxs-lookup"><span data-stu-id="c971a-165">Date and time that the call was initially placed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c971a-166"><strong>[仲介サーバーのバイパス通話]</strong></span><span class="sxs-lookup"><span data-stu-id="c971a-166"><strong>Mediation Server bypass call</strong></span></span></p></td>
<td><p><span data-ttu-id="c971a-167">不可</span><span class="sxs-lookup"><span data-stu-id="c971a-167">No</span></span></p></td>
<td><p><span data-ttu-id="c971a-168">呼び出しが仲介サーバーを経由せずに PSTN 音声ゲートウェイまたは適切な IP-PBX に接続されたかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="c971a-168">Indicates whether the call connected to a PSTN voice gateway or qualified IP-PBX without passing through the Mediation Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c971a-169"><strong>[発信者 OS]</strong></span><span class="sxs-lookup"><span data-stu-id="c971a-169"><strong>Caller OS</strong></span></span></p></td>
<td><p><span data-ttu-id="c971a-170">不可</span><span class="sxs-lookup"><span data-stu-id="c971a-170">No</span></span></p></td>
<td><p><span data-ttu-id="c971a-171">呼び出し元のコンピューターのオペレーティング システム。</span><span class="sxs-lookup"><span data-stu-id="c971a-171">Operating system of the caller's computer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c971a-172"><strong>[発信者 CPU]</strong></span><span class="sxs-lookup"><span data-stu-id="c971a-172"><strong>Caller CPU</strong></span></span></p></td>
<td><p><span data-ttu-id="c971a-173">不可</span><span class="sxs-lookup"><span data-stu-id="c971a-173">No</span></span></p></td>
<td><p><span data-ttu-id="c971a-174">呼び出しを開始したユーザーのコンピューターに搭載される CPU。</span><span class="sxs-lookup"><span data-stu-id="c971a-174">CPU installed in the computer of the user who initiated the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c971a-175"><strong>[発信者 CPU コア番号]</strong></span><span class="sxs-lookup"><span data-stu-id="c971a-175"><strong>Caller CPU core number</strong></span></span></p></td>
<td><p><span data-ttu-id="c971a-176">不可</span><span class="sxs-lookup"><span data-stu-id="c971a-176">No</span></span></p></td>
<td><p><span data-ttu-id="c971a-177">呼び出しを開始したユーザーが使用するコンピューターのプロセッサ番号。</span><span class="sxs-lookup"><span data-stu-id="c971a-177">Processor number in the computer used by the person who initiated the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c971a-178"><strong>[発信者 CPU 速度]</strong></span><span class="sxs-lookup"><span data-stu-id="c971a-178"><strong>Caller CPU speed</strong></span></span></p></td>
<td><p><span data-ttu-id="c971a-179">不可</span><span class="sxs-lookup"><span data-stu-id="c971a-179">No</span></span></p></td>
<td><p><span data-ttu-id="c971a-180">呼び出しを開始したユーザーが使用するコンピューターの CPU のクロック速度。</span><span class="sxs-lookup"><span data-stu-id="c971a-180">Clock speed of the CPU of the computer used by the person who initiated the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c971a-181"><strong>[発信者 CPU 仮想化]</strong></span><span class="sxs-lookup"><span data-stu-id="c971a-181"><strong>Caller CPU virtualization</strong></span></span></p></td>
<td><p><span data-ttu-id="c971a-182">不可</span><span class="sxs-lookup"><span data-stu-id="c971a-182">No</span></span></p></td>
<td><p><span data-ttu-id="c971a-183">呼び出しを開始したユーザーが使用するコンピューターでの仮想化 (仮想化されている場合)。</span><span class="sxs-lookup"><span data-stu-id="c971a-183">Virtualization (if any) used on the computer used by the person who initiated the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c971a-184"><strong>[呼び出し先 PAI]</strong></span><span class="sxs-lookup"><span data-stu-id="c971a-184"><strong>Callee PAI</strong></span></span></p></td>
<td><p><span data-ttu-id="c971a-185">不可</span><span class="sxs-lookup"><span data-stu-id="c971a-185">No</span></span></p></td>
<td><p><span data-ttu-id="c971a-p107">通話に招待されたユーザーの P-Asserted-Identity。P-Asserted-Identity は、信頼されたネットワーク内でユーザーの証明済み ID を送信するのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="c971a-p107">P-Asserted-Identity of the user who was invited to join the call. The P-Asserted-Identity is used to convey the proven identity of a user within a trusted network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c971a-188"><strong>[呼び出し先 URI]</strong></span><span class="sxs-lookup"><span data-stu-id="c971a-188"><strong>Callee URI</strong></span></span></p></td>
<td><p><span data-ttu-id="c971a-189">不可</span><span class="sxs-lookup"><span data-stu-id="c971a-189">No</span></span></p></td>
<td><p><span data-ttu-id="c971a-190">呼び出し先ユーザーの SIP アドレス。</span><span class="sxs-lookup"><span data-stu-id="c971a-190">SIP address of the user who was called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c971a-191"><strong>[呼び出し先エンドポイント]</strong></span><span class="sxs-lookup"><span data-stu-id="c971a-191"><strong>Callee endpoint</strong></span></span></p></td>
<td><p><span data-ttu-id="c971a-192">不可</span><span class="sxs-lookup"><span data-stu-id="c971a-192">No</span></span></p></td>
<td><p><span data-ttu-id="c971a-193">呼び出しを受信したデバイス。</span><span class="sxs-lookup"><span data-stu-id="c971a-193">Device used to receive the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c971a-194"><strong>[呼び出し先ユーザー エージェント]</strong></span><span class="sxs-lookup"><span data-stu-id="c971a-194"><strong>Callee user agent</strong></span></span></p></td>
<td><p><span data-ttu-id="c971a-195">不可</span><span class="sxs-lookup"><span data-stu-id="c971a-195">No</span></span></p></td>
<td><p><span data-ttu-id="c971a-196">呼び出しを受信したデバイスで使用されるソフトウェア。</span><span class="sxs-lookup"><span data-stu-id="c971a-196">Software used on the device that received the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c971a-197"><strong>[時間]</strong></span><span class="sxs-lookup"><span data-stu-id="c971a-197"><strong>Duration</strong></span></span></p></td>
<td><p><span data-ttu-id="c971a-198">不可</span><span class="sxs-lookup"><span data-stu-id="c971a-198">No</span></span></p></td>
<td><p><span data-ttu-id="c971a-199">通話時間。</span><span class="sxs-lookup"><span data-stu-id="c971a-199">Length of time for the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c971a-200"><strong>[メディア バイパス警告フラグ]</strong></span><span class="sxs-lookup"><span data-stu-id="c971a-200"><strong>Media bypass warning flag</strong></span></span></p></td>
<td><p><span data-ttu-id="c971a-201">不可</span><span class="sxs-lookup"><span data-stu-id="c971a-201">No</span></span></p></td>
<td><p><span data-ttu-id="c971a-202">仲介サーバーがバイパスされたときに発行された警告。</span><span class="sxs-lookup"><span data-stu-id="c971a-202">Warning issued when the Mediation Server was bypassed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c971a-203"><strong>[呼び出し先 OS]</strong></span><span class="sxs-lookup"><span data-stu-id="c971a-203"><strong>Callee OS</strong></span></span></p></td>
<td><p><span data-ttu-id="c971a-204">不可</span><span class="sxs-lookup"><span data-stu-id="c971a-204">No</span></span></p></td>
<td><p><span data-ttu-id="c971a-205">呼び出し先ユーザーのコンピューターのオペレーティング システム。</span><span class="sxs-lookup"><span data-stu-id="c971a-205">Operating system of the computer for the user who was called.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c971a-206"><strong>[呼び出し先 CPU]</strong></span><span class="sxs-lookup"><span data-stu-id="c971a-206"><strong>Callee CPU</strong></span></span></p></td>
<td><p><span data-ttu-id="c971a-207">不可</span><span class="sxs-lookup"><span data-stu-id="c971a-207">No</span></span></p></td>
<td><p><span data-ttu-id="c971a-208">呼び出し先ユーザーのコンピューターに搭載される CPU。</span><span class="sxs-lookup"><span data-stu-id="c971a-208">CPU installed in the computer of the user who was called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c971a-209"><strong>[呼び出し先コア番号]</strong></span><span class="sxs-lookup"><span data-stu-id="c971a-209"><strong>Callee core number</strong></span></span></p></td>
<td><p><span data-ttu-id="c971a-210">いいえ</span><span class="sxs-lookup"><span data-stu-id="c971a-210">No</span></span></p></td>
<td><p><span data-ttu-id="c971a-211">呼び出し先ユーザーが使用するコンピューターのプロセッサ番号。</span><span class="sxs-lookup"><span data-stu-id="c971a-211">Processor number in the computer used by the person who was called.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c971a-212"><strong>[呼び出し先 CPU 速度]</strong></span><span class="sxs-lookup"><span data-stu-id="c971a-212"><strong>Callee CPU speed</strong></span></span></p></td>
<td><p><span data-ttu-id="c971a-213">不可</span><span class="sxs-lookup"><span data-stu-id="c971a-213">No</span></span></p></td>
<td><p><span data-ttu-id="c971a-214">呼び出し先ユーザーが使用するコンピューターの CPU のクロック速度。</span><span class="sxs-lookup"><span data-stu-id="c971a-214">Clock speed of the CPU of the computer used by the person who was called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c971a-215"><strong>[呼び出し先 CPU 仮想化]</strong></span><span class="sxs-lookup"><span data-stu-id="c971a-215"><strong>Callee CPU virtualization</strong></span></span></p></td>
<td><p><span data-ttu-id="c971a-216">不可</span><span class="sxs-lookup"><span data-stu-id="c971a-216">No</span></span></p></td>
<td><p><span data-ttu-id="c971a-217">呼び出し先ユーザーが使用するコンピューターでの仮想化 (仮想化されている場合)。</span><span class="sxs-lookup"><span data-stu-id="c971a-217">Virtualization (if any) used on the computer used by the person who was called.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="c971a-218">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c971a-218">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

