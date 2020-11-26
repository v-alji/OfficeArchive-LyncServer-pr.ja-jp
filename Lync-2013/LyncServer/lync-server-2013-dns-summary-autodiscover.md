---
title: 'Lync Server 2013: DNS の概要-自動検出'
description: 'Lync Server 2013: DNS の概要-自動検出。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - Autodiscover
ms:assetid: b336a2ae-0e58-4b74-b606-aedbbd411587
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945644(v=OCS.15)
ms:contentKeyID: 51541504
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: eef9bd6a2489561145718c7bbf2f710ab0b1f248
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429043"
---
# <a name="dns-summary---autodiscover-in-lync-server-2013"></a><span data-ttu-id="6ed54-103">DNS 概要-Lync Server 2013 での自動検出</span><span class="sxs-lookup"><span data-stu-id="6ed54-103">DNS summary - Autodiscover in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6ed54-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6ed54-104">

<span> </span></span></span>

<span data-ttu-id="6ed54-105">_**最終更新日:** 2013-02-13_</span><span class="sxs-lookup"><span data-stu-id="6ed54-105">_**Topic Last Modified:** 2013-02-13_</span></span>

<span data-ttu-id="6ed54-106">自動検出は、HTTP または HTTPS 経由での通信を受け付ける、柔軟なサービスです。</span><span class="sxs-lookup"><span data-stu-id="6ed54-106">Autodiscover is a flexible service in that it will accept communication over HTTP or HTTPS.</span></span> <span data-ttu-id="6ed54-107">これを実現するために、ドメインネームシステム (DNS) と自動検出サービスをホストするサーバーによって使われる証明書が正しく構成されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="6ed54-107">To accomplish this, the domain name system (DNS) and the certificates used by servers that host the Autodiscover service must be configured correctly.</span></span> <span data-ttu-id="6ed54-108">証明書の要件については [、「証明書の概要-Lync Server 2013 での自動検出](lync-server-2013-certificate-summary-autodiscover.md)」で説明します。</span><span class="sxs-lookup"><span data-stu-id="6ed54-108">Certificate requirements are covered in [Certificate summary - Autodiscover in Lync Server 2013](lync-server-2013-certificate-summary-autodiscover.md).</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="6ed54-109">Lync Server クライアントの DNS 検索ロジックは、特定の解決方法を使用します。</span><span class="sxs-lookup"><span data-stu-id="6ed54-109">DNS lookup logic for the Lync Server clients uses a specific order of resolution.</span></span> <span data-ttu-id="6ed54-110">常に lyncdiscoverinternal の両方が含まれている必要があります。 &lt;ドメイン &gt; と lyncdiscover &lt;&gt;DNS でドメインを選びます。</span><span class="sxs-lookup"><span data-stu-id="6ed54-110">You should always include both the lyncdiscoverinternal.&lt;domain&gt; and the lyncdiscover.&lt;domain&gt; in your DNS.</span></span> <span data-ttu-id="6ed54-111">Lyncdiscoverinternal を除外します。 &lt;ドメインレコードを使用すると &gt; 、内部クライアントは、目的のサービスに接続できないか、または正しくない自動検出応答を受信します。</span><span class="sxs-lookup"><span data-stu-id="6ed54-111">Excluding the lyncdiscoverinternal.&lt;domain&gt; record will cause internal clients to fail to connect to the intended services or receive the incorrect Autodiscover response.</span></span>



</div>

