---
title: 'Lync Server 2013: ハードウェアのセットアップ'
description: 'Lync Server 2013: ハードウェアのセットアップ。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hardware setup
ms:assetid: 37a9f295-cde3-4beb-9a6a-2580082798ab
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425852(v=OCS.15)
ms:contentKeyID: 48183834
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4e798ce32c1f89bba40ad9245426492b0489e7b4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427692"
---
# <a name="hardware-setup-for-lync-server-2013"></a><span data-ttu-id="b7720-103">Lync Server 2013 のハードウェアのセットアップ</span><span class="sxs-lookup"><span data-stu-id="b7720-103">Hardware setup for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b7720-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b7720-104">

<span> </span></span></span>

<span data-ttu-id="b7720-105">_**最終更新日:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="b7720-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="b7720-106">トポロジを実装するために必要なハードウェアおよびその他のコンポーネントをセットアップするには、トポロジビルダーでトポロジを公開する前に、次の操作を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="b7720-106">Setting up the hardware and other components required in the infrastructure that you need to implement your topology requires that, prior to publishing your topology in Topology Builder, you do the following:</span></span>

  - <span data-ttu-id="b7720-107">必要なすべてのコンピューター (必要に応じて、Lync Server 2013、データベースサーバー、インターネットインフォメーションサービス (IIS) を実行しているサーバー)、ネットワークアダプター、ハードウェアロードバランサー、ストレージデバイス (ファイルサーバーなど) など、トポロジ設計の各コンポーネントのハードウェアをインストールします。</span><span class="sxs-lookup"><span data-stu-id="b7720-107">Install the hardware for each component in the topology design that you created and saved by using Topology Builder, including all required computers (servers running Lync Server 2013, database servers, servers running Internet Information Services (IIS), and reverse proxy servers, as appropriate), network adapters, hardware load balancers, and storage devices (such as file servers).</span></span> <span data-ttu-id="b7720-108">ネットワークアダプターの数と速度に関する推奨事項に従っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b7720-108">Confirm that you have followed the recommendations for the number and speed for network adapters.</span></span> <span data-ttu-id="b7720-109">ハードウェアロードバランサーを使用する場合は、Lync Server 2013 で使用するために、ベンダーから適切な情報が設定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b7720-109">If you will be using hardware load balancers, make sure that you have the proper information from the vendor to configure them for use with Lync Server 2013.</span></span> <span data-ttu-id="b7720-110">ファイルサーバーまたは他のサーバーを使用して、Lync Server に必要なファイル共有を保存する場合は、サーバーが使用可能であり、ファイル共有を構成する準備ができていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b7720-110">If you will be using a file server or other server to house the file share required by Lync Server, make sure that the server is available and ready for the configuration of the file share.</span></span> <span data-ttu-id="b7720-111">展開に必要なコンポーネントを指定するトポロジの定義方法について詳しくは、「 [Lync Server 2013 でトポロジを定義して構成](lync-server-2013-defining-and-configuring-the-topology.md)する」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="b7720-111">For details about how to define a topology that specifies the components needed for your deployment, see [Defining and configuring the topology in Lync Server 2013](lync-server-2013-defining-and-configuring-the-topology.md).</span></span> <span data-ttu-id="b7720-112">サーバーのハードウェア要件の詳細については、サポートされているドキュメントで「 [Lync Server 2013 に](lync-server-2013-supported-hardware.md) 対応したハードウェア」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b7720-112">For details about hardware requirements for servers, see [Supported hardware for Lync Server 2013](lync-server-2013-supported-hardware.md) in the Supportability documentation.</span></span>

  - <span data-ttu-id="b7720-113">ネットワークインフラストラクチャが要件を満たしていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b7720-113">Make sure that the networking infrastructure meets requirements.</span></span> <span data-ttu-id="b7720-114">詳細については、計画ドキュメントの「 [Lync Server 2013 のネットワークインフラストラクチャ要件](lync-server-2013-network-infrastructure-requirements.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b7720-114">For details, see [Network infrastructure requirements for Lync Server 2013](lync-server-2013-network-infrastructure-requirements.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="b7720-115">Active Directory ドメインサービスをセットアップします。</span><span class="sxs-lookup"><span data-stu-id="b7720-115">Set up Active Directory Domain Services.</span></span> <span data-ttu-id="b7720-116">Ad ds のセットアップには、ad ds の準備と、AD DS に展開するすべてのコンポーネントの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b7720-116">Setting up AD DS includes preparing AD DS and defining all components that you want to deploy in AD DS.</span></span> <span data-ttu-id="b7720-117">AD DS の準備について詳しくは、展開ドキュメントの「 [Lync Server 2013 用 Active Directory ドメインサービスの準備](lync-server-2013-preparing-active-directory-domain-services.md) 」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="b7720-117">For details about preparing AD DS, see [Preparing Active Directory Domain Services for Lync Server 2013](lync-server-2013-preparing-active-directory-domain-services.md) in the Deployment documentation.</span></span>

  - <span data-ttu-id="b7720-118">ファイル共有の作成に必要なアクセス許可を設定します。</span><span class="sxs-lookup"><span data-stu-id="b7720-118">Set up the required permissions for creating the file share.</span></span> <span data-ttu-id="b7720-119">Lync Server 2013 によるファイル共有を使用するためのアクセス許可は、トポロジの公開時にトポロジビルダーによって自動的に構成されます。</span><span class="sxs-lookup"><span data-stu-id="b7720-119">Permissions for use of file shares by Lync Server 2013 are automatically configured by Topology Builder when you publish your topology.</span></span> <span data-ttu-id="b7720-120">ただし、トポロジビルダーで必要なアクセス許可を構成するには、トポロジを公開するために使用されるユーザーアカウントで、ファイル共有に対してフルコントロール (読み取り/書き込み/変更) が必要です。</span><span class="sxs-lookup"><span data-stu-id="b7720-120">However, the user account used to publish the topology must have full control (read/write/modify) on the file share in order for Topology Builder to configure the required permissions.</span></span> <span data-ttu-id="b7720-121">トポロジビルダーの公開プロセス中にファイル共有を適切に管理できるようにするには、ユーザーがメンバーになっているユーザーまたはドメイングループを、ファイル共有があるコンピューターのローカル管理者グループのメンバーにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b7720-121">To make sure that the file share can be managed properly during the Topology Builder publishing process, the user or domain group that the user is a member of should be made a member of the local Administrators group on the machine where the file share is located.</span></span> <span data-ttu-id="b7720-122">マルチドメインシナリオでは、ドメインのユーザーまたはグループが、ファイル共有が配置されているドメイン B のコンピューターのローカル管理者グループのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="b7720-122">In a multi-domain scenario, Domain A user or group should be made a member of the local Administrators group on the machine in Domain B where the file share will be located.</span></span>
    
    <span data-ttu-id="b7720-123">分散ファイルシステム (DFS) でファイル共有を使用して更新する方法の詳細については、「 [Lync Server 2013 用にファイルストレージを構成](lync-server-2013-configure-dfs-file-storage.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b7720-123">For details about updating using file shares in a Distributed File System (DFS), see [Configure file storage for Lync Server 2013](lync-server-2013-configure-dfs-file-storage.md).</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="b7720-124">Lync Server 2013 用のファイル共有 (Enterprise Edition) は、フロントエンドサーバー上に配置することはできません。</span><span class="sxs-lookup"><span data-stu-id="b7720-124">The file share for Lync Server 2013, Enterprise Edition cannot be located on the Front End Server.</span></span>

    
    </div>

  - <span data-ttu-id="b7720-125">Web サービス用のハードウェアロードバランサーをインストールしてセットアップします。</span><span class="sxs-lookup"><span data-stu-id="b7720-125">Install and set up the hardware load balancer for Web Services.</span></span> <span data-ttu-id="b7720-126">ドメインネームシステム (DNS) 負荷分散が展開されている場合でも、これらのプールにはハードウェアロードバランサーを使用する必要があります。ただし、HTTP/HTTPS トラフィックに対してのみ必要です。</span><span class="sxs-lookup"><span data-stu-id="b7720-126">With Domain Name System (DNS) load balancing deployed, you still need to also use hardware load balancers for these pools, but only for HTTP/HTTPS traffic.</span></span> <span data-ttu-id="b7720-127">ハードウェアロードバランサーは、ポート443および80経由のクライアントからの HTTPS トラフィックに使用されます。</span><span class="sxs-lookup"><span data-stu-id="b7720-127">The hardware load balancer is used for HTTPS traffic from clients over ports 443 and 80.</span></span> <span data-ttu-id="b7720-128">ただし、これらのプールについては、ハードウェアロードバランサーが必要ですが、これらの設定と管理は主に HTTP/HTTPS トラフィック用であり、ハードウェアロードバランサーの管理者は使い慣れています。</span><span class="sxs-lookup"><span data-stu-id="b7720-128">Although you still need hardware load balancers for these pools, their setup and administration will be primarily for HTTP/HTTPS traffic, which the administrators of the hardware load balancers are accustomed to.</span></span>

<span data-ttu-id="b7720-129">このトピックで説明したすべての準備作業を完了した後で、トポロジを公開する前に、次のことも行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="b7720-129">After you complete all of the preparation tasks as described in this topic, but prior to publishing the topology, you also need to:</span></span>

  - [<span data-ttu-id="b7720-130">Lync Server 2013 のオペレーティング システムと必要なソフトウェアのサーバーへのインストール</span><span class="sxs-lookup"><span data-stu-id="b7720-130">Install operating systems and prerequisite software on servers for Lync Server 2013</span></span>](lync-server-2013-install-operating-systems-and-prerequisite-software-on-servers.md)

  - [<span data-ttu-id="b7720-131">Lync Server 2013 での IIS の構成</span><span class="sxs-lookup"><span data-stu-id="b7720-131">Configure IIS for Lync Server 2013</span></span>](lync-server-2013-configure-iis.md)

  - [<span data-ttu-id="b7720-132">Lync Server 2013 用 SQL Server の構成</span><span class="sxs-lookup"><span data-stu-id="b7720-132">Configure SQL Server for Lync Server 2013</span></span>](lync-server-2013-configure-sql-server-for-lync-server.md)

  - [<span data-ttu-id="b7720-133">Lync Server 2013 でのフロント エンド プールまたは Standard Edition サーバー用の DNS レコードの構成</span><span class="sxs-lookup"><span data-stu-id="b7720-133">Configure DNS records in Lync Server 2013 for a Front End pool or Standard Edition server</span></span>](lync-server-2013-configure-dns-records-for-a-front-end-pool-or-standard-edition-server.md)

<span data-ttu-id="b7720-134"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b7720-134"></div>

<span> </span>

</div>

</div>

</span></span></div>

