---
title: 'Lync Server 2013: 応答グループの障害復旧手順'
description: Lync Server 2013 応答グループの障害回復手順。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Response group disaster recovery procedures
ms:assetid: b49577b7-0ca3-4f20-b614-f3a2a0046b58
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205186(v=OCS.15)
ms:contentKeyID: 48185171
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c9021fb75c8f937bfd298578a9241d6256d26d85
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436301"
---
# <a name="response-group-disaster-recovery-procedures-in-lync-server-2013"></a><span data-ttu-id="b0035-103">Lync Server 2013 の応答グループの障害復旧手順</span><span class="sxs-lookup"><span data-stu-id="b0035-103">Response group disaster recovery procedures in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b0035-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b0035-104">

<span> </span></span></span>

<span data-ttu-id="b0035-105">_**最終更新日:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="b0035-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="b0035-106">障害回復のフェールオーバーフェーズでは、応答グループは、プライマリプール (使用できない) とバックアッププールの複数のプールに存在します。</span><span class="sxs-lookup"><span data-stu-id="b0035-106">During the failover phase of disaster recovery, the response groups reside in multiple pools: in the primary pool (which is unavailable) and in the backup pool.</span></span> <span data-ttu-id="b0035-107">両方のプールの応答グループの名前が同じであり、所有者が同じ所有者 (プライマリプール) であるが、それぞれの親が異なっている。</span><span class="sxs-lookup"><span data-stu-id="b0035-107">The response groups in both pools have the same name and the same owner (the primary pool), but they have different parents.</span></span> <span data-ttu-id="b0035-108">このとき、応答グループコマンドレットの動作は少し異なります。</span><span class="sxs-lookup"><span data-stu-id="b0035-108">During this time, Response Group cmdlets work a little differently.</span></span> <span data-ttu-id="b0035-109">次の手順で示されているように、必ずパラメーターを使用してください。</span><span class="sxs-lookup"><span data-stu-id="b0035-109">Be sure to use parameters as specified in the following procedure.</span></span> <span data-ttu-id="b0035-110">フェールオーバーフェーズでのコマンドレットの動作の詳細については、「NextHop ブログ」「Lync Server 2013: ディザスターリカバリー中の応答グループの回復」を参照してください [https://go.microsoft.com/fwlink/p/?LinkId=263957](https://go.microsoft.com/fwlink/p/?linkid=263957) 。</span><span class="sxs-lookup"><span data-stu-id="b0035-110">For details about how cmdlets work during the failover phase, see NextHop blog article "Lync Server 2013: Recovering Response Groups During Disaster Recovery" at [https://go.microsoft.com/fwlink/p/?LinkId=263957](https://go.microsoft.com/fwlink/p/?linkid=263957).</span></span> <span data-ttu-id="b0035-111">このブログ記事は、リリース版の Lync Server 2013 にも適用されます。</span><span class="sxs-lookup"><span data-stu-id="b0035-111">This blog article also applies to the released version of Lync Server 2013.</span></span>

<span data-ttu-id="b0035-112">Lync Server 応答グループサービスの障害回復を準備して実行するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b0035-112">Use the steps in the following procedure to prepare for and perform disaster recovery for Lync Server Response Group service.</span></span>

<div>

## <a name="to-fail-over-and-fail-back-response-group"></a><span data-ttu-id="b0035-113">フェールオーバーと応答の返信グループをフェイルバックするには</span><span class="sxs-lookup"><span data-stu-id="b0035-113">To fail over and fail back Response Group</span></span>

1.  <span data-ttu-id="b0035-114">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0035-114">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="b0035-115">定期的にバックアップを実行します。</span><span class="sxs-lookup"><span data-stu-id="b0035-115">Routinely perform backups.</span></span> <span data-ttu-id="b0035-116">コマンドラインで、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="b0035-116">At the command line, type:</span></span>
    
        Export-CsRgsConfiguration -Source "service:ApplicationServer:<primary pool FQDN>" -FileName "<backup path and file name>"
    
    <span data-ttu-id="b0035-117">例:</span><span class="sxs-lookup"><span data-stu-id="b0035-117">For example:</span></span>
    
        Export-CsRgsConfiguration -Source "service:ApplicationServer:primary.contoso.com" -FileName "C:\RgsExportPrimary.zip"

