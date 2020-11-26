---
title: 'Lync Server 2013: ポートの概要 - 拡張統合エッジ、パブリック IP アドレスによる DNS 負荷分散'
description: 'Lync Server 2013: ポートの概要-統合されたエッジ、パブリック IP アドレスを使った DNS の負荷分散。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Scaled consolidated edge, DNS load balancing with public IP addresses
ms:assetid: f7cbd0f1-841d-4116-8d17-e9d991daa4a8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205394(v=OCS.15)
ms:contentKeyID: 48185865
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8090435485b4b6a183702a608b139cec91ae26a7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446340"
---
# <a name="port-summary---scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses-in-lync-server-2013"></a><span data-ttu-id="0a3b0-103">ポートの概要 - Lync Server 2013 拡張統合エッジ、パブリック IP アドレスによる DNS 負荷分散</span><span class="sxs-lookup"><span data-stu-id="0a3b0-103">Port summary - Scaled consolidated edge, DNS load balancing with public IP addresses in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0a3b0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0a3b0-104">

<span> </span></span></span>

<span data-ttu-id="0a3b0-105">_**最終更新日:** 2013-04-03_</span><span class="sxs-lookup"><span data-stu-id="0a3b0-105">_**Topic Last Modified:** 2013-04-03_</span></span>

<span data-ttu-id="0a3b0-106">このシナリオアーキテクチャで説明されている Lync Server 2013 のエッジサーバー機能は、Lync Server 2010 で実装されたものとよく似ています。</span><span class="sxs-lookup"><span data-stu-id="0a3b0-106">The Lync Server 2013, Edge Server functionality described in this scenario architecture is very similar to what was implemented in Lync Server 2010.</span></span> <span data-ttu-id="0a3b0-107">最も顕著な追加機能は、拡張メッセージングとプレゼンスプロトコル (XMPP) の TCP エントリのポート **5269** です。</span><span class="sxs-lookup"><span data-stu-id="0a3b0-107">The most noticeable addition is the port **5269 over TCP** entry for the extensible messaging and presence protocol (XMPP).</span></span> <span data-ttu-id="0a3b0-108">Lync Server 2013 では、必要に応じて、microsoft Edge サーバーまたはエッジプールに XMPP プロキシを展開し、フロントエンドサーバーまたはフロントエンドプールに XMPP ゲートウェイサーバーを配置します。</span><span class="sxs-lookup"><span data-stu-id="0a3b0-108">Lync Server 2013 optionally deploys an XMPP proxy on the Edge Server or Edge pool and the XMPP gateway server on the Front End Server or Front End pool.</span></span>

<span data-ttu-id="0a3b0-109">IPv4 に加えて、エッジサーバーは IPv6 をサポートするようになりました。</span><span class="sxs-lookup"><span data-stu-id="0a3b0-109">In addition to IPv4, the Edge Server now supports IPv6.</span></span> <span data-ttu-id="0a3b0-110">わかりやすくするために、シナリオでは IPv4 のみが使用されます。</span><span class="sxs-lookup"><span data-stu-id="0a3b0-110">For clarity, only IPv4 is used in the scenarios.</span></span>

<span data-ttu-id="0a3b0-111">**拡張統合エッジのエンタープライズ境界ネットワーク、パブリック IP アドレスを使った DNS 負荷分散**</span><span class="sxs-lookup"><span data-stu-id="0a3b0-111">**Enterprise perimeter network for Scaled Consolidated Edge, DNS Load Balancing with Public IP Addresses**</span></span>

<span data-ttu-id="0a3b0-112">![96f5a8f5-16d2-464d-b86e-7c7ecfc89ead](images/JJ205394.96f5a8f5-16d2-464d-b86e-7c7ecfc89ead(OCS.15).jpg "96f5a8f5-16d2-464d-b86e-7c7ecfc89ead")</span><span class="sxs-lookup"><span data-stu-id="0a3b0-112">![96f5a8f5-16d2-464d-b86e-7c7ecfc89ead](images/JJ205394.96f5a8f5-16d2-464d-b86e-7c7ecfc89ead(OCS.15).jpg "96f5a8f5-16d2-464d-b86e-7c7ecfc89ead")</span></span>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="0a3b0-113">ポートとプロトコルの詳細</span><span class="sxs-lookup"><span data-stu-id="0a3b0-113">Port and Protocol Details</span></span>

