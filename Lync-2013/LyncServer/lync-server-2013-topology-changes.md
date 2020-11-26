---
title: 'Lync Server 2013: トポロジの変更'
description: Lync Server 2013 トポロジが変更します。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Topology changes
ms:assetid: 9e40ef93-9ab0-498c-9bbf-f94584353e53
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688153(v=OCS.15)
ms:contentKeyID: 49733756
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 562766eae939e4510a0d3af20e40b4731c361040
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436231"
---
# <a name="topology-changes-in-lync-server-2013"></a><span data-ttu-id="eae3f-103">Lync Server 2013 のトポロジの変更</span><span class="sxs-lookup"><span data-stu-id="eae3f-103">Topology changes in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="eae3f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="eae3f-104">

<span> </span></span></span>

<span data-ttu-id="eae3f-105">_**最終更新日:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="eae3f-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="eae3f-106">このセクションで説明するように、トポロジの要件と Lync Server 2013 に関する考慮事項は、以前のリリースとは異なります。</span><span class="sxs-lookup"><span data-stu-id="eae3f-106">Topology requirements and considerations for Lync Server 2013 are different from those for earlier releases, as described in this section.</span></span>

<div>

## <a name="new-front-end-pools-architecture"></a><span data-ttu-id="eae3f-107">新しいフロントエンドプールのアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="eae3f-107">New Front End Pools Architecture</span></span>

<span data-ttu-id="eae3f-108">Lync Server 2013 では、Enterprise Edition のフロントエンドプールのアーキテクチャが分散システムアーキテクチャに変更されています。</span><span class="sxs-lookup"><span data-stu-id="eae3f-108">In Lync Server 2013, the architecture of Enterprise Edition Front End pools has changed to a distributed systems architecture.</span></span>

<span data-ttu-id="eae3f-109">この新しいアーキテクチャでは、バックエンドデータベースはプール内のリアルタイムデータストアではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="eae3f-109">With this new architecture, the Back End database is no longer the real-time data store in a pool.</span></span> <span data-ttu-id="eae3f-110">特定のユーザーに関する情報は、プール内の3つのフロントエンドサーバー上に保持されます。</span><span class="sxs-lookup"><span data-stu-id="eae3f-110">Information about a particular user is kept on three Front End Servers in the pool.</span></span> <span data-ttu-id="eae3f-111">各ユーザーに対して、1つのフロントエンドサーバーがそのユーザーの情報のマスターとして機能し、他の2つのフロントエンドサーバーが複製として機能します。</span><span class="sxs-lookup"><span data-stu-id="eae3f-111">For each user, one Front End Server acts as the master for that user’s information, and two other Front End Servers serve as replicas.</span></span> <span data-ttu-id="eae3f-112">フロントエンドサーバーがダウンした場合、レプリカとして提供されている別のフロントエンドサーバーが自動的にマスターに昇格されます。</span><span class="sxs-lookup"><span data-stu-id="eae3f-112">If a Front End Server goes down, another Front End Server which served as a replica is automatically promoted to master.</span></span>

<span data-ttu-id="eae3f-113">これはバックグラウンドで行われるため、管理者はどのフロントエンドサーバーがどのユーザー用のマスターであるかを知る必要はありません。</span><span class="sxs-lookup"><span data-stu-id="eae3f-113">This happens behind the scenes, and administrators do not need to know which Front End Servers are the masters for which users.</span></span> <span data-ttu-id="eae3f-114">このデータ記憶域の配布によって、プール内のパフォーマンスとスケーラビリティが向上し、1つのバックエンドサーバーの1つの障害ポイントが排除されます。</span><span class="sxs-lookup"><span data-stu-id="eae3f-114">This distribution of data storage improves performance and scalability within the pool, and eliminates the single point of failure of a single Back End Server.</span></span>

<span data-ttu-id="eae3f-115">バックエンドサーバーは、ユーザーおよび会議データのバックアップストレージとして機能します。また、応答グループデータベースなど、他のデータベースのプライマリストレージでもあります。</span><span class="sxs-lookup"><span data-stu-id="eae3f-115">The Back End Server serves as backup storage for user and conference data, and is also the primary storage for other databases such as the Response Group database.</span></span>

