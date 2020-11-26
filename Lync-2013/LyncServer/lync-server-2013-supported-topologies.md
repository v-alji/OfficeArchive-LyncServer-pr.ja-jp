---
title: Lync Server 2013 でサポートされるトポロジ
description: Lync Server 2013 でサポートされているトポロジ。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Supported topologies
ms:assetid: 3475d430-0394-491b-a09b-ba85bd62be70
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425833(v=OCS.15)
ms:contentKeyID: 48183832
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 39c19577fbda7e377e145abfd473d2cf8e6d4a1a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441432"
---
# <a name="supported-topologies-in-lync-server-2013"></a><span data-ttu-id="39b64-103">Lync Server 2013 でサポートされるトポロジ</span><span class="sxs-lookup"><span data-stu-id="39b64-103">Supported topologies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="39b64-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="39b64-104">

<span> </span></span></span>

<span data-ttu-id="39b64-105">_**最終更新日:** 2014-01-14_</span><span class="sxs-lookup"><span data-stu-id="39b64-105">_**Topic Last Modified:** 2014-01-14_</span></span>

<span data-ttu-id="39b64-106">Lync Server 2013 は、組織内のサイトの展開と、オンプレミスの展開と Lync Online の展開との統合をサポートします。これはハイブリッド展開と呼ばれています。</span><span class="sxs-lookup"><span data-stu-id="39b64-106">Lync Server 2013 supports deployment of sites on premises in an organization and integration of on-premises deployments with Lync Online deployments, which is known as a hybrid deployment.</span></span> <span data-ttu-id="39b64-107">ハイブリッド展開では、一部のユーザーがオンプレミスであり、一部のユーザーがオンラインである場合があります。</span><span class="sxs-lookup"><span data-stu-id="39b64-107">In a hybrid deployment, some users are homed on-premises and some users are homed online.</span></span>

<span data-ttu-id="39b64-108">オンプレミスの展開では、Lync Server 2013 は、高可用性と場所の要件を満たすために拡大縮小できる1つ以上のサイトの展開をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="39b64-108">For on-premises deployments, Lync Server 2013 supports deployment of one or more sites that can be scaled to meet high availability and location requirements.</span></span> <span data-ttu-id="39b64-109">組織のアクセスと復元性の要件を満たすために、これらのサイトとコンポーネントを構造化することができます。</span><span class="sxs-lookup"><span data-stu-id="39b64-109">You can structure these sites and their components to meet the access and resiliency requirements of your organization.</span></span>

