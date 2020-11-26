---
title: 'Lync Server 2013: 内部設置型ユニファイド メッセージングを統合するためのガイドライン'
description: 'Lync Server 2013: オンプレミスのユニファイドメッセージングを統合するためのガイドライン。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Guidelines for integrating on-premises Unified Messaging and Lync Server
ms:assetid: 829ac017-6907-40f9-be22-787a28eae0ac
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398656(v=OCS.15)
ms:contentKeyID: 48184681
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 814c927aa36199737712328d3b92c64a8e967a55
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427806"
---
# <a name="guidelines-for-integrating-on-premises-unified-messaging-and-lync-server-2013"></a><span data-ttu-id="ec5ec-103">内部設置型ユニファイド メッセージングおよび Lync Server 2013 を統合するためのガイドライン</span><span class="sxs-lookup"><span data-stu-id="ec5ec-103">Guidelines for integrating on-premises Unified Messaging and Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ec5ec-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ec5ec-104">

<span> </span></span></span>

<span data-ttu-id="ec5ec-105">_**最終更新日:** 2012-09-25_</span><span class="sxs-lookup"><span data-stu-id="ec5ec-105">_**Topic Last Modified:** 2012-09-25_</span></span>

<span data-ttu-id="ec5ec-106">エンタープライズ Voip を展開する際のガイドラインとベストプラクティスを次に示します。</span><span class="sxs-lookup"><span data-stu-id="ec5ec-106">The following are guidelines and best practices to consider when you deploy Enterprise Voice:</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="ec5ec-107">Exchange ユニファイドメッセージング (UM) は、UCMA 4 も使用している場合にのみ、IPv6 をサポートします。</span><span class="sxs-lookup"><span data-stu-id="ec5ec-107">Exchange Unified Messaging (UM) supports IPv6 only if you are also using UCMA 4.</span></span>



