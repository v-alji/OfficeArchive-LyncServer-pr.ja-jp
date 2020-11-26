---
title: コール パーク アプリケーション設定の移行
description: コールパークアプリケーションの設定を移行します。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrate Call Park application settings
ms:assetid: 23b192d2-93ec-42a8-b175-b6ed502a2c35
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687993(v=OCS.15)
ms:contentKeyID: 49733583
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: da90ca4ee4dd53451c29b8c39861dc76a17ca3c7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446900"
---
# <a name="migrate-call-park-application-settings"></a><span data-ttu-id="ae76b-103">コール パーク アプリケーション設定の移行</span><span class="sxs-lookup"><span data-stu-id="ae76b-103">Migrate Call Park application settings</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="https://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ae76b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ae76b-104">

<span> </span></span></span>

<span data-ttu-id="ae76b-105">_**最終更新日:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="ae76b-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="ae76b-106">Lync Server 2010 から Lync Server 2013 へのコールパークアプリケーションの移行には、lync server 2013 プールのプロビジョニングが含まれています。このファイルには、Lync server 2010 にアップロードされたカスタム音楽が含まれています。また、lync server 2013 プールへのすべてのコールパーク orbits を retargeting することもできます。</span><span class="sxs-lookup"><span data-stu-id="ae76b-106">The migration of the Call Park application from Lync Server 2010 to Lync Server 2013 includes provisioning the Lync Server 2013 pool with any custom music on hold files that have been uploaded in Lync Server 2010, restoring the service level settings and retargeting all Call Park orbits to the Lync Server 2013 pool.</span></span> <span data-ttu-id="ae76b-107">カスタマイズした音楽の保留中のファイルが Lync Server 2010 プールで構成されている場合は、これらのファイルを新しい Lync Server 2013 プールにコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae76b-107">If customized music-on-hold files have been configured in the Lync Server 2010 pool, these files need to be copied to the new Lync Server 2013 pool.</span></span> <span data-ttu-id="ae76b-108">さらに、通話パークしたカスタマイズされた音楽の保留中のファイルを Lync Server 2010 から別の場所にバックアップすることをお勧めします。これは、コールパーク用にアップロードされたカスタマイズした音楽の保存ファイルの個別のバックアップコピーを保持するためです。</span><span class="sxs-lookup"><span data-stu-id="ae76b-108">Additionally, it is recommended that you back up any Call Park customized music-on-hold files from Lync Server 2010 to another destination to keep a separate backup copy of any customized music-on-hold files that have been uploaded for Call Park.</span></span> <span data-ttu-id="ae76b-109">コールパークアプリケーション用にカスタマイズされた音楽保留のファイルは、プールのファイルストアに保存されます。</span><span class="sxs-lookup"><span data-stu-id="ae76b-109">The customized music-on-hold files for the Call Park application are stored in the file store of the pool.</span></span> <span data-ttu-id="ae76b-110">Lync Server 2010 プールファイルストアから Lync Server 2013 ファイルストアにオーディオファイルをコピーするには、次のパラメーターを使用して **Xcopy** コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="ae76b-110">To copy the audio files from a Lync Server 2010 pool file store to a Lync Server 2013 file store, use the **Xcopy** command with the following parameters:</span></span>

   ```console
    Xcopy <Source: Lync Server 2010 Pool CPS File Store Path> <Destination: Lync Server 2013 Pool CPS File Store Path>
   ```

   ```console
    Example usage:  Xcopy "<Lync Server 2010 File Store Path>\OcsFileStore\coX-ApplicationServer-X\AppServerFiles\CPS\"  "<Lync Server 2013 File Store Path>\OcsFileStore\coX-ApplicationServer-X\AppServerFiles\CPS\" 
   ```

<span data-ttu-id="ae76b-111">カスタマイズされたすべてのオーディオファイルを Lync Server 2013 ファイルストアにコピーしたら、lync server 2013 プールのコールパークのアプリケーション設定を構成する必要があります。また、Lync Server 2010 プールに関連付けられている通話パーク範囲は、Lync Server 2013 プールに再割り当てする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae76b-111">When all customized audio files have been copied to the Lync Server 2013 file store, the Call Park application settings of the Lync Server 2013 pool must be configured, and the Call Park orbit ranges that are associated with the Lync Server 2010 pool must be reassigned to the Lync Server 2013 pool.</span></span>

