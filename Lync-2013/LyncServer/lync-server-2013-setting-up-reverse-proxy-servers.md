---
title: 'Lync Server 2013: リバース プロキシ サーバーの設定'
description: 'Lync Server 2013: リバースプロキシサーバーをセットアップします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up reverse proxy servers
ms:assetid: 00bc138a-243f-4389-bfa5-9c62fcc95132
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398069(v=OCS.15)
ms:contentKeyID: 48183225
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f8cd5842e4d735637406f6d0fa4f467f1cb8ed03
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399645"
---
# <a name="setting-up-reverse-proxy-servers-for-lync-server-2013"></a><span data-ttu-id="6a99c-103">Lync Server 2013 のリバース プロキシ サーバーの設定</span><span class="sxs-lookup"><span data-stu-id="6a99c-103">Setting up reverse proxy servers for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6a99c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6a99c-104">

<span> </span></span></span>

<span data-ttu-id="6a99c-105">_**最終更新日:** 2014-05-08_</span><span class="sxs-lookup"><span data-stu-id="6a99c-105">_**Topic Last Modified:** 2014-05-08_</span></span>

<span data-ttu-id="6a99c-106">Microsoft Lync Server 2013 Edge Server 展開の場合、外部クライアントがディレクターとユーザーのホームプール上の Lync Server 2013 Web サービス (Office Communications Server の *Web コンポーネント* と呼ばれます) にアクセスするには、境界ネットワーク内の HTTPS リバースプロキシが必要です。</span><span class="sxs-lookup"><span data-stu-id="6a99c-106">For Microsoft Lync Server 2013 Edge Server deployments, an HTTPS reverse proxy in the perimeter network is required for external clients to access the Lync Server 2013 Web Services (called *Web Components* in Office Communications Server) on the Director and the user’s home pool.</span></span> <span data-ttu-id="6a99c-107">リバースプロキシを介して外部アクセスを必要とする機能には、次のようなものがあります。</span><span class="sxs-lookup"><span data-stu-id="6a99c-107">Some of the features that require external access through a reverse proxy include the following:</span></span>

  - <span data-ttu-id="6a99c-108">外部ユーザーによる会議の会議コンテンツのダウンロードを有効にします。</span><span class="sxs-lookup"><span data-stu-id="6a99c-108">Enabling external users to download meeting content for your meetings.</span></span>

  - <span data-ttu-id="6a99c-109">外部ユーザーが配布グループを展開できるようにします。</span><span class="sxs-lookup"><span data-stu-id="6a99c-109">Enabling external users to expand distribution groups.</span></span>

  - <span data-ttu-id="6a99c-110">リモートユーザーがアドレス帳サービスからファイルをダウンロードできるようにします。</span><span class="sxs-lookup"><span data-stu-id="6a99c-110">Enabling remote users to download files from the Address Book service.</span></span>

  - <span data-ttu-id="6a99c-111">Lync Web App クライアントへのアクセス。</span><span class="sxs-lookup"><span data-stu-id="6a99c-111">Accessing the Lync Web App client.</span></span>

  - <span data-ttu-id="6a99c-112">ダイヤルイン会議の設定の web ページにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="6a99c-112">Accessing the Dial-in Conferencing Settings webpage.</span></span>

  - <span data-ttu-id="6a99c-113">デバイス更新 web サービスに接続して更新プログラムを取得するために、外部デバイスを有効にします。</span><span class="sxs-lookup"><span data-stu-id="6a99c-113">Enabling external devices to connect to Device Update web service and obtain updates.</span></span>

  - <span data-ttu-id="6a99c-114">モバイルアプリケーションを有効にして、インターネット上のモビリティー (Mcx) Url を自動的に検出して使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="6a99c-114">Enabling mobile applications to automatically discover and use the mobility (Mcx) URLs from the Internet.</span></span>

  - <span data-ttu-id="6a99c-115">Lync 2013 クライアント、Lync Windows ストアアプリ、Lync 2013 モバイルクライアントを有効にして、Lync Discover (自動検出) Url を検索し、ユニファイドコミュニケーションの Web API (UCWA) を使用します。</span><span class="sxs-lookup"><span data-stu-id="6a99c-115">Enabling the Lync 2013 client, Lync Windows Store app and Lync 2013 Mobile client to locate the Lync Discover (autodiscover) URLs and use Unified Communications Web API (UCWA).</span></span>

