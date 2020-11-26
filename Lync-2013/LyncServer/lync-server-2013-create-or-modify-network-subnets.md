---
title: 'Lync Server 2013: ネットワークサブネットを作成または変更する'
description: 'Lync Server 2013: ネットワークサブネットを作成または変更します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify network subnets
ms:assetid: 1ba8c4e3-fbc7-4758-88ac-d651fef17bed
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520957(v=OCS.15)
ms:contentKeyID: 48183548
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 37695707bf39b10c351a4990b132c9799406f9c4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431653"
---
# <a name="create-or-modify-network-subnets-in-lync-server-2013"></a><span data-ttu-id="1dfe3-103">Lync Server 2013 でネットワークサブネットを作成または変更する</span><span class="sxs-lookup"><span data-stu-id="1dfe3-103">Create or modify network subnets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1dfe3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1dfe3-104">

<span> </span></span></span>

<span data-ttu-id="1dfe3-105">_**最終更新日:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="1dfe3-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="1dfe3-106">ネットワークサブネットは、このサブネットに属しているホストの地理的な場所を判断するために、ネットワークサイトと関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="1dfe3-106">A network subnet must be associated with a network site for the purposes of determining the geographic location of the host belonging to this subnet.</span></span> <span data-ttu-id="1dfe3-107">Lync Server コントロールパネルを使用して、サブネットを構成することができます。</span><span class="sxs-lookup"><span data-stu-id="1dfe3-107">You can use Lync Server Control Panel to configure subnets.</span></span> <span data-ttu-id="1dfe3-108">Lync Server コントロールパネルから、ネットワークサブネットの作成、変更、または削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="1dfe3-108">From the Lync Server Control Panel, you can create, modify, or delete a network subnet.</span></span> <span data-ttu-id="1dfe3-109">ネットワークサブネットの削除の詳細については、「 [Lync Server 2013 でのネットワークサブネットの削除](lync-server-2013-deleting-network-subnets.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1dfe3-109">For details about deleting network subnets, see [Deleting network subnets in Lync Server 2013](lync-server-2013-deleting-network-subnets.md).</span></span>

