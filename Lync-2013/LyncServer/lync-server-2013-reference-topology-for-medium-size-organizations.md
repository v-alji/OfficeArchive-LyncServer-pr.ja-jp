---
title: Lync Server 2013 の中規模組織用の関連トポロジ
description: 中小規模組織向けの Lync Server 2013 リファレンストポロジ。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Reference topology for medium-size organizations
ms:assetid: 446b0914-2198-445e-ab6e-94802acebd5c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425939(v=OCS.15)
ms:contentKeyID: 48184026
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3b9e6ef467506865193dc26887e802198b16f42f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436602"
---
# <a name="reference-topology-for-lync-server-2013-in-medium-size-organizations"></a><span data-ttu-id="bb5a7-103">Lync Server 2013 の中規模組織用の関連トポロジ</span><span class="sxs-lookup"><span data-stu-id="bb5a7-103">Reference topology for Lync Server 2013 in medium-size organizations</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bb5a7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bb5a7-104">

<span> </span></span></span>

<span data-ttu-id="bb5a7-105">_**最終更新日:** 2013-10-07_</span><span class="sxs-lookup"><span data-stu-id="bb5a7-105">_**Topic Last Modified:** 2013-10-07_</span></span>

<span data-ttu-id="bb5a7-p101">高可用性および 1 つのデータ センターを持つ関連トポロジは、1 つの中央サイトを擁する小～中規模組織向けに設計されています。次の図における正確なトポロジは、20,000 ユーザーの組織向けです。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-p101">The reference topology with high availability and a single data center is designed for a small-to-medium size organization with one central site. The exact topology in the following diagram is for an organization of 20,000 users.</span></span>

<span data-ttu-id="bb5a7-108">**中規模組織向けの関連トポロジ**</span><span class="sxs-lookup"><span data-stu-id="bb5a7-108">**Reference topology for medium organizations**</span></span>

