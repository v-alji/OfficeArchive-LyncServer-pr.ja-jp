---
title: 'Lync Server 2013: 内部サーバーのポートとプロトコル'
description: 'Lync Server 2013: 内部サーバーのポートとプロトコル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Ports and protocols for internal servers
ms:assetid: c94063f1-e802-4a61-be90-022fc185335e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398833(v=OCS.15)
ms:contentKeyID: 48185402
ms.date: 04/06/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d7d8f12c78c5dec5caacaeb1156f4d228b7cd591
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424248"
---
# <a name="ports-and-protocols-for-internal-servers-in-lync-server-2013"></a><span data-ttu-id="b59ab-103">Lync Server 2013 の内部サーバーのポートとプロトコル</span><span class="sxs-lookup"><span data-stu-id="b59ab-103">Ports and protocols for internal servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b59ab-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b59ab-104">

<span> </span></span></span>

<span data-ttu-id="b59ab-105">_**最終更新日:** 2016-04-06_</span><span class="sxs-lookup"><span data-stu-id="b59ab-105">_**Topic Last Modified:** 2016-04-06_</span></span>

<span data-ttu-id="b59ab-106">このセクションでは、Lync Server 展開のサーバー、ロードバランサー、クライアントで使用されるポートとプロトコルについて概要を説明します。</span><span class="sxs-lookup"><span data-stu-id="b59ab-106">This section summarizes the ports and protocols used by servers, load balancers, and clients in a Lync Server deployment.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="b59ab-107">Lync と Communicator クライアントが1対1の通信に関わる場合、ピアツーピアと呼ばれることがよくあります。</span><span class="sxs-lookup"><span data-stu-id="b59ab-107">Lync and Communicator clients when involved in a one to one communication, is often referred to as peer-to-peer.</span></span> <span data-ttu-id="b59ab-108">技術的には、2つのクライアントは1つの会話と1つの会話の間でやり取りされ、中央にはインスタントメッセージング multipoint コントロールユニット (IMMCU) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b59ab-108">Technically, the two clients are communicating in a one to one conversation, with the Instant Messaging multipoint control unit (IMMCU) in the middle.</span></span> <span data-ttu-id="b59ab-109">IMMCU は、フロントエンドサーバーのコンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="b59ab-109">The IMMCU is a component of Front End Server.</span></span> <span data-ttu-id="b59ab-110">必要な通信ワークフローに IMMCU を配置すると、フロントエンドサーバーが有効になっている通話の詳細の記録とその他の機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="b59ab-110">Placing the IMMCU in the required communication workflow allows call detail recording and other features that the Front End Server enables.</span></span> <span data-ttu-id="b59ab-111">通信は、クライアント上の動的ソースポートからフロントエンドサーバーポート TLS/TCP/5061 に送信されます (推奨トランスポート層セキュリティを使用していることを前提としています)。</span><span class="sxs-lookup"><span data-stu-id="b59ab-111">Communication is from a dynamic source port on the client to the Front End Server port TLS/TCP/5061 (assuming the use of the recommended transport layer security).</span></span> <span data-ttu-id="b59ab-112">設計上、ピアツーピア通信 (およびマルチパーティの IM) は、Lync Server と IMMCU がアクティブで利用可能な場合にのみ可能です。</span><span class="sxs-lookup"><span data-stu-id="b59ab-112">By design, peer-to-peer communication (as well as multi-party IM) is possible only when Lync Server and the IMMCU is active and available.</span></span>



</div>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="b59ab-113">ポートとプロトコルの詳細</span><span class="sxs-lookup"><span data-stu-id="b59ab-113">Port and Protocol Details</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b59ab-114">サーバー上で Lync Server サービスを開始する前に、Windows ファイアウォールが実行されている必要があります。そのため、Lync Server はファイアウォールで必要なポートを開くことになります。</span><span class="sxs-lookup"><span data-stu-id="b59ab-114">Windows Firewall must be running before you start the Lync Server services on a server, because that is when Lync Server opens the required ports in the firewall.</span></span>



</div>

