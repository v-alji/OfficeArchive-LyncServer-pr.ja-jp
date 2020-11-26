---
title: 'Lync Server 2013: データベースのセキュリティ強化および保護'
description: 'Lync Server 2013: データベースのセキュリティを強化し、保護します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hardening and protecting the databases of Lync Server 2013
ms:assetid: 6953e721-3511-4235-b848-51bab093dc89
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn518330(v=OCS.15)
ms:contentKeyID: 62625490
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: af1ed8f54384e8ecac3b1e4ce6a4253a10bcc2c6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427762"
---
# <a name="hardening-and-protecting-the-databases-of-lync-server-2013"></a><span data-ttu-id="b180a-103">Lync Server 2013 のデータベースのセキュリティ強化および保護</span><span class="sxs-lookup"><span data-stu-id="b180a-103">Hardening and protecting the databases of Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b180a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b180a-104">

<span> </span></span></span>

<span data-ttu-id="b180a-105">_**最終更新日:** 2013-12-05_</span><span class="sxs-lookup"><span data-stu-id="b180a-105">_**Topic Last Modified:** 2013-12-05_</span></span>

<span data-ttu-id="b180a-106">Microsoft Lync Server 2013 は、ユーザー情報、会議の状態、アーカイブデータ、および通話詳細レコード (CDRs) を保存するための SQL Server データベースにも依存しています。</span><span class="sxs-lookup"><span data-stu-id="b180a-106">Microsoft Lync Server 2013 also depends on SQL Server databases for storing user information, conference state, archiving data, and Call Detail Records (CDRs).</span></span> <span data-ttu-id="b180a-107">Lync server 2013 データを Lync Server のバックエンドデータベースで最大限に活用するには、フォールトトレランスを向上させてトラブルシューティングを簡素化する方法でアプリケーションデータを区分することができます。</span><span class="sxs-lookup"><span data-stu-id="b180a-107">You can maximize the availability of Lync Server 2013 data on Lync Server back-end databases, by partitioning the application data in a way that improves fault tolerance and simplifies troubleshooting.</span></span> <span data-ttu-id="b180a-108">これらの目標を達成するには、次の方法でアプリケーションデータをパーティションに分割します。</span><span class="sxs-lookup"><span data-stu-id="b180a-108">To achieve these goals, partition the application data by:</span></span>

  - <span data-ttu-id="b180a-109">**サーバーのパーティション分割のベストプラクティスを使用する**   オペレーティングシステムファイル、アプリケーションファイル、プログラムファイルをデータファイルから分離します。</span><span class="sxs-lookup"><span data-stu-id="b180a-109">**Using server partitioning best practices**   Separate your operating system, application, and program files from your data files.</span></span>

  - <span data-ttu-id="b180a-110">**トランザクションログファイルとデータベースファイルを保存**   する  フォールトトレランスを強化して回復を最適化し、暗号化されたディスクまたはボリュームに保存するには、これらのファイルを個別に保存します。</span><span class="sxs-lookup"><span data-stu-id="b180a-110">**Storing transaction log files and database files**   Store these files separately to increase fault tolerance and optimize recovery, and store them on an encrypted disk or volume.</span></span>

  - <span data-ttu-id="b180a-111">**サーバークラスタリングの使用**   バックエンドサーバーをクラスター化して、Lync Server 2013 システムの可用性を最適化します。</span><span class="sxs-lookup"><span data-stu-id="b180a-111">**Using server clustering**   Cluster the back-end servers to optimize Lync Server 2013 system availability.</span></span>

  - <span data-ttu-id="b180a-112">**すべてのデータバックアップが暗号化され、適切に処理されるようにする**   紛失、廃棄、または紛失したバックアップメディアが、Lync Server 2013 展開のデータセキュリティに大きな脅威をもたらす可能性がある</span><span class="sxs-lookup"><span data-stu-id="b180a-112">**Ensure that all data backups are encrypted and properly handled**   Lost, discarded, or misplaced backup media can pose a significant threat to data security for Lync Server 2013 deployments</span></span>

