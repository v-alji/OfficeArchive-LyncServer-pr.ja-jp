---
title: 'Lync Server 2013: 中央管理ストアをホストしているサーバーの復元'
description: 'Lync Server 2013: 中央管理ストアをホストしているサーバーを復元します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring the server hosting the Central Management store
ms:assetid: 3bd6c82c-07fb-4798-b8f9-e7c78a5a83d5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202172(v=OCS.15)
ms:contentKeyID: 51541464
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c0c07e4c6722695b2bfb4cb478a1f3eefa86b4eb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442517"
---
# <a name="restoring-the-server-hosting-the-central-management-store-in-lync-server-2013"></a><span data-ttu-id="876e3-103">Lync Server 2013 での中央管理ストアをホストしているサーバーの復元</span><span class="sxs-lookup"><span data-stu-id="876e3-103">Restoring the server hosting the Central Management store in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="876e3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="876e3-104">

<span> </span></span></span>

<span data-ttu-id="876e3-105">_**最終更新日:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="876e3-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="876e3-106">Lync Server の展開には、1つの一元管理ストアがあります。これらのコピーは、Lync Server server の役割を実行している各サーバーにレプリケートされます。</span><span class="sxs-lookup"><span data-stu-id="876e3-106">A Lync Server deployment has a single Central Management store, a copy of which is replicated to each server running a Lync Server server role.</span></span> <span data-ttu-id="876e3-107">このトピックでは、中央管理ストアをホストするバックエンドサーバーまたは Standard Edition サーバーを復元する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="876e3-107">This topic describes how to restore a Back End Server or Standard Edition server that hosts the Central Management store.</span></span>

<span data-ttu-id="876e3-108">中央管理サーバーが配置されているプールを見つけるには、トポロジビルダーを開き、[ **Lync Server**] をクリックして、右側のウィンドウの [サーバーの **全体管理**] を確認します。</span><span class="sxs-lookup"><span data-stu-id="876e3-108">To find the pool where the Central Management Server is located, open Topology Builder, click **Lync Server**, and look in the right pane under **Central Management Server**.</span></span>

<span data-ttu-id="876e3-109">中央管理ストアをホストしているバックエンドサーバーがミラーリングされたセットアップであり、ミラーデータベースがまだ機能している場合は、次の復元手順に従って、このバックアップを使用して、プライマリデータベースとミラーデータベースの両方に対して完全な復元を実行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="876e3-109">If the Back End Server that hosts the Central Management store is in a mirrored setup and the mirror database is still functional, we recommend that you make a backup of this still-functioning mirror, and then perform a full restore on both the primary database and the mirror database, using this backup, by following the restoration procedure below.</span></span> <span data-ttu-id="876e3-110">バックエンドの復元ではトポロジを変更して発行する必要があります。これは、CMS をホストしているプライマリデータベースが動作している場合にのみ実行できます。</span><span class="sxs-lookup"><span data-stu-id="876e3-110">This is necessary because Back End restore requires modifying and publishing the topology, and this can be done only if the primary database hosting CMS is operational.</span></span> <span data-ttu-id="876e3-111">また、トポロジを公開できない場合は、プライマリデータベースロールとミラーデータベースロールを交換できないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="876e3-111">Also note that the primary and mirror database roles cannot be interchanged if the topology cannot be published.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="876e3-112">中央管理ストアをホストしていないバックエンドサーバーまたは Standard Edition サーバーで障害が発生した場合は、「 <A href="lync-server-2013-restoring-an-enterprise-edition-back-end-server.md">Lync server 2013 で Enterprise Edition バックエンドサーバーを復元する</A> 」または「 <A href="lync-server-2013-restoring-a-standard-edition-server.md">lync Server 2013 で standard Edition サーバーを復元</A>する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="876e3-112">If a Back End Server or Standard Edition server that does not host the Central Management store failed, see <A href="lync-server-2013-restoring-an-enterprise-edition-back-end-server.md">Restoring an Enterprise Edition Back End Server in Lync Server 2013</A> or <A href="lync-server-2013-restoring-a-standard-edition-server.md">Restoring a Standard Edition server in Lync Server 2013</A>.</span></span> <span data-ttu-id="876e3-113">中央管理ストアをホストするバックエンドサーバーがミラーリングされた構成であり、ミラーに失敗した場合にのみ、「 <A href="lync-server-2013-restoring-a-mirrored-enterprise-edition-back-end-server-mirror.md">Lync Server 2013-mirror でのミラーリングされた Enterprise Edition バックエンドサーバーの復元</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="876e3-113">If a Back End Server that hosts the Central Management store is in a mirrored configuration and only the mirror failed, see <A href="lync-server-2013-restoring-a-mirrored-enterprise-edition-back-end-server-mirror.md">Restoring a mirrored Enterprise Edition Back End Server in Lync Server 2013 - mirror</A>.</span></span> <span data-ttu-id="876e3-114">他のサーバーにエラーが発生した場合は、「 <A href="lync-server-2013-restoring-an-enterprise-edition-member-server.md">Lync server 2013 で Enterprise Edition のメンバーサーバーを復元する</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="876e3-114">If any other server failed, see <A href="lync-server-2013-restoring-an-enterprise-edition-member-server.md">Restoring an Enterprise Edition member server in Lync Server 2013</A>.</span></span>