### <a name="internal-dns-records"></a><span data-ttu-id="6ed54-112">内部 DNS レコード</span><span class="sxs-lookup"><span data-stu-id="6ed54-112">Internal DNS Records</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6ed54-113">レコードの種類</span><span class="sxs-lookup"><span data-stu-id="6ed54-113">Record type</span></span></th>
<th><span data-ttu-id="6ed54-114">ホスト名</span><span class="sxs-lookup"><span data-stu-id="6ed54-114">Host name</span></span></th>
<th><span data-ttu-id="6ed54-115">解決先</span><span class="sxs-lookup"><span data-stu-id="6ed54-115">Resolves to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6ed54-116">CNAME</span><span class="sxs-lookup"><span data-stu-id="6ed54-116">CNAME</span></span></p></td>
<td><p><span data-ttu-id="6ed54-117">Lyncdiscoverinternal。 &lt;内部ドメイン名&gt;</span><span class="sxs-lookup"><span data-stu-id="6ed54-117">Lyncdiscoverinternal.&lt;internal domain name&gt;</span></span></p></td>
<td><p><span data-ttu-id="6ed54-118">ディレクタープールがある場合は、そのディレクタープールの内部 Web サービス FQDN。ディレクターを持っていない場合は、フロントエンドプールにも使用できます。</span><span class="sxs-lookup"><span data-stu-id="6ed54-118">Internal Web Services FQDN for your Director pool, if you have one, or for your Front End pool if you do not have a Director.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed54-119">A (IPv6 の場合は host、AAAA の場合)</span><span class="sxs-lookup"><span data-stu-id="6ed54-119">A (host, if IPv6, AAAA)</span></span></p></td>
<td><p><span data-ttu-id="6ed54-120">lyncdiscoverinternal。 &lt;内部ドメイン名&gt;</span><span class="sxs-lookup"><span data-stu-id="6ed54-120">lyncdiscoverinternal.&lt;internal domain name&gt;</span></span></p></td>
<td><p><span data-ttu-id="6ed54-121">ディレクターを持っていない場合は、ディレクタープールの内部 Web サービス IP アドレス (ロードバランサーを使用している場合は仮想 IP (VIP) のアドレス)。ディレクターを持っていない場合は、フロントエンドプールを所有している場合は、このアドレスを使用します。</span><span class="sxs-lookup"><span data-stu-id="6ed54-121">Internal Web Services IP address (virtual IP (VIP) address if you use a load balancer) of your Director pool, if you have one, or of your Front End pool if you do not have a Director.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6ed54-122">次のいずれかの外部 DNS レコードを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6ed54-122">You need to create one of the following external DNS records:</span></span>

