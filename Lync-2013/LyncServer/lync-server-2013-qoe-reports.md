---
title: 'Lync Server 2013: QoE レポート'
description: 'Lync Server 2013: QoE レポート。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: QoE reports
ms:assetid: 49c827af-b8dd-4c6e-b0dc-b4bc6d60e9a3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720913(v=OCS.15)
ms:contentKeyID: 63969601
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 55965d246b7f0ddd71eaeeec99d218eaf8819c2e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398997"
---
# <a name="qoe-reports-in-lync-server-2013"></a><span data-ttu-id="f9f13-103">Lync Server 2013 の QoE レポート</span><span class="sxs-lookup"><span data-stu-id="f9f13-103">QoE reports in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f9f13-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f9f13-104">

<span> </span></span></span>

<span data-ttu-id="f9f13-105">_**最終更新日:** 2014-05-01_</span><span class="sxs-lookup"><span data-stu-id="f9f13-105">_**Topic Last Modified:** 2014-05-01_</span></span>

<div>

## <a name="qoe-summarytrend-reports"></a><span data-ttu-id="f9f13-106">QoE サマリー/トレンドレポート</span><span class="sxs-lookup"><span data-stu-id="f9f13-106">QoE summary/trend reports</span></span>

<span data-ttu-id="f9f13-107">QoE サマリー/トレンドレポートは、組織のネットワークリソースが十分であることを確認するために、1日のピーク使用時間を見つけてメディアの品質を確認するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="f9f13-107">The QoE summary/trends reports are useful for finding the peak usage times of day and examining the media quality during those times to help assure that your organization's network resources are sufficient.</span></span> <span data-ttu-id="f9f13-108">組織では、レポートで利用可能な多くのフィルターを使用して、特定の場所、クライアントとデバイスの種類、サーバーのパフォーマンスの数値を特定することもできます。</span><span class="sxs-lookup"><span data-stu-id="f9f13-108">Your organization can also use the many filters available in the report to isolate performance numbers for certain locations, client and device types, and servers.</span></span>

<span data-ttu-id="f9f13-109">QoE サマリー/トレンドレポートは次の要素で構成されます。</span><span class="sxs-lookup"><span data-stu-id="f9f13-109">QoE summary/trend reports consist of:</span></span>

  - <span data-ttu-id="f9f13-110">UC 対多集計のサマリー/トレンドレポート</span><span class="sxs-lookup"><span data-stu-id="f9f13-110">UC-to-UC Summary/Trend Report</span></span>

  - <span data-ttu-id="f9f13-111">PSTN サマリー/トレンドレポート</span><span class="sxs-lookup"><span data-stu-id="f9f13-111">PSTN Summary/Trend Report</span></span>

  - <span data-ttu-id="f9f13-112">会議の概要/傾向レポート</span><span class="sxs-lookup"><span data-stu-id="f9f13-112">Conference Summary/Trend Report</span></span>

</div>

<div>

## <a name="qoe-performance-reports"></a><span data-ttu-id="f9f13-113">QoE のパフォーマンスレポート</span><span class="sxs-lookup"><span data-stu-id="f9f13-113">QoE performance reports</span></span>

<span data-ttu-id="f9f13-114">QoE パフォーマンスレポートには、仲介サーバー、A/V 会議サーバー、エンドポイントの場所の QoE パフォーマンスに焦点を当てた3つのレポートに関する詳細が用意されています。</span><span class="sxs-lookup"><span data-stu-id="f9f13-114">QoE performance reports provide details about the three reports that concentrate on the QoE performance of Mediation Servers, A/V Conferencing Servers, and endpoint locations.</span></span>

</div>

<div>

## <a name="mediation-server-performance-report"></a><span data-ttu-id="f9f13-115">仲介サーバーパフォーマンスレポート</span><span class="sxs-lookup"><span data-stu-id="f9f13-115">Mediation server performance report</span></span>

<span data-ttu-id="f9f13-116">仲介サーバーのパフォーマンスレポートには、指定した期間中に、1つ以上の仲介によって得られたメトリックが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="f9f13-116">The Mediation Server Performance report lists the metrics achieved by one or more Mediation during the specified time period.</span></span> <span data-ttu-id="f9f13-117">ユニファイドコミュニケーション (UC) 対仲介サーバーの区間と、各通話の仲介サーバー間の区間のメトリックは、別々に報告されます。</span><span class="sxs-lookup"><span data-stu-id="f9f13-117">The metrics for the unified communications (UC)-to-Mediation Server leg and the Mediation Server-to-Gateway leg of each call are reported separately.</span></span> <span data-ttu-id="f9f13-118">このレポートを使用して、組織のさまざまな仲介サーバーのボリュームとパフォーマンスを比較します。</span><span class="sxs-lookup"><span data-stu-id="f9f13-118">Use this report to compare the volume and performance of your organization's various Mediation Servers.</span></span>

