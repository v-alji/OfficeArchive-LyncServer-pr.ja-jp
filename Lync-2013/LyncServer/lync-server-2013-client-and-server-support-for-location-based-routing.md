---
title: 'Lync Server 2013: 場所に基づくルーティングに対するクライアントとサーバーのサポート'
description: 'Lync Server 2013: Location-Based ルーティング向けのクライアントとサーバーのサポート。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Client and server support for Location-Based Routing
ms:assetid: 26c2ca3d-026d-4dd7-94fa-15ebb4406953
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994024(v=OCS.15)
ms:contentKeyID: 51803933
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 20dca7444f58ee62dbc36edbb7d9e1c976a97807
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434901"
---
# <a name="client-and-server-support-for-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="63189-103">Lync Server 2013 での場所に基づくルーティングに対するクライアントとサーバーのサポート</span><span class="sxs-lookup"><span data-stu-id="63189-103">Client and server support for Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="63189-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="63189-104">

<span> </span></span></span>

<span data-ttu-id="63189-105">_**最終更新日:** 2013-06-18_</span><span class="sxs-lookup"><span data-stu-id="63189-105">_**Topic Last Modified:** 2013-06-18_</span></span>

<span data-ttu-id="63189-106">Location-Based ルーティングは、Lync Server によって適用されます。</span><span class="sxs-lookup"><span data-stu-id="63189-106">Location-Based Routing is enforced by Lync Server.</span></span> <span data-ttu-id="63189-107">Lync Server は、企業ネットワーク内からユーザーが接続するネットワークサイトを特定できます。</span><span class="sxs-lookup"><span data-stu-id="63189-107">Lync Server can identify the network sites where users are connecting from within the corporate network.</span></span> <span data-ttu-id="63189-108">リモート ユーザーは企業ネットワークの外部に存在するため、リモート ユーザーの場所は不明と見なされます。</span><span class="sxs-lookup"><span data-stu-id="63189-108">Since remote users are outside the corporate network, their location is considered to be unknown.</span></span>

<div>

## <a name="lync-server-support"></a><span data-ttu-id="63189-109">Lync Server のサポート</span><span class="sxs-lookup"><span data-stu-id="63189-109">Lync Server Support</span></span>

<span data-ttu-id="63189-110">Location-Based ルーティングを行うには、Lync Server 2013 CU1 が、特定のトポロジに含まれるすべてのフロントエンドプールおよび標準エディションのサーバーに展開されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="63189-110">Location-Based Routing requires that Lync Server 2013 CU1 is deployed on all Front End pools and Standard Edition servers in a given topology.</span></span> <span data-ttu-id="63189-111">トポロジ内の特定の Lync コンポーネントに Lync Server 2013 CU1 がインストールされていない場合は、Location-Based ルーティングの制限を完全に適用することはできません。</span><span class="sxs-lookup"><span data-stu-id="63189-111">If Lync Server 2013 CU1 is not installed on certain Lync components in the topology, Location-Based Routing restrictions cannot be fully enforced.</span></span>

