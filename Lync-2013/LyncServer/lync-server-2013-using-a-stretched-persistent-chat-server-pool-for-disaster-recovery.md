---
title: 障害回復のための拡張型の常設チャット サーバー プールの使用
description: 引き伸ばされた常設チャットサーバープールを使用して災害回復を行います。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using a stretched Persistent Chat Server pool for disaster recovery
ms:assetid: 74c5287e-d70d-490a-9adc-ab419917ddd9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205007(v=OCS.15)
ms:contentKeyID: 48184506
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b83a7226f7b9a49a2676b6222505f53247bd5abf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436091"
---
# <a name="using-a-stretched-persistent-chat-server-pool-for-disaster-recovery-in-lync-server-2013"></a><span data-ttu-id="9a4d4-103">Lync Server 2013 における障害回復のための拡張型の常設チャット サーバー プールの使用</span><span class="sxs-lookup"><span data-stu-id="9a4d4-103">Using a stretched Persistent Chat Server pool for disaster recovery in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9a4d4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9a4d4-104">

<span> </span></span></span>

<span data-ttu-id="9a4d4-105">_**最終更新日:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="9a4d4-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="9a4d4-106">常設チャットサーバーの障害回復ソリューションは、拡張された常設チャットサーバープールを基盤としています。</span><span class="sxs-lookup"><span data-stu-id="9a4d4-106">The disaster recovery solution for Persistent Chat Server is built on a stretched Persistent Chat Server pool.</span></span> <span data-ttu-id="9a4d4-107">これは、Lync Server 2010 のメトロポリタンサイトの回復性に似ています。ただし、ストレッチ仮想ローカルエリアネットワーク (VLAN) を使用する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="9a4d4-107">This is similar to metropolitan site resiliency in Lync Server 2010; however, there is no requirement for a stretched virtual local area network (VLAN).</span></span> <span data-ttu-id="9a4d4-108">常設チャットサーバープールを拡大することで、基本的にトポロジの1つのプールを論理的に構成することができますが、プール内にはサーバーを物理的に2つの異なるデータセンターに配置します。</span><span class="sxs-lookup"><span data-stu-id="9a4d4-108">By stretching Persistent Chat Server pool, you essentially configure one pool in the topology logically, but you physically place the servers in the pool in two different data centers.</span></span> <span data-ttu-id="9a4d4-109">データベースの SQL Server ミラーリングを同じように構成し、同じデータセンターにデータベースとミラーを展開します。</span><span class="sxs-lookup"><span data-stu-id="9a4d4-109">Configure SQL Server mirroring for the database in the same way, and deploy the database and the mirror in the same data center.</span></span> <span data-ttu-id="9a4d4-110">セカンダリ データ センターでは、(障害復旧時に高可用性を提供するためにオプションのミラーを使用して) バックアップ データベースを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a4d4-110">You need to configure a backup database in the secondary data center (with an optional mirror to provide high availability during disaster recovery).</span></span> <span data-ttu-id="9a4d4-111">これは、障害復旧時にフェールオーバー用に使用されるバックアップ データベースです。</span><span class="sxs-lookup"><span data-stu-id="9a4d4-111">This is the backup database used for failover during disaster recovery.</span></span>

<span data-ttu-id="9a4d4-112">高可用性のために SQL Server ミラーリングを構成する方法の詳細については、「 [Lync server 2013 での Sql server のミラーリング](lync-server-2013-sql-server-mirroring.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a4d4-112">For details about how to configure SQL Server mirroring for high availability, see [SQL Server mirroring in Lync Server 2013](lync-server-2013-sql-server-mirroring.md).</span></span> <span data-ttu-id="9a4d4-113">障害回復のためのデータベースのフェイルオーバーについて詳しくは、「 [Lync server 2013 での常設チャットサーバーのプライマリデータベースの sql Server ログの配布の設定](lync-server-2013-setting-up-sql-server-log-shipping-for-the-persistent-chat-server-primary-database.md) 」と「 [lync server 2013 のプライマリミラーとログ配布のセカンダリデータベースの間での Sql Server のログ配布](lync-server-2013-set-up-log-shipping-secondary-database.md)のセットアップ」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="9a4d4-113">For details about failing over the database for disaster recovery, see [Setting up SQL Server Log Shipping in Lync Server 2013 for the Persistent Chat Server primary database](lync-server-2013-setting-up-sql-server-log-shipping-for-the-persistent-chat-server-primary-database.md) and [Setting up SQL Server Log Shipping between the primary mirror and the Log Shipping secondary database in Lync Server 2013](lync-server-2013-set-up-log-shipping-secondary-database.md).</span></span>

<span data-ttu-id="9a4d4-114"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9a4d4-114"></div>

<span> </span>

</div>

</div>

</span></span></div>

