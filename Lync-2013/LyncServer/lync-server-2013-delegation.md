---
title: 'Lync Server 2013: 委任'
description: 'Lync Server 2013: 委任。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delegation
ms:assetid: 89e76e5c-3cfb-4504-8d0d-7509c8ba9815
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994045(v=OCS.15)
ms:contentKeyID: 51803956
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6dc25d0ea3dfd64ee1b71677e6bac55c1cb1ca32
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430743"
---
# <a name="delegation-in-lync-server-2013"></a><span data-ttu-id="cd65c-103">Lync Server 2013 の委任</span><span class="sxs-lookup"><span data-stu-id="cd65c-103">Delegation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cd65c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cd65c-104">

<span> </span></span></span>

<span data-ttu-id="cd65c-105">_**最終更新日:** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="cd65c-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="cd65c-106">Lync の委任機能は、次のような方法で Location-Based ルーティングの影響を受けます。</span><span class="sxs-lookup"><span data-stu-id="cd65c-106">The delegation capabilities in Lync are affected by Location-Based Routing in the following manner:</span></span>

  - <span data-ttu-id="cd65c-107">代理 Location-Based 人が管理者の代わりに通話を発信する場合、代理人の音声ポリシーを使って通話を承認し、代理人のサイトボイスルーティングポリシーを使って通話をルーティングします。</span><span class="sxs-lookup"><span data-stu-id="cd65c-107">When a delegate enabled for Location-Based Routing places a call on behalf of a manager, the delegate’s voice policy is used to authorize the call and the delegate’s site voice routing policy will be used to route the call</span></span>

  - <span data-ttu-id="cd65c-108">マネージャーへの着信 PSTN 通話については、通話の転送または同時呼び出しに適用されるのと同じルールが適用されます (着信の転送と通話の転送および同時呼び出しのトピックを参照してください)。</span><span class="sxs-lookup"><span data-stu-id="cd65c-108">For incoming PSTN calls to a manager, the same rules applicable for call forwarding or simultaneously ringing will apply as described in the Call transfers and forwarding and Simultaneous ringing topics.</span></span>

  - <span data-ttu-id="cd65c-109">代理人がマネージャーへの着信通話に対して PSTN エンドポイントを同時呼び出しターゲットとして設定すると、代理人の PSTN エンドポイントへの通話のルーティングに、受信トランクに関連付けられたサイトの音声ルーティング ポリシーが使用されます。</span><span class="sxs-lookup"><span data-stu-id="cd65c-109">When a delegate sets a PSTN endpoint as a simultaneous ring target, for an incoming call to the manager, the voice routing policy of the site that is associated to the incoming trunk will be used to route the call to the delegate’s PSTN endpoint.</span></span>

  - <span data-ttu-id="cd65c-110">委任に関して、通常はマネージャーとその関連付けられた代理人を同じネットワーク サイトに配置することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="cd65c-110">For delegation, it’s recommended that the manager and his associated delegates to be usually located in the same network site.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="cd65c-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="cd65c-111">See Also</span></span>


[<span data-ttu-id="cd65c-112">Lync Server 2013 の場所に基づくルーティングのシナリオ</span><span class="sxs-lookup"><span data-stu-id="cd65c-112">Scenarios for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-location-based-routing.md)  
  

<span data-ttu-id="cd65c-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cd65c-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

