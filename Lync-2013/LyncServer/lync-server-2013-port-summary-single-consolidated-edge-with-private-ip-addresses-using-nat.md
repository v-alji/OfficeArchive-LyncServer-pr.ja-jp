---
title: ポートの概要 - NAT を使用したプライベート IP アドレスを含む単一統合エッジ
description: ポート概要-NAT を使用したプライベート IP アドレスを持つ単一の統合エッジ。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Single consolidated edge with private IP addresses using NAT
ms:assetid: 3c1a389f-5f42-4719-a05b-e0b84aa3eb9e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425891(v=OCS.15)
ms:contentKeyID: 48183877
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a3fc182b9fbbd24d589feb7f73e3c0086fa23152
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424297"
---
# <a name="port-summary---single-consolidated-edge-with-private-ip-addresses-using-nat-in-lync-server-2013"></a><span data-ttu-id="03b43-103">ポートの概要 - Lync Server 2013 の NAT を使用したプライベート IP アドレスを含む単一統合エッジ</span><span class="sxs-lookup"><span data-stu-id="03b43-103">Port summary - Single consolidated edge with private IP addresses using NAT in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="03b43-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="03b43-104">

<span> </span></span></span>

<span data-ttu-id="03b43-105">_**最終更新日:** 2013-04-03_</span><span class="sxs-lookup"><span data-stu-id="03b43-105">_**Topic Last Modified:** 2013-04-03_</span></span>

<span data-ttu-id="03b43-106">このシナリオアーキテクチャで説明されている Lync Server 2013 のエッジサーバー機能は、Lync Server 2010 で実装されたものとよく似ています。</span><span class="sxs-lookup"><span data-stu-id="03b43-106">The Lync Server 2013, Edge Server functionality described in this scenario architecture is very similar to what was implemented in Lync Server 2010.</span></span> <span data-ttu-id="03b43-107">最も顕著な追加機能は、拡張メッセージングとプレゼンスプロトコル (XMPP) の TCP エントリのポート **5269** です。</span><span class="sxs-lookup"><span data-stu-id="03b43-107">The most noticeable addition is the port **5269 over TCP** entry for the extensible messaging and presence protocol (XMPP).</span></span> <span data-ttu-id="03b43-108">Lync Server 2013 では、必要に応じて、microsoft Edge サーバーまたはエッジプールに XMPP プロキシを展開し、フロントエンドサーバーまたはフロントエンドプールに XMPP ゲートウェイサーバーを配置します。</span><span class="sxs-lookup"><span data-stu-id="03b43-108">Lync Server 2013 optionally deploys an XMPP proxy on the Edge Server or Edge pool and the XMPP gateway server on the Front End Server or Front End pool.</span></span>

<span data-ttu-id="03b43-109">IPv4 に加えて、エッジサーバーは IPv6 をサポートするようになりました。</span><span class="sxs-lookup"><span data-stu-id="03b43-109">In addition to IPv4, the Edge Server now supports IPv6.</span></span> <span data-ttu-id="03b43-110">わかりやすくするために、シナリオでは IPv4 のみが使用されます。</span><span class="sxs-lookup"><span data-stu-id="03b43-110">For clarity, only IPv4 is used in the scenarios.</span></span>

<span data-ttu-id="03b43-111">**NAT を使用するプライベート IP アドレスが指定された単一の統合エッジサーバーのネットワーク境界線**</span><span class="sxs-lookup"><span data-stu-id="03b43-111">**Network Perimeter for a Single Consolidated Edge Server with Private IP Addressing Using NAT**</span></span>

<span data-ttu-id="03b43-112">![f8c144c5-e5fb-498a-823e-eb39f26b6847](images/Gg425891.f8c144c5-e5fb-498a-823e-eb39f26b6847(OCS.15).jpg "f8c144c5-e5fb-498a-823e-eb39f26b6847")</span><span class="sxs-lookup"><span data-stu-id="03b43-112">![f8c144c5-e5fb-498a-823e-eb39f26b6847](images/Gg425891.f8c144c5-e5fb-498a-823e-eb39f26b6847(OCS.15).jpg "f8c144c5-e5fb-498a-823e-eb39f26b6847")</span></span>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="03b43-113">ポートとプロトコルの詳細</span><span class="sxs-lookup"><span data-stu-id="03b43-113">Port and Protocol Details</span></span>

