---
title: 'Lync Server 2013: 応答グループのエージェント グループの作成'
description: 'Lync Server 2013: 応答グループエージェントグループを作成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create Response Group agent groups
ms:assetid: 2a80de17-ead0-46e8-8a27-7a4e233dbde0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520969(v=OCS.15)
ms:contentKeyID: 48183688
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a9420ee5f6fbd4b995c8542b848ef30f53e46fc4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431618"
---
# <a name="create-response-group-agent-groups-lync-server-2013"></a><span data-ttu-id="1302a-103">Lync Server 2013 での応答グループのエージェント グループの作成</span><span class="sxs-lookup"><span data-stu-id="1302a-103">Create Response Group agent groups Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1302a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1302a-104">

<span> </span></span></span>

<span data-ttu-id="1302a-105">_**最終更新日:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="1302a-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="1302a-106">エージェント グループを作成するときは、そのグループに割り当てるエージェントを選択し、詳細なグループ設定 (ルーティング方法、グループに対するエージェントの権限など) を指定します。</span><span class="sxs-lookup"><span data-stu-id="1302a-106">When you create an agent group, you select the agents that are assigned to the group and specify additional group settings, such as the routing method and whether an agent can sign in to and out of the group.</span></span>

<span data-ttu-id="1302a-107">グループからサインアウトする必要があるエージェントは、Lync Server のサインインまたはサインアウトとは異なり、 *正式なエージェント* と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="1302a-107">An agent who must sign in and out of the group, which is different from signing in or out of Lync Server, is called a *formal agent*.</span></span> <span data-ttu-id="1302a-108">公式エージェントが、グループにルーティングされた着信を受信するには、そのグループにサインインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1302a-108">Formal agents must be signed in to the group before they can receive calls routed to the group.</span></span> <span data-ttu-id="1302a-109">これは、パートタイム ベースでグループから通話に応答するエージェントには便利な方法です。</span><span class="sxs-lookup"><span data-stu-id="1302a-109">This can be useful for agents who answer calls from the group on a part-time basis.</span></span> <span data-ttu-id="1302a-110">正式なエージェントは、Lync 2013 のメニュー項目をクリックして、Windows Internet Explorer のインターネットブラウザーを開き、web ページ本体を表示することによって、グループにサインインおよびサインアウトします。</span><span class="sxs-lookup"><span data-stu-id="1302a-110">Formal agents sign in and out of their groups by clicking a menu item in Lync 2013 to open the Windows Internet Explorer Internet browser and display a webpage console.</span></span>

<span data-ttu-id="1302a-111">グループにサインインしていないか、グループからサインアウトしていないエージェントは、" *非公式のエージェント*" と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="1302a-111">An agent who does not sign in or out of the group is called an *informal agent*.</span></span> <span data-ttu-id="1302a-112">非公式のエージェントは、Lync Server へのサインイン時にグループに自動的にサインインされ、グループからサインアウトすることはできません。</span><span class="sxs-lookup"><span data-stu-id="1302a-112">Informal agents are automatically signed in to the group when they sign in to Lync Server, and they cannot sign out of the group.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="1302a-113">エージェントにできるのは社内ユーザーのみです。</span><span class="sxs-lookup"><span data-stu-id="1302a-113">Only on-premises users can be agents.</span></span> <span data-ttu-id="1302a-114">エージェントがオンプレミスからオンラインに移行された場合、応答グループの呼び出しはそのエージェントにルーティングされません。</span><span class="sxs-lookup"><span data-stu-id="1302a-114">If an agent is moved from on-premises to online, Response Group calls will not be routed to that agent.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="1302a-115">このセクション中</span><span class="sxs-lookup"><span data-stu-id="1302a-115">In This Section</span></span>

[<span data-ttu-id="1302a-116">Lync Server 2013 でエージェントグループを作成または変更する</span><span class="sxs-lookup"><span data-stu-id="1302a-116">Create or modify an agent group in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-an-agent-group.md)

<span data-ttu-id="1302a-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1302a-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

