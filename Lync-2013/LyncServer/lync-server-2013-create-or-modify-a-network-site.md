---
title: 'Lync Server 2013: ネットワーク サイトの作成または変更'
description: 'Lync Server 2013: ネットワークサイトを作成または変更します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a network site
ms:assetid: 14e24856-9996-4da4-9f31-300940bdf5aa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398218(v=OCS.15)
ms:contentKeyID: 48183488
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c4db9080f866becfcb94972787e099a69eac28c9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431793"
---
# <a name="create-or-modify-a-network-site-in-lync-server-2013"></a><span data-ttu-id="15805-103">Lync Server 2013 でのネットワーク サイトの作成または変更</span><span class="sxs-lookup"><span data-stu-id="15805-103">Create or modify a network site in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="15805-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="15805-104">

<span> </span></span></span>

<span data-ttu-id="15805-105">_**最終更新日:** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="15805-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<span data-ttu-id="15805-106">通話受付制御 (CAC)、E9、および media バイパスの展開は、ネットワークの領域に定義され、常に関連付けられている *ネットワークサイト* の構成に依存します。</span><span class="sxs-lookup"><span data-stu-id="15805-106">Call admission control (CAC), E9-1-1, and media bypass deployments rely on the configuration of *network sites* which are defined within and always associated with a network region.</span></span> <span data-ttu-id="15805-107">ネットワークサイトは、支社の場所、建物のセット、またはキャンパスを表します。</span><span class="sxs-lookup"><span data-stu-id="15805-107">A network site represents a branch office location, a set of buildings, or a campus.</span></span> <span data-ttu-id="15805-108">ネットワークサイトは、同様の帯域幅のサブネットのコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="15805-108">Network sites represent collections of subnets with similar bandwidth.</span></span>

<span data-ttu-id="15805-109">ネットワークサイトを作成または変更するには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="15805-109">Use the following procedures to create or modify network sites.</span></span> <span data-ttu-id="15805-110">たとえば、1つの音声機能のネットワークサイトを既に作成している場合、新しいネットワークサイトを作成する必要はありません。その他の音声機能でも同じサイトが使用されます。</span><span class="sxs-lookup"><span data-stu-id="15805-110">For example, if you have already created network sites for one Voice feature, you do not need to create new network sites; other Voice features will use those same sites.</span></span> <span data-ttu-id="15805-111">ただし、機能固有の設定を適用するには、既存のネットワークサイト定義を変更する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="15805-111">You may, however, need to modify an existing network site definition to apply feature-specific settings.</span></span> <span data-ttu-id="15805-112">たとえば、E9 のネットワークサイトを作成した場合、通話受付制御の展開中にネットワークサイトを変更して、帯域幅ポリシープロファイルを適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="15805-112">For example, if you created a network site for E9-1-1, you need to modify the network site during deployment of call admission control to apply a bandwidth policy profile.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="15805-113">これらが存在する場合は、各機能の展開ドキュメントの高度な音声機能に関連するネットワークサイトの具体的な例と要件を見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="15805-113">Where they exist, you can find specific examples and requirements for network sites as they pertain to an advanced Voice feature in the Deployment documentation for each feature:</span></span> 
> <UL>
> <LI>
> <P><span data-ttu-id="15805-114"><A href="lync-server-2013-configure-network-sites-for-cac.md">Lync Server 2013 での CAC 用のネットワークサイトの構成</A></span><span class="sxs-lookup"><span data-stu-id="15805-114"><A href="lync-server-2013-configure-network-sites-for-cac.md">Configure network sites for CAC in Lync Server 2013</A></span></span></P></LI></UL>



</div>

<span data-ttu-id="15805-115">ネットワークサイトの操作の詳細については、次のコマンドレットの Lync Server 管理シェルに関するドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="15805-115">For details about working with network sites, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - [<span data-ttu-id="15805-116">新しい-CsNetworkSite</span><span class="sxs-lookup"><span data-stu-id="15805-116">New-CsNetworkSite</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSite)

  - [<span data-ttu-id="15805-117">Get-CsNetworkSite</span><span class="sxs-lookup"><span data-stu-id="15805-117">Get-CsNetworkSite</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkSite)

  - [<span data-ttu-id="15805-118">Set-CsNetworkSite</span><span class="sxs-lookup"><span data-stu-id="15805-118">Set-CsNetworkSite</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkSite)

  - [<span data-ttu-id="15805-119">CsNetworkSite の削除</span><span class="sxs-lookup"><span data-stu-id="15805-119">Remove-CsNetworkSite</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkSite)

<div>

## <a name="create-a-network-site"></a><span data-ttu-id="15805-120">ネットワークサイトを作成する</span><span class="sxs-lookup"><span data-stu-id="15805-120">Create a Network Site</span></span>

