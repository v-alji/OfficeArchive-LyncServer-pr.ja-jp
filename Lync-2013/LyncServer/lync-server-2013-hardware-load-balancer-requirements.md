---
title: Lync Server 2013 のハードウェア ロード バランサーの要件
description: Lync Server 2013 ハードウェアロードバランサーの要件。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hardware load balancer requirements
ms:assetid: 32891268-2059-43d0-adf4-af4ff1e9ce66
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ656815(v=OCS.15)
ms:contentKeyID: 49287208
ms.date: 05/11/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 69cbf79c1fd7551dfd428c23ed22c924d0805c43
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427720"
---
# <a name="hardware-load-balancer-requirements-for-lync-server-2013"></a><span data-ttu-id="089b4-103">Lync Server 2013 のハードウェア ロード バランサーの要件</span><span class="sxs-lookup"><span data-stu-id="089b4-103">Hardware load balancer requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="089b4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="089b4-104">

<span> </span></span></span>

<span data-ttu-id="089b4-105">_**最終更新日:** 2015-05-11_</span><span class="sxs-lookup"><span data-stu-id="089b4-105">_**Topic Last Modified:** 2015-05-11_</span></span>

<span data-ttu-id="089b4-106">Lync Server 2013 スケーリングされた統合エッジトポロジは、新しい展開の場合、Lync Server を使用する他の組織との主な展開のために、DNS の負荷分散のために最適化されています。</span><span class="sxs-lookup"><span data-stu-id="089b4-106">The Lync Server 2013 scaled consolidated Edge topology is optimized for DNS load balancing for new deployments federating primarily with other organizations using Lync Server.</span></span> <span data-ttu-id="089b4-107">次のシナリオのいずれかに対して高可用性が必要な場合は、次のように、エッジサーバープールでハードウェアロードバランサーを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="089b4-107">If high availability is required for any of the following scenarios, a hardware load balancer must be used on Edge Server pools for the following:</span></span>

  - <span data-ttu-id="089b4-108">Office Communications Server 2007 R2 または Office Communications Server 2007 を使用している組織とのフェデレーション</span><span class="sxs-lookup"><span data-stu-id="089b4-108">Federation with organizations using Office Communications Server 2007 R2 or Office Communications Server 2007</span></span>

  - <span data-ttu-id="089b4-109">Exchange 2010 SP1 より前の exchange UM を使用しているリモートユーザーの exchange UM</span><span class="sxs-lookup"><span data-stu-id="089b4-109">Exchange UM for remote users using Exchange UM prior to Exchange 2010 with SP1</span></span>

  - <span data-ttu-id="089b4-110">パブリック IM ユーザーとの接続</span><span class="sxs-lookup"><span data-stu-id="089b4-110">Connectivity to public IM users</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="089b4-p102">1 つのインターフェイスでハードウェア負荷分散を使用し、もう 1 つのインターフェイスで DNS 負荷分散を使用することはできません。両方のインターフェイスでハードウェア負荷分散を使用するか、両方で DNS 負荷分散を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="089b4-p102">Using DNS load balancing on one interface and hardware load balancing on the other is not supported. You must use hardware load balancing for both interfaces or DNS load balancing for both.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="089b4-p103">ロード バランサー機器を使用している場合は、内部ネットワークとの接続用に展開されているロード バランサーを構成して、アクセス エッジ サービスおよび音声ビデオ サービスを実行しているサーバーへのトラフィックのみを負荷分散する必要があります。内部の Web 会議エッジ サービスまたは内部 XMPP プロキシ サービスへのトラフィックを負荷分散することはできません。</span><span class="sxs-lookup"><span data-stu-id="089b4-p103">If you are using a hardware load balancer, the load balancer deployed for connections with the internal network must be configured to load balance only the traffic to servers running the Access Edge service and the A/V Edge service. It cannot load balance the traffic to the internal Web Conferencing Edge service or the internal XMPP Proxy service.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="089b4-115">Direct server return (DSR) NAT は、Lync Server 2013 ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="089b4-115">The direct server return (DSR) NAT is not supported with Lync Server 2013.</span></span>



