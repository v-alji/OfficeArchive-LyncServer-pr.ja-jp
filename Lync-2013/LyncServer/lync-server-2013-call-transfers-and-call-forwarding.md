---
title: 'Lync Server 2013: 通話転送と着信転送'
description: 'Lync Server 2013: 着信の転送と着信の転送。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call transfers and call forwarding
ms:assetid: 978610ec-63c7-4cf6-ad7a-9ef91559bf12
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994051(v=OCS.15)
ms:contentKeyID: 51803962
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d9359cb64b386d022eab33e4523dfaccf784075b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435685"
---
# <a name="call-transfers-and-call-forwarding-in-lync-server-2013"></a><span data-ttu-id="bcc1e-103">Lync Server 2013 の通話転送と着信転送</span><span class="sxs-lookup"><span data-stu-id="bcc1e-103">Call transfers and call forwarding in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bcc1e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bcc1e-104">

<span> </span></span></span>

<span data-ttu-id="bcc1e-105">_**最終更新日:** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="bcc1e-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="bcc1e-106">PSTN エンドポイントが含まれている場合、Location-Based ルーティングは、calle のエンドポイントの場所と、通話が転送または転送されるエンドポイント (転送/転送ターゲット) を分析します。</span><span class="sxs-lookup"><span data-stu-id="bcc1e-106">When a PSTN endpoint is involved, Location-Based Routing analyzes the location of the calle’s endpoint and the endpoint where the call will be transferred or forwarded to (i.e. transfer/forward target).</span></span> <span data-ttu-id="bcc1e-107">Location-Based ルーティングは、両方のエンドポイントの場所に応じて、通話を転送するか転送するかを決定します。</span><span class="sxs-lookup"><span data-stu-id="bcc1e-107">Location-Based Routing determines whether the call should be transferred or forwarded depending on the location of both endpoints.</span></span>

<span data-ttu-id="bcc1e-108">次の表は、PSTN エンドポイントを使用した通話での Lync ユーザーのシナリオと、Lync ユーザーが別の Lync ユーザーに通話を転送するシナリオを示しています。</span><span class="sxs-lookup"><span data-stu-id="bcc1e-108">The following table illustrates the scenario of a Lync user in a call with a PSTN endpoint, and the Lync user transfers the call to another Lync user.</span></span> <span data-ttu-id="bcc1e-109">Transferee のエンドポイントのネットワークサイトの場所に応じて、Location-Based ルーティングは、通話転送または転送のルーティングに影響します。</span><span class="sxs-lookup"><span data-stu-id="bcc1e-109">Depending on the network site location of the transferee’s endpoint, Location-Based Routing affects the routing of the call transfer or forward.</span></span>

### <a name="initiating-call-transfer-or-forward"></a><span data-ttu-id="bcc1e-110">通話転送または着信転送の開始</span><span class="sxs-lookup"><span data-stu-id="bcc1e-110">Initiating call transfer or forward</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bcc1e-111">通話転送または着信転送を開始するユーザー</span><span class="sxs-lookup"><span data-stu-id="bcc1e-111">User initiating the call transfer/forward</span></span></th>
<th><span data-ttu-id="bcc1e-112">ターゲット エンドポイントが、通話転送または着信転送を開始するユーザーと同じネットワーク サイトにある</span><span class="sxs-lookup"><span data-stu-id="bcc1e-112">Target endpoint is in same network site as user initiating call transfer or forward</span></span></th>
<th><span data-ttu-id="bcc1e-113">ターゲット エンドポイントが、通話転送または着信転送を開始するユーザーとは別のネットワーク サイトにある</span><span class="sxs-lookup"><span data-stu-id="bcc1e-113">Target endpoint is in different network site as user initiating call transfer or forward</span></span></th>
<th><span data-ttu-id="bcc1e-114">ターゲットエンドポイントが不明なネットワークサイトにあるか、Location-Based ルーティング用に有効になっていないネットワークサイトにある</span><span class="sxs-lookup"><span data-stu-id="bcc1e-114">Target endpoint is in unknown network site or network site not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bcc1e-115">Lync ユーザー</span><span class="sxs-lookup"><span data-stu-id="bcc1e-115">Lync user</span></span></p></td>
<td><p><span data-ttu-id="bcc1e-116">通話または着信を転送できます。</span><span class="sxs-lookup"><span data-stu-id="bcc1e-116">Call forward or transfer is allowed</span></span></p></td>
<td><p><span data-ttu-id="bcc1e-117">通話または着信を転送できません。</span><span class="sxs-lookup"><span data-stu-id="bcc1e-117">Call forward or transfer is not allowed</span></span></p></td>
<td><p><span data-ttu-id="bcc1e-118">通話または着信を転送できません。</span><span class="sxs-lookup"><span data-stu-id="bcc1e-118">Call forward or transfer is not allowed</span></span></p></td>
</tr>
</tbody>
</table>

  

