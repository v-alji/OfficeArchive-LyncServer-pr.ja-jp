---
title: 'Lync Server 2013: ネットワークの領域、サイト、サブネットの展開'
description: 'Lync Server 2013: ネットワークの領域、サイト、サブネットを展開しています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying network regions, sites, and subnets
ms:assetid: c4b75601-3538-4d07-8d23-1ad90459ae48
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994067(v=OCS.15)
ms:contentKeyID: 51803978
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f1c4c08cd9b78b1439000cdb4a7bbe3ffc2f99d8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429847"
---
# <a name="deploying-network-regions-sites-and-subnets-in-lync-server-2013"></a><span data-ttu-id="1d2db-103">Lync Server 2013 でのネットワークのリージョン、サイト、サブネットの展開</span><span class="sxs-lookup"><span data-stu-id="1d2db-103">Deploying network regions, sites, and subnets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1d2db-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1d2db-104">

<span> </span></span></span>

<span data-ttu-id="1d2db-105">_**最終更新日:** 2013-03-12_</span><span class="sxs-lookup"><span data-stu-id="1d2db-105">_**Topic Last Modified:** 2013-03-12_</span></span>

<span data-ttu-id="1d2db-106">エンタープライズ Voip を展開したら、次のように構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1d2db-106">Once Enterprise Voice is deployed, you need to configure:</span></span>

  - <span data-ttu-id="1d2db-107">ネットワーク領域</span><span class="sxs-lookup"><span data-stu-id="1d2db-107">Network regions</span></span>

  - <span data-ttu-id="1d2db-108">ネットワークサイト</span><span class="sxs-lookup"><span data-stu-id="1d2db-108">Network sites</span></span>

  - <span data-ttu-id="1d2db-109">ネットワークサブネット</span><span class="sxs-lookup"><span data-stu-id="1d2db-109">Network subnets</span></span>

<div>

## <a name="define-network-regions"></a><span data-ttu-id="1d2db-110">ネットワーク領域を定義する</span><span class="sxs-lookup"><span data-stu-id="1d2db-110">Define Network Regions</span></span>

<span data-ttu-id="1d2db-111">Lync Server Windows PowerShell コマンド、新しい CsNetworkRegion、または Lync Server コントロールパネルを使用して、ネットワークの領域を定義します。</span><span class="sxs-lookup"><span data-stu-id="1d2db-111">Use the Lync Server Windows PowerShell command, New-CsNetworkRegion, or Lync Server Control Panel to define network regions.</span></span>

    New-CsNetworkRegion -NetworkRegionID <region ID> -CentralSite <site ID>

<span data-ttu-id="1d2db-112">詳細については、「 [新しい-CsNetworkRegion](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkRegion)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1d2db-112">For more information, see [New-CsNetworkRegion](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkRegion).</span></span>

<span data-ttu-id="1d2db-113">この例では、次の Windows PowerShell コマンドは、このシナリオで定義されたネットワークの領域 (インド) を示しています。</span><span class="sxs-lookup"><span data-stu-id="1d2db-113">For this example, the following Windows PowerShell command illustrates the network region, region 1 (India), defined in this scenario.</span></span>

    New-CsNetworkRegion -NetworkRegionID "India" -CentralSite "India Central Site"

<div>


</div>

</div>

<div>

## <a name="define-network-sites"></a><span data-ttu-id="1d2db-114">ネットワークサイトを定義する</span><span class="sxs-lookup"><span data-stu-id="1d2db-114">Define Network Sites</span></span>

<span data-ttu-id="1d2db-115">Lync Server Windows PowerShell コマンド、新しい CsNetworkSite、または Lync Server コントロールパネルを使用して、ネットワークサイトを定義します。</span><span class="sxs-lookup"><span data-stu-id="1d2db-115">Use the Lync Server Windows PowerShell command, New-CsNetworkSite, or the Lync Server Control Panel to define network sites.</span></span>

    New-CsNetworkSite -NetworkSiteID <site ID> -NetworkRegionID <region ID>

<span data-ttu-id="1d2db-116">詳細については、「 [新しい-CsNetworkSite](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSite)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1d2db-116">For more information, see [New-CsNetworkSite](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSite).</span></span>

