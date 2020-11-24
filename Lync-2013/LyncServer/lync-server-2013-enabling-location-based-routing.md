---
title: 'Lync Server 2013: Location-Based ルーティングを有効にする'
description: 'Lync Server 2013: Location-Based ルーティングを有効にします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enabling Location-Based Routing
ms:assetid: 029ede7e-0c4e-4ad2-af99-909ae674d6fe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994014(v=OCS.15)
ms:contentKeyID: 51803920
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7844af5792468cd5645b6b42c857c63b943c2df1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399285"
---
# <a name="enabling-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="eb1a5-103">Lync Server 2013 での Location-Based ルーティングの有効化</span><span class="sxs-lookup"><span data-stu-id="eb1a5-103">Enabling Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="eb1a5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="eb1a5-104">

<span> </span></span></span>

<span data-ttu-id="eb1a5-105">_**最終更新日:** 2013-04-26_</span><span class="sxs-lookup"><span data-stu-id="eb1a5-105">_**Topic Last Modified:** 2013-04-26_</span></span>

<span data-ttu-id="eb1a5-106">エンタープライズ Voip が展開され、ネットワーク領域、サイト、サブネットが定義されたら、Location-Based ルーティングを有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="eb1a5-106">Once Enterprise Voice is deployed and network regions, sites and subnets are defined, you can enable Location-Based Routing.</span></span> <span data-ttu-id="eb1a5-107">次のエンタープライズボイス要素で Location-Based ルーティングを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="eb1a5-107">Location-Based Routing must be enabled for the following Enterprise Voice elements:</span></span>

  - <span data-ttu-id="eb1a5-108">ネットワークサイト</span><span class="sxs-lookup"><span data-stu-id="eb1a5-108">Network sites</span></span>

  - <span data-ttu-id="eb1a5-109">トランク構成</span><span class="sxs-lookup"><span data-stu-id="eb1a5-109">Trunk configurations</span></span>

  - <span data-ttu-id="eb1a5-110">音声ポリシー</span><span class="sxs-lookup"><span data-stu-id="eb1a5-110">Voice policies</span></span>

  - <span data-ttu-id="eb1a5-111">ルーティング構成</span><span class="sxs-lookup"><span data-stu-id="eb1a5-111">Routing configuration</span></span>

<div>

## <a name="enable-location-based-routing-to-network-sites"></a><span data-ttu-id="eb1a5-112">ネットワークサイトへの Location-Based ルーティングを有効にする</span><span class="sxs-lookup"><span data-stu-id="eb1a5-112">Enable Location-Based Routing to Network Sites</span></span>

<span data-ttu-id="eb1a5-113">エンタープライズ Voip を展開し、ネットワークサイトを構成したら、Location-Based ルーティングを構成することができます。</span><span class="sxs-lookup"><span data-stu-id="eb1a5-113">After you have deployed Enterprise Voice, and configured network sites, you are ready to configure Location-Based Routing.</span></span> <span data-ttu-id="eb1a5-114">まず、音声ルーティングポリシーを作成して、ネットワークサイトを適切な PSTN 使用法に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="eb1a5-114">First, you create a voice routing policy to associate the network site with the appropriate PSTN usages.</span></span> <span data-ttu-id="eb1a5-115">ボイスルーティングポリシーに PSTN の使用を割り当てる場合は、サイトのローカルの PSTN ゲートウェイ、または Location-Based ルーティング制限を必要としない地域にある PSTN ゲートウェイを使用しているボイスルーティングに関連する PSTN の使用のみを使用してください。Lync Server Windows PowerShell コマンド、新規-CsVoiceRoutingPolicy、または Lync Server コントロールパネルを使用して、ボイスルーティングポリシーを作成します。</span><span class="sxs-lookup"><span data-stu-id="eb1a5-115">When assigning PSTN usages to a voice routing policy, make sure to only use PSTN usages that are associated to voice routes that use a PSTN gateway local to the site or a PSTN gateway that is located in a region where Location-Based Routing restrictions are not needed.Use the Lync Server Windows PowerShell command, New-CsVoiceRoutingPolicy, or Lync Server Control Panel to create voice routing policies.</span></span>

    New-CsVoiceRoutingPolicy -Identity <voice routing policy ID> -Name <voice routing policy name> -PstnUsages <usages>

