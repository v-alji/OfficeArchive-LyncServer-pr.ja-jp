---
title: 高可用性と障害復旧に対応した常設チャット サーバーの構成
description: 高可用性と障害回復を実現するための常設チャットサーバーの構成。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Persistent Chat Server for high availability and disaster recovery
ms:assetid: eebc581c-e3a0-4b69-8a43-80b607b4d8f2
ms:mtpsurl: https://technet.microsoft.com/library/JJ205364(v=OCS.15)
ms:contentKeyID: 48185760
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 13935f2ec690deb7f896c13d185680ce1122a892
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432787"
---
# <a name="configuring-persistent-chat-server-for-high-availability-and-disaster-recovery-in-lync-server-2013"></a><span data-ttu-id="1d63d-103">Lync Server 2013 の高可用性と障害復旧に対応した常設チャット サーバーの構成</span><span class="sxs-lookup"><span data-stu-id="1d63d-103">Configuring Persistent Chat Server for high availability and disaster recovery in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1d63d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1d63d-104">

<span> </span></span></span>

<span data-ttu-id="1d63d-105">_**最終更新日:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="1d63d-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="1d63d-106">Lync Server 2013 の常設チャットサーバーサービスは、障害回復のために *拡張プール* 構成を使います。</span><span class="sxs-lookup"><span data-stu-id="1d63d-106">The Lync Server 2013, Persistent Chat Server services use a *stretched pool* configuration for disaster recovery.</span></span> <span data-ttu-id="1d63d-107">ストレッチプールは、2つの物理データセンターの間で配布され、1つの論理的な Lync Server サイト内にあるコンピューターを含むプールです。</span><span class="sxs-lookup"><span data-stu-id="1d63d-107">A stretched pool is a pool that has computers that are distributed between two physical data centers, but are within a single logical Lync Server site.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="1d63d-108">このセクション中</span><span class="sxs-lookup"><span data-stu-id="1d63d-108">In This Section</span></span>

  - [<span data-ttu-id="1d63d-109">Lync Server 2013 の常設チャット サーバーに必要なリソース</span><span class="sxs-lookup"><span data-stu-id="1d63d-109">Required resources for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-required-resources-for-persistent-chat-server.md)

  - [<span data-ttu-id="1d63d-110">Lync Server 2013 でトポロジ ビルダーを使用して高可用性と障害回復を構成する</span><span class="sxs-lookup"><span data-stu-id="1d63d-110">Using Topology Builder to configure high availability and disaster recovery in Lync Server 2013</span></span>](lync-server-2013-using-topology-builder-to-configure-high-availability-and-disaster-recovery.md)

  - [<span data-ttu-id="1d63d-111">Lync Server 2013 における障害回復のための拡張型の常設チャット サーバー プールの使用</span><span class="sxs-lookup"><span data-stu-id="1d63d-111">Using a stretched Persistent Chat Server pool for disaster recovery in Lync Server 2013</span></span>](lync-server-2013-using-a-stretched-persistent-chat-server-pool-for-disaster-recovery.md)

  - [<span data-ttu-id="1d63d-112">Lync Server 2013 での SQL Server のミラーリング</span><span class="sxs-lookup"><span data-stu-id="1d63d-112">SQL Server mirroring in Lync Server 2013</span></span>](lync-server-2013-sql-server-mirroring.md)

  - [<span data-ttu-id="1d63d-113">Lync Server 2013 で常設チャット サーバーのプライマリ データベースの SQL Server ログ配布を設定する</span><span class="sxs-lookup"><span data-stu-id="1d63d-113">Setting up SQL Server Log Shipping in Lync Server 2013 for the Persistent Chat Server primary database</span></span>](lync-server-2013-setting-up-sql-server-log-shipping-for-the-persistent-chat-server-primary-database.md)

  - [<span data-ttu-id="1d63d-114">Lync Server 2013 でのプライマリ ミラーとログ配布セカンダリ データベース間での SQL Server ログ配布のセットアップ</span><span class="sxs-lookup"><span data-stu-id="1d63d-114">Setting up SQL Server Log Shipping between the primary mirror and the Log Shipping secondary database in Lync Server 2013</span></span>](lync-server-2013-set-up-log-shipping-secondary-database.md)

<span data-ttu-id="1d63d-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1d63d-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

