---
title: 'Lync Server 2013: コール パーク アプリケーションの新機能'
description: 'Lync Server 2013: 新しいコールパークアプリケーション機能。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New Call Park application features
ms:assetid: bddff13c-92cc-47fd-bfd4-6e8bfbfed11b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412927(v=OCS.15)
ms:contentKeyID: 48185277
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a000fc288a920773b0dc1e4a7e8fe1fb20fbb3dc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445464"
---
# <a name="new-call-park-application-features-in-lync-server-2013"></a><span data-ttu-id="9b217-103">Lync Server 2013 のコール パーク アプリケーションの新機能</span><span class="sxs-lookup"><span data-stu-id="9b217-103">New Call Park application features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9b217-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9b217-104">

<span> </span></span></span>

<span data-ttu-id="9b217-105">_**最終更新日:** 2012-10-17_</span><span class="sxs-lookup"><span data-stu-id="9b217-105">_**Topic Last Modified:** 2012-10-17_</span></span>

<span data-ttu-id="9b217-106">コールパークアプリケーションを使用すると、エンタープライズボイスユーザーは通話を保留にしてから、どの電話からでも通話を受信することができます。</span><span class="sxs-lookup"><span data-stu-id="9b217-106">The Call Park application makes it possible for Enterprise Voice users to put a call on hold and then retrieve it later from any phone.</span></span> <span data-ttu-id="9b217-107">通話を保留にしたユーザーは、コールパークによって提供された軌道番号をダイヤルして、保留中の通話を取得したり、インスタントメッセージング (IM) やページングシステムなどの外部メカニズムを使って、他の人に通話を取得するように指示することができます。</span><span class="sxs-lookup"><span data-stu-id="9b217-107">The user who parked the call can either dial the orbit number provided by Call Park to retrieve the parked call or use an external mechanism, such as instant messaging (IM) or a paging system, to ask someone else to retrieve the call.</span></span>

<span data-ttu-id="9b217-108">Lync Server 2013 には、フェールオーバーとフェールバックのプロセスの形式での新しい障害回復メカニズムが用意されています。</span><span class="sxs-lookup"><span data-stu-id="9b217-108">Lync Server 2013 provides new disaster recovery mechanisms in the form of failover and failback processes.</span></span> <span data-ttu-id="9b217-109">これらのフェイルオーバーおよびフェイルバック処理は、プライマリプールをホームにしているユーザーが、プライマリプールで停止したときにバックアッププールのコールパークアプリケーションを利用できるようにすることによって、コールパーク機能の回復をサポートします。</span><span class="sxs-lookup"><span data-stu-id="9b217-109">These failover and failback processes support recovery of Call Park functionality by allowing users who are homed in the primary pool to leverage the Call Park application of the backup pool when an outage occurs in the primary pool.</span></span> <span data-ttu-id="9b217-110">コールパークアプリケーションのディザスタリカバリのサポートは、ペアリングされたフロントエンドプールの構成と展開の一環として有効になります。</span><span class="sxs-lookup"><span data-stu-id="9b217-110">Support for disaster recovery of the Call Park application is enabled as part of the configuration and deployment of paired Front End pools.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="9b217-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="9b217-111">See Also</span></span>


[<span data-ttu-id="9b217-112">Lync Server 2013 でのコール パークの計画</span><span class="sxs-lookup"><span data-stu-id="9b217-112">Planning for Call Park in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-park.md)  
  

<span data-ttu-id="9b217-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9b217-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

