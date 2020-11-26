---
title: 'Lync Server 2013: トポロジの選択'
description: 'Lync Server 2013: トポロジを選択します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Choosing a topology
ms:assetid: 23f2aeb6-fed9-4349-8fba-dcbf18ee4b04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425716(v=OCS.15)
ms:contentKeyID: 48183634
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 01ded739c3c5e4e0bd8c0f25f3f0fe8ff1f350b9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434909"
---
# <a name="choosing-a-topology-in-lync-server-2013"></a><span data-ttu-id="97cb2-103">Lync Server 2013 でのトポロジの選択</span><span class="sxs-lookup"><span data-stu-id="97cb2-103">Choosing a topology in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span data-ttu-id="97cb2-104">_**最終更新日:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="97cb2-104">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="97cb2-105">トポロジを選択する場合は、次のサポートされているトポロジオプションのいずれかを使用できます。</span><span class="sxs-lookup"><span data-stu-id="97cb2-105">When you choose a topology, you can use one the following supported topology options:</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="97cb2-106">特に記載がない限り、Microsoft Lync Server 2010 を使用している場合は、次のガイダンスがほとんど変更されていないことがわかります。</span><span class="sxs-lookup"><span data-stu-id="97cb2-106">Unless otherwise noted, if you have experience with Microsoft Lync Server 2010, you will find the guidance here is largely unchanged.</span></span>



</div>

  - [<span data-ttu-id="97cb2-107">Lync Server 2013 におけるプライベート IP アドレスと NAT を用いた単一統合エッジ</span><span class="sxs-lookup"><span data-stu-id="97cb2-107">Single consolidated edge with private IP addresses and NAT in Lync Server 2013</span></span>](lync-server-2013-single-consolidated-edge-with-private-ip-addresses-and-nat.md)

  - [<span data-ttu-id="97cb2-108">Lync Server 2013 のパブリック IP アドレスを使用する単一統合エッジ</span><span class="sxs-lookup"><span data-stu-id="97cb2-108">Single consolidated edge with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-single-consolidated-edge-with-public-ip-addresses.md)

  - [<span data-ttu-id="97cb2-109">Lync Server 2013 における拡張統合エッジ、NAT によるプライベート IP アドレスを使用した DNS 負荷分散</span><span class="sxs-lookup"><span data-stu-id="97cb2-109">Scaled consolidated edge, DNS load balancing with private IP addresses using NAT in Lync Server 2013</span></span>](lync-server-2013-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat.md)

  - [<span data-ttu-id="97cb2-110">Lync Server 2013 での拡張統合エッジ、パブリック IP アドレスによる DNS 負荷分散</span><span class="sxs-lookup"><span data-stu-id="97cb2-110">Scaled consolidated edge, DNS load balancing with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses.md)

  - [<span data-ttu-id="97cb2-111">Lync Server 2013 のハードウェア ロード バランサーによる拡張統合エッジ</span><span class="sxs-lookup"><span data-stu-id="97cb2-111">Scaled consolidated edge with hardware load balancers in Lync Server 2013</span></span>](lync-server-2013-scaled-consolidated-edge-with-hardware-load-balancers.md)

<div>


> [!IMPORTANT]
> <span data-ttu-id="97cb2-112">内部エッジ インターフェイスと外部エッジ インターフェイスでは、同じ種類のロード バランシングを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="97cb2-112">The internal Edge interface and external Edge interface must use the same type of load balancing.</span></span> <span data-ttu-id="97cb2-113">1 つのエッジ インターフェイスで DNS ロード バランシングを使用し、もう 1 つのエッジ インターフェイスでロード バランサー機器を使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="97cb2-113">You cannot use DNS load balancing on one Edge interface and hardware load balancing on the other Edge interface.</span></span>



</div>