</div>

<span data-ttu-id="089b4-116">使用しているハードウェアロードバランサーが Lync Server 2013 に必要な機能をサポートしているかどうかを判断するには、の「Lync Server 2010 ロードバランサーパートナー」を参照してください [https://go.microsoft.com/fwlink/p/?linkId=202452](https://go.microsoft.com/fwlink/p/?linkid=202452) 。</span><span class="sxs-lookup"><span data-stu-id="089b4-116">To determine whether your hardware load balancer supports the necessary features required by Lync Server 2013, see "Lync Server 2010 Load Balancer Partners" at [https://go.microsoft.com/fwlink/p/?linkId=202452](https://go.microsoft.com/fwlink/p/?linkid=202452).</span></span>

<div>

## <a name="hardware-load-balancer-requirements-for-edge-servers-running-the-av-edge-service"></a><span data-ttu-id="089b4-117">音声ビデオ エッジ サービスを実行するエッジ サーバーに対するロード バランサー機器の要件</span><span class="sxs-lookup"><span data-stu-id="089b4-117">Hardware Load Balancer Requirements for Edge Servers Running the A/V Edge Service</span></span>

<span data-ttu-id="089b4-118">A/V Edge サービスを実行しているエッジサーバーのハードウェアロードバランサーの要件を次に示します。</span><span class="sxs-lookup"><span data-stu-id="089b4-118">Following are the hardware load balancer requirements for Edge Servers running the A/V Edge service:</span></span>

  - <span data-ttu-id="089b4-p104">内部と外部の両方のポート 443 に対して TCP のネーグル処理がオフになっていること。ネーグル処理はいくつかの小さなパケットを 1 つの大きなパケットにまとめて転送効率を向上させるプロセスです。</span><span class="sxs-lookup"><span data-stu-id="089b4-p104">Turn off TCP nagling for both internal and external ports 443. Nagling is the process of combining several small packets into a single, larger packet for more efficient transmission.</span></span>

  - <span data-ttu-id="089b4-121">外部ポート範囲 50000 ～ 59999 の TCP のネーグル処理がオフになっていること。</span><span class="sxs-lookup"><span data-stu-id="089b4-121">Turn off TCP nagling for external port range 50,000 – 59,999.</span></span>

  - <span data-ttu-id="089b4-122">内部または外部のファイアウォールで NAT が使用されていないこと。</span><span class="sxs-lookup"><span data-stu-id="089b4-122">Do not use NAT on the internal or external firewall.</span></span>

  - <span data-ttu-id="089b4-123">Edge の内部インターフェイスは、エッジサーバーの外部インターフェイスとは異なるネットワーク上にあり、その間のルーティングを無効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="089b4-123">The edge internal interface must be on a different network than the Edge Server external interface and routing between them must be disabled.</span></span>

  - <span data-ttu-id="089b4-124">A/V Edge サービスを実行しているエッジサーバーの外部インターフェイスでは、公開ルーティング可能な IP アドレスを使用し、エッジ外部 IP アドレスには NAT やポートの変換を行わないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="089b4-124">The external interface of the Edge Server running the A/V Edge Service must use publicly routable IP addresses and no NAT or port translation on any of the edge external IP addresses.</span></span>

</div>

<div>

## <a name="hardware-load-balancer-requirements"></a><span data-ttu-id="089b4-125">ロード バランサー機器の要件</span><span class="sxs-lookup"><span data-stu-id="089b4-125">Hardware Load Balancer Requirements</span></span>

<span data-ttu-id="089b4-126">Cookie ベースのアフィニティ要件は、Web サービスの Lync Server 2013 で大幅に削減されます。</span><span class="sxs-lookup"><span data-stu-id="089b4-126">Cookie-based affinity requirements are greatly reduced in Lync Server 2013 for Web services.</span></span> <span data-ttu-id="089b4-127">Lync server 2013 を展開していて、Lync Server 2010 フロントエンドサーバーまたはフロントエンドプールを保持していない場合は、cookie ベースの常設は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="089b4-127">If you are deploying Lync Server 2013 and will not retain any Lync Server 2010 Front End Servers or Front End pools, you do not need cookie-based persistence.</span></span> <span data-ttu-id="089b4-128">ただし、Lync Server 2010 のフロントエンドサーバーまたはフロントエンドプールを一時的または完全に保持する場合でも、Lync Server 2010 用に展開して構成すると、cookie ベースの常設が使用されます。</span><span class="sxs-lookup"><span data-stu-id="089b4-128">However, if you will temporarily or permanently retain any Lync Server 2010 Front End Servers or Front End pools, you still use cookie-based persistence as it is deployed and configured for Lync Server 2010.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="089b4-129"><STRONG>展開では不要だが、Cookie ベースのアフィニティを使用する場合でも</STRONG>、悪影響はありません。</span><span class="sxs-lookup"><span data-stu-id="089b4-129"><STRONG>If you decide to use cookie-based affinity even though your deployment does not require it</STRONG>, there is no negative impact to doing so.</span></span>



</div>

<span data-ttu-id="089b4-130">Cookie ベースのアフィニティを **使用しない** 展開の場合</span><span class="sxs-lookup"><span data-stu-id="089b4-130">For deployments that **will not use** cookie-based affinity:</span></span>

  - <span data-ttu-id="089b4-p106">リバース プロキシのポート 4443 に対する公開ルールで、[**ホスト ヘッダーを転送する**] を True に設定します。これにより、元の URL が確実に転送されます。</span><span class="sxs-lookup"><span data-stu-id="089b4-p106">On the reverse proxy publishing rule for port 4443, set **Forward host header** to True. This will ensure that the original URL is forwarded.</span></span>

<span data-ttu-id="089b4-133">Cookie ベースのアフィニティを **使用する** 展開の場合</span><span class="sxs-lookup"><span data-stu-id="089b4-133">For deployments that **will use** cookie-based affinity:</span></span>

  - <span data-ttu-id="089b4-p107">リバース プロキシのポート 4443 に対する公開ルールで、[**ホスト ヘッダーを転送する**] を True に設定します。これにより、元の URL が確実に転送されます。</span><span class="sxs-lookup"><span data-stu-id="089b4-p107">On the reverse proxy publishing rule for port 4443, set **Forward host header** to True. This will ensure that the original URL is forwarded.</span></span>

  - <span data-ttu-id="089b4-136">ロード バランサー機器 Cookie が httpOnly とマークされていないこと</span><span class="sxs-lookup"><span data-stu-id="089b4-136">Hardware load balancer cookie MUST NOT be marked httpOnly</span></span>

  - <span data-ttu-id="089b4-137">ロード バランサー機器 Cookie に有効期限がないこと</span><span class="sxs-lookup"><span data-stu-id="089b4-137">Hardware load balancer cookie MUST NOT have an expiration time</span></span>

  - <span data-ttu-id="089b4-138">ロード バランサー機器 Cookie の名前が **MS-WSMAN** であること (これは Web サービスが受け取ることを想定している値であり、変更できません)</span><span class="sxs-lookup"><span data-stu-id="089b4-138">Hardware load balancer cookie MUST be named **MS-WSMAN** (This is the value that the Web services expect, and cannot be changed)</span></span>

  - <span data-ttu-id="089b4-p108">ロード バランサー機器着信 HTTP 要求に Cookie が含まれていなかったすべての HTTP 応答に Cookie が設定されていること。同じ TCP 接続での以前の HTTP 応答で Cookie が既に取得されているかどうかは関係ありません。ロード バランサーによって、Cookie の挿入が TCP 接続ごとに 1 回のみ行われるように最適化されている場合は、その最適化を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="089b4-p108">Hardware load balancer cookie MUST be set in every HTTP response for which the incoming HTTP request did not have a cookie, regardless of whether a previous HTTP response on that same TCP connection had already obtained a cookie. If the load balancer optimizes cookie insert to only occur once per TCP connection, that optimization MUST NOT be used</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="089b4-141">一般的なハードウェアロードバランサー構成では、ソースアドレスのアフィニティと20分の TCP セッションの有効期限が使用されます。これは、クライアントの使用状況やアプリケーションの操作によってセッションの状態が維持されるため、Lync Server と Lync 2013 クライアントにとって適切です。</span><span class="sxs-lookup"><span data-stu-id="089b4-141">Typical hardware load balancer configurations use source-address affinity and a 20 min. TCP session lifetime, which is fine for Lync Server and Lync 2013 clients because session state is maintained through client usage and/or and application interaction.</span></span>



</div>

<span data-ttu-id="089b4-142">モバイル デバイスを展開する場合、ロード バランサー機器で、TCP セッション内の個々の要求を負荷分散できるようにする必要があります (実際には、ターゲット IP アドレスに基づいて個々の要求を負荷分散できる必要があります)。</span><span class="sxs-lookup"><span data-stu-id="089b4-142">If you are deploying mobile devices, your hardware load balancer must be able to load balance individual request within a TCP session (in effect, you must be able to load balance an individual request based on the target IP address).</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="089b4-p109">F5 ロード バランサー機器には、OneConnect と呼ばれる機能があります。この機能を使用すると、TCP 接続内の各要求が個々に負荷分散されます。モバイル デバイスを展開する場合、ロード バランサー機器のベンダーが同じ機能をサポートしていることを確認してください。最新の Apple iOS モバイル アプリでは、トランスポート層セキュリティ (TLS) v1.2 が必要です。F5 は、その固有の設定を備えています。</span><span class="sxs-lookup"><span data-stu-id="089b4-p109">F5 hardware load balancers have a feature called OneConnect that ensures each request within a TCP connection is individually load balanced. If you are deploying mobile devices, ensure your hardware load balancer vendor supports the same functionality. The latest Apple iOS mobile apps require Transport Layer Security (TLS) version 1.2. F5 provides specific settings for this.</span></span><BR><span data-ttu-id="089b4-147">サードパーティのハードウェアロードバランサーの詳細については、 <A href="https://go.microsoft.com/fwlink/p/?linkid=230700">https://go.microsoft.com/fwlink/p/?linkId=230700</A></span><span class="sxs-lookup"><span data-stu-id="089b4-147">For details on third party hardware load balancers, see <A href="https://go.microsoft.com/fwlink/p/?linkid=230700">https://go.microsoft.com/fwlink/p/?linkId=230700</A></span></span>



</div>

<span data-ttu-id="089b4-148">ディレクターおよびフロントエンド プールの Web サービスに対するロード バランサー機器の要件は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="089b4-148">Following are the hardware load balancer requirements for Director and Front End pool Web Services:</span></span>

  - <span data-ttu-id="089b4-149">内部の Web サービス Vip では、 \_ ハードウェアのロードバランサーでソースアドレスの常設 (内部ポート80、443) を設定します。</span><span class="sxs-lookup"><span data-stu-id="089b4-149">For internal Web Services VIPs, set Source\_addr persistence (internal port 80, 443) on the hardware load balancer.</span></span> <span data-ttu-id="089b4-150">Lync Server 2013 の場合、ソース \_ アドレス常設は、1つの IP アドレスからの複数の接続が常に1つのサーバーに送信され、セッションの状態を維持することを意味します。</span><span class="sxs-lookup"><span data-stu-id="089b4-150">For Lync Server 2013, Source\_addr persistence means that multiple connections coming from a single IP address are always sent to one server to maintain session state.</span></span>

  - <span data-ttu-id="089b4-151">TCP アイドル タイムアウトが 1800 秒に設定されていること</span><span class="sxs-lookup"><span data-stu-id="089b4-151">Use TCP idle timeout of 1800 seconds.</span></span>

  - <span data-ttu-id="089b4-p111">リバース プロキシと次ホップ プールのロード バランサー機器間のファイアウォールで、リバース プロキシからロード バランサー機器へのポート 4443 に対する https: トラフィックを許可するルールが作成されていること。ポート 80、443、および 4443 をリッスンするようにロード バランサー機器を構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="089b4-p111">On the firewall between the reverse proxy and the next hop pool’s hardware load balancer, create a rule to allow https: traffic on port 4443, from the reverse proxy to the hardware load balancer. The hardware load balancer must be configured to listen on ports 80, 443, and 4443.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="089b4-154">ハードウェアロードバランサーの構成の詳細については、「 <A href="lync-server-2013-port-summary-scaled-consolidated-edge-with-hardware-load-balancers.md">ポートの概要-Lync Server 2013 でハードウェアロードバランサーを使用して拡大縮小されたエッジを</A>確認する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="089b4-154">For further reading on configuration of the hardware load balancer, please review <A href="lync-server-2013-port-summary-scaled-consolidated-edge-with-hardware-load-balancers.md">Port summary - Scaled consolidated edge with hardware load balancers in Lync Server 2013</A>.</span></span>



</div>

</div>

<div>

## <a name="summary-of-hardware-load-balancer-affinity-requirements"></a><span data-ttu-id="089b4-155">ロード バランサー機器のアフィニティ要件の概要</span><span class="sxs-lookup"><span data-stu-id="089b4-155">Summary of Hardware Load Balancer Affinity Requirements</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="089b4-156">クライアント/ユーザーの場所</span><span class="sxs-lookup"><span data-stu-id="089b4-156">Client/user location</span></span></th>
<th><span data-ttu-id="089b4-157">外部 Web サービスの FQDN のアフィニティ要件</span><span class="sxs-lookup"><span data-stu-id="089b4-157">External web services FQDN affinity requirements</span></span></th>
<th><span data-ttu-id="089b4-158">内部 Web サービスの FQDN のアフィニティ要件</span><span class="sxs-lookup"><span data-stu-id="089b4-158">Internal web services FQDN affinity requirements</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="089b4-159">Lync Web App (内部と外部のユーザー)</span><span class="sxs-lookup"><span data-stu-id="089b4-159">Lync Web App (internal and external users)</span></span></p>
<p><span data-ttu-id="089b4-160">モバイル デバイス (内部および外部ユーザー)</span><span class="sxs-lookup"><span data-stu-id="089b4-160">Mobile device (internal and external users)</span></span></p></td>
<td><p><span data-ttu-id="089b4-161">アフィニティなし</span><span class="sxs-lookup"><span data-stu-id="089b4-161">No affinity</span></span></p></td>
<td><p><span data-ttu-id="089b4-162">送信元アドレスのアフィニティ</span><span class="sxs-lookup"><span data-stu-id="089b4-162">Source address affinity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="089b4-163">Lync Web App (外部ユーザーのみ)</span><span class="sxs-lookup"><span data-stu-id="089b4-163">Lync Web App (external users only)</span></span></p>
<p><span data-ttu-id="089b4-164">モバイル デバイス (内部および外部ユーザー)</span><span class="sxs-lookup"><span data-stu-id="089b4-164">Mobile device (internal and external users)</span></span></p></td>
<td><p><span data-ttu-id="089b4-165">アフィニティなし</span><span class="sxs-lookup"><span data-stu-id="089b4-165">No affinity</span></span></p></td>
<td><p><span data-ttu-id="089b4-166">送信元アドレスのアフィニティ</span><span class="sxs-lookup"><span data-stu-id="089b4-166">Source address affinity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="089b4-167">Lync Web App (内部ユーザーのみ)</span><span class="sxs-lookup"><span data-stu-id="089b4-167">Lync Web App (internal users only)</span></span></p>
<p><span data-ttu-id="089b4-168">モバイル デバイス (展開しない)</span><span class="sxs-lookup"><span data-stu-id="089b4-168">Mobile device (not deployed)</span></span></p></td>
<td><p><span data-ttu-id="089b4-169">アフィニティなし</span><span class="sxs-lookup"><span data-stu-id="089b4-169">No affinity</span></span></p></td>
<td><p><span data-ttu-id="089b4-170">送信元アドレスのアフィニティ</span><span class="sxs-lookup"><span data-stu-id="089b4-170">Source address affinity</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="port-monitoring-for-hardware-load-balancers"></a><span data-ttu-id="089b4-171">ロード バランサー機器のポート監視</span><span class="sxs-lookup"><span data-stu-id="089b4-171">Port Monitoring for Hardware Load Balancers</span></span>

<span data-ttu-id="089b4-172">特定のサービスがハードウェアまたは通信障害によって使用できないような状況を確認する目的で、ロード バランサー機器に対してポート監視を定義します。</span><span class="sxs-lookup"><span data-stu-id="089b4-172">You define port monitoring on the hardware load balancers to determine when specific services are no longer available due to hardware or communications failure.</span></span> <span data-ttu-id="089b4-173">たとえば、フロントエンドサーバーまたはフロントエンドプールに障害が発生したために、フロントエンドサーバーサービス (RTCSRV) が停止した場合、HLB の監視でも Web サービスのトラフィックの受信を停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="089b4-173">For example, if the Front End Server service (RTCSRV) stops because the Front End Server or Front End pool fails, the HLB monitoring should also stop receiving traffic on the Web Services.</span></span> <span data-ttu-id="089b4-174">以下を監視する目的で、HLB にポート監視を実装します。</span><span class="sxs-lookup"><span data-stu-id="089b4-174">You implement port monitoring on the HLB to monitor the following:</span></span>

### <a name="front-end-server-user-pool--hlb-internal-interface"></a><span data-ttu-id="089b4-175">フロントエンドサーバーのユーザープール– HLB 内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="089b4-175">Front End Server User Pool – HLB Internal Interface</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="089b4-176">仮想 IP/ポート</span><span class="sxs-lookup"><span data-stu-id="089b4-176">Virtual IP/Port</span></span></th>
<th><span data-ttu-id="089b4-177">ノード ポート</span><span class="sxs-lookup"><span data-stu-id="089b4-177">Node Port</span></span></th>
<th><span data-ttu-id="089b4-178">ノード コンピューター/モニター</span><span class="sxs-lookup"><span data-stu-id="089b4-178">Node Machine/Monitor</span></span></th>
<th><span data-ttu-id="089b4-179">保存プロファイル</span><span class="sxs-lookup"><span data-stu-id="089b4-179">Persistence Profile</span></span></th>
<th><span data-ttu-id="089b4-180">メモ</span><span class="sxs-lookup"><span data-stu-id="089b4-180">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="089b4-181">&lt;プール &gt; web int_mco_443_vs</span><span class="sxs-lookup"><span data-stu-id="089b4-181">&lt;pool&gt;web-int_mco_443_vs</span></span></p>
<p><span data-ttu-id="089b4-182">443</span><span class="sxs-lookup"><span data-stu-id="089b4-182">443</span></span></p></td>
<td><p><span data-ttu-id="089b4-183">443</span><span class="sxs-lookup"><span data-stu-id="089b4-183">443</span></span></p></td>
<td><p><span data-ttu-id="089b4-184">フロントエンド</span><span class="sxs-lookup"><span data-stu-id="089b4-184">Front End</span></span></p>
<p><span data-ttu-id="089b4-185">5061</span><span class="sxs-lookup"><span data-stu-id="089b4-185">5061</span></span></p></td>
<td><p><span data-ttu-id="089b4-186">ソース</span><span class="sxs-lookup"><span data-stu-id="089b4-186">Source</span></span></p></td>
<td><p><span data-ttu-id="089b4-187">HTTPS</span><span class="sxs-lookup"><span data-stu-id="089b4-187">HTTPS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="089b4-188">&lt;プール &gt; web int_mco_80_vs</span><span class="sxs-lookup"><span data-stu-id="089b4-188">&lt;pool&gt;web-int_mco_80_vs</span></span></p>
<p><span data-ttu-id="089b4-189">80</span><span class="sxs-lookup"><span data-stu-id="089b4-189">80</span></span></p></td>
<td><p><span data-ttu-id="089b4-190">80</span><span class="sxs-lookup"><span data-stu-id="089b4-190">80</span></span></p></td>
<td><p><span data-ttu-id="089b4-191">フロントエンド</span><span class="sxs-lookup"><span data-stu-id="089b4-191">Front End</span></span></p>
<p><span data-ttu-id="089b4-192">5061</span><span class="sxs-lookup"><span data-stu-id="089b4-192">5061</span></span></p></td>
<td><p><span data-ttu-id="089b4-193">ソース</span><span class="sxs-lookup"><span data-stu-id="089b4-193">Source</span></span></p></td>
<td><p><span data-ttu-id="089b4-194">HTTP</span><span class="sxs-lookup"><span data-stu-id="089b4-194">HTTP</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="front-end-server-user-pool--hlb-external-interface"></a><span data-ttu-id="089b4-195">フロントエンドサーバーのユーザープール– HLB 外部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="089b4-195">Front End Server User Pool – HLB External Interface</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="089b4-196">仮想 IP/ポート</span><span class="sxs-lookup"><span data-stu-id="089b4-196">Virtual IP/Port</span></span></th>
<th><span data-ttu-id="089b4-197">ノード ポート</span><span class="sxs-lookup"><span data-stu-id="089b4-197">Node Port</span></span></th>
<th><span data-ttu-id="089b4-198">ノード コンピューター/モニター</span><span class="sxs-lookup"><span data-stu-id="089b4-198">Node Machine/Monitor</span></span></th>
<th><span data-ttu-id="089b4-199">保存プロファイル</span><span class="sxs-lookup"><span data-stu-id="089b4-199">Persistence Profile</span></span></th>
<th><span data-ttu-id="089b4-200">メモ</span><span class="sxs-lookup"><span data-stu-id="089b4-200">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="089b4-201">&lt;プール &gt; web_mco_443_vs</span><span class="sxs-lookup"><span data-stu-id="089b4-201">&lt;pool&gt;web_mco_443_vs</span></span></p>
<p><span data-ttu-id="089b4-202">443</span><span class="sxs-lookup"><span data-stu-id="089b4-202">443</span></span></p></td>
<td><p><span data-ttu-id="089b4-203">4443</span><span class="sxs-lookup"><span data-stu-id="089b4-203">4443</span></span></p></td>
<td><p><span data-ttu-id="089b4-204">フロントエンド</span><span class="sxs-lookup"><span data-stu-id="089b4-204">Front End</span></span></p>
<p><span data-ttu-id="089b4-205">5061</span><span class="sxs-lookup"><span data-stu-id="089b4-205">5061</span></span></p></td>
<td><p><span data-ttu-id="089b4-206">なし</span><span class="sxs-lookup"><span data-stu-id="089b4-206">None</span></span></p></td>
<td><p><span data-ttu-id="089b4-207">HTTPS</span><span class="sxs-lookup"><span data-stu-id="089b4-207">HTTPS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="089b4-208">&lt;プール &gt; web_mco_80_vs</span><span class="sxs-lookup"><span data-stu-id="089b4-208">&lt;pool&gt;web_mco_80_vs</span></span></p>
<p><span data-ttu-id="089b4-209">80</span><span class="sxs-lookup"><span data-stu-id="089b4-209">80</span></span></p></td>
<td><p><span data-ttu-id="089b4-210">8080</span><span class="sxs-lookup"><span data-stu-id="089b4-210">8080</span></span></p></td>
<td><p><span data-ttu-id="089b4-211">フロントエンド</span><span class="sxs-lookup"><span data-stu-id="089b4-211">Front End</span></span></p>
<p><span data-ttu-id="089b4-212">5061</span><span class="sxs-lookup"><span data-stu-id="089b4-212">5061</span></span></p></td>
<td><p><span data-ttu-id="089b4-213">なし</span><span class="sxs-lookup"><span data-stu-id="089b4-213">None</span></span></p></td>
<td><p><span data-ttu-id="089b4-214">HTTP</span><span class="sxs-lookup"><span data-stu-id="089b4-214">HTTP</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="089b4-215">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="089b4-215">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