3.  <span data-ttu-id="b0035-118">停止中は、バックアッププールにフェールオーバーした後、バックアッププールに応答グループをインポートします。</span><span class="sxs-lookup"><span data-stu-id="b0035-118">During an outage, after failover to the backup pool, import the response groups to the backup pool.</span></span> <span data-ttu-id="b0035-119">コマンド ラインで次を入力します。</span><span class="sxs-lookup"><span data-stu-id="b0035-119">At the command line, type:</span></span>
    
        Import-CsRgsConfiguration -Destination "service:ApplicationServer:<backup pool FQDN>" -FileName "<backup path and file name>"
    
    <span data-ttu-id="b0035-120">バックアッププール内のアプリケーションレベルの設定をプライマリプールの設定で置き換える場合は、– ReplaceExistingSettings パラメーターを指定します。</span><span class="sxs-lookup"><span data-stu-id="b0035-120">If you want to replace the application-level settings in the backup pool with the settings from the primary pool, include the –ReplaceExistingSettings parameter.</span></span> <span data-ttu-id="b0035-121">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="b0035-121">For example:</span></span>
    
        Import-CsRgsConfiguration -Destination "service:ApplicationServer:backup.contoso.com" -FileName "C:\RgsExportPrimary.zip" -ReplaceExistingSettings
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="b0035-122">バックアッププールの設定を変更せずに、プライマリプールを復元できない場合、プライマリプールの設定は失われます。</span><span class="sxs-lookup"><span data-stu-id="b0035-122">If you do not replace the settings in the backup pool and the primary pool can't be recovered, the primary pool settings will be lost.</span></span> <span data-ttu-id="b0035-123">詳細については、「 <A href="lync-server-2013-planning-for-response-group-disaster-recovery.md">Lync Server 2013 での応答グループの障害回復の計画</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b0035-123">For details, see <A href="lync-server-2013-planning-for-response-group-disaster-recovery.md">Planning for response group disaster recovery in Lync Server 2013</A>.</span></span>

    
    </div>