<span data-ttu-id="eb1a5-116">詳細については、「[New-CsVoiceRoutingPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsVoiceRoutingPolicy)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="eb1a5-116">For more information, see [New-CsVoiceRoutingPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsVoiceRoutingPolicy).</span></span>

<span data-ttu-id="eb1a5-117">この例では、次の表と Windows PowerShell コマンドは、このシナリオで定義された2つのボイスルーティングポリシーと関連する PSTN 使用法を示しています。</span><span class="sxs-lookup"><span data-stu-id="eb1a5-117">For this example, the following table and Windows PowerShell commands illustrate two voice routing policies and their associated PSTN usages defined in this scenario.</span></span> <span data-ttu-id="eb1a5-118">この表には、Location-Based ルーティングに固有の設定のみが含まれています。</span><span class="sxs-lookup"><span data-stu-id="eb1a5-118">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

    New-CsVoiceRoutingPolicy -Identity "DelhiVoiceRoutingPolicy" -Name "Delhi voice routing policy" -PstnUsages @{add="Delhi usage", "PBX Del usage", "PBX Hyd usage"}
    New-CsVoiceRoutingPolicy -Identity "HyderabadVoiceRoutingPolicy" -Name " Hyderabad voice routing policy" -PstnUsages @{add="Hyderabad usage", "PBX Del usage", "PBX Hyd usage"}


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="eb1a5-119">ボイスルーティングポリシー1</span><span class="sxs-lookup"><span data-stu-id="eb1a5-119">Voice routing policy 1</span></span></th>
<th><span data-ttu-id="eb1a5-120">ボイスルーティングポリシー2</span><span class="sxs-lookup"><span data-stu-id="eb1a5-120">Voice routing policy 2</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eb1a5-121">ボイスポリシー ID</span><span class="sxs-lookup"><span data-stu-id="eb1a5-121">Voice policy ID</span></span></p></td>
<td><p><span data-ttu-id="eb1a5-122">ニューデリーボイスルーティングポリシー</span><span class="sxs-lookup"><span data-stu-id="eb1a5-122">Delhi voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="eb1a5-123">Hyderabad ボイスルーティングポリシー</span><span class="sxs-lookup"><span data-stu-id="eb1a5-123">Hyderabad voice routing policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb1a5-124">PSTN の使用状況</span><span class="sxs-lookup"><span data-stu-id="eb1a5-124">PSTN usages</span></span></p></td>
<td><p><span data-ttu-id="eb1a5-125">ニューデリー使用量, PBX Del usage, PBX Hyd usage</span><span class="sxs-lookup"><span data-stu-id="eb1a5-125">Delhi usage, PBX Del usage, PBX Hyd usage</span></span></p></td>
<td><p><span data-ttu-id="eb1a5-126">Hyderabad usage、PBX Hyd usage、PBX Del usage</span><span class="sxs-lookup"><span data-stu-id="eb1a5-126">Hyderabad usage, PBX Hyd usage, PBX Del usage</span></span></p></td>
</tr>
</tbody>
</table>

  

<span data-ttu-id="eb1a5-127">次に、該当するネットワークサイト用に Location-Based ルーティングを構成し、ボイスルーティングポリシーを関連付けます。</span><span class="sxs-lookup"><span data-stu-id="eb1a5-127">Next, configure Location-Based Routing for the applicable network sites and associate your voice routing policies to them.</span></span> <span data-ttu-id="eb1a5-128">[Lync Server Windows PowerShell] コマンド (新しい CsNetworkSite) を使用して Location-Based ルーティングを有効にし、ルーティングの制限を適用する必要があるネットワークサイトにボイスルーティングポリシーを関連付けます。</span><span class="sxs-lookup"><span data-stu-id="eb1a5-128">Use the Lync Server Windows PowerShell command, New-CsNetworkSite, to enable Location-Based Routing and associate voice routing policies to your network sites that must enforce routing restrictions.</span></span>

    Set-CsNetworkSite -Identity <site ID> -EnableLocationBasedRouting <$true|$false> -VoiceRoutingPolicy <voice routing policy ID>