<span data-ttu-id="39b64-110">Lync Server 2013 オンプレミスの展開は、次のように構成されています。</span><span class="sxs-lookup"><span data-stu-id="39b64-110">A Lync Server 2013 on-premises deployment consists of the following:</span></span>

  - <span data-ttu-id="39b64-111">展開には、少なくとも1つのセントラルサイト (データセンターとも呼ばれます) が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="39b64-111">Your deployment must include at least one central site (also known as a data center).</span></span> <span data-ttu-id="39b64-112">各セントラルサイトには、少なくとも1つの Enterprise Edition フロントエンドプールまたは Standard Edition サーバーが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="39b64-112">Each central site must contain at least one Enterprise Edition Front End pool or one Standard Edition server.</span></span> <span data-ttu-id="39b64-113">以下の要素で構成されています。</span><span class="sxs-lookup"><span data-stu-id="39b64-113">These consist of the following:</span></span>
    
      - <span data-ttu-id="39b64-114">Enterprise Edition のフロントエンドプール。1つ以上のフロントエンドサーバー (通常はスケーラビリティ用の最低2台のフロントエンドサーバー) と個別のバックエンドサーバーで構成されます。</span><span class="sxs-lookup"><span data-stu-id="39b64-114">Enterprise Edition Front End pool, which consists of one or more Front End Servers (typically, at least two Front End Servers for scalability) and a separate Back End Server.</span></span> <span data-ttu-id="39b64-115">フロントエンドプールには、最大で12個のフロントエンドサーバーを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="39b64-115">A Front End pool can contain a maximum of twelve Front End Servers.</span></span> <span data-ttu-id="39b64-116">複数のフロントエンドサーバーでは、負荷分散が必要です。</span><span class="sxs-lookup"><span data-stu-id="39b64-116">Load balancing is required for multiple Front End Servers.</span></span> <span data-ttu-id="39b64-117">SIP トラフィックの場合は、DNS の負荷分散をお勧めしますが、ハードウェア負荷分散もサポートされています。</span><span class="sxs-lookup"><span data-stu-id="39b64-117">For SIP traffic, we recommend DNS load balancing, but hardware load balancing is also supported.</span></span> <span data-ttu-id="39b64-118">SIP トラフィックで DNS 負荷分散を使用している場合も、HTTP トラフィック用のハードウェアロードバランサーが必要です。</span><span class="sxs-lookup"><span data-stu-id="39b64-118">If you use DNS load balancing for SIP traffic, you still need a hardware load balancer for HTTP traffic.</span></span> <span data-ttu-id="39b64-119">データベースの高可用性を実現するには、SQL Server のミラーリングをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="39b64-119">We recommend SQL Server mirroring for high availability of databases.</span></span> <span data-ttu-id="39b64-120">バックエンドデータベースには個別のインスタンスが必要ですが、アーカイブデータベース、監視データベース、常設チャットデータベース、および永続的なチャットのコンプライアンスデータベースを検索することができます。</span><span class="sxs-lookup"><span data-stu-id="39b64-120">The back-end database requires a separate instance, but you can collocate the archiving database, monitoring database, persistent chat database, and persistent chat compliance database with it.</span></span> <span data-ttu-id="39b64-121">Lync Server 2013 では、展開内のファイル共有に対して、共有クラスターの使用がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="39b64-121">Lync Server 2013 supports the use of a shared cluster for the file shares in your deployment.</span></span> <span data-ttu-id="39b64-122">データベース記憶域の要件の詳細については、「 [Lync Server 2013 でのデータベースソフトウェアのサポート](lync-server-2013-database-software-support.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39b64-122">For details about database storage requirements, see [Database software support in Lync Server 2013](lync-server-2013-database-software-support.md).</span></span> <span data-ttu-id="39b64-123">ファイル記憶域の要件の詳細については、「 [Lync Server 2013 でのファイルストレージのサポート](lync-server-2013-file-storage-support.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39b64-123">For details about file storage requirements, see [File storage support in Lync Server 2013](lync-server-2013-file-storage-support.md).</span></span>
        
        <div>
        

        > [!IMPORTANT]  
        > <span data-ttu-id="39b64-124">Lync Server データベースを作成する場合は、可用性とパフォーマンスに影響する可能性があるすべての要因を評価することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="39b64-124">If you collocate Lync Server databases, we highly recommend assessing all factors that might affect availability and performance.</span></span> <span data-ttu-id="39b64-125">フェールオーバー機能を検証する場合は、すべてのフェールオーバー シナリオをテストすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="39b64-125">To verify failover capabilities, we recommend testing all failover scenarios.</span></span>

        
        </div>
    
      - <span data-ttu-id="39b64-126">Standard Edition server: 併置された SQL Server Express データベースが含まれています。</span><span class="sxs-lookup"><span data-stu-id="39b64-126">Standard Edition server, which includes a collocated SQL Server Express database.</span></span>

  - <span data-ttu-id="39b64-127">展開には、1つのセントラルサイトに関連付けられた1つ以上の分岐サイトを含めることもできます。</span><span class="sxs-lookup"><span data-stu-id="39b64-127">Your deployment can also have one or more branch sites associated with a central site.</span></span>

<span data-ttu-id="39b64-128">このセクションでは、Lync Server 2013 展開のサイトとコンポーネントについて説明します。</span><span class="sxs-lookup"><span data-stu-id="39b64-128">This section describes the sites and components of a Lync Server 2013 deployment.</span></span> <span data-ttu-id="39b64-129">Lync Server 2013 サイト、トポロジ、およびコンポーネントの計画の詳細については、「トポロジの基礎」を参照してください。 lync server 2013 と[参照2013トポロジ](lync-server-2013-reference-topologies.md)[の計画](lync-server-2013-topology-basics-you-must-know-before-planning.md)については、計画に関するドキュメントをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="39b64-129">For details about Lync Server 2013 site, topology, and component planning, see [Topology basics you must know before planning for Lync Server 2013](lync-server-2013-topology-basics-you-must-know-before-planning.md) and [Reference topologies in Lync Server 2013](lync-server-2013-reference-topologies.md) in the Planning documentation.</span></span> <span data-ttu-id="39b64-130">以前のリリースのコンポーネントの統合の詳細については、「 [Lync Server 2013 でサポートされている移行パスと共存シナリオ](lync-server-2013-supported-migration-paths-and-coexistence-scenarios.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39b64-130">For details about integration of components of previous releases, see [Supported migration paths and coexistence scenarios in Lync Server 2013](lync-server-2013-supported-migration-paths-and-coexistence-scenarios.md).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="39b64-131">ストレッチプールは、フロントエンド、エッジ、仲介、およびディレクターサーバーの役割に対してはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="39b64-131">Stretched pools are not supported for the Front End, Edge, Mediation, and Director server roles.</span></span>



</div>

<div>

## <a name="central-site-topologies-and-components-on-premises"></a><span data-ttu-id="39b64-132">セントラルサイトトポロジとコンポーネント (オンプレミス)</span><span class="sxs-lookup"><span data-stu-id="39b64-132">Central Site Topologies and Components (On-Premises)</span></span>

<span data-ttu-id="39b64-133">セントラルサイトトポロジには1つのフロントエンドプールまたは1つの Standard Edition サーバーを含める必要がありますが、各セントラルサイトには次の情報も含めることができます。</span><span class="sxs-lookup"><span data-stu-id="39b64-133">Although a central site topology must include one Front End pool or one Standard Edition server, each central site can also contain the following:</span></span>

  - <span data-ttu-id="39b64-134">複数のフロントエンドプール。同じドメインまたは異なるドメインに存在することができます。</span><span class="sxs-lookup"><span data-stu-id="39b64-134">Multiple Front End pools, which can be in the same domain or different domains.</span></span> <span data-ttu-id="39b64-135">ただし、フロントエンドプール内のすべてのフロントエンドサーバーとそのプールのバックエンドサーバーは同じドメイン内に存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="39b64-135">However, all Front End Servers in a Front End pool, and the Back End Server for that pool, must be in the same domain.</span></span>

  - <span data-ttu-id="39b64-136">複数の Standard Edition サーバー。</span><span class="sxs-lookup"><span data-stu-id="39b64-136">Multiple Standard Edition servers.</span></span>

  - <span data-ttu-id="39b64-137">Microsoft PowerPoint プレゼンテーションの共有とレンダリングを処理するために、Lync Server 2013 の Office Web アプリケーションと共に使用される office Web Apps サーバー。</span><span class="sxs-lookup"><span data-stu-id="39b64-137">Office Web Apps Server, which is used with Office Web Applications in Lync Server 2013 to handle the sharing and rendering of Microsoft PowerPoint presentations.</span></span>

  - <span data-ttu-id="39b64-138">境界ネットワーク内のエッジサーバーまたはエッジプール。展開でフェデレーションパートナー、パブリック IM 接続、拡張メッセージングとプレゼンスプロトコル (XMPP) ゲートウェイ、リモートユーザーアクセス、会議での匿名ユーザーの参加、または Exchange ユニファイドメッセージング (UM) をサポートする必要がある場合。</span><span class="sxs-lookup"><span data-stu-id="39b64-138">Edge Server or Edge pool in your perimeter network, if you want your deployment to support federated partners, public IM connectivity, an extensible messaging and presence protocol (XMPP) gateway, remote user access, participation of anonymous users in meetings, or Exchange Unified Messaging (UM).</span></span> <span data-ttu-id="39b64-139">エッジサーバーを使用して、他のサーバーの役割を検索することはできません。</span><span class="sxs-lookup"><span data-stu-id="39b64-139">You cannot collocate any other server role with an Edge Server.</span></span> <span data-ttu-id="39b64-140">必要に応じて DNS の負荷分散をお勧めしますが、ハードウェアの負荷分散もサポートされています。</span><span class="sxs-lookup"><span data-stu-id="39b64-140">We recommend DNS load balancing, where appropriate, but hardware load balancing is also supported.</span></span> <span data-ttu-id="39b64-141">内部エッジ インターフェイスと外部エッジ インターフェイスでは、同じ種類のロード バランシングを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="39b64-141">The internal Edge interface and external Edge interface must use the same type of load balancing.</span></span> <span data-ttu-id="39b64-142">1 つのエッジ インターフェイスで DNS ロード バランシングを使用し、もう 1 つのエッジ インターフェイスでロード バランサー機器を使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="39b64-142">You cannot use DNS load balancing on one Edge interface and hardware load balancing on the other Edge interface.</span></span> <span data-ttu-id="39b64-143">負荷分散の要件とサポートの詳細については、「Lync server 2013 での [外部ユーザーアクセスの計画](lync-server-2013-planning-for-external-user-access.md) 」を参照してください。展開ドキュメントの「 [lync server 2013 での外部ユーザーアクセスの展開](lync-server-2013-deploying-external-user-access.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39b64-143">For details about load balancing requirements and support, see [Planning for external user access in Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) in the Planning documentation and [Deploying external user access in Lync Server 2013](lync-server-2013-deploying-external-user-access.md) in the Deployment documentation.</span></span>

  - <span data-ttu-id="39b64-144">中央サイトのフロントエンドプールでエンタープライズボイスまたはダイヤルイン会議をサポートする場合は、仲介サーバーまたはプール。</span><span class="sxs-lookup"><span data-stu-id="39b64-144">Mediation Server or pool, if you want to support Enterprise Voice or dial-in conferencing in a Front End pool at the central site.</span></span> <span data-ttu-id="39b64-145">エンタープライズボイスのサポートを展開する方法に応じて、仲介サーバーをフロントエンドプール (既定) で検索するか、スタンドアロンの仲介サーバーまたはプールを展開することができます。</span><span class="sxs-lookup"><span data-stu-id="39b64-145">Depending on how you deploy Enterprise Voice support, you can collocate the Mediation Server in a Front End pool (the default) or deploy a stand-alone Mediation Server or pool.</span></span> <span data-ttu-id="39b64-146">DNS、ハードウェア、またはアプリケーションの負荷分散 (該当する場合) を使用して、PSTN ゲートウェイ、IP PBX、SIP トランクセッション境界制御 (SBC) を含む、仲介サーバープールのゲートウェイピアからトラフィックを分散することができます。適切な仲介サーバートポロジの計画の詳細については、計画ドキュメントの「 [Lync server 2013 での仲介サーバーの展開ガイドライン](lync-server-2013-deployment-guidelines-for-mediation-server.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39b64-146">You can use DNS, hardware, or application load balancing (when appropriate) to distribute traffic from a Mediation Server pool’s gateway peer, including a PSTN gateway, IP-PBX, or SIP trunk Session Border Control (SBC).For details about planning the appropriate Mediation Server topology, see [Deployment guidelines for Mediation Server in Lync Server 2013](lync-server-2013-deployment-guidelines-for-mediation-server.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="39b64-147">常設チャットサーバー。ユーザーがマルチパーティに参加できるようにする場合、トピックベースの会話は時間を経て維持されます。</span><span class="sxs-lookup"><span data-stu-id="39b64-147">Persistent Chat Server, if you want to users to be able to participate in multiparty, topic-based conversations that persist over time.</span></span> <span data-ttu-id="39b64-148">容量と信頼性をさらに高めるために、トポロジには、常設チャットサーバーを実行している複数のコンピューターを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="39b64-148">To provide more capacity and increased reliability, your topology can include multiple computers running Persistent Chat Server.</span></span> <span data-ttu-id="39b64-149">エンタープライズプールでは、他のサーバーの役割と共に常設チャットサーバーを検索することはできません。</span><span class="sxs-lookup"><span data-stu-id="39b64-149">You cannot collocate Persistent Chat Server with other server roles in an Enterprise pool.</span></span> <span data-ttu-id="39b64-150">ただし、Standard Edition サーバでは、常設チャットサーバを検索することができます。</span><span class="sxs-lookup"><span data-stu-id="39b64-150">However, you can collocate Persistent Chat Server on a Standard Edition server.</span></span> <span data-ttu-id="39b64-151">常設チャットを使用するにはデータベースが必要です。また、常設チャットのコンプライアンスデータベースを実装していても、データベースがアーカイブデータベース、監視データベース、または Enterprise Edition フロントエンドプールのバックエンドサーバーに関連付けられていることがあります。</span><span class="sxs-lookup"><span data-stu-id="39b64-151">Persistent chat requires a database and, if you implement persistent chat compliance, a persistent chat compliance database, but the databases can be collocated with the Archiving database, Monitoring database, or on the Back End Server of an Enterprise Edition Front End pool.</span></span> <span data-ttu-id="39b64-152">適切な常設チャットサーバートポロジの計画の詳細については、計画ドキュメントの「 [Lync server 2013 での常設チャットサーバーの計画](lync-server-2013-planning-for-persistent-chat-server.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39b64-152">For details about planning the appropriate Persistent Chat Server topology, see [Planning for Persistent Chat Server in Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="39b64-153">監視 (オーディオ/ビデオ品質エクスペリエンス (QoE) のデータ収集をサポートし、展開でのエンタープライズボイスと A/V 会議の通話の詳細記録 (CDR) をサポートする場合。</span><span class="sxs-lookup"><span data-stu-id="39b64-153">Monitoring, if you want to support data collection for audio/video Quality of Experience (QoE) and call detail recording (CDR) for Enterprise Voice and A/V conferences in your deployment.</span></span> <span data-ttu-id="39b64-154">必要に応じて、Microsoft System Center Operations Manager (以前の Microsoft Operations Manager) をインストールできます。これには、データの監視と QoE データを使って、通話の信頼性とメディアの品質の正常性を示す、ほぼリアルタイムの通知を生成することができます。</span><span class="sxs-lookup"><span data-stu-id="39b64-154">Optionally, you can install the Microsoft System Center Operations Manager (formerly Microsoft Operations Manager), which uses Monitoring CDR and QoE data to generate near real-time alerts that show the health of call reliability and media quality.</span></span> <span data-ttu-id="39b64-155">展開された場合、監視はフロントエンドサーバーまたは Standard Edition サーバーに配置されます。</span><span class="sxs-lookup"><span data-stu-id="39b64-155">Monitoring, when deployed, is collocated on Front End Servers or a Standard Edition server.</span></span> <span data-ttu-id="39b64-156">監視にはデータベースが必要ですが、データベースは、アーカイブデータベース、常設チャットデータベース、常設チャットのコンプライアンスデータベース、または Enterprise Edition フロントエンドプールのバックエンドサーバーでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="39b64-156">Monitoring requires a database, but the database can be collocated with the Archiving database, persistent chat database, persistent chat compliance database, or on the Back End Server of an Enterprise Edition Front End pool.</span></span>

  - <span data-ttu-id="39b64-157">展開で IM 通信と会議のコンテンツ (コンプライアンスのための理由) をアーカイブする場合は、[アーカイブ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="39b64-157">Archiving, if you want to archive IM communications and meeting content (for compliance reasons) in your deployment.</span></span> <span data-ttu-id="39b64-158">展開された場合、アーカイブはフロントエンドサーバーまたは Standard Edition サーバーに配置されます。</span><span class="sxs-lookup"><span data-stu-id="39b64-158">Archiving, when deployed, is collocated on Front End Servers or a Standard Edition server.</span></span> <span data-ttu-id="39b64-159">アーカイブストレージを使用するには、アーカイブデータベースの展開または Exchange 2013 ストレージとの統合のいずれかを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="39b64-159">Archiving storage requires either deployment of an Archiving database or integration with Exchange 2013 storage.</span></span> <span data-ttu-id="39b64-160">*混在モード* と呼ばれる両方を使用している場合、exchange 2013 ストレージは exchange 2013 を使用しているユーザーのアーカイブデータを保存するために使用され、アーカイブデータベースは、展開内の他のすべてのユーザーのデータをアーカイブするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="39b64-160">If you use both, which is known as *mixed mode*, Exchange 2013 storage is used to store archive data for users who are homed on Exchange 2013, and the Archiving database is used to archive data for all other users in your deployment.</span></span> <span data-ttu-id="39b64-161">アーカイブデータベースが必要な場合は、データベースを監視データベース、常設チャットデータベース、常設チャットのコンプライアンスデータベース、またはフロントエンドプールのバックエンドサーバーに併置することができます。</span><span class="sxs-lookup"><span data-stu-id="39b64-161">If you require an Archiving database, the database can be collocated on the Monitoring database, persistent chat database, persistent chat compliance database, or on the Back End Server of a Front End pool.</span></span> <span data-ttu-id="39b64-162">適切なアーカイブトポロジの計画の詳細については、計画ドキュメントの「 [Lync Server 2013 でのアーカイブの計画](lync-server-2013-planning-for-archiving.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39b64-162">For details about planning the appropriate Archiving topology, see [Planning for Archiving in Lync Server 2013](lync-server-2013-planning-for-archiving.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="39b64-163">ユーザーのホームプールへの Lync Server 2013 ユーザー要求の回復とリダイレクションを容易にするには、ディレクターまたはディレクタープールを使用します。これは、Enterprise Edition フロントエンドプールまたは Standard Edition サーバーのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="39b64-163">Director or Director pool, if you want to facilitate resiliency and redirection of Lync Server 2013 user requests to the user’s home pool, which can be either an Enterprise Edition Front End pool or a Standard Edition server.</span></span> <span data-ttu-id="39b64-164">外部ユーザーアクセスをサポートするセントラルサイトと、1つ以上のフロントエンドプールを展開する各セントラルサイトにディレクターまたはディレクタープールを展開することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="39b64-164">We recommend that you deploy a Director or Director pool in each central site that supports external user access and in each central site in which you deploy one or more Front End pools.</span></span> <span data-ttu-id="39b64-165">各ディレクタープールには、最大10個のディレクターを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="39b64-165">Each Director pool can contain a maximum of ten Directors.</span></span> <span data-ttu-id="39b64-166">ディレクターは、他のサーバーの役割と併置することはできません。</span><span class="sxs-lookup"><span data-stu-id="39b64-166">A Director cannot be collocated with any other server role.</span></span> <span data-ttu-id="39b64-167">適切なディレクタートポロジの計画の詳細については、計画ドキュメントの「 [Lync Server 2013 のディレクターのシナリオ](lync-server-2013-scenarios-for-the-director.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39b64-167">For details about planning the appropriate Director topology, see [Scenarios for the Director in Lync Server 2013](lync-server-2013-scenarios-for-the-director.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="39b64-168">リバースプロキシ (Lync Server 2013 コンポーネントではありません)。フェデレーションされたユーザーに対して web コンテンツの共有をサポートしたり、モビリティートラフィックをサポートしたりする場合に必要です。</span><span class="sxs-lookup"><span data-stu-id="39b64-168">Reverse proxy, which is not a Lync Server 2013 component, but is required if you want to support sharing of web content for federated users or to support Mobility traffic.</span></span> <span data-ttu-id="39b64-169">任意の Lync Server 2013 サーバーの役割を持つリバースプロキシサーバーを作成することはできませんが、他のアプリケーションで使用されている組織内の既存のリバースプロキシサーバーのサポートを構成することによって、Lync Server 2013 展開のリバースプロキシサポートを実装することができます。</span><span class="sxs-lookup"><span data-stu-id="39b64-169">You cannot collocate a reverse proxy server with any Lync Server 2013 server role, but you can implement reverse proxy support for a Lync Server 2013 deployment by configuring the support on an existing reverse proxy server in your organization that is used for other applications.</span></span> <span data-ttu-id="39b64-170">リバースプロキシサーバーの詳細については、展開ドキュメントで「 [Lync Server 2013 用のリバースプロキシサーバー](lync-server-2013-setting-up-reverse-proxy-servers.md) をセットアップする」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39b64-170">For details about reverse proxy servers, see [Setting up reverse proxy servers for Lync Server 2013](lync-server-2013-setting-up-reverse-proxy-servers.md) in the Deployment documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="39b64-171">Lync Server 2013 では、フロントエンドサーバーで A/V 会議、監視、およびアーカイブが実行され、別のサーバーの役割はありません。</span><span class="sxs-lookup"><span data-stu-id="39b64-171">In Lync Server 2013, A/V Conferencing, Monitoring, and Archiving run on Front End Servers and are no longer separate server roles.</span></span>



</div>

<span data-ttu-id="39b64-172">セントラルサイトに展開するすべてのフロントエンドプールおよび標準エディションのサーバーは、セントラルサイト用に展開する次のいずれかを共有します。</span><span class="sxs-lookup"><span data-stu-id="39b64-172">All Front End pools and Standard Edition servers that you deploy at a central site share any of the following that you deploy for the central site:</span></span>

  - <span data-ttu-id="39b64-173">ディレクターまたはディレクタープール</span><span class="sxs-lookup"><span data-stu-id="39b64-173">Director or Director pool</span></span>

  - <span data-ttu-id="39b64-174">スタンドアロンの仲介サーバーまたはプール</span><span class="sxs-lookup"><span data-stu-id="39b64-174">Stand-alone Mediation Server or pool</span></span>

  - <span data-ttu-id="39b64-175">Office Web Apps サーバー</span><span class="sxs-lookup"><span data-stu-id="39b64-175">Office Web Apps Server</span></span>

  - <span data-ttu-id="39b64-176">エッジサーバーまたはエッジプール</span><span class="sxs-lookup"><span data-stu-id="39b64-176">Edge Server or Edge pool</span></span>

  - <span data-ttu-id="39b64-177">常設チャットサーバーまたはプール</span><span class="sxs-lookup"><span data-stu-id="39b64-177">Persistent Chat Server or pool</span></span>

  - <span data-ttu-id="39b64-178">監視</span><span class="sxs-lookup"><span data-stu-id="39b64-178">Monitoring</span></span>

  - <span data-ttu-id="39b64-179">アーカイブ</span><span class="sxs-lookup"><span data-stu-id="39b64-179">Archiving</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="39b64-180">Exchange 2013 ユニファイドメッセージングの統合をサポートしていても、Lync Server 2013 サイトのコンポーネントではない場合は、Exchange UM サーバーを実装して、Lync Server 2013 展開を使用できます。</span><span class="sxs-lookup"><span data-stu-id="39b64-180">An Exchange UM Server can be implemented with your Lync Server 2013 deployment if you want to support integration of Exchange 2013 Unified Messaging, but it is not a component of the Lync Server 2013 site.</span></span>



</div>

<span data-ttu-id="39b64-181">また、複数のセントラルサイトは、1つのセントラルサイトに展開する次のいずれかを共有することもできます。</span><span class="sxs-lookup"><span data-stu-id="39b64-181">Multiple central sites can also share any of the following that you deploy in one central site:</span></span>

  - <span data-ttu-id="39b64-182">スタンドアロンの仲介サーバーまたはプール</span><span class="sxs-lookup"><span data-stu-id="39b64-182">Stand-alone Mediation Server or pool</span></span>

  - <span data-ttu-id="39b64-183">エッジサーバーまたはエッジプール</span><span class="sxs-lookup"><span data-stu-id="39b64-183">Edge Server or Edge pool</span></span>

  - <span data-ttu-id="39b64-184">常設チャットサーバーまたはプール</span><span class="sxs-lookup"><span data-stu-id="39b64-184">Persistent Chat Server or pool</span></span>

  - <span data-ttu-id="39b64-185">アーカイブ</span><span class="sxs-lookup"><span data-stu-id="39b64-185">Archiving</span></span>

  - <span data-ttu-id="39b64-186">監視</span><span class="sxs-lookup"><span data-stu-id="39b64-186">Monitoring</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="39b64-187">Exchange UM サーバーは、Lync Server 2013 の展開を使用して実装し、複数のセントラルサイトで共有できますが、これは Lync Server 2013 サイトのコンポーネントではありません。</span><span class="sxs-lookup"><span data-stu-id="39b64-187">An Exchange UM Server can be implemented with your Lync Server 2013 deployment and shared by multiple central sites, but it is not a component of the Lync Server 2013 site.</span></span>



</div>

<span data-ttu-id="39b64-188">Lync Server 2013 サーバーの役割と機能の詳細については、計画ドキュメントの「 [Lync server 2013 のサーバーの役割](lync-server-2013-server-roles.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39b64-188">For details about Lync Server 2013 server roles and functionality, see [Server roles in Lync Server 2013](lync-server-2013-server-roles.md) in the Planning documentation.</span></span>

<span data-ttu-id="39b64-189">Lync Server 2013 server collocation のサポートの概要については、「 [Lync server 2013 でサポートされているサーバーの collocation](lync-server-2013-supported-server-collocation.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39b64-189">For a summary of Lync Server 2013 server collocation support, see [Supported server collocation in Lync Server 2013](lync-server-2013-supported-server-collocation.md).</span></span>

<span data-ttu-id="39b64-190">このセクションで既に説明したサーバーの役割と機能に加えて、Lync Server 2013 には、次の一部またはすべてを含めることができるコンポーネントとオプションが追加されています。</span><span class="sxs-lookup"><span data-stu-id="39b64-190">In addition to the server roles and functionality covered previously in this section, Lync Server 2013 has additional components and options, which can include some or all of the following:</span></span>

  - <span data-ttu-id="39b64-191">ファイアウォール</span><span class="sxs-lookup"><span data-stu-id="39b64-191">Firewalls</span></span>

  - <span data-ttu-id="39b64-192">PSTN ゲートウェイ (エンタープライズ Voip を展開している場合)</span><span class="sxs-lookup"><span data-stu-id="39b64-192">PSTN gateways (if deploying Enterprise Voice)</span></span>

  - <span data-ttu-id="39b64-193">Exchange UM サーバー</span><span class="sxs-lookup"><span data-stu-id="39b64-193">Exchange UM Server</span></span>

  - <span data-ttu-id="39b64-194">DNS 負荷分散</span><span class="sxs-lookup"><span data-stu-id="39b64-194">DNS load balancing</span></span>

  - <span data-ttu-id="39b64-195">ハードウェア ロード バランサー</span><span class="sxs-lookup"><span data-stu-id="39b64-195">Hardware load balancers</span></span>

  - <span data-ttu-id="39b64-196">SQL Server データベース</span><span class="sxs-lookup"><span data-stu-id="39b64-196">SQL Server databases</span></span>

  - <span data-ttu-id="39b64-197">ファイル共有</span><span class="sxs-lookup"><span data-stu-id="39b64-197">File shares</span></span>

<span data-ttu-id="39b64-198">Lync Server の2013のすべての機能、コンポーネント、およびオプションの詳細については、計画に関するドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="39b64-198">For details about all of the Lync Server 2013 features, components, and options, see the Planning documentation.</span></span>

</div>

<div>

## <a name="branch-site-topologies-and-components-on-premises"></a><span data-ttu-id="39b64-199">ブランチサイトのトポロジとコンポーネント (オンプレミス)</span><span class="sxs-lookup"><span data-stu-id="39b64-199">Branch Site Topologies and Components (On-Premises)</span></span>

<span data-ttu-id="39b64-200">ブランチサイトはセントラルサイトに関連付けられ、ブランチサイト内の各 Survivable Branch アプライアンスは、関連付けられたセントラルサイトの Enterprise Edition フロントエンドプールまたは Standard Edition サーバーに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="39b64-200">A branch site is associated with a central site, and each Survivable Branch Appliance in a branch site is associated with an Enterprise Edition Front End pool or a Standard Edition server in the associated central site.</span></span> <span data-ttu-id="39b64-201">ブランチサイトは、ほとんどの機能についてセントラルサイトに依存しているため、ブランチサイトのコンポーネントには次のものしかありません。</span><span class="sxs-lookup"><span data-stu-id="39b64-201">Branch sites depend on the central site for most of their functionality, so components at a branch site contain only the following:</span></span>

  - <span data-ttu-id="39b64-202">Survivable Branch Appliance。公衆交換電話網 (PSTN) ゲートウェイと一部の Lync Server 機能を組み合わせたものです。</span><span class="sxs-lookup"><span data-stu-id="39b64-202">A Survivable Branch Appliance, which combines a public switched telephone network (PSTN) gateway with some Lync Server functionality.</span></span> <span data-ttu-id="39b64-203">仲介サーバーは、Survivable Branch Appliance のレジストラーのインスタンスと連携することができます。また、スタンドアロンの仲介サーバーまたは仲介サーバープールを展開することもできます。</span><span class="sxs-lookup"><span data-stu-id="39b64-203">A Mediation Server can be collocated with the instance of the Registrar on the Survivable Branch Appliance, and you can deploy a stand-alone Mediation Server or pool of Mediation Servers.</span></span>

  - <span data-ttu-id="39b64-204">Survivable Branch Server。 Lync Server 2013 レジストラーと仲介サーバーソフトウェアがインストールされている Windows Server を実行しているサーバーです。</span><span class="sxs-lookup"><span data-stu-id="39b64-204">A Survivable Branch Server, which is a server running Windows Server that has Lync Server 2013 Registrar and Mediation Server software installed.</span></span>

  - <span data-ttu-id="39b64-205">スタンドアロンの PSTN ゲートウェイ (Survivable Branch Appliance の一部ではない) とスタンドアロンの仲介サーバー。</span><span class="sxs-lookup"><span data-stu-id="39b64-205">A stand-alone PSTN gateway (not part of the Survivable Branch Appliance) and a stand-alone Mediation Server.</span></span>

<span data-ttu-id="39b64-206">Survivable ブランチサーバーの要件は、Lync Server 2013 サーバーの役割の要件と同じです。</span><span class="sxs-lookup"><span data-stu-id="39b64-206">The requirements for Survivable Branch Servers are the same as the requirements for any Lync Server 2013 server role.</span></span>

<span data-ttu-id="39b64-207"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="39b64-207"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