<span data-ttu-id="15805-121">通話受付制御、E9、またはメディアバイパスで使用できるネットワーク領域を作成します。</span><span class="sxs-lookup"><span data-stu-id="15805-121">Create a network region that can be used by call admission control, E9-1-1, or media bypass.</span></span>

<div>

## <a name="to-create-a-network-site-by-using-management-shell"></a><span data-ttu-id="15805-122">管理シェルを使用してネットワークサイトを作成するには</span><span class="sxs-lookup"><span data-stu-id="15805-122">To create a network site by using Management Shell</span></span>

1.  <span data-ttu-id="15805-123">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="15805-123">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="15805-124">New-CsNetworkSite コマンドレットを実行して、ネットワーク サイトを作成します。</span><span class="sxs-lookup"><span data-stu-id="15805-124">Run the New-CsNetworkSite cmdlet to create network sites:</span></span>
    
        New-CsNetworkSite -NetworkSiteID <string>
    
    <span data-ttu-id="15805-125">例:</span><span class="sxs-lookup"><span data-stu-id="15805-125">For example:</span></span>
    
        New-CsNetworkSite -NetworkSiteID Chicago -Description "Corporate headquarters"-NetworkRegionID NorthAmerica
    
    <span data-ttu-id="15805-126">この例では、"NorthAmerica" ネットワーク地域に "Chicago" という名前のネットワーク サイトが作成されました。</span><span class="sxs-lookup"><span data-stu-id="15805-126">In this example, you created a network site called “Chicago” that is in the “NorthAmerica” network region.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="15805-127">このコマンドを正常に実行するには、NorthAmerica ネットワーク地域があらかじめ存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="15805-127">The NorthAmerica network region must already exist for this command to run successfully.</span></span>

    
    </div>

3.  <span data-ttu-id="15805-128">トポロジのネットワーク サイトを作成するには、他のサイトの設定値を使用してステップ 2 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="15805-128">To finish creating network sites for your topology, repeat step 2 with settings for other sites.</span></span>

</div>

<div>

## <a name="to-create-a-network-site-by-using-lync-server-control-panel"></a><span data-ttu-id="15805-129">Lync Server コントロールパネルを使用してネットワークサイトを作成するには</span><span class="sxs-lookup"><span data-stu-id="15805-129">To create a network site by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="15805-130">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="15805-130">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="15805-131">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="15805-131">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

