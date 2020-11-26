---
title: ユーザーモデルを使用した Lync Server 2013 キャパシティ計画
description: Lync Server 2013 ユーザーモデルを使用した容量の計画。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Capacity planning using the user models
ms:assetid: 902ab23e-94d6-482a-9d6e-c0b28dc3e03d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615015(v=OCS.15)
ms:contentKeyID: 49733733
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6b710f7ec88dd75c872d704f2169fa2f161fc186
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435510"
---
# <a name="capacity-planning-for-lync-server-2013-using-the-user-models"></a><span data-ttu-id="bbe83-103">ユーザーモデルを使用した Lync Server 2013 のキャパシティ計画</span><span class="sxs-lookup"><span data-stu-id="bbe83-103">Capacity planning for Lync Server 2013 using the user models</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bbe83-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bbe83-104">

<span> </span></span></span>

<span data-ttu-id="bbe83-105">_**最終更新日:** 2014-01-14_</span><span class="sxs-lookup"><span data-stu-id="bbe83-105">_**Topic Last Modified:** 2014-01-14_</span></span>

<span data-ttu-id="bbe83-106">このセクションでは、 [Lync Server 2013 のユーザーモデル](lync-server-2013-user-models.md)で説明されている使用法に従って、そのサイトのユーザー数に応じてサイトで必要なサーバー数について説明します。</span><span class="sxs-lookup"><span data-stu-id="bbe83-106">This section provides guidance on how many servers you need at a site for the number of users at that site, according to the usage described in [User models in Lync Server 2013](lync-server-2013-user-models.md).</span></span>

<div>

## <a name="tested-hardware-platform"></a><span data-ttu-id="bbe83-107">テスト済みのハードウェア プラットフォーム</span><span class="sxs-lookup"><span data-stu-id="bbe83-107">Tested Hardware Platform</span></span>

<span data-ttu-id="bbe83-108">このセクションのパフォーマンスの結果と展開に関する推奨事項はすべて、次の表で説明されているハードウェアを実行しているサーバーでのパフォーマンステストに基づいています。</span><span class="sxs-lookup"><span data-stu-id="bbe83-108">All the performance results and deployment recommendations in this section are based on performance testing on servers running the hardware described in the following table.</span></span> <span data-ttu-id="bbe83-109">同様のハードウェアを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="bbe83-109">We recommend that you use similar hardware.</span></span> <span data-ttu-id="bbe83-110">性能の低いハードウェアを使用している場合は、機能の問題が発生するか、パフォーマンスが低下することがあります。</span><span class="sxs-lookup"><span data-stu-id="bbe83-110">If you use less powerful hardware, you may experience functionality problems or poor performance.</span></span> <span data-ttu-id="bbe83-111">これらのハードウェアの推奨事項は、以前のバージョンの Lync Server よりも高いことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="bbe83-111">Note that these hardware recommendations are higher than those of previous versions of Lync Server.</span></span>

### <a name="hardware-used-in-performance-testing"></a><span data-ttu-id="bbe83-112">パフォーマンス テストで使用するハードウェア</span><span class="sxs-lookup"><span data-stu-id="bbe83-112">Hardware Used in Performance Testing</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bbe83-113">ハードウェア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="bbe83-113">Hardware component</span></span></th>
<th><span data-ttu-id="bbe83-114">推奨</span><span class="sxs-lookup"><span data-stu-id="bbe83-114">Recommended</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bbe83-115">CPU</span><span class="sxs-lookup"><span data-stu-id="bbe83-115">CPU</span></span></p></td>
<td><p><span data-ttu-id="bbe83-116">64 ビット デュアル プロセッサ、6 コア、2.26 GHz 以上</span><span class="sxs-lookup"><span data-stu-id="bbe83-116">64-bit dual processor, hex-core, 2.26 gigahertz (GHz) or higher</span></span></p>
<p><span data-ttu-id="bbe83-117">Lync Server server の役割では、Intel Itanium プロセッサはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="bbe83-117">Intel Itanium processors are not supported for Lync Server server roles.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbe83-118">メモリ</span><span class="sxs-lookup"><span data-stu-id="bbe83-118">Memory</span></span></p></td>
<td><p><span data-ttu-id="bbe83-119">32 ギガバイト (GB)</span><span class="sxs-lookup"><span data-stu-id="bbe83-119">32 gigabytes (GB)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbe83-120">ディスク</span><span class="sxs-lookup"><span data-stu-id="bbe83-120">Disk</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="bbe83-121">10,000 RPM のハード ディスク ドライブで 72 GB 以上の空きディスク領域があるものを 8 台以上。</span><span class="sxs-lookup"><span data-stu-id="bbe83-121">8 or more 10,000-RPM hard disk drives with at least 72 GB free disk space.</span></span></p>
<p><span data-ttu-id="bbe83-122">ディスクのうち 2 台で RAID 1 を使用し、6 台で RAID 10 を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bbe83-122">Two of the disks should use RAID 1, and six should use RAID 10.</span></span></p>
<p><span data-ttu-id="bbe83-123">- /</span><span class="sxs-lookup"><span data-stu-id="bbe83-123">- OR -</span></span></p></li>
<li><p><span data-ttu-id="bbe83-124">10,000 RPM の機械的ディスク ドライブ 8 台と同等のパフォーマンスを持つソリッド ステート ドライブ (SSD)</span><span class="sxs-lookup"><span data-stu-id="bbe83-124">Solid state drives (SSDs) which provide performance similar to 8 10,000-RPM mechanical disk drives.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbe83-125">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="bbe83-125">Network</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="bbe83-126">1 Gbps 以上のデュアルポート ネットワーク アダプター 1 つ (2 つを推奨。その場合は 1 つの MAC アドレスと 1 つの IP アドレスのチーミングが必要)</span><span class="sxs-lookup"><span data-stu-id="bbe83-126">1 dual-port network adapter, 1 Gbps or higher (2 recommended, which requires teaming with a single MAC address and single IP address)</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="summary-of-results"></a><span data-ttu-id="bbe83-127">結果の概要</span><span class="sxs-lookup"><span data-stu-id="bbe83-127">Summary of Results</span></span>

