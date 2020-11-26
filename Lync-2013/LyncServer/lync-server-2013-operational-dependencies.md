---
title: 'Lync Server 2013: 操作の依存関係'
description: 'Lync Server 2013: 操作の依存関係。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Operational dependencies
ms:assetid: 450b6be2-7fb3-47d7-8b0b-c05faa331e14
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720559(v=OCS.15)
ms:contentKeyID: 63969597
ms.date: 05/16/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4e240981f5dfded7c27f123c8483794ea3ffedff
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445296"
---
# <a name="operational-dependencies-in-lync-server-2013"></a><span data-ttu-id="c63d2-103">Lync Server 2013 での操作の依存関係</span><span class="sxs-lookup"><span data-stu-id="c63d2-103">Operational dependencies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c63d2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c63d2-104">

<span> </span></span></span>

<span data-ttu-id="c63d2-105">_**最終更新日:** 2015-05-15_</span><span class="sxs-lookup"><span data-stu-id="c63d2-105">_**Topic Last Modified:** 2015-05-15_</span></span>

<span data-ttu-id="c63d2-106">このドキュメントで説明されているリファレンスアーキテクチャでは、組織の要件を満たしているだけでなく、Microsoft のベストプラクティスに従って設計された Lync Server 2013 の展開を確実に行うことができます。</span><span class="sxs-lookup"><span data-stu-id="c63d2-106">The Reference Architecture discussed in this document will help ensure that you have a Lync Server 2013 deployment that not only scales to the organization’s requirements but is architected as per Microsoft best practices.</span></span> <span data-ttu-id="c63d2-107">Lync Server 2013 の実装は動的サービスであり、エンタープライズ内の他のサービスと同様、高レベルのサービスの可用性とサービス品質をビジネスに維持するためには、監視と予防的な管理が必要であると考えてください。</span><span class="sxs-lookup"><span data-stu-id="c63d2-107">Be that as it may the Lync Server 2013 implementation is a dynamic service and like any other service in the enterprise still requires monitoring and proactive management to maintain high level of service availability and service quality to the business.</span></span>

<span data-ttu-id="c63d2-108">Lync Server 2013 は組織の日常業務の ingrained になるため、サービスを正確かつ有形のサービスレベル管理によって管理することが重要です。</span><span class="sxs-lookup"><span data-stu-id="c63d2-108">As Lync Server 2013 becomes deeply ingrained in the organization’s everyday business it is important that the service be managed by accurate and tangible service level management.</span></span> <span data-ttu-id="c63d2-109">Lync システムアーキテクチャは複雑で、非常に統合され、効果的なサービスレベル管理を維持し、Lync Server 2013 の Sla を確立するために、その他のプラットフォームやサーバーに対するシステムの依存関係を理解することが重要になります。</span><span class="sxs-lookup"><span data-stu-id="c63d2-109">The Lync system architecture can become complex and very integrated and in order to maintain effective service level management and establish SLAs for Lync Server 2013 it becomes critical to understand the system’s dependencies on other platforms and servers.</span></span> <span data-ttu-id="c63d2-110">音声や UC に統合されたアプリケーションなど、どのビジネスサービスが Lync に依存しているかを確認することも重要です。</span><span class="sxs-lookup"><span data-stu-id="c63d2-110">Equally important is to note which business services, such as voice and UC integrated applications, become dependent on Lync.</span></span>

<span data-ttu-id="c63d2-111">すべての依存関係をメモするため、Lync Server 2013 を確立する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c63d2-111">Lync Server 2013 must be established noting all the said dependencies.</span></span> <span data-ttu-id="c63d2-112">Service map を使用すると、Lync とその依存サービスの間で SLA を策定し、SLA ネゴシエーションの開始位置を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="c63d2-112">The service map will allow you to formulate a SLA between Lync and its dependent service and provide a starting place for SLA negotiation.</span></span>

<span data-ttu-id="c63d2-113">次の表に、Lync インフラストラクチャの一般的な依存関係サービスを示します。</span><span class="sxs-lookup"><span data-stu-id="c63d2-113">The following table lists the typical dependency services for a Lync infrastructure.</span></span> <span data-ttu-id="c63d2-114">これらの各テクノロジには、独自の事前監視を用意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c63d2-114">Each of these technologies should have its own proactive monitoring.</span></span>

