---
title: 'Lync Server 2013: 常設チャット サーバーの新機能'
description: 'Lync Server 2013: 新しい常設チャットサーバー機能。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New Persistent Chat Server features
ms:assetid: c3ec6f33-6261-4bf5-aa31-baa8ab2a87d8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412965(v=OCS.15)
ms:contentKeyID: 48185341
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 549fa43e115467c373fe8df08f8568aa8715c29d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445352"
---
# <a name="new-persistent-chat-server-features-in-lync-server-2013"></a><span data-ttu-id="b1409-103">Lync Server 2013 の常設チャット サーバーの新機能</span><span class="sxs-lookup"><span data-stu-id="b1409-103">New Persistent Chat Server features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b1409-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b1409-104">

<span> </span></span></span>

<span data-ttu-id="b1409-105">_**最終更新日:** 2012-10-29_</span><span class="sxs-lookup"><span data-stu-id="b1409-105">_**Topic Last Modified:** 2012-10-29_</span></span>

<span data-ttu-id="b1409-106">Lync Server 2013 の常設チャットサーバーでは、時間の経過に伴う、トピックベースの会話に参加することができます。</span><span class="sxs-lookup"><span data-stu-id="b1409-106">Lync Server 2013, Persistent Chat Server enables you to participate in multiparty, topic-based conversations that persist over time.</span></span> <span data-ttu-id="b1409-107">常設チャットサーバーは、組織が次のことを行うのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="b1409-107">Persistent Chat Server can help your organization do the following:</span></span>

  - <span data-ttu-id="b1409-108">地理的に分散したチームと部門間のチーム間のコミュニケーションを向上させる</span><span class="sxs-lookup"><span data-stu-id="b1409-108">Improve communication between geographically dispersed and cross-functional teams</span></span>

  - <span data-ttu-id="b1409-109">情報の認識と参加を広げる</span><span class="sxs-lookup"><span data-stu-id="b1409-109">Broaden information awareness and participation</span></span>

  - <span data-ttu-id="b1409-110">拡張組織とのコミュニケーションを向上させる</span><span class="sxs-lookup"><span data-stu-id="b1409-110">Improve communication with your extended organization</span></span>

  - <span data-ttu-id="b1409-111">情報過多の削減</span><span class="sxs-lookup"><span data-stu-id="b1409-111">Reduce information overload</span></span>

  - <span data-ttu-id="b1409-112">情報認識の向上</span><span class="sxs-lookup"><span data-stu-id="b1409-112">Improve information awareness</span></span>

  - <span data-ttu-id="b1409-113">重要な知識と情報の分散を増やす</span><span class="sxs-lookup"><span data-stu-id="b1409-113">Increase dispersion of important knowledge and information</span></span>

<span data-ttu-id="b1409-114">Lync Server 2013、常設チャットサーバーは、Microsoft 365 または Office 365 では使用できません。</span><span class="sxs-lookup"><span data-stu-id="b1409-114">Lync Server 2013, Persistent Chat Server is not available in Microsoft 365 or Office 365.</span></span> <span data-ttu-id="b1409-115">現時点では、オンプレミスの Lync 2013 ユーザーのみが利用できます。</span><span class="sxs-lookup"><span data-stu-id="b1409-115">At this time, it is available only to on-premise Lync 2013 customers.</span></span>

<span data-ttu-id="b1409-116">Lync 2013 では、常設チャット機能は Lync 2013 クライアントに統合されています。</span><span class="sxs-lookup"><span data-stu-id="b1409-116">In Lync 2013, Persistent Chat functionality is integrated into the Lync 2013 client.</span></span> <span data-ttu-id="b1409-117">この結果、ユーザーは Lync 2013 クライアントで、インスタントメッセージ/プレゼンス、音声/ビデオ、会議、常設チャットにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="b1409-117">As a result, users have access to Instant Messaging/Presence, Audio/Video, Conferencing, and Persistent Chat all in the Lync 2013 client.</span></span> <span data-ttu-id="b1409-118">Lync 2013 クライアントの詳細については、を参照してください <https://go.microsoft.com/fwlink/p/?linkid=270877> 。</span><span class="sxs-lookup"><span data-stu-id="b1409-118">For more information about the Lync 2013 client, see <https://go.microsoft.com/fwlink/p/?linkid=270877>.</span></span>

