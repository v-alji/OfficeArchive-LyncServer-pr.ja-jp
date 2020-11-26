---
title: DNS の概要 - 単一統合エッジ (NAT によるプライベート IP アドレスを使用)
description: DNS 概要-NAT を使用したプライベート IP アドレスを持つ単一の統合エッジ。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - Single consolidated edge with private IP addresses using NAT
ms:assetid: a7e5d792-f397-45e5-af85-20d0f4bf405f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412787(v=OCS.15)
ms:contentKeyID: 48185025
ms.date: 03/09/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 80402e04c1993fddda4d33ece22374e73175b5f5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437694"
---
# <a name="dns-summary---single-consolidated-edge-with-private-ip-addresses-using-nat-in-lync-server-2013"></a><span data-ttu-id="1c68a-103">DNS の概要 - Lync Server 2013 の単一統合エッジ (NAT によるプライベート IP アドレスを使用)</span><span class="sxs-lookup"><span data-stu-id="1c68a-103">DNS summary - Single consolidated edge with private IP addresses using NAT in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1c68a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1c68a-104">

<span> </span></span></span>

<span data-ttu-id="1c68a-105">_**最終更新日:** 2017-03-09_</span><span class="sxs-lookup"><span data-stu-id="1c68a-105">_**Topic Last Modified:** 2017-03-09_</span></span>

<span data-ttu-id="1c68a-106">Lync Server 2013 へのリモートアクセスの DNS レコード要件は、証明書やポートの場合と非常に簡単です。</span><span class="sxs-lookup"><span data-stu-id="1c68a-106">DNS record requirements for remote access to Lync Server 2013 are fairly straightforward compared to those for certificates and ports.</span></span> <span data-ttu-id="1c68a-107">また、Lync 2013 を実行しているクライアントの構成方法とフェデレーションを有効にするかどうかによって、多くのレコードがオプションになります。</span><span class="sxs-lookup"><span data-stu-id="1c68a-107">Also, many records are optional, depending on how you configure clients running Lync 2013 and whether you enable federation.</span></span>

