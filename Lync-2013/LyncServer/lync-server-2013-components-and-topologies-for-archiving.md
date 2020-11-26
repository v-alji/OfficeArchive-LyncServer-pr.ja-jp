---
title: 'Lync Server 2013: アーカイブ用のコンポーネントとトポロジ'
description: 'Lync Server 2013: アーカイブ用のコンポーネントとトポロジ。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components and topologies for Archiving
ms:assetid: 5893063d-a44a-4034-aba9-cbe883ecf710
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204916(v=OCS.15)
ms:contentKeyID: 48184213
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f6ccb62993dc6a8dbc098d4a9c5f28b9b3f7fac9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434614"
---
# <a name="components-and-topologies-for-archiving-in-lync-server-2013"></a><span data-ttu-id="01c97-103">Lync Server 2013 のアーカイブ用のコンポーネントとトポロジ</span><span class="sxs-lookup"><span data-stu-id="01c97-103">Components and topologies for Archiving in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="01c97-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="01c97-104">

<span> </span></span></span>

<span data-ttu-id="01c97-105">_**最終更新日:** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="01c97-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="01c97-106">Lync Server 2013 IM と会議のコンテンツをアーカイブする場合は、Lync Server でアーカイブを実装できます。</span><span class="sxs-lookup"><span data-stu-id="01c97-106">If you want to archive Lync Server 2013 IM and conferencing content, you can implement Archiving in Lync Server.</span></span>

<div>

## <a name="archiving-components"></a><span data-ttu-id="01c97-107">アーカイブコンポーネント</span><span class="sxs-lookup"><span data-stu-id="01c97-107">Archiving Components</span></span>

<span data-ttu-id="01c97-108">アーカイブ機能には、次のコンポーネントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="01c97-108">The Archiving feature includes the following components:</span></span>

  - <span data-ttu-id="01c97-109">**アーカイブ エージェント**。</span><span class="sxs-lookup"><span data-stu-id="01c97-109">**Archiving agents**.</span></span> <span data-ttu-id="01c97-110">アーカイブエージェント (統合データ収集エージェントとも呼ばれます) は、すべてのフロントエンドプールおよび標準エディションのサーバーに自動的にインストールされ、ライセンス認証されます。</span><span class="sxs-lookup"><span data-stu-id="01c97-110">Archiving agents (also known as unified data collection agents) are installed and activated automatically on every Front End pool and Standard Edition server.</span></span> <span data-ttu-id="01c97-111">アーカイブエージェントは自動的に有効になりますが、アーカイブが有効になって適切に構成されるまで、実際にはメッセージはキャプチャされません。</span><span class="sxs-lookup"><span data-stu-id="01c97-111">Although archiving agents are activated automatically, no messages are actually captured until Archiving is enabled and appropriately configured.</span></span>

  - <span data-ttu-id="01c97-112">**データストレージのアーカイブ**。</span><span class="sxs-lookup"><span data-stu-id="01c97-112">**Archiving data storage**.</span></span> <span data-ttu-id="01c97-113">Lync Server 2013 用のデータストレージは、次のいずれかにすることができます。</span><span class="sxs-lookup"><span data-stu-id="01c97-113">Data storage for Lync Server 2013 can be either of the following:</span></span>
    
      - <span data-ttu-id="01c97-114">Exchange 2013 ストレージ。</span><span class="sxs-lookup"><span data-stu-id="01c97-114">Exchange 2013 storage.</span></span> <span data-ttu-id="01c97-115">Microsoft Exchange 統合オプションを有効にしている場合、Exchange 2013 サーバー上にあるユーザーのメールボックスでは、アーカイブデータに Exchange 2013 ストレージが使用されます。ただし、メールボックスが In-Place 保留になっている場合に限ります。</span><span class="sxs-lookup"><span data-stu-id="01c97-115">If you enable the Microsoft Exchange integration option, user mailboxes homed on the Exchange 2013 server use Exchange 2013 storage for archived data, but only if the mailboxes have been put on In-Place Hold.</span></span>
    
      - <span data-ttu-id="01c97-116">SQL Server ストレージ。</span><span class="sxs-lookup"><span data-stu-id="01c97-116">SQL Server storage.</span></span> <span data-ttu-id="01c97-117">組織内のユーザーが Lync Server 2013 を使っている場合は、サポートされているバージョンの SQL Server を実行するアーカイブデータベースをセットアップして、それらのユーザーのアーカイブを有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="01c97-117">If you have users in your deployment who are homed on Lync Server 2013, you can set up Archiving databases that run a supported version of SQL Server to enable archiving for those users.</span></span>

