---
title: ポートの概要 - 拡張統合エッジ (ロード バランサー機器を使用)
description: ポートの概要-ハードウェアロードバランサーを使った統合エッジスケール。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Scaled consolidated edge with hardware load balancers
ms:assetid: 91213b1e-f875-464b-83e8-fe3a351595a4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398739(v=OCS.15)
ms:contentKeyID: 48184841
ms.date: 04/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1a03acb3644d83669bcf0065ebb20c526ef5fa32
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424320"
---
# <a name="port-summary---scaled-consolidated-edge-with-hardware-load-balancers-in-lync-server-2013"></a><span data-ttu-id="e3390-103">ポートの概要 - Lync Server 2013 の拡張統合エッジ (ロード バランサー機器を使用)</span><span class="sxs-lookup"><span data-stu-id="e3390-103">Port summary - Scaled consolidated edge with hardware load balancers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e3390-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e3390-104">

<span> </span></span></span>

<span data-ttu-id="e3390-105">_**最終更新日:** 2015-04-27_</span><span class="sxs-lookup"><span data-stu-id="e3390-105">_**Topic Last Modified:** 2015-04-27_</span></span>

<span data-ttu-id="e3390-106">このシナリオアーキテクチャで説明されている Lync Server 2013 のエッジサーバー機能は、Lync Server 2010 で実装されたものとよく似ています。</span><span class="sxs-lookup"><span data-stu-id="e3390-106">The Lync Server 2013, Edge Server functionality described in this scenario architecture is very similar to what was implemented in Lync Server 2010.</span></span> <span data-ttu-id="e3390-107">最も顕著な追加機能は、拡張メッセージングとプレゼンスプロトコル (XMPP) の TCP エントリのポート **5269** です。</span><span class="sxs-lookup"><span data-stu-id="e3390-107">The most noticeable addition is the port **5269 over TCP** entry for the extensible messaging and presence protocol (XMPP).</span></span> <span data-ttu-id="e3390-108">Lync Server 2013 では、必要に応じて、microsoft Edge サーバーまたはエッジプールに XMPP プロキシを展開し、フロントエンドサーバーまたはフロントエンドプールに XMPP ゲートウェイサーバーを配置します。</span><span class="sxs-lookup"><span data-stu-id="e3390-108">Lync Server 2013 optionally deploys an XMPP proxy on the Edge Server or Edge pool and the XMPP gateway server on the Front End Server or Front End pool.</span></span>

<span data-ttu-id="e3390-109">IPv4 に加えて、エッジサーバーは IPv6 をサポートするようになりました。</span><span class="sxs-lookup"><span data-stu-id="e3390-109">In addition to IPv4, the Edge Server now supports IPv6.</span></span> <span data-ttu-id="e3390-110">わかりやすくするために、シナリオでは IPv4 のみが使用されます。</span><span class="sxs-lookup"><span data-stu-id="e3390-110">For clarity, only IPv4 is used in the scenarios.</span></span>

<span data-ttu-id="e3390-111">**ハードウェア負荷分散を使用した拡大縮小エッジ**</span><span class="sxs-lookup"><span data-stu-id="e3390-111">**Scaled Consolidated Edge using Hardware Load Balancing**</span></span>

<span data-ttu-id="e3390-112">![エッジ サーバー境界ネットワークのポートおよびプロトコル](images/Gg398739.063f7dd1-16db-4cc7-8708-bca9bc41184d(OCS.15).jpg "エッジ サーバー境界ネットワークのポートおよびプロトコル")</span><span class="sxs-lookup"><span data-stu-id="e3390-112">![Edge Server Perimeter Network ports and protocols](images/Gg398739.063f7dd1-16db-4cc7-8708-bca9bc41184d(OCS.15).jpg "Edge Server Perimeter Network ports and protocols")</span></span>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="e3390-113">ポートとプロトコルの詳細</span><span class="sxs-lookup"><span data-stu-id="e3390-113">Port and Protocol Details</span></span>

<span data-ttu-id="e3390-114">外部アクセスを提供する機能をサポートするために必要なポートのみを開くことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e3390-114">It is recommended that you open only the ports required to support the functionality for which you are providing external access.</span></span>

<span data-ttu-id="e3390-115">エッジサービスに対してリモートアクセスを使用するには、受信/送信エッジトラフィックの図に示すように、SIP トラフィックが双方向に流れるようにすることが必須です。</span><span class="sxs-lookup"><span data-stu-id="e3390-115">For remote access to work for any edge service, it is mandatory that SIP traffic is allowed to flow bi-directionally as shown in the Inbound/Outbound edge traffic figure.</span></span> <span data-ttu-id="e3390-116">別の方法として、アクセスエッジサービスとの間の SIP メッセージングは、インスタントメッセージング (IM)、プレゼンス、web 会議、音声/ビデオ (A/V)、およびフェデレーションに関連しています。</span><span class="sxs-lookup"><span data-stu-id="e3390-116">Stated another way, the SIP messaging to and from the Access Edge service is involved in instant messaging (IM), presence, web conferencing, audio/video (A/V) and federation.</span></span>

