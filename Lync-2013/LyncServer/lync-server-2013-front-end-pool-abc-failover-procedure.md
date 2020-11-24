---
title: 'Lync Server 2013: フロントエンド プール ABC フェールオーバーの手順'
description: 'Lync Server 2013: フロントエンドプール ABC フェールオーバー手順。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Front End pool ABC failover procedure
ms:assetid: 67763ad3-6796-45eb-a486-901f21ac1a95
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945635(v=OCS.15)
ms:contentKeyID: 51541486
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b86f196d53afdc1dcad6fe41191c2aa1582f717e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399135"
---
# <a name="front-end-pool-abc-failover-procedure-in-lync-server-2013"></a><span data-ttu-id="8bb93-103">Lync Server 2013 フロントエンド プール ABC フェールオーバーの手順</span><span class="sxs-lookup"><span data-stu-id="8bb93-103">Front End pool ABC failover procedure in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8bb93-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8bb93-104">

<span> </span></span></span>

<span data-ttu-id="8bb93-105">_**最終更新日:** 2014-05-22_</span><span class="sxs-lookup"><span data-stu-id="8bb93-105">_**Topic Last Modified:** 2014-05-22_</span></span>

<span data-ttu-id="8bb93-106">次の手順を使用して、ABC フェールオーバーの手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8bb93-106">Use the following steps to perform the ABC failover procedure.</span></span> <span data-ttu-id="8bb93-107">この手順では、各手順の概要と、各手順で実行されるコマンドとコマンドレットについて説明します。</span><span class="sxs-lookup"><span data-stu-id="8bb93-107">This procedure contains a high-level description of each step, followed by commands and cmdlets to be run for each step.</span></span>

<span data-ttu-id="8bb93-108">コマンドレットを実行するには、[管理者として実行] を使用して、Lync Server 管理シェルを開きます。</span><span class="sxs-lookup"><span data-stu-id="8bb93-108">To run the cmdlets, open a Lync Server Management Shell using Run as Administrator.</span></span>

<div>

## <a name="to-perform-an-abc-failover"></a><span data-ttu-id="8bb93-109">ABC フェールオーバーを実行するには</span><span class="sxs-lookup"><span data-stu-id="8bb93-109">To Perform an ABC Failover</span></span>

1.  <span data-ttu-id="8bb93-110">プール A がセントラル管理サーバー (CMS) のホストであるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="8bb93-110">Check whether the pool A is the host for the Central Management Server (CMS).</span></span>
    
      - <span data-ttu-id="8bb93-111">次のコマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="8bb93-111">Run the following cmdlet:</span></span>
        
            Get-CsService -CentralManagement
        
        <span data-ttu-id="8bb93-112">Active CMS の Id フィールドが Pool A の完全修飾ドメイン名 (FQDN) をポイントしている場合は、この手順の手順2と3を使用して、最初に中央管理サーバーをフェールオーバーします。</span><span class="sxs-lookup"><span data-stu-id="8bb93-112">If the Identity field of the active CMS points to the fully qualified domain name (FQDN) of Pool A, then you use steps 2 and 3 of this procedure to fail over the Central Management Server first.</span></span> <span data-ttu-id="8bb93-113">それ以外の場合は、手順4に進みます。</span><span class="sxs-lookup"><span data-stu-id="8bb93-113">Otherwise, skip to step 4.</span></span>

