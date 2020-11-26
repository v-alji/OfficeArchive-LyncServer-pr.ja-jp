---
title: 'Lync Server 2013: SQL Server データとログ ファイルの配置'
description: 'Lync Server 2013: SQL Server データとログファイルの配置。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: SQL Server data and log file placement
ms:assetid: 67aa525b-8aa3-474f-827e-8e1d4697f30f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398479(v=OCS.15)
ms:contentKeyID: 48184395
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a127254fec41a734136df9b63fc6cc8929745df7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444596"
---
# <a name="sql-server-data-and-log-file-placement-for-lync-server-2013"></a><span data-ttu-id="3de0a-103">Lync Server 2013 の SQL Server データとログ ファイルの配置</span><span class="sxs-lookup"><span data-stu-id="3de0a-103">SQL Server data and log file placement for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3de0a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3de0a-104">

<span> </span></span></span>

<span data-ttu-id="3de0a-105">_**最終更新日:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="3de0a-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="3de0a-106">Lync Server 2013 フロントエンドプール用の Microsoft SQL Server 2012 または Microsoft SQL Server 2008 R2 SP1 の計画および展開中に、パフォーマンスを考慮して、データとログファイルを物理ハードディスクに配置することが重要となります。</span><span class="sxs-lookup"><span data-stu-id="3de0a-106">During the planning and deployment of Microsoft SQL Server 2012 or Microsoft SQL Server 2008 R2 SP1 for your Lync Server 2013 Front End pool, an important consideration is the placement of data and log files onto physical hard disks for performance.</span></span> <span data-ttu-id="3de0a-107">推奨されるディスク構成は、6つのスピンドルを使用した 1 + 0 RAID セットの実装です。</span><span class="sxs-lookup"><span data-stu-id="3de0a-107">The recommended disk configuration is to implement a 1+0 RAID set using 6 spindles.</span></span> <span data-ttu-id="3de0a-108">[Lync Server 展開ウィザード] を使用して、フロントエンドプールおよび関連するサーバーの役割とサービス (つまり、アーカイブおよび監視サーバー、Lync server 通話パークサービス、Lync Server Call パークサービス、Lync Server Call パークサービス、Lync Server Call パーク service) で使用されているすべてのデータベースおよびログファイルを、良好なパフォーマンスをテストするために設定します</span><span class="sxs-lookup"><span data-stu-id="3de0a-108">Placing all database and log files that are used by the Front End pool and associated server roles and services (that is, Archiving and Monitoring Server, Lync Server Response Group service, Lync Server Call Park service) onto the RAID drive set using the Lync Server Deployment Wizard will result in a configuration that has been tested for good performance.</span></span> <span data-ttu-id="3de0a-109">次の表では、データベースファイルとその役割について説明します。</span><span class="sxs-lookup"><span data-stu-id="3de0a-109">The database files and what they are responsible for is detailed in the following table.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3de0a-110">ポリシーと SQL Server の構成でより特殊なインストールが必要な場合は、Lync Server 管理シェルを使用して、定義済みの場所にデータベースとログファイルをインストールできます。</span><span class="sxs-lookup"><span data-stu-id="3de0a-110">If your policies and SQL Server configurations require a more specialized installation, the database and log files can be installed to any pre-defined location using the Lync Server Management Shell.</span></span> <span data-ttu-id="3de0a-111">詳細については、「lync server <A href="lync-server-2013-database-installation-using-lync-server-management-shell.md">の管理シェルを使用したデータベースのインストール 2013</A> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3de0a-111">See <A href="lync-server-2013-database-installation-using-lync-server-management-shell.md">Database installation using Lync Server Management Shell in Lync Server 2013</A> for more details.</span></span>



</div>

