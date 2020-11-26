---
title: ポートの概要 - パブリック IP アドレスを使用する単一の統合エッジ
description: ポート概要-パブリック IP アドレスを持つ単一の統合エッジ。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Single consolidated edge with public IP addresses
ms:assetid: 28407acc-8b92-4f78-875c-fd6b4323b602
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204756(v=OCS.15)
ms:contentKeyID: 48183685
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 82ab2d89404fb174994d8e5b798f64bb68768326
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424263"
---
# <a name="port-summary---single-consolidated-edge-with-public-ip-addresses-in-lync-server-2013"></a><span data-ttu-id="20116-103">ポートの概要 - Lync Server 2013 でパブリック IP アドレスを使用する単一の統合エッジ</span><span class="sxs-lookup"><span data-stu-id="20116-103">Port summary - Single consolidated edge with public IP addresses in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="20116-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="20116-104">

<span> </span></span></span>

<span data-ttu-id="20116-105">_**最終更新日:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="20116-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="20116-106">このシナリオアーキテクチャで説明されている Lync Server 2013 のエッジサーバー機能は、Lync Server 2010 で実装されたものとよく似ています。</span><span class="sxs-lookup"><span data-stu-id="20116-106">The Lync Server 2013, Edge Server functionality described in this scenario architecture is very similar to what was implemented in Lync Server 2010.</span></span> <span data-ttu-id="20116-107">最も顕著な追加機能は、拡張メッセージングとプレゼンスプロトコル (XMPP) の TCP エントリのポート **5269** です。</span><span class="sxs-lookup"><span data-stu-id="20116-107">The most noticeable addition is the port **5269 over TCP** entry for the extensible messaging and presence protocol (XMPP).</span></span> <span data-ttu-id="20116-108">Lync Server 2013 では、必要に応じて、microsoft Edge サーバーまたはエッジプールに XMPP プロキシを展開し、フロントエンドサーバーまたはフロントエンドプールに XMPP ゲートウェイサーバーを配置します。</span><span class="sxs-lookup"><span data-stu-id="20116-108">Lync Server 2013 optionally deploys an XMPP proxy on the Edge Server or Edge pool and the XMPP gateway server on the Front End Server or Front End pool.</span></span> <span data-ttu-id="20116-109">リバースプロキシおよびフェデレーションの計画情報については、「 [lync server 2013 のリバースプロキシのシナリオ](lync-server-2013-scenarios-for-reverse-proxy.md) 」および「 [lync server 2013 セクションでの SIP、xmpp フェデレーション、パブリックインスタントメッセージングの計画](lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20116-109">Planning information for the reverse proxy and federation are found in [Scenarios for reverse proxy in Lync Server 2013](lync-server-2013-scenarios-for-reverse-proxy.md) and [Planning for SIP, XMPP federation, and public instant messaging in Lync Server 2013](lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md) sections, respectively.</span></span>

<span data-ttu-id="20116-110">IPv4 に加えて、エッジサーバーは IPv6 をサポートするようになりました。</span><span class="sxs-lookup"><span data-stu-id="20116-110">In addition to IPv4, the Edge Server now supports IPv6.</span></span> <span data-ttu-id="20116-111">わかりやすくするために、シナリオでは IPv4 のみが使用されます。</span><span class="sxs-lookup"><span data-stu-id="20116-111">For clarity, only IPv4 is used in the scenarios.</span></span>

<span data-ttu-id="20116-112">**パブリック IP アドレスを使った単一の統合エッジのエンタープライズ境界ネットワーク**</span><span class="sxs-lookup"><span data-stu-id="20116-112">**Enterprise perimeter network for single consolidated edge with public IP addressing**</span></span>