</div>

<div>


> [!TIP]  
> <span data-ttu-id="876e3-115">復元を開始する前に、システムのイメージコピーを取得することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="876e3-115">We recommend that you take an image copy of the system before you start restoration.</span></span> <span data-ttu-id="876e3-116">復元中に問題が発生した場合に備えて、この画像をロールバックポイントとして使うことができます。</span><span class="sxs-lookup"><span data-stu-id="876e3-116">You can use this image as a rollback point, in case something goes wrong during restoration.</span></span> <span data-ttu-id="876e3-117">オペレーティングシステムと SQL Server をインストールした後に画像のコピーを取得し、証明書を復元または reenroll することができます。</span><span class="sxs-lookup"><span data-stu-id="876e3-117">You might want to take the image copy after you install the operating system and SQL Server, and restore or reenroll the certificates.</span></span>



</div>

<div>

## <a name="to-restore-the-central-management-store"></a><span data-ttu-id="876e3-118">中央管理ストアを復元するには</span><span class="sxs-lookup"><span data-stu-id="876e3-118">To restore the Central Management store</span></span>

1.  <span data-ttu-id="876e3-119">障害のあるコンピューターと同じ完全修飾ドメイン名 (FQDN) を持つクリーンで、または新しいサーバーから始め、オペレーティングシステムをインストールして、証明書を復元または reenroll します。</span><span class="sxs-lookup"><span data-stu-id="876e3-119">Start with a clean or new server that has the same fully qualified domain name (FQDN) as the failed computer, install the operating system, and then restore or reenroll the certificates.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="876e3-120">組織のサーバー展開手順に従って、この手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="876e3-120">Follow your organization's server deployment procedures to perform this step.</span></span>

    
    </div>

2.  <span data-ttu-id="876e3-121">RTCUniversalServerAdmins グループとローカルの管理者グループのメンバーであるユーザーアカウントから、復元しているサーバーにログオンします。</span><span class="sxs-lookup"><span data-stu-id="876e3-121">From a user account that is a member of the RTCUniversalServerAdmins group and the Local Administrators group, log on to the server that you are restoring.</span></span>

3.  <span data-ttu-id="876e3-122">Standard Edition サーバーを復元する場合は、適切なファイルストアを $Backup からサーバー上のファイルストアの場所にコピーして、ファイルストアを復元し、そのフォルダーを共有します。</span><span class="sxs-lookup"><span data-stu-id="876e3-122">If you are restoring a Standard Edition server, restore the File Store by copying the appropriate File Store from $Backup to the File Store location on the server, and then share the folder.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="876e3-123">復元されたファイルストアのパスとファイル名は、ファイルを使用するコンポーネントがアクセスできるように、バックアップされたファイルストアとまったく同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="876e3-123">The path and file name for the restored File Store should be exactly the same as the backed up File Store so that components that use the files can access them.</span></span>

    
    </div>

