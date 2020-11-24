---
title: 'Lync Server 2013: 自動検出について'
description: 'Lync Server 2013: 自動検出について説明します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Understanding Autodiscover
ms:assetid: d70a15b7-750b-4e0f-9a7f-0254d6d486c3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945654(v=OCS.15)
ms:contentKeyID: 51541522
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 295aba4bffbe5d17070702203cfd933284cb12c0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399494"
---
# <a name="understanding-autodiscover-in-lync-server-2013"></a><span data-ttu-id="0fc31-103">Lync Server 2013 での自動検出について</span><span class="sxs-lookup"><span data-stu-id="0fc31-103">Understanding Autodiscover in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0fc31-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0fc31-104">

<span> </span></span></span>

<span data-ttu-id="0fc31-105">_**最終更新日:** 2013-06-03_</span><span class="sxs-lookup"><span data-stu-id="0fc31-105">_**Topic Last Modified:** 2013-06-03_</span></span>

<span data-ttu-id="0fc31-106">Lync Server 2013 自動検出サービスは、最初に Microsoft Lync server 2010 で導入された機能です。 Lync Server 2010: 2011 の累積的な更新プログラムの一部として使用されています。</span><span class="sxs-lookup"><span data-stu-id="0fc31-106">The Lync Server 2013 Autodiscover Service is a feature that was originally introduced in Microsoft Lync Server 2010 as part of the Cumulative Update for Lync Server 2010: November 2011.</span></span> <span data-ttu-id="0fc31-107">この累積的な更新プログラムでは、修正に加えて、Lync Mobile および Lync 2013 クライアントのサポートが提供されています。</span><span class="sxs-lookup"><span data-stu-id="0fc31-107">In addition to fixes, this cumulative update delivered support for Lync Mobile and Lync 2013 clients.</span></span>

<span data-ttu-id="0fc31-108">Lync Server 2013 では、自動検出サービスは、外部および内部のモバイルクライアントの操作の重要な部分であり、自動検出も Windows 8 向けの最近導入された Lync Windows ストアアプリなどの新しいクライアントにも拡張されています。</span><span class="sxs-lookup"><span data-stu-id="0fc31-108">In Lync Server 2013, the Autodiscover Service is an integral part of the operation of external and internal mobile clients, and Autodiscover is also extended to new clients, such as the recently introduced Lync Windows Store app for Windows 8.</span></span> <span data-ttu-id="0fc31-109">自動検出は、Lync 2013 デスクトップクライアントでも使用されます。</span><span class="sxs-lookup"><span data-stu-id="0fc31-109">Autodiscover is also used by the Lync 2013 desktop clients.</span></span> <span data-ttu-id="0fc31-110">自動検出は、Lync Server では、必要なドメインネームシステム (DNS) レコード lyncdiscover によって認識され **ます。 \<domain\>**</span><span class="sxs-lookup"><span data-stu-id="0fc31-110">Autodiscover is recognized in Lync Server by the required domain name system (DNS) records **lyncdiscover.\<domain\>**</span></span> <span data-ttu-id="0fc31-111">**lyncdiscoverinternal \<domain\>**</span><span class="sxs-lookup"><span data-stu-id="0fc31-111">and **lyncdiscoverinternal.\<domain\>**.</span></span> <span data-ttu-id="0fc31-112">さらに、新しいバージョンの Lync 2010 および Lync 2013 デスクトップクライアントでは、lyncdiscover の場合にのみ DNS SRV レコードを使用して、ドメインネームシステム (DNS) SRV レコードを自動検出します。\<domain\></span><span class="sxs-lookup"><span data-stu-id="0fc31-112">Additionally, newer versions of the Lync 2010 and Lync 2013 desktop client prefer Autodiscover over the domain name system (DNS) SRV records, using DNS SRV records only if lyncdiscover.\<domain\></span></span> <span data-ttu-id="0fc31-113">または lyncdiscoverinternal。\<domain\></span><span class="sxs-lookup"><span data-stu-id="0fc31-113">or lyncdiscoverinternal.\<domain\></span></span> <span data-ttu-id="0fc31-114">応答しないか、解決しません。</span><span class="sxs-lookup"><span data-stu-id="0fc31-114">does not respond or does not resolve.</span></span> <span data-ttu-id="0fc31-115">Windows 8 および Lync Mobile 用の Lync Windows ストアアプリでは、自動検出のみが使用され、従来の DNS SRV レコードは参照されません。</span><span class="sxs-lookup"><span data-stu-id="0fc31-115">The Lync Windows Store app for Windows 8 and Lync Mobile uses Autodiscover exclusively and will not refer to the traditional DNS SRV records.</span></span>