### <a name="typical-dependency-services"></a><span data-ttu-id="c63d2-115">一般的な依存関係サービス</span><span class="sxs-lookup"><span data-stu-id="c63d2-115">Typical dependency services</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c63d2-116">依存関係サービス</span><span class="sxs-lookup"><span data-stu-id="c63d2-116">Dependency Service</span></span></th>
<th></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c63d2-117">オペレーティング システム</span><span class="sxs-lookup"><span data-stu-id="c63d2-117">Operating systems</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c63d2-118">サーバーハードウェア</span><span class="sxs-lookup"><span data-stu-id="c63d2-118">Server Hardware</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c63d2-119">Active Directory</span><span class="sxs-lookup"><span data-stu-id="c63d2-119">Active Directory</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c63d2-120">公開キー基盤</span><span class="sxs-lookup"><span data-stu-id="c63d2-120">Public Key Infrastructure</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c63d2-121">ドメインネーミングサービス</span><span class="sxs-lookup"><span data-stu-id="c63d2-121">Domain Naming Service</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c63d2-122">データベースサービス</span><span class="sxs-lookup"><span data-stu-id="c63d2-122">Database Services</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c63d2-123">ストレージサービス</span><span class="sxs-lookup"><span data-stu-id="c63d2-123">Storage Services</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c63d2-124">システム管理–監視と配布</span><span class="sxs-lookup"><span data-stu-id="c63d2-124">System Management – Monitoring and distribution</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c63d2-125">セキュリティサービス-ウイルス対策</span><span class="sxs-lookup"><span data-stu-id="c63d2-125">Security Services - Antivirus</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c63d2-126">ネットワークインフラストラクチャ-インターネット</span><span class="sxs-lookup"><span data-stu-id="c63d2-126">Network Infrastructure - Internet</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c63d2-127">ネットワークインフラストラクチャ–内部 (LAN/WAN)</span><span class="sxs-lookup"><span data-stu-id="c63d2-127">Network Infrastructure – Internal (LAN/WAN)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c63d2-128">テレフォニーインフラストラクチャ– IP PBX とゲートウェイ</span><span class="sxs-lookup"><span data-stu-id="c63d2-128">Telephony Infrastructure – IP-PBX and Gateways</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c63d2-129">クラウドサービス</span><span class="sxs-lookup"><span data-stu-id="c63d2-129">Cloud Services</span></span></p></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c63d2-130">MOF で規定されている変更、インシデント、リリース管理などの基本的なサービスレベル管理機能を利用するために、組織が運用されていることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="c63d2-130">It is assumed that the organization is operationally mature in exercising basic service level management functions such as change, incident and release management as prescribed by the MOF.</span></span> <span data-ttu-id="c63d2-131">Lync ソリューションは、これらの機能によって採用され、同じ運用管理プロセスの対象となります。</span><span class="sxs-lookup"><span data-stu-id="c63d2-131">The Lync solution should be adopted by these functions and become subject to the same operational management processes.</span></span>

<span data-ttu-id="c63d2-132">上に記載された情報に基づいて構築することで、企業の Lync サービスに影響を与える可能性が高くなります。</span><span class="sxs-lookup"><span data-stu-id="c63d2-132">Building on the information obtained above we now have a greater understanding of what can impact the Lync service in the enterprise.</span></span> <span data-ttu-id="c63d2-133">Lync Server 2013 サービスの可用性と品質を確保するために、次の監視ツールを参照アーキテクチャの展開に付随させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="c63d2-133">To help ensure Lync Server 2013 service availability and quality, the following monitoring tools must accompany the reference architecture deployment:</span></span>