2.  <span data-ttu-id="8bb93-114">次のコマンドレットを実行して、CMS を障害復旧モードでプール B にフェールオーバーします。</span><span class="sxs-lookup"><span data-stu-id="8bb93-114">Fail over the CMS to Pool B in disaster recovery mode by running the following cmdlet:</span></span>
    
        Invoke-CsManagementServerFailover -BackupSqlServerFqdn <Pool B BE FQDN> -BackupSqlInstanceName <Pool B BE instance name> [-BackupMirrorSqlServerFqdn <Pool B Mirror BE FQDN> -BackupMirrorSqlInstanceName <Pool B Mirror BE Instance name>] -Force -Verbose
    
    <span data-ttu-id="8bb93-115">この操作を行った後、回復性を強化するために、CMS を pool B から既存のペアリングされた別のプールに移動することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="8bb93-115">After you do this, we recommend that you move the CMS from pool B to another existing paired pool for extra resiliency.</span></span> <span data-ttu-id="8bb93-116">詳細については、「 [CsManagementServer](https://docs.microsoft.com/powershell/module/skype/Move-CsManagementServer)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8bb93-116">For details, see [Move-CsManagementServer](https://docs.microsoft.com/powershell/module/skype/Move-CsManagementServer)..</span></span>

3.  <span data-ttu-id="8bb93-117">Pool A に CMS が含まれている場合、プール A から pool B の LIS データベース (Lis) に LIS 構成をインポートします。</span><span class="sxs-lookup"><span data-stu-id="8bb93-117">If Pool A contains CMS, import the LIS configuration from pool A into pool B’s LIS database (Lis.mdf).</span></span> <span data-ttu-id="8bb93-118">これは、LIS データを定期的にバックアップしている場合にのみ機能します。</span><span class="sxs-lookup"><span data-stu-id="8bb93-118">This will work only if you have been backing up LIS data on a regular basis.</span></span> <span data-ttu-id="8bb93-119">LIS 構成をインポートするには、次のコマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="8bb93-119">To import the LIS configuration, run the following cmdlets:</span></span>
    
        Import-CsLisConfiguration -FileName <String> 
        Publish-CsLisConfiguration

4.  <span data-ttu-id="8bb93-120">バックアップされた Lync Server 応答グループサービスワークフローをプール A から pool B にインポートします。</span><span class="sxs-lookup"><span data-stu-id="8bb93-120">Import backed-up Lync Server Response Group service workflows from pool A into pool B.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="8bb93-121">現在、 <STRONG>Import-CsRgsConfiguration</STRONG> コマンドレットでは、pool a のキューとワークフロー名が、プール B のキューとワークフロー名と異なる必要があります。名前が異なる場合は、 <STRONG>import-CsRgsConfiguration</STRONG> コマンドレットを実行しているときにエラーが発生します。また、キューとワークフローは、 <STRONG>Import-CsRgsConfiguration</STRONG> コマンドレットを続行する前に、プール B で名前を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8bb93-121">Currently, the <STRONG>Import-CsRgsConfiguration</STRONG> cmdlet requires that the queue and workflow names on pool A are distinct from the queue and workflow names on pool B. If the names are not distinct, you will get an error when running the <STRONG>Import-CsRgsConfiguration</STRONG> cmdlet, and the queues and workflows will need to be renamed in pool B before proceeding with <STRONG>Import-CsRgsConfiguration</STRONG> cmdlet.</span></span>

    
    </div>
    
    <span data-ttu-id="8bb93-122">[プール A] から [プール B] に応答グループの構成をインポートするには、2つのオプションがあります。どちらのオプションを使うかは、pool B のアプリケーションレベルの設定をプール A のアプリケーションレベルの設定で上書きするかどうかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="8bb93-122">You have two options for importing the Response Group configuration from pool A to pool B. Which option you use depends on whether you want to overwrite the application-level settings of pool B with the application-level settings in pool A.</span></span>
    
      - <span data-ttu-id="8bb93-123">プール B の設定を上書きする場合は、 **Replaceexistingsettings** オプションを使用して、 **Import-CsRgsConfiguration** コマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="8bb93-123">If you want to overwrite the Pool B settings, run the **Import-CsRgsConfiguration** cmdlet with the **ReplaceExistingSettings** option:</span></span>
        
            Import-CsRgsConfiguration -Destination "service:ApplicationServer:<Pool B FQDN>" -FileName "C:\RgsExportPrimary.zip"  -ReplaceExistingRgsSettings
    
      - <span data-ttu-id="8bb93-124">プール B の設定を上書きしない場合は、 **Replaceexistingsettings** オプションを指定せずに、 **Import-CsRgsConfiguration** コマンドレットを使います。</span><span class="sxs-lookup"><span data-stu-id="8bb93-124">If you do not want to overwrite the Pool B settings, use the **Import-CsRgsConfiguration** cmdlet without the **ReplaceExistingSettings** option.</span></span>
        
            Import-CsRgsConfiguration -Destination "service:ApplicationServer:<Pool B FQDN>" -FileName "C:\RgsExportPrimary.zip"
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="8bb93-125">バックアッププール (プール B) のアプリケーションレベルの設定をプライマリプール (プール A) の設定で上書きしないように注意してください。この場合、応答グループアプリケーションはプールごとに1つのアプリケーションレベルの設定しか保存できないため、プール a のアプリケーションレベルの設定は失われます。</span><span class="sxs-lookup"><span data-stu-id="8bb93-125">Keep in mind that if you do not want to overwrite the application-level settings of the backup pool (pool B) with the settings of the primary pool (pool A), pool A’s application-level settings will be lost if pool A is lost, because the Response Group application can store only one set of application-level settings per pool.</span></span> <span data-ttu-id="8bb93-126">Pool C を展開してプール A を置き換える場合は、既定の音楽保留オーディオファイルなどのアプリケーションレベルの設定を再構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8bb93-126">When pool C is deployed to replace pool A, the application-level settings must be reconfigured, including the default music-on-hold audio file.</span></span>

    
    </div>

5.  <span data-ttu-id="8bb93-127">インポートされた応答グループを表示するために、次のコマンドレットを実行して、応答グループの構成インポートが正常に完了したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="8bb93-127">Verify that the Response Group configuration import was successful by running the following cmdlets to display the imported response groups.</span></span> <span data-ttu-id="8bb93-128">インポートされた応答グループは、引き続き pool A によって所有されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="8bb93-128">Note that the imported response groups are still owned by pool A.</span></span>
    
        Get-CsRgsWorkflow -Identity "service:ApplicationServer:<Pool B FQDN>" -Owner "service:ApplicationServer:<Pool A FQDN>"
        
        Get-CsRgsQueue -Identity "service:ApplicationServer:<Pool B FQDN>" -Owner "service:ApplicationServer:<Pool A FQDN>"
        
        Get-CsRgsAgentGroup -Identity "service:ApplicationServer:<Pool B FQDN>" -Owner "service:ApplicationServer:<Pool A FQDN>"

6.  <span data-ttu-id="8bb93-129">未割り当て番号については、選択したアナウンスメントサービスとして "お知らせ" を使用している、割り当てられていない番号範囲をプール A から pool B に移動します。目的:</span><span class="sxs-lookup"><span data-stu-id="8bb93-129">For Unassigned Numbers, move the Unassigned Number ranges that are using "Announcement" as the selected announcement service from pool A to pool B. To do so:</span></span>
    
      - <span data-ttu-id="8bb93-130">プール B のプール A に展開されたすべてのアナウンスを再作成します。プール A でお知らせを展開するときにオーディオファイルが使用されていた場合、これらのファイルはプール B でアナウンスを再作成するために必要です。Pool B でお知らせを再作成するには、 **新しい-CsAnnouncement** コマンドレットを使って、プール b を親サービスとして使用します。</span><span class="sxs-lookup"><span data-stu-id="8bb93-130">Re-create all announcements that were deployed in pool A on pool B. If any audio files were used when deploying the announcements in pool A, these files will be needed to re-create the announcements in pool B. To re-create the announcements in pool B, use the **New-CsAnnouncement** cmdlets, with pool B as the Parent service.</span></span>
    
      - <span data-ttu-id="8bb93-131">プール A のアナウンスをターゲットとしている未使用のすべての番号範囲を、プール B の新しく展開されたアナウンスに再ターゲットします。プール A のアナウンスのターゲットとして、次のコマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="8bb93-131">Retarget all the Unassigned Number ranges that are targeting an announcement in pool A to the newly deployed announcements in pool B. Run the following cmdlet for every Unassigned Number range targeting an announcement of pool A:</span></span>
        
            Set-CsUnassignedNumber -Identity "<Range Name>" -AnnouncementService "<Pool B FQDN>" -AnnouncementName "<New Announcement in pool B>"
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="8bb93-132">この手順は、選択したアナウンスメントサービスとして "Exchange UM" を使用している、割り当てられていない番号範囲には必要ありません。</span><span class="sxs-lookup"><span data-stu-id="8bb93-132">This step is not required for unassigned number ranges that use "Exchange UM" as the selected announcement service.</span></span>

    
    </div>

7.  <span data-ttu-id="8bb93-133">次のコマンドレットを実行して、障害回復 (DR) モードでプール A をプール B にフェールオーバーします。</span><span class="sxs-lookup"><span data-stu-id="8bb93-133">Fail over Pool A to Pool B in Disaster Recovery (DR) mode, by running the following cmdlet:</span></span>
    
        Invoke-CsPoolFailover -PoolFqdn <Pool A FQDN> -DisasterMode

8.  <span data-ttu-id="8bb93-134">プール c をビルドしますが、プール C ではサービスを開始しないでください。</span><span class="sxs-lookup"><span data-stu-id="8bb93-134">Build pool C, but do not start any services on pool C.</span></span>
    
    <span data-ttu-id="8bb93-135">この手順は、手順5と6を同時に実行することができます。</span><span class="sxs-lookup"><span data-stu-id="8bb93-135">Note that this step can be carried out concurrently with steps 5 and 6.</span></span>

9.  <span data-ttu-id="8bb93-136">次のコマンドレットを実行して、プール A をホームにしているユーザーをプール C に強制的に移動します。</span><span class="sxs-lookup"><span data-stu-id="8bb93-136">Force users homed on pool A to move to pool C by running the following cmdlet:</span></span>
    
        Get-csuser -Filter {RegistrarPool -eq "<Pool A FQDN>"} | Move-CsUser -Target <Pool C FQDN> -Force
    
    <span data-ttu-id="8bb93-137">この時点で、プール A をホームにしているユーザーは、サービスの停止を経験し始めます。</span><span class="sxs-lookup"><span data-stu-id="8bb93-137">At this point, users homed on pool A will begin to experience a service outage.</span></span> <span data-ttu-id="8bb93-138">この停止は、手順16まで継続され、プール C ではサービスが開始されます。</span><span class="sxs-lookup"><span data-stu-id="8bb93-138">This outage will continue until step 16, at which point services are started on pool C.</span></span>

10. <span data-ttu-id="8bb93-139">次のコマンドレットを実行して、pool A の会議ディレクトリをプール C に強制的に移動させます。</span><span class="sxs-lookup"><span data-stu-id="8bb93-139">Force the conference directory of pool A to move to pool C by running the following cmdlet:</span></span>
    
        Move-CsConferenceDirectory -Identity <Conference Directory ID of Pool A> -TargetPool <Pool C FQDN> -Force

11. <span data-ttu-id="8bb93-140">次のコマンドレットを実行して、電話会議の自動応答 (CAA を) の連絡先オブジェクトをプール A からプール C に強制的に移動します。</span><span class="sxs-lookup"><span data-stu-id="8bb93-140">Force the Conference Auto Attendant (CAA) Contact Object to move from pool A to pool C by running the following cmdlet:</span></span>
    
        Move-csApplicationEndpoint -Identity "<Pool A CAA Uri>" -targetApplicationPool <Pool C FQDN> -force

12. <span data-ttu-id="8bb93-141">会議コンテンツを pool B から pool C にコピーします。</span><span class="sxs-lookup"><span data-stu-id="8bb93-141">Copy conference content from pool B to pool C.</span></span>

13. <span data-ttu-id="8bb93-142">プール B からユーザーデータをエクスポートし、次のコマンドレットを実行してユーザーデータを pool C にインポートします。</span><span class="sxs-lookup"><span data-stu-id="8bb93-142">Export user data from pool B and import the user data into pool C by running the following cmdlets:</span></span>
    
        Export-CsUserData -PoolFqdn <Pool B Fqdn> -FileName <String>
        Import-CsUserData -PoolFqdn <Pool C Fqdn> -FileName <String>

14. <span data-ttu-id="8bb93-143">バックアップされた通話を復元します。プール A からプール C へのアプリケーションデータの割り当てと、プール A のプール C へのコールパーク軌道の範囲の割り当てを行います。</span><span class="sxs-lookup"><span data-stu-id="8bb93-143">Restore backed-up Call Park application data from pool A into pool C and assign the Call Park orbit ranges of pool A to pool C.</span></span>
    
      - <span data-ttu-id="8bb93-144">通話パークは、Lync Server コントロールパネルまたは Lync Server 管理シェルを使用して、プール A の範囲をプール C に再割り当てすることができます。</span><span class="sxs-lookup"><span data-stu-id="8bb93-144">You can reassign a Call Park orbit range of pool A to pool C either through the Lync Server Control Panel or the Lync Server Management Shell.</span></span> <span data-ttu-id="8bb93-145">Lync Server 管理シェルで、pool A に割り当てられているすべての通話パークの範囲に対して、次のコマンドレットを実行します (Id パラメーターは、pool A に属しているコールパークの範囲を参照していることに注意してください)。</span><span class="sxs-lookup"><span data-stu-id="8bb93-145">For the Lync Server Management Shell, run the following cmdlet for every Call Park orbit range assigned to pool A (note that the Identity parameter refers to the Call Park Orbit Ranges that belong to pool A):</span></span>
        
            Set-CsCallParkOrbit -Identity "<Call Park Orbit Identity>" -CallParkService "service:ApplicationServer:<Pool C FQDN>"
    
      - <span data-ttu-id="8bb93-146">カスタマイズした音楽の保留がプール A のコールパーク用に構成されている場合は、プール C で、カスタマイズした音楽の保留中のファイルを復元します。</span><span class="sxs-lookup"><span data-stu-id="8bb93-146">If a customized music-on-hold has been configured for Call Park in pool A, restore the Call Park customized music-on-hold file in pool C.</span></span>
        
            Xcopy <Source> <Destination: Pool C CPS File Store Path>
        
        <span data-ttu-id="8bb93-147">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="8bb93-147">For example:</span></span>
        
            Xcopy "Source Path" "<Pool C File Store Path>\OcsFileStore\coX-ApplicationServer-X\AppServerFiles\CPS\"
    
      - <span data-ttu-id="8bb93-148">最後に、 **CsCpsConfiguration** コマンドレットを使用して、プール C のコールパーク設定を再設定します。</span><span class="sxs-lookup"><span data-stu-id="8bb93-148">Finally, reconfigure the Call Park settings on pool C by using the **Set-CsCpsConfiguration** cmdlet.</span></span> <span data-ttu-id="8bb93-149">コールパークアプリケーションには、1つのプールに1セットの設定と1つのカスタマイズされた音楽オンホールドオーディオファイルのみを保存できます。これらの設定は、障害が発生したときにバックアップまたは保持されません。</span><span class="sxs-lookup"><span data-stu-id="8bb93-149">The Call Park application can store only one set of settings and one customized music-on-hold audio file per pool, and these settings are not backed up or preserved in the event of a disaster.</span></span>

15. <span data-ttu-id="8bb93-150">常設チャットの next-hop プールがプール A を指している場合は、次ホップサーバーがプール C をポイントするようにトポロジの変更を加えて公開します。</span><span class="sxs-lookup"><span data-stu-id="8bb93-150">If the next hop pool for Persistent Chat is pointing to pool A, make and publish topology changes so that the next hop server points to pool C.</span></span>
    
      - <span data-ttu-id="8bb93-151">トポロジービルダーで、次ホップとしてプール C をポイントするように、常設チャットプールを変更します。</span><span class="sxs-lookup"><span data-stu-id="8bb93-151">In Topology Builder, change the Persistent Chat pool to point to Pool C as its next hop.</span></span> <span data-ttu-id="8bb93-152">そのためには、常設チャットプールを右クリックし、[ **全般** ] タブをクリックして、[ **次ホッププール**] にプール C の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="8bb93-152">To do so, right-click on the Persistent Chat pool, then click the **General** tab, and then type the name of Pool C in **Next Hop Pool**.</span></span>
    
      - <span data-ttu-id="8bb93-153">次のコマンドレットを実行して、プール C でサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="8bb93-153">Start services on pool C by running the following cmdlet:</span></span>
        
            Start-csWindowsService
    
    <span data-ttu-id="8bb93-154">この時点では、サービスの停止が、元々プール A に所属していたユーザーによって終了します。</span><span class="sxs-lookup"><span data-stu-id="8bb93-154">At this point, the service outage ends for users originally homed on pool A.</span></span>

16. <span data-ttu-id="8bb93-155">次のコマンドレットを実行して、プール A によって所有されているプール B から、プール C にインポートして Lync Server 応答グループサービスワークフローをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="8bb93-155">Export Lync Server Response Group service workflows from pool B owned by pool A for import into pool C by running the following cmdlet:</span></span>
    
        Export-CsRgsConfiguration -Source "service:ApplicationServer:<Pool B FQDN>" -Owner "service:ApplicationServer:<Pool A FQDN>" -FileName "C:\RgsExportPrimaryUpdated.zip" 

17. <span data-ttu-id="8bb93-156">プール B からプール C に Lync Server 応答グループサービスワークフローをインポートします。</span><span class="sxs-lookup"><span data-stu-id="8bb93-156">Import Lync Server Response Group service workflows into pool C from pool B.</span></span>
    
    <span data-ttu-id="8bb93-157">[プール B] から [プール C] に応答グループの構成をインポートするには、2つのオプションがあります。どちらのオプションを使用するかは、プール C のアプリケーションレベルの設定をプール B のアプリケーションレベルの設定で上書きするかどうかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="8bb93-157">You have two options are for importing the Response Group configuration from pool B to pool C. Which option you use depends on whether you want to overwrite the application-level settings of pool C with the application-level settings in pool B.</span></span>
    
      - <span data-ttu-id="8bb93-158">プール C の設定を上書きする場合は、 **Replaceexistingsettings** オプションを指定して、 **Import-CsRgsConfiguration** コマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="8bb93-158">If you want to overwrite the Pool C settings, run the **Import-CsRgsConfiguration** cmdlet with the **ReplaceExistingSettings** option:</span></span>
        
            Import-CsRgsConfiguration -Destination "service:ApplicationServer:<Pool C FQDN>" -FileName "C:\RgsExportPrimary.zip"  -ReplaceExistingRgsSettings
    
      - <span data-ttu-id="8bb93-159">プール C の設定を上書きしない場合は、 **Replaceexistingsettings** オプションを指定せずに、 **Import-CsRgsConfiguration** コマンドレットを使います。</span><span class="sxs-lookup"><span data-stu-id="8bb93-159">If you do not want to overwrite the Pool C settings, use the **Import-CsRgsConfiguration** cmdlet without the **ReplaceExistingSettings** option.</span></span>
        
            Import-CsRgsConfiguration -Destination "service:ApplicationServer:<Pool B FQDN>" -FileName "C:\RgsExportPrimary.zip"
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="8bb93-160">プール C のアプリケーションレベルの設定をバックアッププール (プール B) の設定で上書きしないように注意してください。応答グループのアプリケーションは、プールごとに1つのアプリケーションレベルの設定しか保存できないため、プール B のアプリケーションレベルの設定は失われます。</span><span class="sxs-lookup"><span data-stu-id="8bb93-160">Keep in mind that if you do not want to overwrite the application-level settings of Pool C with the settings of the backup pool (pool B), pool B’s application-level settings will be lost because the Response Group application can store only one set of application-level settings per pool.</span></span>

    
    </div>

18. <span data-ttu-id="8bb93-161">プール C にインポートされた応答グループを表示するために、次のコマンドレットを実行して、応答グループの構成インポートが正常に完了したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="8bb93-161">Verify that the Response Group configuration import was successful by running the following cmdlets to display the response groups that have been imported to Pool C.</span></span>
    
        Get-CsRgsWorkflow -Identity "service:ApplicationServer:<Pool C FQDN>" -ShowAll
         Get-CsRgsQueue -Identity "service:ApplicationServer:<Pool C FQDN>" -ShowAll
        Get-CsRgsAgentGroup -Identity "service:ApplicationServer:<Pool C FQDN>" -ShowAll

19. <span data-ttu-id="8bb93-162">インポートした構成がプール C で確認されたら、プライマリプールによって所有されている応答グループを pool B から削除します。これにより、応答グループのダウンタイムを最小限に抑えることができます。</span><span class="sxs-lookup"><span data-stu-id="8bb93-162">When the imported configuration has been verified in pool C, remove the response groups owned by the primary pool from pool B. This will minimize the downtime of the response groups.</span></span>
    
    <span data-ttu-id="8bb93-163">この手順では、エクスポートされた構成で新しいファイルを作成し、そのファイルを pool B から削除します。</span><span class="sxs-lookup"><span data-stu-id="8bb93-163">This step creates a new file with the exported configuration, and then removes the file from pool B.</span></span>
    
        Export-CsRgsConfiguration -Source "service:ApplicationServer:<Pool B FQDN>" -Owner "service:ApplicationServer:<Pool A FQDN>" -FileName "C:\RgsExportPrimaryUpdated.zip" -RemoveExportedConfiguration

20. <span data-ttu-id="8bb93-164">プール A からプール B に移動された割り当てられていない番号範囲に移動します。</span><span class="sxs-lookup"><span data-stu-id="8bb93-164">Move to pool C the Unassigned Number ranges that were moved from pool A to pool B.</span></span>
    
      - <span data-ttu-id="8bb93-165">プール B のプール A から再作成されたすべてのアナウンスをプール C で再作成します。移動するアナウンスの展開時にオーディオファイルが使用されていた場合は、これらのファイルを使用して、プール C でアナウンスを再作成する必要があります。プール C でお知らせを再作成するには、 **新しい-CsAnnouncement** コマンドレットを親サービスとしてプール c を使用して使います。</span><span class="sxs-lookup"><span data-stu-id="8bb93-165">Re-create in pool C all announcements that were re-created from pool A in pool B. If any audio files were used when deploying the announcements to be moved, you will need to use these files to re-create the announcements in pool C. To re-create the announcements in pool C, use the **New-CsAnnouncement** cmdlets, with pool C as the Parent service.</span></span>
    
      - <span data-ttu-id="8bb93-166">Pool A から pool B に再ターゲットされたすべての未使用の番号範囲に対して、グループを解除します。再ターゲットとする必要がある、未使用のすべての番号範囲に対して次のコマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="8bb93-166">Retarget to pool C all the unassigned number ranges that were retargeted from pool A to pool B. Run the following cmdlet for every Unassigned Number range that needs to be retargeted:</span></span>
        
            Set-CsUnassignedNumber -Identity "<Range Name>" -AnnouncementService "<Pool C FQDN>" -AnnouncementName "<New Announcement in pool C>"
    
      - <span data-ttu-id="8bb93-167">省略プール B から削除されたお知らせ (プール B で使用されていない場合は、プール C で再作成したアナウンス)。お知らせを削除するには、" **CsAnnouncement の削除** " コマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="8bb93-167">(Optional) Remove from pool B the announcements that were re-created in pool C if they are no longer in use in pool B. To remove announcements, use the **Remove-CsAnnouncement** cmdlet.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="8bb93-168">この手順は、"Exchange UM" をアナウンスメントサービスとして使用する、割り当てられていない番号範囲には必要ありません。</span><span class="sxs-lookup"><span data-stu-id="8bb93-168">This step is not required for unassigned number ranges that use "Exchange UM" as the announcement service.</span></span>

        
        </div>

21. <span data-ttu-id="8bb93-169">次のコマンドレットを実行して、プール B のプール A のユーザーデータをクリーンアップします。</span><span class="sxs-lookup"><span data-stu-id="8bb93-169">Clean up user data of pool A in pool B by running the following cmdlet:</span></span>
    
        Remove-CsUserStoreBackupData -PoolFqdn <Pool B FQDN> -Verbose

22. <span data-ttu-id="8bb93-170">トポロジービルダーで次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="8bb93-170">Do the following in Topology Builder:</span></span>
    
      - <span data-ttu-id="8bb93-171">プール b とプール C をペアリング解除します。次に、トポロジからプール A を削除して公開します。</span><span class="sxs-lookup"><span data-stu-id="8bb93-171">Unpair pool A and pool B. Pair pool B and pool C. Then remove Pool A from the topology and publish it.</span></span> <span data-ttu-id="8bb93-172">これを行うには、以下のようにします。</span><span class="sxs-lookup"><span data-stu-id="8bb93-172">To do so:</span></span>
        
          - <span data-ttu-id="8bb93-173">[トポロジビルダー] で、[Pool B] を右クリックし、[ **プロパティの編集**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8bb93-173">In Topology Builder, right-click on Pool B, and then click **Edit Properties**.</span></span>
        
          - <span data-ttu-id="8bb93-174">左側のウィンドウで [ **復元性** ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8bb93-174">Click **Resiliency** in the left pane.</span></span>
        
          - <span data-ttu-id="8bb93-175">[ **関連付けられたバックアッププール**] の下のボックスで、[pool C] を選びます。関連付けられているバックアッププールの選択ボックスには、最初にプール a が表示されます。これは、pool B がこのプールと関連付けられているためです。</span><span class="sxs-lookup"><span data-stu-id="8bb93-175">In the box below **Associated Backup Pool**, select Pool C. Note that the Associated Backup Pool selection box will initially display pool A, because pool B was previously associated with this pool.</span></span>
        
          - <span data-ttu-id="8bb93-176">**[音声の自動フェールオーバーとフェールバック]** を選択し、**[OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8bb93-176">Select **Automatic failover and failback for Voice**, and then click **OK**.</span></span>
            
            <span data-ttu-id="8bb93-177">このプールの詳細情報を表示すると、関連付けられているプールが右ウィンドウの **[復元]** の下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="8bb93-177">When you view the details about this pool, the associated pool now appears in the right pane under **Resiliency**.</span></span>
        
          - <span data-ttu-id="8bb93-178">コンソールツリーで、[pool A] を右クリックし、[削除] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8bb93-178">In the console tree, right-click pool A, and then click Delete.</span></span>
        
          - <span data-ttu-id="8bb93-179">トポロジを公開します。</span><span class="sxs-lookup"><span data-stu-id="8bb93-179">Publish the topology.</span></span>

23. <span data-ttu-id="8bb93-180">Pool C でブートストラップアプリケーションを実行して backup service アプリケーションをインストールしてから、pool C のローカルコンピューター上の展開フォルダーから次のように実行して、backup service アプリケーションを起動します。</span><span class="sxs-lookup"><span data-stu-id="8bb93-180">Run the bootstrapping application on pool C to install the backup service application, and then start the backup service application by running the following from the deployment folder on a local machine in pool C:</span></span>
    
        Run "%SYSTEMROOT%\Program Files\Microsoft Lync Server 2013\Deployment\Bootstrapper.exe"
        Start-CsWindowsService -name LyncBackup

24. <span data-ttu-id="8bb93-181">次のコマンドレットを実行して、プール B の backup service アプリケーションを再起動します。</span><span class="sxs-lookup"><span data-stu-id="8bb93-181">Restart the backup service application on pool B by running the following cmdlets:</span></span>
    
        Stop-CsWindowsService -name LyncBackup
        Start-CsWindowsService -name LyncBackup

25. <span data-ttu-id="8bb93-182">Pool C が標準エディション (SE) プールであり、pool B に CMS がある場合は、次のコマンドレットを実行して、プール C に CMS データベースを手動でインストールします。</span><span class="sxs-lookup"><span data-stu-id="8bb93-182">If pool C is a Standard Edition (SE) Pool and pool B has CMS, install the CMS database manually on pool C by running the following cmdlet:</span></span>
    
        Install-CsDatabase -CentralManagementDatabase -SqlServerFqdn <Pool C FQDN> -SqlInstanceName rtc

26. <span data-ttu-id="8bb93-183">バックアップサービスを呼び出して、B と C をペアリングする前に生成された新しい会議コンテンツをプール B からプール C に同期し、プール c と B の開始後、B と C の間で作成された新しい会議コンテンツをプール B に同期します。</span><span class="sxs-lookup"><span data-stu-id="8bb93-183">Invoke the backup service to sync old conferencing content from pool B to pool C that was generated before pairing B and C together, and to sync new conferencing content from pool C to pool B that was generated after starting pool C and before B and C were paired together.</span></span> <span data-ttu-id="8bb93-184">そのためには、次のコマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="8bb93-184">To do so, run the following cmdlets:</span></span>
    
        Invoke-CsBackupServiceSync -PoolFqdn <Pool C FQDN>
        Invoke-CsBackupServiceSync -PoolFqdn <Pool B FQDN>

27. <span data-ttu-id="8bb93-185">Pool A に関連付けられている Survivable Branch Appliance X について、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="8bb93-185">For each Survivable Branch Appliance X associated with pool A:</span></span>
    
      - <span data-ttu-id="8bb93-186">次のコマンドレットを実行して、SBA X をシャットダウンします。</span><span class="sxs-lookup"><span data-stu-id="8bb93-186">Shut down SBA X by running the following cmdlet:</span></span>
        
            Stop-CsWindowsService
    
      - <span data-ttu-id="8bb93-187">SBA X のホームユーザーの一覧を含むファイルを作成します。ユーザーを SBA X に戻す場合は、手順30でリストを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8bb93-187">Create a file that contains a list of users homed on SBA X. The list will be needed when the users are moved back to SBA X in step 30.</span></span> <span data-ttu-id="8bb93-188">そのためには、次のコマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="8bb93-188">To do so, run the following cmdlet:</span></span>
        
            Get-CsUser -Filter {RegistrarPool -eq "<SBA X FQDN>"} | Export-Csv d:\sbaxusers.txt
    
      - <span data-ttu-id="8bb93-189">次のコマンドレットを実行して、SBA X をホームにしているユーザーをプール C に移動します。</span><span class="sxs-lookup"><span data-stu-id="8bb93-189">Force users homed on SBA X to move to pool C by running the following cmdlet:</span></span>
        
            Get-CsUser -Filter {RegistrarPool -eq "<SBA X FQDN>"} | Move-CsUser -Target <Pool C FQDN> -Force -Verbose
    
      - <span data-ttu-id="8bb93-190">次のコマンドレットを実行してから、これらのユーザーのデータを更新します。</span><span class="sxs-lookup"><span data-stu-id="8bb93-190">Update the data of these users by first running the following cmdlets:</span></span>
        
            Convert-csUserData -InputFile <Data file exported from PoolB> -OutputFile c:\Logs\ExportedUserData.xml -TargetVersionLync2010 
            $a=get-csuser -Filter {RegistrarPool -eq "FQDN of SBA X"} | select SipAddress
            foreach($x in $a) {$x.SipAddress.Substring(4) >> users.txt}
        
        <span data-ttu-id="8bb93-191">次に、次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="8bb93-191">And then run this script:</span></span>
        
            $users=gc c:\logs\users.txt
            foreach ($user in $users)
            {
            Update-CsUserData -FileName c:\logs\exportedUserDAta.xml -UserFilter $user - 
            }
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="8bb93-192">このユーザーがプール C に移動されるまでは、プール A に関連付けられている SBAs に所属しているユーザーに対してサービスの停止が発生します。</span><span class="sxs-lookup"><span data-stu-id="8bb93-192">A service outage will occur for users who are homed on SBAs that are associated with pool A until these users are moved to pool C.</span></span>

        
        </div>

28. <span data-ttu-id="8bb93-193">Topology Builder で、以前は Pool A に関連付けられていた各 SBA X について、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="8bb93-193">In Topology Builder, for each SBA X previously associated with Pool A, do the following:</span></span>
    
      - <span data-ttu-id="8bb93-194">関連付けを Pool C に変更します。そのためには、ブランチサイトをクリックし、[Survivable Branch Appliance] または [Servers] ノードを展開して、[ **Survivable Branch Appliance**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8bb93-194">Change the association to Pool C. To do so, click the branch site, expand the Survivable Branch Appliances or Servers node, and click **Survivable Branch Appliance**.</span></span> <span data-ttu-id="8bb93-195">次に、この Survivable Branch アプライアンスがプール C として接続する **フロントエンドプール、ユーザサービスプール** を選択して、「 **次へ**」をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8bb93-195">Then select the **Front End pool, User Services Pool** that this Survivable Branch Appliance will connect to as Pool C, and then click **Next**.</span></span>
    
      - <span data-ttu-id="8bb93-196">トポロジを公開します。</span><span class="sxs-lookup"><span data-stu-id="8bb93-196">Publish the topology.</span></span> <span data-ttu-id="8bb93-197">そのためには、コンソールツリーで、新しい **Survivable Branch Appliance** を右クリックし、[ **Topology**] をクリックして、[ **発行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8bb93-197">To do so, in the console tree, right-click the new **Survivable Branch Appliance**, click **Topology**, and then click **Publish**.</span></span>

29. <span data-ttu-id="8bb93-198">プール C に関連付けられた SBA X ごとに、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="8bb93-198">For each SBA X now associated with pool C:</span></span>
    
      - <span data-ttu-id="8bb93-199">SBA X を開始するには、survivable branch appliance で次のコマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="8bb93-199">Start SBA X by running the following cmdlet on the survivable branch appliance:</span></span>
        
            Start-CsWindowsService
    
      - <span data-ttu-id="8bb93-200">次のコマンドレットを実行して、最初に SBA X に置かれたユーザーのプール C から SBA X に移動します。</span><span class="sxs-lookup"><span data-stu-id="8bb93-200">Move users who were originally homed on SBA X from pool C to SBA X by running the following cmdlet.</span></span>
        
            Import-Csv d:\sbaxusers.txt | Move-CsUser -Target <SBA X FQDN> -Force

<span data-ttu-id="8bb93-201"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8bb93-201"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