<span data-ttu-id="0fc31-116">Lync Server 2013 では、自動検出が拡張され、クライアントに対して、どの要素、機能、通信方法がクライアントから利用可能であるかが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0fc31-116">In Lync Server 2013, Autodiscover is expanded to communicate to the client which elements, features, and communication methods are available to the client.</span></span> <span data-ttu-id="0fc31-117">情報は、クライアントから送信された要求によって伝達され、Lync Server web サービスは、クライアントで利用可能な機能と、自動検出応答ドキュメントの形式でそれらの機能に連絡する方法について明確に定義された応答を返します。</span><span class="sxs-lookup"><span data-stu-id="0fc31-117">The information is communicated through a request that is sent from the client, and the Lync Server web services responds with a clearly defined response that names what is available to the client, and how to contact those features in the format of the Autodiscover Response document.</span></span>

<span data-ttu-id="0fc31-118">このドキュメントを通じて web サービスがクライアントに機能をどのようにやり取りするかなど、自動検出応答ドキュメントを理解する最良の方法は、Lync web サービス自動検出応答ドキュメントからの一般的な応答で各行を dissect して定義することです。</span><span class="sxs-lookup"><span data-stu-id="0fc31-118">The best way to understand the Autodiscover response document, including how the web services communicate features to clients through this document, is to dissect and define each line in a typical response from the Lync web service Autodiscover response document.</span></span>

<div class="">


> [!NOTE]  
> <span data-ttu-id="0fc31-119">この後の詳細では、ユーザーは認証要求に応答して、既にホームサーバーに対して認証されています。</span><span class="sxs-lookup"><span data-stu-id="0fc31-119">In the details that follow, the user has already authenticated to the home server by responding to an authentication request.</span></span>



</div>

<div class="">


> [!NOTE]  
> <span data-ttu-id="0fc31-120">Lync 自動検出 Web サービスは、microsoft <STRONG>Developer Network</STRONG> (MSDN) ライブラリの [<STRONG>定義を開く</STRONG>] セクションの<STRONG>microsoft Office プロトコル</STRONG>で定義されます。</span><span class="sxs-lookup"><span data-stu-id="0fc31-120">The Lync Autodiscover Web Service is defined in the <STRONG>Microsoft Office Protocols</STRONG> in the <STRONG>Open Specifications</STRONG> section of the <STRONG>Microsoft Developer Network</STRONG> (MSDN) library.</span></span> <span data-ttu-id="0fc31-121">詳細については、「Lync の自動検出 Web サービスプロトコル」を参照してください <A href="https://go.microsoft.com/fwlink/?linkid=273839">https://go.microsoft.com/fwlink/?LinkId=273839</A> 。</span><span class="sxs-lookup"><span data-stu-id="0fc31-121">For details, see the full specification document, "Lync Autodiscover Web Service Protocol," at: <A href="https://go.microsoft.com/fwlink/?linkid=273839">https://go.microsoft.com/fwlink/?LinkId=273839</A>.</span></span> <span data-ttu-id="0fc31-122">認証の詳細については、「」の「OC Authentication Web Service Protocol」を参照してください <A href="https://go.microsoft.com/fwlink/?linkid=279015">https://go.microsoft.com/fwlink/?LinkId=279015</A> 。</span><span class="sxs-lookup"><span data-stu-id="0fc31-122">For details about authentication, see "OC Authentication Web Service Protocol" at <A href="https://go.microsoft.com/fwlink/?linkid=279015">https://go.microsoft.com/fwlink/?LinkId=279015</A>.</span></span>



</div>

<div>

## <a name="the-lync-server-web-service-autodiscover-response"></a><span data-ttu-id="0fc31-123">Lync Server Web サービスの自動検出の応答</span><span class="sxs-lookup"><span data-stu-id="0fc31-123">The Lync Server Web Service Autodiscover Response</span></span>

