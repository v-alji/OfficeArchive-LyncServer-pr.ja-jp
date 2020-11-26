---
title: 'Lync Server 2013: 常設チャットサーバーのキャパシティ計画'
description: 'Lync Server 2013: 常設チャットサーバーのキャパシティ計画。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Capacity planning for Persistent Chat Server
ms:assetid: 7a850cd5-c789-4795-a8ff-083be21ae784
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615006(v=OCS.15)
ms:contentKeyID: 48184580
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f78f9f3666fb272b808ef36da2d3010f451d0079
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435559"
---
# <a name="capacity-planning-for-persistent-chat-server-in-lync-server-2013"></a><span data-ttu-id="6e5ff-103">Lync Server 2013 の常設チャットサーバーのキャパシティ計画</span><span class="sxs-lookup"><span data-stu-id="6e5ff-103">Capacity planning for Persistent Chat Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6e5ff-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6e5ff-104">

<span> </span></span></span>

<span data-ttu-id="6e5ff-105">_**最終更新日:** 2012-10-05_</span><span class="sxs-lookup"><span data-stu-id="6e5ff-105">_**Topic Last Modified:** 2012-10-05_</span></span>

<span data-ttu-id="6e5ff-106">常設チャットサーバーでは、ユーザーがリアルタイムでリアルタイムでチャットを行うことができます。これは、今後の取得や検索のために保持されます。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-106">Persistent Chat Server can perform multi-user real-time chat that can persist for future retrieval and search.</span></span> <span data-ttu-id="6e5ff-107">ユーザーのメールボックスに保存されているグループのインスタントメッセージング (IM) とは異なり、会話履歴が構成されている場合、常設チャットサーバーセッションは開いたままになり、コンテンツはサーバーに保存され、メッセージ、ファイル、Url、および進行中の会話の一部であるその他のデータが保存されます。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-107">Unlike group instant messaging (IM) that is saved in a user’s mailbox if conversation history is configured, a Persistent Chat Server session stays open longer, and the content is saved on a server, along with the messages, files, URLs, and other data that are part of an ongoing conversation.</span></span>

<span data-ttu-id="6e5ff-108">キャパシティプランニングは、常設チャットサーバーの展開を準備するための重要な要素です。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-108">Capacity planning is an important part of preparing to deploy Persistent Chat Server.</span></span> <span data-ttu-id="6e5ff-109">このトピックでは、サポートされている常設チャットサーバートポロジとキャパシティ計画の表について詳しく説明します。これを使用すると、展開に最適な構成を決定することができます。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-109">This topic provides details about supported Persistent Chat Server topologies and capacity planning tables that you can use to determine the best configuration for your deployment.</span></span> <span data-ttu-id="6e5ff-110">また、ピーク時に容量を大きくする必要がある常設チャットサーバーの展開を適切に管理する方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-110">It also describes how to best manage Persistent Chat Server deployments that require greater capacity at peak times.</span></span>

