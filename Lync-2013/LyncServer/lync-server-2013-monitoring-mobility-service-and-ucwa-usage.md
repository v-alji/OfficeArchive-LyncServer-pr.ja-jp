---
title: 'Lync Server 2013: モビリティサービスと UCWA の使用状況を監視する'
description: 'Lync Server 2013: モビリティサービスと UCWA の使用状況を監視します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Monitoring Mobility Service and UCWA usage
ms:assetid: 8389b37a-ca3e-4047-8b51-85bc07da87e8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690025(v=OCS.15)
ms:contentKeyID: 48184683
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6575941faf904e46cd1f66d7226a16c88e8cbaa3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425396"
---
# <a name="monitoring-mobility-service-and-ucwa-usage-in-lync-server-2013"></a><span data-ttu-id="3f1a1-103">Lync Server 2013 でのモビリティサービスと UCWA の使用状況の監視</span><span class="sxs-lookup"><span data-stu-id="3f1a1-103">Monitoring Mobility Service and UCWA usage in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3f1a1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3f1a1-104">

<span> </span></span></span>

<span data-ttu-id="3f1a1-105">_**最終更新日:** 2013-02-14_</span><span class="sxs-lookup"><span data-stu-id="3f1a1-105">_**Topic Last Modified:** 2013-02-14_</span></span>

<span data-ttu-id="3f1a1-106">継続的に、Lync Server Mobility Service (Mcx) とユニファイドコミュニケーション Web API (UCWA) で使用されている CPU とメモリを監視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3f1a1-106">On an ongoing basis, you should monitor the CPU and memory that is used by the Lync Server Mobility Service (Mcx) and the Unified Communications Web API (UCWA).</span></span> <span data-ttu-id="3f1a1-107">使用状況を監視するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="3f1a1-107">To monitor usage, you can use the following:</span></span>

<span data-ttu-id="3f1a1-108">**Unified Communications Web API (UCWA):**</span><span class="sxs-lookup"><span data-stu-id="3f1a1-108">**For Unified Communications Web API (UCWA):**</span></span>

  - <span data-ttu-id="3f1a1-109">インターネットインフォメーションサービス (IIS) マネージャーでの **LyncUcwa** worker プロセス。</span><span class="sxs-lookup"><span data-stu-id="3f1a1-109">The **LyncUcwa** worker process in Internet Information Services (IIS) Manager.</span></span> <span data-ttu-id="3f1a1-110">[**ワーカー プロセス**] ウィンドウで、[**CPU %**] および [**プライベート バイト (KB)**] (メモリ) の列を確認します。</span><span class="sxs-lookup"><span data-stu-id="3f1a1-110">In the **Worker Processes** pane, look at the **CPU %** and **Private Bytes (KB)** (memory) columns.</span></span>

  - <span data-ttu-id="3f1a1-111">[**CPU**] および [**プロセッサ**] パフォーマンス カウンター。</span><span class="sxs-lookup"><span data-stu-id="3f1a1-111">The **CPU** and **Processor** performance counters.</span></span>

<span data-ttu-id="3f1a1-112">ほとんどの展開で、UCWA の CPU 使用率は平均で 15% を下回っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="3f1a1-112">For most deployments, UCWA CPU usage should be below 15 percent on average.</span></span> <span data-ttu-id="3f1a1-113">メモリ使用量は、「 [Lync server 2013 でのサーバーメモリ容量の上限を監視](lync-server-2013-monitoring-for-server-memory-capacity-limits.md)する」で説明されている制限内に収まる必要があります。</span><span class="sxs-lookup"><span data-stu-id="3f1a1-113">Memory usage should fall within the limits described in [Monitoring for server memory capacity limits in Lync Server 2013](lync-server-2013-monitoring-for-server-memory-capacity-limits.md).</span></span>

<span data-ttu-id="3f1a1-114">CPU とメモリの使用状況カウンターに加えて、以下のパフォーマンス カウンターを使用すると、サーバーが要求で過負荷になっていないかどうかを確認するのに役立つ場合があります。</span><span class="sxs-lookup"><span data-stu-id="3f1a1-114">In addition to CPU and memory usage counters, you can use the following performance counters to help determine when a server is overloaded with requests:</span></span>

  - <span data-ttu-id="3f1a1-115">**LS: WEB –調整と認証 \\WEB –要求の合計が処理中で** あることを示します。これは、サーバー上の保留中の web 要求の数を示します。</span><span class="sxs-lookup"><span data-stu-id="3f1a1-115">**LS:WEB – Throttling and Authentication\\WEB – Total Requests in Processing**, which indicates the number of pending web requests on the server.</span></span> <span data-ttu-id="3f1a1-116">このカウンターが1万に達すると、その後の要求は失敗し、"503-サービスを利用できません" というエラーメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3f1a1-116">When this counter reaches 10,000, subsequent requests will fail, with the error message, "503 - Service Unavailable."</span></span>

  - <span data-ttu-id="3f1a1-117">**ASP.NET \\要求はキューに入れら** れます (常に0である必要があります)。</span><span class="sxs-lookup"><span data-stu-id="3f1a1-117">**ASP.NET\\Requests Queued** (should always be zero).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3f1a1-118">これらの値を満たしているか、それ以上の場合は、Web サービスをホストしているコンピューターの CPU、コア数、メモリのサイズが適切に調整されるように、キャパシティ計画を再検討して再計算する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3f1a1-118">If you meet or exceed these values, you should revisit and re-compute your capacity planning for the correct sizing of CPU, number of cores and memory for the computers hosting the Web services.</span></span>



