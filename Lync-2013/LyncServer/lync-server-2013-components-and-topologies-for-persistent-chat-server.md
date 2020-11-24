---
title: 'Lync Server 2013: 常設チャットサーバー用のコンポーネントとトポロジ'
description: 'Lync Server 2013: 常設チャットサーバー用のコンポーネントとトポロジ。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components and topologies for Persistent Chat Server
ms:assetid: 6a0a14a0-baad-44e9-b26e-4d192c0a0e70
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398500(v=OCS.15)
ms:contentKeyID: 48184420
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 937b3d6f2716d9471e61cffd651847f6de9d83f1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398241"
---
# <a name="components-and-topologies-for-persistent-chat-server-in-lync-server-2013"></a><span data-ttu-id="03dd1-103">Lync Server 2013 の常設チャットサーバーのコンポーネントとトポロジ</span><span class="sxs-lookup"><span data-stu-id="03dd1-103">Components and topologies for Persistent Chat Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="03dd1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="03dd1-104">

<span> </span></span></span>

<span data-ttu-id="03dd1-105">_**最終更新日:** 2012-10-05_</span><span class="sxs-lookup"><span data-stu-id="03dd1-105">_**Topic Last Modified:** 2012-10-05_</span></span>

<span data-ttu-id="03dd1-106">常設チャットサーバーでは、単一サーバー構成と複数サーバー構成の両方がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="03dd1-106">Persistent Chat Server supports both single-server configurations and multiple-server configurations.</span></span> <span data-ttu-id="03dd1-107">常設チャットサーバーは、Lync Server 2013 Standard Edition サーバーでも実行できます。</span><span class="sxs-lookup"><span data-stu-id="03dd1-107">Persistent Chat Server can also run on a Lync Server 2013 Standard Edition server.</span></span> <span data-ttu-id="03dd1-108">これらの構成は、次の常設チャットサーバーのコンポーネントとトポロジで構成されています。</span><span class="sxs-lookup"><span data-stu-id="03dd1-108">These configurations consist of the following Persistent Chat Server components and topologies.</span></span>

<div>

## <a name="persistent-chat-server-components"></a><span data-ttu-id="03dd1-109">常設チャットサーバーコンポーネント</span><span class="sxs-lookup"><span data-stu-id="03dd1-109">Persistent Chat Server Components</span></span>

<span data-ttu-id="03dd1-110">最新バージョンの常設チャットサーバーをインストールするには、次のコンポーネントが必要です。</span><span class="sxs-lookup"><span data-stu-id="03dd1-110">Installing the latest version of Persistent Chat Server requires the following components:</span></span>

  - <span data-ttu-id="03dd1-111">常設チャットサーバーを実行していて、次のサービスを提供している1台以上のコンピューター。</span><span class="sxs-lookup"><span data-stu-id="03dd1-111">One or more computers running Persistent Chat Server and providing the following services:</span></span>
    
      - <span data-ttu-id="03dd1-112">常設チャットサービス</span><span class="sxs-lookup"><span data-stu-id="03dd1-112">Persistent Chat service</span></span>
    
      - <span data-ttu-id="03dd1-113">コンプライアンスが有効な場合にオンになるコンプライアンス サービス</span><span class="sxs-lookup"><span data-stu-id="03dd1-113">Compliance service, which is turned on if compliance is enabled</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="03dd1-114">Lync Server 2013 では、ファイルアップロード/ダウンロード用の常設チャット Web サービスが Lync Server 2013 フロントエンドサーバーと併置されました &nbsp; 。</span><span class="sxs-lookup"><span data-stu-id="03dd1-114">In Lync Server 2013, the Persistent Chat Web Services for File Upload/Download is now collocated with Lync Server 2013&nbsp;Front End Server.</span></span><BR><span data-ttu-id="03dd1-115">チャットルーム管理用の常設チャット Web サービスも、Lync Server 2013 フロントエンドサーバーと連携してい &nbsp; ます。</span><span class="sxs-lookup"><span data-stu-id="03dd1-115">The Persistent Chat Web Services for Chat Room Management is also collocated with Lync Server 2013&nbsp;Front End Server.</span></span>

    
    </div>

  - <span data-ttu-id="03dd1-116">サーバー (ミラーリングが使用されている場合は複数のサーバー)。チャットルームのコンテンツ、ルーム、カテゴリが保存されている常設チャットコンテンツデータベースをホストするための SQL Server バックエンドデータベースをホストしています。</span><span class="sxs-lookup"><span data-stu-id="03dd1-116">Server(s) (more than one server if mirroring is used) that host the SQL Server back-end database for hosting the Persistent Chat content database where chat room content, rooms, and categories are stored.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="03dd1-117">バックエンドデータベースには、作成されたカテゴリや常設チャットルームに関する情報など、チャット履歴データが格納されます。</span><span class="sxs-lookup"><span data-stu-id="03dd1-117">The back-end database stores chat history data, including information about categories and Persistent Chat rooms that are created.</span></span>

    
    </div>

  - <span data-ttu-id="03dd1-118">コンプライアンスが有効になっている場合は、常設チャットのコンプライアンスデータベースをホストするために SQL Server バックエンドデータベースをホストしているサーバー (1 つ以上のサーバーがミラーリングされている場合) で、コンプライアンスイベントと、コンプライアンスのためのチャットコンテンツが保存されています。</span><span class="sxs-lookup"><span data-stu-id="03dd1-118">If compliance was enabled, a server(s) (more than one server if mirroring is used) that host the SQL Server back-end database for hosting the Persistent Chat Compliance database, where compliance events and chat content for the purpose of compliance are stored.</span></span>