### <a name="data-and-log-files-for-central-management-store"></a><span data-ttu-id="3de0a-112">中央管理ストアのデータとログファイル</span><span class="sxs-lookup"><span data-stu-id="3de0a-112">Data and Log Files for Central Management Store</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3de0a-113">一元管理ストアのデータベースファイル</span><span class="sxs-lookup"><span data-stu-id="3de0a-113">Central Management store database files</span></span></th>
<th><span data-ttu-id="3de0a-114">データファイルまたはログ目的</span><span class="sxs-lookup"><span data-stu-id="3de0a-114">Data file or log purpose</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3de0a-115">Xds</span><span class="sxs-lookup"><span data-stu-id="3de0a-115">Xds.ldf</span></span></p></td>
<td><p><span data-ttu-id="3de0a-116">中央管理ストアのトランザクションログファイル</span><span class="sxs-lookup"><span data-stu-id="3de0a-116">Transaction log file for the Central Management store</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3de0a-117">Xds</span><span class="sxs-lookup"><span data-stu-id="3de0a-117">Xds.mdf</span></span></p></td>
<td><p><span data-ttu-id="3de0a-118">トポロジビルダーで定義および公開されている、現在の Lync Server 2013 トポロジの構成を保持します。</span><span class="sxs-lookup"><span data-stu-id="3de0a-118">Maintains the configuration of the current Lync Server 2013 topology, as defined and published by Topology Builder</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3de0a-119">Lis</span><span class="sxs-lookup"><span data-stu-id="3de0a-119">Lis.mdf</span></span></p></td>
<td><p><span data-ttu-id="3de0a-120">位置情報サービスデータファイル</span><span class="sxs-lookup"><span data-stu-id="3de0a-120">Location Information service data file</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3de0a-121">Lis</span><span class="sxs-lookup"><span data-stu-id="3de0a-121">Lis.ldf</span></span></p></td>
<td><p><span data-ttu-id="3de0a-122">位置情報サービスデータファイルのトランザクションログ</span><span class="sxs-lookup"><span data-stu-id="3de0a-122">Transaction log for the Location Information service data file</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="data-and-log-files-for-user-conferencing-and-address-book"></a><span data-ttu-id="3de0a-123">ユーザー、会議、アドレス帳のデータとログファイル</span><span class="sxs-lookup"><span data-stu-id="3de0a-123">Data and Log files for User, Conferencing, and Address Book</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3de0a-124">主要な Lync Server 2013 データベースファイル</span><span class="sxs-lookup"><span data-stu-id="3de0a-124">Core Lync Server 2013 database files</span></span></th>
<th><span data-ttu-id="3de0a-125">データファイルまたはログ目的</span><span class="sxs-lookup"><span data-stu-id="3de0a-125">Data file or log purpose</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3de0a-126">Rtc</span><span class="sxs-lookup"><span data-stu-id="3de0a-126">Rtc.mdf</span></span></p></td>
<td><p><span data-ttu-id="3de0a-127">固定ユーザーデータ (アクセス制御リスト (Acl)、連絡先、スケジュールされた会議など)</span><span class="sxs-lookup"><span data-stu-id="3de0a-127">Persistent user data (for example, access control lists (ACLs), contacts, scheduled conferences)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3de0a-128">Rtc. .ldf</span><span class="sxs-lookup"><span data-stu-id="3de0a-128">Rtc.ldf</span></span></p></td>
<td><p><span data-ttu-id="3de0a-129">Rtc データのトランザクションログ</span><span class="sxs-lookup"><span data-stu-id="3de0a-129">Transaction log for Rtc data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3de0a-130">Rtcdyn</span><span class="sxs-lookup"><span data-stu-id="3de0a-130">Rtcdyn.mdf</span></span></p></td>
<td><p><span data-ttu-id="3de0a-131">一時的なユーザーデータ (プレゼンスランタイムデータ) を保持する</span><span class="sxs-lookup"><span data-stu-id="3de0a-131">Maintains transient user data (presence runtime data)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3de0a-132">Rtcdyn</span><span class="sxs-lookup"><span data-stu-id="3de0a-132">Rtcdyn.ldf</span></span></p></td>
<td><p><span data-ttu-id="3de0a-133">Rtcdyn データのトランザクションログ</span><span class="sxs-lookup"><span data-stu-id="3de0a-133">Transaction log for Rtcdyn data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3de0a-134">Rtcab. mdf</span><span class="sxs-lookup"><span data-stu-id="3de0a-134">Rtcab.mdf</span></span></p></td>
<td><p><span data-ttu-id="3de0a-135">リアルタイム通信 (RTC) アドレス帳データベースは、アドレス帳サービス情報が保存される SQL Server リポジトリです。</span><span class="sxs-lookup"><span data-stu-id="3de0a-135">Real-time communications (RTC) address book database is the SQL Server repository where Address Book service information is stored</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3de0a-136">Rtcab. .ldf</span><span class="sxs-lookup"><span data-stu-id="3de0a-136">Rtcab.ldf</span></span></p></td>
<td><p><span data-ttu-id="3de0a-137">アドレス帳サービスのトランザクションログ</span><span class="sxs-lookup"><span data-stu-id="3de0a-137">Transaction log for Address Book Service</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3de0a-138">Rtclocal</span><span class="sxs-lookup"><span data-stu-id="3de0a-138">Rtclocal.mdb</span></span></p></td>
<td><p><span data-ttu-id="3de0a-139">会議ディレクトリのホスト</span><span class="sxs-lookup"><span data-stu-id="3de0a-139">Hosts the conference directory</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3de0a-140">Rtcxds</span><span class="sxs-lookup"><span data-stu-id="3de0a-140">Rtcxds.mdf</span></span></p></td>
<td><p><span data-ttu-id="3de0a-141">ユーザーデータのバックアップを保持する</span><span class="sxs-lookup"><span data-stu-id="3de0a-141">Maintains the backup for user data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3de0a-142">Rtcxds</span><span class="sxs-lookup"><span data-stu-id="3de0a-142">Rtcxds.ldf</span></span></p></td>
<td><p><span data-ttu-id="3de0a-143">Rtcxds データのトランザクションログ</span><span class="sxs-lookup"><span data-stu-id="3de0a-143">Transaction log for Rtcxds data</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="data-and-log-files-for-call-park-and-response-group"></a><span data-ttu-id="3de0a-144">コールパークと応答グループのデータとログファイル</span><span class="sxs-lookup"><span data-stu-id="3de0a-144">Data and Log Files for Call Park and Response Group</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3de0a-145">アプリケーション データベース</span><span class="sxs-lookup"><span data-stu-id="3de0a-145">Application database</span></span></th>
<th><span data-ttu-id="3de0a-146">データファイルまたはログ目的</span><span class="sxs-lookup"><span data-stu-id="3de0a-146">Data file or log purpose</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3de0a-147">Cpsdyn</span><span class="sxs-lookup"><span data-stu-id="3de0a-147">Cpsdyn.mdf</span></span></p></td>
<td><p><span data-ttu-id="3de0a-148">コールパークアプリケーションの動的情報データベース</span><span class="sxs-lookup"><span data-stu-id="3de0a-148">Dynamic information database for the Call Park application</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3de0a-149">Cpsdyn</span><span class="sxs-lookup"><span data-stu-id="3de0a-149">Cpsdyn.ldf</span></span></p></td>
<td><p><span data-ttu-id="3de0a-150">コールパークアプリケーションデータファイルのトランザクションログ</span><span class="sxs-lookup"><span data-stu-id="3de0a-150">Transaction log for Call Park application data file</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3de0a-151">Rgsconfig</span><span class="sxs-lookup"><span data-stu-id="3de0a-151">Rgsconfig.mdf</span></span></p></td>
<td><p><span data-ttu-id="3de0a-152">サービスの構成用の Lync サーバー応答グループサービスデータファイル</span><span class="sxs-lookup"><span data-stu-id="3de0a-152">Lync Server Response Group service data file for the configuration of the services</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3de0a-153">Rgsconfig</span><span class="sxs-lookup"><span data-stu-id="3de0a-153">Rgsconfig.ldf</span></span></p></td>
<td><p><span data-ttu-id="3de0a-154">応答グループアプリケーション構成のトランザクションログファイル</span><span class="sxs-lookup"><span data-stu-id="3de0a-154">Transaction log file for the Response Group application configuration</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3de0a-155">Rgsdyn</span><span class="sxs-lookup"><span data-stu-id="3de0a-155">Rgsdyn.mdf</span></span></p></td>
<td><p><span data-ttu-id="3de0a-156">ランタイム操作の応答グループサービスデータファイル</span><span class="sxs-lookup"><span data-stu-id="3de0a-156">Response Group service data file for runtime operations</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3de0a-157">Rgsdyn</span><span class="sxs-lookup"><span data-stu-id="3de0a-157">Rgsdyn.ldf</span></span></p></td>
<td><p><span data-ttu-id="3de0a-158">応答グループサービスランタイムデータファイルのトランザクションログ</span><span class="sxs-lookup"><span data-stu-id="3de0a-158">Transaction log for the Response Group service runtime data file</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="data-and-log-files-for-archiving-and-monitoring-server"></a><span data-ttu-id="3de0a-159">アーカイブおよび監視サーバー用のデータとログファイル</span><span class="sxs-lookup"><span data-stu-id="3de0a-159">Data and Log Files for Archiving and Monitoring Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3de0a-160">データベースファイルのアーカイブと監視</span><span class="sxs-lookup"><span data-stu-id="3de0a-160">Archiving and Monitoring database files</span></span></th>
<th><span data-ttu-id="3de0a-161">データファイルまたはログ目的</span><span class="sxs-lookup"><span data-stu-id="3de0a-161">Data file or log purpose</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3de0a-162">LcsCdr mdf</span><span class="sxs-lookup"><span data-stu-id="3de0a-162">LcsCdr.mdf</span></span></p></td>
<td><p><span data-ttu-id="3de0a-163">監視サーバーの通話の詳細記録 (CDR) プロセスのデータストア</span><span class="sxs-lookup"><span data-stu-id="3de0a-163">Data store for the call detail recording (CDR) process of the Monitoring Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3de0a-164">LcsCdr .ldf</span><span class="sxs-lookup"><span data-stu-id="3de0a-164">LcsCdr.ldf</span></span></p></td>
<td><p><span data-ttu-id="3de0a-165">通話の詳細記録 (CDR) データのトランザクションログ</span><span class="sxs-lookup"><span data-stu-id="3de0a-165">Transaction log for call detail recording (CDR) data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3de0a-166">QoEMetrics</span><span class="sxs-lookup"><span data-stu-id="3de0a-166">QoEMetrics.mdf</span></span></p></td>
<td><p><span data-ttu-id="3de0a-167">監視サーバーから保存された環境の品質データファイル</span><span class="sxs-lookup"><span data-stu-id="3de0a-167">Quality of Experience data file stored from the Monitoring Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3de0a-168">QoEMetrics</span><span class="sxs-lookup"><span data-stu-id="3de0a-168">QoEMetrics.ldf</span></span></p></td>
<td><p><span data-ttu-id="3de0a-169">データを監視するためのトランザクションログ</span><span class="sxs-lookup"><span data-stu-id="3de0a-169">Transaction log for Monitoring data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3de0a-170">Lcslog</span><span class="sxs-lookup"><span data-stu-id="3de0a-170">Lcslog.mdf</span></span></p></td>
<td><p><span data-ttu-id="3de0a-171">アーカイブサーバー上のインスタントメッセージングと会議データの保持に使用するデータファイル</span><span class="sxs-lookup"><span data-stu-id="3de0a-171">Data file for the retention of instant messaging and conferencing data on an Archiving Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3de0a-172">Lcslog</span><span class="sxs-lookup"><span data-stu-id="3de0a-172">Lcslog.ldf</span></span></p></td>
<td><p><span data-ttu-id="3de0a-173">データをアーカイブするためのトランザクションログ</span><span class="sxs-lookup"><span data-stu-id="3de0a-173">Transaction log for Archiving data</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3de0a-174">このトピックでは、ディスクと RAID セットへの参照が行われます。</span><span class="sxs-lookup"><span data-stu-id="3de0a-174">In this topic, references are made to disk and to RAID set.</span></span> <span data-ttu-id="3de0a-175">ディスクを参照する SQL Server リソースの構成では、単一のハードウェアデバイスを指します。</span><span class="sxs-lookup"><span data-stu-id="3de0a-175">Note that in the configuration of SQL Server resources, referring to a disk means a single hardware device.</span></span> <span data-ttu-id="3de0a-176">2つのパーティション、1つのログファイルを保持する他のパーティションのハードディスクドライブは、それぞれログファイルまたはデータファイル専用の2つのディスクとは異なります。</span><span class="sxs-lookup"><span data-stu-id="3de0a-176">A hard disk drive with two partitions, one holding log files and the other partition holding data files, is not the same as two disks, each dedicated to either log or data files.</span></span>

