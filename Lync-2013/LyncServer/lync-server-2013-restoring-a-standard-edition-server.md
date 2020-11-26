---
title: 'Lync Server 2013: Standard Edition サーバーの復元'
description: 'Lync Server 2013: Standard Edition サーバーを復元します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring a Standard Edition server
ms:assetid: d1845663-3138-4fd6-b3e7-337e294d40d8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202190(v=OCS.15)
ms:contentKeyID: 51541519
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1d2cd6976324492e0539c47999f78434e1a82706
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436224"
---
# <a name="restoring-a-standard-edition-server-in-lync-server-2013"></a><span data-ttu-id="d2f51-103">Lync Server 2013 での Standard Edition サーバーの復元</span><span class="sxs-lookup"><span data-stu-id="d2f51-103">Restoring a Standard Edition server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d2f51-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d2f51-104">

<span> </span></span></span>

<span data-ttu-id="d2f51-105">_**最終更新日:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="d2f51-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="d2f51-106">中央管理ストアをホストしていない Standard Edition サーバーで問題が発生した場合は、このセクションの手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="d2f51-106">If a Standard Edition server that does not host the Central Management store fails, follow the procedures in this section.</span></span> <span data-ttu-id="d2f51-107">サーバーの全体管理ストアでエラーが発生した場合は、「 [Lync server 2013 で中央管理ストアをホストしているサーバーの復元](lync-server-2013-restoring-the-server-hosting-the-central-management-store.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d2f51-107">If the Central Management store fails, see [Restoring the server hosting the Central Management store in Lync Server 2013](lync-server-2013-restoring-the-server-hosting-the-central-management-store.md).</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="d2f51-108">復元を開始する前に、システムのイメージコピーを取得することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d2f51-108">We recommend that you take an image copy of the system before you start restoration.</span></span> <span data-ttu-id="d2f51-109">復元中に問題が発生した場合に備えて、この画像をロールバックポイントとして使うことができます。</span><span class="sxs-lookup"><span data-stu-id="d2f51-109">You can use this image as a rollback point, in case something goes wrong during restoration.</span></span> <span data-ttu-id="d2f51-110">オペレーティングシステムと SQL Server をインストールした後に画像のコピーを取得し、証明書を復元または再登録することができます。</span><span class="sxs-lookup"><span data-stu-id="d2f51-110">You might want to take the image copy after you install the operating system and SQL Server, and restore or re-enroll the certificates.</span></span>



</div>

<div>

## <a name="to-restore-a-standard-edition-server"></a><span data-ttu-id="d2f51-111">Standard Edition サーバーを復元するには</span><span class="sxs-lookup"><span data-stu-id="d2f51-111">To restore a Standard Edition server</span></span>

1.  <span data-ttu-id="d2f51-112">障害のあるコンピューターと同じ完全修飾ドメイン名 (FQDN) を持つクリーンで、または新しいサーバーから始め、オペレーティングシステムをインストールして、証明書を復元または reenroll します。</span><span class="sxs-lookup"><span data-stu-id="d2f51-112">Start with a clean or new server that has the same fully qualified domain name (FQDN) as the failed computer, install the operating system, and then restore or reenroll the certificates.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="d2f51-113">組織のサーバー展開手順に従って、この手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="d2f51-113">Follow your organization's server deployment procedures to perform this step.</span></span>

    
    </div>

2.  <span data-ttu-id="d2f51-114">RTCUniversalServerAdmins グループとローカルの管理者グループのメンバーであるユーザーアカウントから、復元しているサーバーにログオンします。</span><span class="sxs-lookup"><span data-stu-id="d2f51-114">From a user account that is a member of the RTCUniversalServerAdmins group and the Local Administrators group, log on to the server that you are restoring.</span></span>

3.  <span data-ttu-id="d2f51-115">適切なファイルストアを $Backup からサーバー上のファイルストアの場所にコピーして、ファイルストアを復元し、フォルダーを共有します。</span><span class="sxs-lookup"><span data-stu-id="d2f51-115">Restore the File Store by copying the appropriate File Store from $Backup to the File Store location on the server and share the folder.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="d2f51-116">復元されたファイルストアのパスとファイル名は、ファイルを使用するコンポーネントがアクセスできるように、バックアップされたファイルストアとまったく同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2f51-116">The path and file name for the restored File Store should be exactly the same as the backed up File Store so that components that use the files can access them.</span></span>

    
    </div>

