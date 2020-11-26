---
title: 'Lync Server 2013: 外部の音声ビデオ ファイアウォールおよびポートの要件を決定する'
description: 'Lync Server 2013: 外部の A/V ファイアウォールとポートの要件を特定します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Determine external A/V firewall and port requirements
ms:assetid: 3b849dc7-175d-40d1-820d-80e6ade6d332
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425882(v=OCS.15)
ms:contentKeyID: 48183872
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 38c2a8c1e8e332a4a1e65adb87a1e962e82941c2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429519"
---
# <a name="determine-external-av-firewall-and-port-requirements-for-lync-server-2013"></a><span data-ttu-id="cb8ec-103">Lync Server 2013 の外部の音声ビデオ ファイアウォールおよびポートの要件を決定する</span><span class="sxs-lookup"><span data-stu-id="cb8ec-103">Determine external A/V firewall and port requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cb8ec-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cb8ec-104">

<span> </span></span></span>

<span data-ttu-id="cb8ec-105">_**最終更新日:** 2012-10-29_</span><span class="sxs-lookup"><span data-stu-id="cb8ec-105">_**Topic Last Modified:** 2012-10-29_</span></span>

<span data-ttu-id="cb8ec-106">音声/ビデオ (A/V) 通信は複雑な場合があります。</span><span class="sxs-lookup"><span data-stu-id="cb8ec-106">Audio/Video (A/V) communication can be a complex.</span></span> <span data-ttu-id="cb8ec-107">A/V で使用されるプロトコルの性質、およびクライアントとサーバーでのプロトコルの使用方法については、クライアントとサーバーのバージョンの違いを説明するための特別なセクションが保証されています。</span><span class="sxs-lookup"><span data-stu-id="cb8ec-107">Because of the nature of protocols used in A/V and how clients and servers use the protocols, a special section is warranted to explain the differences between client and server versions.</span></span>

<span data-ttu-id="cb8ec-108">ファイアウォール要件と開くポートを決定するには、次の A/V ファイアウォールとポートテーブルを使用します。</span><span class="sxs-lookup"><span data-stu-id="cb8ec-108">Use the following A/V Firewall and Port table to determine firewall requirements and which ports to open.</span></span> <span data-ttu-id="cb8ec-109">次に、NAT がさまざまな方法で実装されるため、ネットワークアドレス変換 (NAT) 用語を確認します。</span><span class="sxs-lookup"><span data-stu-id="cb8ec-109">Then, review the network address translation (NAT) terminology because NAT can be implemented in many different ways.</span></span> <span data-ttu-id="cb8ec-110">ファイアウォールポート設定の詳細な例については、「 [Lync Server 2013 での外部ユーザーアクセスのシナリオ](lync-server-2013-scenarios-for-external-user-access.md)でのリファレンスアーキテクチャ」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cb8ec-110">For a detailed example of firewall port settings, see the reference architectures in [Scenarios for external user access in Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md).</span></span>

### <a name="general-protocol-usage-for-udp-and-tcp-in-audiovideo-and-media-traffic"></a><span data-ttu-id="cb8ec-111">音声/ビデオおよびメディアトラフィックでの UDP および TCP の一般的なプロトコルの使用</span><span class="sxs-lookup"><span data-stu-id="cb8ec-111">General Protocol Usage for UDP and TCP in Audio/Video and Media Traffic</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cb8ec-112">音声/ビデオトランスポート</span><span class="sxs-lookup"><span data-stu-id="cb8ec-112">Audio/Video Transport</span></span></th>
<th><span data-ttu-id="cb8ec-113">用途</span><span class="sxs-lookup"><span data-stu-id="cb8ec-113">Usage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cb8ec-114">UDP</span><span class="sxs-lookup"><span data-stu-id="cb8ec-114">UDP</span></span></p></td>
<td><p><span data-ttu-id="cb8ec-115">オーディオおよびビデオの優先トランスポート層プロトコル</span><span class="sxs-lookup"><span data-stu-id="cb8ec-115">Preferred transport layer protocol for audio and video</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb8ec-116">TCP</span><span class="sxs-lookup"><span data-stu-id="cb8ec-116">TCP</span></span></p></td>
<td><p><span data-ttu-id="cb8ec-117">オーディオおよびビデオのフォールバックトランスポート層プロトコル</span><span class="sxs-lookup"><span data-stu-id="cb8ec-117">Fallback transport layer protocol for audio and video</span></span></p>
<p><span data-ttu-id="cb8ec-118">Office Communications Server 2007 R2、Lync Server 2010、Lync Server 2013 へのアプリケーション共有に必要なトランスポートレイヤープロトコル</span><span class="sxs-lookup"><span data-stu-id="cb8ec-118">Required transport layer protocol for application sharing to Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013</span></span></p>
<p><span data-ttu-id="cb8ec-119">Lync Server 2010 および Lync Server 2013 へのファイル転送に必要なトランスポートレイヤープロトコル</span><span class="sxs-lookup"><span data-stu-id="cb8ec-119">Required transport layer protocol for file transfer to Lync Server 2010 and Lync Server 2013</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="external-av-firewall-port-requirements-for-external-user-access"></a><span data-ttu-id="cb8ec-120">外部ユーザーアクセスの外部の A/V ファイアウォールポートの要件</span><span class="sxs-lookup"><span data-stu-id="cb8ec-120">External A/V Firewall Port Requirements for External User Access</span></span>

