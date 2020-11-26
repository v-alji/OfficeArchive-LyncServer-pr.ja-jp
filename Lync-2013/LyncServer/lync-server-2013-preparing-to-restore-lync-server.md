---
title: 'Lync Server 2013: Lync Server を復元するための準備'
description: 'Lync Server 2013: Lync Server を復元するための準備をしています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing to restore Lync Server
ms:assetid: 857e4e02-908e-433a-96c6-be1795a9cb61
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202179(v=OCS.15)
ms:contentKeyID: 51541490
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1875a691cfb70a6a824ab19bfde3dee4d699e48a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424094"
---
# <a name="preparing-to-restore-lync-server-2013"></a><span data-ttu-id="9e7f7-103">Lync Server 2013 を復元するための準備</span><span class="sxs-lookup"><span data-stu-id="9e7f7-103">Preparing to restore Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9e7f7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9e7f7-104">

<span> </span></span></span>

<span data-ttu-id="9e7f7-105">_**最終更新日:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="9e7f7-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="9e7f7-106">障害の後にサーバーとデータベースの復元を開始する前に、次のことを決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e7f7-106">Before you begin restoring servers and databases after a failure, you need to determine the following:</span></span>

  - <span data-ttu-id="9e7f7-107">何を復元する必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="9e7f7-107">What needs to be restored.</span></span>

  - <span data-ttu-id="9e7f7-108">復元に必要なハードウェア、ソフトウェア、データ、およびツール。</span><span class="sxs-lookup"><span data-stu-id="9e7f7-108">The hardware, software, data, and tools you need for restoration.</span></span>

<div>

## <a name="determining-what-to-restore"></a><span data-ttu-id="9e7f7-109">復元するものを決定する</span><span class="sxs-lookup"><span data-stu-id="9e7f7-109">Determining What to Restore</span></span>

<span data-ttu-id="9e7f7-110">このトピックでは、サーバー、プール、または全体管理ストアのレベルで発生した Lync Server の停止を復元する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9e7f7-110">This topic describes how to restore Lync Server outages that occur at the server, pool, or Central Management store level.</span></span> <span data-ttu-id="9e7f7-111">サーバーの全体管理ストアで障害が発生した場合、Lync Server の展開は機能し続けますが、構成を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="9e7f7-111">If the Central Management store fails, your Lync Server deployment continues to function, but you cannot make any configuration changes.</span></span> <span data-ttu-id="9e7f7-112">バックエンドサーバーまたは Standard Edition サーバーに障害が発生した場合、ユーザープールは機能しなくなります。</span><span class="sxs-lookup"><span data-stu-id="9e7f7-112">If a Back End Server or Standard Edition server fails, the user pool stops functioning.</span></span> <span data-ttu-id="9e7f7-113">他のサーバーで障害が発生した場合、このエラーの大きさは、サーバーが実行しているサーバーの役割と、サーバーが1つ以上のデータベースをホストしているかどうかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="9e7f7-113">If any other server fails, the magnitude of the failure depends on the server role the server is running and whether the server hosts one or more databases.</span></span>