2.  <span data-ttu-id="15805-132">左側のナビゲーション バーで [**ネットワーク構成**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="15805-132">In the left navigation bar, click **Network Configuration**.</span></span>

3.  <span data-ttu-id="15805-133">[**サイト**] ナビゲーション ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="15805-133">Click the **Site** navigation button.</span></span>

4.  <span data-ttu-id="15805-134">[**新規**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="15805-134">Click **New**.</span></span>

5.  <span data-ttu-id="15805-135">[**新しいサイト**] ページで、[**名前**] をクリックしてネットワーク サイトの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="15805-135">On the **New Site** page, click **Name** and then type a name for the network site.</span></span>

6.  <span data-ttu-id="15805-136">[**地域**] をクリックして、リストで地域をクリックします。</span><span class="sxs-lookup"><span data-stu-id="15805-136">Click **Region**, and then click a region in the list.</span></span>

7.  <span data-ttu-id="15805-137">オプションで、[**帯域幅ポリシー**] をクリックして、リストで帯域幅ポリシーをクリックします。</span><span class="sxs-lookup"><span data-stu-id="15805-137">Optionally, click **Bandwidth policy**, and then click a bandwidth policy in the list.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="15805-138">帯域幅ポリシーが必要なのは、サイトで通話受付管理を展開する場合だけです。</span><span class="sxs-lookup"><span data-stu-id="15805-138">Bandwidth policy is required only if you deploy call admission control at the site.</span></span>

    
    </div>

8.  <span data-ttu-id="15805-139">オプションで、[**場所のポリシー**] をクリックして、リストで場所のポリシーをクリックします。</span><span class="sxs-lookup"><span data-stu-id="15805-139">Optionally, click **Location policy**, and then click a location policy in the list.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="15805-140">場所のポリシーが必要なのは、サイトで E9-1-1 を展開する場合だけです。</span><span class="sxs-lookup"><span data-stu-id="15805-140">Location policy is required only if you deploy E9-1-1 at the site.</span></span>

    
    </div>

9.  <span data-ttu-id="15805-141">オプションで、[**説明**] をクリックして、このネットワーク サイトを説明する追加情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="15805-141">Optionally, click **Description**, and then type additional information to describe this network site.</span></span>

10. <span data-ttu-id="15805-142">[**確定**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="15805-142">Click **Commit**.</span></span>

11. <span data-ttu-id="15805-143">使用しているトポロジのネットワーク サイトの作成を完了するには、他のサイトの設定値を使用してステップ 4 ～ 10 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="15805-143">To finish creating network sites for your topology, repeat steps 4 through 10 with settings for other sites.</span></span>

</div>

</div>

<div>

## <a name="modify-a-network-site"></a><span data-ttu-id="15805-144">ネットワークサイトを変更する</span><span class="sxs-lookup"><span data-stu-id="15805-144">Modify a Network Site</span></span>

<span data-ttu-id="15805-145">通話受付制御、E9、またはメディアバイパスで使用できるネットワークの領域を変更します。</span><span class="sxs-lookup"><span data-stu-id="15805-145">Modify a network region that can be used by call admission control, E9-1-1, or media bypass.</span></span>

<div>

## <a name="to-modify-a-network-site"></a><span data-ttu-id="15805-146">ネットワークサイトを変更するには</span><span class="sxs-lookup"><span data-stu-id="15805-146">To modify a network site</span></span>

1.  <span data-ttu-id="15805-147">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="15805-147">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="15805-148">Set-CsNetworkSite コマンドレットを実行して、ネットワーク サイトを変更します。</span><span class="sxs-lookup"><span data-stu-id="15805-148">Run the Set-CsNetworkSite cmdlet to modify network sites:</span></span>
    
        Set-CsNetworkSite -Identity <string>
    
    <span data-ttu-id="15805-149">例:</span><span class="sxs-lookup"><span data-stu-id="15805-149">For example:</span></span>
    
        Set-CsNetworkSite -Identity Albuquerque -NetworkRegionID NorthAmerica
    
    <span data-ttu-id="15805-p104">この例では、"Albuquerque" という名前のサイトが "NorthAmerica" ネットワーク地域に移動されます。ネットワーク サイトの構成を変更して、通話受付管理、E9-1-1、またはメディア バイパスを展開するには、Set-CsNetworkSite コマンドレットをそれぞれ BWPolicyProfileID または LocationPolicy パラメーターと組み合わせて実行し、ネットワーク サイトの設定を変更します。</span><span class="sxs-lookup"><span data-stu-id="15805-p104">In this example, the site called “Albuquerque” is moved to the “NorthAmerica” network region. To modify the network site configuration to deploy call admission control, E9-1-1, or media bypass, modify the network site settings by running the Set-CsNetworkSite cmdlet with the BWPolicyProfileID or LocationPolicy parameter, respectively.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="15805-p105">メディア バイパス用に BypassID パラメーターが用意されていますが、自動生成されるバイパス ID を上書きしないことを強くお勧めします。 メディア バイパス用にネットワーク サイトを構成するために、追加パラメーターを指定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="15805-p105">Although the BypassID parameter exists for media bypass, we strongly recommend that you do not override automatically generated bypass IDs. You do not need to specify additional parameters to configure a network site for media bypass.</span></span>

    
    </div>

3.  <span data-ttu-id="15805-154">使用しているトポロジのネットワーク サイトの変更を完了するには、他のサイトの設定値を使用してステップ 2 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="15805-154">To finish modifying network sites for your topology, repeat step 2 with settings for other sites.</span></span>

</div>

<div>

## <a name="to-modify-a-network-site-by-using-lync-server-control-panel"></a><span data-ttu-id="15805-155">Lync Server コントロールパネルを使用してネットワークサイトを変更するには</span><span class="sxs-lookup"><span data-stu-id="15805-155">To modify a network site by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="15805-156">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="15805-156">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="15805-157">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="15805-157">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

2.  <span data-ttu-id="15805-158">左側のナビゲーション バーで [**ネットワーク構成**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="15805-158">In the left navigation bar, click **Network Configuration**.</span></span>

3.  <span data-ttu-id="15805-159">[**サイト**] ナビゲーション ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="15805-159">Click the **Site** navigation button.</span></span>

4.  <span data-ttu-id="15805-160">表内で、変更するネットワーク サイトをクリックします。</span><span class="sxs-lookup"><span data-stu-id="15805-160">In the table, click the network site that you want to modify.</span></span>

5.  <span data-ttu-id="15805-161">[**編集**] をクリックして、[**詳細の表示...**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="15805-161">Click **Edit**, and then click **Show details…**.</span></span>

6.  <span data-ttu-id="15805-162">[**サイトの編集**] ページで、このネットワーク サイトの設定値を必要に応じて変更します。</span><span class="sxs-lookup"><span data-stu-id="15805-162">On the **Edit Site** page, change the values for this network site’s settings as appropriate.</span></span>

7.  <span data-ttu-id="15805-163">[**確定**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="15805-163">Click **Commit**.</span></span>

8.  <span data-ttu-id="15805-164">ネットワーク サイトの変更を完了するには、他のサイトの設定値を使用してステップ 4 ～ 7 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="15805-164">To finish modify network sites, repeat steps 4 through 7 with settings for other sites.</span></span>

<span data-ttu-id="15805-165"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="15805-165"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

