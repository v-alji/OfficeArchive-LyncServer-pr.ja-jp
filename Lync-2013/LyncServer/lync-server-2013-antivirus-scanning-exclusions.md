---
title: 'Lync Server 2013: ウイルス スキャン除外範囲'
description: 'Lync Server 2013: ウイルス対策スキャンの除外。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Antivirus scanning exclusions for Lync Server 2013
ms:assetid: 71e1f1cc-2d16-4111-9864-9276bf24dfe0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn440138(v=OCS.15)
ms:contentKeyID: 57793042
ms.date: 11/03/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 20c395f529cad91993d003efdeb231bd66f4b9bc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440662"
---
# <a name="antivirus-scanning-exclusions-for-lync-server-2013"></a><span data-ttu-id="9f63c-103">Lync Server 2013 用のウイルス スキャン除外範囲</span><span class="sxs-lookup"><span data-stu-id="9f63c-103">Antivirus scanning exclusions for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9f63c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9f63c-104">

<span> </span></span></span>

<span data-ttu-id="9f63c-105">_**最終更新日:** 2015-11-02_</span><span class="sxs-lookup"><span data-stu-id="9f63c-105">_**Topic Last Modified:** 2015-11-02_</span></span>

<span data-ttu-id="9f63c-106">ウイルス対策スキャナーが Lync Server 2013 の動作を妨害しないようにするには、ウイルススキャンを実行している Lync Server 2013 サーバーまたはサーバーの役割ごとに、特定のプロセスとディレクトリを除外する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f63c-106">To ensure that the antivirus scanner does not interfere with the operation of Lync Server 2013, you must exclude specific processes and directories for each Lync Server 2013 server or server role on which you run an antivirus scanner.</span></span> <span data-ttu-id="9f63c-107">除外が必要なプロセスとディレクトリを以下に示します。</span><span class="sxs-lookup"><span data-stu-id="9f63c-107">The following processes and directories should be excluded:</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="9f63c-108">次に示すフォルダーとファイルの場所は、Lync Server 2013 の既定の場所です。</span><span class="sxs-lookup"><span data-stu-id="9f63c-108">Folder and file locations listed below are the default locations for Lync Server 2013.</span></span> <span data-ttu-id="9f63c-109">既定の設定を使用しなかったすべての場所については、ここに示す既定の場所の代わりに、組織で指定した場所を除外してください。</span><span class="sxs-lookup"><span data-stu-id="9f63c-109">For any locations for which you did not use the default, exclude the locations you specified for your organization instead of the default locations specified in this topic.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="9f63c-110">一部のウイルス対策プログラムでは、除外リストに相対パスでなく絶対パスが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="9f63c-110">Please note that some antivirus programs may need absolute, not relative paths, for their exclusion list.</span></span>



