---
title: 'Lync Server 2013: ポスター: Lync 通話品質の方法'
description: 'Lync Server 2013: ポスター: Lync 通話品質の方法論。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: 'Poster: Lync Call Quality Methodology'
ms:assetid: a069f4e5-4f80-4f0f-8657-2e07276b6b41
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn593600(v=OCS.15)
ms:contentKeyID: 61084874
ms.date: 06/24/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0db34da35ce32d32aa00f10cd3523a0f508f8ffd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446347"
---
# <a name="lync-call-quality-methodology-in-lync-server-2013"></a><span data-ttu-id="f03a9-103">Lync Server 2013 での lync 通話品質の方法</span><span class="sxs-lookup"><span data-stu-id="f03a9-103">Lync Call Quality Methodology in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f03a9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f03a9-104">

<span> </span></span></span>

<span data-ttu-id="f03a9-105">_**最終更新日:** 2016-06-24_</span><span class="sxs-lookup"><span data-stu-id="f03a9-105">_**Topic Last Modified:** 2016-06-24_</span></span>

<span data-ttu-id="f03a9-106">この記事は、 [Lync 通話品質の方法](https://go.microsoft.com/fwlink/?linkid=391841) のポスターに対応しており、ダウンロードセンターからダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="f03a9-106">This article is a companion to the [Lync Call Quality Methodology](https://go.microsoft.com/fwlink/?linkid=391841) poster, which you can download from the Download Center.</span></span>

<span data-ttu-id="f03a9-107">![CQM プロセスについて説明するポスター](images/Dn594589.d239e04a-1c3b-4f0e-93af-88b85198615a(OCS.15).jpg "CQM プロセスについて説明するポスター")</span><span class="sxs-lookup"><span data-stu-id="f03a9-107">![Poster describing the CQM process](images/Dn594589.d239e04a-1c3b-4f0e-93af-88b85198615a(OCS.15).jpg "Poster describing the CQM process")</span></span>

<span data-ttu-id="f03a9-108">このポスターを使って、エンタープライズ voip 機能を含む Lync の実装での通話品質とユーザーエクスペリエンスに影響する問題を見つけて解決するのに役立つ、CQM、Lync 2013 および2010の通話品質の方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-108">You can use this poster to learn about CQM, the Call Quality Methodology for Lync 2013 and 2010 that helps you find and eliminate issues affecting call quality and user experience for Lync implementations that include enterprise voice features.</span></span> <span data-ttu-id="f03a9-109">通話品質の方法論は、Lync のエンタープライズ voip サービスの向上に役立つ、新しいトラブルシューティングとサービス管理フレームワークです。</span><span class="sxs-lookup"><span data-stu-id="f03a9-109">Call Quality Methodology is a new troubleshooting and service management framework that can better focus efforts to improve enterprise voice services in Lync.</span></span> <span data-ttu-id="f03a9-110">この記事では、CQM、監視対象のサーバーとソリューションの種類、収集されたテレメトリデータについて詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-110">In this article, you can learn more about CQM, the kinds of servers and solutions that are monitored, and what to do with the collected telemetry data.</span></span>

<span data-ttu-id="f03a9-111">CQM の使い方について質問がある場合は、cqmfeedback@microsoft.com に質問を送信できます。</span><span class="sxs-lookup"><span data-stu-id="f03a9-111">If you have questions about how to use CQM, you can submit your questions to cqmfeedback@microsoft.com.</span></span>

<span data-ttu-id="f03a9-112">このポスターでは、次の領域について説明します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-112">The poster explains the following areas:</span></span>

  - <span data-ttu-id="f03a9-113">Lync CQM とは何ですか?</span><span class="sxs-lookup"><span data-stu-id="f03a9-113">What is Lync CQM?</span></span>

  - <span data-ttu-id="f03a9-114">優先度: トレンド分析クエリを実行する</span><span class="sxs-lookup"><span data-stu-id="f03a9-114">Prioritize: Run Trending Queries</span></span>

  - <span data-ttu-id="f03a9-115">PCD</span><span class="sxs-lookup"><span data-stu-id="f03a9-115">PCD</span></span>

  - <span data-ttu-id="f03a9-116">管理/非管理</span><span class="sxs-lookup"><span data-stu-id="f03a9-116">Managed/Unmanaged</span></span>

  - <span data-ttu-id="f03a9-117">サーバープラントの交通</span><span class="sxs-lookup"><span data-stu-id="f03a9-117">The Server Plant Road</span></span>

  - <span data-ttu-id="f03a9-118">最終マイルの道路</span><span class="sxs-lookup"><span data-stu-id="f03a9-118">The Last Mile Road</span></span>

  - <span data-ttu-id="f03a9-119">エンドポイントの道路</span><span class="sxs-lookup"><span data-stu-id="f03a9-119">The End Points Road</span></span>

  - <span data-ttu-id="f03a9-120">サービス管理</span><span class="sxs-lookup"><span data-stu-id="f03a9-120">Service Management</span></span>

  - <span data-ttu-id="f03a9-121">ボードゲームのルール</span><span class="sxs-lookup"><span data-stu-id="f03a9-121">Board Game Rules</span></span>

<span id="WhatIs"></span>

<div>

## <a name="what-is-lync-cqm"></a><span data-ttu-id="f03a9-122">Lync CQM とは何ですか?</span><span class="sxs-lookup"><span data-stu-id="f03a9-122">What is Lync CQM?</span></span>

<span data-ttu-id="f03a9-123">通話品質の方法論は、Lync のエンタープライズ voip サービスの向上に役立つ、新しいトラブルシューティングとサービス管理フレームワークです。</span><span class="sxs-lookup"><span data-stu-id="f03a9-123">Call Quality Methodology is a new troubleshooting and service management framework that can better focus efforts to improve enterprise voice services in Lync.</span></span> <span data-ttu-id="f03a9-124">CQM を使用する場合は、エンタープライズ voip サービスの品質とユーザーの満足度を確保するために、労力を節約する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f03a9-124">When you use CQM, less effort is needed to assure call quality and user satisfaction for enterprise voice services.</span></span> <span data-ttu-id="f03a9-125">CQM の詳細については、 [通話品質の方法](https://go.microsoft.com/fwlink/p/?linkid=615208)で詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-125">CQM is more fully explained in the [Call Quality Methodology](https://go.microsoft.com/fwlink/p/?linkid=615208).</span></span> <span data-ttu-id="f03a9-126">この記事とポスターには、その内容の概要が記載されています。</span><span class="sxs-lookup"><span data-stu-id="f03a9-126">This article and the poster are summaries of that content.</span></span>

<span data-ttu-id="f03a9-127">CQM は、システムのトラブルシューティングを3つのパスまたは "道路" に分割します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-127">CQM breaks down System troubleshooting into three paths or “Roads.”</span></span> <span data-ttu-id="f03a9-128">次のような機能があります。サーバーと、それらの間のリンク、および通話の発信に使用されたユーザーデバイスとメディアを参照するエンドポイントのロード、および従来の電話網かけとの統合について説明する、最終マイルの道路です。</span><span class="sxs-lookup"><span data-stu-id="f03a9-128">These are: the Server Plant Road, which looks at the servers and the links between them, the End Points Road, which looks at user devices and media used to carry calls, and the Last Mile Road, which addresses integration of traditional switched telephone network calls.</span></span>

<span data-ttu-id="f03a9-129">各道路は、特定の領域またはトピックに関連するいくつかのセグメントに分けられます。各セグメントの定義では、どのような品質レベルを実現するために実行され、その品質レベルを実現するために、サービス管理計画がその品質レベルを維持するために用意されています。</span><span class="sxs-lookup"><span data-stu-id="f03a9-129">Each Road is divided into several segments relating to a specific area or topic, and at each segment definitions are made about what is an acceptable quality level, actions are taken to achieve that quality level, and a service management plan is put in place to maintain that quality level before moving on to the next topic.</span></span>

<span data-ttu-id="f03a9-130">このポスターは、Lync CQM を3人のボードゲームとして表示します。各参加者は、いずれかの道路を通過します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-130">The poster presents Lync CQM as a board game for three players, each of whom will go through one of the roads.</span></span> <span data-ttu-id="f03a9-131">ダウンロードに含まれているカードは、通話品質の障害をシミュレートするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="f03a9-131">Cards included with the download are used to simulate impediments to call quality that must be overcome.</span></span> <span data-ttu-id="f03a9-132">ターゲットに関するヒントと提案、およびそれらを実現する方法については、3つのパスに加えて、実際のアプリケーション (ゲームでは、3つのすべての道路が並列で対応する) の優先順位ガイドラインについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-132">Hints and suggestions about targets and how to achieve them are included along the three paths, as well as prioritization guidelines for which road to pursue first in actual applications (in the game, all three roads are addressed in parallel).</span></span>

<span data-ttu-id="f03a9-133">以前のバージョンの Lync では、CQM はどのように動作しますか?</span><span class="sxs-lookup"><span data-stu-id="f03a9-133">How does CQM work in earlier versions of Lync?</span></span> <span data-ttu-id="f03a9-134">CQM は Lync 2013 で新しくなっていますが、ほとんどは Lync 2010 で使用するために調整できます。</span><span class="sxs-lookup"><span data-stu-id="f03a9-134">CQM is new for Lync 2013, but most of it can be adapted to be used with Lync 2010.</span></span> <span data-ttu-id="f03a9-135">CQM は Microsoft Office Communicator で動作する可能性がありますが、これは未テストであり、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="f03a9-135">CQM may work to a degree with Microsoft Office Communicator, but this is untested and not supported.</span></span>

<span data-ttu-id="f03a9-136">CQM の使い方について質問がある場合は、cqmfeedback@microsoft.com に質問を送信できます。</span><span class="sxs-lookup"><span data-stu-id="f03a9-136">If you have questions about how to use CQM, you can submit your questions to cqmfeedback@microsoft.com.</span></span>

</div>

<span id="Trending"></span>

<div>

## <a name="prioritize-run-trending-queries"></a><span data-ttu-id="f03a9-137">優先度: トレンド分析クエリを実行する</span><span class="sxs-lookup"><span data-stu-id="f03a9-137">Prioritize: Run Trending Queries</span></span>

<span data-ttu-id="f03a9-138">CQM の最初の手順では、2週間の各トレンドクエリを実行して、結果を分析します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-138">The first step in CQM is to run each of the trending queries for two weeks and then analyze the results.</span></span> <span data-ttu-id="f03a9-139">最大のストリーム作成者、低品質のストリーム比率、管理領域 (制御しているもの) によって、是正措置の優先順位を設定します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-139">Prioritize corrective action by the largest stream contributor, the highest poor stream ratio, and managed areas (ones you control).</span></span>  <span data-ttu-id="f03a9-140">オーディオ/ビデオのマルチポイントコントロールユニット (AV MCU) または仲介クエリで、不適切な結果が表示される場合は、赤またはサーバーのプラントでの交通を開始します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-140">If the Audio/Video Multi-point Control Unit (AV MCU) or Mediation queries show poor results, start on the Red or Server Plant road.</span></span>  <span data-ttu-id="f03a9-141">有線またはワイヤレスのクエリで低品質の結果が表示される場合は、青色または最終マイルの道路を開始します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-141">If the Wired or Wireless queries show poor results, start on the Blue or Last Mile road.</span></span>  <span data-ttu-id="f03a9-142">VPN または外部のクエリの結果が不十分な場合は、緑または終点の道路で開始します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-142">If the VPN or External queries show poor results, start on the Green or End Points road.</span></span>

<span data-ttu-id="f03a9-143">開始する道路を選択した後、各領域のターゲットを定義し (Assert)、そのターゲットに対応するための作業を行い (達成)、目的の場所に維持するための手順を実装します (維持)。</span><span class="sxs-lookup"><span data-stu-id="f03a9-143">After you choose a road to start with, define a target for each area (Assert), work to meet that target (Achieve) and then implement procedures to stay on target (Maintain).</span></span> <span data-ttu-id="f03a9-144">CQM の背後の原則を理解するために、このポスターをゲームとして使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="f03a9-144">You can also use this poster as a game to understand the principles behind CQM.</span></span>

</div>

<span id="PCD"></span>

<div>

## <a name="pcd"></a><span data-ttu-id="f03a9-145">PCD</span><span class="sxs-lookup"><span data-stu-id="f03a9-145">PCD</span></span>

<span data-ttu-id="f03a9-146">すべての PreCall ツール (PCD) は、境界ネットワーク内の問題を特定して診断するのに役立ちます (QoE データベースはエッジまたは境界ネットワーク上の情報を収集しません)。また、最終マイルの接続のトラブルシューティングを行うこともできます。</span><span class="sxs-lookup"><span data-stu-id="f03a9-146">The PreCall Diagnostics tool (PCD) will help you identify and diagnose problems in your perimeter network (the QoE database doesn’t collect information on your edge or perimeter network) and also to troubleshoot connections in the Last Mile.</span></span> <span data-ttu-id="f03a9-147">このツールは、Windows 8 のモダンアプリまたは Windows デスクトップアプリの両方として使用でき https://apps.microsoft.com/windows/en-us/app/lync-2013-precall-diagnostics/9607fe33-2b51-403d-9615-c23f248e7c88 ます。</span><span class="sxs-lookup"><span data-stu-id="f03a9-147">The tool is available as both a Windows 8 Modern App or a Windows Desktop App at https://apps.microsoft.com/windows/en-us/app/lync-2013-precall-diagnostics/9607fe33-2b51-403d-9615-c23f248e7c88.</span></span>

</div>

<span id="ManagedUn"></span>

<div>

## <a name="managedunmanaged"></a><span data-ttu-id="f03a9-148">管理/非管理</span><span class="sxs-lookup"><span data-stu-id="f03a9-148">Managed/Unmanaged</span></span>

<span data-ttu-id="f03a9-149">通常、Lync Server の展開とネットワークインフラストラクチャは、管理と非管理のスペースに分けることができます。</span><span class="sxs-lookup"><span data-stu-id="f03a9-149">The Lync Server deployment and network infrastructure can usually be divided into managed and unmanaged spaces.</span></span> <span data-ttu-id="f03a9-150">管理スペースには、内部の有線ネットワークとサーバーインフラストラクチャ全体が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f03a9-150">The managed space includes your entire inside wired network and server infrastructure.</span></span> <span data-ttu-id="f03a9-151">このアンマネージ空間は、ワイヤレスインフラストラクチャと外部ネットワークインフラストラクチャです。</span><span class="sxs-lookup"><span data-stu-id="f03a9-151">The unmanaged space is the wireless infrastructure and the outside network infrastructure.</span></span>

<span data-ttu-id="f03a9-152">この区別を付けることで、データをより明確にすることができ、ユーザーの音声とビデオの品質に大きな影響を与えるワークロードに組織が集中するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="f03a9-152">Making this distinction increases the clarity of your data and helps your organization focus on workloads that will have a measurable impact on your users’ voice and video quality.</span></span> <span data-ttu-id="f03a9-153">ユーザーは、自分が所有するインフラストラクチャ (管理されている) と、他の一部のエンティティ (管理されていない) の管理下にあるインフラストラクチャとの間で、異なる品質を期待できます。</span><span class="sxs-lookup"><span data-stu-id="f03a9-153">Users have a different expectation of quality if the call is placed on infrastructure that you own (managed) versus infrastructure that is partly under the control of some other entity (unmanaged).</span></span> <span data-ttu-id="f03a9-154">これは、ワイヤレスユーザーが Lync Server の優れたエクスペリエンスを実現するために、独自のデバイスに残されていることを示すものではありません。</span><span class="sxs-lookup"><span data-stu-id="f03a9-154">This is not to say that wireless users are left to their own devices to have excellent Lync Server experiences.</span></span>

<span data-ttu-id="f03a9-155">音声認識の品質を向上させるには、管理スペースの品質を高める必要があります。</span><span class="sxs-lookup"><span data-stu-id="f03a9-155">Improving voice quality in the unmanaged space requires you to have high quality in the managed space.</span></span> <span data-ttu-id="f03a9-156">ワイヤレス (Wi-fi) が管理されていると見なされるかどうかは、組織によって異なります。</span><span class="sxs-lookup"><span data-stu-id="f03a9-156">Whether wireless (Wi-Fi) is considered managed or unmanaged space is up to your organization.</span></span> <span data-ttu-id="f03a9-157">正常な環境を実現するための手法は、解決策と同じように、2つのスペースとは異なります。</span><span class="sxs-lookup"><span data-stu-id="f03a9-157">The techniques to achieve a healthy environment are different in the two spaces, as are the solutions.</span></span>

</div>

<span id="ServRd"></span>

<div>

## <a name="the-server-plant-road"></a><span data-ttu-id="f03a9-158">サーバープラントの交通</span><span class="sxs-lookup"><span data-stu-id="f03a9-158">The Server Plant Road</span></span>

<span data-ttu-id="f03a9-159">サーバープラントロードのセグメント1では、Lync の実装で実際のサーバーに対応しています。</span><span class="sxs-lookup"><span data-stu-id="f03a9-159">Segment 1 of the Server Plant Road addresses the actual servers in the Lync implementation.</span></span> <span data-ttu-id="f03a9-160">実装でサーバー自体とその役割の両方に関する KHI データを収集し、結果を分析します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-160">Gather KHI data regarding both the server itself and its role in the implementation and analyze the result.</span></span> <span data-ttu-id="f03a9-161">動作が保証されている場合は、検出された問題を修正します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-161">If action is warranted, correct any problems found.</span></span> <span data-ttu-id="f03a9-162">このトピックについて詳しくは、「KHI ポスターに付属する [Lync Server 2013 の主要な正常性インジケーター](lync-server-2013-poster-key-health-indicators.md) について」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="f03a9-162">More detail on this topic is presented in the article about [Key Health Indicators in Lync Server 2013](lync-server-2013-poster-key-health-indicators.md) that accompanies the KHI poster.</span></span>

<span data-ttu-id="f03a9-163">次のセグメントは、AV MCU サーバーと仲介サーバーの間でメディアストリームを解決します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-163">The next segment addresses media streams between the AV MCU server and mediation server.</span></span> <span data-ttu-id="f03a9-164">まず、不適切なストリームのしきい値のターゲットを特定します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-164">Begin by determining your targets for poor stream thresholds.</span></span> <span data-ttu-id="f03a9-165">不適切なストリームは、通常は PacketLossRate \> .01 または PacketLossRateMax \> です。</span><span class="sxs-lookup"><span data-stu-id="f03a9-165">Poor streams are usually PacketLossRate \> .01 or PacketLossRateMax \> .05.</span></span> <span data-ttu-id="f03a9-166">もう1つの望ましいターゲットは PoorStreamsRatio \< 2% です。</span><span class="sxs-lookup"><span data-stu-id="f03a9-166">Another desirable target is PoorStreamsRatio \< 2%.</span></span> <span data-ttu-id="f03a9-167">次に、詳細なクエリを使用して、不十分なストリームで AVMCU と仲介サーバーのペアを探し、不十分なストリームの原因を調査し、不十分なストリームパスのネットワーク機器を確認し、不十分なストリームの修復を行い、ネットワーク機器の最適な設定または "ゴールド" を定義します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-167">Next, use detailed queries to find AVMCU and Mediation server pairs with poor streams, investigate the cause of poor streams, look at network equipment in the poor stream paths, remediate poor streams, and define optimal or “gold” configuration for network equipment.</span></span> <span data-ttu-id="f03a9-168">アチーブメントを維持するために、プロセスとツールを実装して、構成のドリフトを管理し、新しい問題領域を報告します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-168">To maintain your achievement, implement processes and tools to manage configuration drift and to report new problem areas.</span></span>

<span data-ttu-id="f03a9-169">次に、仲介サーバーと公衆交換電話網 (PSTN) ゲートウェイ間のメディアストリームを調べます。</span><span class="sxs-lookup"><span data-stu-id="f03a9-169">Next, examine the media streams between the Mediation server and the Public Switched Telephone Network (PSTN) gateway.</span></span> <span data-ttu-id="f03a9-170">まず、不適切なストリームのしきい値のターゲットを特定します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-170">Begin by determining your targets for poor stream thresholds.</span></span> <span data-ttu-id="f03a9-171">不適切なストリームは、通常は PacketLossRate \> .01 または PacketLossRateMax \> です。</span><span class="sxs-lookup"><span data-stu-id="f03a9-171">Poor streams are usually PacketLossRate \> .01 or PacketLossRateMax \> .05.</span></span> <span data-ttu-id="f03a9-172">もう1つの望ましいターゲットは PoorStreamsRatio \< 2% です。</span><span class="sxs-lookup"><span data-stu-id="f03a9-172">Another desirable target is PoorStreamsRatio \< 2%.</span></span> <span data-ttu-id="f03a9-173">次に、詳細なクエリを使用して、不十分なストリームで仲介サーバーとゲートウェイのペアを探し、不十分なストリームの原因を調査し、低品質のストリームパスのネットワーク機器を確認し、不十分なストリームの修復を行い、ネットワーク機器の最適な設定または "ゴールド" を定義します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-173">Next, use detailed queries to find Mediation server and gateway pairs with poor streams, investigate the cause of poor streams, look at network equipment in the poor stream paths, remediate poor streams, and define optimal or “gold” configuration for network equipment.</span></span> <span data-ttu-id="f03a9-174">アチーブメントを維持するために、プロセスとツールを実装して、構成のドリフトを管理し、新しい問題領域を報告します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-174">To maintain your achievement, implement processes and tools to manage configuration drift and to report new problem areas.</span></span>

<span data-ttu-id="f03a9-175">最後に、PSTN ゲートウェイの正常性メトリックを調べます。</span><span class="sxs-lookup"><span data-stu-id="f03a9-175">Finally, examine the health metrics for your PSTN gateway.</span></span> <span data-ttu-id="f03a9-176">状態を表示し、それに対してターゲットを定義する統計情報を特定します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-176">Identify the statistics that show health and define targets against them.</span></span> <span data-ttu-id="f03a9-177">ここでは、さまざまなゲートウェイを使用できるため、特定のガイダンスは提供されていません。</span><span class="sxs-lookup"><span data-stu-id="f03a9-177">No specific guidance is provided here as many possible gateways can be used.</span></span> <span data-ttu-id="f03a9-178">ターゲットを確立したら、ターゲットを達成するために必要に応じて修復します。このプロセスでは、ゲートウェイの "ゴールド" または最適な構成を定義する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f03a9-178">Once targets are established, remediate as needed to achieve the target; in the process you will likely define a “gold” or optimal configuration for the gateway.</span></span> <span data-ttu-id="f03a9-179">アチーブメントを維持するために、プロセスとツールを実装して、構成のドリフトを管理し、新しい問題領域を報告します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-179">To maintain your achievement, implement processes and tools to manage configuration drift and to report new problem areas.</span></span> <span data-ttu-id="f03a9-180">ファームウェアとソフトウェアの更新によって構成が変更される可能性があるため、または "ゴールド" 構成の定義を変更する場合は、これらのアクティビティについて慎重に対処してください。</span><span class="sxs-lookup"><span data-stu-id="f03a9-180">Be aware that firmware and software updates may alter your configuration or lead you to change the definition of the “gold” configuration, so approach these activities with care.</span></span>

</div>

<span id="LastMi"></span>

<div>

## <a name="the-last-mile-road"></a><span data-ttu-id="f03a9-181">最終マイルの道路</span><span class="sxs-lookup"><span data-stu-id="f03a9-181">The Last Mile Road</span></span>

<span data-ttu-id="f03a9-182">クライアントがネットワークに接続する2つの方法のうち、有線は最高品質を実現することが求められます。これは、第1マイルの問題に対する最初の焦点となる必要があります。</span><span class="sxs-lookup"><span data-stu-id="f03a9-182">Of the two ways clients connect to the network, wired is expected to deliver the highest quality and correspondingly this must be your initial focus for last mile issues.</span></span> <span data-ttu-id="f03a9-183">CQM ワイヤードクエリ (LastMile \_ 0 \_ ワイヤード) と、提供されている不十分なストリーム比データを使います。</span><span class="sxs-lookup"><span data-stu-id="f03a9-183">Use the CQM Wired query (LastMile\_0\_Wired) and the Poor Streams ratio data it provides.</span></span> <span data-ttu-id="f03a9-184">ターゲット PoorStreamsRatio 300 ストリームを定義することをお勧め \< 5% for sites with \> します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-184">We suggest defining a target PoorStreamsRatio \< 5% for sites with \> 300 streams).</span></span> <span data-ttu-id="f03a9-185">ターゲットを達成するには、最低レベルから最高のサブネットを修復し、QoS を実装します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-185">To achieve your targets, remediate subnets ordered from worst to best, and implement QoS.</span></span>

<span data-ttu-id="f03a9-186">有線接続の品質を最適化すると、ワイヤレスインフラストラクチャはそれぞれの場所で有線コアの上にあるため、ワイヤレスの品質を向上させることが簡単になります。</span><span class="sxs-lookup"><span data-stu-id="f03a9-186">After you optimize the quality of your wired connections, improving wireless quality becomes easier because the wireless infrastructure sits atop the wired core at each location.</span></span> <span data-ttu-id="f03a9-187">適切な有線品質を備えたサイトのワイヤレスストリームの品質が低い場合は、特定のワイヤレスコンポーネントの属性を持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="f03a9-187">Poor wireless streams in a site with good wired quality must be attributed to the specific wireless components.</span></span> <span data-ttu-id="f03a9-188">CQM ワイヤレスクエリ (LastMile \_ 1 \_ ワイヤレス) は、日付範囲に基づいて処理され、会議サーバーまたは仲介サーバーのいずれかから、またはその両方から、環境内のすべての内部ワイヤレスストリームを返します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-188">The CQM Wireless query (LastMile\_1\_Wireless) operates on a date range and will return all internal wireless streams in your environment from Lync clients to or from either conferencing servers or mediation servers.</span></span> <span data-ttu-id="f03a9-189">ターゲット PoorStreamsRatio 300 ストリームを定義することをお勧め \< 5% for sites with \> します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-189">We suggest defining a target PoorStreamsRatio \< 5% for sites with \> 300 streams).</span></span> <span data-ttu-id="f03a9-190">ターゲットを達成するには、最低レベルから最高のサブネットを修復し、QoS を実装します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-190">To achieve your targets, remediate subnets ordered from worst to best, and implement QoS.</span></span>

</div>

<span id="EndPt"></span>

<div>

## <a name="the-end-points-road"></a><span data-ttu-id="f03a9-191">エンドポイントの道路</span><span class="sxs-lookup"><span data-stu-id="f03a9-191">The End Points Road</span></span>

<span data-ttu-id="f03a9-192">ヘッドセットやその他のデバイスを使って、Lync と共に使用するときに品質を向上させることがわかっているエンドポイントの道路への照会を開始します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-192">Begin inquiries into the End Points Road with the headsets and other devices known to produce acceptable quality when used with Lync.</span></span> <span data-ttu-id="f03a9-193">\>100 以上のストリームを使った実装には、Target AVGSENDLISTEN MOS 3.6 をお勧めします。)問題が発生したデバイスを特定して修正または交換して、目標を達成します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-193">We suggest a target AvgSendListen MOS \> 3.6 for implementations with over 100 streams.) Achieve the target by identifying problematic devices and fix or replace them.</span></span>

