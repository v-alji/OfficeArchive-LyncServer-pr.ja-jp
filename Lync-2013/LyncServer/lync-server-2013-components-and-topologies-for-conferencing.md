---
title: 'Lync Server 2013: 会議のコンポーネントおよびトポロジ'
description: Lync Server 2013 の会議用のコンポーネントとトポロジ。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components and topologies for conferencing
ms:assetid: eb83052a-3360-4ba1-a6a0-6ee419942809
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399061(v=OCS.15)
ms:contentKeyID: 48185707
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 719fe81d0f634b1eab1e79c2e7e665e89b0a791a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434628"
---
# <a name="components-and-topologies-for-conferencing-in-lync-server-2013"></a><span data-ttu-id="76c06-103">Lync Server 2013 の会議のコンポーネントおよびトポロジ</span><span class="sxs-lookup"><span data-stu-id="76c06-103">Components and topologies for conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="76c06-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="76c06-104">

<span> </span></span></span>

<span data-ttu-id="76c06-105">_**最終更新日:** 2013-02-04_</span><span class="sxs-lookup"><span data-stu-id="76c06-105">_**Topic Last Modified:** 2013-02-04_</span></span>

<span data-ttu-id="76c06-106">[トポロジビルダー] で [会議] を選択すると、会議はフロントエンドサーバーまたは Standard Edition サーバーの一部として展開されます。</span><span class="sxs-lookup"><span data-stu-id="76c06-106">When you select conferencing in Topology Builder, conferencing is deployed as part of the Front End Server or Standard Edition server.</span></span> <span data-ttu-id="76c06-107">ダイヤルイン会議と PowerPoint 共有には、追加のコンポーネントと構成が必要です。</span><span class="sxs-lookup"><span data-stu-id="76c06-107">Dial-in conferencing and PowerPoint sharing requires additional components and configuration.</span></span> <span data-ttu-id="76c06-108">以下のセクションでは、web 会議、A/V 会議、ダイヤルイン会議でサポートされているコンポーネントとトポロジについて説明します。</span><span class="sxs-lookup"><span data-stu-id="76c06-108">The following sections describe the supported components and topologies for web conferencing, A/V conferencing, and dial-in conferencing.</span></span>

<div>

## <a name="supported-components"></a><span data-ttu-id="76c06-109">サポートされているコンポーネント</span><span class="sxs-lookup"><span data-stu-id="76c06-109">Supported Components</span></span>

