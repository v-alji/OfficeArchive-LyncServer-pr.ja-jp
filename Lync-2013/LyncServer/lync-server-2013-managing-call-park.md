---
title: 'Lync Server 2013: コールパークの管理'
description: 'Lync Server 2013: コールパークの管理'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing Call Park
ms:assetid: 9554cdf6-8e7c-48c8-94dd-f28e2befefdc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688140(v=OCS.15)
ms:contentKeyID: 49733740
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6540cc6d4df06b3eaadd78dce8fe01990928045a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425970"
---
# <a name="managing-call-park-in-lync-server-2013"></a><span data-ttu-id="c607b-103">Lync Server 2013 でのコールパークの管理</span><span class="sxs-lookup"><span data-stu-id="c607b-103">Managing Call Park in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c607b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c607b-104">

<span> </span></span></span>

<span data-ttu-id="c607b-105">_**最終更新日:** 2012-09-10_</span><span class="sxs-lookup"><span data-stu-id="c607b-105">_**Topic Last Modified:** 2012-09-10_</span></span>

<span data-ttu-id="c607b-106">コールパークアプリケーションを使うと、エンタープライズボイスユーザーは1つの電話から通話を保留にすることができ、その後で任意の電話から通話を受信することができます。</span><span class="sxs-lookup"><span data-stu-id="c607b-106">The Call Park application enables an Enterprise Voice user to put a call on hold from one telephone and then retrieve the call later from any telephone.</span></span> <span data-ttu-id="c607b-107">ユーザーが通話をパークすると、Lync Server は、着信が転送されるまでの一時的な電話番号に通話を *転送します*。この番号は、だれかが通話を発信するか、またはタイムアウトします。</span><span class="sxs-lookup"><span data-stu-id="c607b-107">When the user parks a call, Lync Server transfers the call to a temporary number, called an *orbit*, where the call is held until someone retrieves it or it times out.</span></span>

<span data-ttu-id="c607b-108">このセクションのトピックでは、展開でコールパークアプリケーションをカスタマイズして維持するために実行できるタスクのステップバイステップの手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="c607b-108">Topics in this section provide step-by-step procedures for tasks that you can perform to customize and maintain the Call Park application in your deployment.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="c607b-109">このセクション中</span><span class="sxs-lookup"><span data-stu-id="c607b-109">In This Section</span></span>

  - [<span data-ttu-id="c607b-110">Lync Server 2013 でのパーキング通話用の電話番号の内線番号を構成する</span><span class="sxs-lookup"><span data-stu-id="c607b-110">Configure phone number extensions for parking calls in Lync Server 2013</span></span>](lync-server-2013-configure-phone-number-extensions-for-parking-calls.md)

  - [<span data-ttu-id="c607b-111">Lync Server 2013 でのコールパーク設定の構成</span><span class="sxs-lookup"><span data-stu-id="c607b-111">Configure Call Park settings in Lync Server 2013</span></span>](lync-server-2013-configure-call-park-settings.md)

  - [<span data-ttu-id="c607b-112">通話パークをカスタマイズする Lync Server 2013 の保留中の音楽</span><span class="sxs-lookup"><span data-stu-id="c607b-112">Customize Call Park music on hold in Lync Server 2013</span></span>](lync-server-2013-customize-call-park-music-on-hold.md)

  - [<span data-ttu-id="c607b-113">Lync Server 2013 での障害復旧時のコール パークの管理</span><span class="sxs-lookup"><span data-stu-id="c607b-113">Manage Call Park during disaster recovery in Lync Server 2013</span></span>](lync-server-2013-manage-call-park-during-disaster-recovery.md)

<span data-ttu-id="c607b-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c607b-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

