---
title: 通話受付制御の要件を収集する例
description: 通話受付制御の要件を収集する例。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Example of gathering your requirements for call admission control
ms:assetid: 3363ac53-b7c4-4a59-aea1-b2f3ee016ae1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425827(v=OCS.15)
ms:contentKeyID: 48183820
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 25c0b450070bda62c2610d98cfff8c8cd16ad2af
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428499"
---
# <a name="example-gathering-your-requirements-for-call-admission-control-in-lync-server-2013"></a><span data-ttu-id="c3b05-103">例: Lync Server 2013 での通話受付制御の要件の収集</span><span class="sxs-lookup"><span data-stu-id="c3b05-103">Example: Gathering your requirements for call admission control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c3b05-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c3b05-104">

<span> </span></span></span>

<span data-ttu-id="c3b05-105">_**最終更新日:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="c3b05-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="c3b05-p101">この例では、通話受付管理 (CAC) の計画および実装方法を示します。これは大まかに次の作業で構成されます。</span><span class="sxs-lookup"><span data-stu-id="c3b05-p101">This example shows you how to plan for and implement call admission control (CAC). At a high level, this consists of the following activities:</span></span>

1.  <span data-ttu-id="c3b05-108">すべてのネットワーク ハブおよびバックボーン (*ネットワーク地域* とも呼ばれます) を特定します。</span><span class="sxs-lookup"><span data-stu-id="c3b05-108">Identify all of your network hubs and backbones (known as *network regions*).</span></span>

2.  <span data-ttu-id="c3b05-109">各ネットワーク領域の CAC を管理する Lync Server セントラルサイトを特定します。</span><span class="sxs-lookup"><span data-stu-id="c3b05-109">Identify the Lync Server central site that will manage CAC for each network region.</span></span>

3.  <span data-ttu-id="c3b05-110">各ネットワーク地域に接続される *ネットワーク サイト* を特定および定義します。</span><span class="sxs-lookup"><span data-stu-id="c3b05-110">Identify and define the *network sites* that are connected to each network region.</span></span>

4.  <span data-ttu-id="c3b05-111">WAN への接続に帯域幅の制約がある各ネットワークサイトについては、WAN 接続の帯域幅の容量と、ネットワーク管理者が Lync Server メディアトラフィック用に設定した帯域幅制限 (該当する場合) について説明します。</span><span class="sxs-lookup"><span data-stu-id="c3b05-111">For each network site whose connection to the WAN is bandwidth-constrained, describe the bandwidth capacity of the WAN connection and the bandwidth limits that to the network administrator has set for Lync Server media traffic, if applicable.</span></span> <span data-ttu-id="c3b05-112">WAN への接続に帯域幅の制限がないサイトは含める必要はありません。</span><span class="sxs-lookup"><span data-stu-id="c3b05-112">You do not need to include sites whose connection to the WAN is not bandwidth-constrained.</span></span>

5.  <span data-ttu-id="c3b05-113">ネットワークの各サブネットをネットワーク サイトに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="c3b05-113">Associate each subnet in your network with a network site.</span></span>

6.  <span data-ttu-id="c3b05-114">ネットワーク地域間のリンクをマップします。</span><span class="sxs-lookup"><span data-stu-id="c3b05-114">Map the links between the network regions.</span></span> <span data-ttu-id="c3b05-115">各リンクについて、帯域幅の容量と、ネットワーク管理者が Lync Server メディアトラフィックに使用した制限事項について説明します。</span><span class="sxs-lookup"><span data-stu-id="c3b05-115">For each link, describe its bandwidth capacity and any limits that the network administrator has placed on Lync Server media traffic.</span></span>

7.  <span data-ttu-id="c3b05-116">ネットワーク地域のすべてのペア間のルートを定義します。</span><span class="sxs-lookup"><span data-stu-id="c3b05-116">Define a route between every pair of network regions.</span></span>

<div>

## <a name="gather-the-required-information"></a><span data-ttu-id="c3b05-117">必要な情報の収集</span><span class="sxs-lookup"><span data-stu-id="c3b05-117">Gather the Required Information</span></span>

<span data-ttu-id="c3b05-118">通話受付管理の準備を行うには、次の手順で示されている情報を収集します。</span><span class="sxs-lookup"><span data-stu-id="c3b05-118">To prepare for call admission control, gather the information described in the following steps:</span></span>

1.  <span data-ttu-id="c3b05-p104">ネットワーク地域を特定します。ネットワーク地域とは、ネットワーク バックボーンまたはネットワーク ハブを示します。</span><span class="sxs-lookup"><span data-stu-id="c3b05-p104">Identify your network regions. A network region represents a network backbone or a network hub.</span></span>
    
    <span data-ttu-id="c3b05-p105">ネットワーク バックボーンまたはネットワーク ハブとは、異なる LAN またはサブネット間の情報交換用パスを提供して、ネットワークのさまざまな部分を相互接続するコンピューター ネットワーク インフラストラクチャの一部です。バックボーンは、小規模ロケーションから地理的に広範囲な地域まで、さまざまなネットワークを繋ぐことができます。通常、バックボーンの処理能力はバックボーンに接続するネットワークの処理能力よりも高くなっています。</span><span class="sxs-lookup"><span data-stu-id="c3b05-p105">A network backbone or a network hub is a part of computer network infrastructure that interconnects various pieces of network, providing a path for the exchange of information between different LANs or subnets. A backbone can tie together diverse networks, from a small location to a wide geographic area. The backbone's capacity is typically greater than that of the networks connected to it.</span></span>
    
    <span data-ttu-id="c3b05-p106">このトポロジ例では、北アメリカ、EMEA、および APAC の 3 つのネットワーク地域が存在します。 ネットワーク地域にはネットワーク サイトのコレクションが含まれます。 ネットワーク管理者と協力して、組織のネットワーク地域を定義します。</span><span class="sxs-lookup"><span data-stu-id="c3b05-p106">Our example topology has three network regions: North America, EMEA, and APAC. A network region contains a collection of network sites. Work with your network administrator to define the network regions for your enterprise.</span></span>