<span data-ttu-id="97cb2-114">次の表は、サポートされている Microsoft Lync Server 2013 トポロジで利用できる機能をまとめたものです。</span><span class="sxs-lookup"><span data-stu-id="97cb2-114">The following table summarizes the functionality available with the supported Microsoft Lync Server 2013 topologies.</span></span> <span data-ttu-id="97cb2-115">列見出しは、特定の Edge 構成オプションで使用できる機能を示します。</span><span class="sxs-lookup"><span data-stu-id="97cb2-115">The column headings indicate the functionality available for a given Edge configuration option.</span></span> <span data-ttu-id="97cb2-116">スケーリングされたエッジ (DNS load 平衡) オプションを使用すると、高可用性をサポートしていること、ルーティング可能ではないプライベート IP アドレス (NAT を含む)、またはエッジの外部インターフェイスに割り当てられているルーティング可能なパブリック IP アドレスを使用できることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="97cb2-116">Using the Scaled Edge (DNS load balanced) option as an example, you can see that it supports high availability, can use non-routable private IP addresses (with NAT) or routable public IP addresses assigned to the Edge external interfaces, and reduces cost because a hardware load balancer is not required.</span></span>

<span data-ttu-id="97cb2-117">DNS の負荷分散でサポートされるエッジフェールオーバーシナリオには、lync 間のポイントツーポイントセッション、Lync 会議セッション、Lync 間のセッション、Office 365、Microsoft 365 があります。</span><span class="sxs-lookup"><span data-stu-id="97cb2-117">Edge failover scenarios supported with DNS Load Balancing are Lync-to-Lync point-to-point sessions, Lync conferencing sessions, Lync-to-PSTN sessions, Office 365, and Microsoft 365.</span></span> <span data-ttu-id="97cb2-118">DNS 負荷分散のメリットが得られないエッジフェールオーバーのシナリオは、リモートユーザーの Exchange ユニファイドメッセージング (UM 2010)、パブリックインスタントメッセージング (IM) 接続、Office Communications Server を実行しているサーバーとのフェデレーションなどのフェールオーバーです。</span><span class="sxs-lookup"><span data-stu-id="97cb2-118">Edge failover scenarios that do not benefit from DNS Load Balancing are failover for remote user Exchange Unified Messaging (UM) (prior to Exchange 2010 SP1), public instant messaging (IM) connectivity, and federation with servers running Office Communications Server.</span></span>

