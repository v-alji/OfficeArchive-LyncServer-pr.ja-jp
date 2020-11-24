---
title: 'Lync Server 2013: 通話管理機能の計画'
description: 'Lync Server 2013: 通話管理機能の計画。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for call management features
ms:assetid: 5f557345-5a04-45d6-b274-c02dbfe41b33
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398421(v=OCS.15)
ms:contentKeyID: 48184298
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1ec990aad40baf33365e92e78ee8071216a2add1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49397880"
---
# <a name="planning-for-call-management-features-in-lync-server-2013"></a><span data-ttu-id="18353-103">Lync Server 2013 の通話管理機能の計画</span><span class="sxs-lookup"><span data-stu-id="18353-103">Planning for call management features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="18353-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="18353-104">

<span> </span></span></span>

<span data-ttu-id="18353-105">_**最終更新日:** 2012-12-17_</span><span class="sxs-lookup"><span data-stu-id="18353-105">_**Topic Last Modified:** 2012-12-17_</span></span>

<span data-ttu-id="18353-106">エンタープライズ音声通話管理機能は、着信通話のルーティングと応答の方法を制御します。</span><span class="sxs-lookup"><span data-stu-id="18353-106">Enterprise Voice call management features control how incoming calls are routed and answered.</span></span> <span data-ttu-id="18353-107">Lync Server 2013 には、次のような通話管理機能が用意されています。</span><span class="sxs-lookup"><span data-stu-id="18353-107">Lync Server 2013 provides the following call management features:</span></span>

  - <span data-ttu-id="18353-108">**コール パーク**: VoIP ユーザーは、通話を一時的に保留し、同じ電話や別の電話で受けることができます。</span><span class="sxs-lookup"><span data-stu-id="18353-108">**Call Park**:   Enables voice users to temporarily park a call and then pick it up from the same or another phone.</span></span>

  - <span data-ttu-id="18353-109">**グループ ピックアップ**: VoIP ユーザーは、通話ピックアップ グループに割り当てられている他の VoIP ユーザーへの電話を受けることができます。</span><span class="sxs-lookup"><span data-stu-id="18353-109">**Group Pickup**:   Enables voice users to pick up calls that are ringing for other voice users who are assigned to call pickup groups.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="18353-110">グループピックアップは、Lync Server 2013 の累積更新プログラムで、2013年2月に追加されています。</span><span class="sxs-lookup"><span data-stu-id="18353-110">Group Pickup is new with Cumulative Updates for Lync Server 2013: February 2013.</span></span>

    
    </div>

  - <span data-ttu-id="18353-111">**応答グループ**: ハント グループまたは対話型音声応答 (IVR) の質問と回答を使用して、着信通話をエージェントのグループにルーティングします。</span><span class="sxs-lookup"><span data-stu-id="18353-111">**Response Group**:   Routes incoming calls to groups of agents by using hunt groups or interactive voice response (IVR) questions and answers.</span></span>

  - <span data-ttu-id="18353-112">**お知らせ:**    割り当てられていない番号への通話に対してメッセージを再生するか、通話を別の場所またはその両方にルーティングします。</span><span class="sxs-lookup"><span data-stu-id="18353-112">**Announcement:**    Plays a message for calls made to an unassigned number, or routes the call elsewhere, or both.</span></span>

<span data-ttu-id="18353-113">エンタープライズ VoIP の展開を計画している場合、これらの通話管理機能のいずれかまたはすべてを実装するように選択できます。</span><span class="sxs-lookup"><span data-stu-id="18353-113">If you plan to deploy Enterprise Voice, you can choose to implement any or all of these call management features.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="18353-114">このセクション中</span><span class="sxs-lookup"><span data-stu-id="18353-114">In This Section</span></span>

  - [<span data-ttu-id="18353-115">Lync Server 2013 でのコール パークの計画</span><span class="sxs-lookup"><span data-stu-id="18353-115">Planning for Call Park in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-park.md)

  - [<span data-ttu-id="18353-116">Lync Server 2013 でグループ通話のピックアップを計画する</span><span class="sxs-lookup"><span data-stu-id="18353-116">Planning for Group Call Pickup in Lync Server 2013</span></span>](lync-server-2013-planning-for-group-call-pickup.md)

  - [<span data-ttu-id="18353-117">Lync Server 2013 での応答グループの計画</span><span class="sxs-lookup"><span data-stu-id="18353-117">Planning for response groups in Lync Server 2013</span></span>](lync-server-2013-planning-for-response-groups.md)

  - [<span data-ttu-id="18353-118">Lync Server 2013 でのアナウンスの計画</span><span class="sxs-lookup"><span data-stu-id="18353-118">Planning for announcements in Lync Server 2013</span></span>](lync-server-2013-planning-for-announcements.md)

<span data-ttu-id="18353-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="18353-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

