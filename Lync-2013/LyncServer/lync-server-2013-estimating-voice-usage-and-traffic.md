---
title: 'Lync Server 2013: 音声の利用状況とトラフィックの予測'
description: 'Lync Server 2013: 音声の使用状況とトラフィックを見積もります。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Estimating voice usage and traffic
ms:assetid: 621b08fb-f894-4d91-ac38-e443401b098b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398439(v=OCS.15)
ms:contentKeyID: 48184332
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1fc288e6da65e8e6f221a05c6c82f0588414c8af
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428453"
---
# <a name="estimating-voice-usage-and-traffic-for-lync-server-2013"></a><span data-ttu-id="eb1ea-103">Lync Server 2013 の音声の利用状況とトラフィックの予測</span><span class="sxs-lookup"><span data-stu-id="eb1ea-103">Estimating voice usage and traffic for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="eb1ea-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="eb1ea-104">

<span> </span></span></span>

<span data-ttu-id="eb1ea-105">_**最終更新日:** 2012-08-07_</span><span class="sxs-lookup"><span data-stu-id="eb1ea-105">_**Topic Last Modified:** 2012-08-07_</span></span>

<span data-ttu-id="eb1ea-106">Microsoft Lync Server 2013 の計画ツールでは、次のメトリックを使用して、各サイトのユーザートラフィックを見積もり、そのトラフィックをサポートするために必要なポート数を見積もります。</span><span class="sxs-lookup"><span data-stu-id="eb1ea-106">The Microsoft Lync Server 2013, Planning Tool uses the following metric to estimate user traffic at each site and the number of ports that are required to support that traffic.</span></span>

  - <span></span>  
    <span data-ttu-id="eb1ea-107">**軽度のトラフィック** (1 人あたり 1 時間に 1 PSTN 通話) の場合、1 ポートに対して 15 ユーザーを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="eb1ea-107">For **Light traffic** (one PSTN call per user per hour), figure 15 users per port.</span></span>

  - <span></span>  
    <span data-ttu-id="eb1ea-108">**中度のトラフィック** (1 人あたり 1 時間に 2 PSTN 通話) の場合、1 ポートに対して 10 ユーザーを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="eb1ea-108">For **Medium traffic** (2 PSTN calls per user per hour), figure 10 users per port.</span></span>

  - <span></span>  
    <span data-ttu-id="eb1ea-109">**重度のトラフィック** (1 人あたり 1 時間に 3 以上の PSTN 通話) の場合、1 ポートに対して 5 ユーザーを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="eb1ea-109">For **Heavy traffic** (3 or more PSTN per user calls per hour), figure 5 users per port.</span></span>

<span data-ttu-id="eb1ea-110">ポートの数によって、必要な仲介サーバーとゲートウェイの数が決まります。</span><span class="sxs-lookup"><span data-stu-id="eb1ea-110">The number of ports in turn determines the number of Mediation Servers and gateways that will be required.</span></span> <span data-ttu-id="eb1ea-111">ほとんどの組織が、2つのポートから最大960ポートへの展開を検討している公衆交換電話網 (PSTN) ゲートウェイ。</span><span class="sxs-lookup"><span data-stu-id="eb1ea-111">The public switched telephone network (PSTN) gateways that most organizations consider deploying range in size from 2 ports to as many as 960 ports.</span></span> <span data-ttu-id="eb1ea-112">(大規模なゲートウェイもありますが、主にテレフォニーサービスプロバイダーによって使用されます)。</span><span class="sxs-lookup"><span data-stu-id="eb1ea-112">(There are even larger gateways, but these are used mainly by telephony service providers.)</span></span>

<span data-ttu-id="eb1ea-p102">たとえば、10,000 名のユーザーを擁する中度のトラフィックの組織の場合、1000 ポートが必要となります。必要となるゲートウェイ数は、ゲートウェイの総合した処理能力によって決まる、必要とされるポート数の合計と同じになります。</span><span class="sxs-lookup"><span data-stu-id="eb1ea-p102">For example, an organization with 10,000 users and medium traffic would require 1000 ports. The number of gateways required would equal the total number of ports required as determined by the total capacity of the gateways.</span></span>

<span data-ttu-id="eb1ea-115"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="eb1ea-115"></div>

<span> </span>

</div>

</div>

</span></span></div>