### <a name="summary-of-edge-server-topology-options"></a><span data-ttu-id="97cb2-119">エッジサーバーのトポロジオプションの概要</span><span class="sxs-lookup"><span data-stu-id="97cb2-119">Summary of Edge Server Topology Options</span></span>

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
<th><span data-ttu-id="97cb2-120">トポロジ</span><span class="sxs-lookup"><span data-stu-id="97cb2-120">Topology</span></span></th>
<th><span data-ttu-id="97cb2-121">高可用性</span><span class="sxs-lookup"><span data-stu-id="97cb2-121">High availability</span></span></th>
<th><span data-ttu-id="97cb2-122">追加 DNS A Edge プールの外部エッジサーバーに必要なレコード</span><span class="sxs-lookup"><span data-stu-id="97cb2-122">Additional DNS A records required for external Edge Server in the Edge pool</span></span></th>
<th><span data-ttu-id="97cb2-123">Lync to Lync セッションのエッジフェールオーバー</span><span class="sxs-lookup"><span data-stu-id="97cb2-123">Edge Failover for Lync-to-Lync sessions</span></span></th>
<th><span data-ttu-id="97cb2-124">Lync 対 Lync EUM/PIC/OCS フェデレーションセッションのエッジフェールオーバー</span><span class="sxs-lookup"><span data-stu-id="97cb2-124">Edge Failover for Lync-to-Lync EUM/PIC/OCS Federation sessions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="97cb2-125">NAT を使用する単一エッジ</span><span class="sxs-lookup"><span data-stu-id="97cb2-125">Single Edge using NAT</span></span></p></td>
<td><p><span data-ttu-id="97cb2-126">いいえ</span><span class="sxs-lookup"><span data-stu-id="97cb2-126">No</span></span></p></td>
<td><p><span data-ttu-id="97cb2-127">いいえ</span><span class="sxs-lookup"><span data-stu-id="97cb2-127">No</span></span></p></td>
<td><p><span data-ttu-id="97cb2-128">いいえ</span><span class="sxs-lookup"><span data-stu-id="97cb2-128">No</span></span></p></td>
<td><p><span data-ttu-id="97cb2-129">いいえ</span><span class="sxs-lookup"><span data-stu-id="97cb2-129">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97cb2-130">パブリック IP を使った単一エッジ</span><span class="sxs-lookup"><span data-stu-id="97cb2-130">Single Edge using Public IP</span></span></p></td>
<td><p><span data-ttu-id="97cb2-131">いいえ</span><span class="sxs-lookup"><span data-stu-id="97cb2-131">No</span></span></p></td>
<td><p><span data-ttu-id="97cb2-132">いいえ</span><span class="sxs-lookup"><span data-stu-id="97cb2-132">No</span></span></p></td>
<td><p><span data-ttu-id="97cb2-133">いいえ</span><span class="sxs-lookup"><span data-stu-id="97cb2-133">No</span></span></p></td>
<td><p><span data-ttu-id="97cb2-134">いいえ</span><span class="sxs-lookup"><span data-stu-id="97cb2-134">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97cb2-135">NAT を使用した拡張エッジ (DNS 負荷分散)</span><span class="sxs-lookup"><span data-stu-id="97cb2-135">Scaled Edge (DNS Load Balanced) using NAT</span></span></p></td>
<td><p><span data-ttu-id="97cb2-136">はい</span><span class="sxs-lookup"><span data-stu-id="97cb2-136">Yes</span></span></p></td>
<td><p><span data-ttu-id="97cb2-137">はい</span><span class="sxs-lookup"><span data-stu-id="97cb2-137">Yes</span></span></p></td>
<td><p><span data-ttu-id="97cb2-138">はい</span><span class="sxs-lookup"><span data-stu-id="97cb2-138">Yes</span></span></p></td>
<td><p>*</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97cb2-139">パブリック IP を使った拡張エッジ (DNS 負荷分散)</span><span class="sxs-lookup"><span data-stu-id="97cb2-139">Scaled Edge (DNS Load Balanced) using Public IP</span></span></p></td>
<td><p><span data-ttu-id="97cb2-140">はい</span><span class="sxs-lookup"><span data-stu-id="97cb2-140">Yes</span></span></p></td>
<td><p><span data-ttu-id="97cb2-141">はい</span><span class="sxs-lookup"><span data-stu-id="97cb2-141">Yes</span></span></p></td>
<td><p><span data-ttu-id="97cb2-142">はい</span><span class="sxs-lookup"><span data-stu-id="97cb2-142">Yes</span></span></p></td>
<td><p>*</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97cb2-143">スケーリングされたエッジハードウェアの負荷分散)</span><span class="sxs-lookup"><span data-stu-id="97cb2-143">Scaled Edge Hardware load balanced)</span></span></p></td>
<td><p><span data-ttu-id="97cb2-144">はい</span><span class="sxs-lookup"><span data-stu-id="97cb2-144">Yes</span></span></p></td>
<td><p><span data-ttu-id="97cb2-145">× (VIP ごとに 1 つの DNS A レコード)</span><span class="sxs-lookup"><span data-stu-id="97cb2-145">No (one DNS A record per VIP)</span></span></p></td>
<td><p><span data-ttu-id="97cb2-146">はい</span><span class="sxs-lookup"><span data-stu-id="97cb2-146">Yes</span></span></p></td>
<td><p><span data-ttu-id="97cb2-147">はい</span><span class="sxs-lookup"><span data-stu-id="97cb2-147">Yes</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="97cb2-148">\**\** _ パブリックインスタントメッセージング (IM) 接続のためのフェールオーバー、および Office Communications Server を実行しているサーバーとのフェデレーションは、DNS の負荷分散では使用できません。</span><span class="sxs-lookup"><span data-stu-id="97cb2-148">\**\** _ Failover for public instant messaging (IM) connectivity, and federation with servers running Office Communications Server is not available with DNS load balancing.</span></span> <span data-ttu-id="97cb2-149">DNS 負荷分散を使用した exchange UM (リモートユーザー) のフェールオーバーには、Exchange Server 2010 SP1 以上が必要です。</span><span class="sxs-lookup"><span data-stu-id="97cb2-149">Exchange UM (remote user) failover using DNS load balancing requires Exchange Server 2010 SP1 or newer.</span></span>



