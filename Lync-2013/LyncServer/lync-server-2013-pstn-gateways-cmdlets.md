---
title: 'Lync Server 2013: PSTN ゲートウェイのコマンドレット'
description: 'Lync Server 2013: PSTN ゲートウェイのコマンドレット。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: PSTN gateways cmdlets
ms:assetid: 6a8aa6ea-f349-4b95-b3ce-c28d2ae0a84b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg416491(v=OCS.15)
ms:contentKeyID: 48184397
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8f5bf26682e3246b1eec732190ee8d2bd5933b68
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399092"
---
# <a name="pstn-gateways-cmdlets-in-lync-server-2013"></a><span data-ttu-id="a4c55-103">Lync Server 2013 の PSTN ゲートウェイのコマンドレット</span><span class="sxs-lookup"><span data-stu-id="a4c55-103">PSTN gateways cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a4c55-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a4c55-104">

<span> </span></span></span>

<span data-ttu-id="a4c55-105">_**最終更新日:** 2012-03-21_</span><span class="sxs-lookup"><span data-stu-id="a4c55-105">_**Topic Last Modified:** 2012-03-21_</span></span>

<span data-ttu-id="a4c55-106">PSTN ゲートウェイを使用すると、エンタープライズボイスユーザーは、PSTN ネットワーク上のユーザー (つまり、公衆交換電話網) を使って電話をかけたり、通話を受けたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="a4c55-106">PSTN gateways enable your Enterprise Voice users to make phone calls to, and receive phone calls from, people on the PSTN network (that is, the public switched telephone network).</span></span> <span data-ttu-id="a4c55-107">これらのゲートウェイは、仲介サーバーと PSTN ネットワーク間のブリッジとして機能します。</span><span class="sxs-lookup"><span data-stu-id="a4c55-107">These gateways act as a bridge between the Mediation Server and the PSTN network.</span></span>

<div>

## <a name="pstn-gateways-cmdlets"></a><span data-ttu-id="a4c55-108">PSTN ゲートウェイのコマンドレット</span><span class="sxs-lookup"><span data-stu-id="a4c55-108">PSTN Gateways Cmdlets</span></span>

<span data-ttu-id="a4c55-109">[テスト用の CsPstnOutboundCall](https://technet.microsoft.com/library/Gg398207(v=OCS.15))と[Test-CsPstnPeerToPeerCall](https://technet.microsoft.com/library/Gg398662(v=OCS.15))コマンドレットを使用して、ユーザーが PSTN ネットワーク経由で通話を発信できることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="a4c55-109">The [Test-CsPstnOutboundCall](https://technet.microsoft.com/library/Gg398207(v=OCS.15)) and [Test-CsPstnPeerToPeerCall](https://technet.microsoft.com/library/Gg398662(v=OCS.15)) cmdlets enable you to verify that users are able to make call over the PSTN network.</span></span>

<span data-ttu-id="a4c55-110">**PSTN ゲートウェイ**</span><span class="sxs-lookup"><span data-stu-id="a4c55-110">**PSTN Gateways**</span></span>

  - <span></span>  
    <span data-ttu-id="a4c55-111">[Set-CsPstnGateway](https://technet.microsoft.com/library/Gg398408(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="a4c55-111">[Set-CsPstnGateway](https://technet.microsoft.com/library/Gg398408(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="a4c55-112">[Test-CsPstnOutboundCall](https://technet.microsoft.com/library/Gg398207(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="a4c55-112">[Test-CsPstnOutboundCall](https://technet.microsoft.com/library/Gg398207(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="a4c55-113">[Test-CsPstnPeerToPeerCall](https://technet.microsoft.com/library/Gg398662(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="a4c55-113">[Test-CsPstnPeerToPeerCall](https://technet.microsoft.com/library/Gg398662(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="a4c55-114">[Set-CsMediationServer](https://technet.microsoft.com/library/Gg398213(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="a4c55-114">[Set-CsMediationServer](https://technet.microsoft.com/library/Gg398213(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="a4c55-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="a4c55-115">See Also</span></span>


[<span data-ttu-id="a4c55-116">Lync Server PowerShell ブログ</span><span class="sxs-lookup"><span data-stu-id="a4c55-116">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="a4c55-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a4c55-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

