---
title: DNS の概要 - パブリック IP アドレスを持つ単一統合エッジ
description: DNS 概要-パブリック IP アドレスを持つ単一の統合エッジ。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - Single consolidated edge with public IP addresses
ms:assetid: 7b83eae4-aa1a-4cc6-8077-42176d56cab5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205025(v=OCS.15)
ms:contentKeyID: 48184601
ms.date: 03/09/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 58f0787d894e741951fd220ef3b2a9fada8183b3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428980"
---
# <a name="dns-summary---single-consolidated-edge-with-public-ip-addresses-in-lync-server-2013"></a><span data-ttu-id="5896d-103">DNS の概要 - Lync Server 2013 でパブリック IP アドレスを持つ単一統合エッジ</span><span class="sxs-lookup"><span data-stu-id="5896d-103">DNS summary - Single consolidated edge with public IP addresses in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5896d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5896d-104">

<span> </span></span></span>

<span data-ttu-id="5896d-105">_**最終更新日:** 2017-03-09_</span><span class="sxs-lookup"><span data-stu-id="5896d-105">_**Topic Last Modified:** 2017-03-09_</span></span>

<span data-ttu-id="5896d-106">Lync Server 2013 へのリモートアクセスの DNS レコード要件は、証明書やポートの場合と非常に簡単です。</span><span class="sxs-lookup"><span data-stu-id="5896d-106">DNS record requirements for remote access to Lync Server 2013 are fairly straightforward compared to those for certificates and ports.</span></span> <span data-ttu-id="5896d-107">また、Lync 2013 を実行しているクライアントの構成方法とフェデレーションを有効にするかどうかによって、多くのレコードがオプションになります。</span><span class="sxs-lookup"><span data-stu-id="5896d-107">Also, many records are optional, depending on how you configure clients running Lync 2013 and whether you enable federation.</span></span>