### <a name="what-to-restore"></a><span data-ttu-id="9e7f7-114">復元方法</span><span class="sxs-lookup"><span data-stu-id="9e7f7-114">What to Restore</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9e7f7-115">失敗した場合</span><span class="sxs-lookup"><span data-stu-id="9e7f7-115">If this failed</span></span></th>
<th><span data-ttu-id="9e7f7-116">以下のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9e7f7-116">See this section:</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9e7f7-117">Standard Edition サーバー</span><span class="sxs-lookup"><span data-stu-id="9e7f7-117">Standard Edition server</span></span></p></td>
<td><p><span data-ttu-id="9e7f7-118"><a href="lync-server-2013-restoring-a-standard-edition-server.md">Lync Server 2013 での Standard Edition サーバーの復元</a></span><span class="sxs-lookup"><span data-stu-id="9e7f7-118"><a href="lync-server-2013-restoring-a-standard-edition-server.md">Restoring a Standard Edition server in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e7f7-119">中央管理ストア</span><span class="sxs-lookup"><span data-stu-id="9e7f7-119">Central Management store</span></span></p></td>
<td><p><span data-ttu-id="9e7f7-120"><a href="lync-server-2013-restoring-the-server-hosting-the-central-management-store.md">Lync Server 2013 での中央管理ストアをホストしているサーバーの復元</a></span><span class="sxs-lookup"><span data-stu-id="9e7f7-120"><a href="lync-server-2013-restoring-the-server-hosting-the-central-management-store.md">Restoring the server hosting the Central Management store in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e7f7-121">Enterprise Edition のバックエンド</span><span class="sxs-lookup"><span data-stu-id="9e7f7-121">Enterprise Edition Back End</span></span></p></td>
<td><p><span data-ttu-id="9e7f7-122"><a href="lync-server-2013-restoring-an-enterprise-edition-back-end-server.md">Lync Server 2013 で Enterprise Edition バックエンドサーバーを復元する</a></span><span class="sxs-lookup"><span data-stu-id="9e7f7-122"><a href="lync-server-2013-restoring-an-enterprise-edition-back-end-server.md">Restoring an Enterprise Edition Back End Server in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e7f7-123">Enterprise Edition のミラーバックエンドプライマリサーバー</span><span class="sxs-lookup"><span data-stu-id="9e7f7-123">Enterprise Edition Mirrored Back End Primary Server</span></span></p></td>
<td><p><span data-ttu-id="9e7f7-124"><a href="lync-server-2013-restoring-a-mirrored-enterprise-edition-back-end-server-primary.md">Lync Server 2013 でのミラー化された Enterprise Edition バックエンドサーバーの復元-プライマリ</a></span><span class="sxs-lookup"><span data-stu-id="9e7f7-124"><a href="lync-server-2013-restoring-a-mirrored-enterprise-edition-back-end-server-primary.md">Restoring a mirrored Enterprise Edition Back End Server in Lync Server 2013 - primary</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e7f7-125">Enterprise Edition のミラーリングされたバックエンドセカンダリサーバー</span><span class="sxs-lookup"><span data-stu-id="9e7f7-125">Enterprise Edition Mirrored Back End Secondary Server</span></span></p></td>
<td><p><span data-ttu-id="9e7f7-126"><a href="lync-server-2013-restoring-a-mirrored-enterprise-edition-back-end-server-mirror.md">Lync Server 2013-mirror でのミラー化された Enterprise Edition バックエンドサーバーの復元</a></span><span class="sxs-lookup"><span data-stu-id="9e7f7-126"><a href="lync-server-2013-restoring-a-mirrored-enterprise-edition-back-end-server-mirror.md">Restoring a mirrored Enterprise Edition Back End Server in Lync Server 2013 - mirror</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e7f7-127">フロントエンドサーバー、エッジサーバー、監督、仲介サーバー、常設チャットサーバーなど、サーバーの役割を実行している Enterprise Edition サーバー。</span><span class="sxs-lookup"><span data-stu-id="9e7f7-127">Any Enterprise Edition server running a server role, such as a Front End Server, Edge Server, Director, Mediation Server,.or Persistent Chat Server.</span></span></p></td>
<td><p><span data-ttu-id="9e7f7-128"><a href="lync-server-2013-restoring-an-enterprise-edition-member-server.md">Lync Server 2013 で Enterprise Edition メンバーサーバーを復元する</a></span><span class="sxs-lookup"><span data-stu-id="9e7f7-128"><a href="lync-server-2013-restoring-an-enterprise-edition-member-server.md">Restoring an Enterprise Edition member server in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e7f7-129">Lync Server プール全体</span><span class="sxs-lookup"><span data-stu-id="9e7f7-129">An entire Lync Server pool</span></span></p></td>
<td><p><span data-ttu-id="9e7f7-130"><a href="lync-server-2013-restoring-a-lync-server-pool.md">Lync server 2013 での Lync Server プールの復元</a></span><span class="sxs-lookup"><span data-stu-id="9e7f7-130"><a href="lync-server-2013-restoring-a-lync-server-pool.md">Restoring a Lync Server pool in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e7f7-131">Enterprise Edition ファイルストア</span><span class="sxs-lookup"><span data-stu-id="9e7f7-131">Enterprise Edition File Store</span></span></p></td>
<td><p><span data-ttu-id="9e7f7-132"><a href="lync-server-2013-restoring-a-file-store.md">Lync Server 2013 でのファイルストアの復元</a></span><span class="sxs-lookup"><span data-stu-id="9e7f7-132"><a href="lync-server-2013-restoring-a-file-store.md">Restoring a file store in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e7f7-133">スタンドアロンの監視データベースまたはアーカイブデータベース</span><span class="sxs-lookup"><span data-stu-id="9e7f7-133">A standalone Monitoring database or Archiving database</span></span></p></td>
<td><p><span data-ttu-id="9e7f7-134"><a href="lync-server-2013-restoring-monitoring-or-archiving-data.md">Lync Server 2013 での監視またはアーカイブデータの復元</a></span><span class="sxs-lookup"><span data-stu-id="9e7f7-134"><a href="lync-server-2013-restoring-monitoring-or-archiving-data.md">Restoring monitoring or archiving data in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e7f7-135">スタンドアロンの常設チャットデータベース</span><span class="sxs-lookup"><span data-stu-id="9e7f7-135">A stand-alone Persistent Chat database</span></span></p></td>
<td><p><span data-ttu-id="9e7f7-136"><a href="lync-server-2013-restoring-persistent-chat-data.md">Lync Server 2013 での常設チャットデータの復元</a></span><span class="sxs-lookup"><span data-stu-id="9e7f7-136"><a href="lync-server-2013-restoring-persistent-chat-data.md">Restoring Persistent Chat data in Lync Server 2013</a></span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="gathering-hardware-software-and-tools"></a><span data-ttu-id="9e7f7-137">ハードウェア、ソフトウェア、ツールの収集</span><span class="sxs-lookup"><span data-stu-id="9e7f7-137">Gathering Hardware, Software, and Tools</span></span>

