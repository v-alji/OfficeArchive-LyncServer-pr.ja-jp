---
title: 'Lync Server 2013: 同時呼び出し'
description: 'Lync Server 2013: 同時呼び出し'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Simultaneous ringing
ms:assetid: df02f919-4d50-4832-9300-6c51f8b4fc56
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994079(v=OCS.15)
ms:contentKeyID: 51803990
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 595c8c1d4ce105e2189002f18733ffae92cff8bf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423821"
---
# <a name="simultaneous-ringing-in-lync-server-2013"></a><span data-ttu-id="e97d4-103">Lync Server 2013 での同時呼び出し</span><span class="sxs-lookup"><span data-stu-id="e97d4-103">Simultaneous ringing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e97d4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e97d4-104">

<span> </span></span></span>

<span data-ttu-id="e97d4-105">_**最終更新日:** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="e97d4-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="e97d4-106">通話先の当事者が同時呼び出しを有効にしている場合、Location-Based ルーティングでは、通話をルーティングする必要があるかどうかを判断するために、発信元の場所と、相手のエンドポイントが分析されます。</span><span class="sxs-lookup"><span data-stu-id="e97d4-106">When the called party has simultaneous ringing enabled, Location-Based Routing analyzes the location of the calling party and the endpoints of the called parties to determine whether the call should be routed.</span></span>

<span data-ttu-id="e97d4-107">次の表は、同時呼び出しが構成されたユーザーを示します。同時呼び出しのターゲット ユーザーは、同じネットワーク サイトのユーザー、異なるネットワーク サイトのユーザー、または不明なネットワーク サイトのユーザーです。</span><span class="sxs-lookup"><span data-stu-id="e97d4-107">The following table illustrates a user configured with simultaneous ringing, and the simultaneous ringing target is a user in the same network site, in a different network site, or in an unknown network site.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e97d4-108">PSTN 着信の対象</span><span class="sxs-lookup"><span data-stu-id="e97d4-108">Incoming PSTN call for</span></span></th>
<th><span data-ttu-id="e97d4-109">呼び出し先と同じネットワーク サイトにある</span><span class="sxs-lookup"><span data-stu-id="e97d4-109">Located in the same network site as callee</span></span></th>
<th><span data-ttu-id="e97d4-110">呼び出し先とは別のネットワーク サイトにある</span><span class="sxs-lookup"><span data-stu-id="e97d4-110">Located in different network site than callee</span></span></th>
<th><span data-ttu-id="e97d4-111">不明のネットワークサイトに配置されている、または Location-Based ルーティング用に有効になっていない</span><span class="sxs-lookup"><span data-stu-id="e97d4-111">Located in unknown network site or not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e97d4-112">Lync ユーザー</span><span class="sxs-lookup"><span data-stu-id="e97d4-112">Lync user</span></span></p></td>
<td><p><span data-ttu-id="e97d4-113">同時呼び出しが許可される</span><span class="sxs-lookup"><span data-stu-id="e97d4-113">Simultaneous ring allowed</span></span></p></td>
<td><p><span data-ttu-id="e97d4-114">同時呼び出しは許可されない</span><span class="sxs-lookup"><span data-stu-id="e97d4-114">Simultaneous ring not allowed</span></span></p></td>
<td><p><span data-ttu-id="e97d4-115">同時呼び出しは許可されない</span><span class="sxs-lookup"><span data-stu-id="e97d4-115">Simultaneous ring not allowed</span></span></p></td>
</tr>
</tbody>
</table>

  
<span data-ttu-id="e97d4-116">次の表は、同じネットワークサイト、別のネットワークサイト、または不明なネットワークサイトの Lync ユーザー (Lync 発信者) からの通話の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="e97d4-116">The following table illustrates a call from a Lync user (i.e. Lync caller) in the same network site, in a different network site, or from an unknown network site.</span></span> <span data-ttu-id="e97d4-117">呼び出し先には、同時呼び出しのターゲット ユーザーとして、PSTN エンドポイント (携帯電話) が構成されています。</span><span class="sxs-lookup"><span data-stu-id="e97d4-117">The callee has a PSTN endpoint (i.e. cellphone) configured as a simultaneous ring target.</span></span> <span data-ttu-id="e97d4-118">このシナリオでは、Location-Based ルーティングによって、呼び出し元の同時呼び出しターゲット (携帯電話) に通話をルーティングするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="e97d4-118">In this scenario, Location-Based Routing will determine whether the call should be routed to the simultaneous ring target (i.e. cellphone) of the callee or not.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e97d4-119">同時呼び出しのターゲット ユーザー</span><span class="sxs-lookup"><span data-stu-id="e97d4-119">Simultaneous ring target</span></span></th>
<th><span data-ttu-id="e97d4-120">呼び出し先と同じネットワーク サイトにある</span><span class="sxs-lookup"><span data-stu-id="e97d4-120">Located in the same network site as callee</span></span></th>
<th><span data-ttu-id="e97d4-121">呼び出し先とは別のネットワーク サイトにある</span><span class="sxs-lookup"><span data-stu-id="e97d4-121">Located in different network site than callee</span></span></th>
<th><span data-ttu-id="e97d4-122">不明のネットワークサイトに配置されている、または Location-Based ルーティング用に有効になっていない</span><span class="sxs-lookup"><span data-stu-id="e97d4-122">Located in unknown network site or not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e97d4-123">PSTN エンドポイント</span><span class="sxs-lookup"><span data-stu-id="e97d4-123">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="e97d4-124">呼び出し元のサイトの音声ルーティング ポリシーによって同時呼び出しが許可される</span><span class="sxs-lookup"><span data-stu-id="e97d4-124">Simultaneous ring allowed through the caller’s site voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="e97d4-125">呼び出し元のサイトの音声ルーティング ポリシーによって同時呼び出しが許可される</span><span class="sxs-lookup"><span data-stu-id="e97d4-125">Simultaneous ring allowed through the caller’s site voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="e97d4-126">場所に基づくルーティングが有効になっていないトランクへの呼び出し元の音声ポリシーによって同時呼び出しが許可される</span><span class="sxs-lookup"><span data-stu-id="e97d4-126">Simultaneous ring allowed through the caller’s voice policy to trunks not enabled for Location-Based Routing</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="e97d4-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="e97d4-127">See Also</span></span>


[<span data-ttu-id="e97d4-128">Lync Server 2013 の場所に基づくルーティングのシナリオ</span><span class="sxs-lookup"><span data-stu-id="e97d4-128">Scenarios for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-location-based-routing.md)  
  

<span data-ttu-id="e97d4-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e97d4-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