<span data-ttu-id="bbe83-128">次の表は、これらの推奨事項をまとめたものです。</span><span class="sxs-lookup"><span data-stu-id="bbe83-128">The following table summarizes these recommendations.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bbe83-129">サーバーの役割</span><span class="sxs-lookup"><span data-stu-id="bbe83-129">Server role</span></span></th>
<th><span data-ttu-id="bbe83-130">サポートされる最大ユーザー数</span><span class="sxs-lookup"><span data-stu-id="bbe83-130">Maximum number of users supported</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bbe83-131">12個のフロントエンドサーバーと1つのバックエンドサーバー、またはバックエンドサーバーのミラーされたペアのフロントエンドプール。</span><span class="sxs-lookup"><span data-stu-id="bbe83-131">Front End pool with twelve Front End Servers and one Back End Server or a mirrored pair of Back End Servers.</span></span></p></td>
<td><p><span data-ttu-id="bbe83-132">エンドポイントの合計 152,000 に対し、同時にログインする 80,000 の一意ユーザー、および非モバイル インスタンスを表す 50% の複数の MPOP (Multiple Point of Presence)、モビリティが有効な 40% のユーザー。</span><span class="sxs-lookup"><span data-stu-id="bbe83-132">80,000 unique users simultaneously logged in, plus 50% multiple points of presence (MPOP) representing non-mobile instances, plus 40% of users enabled for Mobility for a total of 152,000 endpoints.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbe83-133">音声ビデオ会議</span><span class="sxs-lookup"><span data-stu-id="bbe83-133">A/V Conferencing</span></span></p></td>
<td><p><span data-ttu-id="bbe83-134">フロントエンドプールによって提供される A/V 会議サービスは、最大会議サイズが250ユーザーであり、その大人数の会議は一度に1つだけ実行されることを前提とした、プールの会議をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="bbe83-134">The A/V Conferencing service provided by a Front End pool supports the pool’s conferences assuming a maximum conference size of 250 users, and only one such large conference running at a time.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="bbe83-135">さらに、250と1000ユーザーの間の大規模な会議をサポートするには、2つのフロントエンドサーバーと、大きな会議をホストするための、別々のフロントエンドプールを展開します。</span><span class="sxs-lookup"><span data-stu-id="bbe83-135">Additionally, you can support large conferences of between 250 and 1000 users by deploying a separate Front End pool with two Front End Servers to host the large conferences.</span></span> <span data-ttu-id="bbe83-136">詳細については、「 <A href="lync-server-2013-supporting-large-meetings.md">Lync Server 2013 を使用した大規模な会議のサポート</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bbe83-136">For details, see <A href="lync-server-2013-supporting-large-meetings.md">Supporting large meetings using Lync Server 2013</A>.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbe83-137">1つのエッジサーバー</span><span class="sxs-lookup"><span data-stu-id="bbe83-137">One Edge Server</span></span></p></td>
<td><p><span data-ttu-id="bbe83-138">12000同時リモートユーザー</span><span class="sxs-lookup"><span data-stu-id="bbe83-138">12,000 concurrent remote users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbe83-139">1人のディレクター</span><span class="sxs-lookup"><span data-stu-id="bbe83-139">One Director</span></span></p></td>
<td><p><span data-ttu-id="bbe83-140">12000同時リモートユーザー</span><span class="sxs-lookup"><span data-stu-id="bbe83-140">12,000 concurrent remote users</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbe83-141">監視およびアーカイブ</span><span class="sxs-lookup"><span data-stu-id="bbe83-141">Monitoring and Archiving</span></span></p></td>
<td><p><span data-ttu-id="bbe83-142">Lync Server 2013 では、個別のサーバーの役割ではなく、フロントエンドサーバーごとに、監視およびアーカイブのフロントエンドサービスが実行されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="bbe83-142">In Lync Server 2013, the Monitoring and Archiving front end services now run on each Front End Server, instead of on separate server roles.</span></span></p>
<p><span data-ttu-id="bbe83-143">監視とアーカイブにはそれぞれ専用のデータベース ストアが必要です。</span><span class="sxs-lookup"><span data-stu-id="bbe83-143">Monitoring and Archiving each still require their own database stores.</span></span> <span data-ttu-id="bbe83-144">Exchange 2013 も実行している場合は、専用の SQL データベースではなく、Exchange でアーカイブデータを保持することができます。</span><span class="sxs-lookup"><span data-stu-id="bbe83-144">If you also run Exchange 2013, you can keep your Archiving data in Exchange, rather than in a dedicated SQL database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbe83-145">1つの仲介サーバー</span><span class="sxs-lookup"><span data-stu-id="bbe83-145">One Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="bbe83-146">フロントエンドサーバーと併置されている仲介サーバーは、プール内のすべてのフロントエンドサーバー上で実行され、プール内のユーザーに十分な容量を提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bbe83-146">Mediation Server collocated with Front End Server runs on every Front End Server in a pool, and should provide enough capacity for the users in the pool.</span></span> <span data-ttu-id="bbe83-147">スタンドアロンの仲介サーバーの場合は、このトピックで後述する「仲介サーバー」のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="bbe83-147">For stand-alone Mediation Server, see the “Mediation Server” section later in this topic.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbe83-148">Standard Edition server 1 台</span><span class="sxs-lookup"><span data-stu-id="bbe83-148">One Standard Edition server</span></span></p></td>
<td><p><span data-ttu-id="bbe83-149">Standard Edition サーバーを使用してユーザーをホストする場合は、常に2つのサーバーを使用し、 <a href="lync-server-2013-planning-for-high-availability-and-disaster-recovery.md">高可用性と障害回復の計画</a>に関する推奨事項を Lync Server 2013 で使用することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="bbe83-149">We strongly recommend that if you use Standard Edition servers to host users, you always use two servers, paired using the recommendations in <a href="lync-server-2013-planning-for-high-availability-and-disaster-recovery.md">Planning for high availability and disaster recovery in Lync Server 2013</a>.</span></span> <span data-ttu-id="bbe83-150">ペアの中の各サーバーは、最大 2,500 ユーザーをホストすることができ、フェールオーバー シナリオでは、1 台のサーバーに障害が発生した場合は残りの 1 台で 5,000 ユーザーをサポートできます。</span><span class="sxs-lookup"><span data-stu-id="bbe83-150">Each server in the pair can host up to 2,500 users, and if one server fails the remaining server can support 5,000 users in a failover scenario.</span></span></p>
<p><span data-ttu-id="bbe83-151">展開に大量のオーディオまたは動画トラフィックがある場合、サーバーあたりのユーザー数が 2,500 名を超えるとサーバー パフォーマンスが低下することがあります。</span><span class="sxs-lookup"><span data-stu-id="bbe83-151">If your deployment includes a significant amount of audio or video traffic, server performance may suffer with more than 2,500 users per server.</span></span> <span data-ttu-id="bbe83-152">この場合は、Standard Edition サーバーの追加または Lync Server Enterprise Edition への移行を検討してください。</span><span class="sxs-lookup"><span data-stu-id="bbe83-152">In this case, you should consider adding more Standard Edition servers or moving to Lync Server Enterprise Edition.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="front-end-server"></a><span data-ttu-id="bbe83-153">フロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="bbe83-153">Front End Server</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="bbe83-154">ストレッチプールは、このサーバーの役割ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="bbe83-154">Stretched pools are not supported for this server role.</span></span>



</div>

