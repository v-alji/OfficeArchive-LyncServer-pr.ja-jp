---
title: 'Lync Server 2013: メディア バイパスと仲介サーバー'
description: 'Lync Server 2013: メディアバイパスと仲介サーバー。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Media bypass and Mediation Server
ms:assetid: 8ed35f95-05cd-4b5d-8470-442d2323df71
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398719(v=OCS.15)
ms:contentKeyID: 48184774
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ebb005d3d52fa9e5a38fdf56a65dfcbd73616d87
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425704"
---
# <a name="media-bypass-and-mediation-server-in-lync-server-2013"></a><span data-ttu-id="070bf-103">Lync Server 2013 のメディア バイパスと仲介サーバー</span><span class="sxs-lookup"><span data-stu-id="070bf-103">Media bypass and Mediation Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="070bf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="070bf-104">

<span> </span></span></span>

<span data-ttu-id="070bf-105">_**最終更新日:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="070bf-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="070bf-106">メディアのバイパスは、管理者がユーザーのエンドポイントと公衆交換電話網 (PSTN) ゲートウェイの間で直接流れるようにするための Lync Server の機能です。</span><span class="sxs-lookup"><span data-stu-id="070bf-106">Media bypass is a Lync Server capability that enables an administrator to configure call routing to flow directly between the user endpoint and the public switched telephone network (PSTN) gateway without traversing the Mediation Server.</span></span> <span data-ttu-id="070bf-107">メディアのバイパスでは、待ち時間の削減、不必要な翻訳、パケット損失の可能性、および潜在的な障害ポイントの数によって通話品質が向上します。</span><span class="sxs-lookup"><span data-stu-id="070bf-107">Media bypass improves call quality by reducing latency, unnecessary translation, possibility of packet loss, and the number of potential points of failure.</span></span> <span data-ttu-id="070bf-108">仲介サーバーのないリモートサイトが1つまたは複数の WAN リンクによって中央サイトに接続されていて、帯域幅が制限されている場合、メディアのバイパスでは、リモートサイトのクライアントから中央サイトの仲介サーバーへの直接フローを行うことなく、そのローカルゲートウェイに直接流れるメディアを有効にすることによって、帯域このメディア処理の削減は、複数のゲートウェイを制御するための仲介サーバーの機能にも補います。</span><span class="sxs-lookup"><span data-stu-id="070bf-108">Where a remote site without a Mediation Server is connected to a central site by one or more WAN links with constrained bandwidth, media bypass lowers the bandwidth requirement by enabling media from a client at a remote site to flow directly to its local gateway without first having to flow across the WAN link to a Mediation Server at the central site and back.This reduction in media processing also complements the Mediation Server’s ability to control multiple gateways.</span></span>

<span data-ttu-id="070bf-p102">メディア バイパスと通話受付管理 (CAC) を同時に使用することはできません。 通話にメディア バイパスを使用している場合、その通話に対して CAC は実行されません。 通話に関連するリンクについて、帯域幅に制約のあるリンクがないことを前提としています。</span><span class="sxs-lookup"><span data-stu-id="070bf-p102">Media bypass and call admission control (CAC) are mutually exclusive. If media bypass is employed for a call, CAC is not performed for that call. The assumption is that there are no links with constrained bandwidth involved in the call.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="070bf-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="070bf-112">See Also</span></span>


[<span data-ttu-id="070bf-113">Lync Server 2013 の通話受付管理と仲介サーバー</span><span class="sxs-lookup"><span data-stu-id="070bf-113">Call admission control and Mediation Server in Lync Server 2013</span></span>](lync-server-2013-call-admission-control-and-mediation-server.md)  


[<span data-ttu-id="070bf-114">Lync Server 2013 でのメディア バイパスの計画</span><span class="sxs-lookup"><span data-stu-id="070bf-114">Planning for media bypass in Lync Server 2013</span></span>](lync-server-2013-planning-for-media-bypass.md)  
  

<span data-ttu-id="070bf-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="070bf-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