<span data-ttu-id="eb1a5-129">この例では、次の表に、Lync Server Windows PowerShell を使用して、このシナリオで定義されている2つの異なるネットワークサイト、Hyderabad のルーティングを Location-Based 示します。</span><span class="sxs-lookup"><span data-stu-id="eb1a5-129">In this example, the following table illustrates Location-Based Routing for two different network sites, Delhi and Hyderabad, defined in this scenario using the Lync Server Windows PowerShell.</span></span> <span data-ttu-id="eb1a5-130">この表には、Location-Based ルーティングに固有の設定のみが含まれています。</span><span class="sxs-lookup"><span data-stu-id="eb1a5-130">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

    Set-CsNetworkSite -Identity "Delhi" -EnableLocationBasedRouting $true -VoiceRoutingPolicy "DelhiVoiceRoutingPolicy"
    Set-CsNetworkSite -Identity "Hyderabad" -EnableLocationBasedRouting $true -VoiceRoutingPolicy "HyderabadVoiceRoutingPolicy"


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="eb1a5-131">サイト 1 (ニューデリー)</span><span class="sxs-lookup"><span data-stu-id="eb1a5-131">Site 1 (Delhi)</span></span></th>
<th><span data-ttu-id="eb1a5-132">サイト 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="eb1a5-132">Site 2 (Hyderabad)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eb1a5-133">サイト名</span><span class="sxs-lookup"><span data-stu-id="eb1a5-133">Site Name</span></span></p></td>
<td><p><span data-ttu-id="eb1a5-134">サイト 1 (ニューデリー)</span><span class="sxs-lookup"><span data-stu-id="eb1a5-134">Site 1 (Delhi)</span></span></p></td>
<td><p><span data-ttu-id="eb1a5-135">サイト 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="eb1a5-135">Site 2 (Hyderabad)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb1a5-136">Enablelocationrouting ルーティング</span><span class="sxs-lookup"><span data-stu-id="eb1a5-136">EnableLocationBasedRouting</span></span></p></td>
<td><p><span data-ttu-id="eb1a5-137">True</span><span class="sxs-lookup"><span data-stu-id="eb1a5-137">True</span></span></p></td>
<td><p><span data-ttu-id="eb1a5-138">True</span><span class="sxs-lookup"><span data-stu-id="eb1a5-138">True</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb1a5-139">ボイスルーティングポリシー</span><span class="sxs-lookup"><span data-stu-id="eb1a5-139">Voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="eb1a5-140">ニューデリーボイスルーティングポリシー</span><span class="sxs-lookup"><span data-stu-id="eb1a5-140">Delhi voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="eb1a5-141">Hyderabad ボイスルーティングポリシー</span><span class="sxs-lookup"><span data-stu-id="eb1a5-141">Hyderabad voice routing policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb1a5-142">サブネット</span><span class="sxs-lookup"><span data-stu-id="eb1a5-142">Subnets</span></span></p></td>
<td><p><span data-ttu-id="eb1a5-143">Subnet 1 (ニューデリー)</span><span class="sxs-lookup"><span data-stu-id="eb1a5-143">Subnet 1 (Delhi)</span></span></p></td>
<td><p><span data-ttu-id="eb1a5-144">Subnet 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="eb1a5-144">Subnet 2 (Hyderabad)</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="enable-location-based-routing-to-trunks"></a><span data-ttu-id="eb1a5-145">Trunks への Location-Based ルーティングを有効にする</span><span class="sxs-lookup"><span data-stu-id="eb1a5-145">Enable Location-Based Routing to Trunks</span></span>

<span data-ttu-id="eb1a5-146">トランク構成を Location-Based ルーティング用に有効にするには、各トランクまたは各ネットワークサイト用にトランク構成を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eb1a5-146">Before a trunk configuration can be enabled for Location-Based Routing, you need to create a trunk configuration for each trunk or each network site.</span></span> <span data-ttu-id="eb1a5-147">Lync Server Windows PowerShell コマンドの New-Set-cstrunkconfiguration を使用して、トランク構成を作成します。</span><span class="sxs-lookup"><span data-stu-id="eb1a5-147">Use the Lync Server Windows PowerShell command, New-CsTrunkConfiguration, to create a trunk configuration.</span></span> <span data-ttu-id="eb1a5-148">特定のシステム (ゲートウェイまたは PBX など) に複数の trunks が関連付けられている場合は、各トランク構成を変更して Location-Based ルーティングの制限を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="eb1a5-148">If multiple trunks are associated with a given system (i.e. Gateway or PBX), each trunk configuration must be modified to enable Location-Based Routing restrictions.</span></span>

    New-CsTrunkConfiguration -Identity < trunk configuration ID>

