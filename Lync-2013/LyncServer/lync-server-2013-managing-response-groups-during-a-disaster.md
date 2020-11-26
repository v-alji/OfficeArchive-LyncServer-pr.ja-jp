---
title: 'Lync Server 2013: 障害時の応答グループの管理'
description: 'Lync Server 2013: 障害発生時に応答グループを管理します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing response groups during a disaster
ms:assetid: 9f14e677-7be8-4f08-88ba-444ec2148ce8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688154(v=OCS.15)
ms:contentKeyID: 49733757
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 16018f170395e4657daf4405798be05c6da62581
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446061"
---
# <a name="managing-response-groups-in-lync-server-2013-during-a-disaster"></a><span data-ttu-id="3f91a-103">障害時の Lync Server 2013 での応答グループの管理</span><span class="sxs-lookup"><span data-stu-id="3f91a-103">Managing response groups in Lync Server 2013 during a disaster</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3f91a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3f91a-104">

<span> </span></span></span>

<span data-ttu-id="3f91a-105">_**最終更新日:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="3f91a-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="3f91a-106">Lync Server 2013 は、障害回復中のバックアッププールでの応答グループの実行をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="3f91a-106">Lync Server 2013 supports running response groups in the backup pool during disaster recovery.</span></span> <span data-ttu-id="3f91a-107">このセクションでは、停止中の応答グループの計画方法、停止中の返信グループのしくみ、フェイルオーバーおよび応答グループのフェールオーバーとフェイルバックに必要な手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="3f91a-107">This section describes how to plan for response groups during an outage, how response groups work during the outage, and the steps required to fail over and fail back response groups.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="3f91a-108">このセクション中</span><span class="sxs-lookup"><span data-stu-id="3f91a-108">In This Section</span></span>

  - [<span data-ttu-id="3f91a-109">Lync Server 2013 での応答グループの障害復旧の計画</span><span class="sxs-lookup"><span data-stu-id="3f91a-109">Planning for response group disaster recovery in Lync Server 2013</span></span>](lync-server-2013-planning-for-response-group-disaster-recovery.md)

  - [<span data-ttu-id="3f91a-110">Lync Server 2013 でのプール障害時の応答グループのエクスペリエンス</span><span class="sxs-lookup"><span data-stu-id="3f91a-110">Response group experience in Lync Server 2013 during pool failure</span></span>](lync-server-2013-response-group-experience-during-pool-failure.md)

  - [<span data-ttu-id="3f91a-111">Lync Server 2013 の応答グループの障害復旧手順</span><span class="sxs-lookup"><span data-stu-id="3f91a-111">Response group disaster recovery procedures in Lync Server 2013</span></span>](lync-server-2013-response-group-disaster-recovery-procedures.md)

<span data-ttu-id="3f91a-112"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3f91a-112"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