<span data-ttu-id="63189-112">次の表では、Location-Based ルーティングでサポートされているサーバーの役割とバージョンの組み合わせを示します。</span><span class="sxs-lookup"><span data-stu-id="63189-112">The following table identifies the combination of server roles and versions that is supported for Location-Based Routing.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="63189-113">プールのバージョン</span><span class="sxs-lookup"><span data-stu-id="63189-113">Pool version</span></span></th>
<th><span data-ttu-id="63189-114">仲介サーバーのバージョン</span><span class="sxs-lookup"><span data-stu-id="63189-114">Mediation Server version</span></span></th>
<th><span data-ttu-id="63189-115">サポート対象</span><span class="sxs-lookup"><span data-stu-id="63189-115">Supported</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="63189-116">Lync Server 2013 (2013 年2月の累積更新プログラム)</span><span class="sxs-lookup"><span data-stu-id="63189-116">Lync Server 2013 February 2013 Cumulative Update</span></span></p></td>
<td><p><span data-ttu-id="63189-117">Lync Server 2013 (2013 年2月の累積更新プログラム)</span><span class="sxs-lookup"><span data-stu-id="63189-117">Lync Server 2013 February 2013 Cumulative Update</span></span></p></td>
<td><p><span data-ttu-id="63189-118">はい</span><span class="sxs-lookup"><span data-stu-id="63189-118">yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63189-119">Lync Server 2013 (2013 年2月の累積更新プログラム)</span><span class="sxs-lookup"><span data-stu-id="63189-119">Lync Server 2013 February 2013 Cumulative Update</span></span></p></td>
<td><p><span data-ttu-id="63189-120">Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="63189-120">Lync Server 2013</span></span></p></td>
<td><p><span data-ttu-id="63189-121">いいえ</span><span class="sxs-lookup"><span data-stu-id="63189-121">no</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63189-122">Lync Server 2013 (2013 年2月の累積更新プログラム)</span><span class="sxs-lookup"><span data-stu-id="63189-122">Lync Server 2013 February 2013 Cumulative Update</span></span></p></td>
<td><p><span data-ttu-id="63189-123">Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="63189-123">Lync Server 2010</span></span></p></td>
<td><p><span data-ttu-id="63189-124">いいえ</span><span class="sxs-lookup"><span data-stu-id="63189-124">no</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63189-125">Lync Server 2013 (2013 年2月の累積更新プログラム)</span><span class="sxs-lookup"><span data-stu-id="63189-125">Lync Server 2013 February 2013 Cumulative Update</span></span></p></td>
<td><p><span data-ttu-id="63189-126">Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="63189-126">Office Communications Server 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="63189-127">いいえ</span><span class="sxs-lookup"><span data-stu-id="63189-127">no</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63189-128">Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="63189-128">Lync Server 2013</span></span></p></td>
<td><p><span data-ttu-id="63189-129">任意</span><span class="sxs-lookup"><span data-stu-id="63189-129">any</span></span></p></td>
<td><p><span data-ttu-id="63189-130">いいえ</span><span class="sxs-lookup"><span data-stu-id="63189-130">no</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63189-131">Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="63189-131">Lync Server 2010</span></span></p></td>
<td><p><span data-ttu-id="63189-132">任意</span><span class="sxs-lookup"><span data-stu-id="63189-132">any</span></span></p></td>
<td><p><span data-ttu-id="63189-133">いいえ</span><span class="sxs-lookup"><span data-stu-id="63189-133">no</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63189-134">Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="63189-134">Office Communications Server 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="63189-135">任意</span><span class="sxs-lookup"><span data-stu-id="63189-135">any</span></span></p></td>
<td><p><span data-ttu-id="63189-136">いいえ</span><span class="sxs-lookup"><span data-stu-id="63189-136">no</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="lync-client-support"></a><span data-ttu-id="63189-137">Lync クライアントのサポート</span><span class="sxs-lookup"><span data-stu-id="63189-137">Lync Client Support</span></span>

