---
title: 'Lync Server 2013: 発信通話'
description: 'Lync Server 2013: 発信通話。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Outgoing calls
ms:assetid: 885ffe6f-cd51-4f21-8d4f-a1ff8d818858
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994049(v=OCS.15)
ms:contentKeyID: 51803960
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e14f19dec35a6da47a2ddd62657d5d087a854f16
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424836"
---
# <a name="outgoing-calls-in-lync-server-2013"></a><span data-ttu-id="d53a8-103">Lync Server 2013 の発信通話</span><span class="sxs-lookup"><span data-stu-id="d53a8-103">Outgoing calls in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d53a8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d53a8-104">

<span> </span></span></span>

<span data-ttu-id="d53a8-105">_**最終更新日:** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="d53a8-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="d53a8-106">Location-Based ルーティングが有効になっているユーザーの発信通話のルーティングは、ユーザーのエンドポイントのネットワークの場所によって影響を受けます。</span><span class="sxs-lookup"><span data-stu-id="d53a8-106">The routing of outbound calls of users enabled for Location-Based Routing is affected by the network location of the user’s endpoint.</span></span> <span data-ttu-id="d53a8-107">次の表では、呼び出し元のエンドポイントの場所に応じて、Location-Based ルーティングが発信通話のルーティングにどのように影響するかを示しています。</span><span class="sxs-lookup"><span data-stu-id="d53a8-107">The following table illustrates how Location-Based Routing affects the routing of outbound calls depending on the location of the caller’s endpoint.</span></span>

### <a name="caller-placing-an-outbound-call-to-the-pstn"></a><span data-ttu-id="d53a8-108">発信者から PSTN への発信通話</span><span class="sxs-lookup"><span data-stu-id="d53a8-108">Caller placing an outbound call to the PSTN</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="d53a8-109">ユーザーのエンドポイントが、場所に基づくルーティングが有効なネットワーク サイトにある</span><span class="sxs-lookup"><span data-stu-id="d53a8-109">User endpoint located in a network site enabled for Location-Based Routing</span></span></th>
<th><span data-ttu-id="d53a8-110">ユーザーのエンドポイントが不明なネットワーク サイトまたは場所に基づくルーティングが有効でないネットワーク サイトにある</span><span class="sxs-lookup"><span data-stu-id="d53a8-110">User endpoint located in unknown network site or not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d53a8-111">発信の承認</span><span class="sxs-lookup"><span data-stu-id="d53a8-111">Authorization of outbound calls</span></span></p></td>
<td><p><span data-ttu-id="d53a8-112">通話はユーザーの音声ポリシーに基づいて承認される</span><span class="sxs-lookup"><span data-stu-id="d53a8-112">Call is authorized based on user’s voice policy</span></span></p></td>
<td><p><span data-ttu-id="d53a8-113">通話はユーザーの音声ポリシーに基づいて承認される</span><span class="sxs-lookup"><span data-stu-id="d53a8-113">Call is authorized based on user’s voice policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d53a8-114">発信通話のルーティング</span><span class="sxs-lookup"><span data-stu-id="d53a8-114">Routing of outbound call</span></span></p></td>
<td><p><span data-ttu-id="d53a8-115">通話はネットワーク サイトの音声ルーティング ポリシーに従ってルーティングされる</span><span class="sxs-lookup"><span data-stu-id="d53a8-115">Call is routed according to the network site’s voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="d53a8-116">通話はユーザーの音声ポリシーに従い、場所に基づくルーティングが有効になっていないトランク (使用可能な場合) のみを経由してルーティングされる</span><span class="sxs-lookup"><span data-stu-id="d53a8-116">Call is routed according to user’s voice policy and only through trunks not enabled for Location-Based Routing (if available)</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="d53a8-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="d53a8-117">See Also</span></span>


[<span data-ttu-id="d53a8-118">Lync Server 2013 の場所に基づくルーティングのシナリオ</span><span class="sxs-lookup"><span data-stu-id="d53a8-118">Scenarios for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-location-based-routing.md)  
  

<span data-ttu-id="d53a8-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d53a8-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