<span data-ttu-id="20116-113">![f8c144c5-e5fb-498a-823e-eb39f26b6847](images/Gg425891.f8c144c5-e5fb-498a-823e-eb39f26b6847(OCS.15).jpg "f8c144c5-e5fb-498a-823e-eb39f26b6847")</span><span class="sxs-lookup"><span data-stu-id="20116-113">![f8c144c5-e5fb-498a-823e-eb39f26b6847](images/Gg425891.f8c144c5-e5fb-498a-823e-eb39f26b6847(OCS.15).jpg "f8c144c5-e5fb-498a-823e-eb39f26b6847")</span></span>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="20116-114">ポートとプロトコルの詳細</span><span class="sxs-lookup"><span data-stu-id="20116-114">Port and Protocol Details</span></span>

<span data-ttu-id="20116-115">外部アクセスを提供する機能をサポートするために必要なポートのみを開くことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="20116-115">We recommend that you open only the ports required to support the functionality for which you are providing external access.</span></span>

<span data-ttu-id="20116-116">エッジサービスに対してリモートアクセスを使用するには、受信/送信エッジトラフィックの図に示すように、SIP トラフィックが双方向に流れるようにすることが必須です。</span><span class="sxs-lookup"><span data-stu-id="20116-116">For remote access to work for any edge service, it is mandatory that SIP traffic is allowed to flow bidirectionally as shown in the Inbound/Outbound edge traffic figure.</span></span> <span data-ttu-id="20116-117">別の方法として、アクセスエッジサービスとの間の SIP メッセージングは、インスタントメッセージング (IM)、プレゼンス、web 会議、音声/ビデオ (A/V)、およびフェデレーションに関連しています。</span><span class="sxs-lookup"><span data-stu-id="20116-117">Stated another way, the SIP messaging to and from the Access Edge service is involved in instant messaging (IM), presence, web conferencing, audio/video (A/V) and federation.</span></span>

