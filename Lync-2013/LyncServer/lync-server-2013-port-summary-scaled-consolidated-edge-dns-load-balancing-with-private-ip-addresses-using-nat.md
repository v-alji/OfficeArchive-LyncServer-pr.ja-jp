---
title: 'Lync Server 2013: ポートの概要 - 拡張統合エッジ、NAT によるプライベート IP アドレスを使用した DNS 負荷分散'
description: 'Lync Server 2013: ポートの概要-拡張された統合エッジ、NAT を使用したプライベート IP アドレスを使った DNS の負荷分散。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Scaled consolidated edge, DNS load balancing with private IP addresses using NAT
ms:assetid: a296c2af-54d4-4b4f-9795-9191baf688cb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412756(v=OCS.15)
ms:contentKeyID: 48184955
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e0402b6682e86e5edf263fca78dfbe0f8fa070b4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424291"
---
# <a name="port-summary---scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat-in-lync-server-2013"></a><span data-ttu-id="783c1-103">ポートの概要 - Lync Server 2013 における拡張統合エッジ、NAT によるプライベート IP アドレスを使用した DNS 負荷分散</span><span class="sxs-lookup"><span data-stu-id="783c1-103">Port summary - Scaled consolidated edge, DNS load balancing with private IP addresses using NAT in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="783c1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="783c1-104">

<span> </span></span></span>

<span data-ttu-id="783c1-105">_**最終更新日:** 2012-12-04_</span><span class="sxs-lookup"><span data-stu-id="783c1-105">_**Topic Last Modified:** 2012-12-04_</span></span>

<span data-ttu-id="783c1-106">このシナリオアーキテクチャで説明されている Lync Server 2013 のエッジサーバー機能は、Lync Server 2010 で実装されたものとよく似ています。</span><span class="sxs-lookup"><span data-stu-id="783c1-106">The Lync Server 2013, Edge Server functionality described in this scenario architecture is very similar to what was implemented in Lync Server 2010.</span></span> <span data-ttu-id="783c1-107">最も顕著な追加機能は、拡張メッセージングとプレゼンスプロトコル (XMPP) の TCP エントリのポート **5269** です。</span><span class="sxs-lookup"><span data-stu-id="783c1-107">The most noticeable addition is the port **5269 over TCP** entry for the extensible messaging and presence protocol (XMPP).</span></span> <span data-ttu-id="783c1-108">Lync Server 2013 では、必要に応じて、microsoft Edge サーバーまたはエッジプールに XMPP プロキシを展開し、フロントエンドサーバーまたはフロントエンドプールに XMPP ゲートウェイサーバーを配置します。</span><span class="sxs-lookup"><span data-stu-id="783c1-108">Lync Server 2013 optionally deploys an XMPP proxy on the Edge Server or Edge pool and the XMPP gateway server on the Front End Server or Front End pool.</span></span>

<span data-ttu-id="783c1-109">IPv4 に加えて、エッジサーバーは IPv6 をサポートするようになりました。</span><span class="sxs-lookup"><span data-stu-id="783c1-109">In addition to IPv4, the Edge Server now supports IPv6.</span></span> <span data-ttu-id="783c1-110">わかりやすくするために、シナリオでは IPv4 のみが使用されます。</span><span class="sxs-lookup"><span data-stu-id="783c1-110">For clarity, only IPv4 is used in the scenarios.</span></span>

<span data-ttu-id="783c1-111">**NAT を使用する統合エッジ用のエンタープライズ境界ネットワークとプライベート IP アドレス**</span><span class="sxs-lookup"><span data-stu-id="783c1-111">**Enterprise perimeter network for scaled consolidated edge with private IP addresses using NAT**</span></span>

<span data-ttu-id="783c1-112">![96f5a8f5-16d2-464d-b86e-7c7ecfc89ead](images/JJ205394.96f5a8f5-16d2-464d-b86e-7c7ecfc89ead(OCS.15).jpg "96f5a8f5-16d2-464d-b86e-7c7ecfc89ead")</span><span class="sxs-lookup"><span data-stu-id="783c1-112">![96f5a8f5-16d2-464d-b86e-7c7ecfc89ead](images/JJ205394.96f5a8f5-16d2-464d-b86e-7c7ecfc89ead(OCS.15).jpg "96f5a8f5-16d2-464d-b86e-7c7ecfc89ead")</span></span>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="783c1-113">ポートとプロトコルの詳細</span><span class="sxs-lookup"><span data-stu-id="783c1-113">Port and Protocol Details</span></span>