2.  <span data-ttu-id="c3b05-127">各ネットワーク地域が関連付けられている中央サイトを特定します。</span><span class="sxs-lookup"><span data-stu-id="c3b05-127">Identify each network region’s associated central site.</span></span> <span data-ttu-id="c3b05-128">セントラルサイトには、少なくとも1つのフロントエンドサーバーが含まれています。また、ネットワーク領域の WAN 接続を通過するすべてのメディアトラフィックで CAC を管理する Lync Server 展開です。</span><span class="sxs-lookup"><span data-stu-id="c3b05-128">A central site contains at least one Front End Server and is the Lync Server deployment that will manage CAC for all media traffic that passes through the network region’s WAN connection.</span></span>
    
    <span data-ttu-id="c3b05-129">**3 つのネットワーク地域に分けられたエンタープライズ ネットワークの例**</span><span class="sxs-lookup"><span data-stu-id="c3b05-129">**An example enterprise network divided into three network regions**</span></span>
    
    <span data-ttu-id="c3b05-130">![3 つのネットワーク地域が含まれるネットワーク トポロジの例](images/Gg425827.08937347-250f-488f-ba5f-c256e6afcd8b(OCS.15).jpg "3 つのネットワーク地域が含まれるネットワーク トポロジの例")</span><span class="sxs-lookup"><span data-stu-id="c3b05-130">![Network Topology Example with 3 Network Regions](images/Gg425827.08937347-250f-488f-ba5f-c256e6afcd8b(OCS.15).jpg "Network Topology Example with 3 Network Regions")</span></span>  
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="c3b05-131">Multiprotocol Label Switching (MPLS) ネットワークは、それぞれの地理的な場所が対応するネットワーク サイトを有する、ネットワーク地域として表される必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3b05-131">A Multiprotocol Label Switching (MPLS) network should be represented as a network region in which each geographic location has a corresponding network site.</span></span> <span data-ttu-id="c3b05-132">詳細については、計画ドキュメントの「<A href="lync-server-2013-call-admission-control-on-an-mpls-network.md">MPLS ネットワークでの、Lync Server 2013 による通話受付制御</A>」トピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c3b05-132">For details, see the “<A href="lync-server-2013-call-admission-control-on-an-mpls-network.md">Call admission control on an MPLS network with Lync Server 2013</A>” topic in the Planning documentation.</span></span>

    
    </div>
    
    <span data-ttu-id="c3b05-133">上記のネットワークトポロジの例では、3つのネットワーク領域があります。それぞれに、CAC を管理する Lync Server セントラルサイトがあります。</span><span class="sxs-lookup"><span data-stu-id="c3b05-133">In the preceding example network topology, there are three network regions, each with a Lync Server central site that manages CAC.</span></span> <span data-ttu-id="c3b05-134">ネットワーク地域の適切な中央サイトは、地理的な近さによって選択されます。</span><span class="sxs-lookup"><span data-stu-id="c3b05-134">The appropriate central site for a network region is chosen by the geographic vicinity.</span></span> <span data-ttu-id="c3b05-135">メディア トラフィックはネットワーク地域内で最も重くなるため、所有権が地理的な近さで決まることで自己完結型となり、その他の中央サイトが使用できなくなった場合でも、機能し続けます。</span><span class="sxs-lookup"><span data-stu-id="c3b05-135">Because media traffic will be heaviest within network regions, the ownership by geographic vicinity makes it self-contained and will continue to be functional even if other central sites become unavailable.</span></span>
    
    <span data-ttu-id="c3b05-136">この例では、シカゴという名前の Lync Server 展開は北米地域のセントラルサイトです。</span><span class="sxs-lookup"><span data-stu-id="c3b05-136">In this example, a Lync Server deployment named Chicago is the central site for the North America region.</span></span>
    
    <span data-ttu-id="c3b05-137">北米のすべての Lync ユーザーは、シカゴの展開でサーバーに所属しています。</span><span class="sxs-lookup"><span data-stu-id="c3b05-137">All Lync users in North America are homed on servers in the Chicago deployment.</span></span> <span data-ttu-id="c3b05-138">次の表に 3 つすべてのネットワーク地域の中央サイトを示します。</span><span class="sxs-lookup"><span data-stu-id="c3b05-138">The following table shows central sites for all three network regions.</span></span>
    
    ### <a name="network-regions-and-their-associated-central-sites"></a><span data-ttu-id="c3b05-139">ネットワーク地域と関連付けられた中央サイト</span><span class="sxs-lookup"><span data-stu-id="c3b05-139">Network Regions and their Associated Central Sites</span></span>
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="c3b05-140">ネットワーク地域</span><span class="sxs-lookup"><span data-stu-id="c3b05-140">Network Region</span></span></th>
    <th><span data-ttu-id="c3b05-141">中央サイト</span><span class="sxs-lookup"><span data-stu-id="c3b05-141">Central Site</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="c3b05-142">北アメリカ</span><span class="sxs-lookup"><span data-stu-id="c3b05-142">North America</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-143">シカゴ</span><span class="sxs-lookup"><span data-stu-id="c3b05-143">Chicago</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="c3b05-144">EMEA</span><span class="sxs-lookup"><span data-stu-id="c3b05-144">EMEA</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-145">ロンドン</span><span class="sxs-lookup"><span data-stu-id="c3b05-145">London</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="c3b05-146">APAC</span><span class="sxs-lookup"><span data-stu-id="c3b05-146">APAC</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-147">北京</span><span class="sxs-lookup"><span data-stu-id="c3b05-147">Beijing</span></span></p></td>
    </tr>
    </tbody>
    </table>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="c3b05-148">Lync Server のトポロジによっては、同じセントラルサイトを複数のネットワーク領域に割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="c3b05-148">Depending on your Lync Server topology, the same central site can be assigned to multiple network regions.</span></span>

    
    </div>

3.  <span data-ttu-id="c3b05-p111">それぞれのネットワーク地域で、帯域幅に制限がない WAN 接続を有するネットワーク サイト (オフィスまたは場所) すべてを特定します。 これらのサイトは帯域幅の制限がないため、CAC 帯域幅ポリシーを適用する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="c3b05-p111">For each network region, identify all of the network sites (offices or locations) whose WAN connections are not bandwidth-constrained. Because these sites are not bandwidth constrained, you do not need to apply CAC bandwidth policies to them.</span></span>
    
    <span data-ttu-id="c3b05-151">次の表に示されている例では、3 つのネットワーク サイトには帯域幅の制限がある WAN リンクがありません: ニューヨーク、シカゴ、およびデトロイト。</span><span class="sxs-lookup"><span data-stu-id="c3b05-151">In the example shown in the following table, three network sites do not have bandwidth-constrained WAN links: New York, Chicago, and Detroit.</span></span>
    
    ### <a name="network-sites-not-constrained-by-wan-bandwidth"></a><span data-ttu-id="c3b05-152">WAN 帯域幅による制限がないネットワーク サイト</span><span class="sxs-lookup"><span data-stu-id="c3b05-152">Network Sites not Constrained by WAN Bandwidth</span></span>
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="c3b05-153">ネットワーク サイト</span><span class="sxs-lookup"><span data-stu-id="c3b05-153">Network Site</span></span></th>
    <th><span data-ttu-id="c3b05-154">ネットワーク地域</span><span class="sxs-lookup"><span data-stu-id="c3b05-154">Network Region</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="c3b05-155">ニューヨーク</span><span class="sxs-lookup"><span data-stu-id="c3b05-155">New York</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-156">北アメリカ</span><span class="sxs-lookup"><span data-stu-id="c3b05-156">North America</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="c3b05-157">シカゴ</span><span class="sxs-lookup"><span data-stu-id="c3b05-157">Chicago</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-158">北アメリカ</span><span class="sxs-lookup"><span data-stu-id="c3b05-158">North America</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="c3b05-159">デトロイト</span><span class="sxs-lookup"><span data-stu-id="c3b05-159">Detroit</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-160">北アメリカ</span><span class="sxs-lookup"><span data-stu-id="c3b05-160">North America</span></span></p></td>
    </tr>
    </tbody>
    </table>


