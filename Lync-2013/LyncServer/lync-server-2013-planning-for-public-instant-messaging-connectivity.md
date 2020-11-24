---
title: 'Lync Server 2013: パブリックインスタントメッセージング接続の計画'
description: 'Lync Server 2013: パブリックインスタントメッセージング接続の計画。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for public instant messaging connectivity
ms:assetid: e75e8884-05c7-414a-8014-bc9aa8126fb7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205349(v=OCS.15)
ms:contentKeyID: 48185698
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9a020a291a39d78aea9271926c99b508a8cd9827
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400215"
---
# <a name="planning-for-public-instant-messaging-connectivity-in-lync-server-2013"></a><span data-ttu-id="39e7d-103">Lync Server 2013 でのパブリックインスタントメッセージング接続の計画</span><span class="sxs-lookup"><span data-stu-id="39e7d-103">Planning for public instant messaging connectivity in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="39e7d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="39e7d-104">

<span> </span></span></span>

<span data-ttu-id="39e7d-105">_**最終更新日:** 2013-10-07_</span><span class="sxs-lookup"><span data-stu-id="39e7d-105">_**Topic Last Modified:** 2013-10-07_</span></span>

<span data-ttu-id="39e7d-106">パブリックインスタントメッセージング接続はフェデレーションのクラスであり、内部および外部の Lync Server 2013 ユーザーが次のいずれかから連絡先を追加できるように構成されています。</span><span class="sxs-lookup"><span data-stu-id="39e7d-106">Public Instant Messaging Connectivity is a class of federation, and is configured to allow your internal and external Lync Server 2013 users to add contacts from any of the following:</span></span>

  - <span data-ttu-id="39e7d-107">Messenger の連絡先</span><span class="sxs-lookup"><span data-stu-id="39e7d-107">Messenger contacts</span></span>

  - <span data-ttu-id="39e7d-108">!\!</span><span class="sxs-lookup"><span data-stu-id="39e7d-108">Yahoo\!</span></span> <span data-ttu-id="39e7d-109">連絡先</span><span class="sxs-lookup"><span data-stu-id="39e7d-109">contacts</span></span>

  - <span data-ttu-id="39e7d-110">America Online (AOL) の連絡先</span><span class="sxs-lookup"><span data-stu-id="39e7d-110">America Online (AOL) contacts</span></span>

<div>


> [!IMPORTANT]  
> <UL>
> <LI>
> <P><span data-ttu-id="39e7d-111">2012年9月1日以降、Microsoft Lync パブリック IM 接続ユーザーサブスクリプションライセンス (PIC USL) は、新規または更新契約の購入に使用できなくなりました。</span><span class="sxs-lookup"><span data-stu-id="39e7d-111">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (PIC USL) is no longer available for the purchase for new or renewing agreements.</span></span> <span data-ttu-id="39e7d-112">アクティブなライセンスを持っているお客様は、Yahoo! とのフェデレーションを継続できます。</span><span class="sxs-lookup"><span data-stu-id="39e7d-112">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="39e7d-113">サービスのシャットダウン日までメッセンジャーを終了します。</span><span class="sxs-lookup"><span data-stu-id="39e7d-113">Messenger until the service shutdown date.</span></span> <span data-ttu-id="39e7d-114">AOL および Yahoo! の2014年6月の終了日</span><span class="sxs-lookup"><span data-stu-id="39e7d-114">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="39e7d-115">が発表されました。</span><span class="sxs-lookup"><span data-stu-id="39e7d-115">has been announced.</span></span> <span data-ttu-id="39e7d-116">詳細については、「 <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Lync Server 2013 でのパブリックインスタントメッセンジャー接続のサポート</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39e7d-116">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
> <LI>
> <P><span data-ttu-id="39e7d-117">PIC USL は、Lync Server または Office Communications Server が Yahoo! とのフェデレーションを行うために必要なユーザーごとの1か月間のサブスクリプションライセンスです。</span><span class="sxs-lookup"><span data-stu-id="39e7d-117">The PIC USL is a per-user, per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="39e7d-118">Messenger.</span><span class="sxs-lookup"><span data-stu-id="39e7d-118">Messenger.</span></span> <span data-ttu-id="39e7d-119">このサービスを提供するための Microsoft の機能は、Yahoo! からのサポートによって決定されましたが、その基となる契約は更新されません。</span><span class="sxs-lookup"><span data-stu-id="39e7d-119">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which will not be renewed.</span></span></P>
> <LI>
> <P><span data-ttu-id="39e7d-120">Lync は、組織間、および世界各地の個人と接続するための強力なツールです。</span><span class="sxs-lookup"><span data-stu-id="39e7d-120">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="39e7d-121">Windows Live Messenger とのフェデレーションには、Lync 標準 CAL 以外の追加のユーザー/デバイスライセンスは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="39e7d-121">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="39e7d-122">Skype federation はこのリストに追加されるため、Lync ユーザーは IM や音声を通じて数百人の何百万ものユーザーに連絡できます。</span><span class="sxs-lookup"><span data-stu-id="39e7d-122">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people through IM and voice.</span></span></P></LI></UL>



