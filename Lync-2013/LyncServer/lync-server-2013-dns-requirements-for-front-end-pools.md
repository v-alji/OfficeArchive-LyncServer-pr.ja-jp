---
title: 'Lync Server 2013: フロント エンド プールの DNS 要件'
description: 'Lync Server 2013: フロント エンド プールの DNS 要件。'
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
# <a name="dns-requirements-for-front-end-pools-in-lync-server-2013"></a><span data-ttu-id="3880e-103">Lync Server 2013 のフロント エンド プールの DNS 要件</span><span class="sxs-lookup"><span data-stu-id="3880e-103">DNS requirements for Front End pools in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3880e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3880e-104">

<span> </span></span></span>

<span data-ttu-id="3880e-105">_**トピック最終更新日:** 2012-11-07_</span><span class="sxs-lookup"><span data-stu-id="3880e-105">_**Topic Last Modified:** 2012-11-07_</span></span>

<span data-ttu-id="3880e-106">このセクションでは、フロント エンド プールの展開に必要なドメイン ネーム システム (DNS) レコードについて説明します。</span><span class="sxs-lookup"><span data-stu-id="3880e-106">This section describes the Domain Name System (DNS) records that are required for deployment of Front End pools.</span></span>

<div>

## <a name="dns-records-for-front-end-pools"></a><span data-ttu-id="3880e-107">フロント エンド プールの DNS レコード</span><span class="sxs-lookup"><span data-stu-id="3880e-107">DNS Records for Front End Pools</span></span>

<span data-ttu-id="3880e-108">次の表は、Lync Server 2013 フロント エンド プール展開の DNS 要件を示しています。</span><span class="sxs-lookup"><span data-stu-id="3880e-108">The following table specifies DNS requirements for a Lync Server 2013 Front End pool deployment.</span></span>

### <a name="dns-requirements-for-a-front-end-pool"></a><span data-ttu-id="3880e-109">フロント エンド プールの DNS 要件</span><span class="sxs-lookup"><span data-stu-id="3880e-109">DNS Requirements for a Front End Pool</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3880e-110">展開シナリオ</span><span class="sxs-lookup"><span data-stu-id="3880e-110">Deployment scenario</span></span></th>
<th><span data-ttu-id="3880e-111">DNS 要件</span><span class="sxs-lookup"><span data-stu-id="3880e-111">DNS requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3880e-112">複数のフロント エンド サーバーとハードウェア ロード バランサーを備えたフロント エンド プール (DNS ロード バランシングもそのプールに展開されるかどうか)</span><span class="sxs-lookup"><span data-stu-id="3880e-112">Front End pool with multiple Front End Servers and a hardware load balancer (whether or not DNS load balancing is also deployed on that pool)</span></span></p></td>
<td><p><span data-ttu-id="3880e-113">DNS ロード バランシングとハードウェア ロード バランサーの両方を使用する場合は、レコードをホスト (A) する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3880e-113">When using both DNS load balancing and a hardware load balancer, you need to Host (A) records.</span></span> <span data-ttu-id="3880e-114">DNS ロード バランシングのためにフロント エンド プールの完全修飾ドメイン名 (FQDN) を解決する内部 A レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="3880e-114">Create an internal A record that resolves the fully qualified domain name (FQDN) of the Front End pool for DNS load balancing.</span></span> <span data-ttu-id="3880e-115">ロード バランサーの仮想 IP (VIP) アドレスに対する内部 Web サービスの内部ホスト (A) レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="3880e-115">Create an internal host (A) record for the internal Web services to the virtual IP (VIP) address of the load balancer.</span></span> <span data-ttu-id="3880e-116">トポロジ ビルダーで定義されている内部 Web サービス名を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3880e-116">You must use the internal Web services name as defined in Topology Builder.</span></span></p>
<p><span data-ttu-id="3880e-117">たとえば、DNS ロード バランシングとハードウェア ロード バランシングの両方を使用する場合、DNS ロード バランシング用のプール内の各フロント エンド サーバーの A レコードと、ハードウェア ロード バランサーの仮想 IP をポイントする内部 Web サービスの A レコードがあります。</span><span class="sxs-lookup"><span data-stu-id="3880e-117">For example, if you use both DNS load balancing and hardware load balancing, you would have an A record for each Front End Server in a pool for DNS load balancing, and an A record for the internal Web services pointing to the virtual IP of the hardware load balancer:</span></span></p>
<ul>
<li><p><span data-ttu-id="3880e-118">DNS ロード バランシング: Pool01.contoso.net プール 10.10.10.5 の IP アドレス</span><span class="sxs-lookup"><span data-stu-id="3880e-118">DNS load balancing:   Pool01.contoso.net   IP Address of pool   10.10.10.5</span></span></p>
<div>