<span data-ttu-id="b1409-119">このトピックでは、次のような新しいバージョンの Lync Server 2013、常設チャットサーバー、および以前のバージョン (Microsoft Lync Server 2010、グループチャット) の機能の変更について説明します。</span><span class="sxs-lookup"><span data-stu-id="b1409-119">This topic describes feature changes between the new version of Lync Server 2013, Persistent Chat Server and the previous version (Microsoft Lync Server 2010, Group Chat), including:</span></span>

  - <span data-ttu-id="b1409-120">Lync Server コントロールパネルで管理者エクスペリエンスを提供し、グループチャット管理ツールを削除する</span><span class="sxs-lookup"><span data-stu-id="b1409-120">Provide an administrative experience in Lync Server Control Panel, and eliminate the Group Chat Admin Tool</span></span>

  - <span data-ttu-id="b1409-121">グループチャット構成ツールを削除して、常設チャットサーバーの構成設定をトポロジビルダーに統合する</span><span class="sxs-lookup"><span data-stu-id="b1409-121">Integrate configuration settings for Persistent Chat Server into Topology Builder by eliminating the Group Chat Configuration tool</span></span>

  - <span data-ttu-id="b1409-122">以前のバージョンの常設チャットサーバーからの移行とアップグレードを容易にする</span><span class="sxs-lookup"><span data-stu-id="b1409-122">Ease migration and upgrade from previous versions of Persistent Chat Server</span></span>

  - <span data-ttu-id="b1409-123">高可用性と災害復旧のソリューションを提供する</span><span class="sxs-lookup"><span data-stu-id="b1409-123">Provide high availability and disaster recovery solutions</span></span>

<span data-ttu-id="b1409-124">常設チャットサーバーの最新バージョンについて詳しくは、以下をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="b1409-124">For additional details about the latest version of Persistent Chat Server, see the following:</span></span>

  - <span data-ttu-id="b1409-125">常設チャットのヘルプでは、常設チャットの <https://go.microsoft.com/fwlink/p/?linkid=270945> 機能の詳細な一覧、機能、および常設チャットサーバーの実行時に使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b1409-125">The Persistent Chat Help at <https://go.microsoft.com/fwlink/p/?linkid=270945> which provides a detailed list of Persistent Chat features, how they work, and how to use them while running Persistent Chat Server.</span></span>

  - <span data-ttu-id="b1409-126">計画ドキュメントの [Lync server 2013 での常設チャットサーバーの計画](lync-server-2013-planning-for-persistent-chat-server.md) 展開ドキュメントの [lync server 2013 での常設チャットサーバーの展開](lync-server-2013-deploying-persistent-chat-server.md) 、 [Lync server 2010 からの移行、グループチャットまたは Office Communications server 2007 R2 グループチャットから Lync server 2013 への移行](migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server.md) 、移行 [ドキュメント](managing-lync-server-2013-persistent-chat-server.md) での常設チャットサーバー、常設チャットサーバーのセットアップ手順2013について説明します。</span><span class="sxs-lookup"><span data-stu-id="b1409-126">The [Planning for Persistent Chat Server in Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md) in the Planning documentation, [Deploying Persistent Chat Server in Lync Server 2013](lync-server-2013-deploying-persistent-chat-server.md) in the Deployment documentation, [Migration from Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server](migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server.md) in the Migration documentation, and [Managing Lync Server 2013, Persistent Chat Server](managing-lync-server-2013-persistent-chat-server.md) in the Operations documentation, all of which provide instructions for setting up Persistent Chat Server.</span></span>

  - <span data-ttu-id="b1409-127">常設チャットサーバー Documentation.msi ファイル (Windows Installer ファイル) を使うと、ユーザーは常設チャットサーバーに関する包括的なオフラインドキュメントにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="b1409-127">The Persistent Chat Server Documentation.msi file (Windows Installer file) lets users access comprehensive offline documentation about Persistent Chat Server.</span></span>

<div>

## <a name="key-topology-changes-for-persistent-chat-server"></a><span data-ttu-id="b1409-128">常設チャットサーバーの主要なトポロジの変更</span><span class="sxs-lookup"><span data-stu-id="b1409-128">Key Topology Changes for Persistent Chat Server</span></span>

<span data-ttu-id="b1409-129">常設チャットサーバーの次のような上位の変更があります。</span><span class="sxs-lookup"><span data-stu-id="b1409-129">The following high-level changes for Persistent Chat Server include:</span></span>