<span data-ttu-id="cb8ec-121">クライアントのバージョンやフェデレーションパートナーのバージョンに関係なく、外部 (および内部) SIP と会議インターフェイスのファイアウォールポート要件は一貫しています。</span><span class="sxs-lookup"><span data-stu-id="cb8ec-121">The firewall port requirements for external (and internal) SIP and conferencing interfaces are consistent, regardless of the version of your client or the version of the federation partner.</span></span>

<span data-ttu-id="cb8ec-122">オーディオ/ビデオエッジの外部インターフェイスには、同じことが当てはまりません。</span><span class="sxs-lookup"><span data-stu-id="cb8ec-122">The same is not true for the Audio/Video Edge external interface.</span></span> <span data-ttu-id="cb8ec-123">Office Communications Server 2007 とのフェデレーションの場合、A/V Edge サービスでは、外部ファイアウォールルールによって、5万 ~ 59999 ポート範囲内の RTP/TCP トラフィックと RTP/UDP トラフィックが両方の方向に流れるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb8ec-123">For federation with Office Communications Server 2007, the A/V Edge service requires that external firewall rules allow RTP/TCP and RTP/UDP traffic in the 50,000 through 59,999 port range to flow in both directions.</span></span> <span data-ttu-id="cb8ec-124">上記の表では、Lync Server 2013 がプライマリフェデレーションパートナーであり、一覧されている他のフェデレーションパートナーのいずれかと通信するように構成されていることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="cb8ec-124">The previous table assumes that Lync Server 2013 is the primary federation partner and it is being configured to communicate with one of the other federation partner types listed.</span></span>

<span data-ttu-id="cb8ec-125">59,999 の音声/ビデオポート範囲を構成するには、ポート範囲にフェデレーションパートナーへの通信のソースポートが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb8ec-125">Configuring the Audio/Video port range of 50,000-59,999 must take into account that the port range will contain the source ports for communications to federation partners.</span></span> <span data-ttu-id="cb8ec-126">詳細については、通信がフェデレーションパートナーから開始されることを考慮してください。</span><span class="sxs-lookup"><span data-stu-id="cb8ec-126">In detail, consider that a communication is initiated from a federation partner.</span></span> <span data-ttu-id="cb8ec-127">59,999 範囲の A/V Edge サービスポートからの通信は、パートナーの A/V Edge サービスの予期されるポート TCP 443 に接続します。</span><span class="sxs-lookup"><span data-stu-id="cb8ec-127">The communication from the A/V Edge service ports in the 50,000-59,999 range will connect to the expected port TCP 443 of the partner’s A/V Edge service.</span></span> <span data-ttu-id="cb8ec-128">反対に、A/V Edge サービス443ポートへの受信トラフィックは、59,999 の範囲のソースポートを持ちます。</span><span class="sxs-lookup"><span data-stu-id="cb8ec-128">Conversely, inbound traffic to your A/V Edge service port TCP 443 will have a source port in the range of 50,000-59,999.</span></span>