4.  <span data-ttu-id="b0035-124">インポートされた応答グループを表示して、インポートが正常に完了したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="b0035-124">Verify that the import was successful by displaying the imported response groups.</span></span> <span data-ttu-id="b0035-125">インポートされた応答グループは、依然としてプライマリプールによって所有されます。</span><span class="sxs-lookup"><span data-stu-id="b0035-125">The imported response groups are still owned by the primary pool.</span></span> <span data-ttu-id="b0035-126">以下の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="b0035-126">Do the following:</span></span>
    
      - <span data-ttu-id="b0035-127">プライマリプールによって所有されているバックアッププール内のすべてのワークフローを表示し、プライマリプールワークフローがすべて含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b0035-127">Display all the workflows in the backup pool that are owned by the primary pool, and verify that all the primary pool workflows are included.</span></span> <span data-ttu-id="b0035-128">コマンドラインで、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="b0035-128">At the command line, type:</span></span>
        
            Get-CsRgsWorkflow -Identity "service:ApplicationServer:<backup pool FQDN>" -Owner "service:ApplicationServer"<primary pool FQDN>
        
        <span data-ttu-id="b0035-129">例:</span><span class="sxs-lookup"><span data-stu-id="b0035-129">For example:</span></span>
        
            Get-CsRgsWorkflow -Identity "service:ApplicationServer:backup.contoso.com" -Owner "service:ApplicationServer:primary.contoso.com"
    
      - <span data-ttu-id="b0035-130">プライマリプールによって所有されているバックアッププール内のすべてのキューを表示し、すべてのプライマリプールキューが含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b0035-130">Display all the queues in the backup pool that are owned by the primary pool, and verify that all the primary pool queues are included.</span></span> <span data-ttu-id="b0035-131">コマンドラインで、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="b0035-131">At the command line, type:</span></span>
        
            Get-CsRgsQueue -Identity "service:ApplicationServer:<backup pool FQDN>" -Owner "service:ApplicationServer"<primary pool FQDN>
        
        <span data-ttu-id="b0035-132">例:</span><span class="sxs-lookup"><span data-stu-id="b0035-132">For example:</span></span>
        
            Get-CsRgsQueue -Identity "service:ApplicationServer:backup.contoso.com" -Owner "service:ApplicationServer"primary.contoso.com"
    
      - <span data-ttu-id="b0035-133">プライマリプールによって所有されているバックアッププール内のすべてのエージェントグループを表示し、プライマリプールエージェントグループがすべて含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b0035-133">Display all the agent groups in the backup pool that are owned by the primary pool, and verify that all the primary pool agent groups are included.</span></span> <span data-ttu-id="b0035-134">コマンドラインで、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="b0035-134">At the command line, type:</span></span>
        
            Get-CsRgsAgentGroup -Identity "service:ApplicationServer:<backup pool FQDN>" -Owner "service:ApplicationServer"<primary pool FQDN>
        
        <span data-ttu-id="b0035-135">例:</span><span class="sxs-lookup"><span data-stu-id="b0035-135">For example:</span></span>
        
            Get-CsRgsAgentGroup -Identity "service:ApplicationServer:backup.contoso.com" -Owner "service:ApplicationServer"primary.contoso.com"
    
      - <span data-ttu-id="b0035-136">プライマリプールによって所有されているバックアッププール内のビジネス時間をすべて表示し、プライマリプールのすべての業務時間が含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b0035-136">Display all the hours of business in the backup pool that are owned by the primary pool, and verify that all the primary pool hours of business are included.</span></span> <span data-ttu-id="b0035-137">コマンドラインで、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="b0035-137">At the command line, type:</span></span>
        
            Get-CsRgsHoursOfBusiness -Identity "service:ApplicationServer:<backup pool FQDN>" -Owner "service:ApplicationServer"<primary pool FQDN>
        
        <span data-ttu-id="b0035-138">例:</span><span class="sxs-lookup"><span data-stu-id="b0035-138">For example:</span></span>
        
            Get-CsRgsHoursOfBusiness -Identity "service:ApplicationServer:backup.contoso.com" -Owner "service:ApplicationServer"primary.contoso.com"
    
      - <span data-ttu-id="b0035-139">プライマリプールによって所有されているバックアッププール内のすべての休日セットを表示し、すべてのプライマリプールの休日セットが含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b0035-139">Display all the holiday sets in the backup pool that are owned by the primary pool, and verify that all the primary pool holiday sets are included.</span></span> <span data-ttu-id="b0035-140">コマンドラインで、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="b0035-140">At the command line, type:</span></span>
        
            Get-CsRgsHolidaySet -Identity "service:ApplicationServer:<backup pool FQDN>" -Owner "service:ApplicationServer"<primary pool FQDN>
        
        <span data-ttu-id="b0035-141">例:</span><span class="sxs-lookup"><span data-stu-id="b0035-141">For example:</span></span>
        
            Get-CsRgsHolidaySet -Identity "service:ApplicationServer:backup.contoso.com" -Owner "service:ApplicationServer"primary.contoso.com"
    
    <span data-ttu-id="b0035-142">または、[-Owner] パラメーターの代わりに– ShowAll パラメーターを使用して、プライマリプールに所有されているものとバックアッププールに所有されているものを含め、すべての応答グループをバックアッププールに表示することができます。</span><span class="sxs-lookup"><span data-stu-id="b0035-142">Alternatively, you can display all the response groups in the backup pool, including the ones owned by the primary pool and the ones owned by the backup pool by using the –ShowAll parameter instead of the –Owner parameter.</span></span> <span data-ttu-id="b0035-143">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="b0035-143">For example:</span></span>
    
        Get-CsRgsWorkflow -Identity "service:ApplicationServer:<backup pool FQDN>" -ShowAll
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="b0035-144">– ShowAll パラメーターまたは– Owner パラメーターのいずれかを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b0035-144">You must use either the –ShowAll parameter or the –Owner parameter.</span></span> <span data-ttu-id="b0035-145">これらのパラメーターのどちらも使用しない場合、バックアッププールにインポートした応答グループは、コマンドレットによって返される結果に一覧表示されません。</span><span class="sxs-lookup"><span data-stu-id="b0035-145">If you do not use either of these parameters, the response groups that you imported to the backup pool will not be listed in the results returned by the cmdlets.</span></span>

    
    </div>