4.  <span data-ttu-id="c3b05-161">それぞれのネットワーク地域で、帯域幅の制限がある WAN リンクを介してネットワーク地域に接続しているすべてのネットワーク サイトを特定します。</span><span class="sxs-lookup"><span data-stu-id="c3b05-161">For each network region, identify all of the network sites that connect to the network region through bandwidth-constrained WAN links.</span></span>
    
    <span data-ttu-id="c3b05-162">音声およびビデオの品質を確実なものにできるように、これらの帯域幅の制限があるネットワーク サイトは、WAN を監視し、ネットワーク地域への、およびネットワーク地域からのメディア (音声またはビデオ) トラフィック フローを制限する CAC 帯域幅ポリシーを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="c3b05-162">To help ensure audio and video quality, we recommend that these bandwidth-constrained network sites have their WANs monitored and CAC bandwidth policies that limit media (voice or video) traffic flow to and from the network region.</span></span>
    
    <span data-ttu-id="c3b05-163">次の表に示されている例では、WAN 帯域幅による制限がある 3 つのネットワーク サイトが存在します。 ポートランド、リノ、およびアルバカーキ。</span><span class="sxs-lookup"><span data-stu-id="c3b05-163">In the example shown in the following table, there are three network sites that are constrained by WAN bandwidth: Portland, Reno and Albuquerque.</span></span>
    
    ### <a name="network-sites-constrained-by-wan-bandwidth"></a><span data-ttu-id="c3b05-164">WAN 帯域幅による制限があるネットワーク サイト</span><span class="sxs-lookup"><span data-stu-id="c3b05-164">Network Sites Constrained by WAN Bandwidth</span></span>
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="c3b05-165">ネットワーク サイト</span><span class="sxs-lookup"><span data-stu-id="c3b05-165">Network Site</span></span></th>
    <th><span data-ttu-id="c3b05-166">ネットワーク地域</span><span class="sxs-lookup"><span data-stu-id="c3b05-166">Network Region</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="c3b05-167">アルバカーキ</span><span class="sxs-lookup"><span data-stu-id="c3b05-167">Albuquerque</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-168">北アメリカ</span><span class="sxs-lookup"><span data-stu-id="c3b05-168">North America</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="c3b05-169">リノ</span><span class="sxs-lookup"><span data-stu-id="c3b05-169">Reno</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-170">北アメリカ</span><span class="sxs-lookup"><span data-stu-id="c3b05-170">North America</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="c3b05-171">ポートランド</span><span class="sxs-lookup"><span data-stu-id="c3b05-171">Portland</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-172">北アメリカ</span><span class="sxs-lookup"><span data-stu-id="c3b05-172">North America</span></span></p></td>
    </tr>
    </tbody>
    </table>
    
    <span data-ttu-id="c3b05-173">**帯域幅の制限がない 3 つのネットワーク サイト (シカゴ、ニューヨーク、デトロイト) および WAN 帯域幅の制限がある 3 つのネットワーク サイト (ポートランド、リノ、アルバカーキ) を持つ CAC ネットワーク地域、北アメリカ**</span><span class="sxs-lookup"><span data-stu-id="c3b05-173">**CAC network region North America with three network sites that are unconstrained by bandwidth (Chicago, New York, and Detroit) and three network sites that are constrained by WAN bandwidth (Portland, Reno, and Albuquerque)**</span></span>
    
    <span data-ttu-id="c3b05-174">![WAN 帯域幅による制限があるネットワーク サイトの例](images/Gg425827.d9d1f231-db4d-4dd7-8fbc-eb0b6d1e705d(OCS.15).jpg "WAN 帯域幅による制限があるネットワーク サイトの例")</span><span class="sxs-lookup"><span data-stu-id="c3b05-174">![Example network sites constrained by WAN bandwidth](images/Gg425827.d9d1f231-db4d-4dd7-8fbc-eb0b6d1e705d(OCS.15).jpg "Example network sites constrained by WAN bandwidth")</span></span>  

5.  <span data-ttu-id="c3b05-175">帯域幅の制限がある WAN リンクに対して、次の項目を決定します。</span><span class="sxs-lookup"><span data-stu-id="c3b05-175">For each bandwidth-constrained WAN link, determine the following:</span></span>
    
      - <span data-ttu-id="c3b05-176">すべての同時音声セッションに対して設定する全体的な帯域幅制限。</span><span class="sxs-lookup"><span data-stu-id="c3b05-176">Overall bandwidth limit that you want to set for all concurrent audio sessions.</span></span> <span data-ttu-id="c3b05-177">新しいオーディオセッションによってこの制限を超過すると、Lync Server ではセッションの開始が許可されません。</span><span class="sxs-lookup"><span data-stu-id="c3b05-177">If a new audio session will cause this limit to be exceeded, Lync Server does not allow the session to start.</span></span>
    
      - <span data-ttu-id="c3b05-178">個々のオーディオセッションごとに設定する帯域幅の制限。</span><span class="sxs-lookup"><span data-stu-id="c3b05-178">Bandwidth limit that you want to set for each individual audio session.</span></span> <span data-ttu-id="c3b05-179">既定の CAC 帯域幅制限は 175 kbps ですが、管理者が変更することができます。</span><span class="sxs-lookup"><span data-stu-id="c3b05-179">The default CAC bandwidth limit is 175 kbps, but it can be modified by the administrator.</span></span>
    
      - <span data-ttu-id="c3b05-180">すべての同時ビデオセッションに対して設定する全体的な帯域幅制限。</span><span class="sxs-lookup"><span data-stu-id="c3b05-180">Overall bandwidth limit that you want to set for all concurrent video sessions.</span></span> <span data-ttu-id="c3b05-181">新しいビデオセッションによってこの制限を超過する場合、Lync Server ではセッションの開始が許可されません。</span><span class="sxs-lookup"><span data-stu-id="c3b05-181">If a new video session will cause this limit to be exceeded, Lync Server does not allow the session to start.</span></span>
    
      - <span data-ttu-id="c3b05-182">個々のビデオセッションに対して設定する帯域幅の制限。</span><span class="sxs-lookup"><span data-stu-id="c3b05-182">Bandwidth limit that you want to set for each individual video session.</span></span> <span data-ttu-id="c3b05-183">既定の CAC 帯域幅制限は 700 kbps ですが、管理者が変更することができます。</span><span class="sxs-lookup"><span data-stu-id="c3b05-183">The default CAC bandwidth limit is 700 kbps, but it can be modified by the administrator.</span></span>
    
    ### <a name="network-sites-with-wan-bandwidth-constraint-information-bandwidth-in-kbps"></a><span data-ttu-id="c3b05-184">WAN 帯域幅の制約情報 (kbps の帯域幅) を備えたネットワークサイト</span><span class="sxs-lookup"><span data-stu-id="c3b05-184">Network Sites with WAN Bandwidth Constraint Information (Bandwidth in kbps)</span></span>
    
    <table style="width:100%;">
    <colgroup>
    <col style="width: 14%" />
    <col style="width: 14%" />
    <col style="width: 14%" />
    <col style="width: 14%" />
    <col style="width: 14%" />
    <col style="width: 14%" />
    <col style="width: 14%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="c3b05-185">ネットワーク サイト</span><span class="sxs-lookup"><span data-stu-id="c3b05-185">Network Site</span></span></th>
    <th><span data-ttu-id="c3b05-186">ネットワーク地域</span><span class="sxs-lookup"><span data-stu-id="c3b05-186">Network Region</span></span></th>
    <th><span data-ttu-id="c3b05-187">BW Limit</span><span class="sxs-lookup"><span data-stu-id="c3b05-187">BW Limit</span></span></th>
    <th><span data-ttu-id="c3b05-188">オーディオ制限</span><span class="sxs-lookup"><span data-stu-id="c3b05-188">Audio Limit</span></span></th>
    <th><span data-ttu-id="c3b05-189">オーディオセッションの制限</span><span class="sxs-lookup"><span data-stu-id="c3b05-189">Audio Session Limit</span></span></th>
    <th><span data-ttu-id="c3b05-190">ビデオの制限</span><span class="sxs-lookup"><span data-stu-id="c3b05-190">Video Limit</span></span></th>
    <th><span data-ttu-id="c3b05-191">ビデオセッションの制限</span><span class="sxs-lookup"><span data-stu-id="c3b05-191">Video Session Limit</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="c3b05-192">アルバカーキ</span><span class="sxs-lookup"><span data-stu-id="c3b05-192">Albuquerque</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-193">北アメリカ</span><span class="sxs-lookup"><span data-stu-id="c3b05-193">North America</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-194">5,000</span><span class="sxs-lookup"><span data-stu-id="c3b05-194">5,000</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-195">2000</span><span class="sxs-lookup"><span data-stu-id="c3b05-195">2,000</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-196">175</span><span class="sxs-lookup"><span data-stu-id="c3b05-196">175</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-197">1400</span><span class="sxs-lookup"><span data-stu-id="c3b05-197">1,400</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-198">700</span><span class="sxs-lookup"><span data-stu-id="c3b05-198">700</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="c3b05-199">リノ</span><span class="sxs-lookup"><span data-stu-id="c3b05-199">Reno</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-200">北アメリカ</span><span class="sxs-lookup"><span data-stu-id="c3b05-200">North America</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-201">10,000</span><span class="sxs-lookup"><span data-stu-id="c3b05-201">10,000</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-202">4000</span><span class="sxs-lookup"><span data-stu-id="c3b05-202">4,000</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-203">175</span><span class="sxs-lookup"><span data-stu-id="c3b05-203">175</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-204">2800</span><span class="sxs-lookup"><span data-stu-id="c3b05-204">2,800</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-205">700</span><span class="sxs-lookup"><span data-stu-id="c3b05-205">700</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="c3b05-206">ポートランド</span><span class="sxs-lookup"><span data-stu-id="c3b05-206">Portland</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-207">北アメリカ</span><span class="sxs-lookup"><span data-stu-id="c3b05-207">North America</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-208">5,000</span><span class="sxs-lookup"><span data-stu-id="c3b05-208">5,000</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-209">4000</span><span class="sxs-lookup"><span data-stu-id="c3b05-209">4,000</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-210">175</span><span class="sxs-lookup"><span data-stu-id="c3b05-210">175</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-211">2800</span><span class="sxs-lookup"><span data-stu-id="c3b05-211">2,800</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-212">700</span><span class="sxs-lookup"><span data-stu-id="c3b05-212">700</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="c3b05-213">ニューヨーク</span><span class="sxs-lookup"><span data-stu-id="c3b05-213">New York</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-214">北アメリカ</span><span class="sxs-lookup"><span data-stu-id="c3b05-214">North America</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-215">(制限なし)</span><span class="sxs-lookup"><span data-stu-id="c3b05-215">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-216">(制限なし)</span><span class="sxs-lookup"><span data-stu-id="c3b05-216">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-217">(制限なし)</span><span class="sxs-lookup"><span data-stu-id="c3b05-217">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-218">(制限なし)</span><span class="sxs-lookup"><span data-stu-id="c3b05-218">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-219">(制限なし)</span><span class="sxs-lookup"><span data-stu-id="c3b05-219">(no limit)</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="c3b05-220">シカゴ</span><span class="sxs-lookup"><span data-stu-id="c3b05-220">Chicago</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-221">北アメリカ</span><span class="sxs-lookup"><span data-stu-id="c3b05-221">North America</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-222">(制限なし)</span><span class="sxs-lookup"><span data-stu-id="c3b05-222">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-223">(制限なし)</span><span class="sxs-lookup"><span data-stu-id="c3b05-223">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-224">(制限なし)</span><span class="sxs-lookup"><span data-stu-id="c3b05-224">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-225">(制限なし)</span><span class="sxs-lookup"><span data-stu-id="c3b05-225">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-226">(制限なし)</span><span class="sxs-lookup"><span data-stu-id="c3b05-226">(no limit)</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="c3b05-227">デトロイト</span><span class="sxs-lookup"><span data-stu-id="c3b05-227">Detroit</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-228">北アメリカ</span><span class="sxs-lookup"><span data-stu-id="c3b05-228">North America</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-229">(制限なし)</span><span class="sxs-lookup"><span data-stu-id="c3b05-229">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-230">(制限なし)</span><span class="sxs-lookup"><span data-stu-id="c3b05-230">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-231">(制限なし)</span><span class="sxs-lookup"><span data-stu-id="c3b05-231">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-232">(制限なし)</span><span class="sxs-lookup"><span data-stu-id="c3b05-232">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-233">(制限なし)</span><span class="sxs-lookup"><span data-stu-id="c3b05-233">(no limit)</span></span></p></td>
    </tr>
    </tbody>
    </table>


