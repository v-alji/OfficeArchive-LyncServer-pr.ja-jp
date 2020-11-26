---
title: 'Lync Server 2013: 場所に基づくルーティングに関する技術的考慮事項'
description: 'Lync Server 2013: Location-Based ルーティングの技術的な考慮事項'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Technical considerations for Location-Based Routing
ms:assetid: 2e2a9199-7c6f-48d3-9adb-3873fc4f8c4e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994027(v=OCS.15)
ms:contentKeyID: 51803936
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 54a025af81ab148ad41f95d0a8cf4f900beb7e00
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423429"
---
# <a name="technical-considerations-for-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="ba240-103">場所に基づくルーティングに関する Lync Server 2013 の技術的考慮事項</span><span class="sxs-lookup"><span data-stu-id="ba240-103">Technical considerations for Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ba240-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ba240-104">

<span> </span></span></span>

<span data-ttu-id="ba240-105">_**最終更新日:** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="ba240-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="ba240-106">ルーティング Location-Based 計画を立てるときは、次のシナリオへの影響を考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ba240-106">When planning Location-Based Routing, you should consider the impact to the following scenarios.</span></span>

<div>

## <a name="disaster-recovery"></a><span data-ttu-id="ba240-107">障害復旧</span><span class="sxs-lookup"><span data-stu-id="ba240-107">Disaster Recovery</span></span>

<span data-ttu-id="ba240-108">プライマリプールからバックアッププールへのフェールオーバー、および通常の操作をプライマリプールに復元したときに、Location-Based ルーティングは、障害発生時と回復時に常に適用されたままになります。</span><span class="sxs-lookup"><span data-stu-id="ba240-108">During a failover from the primary pool to a backup pool as well as when restoring normal operations to the primary pool, Location-Based Routing remains enforced at all times during a disaster and recovery procedure.</span></span>

</div>

<div>

## <a name="survivable-branch-appliance"></a><span data-ttu-id="ba240-109">存続可能ブランチ アプライアンス</span><span class="sxs-lookup"><span data-stu-id="ba240-109">Survivable Branch Appliance</span></span>

<span data-ttu-id="ba240-110">Location-Based ルーティングを構成すると、Survivable Branch アプライアンスに関連付けられているゲートウェイの展開先が計画されます。</span><span class="sxs-lookup"><span data-stu-id="ba240-110">Configuring Location-Based Routing impacts the planning of where you deploy the gateways associated to your Survivable Branch Appliances.</span></span> <span data-ttu-id="ba240-111">SBA に関連付けられているゲートウェイは、Survivable Branch Appliance と同じネットワークサイトにある必要があります。そうしないと、Location-Based ルーティングが構成されている場合に、Survivable Branch アプライアンスをホームとしているユーザーは、発信通話を行うことができなくなります。</span><span class="sxs-lookup"><span data-stu-id="ba240-111">The gateway associated to your SBA must be located in the same network site as your Survivable Branch Appliance; otherwise, users homed on your Survivable Branch Appliance will not be permitted to place outbound calls if Location-Based Routing is configured.</span></span> <span data-ttu-id="ba240-112">Survivable Branch Appliance とセントラルサイト間の WAN 接続がダウンしている場合、Location-Based ルーティング制限は適用されません。</span><span class="sxs-lookup"><span data-stu-id="ba240-112">When the WAN connection between your Survivable Branch Appliance and the central site is down, Location-Based Routing restrictions remains enforced.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ba240-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="ba240-113">See Also</span></span>


[<span data-ttu-id="ba240-114">Lync Server 2013 での場所に基づくルーティングの計画</span><span class="sxs-lookup"><span data-stu-id="ba240-114">Planning for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-planning-for-location-based-routing.md)  
  

<span data-ttu-id="ba240-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ba240-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