<span data-ttu-id="eb1a5-149">詳細については、「 [New-set-cstrunkconfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsTrunkConfiguration)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="eb1a5-149">For more information, see [New-CsTrunkConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsTrunkConfiguration).</span></span>

<span data-ttu-id="eb1a5-150">この例では、次の Windows PowerShell コマンドを使用して、このシナリオで定義されている展開の各トランクに対してトランク構成を1つ作成しています。</span><span class="sxs-lookup"><span data-stu-id="eb1a5-150">For this example, the following Windows PowerShell commands illustrate creating one trunk configuration for each trunk in the deployment defined in this scenario.</span></span>

    New-CsTrunkConfiguration -Identity Service:PstnGateway:"<Trunk 1 DEL-GW>"
    New-CsTrunkConfiguration -Identity Service:PstnGateway:"<Trunk 2 HYD-GW>"
    New-CsTrunkConfiguration -Identity Service:PstnGateway:"<Trunk 3 DEL-PBX>"
    New-CsTrunkConfiguration -Identity Service:PstnGateway:"<Trunk 4 HYD-PBX>"

<span data-ttu-id="eb1a5-151">トランク構成がトランクごとに構成されると、Lync Server Windows PowerShell コマンド Set-cstrunkconfiguration を使用して、ルーティングの制限を適用する必要がある trunks へのルーティングを Location-Based 有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="eb1a5-151">Once a trunk configuration is configured per trunk, you can use the Lync Server Windows PowerShell command, Set-CsTrunkConfiguration, to enable Location-Based Routing to your trunks that must enforce routing restrictions.</span></span> <span data-ttu-id="eb1a5-152">Trunks へのルーティングを有効 Location-Based にします。 pstn への通話をルーティングする PSTN ゲートウェイへの通話をルーティングし、ゲートウェイが配置されているネットワークサイトを関連付けます。</span><span class="sxs-lookup"><span data-stu-id="eb1a5-152">Enable Location-Based Routing to trunks that route calls to PSTN gateways that route calls to the PSTN, and associate the network site where the gateway is located.</span></span>

    Set-CsTrunkConfiguration -Identity <trunk configuration ID> -EnableLocationRestriction $true -NetworkSiteID <site ID>

<span data-ttu-id="eb1a5-153">詳細については、「 [New-set-cstrunkconfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsTrunkConfiguration)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="eb1a5-153">For more information, see [New-CsTrunkConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsTrunkConfiguration).</span></span>

<span data-ttu-id="eb1a5-154">この例では、ニューデリーと Hyderabad の PSTN ゲートウェイに関連付けられている各トランクで Location-Based ルーティングが有効になっています。</span><span class="sxs-lookup"><span data-stu-id="eb1a5-154">In this example, Location-Based Routing is enabled for each trunk that is associated to PSTN gateways in Delhi and Hyderabad:</span></span>

    Set-CsTrunkConfiguration -Identity Service:PstnGateway:Trunk 1 DEL-GW -EnableLocationRestriction $true -NetworkSiteID "Delhi"
    Set-CsTrunkConfiguration -Identity Service:PstnGateway:Trunk 2 HYD-GW -EnableLocationRestriction $true -NetworkSiteID "Hyderabad"

  

<span data-ttu-id="eb1a5-155">PSTN への通話をルーティングしない trunks の Location-Based ルーティングを有効にしないでください。ただし、このトランク経由で接続されているエンドポイントに対応する PSTN 通話には、Location-Based ルーティング制限を適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eb1a5-155">Do not enable Location-Based Routing for trunks that do not route calls to the PSTN; however, you must still associate the trunk to the network site where the system is located as Location-Based Routing restrictions need to be enforced for PSTN calls reaching endpoints connected via this trunk.</span></span> <span data-ttu-id="eb1a5-156">この例では、ニューデリーと Hyderabad の PBX システムに関連付けられている各トランクの Location-Based ルーティングが有効になっていません。</span><span class="sxs-lookup"><span data-stu-id="eb1a5-156">For this example, Location-Based Routing is not enabled for each trunk that is associated to PBX systems in Delhi and Hyderabad:</span></span>

    Set-CsTrunkConfiguration -Identity Service:PstnGateway:Trunk 3 DEL-PBX -EnableLocationRestriction $false -NetworkSiteID "Delhi"
    Set-CsTrunkConfiguration -Identity Service:PstnGateway:Trunk 4 HYD-PBX -EnableLocationRestriction $false -NetworkSiteID "Hyderabad"

  