<span data-ttu-id="5896d-108">Lync 2013 DNS の要件の詳細については、「 [Lync Server 2013 の dns 要件を確認](lync-server-2013-determine-dns-requirements.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5896d-108">For details about Lync 2013 DNS requirements, see [Determine DNS requirements for Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span></span>

<span data-ttu-id="5896d-109">Lync 2013 を実行しているクライアントの自動構成の詳細については、「 [Lync Server 2013 の dns 要件を決定](lync-server-2013-determine-dns-requirements.md)する」の「Split-Brain dns を使用しない自動構成」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5896d-109">For details about automatic configuration of clients running Lync 2013 if split-brain DNS is not configured, see “Automatic Configuration without Split-Brain DNS” in [Determine DNS requirements for Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span></span>

<span data-ttu-id="5896d-110">次の表には、単一の統合されたエッジトポロジの図に示されている単一の統合エッジトポロジをサポートするために必要な DNS レコードの概要を示します。</span><span class="sxs-lookup"><span data-stu-id="5896d-110">The following table contains a summary of the DNS records that are required to support the single consolidated edge topology shown in the Single Consolidated Edge Topology figure.</span></span> <span data-ttu-id="5896d-111">特定の DNS レコードは、Lync 2013 および Lync 2010 クライアントの自動構成にのみ必要であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="5896d-111">Note that certain DNS records are required only for automatic configuration of Lync 2013 and Lync 2010 clients.</span></span> <span data-ttu-id="5896d-112">グループポリシーオブジェクト (Gpo) を使って Lync クライアントを構成することを計画している場合は、関連付けられた自動構成レコードは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="5896d-112">If you plan to use group policy objects (GPOs) to configure Lync clients, the associated automatic configuration records are not necessary.</span></span>

<div>

## <a name="important-edge-server-network-adapter-requirements"></a><span data-ttu-id="5896d-113">重要: エッジサーバーのネットワークアダプターの要件</span><span class="sxs-lookup"><span data-stu-id="5896d-113">IMPORTANT: Edge Server Network Adapter Requirements</span></span>

<span data-ttu-id="5896d-114">ルーティングの問題を回避するには、エッジサーバーに少なくとも2つのネットワークアダプターがあり、その外部インターフェイスに関連付けられているネットワークアダプターでのみ既定のゲートウェイが設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="5896d-114">To avoid routing issues, verify that there are at least two network adapters in your Edge Servers and that the default gateway is set only on the network adapter associated with the external interface.</span></span> <span data-ttu-id="5896d-115">たとえば、パブリック ip アドレスを持つ単一の統合されたエッジトポロジで、 [Lync Server 2013 のパブリック ip アドレスを持つ単一の統合エッジ](lync-server-2013-single-consolidated-edge-with-public-ip-addresses.md)に表示されている場合、既定のゲートウェイは、インターネット境界またはファイアウォールでパブリック ip アドレスを提供できる外部ルーターを指します。</span><span class="sxs-lookup"><span data-stu-id="5896d-115">For example, as shown in the Single Consolidated Edge Topology with Public IP Addresses figure in [Single consolidated edge with public IP addresses in Lync Server 2013](lync-server-2013-single-consolidated-edge-with-public-ip-addresses.md), the default gateway would point to the external router at your Internet perimeter or firewall that can provide a public IP addresses.</span></span> <span data-ttu-id="5896d-116">エッジサーバーインターフェイスのネットワーク関係は、NAT 関係ではなくルートリレーションシップです。</span><span class="sxs-lookup"><span data-stu-id="5896d-116">The network relationship for Edge Server interfaces is a route relationship instead of a NAT relationship.</span></span>

<span data-ttu-id="5896d-117">エッジサーバーでは、次のように2つのネットワークアダプターを構成できます。</span><span class="sxs-lookup"><span data-stu-id="5896d-117">You can configure two network adapters in your Edge Server as follows:</span></span>

  - <span data-ttu-id="5896d-118">**ネットワークアダプター 1 (内部インターフェイス)**</span><span class="sxs-lookup"><span data-stu-id="5896d-118">**Network adapter 1 (Internal Interface)**</span></span>
    
    <span data-ttu-id="5896d-119">172.25.33.10 が割り当てられている内部インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="5896d-119">Internal interface with 172.25.33.10 assigned.</span></span>
    
    <span data-ttu-id="5896d-120">既定のゲートウェイは定義されていません。</span><span class="sxs-lookup"><span data-stu-id="5896d-120">No default gateway is defined.</span></span>
    
    <span data-ttu-id="5896d-121">Lync Server 2013 または Lync Server 2013 クライアントを実行しているサーバー (172.25.33.0 から192.168.10.0 など) が含まれているすべてのネットワークへの Edge 内部インターフェイスが含まれているネットワークからのルートがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="5896d-121">Ensure that there is a route from the network containing the Edge internal interface to any networks that contain servers running Lync Server 2013 or Lync Server 2013 clients (for example, from 172.25.33.0 to 192.168.10.0).</span></span>

  - <span data-ttu-id="5896d-122">**ネットワークアダプター 2 (外部インターフェイス)**</span><span class="sxs-lookup"><span data-stu-id="5896d-122">**Network adapter 2 (External Interface)**</span></span>
    
    <span data-ttu-id="5896d-123">3つのパブリック IP アドレスがこのネットワークアダプターに割り当てられます。たとえば、Access Edge の場合は131.107.155.10、Web 会議エッジの場合は131.107.155.20、AV Edge の場合は131.107.155.30 です。</span><span class="sxs-lookup"><span data-stu-id="5896d-123">Three public IP addresses are assigned to this network adapter, for example 131.107.155.10 for Access Edge, 131.107.155.20 for Web Conferencing Edge, 131.107.155.30 for AV Edge.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="5896d-124">すべての3エッジサービスインターフェイスで単一の IP アドレスを使うことはできますが、お勧めしません。</span><span class="sxs-lookup"><span data-stu-id="5896d-124">It is possible, though not recommended, to use a single IP address for all three Edge service interfaces.</span></span> <span data-ttu-id="5896d-125">これにより、IP アドレスが保存されますが、サービスごとに異なるポート番号が必要になります。</span><span class="sxs-lookup"><span data-stu-id="5896d-125">Though this does save IP addresses, it requires different port numbers for each service.</span></span> <span data-ttu-id="5896d-126">既定のポート番号は 443/TCP であり、ほとんどのリモートファイアウォールでトラフィックが許可されます。</span><span class="sxs-lookup"><span data-stu-id="5896d-126">The default port number is 443/TCP, which ensures that most remote firewalls will allow the traffic.</span></span> <span data-ttu-id="5896d-127">ポートの値を変更する (たとえば、アクセスエッジの場合は 5061/tcp、Web 会議エッジの場合は 444/TCP、AV Edge の場合は、ファイアウォールを使用しているファイアウォールでは 5061/tcp および 444/TCP 経由のトラフィックが許可されていないことがあります)。</span><span class="sxs-lookup"><span data-stu-id="5896d-127">Changing the port values to (for example) 5061/TCP for the Access Edge, 444/TCP for the Web Conferencing Edge and 443/TCP for the AV Edge might cause problems for remote users where a firewall that they are behind does not allow the traffic over 5061/TCP and 444/TCP.</span></span> <span data-ttu-id="5896d-128">さらに、3つの異なる IP アドレスで、IP アドレスをフィルター処理できるため、トラブルシューティングが容易になります。</span><span class="sxs-lookup"><span data-stu-id="5896d-128">Additionally, three distinct IP addresses makes troubleshooting easier due to being able to filter on IP address.</span></span>

    
    </div>
    
    <span data-ttu-id="5896d-129">アクセスエッジのパブリック IP アドレスは、パブリックルータ (131.107.155.1) に設定されたデフォルトゲートウェイのプライマリ IP アドレスです。</span><span class="sxs-lookup"><span data-stu-id="5896d-129">The Access Edge public IP address is primary with default gateway set to the public router (131.107.155.1).</span></span>
    
    <span data-ttu-id="5896d-130">Web 会議と A/V Edge のパブリック IP アドレスは、Windows Server の **ローカルエリア接続プロパティ** の **インターネットプロトコルバージョン 4 (tcp/IPv4)** と **INTERNET protocol Version 6 (tcp/IPv6)** のプロパティの **[詳細**] セクションで追加の ip アドレスとなります。</span><span class="sxs-lookup"><span data-stu-id="5896d-130">Web conferencing and A/V Edge public IP addresses are additional IP addresses in the **Advanced** section of the properties of **Internet Protocol Version 4 (TCP/IPv4)** and **Internet Protocol Version 6 (TCP/IPv6)** of the **Local Area Connection Properties** in Windows Server.</span></span>

<div>


> [!TIP]
> <span data-ttu-id="5896d-131">2つのネットワークアダプターでエッジサーバーを構成するには、2つのオプションのいずれかを使用します。</span><span class="sxs-lookup"><span data-stu-id="5896d-131">Configuring the Edge Server with two network adapters is one of two options.</span></span> <span data-ttu-id="5896d-132">もう1つの方法として、内部側とエッジサーバーの外部側の3つのネットワークアダプター用に1つのネットワークアダプターを使うことができます。</span><span class="sxs-lookup"><span data-stu-id="5896d-132">The other option is to use one network adapter for the internal side and three network adapters for the external side of the Edge Server.</span></span> <span data-ttu-id="5896d-133">このオプションの主な利点は、Edge Server サービスごとの個別のネットワークアダプターであり、トラブルシューティングが必要な場合は、より簡潔なデータ収集を行うことです。</span><span class="sxs-lookup"><span data-stu-id="5896d-133">The main benefit of this option is a distinct network adapter per Edge Server service, and potentially more concise data collection when troubleshooting is necessary</span></span>



</div>

### <a name="dns-records-required-for-single-consolidated-edge-with-public-ip-addresses-example"></a><span data-ttu-id="5896d-134">パブリック IP アドレスを使った単一の統合エッジに必要な DNS レコード (例)</span><span class="sxs-lookup"><span data-stu-id="5896d-134">DNS Records Required for Single Consolidated Edge with Public IP Addresses (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5896d-135">場所/種類/ポート</span><span class="sxs-lookup"><span data-stu-id="5896d-135">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="5896d-136">FQDN/DNS レコード</span><span class="sxs-lookup"><span data-stu-id="5896d-136">FQDN/DNS Record</span></span></th>
<th><span data-ttu-id="5896d-137">IP アドレス/FQDN</span><span class="sxs-lookup"><span data-stu-id="5896d-137">IP Address/FQDN</span></span></th>
<th><span data-ttu-id="5896d-138">マップ先/コメント</span><span class="sxs-lookup"><span data-stu-id="5896d-138">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5896d-139">外部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="5896d-139">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="5896d-140">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="5896d-140">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="5896d-141">131.107.155.10</span><span class="sxs-lookup"><span data-stu-id="5896d-141">131.107.155.10</span></span></p></td>
<td><p><span data-ttu-id="5896d-142">Access Edge の外部インターフェイス (Contoso) は、Lync が有効になっているユーザーがいるすべての SIP ドメインについて、必要に応じて繰り返す</span><span class="sxs-lookup"><span data-stu-id="5896d-142">Access Edge external interface (Contoso) Repeat as necessary for all SIP domains with Lync enabled users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5896d-143">外部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="5896d-143">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="5896d-144">webcon.contoso.com</span><span class="sxs-lookup"><span data-stu-id="5896d-144">webcon.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="5896d-145">131.107.155.20</span><span class="sxs-lookup"><span data-stu-id="5896d-145">131.107.155.20</span></span></p></td>
<td><p><span data-ttu-id="5896d-146">Web 会議エッジの外部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="5896d-146">Web Conferencing Edge external interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5896d-147">外部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="5896d-147">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="5896d-148">av.contoso.com</span><span class="sxs-lookup"><span data-stu-id="5896d-148">av.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="5896d-149">131.107.155.30</span><span class="sxs-lookup"><span data-stu-id="5896d-149">131.107.155.30</span></span></p></td>
<td><p><span data-ttu-id="5896d-150">A/V Edge の外部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="5896d-150">A/V Edge external interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5896d-151">外部 DNS/SRV/443</span><span class="sxs-lookup"><span data-stu-id="5896d-151">External DNS/SRV/443</span></span></p></td>
<td><p><span data-ttu-id="5896d-152">_sip._tls.contoso.com</span><span class="sxs-lookup"><span data-stu-id="5896d-152">_sip._tls.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="5896d-153">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="5896d-153">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="5896d-154">Access Edge の外部インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="5896d-154">Access Edge external interface.</span></span> <span data-ttu-id="5896d-155">Lync 2013 および Lync 2010 クライアントを外部で動作させるために、自動構成が必要です。</span><span class="sxs-lookup"><span data-stu-id="5896d-155">Required for automatic configuration of Lync 2013 and Lync 2010 clients to work externally.</span></span> <span data-ttu-id="5896d-156">Lync が有効になっているユーザーがいるすべての SIP ドメインで、必要に応じてこの手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="5896d-156">Repeat as necessary for all SIP domains with Lync enabled users.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5896d-157">外部 DNS/SRV/5061</span><span class="sxs-lookup"><span data-stu-id="5896d-157">External DNS/SRV/5061</span></span></p></td>
<td><p><span data-ttu-id="5896d-158">_sipfederationtls._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="5896d-158">_sipfederationtls._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="5896d-159">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="5896d-159">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="5896d-160">SIP アクセスエッジの外部インターフェイスは、"許可された SIP ドメイン" と呼ばれるフェデレーションパートナー (以前のリリースで拡張フェデレーションと呼ばれる) を自動的に検出するために必要です。Lync を有効にしたユーザーがいるすべての SIP ドメインで、必要に応じて繰り返す</span><span class="sxs-lookup"><span data-stu-id="5896d-160">SIP Access Edge external interface Required for automatic DNS discovery of federated partners known as “Allowed SIP Domain” (called enhanced federation in previous releases).Repeat as necessary for all SIP domains with Lync enabled users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5896d-161">内部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="5896d-161">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="5896d-162">lsedge.contoso.net</span><span class="sxs-lookup"><span data-stu-id="5896d-162">lsedge.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="5896d-163">172.25.33.10</span><span class="sxs-lookup"><span data-stu-id="5896d-163">172.25.33.10</span></span></p></td>
<td><p><span data-ttu-id="5896d-164">統合エッジ内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="5896d-164">Consolidated Edge internal interface</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!IMPORTANT]
> <span data-ttu-id="5896d-165">前の表に記載されているレコードは、 <EM>.net</EM> extension または <EM>.com</EM> の拡張子を使って表示され、分割ブレイン DNS を使用していない場合は、どのゾーンを含める必要があるかを強調します。</span><span class="sxs-lookup"><span data-stu-id="5896d-165">The records listed in the previous table are shown with either a <EM>.net</EM> extension or a <EM>.com</EM> extension to highlight which zone they need to reside in if you are not using split-brain DNS.</span></span> <span data-ttu-id="5896d-166">分割ブレイン DNS を使用している場合は、すべてのレコードが同じゾーンに存在し、内部または外部のどちらのバージョンであるかだけが区別されます。</span><span class="sxs-lookup"><span data-stu-id="5896d-166">If you are using split-brain DNS, all records would be in the same zone, with the only distinction being whether they are in the internal or external version.</span></span> <span data-ttu-id="5896d-167">詳細については、「 <A href="lync-server-2013-determine-dns-requirements.md">Lync Server 2013 の DNS 要件を特定</A>する」の「スプリットブレイン dns」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5896d-167">For details, see “Split-Brain DNS” in <A href="lync-server-2013-determine-dns-requirements.md">Determine DNS requirements for Lync Server 2013</A>.</span></span>



