---
title: リモート通話コントロールを有効にする
description: リモート通話コントロールを有効にします。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Enable remote call control
ms:assetid: 0b91d418-e6ed-4556-97af-e8523e01f249
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204664(v=OCS.15)
ms:contentKeyID: 48183380
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8009ffc927ad3f7a4f83ad3505100f3a9d4e82d6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398781"
---
# <a name="enable-remote-call-control"></a><span data-ttu-id="52025-103">リモート通話コントロールを有効にする</span><span class="sxs-lookup"><span data-stu-id="52025-103">Enable remote call control</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="52025-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="52025-104">

<span> </span></span></span>

<span data-ttu-id="52025-105">_**最終更新日:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="52025-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="52025-106">リモート通話コントロールを使用すると、ユーザーは Lync Server 2013 を使用して、デスクトップのプライベートブランチ exchange (PBX) 電話を制御できます。</span><span class="sxs-lookup"><span data-stu-id="52025-106">Remote call control enables users to control their desktop private branch exchange (PBX) phones by using Lync Server 2013.</span></span> <span data-ttu-id="52025-107">従来の環境でリモート通話コントロールを展開して、Lync Server 2013 を移行する必要がある場合は、次のタスクを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="52025-107">If you deployed remote call control in your legacy environment and want to migrate it Lync Server 2013, you need to perform the following tasks:</span></span>

1.  <span data-ttu-id="52025-108">SIP/CSTA ゲートウェイをインストールして、PBX と通信できるように設定します。</span><span class="sxs-lookup"><span data-stu-id="52025-108">Install a SIP/CSTA gateway and configure it to communicate with your PBX.</span></span> <span data-ttu-id="52025-109">Lync Server 2013 パイロットプールを展開する場合は、この手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="52025-109">You need to do this step when you deploy your Lync Server 2013 pilot pool.</span></span>

2.  <span data-ttu-id="52025-110">トポロジを結合してポリシーと設定を移行した後で、Lync Server 2013 を構成して、CSTA 要求が SIP/CSTA ゲートウェイにルーティングされるようにします。</span><span class="sxs-lookup"><span data-stu-id="52025-110">After you merge your topology and migrate your policies and settings, configure Lync Server 2013 to route CSTA requests to the SIP/CSTA gateway.</span></span> <span data-ttu-id="52025-111">この手順は、自動移行の後に続く手動の手順です。</span><span class="sxs-lookup"><span data-stu-id="52025-111">This step is a manual step that follows the automated migration.</span></span> <span data-ttu-id="52025-112">CSTA 要求のルーティングを構成するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="52025-112">To configure routing for CSTA requests, do the following:</span></span>
    
      - <span data-ttu-id="52025-113">従来の承認済みホストエントリを削除します (Lync Server 2013 では、 *信頼されたサーバーエントリ* と呼ばれます)。</span><span class="sxs-lookup"><span data-stu-id="52025-113">Remove legacy authorized host entries (known as *trusted server entries* in Lync Server 2013).</span></span> <span data-ttu-id="52025-114">従来の展開からユーザーを移行する場合は、Lync Server 2013 パイロットプールで新しい信頼されたアプリケーションのエントリを構成する前に、SIP/CSTA ゲートウェイ用に作成した既存の認証済みホストエントリをすべて削除してください。</span><span class="sxs-lookup"><span data-stu-id="52025-114">If you are migrating users from your legacy deployment, ensure that you remove all existing authorized host entries that you created for the SIP/CSTA gateway before you configure new trusted application entries on the Lync Server 2013 pilot pool.</span></span> <span data-ttu-id="52025-115">従来の承認済みホストのエントリを削除する方法について詳しくは、「承認され [たホストエントリを削除](remove-an-authorized-host-entry.md)する」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="52025-115">For details about how to remove legacy authorized host entries, see [Remove an authorized host entry](remove-an-authorized-host-entry.md).</span></span>
    
      - <span data-ttu-id="52025-116">リモート通話コントロールの静的ルートを構成します。</span><span class="sxs-lookup"><span data-stu-id="52025-116">Configure a static route for remote call control.</span></span> <span data-ttu-id="52025-117">リモート通話コントロールをサポートする個々のプールに対して静的ルートを構成できます。また、プールレベルの静的ルートで構成されていない各プールがグローバル静的ルートを使うように、グローバル静的ルートを構成することもできます。</span><span class="sxs-lookup"><span data-stu-id="52025-117">You can configure a static route for individual pools that you want to support remote call control, or you can configure a global static route so that each pool that is not configured with a pool-level static route uses the global static route.</span></span> <span data-ttu-id="52025-118">静的ルートを構成する方法の詳細については、展開ドキュメントの「 [Lync Server 2013 でリモート通話コントロールの静的ルートを構成](lync-server-2013-configure-a-static-route-for-remote-call-control.md) する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="52025-118">For details about how to configure the static route, see [Configure a static route for remote call control in Lync Server 2013](lync-server-2013-configure-a-static-route-for-remote-call-control.md) in the Deployment documentation.</span></span>
    
      - <span data-ttu-id="52025-119">リモート通話コントロールをサポートする各プールで、リモート通話コントロール用の信頼されたアプリケーションエントリを構成します。</span><span class="sxs-lookup"><span data-stu-id="52025-119">Configure a trusted application entry for remote call control on each pool for which you want to support remote call control.</span></span> <span data-ttu-id="52025-120">信頼されたアプリケーションのエントリを構成する方法の詳細については、展開ドキュメントの「 [Lync Server 2013 でのリモート通話コントロール用に信頼されているアプリケーションエントリを構成](lync-server-2013-configure-a-trusted-application-entry-for-remote-call-control.md) する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="52025-120">For details about how to configure a trusted application entry, see [Configure a trusted application entry for remote call control in Lync Server 2013](lync-server-2013-configure-a-trusted-application-entry-for-remote-call-control.md) in the Deployment documentation.</span></span>