<span data-ttu-id="1c68a-108">Lync 2013 DNS の要件の詳細については、「 [Lync Server 2013 の dns 要件を確認](lync-server-2013-determine-dns-requirements.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1c68a-108">For details about Lync 2013 DNS requirements, see [Determine DNS requirements for Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span></span>

<span data-ttu-id="1c68a-109">Lync 2013 を実行しているクライアントの自動構成の詳細については、「 [Lync Server 2013 の dns 要件を決定](lync-server-2013-determine-dns-requirements.md)する」の「Split-Brain dns を使用しない自動構成」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1c68a-109">For details about automatic configuration of clients running Lync 2013 if split-brain DNS is not configured, see “Automatic Configuration without Split-Brain DNS” in [Determine DNS requirements for Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span></span>

<span data-ttu-id="1c68a-110">次の表には、単一の統合されたエッジトポロジの図に示されている単一の統合エッジトポロジをサポートするために必要な DNS レコードの概要を示します。</span><span class="sxs-lookup"><span data-stu-id="1c68a-110">The following table contains a summary of the DNS records that are required to support the single consolidated edge topology shown in the Single Consolidated Edge Topology figure.</span></span> <span data-ttu-id="1c68a-111">特定の DNS レコードは、Lync 2013 および Lync 2010 クライアントの自動構成にのみ必要であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="1c68a-111">Note that certain DNS records are required only for automatic configuration of Lync 2013 and Lync 2010 clients.</span></span> <span data-ttu-id="1c68a-112">グループポリシーオブジェクト (Gpo) を使って Lync クライアントを構成することを計画している場合は、関連付けられた自動構成レコードは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="1c68a-112">If you plan to use group policy objects (GPOs) to configure Lync clients, the associated automatic configuration records are not necessary.</span></span>

<div>

## <a name="important-edge-server-network-adapter-requirements"></a><span data-ttu-id="1c68a-113">重要: エッジサーバーのネットワークアダプターの要件</span><span class="sxs-lookup"><span data-stu-id="1c68a-113">IMPORTANT: Edge Server Network Adapter Requirements</span></span>

<span data-ttu-id="1c68a-114">ルーティングの問題を回避するには、エッジサーバーに少なくとも2つのネットワークアダプターがあり、その外部インターフェイスに関連付けられているネットワークアダプターでのみ既定のゲートウェイが設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1c68a-114">To avoid routing issues, verify that there are at least two network adapters in your Edge Servers and that the default gateway is set only on the network adapter associated with the external interface.</span></span> <span data-ttu-id="1c68a-115">たとえば、統合された1つの Edge トポロジ (単一の統合エッジの、 [プライベート IP アドレスと NAT を持つ1つの統合エッジ) と、Lync Server 2013 で](lync-server-2013-single-consolidated-edge-with-private-ip-addresses-and-nat.md)は、既定のゲートウェイは外部ファイアウォール (10.45.16.1) をポイントします。</span><span class="sxs-lookup"><span data-stu-id="1c68a-115">For example, as shown in the Single Consolidated Edge Topology figure in [Single consolidated edge with private IP addresses and NAT in Lync Server 2013](lync-server-2013-single-consolidated-edge-with-private-ip-addresses-and-nat.md), the default gateway would point to the external firewall (10.45.16.1).</span></span>

<span data-ttu-id="1c68a-116">エッジサーバーでは、次のように2つのネットワークアダプターを構成できます。</span><span class="sxs-lookup"><span data-stu-id="1c68a-116">You can configure two network adapters in your Edge Server as follows:</span></span>

  - <span data-ttu-id="1c68a-117">**ネットワークアダプター 1 (内部インターフェイス)**</span><span class="sxs-lookup"><span data-stu-id="1c68a-117">**Network adapter 1 (Internal Interface)**</span></span>
    
    <span data-ttu-id="1c68a-118">172.25.33.10 が割り当てられている内部インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="1c68a-118">Internal interface with 172.25.33.10 assigned.</span></span>
    
    <span data-ttu-id="1c68a-119">既定のゲートウェイは定義されていません。</span><span class="sxs-lookup"><span data-stu-id="1c68a-119">No default gateway is defined.</span></span>
    
    <span data-ttu-id="1c68a-120">Lync Server 2013 または Lync Server 2013 クライアントを実行しているサーバー (172.25.33.0 から192.168.10.0 など) が含まれているすべてのネットワークへの Edge 内部インターフェイスが含まれているネットワークからのルートがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1c68a-120">Ensure that there is a route from the network containing the Edge internal interface to any networks that contain servers running Lync Server 2013 or Lync Server 2013 clients (for example, from 172.25.33.0 to 192.168.10.0).</span></span>

  - <span data-ttu-id="1c68a-121">**ネットワークアダプター 2 (外部インターフェイス)**</span><span class="sxs-lookup"><span data-stu-id="1c68a-121">**Network adapter 2 (External Interface)**</span></span>
    
    <span data-ttu-id="1c68a-122">このネットワークアダプターには3つのプライベート IP アドレスが割り当てられています。たとえば、Access Edge の場合は10.45.16.10、Web 会議エッジの場合は10.45.16.20、AV Edge の場合は10.45.16.30</span><span class="sxs-lookup"><span data-stu-id="1c68a-122">Three private IP addresses are assigned to this network adapter, for example 10.45.16.10 for Access Edge, 10.45.16.20 for Web Conferencing Edge, 10.45.16.30 for AV Edge</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="1c68a-123">すべての3エッジサービスインターフェイスで単一の IP アドレスを使うことはできますが、お勧めしません。</span><span class="sxs-lookup"><span data-stu-id="1c68a-123">It is possible, though not recommended, to use a single IP address for all three Edge service interfaces.</span></span> <span data-ttu-id="1c68a-124">これにより、IP アドレスが保存されますが、サービスごとに異なるポート番号が必要になります。</span><span class="sxs-lookup"><span data-stu-id="1c68a-124">Though this does save IP addresses, it requires different port numbers for each service.</span></span> <span data-ttu-id="1c68a-125">既定のポート番号は 443/TCP であり、ほとんどのリモートファイアウォールでトラフィックが許可されます。</span><span class="sxs-lookup"><span data-stu-id="1c68a-125">The default port number is 443/TCP, which ensures that most remote firewalls will allow the traffic.</span></span> <span data-ttu-id="1c68a-126">ポートの値を変更する (たとえば、アクセスエッジの場合は 5061/tcp、Web 会議エッジの場合は 444/TCP、AV Edge の場合は、ファイアウォールを使用しているファイアウォールでは 5061/tcp および 444/TCP 経由のトラフィックが許可されていないことがあります)。</span><span class="sxs-lookup"><span data-stu-id="1c68a-126">Changing the port values to (for example) 5061/TCP for the Access Edge, 444/TCP for the Web Conferencing Edge and 443/TCP for the AV Edge might cause problems for remote users where a firewall that they are behind does not allow the traffic over 5061/TCP and 444/TCP.</span></span> <span data-ttu-id="1c68a-127">さらに、3つの異なる IP アドレスで、IP アドレスをフィルター処理できるため、トラブルシューティングが容易になります。</span><span class="sxs-lookup"><span data-stu-id="1c68a-127">Additionally, three distinct IP addresses makes troubleshooting easier due to being able to filter on IP address.</span></span>

    
    </div>
    
    <span data-ttu-id="1c68a-128">アクセスエッジ IP アドレスは、既定のゲートウェイが統合ルーター (10.45.16.1) に設定されているプライマリ IP アドレスです。</span><span class="sxs-lookup"><span data-stu-id="1c68a-128">Access Edge IP address is primary with default gateway set to integrated router (10.45.16.1).</span></span>
    
    <span data-ttu-id="1c68a-129">Web 会議と A/V Edge の IP アドレス。</span><span class="sxs-lookup"><span data-stu-id="1c68a-129">Web conferencing and A/V Edge IP addresses secondary.</span></span>

<div>


> [!TIP]
> <span data-ttu-id="1c68a-130">2つのネットワークアダプターでエッジサーバーを構成するには、2つのオプションのいずれかを使用します。</span><span class="sxs-lookup"><span data-stu-id="1c68a-130">Configuring the Edge Server with two network adapters is one of two options.</span></span> <span data-ttu-id="1c68a-131">もう1つの方法として、内部側とエッジサーバーの外部側の3つのネットワークアダプター用に1つのネットワークアダプターを使うことができます。</span><span class="sxs-lookup"><span data-stu-id="1c68a-131">The other option is to use one network adapter for the internal side and three network adapters for the external side of the Edge Server.</span></span> <span data-ttu-id="1c68a-132">このオプションの主な利点は、Edge Server サービスごとの個別のネットワークアダプターであり、トラブルシューティングが必要な場合は、より簡潔なデータ収集を行うことです。</span><span class="sxs-lookup"><span data-stu-id="1c68a-132">The main benefit of this option is a distinct network adapter per Edge Server service, and potentially more concise data collection when troubleshooting is necessary</span></span>



</div>

### <a name="dns-records-required-for-single-consolidated-edge-with-private-ip-addresses-using-nat-example"></a><span data-ttu-id="1c68a-133">NAT を使用してプライベート IP アドレスを持つ単一の統合エッジに必要な DNS レコード (例)</span><span class="sxs-lookup"><span data-stu-id="1c68a-133">DNS Records Required for Single Consolidated Edge with Private IP Addresses Using NAT (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1c68a-134">場所/種類/ポート</span><span class="sxs-lookup"><span data-stu-id="1c68a-134">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="1c68a-135">FQDN/DNS レコード</span><span class="sxs-lookup"><span data-stu-id="1c68a-135">FQDN/DNS Record</span></span></th>
<th><span data-ttu-id="1c68a-136">IP アドレス/FQDN</span><span class="sxs-lookup"><span data-stu-id="1c68a-136">IP Address/FQDN</span></span></th>
<th><span data-ttu-id="1c68a-137">マップ先/コメント</span><span class="sxs-lookup"><span data-stu-id="1c68a-137">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1c68a-138">外部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="1c68a-138">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="1c68a-139">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="1c68a-139">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="1c68a-140">131.107.155.10</span><span class="sxs-lookup"><span data-stu-id="1c68a-140">131.107.155.10</span></span></p></td>
<td><p><span data-ttu-id="1c68a-141">Access Edge の外部インターフェイス (Contoso) は、Lync が有効になっているユーザーがいるすべての SIP ドメインについて、必要に応じて繰り返す</span><span class="sxs-lookup"><span data-stu-id="1c68a-141">Access Edge external interface (Contoso)Repeat as necessary for all SIP domains with Lync enabled users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c68a-142">外部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="1c68a-142">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="1c68a-143">webcon.contoso.com</span><span class="sxs-lookup"><span data-stu-id="1c68a-143">webcon.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="1c68a-144">131.107.155.20</span><span class="sxs-lookup"><span data-stu-id="1c68a-144">131.107.155.20</span></span></p></td>
<td><p><span data-ttu-id="1c68a-145">Web 会議エッジの外部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="1c68a-145">Web Conferencing Edge external interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c68a-146">外部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="1c68a-146">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="1c68a-147">av.contoso.com</span><span class="sxs-lookup"><span data-stu-id="1c68a-147">av.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="1c68a-148">131.107.155.30</span><span class="sxs-lookup"><span data-stu-id="1c68a-148">131.107.155.30</span></span></p></td>
<td><p><span data-ttu-id="1c68a-149">A/V Edge の外部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="1c68a-149">A/V Edge external interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c68a-150">外部 DNS/SRV/443</span><span class="sxs-lookup"><span data-stu-id="1c68a-150">External DNS/SRV/443</span></span></p></td>
<td><p><span data-ttu-id="1c68a-151">_sip._tls.contoso.com</span><span class="sxs-lookup"><span data-stu-id="1c68a-151">_sip._tls.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="1c68a-152">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="1c68a-152">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="1c68a-153">Access Edge の外部インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="1c68a-153">Access Edge external interface.</span></span> <span data-ttu-id="1c68a-154">Lync 2013 および Lync 2010 クライアントを外部で動作させるために、自動構成が必要です。</span><span class="sxs-lookup"><span data-stu-id="1c68a-154">Required for automatic configuration of Lync 2013 and Lync 2010 clients to work externally.</span></span> <span data-ttu-id="1c68a-155">Lync が有効になっているユーザーがいるすべての SIP ドメインで、必要に応じてこの手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="1c68a-155">Repeat as necessary for all SIP domains with Lync enabled users.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c68a-156">外部 DNS/SRV/5061</span><span class="sxs-lookup"><span data-stu-id="1c68a-156">External DNS/SRV/5061</span></span></p></td>
<td><p><span data-ttu-id="1c68a-157">_sipfederationtls._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="1c68a-157">_sipfederationtls._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="1c68a-158">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="1c68a-158">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="1c68a-159">SIP アクセスエッジの外部インターフェイスは、"許可された SIP ドメイン" と呼ばれるフェデレーションパートナー (以前のリリースで拡張フェデレーションと呼ばれる) を自動的に検出するために必要です。Lync を有効にしたユーザーがいるすべての SIP ドメインで、必要に応じて繰り返す</span><span class="sxs-lookup"><span data-stu-id="1c68a-159">SIP Access Edge external interface Required for automatic DNS discovery of federated partners known as “Allowed SIP Domain” (called enhanced federation in previous releases).Repeat as necessary for all SIP domains with Lync enabled users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c68a-160">内部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="1c68a-160">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="1c68a-161">lsedge.contoso.net</span><span class="sxs-lookup"><span data-stu-id="1c68a-161">lsedge.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="1c68a-162">172.25.33.10</span><span class="sxs-lookup"><span data-stu-id="1c68a-162">172.25.33.10</span></span></p></td>
<td><p><span data-ttu-id="1c68a-163">統合エッジ内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="1c68a-163">Consolidated Edge internal interface</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!IMPORTANT]
> <span data-ttu-id="1c68a-164">前の表に記載されているレコードは、 <EM>.net</EM> extension または <EM>.com</EM> の拡張子を使って表示され、分割ブレイン DNS を使用していない場合は、どのゾーンを含める必要があるかを強調します。</span><span class="sxs-lookup"><span data-stu-id="1c68a-164">The records listed in the previous table are shown with either a <EM>.net</EM> extension or a <EM>.com</EM> extension to highlight which zone they need to reside in if you are not using split-brain DNS.</span></span> <span data-ttu-id="1c68a-165">分割ブレイン DNS を使用している場合、すべてのレコードは同じ <EM>.com</EM> ゾーン内にあります。これは、内部または外部の DNS ゾーンのバージョンであるかどうかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="1c68a-165">If you are using split-brain DNS, all records would be in the same <EM>.com</EM> zone, with the only distinction being whether they are in the internal or external DNS zone version.</span></span> <span data-ttu-id="1c68a-166">詳細については、「 <A href="lync-server-2013-determine-dns-requirements.md">Lync Server 2013 の DNS 要件を特定</A>する」の「スプリットブレイン dns」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1c68a-166">For details, see “Split-Brain DNS” in <A href="lync-server-2013-determine-dns-requirements.md">Determine DNS requirements for Lync Server 2013</A>.</span></span>