</div>

  - <span data-ttu-id="ec5ec-108">Lync Server 2013 Standard Edition サーバーまたはフロントエンドプールを展開します。</span><span class="sxs-lookup"><span data-stu-id="ec5ec-108">Deploy a Lync Server 2013 Standard Edition server or a Front End pool.</span></span> <span data-ttu-id="ec5ec-109">インストールの詳細については、「展開ドキュメントに [Lync Server 2013 を展開](lync-server-2013-deploying-lync-server.md) する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ec5ec-109">For details about installation, see [Deploying Lync Server 2013](lync-server-2013-deploying-lync-server.md) in the Deployment documentation.</span></span>

  - <span data-ttu-id="ec5ec-110">Exchange 管理者と協力して、どのタスクが実行されるかを確認して、円滑かつ確実に統合されるようにします。</span><span class="sxs-lookup"><span data-stu-id="ec5ec-110">Work with Exchange administrators to confirm which tasks each of you will perform to assure a smooth and successful integration.</span></span>

  - <span data-ttu-id="ec5ec-111">Exchange UM のユーザーを有効にする exchange の各ユニファイドメッセージング (UM) フォレストに Exchange メールボックスサーバーの役割を展開します。</span><span class="sxs-lookup"><span data-stu-id="ec5ec-111">Deploy the Exchange Mailbox server roles in each Exchange Unified Messaging (UM) forest where you want to enable users for Exchange UM.</span></span> <span data-ttu-id="ec5ec-112">Exchange server の役割のインストールの詳細については、Microsoft Exchange Server 2013 に関するドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ec5ec-112">For details about installing Exchange server roles, see the Microsoft Exchange Server 2013 documentation.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="ec5ec-113">Exchange ユニファイドメッセージング (UM) がインストールされている場合は、自己署名証明書を使用するように構成されています。</span><span class="sxs-lookup"><span data-stu-id="ec5ec-113">When Exchange Unified Messaging (UM) is installed, it is configured to use a self-signed certificate.</span></span><BR><span data-ttu-id="ec5ec-114">ただし、自己署名された証明書では、Lync Server 2013 と Exchange UM が相互に信頼することはできません。そのため、両方のサーバーが信頼する証明機関の証明書を個別に要求する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec5ec-114">The self-signed certificate, however, does not enable Lync Server 2013 and Exchange UM to trust each other, which is why it is necessary to request a separate certificate from a certification authority that both servers trust.</span></span>

    
    </div>

  - <span data-ttu-id="ec5ec-115">Lync Server 2013 および Exchange UM がさまざまなフォレストにインストールされている場合は、各 Exchange フォレストが Lync Server 2013 フォレストと Lync Server 2013 フォレストを信頼するように構成して、各 Exchange フォレストを信頼するようにします。</span><span class="sxs-lookup"><span data-stu-id="ec5ec-115">If Lync Server 2013 and Exchange UM are installed in different forests, configure each Exchange forest to trust the Lync Server 2013 forest and the Lync Server 2013 forest to trust each Exchange forest.</span></span> <span data-ttu-id="ec5ec-116">また、ユーザーの Exchange UM 設定を Lync Server 2013 フォレストのユーザーオブジェクトに対して設定します。通常は、スクリプトまたは Id ライフサイクルマネージャー (ILM) などのフォレスト間ツールを使用します。</span><span class="sxs-lookup"><span data-stu-id="ec5ec-116">Also, set the users’ Exchange UM settings on the user objects in the Lync Server 2013 forest, typically by using a script or a cross-forest tool, such as Identity Lifecycle Manager (ILM).</span></span>

  - <span data-ttu-id="ec5ec-117">必要に応じて、Exchange 管理コンソールをインストールしてユニファイドメッセージングサーバーを管理します。</span><span class="sxs-lookup"><span data-stu-id="ec5ec-117">If necessary, install the Exchange Management Console to manage your Unified Messaging servers.</span></span>

  - <span data-ttu-id="ec5ec-118">Outlook Voice Access および自動応答の有効な電話番号を取得します。</span><span class="sxs-lookup"><span data-stu-id="ec5ec-118">Obtain valid phone numbers for Outlook Voice Access and auto attendant.</span></span>

  - <span data-ttu-id="ec5ec-119">Microsoft Exchange Server 2010 Service Pack 1 (SP1) より前のバージョンの Exchange UM を使用している場合は、Exchange UM SIP URI ダイヤルプランとエンタープライズボイスダイヤルプランの名前を調整します。</span><span class="sxs-lookup"><span data-stu-id="ec5ec-119">If you are using a version of Exchange UM earlier than Microsoft Exchange Server 2010 Service Pack 1 (SP1), coordinate names for Exchange UM SIP URI dial plans and Enterprise Voice dial plans.</span></span>

<div>

## <a name="deploying-redundant-exchange-um-servers"></a><span data-ttu-id="ec5ec-120">冗長な Exchange UM サーバーの展開</span><span class="sxs-lookup"><span data-stu-id="ec5ec-120">Deploying Redundant Exchange UM Servers</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="ec5ec-121">組織に対して構成した各 Exchange UM SIP URI ダイヤルプランについて、Exchange UM サービスが実行されている最低2台のサーバーを展開することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ec5ec-121">We recommend that you deploy a minimum of two servers on which Exchange UM services is running for each Exchange UM SIP URI dial plan that you configure for your organization.</span></span> <span data-ttu-id="ec5ec-122">拡張された容量の提供に加えて、冗長サーバーの展開によって可用性が高まります。</span><span class="sxs-lookup"><span data-stu-id="ec5ec-122">In addition to providing expanded capacity, deploying redundant servers provides high availability.</span></span> <span data-ttu-id="ec5ec-123">サーバーに障害が発生した場合、Lync Server 2013 を別のサーバーにフェールオーバーするように構成できます。</span><span class="sxs-lookup"><span data-stu-id="ec5ec-123">In the event of an server failure, Lync Server 2013 can be configured to fail over to another server.</span></span>