<span data-ttu-id="f9f13-119">各仲介サーバー (および各通話区間用) には、次のようなレポートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f9f13-119">For each Mediation Server (and for each call leg), the report displays the following:</span></span>

  - <span data-ttu-id="f9f13-120">通話の数</span><span class="sxs-lookup"><span data-stu-id="f9f13-120">Number of calls</span></span>

  - <span data-ttu-id="f9f13-121">パケット損失</span><span class="sxs-lookup"><span data-stu-id="f9f13-121">Packet Loss</span></span>

  - <span data-ttu-id="f9f13-122">ラウンドトリップ時間</span><span class="sxs-lookup"><span data-stu-id="f9f13-122">Round Trip Time</span></span>

  - <span data-ttu-id="f9f13-123">ジッター</span><span class="sxs-lookup"><span data-stu-id="f9f13-123">Jitter</span></span>

  - <span data-ttu-id="f9f13-124">話し言葉平均の意見 (MOS)</span><span class="sxs-lookup"><span data-stu-id="f9f13-124">Conversational mean opinion score (MOS)</span></span>

  - <span data-ttu-id="f9f13-125">MOS を送信中</span><span class="sxs-lookup"><span data-stu-id="f9f13-125">Sending MOS</span></span>

  - <span data-ttu-id="f9f13-126">聞き取り MOS</span><span class="sxs-lookup"><span data-stu-id="f9f13-126">Listening MOS</span></span>

  - <span data-ttu-id="f9f13-127">Network MOS</span><span class="sxs-lookup"><span data-stu-id="f9f13-127">Network MOS</span></span>

  - <span data-ttu-id="f9f13-128">ネットワーク MOS の低下</span><span class="sxs-lookup"><span data-stu-id="f9f13-128">Network MOS Degradation</span></span>

  - <span data-ttu-id="f9f13-129">エコーリターン</span><span class="sxs-lookup"><span data-stu-id="f9f13-129">Echo Return</span></span>

  - <span data-ttu-id="f9f13-130">シグナルレベル</span><span class="sxs-lookup"><span data-stu-id="f9f13-130">Signal Level</span></span>

</div>

<div>

## <a name="av-conferencing-server-performance-report"></a><span data-ttu-id="f9f13-131">A/V 会議サーバーパフォーマンスレポート</span><span class="sxs-lookup"><span data-stu-id="f9f13-131">A/V conferencing server performance report</span></span>

<span data-ttu-id="f9f13-132">A/V 会議サーバーパフォーマンスレポートでは、指定された期間中に1つ以上の A/V 会議サーバーによって達成された指標の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="f9f13-132">The A/V Conferencing Server Performance report provides lists of metrics achieved by one or more A/V Conferencing Servers during the specified time period.</span></span> <span data-ttu-id="f9f13-133">このレポートは、組織のさまざまな A/V 会議サーバーのボリュームとパフォーマンスを比較するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="f9f13-133">This report can be used to compare the volume and performance of your organization’s various A/V Conferencing Servers.</span></span> <span data-ttu-id="f9f13-134">組織でレポートを分離して、Lync クライアントや PSTN クライアントなど、特定のクライアントの種類のエクスペリエンスのみを表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="f9f13-134">Your organization can also isolate the report to show only the experience for specific client types, such as Lync clients or PSTN clients.</span></span>

