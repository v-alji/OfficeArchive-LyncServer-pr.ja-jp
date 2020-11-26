---
title: 'Lync Server 2013: メディア バイパスの構成'
description: 'Lync Server 2013: メディアのバイパスを構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure media bypass
ms:assetid: f50a7a13-c6a0-48f1-bee1-e45fa2b2f9b8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413028(v=OCS.15)
ms:contentKeyID: 48185836
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: eefe960b9811f16544b7dabdd6aa07960e273806
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433907"
---
# <a name="configure-media-bypass-in-lync-server-2013"></a><span data-ttu-id="131f3-103">Lync Server 2013 メディア バイパスの構成</span><span class="sxs-lookup"><span data-stu-id="131f3-103">Configure media bypass in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="131f3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="131f3-104">

<span> </span></span></span>

<span data-ttu-id="131f3-105">_**最終更新日:** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="131f3-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<span data-ttu-id="131f3-106">このセクションでは、少なくとも1つ以上の仲介サーバーを既に公開して構成していることを前提としています (「 [lync server 2013 のトポロジビルダーでの仲介サーバーの定義](lync-server-2013-define-a-mediation-server-in-topology-builder.md)」および「lync server [2013](lync-server-2013-publish-the-topology.md)での[フロントエンドプールまたは Standard Edition 2013 2013 サーバーの定義と構成](lync-server-2013-define-and-configure-a-front-end-pool-or-standard-edition-server.md)」で説明しています)。 [Publish the topology in Lync Server 2013](lync-server-2013-publish-the-topology.md)</span><span class="sxs-lookup"><span data-stu-id="131f3-106">This section assumes that you have already published and configured either at least one or more Mediation Servers (as described in [Define a Mediation Server in Topology Builder in Lync Server 2013](lync-server-2013-define-a-mediation-server-in-topology-builder.md) and [Publish the topology in Lync Server 2013](lync-server-2013-publish-the-topology.md), or in [Define and configure a Front End pool or Standard Edition server in Lync Server 2013](lync-server-2013-define-and-configure-a-front-end-pool-or-standard-edition-server.md) and [Publish the topology in Lync Server 2013](lync-server-2013-publish-the-topology.md), respectively, all in the Deployment documentation).</span></span>

<span data-ttu-id="131f3-107">また、このセクションでは、「 [Lync Server 2013 のトポロジビルダーでゲートウェイを定義](lync-server-2013-define-a-gateway-in-topology-builder.md)する」の説明に従って、PSTN 接続を提供するために少なくとも1つのゲートウェイピアを定義していることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="131f3-107">This section also assumes that you have defined at least one gateway peer to provide PSTN connectivity, as described in [Define a gateway in Topology Builder in Lync Server 2013](lync-server-2013-define-a-gateway-in-topology-builder.md).</span></span> <span data-ttu-id="131f3-108">接続するピアが SIP トランキング プロバイダーの SBC の場合は、プロバイダーが認定プロバイダーであることとプロバイダーがメディア バイパスをサポートしていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="131f3-108">If the peer you connect to is the SBC of a SIP trunking provider, make sure that the provider is a qualified provider and that the provider supports media bypass.</span></span> <span data-ttu-id="131f3-109">たとえば、多くの SIP トランキング プロバイダーが、その SBC に仲介サーバーからのトラフィックを受信することだけを許可します。</span><span class="sxs-lookup"><span data-stu-id="131f3-109">For example, many SIP trunking providers will only allow their SBC to receive traffic from the Mediation Server.</span></span> <span data-ttu-id="131f3-110">その場合は、当該のトランクに対してバイパスを有効にしないでください。</span><span class="sxs-lookup"><span data-stu-id="131f3-110">If so, then bypass must not be enabled for the trunk in question.</span></span> <span data-ttu-id="131f3-111">また、組織がその内部ネットワーク IP アドレスを SIP トランキング プロバイダーに公開していなければ、メディア バイパスを有効にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="131f3-111">Also, you cannot enable media bypass unless your organization reveals its internal network IP addresses to the SIP trunking provider.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="131f3-112">メディア バイパスは、すべての PSTN ゲートウェイ、IP-PBX、および SBC と相互運用できるとは限りません。</span><span class="sxs-lookup"><span data-stu-id="131f3-112">Media bypass will not interoperate with every PSTN gateway, IP-PBX, and SBC.</span></span> <span data-ttu-id="131f3-113">マイクロソフトでは、認定パートナーの PSTN ゲートウェイと SBC でテストを行い、Cisco IP-PBX でも一定のテストを行いました。</span><span class="sxs-lookup"><span data-stu-id="131f3-113">Microsoft has tested a set of PSTN gateways and SBCs with certified partners and has done some testing with Cisco IP-PBXs.</span></span> <span data-ttu-id="131f3-114">メディアのバイパスは、統合された通信のオープンな相互運用性プログラム– Lync Server at の製品とバージョンでのみサポートされ <A href="https://go.microsoft.com/fwlink/p/?linkid=214406">https://go.microsoft.com/fwlink/p/?linkId=214406</A> ます。</span><span class="sxs-lookup"><span data-stu-id="131f3-114">Media bypass is supported only with products and versions listed on Unified Communications Open Interoperability Program – Lync Server at <A href="https://go.microsoft.com/fwlink/p/?linkid=214406">https://go.microsoft.com/fwlink/p/?linkId=214406</A>.</span></span>



</div>

