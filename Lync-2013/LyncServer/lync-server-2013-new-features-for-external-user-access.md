---
title: 'Lync Server 2013: 外部ユーザー アクセスの新機能'
description: 'Lync Server 2013: 外部ユーザーアクセスの新機能。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New features for external user access
ms:assetid: 99da6bd5-ec14-4ad9-8f7d-37fbddf567dd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398794(v=OCS.15)
ms:contentKeyID: 48184884
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d9d960a469334a836c453e8ae3bbf51f1b66bb93
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445401"
---
# <a name="new-features-for-external-user-access-in-lync-server-2013"></a><span data-ttu-id="6e3a5-103">Lync Server 2013 の外部ユーザー アクセスの新機能</span><span class="sxs-lookup"><span data-stu-id="6e3a5-103">New features for external user access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6e3a5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6e3a5-104">

<span> </span></span></span>

<span data-ttu-id="6e3a5-105">_**最終更新日:** 2012-10-17_</span><span class="sxs-lookup"><span data-stu-id="6e3a5-105">_**Topic Last Modified:** 2012-10-17_</span></span>

<span data-ttu-id="6e3a5-106">Lync Server 2013 には、ユーザーの機能と通信方法を拡張する新機能が導入されています。</span><span class="sxs-lookup"><span data-stu-id="6e3a5-106">Lync Server 2013 introduces new features that extend the features and communications methods for your users.</span></span> <span data-ttu-id="6e3a5-107">また、Lync Server 2013 では、組織で利用できるサービスをより適切に統合および拡張するために、既存のサービスへの変更が導入されています。</span><span class="sxs-lookup"><span data-stu-id="6e3a5-107">Also, Lync Server 2013 introduces changes to existing services to better integrate and extend the services that are available to your organization.</span></span> <span data-ttu-id="6e3a5-108">以下は、Lync Server 2013 Edge Server サービスの計画と展開に影響を与える可能性のある変更内容をまとめたものです。</span><span class="sxs-lookup"><span data-stu-id="6e3a5-108">Following is a summary of changes that may affect your planning and deployment of Lync Server 2013 Edge Server services.</span></span>

  - <span data-ttu-id="6e3a5-109">**IPv6 アドレス指定のサポート**   Lync Server 2013 は、すべての Edge Server サービスの IPv6 アドレス指定をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="6e3a5-109">**Support for IPv6 addressing**   Lync Server 2013 supports IPv6 addressing for all Edge Server services.</span></span> <span data-ttu-id="6e3a5-110">Windows Server の構成を通じてインターフェイスの IPv6 アドレスを指定している場合は、トポロジビルダーの IP アドレス構成を使用して、エッジサーバー構成の IPv6 アドレスを使うことができます。</span><span class="sxs-lookup"><span data-stu-id="6e3a5-110">If you have provided IPv6 addresses for the interfaces through configuration in Windows Server, you can use IPv6 addresses in your Edge Server configuration through the IP address configuration in Topology Builder.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="6e3a5-111">Lync Server 2013 での IPv6 アドレスの使用は、組織が展開するルーターやファイアウォールでの IPv6 のサポート、およびインターネットサービスプロバイダーによるサポートによって異なります。</span><span class="sxs-lookup"><span data-stu-id="6e3a5-111">Use of IPv6 addresses in Lync Server 2013 depends on support of IPv6 in routers and firewalls that your organization deploys, as well as support through your Internet service provider.</span></span>

    
    </div>

  - <span data-ttu-id="6e3a5-112">**拡張可能なメッセージングとプレゼンスプロトコル (XMPP)**   Lync Server 2013 は、完全に統合された XMPP プロキシ (エッジサーバーに展開) と、フロントエンドサーバーに XMPP ゲートウェイを展開したものです。</span><span class="sxs-lookup"><span data-stu-id="6e3a5-112">**Extensible Messaging and Presence Protocol (XMPP)**   Lync Server 2013 introduces a fully integrated XMPP proxy (deployed on the Edge Servers) and an XMPP gateway deployed on your Front End Servers.</span></span> <span data-ttu-id="6e3a5-113">XMPP フェデレーションは、オプションのコンポーネントとして展開できます。</span><span class="sxs-lookup"><span data-stu-id="6e3a5-113">You can deploy XMPP federation as an optional component.</span></span> <span data-ttu-id="6e3a5-114">XMPP プロキシと XMPP ゲートウェイを追加して構成することにより、Microsoft Lync 2013 ユーザーは、インスタントメッセージング (IM) とプレゼンスのために、XMPP ベースのパートナーから連絡先を追加できます。</span><span class="sxs-lookup"><span data-stu-id="6e3a5-114">Adding and configuring the XMPP proxy and XMPP gateway will allow your Microsoft Lync 2013 users to add contacts from XMPP-based partners for instant messaging (IM) and presence.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="6e3a5-115">現時点では、Lync Server 2013 の XMPP サービスは、Lync クライアントと XMPP ベースの連絡先の間でインスタントメッセージ (im) とプレゼンスを提供します。</span><span class="sxs-lookup"><span data-stu-id="6e3a5-115">Currently, the XMPP services in Lync Server 2013 only provide instant messaging and presence between Lync clients and XMPP-based contacts.</span></span>

    
    </div>

  - <span data-ttu-id="6e3a5-116">**モバイルクライアント用のモバイルサービス**   Lync Server 2010 のモバイルサービスで導入された lync Server 2013 のモバイルサービスでは、サポートされている Apple iOS、Android、Windows Phone、または Nokia モバイルデバイスを使用して、Microsoft Lync モバイルクライアントが、インスタントメッセージの送受信、連絡先の表示、プレゼンスの表示などの操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="6e3a5-116">**Mobility services for Mobile clients**   Introduced in a customer update for Lync Server 2010, Mobility services in Lync Server 2013 allow Microsoft Lync Mobile clients on mobile phones and tablet devices using supported Apple iOS, Android, Windows Phone, or Nokia mobile devices to perform such activities as sending and receiving instant messages, viewing contacts, and viewing presence.</span></span> <span data-ttu-id="6e3a5-117">さらに、モバイルデバイスでは、クリックして会議に参加したり、勤務先の電話、1回の通話、ボイスメール、不在着信通知など、一部のエンタープライズ音声機能をサポートしたりします。</span><span class="sxs-lookup"><span data-stu-id="6e3a5-117">In addition, mobile devices support some Enterprise Voice features, such as click to join a conference, Call via Work, single number reach, voice mail, and missed call notification.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="6e3a5-118">モビリティサービスは、フロントエンドサーバーに展開されているリバースプロキシと公開されたサービスを使用します。</span><span class="sxs-lookup"><span data-stu-id="6e3a5-118">The mobility services use the reverse proxy and published services that are deployed on your Front End Servers.</span></span> <span data-ttu-id="6e3a5-119">エッジサーバーへの変更は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="6e3a5-119">No changes are required to Edge Servers.</span></span>

    
    </div>

  - <span data-ttu-id="6e3a5-120">**ディレクターはオプションの役割**   Lync Server 2013 トポロジでのディレクターサーバーの役割が変更されていません。</span><span class="sxs-lookup"><span data-stu-id="6e3a5-120">**Directors are an optional role**   The role of the Director server in the Lync Server 2013 topology has not changed.</span></span> <span data-ttu-id="6e3a5-121">さらに、web サービスのホスト、着信ユーザー要求の事前認証、外部ユーザーのホームプールへの送信を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="6e3a5-121">It still hosts web services, pre-authenticates incoming user requests, and directs external users to their home pool.</span></span> <span data-ttu-id="6e3a5-122">推奨された役割からのディレクターをオプションの役割に変更しても、ディレクターの値を減らすことはできませんが、機能が損なわれることなく、サーバー数やその他のハードウェア要件 (ディレクターのハードウェアロードバランサーなど) が必要になります。</span><span class="sxs-lookup"><span data-stu-id="6e3a5-122">Changing the Director from a recommended role to an optional role does not diminish the value of the Director, but emphasizes reducing server count and other hardware requirements (for example, hardware load balancers for the Director) requirements without compromising features and functionality.</span></span> <span data-ttu-id="6e3a5-123">フロントエンドサーバーは、提供されたサービスに影響を与えずにディレクターと同じジョブを行うことができるため、必要に応じて、[ディレクター] を展開することもできます。</span><span class="sxs-lookup"><span data-stu-id="6e3a5-123">Because the Front End Servers can do the same job as the Director with no impact to services provided, you can optionally deploy Directors if you choose to.</span></span> <span data-ttu-id="6e3a5-124">フロントエンドサーバーによって同じサービスが提供されるという確信を持って、ディレクターを安全に除外することができます。</span><span class="sxs-lookup"><span data-stu-id="6e3a5-124">You can safely exclude the Director with confidence that the Front End Servers will provide the same services in their place.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="6e3a5-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="6e3a5-125">See Also</span></span>


[<span data-ttu-id="6e3a5-126">Lync Server 2013 での IPv6 の計画と構成</span><span class="sxs-lookup"><span data-stu-id="6e3a5-126">Planning for and configuring IPv6 in Lync Server 2013</span></span>](lync-server-2013-planning-for-and-configuring-ipv6.md)  


[<span data-ttu-id="6e3a5-127">Lync Server 2013 の外部ユーザー アクセスの計画</span><span class="sxs-lookup"><span data-stu-id="6e3a5-127">Planning for external user access in Lync Server 2013</span></span>](lync-server-2013-planning-for-external-user-access.md)  
[<span data-ttu-id="6e3a5-128">Lync Server 2013 での拡張メッセージングとプレゼンスプロトコル (XMPP) フェデレーションの計画</span><span class="sxs-lookup"><span data-stu-id="6e3a5-128">Planning for extensible messaging and presence protocol (XMPP) federation in Lync Server 2013</span></span>](lync-server-2013-planning-for-extensible-messaging-and-presence-protocol-xmpp-federation.md)  
  

<span data-ttu-id="6e3a5-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6e3a5-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

