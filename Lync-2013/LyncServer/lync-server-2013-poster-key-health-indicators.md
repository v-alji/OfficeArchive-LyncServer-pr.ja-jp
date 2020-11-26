---
title: 'Lync Server 2013: ポスター: 主要な正常性インジケーター'
description: 'Lync Server 2013: ポスター: 主要な正常性インジケーター。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: 'Poster: Key Health Indicators'
ms:assetid: 8367dccf-adaa-4a0b-a4ed-bc9570cc5e24
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn593599(v=OCS.15)
ms:contentKeyID: 61084873
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9962d1764d5d2c664bb8415261344d9b48c81149
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424242"
---
# <a name="key-health-indicators-in-lync-server-2013"></a><span data-ttu-id="c53ca-103">Lync Server 2013 の主要な正常性インジケーター</span><span class="sxs-lookup"><span data-stu-id="c53ca-103">Key Health Indicators in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c53ca-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c53ca-104">

<span> </span></span></span>

<span data-ttu-id="c53ca-105">_**最終更新日:** 2014-02-10_</span><span class="sxs-lookup"><span data-stu-id="c53ca-105">_**Topic Last Modified:** 2014-02-10_</span></span>

<span data-ttu-id="c53ca-106">この記事では、主要な正常性インジケーターの管理について説明します。これは、ダウンロードセンターからダウンロードできる [正常な Lync server ポスターを保守するための基盤](https://go.microsoft.com/fwlink/?linkid=391838) です。</span><span class="sxs-lookup"><span data-stu-id="c53ca-106">This article is a companion to the [Key Health Indicators: The Foundation for Maintaining Healthy Lync Servers](https://go.microsoft.com/fwlink/?linkid=391838) poster, which you can download from the Download Center.</span></span>

<span data-ttu-id="c53ca-107">![KHI データを使ったトラブルシューティングについて説明しているポスター](images/Dn594589.b6fe82bd-d70f-4c1f-a812-b615ac5fa7d7(OCS.15).jpg "KHI データを使ったトラブルシューティングについて説明しているポスター")</span><span class="sxs-lookup"><span data-stu-id="c53ca-107">![Poster describing troubleshooting using KHI data](images/Dn594589.b6fe82bd-d70f-4c1f-a812-b615ac5fa7d7(OCS.15).jpg "Poster describing troubleshooting using KHI data")</span></span>

<span data-ttu-id="c53ca-108">このポスターを使って、重要な正常性インジケーター (KHIs) について説明します。パフォーマンスカウンターは、ユーザーエクスペリエンスの問題を明らかにすることを目的としたしきい値を備えています。</span><span class="sxs-lookup"><span data-stu-id="c53ca-108">You can use this poster to learn about Key Health Indicators (KHIs), performance counters with thresholds aimed at revealing user experience issues.</span></span> <span data-ttu-id="c53ca-109">KHI データの収集は、通常、通話品質の方法 (CQM) を実装するための最初の手順であり、Lync ユーザーの品質オーディオエクスペリエンスを実現することに重点を置いています。</span><span class="sxs-lookup"><span data-stu-id="c53ca-109">Gathering KHI data is usually the first step to implementing the Call Quality Methodology (CQM), which is focused on ensuring a quality audio experience for Lync users.</span></span>

<span data-ttu-id="c53ca-110">CQM の使い方について質問がある場合は、cqmfeedback@microsoft.com に質問を送信できます。</span><span class="sxs-lookup"><span data-stu-id="c53ca-110">If you have questions about how to use CQM, you can submit your questions to cqmfeedback@microsoft.com.</span></span>

<span data-ttu-id="c53ca-111">このポスターでは、次の領域について説明します。</span><span class="sxs-lookup"><span data-stu-id="c53ca-111">The poster explains the following areas:</span></span>

  - <span data-ttu-id="c53ca-112">主要な正常性インジケーターとは</span><span class="sxs-lookup"><span data-stu-id="c53ca-112">What are Key Health Indicators?</span></span>

  - <span data-ttu-id="c53ca-113">KHI データを収集するには</span><span class="sxs-lookup"><span data-stu-id="c53ca-113">To Collect KHI Data</span></span>

  - <span data-ttu-id="c53ca-114">すべてのサーバーの役割の改善フロー</span><span class="sxs-lookup"><span data-stu-id="c53ca-114">Remediation Flow for all Server Roles</span></span>

  - <span data-ttu-id="c53ca-115">解説</span><span class="sxs-lookup"><span data-stu-id="c53ca-115">Glossary</span></span>

  - <span data-ttu-id="c53ca-116">フロントエンドサーバー</span><span class="sxs-lookup"><span data-stu-id="c53ca-116">Front-end Servers</span></span>

  - <span data-ttu-id="c53ca-117">バックエンドの SQL Server</span><span class="sxs-lookup"><span data-stu-id="c53ca-117">Backend SQL Servers</span></span>

  - <span data-ttu-id="c53ca-118">仲介サーバー</span><span class="sxs-lookup"><span data-stu-id="c53ca-118">Mediation Servers</span></span>

  - <span data-ttu-id="c53ca-119">エッジ サーバー</span><span class="sxs-lookup"><span data-stu-id="c53ca-119">Edge Servers</span></span>

<span id="WhatIs"></span>

<div>

## <a name="what-are-key-health-indicators"></a><span data-ttu-id="c53ca-120">主要な正常性インジケーターとは</span><span class="sxs-lookup"><span data-stu-id="c53ca-120">What are Key Health Indicators?</span></span>

<span data-ttu-id="c53ca-121">主要な正常性インジケーターは、ユーザーエクスペリエンスの問題を明らかにするしきい値を持つパフォーマンスカウンターです。</span><span class="sxs-lookup"><span data-stu-id="c53ca-121">Key Health Indicators are performance counters with thresholds aimed at revealing user experience issues.</span></span> <span data-ttu-id="c53ca-122">KHI データの収集は、通常、通話品質の方法 (CQM) を実装するための最初の手順であり、Lync ユーザーの品質オーディオエクスペリエンスを実現することに重点を置いています。</span><span class="sxs-lookup"><span data-stu-id="c53ca-122">Gathering KHI data is usually the first step to implementing the Call Quality Methodology (CQM), which is focused on ensuring a quality audio experience for Lync users.</span></span>

<span data-ttu-id="c53ca-123">KHIs は、これらのソリューションではなく、標準の Lync 監視ソリューション (System Center Operations Manager、代理トランザクション、監視サーバーなど) に加えて使用されます。</span><span class="sxs-lookup"><span data-stu-id="c53ca-123">KHIs are used in addition to standard Lync Monitoring Solutions (e.g. System Center Operations Manager, Synthetic Transactions, Monitoring Server) and not instead of those solutions.</span></span>

<span data-ttu-id="c53ca-124">KHI パフォーマンスカウンターを収集し、[ネットワークガイド] に [ネットワークガイド] と表示された、Lync 展開のサーバーの正常性を判断するのに役立つスコアカードを作成します。</span><span class="sxs-lookup"><span data-stu-id="c53ca-124">Collect the KHI performance counters and populate the KHI spreadsheet accompanying the Networking Guide to produce a scorecard that will help you determine the server health of a Lync deployment.</span></span> <span data-ttu-id="c53ca-125">設定が完了したら、環境の修復について説明し、他の関係者に関する詳しい情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="c53ca-125">Once populated, it guides you in repairing the environment and gives additional insight to other stakeholders.</span></span> <span data-ttu-id="c53ca-126">KHIs を月単位で評価し、展開の進行中の運用プロセスに組み込みます。</span><span class="sxs-lookup"><span data-stu-id="c53ca-126">Evaluate KHIs on a monthly basis and incorporate them into any deployment’s ongoing operational processes.</span></span>

<span data-ttu-id="c53ca-127">[Lync Server ネットワークガイド](https://go.microsoft.com/fwlink/p/?linkid=390677)をダウンロードして、khis の一覧を参照し、関連するスプレッドシートを取得してください。</span><span class="sxs-lookup"><span data-stu-id="c53ca-127">Download the [Lync Server Networking Guide](https://go.microsoft.com/fwlink/p/?linkid=390677) to see the full list of KHIs and to get the related spreadsheets.</span></span>

</div>

<span id="ToCollect"></span>

<div>

## <a name="to-collect-khi-data"></a><span data-ttu-id="c53ca-128">KHI データを収集するには</span><span class="sxs-lookup"><span data-stu-id="c53ca-128">To Collect KHI Data</span></span>

1.  <span data-ttu-id="c53ca-129">Lync Server ネットワークガイドに含まれている KHI スクリプトを各 Lync サーバーに実行します。</span><span class="sxs-lookup"><span data-stu-id="c53ca-129">Run the KHI script included with the Lync Server Networking Guide on each Lync Server.</span></span> <span data-ttu-id="c53ca-130">これにより、パフォーマンスモニターの内部にデータコレクターが作成され、その名前に "こんにちは" という名前が付いています。</span><span class="sxs-lookup"><span data-stu-id="c53ca-130">This will create a Data Collector inside of Performance Monitor and name it KHI.</span></span> <span data-ttu-id="c53ca-131">既定では、データは15秒ごとにポーリングされます。</span><span class="sxs-lookup"><span data-stu-id="c53ca-131">By default, data will be polled every 15 seconds.</span></span>

2.  <span data-ttu-id="c53ca-132">会社の就業日の開始前に、各 Lync サーバーに移動し、KHI データコレクターを開始します。</span><span class="sxs-lookup"><span data-stu-id="c53ca-132">Before the start of your company's business day, go to each Lync Server and start the KHI Data Collector.</span></span>

3.  <span data-ttu-id="c53ca-133">その日の最後に、KHI データコレクターを停止し、データを1か所にコピーします。</span><span class="sxs-lookup"><span data-stu-id="c53ca-133">At the end of that day, stop the KHI Data Collector and copy the data to a central location.</span></span>

4.  <span data-ttu-id="c53ca-134">パフォーマンスモニターを使用して、Lync Server ネットワークガイドのダウンロードに含まれている KHI スプレッドシートに入力したら、結果と推奨されるターゲットを比較します。</span><span class="sxs-lookup"><span data-stu-id="c53ca-134">After using Performance Monitor to fill in the KHI spreadsheet included with the Lync Server Networking Guide download, compare the results to the recommended targets.</span></span>

</div>

<span id="Remidiation"></span>

<div>

## <a name="remediation-flow-for-all-server-roles"></a><span data-ttu-id="c53ca-135">すべてのサーバーの役割の改善フロー</span><span class="sxs-lookup"><span data-stu-id="c53ca-135">Remediation Flow for all Server Roles</span></span>

<span data-ttu-id="c53ca-136">Lync の実装の各サーバーについて、サーバーのコンポーネントの正常性とシステムのパフォーマンスが目的のレベル以上であることを確認することから始めます。</span><span class="sxs-lookup"><span data-stu-id="c53ca-136">For each server in your Lync implementation, begin by verifying that the server’s component health and system performance is at or above the desired level.</span></span> <span data-ttu-id="c53ca-137">その後にのみ、Lync の実装でのサーバーの役割に関連するインジケーターを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c53ca-137">Only after that should you look at the indicators relating to the server’s role in the overall Lync implementation.</span></span>

<span data-ttu-id="c53ca-138">まず、すべてのサーバーについて KHI のパフォーマンスデータを収集します。</span><span class="sxs-lookup"><span data-stu-id="c53ca-138">Begin by collecting KHI Performance Data for all servers.</span></span> <span data-ttu-id="c53ca-139">システムの各役割 (このドキュメントの後半で説明します) で、基本的なシステムコンポーネントが推奨されるターゲットを満たしているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="c53ca-139">For each of the system roles (details discussed later in this document) determine whether the basic system components meet the recommended targets.</span></span> <span data-ttu-id="c53ca-140">そうしない場合は、システムのパフォーマンスを改善し、KHI データを再収集して、Lync の実装でサーバーの役割に固有の基準を確認する前に、システムの正常性を確保します。</span><span class="sxs-lookup"><span data-stu-id="c53ca-140">If they do not, remediate the system performance then re-collect KHI data and ensure system health before looking at the metrics specific to the server’s role in the Lync implementation.</span></span> <span data-ttu-id="c53ca-141">すべての役割のコンポーネントの正常性は、次のように定義されます。</span><span class="sxs-lookup"><span data-stu-id="c53ca-141">Component health for all roles is defined as:</span></span>

  - <span data-ttu-id="c53ca-142">CPU 使用率 \< 80%</span><span class="sxs-lookup"><span data-stu-id="c53ca-142">CPU Utilization \< 80%</span></span>

  - <span data-ttu-id="c53ca-143">平均ディスク書き込み \< 10 ms</span><span class="sxs-lookup"><span data-stu-id="c53ca-143">Avg. Disk Write \< 10 ms</span></span>

  - <span data-ttu-id="c53ca-144">平均ディスク読み取り \< 10 ms</span><span class="sxs-lookup"><span data-stu-id="c53ca-144">Avg. Disk Read \< 10 ms</span></span>

  - <span data-ttu-id="c53ca-145">使用可能なメモリ \> 20% システム合計 MB</span><span class="sxs-lookup"><span data-stu-id="c53ca-145">Available memory \>20% System Total MB</span></span>

  - <span data-ttu-id="c53ca-146">ネットワークキューの長さ \< 2</span><span class="sxs-lookup"><span data-stu-id="c53ca-146">Network Queue Length \< 2</span></span>

  - <span data-ttu-id="c53ca-147">破棄されたパケット (in/out) = 0</span><span class="sxs-lookup"><span data-stu-id="c53ca-147">Discarded Packets (in / out) = 0</span></span>

</div>

<span id="Glossary"></span>

<div>

## <a name="glossary"></a><span data-ttu-id="c53ca-148">解説</span><span class="sxs-lookup"><span data-stu-id="c53ca-148">Glossary</span></span>

<span data-ttu-id="c53ca-149">このポスターでは、次の用語と頭字語が使用されています。</span><span class="sxs-lookup"><span data-stu-id="c53ca-149">The following terms and acronyms are used in this poster:</span></span>

<span data-ttu-id="c53ca-150">MCU = アプリケーション共有マルチポイントコントロールユニット</span><span class="sxs-lookup"><span data-stu-id="c53ca-150">AS MCU = Application Sharing Multi-point Control Unit</span></span>

<span data-ttu-id="c53ca-151">AV MCU = オーディオ/ビデオ MCU</span><span class="sxs-lookup"><span data-stu-id="c53ca-151">AV MCU = Audio/Video MCU</span></span>

<span data-ttu-id="c53ca-152">IM MCU = インスタントメッセージング MCU</span><span class="sxs-lookup"><span data-stu-id="c53ca-152">IM MCU = Instant Messaging MCU</span></span>

<span data-ttu-id="c53ca-153">UCWA = ユニファイドコミュニケーションの Web API</span><span class="sxs-lookup"><span data-stu-id="c53ca-153">UCWA = Unified Communications Web API</span></span>

<span data-ttu-id="c53ca-154">AV Edge = edge 経由の音声/ビデオのトラバーサル</span><span class="sxs-lookup"><span data-stu-id="c53ca-154">AV Edge = Traversal of audio/video via edge</span></span>

<span data-ttu-id="c53ca-155">AV Auth = 音声/ビデオ認証</span><span class="sxs-lookup"><span data-stu-id="c53ca-155">AV Auth = Audio/Video Authentication</span></span>

<span data-ttu-id="c53ca-156">SIP スタック = Lync のコア SIP の実装が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c53ca-156">SIP Stack = Contains Lync’s core SIP implementation</span></span>

<span data-ttu-id="c53ca-157">データプロキシ = edge 会議に使用</span><span class="sxs-lookup"><span data-stu-id="c53ca-157">Data Proxy = Used for edge conferencing</span></span>

<span data-ttu-id="c53ca-158">I Ss = Lync ストレージサービス</span><span class="sxs-lookup"><span data-stu-id="c53ca-158">LySS = Lync Storage Service</span></span>

</div>

<span id="Front"></span>

<div>

## <a name="front-end-servers"></a><span data-ttu-id="c53ca-159">フロントエンドサーバー</span><span class="sxs-lookup"><span data-stu-id="c53ca-159">Front-end Servers</span></span>

<span data-ttu-id="c53ca-160">以下の KHI ターゲットは、基本的なコンポーネントの正常性に加えて、フロントエンドサーバーに固有のものです。</span><span class="sxs-lookup"><span data-stu-id="c53ca-160">The following recommended KHI targets are specific to front-end servers in addition to basic component health:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c53ca-161">機能領域</span><span class="sxs-lookup"><span data-stu-id="c53ca-161">Functional area</span></span></th>
<th><span data-ttu-id="c53ca-162">目標指標</span><span class="sxs-lookup"><span data-stu-id="c53ca-162">Target Metrics</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c53ca-163">/AV/IM MCU</span><span class="sxs-lookup"><span data-stu-id="c53ca-163">AS/AV/IM MCU</span></span></p></td>
<td><p><span data-ttu-id="c53ca-164">MCU 正常性状態 &lt; 2</span><span class="sxs-lookup"><span data-stu-id="c53ca-164">MCU Health State &lt;2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c53ca-165">Web コンポーネント</span><span class="sxs-lookup"><span data-stu-id="c53ca-165">Web Components</span></span></p></td>
<td><p><span data-ttu-id="c53ca-166">配布リスト展開広告タイムアウト &lt; 0</span><span class="sxs-lookup"><span data-stu-id="c53ca-166">Distribution List expansion AD timeouts &lt;0</span></span></p>
<p><span data-ttu-id="c53ca-167">ABWQ エラー = 0</span><span class="sxs-lookup"><span data-stu-id="c53ca-167">ABWQ failures = 0</span></span></p>
<p><span data-ttu-id="c53ca-168">LIS のエラー = 0</span><span class="sxs-lookup"><span data-stu-id="c53ca-168">LIS failures = 0</span></span></p>
<p><span data-ttu-id="c53ca-169">認証エラー &lt; 1/秒</span><span class="sxs-lookup"><span data-stu-id="c53ca-169">Authentication Errors &lt; 1/sec</span></span></p>
<p><span data-ttu-id="c53ca-170">ASP.NET v4 要求が拒否されました = 0</span><span class="sxs-lookup"><span data-stu-id="c53ca-170">ASP.NET v4 Requests Rejected = 0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c53ca-171">SIP スタック</span><span class="sxs-lookup"><span data-stu-id="c53ca-171">SIP Stack</span></span></p></td>
<td><p><span data-ttu-id="c53ca-172">平均受信メッセージ ( &lt; 1 秒)</span><span class="sxs-lookup"><span data-stu-id="c53ca-172">Avg. Incoming Message Processing &lt; 1 sec</span></span></p>
<p><span data-ttu-id="c53ca-173">着信応答のドロップ &lt; 1/秒の受信要求 &lt; 1/秒</span><span class="sxs-lookup"><span data-stu-id="c53ca-173">Incoming Responses Dropped &lt; 1/sec Incoming Requests Dropped &lt; 1/sec</span></span></p>
<p><span data-ttu-id="c53ca-174">キュー待機時間 &lt; 100 ミリ秒</span><span class="sxs-lookup"><span data-stu-id="c53ca-174">Queue Latency &lt; 100 ms</span></span></p>
<p><span data-ttu-id="c53ca-175">ストアドプロシージャ待機時間 &lt; 100 ミリ秒</span><span class="sxs-lookup"><span data-stu-id="c53ca-175">Sproc Latency &lt; 100 ms</span></span></p>
<p><span data-ttu-id="c53ca-176">調整要求 = 0</span><span class="sxs-lookup"><span data-stu-id="c53ca-176">Throttled Requests = 0</span></span></p>
<p><span data-ttu-id="c53ca-177">認証エラー &lt; 1/秒</span><span class="sxs-lookup"><span data-stu-id="c53ca-177">Authentication Errors &lt; 1/sec</span></span></p>
<p><span data-ttu-id="c53ca-178">受信メッセージがタイムアウトしました &lt; 2</span><span class="sxs-lookup"><span data-stu-id="c53ca-178">Incoming Messages Timed Out &lt; 2</span></span></p>
<p><span data-ttu-id="c53ca-179">平均受信メッセージ &lt; 1 秒を保持</span><span class="sxs-lookup"><span data-stu-id="c53ca-179">Avg. Incoming Message Hold &lt; 1 sec</span></span></p>
<p><span data-ttu-id="c53ca-180">フロー制御接続 &lt; 2</span><span class="sxs-lookup"><span data-stu-id="c53ca-180">Flow Controlled Connections &lt; 2</span></span></p>
<p><span data-ttu-id="c53ca-181">Avg キューの遅延 &lt; 2 秒</span><span class="sxs-lookup"><span data-stu-id="c53ca-181">Avg. Out Queue Delay &lt; 2 sec</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c53ca-182">一 Ss</span><span class="sxs-lookup"><span data-stu-id="c53ca-182">LySS</span></span></p></td>
<td><p><span data-ttu-id="c53ca-183">Storage Service DB 80 で使用されている領域の割合 &lt;</span><span class="sxs-lookup"><span data-stu-id="c53ca-183">% of space used by Storage Service DB &lt; 80</span></span></p>
<p><span data-ttu-id="c53ca-184"># レプリカレプリケーションエラーの数 = 0</span><span class="sxs-lookup"><span data-stu-id="c53ca-184"># of replica replication failures = 0</span></span></p>
<p><span data-ttu-id="c53ca-185"># データ損失イベントの数 = 0</span><span class="sxs-lookup"><span data-stu-id="c53ca-185"># of data loss events = 0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c53ca-186">『</span><span class="sxs-lookup"><span data-stu-id="c53ca-186">SQL</span></span></p></td>
<td><p><span data-ttu-id="c53ca-187">ページ寿命 &gt; の予測300秒</span><span class="sxs-lookup"><span data-stu-id="c53ca-187">Page life expectancy &gt; 300 Sec.</span></span></p>
<p><span data-ttu-id="c53ca-188">バッチ要求/秒 &lt; 2500</span><span class="sxs-lookup"><span data-stu-id="c53ca-188">Batch requests / sec &lt; 2500</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<span id="BackEnd"></span>

<div>

## <a name="backend-sql-servers"></a><span data-ttu-id="c53ca-189">バックエンドの SQL Server</span><span class="sxs-lookup"><span data-stu-id="c53ca-189">Backend SQL Servers</span></span>

<span data-ttu-id="c53ca-190">以下の KHI ターゲットは、基本的なコンポーネントの正常性に加えて、SQL server に固有のものです。</span><span class="sxs-lookup"><span data-stu-id="c53ca-190">The following recommended KHI targets are specific to SQL servers in addition to basic component health:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c53ca-191">機能領域</span><span class="sxs-lookup"><span data-stu-id="c53ca-191">Functional area</span></span></th>
<th><span data-ttu-id="c53ca-192">目標指標</span><span class="sxs-lookup"><span data-stu-id="c53ca-192">Target Metrics</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c53ca-193">『</span><span class="sxs-lookup"><span data-stu-id="c53ca-193">SQL</span></span></p></td>
<td><p><span data-ttu-id="c53ca-194">ページ寿命 &gt; の予測300秒</span><span class="sxs-lookup"><span data-stu-id="c53ca-194">Page life expectancy &gt; 300 Sec.</span></span></p>
<p><span data-ttu-id="c53ca-195">バッチ要求/秒 &lt; 2500</span><span class="sxs-lookup"><span data-stu-id="c53ca-195">Batch requests / sec &lt; 2500</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<span id="Mediation"></span>

<div>

## <a name="mediation-servers"></a><span data-ttu-id="c53ca-196">仲介サーバー</span><span class="sxs-lookup"><span data-stu-id="c53ca-196">Mediation Servers</span></span>

<span data-ttu-id="c53ca-197">以下の KHI ターゲットは、基本的なコンポーネントの正常性に加えて、仲介サーバーに固有のものです。</span><span class="sxs-lookup"><span data-stu-id="c53ca-197">The following recommended KHI targets are specific to mediation servers in addition to basic component health:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c53ca-198">機能領域</span><span class="sxs-lookup"><span data-stu-id="c53ca-198">Functional area</span></span></th>
<th><span data-ttu-id="c53ca-199">目標指標</span><span class="sxs-lookup"><span data-stu-id="c53ca-199">Target Metrics</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c53ca-200">仲介サーバーサービス</span><span class="sxs-lookup"><span data-stu-id="c53ca-200">Mediation Server Service</span></span></p></td>
<td><p><span data-ttu-id="c53ca-201">通話の読み込みエラーのインデックス = 0</span><span class="sxs-lookup"><span data-stu-id="c53ca-201">Load Call Failure Index = 0</span></span></p>
<p><span data-ttu-id="c53ca-202">プロキシ10のために失敗した通話 &lt;</span><span class="sxs-lookup"><span data-stu-id="c53ca-202">Failed Calls due to Proxy &lt;10</span></span></p>
<p><span data-ttu-id="c53ca-203">ゲートウェイ10のために失敗した通話 &lt;</span><span class="sxs-lookup"><span data-stu-id="c53ca-203">Failed Calls due to Gateway &lt;10</span></span></p>
<p><span data-ttu-id="c53ca-204">通話 (in または out) 拒否 = 0</span><span class="sxs-lookup"><span data-stu-id="c53ca-204">Calls (in or out) rejected = 0</span></span></p>
<p><span data-ttu-id="c53ca-205">メディア候補が見つかりません = 0</span><span class="sxs-lookup"><span data-stu-id="c53ca-205">Media Candidates missing = 0</span></span></p>
<p><span data-ttu-id="c53ca-206">メディア接続の確認エラー = 0</span><span class="sxs-lookup"><span data-stu-id="c53ca-206">Media Connectivity Check Failures = 0</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<span id="Edge"></span>

<div>

## <a name="edge-servers"></a><span data-ttu-id="c53ca-207">エッジ サーバー</span><span class="sxs-lookup"><span data-stu-id="c53ca-207">Edge Servers</span></span>

<span data-ttu-id="c53ca-208">以下の KHI ターゲットは、基本的なコンポーネントの正常性に加えて、エッジサーバーに固有のものです。</span><span class="sxs-lookup"><span data-stu-id="c53ca-208">The following recommended KHI targets are specific to edge servers in addition to basic component health:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c53ca-209">機能領域</span><span class="sxs-lookup"><span data-stu-id="c53ca-209">Functional area</span></span></th>
<th><span data-ttu-id="c53ca-210">目標指標</span><span class="sxs-lookup"><span data-stu-id="c53ca-210">Target Metrics</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c53ca-211">AV Auth</span><span class="sxs-lookup"><span data-stu-id="c53ca-211">AV Auth</span></span></p></td>
<td><p><span data-ttu-id="c53ca-212">不正なリクエスト &lt; 20/秒</span><span class="sxs-lookup"><span data-stu-id="c53ca-212">Bad Requests &lt; 20/sec</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c53ca-213">AV Edge</span><span class="sxs-lookup"><span data-stu-id="c53ca-213">AV Edge</span></span></p></td>
<td><p><span data-ttu-id="c53ca-214">Auth. 失敗率 &lt; 20/秒</span><span class="sxs-lookup"><span data-stu-id="c53ca-214">Auth. Failures &lt;20/sec</span></span></p>
<p><span data-ttu-id="c53ca-215">割り当てエラー &lt; 20/秒</span><span class="sxs-lookup"><span data-stu-id="c53ca-215">Allocation Failures &lt;20/sec</span></span></p>
<p><span data-ttu-id="c53ca-216">パケットドロップ &lt; 300/秒</span><span class="sxs-lookup"><span data-stu-id="c53ca-216">Packets Dropped &lt;300/sec</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c53ca-217">データプロキシ</span><span class="sxs-lookup"><span data-stu-id="c53ca-217">Data Proxy</span></span></p></td>
<td><p><span data-ttu-id="c53ca-218">サーバー接続の調整 &lt; 3</span><span class="sxs-lookup"><span data-stu-id="c53ca-218">Throttled Server connections &lt; 3</span></span></p>
<p><span data-ttu-id="c53ca-219">システムの調整は &lt; 1</span><span class="sxs-lookup"><span data-stu-id="c53ca-219">System is Throttling &lt;1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c53ca-220">SIP スタック</span><span class="sxs-lookup"><span data-stu-id="c53ca-220">SIP Stack</span></span></p></td>
<td><p><span data-ttu-id="c53ca-221">制限を超えた接続は切断されました &lt; 1</span><span class="sxs-lookup"><span data-stu-id="c53ca-221">Connections over limit dropped &lt; 1</span></span></p>
<p><span data-ttu-id="c53ca-222">送信タイムアウト &lt; 10</span><span class="sxs-lookup"><span data-stu-id="c53ca-222">Sends timed out &lt;10</span></span></p>
<p><span data-ttu-id="c53ca-223">フロー制御接続 &lt; 100</span><span class="sxs-lookup"><span data-stu-id="c53ca-223">Flow Controlled Connections &lt;100</span></span></p>
<p><span data-ttu-id="c53ca-224">着信要求が &lt; 1/秒をドロップしました</span><span class="sxs-lookup"><span data-stu-id="c53ca-224">Incoming requests dropped &lt; 1/sec</span></span></p>
<p><span data-ttu-id="c53ca-225">平均メッセージ処理 &lt; 3 秒</span><span class="sxs-lookup"><span data-stu-id="c53ca-225">Avg. Message Processing &lt; 3 sec</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="c53ca-226">関連項目</span><span class="sxs-lookup"><span data-stu-id="c53ca-226">See Also</span></span>


[<span data-ttu-id="c53ca-227">Lync Server ネットワークガイド</span><span class="sxs-lookup"><span data-stu-id="c53ca-227">Lync Server Networking Guide</span></span>](https://go.microsoft.com/fwlink/p/?linkid=390677)  
[<span data-ttu-id="c53ca-228">主要な正常性インジケーター: 正常な Lync サーバーを管理するための基盤</span><span class="sxs-lookup"><span data-stu-id="c53ca-228">Key Health Indicators: The Foundation for Maintaining Healthy Lync Servers</span></span>](https://go.microsoft.com/fwlink/?linkid=391838)  
[<span data-ttu-id="c53ca-229">Lync 通話品質の方法</span><span class="sxs-lookup"><span data-stu-id="c53ca-229">Lync Call Quality Methodology</span></span>](https://go.microsoft.com/fwlink/?linkid=391841)  
  

<span data-ttu-id="c53ca-230"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c53ca-230"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

