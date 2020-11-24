---
title: 'Lync Server 2013: 外部ユーザー アクセスの概要'
description: 'Lync Server 2013: 外部ユーザーアクセスの概要。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of external user access
ms:assetid: 97aded6c-5fa3-4225-95a6-9ad094d61654
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398775(v=OCS.15)
ms:contentKeyID: 48184934
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d2900dde457da34c4438892878ae7ddb4f74723a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399549"
---
# <a name="overview-of-external-user-access-in-lync-server-2013"></a><span data-ttu-id="f23a4-103">Lync Server 2013 における外部ユーザー アクセスの概要</span><span class="sxs-lookup"><span data-stu-id="f23a4-103">Overview of external user access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f23a4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f23a4-104">

<span> </span></span></span>

<span data-ttu-id="f23a4-105">_**最終更新日:** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="f23a4-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="f23a4-106">このドキュメントでは、 *外部ユーザー* という用語を使用して、ファイアウォールの外側から lync Server 2013 および lync 2013 ユーザーと通信する大規模なユーザーのカテゴリを定義しています。</span><span class="sxs-lookup"><span data-stu-id="f23a4-106">In this documentation, we use the term *external user* to define a large category of users who communicate with your Lync Server 2013 and Lync 2013 users from outside the firewall.</span></span> <span data-ttu-id="f23a4-107">Lync Server 2013 と内部ユーザーとの通信を承認できる外部ユーザー (つまり、ファイアウォール内から Lync Server にサインインしているユーザー) には、次のものが含まれます。</span><span class="sxs-lookup"><span data-stu-id="f23a4-107">External users that you can authorize to communicate Lync Server 2013 with internal users (that is, users who sign in to Lync Server from inside the firewall) can include the following:</span></span>

  - <span data-ttu-id="f23a4-108">**リモートユーザー**   ファイアウォールの外側から Lync Server にサインインしている組織のユーザー。</span><span class="sxs-lookup"><span data-stu-id="f23a4-108">**Remote users**   Users of your organization who sign in to Lync Server from outside the firewall.</span></span>

  - <span data-ttu-id="f23a4-109">**フェデレーション**   されたユーザー  Lync Server 2010、Lync Server 2013、Office Communications Server 2007 R2 など、信頼できる顧客またはパートナーの組織のアカウントを持っているユーザー。</span><span class="sxs-lookup"><span data-stu-id="f23a4-109">**Federated users**   Users who have an account with a trusted customer or partner organization, such as Lync Server 2010, Lync Server 2013 or Office Communications Server 2007 R2.</span></span> <span data-ttu-id="f23a4-110">フェデレーションされたユーザーは、エッジサーバー上の XMPP プロキシと、フロントエンドサーバーまたはプール上の XMPP ゲートウェイを使用して、定義済みパートナー組織のメンバーになることもできます。</span><span class="sxs-lookup"><span data-stu-id="f23a4-110">Federated users can also be members of defined partner organizations using extensible messaging and presence protocol (XMPP) by way of the XMPP proxy on the Edge Server and XMPP gateway on the Front End Server or pool.</span></span> <span data-ttu-id="f23a4-111">フェデレーションと呼ばれる定義済みの信頼関係は、Active Directory ドメインサービスの信頼関係に関連していないか、または依存していません。</span><span class="sxs-lookup"><span data-stu-id="f23a4-111">A defined trust relationship, called a federation, is not related to or dependent upon an Active Directory Domain Services trust relationship.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="f23a4-112">AOL および Yahoo! の2014年6月の終了日</span><span class="sxs-lookup"><span data-stu-id="f23a4-112">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="f23a4-113">が発表されました。</span><span class="sxs-lookup"><span data-stu-id="f23a4-113">has been announced.</span></span> <span data-ttu-id="f23a4-114">詳細については、「 <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Lync Server 2013 でのパブリックインスタントメッセンジャー接続のサポート</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f23a4-114">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span>

    
    </div>

  - <span data-ttu-id="f23a4-115">**パブリックインスタントメッセージング接続ユーザー**   パブリックインスタントメッセージング接続サービス (Windows Live、Yahoo) を介してユーザーが確立した連絡先\!</span><span class="sxs-lookup"><span data-stu-id="f23a4-115">**Public Instant Messaging Connectivity users**   Contacts that your users establish through public instant messaging connectivity services (Windows Live, Yahoo\!</span></span> <span data-ttu-id="f23a4-116">および AOL)。</span><span class="sxs-lookup"><span data-stu-id="f23a4-116">and AOL).</span></span>

  - <span data-ttu-id="f23a4-117">**モバイルユーザー**   組織のメンバーであり、スマートフォンまたはタブレットを使用していて、Lync モバイルクライアントを実行しているユーザーは、内部展開にサインインして、他のクラスのユーザーと通信できます。</span><span class="sxs-lookup"><span data-stu-id="f23a4-117">**Mobile users**   Users that are members of your organization that use a smart phone or tablet running a Lync Mobile client sign in to your internal deployment and are able to communicate with the other classes of users.</span></span> <span data-ttu-id="f23a4-118">モバイルユーザーは、リバースプロキシ経由で公開されているモビリティーサービスを使って、内部展開にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="f23a4-118">The mobile user uses mobility services that are published through the reverse proxy to access the internal deployment.</span></span> <span data-ttu-id="f23a4-119">Lync Mobile で利用できる機能の詳細については、「モバイルクライアントの比較表」を参照してください [https://go.microsoft.com/fwlink/p/?LinkID=234777](https://go.microsoft.com/fwlink/p/?linkid=234777) 。</span><span class="sxs-lookup"><span data-stu-id="f23a4-119">For details on features and capabilities available to Lync Mobile , see the Mobile Client Comparison Tables at [https://go.microsoft.com/fwlink/p/?LinkID=234777](https://go.microsoft.com/fwlink/p/?linkid=234777).</span></span>

  - <span data-ttu-id="f23a4-120">**匿名ユーザー**   組織の Active Directory ドメインサービスまたはサポートされているフェデレーションドメインでユーザーアカウントを持っていないユーザーが、オンプレミスの会議にリモートで参加するための招待を受信したユーザー。</span><span class="sxs-lookup"><span data-stu-id="f23a4-120">**Anonymous users**   Users who do not have a user account in your organization's Active Directory Domain Services or in a supported federated domain, but who have received invitations to participate remotely in an on-premises conference.</span></span>

<span data-ttu-id="f23a4-121">エッジの展開では、次の種類の通信に対する外部アクセスが提供されます。</span><span class="sxs-lookup"><span data-stu-id="f23a4-121">Your edge deployment provides external access for the following types of communication:</span></span>

  - <span data-ttu-id="f23a4-122">**IM とプレゼンス**   承認された外部ユーザーは、IM の会話と会議に参加することができます。また、互いのプレゼンス状態に関する情報を取得することもできます。</span><span class="sxs-lookup"><span data-stu-id="f23a4-122">**IM and presence**   Authorized external users can participate in IM conversations and conferences, and they can get information about one another’s presence status.</span></span> <span data-ttu-id="f23a4-123">パブリック IM サービスプロバイダーのユーザーは、組織内の個々の Lync サーバーユーザーとの IM 会話に参加したり、プレゼンス情報にアクセスしたりすることはできますが、Lync Server を使って IM マルチパーティ会議に参加することはできません。</span><span class="sxs-lookup"><span data-stu-id="f23a4-123">Users of public IM service providers can participate in IM conversations with individual Lync Server users in your organization and access presence information, but they cannot participate in IM multiparty conferences using Lync Server.</span></span> <span data-ttu-id="f23a4-124">これは、厳密なピアツーピア通信です。</span><span class="sxs-lookup"><span data-stu-id="f23a4-124">It is strictly peer-to-peer communication.</span></span> <span data-ttu-id="f23a4-125">ファイル送信は、パブリック IM サービスプロバイダーのユーザーに対してはサポートされておらず、ピアツーピア通信での音声/ビデオは、Windows Messenger 2011 ユーザーに対してはサポートされていますが、パブリック IM サービスプロバイダーの他のユーザーには対応していません。</span><span class="sxs-lookup"><span data-stu-id="f23a4-125">File transfer is not supported for users of public IM service providers, and audio/video in peer-to-peer communications is supported for Windows Messenger 2011 users, but not other users of public IM service providers.</span></span>
    
    <span data-ttu-id="f23a4-126">SIP と XMPP の両方のプロトコルがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="f23a4-126">Both SIP and XMPP protocols are supported.</span></span> <span data-ttu-id="f23a4-127">XMPP のサービスを提供するには、「 [Lync Server 2013 での SIP、XMPP フェデレーション、およびパブリックインスタントメッセージングの計画](lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f23a4-127">To provide services for XMPP, see [Planning for SIP, XMPP federation, and public instant messaging in Lync Server 2013](lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md).</span></span>

  - <span data-ttu-id="f23a4-128">**Web 会議**   承認済みの外部ユーザーは、Lync Server の展開でホストされている会議に参加できます。</span><span class="sxs-lookup"><span data-stu-id="f23a4-128">**Web conferencing**   Authorized external users can participate in conferences that are hosted on your Lync Server deployment.</span></span> <span data-ttu-id="f23a4-129">リモートユーザー、フェデレーションユーザー、匿名ユーザーは、web 会議への参加を有効にできますが、パブリック IM ユーザーは会議に参加できません。</span><span class="sxs-lookup"><span data-stu-id="f23a4-129">Remote users, federated users, and anonymous users can be enabled for participation in web conferencing, but public IM users cannot participate in conferences.</span></span> <span data-ttu-id="f23a4-130">選択したオプションに応じて、web 会議対応ユーザーはデスクトップとアプリケーションの共有に参加でき、会議の開催者または発表者として機能することができます。</span><span class="sxs-lookup"><span data-stu-id="f23a4-130">Depending on the options that you select, web conferencing-enabled users can participate in desktop and application sharing and can act as meeting organizers or presenters.</span></span>

  - <span data-ttu-id="f23a4-131">**A/V 会議**   承認された外部ユーザーは、Lync Server 展開でホストされている音声会議やビデオ会議に参加できます。</span><span class="sxs-lookup"><span data-stu-id="f23a4-131">**A/V conferencing**   Authorized external users can participate in audio and video conferences that your Lync Server deployment hosts.</span></span> <span data-ttu-id="f23a4-132">ピアツーピア通信での音声/ビデオは、Windows Messenger 2011 ユーザーに対してはサポートされますが、パブリック IM サービスプロバイダーの他のユーザーには対応していません。</span><span class="sxs-lookup"><span data-stu-id="f23a4-132">Audio/video in peer-to-peer communications is supported for Windows Messenger 2011 users, but not for other users of public IM service providers.</span></span>

<span data-ttu-id="f23a4-133">通信を制御するために、組織内外のユーザーが相互に通信する方法を定義する1つまたは複数のポリシーを構成することができます。</span><span class="sxs-lookup"><span data-stu-id="f23a4-133">In order to control communications, you can configure one or more policies that define how users inside and outside your organization communicate with each other.</span></span> <span data-ttu-id="f23a4-134">また、個々の内部ユーザーの設定を構成し、ポリシーを適用することができます。また、外部ユーザーとの通信を制御するために、特定の種類の外部ユーザーのポリシーを適用することもできます</span><span class="sxs-lookup"><span data-stu-id="f23a4-134">You can also configure settings and apply policies for individual internal users or for specific types of external users to control communications with external users.</span></span>

<span data-ttu-id="f23a4-135">外部アクセスを提供するために使用される Lync Server 2013 の役割:</span><span class="sxs-lookup"><span data-stu-id="f23a4-135">Lync Server 2013 roles that are used to provide external access:</span></span>

<span data-ttu-id="f23a4-136">**エッジサーバー**   エッジサーバーは、IM、プレゼンス、会議、音声/ビデオ、その他のメディア (ファイル転送など) サービスへの外部アクセスを可能にするサービスを実行するサーバーまたはサーバーのプールです。</span><span class="sxs-lookup"><span data-stu-id="f23a4-136">**Edge Server**   The Edge Server is a server or a pool of servers that run the services that allow external access to IM and presence, conferencing, audio/video, and other media (for example, file transfer) services.</span></span> <span data-ttu-id="f23a4-137">必要に応じて、他の Lync Server または Office Communications Server 2007 R2 の展開と他の XMPP の展開とのフェデレーションを行うようにエッジサーバーを構成することができます。</span><span class="sxs-lookup"><span data-stu-id="f23a4-137">Optionally, you can configure the Edge Server to federate with other Lync Server or Office Communications Server 2007 R2 deployments, and other XMPP deployments.</span></span> <span data-ttu-id="f23a4-138">オプションのパブリック IM 接続機能が有効になり、エッジサーバーによって構成されます。</span><span class="sxs-lookup"><span data-stu-id="f23a4-138">The optional public IM connectivity feature is enabled and configured through the Edge Server.</span></span>

<span data-ttu-id="f23a4-139">**監督**   ディレクターは、ユーザー要求の事前認証とユーザーのホームフロントエンドサーバーまたはフロントエンドプールへの要求のルーティングを実行する、Lync Server 2013 ディレクターの役割を実行する、オプションのサーバーまたはサーバープールですが、ユーザーアカウントのホームにはなりません。</span><span class="sxs-lookup"><span data-stu-id="f23a4-139">**Director**   The Director is an optional server or server pool running the Lync Server 2013 Director role that pre-authenticates user requests and routes requests to the users’ home Front End Server or Front End pool, but does not home any user accounts.</span></span>

<span data-ttu-id="f23a4-140">**リバースプロキシ**   リバースプロキシは、内部ネットワークで利用可能なリソースを公開し、公開されたリソースからクライアントの情報を取得する、専用サーバーの一般的な用語です。</span><span class="sxs-lookup"><span data-stu-id="f23a4-140">**Reverse Proxy**   A reverse proxy is a general term for specialized servers that publish resources available on the internal network and retrieve information for clients from the published resource.</span></span> <span data-ttu-id="f23a4-141">Lync Server 2013 は、リバースプロキシを使用して、会議会議、電話会議の場所、アドレス帳、配布リストの拡張、会議コンテンツのダウンロード、デバイスの更新、モバイルサービスなど、さまざまな機能を公開します。</span><span class="sxs-lookup"><span data-stu-id="f23a4-141">Lync Server 2013 uses the reverse proxy to publish a number of features, such as conferencing meetings, conference join locations, the address book, distribution list expansion, downloading meeting content, device updates, Mobility services, and more.</span></span> <span data-ttu-id="f23a4-142">必要なリソースの場所を公開するための要件を満たしているリバースプロキシを使用できます。</span><span class="sxs-lookup"><span data-stu-id="f23a4-142">Any reverse proxy that can meet the requirements for publishing the necessary resource locations can be used.</span></span> <span data-ttu-id="f23a4-143">Microsoft Forefront Threat Management Gateway (TMG) 2010 は、必要な公開ルールを示す目的で例として使用されますが、Forefront TMG 2010 は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="f23a4-143">Microsoft Forefront Threat Management Gateway (TMG) 2010 is used as an example for the purposes of illustrating the publishing rules necessary, but Forefront TMG 2010 is not required.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="f23a4-144">Lync Server 2013 は、IPv4 と IPv6 の両方をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="f23a4-144">Lync Server 2013 supports both IPv4 and IPv6.</span></span> <span data-ttu-id="f23a4-145">Windows server &nbsp; 2008 &nbsp; R2、windows server 2012、および windows Server 2012 R2 では、IPv4 と IPv6 の両方で同時に使用できるデュアルスタックを使用します。</span><span class="sxs-lookup"><span data-stu-id="f23a4-145">Windows Server&nbsp;2008&nbsp;R2, Windows Server 2012, and Windows Server 2012 R2 use a dual stack that can use both IPv4 and IPv6 concurrently.</span></span> <span data-ttu-id="f23a4-146">これは、IPv4 から IPv6 への展開の移行の性質が原因で重要です。</span><span class="sxs-lookup"><span data-stu-id="f23a4-146">This is important because of the transitional nature of a deployment moving from IPv4 to IPv6.</span></span> <span data-ttu-id="f23a4-147">IPv4 は、展開の他の領域で IPv6 を使うことができるいくつかの領域でサポートされます。</span><span class="sxs-lookup"><span data-stu-id="f23a4-147">IPv4 can be supported in some areas, where in other areas of the deployment, IPv6 can be used.</span></span> <span data-ttu-id="f23a4-148">これは、インターネットと社内の展開が関係する場合に特に重要です。</span><span class="sxs-lookup"><span data-stu-id="f23a4-148">This is especially important where the Internet and internal deployments are concerned.</span></span> <span data-ttu-id="f23a4-149">外部クライアントは、モビリティ、会議、アドレス帳のダウンロードなどのサービスを使用するためにリバースプロキシ経由で通信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f23a4-149">External clients must communicate through the reverse proxy to use services such as mobility, meetings, address book download, and others.</span></span> <span data-ttu-id="f23a4-150">現時点では、展開されているオペレーティングシステムのバージョンに関係なく、Forefront Threat Management Gateway 2010 およびインターネットセキュリティとアクセラレータサーバー2006は IPv6 アドレスをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="f23a4-150">Currently, Forefront Threat Management Gateway 2010 and Internet Security and Acceleration Server 2006 do not support IPv6 addressing, regardless of the operating system version that they are deployed on.</span></span> <span data-ttu-id="f23a4-151">IPv6 と IPv4 を外部クライアントと関連付けて使用する場合は、それに合わせて計画する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f23a4-151">You must plan accordingly in relation to your use of IPv6 and IPv4 as they relate to external clients.</span></span>



<span data-ttu-id="f23a4-152"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f23a4-152"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

