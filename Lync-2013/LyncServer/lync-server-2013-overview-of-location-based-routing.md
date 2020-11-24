---
title: 'Lync Server 2013: Location-Based ルーティングの概要'
description: 'Lync Server 2013: Location-Based ルーティングの概要'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of Location-Based Routing
ms:assetid: 4aa494bd-0d66-4335-b9e8-f758d44a7202
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994032(v=OCS.15)
ms:contentKeyID: 51803941
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0b1e026791a8562629231b91b58d7e7eff569ffa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399680"
---
# <a name="overview-of-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="9c41d-103">Lync Server 2013 での Location-Based ルーティングの概要</span><span class="sxs-lookup"><span data-stu-id="9c41d-103">Overview of Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9c41d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9c41d-104">

<span> </span></span></span>

<span data-ttu-id="9c41d-105">_**最終更新日:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="9c41d-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="9c41d-p101">場所に基づいたルーティングでは、国内および国際 PSTN 通話のルーティングを変更する新しいルール セットを導入して、課金回避を防止します。場所に基づいたルーティングによって、これらのルールを特定の地域、ゲートウェイ、ユーザー群のみに柔軟に適用できます。</span><span class="sxs-lookup"><span data-stu-id="9c41d-p101">Location-Based Routing introduces a new set of rules that modifies the routing of national and international PSTN calls to prevent toll bypass. Location-Based Routing provides the flexibility to scope these rules to specific regions, specific gateways or to specific set of users only.</span></span>

<span data-ttu-id="9c41d-108">次のシナリオでは、ルーティングで適用 Location-Based 主な種類の制限について説明します。</span><span class="sxs-lookup"><span data-stu-id="9c41d-108">The following scenarios illustrate the main types of restrictions Location-Based Routing can enforce:</span></span>

  - <span data-ttu-id="9c41d-109">出口通話– Location-Based ルーティングでは、発信者が PSTN の電話と同じ地域に配置されている PSTN ゲートウェイからの出口を強制することができます。これにより、発信者は、別の地域にある PSTN ゲートウェイからの着信を拒否します。</span><span class="sxs-lookup"><span data-stu-id="9c41d-109">Egress calls – Location-Based Routing can enforce outgoing calls to egress from a PSTN gateway that is located in the same region as where the caller is to prevent PSTN toll bypass, which prevents calls to egress from a PSTN gateway located in a different region as the caller.</span></span>

  - <span data-ttu-id="9c41d-110">受信した通話– Location-Based ルーティングは、着信通話を転送する PSTN ゲートウェイが、相手の Lync ユーザーと同じ地域に配置されていない場合に、着信する PSTN 通話が Lync エンドポイントを呼び出すことを防止できます。</span><span class="sxs-lookup"><span data-stu-id="9c41d-110">Ingress calls – Location-Based Routing can prevent incoming PSTN calls to ring Lync endpoints if the PSTN gateway routing the incoming call is not located in the same region as the called Lync user.</span></span>

  - <span data-ttu-id="9c41d-111">不明な地域– Location-Based ルーティングは、不明な場所 (インターネット経由で接続されているか、不明な地域にいるリモートユーザー) との間で、着信と発信の PSTN 通話を制限します。</span><span class="sxs-lookup"><span data-stu-id="9c41d-111">Unknown regions – Location-Based Routing restricts incoming and outgoing PSTN calls to and from users that are located in undetermined locations (i.e. remote users connecting from the Internet or located in unknown regions).</span></span>

  - <span data-ttu-id="9c41d-112">国際地域– Location-Based ルーティングでは、ユーザーの位置情報に対してローカルゲートウェイが見つからない場合は、国際 PSTN ゲートウェイを介した発信通話のルーティングが適用されます。</span><span class="sxs-lookup"><span data-stu-id="9c41d-112">International regions – Location-Based Routing enforces routing of outgoing calls through international PSTN gateways if a gateway local to the user’s location cannot be found.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="9c41d-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="9c41d-113">See Also</span></span>


[<span data-ttu-id="9c41d-114">Lync Server 2013 での場所に基づくルーティングの計画</span><span class="sxs-lookup"><span data-stu-id="9c41d-114">Planning for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-planning-for-location-based-routing.md)  
  

<span data-ttu-id="9c41d-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9c41d-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

