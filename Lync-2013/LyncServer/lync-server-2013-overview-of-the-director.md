---
title: 'Lync Server 2013: ディレクターの概要'
description: 'Lync Server 2013: ディレクターの概要。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of the Director
ms:assetid: cf9919b3-e16b-47c5-be1d-2c4bc64f44ea
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398879(v=OCS.15)
ms:contentKeyID: 48185393
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6686534e22bab5b02a2663789298e4cf7ea582c2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424710"
---
# <a name="overview-of-the-director-in-lync-server-2013"></a><span data-ttu-id="a1345-103">Lync Server 2013 のディレクターの概要</span><span class="sxs-lookup"><span data-stu-id="a1345-103">Overview of the Director in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a1345-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a1345-104">

<span> </span></span></span>

<span data-ttu-id="a1345-105">_**最終更新日:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="a1345-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="a1345-106">ディレクターは、Lync Server 2013 を実行しているサーバーで、ユーザー要求は認証されますが、ユーザーアカウントのホームにはなりません。</span><span class="sxs-lookup"><span data-stu-id="a1345-106">A Director is a server running Lync Server 2013 that authenticates user requests, but does not home any user accounts.</span></span> <span data-ttu-id="a1345-107">次の2つのシナリオでは、必要に応じてディレクターを展開できます。</span><span class="sxs-lookup"><span data-stu-id="a1345-107">You optionally can deploy a Director in the following two scenarios:</span></span>

  - <span data-ttu-id="a1345-108">エッジサーバーを展開して外部ユーザーからのアクセスを有効にする場合は、ディレクターも展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a1345-108">If you enable access by external users by deploying Edge Servers, you should also deploy a Director.</span></span> <span data-ttu-id="a1345-109">このシナリオでは、ディレクターが外部ユーザーを認証し、そのトラフィックを内部サーバーに渡します。</span><span class="sxs-lookup"><span data-stu-id="a1345-109">In this scenario, the Director authenticates the external users, and then passes their traffic on to internal servers.</span></span> <span data-ttu-id="a1345-110">ディレクターを使用して外部ユーザーを認証すると、フロントエンドプールサーバーは、これらのユーザーの認証を実行するオーバーヘッドから解放されます。</span><span class="sxs-lookup"><span data-stu-id="a1345-110">When a Director is used to authenticate external users, it relieves Front End pool servers from the overhead of performing authentication of these users.</span></span> <span data-ttu-id="a1345-111">また、サービス拒否攻撃などの悪意のあるトラフィックから、内部のフロントエンドプールを分離することもできます。</span><span class="sxs-lookup"><span data-stu-id="a1345-111">It also helps insulate internal Front End pools from malicious traffic such as denial-of-service attacks.</span></span> <span data-ttu-id="a1345-112">このような攻撃で無効な外部トラフィックがネットワークにあふれている場合、このトラフィックはディレクターで終了します。</span><span class="sxs-lookup"><span data-stu-id="a1345-112">If the network is flooded with invalid external traffic in such an attack, this traffic ends at the Director.</span></span>

  - <span data-ttu-id="a1345-113">セントラルサイトに複数のフロントエンドプールを展開している場合、そのサイトにディレクターを追加すると、認証要求が簡素化され、パフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="a1345-113">If you deploy multiple Front End pools at a central site, by adding a Director to that site you can streamline authentication requests and improve performance.</span></span> <span data-ttu-id="a1345-114">このシナリオでは、すべての要求が最初にディレクターに送られ、適切なフロントエンドプールに転送されます。</span><span class="sxs-lookup"><span data-stu-id="a1345-114">In this scenario, all requests go first to the Director, which then routes them to the correct Front End pool.</span></span>

<span data-ttu-id="a1345-115"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a1345-115"></div>

<span> </span>

</div>

</div>

</span></span></div>