<span data-ttu-id="6a99c-116">すべてのプールのすべての Web サービスを公開するように HTTP リバースプロキシを構成することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="6a99c-116">We recommend that you configure your HTTP reverse proxy to publish all Web Services in all pools.</span></span> <span data-ttu-id="6a99c-117">公開 https://ExternalFQDN/ \* プールのすべての IIS 仮想ディレクトリを公開します。</span><span class="sxs-lookup"><span data-stu-id="6a99c-117">Publishing https:// ExternalFQDN/\* publishes all IIS virtual directories for a pool.</span></span> <span data-ttu-id="6a99c-118">組織内の標準エディションサーバー、フロントエンドプール、またはディレクターまたはディレクタープールごとに1つの公開ルールが必要です。</span><span class="sxs-lookup"><span data-stu-id="6a99c-118">You need one publishing rule for each Standard Edition server, Front End pool, or Director or Director pool in your organization.</span></span>

<span data-ttu-id="6a99c-119">さらに、単純な Url を公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6a99c-119">In addition, you need to publish the simple URLs.</span></span> <span data-ttu-id="6a99c-120">組織がディレクターまたはディレクタープールを使用している場合、HTTP リバースプロキシは、HTTP/HTTPS 要求をリッスンし、その Url をディレクターまたはディレクタープールの外部 Web サービスの仮想ディレクトリにプロキシします。</span><span class="sxs-lookup"><span data-stu-id="6a99c-120">If the organization has a Director or Director pool, the HTTP reverse proxy listens for HTTP/HTTPS requests to the simple URLs and proxies them to the external Web Services virtual directory on the Director or Director pool.</span></span> <span data-ttu-id="6a99c-121">ディレクターを展開していない場合は、単純な Url への要求を処理するために、1つのプールを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6a99c-121">If you have not deployed a Director, you need to designate one pool to handle requests to the simple URLs.</span></span> <span data-ttu-id="6a99c-122">(これがユーザーのホームプールではない場合は、ユーザーのホームプールの Web サービスにリダイレクトされます)。</span><span class="sxs-lookup"><span data-stu-id="6a99c-122">(If this is not the user’s home pool, it will redirect them onward to the Web Services on the user’s home pool).</span></span> <span data-ttu-id="6a99c-123">単純な Url は、専用の web 発行ルールによって処理することも、ディレクターの web 公開ルールのパブリック名に追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="6a99c-123">The simple URLs can be handled by a dedicated web publishing rule, or you can add it to the public names of the web publishing rule for the Director.</span></span> <span data-ttu-id="6a99c-124">また、外部自動検出サービス URL を公開する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="6a99c-124">You also need to publish the external Autodiscover Service URL.</span></span>

