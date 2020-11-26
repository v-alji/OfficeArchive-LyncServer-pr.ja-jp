---
title: 'Lync Server 2013: フロントエンドプールの DNS 要件'
description: 'Lync Server 2013: フロントエンドプールの DNS 要件。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for Front End pools
ms:assetid: ba28919c-fbbe-4c54-8bf9-2b0cd3fa39c7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412910(v=OCS.15)
ms:contentKeyID: 48185228
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8c0369e82bd8ed2ea63e2156728b41f9942b0148
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429071"
---
# <a name="dns-requirements-for-front-end-pools-in-lync-server-2013"></a><span data-ttu-id="b5a8d-103">Lync Server 2013 のフロントエンドプールの DNS 要件</span><span class="sxs-lookup"><span data-stu-id="b5a8d-103">DNS requirements for Front End pools in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b5a8d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b5a8d-104">

<span> </span></span></span>

<span data-ttu-id="b5a8d-105">_**最終更新日:** 2012-11-07_</span><span class="sxs-lookup"><span data-stu-id="b5a8d-105">_**Topic Last Modified:** 2012-11-07_</span></span>

<span data-ttu-id="b5a8d-106">このセクションでは、フロントエンドプールの展開に必要なドメインネームシステム (DNS) レコードについて説明します。</span><span class="sxs-lookup"><span data-stu-id="b5a8d-106">This section describes the Domain Name System (DNS) records that are required for deployment of Front End pools.</span></span>

<div>

## <a name="dns-records-for-front-end-pools"></a><span data-ttu-id="b5a8d-107">フロントエンドプールの DNS レコード</span><span class="sxs-lookup"><span data-stu-id="b5a8d-107">DNS Records for Front End Pools</span></span>

<span data-ttu-id="b5a8d-108">次の表は、Lync Server 2013 フロントエンドプールの展開の DNS 要件を示しています。</span><span class="sxs-lookup"><span data-stu-id="b5a8d-108">The following table specifies DNS requirements for a Lync Server 2013 Front End pool deployment.</span></span>

### <a name="dns-requirements-for-a-front-end-pool"></a><span data-ttu-id="b5a8d-109">フロントエンドプールの DNS 要件</span><span class="sxs-lookup"><span data-stu-id="b5a8d-109">DNS Requirements for a Front End Pool</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b5a8d-110">展開シナリオ</span><span class="sxs-lookup"><span data-stu-id="b5a8d-110">Deployment scenario</span></span></th>
<th><span data-ttu-id="b5a8d-111">DNS 要件</span><span class="sxs-lookup"><span data-stu-id="b5a8d-111">DNS requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b5a8d-112">複数のフロントエンドサーバーとハードウェアロードバランサーを備えたフロントエンドプール (このプールには DNS 負荷分散も展開されているかどうかにかかわらず)</span><span class="sxs-lookup"><span data-stu-id="b5a8d-112">Front End pool with multiple Front End Servers and a hardware load balancer (whether or not DNS load balancing is also deployed on that pool)</span></span></p></td>
<td><p><span data-ttu-id="b5a8d-113">DNS ロードバランシングとハードウェアロードバランサーの両方を使用する場合は、(A) レコードをホストする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5a8d-113">When using both DNS load balancing and a hardware load balancer, you need to Host (A) records.</span></span> <span data-ttu-id="b5a8d-114">DNS の負荷分散のために、フロントエンドプールの完全修飾ドメイン名 (FQDN) を解決する内部 A レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="b5a8d-114">Create an internal A record that resolves the fully qualified domain name (FQDN) of the Front End pool for DNS load balancing.</span></span> <span data-ttu-id="b5a8d-115">内部 Web サービスの内部ホスト (A) レコードを、ロードバランサーの仮想 IP (VIP) アドレスに作成します。</span><span class="sxs-lookup"><span data-stu-id="b5a8d-115">Create an internal host (A) record for the internal Web services to the virtual IP (VIP) address of the load balancer.</span></span> <span data-ttu-id="b5a8d-116">トポロジビルダーで定義されている内部 Web サービス名を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5a8d-116">You must use the internal Web services name as defined in Topology Builder.</span></span></p>
<p><span data-ttu-id="b5a8d-117">たとえば、DNS の負荷分散とハードウェアの負荷分散の両方を使用する場合は、DNS の負荷分散用のプール内の各フロントエンドサーバーの A レコードと、ハードウェアロードバランサーの仮想 IP を指す内部 Web サービスの A レコードがあります。</span><span class="sxs-lookup"><span data-stu-id="b5a8d-117">For example, if you use both DNS load balancing and hardware load balancing, you would have an A record for each Front End Server in a pool for DNS load balancing, and an A record for the internal Web services pointing to the virtual IP of the hardware load balancer:</span></span></p>
<ul>
<li><p><span data-ttu-id="b5a8d-118">DNS の負荷分散: Pool01.contoso.net プールの IP アドレス10.10.10.5</span><span class="sxs-lookup"><span data-stu-id="b5a8d-118">DNS load balancing:   Pool01.contoso.net   IP Address of pool   10.10.10.5</span></span></p>
<div>

