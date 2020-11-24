---
title: 'Lync Server 2013: リバース プロキシのシナリオ'
description: 'Lync Server 2013: リバースプロキシのシナリオ'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Scenarios for reverse proxy
ms:assetid: 13108f59-a660-4ff1-8404-079d1cb646f2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204691(v=OCS.15)
ms:contentKeyID: 48183468
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cb714182fd13e42c6295e26ffd1edbb8b6041866
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398450"
---
# <a name="scenarios-for-reverse-proxy-in-lync-server-2013"></a><span data-ttu-id="8f19d-103">Lync Server 2013 のリバース プロキシのシナリオ</span><span class="sxs-lookup"><span data-stu-id="8f19d-103">Scenarios for reverse proxy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8f19d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8f19d-104">

<span> </span></span></span>

<span data-ttu-id="8f19d-105">_**最終更新日:** 2013-01-21_</span><span class="sxs-lookup"><span data-stu-id="8f19d-105">_**Topic Last Modified:** 2013-01-21_</span></span>

<span data-ttu-id="8f19d-106">会議とダイヤルインのシンプルな Url、アドレス帳、会議コンテンツ、配布リストの展開、モビリティサービスなどのサービスとリソースへのアクセスを提供するために、Lync Server 2013 で逆プロキシを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f19d-106">Reverse proxies are required in Lync Server 2013 for providing access to services and resources such as the meeting and dial-in Simple URLs, address book, meeting content, distribution list expansion, mobility services, and others.</span></span> <span data-ttu-id="8f19d-107">Lync Server 2013 の一般的なリバースプロキシシナリオでは、外部クライアント (デスクトップクライアントや Lync Web App クライアントなど) がディレクターまたはフロントエンドサーバーの外部 Web サービスにアクセスすることを許可します。</span><span class="sxs-lookup"><span data-stu-id="8f19d-107">The typical reverse proxy scenario in Lync Server 2013 is to allow external clients (for example, the desktop client or Lync Web App client) access to the Director or Front End Server external Web Services.</span></span>

<span data-ttu-id="8f19d-108">**リバースプロキシと外部 web サービス**</span><span class="sxs-lookup"><span data-stu-id="8f19d-108">**Reverse proxy and external web services**</span></span>

<span data-ttu-id="8f19d-109">![13142405-d5c9-45b7-a8b7-a8c89f09c97c](images/JJ204932.13142405-d5c9-45b7-a8b7-a8c89f09c97c(OCS.15).jpg "13142405-d5c9-45b7-a8b7-a8c89f09c97c")</span><span class="sxs-lookup"><span data-stu-id="8f19d-109">![13142405-d5c9-45b7-a8b7-a8c89f09c97c](images/JJ204932.13142405-d5c9-45b7-a8b7-a8c89f09c97c(OCS.15).jpg "13142405-d5c9-45b7-a8b7-a8c89f09c97c")</span></span>

<span data-ttu-id="8f19d-110">計画フェーズでは、Lync Server 2013 展開でのリバースプロキシの要件を定義します。</span><span class="sxs-lookup"><span data-stu-id="8f19d-110">During the planning phase, you define the requirements for the reverse proxy in a Lync Server 2013 deployment.</span></span> <span data-ttu-id="8f19d-111">リバースプロキシは、次の外部クライアントの機能にアクセスできるようにします。</span><span class="sxs-lookup"><span data-stu-id="8f19d-111">The reverse proxy enables access to features for the following external clients:</span></span>

  - <span data-ttu-id="8f19d-112">Microsoft Lync 2013 デスクトップクライアント</span><span class="sxs-lookup"><span data-stu-id="8f19d-112">Microsoft Lync 2013 desktop client</span></span>

  - <span data-ttu-id="8f19d-113">Microsoft Lync Web App</span><span class="sxs-lookup"><span data-stu-id="8f19d-113">Microsoft Lync Web App</span></span>

  - <span data-ttu-id="8f19d-114">Microsoft Lync Mobile</span><span class="sxs-lookup"><span data-stu-id="8f19d-114">Microsoft Lync Mobile</span></span>

  - <span data-ttu-id="8f19d-115">Lync Windows ストア アプリ</span><span class="sxs-lookup"><span data-stu-id="8f19d-115">Lync Windows Store app</span></span>