</div>

</div>

<div>

## <a name="records-required-for-federation"></a><span data-ttu-id="5896d-168">フェデレーションに必要なレコード</span><span class="sxs-lookup"><span data-stu-id="5896d-168">Records Required for Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5896d-169">場所/種類/ポート</span><span class="sxs-lookup"><span data-stu-id="5896d-169">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="5896d-170">FQDN</span><span class="sxs-lookup"><span data-stu-id="5896d-170">FQDN</span></span></th>
<th><span data-ttu-id="5896d-171">IP アドレス/FQDN ホストレコード</span><span class="sxs-lookup"><span data-stu-id="5896d-171">IP address/FQDN host record</span></span></th>
<th><span data-ttu-id="5896d-172">マップ先/コメント</span><span class="sxs-lookup"><span data-stu-id="5896d-172">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5896d-173">外部 DNS/SRV/5061</span><span class="sxs-lookup"><span data-stu-id="5896d-173">External DNS/SRV/5061</span></span></p></td>
<td><p><span data-ttu-id="5896d-174">_sipfederationtls._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="5896d-174">_sipfederationtls._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="5896d-175">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="5896d-175">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="5896d-176">SIP アクセスエッジ外部インタフェースは、他の潜在的なフェデレーションパートナーとのフェデレーションを自動的に検出するために必要です。また、"許可された SIP ドメイン" と呼ばれます (以前のリリースでは拡張フェデレーションと呼ばれます)。Lync を有効にしたユーザーがいるすべての SIP ドメインで、必要に応じて繰り返す</span><span class="sxs-lookup"><span data-stu-id="5896d-176">SIP Access Edge external interface Required for automatic DNS discovery of your federation to other potential federation partners, and is known as “Allowed SIP Domains” (called enhanced federation in previous releases).Repeat as necessary for all SIP domains with Lync enabled users</span></span></p>