<span data-ttu-id="f03a9-194">次に、エンドユーザーの通話のためにオーディオを処理しているデバイスまたは PC を調べます。</span><span class="sxs-lookup"><span data-stu-id="f03a9-194">Next, examine the device or PC processing the audio for end user calls.</span></span> <span data-ttu-id="f03a9-195">推奨されるターゲット品質メトリックは、AudioMicGlitchRate \< = 1 です。</span><span class="sxs-lookup"><span data-stu-id="f03a9-195">A suggested target quality metric is an AudioMicGlitchRate \<= 1.</span></span> <span data-ttu-id="f03a9-196">ユーザーシステムに最適なシステム構成を特定するときは、ドライババージョンなどの "ゴールデン" PC 構成を定義します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-196">As you identify optimal system configurations for the user systems, define a “golden” PC configuration including driver versions.</span></span>

<span data-ttu-id="f03a9-197">オーディオストリームが Lync エンドポイントシステムから受け取るネットワークパスを確認します。これにより、音質が低下する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f03a9-197">Now examine the network path an audio stream takes from a Lync endpoint system, which can cause poor audio quality.</span></span> <span data-ttu-id="f03a9-198">オーディオが VPN 接続を介して転送されると、遅延の問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f03a9-198">If audio travels over a VPN connection you might see latency issues.</span></span> <span data-ttu-id="f03a9-199">内部の Lync クライアントが、2パーティまたはピアツーピアの通話のために、別の内部 Lync クライアントに直接メディアストリームを確立できない場合は、Lync Edge サーバー経由で中継するパスに戻り、遅延とジッタの可能性を高めることができます。</span><span class="sxs-lookup"><span data-stu-id="f03a9-199">If an internal Lync client cannot establish a direct media stream to another internal Lync client for a two-party or peer-to-peer call, it will fall back to a path that relays through a Lync Edge server, again leading to latency issues as well as increased potential for loss and jitter.</span></span> <span data-ttu-id="f03a9-200">VPN 経由で、0% のメディアの品質メトリックを定義することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f03a9-200">We suggest you define a quality metric of 0% Media over VPN.</span></span> <span data-ttu-id="f03a9-201">設定したターゲットを実現するために修復するときに、問題のサブネットを特定し、ファイアウォールルール、パケットコントローラー、その他の関連するネットワーク機器構成を調査します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-201">As you remediate to achieve the target you set, identify problem subnets and investigate firewall rules, packet shapers, and other relevant network equipment configuration.</span></span>