5.  <span data-ttu-id="b0035-146">インポートされた応答グループに通話を発信し、通話が正しく処理されていることを確認して、インポートが成功したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="b0035-146">Verify that the import was successful by placing a call to an imported response group and verifying that the call is handled correctly.</span></span>

6.  <span data-ttu-id="b0035-147">バックアッププールのエージェントグループにサインインするために、正式なエージェントグループのメンバーであるエージェントを要求します。</span><span class="sxs-lookup"><span data-stu-id="b0035-147">Request agents who are members of formal agent groups to sign in to their agent groups in the backup pool.</span></span>

7.  <span data-ttu-id="b0035-148">インポートした応答グループを通常どおりに管理および変更します。</span><span class="sxs-lookup"><span data-stu-id="b0035-148">Manage and modify the imported response groups as usual.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="b0035-149">応答グループはバックアッププールに含まれていますが、Lync Server 管理シェルを使用してそれらを管理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b0035-149">While the response groups are in the backup pool, you need to use Lync Server Management Shell to manage them.</span></span> <span data-ttu-id="b0035-150">Lync Server コントロールパネルを使用して、バックアッププールにインポートした応答グループを管理することはできません。</span><span class="sxs-lookup"><span data-stu-id="b0035-150">You cannot use Lync Server Control Panel to manage the response groups that you imported to the backup pool.</span></span>

    
    </div>

8.  <span data-ttu-id="b0035-151">プライマリプールが復元され、フェールバックが完了したら、バックアッププールにインポートされたプライマリプール応答グループをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="b0035-151">After the primary pool is restored and failback is complete, export the primary pool response groups that were imported to the backup pool.</span></span> <span data-ttu-id="b0035-152">コマンド ラインで次を入力します。</span><span class="sxs-lookup"><span data-stu-id="b0035-152">At the command line, type:</span></span>
    
        Export-CsRgsConfiguration -Source ApplicationServer:<backup pool FQDN> -Owner ApplicationServer:<primary pool FQDN> -FileName "<backup path and file name>"

