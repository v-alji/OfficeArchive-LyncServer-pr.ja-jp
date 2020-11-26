---
title: 'Lync Server 2013: バックアップと復元の戦略と計画を策定する'
description: 'Lync Server 2013: バックアップと復元の戦略と計画を作成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Developing a backup and restoration strategy and plan
ms:assetid: 17599b76-1a84-4dd6-b695-c19637deb8a6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202164(v=OCS.15)
ms:contentKeyID: 51541447
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3d55eeb541cdde5c43d7d680ceb212d87da0d517
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429452"
---
# <a name="developing-a-backup-and-restoration-strategy-and-plan-for-lync-server-2013"></a><span data-ttu-id="f4a30-103">バックアップと復元の戦略と Lync Server 2013 の計画を作成する</span><span class="sxs-lookup"><span data-stu-id="f4a30-103">Developing a backup and restoration strategy and plan for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f4a30-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f4a30-104">

<span> </span></span></span>

<span data-ttu-id="f4a30-105">_**最終更新日:** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="f4a30-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<span data-ttu-id="f4a30-106">Lync Server のバックアップと復元の操作の有効性は、バックアップと復元の戦略と計画によって異なります。</span><span class="sxs-lookup"><span data-stu-id="f4a30-106">The effectiveness of your Lync Server backup and restoration operations depends on your backup and restoration strategy and plan.</span></span> <span data-ttu-id="f4a30-107">組織の全体的な戦略に適合する Lync Server のバックアップと復元の戦略、データと設定のバックアップを行うための包括的な計画、およびサービスの復元の計画を確立する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4a30-107">You should establish a strategy for backing up and restoring Lync Server that fits with your organization's overall strategy, and a comprehensive, concise plan for backing up data and settings, and, in the event of an outage, a plan for restoring service.</span></span>

<span data-ttu-id="f4a30-108">フロントエンドプールの最も強力な障害回復を行うには、Lync Server 2013 で導入された、ペアリングされたプールの障害回復トポロジを使用します。</span><span class="sxs-lookup"><span data-stu-id="f4a30-108">For the most robust disaster recovery of a Front End Pool, use the paired-pool disaster recovery topology introduced in Lync Server 2013.</span></span> <span data-ttu-id="f4a30-109">詳細については、「 [Lync Server 2013 での高可用性と障害回復の計画](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f4a30-109">For more information, see [Planning for high availability and disaster recovery in Lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md).</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="f4a30-110">このセクション中</span><span class="sxs-lookup"><span data-stu-id="f4a30-110">In This Section</span></span>

  - [<span data-ttu-id="f4a30-111">Lync Server 2013 のバックアップと復元の戦略を確立する</span><span class="sxs-lookup"><span data-stu-id="f4a30-111">Establishing a backup and restoration strategy for Lync Server 2013</span></span>](lync-server-2013-establishing-a-backup-and-restoration-strategy.md)

  - [<span data-ttu-id="f4a30-112">Lync Server 2013 のバックアップと復元の計画を立てる</span><span class="sxs-lookup"><span data-stu-id="f4a30-112">Establishing a backup and restoration plan for Lync Server 2013</span></span>](lync-server-2013-establishing-a-backup-and-restoration-plan.md)

  - [<span data-ttu-id="f4a30-113">Lync Server 2013 のバックアップ場所の設定</span><span class="sxs-lookup"><span data-stu-id="f4a30-113">Setting up a backup location for Lync Server 2013</span></span>](lync-server-2013-setting-up-a-backup-location.md)

<span data-ttu-id="f4a30-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f4a30-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