</div>

</div>

<div>

## <a name="records-required-for-federation"></a><span data-ttu-id="1c68a-167">フェデレーションに必要なレコード</span><span class="sxs-lookup"><span data-stu-id="1c68a-167">Records Required for Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1c68a-168">場所/種類/ポート</span><span class="sxs-lookup"><span data-stu-id="1c68a-168">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="1c68a-169">FQDN</span><span class="sxs-lookup"><span data-stu-id="1c68a-169">FQDN</span></span></th>
<th><span data-ttu-id="1c68a-170">IP アドレス/FQDN ホストレコード</span><span class="sxs-lookup"><span data-stu-id="1c68a-170">IP address/FQDN host record</span></span></th>
<th><span data-ttu-id="1c68a-171">マップ先/コメント</span><span class="sxs-lookup"><span data-stu-id="1c68a-171">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1c68a-172">外部 DNS/SRV/5061</span><span class="sxs-lookup"><span data-stu-id="1c68a-172">External DNS/SRV/5061</span></span></p></td>
<td><p><span data-ttu-id="1c68a-173">_sipfederationtls._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="1c68a-173">_sipfederationtls._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="1c68a-174">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="1c68a-174">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="1c68a-175">SIP アクセスエッジ外部インタフェースは、他の潜在的なフェデレーションパートナーとのフェデレーションを自動的に検出するために必要です。また、"許可された SIP ドメイン" と呼ばれます (以前のリリースでは拡張フェデレーションと呼ばれます)。Lync を有効にしたユーザーがいるすべての SIP ドメインで、必要に応じて繰り返す</span><span class="sxs-lookup"><span data-stu-id="1c68a-175">SIP Access Edge external interface Required for automatic DNS discovery of your federation to other potential federation partners, and is known as “Allowed SIP Domains” (called enhanced federation in previous releases).Repeat as necessary for all SIP domains with Lync enabled users</span></span></p>