<span data-ttu-id="76c06-110">唯一のコンポーネント web 会議と A/V 会議が必要なのは、組織のフロントエンドサーバーまたは Standard Edition サーバーだけです。</span><span class="sxs-lookup"><span data-stu-id="76c06-110">The only components web conferencing and A/V conferencing require are your organization’s Front End Servers or Standard Edition servers.</span></span> <span data-ttu-id="76c06-111">フロントエンドサーバーおよび Standard Edition サーバーのハードウェアとソフトウェアの要件の一覧については、「[サポートされているハードウェアと lync 2013 server 2013 の](lync-server-2013-supported-hardware.md)[サーバーソフトウェアおよびサーバーソフトウェアとインフラストラクチャのサポート](lync-server-2013-server-software-and-infrastructure-support.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="76c06-111">For a list of hardware and software requirements for the Front End Servers and Standard Edition servers, see [Supported hardware for Lync Server 2013](lync-server-2013-supported-hardware.md) and [Server software and infrastructure support in Lync Server 2013](lync-server-2013-server-software-and-infrastructure-support.md).</span></span>

<span data-ttu-id="76c06-112">Lync Server 2013 は、PowerPoint プレゼンテーションの共有とレンダリングを処理するために、Office Web Apps と Office Web Apps サーバーを使用します。</span><span class="sxs-lookup"><span data-stu-id="76c06-112">Lync Server 2013 uses Office Web Apps and the Office Web Apps Server to handle sharing and rendering of PowerPoint presentations.</span></span> <span data-ttu-id="76c06-113">Office Web Apps サーバーのインストールと構成の詳細については、「 [Office Web Apps サーバーおよび Lync server 2013 との統合を構成する](lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="76c06-113">For details about installing and configuring the Office Web Apps Server, see [Configuring integration with Office Web Apps Server and Lync Server 2013](lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md).</span></span>

<span data-ttu-id="76c06-114">ダイヤルイン会議では、web 会議と A/V 会議の要件に加えて、次の Lync Server 2013 コンポーネントを使用します。</span><span class="sxs-lookup"><span data-stu-id="76c06-114">In addition to the requirements for web conferencing and A/V conferencing, dial-in conferencing uses the following Lync Server 2013 components:</span></span>

  - <span data-ttu-id="76c06-115">**アプリケーションサービス**   アプリケーションサービスは、統合コミュニケーション (UC) アプリケーションの展開、ホスティング、管理のためのプラットフォームを提供します。</span><span class="sxs-lookup"><span data-stu-id="76c06-115">**Application service**   Application service provides a platform for deploying, hosting, and managing unified communications (UC) applications.</span></span> <span data-ttu-id="76c06-116">[ダイヤルイン会議] では、アプリケーションサービスが必要な2つの UC アプリケーション (会議アテンダントと会議のお知らせ) を使用します。</span><span class="sxs-lookup"><span data-stu-id="76c06-116">Dial-in conferencing uses two UC applications that require Application service: Conferencing Attendant and Conferencing Announcement.</span></span> <span data-ttu-id="76c06-117">アプリケーションサービスは、電話会議のワークロードを展開して、[ダイヤルイン会議] オプションを選択すると、フロントエンドプールのすべてのフロントエンドサーバーと、すべての Standard Edition サーバーで既定でインストールされ、有効になります。</span><span class="sxs-lookup"><span data-stu-id="76c06-117">Application service is installed and activated by default on every Front End Server in a Front End pool and on every Standard Edition server when you deploy a Conferencing workload and select the dial-in conferencing option.</span></span>

  - <span data-ttu-id="76c06-118">**会議アテンダントアプリケーション**   会議アテンダントアプリケーションは、公衆交換電話網 (PSTN) 通話、プロンプトの再生、A/V 会議への通話の参加を行う、統合された通信アプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="76c06-118">**Conferencing Attendant application**   Conferencing Attendant application is a unified communications application that accepts public switched telephone network (PSTN) calls, plays prompts, and joins the calls to an A/V conference.</span></span> <span data-ttu-id="76c06-119">会議のワークロードを展開して、[ダイヤルイン会議] オプションを選択すると、会議アテンダントアプリケーションが既定でインストールされ、有効になります。</span><span class="sxs-lookup"><span data-stu-id="76c06-119">Conferencing Attendant application is installed and activated by default when you deploy a Conferencing workload and select the dial-in conferencing option.</span></span>

  - <span data-ttu-id="76c06-120">**会議のお知らせアプリケーション**   会議のお知らせアプリケーションは、参加者が会議に参加または退出したとき、参加者がミュートまたはミュートしたとき、会議ロビーに入っているユーザー、または会議がロックまたはロック解除されている場合など、特定のアクションについて PSTN の参加者に対してトーンを再生し、PSTN 参加者にメッセージを表示するユニファイドコミュニケーションアプリケーション</span><span class="sxs-lookup"><span data-stu-id="76c06-120">**Conferencing Announcement application**   Conferencing Announcement application is a unified communications application that plays tones and prompts to PSTN participants on certain actions, such as when participants join or leave a conference, participants are muted or unmuted, someone enters the conference lobby, or the conference is locked or unlocked.</span></span> <span data-ttu-id="76c06-121">会議アナウンスメントアプリケーションでは、電話のキーパッドからのデュアルトーンマルチ周波数 (DTMF) コマンドもサポートされています。</span><span class="sxs-lookup"><span data-stu-id="76c06-121">Conferencing Announcement application also supports dual-tone multifrequency (DTMF) commands from the phone keypad.</span></span> <span data-ttu-id="76c06-122">会議のワークロードを展開して、[ダイヤルイン会議] オプションを選択すると、会議のお知らせアプリケーションが既定で自動的にインストールされ、有効になります。</span><span class="sxs-lookup"><span data-stu-id="76c06-122">Conferencing Announcement application is automatically installed and activated by default when you deploy a Conferencing workload and select the dial-in conferencing option.</span></span>

  - <span data-ttu-id="76c06-123">**[ダイヤルイン会議の設定] ページ**   [ダイヤルイン会議の設定] ページには、利用可能な言語を含む会議のダイヤルイン番号、割り当てられている会議情報 (スケジュールされていない会議)、会議中の DTMF コントロールが表示され、個人識別番号 (PIN) と割り当てられた会議情報の管理がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="76c06-123">**Dial-in Conferencing Settings page**   The Dial-in Conferencing Settings page displays conference dial-in numbers with their available languages, assigned conference information (that is, for meetings that do not need to be scheduled), and in-conference DTMF controls, and supports management of personal identification number (PIN) and assigned conferencing information.</span></span> <span data-ttu-id="76c06-124">ダイヤルイン会議の設定ページは、Web サービスの一部として自動的にインストールされます。</span><span class="sxs-lookup"><span data-stu-id="76c06-124">The Dial-in Conferencing Settings page is automatically installed as part of Web Services.</span></span>

  - <span data-ttu-id="76c06-125">**Lync server 2013、仲介サーバー、PSTN ゲートウェイ**   ダイヤルイン会議には、Lync Server 2013 と PSTN ゲートウェイの間でシグナリング (およびメディア) を変換するための仲介サーバーと、仲介サーバーと PSTN ゲートウェイ間のシグナリングとメディアを変換する PSTN ゲートウェイが必要です。</span><span class="sxs-lookup"><span data-stu-id="76c06-125">**Lync Server 2013, Mediation Server and PSTN gateway**   Dial-in conferencing requires a Mediation Server to translate signaling (and media, in some configurations) between Lync Server 2013 and the PSTN gateway, and a PSTN gateway to translate signaling and media between the Mediation Server and the PSTN gateway.</span></span> <span data-ttu-id="76c06-126">ダイヤルイン会議の場合、少なくとも1つの仲介サーバーと、少なくとも次のいずれかを展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="76c06-126">For dial-in conferencing, you must deploy at least one Mediation Server and at least one of the following:</span></span>
    
      - <span data-ttu-id="76c06-127">PSTN ゲートウェイ</span><span class="sxs-lookup"><span data-stu-id="76c06-127">PSTN gateway</span></span>
    
      - <span data-ttu-id="76c06-128">IP-PBX</span><span class="sxs-lookup"><span data-stu-id="76c06-128">IP-PBX</span></span>
    
      - <span data-ttu-id="76c06-129">セッション ボーダー コントローラー (SBC) (SIP トランクを構成して接続するインターネット テレフォニー サービス プロバイダー (ITSP) のため)</span><span class="sxs-lookup"><span data-stu-id="76c06-129">Session Border Controller (SBC) (for an Internet telephony service provider to which you connect by configuring a SIP trunk)</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="76c06-130">エンタープライズ Voip も展開している場合、仲介サーバーと PSTN ゲートウェイはエンタープライズ Voip 展開の一部です。</span><span class="sxs-lookup"><span data-stu-id="76c06-130">If you are also deploying Enterprise Voice, Mediation Server and PSTN gateways are part of the Enterprise Voice deployment.</span></span> <span data-ttu-id="76c06-131">エンタープライズ Voip を展開していない場合は、少なくとも1つの仲介サーバーと、少なくとも1つの PSTN ゲートウェイ、IP PBX、またはダイヤルイン会議用の SBC を展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="76c06-131">If you are not deploying Enterprise Voice, you need to deploy at least one Mediation Server and at least one PSTN gateway, IP-PBX, or SBC for dial-in conferencing.</span></span>

    
    </div>

  - <span data-ttu-id="76c06-132">**ファイルストア**   ファイルストアは、記録された名前のオーディオファイルに使用されます。</span><span class="sxs-lookup"><span data-stu-id="76c06-132">**File store**   File store is used for recorded name audio files.</span></span> <span data-ttu-id="76c06-133">ファイルストアは、すべての Enterprise Edition または Standard Edition の展開における標準的なコンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="76c06-133">File Store is a standard component in every Enterprise Edition or Standard Edition deployment.</span></span>

  - <span data-ttu-id="76c06-134">**ユーザーストア**   ユーザーストアは、ユーザーの Lync Server 2013 Pin の保存に使用されます。</span><span class="sxs-lookup"><span data-stu-id="76c06-134">**User store**   User store is used to store user Lync Server 2013 PINs.</span></span> <span data-ttu-id="76c06-135">ピンはハッシュされています。</span><span class="sxs-lookup"><span data-stu-id="76c06-135">PINs are hashed.</span></span> <span data-ttu-id="76c06-136">ユーザーストアは、すべての Enterprise Edition または Standard Edition の展開における標準的なコンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="76c06-136">The User store is a standard component in every Enterprise Edition or Standard Edition deployment.</span></span>

  - <span data-ttu-id="76c06-137">**Lync Server コントロールパネル**   一部のダイヤルイン設定は、Lync Server コントロールパネルを使用して構成できます。</span><span class="sxs-lookup"><span data-stu-id="76c06-137">**Lync Server Control Panel**   Some dial-in settings can be configured by using Lync Server Control Panel.</span></span>

  - <span data-ttu-id="76c06-138">**Lync Server 管理シェル**   すべてのダイヤルイン設定は、Lync Server 管理シェルコマンドレットを使用して構成できます。</span><span class="sxs-lookup"><span data-stu-id="76c06-138">**Lync Server Management Shell**   All dial-in settings can be configured by using Lync Server Management Shell cmdlets.</span></span> <span data-ttu-id="76c06-139">Lync Server 管理シェルコマンドレットを使用して、会議アテンダントアプリケーションと会議アナウンスメントアプリケーションの展開、構成、実行、監視、トラブルシューティングを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="76c06-139">Lync Server Management Shell cmdlets are available for deploying, configuring, running, monitoring, and troubleshooting Conferencing Attendant application and Conferencing Announcement application.</span></span> <span data-ttu-id="76c06-140">特定のコマンドレットの詳細については、「Lync Server 管理シェルのドキュメント」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="76c06-140">For details about specific cmdlets, see Lync Server Management Shell documentation.</span></span>

</div>

<div>

## <a name="supported-topologies"></a><span data-ttu-id="76c06-141">サポートされるトポロジ</span><span class="sxs-lookup"><span data-stu-id="76c06-141">Supported Topologies</span></span>

<span data-ttu-id="76c06-142">Lync Server 2013 では、会議サービスを実行しているサーバーは、常にフロントエンドサーバーまたは Standard Edition サーバーと併置されます。</span><span class="sxs-lookup"><span data-stu-id="76c06-142">In Lync Server 2013, the server running conferencing services is always collocated with the Front End Servers or Standard Edition servers.</span></span> <span data-ttu-id="76c06-143">最初の展開時に、トポロジビルダーにより、お客様のトポロジに会議を含めるオプションが提供されます。</span><span class="sxs-lookup"><span data-stu-id="76c06-143">During your initial deployment, Topology Builder gives you the option to include conferencing in your topology.</span></span> <span data-ttu-id="76c06-144">また、トポロジ ビルダーを使用して、既存の展開に会議を追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="76c06-144">You can also use Topology Builder to add conferencing to an existing deployment.</span></span> <span data-ttu-id="76c06-145">詳細については、「 [Lync Server 2013 でトポロジを定義して構成する](lync-server-2013-defining-and-configuring-the-topology.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="76c06-145">For details, see [Defining and configuring the topology in Lync Server 2013](lync-server-2013-defining-and-configuring-the-topology.md).</span></span>

<div>

## <a name="dial-in-conferencing-toplogies"></a><span data-ttu-id="76c06-146">会議 Toplogies でダイヤルする</span><span class="sxs-lookup"><span data-stu-id="76c06-146">Dial in Conferencing Toplogies</span></span>

<span data-ttu-id="76c06-147">ダイヤルイン会議は、次のトポロジと構成で展開できます。</span><span class="sxs-lookup"><span data-stu-id="76c06-147">You can deploy dial-in conferencing in the following topologies and configurations:</span></span>

  - <span data-ttu-id="76c06-148">Lync Server 2013 Standard Edition</span><span class="sxs-lookup"><span data-stu-id="76c06-148">Lync Server 2013 Standard Edition</span></span>

  - <span data-ttu-id="76c06-149">Lync Server 2013 Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="76c06-149">Lync Server 2013 Enterprise Edition</span></span>

  - <span data-ttu-id="76c06-150">エンタープライズ VoIP の有無は問いません</span><span class="sxs-lookup"><span data-stu-id="76c06-150">With or without Enterprise Voice</span></span>

<span data-ttu-id="76c06-151">アプリケーションサービス、会議アテンダントアプリケーション、会議のお知らせアプリケーションはセントラルサイトに展開できますが、ブランチサイトでは展開できません。</span><span class="sxs-lookup"><span data-stu-id="76c06-151">You can deploy Application service, Conferencing Attendant application, and Conferencing Announcement application in a central site, but not in a branch site.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="76c06-152">ダイヤルイン会議を展開する場合は、Lync Server 2013 会議を展開するすべてのプールに展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="76c06-152">If you deploy dial-in conferencing, you must deploy it in every pool where you deploy Lync Server 2013 conferencing.</span></span> <span data-ttu-id="76c06-153">プールごとにアクセス番号を割り当てる必要はありませんが、プールごとにダイヤルイン会議機能を展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="76c06-153">You do not need to assign access numbers in every pool, but you must deploy the dial-in conferencing feature in every pool.</span></span> <span data-ttu-id="76c06-154">この要件では、ユーザーが1つのプールのアクセス番号を呼び出して Lync Server 2013 会議に別のプールで参加した場合に、記録された名前の機能がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="76c06-154">This requirement supports the recorded name feature when a user calls an access number from one pool to join a Lync Server 2013 conference in a different pool.</span></span>



</div>

</div>

<div>

## <a name="supported-topologies-for-lync-server-2013-and-office-web-apps"></a><span data-ttu-id="76c06-155">Lync Server 2013 および Office Web Apps でサポートされているトポロジ</span><span class="sxs-lookup"><span data-stu-id="76c06-155">Supported Topologies for Lync Server 2013 and Office Web Apps</span></span>

<span data-ttu-id="76c06-156">Lync Server 2013 では、次の方法で Office Web Apps サーバーを構成できます。</span><span class="sxs-lookup"><span data-stu-id="76c06-156">Lync Server 2013 provides the following ways to configure Office Web Apps Server.</span></span> <span data-ttu-id="76c06-157">必要に応じて次のことができます。</span><span class="sxs-lookup"><span data-stu-id="76c06-157">Depending on your needs you can:</span></span>

  - <span data-ttu-id="76c06-158">**Lync Server 2013 と Office Web Apps サーバーの両方をオンプレミスの組織のファイアウォールと同じネットワークゾーンにインストールします。**</span><span class="sxs-lookup"><span data-stu-id="76c06-158">**Install both Lync Server 2013 and Office Web Apps Server on-premises behind your organization’s firewall, and in the same network zone.**</span></span> <span data-ttu-id="76c06-159">このトポロジでは、Office Web Apps サーバーへの外部アクセスがリバースプロキシサーバーによって提供されます。</span><span class="sxs-lookup"><span data-stu-id="76c06-159">With this topology, external access to Office Web Apps Server will be provided through your reverse proxy server.</span></span> <span data-ttu-id="76c06-160">Lync Server 2013 と Office Web Apps サーバー (または Office Web Apps サーバーファーム) の両方がオンプレミスと組織のファイアウォールの背後にインストールされている。</span><span class="sxs-lookup"><span data-stu-id="76c06-160">Both Lync Server 2013 and Office Web Apps Server (or an Office Web Apps Server farm) are installed on-premises and behind your organization's firewall.</span></span> <span data-ttu-id="76c06-161">理想的には、Lync Server と同じネットワークゾーンに Office Web Apps サーバーをインストールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="76c06-161">Ideally, you should install Office Web Apps Server in the same network zone as Lync Server.</span></span>
    
    <span data-ttu-id="76c06-162">外部の Lync クライアントは、インターネットからの要求を受け取り、内部ネットワークに転送するサーバーであるリバースプロキシサーバーを使用して、Lync Server 2013 および Office Web Apps Server に接続できます。</span><span class="sxs-lookup"><span data-stu-id="76c06-162">External Lync clients can connect to Lync Server 2013 and to Office Web Apps Server by using a reverse proxy server, which is a server that takes requests from the Internet and forwards them to the internal network.</span></span> <span data-ttu-id="76c06-163">(内部クライアントは、Office Web Apps サーバーに直接接続できるため、リバースプロキシサーバーを使用する必要はありません)。このトポロジは、Lync Server 2013 のみで使用される専用の Office Web Apps サーバーファームを使用する場合に最適です。</span><span class="sxs-lookup"><span data-stu-id="76c06-163">(Internal clients do not need to use the reverse proxy server because they can connect to Office Web Apps Server directly.) This topology works best if you want to use a dedicated Office Web Apps Server farm that is only used by Lync Server 2013.</span></span>

  - <span data-ttu-id="76c06-164">**外部で展開された Office Web Apps サーバーを使用する**</span><span class="sxs-lookup"><span data-stu-id="76c06-164">**Using an externally deployed Office Web Apps Server**</span></span>
    
    <span data-ttu-id="76c06-165">このトポロジでは、Lync Server 2013 はオンプレミスで展開され、Lync Server ネットワークゾーンの外部に展開されている Office Web Apps サーバーを使用します。</span><span class="sxs-lookup"><span data-stu-id="76c06-165">In this topology, Lync Server 2013 is deployed on-premises, and uses an Office Web Apps Server that is deployed outside of Lync Server network zone.</span></span> <span data-ttu-id="76c06-166">この問題は、Office Web Apps サーバーが企業内の複数のアプリケーション間で共有されており、Lync Server が Office Web Apps サーバーの外部インターフェイスを使用する必要があるネットワークに展開されている場合に発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="76c06-166">This may happen when Office Web Apps Server is shared across multiple applications in the corporation and is deployed in a network requiring Lync Server to use the external interface of Office Web Apps Server and vice versa.</span></span>
    
    <span data-ttu-id="76c06-167">リバースプロキシサーバーをインストールする必要はありません。代わりに、Office Web Apps サーバーから Lync Server 2013 へのすべての要求は、Edge サーバー経由でルーティングされます。</span><span class="sxs-lookup"><span data-stu-id="76c06-167">You do not need to install a reverse proxy server; instead, all the requests from the Office Web Apps Server to Lync Server 2013 are routed through your Edge Server.</span></span> <span data-ttu-id="76c06-168">内部と外部の Lync クライアントの両方が、外部 URL を使用して Office Web Apps サーバーに接続されます。</span><span class="sxs-lookup"><span data-stu-id="76c06-168">Both your internal and your external Lync clients connect to Office Web Apps Server using the external URL.</span></span>
    
    <span data-ttu-id="76c06-169">Office Web Apps サーバーが内部ファイアウォールの外側に展開されている場合は、[Office Web Apps Server] が [トポロジビルダー] の **外部ネットワーク ([境界/インターネット]) に展開** されていることを選択します。</span><span class="sxs-lookup"><span data-stu-id="76c06-169">If the Office Web Apps Server is deployed outside your internal firewall, then select the option **Office Web Apps Server is deployed in an external network (that is, perimeter/Internet)** in Topology Builder.</span></span> <span data-ttu-id="76c06-170">詳細については [、「Office Web Apps Server および Lync server 2013 との統合の構成](lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="76c06-170">For more details see [Configuring integration with Office Web Apps Server and Lync Server 2013](lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md).</span></span>

<span data-ttu-id="76c06-171">選択するトポロジにかかわらず、ファイアウォールの正しいポートを開くことは重要です。</span><span class="sxs-lookup"><span data-stu-id="76c06-171">Regardless of the topology you select, it is critical that the correct firewall ports be opened.</span></span> <span data-ttu-id="76c06-172">DNS 名、IP アドレス、およびポートが、Office Web Apps サーバー、ロードバランサー、または Lync サーバー上のファイアウォールによってブロックされていないことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="76c06-172">You must make sure that DNS names, IP addresses, and ports are not blocked by firewalls on the Office Web Apps Server, the load balancer, or Lync Server.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="76c06-173">Office Web Apps サーバーへの外部アクセスを提供するもう1つの方法は、境界ネットワークにサーバーを展開することです。</span><span class="sxs-lookup"><span data-stu-id="76c06-173">Another option for providing external access to Office Web Apps Server is to deploy the server in the perimeter network.</span></span> <span data-ttu-id="76c06-174">Office Web Apps サーバーのセットアップでは、サーバーコンピューターが Active Directory ドメインのメンバーである必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="76c06-174">If you elect to do this, keep in mind that Office Web Apps Server setup requires the server computer to be a member of your Active Directory domain.</span></span> <span data-ttu-id="76c06-175">ネットワークポリシーで境界ネットワーク内のコンピューターが Active Directory ドメインメンバーになることを許可していない場合は、境界ネットワークに Office Web Apps サーバーをインストールしないことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="76c06-175">Unless your network policy allows computers in the perimeter network to be Active Directory domain members, it is recommended that you do not install Office Web Apps Server in the perimeter network.</span></span> <span data-ttu-id="76c06-176">代わりに、内部ネットワークに Office Web Apps サーバーをインストールし、リバースプロキシサーバー経由で外部ユーザーのアクセスを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="76c06-176">Instead, you should install Office Web Apps Server in the internal network and provide external user access through your reverse proxy server.</span></span>



<span data-ttu-id="76c06-177"></div>

</div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="76c06-177"></div>

</div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