<span data-ttu-id="0fc31-124">自動検出要求が送信されたときに返される応答は、内部または外部クライアントに対して同じです。</span><span class="sxs-lookup"><span data-stu-id="0fc31-124">The response returned when the Autodiscover request is sent is the same for an internal or an external client.</span></span> <span data-ttu-id="0fc31-125">場所によっては、一部のパラメーターが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="0fc31-125">Some parameters that are location–aware may change.</span></span> <span data-ttu-id="0fc31-126">クライアント要求を受信したが、実際のプールが、連絡されたもの以外の場合は、ユーザーのホームプールがそのユーザーに設定されます。</span><span class="sxs-lookup"><span data-stu-id="0fc31-126">If a client request is received, but the actual pool is other than the one that has been contacted, the user’s home pool will be set for that user.</span></span> <span data-ttu-id="0fc31-127">ユーザーアカウントが別のプールにあるが、同じ office からログインしている同僚は、若干異なる応答を得ることができます。</span><span class="sxs-lookup"><span data-stu-id="0fc31-127">A colleague whose user account is on a different pool, but logging in from the same office, would get a slightly different response.</span></span> <span data-ttu-id="0fc31-128">応答には、そのユーザーの正しいフロントエンドサーバーまたはフロントエンドプールが示されます。</span><span class="sxs-lookup"><span data-stu-id="0fc31-128">The response indicates the correct Front End Server or Front End pool for that user.</span></span>

<span data-ttu-id="0fc31-129">自動検出応答ドキュメントの例:</span><span class="sxs-lookup"><span data-stu-id="0fc31-129">An example of an Autodiscover Response document:</span></span>

    <AutodiscoverResponse xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" AccessLocation="External">
       <User>
          <SipServerInternalAccess fqdn="pool01.contoso.com" port="5061"/>
          <SipClientInternalAccess fqdn=" pool01.contoso.com" port="443"/>
          <SipServerExternalAccess fqdn="sip.contoso.com" port="5061"/>
          <SipClientExternalAccess fqdn="sip.contoso.com " port="443"/>
          <Link token ="External/Autodiscover" href="https://webexternal.contoso.com/Autodiscover/AutodiscoverService.svc/root"/>
          <Link token="Internal/Autodiscover" href="https://webinternal.contoso.net/Autodiscover/AutodiscoverService.svc/root"/>
          <Link token="External/AuthBroker" href="https://webexternal.contoso.com/Reach/sip.svc"/>
          <Link token="Internal/AuthBroker" href="https://webinternal.contoso.net/Reach/sip.svc"/>
          <Link token="External/WebScheduler" href="https://webexternal.contoso.com/Scheduler"/>
          <Link token="Internal/WebScheduler" href="https://webinternal.contoso.net/Scheduler"/>
          <Link token="External/Mcx" href="https://webexternal.contoso.com/Mcx/McxService.svc"/>
          <Link token="Internal/Mcx" href="https://webexternal.contoso.net/Mcx/McxService.svc"/>
          <Link token="External/Ucwa" href="https://webexternal.contoso.com/ucwa/v1/applications"/>
          <Link token="Internal/Ucwa" href="https://webinternal.contoso.net/ucwa/v1/applications"/>
          <Link token="Ucwa" href="https://webexternal.contoso.com/ucwa/v1/applications"/>
          <Link token="External/XFrame" href="https://webexternal.contoso.com/Autodiscover/XFrame/XFrame.html"/>
          <Link token="Internal/XFrame" href="https://webinternal.contoso.net/Autodiscover/XFrame/XFrame.html"/>
          <Link token="XFrame" href="https://webexternal.contoso.com/Autodiscover/XFrame/XFrame.html"/>
          <Link token="Self" href="https://webexternal.contoso.net/Autodiscover/AutodiscoverService.svc/root/user"/>
       </User>
    </AutodiscoverResponse>

<div>

## <a name="autodiscover-response-document-details"></a><span data-ttu-id="0fc31-130">自動検出応答ドキュメントの詳細</span><span class="sxs-lookup"><span data-stu-id="0fc31-130">Autodiscover Response Document Details</span></span>