<span data-ttu-id="cb8ec-129">ファイアウォール管理用のさまざまなファイアウォールとポリシーには、構成するためのターゲットルールのみを設定するか、またはソースとターゲットの両方を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb8ec-129">Different firewalls and policies for firewall administration may require only destination rules to be configured, or they may require both source and destination to be configured.</span></span> <span data-ttu-id="cb8ec-130">目的が宛先ポート専用の場合は、オーディオ/ビデオの要件は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="cb8ec-130">If your requirements are for destination ports only, the Audio/Video requirements are:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cb8ec-131">発信元 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="cb8ec-131">Source IP</span></span></th>
<th><span data-ttu-id="cb8ec-132">送信先 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="cb8ec-132">Destination IP</span></span></th>
<th><span data-ttu-id="cb8ec-133">送信先ポート</span><span class="sxs-lookup"><span data-stu-id="cb8ec-133">Destination Port</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cb8ec-134">A/V Edge サービスインターフェイス</span><span class="sxs-lookup"><span data-stu-id="cb8ec-134">A/V Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="cb8ec-135">任意</span><span class="sxs-lookup"><span data-stu-id="cb8ec-135">Any</span></span></p></td>
<td><p><span data-ttu-id="cb8ec-136">TCP 443</span><span class="sxs-lookup"><span data-stu-id="cb8ec-136">TCP 443</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb8ec-137">A/V Edge サービスインターフェイス</span><span class="sxs-lookup"><span data-stu-id="cb8ec-137">A/V Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="cb8ec-138">任意</span><span class="sxs-lookup"><span data-stu-id="cb8ec-138">Any</span></span></p></td>
<td><p><span data-ttu-id="cb8ec-139">UDP 3478</span><span class="sxs-lookup"><span data-stu-id="cb8ec-139">UDP 3478</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb8ec-140">任意</span><span class="sxs-lookup"><span data-stu-id="cb8ec-140">Any</span></span></p></td>
<td><p><span data-ttu-id="cb8ec-141">A/V Edge サービスインターフェイス</span><span class="sxs-lookup"><span data-stu-id="cb8ec-141">A/V Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="cb8ec-142">TCP 443</span><span class="sxs-lookup"><span data-stu-id="cb8ec-142">TCP 443</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb8ec-143">任意</span><span class="sxs-lookup"><span data-stu-id="cb8ec-143">Any</span></span></p></td>
<td><p><span data-ttu-id="cb8ec-144">A/V Edge サービスインターフェイス</span><span class="sxs-lookup"><span data-stu-id="cb8ec-144">A/V Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="cb8ec-145">UDP 3478</span><span class="sxs-lookup"><span data-stu-id="cb8ec-145">UDP 3478</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cb8ec-146">ポリシーで受信と送信の両方のファイアウォール規則の定義が必要な場合、音声/ビデオの要件は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="cb8ec-146">If your policies require both inbound and outbound firewall rule definitions, the Audio/Video requirements are:</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cb8ec-147">発信元 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="cb8ec-147">Source IP</span></span></th>
<th><span data-ttu-id="cb8ec-148">送信先 IP アドレス</span><span class="sxs-lookup"><span data-stu-id="cb8ec-148">Destination IP</span></span></th>
<th><span data-ttu-id="cb8ec-149">発信元ポート</span><span class="sxs-lookup"><span data-stu-id="cb8ec-149">Source Port</span></span></th>
<th><span data-ttu-id="cb8ec-150">送信先ポート</span><span class="sxs-lookup"><span data-stu-id="cb8ec-150">Destination Port</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cb8ec-151">A/V Edge サービスインターフェイス</span><span class="sxs-lookup"><span data-stu-id="cb8ec-151">A/V Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="cb8ec-152">任意</span><span class="sxs-lookup"><span data-stu-id="cb8ec-152">Any</span></span></p></td>
<td><p><span data-ttu-id="cb8ec-153">TCP 50,000 ～ 59,999</span><span class="sxs-lookup"><span data-stu-id="cb8ec-153">TCP 50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="cb8ec-154">TCP 443</span><span class="sxs-lookup"><span data-stu-id="cb8ec-154">TCP 443</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb8ec-155">A/V Edge サービスインターフェイス</span><span class="sxs-lookup"><span data-stu-id="cb8ec-155">A/V Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="cb8ec-156">任意</span><span class="sxs-lookup"><span data-stu-id="cb8ec-156">Any</span></span></p></td>
<td><p><span data-ttu-id="cb8ec-157">UDP 3478</span><span class="sxs-lookup"><span data-stu-id="cb8ec-157">UDP 3478</span></span></p></td>
<td><p><span data-ttu-id="cb8ec-158">UDP 3478</span><span class="sxs-lookup"><span data-stu-id="cb8ec-158">UDP 3478</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb8ec-159">任意</span><span class="sxs-lookup"><span data-stu-id="cb8ec-159">Any</span></span></p></td>
<td><p><span data-ttu-id="cb8ec-160">A/V Edge サービスインターフェイス</span><span class="sxs-lookup"><span data-stu-id="cb8ec-160">A/V Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="cb8ec-161">任意</span><span class="sxs-lookup"><span data-stu-id="cb8ec-161">Any</span></span></p></td>
<td><p><span data-ttu-id="cb8ec-162">TCP 443</span><span class="sxs-lookup"><span data-stu-id="cb8ec-162">TCP 443</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb8ec-163">任意</span><span class="sxs-lookup"><span data-stu-id="cb8ec-163">Any</span></span></p></td>
<td><p><span data-ttu-id="cb8ec-164">A/V Edge サービスインターフェイス</span><span class="sxs-lookup"><span data-stu-id="cb8ec-164">A/V Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="cb8ec-165">任意</span><span class="sxs-lookup"><span data-stu-id="cb8ec-165">Any</span></span></p></td>
<td><p><span data-ttu-id="cb8ec-166">UDP 3478</span><span class="sxs-lookup"><span data-stu-id="cb8ec-166">UDP 3478</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!IMPORTANT]  
> <span data-ttu-id="cb8ec-167">Microsoft Office Communications Server 2007 では、若干異なる構成が必要です。</span><span class="sxs-lookup"><span data-stu-id="cb8ec-167">Microsoft Office Communications Server 2007 requires a slightly different configuration.</span></span> <span data-ttu-id="cb8ec-168">59,999 の TCP ポート範囲と UDP ポート範囲は、受信と送信が開いている必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb8ec-168">The TCP and UDP port range of 50,000-59,999 must be open inbound and outbound.</span></span> <span data-ttu-id="cb8ec-169">この要件は、Office Communicator 2007 に限定されます。</span><span class="sxs-lookup"><span data-stu-id="cb8ec-169">This requirement is only for Office Communicator 2007.</span></span> <span data-ttu-id="cb8ec-170">Office Communications Server 2007 R2、Lync Server 2010、Lync Server 2013 には、TCP 範囲 50000-59,999 open outbound が必要です。</span><span class="sxs-lookup"><span data-stu-id="cb8ec-170">Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013 only require TCP range 50,000-59,999 open outbound.</span></span>