</div>

<span data-ttu-id="ec5ec-124">次に示す構成の例では、Exchange UM の回復性が提供されています。</span><span class="sxs-lookup"><span data-stu-id="ec5ec-124">The following example configurations provide Exchange UM resiliency.</span></span>

<span data-ttu-id="ec5ec-125">**例 1: Exchange UM の回復性**</span><span class="sxs-lookup"><span data-stu-id="ec5ec-125">**Example 1: Exchange UM Resiliency**</span></span>

<span data-ttu-id="ec5ec-126">![Exchange UM の例 1](images/Gg398656.3644b847-0847-4550-a989-e3fc51de5c4b(OCS.15).jpg "Exchange UM の例 1")</span><span class="sxs-lookup"><span data-stu-id="ec5ec-126">![Exchange UM Example 1](images/Gg398656.3644b847-0847-4550-a989-e3fc51de5c4b(OCS.15).jpg "Exchange UM Example 1")</span></span>

<span data-ttu-id="ec5ec-127">例1では、Exchange UM サーバー1と2が、データセンターで有効になっています。また、Exchange UM サーバー3と4は、ダブリンデータセンターで有効になっています。</span><span class="sxs-lookup"><span data-stu-id="ec5ec-127">In Example 1, Exchange UM servers 1 and 2 are enabled in the Tukwila data center, and Exchange UM servers 3 and 4 are enabled in the Dublin data center.</span></span> <span data-ttu-id="ec5ec-128">Tua で Exchange UM が停止した場合、サーバー1と2のドメインネームシステム (DNS) A レコードは、それぞれサーバー3と4をポイントするように構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec5ec-128">In the event of an Exchange UM outage in Tukwila, the Domain Name System (DNS) A records for servers 1 and 2 should be configured to point to servers 3 and 4, respectively.</span></span> <span data-ttu-id="ec5ec-129">Dublin で Exchange UM が停止した場合は、サーバー3および4の DNS A レコードをそれぞれサーバー1と2にポイントするように構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec5ec-129">In the event of an Exchange UM outage in Dublin, the DNS A records for servers 3 and 4 should be configured to point to servers 1 and 2, respectively.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="ec5ec-130">たとえば、1つの Exchange UM サーバーに次のいずれかの証明書を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec5ec-130">For Example 1, you should also assign one of following certificate on each Exchange UM server:</span></span> 
> <UL>
> <LI>
> <P><span data-ttu-id="ec5ec-131">サブジェクトの別名 (SAN) でワイルドカード付きの証明書を使用します。</span><span class="sxs-lookup"><span data-stu-id="ec5ec-131">Use a certificate with a wildcard in the Subject Alternative Name (SAN).</span></span></P>
> <LI>
> <P><span data-ttu-id="ec5ec-132">SAN の4つの Exchange UM サーバーのそれぞれについて、完全修飾ドメイン名 (FQDN) を入力します。</span><span class="sxs-lookup"><span data-stu-id="ec5ec-132">Put the fully qualified domain name (FQDN) of each of the four Exchange UM servers in the SAN.</span></span></P></LI></UL>



</div>

<span data-ttu-id="ec5ec-133">**例 2: Exchange UM の回復性**</span><span class="sxs-lookup"><span data-stu-id="ec5ec-133">**Example 2: Exchange UM Resiliency**</span></span>

<span data-ttu-id="ec5ec-134">![Exchange UM の例 2](images/Gg398656.15754273-306e-448d-b258-84bc2936a2e8(OCS.15).jpg "Exchange UM の例 2")</span><span class="sxs-lookup"><span data-stu-id="ec5ec-134">![Exchange UM Example 2](images/Gg398656.15754273-306e-448d-b258-84bc2936a2e8(OCS.15).jpg "Exchange UM Example 2")</span></span>