> [!IMPORTANT]
> <span data-ttu-id="1c68a-176">この SRV レコードは、モビリティとプッシュ通知のクリアリングハウスに必要です</span><span class="sxs-lookup"><span data-stu-id="1c68a-176">This SRV record is required for mobility and the push notification clearing house</span></span>

</td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="dns-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="1c68a-177">拡張メッセージングとプレゼンスプロトコルの DNS 概要</span><span class="sxs-lookup"><span data-stu-id="1c68a-177">DNS Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1c68a-178">場所/種類/ポート</span><span class="sxs-lookup"><span data-stu-id="1c68a-178">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="1c68a-179">FQDN</span><span class="sxs-lookup"><span data-stu-id="1c68a-179">FQDN</span></span></th>
<th><span data-ttu-id="1c68a-180">IP アドレス/FQDN ホストレコード</span><span class="sxs-lookup"><span data-stu-id="1c68a-180">IP address/FQDN host record</span></span></th>
<th><span data-ttu-id="1c68a-181">マップ先/コメント</span><span class="sxs-lookup"><span data-stu-id="1c68a-181">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1c68a-182">外部 DNS/SRV/5269</span><span class="sxs-lookup"><span data-stu-id="1c68a-182">External DNS/SRV/5269</span></span></p></td>
<td><p><span data-ttu-id="1c68a-183">_xmpp-server._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="1c68a-183">_xmpp-server._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="1c68a-184">xmpp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="1c68a-184">xmpp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="1c68a-185">アクセスエッジサービスまたはエッジプールの XMPP プロキシ外部インターフェイス。グローバルポリシー、ユーザーが配置されているサイトポリシー、または Lync 対応ユーザーに適用されているユーザーポリシーを通じて、外部アクセスポリシーの構成を通じて、すべての内部 SIP ドメインで、必要に応じてこの手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="1c68a-185">XMPP proxy external interface on the Access Edge service or Edge pool.Repeat as necessary for all internal SIP domains with Lync enabled users where contact with XMPP contacts is allowed through the configuration of the External Access Policy through a global policy, site policy where the user is located, or user policy applied to the Lync-enabled user.</span></span> <span data-ttu-id="1c68a-186">許可されている XMPP ドメインは、XMPP フェデレーションパートナーポリシーでも構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1c68a-186">An allowed XMPP domain must also be configured in the XMPP Federated Partners policy.</span></span> <span data-ttu-id="1c68a-187">詳細については、 <strong>「</strong> 関連項目」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1c68a-187">See topics in <strong>See Also</strong> for additional details</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c68a-188">外部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="1c68a-188">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="1c68a-189">xmpp.contoso.com (など)</span><span class="sxs-lookup"><span data-stu-id="1c68a-189">xmpp.contoso.com (for example)</span></span></p></td>
<td><p><span data-ttu-id="1c68a-190">エッジサーバーまたは XMPP プロキシをホストしているエッジプールのアクセスエッジサービスの IP アドレス</span><span class="sxs-lookup"><span data-stu-id="1c68a-190">IP address of Access Edge service on your Edge Server or Edge pool hosting XMPP proxy</span></span></p></td>
<td><p><span data-ttu-id="1c68a-191">XMPP プロキシサービスをホストしているアクセスエッジサービスまたはエッジプールへのポイント。</span><span class="sxs-lookup"><span data-stu-id="1c68a-191">Points to the Access Edge service or Edge pool that hosts the XMPP proxy service.</span></span> <span data-ttu-id="1c68a-192">通常、作成した SRV レコードは、このホスト (A または AAAA) レコードをポイントします。</span><span class="sxs-lookup"><span data-stu-id="1c68a-192">Typically, the SRV record that you create will point to this host (A or AAAA) record</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="1c68a-193">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1c68a-193">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

