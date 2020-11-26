---
title: 'Lync Server 2013: DNS の概要 - 拡張統合エッジ、パブリック IP アドレスによる DNS 負荷分散'
description: 'Lync Server 2013: DNS の概要-拡張された統合エッジ、パブリック IP アドレスを使った DNS の負荷分散。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - Scaled consolidated edge, DNS load balancing with public IP addresses
ms:assetid: dc8f096a-a0a4-4f71-8930-88ff8fc089d9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205319(v=OCS.15)
ms:contentKeyID: 48185594
ms.date: 03/09/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ca88043b76365508ea00ca840e9a9fdcb0e270be
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429015"
---
# <a name="dns-summary---scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses-in-lync-server-2013"></a><span data-ttu-id="6c83f-103">DNS の概要 - Lync Server 2013 における拡張統合エッジ、パブリック IP アドレスによる DNS 負荷分散</span><span class="sxs-lookup"><span data-stu-id="6c83f-103">DNS summary - Scaled consolidated edge, DNS load balancing with public IP addresses in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6c83f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6c83f-104">

<span> </span></span></span>

<span data-ttu-id="6c83f-105">_**最終更新日:** 2017-03-09_</span><span class="sxs-lookup"><span data-stu-id="6c83f-105">_**Topic Last Modified:** 2017-03-09_</span></span>

<span data-ttu-id="6c83f-106">Lync Server 2013 へのリモートアクセスの DNS レコード要件は、証明書やポートの場合と非常に簡単です。</span><span class="sxs-lookup"><span data-stu-id="6c83f-106">DNS record requirements for remote access to Lync Server 2013 are fairly straightforward compared to those for certificates and ports.</span></span> <span data-ttu-id="6c83f-107">また、Lync 2013 を実行しているクライアントの構成方法とフェデレーションを有効にするかどうかによって、多くのレコードがオプションになります。</span><span class="sxs-lookup"><span data-stu-id="6c83f-107">Also, many records are optional, depending on how you configure clients running Lync 2013 and whether you enable federation.</span></span>

