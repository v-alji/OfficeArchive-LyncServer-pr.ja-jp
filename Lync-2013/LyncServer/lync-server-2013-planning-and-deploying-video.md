---
title: 'Lync Server 2013: ビデオの計画と展開'
description: 'Lync Server 2013: ビデオの計画と展開。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning and deploying video
ms:assetid: dadfb7f3-dfd6-4847-b137-17dacafd7368
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205307(v=OCS.15)
ms:contentKeyID: 48185558
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b9fd8a93f890295daebd2bc887414a2417b86395
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398457"
---
# <a name="planning-and-deploying-video-in-lync-server-2013"></a><span data-ttu-id="a024b-103">Lync Server 2013 でのビデオの計画と展開</span><span class="sxs-lookup"><span data-stu-id="a024b-103">Planning and deploying video in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a024b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a024b-104">

<span> </span></span></span>

<span data-ttu-id="a024b-105">_**最終更新日:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="a024b-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="a024b-106">Lync Server 2013 には、次の新しいビデオ機能が導入されています。</span><span class="sxs-lookup"><span data-stu-id="a024b-106">Lync Server 2013 introduces the following new video features:</span></span>

  - <span data-ttu-id="a024b-107">**HD ビデオ**   ユーザーは、2パーティーの通話とマルチパーティの会議で、フル品位 (HD) (1920 x 1080) までの解像度を体験できます。</span><span class="sxs-lookup"><span data-stu-id="a024b-107">**HD video**   Users can experience resolutions up to full high definition (HD) (that is, 1920 x 1080) in two-party calls and multiparty conferences.</span></span>

  - <span data-ttu-id="a024b-108">**ギャラリービュー**   2人以上のユーザーがいるビデオ会議では、ユーザーは会議の参加者のビデオを見ることができます。</span><span class="sxs-lookup"><span data-stu-id="a024b-108">**Gallery View**   In video conferences that have more than two people, users can see videos of participants in the conference.</span></span> <span data-ttu-id="a024b-109">会議に5人以上の参加者がいる場合は、最もアクティブな参加者のみのビデオが一番上の行に表示され、他の参加者の写真が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a024b-109">If the conference has more than five participants, video of only the most active participants appears in the top row, and a photo appears for the other participants.</span></span>

  - <span data-ttu-id="a024b-110">**.H ビデオ**   Lync 2013 クライアント上のビデオをエンコードするための既定の形式は、"264" ビデオコーデックです。</span><span class="sxs-lookup"><span data-stu-id="a024b-110">**H.264 video**   The H.264 video codec is now the default for encoding video on Lync 2013 clients.</span></span> <span data-ttu-id="a024b-111">.H ビデオでは、さまざまな解像度とフレームレートをサポートしており、ビデオのスケーラビリティが向上しています。</span><span class="sxs-lookup"><span data-stu-id="a024b-111">H.264 video supports a greater range of resolutions and frame rates, and improves video scalability.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a024b-112">Lync Server 2013 は、以前のバージョンの Lync との相互運用性を実現するために、引き続き VC1 コーデックをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="a024b-112">Lync Server 2013 still supports the VC1 codec for interoperability with previous versions of Lync.</span></span> <span data-ttu-id="a024b-113">新しいビデオコーデックの詳細および背景情報については、「Jeff の概要」のブログ記事「Lync 2013 でのビデオの相互運用性」を参照してください <A class=uri href="http://blog.schertz.name/2012/07/video-interoperability-in-lync-2013/">http://blog.schertz.name/2012/07/video-interoperability-in-lync-2013/</A> 。</span><span class="sxs-lookup"><span data-stu-id="a024b-113">For details and background information about the new video codec, see Jeff Schertz's Blog article, "Video Interoperability in Lync 2013," at <A class=uri href="http://blog.schertz.name/2012/07/video-interoperability-in-lync-2013/">http://blog.schertz.name/2012/07/video-interoperability-in-lync-2013/</A>.</span></span>

    
    </div>

<span data-ttu-id="a024b-114">このセクションでは、Lync Server 2013 でビデオの帯域幅を管理する方法と、ビデオ機能を構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a024b-114">This section describes how to manage bandwidth for video in Lync Server 2013 and how to configure video features.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="a024b-115">このセクション中</span><span class="sxs-lookup"><span data-stu-id="a024b-115">In This Section</span></span>

  - [<span data-ttu-id="a024b-116">Lync Server 2013 でのビデオ帯域幅の構成</span><span class="sxs-lookup"><span data-stu-id="a024b-116">Configuring video bandwidth in Lync Server 2013</span></span>](lync-server-2013-configuring-video-bandwidth.md)

  - [<span data-ttu-id="a024b-117">Lync Server 2013 でギャラリービューを構成する</span><span class="sxs-lookup"><span data-stu-id="a024b-117">Configuring Gallery View in Lync Server 2013</span></span>](lync-server-2013-configuring-gallery-view.md)

  - [<span data-ttu-id="a024b-118">ビデオの構成 Lync Server 2013 のシナリオの例</span><span class="sxs-lookup"><span data-stu-id="a024b-118">Configuring video example scenarios for Lync Server 2013</span></span>](lync-server-2013-configuring-video-example-scenarios.md)

  - [<span data-ttu-id="a024b-119">Lync Server 2013 でのビデオ会議の相互運用性に関する考慮事項</span><span class="sxs-lookup"><span data-stu-id="a024b-119">Interoperability considerations for video conferencing in Lync Server 2013</span></span>](lync-server-2013-interoperability-considerations-for-video-conferencing.md)

<span data-ttu-id="a024b-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a024b-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