<span data-ttu-id="63189-138">次の表では、Location-Based ルーティングでサポートされているクライアントを示します。</span><span class="sxs-lookup"><span data-stu-id="63189-138">The following table identifies the clients that Location-Based Routing supports.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="63189-139">クライアントの種類</span><span class="sxs-lookup"><span data-stu-id="63189-139">Client type</span></span></th>
<th><span data-ttu-id="63189-140">サポート対象</span><span class="sxs-lookup"><span data-stu-id="63189-140">Supported</span></span></th>
<th><span data-ttu-id="63189-141">詳細</span><span class="sxs-lookup"><span data-stu-id="63189-141">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="63189-142">Lync 2013</span><span class="sxs-lookup"><span data-stu-id="63189-142">Lync 2013</span></span></p></td>
<td><p><span data-ttu-id="63189-143">はい</span><span class="sxs-lookup"><span data-stu-id="63189-143">yes</span></span></p></td>
<td><p><span data-ttu-id="63189-144">2013年 2 2013 月の累積更新プログラム (Lync)</span><span class="sxs-lookup"><span data-stu-id="63189-144">Including Lync 2013 February 2013 Cumulative Update</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63189-145">Lync 2010</span><span class="sxs-lookup"><span data-stu-id="63189-145">Lync 2010</span></span></p></td>
<td><p><span data-ttu-id="63189-146">はい</span><span class="sxs-lookup"><span data-stu-id="63189-146">yes</span></span></p></td>
<td> </td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63189-147">Office Communicator 2007 R2</span><span class="sxs-lookup"><span data-stu-id="63189-147">Office Communicator 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="63189-148">いいえ</span><span class="sxs-lookup"><span data-stu-id="63189-148">no</span></span></p></td>
<td> </td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63189-149">Lync Phone Edition</span><span class="sxs-lookup"><span data-stu-id="63189-149">Lync Phone Edition</span></span></p></td>
<td><p><span data-ttu-id="63189-150">はい</span><span class="sxs-lookup"><span data-stu-id="63189-150">yes</span></span></p></td>
<td> </td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63189-151">Lync Attendant</span><span class="sxs-lookup"><span data-stu-id="63189-151">Lync Attendant</span></span></p></td>
<td><p><span data-ttu-id="63189-152">はい</span><span class="sxs-lookup"><span data-stu-id="63189-152">yes</span></span></p></td>
<td> </td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63189-153">Windows 8 版 Lync</span><span class="sxs-lookup"><span data-stu-id="63189-153">Lync for Windows 8</span></span></p></td>
<td><p><span data-ttu-id="63189-154">いいえ</span><span class="sxs-lookup"><span data-stu-id="63189-154">no</span></span></p></td>
<td> </td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63189-155">Lync Mobile 2013</span><span class="sxs-lookup"><span data-stu-id="63189-155">Lync Mobile 2013</span></span></p></td>
<td><p><span data-ttu-id="63189-156">いいえ</span><span class="sxs-lookup"><span data-stu-id="63189-156">no</span></span></p></td>
<td><p><span data-ttu-id="63189-157">Location-Based ルーティングを有効にしているユーザーが使用した場合、Lync Mobile 2013 クライアントで VoIP を無効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="63189-157">VoIP must be disabled for Lync Mobile 2013 clients if used by users with Location-Based Routing enabled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63189-158">Lync Mobile 2010</span><span class="sxs-lookup"><span data-stu-id="63189-158">Lync Mobile 2010</span></span></p></td>
<td><p><span data-ttu-id="63189-159">はい</span><span class="sxs-lookup"><span data-stu-id="63189-159">yes</span></span></p></td>
<td> </td>
</tr>
</tbody>
</table>

  

<div>


> [!NOTE]  
> <span data-ttu-id="63189-160">Lync Mobile 2013 クライアントで VoIP を無効にするには、位置情報に基づくルーティングが有効になっているすべてのユーザーに対して、設定、[IP Audio/ビデオ] の順に移動して、モビリティポリシーを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="63189-160">To disable VoIP for Lync Mobile 2013 clients, assign a mobility policy with the setting, IP Audio/Video, disabled for all users enabled for Location Based Routing.</span></span> <span data-ttu-id="63189-161">モビリティ ポリシーの詳細については、「<A href="https://docs.microsoft.com/powershell/module/skype/New-CsMobilityPolicy">New-CsMobilityPolicy</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="63189-161">For more details about mobility policy, see <A href="https://docs.microsoft.com/powershell/module/skype/New-CsMobilityPolicy">New-CsMobilityPolicy</A>.</span></span>



</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="63189-162">関連項目</span><span class="sxs-lookup"><span data-stu-id="63189-162">See Also</span></span>


[<span data-ttu-id="63189-163">Lync Server 2013 での場所に基づくルーティングの計画</span><span class="sxs-lookup"><span data-stu-id="63189-163">Planning for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-planning-for-location-based-routing.md)  
  

<span data-ttu-id="63189-164"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="63189-164"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

