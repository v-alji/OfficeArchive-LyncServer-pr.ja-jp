---
title: 'Lync Server 2013: バックアップと復元の要件: ツールと権限'
description: 'Lync Server 2013: バックアップと復元の要件: ツールと権限。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: 'Backup and restoration requirements: tools and permissions'
ms:assetid: 35ec2e33-f33e-4f84-9e64-6550fd78aa52
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202171(v=OCS.15)
ms:contentKeyID: 51541465
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 36327d1214854586b44024f126bbd87acad6c4b2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437981"
---
# <a name="backup-and-restoration-requirements-in-lync-server-2013-tools-and-permissions"></a><span data-ttu-id="9e56d-103">Lync Server 2013 でのバックアップと復元の要件: ツールと権限</span><span class="sxs-lookup"><span data-stu-id="9e56d-103">Backup and restoration requirements in Lync Server 2013: tools and permissions</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9e56d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9e56d-104">

<span> </span></span></span>

<span data-ttu-id="9e56d-105">_**最終更新日:** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="9e56d-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<span data-ttu-id="9e56d-106">このトピックでは、Lync Server 2013 のバックアップと復元に使用できるツール、必要なアクセス許可、コマンドをリモートまたはローカルで実行できるかどうかについて説明します。</span><span class="sxs-lookup"><span data-stu-id="9e56d-106">This topic identifies the tools that you can use to back up and restore Lync Server 2013, the permissions that you need, and whether you can run commands remotely or locally.</span></span> <span data-ttu-id="9e56d-107">具体的には、このトピックでは、Lync Server にバックアップと復元のために提供されるツールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="9e56d-107">Specifically, this topic focuses on tools that are provided with Lync Server for backup and restoration.</span></span>

<div>

## <a name="backups"></a><span data-ttu-id="9e56d-108">バックアップ</span><span class="sxs-lookup"><span data-stu-id="9e56d-108">Backups</span></span>

<span data-ttu-id="9e56d-109">Lync Server をバックアップするには、次の表で示されているツールを使用します。</span><span class="sxs-lookup"><span data-stu-id="9e56d-109">To back up Lync Server, use the tools identified in the following table.</span></span> <span data-ttu-id="9e56d-110">Lync Server のバックアップに必要なすべてのコマンドをスクリプト化して、リモートで実行することができます。</span><span class="sxs-lookup"><span data-stu-id="9e56d-110">All the commands that you need to back up Lync Server can be scripted and can be run remotely.</span></span>

### <a name="tools-for-backing-up-lync-server"></a><span data-ttu-id="9e56d-111">Lync Server のバックアップツール</span><span class="sxs-lookup"><span data-stu-id="9e56d-111">Tools for Backing Up Lync Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9e56d-112">バックアップするには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="9e56d-112">To back up this:</span></span></th>
<th><span data-ttu-id="9e56d-113">このツールまたはコマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="9e56d-113">Use this tool or cmdlet:</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9e56d-114">トポロジ構成データ (Xds)</span><span class="sxs-lookup"><span data-stu-id="9e56d-114">Topology configuration data (Xds.mdf)</span></span></p></td>
<td><p><span data-ttu-id="9e56d-115">Export-CsConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e56d-115">Export-CsConfiguration</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e56d-116">位置情報サービス (E9-1) データ (Lis)</span><span class="sxs-lookup"><span data-stu-id="9e56d-116">Location information service (E9-1-1) data (Lis.mdf)</span></span></p></td>
<td><p><span data-ttu-id="9e56d-117">Export-CsLisConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e56d-117">Export-CsLisConfiguration</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e56d-118">応答グループの構成データ (RgsConfig)</span><span class="sxs-lookup"><span data-stu-id="9e56d-118">Response Group configuration data (RgsConfig.mdf)</span></span></p></td>
<td><p><span data-ttu-id="9e56d-119">Export-CsRgsConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e56d-119">Export-CsRgsConfiguration</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e56d-120">常設ユーザーデータ (Rtcxds データベース)</span><span class="sxs-lookup"><span data-stu-id="9e56d-120">Persistent user data (Rtcxds.mdf database)</span></span></p>
<p><span data-ttu-id="9e56d-121">会議 Id</span><span class="sxs-lookup"><span data-stu-id="9e56d-121">Conference IDs</span></span></p></td>
<td><p><span data-ttu-id="9e56d-122">Export-CsUserData</span><span class="sxs-lookup"><span data-stu-id="9e56d-122">Export-CsUserData</span></span></p></td>
</tr>
<tr class="odd">
<td><ul>
<li><p><span data-ttu-id="9e56d-123">アーカイブデータベース (LcsLog)</span><span class="sxs-lookup"><span data-stu-id="9e56d-123">Archiving database (LcsLog.mdf)</span></span></p></li>
<li><p><span data-ttu-id="9e56d-124">通話の詳細レコードデータベース (LcsCDR. mdf) を監視する</span><span class="sxs-lookup"><span data-stu-id="9e56d-124">Monitoring call detail record database (LcsCDR.mdf)</span></span></p></li>
<li><p><span data-ttu-id="9e56d-125">QoE データベース (QoEMetrics) の監視</span><span class="sxs-lookup"><span data-stu-id="9e56d-125">Monitoring QoE database (QoEMetrics.mdf)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="9e56d-126">Sql server Management Studio などの SQL Server データベースツール</span><span class="sxs-lookup"><span data-stu-id="9e56d-126">SQL Server database tool, such as SQL Server Management Studio</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e56d-127">常設チャットデータベース (行う)</span><span class="sxs-lookup"><span data-stu-id="9e56d-127">Persistent Chat database (Mgc.mdf)</span></span></p></td>
<td><p><span data-ttu-id="9e56d-128">SQL Server のバックアップ手順またはエクスポート-CsPersistentChatData。</span><span class="sxs-lookup"><span data-stu-id="9e56d-128">SQL Server backup procedures or Export-CsPersistentChatData.</span></span> <span data-ttu-id="9e56d-129">Export-CsPersistentChatData 永続的なチャットデータをファイルとしてエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="9e56d-129">Export-CsPersistentChatData exports Persistent Chat data as a file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e56d-130">すべてのファイルストア: Lync Server ファイルストア、アーカイブファイルストア</span><span class="sxs-lookup"><span data-stu-id="9e56d-130">All file stores: Lync Server file store, Archiving file store</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="9e56d-131">" <STRONG>Meeting. Active</STRONG> " という名前のファイルはバックアップしないでください。</span><span class="sxs-lookup"><span data-stu-id="9e56d-131">Files named <STRONG>Meeting.Active</STRONG> should not be backed up.</span></span> <span data-ttu-id="9e56d-132">これらのファイルは、会議の実行時に使用され、ロックされます。</span><span class="sxs-lookup"><span data-stu-id="9e56d-132">These files are in use and locked while a meeting takes place.</span></span>


