---
title: 'Lync Server 2013: プールのフェールオーバー'
description: 'Lync Server 2013: プールのフェイルオーバー。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failing over a pool
ms:assetid: 10b13732-bc80-4cb2-a71c-56b1d6cb5bbb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204678(v=OCS.15)
ms:contentKeyID: 48183432
ms.date: 10/10/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 819137c1277c5058f4e5d36ef5dbe71e672e8641
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428266"
---
# <a name="failing-over-a-pool-in-lync-server-2013"></a><span data-ttu-id="7f524-103">Lync Server 2013 でのプールのフェールオーバー</span><span class="sxs-lookup"><span data-stu-id="7f524-103">Failing over a pool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7f524-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7f524-104">

<span> </span></span></span>

<span data-ttu-id="7f524-105">_**最終更新日:** 2014-10-10_</span><span class="sxs-lookup"><span data-stu-id="7f524-105">_**Topic Last Modified:** 2014-10-10_</span></span>

<span data-ttu-id="7f524-106">1つのフロントエンドプールで障害が発生し、フェールオーバーを行う必要がある場合は、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="7f524-106">If a single Front End pool has failed and needs to be failed over, use the following procedure.</span></span> <span data-ttu-id="7f524-107">この手順では、Datacenter1 に Pool1 が含まれており、Pool1 は失敗しています。</span><span class="sxs-lookup"><span data-stu-id="7f524-107">In this procedure, Datacenter1 contains Pool1, and Pool1 has failed.</span></span> <span data-ttu-id="7f524-108">Datacenter2 にある Pool2 にフェイルオーバーしています。</span><span class="sxs-lookup"><span data-stu-id="7f524-108">You are failing over to Pool2 located in Datacenter2.</span></span>

<span data-ttu-id="7f524-109">プールフェールオーバーのほとんどの作業には、必要に応じて、中央管理ストアのフェールオーバーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="7f524-109">Most of the work for the pool failover involves failing over the Central Management store, if it is required.</span></span> <span data-ttu-id="7f524-110">プールのユーザーがフェールオーバーされた場合は、中央管理ストアが機能している必要があるため、これは重要です。</span><span class="sxs-lookup"><span data-stu-id="7f524-110">This is important because the Central Management store must be functional when the pool’s users are failed over.</span></span>

<span data-ttu-id="7f524-111">さらに、フロントエンドプールに障害が発生しても、そのサイトの Edge プールがまだ実行されている場合は、Edge プールが、失敗したプールを次のホッププールとして使用するかどうかを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f524-111">Additionally, if a Front End pool fails but the Edge pool at that site is still running, you must know whether the Edge pool uses the failed pool as a next hop pool.</span></span> <span data-ttu-id="7f524-112">問題が発生した場合は、失敗したフロントエンドプールを使用するようにエッジプールを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f524-112">If it does, you must change the Edge pool to use a different Front End pool before failing over the failed Front End pool.</span></span> <span data-ttu-id="7f524-113">次ホップの設定を変更する方法は、エッジプールと同じサイトのプールを使用するか、または別のサイトを使うかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="7f524-113">How you change the next hop setting depends on whether the Edge will use a pool at the same site as the Edge pool, or a different site.</span></span>

<span data-ttu-id="7f524-114">**エッジプールで、同じサイトの次ホッププールを使用するように設定するには**</span><span class="sxs-lookup"><span data-stu-id="7f524-114">**To Set an Edge Pool to Use a Next Hop Pool at the Same Site**</span></span>