</div>

</div>

<div>

## <a name="nat-requirements-for-the-edge-service"></a><span data-ttu-id="cb8ec-171">エッジサービスの NAT 要件</span><span class="sxs-lookup"><span data-stu-id="cb8ec-171">NAT requirements for the Edge service</span></span>

<span data-ttu-id="cb8ec-172">エッジサービスに対してルーティングできないプライベート IP アドレスを構成する場合は、次の NAT 要件が適用されます。</span><span class="sxs-lookup"><span data-stu-id="cb8ec-172">The following NAT requirements apply if you choose to configure non-routable private IP addresses for the Edge service:</span></span>

  - <span data-ttu-id="cb8ec-173">NAT は、DNS の負荷分散でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="cb8ec-173">NAT can only be used with DNS load-balancing.</span></span> <span data-ttu-id="cb8ec-174">NAT は、ハードウェア負荷分散 (HLB) エッジトポロジではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="cb8ec-174">NAT is not supported with a hardware load balancing (HLB) Edge topology.</span></span>

  - <span data-ttu-id="cb8ec-175">NAT は、外部 Edge インターフェイスでのみ使うことができます。</span><span class="sxs-lookup"><span data-stu-id="cb8ec-175">NAT can only be used on the external Edge interface.</span></span> <span data-ttu-id="cb8ec-176">NAT は、内部エッジインターフェイスではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="cb8ec-176">NAT is not supported on the internal Edge interface.</span></span>

  - <span data-ttu-id="cb8ec-177">NAT は、受信トラフィックと発信トラフィックに対称である必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb8ec-177">NAT must be symmetric for incoming and outgoing traffic.</span></span>
    
  - <span data-ttu-id="cb8ec-178">インターネットからのトラフィックの場合、NAT は、宛先の IP アドレスを、A/V Edge サービスの NAT 対応のパブリック IP アドレスから外部 IP アドレスに変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb8ec-178">For traffic from the Internet, NAT must change the destination IP address from the NAT-enabled public IP address of the A/V Edge service to its external IP address.</span></span> <span data-ttu-id="cb8ec-179">ソース IP アドレスはそのままにしておく必要があります。そのため、A/V Edge サービスは最適なメディアパスを見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="cb8ec-179">The source IP address must remain intact, so that the A/V Edge service can find the optimal media path.</span></span>
  
  <span data-ttu-id="cb8ec-180">たとえば、次の図の受信方向では、パブリック IP アドレスの131.107.155.30 が外部 (プライベート) IP アドレス10.45.16.10 に変更されました。</span><span class="sxs-lookup"><span data-stu-id="cb8ec-180">For example, in the inbound direction in the figure below, the public IP address 131.107.155.30 was changed to the external (private) IP address 10.45.16.10.</span></span> <span data-ttu-id="cb8ec-181">ソース IP アドレスは変更されていません。</span><span class="sxs-lookup"><span data-stu-id="cb8ec-181">The source IP address remained unchanged.</span></span>
  
  - <span data-ttu-id="cb8ec-182">NAT では、A/v Edge サービスからインターネットへのトラフィックについて、ソース IP アドレスを、A/V Edge サービスの外部 IP アドレスから NAT 対応のパブリック IP アドレスに変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb8ec-182">For traffic from the A/V Edge service to the Internet, NAT must change the source IP address from the external IP address of the A/V Edge service to the NAT-enabled public IP address.</span></span>

