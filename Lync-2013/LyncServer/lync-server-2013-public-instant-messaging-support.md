---
title: 'Lync Server 2013: パブリック インスタント メッセージングのサポート'
description: 'Lync Server 2013: パブリックインスタントメッセージングのサポート。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Public instant messaging support
ms:assetid: 1f45163b-52c6-4a78-b9c8-dfe3abe4e5eb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204732(v=OCS.15)
ms:contentKeyID: 48183582
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1e071e8b79be82d865a85a9488e48dd0a4264c7f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399080"
---
# <a name="public-instant-messaging-support-in-lync-server-2013"></a><span data-ttu-id="fec81-103">Lync Server 2013 でのパブリック インスタント メッセージングのサポート</span><span class="sxs-lookup"><span data-stu-id="fec81-103">Public instant messaging support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fec81-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fec81-104">

<span> </span></span></span>

<span data-ttu-id="fec81-105">_**最終更新日:** 2013-10-07_</span><span class="sxs-lookup"><span data-stu-id="fec81-105">_**Topic Last Modified:** 2013-10-07_</span></span>

<span data-ttu-id="fec81-106">Lync Server 2013 では、ライセンス供与されたパブリックメッセージング (IM) 接続プロバイダーの使用、および Lync Server が Lync 2013 クライアントを使用して構成された XMPP ドメインパートナーにアクセスできるようにする、拡張メッセージングとプレゼンスプロトコル (XMPP) の使用をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="fec81-106">Lync Server 2013 supports the use of licensed public instant messaging (IM) connectivity providers, as well as the use of eXtensible Messaging and Presence Protocol (XMPP) to implement a special type of federation that enables a Lync Server to access configured XMPP domain partners by using the Lync 2013 client.</span></span>

<div>

## <a name="public-im-connectivity-provider-support"></a><span data-ttu-id="fec81-107">パブリック IM 接続プロバイダーのサポート</span><span class="sxs-lookup"><span data-stu-id="fec81-107">Public IM Connectivity Provider Support</span></span>

<span data-ttu-id="fec81-108">現在サポートされているパブリックインスタントメッセージング接続パートナーは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="fec81-108">The currently supported public instant messaging connectivity partners are:</span></span>

  - <span data-ttu-id="fec81-109">America Online</span><span class="sxs-lookup"><span data-stu-id="fec81-109">America Online</span></span>

  - <span data-ttu-id="fec81-110">Windows Live</span><span class="sxs-lookup"><span data-stu-id="fec81-110">Windows Live</span></span>

  - <span data-ttu-id="fec81-111">!\!</span><span class="sxs-lookup"><span data-stu-id="fec81-111">Yahoo\!</span></span>

<span data-ttu-id="fec81-112">Windows Live ユーザーとの通信には、Lync Server 2013 でピアツーピアの IM、音声通話、ビデオ通話がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="fec81-112">For communications with Windows Live users, Lync Server 2013 supports peer-to-peer IM and audio and video calls.</span></span> <span data-ttu-id="fec81-113">AOL および Yahoo との通信に \! は、Lync Server 2013 でピアツーピア IM がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="fec81-113">For communications with AOL and Yahoo\!, Lync Server 2013 supports peer-to-peer IM.</span></span> <span data-ttu-id="fec81-114">別のライセンスが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="fec81-114">A separate license may be required.</span></span>

<div>


> [!IMPORTANT]  
> <UL>
> <LI>
> <P><span data-ttu-id="fec81-115">2012年9月1日以降、Microsoft Lync パブリック IM 接続ユーザーサブスクリプションライセンス ("PIC USL") は、新規または更新契約の購入に使用できなくなりました。</span><span class="sxs-lookup"><span data-stu-id="fec81-115">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) is no longer available for purchase for new or renewing agreements.</span></span> <span data-ttu-id="fec81-116">アクティブなライセンスを持っているお客様は、Yahoo! とのフェデレーションを継続できます。</span><span class="sxs-lookup"><span data-stu-id="fec81-116">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="fec81-117">サービスが終了するまでの Messenger。</span><span class="sxs-lookup"><span data-stu-id="fec81-117">Messenger until the service shut down date.</span></span> <span data-ttu-id="fec81-118">AOL および Yahoo! の2014年6月の終了日</span><span class="sxs-lookup"><span data-stu-id="fec81-118">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="fec81-119">が発表されました。</span><span class="sxs-lookup"><span data-stu-id="fec81-119">has been announced.</span></span> <span data-ttu-id="fec81-120">詳細については、「 <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Lync Server 2013 でのパブリックインスタントメッセンジャー接続のサポート</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fec81-120">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
> <LI>
> <P><span data-ttu-id="fec81-121">PIC USL は、Lync Server または Office Communications Server が Yahoo! とのフェデレーションを行うために必要な1か月あたりのユーザーごとのサブスクリプションライセンスです。</span><span class="sxs-lookup"><span data-stu-id="fec81-121">The PIC USL is a per-user per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="fec81-122">Messenger.</span><span class="sxs-lookup"><span data-stu-id="fec81-122">Messenger.</span></span> <span data-ttu-id="fec81-123">このサービスを提供するための Microsoft の機能は、Yahoo! からのサポートによって決定されたものであり、その基となる契約は "巻停止" となります。</span><span class="sxs-lookup"><span data-stu-id="fec81-123">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which is winding down.</span></span></P>
> <LI>
> <P><span data-ttu-id="fec81-124">Lync は、組織間、および世界各地の個人と接続するための強力なツールです。</span><span class="sxs-lookup"><span data-stu-id="fec81-124">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="fec81-125">Windows Live Messenger とのフェデレーションには、Lync 標準 CAL 以外の追加のユーザー/デバイスライセンスは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="fec81-125">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="fec81-126">Skype federation はこのリストに追加されます。 Lync ユーザーは、IM と音声を使用して、数百人の何百万ものユーザーに連絡できます。</span><span class="sxs-lookup"><span data-stu-id="fec81-126">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span></P></LI></UL>



</div>

</div>

<div>

## <a name="xmpp-federation-support"></a><span data-ttu-id="fec81-127">XMPP フェデレーションサポート</span><span class="sxs-lookup"><span data-stu-id="fec81-127">XMPP Federation Support</span></span>

<span data-ttu-id="fec81-128">XMPP フェデレーションは、GTalk などのパブリックプロバイダーを使用する構成済みの XMPP ドメインユーザーとの Lync ユーザーとの通信をサポートします。</span><span class="sxs-lookup"><span data-stu-id="fec81-128">XMPP federation supports Lync users communication with configured XMPP domain users who use a public provider, such as GTalk.</span></span> <span data-ttu-id="fec81-129">次のようなユーザーとのコミュニケーションを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="fec81-129">Communications with these users can include the following:</span></span>

  - <span data-ttu-id="fec81-130">ピアツーピアの IM とプレゼンス</span><span class="sxs-lookup"><span data-stu-id="fec81-130">Peer-to-peer IM and presence</span></span>

  - <span data-ttu-id="fec81-131">Lync クライアントでの XMPP フェデレーション連絡先の作成</span><span class="sxs-lookup"><span data-stu-id="fec81-131">Creation of XMPP federated contacts in the Lync client</span></span>

<span data-ttu-id="fec81-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fec81-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

