---
title: 'Lync Server 2013: Lync Server サービスを開始または停止する'
description: 'Lync Server 2013: Lync Server サービスを開始または停止する'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Start or stop Lync Server 2013 services
ms:assetid: 1c70b4ec-9de5-4f7a-a3c9-c0eb76710505
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520958(v=OCS.15)
ms:contentKeyID: 48183554
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1d6e6520cbf6fda38676beab984c2d006061b019
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423681"
---
# <a name="start-or-stop-lync-server-2013-services"></a><span data-ttu-id="63722-103">Lync Server 2013 サービスを開始または停止する</span><span class="sxs-lookup"><span data-stu-id="63722-103">Start or stop Lync Server 2013 services</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="63722-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="63722-104">

<span> </span></span></span>

<span data-ttu-id="63722-105">_**最終更新日:** 2014-02-05_</span><span class="sxs-lookup"><span data-stu-id="63722-105">_**Topic Last Modified:** 2014-02-05_</span></span>

<span data-ttu-id="63722-106">Lync Server コントロールパネルを使用すると、特定のコンピューターで実行されているすべての Lync Server 2013 サービスを開始または停止したり、特定のサービスを開始または停止することができます。</span><span class="sxs-lookup"><span data-stu-id="63722-106">You can use Lync Server Control Panel to start or stop all the Lync Server 2013 services running on a specific computer or to start or stop a specific service.</span></span>

<div>

## <a name="to-start-or-stop-all-lync-server-services-on-a-computer"></a><span data-ttu-id="63722-107">コンピューター上のすべての Lync Server サービスを開始または停止するには</span><span class="sxs-lookup"><span data-stu-id="63722-107">To start or stop all Lync Server services on a computer</span></span>

1.  <span data-ttu-id="63722-108">RTCUniversalServerAdmins グループのメンバーであるか (または同等のユーザー権限を持っている)、または CsServerAdministrator または CsAdministrator の役割に割り当てられているユーザーアカウントで、Lync Server 2013 を展開したネットワーク上のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="63722-108">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span> <span data-ttu-id="63722-109">次のようなコマンドを実行すると、CsServerAdministrator または CsAdministrator の RBAC 役割が割り当てられているかどうかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="63722-109">You can determine whether you have been assigned the CsServerAdministrator or the CsAdministrator RBAC role by running a command similar to the following:</span></span>
    
        Get-CsAdminRoleAssignment -Identity "kenmyer"

2.  <span data-ttu-id="63722-110">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="63722-110">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="63722-111">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="63722-111">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="63722-112">左側のナビゲーションバーで、[ **トポロジ** ] をクリックし、[ **状態**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="63722-112">In the left navigation bar, click **Topology** and then click **Status**.</span></span>

4.  <span data-ttu-id="63722-113">[ **状態** ] ページで、必要に応じて一覧を並べ替えて検索するか、開始または停止するサービスを実行しているコンピューターを検索して、それをクリックします。</span><span class="sxs-lookup"><span data-stu-id="63722-113">On the **Status** page, sort or search through the list as needed to find the computer that is running the services you want to start or stop, and then click it.</span></span>

5.  <span data-ttu-id="63722-114">[ **アクション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="63722-114">Click **Action**.</span></span>

6.  <span data-ttu-id="63722-115">[ **すべてのサービスの開始** ] または [ **すべてのサービスの停止**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="63722-115">Click **Start All services** or **Stop All services**.</span></span>

</div>

<div>

## <a name="to-start-or-stop-a-specific-service"></a><span data-ttu-id="63722-116">特定のサービスを開始または停止するには</span><span class="sxs-lookup"><span data-stu-id="63722-116">To start or stop a specific service</span></span>

1.  <span data-ttu-id="63722-117">CsUserAdministrator または CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="63722-117">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="63722-118">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="63722-118">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="63722-119">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="63722-119">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="63722-120">左側のナビゲーションバーで、[ **トポロジ** ] をクリックし、[ **状態**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="63722-120">In the left navigation bar, click **Topology** and then click **Status**.</span></span>

4.  <span data-ttu-id="63722-121">[ **状態** ] ページで、必要に応じて一覧を並べ替えます。または、開始または停止するサービスを実行しているコンピューターを検索して、それをクリックします。</span><span class="sxs-lookup"><span data-stu-id="63722-121">On the **Status** page, sort or search through the list as needed to find the computer that is running the service you want to start or stop, and then click it.</span></span>

5.  <span data-ttu-id="63722-122">[ **プロパティ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="63722-122">Click **Properties**.</span></span>

6.  <span data-ttu-id="63722-123">必要に応じてサービスの一覧を並べ替え、開始または停止するサービスをクリックします。</span><span class="sxs-lookup"><span data-stu-id="63722-123">Sort the list of services, if necessary, and click the service you want to start or stop.</span></span>

7.  <span data-ttu-id="63722-124">[ **アクション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="63722-124">Click **Action**.</span></span>

8.  <span data-ttu-id="63722-125">[ **サービスの開始** ] または [ **サービスの停止**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="63722-125">Click **Start service** or **Stop service**.</span></span>

9.  <span data-ttu-id="63722-126">[**閉じる**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="63722-126">Click **Close**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="63722-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="63722-127">See Also</span></span>


[<span data-ttu-id="63722-128">Lync Server 2013 でサービスのセッションを禁止する</span><span class="sxs-lookup"><span data-stu-id="63722-128">Prevent sessions for services in Lync Server 2013</span></span>](lync-server-2013-prevent-sessions-for-services.md)  


[<span data-ttu-id="63722-129">Lync Server 2013 トポロジの管理</span><span class="sxs-lookup"><span data-stu-id="63722-129">Managing the Lync Server 2013 topology</span></span>](lync-server-2013-managing-the-lync-server-topology.md)  
  

<span data-ttu-id="63722-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="63722-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