<span data-ttu-id="f03a9-202">IP パケットでは、伝送制御プロトコル (TCP) またはユーザーデータグラムプロトコル (UDP) を使うことができます。</span><span class="sxs-lookup"><span data-stu-id="f03a9-202">IP Packets can use either Transmission Control Protocol (TCP) or User Datagram Protocol (UDP).</span></span> <span data-ttu-id="f03a9-203">TCP はデータストリームに最適です。</span><span class="sxs-lookup"><span data-stu-id="f03a9-203">TCP is optimal for data streams.</span></span> <span data-ttu-id="f03a9-204">UDP はコネクションレス型であり、TCP 回復メカニズムではリアルタイムメディアの損失を解決できないため、メディアの方が効率的です。</span><span class="sxs-lookup"><span data-stu-id="f03a9-204">UDP is connectionless and is more efficient for media since TCP recovery mechanisms cannot address loss in real time media.</span></span> <span data-ttu-id="f03a9-205">Lync では常に UDP が優先されますが、UDP セッションを確立できない場合は TCP に戻ります。</span><span class="sxs-lookup"><span data-stu-id="f03a9-205">Lync always prefers UDP, but will revert to TCP if a UDP session cannot be established.</span></span> <span data-ttu-id="f03a9-206">TCP 経由のメディアセッションでは、UDP よりも音質が低下します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-206">Media sessions over TCP will exhibit poorer quality than over UDP.</span></span> <span data-ttu-id="f03a9-207">TCP 経由の接続の品質定義は、0% にすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f03a9-207">We recommend a quality definition of 0% connections over TCP.</span></span> <span data-ttu-id="f03a9-208">設定したターゲットを実現するために修復するときに、問題のサブネットを特定し、ファイアウォールルール、パケットコントローラー、その他の関連するネットワーク機器構成を調査します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-208">As you remediate to achieve the target you set, identify problem subnets and investigate firewall rules, packet shapers, and other relevant network equipment configuration.</span></span>

