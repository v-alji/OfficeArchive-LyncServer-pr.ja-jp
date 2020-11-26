---
title: 'Lync Server 2013: DNS の概要 - 拡張統合エッジ、NAT によるプライベート IP アドレスを使用した DNS 負荷分散'
description: 'Lync Server 2013: DNS の概要-拡張された統合エッジ、NAT を使用したプライベート IP アドレスを使った DNS の負荷分散。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - Scaled consolidated edge, DNS load balancing with private IP addresses using NAT
ms:assetid: 11bc7b84-91cf-48f9-ad0e-06ad30b46a2e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398201(v=OCS.15)
ms:contentKeyID: 48183447
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2eef3029323c1c2f798fddc721df832a932524c8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437708"
---
# <a name="dns-summary---scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat-in-lync-server-2013"></a><span data-ttu-id="3f371-103">DNS の概要 - Lync Server 2013 での拡張統合エッジ、NAT によるプライベート IP アドレスを使用した DNS 負荷分散</span><span class="sxs-lookup"><span data-stu-id="3f371-103">DNS summary - Scaled consolidated edge, DNS load balancing with private IP addresses using NAT in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3f371-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3f371-104">

<span> </span></span></span>

<span data-ttu-id="3f371-105">_**最終更新日:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="3f371-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="3f371-106">Lync Server 2013 へのリモートアクセスの DNS レコード要件は、証明書やポートの場合と非常に簡単です。</span><span class="sxs-lookup"><span data-stu-id="3f371-106">DNS record requirements for remote access to Lync Server 2013 are fairly straightforward compared to those for certificates and ports.</span></span> <span data-ttu-id="3f371-107">また、Lync 2013 を実行しているクライアントの構成方法とフェデレーションを有効にするかどうかによって、多くのレコードがオプションになります。</span><span class="sxs-lookup"><span data-stu-id="3f371-107">Also, many records are optional, depending on how you configure clients running Lync 2013 and whether you enable federation.</span></span>