<span data-ttu-id="bbe83-155">フロントエンドプールでは、プール内のすべてのサーバーでハイパースレッディングが有効であり、サーバーハードウェアが [Lync server 2013 のサーバーハードウェアプラットフォーム](lync-server-2013-server-hardware-platforms.md)で推奨事項を満たしていることを前提として、すべての6660ユーザーに対して1つのフロントエンドサーバーを用意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bbe83-155">In a Front End pool, you should have one Front End Server for every 6,660 users homed in the pool, assuming that hyper-threading is enabled on all servers in the pool, and that the server hardware meets the recommendations in [Server hardware platforms for Lync Server 2013](lync-server-2013-server-hardware-platforms.md).</span></span> <span data-ttu-id="bbe83-156">1つのフロントエンドプール内のユーザーの最大数は8万で、そのプール内のすべてのサーバーでハイパースレッディングが有効になっていることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="bbe83-156">The maximum number of users in one Front End pool is 80,000, assuming that hyper-threading is enabled on all the servers in the pool.</span></span> <span data-ttu-id="bbe83-157">1つのサイトで8万を超えるユーザーがいる場合は、複数のフロントエンドプールを展開できます。</span><span class="sxs-lookup"><span data-stu-id="bbe83-157">If you have more than 80,000 users at a site, you can deploy more than one Front End pool.</span></span>

<span data-ttu-id="bbe83-158">フロントエンドプールのユーザー数を考慮している場合は、このフロントエンドプールに関連付けられている支社で、Survivable Branch アプライアンスと Survivable ブランチサーバーを含むユーザーを含めます。</span><span class="sxs-lookup"><span data-stu-id="bbe83-158">When you account for the number of users in a Front End pool, include the users homed on Survivable Branch Appliances and Survivable Branch Servers at branch offices that are associated with this Front End pool.</span></span>

<span data-ttu-id="bbe83-159">アクティブなサーバーが使用できなくなると、その接続はプール内にある他のサーバーに自動的に転送されます。</span><span class="sxs-lookup"><span data-stu-id="bbe83-159">When an active server is unavailable, its connections are transferred automatically to the other servers in the pool.</span></span> <span data-ttu-id="bbe83-160">たとえば、3万ユーザーと5台のフロントエンドサーバーがある場合、1つのサーバーを使用できない場合は、6000ユーザーの接続を他の4台のサーバーに移行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bbe83-160">For example, if you have 30,000 users and five Front End Servers, then if one server is unavailable, the connections of 6000 users need to be transferred to the other four servers.</span></span> <span data-ttu-id="bbe83-161">残りの4台のサーバーにはそれぞれ7500ユーザーが含まれています。これは推奨されるよりも大きい数値です。</span><span class="sxs-lookup"><span data-stu-id="bbe83-161">The remaining four servers will each have 7500 users, which is a larger number than recommended.</span></span>

<span data-ttu-id="bbe83-162">代わりに、3万ユーザー用に6つのフロントエンドサーバーを使い始めた後で、そのサーバーが利用できなくなった場合は、合計5000ユーザーが残りの5台のサーバーに移動されます。</span><span class="sxs-lookup"><span data-stu-id="bbe83-162">If instead you had started with six Front End Servers for your 30,000 users and subsequently one became unavailable, a total of 5000 users will be moved to the remaining five servers.</span></span> <span data-ttu-id="bbe83-163">これら5つのサーバーはそれぞれ、6000ユーザーをホストします。これらは、推奨される範囲内にあります。</span><span class="sxs-lookup"><span data-stu-id="bbe83-163">These five servers will each host 6000 users, which is in the recommended range.</span></span>

<span data-ttu-id="bbe83-164">フロントエンドプールのユーザーの最大数は8万です。</span><span class="sxs-lookup"><span data-stu-id="bbe83-164">The maximum number of users in a Front End pool is 80,000.</span></span> <span data-ttu-id="bbe83-165">プール内のフロントエンドサーバーの最大数は12です。</span><span class="sxs-lookup"><span data-stu-id="bbe83-165">The maximum number of Front End Servers in a pool is 12.</span></span>

<span data-ttu-id="bbe83-166">8万ユーザーを含むフロントエンドプールの場合、パフォーマンスを向上させるには、 [Lync Server 2013 のユーザーモデル](lync-server-2013-user-models.md)に従った通常の展開で、12個のフロントエンドサーバーで十分です。</span><span class="sxs-lookup"><span data-stu-id="bbe83-166">For a Front End pool with 80,000 users, twelve Front End Servers is sufficient for performance, in typical deployments that follow the [User models in Lync Server 2013](lync-server-2013-user-models.md).</span></span> <span data-ttu-id="bbe83-167">障害回復フェールオーバーをサポートするように設計された展開では、2つのペアのフロントエンドプールのそれぞれに最大4万ユーザーをホストできます。各プールには、両方のプールのユーザーに対応するための十分なフロントエンドサーバーがあることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="bbe83-167">Deployments designed to support disaster recovery failover assume that a maximum of 40,000 users can be hosted in each of two paired Front End pools, in which each pool has enough Front End Servers to accommodate the users in both pools should one pool need to be failed over to the other.</span></span>

<span data-ttu-id="bbe83-168">特定のフロントエンドプールによる良好なパフォーマンスでサポートされるユーザーの数は、次のような理由により、これらの数値とは異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="bbe83-168">The number of users supported with good performance by a particular Front End pool may differ from these numbers for the following reasons:</span></span>

  - <span data-ttu-id="bbe83-169">フロントエンドサーバーのハードウェアは、 [Lync server 2013 のサーバーハードウェアプラットフォーム](lync-server-2013-server-hardware-platforms.md)の推奨事項を満たしていません。</span><span class="sxs-lookup"><span data-stu-id="bbe83-169">The hardware for your Front End Servers does not meet the recommendations in [Server hardware platforms for Lync Server 2013](lync-server-2013-server-hardware-platforms.md).</span></span>

  - <span data-ttu-id="bbe83-170">組織の使用状況は、多くの会議トラフィックなど、ユーザーモデルとは大きく異なります。</span><span class="sxs-lookup"><span data-stu-id="bbe83-170">Your organization’s usage differs significantly from the user models, such as significantly more conferencing traffic.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="bbe83-171">Lync Server 2013 では、バックエンドサーバーでホストされていた Lync Server 2010 ではなく、フロントエンドサーバーでプレゼンスデータベースがホストされるようになりました。</span><span class="sxs-lookup"><span data-stu-id="bbe83-171">In Lync Server 2013, the presence databases are now hosted on Front End Servers, unlike in Lync Server 2010 where they were hosted on the Back End Server.</span></span> <span data-ttu-id="bbe83-172">つまり、フロントエンドサーバーによってホストされているユーザーの数に関係なく、フロントエンドサーバーのディスクパフォーマンスと容量が、このセクションで説明した推奨事項、および <A href="lync-server-2013-server-hardware-platforms.md">Lync server 2013 のサーバーハードウェアプラットフォーム</A>では危険ではないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="bbe83-172">This means that the disk performance and capacity of your Front End Servers should not be compromised from the recommendations listed earlier in this section and in <A href="lync-server-2013-server-hardware-platforms.md">Server hardware platforms for Lync Server 2013</A>, regardless of the number of users hosted by your Front End Servers.</span></span>



</div>

