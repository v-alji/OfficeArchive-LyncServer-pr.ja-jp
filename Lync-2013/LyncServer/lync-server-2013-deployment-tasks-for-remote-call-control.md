---
title: 'Lync Server 2013: リモート通話コントロールの展開タスク'
description: 'Lync Server 2013: リモート呼び出しコントロールの展開タスク。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment tasks for remote call control
ms:assetid: 20218871-4f27-4611-9b7e-c0ca55908284
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558624(v=OCS.15)
ms:contentKeyID: 48183599
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 61d0d57489bd93d7e6ce0209c605f05a2417bded
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429609"
---
# <a name="deployment-tasks-for-remote-call-control-in-lync-server-2013"></a><span data-ttu-id="3f77e-103">Lync Server 2013 のリモート通話コントロールの展開タスク</span><span class="sxs-lookup"><span data-stu-id="3f77e-103">Deployment tasks for remote call control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3f77e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3f77e-104">

<span> </span></span></span>

<span data-ttu-id="3f77e-105">_**最終更新日:** 2012-10-05_</span><span class="sxs-lookup"><span data-stu-id="3f77e-105">_**Topic Last Modified:** 2012-10-05_</span></span>

<span data-ttu-id="3f77e-106">このトピックでは、Lync Server 環境のユーザーに対してリモート通話コントロールを有効にするために実行する必要がある展開タスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="3f77e-106">This topic describes the deployment tasks that you must perform to enable remote call control for users in your Lync Server environment.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3f77e-107">Microsoft Office Communicator 2007 R2 で、リモート通話コントロールに対して以前有効にしたユーザーを移行する場合は、このトピックで説明されているリモート通話コントロールの展開タスクを実行する前に、追加の展開タスクを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3f77e-107">If you are migrating users previously enabled for remote call control in Microsoft Office Communicator 2007 R2, you must perform an additional deployment task before you begin performing the remote call control deployment tasks described in this topic.</span></span> <span data-ttu-id="3f77e-108">Lync Server への移行プロセスでは、必要に応じて、Office Communications Server 2007 R2 管理ツールを使用して、信頼済みアプリケーションエントリ (以前は <EM>承認済みホストエントリ</EM>) を削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3f77e-108">During the migration process to Lync Server, trusted application entries (previously known as <EM>authorized host entries</EM>) must be removed by using the Office Communications Server 2007 R2 administrative tools, as appropriate.</span></span><BR><span data-ttu-id="3f77e-109">承認済みホストの削除の詳細については、「 <A href="lync-server-2013-remove-a-legacy-authorized-host-optional.md">Lync Server 2013 で従来の承認済みホストを削除する (オプション)</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3f77e-109">For details about removing authorized hosts, see <A href="lync-server-2013-remove-a-legacy-authorized-host-optional.md">Remove a legacy authorized host in Lync Server 2013 (optional)</A>.</span></span>



</div>

<div>

## <a name="step-1-install-and-configure-the-sipcsta-gateway-to-communicate-with-your-pbx"></a><span data-ttu-id="3f77e-110">手順 1: PBX と通信するために SIP/CSTA ゲートウェイをインストールして構成する</span><span class="sxs-lookup"><span data-stu-id="3f77e-110">Step 1: Install and Configure the SIP/CSTA Gateway to Communicate with Your PBX</span></span>

<span data-ttu-id="3f77e-111">ユーザーにリモート通話コントロール機能を提供するには、環境内の Lync Server と既存の構内交換機 (PBX) の両方に接続できる SIP/CSTA ゲートウェイを少なくとも1つインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3f77e-111">You need to install at least one SIP/CSTA gateway that can connect to both Lync Server and the existing private branch exchange (PBX) in your environment in order to provide remote call control features to your users.</span></span> <span data-ttu-id="3f77e-112">SIP/CSTA ゲートウェイは、SIP とコンピュータでサポートされている通信アプリケーション (CSTA) の間のゲートウェイです。</span><span class="sxs-lookup"><span data-stu-id="3f77e-112">A SIP/CSTA gateway is a gateway between SIP and a computer-supported telecommunications application (CSTA).</span></span> <span data-ttu-id="3f77e-113">複数のゲートウェイをインストールする場合でも、1つだけの場合でも、各ユーザーを1つのゲートウェイまたは PBX で構成できます。</span><span class="sxs-lookup"><span data-stu-id="3f77e-113">Whether you install multiple gateways or just one, each user can be configured with only one gateway or PBX.</span></span> <span data-ttu-id="3f77e-114">既存の PBX に SIP/CSTA のインタフェースがない場合は、pbx をサポートできる SIP/CSTA ゲートウェイ (pbx ベンダー固有のシグナリングプロトコルのサポートを含む) を展開してください。</span><span class="sxs-lookup"><span data-stu-id="3f77e-114">If your existing PBX does not have a SIP/CSTA interface, ensure you deploy a SIP/CSTA gateway that can support the PBX, including support for proprietary PBX vendor-specific signaling protocols.</span></span> <span data-ttu-id="3f77e-115">機能の詳細については、各ベンダーに直接お問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="3f77e-115">For details about capabilities, consult each vendor directly.</span></span>

