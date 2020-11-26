---
title: 'Lync Server 2013: ユーザーの場所'
description: 'Lync Server 2013: ユーザーの場所。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: User's location
ms:assetid: ce57941d-086b-448e-8ada-c7d636a2a1c9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994073(v=OCS.15)
ms:contentKeyID: 51803984
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a92ec780809cdb3e1ee582ce6c348c884bbb5890
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439171"
---
# <a name="users-location-in-lync-server-2013"></a><span data-ttu-id="20f11-103">Lync Server 2013 のユーザーの場所</span><span class="sxs-lookup"><span data-stu-id="20f11-103">User's location in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="20f11-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="20f11-104">

<span> </span></span></span>

<span data-ttu-id="20f11-105">_**最終更新日:** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="20f11-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="20f11-106">Location-Based ルーティングでは、E9 によって使用されている Lync Server で定義されているものと同じネットワーク領域、サイト、サブネットを利用します。これは、PSTN の有料サービスを回避するために、通話ルーティングの制限を適用するために、着信ルーティングの制限を適用するために、</span><span class="sxs-lookup"><span data-stu-id="20f11-106">Location-Based Routing leverages the same network regions, sites and subnets as defined in Lync Server used by E9-1-1, CAC and Media Bypass to apply call routing restrictions to prevent PSTN toll bypass.</span></span> <span data-ttu-id="20f11-107">ユーザーの位置情報は、ユーザーの Lync エンドポイントの IP サブネットによって接続されます。</span><span class="sxs-lookup"><span data-stu-id="20f11-107">A user’s location is determined by the IP subnet of the user’s Lync endpoint(s) are connected from.</span></span> <span data-ttu-id="20f11-108">各 IP サブネットは、ネットワーク サイトに関連付けられ、管理者が定義したネットワーク地域に集約されます。</span><span class="sxs-lookup"><span data-stu-id="20f11-108">Each IP subnet is associated to a network site, which are aggregated into network regions defined by the administrator.</span></span> <span data-ttu-id="20f11-109">場所に基づくルーティングは、ユーザーのネットワーク サイトに基づいて適用されます。</span><span class="sxs-lookup"><span data-stu-id="20f11-109">Location-Based Routing is enforced based on the user’s network site.</span></span>

<span data-ttu-id="20f11-110">ルーティングルールは、ネットワークサイト単位で適用されます。つまり、指定したルールセットは、同じネットワークサイト内に存在する Location-Based ルーティングで有効になっているすべてのエンドポイントに適用されます。 Location-Based</span><span class="sxs-lookup"><span data-stu-id="20f11-110">Location-Based Routing rules are applied on a per network site basis, meaning that a given set of rules will be applied to all endpoints enabled for Location-Based Routing that are located within the same network site.</span></span> <span data-ttu-id="20f11-111">管理者は、必要なネットワークサイトにルーティング Location-Based を適用できます。</span><span class="sxs-lookup"><span data-stu-id="20f11-111">Administrators can apply Location-Based Routing to network sites that require it.</span></span>

<span data-ttu-id="20f11-112">ボイスルーティングポリシーは、ネットワークサイトごとに定義できます。このような特定の PSTN ゲートウェイは、ネットワークサイト内のすべてのユーザーが PSTN 電話番号に発信するために使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="20f11-112">Voice routing policies can be defined on a per network site basis to define a particular PSTN gateway that should be used by all users located in the network site to call PSTN phone numbers.</span></span> <span data-ttu-id="20f11-113">このような音声ルーティングポリシーは、ユーザーのボイスポリシーによって定義されたルーティングによって、Location-Based ルーティング用に有効になっているネットワークサイトに配置されている場合に、ルーティングが有効になっていると、そのルーティングが、Location-Based ルーティング用に有効になっている他の PSTN ゲートウェイ経由でルーティングできなくなります。</span><span class="sxs-lookup"><span data-stu-id="20f11-113">Such voice routing policies will take precedence over the routing defined by the user’s voice policy when the user is located in a network site enabled for Location-Based Routing, and it will prevent the routing of calls via other PSTN gateways that are enabled for Location-Based Routing.</span></span> <span data-ttu-id="20f11-114">Lync ユーザーが PSTN 通話を発信すると、ユーザーの音声ポリシーによって、そのユーザーが通話を発信することを許可されているかどうかが決定されます。</span><span class="sxs-lookup"><span data-stu-id="20f11-114">When a Lync user places a PSTN call, the user’s voice policy determines whether the user can be authorized to place the call.</span></span> <span data-ttu-id="20f11-115">ユーザーが通話を発信することをユーザーに許可している場合、Location-Based ルーティングによって、通話の発信元となる PSTN ゲートウェイが決定されます。</span><span class="sxs-lookup"><span data-stu-id="20f11-115">If the user’s voice policy allows the user to place the call, Location-Based Routing determines which PSTN gateway the call should egress from.</span></span> <span data-ttu-id="20f11-116">Location-Based ルーティングでは、ユーザーの位置に基づいてこの決定が行われます。</span><span class="sxs-lookup"><span data-stu-id="20f11-116">Location-Based Routing makes this determination based on the user’s location.</span></span>