<span data-ttu-id="8f19d-116">Lync Server 2013 の展開を計画する場合は、Lync Server 2013 の実際の要件をリバースプロキシ機能にマップします。</span><span class="sxs-lookup"><span data-stu-id="8f19d-116">When planning your Lync Server 2013 deployment, you map the actual requirements for Lync Server 2013 to the reverse proxy features.</span></span>

1.  <span data-ttu-id="8f19d-117">外部クライアントは、ポート TCP 443 上のリバースプロキシに接続し、セキュアソケットレイヤー (SSL) またはトランスポートレイヤーセキュリティ (TLS) を使用します。</span><span class="sxs-lookup"><span data-stu-id="8f19d-117">External clients will connect to the reverse proxy on port TCP 443 and will use secure socket layer (SSL) or transport layer security (TLS).</span></span> <span data-ttu-id="8f19d-118">Microsoft Lync モバイルクライアントは、ポート TCP 80 に接続できますが、Lync discover サービスへの最初の接続を実行しているときにのみ、管理者が適切なドメインネームシステム (DNS) CNAME (または alias) レコードを設定しており、この通信が暗号化されていないことを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="8f19d-118">Microsoft Lync Mobile clients can connect on port TCP 80, but only when performing the initial connection to the Lync discover services and the administrator has configured the proper domain name system (DNS) CNAME (or alias) records, and accepts that this communication will not be encrypted.</span></span>

2.  <span data-ttu-id="8f19d-119">Lync Server 2013 の外部 web サービス (フロントエンドサーバーまたはディレクターに展開) では、ポート TCP 4443 上のリバースプロキシとの接続を想定しており、接続が SSL/TLS であると想定しています。</span><span class="sxs-lookup"><span data-stu-id="8f19d-119">Lync Server 2013 external web services (deployed on the Front End Server and/or the Director) expect a connection from a reverse proxy on port TCP 4443, and it expects that the connection will be SSL/TLS.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="8f19d-120">外部 web サービスの既定のリスニングポートとして、HTTP トラフィックの場合は TCP 8080、HTTPS トラフィックの場合は TCP 4443 が推奨されます。</span><span class="sxs-lookup"><span data-stu-id="8f19d-120">The suggested default listening ports for the external web services are TCP 8080 for HTTP traffic, and TCP 4443 for HTTPS traffic.</span></span> <span data-ttu-id="8f19d-121">トポロジビルダーでは、既定値を上書きして、外部 web サービスの独自のリッスンポートを定義できます。</span><span class="sxs-lookup"><span data-stu-id="8f19d-121">Topology Builder provides an opportunity to override the defaults and define your own listening ports for the external web services.</span></span> <span data-ttu-id="8f19d-122">逆プロキシは外部の web サービスと通信し、外部クライアントはリバースプロキシと通信することに注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f19d-122">It’s important to note that the reverse proxy communicates with the external web services, and the external clients communicate with the reverse proxy.</span></span> <span data-ttu-id="8f19d-123">外部クライアントは、ポート TCP 443 上のリバースプロキシと通信しますが、リバースプロキシがの外部 web サービスと通信するポートを再定義することができます。</span><span class="sxs-lookup"><span data-stu-id="8f19d-123">The external client communicates with the reverse proxy on port TCP 443, but you can redefine what port the reverse proxy communicates with the external web services on.</span></span> <span data-ttu-id="8f19d-124">トポロジビルダーのオプションを使用して、web サービスの既定のリスニングポートを上書きすると、インフラストラクチャで発生する可能性があるリッスンポートの競合を解決することができます。</span><span class="sxs-lookup"><span data-stu-id="8f19d-124">The options in Topology Builder to override the default listening ports for the web services allows you to resolve listening port conflicts that may arise in your infrastructure.</span></span>

    
    </div>