<span data-ttu-id="bbe83-173">次の表は、 [Lync Server 2013 のユーザー](lync-server-2013-user-models.md)モデルで定義されているユーザーモデルに基づいて、IM とプレゼンスの平均帯域幅を示しています。</span><span class="sxs-lookup"><span data-stu-id="bbe83-173">The following table shows the average bandwidth for IM and presence, given the user model, as defined in [User models in Lync Server 2013](lync-server-2013-user-models.md).</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bbe83-174">ユーザー単位の平均帯域幅</span><span class="sxs-lookup"><span data-stu-id="bbe83-174">Average bandwidth per user</span></span></th>
<th><span data-ttu-id="bbe83-175">6660ユーザーとのフロントエンドサーバーあたりの帯域幅要件</span><span class="sxs-lookup"><span data-stu-id="bbe83-175">Bandwidth requirements per Front End Server with 6,660 users</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bbe83-176">1.3 Kpbs</span><span class="sxs-lookup"><span data-stu-id="bbe83-176">1.3 Kpbs</span></span></p></td>
<td><p><span data-ttu-id="bbe83-177">13 Mbps</span><span class="sxs-lookup"><span data-stu-id="bbe83-177">13 Mbps</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="bbe83-178">フロントエンドサーバー上の併置された A/V 会議および仲介サーバー機能のメディアパフォーマンスを向上させるには、フロントエンドサーバー上のネットワークアダプターで受信側スケーリング (RSS) を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="bbe83-178">To improve the media performance of the co-located A/V Conferencing and Mediation Server functionality on your Front End Servers, you should enable receive-side scaling (RSS) on the network adapters on your Front End Servers.</span></span> <span data-ttu-id="bbe83-179">RSS は、着信パケットがサーバーの複数のプロセッサによって平行して処理されるのを可能にします。</span><span class="sxs-lookup"><span data-stu-id="bbe83-179">RSS enables incoming packets to be handled in parallel by multiple processors on the server.</span></span> <span data-ttu-id="bbe83-180">詳細については、「Windows Server 2008 の受信側スケーリングの拡張機能」を参照してください <A href="https://go.microsoft.com/fwlink/p/?linkid=268731">https://go.microsoft.com/fwlink/p/?linkId=268731</A> 。</span><span class="sxs-lookup"><span data-stu-id="bbe83-180">For details, see "Receive-Side Scaling Enhancements in Windows Server 2008" at <A href="https://go.microsoft.com/fwlink/p/?linkid=268731">https://go.microsoft.com/fwlink/p/?linkId=268731</A>.</span></span> <span data-ttu-id="bbe83-181">RSS を有効にする方法の詳細については、ネットワーク アダプターのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="bbe83-181">For details about how to enable RSS, see your network adapter documentation.</span></span>



</div>

</div>

<div>

## <a name="conferencing-maximums"></a><span data-ttu-id="bbe83-182">最大会議数</span><span class="sxs-lookup"><span data-stu-id="bbe83-182">Conferencing Maximums</span></span>