<span data-ttu-id="ae76b-112">コールパークアプリケーションの設定には、ピックアップタイムアウトしきい値、保留中の音楽を有効または無効にする、最大通話ピックアップ試行回数、タイムアウト要求が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ae76b-112">The Call Park application settings include the pickup timeout threshold, enabling or disabling music on hold, the maximum call pickup attempts and the timeout request.</span></span> <span data-ttu-id="ae76b-113">**CsCpsConfiguration** コマンドレットを実行するには、Lync Server 管理シェルを使用して、コールパークアプリケーションの設定を管理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae76b-113">You must manage Call Park application settings by using the Lync Server Management Shell to run the **Set-CsCpsConfiguration** cmdlet.</span></span> <span data-ttu-id="ae76b-114">Lync Server コントロールパネルを使用して、[コールパーク] のアプリケーション設定を管理することはできません。</span><span class="sxs-lookup"><span data-stu-id="ae76b-114">You cannot manage the Call Park application settings using the Lync Server Control Panel.</span></span>

<span data-ttu-id="ae76b-115">**コールパークサービス設定を再構成する**</span><span class="sxs-lookup"><span data-stu-id="ae76b-115">**Reconfigure the Call Park Service Settings**</span></span>

1.  <span data-ttu-id="ae76b-116">Lync Server 2013 フロントエンドサーバーから、Lync Server 管理シェルを開きます。</span><span class="sxs-lookup"><span data-stu-id="ae76b-116">From the Lync Server 2013 Front End Server, open the Lync Server Management Shell.</span></span>

2.  <span data-ttu-id="ae76b-117">コマンドラインで、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="ae76b-117">At the command line, type the following:</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ae76b-118">Lync Server 2013 Call パークのアプリケーション設定が従来の Lync Server の2010設定と同じである場合は、この手順の実行をスキップできます。</span><span class="sxs-lookup"><span data-stu-id="ae76b-118">If your Lync Server 2013 Call Park application settings are identical to the legacy Lync Server 2010 settings, you can skip running this step.</span></span> <span data-ttu-id="ae76b-119">会議の設定が Lync Server 2013 および Lync Server 2010 環境で異なる場合は、次のコマンドレットをテンプレートとして使用して、それらの変更を更新します。</span><span class="sxs-lookup"><span data-stu-id="ae76b-119">If Call Park application settings are different for the Lync Server 2013 and Lync Server 2010 environments, use the cmdlet below as a template to update those changes.</span></span>

    
    <span data-ttu-id="ae76b-120"></div>
    ```powershell
        Set-CsCpsConfiguration -Identity "<LS2013 Call Park Service ID>"-Callpup Uptimeoutthreshold" "- <LS2010 CPS TimeSpan> enablemusiconhold" "- <LS2010 CPS value> maxcallピック upattempts" <LS2010 CPS pickup attempts> "-ontimeouturi" <LS2010 CPS timeout URI> " ```</span><span class="sxs-lookup"><span data-stu-id="ae76b-120"></div>
    ```powershell
        Set-CsCpsConfiguration -Identity "<LS2013 Call Park Service ID>" -CallPickupTimeoutThreshold "<LS2010 CPS TimeSpan>" -EnableMusicOnHold "<LS2010 CPS value>" -MaxCallPickupAttempts "<LS2010 CPS pickup attempts>" -OnTimeoutURI "<LS2010 CPS timeout URI>" ```</span></span>

<span data-ttu-id="ae76b-121">すべてのコールパークの範囲を Lync server 2010 プールから Lync Server 2013 プールに再割り当てするには、Lync Server コントロールパネルまたは Lync server 管理シェルを使用できます。</span><span class="sxs-lookup"><span data-stu-id="ae76b-121">To reassign all Call Park orbit ranges from Lync Server 2010 pool to the Lync Server 2013 pool, you can use either the Lync Server Control Panel or the Lync Server Management Shell.</span></span>