<span data-ttu-id="eae3f-116">これらの改善により、プールの計画や管理方法が変更されることもあります。</span><span class="sxs-lookup"><span data-stu-id="eae3f-116">These improvements also mean there are changes in how you plan and maintain your pools.</span></span> <span data-ttu-id="eae3f-117">すべての Enterprise Edition のフロントエンドプールには、少なくとも3台のフロントエンドサーバーが含まれていることをお勧めします。これには、フロントエンドプールアーキテクチャが設計されているすべてのレプリカの数を指定します。</span><span class="sxs-lookup"><span data-stu-id="eae3f-117">We recommend that all your Enterprise Edition Front End pools include at least three Front End Servers, to provide the full number of replicas that the Front End pool architecture is designed for.</span></span> <span data-ttu-id="eae3f-118">また、フロントエンドプールにサーバーを追加するとき、サーバーからサーバーを削除するとき、またはサーバーをアップグレードするときに、特定の手順に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="eae3f-118">Additionally, you must follow certain procedures when adding servers to a Front End pool, removing servers from it, or upgrading servers.</span></span> <span data-ttu-id="eae3f-119">詳細については、「 [Lync Server 2013 のフロントエンドサーバー、インスタントメッセージング、およびプレゼンスのトポロジとコンポーネント」を](lync-server-2013-topologies-and-components-for-front-end-servers-instant-messaging-and-presence.md)参照してください。</span><span class="sxs-lookup"><span data-stu-id="eae3f-119">For more information, see [Topologies and components for Front End Servers, instant messaging, and presence in Lync Server 2013](lync-server-2013-topologies-and-components-for-front-end-servers-instant-messaging-and-presence.md).</span></span>

<div>

## <a name="server-role-topology-changes"></a><span data-ttu-id="eae3f-120">サーバーの役割のトポロジの変更</span><span class="sxs-lookup"><span data-stu-id="eae3f-120">Server Role Topology Changes</span></span>

<span data-ttu-id="eae3f-121">別のサーバー上で以前に実行した一部のサーバーの役割は、フロントエンドサーバーの役割に統合され、ハードウェアのコストを節約できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="eae3f-121">Some server roles that previously ran on separate servers are now consolidated into the Front End Server role, enabling you to save on hardware costs</span></span>

  - <span data-ttu-id="eae3f-122">Lync Server 2013 では、A/V 会議サーバーは、常にフロントエンドサーバーと連携しています。</span><span class="sxs-lookup"><span data-stu-id="eae3f-122">In Lync Server 2013, A/V Conferencing Server is always collocated with Front End Server.</span></span>

  - <span data-ttu-id="eae3f-123">監視とアーカイブの両方のフロントエンドが、常にフロントエンドサーバーと併置されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="eae3f-123">The front ends for both Monitoring and Archiving are now always collocated with Front End Server.</span></span> <span data-ttu-id="eae3f-124">監視とアーカイブを行うには、フロントエンドプールのバックエンドデータベースと同じサーバーに併置できる個別の Back-End データベースが必要です。または、別々の Back-End サーバー上でホストすることもできます。</span><span class="sxs-lookup"><span data-stu-id="eae3f-124">Monitoring and Archiving each still require a separate Back-End Database, which can be collocated on the same server as the Front End Pool’s back-end database, or can be hosted on separate Back-End Servers.</span></span>

  - <span data-ttu-id="eae3f-125">常設チャットサーバーがサーバーの役割になりました。</span><span class="sxs-lookup"><span data-stu-id="eae3f-125">Persistent Chat Server is now a server role.</span></span> <span data-ttu-id="eae3f-126">Microsoft Lync Server 2010 では、グループチャットサーバーは Microsoft Lync Server 2010 用のサードパーティの信頼済みアプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="eae3f-126">In Microsoft Lync Server 2010, Group Chat Server was a third-party trusted application for Microsoft Lync Server 2010.</span></span> <span data-ttu-id="eae3f-127">Lync Server 2013 では、次の3つの新しいサーバーの役割を使用して、常設チャットサーバー機能が実装されています。</span><span class="sxs-lookup"><span data-stu-id="eae3f-127">In Lync Server 2013, Persistent Chat Server functionality is implemented using three new server roles:</span></span>
    
      - <span data-ttu-id="eae3f-128">**PersistentChatService:** フロントエンドロールとして実装されたメインの常設チャットサーバーサービス</span><span class="sxs-lookup"><span data-stu-id="eae3f-128">**PersistentChatService:** Main Persistent Chat Server services implemented as a front end role</span></span>
    
      - <span data-ttu-id="eae3f-129">**PersistentChatStore:** バックエンドサーバーの役割</span><span class="sxs-lookup"><span data-stu-id="eae3f-129">**PersistentChatStore:** Back End Server role</span></span>
    
      - <span data-ttu-id="eae3f-130">**PersistentChatComplianceStore:** 常設チャットのコンプライアンスのためのバックエンドサーバーの役割</span><span class="sxs-lookup"><span data-stu-id="eae3f-130">**PersistentChatComplianceStore:** Back End Server role for Persistent Chat Compliance</span></span>

<span data-ttu-id="eae3f-131"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="eae3f-131"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