<span data-ttu-id="03dd1-119">別のコンピューター (管理コンソールなど) から常設チャットサーバーを管理するには、コンピューターの Lync Server コントロールパネルを使用します。</span><span class="sxs-lookup"><span data-stu-id="03dd1-119">To administer Persistent Chat Server from a separate computer (such as an administrative console), use the Lync Server Control Panel on the computer.</span></span> <span data-ttu-id="03dd1-120">このコンピューターは、フォレストルートに1つ以上のグローバルカタログサーバーがある Active Directory ドメインサービスドメインに展開されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="03dd1-120">This computer must then be deployed in an Active Directory Domain Services domain, with at least one global catalog server in the forest root.</span></span>

<span data-ttu-id="03dd1-121">常設チャットサーバーのハードウェアとソフトウェアの要件の詳細については、「 [lync server 2013 の常設チャットサーバーの技術要件](lync-server-2013-technical-requirements-for-persistent-chat-server.md)」および「lync [server 2013 でサポートされているハードウェア](lync-server-2013-supported-hardware.md)」および「 [サーバーのソフトウェアとインフラストラクチャの2013サポート](lync-server-2013-server-software-and-infrastructure-support.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="03dd1-121">For details about hardware and software requirements for Persistent Chat Server, see [Technical requirements for Persistent Chat Server in Lync Server 2013](lync-server-2013-technical-requirements-for-persistent-chat-server.md), [Supported hardware for Lync Server 2013](lync-server-2013-supported-hardware.md), and [Server software and infrastructure support in Lync Server 2013](lync-server-2013-server-software-and-infrastructure-support.md) in the Supportability documentation.</span></span>

</div>

<div>

## <a name="supported-collocation"></a><span data-ttu-id="03dd1-122">サポートされている Collocation</span><span class="sxs-lookup"><span data-stu-id="03dd1-122">Supported Collocation</span></span>

<span data-ttu-id="03dd1-123">Lync Server 2013 は、さまざまな collocation シナリオをサポートしており、1台のサーバーに複数のコンポーネントを実行して (小規模組織の場合)、または異なるサーバーで個別のコンポーネントを実行することにより、ハードウェアコストを節約することができます (スケーラビリティとパフォーマンスが必要な大規模組織の場合)。</span><span class="sxs-lookup"><span data-stu-id="03dd1-123">Lync Server 2013 supports a variety of collocation scenarios, providing you the flexibility to save hardware costs by running multiple components on one server (if you have a small organization), or to run individual components on different servers (if you have a larger organization that needs scalability and performance).</span></span> <span data-ttu-id="03dd1-124">コンポーネントを検索するかどうかを決定する前に、スケーラビリティの要因を考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="03dd1-124">Scalability factors should certainly be considered before you decide whether to collocate components.</span></span>

<span data-ttu-id="03dd1-125">コンプライアンスが有効になっている場合、常設チャットのコンプライアンスサービスは、Lync Server 2013 フロントエンドサーバーと関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="03dd1-125">The Persistent Chat Compliance service, if compliance is enabled, is collocated with the Lync Server 2013 Front End Server.</span></span>

<span data-ttu-id="03dd1-126">常設チャットサーバーは Standard Edition サーバーに展開できます。</span><span class="sxs-lookup"><span data-stu-id="03dd1-126">Persistent Chat Server can be deployed on the Standard Edition server.</span></span> <span data-ttu-id="03dd1-127">常設チャットサーバーバックエンドサーバーと常設チャットのコンプライアンスデータベースは、SQL Server Express バックエンドサーバーの Standard Edition サーバーに併置できます。</span><span class="sxs-lookup"><span data-stu-id="03dd1-127">The Persistent Chat Server Back End Server and the Persistent Chat Compliance database can be collocated on the Standard Edition server on the local SQL Server Express Back End Server.</span></span> <span data-ttu-id="03dd1-128">併置できるコンポーネントの詳細については、サポート対象ドキュメントの「 [Lync server 2013 でサポートされているサーバーの場所](lync-server-2013-supported-server-collocation.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="03dd1-128">For details about components that can be collocated there, see [Supported server collocation in Lync Server 2013](lync-server-2013-supported-server-collocation.md) in the Supportability documentation.</span></span>

<span data-ttu-id="03dd1-129">Lync Server 2013 Enterprise Edition では、常設チャットサーバーを Enterprise Edition サーバーに併置することはできません。</span><span class="sxs-lookup"><span data-stu-id="03dd1-129">For Lync Server 2013 Enterprise Edition, Persistent Chat Servers cannot be collocated on the Enterprise Edition server.</span></span> <span data-ttu-id="03dd1-130">常設チャットサーバー用の SQL Server データベースは、Enterprise Edition フロントエンドプールのバックエンドサーバーデータベースに併置できます。</span><span class="sxs-lookup"><span data-stu-id="03dd1-130">The SQL Server database for Persistent Chat Server can be collocated with the Back End Server database of an Enterprise Edition Front End pool.</span></span> <span data-ttu-id="03dd1-131">常設チャットのコンプライアンス用の SQL Server データベースは、Enterprise Edition プールのバックエンドサーバーデータベースと連携することもできます。</span><span class="sxs-lookup"><span data-stu-id="03dd1-131">The SQL Server database for Persistent Chat compliance can also be collocated with the Back End Server database of an Enterprise Edition pool.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="03dd1-132">常設チャットデータベースをホストしているサーバーは、他のデータベースをホストできます。</span><span class="sxs-lookup"><span data-stu-id="03dd1-132">The server hosting the Persistent Chat database can host other databases.</span></span> <span data-ttu-id="03dd1-133">ただし、他のデータベースとの間で永続的なチャットデータベースを検索することを検討している場合は、常設チャットデータベースに必要なディスク領域が非常に大きくなる可能性があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="03dd1-133">However, when you consider collocating the Persistent Chat database with other databases, be aware that if you are storing the messages of more than a few users, the disk space needed by the Persistent Chat database can grow very large.</span></span> <span data-ttu-id="03dd1-134">このため、バックエンドデータベースを使用して常設チャットデータベースを検索することはお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="03dd1-134">For this reason, we do not recommend collocating the Persistent Chat database with the back-end database.</span></span>



</div>

<span data-ttu-id="03dd1-135">バックエンドデータベースで永続的なチャットデータベースを検索する場合は、任意またはすべてのデータベースに対して SQL Server の1つのインスタンスを使うか、データベースごとに SQL Server の個別のインスタンスを使うことができます。次の制限があります。</span><span class="sxs-lookup"><span data-stu-id="03dd1-135">If you collocate the Persistent Chat database with the back-end database, you can either use a single instance of SQL Server for any or all of the databases, or you can use a separate instance of SQL Server for each database, with the following limitation:</span></span>

  - <span data-ttu-id="03dd1-136">SQL Server の各インスタンスには、1つのバックエンドデータベースと1つの常設チャットデータベースのみを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="03dd1-136">Each instance of SQL Server can contain only a single back-end database and a single Persistent Chat database.</span></span>

<span data-ttu-id="03dd1-137">すべてのサーバーの役割とデータベースの collocation の詳細については、サポートドキュメントの「 [Lync server 2013 でサポートされているサーバーの場所](lync-server-2013-supported-server-collocation.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="03dd1-137">For details about collocation of all server roles and databases, see [Supported server collocation in Lync Server 2013](lync-server-2013-supported-server-collocation.md) in the Supportability documentation.</span></span>

</div>

<div>

## <a name="persistent-chat-server-topologies"></a><span data-ttu-id="03dd1-138">常設チャットサーバーのトポロジ</span><span class="sxs-lookup"><span data-stu-id="03dd1-138">Persistent Chat Server Topologies</span></span>

<span data-ttu-id="03dd1-139">常設チャットサーバーでは、次のトポロジがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="03dd1-139">Persistent Chat Server supports the following topologies:</span></span>

  - <span data-ttu-id="03dd1-140">Lync Server 2013 Enterprise Edition single server 常設チャットサーバーフロントエンドサーバー</span><span class="sxs-lookup"><span data-stu-id="03dd1-140">Lync Server 2013 Enterprise Edition single server Persistent Chat Server Front End Server</span></span>

  - <span data-ttu-id="03dd1-141">Lync Server 2013 Enterprise Edition multiple server 常設チャットサーバーフロントエンドサーバー</span><span class="sxs-lookup"><span data-stu-id="03dd1-141">Lync Server 2013 Enterprise Edition multiple server Persistent Chat Server Front End Server</span></span>

  - <span data-ttu-id="03dd1-142">SQL Server Express を使用した Lync Server 2013 Standard Edition Server</span><span class="sxs-lookup"><span data-stu-id="03dd1-142">Lync Server 2013 Standard Edition server using SQL Server Express</span></span>

  - <span data-ttu-id="03dd1-143">Standard Edition server を使用して、別のサーバー上の Lync Server 2013 Standard Edition server と常設チャットサーバーが次ホップサーバーとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="03dd1-143">Lync Server 2013 Standard Edition server and Persistent Chat Server on a separate server using Standard Edition server as the next hop server.</span></span>

<span data-ttu-id="03dd1-144">[トポロジビルダーを使用して、常設チャットサーバーを Lync Server 2013 に追加することができます。</span><span class="sxs-lookup"><span data-stu-id="03dd1-144">You can add Persistent Chat Server to your Lync Server 2013 deployment by using Topology Builder.</span></span> <span data-ttu-id="03dd1-145">1台のサーバーまたは複数サーバーの常設チャットサーバープールをトポロジに追加することができます。</span><span class="sxs-lookup"><span data-stu-id="03dd1-145">You can add a single server or a multiple server Persistent Chat Server pool to your topology.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="03dd1-146">トポロジビルダーを使用して単一のサーバーで永続的なチャットサーバープールを作成した後は、そのプールにサーバーを追加することはできません。</span><span class="sxs-lookup"><span data-stu-id="03dd1-146">After you create a Persistent Chat Server pool with a single server by using Topology Builder, you cannot add additional servers to the pool.</span></span>



</div>

<div>

## <a name="single-server-topology"></a><span data-ttu-id="03dd1-147">Single-Server トポロジ</span><span class="sxs-lookup"><span data-stu-id="03dd1-147">Single-Server Topology</span></span>

<span data-ttu-id="03dd1-148">常設チャットサーバー向けの最小構成と最も簡単な展開は、1つの常設チャットサーバーのフロントエンドサーバートポロジです。</span><span class="sxs-lookup"><span data-stu-id="03dd1-148">The minimum configuration and simplest deployment for Persistent Chat Server is a single Persistent Chat Server Front End Server topology.</span></span> <span data-ttu-id="03dd1-149">この展開を行うには、常設チャットサーバーを実行する単一のサーバー (必要に応じてコンプライアンスサービスを実行します)、SQL Server データベースをホストしているサーバー、コンプライアンスが必要な場合は、コンプライアンスデータを格納する SQL Server データベースが必要です。</span><span class="sxs-lookup"><span data-stu-id="03dd1-149">This deployment requires a single server that runs Persistent Chat Server (which optionally runs the Compliance service, if compliance is enabled), a server that hosts both the SQL Server database, and if compliance is required, the SQL Server database to store the compliance data.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="03dd1-150">トポロジビルダーでシングルサーバー展開として開始された常設チャットサーバープールにサーバーを追加することはできません。</span><span class="sxs-lookup"><span data-stu-id="03dd1-150">You cannot add additional servers to a Persistent Chat Server pool that is started as a single-server deployment in Topology Builder.</span></span> <span data-ttu-id="03dd1-151">単一のサーバーを使用している場合でも、複数サーバープールトポロジを使用することをお勧めします。必要に応じて、後でサーバーを追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="03dd1-151">We recommend using the multiple-server pool topology, even if you’re using a single server, so that you can add more servers later, if needed..</span></span>



</div>

<span data-ttu-id="03dd1-152">次の図は、コンプライアンスを備えた単一の常設チャットサーバーフロントエンドサーバーのトポロジの必須コンポーネントとオプションコンポーネントをすべて示しています。</span><span class="sxs-lookup"><span data-stu-id="03dd1-152">The following figure shows all required and optional components of a topology for a single Persistent Chat Server Front End Server with compliance.</span></span>

<span data-ttu-id="03dd1-153">**1つの常設チャットサーバー**</span><span class="sxs-lookup"><span data-stu-id="03dd1-153">**Single Persistent Chat Server**</span></span>

<span data-ttu-id="03dd1-154">![コンプライアンスサービスを備えた単一サーバートポロジ](images/Gg398500.9168fa52-61e0-4d17-a14d-45fd32e81456(OCS.15).jpg "コンプライアンスサービスを備えた単一サーバートポロジ")</span><span class="sxs-lookup"><span data-stu-id="03dd1-154">![Single server topology with Compliance service](images/Gg398500.9168fa52-61e0-4d17-a14d-45fd32e81456(OCS.15).jpg "Single server topology with Compliance service")</span></span>

</div>

<div>

## <a name="multiple-server-topology"></a><span data-ttu-id="03dd1-155">Multiple-Server トポロジ</span><span class="sxs-lookup"><span data-stu-id="03dd1-155">Multiple-Server Topology</span></span>

<span data-ttu-id="03dd1-156">より多くの容量と信頼性を実現するには、「 [Lync server 2013 での常設チャットサーバーの計画](lync-server-2013-planning-for-persistent-chat-server.md)」で説明されているように、複数サーバートポロジを展開します。</span><span class="sxs-lookup"><span data-stu-id="03dd1-156">To provide greater capacity and reliability, you can deploy a multiple-server topology, as described in [Planning for Persistent Chat Server in Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md).</span></span> <span data-ttu-id="03dd1-157">複数サーバーのトポロジには、常設チャットサーバーを実行しているアクティブなコンピューターを4つまで含めることができます (高可用性および障害回復構成では最大8個まで可能)。ただし、4つはアクティブ、残りの4つはスタンバイ状態になります。</span><span class="sxs-lookup"><span data-stu-id="03dd1-157">The multiple-server topology can include as many as four active computers running Persistent Chat Server (high availability and disaster recovery configurations will allow up to eight, but only four can be active and the remaining four on standby).</span></span> <span data-ttu-id="03dd1-158">各サーバーは、最大で2万の同時ユーザーをサポートできます。合計で8万の同時使用ユーザーは、4台のサーバーで常設チャットサーバープールに接続されています。</span><span class="sxs-lookup"><span data-stu-id="03dd1-158">Each server can support as many as 20,000 concurrent users, for a total of 80,000 concurrent users connected to a Persistent Chat Server pool with 4 servers.</span></span> <span data-ttu-id="03dd1-159">複数サーバーのトポロジは、複数のサーバーが常設チャットサーバーをホストしていることを除いて、単一サーバートポロジと同じで、拡大縮小できます。</span><span class="sxs-lookup"><span data-stu-id="03dd1-159">A multiple-server topology is the same as the single-server topology except that multiple servers host Persistent Chat Server, and can scale higher.</span></span> <span data-ttu-id="03dd1-160">常設チャットサーバーを実行している複数のコンピューターは、Lync Server とコンプライアンスサービスと同じ Active Directory ドメインサービスドメインに存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="03dd1-160">Multiple computers running Persistent Chat Server should reside in the same Active Directory Domain Services domain as Lync Server and the Compliance service.</span></span>

<span data-ttu-id="03dd1-161">次の図は、常設チャットサーバーを実行している複数のコンピューター、オプションのコンプライアンスサービス、および別のコンプライアンスデータベースの複数サーバートポロジのすべてのコンポーネントを示しています。</span><span class="sxs-lookup"><span data-stu-id="03dd1-161">The following figure shows all the components of a multiple-server topology with multiple computers running Persistent Chat Server, the optional Compliance service, and a separate compliance database.</span></span>

<span data-ttu-id="03dd1-162">**複数の常設チャットサーバー**</span><span class="sxs-lookup"><span data-stu-id="03dd1-162">**Multiple Persistent Chat Servers**</span></span>

<span data-ttu-id="03dd1-163">![複数サーバートポロジ](images/Gg398500.19aea898-28df-4d9b-903c-f72ef062d919(OCS.15).jpg "複数サーバートポロジ")</span><span class="sxs-lookup"><span data-stu-id="03dd1-163">![Multiple server topology](images/Gg398500.19aea898-28df-4d9b-903c-f72ef062d919(OCS.15).jpg "Multiple server topology")</span></span>

<span data-ttu-id="03dd1-164">複数サーバー トポロジでは、サーバー機能をプールできます。</span><span class="sxs-lookup"><span data-stu-id="03dd1-164">Multiple-server topologies provide pooling of server functionality.</span></span> <span data-ttu-id="03dd1-165">サーバープールでは、常設チャットサービスはデータをやり取りして共有します。</span><span class="sxs-lookup"><span data-stu-id="03dd1-165">In a server pool, the Persistent Chat services communicate and share data.</span></span> <span data-ttu-id="03dd1-166">たとえば、1つの常設チャットサービスに最初に投稿されたチャット履歴は、システムの任意の常設チャットサービスから入手できます。</span><span class="sxs-lookup"><span data-stu-id="03dd1-166">For example, chat history that was originally posted to one Persistent Chat service is available from any Persistent Chat service in the system.</span></span> <span data-ttu-id="03dd1-167">1つの常設チャットサービスを通じてアップロードされたファイルには、任意の常設チャットサービスからアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="03dd1-167">A file that is uploaded through one Persistent Chat service can be accessed by any Persistent Chat service.</span></span> <span data-ttu-id="03dd1-168">ユーザーは、さまざまな常設チャットサーバーフロントエンドサーバーに接続することができ、チャットして互いに通信することができます。</span><span class="sxs-lookup"><span data-stu-id="03dd1-168">Users can be connected to different Persistent Chat Server Front End Servers and can be chatting and communicating with each other.</span></span>

<span data-ttu-id="03dd1-169">TCP 8011 の既定のポートはサーバープールにサーバーを接続し、常設チャットサービスで自分との通信や管理目的のために使用されます。</span><span class="sxs-lookup"><span data-stu-id="03dd1-169">The default port of TCP 8011 connects a server to a server pool, and is used by the Persistent Chat service to communicate between themselves, or for administrative purposes.</span></span>

<span data-ttu-id="03dd1-170"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="03dd1-170"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

