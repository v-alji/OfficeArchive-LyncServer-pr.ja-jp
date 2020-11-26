---
title: 'Lync Server 2013: Lync Server 2013 ネットワーク インフラストラクチャの管理'
description: 'Lync Server 2013: Lync Server 2013 ネットワークインフラストラクチャの管理'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing the Lync Server 2013 network infrastructure
ms:assetid: cb13456a-8f66-4595-be21-8887f30ad4eb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182585(v=OCS.15)
ms:contentKeyID: 48185638
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ab1b5c6fe52374b012063ac26640e9bb25496ad7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425858"
---
# <a name="managing-the-lync-server-2013-network-infrastructure"></a><span data-ttu-id="5f0db-103">Lync Server 2013 ネットワーク インフラストラクチャの管理</span><span class="sxs-lookup"><span data-stu-id="5f0db-103">Managing the Lync Server 2013 network infrastructure</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5f0db-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5f0db-104">

<span> </span></span></span>

<span data-ttu-id="5f0db-105">_**最終更新日:** 2014-02-11_</span><span class="sxs-lookup"><span data-stu-id="5f0db-105">_**Topic Last Modified:** 2014-02-11_</span></span>

<span data-ttu-id="5f0db-106">Microsoft Lync Server 2013 には、通話受付制御 (CAC) とメディアバイパスのサポートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="5f0db-106">Microsoft Lync Server 2013 includes support for call admission control (CAC) and media bypass.</span></span> <span data-ttu-id="5f0db-107">これらの機能を実装するには、領域、サイト、サブネットなどのネットワークを構成する必要があります。これにより、オーディオとビデオの伝送を制限する必要がある状況で帯域幅を管理できるようになります。</span><span class="sxs-lookup"><span data-stu-id="5f0db-107">To implement these features you must configure a network of regions, sites, subnets, and so on that will allow you to manage bandwidth in situations where audio and video transmissions need to be restricted.</span></span> <span data-ttu-id="5f0db-108">また、QoS (Quality of Service) ネットワーク技術を使用して、音声およびビデオ通信に最適なエンドユーザーエクスペリエンスを提供することもできます。</span><span class="sxs-lookup"><span data-stu-id="5f0db-108">You can also use the Quality of Service (QoS) networking technology to help provide an optimal end-user experience for audio and video communications.</span></span>

<span data-ttu-id="5f0db-109">Lync Server コントロールパネルを使用して、CAC、メディアバイパス、および QoS のセットアップと管理を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="5f0db-109">You can use the Lync Server Control Panel to set up and manage CAC, media bypass, and QoS.</span></span> <span data-ttu-id="5f0db-110">次のトピックでは、この方法の手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="5f0db-110">The following topics provide steps for how to do this.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="5f0db-111">このセクション中</span><span class="sxs-lookup"><span data-stu-id="5f0db-111">In This Section</span></span>

  - [<span data-ttu-id="5f0db-112">Lync Server 2013 での QoS (Quality of Service) の管理</span><span class="sxs-lookup"><span data-stu-id="5f0db-112">Managing Quality of Service (QoS) in Lync Server 2013</span></span>](lync-server-2013-managing-quality-of-service-qos.md)

  - [<span data-ttu-id="5f0db-113">Lync Server 2013 での通話受付制御の管理</span><span class="sxs-lookup"><span data-stu-id="5f0db-113">Managing call admission control in Lync Server 2013</span></span>](lync-server-2013-managing-call-admission-control.md)

  - [<span data-ttu-id="5f0db-114">Lync Server 2013 ネットワークインターフェイス</span><span class="sxs-lookup"><span data-stu-id="5f0db-114">Lync Server 2013 network interfaces</span></span>](lync-server-2013-lync-server-network-interfaces.md)

  - [<span data-ttu-id="5f0db-115">Lync Server 2013 への新しい接続でサーバーのメンテナンスができないようにする</span><span class="sxs-lookup"><span data-stu-id="5f0db-115">Prevent new connections to Lync Server 2013 for server maintenance</span></span>](lync-server-2013-prevent-new-connections-to-lync-server-for-server-maintenance.md)

  - [<span data-ttu-id="5f0db-116">Lync Server 2013 での lync 通話品質の方法</span><span class="sxs-lookup"><span data-stu-id="5f0db-116">Lync Call Quality Methodology in Lync Server 2013</span></span>](lync-server-2013-poster-lync-call-quality-methodology.md)

  - [<span data-ttu-id="5f0db-117">Lync Server 2013 の主要な正常性インジケーター</span><span class="sxs-lookup"><span data-stu-id="5f0db-117">Key Health Indicators in Lync Server 2013</span></span>](lync-server-2013-poster-key-health-indicators.md)

<span data-ttu-id="5f0db-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5f0db-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

