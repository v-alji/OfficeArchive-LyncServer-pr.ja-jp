---
title: 'Lync Server 2013: ディレクターに必要なコンポーネント'
description: 'Lync Server 2013: ディレクターに必要なコンポーネント。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components required for the Director
ms:assetid: 15c7c8d4-b93f-4386-b2d1-d76dab8f801e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398228(v=OCS.15)
ms:contentKeyID: 48183502
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 57f717b9ddb9557f212321cdab075713a4b85c2d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398240"
---
# <a name="components-required-for-the-director-in-lync-server-2013"></a><span data-ttu-id="2f81a-103">Lync Server 2013 のディレクターに必要なコンポーネント</span><span class="sxs-lookup"><span data-stu-id="2f81a-103">Components required for the Director in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2f81a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2f81a-104">

<span> </span></span></span>

<span data-ttu-id="2f81a-105">_**最終更新日:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="2f81a-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="2f81a-106">ディレクターを作成して構成するために必要なコンポーネントは、ディレクターサーバーの役割を展開することだけです。</span><span class="sxs-lookup"><span data-stu-id="2f81a-106">The only component required to create and configure a Director is to deploy the Director server role.</span></span> <span data-ttu-id="2f81a-107">これを行うには、トポロジビルダーを使用し、1台のコンピュータープールまたはディレクタープールノードの複数のコンピュータープールを定義します。</span><span class="sxs-lookup"><span data-stu-id="2f81a-107">You do this by using Topology Builder and define either a single computer pool or a multiple computer pool in the Director pool node.</span></span> <span data-ttu-id="2f81a-108">ディレクターまたはディレクタープールを定義したら、ディレクターになるコンピューターで Lync Server Deployment ウィザードを実行します。</span><span class="sxs-lookup"><span data-stu-id="2f81a-108">After you have defined the Director or Director pool, run the Lync Server Deployment Wizard on the computer that will be a Director.</span></span> <span data-ttu-id="2f81a-109">ディレクタープールの場合は、プールのメンバーになっている各サーバーで Lync Server Deployment ウィザードを実行します。</span><span class="sxs-lookup"><span data-stu-id="2f81a-109">In the case of a Director pool, you run the Lync Server Deployment Wizard on each server that will be a member of the pool.</span></span>

<div>

## <a name="topologies"></a><span data-ttu-id="2f81a-110">トポロジー</span><span class="sxs-lookup"><span data-stu-id="2f81a-110">Topologies</span></span>

<span data-ttu-id="2f81a-111">1つのディレクターサーバーまたはディレクタープールを実装できます。</span><span class="sxs-lookup"><span data-stu-id="2f81a-111">You can implement a single Director server or a Director pool.</span></span> <span data-ttu-id="2f81a-112">ディレクターは常に個別のサーバーまたはプールであり、Lync Server 2013 では他のサーバーの役割とは関係ありません。</span><span class="sxs-lookup"><span data-stu-id="2f81a-112">The Director is always a separate server or pool, not collocated with any other server role in Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="2f81a-113">ディレクターを展開しない場合は、フロントエンドサーバーまたはフロントエンドプールによってディレクターの役割が想定されます。</span><span class="sxs-lookup"><span data-stu-id="2f81a-113">If you do not deploy Directors, the Front End Server or Front End pool will assume the Director role.</span></span>



</div>

<span data-ttu-id="2f81a-114">ディレクターのプールは、負荷分散されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f81a-114">A pool of Directors must be load balanced.</span></span> <span data-ttu-id="2f81a-115">次のいずれかの操作を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="2f81a-115">You can do one of the following:</span></span>

  - <span data-ttu-id="2f81a-116">その他の種類のトラフィックに対して、web サービスとドメインネームシステム (DNS) 負荷分散用のハードウェアロードバランサーを使用するトポロジを作成します。</span><span class="sxs-lookup"><span data-stu-id="2f81a-116">Create a topology that uses a hardware load balancer for web services and Domain Name System (DNS) load balancing for the other traffic types.</span></span>
    
    [<span data-ttu-id="2f81a-117">拡張ディレクター プール - Lync Server 2013 の DNS 負荷分散とロード バランサー機器</span><span class="sxs-lookup"><span data-stu-id="2f81a-117">Scaled Director pool - DNS load balancing and hardware load balancer in Lync Server 2013</span></span>](lync-server-2013-scaled-director-pool-dns-load-balancing-and-hardware-load-balancer.md)

  - <span data-ttu-id="2f81a-118">ハードウェアロードバランサーを使用するトポロジを作成して、ディレクタープールに必要な負荷分散を行います。</span><span class="sxs-lookup"><span data-stu-id="2f81a-118">Create a topology that uses a hardware load balancer for load balancing needed for the Director pool.</span></span>
    
    [<span data-ttu-id="2f81a-119">拡張ディレクター プール - Lync Server 2013 のハードウェア負荷分散</span><span class="sxs-lookup"><span data-stu-id="2f81a-119">Scaled Director pool - hardware load balancer in Lync Server 2013</span></span>](lync-server-2013-scaled-director-pool-hardware-load-balancer.md)

<span data-ttu-id="2f81a-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2f81a-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