4.  <span data-ttu-id="876e3-124">次のいずれかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="876e3-124">Do one of the following:</span></span>
    
      - <span data-ttu-id="876e3-125">Standard Edition サーバーをインストールする場合は、Lync Server のインストールフォルダーまたはメディアを参照して、setup amd64Setup.exe にある Lync Server 展開ウィザードを起動し \\ \\ \\ ます。</span><span class="sxs-lookup"><span data-stu-id="876e3-125">If you are installing a Standard Edition server, browse to the Lync Server installation folder or media, and then start the Lync Server Deployment Wizard located at \\setup\\amd64\\Setup.exe.</span></span> <span data-ttu-id="876e3-126">展開ウィザードで、[ **最初の Standard Edition サーバーの準備** ] をクリックし、ウィザードに従って中央管理ストアをインストールします。</span><span class="sxs-lookup"><span data-stu-id="876e3-126">In the Deployment Wizard, click **Prepare first Standard Edition server** and follow the wizard to install the Central Management store.</span></span>
    
      - <span data-ttu-id="876e3-127">エンタープライズバックエンドサーバーをインストールする場合は、SQL Server 2012 または SQL Server 2008 R2 をインストールして、インスタンス名がエラーの前と同じになるようにします。</span><span class="sxs-lookup"><span data-stu-id="876e3-127">If you are installing an Enterprise Back End Server, install SQL Server 2012 or SQL Server 2008 R2, keeping the instance names the same as before the failure.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="876e3-128">復元しているサーバーによって、展開時にサーバーに複数の併置されたデータベースや個別のデータベースが含まれている場合があります。</span><span class="sxs-lookup"><span data-stu-id="876e3-128">Depending on the server that you are restoring and on your deployment, the server might include multiple collocated or separate databases.</span></span> <span data-ttu-id="876e3-129">SQL Server の権限とログインなど、サーバーの展開に最初に使用した SQL Server をインストールするには、同じ手順に従います。</span><span class="sxs-lookup"><span data-stu-id="876e3-129">Follow the same procedure to install SQL Server that you used originally to deploy the server, including SQL Server permissions and logins.</span></span>

        
        </div>

5.  <span data-ttu-id="876e3-130">フロントエンドサーバーから、Lync Server 管理シェルを起動します。 [ **スタート**]、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="876e3-130">From a Front End Server, Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

6.  <span data-ttu-id="876e3-131">中央管理ストアを再作成します。</span><span class="sxs-lookup"><span data-stu-id="876e3-131">Re-create the Central Management store.</span></span> <span data-ttu-id="876e3-132">コマンドラインで、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="876e3-132">At the command line, type:</span></span>
    
        Install-CsDatabase -CentralManagementDatabase -Clean -SqlServerFqdn <FQDN> -SqlInstanceName <instance name> -Verbose
    
    <span data-ttu-id="876e3-133">例:</span><span class="sxs-lookup"><span data-stu-id="876e3-133">For example:</span></span>
    
        Install-CsDatabase -CentralManagementDatabase -Clean -SqlServerFqdn Server01.contoso.com -SqlInstanceName cms -Verbose

7.  <span data-ttu-id="876e3-134">中央管理ストアの Active Directory ドメインサービスの制御点を設定します。</span><span class="sxs-lookup"><span data-stu-id="876e3-134">Set the Active Directory Domain Services control point for the Central Management store.</span></span> <span data-ttu-id="876e3-135">コマンドラインで、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="876e3-135">At the command line, type:</span></span>
    
        Set-CsConfigurationStoreLocation -SqlServerFqdn <FQDN> -SqlInstanceName <instance name> -Verbose
    
    <span data-ttu-id="876e3-136">例:</span><span class="sxs-lookup"><span data-stu-id="876e3-136">For example:</span></span>
    
        Set-CsConfigurationStoreLocation -SqlServerFqdn Server01.contoso.com -SqlInstanceName cms -Verbose
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="876e3-137">接続ポイントを失った場合は、このコマンドレットを再実行できます。</span><span class="sxs-lookup"><span data-stu-id="876e3-137">If you lose the connection point, you can rerun this cmdlet.</span></span>

    
    </div>