</div>

<span id="ServMgt"></span>

<div>

## <a name="service-management"></a><span data-ttu-id="f03a9-209">サービス管理</span><span class="sxs-lookup"><span data-stu-id="f03a9-209">Service Management</span></span>

<span data-ttu-id="f03a9-210">サービス管理は、CQM の終了状態であり、3本すべての道路の目的地です。</span><span class="sxs-lookup"><span data-stu-id="f03a9-210">Service management is the end state of CQM, and the destination for all three roads.</span></span> <span data-ttu-id="f03a9-211">高レベルの通話品質を維持するには、次の領域を監視します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-211">To maintain high levels of call quality, monitor these areas:</span></span>

1.  <span data-ttu-id="f03a9-212">**ユーザー** -改善活動は、ユーザーの満足度を向上させることができます。</span><span class="sxs-lookup"><span data-stu-id="f03a9-212">**Users** - Remediation activities should show a measurable increase in user satisfaction.</span></span> <span data-ttu-id="f03a9-213">これは、問題のチケットやその他のフィードバックメカニズムによって測定できます。</span><span class="sxs-lookup"><span data-stu-id="f03a9-213">You can measure this by problem tickets or other feedback mechanisms.</span></span> <span data-ttu-id="f03a9-214">品質指標を公開することもできます。</span><span class="sxs-lookup"><span data-stu-id="f03a9-214">You can also publish quality metrics.</span></span>