> [!WARNING]  
> <span data-ttu-id="3880e-119">各フロント エンド サーバーには、次の異なる A レコードも含されます。</span><span class="sxs-lookup"><span data-stu-id="3880e-119">Each Front End Server will also have a distinct A record:</span></span>


</div>
<ol>
<li><p><span data-ttu-id="3880e-120">FE01.contoso.net 10.10.10.1</span><span class="sxs-lookup"><span data-stu-id="3880e-120">FE01.contoso.net    10.10.10.1</span></span></p></li>
<li><p><span data-ttu-id="3880e-121">FE02.contoso.net 10.10.10.2</span><span class="sxs-lookup"><span data-stu-id="3880e-121">FE02.contoso.net    10.10.10.2</span></span></p></li>
<li><p><span data-ttu-id="3880e-122">FE03.contoso.net 10.10.10.3</span><span class="sxs-lookup"><span data-stu-id="3880e-122">FE03.contoso.net    10.10.10.3</span></span></p></li>
<li><p><span data-ttu-id="3880e-123">FE04.contoso.net 10.10.10.4</span><span class="sxs-lookup"><span data-stu-id="3880e-123">FE04.contoso.net    10.10.10.4</span></span></p></li>
</ol></li>
<li><p><span data-ttu-id="3880e-124">ハードウェア ロード バランシング: WebInternal.contoso.net HLB VIP 192.168.10.5 の IP アドレス</span><span class="sxs-lookup"><span data-stu-id="3880e-124">Hardware load balancing:   WebInternal.contoso.net   IP Address of HLB VIP   192.168.10.5</span></span></p></li>
</ul>
<p><span data-ttu-id="3880e-125">HTTP/HTTPS トラフィックを除くすべてのトラフィックは、そのレコード Pool01.contoso.net します。</span><span class="sxs-lookup"><span data-stu-id="3880e-125">All traffic except for HTTP/HTTPS traffic will use the Pool01.contoso.net record.</span></span> <span data-ttu-id="3880e-126">HTTP/HTTPS トラフィックでは、定義された内部 Web サービス アドレス 192.168.10.5 が使用されます。</span><span class="sxs-lookup"><span data-stu-id="3880e-126">HTTP/HTTPS traffic will use the defined internal Web services address of 192.168.10.5</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3880e-127">DNS ロード バランシングが展開されたフロント エンド プール</span><span class="sxs-lookup"><span data-stu-id="3880e-127">Front End pool with DNS load balancing deployed</span></span></p></td>
<td><p><span data-ttu-id="3880e-128">プールの FQDN をプール内の各サーバーの IP アドレスに解決する内部 A レコードのセット。</span><span class="sxs-lookup"><span data-stu-id="3880e-128">A set of internal A records that resolve the FQDN of the pool to the IP address of each server in the pool.</span></span> <span data-ttu-id="3880e-129">プール内のサーバーごとに 1 つの A レコードが必要です。</span><span class="sxs-lookup"><span data-stu-id="3880e-129">There must one A record for each server in the pool.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3880e-130">DNS ロード バランシングが展開されたフロント エンド プール</span><span class="sxs-lookup"><span data-stu-id="3880e-130">Front End pool with DNS load balancing deployed</span></span></p></td>
<td><p><span data-ttu-id="3880e-131">プール内の各サーバーの FQDN をそのサーバーの IP アドレスに解決する内部 A レコードのセット。</span><span class="sxs-lookup"><span data-stu-id="3880e-131">A set of internal A records that resolve the FQDN of each server in the pool to the IP address of that server.</span></span> <span data-ttu-id="3880e-132">詳細については、計画に関するドキュメントの <a href="lync-server-2013-dns-load-balancing.md">「Lync Server 2013</a> の DNS ロード バランシング」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3880e-132">For details, see <a href="lync-server-2013-dns-load-balancing.md">DNS load balancing in Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3880e-133">1 つのフロント エンド サーバーと専用のバック エンド データベースを備え、ロード バランサーがないフロント エンド プール</span><span class="sxs-lookup"><span data-stu-id="3880e-133">Front End pool with a single Front End Server and a dedicated back-end database but no load balancer</span></span></p></td>
<td><p><span data-ttu-id="3880e-134">フロント エンド プールの FQDN を単一の Enterprise Edition フロント エンド サーバーの IP アドレスに解決する内部 A レコード。</span><span class="sxs-lookup"><span data-stu-id="3880e-134">An internal A record that resolves the FQDN of the Front End pool to the IP address of the single Enterprise Edition Front End Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3880e-135">クライアントの自動サインイン</span><span class="sxs-lookup"><span data-stu-id="3880e-135">Automatic client sign-in</span></span></p></td>
<td><p><span data-ttu-id="3880e-136">サポートされている SIP ドメインごとに、_sipinternaltls._tcp の SRV レコード。 &lt;サインイン要求を認証してリダイレクトするフロント エンド プールの FQDN にマップされるポート &gt; 5061 を超えるドメイン。</span><span class="sxs-lookup"><span data-stu-id="3880e-136">For each supported SIP domain, an SRV record for _sipinternaltls._tcp.&lt;domain&gt; over port 5061 that maps to the FQDN of the Front End pool that authenticates and redirects client requests for sign-in.</span></span> <span data-ttu-id="3880e-137">詳細については <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">、Lync Server 2013</a>での自動クライアント サインインの DNS 要件を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3880e-137">For details, see <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">DNS requirements for automatic client sign-in in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3880e-138">ユニファイド コミュニケーション (UC) デバイスによるデバイス更新 Web サービス検出</span><span class="sxs-lookup"><span data-stu-id="3880e-138">Device Update Web service discovery by unified communications (UC) devices</span></span></p></td>
<td><p><span data-ttu-id="3880e-139">ucupdates-r2 という名前の内部 A レコード。 &lt;Device Update Web サービスをホストするフロント エンド プールの IP アドレスに解決 &gt; される SIP ドメイン。</span><span class="sxs-lookup"><span data-stu-id="3880e-139">An internal A record with the name ucupdates-r2.&lt;SIP domain&gt; that resolves to the IP address of the Front End pool that hosts the Device Update Web service.</span></span> <span data-ttu-id="3880e-140">UC デバイスがオンになっているが、ユーザーがデバイスにログインしたことがない場合、A レコードにより、デバイスは Device Update Web サービスをホストするフロント エンド プールを検出し、更新プログラムを取得できます。</span><span class="sxs-lookup"><span data-stu-id="3880e-140">In the situation where a UC device is turned on, but a user has never logged into the device, the A record allows the device to discover the Front End pool hosting Device Update Web service and obtain updates.</span></span> <span data-ttu-id="3880e-141">それ以外の場合、ユーザーが初めてログインすると、デバイスはインバンド プロビジョニングを行ってこの情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="3880e-141">Otherwise, devices obtain this information though in-band provisioning the first time a user logs in.</span></span></p>
<div>

