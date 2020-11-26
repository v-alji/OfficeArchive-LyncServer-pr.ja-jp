---
title: 'Lync Server 2013: 新しいトランク機能'
description: 'Lync Server 2013: 新しいトランク機能。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New trunk feature
ms:assetid: 9b398bc8-2760-4218-b1a4-89b9694b1171
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688152(v=OCS.15)
ms:contentKeyID: 49733755
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d8f923ceada899608cc350bd1343345c12d0996b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445338"
---
# <a name="new-trunk-feature-in-lync-server-2013"></a><span data-ttu-id="b6e7f-103">Lync Server 2013 の新しいトランク機能</span><span class="sxs-lookup"><span data-stu-id="b6e7f-103">New trunk feature in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b6e7f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b6e7f-104">

<span> </span></span></span>

<span data-ttu-id="b6e7f-105">_**最終更新日:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="b6e7f-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="b6e7f-106">Microsoft Lync Server 2013 では、仲介サーバーとゲートウェイ間の複数の trunks を定義できます。</span><span class="sxs-lookup"><span data-stu-id="b6e7f-106">In Microsoft Lync Server 2013, multiple trunks between a Mediation Server and a gateway can be defined.</span></span> <span data-ttu-id="b6e7f-107">Microsoft Lync Server 2010 は、仲介サーバーと PSTN ゲートウェイ間の1つのトランクでのみ許可されています。</span><span class="sxs-lookup"><span data-stu-id="b6e7f-107">Microsoft Lync Server 2010 only allowed for a single trunk between a Mediation Server and a PSTN gateway.</span></span> <span data-ttu-id="b6e7f-108">この機能を使うと、追加の trunks を柔軟に定義できます。</span><span class="sxs-lookup"><span data-stu-id="b6e7f-108">This feature provides the flexibility to define additional trunks.</span></span> <span data-ttu-id="b6e7f-109">トランクは、仲介サーバーの FQDN とリッスンポート、および PSTN ゲートウェイの FQDN とリッスンポートの間の論理的な関連付けです。</span><span class="sxs-lookup"><span data-stu-id="b6e7f-109">A trunk is a logical association between a Mediation Server FQDN and listening port and a PSTN gateway FQDN and listening port.</span></span> <span data-ttu-id="b6e7f-110">この新しい機能を使用すると、回復性 (複数の仲介サーバーを使用して、同じ PSTN ゲートウェイへの通話をルーティングすることができます) で、複数の trunks に関連付けられた複数のポリシーを、複数の異なるサイトの仲介サーバーと同じキャリア FQDN によって参照される sip trunks に設定することができます。</span><span class="sxs-lookup"><span data-stu-id="b6e7f-110">This new capability allows for easy trunk definition for resiliency (where multiple Mediation Servers can be used to route calls to the same PSTN Gateway), for PBX interoperability, where multiple trunks with different associated policies can be used between and IP-PBX and a Mediation Server, and for SIP trunk configurations where Mediation Servers at different sites have SIP trunks to the carrier referenced by the same carrier FQDN.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="b6e7f-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="b6e7f-111">See Also</span></span>


[<span data-ttu-id="b6e7f-112">Lync Server 2013 の新しいエンタープライズ VoIP 機能</span><span class="sxs-lookup"><span data-stu-id="b6e7f-112">New Enterprise Voice features in Lync Server 2013</span></span>](lync-server-2013-new-enterprise-voice-features.md)  
  

<span data-ttu-id="b6e7f-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b6e7f-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

