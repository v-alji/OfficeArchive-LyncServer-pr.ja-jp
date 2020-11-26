---
title: 'Lync Server 2013: 着信通話'
description: 'Lync Server 2013: 着信通話。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Incoming calls
ms:assetid: 65b9c1b4-6af7-4527-8c33-22c4442bd209
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994038(v=OCS.15)
ms:contentKeyID: 51803948
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3a72c7fc378240f9751eae8e6c24e9cc601b08d3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427300"
---
# <a name="incoming-calls-in-lync-server-2013"></a><span data-ttu-id="28a53-103">Lync Server 2013 着信通話</span><span class="sxs-lookup"><span data-stu-id="28a53-103">Incoming calls in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="28a53-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="28a53-104">

<span> </span></span></span>

<span data-ttu-id="28a53-105">_**最終更新日:** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="28a53-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="28a53-106">Location-Based ルーティングが有効になっているユーザーに対して呼び出される着信のルーティングは、ユーザーのエンドポイントの場所によって異なります。</span><span class="sxs-lookup"><span data-stu-id="28a53-106">The routing of incoming calls to users enabled for Location-Based Routing depends on the location of the user’s endpoint.</span></span> <span data-ttu-id="28a53-107">着信通話のルーティングは、次のように影響されます。</span><span class="sxs-lookup"><span data-stu-id="28a53-107">The routing of incoming calls is affected in the following way.</span></span> <span data-ttu-id="28a53-108">ユーザーが Location-Based ルーティングを有効にしたネットワークサイトにあるエンドポイントへの着信通話を行っていて、そのエンドポイントが PSTN ゲートウェイと同じネットワークサイトにある場合、通話はルーティングされます。</span><span class="sxs-lookup"><span data-stu-id="28a53-108">If a user has an incoming call to an endpoint located in a Location-Based Routing enabled network site, and the endpoint is located in the same network site as the PSTN gateway, the call will be routed.</span></span> <span data-ttu-id="28a53-109">ユーザーが Location-Based ルーティングを有効にしたネットワークサイトにあるエンドポイントへの着信通話を行っていて、そのエンドポイントが PSTN ゲートウェイとは異なるネットワークサイトにある場合、通話はルーティングされません。</span><span class="sxs-lookup"><span data-stu-id="28a53-109">If a user has an incoming call to an endpoint located in a Location-Based Routing enabled network site, and the endpoint is located in a different network site than the PSTN gateway, the call will not be routed.</span></span> <span data-ttu-id="28a53-110">着信通話の発信元の PSTN ゲートウェイと同じネットワーク サイトにエンドポイントがない場合、着信通話はユーザーのボイスメールに直接ルーティングされ、不在着信通知が呼び出し先に送信されます。</span><span class="sxs-lookup"><span data-stu-id="28a53-110">When a user has no endpoints located in the same network site as the PSTN gateway where the incoming call is originating from, the incoming call will be routed directly to the user’s voicemail and a missed call notification will be sent to the called party.</span></span>

<span data-ttu-id="28a53-111">Location-Based ルーティングが有効になっているユーザーの着信の転送設定は引き続き適用されますが、転送された通話には、ユーザーの Location-Based ルーティングの制限が適用されます。</span><span class="sxs-lookup"><span data-stu-id="28a53-111">The call forwarding settings of a user that is enabled for Location-Based Routing will continue to be enforced, however, calls forwarded will be subject to Location-Based Routing restrictions of the user.</span></span>

<span data-ttu-id="28a53-112">次の表は、呼び出し先のエンドポイントの場所に応じて、Location-Based ルーティングが着信のルーティングにどのように影響するかを示しています。</span><span class="sxs-lookup"><span data-stu-id="28a53-112">The following table illustrates how Location-Based Routing affects the routing of inbound calls depending on the location of the callee’s endpoint.</span></span> <span data-ttu-id="28a53-113">PSTN ゲートウェイのネットワークサイトが Location-Based ルーティング用に有効になっていて、Location-Based ルーティングでは、同じネットワークサイト内のエンドポイントへの PSTN 通話のルーティングのみが許可されています。</span><span class="sxs-lookup"><span data-stu-id="28a53-113">The network site of the PSTN gateway is enabled for Location-Based Routing, and Location-Based Routing only permits routing of PSTN calls to endpoints within the same network site.</span></span>

### <a name="callee-receiving-an-inbound-call-from-the-pstn"></a><span data-ttu-id="28a53-114">呼び出し先が PSTN から着信通話を受信する</span><span class="sxs-lookup"><span data-stu-id="28a53-114">Callee receiving an inbound call from the PSTN</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="28a53-115">呼び出し先のエンドポイントが PSTN ゲートウェイと同じネットワーク サイトにある</span><span class="sxs-lookup"><span data-stu-id="28a53-115">Callee’s endpoint located in the same network site as PSTN gateway</span></span></th>
<th><span data-ttu-id="28a53-116">呼び出し先のエンドポイントが PSTN ゲートウェイと同じネットワーク サイトにない</span><span class="sxs-lookup"><span data-stu-id="28a53-116">Callee’s endpoint not located in the same network site as PSTN gateway</span></span></th>
<th><span data-ttu-id="28a53-117">呼び出し先のエンドポイントが不明なネットワーク サイトにある、または場所に基づくルーティングが有効になっていない</span><span class="sxs-lookup"><span data-stu-id="28a53-117">Callee’s endpoint located in unknown network site or not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="28a53-118">着信 PSTN 通話のルーティング</span><span class="sxs-lookup"><span data-stu-id="28a53-118">Routing of inbound PSTN call</span></span></p></td>
<td><p><span data-ttu-id="28a53-119">着信通話は呼び出し先のエンドポイントにルーティングされる</span><span class="sxs-lookup"><span data-stu-id="28a53-119">Incoming call is routed to callee’s endpoints</span></span></p></td>
<td><p><span data-ttu-id="28a53-120">着信通話は呼び出し先のエンドポイントにルーティングされない</span><span class="sxs-lookup"><span data-stu-id="28a53-120">Incoming call is not routed to callee’s endpoints</span></span></p></td>
<td><p><span data-ttu-id="28a53-121">着信通話は呼び出し先のエンドポイントにルーティングされない</span><span class="sxs-lookup"><span data-stu-id="28a53-121">Incoming call is not routed to callee’s endpoints</span></span></p></td>
</tr>
</tbody>
</table>

  

<div>

## <a name="see-also"></a><span data-ttu-id="28a53-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="28a53-122">See Also</span></span>


[<span data-ttu-id="28a53-123">Lync Server 2013 の場所に基づくルーティングのシナリオ</span><span class="sxs-lookup"><span data-stu-id="28a53-123">Scenarios for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-location-based-routing.md)  
  

<span data-ttu-id="28a53-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="28a53-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