2.  <span data-ttu-id="f03a9-215">**プロセス** -デイリー、weekly、毎月のプロセスを operationalize cqm に定義します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-215">**Process** - define daily, weekly and monthly processes to operationalize CQM.</span></span> <span data-ttu-id="f03a9-216">を修復する (毎日) では、一定の間隔で再生が開始され、安定したら低い周波数 (月間) に移動します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-216">Monitoring rhythm starts at a higher frequency while you are remediating (daily) and moves to a lower frequency (monthly) as you stabilize.</span></span>

3.  <span data-ttu-id="f03a9-217">**ツール** -測定と修復の両方のツールを識別します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-217">**Tools** - identify tools to both measure and remediate.</span></span> <span data-ttu-id="f03a9-218">プロセスをサポートするために、CQM クエリの実行を自動化した方が便利な場合があります。</span><span class="sxs-lookup"><span data-stu-id="f03a9-218">You may find it useful to automate running the CQM queries to support your processes.</span></span> <span data-ttu-id="f03a9-219">場合によっては、ネットワーク要素に標準化された構成を適用したり、不適切なストリームで損失をトラブルシューティングしたりするために、その他のツールが必要になる</span><span class="sxs-lookup"><span data-stu-id="f03a9-219">Remediation may require additional tools for example to enforce standardized configurations on network elements or troubleshooting loss in poor streams.</span></span>

