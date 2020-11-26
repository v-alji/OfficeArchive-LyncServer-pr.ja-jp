---
title: 'Lync Server 2013: 常設チャット サーバーに必要なリソース'
description: 'Lync Server 2013: 常設チャットサーバーに必要なリソース'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Required resources
ms:assetid: bce50b95-f3c8-407e-963a-d8896ee77fbc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205211(v=OCS.15)
ms:contentKeyID: 48185255
ms.date: 02/05/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 18c81f0017428e4305e46fbcf5580a83af38accf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442708"
---
# <a name="required-resources-for-persistent-chat-server-in-lync-server-2013"></a><span data-ttu-id="06477-103">Lync Server 2013 の常設チャット サーバーに必要なリソース</span><span class="sxs-lookup"><span data-stu-id="06477-103">Required resources for Persistent Chat Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="06477-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="06477-104">

<span> </span></span></span>

<span data-ttu-id="06477-105">_**最終更新日:** 2016-02-05_</span><span class="sxs-lookup"><span data-stu-id="06477-105">_**Topic Last Modified:** 2016-02-05_</span></span>

<span data-ttu-id="06477-106">常設チャットサーバーの高可用性と障害回復には、通常、完全な操作に必要なもの以外に追加のリソースが必要です。</span><span class="sxs-lookup"><span data-stu-id="06477-106">High availability and disaster recovery for Persistent Chat Server requires additional resources beyond what is typically needed for full operation.</span></span> <span data-ttu-id="06477-107">高可用性と障害回復のために常設チャットサーバーを構成する前に、標準の常設チャットサーバー操作に必要なものに加えて、次のリソースがあることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="06477-107">Before configuring Persistent Chat Server for high availability and disaster recovery, ensure that you have the following resources in addition to what is required for standard Persistent Chat Server operation.</span></span> <span data-ttu-id="06477-108">その他の構成情報については、「 [Lync server 2013 での常設チャットサーバーの構成](lync-server-2013-configuring-persistent-chat-server.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="06477-108">For additional configuration information, see [Configuring Persistent Chat Server in Lync Server 2013](lync-server-2013-configuring-persistent-chat-server.md).</span></span>

  - <span data-ttu-id="06477-109">常設チャットサーバーサービスのホームフロントエンドが存在する同じ物理データセンターに、1つの専用データベースインスタンスがあります。</span><span class="sxs-lookup"><span data-stu-id="06477-109">One dedicated database instance located in the same physical data center in which the home front end of the Persistent Chat Server service is located.</span></span> <span data-ttu-id="06477-110">このデータベースは、プライマリ常設チャットデータベースの SQL Server mirror として機能します。</span><span class="sxs-lookup"><span data-stu-id="06477-110">This database will serve as the SQL Server mirror for the primary Persistent Chat database.</span></span> <span data-ttu-id="06477-111">必要に応じて、ミラーデータベースへの自動フェールオーバーが必要な場合は、ミラーリング監視として機能する追加の SQL Server を指定します。</span><span class="sxs-lookup"><span data-stu-id="06477-111">Optionally, designate an additional SQL Server to serve as the mirroring witness if you want an automated failover to the mirror database.</span></span>

  - <span data-ttu-id="06477-112">他の物理データ センターに存在する、1 つの専用データベース インスタンス。</span><span class="sxs-lookup"><span data-stu-id="06477-112">One dedicated database instance located in the other physical data center.</span></span> <span data-ttu-id="06477-113">このデータベースは、プライマリデータセンターのデータベースの SQL Server Log 配布セカンダリデータベースとして機能します。</span><span class="sxs-lookup"><span data-stu-id="06477-113">This database will serve as the SQL Server Log Shipping secondary database for the database in the primary data center.</span></span>

  - <span data-ttu-id="06477-114">セカンダリデータベースの SQL Server ミラーとして機能する1つの専用データベースインスタンス。</span><span class="sxs-lookup"><span data-stu-id="06477-114">One dedicated database instance to serve as the SQL Server mirror for the secondary database.</span></span> <span data-ttu-id="06477-115">必要に応じて、ミラーリング監視として追加の SQL Server をサーバーに指定します。</span><span class="sxs-lookup"><span data-stu-id="06477-115">Optionally, designate an additional SQL Server to server as the mirroring witness.</span></span> <span data-ttu-id="06477-116">どちらもセカンダリ データベースと同じ物理データ センターに存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="06477-116">Both of these must be located in the same physical data center as the secondary database.</span></span>

  - <span data-ttu-id="06477-117">常設チャットサーバーのコンプライアンスが有効になっている場合は、3つの専用データベースインスタンスが必要になります。</span><span class="sxs-lookup"><span data-stu-id="06477-117">If Persistent Chat Server compliance is enabled, an additional three dedicated database instances are required.</span></span> <span data-ttu-id="06477-118">これらの配布は、常設チャットデータベースで前に説明したものと同じです。</span><span class="sxs-lookup"><span data-stu-id="06477-118">Their distribution is the same as those previously outlined for the Persistent Chat database.</span></span> <span data-ttu-id="06477-119">コンプライアンスデータベースは、永続的なチャットデータベースと同じ SQL Server インスタンスを共有することはできますが、高可用性と障害回復にはスタンドアロンインスタンスをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="06477-119">While it is possible for the compliance database to share the same SQL Server instance as the Persistent Chat database, we recommend standalone instances for high availability and disaster recovery.</span></span>

  - <span data-ttu-id="06477-120">ファイル共有を作成し、SQL Server のログ配布トランザクションログに指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="06477-120">A file share must be created and designated for the SQL Server Log Shipping transaction logs.</span></span> <span data-ttu-id="06477-121">常設チャットデータベースを実行する両方のデータセンターにあるすべての SQL Server は、このファイル共有に対する読み取り/書き込みアクセス権を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="06477-121">All SQL Servers in both data centers that run Persistent Chat databases must have read/write access to this file share.</span></span> <span data-ttu-id="06477-122">この共有は、FileStore 役割の一部としては定義されません。</span><span class="sxs-lookup"><span data-stu-id="06477-122">This share is not defined as part of a FileStore role.</span></span>

  - <span data-ttu-id="06477-123">セカンダリデータベースサーバー上のファイル共有は、プライマリサーバーファイル共有からコピーした SQL Server トランザクションログの移動先フォルダーとして機能します。</span><span class="sxs-lookup"><span data-stu-id="06477-123">A file share on the secondary database server to serve as the destination folder for the SQL Server transaction logs that are copied from the primary server file share.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="06477-124">常設チャットサーバープール内のアクティブな常設チャットサーバーは、トポロジで定義された次ホップの Lync プールと同じタイムゾーンに存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="06477-124">Active Persistent Chat servers in a Persistent Chat Server pool MUST reside in the same time zone as the next hop Lync Pool defined in the topology.</span></span>



</div>

<span data-ttu-id="06477-125">次の図は、2つの異なるストレッチプールトポロジでの常設チャットサーバープール全体の構成方法の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="06477-125">The following figures provide examples about how the entire Persistent Chat Server pool can be configured in the two different stretched pool topologies:</span></span>

  - <span data-ttu-id="06477-126">帯域幅が高く、待機時間が短い場合、データセンターが地理的な位置にある場合は、常設チャットサーバープールが拡張されます。</span><span class="sxs-lookup"><span data-stu-id="06477-126">Stretched Persistent Chat Server pool when data centers are geo-located with high bandwidth/low latency.</span></span>

  - <span data-ttu-id="06477-127">データセンターが低帯域幅または長い待ち時間で配置されている場合は、常設チャットサーバープールが拡張されます。</span><span class="sxs-lookup"><span data-stu-id="06477-127">Stretched Persistent Chat Server pool when data centers are geo-located with low bandwidth/high latency.</span></span>

<span data-ttu-id="06477-128">次の図は、高帯域幅/低レイテンシでデータセンターが地理的に配置されている、ストレッチ型の常設チャットサーバープールトポロジを示しています。</span><span class="sxs-lookup"><span data-stu-id="06477-128">The following figure shows a stretched Persistent Chat Server pool topology where data centers are geo-located with high bandwidth/low latency.</span></span>

<span data-ttu-id="06477-129">**帯域幅が高く、待機時間が短い場合、データセンターが地理的な位置にある場合は、常設チャットサーバープールが拡張されます。**</span><span class="sxs-lookup"><span data-stu-id="06477-129">**Stretched Persistent Chat Server pool when data centers are geo-located with high bandwidth/low latency.**</span></span>

<span data-ttu-id="06477-130">![常設チャットサーバープール HBW 構成試験](images/JJ205211.55d10910-c824-41e6-bed2-08d13a2abd65(OCS.15).jpg "常設チャットサーバープール HBW 構成試験")</span><span class="sxs-lookup"><span data-stu-id="06477-130">![Persistent Chat Server pool HBW configuration exam](images/JJ205211.55d10910-c824-41e6-bed2-08d13a2abd65(OCS.15).jpg "Persistent Chat Server pool HBW configuration exam")</span></span>

<span data-ttu-id="06477-131">次の図は、帯域幅が少なく、待機時間が長い、データセンターが地理的に配置されている、ストレッチ型の常設チャットサーバープールトポロジを示しています。</span><span class="sxs-lookup"><span data-stu-id="06477-131">The following figure shows a stretched Persistent Chat Server pool topology where data centers are geo-located with low bandwidth/high latency.</span></span>

<span data-ttu-id="06477-132">**データセンターが低帯域幅または長い待ち時間で配置されている場合は、常設チャットサーバープールが拡張されます。**</span><span class="sxs-lookup"><span data-stu-id="06477-132">**Stretched Persistent Chat Server pool when data centers are geo-located with low bandwidth/high latency.**</span></span>

<span data-ttu-id="06477-133">![常設チャットサーバープール LBW 構成試験](images/JJ205211.586b0a3a-3767-4991-944f-ee54389512aa(OCS.15).jpg "常設チャットサーバープール LBW 構成試験")</span><span class="sxs-lookup"><span data-stu-id="06477-133">![Persistent Chat Server pool LBW configuration exam](images/JJ205211.586b0a3a-3767-4991-944f-ee54389512aa(OCS.15).jpg "Persistent Chat Server pool LBW configuration exam")</span></span>

<span data-ttu-id="06477-134"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="06477-134"></div>

<span> </span>

</div>

</div>

</span></span></div>

