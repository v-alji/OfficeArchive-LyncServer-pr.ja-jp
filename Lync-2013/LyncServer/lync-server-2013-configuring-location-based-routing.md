---
title: 'Lync Server 2013: 場所に基づくルーティングの構成'
description: 'Lync Server 2013: Location-Based ルーティングを構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Location-Based Routing
ms:assetid: 63cdc474-e80f-43b1-a237-9d9ed673300a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994036(v=OCS.15)
ms:contentKeyID: 51803946
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 080c2a3a82a8714fc35ce882b0c6cb1630552f27
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433047"
---
# <a name="configuring-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="6e1d6-103">Lync Server 2013 の場所に基づくルーティングの構成</span><span class="sxs-lookup"><span data-stu-id="6e1d6-103">Configuring Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6e1d6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6e1d6-104">

<span> </span></span></span>

<span data-ttu-id="6e1d6-105">_**最終更新日:** 2013-03-12_</span><span class="sxs-lookup"><span data-stu-id="6e1d6-105">_**Topic Last Modified:** 2013-03-12_</span></span>

<span data-ttu-id="6e1d6-106">Lync Server 2013 CU1、Location-Based ルーティングはエンタープライズ Voip の機能です。</span><span class="sxs-lookup"><span data-stu-id="6e1d6-106">Lync Server 2013 CU1, Location-Based Routing is a feature of Enterprise Voice.</span></span> <span data-ttu-id="6e1d6-107">Location-Based ルーティングは、Lync Server 2013 CU1 による通話のルーティング方法を制御する通話管理機能です。</span><span class="sxs-lookup"><span data-stu-id="6e1d6-107">Location-Based Routing is a call management feature that controls how calls are routed by Lync Server 2013 CU1.</span></span> <span data-ttu-id="6e1d6-108">Lync の発信者の所在地に基づいて、通話を PBX または PSTN にルーティングできるかどうかに関する制限を適用します。</span><span class="sxs-lookup"><span data-stu-id="6e1d6-108">It enforces restrictions on whether calls can be routed to PBX or PSTN destinations based on the Lync caller’s location.</span></span> <span data-ttu-id="6e1d6-109">Location-Based ルーティングは、呼び出し元のネットワークの場所に基づいて着信の承認規則を PSTN 通話に適用します。</span><span class="sxs-lookup"><span data-stu-id="6e1d6-109">Location-Based Routing applies call authorization rules to PSTN calls based on the caller’s network location.</span></span> <span data-ttu-id="6e1d6-110">発信者の場所は、発信者が接続されているネットワークサブネットに関連付けられたネットワークサイトに基づいて決定されます。</span><span class="sxs-lookup"><span data-stu-id="6e1d6-110">The caller’s location is determined based on the network site associated with the network subnet the caller is connected on.</span></span> <span data-ttu-id="6e1d6-111">Location-Based ルーティングを構成するには、最初にエンタープライズボイスを展開してから、ネットワークリージョン、サイト、サブネットを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e1d6-111">Configuring Location-Based Routing requires first deploying Enterprise Voice, then configuring network regions, sites and subnets.</span></span> <span data-ttu-id="6e1d6-112">これにより、Location-Based ルーティングを有効にするための基盤が設定されます。</span><span class="sxs-lookup"><span data-stu-id="6e1d6-112">This sets up the foundation for enabling Location-Based Routing.</span></span>

<span data-ttu-id="6e1d6-113">Location-Based ルーティングを展開する前に、まずエンタープライズボイスを展開し、ネットワークの地域、サイトを構成し、ネットワークのサブネットをネットワークサイトに関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e1d6-113">Before deploying Location-Based Routing, you must first deploy Enterprise Voice, and configure network regions, sites, and associate network subnets to your network sites.</span></span> <span data-ttu-id="6e1d6-114">完了したら、Location-Based ルーティングを構成できます。</span><span class="sxs-lookup"><span data-stu-id="6e1d6-114">Once completed, you can configure Location-Based Routing.</span></span> <span data-ttu-id="6e1d6-115">ネットワークの地域、サイト、サブネットを構成する手順については、「 [Lync Server 2013 での高度なエンタープライズ voip 機能の展開](lync-server-2013-deploying-advanced-enterprise-voice-features.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6e1d6-115">For steps on how to configure network regions, sites and subnets, see [Deploying advanced Enterprise Voice features in Lync Server 2013](lync-server-2013-deploying-advanced-enterprise-voice-features.md)</span></span>

<span data-ttu-id="6e1d6-116">このセクションでは、図に示すように、次の例を使用してルーティング Location-Based の構成について説明します。</span><span class="sxs-lookup"><span data-stu-id="6e1d6-116">This section guides you through the configuration of Location-Based Routing using the following example as illustration.</span></span>