<span data-ttu-id="3f77e-116">リモート通話コントロール用に Lync Server と統合できる SIP/CSTA ゲートウェイを展開する準備ができたら、ゲートウェイベンダーに問い合わせるか、ゲートウェイで必要な以下の情報については、ベンダーのゲートウェイドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3f77e-116">When you are ready to deploy a SIP/CSTA gateway that can integrate with Lync Server for remote call control, also consult with your gateway vendor or the vendor’s gateway documentation regarding the syntax required by the gateway for the following information:</span></span>

  - <span data-ttu-id="3f77e-117">ゲートウェイのラインサーバーの URI</span><span class="sxs-lookup"><span data-stu-id="3f77e-117">Line server URI of the gateway</span></span>

  - <span data-ttu-id="3f77e-118">ゲートウェイに割り当てるユーザーの行の URI</span><span class="sxs-lookup"><span data-stu-id="3f77e-118">Line URI for users that will be assigned to the gateway</span></span>

<span data-ttu-id="3f77e-119">上記の設定は、ユーザーの構成時に必須であり、PBX のルーティングと接続が適切に行われるように、ゲートウェイで指定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="3f77e-119">The preceding settings are required during user configuration and must be specified as expected by the gateway to route and connect to the PBX properly.</span></span>

<span data-ttu-id="3f77e-120">Microsoft ユニファイドコミュニケーションのオープンな相互運用性プログラム web サイトでベンダーを参照するには、を参照 [https://go.microsoft.com/fwlink/p/?linkId=203309](https://go.microsoft.com/fwlink/p/?linkid=203309) してください。</span><span class="sxs-lookup"><span data-stu-id="3f77e-120">You can refer to vendors on the Microsoft Unified Communications Open Interoperability Program website at [https://go.microsoft.com/fwlink/p/?linkId=203309](https://go.microsoft.com/fwlink/p/?linkid=203309).</span></span>

</div>

<div>

## <a name="step-2-configure-lync-server-to-route-csta-requests-to-the-sipcsta-gateway"></a><span data-ttu-id="3f77e-121">手順 2: CSTA 要求を SIP/CSTA ゲートウェイにルーティングするように Lync Server を構成する</span><span class="sxs-lookup"><span data-stu-id="3f77e-121">Step 2: Configure Lync Server to Route CSTA Requests to the SIP/CSTA Gateway</span></span>

<span data-ttu-id="3f77e-122">リモート通話制御要求をルーティングする対象となる、展開内のすべての SIP/CSTA ゲートウェイの宛先アドレス (サーバー URI) に、Lync サーバープールで静的ルートを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3f77e-122">You must create static routes on Lync Server pools to the destination address (server URI) of all SIP/CSTA gateways in your deployment to which you intend to route remote call control requests.</span></span> <span data-ttu-id="3f77e-123">また、各宛先アドレスに対応する信頼されたアプリケーションエントリも作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3f77e-123">You must also create a trusted application entry that corresponds to each destination address.</span></span> <span data-ttu-id="3f77e-124">ゲートウェイを信頼済みアプリケーションとして指定すると、サードパーティによって開発されている場合でも、Lync Server 環境の一部として実行される信頼された状態が与えられます (これは、製品の組み込みの一部ではないサービスであるため、 *外部サービス* と呼ばれます)。</span><span class="sxs-lookup"><span data-stu-id="3f77e-124">When you designate the gateway as a trusted application, it is given trusted status to run as part of the Lync Server environment even though it is developed by a third party (and runs what is referred to as an *external service* because it is a service that is not a built-in part of the product).</span></span> <span data-ttu-id="3f77e-125">最後に、Lync Server がトランスポート層セキュリティ (TLS) 接続ではなく、伝送制御プロトコル (TCP) 接続を使用して SIP/CSTA ゲートウェイに接続している場合は、トポロジビルダーを使用してゲートウェイの IP アドレスを定義する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="3f77e-125">Finally, if Lync Server will connect to the SIP/CSTA gateway using a Transmission Control Protocol (TCP) connection instead of a Transport Layer Security (TLS) connection, you must also define the gateway IP address by using Topology Builder.</span></span>

<span data-ttu-id="3f77e-126">静的ルートの構成の詳細については、「 [Lync Server 2013 でリモート通話コントロールの静的ルートを構成](lync-server-2013-configure-a-static-route-for-remote-call-control.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3f77e-126">For details about configuring static routes, see [Configure a static route for remote call control in Lync Server 2013](lync-server-2013-configure-a-static-route-for-remote-call-control.md).</span></span>

<span data-ttu-id="3f77e-127">信頼されたアプリケーションエントリの構成の詳細については、「 [Lync Server 2013 で、「リモート通話コントロール用の信頼されたアプリケーションエントリを構成](lync-server-2013-configure-a-trusted-application-entry-for-remote-call-control.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3f77e-127">For details about configuring trusted application entries, see [Configure a trusted application entry for remote call control in Lync Server 2013](lync-server-2013-configure-a-trusted-application-entry-for-remote-call-control.md).</span></span>

<span data-ttu-id="3f77e-128">Topology Builder での SIP/CSTA ゲートウェイ IP アドレスの定義の詳細については、「 [Lync Server 2013 で sip/csta ゲートウェイの ip アドレスを定義する](lync-server-2013-define-a-sip-csta-gateway-ip-address.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3f77e-128">For details about defining a SIP/CSTA gateway IP address in Topology Builder, see [Define a SIP/CSTA gateway IP address in Lync Server 2013](lync-server-2013-define-a-sip-csta-gateway-ip-address.md).</span></span>

</div>

<div>

## <a name="step-3-configure-lync-users-for-remote-call-control"></a><span data-ttu-id="3f77e-129">手順 3: リモート通話コントロール用に Lync ユーザーを構成する</span><span class="sxs-lookup"><span data-stu-id="3f77e-129">Step 3: Configure Lync Users for Remote Call Control</span></span>

<span data-ttu-id="3f77e-130">Lync server のユーザーを有効にした後、Lync Server コントロールパネルまたは Lync Server 管理シェルを使用して、リモートでの通話の制御を有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="3f77e-130">After users have been enabled for Lync Server, you can use Lync Server Control Panel or Lync Server Management Shell to enable them for remote call control.</span></span> <span data-ttu-id="3f77e-131">この展開手順では、各ユーザーに行サーバーの URI と行の URI を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="3f77e-131">It is during this deployment step that you assign each user a line server URI and a line URI.</span></span> <span data-ttu-id="3f77e-132">Line server URI は、ユーザーに割り当てようとして計画している SIP/CSTA ゲートウェイの SIP URI です。</span><span class="sxs-lookup"><span data-stu-id="3f77e-132">The line server URI is the SIP URI of the SIP/CSTA gateway that you plan to assign to the user.</span></span> <span data-ttu-id="3f77e-133">ライン URI は、ユーザーに割り当てられている一意の電話番号です。</span><span class="sxs-lookup"><span data-stu-id="3f77e-133">The line URI is the unique phone number assigned to the user.</span></span>

<span data-ttu-id="3f77e-134">リモート通話コントロール用にユーザーを構成する方法について詳しくは、「 [Lync Server 2013 のリモート通話コントロールで lync ユーザーを有効にする](lync-server-2013-enable-lync-users-for-remote-call-control.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="3f77e-134">For details about configuring users for remote call control, see [Enable Lync users for remote call control in Lync Server 2013](lync-server-2013-enable-lync-users-for-remote-call-control.md).</span></span>

</div>

<div>

## <a name="step-4-define-the-lync-server-phone-number-normalization-rules"></a><span data-ttu-id="3f77e-135">手順 4: Lync Server 電話番号の正規化ルールを定義する</span><span class="sxs-lookup"><span data-stu-id="3f77e-135">Step 4: Define the Lync Server Phone Number Normalization Rules</span></span>

<span data-ttu-id="3f77e-136">リモート通話コントロールのシナリオでは、Lync Server は電話番号の正規化ルールを使用して、SIP/CGI ゲートウェイから取得した電話番号を E.i 形式に変換します。</span><span class="sxs-lookup"><span data-stu-id="3f77e-136">In remote call control scenarios, Lync Server uses phone number normalization rules to convert phone numbers it receives from the SIP/CSTA gateway to E.164 format.</span></span> <span data-ttu-id="3f77e-137">特定のリモート通話コントロール機能が正しく動作するためには、この標準化された形式で電話番号を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3f77e-137">Phone numbers must be in this standardized format for certain remote call control features to function properly.</span></span> <span data-ttu-id="3f77e-138">リモート通話コントロールは、アドレス帳サービス電話番号の正規化に対して構成したものと同じ電話番号の正規化ルールを使用します。これは、エンタープライズ Voip に使われる電話番号の正規化ルールとは異なります。</span><span class="sxs-lookup"><span data-stu-id="3f77e-138">Remote call control uses the same phone number normalization rules that you configure for Address Book Service phone number normalization, which are different from the phone number normalization rules used for Enterprise Voice.</span></span>

<span data-ttu-id="3f77e-139">リモート通話コントロールで電話番号の正規化ルールを使用する方法について詳しくは、「 [Lync Server 2013 でのリモート通話コントロールと電話番号の正規化](lync-server-2013-remote-call-control-and-phone-number-normalization.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="3f77e-139">For details about how remote call control uses phone number normalization rules, see [Remote call control and phone number normalization in Lync Server 2013](lync-server-2013-remote-call-control-and-phone-number-normalization.md).</span></span> <span data-ttu-id="3f77e-140">アドレス帳サービスの電話番号の正規化ルールの詳細については、操作のドキュメントで「 [Lync Server 2013 のアドレス帳サービスを管理](lync-server-2013-administering-the-address-book-service.md) する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3f77e-140">For details about phone number normalization rules for Address Book Service, see [Administering the Address Book Service in Lync Server 2013](lync-server-2013-administering-the-address-book-service.md) topic in the Operations documentation.</span></span>

<span data-ttu-id="3f77e-141"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3f77e-141"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