8.  <span data-ttu-id="876e3-138">$Backup から中央管理ストアのデータをインポートします。</span><span class="sxs-lookup"><span data-stu-id="876e3-138">Import the Central Management store data from $Backup.</span></span> <span data-ttu-id="876e3-139">コマンドラインで、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="876e3-139">At the command line, type:</span></span>
    
        Import-CsConfiguration -FileName <CMS backup file name>
    
    <span data-ttu-id="876e3-140">例:</span><span class="sxs-lookup"><span data-stu-id="876e3-140">For example:</span></span>
    
        Import-CsConfiguration -FileName "C:\Config.zip"

9.  <span data-ttu-id="876e3-141">直前に行った変更を有効にします。</span><span class="sxs-lookup"><span data-stu-id="876e3-141">Enable the changes you have just made.</span></span> <span data-ttu-id="876e3-142">コマンド ラインで次を入力します。</span><span class="sxs-lookup"><span data-stu-id="876e3-142">At the command line, type:</span></span>
    
        Enable-CsTopology
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="876e3-143">トポロジを有効にすると、データベース内でトポロジドキュメントを見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="876e3-143">After you enable the topology, you can find the topology document in the database.</span></span>

    
    </div>

10. <span data-ttu-id="876e3-144">CMS をホストしている Enterprise Edition バックエンドサーバーを復元している場合、または CMS のミラーを再作成する必要がある場合は、この手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="876e3-144">If you are restoring an Enterprise Edition Back End Server that also hosted the CMS, or if you need to re-create a mirror of the CMS, then follow this step.</span></span> <span data-ttu-id="876e3-145">それ以外の場合は、手順11に進んでください。</span><span class="sxs-lookup"><span data-stu-id="876e3-145">Otherwise, skip to step 11.</span></span>
    
    <span data-ttu-id="876e3-146">次の手順に従って、スタンドアロンデータベースをインストールします。</span><span class="sxs-lookup"><span data-stu-id="876e3-146">Install the stand-alone databases by doing the following:</span></span>
    
    1.  <span data-ttu-id="876e3-147">トポロジビルダーを開始します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server Topology Builder**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="876e3-147">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>
    
    2.  <span data-ttu-id="876e3-148">[ **既存の展開からトポロジをダウンロード**] をクリックし、[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="876e3-148">Click **Download Topology from existing deployment**, and then click **OK**.</span></span>
    
    3.  <span data-ttu-id="876e3-149">トポロジを選択し、[ **保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="876e3-149">Select the topology, and then click **Save**.</span></span> <span data-ttu-id="876e3-150">選択内容を確認するには、[ **はい]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="876e3-150">Click **Yes** to confirm your selection.</span></span>
    
    4.  <span data-ttu-id="876e3-151">[ **Lync Server 2013** ] ノードを右クリックし、[ **データベースのインストール**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="876e3-151">Right-click the **Lync Server 2013** node, and then click **Install Database**.</span></span>
    
    5.  <span data-ttu-id="876e3-152">データベースの **インストール** ウィザードを実行します。</span><span class="sxs-lookup"><span data-stu-id="876e3-152">Follow the **Install Database** wizard.</span></span> <span data-ttu-id="876e3-153">このサーバーの中央管理ストア以外のデータベースを復元する場合は、[データベースの **作成** ] ページで、再作成するデータベースを選びます。</span><span class="sxs-lookup"><span data-stu-id="876e3-153">If you are restoring a database other than the Central Management store on this server, on the **Create databases** page, select the databases you want to recreate.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="876e3-154"><STRONG>データベースの作成</STRONG>ページには、スタンドアロンデータベースのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="876e3-154">Only stand-alone databases are displayed on the <STRONG>Create databases</STRONG> page.</span></span> <span data-ttu-id="876e3-155">併置されたデータベースは、Lync Server 展開ウィザードを実行したときに作成されます。</span><span class="sxs-lookup"><span data-stu-id="876e3-155">Collocated databases are created when you run the Lync Server Deployment Wizard.</span></span>

        
        </div>
    
    6.  <span data-ttu-id="876e3-156">ミラーバックエンドサーバーを復元する場合は、「ミラーデータベースの作成」のプロンプトが表示されるまで、ウィザードの残りの指示に従って操作を続けます。</span><span class="sxs-lookup"><span data-stu-id="876e3-156">If you are restoring a mirrored Back End Server, continue to follow the rest of the wizard until you come to a prompt of Create Mirror Database.</span></span> <span data-ttu-id="876e3-157">インストールするデータベースを選択し、プロセスを完了します。</span><span class="sxs-lookup"><span data-stu-id="876e3-157">Select the database you want to install, and complete the process.</span></span>
    
    7.  <span data-ttu-id="876e3-158">ウィザードの残りの手順に従って、[ **完了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="876e3-158">Follow the rest of the wizard, and then click **Finish**.</span></span>
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="876e3-159">トポロジビルダーを実行する代わりに、 <STRONG>CsMirrorDatabase</STRONG>コマンド<STRONG>レットを</STRONG>使用して各データベースを作成し、このコマンドレットを使ってミラーリングを構成することができます。</span><span class="sxs-lookup"><span data-stu-id="876e3-159">Instead of running Topology Builder, you can use the <STRONG>Install-CsDatabase</STRONG> cmdlet to create each database, and the <STRONG>Install-CsMirrorDatabase</STRONG> cmdlet to configure mirroring.</span></span> <span data-ttu-id="876e3-160">詳細については、「 <A href="https://docs.microsoft.com/powershell/module/skype/Install-CsDatabase">CsDatabase</A> と <A href="https://docs.microsoft.com/powershell/module/skype/Install-CsMirrorDatabase">CsMirrorDatabase</A>をインストールする」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="876e3-160">For details, see <A href="https://docs.microsoft.com/powershell/module/skype/Install-CsDatabase">Install-CsDatabase</A> and <A href="https://docs.microsoft.com/powershell/module/skype/Install-CsMirrorDatabase">Install-CsMirrorDatabase</A>.</span></span>

    
    </div>

11. <span data-ttu-id="876e3-161">Standard Edition サーバーを復元する場合は、Lync Server のインストールフォルダーまたはメディアを参照して、セットアップ amd64Setup.exe にある Lync Server 展開ウィザードを開始し \\ \\ \\ ます。</span><span class="sxs-lookup"><span data-stu-id="876e3-161">If you are restoring a Standard Edition server, browse to the Lync Server installation folder or media, and start the Lync Server Deployment Wizard located at \\setup\\amd64\\Setup.exe.</span></span> <span data-ttu-id="876e3-162">Lync Server 展開ウィザードを使用して、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="876e3-162">Use the Lync Server Deployment Wizard to do the following:</span></span>
    
    1.  <span data-ttu-id="876e3-163">**手順 1: ローカル構成ストアをインストール** して、ローカル構成ファイルをインストールします。</span><span class="sxs-lookup"><span data-stu-id="876e3-163">Run **Step 1: Install Local Configuration Store** to install the local configuration files.</span></span>
    
    2.  <span data-ttu-id="876e3-164">**手順 2: lync server のコンポーネントをセットアップまたは削除** して lync server サーバーの役割をインストールする</span><span class="sxs-lookup"><span data-stu-id="876e3-164">Run **Step 2: Setup or Remove Lync Server Components** to install the Lync Server server roles.</span></span>
    
    3.  <span data-ttu-id="876e3-165">手順 3: 証明書を割り当てるために **証明書を要求、インストール、または割り当て** ます。</span><span class="sxs-lookup"><span data-stu-id="876e3-165">Run **Step 3: Request, Install or Assign Certificates** to assign the certificates.</span></span>
    
    4.  <span data-ttu-id="876e3-166">**手順 4: サービスを開始** して、サーバー上のサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="876e3-166">Run **Step 4: Start Services** to start services on the server.</span></span>
    
    <span data-ttu-id="876e3-167">展開ウィザードの実行の詳細については、復元するサーバーの役割の展開ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="876e3-167">For details about running the Deployment Wizard, see the Deployment documentation for the server role that you are restoring.</span></span>

12. <span data-ttu-id="876e3-168">ユーザーデータを復元するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="876e3-168">Restore user data by performing the following:</span></span>
    
    1.  <span data-ttu-id="876e3-169">$Backup から \\ ローカルディレクトリに ExportedUserData.zip をコピーします。</span><span class="sxs-lookup"><span data-stu-id="876e3-169">Copy ExportedUserData.zip from $Backup\\ to a local directory.</span></span>
    
    2.  <span data-ttu-id="876e3-170">ユーザーデータを復元する前に、Lync サービスを停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="876e3-170">Before you restore the user data, you must stop Lync services.</span></span> <span data-ttu-id="876e3-171">そのためには、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="876e3-171">To do so, type:</span></span>
        
            Stop-CsWindowsService
    
    3.  <span data-ttu-id="876e3-172">ユーザーデータを復元するには、コマンドラインで次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="876e3-172">To restore the user data, at the command line, type:</span></span>
        
            Import-CsUserData -PoolFqdn <Fqdn> -FileName <String>
        
        <span data-ttu-id="876e3-173">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="876e3-173">For example:</span></span>
        
            Import-CsUserData -PoolFqdn "atl0cs-001.litwareinc.com" -FileName "C:\Logs\ExportedUserDatal.zip"
    
    4.  <span data-ttu-id="876e3-174">次のように入力して Lync サービスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="876e3-174">Restart Lync services by typing:</span></span>
        
            Start-CsWindowsService

13. <span data-ttu-id="876e3-175">位置情報データを中央管理ストアに復元します。</span><span class="sxs-lookup"><span data-stu-id="876e3-175">Restore Location Information data to the Central Management store.</span></span> <span data-ttu-id="876e3-176">コマンドラインで、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="876e3-176">At the command line, type:</span></span>
    
        Import-CsLisConfiguration -FileName <LIS backup file name>
    
    <span data-ttu-id="876e3-177">例:</span><span class="sxs-lookup"><span data-stu-id="876e3-177">For example:</span></span>
    
        Import-CsLisConfiguration -FileName "D:\E911Config.zip"

14. <span data-ttu-id="876e3-178">このプールまたは Standard Edition サーバーに応答グループを展開した場合は、応答グループの構成データを復元します。</span><span class="sxs-lookup"><span data-stu-id="876e3-178">If you deployed Response Group on this pool or Standard Edition server, restore the Response Group configuration data.</span></span> <span data-ttu-id="876e3-179">詳細については、「 [Lync Server 2013 での応答グループの設定の復元](lync-server-2013-restoring-response-group-settings.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="876e3-179">For details, see [Restoring Response Group settings in Lync Server 2013](lync-server-2013-restoring-response-group-settings.md).</span></span>

15. <span data-ttu-id="876e3-180">アーカイブデータベースや監視データベースを含むバックエンドサーバーを復元する場合は、sql Server Management Studio などの SQL Server 管理ツールを使用して、アーカイブまたは監視データを復元します。</span><span class="sxs-lookup"><span data-stu-id="876e3-180">If you are restoring a Back End Server that includes Archiving or Monitoring databases, restore the Archiving or Monitoring data by using a SQL Server management tool, such as SQL Server Management Studio.</span></span> <span data-ttu-id="876e3-181">詳細について [は、「Lync Server 2013 で監視またはアーカイブデータを復元](lync-server-2013-restoring-monitoring-or-archiving-data.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="876e3-181">For details, see [Restoring monitoring or archiving data in Lync Server 2013](lync-server-2013-restoring-monitoring-or-archiving-data.md).</span></span>

<span data-ttu-id="876e3-182"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="876e3-182"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