<span data-ttu-id="9e7f7-138">サーバーを復元する場合は、新しいコンピューターまたはクリーンコンピューターから起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e7f7-138">When you restore a server, you need to start with a new or clean computer.</span></span> <span data-ttu-id="9e7f7-139">さらに、次のハードウェアとソフトウェアを使用できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e7f7-139">Additionally, you must have the following hardware and software available:</span></span>

  - <span data-ttu-id="9e7f7-140">障害が発生したサーバーと同じ完全修飾ドメイン名 (FQDN) を含むクリーンなサーバーまたは新規サーバー。</span><span class="sxs-lookup"><span data-stu-id="9e7f7-140">A clean or new server with the same fully qualified domain name (FQDN) as the server that failed.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="9e7f7-141">オペレーティングシステムをインストールするときには、Active Directory ドメインサービスでコンピューターアカウントを削除していないことを確認して、アカウントのグループアクセス許可が保持されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9e7f7-141">When you install the operating system, make sure that you do not delete the computer account in Active Directory Domain Services, and verify that the group permissions for the account are retained.</span></span>

    
    </div>

  - <span data-ttu-id="9e7f7-142">オペレーティングシステムのインストールソフトウェア。</span><span class="sxs-lookup"><span data-stu-id="9e7f7-142">Installation software for the operating system.</span></span> <span data-ttu-id="9e7f7-143">オペレーティングシステムをインストールするには、組織によって確立されたサーバーの展開手順と構成を使用します。</span><span class="sxs-lookup"><span data-stu-id="9e7f7-143">To install the operating system, use the server deployment procedures and configurations established by your organization.</span></span> <span data-ttu-id="9e7f7-144">サービスを復元する場合は、以下の手順と構成要件を利用できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e7f7-144">You should have these procedures and configuration requirements available when you restore service.</span></span>

  - <span data-ttu-id="9e7f7-145">SQL Server 2012 または SQL Server 2008 R2 のインストールソフトウェア。</span><span class="sxs-lookup"><span data-stu-id="9e7f7-145">Installation software for SQL Server 2012 or SQL Server 2008 R2.</span></span> <span data-ttu-id="9e7f7-146">データベースサーバーをインストールするには、適切なバージョンの SQL Server と、組織によって確立されたデータベースサーバーの展開手順と構成を使用します。</span><span class="sxs-lookup"><span data-stu-id="9e7f7-146">To install a database server, use the appropriate version of SQL Server and the database server deployment procedures and configurations established by your organization.</span></span> <span data-ttu-id="9e7f7-147">サービスを復元する場合は、以下の手順と構成要件を利用できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e7f7-147">You should have these procedures and configuration requirements available when you restore service.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9e7f7-148">サーバーに SQL Server 2012 または SQL Server 2008 R2 がプレインストールされている場合を除き、Lync Server Deployment Wizard は、ローカル構成ストアがインストールされている場合に、各標準エディションサーバーおよび他の Lync Server サーバーに SQL Server 2012 Express を自動的にインストールします。</span><span class="sxs-lookup"><span data-stu-id="9e7f7-148">The Lync Server Deployment Wizard automatically installs SQL Server 2012 Express on each Standard Edition server and on any other Lync Server server when a local configuration store is installed, unless you have preinstalled SQL Server 2012 or SQL Server 2008 R2 on the server.</span></span>

    
    </div>

  - <span data-ttu-id="9e7f7-149">システムイメージを取得するためのソフトウェア。</span><span class="sxs-lookup"><span data-stu-id="9e7f7-149">Software for taking system images.</span></span>
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="9e7f7-150">オペレーティングシステムと SQL Server をインストールしてから復元を開始する前に、システムのイメージコピーを取得することをお勧めします。復元中に問題が発生した場合に、この画像をロールバックポイントとして使うことができます。</span><span class="sxs-lookup"><span data-stu-id="9e7f7-150">We recommend that you take an image copy of the system after you install the operating system and SQL Server, and before you start restoration, so that you can use this image as a rollback point in case something goes wrong during restoration.</span></span>

    
    </div>

  - <span data-ttu-id="9e7f7-151">Lync Server 2013 インストールソフトウェア。</span><span class="sxs-lookup"><span data-stu-id="9e7f7-151">Lync Server 2013 installation software.</span></span> <span data-ttu-id="9e7f7-152">Lync Server 展開ウィザードは、Lync Server のインストールフォルダーまたはセットアップ amd64Setup.exe のメディアにあり \\ \\ \\ ます。</span><span class="sxs-lookup"><span data-stu-id="9e7f7-152">The Lync Server Deployment Wizard is located in the Lync Server installation folder or media at \\setup\\amd64\\Setup.exe.</span></span>