<span data-ttu-id="01c97-118">アーカイブにもファイルストレージが必要ですが、アーカイブでは、フロントエンドサーバーまたは Standard Edition サーバーと同じファイルストレージが使用されます。</span><span class="sxs-lookup"><span data-stu-id="01c97-118">Archiving also requires file storage, but Archiving uses the same file storage as the Front End Servers or Standard Edition server.</span></span>

<span data-ttu-id="01c97-119">アーカイブのためのハードウェアとソフトウェアの要件の一覧については、 [サポートされているハードウェア (Lync server 2013](lync-server-2013-supported-hardware.md) および [サーバーソフトウェアおよびサーバーソフトウェアと](lync-server-2013-server-software-and-infrastructure-support.md) 、サポートされているドキュメントの「サーバーソフトウェアとインフラストラクチャの2013サポート)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="01c97-119">For a list of hardware and software requirements for Archiving, see [Supported hardware for Lync Server 2013](lync-server-2013-supported-hardware.md) and [Server software and infrastructure support in Lync Server 2013](lync-server-2013-server-software-and-infrastructure-support.md) in the Supportability documentation.</span></span>

</div>

<div>

## <a name="supported-topologies"></a><span data-ttu-id="01c97-120">サポートされるトポロジ</span><span class="sxs-lookup"><span data-stu-id="01c97-120">Supported Topologies</span></span>

<span data-ttu-id="01c97-121">アーカイブサポートが必要なユーザーがいる各プールにアーカイブを展開します。</span><span class="sxs-lookup"><span data-stu-id="01c97-121">You deploy Archiving in each pool that has users that require archiving support.</span></span> <span data-ttu-id="01c97-122">アーカイブは、Enterprise Edition プールのフロントエンドサーバーと Standard Edition サーバー上で実行されます。</span><span class="sxs-lookup"><span data-stu-id="01c97-122">Archiving runs on Front End Servers in Enterprise Edition pools and on Standard Edition servers.</span></span> <span data-ttu-id="01c97-123">データ記憶域のアーカイブは、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="01c97-123">Archiving data storage can be the following:</span></span>

  - <span data-ttu-id="01c97-124">Exchange 2013 ストレージとの統合</span><span class="sxs-lookup"><span data-stu-id="01c97-124">Integrated with Exchange 2013 storage</span></span>

  - <span data-ttu-id="01c97-125">個別の SQL Server データベースを使用して展開する</span><span class="sxs-lookup"><span data-stu-id="01c97-125">Deployed using separate SQL Server databases</span></span>

<span data-ttu-id="01c97-126">使用している Exchange 2013 の展開に Lync Server の展開に関するすべてのユーザーが含まれていない場合は、Exchange 2013 サーバー上のメールボックスを使用しているユーザーに対して Microsoft Exchange 統合を使用する必要があります。また、他のすべての Lync ユーザーがアーカイブ用に使用する別の SQL Server データベースを展開する必要があります</span><span class="sxs-lookup"><span data-stu-id="01c97-126">If your Exchange 2013 deployment does not include all users in your Lync Server deployment, you must use Microsoft Exchange integration for the users whose mailboxes are home on Exchange 2013 servers, and you must deploy separate SQL Server databases for all other Lync users to use for archiving.</span></span>

</div>

<div>

## <a name="supported-collocation"></a><span data-ttu-id="01c97-127">サポートされている Collocation</span><span class="sxs-lookup"><span data-stu-id="01c97-127">Supported Collocation</span></span>

