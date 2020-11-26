---
title: 'Lync Server 2013: ABC プールフェールオーバーのバックアップ前提条件'
description: 'Lync Server 2013: ABC プールフェールオーバーのバックアップ前提条件。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Backup prerequisites for ABC pool failover
ms:assetid: 652046f5-6086-4592-902d-d5789581977d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945634(v=OCS.15)
ms:contentKeyID: 51541485
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 05eb0d2ad50f1ed4f04964158fb5d22d079f3b50
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437911"
---
# <a name="backup-prerequisites-for-abc-pool-failover-in-lync-server-2013"></a><span data-ttu-id="ae7c5-103">Lync Server 2013 での ABC プールフェールオーバーのバックアップの前提条件</span><span class="sxs-lookup"><span data-stu-id="ae7c5-103">Backup prerequisites for ABC pool failover in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ae7c5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ae7c5-104">

<span> </span></span></span>

<span data-ttu-id="ae7c5-105">_**最終更新日:** 2013-03-26_</span><span class="sxs-lookup"><span data-stu-id="ae7c5-105">_**Topic Last Modified:** 2013-03-26_</span></span>

<span data-ttu-id="ae7c5-106">ABC プールフェールオーバーの手順を最大限に活用するには、障害が発生してフェールオーバーが発生する前に、特定のバックアップを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae7c5-106">To get the maximum benefit from using the ABC pool failover procedure, you must perform certain backups before the disaster and failover happen:</span></span>

  - <span data-ttu-id="ae7c5-107">**CsLISConfiguration** コマンドレットを使用して、場所情報サービス (LIS) 構成データをプール A から定期的にバックアップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae7c5-107">You must regularly back up the Location Information Service (LIS) configuration data from pool A by using the **Export-CsLISConfiguration** cmdlet.</span></span>
    
        Export-csLisConfiguration -FileName <C:\LISExportPrimary.zip>

  - <span data-ttu-id="ae7c5-108">**Export-CsRgsConfiguration** コマンドレットを使用して、プール A の応答グループの構成データを定期的にバックアップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae7c5-108">You must regularly back up the Response Group configuration data in pool A by using the **Export-CsRgsConfiguration** cmdlet.</span></span>
    
        Export-CsRgsConfiguration -Source "service:ApplicationServer:<Pool A FQDN>" -FileName "C:\RgsExportPrimary.zip"
    
    <span data-ttu-id="ae7c5-109">一般的に、毎日のバックアップを実行することをお勧めしますが、変更の量が多い場合は、より頻繁にバックアップをスケジュールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ae7c5-109">In general, we recommend that you perform daily backups, but if you have a high volume of changes, you might want to schedule more frequent backups.</span></span> <span data-ttu-id="ae7c5-110">障害が発生した場合に失われる可能性のある情報の量は、バックアップの頻度、および変更の頻度と量によって異なります。</span><span class="sxs-lookup"><span data-stu-id="ae7c5-110">The amount of information that you can lose in the event of a disaster depends on the frequency of your backups, as well as on the frequency and volume of changes.</span></span>
    
    <span data-ttu-id="ae7c5-111">応答グループのアプリケーションは、1つのプールにつき1つのアプリケーションレベルの設定のみを格納できます。</span><span class="sxs-lookup"><span data-stu-id="ae7c5-111">The Response Group application can store only one set of application-level settings per pool.</span></span> <span data-ttu-id="ae7c5-112">これらの設定にアクセスするには、 **Get-CsRgsConfiguration** コマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="ae7c5-112">These settings can be accessed through the **Get-CsRgsConfiguration** cmdlets.</span></span> <span data-ttu-id="ae7c5-113">設定には、既定の音楽保留の構成、既定の音楽保留中のオーディオファイル、エージェントの呼び出し元の猶予期間、通話コンテキストの構成が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ae7c5-113">The settings include the default music-on-hold configuration, the default music-on-hold audio file, the agent ring-back grace period, and the call context configuration.</span></span> <span data-ttu-id="ae7c5-114">これらの設定は、" **Replaceexistingsettings** " パラメーターを使用して、 **Import-CsRgsConfiguration** コマンドレットを通じて、1つのプールから別のプールに転送できますが、この操作を行うと、移動先のプールのアプリケーションレベルの設定が上書きされます。</span><span class="sxs-lookup"><span data-stu-id="ae7c5-114">These settings can be transferred from one pool to another through the **Import-CsRgsConfiguration** cmdlet by using the **ReplaceExistingSettings** parameter, but this operation will override any application-level settings in the destination pool.</span></span>
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="ae7c5-115">別の場所で、応答グループアプリケーションの構成に使用されているすべての元のオーディオファイル (つまり、レコーディングまたは音楽の保留ファイル) のバックアップコピーを保持します。</span><span class="sxs-lookup"><span data-stu-id="ae7c5-115">In a separate location, keep a backup copy of all the original audio files that have been used to configure the Response Group application (that is, any recordings or music-on-hold files).</span></span>

    
    </div>
    
    <span data-ttu-id="ae7c5-116">プール内のコールパークにアップロードされたカスタマイズ済みの音楽の保存ファイルがある場合は、そのファイルのコピーを別の場所に保存しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae7c5-116">If you have any customized music-on-hold files that have been uploaded for Call Park in a pool, you should keep a copy of these in another location.</span></span> <span data-ttu-id="ae7c5-117">これらのファイルは、Lync Server 2013 の障害回復プロセスの一部としてはバックアップされません。プールにアップロードされたファイルが破損、破損、または消去された場合、これらのファイルは失われます。</span><span class="sxs-lookup"><span data-stu-id="ae7c5-117">These files are not backed up as part of the Lync Server 2013 disaster recovery process, and they will be lost if the files uploaded to the pool are damaged, corrupted, or erased.</span></span>
    
        Xcopy  <Source: Pool A CPS File Store Path>  <Destination>
        Example: Xcopy  "<Pool A File Store Path>\LyncFileStore\coX-ApplicationServer-X\AppServerFiles\CPS\"  "<Destination:  Backup location 1>"
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ae7c5-118">コールパークアプリケーションには、1つのセットの設定と、1つのプールにつき1つのカスタマイズされた音楽オンホールドオーディオファイルしか保存できません。</span><span class="sxs-lookup"><span data-stu-id="ae7c5-118">The Call Park application can store only one set of settings and one customized music-on-hold audio file per pool.</span></span> <span data-ttu-id="ae7c5-119">これらの設定にアクセスするには、 <STRONG>CsCpsConfiguration</STRONG> コマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="ae7c5-119">These settings can be accessed through the <STRONG>Get-CsCpsConfiguration</STRONG> cmdlet.</span></span> <span data-ttu-id="ae7c5-120">コールパークの障害回復メカニズムはバックアッププールのコールパークアプリケーションに依存するため、障害が発生した場合、プライマリプールの設定はバックアップされないか、維持されません。</span><span class="sxs-lookup"><span data-stu-id="ae7c5-120">Because the disaster recovery mechanism for Call Park relies on the Call Park application of the backup pool, the settings of the primary pool are not backed up or preserved if a disaster occurs.</span></span> <span data-ttu-id="ae7c5-121">プライマリプールが失われた場合は、これらの設定を復元することはできません。また、新しいプールがプライマリプールの代わりとして展開されている場合は、コールパークの設定と、カスタマイズされた音楽の保留中のオーディオファイルを再構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae7c5-121">If the primary pool is lost, these settings cannot be recovered, and when a new pool is deployed to replace the primary pool, the Call Park settings and any customized music-on-hold audio file would need to be reconfigured.</span></span>

    
    </div>

  - <span data-ttu-id="ae7c5-122">未割り当ての電話機能の一部としてアナウンスを構成する場合は、最初の設定で使用した元のオーディオファイルのコピーを別の場所に残しておくことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ae7c5-122">If you configure any announcements as part of the Unassigned Number Voice Feature, we recommend that you keep in another location a copy of any original audio file used during the initial configuration.</span></span> <span data-ttu-id="ae7c5-123">この操作を行わなかった場合は、オーディオファイルがインポートされたサーバーまたはプールのファイルストアに、構成されたオーディオファイルのコピーを取得できます。</span><span class="sxs-lookup"><span data-stu-id="ae7c5-123">If you did not do that, you can get a copy of the configured audio files in the file store of the server or pool to which the audio files were imported.</span></span> <span data-ttu-id="ae7c5-124">これらのファイルは、Lync Server 2013 の障害回復プロセスの一部としてはバックアップされません。プールにアップロードされたファイルが破損、破損、または消去された場合、これらのファイルは失われます。</span><span class="sxs-lookup"><span data-stu-id="ae7c5-124">These files are not backed up as part of the Lync Server 2013 disaster recovery process, and they will be lost if the files uploaded to the pool are damaged, corrupted, or erased.</span></span> <span data-ttu-id="ae7c5-125">割り当てられていない番号の音声機能を構成するために使用されるすべてのオーディオファイルをサーバーまたはプールのファイルストアからコピーするには、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="ae7c5-125">To copy all the audio files used to configure the Unassigned Number Voice Feature from the file store of a server or a pool, use:</span></span>
    
        Use: Xcopy  <Source: Pool A Announcement Service File Store Path>  <Destination>
        Example Usage:  Xcopy  "<Pool A File Store Path>\X-ApplicationServer-X\AppServerFiles\RGS\AS"  "<Destination: Backup location>"

  - <span data-ttu-id="ae7c5-126">プールにデータベースの監視とアーカイブを行っている場合は、SQL Server 管理ツールを使用してバックアップを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae7c5-126">If you have Monitoring and Archiving databases in a pool, you should use SQL Server management tools to back them up.</span></span> <span data-ttu-id="ae7c5-127">"データベースは Lync Server Backup Service でバックアップされていないため、データベースがプール A に併置されている場合、" データベースの監視 "および" アーカイブ "プロシージャでは、データベースは保持されません。</span><span class="sxs-lookup"><span data-stu-id="ae7c5-127">In the ABC failover procedure, Monitoring and Archiving databases are not preserved if they are collocated in pool A, because these databases are not backed up through Lync Server Backup Service.</span></span>

<span data-ttu-id="ae7c5-128"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ae7c5-128"></div>

<span> </span>

</div>

</div>

</span></span></div>