<span data-ttu-id="bb5a7-109">![単一データ センター向けの関連トポロジの図](images/Gg425939.12b574fd-0b14-4563-a88c-3c8b0809bb90(OCS.15).jpg "単一データ センター向けの関連トポロジの図")</span><span class="sxs-lookup"><span data-stu-id="bb5a7-109">![Reference topology for single data center diagram](images/Gg425939.12b574fd-0b14-4563-a88c-3c8b0809bb90(OCS.15).jpg "Reference topology for single data center diagram")</span></span>

  - <span data-ttu-id="bb5a7-110">**より多くのフロントエンド サーバーを追加することでより多くのユーザーに対応。**</span><span class="sxs-lookup"><span data-stu-id="bb5a7-110">**Accommodate more users by adding more Front End Servers.**</span></span>   <span data-ttu-id="bb5a7-111">この図の正確なトポロジは 3 台のフロントエンド サーバーを擁するので、20,000 ユーザーをサポートします。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-111">The exact topology in this diagram has three Front End Servers to provide support for 20,000 users.</span></span> <span data-ttu-id="bb5a7-112">1 つの中央サイトおよびより多くのユーザーが存在する場合、単純により多くのフロントエンド サーバーをプールに追加できます。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-112">If you have a single central site and more users, you can simply add more Front End Servers to the pool.</span></span> <span data-ttu-id="bb5a7-113">プールごとの最大ユーザー数は、12 台のフロントエンド サーバーで、80,000 ユーザーです。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-113">The maximum number of users per pool is 80,000, with twelve Front End Servers.</span></span>
    
    <span data-ttu-id="bb5a7-114">ただし、サイトにもう 1 つのフロントエンド プールを追加すると、1 つのサイトのトポロジがさらに多くのユーザーをサポートできます。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-114">However, the single site topology can support even more users by adding another Front End pool to the site.</span></span>

  - <span data-ttu-id="bb5a7-115">**障害復旧機能を追加可能。**</span><span class="sxs-lookup"><span data-stu-id="bb5a7-115">**Disaster Recovery could be added.**</span></span>   <span data-ttu-id="bb5a7-116">この組織では、Lync Server サービスの高可用性が必要ですが、障害回復機能はありません。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-116">For this organization, high availability for their Lync Server services is a necessary feature, but disaster recovery is not.</span></span> <span data-ttu-id="bb5a7-117">展開されたフロントエンドサーバーのプールは、高可用性を実現します。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-117">The pool of Front End Servers they have deployed provides high availability.</span></span>
    
    <span data-ttu-id="bb5a7-p104">この組織が障害復旧機能を追加する場合は、別のデータセンターを確立し、そこに別のフロントエンド プールを追加して、そのフロントエンド プールを現在のデータセンターにあるフロントエンド プールとペアリングすることを検討します。プライマリ プールに影響を及ぼす障害が発生した場合は、管理者はユーザーをバックアップ プールにフェールオーバーすることができます。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-p104">If they wanted to add disaster recovery ability, they could consider establishing another datacenter and adding another Front End pool there, and pairing it with the Front End pool in their current datacenter. Then, if there was a disaster affecting their primary pool, the administrators could fail over users to the backup pool.</span></span>

  - <span data-ttu-id="bb5a7-120">**バックエンドサーバーがミラーリングされている**   基本的なユーザー機能の高可用性を実現するために、組織では、フロントエンドプールごとにバックエンドサーバーのミラーペアを展開しています。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-120">**Back End Servers are mirrored**   To provide more high availability for basic user features, the organization has deployed a mirrored pair of Back End Servers for each Front End pool.</span></span> <span data-ttu-id="bb5a7-121">これは Lync Server 2013 の新しいトポロジオプションであり、オプションです。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-121">This is a new topology option for Lync Server 2013, and is optional.</span></span> <span data-ttu-id="bb5a7-122">代わりに、単一のバックエンドサーバーを展開することもできます。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-122">You could choose to deploy a single Back End Server instead.</span></span>

  - <span data-ttu-id="bb5a7-123">**監視サーバー データベースのオプション。**</span><span class="sxs-lookup"><span data-stu-id="bb5a7-123">**Monitoring Server database options.**</span></span>   <span data-ttu-id="bb5a7-124">この組織は、エンタープライズ音声通話と A/V 会議の品質を確保するために、監視機能を導入しています。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-124">This organization has deployed Monitoring to ensure the quality of Enterprise Voice calls and A/V conferences.</span></span> <span data-ttu-id="bb5a7-125">監視機能は各フロントエンド サーバーに展開され、監視データベースはバックエンド サーバーと併置されます。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-125">Monitoring is deployed on every Front End Server, and the Monitoring database is collocated with the Back End Servers.</span></span> <span data-ttu-id="bb5a7-126">監視データベースが単独のサーバーに配置されるトポロジもサポートしています。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-126">We also support topologies in which the Monitoring database is located on a separate server.</span></span>

  - <span data-ttu-id="bb5a7-127">**エッジサーバーの高可用性**    この例の組織では、2万を使用していますが、パフォーマンスを向上させるには、1つのエッジサーバーだけで十分です。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-127">**Edge Server high availability**    In this example organization with 20,000 users, just one Edge Server would be sufficient for performance.</span></span> <span data-ttu-id="bb5a7-128">ただし、高可用性を実現するために展開された2つのエッジサーバーのプールがあります。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-128">However, there is a pool of two Edge Servers deployed to provide high availability.</span></span>

  - <span data-ttu-id="bb5a7-129">**ブランチ サイト展開のオプション。**</span><span class="sxs-lookup"><span data-stu-id="bb5a7-129">**Branch site deployment options.**</span></span>   <span data-ttu-id="bb5a7-130">このトポロジの組織は、ボイスソリューションとしてエンタープライズ Voip を展開しています。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-130">The organization in this topology has Enterprise Voice deployed as their voice solution.</span></span> <span data-ttu-id="bb5a7-131">ブランチサイト1には、セントラルサイトへの回復力のあるワイドエリアネットワーク (WAN) リンクがありません。そのため、セントラルサイトへの WAN リンクがダウンした場合に備えて、多くの Lync Server 機能を維持するために展開された Survivable Branch Appliance が導入されています。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-131">Branch Site 1 does not have a resilient wide area network (WAN) link to the central site, so it has a Survivable Branch Appliance deployed to maintain many Lync Server features in case the WAN link to the central site goes down.</span></span> <span data-ttu-id="bb5a7-132">ただし、ブランチ サイト 2 には回復可能な WAN リンクが存在するため、公衆交換電話網 (PSTN) ゲートウェイのみが必要となります。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-132">Branch Site 2 however has a resilient WAN link, so only a public switched telephone network (PSTN) gateway is needed.</span></span> <span data-ttu-id="bb5a7-133">そこで展開された PSTN ゲートウェイはメディア バイパスをサポートしているため、ブランチ サイト 2 では仲介サーバーが必要ありません。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-133">The PSTN gateway deployed there supports media bypass, so no Mediation Server is needed at Branch Site 2.</span></span> <span data-ttu-id="bb5a7-134">ブランチサイトで展開するものを決定する方法の詳細については、計画ドキュメントの「 [Lync Server 2013 でのブランチサイトの音声回復性の計画](lync-server-2013-planning-for-branch-site-voice-resiliency.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-134">For details about deciding what to deploy at a branch site, see [Planning for branch-site voice resiliency in Lync Server 2013](lync-server-2013-planning-for-branch-site-voice-resiliency.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="bb5a7-135">**DNS 負荷分散。**</span><span class="sxs-lookup"><span data-stu-id="bb5a7-135">**DNS load balancing.**</span></span>   <span data-ttu-id="bb5a7-136">フロントエンドプール andEdge サーバープールには、SIP トラフィックを展開するための DNS 負荷分散があります。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-136">The Front End pool andEdge Server pool, have DNS load balancing for SIP traffic deployed.</span></span> <span data-ttu-id="bb5a7-137">この機能によって、ロード バランサー機器は HTTP トラフィックに対してのみ必要となるため、エッジ サーバーにはロード バランサー機器が必要なくなり、その他のプールへのロード バランサー機器のセットアップおよびメンテナンスが非常に少なくなります。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-137">This eliminates the need for hardware load balancers for the Edge Servers, and significantly lessens the setup and maintenance of the hardware load balancers for the other pools, as the hardware load balancers are needed only for HTTP traffic.</span></span> <span data-ttu-id="bb5a7-138">DNS の負荷分散の詳細については、計画ドキュメントの「 [Lync Server 2013 での dns の負荷分散](lync-server-2013-dns-load-balancing.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-138">For details about DNS load balancing, see [DNS load balancing in Lync Server 2013](lync-server-2013-dns-load-balancing.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="bb5a7-139">**Exchange UM の展開。**</span><span class="sxs-lookup"><span data-stu-id="bb5a7-139">**Exchange UM deployment.**</span></span> <span data-ttu-id="bb5a7-140">このリファレンストポロジには、Lync Server ではなく Microsoft Exchange Server を実行する Exchange ユニファイドメッセージング (UM) サーバーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-140">This reference topology includes an Exchange Unified Messaging (UM) Server, which runs Microsoft Exchange Server, not Lync Server.</span></span>
    
    <span data-ttu-id="bb5a7-141">Exchange UM の詳細については、計画ドキュメントの「 [Lync server 2013 での Exchange ユニファイドメッセージングの統合](lync-server-2013-planning-for-exchange-unified-messaging-integration.md) と [lync server 2013 でのホストされた Exchange ユニファイドメッセージングの統合](lync-server-2013-hosted-exchange-unified-messaging-integration.md) の計画」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-141">For details about Exchange UM, see [Planning for Exchange Unified Messaging integration in Lync Server 2013](lync-server-2013-planning-for-exchange-unified-messaging-integration.md) and [Hosted Exchange Unified Messaging integration in Lync Server 2013](lync-server-2013-hosted-exchange-unified-messaging-integration.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="bb5a7-142">**Office Web Apps サーバー。**</span><span class="sxs-lookup"><span data-stu-id="bb5a7-142">**Office Web Apps Server.**</span></span> <span data-ttu-id="bb5a7-143">Web 会議を使用するすべての組織に Office Web Apps サーバーまたは Office Web Apps サーバー ファームを展開することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-143">We recommend deploying an Office Web Apps Server or Office Web Apps Server farm in every organization that uses web conferencing.</span></span> <span data-ttu-id="bb5a7-144">Office Web Apps サーバーを使用すると、Web 会議で PowerPoint スライドのプレゼンテーションを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-144">Office Web Apps Server makes it possible for Powerpoint slides to be presented in web conferences.</span></span> <span data-ttu-id="bb5a7-145">詳細については、「 [Office Web Apps サーバーおよび Lync server 2013 との統合を構成する](lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-145">For more information, see [Configuring integration with Office Web Apps Server and Lync Server 2013](lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md).</span></span>

  - <span data-ttu-id="bb5a7-146">**エッジサーバーをお勧めします。**</span><span class="sxs-lookup"><span data-stu-id="bb5a7-146">**Edge Servers are recommended.**</span></span>   <span data-ttu-id="bb5a7-147">エッジサーバーの展開は必須ではありませんが、展開の規模にかかわらずお勧めします。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-147">Although deploying an Edge Server is not required, we recommend it for any size of deployment.</span></span> <span data-ttu-id="bb5a7-148">組織のファイアウォールの外側にいるユーザーにサービスを提供するために、エッジサーバーを展開することで、Lync Server への投資を最大限に活用できます。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-148">You can maximize your Lync Server investment by deploying an Edge Server to provide service to users currently outside your organization’s firewalls.</span></span> <span data-ttu-id="bb5a7-149">その利点は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-149">The benefits include the following:</span></span>
    
      - <span data-ttu-id="bb5a7-150">組織の独自のユーザーは、自宅で作業しているか、外出先にいる場合でも、Lync Server 機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-150">Your organization’s own users can use Lync Server functionality, if they are working from home or are out on the road.</span></span>
    
      - <span data-ttu-id="bb5a7-151">ユーザーは、外部ユーザーを会議に参加するように招待できます。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-151">Your users can invite outside users to participate in meetings.</span></span>
    
      - <span data-ttu-id="bb5a7-152">Lync Server も使用しているパートナー、ベンダー、または顧客の組織がある場合は、その組織と *フェデレーション関係* を形成することができます。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-152">If you have a partner, vendor or customer organization that also uses Lync Server, you can form a *federated relationship* with that organization.</span></span> <span data-ttu-id="bb5a7-153">Lync Server の展開では、フェデレーションされた組織のユーザーが認識され、より効果的なコラボレーションが実現されます。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-153">Your Lync Server deployment would then recognize users from that federated organization, leading to better collaboration.</span></span>
    
      - <span data-ttu-id="bb5a7-154">ユーザーは、次のいずれか、またはすべて、Windows Live、AOL、Yahoo、Google Talk などのパブリック IM サービスのユーザーとインスタントメッセージをやり取りできます \! 。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-154">Your users can exchange instant messages with users of public IM services, including any or all of the following: Windows Live, AOL, Yahoo\!, and Google Talk.</span></span> <span data-ttu-id="bb5a7-155">これらのサービスとのパブリック IM 接続には、個別のライセンスが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-155">A separate license might be required for public IM connectivity with these services.</span></span>
        
        <div>
        

        > [!IMPORTANT]  
        > <UL>
        > <LI>
        > <P><span data-ttu-id="bb5a7-156">2012年9月1日以降、Microsoft Lync パブリック IM 接続ユーザーサブスクリプションライセンス ("PIC USL") は、新規または更新契約の購入に使用できなくなりました。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-156">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) is no longer available for purchase for new or renewing agreements.</span></span> <span data-ttu-id="bb5a7-157">アクティブなライセンスを持っているお客様は、Yahoo! とのフェデレーションを継続できます。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-157">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="bb5a7-158">サービスが終了するまでの Messenger。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-158">Messenger until the service shut down date.</span></span> <span data-ttu-id="bb5a7-159">AOL および Yahoo! の2014年6月の終了日</span><span class="sxs-lookup"><span data-stu-id="bb5a7-159">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="bb5a7-160">が発表されました。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-160">has been announced.</span></span> <span data-ttu-id="bb5a7-161">詳細については、「 <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Lync Server 2013 でのパブリックインスタントメッセンジャー接続のサポート</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-161">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
        > <LI>
        > <P><span data-ttu-id="bb5a7-162">PIC USL は、Lync Server または Office Communications Server が Yahoo! とのフェデレーションを行うために必要な1か月あたりのユーザーごとのサブスクリプションライセンスです。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-162">The PIC USL is a per-user per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="bb5a7-163">Messenger.</span><span class="sxs-lookup"><span data-stu-id="bb5a7-163">Messenger.</span></span> <span data-ttu-id="bb5a7-164">このサービスを提供するための Microsoft の機能は、Yahoo! からのサポートによって決定されたものであり、その基となる契約は "巻停止" となります。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-164">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which is winding down.</span></span></P>
        > <LI>
        > <P><span data-ttu-id="bb5a7-165">Lync は、組織間、および世界各地の個人と接続するための強力なツールです。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-165">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="bb5a7-166">Windows Live Messenger とのフェデレーションには、Lync 標準 CAL 以外の追加のユーザー/デバイスライセンスは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-166">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="bb5a7-167">Skype federation はこのリストに追加されます。 Lync ユーザーは、IM と音声を使用して、数百人の何百万ものユーザーに連絡できます。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-167">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span></P></LI></UL>

        
        </div>

  - <span data-ttu-id="bb5a7-168">**ディレクターを追加可能。**</span><span class="sxs-lookup"><span data-stu-id="bb5a7-168">**Directors could be added.**</span></span>   <span data-ttu-id="bb5a7-169">この組織は、サービス拒否攻撃に対するセキュリティを強化する場合、ディレクターのプールを展開することもできます。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-169">If this organization wanted to help to increase security against denial of service attacks, it could also deploy a pool of Directors.</span></span> <span data-ttu-id="bb5a7-170">ディレクターは、Lync Server で、ユーザーアカウントを持たない、またはプレゼンスまたは会議サービスを提供する、個別のオプションのサーバーの役割です。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-170">A Director is a separate, optional server role in Lync Server that does not home user accounts, or provide presence or conferencing services.</span></span> <span data-ttu-id="bb5a7-171">これは、内部サーバーに向けて、エッジサーバーが受信 SIP トラフィックをルーティングする、内部の次ホップサーバーとして機能します。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-171">It serves as an internal next hop server to which an Edge Server routes inbound SIP traffic destined for internal servers.</span></span> <span data-ttu-id="bb5a7-172">ディレクターは受信要求を事前に認証し、ユーザーのホームプールまたはサーバーにリダイレクトします。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-172">The Director pre-authenticates inbound requests and redirects them to the user’s home pool or server.</span></span> <span data-ttu-id="bb5a7-173">ディレクターでの事前認証により、展開にとって不明なユーザー アカウントからの要求を削除できます。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-173">Pre-authentication at the Director allows for dropping of requests from user accounts unknown to the deployment.</span></span> <span data-ttu-id="bb5a7-174">ディレクターは、サービス拒否 (DoS) 攻撃などの悪意のあるトラフィックからフロントエンドサーバーを分離するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-174">A Director helps insulate Front End Servers from malicious traffic such as denial-of-service (DoS) attacks.</span></span> <span data-ttu-id="bb5a7-175">このような攻撃で無効な外部トラフィックがネットワークにあふれている場合、トラフィックはディレクターで終了します。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-175">If the network is flooded with invalid external traffic in such an attack, the traffic ends at the Director.</span></span>

  - <span data-ttu-id="bb5a7-176">**System Center Operations Manager をお勧めします。**</span><span class="sxs-lookup"><span data-stu-id="bb5a7-176">**System Center Operations Manager is recommended.**</span></span>  <span data-ttu-id="bb5a7-177">Lync Server の展開の正常性を監視して、エンドユーザーがサービスを利用できるようにすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-177">We recommend that you monitor the health of your Lync Server deployment to help ensure service availability for end-users.</span></span> <span data-ttu-id="bb5a7-178">Lync の System Center Operations Manager 管理パックを使用して Lync を監視すると、Microsoft から無料でダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-178">You can monitor Lync with the System Center Operations Manager Management Pack for Lync that is available as a free download from Microsoft.</span></span> <span data-ttu-id="bb5a7-179">Lync 管理パックを使用すると、問題が発生したときにリアルタイムの通知を受信したり、代理として Lync 機能をテストしたり、サービスの可用性のレポートを取得したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="bb5a7-179">With the Lync Management Pack, you can proactively get real-time alerts when issues occur, run synthetic transactions to test end-to-end Lync functionality, get reports for service availability, and so on.</span></span>  <span data-ttu-id="bb5a7-180">This helps you to proactively respond to issues with your deployment before end-users experience them.</span><span class="sxs-lookup"><span data-stu-id="bb5a7-180">This helps you to proactively respond to issues with your deployment before end-users experience them.</span></span>

<span data-ttu-id="bb5a7-181"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bb5a7-181"></div>

<span> </span>

</div>

</div>

</span></span></div>