<span data-ttu-id="6c83f-108">Lync 2013 DNS の要件の詳細については、「 [Lync Server 2013 の dns 要件を確認](lync-server-2013-determine-dns-requirements.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6c83f-108">For details about Lync 2013 DNS requirements, see [Determine DNS requirements for Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span></span>

<span data-ttu-id="6c83f-109">Lync 2013 クライアントの自動構成の構成の詳細については、「 [Lync Server 2013 の DNS 要件を特定](lync-server-2013-determine-dns-requirements.md)する」の「スプリットブレイン dns を使わない自動構成」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6c83f-109">For details about configuring automatic configuration of Lync 2013 clients if split-brain DNS is not configured, see the "Automatic Configuration without Split Brain DNS" section in [Determine DNS requirements for Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span></span>

<span data-ttu-id="6c83f-110">次の表には、単一の統合されたエッジトポロジの図に示されている単一の統合エッジトポロジをサポートするために必要な DNS レコードの概要を示します。</span><span class="sxs-lookup"><span data-stu-id="6c83f-110">The following table contains a summary of the DNS records that are required to support the single consolidated edge topology shown in the Single Consolidated Edge Topology figure.</span></span> <span data-ttu-id="6c83f-111">特定の DNS レコードは、Lync 2013 クライアントの自動構成にのみ必要であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="6c83f-111">Note that certain DNS records are required only for automatic configuration of Lync 2013 clients.</span></span> <span data-ttu-id="6c83f-112">グループポリシーオブジェクト (Gpo) を使って Lync クライアントを構成することを計画している場合は、関連付けられたレコードは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="6c83f-112">If you plan to use group policy objects (GPOs) to configure Lync clients, the associated records are not necessary.</span></span>

<div>

## <a name="important-edge-server-network-adapter-requirements"></a><span data-ttu-id="6c83f-113">重要: エッジサーバーのネットワークアダプターの要件</span><span class="sxs-lookup"><span data-stu-id="6c83f-113">IMPORTANT: Edge Server Network Adapter Requirements</span></span>

<span data-ttu-id="6c83f-114">ルーティングの問題を回避するには、エッジサーバーに少なくとも2つのネットワークアダプターがあり、その外部インターフェイスに関連付けられているネットワークアダプターでのみ既定のゲートウェイが設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6c83f-114">To avoid routing issues, verify that there are at least two network adapters in your Edge Servers and that the default gateway is set only on the network adapter associated with the external interface.</span></span> <span data-ttu-id="6c83f-115">たとえば、スケーリングされた統合エッジシナリオでは、拡大縮小された統合エッジでは、 [Lync Server 2013 でのパブリック IP アドレスを使った DNS 負荷分散](lync-server-2013-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses.md) の場合、既定のゲートウェイは外部ファイアウォールをポイントします。</span><span class="sxs-lookup"><span data-stu-id="6c83f-115">For example, as shown in the Scaled Consolidated Edge Scenario figure in [Scaled consolidated edge, DNS load balancing with public IP addresses in Lync Server 2013](lync-server-2013-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses.md) , the default gateway would point to the external firewall.</span></span>

<span data-ttu-id="6c83f-116">次のように、各エッジサーバーで2つのネットワークアダプターを構成できます。</span><span class="sxs-lookup"><span data-stu-id="6c83f-116">You can configure two network adapters in each of your Edge Server as follows:</span></span>

  - <span data-ttu-id="6c83f-117">**ネットワークアダプター 1-ノード 1 (内部インターフェイス)**</span><span class="sxs-lookup"><span data-stu-id="6c83f-117">**Network adapter 1 - Node 1 (Internal Interface)**</span></span>
    
    <span data-ttu-id="6c83f-118">172.25.33.10 が割り当てられている内部インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="6c83f-118">Internal interface with 172.25.33.10 assigned.</span></span>
    
    <span data-ttu-id="6c83f-119">既定のゲートウェイは定義されていません。</span><span class="sxs-lookup"><span data-stu-id="6c83f-119">No default gateway is defined.</span></span>
    
    <span data-ttu-id="6c83f-120">Lync Server 2013 または Lync Server 2013 クライアントを実行しているサーバー (172.25.33.0 から192.168.10.0 など) が含まれているすべてのネットワークへの Edge 内部インターフェイスが含まれているネットワークからのルートがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6c83f-120">Ensure that there is a route from the network containing the Edge internal interface to any networks that contain servers running Lync Server 2013 or Lync Server 2013 clients (for example, from 172.25.33.0 to 192.168.10.0).</span></span>

  - <span data-ttu-id="6c83f-121">**ネットワークアダプター 1-ノード 2 (内部インターフェイス)**</span><span class="sxs-lookup"><span data-stu-id="6c83f-121">**Network adapter 1 - Node 2 (Internal Interface)**</span></span>
    
    <span data-ttu-id="6c83f-122">172.25.33.11 が割り当てられている内部インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="6c83f-122">Internal interface with 172.25.33.11 assigned.</span></span>
    
    <span data-ttu-id="6c83f-123">既定のゲートウェイは定義されていません。</span><span class="sxs-lookup"><span data-stu-id="6c83f-123">No default gateway is defined.</span></span>
    
    <span data-ttu-id="6c83f-124">Lync Server 2013 または Lync Server 2013 クライアントを実行しているサーバー (172.25.33.0 から192.168.10.0 など) が含まれているすべてのネットワークへの Edge 内部インターフェイスが含まれているネットワークからのルートがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6c83f-124">Ensure that there is a route from the network containing the Edge internal interface to any networks that contain servers running Lync Server 2013 or Lync Server 2013 clients (for example, from 172.25.33.0 to 192.168.10.0).</span></span>

  - <span data-ttu-id="6c83f-125">**ネットワークアダプター2ノード 1 (外部インターフェイス)**</span><span class="sxs-lookup"><span data-stu-id="6c83f-125">**Network adapter 2 Node 1 (External Interface)**</span></span>
    
    <span data-ttu-id="6c83f-126">3つのプライベート IP アドレスがこのネットワークアダプターに割り当てられます。たとえば、アクセスエッジサービスの131.107.155.10、Web 会議エッジサービスの場合は131.107.155.20、A/V Edge サービスの場合は131.107.155.30。</span><span class="sxs-lookup"><span data-stu-id="6c83f-126">Three private IP addresses are assigned to this network adapter, for example 131.107.155.10 for Access Edge service, 131.107.155.20 for Web Conferencing Edge service, 131.107.155.30 for A/V Edge service.</span></span>
    
    <span data-ttu-id="6c83f-127">アクセスエッジサービスのパブリック IP アドレスは、既定のゲートウェイがパブリックルーター (131.107.155.1) に設定されているプライマリ IP アドレスです。</span><span class="sxs-lookup"><span data-stu-id="6c83f-127">The Access Edge service public IP address is primary with default gateway set to the public router (131.107.155.1).</span></span>
    
    <span data-ttu-id="6c83f-128">Web 会議エッジサービスと A/V Edge サービスのプライベート IP アドレスは、Windows Server の **ローカルエリア接続プロパティ** の **インターネットプロトコルバージョン 4 (tcp/IPv4)** と **INTERNET protocol Version 6 (tcp/IPv6)** のプロパティの **[詳細設定**] セクションで追加の ip アドレスとなります。</span><span class="sxs-lookup"><span data-stu-id="6c83f-128">Web Conferencing Edge service and A/V Edge service private IP addresses are additional IP addresses in the **Advanced** section of the properties of **Internet Protocol Version 4 (TCP/IPv4)** and **Internet Protocol Version 6 (TCP/IPv6)** of the **Local Area Connection Properties** in Windows Server.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="6c83f-129">すべての3エッジサービスインターフェイスで単一の IP アドレスを使うことはできますが、お勧めしません。</span><span class="sxs-lookup"><span data-stu-id="6c83f-129">It is possible, though not recommended, to use a single IP address for all three Edge service interfaces.</span></span> <span data-ttu-id="6c83f-130">これにより、IP アドレスが保存されますが、サービスごとに異なるポート番号が必要になります。</span><span class="sxs-lookup"><span data-stu-id="6c83f-130">Though this does save IP addresses, it requires different port numbers for each service.</span></span> <span data-ttu-id="6c83f-131">既定のポート番号は 443/TCP であり、ほとんどのリモートファイアウォールでトラフィックが許可されます。</span><span class="sxs-lookup"><span data-stu-id="6c83f-131">The default port number is 443/TCP, which ensures that most remote firewalls will allow the traffic.</span></span> <span data-ttu-id="6c83f-132">ポートの値を変更する (たとえば、アクセスエッジサービスの場合は 5061/tcp、Web 会議エッジサービスの場合は 444/TCP、A/V Edge サービスの場合は、443/tcp) という問題が発生する可能性があります。これは、相手のファイアウォールによって 5061/TCP および 444/TCP 経由のトラフィックが許可されないリモート</span><span class="sxs-lookup"><span data-stu-id="6c83f-132">Changing the port values to (for example) 5061/TCP for the Access Edge service, 444/TCP for the Web Conferencing Edge service and 443/TCP for the A/V Edge service might cause problems for remote users where a firewall that they are behind does not allow the traffic over 5061/TCP and 444/TCP.</span></span> <span data-ttu-id="6c83f-133">さらに、3つの異なる IP アドレスで、IP アドレスをフィルター処理できるため、トラブルシューティングが容易になります。</span><span class="sxs-lookup"><span data-stu-id="6c83f-133">Additionally, three distinct IP addresses makes troubleshooting easier due to being able to filter on IP address.</span></span>

    
    </div>

  - <span data-ttu-id="6c83f-134">**ネットワークアダプター2ノード 2 (外部インターフェイス)**</span><span class="sxs-lookup"><span data-stu-id="6c83f-134">**Network adapter 2 Node 2 (External Interface)**</span></span>
    
    <span data-ttu-id="6c83f-135">3つのプライベート IP アドレスがこのネットワークアダプターに割り当てられます。たとえば、アクセスエッジサービスの131.107.155.11、Web 会議エッジサービスの場合は131.107.155.21、A/V Edge サービスの場合は131.107.155.31。</span><span class="sxs-lookup"><span data-stu-id="6c83f-135">Three private IP addresses are assigned to this network adapter, for example 131.107.155.11 for Access Edge service, 131.107.155.21 for Web Conferencing Edge service, 131.107.155.31 for A/V Edge service.</span></span>
    
    <span data-ttu-id="6c83f-136">アクセスエッジサービスのパブリック IP アドレスは、既定のゲートウェイがパブリックルーター (131.107.155.1) に設定されているプライマリ IP アドレスです。</span><span class="sxs-lookup"><span data-stu-id="6c83f-136">The Access Edge service public IP address is primary with default gateway set to the public router (131.107.155.1).</span></span>
    
    <span data-ttu-id="6c83f-137">Web 会議エッジサービスと A/V Edge サービスのプライベート IP アドレスは、Windows Server の **ローカルエリア接続プロパティ** の **インターネットプロトコルバージョン 4 (tcp/IPv4)** と **INTERNET protocol Version 6 (tcp/IPv6)** のプロパティの **[詳細設定**] セクションで追加の ip アドレスとなります。</span><span class="sxs-lookup"><span data-stu-id="6c83f-137">Web Conferencing Edge service and A/V Edge service private IP addresses are additional IP addresses in the **Advanced** section of the properties of **Internet Protocol Version 4 (TCP/IPv4)** and **Internet Protocol Version 6 (TCP/IPv6)** of the **Local Area Connection Properties** in Windows Server.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="6c83f-138">2つのネットワークアダプターでエッジサーバーを構成するには、2つのオプションのいずれかを使用します。</span><span class="sxs-lookup"><span data-stu-id="6c83f-138">Configuring the Edge Server with two network adapters is one of two options.</span></span> <span data-ttu-id="6c83f-139">もう1つの方法として、内部側とエッジサーバーの外部側の3つのネットワークアダプター用に1つのネットワークアダプターを使うことができます。</span><span class="sxs-lookup"><span data-stu-id="6c83f-139">The other option is to use one network adapter for the internal side and three network adapters for the external side of the Edge Server.</span></span> <span data-ttu-id="6c83f-140">このオプションの主な利点は、Edge Server サービスごとの個別のネットワークアダプターであり、トラブルシューティングが必要な場合は、より簡潔なデータ収集を行うことです。</span><span class="sxs-lookup"><span data-stu-id="6c83f-140">The main benefit of this option is a distinct network adapter per Edge Server service, and potentially more concise data collection when troubleshooting is necessary</span></span>



</div>

### <a name="dns-records-required-for-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses-example"></a><span data-ttu-id="6c83f-141">スケーリングされた統合エッジに必要な DNS レコード、パブリック IP アドレスを使った DNS 負荷分散 (例)</span><span class="sxs-lookup"><span data-stu-id="6c83f-141">DNS Records Required for Scaled Consolidated Edge, DNS Load Balancing with Public IP Addresses (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6c83f-142">場所/種類/ポート</span><span class="sxs-lookup"><span data-stu-id="6c83f-142">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="6c83f-143">FQDN/DNS レコード</span><span class="sxs-lookup"><span data-stu-id="6c83f-143">FQDN/DNS Record</span></span></th>
<th><span data-ttu-id="6c83f-144">IP アドレス/FQDN</span><span class="sxs-lookup"><span data-stu-id="6c83f-144">IP Address/FQDN</span></span></th>
<th><span data-ttu-id="6c83f-145">マップ先/コメント</span><span class="sxs-lookup"><span data-stu-id="6c83f-145">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c83f-146">外部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="6c83f-146">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="6c83f-147">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="6c83f-147">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="6c83f-148">131.107.155.10 および 131.107.155.11</span><span class="sxs-lookup"><span data-stu-id="6c83f-148">131.107.155.10 and 131.107.155.11</span></span></p></td>
<td><p><span data-ttu-id="6c83f-149">Access Edge service の外部インターフェイス (Contoso) は、Lync を有効にしたユーザーがいるすべての SIP ドメインについて、必要に応じて繰り返します。</span><span class="sxs-lookup"><span data-stu-id="6c83f-149">Access Edge service external interface (Contoso) Repeat as necessary for all SIP domains with Lync enabled users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c83f-150">外部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="6c83f-150">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="6c83f-151">webcon.contoso.com</span><span class="sxs-lookup"><span data-stu-id="6c83f-151">webcon.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="6c83f-152">131.107.155.20 および 131.107.155.21</span><span class="sxs-lookup"><span data-stu-id="6c83f-152">131.107.155.20 and 131.107.155.21</span></span></p></td>
<td><p><span data-ttu-id="6c83f-153">Web 会議エッジサービスの外部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="6c83f-153">Web Conferencing Edge service external interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c83f-154">外部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="6c83f-154">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="6c83f-155">av.contoso.com</span><span class="sxs-lookup"><span data-stu-id="6c83f-155">av.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="6c83f-156">131.107.155.30 および 131.107.155.31</span><span class="sxs-lookup"><span data-stu-id="6c83f-156">131.107.155.30 and 131.107.155.31</span></span></p></td>
<td><p><span data-ttu-id="6c83f-157">A/V Edge サービスの外部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="6c83f-157">A/V Edge service external interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c83f-158">外部 DNS/SRV/443</span><span class="sxs-lookup"><span data-stu-id="6c83f-158">External DNS/SRV/443</span></span></p></td>
<td><p><span data-ttu-id="6c83f-159">_sip._tls.contoso.com</span><span class="sxs-lookup"><span data-stu-id="6c83f-159">_sip._tls.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="6c83f-160">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="6c83f-160">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="6c83f-161">Access Edge サービスの外部インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="6c83f-161">Access Edge service external interface.</span></span> <span data-ttu-id="6c83f-162">Lync 2013 および Lync 2010 クライアントを外部で動作させるために、自動構成が必要です。</span><span class="sxs-lookup"><span data-stu-id="6c83f-162">Required for automatic configuration of Lync 2013 and Lync 2010 clients to work externally.</span></span> <span data-ttu-id="6c83f-163">Lync が有効になっているユーザーがいるすべての SIP ドメインで、必要に応じてこの手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="6c83f-163">Repeat as necessary for all SIP domains with Lync enabled users.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c83f-164">外部 DNS/SRV/5061</span><span class="sxs-lookup"><span data-stu-id="6c83f-164">External DNS/SRV/5061</span></span></p></td>
<td><p><span data-ttu-id="6c83f-165">_sipfederationtls._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="6c83f-165">_sipfederationtls._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="6c83f-166">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="6c83f-166">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="6c83f-167">Access Edge service の外部インターフェイスは、"許可された SIP ドメイン" と呼ばれるフェデレーションパートナー (以前のリリースで拡張フェデレーションと呼ばれる) を自動的に検出するために必要です。</span><span class="sxs-lookup"><span data-stu-id="6c83f-167">Access Edge service external interface Required for automatic DNS discovery of federated partners known as “Allowed SIP Domain” (called enhanced federation in previous releases).</span></span> <span data-ttu-id="6c83f-168">Lync を有効にしたユーザーがいるすべての SIP ドメインで、必要に応じて繰り返す</span><span class="sxs-lookup"><span data-stu-id="6c83f-168">Repeat as necessary for all SIP domains with Lync enabled users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c83f-169">内部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="6c83f-169">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="6c83f-170">lsedge.contoso.net</span><span class="sxs-lookup"><span data-stu-id="6c83f-170">lsedge.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="6c83f-171">172.25.33.10 および 172.25.33.11</span><span class="sxs-lookup"><span data-stu-id="6c83f-171">172.25.33.10 and 172.25.33.11</span></span></p></td>
<td><p><span data-ttu-id="6c83f-172">統合エッジ内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="6c83f-172">Consolidated Edge internal interface</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="records-required-for-federation"></a><span data-ttu-id="6c83f-173">フェデレーションに必要なレコード</span><span class="sxs-lookup"><span data-stu-id="6c83f-173">Records Required for Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6c83f-174">場所/種類/ポート</span><span class="sxs-lookup"><span data-stu-id="6c83f-174">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="6c83f-175">FQDN</span><span class="sxs-lookup"><span data-stu-id="6c83f-175">FQDN</span></span></th>
<th><span data-ttu-id="6c83f-176">IP アドレス/FQDN ホストレコード</span><span class="sxs-lookup"><span data-stu-id="6c83f-176">IP address/FQDN host record</span></span></th>
<th><span data-ttu-id="6c83f-177">マップ先/コメント</span><span class="sxs-lookup"><span data-stu-id="6c83f-177">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c83f-178">外部 DNS/SRV/5061</span><span class="sxs-lookup"><span data-stu-id="6c83f-178">External DNS/SRV/5061</span></span></p></td>
<td><p><span data-ttu-id="6c83f-179">_sipfederationtls._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="6c83f-179">_sipfederationtls._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="6c83f-180">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="6c83f-180">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="6c83f-181">SIP アクセスエッジサービスの外部インターフェイスは、他の潜在的なフェデレーションパートナーとのフェデレーションを自動的に検出するために必要です。また、"許可 SIP ドメイン" と呼ばれます (以前のリリースで拡張フェデレーションと呼ばれます)。</span><span class="sxs-lookup"><span data-stu-id="6c83f-181">SIP Access Edge service external interface Required for automatic DNS discovery of your federation to other potential federation partners, and is known as “Allowed SIP Domains” (called enhanced federation in previous releases).</span></span></p>
<div>

> [!IMPORTANT]  
> <span data-ttu-id="6c83f-182">Lync が有効なユーザーと、プッシュ通知サービスまたは Apple プッシュ通知サービスを使用している Microsoft Lync モバイルクライアントが含まれるすべての SIP ドメインで、必要に応じてこの手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="6c83f-182">Repeat as necessary for all SIP domains with Lync enabled users and Microsoft Lync Mobile clients that use either the Push Notification Service or the Apple Push Notification service</span></span>


</div></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="dns-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="6c83f-183">拡張メッセージングとプレゼンスプロトコルの DNS 概要</span><span class="sxs-lookup"><span data-stu-id="6c83f-183">DNS Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6c83f-184">場所/種類/ポート</span><span class="sxs-lookup"><span data-stu-id="6c83f-184">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="6c83f-185">FQDN</span><span class="sxs-lookup"><span data-stu-id="6c83f-185">FQDN</span></span></th>
<th><span data-ttu-id="6c83f-186">IP アドレス/FQDN ホストレコード</span><span class="sxs-lookup"><span data-stu-id="6c83f-186">IP address/FQDN host record</span></span></th>
<th><span data-ttu-id="6c83f-187">マップ先/コメント</span><span class="sxs-lookup"><span data-stu-id="6c83f-187">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c83f-188">外部 DNS/SRV/5269</span><span class="sxs-lookup"><span data-stu-id="6c83f-188">External DNS/SRV/5269</span></span></p></td>
<td><p><span data-ttu-id="6c83f-189">_xmpp-server._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="6c83f-189">_xmpp-server._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="6c83f-190">xmpp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="6c83f-190">xmpp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="6c83f-191">アクセスエッジサービスまたはエッジプールの XMPP プロキシ外部インターフェイス。グローバルポリシー、ユーザーが配置されているサイトポリシー、または Lync 対応ユーザーに適用されているユーザーポリシーを通じて、外部アクセスポリシーの構成を通じて、すべての内部 SIP ドメインで、必要に応じてこの手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="6c83f-191">XMPP proxy external interface on the Access Edge service or Edge pool.Repeat as necessary for all internal SIP domains with Lync enabled users where contact with XMPP contacts is allowed through the configuration of the External Access Policy through a global policy, site policy where the user is located, or user policy applied to the Lync-enabled user.</span></span> <span data-ttu-id="6c83f-192">許可されている XMPP ドメインは、XMPP フェデレーションパートナーポリシーでも構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c83f-192">An allowed XMPP domain must also be configured in the XMPP Federated Partners policy.</span></span> <span data-ttu-id="6c83f-193">詳細については、 <strong>「</strong> 関連項目」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6c83f-193">See topics in <strong>See Also</strong> for additional details</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c83f-194">外部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="6c83f-194">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="6c83f-195">xmpp.contoso.com (など)</span><span class="sxs-lookup"><span data-stu-id="6c83f-195">xmpp.contoso.com (for example)</span></span></p></td>
<td><p><span data-ttu-id="6c83f-196">エッジサーバーまたは XMPP プロキシをホストしているエッジプールのアクセスエッジサービスの IP アドレス</span><span class="sxs-lookup"><span data-stu-id="6c83f-196">IP address of Access Edge service on your Edge Server or Edge pool hosting XMPP proxy</span></span></p></td>
<td><p><span data-ttu-id="6c83f-197">XMPP プロキシサービスをホストしているアクセスエッジサービスまたはエッジプールへのポイント。</span><span class="sxs-lookup"><span data-stu-id="6c83f-197">Points to the Access Edge service or Edge pool that hosts the XMPP proxy service.</span></span> <span data-ttu-id="6c83f-198">通常、作成した SRV レコードは、このホスト (A または AAAA) レコードをポイントします。</span><span class="sxs-lookup"><span data-stu-id="6c83f-198">Typically, the SRV record that you create will point to this host (A or AAAA) record</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="6c83f-199">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6c83f-199">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