<span data-ttu-id="6a99c-125">Microsoft Forefront Threat Management Gateway 2010、Microsoft インターネットセキュリティとアクセラレータ (ISA) サーバー 2006 SP1、または Internet Information Server 7.0、7.5 または 8.0 (アプリケーション要求ルーティング (IIS) をリバースプロキシとして使うことができます。</span><span class="sxs-lookup"><span data-stu-id="6a99c-125">You can use Microsoft Forefront Threat Management Gateway 2010, Microsoft Internet Security and Acceleration (ISA) Server 2006 SP1, or Internet Information Server 7.0, 7.5 or 8.0 with Application Request Routing (IIS ARR) as a reverse proxy.</span></span> <span data-ttu-id="6a99c-126">このセクションの詳細な手順では、Forefront Threat Management Gateway 2010 を構成する方法と ISA Server 2006 を構成する手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="6a99c-126">The detailed steps in this section describe how to configure Forefront Threat Management Gateway 2010, and the steps for configuring ISA Server 2006 are almost identical.</span></span> <span data-ttu-id="6a99c-127">ガイダンスは、IIS の ARR にも提供されています。</span><span class="sxs-lookup"><span data-stu-id="6a99c-127">Guidance is also provided for IIS ARR.</span></span> <span data-ttu-id="6a99c-128">別のリバースプロキシを使用している場合は、その製品のドキュメントを参照して、ここで定義されている要件を、他のリバースプロキシの関連機能にマップします。</span><span class="sxs-lookup"><span data-stu-id="6a99c-128">If you are using a different reverse proxy, consult the documentation for that product and map the requirements defined here to the associated features in other reverse proxies.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="6a99c-129">インターネット Information Server アプリケーション要求ルーティング (IIS ARR) は、Lync Server 2010 および Lync Server 2013 のリバースプロキシを実装するための完全にテストされ、サポートされるオプションです。</span><span class="sxs-lookup"><span data-stu-id="6a99c-129">Internet Information Server Application Request Routing (IIS ARR) is a fully tested and supported option for implementing a reverse proxy for Lync Server 2010 and Lync Server 2013.</span></span> <span data-ttu-id="6a99c-130">2012年11月、Microsoft おの ForeFront Threat Management Gateway 2010、または TMG のライセンス販売。</span><span class="sxs-lookup"><span data-stu-id="6a99c-130">In November, 2012, Microsoft ceased license sales of ForeFront Threat Management Gateway 2010, or TMG.</span></span> <span data-ttu-id="6a99c-131">TMG は、完全にサポートされる製品であり、サードパーティによって販売されているアプライアンスで販売することもできます。</span><span class="sxs-lookup"><span data-stu-id="6a99c-131">TMG is still a fully supported product, and is still available for sale on appliances sold by third parties.</span></span> <span data-ttu-id="6a99c-132">また、多くのサードパーティ製ハードウェアロードバランサーおよびファイアウォールでは、リバースプロキシのサポートが提供されています。</span><span class="sxs-lookup"><span data-stu-id="6a99c-132">Also, many third party hardware load balancers and firewalls provide reverse proxy support.</span></span> <span data-ttu-id="6a99c-133">ハードウェアロードバランサーとリバースプロキシ機能を提供するファイアウォールについては、「Lync Server のリバースプロキシサポートを提供するためにその製品を構成する方法については、ベンダーに確認する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6a99c-133">For hardware load balancers and firewalls that provide reverse proxy features, check with your vendor for specific instructions on how to configure their product to provide reverse proxy support for Lync Server.</span></span> <span data-ttu-id="6a99c-134">お客様の製品のドキュメントを Microsoft に送信している第三者を表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="6a99c-134">You can also view third parties that have submitted documentation for their product to Microsoft.</span></span> <span data-ttu-id="6a99c-135">サポートは、お客様のソリューションのサードパーティによって提供されます。</span><span class="sxs-lookup"><span data-stu-id="6a99c-135">Support is provided by the third party for their solution.</span></span> <span data-ttu-id="6a99c-136">ソリューションの提供でアクティブなサードパーティを確認するには、「 <A href="https://go.microsoft.com/fwlink/?linkid=268730">Microsoft Lync 用のインフラストラクチャ認定</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6a99c-136">To see third parties that are active in providing solutions, see <A href="https://go.microsoft.com/fwlink/?linkid=268730">Infrastructure qualified for Microsoft Lync</A>.</span></span>



</div>

<span data-ttu-id="6a99c-137">次のトピックと手順では、展開と構成手順のベースとして Forefront Threat Management Gateway 2010 と IIS ARR を使用します。</span><span class="sxs-lookup"><span data-stu-id="6a99c-137">The following topics and procedures use Forefront Threat Management Gateway 2010 and IIS ARR as the basis for the deployment and configuration procedures.</span></span>

  - [<span data-ttu-id="6a99c-138">Lync Server 2013 向けの Web ファームの FQDN の構成</span><span class="sxs-lookup"><span data-stu-id="6a99c-138">Configure web farm FQDNs for Lync Server 2013</span></span>](lync-server-2013-configure-web-farm-fqdns.md)

  - [<span data-ttu-id="6a99c-139">Lync Server 2013 ネットワーク アダプターの構成</span><span class="sxs-lookup"><span data-stu-id="6a99c-139">Configure network adapters in Lync Server 2013</span></span>](lync-server-2013-configure-network-adapters.md)

  - [<span data-ttu-id="6a99c-140">Lync Server 2013 でのリバース HTTP プロキシ用の証明書の要求と構成</span><span class="sxs-lookup"><span data-stu-id="6a99c-140">Request and configure a certificate for your reverse HTTP proxy in Lync Server 2013</span></span>](lync-server-2013-request-and-configure-a-certificate-for-your-reverse-http-proxy.md)

  - [<span data-ttu-id="6a99c-141">Lync Server 2013 での単一内部プールの Web 公開ルールの構成</span><span class="sxs-lookup"><span data-stu-id="6a99c-141">Configure web publishing rules for a single internal pool in Lync Server 2013</span></span>](lync-server-2013-configure-web-publishing-rules-for-a-single-internal-pool.md)

  - [<span data-ttu-id="6a99c-142">Lync Server 2013 で IIS 仮想ディレクトリの認証と証明書を検証または構成する</span><span class="sxs-lookup"><span data-stu-id="6a99c-142">Verify or configure authentication and certification on IIS virtual directories in Lync Server 2013</span></span>](lync-server-2013-verify-or-configure-authentication-and-certification-on-iis-virtual-directories.md)

  - [<span data-ttu-id="6a99c-143">Lync Server 2013 でのリバース プロキシ サーバーの DNS レコードの作成</span><span class="sxs-lookup"><span data-stu-id="6a99c-143">Create DNS records for reverse proxy servers in Lync Server 2013</span></span>](lync-server-2013-create-dns-records-for-reverse-proxy-servers.md)

  - [<span data-ttu-id="6a99c-144">Lync Server 2013 でリバース プロキシ経由のアクセスを確認する</span><span class="sxs-lookup"><span data-stu-id="6a99c-144">Verify access through your reverse proxy in Lync Server 2013</span></span>](lync-server-2013-verify-access-through-your-reverse-proxy.md)

<div>

## <a name="before-you-begin"></a><span data-ttu-id="6a99c-145">始める前に</span><span class="sxs-lookup"><span data-stu-id="6a99c-145">Before You Begin</span></span>

<span data-ttu-id="6a99c-146">リバースプロキシとして Forefront Threat Management Gateway 2010 を正常に展開するには、Forefront Threat Management Gateway 2010 ドキュメントで定義されている前提条件とハードウェア要件を使用してサーバーをセットアップして構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6a99c-146">To successfully deploy Forefront Threat Management Gateway 2010 as your reverse proxy, you need to setup and configure a server, using the prerequisites and hardware requirements defined in the Forefront Threat Management Gateway 2010 documentation.</span></span> <span data-ttu-id="6a99c-147">続行する前に、次のトピック「ハードウェアを適切に構成し、Forefront Threat Management Gateway 2010 をサーバーにインストールする」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6a99c-147">See the following topic set to properly configure the hardware and to install Forefront Threat Management Gateway 2010 on the server before proceeding.</span></span>

  - <span></span>  
    [<span data-ttu-id="6a99c-148">Forefront Threat Management Gateway (TMG) 2010</span><span class="sxs-lookup"><span data-stu-id="6a99c-148">Forefront Threat Management Gateway (TMG) 2010</span></span>](https://go.microsoft.com/fwlink/?linkid=291292)

  - <span></span>  
    [<span data-ttu-id="6a99c-149">Forefront TMG 2010 ハードウェア推奨事項</span><span class="sxs-lookup"><span data-stu-id="6a99c-149">Forefront TMG 2010 hardware recommendations</span></span>](https://go.microsoft.com/fwlink/?linkid=291293)

<span data-ttu-id="6a99c-150">IIS ARR をリバースプロキシとして正常に展開するには、次のトピックを参照して、ハードウェアおよび必要なソフトウェアを構成します。</span><span class="sxs-lookup"><span data-stu-id="6a99c-150">To successfully deploy IIS ARR as your reverse proxy, review the following topics to configure the hardware and the prerequisite software.</span></span>

  - <span></span>  
    <span data-ttu-id="6a99c-151">Windows Server 2008 または Windows Server 2008 R2 に IIS をインストールする方法については、「 [Windows server 2008 または Windows server 2008 r2 で iis 7 をインストール](https://go.microsoft.com/fwlink/?linkid=291296)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6a99c-151">To install IIS on Windows Server 2008 or Windows Server 2008 R2, see [Installing IIS 7 on Windows Server 2008 or Windows Server 2008 R2](https://go.microsoft.com/fwlink/?linkid=291296)</span></span>

  - <span></span>  
    <span data-ttu-id="6a99c-152">Windows Server 2012 に IIS をインストールする方法については、「 [Windows server 2012 で iis 8](https://go.microsoft.com/fwlink/?linkid=291297)をインストールする」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6a99c-152">To install IIS on Windows Server 2012, see [Installing IIS 8 on Windows Server 2012](https://go.microsoft.com/fwlink/?linkid=291297)</span></span>

  - <span></span>  
    <span data-ttu-id="6a99c-153">Windows Server 2012 R2 に IIS をインストールする方法については、「 [Windows server 2012 r2 で iis 8.5](https://go.microsoft.com/fwlink/?linkid=330687)をインストールする」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6a99c-153">To install IIS on Windows Server 2012 R2, see [Installing IIS 8.5 on Windows Server 2012 R2](https://go.microsoft.com/fwlink/?linkid=330687)</span></span>

  - <span></span>  
    <span data-ttu-id="6a99c-154">IIS のアプリケーション要求ルーティング拡張機能をダウンロードするには、「[アプリケーション要求ルーティング v 2.5 のダウンロード](https://go.microsoft.com/fwlink/?linkid=291298)」の指示に従ってください。</span><span class="sxs-lookup"><span data-stu-id="6a99c-154">To download the Application Request Routing extension for IIS, follow the instructions at [Application Request Routing v2.5 Download](https://go.microsoft.com/fwlink/?linkid=291298)</span></span>

  - <span></span>  
    <span data-ttu-id="6a99c-155">[アプリケーション要求ルーティングバージョン2のインストール](https://go.microsoft.com/fwlink/?linkid=291299)の手順については、ARR をインストールする</span><span class="sxs-lookup"><span data-stu-id="6a99c-155">To install ARR, for the instructions at [Install Application Request Routing Version 2](https://go.microsoft.com/fwlink/?linkid=291299)</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="6a99c-156">現在投稿されている命令は、ARR 2.0 に対応しています。</span><span class="sxs-lookup"><span data-stu-id="6a99c-156">The instructions currently posted are for ARR 2.0.</span></span> <span data-ttu-id="6a99c-157">拡張機能のインストールでは、2つのバージョンの違いはありません。</span><span class="sxs-lookup"><span data-stu-id="6a99c-157">For installation of the extension, there is no difference between the two versions.</span></span>

    
    <span data-ttu-id="6a99c-158"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6a99c-158"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