<span data-ttu-id="3f371-108">Lync 2013 DNS の要件の詳細については、「 [Lync Server 2013 の dns 要件を確認](lync-server-2013-determine-dns-requirements.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3f371-108">For details about Lync 2013 DNS requirements, see [Determine DNS requirements for Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span></span>

<span data-ttu-id="3f371-109">Lync 2013 クライアントの自動構成の構成の詳細については、「 [Lync Server 2013 の DNS 要件を特定](lync-server-2013-determine-dns-requirements.md)する」の「スプリットブレイン dns を使わない自動構成」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3f371-109">For details about configuring automatic configuration of Lync 2013 clients if split-brain DNS is not configured, see the "Automatic Configuration without Split Brain DNS" section in [Determine DNS requirements for Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span></span>

<span data-ttu-id="3f371-110">次の表には、単一の統合されたエッジトポロジの図に示されている単一の統合エッジトポロジをサポートするために必要な DNS レコードの概要を示します。</span><span class="sxs-lookup"><span data-stu-id="3f371-110">The following table contains a summary of the DNS records that are required to support the single consolidated edge topology shown in the Single Consolidated Edge Topology figure.</span></span> <span data-ttu-id="3f371-111">特定の DNS レコードは、Lync 2013 クライアントの自動構成にのみ必要であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="3f371-111">Note that certain DNS records are required only for automatic configuration of Lync 2013 clients.</span></span> <span data-ttu-id="3f371-112">グループポリシーオブジェクト (Gpo) を使って Lync クライアントを構成することを計画している場合は、関連付けられたレコードは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="3f371-112">If you plan to use group policy objects (GPOs) to configure Lync clients, the associated records are not necessary.</span></span>

<div>

## <a name="important-edge-server-network-adapter-requirements"></a><span data-ttu-id="3f371-113">重要: エッジサーバーのネットワークアダプターの要件</span><span class="sxs-lookup"><span data-stu-id="3f371-113">IMPORTANT: Edge Server Network Adapter Requirements</span></span>

<span data-ttu-id="3f371-114">ルーティングの問題を回避するには、エッジサーバーに少なくとも2つのネットワークアダプターがあり、その外部インターフェイスに関連付けられているネットワークアダプターでのみ既定のゲートウェイが設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="3f371-114">To avoid routing issues, verify that there are at least two network adapters in your Edge Servers and that the default gateway is set only on the network adapter associated with the external interface.</span></span> <span data-ttu-id="3f371-115">たとえば、スケーリングされた統合エッジシナリオの図では、拡大縮小された統合エッジ [、Lync Server 2013 の NAT を使用したプライベート IP アドレスを使った DNS の負荷分散](lync-server-2013-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat.md)は、既定のゲートウェイで外部ファイアウォールをポイントしています。</span><span class="sxs-lookup"><span data-stu-id="3f371-115">For example, as shown in the Scaled Consolidated Edge Scenario figure in [Scaled consolidated edge, DNS load balancing with private IP addresses using NAT in Lync Server 2013](lync-server-2013-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat.md), the default gateway would point to the external firewall.</span></span>

<span data-ttu-id="3f371-116">次のように、各エッジサーバーで2つのネットワークアダプターを構成できます。</span><span class="sxs-lookup"><span data-stu-id="3f371-116">You can configure two network adapters in each of your Edge Server as follows:</span></span>

  - <span data-ttu-id="3f371-117">**ネットワークアダプター 1-ノード 1 (内部インターフェイス)**</span><span class="sxs-lookup"><span data-stu-id="3f371-117">**Network adapter 1 - Node 1 (Internal Interface)**</span></span>
    
    <span data-ttu-id="3f371-118">172.25.33.10 が割り当てられている内部インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="3f371-118">Internal interface with 172.25.33.10 assigned.</span></span>
    
    <span data-ttu-id="3f371-119">既定のゲートウェイは定義されていません。</span><span class="sxs-lookup"><span data-stu-id="3f371-119">No default gateway is defined.</span></span>
    
    <span data-ttu-id="3f371-120">Lync Server 2013 または Lync Server 2013 クライアントを実行しているサーバー (172.25.33.0 から192.168.10.0 など) が含まれているすべてのネットワークへの Edge 内部インターフェイスが含まれているネットワークからのルートがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="3f371-120">Ensure that there is a route from the network containing the Edge internal interface to any networks that contain servers running Lync Server 2013 or Lync Server 2013 clients (for example, from 172.25.33.0 to 192.168.10.0).</span></span>

  - <span data-ttu-id="3f371-121">**ネットワークアダプター 1-ノード 2 (内部インターフェイス)**</span><span class="sxs-lookup"><span data-stu-id="3f371-121">**Network adapter 1 - Node 2 (Internal Interface)**</span></span>
    
    <span data-ttu-id="3f371-122">172.25.33.11 が割り当てられている内部インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="3f371-122">Internal interface with 172.25.33.11 assigned.</span></span>
    
    <span data-ttu-id="3f371-123">既定のゲートウェイは定義されていません。</span><span class="sxs-lookup"><span data-stu-id="3f371-123">No default gateway is defined.</span></span>
    
    <span data-ttu-id="3f371-124">Lync Server 2013 または Lync Server 2013 クライアントを実行しているサーバー (172.25.33.0 から192.168.10.0 など) が含まれているすべてのネットワークへの Edge 内部インターフェイスが含まれているネットワークからのルートがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="3f371-124">Ensure that there is a route from the network containing the Edge internal interface to any networks that contain servers running Lync Server 2013 or Lync Server 2013 clients (for example, from 172.25.33.0 to 192.168.10.0).</span></span>

  - <span data-ttu-id="3f371-125">**ネットワークアダプター2ノード 1 (外部インターフェイス)**</span><span class="sxs-lookup"><span data-stu-id="3f371-125">**Network adapter 2 Node 1 (External Interface)**</span></span>
    
    <span data-ttu-id="3f371-126">3つのプライベート IP アドレスがこのネットワークアダプターに割り当てられます。たとえば、Access Edge の場合は10.45.16.10、Web 会議エッジの場合は10.45.16.20、AV Edge の場合は10.45.16.30 です。</span><span class="sxs-lookup"><span data-stu-id="3f371-126">Three private IP addresses are assigned to this network adapter, for example 10.45.16.10 for Access Edge, 10.45.16.20 for Web Conferencing Edge, 10.45.16.30 for AV Edge.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="3f371-127">すべての3エッジサービスインターフェイスで単一の IP アドレスを使うことはできますが、お勧めしません。</span><span class="sxs-lookup"><span data-stu-id="3f371-127">It is possible, though not recommended, to use a single IP address for all three Edge service interfaces.</span></span> <span data-ttu-id="3f371-128">これにより、IP アドレスが保存されますが、サービスごとに異なるポート番号が必要になります。</span><span class="sxs-lookup"><span data-stu-id="3f371-128">Though this does save IP addresses, it requires different port numbers for each service.</span></span> <span data-ttu-id="3f371-129">既定のポート番号は 443/TCP であり、ほとんどのリモートファイアウォールでトラフィックが許可されます。</span><span class="sxs-lookup"><span data-stu-id="3f371-129">The default port number is 443/TCP, which ensures that most remote firewalls will allow the traffic.</span></span> <span data-ttu-id="3f371-130">ポートの値を変更する (たとえば、アクセスエッジの場合は 5061/tcp、Web 会議エッジの場合は 444/TCP、AV Edge の場合は、ファイアウォールを使用しているファイアウォールでは 5061/tcp および 444/TCP 経由のトラフィックが許可されていないことがあります)。</span><span class="sxs-lookup"><span data-stu-id="3f371-130">Changing the port values to (for example) 5061/TCP for the Access Edge, 444/TCP for the Web Conferencing Edge and 443/TCP for the AV Edge might cause problems for remote users where a firewall that they are behind does not allow the traffic over 5061/TCP and 444/TCP.</span></span> <span data-ttu-id="3f371-131">さらに、3つの異なる IP アドレスで、IP アドレスをフィルター処理できるため、トラブルシューティングが容易になります。</span><span class="sxs-lookup"><span data-stu-id="3f371-131">Additionally, three distinct IP addresses makes troubleshooting easier due to being able to filter on IP address.</span></span>

    
    </div>
    
    <span data-ttu-id="3f371-132">アクセスエッジのパブリック IP アドレスは、統合ルータ (10.45.16.1) に設定されたデフォルトゲートウェイのプライマリ IP アドレスです。</span><span class="sxs-lookup"><span data-stu-id="3f371-132">The Access Edge public IP address is primary with default gateway set to the integrated router (10.45.16.1).</span></span>
    
    <span data-ttu-id="3f371-133">Web 会議と A/V Edge のプライベート IP アドレスは、Windows Server の **ローカルエリア接続プロパティ** の **インターネットプロトコルバージョン 4 (tcp/IPv4)** および **インターネットプロトコルバージョン 6 (tcp/IPv6)** のプロパティの **[詳細設定**] セクションで追加の ip アドレスとなります。</span><span class="sxs-lookup"><span data-stu-id="3f371-133">Web conferencing and A/V Edge private IP addresses are additional IP addresses in the **Advanced** section of the properties of **Internet Protocol Version 4 (TCP/IPv4)** and **Internet Protocol Version 6 (TCP/IPv6)** of the **Local Area Connection Properties** in Windows Server.</span></span>

  - <span data-ttu-id="3f371-134">**ネットワークアダプター2ノード 2 (外部インターフェイス)**</span><span class="sxs-lookup"><span data-stu-id="3f371-134">**Network adapter 2 Node 2 (External Interface)**</span></span>
    
    <span data-ttu-id="3f371-135">3つのプライベート IP アドレスがこのネットワークアダプターに割り当てられます。たとえば、Access Edge の場合は10.45.16.11、Web 会議エッジの場合は10.45.16.21、AV Edge の場合は10.45.16.31 です。</span><span class="sxs-lookup"><span data-stu-id="3f371-135">Three private IP addresses are assigned to this network adapter, for example 10.45.16.11 for Access Edge, 10.45.16.21 for Web Conferencing Edge, 10.45.16.31 for AV Edge.</span></span>
    
    <span data-ttu-id="3f371-136">アクセスエッジのパブリック IP アドレスは、統合ルータ (10.45.16.1) に設定されたデフォルトゲートウェイのプライマリ IP アドレスです。</span><span class="sxs-lookup"><span data-stu-id="3f371-136">The Access Edge public IP address is primary with default gateway set to the integrated router (10.45.16.1).</span></span>
    
    <span data-ttu-id="3f371-137">Web 会議と A/V Edge のプライベート IP アドレスは、Windows Server の **ローカルエリア接続プロパティ** の **インターネットプロトコルバージョン 4 (tcp/IPv4)** および **インターネットプロトコルバージョン 6 (tcp/IPv6)** のプロパティの **[詳細設定**] セクションで追加の ip アドレスとなります。</span><span class="sxs-lookup"><span data-stu-id="3f371-137">Web conferencing and A/V Edge private IP addresses are additional IP addresses in the **Advanced** section of the properties of **Internet Protocol Version 4 (TCP/IPv4)** and **Internet Protocol Version 6 (TCP/IPv6)** of the **Local Area Connection Properties** in Windows Server.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="3f371-138">2つのネットワークアダプターでエッジサーバーを構成するには、2つのオプションのいずれかを使用します。</span><span class="sxs-lookup"><span data-stu-id="3f371-138">Configuring the Edge Server with two network adapters is one of two options.</span></span> <span data-ttu-id="3f371-139">もう1つの方法として、内部側とエッジサーバーの外部側の3つのネットワークアダプター用に1つのネットワークアダプターを使うことができます。</span><span class="sxs-lookup"><span data-stu-id="3f371-139">The other option is to use one network adapter for the internal side and three network adapters for the external side of the Edge Server.</span></span> <span data-ttu-id="3f371-140">このオプションの主な利点は、Edge Server サービスごとの個別のネットワークアダプターであり、トラブルシューティングが必要な場合は、より簡潔なデータ収集を行うことです。</span><span class="sxs-lookup"><span data-stu-id="3f371-140">The main benefit of this option is a distinct network adapter per Edge Server service, and potentially more concise data collection when troubleshooting is necessary</span></span>



</div>

### <a name="dns-records-required-for-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat-example"></a><span data-ttu-id="3f371-141">スケーリングされた統合エッジに必要な DNS レコード、NAT を使ったプライベート IP アドレスによる DNS の負荷分散 (例)</span><span class="sxs-lookup"><span data-stu-id="3f371-141">DNS Records Required for Scaled Consolidated Edge, DNS Load Balancing with Private IP Addresses Using NAT (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3f371-142">場所/種類/ポート</span><span class="sxs-lookup"><span data-stu-id="3f371-142">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="3f371-143">FQDN/DNS レコード</span><span class="sxs-lookup"><span data-stu-id="3f371-143">FQDN/DNS Record</span></span></th>
<th><span data-ttu-id="3f371-144">IP アドレス/FQDN</span><span class="sxs-lookup"><span data-stu-id="3f371-144">IP Address/FQDN</span></span></th>
<th><span data-ttu-id="3f371-145">マップ先/コメント</span><span class="sxs-lookup"><span data-stu-id="3f371-145">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3f371-146">外部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="3f371-146">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="3f371-147">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="3f371-147">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="3f371-148">131.107.155.10 および 131.107.155.11</span><span class="sxs-lookup"><span data-stu-id="3f371-148">131.107.155.10 and 131.107.155.11</span></span></p></td>
<td><p><span data-ttu-id="3f371-149">Access Edge の外部インターフェイス (Contoso) は、Lync が有効になっているユーザーがいるすべての SIP ドメインについて、必要に応じて繰り返す</span><span class="sxs-lookup"><span data-stu-id="3f371-149">Access Edge external interface (Contoso) Repeat as necessary for all SIP domains with Lync enabled users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f371-150">外部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="3f371-150">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="3f371-151">webcon.contoso.com</span><span class="sxs-lookup"><span data-stu-id="3f371-151">webcon.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="3f371-152">131.107.155.20 および 131.107.155.21</span><span class="sxs-lookup"><span data-stu-id="3f371-152">131.107.155.20 and 131.107.155.21</span></span></p></td>
<td><p><span data-ttu-id="3f371-153">Web 会議エッジの外部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="3f371-153">Web Conferencing Edge external interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f371-154">外部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="3f371-154">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="3f371-155">av.contoso.com</span><span class="sxs-lookup"><span data-stu-id="3f371-155">av.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="3f371-156">131.107.155.30 および 131.107.155.31</span><span class="sxs-lookup"><span data-stu-id="3f371-156">131.107.155.30 and 131.107.155.31</span></span></p></td>
<td><p><span data-ttu-id="3f371-157">A/V Edge の外部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="3f371-157">A/V Edge external interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f371-158">外部 DNS/SRV/443</span><span class="sxs-lookup"><span data-stu-id="3f371-158">External DNS/SRV/443</span></span></p></td>
<td><p><span data-ttu-id="3f371-159">_sip._tls.contoso.com</span><span class="sxs-lookup"><span data-stu-id="3f371-159">_sip._tls.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="3f371-160">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="3f371-160">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="3f371-161">Access Edge の外部インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="3f371-161">Access Edge external interface.</span></span> <span data-ttu-id="3f371-162">Lync 2013 および Lync 2010 クライアントを外部で動作させるために、自動構成が必要です。</span><span class="sxs-lookup"><span data-stu-id="3f371-162">Required for automatic configuration of Lync 2013 and Lync 2010 clients to work externally.</span></span> <span data-ttu-id="3f371-163">Lync が有効になっているユーザーがいるすべての SIP ドメインで、必要に応じてこの手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="3f371-163">Repeat as necessary for all SIP domains with Lync enabled users.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f371-164">外部 DNS/SRV/5061</span><span class="sxs-lookup"><span data-stu-id="3f371-164">External DNS/SRV/5061</span></span></p></td>
<td><p><span data-ttu-id="3f371-165">_sipfederationtls._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="3f371-165">_sipfederationtls._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="3f371-166">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="3f371-166">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="3f371-167">SIP アクセスエッジ外部インタフェース。</span><span class="sxs-lookup"><span data-stu-id="3f371-167">SIP Access Edge external interface.</span></span> <span data-ttu-id="3f371-168">"許可された SIP ドメイン" と呼ばれるフェデレーションパートナー (以前のリリースで拡張フェデレーションと呼ばれる) を自動的に検出するために必要です。</span><span class="sxs-lookup"><span data-stu-id="3f371-168">Required for automatic DNS discovery of federated partners known as “Allowed SIP Domain” (called enhanced federation in previous releases).</span></span> <span data-ttu-id="3f371-169">Lync を有効にしたユーザーがいるすべての SIP ドメインで、必要に応じて繰り返す</span><span class="sxs-lookup"><span data-stu-id="3f371-169">Repeat as necessary for all SIP domains with Lync enabled users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f371-170">内部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="3f371-170">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="3f371-171">lsedge.contoso.net</span><span class="sxs-lookup"><span data-stu-id="3f371-171">lsedge.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="3f371-172">172.25.33.10 および 172.25.33.11</span><span class="sxs-lookup"><span data-stu-id="3f371-172">172.25.33.10 and 172.25.33.11</span></span></p></td>
<td><p><span data-ttu-id="3f371-173">統合エッジ内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="3f371-173">Consolidated Edge internal interface</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="records-required-for-federation"></a><span data-ttu-id="3f371-174">フェデレーションに必要なレコード</span><span class="sxs-lookup"><span data-stu-id="3f371-174">Records Required for Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3f371-175">場所/種類/ポート</span><span class="sxs-lookup"><span data-stu-id="3f371-175">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="3f371-176">FQDN</span><span class="sxs-lookup"><span data-stu-id="3f371-176">FQDN</span></span></th>
<th><span data-ttu-id="3f371-177">IP アドレス/FQDN ホストレコード</span><span class="sxs-lookup"><span data-stu-id="3f371-177">IP address/FQDN host record</span></span></th>
<th><span data-ttu-id="3f371-178">マップ先/コメント</span><span class="sxs-lookup"><span data-stu-id="3f371-178">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3f371-179">外部 DNS/SRV/5061</span><span class="sxs-lookup"><span data-stu-id="3f371-179">External DNS/SRV/5061</span></span></p></td>
<td><p><span data-ttu-id="3f371-180">_sipfederationtls._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="3f371-180">_sipfederationtls._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="3f371-181">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="3f371-181">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="3f371-182">SIP アクセスエッジ外部インタフェースは、他の潜在的なフェデレーションパートナーとのフェデレーションを自動的に検出するために必要です。また、"許可された SIP ドメイン" と呼ばれます (以前のリリースでは拡張フェデレーションと呼ばれます)。Lync を有効にしたユーザーがいるすべての SIP ドメインで、必要に応じて繰り返す</span><span class="sxs-lookup"><span data-stu-id="3f371-182">SIP Access Edge external interface Required for automatic DNS discovery of your federation to other potential federation partners, and is known as “Allowed SIP Domains” (called enhanced federation in previous releases).Repeat as necessary for all SIP domains with Lync enabled users</span></span></p>
<div>

> [!IMPORTANT]  
> <span data-ttu-id="3f371-183">この SRV レコードは、モビリティとプッシュ通知のクリアリングハウスに必要です</span><span class="sxs-lookup"><span data-stu-id="3f371-183">This SRV record is required for mobility and the push notification clearing house</span></span>


</div></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="dns-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="3f371-184">DNS 概要–パブリックインスタントメッセージング接続</span><span class="sxs-lookup"><span data-stu-id="3f371-184">DNS Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3f371-185">場所/種類/ポート</span><span class="sxs-lookup"><span data-stu-id="3f371-185">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="3f371-186">FQDN/DNS レコード</span><span class="sxs-lookup"><span data-stu-id="3f371-186">FQDN/DNS Record</span></span></th>
<th><span data-ttu-id="3f371-187">IP アドレス/FQDN</span><span class="sxs-lookup"><span data-stu-id="3f371-187">IP Address/FQDN</span></span></th>
<th><span data-ttu-id="3f371-188">マップ先/コメント</span><span class="sxs-lookup"><span data-stu-id="3f371-188">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3f371-189">外部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="3f371-189">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="3f371-190">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="3f371-190">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="3f371-191">Access Edge サービスインターフェイス</span><span class="sxs-lookup"><span data-stu-id="3f371-191">Access Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="3f371-192">Access Edge の外部インターフェイス (Contoso) は、Lync が有効になっているユーザーがいるすべての SIP ドメインについて、必要に応じて繰り返す</span><span class="sxs-lookup"><span data-stu-id="3f371-192">Access Edge external interface (Contoso)Repeat as necessary for all SIP domains with Lync enabled users</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="dns-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="3f371-193">拡張メッセージングとプレゼンスプロトコルの DNS 概要</span><span class="sxs-lookup"><span data-stu-id="3f371-193">DNS Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3f371-194">場所/種類/ポート</span><span class="sxs-lookup"><span data-stu-id="3f371-194">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="3f371-195">FQDN</span><span class="sxs-lookup"><span data-stu-id="3f371-195">FQDN</span></span></th>
<th><span data-ttu-id="3f371-196">IP アドレス/FQDN ホストレコード</span><span class="sxs-lookup"><span data-stu-id="3f371-196">IP address/FQDN host record</span></span></th>
<th><span data-ttu-id="3f371-197">マップ先/コメント</span><span class="sxs-lookup"><span data-stu-id="3f371-197">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3f371-198">外部 DNS/SRV/5269</span><span class="sxs-lookup"><span data-stu-id="3f371-198">External DNS/SRV/5269</span></span></p></td>
<td><p><span data-ttu-id="3f371-199">_xmpp-server._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="3f371-199">_xmpp-server._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="3f371-200">xmpp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="3f371-200">xmpp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="3f371-201">アクセスエッジサービスまたはエッジプールの XMPP プロキシ外部インターフェイス。グローバルポリシー、ユーザーが配置されているサイトポリシー、または Lync 対応ユーザーに適用されているユーザーポリシーを通じて、外部アクセスポリシーの構成を通じて、すべての内部 SIP ドメインで、必要に応じてこの手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="3f371-201">XMPP proxy external interface on the Access Edge service or Edge pool.Repeat as necessary for all internal SIP domains with Lync enabled users where contact with XMPP contacts is allowed through the configuration of the External Access Policy through a global policy, site policy where the user is located, or user policy applied to the Lync-enabled user.</span></span> <span data-ttu-id="3f371-202">許可されている XMPP ドメインは、XMPP フェデレーションパートナーポリシーでも構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3f371-202">An allowed XMPP domain must also be configured in the XMPP Federated Partners policy.</span></span> <span data-ttu-id="3f371-203">詳細については、 <strong>「</strong> 関連項目」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3f371-203">See topics in <strong>See Also</strong> for additional details</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f371-204">外部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="3f371-204">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="3f371-205">xmpp.contoso.com (など)</span><span class="sxs-lookup"><span data-stu-id="3f371-205">xmpp.contoso.com (for example)</span></span></p></td>
<td><p><span data-ttu-id="3f371-206">エッジサーバーまたは XMPP プロキシをホストしているエッジプールのアクセスエッジサービスの IP アドレス</span><span class="sxs-lookup"><span data-stu-id="3f371-206">IP address of Access Edge service on your Edge Server or Edge pool hosting XMPP proxy</span></span></p></td>
<td><p><span data-ttu-id="3f371-207">XMPP プロキシサービスをホストしているアクセスエッジサービスまたはエッジプールへのポイント。</span><span class="sxs-lookup"><span data-stu-id="3f371-207">Points to the Access Edge service or Edge pool that hosts the XMPP proxy service.</span></span> <span data-ttu-id="3f371-208">通常、作成した SRV レコードは、このホスト (A または AAAA) レコードをポイントします。</span><span class="sxs-lookup"><span data-stu-id="3f371-208">Typically, the SRV record that you create will point to this host (A or AAAA) record</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="3f371-209">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3f371-209">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