9.  <span data-ttu-id="b0035-153">応答グループをプライマリプールにインポートします。</span><span class="sxs-lookup"><span data-stu-id="b0035-153">Import the response groups back to the primary pool.</span></span> <span data-ttu-id="b0035-154">コマンドラインで、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="b0035-154">At the command line, type:</span></span>
    
        Import-CsRgsConfiguration -Destination "service:ApplicationServer:<primary pool FQDN>" -OverwriteOwner -FileName "<exported path and file name>"
    
    <span data-ttu-id="b0035-155">例:</span><span class="sxs-lookup"><span data-stu-id="b0035-155">For example:</span></span>
    
        Import-CsRgsConfiguration -Destination "service:ApplicationServer:primary.contoso.com" -OverwriteOwner -FileName "C:\RgsExportPrimaryUpdated.zip"
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="b0035-156">回復中にプールを再構築する場合、同一または別の完全修飾ドメイン名 (FQDN) を使用している場合は、– OverwriteOwner パラメーターを使う必要があります。</span><span class="sxs-lookup"><span data-stu-id="b0035-156">If you rebuild a pool during recovery, whether with the same or a different fully qualified domain name (FQDN), you need to use the –OverwriteOwner parameter.</span></span> <span data-ttu-id="b0035-157">原則として、応答グループをプライマリプールにインポートするときに、常に– OverwriteOwner パラメーターを使うことができます。</span><span class="sxs-lookup"><span data-stu-id="b0035-157">As a rule of thumb, you can always use the –OverwriteOwner parameter when you import response groups back to the primary pool.</span></span>

    
    </div>
    
    <span data-ttu-id="b0035-158">新しいプール (同じまたは別の FQDN を含む) を展開して、プライマリプールの代わりにバックアッププールのアプリケーションレベルの設定を使用する場合は、– ReplaceExistingSettings パラメーターを含めます。</span><span class="sxs-lookup"><span data-stu-id="b0035-158">If you deployed a new pool (with the same or a different FQDN) to replace the primary pool, and you want to use the application-level settings from the backup pool for the new pool, include the –ReplaceExistingSettings parameter.</span></span> <span data-ttu-id="b0035-159">コマンドラインで、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="b0035-159">At the command line, type:</span></span>
    
        Import-CsRgsConfiguration -Destination "service:ApplicationServer:<new primary pool FQDN>" -OverwriteOwner -FileName "<exported path and file name>" -ReplaceExistingSettings
    
    <span data-ttu-id="b0035-160">例:</span><span class="sxs-lookup"><span data-stu-id="b0035-160">For example:</span></span>
    
        Import-CsRgsConfiguration -Destination "service:ApplicationServer:newprimary.contoso.com" -OverwriteOwner -FileName "C:\RgsExportPrimaryUpdated.zip" -ReplaceExistingSettings
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="b0035-161">新しいプールのアプリケーションレベルの設定と既定の音楽の保留オーディオファイルをバックアッププールの設定で置き換える必要がない場合は、新しいプールで既定のアプリケーションレベルの設定が使用されます。</span><span class="sxs-lookup"><span data-stu-id="b0035-161">If you don't want to replace the application-level settings and default music-on-hold audio file for the new pool with the settings from the backup pool, the new pool will use the default application-level settings.</span></span>

    
    </div>