<span data-ttu-id="9e7f7-153">復元中には、次のツールを使用します。</span><span class="sxs-lookup"><span data-stu-id="9e7f7-153">During restoration, you use the following tools:</span></span>

  - <span data-ttu-id="9e7f7-154">Lync Server 管理シェルコマンドレット</span><span class="sxs-lookup"><span data-stu-id="9e7f7-154">Lync Server Management Shell cmdlets</span></span>

  - <span data-ttu-id="9e7f7-155">Import-CsUserData</span><span class="sxs-lookup"><span data-stu-id="9e7f7-155">Import-CsUserData</span></span>

  - <span data-ttu-id="9e7f7-156">Windows フォルダーを復元するためのツール</span><span class="sxs-lookup"><span data-stu-id="9e7f7-156">Tools for restoring Windows folders</span></span>

  - <span data-ttu-id="9e7f7-157">トポロジ ビルダー</span><span class="sxs-lookup"><span data-stu-id="9e7f7-157">Topology Builder</span></span>

  - <span data-ttu-id="9e7f7-158">Sql server Management Studio などの SQL Server データベースユーティリティ</span><span class="sxs-lookup"><span data-stu-id="9e7f7-158">SQL Server database utilities, such as SQL Server Management Studio</span></span>

</div>

<div>

