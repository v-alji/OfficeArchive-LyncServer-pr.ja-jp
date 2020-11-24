---
title: 'Lync Server 2013: 通話管理機能の管理'
description: 'Lync Server 2013: 通話管理機能を管理します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing call management features
ms:assetid: c1261140-7a17-4bb2-9823-aa2cf307067c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721872(v=OCS.15)
ms:contentKeyID: 49733805
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6c51aa3174ee42047e6b6fe25a834ec832ebc889
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399123"
---
# <a name="managing-call-management-features-in-lync-server-2013"></a><span data-ttu-id="a8e74-103">Lync Server 2013 での通話管理機能の管理</span><span class="sxs-lookup"><span data-stu-id="a8e74-103">Managing call management features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a8e74-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a8e74-104">

<span> </span></span></span>

<span data-ttu-id="a8e74-105">_**最終更新日:** 2012-12-18_</span><span class="sxs-lookup"><span data-stu-id="a8e74-105">_**Topic Last Modified:** 2012-12-18_</span></span>

<span data-ttu-id="a8e74-106">エンタープライズ音声通話管理機能は、着信通話のルーティングと応答の方法を制御します。</span><span class="sxs-lookup"><span data-stu-id="a8e74-106">Enterprise Voice call management features control how incoming calls are routed and answered.</span></span> <span data-ttu-id="a8e74-107">Lync Server 2013 には、次のような通話管理機能が用意されています。</span><span class="sxs-lookup"><span data-stu-id="a8e74-107">Lync Server 2013 provides the following call management features:</span></span>

  - <span data-ttu-id="a8e74-108">**コールパーク:** 音声ユーザーが一時的に通話をパークして、同じ電話または別の電話から通話を受け取れるようにします。</span><span class="sxs-lookup"><span data-stu-id="a8e74-108">**Call Park:** Enables voice users to temporarily park a call and then pick it up from the same phone or another phone.</span></span>

  - <span data-ttu-id="a8e74-109">**グループピックアップ:** 通話の集配グループ番号にダイヤルすることで、ユーザーが他のユーザーの着信を受け取れるようにします。</span><span class="sxs-lookup"><span data-stu-id="a8e74-109">**Group Pickup:** Enables users to pick up calls that are ringing for other users by dialing a call pickup group number.</span></span>

  - <span data-ttu-id="a8e74-110">**応答グループ:** ハントグループまたはインタラクティブな音声応答 (IVR) の質問と回答を使って、着信通話をエージェントのグループにルーティングします。</span><span class="sxs-lookup"><span data-stu-id="a8e74-110">**Response Group:** Routes incoming calls to groups of agents by using hunt groups or interactive voice response (IVR) questions and answers.</span></span>

  - <span data-ttu-id="a8e74-111">**お知らせ:** 割り当てられていない番号への通話に対してメッセージを再生するか、通話を別の場所またはその両方にルーティングします。</span><span class="sxs-lookup"><span data-stu-id="a8e74-111">**Announcement:** Plays a message for calls made to an unassigned number, or routes the call elsewhere, or both.</span></span>

<span data-ttu-id="a8e74-112">このセクションでは、エンタープライズ Voip 展開でこれらの通話管理機能を管理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a8e74-112">This section describes how to manage these call management features in your Enterprise Voice deployment.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="a8e74-113">このセクション中</span><span class="sxs-lookup"><span data-stu-id="a8e74-113">In This Section</span></span>

  - [<span data-ttu-id="a8e74-114">Lync Server 2013 でのコールパークの管理</span><span class="sxs-lookup"><span data-stu-id="a8e74-114">Managing Call Park in Lync Server 2013</span></span>](lync-server-2013-managing-call-park.md)

  - [<span data-ttu-id="a8e74-115">Lync Server 2013 でグループ通話のピックアップを管理する</span><span class="sxs-lookup"><span data-stu-id="a8e74-115">Managing Group Call Pickup in Lync Server 2013</span></span>](lync-server-2013-managing-group-call-pickup.md)

  - [<span data-ttu-id="a8e74-116">Lync Server 2013 での応答グループの管理</span><span class="sxs-lookup"><span data-stu-id="a8e74-116">Managing response groups in Lync Server 2013</span></span>](lync-server-2013-managing-response-groups.md)

  - [<span data-ttu-id="a8e74-117">Lync Server 2013 で未割り当ての電話番号への通話を管理する</span><span class="sxs-lookup"><span data-stu-id="a8e74-117">Managing calls to unassigned numbers in Lync Server 2013</span></span>](lync-server-2013-managing-calls-to-unassigned-numbers.md)

<span data-ttu-id="a8e74-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a8e74-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