<span data-ttu-id="6e1d6-117">![エンタープライズ Voip の位置情報に基づくルーティングの例](images/JJ994036.b6ef5afc-36ac-406f-8ec2-a87532b20612(OCS.15).png "エンタープライズ Voip の位置情報に基づくルーティングの例")</span><span class="sxs-lookup"><span data-stu-id="6e1d6-117">![Enterprise Voice location-based routing example](images/JJ994036.b6ef5afc-36ac-406f-8ec2-a87532b20612(OCS.15).png "Enterprise Voice location-based routing example")</span></span>

  
<span data-ttu-id="6e1d6-118">次の表は、この例で定義されているユーザーを示しています。</span><span class="sxs-lookup"><span data-stu-id="6e1d6-118">The following table represents the users defined in this example.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6e1d6-119">エンドポイントの種類</span><span class="sxs-lookup"><span data-stu-id="6e1d6-119">Endpoint type</span></span></th>
<th><span data-ttu-id="6e1d6-120">場所</span><span class="sxs-lookup"><span data-stu-id="6e1d6-120">Location</span></span></th>
<th><span data-ttu-id="6e1d6-121">ユーザー</span><span class="sxs-lookup"><span data-stu-id="6e1d6-121">Users</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6e1d6-122">Lync</span><span class="sxs-lookup"><span data-stu-id="6e1d6-122">Lync</span></span></p></td>
<td><p><span data-ttu-id="6e1d6-123">ニューデリーの会社オフィス</span><span class="sxs-lookup"><span data-stu-id="6e1d6-123">Delhi corporate office</span></span></p></td>
<td><p><span data-ttu-id="6e1d6-124">DEL-LYNC-1、DEL-LYNC-2、DEL-LYNC-3</span><span class="sxs-lookup"><span data-stu-id="6e1d6-124">DEL-LYNC-1,DEL-LYNC-2,DEL-LYNC-3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e1d6-125">Lync</span><span class="sxs-lookup"><span data-stu-id="6e1d6-125">Lync</span></span></p></td>
<td><p><span data-ttu-id="6e1d6-126">Hyderabad 企業オフィス</span><span class="sxs-lookup"><span data-stu-id="6e1d6-126">Hyderabad corporate office</span></span></p></td>
<td><p><span data-ttu-id="6e1d6-127">HYD-1、HYD、LYNC-2、HYD、LYNC-3</span><span class="sxs-lookup"><span data-stu-id="6e1d6-127">HYD-LYNC-1, HYD-LYNC-2, HYD-LYNC-3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e1d6-128">Lync</span><span class="sxs-lookup"><span data-stu-id="6e1d6-128">Lync</span></span></p></td>
<td><p><span data-ttu-id="6e1d6-129">不明 (例: ホテル)</span><span class="sxs-lookup"><span data-stu-id="6e1d6-129">Unknown (i.e. hotel)</span></span></p></td>
<td><p><span data-ttu-id="6e1d6-130">UNK-LYNC-1</span><span class="sxs-lookup"><span data-stu-id="6e1d6-130">UNK-LYNC-1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e1d6-131">PBX</span><span class="sxs-lookup"><span data-stu-id="6e1d6-131">PBX</span></span></p></td>
<td><p><span data-ttu-id="6e1d6-132">ニューデリーの会社オフィス</span><span class="sxs-lookup"><span data-stu-id="6e1d6-132">Delhi corporate office</span></span></p></td>
<td><p><span data-ttu-id="6e1d6-133">DELETE-PBX-1、DEL-PBX-2</span><span class="sxs-lookup"><span data-stu-id="6e1d6-133">DEL-PBX-1, DEL-PBX-2</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e1d6-134">PBX</span><span class="sxs-lookup"><span data-stu-id="6e1d6-134">PBX</span></span></p></td>
<td><p><span data-ttu-id="6e1d6-135">Hyderabad 企業オフィス</span><span class="sxs-lookup"><span data-stu-id="6e1d6-135">Hyderabad corporate office</span></span></p></td>
<td><p><span data-ttu-id="6e1d6-136">HYD-1、HYD、PBX-2</span><span class="sxs-lookup"><span data-stu-id="6e1d6-136">HYD-PBX-1, HYD-PBX-2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e1d6-137">PSTN</span><span class="sxs-lookup"><span data-stu-id="6e1d6-137">PSTN</span></span></p></td>
<td><p><span data-ttu-id="6e1d6-138">未</span><span class="sxs-lookup"><span data-stu-id="6e1d6-138">Unknown</span></span></p></td>
<td><p><span data-ttu-id="6e1d6-139">PSTN-1、PSTN-2、PSTN-3</span><span class="sxs-lookup"><span data-stu-id="6e1d6-139">PSTN-1, PSTN-2, PSTN-3</span></span></p></td>
</tr>
</tbody>
</table>

  