</div>

<span id="BoardGm"></span>

<div>

## <a name="board-game-rules"></a><span data-ttu-id="f03a9-220">ボードゲームのルール</span><span class="sxs-lookup"><span data-stu-id="f03a9-220">Board Game Rules</span></span>

<span data-ttu-id="f03a9-221">このポスターは、CQM 実装への参照として使うか、またはゲームとして使用して概念を練習することができます。</span><span class="sxs-lookup"><span data-stu-id="f03a9-221">You can use this poster either as a reference to a CQM implementation or as a game to practice the concepts.</span></span> <span data-ttu-id="f03a9-222">プレイするには、1 6 サイドとそのカードが必要です。</span><span class="sxs-lookup"><span data-stu-id="f03a9-222">To play, you will need one six-sided die and the cards provided.</span></span> <span data-ttu-id="f03a9-223">このカードのダウンロード可能なバージョンは、標準の Avery 5871 名刺に印刷できます。</span><span class="sxs-lookup"><span data-stu-id="f03a9-223">A downloadable version of the cards is available to print on standard Avery 5871 business cards.</span></span>

<span data-ttu-id="f03a9-224">ゲームは3人のプレーヤーを対象としています。</span><span class="sxs-lookup"><span data-stu-id="f03a9-224">The game is for 3 players.</span></span> <span data-ttu-id="f03a9-225">目的の品質を実現し、センターサービス管理の状態 (サーバープラント、エンドポイント、最終マイル) に達するには、次の3つのパスを使用できます。</span><span class="sxs-lookup"><span data-stu-id="f03a9-225">There are three paths the players can use to achieve the desired quality and reach the center Service Management state: Server Plant, End Point, and Last Mile.</span></span> <span data-ttu-id="f03a9-226">各パスは、品質目標のアサート、目標の達成、システムの側面の維持のために、停止します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-226">Each path has stops along the way where you Assert quality targets, Achieve goals, and Maintain an aspect of your system.</span></span> <span data-ttu-id="f03a9-227">上の指示された領域にカードを配置し、5枚のカードを描画します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-227">Place the cards in the indicated area above, and then draw 5 cards.</span></span> <span data-ttu-id="f03a9-228">描画したカードを確認し、関連するボードセグメントに配置します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-228">Review the cards you’ve drawn and place them on the relevant board segment.</span></span> <span data-ttu-id="f03a9-229">各プレイヤーは、パス上の各カードの手順、品質目標のアサート、目標の達成、サービスレベルの維持などを行います。</span><span class="sxs-lookup"><span data-stu-id="f03a9-229">Each player moves through the cards on their path step by step, asserting quality targets, achieving those targets, and maintaining the service levels.</span></span> <span data-ttu-id="f03a9-230">すべてのプレイヤーがセンターサービス管理の状態に到達すると、ゲームが完了します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-230">The game is completed when all players reach the center Service Management state.</span></span> <span data-ttu-id="f03a9-231">詳細なルールについては、「ゲームカードのダウンロード」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="f03a9-231">More detailed rules are provided with the game card download.</span></span>

