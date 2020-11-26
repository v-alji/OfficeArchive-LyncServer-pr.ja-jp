---
title: 'Lync Server 2013: 常設チャット サーバーのフェールオーバーとフェールバック'
description: 'Lync Server 2013: 常設チャットサーバーのフェイルオーバーとフェイルバック'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failing over and failing back Persistent Chat Server
ms:assetid: bc9a791f-d15c-48c8-8682-1a8ad19d8c75
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205214(v=OCS.15)
ms:contentKeyID: 48185259
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a86a9f809a853d48103a8c50a04773e4625a2b8a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428259"
---
# <a name="failing-over-and-failing-back-persistent-chat-server-in-lync-server-2013"></a><span data-ttu-id="5d5e0-103">Lync Server 2013 での常設チャット サーバーのフェールオーバーとフェールバック</span><span class="sxs-lookup"><span data-stu-id="5d5e0-103">Failing over and failing back Persistent Chat Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5d5e0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5d5e0-104">

<span> </span></span></span>

<span data-ttu-id="5d5e0-105">_**最終更新日:** 2012-08-03_</span><span class="sxs-lookup"><span data-stu-id="5d5e0-105">_**Topic Last Modified:** 2012-08-03_</span></span>

<span data-ttu-id="5d5e0-106">Lync Server 2013 の常設チャットサーバーにフェールオーバーしてフェールバックするには、Microsoft SQL Server 2008 R2 以降のレプリケーションとフェールオーバープロセスについて理解している必要があります。</span><span class="sxs-lookup"><span data-stu-id="5d5e0-106">To fail over and fail back Lync Server 2013, Persistent Chat Server, you should be familiar with replication and failover processes for Microsoft SQL Server 2008 R2 and later.</span></span> <span data-ttu-id="5d5e0-107">また、常設チャットサーバーサービスについても理解している必要があります。</span><span class="sxs-lookup"><span data-stu-id="5d5e0-107">You should also be familiar with the Persistent Chat Server services.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="5d5e0-108">このセクション中</span><span class="sxs-lookup"><span data-stu-id="5d5e0-108">In This Section</span></span>

  - [<span data-ttu-id="5d5e0-109">Lync Server 2013 での常設チャット サーバーのフェールオーバー</span><span class="sxs-lookup"><span data-stu-id="5d5e0-109">Failing over Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-failing-over-persistent-chat-server.md)

  - [<span data-ttu-id="5d5e0-110">Lync Server 2013 常設チャット サーバーのフェールバック</span><span class="sxs-lookup"><span data-stu-id="5d5e0-110">Failing back Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-failing-back-persistent-chat-server.md)

<span data-ttu-id="5d5e0-111"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5d5e0-111"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