4.  <span data-ttu-id="d2f51-117">トポロジビルダーを実行します。</span><span class="sxs-lookup"><span data-stu-id="d2f51-117">Run Topology Builder:</span></span>
    
    1.  <span data-ttu-id="d2f51-118">トポロジビルダーを開始します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server Topology Builder**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="d2f51-118">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>
    
    2.  <span data-ttu-id="d2f51-119">[ **既存の展開からトポロジをダウンロード**] をクリックし、[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d2f51-119">Click **Download Topology from existing deployment**, and then click **OK**.</span></span>
    
    3.  <span data-ttu-id="d2f51-120">トポロジを選択し、[ **保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d2f51-120">Select the topology, and then click **Save**.</span></span> <span data-ttu-id="d2f51-121">選択内容を確認するには、[ **はい]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d2f51-121">Click **Yes** to confirm your selection.</span></span>

5.  <span data-ttu-id="d2f51-122">Lync Server のインストールフォルダーまたはメディアを参照して、setup amd64Setup.exe にある Lync Server 展開ウィザードを起動し \\ \\ \\ ます。</span><span class="sxs-lookup"><span data-stu-id="d2f51-122">Browse to the Lync Server installation folder or media, and then start the Lync Server Deployment Wizard located at \\setup\\amd64\\Setup.exe.</span></span> <span data-ttu-id="d2f51-123">Lync Server 展開ウィザードを使用して、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="d2f51-123">Use the Lync Server Deployment Wizard to do the following:</span></span>
    
    1.  <span data-ttu-id="d2f51-124">**手順 1: ローカル構成ストアをインストール** して、ローカル構成ファイルをインストールします。</span><span class="sxs-lookup"><span data-stu-id="d2f51-124">Run **Step 1: Install Local Configuration Store** to install the local configuration files.</span></span>
    
    2.  <span data-ttu-id="d2f51-125">**手順 2: lync server のコンポーネントをセットアップまたは削除** して lync server サーバーの役割をインストールする</span><span class="sxs-lookup"><span data-stu-id="d2f51-125">Run **Step 2: Setup or Remove Lync Server Components** to install the Lync Server server roles.</span></span>
    
    3.  <span data-ttu-id="d2f51-126">手順 3: 証明書を割り当てるために **証明書を要求、インストール、または割り当て** ます。</span><span class="sxs-lookup"><span data-stu-id="d2f51-126">Run **Step 3: Request, Install or Assign Certificates** to assign the certificates.</span></span>
    
    4.  <span data-ttu-id="d2f51-127">**手順 4: サービスを開始** して、サーバー上のサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="d2f51-127">Run **Step 4: Start Services** to start services on the server.</span></span>
    
    <span data-ttu-id="d2f51-128">展開ウィザードの実行の詳細については、復元するサーバーの役割の展開ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d2f51-128">For details about running the Deployment Wizard, see the Deployment documentation for the server role you are restoring.</span></span>

6.  <span data-ttu-id="d2f51-129">ユーザーデータを復元するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="d2f51-129">Restore user data by performing the following:</span></span>
    
    1.  <span data-ttu-id="d2f51-130">$Backup から \\ ローカルディレクトリに ExportedUserData.zip をコピーします。</span><span class="sxs-lookup"><span data-stu-id="d2f51-130">Copy ExportedUserData.zip from $Backup\\ to a local directory.</span></span>
    
    2.  <span data-ttu-id="d2f51-131">ユーザーデータを復元する前に、Lync サービスを停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2f51-131">Before you restore the user data, you must stop Lync services.</span></span> <span data-ttu-id="d2f51-132">そのためには、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="d2f51-132">To do so, type:</span></span>
        
            Stop-CsWindowsService
    
    3.  <span data-ttu-id="d2f51-133">ユーザーデータを復元するには、コマンドラインで次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="d2f51-133">To restore the user data, at the command line, type:</span></span>
        
            Import-CsUserData -PoolFqdn <Fqdn> -FileName <String>
        
        <span data-ttu-id="d2f51-134">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="d2f51-134">For example:</span></span>
        
            Import-CsUserData -PoolFqdn "atl0cs-001.litwareinc.com" -FileName "C:\Logs\ExportedUserDatal.zip"
    
    4.  <span data-ttu-id="d2f51-135">次のように入力して Lync サービスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="d2f51-135">Restart Lync services by typing:</span></span>
        
            Start-CsWindowsService

7.  <span data-ttu-id="d2f51-136">この Standard Edition サーバーで応答グループを展開した場合は、応答グループの構成データを復元します。</span><span class="sxs-lookup"><span data-stu-id="d2f51-136">If you deployed Response Group on this Standard Edition server, restore the Response Group configuration data.</span></span> <span data-ttu-id="d2f51-137">詳細については、「 [Lync Server 2013 での応答グループの設定の復元](lync-server-2013-restoring-response-group-settings.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d2f51-137">For details, see [Restoring Response Group settings in Lync Server 2013](lync-server-2013-restoring-response-group-settings.md).</span></span>

8.  <span data-ttu-id="d2f51-138">この Standard Edition サーバーに常設チャットを展開した場合は、常設チャットデータベース (行う) を復元します。</span><span class="sxs-lookup"><span data-stu-id="d2f51-138">If you deployed Persistent Chat on this Standard Edition server, restore the Persistent Chat database (mgc.mdf).</span></span>
    
    <span data-ttu-id="d2f51-139">SQL Server バックアップを使って常設チャットデータベースをバックアップした場合は、SQL Server の復元手順を使用して復元します。</span><span class="sxs-lookup"><span data-stu-id="d2f51-139">If you used SQL Server Backup to back up the Persistent Chat database, use SQL Server restore procedures to restore it.</span></span>
    
    <span data-ttu-id="d2f51-140">Export-CsPersistentChatData コマンドレットを使用してバックアップを作成した場合は、Import-CsPersistentChatData を使って復元します。</span><span class="sxs-lookup"><span data-stu-id="d2f51-140">If you used the Export-CsPersistentChatData cmdlet to back it up, use the Import-CsPersistentChatData to restore it.</span></span>

<span data-ttu-id="d2f51-141"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d2f51-141"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

