---
title: 'Lync Server 2013: エッジサーバーのコマンドレット'
description: 'Lync Server 2013: Edge Server コマンドレット。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Edge Server cmdlets
ms:assetid: 1a5427f4-a0d1-4652-8135-91333158ffc8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415635(v=OCS.15)
ms:contentKeyID: 48183534
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4b73172331ddcde76672cccda682669f71dd7262
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49397898"
---
# <a name="edge-server-cmdlets-in-lync-server-2013"></a><span data-ttu-id="5cd86-103">Lync Server 2013 のエッジサーバーコマンドレット</span><span class="sxs-lookup"><span data-stu-id="5cd86-103">Edge Server cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5cd86-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5cd86-104">

<span> </span></span></span>

<span data-ttu-id="5cd86-105">_**最終更新日:** 2013-10-07_</span><span class="sxs-lookup"><span data-stu-id="5cd86-105">_**Topic Last Modified:** 2013-10-07_</span></span>

<span data-ttu-id="5cd86-106">エッジサーバーは、Microsoft Lync Server 2013 の機能を、内部ネットワークにログオンしていないユーザーに拡張するための手段を提供します。</span><span class="sxs-lookup"><span data-stu-id="5cd86-106">Edge Servers provide a way for you to extend the capabilities of Microsoft Lync Server 2013 to people who are not logged on to your internal network.</span></span> <span data-ttu-id="5cd86-107">たとえば、内部ネットワーク経由ではなくインターネット経由で Lync Server 2013 にログオンするリモートユーザーが認証されている場合は、Lync Server アクセスエッジサービスを実行するエッジサーバーをセットアップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5cd86-107">For example, if you have remote users -- authenticated users who log on to Lync Server 2013 over the Internet rather than through the internal network -- you will need to set up an Edge Server that runs the Lync Server Access Edge service.</span></span> <span data-ttu-id="5cd86-108">さらに、別の組織とのフェデレーションを確立する場合や、ユーザーが Yahoo \! 、AOL、MSN などのパブリックインスタントメッセージングサービスを使用するユーザーと通信できるようにする場合は、エッジサーバーが必要です。</span><span class="sxs-lookup"><span data-stu-id="5cd86-108">Additionally, Edge Servers are required if you want to establish federation with another organization or if you want to give your users the right to communicate with people who have accounts with a public instant messaging service such as Yahoo\!, AOL, or MSN.</span></span>

<div>


> [!IMPORTANT]
> <UL>
> <LI>
> <P><span data-ttu-id="5cd86-109">2012年9月1日以降、Microsoft Lync パブリック IM 接続ユーザーサブスクリプションライセンス ("PIC USL") は、新規または更新契約の購入に使用できなくなりました。</span><span class="sxs-lookup"><span data-stu-id="5cd86-109">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) is no longer available for purchase for new or renewing agreements.</span></span> <span data-ttu-id="5cd86-110">アクティブなライセンスを持っているお客様は、Yahoo! とのフェデレーションを継続できます。</span><span class="sxs-lookup"><span data-stu-id="5cd86-110">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="5cd86-111">サービスが終了するまでの Messenger。</span><span class="sxs-lookup"><span data-stu-id="5cd86-111">Messenger until the service shut down date.</span></span> <span data-ttu-id="5cd86-112">AOL および Yahoo! の2014年6月の終了日</span><span class="sxs-lookup"><span data-stu-id="5cd86-112">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="5cd86-113">が発表されました。</span><span class="sxs-lookup"><span data-stu-id="5cd86-113">has been announced.</span></span> <span data-ttu-id="5cd86-114">詳細については、「 <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Lync Server 2013 でのパブリックインスタントメッセンジャー接続のサポート</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5cd86-114">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
> <LI>
> <P><span data-ttu-id="5cd86-115">PIC USL は、Lync Server または Office Communications Server が Yahoo! とのフェデレーションを行うために必要な1か月あたりのユーザーごとのサブスクリプションライセンスです。</span><span class="sxs-lookup"><span data-stu-id="5cd86-115">The PIC USL is a per-user per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="5cd86-116">Messenger.</span><span class="sxs-lookup"><span data-stu-id="5cd86-116">Messenger.</span></span> <span data-ttu-id="5cd86-117">このサービスを提供するための Microsoft の機能は、Yahoo! からのサポートによって決定されたものであり、その基となる契約は "巻停止" となります。</span><span class="sxs-lookup"><span data-stu-id="5cd86-117">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which is winding down.</span></span></P>
> <LI>
> <P><span data-ttu-id="5cd86-118">Lync は、組織間、および世界各地の個人と接続するための強力なツールです。</span><span class="sxs-lookup"><span data-stu-id="5cd86-118">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="5cd86-119">Windows Live Messenger とのフェデレーションには、Lync 標準 CAL 以外の追加のユーザー/デバイスライセンスは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="5cd86-119">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="5cd86-120">Skype federation はこのリストに追加されます。 Lync ユーザーは、IM と音声を使用して、数百人の何百万ものユーザーに連絡できます。</span><span class="sxs-lookup"><span data-stu-id="5cd86-120">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span></P></LI></UL>



</div>

<div>

## <a name="edge-server-cmdlets"></a><span data-ttu-id="5cd86-121">エッジサーバーのコマンドレット</span><span class="sxs-lookup"><span data-stu-id="5cd86-121">Edge Server Cmdlets</span></span>

<span data-ttu-id="5cd86-122">エッジサーバーの管理に直接関連するコマンドレットの一覧を次に示します。</span><span class="sxs-lookup"><span data-stu-id="5cd86-122">The following is a list of cmdlets that relate directly to managing Edge Servers:</span></span>

<span data-ttu-id="5cd86-123">**エッジ サーバー**</span><span class="sxs-lookup"><span data-stu-id="5cd86-123">**Edge Server**</span></span>

  - <span></span>  
    <span data-ttu-id="5cd86-124">[Get-CsAccessEdgeConfiguration](https://technet.microsoft.com/library/Gg398574(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="5cd86-124">[Get-CsAccessEdgeConfiguration](https://technet.microsoft.com/library/Gg398574(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="5cd86-125">[Set-CsAccessEdgeConfiguration](https://technet.microsoft.com/library/Gg413017(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="5cd86-125">[Set-CsAccessEdgeConfiguration](https://technet.microsoft.com/library/Gg413017(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="5cd86-126">[Get-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg413008(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="5cd86-126">[Get-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg413008(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="5cd86-127">[新規-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg412884(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="5cd86-127">[New-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg412884(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="5cd86-128">[Remove-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg398786(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="5cd86-128">[Remove-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg398786(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="5cd86-129">[Set-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg412869(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="5cd86-129">[Set-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg412869(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="5cd86-130">[Test-CsAVEdgeConnectivity](https://technet.microsoft.com/library/JJ205138(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="5cd86-130">[Test-CsAVEdgeConnectivity](https://technet.microsoft.com/library/JJ205138(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="5cd86-131">[Set-CsEdgeServer](https://technet.microsoft.com/library/Gg398859(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="5cd86-131">[Set-CsEdgeServer](https://technet.microsoft.com/library/Gg398859(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="5cd86-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="5cd86-132">See Also</span></span>


[<span data-ttu-id="5cd86-133">Lync Server PowerShell ブログ</span><span class="sxs-lookup"><span data-stu-id="5cd86-133">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="5cd86-134"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5cd86-134"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