<span data-ttu-id="eb1a5-157">PSTN (つまり PBX) への通話をルーティングしないシステムに接続されているエンドポイントは、Location-Based ルーティングが有効になっているユーザーの Lync エンドポイントと同様の制限があります。</span><span class="sxs-lookup"><span data-stu-id="eb1a5-157">Endpoints that are connected to systems that do not route calls to the PSTN (i.e. a PBX) will have similar restrictions as Lync endpoints of users enabled for Location-Based Routing.</span></span> <span data-ttu-id="eb1a5-158">これは、ユーザーの場所に関係なく、ユーザーが Lync ユーザーとの間で通話を発信および受信できることを意味します。</span><span class="sxs-lookup"><span data-stu-id="eb1a5-158">This means that these users will be able to place and receive calls to and from Lync user regardless of the user’s location.</span></span> <span data-ttu-id="eb1a5-159">また、システムが関連付けられているネットワークサイトに関係なく、PSTN ネットワーク (つまり、別の PBX に接続されているエンドポイント) との間で着信を転送することができます。</span><span class="sxs-lookup"><span data-stu-id="eb1a5-159">They will also be able to place an receive calls to and from other systems that do not route calls to the PSTN network (i.e. an endpoint connected to a different PBX) regardless of the network site to which the system is associated.</span></span> <span data-ttu-id="eb1a5-160">PSTN エンドポイントを含むすべての着信通話、発信通話、通話転送、着信転送は Location-Based ルーティング enforcements の対象になります。</span><span class="sxs-lookup"><span data-stu-id="eb1a5-160">All inbound calls, outbound calls, call transfers and call forwarding involving PSTN endpoints will be subject to Location-Based Routing enforcements.</span></span> <span data-ttu-id="eb1a5-161">このような呼び出しでは、そのようなシステムのローカルとして定義されている PSTN ゲートウェイのみを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eb1a5-161">Such calls must use only PSTN gateways that are defined as local to such systems.</span></span>