<span data-ttu-id="03b43-114">外部アクセスを提供する機能をサポートするために必要なポートのみを開くことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="03b43-114">We recommend that you open only the ports required to support the functionality for which you are providing external access.</span></span>

<span data-ttu-id="03b43-115">エッジサービスに対してリモートアクセスを使用するには、受信/送信エッジトラフィックの図に示すように、SIP トラフィックが双方向に流れるようにすることが必須です。</span><span class="sxs-lookup"><span data-stu-id="03b43-115">For remote access to work for any edge service, it is mandatory that SIP traffic is allowed to flow bi-directionally as shown in the Inbound/Outbound edge traffic figure.</span></span> <span data-ttu-id="03b43-116">別の方法として、アクセスエッジサービスとの間の SIP メッセージングは、インスタントメッセージング (IM)、プレゼンス、web 会議、音声/ビデオ (A/V)、およびフェデレーションに関連しています。</span><span class="sxs-lookup"><span data-stu-id="03b43-116">Stated another way, the SIP messaging to and from the Access Edge service is involved in instant messaging (IM), presence, web conferencing, audio/video (A/V), and federation.</span></span>

### <a name="firewall-summary-for-single-consolidated-edge-with-private-ip-addresses-using-nat-external-interface"></a><span data-ttu-id="03b43-117">NAT を使用してプライベート IP アドレスを持つ単一の統合エッジのファイアウォールの概要: 外部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="03b43-117">Firewall Summary for Single Consolidated Edge with Private IP Addresses using NAT: External Interface</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="03b43-118">Role/Protocol/TCP または UDP/ポート</span><span class="sxs-lookup"><span data-stu-id="03b43-118">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="03b43-119">送信元 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="03b43-119">Source IP address</span></span></th>
<th><span data-ttu-id="03b43-120">宛先 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="03b43-120">Destination IP address</span></span></th>
<th><span data-ttu-id="03b43-121">メモ</span><span class="sxs-lookup"><span data-stu-id="03b43-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03b43-122">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="03b43-122">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="03b43-123">任意</span><span class="sxs-lookup"><span data-stu-id="03b43-123">Any</span></span></p></td>
<td><p><span data-ttu-id="03b43-124">XMPP プロキシサービス (アクセスエッジサービスで IP アドレスを共有)</span><span class="sxs-lookup"><span data-stu-id="03b43-124">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="03b43-125">XMPP プロキシサービスは、定義された XMPP フェデレーションの XMPP 連絡先からのトラフィックを受け入れます。</span><span class="sxs-lookup"><span data-stu-id="03b43-125">XMPP Proxy service accepts traffic from XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03b43-126">Access/HTTP/TCP/80</span><span class="sxs-lookup"><span data-stu-id="03b43-126">Access/HTTP/TCP/80</span></span></p></td>
<td><p><span data-ttu-id="03b43-127">エッジサーバーアクセスエッジサービス</span><span class="sxs-lookup"><span data-stu-id="03b43-127">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="03b43-128">任意</span><span class="sxs-lookup"><span data-stu-id="03b43-128">Any</span></span></p></td>
<td><p><span data-ttu-id="03b43-129">証明書の失効/CRL の確認と取得</span><span class="sxs-lookup"><span data-stu-id="03b43-129">Certificate revocation/CRL check and retrieval</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03b43-130">Access/DNS/TCP/53</span><span class="sxs-lookup"><span data-stu-id="03b43-130">Access/DNS/TCP/53</span></span></p></td>
<td><p><span data-ttu-id="03b43-131">エッジサーバーアクセスエッジサービス</span><span class="sxs-lookup"><span data-stu-id="03b43-131">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="03b43-132">任意</span><span class="sxs-lookup"><span data-stu-id="03b43-132">Any</span></span></p></td>
<td><p><span data-ttu-id="03b43-133">TCP 経由の DNS クエリ</span><span class="sxs-lookup"><span data-stu-id="03b43-133">DNS query over TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03b43-134">Access/DNS/UDP/53</span><span class="sxs-lookup"><span data-stu-id="03b43-134">Access/DNS/UDP/53</span></span></p></td>
<td><p><span data-ttu-id="03b43-135">エッジサーバーアクセスエッジサービス</span><span class="sxs-lookup"><span data-stu-id="03b43-135">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="03b43-136">任意</span><span class="sxs-lookup"><span data-stu-id="03b43-136">Any</span></span></p></td>
<td><p><span data-ttu-id="03b43-137">UDP 経由の DNS クエリ</span><span class="sxs-lookup"><span data-stu-id="03b43-137">DNS query over UDP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03b43-138">アクセス/SIP (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="03b43-138">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="03b43-139">任意</span><span class="sxs-lookup"><span data-stu-id="03b43-139">Any</span></span></p></td>
<td><p><span data-ttu-id="03b43-140">エッジサーバーアクセスエッジサービス</span><span class="sxs-lookup"><span data-stu-id="03b43-140">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="03b43-141">外部ユーザーアクセスのクライアントツーサーバー SIP トラフィック</span><span class="sxs-lookup"><span data-stu-id="03b43-141">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03b43-142">アクセス/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="03b43-142">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="03b43-143">任意</span><span class="sxs-lookup"><span data-stu-id="03b43-143">Any</span></span></p></td>
<td><p><span data-ttu-id="03b43-144">エッジサーバーアクセスエッジサービス</span><span class="sxs-lookup"><span data-stu-id="03b43-144">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="03b43-145">SIP を使用するフェデレーションおよびパブリック IM 接続の場合</span><span class="sxs-lookup"><span data-stu-id="03b43-145">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03b43-146">アクセス/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="03b43-146">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="03b43-147">エッジサーバーアクセスエッジサービス</span><span class="sxs-lookup"><span data-stu-id="03b43-147">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="03b43-148">任意</span><span class="sxs-lookup"><span data-stu-id="03b43-148">Any</span></span></p></td>
<td><p><span data-ttu-id="03b43-149">SIP を使用するフェデレーションおよびパブリック IM 接続の場合</span><span class="sxs-lookup"><span data-stu-id="03b43-149">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03b43-150">Web 会議/PSOM (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="03b43-150">Web Conferencing/PSOM(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="03b43-151">任意</span><span class="sxs-lookup"><span data-stu-id="03b43-151">Any</span></span></p></td>
<td><p><span data-ttu-id="03b43-152">エッジサーバー Web 会議エッジサービス</span><span class="sxs-lookup"><span data-stu-id="03b43-152">Edge Server Web Conferencing Edge service</span></span></p></td>
<td><p><span data-ttu-id="03b43-153">Web 会議メディア</span><span class="sxs-lookup"><span data-stu-id="03b43-153">Web Conferencing media</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03b43-154">A/V/RTP/59,999</span><span class="sxs-lookup"><span data-stu-id="03b43-154">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="03b43-155">エッジサーバーの A/V Edge サービス</span><span class="sxs-lookup"><span data-stu-id="03b43-155">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="03b43-156">任意</span><span class="sxs-lookup"><span data-stu-id="03b43-156">Any</span></span></p></td>
<td><p><span data-ttu-id="03b43-157">Office Communications Server 2007、Office Communications Server 2007 R2、Lync Server 2010、および Lync Server 2013 を実行しているパートナーとのフェデレーションに必要。</span><span class="sxs-lookup"><span data-stu-id="03b43-157">Required for federating with partners running Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03b43-158">A/V/RTP/59,999</span><span class="sxs-lookup"><span data-stu-id="03b43-158">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="03b43-159">エッジサーバーの A/V Edge サービス</span><span class="sxs-lookup"><span data-stu-id="03b43-159">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="03b43-160">任意</span><span class="sxs-lookup"><span data-stu-id="03b43-160">Any</span></span></p></td>
<td><p><span data-ttu-id="03b43-161">Office Communications Server 2007 を実行しているパートナーとのフェデレーションの場合のみ必須です。</span><span class="sxs-lookup"><span data-stu-id="03b43-161">Required only for federation with partners running Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03b43-162">A/V/RTP/59,999</span><span class="sxs-lookup"><span data-stu-id="03b43-162">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="03b43-163">任意</span><span class="sxs-lookup"><span data-stu-id="03b43-163">Any</span></span></p></td>
<td><p><span data-ttu-id="03b43-164">エッジサーバーの A/V Edge サービス</span><span class="sxs-lookup"><span data-stu-id="03b43-164">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="03b43-165">Office Communications Server 2007 を実行しているパートナーとのフェデレーションにのみ必須</span><span class="sxs-lookup"><span data-stu-id="03b43-165">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03b43-166">A/V/RTP/59,999</span><span class="sxs-lookup"><span data-stu-id="03b43-166">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="03b43-167">任意</span><span class="sxs-lookup"><span data-stu-id="03b43-167">Any</span></span></p></td>
<td><p><span data-ttu-id="03b43-168">エッジサーバーの A/V Edge サービス</span><span class="sxs-lookup"><span data-stu-id="03b43-168">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="03b43-169">Office Communications Server 2007 を実行しているパートナーとのフェデレーションにのみ必須</span><span class="sxs-lookup"><span data-stu-id="03b43-169">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03b43-170">A/V/STUN、MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="03b43-170">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="03b43-171">エッジサーバーの A/V Edge サービス</span><span class="sxs-lookup"><span data-stu-id="03b43-171">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="03b43-172">任意</span><span class="sxs-lookup"><span data-stu-id="03b43-172">Any</span></span></p></td>
<td><p><span data-ttu-id="03b43-173">3478送信は、Lync Server が通信するエッジサーバーのバージョンと、エッジサーバーからエッジサーバーへのメディアトラフィックも確認するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="03b43-173">3478 outbound is used to determine the version of Edge Server that Lync Server is communicating with and also for media traffic from Edge Server-to-Edge Server.</span></span> <span data-ttu-id="03b43-174">Lync Server 2010、Windows Live Messenger、Office Communications Server 2007 R2 とのフェデレーション、および複数のエッジプールが会社内に展開されている場合に必要です。</span><span class="sxs-lookup"><span data-stu-id="03b43-174">Required for federation with Lync Server 2010, Windows Live Messenger, and Office Communications Server 2007 R2, and also if multiple Edge pools are deployed within a company.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03b43-175">A/V/STUN、MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="03b43-175">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="03b43-176">任意</span><span class="sxs-lookup"><span data-stu-id="03b43-176">Any</span></span></p></td>
<td><p><span data-ttu-id="03b43-177">エッジサーバーの A/V Edge サービス</span><span class="sxs-lookup"><span data-stu-id="03b43-177">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="03b43-178">UDP/3478 経由の候補のネゴシエーションをオフ/オンにする</span><span class="sxs-lookup"><span data-stu-id="03b43-178">STUN/TURN negotiation of candidates over UDP/3478</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03b43-179">A/V/STUN、MSTURN/443</span><span class="sxs-lookup"><span data-stu-id="03b43-179">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="03b43-180">任意</span><span class="sxs-lookup"><span data-stu-id="03b43-180">Any</span></span></p></td>
<td><p><span data-ttu-id="03b43-181">エッジサーバーの A/V Edge サービス</span><span class="sxs-lookup"><span data-stu-id="03b43-181">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="03b43-182">TCP/443 経由での候補のネゴシエーションをオフ/オンにする</span><span class="sxs-lookup"><span data-stu-id="03b43-182">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03b43-183">A/V/STUN、MSTURN/443</span><span class="sxs-lookup"><span data-stu-id="03b43-183">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="03b43-184">エッジサーバーの A/V Edge サービス</span><span class="sxs-lookup"><span data-stu-id="03b43-184">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="03b43-185">任意</span><span class="sxs-lookup"><span data-stu-id="03b43-185">Any</span></span></p></td>
<td><p><span data-ttu-id="03b43-186">TCP/443 経由での候補のネゴシエーションをオフ/オンにする</span><span class="sxs-lookup"><span data-stu-id="03b43-186">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-summary-for-single-consolidated-edge-with-private-ip-addresses-using-nat-internal-interface"></a><span data-ttu-id="03b43-187">NAT を使用してプライベート IP アドレスを持つ単一の統合エッジのファイアウォールの概要: 内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="03b43-187">Firewall Summary for Single Consolidated Edge with Private IP Addresses Using NAT: Internal Interface</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="03b43-188">Protocol/TCP または UDP/ポート</span><span class="sxs-lookup"><span data-stu-id="03b43-188">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="03b43-189">送信元 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="03b43-189">Source IP address</span></span></th>
<th><span data-ttu-id="03b43-190">宛先 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="03b43-190">Destination IP address</span></span></th>
<th><span data-ttu-id="03b43-191">注釈</span><span class="sxs-lookup"><span data-stu-id="03b43-191">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03b43-192">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="03b43-192">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="03b43-193">Any (標準エディションサーバー IP、Standard Edition server IP アドレス、または XMPP ゲートウェイサービスを実行しているプール IP アドレスとして定義できます)</span><span class="sxs-lookup"><span data-stu-id="03b43-193">Any (can be defined as Standard Edition server IP, Standard Edition server IP address, or pool IP address running the XMPP Gateway service)</span></span></p></td>
<td><p><span data-ttu-id="03b43-194">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="03b43-194">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="03b43-195">フロントエンドサーバーまたはフロントエンドプールで実行されている XMPP ゲートウェイサービスからの送信 XMPP トラフィック</span><span class="sxs-lookup"><span data-stu-id="03b43-195">Outbound XMPP traffic from XMPP Gateway service running on Front End Server or Front End pool</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03b43-196">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="03b43-196">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="03b43-197">Any (ディレクター、ディレクタープールの IP アドレス、フロントエンドサーバー、フロントエンドプールの IP アドレスとして定義できます)</span><span class="sxs-lookup"><span data-stu-id="03b43-197">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="03b43-198">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="03b43-198">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="03b43-199">送信 SIP トラフィック (ディレクター、ディレクタープール IP アドレス、フロントエンドサーバーまたはフロントエンドプールの IP アドレス) からエッジサーバーの内部インターフェイスへ</span><span class="sxs-lookup"><span data-stu-id="03b43-199">Outbound SIP traffic (from Director, Director pool IP address, Front End Server or Front End pool IP address) to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03b43-200">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="03b43-200">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="03b43-201">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="03b43-201">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="03b43-202">Any (ディレクター、ディレクタープールの IP アドレス、フロントエンドサーバー、フロントエンドプールの IP アドレスとして定義できます)</span><span class="sxs-lookup"><span data-stu-id="03b43-202">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="03b43-203">エッジサーバーの内部インターフェイスから受信 SIP トラフィック (ディレクター、ディレクタープール IP アドレス、フロントエンドサーバー、またはフロントエンドプールの IP アドレス)</span><span class="sxs-lookup"><span data-stu-id="03b43-203">Inbound SIP traffic (to Director, Director pool IP address, Front End Server or Front End pool IP address) from Edge Server internal interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03b43-204">PSOM/MTLS/TCP/8057</span><span class="sxs-lookup"><span data-stu-id="03b43-204">PSOM/MTLS/TCP/8057</span></span></p></td>
<td><p><span data-ttu-id="03b43-205">Any (フロントエンドサーバーの IP アドレス、またはフロントエンドプールの各フロントエンドサーバー IP アドレスとして定義できます)</span><span class="sxs-lookup"><span data-stu-id="03b43-205">Any (can be defined as Front End Server IP address, or each Front End Server IP address in a Front End pool)</span></span></p></td>
<td><p><span data-ttu-id="03b43-206">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="03b43-206">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="03b43-207">フロントエンドサーバーからの Web 会議トラフィック、またはプール内の各フロントエンドサーバーから Edge Server の内部インターフェイスへの Web 会議トラフィック</span><span class="sxs-lookup"><span data-stu-id="03b43-207">Web conferencing traffic from Front End Server or each Front End Server if in a pool, to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03b43-208">SIP/MTLS/TCP/5062</span><span class="sxs-lookup"><span data-stu-id="03b43-208">SIP/MTLS/TCP/5062</span></span></p></td>
<td><p><span data-ttu-id="03b43-209">Any (フロントエンドサーバーの IP アドレス、またはこのエッジサーバーを使用している Survivable Branch Appliance または Survivable ブランチサーバー) として定義することができます。</span><span class="sxs-lookup"><span data-stu-id="03b43-209">Any (can be defined as Front End Server IP address, or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server)</span></span></p></td>
<td><p><span data-ttu-id="03b43-210">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="03b43-210">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="03b43-211">このエッジサーバーを使用して、フロントエンドサーバーまたはフロントエンドプールの IP アドレスまたは Survivable Branch Appliance または Survivable ブランチサーバーからの、A/V ユーザー (A/V 認証サービス) の認証</span><span class="sxs-lookup"><span data-stu-id="03b43-211">Authentication of A/V users (A/V authentication service) from Front End Server or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03b43-212">STUN/MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="03b43-212">STUN/MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="03b43-213">任意</span><span class="sxs-lookup"><span data-stu-id="03b43-213">Any</span></span></p></td>
<td><p><span data-ttu-id="03b43-214">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="03b43-214">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="03b43-215">内部と外部のユーザー、Survivable Branch Appliance または Survivable ブランチサーバー間の A/V メディア転送の優先パス</span><span class="sxs-lookup"><span data-stu-id="03b43-215">Preferred path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03b43-216">STUN/MSTURN/443</span><span class="sxs-lookup"><span data-stu-id="03b43-216">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="03b43-217">任意</span><span class="sxs-lookup"><span data-stu-id="03b43-217">Any</span></span></p></td>
<td><p><span data-ttu-id="03b43-218">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="03b43-218">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="03b43-219">内部と外部のユーザーとの間でのメディア転送のフォールバックパス Survivable Branch Appliance または Survivable Branch Server (UDP 通信が確立できない場合は、TCP を使ってファイル転送とデスクトップ共有を行う)</span><span class="sxs-lookup"><span data-stu-id="03b43-219">Fallback path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03b43-220">HTTPS/TCP/4443</span><span class="sxs-lookup"><span data-stu-id="03b43-220">HTTPS/TCP/4443</span></span></p></td>
<td><p><span data-ttu-id="03b43-221">Any (任意) (フロントエンドサーバーの IP アドレス、または全体管理ストアを保持するプールとして定義できます)</span><span class="sxs-lookup"><span data-stu-id="03b43-221">Any (can be defined as the Front End Server IP address, or pool that holds the Central Management store)</span></span></p></td>
<td><p><span data-ttu-id="03b43-222">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="03b43-222">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="03b43-223">中央管理ストアからエッジサーバーへの変更のレプリケーション</span><span class="sxs-lookup"><span data-stu-id="03b43-223">Replication of changes from the Central Management store to the Edge Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03b43-224">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="03b43-224">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="03b43-225">任意</span><span class="sxs-lookup"><span data-stu-id="03b43-225">Any</span></span></p></td>
<td><p><span data-ttu-id="03b43-226">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="03b43-226">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="03b43-227">Lync Server 管理シェルと一元ログサービスコマンドレット、ClsController コマンドライン (ClsController.exe) または agent (ClsAgent.exe) コマンドとログ収集を使用した一元的なログサービスコントローラー</span><span class="sxs-lookup"><span data-stu-id="03b43-227">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03b43-228">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="03b43-228">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="03b43-229">任意</span><span class="sxs-lookup"><span data-stu-id="03b43-229">Any</span></span></p></td>
<td><p><span data-ttu-id="03b43-230">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="03b43-230">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="03b43-231">Lync Server 管理シェルと一元ログサービスコマンドレット、ClsController コマンドライン (ClsController.exe) または agent (ClsAgent.exe) コマンドとログ収集を使用した一元的なログサービスコントローラー</span><span class="sxs-lookup"><span data-stu-id="03b43-231">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03b43-232">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="03b43-232">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="03b43-233">任意</span><span class="sxs-lookup"><span data-stu-id="03b43-233">Any</span></span></p></td>
<td><p><span data-ttu-id="03b43-234">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="03b43-234">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="03b43-235">Lync Server 管理シェルと一元ログサービスコマンドレット、ClsController コマンドライン (ClsController.exe) または agent (ClsAgent.exe) コマンドとログ収集を使用した一元的なログサービスコントローラー</span><span class="sxs-lookup"><span data-stu-id="03b43-235">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-federation"></a><span data-ttu-id="03b43-236">フェデレーションのためのファイアウォールの概要</span><span class="sxs-lookup"><span data-stu-id="03b43-236">Firewall Summary for Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="03b43-237">Role/Protocol/TCP または UDP/ポート</span><span class="sxs-lookup"><span data-stu-id="03b43-237">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="03b43-238">送信元 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="03b43-238">Source IP address</span></span></th>
<th><span data-ttu-id="03b43-239">宛先 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="03b43-239">Destination IP address</span></span></th>
<th><span data-ttu-id="03b43-240">メモ</span><span class="sxs-lookup"><span data-stu-id="03b43-240">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03b43-241">アクセス/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="03b43-241">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="03b43-242">アクセスエッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="03b43-242">Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="03b43-243">任意</span><span class="sxs-lookup"><span data-stu-id="03b43-243">Any</span></span></p></td>
<td><p><span data-ttu-id="03b43-244">SIP を使用するフェデレーションおよびパブリック IM 接続の場合</span><span class="sxs-lookup"><span data-stu-id="03b43-244">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="03b43-245">ファイアウォールの概要–パブリックインスタントメッセージング接続</span><span class="sxs-lookup"><span data-stu-id="03b43-245">Firewall Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="03b43-246">Role/Protocol/TCP または UDP/ポート</span><span class="sxs-lookup"><span data-stu-id="03b43-246">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="03b43-247">送信元 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="03b43-247">Source IP address</span></span></th>
<th><span data-ttu-id="03b43-248">宛先 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="03b43-248">Destination IP address</span></span></th>
<th><span data-ttu-id="03b43-249">メモ</span><span class="sxs-lookup"><span data-stu-id="03b43-249">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03b43-250">アクセス/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="03b43-250">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="03b43-251">パブリック IM 接続パートナー</span><span class="sxs-lookup"><span data-stu-id="03b43-251">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="03b43-252">エッジサーバーアクセスエッジサービス</span><span class="sxs-lookup"><span data-stu-id="03b43-252">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="03b43-253">SIP を使用するフェデレーションおよびパブリック IM 接続の場合</span><span class="sxs-lookup"><span data-stu-id="03b43-253">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03b43-254">アクセス/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="03b43-254">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="03b43-255">エッジサーバーアクセスエッジサービス</span><span class="sxs-lookup"><span data-stu-id="03b43-255">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="03b43-256">パブリック IM 接続パートナー</span><span class="sxs-lookup"><span data-stu-id="03b43-256">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="03b43-257">SIP を使用するフェデレーションおよびパブリック IM 接続の場合</span><span class="sxs-lookup"><span data-stu-id="03b43-257">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03b43-258">アクセス/SIP (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="03b43-258">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="03b43-259">クライアント</span><span class="sxs-lookup"><span data-stu-id="03b43-259">Clients</span></span></p></td>
<td><p><span data-ttu-id="03b43-260">エッジサーバーアクセスエッジサービス</span><span class="sxs-lookup"><span data-stu-id="03b43-260">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="03b43-261">外部ユーザーアクセスのクライアントツーサーバー SIP トラフィック</span><span class="sxs-lookup"><span data-stu-id="03b43-261">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03b43-262">A/V/RTP/59,999</span><span class="sxs-lookup"><span data-stu-id="03b43-262">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="03b43-263">エッジサーバーの A/V Edge サービス</span><span class="sxs-lookup"><span data-stu-id="03b43-263">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="03b43-264">Live Messenger クライアント</span><span class="sxs-lookup"><span data-stu-id="03b43-264">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="03b43-265">パブリック IM 接続が構成されている場合、Windows Live Messenger でのセッションに使用されます。</span><span class="sxs-lookup"><span data-stu-id="03b43-265">Used for A/V sessions with Windows Live Messenger if public IM connectivity is configured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03b43-266">A/V/STUN、MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="03b43-266">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="03b43-267">エッジサーバーの A/V Edge サービス</span><span class="sxs-lookup"><span data-stu-id="03b43-267">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="03b43-268">Live Messenger クライアント</span><span class="sxs-lookup"><span data-stu-id="03b43-268">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="03b43-269">Windows Live Messenger とのパブリック IM 接続に必要</span><span class="sxs-lookup"><span data-stu-id="03b43-269">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03b43-270">A/V/STUN、MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="03b43-270">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="03b43-271">Live Messenger クライアント</span><span class="sxs-lookup"><span data-stu-id="03b43-271">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="03b43-272">エッジサーバーの A/V Edge サービス</span><span class="sxs-lookup"><span data-stu-id="03b43-272">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="03b43-273">Windows Live Messenger とのパブリック IM 接続に必要</span><span class="sxs-lookup"><span data-stu-id="03b43-273">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="03b43-274">拡張メッセージングとプレゼンスプロトコルのファイアウォールの概要</span><span class="sxs-lookup"><span data-stu-id="03b43-274">Firewall Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="03b43-275">Protocol/TCP または UDP/ポート</span><span class="sxs-lookup"><span data-stu-id="03b43-275">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="03b43-276">ソース (IP アドレス)</span><span class="sxs-lookup"><span data-stu-id="03b43-276">Source (IP address)</span></span></th>
<th><span data-ttu-id="03b43-277">宛先 (IP アドレス)</span><span class="sxs-lookup"><span data-stu-id="03b43-277">Destination (IP address)</span></span></th>
<th><span data-ttu-id="03b43-278">注釈</span><span class="sxs-lookup"><span data-stu-id="03b43-278">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03b43-279">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="03b43-279">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="03b43-280">任意</span><span class="sxs-lookup"><span data-stu-id="03b43-280">Any</span></span></p></td>
<td><p><span data-ttu-id="03b43-281">エッジサーバーアクセスエッジサービスインターフェイスの IP アドレス</span><span class="sxs-lookup"><span data-stu-id="03b43-281">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="03b43-282">XMPP 向けの標準的なサーバー間通信ポート。</span><span class="sxs-lookup"><span data-stu-id="03b43-282">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="03b43-283">フェデレーションされた XMPP パートナーからエッジサーバーの XMPP プロキシへの通信を許可します。</span><span class="sxs-lookup"><span data-stu-id="03b43-283">Allows communication to the Edge Server XMPP proxy from federated XMPP partners</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03b43-284">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="03b43-284">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="03b43-285">エッジサーバーアクセスエッジサービスインターフェイスの IP アドレス</span><span class="sxs-lookup"><span data-stu-id="03b43-285">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="03b43-286">任意</span><span class="sxs-lookup"><span data-stu-id="03b43-286">Any</span></span></p></td>
<td><p><span data-ttu-id="03b43-287">XMPP 向けの標準的なサーバー間通信ポート。</span><span class="sxs-lookup"><span data-stu-id="03b43-287">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="03b43-288">エッジサーバーの XMPP プロキシからフェデレーションされた XMPP パートナーへの通信を許可します。</span><span class="sxs-lookup"><span data-stu-id="03b43-288">Allows communication from the Edge Server XMPP proxy to federated XMPP partners</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03b43-289">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="03b43-289">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="03b43-290">任意</span><span class="sxs-lookup"><span data-stu-id="03b43-290">Any</span></span></p></td>
<td><p><span data-ttu-id="03b43-291">各内部エッジサーバーインターフェイス IP</span><span class="sxs-lookup"><span data-stu-id="03b43-291">Each internal Edge Server Interface IP</span></span></p></td>
<td><p><span data-ttu-id="03b43-292">フロントエンドサーバーまたはフロントエンドプールの XMPP ゲートウェイから Edge Server 内部 IP アドレスまたは各エッジプールメンバーの内部 IP アドレスへの内部の XMPP トラフィック</span><span class="sxs-lookup"><span data-stu-id="03b43-292">Internal XMPP traffic from the XMPP Gateway on the Front End Server or Front End pool to the Edge Server internal IP address or each Edge pool member’s internal IP address</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="03b43-293">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="03b43-293">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