</div>

<span data-ttu-id="3f1a1-119">**Mobility Service (Mcx):**</span><span class="sxs-lookup"><span data-stu-id="3f1a1-119">**For the Mobility Service (Mcx):**</span></span>

  - <span data-ttu-id="3f1a1-120">**Csintmcxapppool** と **csextmcxapppool** ワーカープロセス (インターネットインフォメーションサービス (IIS) マネージャー)。</span><span class="sxs-lookup"><span data-stu-id="3f1a1-120">The **CSIntMcxAppPool** and **CSExtMcxAppPool** worker processes in Internet Information Services (IIS) Manager.</span></span> <span data-ttu-id="3f1a1-121">[**ワーカー プロセス**] ウィンドウで、[**CPU %**] および [**プライベート バイト (KB)**] (メモリ) の列を確認します。</span><span class="sxs-lookup"><span data-stu-id="3f1a1-121">In the **Worker Processes** pane, look at the **CPU %** and **Private Bytes (KB)** (memory) columns.</span></span>

  - <span data-ttu-id="3f1a1-122">[**CPU**] および [**プロセッサ**] パフォーマンス カウンター。</span><span class="sxs-lookup"><span data-stu-id="3f1a1-122">The **CPU** and **Processor** performance counters.</span></span>

<span data-ttu-id="3f1a1-123">ほとんどの展開で、Mobility Service の CPU 使用率は平均で 15% を下回っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="3f1a1-123">For most deployments, Mobility Service CPU usage should be below 15 percent, on average.</span></span> <span data-ttu-id="3f1a1-124">メモリ使用量は、「 [Lync server 2013 でのサーバーメモリ容量の上限を監視](lync-server-2013-monitoring-for-server-memory-capacity-limits.md)する」で説明されている制限内に収まる必要があります。</span><span class="sxs-lookup"><span data-stu-id="3f1a1-124">Memory usage should fall within the limits described in [Monitoring for server memory capacity limits in Lync Server 2013](lync-server-2013-monitoring-for-server-memory-capacity-limits.md).</span></span>

<span data-ttu-id="3f1a1-125">CPU とメモリの使用状況カウンターに加えて、以下の ASP.NET パフォーマンス カウンターを使用すると、サーバーが要求で過負荷になっていないかどうかを確認するのに役立つ場合があります。</span><span class="sxs-lookup"><span data-stu-id="3f1a1-125">In addition to CPU and memory usage counters, you can use the following ASP.NET performance counters to help determine when a server is overloaded with requests:</span></span>

  - <span data-ttu-id="3f1a1-126">**ASP.NET v 2.0.50727 \\現在の要求**: サーバー上の保留中の web 要求の数を示します。</span><span class="sxs-lookup"><span data-stu-id="3f1a1-126">**ASP.NET v2.0.50727\\Requests Current**, which indicates the number of pending web requests on the server.</span></span> <span data-ttu-id="3f1a1-127">このカウンターが5000に達すると、その後の要求は失敗し、"503-サービスを利用できません" というエラーメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3f1a1-127">When this counter reaches 5,000, subsequent requests will fail with the error message, "503 - Service Unavailable."</span></span>

  - <span data-ttu-id="3f1a1-128">**ASP.NET \\要求はキューに入れら** れます (常に0である必要があります)。</span><span class="sxs-lookup"><span data-stu-id="3f1a1-128">**ASP.NET\\Requests Queued** (should always be zero).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3f1a1-129">これらの値を満たしている、または超える場合は、Web サービスをホストしているコンピューターの CPU、コア数、メモリの適切なサイズ変更のために、キャパシティ計画を再検討して再計算する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3f1a1-129">If you meet or exceed these values, you should revisit and recompute your capacity planning for the correct sizing of CPU, number of cores, and memory for the computers hosting the Web services.</span></span>



</div>

<div>

## <a name="see-also"></a><span data-ttu-id="3f1a1-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="3f1a1-130">See Also</span></span>


[<span data-ttu-id="3f1a1-131">Lync Server 2013 でのサーバーメモリ容量の上限を監視する</span><span class="sxs-lookup"><span data-stu-id="3f1a1-131">Monitoring for server memory capacity limits in Lync Server 2013</span></span>](lync-server-2013-monitoring-for-server-memory-capacity-limits.md)  
  

<span data-ttu-id="3f1a1-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3f1a1-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