<span data-ttu-id="f9f13-135">各 A/V 会議サーバーでは、レポートに次の内容が表示されます。</span><span class="sxs-lookup"><span data-stu-id="f9f13-135">For each A/V Conferencing Server, the report displays the following:</span></span>

  - <span data-ttu-id="f9f13-136">会議の数</span><span class="sxs-lookup"><span data-stu-id="f9f13-136">Number of conferences</span></span>

  - <span data-ttu-id="f9f13-137">パケット損失</span><span class="sxs-lookup"><span data-stu-id="f9f13-137">Packet Loss</span></span>

  - <span data-ttu-id="f9f13-138">ラウンドトリップ時間</span><span class="sxs-lookup"><span data-stu-id="f9f13-138">Round Trip Time</span></span>

  - <span data-ttu-id="f9f13-139">ジッター</span><span class="sxs-lookup"><span data-stu-id="f9f13-139">Jitter</span></span>

  - <span data-ttu-id="f9f13-140">話し言葉平均の意見 (MOS)</span><span class="sxs-lookup"><span data-stu-id="f9f13-140">Conversational mean opinion score (MOS)</span></span>

  - <span data-ttu-id="f9f13-141">MOS を送信中</span><span class="sxs-lookup"><span data-stu-id="f9f13-141">Sending MOS</span></span>

  - <span data-ttu-id="f9f13-142">聞き取り MOS</span><span class="sxs-lookup"><span data-stu-id="f9f13-142">Listening MOS</span></span>

  - <span data-ttu-id="f9f13-143">Network MOS</span><span class="sxs-lookup"><span data-stu-id="f9f13-143">Network MOS</span></span>

  - <span data-ttu-id="f9f13-144">ネットワーク MOS の低下</span><span class="sxs-lookup"><span data-stu-id="f9f13-144">Network MOS Degradation</span></span>

  - <span data-ttu-id="f9f13-145">エコーリターン</span><span class="sxs-lookup"><span data-stu-id="f9f13-145">Echo Return</span></span>

  - <span data-ttu-id="f9f13-146">シグナルレベル</span><span class="sxs-lookup"><span data-stu-id="f9f13-146">Signal Level</span></span>

</div>

<div>

## <a name="location-based-performance-report"></a><span data-ttu-id="f9f13-147">位置ベースのパフォーマンスレポート</span><span class="sxs-lookup"><span data-stu-id="f9f13-147">Location-based performance report</span></span>

<span data-ttu-id="f9f13-148">Location-Based のパフォーマンスレポートでは、ネットワーク上の場所の一覧が表示され、それぞれの場所には、事前に決定された各品質の範囲の通話数が示されます。</span><span class="sxs-lookup"><span data-stu-id="f9f13-148">The Location-Based Performance report provides a list of network locations and for each location shows the number of calls in each pre-determined range of quality.</span></span> <span data-ttu-id="f9f13-149">このレポートの目標は、さまざまな場所についての組織の電話の大半の通話品質を把握して、組織のさまざまな場所でのさまざまなメディア品質の評価を確認することです。</span><span class="sxs-lookup"><span data-stu-id="f9f13-149">The goal of this report is to provide insight into the media quality of the bulk of your organization’s telephone calls for various locations so that you can identify poorly performing locations, and see the different grades of media quality in your organization’s different locations.</span></span>

<span data-ttu-id="f9f13-150">レポートを表示すると、さまざまなメトリックのテーブルが表示されます。組織がレポートを決定する各指標ごとに1つのテーブルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f9f13-150">When displaying the report, different tables of metrics appear—one table for each metric your organization decides to report on.</span></span> <span data-ttu-id="f9f13-151">このレポートには、次のメトリックから選ぶことができます。</span><span class="sxs-lookup"><span data-stu-id="f9f13-151">You can choose from the following metrics for this report:</span></span>

  - <span data-ttu-id="f9f13-152">話し言葉平均の意見 (MOS)</span><span class="sxs-lookup"><span data-stu-id="f9f13-152">Conversational mean opinion score (MOS)</span></span>

  - <span data-ttu-id="f9f13-153">Network MOS</span><span class="sxs-lookup"><span data-stu-id="f9f13-153">Network MOS</span></span>

  - <span data-ttu-id="f9f13-154">ネットワーク MOS の低下</span><span class="sxs-lookup"><span data-stu-id="f9f13-154">Network MOS Degradation</span></span>

  - <span data-ttu-id="f9f13-155">MOS を送信中</span><span class="sxs-lookup"><span data-stu-id="f9f13-155">Sending MOS</span></span>

  - <span data-ttu-id="f9f13-156">聞き取り MOS</span><span class="sxs-lookup"><span data-stu-id="f9f13-156">Listening MOS</span></span>

  - <span data-ttu-id="f9f13-157">パケット損失</span><span class="sxs-lookup"><span data-stu-id="f9f13-157">Packet Loss</span></span>

  - <span data-ttu-id="f9f13-158">ジッター</span><span class="sxs-lookup"><span data-stu-id="f9f13-158">Jitter</span></span>

  - <span data-ttu-id="f9f13-159">間隔</span><span class="sxs-lookup"><span data-stu-id="f9f13-159">Latency</span></span>

<span data-ttu-id="f9f13-160"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f9f13-160"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