<span data-ttu-id="0fc31-131">自動検出応答ドキュメントは、次の2つの形式のいずれかで指定できます。</span><span class="sxs-lookup"><span data-stu-id="0fc31-131">The Autodiscover Response document can be in one of two formats.</span></span> <span data-ttu-id="0fc31-132">既定の形式は、JavaScript オブジェクト表記 (JSON) です。</span><span class="sxs-lookup"><span data-stu-id="0fc31-132">The default format is a JavaScript Object Notation (JSON).</span></span> <span data-ttu-id="0fc31-133">その他の形式としては、拡張マークアップ言語 (XML) ドキュメントがあります。</span><span class="sxs-lookup"><span data-stu-id="0fc31-133">The other format is extensible markup language (XML) document.</span></span> <span data-ttu-id="0fc31-134">この例では XML が使用されます。</span><span class="sxs-lookup"><span data-stu-id="0fc31-134">The XML is used for this example.</span></span> <span data-ttu-id="0fc31-135">ドキュメントには、書式を決定する定義済みのスキーマが含まれているため、要求と応答は予測可能です。</span><span class="sxs-lookup"><span data-stu-id="0fc31-135">The request and response are predictable because the document has a defined schema that determines the format.</span></span> <span data-ttu-id="0fc31-136">使用しているスキーマを説明する文書内の行は、要求または応答の最初の行です。</span><span class="sxs-lookup"><span data-stu-id="0fc31-136">The line in the document that describes the schema used is the first line in the request or response:</span></span>

    <AutodiscoverResponse xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" AccessLocation="External">

<span data-ttu-id="0fc31-137">**Accesslocation = "external"** の定義では、要求が外部ユーザーから行われたことを示します。</span><span class="sxs-lookup"><span data-stu-id="0fc31-137">The definition of **AccessLocation=”External”** indicates that the request was made from an external user.</span></span>

    <SipServerInternalAccess fqdn="pool01.contoso.com" port="5061"/>

&nbsp;

    <SipServerExternalAccess fqdn="sip.contoso.com" port="5061"/>

<span data-ttu-id="0fc31-138">SipServerInternalAccess と SipServerExternalAccess は現在使用されていません。</span><span class="sxs-lookup"><span data-stu-id="0fc31-138">SipServerInternalAccess and SipServerExternalAccess are currently not used.</span></span> <span data-ttu-id="0fc31-139">これらのエントリは将来使用するために予約されています。</span><span class="sxs-lookup"><span data-stu-id="0fc31-139">These entries are reserved for future use.</span></span>

    <SipClientInternalAccess fqdn=" pool01.contoso.com" port="443"/>

&nbsp;

    <SipClientExternalAccess fqdn="sip.contoso.com " port="443"/>

<span data-ttu-id="0fc31-140">SipClientInternalAccess と SipClientExternalAccess は、内部または外部のクライアントが定義された SIP サーバーへのアクセスに使用する完全修飾ドメイン名とポートについて説明します。</span><span class="sxs-lookup"><span data-stu-id="0fc31-140">SipClientInternalAccess and SipClientExternalAccess describe the fully qualified domain name and port that an internal or external client will use to access the defined SIP Server.</span></span> <span data-ttu-id="0fc31-141">Lync デスクトップクライアントと Lync Windows ストアアプリでは、これらのエントリを場所 (内部または外部) に基づいて、ディレクターまたはフロントエンドサーバーを見つけるために使用します。</span><span class="sxs-lookup"><span data-stu-id="0fc31-141">The Lync desktop client and the Lync Windows Store app use these entries, based on their location (internal or external) to find the Director or Front End Server.</span></span>

    <Link token="Internal/Autodiscover" href="https://webinternal.contoso.net/Autodiscover/AutodiscoverService.svc/root"/>

&nbsp;

    <Link token ="External/Autodiscover" href="https://webexternal.contoso.com/Autodiscover/AutodiscoverService.svc/root"/>

<span data-ttu-id="0fc31-142">参照には、 `Autodiscover` 自動検出サービスのサービスエントリポイントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="0fc31-142">The `Autodiscover` references contain the service entry points for the Autodiscover service.</span></span> <span data-ttu-id="0fc31-143">Token 属性にはサービス名が含まれ、href は、サービスが検出されるクライアントに対して定義する URL です。</span><span class="sxs-lookup"><span data-stu-id="0fc31-143">The token attribute contains the name of the service, and the href is a URL that defines for the client where the service can be found.</span></span> <span data-ttu-id="0fc31-144">外部ネットワーク上のクライアントは、を使用し `External/Autodiscover` ます。</span><span class="sxs-lookup"><span data-stu-id="0fc31-144">Clients on an external network use the `External/Autodiscover`.</span></span> <span data-ttu-id="0fc31-145">自動検出サービスは展開プロセスの一部としてインストールされます。</span><span class="sxs-lookup"><span data-stu-id="0fc31-145">The Autodiscover service is installed as part of the deployment process.</span></span> <span data-ttu-id="0fc31-146">`Internal/Autodiscover` は現在使用されておらず、将来使用するために予約されています。</span><span class="sxs-lookup"><span data-stu-id="0fc31-146">`Internal/Autodiscover` is not currently used, and is reserved for future use.</span></span>

    <Link token="Internal/AuthBroker" href="https://webinternal.contoso.net/Reach/sip.svc"/>