</div></td>
<td><p><span data-ttu-id="9e56d-133">標準ファイルシステム管理ツール (Robocopy など)。</span><span class="sxs-lookup"><span data-stu-id="9e56d-133">Standard file system management tool, such as Robocopy.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="restoration"></a><span data-ttu-id="9e56d-134">回復</span><span class="sxs-lookup"><span data-stu-id="9e56d-134">Restoration</span></span>

<span data-ttu-id="9e56d-135">Lync Server を復元するには、次の表のツールを使用します。</span><span class="sxs-lookup"><span data-stu-id="9e56d-135">To restore Lync Server, use the tools in the following table.</span></span> <span data-ttu-id="9e56d-136">Lync Server を復元するために必要なすべてのコマンドをスクリプト化することができます。</span><span class="sxs-lookup"><span data-stu-id="9e56d-136">All the commands that you need to restore Lync Server can be scripted.</span></span> <span data-ttu-id="9e56d-137">一部はリモートで実行できますが、次の表に示すようにローカルで実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e56d-137">Some can be run remotely, but others need to be run locally, as specified in the following table.</span></span>

### <a name="tools-for-restoring-lync-server"></a><span data-ttu-id="9e56d-138">Lync Server を復元するためのツール</span><span class="sxs-lookup"><span data-stu-id="9e56d-138">Tools for Restoring Lync Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9e56d-139">その手順は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="9e56d-139">To do this:</span></span></th>
<th><span data-ttu-id="9e56d-140">このツールまたはコマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="9e56d-140">Use this tool or cmdlet:</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9e56d-141">新しいコンピューターまたはクリーンコンピューターを作成する</span><span class="sxs-lookup"><span data-stu-id="9e56d-141">Build a new or clean computer</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="9e56d-142">Windows オペレーティングシステムのインストールソフトウェア</span><span class="sxs-lookup"><span data-stu-id="9e56d-142">Windows operating system installation software</span></span></p></li>
<li><p><span data-ttu-id="9e56d-143">SQL Server インストールソフトウェア</span><span class="sxs-lookup"><span data-stu-id="9e56d-143">SQL Server installation software</span></span></p></li>
<li><p><span data-ttu-id="9e56d-144">証明書 Microsoft 管理コンソール (MMC) スナップイン (エクスポート可能な秘密キーで証明書を復元する場合)</span><span class="sxs-lookup"><span data-stu-id="9e56d-144">Certificates Microsoft Management Console (MMC) snap-in, if restoring certificates with an exportable private key</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e56d-145">ファイルストアデータを復元する</span><span class="sxs-lookup"><span data-stu-id="9e56d-145">Restore file store data</span></span></p></td>
<td><p><span data-ttu-id="9e56d-146">標準ファイルシステム管理ツール (Robocopy など)</span><span class="sxs-lookup"><span data-stu-id="9e56d-146">Standard file system management tool, such as Robocopy</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e56d-147">空のデータベースを再作成し、次の権限を設定します。</span><span class="sxs-lookup"><span data-stu-id="9e56d-147">Recreate empty databases and set permissions for the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="9e56d-148">中央管理ストア</span><span class="sxs-lookup"><span data-stu-id="9e56d-148">Central Management store</span></span></p></li>
<li><p><span data-ttu-id="9e56d-149">バック エンド サーバー</span><span class="sxs-lookup"><span data-stu-id="9e56d-149">Back End Server</span></span></p></li>
<li><p><span data-ttu-id="9e56d-150">監視データベース</span><span class="sxs-lookup"><span data-stu-id="9e56d-150">Monitoring database</span></span></p></li>
<li><p><span data-ttu-id="9e56d-151">アーカイブ データベース</span><span class="sxs-lookup"><span data-stu-id="9e56d-151">Archiving database</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="9e56d-152">Install-CsDatabase</span><span class="sxs-lookup"><span data-stu-id="9e56d-152">Install-CsDatabase</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e56d-153">Active Directory ドメインサービスのポインターを中央管理ストアに復元します。</span><span class="sxs-lookup"><span data-stu-id="9e56d-153">Restore the Active Directory Domain Services pointer to the Central Management store</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="9e56d-154">サービス接続ポイントをいつでも紛失した場合は、このコマンドレットを再実行できます。</span><span class="sxs-lookup"><span data-stu-id="9e56d-154">If you lose the service connection point at any time, you can rerun this cmdlet.</span></span>