<span data-ttu-id="eb1a5-162">次の表は、2つの異なるネットワークサイトでの4つの trunks のトランク構成を示しています。2つは PSTN ゲートウェイに接続され、2つは PBX システムに接続されています。</span><span class="sxs-lookup"><span data-stu-id="eb1a5-162">The following table illustrates the trunk configuration of four trunks in two different network sites: two connected to PSTN gateways and two connected to PBX systems.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eb1a5-163">名前</span><span class="sxs-lookup"><span data-stu-id="eb1a5-163">Name</span></span></th>
<th><span data-ttu-id="eb1a5-164">EnableLocationRestriction</span><span class="sxs-lookup"><span data-stu-id="eb1a5-164">EnableLocationRestriction</span></span></th>
<th><span data-ttu-id="eb1a5-165">NetworkSiteID</span><span class="sxs-lookup"><span data-stu-id="eb1a5-165">NetworkSiteID</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eb1a5-166">PstnGateway: トランク1の DEL-GW</span><span class="sxs-lookup"><span data-stu-id="eb1a5-166">PstnGateway:Trunk 1 DEL-GW</span></span></p></td>
<td><p><span data-ttu-id="eb1a5-167">True</span><span class="sxs-lookup"><span data-stu-id="eb1a5-167">True</span></span></p></td>
<td><p><span data-ttu-id="eb1a5-168">サイト 1 (ニューデリー)</span><span class="sxs-lookup"><span data-stu-id="eb1a5-168">Site 1 (Delhi)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb1a5-169">PstnGateway: トランク 2 HYD</span><span class="sxs-lookup"><span data-stu-id="eb1a5-169">PstnGateway:Trunk 2 HYD-GW</span></span></p></td>
<td><p><span data-ttu-id="eb1a5-170">True</span><span class="sxs-lookup"><span data-stu-id="eb1a5-170">True</span></span></p></td>
<td><p><span data-ttu-id="eb1a5-171">サイト 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="eb1a5-171">Site 2 (Hyderabad)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb1a5-172">PstnGateway: トランク 3 DEL-PBX</span><span class="sxs-lookup"><span data-stu-id="eb1a5-172">PstnGateway:Trunk 3 DEL-PBX</span></span></p></td>
<td><p><span data-ttu-id="eb1a5-173">False</span><span class="sxs-lookup"><span data-stu-id="eb1a5-173">False</span></span></p></td>
<td><p><span data-ttu-id="eb1a5-174">サイト 1 (ニューデリー)</span><span class="sxs-lookup"><span data-stu-id="eb1a5-174">Site 1 (Delhi)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb1a5-175">PstnGateway: トランク 4 HYD</span><span class="sxs-lookup"><span data-stu-id="eb1a5-175">PstnGateway:Trunk 4 HYD-PBX</span></span></p></td>
<td><p><span data-ttu-id="eb1a5-176">False</span><span class="sxs-lookup"><span data-stu-id="eb1a5-176">False</span></span></p></td>
<td><p><span data-ttu-id="eb1a5-177">サイト 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="eb1a5-177">Site 2 (Hyderabad)</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="enable-location-based-routing-to-voice-policies"></a><span data-ttu-id="eb1a5-178">ボイスポリシーへの Location-Based ルーティングを有効にする</span><span class="sxs-lookup"><span data-stu-id="eb1a5-178">Enable Location-Based Routing to Voice Policies</span></span>

<span data-ttu-id="eb1a5-179">特定のユーザーへの Location-Based ルーティングを適用するには、これらのユーザーの音声ポリシーを構成して、PSTN の有料電話がバイパスされないようにします。</span><span class="sxs-lookup"><span data-stu-id="eb1a5-179">To enforce Location-Based Routing to specific users, configure those users’ voice policy to prevent PSTN toll bypass.</span></span> <span data-ttu-id="eb1a5-180">Lync Server Windows PowerShell コマンドの CsVoicePolicy を使用して、新しい音声ポリシーを作成するか、既存のポリシーを使用する場合は CsVoicePolicy を使用して、PSTN の有料サービスのバイパスを防ぐことでルーティング Location-Based ルーティングを有効にします。</span><span class="sxs-lookup"><span data-stu-id="eb1a5-180">Use the Lync Server Windows PowerShell command, New-CsVoicePolicy, to create a new voice policy or Set-CsVoicePolicy, if using an existing policy, to enable Location-Based Routing by preventing PSTN toll bypass.</span></span>

    Set-CsVoicePolicy -Identity <voice policy ID> -PreventPSTNTollBypass <$true|$false>

