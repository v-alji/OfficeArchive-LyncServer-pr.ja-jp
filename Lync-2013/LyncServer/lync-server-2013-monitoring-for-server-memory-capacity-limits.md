---
title: 'Lync Server 2013: サーバーのメモリ容量の上限を監視する'
description: 'Lync Server 2013: サーバーのメモリ容量の上限を監視します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Monitoring for server memory capacity limits
ms:assetid: 1697ea71-6fcf-480d-b4e9-cd79f94d247e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh689982(v=OCS.15)
ms:contentKeyID: 48183506
ms.date: 12/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6561908af2c8f2f7b5fb9e347cc6247f7ca6642e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425431"
---
# <a name="monitoring-for-server-memory-capacity-limits-in-lync-server-2013"></a><span data-ttu-id="48674-103">Lync Server 2013 でのサーバーメモリ容量の上限を監視する</span><span class="sxs-lookup"><span data-stu-id="48674-103">Monitoring for server memory capacity limits in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="48674-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="48674-104">

<span> </span></span></span>

<span data-ttu-id="48674-105">_**最終更新日:** 2016-12-08_</span><span class="sxs-lookup"><span data-stu-id="48674-105">_**Topic Last Modified:** 2016-12-08_</span></span>

    Some information in this topic pertains to Cumulative Updates for Lync Server 2013: February 2013.

<div>


> [!WARNING]  
> <span data-ttu-id="48674-106">このトピックでは、キャパシティ計画を参照している情報は、Lync 2010 モバイルクライアントとモビリティサービス (Mcx) のみに関連しています。</span><span class="sxs-lookup"><span data-stu-id="48674-106">The information in this topic that refers to Capacity Planning pertains only to Lync 2010 Mobile clients and the Mobility Service (Mcx).</span></span> <span data-ttu-id="48674-107">Lync 2013 モバイルクライアントで使用されるユニファイドコミュニケーション Web API (UCWA) のキャパシティ計画は、Lync Server 2013、計画ツールによって提供されます。</span><span class="sxs-lookup"><span data-stu-id="48674-107">Capacity Planning for the Unified Communications Web API (UCWA), used by the Lync 2013 Mobile clients, is provided by the Lync Server 2013, Planning Tool.</span></span>



</div>

<span data-ttu-id="48674-108">2つのモバイルパフォーマンスカウンターは、現在の使用状況を特定し、Lync Server 2013 Mobility Service (Mcx) のキャパシティを計画し、UCWA のメモリ使用量を監視するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="48674-108">Two mobility performance counters can help you to determine your current usage and help you plan capacity for the Lync Server 2013 Mobility Service (Mcx), as well as to monitor memory usage for UCWA.</span></span> <span data-ttu-id="48674-109">UCWA では、カウンターカテゴリは **LS: WEB – UCWA** です。</span><span class="sxs-lookup"><span data-stu-id="48674-109">For UCWA, the counter category is **LS:WEB – UCWA**.</span></span> <span data-ttu-id="48674-110">モバイルサービス (Mcx) については、カウンターは "カテゴリ **LS: WEB モバイル通信サービス**" の下にあります。</span><span class="sxs-lookup"><span data-stu-id="48674-110">For the Mobility Service (Mcx), the counters are under the category **LS:WEB - Mobile Communication Service**.</span></span> <span data-ttu-id="48674-111">監視するカウンターは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="48674-111">The counters to monitor are:</span></span>

  - <span data-ttu-id="48674-112">**Currently Active Session Count with Active Presence Subscriptions**。これは、UCWA または Mobility Service (Mcx) 経由で登録されたエンドポイントのうち、アクティブなプレゼンス サブスクリプションを持つエンドポイントの現在数 (常時接続されたモバイル ユーザーの数) です。</span><span class="sxs-lookup"><span data-stu-id="48674-112">**Currently Active Session Count with Active Presence Subscriptions**, which is the current number of endpoints registered through UCWA or the Mobility Service (Mcx) that have active presence subscriptions (number of always-connected mobile users)</span></span>

  - <span data-ttu-id="48674-113">**Currently Active Session Count**。これは、UCWA または Mobility Service 経由で登録されたエンドポイントの現在数です。</span><span class="sxs-lookup"><span data-stu-id="48674-113">**Currently Active Session Count**, which is the current number of endpoints registered through UCWA or the Mobility Service</span></span>

<span data-ttu-id="48674-114">**アクティブなセッション数と** 現在アクティブな **セッション数** の差が時間の経過と共に小さい場合は、モバイルデバイスを使用しているデバイス (Android や Nokia モバイルデバイスなど) が常に接続されていることを意味します (mcx のみ)。</span><span class="sxs-lookup"><span data-stu-id="48674-114">If the difference between **Currently Active Session Count with Active Presence Subscriptions** and **Currently Active Session Count** is small over time, this means that most mobile device users have an always-connected device, such as an Android or Nokia mobile device (for Mcx only).</span></span> <span data-ttu-id="48674-115">UCWA 常に接続されたデバイスには、Lync 2013 モバイルクライアントを実行している Apple と Android デバイスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="48674-115">UCWA always-connected devices include Apple and Android devices running Lync 2013 Mobile clients).</span></span> <span data-ttu-id="48674-116">現在アクティブな **セッション数** が **、アクティブなプレゼンスのサブスクリプションによって現在アクティブなセッション数** を超えている場合は、Apple IOS デバイスや Mcx での Windows Phone などのバックグラウンドエンドポイントデバイスを使用しているユーザーが多いことを示します。</span><span class="sxs-lookup"><span data-stu-id="48674-116">If **Currently Active Session Count** is much higher than **Currently Active Session Count with Active Presence Subscriptions**, this indicates that more users are using a background endpoint device, such as an Apple iOS device or Windows Phone under Mcx.</span></span> <span data-ttu-id="48674-117">(Windows Phone は、これとして登録される唯一の Lync 2013 モバイルクライアントです)。</span><span class="sxs-lookup"><span data-stu-id="48674-117">(Windows Phone is the only Lync 2013 Mobile client that will register as this).</span></span>

