---
title: 'Lync Server 2013: フロントエンドサーバーのアップグレードまたは更新'
description: 'Lync Server 2013: フロントエンドサーバーのアップグレードまたは更新。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Upgrade or update Front End Servers
ms:assetid: 20fa39ae-ecfb-4c72-9cc4-8e183d3c752f
ms:mtpsurl: https://technet.microsoft.com/library/JJ204736(v=OCS.15)
ms:contentKeyID: 48183597
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5340ca5549aeff51b275798572573b2c9f017644
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399459"
---
# <a name="upgrade-or-update-front-end-servers-in-lync-server-2013"></a><span data-ttu-id="8a1b0-103">Upgrade or update Front End Servers in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8a1b0-103">Upgrade or update Front End Servers in Lync Server 2013</span></span>

<div data-xmlns="https://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="https://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8a1b0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8a1b0-104">

<span> </span></span></span>

<span data-ttu-id="8a1b0-105">_**最終更新日:** 2013-06-28_</span><span class="sxs-lookup"><span data-stu-id="8a1b0-105">_**Topic Last Modified:** 2013-06-28_</span></span>

<span data-ttu-id="8a1b0-106">Enterprise Edition プールのフロントエンドサーバーは、 *アップグレードドメイン* として編成されています。</span><span class="sxs-lookup"><span data-stu-id="8a1b0-106">The Front End Servers in an Enterprise Edition pool are organized into *upgrade domains*.</span></span> <span data-ttu-id="8a1b0-107">これらは、プール内のフロントエンドサーバーのサブセットです。</span><span class="sxs-lookup"><span data-stu-id="8a1b0-107">These are subsets of Front End Servers in the pool.</span></span> <span data-ttu-id="8a1b0-108">アップグレードドメインは、トポロジビルダーによって自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="8a1b0-108">Upgrade Domains are created automatically by Topology Builder.</span></span>

<span data-ttu-id="8a1b0-109">サーバーをアップグレードする場合は、一度に1つのアップグレードドメインを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a1b0-109">When you upgrade servers, you must do so one Upgrade Domain at a time.</span></span> <span data-ttu-id="8a1b0-110">各サーバーを1つのアップグレードドメインに移動してアップグレードし、それを再起動してから別のアップグレードドメインに移行します。</span><span class="sxs-lookup"><span data-stu-id="8a1b0-110">Bring each Server in one Upgrade Domain down, upgrade it, and then restart it before you move on to another Upgrade Domain.</span></span> <span data-ttu-id="8a1b0-111">これまでにアップグレードしたアップグレードドメインとサーバーを常に把握しておいてください。</span><span class="sxs-lookup"><span data-stu-id="8a1b0-111">Be sure to keep track of which Upgrade Domains and Servers that you have upgraded so far.</span></span> <span data-ttu-id="8a1b0-112">各サーバーをアップグレードする場合は、次のフローチャート図を使用します。</span><span class="sxs-lookup"><span data-stu-id="8a1b0-112">Use the following flowchart diagram when upgrading each server.</span></span>

![フロントエンドサーバーのアップグレードまたは更新](images/upgradeupdatefrontendserverslync2013.png)

<div>

## <a name="to-apply-an-upgrade-to-the-front-end-servers-in-a-pool"></a><span data-ttu-id="8a1b0-114">プール内のフロントエンド サーバーにアップグレードを適用する</span><span class="sxs-lookup"><span data-stu-id="8a1b0-114">To apply an upgrade to the Front End servers in a pool</span></span>