<span data-ttu-id="b1409-130">常設チャットサーバーがサーバーの役割になりました。</span><span class="sxs-lookup"><span data-stu-id="b1409-130">Persistent Chat Server is now a server role.</span></span> <span data-ttu-id="b1409-131">Microsoft Lync Server 2010 では、グループチャットサーバーは Microsoft Lync Server 2010 用のサードパーティの信頼済みアプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="b1409-131">In Microsoft Lync Server 2010, Group Chat Server was a third-party trusted application for Microsoft Lync Server 2010.</span></span> <span data-ttu-id="b1409-132">常設チャットは、トポロジビルダーを使用して、Lync Server 2013 トポロジに追加することができます。</span><span class="sxs-lookup"><span data-stu-id="b1409-132">Persistent Chat can be added to your Lync Server 2013 topology by using Topology Builder.</span></span> <span data-ttu-id="b1409-133">Lync Server 2013 では、次の3つの新しいサーバーの役割を使用して、常設チャットサーバー機能が実装されます。</span><span class="sxs-lookup"><span data-stu-id="b1409-133">In Lync Server 2013, Persistent Chat Server functionality is implemented by using three new server roles:</span></span>

  - <span data-ttu-id="b1409-134">**PersistentChatService:** これは、常設チャットのフロントエンドロールです。</span><span class="sxs-lookup"><span data-stu-id="b1409-134">**PersistentChatService:** This is the front end role for Persistent Chat.</span></span> <span data-ttu-id="b1409-135">Standard Edition の展開では、他の Lync Server の役割と同じように、ブートストラップによって展開された Standard Edition server に、常設チャットサーバーサービスの役割が併置されています。</span><span class="sxs-lookup"><span data-stu-id="b1409-135">In Standard Edition deployments, Persistent Chat Server Service Role is collocated on the Standard Edition server deployed by Bootstrapper, like any other Lync Server role.</span></span> <span data-ttu-id="b1409-136">Enterprise Edition の展開では、常設チャットサービスの役割は、他の Lync Server の役割と同じように、ブートストラップによってスタンドアロンコンピューターに展開されます。</span><span class="sxs-lookup"><span data-stu-id="b1409-136">In Enterprise Edition deployments, Persistent Chat Service Role is deployed on stand-alone computers by Bootstrapper, like any other Lync Server role.</span></span>

  - <span data-ttu-id="b1409-137">**PersistentChatStore:** 常設チャットコンテンツデータベースに対応し、すべてのチャットコンテンツが保存されているバックエンドサーバー。</span><span class="sxs-lookup"><span data-stu-id="b1409-137">**PersistentChatStore:** Back End Server that corresponds to the Persistent Chat content database, where all the chat content is stored.</span></span>

  - <span data-ttu-id="b1409-138">**PersistentChatComplianceStore:** 常設チャットのコンプライアンスデータベースに対応し、すべてのコンプライアンスイベントが保存されているバックエンドサーバーの役割。</span><span class="sxs-lookup"><span data-stu-id="b1409-138">**PersistentChatComplianceStore:** Back End Server role that corresponds to the Persistent Chat Compliance database, where all compliance events are stored.</span></span>

<span data-ttu-id="b1409-139">これらの常設チャットサーバーの役割はオプションであり、包括的な常設チャットサーバー機能を必要としているユーザーによってのみインストールされます。</span><span class="sxs-lookup"><span data-stu-id="b1409-139">These Persistent Chat Server roles are optional, and are installed only by customers who want comprehensive Persistent Chat Server functionality.</span></span> <span data-ttu-id="b1409-140">**PersistentChatComplianceStore** の役割は、常設チャットのコンプライアンスの展開を選んだ場合にのみ必要です。</span><span class="sxs-lookup"><span data-stu-id="b1409-140">The **PersistentChatComplianceStore** role is needed only if you choose to deploy Persistent Chat Compliance.</span></span>

<span data-ttu-id="b1409-141">**PersistentChatService** role は、次の2つのサービスを実行します。</span><span class="sxs-lookup"><span data-stu-id="b1409-141">The **PersistentChatService** role runs two services:</span></span>

  - <span data-ttu-id="b1409-142">常設チャットサービス</span><span class="sxs-lookup"><span data-stu-id="b1409-142">Persistent Chat service</span></span>

  - <span data-ttu-id="b1409-143">常設チャットのコンプライアンスサービス</span><span class="sxs-lookup"><span data-stu-id="b1409-143">Persistent Chat Compliance service</span></span>

<span data-ttu-id="b1409-144">これらのサービスを各常設チャットサーバーで実行すると、マルチサーバーの常設チャットサーバープールでこれらのサービスの高可用性が実現されます。</span><span class="sxs-lookup"><span data-stu-id="b1409-144">Having these services run on each Persistent Chat Server provides high availability for these services in a multiserver Persistent Chat Server pool.</span></span>