> [!WARNING]  
> <span data-ttu-id="b5a8d-119">各フロントエンドサーバーにも、個別のレコードがあります。</span><span class="sxs-lookup"><span data-stu-id="b5a8d-119">Each Front End Server will also have a distinct A record:</span></span>


</div>
<ol>
<li><p><span data-ttu-id="b5a8d-120">FE01.contoso.net 10.10.10.1</span><span class="sxs-lookup"><span data-stu-id="b5a8d-120">FE01.contoso.net    10.10.10.1</span></span></p></li>
<li><p><span data-ttu-id="b5a8d-121">FE02.contoso.net 10.10.10.2</span><span class="sxs-lookup"><span data-stu-id="b5a8d-121">FE02.contoso.net    10.10.10.2</span></span></p></li>
<li><p><span data-ttu-id="b5a8d-122">FE03.contoso.net 10.10.10.3</span><span class="sxs-lookup"><span data-stu-id="b5a8d-122">FE03.contoso.net    10.10.10.3</span></span></p></li>
<li><p><span data-ttu-id="b5a8d-123">FE04.contoso.net 10.10.10.4</span><span class="sxs-lookup"><span data-stu-id="b5a8d-123">FE04.contoso.net    10.10.10.4</span></span></p></li>
</ol></li>
<li><p><span data-ttu-id="b5a8d-124">ハードウェア負荷分散: HLB VIP 192.168.10.5 の WebInternal.contoso.net IP アドレス</span><span class="sxs-lookup"><span data-stu-id="b5a8d-124">Hardware load balancing:   WebInternal.contoso.net   IP Address of HLB VIP   192.168.10.5</span></span></p></li>
</ul>
<p><span data-ttu-id="b5a8d-125">HTTP/HTTPS トラフィック以外のすべてのトラフィックでは、Pool01.contoso.net レコードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="b5a8d-125">All traffic except for HTTP/HTTPS traffic will use the Pool01.contoso.net record.</span></span> <span data-ttu-id="b5a8d-126">HTTP/HTTPS トラフィックでは、定義された内部 Web サービスのアドレスを使用します192.168.10.5</span><span class="sxs-lookup"><span data-stu-id="b5a8d-126">HTTP/HTTPS traffic will use the defined internal Web services address of 192.168.10.5</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5a8d-127">DNS 負荷分散が展開されたフロントエンドプール</span><span class="sxs-lookup"><span data-stu-id="b5a8d-127">Front End pool with DNS load balancing deployed</span></span></p></td>
<td><p><span data-ttu-id="b5a8d-128">プールの FQDN を、プールの各サーバーの IP アドレスに解決する内部 A レコードのセット。</span><span class="sxs-lookup"><span data-stu-id="b5a8d-128">A set of internal A records that resolve the FQDN of the pool to the IP address of each server in the pool.</span></span> <span data-ttu-id="b5a8d-129">プール内の各サーバーに1つのレコードが必要です。</span><span class="sxs-lookup"><span data-stu-id="b5a8d-129">There must one A record for each server in the pool.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5a8d-130">DNS 負荷分散が展開されたフロントエンドプール</span><span class="sxs-lookup"><span data-stu-id="b5a8d-130">Front End pool with DNS load balancing deployed</span></span></p></td>
<td><p><span data-ttu-id="b5a8d-131">プール内の各サーバーの FQDN をそのサーバーの IP アドレスに解決する内部 A レコードのセット。</span><span class="sxs-lookup"><span data-stu-id="b5a8d-131">A set of internal A records that resolve the FQDN of each server in the pool to the IP address of that server.</span></span> <span data-ttu-id="b5a8d-132">詳細については、計画ドキュメントの「 <a href="lync-server-2013-dns-load-balancing.md">Lync Server 2013 での DNS の負荷分散</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5a8d-132">For details, see <a href="lync-server-2013-dns-load-balancing.md">DNS load balancing in Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5a8d-133">フロントエンドサーバーと、専用のバックエンドデータベースを備えたフロントエンドプール (ロードバランサーはありません)</span><span class="sxs-lookup"><span data-stu-id="b5a8d-133">Front End pool with a single Front End Server and a dedicated back-end database but no load balancer</span></span></p></td>
<td><p><span data-ttu-id="b5a8d-134">フロントエンドプールの FQDN を単一の Enterprise Edition フロントエンドサーバーの IP アドレスに解決する内部の A レコード。</span><span class="sxs-lookup"><span data-stu-id="b5a8d-134">An internal A record that resolves the FQDN of the Front End pool to the IP address of the single Enterprise Edition Front End Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5a8d-135">自動クライアントサインイン</span><span class="sxs-lookup"><span data-stu-id="b5a8d-135">Automatic client sign-in</span></span></p></td>
<td><p><span data-ttu-id="b5a8d-136">サポートされている各 SIP ドメインについて、_sipinternaltls _tcp の SRV レコード&gt;サインインのためのクライアント要求を認証してリダイレクトするフロントエンドプールの FQDN にマップされる、ポート5061経由のドメイン。</span><span class="sxs-lookup"><span data-stu-id="b5a8d-136">For each supported SIP domain, an SRV record for _sipinternaltls._tcp.&lt;domain&gt; over port 5061 that maps to the FQDN of the Front End pool that authenticates and redirects client requests for sign-in.</span></span> <span data-ttu-id="b5a8d-137">詳細については、「 <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">Lync Server 2013 での自動クライアントサインインの DNS 要件</a>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5a8d-137">For details, see <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">DNS requirements for automatic client sign-in in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5a8d-138">ユニファイドコミュニケーション (UC) デバイスによるデバイス更新 Web サービスの検出</span><span class="sxs-lookup"><span data-stu-id="b5a8d-138">Device Update Web service discovery by unified communications (UC) devices</span></span></p></td>
<td><p><span data-ttu-id="b5a8d-139">"Ucupdates-r2" という名前の内部 A レコード。 &lt;&gt;デバイス更新 Web サービスをホストしているフロントエンドプールの IP アドレスに解決される SIP ドメイン。</span><span class="sxs-lookup"><span data-stu-id="b5a8d-139">An internal A record with the name ucupdates-r2.&lt;SIP domain&gt; that resolves to the IP address of the Front End pool that hosts the Device Update Web service.</span></span> <span data-ttu-id="b5a8d-140">UC デバイスが有効になっている状態で、ユーザーがデバイスにログインしたことがない場合、A レコードにより、デバイスはデバイス更新 Web サービスをホストするフロントエンドプールを検出し、更新プログラムを入手できます。</span><span class="sxs-lookup"><span data-stu-id="b5a8d-140">In the situation where a UC device is turned on, but a user has never logged into the device, the A record allows the device to discover the Front End pool hosting Device Update Web service and obtain updates.</span></span> <span data-ttu-id="b5a8d-141">そうしないと、デバイスは、ユーザーが初めてログインしたときに、インバンドプロビジョニングでこの情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="b5a8d-141">Otherwise, devices obtain this information though in-band provisioning the first time a user logs in.</span></span></p>
<div>