6.  <span data-ttu-id="c3b05-234">ネットワーク内のすべてのサブネットについて、関連付けられたネットワークサイトを指定します。</span><span class="sxs-lookup"><span data-stu-id="c3b05-234">For every subnet in your network, specify its associated network site.</span></span>
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="c3b05-235">ネットワークサイトが帯域幅の制約を受けていない場合でも、ネットワーク内のすべてのサブネットがネットワークサイトと関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3b05-235">Every subnet in your network must be associated with a network site, even if the network site is not bandwidth constrained.</span></span> <span data-ttu-id="c3b05-236">これは、通話受付制御がサブネット情報を使用して、どのネットワークサイトでエンドポイントが配置されているかを判断するためです。</span><span class="sxs-lookup"><span data-stu-id="c3b05-236">This is because call admission control uses subnet information to determine at which network site an endpoint is located.</span></span> <span data-ttu-id="c3b05-237">セッションの両方の当事者の場所が決定されると、通話受付制御によって、通話を確立するための十分な帯域幅があるかどうかを判断できます。</span><span class="sxs-lookup"><span data-stu-id="c3b05-237">When the locations of both parties in the session are determined, call admission control can determine if there is sufficient bandwidth to establish a call.</span></span> <span data-ttu-id="c3b05-238">帯域幅の制限がないリンクを経由してセッションが確立されると、通知が生成されます。</span><span class="sxs-lookup"><span data-stu-id="c3b05-238">When a session is established over a link that has no bandwidth limits, an alert is generated.</span></span><BR><span data-ttu-id="c3b05-239">オーディオ/ビデオエッジサーバーを展開する場合、各エッジサーバーのパブリック IP アドレスが、エッジサーバーが展開されているネットワークサイトと関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3b05-239">If you deploy Audio/Video Edge Servers, the public IP addresses of each Edge Server must be associated with the network site where the Edge Server is deployed.</span></span> <span data-ttu-id="c3b05-240">A/V エッジサーバーの各パブリック IP アドレスは、サブネットマスクが32のサブネットとして、ネットワーク構成の設定に追加されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3b05-240">Each public IP address of the A/V Edge Server must be added to your network configuration settings as a subnet with a subnet mask of 32.</span></span> <span data-ttu-id="c3b05-241">たとえば、シカゴに A/V エッジサーバーを展開している場合、それらのサーバーの各外部 IP アドレスに対して、サブネットマスク32を持つサブネットを作成し、そのサブネットにネットワークサイトシカゴを関連付けます。</span><span class="sxs-lookup"><span data-stu-id="c3b05-241">For example, if you deploy A/V Edge Servers in Chicago, then for each external IP address of those servers create a subnet with a subnet mask of 32 and associate network site Chicago with those subnets.</span></span> <span data-ttu-id="c3b05-242">パブリック IP アドレスの詳細については、計画ドキュメントの「 <A href="lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md">Lync Server 2013 の外部の A/V ファイアウォールとポートの要件を確認</A> する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c3b05-242">For details about public IP addresses, see <A href="lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md">Determine external A/V firewall and port requirements for Lync Server 2013</A> in the Planning documentation.</span></span>

    
    </div>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="c3b05-243">ネットワークに存在するが、サブネットに関連付けられていない、または IP アドレスを含むサブネットがネットワークサイトに関連付けられていない IP アドレスのリストを指定して、キー正常性インジケータ (KHI) アラートが発生します。</span><span class="sxs-lookup"><span data-stu-id="c3b05-243">A Key Health Indicator (KHI) alert is raised, specifying a list of IP addresses that are present in your network but are either not associated with a subnet, or the subnet that includes the IP addresses is not associated with a network site.</span></span> <span data-ttu-id="c3b05-244">このアラートは8時間以内に複数回発生することはありません。</span><span class="sxs-lookup"><span data-stu-id="c3b05-244">This alert will not be raised more than once within an 8 hour period.</span></span> <span data-ttu-id="c3b05-245">関連する通知情報と例を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="c3b05-245">The relevant alert information and an example are as follows:</span></span><BR><span data-ttu-id="c3b05-246"><STRONG>ソース:</STRONG> CS 帯域幅ポリシーサービス (コア)</span><span class="sxs-lookup"><span data-stu-id="c3b05-246"><STRONG>Source:</STRONG> CS Bandwidth Policy Service (Core)</span></span><BR><span data-ttu-id="c3b05-247"><STRONG>イベント番号:</STRONG> 36034</span><span class="sxs-lookup"><span data-stu-id="c3b05-247"><STRONG>Event number:</STRONG> 36034</span></span><BR><span data-ttu-id="c3b05-248"><STRONG>レベル:</STRONG> 2</span><span class="sxs-lookup"><span data-stu-id="c3b05-248"><STRONG>Level:</STRONG> 2</span></span><BR><span data-ttu-id="c3b05-249"><STRONG>説明:</STRONG> 次の IP アドレスのサブネット: &lt; Ip アドレスの一覧 &gt; が構成されていないか、サブネットがネットワークサイトに関連付けられていません。</span><span class="sxs-lookup"><span data-stu-id="c3b05-249"><STRONG>Description:</STRONG> The subnets for the following IP Addresses: &lt;List of IP Addresses&gt; are either not configured or the subnets are not associated to a network site.</span></span><BR><span data-ttu-id="c3b05-250"><STRONG>原因:</STRONG> 対応する IP アドレスのサブネットがネットワーク構成の設定で見つからないか、サブネットがネットワークサイトに関連付けられていません。</span><span class="sxs-lookup"><span data-stu-id="c3b05-250"><STRONG>Cause:</STRONG> The subnets for the corresponding IP addresses are missing from the network configuration settings or the subnets are not associated to a network site.</span></span><BR><span data-ttu-id="c3b05-251"><STRONG>解像度:</STRONG> 上記の IP アドレスの一覧に対応するサブネットをネットワーク構成の設定に追加し、すべてのサブネットをネットワークサイトに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="c3b05-251"><STRONG>Resolution:</STRONG> Add subnets corresponding to the preceding list of IP addresses into the network configuration settings and associate every subnet to a network site.</span></span><BR><span data-ttu-id="c3b05-252">たとえば、アラートの IP アドレス一覧に10.121.248.226 と10.121.249.20 が指定されている場合、これらの IP アドレスはサブネットに関連付けられていないか、または関連付けられているサブネットがネットワークサイトに属していません。</span><span class="sxs-lookup"><span data-stu-id="c3b05-252">For example, if the IP address list in the alert specifies 10.121.248.226 and 10.121.249.20, either these IP addresses are not associated with a subnet, or the subnet that they are associated with does not belong to a network site.</span></span> <span data-ttu-id="c3b05-253">10.121.248.0/24 および 10.121.249.0/24 がこれらのアドレスに対応するサブネットである場合、次の手順でこの問題を解決することができます。</span><span class="sxs-lookup"><span data-stu-id="c3b05-253">If 10.121.248.0/24 and 10.121.249.0/24 are the corresponding subnets for these addresses, you can resolve this issue as follows:</span></span> 
    > <OL>
    > <LI>
    > <P><span data-ttu-id="c3b05-254">IP アドレス 10.121.248.226 が 10.121.248.0/24 サブネットに関連付けられていること、および IP アドレス 10.121.249.20 が 10.121.249.0/24 サブネットに関連付けられていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c3b05-254">Be sure that IP address 10.121.248.226 is associated with the 10.121.248.0/24 subnet and IP address 10.121.249.20 is associated with the 10.121.249.0/24 subnet.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="c3b05-255">10.121.248.0/24 および 10.121.249.0/24 サブネットがそれぞれネットワーク サイトに関連付けられていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c3b05-255">Be sure that the 10.121.248.0/24 and 10.121.249.0/24 subnets are each associated with a network site.</span></span></P></LI></OL>

    
    </div>
    
    ### <a name="network-sites-and-associated-subnets-bandwidth-in-kbps"></a><span data-ttu-id="c3b05-256">ネットワークサイトと関連サブネット (kbps の帯域幅)</span><span class="sxs-lookup"><span data-stu-id="c3b05-256">Network Sites and Associated Subnets (Bandwidth in kbps)</span></span>
    
    <table>
    <colgroup>
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="c3b05-257">ネットワーク サイト</span><span class="sxs-lookup"><span data-stu-id="c3b05-257">Network Site</span></span></th>
    <th><span data-ttu-id="c3b05-258">ネットワーク地域</span><span class="sxs-lookup"><span data-stu-id="c3b05-258">Network Region</span></span></th>
    <th><span data-ttu-id="c3b05-259">BW Limit</span><span class="sxs-lookup"><span data-stu-id="c3b05-259">BW Limit</span></span></th>
    <th><span data-ttu-id="c3b05-260">オーディオ制限</span><span class="sxs-lookup"><span data-stu-id="c3b05-260">Audio Limit</span></span></th>
    <th><span data-ttu-id="c3b05-261">オーディオセッションの制限</span><span class="sxs-lookup"><span data-stu-id="c3b05-261">Audio Session Limit</span></span></th>
    <th><span data-ttu-id="c3b05-262">ビデオの制限</span><span class="sxs-lookup"><span data-stu-id="c3b05-262">Video Limit</span></span></th>
    <th><span data-ttu-id="c3b05-263">ビデオセッションの制限</span><span class="sxs-lookup"><span data-stu-id="c3b05-263">Video Session Limit</span></span></th>
    <th><span data-ttu-id="c3b05-264">サブネット</span><span class="sxs-lookup"><span data-stu-id="c3b05-264">Subnets</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="c3b05-265">アルバカーキ</span><span class="sxs-lookup"><span data-stu-id="c3b05-265">Albuquerque</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-266">北アメリカ</span><span class="sxs-lookup"><span data-stu-id="c3b05-266">North America</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-267">5,000</span><span class="sxs-lookup"><span data-stu-id="c3b05-267">5,000</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-268">2000</span><span class="sxs-lookup"><span data-stu-id="c3b05-268">2,000</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-269">175</span><span class="sxs-lookup"><span data-stu-id="c3b05-269">175</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-270">1400</span><span class="sxs-lookup"><span data-stu-id="c3b05-270">1,400</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-271">700</span><span class="sxs-lookup"><span data-stu-id="c3b05-271">700</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-272">172.29.79.0/23、157.57.215.0/25、172.29.90.0/23、172.29.80.0/24</span><span class="sxs-lookup"><span data-stu-id="c3b05-272">172.29.79.0/23, 157.57.215.0/25, 172.29.90.0/23, 172.29.80.0/24</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="c3b05-273">リノ</span><span class="sxs-lookup"><span data-stu-id="c3b05-273">Reno</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-274">北アメリカ</span><span class="sxs-lookup"><span data-stu-id="c3b05-274">North America</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-275">10,000</span><span class="sxs-lookup"><span data-stu-id="c3b05-275">10,000</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-276">4000</span><span class="sxs-lookup"><span data-stu-id="c3b05-276">4,000</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-277">175</span><span class="sxs-lookup"><span data-stu-id="c3b05-277">175</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-278">2800</span><span class="sxs-lookup"><span data-stu-id="c3b05-278">2,800</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-279">700</span><span class="sxs-lookup"><span data-stu-id="c3b05-279">700</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-280">157.57.210.0/23、172.28.151.128、25</span><span class="sxs-lookup"><span data-stu-id="c3b05-280">157.57.210.0/23, 172.28.151.128/25</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="c3b05-281">ポートランド</span><span class="sxs-lookup"><span data-stu-id="c3b05-281">Portland</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-282">北アメリカ</span><span class="sxs-lookup"><span data-stu-id="c3b05-282">North America</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-283">5,000</span><span class="sxs-lookup"><span data-stu-id="c3b05-283">5,000</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-284">4000</span><span class="sxs-lookup"><span data-stu-id="c3b05-284">4,000</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-285">175</span><span class="sxs-lookup"><span data-stu-id="c3b05-285">175</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-286">2800</span><span class="sxs-lookup"><span data-stu-id="c3b05-286">2,800</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-287">700</span><span class="sxs-lookup"><span data-stu-id="c3b05-287">700</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-288">172.29.77.0/24 10.71.108.0/24、157.57.208.0/23</span><span class="sxs-lookup"><span data-stu-id="c3b05-288">172.29.77.0/24 10.71.108.0/24, 157.57.208.0/23</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="c3b05-289">ニューヨーク</span><span class="sxs-lookup"><span data-stu-id="c3b05-289">New York</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-290">北アメリカ</span><span class="sxs-lookup"><span data-stu-id="c3b05-290">North America</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-291">(制限なし)</span><span class="sxs-lookup"><span data-stu-id="c3b05-291">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-292">(制限なし)</span><span class="sxs-lookup"><span data-stu-id="c3b05-292">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-293">(制限なし)</span><span class="sxs-lookup"><span data-stu-id="c3b05-293">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-294">(制限なし)</span><span class="sxs-lookup"><span data-stu-id="c3b05-294">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-295">(制限なし)</span><span class="sxs-lookup"><span data-stu-id="c3b05-295">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-296">172.29.80.0/23、157.57.216.0/25、172.29.91.0/23、172.29.81.0/24</span><span class="sxs-lookup"><span data-stu-id="c3b05-296">172.29.80.0/23, 157.57.216.0/25, 172.29.91.0/23, 172.29.81.0/24</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="c3b05-297">シカゴ</span><span class="sxs-lookup"><span data-stu-id="c3b05-297">Chicago</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-298">北アメリカ</span><span class="sxs-lookup"><span data-stu-id="c3b05-298">North America</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-299">(制限なし)</span><span class="sxs-lookup"><span data-stu-id="c3b05-299">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-300">(制限なし)</span><span class="sxs-lookup"><span data-stu-id="c3b05-300">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-301">(制限なし)</span><span class="sxs-lookup"><span data-stu-id="c3b05-301">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-302">(制限なし)</span><span class="sxs-lookup"><span data-stu-id="c3b05-302">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-303">(制限なし)</span><span class="sxs-lookup"><span data-stu-id="c3b05-303">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-304">157.57.211.0/23、172.28.152.128、25</span><span class="sxs-lookup"><span data-stu-id="c3b05-304">157.57.211.0/23, 172.28.152.128/25</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="c3b05-305">デトロイト</span><span class="sxs-lookup"><span data-stu-id="c3b05-305">Detroit</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-306">北アメリカ</span><span class="sxs-lookup"><span data-stu-id="c3b05-306">North America</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-307">(制限なし)</span><span class="sxs-lookup"><span data-stu-id="c3b05-307">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-308">(制限なし)</span><span class="sxs-lookup"><span data-stu-id="c3b05-308">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-309">(制限なし)</span><span class="sxs-lookup"><span data-stu-id="c3b05-309">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-310">(制限なし)</span><span class="sxs-lookup"><span data-stu-id="c3b05-310">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-311">(制限なし)</span><span class="sxs-lookup"><span data-stu-id="c3b05-311">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-312">172.29.78.0/24 10.71.109.0/24、157.57.209.0/23</span><span class="sxs-lookup"><span data-stu-id="c3b05-312">172.29.78.0/24 10.71.109.0/24, 157.57.209.0/23</span></span></p></td>
    </tr>
    </tbody>
    </table>