> [!IMPORTANT]  
> <span data-ttu-id="3880e-142">Lync Server 2010 で Device Update Web サービスを展開している場合は、ucupdates という名前の内部 A レコードを既に作成しています。 &lt;SIP ドメイン &gt; 。</span><span class="sxs-lookup"><span data-stu-id="3880e-142">If you have an existing deployment of Device Update Web service in Lync Server 2010, you have already created an internal A record with the name ucupdates.&lt;SIP domain&gt;.</span></span> <span data-ttu-id="3880e-143">Communications Server 2007 R2 Microsoft Office、ucupdates-r2 という名前の追加の DNS A レコードを作成する必要があります。 &lt;SIP ドメイン &gt; 。</span><span class="sxs-lookup"><span data-stu-id="3880e-143">For Microsoft Office Communications Server 2007 R2, you must create an additional DNS A record with the name ucupdates-r2.&lt;SIP domain&gt;.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3880e-144">HTTP トラフィックをサポートするリバース プロキシ</span><span class="sxs-lookup"><span data-stu-id="3880e-144">A reverse proxy to support HTTP traffic</span></span></p></td>
<td><p><span data-ttu-id="3880e-145">外部 Web ファームの FQDN をリバース プロキシの外部 IP アドレスに解決する外部 A レコード。</span><span class="sxs-lookup"><span data-stu-id="3880e-145">An external A record that resolves the external web farm FQDN to the external IP address of the reverse proxy.</span></span> <span data-ttu-id="3880e-146">クライアントと UC デバイスは、このレコードを使用してリバース プロキシに接続します。</span><span class="sxs-lookup"><span data-stu-id="3880e-146">Clients and UC devices use this record to connect to the reverse proxy.</span></span> <span data-ttu-id="3880e-147">詳細については、計画に <a href="lync-server-2013-determine-dns-requirements.md">関するドキュメントの「Lync Server 2013</a> の DNS 要件を決定する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3880e-147">For details, see <a href="lync-server-2013-determine-dns-requirements.md">Determine DNS requirements for Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3880e-148">次の表は、内部 Web ファームの FQDN に必要な DNS レコードの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="3880e-148">The following table shows an example of the DNS records required for the internal web farm FQDN.</span></span>