### <a name="firewall-summary-for-scaled-consolidated-edge-hardware-load-balanced-external-interface--node-1-and-node-2-example"></a><span data-ttu-id="e3390-117">スケーリングされた統合エッジのファイアウォールの概要: ハードウェア負荷分散: ノード1とノード 2 (例)</span><span class="sxs-lookup"><span data-stu-id="e3390-117">Firewall Summary for Scaled Consolidated Edge, Hardware Load Balanced: External Interface – Node 1 and Node 2 (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e3390-118">Role/Protocol/TCP または UDP/ポート</span><span class="sxs-lookup"><span data-stu-id="e3390-118">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="e3390-119">送信元 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="e3390-119">Source IP address</span></span></th>
<th><span data-ttu-id="e3390-120">宛先 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="e3390-120">Destination IP address</span></span></th>
<th><span data-ttu-id="e3390-121">メモ</span><span class="sxs-lookup"><span data-stu-id="e3390-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e3390-122">Access/HTTP/TCP/80</span><span class="sxs-lookup"><span data-stu-id="e3390-122">Access/HTTP/TCP/80</span></span></p></td>
<td><p><span data-ttu-id="e3390-123">エッジサーバーアクセスエッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="e3390-123">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="e3390-124">任意</span><span class="sxs-lookup"><span data-stu-id="e3390-124">Any</span></span></p></td>
<td><p><span data-ttu-id="e3390-125">証明書の失効/CRL の確認と取得</span><span class="sxs-lookup"><span data-stu-id="e3390-125">Certificate revocation/CRL check and retrieval</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3390-126">Access/DNS/TCP/53</span><span class="sxs-lookup"><span data-stu-id="e3390-126">Access/DNS/TCP/53</span></span></p></td>
<td><p><span data-ttu-id="e3390-127">エッジサーバーアクセスエッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="e3390-127">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="e3390-128">任意</span><span class="sxs-lookup"><span data-stu-id="e3390-128">Any</span></span></p></td>
<td><p><span data-ttu-id="e3390-129">TCP 経由の DNS クエリ</span><span class="sxs-lookup"><span data-stu-id="e3390-129">DNS query over TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3390-130">Access/DNS/UDP/53</span><span class="sxs-lookup"><span data-stu-id="e3390-130">Access/DNS/UDP/53</span></span></p></td>
<td><p><span data-ttu-id="e3390-131">エッジサーバーアクセスエッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="e3390-131">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="e3390-132">任意</span><span class="sxs-lookup"><span data-stu-id="e3390-132">Any</span></span></p></td>
<td><p><span data-ttu-id="e3390-133">UDP 経由の DNS クエリ</span><span class="sxs-lookup"><span data-stu-id="e3390-133">DNS query over UDP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3390-134">A/V/RTP/59,999</span><span class="sxs-lookup"><span data-stu-id="e3390-134">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="e3390-135">エッジサーバー A/V Edge サービス IP アドレス</span><span class="sxs-lookup"><span data-stu-id="e3390-135">Edge Server A/V Edge service IP address</span></span></p></td>
<td><p><span data-ttu-id="e3390-136">任意</span><span class="sxs-lookup"><span data-stu-id="e3390-136">Any</span></span></p></td>
<td><p><span data-ttu-id="e3390-137">Office Communications Server 2007、Office Communications Server 2007 R2、Lync Server 2010、および Lync Server 2013 を実行しているパートナーとのフェデレーションに必要。</span><span class="sxs-lookup"><span data-stu-id="e3390-137">Required for federating with partners running Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3390-138">A/V/RTP/59,999</span><span class="sxs-lookup"><span data-stu-id="e3390-138">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="e3390-139">エッジサーバーの A/V エッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="e3390-139">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="e3390-140">任意</span><span class="sxs-lookup"><span data-stu-id="e3390-140">Any</span></span></p></td>
<td><p><span data-ttu-id="e3390-141">Office Communications Server 2007 を実行しているパートナーとのフェデレーションの場合のみ必須です。</span><span class="sxs-lookup"><span data-stu-id="e3390-141">Required only for federation with partners running Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3390-142">A/V/RTP/59,999</span><span class="sxs-lookup"><span data-stu-id="e3390-142">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="e3390-143">任意</span><span class="sxs-lookup"><span data-stu-id="e3390-143">Any</span></span></p></td>
<td><p><span data-ttu-id="e3390-144">エッジサーバーの A/V エッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="e3390-144">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="e3390-145">Office Communications Server 2007 を実行しているパートナーとのフェデレーションにのみ必須</span><span class="sxs-lookup"><span data-stu-id="e3390-145">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3390-146">A/V/RTP/59,999</span><span class="sxs-lookup"><span data-stu-id="e3390-146">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="e3390-147">任意</span><span class="sxs-lookup"><span data-stu-id="e3390-147">Any</span></span></p></td>
<td><p><span data-ttu-id="e3390-148">エッジサーバーの A/V エッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="e3390-148">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="e3390-149">Office Communications Server 2007 を実行しているパートナーとのフェデレーションにのみ必須</span><span class="sxs-lookup"><span data-stu-id="e3390-149">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3390-150">A/V/STUN、MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="e3390-150">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="e3390-151">エッジサーバーの A/V エッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="e3390-151">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="e3390-152">任意</span><span class="sxs-lookup"><span data-stu-id="e3390-152">Any</span></span></p></td>
<td><p><span data-ttu-id="e3390-153">3478送信は、Lync Server が通信するエッジサーバーのバージョンと、エッジサーバーからエッジサーバーへのメディアトラフィックも確認するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="e3390-153">3478 outbound is used to determine the version of Edge Server that Lync Server is communicating with and also for media traffic from Edge Server-to-Edge Server.</span></span> <span data-ttu-id="e3390-154">Lync Server 2010、Windows Live Messenger、Office Communications Server 2007 R2 とのフェデレーション、および複数のエッジプールが会社内に展開されている場合に必要です。</span><span class="sxs-lookup"><span data-stu-id="e3390-154">Required for federation with Lync Server 2010, Windows Live Messenger, and Office Communications Server 2007 R2, and also if multiple Edge pools are deployed within a company.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3390-155">A/V/STUN、MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="e3390-155">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="e3390-156">任意</span><span class="sxs-lookup"><span data-stu-id="e3390-156">Any</span></span></p></td>
<td><p><span data-ttu-id="e3390-157">エッジサーバーの A/V エッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="e3390-157">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="e3390-158">UDP/3478 経由の候補のネゴシエーションをオフ/オンにする</span><span class="sxs-lookup"><span data-stu-id="e3390-158">STUN/TURN negotiation of candidates over UDP/3478</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3390-159">A/V/STUN、MSTURN/443</span><span class="sxs-lookup"><span data-stu-id="e3390-159">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="e3390-160">任意</span><span class="sxs-lookup"><span data-stu-id="e3390-160">Any</span></span></p></td>
<td><p><span data-ttu-id="e3390-161">エッジサーバーの A/V エッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="e3390-161">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="e3390-162">TCP/443 経由での候補のネゴシエーションをオフ/オンにする</span><span class="sxs-lookup"><span data-stu-id="e3390-162">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3390-163">A/V/STUN、MSTURN/443</span><span class="sxs-lookup"><span data-stu-id="e3390-163">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="e3390-164">エッジサーバーの A/V エッジサービスのパブリック IP アドレス</span><span class="sxs-lookup"><span data-stu-id="e3390-164">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="e3390-165">任意</span><span class="sxs-lookup"><span data-stu-id="e3390-165">Any</span></span></p></td>
<td><p><span data-ttu-id="e3390-166">TCP/443 経由での候補のネゴシエーションをオフ/オンにする</span><span class="sxs-lookup"><span data-stu-id="e3390-166">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-summary-for-scaled-consolidated-edge-hardware-load-balanced-internal-interface-node-1-and-node-2"></a><span data-ttu-id="e3390-167">スケーリングされた統合エッジのファイアウォールの概要、ハードウェア負荷分散: 内部インターフェイスノード1とノード2</span><span class="sxs-lookup"><span data-stu-id="e3390-167">Firewall Summary for Scaled Consolidated Edge, Hardware Load Balanced: Internal Interface Node 1 and Node 2</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e3390-168">Role/Protocol/TCP または UDP/ポート</span><span class="sxs-lookup"><span data-stu-id="e3390-168">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="e3390-169">送信元 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="e3390-169">Source IP address</span></span></th>
<th><span data-ttu-id="e3390-170">宛先 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="e3390-170">Destination IP address</span></span></th>
<th><span data-ttu-id="e3390-171">メモ</span><span class="sxs-lookup"><span data-stu-id="e3390-171">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e3390-172">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="e3390-172">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="e3390-173">Any (フロントエンドサーバーアドレスとして定義可能、または XMPP ゲートウェイサービスを実行するフロントエンドプール仮想 IP アドレス)</span><span class="sxs-lookup"><span data-stu-id="e3390-173">Any (can be defined as Front End Server address, or Front End pool virtual IP address running the XMPP Gateway service)</span></span></p></td>
<td><p><span data-ttu-id="e3390-174">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e3390-174">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="e3390-175">フロントエンドサーバーまたはフロントエンドプールで実行されている XMPP ゲートウェイサービスからの送信 XMPP トラフィック</span><span class="sxs-lookup"><span data-stu-id="e3390-175">Outbound XMPP traffic from XMPP Gateway service running on Front End Server or Front End pool</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3390-176">HTTPS/TCP/4443</span><span class="sxs-lookup"><span data-stu-id="e3390-176">HTTPS/TCP/4443</span></span></p></td>
<td><p><span data-ttu-id="e3390-177">Any (任意) (中央管理ストアを保持するフロントエンドサーバーサーバーの IP またはプールとして定義できます)</span><span class="sxs-lookup"><span data-stu-id="e3390-177">Any (can be defined as the Front End Server server IP or pool that holds the Central Management store)</span></span></p></td>
<td><p><span data-ttu-id="e3390-178">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e3390-178">Edge Server Internal interface</span></span></p></td>
<td><p><span data-ttu-id="e3390-179">中央管理ストアからエッジサーバーへの変更のレプリケーション</span><span class="sxs-lookup"><span data-stu-id="e3390-179">Replication of changes from the Central Management store to the Edge Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3390-180">PSOM/MTLS/TCP/8057</span><span class="sxs-lookup"><span data-stu-id="e3390-180">PSOM/MTLS/TCP/8057</span></span></p></td>
<td><p><span data-ttu-id="e3390-181">Any (ディレクター IP、フロントエンドサーバー IP またはプール仮想 IP として定義可能)</span><span class="sxs-lookup"><span data-stu-id="e3390-181">Any (can be defined as Director IP, Front End Server IP or Pool virtual IP)</span></span></p></td>
<td><p><span data-ttu-id="e3390-182">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e3390-182">Edge Server Internal interface</span></span></p></td>
<td><p><span data-ttu-id="e3390-183">内部展開から内部のエッジサーバーインターフェイスへの Web 会議トラフィック</span><span class="sxs-lookup"><span data-stu-id="e3390-183">Web conferencing traffic from Internal deployment to Internal Edge Server interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3390-184">STUN/MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="e3390-184">STUN/MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="e3390-185">Any (ディレクター IP、フロントエンドサーバー IP またはプール仮想 IP として定義可能)</span><span class="sxs-lookup"><span data-stu-id="e3390-185">Any (can be defined as Director IP, Front End Server IP or Pool virtual IP)</span></span></p></td>
<td><p><span data-ttu-id="e3390-186">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e3390-186">Edge Server Internal interface</span></span></p></td>
<td><p><span data-ttu-id="e3390-187">内部と外部のユーザー、Survivable Branch Appliance または Survivable ブランチサーバー間の A/V メディア転送の優先パス</span><span class="sxs-lookup"><span data-stu-id="e3390-187">Preferred path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3390-188">STUN/MSTURN/443</span><span class="sxs-lookup"><span data-stu-id="e3390-188">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="e3390-189">Any (ディレクター IP、フロントエンドサーバー IP またはプール仮想 IP として定義可能)</span><span class="sxs-lookup"><span data-stu-id="e3390-189">Any (can be defined as Director IP, Front End Server IP or Pool virtual IP)</span></span></p></td>
<td><p><span data-ttu-id="e3390-190">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e3390-190">Edge Server Internal interface</span></span></p></td>
<td><p><span data-ttu-id="e3390-191">内部と外部のユーザーとの間でのメディア転送のフォールバックパス Survivable Branch Appliance または Survivable Branch Server (UDP 通信が確立できない場合は、TCP を使ってファイル転送とデスクトップ共有を行う)</span><span class="sxs-lookup"><span data-stu-id="e3390-191">Fallback path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3390-192">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="e3390-192">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="e3390-193">任意</span><span class="sxs-lookup"><span data-stu-id="e3390-193">Any</span></span></p></td>
<td><p><span data-ttu-id="e3390-194">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e3390-194">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="e3390-195">Lync Server 管理シェルと一元ログサービスコマンドレット、ClsController コマンドライン (ClsController.exe) または agent (ClsAgent.exe) コマンドとログ収集を使用した一元的なログサービスコントローラー</span><span class="sxs-lookup"><span data-stu-id="e3390-195">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3390-196">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="e3390-196">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="e3390-197">任意</span><span class="sxs-lookup"><span data-stu-id="e3390-197">Any</span></span></p></td>
<td><p><span data-ttu-id="e3390-198">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e3390-198">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="e3390-199">Lync Server 管理シェルと一元ログサービスコマンドレット、ClsController コマンドライン (ClsController.exe) または agent (ClsAgent.exe) コマンドとログ収集を使用した一元的なログサービスコントローラー</span><span class="sxs-lookup"><span data-stu-id="e3390-199">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3390-200">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="e3390-200">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="e3390-201">任意</span><span class="sxs-lookup"><span data-stu-id="e3390-201">Any</span></span></p></td>
<td><p><span data-ttu-id="e3390-202">エッジサーバーの内部インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e3390-202">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="e3390-203">Lync Server 管理シェルと一元ログサービスコマンドレット、ClsController コマンドライン (ClsController.exe) または agent (ClsAgent.exe) コマンドとログ収集を使用した一元的なログサービスコントローラー</span><span class="sxs-lookup"><span data-stu-id="e3390-203">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e3390-204">ハードウェアロードバランサーを展開するときに、Lync Server の可用性と負荷分散を提供するための特定の要件があります。</span><span class="sxs-lookup"><span data-stu-id="e3390-204">Hardware load balancers have specific requirements when deployed to provide availability and load balancing for Lync Server.</span></span> <span data-ttu-id="e3390-205">要件は、次の図と表で定義されています。</span><span class="sxs-lookup"><span data-stu-id="e3390-205">The requirements are defined in the following figure and tables.</span></span> <span data-ttu-id="e3390-206">サードパーティベンダーは、ここで定義されている要件について別の用語を使用する場合があります。</span><span class="sxs-lookup"><span data-stu-id="e3390-206">Third party vendors may use different terminology for the requirements defined here.</span></span> <span data-ttu-id="e3390-207">Lync Server の要件を、ハードウェアロードバランサーのベンダーから提供されている機能と構成オプションにマップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e3390-207">It will be necessary to map the requirements of Lync Server to the features and configuration options provided by your hardware load balancer vendor.</span></span>

