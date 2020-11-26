---
title: 拡張ディレクター プール - DNS 負荷分散とロード バランサー機器
description: スケーリングされたディレクタープール-DNS 負荷分散とハードウェアロードバランサー。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Scaled Director pool - DNS load balancing and hardware load balancer
ms:assetid: a1f6ffc0-9e6e-4217-a923-025c9679e154
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205142(v=OCS.15)
ms:contentKeyID: 48185023
ms.date: 03/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b30dfcc3515420ffb34343e4653e9518b1b9c3ed
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442062"
---
# <a name="scaled-director-pool---dns-load-balancing-and-hardware-load-balancer-in-lync-server-2013"></a><span data-ttu-id="384ea-103">拡張ディレクター プール - Lync Server 2013 の DNS 負荷分散とロード バランサー機器</span><span class="sxs-lookup"><span data-stu-id="384ea-103">Scaled Director pool - DNS load balancing and hardware load balancer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="384ea-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="384ea-104">

<span> </span></span></span>

<span data-ttu-id="384ea-105">_**最終更新日:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="384ea-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="384ea-106">スケーリングされたディレクタープール。追加の容量を処理し、高可用性を実現するために複数のディレクターが展開されている場合は、プールのすべてのメンバーにクライアントとサーバーの通信を配布するために負荷分散を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="384ea-106">A scaled Director pool, where there are more than one Director deployed to handle additional capacity and to provide high availability, requires load balancing to distribute client and server communication to all members of the pool.</span></span> <span data-ttu-id="384ea-107">ディレクターは、フロントエンドプールのような web サービスをホストします。</span><span class="sxs-lookup"><span data-stu-id="384ea-107">A Director hosts web services much like a Front End pool.</span></span> <span data-ttu-id="384ea-108">負荷分散を実現するには、ハードウェア負荷分散またはドメインネームシステム (DNS) の負荷分散とハードウェアの負荷分散のいずれかを使用できます。</span><span class="sxs-lookup"><span data-stu-id="384ea-108">To provide the load balancing, you can use either hardware load balancing or domain name system (DNS) load balancing and hardware load balancing.</span></span> <span data-ttu-id="384ea-109">Web サービスにはハードウェア負荷分散が必要であり、DNS 負荷分散単体では、web サービスに必要な機能が提供されません。</span><span class="sxs-lookup"><span data-stu-id="384ea-109">Hardware load balancing is required for the web services, and DNS load balancing alone does not provide the capabilities required for the web services.</span></span>

<span data-ttu-id="384ea-110">次のトピックでは、DNS の負荷分散とハードウェアの負荷分散を使用して、ディレクタープールを展開する場合の計画に関する考慮事項について説明します。</span><span class="sxs-lookup"><span data-stu-id="384ea-110">The following topics describe the planning considerations for deploying a Director pool using DNS load balancing in conjunction with hardware load balancing.</span></span> <span data-ttu-id="384ea-111">ハードウェアの負荷分散は使用するが、ディレクタープールでは DNS の負荷分散を使用しない場合は、そのトポロジの計画要件について説明している「 [Lync Server 2013 のスケーリングされたディレクタープール-ハードウェアロードバランサー](lync-server-2013-scaled-director-pool-hardware-load-balancer.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="384ea-111">If you intend to use hardware load balancing, but not DNS load balancing for the Director pool, see the topic [Scaled Director pool - hardware load balancer in Lync Server 2013](lync-server-2013-scaled-director-pool-hardware-load-balancer.md) that describes the planning requirements for that topology.</span></span>

<span data-ttu-id="384ea-112">![スケーリングされたディレクタープール](images/JJ205142.35a78a7a-b781-4c8f-951e-168451ba6a65(OCS.15).jpg "スケーリングされたディレクタープール")</span><span class="sxs-lookup"><span data-stu-id="384ea-112">![Scaled Director Pool](images/JJ205142.35a78a7a-b781-4c8f-951e-168451ba6a65(OCS.15).jpg "Scaled Director Pool")</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="384ea-113">このセクション中</span><span class="sxs-lookup"><span data-stu-id="384ea-113">In This Section</span></span>

  - [<span data-ttu-id="384ea-114">証明書の概要 - Lync Server 2013 の DNS および HLB による負荷分散</span><span class="sxs-lookup"><span data-stu-id="384ea-114">Certificate summary - DNS and HLB load balanced in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-dns-and-hlb-load-balanced.md)

  - [<span data-ttu-id="384ea-115">ポートの概要 - Lync Server 2013 における DNS および HLB による負荷分散</span><span class="sxs-lookup"><span data-stu-id="384ea-115">Port summary - DNS and HLB load balanced in Lync Server 2013</span></span>](lync-server-2013-port-summary-dns-and-hlb-load-balanced.md)

  - [<span data-ttu-id="384ea-116">DNS の概要 - Lync Server 2013 での DNS と HLB 負荷分散</span><span class="sxs-lookup"><span data-stu-id="384ea-116">DNS summary - DNS and HLB load balanced in Lync Server 2013</span></span>](lync-server-2013-dns-summary-dns-and-hlb-load-balanced.md)

<span data-ttu-id="384ea-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="384ea-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