> [!IMPORTANT]  
> <span data-ttu-id="b5a8d-142">Lync Server 2010 で既存のデバイス更新 Web サービスを展開している場合は、「ucupdates」という名前の内部レコードが既に作成されています。 &lt;SIP ドメイン &gt; 。</span><span class="sxs-lookup"><span data-stu-id="b5a8d-142">If you have an existing deployment of Device Update Web service in Lync Server 2010, you have already created an internal A record with the name ucupdates.&lt;SIP domain&gt;.</span></span> <span data-ttu-id="b5a8d-143">Microsoft Office Communications Server 2007 R2 の場合は、ucupdates-R2 という名前の追加 DNS A レコードを作成する必要があります。 &lt;SIP ドメイン &gt; 。</span><span class="sxs-lookup"><span data-stu-id="b5a8d-143">For Microsoft Office Communications Server 2007 R2, you must create an additional DNS A record with the name ucupdates-r2.&lt;SIP domain&gt;.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5a8d-144">HTTP トラフィックをサポートする逆プロキシ</span><span class="sxs-lookup"><span data-stu-id="b5a8d-144">A reverse proxy to support HTTP traffic</span></span></p></td>
<td><p><span data-ttu-id="b5a8d-145">外部の web ファーム FQDN をリバースプロキシの外部 IP アドレスに解決する外部の A レコード。</span><span class="sxs-lookup"><span data-stu-id="b5a8d-145">An external A record that resolves the external web farm FQDN to the external IP address of the reverse proxy.</span></span> <span data-ttu-id="b5a8d-146">クライアントと UC デバイスこのレコードを使ってリバースプロキシに接続します。</span><span class="sxs-lookup"><span data-stu-id="b5a8d-146">Clients and UC devices use this record to connect to the reverse proxy.</span></span> <span data-ttu-id="b5a8d-147">詳細については、「計画ドキュメントの「 <a href="lync-server-2013-determine-dns-requirements.md">Lync Server 2013 の DNS 要件を決定</a> する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5a8d-147">For details, see <a href="lync-server-2013-determine-dns-requirements.md">Determine DNS requirements for Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b5a8d-148">次の表は、内部 web ファーム FQDN に必要な DNS レコードの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="b5a8d-148">The following table shows an example of the DNS records required for the internal web farm FQDN.</span></span>