<span data-ttu-id="e3390-208">ハードウェアロードバランサーを構成する場合は、次の要件を考慮してください。</span><span class="sxs-lookup"><span data-stu-id="e3390-208">When configuring hardware load balancers, consider the following requirements:</span></span>

  - <span data-ttu-id="e3390-209">ソースネットワークアドレス変換 (SNAT) を、Access Edge サービスおよび Web 会議エッジサービスのハードウェアロードバランサー (HLB) で構成することができます。</span><span class="sxs-lookup"><span data-stu-id="e3390-209">Source Network Address Translation (SNAT) can be configured on the hardware load balancer (HLB) for Access Edge service and Web Conferencing Edge service</span></span>

  - <span data-ttu-id="e3390-210">SNAT を A/V Edge サービスで構成することはできません。 A/V Edge サービスは、UDP 経由の単純なトラバーサル (STUN)、または relay NAT (TURN) を使用したトラバーサル (FTURN) で正常に動作するように、実際のサーバーアドレスに応答する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e3390-210">SNAT cannot be configured on the A/V Edge service– the A/V Edge service must respond with the real server address, not the HLB virtual IP (VIP), for simple traversal of UDP over NAT (STUN)/traversal using relay NAT (TURN)/federation TURN (FTURN) to work properly</span></span>
    
      - <span data-ttu-id="e3390-211">クライアントが HLB に要求を送信した場合、応答は HLB VIP から返される必要があります。</span><span class="sxs-lookup"><span data-stu-id="e3390-211">If the client sends a request to the HLB, the response must come back from the HLB VIP</span></span>
    
      - <span data-ttu-id="e3390-212">クライアントが要求をエッジに送信した場合、応答はエッジ IP から返される必要があります。</span><span class="sxs-lookup"><span data-stu-id="e3390-212">If the client sends a request to the Edge, the response must come back from the Edge IP</span></span>

  - <span data-ttu-id="e3390-213">パブリック IP アドレスは、各サーバーインターフェイスと HLB の Vip で使用され、パブリック ip アドレスの要件は、それぞれの実際のサーバーインターフェイスのパブリック IP アドレスと、各 HLB VIP 用に1つずつ使用されます。</span><span class="sxs-lookup"><span data-stu-id="e3390-213">Public IP addresses are used on each server interface and on the VIPs of the HLB, and your public IP address requirements are N+1, where there is a public IP address for each real server interface and one for each HLB VIP.</span></span> <span data-ttu-id="e3390-214">プール内に2台のエッジサーバーがある場合、この結果、3つのパブリック IP アドレスが作成されます。ここでは、3は HLB Vip として、3は各エッジサーバーインターフェイスに対して使います (サーバーの場合は合計 6)。</span><span class="sxs-lookup"><span data-stu-id="e3390-214">Where you have 2 Edge servers in the pool, this results in 9 public IP addresses, where 3 are used for the HLB VIPs, and one for each Edge server interface (a total of six for the servers)</span></span>

  - <span data-ttu-id="e3390-215">クライアントは、アクセスエッジサービスおよび Web 会議エッジサービス (および HLB で NAT を使う) について、VIP に接続して、クライアントのソース IP アドレスをクライアントの IP アドレスに変更します。</span><span class="sxs-lookup"><span data-stu-id="e3390-215">For the Access Edge service and Web Conferencing Edge service, (and using NAT on the HLB) the client contacts the VIP, the VIP changes the source IP address from the client to its own IP address.</span></span> <span data-ttu-id="e3390-216">サーバーインターフェイスは、VIP に対して差出人住所を解決し、VIP によってサーバーインターフェイスの IP アドレスからソースアドレスが変更され、パケットがクライアントに送信されます。</span><span class="sxs-lookup"><span data-stu-id="e3390-216">The server interface addresses the return address to the VIP, the VIP changes the source address from the server interface IP address and sends the packet to the client</span></span>

  - <span data-ttu-id="e3390-217">A/V Edge サービスの場合、VIP はソースの IP アドレスを変更してはなりません。実際のサーバーのアドレスはクライアントに直接返され、AV トラフィック用に HLB で NAT を構成することはできません。</span><span class="sxs-lookup"><span data-stu-id="e3390-217">For the A/V Edge service, the VIP must NOT change the source IP address, and the real server address is returned to the client directly – you cannot configure NAT on the HLB for AV traffic</span></span>
    
      - <span data-ttu-id="e3390-218">クライアントが HLB VIP に要求を送信した場合、応答は HLB VIP から返される必要があります。</span><span class="sxs-lookup"><span data-stu-id="e3390-218">If the client sends a request to the HLB VIP, the response must come back from the HLB VIP</span></span>
    
      - <span data-ttu-id="e3390-219">クライアントが要求をエッジ IP に送信した場合、応答はエッジ IP から返される必要があります。</span><span class="sxs-lookup"><span data-stu-id="e3390-219">If the client sends a request to the Edge IP, the response must come back from the Edge IP</span></span>

  - <span data-ttu-id="e3390-220">AV の場合、外部ファイアウォールは、すべてのパケットに対して実際のサーバーのパブリック IP アドレスを保持します。</span><span class="sxs-lookup"><span data-stu-id="e3390-220">For AV, the external firewall will retain the real server public IP address for all packets</span></span>

  - <span data-ttu-id="e3390-221">確立されたクライアントから A/V Edge サービス通信は、HLB ではなく、実際のサーバーに対して行われます。</span><span class="sxs-lookup"><span data-stu-id="e3390-221">Once established, client to A/V Edge service communication is to the real server, not the HLB</span></span>

  - <span data-ttu-id="e3390-222">内部サーバーとクライアント間の内部境界はルーティングされる必要があり、サーバーまたはクライアントをホストするすべての内部ネットワークに対して固定ルートが設定されます。</span><span class="sxs-lookup"><span data-stu-id="e3390-222">Internal edge to internal servers and clients must be routed, and persistent routes are set for all internal networks that host servers or clients</span></span>

  - <span data-ttu-id="e3390-223">HLB Access Edge service VIP は、各エッジサーバーインターフェイスの既定のゲートウェイとして機能します。</span><span class="sxs-lookup"><span data-stu-id="e3390-223">The HLB Access Edge service VIP will act as the default gateway for each Edge server interface</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="e3390-224">NAT の計画と機能の詳細については、「 <A href="lync-server-2013-hardware-load-balancer-requirements.md">Lync Server 2013 のハードウェアロードバランサーの要件</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e3390-224">For further information on NAT planning and functionality, please refer to <A href="lync-server-2013-hardware-load-balancer-requirements.md">Hardware load balancer requirements for Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="e3390-225">![エッジ サーバーのポートおよびプロトコルの詳細](images/Gg398739.1c193b80-98ab-4d59-a854-dbfdb5e209e2(OCS.15).jpg "エッジ サーバーのポートおよびプロトコルの詳細")</span><span class="sxs-lookup"><span data-stu-id="e3390-225">![Edge Server ports and protocols details](images/Gg398739.1c193b80-98ab-4d59-a854-dbfdb5e209e2(OCS.15).jpg "Edge Server ports and protocols details")</span></span>