3.  <span data-ttu-id="52025-121">伝送制御プロトコル (TCP) を使って Lync Server 2013 に接続している SIP/CSTA ゲートウェイを展開した場合は、トポロジビルダーでゲートウェイの IP アドレスを定義してください。</span><span class="sxs-lookup"><span data-stu-id="52025-121">If you deployed a SIP/CSTA gateway that uses Transmission Control Protocol (TCP) to connect to Lync Server 2013, define the IP address of the gateway in Topology Builder.</span></span> <span data-ttu-id="52025-122">IP アドレスの定義の詳細については、展開ドキュメントの「 [Lync Server 2013 で SIP/CSTA ゲートウェイの IP アドレスを定義する](lync-server-2013-define-a-sip-csta-gateway-ip-address.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="52025-122">For details about defining the IP address, see [Define a SIP/CSTA gateway IP address in Lync Server 2013](lync-server-2013-define-a-sip-csta-gateway-ip-address.md) in the Deployment documentation.</span></span>

4.  <span data-ttu-id="52025-123">リモートの通話コントロールを有効にし、line server の Uniform Resource Identifier (URI) と行の URI を割り当てることで、リモート通話コントロール用に Lync 2013 ユーザーを構成します。</span><span class="sxs-lookup"><span data-stu-id="52025-123">Configure Lync 2013 users for remote call control by enabling remote call control and assigning a line server Uniform Resource Identifier (URI) and a line URI.</span></span> <span data-ttu-id="52025-124">従来の展開から Lync Server 2013 にユーザーを移行すると、リモートの通話コントロールの設定が他のユーザーの設定とともに移行されます。</span><span class="sxs-lookup"><span data-stu-id="52025-124">When you migrate users from your legacy deployment to Lync Server 2013, the remote call control settings are migrated along with the other user settings.</span></span>

5.  <span data-ttu-id="52025-125">従来の展開で、アドレス帳の電話番号の正規化ルールをカスタマイズした場合、カスタマイズされた正規化ルールを移行するには、ポリシーの自動移行と設定が完了した後に、いくつかの手動タスクを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="52025-125">If you customized Address Book phone number normalization rules in your legacy deployment, you need to perform some manual tasks after the automated migration of policies and settings is complete to migrate the customized normalization rules.</span></span> <span data-ttu-id="52025-126">正規化ルールをカスタマイズしていない場合は、アドレス帳が他のトポロジと共に移行されます。</span><span class="sxs-lookup"><span data-stu-id="52025-126">If you did not customize normalization rules, Address Book is migrated along with the rest of your topology.</span></span> <span data-ttu-id="52025-127">カスタマイズされた正規化ルールを手動で移行する方法について詳しくは、「 [アドレス帳を移行](migrate-address-book.md)する」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="52025-127">For details about manually migrating customized normalization rules, see [Migrate Address Book](migrate-address-book.md).</span></span>

<span data-ttu-id="52025-128"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="52025-128"></div>

<span> </span>

</div>

</div>

</span></span></div>