<span data-ttu-id="f03a9-232">品質目標を **アサート** するには、対象のターゲットに該当するパラメーターを確認し、状態を把握して、承諾しないようにします。</span><span class="sxs-lookup"><span data-stu-id="f03a9-232">To **Assert** a quality target, review the parameters applicable to that target, and state out loud what you will and won’t choose to accept.</span></span> <span data-ttu-id="f03a9-233">最初のポイントをお勧めしますが、最終的な通話を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="f03a9-233">We have recommended beginning points, but you must make the final call.</span></span> <span data-ttu-id="f03a9-234">例外は KHI データであり、Microsoft によって確立された標準を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f03a9-234">The exception is KHI data, where the standards established by Microsoft should be used.</span></span> <span data-ttu-id="f03a9-235">付属の KHI ポスターを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f03a9-235">See the accompanying KHI poster.</span></span>

<span data-ttu-id="f03a9-236">この **ゲームでは** 、khi データとシステムクエリの代わりに提供されているカードを使用します。</span><span class="sxs-lookup"><span data-stu-id="f03a9-236">To **Achieve** in the game, use the cards provided in place of KHI data and system queries.</span></span> <span data-ttu-id="f03a9-237">ゲームの開始時に、特定のアスペクトに関連するカードを描画していない場合は、それ以降の操作を続けることができます。</span><span class="sxs-lookup"><span data-stu-id="f03a9-237">If at the start of the game you did not draw a card relating to a given aspect, you can continue past it.</span></span> <span data-ttu-id="f03a9-238">関連するカードがある場合は、さいころをロールします。</span><span class="sxs-lookup"><span data-stu-id="f03a9-238">If there is a relevant card, roll the die.</span></span> <span data-ttu-id="f03a9-239">カードに記載されている番号でロールされた場合は、成功したことになります。</span><span class="sxs-lookup"><span data-stu-id="f03a9-239">If you rolled under the number indicated on the card, you have succeeded.</span></span> <span data-ttu-id="f03a9-240">指定した番号の上または上に重ねている場合は、デッキから別のカードを描画する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f03a9-240">If you roll at or over the indicated number, you must draw another card from the deck.</span></span> <span data-ttu-id="f03a9-241">2人以上のプレイヤーがロールする必要があることがカードで示されている場合は、すべてロールアウトする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f03a9-241">If the card indicates two or more players need to roll, they must all roll successfully.</span></span>

