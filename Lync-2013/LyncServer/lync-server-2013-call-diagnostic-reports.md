---
title: 'Lync Server 2013: 診断レポートを発信する'
description: 'Lync Server 2013: 診断レポートに通話を発信します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call Diagnostic Reports
ms:assetid: 8d362dd9-a119-4601-a3b4-3e7ed0aaa92e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615013(v=OCS.15)
ms:contentKeyID: 48184794
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6acc41585414e134eebde1635729b470c7f3472c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399410"
---
# <a name="call-diagnostic-reports-in-lync-server-2013"></a><span data-ttu-id="b882b-103">Lync Server 2013 での通話診断レポート</span><span class="sxs-lookup"><span data-stu-id="b882b-103">Call Diagnostic Reports in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b882b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b882b-104">

<span> </span></span></span>

<span data-ttu-id="b882b-105">_**最終更新日:** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="b882b-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="b882b-106">通話診断レポートは、エラーが発生したピアツーピア セッションと電話会議セッションに関する概要情報と診断データを提供します。</span><span class="sxs-lookup"><span data-stu-id="b882b-106">The Call Diagnostic Reports provide summary information and diagnostic data for failed peer-to-peer and conferencing sessions.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="b882b-107">このセクション中</span><span class="sxs-lookup"><span data-stu-id="b882b-107">In This Section</span></span>

  - <span data-ttu-id="b882b-108">[Lync Server 2013 の通話診断サマリーレポート](lync-server-2013-call-diagnostic-summary-report.md)   ピアツーピアセッションと会議セッションの失敗に関する全体的な概要を説明します。</span><span class="sxs-lookup"><span data-stu-id="b882b-108">[Call Diagnostic Summary Report in Lync Server 2013](lync-server-2013-call-diagnostic-summary-report.md)   Provides an overall summary of failed peer-to-peer sessions and conference sessions.</span></span> <span data-ttu-id="b882b-109">ピアツーピアセッションは、2人の参加者に関連するセッションです。</span><span class="sxs-lookup"><span data-stu-id="b882b-109">Peer-to-peer sessions are sessions that involve just two participants.</span></span> <span data-ttu-id="b882b-110">会議セッションには3人以上の参加者が関係します。</span><span class="sxs-lookup"><span data-stu-id="b882b-110">Conferencing sessions involve three or more participants.</span></span>

  - <span data-ttu-id="b882b-111">[Lync Server 2013 のピアツーピアアクティビティ診断レポート](lync-server-2013-peer-to-peer-activity-diagnostic-report.md)   失敗したピアツーピアセッションの全体的な傾向ビューを提供します。</span><span class="sxs-lookup"><span data-stu-id="b882b-111">[Peer-to-Peer Activity Diagnostic Report in Lync Server 2013](lync-server-2013-peer-to-peer-activity-diagnostic-report.md)   Provides an overall trend view of failed peer-to-peer sessions.</span></span> <span data-ttu-id="b882b-112">ピアツーピアセッションには、2人の参加者のみが関係します。</span><span class="sxs-lookup"><span data-stu-id="b882b-112">A peer-to-peer session involves just two participants.</span></span>

  - <span data-ttu-id="b882b-113">[Lync Server 2013 での会議の診断レポート](lync-server-2013-conference-diagnostic-report.md)   失敗した会議セッションと、各会議モードのトレンドビューについての全体的なトレンドビューを提供します。</span><span class="sxs-lookup"><span data-stu-id="b882b-113">[Conference Diagnostic Report in Lync Server 2013](lync-server-2013-conference-diagnostic-report.md)   Provides an overall trend view of failed conferencing sessions and trend views for each conference modality.</span></span> <span data-ttu-id="b882b-114">会議セッションには、少なくとも3人の参加者が関係します。</span><span class="sxs-lookup"><span data-stu-id="b882b-114">Conferencing sessions involve at least three participants.</span></span>

  - <span data-ttu-id="b882b-115">[Lync Server 2013 の上位エラーレポート](lync-server-2013-top-failures-report.md)   最も頻繁に発生するエラーの一覧と、時間の経過に伴う傾向を示します。</span><span class="sxs-lookup"><span data-stu-id="b882b-115">[Top Failures Report in Lync Server 2013](lync-server-2013-top-failures-report.md)   Provides a list of the most frequent failures and their trends over time.</span></span>

  - <span data-ttu-id="b882b-116">[Lync Server 2013 でのエラー配布レポート](lync-server-2013-failure-distribution-report.md)   失敗したセッションの分析を提供します。</span><span class="sxs-lookup"><span data-stu-id="b882b-116">[Failure Distribution Report in Lync Server 2013](lync-server-2013-failure-distribution-report.md)   Provides an analysis of failed sessions.</span></span>

  - <span data-ttu-id="b882b-117">[Lync Server 2013 のエラーリストレポート](lync-server-2013-failure-list-report.md)   失敗した会議に参加している個々の参加者に関する詳細情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="b882b-117">[Failure List Report in Lync Server 2013](lync-server-2013-failure-list-report.md)   Provides detailed information about the individual participants involved in a failed conference.</span></span>

  - <span data-ttu-id="b882b-118">[Lync Server 2013 の診断レポート](lync-server-2013-diagnostic-report.md)   失敗したセッションの診断とトラブルシューティングの情報 (SIP 応答コード、診断ヘッダー、IDs など) について説明します。</span><span class="sxs-lookup"><span data-stu-id="b882b-118">[Diagnostic Report in Lync Server 2013](lync-server-2013-diagnostic-report.md)   Provides diagnostic and troubleshooting information (including SIP response codes and diagnostic headers and IDs) for failed sessions.</span></span>

<span data-ttu-id="b882b-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b882b-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