<span data-ttu-id="bbe83-183">プール内のユーザーの5% が1つの会議に参加している可能性がある場合、8万ユーザーのプールは、一度に1人の会議で4000ユーザーを持つことがあります。</span><span class="sxs-lookup"><span data-stu-id="bbe83-183">Given the user model that 5% of users in a pool may be in a conference at any one time, a pool of 80,000 users could have about 4,000 users in conferences at one time.</span></span> <span data-ttu-id="bbe83-184">これらの会議は、メディアが混在していることを前提としています (一部の IM のみ、音声での IM、一部の音声/ビデオなど)、参加者の数が含まれます。</span><span class="sxs-lookup"><span data-stu-id="bbe83-184">These conferences are expected to be a mix of media (some IM-only, some IM with audio, some audio/video, for example) and number of participants.</span></span> <span data-ttu-id="bbe83-185">許可されている電話会議の実際の数には制限はありません。実際の使用状況によって実際のパフォーマンスが決まります。</span><span class="sxs-lookup"><span data-stu-id="bbe83-185">There is no hard limit for the actual number of conferences allowed, and actual usage determines the actual performance.</span></span> <span data-ttu-id="bbe83-186">たとえば、組織にユーザーモデルで想定されているよりも多くの混在モードの会議がある場合は、このドキュメントの推奨事項よりも多くのフロントエンドサーバーまたは A/V の会議サーバーを展開する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="bbe83-186">For example, if your organization has many more mixed-mode conferences than are assumed in the user model, you might need to deploy more Front End Servers or A/V Conferencing Servers than the recommendations in this document.</span></span> <span data-ttu-id="bbe83-187">ユーザーモデルの前提条件の詳細については、「 [Lync Server 2013 のユーザーモデル](lync-server-2013-user-models.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bbe83-187">For details about the assumptions in the user model, see [User models in Lync Server 2013](lync-server-2013-user-models.md).</span></span>

<span data-ttu-id="bbe83-188">定期的な Lync Server 2013 フロントエンドプールによってホストされる最大サポートされている会議サイズであり、ユーザーは、250の参加者でもあります。</span><span class="sxs-lookup"><span data-stu-id="bbe83-188">The maximum supported conference size hosted by a regular Lync Server 2013 Front End pool which also hosts users is 250 participants.</span></span> <span data-ttu-id="bbe83-189">250 ユーザーが参加する会議が行われている場合、プールは同時に他の会議もサポートします (同時に行われる会議にプール ユーザーのうちの 5% が参加している場合など)。</span><span class="sxs-lookup"><span data-stu-id="bbe83-189">While a 250-user conference is happening, the pool still supports other conferences as well, such that a total of 5% of pool users are in concurrent conferences.</span></span> <span data-ttu-id="bbe83-190">たとえば、12台のフロントエンドサーバーと8万ユーザーのプールでは、250ユーザーの会議が行われている間、Lync Server は小規模の会議に参加している3750他のユーザーをサポートします。</span><span class="sxs-lookup"><span data-stu-id="bbe83-190">For example, in a pool of twelve Front End Servers and 80,000 users, while the 250-user conference is happening, Lync Server supports 3,750 other users participating in smaller conferences.</span></span>

<span data-ttu-id="bbe83-191">フロントエンドプールまたは Standard Edition サーバーに所属しているユーザー数にかかわらず、Lync Server は、250ユーザー会議をホストしている同一のプールまたはサーバー上の小さい会議に参加している、少なくとも125の他のユーザーをサポートします。</span><span class="sxs-lookup"><span data-stu-id="bbe83-191">Regardless of the number of users homed on the Front End pool or Standard Edition server, Lync Server supports a minimum of 125 other users participating in smaller conferences on the same pool or server which is hosting a 250-user conference.</span></span>

<span data-ttu-id="bbe83-192">250と1000のユーザーの間で会議を有効にするには、個別のフロントエンドプールをセットアップして、会議を主催することができます。</span><span class="sxs-lookup"><span data-stu-id="bbe83-192">To enable conferences with between 250 and 1000 users, you can set up a separate Front End pool just to host those conferences.</span></span> <span data-ttu-id="bbe83-193">このフロントエンドプールでは、ユーザーはホストされません。</span><span class="sxs-lookup"><span data-stu-id="bbe83-193">This Front End pool will not host any users.</span></span> <span data-ttu-id="bbe83-194">詳細については、「 [Lync Server 2013 を使用した大規模な会議のサポート](lync-server-2013-supporting-large-meetings.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bbe83-194">For details, see [Supporting large meetings using Lync Server 2013](lync-server-2013-supporting-large-meetings.md).</span></span>

<span data-ttu-id="bbe83-195">組織で、ユーザーモデルで想定されているよりも多くの混在モードの会議がある場合は、このドキュメントの推奨事項よりも多くのフロントエンドサーバーを展開する必要がある場合があります (上限は 12 FEs)。</span><span class="sxs-lookup"><span data-stu-id="bbe83-195">If your organization has many more mixed-mode conferences than are assumed in the user model, you might need to deploy more Front End Servers than the recommendations in this document (up to a limit of 12 FEs).</span></span> <span data-ttu-id="bbe83-196">ユーザーモデルの前提条件の詳細については、「 [Lync Server 2013 のユーザーモデル](lync-server-2013-user-models.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bbe83-196">For details about the assumptions in the user model, see [User models in Lync Server 2013](lync-server-2013-user-models.md).</span></span>

</div>

<div>

## <a name="edge-server"></a><span data-ttu-id="bbe83-197">エッジ サーバー</span><span class="sxs-lookup"><span data-stu-id="bbe83-197">Edge Server</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="bbe83-198">ストレッチプールは、このサーバーの役割ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="bbe83-198">Stretched pools are not supported for this server role.</span></span>



</div>

<span data-ttu-id="bbe83-199">サイトに同時にアクセスするすべての12000リモートユーザーに対して、1つのエッジサーバーを展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bbe83-199">You should deploy one Edge Server for every 12,000 remote users who will access a site concurrently.</span></span> <span data-ttu-id="bbe83-200">少なくとも、高可用性を実現するには、2台のエッジサーバーをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="bbe83-200">At a minimum we recommend two Edge Servers for high availability.</span></span> <span data-ttu-id="bbe83-201">これらの推奨事項は、エッジサーバーのハードウェアが [Lync server 2013 のサーバーハードウェアプラットフォーム](lync-server-2013-server-hardware-platforms.md)の推奨事項を満たしていることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="bbe83-201">These recommendations assume that the hardware for your Edge Servers meets the recommendations in [Server hardware platforms for Lync Server 2013](lync-server-2013-server-hardware-platforms.md).</span></span>

<span data-ttu-id="bbe83-202">エッジサーバーのユーザー数を考慮する場合は、このサイトのフロントエンドプールに関連付けられている支社で、Survivable Branch アプライアンスと Survivable ブランチサーバーを含むユーザーを含めます。</span><span class="sxs-lookup"><span data-stu-id="bbe83-202">When you account for the number of users for the Edge Servers, include the users homed on Survivable Branch Appliances and Survivable Branch Servers at branch offices that are associated with a Front End pool at this site.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="bbe83-203">エッジサーバー上の A/V 会議エッジサービスのパフォーマンスを向上させるには、エッジサーバーのネットワークアダプターで受信側スケーリング (RSS) を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="bbe83-203">To improve the performance of the A/V Conferencing Edge service on your Edge Servers, you should enable receive-side scaling (RSS) on the network adapters on your Edge Servers.</span></span> <span data-ttu-id="bbe83-204">RSS は、着信パケットがサーバーの複数のプロセッサによって平行して処理されるのを可能にします。</span><span class="sxs-lookup"><span data-stu-id="bbe83-204">RSS enables incoming packets to be handled in parallel by multiple processors on the server.</span></span> <span data-ttu-id="bbe83-205">詳細については、「Windows Server 2008 の受信側スケーリングの拡張機能」を参照してください <A href="https://go.microsoft.com/fwlink/p/?linkid=268731">https://go.microsoft.com/fwlink/p/?linkId=268731</A> 。</span><span class="sxs-lookup"><span data-stu-id="bbe83-205">For details, see "Receive-Side Scaling Enhancements in Windows Server 2008" at <A href="https://go.microsoft.com/fwlink/p/?linkid=268731">https://go.microsoft.com/fwlink/p/?linkId=268731</A>.</span></span> <span data-ttu-id="bbe83-206">RSS を有効にする方法の詳細については、ネットワーク アダプターのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="bbe83-206">For details about how to enable RSS, see your network adapter documentation.</span></span>



</div>

</div>

<div>

## <a name="director"></a><span data-ttu-id="bbe83-207">ディレクター</span><span class="sxs-lookup"><span data-stu-id="bbe83-207">Director</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="bbe83-208">ストレッチプールは、このサーバーの役割ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="bbe83-208">Stretched pools are not supported for this server role.</span></span>



</div>

<span data-ttu-id="bbe83-209">ディレクターサーバーの役割を展開する場合は、サイトに同時にアクセスするすべての12000リモートユーザーに対してディレクターを1つ展開することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="bbe83-209">If you deploy the Director server role we recommend that you deploy one Director for every 12,000 remote users who will access a site concurrently.</span></span> <span data-ttu-id="bbe83-210">少なくとも、高可用性を実現するために2つのディレクターをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="bbe83-210">At a minimum we recommend two Directors for high availability.</span></span> <span data-ttu-id="bbe83-211">これらの推奨事項は、エッジサーバーのハードウェアが [Lync server 2013 のサーバーハードウェアプラットフォーム](lync-server-2013-server-hardware-platforms.md)の推奨事項を満たしていることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="bbe83-211">These recommendations assume that the hardware for your Edge Servers meets the recommendations in [Server hardware platforms for Lync Server 2013](lync-server-2013-server-hardware-platforms.md).</span></span>

<span data-ttu-id="bbe83-212">ディレクターのユーザー数を考慮する場合は、このサイトのフロントエンドプールに関連付けられている支社で、Survivable Branch アプライアンスと Survivable ブランチサーバーを使用しているユーザーを含めます。</span><span class="sxs-lookup"><span data-stu-id="bbe83-212">When you account for the number of users for the Directors, include the users homed on Survivable Branch Appliances and Survivable Branch Servers at branch offices that are associated with a Front End pool at this site.</span></span>

</div>

<div>

## <a name="mediation-server"></a><span data-ttu-id="bbe83-213">仲介サーバー</span><span class="sxs-lookup"><span data-stu-id="bbe83-213">Mediation Server</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="bbe83-214">ストレッチプールは、このサーバーの役割ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="bbe83-214">Stretched pools are not supported for this server role.</span></span>



</div>

<span data-ttu-id="bbe83-215">フロントエンドサーバーで仲介サーバーを使用している場合、仲介サーバーはプール内の各フロントエンドサーバー上で実行され、プール内のユーザーに十分な容量を提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bbe83-215">If you collocate Mediation Server with Front End Server, Mediation Server runs on every Front End Server in the pool, and should provide enough capacity for the users in the pool.</span></span>

<span data-ttu-id="bbe83-216">スタンドアロンの仲介サーバープールを展開する場合は、仲介サーバーに使用されているハードウェア、使用している VoIP ユーザーの数、各仲介サーバープールが制御するゲートウェイピアの数、それらのゲートウェイ経由でのビジーな時間トラフィック、および仲介サーバーをバイパスするメディアでの通話のパーセンテージなど、さまざまな要因によって展開される仲介サーバーの</span><span class="sxs-lookup"><span data-stu-id="bbe83-216">If you deploy a stand-alone Mediation Server pool, then how many Mediation Servers to deploy depends on many factors, including the hardware used for Mediation Server, the number of VoIP users you have, the number of gateway peers that each Mediation Server pool controls, the busy hour traffic through those gateways, and the percentage of calls with media that bypasses the Mediation Server.</span></span>

<span data-ttu-id="bbe83-217">次の表では、仲介サーバーのハードウェアが [Lync server 2013 のサーバーハードウェアプラットフォーム](lync-server-2013-server-hardware-platforms.md) の要件を満たしていて、ハイパースレッディングが有効になっていることを前提として、仲介サーバーが処理できる同時通話数に関するガイドラインを提供します。</span><span class="sxs-lookup"><span data-stu-id="bbe83-217">The following tables provide a guideline for how many concurrent calls a Mediation Server can handle, assuming that the hardware for the Mediation Servers meets the requirements in [Server hardware platforms for Lync Server 2013](lync-server-2013-server-hardware-platforms.md) and that hyper-threading is enabled.</span></span> <span data-ttu-id="bbe83-218">仲介サーバーのスケーラビリティの詳細については、「 [Lync server 2013 の音声使用量とトラフィックの見積もり](lync-server-2013-estimating-voice-usage-and-traffic.md) 」および「 [lync server 2013 での仲介サーバーの展開ガイドライン](lync-server-2013-deployment-guidelines-for-mediation-server.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bbe83-218">For details about Mediation Server scalability, see [Estimating voice usage and traffic for Lync Server 2013](lync-server-2013-estimating-voice-usage-and-traffic.md) and [Deployment guidelines for Mediation Server in Lync Server 2013](lync-server-2013-deployment-guidelines-for-mediation-server.md).</span></span>

<span data-ttu-id="bbe83-219">次の表では、 [Lync Server 2013 のユーザーモデル](lync-server-2013-user-models.md)での使用状況を想定しています。</span><span class="sxs-lookup"><span data-stu-id="bbe83-219">All the following tables assume usage as summarized in [User models in Lync Server 2013](lync-server-2013-user-models.md).</span></span>

### <a name="stand-alone-mediation-server-capacity-70-internal-users-30-external-users-with-non-bypass-call-capacity-media-transcoding-performed-by-mediation-server"></a><span data-ttu-id="bbe83-220">スタンドアロンの仲介サーバー容量: 70% 内部ユーザー、非バイパス通話容量を持つ外部ユーザー 30% (仲介サーバーによって実行されるメディアのトランスコード)</span><span class="sxs-lookup"><span data-stu-id="bbe83-220">Stand-alone Mediation Server Capacity: 70% Internal Users, 30% External users with non-bypass call capacity (media transcoding performed by Mediation Server)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bbe83-221">サーバー ハードウェア</span><span class="sxs-lookup"><span data-stu-id="bbe83-221">Server hardware</span></span></th>
<th><span data-ttu-id="bbe83-222">最大通話数</span><span class="sxs-lookup"><span data-stu-id="bbe83-222">Maximum number of calls</span></span></th>
<th><span data-ttu-id="bbe83-223">T1 回線の最大数</span><span class="sxs-lookup"><span data-stu-id="bbe83-223">Maximum number of T1 lines</span></span></th>
<th><span data-ttu-id="bbe83-224">E1 回線の最大数</span><span class="sxs-lookup"><span data-stu-id="bbe83-224">Maximum number of E1 lines</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bbe83-225">デュアル プロセッサ、6 コア、2.26 GHz ハイパースレッディング CPU (<strong>ハイパースレッディング無効</strong>)、32 GB メモリ、デュアルポート ネットワーク アダプター カード 1 つ</span><span class="sxs-lookup"><span data-stu-id="bbe83-225">Dual processor, hex core, 2.26 GHz hyper-threaded CPU <strong>with hyper-threading disabled</strong>, with 32 GB memory and one dual-port network adapter card.</span></span></p></td>
<td><p><span data-ttu-id="bbe83-226">1100</span><span class="sxs-lookup"><span data-stu-id="bbe83-226">1100</span></span></p></td>
<td><p><span data-ttu-id="bbe83-227">46</span><span class="sxs-lookup"><span data-stu-id="bbe83-227">46</span></span></p></td>
<td><p><span data-ttu-id="bbe83-228">35</span><span class="sxs-lookup"><span data-stu-id="bbe83-228">35</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbe83-229">デュアル プロセッサ、6 コア、2.26 GHz ハイパースレッディング CPU、32 GB メモリ、デュアルポート ネットワーク アダプター カード 1 つ</span><span class="sxs-lookup"><span data-stu-id="bbe83-229">Dual processor, hex core, 2.26 GHz hyper-threaded CPU, with 32 GB memory and one dual-port network adapter card.</span></span></p></td>
<td><p><span data-ttu-id="bbe83-230">1500</span><span class="sxs-lookup"><span data-stu-id="bbe83-230">1500</span></span></p></td>
<td><p><span data-ttu-id="bbe83-231">63</span><span class="sxs-lookup"><span data-stu-id="bbe83-231">63</span></span></p></td>
<td><p><span data-ttu-id="bbe83-232">47</span><span class="sxs-lookup"><span data-stu-id="bbe83-232">47</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="bbe83-233">32 GB のメモリを搭載したサーバーはパフォーマンステストに使用されていますが、16 GB のメモリを持つサーバーは、スタンドアロンの仲介サーバーでサポートされており、この表に示すパフォーマンスを提供するのに十分な方法です。</span><span class="sxs-lookup"><span data-stu-id="bbe83-233">Although servers with 32 GB of memory were used for performance testing, servers with 16 GB of memory are supported for stand-alone Mediation Server, and are sufficient to provide the performance shown in this table.</span></span>



</div>

### <a name="mediation-server-capacity-mediation-server-collocated-with-front-end-server-70-internal-users-30-external-users-non-bypass-call-capacity-media-processing-performed-by-mediation-server"></a><span data-ttu-id="bbe83-234">仲介サーバーの容量 (フロントエンドサーバーと連携している仲介サーバー) 70% 内部ユーザー、30% の外部ユーザー、非バイパス通話キャパシティ (仲介サーバーによって実行されるメディア処理)</span><span class="sxs-lookup"><span data-stu-id="bbe83-234">Mediation Server Capacity (Mediation Server Collocated with Front End Server) 70% Internal Users, 30% External Users, Non-Bypass Call Capacity (Media Processing Performed by Mediation Server)</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bbe83-235">サーバー ハードウェア</span><span class="sxs-lookup"><span data-stu-id="bbe83-235">Server hardware</span></span></th>
<th><span data-ttu-id="bbe83-236">最大通話数</span><span class="sxs-lookup"><span data-stu-id="bbe83-236">Maximum number of calls</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bbe83-237">デュアル プロセッサ、6 コア、2.26 GHz ハイパースレッディング CPU、32 GB メモリ、1 GB ネットワーク アダプター カード × 2</span><span class="sxs-lookup"><span data-stu-id="bbe83-237">Dual processor, hex core, 2.26 GHz hyper-threaded CPU, with 32 GB memory and 2 1GB network adapter cards.</span></span></p></td>
<td><p><span data-ttu-id="bbe83-238">150</span><span class="sxs-lookup"><span data-stu-id="bbe83-238">150</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="bbe83-239">この数値は、スタンドアロンの仲介サーバーの数値よりもかなり小さいです。フロントエンドサーバーでは、ホームに必要な6600ユーザーのその他の機能や機能を処理する必要があります。また、音声通話に必要なトランスコードを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bbe83-239">This number is much smaller than the numbers for the stand-alone Mediation Server because the Front End Server has to handle other features and functions for the 6600 users homed on it, in addition to the transcoding needed for voice calls.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="bbe83-240">仲介サーバーのパフォーマンスを向上させるには、仲介サーバーのネットワークアダプターで受信側スケーリング (RSS) を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="bbe83-240">To improve the performance of the Mediation Server, you should enable receive-side scaling (RSS) on the network adapters on your Mediation Servers.</span></span> <span data-ttu-id="bbe83-241">RSS は、着信パケットがサーバーの複数のプロセッサによって平行して処理されるのを可能にします。</span><span class="sxs-lookup"><span data-stu-id="bbe83-241">RSS enables incoming packets to be handled in parallel by multiple processors on the server.</span></span> <span data-ttu-id="bbe83-242">詳細については、「Windows Server 2008 の受信側スケーリングの拡張機能」を参照してください <A href="https://go.microsoft.com/fwlink/p/?linkid=268731">https://go.microsoft.com/fwlink/p/?linkId=268731</A> 。</span><span class="sxs-lookup"><span data-stu-id="bbe83-242">For details, see "Receive-Side Scaling Enhancements in Windows Server 2008" at <A href="https://go.microsoft.com/fwlink/p/?linkid=268731">https://go.microsoft.com/fwlink/p/?linkId=268731</A>.</span></span> <span data-ttu-id="bbe83-243">RSS を有効にする方法の詳細については、ネットワーク アダプターのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="bbe83-243">For details about how to enable RSS, see your network adapter documentation.</span></span>



</div>

</div>

<div>

## <a name="back-end-server"></a><span data-ttu-id="bbe83-244">バック エンド サーバー</span><span class="sxs-lookup"><span data-stu-id="bbe83-244">Back End Server</span></span>

<span data-ttu-id="bbe83-245">Lync Server 2013 では、プレゼンスデータベースはバックエンドサーバーではなく、フロントエンドサーバー上に配置されています。</span><span class="sxs-lookup"><span data-stu-id="bbe83-245">In Lync Server 2013, the presence databases are located on the Front End Servers instead of the Back End Server.</span></span> <span data-ttu-id="bbe83-246">このため、Lync Server 2013 のバックエンドサーバーごとに、フロントエンドサーバーのハードウェア要件と同等の要件が大幅に簡素化されています。</span><span class="sxs-lookup"><span data-stu-id="bbe83-246">This has resulted in a much simpler requirement for each Back End Server in Lync Server 2013, equivalent to the hardware requirement for the Front End Server.</span></span> <span data-ttu-id="bbe83-247">この点2010について、バックエンドサーバーは、25ディスクでより高いグレードのサーバーである必要がありました。</span><span class="sxs-lookup"><span data-stu-id="bbe83-247">Contrast this to Lync Server 2010, where the Back End Server was required to be a much higher grade server with 25 disks.</span></span> <span data-ttu-id="bbe83-248">ただし、バックエンドサーバーの作業負荷は依然としているため、このセクションで説明したハードウェア推奨事項、および [Lync server 2013 のサーバーハードウェアプラットフォーム](lync-server-2013-server-hardware-platforms.md)には合格しない必要があります。</span><span class="sxs-lookup"><span data-stu-id="bbe83-248">However, the workload of Back End Servers is still such that you should not fail to meet the hardware recommendations listed earlier in this section and in [Server hardware platforms for Lync Server 2013](lync-server-2013-server-hardware-platforms.md).</span></span>

<span data-ttu-id="bbe83-249">バックエンドサーバーの高可用性を実現するには、サーバーのミラーリングを展開することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="bbe83-249">To provide high availability of your Back End Server, we recommend deploying server mirroring.</span></span> <span data-ttu-id="bbe83-250">詳細については、「 [Lync Server 2013 のバックエンドサーバーの高可用性](lync-server-2013-back-end-server-high-availability.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bbe83-250">For more information, see [Back End Server high availability in Lync Server 2013](lync-server-2013-back-end-server-high-availability.md).</span></span>

</div>

<div>

## <a name="monitoring-and-archiving"></a><span data-ttu-id="bbe83-251">監視およびアーカイブ</span><span class="sxs-lookup"><span data-stu-id="bbe83-251">Monitoring and Archiving</span></span>

<span data-ttu-id="bbe83-252">Lync Server 2013 では、監視またはアーカイブを展開した場合、これらのサービスのフロントエンド機能は、個別のサーバーの役割ではなく、フロントエンドサーバー上で実行されます。</span><span class="sxs-lookup"><span data-stu-id="bbe83-252">In Lync Server 2013, if you deploy Monitoring or Archiving, the front end functionality of these services runs on the Front End Servers, instead of on separate server roles.</span></span> <span data-ttu-id="bbe83-253">監視とアーカイブの各機能は、バックエンドストアとは別に、独自のデータベースストアを使用します。</span><span class="sxs-lookup"><span data-stu-id="bbe83-253">Monitoring and Archiving each still use their own database store, separate from the Back End store.</span></span> <span data-ttu-id="bbe83-254">また、Exchange 2013 が展開されている場合は、専用の SQL ストアではなく、インスタントメッセージのアーカイブデータを Exchange に保存することもできます。</span><span class="sxs-lookup"><span data-stu-id="bbe83-254">Alternatively, if you have Exchange 2013 deployed, you can store instant message Archiving data in Exchange instead of in a dedicated SQL store.</span></span>

<span data-ttu-id="bbe83-255">次の表は、監視およびアーカイブのデータに必要な、ユーザーごとの 1 日あたりのデータベース記憶域 (概算) を示します。</span><span class="sxs-lookup"><span data-stu-id="bbe83-255">The following table indicates approximately how much database storage is required per user per day for Monitoring and Archiving data.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="bbe83-256"><strong>CDR (監視)</strong></span><span class="sxs-lookup"><span data-stu-id="bbe83-256"><strong>CDR (Monitoring)</strong></span></span></p></td>
<td><p><span data-ttu-id="bbe83-257"><strong>QoE (監視)</strong></span><span class="sxs-lookup"><span data-stu-id="bbe83-257"><strong>QoE (Monitoring)</strong></span></span></p></td>
<td><p><span data-ttu-id="bbe83-258"><strong>アーカイブ</strong></span><span class="sxs-lookup"><span data-stu-id="bbe83-258"><strong>Archiving</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbe83-259">ユーザーごとに 1 日に必要なディスク容量</span><span class="sxs-lookup"><span data-stu-id="bbe83-259">Disk space required per user per day</span></span></p></td>
<td><p><span data-ttu-id="bbe83-260">49 KB</span><span class="sxs-lookup"><span data-stu-id="bbe83-260">49 KB</span></span></p></td>
<td><p><span data-ttu-id="bbe83-261">28 KB</span><span class="sxs-lookup"><span data-stu-id="bbe83-261">28 KB</span></span></p></td>
<td><p><span data-ttu-id="bbe83-262">57 KB</span><span class="sxs-lookup"><span data-stu-id="bbe83-262">57 KB</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bbe83-263">Microsoft では、パフォーマンス テストの際に、次の表に示すハードウェアを監視およびアーカイブ用のデータベース サーバーとして使用しました。</span><span class="sxs-lookup"><span data-stu-id="bbe83-263">Microsoft used the hardware in the following table for the database server for Monitoring and Archiving during its performance testing.</span></span> <span data-ttu-id="bbe83-264">テストでは、2つのフロントエンドプールのデータが収集されます。各データには8万ユーザーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="bbe83-264">The testing collected the data of two Front End pools, each of which contained 80,000 users.</span></span>

### <a name="hardware-used-in-monitoring-and-archiving-performance-testing"></a><span data-ttu-id="bbe83-265">監視およびアーカイブのパフォーマンス テストで使用したハードウェア</span><span class="sxs-lookup"><span data-stu-id="bbe83-265">Hardware Used in Monitoring and Archiving Performance Testing</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bbe83-266">ハードウェア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="bbe83-266">Hardware component</span></span></th>
<th><span data-ttu-id="bbe83-267">推奨</span><span class="sxs-lookup"><span data-stu-id="bbe83-267">Recommended</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bbe83-268">CPU</span><span class="sxs-lookup"><span data-stu-id="bbe83-268">CPU</span></span></p></td>
<td><p><span data-ttu-id="bbe83-269">64 ビット デュアル プロセッサ、6 コア、2.26 GHz 以上</span><span class="sxs-lookup"><span data-stu-id="bbe83-269">64-bit dual processor, hex-core, 2.26 gigahertz (GHz) or higher</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbe83-270">メモリ</span><span class="sxs-lookup"><span data-stu-id="bbe83-270">Memory</span></span></p></td>
<td><p><span data-ttu-id="bbe83-271">48 ギガバイト (GB)</span><span class="sxs-lookup"><span data-stu-id="bbe83-271">48 gigabytes (GB)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbe83-272">ディスク</span><span class="sxs-lookup"><span data-stu-id="bbe83-272">Disk</span></span></p></td>
<td><p><span data-ttu-id="bbe83-273">次の構成を持つ 10,000 RPM のハード ディスク ドライブ × 25 (各ディスクのサイズは 300 GB)</span><span class="sxs-lookup"><span data-stu-id="bbe83-273">25 10,000-RPM hard disk drives with 300 GB on each disk, with the following configuration</span></span></p>
<h3 id="section-3"> </h3>
<div>
<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bbe83-274"><strong>ドライブ</strong></span><span class="sxs-lookup"><span data-stu-id="bbe83-274"><strong>Drive</strong></span></span></p></td>
<td><p><span data-ttu-id="bbe83-275"><strong>RAID 構成</strong></span><span class="sxs-lookup"><span data-stu-id="bbe83-275"><strong>RAID Configuration</strong></span></span></p></td>
<td><p><span data-ttu-id="bbe83-276"><strong>ディスク数</strong></span><span class="sxs-lookup"><span data-stu-id="bbe83-276"><strong>Number of disks</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbe83-277">CDR、QoE、およびアーカイブ データベースのデータ ファイル (単一のドライブ上)</span><span class="sxs-lookup"><span data-stu-id="bbe83-277">CDR, QoE, and Archiving database data files, on a single drive</span></span></p></td>
<td><p><span data-ttu-id="bbe83-278">1+0</span><span class="sxs-lookup"><span data-stu-id="bbe83-278">1+0</span></span></p></td>
<td><p><span data-ttu-id="bbe83-279">16</span><span class="sxs-lookup"><span data-stu-id="bbe83-279">16</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbe83-280">CDR データベースのログ ファイル</span><span class="sxs-lookup"><span data-stu-id="bbe83-280">CDR database log file</span></span></p></td>
<td><p><span data-ttu-id="bbe83-281">1</span><span class="sxs-lookup"><span data-stu-id="bbe83-281">1</span></span></p></td>
<td><p><span data-ttu-id="bbe83-282">2</span><span class="sxs-lookup"><span data-stu-id="bbe83-282">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbe83-283">QoE データベースのログ ファイル</span><span class="sxs-lookup"><span data-stu-id="bbe83-283">QoE database log file</span></span></p></td>
<td><p><span data-ttu-id="bbe83-284">1</span><span class="sxs-lookup"><span data-stu-id="bbe83-284">1</span></span></p></td>
<td><p><span data-ttu-id="bbe83-285">2</span><span class="sxs-lookup"><span data-stu-id="bbe83-285">2</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbe83-286">アーカイブ データベースのログ ファイル</span><span class="sxs-lookup"><span data-stu-id="bbe83-286">Archiving database log file</span></span></p></td>
<td><p><span data-ttu-id="bbe83-287">1</span><span class="sxs-lookup"><span data-stu-id="bbe83-287">1</span></span></p></td>
<td><p><span data-ttu-id="bbe83-288">2</span><span class="sxs-lookup"><span data-stu-id="bbe83-288">2</span></span></p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbe83-289">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="bbe83-289">Network</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="bbe83-290">1 Gbps 以上のデュアルポート ネットワーク アダプター 1 つ (2 つを推奨。その場合は 1 つの MAC アドレスと 1 つの IP アドレスのチーミングが必要)</span><span class="sxs-lookup"><span data-stu-id="bbe83-290">1 dual-port network adapter, 1 Gbps or higher (2 recommended, which requires teaming with a single MAC address and single IP address)</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="bbe83-291">このセクション中</span><span class="sxs-lookup"><span data-stu-id="bbe83-291">In This Section</span></span>

  - [<span data-ttu-id="bbe83-292">Lync Server 2013 の音声の利用状況とトラフィックの予測</span><span class="sxs-lookup"><span data-stu-id="bbe83-292">Estimating voice usage and traffic for Lync Server 2013</span></span>](lync-server-2013-estimating-voice-usage-and-traffic.md)

  - [<span data-ttu-id="bbe83-293">Lync Server 2013 での仲介サーバーの展開ガイドライン</span><span class="sxs-lookup"><span data-stu-id="bbe83-293">Deployment guidelines for Mediation Server in Lync Server 2013</span></span>](lync-server-2013-deployment-guidelines-for-mediation-server.md)

<span data-ttu-id="bbe83-294"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bbe83-294"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