> [!IMPORTANT]
> <span data-ttu-id="5896d-177">この SRV レコードは、モビリティとプッシュ通知のクリアリングハウスに必要です</span><span class="sxs-lookup"><span data-stu-id="5896d-177">This SRV record is required for mobility and the push notification clearing house</span></span>

</td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="dns-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="5896d-178">拡張メッセージングとプレゼンスプロトコルの DNS 概要</span><span class="sxs-lookup"><span data-stu-id="5896d-178">DNS Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5896d-179">場所/種類/ポート</span><span class="sxs-lookup"><span data-stu-id="5896d-179">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="5896d-180">FQDN</span><span class="sxs-lookup"><span data-stu-id="5896d-180">FQDN</span></span></th>
<th><span data-ttu-id="5896d-181">IP アドレス/FQDN ホストレコード</span><span class="sxs-lookup"><span data-stu-id="5896d-181">IP address/FQDN host record</span></span></th>
<th><span data-ttu-id="5896d-182">マップ先/コメント</span><span class="sxs-lookup"><span data-stu-id="5896d-182">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5896d-183">外部 DNS/SRV/5269</span><span class="sxs-lookup"><span data-stu-id="5896d-183">External DNS/SRV/5269</span></span></p></td>
<td><p><span data-ttu-id="5896d-184">_xmpp-server._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="5896d-184">_xmpp-server._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="5896d-185">xmpp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="5896d-185">xmpp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="5896d-186">アクセスエッジサービスまたはエッジプールの XMPP プロキシ外部インターフェイス。グローバルポリシー、ユーザーが配置されているサイトポリシー、または Lync 対応ユーザーに適用されているユーザーポリシーを通じて、外部アクセスポリシーの構成を通じて、すべての内部 SIP ドメインで、必要に応じてこの手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="5896d-186">XMPP proxy external interface on the Access Edge service or Edge pool.Repeat as necessary for all internal SIP domains with Lync enabled users where contact with XMPP contacts is allowed through the configuration of the External Access Policy through a global policy, site policy where the user is located, or user policy applied to the Lync-enabled user.</span></span> <span data-ttu-id="5896d-187">許可されている XMPP ドメインは、XMPP フェデレーションパートナーポリシーでも構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5896d-187">An allowed XMPP domain must also be configured in the XMPP Federated Partners policy.</span></span> <span data-ttu-id="5896d-188">詳細については、 <strong>「</strong> 関連項目」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5896d-188">See topics in <strong>See Also</strong> for additional details</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5896d-189">外部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="5896d-189">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="5896d-190">xmpp.contoso.com (など)</span><span class="sxs-lookup"><span data-stu-id="5896d-190">xmpp.contoso.com (for example)</span></span></p></td>
<td><p><span data-ttu-id="5896d-191">エッジサーバーまたは XMPP プロキシをホストしているエッジプールのアクセスエッジサービスの IP アドレス</span><span class="sxs-lookup"><span data-stu-id="5896d-191">IP address of Access Edge service on your Edge Server or Edge pool hosting XMPP proxy</span></span></p></td>
<td><p><span data-ttu-id="5896d-192">XMPP プロキシサービスをホストしているアクセスエッジサービスまたはエッジプールへのポイント。</span><span class="sxs-lookup"><span data-stu-id="5896d-192">Points to the Access Edge service or Edge pool that hosts the XMPP proxy service.</span></span> <span data-ttu-id="5896d-193">通常、作成した SRV レコードは、このホスト (A または AAAA) レコードをポイントします。</span><span class="sxs-lookup"><span data-stu-id="5896d-193">Typically, the SRV record that you create will point to this host (A or AAAA) record</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="5896d-194">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5896d-194">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

