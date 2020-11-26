---
title: Lync Server 2013 の計画
description: Lync Server 2013 の計画。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning
ms:assetid: 6398cd91-8773-41bc-9b66-725d65ba9d66
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398447(v=OCS.15)
ms:contentKeyID: 48184302
ms.date: 12/10/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fc4468300195760e7e994087875b5f49489828d2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424402"
---
# <a name="planning-for-lync-server-2013"></a><span data-ttu-id="128bd-103">Lync Server 2013 の計画</span><span class="sxs-lookup"><span data-stu-id="128bd-103">Planning for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="128bd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="128bd-104">

<span> </span></span></span>

<span data-ttu-id="128bd-105">_**最終更新日:** 2014-12-09_</span><span class="sxs-lookup"><span data-stu-id="128bd-105">_**Topic Last Modified:** 2014-12-09_</span></span>

<span data-ttu-id="128bd-106">このセクションのトピックでは、Lync Server の展開を成功させるための計画を立てる方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="128bd-106">The topics in this section describe how to plan for a successful Lync Server deployment.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="128bd-107">このセクション中</span><span class="sxs-lookup"><span data-stu-id="128bd-107">In This Section</span></span>

  - [<span data-ttu-id="128bd-108">Lync Server 2013 の組織の計画</span><span class="sxs-lookup"><span data-stu-id="128bd-108">Organization planning for Lync Server 2013</span></span>](lync-server-2013-planning-for-your-organization.md)

  - [<span data-ttu-id="128bd-109">Lync Server 2013 に関するインフラストラクチャ要件の決定</span><span class="sxs-lookup"><span data-stu-id="128bd-109">Determining your infrastructure requirements for Lync Server 2013</span></span>](lync-server-2013-determining-your-infrastructure-requirements.md)

  - [<span data-ttu-id="128bd-110">Lync Server 2013 のネットワーク計画</span><span class="sxs-lookup"><span data-stu-id="128bd-110">Network planning for Lync Server 2013</span></span>](lync-server-2013-network-planning.md)

  - [<span data-ttu-id="128bd-111">Lync Server 2013 のキャパシティ計画</span><span class="sxs-lookup"><span data-stu-id="128bd-111">Capacity planning for Lync Server 2013</span></span>](lync-server-2013-capacity-planning.md)

  - [<span data-ttu-id="128bd-112">Lync Server 2013 での高可用性および障害復旧の計画</span><span class="sxs-lookup"><span data-stu-id="128bd-112">Planning for high availability and disaster recovery in Lync Server 2013</span></span>](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md)

  - [<span data-ttu-id="128bd-113">Lync Server 2013 での管理性と仮想化の計画</span><span class="sxs-lookup"><span data-stu-id="128bd-113">Planning for manageability and virtualization in Lync Server 2013</span></span>](lync-server-2013-planning-for-manageability-and-virtualization.md)

  - [<span data-ttu-id="128bd-114">Lync Server 2013 でのフロントエンド サーバー、インスタント メッセージングおよびプレゼンスの計画</span><span class="sxs-lookup"><span data-stu-id="128bd-114">Planning for Front End Servers, instant messaging, and presence in Lync Server 2013</span></span>](lync-server-2013-planning-for-front-end-servers-instant-messaging-and-presence.md)

  - [<span data-ttu-id="128bd-115">Lync Server 2013 での会議の計画</span><span class="sxs-lookup"><span data-stu-id="128bd-115">Planning for conferencing in Lync Server 2013</span></span>](lync-server-2013-planning-for-conferencing.md)

  - [<span data-ttu-id="128bd-116">Lync Server 2013 の外部ユーザー アクセスの計画</span><span class="sxs-lookup"><span data-stu-id="128bd-116">Planning for external user access in Lync Server 2013</span></span>](lync-server-2013-planning-for-external-user-access.md)

  - [<span data-ttu-id="128bd-117">Lync Server 2013 でのエンタープライズ Voip の計画</span><span class="sxs-lookup"><span data-stu-id="128bd-117">Planning for Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-planning-for-enterprise-voice.md)

  - [<span data-ttu-id="128bd-118">Lync Server 2013 での監視の計画</span><span class="sxs-lookup"><span data-stu-id="128bd-118">Planning for monitoring in Lync Server 2013</span></span>](lync-server-2013-planning-for-monitoring.md)

  - [<span data-ttu-id="128bd-119">Lync Server 2013 のアーカイブの計画</span><span class="sxs-lookup"><span data-stu-id="128bd-119">Planning for Archiving in Lync Server 2013</span></span>](lync-server-2013-planning-for-archiving.md)

  - [<span data-ttu-id="128bd-120">Lync Server 2013 での常設チャット サーバーの計画</span><span class="sxs-lookup"><span data-stu-id="128bd-120">Planning for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-planning-for-persistent-chat-server.md)

  - [<span data-ttu-id="128bd-121">Exchange Server と Lync Server 2013 の統合計画</span><span class="sxs-lookup"><span data-stu-id="128bd-121">Planning for Exchange Server integration with Lync Server 2013</span></span>](lync-server-2013-planning-for-exchange-server-integration.md)

  - [<span data-ttu-id="128bd-122">Lync Server 2013 でのクライアントとデバイスの計画</span><span class="sxs-lookup"><span data-stu-id="128bd-122">Planning for clients and devices in Lync Server 2013</span></span>](lync-server-2013-planning-for-clients-and-devices.md)

  - [<span data-ttu-id="128bd-123">Lync Server 2013 でのリモート通話コントロールの計画</span><span class="sxs-lookup"><span data-stu-id="128bd-123">Planning for remote call control in Lync Server 2013</span></span>](lync-server-2013-planning-for-remote-call-control.md)

  - [<span data-ttu-id="128bd-124">Lync Server 2013 でのモビリティの計画</span><span class="sxs-lookup"><span data-stu-id="128bd-124">Planning for mobility in Lync Server 2013</span></span>](lync-server-2013-planning-for-mobility.md)

  - [<span data-ttu-id="128bd-125">Lync Server 2013 のセキュリティの計画</span><span class="sxs-lookup"><span data-stu-id="128bd-125">Planning for security in Lync Server 2013</span></span>](lync-server-2013-planning-for-security.md)

<span data-ttu-id="128bd-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="128bd-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