<span data-ttu-id="01c97-128">Lync Server 2013 は、さまざまな collocation シナリオをサポートしており、1台のサーバーに複数のコンポーネントを実行して (小規模組織の場合)、または異なるサーバーで個別のコンポーネントを実行することにより、ハードウェアコストを節約することができます (スケーラビリティとパフォーマンスが必要な大規模組織の場合)。</span><span class="sxs-lookup"><span data-stu-id="01c97-128">Lync Server 2013 supports a variety of collocation scenarios, allowing you flexibility to save hardware costs by running multiple components on one server (if you have a small organization), or to run individual components on different servers (if you have a larger organization that needs scalability and performance).</span></span> <span data-ttu-id="01c97-129">コンポーネントを検索するかどうかを決定する前に、スケーラビリティの要因を考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="01c97-129">Scalability factors should certainly be considered before you decide whether to collocate components.</span></span>

<span data-ttu-id="01c97-130">アーカイブは、プールまたは Standard Edition サーバーのフロントエンドサーバーに展開されます。</span><span class="sxs-lookup"><span data-stu-id="01c97-130">Archiving is deployed on the Front End Servers of a pool or Standard Edition servers.</span></span> <span data-ttu-id="01c97-131">併置できるコンポーネントの詳細については、サポート対象ドキュメントの「 [Lync server 2013 でサポートされているサーバーの場所](lync-server-2013-supported-server-collocation.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="01c97-131">For details about components that can be collocated there, see [Supported server collocation in Lync Server 2013](lync-server-2013-supported-server-collocation.md) in the Supportability documentation.</span></span>

<span data-ttu-id="01c97-132">アーカイブ用に別の SQL Server データベースを使用している場合、またはストレージを Exchange 2013 ストレージと統合するのではなく、次のいずれかでアーカイブデータベースを検索することができます。</span><span class="sxs-lookup"><span data-stu-id="01c97-132">If you use separate SQL Server databases for Archiving, instead of or in addition to integrating storage with Exchange 2013 storage, you can collocate the Archiving database with any of the following:</span></span>

  - <span data-ttu-id="01c97-133">監視データベース</span><span class="sxs-lookup"><span data-stu-id="01c97-133">Monitoring database</span></span>

  - <span data-ttu-id="01c97-134">Enterprise Edition フロントエンド プールのバックエンド データベース</span><span class="sxs-lookup"><span data-stu-id="01c97-134">Back-end database of an Enterprise Edition Front End pool</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="01c97-p108">アーカイブ データベースをホストするサーバーでは、他のデータベースもホストできます。ただし、アーカイブ データベースと他のデータベースを併置することを考慮するときには、数名以上のユーザーのメッセージをアーカイブすると、アーカイブ データベースに必要なディスク領域が非常に大きくなる可能性があることに注意してください。そのため、アーカイブ データベースとバックエンド データベースを併置することはお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="01c97-p108">The server hosting the Archiving database can host other databases. However, when you consider collocating the Archiving database with other databases, be aware that if you are archiving the messages of more than a few users, the disk space needed by the Archiving database can grow very large. For this reason, we do not recommend collocating the Archiving database with the back-end database.</span></span>



</div>

<span data-ttu-id="01c97-138">監視データベース、バックエンドデータベース、またはこれら両方のデータベースの両方でアーカイブデータベースを検索する場合は、1つまたはすべてのデータベースに対して単一の SQL インスタンスを使用するか、データベースごとに個別の SQL インスタンスを使用できます。次の制限があります。</span><span class="sxs-lookup"><span data-stu-id="01c97-138">If you collocate the Archiving database with the Monitoring database, back-end database, or both of these databases, you can either use a single SQL instance for any or all of the databases, or you can use a separate SQL instance for each database, with the following limitation:</span></span>

  - <span data-ttu-id="01c97-139">各 SQL インスタンスには、1つのバックエンドデータベース、単一の監視データベース、単一のアーカイブデータベースのみを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="01c97-139">Each SQL instance can contain only a single back-end database, single Monitoring database, and single Archiving database.</span></span>

<span data-ttu-id="01c97-140">すべてのサーバーの役割とデータベースの collocation の詳細については、サポートドキュメントの「 [Lync server 2013 でサポートされているサーバーの場所](lync-server-2013-supported-server-collocation.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="01c97-140">For details about collocation of all server roles and databases, see [Supported server collocation in Lync Server 2013](lync-server-2013-supported-server-collocation.md) in the Supportability documentation.</span></span>

<span data-ttu-id="01c97-141"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="01c97-141"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