<span data-ttu-id="b59ab-115">エッジコンポーネントのファイアウォール構成の詳細については、「 [Lync Server 2013 の外部の A/V ファイアウォールとポートの要件を確認](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b59ab-115">For details about firewall configuration for edge components, see [Determine external A/V firewall and port requirements for Lync Server 2013](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md).</span></span>

<span data-ttu-id="b59ab-116">次の表に、各内部サーバー役割で開く必要のあるポートの一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="b59ab-116">The following table lists the ports that need to be open on each internal server role.</span></span>

### <a name="required-server-ports-by-server-role"></a><span data-ttu-id="b59ab-117">必要なサーバー ポート (サーバー役割別)</span><span class="sxs-lookup"><span data-stu-id="b59ab-117">Required Server Ports (by Server Role)</span></span>

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
<th><span data-ttu-id="b59ab-118">サーバーの役割</span><span class="sxs-lookup"><span data-stu-id="b59ab-118">Server role</span></span></th>
<th><span data-ttu-id="b59ab-119">サービス名</span><span class="sxs-lookup"><span data-stu-id="b59ab-119">Service name</span></span></th>
<th><span data-ttu-id="b59ab-120">ポート</span><span class="sxs-lookup"><span data-stu-id="b59ab-120">Port</span></span></th>
<th><span data-ttu-id="b59ab-121">プロトコル</span><span class="sxs-lookup"><span data-stu-id="b59ab-121">Protocol</span></span></th>
<th><span data-ttu-id="b59ab-122">メモ</span><span class="sxs-lookup"><span data-stu-id="b59ab-122">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-123">すべてのサーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-123">All Servers</span></span></p></td>
<td><p><span data-ttu-id="b59ab-124">SQL ブラウザー</span><span class="sxs-lookup"><span data-stu-id="b59ab-124">SQL Browser</span></span></p></td>
<td><p><span data-ttu-id="b59ab-125">1434</span><span class="sxs-lookup"><span data-stu-id="b59ab-125">1434</span></span></p></td>
<td><p><span data-ttu-id="b59ab-126">UDP</span><span class="sxs-lookup"><span data-stu-id="b59ab-126">UDP</span></span></p></td>
<td><p><span data-ttu-id="b59ab-127">中央管理ストアデータベースのローカルでレプリケートされたコピーの SQL ブラウザー。</span><span class="sxs-lookup"><span data-stu-id="b59ab-127">SQL Browser for the local replicated copy of the Central Management Store database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-128">フロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-128">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b59ab-129">Lync Server Front-End サービス</span><span class="sxs-lookup"><span data-stu-id="b59ab-129">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="b59ab-130">5060</span><span class="sxs-lookup"><span data-stu-id="b59ab-130">5060</span></span></p></td>
<td><p><span data-ttu-id="b59ab-131">TCP</span><span class="sxs-lookup"><span data-stu-id="b59ab-131">TCP</span></span></p></td>
<td><p><span data-ttu-id="b59ab-132">リモート通話コントロール サーバーなどの Standard Edition サーバーとフロントエンド サーバーで、信頼されたサービスへの静的ルートの場合にオプションとして使用。</span><span class="sxs-lookup"><span data-stu-id="b59ab-132">Optionally used by Standard Edition servers and Front End Servers for static routes to trusted services, such as remote call control servers.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-133">フロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-133">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b59ab-134">Lync Server Front-End サービス</span><span class="sxs-lookup"><span data-stu-id="b59ab-134">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="b59ab-135">5061</span><span class="sxs-lookup"><span data-stu-id="b59ab-135">5061</span></span></p></td>
<td><p><span data-ttu-id="b59ab-136">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="b59ab-136">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="b59ab-137">サーバー間のすべての内部 SIP 通信 (MTLS)、サーバーとクライアントの間の SIP 通信 (TLS)、およびフロントエンド サーバーと仲介サーバーの間の SIP 通信 (MTLS) において、Standard Edition サーバーとフロントエンド プールで使用。</span><span class="sxs-lookup"><span data-stu-id="b59ab-137">Used by Standard Edition servers and Front End pools for all internal SIP communications between servers (MTLS), for SIP communications between Server and Client (TLS) and for SIP communications between Front End Servers and Mediation Servers (MTLS).</span></span> <span data-ttu-id="b59ab-138">監視サーバーとの通信にも使用されます。</span><span class="sxs-lookup"><span data-stu-id="b59ab-138">Also used for communications with Monitoring Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-139">フロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-139">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b59ab-140">Lync Server Front-End サービス</span><span class="sxs-lookup"><span data-stu-id="b59ab-140">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="b59ab-141">444</span><span class="sxs-lookup"><span data-stu-id="b59ab-141">444</span></span></p></td>
<td><p><span data-ttu-id="b59ab-142">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b59ab-142">HTTPS</span></span></p>
<p><span data-ttu-id="b59ab-143">TCP</span><span class="sxs-lookup"><span data-stu-id="b59ab-143">TCP</span></span></p></td>
<td><p><span data-ttu-id="b59ab-144">フォーカス (会議の状態を管理する Lync Server コンポーネント) と個々のサーバーの間の HTTPS 通信に使用されます。</span><span class="sxs-lookup"><span data-stu-id="b59ab-144">Used for HTTPS communication between the Focus (the Lync Server component that manages conference state) and the individual servers.</span></span></p>
<p><span data-ttu-id="b59ab-145">このポートは、Survivable Branch アプライアンスとフロントエンドサーバー間の TCP 通信にも使用されます。</span><span class="sxs-lookup"><span data-stu-id="b59ab-145">This port is also used for TCP communication between Survivable Branch Appliances and Front End Servers.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-146">フロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-146">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b59ab-147">Lync Server Front-End サービス</span><span class="sxs-lookup"><span data-stu-id="b59ab-147">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="b59ab-148">135</span><span class="sxs-lookup"><span data-stu-id="b59ab-148">135</span></span></p></td>
<td><p><span data-ttu-id="b59ab-149">DCOM およびリモート プロシージャ コール (RPC)</span><span class="sxs-lookup"><span data-stu-id="b59ab-149">DCOM and remote procedure call (RPC)</span></span></p></td>
<td><p><span data-ttu-id="b59ab-150">ユーザーの移行、ユーザー レプリケーター同期、およびアドレス帳同期などの DCOM ベースの操作で使用。</span><span class="sxs-lookup"><span data-stu-id="b59ab-150">Used for DCOM based operations such as Moving Users, User Replicator Synchronization, and Address Book Synchronization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-151">フロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-151">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b59ab-152">Lync Server IM 会議サービス</span><span class="sxs-lookup"><span data-stu-id="b59ab-152">Lync Server IM Conferencing service</span></span></p></td>
<td><p><span data-ttu-id="b59ab-153">5062</span><span class="sxs-lookup"><span data-stu-id="b59ab-153">5062</span></span></p></td>
<td><p><span data-ttu-id="b59ab-154">TCP</span><span class="sxs-lookup"><span data-stu-id="b59ab-154">TCP</span></span></p></td>
<td><p><span data-ttu-id="b59ab-155">インスタント メッセージング (IM) 会議の SIP 要求を受信するために使用。</span><span class="sxs-lookup"><span data-stu-id="b59ab-155">Used for incoming SIP requests for instant messaging (IM) conferencing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-156">フロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-156">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b59ab-157">Lync Server Web 会議サービス</span><span class="sxs-lookup"><span data-stu-id="b59ab-157">Lync Server Web Conferencing service</span></span></p></td>
<td><p><span data-ttu-id="b59ab-158">8057</span><span class="sxs-lookup"><span data-stu-id="b59ab-158">8057</span></span></p></td>
<td><p><span data-ttu-id="b59ab-159">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="b59ab-159">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="b59ab-160">クライアントからの PSOM (永続共有オブジェクト モデル) 接続をリッスンするために使用。</span><span class="sxs-lookup"><span data-stu-id="b59ab-160">Used to listen for Persistent Shared Object Model (PSOM) connections from client.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-161">フロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-161">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b59ab-162">Lync Server Web 会議互換サービス</span><span class="sxs-lookup"><span data-stu-id="b59ab-162">Lync Server Web Conferencing Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="b59ab-163">8058</span><span class="sxs-lookup"><span data-stu-id="b59ab-163">8058</span></span></p></td>
<td><p><span data-ttu-id="b59ab-164">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="b59ab-164">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="b59ab-165">Live Meeting クライアントと以前のバージョンの Lync Server からの永続的な共有オブジェクトモデル (PSOM) 接続をリッスンするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b59ab-165">Used to listen for Persistent Shared Object Model (PSOM) connections from the Live Meeting client and previous versions of Lync Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-166">フロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-166">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b59ab-167">Lync Server の音声/ビデオ会議サービス</span><span class="sxs-lookup"><span data-stu-id="b59ab-167">Lync Server Audio/Video Conferencing service</span></span></p></td>
<td><p><span data-ttu-id="b59ab-168">5063</span><span class="sxs-lookup"><span data-stu-id="b59ab-168">5063</span></span></p></td>
<td><p><span data-ttu-id="b59ab-169">TCP</span><span class="sxs-lookup"><span data-stu-id="b59ab-169">TCP</span></span></p></td>
<td><p><span data-ttu-id="b59ab-170">音声ビデオ会議の SIP 要求を受信するために使用。</span><span class="sxs-lookup"><span data-stu-id="b59ab-170">Used for incoming SIP requests for audio/video (A/V) conferencing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-171">フロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-171">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b59ab-172">Lync Server の音声/ビデオ会議サービス</span><span class="sxs-lookup"><span data-stu-id="b59ab-172">Lync Server Audio/Video Conferencing service</span></span></p></td>
<td><p><span data-ttu-id="b59ab-173">57501-65535</span><span class="sxs-lookup"><span data-stu-id="b59ab-173">57501-65535</span></span></p></td>
<td><p><span data-ttu-id="b59ab-174">TCP/UDP</span><span class="sxs-lookup"><span data-stu-id="b59ab-174">TCP/UDP</span></span></p></td>
<td><p><span data-ttu-id="b59ab-175">ビデオ会議で使用するメディア ポート範囲。</span><span class="sxs-lookup"><span data-stu-id="b59ab-175">Media port range used for video conferencing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-176">フロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-176">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b59ab-177">Lync Server Web 互換サービス</span><span class="sxs-lookup"><span data-stu-id="b59ab-177">Lync Server Web Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="b59ab-178">80</span><span class="sxs-lookup"><span data-stu-id="b59ab-178">80</span></span></p></td>
<td><p><span data-ttu-id="b59ab-179">HTTP</span><span class="sxs-lookup"><span data-stu-id="b59ab-179">HTTP</span></span></p></td>
<td><p><span data-ttu-id="b59ab-180">HTTPS が使用されない場合の、フロントエンド サーバーから Web ファーム FQDN (IIS Web コンポーネントで使用される URL) への通信に使用。</span><span class="sxs-lookup"><span data-stu-id="b59ab-180">Used for communication from Front End Servers to the web farm FQDNs (the URLs used by IIS web components) when HTTPS is not used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-181">フロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-181">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b59ab-182">Lync Server Web 互換サービス</span><span class="sxs-lookup"><span data-stu-id="b59ab-182">Lync Server Web Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="b59ab-183">443</span><span class="sxs-lookup"><span data-stu-id="b59ab-183">443</span></span></p></td>
<td><p><span data-ttu-id="b59ab-184">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b59ab-184">HTTPS</span></span></p></td>
<td><p><span data-ttu-id="b59ab-185">フロントエンド サーバーから Web ファーム FQDN (IIS Web コンポーネントで使用される URL) への通信に使用。</span><span class="sxs-lookup"><span data-stu-id="b59ab-185">Used for communication from Front End Servers to the web farm FQDNs (the URLs used by IIS web components).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-186">フロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-186">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b59ab-187">Lync Server Web 互換サービス</span><span class="sxs-lookup"><span data-stu-id="b59ab-187">Lync Server Web Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="b59ab-188">8080</span><span class="sxs-lookup"><span data-stu-id="b59ab-188">8080</span></span></p></td>
<td><p><span data-ttu-id="b59ab-189">TCP および HTTP</span><span class="sxs-lookup"><span data-stu-id="b59ab-189">TCP and HTTP</span></span></p></td>
<td><p><span data-ttu-id="b59ab-190">外部アクセスのために Web コンポーネントで使用。</span><span class="sxs-lookup"><span data-stu-id="b59ab-190">Used by web components for external access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-191">フロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-191">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b59ab-192">Web サーバー コンポーネント</span><span class="sxs-lookup"><span data-stu-id="b59ab-192">Web server component</span></span></p></td>
<td><p><span data-ttu-id="b59ab-193">4443</span><span class="sxs-lookup"><span data-stu-id="b59ab-193">4443</span></span></p></td>
<td><p><span data-ttu-id="b59ab-194">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b59ab-194">HTTPS</span></span></p></td>
<td><p><span data-ttu-id="b59ab-195">Autodiscover サインインのための HTTPS (リバース プロキシから) および HTTPS フロント エンドのプール間通信。</span><span class="sxs-lookup"><span data-stu-id="b59ab-195">HTTPS (from Reverse Proxy) and HTTPS Front End inter-pool communications for Autodiscover sign-in.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-196">フロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-196">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b59ab-197">Web サーバー コンポーネント</span><span class="sxs-lookup"><span data-stu-id="b59ab-197">Web server component</span></span></p></td>
<td><p><span data-ttu-id="b59ab-198">8060</span><span class="sxs-lookup"><span data-stu-id="b59ab-198">8060</span></span></p></td>
<td><p><span data-ttu-id="b59ab-199">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="b59ab-199">TCP (MTLS)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-200">フロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-200">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b59ab-201">Web サーバー コンポーネント</span><span class="sxs-lookup"><span data-stu-id="b59ab-201">Web server component</span></span></p></td>
<td><p><span data-ttu-id="b59ab-202">8061</span><span class="sxs-lookup"><span data-stu-id="b59ab-202">8061</span></span></p></td>
<td><p><span data-ttu-id="b59ab-203">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="b59ab-203">TCP (MTLS)</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-204">フロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-204">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b59ab-205">Mobility Service コンポーネント</span><span class="sxs-lookup"><span data-stu-id="b59ab-205">Mobility Services component</span></span></p></td>
<td><p><span data-ttu-id="b59ab-206">5086</span><span class="sxs-lookup"><span data-stu-id="b59ab-206">5086</span></span></p></td>
<td><p><span data-ttu-id="b59ab-207">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="b59ab-207">TCP (MTLS)</span></span></p></td>
<td><p><span data-ttu-id="b59ab-208">Mobility Service の内部プロセスに使用される SIP ポート。</span><span class="sxs-lookup"><span data-stu-id="b59ab-208">SIP port used by Mobility Services internal processes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-209">フロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-209">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b59ab-210">Mobility Service コンポーネント</span><span class="sxs-lookup"><span data-stu-id="b59ab-210">Mobility Services component</span></span></p></td>
<td><p><span data-ttu-id="b59ab-211">5087</span><span class="sxs-lookup"><span data-stu-id="b59ab-211">5087</span></span></p></td>
<td><p><span data-ttu-id="b59ab-212">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="b59ab-212">TCP (MTLS)</span></span></p></td>
<td><p><span data-ttu-id="b59ab-213">Mobility Service の内部プロセスに使用される SIP ポート。</span><span class="sxs-lookup"><span data-stu-id="b59ab-213">SIP port used by Mobility Services internal processes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-214">フロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-214">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b59ab-215">Mobility Service コンポーネント</span><span class="sxs-lookup"><span data-stu-id="b59ab-215">Mobility Services component</span></span></p></td>
<td><p><span data-ttu-id="b59ab-216">443</span><span class="sxs-lookup"><span data-stu-id="b59ab-216">443</span></span></p></td>
<td><p><span data-ttu-id="b59ab-217">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b59ab-217">HTTPS</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-218">フロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-218">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b59ab-219">Lync Server 会議アテンダントサービス (ダイヤルイン会議)</span><span class="sxs-lookup"><span data-stu-id="b59ab-219">Lync Server Conferencing Attendant service (dial-in conferencing)</span></span></p></td>
<td><p><span data-ttu-id="b59ab-220">5064</span><span class="sxs-lookup"><span data-stu-id="b59ab-220">5064</span></span></p></td>
<td><p><span data-ttu-id="b59ab-221">TCP</span><span class="sxs-lookup"><span data-stu-id="b59ab-221">TCP</span></span></p></td>
<td><p><span data-ttu-id="b59ab-222">ダイヤルイン会議の SIP 要求を受信するために使用。</span><span class="sxs-lookup"><span data-stu-id="b59ab-222">Used for incoming SIP requests for dial-in conferencing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-223">フロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-223">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b59ab-224">Lync Server 会議アテンダントサービス (ダイヤルイン会議)</span><span class="sxs-lookup"><span data-stu-id="b59ab-224">Lync Server Conferencing Attendant service (dial-in conferencing)</span></span></p></td>
<td><p><span data-ttu-id="b59ab-225">5072</span><span class="sxs-lookup"><span data-stu-id="b59ab-225">5072</span></span></p></td>
<td><p><span data-ttu-id="b59ab-226">TCP</span><span class="sxs-lookup"><span data-stu-id="b59ab-226">TCP</span></span></p></td>
<td><p><span data-ttu-id="b59ab-227">応答の受信 SIP 要求 (ダイヤルイン会議) に使用されます。</span><span class="sxs-lookup"><span data-stu-id="b59ab-227">Used for incoming SIP requests for Attendant (dial in conferencing).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-228">併置された仲介サーバーも実行するフロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-228">Front End Servers that also run a Collocated Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="b59ab-229">Lync Server 仲介サービス</span><span class="sxs-lookup"><span data-stu-id="b59ab-229">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="b59ab-230">5070</span><span class="sxs-lookup"><span data-stu-id="b59ab-230">5070</span></span></p></td>
<td><p><span data-ttu-id="b59ab-231">TCP</span><span class="sxs-lookup"><span data-stu-id="b59ab-231">TCP</span></span></p></td>
<td><p><span data-ttu-id="b59ab-232">フロントエンド サーバーから仲介サーバーへの要求を受信するために仲介サーバーで使用。</span><span class="sxs-lookup"><span data-stu-id="b59ab-232">Used by the Mediation Server for incoming requests from the Front End Server to the Mediation Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-233">併置された仲介サーバーも実行するフロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-233">Front End Servers that also run a Collocated Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="b59ab-234">Lync Server 仲介サービス</span><span class="sxs-lookup"><span data-stu-id="b59ab-234">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="b59ab-235">5067</span><span class="sxs-lookup"><span data-stu-id="b59ab-235">5067</span></span></p></td>
<td><p><span data-ttu-id="b59ab-236">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="b59ab-236">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="b59ab-237">PSTN ゲートウェイから仲介サーバーへの SIP 要求を受信するために使用。</span><span class="sxs-lookup"><span data-stu-id="b59ab-237">Used for incoming SIP requests from the PSTN gateway to the Mediation Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-238">併置された仲介サーバーも実行するフロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-238">Front End Servers that also run a Collocated Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="b59ab-239">Lync Server 仲介サービス</span><span class="sxs-lookup"><span data-stu-id="b59ab-239">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="b59ab-240">5068</span><span class="sxs-lookup"><span data-stu-id="b59ab-240">5068</span></span></p></td>
<td><p><span data-ttu-id="b59ab-241">TCP</span><span class="sxs-lookup"><span data-stu-id="b59ab-241">TCP</span></span></p></td>
<td><p><span data-ttu-id="b59ab-242">PSTN ゲートウェイから仲介サーバーへの SIP 要求を受信するために使用。</span><span class="sxs-lookup"><span data-stu-id="b59ab-242">Used for incoming SIP requests from the PSTN gateway to the Mediation Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-243">併置された仲介サーバーも実行するフロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-243">Front End Servers that also run a Collocated Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="b59ab-244">Lync Server 仲介サービス</span><span class="sxs-lookup"><span data-stu-id="b59ab-244">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="b59ab-245">5081</span><span class="sxs-lookup"><span data-stu-id="b59ab-245">5081</span></span></p></td>
<td><p><span data-ttu-id="b59ab-246">TCP</span><span class="sxs-lookup"><span data-stu-id="b59ab-246">TCP</span></span></p></td>
<td><p><span data-ttu-id="b59ab-247">仲介サーバーから PSTN ゲートウェイへの SIP 要求を送信するために使用。</span><span class="sxs-lookup"><span data-stu-id="b59ab-247">Used for outgoing SIP requests from the Mediation Server to the PSTN gateway.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-248">併置された仲介サーバーも実行するフロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-248">Front End Servers that also run a Collocated Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="b59ab-249">Lync Server 仲介サービス</span><span class="sxs-lookup"><span data-stu-id="b59ab-249">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="b59ab-250">5082</span><span class="sxs-lookup"><span data-stu-id="b59ab-250">5082</span></span></p></td>
<td><p><span data-ttu-id="b59ab-251">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="b59ab-251">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="b59ab-252">仲介サーバーから PSTN ゲートウェイへの SIP 要求を送信するために使用。</span><span class="sxs-lookup"><span data-stu-id="b59ab-252">Used for outgoing SIP requests from the Mediation Server to the PSTN gateway.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-253">フロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-253">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b59ab-254">Lync Server アプリケーション共有サービス</span><span class="sxs-lookup"><span data-stu-id="b59ab-254">Lync Server Application Sharing service</span></span></p></td>
<td><p><span data-ttu-id="b59ab-255">5065</span><span class="sxs-lookup"><span data-stu-id="b59ab-255">5065</span></span></p></td>
<td><p><span data-ttu-id="b59ab-256">TCP</span><span class="sxs-lookup"><span data-stu-id="b59ab-256">TCP</span></span></p></td>
<td><p><span data-ttu-id="b59ab-257">アプリケーション共有の SIP リッスン要求を受信するために使用。</span><span class="sxs-lookup"><span data-stu-id="b59ab-257">Used for incoming SIP listening requests for application sharing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-258">フロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-258">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b59ab-259">Lync Server アプリケーション共有サービス</span><span class="sxs-lookup"><span data-stu-id="b59ab-259">Lync Server Application Sharing service</span></span></p></td>
<td><p><span data-ttu-id="b59ab-260">49152-65535</span><span class="sxs-lookup"><span data-stu-id="b59ab-260">49152-65535</span></span></p></td>
<td><p><span data-ttu-id="b59ab-261">TCP</span><span class="sxs-lookup"><span data-stu-id="b59ab-261">TCP</span></span></p></td>
<td><p><span data-ttu-id="b59ab-262">アプリケーション共有で使用するメディア ポート範囲。</span><span class="sxs-lookup"><span data-stu-id="b59ab-262">Media port range used for application sharing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-263">フロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-263">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b59ab-264">Lync Server 会議のアナウンスメントサービス</span><span class="sxs-lookup"><span data-stu-id="b59ab-264">Lync Server Conferencing Announcement service</span></span></p></td>
<td><p><span data-ttu-id="b59ab-265">5073</span><span class="sxs-lookup"><span data-stu-id="b59ab-265">5073</span></span></p></td>
<td><p><span data-ttu-id="b59ab-266">TCP</span><span class="sxs-lookup"><span data-stu-id="b59ab-266">TCP</span></span></p></td>
<td><p><span data-ttu-id="b59ab-267">Lync Server 会議のアナウンスメントサービス (ダイヤルイン会議) の受信 SIP 要求に使用されます。</span><span class="sxs-lookup"><span data-stu-id="b59ab-267">Used for incoming SIP requests for the Lync Server Conferencing Announcement service (that is, for dial-in conferencing).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-268">フロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-268">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b59ab-269">Lync Server コール パーク サービス</span><span class="sxs-lookup"><span data-stu-id="b59ab-269">Lync Server Call Park service</span></span></p></td>
<td><p><span data-ttu-id="b59ab-270">5075</span><span class="sxs-lookup"><span data-stu-id="b59ab-270">5075</span></span></p></td>
<td><p><span data-ttu-id="b59ab-271">TCP</span><span class="sxs-lookup"><span data-stu-id="b59ab-271">TCP</span></span></p></td>
<td><p><span data-ttu-id="b59ab-272">コール パーク アプリケーションの SIP 要求を受信するために使用。</span><span class="sxs-lookup"><span data-stu-id="b59ab-272">Used for incoming SIP requests for the Call Park application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-273">フロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-273">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b59ab-274">Lync Server の音声テストサービス</span><span class="sxs-lookup"><span data-stu-id="b59ab-274">Lync Server Audio Test service</span></span></p></td>
<td><p><span data-ttu-id="b59ab-275">5076</span><span class="sxs-lookup"><span data-stu-id="b59ab-275">5076</span></span></p></td>
<td><p><span data-ttu-id="b59ab-276">TCP</span><span class="sxs-lookup"><span data-stu-id="b59ab-276">TCP</span></span></p></td>
<td><p><span data-ttu-id="b59ab-277">オーディオ テスト サービスの SIP 要求を受信するために使用。</span><span class="sxs-lookup"><span data-stu-id="b59ab-277">Used for incoming SIP requests for the Audio Test service.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-278">フロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-278">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b59ab-279">該当なし</span><span class="sxs-lookup"><span data-stu-id="b59ab-279">Not applicable</span></span></p></td>
<td><p><span data-ttu-id="b59ab-280">5066</span><span class="sxs-lookup"><span data-stu-id="b59ab-280">5066</span></span></p></td>
<td><p><span data-ttu-id="b59ab-281">TCP</span><span class="sxs-lookup"><span data-stu-id="b59ab-281">TCP</span></span></p></td>
<td><p><span data-ttu-id="b59ab-282">発信 Enhanced 9-1-1 (E9-1-1) ゲートウェイで使用。</span><span class="sxs-lookup"><span data-stu-id="b59ab-282">Used for outbound Enhanced 9-1-1 (E9-1-1) gateway.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-283">フロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-283">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b59ab-284">Lync Server 応答グループ サービス</span><span class="sxs-lookup"><span data-stu-id="b59ab-284">Lync Server Response Group service</span></span></p></td>
<td><p><span data-ttu-id="b59ab-285">5071</span><span class="sxs-lookup"><span data-stu-id="b59ab-285">5071</span></span></p></td>
<td><p><span data-ttu-id="b59ab-286">TCP</span><span class="sxs-lookup"><span data-stu-id="b59ab-286">TCP</span></span></p></td>
<td><p><span data-ttu-id="b59ab-287">応答グループ アプリケーションの SIP 要求を受信するために使用。</span><span class="sxs-lookup"><span data-stu-id="b59ab-287">Used for incoming SIP requests for the Response Group application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-288">フロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-288">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b59ab-289">Lync Server 応答グループ サービス</span><span class="sxs-lookup"><span data-stu-id="b59ab-289">Lync Server Response Group service</span></span></p></td>
<td><p><span data-ttu-id="b59ab-290">8404</span><span class="sxs-lookup"><span data-stu-id="b59ab-290">8404</span></span></p></td>
<td><p><span data-ttu-id="b59ab-291">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="b59ab-291">TCP (MTLS)</span></span></p></td>
<td><p><span data-ttu-id="b59ab-292">応答グループ アプリケーションの SIP 要求を受信するために使用。</span><span class="sxs-lookup"><span data-stu-id="b59ab-292">Used for incoming SIP requests for the Response Group application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-293">フロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-293">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b59ab-294">Lync Server 帯域幅ポリシーサービス</span><span class="sxs-lookup"><span data-stu-id="b59ab-294">Lync Server Bandwidth Policy Service</span></span></p></td>
<td><p><span data-ttu-id="b59ab-295">5080</span><span class="sxs-lookup"><span data-stu-id="b59ab-295">5080</span></span></p></td>
<td><p><span data-ttu-id="b59ab-296">TCP</span><span class="sxs-lookup"><span data-stu-id="b59ab-296">TCP</span></span></p></td>
<td><p><span data-ttu-id="b59ab-297">音声ビデオ エッジ TURN トラフィックの帯域幅ポリシー サービスによる通話受付管理で使用。</span><span class="sxs-lookup"><span data-stu-id="b59ab-297">Used for call admission control by the Bandwidth Policy service for A/V Edge TURN traffic.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-298">フロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-298">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b59ab-299">Lync Server 帯域幅ポリシーサービス</span><span class="sxs-lookup"><span data-stu-id="b59ab-299">Lync Server Bandwidth Policy Service</span></span></p></td>
<td><p><span data-ttu-id="b59ab-300">448</span><span class="sxs-lookup"><span data-stu-id="b59ab-300">448</span></span></p></td>
<td><p><span data-ttu-id="b59ab-301">TCP</span><span class="sxs-lookup"><span data-stu-id="b59ab-301">TCP</span></span></p></td>
<td><p><span data-ttu-id="b59ab-302">Lync Server 帯域幅ポリシーサービスによる通話受付制御に使用されます。</span><span class="sxs-lookup"><span data-stu-id="b59ab-302">Used for call admission control by the Lync Server Bandwidth Policy Service.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-303">中央管理ストアが配置されているフロントエンドサーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-303">Front End Servers where the Central Management store resides</span></span></p></td>
<td><p><span data-ttu-id="b59ab-304">Lync Server マスターレプリケーターエージェントサービス</span><span class="sxs-lookup"><span data-stu-id="b59ab-304">Lync Server Master Replicator Agent service</span></span></p></td>
<td><p><span data-ttu-id="b59ab-305">445</span><span class="sxs-lookup"><span data-stu-id="b59ab-305">445</span></span></p></td>
<td><p><span data-ttu-id="b59ab-306">TCP</span><span class="sxs-lookup"><span data-stu-id="b59ab-306">TCP</span></span></p></td>
<td><p><span data-ttu-id="b59ab-307">Lync Server を実行しているサーバーに、中央の管理ストアから構成データをプッシュするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b59ab-307">Used to push configuration data from the Central Management store to servers running Lync Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-308">すべてのサーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-308">All Servers</span></span></p></td>
<td><p><span data-ttu-id="b59ab-309">SQL ブラウザー</span><span class="sxs-lookup"><span data-stu-id="b59ab-309">SQL Browser</span></span></p></td>
<td><p><span data-ttu-id="b59ab-310">1434</span><span class="sxs-lookup"><span data-stu-id="b59ab-310">1434</span></span></p></td>
<td><p><span data-ttu-id="b59ab-311">UDP</span><span class="sxs-lookup"><span data-stu-id="b59ab-311">UDP</span></span></p></td>
<td><p><span data-ttu-id="b59ab-312">ローカルの SQL Server インスタンスの中央管理ストアデータのローカルにレプリケートされたコピー用の SQL ブラウザー</span><span class="sxs-lookup"><span data-stu-id="b59ab-312">SQL Browser for local replicated copy of Central Management store data in local SQL Server instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-313">すべての内部サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-313">All internal servers</span></span></p></td>
<td><p><span data-ttu-id="b59ab-314">各種</span><span class="sxs-lookup"><span data-stu-id="b59ab-314">Various</span></span></p></td>
<td><p><span data-ttu-id="b59ab-315">49152-57500</span><span class="sxs-lookup"><span data-stu-id="b59ab-315">49152-57500</span></span></p></td>
<td><p><span data-ttu-id="b59ab-316">TCP/UDP</span><span class="sxs-lookup"><span data-stu-id="b59ab-316">TCP/UDP</span></span></p></td>
<td><p><span data-ttu-id="b59ab-317">すべての内部サーバーでのオーディオ会議で使用するメディア ポート範囲。</span><span class="sxs-lookup"><span data-stu-id="b59ab-317">Media port range used for audio conferencing on all internal servers.</span></span> <span data-ttu-id="b59ab-318">オーディオを終了するすべてのサーバーで使用されます。フロントエンドサーバー (Lync Server 会議アテンダントサービス、Lync Server 会議のアナウンスメントサービス、Lync Server Audio/ビデオ会議サービス、および仲介サーバー)。</span><span class="sxs-lookup"><span data-stu-id="b59ab-318">Used by all servers that terminate audio: Front End Servers (for Lync Server Conferencing Attendant service, Lync Server Conferencing Announcement service, and Lync Server Audio/Video Conferencing service), and Mediation Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-319">Office Web Apps サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-319">Office Web Apps Servers</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b59ab-320">443</span><span class="sxs-lookup"><span data-stu-id="b59ab-320">443</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b59ab-321">Lync Server 2013 で Office Web Apps サーバーに接続するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b59ab-321">Used by Lync Server 2013 to connect to Office Web Apps Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-322">ディレクター</span><span class="sxs-lookup"><span data-stu-id="b59ab-322">Directors</span></span></p></td>
<td><p><span data-ttu-id="b59ab-323">Lync Server Front-End サービス</span><span class="sxs-lookup"><span data-stu-id="b59ab-323">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="b59ab-324">5060</span><span class="sxs-lookup"><span data-stu-id="b59ab-324">5060</span></span></p></td>
<td><p><span data-ttu-id="b59ab-325">TCP</span><span class="sxs-lookup"><span data-stu-id="b59ab-325">TCP</span></span></p></td>
<td><p><span data-ttu-id="b59ab-326">リモート通話コントロール サーバーなど、信頼されたサービスへの静的ルートの場合にオプションで使用。</span><span class="sxs-lookup"><span data-stu-id="b59ab-326">Optionally used for static routes to trusted services, such as remote call control servers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-327">ディレクター</span><span class="sxs-lookup"><span data-stu-id="b59ab-327">Directors</span></span></p></td>
<td><p><span data-ttu-id="b59ab-328">Lync Server Front-End サービス</span><span class="sxs-lookup"><span data-stu-id="b59ab-328">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="b59ab-329">444</span><span class="sxs-lookup"><span data-stu-id="b59ab-329">444</span></span></p></td>
<td><p><span data-ttu-id="b59ab-330">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b59ab-330">HTTPS</span></span></p>
<p><span data-ttu-id="b59ab-331">TCP</span><span class="sxs-lookup"><span data-stu-id="b59ab-331">TCP</span></span></p></td>
<td><p><span data-ttu-id="b59ab-332">フロントエンドとディレクターの間のサーバー間通信。</span><span class="sxs-lookup"><span data-stu-id="b59ab-332">Inter-server communication between Front End and Director.</span></span> <span data-ttu-id="b59ab-333">さらに、クライアント証明書公開 (フロントエンドサーバー) またはクライアント証明書が既に公開されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="b59ab-333">Additionally, client certificate publish (to Front End Servers) or validate if the client certificate has already been published.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-334">ディレクター</span><span class="sxs-lookup"><span data-stu-id="b59ab-334">Directors</span></span></p></td>
<td><p><span data-ttu-id="b59ab-335">Lync Server Web 互換サービス</span><span class="sxs-lookup"><span data-stu-id="b59ab-335">Lync Server Web Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="b59ab-336">80</span><span class="sxs-lookup"><span data-stu-id="b59ab-336">80</span></span></p></td>
<td><p><span data-ttu-id="b59ab-337">TCP</span><span class="sxs-lookup"><span data-stu-id="b59ab-337">TCP</span></span></p></td>
<td><p><span data-ttu-id="b59ab-p105">ディレクターから Web ファーム FQDN (IIS Web コンポーネントで使用される URL) への初期通信に使用。通常の動作では HTTPS トラフィックに切り替わり、ポート 443 およびプロトコル TCP を使用します。</span><span class="sxs-lookup"><span data-stu-id="b59ab-p105">Used for initial communication from Directors to the web farm FQDNs (the URLs used by IIS web components). In normal operation, will switch to HTTPS traffic, using port 443 and protocol type TCP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-340">ディレクター</span><span class="sxs-lookup"><span data-stu-id="b59ab-340">Directors</span></span></p></td>
<td><p><span data-ttu-id="b59ab-341">Lync Server Web 互換サービス</span><span class="sxs-lookup"><span data-stu-id="b59ab-341">Lync Server Web Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="b59ab-342">443</span><span class="sxs-lookup"><span data-stu-id="b59ab-342">443</span></span></p></td>
<td><p><span data-ttu-id="b59ab-343">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b59ab-343">HTTPS</span></span></p></td>
<td><p><span data-ttu-id="b59ab-344">ディレクターから Web ファーム FQDN (IIS Web コンポーネントで使用される URL) への通信に使用。</span><span class="sxs-lookup"><span data-stu-id="b59ab-344">Used for communication from Directors to the web farm FQDNs (the URLs used by IIS web components).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-345">ディレクター</span><span class="sxs-lookup"><span data-stu-id="b59ab-345">Directors</span></span></p></td>
<td><p><span data-ttu-id="b59ab-346">Lync Server Front-End サービス</span><span class="sxs-lookup"><span data-stu-id="b59ab-346">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="b59ab-347">5061</span><span class="sxs-lookup"><span data-stu-id="b59ab-347">5061</span></span></p></td>
<td><p><span data-ttu-id="b59ab-348">TCP</span><span class="sxs-lookup"><span data-stu-id="b59ab-348">TCP</span></span></p></td>
<td><p><span data-ttu-id="b59ab-349">サーバー間の内部通信とクライアント接続に使用。</span><span class="sxs-lookup"><span data-stu-id="b59ab-349">Used for internal communications between servers and for client connections.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-350">仲介サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-350">Mediation Servers</span></span></p></td>
<td><p><span data-ttu-id="b59ab-351">Lync Server 仲介サービス</span><span class="sxs-lookup"><span data-stu-id="b59ab-351">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="b59ab-352">5070</span><span class="sxs-lookup"><span data-stu-id="b59ab-352">5070</span></span></p></td>
<td><p><span data-ttu-id="b59ab-353">TCP</span><span class="sxs-lookup"><span data-stu-id="b59ab-353">TCP</span></span></p></td>
<td><p><span data-ttu-id="b59ab-354">フロントエンド サーバーからの要求を受信するために仲介サーバーで使用。</span><span class="sxs-lookup"><span data-stu-id="b59ab-354">Used by the Mediation Server for incoming requests from the Front End Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-355">仲介サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-355">Mediation Servers</span></span></p></td>
<td><p><span data-ttu-id="b59ab-356">Lync Server 仲介サービス</span><span class="sxs-lookup"><span data-stu-id="b59ab-356">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="b59ab-357">5067</span><span class="sxs-lookup"><span data-stu-id="b59ab-357">5067</span></span></p></td>
<td><p><span data-ttu-id="b59ab-358">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="b59ab-358">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="b59ab-359">PSTN ゲートウェイからの SIP 要求を受信するために使用。</span><span class="sxs-lookup"><span data-stu-id="b59ab-359">Used for incoming SIP requests from the PSTN gateway.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-360">仲介サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-360">Mediation Servers</span></span></p></td>
<td><p><span data-ttu-id="b59ab-361">Lync Server 仲介サービス</span><span class="sxs-lookup"><span data-stu-id="b59ab-361">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="b59ab-362">5068</span><span class="sxs-lookup"><span data-stu-id="b59ab-362">5068</span></span></p></td>
<td><p><span data-ttu-id="b59ab-363">TCP</span><span class="sxs-lookup"><span data-stu-id="b59ab-363">TCP</span></span></p></td>
<td><p><span data-ttu-id="b59ab-364">PSTN ゲートウェイからの SIP 要求を受信するために使用。</span><span class="sxs-lookup"><span data-stu-id="b59ab-364">Used for incoming SIP requests from the PSTN gateway.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-365">仲介サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-365">Mediation Servers</span></span></p></td>
<td><p><span data-ttu-id="b59ab-366">Lync Server 仲介サービス</span><span class="sxs-lookup"><span data-stu-id="b59ab-366">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="b59ab-367">5070</span><span class="sxs-lookup"><span data-stu-id="b59ab-367">5070</span></span></p></td>
<td><p><span data-ttu-id="b59ab-368">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="b59ab-368">TCP (MTLS)</span></span></p></td>
<td><p><span data-ttu-id="b59ab-369">フロントエンド サーバーからの SIP 要求で使用。</span><span class="sxs-lookup"><span data-stu-id="b59ab-369">Used for SIP requests from the Front End Servers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-370">常設チャット フロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-370">Persistent Chat Front End Server</span></span></p></td>
<td><p><span data-ttu-id="b59ab-371">常設チャット SIP</span><span class="sxs-lookup"><span data-stu-id="b59ab-371">Persistent Chat SIP</span></span></p></td>
<td><p><span data-ttu-id="b59ab-372">5041</span><span class="sxs-lookup"><span data-stu-id="b59ab-372">5041</span></span></p></td>
<td><p><span data-ttu-id="b59ab-373">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="b59ab-373">TCP (MTLS)</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-374">常設チャット フロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-374">Persistent Chat Front End Server</span></span></p></td>
<td><p><span data-ttu-id="b59ab-375">常設チャット Windows Communication Foundation (WCF)</span><span class="sxs-lookup"><span data-stu-id="b59ab-375">Persistent Chat Windows Communication Foundation (WCF)</span></span></p></td>
<td><p><span data-ttu-id="b59ab-376">881</span><span class="sxs-lookup"><span data-stu-id="b59ab-376">881</span></span></p></td>
<td><p><span data-ttu-id="b59ab-377">TCP (TLS) および TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="b59ab-377">TCP (TLS) and TCP (MTLS)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-378">常設チャット フロントエンド サーバー</span><span class="sxs-lookup"><span data-stu-id="b59ab-378">Persistent Chat Front End Server</span></span></p></td>
<td><p><span data-ttu-id="b59ab-379">常設チャット ファイル転送サービス</span><span class="sxs-lookup"><span data-stu-id="b59ab-379">Persistent Chat File Transfer Service</span></span></p></td>
<td><p><span data-ttu-id="b59ab-380">443</span><span class="sxs-lookup"><span data-stu-id="b59ab-380">443</span></span></p></td>
<td><p><span data-ttu-id="b59ab-381">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="b59ab-381">TCP (TLS)</span></span></p></td>
<td></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="b59ab-382">一部のリモート通話コントロールシナリオでは、フロントエンドサーバーまたはディレクターと PBX の間に TCP 接続が必要です。</span><span class="sxs-lookup"><span data-stu-id="b59ab-382">Some remote call control scenarios require a TCP connection between the Front End Server or Director and the PBX.</span></span> <span data-ttu-id="b59ab-383">Lync Server は TCP ポート5060を使用しなくなりましたが、リモートコールコントロールの展開時には、RCC Line Server の FQDN と、フロントエンドサーバーまたはディレクターが PBX システムに接続するために使用する TCP ポートを関連付ける信頼されたサーバー構成を作成します。</span><span class="sxs-lookup"><span data-stu-id="b59ab-383">Although Lync Server no longer uses TCP port 5060, during remote call control deployment you create a trusted server configuration, which associates the RCC Line Server FQDN with the TCP port that the Front End Server or Director will use to connect to the PBX system.</span></span> <span data-ttu-id="b59ab-384">詳細については、「Lync Server 管理シェルドキュメントの <STRONG>CsTrustedApplicationComputer</STRONG> コマンドレット」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b59ab-384">For details, see the <STRONG>CsTrustedApplicationComputer</STRONG> cmdlet in the Lync Server Management Shell documentation.</span></span>



</div>

<span data-ttu-id="b59ab-385">次の表に、(DNS 負荷分散ではない) ハードウェア負荷分散のみを使用するプールでハードウェア ロード バランサーを開くために必要なポートを示します。</span><span class="sxs-lookup"><span data-stu-id="b59ab-385">For your pools that use only hardware load balancing (not DNS load balancing), the following table shows the ports that need to open the hardware load balancers.</span></span>

### <a name="hardware-load-balancer-ports-if-using-only-hardware-load-balancing"></a><span data-ttu-id="b59ab-386">ハードウェア負荷分散のみを使用する場合のハードウェア ロード バランサー</span><span class="sxs-lookup"><span data-stu-id="b59ab-386">Hardware Load Balancer Ports if Using Only Hardware Load Balancing</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b59ab-387">ロード バランサー</span><span class="sxs-lookup"><span data-stu-id="b59ab-387">Load Balancer</span></span></th>
<th><span data-ttu-id="b59ab-388">ポート</span><span class="sxs-lookup"><span data-stu-id="b59ab-388">Port</span></span></th>
<th><span data-ttu-id="b59ab-389">プロトコル</span><span class="sxs-lookup"><span data-stu-id="b59ab-389">Protocol</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-390">フロントエンド サーバーのロード バランサー</span><span class="sxs-lookup"><span data-stu-id="b59ab-390">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b59ab-391">5061</span><span class="sxs-lookup"><span data-stu-id="b59ab-391">5061</span></span></p></td>
<td><p><span data-ttu-id="b59ab-392">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="b59ab-392">TCP (TLS)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-393">フロントエンド サーバーのロード バランサー</span><span class="sxs-lookup"><span data-stu-id="b59ab-393">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b59ab-394">444</span><span class="sxs-lookup"><span data-stu-id="b59ab-394">444</span></span></p></td>
<td><p><span data-ttu-id="b59ab-395">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b59ab-395">HTTPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-396">フロントエンド サーバーのロード バランサー</span><span class="sxs-lookup"><span data-stu-id="b59ab-396">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b59ab-397">135</span><span class="sxs-lookup"><span data-stu-id="b59ab-397">135</span></span></p></td>
<td><p><span data-ttu-id="b59ab-398">DCOM およびリモート プロシージャ コール (RPC)</span><span class="sxs-lookup"><span data-stu-id="b59ab-398">DCOM and remote procedure call (RPC)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-399">フロントエンド サーバーのロード バランサー</span><span class="sxs-lookup"><span data-stu-id="b59ab-399">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b59ab-400">80</span><span class="sxs-lookup"><span data-stu-id="b59ab-400">80</span></span></p></td>
<td><p><span data-ttu-id="b59ab-401">HTTP</span><span class="sxs-lookup"><span data-stu-id="b59ab-401">HTTP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-402">フロントエンド サーバーのロード バランサー</span><span class="sxs-lookup"><span data-stu-id="b59ab-402">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b59ab-403">8080</span><span class="sxs-lookup"><span data-stu-id="b59ab-403">8080</span></span></p></td>
<td><p><span data-ttu-id="b59ab-404">TCP - フロントエンド サーバーからのクライアントとデバイスのルート証明書取得 - NTLM で認証されたクライアントとデバイス</span><span class="sxs-lookup"><span data-stu-id="b59ab-404">TCP - Client and device retrieval of root certificate from Front End Server – clients and devices authenticated by NTLM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-405">フロントエンド サーバーのロード バランサー</span><span class="sxs-lookup"><span data-stu-id="b59ab-405">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b59ab-406">443</span><span class="sxs-lookup"><span data-stu-id="b59ab-406">443</span></span></p></td>
<td><p><span data-ttu-id="b59ab-407">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b59ab-407">HTTPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-408">フロントエンド サーバーのロード バランサー</span><span class="sxs-lookup"><span data-stu-id="b59ab-408">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b59ab-409">4443</span><span class="sxs-lookup"><span data-stu-id="b59ab-409">4443</span></span></p></td>
<td><p><span data-ttu-id="b59ab-410">HTTPS (リバース プロキシから)</span><span class="sxs-lookup"><span data-stu-id="b59ab-410">HTTPS (from reverse proxy)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-411">フロントエンド サーバーのロード バランサー</span><span class="sxs-lookup"><span data-stu-id="b59ab-411">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b59ab-412">5072</span><span class="sxs-lookup"><span data-stu-id="b59ab-412">5072</span></span></p></td>
<td><p><span data-ttu-id="b59ab-413">TCP</span><span class="sxs-lookup"><span data-stu-id="b59ab-413">TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-414">フロントエンド サーバーのロード バランサー</span><span class="sxs-lookup"><span data-stu-id="b59ab-414">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b59ab-415">5073</span><span class="sxs-lookup"><span data-stu-id="b59ab-415">5073</span></span></p></td>
<td><p><span data-ttu-id="b59ab-416">TCP</span><span class="sxs-lookup"><span data-stu-id="b59ab-416">TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-417">フロントエンド サーバーのロード バランサー</span><span class="sxs-lookup"><span data-stu-id="b59ab-417">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b59ab-418">5075</span><span class="sxs-lookup"><span data-stu-id="b59ab-418">5075</span></span></p></td>
<td><p><span data-ttu-id="b59ab-419">TCP</span><span class="sxs-lookup"><span data-stu-id="b59ab-419">TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-420">フロントエンド サーバーのロード バランサー</span><span class="sxs-lookup"><span data-stu-id="b59ab-420">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b59ab-421">5076</span><span class="sxs-lookup"><span data-stu-id="b59ab-421">5076</span></span></p></td>
<td><p><span data-ttu-id="b59ab-422">TCP</span><span class="sxs-lookup"><span data-stu-id="b59ab-422">TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-423">フロントエンド サーバーのロード バランサー</span><span class="sxs-lookup"><span data-stu-id="b59ab-423">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b59ab-424">5071</span><span class="sxs-lookup"><span data-stu-id="b59ab-424">5071</span></span></p></td>
<td><p><span data-ttu-id="b59ab-425">TCP</span><span class="sxs-lookup"><span data-stu-id="b59ab-425">TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-426">フロントエンド サーバーのロード バランサー</span><span class="sxs-lookup"><span data-stu-id="b59ab-426">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b59ab-427">5080</span><span class="sxs-lookup"><span data-stu-id="b59ab-427">5080</span></span></p></td>
<td><p><span data-ttu-id="b59ab-428">TCP</span><span class="sxs-lookup"><span data-stu-id="b59ab-428">TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-429">フロントエンド サーバーのロード バランサー</span><span class="sxs-lookup"><span data-stu-id="b59ab-429">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b59ab-430">448</span><span class="sxs-lookup"><span data-stu-id="b59ab-430">448</span></span></p></td>
<td><p><span data-ttu-id="b59ab-431">TCP</span><span class="sxs-lookup"><span data-stu-id="b59ab-431">TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-432">仲介サーバーのロード バランサー</span><span class="sxs-lookup"><span data-stu-id="b59ab-432">Mediation Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b59ab-433">5070</span><span class="sxs-lookup"><span data-stu-id="b59ab-433">5070</span></span></p></td>
<td><p><span data-ttu-id="b59ab-434">TCP</span><span class="sxs-lookup"><span data-stu-id="b59ab-434">TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-435">フロントエンド サーバーのロード バランサー (プールで仲介サーバーも稼働する場合)</span><span class="sxs-lookup"><span data-stu-id="b59ab-435">Front End Server load balancer (if the pool also runs Mediation Server)</span></span></p></td>
<td><p><span data-ttu-id="b59ab-436">5070</span><span class="sxs-lookup"><span data-stu-id="b59ab-436">5070</span></span></p></td>
<td><p><span data-ttu-id="b59ab-437">TCP</span><span class="sxs-lookup"><span data-stu-id="b59ab-437">TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-438">ディレクターのロード バランサー</span><span class="sxs-lookup"><span data-stu-id="b59ab-438">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="b59ab-439">443</span><span class="sxs-lookup"><span data-stu-id="b59ab-439">443</span></span></p></td>
<td><p><span data-ttu-id="b59ab-440">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b59ab-440">HTTPS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-441">ディレクターのロード バランサー</span><span class="sxs-lookup"><span data-stu-id="b59ab-441">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="b59ab-442">444</span><span class="sxs-lookup"><span data-stu-id="b59ab-442">444</span></span></p></td>
<td><p><span data-ttu-id="b59ab-443">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b59ab-443">HTTPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-444">ディレクターのロード バランサー</span><span class="sxs-lookup"><span data-stu-id="b59ab-444">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="b59ab-445">5061</span><span class="sxs-lookup"><span data-stu-id="b59ab-445">5061</span></span></p></td>
<td><p><span data-ttu-id="b59ab-446">TCP</span><span class="sxs-lookup"><span data-stu-id="b59ab-446">TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-447">ディレクターのロード バランサー</span><span class="sxs-lookup"><span data-stu-id="b59ab-447">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="b59ab-448">4443</span><span class="sxs-lookup"><span data-stu-id="b59ab-448">4443</span></span></p></td>
<td><p><span data-ttu-id="b59ab-449">HTTPS (リバース プロキシから)</span><span class="sxs-lookup"><span data-stu-id="b59ab-449">HTTPS (from reverse proxy)</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b59ab-p107">DNS 負荷分散を使用するフロントエンド プールとディレクター プールでも、ハードウェア ロード バランサーを展開しておく必要があります。次の表に、これらのハードウェア ロード バランサーで開く必要があるポートを示します。</span><span class="sxs-lookup"><span data-stu-id="b59ab-p107">Your Front End pools and Director pools that use DNS load balancing also must have a hardware load balancer deployed. The following table shows the ports that need to be open on these hardware load balancers.</span></span>

### <a name="hardware-load-balancer-ports-if-using-dns-load-balancing"></a><span data-ttu-id="b59ab-452">DNS 負荷分散を使用する場合のハードウェア ロード バランサー</span><span class="sxs-lookup"><span data-stu-id="b59ab-452">Hardware Load Balancer Ports if Using DNS Load Balancing</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b59ab-453">ロード バランサー</span><span class="sxs-lookup"><span data-stu-id="b59ab-453">Load Balancer</span></span></th>
<th><span data-ttu-id="b59ab-454">ポート</span><span class="sxs-lookup"><span data-stu-id="b59ab-454">Port</span></span></th>
<th><span data-ttu-id="b59ab-455">プロトコル</span><span class="sxs-lookup"><span data-stu-id="b59ab-455">Protocol</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-456">フロントエンド サーバーのロード バランサー</span><span class="sxs-lookup"><span data-stu-id="b59ab-456">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b59ab-457">80</span><span class="sxs-lookup"><span data-stu-id="b59ab-457">80</span></span></p></td>
<td><p><span data-ttu-id="b59ab-458">HTTP</span><span class="sxs-lookup"><span data-stu-id="b59ab-458">HTTP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-459">フロントエンド サーバーのロード バランサー</span><span class="sxs-lookup"><span data-stu-id="b59ab-459">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b59ab-460">443</span><span class="sxs-lookup"><span data-stu-id="b59ab-460">443</span></span></p></td>
<td><p><span data-ttu-id="b59ab-461">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b59ab-461">HTTPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-462">フロントエンド サーバーのロード バランサー</span><span class="sxs-lookup"><span data-stu-id="b59ab-462">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b59ab-463">8080</span><span class="sxs-lookup"><span data-stu-id="b59ab-463">8080</span></span></p></td>
<td><p><span data-ttu-id="b59ab-464">TCP - フロントエンド サーバーからのクライアントとデバイスのルート証明書取得 - NTLM で認証されたクライアントとデバイス</span><span class="sxs-lookup"><span data-stu-id="b59ab-464">TCP - Client and device retrieval of root certificate from Front End Server – clients and devices authenticated by NTLM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-465">フロントエンド サーバーのロード バランサー</span><span class="sxs-lookup"><span data-stu-id="b59ab-465">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b59ab-466">4443</span><span class="sxs-lookup"><span data-stu-id="b59ab-466">4443</span></span></p></td>
<td><p><span data-ttu-id="b59ab-467">HTTPS (リバース プロキシから)</span><span class="sxs-lookup"><span data-stu-id="b59ab-467">HTTPS (from reverse proxy)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-468">ディレクターのロード バランサー</span><span class="sxs-lookup"><span data-stu-id="b59ab-468">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="b59ab-469">443</span><span class="sxs-lookup"><span data-stu-id="b59ab-469">443</span></span></p></td>
<td><p><span data-ttu-id="b59ab-470">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b59ab-470">HTTPS</span></span></p></td>
</tr>
<tr class="even">
<td> </td>
<td> </td>
<td> </td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-471">ディレクターのロード バランサー</span><span class="sxs-lookup"><span data-stu-id="b59ab-471">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="b59ab-472">4443</span><span class="sxs-lookup"><span data-stu-id="b59ab-472">4443</span></span></p></td>
<td><p><span data-ttu-id="b59ab-473">HTTPS (リバース プロキシから)</span><span class="sxs-lookup"><span data-stu-id="b59ab-473">HTTPS (from reverse proxy)</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="required-client-ports"></a><span data-ttu-id="b59ab-474">必要なクライアント ポート</span><span class="sxs-lookup"><span data-stu-id="b59ab-474">Required Client Ports</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b59ab-475">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="b59ab-475">Component</span></span></th>
<th><span data-ttu-id="b59ab-476">ポート</span><span class="sxs-lookup"><span data-stu-id="b59ab-476">Port</span></span></th>
<th><span data-ttu-id="b59ab-477">プロトコル</span><span class="sxs-lookup"><span data-stu-id="b59ab-477">Protocol</span></span></th>
<th><span data-ttu-id="b59ab-478">メモ</span><span class="sxs-lookup"><span data-stu-id="b59ab-478">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-479">クライアント</span><span class="sxs-lookup"><span data-stu-id="b59ab-479">Clients</span></span></p></td>
<td><p><span data-ttu-id="b59ab-480">67/68</span><span class="sxs-lookup"><span data-stu-id="b59ab-480">67/68</span></span></p></td>
<td><p><span data-ttu-id="b59ab-481">DHCP</span><span class="sxs-lookup"><span data-stu-id="b59ab-481">DHCP</span></span></p></td>
<td><p><span data-ttu-id="b59ab-482">Lync Server によってレジストラーの FQDN が検索されます (つまり、DNS SRV に障害が発生した場合は、手動の設定が構成されていない場合)。</span><span class="sxs-lookup"><span data-stu-id="b59ab-482">Used by Lync Server to find the Registrar FQDN (that is, if DNS SRV fails and manual settings are not configured).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-483">クライアント</span><span class="sxs-lookup"><span data-stu-id="b59ab-483">Clients</span></span></p></td>
<td><p><span data-ttu-id="b59ab-484">443</span><span class="sxs-lookup"><span data-stu-id="b59ab-484">443</span></span></p></td>
<td><p><span data-ttu-id="b59ab-485">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="b59ab-485">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="b59ab-486">外部ユーザー アクセスのクライアントとサーバー間の SIP トラフィックで使用。</span><span class="sxs-lookup"><span data-stu-id="b59ab-486">Used for client-to-server SIP traffic for external user access.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-487">クライアント</span><span class="sxs-lookup"><span data-stu-id="b59ab-487">Clients</span></span></p></td>
<td><p><span data-ttu-id="b59ab-488">443</span><span class="sxs-lookup"><span data-stu-id="b59ab-488">443</span></span></p></td>
<td><p><span data-ttu-id="b59ab-489">TCP (PSOM/TLS)</span><span class="sxs-lookup"><span data-stu-id="b59ab-489">TCP (PSOM/TLS)</span></span></p></td>
<td><p><span data-ttu-id="b59ab-490">Web 会議セッションへの外部ユーザー アクセスで使用。</span><span class="sxs-lookup"><span data-stu-id="b59ab-490">Used for external user access to web conferencing sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-491">クライアント</span><span class="sxs-lookup"><span data-stu-id="b59ab-491">Clients</span></span></p></td>
<td><p><span data-ttu-id="b59ab-492">443</span><span class="sxs-lookup"><span data-stu-id="b59ab-492">443</span></span></p></td>
<td><p><span data-ttu-id="b59ab-493">TCP (STUN/MSTURN)</span><span class="sxs-lookup"><span data-stu-id="b59ab-493">TCP (STUN/MSTURN)</span></span></p></td>
<td><p><span data-ttu-id="b59ab-494">音声ビデオ セッションとメディアへの外部ユーザー アクセス (TCP) で使用。</span><span class="sxs-lookup"><span data-stu-id="b59ab-494">Used for external user access to A/V sessions and media (TCP)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-495">クライアント</span><span class="sxs-lookup"><span data-stu-id="b59ab-495">Clients</span></span></p></td>
<td><p><span data-ttu-id="b59ab-496">3478</span><span class="sxs-lookup"><span data-stu-id="b59ab-496">3478</span></span></p></td>
<td><p><span data-ttu-id="b59ab-497">UDP (STUN/MSTURN)</span><span class="sxs-lookup"><span data-stu-id="b59ab-497">UDP (STUN/MSTURN)</span></span></p></td>
<td><p><span data-ttu-id="b59ab-498">音声ビデオ セッションとメディアへの外部ユーザー アクセス (UDP) で使用。</span><span class="sxs-lookup"><span data-stu-id="b59ab-498">Used for external user access to A/V sessions and media (UDP)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-499">クライアント</span><span class="sxs-lookup"><span data-stu-id="b59ab-499">Clients</span></span></p></td>
<td><p><span data-ttu-id="b59ab-500">5061</span><span class="sxs-lookup"><span data-stu-id="b59ab-500">5061</span></span></p></td>
<td><p><span data-ttu-id="b59ab-501">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="b59ab-501">TCP (MTLS)</span></span></p></td>
<td><p><span data-ttu-id="b59ab-502">外部ユーザー アクセスのクライアントとサーバー間の SIP トラフィックで使用。</span><span class="sxs-lookup"><span data-stu-id="b59ab-502">Used for client-to-server SIP traffic for external user access.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-503">クライアント</span><span class="sxs-lookup"><span data-stu-id="b59ab-503">Clients</span></span></p></td>
<td><p><span data-ttu-id="b59ab-504">6891-6901</span><span class="sxs-lookup"><span data-stu-id="b59ab-504">6891-6901</span></span></p></td>
<td><p><span data-ttu-id="b59ab-505">TCP</span><span class="sxs-lookup"><span data-stu-id="b59ab-505">TCP</span></span></p></td>
<td><p><span data-ttu-id="b59ab-506">Lync クライアントと以前のクライアント (Microsoft Office Communications Server 2007 R2、Microsoft Office Communications Server 2007、Live Communications Server 2005) の間でのファイル送信に使用されます。</span><span class="sxs-lookup"><span data-stu-id="b59ab-506">Used for file transfer between Lync clients and previous clients (clients of Microsoft Office Communications Server 2007 R2, Microsoft Office Communications Server 2007, and Live Communications Server 2005).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-507">クライアント</span><span class="sxs-lookup"><span data-stu-id="b59ab-507">Clients</span></span></p></td>
<td><p><span data-ttu-id="b59ab-508">1024-65535 \*</span><span class="sxs-lookup"><span data-stu-id="b59ab-508">1024-65535 \*</span></span></p></td>
<td><p><span data-ttu-id="b59ab-509">TCP/UDP</span><span class="sxs-lookup"><span data-stu-id="b59ab-509">TCP/UDP</span></span></p></td>
<td><p><span data-ttu-id="b59ab-510">オーディオ ポート範囲 (少なくとも 20 個のポートが必要)。</span><span class="sxs-lookup"><span data-stu-id="b59ab-510">Audio port range (minimum of 20 ports required)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-511">クライアント</span><span class="sxs-lookup"><span data-stu-id="b59ab-511">Clients</span></span></p></td>
<td><p><span data-ttu-id="b59ab-512">1024-65535 \*</span><span class="sxs-lookup"><span data-stu-id="b59ab-512">1024-65535 \*</span></span></p></td>
<td><p><span data-ttu-id="b59ab-513">TCP/UDP</span><span class="sxs-lookup"><span data-stu-id="b59ab-513">TCP/UDP</span></span></p></td>
<td><p><span data-ttu-id="b59ab-514">ビデオ ポート範囲 (少なくとも 20 個のポートが必要)。</span><span class="sxs-lookup"><span data-stu-id="b59ab-514">Video port range (minimum of 20 ports required).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-515">クライアント</span><span class="sxs-lookup"><span data-stu-id="b59ab-515">Clients</span></span></p></td>
<td><p><span data-ttu-id="b59ab-516">1024-65535 \*</span><span class="sxs-lookup"><span data-stu-id="b59ab-516">1024-65535 \*</span></span></p></td>
<td><p><span data-ttu-id="b59ab-517">TCP</span><span class="sxs-lookup"><span data-stu-id="b59ab-517">TCP</span></span></p></td>
<td><p><span data-ttu-id="b59ab-518">ピアツーピア ファイル転送 (会議ファイル転送の場合、クライアントは PSOM を使用)。</span><span class="sxs-lookup"><span data-stu-id="b59ab-518">Peer-to-peer file transfer (for conferencing file transfer, clients use PSOM).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b59ab-519">クライアント</span><span class="sxs-lookup"><span data-stu-id="b59ab-519">Clients</span></span></p></td>
<td><p><span data-ttu-id="b59ab-520">1024-65535 \*</span><span class="sxs-lookup"><span data-stu-id="b59ab-520">1024-65535 \*</span></span></p></td>
<td><p><span data-ttu-id="b59ab-521">TCP</span><span class="sxs-lookup"><span data-stu-id="b59ab-521">TCP</span></span></p></td>
<td><p><span data-ttu-id="b59ab-522">アプリケーション共有。</span><span class="sxs-lookup"><span data-stu-id="b59ab-522">Application sharing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b59ab-523">Aastra 6721ip 共通領域電話</span><span class="sxs-lookup"><span data-stu-id="b59ab-523">Aastra 6721ip common area phone</span></span></p>
<p><span data-ttu-id="b59ab-524">Aastra 6725ip 卓上電話</span><span class="sxs-lookup"><span data-stu-id="b59ab-524">Aastra 6725ip desk phone</span></span></p>
<p><span data-ttu-id="b59ab-525">HP 4110 IP 電話 (共通領域電話)</span><span class="sxs-lookup"><span data-stu-id="b59ab-525">HP 4110 IP Phone (common area phone)</span></span></p>
<p><span data-ttu-id="b59ab-526">HP 4120 IP 電話 (卓上電話)</span><span class="sxs-lookup"><span data-stu-id="b59ab-526">HP 4120 IP Phone (desk phone)</span></span></p>
<p><span data-ttu-id="b59ab-527">Polycom CX500 IP 共通領域電話</span><span class="sxs-lookup"><span data-stu-id="b59ab-527">Polycom CX500 IP common area phone</span></span></p>
<p><span data-ttu-id="b59ab-528">Polycom CX600 IP 卓上電話</span><span class="sxs-lookup"><span data-stu-id="b59ab-528">Polycom CX600 IP desk phone</span></span></p>
<p><span data-ttu-id="b59ab-529">Polycom CX700 IP 卓上電話</span><span class="sxs-lookup"><span data-stu-id="b59ab-529">Polycom CX700 IP desk phone</span></span></p>
<p><span data-ttu-id="b59ab-530">Polycom CX3000 IP 会議電話</span><span class="sxs-lookup"><span data-stu-id="b59ab-530">Polycom CX3000 IP conference phone</span></span></p></td>
<td><p><span data-ttu-id="b59ab-531">67/68</span><span class="sxs-lookup"><span data-stu-id="b59ab-531">67/68</span></span></p></td>
<td><p><span data-ttu-id="b59ab-532">DHCP</span><span class="sxs-lookup"><span data-stu-id="b59ab-532">DHCP</span></span></p></td>
<td><p><span data-ttu-id="b59ab-533">リストされているデバイスで使用され、Lync Server 証明書、プロビジョニング FQDN、レジストラー FQDN を検索します。</span><span class="sxs-lookup"><span data-stu-id="b59ab-533">Used by the listed devices to find the Lync Server certificate, provisioning FQDN, and Registrar FQDN.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b59ab-534">**\*** これらのメディアの種類に対して特定のポートを構成するには、CsConferencingConfiguration コマンドレット (ClientMediaPortRangeEnabled、ClientMediaPort、ClientMediaPortRange parameters) を使用します。</span><span class="sxs-lookup"><span data-stu-id="b59ab-534">**\*** To configure specific ports for these media types, use the CsConferencingConfiguration cmdlet (ClientMediaPortRangeEnabled, ClientMediaPort, and ClientMediaPortRange parameters).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b59ab-535">Lync クライアント用のプログラムを設定すると、必要なオペレーティングシステムファイアウォール例外がクライアントコンピューターに自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="b59ab-535">The set programs for Lync clients automatically create the required operating-system firewall exceptions on the client computer.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="b59ab-536">外部ユーザー アクセス用に使用されるポートは、クライアントが組織のファイアウォールを通過する必要のあるすべてのシナリオにおいて必要です (たとえば、他の組織によってホストされる外部の通信や会議)。</span><span class="sxs-lookup"><span data-stu-id="b59ab-536">The ports that are used for external user access are required for any scenario in which the client must traverse the organization’s firewall (for example, any external communications or meetings hosted by other organizations).</span></span>



<span data-ttu-id="b59ab-537"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b59ab-537"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