<span data-ttu-id="6e5ff-111">常設チャットサーバーをダウンロードするには、の「Microsoft Lync Server 13 常設チャットサーバー」を参照してください [https://go.microsoft.com/fwlink/p/?linkId=209539](https://go.microsoft.com/fwlink/p/?linkid=209539) 。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-111">To download Persistent Chat Server, see "Microsoft Lync Server 13 Persistent Chat Server" at [https://go.microsoft.com/fwlink/p/?linkId=209539](https://go.microsoft.com/fwlink/p/?linkid=209539).</span></span>

<span data-ttu-id="6e5ff-112">常設チャットサーバーのインストールの詳細については、展開ドキュメントの「lync server [2013 での](lync-server-2013-installing-persistent-chat-server.md) 常設チャットサーバーのインストールと [常設チャット2013サーバーの構成](lync-server-2013-configuring-persistent-chat-server.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-112">For details about installing Persistent Chat Server, see [Installing Persistent Chat Server in Lync Server 2013](lync-server-2013-installing-persistent-chat-server.md) and [Configuring Persistent Chat Server in Lync Server 2013](lync-server-2013-configuring-persistent-chat-server.md) in the Deployment documentation.</span></span>

<span data-ttu-id="6e5ff-113">Lync Server 計画ツールなどのサポートツールを利用すると、容量の計画をさらに助けることができます。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-113">Support tools, such as Lync Server Planning Tool, can further assist you with capacity planning.</span></span> <span data-ttu-id="6e5ff-114">計画ツールの詳細については、計画ドキュメントの「 [Lync Server 2013 の計画プロセスの開始](lync-server-2013-beginning-the-planning-process.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-114">For details about the Planning Tool, see [Beginning the planning process for Lync Server 2013](lync-server-2013-beginning-the-planning-process.md) in the Planning documentation.</span></span>

<div>

## <a name="persistent-chat-server-supported-topologies"></a><span data-ttu-id="6e5ff-115">常設チャットサーバーでサポートされているトポロジ</span><span class="sxs-lookup"><span data-stu-id="6e5ff-115">Persistent Chat Server Supported Topologies</span></span>

<span data-ttu-id="6e5ff-116">常設チャットサーバーは、単一サーバープールまたは複数サーバープール、または単一プールトポロジまたは複数プールトポロジで展開できます。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-116">You can deploy Persistent Chat Server in single-server or multiple-server pools, and with single-pool or multiple-pool topology.</span></span>

<span data-ttu-id="6e5ff-117">新しい Lync Server 2013 の展開用に、Standard Edition server 上の常設チャットサーバーもサポートされるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-117">We now also support Persistent Chat Server on Standard Edition server for new Lync Server 2013 deployments.</span></span> <span data-ttu-id="6e5ff-118">ただし、パフォーマンスと規模が影響を受けます。また、この新しい展開には高可用性オプションがないため、これは主に概念や評価の証明のために使用することを前提としています。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-118">However, performance and scale will be affected, and because there is no high availability option for this new deployment, we expect you to use this primarily for the purposes of proof of concept, evaluation, and so on.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="6e5ff-119">両方のトポロジの詳細については、このドキュメントの「 <A href="lync-server-2013-planning-for-persistent-chat-server.md">常設チャット2013サーバーの計画</A> 」を参照してください。展開ドキュメントには、「 <A href="lync-server-2013-deploying-persistent-chat-server.md">lync server 2013 での常設チャットサーバー</A> の設定と展開」が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-119">For additional details about both topologies, see <A href="lync-server-2013-planning-for-persistent-chat-server.md">Planning for Persistent Chat Server in Lync Server 2013</A> in this documentation set and <A href="lync-server-2013-deploying-persistent-chat-server.md">Deploying Persistent Chat Server in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="single-server-topology"></a><span data-ttu-id="6e5ff-120">Single-Server トポロジ</span><span class="sxs-lookup"><span data-stu-id="6e5ff-120">Single-Server Topology</span></span>

<span data-ttu-id="6e5ff-121">常設チャットサーバー向けの最小構成と最も簡単な展開は、1つの常設チャットサーバーのフロントエンドサーバートポロジです。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-121">The minimum configuration and simplest deployment for Persistent Chat Server is a single Persistent Chat Server Front End Server topology.</span></span> <span data-ttu-id="6e5ff-122">この展開を行うには、常設チャットサーバーを実行する単一のサーバー (必要に応じてコンプライアンスサービスを実行します)、SQL Server データベースをホストしているサーバー、コンプライアンスが必要な場合は、コンプライアンスデータを格納する SQL Server データベースが必要です。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-122">This deployment requires a single server that runs Persistent Chat Server (which optionally runs the Compliance service, if compliance is enabled), a server that hosts both the SQL Server database, and if compliance is required, the SQL Server database to store the compliance data.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="6e5ff-123">トポロジビルダーでシングルサーバー展開として開始された常設チャットサーバープールにサーバーを追加することはできません。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-123">You cannot add additional servers to a Persistent Chat Server pool that is started as a single-server deployment in Topology Builder.</span></span> <span data-ttu-id="6e5ff-124">単一のサーバーを使用している場合でも、複数サーバープールトポロジの使用をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-124">We recommend using the multiple-server pool topology, even if you’re using a single server.</span></span> <span data-ttu-id="6e5ff-125">これは、必要に応じて後でサーバーを追加できるようにするためです。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-125">This is so that you’ll be able to add more servers later, if it's necessary.</span></span> 


</div>

<span data-ttu-id="6e5ff-126">次の図は、コンプライアンスを備えた単一の常設チャットサーバーフロントエンドサーバーのトポロジの必須コンポーネントとオプションコンポーネントをすべて示しています。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-126">The following figure shows all required and optional components of a topology for a single Persistent Chat Server Front End Server with compliance.</span></span>

<span data-ttu-id="6e5ff-127">**1つの常設チャットサーバー**</span><span class="sxs-lookup"><span data-stu-id="6e5ff-127">**Single Persistent Chat Server**</span></span>

<span data-ttu-id="6e5ff-128">![コンプライアンスサービスを備えた単一サーバートポロジ](images/Gg398500.9168fa52-61e0-4d17-a14d-45fd32e81456(OCS.15).jpg "コンプライアンスサービスを備えた単一サーバートポロジ")</span><span class="sxs-lookup"><span data-stu-id="6e5ff-128">![Single server topology with Compliance service](images/Gg398500.9168fa52-61e0-4d17-a14d-45fd32e81456(OCS.15).jpg "Single server topology with Compliance service")</span></span>

</div>

<div>

## <a name="multiple-server-topology"></a><span data-ttu-id="6e5ff-129">Multiple-Server トポロジ</span><span class="sxs-lookup"><span data-stu-id="6e5ff-129">Multiple-Server Topology</span></span>

<span data-ttu-id="6e5ff-130">より多くの容量と信頼性を実現するには、「 [Lync server 2013 での常設チャットサーバーの計画](lync-server-2013-planning-for-persistent-chat-server.md)」で説明されているように、複数サーバートポロジを展開します。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-130">To provide greater capacity and reliability, you can deploy a multiple-server topology, as described in [Planning for Persistent Chat Server in Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md).</span></span> <span data-ttu-id="6e5ff-131">複数サーバーのトポロジには、常設チャットサーバーを実行しているアクティブなコンピューターを4つまで含めることができます (高可用性および障害回復構成では最大8個まで可能)。ただし、4つはアクティブ、残りの4つはスタンバイ状態になります。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-131">The multiple-server topology can include as many as four active computers running Persistent Chat Server (high availability and disaster recovery configurations will allow up to eight, but only four can be active and the remaining four on standby).</span></span> <span data-ttu-id="6e5ff-132">各サーバーは、最大で2万の同時ユーザーをサポートできます。合計で8万の同時使用ユーザーは、4台のサーバーで常設チャットサーバープールに接続されています。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-132">Each server can support as many as 20,000 concurrent users, for a total of 80,000 concurrent users connected to a Persistent Chat Server pool with 4 servers.</span></span> <span data-ttu-id="6e5ff-133">複数サーバーのトポロジは、複数のサーバーが常設チャットサーバーをホストしていることを除いて、単一サーバートポロジと同じで、拡大縮小できます。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-133">A multiple-server topology is the same as the single-server topology except that multiple servers host Persistent Chat Server, and can scale higher.</span></span> <span data-ttu-id="6e5ff-134">常設チャットサーバーを実行している複数のコンピューターは、Lync Server とコンプライアンスサービスと同じ Active Directory ドメインサービスドメインに存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-134">Multiple computers running Persistent Chat Server should reside in the same Active Directory Domain Services domain as Lync Server and the Compliance service.</span></span>

<span data-ttu-id="6e5ff-135">次の図は、常設チャットサーバーを実行している複数のコンピューター、オプションのコンプライアンスサービス、および別のコンプライアンスデータベースの複数サーバートポロジのすべてのコンポーネントを示しています。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-135">The following figure shows all the components of a multiple-server topology with multiple computers running Persistent Chat Server, the optional Compliance service, and a separate compliance database.</span></span>

<span data-ttu-id="6e5ff-136">**複数の常設チャットサーバー**</span><span class="sxs-lookup"><span data-stu-id="6e5ff-136">**Multiple Persistent Chat Servers**</span></span>

<span data-ttu-id="6e5ff-137">![複数サーバートポロジ](images/Gg398500.19aea898-28df-4d9b-903c-f72ef062d919(OCS.15).jpg "複数サーバートポロジ")</span><span class="sxs-lookup"><span data-stu-id="6e5ff-137">![Multiple server topology](images/Gg398500.19aea898-28df-4d9b-903c-f72ef062d919(OCS.15).jpg "Multiple server topology")</span></span>

<span data-ttu-id="6e5ff-138">4サーバーの常設チャットサーバーの展開では、8万ユーザーは同時にサインインして常設チャットを使用することができます。ロードは、サーバーあたり2万ユーザーに均等に配布されます。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-138">In a four-server Persistent Chat Server deployment, where 80,000 users can be simultaneously signed in to and using Persistent Chat, the load is distributed evenly at 20,000 users per server.</span></span> <span data-ttu-id="6e5ff-139">1つのサーバーが利用できなくなった場合、そのサーバーに接続されているユーザーは、常設チャットサーバーにアクセスできなくなります。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-139">If one server becomes unavailable, the users who are connected to that server will lose their access to Persistent Chat Server.</span></span> <span data-ttu-id="6e5ff-140">切断されたユーザーは、利用できなくなったサーバーが復元されるまでは、残りのサーバーに自動的に転送されます。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-140">The disconnected users will be automatically transferred to the remaining servers until the unavailable server is restored.</span></span> <span data-ttu-id="6e5ff-141">ネットワーク上での常設チャットトラフィックの量によっては、この転送には数分かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-141">Depending on the amount of Persistent Chat traffic on the network, this transfer can take a few minutes or longer.</span></span> <span data-ttu-id="6e5ff-142">残りの各サーバーは、最大3万ユーザーとしてホストされている可能性があるため、パフォーマンスの問題を回避するために、使用できないサーバーをできるだけ早く復元することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-142">Because each of the remaining servers might be hosting as many as 30,000 users, we recommend that you restore the unavailable server as quickly as possible to avoid performance issues.</span></span> <span data-ttu-id="6e5ff-143">それ以外の場合は、Topology Builder または Windows PowerShell コマンドレット **CsPersistentChatActiveServer** を使用して、別の常設チャットサーバーを利用できるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-143">Otherwise, you can make another Persistent Chat Server available by using the Topology Builder or the Windows PowerShell cmdlet, **set-CsPersistentChatActiveServer**.</span></span>

</div>

</div>

<div>

## <a name="persistent-chat-server-capacity-planning"></a><span data-ttu-id="6e5ff-144">常設チャットサーバーのキャパシティプランニング</span><span class="sxs-lookup"><span data-stu-id="6e5ff-144">Persistent Chat Server Capacity Planning</span></span>

<span data-ttu-id="6e5ff-145">常設チャットサーバーの容量計画については、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-145">The following tables can help you with capacity planning for Persistent Chat Server.</span></span> <span data-ttu-id="6e5ff-146">これは、常設チャットサーバー設定の変更による容量機能への影響をモデル化しています。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-146">They model how changing various Persistent Chat Server settings affect capacity capabilities.</span></span>

<div>

## <a name="planning-your-maximum-capacity-for-persistent-chat-server"></a><span data-ttu-id="6e5ff-147">常設チャットサーバーの最大キャパシティの計画</span><span class="sxs-lookup"><span data-stu-id="6e5ff-147">Planning Your Maximum Capacity for Persistent Chat Server</span></span>

<span data-ttu-id="6e5ff-148">次のサンプル表を使用して、サポートすることができるユーザー数を判断します。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-148">Use the following sample table to determine the number of users you will be able to support.</span></span>

### <a name="persistent-chat-server-pool-maximum-capacity-sample"></a><span data-ttu-id="6e5ff-149">常設チャットサーバープールの最大容量のサンプル</span><span class="sxs-lookup"><span data-stu-id="6e5ff-149">Persistent Chat Server pool Maximum Capacity Sample</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6e5ff-150">アクティブな常設チャットサービスのインスタンス</span><span class="sxs-lookup"><span data-stu-id="6e5ff-150">Active Persistent Chat service instances</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-151"><em>4</em></span><span class="sxs-lookup"><span data-stu-id="6e5ff-151"><em>4</em></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e5ff-152">常設チャットサービスのインスタンス</span><span class="sxs-lookup"><span data-stu-id="6e5ff-152">Persistent Chat service instances</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-153"><em>8 (4 は非アクティブにする必要がありますが、最大値は4です)</em></span><span class="sxs-lookup"><span data-stu-id="6e5ff-153"><em>8 (4 must be inactive; only a maximum of 4 can be active)</em></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e5ff-154">アクティブな接続ユーザー数</span><span class="sxs-lookup"><span data-stu-id="6e5ff-154">Active users connected</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-155"><em>80,000</em></span><span class="sxs-lookup"><span data-stu-id="6e5ff-155"><em>80,000</em></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e5ff-156">プロビジョニング対象ユーザーの総数</span><span class="sxs-lookup"><span data-stu-id="6e5ff-156">Total provisioned users</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-157">150,000</span><span class="sxs-lookup"><span data-stu-id="6e5ff-157">150,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e5ff-158">エンドポイント数</span><span class="sxs-lookup"><span data-stu-id="6e5ff-158">Number of endpoints</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-159">120,000</span><span class="sxs-lookup"><span data-stu-id="6e5ff-159">120,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6e5ff-160">上記のサンプルでは、常設チャットサーバーで許可されているユーザーの最大数をサポートしています。常設チャットサービスの4つのサーバーとインスタンス (高可用性と障害回復のために常設チャットサーバーを実行している場合は4つのパッシブサーバー、サーバーあたりは2万ユーザー)、合計8万のアクティブユーザーを対象とします。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-160">In the preceding sample, the plan is to support the maximum number of users that Persistent Chat Server allows: four servers/instances of the Persistent Chat service (can have four more passive servers running Persistent Chat Server for high availability and disaster recovery) and 20,000 users per server, for a total of 80,000 active users.</span></span>

</div>

<div>

## <a name="capacity-planning-for-managing-persistent-chat-room-access"></a><span data-ttu-id="6e5ff-161">常設チャットルームへのアクセスを管理するためのキャパシティ計画</span><span class="sxs-lookup"><span data-stu-id="6e5ff-161">Capacity Planning for Managing Persistent Chat Room Access</span></span>

<span data-ttu-id="6e5ff-162">次のサンプルテーブルは、常設チャットサーバープールでの常設チャットルームへのアクセスを管理するための計画に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-162">The following sample table can help you plan for managing Persistent Chat room access in a Persistent Chat Server pool.</span></span>

### <a name="managing-chat-room-access-sample"></a><span data-ttu-id="6e5ff-163">チャットルームへのアクセスサンプルの管理</span><span class="sxs-lookup"><span data-stu-id="6e5ff-163">Managing Chat Room Access Sample</span></span>

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
<th></th>
<th><span data-ttu-id="6e5ff-164">小規模チャット ルーム</span><span class="sxs-lookup"><span data-stu-id="6e5ff-164">Small Chat Rooms</span></span></th>
<th><span data-ttu-id="6e5ff-165">中規模チャット ルーム</span><span class="sxs-lookup"><span data-stu-id="6e5ff-165">Medium Chat Rooms</span></span></th>
<th><span data-ttu-id="6e5ff-166">大規模チャット ルーム</span><span class="sxs-lookup"><span data-stu-id="6e5ff-166">Large Chat Rooms</span></span></th>
<th><span data-ttu-id="6e5ff-167">合計</span><span class="sxs-lookup"><span data-stu-id="6e5ff-167">Total</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6e5ff-168">チャット ルームのサイズ (接続ユーザー数)</span><span class="sxs-lookup"><span data-stu-id="6e5ff-168">Size of chat rooms (number of users connected)</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-169">ルームあたり 30 ユーザー</span><span class="sxs-lookup"><span data-stu-id="6e5ff-169">30 per room</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-170">ルームあたり 150 ユーザー</span><span class="sxs-lookup"><span data-stu-id="6e5ff-170">150 per room</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-171">ルームあたり 16,000 ユーザー</span><span class="sxs-lookup"><span data-stu-id="6e5ff-171">16,000 per room</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e5ff-172">チャット ルーム</span><span class="sxs-lookup"><span data-stu-id="6e5ff-172">Chat rooms</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-173">32,000</span><span class="sxs-lookup"><span data-stu-id="6e5ff-173">32,000</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-174">1,067</span><span class="sxs-lookup"><span data-stu-id="6e5ff-174">1,067</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-175">常用</span><span class="sxs-lookup"><span data-stu-id="6e5ff-175">10</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-176">33,077</span><span class="sxs-lookup"><span data-stu-id="6e5ff-176">33,077</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e5ff-177">大会議室の割合 (%)</span><span class="sxs-lookup"><span data-stu-id="6e5ff-177">% of rooms that are auditorium</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-178">1%</span><span class="sxs-lookup"><span data-stu-id="6e5ff-178">1%</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-179">1%</span><span class="sxs-lookup"><span data-stu-id="6e5ff-179">1%</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-180">50%</span><span class="sxs-lookup"><span data-stu-id="6e5ff-180">50%</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e5ff-181">オープン ルームの割合 (%)</span><span class="sxs-lookup"><span data-stu-id="6e5ff-181">% of rooms that are open</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-182">3%</span><span class="sxs-lookup"><span data-stu-id="6e5ff-182">3%</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-183">3%</span><span class="sxs-lookup"><span data-stu-id="6e5ff-183">3%</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-184">50%</span><span class="sxs-lookup"><span data-stu-id="6e5ff-184">50%</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e5ff-185">オープン ルーム数 (明示的なメンバーシップなし)</span><span class="sxs-lookup"><span data-stu-id="6e5ff-185">Open rooms (no explicit membership)</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-186">960</span><span class="sxs-lookup"><span data-stu-id="6e5ff-186">960</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-187">32</span><span class="sxs-lookup"><span data-stu-id="6e5ff-187">32</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-188">5</span><span class="sxs-lookup"><span data-stu-id="6e5ff-188">5</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-189">997</span><span class="sxs-lookup"><span data-stu-id="6e5ff-189">997</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e5ff-190">非オープン ルーム数 (明示的なメンバーシップがある通常のルーム)</span><span class="sxs-lookup"><span data-stu-id="6e5ff-190">Non-open rooms (regular rooms with explicit membership)</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-191">31,040</span><span class="sxs-lookup"><span data-stu-id="6e5ff-191">31,040</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-192">1.035</span><span class="sxs-lookup"><span data-stu-id="6e5ff-192">1.035</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-193">5</span><span class="sxs-lookup"><span data-stu-id="6e5ff-193">5</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-194">32,080</span><span class="sxs-lookup"><span data-stu-id="6e5ff-194">32,080</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e5ff-195">大会議室数 (追加の発表者エントリ)</span><span class="sxs-lookup"><span data-stu-id="6e5ff-195">Auditorium rooms (additional presenters entry)</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-196">0</span><span class="sxs-lookup"><span data-stu-id="6e5ff-196">0</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-197">32</span><span class="sxs-lookup"><span data-stu-id="6e5ff-197">32</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-198">5</span><span class="sxs-lookup"><span data-stu-id="6e5ff-198">5</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e5ff-199">直接メンバーシップによって管理されるルーム</span><span class="sxs-lookup"><span data-stu-id="6e5ff-199">Rooms managed by direct membership</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-200">50%</span><span class="sxs-lookup"><span data-stu-id="6e5ff-200">50%</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-201">10%</span><span class="sxs-lookup"><span data-stu-id="6e5ff-201">10%</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-202">0%</span><span class="sxs-lookup"><span data-stu-id="6e5ff-202">0%</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e5ff-203">ユーザー グループによって管理されるルーム</span><span class="sxs-lookup"><span data-stu-id="6e5ff-203">Rooms managed by user groups</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-204">50%</span><span class="sxs-lookup"><span data-stu-id="6e5ff-204">50%</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-205">90%</span><span class="sxs-lookup"><span data-stu-id="6e5ff-205">90%</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-206">100%</span><span class="sxs-lookup"><span data-stu-id="6e5ff-206">100%</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e5ff-207">各チャット ルームのメンバーシップ一覧におけるユーザー グループ数 (オープン ルーム (明示的には指定されていない))</span><span class="sxs-lookup"><span data-stu-id="6e5ff-207">User groups in each chat room's membership list for open rooms (not specified explicitly)</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-208">0</span><span class="sxs-lookup"><span data-stu-id="6e5ff-208">0</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-209">0</span><span class="sxs-lookup"><span data-stu-id="6e5ff-209">0</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-210">0</span><span class="sxs-lookup"><span data-stu-id="6e5ff-210">0</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e5ff-211">各チャット ルームのメンバーシップ一覧におけるユーザー数 (非オープン ルーム)</span><span class="sxs-lookup"><span data-stu-id="6e5ff-211">Users in each chat room's membership list for non-open rooms</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-212">求める</span><span class="sxs-lookup"><span data-stu-id="6e5ff-212">30</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-213">150</span><span class="sxs-lookup"><span data-stu-id="6e5ff-213">150</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-214">16,000</span><span class="sxs-lookup"><span data-stu-id="6e5ff-214">16,000</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e5ff-215">各チャット ルームのメンバーシップ一覧におけるユーザー グループ数 (非オープン ルーム)</span><span class="sxs-lookup"><span data-stu-id="6e5ff-215">User groups in each chat room's membership list for non-open rooms</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-216">3</span><span class="sxs-lookup"><span data-stu-id="6e5ff-216">3</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-217">5</span><span class="sxs-lookup"><span data-stu-id="6e5ff-217">5</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-218">常用</span><span class="sxs-lookup"><span data-stu-id="6e5ff-218">10</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e5ff-219">各チャット ルームのマネージャー一覧におけるユーザーおよびユーザー グループ数 (オープン ルームと非オープン ルーム)</span><span class="sxs-lookup"><span data-stu-id="6e5ff-219">Users and user groups in each chat room's manager list (for open and non-open rooms)</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-220">6</span><span class="sxs-lookup"><span data-stu-id="6e5ff-220">6</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-221">6</span><span class="sxs-lookup"><span data-stu-id="6e5ff-221">6</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-222">6</span><span class="sxs-lookup"><span data-stu-id="6e5ff-222">6</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e5ff-223">各大会議室のチャット ルームの発表者一覧におけるユーザーおよびユーザー グループ数 (オープン ルームと非オープン ルーム)</span><span class="sxs-lookup"><span data-stu-id="6e5ff-223">Users and user groups in each auditorium chat room's presenters list (for open and non-open rooms)</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-224">6</span><span class="sxs-lookup"><span data-stu-id="6e5ff-224">6</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-225">6</span><span class="sxs-lookup"><span data-stu-id="6e5ff-225">6</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-226">6</span><span class="sxs-lookup"><span data-stu-id="6e5ff-226">6</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e5ff-227">すべての非オープン ルームにおけるユーザー ベースのメンバーシップ エンティティ数</span><span class="sxs-lookup"><span data-stu-id="6e5ff-227">User-based membership entities across all non-open rooms</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-228">465,600</span><span class="sxs-lookup"><span data-stu-id="6e5ff-228">465,600</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-229">15,520</span><span class="sxs-lookup"><span data-stu-id="6e5ff-229">15,520</span></span></p></td>
<td><p>-</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e5ff-230">すべての非オープン ルームにおけるユーザー グループ ベースのメンバーシップ エンティティ数</span><span class="sxs-lookup"><span data-stu-id="6e5ff-230">User-group-based membership entities across all non-open rooms</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-231">46,560</span><span class="sxs-lookup"><span data-stu-id="6e5ff-231">46,560</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-232">4656</span><span class="sxs-lookup"><span data-stu-id="6e5ff-232">4656</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-233">50</span><span class="sxs-lookup"><span data-stu-id="6e5ff-233">50</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e5ff-234">すべての大会議室のチャット ルームにおけるユーザーおよびユーザー グループ ベースのエンティティ数</span><span class="sxs-lookup"><span data-stu-id="6e5ff-234">Users and user groups based entities across all auditorium chat rooms</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-235">0</span><span class="sxs-lookup"><span data-stu-id="6e5ff-235">0</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-236">192</span><span class="sxs-lookup"><span data-stu-id="6e5ff-236">192</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-237">50</span><span class="sxs-lookup"><span data-stu-id="6e5ff-237">50</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e5ff-238">すべてのチャット ルーム マネージャー一覧におけるユーザーおよびユーザー グループ ベースのマネージャー エンティティ数</span><span class="sxs-lookup"><span data-stu-id="6e5ff-238">Users and user groups based manager entities across all chat rooms manager lists</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-239">192,000</span><span class="sxs-lookup"><span data-stu-id="6e5ff-239">192,000</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-240">6,400</span><span class="sxs-lookup"><span data-stu-id="6e5ff-240">6,400</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-241">60</span><span class="sxs-lookup"><span data-stu-id="6e5ff-241">60</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e5ff-242">チャット ルームあたりのアクティブ ユーザー</span><span class="sxs-lookup"><span data-stu-id="6e5ff-242">Active users per chat room</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-243"><em>求める</em></span><span class="sxs-lookup"><span data-stu-id="6e5ff-243"><em>30</em></span></span></p></td>
<td><p><span data-ttu-id="6e5ff-244"><em>150</em></span><span class="sxs-lookup"><span data-stu-id="6e5ff-244"><em>150</em></span></span></p></td>
<td><p><span data-ttu-id="6e5ff-245"><em>16,000</em></span><span class="sxs-lookup"><span data-stu-id="6e5ff-245"><em>16,000</em></span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e5ff-246">ユーザーあたりのチャット ルーム</span><span class="sxs-lookup"><span data-stu-id="6e5ff-246">Chat rooms per user</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-247"><em>以内</em></span><span class="sxs-lookup"><span data-stu-id="6e5ff-247"><em>12</em></span></span></p></td>
<td><p><span data-ttu-id="6e5ff-248"><em>2</em></span><span class="sxs-lookup"><span data-stu-id="6e5ff-248"><em>2</em></span></span></p></td>
<td><p><span data-ttu-id="6e5ff-249"><em>2</em></span><span class="sxs-lookup"><span data-stu-id="6e5ff-249"><em>2</em></span></span></p></td>
<td><p><span data-ttu-id="6e5ff-250"><em>16</em></span><span class="sxs-lookup"><span data-stu-id="6e5ff-250"><em>16</em></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e5ff-251">各チャット ルームのメンバーシップ リストのユーザー グループ</span><span class="sxs-lookup"><span data-stu-id="6e5ff-251">User groups in each chat room’s membership list</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-252"><em>常用</em></span><span class="sxs-lookup"><span data-stu-id="6e5ff-252"><em>10</em></span></span></p></td>
<td><p><span data-ttu-id="6e5ff-253"><em>常用</em></span><span class="sxs-lookup"><span data-stu-id="6e5ff-253"><em>10</em></span></span></p></td>
<td><p><span data-ttu-id="6e5ff-254"><em>マート</em></span><span class="sxs-lookup"><span data-stu-id="6e5ff-254"><em>15</em></span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e5ff-255">ユーザー グループによって管理されるルーム</span><span class="sxs-lookup"><span data-stu-id="6e5ff-255">Rooms managed by user groups</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-256"><em>50%</em></span><span class="sxs-lookup"><span data-stu-id="6e5ff-256"><em>50%</em></span></span></p></td>
<td><p><span data-ttu-id="6e5ff-257"><em>50%</em></span><span class="sxs-lookup"><span data-stu-id="6e5ff-257"><em>50%</em></span></span></p></td>
<td><p><span data-ttu-id="6e5ff-258"><em>50%</em></span><span class="sxs-lookup"><span data-stu-id="6e5ff-258"><em>50%</em></span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e5ff-259">すべてのチャット ルームのユーザー グループ ベースのメンバーシップ エンティティ</span><span class="sxs-lookup"><span data-stu-id="6e5ff-259">User-group-based membership entities across all chat rooms</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-260">155,200</span><span class="sxs-lookup"><span data-stu-id="6e5ff-260">155,200</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-261">5173</span><span class="sxs-lookup"><span data-stu-id="6e5ff-261">5173</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-262">68</span><span class="sxs-lookup"><span data-stu-id="6e5ff-262">68</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e5ff-263">すべてのチャット ルームのユーザー ベースのメンバーシップ エンティティ</span><span class="sxs-lookup"><span data-stu-id="6e5ff-263">User-based membership entities across all chat rooms</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-264">465,600</span><span class="sxs-lookup"><span data-stu-id="6e5ff-264">465,600</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-265">77,600</span><span class="sxs-lookup"><span data-stu-id="6e5ff-265">77,600</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-266">72,000</span><span class="sxs-lookup"><span data-stu-id="6e5ff-266">72,000</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e5ff-267">各チャット ルームのマネージャーの一覧、発表者の一覧、およびスコープの一覧のユーザーおよびユーザー グループ</span><span class="sxs-lookup"><span data-stu-id="6e5ff-267">Users and user groups in each chat room's manager, presenter, and scope lists</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-268">6</span><span class="sxs-lookup"><span data-stu-id="6e5ff-268">6</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-269">6</span><span class="sxs-lookup"><span data-stu-id="6e5ff-269">6</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-270">6</span><span class="sxs-lookup"><span data-stu-id="6e5ff-270">6</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e5ff-271">すべてのチャット ルームのマネージャーの一覧、発表者の一覧、およびスコープの一覧のユーザーおよびユーザー グループ</span><span class="sxs-lookup"><span data-stu-id="6e5ff-271">Users and user groups across all chat rooms' manager, presenter, and scope lists</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-272">192,000</span><span class="sxs-lookup"><span data-stu-id="6e5ff-272">192,000</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-273">6400</span><span class="sxs-lookup"><span data-stu-id="6e5ff-273">6400</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-274">60</span><span class="sxs-lookup"><span data-stu-id="6e5ff-274">60</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e5ff-275">アクセス制御エントリ</span><span class="sxs-lookup"><span data-stu-id="6e5ff-275">Access control entries</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-276">704,160</span><span class="sxs-lookup"><span data-stu-id="6e5ff-276">704,160</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-277">26,768</span><span class="sxs-lookup"><span data-stu-id="6e5ff-277">26,768</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-278">160</span><span class="sxs-lookup"><span data-stu-id="6e5ff-278">160</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-279">731,088</span><span class="sxs-lookup"><span data-stu-id="6e5ff-279">731,088</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e5ff-280">最大アクセス制御エントリ</span><span class="sxs-lookup"><span data-stu-id="6e5ff-280">Maximum access control entries</span></span></p></td>
<td></td>
<td></td>
<td></td>
<td><p><span data-ttu-id="6e5ff-281">2,000,000</span><span class="sxs-lookup"><span data-stu-id="6e5ff-281">2,000,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6e5ff-282">上記のサンプルでは、推奨されるガイドラインに従って常設チャットサーバーを展開すると、コンプライアンスが有効になっている4台のサーバープールで最大8万のアクティブユーザーを処理することができます。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-282">In the preceding sample, when you deploy the Persistent Chat Servers according to the recommended guidelines, they can handle up to 80,000 active users across a four-server pool with compliance enabled.</span></span>

<span data-ttu-id="6e5ff-283">このサンプルは、小規模 (常時 30 のアクティブ ユーザー)、中規模 (150 のアクティブ ユーザー)、および大規模 (16,000 のアクティブ ユーザー) として分類されたチャット ルームを示しています。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-283">This sample shows chat rooms categorized as small (30 active users at any given time), medium (150 active users), and large (16,000 active users).</span></span> <span data-ttu-id="6e5ff-284">特定のサイズのチャットルームの数は、次の合計数に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-284">The number of chat rooms of a certain size is computed based on the total number of:</span></span>

  - <span data-ttu-id="6e5ff-285">システム内のアクティブ ユーザー</span><span class="sxs-lookup"><span data-stu-id="6e5ff-285">Active users in the system</span></span>

  - <span data-ttu-id="6e5ff-286">特定のサイズのチャット ルームのアクティブ ユーザー</span><span class="sxs-lookup"><span data-stu-id="6e5ff-286">Active users in chat rooms of the given size</span></span>

  - <span data-ttu-id="6e5ff-287">単一ユーザーが参加する特定のサイズのチャット ルーム</span><span class="sxs-lookup"><span data-stu-id="6e5ff-287">Chat rooms of the given size that a single user joins</span></span>

<span data-ttu-id="6e5ff-p111">上記の処理能力の計画表では、各チャット ルームについて、チャット ルームに直接割り当てられたエントリなど、チャット ルームに関連付けられたアクセス制御エントリの数を示しています。アクセス制御リスト (ACL) を使用して、個々のチャット ルームへのアクセスを制御できます。また、カテゴリ レベルでアクセスを制御することもできます。ACL では、個々のアクセス制御エントリは、ユーザー グループ (セキュリティ グループ、配布リストなど) または単一ユーザーのどちらかになります。アクセス制御エントリは、チャット ルームのマネージャー、発表者、およびメンバーに対して定義できます。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-p111">For each chat room, the preceding capacity planning table specifies the number of access control entries that are associated with the chat room, including entries that are assigned directly to the chat room. You can control access to individual chat rooms by using access control lists (ACLs). You can also control access at the category level. In an ACL, an individual access control entry can be either a user group—for example, a security group, a distribution list, or a single user. You can define access control entries for chat room managers, presenters, and members.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="6e5ff-p112">チャット ルームの管理戦略を計画する際に、許容されるアクセス制御エントリの合計数は 200 万であることに注意してください。計算されたアクセス制御エントリが 200 万を超える場合は、サーバーのパフォーマンスが大幅に低下する可能性があります。この問題を可能な限り回避するには、アクセス制御エントリが個々のユーザーではなくユーザー グループとなるようにします。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-p112">In planning your strategy for managing chat rooms, keep in mind that the total number of allowed access control entries is 2 million. If the calculated access control entries exceed 2 million, server performance could degrade significantly. To avoid this issue, whenever possible, be sure that your access control entries are user groups instead of individual users.</span></span>



</div>

</div>

<div>

## <a name="capacity-planning-for-managing-chat-room-access-by-invitation"></a><span data-ttu-id="6e5ff-296">招待によってチャットルームへのアクセスを管理するためのキャパシティ計画</span><span class="sxs-lookup"><span data-stu-id="6e5ff-296">Capacity Planning for Managing Chat Room Access by Invitation</span></span>

<span data-ttu-id="6e5ff-297">次のキャパシティ計画の表を使用して、招待状を送信するように構成されている場合に、常設チャットサーバーによって作成および保存される招待状の数を理解することができます。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-297">You can use the following capacity planning table to understand the number of invitations that Persistent Chat Server creates and stores in the Persistent Chat database when it is configured to send invitations.</span></span> <span data-ttu-id="6e5ff-298">カテゴリの招待を管理するには、Lync Server コントロールパネルの [ **チャットルームのカテゴリ設定** ] ページを使用するか、または Windows PowerShell コマンドレット **csPersistentChatCategory** を使用します。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-298">You manage invitations on the Category by using the **Chat Room Category settings** page in the Lync Server Control Panel, or by using the Windows PowerShell cmdlet, **set-csPersistentChatCategory**.</span></span> <span data-ttu-id="6e5ff-299">Lync クライアントから起動した [会議室の **管理** ] ページ、または Windows PowerShell コマンドレット **csPersistentChatRoom** を使用して、チャットルームの招待を管理することができます。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-299">You can manage invitations on a chat room (in line with what the category allows) by using the **Room Management** page launched from the Lync client, or by using a Windows PowerShell cmdlet, **set-csPersistentChatRoom**.</span></span>

<span data-ttu-id="6e5ff-300">次の表のサンプル データでは、[**チャット ルームの設定**] ページの [**招待**] オプションがすべてのチャット ルームの 50 パーセントで [**はい**] に設定されていることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-300">The sample data in the following table assumes that, on the **Chat room settings** page for 50 percent of all chat rooms, the **Invitations** option is set to **Yes**.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="6e5ff-301">サーバーによって生成された招待の数の計算値が 100 万を超えると、サーバーのパフォーマンスが大幅に低下する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-301">If the calculated value for the number of invitations that is generated by the server exceeds 1 million, server performance could degrade significantly.</span></span> <span data-ttu-id="6e5ff-302">この問題を回避するには、招待を送信するように構成されているチャットルームの数を最小化するか、招待状を送信するように設定されているチャットルームに参加できるユーザー数を制限してください。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-302">To avoid this issue, be sure that you minimize the number of chat rooms that are configured to send invitations or restrict the number of users who can join chat rooms that have been configured to send invitations.</span></span>



</div>

### <a name="chat-room-access-by-invitation-sample"></a><span data-ttu-id="6e5ff-303">招待によるチャットルームへのアクセスのサンプル</span><span class="sxs-lookup"><span data-stu-id="6e5ff-303">Chat Room Access by Invitation Sample</span></span>

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
<th></th>
<th><span data-ttu-id="6e5ff-304">小規模チャット ルーム</span><span class="sxs-lookup"><span data-stu-id="6e5ff-304">Small Chat Rooms</span></span></th>
<th><span data-ttu-id="6e5ff-305">中規模チャット ルーム</span><span class="sxs-lookup"><span data-stu-id="6e5ff-305">Medium Chat Rooms</span></span></th>
<th><span data-ttu-id="6e5ff-306">大規模チャット ルーム</span><span class="sxs-lookup"><span data-stu-id="6e5ff-306">Large Chat Rooms</span></span></th>
<th><span data-ttu-id="6e5ff-307">合計</span><span class="sxs-lookup"><span data-stu-id="6e5ff-307">Total</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6e5ff-308">チャット ルームにアクセスできるユーザー数</span><span class="sxs-lookup"><span data-stu-id="6e5ff-308">Users who can access chat room</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-309">ルームあたり 30 ユーザー</span><span class="sxs-lookup"><span data-stu-id="6e5ff-309">30 per room</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-310">ルームあたり 150 ユーザー</span><span class="sxs-lookup"><span data-stu-id="6e5ff-310">150 per room</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-311">ルームあたり 16,000 ユーザー</span><span class="sxs-lookup"><span data-stu-id="6e5ff-311">16,000 per room</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e5ff-312">招待があるルームの割合</span><span class="sxs-lookup"><span data-stu-id="6e5ff-312">Percentage of rooms that have invitations</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-313">50%</span><span class="sxs-lookup"><span data-stu-id="6e5ff-313">50%</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-314">50%</span><span class="sxs-lookup"><span data-stu-id="6e5ff-314">50%</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-315">50%</span><span class="sxs-lookup"><span data-stu-id="6e5ff-315">50%</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e5ff-316">招待を送信するように構成されているチャット ルーム</span><span class="sxs-lookup"><span data-stu-id="6e5ff-316">Chat rooms configured to send invitations</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-317"><em>16,000</em></span><span class="sxs-lookup"><span data-stu-id="6e5ff-317"><em>16,000</em></span></span></p></td>
<td><p><span data-ttu-id="6e5ff-318"><em>533</em></span><span class="sxs-lookup"><span data-stu-id="6e5ff-318"><em>533</em></span></span></p></td>
<td><p><span data-ttu-id="6e5ff-319"><em>5</em></span><span class="sxs-lookup"><span data-stu-id="6e5ff-319"><em>5</em></span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e5ff-320">チャット ルームにアクセスできるユーザー</span><span class="sxs-lookup"><span data-stu-id="6e5ff-320">Users who can access the chat room</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-321"><em>60</em></span><span class="sxs-lookup"><span data-stu-id="6e5ff-321"><em>60</em></span></span></p></td>
<td><p><span data-ttu-id="6e5ff-322"><em>225</em></span><span class="sxs-lookup"><span data-stu-id="6e5ff-322"><em>225</em></span></span></p></td>
<td><p><span data-ttu-id="6e5ff-323"><em>16,000</em></span><span class="sxs-lookup"><span data-stu-id="6e5ff-323"><em>16,000</em></span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e5ff-324">常設チャットサーバーによって生成された招待状</span><span class="sxs-lookup"><span data-stu-id="6e5ff-324">Invitations generated by Persistent Chat Server</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-325">960,000</span><span class="sxs-lookup"><span data-stu-id="6e5ff-325">960,000</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-326">120,000</span><span class="sxs-lookup"><span data-stu-id="6e5ff-326">120,000</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-327">80,000</span><span class="sxs-lookup"><span data-stu-id="6e5ff-327">80,000</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-328">1,160,000</span><span class="sxs-lookup"><span data-stu-id="6e5ff-328">1,160,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e5ff-329">招待の上限数</span><span class="sxs-lookup"><span data-stu-id="6e5ff-329">Maximum allowable number of invitations</span></span></p></td>
<td></td>
<td></td>
<td></td>
<td><p><span data-ttu-id="6e5ff-330">2,000,000</span><span class="sxs-lookup"><span data-stu-id="6e5ff-330">2,000,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e5ff-331">モデル 1 - 1 日、1 ルームあたりの想定メッセージ数で開始</span><span class="sxs-lookup"><span data-stu-id="6e5ff-331">Model 1 - Start with expected number of messages per room per day</span></span></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e5ff-332">ルームあたりのチャット レート (1 日あたり)</span><span class="sxs-lookup"><span data-stu-id="6e5ff-332">Chat Rate Per Room (per day)</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-333">50</span><span class="sxs-lookup"><span data-stu-id="6e5ff-333">50</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-334">500</span><span class="sxs-lookup"><span data-stu-id="6e5ff-334">500</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-335">100</span><span class="sxs-lookup"><span data-stu-id="6e5ff-335">100</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-336">650</span><span class="sxs-lookup"><span data-stu-id="6e5ff-336">650</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e5ff-337">すべてのチャット ルームにおけるチャット レート (1 秒あたり)</span><span class="sxs-lookup"><span data-stu-id="6e5ff-337">Chat rate (per second) across all rooms</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-338">55.56</span><span class="sxs-lookup"><span data-stu-id="6e5ff-338">55.56</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-339">18.52</span><span class="sxs-lookup"><span data-stu-id="6e5ff-339">18.52</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-340">0.03</span><span class="sxs-lookup"><span data-stu-id="6e5ff-340">0.03</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-341">74</span><span class="sxs-lookup"><span data-stu-id="6e5ff-341">74</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e5ff-342">モデル 2 - 1 日、1 ユーザーあたりの投稿メッセージ数で開始</span><span class="sxs-lookup"><span data-stu-id="6e5ff-342">Model 2 - Start with number of messages posted per user per day</span></span></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e5ff-343">ユーザーあたりのチャット レート (1 日あたり)</span><span class="sxs-lookup"><span data-stu-id="6e5ff-343">Chat rate per user per day</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-344">マート</span><span class="sxs-lookup"><span data-stu-id="6e5ff-344">15</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-345">5</span><span class="sxs-lookup"><span data-stu-id="6e5ff-345">5</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-346">0.1</span><span class="sxs-lookup"><span data-stu-id="6e5ff-346">0.1</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-347">超える</span><span class="sxs-lookup"><span data-stu-id="6e5ff-347">20</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e5ff-348">ルームあたりのチャット レート (1 日あたり)</span><span class="sxs-lookup"><span data-stu-id="6e5ff-348">Chat rate per room (per day)</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-349">38</span><span class="sxs-lookup"><span data-stu-id="6e5ff-349">38</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-350">375</span><span class="sxs-lookup"><span data-stu-id="6e5ff-350">375</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-351">800</span><span class="sxs-lookup"><span data-stu-id="6e5ff-351">800</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-352">1,213</span><span class="sxs-lookup"><span data-stu-id="6e5ff-352">1,213</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e5ff-353">すべてのチャット ルームにおけるチャット レート (1 秒あたり)</span><span class="sxs-lookup"><span data-stu-id="6e5ff-353">Chat rate (per second) across all rooms</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-354">41.67</span><span class="sxs-lookup"><span data-stu-id="6e5ff-354">41.67</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-355">13.89</span><span class="sxs-lookup"><span data-stu-id="6e5ff-355">13.89</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-356">0.28</span><span class="sxs-lookup"><span data-stu-id="6e5ff-356">0.28</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-357">56</span><span class="sxs-lookup"><span data-stu-id="6e5ff-357">56</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="persistent-chat-server-performance-user-model"></a><span data-ttu-id="6e5ff-358">常設チャットサーバーのパフォーマンスユーザーモデル</span><span class="sxs-lookup"><span data-stu-id="6e5ff-358">Persistent Chat Server Performance User Model</span></span>

<span data-ttu-id="6e5ff-359">次の表では、常設チャットサーバーのユーザーモデルについて説明します。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-359">The following table describes the user model for Persistent Chat Server.</span></span> <span data-ttu-id="6e5ff-360">この表は、処理能力の計画の要件に関する基礎を提供し、4 台のサーバーで同時に 80,000 のユーザーに対処できる一般的な組織を表しています。</span><span class="sxs-lookup"><span data-stu-id="6e5ff-360">It provides the basis for the capacity planning requirements and represents a typical organization with 80,000 concurrent users on four servers.</span></span>

### <a name="persistent-chat-server-performance-user-model"></a><span data-ttu-id="6e5ff-361">常設チャットサーバーのパフォーマンスユーザーモデル</span><span class="sxs-lookup"><span data-stu-id="6e5ff-361">Persistent Chat Server Performance User Model</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6e5ff-362">アクティブな接続ユーザー数</span><span class="sxs-lookup"><span data-stu-id="6e5ff-362">Number of active users connected</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-363">80,000</span><span class="sxs-lookup"><span data-stu-id="6e5ff-363">80,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e5ff-364">常設チャットサーバーサービスインスタンスの数</span><span class="sxs-lookup"><span data-stu-id="6e5ff-364">Number of Persistent Chat Server service instances</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-365">4</span><span class="sxs-lookup"><span data-stu-id="6e5ff-365">4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e5ff-366">小規模チャット ルームのサイズ</span><span class="sxs-lookup"><span data-stu-id="6e5ff-366">Size of small chat rooms</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-367">30 ユーザー</span><span class="sxs-lookup"><span data-stu-id="6e5ff-367">30 users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e5ff-368">中規模チャット ルームのサイズ</span><span class="sxs-lookup"><span data-stu-id="6e5ff-368">Size of medium chat rooms</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-369">150 ユーザー</span><span class="sxs-lookup"><span data-stu-id="6e5ff-369">150 users</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e5ff-370">大規模チャット ルームのサイズ</span><span class="sxs-lookup"><span data-stu-id="6e5ff-370">Size of large chat rooms</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-371">16,000 ユーザー</span><span class="sxs-lookup"><span data-stu-id="6e5ff-371">16,000 users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e5ff-372">チャット ルームの合計数</span><span class="sxs-lookup"><span data-stu-id="6e5ff-372">Total number of chat rooms</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-373">33,077</span><span class="sxs-lookup"><span data-stu-id="6e5ff-373">33,077</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e5ff-374">小規模チャット ルームの数</span><span class="sxs-lookup"><span data-stu-id="6e5ff-374">Number of small chat rooms</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-375">32,000</span><span class="sxs-lookup"><span data-stu-id="6e5ff-375">32,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e5ff-376">中規模チャット ルームの数</span><span class="sxs-lookup"><span data-stu-id="6e5ff-376">Number of medium chat rooms</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-377">1,067</span><span class="sxs-lookup"><span data-stu-id="6e5ff-377">1,067</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e5ff-378">大規模チャット ルームの数</span><span class="sxs-lookup"><span data-stu-id="6e5ff-378">Number of large chat rooms</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-379">常用</span><span class="sxs-lookup"><span data-stu-id="6e5ff-379">10</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e5ff-380">ユーザーあたりのチャット ルームの合計数</span><span class="sxs-lookup"><span data-stu-id="6e5ff-380">Total number of chat rooms per user</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-381">16</span><span class="sxs-lookup"><span data-stu-id="6e5ff-381">16</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e5ff-382">ユーザーあたりの小規模チャット ルームの数</span><span class="sxs-lookup"><span data-stu-id="6e5ff-382">Number of small chat rooms per user</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-383">以内</span><span class="sxs-lookup"><span data-stu-id="6e5ff-383">12</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e5ff-384">ユーザーあたりの中規模チャット ルームの数</span><span class="sxs-lookup"><span data-stu-id="6e5ff-384">Number of medium chat rooms per user</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-385">2</span><span class="sxs-lookup"><span data-stu-id="6e5ff-385">2</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e5ff-386">ユーザーあたりの大規模チャット ルームの数</span><span class="sxs-lookup"><span data-stu-id="6e5ff-386">Number of large chat rooms per user</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-387">2</span><span class="sxs-lookup"><span data-stu-id="6e5ff-387">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e5ff-388">ユーザーあたりの参加ルーム数</span><span class="sxs-lookup"><span data-stu-id="6e5ff-388">Number of rooms joined per user</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-389">24</span><span class="sxs-lookup"><span data-stu-id="6e5ff-389">24</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e5ff-390">ピーク時の参加レート</span><span class="sxs-lookup"><span data-stu-id="6e5ff-390">Peak join rate</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-391">10/秒</span><span class="sxs-lookup"><span data-stu-id="6e5ff-391">10/second</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e5ff-392">チャット レート合計</span><span class="sxs-lookup"><span data-stu-id="6e5ff-392">Total chat rate</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-393">24/秒</span><span class="sxs-lookup"><span data-stu-id="6e5ff-393">24/second</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e5ff-394">小規模チャット ルームのチャット レート</span><span class="sxs-lookup"><span data-stu-id="6e5ff-394">Chat rate for small chat rooms</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-395">22.22/second</span><span class="sxs-lookup"><span data-stu-id="6e5ff-395">22.22/second</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e5ff-396">中規模チャット ルームのチャット レート</span><span class="sxs-lookup"><span data-stu-id="6e5ff-396">Chat rate for medium chat rooms</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-397">1.67/second</span><span class="sxs-lookup"><span data-stu-id="6e5ff-397">1.67/second</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e5ff-398">大規模チャット ルームのチャット レート</span><span class="sxs-lookup"><span data-stu-id="6e5ff-398">Chat rate for large chat rooms</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-399">~0.15/second</span><span class="sxs-lookup"><span data-stu-id="6e5ff-399">~0.15/second</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e5ff-400">招待が構成されているチャット ルームの割合</span><span class="sxs-lookup"><span data-stu-id="6e5ff-400">Percentage of chat rooms configured for invitations</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-401">50%</span><span class="sxs-lookup"><span data-stu-id="6e5ff-401">50%</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e5ff-402">直接メンバーシップの割合</span><span class="sxs-lookup"><span data-stu-id="6e5ff-402">Percentage of direct memberships</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-403">50%</span><span class="sxs-lookup"><span data-stu-id="6e5ff-403">50%</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e5ff-404">グループ メンバーシップの割合</span><span class="sxs-lookup"><span data-stu-id="6e5ff-404">Percentage of group memberships</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-405">50%</span><span class="sxs-lookup"><span data-stu-id="6e5ff-405">50%</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e5ff-406">Active Directory ドメインサービスの親所属の平均数</span><span class="sxs-lookup"><span data-stu-id="6e5ff-406">Average number of ancestor affiliations in Active Directory Domain Services</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-407">100 - 200</span><span class="sxs-lookup"><span data-stu-id="6e5ff-407">100 - 200</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e5ff-408">ユーザーごとの加入する連絡先の数</span><span class="sxs-lookup"><span data-stu-id="6e5ff-408">Number of subscribed contacts per user</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-409">80</span><span class="sxs-lookup"><span data-stu-id="6e5ff-409">80</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e5ff-410">ユーザーあたりの平均エンドポイント数</span><span class="sxs-lookup"><span data-stu-id="6e5ff-410">Average number of endpoints per user</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-411">1.5</span><span class="sxs-lookup"><span data-stu-id="6e5ff-411">1.5</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e5ff-412">エンドポイントあたりの表示されるチャット ルームの平均数</span><span class="sxs-lookup"><span data-stu-id="6e5ff-412">Average number of visible chat rooms per endpoint</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-413">1.5</span><span class="sxs-lookup"><span data-stu-id="6e5ff-413">1.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e5ff-414">ユーザーあたりの表示されるチャット ルームの平均数</span><span class="sxs-lookup"><span data-stu-id="6e5ff-414">Average number of visible chat rooms per user</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-415">2.25 (1 ルームと 2 ルームが 50% ずつ)。最大 6 ルームがオープン (1 モニターにつき 1 つ)</span><span class="sxs-lookup"><span data-stu-id="6e5ff-415">2.25 (50% for 1 room and 50% for 2 rooms); Up to 6 rooms open, one per monitor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e5ff-416">一定間隔でポーリングされる参加者の数</span><span class="sxs-lookup"><span data-stu-id="6e5ff-416">Number of participants polled per interval</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-417">25 (表示されるチャット ルーム 1 つあたり)</span><span class="sxs-lookup"><span data-stu-id="6e5ff-417">25 per visible chat room</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e5ff-418">ポーリング間隔の長さ</span><span class="sxs-lookup"><span data-stu-id="6e5ff-418">Length of polling interval</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-419">5 分</span><span class="sxs-lookup"><span data-stu-id="6e5ff-419">5 minutes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e5ff-420">1 秒あたりにポーリングされる参加者の数</span><span class="sxs-lookup"><span data-stu-id="6e5ff-420">Number of participants polled per second</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-421">15,000</span><span class="sxs-lookup"><span data-stu-id="6e5ff-421">15,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e5ff-422">1 時間あたりのユーザーごとのプレゼンス変更の数</span><span class="sxs-lookup"><span data-stu-id="6e5ff-422">Number of presence changes per hour per user</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-423">6</span><span class="sxs-lookup"><span data-stu-id="6e5ff-423">6</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e5ff-424">1 秒あたりのプレゼンス変更の数</span><span class="sxs-lookup"><span data-stu-id="6e5ff-424">Number of presence changes per second</span></span></p></td>
<td><p><span data-ttu-id="6e5ff-425">133.33</span><span class="sxs-lookup"><span data-stu-id="6e5ff-425">133.33</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="6e5ff-426">


</div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6e5ff-426">


</div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

