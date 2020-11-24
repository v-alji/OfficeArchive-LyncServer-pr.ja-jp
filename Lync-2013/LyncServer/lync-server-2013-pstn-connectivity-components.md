---
title: 'Lync Server 2013: PSTN 接続コンポーネント'
description: 'Lync Server 2013: PSTN 接続コンポーネント。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: PSTN connectivity components
ms:assetid: 6b2a3f7d-760f-4f09-8432-312c98a7e6b7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398504(v=OCS.15)
ms:contentKeyID: 48184408
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c2ae5a6a7bc5db1cd7a23c44719d7123a624317d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399116"
---
# <a name="pstn-connectivity-components-in-lync-server-2013"></a><span data-ttu-id="82c85-103">Lync Server 2013 の PSTN 接続コンポーネント</span><span class="sxs-lookup"><span data-stu-id="82c85-103">PSTN connectivity components in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="82c85-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="82c85-104">

<span> </span></span></span>

<span data-ttu-id="82c85-105">_**最終更新日:** 2012-10-04_</span><span class="sxs-lookup"><span data-stu-id="82c85-105">_**Topic Last Modified:** 2012-10-04_</span></span>

<span data-ttu-id="82c85-106">エンタープライズ レベルの VoIP ソリューションでは、サービスの品質 (QoS) を低下させずに公衆交換電話網 (PSTN) との通話の発信および着信を処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="82c85-106">An enterprise-grade VoIP solution must provide for calls to and from the public switched telephone network (PSTN) without any decline in Quality of Service (QoS).</span></span> <span data-ttu-id="82c85-107">また、通話の発信時および着信時に、基礎となるテクノロジをユーザーが意識しなくても済むようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="82c85-107">In addition, users should not be aware of the underlying technology when they place and receive calls.</span></span> <span data-ttu-id="82c85-108">ユーザーから見れば、エンタープライズボイスインフラストラクチャと PSTN 間の通話は、別の SIP セッションと同じように見えます。</span><span class="sxs-lookup"><span data-stu-id="82c85-108">From the user's perspective, a call between the Enterprise Voice infrastructure and the PSTN should seem like just another SIP session.</span></span>

<span data-ttu-id="82c85-109">PSTN 接続を行うには、(PBX (直接 SIP リンク) を使用して、または PBX を使用せずに) SIP トランクまたは PSTN ゲートウェイを展開します。</span><span class="sxs-lookup"><span data-stu-id="82c85-109">For PSTN connections, you can either deploy a SIP trunk or a PSTN gateway (with a PBX, also known as a Direct SIP link, or without a PBX).</span></span>

<div>

## <a name="sip-trunking"></a><span data-ttu-id="82c85-110">SIP トランキング</span><span class="sxs-lookup"><span data-stu-id="82c85-110">SIP Trunking</span></span>

<span data-ttu-id="82c85-111">PSTN ゲートウェイを使用する代わりに、SIP トランキングを使用してエンタープライズ Voip ソリューションを PSTN に接続することもできます。</span><span class="sxs-lookup"><span data-stu-id="82c85-111">As an alternative to using PSTN gateways, you can connect your Enterprise Voice solution to the PSTN by using SIP trunking.</span></span> <span data-ttu-id="82c85-112">SIP トランキングを使用すると、次のようなシナリオが実現します。</span><span class="sxs-lookup"><span data-stu-id="82c85-112">SIP trunking enables the following scenarios:</span></span>

  - <span data-ttu-id="82c85-113">企業のファイアウォールの内側または外側にいるエンタープライズ ユーザーが、E.164 準拠の番号で指定される市内通話や長距離通話を発信できます。この通話は、対応するサービス プロバイダーのサービスとして PSTN 上で終端されます。</span><span class="sxs-lookup"><span data-stu-id="82c85-113">An enterprise user inside or outside the corporate firewall can make a local or long-distance call specified by an E.164-compliant number that is terminated on the PSTN as a service of the corresponding service provider.</span></span>

  - <span data-ttu-id="82c85-114">PSTN サブスクライバーはだれでも、エンタープライズ ユーザーに関連付けられた Direct Inward Dialing (DID) 番号をダイヤルして、企業のファイアウォールの内側または外側にいるエンタープライズ ユーザーに連絡することができます。</span><span class="sxs-lookup"><span data-stu-id="82c85-114">Any PSTN subscriber can contact an enterprise user inside or outside the corporate firewall by dialing a Direct Inward Dialing (DID) number associated with that enterprise user.</span></span>

<span data-ttu-id="82c85-115">この展開ソリューションを使用するには、SIP トランキング サービス プロバイダーが必要です。</span><span class="sxs-lookup"><span data-stu-id="82c85-115">The use of this deployment solution requires a SIP trunking service provider.</span></span>

</div>

<div>

## <a name="pstn-gateways"></a><span data-ttu-id="82c85-116">PSTN ゲートウェイ</span><span class="sxs-lookup"><span data-stu-id="82c85-116">PSTN gateways</span></span>