&nbsp;

    <Link token="External/AuthBroker" href="https://webexternal.contoso.com/Reach/sip.svc"/>

<span data-ttu-id="0fc31-147">参照には、 `AuthBroker` 内部および外部認証ブローカーサービスのサービスエントリポイント (この場合は、sip-pstn) が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0fc31-147">The `AuthBroker` references contain the service entry points for the internal and the external authentication broker service, in this case, sip.svc.</span></span> <span data-ttu-id="0fc31-148">Token 属性にはサービス名が含まれ、href は、サービスが検出されるクライアントに対して定義する URL です。</span><span class="sxs-lookup"><span data-stu-id="0fc31-148">The token attribute contains the name of the service, and the href is a URL that defines for the client where the service can be found.</span></span> <span data-ttu-id="0fc31-149">使用している内部ネットワーク上のクライアント `Internal/AuthBroker` 。</span><span class="sxs-lookup"><span data-stu-id="0fc31-149">Clients on the internal network with use `Internal/AuthBroker`.</span></span> <span data-ttu-id="0fc31-150">外部ネットワーク上のクライアントは、を使用し `External/AuthBroker` ます。</span><span class="sxs-lookup"><span data-stu-id="0fc31-150">Clients on an external network use the `External/AuthBroker`.</span></span> <span data-ttu-id="0fc31-151">AuthBroker サービスは、内部の Lync Server 2013 展開 web サービスの展開プロセスの一部としてインストールされます。</span><span class="sxs-lookup"><span data-stu-id="0fc31-151">The AuthBroker service is installed as part of the deployment process of your internal Lync Server 2013 deployment web services.</span></span>

    <Link token="Internal/WebScheduler" href="https://webinternal.contoso.net/Scheduler"/>

&nbsp;

    <Link token="External/WebScheduler" href="https://webexternal.contoso.com/Scheduler"/>

<span data-ttu-id="0fc31-152">トークンは、 `WebScheduler` Lync Server 会議の web ベースのスケジュールに対するクライアントアクセスの url を参照します。</span><span class="sxs-lookup"><span data-stu-id="0fc31-152">The `WebScheduler` token references the URLs for client access to the web-based scheduling for Lync Server conferences.</span></span> <span data-ttu-id="0fc31-153">現時点では、 `External/WebScheduler` が使用されています。</span><span class="sxs-lookup"><span data-stu-id="0fc31-153">Currently, only the `External/WebScheduler` is used.</span></span> <span data-ttu-id="0fc31-154">WebScheduler は、内部の Lync Server 2013 展開 web サービスの展開プロセスの一部としてインストールされます。</span><span class="sxs-lookup"><span data-stu-id="0fc31-154">The WebScheduler is installed as part of the deployment process of your internal Lync Server 2013 deployment web services.</span></span>

    <Link token="Internal/Mcx" href="https://webexternal.contoso.net/Mcx/McxService.svc"/>

&nbsp;

    <Link token="External/Mcx" href="https://webexternal.contoso.com/Mcx/McxService.svc"/>

<span data-ttu-id="0fc31-155">`Internal/Mcx` および `External/Mcx` は、Lync Server 2010 用の累積更新プログラム (2011 年11月) で導入されたモビリティサービスの場所です。</span><span class="sxs-lookup"><span data-stu-id="0fc31-155">`Internal/Mcx` and `External/Mcx` are the locations of the Mobility services, introduced in Cumulative Update for Lync Server 2010: November 2011.</span></span> <span data-ttu-id="0fc31-156">これらの参照は、サポートされているすべてのデバイスで Lync 2010 Mobile によって引き続き使用されます。</span><span class="sxs-lookup"><span data-stu-id="0fc31-156">These references will continue to be used by Lync 2010 Mobile on all supported devices.</span></span> <span data-ttu-id="0fc31-157">Mcx サービスは、内部の Lync Server 2013 展開 web サービスの展開プロセスの一部としてインストールされています。</span><span class="sxs-lookup"><span data-stu-id="0fc31-157">The Mcx service is installed as part of the deployment process of your internal Lync Server 2013 deployment web services.</span></span>

    <Link token="Internal/Ucwa" href="https://webinternal.contoso.net/ucwa/v1/applications"/>

&nbsp;

    <Link token="External/Ucwa" href="https://webexternal.contoso.com/ucwa/v1/applications"/>