<span data-ttu-id="131f3-115">このセクションでは、メディアのバイパスを有効にして、仲介サーバーで必要な処理を軽減する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="131f3-115">This section describes how to enable media bypass to reduce the processing required of the Mediation Server.</span></span> <span data-ttu-id="131f3-116">メディアのバイパスを有効にする前に、計画ドキュメントの「 [Lync Server 2013 でのメディアのバイパスの計画](lync-server-2013-planning-for-media-bypass.md) 」で説明されているように、使用している環境がメディアのバイパスをサポートするために必要な条件を満たしていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="131f3-116">Before you enable media bypass, make sure that your environment meets the conditions required to support media bypass, as described in [Planning for media bypass in Lync Server 2013](lync-server-2013-planning-for-media-bypass.md) in the Planning documentation.</span></span> <span data-ttu-id="131f3-117">また、「 [Lync server 2013 でメディアバイパスの計画](lync-server-2013-planning-for-media-bypass.md) 」に記載されている情報を使用して、仲介サーバーを無視するか、またはサイトと地域の情報を使用して、仲介サーバーをバイパスするかどうかを決定してください。</span><span class="sxs-lookup"><span data-stu-id="131f3-117">Also make sure that you used the information in [Planning for media bypass in Lync Server 2013](lync-server-2013-planning-for-media-bypass.md) to decide whether to enable media bypass global settings to always bypass the Mediation Server or to use site and region information when determining whether to bypass the Mediation Server.</span></span>

<span data-ttu-id="131f3-p104">もう 1 つの高度なエンタープライズ VoIP 機能に当たる、オプションの通話受付管理 (CAC) の構成が済んでいる場合は、通話受付管理が実行する帯域幅の予約がメディア バイパスを採用する通話に適用されないようにしてください。メディア バイパスが採用されているかどうかの検証は最初に行われます。採用されている場合は、その通話に対しては通話受付管理は使用されません。通話受付管理に対するチェックは、メディア バイパスのチェックが不合格の場合にのみ行われます。このため、PSTN にルーティングされる特定の通話に対して 2 つの機能がともに適用されることはありません。メディア バイパスは、通話のメディア エンドポイント間に帯域幅の制約がないことを前提にしているため、2 つの機能が両立しないという論理的結論にたどり着きます。メディア バイパスは、帯域幅制限のあるリンク上では実行できません。このことから、PSTN の通話には次のいずれかが適用されます。a) 仲介サーバーをメディア バイパスし、通話受付管理は通話に対して帯域幅を予約しない。または b) 通話受付管理が通話に帯域幅の予約を適用し、メディアはその通話に関わる仲介サーバーで処理される。</span><span class="sxs-lookup"><span data-stu-id="131f3-p104">If you have already optionally configured call admission control (CAC), another advanced Enterprise Voice feature, note that the bandwidth reservation performed by call admission control does not apply to any calls for which media bypass is employed. The verification of whether to employ media bypass is performed first, and if media bypass is employed, call admission control is not used for the call; only if the media bypass check fails is the check performed for call admission control. The two features are thus mutually exclusive for any particular call that is routed to the PSTN. This is the logic because media bypass assumes that bandwidth constraints do not exist between the media endpoints on a call; media bypass cannot be performed on links with restricted bandwidth. As a result, one of the following will apply to a PSTN call: a) media bypasses the Mediation Server, and call admission control does not reserve bandwidth for the call; or b) call admission control applies bandwidth reservation to the call, and media is processed by the Mediation Server involved in the call.</span></span>

<div>

## <a name="next-steps-enable-media-bypass-on-the-trunk-connection"></a><span data-ttu-id="131f3-123">次の手順: トランク接続でメディアバイパスを有効にする</span><span class="sxs-lookup"><span data-stu-id="131f3-123">Next Steps: Enable Media Bypass on the Trunk Connection</span></span>

<span data-ttu-id="131f3-124">PSTN 接続の初期設定 (ダイヤルプラン、音声ポリシー、PSTN 使用状況レコード、発信通話ルート、および翻訳ルール) を構成したら、「 [Lync Server 2013 でメディアバイパス](lync-server-2013-configure-a-trunk-with-media-bypass.md)を有効にする」の手順に従って、メディアのバイパスを有効にするプロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="131f3-124">After configuring initial settings for PSTN connectivity (dial plans, voice policies, PSTN usage records, outbound call routes, and translation rules), begin the process of enabling media bypass by using the steps in [Configure a trunk with media bypass in Lync Server 2013](lync-server-2013-configure-a-trunk-with-media-bypass.md).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="131f3-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="131f3-125">See Also</span></span>


[<span data-ttu-id="131f3-126">Configure a trunk with media bypass in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="131f3-126">Configure a trunk with media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-a-trunk-with-media-bypass.md)  
[<span data-ttu-id="131f3-127">Configure media bypass in Lync Server 2013 to always bypass the Mediation Server</span><span class="sxs-lookup"><span data-stu-id="131f3-127">Configure media bypass in Lync Server 2013 to always bypass the Mediation Server</span></span>](lync-server-2013-configure-media-bypass-to-always-bypass-the-mediation-server.md)  
[<span data-ttu-id="131f3-128">Configure media bypass global settings in Lync Server 2013 to use site and region information</span><span class="sxs-lookup"><span data-stu-id="131f3-128">Configure media bypass global settings in Lync Server 2013 to use site and region information</span></span>](lync-server-2013-configure-media-bypass-global-settings-to-use-site-and-region-information.md)  


[<span data-ttu-id="131f3-129">Lync Server 2013 のグローバルメディアバイパスオプション</span><span class="sxs-lookup"><span data-stu-id="131f3-129">Global media bypass options in Lync Server 2013</span></span>](lync-server-2013-global-media-bypass-options.md)  


[<span data-ttu-id="131f3-130">Lync Server 2013 でのメディア バイパスの計画</span><span class="sxs-lookup"><span data-stu-id="131f3-130">Planning for media bypass in Lync Server 2013</span></span>](lync-server-2013-planning-for-media-bypass.md)  
  

<span data-ttu-id="131f3-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="131f3-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

