---
title: 'Lync Server 2013: Web サービスの URL を変更する'
description: 'Lync Server 2013: Web サービスの URL を変更します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Change the Web Services URL
ms:assetid: 4cee37c0-3b99-4207-997f-bf4229d760c0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520992(v=OCS.15)
ms:contentKeyID: 48184063
ms.date: 11/16/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 78a7a9b70d475aa952a43d215a8e5cd2068911e6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435154"
---
# <a name="change-the-web-services-url-in-lync-server-2013"></a><span data-ttu-id="a2234-103">Lync Server 2013 で Web サービスの URL を変更する</span><span class="sxs-lookup"><span data-stu-id="a2234-103">Change the Web Services URL in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a2234-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a2234-104">

<span> </span></span></span>

<span data-ttu-id="a2234-105">_**最終更新日:** 2015-11-16_</span><span class="sxs-lookup"><span data-stu-id="a2234-105">_**Topic Last Modified:** 2015-11-16_</span></span>

<span data-ttu-id="a2234-106">フロントエンドプールと Standard Edition サーバーをセットアップするときに、外部 Web ファームの完全修飾ドメイン名 (FQDN) と関連付けられたポートを構成するオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="a2234-106">When you set up your Front End pools and Standard Edition servers, you have the option to configure an external Web farm fully qualified domain name (FQDN) and associated ports.</span></span> <span data-ttu-id="a2234-107">Lync Server 展開ウィザードを実行したときにこの URL を構成しなかった場合は、これらの設定を手動で構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2234-107">If you did not configure this URL when you ran the Lync Server Deployment Wizard, you need to manually configure these settings.</span></span> <span data-ttu-id="a2234-108">通常、管理者はこれらの設定を変更する必要はありません。これは、推奨される既定のポートであるためです。</span><span class="sxs-lookup"><span data-stu-id="a2234-108">An administrator typically does not need to modify these settings, as these are the recommended and default ports.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a2234-109">Standard Edition サーバーの構成中に、次のスクリーンショットが表示されたため、[FQDN の上書き] オプションが無効になっています。</span><span class="sxs-lookup"><span data-stu-id="a2234-109">The following screen shot was taken while configuring a Standard Edition server, so the Override FQDN option is disabled.</span></span> <span data-ttu-id="a2234-110">このオプションは、フロントエンドプールで Enterprise Edition サーバーを構成するときに有効になります。</span><span class="sxs-lookup"><span data-stu-id="a2234-110">That option is enabled when configuring an Enterprise Edition server in a Front End pool.</span></span>



</div>

<span data-ttu-id="a2234-111">![Web サービスプール設定を編集する](images/Gg520992.fbdf5cc9-479a-463f-bb1d-53575ecdfc9d(OCS.15).jpg "Web サービスプール設定を編集する")</span><span class="sxs-lookup"><span data-stu-id="a2234-111">![Edit Web Services Pool Settings](images/Gg520992.fbdf5cc9-479a-463f-bb1d-53575ecdfc9d(OCS.15).jpg "Edit Web Services Pool Settings")</span></span>

<div>

## <a name="to-configure-web-services"></a><span data-ttu-id="a2234-112">Web サービスを構成するには</span><span class="sxs-lookup"><span data-stu-id="a2234-112">To configure web services</span></span>

1.  <span data-ttu-id="a2234-113">トポロジ ビルダーがインストールされているコンピューターに、Domain Admins グループおよび RTCUniversalServerAdmins グループのメンバーとしてログオンします。</span><span class="sxs-lookup"><span data-stu-id="a2234-113">Log on to the computer where Topology Builder is installed as a member of the Domain Admins group and the RTCUniversalServerAdmins group.</span></span>

2.  <span data-ttu-id="a2234-114">トポロジビルダーを開始します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server Topology Builder**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2234-114">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