<span data-ttu-id="b1409-145">さらに、常設チャットルームでのファイルのアップロードとダウンロードをサポートするには、常設チャットサーバーに web サービスが用意されています。</span><span class="sxs-lookup"><span data-stu-id="b1409-145">Additionally, to support the file upload and download in Persistent Chat rooms, Persistent Chat Server includes a web service.</span></span> <span data-ttu-id="b1409-146">以前は、このサービスは永続的チャットサーバー、フロントエンドサーバー、必須のインターネットインフォメーションサービス (IIS) に、前提条件としてインストールされています。</span><span class="sxs-lookup"><span data-stu-id="b1409-146">Previously, this service was collocated on the Persistent Chat Server, Front End Server and required Internet Information Services (IIS) to be installed as a prerequisite.</span></span> <span data-ttu-id="b1409-147">Lync Server 2013 常設チャットサーバーでは、ファイルアップロード/ダウンロード web サービスは Lync Server 2013 フロントエンドサーバーと併置されています。</span><span class="sxs-lookup"><span data-stu-id="b1409-147">In Lync Server 2013 Persistent Chat Server, the File Upload/Download web service is collocated with the Lync Server 2013 Front End Server.</span></span> <span data-ttu-id="b1409-148">副次的効果として、インターネットインフォメーションサービス (IIS) は、常設チャットサーバーの前提条件を超えています。</span><span class="sxs-lookup"><span data-stu-id="b1409-148">As a side effect, Internet Information Services (IIS) is no longer a prerequisite for Persistent Chat Server.</span></span> <span data-ttu-id="b1409-149">ファイルのアップロード/ダウンロード web サービスは、インターネットインフォメーションサービス (IIS) マネージャーで **PersistentChat** として識別されます。</span><span class="sxs-lookup"><span data-stu-id="b1409-149">The File Upload/Download web service is identified as **PersistentChat** in the Internet Information Services (IIS) Manager.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="b1409-150"><STRONG>PersistentChatService</STRONG>の役割は、 &nbsp; フロントエンドサーバーが標準エディションのフロントエンドサーバーである場合にのみ、Lync Server 2013 フロントエンドサーバーと同じサーバーで実行でき &nbsp; ます。</span><span class="sxs-lookup"><span data-stu-id="b1409-150">The <STRONG>PersistentChatService</STRONG> role can run on the same server as a Lync Server 2013&nbsp;Front End Server only if that Front End Server is a Standard Edition&nbsp;Front End Server.</span></span> <span data-ttu-id="b1409-151"><STRONG>PersistentChatService</STRONG> role は、Lync Server 2013 フロントエンドサーバーとは独立して実行することはできません &nbsp; 。</span><span class="sxs-lookup"><span data-stu-id="b1409-151">The <STRONG>PersistentChatService</STRONG> role cannot run independently of a Lync Server 2013&nbsp;Front End Server.</span></span> <span data-ttu-id="b1409-152">このツールは、Lync Server 2013 展開のコンテキストでのみインストールできます。</span><span class="sxs-lookup"><span data-stu-id="b1409-152">It can be installed only in the context of a Lync Server 2013 deployment.</span></span>



</div>

<span data-ttu-id="b1409-153">常設チャットサーバーでは、Lookup サービスは廃止されました。</span><span class="sxs-lookup"><span data-stu-id="b1409-153">In Persistent Chat Server, Lookup service has been eliminated.</span></span> <span data-ttu-id="b1409-154">Lync Server 2010 のグループチャットでは、検索サービスはすべてのグループチャットサーバーフロントエンドサーバーで実行され、チャネルサーバーの1つへのルーティングが実行されました。</span><span class="sxs-lookup"><span data-stu-id="b1409-154">In Lync Server 2010, Group Chat, the Lookup service ran on every Group Chat Server Front End Server, and performed routing to one of the Channel Servers.</span></span> <span data-ttu-id="b1409-155">Lync Server 2013 は、[連絡先オブジェクト] を使ってルーティングを利用します。各常設チャットサーバープールは、適切な常設チャットサーバープールと、プール内の常設チャットサーバーを実行しているコンピューターのいずれかに要求をルーティングするために、Lync Server のフロントエンドサーバーで使用される連絡先オブジェクトで表されます。</span><span class="sxs-lookup"><span data-stu-id="b1409-155">Lync Server 2013 relies on routing by using contact objects, where each Persistent Chat Server pool is represented by a contact object that is used by the Lync Server Front End Servers to identify and route requests to an appropriate Persistent Chat Server pool, and to one of the computers running Persistent Chat Server in the pool.</span></span>

