---
title: 小規模組織向けの Lync Server 2013 リファレンストポロジ
description: 小規模組織向けの Lync Server 2013 リファレンストポロジ。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Reference topology for small organizations
ms:assetid: 0453aeee-c41f-44e6-a6e0-aaace526ca08
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398095(v=OCS.15)
ms:contentKeyID: 48183272
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7f2f23a963543c303e54f8f2773d499e8317a63a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436610"
---
# <a name="reference-topology-for-lync-server-2013-in-small-organizations"></a><span data-ttu-id="c014e-103">小規模組織の Lync Server 2013 のリファレンストポロジ</span><span class="sxs-lookup"><span data-stu-id="c014e-103">Reference topology for Lync Server 2013 in small organizations</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c014e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c014e-104">

<span> </span></span></span>

<span data-ttu-id="c014e-105">_**最終更新日:** 2013-10-07_</span><span class="sxs-lookup"><span data-stu-id="c014e-105">_**Topic Last Modified:** 2013-10-07_</span></span>

<span data-ttu-id="c014e-106">小規模組織向けのリファレンストポロジは、Lync Server を実行している3台のサーバーのみを展開することで、堅牢で可用性の高いソリューションを展開する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="c014e-106">The reference topology for small organizations shows how you can deploy a robust, highly available solution by deploying only three servers running Lync Server.</span></span>

<span data-ttu-id="c014e-107">**小規模な組織向けの関連トポロジ**</span><span class="sxs-lookup"><span data-stu-id="c014e-107">**Reference topology for small organizations**</span></span>

