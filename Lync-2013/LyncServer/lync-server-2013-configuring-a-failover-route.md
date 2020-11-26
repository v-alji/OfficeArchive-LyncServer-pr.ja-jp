---
title: 'Lync Server 2013: フェールオーバー ルートの構成'
description: 'Lync Server 2013: フェールオーバールートを構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring a failover route
ms:assetid: 76e48df4-3b78-4fb7-b1f7-c1e604b81bad
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398581(v=OCS.15)
ms:contentKeyID: 48184542
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e7cfc45276931685a2d42103b1b7f1d5015dcd7e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433522"
---
# <a name="configuring-a-failover-route-in-lync-server-2013"></a><span data-ttu-id="a502c-103">Lync Server 2013 でのフェールオーバー ルートの構成</span><span class="sxs-lookup"><span data-stu-id="a502c-103">Configuring a failover route in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a502c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a502c-104">

<span> </span></span></span>

<span data-ttu-id="a502c-105">_**最終更新日:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="a502c-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="a502c-p101">次の例では、Dallas-GW1 がメンテナンスで停止したり、利用できなくなったりしたときに使用するフェールオーバー ルートの定義方法を示します。必要な構成の変更を次の表に示します。</span><span class="sxs-lookup"><span data-stu-id="a502c-p101">The following example shows how an administrator can define a failover route for use if the Dallas-GW1 is down for maintenance or is otherwise unavailable. The following tables illustrate the required configuration change.</span></span>