<span data-ttu-id="48674-118">現在アクティブになっている **セッション数** の上限を設定する必要があります。これには、想定される使用状況、キャパシティ計画の結果、モビリティサービスおよびその他のフロントエンドサーバーカウンターの継続的な監視に基づいて、現在のアクティブなセッション数 **のパフォーマンスカウンター** が使用されます。</span><span class="sxs-lookup"><span data-stu-id="48674-118">You should set a limit on the **Currently Active Session Count with Active Presence Subscriptions** and **Currently Active Session Count** performance counters based on your expected usage, capacity planning results, and ongoing monitoring of Mobility Service and other Front End Server counters.</span></span> <span data-ttu-id="48674-119">制限を設定することで、キャパシティを超えたときにサーバーの容量を評価し、警告を発生させることができるようになります。</span><span class="sxs-lookup"><span data-stu-id="48674-119">The limits you set should enable you to evaluate server capacity and raise alerts when capacity is exceeded.</span></span>

<span data-ttu-id="48674-120">適切な制限を決定するには、まず、モビリティサービスのフロントエンドサーバーで利用可能なメモリ量を決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="48674-120">To determine the appropriate limits, you need to first determine how much memory is available on the Front End Server for the Mobility Service.</span></span> <span data-ttu-id="48674-121">カウンターを監視し、次の式に従って、追加容量の計画が必要な時期を確認します。</span><span class="sxs-lookup"><span data-stu-id="48674-121">Monitor the counters to determine when you need to plan for extra capacity, according to the following formula:</span></span>

<span data-ttu-id="48674-122">Mcx Mobility Service (MB) = 164 + (400 + 134)/1024 \* **現在アクティブなセッション数** (現在のアクティブな \* **セッションカウント** –現在アクティブな **プレゼンスサブスクリプションに** よるアクティブなセッションカウント) 400 が使用されている合計メモリ</span><span class="sxs-lookup"><span data-stu-id="48674-122">Total memory used by the Mcx Mobility Service (MB) = 164 + (400 + 134) / 1024 \* **Currently Active Session Count with Active Presence Subscriptions** + 400 / 1024 \* (**Currently Active Session Count** – **Currently Active Session Count with Active Presence Subscriptions**)</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="48674-123">Microsoft Lync Server 2010 容量計算ツールは、CPU、メモリ、ハードドライブなど、プランナーでサーバーの要件を決定するためのすべての数式で事前に用意されたスプレッドシートです。</span><span class="sxs-lookup"><span data-stu-id="48674-123">The Microsoft Lync Server 2010 Capacity Calculator is a spreadsheet that is prepopulated with all of the formulas that enable a planner to determine what the requirements will be for the servers, including CPU, memory, and hard drive.</span></span> <span data-ttu-id="48674-124">スプレッドシートと関連ドキュメントをダウンロードするには、次の操作を行います。 <A href="https://go.microsoft.com/fwlink/p/?linkid=212657">https://go.microsoft.com/fwlink/p/?LinkID=212657</A></span><span class="sxs-lookup"><span data-stu-id="48674-124">You can download the spreadsheet and an associated document at: <A href="https://go.microsoft.com/fwlink/p/?linkid=212657">https://go.microsoft.com/fwlink/p/?LinkID=212657</A></span></span>



</div>

<span data-ttu-id="48674-125">フロントエンドサーバーには、フェールオーバーの状況でモビリティサービスをサポートするための十分なメモリが必要です。</span><span class="sxs-lookup"><span data-stu-id="48674-125">The Front End Server needs enough available memory to support the Mobility Service in failover situations.</span></span> <span data-ttu-id="48674-126">フロントエンドサーバーで利用可能な現在のメモリを監視するには、 **memory \\ available m** カウンターを使用するか、前に説明した式を使用して、モビリティサービスで使用する必要のあるメモリ量を計画します。</span><span class="sxs-lookup"><span data-stu-id="48674-126">You can monitor the current available memory on the Front End Server by using the **Memory\\Available Mbytes** counter, or by using the equation mentioned earlier, to plan for the amount of memory that you expect the Mobility Service to use.</span></span>

<span data-ttu-id="48674-127">フロントエンドサーバーで利用可能なメモリの量が 1500 MB よりも小さい場合は、モビリティユーザーの想定される数を計画するときに、モビリティサービスをサポートするためにハードウェアを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="48674-127">If the amount of memory available on the Front End Server is lower than 1,500 MB when you plan for the expected number of mobility users, you need to add more hardware to support the Mobility Service.</span></span> <span data-ttu-id="48674-128">詳細については、操作のドキュメントで「 [Lync Server 2013 のパフォーマンスを監視する](lync-server-2013-monitoring-mobility-for-performance.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="48674-128">For more details, see [Monitoring mobility for performance in Lync Server 2013](lync-server-2013-monitoring-mobility-for-performance.md) in the Operations documentation.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="48674-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="48674-129">See Also</span></span>


[<span data-ttu-id="48674-130">Lync Server 2013 でのモバイルパフォーマンスの監視</span><span class="sxs-lookup"><span data-stu-id="48674-130">Monitoring mobility for performance in Lync Server 2013</span></span>](lync-server-2013-monitoring-mobility-for-performance.md)  
  

<span data-ttu-id="48674-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="48674-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