<span data-ttu-id="b1409-156">Lync Server 2013 には、コンプライアンスサービスの変更があります。</span><span class="sxs-lookup"><span data-stu-id="b1409-156">In Lync Server 2013, there are Compliance service modifications:</span></span>

  - <span data-ttu-id="b1409-157">Lync Server 2010 では、コンプライアンスサービスがスタンドアロン (併置されていない) で実行され、1つのサーバーでのみ実行されています。</span><span class="sxs-lookup"><span data-stu-id="b1409-157">In Lync Server 2010, the Compliance service ran stand-alone (non-collocated), and only on a single server.</span></span> <span data-ttu-id="b1409-158">コンプライアンスサービスは、常設チャットサービスと共にすべての常設チャットサーバーのフロントエンドサーバーで実行されるようになり、マルチサーバーの常設チャットサーバープールで高可用性を実現します。</span><span class="sxs-lookup"><span data-stu-id="b1409-158">The Compliance service now runs on all the Persistent Chat Server Front End Servers, alongside the Persistent Chat service, and thereby provides high availability in a multiserver Persistent Chat Server pool.</span></span> <span data-ttu-id="b1409-159">1つのコンプライアンスアダプターは、コンプライアンスデータベースからデータを抽出するように構成することができます (XML ファイル、Exchange でホストされるアーカイブなど)。</span><span class="sxs-lookup"><span data-stu-id="b1409-159">A single compliance adapter can be configured to extract data from the compliance database and into one of the other systems (XML file, Exchange-hosted archives, and so on).</span></span> <span data-ttu-id="b1409-160">常設チャットサーバーには XML アダプターが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b1409-160">Persistent Chat Server includes an XML adapter.</span></span>

  - <span data-ttu-id="b1409-161">常設チャットサービスで共有されるメッセージキュー (MSMQ とも呼ばれます) キューと、各常設チャットサーバーのフロントエンドサーバーのコンプライアンスサービスは、2つのサービスによってのみ共有されるプライベートキューになりました。</span><span class="sxs-lookup"><span data-stu-id="b1409-161">The Message Queuing (also known as MSMQ) queue that is shared by the Persistent Chat service and the Compliance service on each Persistent Chat Server Front End Server is now a private queue shared only by the two services.</span></span> <span data-ttu-id="b1409-162">すべてのコンプライアンスサービスは、同じコンプライアンスバックエンドデータベースに書き込みを行います。</span><span class="sxs-lookup"><span data-stu-id="b1409-162">All compliance services write to the same Compliance Back End database.</span></span> <span data-ttu-id="b1409-163">また、これらのユーザーは、アダプターのインスタンスにデータを送信する目的で、そのデータベースからすべて読み取ります。</span><span class="sxs-lookup"><span data-stu-id="b1409-163">They also all read from that database, for the purpose of sending the data to their instance of the adapter.</span></span> <span data-ttu-id="b1409-164">コンプライアンスバックエンドサーバーは、新しいバックエンドサーバーの役割として表されます。</span><span class="sxs-lookup"><span data-stu-id="b1409-164">The Compliance Back End Server is represented as a new Back End Server role.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="b1409-165">以前のバージョンと同様に、すべてのコンプライアンスデータは1回のみ処理されます。</span><span class="sxs-lookup"><span data-stu-id="b1409-165">As in previous versions, all compliance data is processed only once.</span></span> <span data-ttu-id="b1409-166">データは、さまざまな Lync Server 2013、常設チャットサーバーコンピューターで実行されているコンプライアンスサービスによって呼び出されたいずれかのアダプターインスタンスによって処理される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b1409-166">The data may be processed by any of the adapter instances invoked by the compliance service running on the various Lync Server 2013, Persistent Chat Server computers.</span></span> <span data-ttu-id="b1409-167">常設チャットサーバーでは、いずれかのアダプターインスタンスでデータを処理できます。</span><span class="sxs-lookup"><span data-stu-id="b1409-167">In Persistent Chat Server, any one of the adapter instances could process the data.</span></span>

    
    </div>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="b1409-168">メッセージキューのインストールの詳細については、展開ドキュメントの「 <A href="lync-server-2013-install-operating-systems-and-prerequisite-software-on-servers.md">Lync Server 2013 のサーバーにオペレーティングシステムと必須ソフトウェアをインストール</A> する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b1409-168">For information about installing Message Queuing, see <A href="lync-server-2013-install-operating-systems-and-prerequisite-software-on-servers.md">Install operating systems and prerequisite software on servers for Lync Server 2013</A> in the Deployment documentation.</span></span>

    
    </div>

<span data-ttu-id="b1409-169">Lync Server 2013 では、高可用性と障害回復の両方が強化されています。</span><span class="sxs-lookup"><span data-stu-id="b1409-169">In Lync Server 2013, there are improvements in both high availability and disaster recovery:</span></span>

  - <span data-ttu-id="b1409-170">高可用性の強化: SQL Server のミラーリングは、常設チャットサーバーコンテンツデータベースと永続的なチャットのコンプライアンスデータベース (インサイト) で高可用性を実現するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b1409-170">High availability improvements: SQL Server mirroring is used to provide high availability for the Persistent Chat Server content database and Persistent Chat compliance database within a data center (in-site).</span></span>

  - <span data-ttu-id="b1409-171">障害回復機能の改善: 常設チャットサーバーは、2つのサイト間で1つの常設チャットサーバープールを拡張できるようにする、ストレッチプールアーキテクチャをサポートしています (つまり、トポロジの1つの論理プールであり、2つのサイトに物理的に配置されたプール内のサーバーを使用します)。</span><span class="sxs-lookup"><span data-stu-id="b1409-171">Disaster recovery improvements: Persistent Chat Server supports a stretched pool architecture that enables a single Persistent Chat Server pool to be stretched across two sites (that is, a single logical pool in the topology, with servers in the pool physically located across two sites).</span></span> <span data-ttu-id="b1409-172">SQL Server のログ配布は、クロスサイトの障害回復に使用されます。</span><span class="sxs-lookup"><span data-stu-id="b1409-172">SQL Server Log Shipping is used for cross-site disaster recovery.</span></span>

<span data-ttu-id="b1409-173">高可用性と障害回復の詳細については、「展開ドキュメントの [Lync server 2013 で高可用性と障害復旧のための常設チャットサーバーを構成](lync-server-2013-configuring-persistent-chat-server-for-high-availability-and-disaster-recovery.md) する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b1409-173">For more information about high availability and disaster recovery, see [Configuring Persistent Chat Server for high availability and disaster recovery in Lync Server 2013](lync-server-2013-configuring-persistent-chat-server-for-high-availability-and-disaster-recovery.md) in the Deployment documentation.</span></span>