10. <span data-ttu-id="b0035-162">インポートされた応答グループの構成を表示して、プライマリプールへのインポートが正常に完了したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="b0035-162">Verify that the import back to the primary pool was successful by displaying the imported response group configuration.</span></span> <span data-ttu-id="b0035-163">以下の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="b0035-163">Do the following:</span></span>
    
      - <span data-ttu-id="b0035-164">プライマリプール内のすべてのワークフローを表示し、インポートされたすべてのワークフローが含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b0035-164">Display all the workflows in the primary pool, and verify that all the imported workflows are included.</span></span> <span data-ttu-id="b0035-165">コマンドラインで、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="b0035-165">At the command line, type:</span></span>
        
            Get-CsRgsWorkflow -Identity "service:ApplicationServer:<primary pool FQDN>" -ShowAll
        
        <span data-ttu-id="b0035-166">例:</span><span class="sxs-lookup"><span data-stu-id="b0035-166">For example:</span></span>
        
            Get-CsRgsWorkflow -Identity "service:ApplicationServer: primary.contoso.com" -ShowAll
    
      - <span data-ttu-id="b0035-167">プライマリプール内のすべてのキューを表示し、インポートされたすべてのキューが含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b0035-167">Display all the queues in the primary pool, and verify that all the imported queues are included.</span></span> <span data-ttu-id="b0035-168">コマンドラインで、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="b0035-168">At the command line, type:</span></span>
        
            Get-CsRgsQueue -Identity "service:ApplicationServer:<primary pool FQDN>" -ShowAll
        
        <span data-ttu-id="b0035-169">例:</span><span class="sxs-lookup"><span data-stu-id="b0035-169">For example:</span></span>
        
            Get-CsRgsQueue -Identity "service:ApplicationServer:primary.contoso.com" -ShowAll
    
      - <span data-ttu-id="b0035-170">プライマリプール内のすべてのエージェントグループを表示し、インポートされたすべてのエージェントグループが含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b0035-170">Display all the agent groups in the primary pool, and verify that all the imported agent groups are included.</span></span> <span data-ttu-id="b0035-171">コマンドラインで、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="b0035-171">At the command line, type:</span></span>
        
            Get-CsRgsAgentGroup -Identity "service:ApplicationServer: <primary pool FQDN>" -ShowAll
        
        <span data-ttu-id="b0035-172">例:</span><span class="sxs-lookup"><span data-stu-id="b0035-172">For example:</span></span>
        
            Get-CsRgsAgentGroup -Identity "service:ApplicationServer:primary.contoso.com" -ShowAll
    
      - <span data-ttu-id="b0035-173">プライマリプールのビジネス時間をすべて表示し、インポートされたすべての勤務時間が含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b0035-173">Display all the hours of business in the primary pool, and verify that all the imported hours of business are included.</span></span> <span data-ttu-id="b0035-174">コマンドラインで、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="b0035-174">At the command line, type:</span></span>
        
            Get-CsRgsHoursOfBusiness -Identity "service:ApplicationServer:<primary pool FQDN>" -ShowAll
        
        <span data-ttu-id="b0035-175">例:</span><span class="sxs-lookup"><span data-stu-id="b0035-175">For example:</span></span>
        
            Get-CsRgsHoursOfBusiness -Identity "service:ApplicationServer:primary.contoso.com" -ShowAll
    
      - <span data-ttu-id="b0035-176">プライマリプールのすべての休日セットを表示し、インポートされたすべての祝日セットが含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b0035-176">Display all the holiday sets in the primary pool, and verify that all the imported holiday sets are included.</span></span> <span data-ttu-id="b0035-177">コマンドラインで、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="b0035-177">At the command line, type:</span></span>
        
            Get-CsRgsHolidaySet -Identity "service:ApplicationServer:<primary pool FQDN>" -ShowAll
        
        <span data-ttu-id="b0035-178">例:</span><span class="sxs-lookup"><span data-stu-id="b0035-178">For example:</span></span>
        
            Get-CsRgsHolidaySet -Identity "service:ApplicationServer:primary.contoso.com" -ShowAll

11. <span data-ttu-id="b0035-179">インポートされた応答グループに通話を発信し、通話が正しく処理されていることを確認して、インポートが成功したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="b0035-179">Verify that the import was successful by placing a call to an imported response group and verifying that the call is handled correctly.</span></span>

12. <span data-ttu-id="b0035-180">必要に応じて、プライマリプールによって所有されている応答グループをバックアッププールから削除します。</span><span class="sxs-lookup"><span data-stu-id="b0035-180">Optionally, remove the response groups owned by the primary pool from the backup pool.</span></span> <span data-ttu-id="b0035-181">コマンドラインで、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="b0035-181">At the command line, type:</span></span>
    
        Export-CsRgsConfiguration -Source "service:ApplicationServer:<backup pool FQDN>" -Owner "service:ApplicationServer:<primary pool FQDN>" -FileName "<backup path and file name>" -RemoveExportedConfiguration
    
    <span data-ttu-id="b0035-182">例:</span><span class="sxs-lookup"><span data-stu-id="b0035-182">For example:</span></span>
    
        Export-CsRgsConfiguration -Source "service:ApplicationServer:backup.contoso.com" -Owner "service:ApplicationServer:primary.contoso.com" -FileName "C:\RgsExportPrimaryUpdated.zip" -RemoveExportedConfiguration
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="b0035-183">この手順では、エクスポートされた構成で新しいファイルを作成し、それをバックアッププールから削除します。</span><span class="sxs-lookup"><span data-stu-id="b0035-183">This step creates a new file with the exported configuration, and then removes it from the backup pool.</span></span>

    
    <span data-ttu-id="b0035-184"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b0035-184"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

