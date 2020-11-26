---
title: 'Lync Server 2013: トポロジビルダーで仲介サーバーを定義する'
description: 'Lync Server 2013: トポロジビルダーで仲介サーバーを定義します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Define a Mediation Server in Topology Builder
ms:assetid: 59d8f5ba-5064-4ea5-b4bf-2b9736e0fedd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398391(v=OCS.15)
ms:contentKeyID: 48184217
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2159b06c5587a17d24928febc11a883bc1520778
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431135"
---
# <a name="define-a-mediation-server-in-topology-builder-in-lync-server-2013"></a><span data-ttu-id="fa739-103">Lync Server 2013 でのトポロジビルダーでの仲介サーバーの定義</span><span class="sxs-lookup"><span data-stu-id="fa739-103">Define a Mediation Server in Topology Builder in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fa739-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fa739-104">

<span> </span></span></span>

<span data-ttu-id="fa739-105">_**最終更新日:** 2013-03-25_</span><span class="sxs-lookup"><span data-stu-id="fa739-105">_**Topic Last Modified:** 2013-03-25_</span></span>

<span data-ttu-id="fa739-106">このトピックの手順に従って、トポロジビルダーを使用して、まだエンタープライズ Voip を展開していないサイトで、フロントエンドプールと共に管理されているスタンドアロンの仲介サーバーまたはプールを定義します。</span><span class="sxs-lookup"><span data-stu-id="fa739-106">Follow the steps in this topic to use Topology Builder to define a stand-alone Mediation Server or a pool collocated with a Front End pool at a site for which you did not previously deploy Enterprise Voice.</span></span>

<span data-ttu-id="fa739-107">[管理者] グループのメンバーであるアカウントを使用してトポロジを定義できます。</span><span class="sxs-lookup"><span data-stu-id="fa739-107">You can define a topology using an account that is a member of the Administrators group.</span></span>

<div>

## <a name="define-mediation-server-collocated-to-a-front-end-pool"></a><span data-ttu-id="fa739-108">フロントエンドプールに併置した仲介サーバーの定義</span><span class="sxs-lookup"><span data-stu-id="fa739-108">Define Mediation Server collocated to a Front End pool</span></span>

<span data-ttu-id="fa739-109">このトピックの手順に従って、トポロジビルダーを使用して、エンタープライズ Voip を展開していないサイトのフロントエンドプールに併置されている仲介サーバーを定義します。</span><span class="sxs-lookup"><span data-stu-id="fa739-109">Follow the steps in this topic to use Topology Builder to define a Mediation Server collocated to a Front End pool in a site where Enterprise Voice has not been previously deployed.</span></span>

<div>

## <a name="to-add-a-mediation-server-to-a-front-end-pool"></a><span data-ttu-id="fa739-110">フロントエンドプールに仲介サーバーを追加するには</span><span class="sxs-lookup"><span data-stu-id="fa739-110">To Add a Mediation Server to a Front End pool</span></span>

1.  <span data-ttu-id="fa739-111">トポロジビルダーを開始します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server Topology Builder**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="fa739-111">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="fa739-112">[トポロジビルダー] のコンソールツリーで、フロントエンドプールを定義するサイト名を展開します。</span><span class="sxs-lookup"><span data-stu-id="fa739-112">In Topology Builder, in the console tree, expand the name of the site for which you want to define a Front End pool.</span></span>

