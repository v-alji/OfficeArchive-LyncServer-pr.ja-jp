---
title: 'Lync Server 2013: ビデオ会議の相互運用性に関する考慮事項'
description: 'Lync Server 2013: ビデオ会議の相互運用性に関する考慮事項。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Interoperability considerations for video conferencing
ms:assetid: 31ead3b5-ed95-42d4-96e2-7d9403d5c026
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204790(v=OCS.15)
ms:contentKeyID: 48183782
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 89675954ea4c4f188f50aab8fb2cb49494bcc247
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426789"
---
# <a name="interoperability-considerations-for-video-conferencing-in-lync-server-2013"></a><span data-ttu-id="2aa1e-103">Lync Server 2013 でのビデオ会議の相互運用性に関する考慮事項</span><span class="sxs-lookup"><span data-stu-id="2aa1e-103">Interoperability considerations for video conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2aa1e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2aa1e-104">

<span> </span></span></span>

<span data-ttu-id="2aa1e-105">_**最終更新日:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="2aa1e-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="2aa1e-106">このセクションでは、従来のクライアントと Lync Server 2013 プールの間、または Lync Server 2013 クライアントと従来のプールの間で相互運用性がある場合に、移行の共存フェーズでのユーザーエクスペリエンスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="2aa1e-106">This section describes the user experience during the coexistence phase of migration, when there is interoperability between legacy clients and a Lync Server 2013 pool or Lync Server 2013 clients and a legacy pool.</span></span>

<div>

## <a name="lync-server-2013-pools"></a><span data-ttu-id="2aa1e-107">Lync Server 2013 プール</span><span class="sxs-lookup"><span data-stu-id="2aa1e-107">Lync Server 2013 Pools</span></span>

<span data-ttu-id="2aa1e-108">Lync Server 2013 プールでレガシクライアントが使用されている場合、ユーザーには次の動作が発生します。</span><span class="sxs-lookup"><span data-stu-id="2aa1e-108">Users will experience the following behavior when a legacy client is used in a Lync Server 2013 pool:</span></span>

  - <span data-ttu-id="2aa1e-109">2パーティーの通話では、ビデオ解像度は従来のプールと同じです。</span><span class="sxs-lookup"><span data-stu-id="2aa1e-109">For two-party calls, video resolution is the same as in the legacy pool.</span></span>

  - <span data-ttu-id="2aa1e-110">マルチパーティ会議の場合、ビデオの解像度とビデオ会議の機能は、従来のプールと同じです。</span><span class="sxs-lookup"><span data-stu-id="2aa1e-110">For multiparty conferences, video resolution and video conferencing features are the same as in the legacy pool.</span></span> <span data-ttu-id="2aa1e-111">ギャラリービューと高解像度は使用できません。</span><span class="sxs-lookup"><span data-stu-id="2aa1e-111">Gallery View and high resolution are not available.</span></span>

</div>

<div>

## <a name="legacy-pools"></a><span data-ttu-id="2aa1e-112">従来のプール</span><span class="sxs-lookup"><span data-stu-id="2aa1e-112">Legacy Pools</span></span>

<span data-ttu-id="2aa1e-113">従来のプールで Lync Server 2013 クライアントが使用されている場合、ユーザーには次の動作が発生します。</span><span class="sxs-lookup"><span data-stu-id="2aa1e-113">Users will experience the following behavior when a Lync Server 2013 client is used in a legacy pool:</span></span>

  - <span data-ttu-id="2aa1e-114">2パーティの通話の場合、Lync Server 2013 クライアントでは次のような新機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="2aa1e-114">For two-party calls, Lync Server 2013 clients can use new features as follows:</span></span>
    
      - <span data-ttu-id="2aa1e-115">両方の参加者が Lync Server 2013 クライアントを使用している場合は、"264. 264" を使うことができます。</span><span class="sxs-lookup"><span data-stu-id="2aa1e-115">H.264 is available if both participants are using Lync Server 2013 clients.</span></span>
    
      - <span data-ttu-id="2aa1e-116">従来のサーバーは、インバンドプロビジョニングでこの情報を送信しないため、Lync Server 2013 クライアントは TotalReceiveVideoBitRateKb の既定値を使います。</span><span class="sxs-lookup"><span data-stu-id="2aa1e-116">The Lync Server 2013 client uses the default value for TotalReceiveVideoBitRateKb, since the legacy server doesn’t send this information with in-band provisioning.</span></span>

  - <span data-ttu-id="2aa1e-117">マルチパーティ会議の場合、ビデオの解像度とビデオ会議の機能は、従来のプールのレガシクライアントでの経験と同じです。</span><span class="sxs-lookup"><span data-stu-id="2aa1e-117">For multiparty conferences, video resolution and video conferencing features are the same as experienced by a legacy client in the legacy pool.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="2aa1e-118">従来のサーバーが Lync Server 2013 クライアントをホストしている場合は、プールのすべてのユーザーが低解像度のビデオを受信できるだけで、高解像度のビデオを送信できるように、ビデオ会議の帯域幅を構成することができます。</span><span class="sxs-lookup"><span data-stu-id="2aa1e-118">When a legacy server hosts a Lync Server 2013 client, it's possible to configure video conferencing bandwidth so that all users on the pool receive only low-resolution video, but send high-resolution video.</span></span> <span data-ttu-id="2aa1e-119">この例としては、メディア構成の MaxVideoRateAllowed が250K に設定されていて、VideoBitRateKb が会議ポリシーで 2000 kbps に設定されている場合です。</span><span class="sxs-lookup"><span data-stu-id="2aa1e-119">An example of this is when MaxVideoRateAllowed is set to CIF-250K in the media configuration and VideoBitRateKb is set to 2000 kbps in conferencing policy.</span></span> <span data-ttu-id="2aa1e-120">この状況では、プールのユーザーに対して高解像度を実現することはできません。</span><span class="sxs-lookup"><span data-stu-id="2aa1e-120">The net effect in this situation is that high resolution is not possible for users on the pool.</span></span><BR><span data-ttu-id="2aa1e-121">MaxVideoRateAllowed は Lync Server 2013 クライアントでは使われなくなったため、Lync Server 2013 クライアントから高解像度ビデオを要求することはできません。</span><span class="sxs-lookup"><span data-stu-id="2aa1e-121">Because MaxVideoRateAllowed is no longer used for Lync Server 2013 clients, it cannot prevent Lync Server 2013 clients from requesting high-resolution video.</span></span> <span data-ttu-id="2aa1e-122">代わりに、プールのすべてのユーザーに対して、プールのすべてのユーザーに対して、VideoBitRateKb を MaxVideoRateAllowed (つまり、250 kbps に設定されているか、VGA が 600 kbps に設定されているか、HD が 1500 kbps に設定されている) と同じ値に設定します。</span><span class="sxs-lookup"><span data-stu-id="2aa1e-122">Instead, set VideoBitRateKb in conferencing policy for all users on the pool to the same value as MaxVideoRateAllowed (that is, CIF is set to 250 kbps, or VGA is set to 600 kbps, or HD is set to 1500 kbps).</span></span>



<span data-ttu-id="2aa1e-123"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2aa1e-123"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