</div>

<div>

## <a name="key-administration-and-management-changes-for-persistent-chat-server"></a><span data-ttu-id="b1409-174">常設チャットサーバーのキーの管理と管理の変更</span><span class="sxs-lookup"><span data-stu-id="b1409-174">Key Administration and Management Changes for Persistent Chat Server</span></span>

<span data-ttu-id="b1409-175">Lync Server 2013 では、次のような方法で永続的なチャットサーバーの管理と管理が簡単になりました。</span><span class="sxs-lookup"><span data-stu-id="b1409-175">Lync Server 2013 has made it easier to administer and manage Persistent Chat Server by providing:</span></span>

  - <span data-ttu-id="b1409-176">管理の統合</span><span class="sxs-lookup"><span data-stu-id="b1409-176">Unified administration and management.</span></span> <span data-ttu-id="b1409-177">Lync Server 2013 を使用すると、Lync 管理者が既に使い慣れているツールを使用して、より簡単に永続的なチャットサーバーの管理と管理を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="b1409-177">Lync Server 2013 makes it easier to manage and administer Persistent Chat Server by using tools that are already familiar to Lync administrators.</span></span> <span data-ttu-id="b1409-178">常設チャットサーバーには、Lync Server コントロールパネルと統合された管理ユーザーインターフェイスエクスペリエンスが含まれています。これは、グループチャットサーバーのユーザーインターフェイスの以前のバージョンに関するパフォーマンスの問題に対処するものです。</span><span class="sxs-lookup"><span data-stu-id="b1409-178">Persistent Chat Server includes an administrative user interface experience that is integrated with the Lync Server Control Panel, which addresses performance issues with the previous versions of the Group Chat Server user interface.</span></span> <span data-ttu-id="b1409-179">また、常設チャットサーバーには Windows PowerShell コマンドレットのコレクションが含まれており、常設チャットサーバーのカテゴリ、常設チャットサーバールーム (会議室の削除、廃止されたコンテンツの削除を含む)、アドインを管理して管理します。</span><span class="sxs-lookup"><span data-stu-id="b1409-179">Also, Persistent Chat Server includes a collection of Windows PowerShell cmdlets to administer and manage Persistent Chat Server categories, Persistent Chat Server rooms (including deleting rooms and purging obsolete content), and add-ins.</span></span>

  - <span data-ttu-id="b1409-180">簡素化された管理モデル。</span><span class="sxs-lookup"><span data-stu-id="b1409-180">Simplified administration model.</span></span> <span data-ttu-id="b1409-181">Lync Server 2013 は、次の主要な顧客要件に対応して、常設チャットサーバーモデルを変更し、簡素化しました。</span><span class="sxs-lookup"><span data-stu-id="b1409-181">Lync Server 2013 has changed and simplified the Persistent Chat Server model by addressing the following key customer requirements:</span></span>
    
      - <span data-ttu-id="b1409-182">スコープとカテゴリの複雑な入れ子になった階層を削除します。</span><span class="sxs-lookup"><span data-stu-id="b1409-182">Remove the complex nested hierarchies of scopes and categories.</span></span>
    
      - <span data-ttu-id="b1409-183">許可リストと、現在の MindAlign のユーザーに対して許可されているリスト (スコープ) と、常設チャットサーバーへの移行を計画していることをサポートします。</span><span class="sxs-lookup"><span data-stu-id="b1409-183">Support to define deny lists as well as allowed lists (scopes) for current MindAlign customers who are planning to migrate to Persistent Chat Server.</span></span>

</div>

<div>

## <a name="whats-different-about-user-roles-from-previous-group-chat-server-versions"></a><span data-ttu-id="b1409-184">グループチャットサーバの以前のバージョンからのユーザロールについては、どのような違いがありますか?</span><span class="sxs-lookup"><span data-stu-id="b1409-184">What’s Different about User Roles from Previous Group Chat Server Versions?</span></span>

<span data-ttu-id="b1409-185">Lync Server 2010 のグループチャットには、ユーザー管理者の役割、チャットルーム管理者の役割、アドインを管理できる Lync Server 管理者の役割があります。常設チャットサーバーは、常設チャット管理者の役割 (他の Lync Server ロールベースのアクセス制御 (RBAC) ロールに似ています) を提供します。</span><span class="sxs-lookup"><span data-stu-id="b1409-185">Lync Server 2010, Group Chat had a user administrator role, a chat room administrator role and a Lync Server administrator role that could manage add-ins. Persistent Chat Server simply provides a Persistent Chat Administrator role (which is similar to other Lync Server role-based access control (RBAC) roles).</span></span> <span data-ttu-id="b1409-186">この RBAC ロールのメンバーであればだれでも、チャットルーム、アドイン、カテゴリ (そのため、これらのカテゴリのユーザーアクセスを取得)、および常設チャットサーバープールの構成を管理できます。</span><span class="sxs-lookup"><span data-stu-id="b1409-186">Anyone who is a member of this RBAC role can manage chat rooms, add-ins, and categories (and therefore gain user access for these categories), and configuration of the Persistent Chat Server pool.</span></span>