### <a name="firewall-summary-for-single-consolidated-edge-with-public-ip-addresses-external-interface"></a><span data-ttu-id="20116-118">パブリック IP アドレスを持つ単一の統合エッジのファイアウォールの概要: 外部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="20116-118">Firewall Summary for Single Consolidated Edge with Public IP Addresses: External Interface</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="20116-119">Role/Protocol/TCP または UDP/ポート</span><span class="sxs-lookup"><span data-stu-id="20116-119">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="20116-120">送信元 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="20116-120">Source IP address</span></span></th>
<th><span data-ttu-id="20116-121">宛先 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="20116-121">Destination IP address</span></span></th>
<th><span data-ttu-id="20116-122">メモ</span><span class="sxs-lookup"><span data-stu-id="20116-122">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20116-123">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="20116-123">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="20116-124">任意</span><span class="sxs-lookup"><span data-stu-id="20116-124">Any</span></span></p></td>
<td><p><span data-ttu-id="20116-125">XMPP プロキシサービス (アクセスエッジサービスで IP アドレスを共有)</span><span class="sxs-lookup"><span data-stu-id="20116-125">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="20116-126">XMPP プロキシサービスは、定義された XMPP フェデレーションの XMPP 連絡先からのトラフィックを受け入れます。</span><span class="sxs-lookup"><span data-stu-id="20116-126">XMPP Proxy service accepts traffic from XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20116-127">Access/HTTP/TCP/80</span><span class="sxs-lookup"><span data-stu-id="20116-127">Access/HTTP/TCP/80</span></span></p></td>
<td><p><span data-ttu-id="20116-128">エッジサーバーアクセスエッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="20116-128">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="20116-129">任意</span><span class="sxs-lookup"><span data-stu-id="20116-129">Any</span></span></p></td>
<td><p><span data-ttu-id="20116-130">証明書の失効/CRL の確認と取得</span><span class="sxs-lookup"><span data-stu-id="20116-130">Certificate revocation/CRL check and retrieval</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20116-131">Access/DNS/TCP/53</span><span class="sxs-lookup"><span data-stu-id="20116-131">Access/DNS/TCP/53</span></span></p></td>
<td><p><span data-ttu-id="20116-132">エッジサーバーアクセスエッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="20116-132">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="20116-133">任意</span><span class="sxs-lookup"><span data-stu-id="20116-133">Any</span></span></p></td>
<td><p><span data-ttu-id="20116-134">TCP 経由の DNS クエリ</span><span class="sxs-lookup"><span data-stu-id="20116-134">DNS query over TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20116-135">Access/DNS/UDP/53</span><span class="sxs-lookup"><span data-stu-id="20116-135">Access/DNS/UDP/53</span></span></p></td>
<td><p><span data-ttu-id="20116-136">エッジサーバーアクセスエッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="20116-136">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="20116-137">任意</span><span class="sxs-lookup"><span data-stu-id="20116-137">Any</span></span></p></td>
<td><p><span data-ttu-id="20116-138">UDP 経由の DNS クエリ</span><span class="sxs-lookup"><span data-stu-id="20116-138">DNS query over UDP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20116-139">アクセス/SIP (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="20116-139">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="20116-140">任意</span><span class="sxs-lookup"><span data-stu-id="20116-140">Any</span></span></p></td>
<td><p><span data-ttu-id="20116-141">エッジサーバーアクセスエッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="20116-141">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="20116-142">外部ユーザーアクセスのクライアントツーサーバー SIP トラフィック</span><span class="sxs-lookup"><span data-stu-id="20116-142">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20116-143">アクセス/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="20116-143">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="20116-144">任意</span><span class="sxs-lookup"><span data-stu-id="20116-144">Any</span></span></p></td>
<td><p><span data-ttu-id="20116-145">エッジサーバーアクセスエッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="20116-145">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="20116-146">SIP を使用するフェデレーションおよびパブリック IM 接続の場合</span><span class="sxs-lookup"><span data-stu-id="20116-146">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20116-147">アクセス/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="20116-147">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="20116-148">エッジサーバーアクセスエッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="20116-148">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="20116-149">任意</span><span class="sxs-lookup"><span data-stu-id="20116-149">Any</span></span></p></td>
<td><p><span data-ttu-id="20116-150">SIP を使用するフェデレーションおよびパブリック IM 接続の場合</span><span class="sxs-lookup"><span data-stu-id="20116-150">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20116-151">Web 会議/PSOM (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="20116-151">Web Conferencing/PSOM(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="20116-152">任意</span><span class="sxs-lookup"><span data-stu-id="20116-152">Any</span></span></p></td>
<td><p><span data-ttu-id="20116-153">エッジサーバー Web 会議エッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="20116-153">Edge Server Web Conferencing Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="20116-154">Web 会議メディア</span><span class="sxs-lookup"><span data-stu-id="20116-154">Web Conferencing media</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20116-155">A/V/RTP/59,999</span><span class="sxs-lookup"><span data-stu-id="20116-155">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="20116-156">エッジサーバーアクセスエッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="20116-156">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="20116-157">任意</span><span class="sxs-lookup"><span data-stu-id="20116-157">Any</span></span></p></td>
<td><p><span data-ttu-id="20116-158">Office Communications Server 2007、Office Communications Server 2007 R2、Lync Server 2010、および Lync Server 2013 を実行しているパートナーとのフェデレーションに必要。</span><span class="sxs-lookup"><span data-stu-id="20116-158">Required for federating with partners running Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20116-159">A/V/RTP/59,999</span><span class="sxs-lookup"><span data-stu-id="20116-159">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="20116-160">エッジサーバーの A/V エッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="20116-160">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="20116-161">任意</span><span class="sxs-lookup"><span data-stu-id="20116-161">Any</span></span></p></td>
<td><p><span data-ttu-id="20116-162">Office Communications Server 2007 を実行しているパートナーとのフェデレーションにのみ必須</span><span class="sxs-lookup"><span data-stu-id="20116-162">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20116-163">A/V/RTP/59,999</span><span class="sxs-lookup"><span data-stu-id="20116-163">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="20116-164">任意</span><span class="sxs-lookup"><span data-stu-id="20116-164">Any</span></span></p></td>
<td><p><span data-ttu-id="20116-165">エッジサーバーの A/V エッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="20116-165">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="20116-166">Office Communications Server 2007 を実行しているパートナーとのフェデレーションの場合のみ必須です。</span><span class="sxs-lookup"><span data-stu-id="20116-166">Required only for federation with partners running Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20116-167">A/V/RTP/59,999</span><span class="sxs-lookup"><span data-stu-id="20116-167">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="20116-168">任意</span><span class="sxs-lookup"><span data-stu-id="20116-168">Any</span></span></p></td>
<td><p><span data-ttu-id="20116-169">エッジサーバーの A/V エッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="20116-169">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="20116-170">Office Communications Server 2007 を実行しているパートナーとのフェデレーションの場合のみ必須です。</span><span class="sxs-lookup"><span data-stu-id="20116-170">Required only for federation with partners running Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20116-171">A/V/STUN、MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="20116-171">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="20116-172">エッジサーバーの A/V エッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="20116-172">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="20116-173">任意</span><span class="sxs-lookup"><span data-stu-id="20116-173">Any</span></span></p></td>
<td><p><span data-ttu-id="20116-174">3478送信は、Lync Server が通信するエッジサーバーのバージョンと、エッジサーバーからエッジサーバーへのメディアトラフィックも確認するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="20116-174">3478 outbound is used to determine the version of Edge Server that Lync Server is communicating with and also for media traffic from Edge Server-to-Edge Server.</span></span> <span data-ttu-id="20116-175">Lync Server 2010、Windows Live Messenger、Office Communications Server 2007 R2 とのフェデレーション、および複数のエッジプールが会社内に展開されている場合に必要です。</span><span class="sxs-lookup"><span data-stu-id="20116-175">Required for federation with Lync Server 2010, Windows Live Messenger, and Office Communications Server 2007 R2, and also if multiple Edge pools are deployed within a company.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20116-176">A/V/STUN、MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="20116-176">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="20116-177">任意</span><span class="sxs-lookup"><span data-stu-id="20116-177">Any</span></span></p></td>
<td><p><span data-ttu-id="20116-178">エッジサーバーの A/V エッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="20116-178">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="20116-179">UDP/3478 経由の候補のネゴシエーションをオフ/オンにする</span><span class="sxs-lookup"><span data-stu-id="20116-179">STUN/TURN negotiation of candidates over UDP/3478</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20116-180">A/V/STUN、MSTURN/443</span><span class="sxs-lookup"><span data-stu-id="20116-180">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="20116-181">任意</span><span class="sxs-lookup"><span data-stu-id="20116-181">Any</span></span></p></td>
<td><p><span data-ttu-id="20116-182">エッジサーバーの A/V エッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="20116-182">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="20116-183">TCP/443 経由での候補のネゴシエーションをオフ/オンにする</span><span class="sxs-lookup"><span data-stu-id="20116-183">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20116-184">A/V/STUN、MSTURN/443</span><span class="sxs-lookup"><span data-stu-id="20116-184">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="20116-185">エッジサーバーの A/V エッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="20116-185">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="20116-186">任意</span><span class="sxs-lookup"><span data-stu-id="20116-186">Any</span></span></p></td>
<td><p><span data-ttu-id="20116-187">TCP/443 経由での候補のネゴシエーションをオフ/オンにする</span><span class="sxs-lookup"><span data-stu-id="20116-187">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-summary-for-single-consolidated-edge-with-public-ip-addresses-internal-interface"></a><span data-ttu-id="20116-188">パブリック IP アドレスを持つ単一の統合エッジのファイアウォールの概要: 内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="20116-188">Firewall Summary for Single Consolidated Edge with Public IP Addresses: Internal Interface</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="20116-189">Protocol/TCP または UDP/ポート</span><span class="sxs-lookup"><span data-stu-id="20116-189">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="20116-190">送信元 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="20116-190">Source IP address</span></span></th>
<th><span data-ttu-id="20116-191">宛先 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="20116-191">Destination IP address</span></span></th>
<th><span data-ttu-id="20116-192">注釈</span><span class="sxs-lookup"><span data-stu-id="20116-192">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20116-193">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="20116-193">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="20116-194">Any (標準エディションサーバー IP、Standard Edition server IP アドレス、または XMPP ゲートウェイサービスを実行しているプール IP アドレスとして定義できます)</span><span class="sxs-lookup"><span data-stu-id="20116-194">Any (can be defined as Standard Edition server IP, Standard Edition server IP address, or pool IP address running the XMPP Gateway service)</span></span></p></td>
<td><p><span data-ttu-id="20116-195">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="20116-195">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="20116-196">フロントエンドサーバーまたはフロントエンドプールで実行されている XMPP ゲートウェイサービスからの送信 XMPP トラフィック</span><span class="sxs-lookup"><span data-stu-id="20116-196">Outbound XMPP traffic from XMPP Gateway service running on Front End Server or Front End pool</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20116-197">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="20116-197">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="20116-198">Any (ディレクター、ディレクタープールの IP アドレス、フロントエンドサーバー、フロントエンドプールの IP アドレスとして定義できます)</span><span class="sxs-lookup"><span data-stu-id="20116-198">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="20116-199">エッジサーバー IP、または内部インターフェイスを保持するプール</span><span class="sxs-lookup"><span data-stu-id="20116-199">Edge Server IP, or pool that holds the internal interface</span></span></p></td>
<td><p><span data-ttu-id="20116-200">送信 SIP トラフィック (ディレクター、ディレクタープール IP アドレス、フロントエンドサーバーまたはフロントエンドプールの IP アドレス) からエッジサーバーの内部インターフェイスへ</span><span class="sxs-lookup"><span data-stu-id="20116-200">Outbound SIP traffic (from Director, Director pool IP address, Front End Server or Front End pool IP address) to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20116-201">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="20116-201">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="20116-202">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="20116-202">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="20116-203">Any (ディレクター、ディレクタープール IP アドレス、フロントエンドサーバー、フロントエンドプールのアドレスとして定義できます)</span><span class="sxs-lookup"><span data-stu-id="20116-203">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool address)</span></span></p></td>
<td><p><span data-ttu-id="20116-204">エッジサーバーの内部インターフェイスから受信 SIP トラフィック (ディレクター、ディレクタープール IP アドレス、フロントエンドサーバー、またはフロントエンドプールの IP アドレス)</span><span class="sxs-lookup"><span data-stu-id="20116-204">Inbound SIP traffic (to Director, Director pool IP address, Front End Server or Front End pool IP address) from Edge Server internal interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20116-205">PSOM/MTLS/TCP/8057</span><span class="sxs-lookup"><span data-stu-id="20116-205">PSOM/MTLS/TCP/8057</span></span></p></td>
<td><p><span data-ttu-id="20116-206">Any (フロントエンドサーバーの IP アドレス、またはフロントエンドプールの各フロントエンドサーバー IP アドレスとして定義できます)</span><span class="sxs-lookup"><span data-stu-id="20116-206">Any (can be defined as Front End Server IP address, or each Front End Server IP address in a Front End pool)</span></span></p></td>
<td><p><span data-ttu-id="20116-207">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="20116-207">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="20116-208">フロントエンドサーバーからの Web 会議トラフィック、またはプール内の各フロントエンドサーバーから Edge Server の内部インターフェイスへの Web 会議トラフィック</span><span class="sxs-lookup"><span data-stu-id="20116-208">Web conferencing traffic from Front End Server or each Front End Server if in a pool, to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20116-209">SIP/MTLS/TCP/5062</span><span class="sxs-lookup"><span data-stu-id="20116-209">SIP/MTLS/TCP/5062</span></span></p></td>
<td><p><span data-ttu-id="20116-210">Any (フロントエンドサーバーの IP アドレス、またはこのエッジサーバーを使用している Survivable Branch Appliance または Survivable ブランチサーバー) として定義することができます。</span><span class="sxs-lookup"><span data-stu-id="20116-210">Any (can be defined as Front End Server IP address, or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server)</span></span></p></td>
<td><p><span data-ttu-id="20116-211">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="20116-211">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="20116-212">このエッジサーバーを使用して、フロントエンドサーバーまたはフロントエンドプールの IP アドレスまたは Survivable Branch Appliance または Survivable ブランチサーバーからの、A/V ユーザー (A/V 認証サービス) の認証</span><span class="sxs-lookup"><span data-stu-id="20116-212">Authentication of A/V users (A/V authentication service) from Front End Server or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20116-213">STUN/MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="20116-213">STUN/MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="20116-214">任意</span><span class="sxs-lookup"><span data-stu-id="20116-214">Any</span></span></p></td>
<td><p><span data-ttu-id="20116-215">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="20116-215">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="20116-216">内部と外部のユーザー、Survivable Branch Appliance または Survivable ブランチサーバー間の A/V メディア転送の優先パス</span><span class="sxs-lookup"><span data-stu-id="20116-216">Preferred path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20116-217">STUN/MSTURN/443</span><span class="sxs-lookup"><span data-stu-id="20116-217">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="20116-218">任意</span><span class="sxs-lookup"><span data-stu-id="20116-218">Any</span></span></p></td>
<td><p><span data-ttu-id="20116-219">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="20116-219">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="20116-220">内部と外部のユーザーとの間でのメディア転送のフォールバックパス Survivable Branch Appliance または Survivable Branch Server (UDP 通信が確立できない場合は、TCP を使ってファイル転送とデスクトップ共有を行う)</span><span class="sxs-lookup"><span data-stu-id="20116-220">Fallback path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20116-221">HTTPS/TCP/4443</span><span class="sxs-lookup"><span data-stu-id="20116-221">HTTPS/TCP/4443</span></span></p></td>
<td><p><span data-ttu-id="20116-222">Any (任意) (フロントエンドサーバーの IP アドレス、または全体管理ストアを保持するプールとして定義できます)</span><span class="sxs-lookup"><span data-stu-id="20116-222">Any (can be defined as the Front End Server IP address, or pool that holds the Central Management store)</span></span></p></td>
<td><p><span data-ttu-id="20116-223">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="20116-223">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="20116-224">中央管理ストアからエッジサーバーへの変更のレプリケーション</span><span class="sxs-lookup"><span data-stu-id="20116-224">Replication of changes from the Central Management store to the Edge Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20116-225">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="20116-225">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="20116-226">任意</span><span class="sxs-lookup"><span data-stu-id="20116-226">Any</span></span></p></td>
<td><p><span data-ttu-id="20116-227">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="20116-227">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="20116-228">Lync Server 管理シェルと一元ログサービスコマンドレット、ClsController コマンドライン (ClsController.exe) または agent (ClsAgent.exe) コマンドとログ収集を使用した一元的なログサービスコントローラー</span><span class="sxs-lookup"><span data-stu-id="20116-228">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20116-229">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="20116-229">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="20116-230">任意</span><span class="sxs-lookup"><span data-stu-id="20116-230">Any</span></span></p></td>
<td><p><span data-ttu-id="20116-231">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="20116-231">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="20116-232">Lync Server 管理シェルと一元ログサービスコマンドレット、ClsController コマンドライン (ClsController.exe) または agent (ClsAgent.exe) コマンドとログ収集を使用した一元的なログサービスコントローラー</span><span class="sxs-lookup"><span data-stu-id="20116-232">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20116-233">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="20116-233">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="20116-234">任意</span><span class="sxs-lookup"><span data-stu-id="20116-234">Any</span></span></p></td>
<td><p><span data-ttu-id="20116-235">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="20116-235">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="20116-236">Lync Server 管理シェルと一元ログサービスコマンドレット、ClsController コマンドライン (ClsController.exe) または agent (ClsAgent.exe) コマンドとログ収集を使用した一元的なログサービスコントローラー</span><span class="sxs-lookup"><span data-stu-id="20116-236">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-federation"></a><span data-ttu-id="20116-237">フェデレーションのためのファイアウォールの概要</span><span class="sxs-lookup"><span data-stu-id="20116-237">Firewall Summary for Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="20116-238">Role/Protocol/TCP または UDP/ポート</span><span class="sxs-lookup"><span data-stu-id="20116-238">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="20116-239">送信元 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="20116-239">Source IP address</span></span></th>
<th><span data-ttu-id="20116-240">宛先 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="20116-240">Destination IP address</span></span></th>
<th><span data-ttu-id="20116-241">メモ</span><span class="sxs-lookup"><span data-stu-id="20116-241">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20116-242">アクセス/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="20116-242">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="20116-243">アクセスエッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="20116-243">Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="20116-244">任意</span><span class="sxs-lookup"><span data-stu-id="20116-244">Any</span></span></p></td>
<td><p><span data-ttu-id="20116-245">SIP を使用するフェデレーションおよびパブリック IM 接続の場合</span><span class="sxs-lookup"><span data-stu-id="20116-245">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="20116-246">ファイアウォールの概要–パブリックインスタントメッセージング接続</span><span class="sxs-lookup"><span data-stu-id="20116-246">Firewall Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="20116-247">Role/Protocol/TCP または UDP/ポート</span><span class="sxs-lookup"><span data-stu-id="20116-247">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="20116-248">送信元 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="20116-248">Source IP address</span></span></th>
<th><span data-ttu-id="20116-249">宛先 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="20116-249">Destination IP address</span></span></th>
<th><span data-ttu-id="20116-250">メモ</span><span class="sxs-lookup"><span data-stu-id="20116-250">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20116-251">アクセス/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="20116-251">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="20116-252">パブリック IM 接続パートナー</span><span class="sxs-lookup"><span data-stu-id="20116-252">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="20116-253">エッジサーバーアクセスエッジサービス</span><span class="sxs-lookup"><span data-stu-id="20116-253">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="20116-254">SIP を使用するフェデレーションおよびパブリック IM 接続の場合</span><span class="sxs-lookup"><span data-stu-id="20116-254">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20116-255">アクセス/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="20116-255">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="20116-256">エッジサーバーアクセスエッジサービス</span><span class="sxs-lookup"><span data-stu-id="20116-256">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="20116-257">パブリック IM 接続パートナー</span><span class="sxs-lookup"><span data-stu-id="20116-257">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="20116-258">SIP を使用するフェデレーションおよびパブリック IM 接続の場合</span><span class="sxs-lookup"><span data-stu-id="20116-258">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20116-259">アクセス/SIP (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="20116-259">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="20116-260">クライアント</span><span class="sxs-lookup"><span data-stu-id="20116-260">Clients</span></span></p></td>
<td><p><span data-ttu-id="20116-261">エッジサーバーアクセスエッジサービス</span><span class="sxs-lookup"><span data-stu-id="20116-261">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="20116-262">外部ユーザーアクセスのクライアントツーサーバー SIP トラフィック</span><span class="sxs-lookup"><span data-stu-id="20116-262">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20116-263">A/V/RTP/59,999</span><span class="sxs-lookup"><span data-stu-id="20116-263">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="20116-264">エッジサーバーの A/V Edge サービス</span><span class="sxs-lookup"><span data-stu-id="20116-264">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="20116-265">Live Messenger クライアント</span><span class="sxs-lookup"><span data-stu-id="20116-265">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="20116-266">パブリック IM 接続が構成されている場合、Windows Live Messenger でのセッションに使用されます。</span><span class="sxs-lookup"><span data-stu-id="20116-266">Used for A/V sessions with Windows Live Messenger if public IM connectivity is configured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20116-267">A/V/STUN、MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="20116-267">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="20116-268">エッジサーバーの A/V Edge サービス</span><span class="sxs-lookup"><span data-stu-id="20116-268">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="20116-269">Live Messenger クライアント</span><span class="sxs-lookup"><span data-stu-id="20116-269">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="20116-270">Windows Live Messenger とのパブリック IM 接続に必要</span><span class="sxs-lookup"><span data-stu-id="20116-270">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20116-271">A/V/STUN、MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="20116-271">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="20116-272">Live Messenger クライアント</span><span class="sxs-lookup"><span data-stu-id="20116-272">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="20116-273">エッジサーバーの A/V Edge サービス</span><span class="sxs-lookup"><span data-stu-id="20116-273">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="20116-274">Windows Live Messenger とのパブリック IM 接続に必要</span><span class="sxs-lookup"><span data-stu-id="20116-274">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="20116-275">拡張メッセージングとプレゼンスプロトコルのファイアウォールの概要</span><span class="sxs-lookup"><span data-stu-id="20116-275">Firewall Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="20116-276">Protocol/TCP または UDP/ポート</span><span class="sxs-lookup"><span data-stu-id="20116-276">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="20116-277">ソース (IP アドレス)</span><span class="sxs-lookup"><span data-stu-id="20116-277">Source (IP address)</span></span></th>
<th><span data-ttu-id="20116-278">宛先 (IP アドレス)</span><span class="sxs-lookup"><span data-stu-id="20116-278">Destination (IP address)</span></span></th>
<th><span data-ttu-id="20116-279">注釈</span><span class="sxs-lookup"><span data-stu-id="20116-279">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20116-280">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="20116-280">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="20116-281">任意</span><span class="sxs-lookup"><span data-stu-id="20116-281">Any</span></span></p></td>
<td><p><span data-ttu-id="20116-282">エッジサーバーアクセスエッジサービスインターフェイスの IP アドレス</span><span class="sxs-lookup"><span data-stu-id="20116-282">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="20116-283">XMPP 向けの標準的なサーバー間通信ポート。</span><span class="sxs-lookup"><span data-stu-id="20116-283">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="20116-284">フェデレーションされた XMPP パートナーからエッジサーバーの XMPP プロキシへの通信を許可します。</span><span class="sxs-lookup"><span data-stu-id="20116-284">Allows communication to the Edge Server XMPP proxy from federated XMPP partners</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20116-285">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="20116-285">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="20116-286">エッジサーバーアクセスエッジサービスインターフェイスの IP アドレス</span><span class="sxs-lookup"><span data-stu-id="20116-286">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="20116-287">任意</span><span class="sxs-lookup"><span data-stu-id="20116-287">Any</span></span></p></td>
<td><p><span data-ttu-id="20116-288">XMPP 向けの標準的なサーバー間通信ポート。</span><span class="sxs-lookup"><span data-stu-id="20116-288">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="20116-289">エッジサーバーの XMPP プロキシからフェデレーションされた XMPP パートナーへの通信を許可します。</span><span class="sxs-lookup"><span data-stu-id="20116-289">Allows communication from the Edge Server XMPP proxy to federated XMPP partners</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20116-290">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="20116-290">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="20116-291">任意</span><span class="sxs-lookup"><span data-stu-id="20116-291">Any</span></span></p></td>
<td><p><span data-ttu-id="20116-292">各内部エッジサーバーインターフェイス IP</span><span class="sxs-lookup"><span data-stu-id="20116-292">Each internal Edge Server Interface IP</span></span></p></td>
<td><p><span data-ttu-id="20116-293">フロントエンドサーバーまたはフロントエンドプールの XMPP ゲートウェイから Edge Server 内部 IP アドレスまたは各エッジプールメンバーの内部 IP アドレスへの内部の XMPP トラフィック</span><span class="sxs-lookup"><span data-stu-id="20116-293">Internal XMPP traffic from the XMPP Gateway on the Front End Server or Front End pool to the Edge Server internal IP address or each Edge pool member’s internal IP address</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="20116-294">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="20116-294">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