<span data-ttu-id="f03a9-242">ゲームを **維持** するために、Lync 環境のその側面に関するサービス管理計画を把握しておきます。</span><span class="sxs-lookup"><span data-stu-id="f03a9-242">To **Maintain** in the game, state out loud the service management plan regarding that aspect of the Lync environment.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f03a9-243">関連項目</span><span class="sxs-lookup"><span data-stu-id="f03a9-243">See Also</span></span>


[<span data-ttu-id="f03a9-244">Lync Server ネットワークガイド</span><span class="sxs-lookup"><span data-stu-id="f03a9-244">Lync Server Networking Guide</span></span>](https://go.microsoft.com/fwlink/p/?linkid=390677)  
[<span data-ttu-id="f03a9-245">主要な正常性インジケーター: 正常な Lync サーバーを管理するための基盤</span><span class="sxs-lookup"><span data-stu-id="f03a9-245">Key Health Indicators: The Foundation for Maintaining Healthy Lync Servers</span></span>](https://go.microsoft.com/fwlink/?linkid=391838)  
[<span data-ttu-id="f03a9-246">Lync 通話品質の方法</span><span class="sxs-lookup"><span data-stu-id="f03a9-246">Lync Call Quality Methodology</span></span>](https://go.microsoft.com/fwlink/?linkid=391841)  
  

<span data-ttu-id="f03a9-247"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f03a9-247"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