</div>

<div>

## <a name="whats-different-about-chat-room-categories-from-previous-group-chat-server-versions"></a><span data-ttu-id="b1409-187">チャットルームのカテゴリについては、以前のグループチャットサーバのバージョンとはどのような違いがありますか?</span><span class="sxs-lookup"><span data-stu-id="b1409-187">What’s Different about Chat Room Categories from Previous Group Chat Server Versions?</span></span>

<span data-ttu-id="b1409-188">チャットルームのカテゴリを入れ子にすることはできなくなり、ルートカテゴリを変更することはできなくなりました。</span><span class="sxs-lookup"><span data-stu-id="b1409-188">Chat room categories can no longer be nested, and the root category can no longer be modified.</span></span> <span data-ttu-id="b1409-189">AllowedMembers/DeniedMembers は、従来のグループチャットサーバーバージョンで使用されていたスコープ (拒否されたリストの指定をサポートしていないことを除く) を構成します。</span><span class="sxs-lookup"><span data-stu-id="b1409-189">AllowedMembers/DeniedMembers comprise what a scope used to be in legacy Group Chat Server versions (except that it didn’t support specifying a Denied list).</span></span> <span data-ttu-id="b1409-190">スコープは入れ子になっていないため、無効にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="b1409-190">Scopes can no longer be overridden, because there are no nested categories.</span></span> <span data-ttu-id="b1409-191">Lync Server 2013 の常設チャット管理者は、チャットルームのカテゴリを作成して管理することができます。</span><span class="sxs-lookup"><span data-stu-id="b1409-191">A Persistent Chat Administrator in Lync Server 2013 can create and manage chat room categories.</span></span> <span data-ttu-id="b1409-192">チャットルームカテゴリの作成と管理の一環として、常設チャット管理者は、特定のカテゴリのチャットルームのメンバー/作成者としてアクセスできるプリンシパル (Active Directory グループ/コンテナー/ユーザー) を構成することができます。</span><span class="sxs-lookup"><span data-stu-id="b1409-192">As part of creating and managing chat room categories, a Persistent Chat Administrator can configure principals (Active Directory groups/containers/users) that have access to be members/creators of chat rooms of a particular category.</span></span> <span data-ttu-id="b1409-193">常設チャット管理者は、カテゴリに DeniedMembers を追加することもできます。これは、許可リストに明示的に除外されることになります。</span><span class="sxs-lookup"><span data-stu-id="b1409-193">A Persistent Chat Administrator can also add DeniedMembers to a category, and these become explicit exclusions to the allowed list.</span></span> <span data-ttu-id="b1409-194">拒否されたメンバーは許可されたメンバーより優先されます。</span><span class="sxs-lookup"><span data-stu-id="b1409-194">DeniedMembers override what’s in AllowedMembers.</span></span>

</div>

<div>

## <a name="whats-different-about-chat-room-properties-from-previous-group-chat-server-versions"></a><span data-ttu-id="b1409-195">チャットルームのプロパティについては、以前のグループチャットサーバのバージョンとはどのような違いがありますか?</span><span class="sxs-lookup"><span data-stu-id="b1409-195">What’s Different about Chat Room Properties from Previous Group Chat Server Versions?</span></span>

<span data-ttu-id="b1409-196">オープンチャットルームの新しい概念は、Lync Server 2013 の常設チャットサーバーにあります。</span><span class="sxs-lookup"><span data-stu-id="b1409-196">A new concept of open chat rooms exists in Lync Server 2013, Persistent Chat Server.</span></span> <span data-ttu-id="b1409-197">このチャットルームには、排他的なメンバーシップなしで、許可されているすべてのメンバーが参加できます。</span><span class="sxs-lookup"><span data-stu-id="b1409-197">All allowed members can join the chat room, without exclusive membership.</span></span>