<span data-ttu-id="6e1d6-140">次の表は、この例の環境で示されているシステムを示しています。</span><span class="sxs-lookup"><span data-stu-id="6e1d6-140">The following table represents the systems illustrated in this example environment.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6e1d6-141">Bios</span><span class="sxs-lookup"><span data-stu-id="6e1d6-141">System</span></span></th>
<th><span data-ttu-id="6e1d6-142">場所</span><span class="sxs-lookup"><span data-stu-id="6e1d6-142">Location</span></span></th>
<th><span data-ttu-id="6e1d6-143">名前</span><span class="sxs-lookup"><span data-stu-id="6e1d6-143">Name</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6e1d6-144">Lync Server 2013 CU1 プール</span><span class="sxs-lookup"><span data-stu-id="6e1d6-144">Lync Server 2013 CU1 pool</span></span></p></td>
<td><p><span data-ttu-id="6e1d6-145">任意</span><span class="sxs-lookup"><span data-stu-id="6e1d6-145">any</span></span></p></td>
<td><p><span data-ttu-id="6e1d6-146">LS-PL1</span><span class="sxs-lookup"><span data-stu-id="6e1d6-146">LS-PL1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e1d6-147">Lync Server 2013 CU1、仲介サーバー</span><span class="sxs-lookup"><span data-stu-id="6e1d6-147">Lync Server 2013 CU1, Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="6e1d6-148">任意</span><span class="sxs-lookup"><span data-stu-id="6e1d6-148">any</span></span></p></td>
<td><p><span data-ttu-id="6e1d6-149">MS-PL1</span><span class="sxs-lookup"><span data-stu-id="6e1d6-149">MS-PL1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e1d6-150">PSTN ゲートウェイ1</span><span class="sxs-lookup"><span data-stu-id="6e1d6-150">PSTN gateway 1</span></span></p></td>
<td><p><span data-ttu-id="6e1d6-151">Delhi</span><span class="sxs-lookup"><span data-stu-id="6e1d6-151">Delhi</span></span></p></td>
<td><p><span data-ttu-id="6e1d6-152">DEL-GW</span><span class="sxs-lookup"><span data-stu-id="6e1d6-152">DEL-GW</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e1d6-153">PSTN ゲートウェイ2</span><span class="sxs-lookup"><span data-stu-id="6e1d6-153">PSTN gateway 2</span></span></p></td>
<td><p><span data-ttu-id="6e1d6-154">Hyderabad</span><span class="sxs-lookup"><span data-stu-id="6e1d6-154">Hyderabad</span></span></p></td>
<td><p><span data-ttu-id="6e1d6-155">HYD</span><span class="sxs-lookup"><span data-stu-id="6e1d6-155">HYD-GW</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e1d6-156">PBX 1</span><span class="sxs-lookup"><span data-stu-id="6e1d6-156">PBX 1</span></span></p></td>
<td><p><span data-ttu-id="6e1d6-157">Delhi</span><span class="sxs-lookup"><span data-stu-id="6e1d6-157">Delhi</span></span></p></td>
<td><p><span data-ttu-id="6e1d6-158">DEL-PBX</span><span class="sxs-lookup"><span data-stu-id="6e1d6-158">DEL-PBX</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e1d6-159">PBX 2</span><span class="sxs-lookup"><span data-stu-id="6e1d6-159">PBX 2</span></span></p></td>
<td><p><span data-ttu-id="6e1d6-160">Hyderabad</span><span class="sxs-lookup"><span data-stu-id="6e1d6-160">Hyderabad</span></span></p></td>
<td><p><span data-ttu-id="6e1d6-161">赤-PBX</span><span class="sxs-lookup"><span data-stu-id="6e1d6-161">RED-PBX</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="in-this-section"></a><span data-ttu-id="6e1d6-162">このセクション中</span><span class="sxs-lookup"><span data-stu-id="6e1d6-162">In This Section</span></span>

  - [<span data-ttu-id="6e1d6-163">Lync Server 2013 でのエンタープライズ Voip の設定</span><span class="sxs-lookup"><span data-stu-id="6e1d6-163">Configuring Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-configuring-enterprise-voice.md)

  - [<span data-ttu-id="6e1d6-164">Lync Server 2013 でのネットワークのリージョン、サイト、サブネットの展開</span><span class="sxs-lookup"><span data-stu-id="6e1d6-164">Deploying network regions, sites, and subnets in Lync Server 2013</span></span>](lync-server-2013-deploying-network-regions-sites-and-subnets.md)

  - [<span data-ttu-id="6e1d6-165">Lync Server 2013 での Location-Based ルーティングの有効化</span><span class="sxs-lookup"><span data-stu-id="6e1d6-165">Enabling Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-enabling-location-based-routing.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="6e1d6-166">関連項目</span><span class="sxs-lookup"><span data-stu-id="6e1d6-166">See Also</span></span>


[<span data-ttu-id="6e1d6-167">Lync Server 2013 での高度なエンタープライズ Voip 機能の展開</span><span class="sxs-lookup"><span data-stu-id="6e1d6-167">Deploying advanced Enterprise Voice features in Lync Server 2013</span></span>](lync-server-2013-deploying-advanced-enterprise-voice-features.md)  
  

<span data-ttu-id="6e1d6-168"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6e1d6-168"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