<span data-ttu-id="ae76b-122">**Lync Server コントロールパネルを使用してすべてのコールパークの範囲を再割り当てする**</span><span class="sxs-lookup"><span data-stu-id="ae76b-122">**Reassign all Call Park Orbit Ranges using Lync Server Control Panel**</span></span>

1.  <span data-ttu-id="ae76b-123">[Lync Server コントロール パネル] を開きます。</span><span class="sxs-lookup"><span data-stu-id="ae76b-123">Open Lync Server Control Panel.</span></span>

2.  <span data-ttu-id="ae76b-124">左側のウィンドウで、[ **音声機能**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="ae76b-124">In the left pane, select **Voice Features**.</span></span>

3.  <span data-ttu-id="ae76b-125">[ **Call パーク** ] タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="ae76b-125">Select the **Call Park** tab.</span></span>

4.  <span data-ttu-id="ae76b-126">Lync Server 2010 プールに割り当てられている各通話パークの範囲は、[ **宛先サーバーの FQDN** ] の設定を編集し、コールパーク要求を処理する lync server 2013 プールを選択します。</span><span class="sxs-lookup"><span data-stu-id="ae76b-126">For each Call Park orbit range assigned to a Lync Server 2010 pool, edit the **FQDN of destination server** setting and select the Lync Server 2013 pool that will process the Call Park requests.</span></span>

5.  <span data-ttu-id="ae76b-127">[ **コミット** ] を選んで変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="ae76b-127">Select **Commit** to save the changes.</span></span>

<span data-ttu-id="ae76b-128">**Lync Server 管理シェルを使用してすべてのコールパーク範囲を再割り当てする**</span><span class="sxs-lookup"><span data-stu-id="ae76b-128">**Reassign all Call Park Orbit Ranges using Lync Server Management Shell**</span></span>

1.  <span data-ttu-id="ae76b-129">Lync Server 管理シェルを開きます。</span><span class="sxs-lookup"><span data-stu-id="ae76b-129">Open Lync Server Management Shell.</span></span>

2.  <span data-ttu-id="ae76b-130">コマンドラインで、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="ae76b-130">At the command line, type the following:</span></span>
    ```powershell
    Get-CsCallParkOrbit
    ```
    
    <span data-ttu-id="ae76b-131">このコマンドレットは、展開内のすべてのコールパーク範囲の範囲を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="ae76b-131">This cmdlet lists all of the Call Park orbit ranges in the deployment.</span></span> <span data-ttu-id="ae76b-132">Lync Server 2010 プールとして **CallParkServiceId** と **Callparkserverfqdn** パラメーターが設定されているすべての Call パーク orbits は、再割り当てする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae76b-132">All Call Park orbits that have the **CallParkServiceId** and **CallParkServerFqdn** parameters set as the Lync Server 2010 pool must be reassigned.</span></span>
    
    <span data-ttu-id="ae76b-133">Lync Server 2010 Call パークの範囲を Lync Server 2013 プールに再割り当てするには、コマンドラインで次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="ae76b-133">To reassign the Lync Server 2010 Call Park orbit ranges to the Lync Server 2013 pool, at the command line, type the following:</span></span>
    
    ```powershell
    Set-CsCallParkOrbit -Identity "<Call Park Orbit Identity>" -CallParkService "service:ApplicationServer:<Lync Server 2013 Pool FQDN>"
    ```

<span data-ttu-id="ae76b-134">すべてのコールパークの範囲を Lync Server 2013 プールに再割り当てすると、コールパークアプリケーションの移行プロセスが完了し、Lync Server 2013 プールは、今後のすべてのコールパーク要求を処理します。</span><span class="sxs-lookup"><span data-stu-id="ae76b-134">After reassigning all Call Park orbit ranges to the Lync Server 2013 pool, the migration process for the Call Park application will be completed and the Lync Server 2013 pool will handle all future Call Park requests.</span></span>

<span data-ttu-id="ae76b-135"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ae76b-135"></div>

<span> </span>

</div>

</div>

</span></span></div>