1.  <span data-ttu-id="7f524-115">トポロジビルダーを開き、変更する必要があるエッジプールを右クリックして、[ **プロパティの編集**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f524-115">Open Topology Builder, right-click the Edge pool that needs to be changed, and click **Edit Properties**.</span></span>

2.  <span data-ttu-id="7f524-116">[ **次ホップ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f524-116">Click **Next Hop**.</span></span> <span data-ttu-id="7f524-117">[ **Next ホッププール:** ] ボックスの一覧で、次ホッププールとして機能するプールを選択します。</span><span class="sxs-lookup"><span data-stu-id="7f524-117">From the **Next hop pool:** list, select the pool which will now serve as the next hop pool.</span></span>

3.  <span data-ttu-id="7f524-118">[ **OK**] をクリックして、変更を公開します。</span><span class="sxs-lookup"><span data-stu-id="7f524-118">Click **OK**, and then publish the changes.</span></span>

<span data-ttu-id="7f524-119">**別のサイトで次ホッププールを使用するようにエッジプールを設定するには**</span><span class="sxs-lookup"><span data-stu-id="7f524-119">**To Set an Edge Pool to Use a Next Hop Pool at a Different Site**</span></span>

1.  <span data-ttu-id="7f524-120">Lync Server 管理シェルウィンドウを開いて、次のコマンドレットを入力します。</span><span class="sxs-lookup"><span data-stu-id="7f524-120">Open a Lync Server Management Shell window and type the following cmdlet:</span></span>
    
        Set-CsEdgeServer -Identity EdgeServer:<Edge Server pool FQDN> -Registrar Registrar:<NextHopPoolFQDN>

<span data-ttu-id="7f524-121">**障害が発生したプールをフェイルオーバーするには**</span><span class="sxs-lookup"><span data-stu-id="7f524-121">**To Fail Over a Pool in a Disaster**</span></span>

1.  <span data-ttu-id="7f524-122">Pool2 のフロントエンドサーバーに次のコマンドレットを入力して、中央管理サーバーのホストとなるプールを見つけます。</span><span class="sxs-lookup"><span data-stu-id="7f524-122">Find which pool is the host for the Central Management Server by typing the following cmdlet on a Front End server in Pool2:</span></span>
    
        Invoke-CsManagementServerFailover -Whatif
    
    <span data-ttu-id="7f524-123">このコマンドレットの結果は、現在中央管理サーバーをホストしているプールを示します。</span><span class="sxs-lookup"><span data-stu-id="7f524-123">The results of this cmdlet show which pool currently hosts the Central Management Server.</span></span> <span data-ttu-id="7f524-124">この手順の残りの部分では、このプールを CMS \_ プールと呼びます。</span><span class="sxs-lookup"><span data-stu-id="7f524-124">In the rest of this procedure, this pool is known as CMS\_Pool.</span></span>

2.  <span data-ttu-id="7f524-125">トポロジビルダーを使用して、CMS プールで実行されている Lync Server のバージョンを確認 \_ します。</span><span class="sxs-lookup"><span data-stu-id="7f524-125">Use Topology Builder to find the version of Lync Server running on the CMS\_Pool.</span></span> <span data-ttu-id="7f524-126">Lync Server 2013 を実行している場合は、次のコマンドレットを使用して、Pool 1 のバックアッププールを検索します。</span><span class="sxs-lookup"><span data-stu-id="7f524-126">If it is running Lync Server 2013, use the following cmdlet to find the backup pool of Pool 1.</span></span>
    
        Get-CsPoolBackupRelationship -PoolFQDN <CMS_Pool FQDN>
    
    <span data-ttu-id="7f524-127">バックアッププール \_ をバックアッププールにします。</span><span class="sxs-lookup"><span data-stu-id="7f524-127">Let Backup\_Pool be the backup pool.</span></span>

3.  <span data-ttu-id="7f524-128">次のコマンドレットを使用して、サーバーの全体管理ストアの状態を確認します。</span><span class="sxs-lookup"><span data-stu-id="7f524-128">Check the status of the Central Management store with the following cmdlet:</span></span>
    
        Get-CsManagementStoreReplicationStatus -CentralManagementStoreStatus 
    
    <span data-ttu-id="7f524-129">このコマンドレットでは、ActiveMasterFQDN と ActiveFileTransferAgents の両方が CMS プールの FQDN を指していることを示して \_ います。</span><span class="sxs-lookup"><span data-stu-id="7f524-129">This cmdlet should show that both ActiveMasterFQDN and ActiveFileTransferAgents are pointing to the FQDN of CMS\_Pool.</span></span> <span data-ttu-id="7f524-130">空の場合は、サーバーの全体管理サーバーを利用できないため、フェールオーバーを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f524-130">If they are empty, the Central Management Server is not available and you must fail it over.</span></span>

4.  <span data-ttu-id="7f524-131">中央管理ストアを使用できない場合、または Pool1 で中央管理ストアが実行されている場合 (つまり、失敗したプール)、プールをフェールオーバーする前に、中央管理サーバーをフェールオーバーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f524-131">If the Central Management store is not available or if the Central Management store was running on Pool1 (that is, the pool that has failed), you must fail over the Central Management Server before failing over the pool.</span></span> <span data-ttu-id="7f524-132">Lync Server 2013 を実行しているプールでホストされていた中央管理サーバーをフェールオーバーする必要がある場合は、この手順の手順5のコマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="7f524-132">If you need to fail over the Central Management Server that was hosted on a pool running Lync Server 2013, use the cmdlet in step 5 of this procedure.</span></span> <span data-ttu-id="7f524-133">Lync Server 2010 を実行しているプールでホストされていた中央管理サーバーをフェールオーバーする必要がある場合は、この手順の手順6でコマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="7f524-133">If you need to fail over the Central Management Server that was hosted on a pool running Lync Server 2010, use the cmdlet in step 6 of this procedure.</span></span> <span data-ttu-id="7f524-134">サーバーの全体管理サーバーにフェールオーバーする必要がない場合は、手順7に進んでください。</span><span class="sxs-lookup"><span data-stu-id="7f524-134">If you do not need to fail over the Central Management Server, skip to step 7 of this procedure.</span></span>

5.  <span data-ttu-id="7f524-135">Lync Server 2013 を実行しているプールの中央管理ストアをフェールオーバーするには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="7f524-135">To fail over the Central Management store on a pool running Lync Server 2013, do the following:</span></span>
    
      - <span data-ttu-id="7f524-136">まず、次のように入力して、バックアッププールのどのバックエンドサーバーで \_ 中央管理ストアのプリンシパルインスタンスを実行するかを確認します。</span><span class="sxs-lookup"><span data-stu-id="7f524-136">First, check which Back End Server in Backup\_Pool runs the principal instance of the Central Management store by typing the following:</span></span>
        
            Get-CsDatabaseMirrorState -DatabaseType Centralmgmt -PoolFqdn <Backup_Pool Fqdn>
    
      - <span data-ttu-id="7f524-137">バックアッププールのプライマリバックエンドサーバーがプリンシパルである場合は \_ 、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="7f524-137">If the primary Back End Server in Backup\_Pool is the principal, type:</span></span>
        
            Invoke-CSManagementServerFailover -BackupSQLServerFqdn <Backup_Pool Primary BackEnd Server FQDN> -BackupSQLInstanceName <Backup_Pool Primary SQL Instance Name>
        
        <span data-ttu-id="7f524-138">バックアッププールのミラーバックエンドサーバーがプリンシパルである場合は \_ 、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="7f524-138">If the mirror Back End Server in Backup\_Pool is the principal, type:</span></span>
        
            Invoke-CSManagementServerFailover -MirrorSQLServerFqdn <Backup_Pool Mirror BackEnd Server FQDN> -MirrorSQLInstanceName <Backup_Pool Mirror SQL Instance Name>
    
      - <span data-ttu-id="7f524-139">サーバーの全体のフェールオーバーが完了していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7f524-139">Validate that the Central Management Server failover is complete.</span></span> <span data-ttu-id="7f524-140">次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="7f524-140">Type the following:</span></span>
        
            Get-CsManagementStoreReplicationStatus -CentralManagementStoreStatus 
        
        <span data-ttu-id="7f524-141">ActiveMasterFQDN と ActiveFileTransferAgents の両方がバックアッププールの FQDN を指していることを確認 \_ します。</span><span class="sxs-lookup"><span data-stu-id="7f524-141">Check that both ActiveMasterFQDN and ActiveFileTransferAgents are pointing to the FQDN of Backup\_Pool.</span></span>
    
      - <span data-ttu-id="7f524-142">最後に、次のように入力して、すべてのフロントエンドサーバーのレプリカの状態を確認します。</span><span class="sxs-lookup"><span data-stu-id="7f524-142">Finally, check the replica status for all Front End Servers by typing the following:</span></span>
        
            Get-CsManagementStoreReplicationStatus 
        
        <span data-ttu-id="7f524-143">すべてのレプリカの値が True であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7f524-143">Check that all replicas have a value of True.</span></span>
        
        <span data-ttu-id="7f524-144">この手順の手順7に進みます。</span><span class="sxs-lookup"><span data-stu-id="7f524-144">Skip to step 7 in this procedure.</span></span>

6.  <span data-ttu-id="7f524-145">バックアッププールのバックエンドサーバーに中央管理ストアをインストールし \_ ます。</span><span class="sxs-lookup"><span data-stu-id="7f524-145">Install the Central Management store on the Back End Server of Backup\_Pool.</span></span>
    
      - <span data-ttu-id="7f524-146">最初に、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="7f524-146">First, run the following command:</span></span>
        
        ```PowerShell 
        Install-CsDatabase -CentralManagementDatabase -Clean -SqlServerFqdn <Backup_Pool Back End Server FQDN> -SqlInstanceName rtc  
        ```
    
      - <span data-ttu-id="7f524-147">バックアッププールのいずれかのフロントエンドサーバーで次のコマンドを実行して、 \_ 中央管理ストアの移動を強制します。</span><span class="sxs-lookup"><span data-stu-id="7f524-147">Run the next command on one of the Front End Servers of Backup\_Pool to force the move of the Central Management store:</span></span>
        
            Move-CsManagementServer -ConfigurationFileName c:\CsConfigurationFile.zip -LisConfigurationFileName c:\CsLisConfigurationFile.zip -Force 
    
      - <span data-ttu-id="7f524-148">移動が完了したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="7f524-148">Validate the move is complete:</span></span>
        
            Get-CsManagementStoreReplicationStatus -CentralManagementStoreStatus 
        
        <span data-ttu-id="7f524-149">ActiveMasterFQDN と ActiveFileTransferAgents の両方がバックアッププールの FQDN を指していることを確認 \_ します。</span><span class="sxs-lookup"><span data-stu-id="7f524-149">Check that both ActiveMasterFQDN and ActiveFileTransferAgents are pointing to the FQDN of Backup\_Pool.</span></span>
    
      - <span data-ttu-id="7f524-150">次のように入力して、すべてのフロントエンドサーバーのレプリカの状態を確認します。</span><span class="sxs-lookup"><span data-stu-id="7f524-150">Check the replica status for all Front End Servers by typing the following:</span></span>
        
            Get-CsManagementStoreReplicationStatus 
        
        <span data-ttu-id="7f524-151">すべてのレプリカの値が True であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7f524-151">Check that all replicas have a value of True.</span></span>
    
      - <span data-ttu-id="7f524-152">中央管理サーバーサービスを、バックアッププールのフロントエンドサーバーの残りの部分にインストールし \_ ます。</span><span class="sxs-lookup"><span data-stu-id="7f524-152">Install the Central Management Server service on the rest of the Front End Servers in Backup\_Pool.</span></span> <span data-ttu-id="7f524-153">この操作を行うには、この手順の最初に中央管理ストアを強制するときに使用したものを除き、すべてのフロントエンドサーバーで次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="7f524-153">To do so, run the following command on all the Front End Servers, except the one you used when forcing the Central Management store move earlier in this procedure:</span></span>
        
            Bootstrapper /Setup 

7.  <span data-ttu-id="7f524-154">Lync Server 管理シェルウィンドウで次のコマンドレットを実行して、Pool1 から Pool2 にユーザーをフェールオーバーします。</span><span class="sxs-lookup"><span data-stu-id="7f524-154">Fail over the users from Pool1 to Pool2 by running the following cmdlet in a Lync Server Management Shell window:</span></span>
    
        Invoke-CsPoolFailover -PoolFQDN <Pool1 FQDN> -DisasterMode -Verbose
    
    <span data-ttu-id="7f524-155">この手順の前の部分で実行した手順では、全体管理ストアの状態を確認する必要があるため、中央管理ストアはまだ完全にフェールオーバーしていないため、このコマンドレットは失敗する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7f524-155">Because the steps taken in the previous parts of this procedure to check the Central Management store status are not universal, there is still a chance this cmdlet will fail because the Central Management store is not yet fully failed over.</span></span> <span data-ttu-id="7f524-156">この場合は、表示されるエラーメッセージに基づいて、中央管理ストアを修正し、このコマンドレットをもう一度実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f524-156">In this case, you must fix the Central Management store based on the error messages that you see, and then run this cmdlet again.</span></span>
    
    <span data-ttu-id="7f524-157">次のエラーメッセージが表示された場合は、プールをフェールオーバーする前に、このサイトの Edge プールを別のホップとして使用するように変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f524-157">If you see the following error message, then you need to change the Edge pool at this site to use a different pool as its next hop before failing over the pool.</span></span> <span data-ttu-id="7f524-158">詳細については、このトピックの最初の手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7f524-158">For details, see the procedures at the beginning of this topic.</span></span>
    
        Invoke-CsPoolFailOver : This Front-end pool "pool1.contoso.com" is specified in
        topology as the next hop for the Edge server. Failing over this pool may cause External
        access/Federation/Split-domain/XMPP features to stop working. Please use Topology Builder to
        change the Edge internal next hop setting to point to a different Front-end pool,  before you
        proceed.

<span data-ttu-id="7f524-159"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7f524-159"></div>

<span> </span>

</div>

</div>

</span></span></div>

