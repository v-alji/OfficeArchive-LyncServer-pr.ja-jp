---
title: 'Lync Server 2013: ネットワーク領域の作成または変更'
description: 'Lync Server 2013: ネットワークの領域を作成または変更します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Creating or modifying network regions
ms:assetid: bd08bb66-5976-4ece-b45c-7de19569f814
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182579(v=OCS.15)
ms:contentKeyID: 48185266
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1b02a041272f0df27d2133ca26096caeb01816c7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431415"
---
# <a name="creating-or-modifying-network-regions-in-lync-server-2013"></a><span data-ttu-id="0ee10-103">Lync Server 2013 でのネットワーク領域の作成または変更</span><span class="sxs-lookup"><span data-stu-id="0ee10-103">Creating or modifying network regions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0ee10-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0ee10-104">

<span> </span></span></span>

<span data-ttu-id="0ee10-105">_**最終更新日:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="0ee10-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="0ee10-106">ネットワーク領域は、ネットワークのさまざまな部分を複数の地域で相互接続します。</span><span class="sxs-lookup"><span data-stu-id="0ee10-106">A network region interconnects various parts of a network across multiple geographic areas.</span></span> <span data-ttu-id="0ee10-107">すべてのネットワーク領域はセントラルサイトと関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ee10-107">Every network region must be associated with a central site.</span></span> <span data-ttu-id="0ee10-108">セントラルサイトは、通話受付制御 (CAC) 帯域幅ポリシーサービスが実行されているデータセンターサイトです。</span><span class="sxs-lookup"><span data-stu-id="0ee10-108">The central site is the data center site on which the call admission control (CAC) bandwidth policy service is running.</span></span> <span data-ttu-id="0ee10-109">Lync Server コントロールパネルを使用して、ネットワークの領域を構成することができます。</span><span class="sxs-lookup"><span data-stu-id="0ee10-109">You can use Lync Server Control Panel to configure network regions.</span></span> <span data-ttu-id="0ee10-110">[ネットワーク] 領域には、インターネット経由の代替パスが音声とビデオに接続できるかどうかを決定する設定が含まれます。</span><span class="sxs-lookup"><span data-stu-id="0ee10-110">Network regions include settings that determine whether alternate paths through the Internet are allowed for audio and video connections.</span></span> <span data-ttu-id="0ee10-111">Lync Server コントロールパネルから、ネットワークの領域を作成、変更、または削除することができます。</span><span class="sxs-lookup"><span data-stu-id="0ee10-111">From the Lync Server Control Panel, you can create, modify, or delete a network region.</span></span> <span data-ttu-id="0ee10-112">このトピックは、ネットワーク領域の作成と変更に使用します。</span><span class="sxs-lookup"><span data-stu-id="0ee10-112">Use this topic to create and modify network regions.</span></span> <span data-ttu-id="0ee10-113">既存のネットワーク領域の削除の詳細については、「 [Lync Server 2013 で既存のネットワーク領域を削除](lync-server-2013-deleting-existing-network-regions.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0ee10-113">For details about deleting existing network regions, see [Deleting existing network regions in Lync Server 2013](lync-server-2013-deleting-existing-network-regions.md).</span></span>

<div>

## <a name="to-create-a-network-region"></a><span data-ttu-id="0ee10-114">ネットワークの領域を作成するには</span><span class="sxs-lookup"><span data-stu-id="0ee10-114">To create a network region</span></span>

1.  <span data-ttu-id="0ee10-115">RTCUniversalServerAdmins グループ (または同等のユーザー権限を持つグループ) のメンバーであるユーザー アカウントまたは CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="0ee10-115">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="0ee10-116">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="0ee10-116">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="0ee10-117">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="0ee10-117">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="0ee10-118">左側のナビゲーションバーで [ **ネットワーク構成** ] をクリックし、[ **地域**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0ee10-118">In the left navigation bar, click **Network Configuration** and then click **Region**.</span></span>

4.  <span data-ttu-id="0ee10-119">[ **領域** ] ページで、[ **新規**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0ee10-119">On the **Region** page, click **New**.</span></span>

5.  <span data-ttu-id="0ee10-120">[ **新しい領域** ] ページで、[ **名前** ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0ee10-120">In the **New Region** page, type a value in the **Name** field.</span></span> <span data-ttu-id="0ee10-121">この値は、Microsoft Lync Server 2013 の展開内で一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ee10-121">This value must be unique within your Microsoft Lync Server 2013 deployment.</span></span>

6.  <span data-ttu-id="0ee10-122">[ **セントラルサイト** ] ドロップダウンリストから、このネットワーク領域のセントラルサイトを選びます。</span><span class="sxs-lookup"><span data-stu-id="0ee10-122">From the **Central site** drop-down list, select the central site for this network region.</span></span>

7.  <span data-ttu-id="0ee10-123">[ **オーディオ代替パスを有効にする** ] チェックボックスは、既定でオンになっています。</span><span class="sxs-lookup"><span data-stu-id="0ee10-123">The **Enable audio alternate path** check box is checked by default.</span></span> <span data-ttu-id="0ee10-124">このフィールドは、十分な帯域幅がプライマリパスに存在しない場合に、代替パスを介して音声通話をルーティングするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0ee10-124">This field determines whether audio calls will be routed through an alternate path if adequate bandwidth does not exist in the primary path.</span></span> <span data-ttu-id="0ee10-125">オフロードをインターネットにオフにする必要がある場合にのみ、このチェックボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="0ee10-125">Clear this check box only if you need to turn off the offload to the Internet.</span></span> <span data-ttu-id="0ee10-126">いずれかの通話がインターネット通話の場合は、帯域幅の設定に関係なく、このチェックボックスをオンにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ee10-126">If any of your calls will be Internet calls, this check box must be checked, regardless of bandwidth settings.</span></span>

8.  <span data-ttu-id="0ee10-127">[ **ビデオの代替パスを有効にする** ] チェックボックスは、既定でオンになっています。</span><span class="sxs-lookup"><span data-stu-id="0ee10-127">The **Enable video alternate path** check box is checked by default.</span></span> <span data-ttu-id="0ee10-128">このフィールドは、ビデオ通話が、プライマリパスに十分な帯域幅が存在しない場合に、代替パスを使用してビデオ通話をルーティングするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0ee10-128">This field determines whether video calls will be routed through an alternate path if adequate bandwidth does not exist in the primary path.</span></span> <span data-ttu-id="0ee10-129">オフロードをインターネットにオフにする必要がある場合にのみ、このチェックボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="0ee10-129">Clear this check box only if you need to turn off the offload to the Internet.</span></span> <span data-ttu-id="0ee10-130">いずれかの通話がインターネット通話の場合は、帯域幅の設定に関係なく、このチェックボックスをオンにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ee10-130">If any of your calls will be Internet calls, this check box must be checked, regardless of bandwidth settings.</span></span>

9.  <span data-ttu-id="0ee10-131">省略[ **説明** ] フィールドに値を入力して、この領域について、名前だけでは表現できない詳細情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="0ee10-131">(Optional) Type a value in the **Description** field to provide more information about this region that cannot be expressed by the name alone.</span></span>

10. <span data-ttu-id="0ee10-132">[**コミット**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0ee10-132">Click **Commit**.</span></span>

<span data-ttu-id="0ee10-133">**関連付けら** れたサイトテーブルは、ネットワーク領域の作成には使用されません。</span><span class="sxs-lookup"><span data-stu-id="0ee10-133">The **Associated sites** table is not used for creating a network region.</span></span> <span data-ttu-id="0ee10-134">サイトを作成または変更するときに、サイトを地域に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="0ee10-134">You associate a site with a region when you create or modify the site.</span></span> <span data-ttu-id="0ee10-135">詳細について [は、「Lync Server 2013 でネットワークサイトを作成または変更する](lync-server-2013-creating-or-modifying-network-sites.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0ee10-135">For details, see [Creating or modifying network sites in Lync Server 2013](lync-server-2013-creating-or-modifying-network-sites.md).</span></span>

</div>

<div>

## <a name="to-modify-a-network-region"></a><span data-ttu-id="0ee10-136">ネットワークの領域を変更するには</span><span class="sxs-lookup"><span data-stu-id="0ee10-136">To modify a network region</span></span>

1.  <span data-ttu-id="0ee10-137">RTCUniversalServerAdmins グループ (または同等のユーザー権限を持つグループ) のメンバーであるユーザー アカウントまたは CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="0ee10-137">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="0ee10-138">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="0ee10-138">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="0ee10-139">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="0ee10-139">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="0ee10-140">左側のナビゲーションバーで [ **ネットワーク構成** ] をクリックし、[ **地域**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0ee10-140">In the left navigation bar, click **Network Configuration** and then click **Region**.</span></span>

4.  <span data-ttu-id="0ee10-141">[ **領域** ] ページで、変更する領域をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0ee10-141">On the **Region** page, click the region that you want to modify.</span></span>

5.  <span data-ttu-id="0ee10-142">[**編集**] メニューの [**詳細の表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0ee10-142">On the **Edit** menu, click **Show details**.</span></span>

6.  <span data-ttu-id="0ee10-143">[ **領域の編集** ] ページで、オーディオおよびビデオの代替パスを有効または無効にする設定を変更したり、説明を変更したりすることができます (詳細については、このトピックの「ネットワーク領域を作成する」セクションを参照してください)。</span><span class="sxs-lookup"><span data-stu-id="0ee10-143">On the **Edit Region** page, you can modify the settings for enabling and disabling audio and video alternate paths, and change the description (for details, see the "To create a network region" section earlier in this topic.</span></span>

7.  <span data-ttu-id="0ee10-144">[**コミット**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0ee10-144">Click **Commit**.</span></span>

<span data-ttu-id="0ee10-145">このページでは、 **関連付けられたサイト** を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="0ee10-145">You cannot modify the **Associated sites** on this page.</span></span> <span data-ttu-id="0ee10-146">関連付けられたサイトの一覧は参照用に提供されるため、地域設定を変更したときに影響を受けるサイトがわかります。</span><span class="sxs-lookup"><span data-stu-id="0ee10-146">The list of associated sites is provided for reference so you are aware of which sites will be affected when you modify the region settings.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="0ee10-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="0ee10-147">See Also</span></span>


[<span data-ttu-id="0ee10-148">Lync Server 2013 で既存のネットワーク領域を削除する</span><span class="sxs-lookup"><span data-stu-id="0ee10-148">Deleting existing network regions in Lync Server 2013</span></span>](lync-server-2013-deleting-existing-network-regions.md)  
[<span data-ttu-id="0ee10-149">Lync Server 2013 での CAC のネットワーク領域の構成</span><span class="sxs-lookup"><span data-stu-id="0ee10-149">Configure network regions for CAC in Lync Server 2013</span></span>](lync-server-2013-configure-network-regions-for-cac.md)  


[<span data-ttu-id="0ee10-150">新しい CsNetworkRegion</span><span class="sxs-lookup"><span data-stu-id="0ee10-150">New-CsNetworkRegion</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkRegion)  
[<span data-ttu-id="0ee10-151">Set-CsNetworkRegion</span><span class="sxs-lookup"><span data-stu-id="0ee10-151">Set-CsNetworkRegion</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkRegion)  
[<span data-ttu-id="0ee10-152">CsNetworkRegion の削除</span><span class="sxs-lookup"><span data-stu-id="0ee10-152">Remove-CsNetworkRegion</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkRegion)  
[<span data-ttu-id="0ee10-153">Get-CsNetworkRegion</span><span class="sxs-lookup"><span data-stu-id="0ee10-153">Get-CsNetworkRegion</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkRegionLink)  
  

<span data-ttu-id="0ee10-154"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0ee10-154"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