### <a name="external-dns-records"></a><span data-ttu-id="6ed54-123">外部 DNS レコード</span><span class="sxs-lookup"><span data-stu-id="6ed54-123">External DNS Records</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6ed54-124">レコードの種類</span><span class="sxs-lookup"><span data-stu-id="6ed54-124">Record type</span></span></th>
<th><span data-ttu-id="6ed54-125">ホスト名</span><span class="sxs-lookup"><span data-stu-id="6ed54-125">Host name</span></span></th>
<th><span data-ttu-id="6ed54-126">解決先</span><span class="sxs-lookup"><span data-stu-id="6ed54-126">Resolves to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6ed54-127">CNAME</span><span class="sxs-lookup"><span data-stu-id="6ed54-127">CNAME</span></span></p></td>
<td><p><span data-ttu-id="6ed54-128">lyncdiscover。 &lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="6ed54-128">lyncdiscover.&lt;sipdomain&gt;</span></span></p></td>
<td><p><span data-ttu-id="6ed54-129">ディレクタープールを所有している場合は、そのディレクタープールの外部 Web サービス FQDN。ディレクターを持っていない場合は、フロントエンドプールに対応する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6ed54-129">External Web Services FQDN for your Director pool, if you have one, or for your Front End pool if you do not have a Director.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed54-130">A (IPv6 の場合は host、AAAA の場合)</span><span class="sxs-lookup"><span data-stu-id="6ed54-130">A (host, if IPv6, AAAA)</span></span></p></td>
<td><p><span data-ttu-id="6ed54-131">lyncdiscover。 &lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="6ed54-131">lyncdiscover.&lt;sipdomain&gt;</span></span></p></td>
<td><p><span data-ttu-id="6ed54-132">リバースプロキシの外部またはパブリック IP アドレス。</span><span class="sxs-lookup"><span data-stu-id="6ed54-132">External or public IP address of the reverse proxy.</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="6ed54-133">外部トラフィックはリバースプロキシ経由で送信されます。</span><span class="sxs-lookup"><span data-stu-id="6ed54-133">External traffic goes through the reverse proxy.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="6ed54-134">モバイルデバイスクライアントは、異なるドメインからの複数の Secure Sockets Layer (SSL) 証明書をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="6ed54-134">Mobile device clients do not support multiple Secure Sockets Layer (SSL) certificates from different domains.</span></span> <span data-ttu-id="6ed54-135">したがって、異なるドメインへの CNAME リダイレクションは HTTPS 経由ではサポートされません。</span><span class="sxs-lookup"><span data-stu-id="6ed54-135">Therefore, CNAME redirection to different domains is not supported over HTTPS.</span></span> <span data-ttu-id="6ed54-136">たとえば、director.contoso.net のアドレスにリダイレクトされる lyncdiscover.contoso.com の DNS CNAME レコードは HTTPS ではサポートされません。</span><span class="sxs-lookup"><span data-stu-id="6ed54-136">For example, a DNS CNAME record for lyncdiscover.contoso.com that redirects to an address of director.contoso.net is not supported over HTTPS.</span></span> <span data-ttu-id="6ed54-137">このようなトポロジでは、モバイルデバイスクライアントは、最初の要求に対して HTTP を使う必要があるため、CNAME リダイレクションが HTTP で解決されます。</span><span class="sxs-lookup"><span data-stu-id="6ed54-137">In such a topology, a mobile device client needs to use HTTP for the first request, so that the CNAME redirection is resolved over HTTP.</span></span> <span data-ttu-id="6ed54-138">それ以降の要求では HTTPS を使用します。</span><span class="sxs-lookup"><span data-stu-id="6ed54-138">Subsequent requests then use HTTPS.</span></span> <span data-ttu-id="6ed54-139">このシナリオをサポートするには、ポート 80 (HTTP) 用の web 公開ルールを使用してリバースプロキシを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6ed54-139">To support this scenario, you need to configure your reverse proxy with a web publishing rule for port 80 (HTTP).</span></span> <span data-ttu-id="6ed54-140">詳細については、「 <A href="lync-server-2013-configuring-the-reverse-proxy-for-mobility.md">Lync Server 2013 でモビリティのリバースプロキシを構成</A>する」の「ポート80用の web 公開ルールを作成するには」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ed54-140">For details, see "To create a web publishing rule for port 80" in <A href="lync-server-2013-configuring-the-reverse-proxy-for-mobility.md">Configuring the reverse proxy for mobility in Lync Server 2013</A>.</span></span> <span data-ttu-id="6ed54-141">同じドメインへの CNAME リダイレクションは HTTPS 経由でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="6ed54-141">CNAME redirection to the same domain is supported over HTTPS.</span></span> <span data-ttu-id="6ed54-142">この場合、宛先ドメインの証明書は元のドメインを対象としています。</span><span class="sxs-lookup"><span data-stu-id="6ed54-142">In this case, the destination domain's certificate covers the originating domain.</span></span>



</div>

<div>

## <a name="see-also"></a><span data-ttu-id="6ed54-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="6ed54-143">See Also</span></span>


[<span data-ttu-id="6ed54-144">Lync Server 2013 での、モビリティに合わせたリバース プロキシの構成</span><span class="sxs-lookup"><span data-stu-id="6ed54-144">Configuring the reverse proxy for mobility in Lync Server 2013</span></span>](lync-server-2013-configuring-the-reverse-proxy-for-mobility.md)  


[<span data-ttu-id="6ed54-145">証明書の概要-Lync Server 2013 での自動検出</span><span class="sxs-lookup"><span data-stu-id="6ed54-145">Certificate summary - Autodiscover in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-autodiscover.md)  
  

<span data-ttu-id="6ed54-146"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6ed54-146"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

