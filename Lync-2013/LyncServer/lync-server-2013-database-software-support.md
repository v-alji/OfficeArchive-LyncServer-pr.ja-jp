---
title: 'Lync Server 2013: データベース ソフトウェアのサポート'
description: Lync Server 2013 データベースソフトウェアのサポート。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Database software support
ms:assetid: e05d0032-bbea-4e61-987d-d07b1c045fd5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398990(v=OCS.15)
ms:contentKeyID: 48185517
ms.date: 12/02/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1c5d7b44e5febc4123dbcdf7072b98fcfd004609
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431226"
---
# <a name="database-software-support-in-lync-server-2013"></a><span data-ttu-id="168d4-103">Lync Server 2013 でのデータベース ソフトウェアのサポート</span><span class="sxs-lookup"><span data-stu-id="168d4-103">Database software support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="168d4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="168d4-104">

<span> </span></span></span>

<span data-ttu-id="168d4-105">_**最終更新日:** 2014-12-01_</span><span class="sxs-lookup"><span data-stu-id="168d4-105">_**Topic Last Modified:** 2014-12-01_</span></span>

<span data-ttu-id="168d4-106">Lync Server 2013 では、次のデータベース管理システムがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="168d4-106">Lync Server 2013 supports the following database management systems:</span></span>

  - <span data-ttu-id="168d4-107">**フロントエンド プールのバックエンド データベース、アーカイブ データベース、監視データベース、グループ チャット データベース、およびグループ チャット コンプライアンス データベース**</span><span class="sxs-lookup"><span data-stu-id="168d4-107">**Back-end database of a Front End pool, Archiving database, Monitoring database, persistent chat database, and persistent chat compliance database**</span></span>
    
      - <span data-ttu-id="168d4-p101">Microsoft SQL Server 2008 R2 Enterprise データベース ソフトウェア (64 ビット版)。追加で最新のサービス パックを実行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="168d4-p101">Microsoft SQL Server 2008 R2 Enterprise database software (64-bit edition). Additionally running the latest service pack is recommended.</span></span>
    
      - <span data-ttu-id="168d4-p102">Microsoft SQL Server 2008 R2 Standard (64 ビット版)。追加で最新のサービス パックを実行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="168d4-p102">Microsoft SQL Server 2008 R2 Standard (64-bit edition). Additionally running the latest service pack is recommended.</span></span>
    
      - <span data-ttu-id="168d4-p103">Microsoft SQL Server 2012 Enterprise (64 ビット版)。追加で最新のサービス パックを実行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="168d4-p103">Microsoft SQL Server 2012 Enterprise (64-bit edition). Additionally running the latest service pack is recommended.</span></span>
    
      - <span data-ttu-id="168d4-p104">Microsoft SQL Server 2012 Standard (64 ビット版)。追加で最新のサービス パックを実行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="168d4-p104">Microsoft SQL Server 2012 Standard (64-bit edition). Additionally running the latest service pack is recommended.</span></span>

  - <span data-ttu-id="168d4-116">**Standard Edition server データベースとフロントエンドサーバーデータベース**</span><span class="sxs-lookup"><span data-stu-id="168d4-116">**Standard Edition server database and Front End Server databases**</span></span>
    
      - <span data-ttu-id="168d4-117">Microsoft SQL Server 2012 Express (64 ビット版)。</span><span class="sxs-lookup"><span data-stu-id="168d4-117">Microsoft SQL Server 2012 Express (64-bit edition).</span></span> <span data-ttu-id="168d4-118">追加で最新のサービス パックを実行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="168d4-118">Additionally running the latest service pack is recommended.</span></span>
        
        <span data-ttu-id="168d4-119">Microsoft は、フロントエンドサーバーと Standard Edition サーバーにおける Microsoft SQL Server の修正プログラムとアップグレードをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="168d4-119">We support the patching and upgrade of Microsoft SQL Server on Front End Servers and Standard Edition servers.</span></span> <span data-ttu-id="168d4-120">ただし、フロントエンドサーバーに対して何らかのアップグレードまたは更新プログラムを作成する場合は、クォーラム要件を考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="168d4-120">However, when you make any kind of upgrade or patch on Front End Servers, you must account for quorum requirements.</span></span> <span data-ttu-id="168d4-121">詳細については、「[Upgrade or update Front End Servers in Lync Server 2013](lync-server-2013-upgrade-or-update-front-end-servers.md)」および「[Topologies and components for Front End Servers, instant messaging, and presence in Lync Server 2013](lync-server-2013-topologies-and-components-for-front-end-servers-instant-messaging-and-presence.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="168d4-121">For more information, see [Upgrade or update Front End Servers in Lync Server 2013](lync-server-2013-upgrade-or-update-front-end-servers.md) and [Topologies and components for Front End Servers, instant messaging, and presence in Lync Server 2013](lync-server-2013-topologies-and-components-for-front-end-servers-instant-messaging-and-presence.md).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="168d4-122">Microsoft SQL Server 2012 Express (64 ビット版) は、Lync Server 2013 (各標準エディションサーバーおよび各フロントエンドサーバーサーバー上) によって自動的にインストールされます。</span><span class="sxs-lookup"><span data-stu-id="168d4-122">Microsoft SQL Server 2012 Express (64-bit edition) is automatically installed by Lync Server 2013 on each Standard Edition server and each Front End Server server.</span></span>

    
    </div>

<div>


> [!IMPORTANT]  
> <UL>
> <LI>
> <P><span data-ttu-id="168d4-123">Lync Server 2013 では、32ビット版の SQL Server はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="168d4-123">Lync Server 2013 does not support the 32-bit edition of SQL Server.</span></span> <span data-ttu-id="168d4-124">64 ビット版を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="168d4-124">You must use the 64-bit edition.</span></span></P>
> <LI>
> <P><span data-ttu-id="168d4-125">SQL Server Web edition と SQL Server Workgroup edition はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="168d4-125">SQL Server Web edition and SQL Server Workgroup edition are not supported.</span></span> <span data-ttu-id="168d4-126">Lync Server 2013 では使用できません。</span><span class="sxs-lookup"><span data-stu-id="168d4-126">You cannot use them with Lync Server 2013.</span></span></P>
> <LI>
> <P><span data-ttu-id="168d4-127">Lync Server 2013 では、ネイティブデータベースのミラーリングがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="168d4-127">Lync Server 2013 does support native database mirroring.</span></span></P>
> <LI>
> <P><span data-ttu-id="168d4-128">監視サーバーの役割を使用するには、SQL Server Reporting Services をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="168d4-128">To use the Monitoring Server role, you should install SQL Server Reporting Services.</span></span></P></LI></UL>



</div>

<span data-ttu-id="168d4-129">フロントエンドプールでは、バックエンドデータベースを単一の SQL Server コンピューターにすることができます。</span><span class="sxs-lookup"><span data-stu-id="168d4-129">In a Front End pool, the back-end database can be a single SQL Server computer.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="168d4-130">他のデータベースを使用して Lync Server データベースを作成する場合は、可用性とパフォーマンスに影響する可能性のあるすべての要素を評価することと、1つのノードに障害が発生した場合に、残りのノードがその読み込みを処理できることを確認することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="168d4-130">If you collocate Lync Server databases with other databases, we highly recommend assessing all factors that might affect availability and performance, as well as ensuring that, if one node fails, the remaining node can handle the load.</span></span> <span data-ttu-id="168d4-131">フェールオーバー機能を検証する場合は、すべてのフェールオーバー シナリオをテストすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="168d4-131">To verify failover capabilities, we recommend testing all failover scenarios.</span></span>



</div>

<div>

## <a name="using-sql-mirroring-and-sql-clustering"></a><span data-ttu-id="168d4-132">SQL ミラーリングと SQL クラスタリングの使用</span><span class="sxs-lookup"><span data-stu-id="168d4-132">Using SQL Mirroring and SQL Clustering</span></span>

<span data-ttu-id="168d4-133">Lync Server 2013 では、各 Lync Server データベースに対して SQL ミラーリングと SQL クラスタリングのいずれかがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="168d4-133">Lync Server 2013 supports the use of either SQL mirroring or SQL clustering for each Lync Server database.</span></span> <span data-ttu-id="168d4-134">Lync Server 2013 のトポロジビルダーツールを使用して、簡単に SQL ミラーリングを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="168d4-134">You can easily set up SQL mirroring with the Topology Builder tool in Lync Server 2013.</span></span> <span data-ttu-id="168d4-135">SQL フェールオーバー クラスタリングの場合、設定に SQL Server を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="168d4-135">For SQL failover clustering, you must use SQL Server for setup.</span></span>

<span data-ttu-id="168d4-136">Lync Server 2013 は、以前のバージョンの Lync Server からアップグレードしたから始めの展開や組織を含む、すべての展開で SQL ミラーリングと SQL クラスタリングのトポロジの両方をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="168d4-136">Lync Server 2013 supports both SQL mirroring and SQL clustering topologies for all deployments, including greenfield deployments and organizations that have upgraded from previous versions of Lync Server.</span></span>

<span data-ttu-id="168d4-p111">SQL クラスタリングのサポートは、アクティブ/パッシブ構成用です。パフォーマンス上の理由から、パッシブ ノードを他の SQL インスタンスと共有しないでください。</span><span class="sxs-lookup"><span data-stu-id="168d4-p111">SQL Clustering support is for an active/passive configuration. For performance reasons, the passive node should not be shared by any other SQL instance.</span></span>

<span data-ttu-id="168d4-139">次のサポートが含まれます。</span><span class="sxs-lookup"><span data-stu-id="168d4-139">The following support is included:</span></span>

  - <span data-ttu-id="168d4-140">以下の製品用の 2 ノードのフェールオーバー クラスタリング:</span><span class="sxs-lookup"><span data-stu-id="168d4-140">Two-node failover clustering for the following:</span></span>
    
      - <span data-ttu-id="168d4-p112">Microsoft SQL Server 2012 Standard (64 ビット版)。追加で最新のサービス パックを実行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="168d4-p112">Microsoft SQL Server 2012 Standard (64-bit edition). Additionally running the latest service pack is recommended.</span></span>
    
      - <span data-ttu-id="168d4-p113">Microsoft SQL Server 2008 R2 Standard (64 ビット版)。追加で最新のサービス パックを実行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="168d4-p113">Microsoft SQL Server 2008 R2 Standard (64-bit edition). Additionally running the latest service pack is recommended.</span></span>

  - <span data-ttu-id="168d4-145">以下の製品用の最大 16 ノードのフェールオーバー クラスタリング:</span><span class="sxs-lookup"><span data-stu-id="168d4-145">Up to sixteen-node failover clustering for the following:</span></span>
    
      - <span data-ttu-id="168d4-p114">Microsoft SQL Server 2012 Enterprise (64 ビット版)。追加で最新のサービス パックを実行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="168d4-p114">Microsoft SQL Server 2012 Enterprise (64-bit edition). Additionally running the latest service pack is recommended.</span></span>
    
      - <span data-ttu-id="168d4-p115">Microsoft SQL Server 2008 R2 Enterprise データベース ソフトウェア (64 ビット版)。追加で最新のサービス パックを実行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="168d4-p115">Microsoft SQL Server 2008 R2 Enterprise database software (64-bit edition). Additionally running the latest service pack is recommended.</span></span>

<span data-ttu-id="168d4-150">SQL のミラーリングの詳細については、「 [Lync Server 2013 のバックエンドサーバーの高可用性](lync-server-2013-back-end-server-high-availability.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="168d4-150">For more information about SQL mirroring, see [Back End Server high availability in Lync Server 2013](lync-server-2013-back-end-server-high-availability.md).</span></span> <span data-ttu-id="168d4-151">SQL クラスタリングの展開方法の詳細については、「 [Lync server 2013 用の Sql Server クラスタリングを構成](lync-server-2013-configure-sql-server-clustering.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="168d4-151">For details on how to deploy SQL clustering, see [Configure SQL Server clustering for Lync Server 2013](lync-server-2013-configure-sql-server-clustering.md).</span></span>

<span data-ttu-id="168d4-152">SQL Server 2012 のフェールオーバークラスタリングの詳細とベストプラクティスについては、を参照してください <https://technet.microsoft.com/library/hh231721.aspx> 。</span><span class="sxs-lookup"><span data-stu-id="168d4-152">For more information and best practices for failover clustering in SQL Server 2012, see <https://technet.microsoft.com/library/hh231721.aspx>.</span></span> <span data-ttu-id="168d4-153">SQL Server 2008 のフェールオーバークラスタリングについては、を参照してください <https://technet.microsoft.com/library/ms189134(v=sql.105).aspx> 。</span><span class="sxs-lookup"><span data-stu-id="168d4-153">For failover clustering in SQL Server 2008, see <https://technet.microsoft.com/library/ms189134(v=sql.105).aspx>.</span></span>

<span data-ttu-id="168d4-154"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="168d4-154"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