7.  <span data-ttu-id="c3b05-313">Lync Server の通話受付制御では、ネットワーク領域間の接続は *地域リンク* と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="c3b05-313">In Lync Server call admission control, the connections between network regions are called *region links*.</span></span> <span data-ttu-id="c3b05-314">各地域のリンクについて、ネットワークサイトの場合と同様に、次のことを確認します。</span><span class="sxs-lookup"><span data-stu-id="c3b05-314">For each region link, determine the following, just as you did for the network sites:</span></span>
    
      - <span data-ttu-id="c3b05-315">すべての同時音声セッションに対して設定する全体的な帯域幅制限。</span><span class="sxs-lookup"><span data-stu-id="c3b05-315">Overall bandwidth limit that you want to set for all concurrent audio sessions.</span></span> <span data-ttu-id="c3b05-316">新しいオーディオセッションによってこの制限を超過すると、Lync Server ではセッションの開始が許可されません。</span><span class="sxs-lookup"><span data-stu-id="c3b05-316">If a new audio session will cause this limit to be exceeded, Lync Server does not allow the session to start.</span></span>
    
      - <span data-ttu-id="c3b05-317">個々のオーディオセッションごとに設定する帯域幅の制限。</span><span class="sxs-lookup"><span data-stu-id="c3b05-317">Bandwidth limit that you want to set for each individual audio session.</span></span> <span data-ttu-id="c3b05-318">既定の CAC 帯域幅制限は 175 kbps ですが、管理者が変更することができます。</span><span class="sxs-lookup"><span data-stu-id="c3b05-318">The default CAC bandwidth limit is 175 kbps, but it can be modified by the administrator.</span></span>
    
      - <span data-ttu-id="c3b05-319">すべての同時ビデオセッションに対して設定する全体的な帯域幅制限。</span><span class="sxs-lookup"><span data-stu-id="c3b05-319">Overall bandwidth limit that you want to set for all concurrent video sessions.</span></span> <span data-ttu-id="c3b05-320">新しいビデオセッションによってこの制限を超過する場合、Lync Server ではセッションの開始が許可されません。</span><span class="sxs-lookup"><span data-stu-id="c3b05-320">If a new video session will cause this limit to be exceeded, Lync Server does not allow the session to start.</span></span>
    
      - <span data-ttu-id="c3b05-321">個々のビデオセッションに対して設定する帯域幅の制限。</span><span class="sxs-lookup"><span data-stu-id="c3b05-321">Bandwidth limit that you want to set for each individual video session.</span></span> <span data-ttu-id="c3b05-322">既定の CAC 帯域幅制限は 700 kbps ですが、管理者が変更することができます。</span><span class="sxs-lookup"><span data-stu-id="c3b05-322">The default CAC bandwidth limit is 700 kbps, but it can be modified by the administrator.</span></span>
    
    <span data-ttu-id="c3b05-323">**帯域幅の制限が関連付けられたネットワーク領域のリンク**</span><span class="sxs-lookup"><span data-stu-id="c3b05-323">**Network Region links with associated bandwidth limits**</span></span>
    
    <span data-ttu-id="c3b05-324">![3 つの地域間の制限の例](images/Gg425827.25259afa-ee7c-4d26-bc41-92ba9cb56dec(OCS.15).jpg "3 つの地域間の制限の例")</span><span class="sxs-lookup"><span data-stu-id="c3b05-324">![Example of Limitations between 3 Regions](images/Gg425827.25259afa-ee7c-4d26-bc41-92ba9cb56dec(OCS.15).jpg "Example of Limitations between 3 Regions")</span></span>  
    
    ### <a name="region-link-bandwidth-information-bandwidth-in-kbps"></a><span data-ttu-id="c3b05-325">地域リンクの帯域幅情報 (kbps の帯域幅)</span><span class="sxs-lookup"><span data-stu-id="c3b05-325">Region Link Bandwidth Information (Bandwidth in kbps)</span></span>
    
    <table>
    <colgroup>
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="c3b05-326">地域リンク名</span><span class="sxs-lookup"><span data-stu-id="c3b05-326">Region Link Name</span></span></th>
    <th><span data-ttu-id="c3b05-327">First Region</span><span class="sxs-lookup"><span data-stu-id="c3b05-327">First Region</span></span></th>
    <th><span data-ttu-id="c3b05-328">Second Region</span><span class="sxs-lookup"><span data-stu-id="c3b05-328">Second Region</span></span></th>
    <th><span data-ttu-id="c3b05-329">BW Limit</span><span class="sxs-lookup"><span data-stu-id="c3b05-329">BW Limit</span></span></th>
    <th><span data-ttu-id="c3b05-330">オーディオ制限</span><span class="sxs-lookup"><span data-stu-id="c3b05-330">Audio Limit</span></span></th>
    <th><span data-ttu-id="c3b05-331">オーディオセッションの制限</span><span class="sxs-lookup"><span data-stu-id="c3b05-331">Audio Session Limit</span></span></th>
    <th><span data-ttu-id="c3b05-332">ビデオの制限</span><span class="sxs-lookup"><span data-stu-id="c3b05-332">Video Limit</span></span></th>
    <th><span data-ttu-id="c3b05-333">ビデオセッションの制限</span><span class="sxs-lookup"><span data-stu-id="c3b05-333">Video Session Limit</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="c3b05-334">NA-EMEA-リンク</span><span class="sxs-lookup"><span data-stu-id="c3b05-334">NA-EMEA-LINK</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-335">北アメリカ</span><span class="sxs-lookup"><span data-stu-id="c3b05-335">North America</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-336">EMEA</span><span class="sxs-lookup"><span data-stu-id="c3b05-336">EMEA</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-337">5万</span><span class="sxs-lookup"><span data-stu-id="c3b05-337">50,000</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-338">2万</span><span class="sxs-lookup"><span data-stu-id="c3b05-338">20,000</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-339">175</span><span class="sxs-lookup"><span data-stu-id="c3b05-339">175</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-340">14000</span><span class="sxs-lookup"><span data-stu-id="c3b05-340">14,000</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-341">700</span><span class="sxs-lookup"><span data-stu-id="c3b05-341">700</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="c3b05-342">EMEA-APAC リンク</span><span class="sxs-lookup"><span data-stu-id="c3b05-342">EMEA-APAC-LINK</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-343">EMEA</span><span class="sxs-lookup"><span data-stu-id="c3b05-343">EMEA</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-344">APAC</span><span class="sxs-lookup"><span data-stu-id="c3b05-344">APAC</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-345">25,000</span><span class="sxs-lookup"><span data-stu-id="c3b05-345">25,000</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-346">10,000</span><span class="sxs-lookup"><span data-stu-id="c3b05-346">10,000</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-347">175</span><span class="sxs-lookup"><span data-stu-id="c3b05-347">175</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-348">7000</span><span class="sxs-lookup"><span data-stu-id="c3b05-348">7,000</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-349">700</span><span class="sxs-lookup"><span data-stu-id="c3b05-349">700</span></span></p></td>
    </tr>
    </tbody>
    </table>


