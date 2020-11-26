---
title: 'Lync Server 2013: フロントエンド サーバー、インスタント メッセージング、およびプレゼンスに関する要件の定義'
description: 'Lync Server 2013: フロントエンドサーバー、インスタントメッセージング、プレゼンスの要件を定義します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Defining your requirements for Front End Servers, instant messaging, and presence
ms:assetid: c21198bc-520c-4d17-8b84-7ff1475b9b0a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412956(v=OCS.15)
ms:contentKeyID: 48185319
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 923132b32d5aef80191b19a7b85c3f17276e5946
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430813"
---
# <a name="defining-your-requirements-for-front-end-servers-instant-messaging-and-presence-in-lync-server-2013"></a><span data-ttu-id="8bf31-103">Lync Server 2013 でのフロントエンド サーバー、インスタント メッセージング、およびプレゼンスに関する要件の定義</span><span class="sxs-lookup"><span data-stu-id="8bf31-103">Defining your requirements for Front End Servers, instant messaging, and presence in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8bf31-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8bf31-104">

<span> </span></span></span>

<span data-ttu-id="8bf31-105">_**最終更新日:** 2013-10-07_</span><span class="sxs-lookup"><span data-stu-id="8bf31-105">_**Topic Last Modified:** 2013-10-07_</span></span>

<span data-ttu-id="8bf31-106">インスタントメッセージング (IM) とプレゼンスを計画する主なタスクは、ユーザーに対して十分なフロントエンドサーバーがあることを確認することです。</span><span class="sxs-lookup"><span data-stu-id="8bf31-106">The main task of planning for instant messaging (IM) and presence is ensuring that you have enough Front End Servers for your users.</span></span>

<div>

## <a name="enabling-communication-with-external-users"></a><span data-ttu-id="8bf31-107">外部ユーザーとの通信を有効にする</span><span class="sxs-lookup"><span data-stu-id="8bf31-107">Enabling Communication with External Users</span></span>

<span data-ttu-id="8bf31-108">ユーザーが外部ユーザーと通信できるようにすることで、Lync Server での投資の利点を大幅に高めることができます。</span><span class="sxs-lookup"><span data-stu-id="8bf31-108">You can greatly increase the benefits of your investment in Lync Server by enabling your users to communicate with external users.</span></span> <span data-ttu-id="8bf31-109">外部ユーザーには次のユーザーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="8bf31-109">External users can include:</span></span>

  - <span data-ttu-id="8bf31-110">**リモートユーザー**   ファイアウォール外で作業していて、ノート pc やその他の Lync Server デバイスを使用している場合に、組織の独自のユーザー。</span><span class="sxs-lookup"><span data-stu-id="8bf31-110">**Remote users**   Your organization’s own users, when they are working outside your firewalls and are using their laptops or other Lync Server devices.</span></span>

  - <span data-ttu-id="8bf31-111">**フェデレーション**   されたユーザー  Lync Server も実行している会社のユーザー。</span><span class="sxs-lookup"><span data-stu-id="8bf31-111">**Federated users**   Users from companies you work with who also run Lync Server.</span></span> <span data-ttu-id="8bf31-112">自社ユーザーがこうしたユーザーに容易にコンタクトできるようにするには、これらの企業とフェデレーション関係を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8bf31-112">To enable your users to easily contact these users, you create federated relationships with these companies.</span></span>

  - <span data-ttu-id="8bf31-113">**パブリックユーザー**   インターネットサービス、Yahoo、AOL の Windows Live ネットワークによって提供される IM サービスなどのパブリック IM サービスのユーザー、 \! および拡張メッセージングとプレゼンスプロトコル (XMPP) を使用するプロバイダーとサーバーのユーザー (Google Talk など)。</span><span class="sxs-lookup"><span data-stu-id="8bf31-113">**Public users**   Users of public IM services, such as IM services provided by the Windows Live network of Internet services, Yahoo\!, and AOL, and users of providers and servers that use Extensible Messaging and Presence Protocol (XMPP), such as Google Talk.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="8bf31-114">Windows Live、AOL、Yahoo! のパブリック IM 接続には個別のライセンスが必要になる場合があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="8bf31-114">Note that a separate license might be required for public IM connectivity with Windows Live, AOL, and Yahoo!</span></span>

    
    </div>
    
    <div>
    

    > [!IMPORTANT]  
    > <UL>
    > <LI>
    > <P><span data-ttu-id="8bf31-115">2012年9月1日以降、Microsoft Lync パブリック IM 接続ユーザーサブスクリプションライセンス ("PIC USL") は、新規または更新契約の購入に使用できなくなりました。</span><span class="sxs-lookup"><span data-stu-id="8bf31-115">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) is no longer available for purchase for new or renewing agreements.</span></span> <span data-ttu-id="8bf31-116">アクティブなライセンスを持っているお客様は、Yahoo! とのフェデレーションを継続できます。</span><span class="sxs-lookup"><span data-stu-id="8bf31-116">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="8bf31-117">サービスが終了するまでの Messenger。</span><span class="sxs-lookup"><span data-stu-id="8bf31-117">Messenger until the service shut down date.</span></span> <span data-ttu-id="8bf31-118">AOL および Yahoo! の2014年6月の終了日</span><span class="sxs-lookup"><span data-stu-id="8bf31-118">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="8bf31-119">が発表されました。</span><span class="sxs-lookup"><span data-stu-id="8bf31-119">has been announced.</span></span> <span data-ttu-id="8bf31-120">詳細については、「 <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Lync Server 2013 でのパブリックインスタントメッセンジャー接続のサポート</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8bf31-120">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="8bf31-121">PIC USL は、Lync Server または Office Communications Server が Yahoo! とのフェデレーションを行うために必要な1か月あたりのユーザーごとのサブスクリプションライセンスです。</span><span class="sxs-lookup"><span data-stu-id="8bf31-121">The PIC USL is a per-user per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="8bf31-122">Messenger.</span><span class="sxs-lookup"><span data-stu-id="8bf31-122">Messenger.</span></span> <span data-ttu-id="8bf31-123">このサービスを提供するための Microsoft の機能は、Yahoo! からのサポートによって決定されたものであり、その基となる契約は "巻停止" となります。</span><span class="sxs-lookup"><span data-stu-id="8bf31-123">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which is winding down.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="8bf31-124">Lync は、組織間、および世界各地の個人と接続するための強力なツールです。</span><span class="sxs-lookup"><span data-stu-id="8bf31-124">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="8bf31-125">Windows Live Messenger とのフェデレーションには、Lync 標準 CAL 以外の追加のユーザー/デバイスライセンスは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="8bf31-125">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="8bf31-126">Skype federation はこのリストに追加されます。 Lync ユーザーは、IM と音声を使用して、数百人の何百万ものユーザーに連絡できます。</span><span class="sxs-lookup"><span data-stu-id="8bf31-126">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span></P></LI></UL>

    
    </div>