3.  <span data-ttu-id="a2234-115">[トポロジビルダー] のコンソールツリーで、[ **Standard Edition フロントエンドサーバー**]、[ **Enterprise Edition フロントエンドプール**]、[ **ディレクトリプール**] の [プール名] を選びます。</span><span class="sxs-lookup"><span data-stu-id="a2234-115">In Topology Builder, in the console tree under **Standard Edition Front End Servers**, **Enterprise Edition Front End pools**, and **Directory pools**, select the pool name.</span></span> <span data-ttu-id="a2234-116">名前を右クリックし、[ **プロパティの編集**] をクリックして、[ **Web サービス**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2234-116">Right-click the name, click **Edit Properties**, and then click **Web Services**.</span></span>

4.  <span data-ttu-id="a2234-117">**外部 Web サービスの FQDN** を追加または編集して、[ **OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2234-117">Add or edit the **External Web Services FQDN**, and then click **OK**.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="a2234-118">複数のフロントエンドプールまたはフロントエンドサーバーがある場合は、外部 Web サービスの FQDN が一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2234-118">If you have more than one Front End pool or Front End Server the external Web services FQDN must be unique.</span></span> <span data-ttu-id="a2234-119">たとえば、フロントエンドサーバーの外部 Web サービス FQDN を <STRONG>pool01.contoso.com</STRONG>として定義する場合、別のフロントエンドプールまたはフロントエンドサーバーに対して <STRONG>pool01.contoso.com</STRONG> を使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="a2234-119">For example, if you define the external Web services FQDN of a Front End Server as <STRONG>pool01.contoso.com</STRONG>, you cannot use <STRONG>pool01.contoso.com</STRONG> for another Front End pool or Front End Server.</span></span> <span data-ttu-id="a2234-120">ディレクターも展開する場合、任意のディレクターまたはディレクタープール用に定義された外部 Web サービスの FQDN は、他のすべてのディレクターまたはディレクタープールと、フロントエンドプールまたはフロントエンドサーバーから一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2234-120">If you are also deploying Directors, the external Web services FQDN defined for any Director or Director pool must be unique from any other Director or Director pool as well as any Front End pool or Front End Server.</span></span>

    
    </div>

5.  <span data-ttu-id="a2234-121">リッスンおよび公開されているポートが、お使いの環境に対して正しく構成されていることを確認します</span><span class="sxs-lookup"><span data-stu-id="a2234-121">Verify the listening and published ports are configured correctly for your environment.</span></span>

6.  <span data-ttu-id="a2234-122">環境内のすべての標準エディションサーバー、フロントエンドプール、およびディレクタープールについて、この手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="a2234-122">Repeat these steps for all Standard Edition servers, Front End Pools, and Director pools in your environment.</span></span>

7.  <span data-ttu-id="a2234-123">コンソールツリーで、[ **Lync Server 2013**] をクリックし、[ **操作** ] ウィンドウで [ **トポロジの公開**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2234-123">In the console tree, click **Lync Server 2013**, and then, in the **Actions** pane, click **Publish Topology**.</span></span>

<span data-ttu-id="a2234-124">リッスンポートと発行ポートを構成する際に注意すべき要件がいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="a2234-124">There are a few requirements you should be aware of when configuring the Listening and Publishing ports:</span></span>

  - <span data-ttu-id="a2234-125">表示されるリスニングポートは、各フロントエンドサーバー上でインターネットインフォメーションサーバー (IIS) 用に構成されているポートです。</span><span class="sxs-lookup"><span data-stu-id="a2234-125">The listening ports shown are the ports that are configured for Internet Information Server (IIS) on each Front End Server.</span></span>

  - <span data-ttu-id="a2234-126">内部と外部のリッスンポートは、IIS によって異なる必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2234-126">The internal and external listening ports must be different for IIS.</span></span> <span data-ttu-id="a2234-127">外部リッスンポートの場合、通常は、内部 web トラフィック用のハードウェアロードバランサーを表し、1つは外部 web トラフィックのリバースプロキシサーバーを表します。</span><span class="sxs-lookup"><span data-stu-id="a2234-127">For the external listening ports, these are typically the same because one represents the hardware load balancer for internal web traffic and one represents the reverse proxy server for external web traffic.</span></span>

  - <span data-ttu-id="a2234-128">フロントエンドプール、ディレクター、またはディレクタープールの内部 web サービスを上書きして、独自の FQDN を定義することができます。</span><span class="sxs-lookup"><span data-stu-id="a2234-128">You can override the Internal web services on a Front End pool, Director or a Director pool and define your own FQDN.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="a2234-129">自動定義の FQDN を使用して内部 web サービスを上書きする場合、各 FQDN は、他のフロントエンドプール、ディレクター、またはディレクタープールから一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2234-129">If you decide to override the Internal web services with a self-defined FQDN, each FQDN must be unique from any other Front End pool, Director or a Director pool.</span></span>

    
    </div>

  - <span data-ttu-id="a2234-130">公開されたポートは、リバースプロキシまたはハードウェアロードバランサーでリスニングポートとして構成されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2234-130">The published ports must be configured on the reverse proxy or hardware load balancer as listening ports.</span></span>

  - <span data-ttu-id="a2234-131">フロントエンドプール (この例では説明しません) については、web トラフィックがハードウェアロードバランサーを介して送信され、内部 SIP プールトラフィックが DNS ロードバランサーを経由しているため、内部 SIP プールの FQDN と内部 web サービス FQDN との間に違いがある必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2234-131">For an Front End pool (not shown in the example), the internal SIP pool FQDN must be different from the internal web services FQDN, because web traffic comes through the hardware load balancer and the internal SIP pool traffic travels comes through the DNS load balancer.</span></span> <span data-ttu-id="a2234-132">この要件は満たされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2234-132">This requirement must be met.</span></span>

  - <span data-ttu-id="a2234-133">Lync Server Standard Edition の展開では、サーバーの負荷を分散できないため、内部 web サービスの FQDN を上書きする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="a2234-133">A Lync Server Standard Edition deployment does not need or allow an internal web services FQDN to be overridden because this server cannot be load balanced.</span></span>

  - <span data-ttu-id="a2234-134">内部 SIP と web トラフィックの両方に使用している環境にハードウェアロードバランサーがある場合、トポロジビルダーで区別することはできません。</span><span class="sxs-lookup"><span data-stu-id="a2234-134">If you have a hardware load balancer in your environment that you use for both internal SIP and web traffic, the Topology Builder cannot make the distinction.</span></span>
    
    <span data-ttu-id="a2234-135">Web サービスの Fqdn は、相互に簡単に区別する必要があります。これにより、URL リダイレクションが適切なサーバーにクライアントを確実に指し示すことができます。</span><span class="sxs-lookup"><span data-stu-id="a2234-135">Web service FQDNs should be easily-differentiated from one another; that helps to ensure that URL redirection points clients towards the appropriate server.</span></span> <span data-ttu-id="a2234-136">たとえば、2つの Fqdn がある場合は、1つの meeting.contoso.com とその他の conferencing.contoso.com に名前を付けることを検討します。</span><span class="sxs-lookup"><span data-stu-id="a2234-136">For example, if you have two FQDNs you might consider naming one meeting.contoso.com and the other conferencing.contoso.com.</span></span> <span data-ttu-id="a2234-137">Meet1.contoso.com や meet2.contoso.com などの類似した名前の Fqdn を使用している場合は、リダイレクトの問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a2234-137">You could potentially run into redirection issues if you have FQDNs with more similar names, such as meet1.contoso.com and meet2.contoso.com.</span></span>

<span data-ttu-id="a2234-138">外部 web サービスは、境界ネットワークのリバースプロキシと連携して動作します。</span><span class="sxs-lookup"><span data-stu-id="a2234-138">The external web services works in conjunction with a reverse proxy in the perimeter network.</span></span> <span data-ttu-id="a2234-139">これらの web サービスを使用して、クライアントが外部アクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="a2234-139">It provides clients external access to by using these web services.</span></span> <span data-ttu-id="a2234-140">ここで構成された Fqdn は、ユーザーがログオンするときにクライアントに送信され、リモート接続時に HTTPS 接続をリバースプロキシに戻すために使用されます。</span><span class="sxs-lookup"><span data-stu-id="a2234-140">The FQDNs configured here are sent to clients when they log on, and are used to make an HTTPS connection back to the reverse proxy when connecting remotely.</span></span> <span data-ttu-id="a2234-141">リバースプロキシサーバーは、外部 web サービスの FQDN を内部のハードウェアロードバランサーに転送するか、直接プールに転送します。</span><span class="sxs-lookup"><span data-stu-id="a2234-141">The reverse-proxy server forwards the external web service FQDN to an internal hardware load balancer, or directly to the pool.</span></span> <span data-ttu-id="a2234-142">リバースプロキシは、内部 Web サーバーの IP アドレスに対して、外部 web サービスの FQDN を解決できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2234-142">The reverse proxy must be able to resolve the external web services FQDN to the IP address of the internal Web server.</span></span> <span data-ttu-id="a2234-143">外部 web サービスの FDQN、公開インターネットで解決できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2234-143">The external web services FDQN must be resolvable in the public Internet.</span></span>

<span data-ttu-id="a2234-144">内部サーバーが Standard Edition サーバーの場合、内部 FQDN は標準エディションのサーバー FQDN です。</span><span class="sxs-lookup"><span data-stu-id="a2234-144">If your internal server is a Standard Edition server, the internal FQDN is the Standard Edition server FQDN.</span></span> <span data-ttu-id="a2234-145">内部サーバーがフロントエンドプールの場合、FQDN は、内部の web ファームサーバーの負荷を分散するハードウェアロードバランサー仮想 IP (VIP) です。</span><span class="sxs-lookup"><span data-stu-id="a2234-145">If your internal server is a Front End pool, the FQDN is a hardware load balancer virtual IP (VIP) that load balances the internal web farm servers.</span></span> <span data-ttu-id="a2234-146">複数の Enterprise Edition サーバーがあるフロントエンドプールでは、ハードウェアロードバランサーが必要です。</span><span class="sxs-lookup"><span data-stu-id="a2234-146">A hardware load balancer is required in a Front End pool with more than one Enterprise Edition server.</span></span> <span data-ttu-id="a2234-147">Standard Edition サーバーまたは1つの Enterprise Edition フロントエンドサーバーでは、ロードバランサーは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="a2234-147">A load balancer is not required for a Standard Edition server or a single Enterprise Edition Front End Server.</span></span>

<span data-ttu-id="a2234-148"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a2234-148"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

