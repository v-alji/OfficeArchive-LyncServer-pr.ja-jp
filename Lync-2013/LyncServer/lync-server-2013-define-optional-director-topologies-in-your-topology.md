---
title: 'Lync Server 2013: トポロジにオプションのディレクター トポロジを定義する'
description: 'Lync Server 2013: トポロジでオプションのディレクタートポロジを定義します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Define optional Director topologies in your topology
ms:assetid: 8e9a659d-23b0-401d-b296-59c7df414d49
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398717(v=OCS.15)
ms:contentKeyID: 48184808
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5bc82108d4277969489739fc81db07ec6f96bb96
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431051"
---
# <a name="define-optional-director-topologies-in-your-topology-for-lync-server-2013"></a><span data-ttu-id="673f2-103">Lync Server 2013 のトポロジにオプションのディレクター トポロジを定義する</span><span class="sxs-lookup"><span data-stu-id="673f2-103">Define optional Director topologies in your topology for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="673f2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="673f2-104">

<span> </span></span></span>

<span data-ttu-id="673f2-105">_**最終更新日:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="673f2-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="673f2-106">Lync Server 2013 ディレクターは、単一インスタンスのサーバーにすることも、複数のディレクターの負荷分散プールとしてインストールして可用性と容量を高めることもできます。</span><span class="sxs-lookup"><span data-stu-id="673f2-106">Lync Server 2013 Directors can be single-instance servers or they can be installed as a load-balanced pool of multiple Directors for higher availability and capacity.</span></span> <span data-ttu-id="673f2-107">ハードウェア負荷分散とドメインネームシステム (DNS) の負荷分散は両方ともサポートされています。</span><span class="sxs-lookup"><span data-stu-id="673f2-107">Both hardware load balancing and Domain Name System (DNS) load balancing are supported.</span></span> <span data-ttu-id="673f2-108">このトピックでは、ディレクタープールの DNS 負荷分散を構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="673f2-108">This topic explains how to configure DNS load balancing for Director pools.</span></span>

<span data-ttu-id="673f2-109">トポロジを正常に発行、有効化、または無効にするには、サーバーの役割を追加または削除するときに、 **RTCUniversalServerAdmins** と **domain Admins** グループのメンバーであるユーザーとしてログオンする必要があります。</span><span class="sxs-lookup"><span data-stu-id="673f2-109">To successfully publish, enable, or disable a topology when you add or remove a server role, you should be logged on as a user who is a member of the **RTCUniversalServerAdmins** and **Domain Admins** groups.</span></span> <span data-ttu-id="673f2-110">また、サーバーの役割を追加するための適切な管理者権限と権限を委任することもできます。</span><span class="sxs-lookup"><span data-stu-id="673f2-110">You can also delegate the proper administrator rights and permissions for adding server roles.</span></span> <span data-ttu-id="673f2-111">詳細については、Standard Edition server または Enterprise Edition server 展開ドキュメントの「 [Lync server 2013 でのセットアップ権限の委任](lync-server-2013-delegate-setup-permissions.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="673f2-111">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md) in the Standard Edition server or Enterprise Edition server Deployment documentation.</span></span> <span data-ttu-id="673f2-112">その他の構成変更については、 **RTCUniversalServerAdmins** グループのメンバーシップのみが必要です。</span><span class="sxs-lookup"><span data-stu-id="673f2-112">For other configuration changes, only membership in the **RTCUniversalServerAdmins** group is required.</span></span>

<span data-ttu-id="673f2-113">このトピックでは、2つのディレクタートポロジのトポロジを定義して公開するための手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="673f2-113">This topic describes the steps to define and publish the topology for the two Director topologies:</span></span>

  - <span data-ttu-id="673f2-114">ディレクターを定義するには (単一インスタンス)</span><span class="sxs-lookup"><span data-stu-id="673f2-114">To define the Director (single instance)</span></span>

  - <span data-ttu-id="673f2-115">ディレクター (複数のディレクタープール) を定義するには</span><span class="sxs-lookup"><span data-stu-id="673f2-115">To define the Director (multiple Director pool)</span></span>

<div>

## <a name="to-define-the-director-single-instance"></a><span data-ttu-id="673f2-116">ディレクターを定義するには (単一インスタンス)</span><span class="sxs-lookup"><span data-stu-id="673f2-116">To define the Director (single instance)</span></span>