<span data-ttu-id="cb8ec-183">たとえば、次の図のような送信方向の場合、外部 (プライベート) IP アドレス10.45.16.10 はパブリック IP アドレス131.107.155.30 に変更されました。</span><span class="sxs-lookup"><span data-stu-id="cb8ec-183">For example, in the outbound direction in the figure below, the external (private) IP address 10.45.16.10 was changed to the public IP address 131.107.155.30.</span></span>

<span data-ttu-id="cb8ec-184">**次の図は、NAT で受信トラフィックの送信先 IP アドレスと送信トラフィックのソース IP アドレスを変更する方法を示しています。**</span><span class="sxs-lookup"><span data-stu-id="cb8ec-184">**The figure below shows how NAT changes the destination IP address for inbound traffic and the source IP Address for outbound traffic.**</span></span>

<span data-ttu-id="cb8ec-185">![送信先/送信元 IP アドレスの変更](images/Gg425882.0fee7ec5-4cb8-4aff-9164-e7fbab73336d(OCS.15).jpg "送信先/送信元 IP アドレスの変更")</span><span class="sxs-lookup"><span data-stu-id="cb8ec-185">![Changing destination/source IP addresses](images/Gg425882.0fee7ec5-4cb8-4aff-9164-e7fbab73336d(OCS.15).jpg "Changing destination/source IP addresses")</span></span>

<span data-ttu-id="cb8ec-186">重要なポイントは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="cb8ec-186">The key points are:</span></span>

  - <span data-ttu-id="cb8ec-187">A/V Edge サービスを実行しているサーバーへのトラフィックは、ソース IP アドレスは変更されませんが、宛先 IP アドレスは131.107.155.30 から10.45.16.10 の変換済み IP アドレスに変わります。</span><span class="sxs-lookup"><span data-stu-id="cb8ec-187">Traffic that is inbound to the server running the A/V Edge service, the source IP address does not change but the destination IP address changes from 131.107.155.30 to the translated IP address of 10.45.16.10.</span></span>

  - <span data-ttu-id="cb8ec-188">A/V Edge サービスを実行しているサーバーからワークステーションに送信されるトラフィックについては、ソース IP アドレスがサーバーのパブリック IP アドレスから、A/V Edge サービスを実行しているサーバーのパブリック IP アドレスに変わります。</span><span class="sxs-lookup"><span data-stu-id="cb8ec-188">Traffic that is outbound from the server running the A/V Edge service back to the workstation, the source IP address changes from the server’s public IP address to the public IP address of the server running the A/V Edge service.</span></span> <span data-ttu-id="cb8ec-189">送信先 IP は、ワークステーションのパブリック IP アドレスのままです。</span><span class="sxs-lookup"><span data-stu-id="cb8ec-189">The destination IP remains the workstation’s public IP address.</span></span> <span data-ttu-id="cb8ec-190">パケットが最初の NAT デバイスから送信されると、NAT デバイス上のルールによって、A/V Edge サービスの外部インターフェイス IP アドレス (10.45.16.10) を実行しているサーバーのソース IP アドレスが、そのパブリック IP アドレス (131.107.155.30) に変更されます。</span><span class="sxs-lookup"><span data-stu-id="cb8ec-190">After the packet leaves the first NAT device outbound, the rule on the NAT device changes the source IP address of the server running the A/V Edge service external interface IP address (10.45.16.10) to its public IP address (131.107.155.30).</span></span>

<span data-ttu-id="cb8ec-191"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cb8ec-191"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

