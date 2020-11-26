---
title: 'Lync Server 2013: ルーティングと提案型通話の転送を Location-Based'
description: 'Lync Server 2013: ルーティングと提案型通話の転送 Location-Based。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Location-Based Routing and consultative call transfers
ms:assetid: b12460c2-36c8-481f-b867-fe10dc1c0bdf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362836(v=OCS.15)
ms:contentKeyID: 56335089
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0d07cf6a33ff4d6ad57f8913a798fac3bc393a00
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426559"
---
# <a name="location-based-routing-and-consultative-call-transfers-in-lync-server-2013"></a><span data-ttu-id="439e4-103">Lync Server 2013 での Location-Based ルーティングとコンサルティングによる通話転送</span><span class="sxs-lookup"><span data-stu-id="439e4-103">Location-Based Routing and consultative call transfers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="439e4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="439e4-104">

<span> </span></span></span>

<span data-ttu-id="439e4-105">_**最終更新日:** 2013-07-31_</span><span class="sxs-lookup"><span data-stu-id="439e4-105">_**Topic Last Modified:** 2013-07-31_</span></span>

<span data-ttu-id="439e4-106">Location-Based ルーティング会議アプリケーションは、Lync 会議への Location-Based ルーティングを適用することに加えて、PSTN エンドポイントに送信されるコンサルティング呼び出しの転送に対して Location-Based ルーティングの制限を適用します。</span><span class="sxs-lookup"><span data-stu-id="439e4-106">In addition to enforcing Location-Based Routing to Lync meetings, the Location-Based Routing Conferencing application enforces Location-Based Routing restrictions on consultative call transfers that egress to PSTN endpoints.</span></span> <span data-ttu-id="439e4-107">お客様による発信は、2つの当事者間で確立された通話であり、一方の当事者が新しいユーザーに通話を転送します。</span><span class="sxs-lookup"><span data-stu-id="439e4-107">A consultative call transfer is a call established between two parties where one of the parties transfers the call to a new user.</span></span> <span data-ttu-id="439e4-108">たとえば、PSTN エンドポイントはユーザー A (Lync 呼び出し元) を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="439e4-108">For example, a PSTN endpoint calls user A (Lync callee).</span></span> <span data-ttu-id="439e4-109">ユーザー A は、PSTN ユーザーをユーザー B (Lync ユーザー) に転送する必要があることを決定します。</span><span class="sxs-lookup"><span data-stu-id="439e4-109">User A determines the PSTN user should be forwarded to user B (Lync user).</span></span> <span data-ttu-id="439e4-110">ユーザー A は、PSTN ユーザーとの通話を保留にし、ユーザー B を呼び出します。ユーザー B は PSTN ユーザーとの通信に同意します。</span><span class="sxs-lookup"><span data-stu-id="439e4-110">User A places the call with the PSTN user on hold, and calls user B. User B agrees to talk to the PSTN user.</span></span> <span data-ttu-id="439e4-111">ユーザー A は、着信をユーザー B に転送します。</span><span class="sxs-lookup"><span data-stu-id="439e4-111">User A transfers the call on-hold to user B.</span></span>

<span data-ttu-id="439e4-112">**取次通話転送の通話フロー**</span><span class="sxs-lookup"><span data-stu-id="439e4-112">**Consultative call transfer call flow**</span></span>

<span data-ttu-id="439e4-113">![会議の位置情報に基づくルーティングの図](images/Dn362836.e4d43d6f-23d2-49c9-b12b-15248a743f92(OCS.15).jpg "会議の位置情報に基づくルーティングの図")</span><span class="sxs-lookup"><span data-stu-id="439e4-113">![Location-based routing for conferencing diagram](images/Dn362836.e4d43d6f-23d2-49c9-b12b-15248a743f92(OCS.15).jpg "Location-based routing for conferencing diagram")</span></span>