1.  <span data-ttu-id="8a1b0-115">プール内のフロントエンドサーバーで、次のコマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="8a1b0-115">On a Front End Server in the pool, run the following cmdlet:</span></span>
    
    <span data-ttu-id="8a1b0-116">**Get-CsPoolUpgradeReadinessState**</span><span class="sxs-lookup"><span data-stu-id="8a1b0-116">**Get-CsPoolUpgradeReadinessState**</span></span>
    
    <span data-ttu-id="8a1b0-117">*Poolupgradestate* の値が **Busy** の場合は、10分間待ってから、もう一度 **CsPoolUpgradeReadinessState** を試してください。</span><span class="sxs-lookup"><span data-stu-id="8a1b0-117">If the value of *PoolUpgradeState* is **Busy**, wait for 10 minutes, and then try **Get-CsPoolUpgradeReadinessState** again.</span></span> <span data-ttu-id="8a1b0-118">3回以上連続して [ **取り込み中** ] と表示されている場合、それぞれの試行の間に10分待ってから、または **InsufficientActiveFrontEnds** の **poolupgradestate** の結果が表示された場合は、プールに問題があります。</span><span class="sxs-lookup"><span data-stu-id="8a1b0-118">If you see **Busy** for at least three consecutive times, after waiting 10 minutes in between each attempt, or if you see any result of **InsufficientActiveFrontEnds** for **PoolUpgradeState,** then there is an issue with the pool.</span></span> <span data-ttu-id="8a1b0-119">このプールが、障害回復トポロジの別のフロントエンドプールとペアリングされている場合は、プールをバックアッププールにフェールオーバーし、このプール内のサーバーを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a1b0-119">If this pool is paired with another Front End pool in a disaster recovery topology, you should fail the pool over to the backup pool, and then update the servers in this pool.</span></span> <span data-ttu-id="8a1b0-120">詳細については、「 [Lync Server 2013 でのプールのフェールオーバー](lync-server-2013-failing-over-a-pool.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8a1b0-120">For details, see [Failing over a pool in Lync Server 2013](lync-server-2013-failing-over-a-pool.md).</span></span>
    
    <span data-ttu-id="8a1b0-121">*Poolupgradestate* の値の準備が **でき** ている場合は、手順2に進みます。</span><span class="sxs-lookup"><span data-stu-id="8a1b0-121">If the value of *PoolUpgradeState* is **Ready**, go to step 2.</span></span>

2.  <span data-ttu-id="8a1b0-122">**CsPoolUpgradeReadinessState** コマンドレットは、プール内の各アップグレードドメインについての情報と、各アップグレードドメインに含まれるフロントエンドサーバーについても返します。</span><span class="sxs-lookup"><span data-stu-id="8a1b0-122">The **Get-CsPoolUpgradeReadinessState** cmdlet also returns information about each upgrade domain in the pool, and about which Front End Servers are in each upgrade domain.</span></span> <span data-ttu-id="8a1b0-123">アップグレードするサーバーが含まれているアップグレードドメインに対して **ReadyforUpgrade** 値が **True** の場合は、これらのサーバーを現在安全にアップグレードできます。</span><span class="sxs-lookup"><span data-stu-id="8a1b0-123">If the **ReadyforUpgrade** value is **True** for the upgrade domain that contains the server or servers you want to upgrade, you can safely upgrade those servers now.</span></span> <span data-ttu-id="8a1b0-124">そのためには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="8a1b0-124">To do so, do the following:</span></span>
    
    1.  <span data-ttu-id="8a1b0-125">アップグレードするフロントエンドサーバーへの新しい接続を停止するには、コマンドレットを使用し `Stop-CsWindowsService -Graceful -Verbose` ます。</span><span class="sxs-lookup"><span data-stu-id="8a1b0-125">Stop new connections to the Front End Servers you are going to upgrade by using the `Stop-CsWindowsService -Graceful -Verbose` cmdlet.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="8a1b0-126">スケジュールされたサーバーのダウンタイムにサーバーのアップグレードを実行している場合は、次のように、"-<STRONG>正常</STRONG>" パラメーターを指定せずにこのコマンドレットを実行でき<STRONG>ます。</STRONG></span><span class="sxs-lookup"><span data-stu-id="8a1b0-126">If you are performing these server upgrades during a scheduled server downtime, you can run this cmdlet without the ‘-<STRONG>Graceful</STRONG>‘ parameter, as follows: <STRONG>Stop-CsWindowsService</STRONG>.</span></span> <span data-ttu-id="8a1b0-127">これにより、すべての既存のサービスリクエストがいっぱいになるのを待たずに、すぐにサービスが終了します。</span><span class="sxs-lookup"><span data-stu-id="8a1b0-127">This will immediately shut down services, without waiting for all existing service requests to be filled.</span></span>

        
        </div>
    
    2.  <span data-ttu-id="8a1b0-128">このアップグレードドメインに関連付けられているサーバーをアップグレードします。</span><span class="sxs-lookup"><span data-stu-id="8a1b0-128">Upgrade the servers associated with this the Upgrade Domain.</span></span>
    
    3.  <span data-ttu-id="8a1b0-129">サーバーを再起動して、新しい接続を受け入れていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8a1b0-129">Restart the servers, and make sure they are accepting new connections.</span></span>

3.  <span data-ttu-id="8a1b0-130">すべてのフロントエンドサーバーがアップグレードされるまで、プール内の各アップグレードドメインについて、手順1と2を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="8a1b0-130">Repeat Steps 1 and 2 for each other Upgrade Domain in the pool, until all Front End Servers have been upgraded.</span></span>

<span data-ttu-id="8a1b0-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8a1b0-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