<span data-ttu-id="3de0a-177">RAID セットのリファレンスとして、さまざまなベンダーからのさまざまな RAID テクノロジが用意されています。</span><span class="sxs-lookup"><span data-stu-id="3de0a-177">In reference to RAID sets, there are a number of different RAID technologies from various vendors.</span></span> <span data-ttu-id="3de0a-178">また、ストレージエリアネットワーク (SAN) が普及しているため、単一システム専用の RAID セットは非常にまれです。</span><span class="sxs-lookup"><span data-stu-id="3de0a-178">And, with the proliferation of storage area networks (SAN), RAID sets dedicated to a single system are rarer.</span></span> <span data-ttu-id="3de0a-179">Lync Server 2013 で SQL Server のパフォーマンスを構成する場合は、使用しているディスクレイアウトの最適な構成を判断するために、お使いの RAID または SAN ベンダーにお問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="3de0a-179">You should consult with your RAID or SAN vendor to determine what the best configuration is for your disk layout when configuring for SQL Server performance with Lync Server 2013.</span></span>

<span data-ttu-id="3de0a-180">また、ディスクドライブがすべて同じではないことにも注意してください。他の機能よりも優れたパフォーマンスを発揮します。</span><span class="sxs-lookup"><span data-stu-id="3de0a-180">Note also that not all disk drives are created equally; some perform better than others.</span></span> <span data-ttu-id="3de0a-181">同じ製造元のドライブでも、回転速度、ハードウェアキャッシュサイズ、その他の要因によってパフォーマンスが異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="3de0a-181">Even drives from the same manufacturer can vary in performance because of rotational speed, hardware cache size, and other factors.</span></span>

<span data-ttu-id="3de0a-182"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3de0a-182"></div>

<span> </span>

</div>

</div>

</span></span></div>