> [!NOTE]
> <span data-ttu-id="97cb2-150">単一のエッジとスケーリングされたエッジ (DNS 負荷分散) には、次のような用途があります。</span><span class="sxs-lookup"><span data-stu-id="97cb2-150">Single Edge and Scaled Edge (DNS load balanced) topologies can use:</span></span>
> <ul><li><p><span data-ttu-id="97cb2-151">ルーティング可能なパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="97cb2-151">Routable public IP addresses</span></span></p></li>
> <li><p><span data-ttu-id="97cb2-152">対称ネットワークアドレス変換 (NAT) が使用されている場合、ルーティング可能ではないプライベート IP アドレス</span><span class="sxs-lookup"><span data-stu-id="97cb2-152">Non-routable private IP address if symmetric network address translation (NAT) is used</span></span></p></li>
>
> <ul><li> <span data-ttu-id="97cb2-153">NAT でパブリック IP アドレスまたはプライベート IP アドレスを使用している場合でも、トポロジビルダーの構成の選択に基づいて、同じ数の IP アドレスを使用します。</span><span class="sxs-lookup"><span data-stu-id="97cb2-153">If you use public IP address or private IP address with NAT, you will still use the same number of IP addresses based on your configuration choice in Topology Builder.</span></span> <span data-ttu-id="97cb2-154">サービスごとに個別のポートを使用するようにエッジサーバーを構成することも、サービスごとに個別の IP アドレスを使用することもできますが、同じポート (既定では TCP 443) を使うことができます。</span><span class="sxs-lookup"><span data-stu-id="97cb2-154">You can configure the Edge Server to use a single IP address with distinct ports per service, or use distinct IP addresses per service, but use the same port (by default, TCP 443).</span></span></li></ul>>
> <span data-ttu-id="97cb2-155">NAT でルーティング不能なプライベート IP アドレスを使用する場合は、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="97cb2-155">If you decide to use non-routable private IP addresses with NAT:</span></span>
> <ul><li><p><span data-ttu-id="97cb2-156">ルーティング可能なプライベート IP アドレスは、すべての3つの外部インターフェイスで使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="97cb2-156">You must use routable private IP addresses on all three external interfaces</span></span></p></li>
> <li><p><span data-ttu-id="97cb2-157">受信および送信トラフィック用に対称 NAT を構成する必要がある</span><span class="sxs-lookup"><span data-stu-id="97cb2-157">You must configure symmetric NAT for incoming and outgoing traffic</span></span></p></li></ul>>
> <span data-ttu-id="97cb2-158">スケーリングされたエッジ (ハードウェア負荷分散) トポロジでは、パブリック IP アドレスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="97cb2-158">Scaled Edge (hardware load balanced) topology must use public IP addresses.</span></span>



<span data-ttu-id="97cb2-159">Lync Server 2013 は、ネットワークアドレス変換 (NAT) を実行するルーターまたはファイアウォールの背後にあるアクセス、Web 会議、および A/V Edge の外部インターフェイスの配置をサポートしています。統合されたエッジサーバートポロジの1つとスケーリングの両方に対応しています。</span><span class="sxs-lookup"><span data-stu-id="97cb2-159">Lync Server 2013 supports placing Access, Web Conferencing, and A/V Edge external interfaces behind a router or firewall that performs network address translation (NAT) for both single and scaled consolidated Edge Server topologies.</span></span>

<span data-ttu-id="97cb2-160">すべてのエッジに NAT を使用するには、DNS の負荷分散を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="97cb2-160">Using NAT for all Edge external interfaces requires the use of DNS load balancing.</span></span> <span data-ttu-id="97cb2-161">ハードウェアロードバランサーの使用と比較した場合、DNS の負荷分散を使用すると、次の一覧に示すように、エッジプールでエッジサーバーあたりのパブリック IP アドレスの数を減らすことができます。</span><span class="sxs-lookup"><span data-stu-id="97cb2-161">When compared to using hardware load balancers, using DNS load balancing without NAT allows you to reduce the number of public IP address per Edge Server in an Edge pool as described in the following list:</span></span>

  - <span data-ttu-id="97cb2-162">Lync Server 2013 の統合エッジ (DNS 負荷分散) には、Edge プールのエッジサーバーごとに3つのパブリック IP アドレスが必要です。</span><span class="sxs-lookup"><span data-stu-id="97cb2-162">Lync Server 2013 Scaled Consolidated Edge (DNS load balanced) Requires three public IP addresses for each Edge Server in an Edge pool.</span></span>

  - <span data-ttu-id="97cb2-163">Lync Server 2013 の統合されたエッジ (ハードウェア負荷分散) には、ロードバランサー仮想 IP アドレス用の3つのパブリック IP アドレス (プールに追加されたエッジサーバーの数が多い場合は1回の要件) とプール内のエッジサーバーあたりの3つのパブリック IP アドレスが必要です。</span><span class="sxs-lookup"><span data-stu-id="97cb2-163">Lync Server 2013 Scaled Consolidated Edge (hardware load balanced) Requires three public IP address for load balancer virtual IP addresses (one time requirement that does not increment as more Edge Servers are added to the pool) plus three public IP addresses per Edge Server in a pool.</span></span>

