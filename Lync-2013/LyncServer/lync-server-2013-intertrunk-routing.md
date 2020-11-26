---
title: 'Lync Server 2013: トランク間ルーティング'
description: 'Lync Server 2013: Intertrunk ルーティング。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Intertrunk routing
ms:assetid: d3a33b4a-8bf4-4a8c-a371-8ef79e740780
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205272(v=OCS.15)
ms:contentKeyID: 48185442
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 30c838ee94a2df0807195c172d7e2a3a393523af
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426777"
---
# <a name="intertrunk-routing-in-lync-server-2013"></a><span data-ttu-id="161b8-103">Lync Server 2013 のトランク間ルーティング</span><span class="sxs-lookup"><span data-stu-id="161b8-103">Intertrunk routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="161b8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="161b8-104">

<span> </span></span></span>

<span data-ttu-id="161b8-105">_**最終更新日:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="161b8-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="161b8-106">Lync Server 2013 は、IP PBX を公衆交換電話網 (PSTN) ゲートウェイに接続して、PBX 携帯電話からの通話を PSTN にルーティングし、着信 PSTN 通話を構内交換機 (PBX) 電話にルーティングすることができます。</span><span class="sxs-lookup"><span data-stu-id="161b8-106">Lync Server 2013 can interconnect an IP-PBX to a public switched telephone network (PSTN) gateway so that calls from a PBX phone can be routed to the PSTN, and incoming PSTN calls can be routed to a private branch exchange (PBX) phone.</span></span> <span data-ttu-id="161b8-107">同様に、Lync Server 2013 は2つ以上の IP PBX システムを相互接続して、さまざまな IP PBX システムからの PBX 電話間で通話を発信および受信できるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="161b8-107">Similarly, Lync Server 2013 can interconnect two or more IP-PBX systems so that calls can be placed and received between PBX phones from the different IP-PBX systems.</span></span>

<span data-ttu-id="161b8-108">このクロストランクルーティング機能を構成するには、Lync Server Management Shell コマンドレット **set-cstrunkconfiguration** を使用して、新しいパラメーター PstnUsages を設定します。</span><span class="sxs-lookup"><span data-stu-id="161b8-108">This intertrunk routing feature can be configured by using the Lync Server Management Shell cmdlet, **Set-CsTrunkConfiguration**, with the new parameter, PstnUsages.</span></span> <span data-ttu-id="161b8-109">このパラメーターは、使用する PSTN 利用状況レコードのセットを指定します。</span><span class="sxs-lookup"><span data-stu-id="161b8-109">This parameter specifies the set of PSTN usage records to use.</span></span> <span data-ttu-id="161b8-110">トランクはこの PSTN 使用法を使ってルートを特定し、着信通話をすべてルーティングします。</span><span class="sxs-lookup"><span data-stu-id="161b8-110">A trunk uses this PSTN usage to determine a route and to route all incoming calls accordingly.</span></span>

    Set-CsTrunkConfiguration -Identity <TrunkId> -PstnUsages @{add="<UsageString>"}

<span data-ttu-id="161b8-111">次の図は、PSTN ゲートウェイと ip-pbx の間の相互に通信できる Lync Server 2013 を示しています。</span><span class="sxs-lookup"><span data-stu-id="161b8-111">The following diagram illustrates Lync Server 2013 providing interconnectivity between a PSTN gateway and an IP-PBX.</span></span>

<span data-ttu-id="161b8-112">**ゲートウェイと IP PBX 間の intertrunk ルーティング**</span><span class="sxs-lookup"><span data-stu-id="161b8-112">**Intertrunk routing between gateway and IP PBX**</span></span>

<span data-ttu-id="161b8-113">![Lync Server、PSTN ゲートウェイ/IP-PBX の接続図](images/JJ721940.cc3858ca-2ee3-4d51-8a51-db078366b50b(OCS.15).jpg "Lync Server、PSTN ゲートウェイ/IP-PBX の接続図")</span><span class="sxs-lookup"><span data-stu-id="161b8-113">![Lync Server connecting PSTN gateway/IP-PBX diagram](images/JJ721940.cc3858ca-2ee3-4d51-8a51-db078366b50b(OCS.15).jpg "Lync Server connecting PSTN gateway/IP-PBX diagram")</span></span>

<span data-ttu-id="161b8-114">次の図は、2つの IP PBX システムでの Lync Server 2013 相互の相互に対応しています。</span><span class="sxs-lookup"><span data-stu-id="161b8-114">The following diagram illustrates Lync Server 2013 interconnecting two IP-PBX systems.</span></span>

<span data-ttu-id="161b8-115">**2つの IP Pbx 間での intertrunk ルーティング**</span><span class="sxs-lookup"><span data-stu-id="161b8-115">**Intertrunk routing between two IP PBXs**</span></span>

<span data-ttu-id="161b8-116">![Lync Server、IP-PAX システムの相互接続図](images/JJ721940.6ba18ec9-df70-498a-9cf7-7fc41e5ec432(OCS.15).jpg "Lync Server、IP-PAX システムの相互接続図")</span><span class="sxs-lookup"><span data-stu-id="161b8-116">![Lync Server interconnecting IP-PAX systems diagram](images/JJ721940.6ba18ec9-df70-498a-9cf7-7fc41e5ec432(OCS.15).jpg "Lync Server interconnecting IP-PAX systems diagram")</span></span>

<span data-ttu-id="161b8-117"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="161b8-117"></div>

<span> </span>

</div>

</div>

</span></span></div>

