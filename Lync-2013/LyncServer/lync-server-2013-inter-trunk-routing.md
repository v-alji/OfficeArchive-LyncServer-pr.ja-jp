---
title: 'Lync Server 2013: トランク間ルーティング'
description: 'Lync Server 2013: トランク間ルーティング。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Inter-trunk routing
ms:assetid: f687a548-1f2e-48ed-9745-a13dc1f3698f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721940(v=OCS.15)
ms:contentKeyID: 49733877
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7e023956f28183423c04e94948acdec0df2c1284
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426866"
---
# <a name="inter-trunk-routing-in-lync-server-2013"></a><span data-ttu-id="2dd13-103">Lync Server 2013 のクロストランクルーティング</span><span class="sxs-lookup"><span data-stu-id="2dd13-103">Inter-trunk routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2dd13-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2dd13-104">

<span> </span></span></span>

<span data-ttu-id="2dd13-105">_**最終更新日:** 2012-10-08_</span><span class="sxs-lookup"><span data-stu-id="2dd13-105">_**Topic Last Modified:** 2012-10-08_</span></span>

<span data-ttu-id="2dd13-106">Lync Server 2013 は、intertrunk ルーティングのサポートによって基本的なセッション管理を提供します。</span><span class="sxs-lookup"><span data-stu-id="2dd13-106">Lync Server 2013 provides basic session management through the support of intertrunk routing.</span></span> <span data-ttu-id="2dd13-107">この新しい機能により、Lync Server は、下流のテレフォニーシステムへの通話コントロール機能を提供できるようになります。</span><span class="sxs-lookup"><span data-stu-id="2dd13-107">This new capability enables Lync Server to provide call control functionalities to downstream telephony systems.</span></span> <span data-ttu-id="2dd13-108">トランク間ルーティングは IP-PBX と公衆交換電話網 (PSTN) ゲートウェイを相互に接続でき、それによって、構内交換機 (PBX) 電話機からの通話を PSTN にルーティングしたり、着信した PSTN の通話を PBX 電話機にルーティングしたりできます。</span><span class="sxs-lookup"><span data-stu-id="2dd13-108">Intertrunk routing can interconnect an IP-PBX to a public switched telephone network (PSTN) gateway so that calls from a private branch exchange (PBX) phone can be routed to the PSTN, and incoming PSTN calls can be routed to a PBX phone.</span></span> <span data-ttu-id="2dd13-109">同様に、Lync Server は2つ以上の IP PBX システムを相互接続して、複数の IP PBX システムから PBX 電話間で通話を発信および受信することができます。</span><span class="sxs-lookup"><span data-stu-id="2dd13-109">Similarly, Lync Server can interconnect two or more IP-PBX systems so that calls can be placed and received between PBX phones from the different IP-PBX systems.</span></span>

<span data-ttu-id="2dd13-110">次の図は、PSTN ゲートウェイと ip-pbx の間の相互攻撃を実現する Lync Server 2013 を示しています。</span><span class="sxs-lookup"><span data-stu-id="2dd13-110">The following figure illustrates Lync Server 2013 providing interconnectivity between a PSTN gateway and an IP-PBX.</span></span>

<span data-ttu-id="2dd13-111">![Lync Server、PSTN ゲートウェイ/IP-PBX の接続図](images/JJ721940.cc3858ca-2ee3-4d51-8a51-db078366b50b(OCS.15).jpg "Lync Server、PSTN ゲートウェイ/IP-PBX の接続図")</span><span class="sxs-lookup"><span data-stu-id="2dd13-111">![Lync Server connecting PSTN gateway/IP-PBX diagram](images/JJ721940.cc3858ca-2ee3-4d51-8a51-db078366b50b(OCS.15).jpg "Lync Server connecting PSTN gateway/IP-PBX diagram")</span></span>

<span data-ttu-id="2dd13-112">次の図は、2つの IP PBX システムを接続する Lync Server 2013 を示しています。</span><span class="sxs-lookup"><span data-stu-id="2dd13-112">The next figure illustrates Lync Server 2013 connecting two IP-PBX systems.</span></span>

<span data-ttu-id="2dd13-113">![Lync Server、IP-PAX システムの相互接続図](images/JJ721940.6ba18ec9-df70-498a-9cf7-7fc41e5ec432(OCS.15).jpg "Lync Server、IP-PAX システムの相互接続図")</span><span class="sxs-lookup"><span data-stu-id="2dd13-113">![Lync Server interconnecting IP-PAX systems diagram](images/JJ721940.6ba18ec9-df70-498a-9cf7-7fc41e5ec432(OCS.15).jpg "Lync Server interconnecting IP-PAX systems diagram")</span></span>

<span data-ttu-id="2dd13-114"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2dd13-114"></div>

<span> </span>

</div>

</div>

</span></span></div>