<span data-ttu-id="b1409-198">以前のバージョンの常設チャットサーバーに含まれていた次のチャットルームのプロパティは廃止されました。</span><span class="sxs-lookup"><span data-stu-id="b1409-198">The following chat room properties that were included in previous versions of Persistent Chat Server have been eliminated:</span></span>

  - <span data-ttu-id="b1409-199">トピック: 会議室には、説明しかありません。</span><span class="sxs-lookup"><span data-stu-id="b1409-199">Topic: A Room now only has a Description.</span></span>

  - <span data-ttu-id="b1409-200">新しいメンバーリストの作成: 常設チャットサーバーでは、すべてのチャットルームが空のメンバーシップで開始されます。また、メンバーのメンバーシップを最大化することもできます。</span><span class="sxs-lookup"><span data-stu-id="b1409-200">Create New Member list: In Persistent Chat Server, all chat rooms start with empty membership (and can maximize to a membership equaling the Allowed Members).</span></span>

  - <span data-ttu-id="b1409-201">ファイルアップロード: チャットルームごとの設定で、ファイルのアップロードとダウンロードが許可されたかどうかを制御します。</span><span class="sxs-lookup"><span data-stu-id="b1409-201">File Upload: Used to be a setting per chat room to control whether file upload/downloads were allowed.</span></span> <span data-ttu-id="b1409-202">これでカテゴリレベルのみが設定され、そのカテゴリのすべてのルームに適用されます。</span><span class="sxs-lookup"><span data-stu-id="b1409-202">This is now set only the category level and applies to all rooms in that category.</span></span>

  - <span data-ttu-id="b1409-203">チャット履歴: チャット履歴が有効になっているかどうかを制御するために、チャットルームごとに設定されていますが、これではカテゴリレベルでのみ設定され、そのカテゴリ内のすべてのルームに適用されます。</span><span class="sxs-lookup"><span data-stu-id="b1409-203">Chat History: Used to be a setting per chat room to control if Chat History was enabled, but is now set only at the category level and applies to all rooms in that category.</span></span>

  - <span data-ttu-id="b1409-204">招待: 会議室は、カテゴリの [招待] 設定を常に継承します。または、ルームで無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="b1409-204">Invites: A room always inherits the Invites setting for the category; or it can be turned off on the room.</span></span> <span data-ttu-id="b1409-205">このカテゴリが以前に「オフ」に設定されている場合、チャットルームは「招待」を有効にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="b1409-205">A room cannot turn on Invites if the category was previously set to Invites off.</span></span>

</div>

<div>

## <a name="whats-different-about-policies-from-previous-group-chat-server-versions"></a><span data-ttu-id="b1409-206">グループチャットサーバの以前のバージョンのポリシーについては、どのような違いがありますか?</span><span class="sxs-lookup"><span data-stu-id="b1409-206">What’s Different about Policies from Previous Group Chat Server Versions?</span></span>

<span data-ttu-id="b1409-207">常設チャットサーバーでは、ユーザー/プール/サイト/グローバル設定ごとに常設チャットを使用して、新しい Lync ポリシーが有効になっています。</span><span class="sxs-lookup"><span data-stu-id="b1409-207">Persistent Chat Server has a new Lync policy enabled with Persistent Chat, per user/pool/site/global settings.</span></span> <span data-ttu-id="b1409-208">Lync 2013 クライアントの常設チャット環境は、常設チャットのポリシーによって有効になっているユーザー (直接またはプール/サイト/グローバル設定) でのみ利用できます。</span><span class="sxs-lookup"><span data-stu-id="b1409-208">In the Lync 2013 client, the Persistent Chat environment is available only for users who are enabled by policy for Persistent Chat (either directly or through the pool/site/global setting).</span></span>

<span data-ttu-id="b1409-209">グループチャットサーバーの以前のバージョンには、Lync Server ポリシーに統合されたポリシーがありませんでした。</span><span class="sxs-lookup"><span data-stu-id="b1409-209">Previous versions of Group Chat Server did not have any policies integrated into the Lync Server policies.</span></span> <span data-ttu-id="b1409-210">ユーザーごとおよびカテゴリごとに、[ユーザーごとに **ファイルをアップロード可能** ] 機能を使用して、ユーザーをユーザー管理者、チャットルーム管理者、またはユーザーがファイルをアップロードできるように構成することができます。</span><span class="sxs-lookup"><span data-stu-id="b1409-210">On a per user and per category/room basis, by using the **Can Upload Files** per user feature, you could make the user a User administrator, a chat room administrator, or configure the user’s ability to upload files.</span></span> <span data-ttu-id="b1409-211">常設チャットサーバーの **ファイルアップロード** 機能は、1つのカテゴリに分類されます。</span><span class="sxs-lookup"><span data-stu-id="b1409-211">The Persistent Chat Server **File Upload** feature is just per category.</span></span>

</div>

<div>

## <a name="logging"></a><span data-ttu-id="b1409-212">ログ記録</span><span class="sxs-lookup"><span data-stu-id="b1409-212">Logging</span></span>

<span data-ttu-id="b1409-213">常設チャットサーバーと System Center Operations Manager のログは、Lync Server 2013 のトレースログに統合されています。</span><span class="sxs-lookup"><span data-stu-id="b1409-213">Logging for Persistent Chat Server and System Center Operations Manager is integrated into the Lync Server 2013 trace logging.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="b1409-214">関連項目</span><span class="sxs-lookup"><span data-stu-id="b1409-214">See Also</span></span>


[<span data-ttu-id="b1409-215">Lync Server 2013 での常設チャット サーバーの計画</span><span class="sxs-lookup"><span data-stu-id="b1409-215">Planning for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-planning-for-persistent-chat-server.md)  
  

<span data-ttu-id="b1409-216"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b1409-216"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>
