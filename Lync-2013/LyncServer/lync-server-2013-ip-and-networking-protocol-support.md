---
title: 'Lync Server 2013: IP とネットワーク プロトコルのサポート'
description: 'Lync Server 2013: IP およびネットワークプロトコルのサポート。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: IP and networking protocol support
ms:assetid: b0cffb10-3478-445c-89c7-8cb8b5027424
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412848(v=OCS.15)
ms:contentKeyID: 48185128
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dbd8022dd7197524334e0c70ea0ad875a30446de
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426747"
---
# <a name="ip-and-networking-protocol-support-in-lync-server-2013"></a><span data-ttu-id="e01fc-103">Lync Server 2013 での IP とネットワーク プロトコルのサポート</span><span class="sxs-lookup"><span data-stu-id="e01fc-103">IP and networking protocol support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e01fc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e01fc-104">

<span> </span></span></span>

<span data-ttu-id="e01fc-105">_**最終更新日:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="e01fc-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="e01fc-106">Lync Server 2013 は、次の IP およびネットワークプロトコルをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="e01fc-106">Lync Server 2013 supports the following IP and networking protocols:</span></span>

  - <span data-ttu-id="e01fc-107">**IP プロトコル。**</span><span class="sxs-lookup"><span data-stu-id="e01fc-107">**IP Protocols.**</span></span>   <span data-ttu-id="e01fc-108">Lync Server 2013 では、サーバーネットワークの IP バージョン 4 (IPv4) または IP version 6 (IPv6) がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="e01fc-108">Lync Server 2013 supports either IP version 4 (IPv4) or IP version 6 (IPv6) for the server network.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="e01fc-109">Lync Server 2013 は、デュアル IP スタックが有効になっているネットワークで機能することができます。</span><span class="sxs-lookup"><span data-stu-id="e01fc-109">Lync Server 2013 can function in a network with dual IP stack enabled.</span></span>

    
    </div>

  - <span data-ttu-id="e01fc-110">**SIP トランスポートプロトコル。**</span><span class="sxs-lookup"><span data-stu-id="e01fc-110">**SIP Transport Protocols.**</span></span>   <span data-ttu-id="e01fc-111">一般的に、SIP では、ユーザーデータグラムプロトコル (UDP)、伝送制御プロトコル (TCP)、トランスポート層セキュリティ (TLS) の3つ以上のトランスポートタイプを使うことができます。</span><span class="sxs-lookup"><span data-stu-id="e01fc-111">Generically, SIP can use at least three transport types: User Datagram Protocol (UDP), Transmission Control Protocol (TCP), and Transport Layer Security (TLS).</span></span> <span data-ttu-id="e01fc-112">既定の SIP トランスポート構成では、TLS は TCP 経由で実行されます。</span><span class="sxs-lookup"><span data-stu-id="e01fc-112">In the default SIP transport configuration, TLS runs over TCP.</span></span> <span data-ttu-id="e01fc-113">TLS は Lync Server 2013 ネットワーク内で使用されます。</span><span class="sxs-lookup"><span data-stu-id="e01fc-113">TLS is used within the Lync Server 2013 network.</span></span> <span data-ttu-id="e01fc-114">ネットワークの端では、Lync Server 2013 は TCP 経由で相互運用できます。</span><span class="sxs-lookup"><span data-stu-id="e01fc-114">At the edge of the network, Lync Server 2013 can interoperate over TCP.</span></span> <span data-ttu-id="e01fc-115">Lync Server 2013 では、エンタープライズ通信のセキュリティ、信頼性、スケーラビリティに関する最小標準を満たしていないため、SIP トランスポートの UDP はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="e01fc-115">Lync Server 2013 does not support UDP for SIP transport because it doesn’t meet the minimum standards for enterprise communications security, reliability, and scalability.</span></span> <span data-ttu-id="e01fc-116">詳細については、「NextHop のブログ記事「udp について」または「UDP ではなく」を参照してください [https://go.microsoft.com/fwlink/p/?linkId=185369](https://go.microsoft.com/fwlink/p/?linkid=185369) 。</span><span class="sxs-lookup"><span data-stu-id="e01fc-116">For details, see the NextHop blog article, "To UDP, or not to UDP, that is the question," at [https://go.microsoft.com/fwlink/p/?linkId=185369](https://go.microsoft.com/fwlink/p/?linkid=185369).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="e01fc-117">各ブログの内容と URL は、将来予告なしに変更されることがあります。</span><span class="sxs-lookup"><span data-stu-id="e01fc-117">The content of each blog and its URL are subject to change without notice.</span></span>

    
    <span data-ttu-id="e01fc-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e01fc-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

