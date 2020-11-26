---
title: 'Lync Server 2013: E9 展開のスコープを定義する'
description: 'Lync Server 2013: E9 展開のスコープを定義します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Defining the scope of the E9-1-1 deployment
ms:assetid: 2c572dfd-e901-471d-b5a0-18bc8d1d5328
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425775(v=OCS.15)
ms:contentKeyID: 48183707
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 14e442718b7230dbc94aebdf6099aae9b430d5e9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430967"
---
# <a name="defining-the-scope-of-the-e9-1-1-deployment-in-lync-server-2013"></a><span data-ttu-id="5b87d-103">Lync Server 2013 での E9 展開のスコープの定義</span><span class="sxs-lookup"><span data-stu-id="5b87d-103">Defining the scope of the E9-1-1 deployment in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5b87d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5b87d-104">

<span> </span></span></span>

<span data-ttu-id="5b87d-105">_**最終更新日:** 2012-06-06_</span><span class="sxs-lookup"><span data-stu-id="5b87d-105">_**Topic Last Modified:** 2012-06-06_</span></span>

<span data-ttu-id="5b87d-106">Microsoft Lync Server 2013 for E9-1 を構成する前に、E9 の展開を計画する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5b87d-106">Before you configure Microsoft Lync Server 2013 for E9-1-1, you need to plan your E9-1-1 deployment.</span></span> <span data-ttu-id="5b87d-107">次のような点を検討します。</span><span class="sxs-lookup"><span data-stu-id="5b87d-107">Some of the questions to consider include:</span></span>

  - <span data-ttu-id="5b87d-108">**E9-1-1 に関して組織にどのようなポリシーと法的義務があるか**</span><span class="sxs-lookup"><span data-stu-id="5b87d-108">**What are your organization’s policy and legal obligations with regard to E9-1-1?**</span></span>  
    <span data-ttu-id="5b87d-109">PBX (E9-1-1 用語では複数回線電話システム (MLTS) と呼ばれます) 使用時の E9-1-1 の法的義務は州ごとに異なります。</span><span class="sxs-lookup"><span data-stu-id="5b87d-109">E9-1-1 legal requirements for PBXs (called Multi-line Telephone Systems, or MLTS, in E9-1-1 parlance) differ from state to state.</span></span> <span data-ttu-id="5b87d-110">法務チームに相談して、関連する地域での Lync Server の展開に適用される可能性がある義務を理解してください。</span><span class="sxs-lookup"><span data-stu-id="5b87d-110">You should consult with your legal team to understand the obligations that may apply to your deployment of Lync Server in your relevant geographies.</span></span>

<!-- end list -->

  - <span data-ttu-id="5b87d-111">**エンタープライズ内のどの領域で E9-1-1 を有効にする必要があるか**</span><span class="sxs-lookup"><span data-stu-id="5b87d-111">**What areas within your enterprise need to be enabled for E9-1-1?**</span></span>  
    <span data-ttu-id="5b87d-p103">E9-1-1 は、エンタープライズ全体で有効にすることも、特定の場所だけで有効にすることもできます。たとえば、オフィスの E9-1-1 の要件が州によって異なる場合や、米国以外のサイトを除外する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="5b87d-p103">You can enable E9-1-1 for the entire enterprise or for selected locations. For example, you may have varying E9-1-1 requirements for offices in different states, or you may want to exclude sites outside the U.S.</span></span>

<!-- end list -->

  - <span data-ttu-id="5b87d-114">**E9-1-1 をブランチ サイトにどのように展開するか**</span><span class="sxs-lookup"><span data-stu-id="5b87d-114">**How will you deploy E9-1-1 to branch sites?**</span></span>  
    <span data-ttu-id="5b87d-115">E9-1-1 をブランチ サイトに展開するときは、音声の復元の概念を理解することが重要です。</span><span class="sxs-lookup"><span data-stu-id="5b87d-115">Voice resiliency is an important concept to understand when deploying E9-1-1 at a branch site.</span></span> <span data-ttu-id="5b87d-116">一元化された電子 9-1-1 SIP trunks を使用していて、WAN の障害が発生した場合、クライアントは、場所情報サービスからの場所を取得できないか、緊急サービスサービスプロバイダに接続できない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5b87d-116">If you have centralized E-9-1-1 SIP trunks and a WAN outage occurs, clients signing in may not be able to obtain a location from Location Information service or to connect to the emergency services service provider.</span></span> <span data-ttu-id="5b87d-117">Lync Server には、回復可能なデータネットワーク、各ブランチへの SIP トランクの展開、停止中のローカルゲートウェイへの緊急通話の配信など、支店の音声回復性を処理するためのいくつかの戦略が用意されています。</span><span class="sxs-lookup"><span data-stu-id="5b87d-117">Lync Server provides several strategies for handling voice resiliency in branch offices, including: having resilient data networks, deploying a SIP trunk at each branch, or pushing emergency calls out to the local gateway during outages.</span></span> <span data-ttu-id="5b87d-118">詳細については、「 [Lync Server 2013 でのブランチサイトの音声回復性の計画](lync-server-2013-planning-for-branch-site-voice-resiliency.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5b87d-118">For details, see [Planning for branch-site voice resiliency in Lync Server 2013](lync-server-2013-planning-for-branch-site-voice-resiliency.md).</span></span>