<span data-ttu-id="20f11-117">ユーザーの場所は、次の方法で分類できます。</span><span class="sxs-lookup"><span data-stu-id="20f11-117">A user location can be categorized in the following ways:</span></span>

  - <span data-ttu-id="20f11-118">ユーザーは、同じネットワークサイト (office など) に配置された PSTN ゲートウェイ上で、Location-Based ルーティングと彼の DID (直接の外線発信番号) で終了する既知のネットワークサイトにあります。</span><span class="sxs-lookup"><span data-stu-id="20f11-118">The user is located in a known network site enabled for Location-Based Routing and his DID (Direct Inward Dial) number terminates on a PSTN gateway placed in the same network site (i.e. office).</span></span> <span data-ttu-id="20f11-119">発信通話のルーティングは、ユーザーが配置されているネットワークサイトの音声ルーティングポリシーを通じて行われます。</span><span class="sxs-lookup"><span data-stu-id="20f11-119">The routing of outbound calls will be through the voice routing policy of the network site in which the user is located.</span></span> <span data-ttu-id="20f11-120">ユーザーへの着信 PSTN 通話は、PSTN ゲートウェイと同じネットワークサイトに配置されているエンドポイントにルーティングされます。</span><span class="sxs-lookup"><span data-stu-id="20f11-120">Incoming PSTN calls to the user are routed to endpoints that are located in the same network site as the PSTN gateway.</span></span>

  - <span data-ttu-id="20f11-p105">ユーザーが、PSTN ゲートウェイがあるネットワーク サイトとは異なる既知のネットワーク サイトに位置する (ユーザーが企業内の別のオフィスに出張している場合など)。発信通話のルーティングでは、ユーザーが位置するネットワーク サイトの音声ルーティング ポリシーを使用します。PSTN 料が適切に課金されるようにするために、ユーザーへの着信した PSTN 通話は、PSTN ゲートウェイとは異なるサイトにあるエンドポイントにルーティングされません。</span><span class="sxs-lookup"><span data-stu-id="20f11-p105">The user is located in a known network site that is in different from the network site where the PSTN gateway is located. (i.e. the user traveled to another corporate office). The routing of outbound calls will be using the voice routing policy of the network site in which the user is located. Incoming PSTN calls to the user will not be routed to endpoints that are located in different sites than the PSTN gateway to prevent PSTN toll bypassing.</span></span>

  - <span data-ttu-id="20f11-125">Lync Server の展開には未知のネットワークサイトにいるユーザーがいる場合、発信通話のルーティングは、ユーザーに割り当てられているボイスポリシーに基づいて、Location-Based ルーティング制限にバインドされていない PSTN ゲートウェイに適用されます。</span><span class="sxs-lookup"><span data-stu-id="20f11-125">When a user is located in a network site that is unknown to the Lync Server deployment, the routing of outbound calls will be based on the voice policy assigned to the user to PSTN gateways not bound to Location-Based Routing restrictions.</span></span> <span data-ttu-id="20f11-126">PSTN 料が適切に課金されるようにするために、着信した PSTN 通話は、不明なネットワーク サイトにあるエンドポイントにルーティングされません。</span><span class="sxs-lookup"><span data-stu-id="20f11-126">Incoming PSTN calls will not be routed to endpoints that are located in unknown network sites to prevent PSTN toll bypassing.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="20f11-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="20f11-127">See Also</span></span>


[<span data-ttu-id="20f11-128">Lync Server 2013 の場所に基づくルーティングのガイダンス</span><span class="sxs-lookup"><span data-stu-id="20f11-128">Guidance for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-guidance-for-location-based-routing.md)  
  

<span data-ttu-id="20f11-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="20f11-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