<span data-ttu-id="b180a-113">Standard Edition server 以外の Lync Server 2013 サーバーでは、SQL Server Express インスタンス (RTCLOCAL インスタンス) にリモートからアクセスすることはできません。また、Standard Edition サーバー上の SQL Server Express を除き、ローカルのファイアウォール例外は作成されません。</span><span class="sxs-lookup"><span data-stu-id="b180a-113">On any Lync Server 2013 server except Standard Edition server, the SQL Server Express instance (RTCLOCAL instance) is not remotely accessible, and no local firewall exceptions are created, except for SQL Server Express on a Standard Edition server.</span></span> <span data-ttu-id="b180a-114">Standard Edition サーバーでは、バックエンドデータベースと中央管理ストア (CMS) の両方が、リモートでアクセスできるように設定されています。</span><span class="sxs-lookup"><span data-stu-id="b180a-114">On a Standard Edition server, both the back-end database and the Central Management store (CMS) are set up to be remotely accessible.</span></span> <span data-ttu-id="b180a-115">SQL Server データベースを強化するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="b180a-115">To harden SQL Server databases, you can do the following:</span></span>

  - <span data-ttu-id="b180a-116">Standard Edition サーバーの SQL Server Express ファイアウォールをカスタマイズして、データベースにリモートアクセスできるサーバーの範囲を制限します。</span><span class="sxs-lookup"><span data-stu-id="b180a-116">Customize the SQL Server Express firewall on Standard Edition servers, limiting the scope of servers that can remotely access the database.</span></span> <span data-ttu-id="b180a-117">既定では、すべての IP アドレスでデータベースにリモートアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="b180a-117">By default, any IP address can remotely access the database.</span></span>

  - <span data-ttu-id="b180a-118">Sql server 構成マネージャーを使用して、SQL Server リモートアクセスのプロトコル、IP アドレス、ポートを指定します。</span><span class="sxs-lookup"><span data-stu-id="b180a-118">Use SQL Server Configuration Manager to specify the protocols, IP addresses, and ports for SQL Server remote access:</span></span>
    
      - <span data-ttu-id="b180a-119">Lync Server 2013 は、TCP/IP プロトコルを使います。</span><span class="sxs-lookup"><span data-stu-id="b180a-119">Lync Server 2013 uses the TCP/IP protocol.</span></span> <span data-ttu-id="b180a-120">IP バージョン 4 (IPv4) をサポートしますが、IP バージョン 6 (IPv6) ではサポートされません。</span><span class="sxs-lookup"><span data-stu-id="b180a-120">It supports IP version 4 (IPv4), but not IP version 6 (IPv6).</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="b180a-121">Lync Server 2013 は、デュアル IP スタックが有効になっているネットワークで機能することができます。</span><span class="sxs-lookup"><span data-stu-id="b180a-121">Lync Server 2013 can function in a network with dual IP stack enabled.</span></span>

        
        </div>
    
      - <span data-ttu-id="b180a-122">Lync Server 2013 は複数の IP アドレス (マルチホームネットワークのアドレスカード) をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="b180a-122">Lync Server 2013 supports multiple IP address (multi-homed network address cards).</span></span> <span data-ttu-id="b180a-123">SQL Server が特定の IP アドレス (個別のアドレスまたはサブネット) のみをリッスンするように指定し、特定のプロトコルのみを使用するように指定することができます。</span><span class="sxs-lookup"><span data-stu-id="b180a-123">You can specify that SQL Server listen only to specific IP addresses (individual address or by subnet) and only use specific protocols.</span></span>
    
      - <span data-ttu-id="b180a-124">Lync Server 2013 は、静的および動的な SQL Server のポートをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="b180a-124">Lync Server 2013 supports static and dynamic SQL Server ports.</span></span>

  - <span data-ttu-id="b180a-125">静的な (既定以外の) ポートで SQL Server を実行します。 SQL Server Browser は実行しないでください (クライアントにリスニングポートを報告することはできません)。</span><span class="sxs-lookup"><span data-stu-id="b180a-125">Run SQL Server on a static (non-default) port, and do not run SQL Server Browser (so it cannot report the listening port to the client).</span></span> <span data-ttu-id="b180a-126">これには、フロントエンドサーバー、監視サーバー、アーカイブサーバー、管理コンソール (Lync Server 管理シェル、Lync Server コントロールパネル、またはトポロジビルダーを実行する)、および Lync Server データベースを実行している他のすべてのサーバーを含む、各 SQL Server クライアントのカスタム構成が必要です。</span><span class="sxs-lookup"><span data-stu-id="b180a-126">This requires a custom configuration on each SQL Server client, including Front End Servers, Monitoring Server, Archiving Server, and administrative consoles (running Lync Server Management Shell, Lync Server Control Panel, or Topology Builder), and all other servers running Lync Server databases).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b180a-127">データベースへのアクセスは、信頼できるデータベース管理者に制限されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b180a-127">Access to databases must be limited to trusted database administrators.</span></span> <span data-ttu-id="b180a-128">悪意のあるデータベース管理者が、Lync server 2013 サーバーに対する直接のアクセスや管理を許可されていない場合でも、データベースにデータを挿入または変更して、Lync Server 2013 サーバー経由の権限を取得したり、サービスから機密情報を取得したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="b180a-128">A malicious database administrator could insert or modify data into the databases to acquire privileges over the Lync Server 2013 servers or obtain sensitive information from the services, even if the database administrator has not been granted direct access or control of the Lync Server 2013 servers.</span></span>



</div>

<span data-ttu-id="b180a-129">カスタム構成と SQL Server データベースの強化の詳細については、「NextHop ブログの記事「カスタム SQL Server ネットワーク構成での Lync Server 2010 の使用」を参照してください [https://go.microsoft.com/fwlink/p/?LinkId=214008](https://go.microsoft.com/fwlink/p/?linkid=214008) 。</span><span class="sxs-lookup"><span data-stu-id="b180a-129">For details about custom configurations and hardening SQL Server databases, see the NextHop blog article, "Using Lync Server 2010 with a Custom SQL Server Network Configuration," at [https://go.microsoft.com/fwlink/p/?LinkId=214008](https://go.microsoft.com/fwlink/p/?linkid=214008).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b180a-130">オペレーティングシステムやアプリケーションサーバーを強化することもできます。また、グループポリシーを使用して、Lync Server の展開にセキュリティ lockdowns を実装することもできます。</span><span class="sxs-lookup"><span data-stu-id="b180a-130">You can also harden operating systems and applications servers, and you can use Group Policy to implement security lockdowns in your Lync Server deployment.</span></span> <span data-ttu-id="b180a-131">詳細については、「 <A href="lync-server-2013-hardening-and-protecting-servers-and-applications.md">Lync Server 2013 用のサーバーとアプリケーションの強化と保護</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b180a-131">For details, see <A href="lync-server-2013-hardening-and-protecting-servers-and-applications.md">Hardening and protecting servers and applications for Lync Server 2013</A>.</span></span>



<span data-ttu-id="b180a-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b180a-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