<span data-ttu-id="82c85-117">PSTN ゲートウェイは、エンタープライズボイスインフラストラクチャと PSTN または PBX 間のシグナリングおよびメディアを変換するサードパーティ製のデバイスです。</span><span class="sxs-lookup"><span data-stu-id="82c85-117">PSTN gateways are third-party devices that translate signaling and media between the Enterprise Voice infrastructure and a PSTN or a PBX.</span></span> <span data-ttu-id="82c85-118">PSTN ゲートウェイは、仲介サーバーと連携して、エンタープライズボイスクライアントに PSTN または PBX 通話を提供します。</span><span class="sxs-lookup"><span data-stu-id="82c85-118">PSTN gateways work with the Mediation Server to present a PSTN or PBX call to an Enterprise Voice client.</span></span> <span data-ttu-id="82c85-119">また、仲介サーバーは、PSTN または PBX にルーティングするために、エンタープライズボイスクライアントから PSTN ゲートウェイへの通話を提供します。</span><span class="sxs-lookup"><span data-stu-id="82c85-119">The Mediation Server also presents calls from Enterprise Voice clients to the PSTN gateway for routing to the PSTN or PBX.</span></span> <span data-ttu-id="82c85-120">Microsoft と連携して Lync Server で動作するデバイスを提供しているパートナーのリストについては、Microsoft ユニファイドコミュニケーションパートナーの web サイトを参照してください [https://go.microsoft.com/fwlink/p/?linkId=202836](https://go.microsoft.com/fwlink/p/?linkid=202836) 。</span><span class="sxs-lookup"><span data-stu-id="82c85-120">For a list of partners who work with Microsoft to provide devices that work with Lync Server, see the Microsoft Unified Communications Partners website at [https://go.microsoft.com/fwlink/p/?linkId=202836](https://go.microsoft.com/fwlink/p/?linkid=202836).</span></span>

</div>

<div>

## <a name="private-branch-exchanges"></a><span data-ttu-id="82c85-121">構内交換機</span><span class="sxs-lookup"><span data-stu-id="82c85-121">Private Branch Exchanges</span></span>

<span data-ttu-id="82c85-122">プライベートブランチ exchange (PBX) を使用する既存の音声インフラストラクチャを使用している場合は、お使いの PBX で Lync Server Enterprise Voice を使用できます。</span><span class="sxs-lookup"><span data-stu-id="82c85-122">If you have an existing voice infrastructure that uses a private branch exchange (PBX), you can use your PBX with Lync Server Enterprise Voice.</span></span>

<span data-ttu-id="82c85-123">サポートされているエンタープライズ Voip 統合シナリオは、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="82c85-123">The supported Enterprise Voice-PBX integration scenarios are as follows:</span></span>

  - <span data-ttu-id="82c85-124">仲介サーバーでメディアバイパスをサポートする IP PBX。</span><span class="sxs-lookup"><span data-stu-id="82c85-124">IP-PBX that supports media bypass, with a Mediation Server.</span></span>

  - <span data-ttu-id="82c85-125">スタンドアロンの PSTN ゲートウェイが必要な IP-PBX。</span><span class="sxs-lookup"><span data-stu-id="82c85-125">IP-PBX that requires a stand-alone PSTN gateway.</span></span>

  - <span data-ttu-id="82c85-126">時分割多重 (TDM) PBX とスタンドアロンの PSTN ゲートウェイ。</span><span class="sxs-lookup"><span data-stu-id="82c85-126">Time division multiplexing (TDM) PBX, with a stand-alone PSTN gateway.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="82c85-127">メディア バイパスは、すべての PSTN ゲートウェイ、IP-PBX、および SBC と相互運用できるとは限りません。</span><span class="sxs-lookup"><span data-stu-id="82c85-127">Media bypass will not interoperate with every PSTN gateway, IP-PBX, and SBC.</span></span> <span data-ttu-id="82c85-128">マイクロソフトでは、認定パートナーの PSTN ゲートウェイと SBC でテストを行い、Cisco IP-PBX でも一定のテストを行いました。</span><span class="sxs-lookup"><span data-stu-id="82c85-128">Microsoft has tested a set of PSTN gateways and SBCs with certified partners and has done some testing with Cisco IP-PBXs.</span></span> <span data-ttu-id="82c85-129">メディアのバイパスは、統合された通信のオープンな相互運用性プログラム– Lync Server at の製品とバージョンでのみサポートされ <A href="https://go.microsoft.com/fwlink/p/?linkid=214406">https://go.microsoft.com/fwlink/p/?linkId=214406</A> ます。</span><span class="sxs-lookup"><span data-stu-id="82c85-129">Media bypass is supported only with products and versions listed on Unified Communications Open Interoperability Program – Lync Server at <A href="https://go.microsoft.com/fwlink/p/?linkid=214406">https://go.microsoft.com/fwlink/p/?linkId=214406</A>.</span></span>



</div>

<span data-ttu-id="82c85-130">エンタープライズ Voip ソリューションを提供しているパートナーの詳細については、Microsoft ユニファイドコミュニケーションパートナーの web サイトを参照してください [https://go.microsoft.com/fwlink/p/?linkId=202836](https://go.microsoft.com/fwlink/p/?linkid=202836) 。</span><span class="sxs-lookup"><span data-stu-id="82c85-130">For details about partners who offer Enterprise Voice solutions, see the Microsoft Unified Communications Partners website at [https://go.microsoft.com/fwlink/p/?linkId=202836](https://go.microsoft.com/fwlink/p/?linkid=202836).</span></span>

<span data-ttu-id="82c85-131">PSTN ゲートウェイなど、エンタープライズボイスハードウェアソリューションを提供しているパートナーの詳細については、Microsoft ユニファイドコミュニケーションパートナーの web サイトを参照してください [https://go.microsoft.com/fwlink/p/?linkId=202836](https://go.microsoft.com/fwlink/p/?linkid=202836) 。</span><span class="sxs-lookup"><span data-stu-id="82c85-131">For details about partners who offer Enterprise Voice hardware solutions, including PSTN gateways, see the Microsoft Unified Communications Partners website [https://go.microsoft.com/fwlink/p/?linkId=202836](https://go.microsoft.com/fwlink/p/?linkid=202836).</span></span>

<span data-ttu-id="82c85-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="82c85-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

