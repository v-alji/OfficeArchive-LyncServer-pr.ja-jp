---
title: 'Lync Server 2013: 監視の計画'
description: 'Lync Server 2013: 監視を計画しています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for monitoring
ms:assetid: 26cead5a-183c-42f1-a4b0-0e8d61c6159d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204752(v=OCS.15)
ms:contentKeyID: 48183671
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f8ee78f06423bc167e26455d399ce2dd16f24262
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442930"
---
# <a name="planning-for-monitoring-in-lync-server-2013"></a><span data-ttu-id="935d6-103">Lync Server 2013 での監視の計画</span><span class="sxs-lookup"><span data-stu-id="935d6-103">Planning for monitoring in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="935d6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="935d6-104">

<span> </span></span></span>

<span data-ttu-id="935d6-105">_**最終更新日:** 2012-09-05_</span><span class="sxs-lookup"><span data-stu-id="935d6-105">_**Topic Last Modified:** 2012-09-05_</span></span>

<span data-ttu-id="935d6-106">Microsoft Lync Server 2013 の監視サービスでは、管理者が、組織内で行われる通信セッションの利用状況、傾向、およびサービスデータの品質を収集するための手段を提供します。</span><span class="sxs-lookup"><span data-stu-id="935d6-106">The monitoring service in Microsoft Lync Server 2013 provides a way for administrators to collect usage, trend, and quality of service data for the communication sessions that take place in their organization.</span></span> <span data-ttu-id="935d6-107">Lync Server 2013 での監視では、別のサーバーの役割が不要になりました。代わりに、監視サービスは各フロントエンドサーバーに組み込まれています。</span><span class="sxs-lookup"><span data-stu-id="935d6-107">Monitoring in Lync Server 2013 no longer requires a separate server role; instead, the monitoring service is built into each Front End server.</span></span> <span data-ttu-id="935d6-108">ただし、既定では、Lync Server 2013 で監視は有効になっていません。</span><span class="sxs-lookup"><span data-stu-id="935d6-108">However, by default monitoring is not enabled in Lync Server 2013.</span></span> <span data-ttu-id="935d6-109">このドキュメントでは、組織で監視を有効にするかどうかを決定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="935d6-109">This document will help you determine whether or not monitoring should be enabled in your organization.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="935d6-110">このセクション中</span><span class="sxs-lookup"><span data-stu-id="935d6-110">In This Section</span></span>

  - [<span data-ttu-id="935d6-111">Lync Server 2013 での監視の概要</span><span class="sxs-lookup"><span data-stu-id="935d6-111">Overview of monitoring in Lync Server 2013</span></span>](lync-server-2013-overview-of-monitoring.md)

  - [<span data-ttu-id="935d6-112">Lync Server 2013 での監視要件の定義</span><span class="sxs-lookup"><span data-stu-id="935d6-112">Defining your requirements for monitoring in Lync Server 2013</span></span>](lync-server-2013-defining-your-requirements-for-monitoring.md)

  - [<span data-ttu-id="935d6-113">Lync Server 2013 で監視を有効にする</span><span class="sxs-lookup"><span data-stu-id="935d6-113">Enabling monitoring in Lync Server 2013</span></span>](lync-server-2013-enabling-monitoring.md)

  - [<span data-ttu-id="935d6-114">Lync Server 2013 での監視データへのアクセス</span><span class="sxs-lookup"><span data-stu-id="935d6-114">Accessing monitoring data in Lync Server 2013</span></span>](lync-server-2013-accessing-monitoring-data.md)

  - [<span data-ttu-id="935d6-115">Lync Server 2013 における監視のためのコンポーネントとトポロジ</span><span class="sxs-lookup"><span data-stu-id="935d6-115">Components and topologies for monitoring in Lync Server 2013</span></span>](lync-server-2013-components-and-topologies-for-monitoring.md)

  - [<span data-ttu-id="935d6-116">Lync Server 2013 の監視の展開チェックリスト</span><span class="sxs-lookup"><span data-stu-id="935d6-116">Deployment checklist for monitoring in Lync Server 2013</span></span>](lync-server-2013-deployment-checklist-for-monitoring.md)

<span data-ttu-id="935d6-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="935d6-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

