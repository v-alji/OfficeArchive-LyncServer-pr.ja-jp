---
title: 共存の考慮事項
description: 共存の考慮事項。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Coexistence considerations
ms:assetid: 9d1a3c0f-492a-4e37-bc2f-63509e328785
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205131(v=OCS.15)
ms:contentKeyID: 48184990
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fd1f9525b37bdee3249e0e47352fdea1bc7f012f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399182"
---
# <a name="coexistence-considerations"></a><span data-ttu-id="4e698-103">共存の考慮事項</span><span class="sxs-lookup"><span data-stu-id="4e698-103">Coexistence considerations</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4e698-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4e698-104">

<span> </span></span></span>

<span data-ttu-id="4e698-105">_**最終更新日:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="4e698-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="4e698-106">移行後、Lync Server 2013、常設チャットサーバープールのみが存在し、従来の展開を廃止することができます。</span><span class="sxs-lookup"><span data-stu-id="4e698-106">After migration, only a Lync Server 2013, Persistent Chat Server pool will exist, and you can decommission your legacy deployment.</span></span>

<span data-ttu-id="4e698-107">移行が完了する前に、現在のグループチャットサーバーの展開を完全に解除する前に、次のいずれかの展開を使用している可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4e698-107">Before migration completes and before you have decommissioned your current Group Chat Server deployment completely, you may have any of the following deployments:</span></span>

  - <span data-ttu-id="4e698-108">Lync server 2013 の常設チャットサーバープール。 Lync Server 2013 プールに所属している必要があります。</span><span class="sxs-lookup"><span data-stu-id="4e698-108">Lync Server 2013, Persistent Chat Server pool, which must be homed on a Lync Server 2013 pool.</span></span>

  - <span data-ttu-id="4e698-109">Lync server 2010、グループチャットプール (Lync Server 2010 プールに所属している必要があります)。</span><span class="sxs-lookup"><span data-stu-id="4e698-109">Lync Server 2010, Group Chat pool, which must be homed on a Lync Server 2010 pool.</span></span>

  - <span data-ttu-id="4e698-110">Office Communications Server 2007 R2 グループチャットプール。これは、Office Communications Server 2007 R2 プールに所属している必要があります。</span><span class="sxs-lookup"><span data-stu-id="4e698-110">Office Communications Server 2007 R2 Group Chat pool, which must be homed on an Office Communications Server 2007 R2 pool.</span></span>

<span data-ttu-id="4e698-111">これらの展開は、並行して行うことができます。</span><span class="sxs-lookup"><span data-stu-id="4e698-111">These deployments can exist side by side.</span></span> <span data-ttu-id="4e698-112">ただし、1つの展開に含まれているカテゴリ、ルーム、アドインは、関連付けられている展開では操作できません。</span><span class="sxs-lookup"><span data-stu-id="4e698-112">However the categories, rooms, and add-ins in one deployment do not interact with those in the accompanying deployment.</span></span>

<span data-ttu-id="4e698-113">手動構成を使用すると、レガシクライアント (グループチャットクライアント) は、Office Communications Server 2007 R2、Lync Server 2010、グループチャット、または Lync Server 2013 で、一度に1つのプールに接続できます。</span><span class="sxs-lookup"><span data-stu-id="4e698-113">Using manual configuration, a legacy client (Group Chat client) can connect to one pool at a time for Office Communications Server 2007 R2, Lync Server 2010, Group Chat, or Lync Server 2013.</span></span>

<span data-ttu-id="4e698-114">Lync 2013 (クライアント) は、従来のグループチャットサーバープールではなく、Lync Server 2013、常設チャットサーバープールのみで操作できます。</span><span class="sxs-lookup"><span data-stu-id="4e698-114">The Lync 2013 (client) can interact only with the Lync Server 2013, Persistent Chat Server pool, not with legacy Group Chat Server pools.</span></span> <span data-ttu-id="4e698-115">Lync 2013 (クライアント) で常設チャットを使用するには、ユーザーが Lync 2013 を使っていて、ポリシーによって有効になっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="4e698-115">To use Persistent Chat in a Lync 2013 (client), the user must be homed on Lync 2013 and enabled by policy.</span></span>

<span data-ttu-id="4e698-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4e698-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