<span data-ttu-id="439e4-114">Location-Based ルーティングが有効になっている場合、PSTN エンドポイントのコンサルティング通話転送 (上の図を参照) が開始されます。これに Location-Based より、2つのアクティブな通話、PSTN ユーザーと Lync ユーザー A の間の通話、および Lync ユーザー A と Lync ユーザー B 間でのその他の操作が実行されます。</span><span class="sxs-lookup"><span data-stu-id="439e4-114">When a user enabled for Location-Based Routing initiates a consultative call transfer of a PSTN endpoint (as shown in the preceding figure), this creates two active calls, one call between the PSTN user and Lync user A, and the other between Lync user A and Lync user B. the following behavior is enforced by the Location-Based Routing Conferencing application:</span></span>

  - <span data-ttu-id="439e4-115">PSTN 通話をルーティングする SIP トランクが、Lync ユーザー B (つまり転送先) があるネットワークサイトへの PSTN 通話を再ルーティングすることを許可されている場合は、通話転送が許可されます。それ以外の場合は、コンサルティング着信の転送がブロックされます。</span><span class="sxs-lookup"><span data-stu-id="439e4-115">If the SIP trunk routing the PSTN call is authorized to re-route the PSTN call to the network site where Lync user B (i.e. transfer target) is located,, then the call transfer will be allowed; otherwise, the consultative call transfer will be blocked.</span></span> <span data-ttu-id="439e4-116">この承認は、転送された当事者が、PSTN エンドポイントへのアクティブな通話をルーティングしている SIP トランクと同じネットワークサイトに配置されている場所に基づいて行われます。</span><span class="sxs-lookup"><span data-stu-id="439e4-116">This authorization is performed based on the transferred party’s location being in the same network site as the SIP trunk that is routing the active call to the PSTN endpoint.</span></span>

  - <span data-ttu-id="439e4-117">受信した PSTN 通話の SIP トランクルーティングが、転送されたパーティ (Lync ユーザー B) が存在するか、または転送されたパーティが不明なネットワークサイトにある場合は、PSTN エンドポイントへの提案型コール転送 (つまり、着信転送ターゲット) はブロックされます。</span><span class="sxs-lookup"><span data-stu-id="439e4-117">If the SIP trunk routing the inbound PSTN call is not authorized to route calls to the network site where the transferred party (Lync user B) is located or the transferred party is located in an unknown network site, then the consultative call transfer to the PSTN endpoint (i.e. call transfer target) will be blocked.</span></span>