### <a name="external-port-settings-required-for-scaled-consolidated-edge-hardware-load-balanced-external-interface-virtual-ips"></a><span data-ttu-id="e3390-226">スケーリングされた統合エッジに必要な外部ポート設定、ハードウェア負荷分散: 外部インターフェイス仮想 Ip</span><span class="sxs-lookup"><span data-stu-id="e3390-226">External Port Settings Required for Scaled Consolidated Edge, Hardware Load Balanced: External Interface Virtual IPs</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e3390-227">Role/Protocol/TCP または UDP/ポート</span><span class="sxs-lookup"><span data-stu-id="e3390-227">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="e3390-228">送信元 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="e3390-228">Source IP address</span></span></th>
<th><span data-ttu-id="e3390-229">宛先 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="e3390-229">Destination IP address</span></span></th>
<th><span data-ttu-id="e3390-230">メモ</span><span class="sxs-lookup"><span data-stu-id="e3390-230">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e3390-231">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="e3390-231">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="e3390-232">任意</span><span class="sxs-lookup"><span data-stu-id="e3390-232">Any</span></span></p></td>
<td><p><span data-ttu-id="e3390-233">XMPP プロキシサービス (アクセスエッジサービスで IP アドレスを共有)</span><span class="sxs-lookup"><span data-stu-id="e3390-233">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="e3390-234">XMPP プロキシサービスは、定義された XMPP フェデレーションの XMPP 連絡先からのトラフィックを受け入れます。</span><span class="sxs-lookup"><span data-stu-id="e3390-234">XMPP Proxy service accepts traffic from XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3390-235">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="e3390-235">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="e3390-236">XMPP プロキシサービス (アクセスエッジサービスで IP アドレスを共有)</span><span class="sxs-lookup"><span data-stu-id="e3390-236">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="e3390-237">任意</span><span class="sxs-lookup"><span data-stu-id="e3390-237">Any</span></span></p></td>
<td><p><span data-ttu-id="e3390-238">XMPP プロキシサービスは、定義された XMPP フェデレーションの XMPP の連絡先にトラフィックを送信します。</span><span class="sxs-lookup"><span data-stu-id="e3390-238">XMPP Proxy service sends traffic to XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3390-239">アクセス/SIP (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="e3390-239">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="e3390-240">任意</span><span class="sxs-lookup"><span data-stu-id="e3390-240">Any</span></span></p></td>
<td><p><span data-ttu-id="e3390-241">アクセスエッジサービスのパブリック VIP アドレス</span><span class="sxs-lookup"><span data-stu-id="e3390-241">Access Edge service public VIP address</span></span></p></td>
<td><p><span data-ttu-id="e3390-242">外部ユーザーアクセスのクライアントツーサーバー SIP トラフィック</span><span class="sxs-lookup"><span data-stu-id="e3390-242">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3390-243">アクセス/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="e3390-243">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="e3390-244">任意</span><span class="sxs-lookup"><span data-stu-id="e3390-244">Any</span></span></p></td>
<td><p><span data-ttu-id="e3390-245">アクセスエッジサービスのパブリック VIP アドレス</span><span class="sxs-lookup"><span data-stu-id="e3390-245">Access Edge service public VIP address</span></span></p></td>
<td><p><span data-ttu-id="e3390-246">Sip を使用した SIP シグナリング、フェデレーションおよびパブリック IM 接続</span><span class="sxs-lookup"><span data-stu-id="e3390-246">SIP signaling, federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3390-247">アクセス/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="e3390-247">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="e3390-248">アクセスエッジサービスのパブリック VIP アドレス</span><span class="sxs-lookup"><span data-stu-id="e3390-248">Access Edge service public VIP address</span></span></p></td>
<td><p><span data-ttu-id="e3390-249">フェデレーションパートナー</span><span class="sxs-lookup"><span data-stu-id="e3390-249">Federated partner</span></span></p></td>
<td><p><span data-ttu-id="e3390-250">Sip を使用した SIP シグナリング、フェデレーションおよびパブリック IM 接続</span><span class="sxs-lookup"><span data-stu-id="e3390-250">SIP signaling, federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3390-251">Web 会議/PSOM (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="e3390-251">Web Conferencing/PSOM(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="e3390-252">任意</span><span class="sxs-lookup"><span data-stu-id="e3390-252">Any</span></span></p></td>
<td><p><span data-ttu-id="e3390-253">エッジサーバー Web 会議エッジサービスのパブリック VIP アドレス</span><span class="sxs-lookup"><span data-stu-id="e3390-253">Edge Server Web Conferencing Edge service public VIP address</span></span></p></td>
<td><p><span data-ttu-id="e3390-254">Web 会議メディア</span><span class="sxs-lookup"><span data-stu-id="e3390-254">Web Conferencing media</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3390-255">A/V/STUN、MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="e3390-255">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="e3390-256">任意</span><span class="sxs-lookup"><span data-stu-id="e3390-256">Any</span></span></p></td>
<td><p><span data-ttu-id="e3390-257">エッジサーバーの A/V エッジサービスのパブリック VIP アドレス</span><span class="sxs-lookup"><span data-stu-id="e3390-257">Edge Server A/V Edge service public VIP address</span></span></p></td>
<td><p><span data-ttu-id="e3390-258">UDP/3478 経由の候補のネゴシエーションをオフ/オンにする</span><span class="sxs-lookup"><span data-stu-id="e3390-258">STUN/TURN negotiation of candidates over UDP/3478</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3390-259">A/V/STUN、MSTURN/443</span><span class="sxs-lookup"><span data-stu-id="e3390-259">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="e3390-260">任意</span><span class="sxs-lookup"><span data-stu-id="e3390-260">Any</span></span></p></td>
<td><p><span data-ttu-id="e3390-261">エッジサーバーの A/V エッジサービスのパブリック VIP アドレス</span><span class="sxs-lookup"><span data-stu-id="e3390-261">Edge Server A/V Edge service public VIP address</span></span></p></td>
<td><p><span data-ttu-id="e3390-262">TCP/443 経由での候補のネゴシエーションをオフ/オンにする</span><span class="sxs-lookup"><span data-stu-id="e3390-262">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-summary-for-scaled-consolidated-edge-hardware-load-balanced-internal-interface-virtual-ips"></a><span data-ttu-id="e3390-263">スケーリングされた統合エッジのファイアウォールの概要: ハードウェア負荷分散: 内部インターフェイス仮想 Ip</span><span class="sxs-lookup"><span data-stu-id="e3390-263">Firewall Summary for Scaled Consolidated Edge, Hardware Load Balanced: Internal Interface Virtual IPs</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e3390-264">Role/Protocol/TCP または UDP/ポート</span><span class="sxs-lookup"><span data-stu-id="e3390-264">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="e3390-265">送信元 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="e3390-265">Source IP address</span></span></th>
<th><span data-ttu-id="e3390-266">宛先 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="e3390-266">Destination IP address</span></span></th>
<th><span data-ttu-id="e3390-267">メモ</span><span class="sxs-lookup"><span data-stu-id="e3390-267">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e3390-268">アクセス/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="e3390-268">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="e3390-269">Any (ディレクター、ディレクタープールの仮想 IP アドレス、フロントエンドサーバー、またはフロントエンドプールの仮想 IP アドレスとして定義できます)</span><span class="sxs-lookup"><span data-stu-id="e3390-269">Any (can be defined as Director, Director pool virtual IP address, Front End Server or Front End pool virtual IP address)</span></span></p></td>
<td><p><span data-ttu-id="e3390-270">エッジサーバーの内部 VIP インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e3390-270">Edge Server Internal VIP interface</span></span></p></td>
<td><p><span data-ttu-id="e3390-271">送信 SIP トラフィック (ディレクター、ディレクタープールの仮想 IP アドレス、フロントエンドサーバーまたはフロントエンドプールの仮想 IP アドレス) から内部エッジ VIP へ</span><span class="sxs-lookup"><span data-stu-id="e3390-271">Outbound SIP traffic (from Director, Director pool virtual IP address, Front End Server or Front End pool virtual IP address)to Internal Edge VIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3390-272">アクセス/SIP (MTLS)/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="e3390-272">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="e3390-273">エッジサーバーの内部 VIP インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e3390-273">Edge Server Internal VIP interface</span></span></p></td>
<td><p><span data-ttu-id="e3390-274">Any (ディレクター、ディレクタープールの仮想 IP アドレス、フロントエンドサーバー、またはフロントエンドプールの仮想 IP アドレスとして定義できます)</span><span class="sxs-lookup"><span data-stu-id="e3390-274">Any (can be defined as Director, Director pool virtual IP address, Front End Server or Front End pool virtual IP address)</span></span></p></td>
<td><p><span data-ttu-id="e3390-275">エッジサーバーの内部インターフェイスから受信 SIP トラフィック (ディレクター、ディレクタープールの仮想 IP アドレス、フロントエンドサーバー、またはフロントエンドプールの仮想 IP アドレス)</span><span class="sxs-lookup"><span data-stu-id="e3390-275">Inbound SIP traffic (to Director, Director pool virtual IP address, Front End Server or Front End pool virtual IP address) from Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3390-276">SIP/MTLS/TCP/5062</span><span class="sxs-lookup"><span data-stu-id="e3390-276">SIP/MTLS/TCP/5062</span></span></p></td>
<td><p><span data-ttu-id="e3390-277">Any (フロントエンドサーバーの IP アドレス、またはこのエッジサーバーを使用している Survivable Branch Appliance または Survivable ブランチサーバー) として定義することができます。</span><span class="sxs-lookup"><span data-stu-id="e3390-277">Any (can be defined as Front End Server IP address, or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server)</span></span></p></td>
<td><p><span data-ttu-id="e3390-278">エッジサーバーの内部 VIP インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e3390-278">Edge Server Internal VIP interface</span></span></p></td>
<td><p><span data-ttu-id="e3390-279">このエッジサーバーを使用して、フロントエンドサーバーまたはフロントエンドプールの IP アドレスまたは Survivable Branch Appliance または Survivable ブランチサーバーからの、A/V ユーザー (A/V 認証サービス) の認証</span><span class="sxs-lookup"><span data-stu-id="e3390-279">Authentication of A/V users (A/V authentication service) from Front End Server or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3390-280">STUN/MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="e3390-280">STUN/MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="e3390-281">任意</span><span class="sxs-lookup"><span data-stu-id="e3390-281">Any</span></span></p></td>
<td><p><span data-ttu-id="e3390-282">エッジサーバーの内部 VIP インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e3390-282">Edge Server Internal VIP interface</span></span></p></td>
<td><p><span data-ttu-id="e3390-283">内部と外部のユーザー間の A/V メディア転送の優先パス</span><span class="sxs-lookup"><span data-stu-id="e3390-283">Preferred path for A/V media transfer between internal and external users</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3390-284">STUN/MSTURN/443</span><span class="sxs-lookup"><span data-stu-id="e3390-284">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="e3390-285">任意</span><span class="sxs-lookup"><span data-stu-id="e3390-285">Any</span></span></p></td>
<td><p><span data-ttu-id="e3390-286">エッジサーバーの内部 VIP インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e3390-286">Edge Server Internal VIP interface</span></span></p></td>
<td><p><span data-ttu-id="e3390-287">内部と外部のユーザーとの間でのメディア転送のフォールバックパス UDP 通信を確立できない場合、TCP がファイル転送とデスクトップ共有に使用されます。</span><span class="sxs-lookup"><span data-stu-id="e3390-287">Fallback path for A/V media transfer between internal and external users if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3390-288">STUN/MSTURN/443</span><span class="sxs-lookup"><span data-stu-id="e3390-288">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="e3390-289">エッジサーバーの内部 VIP インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e3390-289">Edge Server Internal VIP interface</span></span></p></td>
<td><p><span data-ttu-id="e3390-290">任意</span><span class="sxs-lookup"><span data-stu-id="e3390-290">Any</span></span></p></td>
<td><p><span data-ttu-id="e3390-291">内部と外部のユーザーとの間でのメディア転送のフォールバックパス UDP 通信を確立できない場合、TCP がファイル転送とデスクトップ共有に使用されます。</span><span class="sxs-lookup"><span data-stu-id="e3390-291">Fallback path for A/V media transfer between internal and external users if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="e3390-292">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e3390-292">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