### <a name="table-1-user-policy"></a><span data-ttu-id="a502c-p102">表 1. ユーザー ポリシー</span><span class="sxs-lookup"><span data-stu-id="a502c-p102">Table 1. User Policy</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a502c-110">ユーザー ポリシー</span><span class="sxs-lookup"><span data-stu-id="a502c-110">User policy</span></span></th>
<th><span data-ttu-id="a502c-111">電話使用法</span><span class="sxs-lookup"><span data-stu-id="a502c-111">Phone usage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a502c-112">Default Calling Policy</span><span class="sxs-lookup"><span data-stu-id="a502c-112">Default Calling Policy</span></span></p></td>
<td><p><span data-ttu-id="a502c-113">Local</span><span class="sxs-lookup"><span data-stu-id="a502c-113">Local</span></span></p>
<p><span data-ttu-id="a502c-114">GlobalPSTNHopoff</span><span class="sxs-lookup"><span data-stu-id="a502c-114">GlobalPSTNHopoff</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a502c-115">Redmond Local Policy</span><span class="sxs-lookup"><span data-stu-id="a502c-115">Redmond Local Policy</span></span></p></td>
<td><p><span data-ttu-id="a502c-116">RedmondLocal</span><span class="sxs-lookup"><span data-stu-id="a502c-116">RedmondLocal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a502c-117">Dallas Calling Policy</span><span class="sxs-lookup"><span data-stu-id="a502c-117">Dallas Calling Policy</span></span></p></td>
<td><p><span data-ttu-id="a502c-118">DallasUsers</span><span class="sxs-lookup"><span data-stu-id="a502c-118">DallasUsers</span></span></p>
<p><span data-ttu-id="a502c-119">GlobalPSTNHopoff</span><span class="sxs-lookup"><span data-stu-id="a502c-119">GlobalPSTNHopoff</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="table-2-routes"></a><span data-ttu-id="a502c-p103">表 2. ルート</span><span class="sxs-lookup"><span data-stu-id="a502c-p103">Table 2. Routes</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a502c-122">ルート名</span><span class="sxs-lookup"><span data-stu-id="a502c-122">Route name</span></span></th>
<th><span data-ttu-id="a502c-123">番号のパターン</span><span class="sxs-lookup"><span data-stu-id="a502c-123">Number pattern</span></span></th>
<th><span data-ttu-id="a502c-124">電話使用法</span><span class="sxs-lookup"><span data-stu-id="a502c-124">Phone usage</span></span></th>
<th><span data-ttu-id="a502c-125">トランク</span><span class="sxs-lookup"><span data-stu-id="a502c-125">Trunk</span></span></th>
<th><span data-ttu-id="a502c-126">ゲートウェイ</span><span class="sxs-lookup"><span data-stu-id="a502c-126">Gateway</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a502c-127">Redmond Local Route</span><span class="sxs-lookup"><span data-stu-id="a502c-127">Redmond Local Route</span></span></p></td>
<td><p><span data-ttu-id="a502c-128">^\+1 (425 | 206 | 253) (\d {7} ) $</span><span class="sxs-lookup"><span data-stu-id="a502c-128">^\+1(425|206|253)(\d{7})$</span></span></p></td>
<td><p><span data-ttu-id="a502c-129">Local</span><span class="sxs-lookup"><span data-stu-id="a502c-129">Local</span></span></p>
<p><span data-ttu-id="a502c-130">RedmondLocal</span><span class="sxs-lookup"><span data-stu-id="a502c-130">RedmondLocal</span></span></p></td>
<td><p><span data-ttu-id="a502c-131">Trunk1</span><span class="sxs-lookup"><span data-stu-id="a502c-131">Trunk1</span></span></p>
<p><span data-ttu-id="a502c-132">Trunk2</span><span class="sxs-lookup"><span data-stu-id="a502c-132">Trunk2</span></span></p></td>
<td><p><span data-ttu-id="a502c-133">Red-GW1</span><span class="sxs-lookup"><span data-stu-id="a502c-133">Red-GW1</span></span></p>
<p><span data-ttu-id="a502c-134">Red-GW2</span><span class="sxs-lookup"><span data-stu-id="a502c-134">Red-GW2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a502c-135">Dallas Local Route</span><span class="sxs-lookup"><span data-stu-id="a502c-135">Dallas Local Route</span></span></p></td>
<td><p><span data-ttu-id="a502c-136">^\+1 (972 | 214 | 469) (\d {7} ) $</span><span class="sxs-lookup"><span data-stu-id="a502c-136">^\+1(972|214|469)(\d{7})$</span></span></p></td>
<td><p><span data-ttu-id="a502c-137">Local</span><span class="sxs-lookup"><span data-stu-id="a502c-137">Local</span></span></p></td>
<td><p><span data-ttu-id="a502c-138">Trunk3</span><span class="sxs-lookup"><span data-stu-id="a502c-138">Trunk3</span></span></p></td>
<td><p><span data-ttu-id="a502c-139">Dallas-GW1</span><span class="sxs-lookup"><span data-stu-id="a502c-139">Dallas-GW1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a502c-140">Universal Route</span><span class="sxs-lookup"><span data-stu-id="a502c-140">Universal Route</span></span></p></td>
<td><p><span data-ttu-id="a502c-141">^\+?(\d \*) $</span><span class="sxs-lookup"><span data-stu-id="a502c-141">^\+?(\d\*)$</span></span></p></td>
<td><p><span data-ttu-id="a502c-142">GlobalPSTNHopoff</span><span class="sxs-lookup"><span data-stu-id="a502c-142">GlobalPSTNHopoff</span></span></p></td>
<td><p><span data-ttu-id="a502c-143">Trunk1</span><span class="sxs-lookup"><span data-stu-id="a502c-143">Trunk1</span></span></p>
<p><span data-ttu-id="a502c-144">Trunk2</span><span class="sxs-lookup"><span data-stu-id="a502c-144">Trunk2</span></span></p>
<p><span data-ttu-id="a502c-145">Trunk3</span><span class="sxs-lookup"><span data-stu-id="a502c-145">Trunk3</span></span></p></td>
<td><p><span data-ttu-id="a502c-146">Red-GW1</span><span class="sxs-lookup"><span data-stu-id="a502c-146">Red-GW1</span></span></p>
<p><span data-ttu-id="a502c-147">Red-GW2</span><span class="sxs-lookup"><span data-stu-id="a502c-147">Red-GW2</span></span></p>
<p><span data-ttu-id="a502c-148">Dallas-GW1</span><span class="sxs-lookup"><span data-stu-id="a502c-148">Dallas-GW1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a502c-149">Dallas Users Route</span><span class="sxs-lookup"><span data-stu-id="a502c-149">Dallas Users Route</span></span></p></td>
<td><p><span data-ttu-id="a502c-150">^\+?(\d \*) $</span><span class="sxs-lookup"><span data-stu-id="a502c-150">^\+?(\d\*)$</span></span></p></td>
<td><p><span data-ttu-id="a502c-151">DallasUsers</span><span class="sxs-lookup"><span data-stu-id="a502c-151">DallasUsers</span></span></p></td>
<td><p><span data-ttu-id="a502c-152">Trunk3</span><span class="sxs-lookup"><span data-stu-id="a502c-152">Trunk3</span></span></p></td>
<td><p><span data-ttu-id="a502c-153">Dallas-GW1</span><span class="sxs-lookup"><span data-stu-id="a502c-153">Dallas-GW1</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a502c-p104">表 1 では、Dallas Calling Policy の電話使用法 DallasUsers の後に、電話使用法 GlobalPSTNHopoff が追加されます。この結果、電話使用法 DallasUsers に対応したルートが使用できない場合に、Dallas Calling Policy の通話で電話使用法 GlobalPSTNHopoff 用に構成されたルートが使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="a502c-p104">In Table 1, a phone usage of GlobalPSTNHopoff is added after the DallasUsers phone usage in the Dallas Calling Policy. This enables calls with the Dallas Calling policy to use routes that are configured for the GlobalPSTNHopoff phone usage if a route for the DallasUsers phone usage is unavailable.</span></span>

<span data-ttu-id="a502c-156"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a502c-156"></div>

<span> </span>

</div>

</div>

</span></span></div>