</div>

  - <span data-ttu-id="9f63c-111">Lync Server 2013 のプロセス:</span><span class="sxs-lookup"><span data-stu-id="9f63c-111">Lync Server 2013 processes:</span></span>
    
      - <span data-ttu-id="9f63c-112">ABServer.exe</span><span class="sxs-lookup"><span data-stu-id="9f63c-112">ABServer.exe</span></span>
    
      - <span data-ttu-id="9f63c-113">AcpMcuSvc.exe</span><span class="sxs-lookup"><span data-stu-id="9f63c-113">AcpMcuSvc.exe</span></span>
    
      - <span data-ttu-id="9f63c-114">ASMCUSvc.exe</span><span class="sxs-lookup"><span data-stu-id="9f63c-114">ASMCUSvc.exe</span></span>
    
      - <span data-ttu-id="9f63c-115">AVMCUSvc.exe</span><span class="sxs-lookup"><span data-stu-id="9f63c-115">AVMCUSvc.exe</span></span>
    
      - <span data-ttu-id="9f63c-116">ChannelService.exe</span><span class="sxs-lookup"><span data-stu-id="9f63c-116">ChannelService.exe</span></span>
    
      - <span data-ttu-id="9f63c-117">ClsAgent.exe</span><span class="sxs-lookup"><span data-stu-id="9f63c-117">ClsAgent.exe</span></span>
    
      - <span data-ttu-id="9f63c-118">ComplianceService.exe</span><span class="sxs-lookup"><span data-stu-id="9f63c-118">ComplianceService.exe</span></span>
    
      - <span data-ttu-id="9f63c-119">DataMCUSvc.exe</span><span class="sxs-lookup"><span data-stu-id="9f63c-119">DataMCUSvc.exe</span></span>
    
      - <span data-ttu-id="9f63c-120">DataProxy.exe</span><span class="sxs-lookup"><span data-stu-id="9f63c-120">DataProxy.exe</span></span>
    
      - <span data-ttu-id="9f63c-121">FileTransferAgent.exe</span><span class="sxs-lookup"><span data-stu-id="9f63c-121">FileTransferAgent.exe</span></span>
    
      - <span data-ttu-id="9f63c-122">IMMCUSvc.exe</span><span class="sxs-lookup"><span data-stu-id="9f63c-122">IMMCUSvc.exe</span></span>
    
      - <span data-ttu-id="9f63c-123">LysSvc.exe</span><span class="sxs-lookup"><span data-stu-id="9f63c-123">LysSvc.exe</span></span>
    
      - <span data-ttu-id="9f63c-124">MasterReplicatorAgent.exe</span><span class="sxs-lookup"><span data-stu-id="9f63c-124">MasterReplicatorAgent.exe</span></span>
    
      - <span data-ttu-id="9f63c-125">MediaRelaySvc.exe</span><span class="sxs-lookup"><span data-stu-id="9f63c-125">MediaRelaySvc.exe</span></span>
    
      - <span data-ttu-id="9f63c-126">MediationServerSvc.exe</span><span class="sxs-lookup"><span data-stu-id="9f63c-126">MediationServerSvc.exe</span></span>
    
      - <span data-ttu-id="9f63c-127">MRASSvc.exe</span><span class="sxs-lookup"><span data-stu-id="9f63c-127">MRASSvc.exe</span></span>
    
      - <span data-ttu-id="9f63c-128">OcsAppServerHost.exe</span><span class="sxs-lookup"><span data-stu-id="9f63c-128">OcsAppServerHost.exe</span></span>
    
      - <span data-ttu-id="9f63c-129">ReplicaReplicatorAgent.exe</span><span class="sxs-lookup"><span data-stu-id="9f63c-129">ReplicaReplicatorAgent.exe</span></span>
    
      - <span data-ttu-id="9f63c-130">ReplicationApp.exe</span><span class="sxs-lookup"><span data-stu-id="9f63c-130">ReplicationApp.exe</span></span>
    
      - <span data-ttu-id="9f63c-131">RtcHost.exe</span><span class="sxs-lookup"><span data-stu-id="9f63c-131">RtcHost.exe</span></span>
    
      - <span data-ttu-id="9f63c-132">RTCSrv.exe</span><span class="sxs-lookup"><span data-stu-id="9f63c-132">RTCSrv.exe</span></span>
    
      - <span data-ttu-id="9f63c-133">XmppProxy.exe</span><span class="sxs-lookup"><span data-stu-id="9f63c-133">XmppProxy.exe</span></span>
    
      - <span data-ttu-id="9f63c-134">XmppTGW.exe</span><span class="sxs-lookup"><span data-stu-id="9f63c-134">XmppTGW.exe</span></span>

  - <span data-ttu-id="9f63c-135">Windows Fabric Host Service のプロセス:</span><span class="sxs-lookup"><span data-stu-id="9f63c-135">Windows Fabric Host Service processes:</span></span>
    
      - <span data-ttu-id="9f63c-136">Fabric.exe</span><span class="sxs-lookup"><span data-stu-id="9f63c-136">Fabric.exe</span></span>
    
      - <span data-ttu-id="9f63c-137">FabricDCA.exe</span><span class="sxs-lookup"><span data-stu-id="9f63c-137">FabricDCA.exe</span></span>
    
      - <span data-ttu-id="9f63c-138">FabricHost.exe</span><span class="sxs-lookup"><span data-stu-id="9f63c-138">FabricHost.exe</span></span>

  - <span data-ttu-id="9f63c-139">IIS のプロセス:</span><span class="sxs-lookup"><span data-stu-id="9f63c-139">IIS processes:</span></span>
    
      - <span data-ttu-id="9f63c-140">% systemroot% \\ system32 \\ inetsrv \\w3wp.exe</span><span class="sxs-lookup"><span data-stu-id="9f63c-140">%systemroot%\\system32\\inetsrv\\w3wp.exe</span></span>
    
      - <span data-ttu-id="9f63c-141">% systemroot% \\ SysWOW64 \\ inetsrv \\w3wp.exe</span><span class="sxs-lookup"><span data-stu-id="9f63c-141">%systemroot%\\SysWOW64\\inetsrv\\w3wp.exe</span></span>

  - <span data-ttu-id="9f63c-142">SQL Server バックエンドのプロセス:</span><span class="sxs-lookup"><span data-stu-id="9f63c-142">SQL Server Back-End processes:</span></span>
    
      - <span data-ttu-id="9f63c-143">% ProgramFiles% \\ MICROSOFT SQL Server \\ MSSQL11。MSSQLSERVER \\ MSSQL \\ Binn \\SQLServr.exe</span><span class="sxs-lookup"><span data-stu-id="9f63c-143">%ProgramFiles%\\Microsoft SQL Server\\MSSQL11.MSSQLSERVER\\MSSQL\\Binn\\SQLServr.exe</span></span>
    
      - <span data-ttu-id="9f63c-144">% ProgramFiles% \\ MICROSOFT SQL Server \\ MSRS11。MSSQLSERVER \\ Reporting Services の \\ ReportServer \\ Bin \\ReportingServicesService.exe</span><span class="sxs-lookup"><span data-stu-id="9f63c-144">%ProgramFiles%\\Microsoft SQL Server\\MSRS11.MSSQLSERVER\\Reporting Services\\ReportServer\\Bin\\ReportingServicesService.exe</span></span>
    
      - <span data-ttu-id="9f63c-145">% ProgramFiles% \\ MICROSOFT SQL Server \\ MSAS11。MSSQLSERVER \\ OLAP \\ Bin \\MSMDSrv.exe</span><span class="sxs-lookup"><span data-stu-id="9f63c-145">%ProgramFiles%\\Microsoft SQL Server\\MSAS11.MSSQLSERVER\\OLAP\\Bin\\MSMDSrv.exe</span></span>

  - <span data-ttu-id="9f63c-146">SQL Server フロントエンドのプロセス:</span><span class="sxs-lookup"><span data-stu-id="9f63c-146">SQL Server Front-End processes:</span></span>
    
      - <span data-ttu-id="9f63c-147">% ProgramFiles% \\ MICROSOFT SQL Server \\ MSSQL11。LYNCLOCAL \\ MSSQL \\ Binn \\SQLServr.exe</span><span class="sxs-lookup"><span data-stu-id="9f63c-147">%ProgramFiles%\\Microsoft SQL Server\\MSSQL11.LYNCLOCAL\\MSSQL\\Binn\\SQLServr.exe</span></span>
    
      - <span data-ttu-id="9f63c-148">% ProgramFiles% \\ MICROSOFT SQL Server \\ MSSQL11。RTCLOCAL \\ MSSQL \\ Binn \\SQLServr.exe</span><span class="sxs-lookup"><span data-stu-id="9f63c-148">%ProgramFiles%\\Microsoft SQL Server\\MSSQL11.RTCLOCAL\\MSSQL\\Binn\\SQLServr.exe</span></span>

  - <span data-ttu-id="9f63c-149">ディレクトリとファイル:</span><span class="sxs-lookup"><span data-stu-id="9f63c-149">Directories and files:</span></span>
    
      - <span data-ttu-id="9f63c-150">% systemroot% \\ System32 \\ ログのログ</span><span class="sxs-lookup"><span data-stu-id="9f63c-150">%systemroot%\\System32\\LogFiles</span></span>
    
      - <span data-ttu-id="9f63c-151">% systemroot% \\ SysWow64 \\ ログ</span><span class="sxs-lookup"><span data-stu-id="9f63c-151">%systemroot%\\SysWow64\\LogFiles</span></span>
    
      - <span data-ttu-id="9f63c-152">% systemroot% \\ Microsoft.NET \\ assembly \\ GAC \_ MSIL</span><span class="sxs-lookup"><span data-stu-id="9f63c-152">%systemroot%\\Microsoft.NET\\assembly\\GAC\_MSIL</span></span>
    
      - <span data-ttu-id="9f63c-153">% programfiles% \\ Microsoft Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9f63c-153">%programfiles%\\Microsoft Lync Server 2013</span></span>
    
      - <span data-ttu-id="9f63c-154">% programfiles% \\ 共通ファイル \\ Microsoft Lync Server 2013 \\ ウォッチャーノード</span><span class="sxs-lookup"><span data-stu-id="9f63c-154">%programfiles%\\Common Files\\Microsoft Lync Server 2013\\Watcher Node</span></span>
    
      - <span data-ttu-id="9f63c-155">% programfiles% ( \\ 共通ファイル \\ Microsoft Lync Server 2013)</span><span class="sxs-lookup"><span data-stu-id="9f63c-155">%programfiles%\\Common Files\\Microsoft Lync Server 2013</span></span>
    
      - <span data-ttu-id="9f63c-156">% SystemDrive% \\ RtcReplicaRoot</span><span class="sxs-lookup"><span data-stu-id="9f63c-156">%SystemDrive%\\RtcReplicaRoot</span></span>
    
      - <span data-ttu-id="9f63c-157">ファイル共有ストア (トポロジ ビルダーで指定)。</span><span class="sxs-lookup"><span data-stu-id="9f63c-157">File share store (specified in Topology Builder).</span></span> <span data-ttu-id="9f63c-158">ファイル ストアはトポロジ ビルダーで指定されています。</span><span class="sxs-lookup"><span data-stu-id="9f63c-158">File stores are specified in Topology Builder.</span></span>
    
      - <span data-ttu-id="9f63c-159">SQL Server のデータおよびログ ファイル (バックエンド データベース、ユーザー ストア、アーカイブ ストア、監視ストア、およびアプリケーション ストア用のものを含みます)。</span><span class="sxs-lookup"><span data-stu-id="9f63c-159">SQL Server data and log files, including those for the back-end database, user store, archiving store, monitoring store, and application store.</span></span> <span data-ttu-id="9f63c-160">データベースとログ ファイルは、トポロジ ビルダーで指定できます。</span><span class="sxs-lookup"><span data-stu-id="9f63c-160">Database and log files can be specified in Topology Builder.</span></span> <span data-ttu-id="9f63c-161">既定の名前など、各データベースのデータファイルとログファイルの詳細については、「 [SQL server のデータと、Lync Server 2013 用のログファイルの配置](lync-server-2013-sql-server-data-and-log-file-placement.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9f63c-161">For details about the data and log files for each database, including default names, see [SQL Server data and log file placement for Lync Server 2013](lync-server-2013-sql-server-data-and-log-file-placement.md) in the Deployment documentation.</span></span>
    
      - <span data-ttu-id="9f63c-162">SQL Server のデータファイルとログファイル (フロントエンドデータベース、Lync ストア、および RtcDatabase store のものを含む)。</span><span class="sxs-lookup"><span data-stu-id="9f63c-162">SQL Server data and log files, including those for the Front-end database, Lync store, and RtcDatabase store.</span></span> <span data-ttu-id="9f63c-163">通常、% localdrive% csdata の下にあり \\ ます。</span><span class="sxs-lookup"><span data-stu-id="9f63c-163">They are normally under %localdrive%\\CSData.</span></span>

<span data-ttu-id="9f63c-164"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9f63c-164"></div>

<span> </span>

</div>

</div>

</span></span></div>