<span data-ttu-id="eb1a5-181">詳細については、「 [New-CsVoicePolicy](https://docs.microsoft.com/powershell/module/skype/New-CsVoicePolicy)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="eb1a5-181">For more information, see [New-CsVoicePolicy](https://docs.microsoft.com/powershell/module/skype/New-CsVoicePolicy).</span></span>

<span data-ttu-id="eb1a5-182">この例では、次の表と Windows PowerShell コマンドを使用して、このシナリオで定義された、ニューデリーと Hyderabad のボイスポリシーに PSTN 有料電話のバイパスを防ぐことを示します。</span><span class="sxs-lookup"><span data-stu-id="eb1a5-182">For this example, the following table and Windows PowerShell commands illustrate enabling the prevention of PSTN toll bypass to the Delhi and Hyderabad voice policies defined in this scenario.</span></span> <span data-ttu-id="eb1a5-183">この表には、Location-Based ルーティングに固有の設定のみが含まれています。</span><span class="sxs-lookup"><span data-stu-id="eb1a5-183">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

    Set-CsVoicePolicy -Identity "Delhi voice policy" -PreventPSTNTollBypass $true
    Set-CsVoicePolicy -Identity "Hyderabad voice policy" -PreventPSTNTollBypass $true


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="eb1a5-184">ボイスポリシー1</span><span class="sxs-lookup"><span data-stu-id="eb1a5-184">Voice policy 1</span></span></th>
<th><span data-ttu-id="eb1a5-185">ボイスポリシー2</span><span class="sxs-lookup"><span data-stu-id="eb1a5-185">Voice policy 2</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eb1a5-186">ボイスポリシー ID</span><span class="sxs-lookup"><span data-stu-id="eb1a5-186">Voice policy ID</span></span></p></td>
<td><p><span data-ttu-id="eb1a5-187">ニューデリーのボイスポリシー</span><span class="sxs-lookup"><span data-stu-id="eb1a5-187">Delhi voice policy</span></span></p></td>
<td><p><span data-ttu-id="eb1a5-188">Hyderabad ボイスポリシー</span><span class="sxs-lookup"><span data-stu-id="eb1a5-188">Hyderabad voice policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb1a5-189">PSTN の使用状況</span><span class="sxs-lookup"><span data-stu-id="eb1a5-189">PSTN usages</span></span></p></td>
<td><p><span data-ttu-id="eb1a5-190">ニューデリー使用量, PBX Del usage, PBX Hyd usage</span><span class="sxs-lookup"><span data-stu-id="eb1a5-190">Delhi usage, PBX Del usage, PBX Hyd usage</span></span></p></td>
<td><p><span data-ttu-id="eb1a5-191">Hyderabad usage、PBX Hyd usage、PBX Del usage</span><span class="sxs-lookup"><span data-stu-id="eb1a5-191">Hyderabad usage, PBX Hyd usage, PBX Del usage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb1a5-192">PreventPSTNTollBypass</span><span class="sxs-lookup"><span data-stu-id="eb1a5-192">PreventPSTNTollBypass</span></span></p></td>
<td><p><span data-ttu-id="eb1a5-193">True</span><span class="sxs-lookup"><span data-stu-id="eb1a5-193">True</span></span></p></td>
<td><p><span data-ttu-id="eb1a5-194">True</span><span class="sxs-lookup"><span data-stu-id="eb1a5-194">True</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="enable-location-based-routing-in-the-routing-configuration"></a><span data-ttu-id="eb1a5-195">ルーティング構成で Location-Based ルーティングを有効にする</span><span class="sxs-lookup"><span data-stu-id="eb1a5-195">Enable Location-Based Routing in the routing configuration</span></span>

<span data-ttu-id="eb1a5-196">最後に、ルーティング構成への Location-Based ルーティングをグローバルに有効にします。</span><span class="sxs-lookup"><span data-stu-id="eb1a5-196">Finally, globally enable Location-Based Routing to your routing configuration.</span></span> <span data-ttu-id="eb1a5-197">Lync Server Windows PowerShell コマンドの [新しい-CsRoutingConfiguration] を使って Location-Based ルーティングを有効にします。</span><span class="sxs-lookup"><span data-stu-id="eb1a5-197">Use the Lync Server Windows PowerShell command, New-CsRoutingConfiguration, to enable Location-Based Routing.</span></span>

    Set-CsRoutingConfiguration -EnableLocationBasedRouting $true

<span data-ttu-id="eb1a5-198">詳細については、「 [CsRoutingConfiguration を設定](https://docs.microsoft.com/powershell/module/skype/Set-CsRoutingConfiguration)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="eb1a5-198">For more information, see [Set-CsRoutingConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsRoutingConfiguration).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="eb1a5-199">Location-Based ルーティングはグローバル構成で有効にする必要がありますが、適用されるルールのセットは、このドキュメントで指定されているように構成されているサイト、ユーザー、および trunks に対してのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="eb1a5-199">while Location-Based Routing must be enabled via a global configuration, the set of rules to be applied will only be enforced for the sites, users and trunks for which it has been configured as specified in this documentation.</span></span>



</div>

<div>


</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="eb1a5-200">関連項目</span><span class="sxs-lookup"><span data-stu-id="eb1a5-200">See Also</span></span>


[<span data-ttu-id="eb1a5-201">Lync Server 2013 の場所に基づくルーティングの構成</span><span class="sxs-lookup"><span data-stu-id="eb1a5-201">Configuring Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-configuring-location-based-routing.md)  
  

<span data-ttu-id="eb1a5-202"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="eb1a5-202"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