<span data-ttu-id="0a3b0-114">外部アクセスを提供する機能をサポートするために必要なポートのみを開くことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="0a3b0-114">It is recommended that you open only the ports required to support the functionality for which you are providing external access.</span></span>

<span data-ttu-id="0a3b0-115">エッジサービスに対してリモートアクセスを使用するには、受信/送信エッジトラフィックの図に示すように、SIP トラフィックが双方向に流れるようにすることが必須です。</span><span class="sxs-lookup"><span data-stu-id="0a3b0-115">For remote access to work for any edge service, it is mandatory that SIP traffic is allowed to flow bi-directionally as shown in the Inbound/Outbound edge traffic figure.</span></span> <span data-ttu-id="0a3b0-116">別の方法として、アクセスエッジサービスとの間の SIP メッセージングは、インスタントメッセージング (IM)、プレゼンス、web 会議、音声/ビデオ (A/V)、およびフェデレーションに関連しています。</span><span class="sxs-lookup"><span data-stu-id="0a3b0-116">Stated another way, the SIP messaging to and from the Access Edge service is involved in instant messaging (IM), presence, web conferencing, audio/video (A/V) and federation.</span></span>

### <a name="firewall-summary-for-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses-external-interface--node-1-and-node-2-example"></a><span data-ttu-id="0a3b0-117">拡張された統合エッジのファイアウォールの概要、パブリック IP アドレスを使った DNS 負荷分散: ノード1とノード 2 (例)</span><span class="sxs-lookup"><span data-stu-id="0a3b0-117">Firewall Summary for Scaled Consolidated Edge, DNS Load Balancing with Public IP Addresses: External Interface – Node 1 and Node 2 (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0a3b0-118">Role/Protocol/TCP または UDP/ポート</span><span class="sxs-lookup"><span data-stu-id="0a3b0-118">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="0a3b0-119">送信元 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-119">Source IP address</span></span></th>
<th><span data-ttu-id="0a3b0-120">宛先 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-120">Destination IP address</span></span></th>
<th><span data-ttu-id="0a3b0-121">メモ</span><span class="sxs-lookup"><span data-stu-id="0a3b0-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0a3b0-122">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="0a3b0-122">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-123">任意</span><span class="sxs-lookup"><span data-stu-id="0a3b0-123">Any</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-124">XMPP プロキシサービス (アクセスエッジサービスで IP アドレスを共有)</span><span class="sxs-lookup"><span data-stu-id="0a3b0-124">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-125">XMPP プロキシサービスは、定義された XMPP フェデレーションの XMPP 連絡先からのトラフィックを受け入れます。</span><span class="sxs-lookup"><span data-stu-id="0a3b0-125">XMPP Proxy service accepts traffic from XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a3b0-126">Access/HTTP/TCP/80</span><span class="sxs-lookup"><span data-stu-id="0a3b0-126">Access/HTTP/TCP/80</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-127">エッジサーバーアクセスエッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-127">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-128">任意</span><span class="sxs-lookup"><span data-stu-id="0a3b0-128">Any</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-129">証明書の失効/CRL の確認と取得</span><span class="sxs-lookup"><span data-stu-id="0a3b0-129">Certificate revocation/CRL check and retrieval</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a3b0-130">Access/DNS/TCP/53</span><span class="sxs-lookup"><span data-stu-id="0a3b0-130">Access/DNS/TCP/53</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-131">エッジサーバーアクセスエッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-131">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-132">任意</span><span class="sxs-lookup"><span data-stu-id="0a3b0-132">Any</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-133">TCP 経由の DNS クエリ</span><span class="sxs-lookup"><span data-stu-id="0a3b0-133">DNS query over TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a3b0-134">Access/DNS/UDP/53</span><span class="sxs-lookup"><span data-stu-id="0a3b0-134">Access/DNS/UDP/53</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-135">エッジサーバーアクセスエッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-135">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-136">任意</span><span class="sxs-lookup"><span data-stu-id="0a3b0-136">Any</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-137">UDP 経由の DNS クエリ</span><span class="sxs-lookup"><span data-stu-id="0a3b0-137">DNS query over UDP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a3b0-138">アクセス/SIP (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="0a3b0-138">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-139">任意</span><span class="sxs-lookup"><span data-stu-id="0a3b0-139">Any</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-140">エッジサーバーアクセスエッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-140">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-141">外部ユーザーアクセスのクライアントツーサーバー SIP トラフィック</span><span class="sxs-lookup"><span data-stu-id="0a3b0-141">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a3b0-142">アクセス/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="0a3b0-142">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-143">任意</span><span class="sxs-lookup"><span data-stu-id="0a3b0-143">Any</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-144">エッジサーバーアクセスエッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-144">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-145">SIP を使用するフェデレーションおよびパブリック IM 接続の場合</span><span class="sxs-lookup"><span data-stu-id="0a3b0-145">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a3b0-146">アクセス/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="0a3b0-146">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-147">エッジサーバーアクセスエッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-147">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-148">任意</span><span class="sxs-lookup"><span data-stu-id="0a3b0-148">Any</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-149">SIP を使用するフェデレーションおよびパブリック IM 接続の場合</span><span class="sxs-lookup"><span data-stu-id="0a3b0-149">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a3b0-150">Web 会議/PSOM (TLS) TCP/443</span><span class="sxs-lookup"><span data-stu-id="0a3b0-150">Web Conferencing/PSOM(TLS)TCP/443</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-151">任意</span><span class="sxs-lookup"><span data-stu-id="0a3b0-151">Any</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-152">エッジサーバー Web 会議エッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-152">Edge Server Web Conferencing Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-153">Web 会議メディア</span><span class="sxs-lookup"><span data-stu-id="0a3b0-153">Web Conferencing media</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a3b0-154">A/V/RTP/59,999</span><span class="sxs-lookup"><span data-stu-id="0a3b0-154">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-155">エッジサーバーの A/V エッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-155">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-156">任意</span><span class="sxs-lookup"><span data-stu-id="0a3b0-156">Any</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-157">Office Communications Server 2007、Office Communications Server 2007 R2、Lync Server 2010、および Lync Server 2013 を実行しているパートナーとのフェデレーションに必要。</span><span class="sxs-lookup"><span data-stu-id="0a3b0-157">Required for federating with partners running Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a3b0-158">A/V/RTP/59,999</span><span class="sxs-lookup"><span data-stu-id="0a3b0-158">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-159">エッジサーバーの A/V エッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-159">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-160">任意</span><span class="sxs-lookup"><span data-stu-id="0a3b0-160">Any</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-161">Office Communications Server 2007 を実行しているパートナーとのフェデレーションの場合のみ必須です。</span><span class="sxs-lookup"><span data-stu-id="0a3b0-161">Required only for federation with partners running Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a3b0-162">A/V/RTP/59,999</span><span class="sxs-lookup"><span data-stu-id="0a3b0-162">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-163">任意</span><span class="sxs-lookup"><span data-stu-id="0a3b0-163">Any</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-164">エッジサーバーの A/V エッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-164">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-165">Office Communications Server 2007 を実行しているパートナーとのフェデレーションにのみ必須</span><span class="sxs-lookup"><span data-stu-id="0a3b0-165">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a3b0-166">A/V/RTP/59,999</span><span class="sxs-lookup"><span data-stu-id="0a3b0-166">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-167">任意</span><span class="sxs-lookup"><span data-stu-id="0a3b0-167">Any</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-168">エッジサーバーの A/V エッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-168">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-169">Office Communications Server 2007 を実行しているパートナーとのフェデレーションにのみ必須</span><span class="sxs-lookup"><span data-stu-id="0a3b0-169">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a3b0-170">A/V/STUN、MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="0a3b0-170">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-171">エッジサーバーの A/V エッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-171">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-172">任意</span><span class="sxs-lookup"><span data-stu-id="0a3b0-172">Any</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-173">3478送信は、Lync Server が通信するエッジサーバーのバージョンと、エッジサーバーからエッジサーバーへのメディアトラフィックも確認するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="0a3b0-173">3478 outbound is used to determine the version of Edge Server that Lync Server is communicating with and also for media traffic from Edge Server-to-Edge Server.</span></span> <span data-ttu-id="0a3b0-174">Lync Server 2010、Windows Live Messenger、Office Communications Server 2007 R2 とのフェデレーション、および複数のエッジプールが会社内に展開されている場合に必要です。</span><span class="sxs-lookup"><span data-stu-id="0a3b0-174">Required for federation with Lync Server 2010, Windows Live Messenger, and Office Communications Server 2007 R2, and also if multiple Edge pools are deployed within a company.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a3b0-175">A/V/STUN、MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="0a3b0-175">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-176">任意</span><span class="sxs-lookup"><span data-stu-id="0a3b0-176">Any</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-177">エッジサーバーの A/V エッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-177">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-178">UDP/3478 経由の候補のネゴシエーションをオフ/オンにする</span><span class="sxs-lookup"><span data-stu-id="0a3b0-178">STUN/TURN negotiation of candidates over UDP/3478</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a3b0-179">A/V/STUN、MSTURN/443</span><span class="sxs-lookup"><span data-stu-id="0a3b0-179">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-180">任意</span><span class="sxs-lookup"><span data-stu-id="0a3b0-180">Any</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-181">エッジサーバーの A/V エッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-181">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-182">TCP/443 経由での候補のネゴシエーションをオフ/オンにする</span><span class="sxs-lookup"><span data-stu-id="0a3b0-182">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a3b0-183">A/V/STUN、MSTURN/443</span><span class="sxs-lookup"><span data-stu-id="0a3b0-183">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-184">エッジサーバーの A/V Edge サービス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-184">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-185">任意</span><span class="sxs-lookup"><span data-stu-id="0a3b0-185">Any</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-186">TCP/443 経由での候補のネゴシエーションをオフ/オンにする</span><span class="sxs-lookup"><span data-stu-id="0a3b0-186">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-summary-for-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses-internal-interface--node-1-and-node-2-example"></a><span data-ttu-id="0a3b0-187">スケーリングされた統合エッジのファイアウォールの概要、パブリック IP アドレスを使った DNS 負荷分散: ノード1とノード 2 (例)</span><span class="sxs-lookup"><span data-stu-id="0a3b0-187">Firewall Summary for Scaled Consolidated Edge, DNS Load Balancing with Public IP Addresses: Internal Interface – Node 1 and Node 2 (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0a3b0-188">Protocol/TCP または UDP/ポート</span><span class="sxs-lookup"><span data-stu-id="0a3b0-188">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="0a3b0-189">送信元 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-189">Source IP address</span></span></th>
<th><span data-ttu-id="0a3b0-190">宛先 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-190">Destination IP address</span></span></th>
<th><span data-ttu-id="0a3b0-191">注釈</span><span class="sxs-lookup"><span data-stu-id="0a3b0-191">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0a3b0-192">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="0a3b0-192">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-193">Any (フロントエンドサーバーアドレスとして定義可能、または XMPP ゲートウェイサービスを実行するフロントエンドプール IP アドレス)</span><span class="sxs-lookup"><span data-stu-id="0a3b0-193">Any (can be defined as Front End Server address, or Front End pool IP address running the XMPP Gateway service)</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-194">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-194">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-195">フロントエンドサーバーまたはフロントエンドプールで実行されている XMPP ゲートウェイサービスからの送信 XMPP トラフィック</span><span class="sxs-lookup"><span data-stu-id="0a3b0-195">Outbound XMPP traffic from XMPP Gateway service running on Front End Server or Front End pool</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a3b0-196">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="0a3b0-196">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-197">Any (ディレクター、ディレクタープールの IP アドレス、フロントエンドサーバー、フロントエンドプールの IP アドレスとして定義できます)</span><span class="sxs-lookup"><span data-stu-id="0a3b0-197">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-198">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-198">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-199">送信 SIP トラフィック (ディレクター、ディレクタープール IP アドレス、フロントエンドサーバーまたはフロントエンドプールの IP アドレス) からエッジサーバーの内部インターフェイスへ</span><span class="sxs-lookup"><span data-stu-id="0a3b0-199">Outbound SIP traffic (from Director, Director pool IP address, Front End Server or Front End pool IP address) to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a3b0-200">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="0a3b0-200">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-201">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-201">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-202">Any (ディレクター、ディレクタープールの IP アドレス、フロントエンドサーバー、フロントエンドプールの IP アドレスとして定義できます)</span><span class="sxs-lookup"><span data-stu-id="0a3b0-202">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-203">エッジサーバーの内部インターフェイスから受信 SIP トラフィック (ディレクター、ディレクタープール IP アドレス、フロントエンドサーバー、またはフロントエンドプールの IP アドレス)</span><span class="sxs-lookup"><span data-stu-id="0a3b0-203">Inbound SIP traffic (to Director, Director pool IP address, Front End Server or Front End pool IP address) from Edge Server internal interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a3b0-204">PSOM/MTLS/TCP/8057</span><span class="sxs-lookup"><span data-stu-id="0a3b0-204">PSOM/MTLS/TCP/8057</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-205">Any (フロントエンドサーバーの IP アドレス、またはフロントエンドプールの各フロントエンドサーバー IP アドレスとして定義できます)</span><span class="sxs-lookup"><span data-stu-id="0a3b0-205">Any (can be defined as Front End Server IP address, or each Front End Server IP address in a Front End pool)</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-206">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-206">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-207">フロントエンドサーバーからの Web 会議トラフィック、またはプール内の各フロントエンドサーバーから Edge Server の内部インターフェイスへの Web 会議トラフィック</span><span class="sxs-lookup"><span data-stu-id="0a3b0-207">Web conferencing traffic from Front End Server or each Front End Server if in a pool, to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a3b0-208">SIP/MTLS/TCP/5062</span><span class="sxs-lookup"><span data-stu-id="0a3b0-208">SIP/MTLS/TCP/5062</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-209">Any (フロントエンドサーバーの IP アドレス、またはこのエッジサーバーを使用している Survivable Branch Appliance または Survivable ブランチサーバー) として定義することができます。</span><span class="sxs-lookup"><span data-stu-id="0a3b0-209">Any (can be defined as Front End Server IP address, or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server)</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-210">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-210">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-211">このエッジサーバーを使用して、フロントエンドサーバーまたはフロントエンドプールの IP アドレスまたは Survivable Branch Appliance または Survivable ブランチサーバーからの、A/V ユーザー (A/V 認証サービス) の認証</span><span class="sxs-lookup"><span data-stu-id="0a3b0-211">Authentication of A/V users (A/V authentication service) from Front End Server or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a3b0-212">STUN/MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="0a3b0-212">STUN/MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-213">任意</span><span class="sxs-lookup"><span data-stu-id="0a3b0-213">Any</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-214">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-214">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-215">内部と外部のユーザー、Survivable Branch Appliance または Survivable ブランチサーバー間の A/V メディア転送の優先パス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-215">Preferred path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a3b0-216">STUN/MSTURN/443</span><span class="sxs-lookup"><span data-stu-id="0a3b0-216">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-217">任意</span><span class="sxs-lookup"><span data-stu-id="0a3b0-217">Any</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-218">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-218">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-219">内部と外部のユーザーとの間でのメディア転送のフォールバックパス Survivable Branch Appliance または Survivable Branch Server (UDP 通信が確立できない場合は、TCP を使ってファイル転送とデスクトップ共有を行う)</span><span class="sxs-lookup"><span data-stu-id="0a3b0-219">Fallback path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a3b0-220">HTTPS/TCP/4443</span><span class="sxs-lookup"><span data-stu-id="0a3b0-220">HTTPS/TCP/4443</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-221">Any (任意) (フロントエンドサーバーの IP アドレス、または全体管理ストアを保持するプールとして定義できます)</span><span class="sxs-lookup"><span data-stu-id="0a3b0-221">Any (can be defined as the Front End Server IP address, or pool that holds the Central Management store)</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-222">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-222">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-223">中央管理ストアからエッジサーバーへの変更のレプリケーション</span><span class="sxs-lookup"><span data-stu-id="0a3b0-223">Replication of changes from the Central Management store to the Edge Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a3b0-224">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="0a3b0-224">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-225">任意</span><span class="sxs-lookup"><span data-stu-id="0a3b0-225">Any</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-226">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-226">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-227">Lync Server 管理シェルと一元ログサービスコマンドレット、ClsController コマンドライン (ClsController.exe) または agent (ClsAgent.exe) コマンドとログ収集を使用した一元的なログサービスコントローラー</span><span class="sxs-lookup"><span data-stu-id="0a3b0-227">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a3b0-228">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="0a3b0-228">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-229">任意</span><span class="sxs-lookup"><span data-stu-id="0a3b0-229">Any</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-230">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-230">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-231">Lync Server 管理シェルと一元ログサービスコマンドレット、ClsController コマンドライン (ClsController.exe) または agent (ClsAgent.exe) コマンドとログ収集を使用した一元的なログサービスコントローラー</span><span class="sxs-lookup"><span data-stu-id="0a3b0-231">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a3b0-232">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="0a3b0-232">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-233">任意</span><span class="sxs-lookup"><span data-stu-id="0a3b0-233">Any</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-234">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-234">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-235">Lync Server 管理シェルと一元ログサービスコマンドレット、ClsController コマンドライン (ClsController.exe) または agent (ClsAgent.exe) コマンドとログ収集を使用した一元的なログサービスコントローラー</span><span class="sxs-lookup"><span data-stu-id="0a3b0-235">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-federation"></a><span data-ttu-id="0a3b0-236">フェデレーションのためのファイアウォールの概要</span><span class="sxs-lookup"><span data-stu-id="0a3b0-236">Firewall Summary for Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0a3b0-237">Role/Protocol/TCP または UDP/ポート</span><span class="sxs-lookup"><span data-stu-id="0a3b0-237">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="0a3b0-238">送信元 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-238">Source IP address</span></span></th>
<th><span data-ttu-id="0a3b0-239">宛先 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-239">Destination IP address</span></span></th>
<th><span data-ttu-id="0a3b0-240">メモ</span><span class="sxs-lookup"><span data-stu-id="0a3b0-240">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0a3b0-241">アクセス/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="0a3b0-241">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-242">アクセスエッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-242">Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-243">任意</span><span class="sxs-lookup"><span data-stu-id="0a3b0-243">Any</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-244">SIP を使用するフェデレーションおよびパブリック IM 接続の場合</span><span class="sxs-lookup"><span data-stu-id="0a3b0-244">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="0a3b0-245">ファイアウォールの概要–パブリックインスタントメッセージング接続</span><span class="sxs-lookup"><span data-stu-id="0a3b0-245">Firewall Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0a3b0-246">Role/Protocol/TCP または UDP/ポート</span><span class="sxs-lookup"><span data-stu-id="0a3b0-246">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="0a3b0-247">送信元 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-247">Source IP address</span></span></th>
<th><span data-ttu-id="0a3b0-248">宛先 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-248">Destination IP address</span></span></th>
<th><span data-ttu-id="0a3b0-249">メモ</span><span class="sxs-lookup"><span data-stu-id="0a3b0-249">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0a3b0-250">アクセス/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="0a3b0-250">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-251">パブリック IM 接続パートナー</span><span class="sxs-lookup"><span data-stu-id="0a3b0-251">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-252">エッジサーバーアクセスエッジサービス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-252">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-253">SIP を使用するフェデレーションおよびパブリック IM 接続の場合</span><span class="sxs-lookup"><span data-stu-id="0a3b0-253">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a3b0-254">アクセス/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="0a3b0-254">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-255">エッジサーバーアクセスエッジサービス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-255">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-256">パブリック IM 接続パートナー</span><span class="sxs-lookup"><span data-stu-id="0a3b0-256">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-257">SIP を使用するフェデレーションおよびパブリック IM 接続の場合</span><span class="sxs-lookup"><span data-stu-id="0a3b0-257">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a3b0-258">アクセス/SIP (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="0a3b0-258">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-259">クライアント</span><span class="sxs-lookup"><span data-stu-id="0a3b0-259">Clients</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-260">エッジサーバーアクセスエッジサービス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-260">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-261">外部ユーザーアクセスのクライアントツーサーバー SIP トラフィック</span><span class="sxs-lookup"><span data-stu-id="0a3b0-261">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a3b0-262">A/V/RTP/59,999</span><span class="sxs-lookup"><span data-stu-id="0a3b0-262">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-263">エッジサーバーの A/V Edge サービス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-263">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-264">Live Messenger クライアント</span><span class="sxs-lookup"><span data-stu-id="0a3b0-264">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-265">パブリック IM 接続が構成されている場合、Windows Live Messenger でのセッションに使用されます。</span><span class="sxs-lookup"><span data-stu-id="0a3b0-265">Used for A/V sessions with Windows Live Messenger if public IM connectivity is configured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a3b0-266">A/V/STUN、MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="0a3b0-266">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-267">エッジサーバーの A/V Edge サービス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-267">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-268">Live Messenger クライアント</span><span class="sxs-lookup"><span data-stu-id="0a3b0-268">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-269">Windows Live Messenger とのパブリック IM 接続に必要</span><span class="sxs-lookup"><span data-stu-id="0a3b0-269">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a3b0-270">A/V/STUN、MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="0a3b0-270">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-271">Live Messenger クライアント</span><span class="sxs-lookup"><span data-stu-id="0a3b0-271">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-272">エッジサーバーの A/V Edge サービス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-272">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-273">Windows Live Messenger とのパブリック IM 接続に必要</span><span class="sxs-lookup"><span data-stu-id="0a3b0-273">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="0a3b0-274">拡張メッセージングとプレゼンスプロトコルのファイアウォールの概要</span><span class="sxs-lookup"><span data-stu-id="0a3b0-274">Firewall Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0a3b0-275">Protocol/TCP または UDP/ポート</span><span class="sxs-lookup"><span data-stu-id="0a3b0-275">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="0a3b0-276">ソース (IP アドレス)</span><span class="sxs-lookup"><span data-stu-id="0a3b0-276">Source (IP address)</span></span></th>
<th><span data-ttu-id="0a3b0-277">宛先 (IP アドレス)</span><span class="sxs-lookup"><span data-stu-id="0a3b0-277">Destination (IP address)</span></span></th>
<th><span data-ttu-id="0a3b0-278">注釈</span><span class="sxs-lookup"><span data-stu-id="0a3b0-278">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0a3b0-279">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="0a3b0-279">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-280">任意</span><span class="sxs-lookup"><span data-stu-id="0a3b0-280">Any</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-281">エッジサーバーアクセスエッジサービスインターフェイスの IP アドレス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-281">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-282">XMPP 向けの標準的なサーバー間通信ポート。</span><span class="sxs-lookup"><span data-stu-id="0a3b0-282">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="0a3b0-283">フェデレーションされた XMPP パートナーからエッジサーバーの XMPP プロキシへの通信を許可します。</span><span class="sxs-lookup"><span data-stu-id="0a3b0-283">Allows communication to the Edge Server XMPP proxy from federated XMPP partners</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a3b0-284">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="0a3b0-284">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-285">エッジサーバーアクセスエッジサービスインターフェイスの IP アドレス</span><span class="sxs-lookup"><span data-stu-id="0a3b0-285">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-286">任意</span><span class="sxs-lookup"><span data-stu-id="0a3b0-286">Any</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-287">XMPP 向けの標準的なサーバー間通信ポート。</span><span class="sxs-lookup"><span data-stu-id="0a3b0-287">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="0a3b0-288">エッジサーバーの XMPP プロキシからフェデレーションされた XMPP パートナーへの通信を許可します。</span><span class="sxs-lookup"><span data-stu-id="0a3b0-288">Allows communication from the Edge Server XMPP proxy to federated XMPP partners</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a3b0-289">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="0a3b0-289">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-290">任意</span><span class="sxs-lookup"><span data-stu-id="0a3b0-290">Any</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-291">各内部エッジサーバーインターフェイス IP</span><span class="sxs-lookup"><span data-stu-id="0a3b0-291">Each internal Edge Server Interface IP</span></span></p></td>
<td><p><span data-ttu-id="0a3b0-292">フロントエンドサーバーまたはフロントエンドプールの XMPP ゲートウェイから Edge Server 内部 IP アドレスまたは各エッジプールメンバーの内部 IP アドレスへの内部の XMPP トラフィック</span><span class="sxs-lookup"><span data-stu-id="0a3b0-292">Internal XMPP traffic from the XMPP Gateway on the Front End Server or Front End pool to the Edge Server internal IP address or each Edge pool member’s internal IP address</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="0a3b0-293">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0a3b0-293">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