</div>

<span data-ttu-id="39e7d-123">このクラスのフェデレーションには、次の計画の考慮事項が必要です。</span><span class="sxs-lookup"><span data-stu-id="39e7d-123">This class of federation requires the following planning considerations:</span></span>

  - <span data-ttu-id="39e7d-124">Windows Live Messenger ユーザーは、インスタントメッセージに加えて、Lync Server 2013 ユーザーとのピアツーピアの音声/視覚的コミュニケーションを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="39e7d-124">Windows Live Messenger users can have peer-to-peer audio/visual communication with Lync Server 2013 users, in addition to instant messaging.</span></span> <span data-ttu-id="39e7d-125">エッジサーバーは、特定のポートとプロトコルの要件を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="39e7d-125">Your Edge Servers must meet specific port and protocol requirements.</span></span> <span data-ttu-id="39e7d-126">詳細については、「 [Lync Server 2013 の外部の A/V ファイアウォールとポートの要件を確認する](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39e7d-126">For details, see [Determine external A/V firewall and port requirements for Lync Server 2013](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md).</span></span>

  - <span data-ttu-id="39e7d-127">Yahoo インスタントメッセージには、フェデレーションを提供している一般的なエッジサーバーの計画と展開で通常使用される要件以外の固有の要件はありません。</span><span class="sxs-lookup"><span data-stu-id="39e7d-127">Yahoo instant messaging has no unique requirements, other than those typically used in the planning and deployment of the typical Edge Server that is providing federation.</span></span>

  - <span data-ttu-id="39e7d-128">America Online では、アクセスエッジサービスに割り当てられるエッジサーバー証明書に、クライアント拡張キー使用法 (EKU) が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="39e7d-128">America Online requires that your Edge Server certificate assigned to the Access Edge service has a client enhanced key usage (EKU).</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="39e7d-129">このセクション中</span><span class="sxs-lookup"><span data-stu-id="39e7d-129">In This Section</span></span>

  - [<span data-ttu-id="39e7d-130">証明書の概要-Lync Server 2013 でのパブリックインスタントメッセージング接続</span><span class="sxs-lookup"><span data-stu-id="39e7d-130">Certificate summary - Public instant messaging connectivity in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-public-instant-messaging-connectivity.md)

  - [<span data-ttu-id="39e7d-131">ポートの概要-Lync Server 2013 でのパブリックインスタントメッセージング接続</span><span class="sxs-lookup"><span data-stu-id="39e7d-131">Port summary - Public instant messaging connectivity in Lync Server 2013</span></span>](lync-server-2013-port-summary-public-instant-messaging-connectivity.md)

  - <span data-ttu-id="39e7d-132">[DNS の概要-Lync Server 2013 でのパブリックインスタントメッセージング接続](https://technet.microsoft.com/library/jj618375\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="39e7d-132">[DNS summary - Public instant messaging connectivity in Lync Server 2013](https://technet.microsoft.com/library/jj618375\(v=ocs.15\))</span></span>

<span data-ttu-id="39e7d-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="39e7d-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