8.  <span data-ttu-id="c3b05-350">ネットワーク地域のすべてのペア間のルートを定義します。</span><span class="sxs-lookup"><span data-stu-id="c3b05-350">Define a route between every pair of network regions.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="c3b05-351">北アメリカと APAC の地域間のルートには、直接接続する地域のリンクがないため、2つのリンクが必要です。</span><span class="sxs-lookup"><span data-stu-id="c3b05-351">Two links are required for the route between the North America and APAC regions because there is no region link that directly connects them.</span></span>

    
    </div>
    
    ### <a name="region-routes"></a><span data-ttu-id="c3b05-352">地域ルート</span><span class="sxs-lookup"><span data-stu-id="c3b05-352">Region Routes</span></span>
    
    <table>
    <colgroup>
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="c3b05-353">地域ルート名</span><span class="sxs-lookup"><span data-stu-id="c3b05-353">Region Route Name</span></span></th>
    <th><span data-ttu-id="c3b05-354">First Region</span><span class="sxs-lookup"><span data-stu-id="c3b05-354">First Region</span></span></th>
    <th><span data-ttu-id="c3b05-355">Second Region</span><span class="sxs-lookup"><span data-stu-id="c3b05-355">Second Region</span></span></th>
    <th><span data-ttu-id="c3b05-356">地域リンク</span><span class="sxs-lookup"><span data-stu-id="c3b05-356">Region Links</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="c3b05-357">NA-EMEA-ルート</span><span class="sxs-lookup"><span data-stu-id="c3b05-357">NA-EMEA-ROUTE</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-358">北アメリカ</span><span class="sxs-lookup"><span data-stu-id="c3b05-358">North America</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-359">EMEA</span><span class="sxs-lookup"><span data-stu-id="c3b05-359">EMEA</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-360">NA-EMEA-リンク</span><span class="sxs-lookup"><span data-stu-id="c3b05-360">NA-EMEA-LINK</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="c3b05-361">EMEA-APAC-ルート</span><span class="sxs-lookup"><span data-stu-id="c3b05-361">EMEA-APAC-ROUTE</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-362">EMEA</span><span class="sxs-lookup"><span data-stu-id="c3b05-362">EMEA</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-363">APAC</span><span class="sxs-lookup"><span data-stu-id="c3b05-363">APAC</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-364">EMEA-APAC リンク</span><span class="sxs-lookup"><span data-stu-id="c3b05-364">EMEA-APAC-LINK</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="c3b05-365">NA-APAC-ルート</span><span class="sxs-lookup"><span data-stu-id="c3b05-365">NA-APAC-ROUTE</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-366">北アメリカ</span><span class="sxs-lookup"><span data-stu-id="c3b05-366">North America</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-367">APAC</span><span class="sxs-lookup"><span data-stu-id="c3b05-367">APAC</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-368">NA-EMEA-リンク、EMEA-APAC リンク</span><span class="sxs-lookup"><span data-stu-id="c3b05-368">NA-EMEA-LINK, EMEA-APAC-LINK</span></span></p></td>
    </tr>
    </tbody>
    </table>


