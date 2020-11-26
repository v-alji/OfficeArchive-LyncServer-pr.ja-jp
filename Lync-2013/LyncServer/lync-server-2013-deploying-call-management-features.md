---
title: 'Lync Server 2013: 通話管理機能の展開'
description: 'Lync Server 2013: 通話管理機能の展開。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying call management features
ms:assetid: 1667cfe4-76fa-4e10-91bb-b3efbedbf759
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204706(v=OCS.15)
ms:contentKeyID: 48183504
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: aa89b75dbcae9de1069daf99986076b66e0411cc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430071"
---
# <a name="deploying-call-management-features-in-lync-server-2013"></a><span data-ttu-id="e731b-103">Lync Server 2013 での通話管理機能の展開</span><span class="sxs-lookup"><span data-stu-id="e731b-103">Deploying call management features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e731b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e731b-104">

<span> </span></span></span>

<span data-ttu-id="e731b-105">_**最終更新日:** 2012-12-18_</span><span class="sxs-lookup"><span data-stu-id="e731b-105">_**Topic Last Modified:** 2012-12-18_</span></span>

<span data-ttu-id="e731b-106">エンタープライズ音声通話管理機能は、着信通話のルーティングと応答の方法を制御します。</span><span class="sxs-lookup"><span data-stu-id="e731b-106">Enterprise Voice call management features control how incoming calls are routed and answered.</span></span> <span data-ttu-id="e731b-107">Lync Server 2013 には、次のような通話管理機能が用意されています。</span><span class="sxs-lookup"><span data-stu-id="e731b-107">Lync Server 2013 provides the following call management features:</span></span>

  - <span data-ttu-id="e731b-108">**コールパーク:** 音声ユーザーが一時的に通話をパークして、同じ電話または別の電話から通話を受け取れるようにします。</span><span class="sxs-lookup"><span data-stu-id="e731b-108">**Call Park:** Enables voice users to temporarily park a call and then pick it up from the same phone or another phone.</span></span>

  - <span data-ttu-id="e731b-109">**グループピックアップ:** 通話のピックアップグループ番号をダイヤルすることによって、ピックアップグループに割り当てられている別のユーザーに対して発信された通話に応答することができます。</span><span class="sxs-lookup"><span data-stu-id="e731b-109">**Group Pickup:** Enables users to answer calls made to another user who is assigned to a pickup group by dialing the call pickup group number.</span></span>

  - <span data-ttu-id="e731b-110">**応答グループ:** ハントグループまたはインタラクティブな音声応答 (IVR) の質問と回答を使って、着信通話をエージェントのグループにルーティングします。</span><span class="sxs-lookup"><span data-stu-id="e731b-110">**Response Group:** Routes incoming calls to groups of agents by using hunt groups or interactive voice response (IVR) questions and answers.</span></span>

  - <span data-ttu-id="e731b-111">**お知らせ:** 割り当てられていない番号への通話に対してメッセージを再生するか、通話を別の場所またはその両方にルーティングします。</span><span class="sxs-lookup"><span data-stu-id="e731b-111">**Announcement:** Plays a message for calls made to an unassigned number, or routes the call elsewhere, or both.</span></span>

<span data-ttu-id="e731b-112">このセクションでは、エンタープライズ Voip の展開時にこれらの通話管理機能を構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e731b-112">This section describes how to configure these call management features during an Enterprise Voice deployment.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="e731b-113">このセクション中</span><span class="sxs-lookup"><span data-stu-id="e731b-113">In This Section</span></span>

  - [<span data-ttu-id="e731b-114">Lync Server 2013 でのコール パークの構成</span><span class="sxs-lookup"><span data-stu-id="e731b-114">Configuring Call Park in Lync Server 2013</span></span>](lync-server-2013-configuring-call-park.md)

  - [<span data-ttu-id="e731b-115">Lync Server 2013 でグループ通話のピックアップを構成する</span><span class="sxs-lookup"><span data-stu-id="e731b-115">Configuring Group Call Pickup in Lync Server 2013</span></span>](lync-server-2013-configuring-group-call-pickup.md)

  - [<span data-ttu-id="e731b-116">Lync Server 2013 での応答グループの構成</span><span class="sxs-lookup"><span data-stu-id="e731b-116">Configuring Response Group in Lync Server 2013</span></span>](lync-server-2013-configuring-response-group.md)

  - [<span data-ttu-id="e731b-117">Lync Server 2013 での、割り当てられていない番号用のアナウンスの構成</span><span class="sxs-lookup"><span data-stu-id="e731b-117">Configuring announcements for unassigned numbers in Lync Server 2013</span></span>](lync-server-2013-configuring-announcements-for-unassigned-numbers.md)

<span data-ttu-id="e731b-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e731b-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

