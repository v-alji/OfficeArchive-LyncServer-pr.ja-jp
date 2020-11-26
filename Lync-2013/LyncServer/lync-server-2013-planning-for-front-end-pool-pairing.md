---
title: 'Lync Server 2013: フロント エンド プールのペアリングの計画'
description: 'Lync Server 2013: フロントエンドプールのペアリングを計画しています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for Front End pool pairing
ms:assetid: cca5773d-57ff-45ce-a7b4-f82ae697c477
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205293(v=OCS.15)
ms:contentKeyID: 48185508
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ac235cf682e286132836e13b34b457adf2bfc233
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424563"
---
# <a name="planning-for-front-end-pool-pairing-in-lync-server-2013"></a><span data-ttu-id="ed866-103">Lync Server 2013 でのフロント エンド プールのペアリングの計画</span><span class="sxs-lookup"><span data-stu-id="ed866-103">Planning for Front End pool pairing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ed866-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ed866-104">

<span> </span></span></span>

<span data-ttu-id="ed866-105">_**最終更新日:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="ed866-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="ed866-106">Lync Server 2013 で最高の障害回復機能を使用するには、地理的に分散した2つのサイトにフロントエンドプールのペアを展開します。</span><span class="sxs-lookup"><span data-stu-id="ed866-106">For the best disaster recovery abilities in Lync Server 2013, deploy pairs of Front End pools across two geographically dispersed sites.</span></span> <span data-ttu-id="ed866-107">各サイトには、他のサイトで対応するフロントエンドプールとペアリングされたフロントエンドプールが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ed866-107">Each site contains a Front End pool which is paired with a corresponding Front End pool in the other site.</span></span> <span data-ttu-id="ed866-108">両方のサイトがアクティブになり、Lync Server バックアップサービスはリアルタイムのデータレプリケーションを提供して、プールの同期を維持します。</span><span class="sxs-lookup"><span data-stu-id="ed866-108">Both sites are active, and the Lync Server Backup Service provides real-time data replication to keep the pools synchronized.</span></span> <span data-ttu-id="ed866-109">バックアップサービスは、Lync Server 2013 の新機能であり、障害回復ソリューションをサポートするように設計されています。</span><span class="sxs-lookup"><span data-stu-id="ed866-109">The Backup Service is a new feature in Lync Server 2013, designed to support the disaster recovery solution.</span></span> <span data-ttu-id="ed866-110">プールを別のフロントエンドプールとペアリングすると、フロントエンドプールにインストールされます。</span><span class="sxs-lookup"><span data-stu-id="ed866-110">It is installed on a Front End pool when you pair the pool with another Front End pool.</span></span>

<span data-ttu-id="ed866-111">1つのサイトのプールで障害が発生した場合は、そのプールのユーザーを他のサイトのプールにフェイルオーバーすることができます。これにより、両方のプールのすべてのユーザーにサービスが提供されます。</span><span class="sxs-lookup"><span data-stu-id="ed866-111">If the pool in one site fails, you can fail over the users from that pool to the pool in the other site, which then provides services to all the users in both pools.</span></span> <span data-ttu-id="ed866-112">容量の計画を立てるために、各プールは、障害が発生した場合に両方のプールのすべてのユーザーの作業負荷を処理するように設計する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed866-112">For capacity planning purposes, each pool should be designed to handle the workloads of all users in both pools in the event of a disaster.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="ed866-113">このセクション中</span><span class="sxs-lookup"><span data-stu-id="ed866-113">In This Section</span></span>

  - [<span data-ttu-id="ed866-114">サポートされているプールペアリングオプションと Lync Server 2013 のベストプラクティス</span><span class="sxs-lookup"><span data-stu-id="ed866-114">Supported pool pairing options and best practices for Lync Server 2013</span></span>](lync-server-2013-supported-pool-pairing-options-and-best-practices.md)

  - [<span data-ttu-id="ed866-115">Lync Server 2013 のバックアップ レジストラー関係</span><span class="sxs-lookup"><span data-stu-id="ed866-115">Backup Registrar relationships in Lync Server 2013</span></span>](lync-server-2013-backup-registrar-relationships.md)

  - [<span data-ttu-id="ed866-116">Lync Server 2013 のプールのフェールオーバーおよびフェールバックの復旧時間</span><span class="sxs-lookup"><span data-stu-id="ed866-116">Recovery time for pool failover and pool failback in Lync Server 2013</span></span>](lync-server-2013-recovery-time-for-pool-failover-and-pool-failback.md)

  - [<span data-ttu-id="ed866-117">Lync Server 2013 の中央管理ストアのフェールオーバー</span><span class="sxs-lookup"><span data-stu-id="ed866-117">Central Management store failover in Lync Server 2013</span></span>](lync-server-2013-central-management-store-failover.md)

  - [<span data-ttu-id="ed866-118">Lync Server 2013 でのフロントエンド プールのペアリング データのセキュリティ</span><span class="sxs-lookup"><span data-stu-id="ed866-118">Front End pool pairing data security in Lync Server 2013</span></span>](lync-server-2013-front-end-pool-pairing-data-security.md)

<span data-ttu-id="ed866-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ed866-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