<!-- end list -->

  - <span data-ttu-id="5b87d-119">**ネットワーク外のユーザーに対し、E9-1-1 を有効にするかどうか**</span><span class="sxs-lookup"><span data-stu-id="5b87d-119">**Will you enable E9-1-1 for users working outside the network?**</span></span>  
    <span data-ttu-id="5b87d-120">自動的な場所の取得は、組織のネットワーク内にあるクライアントに対してのみ利用できます。そのため、組織では、Lync クライアントから発信された E9 の通話がオフプレミスでサポートされるかどうかを決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5b87d-120">Automatic location acquisition is available only for clients located inside the organization’s network, so your organization needs to decide whether it will support E9-1-1 calls made from Lync clients while off-premises.</span></span> <span data-ttu-id="5b87d-121">たとえば、ユーザーが自宅で作業している場合や顧客サイトから作業している場合に、緊急電話をかけることができますか。</span><span class="sxs-lookup"><span data-stu-id="5b87d-121">For example, will you enable users to place emergency calls if they are working from home or from a customer site?</span></span> <span data-ttu-id="5b87d-122">クライアントがエンタープライズネットワークの外部に配置されている場合は、ユーザーに位置情報の入力を求めるようにクライアントを構成できます。</span><span class="sxs-lookup"><span data-stu-id="5b87d-122">If a client is located outside the enterprise network, the client can be configured to prompt the user for a location.</span></span> <span data-ttu-id="5b87d-123">ただし、ユーザーが指定した場所は、マスター番地の住所ガイド (MSAG) に対して prevalidated できないため、緊急サービスサービスプロバイダーディスパッチャーは、通話を公共の安全な応答ポイント (PSAP) にルーティングする前に、発信者との場所コミュニケーションとるの有効性を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5b87d-123">However, because these user-provided locations cannot be prevalidated against the Master Street Address Guide (MSAG), the emergency services service provider dispatcher will need to confirm the validity of the location verbally with the caller before routing the call to the Public Safety Answering Point (PSAP).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="5b87d-124">VPN を使用して組織のネットワークに接続しているユーザーの Lync クライアントは、内部の IP アドレス情報を取得できますが、これらのアドレスを使ってユーザーの実際の場所を特定することはできません。そのため、VPN サブネットは、位置情報サービスから除外されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="5b87d-124">Lync clients of users who connect to your organization’s network by using VPN can pick up internal IP address information, but because these addresses cannot be used to identify the user’s actual location, it is essential that VPN subnets are excluded from the Location Information service.</span></span>

    
    </div>

<!-- end list -->

  - <span data-ttu-id="5b87d-125">**米国以外のサイトに緊急通話のルーティングを提供するかどうか**</span><span class="sxs-lookup"><span data-stu-id="5b87d-125">**Do you want to provide emergency call routing to sites outside the U.S.?**</span></span>  
    <span data-ttu-id="5b87d-p106">緊急サービスのサービス プロバイダーのサービス対象範囲外 (国外の場所など) にある会社の領域に緊急通話のルーティングを提供したい場合があります。この場合は、新しいサイトを作成し、ローカル PSTN ゲートウェイ経由で通話をルーティングする PSTN 使用法を参照する音声ポリシーをサイトに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="5b87d-p106">You may want to provide emergency routing to areas of your company not served by an emergency services service provider (for example, international locations). To do this, create a new site, and then assign voice policies to the sites that refer to a PSTN usage that routes the call through the local PSTN gateway.</span></span>

<span data-ttu-id="5b87d-128"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5b87d-128"></div>

<span> </span>

</div>

</div>

</span></span></div>