3.  <span data-ttu-id="8f19d-125">Lync Server 2013 の外部 web サービスは、クライアントが使用しようとしているサービスおよび web サーバーディレクトリを特定するために、クライアントから変更されていないホストヘッダーを要求します。</span><span class="sxs-lookup"><span data-stu-id="8f19d-125">Lync Server 2013 external web services expect an unmodified Host Header from the client to identify what service and web server directory the client is attempting to use.</span></span> <span data-ttu-id="8f19d-126">要求はリバースプロキシから送信された場合と同じように表示される</span><span class="sxs-lookup"><span data-stu-id="8f19d-126">Requests should appear as if they came from the reverse proxy</span></span>

4.  <span data-ttu-id="8f19d-127">外部 web サービスでは、定義済みの web サーバー仮想ディレクトリ (vDir) を使って、クライアントに提供されるサービスを提供します。</span><span class="sxs-lookup"><span data-stu-id="8f19d-127">The external web services use defined web server virtual directories (vDir) that provide the services offered to clients.</span></span> <span data-ttu-id="8f19d-128">特定の外部特定の web サービス:</span><span class="sxs-lookup"><span data-stu-id="8f19d-128">Specific externally identifiable web services are:</span></span>
    
      - <span data-ttu-id="8f19d-129">Web 会議の「会議」</span><span class="sxs-lookup"><span data-stu-id="8f19d-129">The “Meet” vDir for web conference meetings</span></span>
    
      - <span data-ttu-id="8f19d-130">電話へのアクセスと電話会議の「ダイヤルイン」の vDir</span><span class="sxs-lookup"><span data-stu-id="8f19d-130">The “Dialin” vDir for phone access and phone conferencing</span></span>
    
      - <span data-ttu-id="8f19d-131">Lync Windows ストアアプリ、Lync Mobile、デスクトップクライアント Lync 2013 用の "自動検出" の vDir。</span><span class="sxs-lookup"><span data-stu-id="8f19d-131">The “Autodiscover” vDir for Lync Windows Store app, Lync Mobile, and the desktop client Lync 2013.</span></span> <span data-ttu-id="8f19d-132">Lync Server 2013 での自動検出は、DNS 名 "lyncdiscover" によって認識されます。</span><span class="sxs-lookup"><span data-stu-id="8f19d-132">Autodiscover in Lync Server 2013 is known by the DNS name “lyncdiscover”</span></span>
    
      - <span data-ttu-id="8f19d-133">定義されていないサービスは、外部の web サービスに直接通話を発信することによって、外部クライアントによってアクセスされます。</span><span class="sxs-lookup"><span data-stu-id="8f19d-133">Services not defined are accessed by the external client by direct calls to the external web services.</span></span> <span data-ttu-id="8f19d-134">たとえば、配布グループの展開 (DLX) とアドレス帳サービス (ABS) は、外部の web サービスと関連する vDirs に直接通話を発信することによってアクセスされます。</span><span class="sxs-lookup"><span data-stu-id="8f19d-134">For example, distribution group expansion (DLX) and the address book service (ABS) are accessed by direct calls to the external web services and associated vDirs.</span></span> <span data-ttu-id="8f19d-135">クライアントは、vDir への実際のパスを認識し、この情報に基づいて uniform レコードロケーター (URL) を構築します。</span><span class="sxs-lookup"><span data-stu-id="8f19d-135">The client knows the actual path to the vDir and constructs a uniform record locator (URL) based on this information.</span></span> <span data-ttu-id="8f19d-136">クライアントは、のような URL を使ってアドレス帳サービスにアクセスします。 `https://externalweb.contoso.com/abs/handler`</span><span class="sxs-lookup"><span data-stu-id="8f19d-136">The client would access the address book service using a URL similar to `https://externalweb.contoso.com/abs/handler`</span></span>
    
      - <span data-ttu-id="8f19d-137">会議が Lync Server トポロジの一部として定義および構成されている場合の Office Web Apps サーバー</span><span class="sxs-lookup"><span data-stu-id="8f19d-137">The Office Web Apps Server when conferencing is defined and configured as part of the Lync Server topology</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="8f19d-138">Office Web Apps サーバーは独立した役割サーバーであり、外部 Web サービスの一部としては構成されていません。</span><span class="sxs-lookup"><span data-stu-id="8f19d-138">The Office Web Apps Server is a separate role server and is not configured as part of the external web services.</span></span> <span data-ttu-id="8f19d-139">このサーバーは、クライアントアクセス用に個別に公開されます。</span><span class="sxs-lookup"><span data-stu-id="8f19d-139">This server is separately published for client access.</span></span>

        
        </div>

