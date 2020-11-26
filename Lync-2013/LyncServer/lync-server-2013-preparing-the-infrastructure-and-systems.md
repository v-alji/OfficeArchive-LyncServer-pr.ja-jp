---
title: 'Lync Server 2013: インフラストラクチャとシステムの準備'
description: 'Lync Server 2013: インフラストラクチャとシステムの準備を行います。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing the infrastructure and systems
ms:assetid: 1254ee38-0679-4714-b293-1050f107c158
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398205(v=OCS.15)
ms:contentKeyID: 48183458
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bfabdda9d117af1534578c8543f9ce72808d5a53
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424101"
---
# <a name="preparing-the-infrastructure-and-systems-for-lync-server-2013"></a><span data-ttu-id="cd1cb-103">Lync Server 2013 のインフラストラクチャとシステムの準備</span><span class="sxs-lookup"><span data-stu-id="cd1cb-103">Preparing the infrastructure and systems for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cd1cb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cd1cb-104">

<span> </span></span></span>

<span data-ttu-id="cd1cb-105">_**最終更新日:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="cd1cb-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="cd1cb-106">Lync Server 2013 を展開するには、トポロジの設計を定義して公開するために、トポロジビルダーを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd1cb-106">Deployment of Lync Server 2013 requires the use of Topology Builder to define and publish the topology design.</span></span> <span data-ttu-id="cd1cb-107">トポロジに必要なコンポーネントを特定するには、トポロジビルダーを使用してトポロジの設計を作成し、保存します。</span><span class="sxs-lookup"><span data-stu-id="cd1cb-107">To identify the components required for your topology, you use Topology Builder to create and save a topology design.</span></span> <span data-ttu-id="cd1cb-108">トポロジビルダーでトポロジを公開する前に、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="cd1cb-108">Prior to publishing your topology in Topology Builder, you do the following:</span></span>

  - <span data-ttu-id="cd1cb-109">必要なすべてのコンピューター (必要に応じて、Lync Server 2013、データベースサーバー、インターネットインフォメーションサービス (IIS) を実行しているサーバー)、ネットワークアダプター、ハードウェアロードバランサー、ストレージデバイス (ファイルサーバーなど) など、トポロジ設計の各コンポーネントのハードウェアを入手してインストールします。</span><span class="sxs-lookup"><span data-stu-id="cd1cb-109">Acquire and install the hardware for each component in the topology design that you created and saved by using Topology Builder, including all required computers (servers running Lync Server 2013, database servers, servers running Internet Information Services (IIS), and reverse proxy servers, as appropriate), network adapters, hardware load balancers, and storage devices (such as file servers).</span></span> <span data-ttu-id="cd1cb-110">展開に必要なコンポーネントを指定するトポロジの定義方法について詳しくは、「 [Lync Server 2013 でトポロジを定義して構成](lync-server-2013-defining-and-configuring-the-topology.md)する」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="cd1cb-110">For details about how to define a topology that specifies the components needed for your deployment, see [Defining and configuring the topology in Lync Server 2013](lync-server-2013-defining-and-configuring-the-topology.md).</span></span> <span data-ttu-id="cd1cb-111">サーバーのハードウェア要件の詳細については、サポートされているドキュメントで「 [Lync Server 2013 に](lync-server-2013-supported-hardware.md) 対応したハードウェア」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cd1cb-111">For details about hardware requirements for servers, see [Supported hardware for Lync Server 2013](lync-server-2013-supported-hardware.md) in the Supportability documentation.</span></span>

  - <span data-ttu-id="cd1cb-112">ネットワークインフラストラクチャが要件を満たしていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="cd1cb-112">Make sure that the networking infrastructure meets requirements.</span></span> <span data-ttu-id="cd1cb-113">詳細については、計画ドキュメントの「 [Lync Server 2013 のネットワークインフラストラクチャ要件](lync-server-2013-network-infrastructure-requirements.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cd1cb-113">For details, see [Network infrastructure requirements for Lync Server 2013](lync-server-2013-network-infrastructure-requirements.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="cd1cb-114">Active Directory ドメインサービスをセットアップします。</span><span class="sxs-lookup"><span data-stu-id="cd1cb-114">Set up Active Directory Domain Services.</span></span> <span data-ttu-id="cd1cb-115">トポロジを公開して有効にするには、内部サーバーを AD DS のコンピューターアカウントで表す必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd1cb-115">To publish and enable the topology, you need the internal servers to be represented by computer accounts in AD DS.</span></span> <span data-ttu-id="cd1cb-116">これは、コンピューターを AD DS に結合することで実現されます。</span><span class="sxs-lookup"><span data-stu-id="cd1cb-116">This is accomplished by joining the computers to AD DS.</span></span> <span data-ttu-id="cd1cb-117">AD DS の準備の詳細については、「 [Lync Server 2013 用の Active Directory ドメインサービスの準備](lync-server-2013-preparing-active-directory-domain-services.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cd1cb-117">For details about preparing AD DS, see [Preparing Active Directory Domain Services for Lync Server 2013](lync-server-2013-preparing-active-directory-domain-services.md).</span></span>

  - <span data-ttu-id="cd1cb-118">ファイル共有を作成します。</span><span class="sxs-lookup"><span data-stu-id="cd1cb-118">Create a file share.</span></span> <span data-ttu-id="cd1cb-119">Standard Edition サーバーは、必要なファイルのファイル共有をホストできますが、エンタープライズ展開では、ファイル共有をフロントエンドサーバーでホストすることはできません。</span><span class="sxs-lookup"><span data-stu-id="cd1cb-119">Standard Edition servers can host the file share for the required file, while in an Enterprise deployment the file share cannot be hosted on the front end server.</span></span> <span data-ttu-id="cd1cb-120">フォルダーおよび共有に対してアクセス制御リスト (ACL) を展開して設定するために必要なアクセス許可とグループメンバーシップは、トポロジビルダーが正常に完了するために適切に設定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd1cb-120">The permissions and group memberships required for deploying and setting the access control list (ACL) on the folder and the share must be set correctly for Topology Builder to complete successfully.</span></span> <span data-ttu-id="cd1cb-121">Topology Builder を実行しているユーザーには、次の権限とグループメンバーシップがあることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd1cb-121">You should make sure that the person running Topology Builder has the following permissions and group memberships:</span></span>
    
      - <span data-ttu-id="cd1cb-122">ローカル管理者のメンバー</span><span class="sxs-lookup"><span data-stu-id="cd1cb-122">Member of Local Administrators</span></span>
    
      - <span data-ttu-id="cd1cb-123">ドメインユーザーのメンバー</span><span class="sxs-lookup"><span data-stu-id="cd1cb-123">Member of Domain Users</span></span>
    
      - <span data-ttu-id="cd1cb-124">ファイルストアの共有とフォルダーのフルコントロール</span><span class="sxs-lookup"><span data-stu-id="cd1cb-124">Full Control on share and folder of file store</span></span>

  - <span data-ttu-id="cd1cb-125">Enterprise Edition の場合、SQL Server をインストールして構成します。</span><span class="sxs-lookup"><span data-stu-id="cd1cb-125">For Enterprise Edition, install and configure SQL Server.</span></span> <span data-ttu-id="cd1cb-126">SQL Server のセットアップを完了するには、SQL Server ベースのサーバーがオンラインであり、トポロジを発行したユーザーが sql Server のローカル管理者であり、sql server インスタンスの SQL Server sysadmin グループのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd1cb-126">For SQL Server setup to succeed the SQL Server-based server must be online and the person publishing the topology be a local admin on the SQL Server and must be a member of the SQL Server sysadmin group on the SQL Server instance.</span></span>

<span data-ttu-id="cd1cb-127">このトピックで説明したすべての準備作業を完了した後で、トポロジを公開する前に、Windows オペレーティングシステムやその他の必須ソフトウェアのインストール、IIS のセットアップ、DNS の構成など、その他の準備作業も実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd1cb-127">After you complete all of the preparation tasks as described in this topic, but prior to publishing the topology, you also need to perform the other preparation tasks, including installing the Windows operating systems and other prerequisite software, setting up IIS, and configuring DNS.</span></span> <span data-ttu-id="cd1cb-128">これらのタスクの詳細については、「 [Lync server 2013 を実行しているサーバーのシステム要件](lync-server-2013-system-requirements-for-servers-running-lync-server-2013.md)」を参照してください。「lync [server 2013 用に IIS を構成する](lync-server-2013-configure-iis.md)」および「 [lync server 2013 用のインフラストラクチャとシステムの準備](lync-server-2013-preparing-the-infrastructure-and-systems.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cd1cb-128">For details about these tasks, see [System requirements for servers running Lync Server 2013](lync-server-2013-system-requirements-for-servers-running-lync-server-2013.md), [Configure IIS for Lync Server 2013](lync-server-2013-configure-iis.md), and [Preparing the infrastructure and systems for Lync Server 2013](lync-server-2013-preparing-the-infrastructure-and-systems.md).</span></span> <span data-ttu-id="cd1cb-129">さらに、クライアントとクライアントの要件について理解しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd1cb-129">Additionally, you should familiarize yourself with the clients and client requirements.</span></span> <span data-ttu-id="cd1cb-130">詳細については、「 [Lync Server 2013 でのクライアントとデバイスの展開](lync-server-2013-deploying-clients-and-devices.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cd1cb-130">For details, see [Deploying clients and devices in Lync Server 2013](lync-server-2013-deploying-clients-and-devices.md).</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="cd1cb-131">このセクション中</span><span class="sxs-lookup"><span data-stu-id="cd1cb-131">In This Section</span></span>

  - [<span data-ttu-id="cd1cb-132">Lync Server 2013 のハードウェアのセットアップ</span><span class="sxs-lookup"><span data-stu-id="cd1cb-132">Hardware setup for Lync Server 2013</span></span>](lync-server-2013-hardware-setup.md)

  - [<span data-ttu-id="cd1cb-133">Lync Server 2013 のソフトウェアのセットアップ</span><span class="sxs-lookup"><span data-stu-id="cd1cb-133">Software setup for Lync Server 2013</span></span>](lync-server-2013-software-setup.md)

  - [<span data-ttu-id="cd1cb-134">Lync Server 2013 用の Active Directory ドメイン サービスの準備</span><span class="sxs-lookup"><span data-stu-id="cd1cb-134">Preparing Active Directory Domain Services for Lync Server 2013</span></span>](lync-server-2013-preparing-active-directory-domain-services.md)

  - [<span data-ttu-id="cd1cb-135">Lync Server 2013 用 SQL Server の構成</span><span class="sxs-lookup"><span data-stu-id="cd1cb-135">Configure SQL Server for Lync Server 2013</span></span>](lync-server-2013-configure-sql-server-for-lync-server.md)

  - [<span data-ttu-id="cd1cb-136">Lync Server 2013 でのフロント エンド プールまたは Standard Edition サーバー用の DNS レコードの構成</span><span class="sxs-lookup"><span data-stu-id="cd1cb-136">Configure DNS records in Lync Server 2013 for a Front End pool or Standard Edition server</span></span>](lync-server-2013-configure-dns-records-for-a-front-end-pool-or-standard-edition-server.md)

  - [<span data-ttu-id="cd1cb-137">Lync Server 2013 管理ツールをインストールする</span><span class="sxs-lookup"><span data-stu-id="cd1cb-137">Install Lync Server 2013 administrative tools</span></span>](lync-server-2013-install-lync-server-administrative-tools.md)

<span data-ttu-id="cd1cb-138"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cd1cb-138"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