<span data-ttu-id="1dfe3-110">通話受付制御 (CAC) が実装されている Microsoft Lync Server 2013 の大半の展開では、通常、多数のサブネットが存在します。</span><span class="sxs-lookup"><span data-stu-id="1dfe3-110">In most deployments of Microsoft Lync Server 2013 where call admission control (CAC) is implemented, there will typically be a large number of subnets.</span></span> <span data-ttu-id="1dfe3-111">このため、多くの場合、Lync Server 管理シェルからサブネットを構成することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="1dfe3-111">Because of this, it is often best to configure subnets from the Lync Server Management Shell.</span></span> <span data-ttu-id="1dfe3-112">そこから、Windows PowerShell コマンドレットの **Import-CSV** と組み合わせて、**新しい csnetworksubnet** を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="1dfe3-112">From there you can call **New-CsNetworkSubnet** in conjunction with the Windows PowerShell cmdlet **Import-CSV**.</span></span> <span data-ttu-id="1dfe3-113">これらのコマンドレットを一緒に使用することで、サブネットの設定をコンマ区切り値 (.csv) ファイルから読み取り、複数のサブネットを同時に作成することができます。</span><span class="sxs-lookup"><span data-stu-id="1dfe3-113">By using these cmdlets together, you can read in subnet settings from a comma-separated values (.csv) file and create multiple subnets at the same time.</span></span> <span data-ttu-id="1dfe3-114">.Csv ファイルからサブネットを作成する方法の例については、「 [新しい-CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1dfe3-114">For examples of how to create subnets from a .csv file, see [New-CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet).</span></span>

<div>

## <a name="to-create-a-network-subnet"></a><span data-ttu-id="1dfe3-115">ネットワークサブネットを作成するには</span><span class="sxs-lookup"><span data-stu-id="1dfe3-115">To create a network subnet</span></span>

1.  <span data-ttu-id="1dfe3-116">RTCUniversalServerAdmins グループ (または同等のユーザー権限を持つグループ) のメンバーであるユーザー アカウントまたは CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="1dfe3-116">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="1dfe3-117">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="1dfe3-117">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="1dfe3-118">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="1dfe3-118">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="1dfe3-119">左側のナビゲーションバーで [ **ネットワーク構成** ] をクリックし、[ **サブネット**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1dfe3-119">In the left navigation bar, click **Network Configuration** and then click **Subnet**.</span></span>

4.  <span data-ttu-id="1dfe3-120">[ **サブネット** ] ページで、[ **新規**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1dfe3-120">On the **Subnet** page, click **New**.</span></span>

5.  <span data-ttu-id="1dfe3-121">[ **新しいサブネット**] で、[ **サブネット ID** ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1dfe3-121">In **New Subnet**, enter a value in the **Subnet ID** field.</span></span> <span data-ttu-id="1dfe3-122">これは IP アドレス (たとえば、174.11.12.0) である必要があり、サブネットで定義された IP アドレス範囲の最初のアドレスである必要があります。</span><span class="sxs-lookup"><span data-stu-id="1dfe3-122">This must be an IP address (for example, 174.11.12.0), and it must be the first address in the IP address range defined by the subnet.</span></span>

6.  <span data-ttu-id="1dfe3-123">[ **マスク** ] フィールドに、1 ~ 32 の数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1dfe3-123">In the **Mask** field, enter a numeric value from 1 through 32.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="1dfe3-124">この値は、作成されるサブネットに適用されるビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="1dfe3-124">This value is the bitmask that is to be applied to the subnet being created.</span></span>

    
    </div>

7.  <span data-ttu-id="1dfe3-125">[ **ネットワークサイト ID**] で、このサブネットが所属するサイトを選びます。</span><span class="sxs-lookup"><span data-stu-id="1dfe3-125">In **Network site ID**, select the site to which this subnet belongs.</span></span>

8.  <span data-ttu-id="1dfe3-126">省略[ **説明** ] フィールドに値を入力して、このサブネットについて、名前だけでは表現できない詳細情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="1dfe3-126">(Optional) Type a value in the **Description** field to provide more information about this subnet that cannot be expressed by the name alone.</span></span>

9.  <span data-ttu-id="1dfe3-127">[**コミット**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1dfe3-127">Click **Commit**.</span></span>

</div>

<div>

## <a name="to-modify-a-network-subnet"></a><span data-ttu-id="1dfe3-128">ネットワークサブネットを変更するには</span><span class="sxs-lookup"><span data-stu-id="1dfe3-128">To modify a network subnet</span></span>

1.  <span data-ttu-id="1dfe3-129">RTCUniversalServerAdmins グループ (または同等のユーザー権限を持つグループ) のメンバーであるユーザー アカウントまたは CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="1dfe3-129">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="1dfe3-130">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="1dfe3-130">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="1dfe3-131">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="1dfe3-131">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="1dfe3-132">左側のナビゲーションバーで [ **ネットワーク構成** ] をクリックし、[ **サブネット**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1dfe3-132">In the left navigation bar, click **Network Configuration** and then click **Subnet**.</span></span>

4.  <span data-ttu-id="1dfe3-133">[ **Subnet** ] ページで、変更するサブネットをクリックします。</span><span class="sxs-lookup"><span data-stu-id="1dfe3-133">On the **Subnet** page, click the subnet that you want to modify.</span></span>

5.  <span data-ttu-id="1dfe3-134">[**編集**] メニューの [**詳細の表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1dfe3-134">On the **Edit** menu, click **Show details**.</span></span>

6.  <span data-ttu-id="1dfe3-135">[ **サブネットの編集** ] ページでは、ビットマスク、関連付けられたネットワークサイト、または説明を変更できます。</span><span class="sxs-lookup"><span data-stu-id="1dfe3-135">On the **Edit Subnet** page, you can modify the bitmask, associated network site, or description.</span></span> <span data-ttu-id="1dfe3-136">ビットマスクを変更する場合は、サブネット ID が、サブネットで定義されている IP アドレス範囲の最初のアドレスである必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="1dfe3-136">If you modify the bitmask, keep in mind that the Subnet ID must still be the first address in the IP address range defined by the subnet.</span></span>

7.  <span data-ttu-id="1dfe3-137">[**コミット**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1dfe3-137">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="1dfe3-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="1dfe3-138">See Also</span></span>


[<span data-ttu-id="1dfe3-139">Lync Server 2013 でのネットワークサブネットの削除</span><span class="sxs-lookup"><span data-stu-id="1dfe3-139">Deleting network subnets in Lync Server 2013</span></span>](lync-server-2013-deleting-network-subnets.md)  


[<span data-ttu-id="1dfe3-140">Lync Server 2013 ネットワーク領域、サイト、およびサブネットの構成</span><span class="sxs-lookup"><span data-stu-id="1dfe3-140">About network regions, sites, and subnets in Lync Server 2013</span></span>](lync-server-2013-about-network-regions-sites-and-subnets.md)  


[<span data-ttu-id="1dfe3-141">新しい-CsNetworkSubnet</span><span class="sxs-lookup"><span data-stu-id="1dfe3-141">New-CsNetworkSubnet</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet)  
[<span data-ttu-id="1dfe3-142">Set-CsNetworkSubnet</span><span class="sxs-lookup"><span data-stu-id="1dfe3-142">Set-CsNetworkSubnet</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkSubnet)  
[<span data-ttu-id="1dfe3-143">CsNetworkSubnet の削除</span><span class="sxs-lookup"><span data-stu-id="1dfe3-143">Remove-CsNetworkSubnet</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkSubnet)  
[<span data-ttu-id="1dfe3-144">Get-CsNetworkSubnet</span><span class="sxs-lookup"><span data-stu-id="1dfe3-144">Get-CsNetworkSubnet</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkSubnet)  
  

<span data-ttu-id="1dfe3-145"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1dfe3-145"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