<span data-ttu-id="ec5ec-135">例2の [通常の運用条件] では、データセンターでの Exchange UM サーバー1と2が有効になっています。また、Exchange UM サーバー3と4は、ダブリンデータセンターで有効になっています。</span><span class="sxs-lookup"><span data-stu-id="ec5ec-135">In Example 2, under ordinary operating conditions Exchange UM servers 1 and 2 are enabled in the Tukwila data center, and Exchange UM servers 3 and 4 are enabled in the Dublin data center.</span></span> <span data-ttu-id="ec5ec-136">この4つのサーバーはすべて、ユーザーの SIP URI ダイヤルプランに含まれています。ただし、サーバー3と4は無効です。</span><span class="sxs-lookup"><span data-stu-id="ec5ec-136">All four servers are included in the Tukwila users' SIP URI dial plan; however, servers 3 and 4 are disabled.</span></span> <span data-ttu-id="ec5ec-137">Tukwila Exchange UM が停止した場合は、Exchange um サーバー1と2を無効にして、exchange UM サーバー3と4を有効にする必要があります。これにより、exchange um トラフィックが Dublin のサーバーにルーティングされるようになります。</span><span class="sxs-lookup"><span data-stu-id="ec5ec-137">In the event of an Exchange UM outage in Tukwila, for example, Exchange UM servers 1 and 2 should be disabled and Exchange UM servers 3 and 4 should be enabled so the Tukwila Exchange UM traffic will be routed to the servers in Dublin.</span></span>

<span data-ttu-id="ec5ec-138">Exchange 2013 でユニファイドメッセージングを有効または無効にする方法について詳しくは、「Exchange 2013 UM と Lync Server の統合」をご覧ください [https://go.microsoft.com/fwlink/p/?LinkId=265372](https://go.microsoft.com/fwlink/p/?linkid=265372) 。</span><span class="sxs-lookup"><span data-stu-id="ec5ec-138">For details about how to enable or disable Unified Messaging on Exchange 2013, see “Integrate Exchange 2013 UM with Lync Server” at [https://go.microsoft.com/fwlink/p/?LinkId=265372](https://go.microsoft.com/fwlink/p/?linkid=265372).</span></span>

<span data-ttu-id="ec5ec-139">Microsoft Exchange Server 2010 でユニファイドメッセージングを有効または無効にする方法の詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ec5ec-139">For details about how to enable or disable Unified Messaging on Microsoft Exchange Server 2010, see:</span></span>

  - <span data-ttu-id="ec5ec-140">「Exchange 2010 でユニファイドメッセージングを有効にする」をご覧 [https://go.microsoft.com/fwlink/p/?LinkId=204418](https://go.microsoft.com/fwlink/p/?linkid=204418) ください。</span><span class="sxs-lookup"><span data-stu-id="ec5ec-140">"Enable Unified Messaging on Exchange 2010" at [https://go.microsoft.com/fwlink/p/?LinkId=204418](https://go.microsoft.com/fwlink/p/?linkid=204418).</span></span>

  - <span data-ttu-id="ec5ec-141">"Exchange 2010 でユニファイドメッセージングを無効にする" をオンに [https://go.microsoft.com/fwlink/p/?LinkId=204416](https://go.microsoft.com/fwlink/p/?linkid=204416) します。</span><span class="sxs-lookup"><span data-stu-id="ec5ec-141">"Disable Unified Messaging on Exchange 2010" at [https://go.microsoft.com/fwlink/p/?LinkId=204416](https://go.microsoft.com/fwlink/p/?linkid=204416).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ec5ec-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="ec5ec-142">See Also</span></span>


[<span data-ttu-id="ec5ec-143">内部設置型ユニファイド メッセージングと Lync Server 2013 を統合するための展開プロセス</span><span class="sxs-lookup"><span data-stu-id="ec5ec-143">Deployment process for integrating on-premises Unified Messaging and Lync Server 2013</span></span>](lync-server-2013-deployment-process-for-integrating-on-premises-unified-messaging.md)  
  

<span data-ttu-id="ec5ec-144"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ec5ec-144"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