<span data-ttu-id="8bf31-127">これらのシナリオのいずれかまたはすべてを有効にするには、お客様が Lync Server の展開と外部ユーザーとの間で安全な通信を実現するために、エッジサーバーを展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8bf31-127">To enable any or all of these scenarios, you need to deploy an Edge Server to help enable secure communications between your Lync Server deployment and external users.</span></span> <span data-ttu-id="8bf31-128">組織のリモート ユーザーとフェデレーション組織のユーザーは、IM を使用して互いのプレゼンスと通信を確認できるようになります。</span><span class="sxs-lookup"><span data-stu-id="8bf31-128">Your organization’s remote users and users at federated organizations will be able to see each other’s presence and communicate using IM.</span></span> <span data-ttu-id="8bf31-129">外部ユーザーとの通信を有効にする方法の詳細については、計画ドキュメントの「 [Lync Server 2013 での外部ユーザーアクセスの計画](lync-server-2013-planning-for-external-user-access.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8bf31-129">For details about enabling communication with external users, see [Planning for external user access in Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) in the Planning documentation.</span></span>

</div>

<div>

## <a name="archiving-im-content"></a><span data-ttu-id="8bf31-130">IM コンテンツのアーカイブ</span><span class="sxs-lookup"><span data-stu-id="8bf31-130">Archiving IM Content</span></span>

<span data-ttu-id="8bf31-131">Lync Server には、組織がコンプライアンス規則に従う必要がある場合に使用できる機能が用意されています。</span><span class="sxs-lookup"><span data-stu-id="8bf31-131">Lync Server provides features you can use if your organization must follow compliance regulations.</span></span> <span data-ttu-id="8bf31-132">アーカイブを使用すると、組織内のすべてのユーザーまたは指定する特定のユーザーの IM メッセージの内容をアーカイブすることができます。</span><span class="sxs-lookup"><span data-stu-id="8bf31-132">You can use Archiving to archive the content of IM messages for all users in your organization or for only certain users that you specify.</span></span> <span data-ttu-id="8bf31-133">詳細については、計画ドキュメントの「 [Lync Server 2013 でのアーカイブの計画](lync-server-2013-planning-for-archiving.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8bf31-133">For details, see [Planning for Archiving in Lync Server 2013](lync-server-2013-planning-for-archiving.md) in the Planning documentation.</span></span>

<span data-ttu-id="8bf31-134">Microsoft Exchange Server 2013 が展開されている場合は、Exchange データのアーカイブを Lync Server データのアーカイブと統合することができます。また、単一のツールを使用して、両方の種類のアーカイブデータを検索することもできます。</span><span class="sxs-lookup"><span data-stu-id="8bf31-134">If you also have Microsoft Exchange Server 2013 deployed, you can integrate the archiving of Exchange data with the archiving of Lync Server data, and use a single tool to search both types of archived data.</span></span> <span data-ttu-id="8bf31-135">詳細については、「microsoft [Lync server 2013 で Microsoft Exchange Server 2013 アーカイブを使用するように構成する](configuring-lync-server-2013-to-use-microsoft-exchange-server-2013-archiving.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8bf31-135">For more information, see [Configuring Microsoft Lync Server 2013 to use Microsoft Exchange Server 2013 archiving](configuring-lync-server-2013-to-use-microsoft-exchange-server-2013-archiving.md).</span></span>

<span data-ttu-id="8bf31-136"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8bf31-136"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

