---
title: 'Lync Server 2013: 運用ガイド'
description: 'Lync Server 2013: 運用ガイド。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Operations Guide
ms:assetid: dcb9ddff-6fe3-4077-a2e3-0ba64f65e264
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720467(v=OCS.15)
ms:contentKeyID: 63969658
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 85e562b96e87f54529a9e2ce077a0a82574020c1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445280"
---
# <a name="operations-guide-for-lync-server-2013"></a><span data-ttu-id="82ba4-103">Operations Guide for Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="82ba4-103">Operations Guide for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="82ba4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="82ba4-104">

<span> </span></span></span>

<span data-ttu-id="82ba4-105">_**最終更新日:** 2014-08-18_</span><span class="sxs-lookup"><span data-stu-id="82ba4-105">_**Topic Last Modified:** 2014-08-18_</span></span>

<span data-ttu-id="82ba4-106">このドキュメントでは、Microsoft Lync Server 2013 通信ソフトウェア環境を維持するために必要な運用プロセス、タスク、ツールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="82ba4-106">This document describes the operational processes, tasks, and tools that are required for you to maintain a Microsoft Lync Server 2013 communications software environment.</span></span> <span data-ttu-id="82ba4-107">ここでは、Microsoft Operations Framework (MOF) モデルに従って Lync Server 2013 を管理する方法について説明します。効率的な運用管理環境を設計するのに役立ちます。これには、効率的な作業環境を維持するためのスケジュール、プロセス、手順の実装が含まれます。</span><span class="sxs-lookup"><span data-stu-id="82ba4-107">It explains how to manage Lync Server 2013 according to the Microsoft Operations Framework (MOF) model and it will help you design an efficient operational management environment, which includes implementing schedules, processes and procedures to maintain an efficient working environment.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="82ba4-108">このセクション中</span><span class="sxs-lookup"><span data-stu-id="82ba4-108">In This Section</span></span>

<span data-ttu-id="82ba4-109">次のセクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="82ba4-109">The following sections are included:</span></span>

  - [<span data-ttu-id="82ba4-110">Lync Server 2013 環境のベストプラクティス</span><span class="sxs-lookup"><span data-stu-id="82ba4-110">Best practices for Lync Server 2013 environments</span></span>](lync-server-2013-best-practices-for-lync-server-environments.md)

  - [<span data-ttu-id="82ba4-111">Lync Server 2013 での日次タスク</span><span class="sxs-lookup"><span data-stu-id="82ba4-111">Daily tasks in Lync Server 2013</span></span>](lync-server-2013-daily-tasks.md)

  - [<span data-ttu-id="82ba4-112">Lync Server 2013 での週次タスク</span><span class="sxs-lookup"><span data-stu-id="82ba4-112">Weekly tasks in Lync Server 2013</span></span>](lync-server-2013-weekly-tasks.md)

  - [<span data-ttu-id="82ba4-113">Lync Server 2013 の月次タスク</span><span class="sxs-lookup"><span data-stu-id="82ba4-113">Monthly tasks in Lync Server 2013</span></span>](lync-server-2013-monthly-tasks.md)

  - [<span data-ttu-id="82ba4-114">Lync Server 2013 での必要なタスク</span><span class="sxs-lookup"><span data-stu-id="82ba4-114">As-needed tasks in Lync Server 2013</span></span>](lync-server-2013-as-needed-tasks.md)

  - [<span data-ttu-id="82ba4-115">Lync Server 2013 の操作チェックリスト</span><span class="sxs-lookup"><span data-stu-id="82ba4-115">Operations checklists for Lync Server 2013</span></span>](lync-server-2013-operations-checklists.md)

  - [<span data-ttu-id="82ba4-116">System Center Operations Manager での Lync Server 2013 の監視</span><span class="sxs-lookup"><span data-stu-id="82ba4-116">Monitoring Lync Server 2013 with System Center Operations Manager</span></span>](lync-server-2013-monitoring-lync-server-with-system-center-operations-manager.md)

  - [<span data-ttu-id="82ba4-117">Lync Server 2013 での操作の依存関係</span><span class="sxs-lookup"><span data-stu-id="82ba4-117">Operational dependencies in Lync Server 2013</span></span>](lync-server-2013-operational-dependencies.md)

  - [<span data-ttu-id="82ba4-118">Lync Server 2013 のトラブルシューティングと主要な正常性インジケーター</span><span class="sxs-lookup"><span data-stu-id="82ba4-118">Troubleshooting and Key Health Indicators in Lync Server 2013</span></span>](lync-server-2013-troubleshooting-and-key-health-indicators.md)

<span data-ttu-id="82ba4-119">Microsoft Lync Server 2013 の展開が完了していることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="82ba4-119">It is assumed that your Microsoft Lync Server 2013 deployment is completed.</span></span> <span data-ttu-id="82ba4-120">このようになっていない場合は、続行する前に、「Microsoft Lync Server 2013 の計画と展開のコンテンツ」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="82ba4-120">If this is not the case, refer to the planning and deployment content for Microsoft Lync Server 2013 before you continue.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="82ba4-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="82ba4-121">See Also</span></span>


[<span data-ttu-id="82ba4-122">Lync Server 2013 での作業の開始</span><span class="sxs-lookup"><span data-stu-id="82ba4-122">Getting started with Lync Server 2013</span></span>](lync-server-2013-getting-started.md)  
[<span data-ttu-id="82ba4-123">Lync Server 2013 の計画</span><span class="sxs-lookup"><span data-stu-id="82ba4-123">Planning for Lync Server 2013</span></span>](lync-server-2013-planning.md)  
[<span data-ttu-id="82ba4-124">Lync Server 2013 の展開</span><span class="sxs-lookup"><span data-stu-id="82ba4-124">Deployment of Lync Server 2013</span></span>](lync-server-2013-deployment.md)  
[<span data-ttu-id="82ba4-125">Lync Server 2013 管理シェル</span><span class="sxs-lookup"><span data-stu-id="82ba4-125">Lync Server 2013 Management Shell</span></span>](lync-server-2013-lync-server-management-shell.md)  
  

<span data-ttu-id="82ba4-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="82ba4-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

