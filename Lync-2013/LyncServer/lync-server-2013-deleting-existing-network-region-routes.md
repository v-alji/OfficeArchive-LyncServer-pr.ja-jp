---
title: 'Lync Server 2013: 既存のネットワーク領域ルートの削除'
description: 'Lync Server 2013: 既存のネットワーク領域ルートを削除します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting existing network region routes
ms:assetid: 6256ff80-5f1e-48b4-928b-24aeb3c1a0e7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688074(v=OCS.15)
ms:contentKeyID: 49733669
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c2501dc3f4ed88a56e9f591e3af11a673046280a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430337"
---
# <a name="deleting-existing-network-region-routes-in-lync-server-2013"></a><span data-ttu-id="820d5-103">Lync Server 2013 での既存のネットワーク領域ルートの削除</span><span class="sxs-lookup"><span data-stu-id="820d5-103">Deleting existing network region routes in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="820d5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="820d5-104">

<span> </span></span></span>

<span data-ttu-id="820d5-105">_**最終更新日:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="820d5-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="820d5-106">通話受付制御 (CAC) 構成内のすべての領域は、他のすべての領域にアクセスするための何らかの手段を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="820d5-106">Every region within a call admission control (CAC) configuration must have some way to access every other region.</span></span> <span data-ttu-id="820d5-107">地域のリンクでは、地域間の接続について帯域幅の制限を設定していますが、物理的なリンクも示しています。ルートによって、ある領域から別の領域に接続するリンク先のパスが決定されます。</span><span class="sxs-lookup"><span data-stu-id="820d5-107">While region links set bandwidth limitations on the connections between regions and also represent the physical links, a route determines which linked path the connection will traverse from one region to another.</span></span> <span data-ttu-id="820d5-108">Lync Server コントロールパネルを使用して、ネットワーク領域ルートを構成することができます。</span><span class="sxs-lookup"><span data-stu-id="820d5-108">You can use Lync Server Control Panel to configure network region routes.</span></span> <span data-ttu-id="820d5-109">Lync Server コントロールパネルでは、ネットワーク領域ルートの作成、変更、または削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="820d5-109">From Lync Server Control Panel, you can create, modify, or delete a network region route.</span></span> <span data-ttu-id="820d5-110">このトピックを使用して、既存のネットワーク領域ルートを削除します。</span><span class="sxs-lookup"><span data-stu-id="820d5-110">Use this topic to delete existing network region routes.</span></span> <span data-ttu-id="820d5-111">ネットワーク領域ルートの作成または変更の詳細については、「 [Lync Server 2013 でネットワーク領域ルートを作成または変更する](lync-server-2013-creating-or-modifying-network-region-routes.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="820d5-111">For details about creating or modifying network region routes, see [Creating or modifying network region routes in Lync Server 2013](lync-server-2013-creating-or-modifying-network-region-routes.md).</span></span>

<div>

## <a name="to-delete-a-network-region-route"></a><span data-ttu-id="820d5-112">ネットワーク領域ルートを削除するには</span><span class="sxs-lookup"><span data-stu-id="820d5-112">To delete a network region route</span></span>

1.  <span data-ttu-id="820d5-113">RTCUniversalServerAdmins グループ (または同等のユーザー権限を持つグループ) のメンバーであるユーザー アカウントまたは CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="820d5-113">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="820d5-114">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="820d5-114">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="820d5-115">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="820d5-115">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="820d5-116">左側のナビゲーションバーで [ **ネットワーク構成** ] をクリックし、[ **地域ルート**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="820d5-116">In the left navigation bar, click **Network Configuration** and then click **Region Route**.</span></span>

4.  <span data-ttu-id="820d5-117">[ **地域ルート** ] ページで、削除する地域ルートをクリックします。</span><span class="sxs-lookup"><span data-stu-id="820d5-117">On the **Region Route** page, click the region route that you want to delete.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="820d5-118">複数の地域のルートを一度に削除できます。</span><span class="sxs-lookup"><span data-stu-id="820d5-118">You can delete more than one region route at a time.</span></span> <span data-ttu-id="820d5-119">これを行うには、ctrl キーを押しながら、CTRL キーを押しながら複数の領域ルートを選択します。</span><span class="sxs-lookup"><span data-stu-id="820d5-119">To do this, press CTRL and select multiple region routes while holding down the CTRL key.</span></span> <span data-ttu-id="820d5-120">または、すべての地域ルートを選択するには、[<STRONG>編集</STRONG>] メニューの [<STRONG>すべて選択</STRONG>] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="820d5-120">Or, to select all region routes, click <STRONG>Select all</STRONG> on the <STRONG>Edit</STRONG> menu.</span></span>

    
    </div>

5.  <span data-ttu-id="820d5-121">[ **編集** ] メニューの [ **削除**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="820d5-121">On the **Edit** menu, click **Delete**.</span></span>

6.  <span data-ttu-id="820d5-122">**[OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="820d5-122">Click **OK**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="820d5-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="820d5-123">See Also</span></span>


[<span data-ttu-id="820d5-124">Lync Server 2013 でのネットワーク領域ルートの作成または変更</span><span class="sxs-lookup"><span data-stu-id="820d5-124">Creating or modifying network region routes in Lync Server 2013</span></span>](lync-server-2013-creating-or-modifying-network-region-routes.md)  


<span data-ttu-id="820d5-125">[ネットワーク地域ルートの構成](https://technet.microsoft.com/library/gg133706\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="820d5-125">[Configure a Network Region Route](https://technet.microsoft.com/library/gg133706\(v=ocs.15\))</span></span>  


[<span data-ttu-id="820d5-126">新しい (CsNetworkInterRegionRoute)</span><span class="sxs-lookup"><span data-stu-id="820d5-126">New-CsNetworkInterRegionRoute</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkInterRegionRoute)  
[<span data-ttu-id="820d5-127">設定-CsNetworkInterRegionRoute</span><span class="sxs-lookup"><span data-stu-id="820d5-127">Set-CsNetworkInterRegionRoute</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkInterRegionRoute)  
[<span data-ttu-id="820d5-128">CsNetworkInterRegionRoute の削除</span><span class="sxs-lookup"><span data-stu-id="820d5-128">Remove-CsNetworkInterRegionRoute</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkInterRegionRoute)  
[<span data-ttu-id="820d5-129">Get-CsNetworkInterRegionRoute</span><span class="sxs-lookup"><span data-stu-id="820d5-129">Get-CsNetworkInterRegionRoute</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkInterRegionRoute)  
  

<span data-ttu-id="820d5-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="820d5-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