5.  <span data-ttu-id="8f19d-140">各サービスの SSL ブリッジングを定義します。</span><span class="sxs-lookup"><span data-stu-id="8f19d-140">Define SSL bridging for each service.</span></span> <span data-ttu-id="8f19d-141">外部ポートの TCP 443 は、TCP 4443 の外部 web サービスポートにマッピングされます。</span><span class="sxs-lookup"><span data-stu-id="8f19d-141">The external port TCP 443 is mapped to the external web services port of TCP 4443.</span></span> <span data-ttu-id="8f19d-142">暗号化されていない HTTP の場合、ポート TCP 80 は外部 web サービスポート TCP 8080 にマッピングされます。</span><span class="sxs-lookup"><span data-stu-id="8f19d-142">For unencrypted HTTP, port TCP 80 is mapped to the external web services port TCP 8080</span></span>

6.  <span data-ttu-id="8f19d-143">Web サーバーリソースを公開するためのリバースプロキシリスナーを計画する</span><span class="sxs-lookup"><span data-stu-id="8f19d-143">Plan for reverse proxy listeners to publish web server resources</span></span>

7.  <span data-ttu-id="8f19d-144">提供されるサービスに基づいて、リバースプロキシ用の証明書を要求して構成します。</span><span class="sxs-lookup"><span data-stu-id="8f19d-144">Request and configure the certificate for the reverse proxy based on the services that will be offered.</span></span> <span data-ttu-id="8f19d-145">正しいサブジェクト代替名で構成されている場合、この証明書はリバースプロキシサーバー上で構成されたすべてのリスナーで共有できます。</span><span class="sxs-lookup"><span data-stu-id="8f19d-145">If configured with the correct subject alternative names, this certificate can be shared by all configured listeners on the reverse proxy server</span></span>

<span data-ttu-id="8f19d-146">リバースプロキシの展開を計画するために利用可能なリソース:</span><span class="sxs-lookup"><span data-stu-id="8f19d-146">Resources available for planning your reverse proxy deployment:</span></span>

  - [<span data-ttu-id="8f19d-147">Lync Server 2013 のデータの収集</span><span class="sxs-lookup"><span data-stu-id="8f19d-147">Data collection in Lync Server 2013</span></span>](lync-server-2013-data-collection.md)

  - [<span data-ttu-id="8f19d-148">証明書の概要 - Lync Server 2013 リバース プロキシ</span><span class="sxs-lookup"><span data-stu-id="8f19d-148">Certificate summary - Reverse proxy in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-reverse-proxy.md)

  - [<span data-ttu-id="8f19d-149">ポートの概要 - Lync Server 2013 のリバース プロキシ</span><span class="sxs-lookup"><span data-stu-id="8f19d-149">Port summary - Reverse proxy in Lync Server 2013</span></span>](lync-server-2013-port-summary-reverse-proxy.md)

  - [<span data-ttu-id="8f19d-150">DNS の概要 - Lync Server 2013 でのリバース プロキシ</span><span class="sxs-lookup"><span data-stu-id="8f19d-150">DNS summary - Reverse proxy in Lync Server 2013</span></span>](lync-server-2013-dns-summary-reverse-proxy.md)

<span data-ttu-id="8f19d-151"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8f19d-151"></div>

<span> </span>

</div>

</div>

</span></span></div>