3.  <span data-ttu-id="fa739-113">コンソールツリーで、使用するフロントエンドプールの種類を右クリックし、[ **新しいフロントエンドプール**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fa739-113">In the console tree, right-click the type of Front End pool you want, and then click **New Front End pool..**.</span></span>

4.  <span data-ttu-id="fa739-114">[**併置されたサーバーの役割の選択**] ページが表示されるまで、**新しいフロントエンド プールの定義** ウィザードを進めます。</span><span class="sxs-lookup"><span data-stu-id="fa739-114">Navigate through the **Define New Front End Pool** wizard until you reach the **Select collocated server roles** page.</span></span>

5.  <span data-ttu-id="fa739-115">[併置された **サーバーの役割を選択** してください] で、オプションの [ **仲介サーバーの検索**] をオンにします。</span><span class="sxs-lookup"><span data-stu-id="fa739-115">In **Select collocated server roles**, check the option **Collocate Mediation Server**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <UL>
    > <LI>
    > <P><span data-ttu-id="fa739-116">選択したフロントエンドプールの種類が Enterprise Edition の場合、仲介サーバーコンポーネントは、そのフロントエンドプールのすべてのフロントエンドサーバーにインストールされます。</span><span class="sxs-lookup"><span data-stu-id="fa739-116">If the type of Front End pool you selected is the Enterprise Edition, then the Mediation Server component will be installed on all the Front End Servers of that Front End pool.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="fa739-117">仲介サーバーによって使用される next-hop <STRONG>プール</STRONG> は、仲介サーバーが併置されているフロントエンドプールになります。</span><span class="sxs-lookup"><span data-stu-id="fa739-117">The <STRONG>Next hop pool</STRONG> used by the Mediation Server will be the Front End pool where the Mediation Server is collocated on.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="fa739-118">仲介サーバーで使用される <STRONG>エッジプール</STRONG> は、仲介サーバーが併置されているフロントエンドプールと同じエッジプールになります。</span><span class="sxs-lookup"><span data-stu-id="fa739-118">The <STRONG>Edge pool</STRONG> used by the Mediation Server will be the same Edge pool associated with the Front End pool where the Mediation Server is collocated on.</span></span></P></LI></UL>

    
    </div>

6.  <span data-ttu-id="fa739-119">[ **既定** にする] をクリックして、Microsoft Office Communications Server 2007 R2 から PSTN に通話をルーティングするために、このフロントエンドプールを使用するように設定します。</span><span class="sxs-lookup"><span data-stu-id="fa739-119">Click **Make Default** to use this Front End pool to route calls from Microsoft Office Communications Server 2007 R2 to the PSTN.</span></span>

7.  <span data-ttu-id="fa739-120">1つまたは複数のピアのフロントエンドプールへの関連付けが終了したら、[ **完了** ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fa739-120">Click **Finish** when you are finished associating one or more peers to the Front End pool.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="fa739-121">エンタープライズ Voip 展開プロセスの次の手順に進む前に、指定した Fqdn を使用して、仲介サーバープール (たとえば、仲介サーバーコンポーネントが含まれているフロントエンドプール) であることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="fa739-121">Before you proceed to the next step in the Enterprise Voice deployment process, make sure that the Mediation Server pool (i.e. Front End pool with the Mediation Server component collocated) is using the FQDNs that you specified.</span></span>

    
    </div>

8.  <span data-ttu-id="fa739-122">次に、展開ガイドドキュメントの「 [Lync server 2013 のトポロジを公開](lync-server-2013-publish-the-topology.md) する」の手順に従って、必要に応じて、仲介サーバーのリッスンポートを変更する次の手順に進みます。</span><span class="sxs-lookup"><span data-stu-id="fa739-122">Next, follow the procedures in [Publish the topology in Lync Server 2013](lync-server-2013-publish-the-topology.md) in the Deployment Guide documentation to add the Mediation Server to your topology before proceeding to the next step of modifying the listening ports of the Mediation Server if needed.</span></span> <span data-ttu-id="fa739-123">トポロジを定義または変更するには、トポロジビルダーを使用するたびにトポロジを公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fa739-123">You must publish your topology each time you use Topology Builder to define or modify your topology.</span></span>

</div>

</div>

<div>

## <a name="define-stand-alone-mediation-server"></a><span data-ttu-id="fa739-124">スタンドアロンの仲介サーバーを定義する</span><span class="sxs-lookup"><span data-stu-id="fa739-124">Define stand-alone Mediation Server</span></span>

<span data-ttu-id="fa739-125">このトピックの手順に従って、トポロジビルダーを使用して、エンタープライズボイスが以前に展開されていないサイトで、スタンドアロンの仲介サーバーまたはプールを定義します。</span><span class="sxs-lookup"><span data-stu-id="fa739-125">Follow the steps in this topic to use Topology Builder to define a stand-alone Mediation Server or pool at a site where Enterprise Voice has not been previously deployed.</span></span>

<span data-ttu-id="fa739-126">このサイトでフロントエンドプールに併置されている仲介サーバーを既に展開している場合は、 [lync server 2013 で trunks を構成](lync-server-2013-configuring-trunks.md)する前に、このセクションをスキップし、[仲介サーバー用のファイルを lync Server 2013 にインストール](lync-server-2013-install-the-files-for-mediation-server.md)することができます。</span><span class="sxs-lookup"><span data-stu-id="fa739-126">If you already deployed Mediation Servers collocated to Front End pools at this site, you can skip this section and [Install the files for Mediation Server in Lync Server 2013](lync-server-2013-install-the-files-for-mediation-server.md) before proceeding to [Configuring trunks in Lync Server 2013](lync-server-2013-configuring-trunks.md).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="fa739-127">このセクションでは、少なくとも1つのフロントエンドプールを既にセットアップしていることを前提としています。「 <A href="lync-server-2013-define-and-configure-a-front-end-pool-or-standard-edition-server.md">Lync server 2013 でフロントエンドプールまたは Standard Edition サーバーを定義して構成</A> する」の説明に従って、展開ガイドドキュメントの「 <A href="lync-server-2013-publish-the-topology.md">lync server 2013 でトポロジを公開</A> する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fa739-127">This section assumes that you have already setup at least one Front End pool, as described in <A href="lync-server-2013-define-and-configure-a-front-end-pool-or-standard-edition-server.md">Define and configure a Front End pool or Standard Edition server in Lync Server 2013</A> and <A href="lync-server-2013-publish-the-topology.md">Publish the topology in Lync Server 2013</A> in the Deployment Guide documentation.</span></span>



</div>

<div>

## <a name="to-add-a-mediation-server"></a><span data-ttu-id="fa739-128">仲介サーバーを追加するには</span><span class="sxs-lookup"><span data-stu-id="fa739-128">To Add a Mediation Server</span></span>

1.  <span data-ttu-id="fa739-129">トポロジビルダーを開始します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server Topology Builder**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="fa739-129">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="fa739-130">[トポロジビルダー] のコンソールツリーで、仲介サーバーを定義するサイトの名前を展開します。</span><span class="sxs-lookup"><span data-stu-id="fa739-130">In Topology Builder, in the console tree, expand the name of the site for which you want to define a Mediation Server.</span></span>

3.  <span data-ttu-id="fa739-131">コンソールツリーで、[ **仲介プール** ] ノードを右クリックし、[ **仲介サーバープール**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fa739-131">In the console tree, right-click the **Mediation pools** node, and then click **Mediation Server pool**.</span></span>

4.  <span data-ttu-id="fa739-132">[ **新しい仲介プールの定義**] で、仲介サーバープールの完全修飾ドメイン名 (FQDN) を入力します。</span><span class="sxs-lookup"><span data-stu-id="fa739-132">In **Define New Mediation Pool**, type the Mediation Server pool fully qualified domain name (FQDN).</span></span>

5.  <span data-ttu-id="fa739-133">次に、以下のいずれかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="fa739-133">Next, do one of the following:</span></span>
    
      - <span data-ttu-id="fa739-134">プールに複数の仲介サーバーを展開して高可用性を提供する場合は、[ **複数のコンピュータープール**] を選びます。</span><span class="sxs-lookup"><span data-stu-id="fa739-134">If you want to deploy multiple Mediation Servers in the pool to provide high availability, then select **Multiple computer pool**.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="fa739-135">複数の仲介サーバーがある仲介サーバープールをサポートするには、DNS の負荷分散を展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fa739-135">You must deploy DNS load balancing to support Mediation Server pools that have multiple Mediation Servers.</span></span> <span data-ttu-id="fa739-136">詳細については、計画ドキュメントの「 <A href="lync-server-2013-dns-load-balancing.md">Lync server 2013 の dns の負荷</A> 分散での Dns 負荷分散の使用」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="fa739-136">For details, see the Using DNS Load Balancing on Mediation Server Pools section of <A href="lync-server-2013-dns-load-balancing.md">DNS load balancing in Lync Server 2013</A> in the Planning documentation.</span></span>

        
        </div>
    
      - <span data-ttu-id="fa739-137">高可用性を必要としないため、プールに1つの仲介サーバーのみを展開する場合は、[ **単一コンピュータープール**] を選びます。</span><span class="sxs-lookup"><span data-stu-id="fa739-137">If you want to deploy only one Mediation Server in the pool because you do not require high availability, then select **Single computer pool**.</span></span> <span data-ttu-id="fa739-138">以下のステップは省略してください。</span><span class="sxs-lookup"><span data-stu-id="fa739-138">Skip the following step.</span></span>

6.  <span data-ttu-id="fa739-139">前の手順 **で複数のコンピュータープール** を選択した場合は、[ **このプールのコンピューターを定義** する] 項目で [コンピューターの **fqdn**] をクリックし、プール内の各サーバーの fqdn を入力して、[ **追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fa739-139">If you selected **Multiple computer pool** in the previous step, on the **Define the computers in this pool** item, click **Computer FQDN**, type the FQDN of each server in the pool, and then click **Add**.</span></span> <span data-ttu-id="fa739-140">プールに追加するその他のすべての仲介サーバーについて、この手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="fa739-140">Repeat this step for all other Mediation Servers that you want to add to the pool.</span></span> <span data-ttu-id="fa739-141">プール内のすべてのコンピューターを定義したら、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fa739-141">When you have defined all the computers in the pool, click **Next**.</span></span>

7.  <span data-ttu-id="fa739-142">[ **次ホップの選択** ] ページで、[ **次ホッププール**] をクリックし、この仲介サーバープールを使用するフロントエンドプールの FQDN をクリックして、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fa739-142">On the **Select the next hop** page, click **Next hop pool**, click the FQDN of the Front End pool that will use this Mediation Server pool, and then click **Next**.</span></span>

8.  <span data-ttu-id="fa739-143">[**エッジ サーバーの選択**] ページで、次のどちらかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="fa739-143">On the **Select an Edge Server** page, do one of the following:</span></span>
    
      - <span data-ttu-id="fa739-144">エンタープライズ Voip が有効になっている外部ユーザーに PSTN 接続を提供する場合は、[ **この仲介サーバーで使用されるエッジプールを選択** してください] で、この仲介サーバープールを使用してそれらの外部ユーザーへの pstn 接続を提供するエッジサーバープールの FQDN をクリックし、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fa739-144">If you want to provide PSTN connectivity to external users enabled for Enterprise Voice, under **Select Edge Pool used by this Mediation Server**, click the FQDN of the Edge Server pool that will use this Mediation Server pool to provide PSTN connectivity to those external users, and then click **Next**.</span></span>
    
      - <span data-ttu-id="fa739-145">外部ユーザーをエンタープライズボイスとして有効にする予定がない場合、または内部ネットワークの外部にいるユーザーに PSTN 接続を提供しない場合は、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fa739-145">If you do not plan to enable external users for Enterprise Voice, or if you do not want to provide PSTN connectivity to users when they are outside the internal network, click **Next**.</span></span>

9.  <span data-ttu-id="fa739-146">次に、展開ドキュメントの「 [Lync server 2013 でトポロジを公開](lync-server-2013-publish-the-topology.md) する」の手順に従って、仲介サーバーをトポロジに追加します。</span><span class="sxs-lookup"><span data-stu-id="fa739-146">Next, follow the procedures in [Publish the topology in Lync Server 2013](lync-server-2013-publish-the-topology.md) in the Deployment documentation to add the Mediation Server to the topology.</span></span> <span data-ttu-id="fa739-147">トポロジビルダーを使用してトポロジを作成または変更するたびにトポロジを公開する必要があります。これにより、Lync Server を実行しているサーバーのファイルをインストールするためにデータを使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="fa739-147">You must publish your topology each time you use Topology Builder to build or modify your topology so that the data can be used to install the files for servers that are running Lync Server.</span></span> <span data-ttu-id="fa739-148">次の手順に進んで、必要に応じて、仲介サーバーのリッスンポートを変更します。</span><span class="sxs-lookup"><span data-stu-id="fa739-148">Then continue to the next steps to modify the listening ports on the Mediation Server, if necessary.</span></span>

</div>

</div>

<div>

## <a name="define-the-mediation-server-listening-ports"></a><span data-ttu-id="fa739-149">仲介サーバーのリッスンポートを定義する</span><span class="sxs-lookup"><span data-stu-id="fa739-149">Define the Mediation Server Listening Ports</span></span>

<span data-ttu-id="fa739-150">このトピックの手順に従って、トポロジビルダーを使用してリッスンポートを定義します。仲介サーバーまたはプールは、ゲートウェイピアからの着信接続を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="fa739-150">Follow the steps in this topic to use Topology Builder to define the listening ports a Mediation Server or pool will accept incoming connections from a gateway peer.</span></span>

<div>

## <a name="to-modify-the-mediation-server-listening-ports"></a><span data-ttu-id="fa739-151">仲介サーバーのリッスンポートを変更するには</span><span class="sxs-lookup"><span data-stu-id="fa739-151">To Modify the Mediation Server Listening Ports</span></span>

1.  <span data-ttu-id="fa739-152">トポロジビルダーを開始します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server Topology Builder**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="fa739-152">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="fa739-153">[トポロジビルダー] のコンソールツリーで、[ **仲介プール** ] ノードを展開し、前に作成した仲介サーバーを右クリックします。</span><span class="sxs-lookup"><span data-stu-id="fa739-153">In Topology Builder, in the console tree, expand the **Mediation pools** node, and right-click the Mediation Server previously created.</span></span>

3.  <span data-ttu-id="fa739-154">既定では、仲介サーバー上の SIP リスニングポートは、Lync Server からの TLS トラフィック用の5070であり5067、ピアからの TLS トラフィック (ゲートウェイ、PBXes、または SBCs) を対象としています。</span><span class="sxs-lookup"><span data-stu-id="fa739-154">By default, the SIP listening ports on the Mediation Server are 5070 for TLS traffic from Lync Server, 5067 for TLS traffic from peers (gateways, PBXes, or SBCs).</span></span> <span data-ttu-id="fa739-155">TCP ポートは既定で無効になっています。</span><span class="sxs-lookup"><span data-stu-id="fa739-155">TCP port is disabled by default.</span></span> <span data-ttu-id="fa739-156">TLS をサポートしていないゲートウェイがある場合は、TCP ポートを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fa739-156">You must enable TCP port if you have gateways that do not support TLS.</span></span>

4.  <span data-ttu-id="fa739-157">目的の TLS または TCP リッスンポートの範囲を指定する仲介サーバーは、PSTN ゲートウェイからの着信接続を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="fa739-157">Specify the desired TLS or TCP listening port range the Mediation Server will accept incoming connections from PSTN gateways.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="fa739-158">[<STRONG>TCP ポートの有効化</STRONG>] がオフになっている場合は、TCP ポート範囲を入力する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="fa739-158">Entering a TCP port range is not required if <STRONG>Enable TCP port</STRONG> is not checked.</span></span> <span data-ttu-id="fa739-159">この設定はオプションです。</span><span class="sxs-lookup"><span data-stu-id="fa739-159">This setting is optional.</span></span>

    
    </div>

<span data-ttu-id="fa739-160">次に、lync server [2013 のトポロジビルダーでゲートウェイを定義](lync-server-2013-define-a-gateway-in-topology-builder.md) し、「 [lync Server 2013 の仲介サーバー用のファイルをインストール](lync-server-2013-install-the-files-for-mediation-server.md)する」の手順に従って、プール内の各仲介サーバーにファイルをインストールします。</span><span class="sxs-lookup"><span data-stu-id="fa739-160">Next, [Define a gateway in Topology Builder in Lync Server 2013](lync-server-2013-define-a-gateway-in-topology-builder.md) and install the files on each Mediation Server in the pool by following the procedures in [Install the files for Mediation Server in Lync Server 2013](lync-server-2013-install-the-files-for-mediation-server.md).</span></span>

<span data-ttu-id="fa739-161"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fa739-161"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