<span data-ttu-id="1d2db-117">この例では、次の表と Lync Server Windows PowerShell コマンドはこのシナリオで定義されたネットワークサイトを示しています。</span><span class="sxs-lookup"><span data-stu-id="1d2db-117">For this example, the following table and Lync Server Windows PowerShell command illustrate the network sites defined in this scenario.</span></span> <span data-ttu-id="1d2db-118">この表には、Location-Based ルーティングに固有の設定のみが含まれています。</span><span class="sxs-lookup"><span data-stu-id="1d2db-118">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

    New-CsNetworkSite -NetworkSiteID "Delhi" -NetworkRegionID "India"
    New-CsNetworkSite -NetworkSiteID "Hyderabad" -NetworkRegionID "India"


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="1d2db-119">サイト 1 (ニューデリー)</span><span class="sxs-lookup"><span data-stu-id="1d2db-119">Site 1 (Delhi)</span></span></th>
<th><span data-ttu-id="1d2db-120">サイト 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="1d2db-120">Site 2 (Hyderabad)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1d2db-121">サイト ID</span><span class="sxs-lookup"><span data-stu-id="1d2db-121">Site ID</span></span></p></td>
<td><p><span data-ttu-id="1d2db-122">サイト 1 (ニューデリー)</span><span class="sxs-lookup"><span data-stu-id="1d2db-122">Site 1 (Delhi)</span></span></p></td>
<td><p><span data-ttu-id="1d2db-123">サイト 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="1d2db-123">Site 2 (Hyderabad)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d2db-124">地域 ID</span><span class="sxs-lookup"><span data-stu-id="1d2db-124">Region ID</span></span></p></td>
<td><p><span data-ttu-id="1d2db-125">地域 1 (インド)</span><span class="sxs-lookup"><span data-stu-id="1d2db-125">Region 1 (India)</span></span></p></td>
<td><p><span data-ttu-id="1d2db-126">地域 1 (インド)</span><span class="sxs-lookup"><span data-stu-id="1d2db-126">Region 1 (India)</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="define-network-subnets"></a><span data-ttu-id="1d2db-127">ネットワークサブネットを定義する</span><span class="sxs-lookup"><span data-stu-id="1d2db-127">Define Network Subnets</span></span>

<span data-ttu-id="1d2db-128">Lync Server Windows PowerShell コマンド、新しい-CsNetworkSubnet、または Lync Server コントロールパネルを使用して、ネットワークサブネットを定義し、それらをネットワークサイトに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="1d2db-128">Use the Lync Server Windows PowerShell command, New-CsNetworkSubnet, or the Lync Server Control Panel to define network subnets and assign them to network sites.</span></span>

    New-CsNetworkSubnet -SubnetID <Subnet IP address> -MaskBits <Subnet bitmask> -NetworkSiteID <site ID>

<span data-ttu-id="1d2db-129">詳細については、「 [新しい-CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1d2db-129">For more information, see [New-CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet).</span></span>

<span data-ttu-id="1d2db-130">この例では、次の表と Windows PowerShell コマンドは、このシナリオで定義されたネットワークサイト、ニューデリー、Hyderabad へのネットワークサブネットの割り当てを示しています。</span><span class="sxs-lookup"><span data-stu-id="1d2db-130">For this example, the following table and Windows PowerShell commands illustrate the assignment of network subnets to the network sites, Delhi and Hyderabad, defined in this scenario.</span></span> <span data-ttu-id="1d2db-131">この表には、Location-Based ルーティングに固有の設定のみが含まれています。</span><span class="sxs-lookup"><span data-stu-id="1d2db-131">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

    New-CsNetworkSubnet -SubnetID "192.168.0.0" -MaskBits "24" -NetworkSiteID "Delhi"
    New-CsNetworkSubnet -SubnetID "192.168.1.0" -MaskBits "24" -NetworkSiteID "Hyderabad"


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="1d2db-132">サイト 1 (ニューデリー)</span><span class="sxs-lookup"><span data-stu-id="1d2db-132">Site 1 (Delhi)</span></span></th>
<th><span data-ttu-id="1d2db-133">サイト 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="1d2db-133">Site 2 (Hyderabad)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1d2db-134">サブネット ID</span><span class="sxs-lookup"><span data-stu-id="1d2db-134">Subnet ID</span></span></p></td>
<td><p><span data-ttu-id="1d2db-135">192.168.0.0</span><span class="sxs-lookup"><span data-stu-id="1d2db-135">192.168.0.0</span></span></p></td>
<td><p><span data-ttu-id="1d2db-136">192.168.1.0</span><span class="sxs-lookup"><span data-stu-id="1d2db-136">192.168.1.0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d2db-137">Mask</span><span class="sxs-lookup"><span data-stu-id="1d2db-137">Mask</span></span></p></td>
<td><p><span data-ttu-id="1d2db-138">24</span><span class="sxs-lookup"><span data-stu-id="1d2db-138">24</span></span></p></td>
<td><p><span data-ttu-id="1d2db-139">24</span><span class="sxs-lookup"><span data-stu-id="1d2db-139">24</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d2db-140">サイト ID</span><span class="sxs-lookup"><span data-stu-id="1d2db-140">Site ID</span></span></p></td>
<td><p><span data-ttu-id="1d2db-141">サイト 1 (ニューデリー)</span><span class="sxs-lookup"><span data-stu-id="1d2db-141">Site 1 (Delhi)</span></span></p></td>
<td><p><span data-ttu-id="1d2db-142">サイト 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="1d2db-142">Site 2 (Hyderabad)</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="1d2db-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="1d2db-143">See Also</span></span>


[<span data-ttu-id="1d2db-144">Lync Server 2013 の場所に基づくルーティングの構成</span><span class="sxs-lookup"><span data-stu-id="1d2db-144">Configuring Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-configuring-location-based-routing.md)  
  

<span data-ttu-id="1d2db-145"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1d2db-145"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