<span data-ttu-id="bcc1e-119">たとえば、PSTN エンドポイントでの Lync ユーザーは、同じネットワークサイト内の別の Lync ユーザーに通話を転送します。</span><span class="sxs-lookup"><span data-stu-id="bcc1e-119">For example: a Lync user in a call with a PSTN endpoint transfers the call to another Lync user that is in the same network site.</span></span> <span data-ttu-id="bcc1e-120">この場合、通話の転送が許可されます。</span><span class="sxs-lookup"><span data-stu-id="bcc1e-120">In this case, the call transfer is allowed.</span></span>

<span data-ttu-id="bcc1e-121">次の表は、別の Lync ユーザーとの通話での Lync ユーザーのシナリオと、いずれかのユーザーが通話を PSTN エンドポイントに転送するシナリオを示しています。</span><span class="sxs-lookup"><span data-stu-id="bcc1e-121">The following table illustrates the scenario of a Lync user in a call with another Lync user, and one of the users transfers the call to a PSTN endpoint.</span></span> <span data-ttu-id="bcc1e-122">一方のユーザーが通話を PSTN エンドポイントに転送した場合に、通話の転送先ユーザーの場所によって、場所に基づくルーティングが通話にどのように影響するかを表しています。</span><span class="sxs-lookup"><span data-stu-id="bcc1e-122">Depending on the location of the user the call is being transferred to, the table details how Location-Based Routing affects the call.</span></span>

### <a name="call-transfer-or-forward-to-pstn-endpoint"></a><span data-ttu-id="bcc1e-123">PSTN エンドポイントへの通話転送または着信転送</span><span class="sxs-lookup"><span data-stu-id="bcc1e-123">Call transfer or forward to PSTN endpoint</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bcc1e-124">通話/着信転送エンドポイント ターゲット</span><span class="sxs-lookup"><span data-stu-id="bcc1e-124">Call transfer/forward endpoint target</span></span></th>
<th><span data-ttu-id="bcc1e-125">同じネットワークサイト内の Lync ユーザー</span><span class="sxs-lookup"><span data-stu-id="bcc1e-125">Lync users in same network site</span></span></th>
<th><span data-ttu-id="bcc1e-126">異なるネットワークサイトの Lync ユーザー</span><span class="sxs-lookup"><span data-stu-id="bcc1e-126">Lync users in different network sites</span></span></th>
<th><span data-ttu-id="bcc1e-127">不明のネットワークサイトまたはネットワークサイト内の一方または両方の Lync ユーザーが Location-Based ルーティング用に有効になっていない</span><span class="sxs-lookup"><span data-stu-id="bcc1e-127">One or both Lync users in unknown network site or network site not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bcc1e-128">PSTN エンドポイント</span><span class="sxs-lookup"><span data-stu-id="bcc1e-128">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="bcc1e-129">転送先ユーザーのサイトの音声ルーティング ポリシーによって、通話または着信の転送が許可される</span><span class="sxs-lookup"><span data-stu-id="bcc1e-129">Call forward or transfer allowed by the transferred user’s site voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="bcc1e-130">転送先ユーザーのサイトの音声ルーティング ポリシーによって、通話または着信の転送が許可される</span><span class="sxs-lookup"><span data-stu-id="bcc1e-130">Call forward or transfer allowed by the transferred user’s site voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="bcc1e-131">通話または着信の転送は、転送先ユーザーの音声ポリシーによって、場所に基づくルーティングが有効になっていないトランクのみを経由して許可される</span><span class="sxs-lookup"><span data-stu-id="bcc1e-131">Call forward or transfer allowed by the transferred user’s voice policy only through trunks not enabled for Location-Based Routing</span></span></p></td>
</tr>
</tbody>
</table>

  
<span data-ttu-id="bcc1e-132">たとえば、同じネットワークサイト内の別の Lync ユーザーとの通話で Lync ユーザーが通話を PSTN エンドポイントに転送し、通話転送が許可されているとします。</span><span class="sxs-lookup"><span data-stu-id="bcc1e-132">For example: a Lync user in a call with another Lync user that is in the same network site transfers the call to a PSTN endpoint and the call transfer is allowed.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="bcc1e-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="bcc1e-133">See Also</span></span>


[<span data-ttu-id="bcc1e-134">Lync Server 2013 の場所に基づくルーティングのシナリオ</span><span class="sxs-lookup"><span data-stu-id="bcc1e-134">Scenarios for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-location-based-routing.md)  
  

<span data-ttu-id="bcc1e-135"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bcc1e-135"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