## <a name="preparing-to-restore-a-server"></a><span data-ttu-id="9e7f7-159">サーバーを復元するための準備</span><span class="sxs-lookup"><span data-stu-id="9e7f7-159">Preparing to Restore a Server</span></span>

<span data-ttu-id="9e7f7-160">サーバーを復元する前に、次の手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e7f7-160">Before you restore the server, you must perform the following steps:</span></span>

1.  <span data-ttu-id="9e7f7-161">オペレーティングシステムをインストールします。</span><span class="sxs-lookup"><span data-stu-id="9e7f7-161">Install the operating system.</span></span>

2.  <span data-ttu-id="9e7f7-162">サーバーがバックエンドサーバーの場合は、SQL Server 2012 または SQL Server 2008 R2 をインストールします。</span><span class="sxs-lookup"><span data-stu-id="9e7f7-162">If the server is a Back End Server, install SQL Server 2012 or SQL Server 2008 R2.</span></span>

3.  <span data-ttu-id="9e7f7-163">証明書を復元または reenroll します。</span><span class="sxs-lookup"><span data-stu-id="9e7f7-163">Restore or reenroll your certificates.</span></span> <span data-ttu-id="9e7f7-164">証明書の詳細については、「 [Lync Server 2013 のバックアップと復元の要件](lync-server-2013-backup-and-restoration-requirements-data.md)」の「その他のバックアップ要件」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9e7f7-164">For details about certificates, see "Additional Backup Requirements" in [Backup and restoration requirements in Lync Server 2013: data](lync-server-2013-backup-and-restoration-requirements-data.md).</span></span>

4.  <span data-ttu-id="9e7f7-165">復元中に問題が発生した場合に備えて、復元を開始する前に、システムのイメージを取得してロールバックポイントとして使用します。</span><span class="sxs-lookup"><span data-stu-id="9e7f7-165">Take an image of the system before starting restoration to use as a rollback point, in case something goes wrong during restoration.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="9e7f7-166">このトピックの手順および関連トピックで説明されている Lync Server 展開ウィザードとコマンドレットでは、必要なすべてのアクセス制御リスト (Acl) を設定します。</span><span class="sxs-lookup"><span data-stu-id="9e7f7-166">The Lync Server Deployment Wizard and cmdlets described in the procedures in this topic, and related topics, set all required access control lists (ACLs).</span></span>



</div>

<span data-ttu-id="9e7f7-167">復元を開始する前に、復元する予定のコンポーネントに必要なハードウェアとソフトウェアが使用可能であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9e7f7-167">Verify that the hardware and the software that you need for the components that you plan to restore are available before you start restoration.</span></span> <span data-ttu-id="9e7f7-168">オペレーティングシステムと SQL Server をインストールした後、次の復元手順のほとんどはリモートで実行できます。</span><span class="sxs-lookup"><span data-stu-id="9e7f7-168">After you install the operating system and SQL Server, most of the steps in the following restoration procedures can be run remotely.</span></span> <span data-ttu-id="9e7f7-169">例外については、手順に記載されています。</span><span class="sxs-lookup"><span data-stu-id="9e7f7-169">The exceptions are noted in the procedures.</span></span>

<span data-ttu-id="9e7f7-170">また、組織のバックアップと復元計画、およびこのドキュメントのワークシートの情報 (詳細については、「 [Lync Server 2013 のバックアップと復元用のワークシート](lync-server-2013-backup-and-restoration-worksheets.md)を参照してください)、復元を開始する前に確認しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e7f7-170">You should also have your organization's backup and restoration plan and the information from your last backup, such as the information in the worksheets in this document (for details, see [Backup and restoration worksheets for Lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md)), available before you begin restoration.</span></span>

<span data-ttu-id="9e7f7-171"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9e7f7-171"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