### <a name="monitoring-tools"></a><span data-ttu-id="c63d2-134">監視ツール</span><span class="sxs-lookup"><span data-stu-id="c63d2-134">Monitoring tools</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c63d2-135">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="c63d2-135">Component</span></span></th>
<th><span data-ttu-id="c63d2-136">説明</span><span class="sxs-lookup"><span data-stu-id="c63d2-136">Description</span></span></th>
<th><span data-ttu-id="c63d2-137">該当するサイト</span><span class="sxs-lookup"><span data-stu-id="c63d2-137">Applicable Site</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c63d2-138">Lync Server 2013 Monitoring Server</span><span class="sxs-lookup"><span data-stu-id="c63d2-138">Lync Server 2013 Monitoring Server</span></span></p></td>
<td><p><span data-ttu-id="c63d2-139">中央サイトあたり少なくとも1つの Lync Server 2013 監視サーバーロールを展開して、Quality of Experience (QoE) レポートパックを構成します。</span><span class="sxs-lookup"><span data-stu-id="c63d2-139">Deploy at least one Lync Server 2013 Monitoring Server role per Central site and configure Quality of Experience (QoE) Reporting Pack.</span></span></p>
<p><span data-ttu-id="c63d2-140">詳細については、Lync Server 2013 展開に関するドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c63d2-140">Refer to the Lync Server 2013 Deployment documentation for further details:</span></span></p>
<p><span data-ttu-id="c63d2-141"><a href="lync-server-2013-deploying-monitoring.md">Lync Server 2013 での監視の展開</a></span><span class="sxs-lookup"><span data-stu-id="c63d2-141"><a href="lync-server-2013-deploying-monitoring.md">Deploying monitoring in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="c63d2-142">セントラルサイト</span><span class="sxs-lookup"><span data-stu-id="c63d2-142">Central sites</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="c63d2-143">各プールを監視サーバーの役割の最も近いインスタンスにします。</span><span class="sxs-lookup"><span data-stu-id="c63d2-143">Tether each pool to its nearest instance of the Monitoring Server role.</span></span></p></td>
<td><p><span data-ttu-id="c63d2-144">セントラルサイト</span><span class="sxs-lookup"><span data-stu-id="c63d2-144">Central sites</span></span></p>
<p><span data-ttu-id="c63d2-145">ブランチサイト</span><span class="sxs-lookup"><span data-stu-id="c63d2-145">Branch sites</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c63d2-146">System Center Operations Manager 2012</span><span class="sxs-lookup"><span data-stu-id="c63d2-146">System Center Operations Manager 2012</span></span></p></td>
<td><p><span data-ttu-id="c63d2-147">System Center Operations Manager 2012 (Microsoft Lync Server 2013 管理パック (MP) をインポートしました。</span><span class="sxs-lookup"><span data-stu-id="c63d2-147">System Center Operations Manager 2012 with the Microsoft Lync Server 2013 Management Pack (MP) imported.</span></span></p>
<p><span data-ttu-id="c63d2-148">管理パックは、従来のイベントログとパフォーマンスカウンターベースのインストルメンテーションを実装するだけでなく、Lync Server 2013 で新しく利用可能なインストルメンテーションを有効にします。</span><span class="sxs-lookup"><span data-stu-id="c63d2-148">The Management Pack implements traditional Event Log and Performance counter based instrumentation is utilized as well as enabling newly available instrumentation in Lync Server 2013.</span></span></p></td>
<td><p><span data-ttu-id="c63d2-149">セントラルサイト</span><span class="sxs-lookup"><span data-stu-id="c63d2-149">Central sites</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="c63d2-150">監視する必要がある役割やコンポーネントの検出に対する集中検出が、全体管理データベースで公開されているトポロジドキュメントを読み取るセントラル検出スクリプトに基づいて、自動的に完了するようにします。</span><span class="sxs-lookup"><span data-stu-id="c63d2-150">Make sure that Central Discovery to discovery of roles and components that need to be monitored are automatically completed based on a central discovery script that reads the topology document published in Central Management Database.</span></span></p></td>
<td><p><span data-ttu-id="c63d2-151">中央サイト</span><span class="sxs-lookup"><span data-stu-id="c63d2-151">Central Site</span></span></p>
<p><span data-ttu-id="c63d2-152">ブランチサイト</span><span class="sxs-lookup"><span data-stu-id="c63d2-152">Branch Site</span></span></p>
<p><span data-ttu-id="c63d2-153">Edge サイト</span><span class="sxs-lookup"><span data-stu-id="c63d2-153">Edge Site</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="c63d2-154">Lync Server を実行しているすべての展開されたサーバーに System Centre Operations Manager 2007 エージェントを展開します。</span><span class="sxs-lookup"><span data-stu-id="c63d2-154">Deploy System Centre Operations Manager 2007 agents to all deployed servers running Lync Server.</span></span></p></td>
<td><p><span data-ttu-id="c63d2-155">中央サイト</span><span class="sxs-lookup"><span data-stu-id="c63d2-155">Central Site</span></span></p>
<p><span data-ttu-id="c63d2-156">ブランチサイト</span><span class="sxs-lookup"><span data-stu-id="c63d2-156">Branch Site</span></span></p>
<p><span data-ttu-id="c63d2-157">Edge サイト</span><span class="sxs-lookup"><span data-stu-id="c63d2-157">Edge Site</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="c63d2-158">優先順位付きのアラートが通知用に構成されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c63d2-158">Make sure Prioritized Alerts are configured for notification:</span></span></p>
<p><span data-ttu-id="c63d2-159">優先度の高い警告</span><span class="sxs-lookup"><span data-stu-id="c63d2-159">High Priority Alerts</span></span></p>
<p><span data-ttu-id="c63d2-160">中程度の優先度の警告</span><span class="sxs-lookup"><span data-stu-id="c63d2-160">Medium Priority Alerts</span></span></p>
<p><span data-ttu-id="c63d2-161">その他のアラート。</span><span class="sxs-lookup"><span data-stu-id="c63d2-161">Other Alerts.</span></span></p></td>
<td><p><span data-ttu-id="c63d2-162">中央サイト</span><span class="sxs-lookup"><span data-stu-id="c63d2-162">Central Site</span></span></p>
<p><span data-ttu-id="c63d2-163">ブランチサイト</span><span class="sxs-lookup"><span data-stu-id="c63d2-163">Branch Site</span></span></p>
<p><span data-ttu-id="c63d2-164">Edge サイト</span><span class="sxs-lookup"><span data-stu-id="c63d2-164">Edge Site</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="c63d2-165">展開のポート監視を構成します。</span><span class="sxs-lookup"><span data-stu-id="c63d2-165">Configure Port monitoring for your deployment.</span></span></p></td>
<td><p><span data-ttu-id="c63d2-166">中央サイト</span><span class="sxs-lookup"><span data-stu-id="c63d2-166">Central Site</span></span></p>
<p><span data-ttu-id="c63d2-167">ブランチサイト</span><span class="sxs-lookup"><span data-stu-id="c63d2-167">Branch Site</span></span></p>
<p><span data-ttu-id="c63d2-168">Edge サイト</span><span class="sxs-lookup"><span data-stu-id="c63d2-168">Edge Site</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="c63d2-169">展開のための URL 監視を構成する</span><span class="sxs-lookup"><span data-stu-id="c63d2-169">Configure URL monitoring for your deployment</span></span></p></td>
<td><p><span data-ttu-id="c63d2-170">中央サイト</span><span class="sxs-lookup"><span data-stu-id="c63d2-170">Central Site</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c63d2-171">Lync と System Center Operations Manager の統合</span><span class="sxs-lookup"><span data-stu-id="c63d2-171">Lync and System Center Operations Manager integration</span></span></p></td>
<td><p><span data-ttu-id="c63d2-172">通話の信頼性とメディア品質監視通話の信頼性とメディアの品質監視監視ノードとして監視サーバーコンピューターを使用して、通話の信頼性とメディア品質を監視します。</span><span class="sxs-lookup"><span data-stu-id="c63d2-172">Deploy Call Reliability and Media Quality MonitoringCall reliability and media quality monitoring use the Monitoring Server computer as their watcher node to monitor call reliability and media quality of Lync Server.</span></span> <span data-ttu-id="c63d2-173">どちらの機能でも、監視サーバーのデータベースに対して分析を実行します。</span><span class="sxs-lookup"><span data-stu-id="c63d2-173">Both of these features query the Monitoring Server databases to do analysis.</span></span></p></td>
<td><p><span data-ttu-id="c63d2-174">中央サイト</span><span class="sxs-lookup"><span data-stu-id="c63d2-174">Central Site</span></span></p>
<p><span data-ttu-id="c63d2-175">ブランチサイト</span><span class="sxs-lookup"><span data-stu-id="c63d2-175">Branch Site</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="c63d2-176">メディア品質の警告しきい値が正確に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c63d2-176">Ensure Media Quality warning thresholds are accurately configured.</span></span> <span data-ttu-id="c63d2-177">次の表は、コーデックによる最大ネットワーク平均の意見スコアを示しています。</span><span class="sxs-lookup"><span data-stu-id="c63d2-177">The following table indicates the maximum Network Mean Opinion Scores by Codec.</span></span> <span data-ttu-id="c63d2-178">実稼働環境では、これらのスコアは設定された期間に対して監視する必要があり、許容されるしきい値は、組織固有の NMOS スコアに基づいて確立する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c63d2-178">In production these scores should be monitored for a set period and acceptable thresholds must be established based on the organization specific NMOS scores.</span></span></p></td>
<td><p><span data-ttu-id="c63d2-179">中央サイト</span><span class="sxs-lookup"><span data-stu-id="c63d2-179">Central Site</span></span></p>
<p><span data-ttu-id="c63d2-180">ブランチサイト</span><span class="sxs-lookup"><span data-stu-id="c63d2-180">Branch Site</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c63d2-181">Lync Server 2013 の代理トランザクションウォッチャー</span><span class="sxs-lookup"><span data-stu-id="c63d2-181">Lync Server 2013 Synthetic Transaction Watcher</span></span></p></td>
<td><p><span data-ttu-id="c63d2-182">専用の Lync サーバーを代理トランザクションウォッチャーとして展開します。</span><span class="sxs-lookup"><span data-stu-id="c63d2-182">Deploy a dedicated Lync Server to be a synthetic transaction watcher.</span></span></p>
<p><span data-ttu-id="c63d2-183">代理トランザクションは、事前に定義された間隔で管理パックによって自動的にトリガーされる Lync Server 2013 Windows PowerShell コマンドレットです。</span><span class="sxs-lookup"><span data-stu-id="c63d2-183">Synthetic transactions are Lync Server 2013 Windows PowerShell cmdlets that are automatically triggered by the management pack on a predefined interval.</span></span> <span data-ttu-id="c63d2-184">これらは、各プールの STs の検出と実行を担当する管理者指定のサーバーである代理トランザクションウォッチャーノードで実行されます。</span><span class="sxs-lookup"><span data-stu-id="c63d2-184">These are executed on a synthetic transaction watcher node which is an administrator designated server responsible for discovery and execution of STs for each pool.</span></span></p>
<p><span data-ttu-id="c63d2-185">既存の Microsoft Lync Server 2013 サーバーを代理トランザクションウォッチャーノードとして使用することはお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="c63d2-185">We do not recommend that you use an existing Microsoft Lync Server 2013 server as a synthetic transaction watcher node.</span></span> <span data-ttu-id="c63d2-186">これは、STs を実行するための CPU またはメモリ使用量の高い要件が原因で発生します。</span><span class="sxs-lookup"><span data-stu-id="c63d2-186">This is due to the high CPU/memory usage requirements for running STs.</span></span> <span data-ttu-id="c63d2-187">代理トランザクションウォッチャーノードには、新しいサーバーコンピューター (または仮想サーバー) を使います。</span><span class="sxs-lookup"><span data-stu-id="c63d2-187">Use a new server computer (or a virtual server) for the synthetic transaction watcher node.</span></span></p></td>
<td><p><span data-ttu-id="c63d2-188">中央サイト</span><span class="sxs-lookup"><span data-stu-id="c63d2-188">Central Site</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="c63d2-189">代理トランザクションウォッチャーノードを展開します。</span><span class="sxs-lookup"><span data-stu-id="c63d2-189">Deploying synthetic transactions watcher node.</span></span></p>
<p><span data-ttu-id="c63d2-190">MonitoringCS_withSCOM.docx ドキュメントを参照してください。 [ドキュメントの接続] をタップします。</span><span class="sxs-lookup"><span data-stu-id="c63d2-190">Refer to the MonitoringCS_withSCOM.docx document from UCTAP connect documentation.</span></span></p></td>
<td><p><span data-ttu-id="c63d2-191">中央サイト</span><span class="sxs-lookup"><span data-stu-id="c63d2-191">Central Site</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="maximum-network-mos-scores-per-codec"></a><span data-ttu-id="c63d2-192">コーデックあたりの最大ネットワーク MOS スコア</span><span class="sxs-lookup"><span data-stu-id="c63d2-192">Maximum Network MOS scores per codec</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c63d2-193">シナリオ</span><span class="sxs-lookup"><span data-stu-id="c63d2-193">Scenario</span></span></th>
<th><span data-ttu-id="c63d2-194">コーデック</span><span class="sxs-lookup"><span data-stu-id="c63d2-194">Codec</span></span></th>
<th><span data-ttu-id="c63d2-195">最大 NMOS</span><span class="sxs-lookup"><span data-stu-id="c63d2-195">Max NMOS</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c63d2-196">UC-UC 通話</span><span class="sxs-lookup"><span data-stu-id="c63d2-196">UC-UC call</span></span></p></td>
<td><p><span data-ttu-id="c63d2-197">RTAudio WB</span><span class="sxs-lookup"><span data-stu-id="c63d2-197">RTAudio WB</span></span></p></td>
<td><p><span data-ttu-id="c63d2-198">4.10</span><span class="sxs-lookup"><span data-stu-id="c63d2-198">4.10</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c63d2-199">UC-UC 通話</span><span class="sxs-lookup"><span data-stu-id="c63d2-199">UC-UC call</span></span></p></td>
<td><p><span data-ttu-id="c63d2-200">RTAudio NB</span><span class="sxs-lookup"><span data-stu-id="c63d2-200">RTAudio NB</span></span></p></td>
<td><p><span data-ttu-id="c63d2-201">2.95</span><span class="sxs-lookup"><span data-stu-id="c63d2-201">2.95</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c63d2-202">電話会議</span><span class="sxs-lookup"><span data-stu-id="c63d2-202">Conference call</span></span></p></td>
<td><p><span data-ttu-id="c63d2-203">Siren</span><span class="sxs-lookup"><span data-stu-id="c63d2-203">Siren</span></span></p></td>
<td><p><span data-ttu-id="c63d2-204">3.72</span><span class="sxs-lookup"><span data-stu-id="c63d2-204">3.72</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c63d2-205">UC-PSTN 通話</span><span class="sxs-lookup"><span data-stu-id="c63d2-205">UC-PSTN call</span></span></p></td>
<td><p><span data-ttu-id="c63d2-206">RTAudio NB</span><span class="sxs-lookup"><span data-stu-id="c63d2-206">RTAudio NB</span></span></p></td>
<td><p><span data-ttu-id="c63d2-207">2.95</span><span class="sxs-lookup"><span data-stu-id="c63d2-207">2.95</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c63d2-208">UC-PSTN 通話</span><span class="sxs-lookup"><span data-stu-id="c63d2-208">UC-PSTN call</span></span></p></td>
<td><p><span data-ttu-id="c63d2-209">G-711</span><span class="sxs-lookup"><span data-stu-id="c63d2-209">G-711</span></span></p></td>
<td><p><span data-ttu-id="c63d2-210">3.61</span><span class="sxs-lookup"><span data-stu-id="c63d2-210">3.61</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c63d2-211">以前のプロアクティブな監視アクティビティの前後に、メンテナンスタスクは、Lync RA 運用ガイドで定義されているように、毎日、毎週、および毎月の定期的、エッジサイトとブランチサイトに対して実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c63d2-211">Over and above the previous pro-active monitoring activities, maintenance tasks should be executed for Central, Edge and Branch sites on a recurring daily, weekly and monthly basis as defined in the Lync RA Operations Guide.</span></span>

<span data-ttu-id="c63d2-212"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c63d2-212"></div>

<span> </span>

</div>

</div>

</span></span></div>