9.  <span data-ttu-id="c3b05-369">1つのリンク ( *サイト間* リンクと呼ばれます) によって直接接続されているネットワークサイトのペアごとに、次のことを確認します。</span><span class="sxs-lookup"><span data-stu-id="c3b05-369">For every pair of network sites that are directly connected by a single link (called an *inter-site* link), determine the following:</span></span>
    
      - <span data-ttu-id="c3b05-370">すべての同時音声セッションに対して設定する全体的な帯域幅制限。</span><span class="sxs-lookup"><span data-stu-id="c3b05-370">Overall bandwidth limit that you want to set for all concurrent audio sessions.</span></span> <span data-ttu-id="c3b05-371">新しいオーディオセッションによってこの制限を超過すると、Lync Server ではセッションの開始が許可されません。</span><span class="sxs-lookup"><span data-stu-id="c3b05-371">If a new audio session will cause this limit to be exceeded, Lync Server does not allow the session to start.</span></span>
    
      - <span data-ttu-id="c3b05-372">個々のオーディオセッションごとに設定する帯域幅の制限。</span><span class="sxs-lookup"><span data-stu-id="c3b05-372">Bandwidth limit that you want to set for each individual audio session.</span></span> <span data-ttu-id="c3b05-373">既定の CAC 帯域幅制限は 175 kbps ですが、管理者が変更することができます。</span><span class="sxs-lookup"><span data-stu-id="c3b05-373">The default CAC bandwidth limit is 175 kbps, but it can be modified by the administrator.</span></span>
    
      - <span data-ttu-id="c3b05-374">すべての同時ビデオセッションに対して設定する全体的な帯域幅制限。</span><span class="sxs-lookup"><span data-stu-id="c3b05-374">Overall bandwidth limit that you want to set for all concurrent video sessions.</span></span> <span data-ttu-id="c3b05-375">新しいビデオセッションによってこの制限を超過する場合、Lync Server ではセッションの開始が許可されません。</span><span class="sxs-lookup"><span data-stu-id="c3b05-375">If a new video session will cause this limit to be exceeded, Lync Server does not allow the session to start.</span></span>
    
      - <span data-ttu-id="c3b05-376">個々のビデオセッションに対して設定する帯域幅の制限。</span><span class="sxs-lookup"><span data-stu-id="c3b05-376">Bandwidth limit that you want to set for each individual video session.</span></span> <span data-ttu-id="c3b05-377">既定の CAC 帯域幅制限は 700 kbps ですが、管理者が変更することができます。</span><span class="sxs-lookup"><span data-stu-id="c3b05-377">The default CAC bandwidth limit is 700 kbps, but it can be modified by the administrator.</span></span>
    
    <span data-ttu-id="c3b05-378">**Reno とアルバカーキの間にあるサイト間リンクの帯域幅と帯域幅の制限を示す CAC ネットワークの地域 (北アメリカ)**</span><span class="sxs-lookup"><span data-stu-id="c3b05-378">**CAC network region North America showing the bandwidth capacities and bandwidth limits for the inter-site link between Reno and Albuquerque**</span></span>
    
    <span data-ttu-id="c3b05-379">![WAN 帯域幅による制限があるネットワーク サイトの例](images/Gg425827.063e5e1d-b6c8-4e8c-98db-c227c78f671d(OCS.15).jpg "WAN 帯域幅による制限があるネットワーク サイトの例")</span><span class="sxs-lookup"><span data-stu-id="c3b05-379">![Network Sites Constrained by WAN Bandwidth example](images/Gg425827.063e5e1d-b6c8-4e8c-98db-c227c78f671d(OCS.15).jpg "Network Sites Constrained by WAN Bandwidth example")</span></span>  
    
    ### <a name="bandwidth-information-for-an-inter-site-link-between-two-network-sites-bandwidth-in-kbps"></a><span data-ttu-id="c3b05-380">2つのネットワークサイト間の Inter-Site リンクの帯域幅 (kbps)</span><span class="sxs-lookup"><span data-stu-id="c3b05-380">Bandwidth Information for an Inter-Site Link between Two Network Sites (Bandwidth in kbps)</span></span>
    
    <table>
    <colgroup>
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="c3b05-381">Inter-Site リンク名</span><span class="sxs-lookup"><span data-stu-id="c3b05-381">Inter-Site Link Name</span></span></th>
    <th><span data-ttu-id="c3b05-382">第1のサイト</span><span class="sxs-lookup"><span data-stu-id="c3b05-382">First Site</span></span></th>
    <th><span data-ttu-id="c3b05-383">第2のサイト</span><span class="sxs-lookup"><span data-stu-id="c3b05-383">Second Site</span></span></th>
    <th><span data-ttu-id="c3b05-384">BW Limit</span><span class="sxs-lookup"><span data-stu-id="c3b05-384">BW Limit</span></span></th>
    <th><span data-ttu-id="c3b05-385">オーディオ制限</span><span class="sxs-lookup"><span data-stu-id="c3b05-385">Audio Limit</span></span></th>
    <th><span data-ttu-id="c3b05-386">オーディオセッションの制限</span><span class="sxs-lookup"><span data-stu-id="c3b05-386">Audio Session Limit</span></span></th>
    <th><span data-ttu-id="c3b05-387">ビデオの制限</span><span class="sxs-lookup"><span data-stu-id="c3b05-387">Video Limit</span></span></th>
    <th><span data-ttu-id="c3b05-388">ビデオセッションの制限</span><span class="sxs-lookup"><span data-stu-id="c3b05-388">Video Session Limit</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="c3b05-389">Reno-Albu-サイト間リンク</span><span class="sxs-lookup"><span data-stu-id="c3b05-389">Reno-Albu-Intersite-Link</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-390">リノ</span><span class="sxs-lookup"><span data-stu-id="c3b05-390">Reno</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-391">アルバカーキ</span><span class="sxs-lookup"><span data-stu-id="c3b05-391">Albuquerque</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-392">2万</span><span class="sxs-lookup"><span data-stu-id="c3b05-392">20,000</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-393">12000</span><span class="sxs-lookup"><span data-stu-id="c3b05-393">12,000</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-394">175</span><span class="sxs-lookup"><span data-stu-id="c3b05-394">175</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-395">5,000</span><span class="sxs-lookup"><span data-stu-id="c3b05-395">5,000</span></span></p></td>
    <td><p><span data-ttu-id="c3b05-396">700</span><span class="sxs-lookup"><span data-stu-id="c3b05-396">700</span></span></p></td>
    </tr>
    </tbody>
    </table>