<span data-ttu-id="439e4-118">次の表では、提案型の通話転送について、Location-Based ルーティング会議アプリケーションで Location-Based ルーティングの制限を適用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="439e4-118">The following table describes how Location-Based Routing restrictions are applied by the Location-Based Routing Conferencing application for consultative call transfers.</span></span> <span data-ttu-id="439e4-119">PBX エンドポイントはネットワーク サイトに直接関連付けられませんが、PBX の接続先の SIP トランクにネットワーク サイトが割り当てられる場合があります。</span><span class="sxs-lookup"><span data-stu-id="439e4-119">Although PBX endpoints are not directly associated with a network site, the SIP trunk the PBX is connected to can be assigned a network site.</span></span> <span data-ttu-id="439e4-120">したがって、PBX エンドポイントがネットワーク サイトに間接的に関連付けられる場合があります。</span><span class="sxs-lookup"><span data-stu-id="439e4-120">Therefore, the PBX endpoint can be indirectly associated with a network site.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="439e4-121">通話転送を受ける側のネットワーク サイト</span><span class="sxs-lookup"><span data-stu-id="439e4-121">Network site of call transferred party</span></span></p></td>
<td><p><span data-ttu-id="439e4-122">通話転送ターゲットのネットワーク サイト</span><span class="sxs-lookup"><span data-stu-id="439e4-122">Network site of call transfer target</span></span></p></td>
<td><p><span data-ttu-id="439e4-123">動作</span><span class="sxs-lookup"><span data-stu-id="439e4-123">Behavior</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="439e4-124">PSTN エンドポイント</span><span class="sxs-lookup"><span data-stu-id="439e4-124">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="439e4-125">同じネットワークサイト内の Lync ユーザー (例: サイト 1)</span><span class="sxs-lookup"><span data-stu-id="439e4-125">Lync user in the same network site (i.e. site 1)</span></span></p></td>
<td><p><span data-ttu-id="439e4-126">取次転送が許可される</span><span class="sxs-lookup"><span data-stu-id="439e4-126">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="439e4-127">PSTN エンドポイント</span><span class="sxs-lookup"><span data-stu-id="439e4-127">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="439e4-128">異なるネットワークサイトの Lync ユーザー (例: サイト 2)</span><span class="sxs-lookup"><span data-stu-id="439e4-128">Lync user in different network sites (i.e. site 2)</span></span></p></td>
<td><p><span data-ttu-id="439e4-129">取次転送が許可されない</span><span class="sxs-lookup"><span data-stu-id="439e4-129">Consultative transfer will be disallowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="439e4-130">PSTN エンドポイント</span><span class="sxs-lookup"><span data-stu-id="439e4-130">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="439e4-131">不明なネットワークサイトの Lync ユーザー</span><span class="sxs-lookup"><span data-stu-id="439e4-131">Lync user in an unknown network site</span></span></p></td>
<td><p><span data-ttu-id="439e4-132">取次転送が許可されない</span><span class="sxs-lookup"><span data-stu-id="439e4-132">Consultative transfer will be disallowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="439e4-133">PSTN エンドポイント</span><span class="sxs-lookup"><span data-stu-id="439e4-133">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="439e4-134">フェデレーションされた Lync ユーザー</span><span class="sxs-lookup"><span data-stu-id="439e4-134">Federated Lync user</span></span></p></td>
<td><p><span data-ttu-id="439e4-135">取次転送が許可されない</span><span class="sxs-lookup"><span data-stu-id="439e4-135">Consultative transfer will be disallowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="439e4-136">PSTN エンドポイント</span><span class="sxs-lookup"><span data-stu-id="439e4-136">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="439e4-137">同じサイト (サイト 1) 内の PBX エンドポイント</span><span class="sxs-lookup"><span data-stu-id="439e4-137">PBX endpoint in the same site (i.e. site 1)</span></span></p></td>
<td><p><span data-ttu-id="439e4-138">取次転送が許可される</span><span class="sxs-lookup"><span data-stu-id="439e4-138">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="439e4-139">PSTN エンドポイント</span><span class="sxs-lookup"><span data-stu-id="439e4-139">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="439e4-140">別のサイト (サイト 2) 内の PBX エンドポイント</span><span class="sxs-lookup"><span data-stu-id="439e4-140">PBX endpoint in a different sites (i.e. site 2)</span></span></p></td>
<td><p><span data-ttu-id="439e4-141">取次転送が許可されない</span><span class="sxs-lookup"><span data-stu-id="439e4-141">Consultative transfer will be disallowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="439e4-142">同じサイト (サイト 1) 内の PBX エンドポイント</span><span class="sxs-lookup"><span data-stu-id="439e4-142">PBX endpoint in the same site (i.e. site 1)</span></span></p></td>
<td><p><span data-ttu-id="439e4-143">PSTN エンドポイント</span><span class="sxs-lookup"><span data-stu-id="439e4-143">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="439e4-144">取次転送が許可される</span><span class="sxs-lookup"><span data-stu-id="439e4-144">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="439e4-145">別のサイト (サイト 2) 内の PBX エンドポイント</span><span class="sxs-lookup"><span data-stu-id="439e4-145">PBX endpoint in a different site (i.e. site 2)</span></span></p></td>
<td><p><span data-ttu-id="439e4-146">PSTN エンドポイント</span><span class="sxs-lookup"><span data-stu-id="439e4-146">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="439e4-147">取次転送が許可されない</span><span class="sxs-lookup"><span data-stu-id="439e4-147">Consultative transfer will be disallowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="439e4-148">任意のサイト内の PBX エンドポイント</span><span class="sxs-lookup"><span data-stu-id="439e4-148">PBX endpoint in any site</span></span></p></td>
<td><p><span data-ttu-id="439e4-149">同じネットワークサイト内の Lync ユーザー (例: サイト 1)</span><span class="sxs-lookup"><span data-stu-id="439e4-149">Lync user in the same network site (i.e. site 1)</span></span></p></td>
<td><p><span data-ttu-id="439e4-150">取次転送が許可される</span><span class="sxs-lookup"><span data-stu-id="439e4-150">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="439e4-151">任意のサイト内の PBX エンドポイント</span><span class="sxs-lookup"><span data-stu-id="439e4-151">PBX endpoint in any site</span></span></p></td>
<td><p><span data-ttu-id="439e4-152">異なるネットワークサイトの Lync ユーザー (例: サイト 2)</span><span class="sxs-lookup"><span data-stu-id="439e4-152">Lync user in different network sites (i.e. site 2)</span></span></p></td>
<td><p><span data-ttu-id="439e4-153">取次転送が許可される</span><span class="sxs-lookup"><span data-stu-id="439e4-153">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="439e4-154">任意のサイト内の PBX エンドポイント</span><span class="sxs-lookup"><span data-stu-id="439e4-154">PBX endpoint in any site</span></span></p></td>
<td><p><span data-ttu-id="439e4-155">不明なネットワークサイトの Lync ユーザー</span><span class="sxs-lookup"><span data-stu-id="439e4-155">Lync user in an unknown network site</span></span></p></td>
<td><p><span data-ttu-id="439e4-156">取次転送が許可される</span><span class="sxs-lookup"><span data-stu-id="439e4-156">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="439e4-157">任意のサイト内の PBX エンドポイント</span><span class="sxs-lookup"><span data-stu-id="439e4-157">PBX endpoint in any site</span></span></p></td>
<td><p><span data-ttu-id="439e4-158">フェデレーションされた Lync ユーザー</span><span class="sxs-lookup"><span data-stu-id="439e4-158">Federated Lync user</span></span></p></td>
<td><p><span data-ttu-id="439e4-159">取次転送が許可される</span><span class="sxs-lookup"><span data-stu-id="439e4-159">Consultative transfer will be allowed</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="439e4-160">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="439e4-160">


</div>

<span> </span>

</div>

</div>

</span></span></div>