</div></td>
<td><p><span data-ttu-id="9e56d-155">Set-CsConfigurationStoreLocation</span><span class="sxs-lookup"><span data-stu-id="9e56d-155">Set-CsConfigurationStoreLocation</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e56d-156">トポロジ、ポリシー、構成の設定を中央管理ストア (Xds) にインポートする</span><span class="sxs-lookup"><span data-stu-id="9e56d-156">Import the topology, policies, and configuration settings to the Central Management store (Xds.mdf)</span></span></p></td>
<td><p><span data-ttu-id="9e56d-157">Import-CsConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e56d-157">Import-CsConfiguration</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e56d-158">トポロジを公開して有効にする</span><span class="sxs-lookup"><span data-stu-id="9e56d-158">Publish and enable the topology</span></span></p></td>
<td><p><span data-ttu-id="9e56d-159">トポロジ ビルダー</span><span class="sxs-lookup"><span data-stu-id="9e56d-159">Topology Builder</span></span></p>
<p><span data-ttu-id="9e56d-160">/</span><span class="sxs-lookup"><span data-stu-id="9e56d-160">-or-</span></span></p>
<p><span data-ttu-id="9e56d-161">Publish-CsTopology と Enable-CsTopology</span><span class="sxs-lookup"><span data-stu-id="9e56d-161">Publish-CsTopology and Enable-CsTopology</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e56d-162">最後に公開されたトポロジを有効にする</span><span class="sxs-lookup"><span data-stu-id="9e56d-162">Enable the last published topology</span></span></p></td>
<td><p><span data-ttu-id="9e56d-163">Enable-CsTopology</span><span class="sxs-lookup"><span data-stu-id="9e56d-163">Enable-CsTopology</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e56d-164">Lync Server コンポーネントを再インストールする</span><span class="sxs-lookup"><span data-stu-id="9e56d-164">Reinstall Lync Server components</span></span></p></td>
<td><p><span data-ttu-id="9e56d-165">Lync Server のセットアップ</span><span class="sxs-lookup"><span data-stu-id="9e56d-165">Lync Server Setup</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="9e56d-166">Lync Server のインストールフォルダーまたは \setup\amd64\Setup.exe のメディアにあります。</span><span class="sxs-lookup"><span data-stu-id="9e56d-166">Located in the Lync Server installation folder or media at \setup\amd64\Setup.exe.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e56d-167">位置情報 (E9-1) データ (Lis) を復元する</span><span class="sxs-lookup"><span data-stu-id="9e56d-167">Restore location information (E9-1-1) data (Lis.mdf)</span></span></p></td>
<td><p><span data-ttu-id="9e56d-168">Import-CsLisConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e56d-168">Import-CsLisConfiguration</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e56d-169">永続的なユーザーデータ (Rtcxds) を復元する</span><span class="sxs-lookup"><span data-stu-id="9e56d-169">Restore persistent user data (Rtcxds.mdf)</span></span></p></td>
<td><p><span data-ttu-id="9e56d-170">Import-CsUserData</span><span class="sxs-lookup"><span data-stu-id="9e56d-170">Import-CsUserData</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e56d-171">応答グループの構成データ (RgsConfig) を復元する</span><span class="sxs-lookup"><span data-stu-id="9e56d-171">Restore Response Group configuration data (RgsConfig.mdf)</span></span></p></td>
<td><p><span data-ttu-id="9e56d-172">Import-CsRgsConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e56d-172">Import-CsRgsConfiguration</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="9e56d-173">データベースに応答グループデータがない、新しく展開されたプールで構成を復元する場合は、– OverwriteOwner オプションを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e56d-173">If the configuration is being restored in a newly deployed pool that has no Response Group data in the database, then you should use the –OverwriteOwner option.</span></span> <span data-ttu-id="9e56d-174">復元されるデータが、同じ完全修飾ドメイン名 (FQDN) を持つプールにある場合でも、このオプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="9e56d-174">Use this option even if the data being restored is in a pool with the same fully qualified domain name (FQDN).</span></span> <span data-ttu-id="9e56d-175">そうしないと、アクティブディレクトリに既に存在する返信グループに連絡先オブジェクトが存在するため、インポートは成功しません。</span><span class="sxs-lookup"><span data-stu-id="9e56d-175">Otherwise, the import will not succeed, due to the contact objects to the Response Groups already existing in Active Directory.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e56d-176">次のデータベースを復元します。</span><span class="sxs-lookup"><span data-stu-id="9e56d-176">Restore the following databases:</span></span></p>
<ul>
<li><p><span data-ttu-id="9e56d-177">アーカイブデータベース (LcsLog)</span><span class="sxs-lookup"><span data-stu-id="9e56d-177">Archiving database (LcsLog.mdf)</span></span></p></li>
<li><p><span data-ttu-id="9e56d-178">監視データベース: call detail レコードデータベース (LcsCDR mdf) と QoE データベース (QoEMetrics)</span><span class="sxs-lookup"><span data-stu-id="9e56d-178">Monitoring databases: call detail record database (LcsCDR.mdf) and QoE database (QoEMetrics.mdf)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="9e56d-179">SQL Server データベース管理ツール</span><span class="sxs-lookup"><span data-stu-id="9e56d-179">SQL Server database management tools</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e56d-180">常設チャットデータベース (Mgs)</span><span class="sxs-lookup"><span data-stu-id="9e56d-180">Persistent Chat database (Mgs.mdf)</span></span></p></td>
<td><p><span data-ttu-id="9e56d-181">SQL Server の復元手順またはインポート-CsPersistentChatData。</span><span class="sxs-lookup"><span data-stu-id="9e56d-181">SQL Server restore procedures or Import-CsPersistentChatData.</span></span> <span data-ttu-id="9e56d-182">Import-CsPersistentChatData は、CsPersistentChatData によって作成されたファイルと共に使用でき、データは永続的なチャットデータベースにインポートされます。</span><span class="sxs-lookup"><span data-stu-id="9e56d-182">You can use Import-CsPersistentChatData with a file created by Export-CsPersistentChatData, and the data will be imported into the Persistent Chat database.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="required-permissions"></a><span data-ttu-id="9e56d-183">必要なアクセス許可</span><span class="sxs-lookup"><span data-stu-id="9e56d-183">Required Permissions</span></span>