<div>

## <a name="next-steps"></a><span data-ttu-id="c3b05-397">次の手順</span><span class="sxs-lookup"><span data-stu-id="c3b05-397">Next Steps</span></span>

<span data-ttu-id="c3b05-398">必要な情報を収集した後は、Lync Server 管理シェルまたは Lync Server コントロールパネルを使用して、CAC 展開を実行できます。</span><span class="sxs-lookup"><span data-stu-id="c3b05-398">After you have gathered the required information, you can perform CAC deployment either by using the Lync Server Management Shell or Lync Server Control Panel.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="c3b05-399">Lync Server コントロールパネルを使用して、ほとんどのネットワーク構成タスクを実行できますが、サブネットとサイト間リンクを作成するには、Lync Server 管理シェルを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3b05-399">Although you can perform most network configuration tasks by using Lync Server Control Panel, to create subnets and intersite links, you must use Lync Server Management Shell.</span></span> <span data-ttu-id="c3b05-400">詳細については、 <STRONG>新しい-CsNetworkSubnet</STRONG> コマンドレットと <STRONG>CsNetworkIntersitePolicy</STRONG> コマンドレットの Lync Server 管理シェルのマニュアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c3b05-400">For details, see the Lync Server Management Shell documentation for the <STRONG>New-CsNetworkSubnet</STRONG> cmdlet and the <STRONG>New-CsNetworkIntersitePolicy</STRONG> cmdlet.</span></span>



<span data-ttu-id="c3b05-401"></div>

</div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c3b05-401"></div>

</div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

