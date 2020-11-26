---
title: 'Lync Server 2013: エンタープライズ Voip の計画'
description: 'Lync Server 2013: エンタープライズ Voip の計画。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for Enterprise Voice
ms:assetid: fd8d5867-0ac9-47f8-94f0-1c3ee5e25575
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413081(v=OCS.15)
ms:contentKeyID: 48185959
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4dfa0d91fe8270e49524d648ef403cd69ede2407
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424584"
---
# <a name="planning-for-enterprise-voice-in-lync-server-2013"></a><span data-ttu-id="7513e-103">Lync Server 2013 でのエンタープライズ Voip の計画</span><span class="sxs-lookup"><span data-stu-id="7513e-103">Planning for Enterprise Voice in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7513e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7513e-104">

<span> </span></span></span>

<span data-ttu-id="7513e-105">_**最終更新日:** 2013-11-01_</span><span class="sxs-lookup"><span data-stu-id="7513e-105">_**Topic Last Modified:** 2013-11-01_</span></span>

<span data-ttu-id="7513e-106">エンタープライズボイスの展開プロセスは、既存のトポロジ、インフラストラクチャ、およびサポートするエンタープライズ Voip 機能によって異なります。</span><span class="sxs-lookup"><span data-stu-id="7513e-106">The deployment process for Enterprise Voice depends on your existing topology, infrastructure, and the Enterprise Voice functionality that you want to support.</span></span> <span data-ttu-id="7513e-107">必要な手順は選択する機能によって異なりますが、計画に関して高レベルで考慮が必要なその他の事項があります。</span><span class="sxs-lookup"><span data-stu-id="7513e-107">The required procedures will depend on what features you choose, but there are other planning considerations that you must make at a high level.</span></span>

<span data-ttu-id="7513e-108">通常は、展開するサイトの種類と数および地理的な場所、各サイトの通話ボリューム、サイト間を接続するネットワーク リンクの種類、各サイトの音声機能に冗長性とフェールオーバーを持たせるかどうか、および既存の PBX 機器を使用するかどうかを考慮してください。</span><span class="sxs-lookup"><span data-stu-id="7513e-108">In general, consider the type and number of sites that you want to deploy and their geographical locations, the call volume at each site, the types of network links that connect sites, whether you want to provide redundancy and failover for voice functionality for each site, and whether you want to use existing PBX equipment.</span></span> <span data-ttu-id="7513e-109">Lync Server の通信ソフトウェアを全体として計画するときに考慮する必要がある、高可用性などの特定の考慮事項があります。</span><span class="sxs-lookup"><span data-stu-id="7513e-109">There are certain considerations, such as high availability, that you should consider when you plan for Lync Server  communications software as a whole.</span></span> <span data-ttu-id="7513e-110">これらの考慮事項については、このセクションのトピックで必要に応じて説明します。</span><span class="sxs-lookup"><span data-stu-id="7513e-110">These considerations are discussed in topics throughout this section, as needed.</span></span>

<div>

## <a name="planning-considerations"></a><span data-ttu-id="7513e-111">計画の考慮事項</span><span class="sxs-lookup"><span data-stu-id="7513e-111">Planning Considerations</span></span>

