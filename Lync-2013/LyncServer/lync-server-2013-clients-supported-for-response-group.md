---
title: 'Lync Server 2013: 応答グループに対してサポートされるクライアント'
description: 'Lync Server 2013: 応答グループでサポートされているクライアント。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Clients supported for Response Group
ms:assetid: 84911025-e754-41a8-ba48-e31c058fc557
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398674(v=OCS.15)
ms:contentKeyID: 48184705
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 898f8e0d7493952a46205d919b5c6b546f14a30d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434768"
---
# <a name="clients-supported-for-response-group-in-lync-server-2013"></a><span data-ttu-id="1f74f-103">Lync Server 2013 の応答グループに対してサポートされるクライアント</span><span class="sxs-lookup"><span data-stu-id="1f74f-103">Clients supported for Response Group in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1f74f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1f74f-104">

<span> </span></span></span>

<span data-ttu-id="1f74f-105">_**最終更新日:** 2014-03-28_</span><span class="sxs-lookup"><span data-stu-id="1f74f-105">_**Topic Last Modified:** 2014-03-28_</span></span>

<span data-ttu-id="1f74f-106">応答グループのアプリケーションでは、次のクライアントがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="1f74f-106">The Response Group application supports the following clients:</span></span>

  - <span data-ttu-id="1f74f-107">Lync 2013 デスクトップクライアント</span><span class="sxs-lookup"><span data-stu-id="1f74f-107">Lync 2013 desktop client</span></span>

  - <span data-ttu-id="1f74f-108">Lync 2010 デスクトップクライアント</span><span class="sxs-lookup"><span data-stu-id="1f74f-108">Lync 2010 desktop client</span></span>

  - <span data-ttu-id="1f74f-109">Lync 2010 Attendant</span><span class="sxs-lookup"><span data-stu-id="1f74f-109">Lync 2010 Attendant</span></span>

  - <span data-ttu-id="1f74f-110">Office Communications Server 2007 R2 Attendant</span><span class="sxs-lookup"><span data-stu-id="1f74f-110">Office Communications Server 2007 R2 Attendant</span></span>

  - <span data-ttu-id="1f74f-111">Lync Phone Edition</span><span class="sxs-lookup"><span data-stu-id="1f74f-111">Lync Phone Edition</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="1f74f-112">応答グループアプリケーションは、Lync モバイルクライアントではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="1f74f-112">The Response Group application is not supported on Lync mobile clients.</span></span>



</div>

<span data-ttu-id="1f74f-113">新機能の詳細については、「はじめに」のドキュメントで「 [Lync Server 2013 の新しい応答グループアプリケーションの機能](lync-server-2013-new-response-group-application-features.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1f74f-113">For details about new features, see [New Response Group application features in Lync Server 2013](lync-server-2013-new-response-group-application-features.md) in the Getting Started documentation.</span></span>

<span data-ttu-id="1f74f-114">使用できる特定のクライアントは、応答グループのユーザーの種類によって異なります。</span><span class="sxs-lookup"><span data-stu-id="1f74f-114">The specific client that you can use depends on the type of Response Group user that you are:</span></span>

  - <span data-ttu-id="1f74f-115">**発信者** は、先にリストされたクライアントのいずれかを使用するか、または公衆交換電話網 (PSTN) 経由で標準的な電話機を使用して、応答グループを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="1f74f-115">**Callers** can call a response group by using any of the clients listed previously, and by using a standard telephone over the public switched telephone network (PSTN).</span></span>

  - <span data-ttu-id="1f74f-116">**非公式のエージェント** (グループにサインインして通話に応答しないエージェント) は、アテンダント、Lync、Lync Phone Edition を使用して通話を受けることができます。</span><span class="sxs-lookup"><span data-stu-id="1f74f-116">**Informal agents** (agents who do not sign into and out of their groups to accept calls) can accept calls by using Attendant, Lync, or Lync Phone Edition.</span></span> <span data-ttu-id="1f74f-117">非公式のエージェントは、これらのクライアントのいずれかを使って Lync Server 2013 にサインインしたときに、自動的にグループにサインインされます。</span><span class="sxs-lookup"><span data-stu-id="1f74f-117">Informal agents are automatically signed into their groups when they sign in to Lync Server 2013 by using one of these clients.</span></span>

  - <span data-ttu-id="1f74f-118">**正式なエージェント** (通話を許可するためにグループにサインインまたはサインアウトする必要があるエージェント) は、Lync 2013 を使用して、メニュー項目からエージェントコンソールにアクセスするか、または応答を使って、Internet Explorer から直接エージェントコンソールにアクセスすることで、通話を受けることができます。</span><span class="sxs-lookup"><span data-stu-id="1f74f-118">**Formal agents** (agents who must sign into and out of their groups to accept calls) can accept calls by using Lync 2013 and accessing the agent console from the menu item, or by using Attendant and accessing the agent console directly from Internet Explorer.</span></span>

<span data-ttu-id="1f74f-119"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1f74f-119"></div>

<span> </span>

</div>

</div>

</span></span></div>