### <a name="example-dns-records-for-internal-web-farm-fqdn"></a><span data-ttu-id="3880e-149">内部 Web ファーム FQDN の DNS レコードの例</span><span class="sxs-lookup"><span data-stu-id="3880e-149">Example DNS Records for Internal Web Farm FQDN</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3880e-150">内部 Web ファームの FQDN</span><span class="sxs-lookup"><span data-stu-id="3880e-150">Internal web farm FQDN</span></span></th>
<th><span data-ttu-id="3880e-151">プールの FQDN</span><span class="sxs-lookup"><span data-stu-id="3880e-151">Pool FQDN</span></span></th>
<th><span data-ttu-id="3880e-152">DNS A レコード</span><span class="sxs-lookup"><span data-stu-id="3880e-152">DNS A record(s)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3880e-153">webcon.contoso.com</span><span class="sxs-lookup"><span data-stu-id="3880e-153">webcon.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="3880e-154">ee-pool.contoso.com</span><span class="sxs-lookup"><span data-stu-id="3880e-154">ee-pool.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="3880e-155">フロントエンド サーバーによって使用 ee-pool.contoso.com ロード バランサーの VIP アドレスに解決される、サーバーの DNS A レコード。</span><span class="sxs-lookup"><span data-stu-id="3880e-155">DNS A record for the ee-pool.contoso.com that resolves to the VIP address of the load balancer used by the Front End Servers.</span></span></p>
<p><span data-ttu-id="3880e-156">フロントエンド サーバーによって webcon.contoso.com ロード バランサーの VIP アドレスに解決される、サーバーの DNS A レコード。</span><span class="sxs-lookup"><span data-stu-id="3880e-156">DNS A record for webcon.contoso.com that resolves to the VIP address of the load balancer used by the Front End Servers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3880e-157">ee-pool.contoso.com</span><span class="sxs-lookup"><span data-stu-id="3880e-157">ee-pool.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="3880e-158">ee-pool.contoso.com</span><span class="sxs-lookup"><span data-stu-id="3880e-158">ee-pool.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="3880e-159">フロント エンド プール ee-pool.contoso.com Enterprise Edition フロント エンド サーバーによって使用されるロード バランサーの仮想 IP (VIP) アドレスに解決する、ee-pool.contoso.com 用の DNS レコード。</span><span class="sxs-lookup"><span data-stu-id="3880e-159">DNS A record for ee-pool.contoso.com that resolves to the virtual IP (VIP) address of the load balancer used by the Enterprise Edition Front End Servers in the Front End pool.</span></span></p>
<p><span data-ttu-id="3880e-160">このプールで DNS ロード バランシングを使用している場合は、フロント エンド プールと内部 Web ファームに同じ FQDN を設定できないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="3880e-160">Note that if you are using DNS load balancing on this pool, your Front End pool and internal web farm cannot have the same FQDN.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="3880e-161">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3880e-161">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