<span data-ttu-id="783c1-114">外部アクセスを提供する機能をサポートするために必要なポートのみを開くことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="783c1-114">It is recommended that you open only the ports required to support the functionality for which you are providing external access.</span></span>

<span data-ttu-id="783c1-115">エッジサービスに対してリモートアクセスを使用するには、受信/送信エッジトラフィックの図に示すように、SIP トラフィックが双方向に流れるようにすることが必須です。</span><span class="sxs-lookup"><span data-stu-id="783c1-115">For remote access to work for any edge service, it is mandatory that SIP traffic is allowed to flow bi-directionally as shown in the Inbound/Outbound edge traffic figure.</span></span> <span data-ttu-id="783c1-116">別の方法として、アクセスエッジサービスとの間の SIP メッセージングは、インスタントメッセージング (IM)、プレゼンス、web 会議、音声/ビデオ (A/V)、およびフェデレーションに関連しています。</span><span class="sxs-lookup"><span data-stu-id="783c1-116">Stated another way, the SIP messaging to and from the Access Edge service is involved in instant messaging (IM), presence, web conferencing, audio/video (A/V) and federation.</span></span>

### <a name="firewall-summary-for-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat-external-interface--node-1-and-node-2-example"></a><span data-ttu-id="783c1-117">拡張統合エッジの場合のファイアウォールの概要、NAT を使用したプライベート IP アドレスを使った DNS 負荷分散: ノード1とノード 2 (例)</span><span class="sxs-lookup"><span data-stu-id="783c1-117">Firewall Summary for Scaled Consolidated Edge, DNS Load Balancing with Private IP Addresses Using NAT: External Interface – Node 1 and Node 2 (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="783c1-118">Role/Protocol/TCP または UDP/ポート</span><span class="sxs-lookup"><span data-stu-id="783c1-118">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="783c1-119">送信元 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="783c1-119">Source IP address</span></span></th>
<th><span data-ttu-id="783c1-120">宛先 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="783c1-120">Destination IP address</span></span></th>
<th><span data-ttu-id="783c1-121">メモ</span><span class="sxs-lookup"><span data-stu-id="783c1-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="783c1-122">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="783c1-122">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="783c1-123">任意</span><span class="sxs-lookup"><span data-stu-id="783c1-123">Any</span></span></p></td>
<td><p><span data-ttu-id="783c1-124">XMPP プロキシサービス (アクセスエッジサービスで IP アドレスを共有)</span><span class="sxs-lookup"><span data-stu-id="783c1-124">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="783c1-125">XMPP プロキシサービスは、定義された XMPP フェデレーションの XMPP 連絡先からのトラフィックを受け入れます。</span><span class="sxs-lookup"><span data-stu-id="783c1-125">XMPP Proxy service accepts traffic from XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="783c1-126">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="783c1-126">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="783c1-127">XMPP プロキシサービス (アクセスエッジサービスで IP アドレスを共有)</span><span class="sxs-lookup"><span data-stu-id="783c1-127">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="783c1-128">任意</span><span class="sxs-lookup"><span data-stu-id="783c1-128">Any</span></span></p></td>
<td><p><span data-ttu-id="783c1-129">XMPP プロキシサービスは、定義された XMPP フェデレーションの XMPP の連絡先にトラフィックを送信します。</span><span class="sxs-lookup"><span data-stu-id="783c1-129">XMPP Proxy service sends traffic to XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="783c1-130">Access/HTTP/TCP/80</span><span class="sxs-lookup"><span data-stu-id="783c1-130">Access/HTTP/TCP/80</span></span></p></td>
<td><p><span data-ttu-id="783c1-131">エッジサーバーアクセスエッジサービス</span><span class="sxs-lookup"><span data-stu-id="783c1-131">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="783c1-132">任意</span><span class="sxs-lookup"><span data-stu-id="783c1-132">Any</span></span></p></td>
<td><p><span data-ttu-id="783c1-133">証明書の失効/CRL の確認と取得</span><span class="sxs-lookup"><span data-stu-id="783c1-133">Certificate revocation/CRL check and retrieval</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="783c1-134">Access/DNS/TCP/53</span><span class="sxs-lookup"><span data-stu-id="783c1-134">Access/DNS/TCP/53</span></span></p></td>
<td><p><span data-ttu-id="783c1-135">エッジサーバーアクセスエッジサービス</span><span class="sxs-lookup"><span data-stu-id="783c1-135">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="783c1-136">任意</span><span class="sxs-lookup"><span data-stu-id="783c1-136">Any</span></span></p></td>
<td><p><span data-ttu-id="783c1-137">TCP 経由の DNS クエリ</span><span class="sxs-lookup"><span data-stu-id="783c1-137">DNS query over TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="783c1-138">Access/DNS/UDP/53</span><span class="sxs-lookup"><span data-stu-id="783c1-138">Access/DNS/UDP/53</span></span></p></td>
<td><p><span data-ttu-id="783c1-139">エッジサーバーアクセスエッジサービス</span><span class="sxs-lookup"><span data-stu-id="783c1-139">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="783c1-140">任意</span><span class="sxs-lookup"><span data-stu-id="783c1-140">Any</span></span></p></td>
<td><p><span data-ttu-id="783c1-141">UDP 経由の DNS クエリ</span><span class="sxs-lookup"><span data-stu-id="783c1-141">DNS query over UDP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="783c1-142">アクセス/SIP (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="783c1-142">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="783c1-143">任意</span><span class="sxs-lookup"><span data-stu-id="783c1-143">Any</span></span></p></td>
<td><p><span data-ttu-id="783c1-144">エッジサーバーアクセスエッジサービス</span><span class="sxs-lookup"><span data-stu-id="783c1-144">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="783c1-145">外部ユーザーアクセスのクライアントツーサーバー SIP トラフィック</span><span class="sxs-lookup"><span data-stu-id="783c1-145">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="783c1-146">アクセス/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="783c1-146">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="783c1-147">任意</span><span class="sxs-lookup"><span data-stu-id="783c1-147">Any</span></span></p></td>
<td><p><span data-ttu-id="783c1-148">エッジサーバーアクセスエッジサービス</span><span class="sxs-lookup"><span data-stu-id="783c1-148">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="783c1-149">SIP を使用するフェデレーションおよびパブリック IM 接続の場合</span><span class="sxs-lookup"><span data-stu-id="783c1-149">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="783c1-150">アクセス/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="783c1-150">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="783c1-151">エッジサーバーアクセスエッジサービス</span><span class="sxs-lookup"><span data-stu-id="783c1-151">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="783c1-152">任意</span><span class="sxs-lookup"><span data-stu-id="783c1-152">Any</span></span></p></td>
<td><p><span data-ttu-id="783c1-153">SIP を使用するフェデレーションおよびパブリック IM 接続の場合</span><span class="sxs-lookup"><span data-stu-id="783c1-153">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="783c1-154">Web 会議/PSOM (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="783c1-154">Web Conferencing/PSOM(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="783c1-155">任意</span><span class="sxs-lookup"><span data-stu-id="783c1-155">Any</span></span></p></td>
<td><p><span data-ttu-id="783c1-156">エッジサーバー Web 会議エッジサービス</span><span class="sxs-lookup"><span data-stu-id="783c1-156">Edge Server Web Conferencing Edge service</span></span></p></td>
<td><p><span data-ttu-id="783c1-157">Web 会議メディア</span><span class="sxs-lookup"><span data-stu-id="783c1-157">Web Conferencing media</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="783c1-158">A/V/RTP/59,999</span><span class="sxs-lookup"><span data-stu-id="783c1-158">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="783c1-159">エッジサーバーの A/V Edge サービス</span><span class="sxs-lookup"><span data-stu-id="783c1-159">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="783c1-160">任意</span><span class="sxs-lookup"><span data-stu-id="783c1-160">Any</span></span></p></td>
<td><p><span data-ttu-id="783c1-161">Office Communications Server 2007、Office Communications Server 2007 R2、Lync Server 2010、および Lync Server 2013 を実行しているパートナーとのフェデレーションに必要。</span><span class="sxs-lookup"><span data-stu-id="783c1-161">Required for federating with partners running Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="783c1-162">A/V/RTP/59,999</span><span class="sxs-lookup"><span data-stu-id="783c1-162">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="783c1-163">エッジサーバーの A/V Edge サービス</span><span class="sxs-lookup"><span data-stu-id="783c1-163">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="783c1-164">任意</span><span class="sxs-lookup"><span data-stu-id="783c1-164">Any</span></span></p></td>
<td><p><span data-ttu-id="783c1-165">Office Communications Server 2007 を実行しているパートナーとのフェデレーションの場合のみ必須です。</span><span class="sxs-lookup"><span data-stu-id="783c1-165">Required only for federation with partners running Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="783c1-166">A/V/RTP/59,999</span><span class="sxs-lookup"><span data-stu-id="783c1-166">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="783c1-167">任意</span><span class="sxs-lookup"><span data-stu-id="783c1-167">Any</span></span></p></td>
<td><p><span data-ttu-id="783c1-168">エッジサーバーの A/V Edge サービス</span><span class="sxs-lookup"><span data-stu-id="783c1-168">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="783c1-169">Office Communications Server 2007 を実行しているパートナーとのフェデレーションにのみ必須</span><span class="sxs-lookup"><span data-stu-id="783c1-169">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="783c1-170">A/V/RTP/59,999</span><span class="sxs-lookup"><span data-stu-id="783c1-170">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="783c1-171">任意</span><span class="sxs-lookup"><span data-stu-id="783c1-171">Any</span></span></p></td>
<td><p><span data-ttu-id="783c1-172">エッジサーバーの A/V Edge サービス</span><span class="sxs-lookup"><span data-stu-id="783c1-172">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="783c1-173">Office Communications Server 2007 を実行しているパートナーとのフェデレーションにのみ必須</span><span class="sxs-lookup"><span data-stu-id="783c1-173">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="783c1-174">A/V/STUN、MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="783c1-174">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="783c1-175">エッジサーバーの A/V Edge サービス</span><span class="sxs-lookup"><span data-stu-id="783c1-175">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="783c1-176">任意</span><span class="sxs-lookup"><span data-stu-id="783c1-176">Any</span></span></p></td>
<td><p><span data-ttu-id="783c1-177">3478送信は、Lync Server が通信するエッジサーバーのバージョンと、エッジサーバーからエッジサーバーへのメディアトラフィックも確認するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="783c1-177">3478 outbound is used to determine the version of Edge Server that Lync Server is communicating with and also for media traffic from Edge Server-to-Edge Server.</span></span> <span data-ttu-id="783c1-178">Lync Server 2010、Windows Live Messenger、Office Communications Server 2007 R2 とのフェデレーション、および複数のエッジプールが会社内に展開されている場合に必要です。</span><span class="sxs-lookup"><span data-stu-id="783c1-178">Required for federation with Lync Server 2010, Windows Live Messenger, and Office Communications Server 2007 R2, and also if multiple Edge pools are deployed within a company.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="783c1-179">A/V/STUN、MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="783c1-179">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="783c1-180">任意</span><span class="sxs-lookup"><span data-stu-id="783c1-180">Any</span></span></p></td>
<td><p><span data-ttu-id="783c1-181">エッジサーバーの A/V Edge サービス</span><span class="sxs-lookup"><span data-stu-id="783c1-181">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="783c1-182">UDP/3478 経由の候補のネゴシエーションをオフ/オンにする</span><span class="sxs-lookup"><span data-stu-id="783c1-182">STUN/TURN negotiation of candidates over UDP/3478</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="783c1-183">A/V/STUN、MSTURN/443</span><span class="sxs-lookup"><span data-stu-id="783c1-183">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="783c1-184">任意</span><span class="sxs-lookup"><span data-stu-id="783c1-184">Any</span></span></p></td>
<td><p><span data-ttu-id="783c1-185">エッジサーバーの A/V Edge サービス</span><span class="sxs-lookup"><span data-stu-id="783c1-185">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="783c1-186">TCP/443 経由での候補のネゴシエーションをオフ/オンにする</span><span class="sxs-lookup"><span data-stu-id="783c1-186">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="783c1-187">A/V/STUN、MSTURN/443</span><span class="sxs-lookup"><span data-stu-id="783c1-187">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="783c1-188">エッジサーバーの A/V Edge サービス</span><span class="sxs-lookup"><span data-stu-id="783c1-188">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="783c1-189">任意</span><span class="sxs-lookup"><span data-stu-id="783c1-189">Any</span></span></p></td>
<td><p><span data-ttu-id="783c1-190">TCP/443 経由での候補のネゴシエーションをオフ/オンにする</span><span class="sxs-lookup"><span data-stu-id="783c1-190">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-summary-for-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat-internal-interface--node-1-and-node-2-example"></a><span data-ttu-id="783c1-191">拡大縮小された統合エッジのファイアウォールの概要: 内部インターフェイス–ノード1とノード 2 (例) のプライベート IP アドレスを使った DNS 負荷分散</span><span class="sxs-lookup"><span data-stu-id="783c1-191">Firewall Summary for Scaled Consolidated Edge, DNS Load Balancing with Private IP Addresses Using NAT: Internal Interface – Node 1 and Node 2 (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="783c1-192">Protocol/TCP または UDP/ポート</span><span class="sxs-lookup"><span data-stu-id="783c1-192">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="783c1-193">送信元 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="783c1-193">Source IP address</span></span></th>
<th><span data-ttu-id="783c1-194">宛先 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="783c1-194">Destination IP address</span></span></th>
<th><span data-ttu-id="783c1-195">注釈</span><span class="sxs-lookup"><span data-stu-id="783c1-195">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="783c1-196">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="783c1-196">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="783c1-197">Any (フロントエンドサーバーアドレスとして定義可能、または XMPP ゲートウェイサービスを実行するフロントエンドプール IP アドレス)</span><span class="sxs-lookup"><span data-stu-id="783c1-197">Any (can be defined as Front End Server address, or Front End pool IP address running the XMPP Gateway service)</span></span></p></td>
<td><p><span data-ttu-id="783c1-198">エッジサーバーの内部インターフェイス IP アドレス</span><span class="sxs-lookup"><span data-stu-id="783c1-198">Edge Server internal interface IP address</span></span></p></td>
<td><p><span data-ttu-id="783c1-199">フロントエンドサーバーまたはフロントエンドプールで実行されている XMPP ゲートウェイサービスからの送信 XMPP トラフィック</span><span class="sxs-lookup"><span data-stu-id="783c1-199">Outbound XMPP traffic from XMPP Gateway service running on Front End Server or Front End pool</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="783c1-200">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="783c1-200">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="783c1-201">Any (ディレクター、ディレクタープールの IP アドレス、フロントエンドサーバー、フロントエンドプールの IP アドレスとして定義できます)</span><span class="sxs-lookup"><span data-stu-id="783c1-201">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="783c1-202">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="783c1-202">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="783c1-203">送信 SIP トラフィック (ディレクター、ディレクタープール IP アドレス、フロントエンドサーバーまたはフロントエンドプールの IP アドレス) からエッジサーバーの内部インターフェイスへ</span><span class="sxs-lookup"><span data-stu-id="783c1-203">Outbound SIP traffic (from Director, Director pool IP address, Front End Server or Front End pool IP address) to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="783c1-204">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="783c1-204">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="783c1-205">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="783c1-205">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="783c1-206">Any (ディレクター、ディレクタープールの IP アドレス、フロントエンドサーバー、フロントエンドプールの IP アドレスとして定義できます)</span><span class="sxs-lookup"><span data-stu-id="783c1-206">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="783c1-207">エッジサーバーの内部インターフェイスから受信 SIP トラフィック (ディレクター、ディレクタープール IP アドレス、フロントエンドサーバー、またはフロントエンドプールの IP アドレス)</span><span class="sxs-lookup"><span data-stu-id="783c1-207">Inbound SIP traffic (to Director, Director pool IP address, Front End Server or Front End pool IP address) from Edge Server internal interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="783c1-208">PSOM/MTLS/TCP/8057</span><span class="sxs-lookup"><span data-stu-id="783c1-208">PSOM/MTLS/TCP/8057</span></span></p></td>
<td><p><span data-ttu-id="783c1-209">Any (フロントエンドサーバーの IP アドレス、またはフロントエンドプールの各フロントエンドサーバー IP アドレスとして定義できます)</span><span class="sxs-lookup"><span data-stu-id="783c1-209">Any (can be defined as Front End Server IP address, or each Front End Server IP address in a Front End pool)</span></span></p></td>
<td><p><span data-ttu-id="783c1-210">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="783c1-210">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="783c1-211">フロントエンドサーバーからの Web 会議トラフィック、またはプール内の各フロントエンドサーバーから Edge Server の内部インターフェイスへの Web 会議トラフィック</span><span class="sxs-lookup"><span data-stu-id="783c1-211">Web conferencing traffic from Front End Server or each Front End Server if in a pool, to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="783c1-212">SIP/MTLS/TCP/5062</span><span class="sxs-lookup"><span data-stu-id="783c1-212">SIP/MTLS/TCP/5062</span></span></p></td>
<td><p><span data-ttu-id="783c1-213">Any (フロントエンドサーバーの IP アドレス、またはこのエッジサーバーを使用している Survivable Branch Appliance または Survivable ブランチサーバー) として定義することができます。</span><span class="sxs-lookup"><span data-stu-id="783c1-213">Any (can be defined as Front End Server IP address, or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server)</span></span></p></td>
<td><p><span data-ttu-id="783c1-214">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="783c1-214">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="783c1-215">このエッジサーバーを使用して、フロントエンドサーバーまたはフロントエンドプールの IP アドレスまたは Survivable Branch Appliance または Survivable ブランチサーバーからの、A/V ユーザー (A/V 認証サービス) の認証</span><span class="sxs-lookup"><span data-stu-id="783c1-215">Authentication of A/V users (A/V authentication service) from Front End Server or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="783c1-216">STUN/MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="783c1-216">STUN/MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="783c1-217">任意</span><span class="sxs-lookup"><span data-stu-id="783c1-217">Any</span></span></p></td>
<td><p><span data-ttu-id="783c1-218">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="783c1-218">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="783c1-219">内部と外部のユーザー、Survivable Branch Appliance または Survivable ブランチサーバー間の A/V メディア転送の優先パス</span><span class="sxs-lookup"><span data-stu-id="783c1-219">Preferred path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="783c1-220">STUN/MSTURN/443</span><span class="sxs-lookup"><span data-stu-id="783c1-220">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="783c1-221">任意</span><span class="sxs-lookup"><span data-stu-id="783c1-221">Any</span></span></p></td>
<td><p><span data-ttu-id="783c1-222">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="783c1-222">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="783c1-223">内部と外部のユーザーとの間でのメディア転送のフォールバックパス Survivable Branch Appliance または Survivable Branch Server (UDP 通信が確立できない場合は、TCP を使ってファイル転送とデスクトップ共有を行う)</span><span class="sxs-lookup"><span data-stu-id="783c1-223">Fallback path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="783c1-224">HTTPS/TCP/4443</span><span class="sxs-lookup"><span data-stu-id="783c1-224">HTTPS/TCP/4443</span></span></p></td>
<td><p><span data-ttu-id="783c1-225">Any (任意) (フロントエンドサーバーの IP アドレス、または全体管理ストアを保持するプールとして定義できます)</span><span class="sxs-lookup"><span data-stu-id="783c1-225">Any (can be defined as the Front End Server IP address, or pool that holds the Central Management store)</span></span></p></td>
<td><p><span data-ttu-id="783c1-226">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="783c1-226">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="783c1-227">中央管理ストアからエッジサーバーへの変更のレプリケーション</span><span class="sxs-lookup"><span data-stu-id="783c1-227">Replication of changes from the Central Management store to the Edge Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="783c1-228">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="783c1-228">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="783c1-229">任意</span><span class="sxs-lookup"><span data-stu-id="783c1-229">Any</span></span></p></td>
<td><p><span data-ttu-id="783c1-230">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="783c1-230">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="783c1-231">Lync Server 管理シェルと一元ログサービスコマンドレット、ClsController コマンドライン (ClsController.exe) または agent (ClsAgent.exe) コマンドとログ収集を使用した一元的なログサービスコントローラー</span><span class="sxs-lookup"><span data-stu-id="783c1-231">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="783c1-232">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="783c1-232">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="783c1-233">任意</span><span class="sxs-lookup"><span data-stu-id="783c1-233">Any</span></span></p></td>
<td><p><span data-ttu-id="783c1-234">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="783c1-234">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="783c1-235">Lync Server 管理シェルと一元ログサービスコマンドレット、ClsController コマンドライン (ClsController.exe) または agent (ClsAgent.exe) コマンドとログ収集を使用した一元的なログサービスコントローラー</span><span class="sxs-lookup"><span data-stu-id="783c1-235">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="783c1-236">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="783c1-236">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="783c1-237">任意</span><span class="sxs-lookup"><span data-stu-id="783c1-237">Any</span></span></p></td>
<td><p><span data-ttu-id="783c1-238">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="783c1-238">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="783c1-239">Lync Server 管理シェルと一元ログサービスコマンドレット、ClsController コマンドライン (ClsController.exe) または agent (ClsAgent.exe) コマンドとログ収集を使用した一元的なログサービスコントローラー</span><span class="sxs-lookup"><span data-stu-id="783c1-239">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-federation"></a><span data-ttu-id="783c1-240">フェデレーションのためのファイアウォールの概要</span><span class="sxs-lookup"><span data-stu-id="783c1-240">Firewall Summary for Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="783c1-241">Role/Protocol/TCP または UDP/ポート</span><span class="sxs-lookup"><span data-stu-id="783c1-241">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="783c1-242">送信元 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="783c1-242">Source IP address</span></span></th>
<th><span data-ttu-id="783c1-243">宛先 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="783c1-243">Destination IP address</span></span></th>
<th><span data-ttu-id="783c1-244">メモ</span><span class="sxs-lookup"><span data-stu-id="783c1-244">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="783c1-245">アクセス/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="783c1-245">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="783c1-246">アクセスエッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="783c1-246">Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="783c1-247">任意</span><span class="sxs-lookup"><span data-stu-id="783c1-247">Any</span></span></p></td>
<td><p><span data-ttu-id="783c1-248">SIP を使用するフェデレーションおよびパブリック IM 接続の場合</span><span class="sxs-lookup"><span data-stu-id="783c1-248">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="783c1-249">ファイアウォールの概要–パブリックインスタントメッセージング接続</span><span class="sxs-lookup"><span data-stu-id="783c1-249">Firewall Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="783c1-250">Role/Protocol/TCP または UDP/ポート</span><span class="sxs-lookup"><span data-stu-id="783c1-250">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="783c1-251">送信元 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="783c1-251">Source IP address</span></span></th>
<th><span data-ttu-id="783c1-252">宛先 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="783c1-252">Destination IP address</span></span></th>
<th><span data-ttu-id="783c1-253">メモ</span><span class="sxs-lookup"><span data-stu-id="783c1-253">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="783c1-254">アクセス/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="783c1-254">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="783c1-255">パブリック IM 接続パートナー</span><span class="sxs-lookup"><span data-stu-id="783c1-255">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="783c1-256">エッジサーバーアクセスエッジサービス</span><span class="sxs-lookup"><span data-stu-id="783c1-256">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="783c1-257">SIP を使用するフェデレーションおよびパブリック IM 接続の場合</span><span class="sxs-lookup"><span data-stu-id="783c1-257">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="783c1-258">アクセス/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="783c1-258">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="783c1-259">エッジサーバーアクセスエッジサービス</span><span class="sxs-lookup"><span data-stu-id="783c1-259">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="783c1-260">パブリック IM 接続パートナー</span><span class="sxs-lookup"><span data-stu-id="783c1-260">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="783c1-261">SIP を使用するフェデレーションおよびパブリック IM 接続の場合</span><span class="sxs-lookup"><span data-stu-id="783c1-261">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="783c1-262">アクセス/SIP (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="783c1-262">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="783c1-263">クライアント</span><span class="sxs-lookup"><span data-stu-id="783c1-263">Clients</span></span></p></td>
<td><p><span data-ttu-id="783c1-264">エッジサーバーアクセスエッジサービス</span><span class="sxs-lookup"><span data-stu-id="783c1-264">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="783c1-265">外部ユーザーアクセスのクライアントツーサーバー SIP トラフィック</span><span class="sxs-lookup"><span data-stu-id="783c1-265">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="783c1-266">A/V/RTP/59,999</span><span class="sxs-lookup"><span data-stu-id="783c1-266">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="783c1-267">エッジサーバーの A/V Edge サービス</span><span class="sxs-lookup"><span data-stu-id="783c1-267">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="783c1-268">Live Messenger クライアント</span><span class="sxs-lookup"><span data-stu-id="783c1-268">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="783c1-269">パブリック IM 接続が構成されている場合、Windows Live Messenger でのセッションに使用されます。</span><span class="sxs-lookup"><span data-stu-id="783c1-269">Used for A/V sessions with Windows Live Messenger if public IM connectivity is configured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="783c1-270">A/V/STUN、MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="783c1-270">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="783c1-271">エッジサーバーの A/V Edge サービス</span><span class="sxs-lookup"><span data-stu-id="783c1-271">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="783c1-272">Live Messenger クライアント</span><span class="sxs-lookup"><span data-stu-id="783c1-272">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="783c1-273">Windows Live Messenger とのパブリック IM 接続に必要</span><span class="sxs-lookup"><span data-stu-id="783c1-273">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="783c1-274">A/V/STUN、MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="783c1-274">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="783c1-275">Live Messenger クライアント</span><span class="sxs-lookup"><span data-stu-id="783c1-275">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="783c1-276">エッジサーバーの A/V Edge サービス</span><span class="sxs-lookup"><span data-stu-id="783c1-276">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="783c1-277">Windows Live Messenger とのパブリック IM 接続に必要</span><span class="sxs-lookup"><span data-stu-id="783c1-277">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="783c1-278">拡張メッセージングとプレゼンスプロトコルのファイアウォールの概要</span><span class="sxs-lookup"><span data-stu-id="783c1-278">Firewall Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="783c1-279">Protocol/TCP または UDP/ポート</span><span class="sxs-lookup"><span data-stu-id="783c1-279">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="783c1-280">ソース (IP アドレス)</span><span class="sxs-lookup"><span data-stu-id="783c1-280">Source (IP address)</span></span></th>
<th><span data-ttu-id="783c1-281">宛先 (IP アドレス)</span><span class="sxs-lookup"><span data-stu-id="783c1-281">Destination (IP address)</span></span></th>
<th><span data-ttu-id="783c1-282">注釈</span><span class="sxs-lookup"><span data-stu-id="783c1-282">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="783c1-283">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="783c1-283">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="783c1-284">任意</span><span class="sxs-lookup"><span data-stu-id="783c1-284">Any</span></span></p></td>
<td><p><span data-ttu-id="783c1-285">エッジサーバーアクセスエッジサービスインターフェイスの IP アドレス</span><span class="sxs-lookup"><span data-stu-id="783c1-285">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="783c1-286">XMPP 向けの標準的なサーバー間通信ポート。</span><span class="sxs-lookup"><span data-stu-id="783c1-286">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="783c1-287">フェデレーションされた XMPP パートナーからエッジサーバーの XMPP プロキシへの通信を許可します。</span><span class="sxs-lookup"><span data-stu-id="783c1-287">Allows communication to the Edge Server XMPP proxy from federated XMPP partners</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="783c1-288">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="783c1-288">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="783c1-289">エッジサーバーアクセスエッジサービスインターフェイスの IP アドレス</span><span class="sxs-lookup"><span data-stu-id="783c1-289">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="783c1-290">任意</span><span class="sxs-lookup"><span data-stu-id="783c1-290">Any</span></span></p></td>
<td><p><span data-ttu-id="783c1-291">XMPP 向けの標準的なサーバー間通信ポート。</span><span class="sxs-lookup"><span data-stu-id="783c1-291">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="783c1-292">エッジサーバーの XMPP プロキシからフェデレーションされた XMPP パートナーへの通信を許可します。</span><span class="sxs-lookup"><span data-stu-id="783c1-292">Allows communication from the Edge Server XMPP proxy to federated XMPP partners</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="783c1-293">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="783c1-293">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="783c1-294">任意</span><span class="sxs-lookup"><span data-stu-id="783c1-294">Any</span></span></p></td>
<td><p><span data-ttu-id="783c1-295">各内部エッジサーバーインターフェイス IP</span><span class="sxs-lookup"><span data-stu-id="783c1-295">Each internal Edge Server interface IP</span></span></p></td>
<td><p><span data-ttu-id="783c1-296">フロントエンドサーバーまたはフロントエンドプールの XMPP ゲートウェイから Edge Server 内部 IP アドレスまたは各エッジプールメンバーの内部 IP アドレスへの内部の XMPP トラフィック</span><span class="sxs-lookup"><span data-stu-id="783c1-296">Internal XMPP traffic from the XMPP Gateway on the Front End Server or Front End pool to the Edge Server internal IP address or each Edge pool member’s internal IP address</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="783c1-297">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="783c1-297">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