&nbsp;

    <Link token="Ucwa" href="https://webexternal.contoso.com/ucwa/v1/applications"/>

<span data-ttu-id="0fc31-158">**Internal/** ucwa、 **External/Ucwa** 、 **Ucwa** は、クライアントがユニファイドコミュニケーションの WEB アプリケーションプログラミングインターフェイス (ucwa API、または単に ucwa) にアクセスするための手段を提供します。</span><span class="sxs-lookup"><span data-stu-id="0fc31-158">**Internal/Ucwa**, **External/Ucwa** and **Ucwa** provide a means for clients to access the Unified Communications Web Application Programming Interface (UCWA API, or simply UCWA).</span></span> <span data-ttu-id="0fc31-159">`Internal/Ucwa``External/Ucwa`仮想ディレクトリは、将来の機能拡張のために予約されているアクセスポイントであり、使用されません。</span><span class="sxs-lookup"><span data-stu-id="0fc31-159">`Internal/Ucwa` and `External/Ucwa` virtual directories are access points reserved for future feature enhancement, and are not used.</span></span> <span data-ttu-id="0fc31-160">`Ucwa`仮想ディレクトリは、サポートされているすべてのデバイスで Microsoft Lync Mobile (Lync Server 2013 で導入) に使用されます。</span><span class="sxs-lookup"><span data-stu-id="0fc31-160">The `Ucwa` virtual directory is used for Microsoft Lync Mobile (introduced with Lync Server 2013) on all supported devices.</span></span> <span data-ttu-id="0fc31-161">UCWA サービスは、内部の Lync Server 2013 展開 web サービスの展開プロセスの一部としてインストールされます。</span><span class="sxs-lookup"><span data-stu-id="0fc31-161">The UCWA service is installed as part of the deployment process of your internal Lync Server 2013 deployment web services.</span></span>

    <Link token="Internal/XFrame" href="https://webinternal.contoso.net/Autodiscover/XFrame/XFrame.html"/>

&nbsp;

    <Link token="External/XFrame" href="https://webexternal.contoso.com/Autodiscover/XFrame/XFrame.html"/>

&nbsp;

    <Link token="XFrame" href="https://webexternal.contoso.com/Autodiscover/XFrame/XFrame.html"/>

<span data-ttu-id="0fc31-162">`Internal/XFrame`、 **External/xframe** と **xframe** は、ucwa ベースのサーバーアプリケーションへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="0fc31-162">`Internal/XFrame`, **External/XFrame** and **XFrame** provide access for UCWA-based server applications.</span></span> <span data-ttu-id="0fc31-163">XFrame は、内部の Lync Server 2013 展開 web サービスの展開プロセスの一部としてインストールされます。</span><span class="sxs-lookup"><span data-stu-id="0fc31-163">XFrame is installed as part of the deployment process of your internal Lync Server 2013 deployment web services.</span></span>

    <Link token="Self" href="https://webexternal.contoso.net/Autodiscover/AutodiscoverService.svc/root/user"/>

<span data-ttu-id="0fc31-164">トークンは、 `Self` 要求を行うクライアント (ユーザー応答の型) に固有の情報を参照します。</span><span class="sxs-lookup"><span data-stu-id="0fc31-164">The `Self` token refers to information specific to the client (user response type) that is making the request.</span></span> <span data-ttu-id="0fc31-165">この要求を行ったクライアントは外部であり、この自動検出参照は自動検出サービスのユーザー部分に対するものです。</span><span class="sxs-lookup"><span data-stu-id="0fc31-165">The client that made this request was external, and this Autodiscover reference is to the user portion of the Autodiscover service.</span></span>

</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="0fc31-166">関連項目</span><span class="sxs-lookup"><span data-stu-id="0fc31-166">See Also</span></span>


[<span data-ttu-id="0fc31-167">Lync Server 2013 の外部ユーザー アクセス コンポーネントのシステム要件</span><span class="sxs-lookup"><span data-stu-id="0fc31-167">System requirements for external user access components for Lync Server 2013</span></span>](lync-server-2013-system-requirements-for-external-user-access-components.md)  
[<span data-ttu-id="0fc31-168">Lync Server 2013 での自動検出の計画</span><span class="sxs-lookup"><span data-stu-id="0fc31-168">Planning for Autodiscover in Lync Server 2013</span></span>](lync-server-2013-planning-for-autodiscover.md)  
  

<span data-ttu-id="0fc31-169"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0fc31-169"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