<span data-ttu-id="9e56d-184">このトピックで説明されているすべてのコマンドを実行するには、ユーザーが **RTCUniversalServerAdmins** group のメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e56d-184">Users must be a member of the **RTCUniversalServerAdmins** group to perform all the commands described in this topic.</span></span> <span data-ttu-id="9e56d-185">ほとんどのバックアップと復元コマンドは、役割ベースのアクセス制御 (RBAC) をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="9e56d-185">Most backup and restore commands do not support role-based access control (RBAC).</span></span> <span data-ttu-id="9e56d-186">2つの例外は永続的なチャットコマンドレット Export-CsPersistentChatData とインポート-CsPersistentChatData であり、CsPersistentChatAdministrator グループのメンバーであるユーザーが実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e56d-186">Two exceptions are the Persistent Chat cmdlets Export-CsPersistentChatData and Import-CsPersistentChatData, which must be run by a user who is a member of the CsPersistentChatAdministrator group.</span></span> <span data-ttu-id="9e56d-187">Lync Server 展開ウィザードを実行するには、ユーザーはローカルの [電話番号] グループのメンバーでもある必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e56d-187">To run Lync Server Deployment Wizard, a user must also be a member of the Local Adminstrators group.</span></span>

<span data-ttu-id="9e56d-188"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9e56d-188"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

