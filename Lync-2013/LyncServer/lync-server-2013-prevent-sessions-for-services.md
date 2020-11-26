---
title: 'Lync Server 2013: サービスのセッションを禁止する'
description: 'Lync Server 2013: サービスのセッションを禁止する。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Prevent sessions for services
ms:assetid: 977dcc5c-2aac-48ef-86a1-a8d47b4d9e74
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182553(v=OCS.15)
ms:contentKeyID: 48184866
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 846a9da5330c3e64f61c27dfadd883f0c43a0ffa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436903"
---
# <a name="prevent-sessions-for-services-in-lync-server-2013"></a><span data-ttu-id="a9171-103">Lync Server 2013 でサービスのセッションを禁止する</span><span class="sxs-lookup"><span data-stu-id="a9171-103">Prevent sessions for services in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a9171-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a9171-104">

<span> </span></span></span>

<span data-ttu-id="a9171-105">_**最終更新日:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="a9171-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="a9171-106">Lync Server コントロールパネルを使用すると、特定のコンピューターで実行されているすべての Lync Server 2013 サービスの新しいセッションを禁止したり、特定の Lync Server 2013 サービスの新しいセッションを禁止したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="a9171-106">You can use Lync Server Control Panel to prevent new sessions for all the Lync Server 2013 services running on a specific computer or to prevent new sessions for a specific Lync Server 2013 service.</span></span>

<div>

## <a name="to-prevent-new-sessions-for-all-lync-server-services-on-a-computer"></a><span data-ttu-id="a9171-107">コンピューター上のすべての Lync Server サービスの新しいセッションを禁止するには</span><span class="sxs-lookup"><span data-stu-id="a9171-107">To prevent new sessions for all Lync Server services on a computer</span></span>

1.  <span data-ttu-id="a9171-108">RTCUniversalServerAdmins グループのメンバーであるか (または同等のユーザー権限を持っている)、または CsServerAdministrator または CsAdministrator の役割に割り当てられているユーザーアカウントで、Lync Server 2013 を展開したネットワーク上のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="a9171-108">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="a9171-109">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="a9171-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="a9171-110">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="a9171-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="a9171-111">左側のナビゲーションバーで、[ **トポロジ** ] をクリックし、[ **状態**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a9171-111">In the left navigation bar, click **Topology** and then click **Status**.</span></span>

4.  <span data-ttu-id="a9171-112">[ **状態** ] ページで、必要に応じて一覧を並べ替えます。または、新しいセッションを禁止するサービスを実行しているコンピューターを検索して、それをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a9171-112">On the **Status** page, sort or search through the list as needed to find the computer that is running the services for which you want to prevent new sessions, and then click it.</span></span>

5.  <span data-ttu-id="a9171-113">[ **アクション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a9171-113">Click **Action**.</span></span>

6.  <span data-ttu-id="a9171-114">[ **すべてのサービスに対して新規セッションを** 許可しない] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a9171-114">Click **Prevent new sessions for all services**.</span></span>

</div>

<div>

## <a name="to-prevent-new-sessions-for-a-specific-service"></a><span data-ttu-id="a9171-115">特定のサービスの新しいセッションを禁止するには</span><span class="sxs-lookup"><span data-stu-id="a9171-115">To prevent new sessions for a specific service</span></span>

1.  <span data-ttu-id="a9171-116">RTCUniversalServerAdmins グループのメンバーであるか (または同等のユーザー権限を持っている)、または CsServerAdministrator または CsAdministrator の役割に割り当てられているユーザーアカウントで、Lync Server 2013 を展開したネットワーク上のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="a9171-116">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="a9171-117">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="a9171-117">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="a9171-118">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="a9171-118">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="a9171-119">左側のナビゲーションバーで、[ **トポロジ** ] をクリックし、[ **状態**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a9171-119">In the left navigation bar, click **Topology** and then click **Status**.</span></span>

4.  <span data-ttu-id="a9171-120">[ **状態** ] ページで、必要に応じて一覧を並べ替えます。または、開始または停止するサービスを実行しているコンピューターを検索して、それをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a9171-120">On the **Status** page, sort or search through the list as needed to find the computer that is running the service you want to start or stop, and then click it.</span></span>

5.  <span data-ttu-id="a9171-121">[ **プロパティ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a9171-121">Click **Properties**.</span></span>

6.  <span data-ttu-id="a9171-122">必要に応じてサービスの一覧を並べ替えて、新しいセッションを禁止するサービスをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a9171-122">Sort the list of services, if necessary, and click the service for which you want to prevent new sessions.</span></span>

7.  <span data-ttu-id="a9171-123">[ **アクション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a9171-123">Click **Action**.</span></span>

8.  <span data-ttu-id="a9171-124">[ **サービスの新規セッションを** 許可しない] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a9171-124">Click **Prevent new sessions for service**.</span></span>

9.  <span data-ttu-id="a9171-125">[**閉じる**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a9171-125">Click **Close**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="a9171-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="a9171-126">See Also</span></span>


[<span data-ttu-id="a9171-127">Lync Server 2013 トポロジの管理</span><span class="sxs-lookup"><span data-stu-id="a9171-127">Managing the Lync Server 2013 topology</span></span>](lync-server-2013-managing-the-lync-server-topology.md)  
  

<span data-ttu-id="a9171-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a9171-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