<span data-ttu-id="c014e-108">![3 台のサーバーを展開している関連トポロジの図](images/Gg398095.25196d0d-dd07-451b-83ba-94c0ddf59030(OCS.15).jpg "3 台のサーバーを展開している関連トポロジの図")</span><span class="sxs-lookup"><span data-stu-id="c014e-108">![Reference topology deploying three servers diagram](images/Gg398095.25196d0d-dd07-451b-83ba-94c0ddf59030(OCS.15).jpg "Reference topology deploying three servers diagram")</span></span>

  - <span data-ttu-id="c014e-109">**展開された Standard Edition サーバーのペア**    この組織には、中央サイトの4000ユーザーがいます。</span><span class="sxs-lookup"><span data-stu-id="c014e-109">**Pair of Standard Edition Servers Deployed**    This organization has 4,000 users at their central site.</span></span> <span data-ttu-id="c014e-110">組織では、2つの標準エディションのサーバーを展開し、それらを組み合わせて、高可用性と障害回復を実現しています。</span><span class="sxs-lookup"><span data-stu-id="c014e-110">The organization has deployed two Standard Edition servers and paired them together to enable high availability and disaster recovery.</span></span> <span data-ttu-id="c014e-111">Each server homes 2,000 users, but information about all users is synchronized between the two servers.</span><span class="sxs-lookup"><span data-stu-id="c014e-111">Each server homes 2,000 users, but information about all users is synchronized between the two servers.</span></span> <span data-ttu-id="c014e-112">If one goes down, an administrator can fail over those users to be served by the other server, with a minimum of disruption to users.</span><span class="sxs-lookup"><span data-stu-id="c014e-112">If one goes down, an administrator can fail over those users to be served by the other server, with a minimum of disruption to users.</span></span> <span data-ttu-id="c014e-113">Lync Server 2013 の高可用性機能と障害回復機能の詳細については、「 [Lync server 2013 での高可用性と障害回復の計画](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c014e-113">For more information about high availability and disaster recovery features in Lync Server 2013, see [Planning for high availability and disaster recovery in Lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md).</span></span>

  - <span data-ttu-id="c014e-114">**エッジ サーバー展開の推奨。**</span><span class="sxs-lookup"><span data-stu-id="c014e-114">**Edge Server deployment is recommended.**</span></span>   <span data-ttu-id="c014e-115">エッジ サーバーの展開は内部 IM、プレゼンス、会議機能に必須ではありませんが、小規模な展開の場合であってもエッジ サーバーを展開することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="c014e-115">Although deploying an Edge Server is not required for internal IM, presence and conferencing, we recommend it even for small deployments.</span></span> <span data-ttu-id="c014e-116">組織のファイアウォールの外側にいるユーザーにサービスを提供するために、エッジサーバーを展開することで、Lync Server への投資を最大限に活用できます。</span><span class="sxs-lookup"><span data-stu-id="c014e-116">You can maximize your Lync Server investment by deploying an Edge Server to provide service to users currently outside your organization’s firewalls.</span></span> <span data-ttu-id="c014e-117">その利点は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="c014e-117">The benefits include the following:</span></span>
    
      - <span data-ttu-id="c014e-118">組織の独自のユーザーは、自宅で作業しているか、外出先にいる場合でも、Lync Server 機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="c014e-118">Your organization’s own users can use Lync Server functionality, if they are working from home or are out on the road.</span></span>
    
      - <span data-ttu-id="c014e-119">ユーザーは、外部ユーザーを会議に参加するように招待できます。</span><span class="sxs-lookup"><span data-stu-id="c014e-119">Your users can invite outside users to participate in meetings.</span></span>
    
      - <span data-ttu-id="c014e-120">Lync Server も使用しているパートナー、ベンダー、または顧客の組織がある場合は、その組織と *フェデレーション関係* を形成することができます。</span><span class="sxs-lookup"><span data-stu-id="c014e-120">If you have a partner, vendor or customer organization that also uses Lync Server, you can form a *federated relationship* with that organization.</span></span> <span data-ttu-id="c014e-121">Lync Server の展開では、フェデレーションされた組織のユーザーが認識され、より効果的なコラボレーションが実現されます。</span><span class="sxs-lookup"><span data-stu-id="c014e-121">Your Lync Server deployment would then recognize users from that federated organization, leading to better collaboration.</span></span>
    
      - <span data-ttu-id="c014e-122">ユーザーは、次のいずれか、またはすべて、Windows Live、AOL、Yahoo、Google Talk などのパブリック IM サービスのユーザーとインスタントメッセージをやり取りできます \! 。</span><span class="sxs-lookup"><span data-stu-id="c014e-122">Your users can exchange instant messages with users of public IM services, including any or all of the following: Windows Live, AOL, Yahoo\!, and Google Talk.</span></span> <span data-ttu-id="c014e-123">これらのサービスとのパブリック IM 接続には、個別のライセンスが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="c014e-123">A separate license might be required for public IM connectivity with these services.</span></span>
        
        <div>
        

        > [!IMPORTANT]  
        > <UL>
        > <LI>
        > <P><span data-ttu-id="c014e-124">2012年9月1日以降、Microsoft Lync パブリック IM 接続ユーザーサブスクリプションライセンス ("PIC USL") は、新規または更新契約の購入に使用できなくなりました。</span><span class="sxs-lookup"><span data-stu-id="c014e-124">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) is no longer available for purchase for new or renewing agreements.</span></span> <span data-ttu-id="c014e-125">アクティブなライセンスを持っているお客様は、Yahoo! とのフェデレーションを継続できます。</span><span class="sxs-lookup"><span data-stu-id="c014e-125">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="c014e-126">サービスが終了するまでの Messenger。</span><span class="sxs-lookup"><span data-stu-id="c014e-126">Messenger until the service shut down date.</span></span> <span data-ttu-id="c014e-127">AOL および Yahoo! の2014年6月の終了日</span><span class="sxs-lookup"><span data-stu-id="c014e-127">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="c014e-128">が発表されました。</span><span class="sxs-lookup"><span data-stu-id="c014e-128">has been announced.</span></span> <span data-ttu-id="c014e-129">詳細については、「 <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Lync Server 2013 でのパブリックインスタントメッセンジャー接続のサポート</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c014e-129">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
        > <LI>
        > <P><span data-ttu-id="c014e-130">PIC USL は、Lync Server または Office Communications Server が Yahoo! とのフェデレーションを行うために必要な1か月あたりのユーザーごとのサブスクリプションライセンスです。</span><span class="sxs-lookup"><span data-stu-id="c014e-130">The PIC USL is a per-user per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="c014e-131">Messenger.</span><span class="sxs-lookup"><span data-stu-id="c014e-131">Messenger.</span></span> <span data-ttu-id="c014e-132">このサービスを提供するための Microsoft の機能は、Yahoo! からのサポートによって決定されたものであり、その基となる契約は "巻停止" となります。</span><span class="sxs-lookup"><span data-stu-id="c014e-132">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which is winding down.</span></span></P>
        > <LI>
        > <P><span data-ttu-id="c014e-133">Lync は、組織間、および世界各地の個人と接続するための強力なツールです。</span><span class="sxs-lookup"><span data-stu-id="c014e-133">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="c014e-134">Windows Live Messenger とのフェデレーションには、Lync 標準 CAL 以外の追加のユーザー/デバイスライセンスは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="c014e-134">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="c014e-135">Skype federation はこのリストに追加されます。 Lync ユーザーは、IM と音声を使用して、数百人の何百万ものユーザーに連絡できます。</span><span class="sxs-lookup"><span data-stu-id="c014e-135">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span></P></LI></UL>

        
        </div>

  - <span data-ttu-id="c014e-136">**ブランチ サイトの存続性。**</span><span class="sxs-lookup"><span data-stu-id="c014e-136">**Branch site survivability.**</span></span>   <span data-ttu-id="c014e-137">この組織は、Lync Server のエンタープライズ Voip 機能のパイロットプログラムを実行しています。</span><span class="sxs-lookup"><span data-stu-id="c014e-137">This organization is running a pilot program of the Enterprise Voice feature of Lync Server.</span></span> <span data-ttu-id="c014e-138">一部のユーザーは、単独の音声ソリューションとして Lync Server を使用しています。</span><span class="sxs-lookup"><span data-stu-id="c014e-138">Some users are using Lync Server as their sole voice solution.</span></span> <span data-ttu-id="c014e-139">一部のボイスパイロットユーザーは、ブランチサイトに配置されています。</span><span class="sxs-lookup"><span data-stu-id="c014e-139">Some of these Voice pilot users are located at the branch site.</span></span> <span data-ttu-id="c014e-140">ブランチサイトには、セントラルサイトへの信頼性の高い広域ネットワーク (WAN) リンクがありません。したがって、Survivable Branch Appliance がそこに展開されます。</span><span class="sxs-lookup"><span data-stu-id="c014e-140">The branch site does not have a reliable wide area network (WAN) link to the central site, so a Survivable Branch Appliance is deployed there.</span></span> <span data-ttu-id="c014e-141">これが展開されていると、WAN リンクがダウンした場合でも、ブランチ サイトのユーザーは通話 (組織内の通話と PSTN 通話の両方) を発信および受信でき、ボイス メール機能は維持され、2 者間のインスタント メッセージング (IM) で通信できます。</span><span class="sxs-lookup"><span data-stu-id="c014e-141">With this deployed, if the WAN link goes down, users at the branch site can still make and receive calls (both calls within the organization and PSTN calls), have voice mail functionality, and communicate with two-party instant messaging (IM).</span></span> <span data-ttu-id="c014e-142">また、WAN リンクが使用不可能なときでも、ユーザーを認証できます。</span><span class="sxs-lookup"><span data-stu-id="c014e-142">Users can also be authenticated when the WAN link is unavailable as well.</span></span>

  - <span data-ttu-id="c014e-143">**Exchange UM の展開。**</span><span class="sxs-lookup"><span data-stu-id="c014e-143">**Exchange UM deployment.**</span></span> <span data-ttu-id="c014e-144">このリファレンストポロジには、Lync Server ではなく Microsoft Exchange Server を実行する Exchange ユニファイドメッセージング (UM) サーバーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="c014e-144">This reference topology includes an Exchange Unified Messaging (UM) Server, which runs Microsoft Exchange Server, not Lync Server.</span></span>
    
    <span data-ttu-id="c014e-145">Exchange UM の詳細については、計画ドキュメントの「 [Lync server 2013 での Exchange ユニファイドメッセージングの統合](lync-server-2013-planning-for-exchange-unified-messaging-integration.md) と [lync server 2013 でのホストされた Exchange ユニファイドメッセージングの統合](lync-server-2013-hosted-exchange-unified-messaging-integration.md) の計画」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c014e-145">For details about Exchange UM, see [Planning for Exchange Unified Messaging integration in Lync Server 2013](lync-server-2013-planning-for-exchange-unified-messaging-integration.md) and [Hosted Exchange Unified Messaging integration in Lync Server 2013](lync-server-2013-hosted-exchange-unified-messaging-integration.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="c014e-146">**Office Web Apps サーバー。**</span><span class="sxs-lookup"><span data-stu-id="c014e-146">**Office Web Apps Server.**</span></span> <span data-ttu-id="c014e-147">Web 会議を使用するすべての組織に Office Web Apps サーバーまたは Office Web Apps サーバー ファームを展開することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="c014e-147">We recommend deploying an Office Web Apps Server or Office Web Apps Server farm in every organization that uses web conferencing.</span></span> <span data-ttu-id="c014e-148">Office Web Apps サーバーを使用すると、PowerPoint スライドを Web 会議に表示することができます。</span><span class="sxs-lookup"><span data-stu-id="c014e-148">Office Web Apps Server makes it possible for PowerPoint slides to be presented in web conferences.</span></span> <span data-ttu-id="c014e-149">詳細については、「 [Office Web Apps サーバーおよび Lync server 2013 との統合を構成する](lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c014e-149">For more information, see [Configuring integration with Office Web Apps Server and Lync Server 2013](lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md).</span></span>

<span data-ttu-id="c014e-150"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c014e-150"></div>

<span> </span>

</div>

</div>

</span></span></div>