### <a name="ip-address-requirements-for-scaled-consolidated-edge-ip-address-per-role"></a><span data-ttu-id="97cb2-164">スケーリングされた統合エッジの IP アドレス要件 (役割ごとの IP アドレス)</span><span class="sxs-lookup"><span data-stu-id="97cb2-164">IP Address Requirements for Scaled Consolidated Edge (IP Address per role)</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="97cb2-165">1つのプールあたりのエッジサーバーの数</span><span class="sxs-lookup"><span data-stu-id="97cb2-165">Number of Edge Servers per pool</span></span></th>
<th><span data-ttu-id="97cb2-166">必要な IP アドレスの数 Lync Server 2013 (DNS 負荷分散)</span><span class="sxs-lookup"><span data-stu-id="97cb2-166">Number of required IP addresses Lync Server 2013 (DNS load balanced)</span></span></th>
<th><span data-ttu-id="97cb2-167">必要な IP アドレスの数 Lync Server 2013 (ハードウェアの負荷分散)</span><span class="sxs-lookup"><span data-stu-id="97cb2-167">Number of required IP addresses Lync Server 2013 (hardware load balanced)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="97cb2-168">2</span><span class="sxs-lookup"><span data-stu-id="97cb2-168">2</span></span></p></td>
<td><p><span data-ttu-id="97cb2-169">6</span><span class="sxs-lookup"><span data-stu-id="97cb2-169">6</span></span></p></td>
<td><p><span data-ttu-id="97cb2-170">3 (VIP ごとに 1 つ) + 6</span><span class="sxs-lookup"><span data-stu-id="97cb2-170">3 (1 per VIP) + 6</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97cb2-171">3</span><span class="sxs-lookup"><span data-stu-id="97cb2-171">3</span></span></p></td>
<td><p><span data-ttu-id="97cb2-172">ファイブ</span><span class="sxs-lookup"><span data-stu-id="97cb2-172">9</span></span></p></td>
<td><p><span data-ttu-id="97cb2-173">3 (VIP ごとに 1 つ) + 9</span><span class="sxs-lookup"><span data-stu-id="97cb2-173">3 (1 per VIP) + 9</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97cb2-174">4</span><span class="sxs-lookup"><span data-stu-id="97cb2-174">4</span></span></p></td>
<td><p><span data-ttu-id="97cb2-175">以内</span><span class="sxs-lookup"><span data-stu-id="97cb2-175">12</span></span></p></td>
<td><p><span data-ttu-id="97cb2-176">3 (VIP ごとに 1 つ) + 12</span><span class="sxs-lookup"><span data-stu-id="97cb2-176">3 (1 per VIP) + 12</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97cb2-177">5</span><span class="sxs-lookup"><span data-stu-id="97cb2-177">5</span></span></p></td>
<td><p><span data-ttu-id="97cb2-178">マート</span><span class="sxs-lookup"><span data-stu-id="97cb2-178">15</span></span></p></td>
<td><p><span data-ttu-id="97cb2-179">3 (VIP あたり 1) + 15</span><span class="sxs-lookup"><span data-stu-id="97cb2-179">3 (1 per VIP) + 15</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="ip-address-requirements-for-scaled-consolidated-edge-single-ip-address-for-all-roles"></a><span data-ttu-id="97cb2-180">スケーリングされた統合エッジの IP アドレス要件 (すべての役割の単一 IP アドレス)</span><span class="sxs-lookup"><span data-stu-id="97cb2-180">IP Address Requirements for Scaled Consolidated Edge (Single IP address for all roles)</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="97cb2-181">1つのプールあたりのエッジサーバーの数</span><span class="sxs-lookup"><span data-stu-id="97cb2-181">Number of Edge Servers per pool</span></span></th>
<th><span data-ttu-id="97cb2-182">必要な IP アドレスの数 Lync Server 2013 (DNS 負荷分散)</span><span class="sxs-lookup"><span data-stu-id="97cb2-182">Number of required IP addresses Lync Server 2013 (DNS load balanced)</span></span></th>
<th><span data-ttu-id="97cb2-183">必要な IP アドレスの数 Lync Server 2013 (ハードウェアの負荷分散)</span><span class="sxs-lookup"><span data-stu-id="97cb2-183">Number of required IP addresses Lync Server 2013 (hardware load balanced)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="97cb2-184">2</span><span class="sxs-lookup"><span data-stu-id="97cb2-184">2</span></span></p></td>
<td><p><span data-ttu-id="97cb2-185">2</span><span class="sxs-lookup"><span data-stu-id="97cb2-185">2</span></span></p></td>
<td><p><span data-ttu-id="97cb2-186">1 (VIP ごとに 1 つ) + 2</span><span class="sxs-lookup"><span data-stu-id="97cb2-186">1 (1 per VIP) + 2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97cb2-187">3</span><span class="sxs-lookup"><span data-stu-id="97cb2-187">3</span></span></p></td>
<td><p><span data-ttu-id="97cb2-188">3</span><span class="sxs-lookup"><span data-stu-id="97cb2-188">3</span></span></p></td>
<td><p><span data-ttu-id="97cb2-189">1 (VIP ごとに 1 つ) + 3</span><span class="sxs-lookup"><span data-stu-id="97cb2-189">1 (1 per VIP) + 3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97cb2-190">4</span><span class="sxs-lookup"><span data-stu-id="97cb2-190">4</span></span></p></td>
<td><p><span data-ttu-id="97cb2-191">4</span><span class="sxs-lookup"><span data-stu-id="97cb2-191">4</span></span></p></td>
<td><p><span data-ttu-id="97cb2-192">1 (VIP ごとに 1 つ) + 4</span><span class="sxs-lookup"><span data-stu-id="97cb2-192">1 (1 per VIP) + 4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97cb2-193">5</span><span class="sxs-lookup"><span data-stu-id="97cb2-193">5</span></span></p></td>
<td><p><span data-ttu-id="97cb2-194">5</span><span class="sxs-lookup"><span data-stu-id="97cb2-194">5</span></span></p></td>
<td><p><span data-ttu-id="97cb2-195">1 (VIP ごとに 1 つ) + 5</span><span class="sxs-lookup"><span data-stu-id="97cb2-195">1 (1 per VIP) + 5</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="97cb2-196">トポロジ選択の主要な決定ポイントは、高可用性と負荷分散です。</span><span class="sxs-lookup"><span data-stu-id="97cb2-196">The primary decision points for topology selection are high availability and load balancing.</span></span> <span data-ttu-id="97cb2-197">高可用性の要件は、負荷分散の決定に影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="97cb2-197">The requirement for high availability can influence the load balancing decision.</span></span>

  - <span data-ttu-id="97cb2-198">@*高* 可用性 \* 高可用性が必要な場合は、少なくとも2台のエッジサーバーをプールに展開します。</span><span class="sxs-lookup"><span data-stu-id="97cb2-198">_ *High availability*\*   If you need high availability, deploy at least two Edge Servers in a pool.</span></span> <span data-ttu-id="97cb2-199">1つのエッジプールは、最大12台のエッジサーバーをサポートします。</span><span class="sxs-lookup"><span data-stu-id="97cb2-199">A single Edge pool will support up to twelve Edge Servers.</span></span> <span data-ttu-id="97cb2-200">さらに多くの容量が必要な場合は、複数のエッジプールを展開できます。</span><span class="sxs-lookup"><span data-stu-id="97cb2-200">If more capacity is required, you can deploy multiple Edge pools.</span></span> <span data-ttu-id="97cb2-201">一般的な規則として、特定のユーザーベースの10% には外部アクセスが必要です。</span><span class="sxs-lookup"><span data-stu-id="97cb2-201">As a general rule, 10% of a given user base will need external access.</span></span>
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="97cb2-202">トポロジビルダーを使用すると、1つのエッジプールで最大20台のエッジサーバーを構成できます。</span><span class="sxs-lookup"><span data-stu-id="97cb2-202">Topology Builder will allow you to configure up to twenty Edge Servers in a single Edge pool.</span></span> <span data-ttu-id="97cb2-203">プール内のエッジサーバーのうち、テストおよびサポートされている最大数は12個とトポロジービルダーで、1つのエッジプールで12台以上のエッジサーバーに対して暗示的なサポートを行うことはできません。</span><span class="sxs-lookup"><span data-stu-id="97cb2-203">The tested and supported maximum number of Edge Servers in a pool is twelve and Topology Builder allowing for a number larger than twelve should not be construed as implied support for more than twelve Edge Servers in a single Edge pool.</span></span>

    
    </div>

  - <span data-ttu-id="97cb2-204">**ハードウェア負荷分散**   エッジ外部インターフェイスに対してパブリックルーティング可能な IP アドレスを使用している場合、ハードウェア負荷分散がサポートさ2013れます。</span><span class="sxs-lookup"><span data-stu-id="97cb2-204">**Hardware load balancing**   Hardware load balancing is supported for load balancing Lync Server 2013 Edge Servers when using publicly routable IP addresses for the Edge external interfaces.</span></span> <span data-ttu-id="97cb2-205">たとえば、次のいずれかのアプリケーションでフェールオーバーが必要な場合に、この方法を使用します。</span><span class="sxs-lookup"><span data-stu-id="97cb2-205">For example, you would use this approach in situations where failover is required for any of the following applications:</span></span>
    
      - <span data-ttu-id="97cb2-206">パブリック IM 接続</span><span class="sxs-lookup"><span data-stu-id="97cb2-206">Public IM connectivity</span></span>
    
      - <span data-ttu-id="97cb2-207">Microsoft Office Communications Server 2007 または Microsoft Office Communications Server 2007 R2 を実行している企業とのフェデレーション</span><span class="sxs-lookup"><span data-stu-id="97cb2-207">Federation with companies running Microsoft Office Communications Server 2007 or Microsoft Office Communications Server 2007 R2</span></span>
    
      - <span data-ttu-id="97cb2-208">Exchange 2007 ユニファイドメッセージング (UM) または Exchange 2010 UM への外部アクセス</span><span class="sxs-lookup"><span data-stu-id="97cb2-208">External access to Exchange 2007 Unified Messaging (UM) or Exchange 2010 UM</span></span>
        
        <div>
        

        > [!IMPORTANT]
        > <span data-ttu-id="97cb2-209">Exchange 2010 SP1 以降の DNS の負荷分散は、Exchange UM でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="97cb2-209">DNS load balancing for Exchange 2010 SP1 and newer is supported for Exchange UM.</span></span>

        
        </div>
    
    <span data-ttu-id="97cb2-210">これら3つのアプリケーションは引き続き動作しますが、DNS の負荷分散に対応しておらず、プールの最初のエッジサーバーにのみ接続されます。</span><span class="sxs-lookup"><span data-stu-id="97cb2-210">These three applications will continue to operate, but they are not DNS load balancing aware and will only connect to the first Edge Server in the pool.</span></span> <span data-ttu-id="97cb2-211">そのサーバーが利用できない場合、接続は失敗します。</span><span class="sxs-lookup"><span data-stu-id="97cb2-211">If that server is unavailable, the connection will fail.</span></span> <span data-ttu-id="97cb2-212">たとえば、フェデレーションされたトラフィックの負荷を処理するために複数のエッジサーバーがプールに展開されている場合、他のユーザーがアイドル状態になっている間、実際にトラフィックを受信するのは1つのアクセスプロキシだけです。</span><span class="sxs-lookup"><span data-stu-id="97cb2-212">For example, if multiple Edge Servers are deployed in a pool to handle the federated traffic load, only one access proxy actually receives traffic while the others are idle.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="97cb2-213">Lync Server 2010 および Office 365 または Microsoft 365 を使用して会社とフェデレーションする場合は、DNS の負荷分散を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="97cb2-213">Using DNS load balancing is recommended if you are federating with companies using Lync Server 2010 and Office 365 or Microsoft 365.</span></span> <span data-ttu-id="97cb2-214">フェデレーションパートナーの大半が Office Communications Server 2007 または Office Communications Server 2007 R2 を使用している場合、パフォーマンスへの影響が大きくなることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="97cb2-214">Be aware that there are significant performance impacts if most of your federated partners are using Office Communications Server 2007 or Office Communications Server 2007 R2.</span></span>



<span data-ttu-id="97cb2-215"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="97cb2-215"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

