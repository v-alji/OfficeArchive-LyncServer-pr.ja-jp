---
title: 'Lync Server 2013: Lync Server のバックアップと復元'
description: 'Lync Server 2013: Lync Server のバックアップと復元'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Backing up and restoring Lync Server 2013
ms:assetid: 07dc1f5e-af66-4e18-bf39-881dceff8bc3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202160(v=OCS.15)
ms:contentKeyID: 51541443
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c1a7024b2264fb895d1562a6da0775f9397644b4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438142"
---
# <a name="backing-up-and-restoring-lync-server-2013"></a><span data-ttu-id="0c9ea-103">Lync Server 2013 のバックアップと復元</span><span class="sxs-lookup"><span data-stu-id="0c9ea-103">Backing up and restoring Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0c9ea-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0c9ea-104">

<span> </span></span></span>

<span data-ttu-id="0c9ea-105">_**最終更新日:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="0c9ea-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="0c9ea-106">このセクションでは、Lync Server 2013 データをバックアップするためのベストプラクティスと、エラーが発生した場合に復元するためのベストプラクティスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="0c9ea-106">In this section, you’ll find the best practices for backing up your Lync Server 2013 data, and for restoring it if you have a failure.</span></span> <span data-ttu-id="0c9ea-107">このベストプラクティスは、次のような場合に適用されます。</span><span class="sxs-lookup"><span data-stu-id="0c9ea-107">These best practices apply to the following situations:</span></span>

  - <span data-ttu-id="0c9ea-108">任意の種類の Lync Server プール全体 (フロントエンドサーバー、エッジサーバー、仲介サーバー、常設チャットサーバー、またはディレクター)、またはこれらのいずれかのプールの個々のサーバー。</span><span class="sxs-lookup"><span data-stu-id="0c9ea-108">An entire Lync Server pool of any type (Front End Server, Edge Server, Mediation Server, Persistent Chat Server, or Director), or an individual server in one of these pools.</span></span>

  - <span data-ttu-id="0c9ea-109">中央管理サーバー</span><span class="sxs-lookup"><span data-stu-id="0c9ea-109">The Central Management Server</span></span>

  - <span data-ttu-id="0c9ea-110">Standard Edition サーバー</span><span class="sxs-lookup"><span data-stu-id="0c9ea-110">A Standard Edition server</span></span>

  - <span data-ttu-id="0c9ea-111">Enterprise Edition バックエンドサーバー</span><span class="sxs-lookup"><span data-stu-id="0c9ea-111">An Enterprise Edition Back End Server</span></span>

  - <span data-ttu-id="0c9ea-112">ファイルストア</span><span class="sxs-lookup"><span data-stu-id="0c9ea-112">A File Store</span></span>

  - <span data-ttu-id="0c9ea-113">アーカイブデータベース、監視データベース、または常設チャットデータベース</span><span class="sxs-lookup"><span data-stu-id="0c9ea-113">An Archiving database, Monitoring database, or Persistent Chat database</span></span>

<span data-ttu-id="0c9ea-114">このセクションには、サイト全体の復元、またはスタンバイサイトの開発に関する情報は含まれていません。</span><span class="sxs-lookup"><span data-stu-id="0c9ea-114">This section does not include information about restoring an entire site or for developing a standby site.</span></span> <span data-ttu-id="0c9ea-115">ペアリングされたフロントエンドプールでの障害回復ソリューションの開発について詳しくは、「 [Lync Server 2013 での高可用性と障害回復の計画](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="0c9ea-115">For details about developing a disaster recovery solution with paired Front End pools, see [Planning for high availability and disaster recovery in Lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md).</span></span> <span data-ttu-id="0c9ea-116">これは、障害回復を計画するための推奨される方法です。</span><span class="sxs-lookup"><span data-stu-id="0c9ea-116">This is the recommended method for planning for disaster recovery.</span></span>

<span data-ttu-id="0c9ea-117">ペアリングされたフロントエンドプールを展開している場合、これらのプールのいずれかが失敗して回復不能になった場合は、そのペアのプールから新しい完全修飾ドメイン名 (FQDN) を使用して、このプールを復元することができます。</span><span class="sxs-lookup"><span data-stu-id="0c9ea-117">If you have deployed paired Front End pools, if one of these pools fails and becomes unrecoverable, you can restore this pool with a new fully qualified domain name (FQDN) from its paired pool.</span></span> <span data-ttu-id="0c9ea-118">この回復を実行する手順の詳細については、「 [Lync Server 2013 でのプールのフェールオーバー](lync-server-2013-failing-over-a-pool.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0c9ea-118">For details on the steps to perform this recovery, see [Failing over a pool in Lync Server 2013](lync-server-2013-failing-over-a-pool.md).</span></span> <span data-ttu-id="0c9ea-119">さらに、フロントエンドペアの一部であった失敗した回復可能なプールを後で再作成する必要がある場合は、「 [Lync Server 2013 で ABC フロントエンドプールフェールオーバーを実行](lync-server-2013-performing-an-abc-front-end-pool-failover.md)する」の手順を使用できます。</span><span class="sxs-lookup"><span data-stu-id="0c9ea-119">Additionally, if you later want to recreate a failed and unrecoverable pool that was part of a Front End pair, you can use the steps in [Performing an ABC Front End pool failover in Lync Server 2013](lync-server-2013-performing-an-abc-front-end-pool-failover.md).</span></span>

<span data-ttu-id="0c9ea-120">このドキュメントで説明する方法には、計画フェーズでの特別な考慮事項が含まれます。</span><span class="sxs-lookup"><span data-stu-id="0c9ea-120">The methodology described in this document involves special considerations during the planning phase.</span></span> <span data-ttu-id="0c9ea-121">詳細については、「 [Lync Server 2013 のバックアップと復元計画を立てる](lync-server-2013-establishing-a-backup-and-restoration-plan.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0c9ea-121">For details, see [Establishing a backup and restoration plan for Lync Server 2013](lync-server-2013-establishing-a-backup-and-restoration-plan.md).</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="0c9ea-122">このセクション中</span><span class="sxs-lookup"><span data-stu-id="0c9ea-122">In This Section</span></span>

  - [<span data-ttu-id="0c9ea-123">Lync Server 2013 のバックアップと復元の準備</span><span class="sxs-lookup"><span data-stu-id="0c9ea-123">Preparing for Lync Server 2013 backup and restoration</span></span>](lync-server-2013-preparing-for-lync-server-backup-and-restoration.md)

  - [<span data-ttu-id="0c9ea-124">Lync Server 2013 でのデータと設定のバックアップ</span><span class="sxs-lookup"><span data-stu-id="0c9ea-124">Backing up data and settings in Lync Server 2013</span></span>](lync-server-2013-backing-up-data-and-settings.md)

  - [<span data-ttu-id="0c9ea-125">Lync Server 2013 でのデータと設定の復元</span><span class="sxs-lookup"><span data-stu-id="0c9ea-125">Restoring data and settings in Lync Server 2013</span></span>](lync-server-2013-restoring-data-and-settings.md)

  - [<span data-ttu-id="0c9ea-126">Lync Server 2013 のバックアップと復元ワークシート</span><span class="sxs-lookup"><span data-stu-id="0c9ea-126">Backup and restoration worksheets for Lync Server 2013</span></span>](lync-server-2013-backup-and-restoration-worksheets.md)

<span data-ttu-id="0c9ea-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0c9ea-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