### <a name="example-dns-records-for-internal-web-farm-fqdn"></a><span data-ttu-id="b5a8d-149">内部 Web ファーム FQDN の DNS レコードの例</span><span class="sxs-lookup"><span data-stu-id="b5a8d-149">Example DNS Records for Internal Web Farm FQDN</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b5a8d-150">内部 web ファーム FQDN</span><span class="sxs-lookup"><span data-stu-id="b5a8d-150">Internal web farm FQDN</span></span></th>
<th><span data-ttu-id="b5a8d-151">プールの FQDN</span><span class="sxs-lookup"><span data-stu-id="b5a8d-151">Pool FQDN</span></span></th>
<th><span data-ttu-id="b5a8d-152">DNS A レコード</span><span class="sxs-lookup"><span data-stu-id="b5a8d-152">DNS A record(s)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b5a8d-153">webcon.contoso.com</span><span class="sxs-lookup"><span data-stu-id="b5a8d-153">webcon.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="b5a8d-154">ee-pool.contoso.com</span><span class="sxs-lookup"><span data-stu-id="b5a8d-154">ee-pool.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="b5a8d-155">DNS A フロントエンドサーバーによって使用されるロードバランサーの VIP アドレスに解決される ee-pool.contoso.com のレコード。</span><span class="sxs-lookup"><span data-stu-id="b5a8d-155">DNS A record for the ee-pool.contoso.com that resolves to the VIP address of the load balancer used by the Front End Servers.</span></span></p>
<p><span data-ttu-id="b5a8d-156">DNS A フロントエンドサーバーによって使用されるロードバランサーの VIP アドレスに解決される webcon.contoso.com のレコード。</span><span class="sxs-lookup"><span data-stu-id="b5a8d-156">DNS A record for webcon.contoso.com that resolves to the VIP address of the load balancer used by the Front End Servers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5a8d-157">ee-pool.contoso.com</span><span class="sxs-lookup"><span data-stu-id="b5a8d-157">ee-pool.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="b5a8d-158">ee-pool.contoso.com</span><span class="sxs-lookup"><span data-stu-id="b5a8d-158">ee-pool.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="b5a8d-159">DNS A ee-pool.contoso.com の A レコード。フロントエンドプールの Enterprise Edition フロントエンドサーバーによって使用されるロードバランサーの仮想 IP (VIP) アドレスに解決されます。</span><span class="sxs-lookup"><span data-stu-id="b5a8d-159">DNS A record for ee-pool.contoso.com that resolves to the virtual IP (VIP) address of the load balancer used by the Enterprise Edition Front End Servers in the Front End pool.</span></span></p>
<p><span data-ttu-id="b5a8d-160">このプールで DNS の負荷分散を使用している場合は、フロントエンドプールと内部 web ファームの FQDN を同じにすることはできません。</span><span class="sxs-lookup"><span data-stu-id="b5a8d-160">Note that if you are using DNS load balancing on this pool, your Front End pool and internal web farm cannot have the same FQDN.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b5a8d-161">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b5a8d-161">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

