---
title: 'Lync Server 2013: MPLS ネットワークの通話受付制御'
description: 'Lync Server 2013: MPLS ネットワークの通話受付制御。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call admission control on an MPLS network
ms:assetid: 0beec6be-2431-4255-a3d2-512dd030e66a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398168(v=OCS.15)
ms:contentKeyID: 48183387
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e26ba95a9191b567520978ee9512cbbc12e934ec
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435890"
---
# <a name="call-admission-control-on-an-mpls-network-with-lync-server-2013"></a><span data-ttu-id="e7906-103">Lync Server 2013 を使って、MPLS ネットワーク上の通話受付制御</span><span class="sxs-lookup"><span data-stu-id="e7906-103">Call admission control on an MPLS network with Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e7906-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e7906-104">

<span> </span></span></span>

<span data-ttu-id="e7906-105">_**最終更新日:** 2012-09-22_</span><span class="sxs-lookup"><span data-stu-id="e7906-105">_**Topic Last Modified:** 2012-09-22_</span></span>

<span data-ttu-id="e7906-p101">Multiprotocol Label Switching (MPLS) では、すべてのサイトがフル メッシュで接続されます。つまり、すべてのサイトがインターネット サービス プロバイダーの MPLS バックボーンに直接接続され、各サイトが WAN リンクから MPLS クラウドにかけて使用されるプロビジョニングされた帯域幅であるということです。IP ルーティングを制御するネットワーク ハブや中央サイトはありません。次の図に、MPLS トポロジに基づく簡単なネットワークを示します。</span><span class="sxs-lookup"><span data-stu-id="e7906-p101">In a Multiprotocol Label Switching (MPLS) network, all sites are connected by a full-mesh. That is, all sites are connected directly to the MPLS backbone of the Internet service provider, and each site is provisioned bandwidth to be used across a WAN link to the MPLS cloud. There is no network hub or central site to control IP routing. The following figure shows a simple network based on MPLS technology.</span></span>

<span data-ttu-id="e7906-110">**MPLS ネットワークの例**</span><span class="sxs-lookup"><span data-stu-id="e7906-110">**Example MPLS network**</span></span>

<span data-ttu-id="e7906-111">![MPLS が含まれる CAC](images/Gg398168.54602e6e-ec11-4dae-936d-b01acda8a179(OCS.15).jpg "MPLS が含まれる CAC")</span><span class="sxs-lookup"><span data-stu-id="e7906-111">![CAC with MPLS](images/Gg398168.54602e6e-ec11-4dae-936d-b01acda8a179(OCS.15).jpg "CAC with MPLS")</span></span>

<span data-ttu-id="e7906-p102">MPLS ネットワークで通話受付管理 (CAC) を展開するには、MPLS クラウドを表すネットワーク地域を作成し、MPLS の各サテライト サイトを表すネットワーク サイトを作成します。 次の図で、前の図の MPLS ネットワークの例を表すための、ネットワーク地域およびネットワーク サイトの構成方法について説明します。 全体的な帯域幅および帯域幅セッションの制限は、各ネットワーク サイトから MPLS クラウドを表すネットワーク地域までの WAN リンクの容量に基づきます。</span><span class="sxs-lookup"><span data-stu-id="e7906-p102">To deploy call admission control (CAC) in an MPLS network, you create a network region to represent the MPLS cloud, and create a network site to represent each MPLS satellite site. The following figure illustrates how the network region and network sites should be configured to represent the example MPLS network in the previous figure. The overall bandwidth limits and bandwidth session limits are then based on the capacity of the WAN link from each network site to the network region that represents the MPLS cloud.</span></span>

<span data-ttu-id="e7906-115">**MPLS ネットワークのネットワーク地域およびネットワーク サイト**</span><span class="sxs-lookup"><span data-stu-id="e7906-115">**Network region and network sites for an MPLS network**</span></span>

<span data-ttu-id="e7906-116">![MPLS が含まれない通話受付管理 (CAC)](images/Gg398168.f8f76283-5c0c-4133-8a78-3fbbfd016dc4(OCS.15).jpg "MPLS が含まれない通話受付管理 (CAC)")</span><span class="sxs-lookup"><span data-stu-id="e7906-116">![Call Admission Control (CAC) with MPLS diagram](images/Gg398168.f8f76283-5c0c-4133-8a78-3fbbfd016dc4(OCS.15).jpg "Call Admission Control (CAC) with MPLS diagram")</span></span>

<span data-ttu-id="e7906-117"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e7906-117"></div>

<span> </span>

</div>

</div>

</span></span></div>