1.  <span data-ttu-id="673f2-117">トポロジビルダーを開始します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server Topology Builder**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="673f2-117">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="673f2-118">[ようこそ] ページで、[ **既存の展開からトポロジをダウンロード**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="673f2-118">On the welcome page, click **Download Topology from Existing Deployment**.</span></span>

3.  <span data-ttu-id="673f2-119">[名前を付け **てトポロジを保存** ] ダイアログボックスで、既存のトポロジのローカルコピーの名前と場所を入力し、[ **保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="673f2-119">In the **Save Topology As** dialog box, type the name and location of the local copy of the existing topology, and then click **Save**.</span></span>

4.  <span data-ttu-id="673f2-120">ディレクターを追加する予定のサイトを展開し、[ **ディレクタープール**] を右クリックして、[ **新しいディレクタープール**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="673f2-120">Expand the site in which you plan to add the Director, right-click **Director pools**, and then click **New Director Pool**.</span></span>

5.  <span data-ttu-id="673f2-121">[ **ディレクタープールの FQDN の定義** ] ダイアログボックスで、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="673f2-121">In the **Define the Director pool FQDN** dialog box, do the following:</span></span>
    
      - <span data-ttu-id="673f2-122">[ **プールの fqdn**] に、ディレクタープールの fqdn を入力します。</span><span class="sxs-lookup"><span data-stu-id="673f2-122">In **Pool FQDN**, type the FQDN for the Director pool.</span></span>
    
      - <span data-ttu-id="673f2-123">[ **単一コンピュータープール**] をクリックし、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="673f2-123">Click **Single computer pool**, and then click **Next**.</span></span>

6.  <span data-ttu-id="673f2-124">[ **ファイル共有の定義** ] ダイアログボックスで、次のいずれかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="673f2-124">In the **Define the file share** dialog box, do one of the following:</span></span>
    
    1.  <span data-ttu-id="673f2-125">既存のファイル共有を使用するには、[ **以前定義したファイル共有を使用** する] をクリックし、一覧からファイル共有を選択して、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="673f2-125">To use an existing file share, click **Use a previously defined file share**, select a file share from the list, and then click **Next**.</span></span>
    
    2.  <span data-ttu-id="673f2-126">新しいファイル共有を作成するには、[ **新しいファイル共有の定義**] をクリックし、[ **ファイルサーバー fqdn**] でファイル共有の場所の FQDN を入力して、[ **ファイル共有**] に共有の名前を入力し、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="673f2-126">To create a new file share, click **Define a new file share**, type the FQDN for the location of the file share in **File Server FQDN**, type the name of the share in **File Share**, and then click **Next**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="673f2-127">この手順で指定または作成したファイル共有は、トポロジを公開する前に存在しているか、作成されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="673f2-127">The file share that you specify or create in this step must exist or be created prior to publishing the topology.</span></span><BR><span data-ttu-id="673f2-128">ディレクターに割り当てられているファイル共有は、実際には使用されていないため、組織内の任意のプールのファイル共有を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="673f2-128">The file share assigned to a Director is not actually used, so you can assign the file share of any pool in the organization.</span></span>

    
    </div>

7.  <span data-ttu-id="673f2-129">[ **Web サービスの URL の指定** ] ダイアログボックスの [ **外部ベース URL**] で、ディレクターの FQDN を指定し、[ **完了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="673f2-129">In the **Specify the Web Services URL** dialog box, in **External Base URL**, specify the FQDN for the Directors, and then click **Finish**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="673f2-130">この名前は、インターネット DNS サーバーから解決できる必要があります。また、その URL への HTTP/HTTPS 要求をリッスンし、そのユーザーをそのディレクターの外部 Web サービスの仮想ディレクトリにプロキシする、リバースプロキシのパブリック IP アドレスをポイントする必要があります。</span><span class="sxs-lookup"><span data-stu-id="673f2-130">The name must be resolvable from Internet DNS servers and point to the public IP address of the reverse proxy, which listens for HTTP/HTTPS requests to that URL and proxies them to the external Web Services virtual directory on that Director.</span></span>

    
    </div>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="673f2-131">複数のフロントエンドプールまたはフロントエンドサーバーがある場合は、外部 Web サービスの FQDN が一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="673f2-131">If you have more than one Front End pool or Front End Server the external Web services FQDN must be unique.</span></span> <span data-ttu-id="673f2-132">たとえば、フロントエンドサーバーの外部 Web サービス FQDN を <STRONG>pool01.contoso.com</STRONG>として定義する場合、別のフロントエンドプールまたはフロントエンドサーバーに対して <STRONG>pool01.contoso.com</STRONG> を使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="673f2-132">For example, if you define the external Web services FQDN of a Front End Server as <STRONG>pool01.contoso.com</STRONG>, you cannot use <STRONG>pool01.contoso.com</STRONG> for another Front End pool or Front End Server.</span></span> <span data-ttu-id="673f2-133">ディレクターも展開する場合、任意のディレクターまたはディレクタープール用に定義された外部 Web サービスの FQDN は、他のすべてのディレクターまたはディレクタープールと、フロントエンドプールまたはフロントエンドサーバーから一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="673f2-133">If you are also deploying Directors, the external Web services FQDN defined for any Director or Director pool must be unique from any other Director or Director pool as well as any Front End pool or Front End Server.</span></span> <span data-ttu-id="673f2-134">自己定義の FQDN を使用して内部 web サービスを上書きする場合、各 FQDN は、他のフロントエンドプール、ディレクター、またはディレクタープールから一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="673f2-134">If decide to override the Internal web services with a self-defined FQDN, each FQDN must be unique from any other Front End pool, Director or a Director pool.</span></span>

    
    </div>

8.  <span data-ttu-id="673f2-135">トポロジを公開します。</span><span class="sxs-lookup"><span data-stu-id="673f2-135">Publish the topology.</span></span>

</div>

<div>

## <a name="to-define-the-director-multiple-director-pool"></a><span data-ttu-id="673f2-136">ディレクター (複数のディレクタープール) を定義するには</span><span class="sxs-lookup"><span data-stu-id="673f2-136">To define the Director (multiple Director pool)</span></span>

1.  <span data-ttu-id="673f2-137">トポロジビルダーを開始します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server Topology Builder**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="673f2-137">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="673f2-138">[ようこそ] ページで、[ **既存の展開からトポロジをダウンロード**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="673f2-138">On the welcome page, click **Download Topology from Existing Deployment**.</span></span>

3.  <span data-ttu-id="673f2-139">[名前を付け **てトポロジを保存** ] ダイアログボックスで、既存のトポロジのローカルコピーの名前と場所を入力し、[ **保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="673f2-139">In the **Save Topology As** dialog box, type the name and location of the local copy of the existing topology, and then click **Save**.</span></span>

4.  <span data-ttu-id="673f2-140">ディレクターを追加する予定のサイトを展開し、[ **ディレクタープール**] を右クリックして、[ **新しいディレクタープール**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="673f2-140">Expand the site in which you plan to add the Director, right-click **Director pools**, and then click **New Director Pool**.</span></span>

5.  <span data-ttu-id="673f2-141">[ **ディレクタープールの FQDN の定義** ] ダイアログボックスで、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="673f2-141">In the **Define the Director pool FQDN** dialog box, do the following:</span></span>
    
      - <span data-ttu-id="673f2-142">[ **プールの fqdn**] に、ディレクタープールの fqdn を入力します。</span><span class="sxs-lookup"><span data-stu-id="673f2-142">In **Pool FQDN**, type the FQDN for the Director pool.</span></span>
    
      - <span data-ttu-id="673f2-143">[ **複数のコンピュータープール**] をクリックし、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="673f2-143">Click **Multiple computer pool**, and then click **Next**.</span></span>

6.  <span data-ttu-id="673f2-144">[ **このプールのコンピューターの定義** ] ダイアログボックスで、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="673f2-144">In the **Define the computers in this pool** dialog box, do the following:</span></span>
    
      - <span data-ttu-id="673f2-145">最初のプールメンバーのコンピューターの FQDN を指定し、[ **追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="673f2-145">Specify the computer FQDN of the first pool member, and then click **Add**.</span></span>
    
      - <span data-ttu-id="673f2-146">追加するコンピューターごとに、上記の手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="673f2-146">Repeat the previous step for each computer that you want to add.</span></span> <span data-ttu-id="673f2-147">完了したら、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="673f2-147">When you are finished, click **Next**.</span></span>

7.  <span data-ttu-id="673f2-148">[ **ファイル共有の定義** ] ダイアログボックスで、次のいずれかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="673f2-148">In the **Define the file share** dialog box, do one of the following:</span></span>
    
      - <span data-ttu-id="673f2-149">既存のファイル共有を使用するには、[ **以前定義したファイル共有を使用** する] をクリックし、一覧からファイル共有を選択して、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="673f2-149">To use an existing file share, click **Use a previously defined file share**, select a file share from the list, and then click **Next**.</span></span>
    
      - <span data-ttu-id="673f2-150">新しいファイル共有を作成するには、[ **新しいファイル共有の定義**] をクリックし、[ **ファイルサーバー fqdn**] でファイル共有の場所の FQDN を入力して、[ **ファイル共有**] に共有の名前を入力し、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="673f2-150">To create a new file share, click **Define a new file share**, type the FQDN for the location of the file share in **File Server FQDN**, type the name of the share in **File Share**, and then click **Next**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="673f2-151">この手順で指定または作成したファイル共有は、トポロジを公開する前に存在しているか、作成されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="673f2-151">The file share that you specify or create in this step must exist or be created prior to publishing the topology.</span></span><BR><span data-ttu-id="673f2-152">ディレクターに割り当てられているファイル共有は、実際には使用されていないため、組織内の任意のプールのファイル共有を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="673f2-152">The file share assigned to a Director is not actually used, so you can assign the file share of any pool in the organization.</span></span>

    
    </div>

8.  <span data-ttu-id="673f2-153">[ **Web サービスの URL の指定** ] ダイアログボックスの [ **外部ベース URL**] で、ディレクターの FQDN を指定し、[ **完了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="673f2-153">In the **Specify the Web Services URL** dialog box, in **External Base URL**, specify the FQDN for the Directors, and then click **Finish**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="673f2-154">この名前は、インターネット DNS サーバーから解決できる必要があります。また、その URL に送信された HTTP/HTTPS 要求をリッスンし、それらをそのディレクタープールの外部 Web サービスの仮想ディレクトリにプロキシする、リバースプロキシのパブリック IP アドレスをポイントする必要があります。</span><span class="sxs-lookup"><span data-stu-id="673f2-154">The name must be resolvable from Internet DNS servers and point to the public IP address of the reverse proxy, which listens for HTTP/HTTPS requests sent to that URL and proxies them to the external Web Services virtual directory on that Director pool.</span></span>

    
    </div>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="673f2-155">複数のフロントエンドプールまたはフロントエンドサーバーがある場合は、外部 Web サービスの FQDN が一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="673f2-155">If you have more than one Front End pool or Front End Server the external Web services FQDN must be unique.</span></span> <span data-ttu-id="673f2-156">たとえば、フロントエンドサーバーの外部 Web サービス FQDN を <STRONG>pool01.contoso.com</STRONG>として定義する場合、別のフロントエンドプールまたはフロントエンドサーバーに対して <STRONG>pool01.contoso.com</STRONG> を使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="673f2-156">For example, if you define the external Web services FQDN of a Front End Server as <STRONG>pool01.contoso.com</STRONG>, you cannot use <STRONG>pool01.contoso.com</STRONG> for another Front End pool or Front End Server.</span></span> <span data-ttu-id="673f2-157">ディレクターも展開する場合、任意のディレクターまたはディレクタープール用に定義された外部 Web サービスの FQDN は、他のすべてのディレクターまたはディレクタープールと、フロントエンドプールまたはフロントエンドサーバーから一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="673f2-157">If you are also deploying Directors, the external Web services FQDN defined for any Director or Director pool must be unique from any other Director or Director pool as well as any Front End pool or Front End Server.</span></span> <span data-ttu-id="673f2-158">自己定義の FQDN を使用して内部 web サービスを上書きする場合、各 FQDN は、他のフロントエンドプール、ディレクター、またはディレクタープールから一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="673f2-158">If decide to override the Internal web services with a self-defined FQDN, each FQDN must be unique from any other Front End pool, Director or a Director pool.</span></span>

    
    </div>

9.  <span data-ttu-id="673f2-159">トポロジを公開します。</span><span class="sxs-lookup"><span data-stu-id="673f2-159">Publish the topology.</span></span>

<span data-ttu-id="673f2-160"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="673f2-160"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

