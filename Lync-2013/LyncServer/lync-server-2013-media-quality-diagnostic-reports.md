---
title: 'Lync Server 2013: メディア品質診断レポート'
description: 'Lync Server 2013: メディア品質診断レポート。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Media Quality Diagnostic Reports
ms:assetid: ea61428e-a1d5-4189-aae6-3db19ddc5cf2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615044(v=OCS.15)
ms:contentKeyID: 48185935
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2e346d0f9b8997158cb926ad830d5477950e846d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400016"
---
# <a name="media-quality-diagnostic-reports-in-lync-server-2013"></a><span data-ttu-id="d7bc3-103">Lync Server 2013 のメディア品質診断レポート</span><span class="sxs-lookup"><span data-stu-id="d7bc3-103">Media Quality Diagnostic Reports in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d7bc3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d7bc3-104">

<span> </span></span></span>

<span data-ttu-id="d7bc3-105">_**最終更新日:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="d7bc3-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="d7bc3-106">メディア品質診断レポートは、通話の品質についての情報、および失敗した通話についての診断とトラブルシューティングの情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="d7bc3-106">The Media Quality Diagnostic Reports provide information about call quality, and diagnostic and troubleshooting information for failed calls.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="d7bc3-107">このセクション中</span><span class="sxs-lookup"><span data-stu-id="d7bc3-107">In This Section</span></span>

  - <span data-ttu-id="d7bc3-108">[Lync Server 2013 のメディア品質サマリーレポート](lync-server-2013-media-quality-summary-report.md)   エンタープライズボイスピアツーピア通話、エンタープライズボイス会議通話、電話会議 (PSTN) 上の少なくとも一部に依存する通話など、エンドポイントの種類ごとに全体的な品質データを提供します。</span><span class="sxs-lookup"><span data-stu-id="d7bc3-108">[Media Quality Summary Report in Lync Server 2013](lync-server-2013-media-quality-summary-report.md)   Provides overall quality data for different endpoint types, including Enterprise Voice peer-to-peer calls, Enterprise Voice conference calls, and calls that rely, at least in part, on the public switched telephone network (PSTN).</span></span>

  - <span data-ttu-id="d7bc3-109">[Lync Server 2013 のメディア品質比較レポート](lync-server-2013-media-quality-comparison-report.md)   さまざまな種類の音声通話 (ワイヤレスネットワーク経由で発信された通話、有線接続を経由した通話など) について、通話音質の値の比較が提供されます。</span><span class="sxs-lookup"><span data-stu-id="d7bc3-109">[Media Quality Comparison Report in Lync Server 2013](lync-server-2013-media-quality-comparison-report.md)   Provides a comparison of call quality values for different types of audio calls (for example, calls made over a wireless network vs. calls made across a wired connection).</span></span>

  - <span data-ttu-id="d7bc3-110">[Lync server 2013 のサーバーパフォーマンスレポート](lync-server-2013-server-performance-report.md)   パフォーマンスの低下、パケット損失、ジッタなどの主要品質指標の測定値に基づいて、問題が発生したサーバーの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d7bc3-110">[Server Performance Report in Lync Server 2013](lync-server-2013-server-performance-report.md)   Lists the servers that have experienced the most problems, based on measurements of such key quality metrics as degradation, packet loss, and jitter.</span></span>

  - <span data-ttu-id="d7bc3-111">[Lync Server 2013 の場所レポート](lync-server-2013-location-report.md)   ネットワーク上の場所の一覧と、各場所で発生した通話のメディア品質の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="d7bc3-111">[Location Report in Lync Server 2013](lync-server-2013-location-report.md)   Provides a list of network locations and a summary of the media quality of the calls that occur at each location.</span></span> <span data-ttu-id="d7bc3-112">このレポートの目的として、場所は IP サブネットに基づいています。</span><span class="sxs-lookup"><span data-stu-id="d7bc3-112">For purposes of this report, locations are based on IP subnets.</span></span>

  - <span data-ttu-id="d7bc3-113">[Lync Server 2013 のデバイスレポート](lync-server-2013-device-report.md)   エンタープライズ音声通話に使用されるデバイスの概要と、デバイス別の通話の平均メディア品質が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d7bc3-113">[Device Report in Lync Server 2013](lync-server-2013-device-report.md)   Provides a summary of devices that are used for Enterprise Voice calls and it includes the average media quality of the calls by device.</span></span>

  - <span data-ttu-id="d7bc3-114">[Lync Server 2013 の通話リストレポート](lync-server-2013-call-list-report.md)   組織内で発信または受信した電話の詳細情報について説明します。</span><span class="sxs-lookup"><span data-stu-id="d7bc3-114">[Call List Report in Lync Server 2013](lync-server-2013-call-list-report.md)   Provides detailed information about phone calls made or received within your organization.</span></span>

  - <span data-ttu-id="d7bc3-115">[Lync Server 2013 の通話詳細レポート](lync-server-2013-call-detail-report.md)   組織内で発信または受信した電話の詳細について説明します。</span><span class="sxs-lookup"><span data-stu-id="d7bc3-115">[Call Detail Report in Lync Server 2013](lync-server-2013-call-detail-report.md)   Provides detailed information about phone calls made from or received within your organization.</span></span>

  - <span data-ttu-id="d7bc3-116">[Lync server 2013 のサーバーメディア品質トレンドレポート](lync-server-2013-server-media-quality-trend-report.md)   通話音量、低品質の通話割合、パケット損失、ジッタなど、さまざまな品質のエクスペリエンスについて、最大5台のサーバーを視覚的に比較するための手段を提供します。</span><span class="sxs-lookup"><span data-stu-id="d7bc3-116">[Server Media Quality Trend Report in Lync Server 2013](lync-server-2013-server-media-quality-trend-report.md)   Provides a way for you to graphically compare up to 5 servers on Quality of Experience metrics such as call volume, poor call percentage, packet loss, and jitter.</span></span>

  - <span data-ttu-id="d7bc3-117">[Lync Server 2013 でのメディア品質指標の配布レポート](lync-server-2013-media-quality-metrics-distribution-report.md)   ジッタ、パケット損失など、質の高いメトリックの分布値を示すグラフを提供します。</span><span class="sxs-lookup"><span data-stu-id="d7bc3-117">[The Media Quality Metrics Distribution Report in Lync Server 2013](lync-server-2013-media-quality-metrics-distribution-report.md)   Provides a graph that shows the distribution values for a Quality of Experience metric such as jitter or packet loss.</span></span>

  - <span data-ttu-id="d7bc3-118">[Lync Server 2013 の位置情報のトレンドレポート](lync-server-2013-location-trend-report.md)   ネットワーク上の場所の通話品質の傾向情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="d7bc3-118">[Location Trend Report in Lync Server 2013](lync-server-2013-location-trend-report.md)   Provides call quality trend information for network locations.</span></span>

<span data-ttu-id="d7bc3-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d7bc3-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