<span data-ttu-id="7513e-112">特定のエンタープライズボイス機能または展開シナリオまたはコンポーネントの展開に関連する計画を決定するには、このセクションのトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7513e-112">For planning decisions that pertain to the deployment of a particular Enterprise Voice capability or deployment scenario or component, consult the topics in this section.</span></span>

  - [<span data-ttu-id="7513e-113">Lync Server 2013 での組織のエンタープライズ VoIP 要件の定義</span><span class="sxs-lookup"><span data-stu-id="7513e-113">Defining your requirements for Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-defining-your-requirements-for-enterprise-voice.md)

  - [<span data-ttu-id="7513e-114">Lync Server 2013 の音声の利用状況とトラフィックの予測</span><span class="sxs-lookup"><span data-stu-id="7513e-114">Estimating voice usage and traffic for Lync Server 2013</span></span>](lync-server-2013-estimating-voice-usage-and-traffic.md)

  - [<span data-ttu-id="7513e-115">Network settings for the advanced Enterprise Voice features in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7513e-115">Network settings for the advanced Enterprise Voice features in Lync Server 2013</span></span>](lync-server-2013-network-settings-for-the-advanced-enterprise-voice-features.md)

  - [<span data-ttu-id="7513e-116">Components required for Enterprise Voice in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7513e-116">Components required for Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-components-required-for-enterprise-voice.md)

  - [<span data-ttu-id="7513e-117">Lync Server 2013 でのエンタープライズ VoIP の復旧の計画</span><span class="sxs-lookup"><span data-stu-id="7513e-117">Planning for Enterprise Voice resiliency in Lync Server 2013</span></span>](lync-server-2013-planning-for-enterprise-voice-resiliency.md)

  - [<span data-ttu-id="7513e-118">Lync Server 2013 での Exchange ユニファイド メッセージング統合の計画</span><span class="sxs-lookup"><span data-stu-id="7513e-118">Planning for Exchange Unified Messaging integration in Lync Server 2013</span></span>](lync-server-2013-planning-for-exchange-unified-messaging-integration.md)

  - [<span data-ttu-id="7513e-119">Lync Server 2013 での通話受付管理の計画</span><span class="sxs-lookup"><span data-stu-id="7513e-119">Planning for call admission control in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-admission-control.md)

  - [<span data-ttu-id="7513e-120">Lync Server 2013 での緊急サービス (E9-1-1) の計画</span><span class="sxs-lookup"><span data-stu-id="7513e-120">Planning for emergency services (E9-1-1) in Lync Server 2013</span></span>](lync-server-2013-planning-for-emergency-services-e9-1-1.md)

  - [<span data-ttu-id="7513e-121">Lync Server 2013 でのメディア バイパスの計画</span><span class="sxs-lookup"><span data-stu-id="7513e-121">Planning for media bypass in Lync Server 2013</span></span>](lync-server-2013-planning-for-media-bypass.md)

  - [<span data-ttu-id="7513e-122">Lync Server 2013 でのプライベート電話回線の計画</span><span class="sxs-lookup"><span data-stu-id="7513e-122">Planning for private telephone lines with Lync Server 2013</span></span>](lync-server-2013-planning-for-private-telephone-lines.md)

  - [<span data-ttu-id="7513e-123">Lync Server 2013 での場所に基づくルーティングの計画</span><span class="sxs-lookup"><span data-stu-id="7513e-123">Planning for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-planning-for-location-based-routing.md)

  - [<span data-ttu-id="7513e-124">Lync Server 2013 でのエンタープライズ VoIP の復旧の計画</span><span class="sxs-lookup"><span data-stu-id="7513e-124">Planning for Enterprise Voice resiliency in Lync Server 2013</span></span>](lync-server-2013-planning-for-enterprise-voice-resiliency.md)

  - [<span data-ttu-id="7513e-125">Lync Server 2013 のエンタープライズ VoIP の展開ガイドライン</span><span class="sxs-lookup"><span data-stu-id="7513e-125">Deployment guidelines for Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-deployment-guidelines-for-enterprise-voice.md)

  - [<span data-ttu-id="7513e-126">Lync Server 2013 のエンタープライズ VoIP の展開プロセスの概要</span><span class="sxs-lookup"><span data-stu-id="7513e-126">Deployment process overview for Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-deployment-process-overview-for-enterprise-voice.md)

  - [<span data-ttu-id="7513e-127">Lync Server 2013 でのエンタープライズ VoIP へのユーザーの移行</span><span class="sxs-lookup"><span data-stu-id="7513e-127">Moving users to Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-moving-users-to-enterprise-voice.md)

  - [<span data-ttu-id="7513e-128">Lync の PreCall のすべての診断ツール (Lync Server 2013)</span><span class="sxs-lookup"><span data-stu-id="7513e-128">Lync PreCall Diagnostics Tool in Lync Server 2013</span></span>](lync-server-2013-lync-precall-diagnostics-tool.md)

<span data-ttu-id="7513e-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7513e-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

