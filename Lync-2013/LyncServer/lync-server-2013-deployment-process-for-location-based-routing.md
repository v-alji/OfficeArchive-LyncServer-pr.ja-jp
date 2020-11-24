---
title: 'Lync Server 2013: 場所に基づくルーティングの展開プロセス'
description: 'Lync Server 2013: Location-Based ルーティングの展開プロセス。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment process for Location-Based Routing
ms:assetid: 9e923e72-83fc-4a4f-8937-28a55739ed3e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994055(v=OCS.15)
ms:contentKeyID: 51803966
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2c321d9b0eada6e9501b2ded69120feae36be171
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399567"
---
# <a name="deployment-process-for-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="cddb0-103">Lync Server 2013 の場所に基づくルーティングの展開プロセス</span><span class="sxs-lookup"><span data-stu-id="cddb0-103">Deployment process for Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cddb0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cddb0-104">

<span> </span></span></span>

<span data-ttu-id="cddb0-105">_**最終更新日:** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="cddb0-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="cddb0-106">このトピックでは、Location-Based ルーティングの構成に関連するプロセスの概要について説明します。</span><span class="sxs-lookup"><span data-stu-id="cddb0-106">This topic provides an overview of the process involved in configuring Location-Based Routing.</span></span> <span data-ttu-id="cddb0-107">Location-Based ルーティングを構成する前に、エンタープライズ Voip で Lync Server Enterprise Edition または Standard エディションを展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cddb0-107">You must deploy Lync Server Enterprise Edition or Standard Edition with Enterprise Voice before you configure Location-Based Routing.</span></span> <span data-ttu-id="cddb0-108">エンタープライズボイスの展開時に Location-Based ルーティングで必要なコンポーネントが既にインストールされ、有効になっている。</span><span class="sxs-lookup"><span data-stu-id="cddb0-108">The components required by Location-Based Routing are already installed and enabled when you deploy Enterprise Voice.</span></span>

### <a name="location-based-routing-deployment-process"></a><span data-ttu-id="cddb0-109">ルーティング展開プロセスの Location-Based</span><span class="sxs-lookup"><span data-stu-id="cddb0-109">Location-Based Routing Deployment Process</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cddb0-110">段階</span><span class="sxs-lookup"><span data-stu-id="cddb0-110">Phase</span></span></th>
<th><span data-ttu-id="cddb0-111">ステップ</span><span class="sxs-lookup"><span data-stu-id="cddb0-111">Steps</span></span></th>
<th><span data-ttu-id="cddb0-112">必要なグループおよび役割</span><span class="sxs-lookup"><span data-stu-id="cddb0-112">Required groups and roles</span></span></th>
<th><span data-ttu-id="cddb0-113">「展開」のドキュメント</span><span class="sxs-lookup"><span data-stu-id="cddb0-113">Deployment documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cddb0-114">エンタープライズ VoIP の展開</span><span class="sxs-lookup"><span data-stu-id="cddb0-114">Deploy Enterprise Voice</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="cddb0-115">Trunks を構成する</span><span class="sxs-lookup"><span data-stu-id="cddb0-115">Configure Trunks</span></span></p></li>
<li><p><span data-ttu-id="cddb0-116">音声ポリシーを作成する</span><span class="sxs-lookup"><span data-stu-id="cddb0-116">Create Voice Policies</span></span></p></li>
<li><p><span data-ttu-id="cddb0-117">ボイスルートの定義</span><span class="sxs-lookup"><span data-stu-id="cddb0-117">Define Voice Routes</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="cddb0-118">CSVoiceAdmins</span><span class="sxs-lookup"><span data-stu-id="cddb0-118">CSVoiceAdmins</span></span><br />
<span data-ttu-id="cddb0-119">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="cddb0-119">CsAdministrator</span></span><br />
<span data-ttu-id="cddb0-120">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="cddb0-120">CsServerAdministrator</span></span></p></td>
<td><p><span data-ttu-id="cddb0-121">エンタープライズボイスの展開</span><span class="sxs-lookup"><span data-stu-id="cddb0-121">Deploying Enterprise Voice</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cddb0-122">エンタープライズ Voip の展開を確認する</span><span class="sxs-lookup"><span data-stu-id="cddb0-122">Verify your Enterprise Voice deployment</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="cddb0-123">CSVoiceAdmins</span><span class="sxs-lookup"><span data-stu-id="cddb0-123">CSVoiceAdmins</span></span><br />
<span data-ttu-id="cddb0-124">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="cddb0-124">CsAdministrator</span></span><br />
<span data-ttu-id="cddb0-125">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="cddb0-125">CsServerAdministrator</span></span></p></td>
<td> </td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cddb0-126">ネットワークのリージョン、サイト、サブネットを構成する</span><span class="sxs-lookup"><span data-stu-id="cddb0-126">Configure network regions, sites, and subnets</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="cddb0-127">ネットワークの領域を作成する</span><span class="sxs-lookup"><span data-stu-id="cddb0-127">Create network regions</span></span></p></li>
<li><p><span data-ttu-id="cddb0-128">ネットワークサイトを作成する</span><span class="sxs-lookup"><span data-stu-id="cddb0-128">Create network sites</span></span></p></li>
<li><p><span data-ttu-id="cddb0-129">サブネットとネットワークサイトを関連付ける</span><span class="sxs-lookup"><span data-stu-id="cddb0-129">Associates subnets with network sites</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="cddb0-130">CSVoiceAdmins</span><span class="sxs-lookup"><span data-stu-id="cddb0-130">CSVoiceAdmins</span></span><br />
<span data-ttu-id="cddb0-131">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="cddb0-131">CsAdministrator</span></span><br />
<span data-ttu-id="cddb0-132">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="cddb0-132">CsServerAdministrator</span></span></p></td>
<td><p><span data-ttu-id="cddb0-133">ネットワークの領域、サイト、サブネットについて</span><span class="sxs-lookup"><span data-stu-id="cddb0-133">About Network Regions, Sites, and Subnets</span></span><br />
<span data-ttu-id="cddb0-134">ネットワーク領域を作成または変更する</span><span class="sxs-lookup"><span data-stu-id="cddb0-134">Create or Modify a Network Region</span></span><br />
<span data-ttu-id="cddb0-135">ネットワークサイトを作成または変更する</span><span class="sxs-lookup"><span data-stu-id="cddb0-135">Create or Modify a Network Site</span></span><br />
<span data-ttu-id="cddb0-136">サブネットとネットワークサイトを関連付ける</span><span class="sxs-lookup"><span data-stu-id="cddb0-136">Associate a Subnet with a Network Site</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cddb0-137">Location-Based ルーティングを構成する</span><span class="sxs-lookup"><span data-stu-id="cddb0-137">Configure Location-Based Routing</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="cddb0-138">ボイスルーティングポリシーを作成する</span><span class="sxs-lookup"><span data-stu-id="cddb0-138">Create voice routing policies</span></span></p></li>
<li><p><span data-ttu-id="cddb0-139">トランクごとに個別のトランク構成を定義する</span><span class="sxs-lookup"><span data-stu-id="cddb0-139">Define separate trunk configuration per trunk</span></span></p></li>
<li><p><span data-ttu-id="cddb0-140">ボイスポリシーの変更</span><span class="sxs-lookup"><span data-stu-id="cddb0-140">Modify voice policies</span></span></p></li>
<li><p><span data-ttu-id="cddb0-141">Location-Based ルーティング構成を有効にする</span><span class="sxs-lookup"><span data-stu-id="cddb0-141">Enable Location-Based Routing configuration</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="cddb0-142">CSVoiceAdmins</span><span class="sxs-lookup"><span data-stu-id="cddb0-142">CSVoiceAdmins</span></span><br />
<span data-ttu-id="cddb0-143">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="cddb0-143">CsAdministrator</span></span><br />
<span data-ttu-id="cddb0-144">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="cddb0-144">CsServerAdministrator</span></span></p></td>
<td></td>
</tr>
</tbody>
</table>


<div>

## <a name="sample-deployment"></a><span data-ttu-id="cddb0-145">展開の例</span><span class="sxs-lookup"><span data-stu-id="cddb0-145">Sample Deployment</span></span>

<span data-ttu-id="cddb0-146">次の展開は、Location-Based ルーティングによって有効になるメカニズムの詳細を示すために使用されます。</span><span class="sxs-lookup"><span data-stu-id="cddb0-146">The following deployment is used to illustrate further the mechanisms enabled by Location-Based Routing.</span></span>

<span data-ttu-id="cddb0-147">![4784 e1bd2230-b359-24572b6ce02d](images/JJ994055.e1bd2230-44da-4784-b359-24572b6ce02d(OCS.15).png "4784 e1bd2230-b359-24572b6ce02d")</span><span class="sxs-lookup"><span data-stu-id="cddb0-147">![e1bd2230-44da-4784-b359-24572b6ce02d](images/JJ994055.e1bd2230-44da-4784-b359-24572b6ce02d(OCS.15).png "e1bd2230-44da-4784-b359-24572b6ce02d")</span></span>

<div>

## <a name="incoming-pstn-calls"></a><span data-ttu-id="cddb0-148">着信 PSTN 通話</span><span class="sxs-lookup"><span data-stu-id="cddb0-148">Incoming PSTN calls</span></span>

<span data-ttu-id="cddb0-149">管理者は、Location-Based ルーティングのために着信をルーティングするように定義されたトランクを有効にして、「サイト1ゲートウェイ」をサイト1に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="cddb0-149">An administrator can enable the trunk defined to route calls to “Site 1 Gateway” for Location-Based Routing and associate the “Site 1 Gateway” to site 1.</span></span> <span data-ttu-id="cddb0-150">有効にすると、"サイト1ゲートウェイ" 経由でルーティングされた通話は、サイト1にあるユーザーにのみルーティングされます。</span><span class="sxs-lookup"><span data-stu-id="cddb0-150">Once enabled, calls that are routed through “Site 1 Gateway“ will only be routed to users that are located in site 1.</span></span> <span data-ttu-id="cddb0-151">サイト2などのサイト内のユーザーに送信される "サイト1ゲートウェイ" トランク経由でルーティングされたすべての通話は、PSTN の有料電話のバイパスを防ぐためにブロックされます。</span><span class="sxs-lookup"><span data-stu-id="cddb0-151">All calls routed through the “Site 1 Gateway” trunk destined to users in a different site, such as site 2 will be blocked to prevent PSTN toll bypass.</span></span>

<span data-ttu-id="cddb0-152">"サイト1ゲートウェイ" 経由でのすべての着信 PSTN 通話は、サイト1にあるエンドポイントにのみルーティングできます。</span><span class="sxs-lookup"><span data-stu-id="cddb0-152">All incoming PSTN calls through “Site 1 Gateway” will only be allowed to route to endpoints located in site 1.</span></span> <span data-ttu-id="cddb0-153">たとえば、"Lync user 1" がサイト2に転送されると、"サイト1ゲートウェイ" を経由するすべての着信 PSTN 通話は、サイト2にある "Lync user 1" エンドポイントにルーティングされません。</span><span class="sxs-lookup"><span data-stu-id="cddb0-153">For example, when “Lync user 1” travels to site 2, all incoming PSTN calls through “Site 1 Gateway” will not be routed to “Lync user 1” endpoints located in site 2.</span></span> <span data-ttu-id="cddb0-154">"Lync user 1" は、ユーザーの位置情報を特定できない不明のネットワークサイトに移動する場合に、同じルーティングルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="cddb0-154">The same routing rule applies if “Lync user 1” travels to an unknown network site where the user’s location can’t be determined.</span></span>

<span data-ttu-id="cddb0-155">次の表は、このコンテキストでの "Lync user 1" のユーザーエクスペリエンスをまとめたものです。</span><span class="sxs-lookup"><span data-stu-id="cddb0-155">The following table outlines the user experience of “Lync user 1” in this context.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="cddb0-156">ネットワークサイト1にある Lync ユーザー1エンドポイント</span><span class="sxs-lookup"><span data-stu-id="cddb0-156">Lync user 1 endpoints located in network site 1</span></span></th>
<th><span data-ttu-id="cddb0-157">ネットワークサイト2にある Lync ユーザー1エンドポイント</span><span class="sxs-lookup"><span data-stu-id="cddb0-157">Lync user 1 endpoints located in network site 2</span></span></th>
<th><span data-ttu-id="cddb0-158">不明のネットワークサイトにある Lync ユーザー1エンドポイント</span><span class="sxs-lookup"><span data-stu-id="cddb0-158">Lync user 1 endpoints located in unknown network site</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cddb0-159">Lync ユーザー1への着信 PSTN 通話</span><span class="sxs-lookup"><span data-stu-id="cddb0-159">Inbound PSTN calls to Lync user 1</span></span></p></td>
<td><p><span data-ttu-id="cddb0-160">通話はこの場所のエンドポイントにルーティングされます</span><span class="sxs-lookup"><span data-stu-id="cddb0-160">Calls are routed to endpoints in this location</span></span></p></td>
<td><p><span data-ttu-id="cddb0-161">通話はこの場所のエンドポイントにはルーティングされません</span><span class="sxs-lookup"><span data-stu-id="cddb0-161">Calls are not routed to endpoints in this location</span></span></p></td>
<td><p><span data-ttu-id="cddb0-162">通話はこの場所のエンドポイントにはルーティングされません</span><span class="sxs-lookup"><span data-stu-id="cddb0-162">Calls are not routed to endpoints in this location</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="outgoing-pstn-calls"></a><span data-ttu-id="cddb0-163">発信 PSTN 通話</span><span class="sxs-lookup"><span data-stu-id="cddb0-163">Outgoing PSTN calls</span></span>

<span data-ttu-id="cddb0-164">音声ルートは、ユーザーに直接割り当てられている音声ポリシーと、ネットワークサイトに割り当てられているボイスルーティングポリシーの両方で参照されます。</span><span class="sxs-lookup"><span data-stu-id="cddb0-164">Voice routes are referenced in both Voice Policies assigned directly to users, and Voice Routing Policies assigned to network sites.</span></span> <span data-ttu-id="cddb0-165">どちらのポリシーにもルートへの参照が含まれており、異なる方法で通話をルーティングするために使うことができます。</span><span class="sxs-lookup"><span data-stu-id="cddb0-165">Both policies contain references to routes, which can be used to route a call differently.</span></span> <span data-ttu-id="cddb0-166">たとえば、管理者は、特定のユーザーのボイスポリシーで "サイト2ゲートウェイ" を使ってすべての発信通話のルートを定義しながら、ネットワークサイト1のすべてのユーザーに対してボイスルーティングポリシーを定義できます。</span><span class="sxs-lookup"><span data-stu-id="cddb0-166">For example, an administrator can define a Voice Routing Policy for all users located in network site 1 to route all outbound calls through the “Site 1 Gateway” while the Voice Policy of some users define a route for all outbound calls through the “Site 2 Gateway”.</span></span> <span data-ttu-id="cddb0-167">これらのユーザーはネットワークサイト1に配置されていますが、発信通話は "サイト1ゲートウェイ" を介してルーティングされます。</span><span class="sxs-lookup"><span data-stu-id="cddb0-167">While these users are located in network site 1, their outbound calls will be routed through the “Site 1 Gateway”.</span></span>

<span data-ttu-id="cddb0-168">ユーザーが Location-Based ルーティング用に構成されたネットワークサイトに配置されている場合、ネットワークサイトのボイスルーティングポリシールートは、ユーザーのボイスポリシールートを上書きします。</span><span class="sxs-lookup"><span data-stu-id="cddb0-168">When a user is located in a network site configured for Location-Based Routing, the network site’s Voice Routing Policy route overrides the user’s Voice Policy route.</span></span> <span data-ttu-id="cddb0-169">この規則は、別のサイトに一時的に移動するユーザーに特に便利です。</span><span class="sxs-lookup"><span data-stu-id="cddb0-169">This rule is particularly useful for users that temporarily move to a different site.</span></span> <span data-ttu-id="cddb0-170">この例では、ユーザーは自分の位置に対してローカルなゲートウェイを常に使用します。"Lync user 3" を "サイト 2" に配置している場合、すべての送信通話は "サイト2ゲートウェイ" 経由でルーティングされますが、サイト1に移動すると、サイト1のユーザーが送信したすべての発信通話は、"サイト1ゲートウェイ" 経由でルーティングされます。</span><span class="sxs-lookup"><span data-stu-id="cddb0-170">In this particular case a user will always use a gateway that is local to his location; if “Lync user 3” is located at “Site 2”, all his outbound calls will be routed via “Site 2 Gateway”, but if he travels to site 1, all his outbound calls placed while he’s at site 1 will be routed through “Site 1 Gateway”.</span></span>

<span data-ttu-id="cddb0-171">次の表は、Lync ユーザー1が次のネットワークサイトから発信通話を発信した場合のユーザーエクスペリエンスを示しています。</span><span class="sxs-lookup"><span data-stu-id="cddb0-171">The following table illustrates the user experience of Lync user 1 placing an outbound call from the following network sites.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="cddb0-172">ネットワークサイト1</span><span class="sxs-lookup"><span data-stu-id="cddb0-172">Network site 1</span></span></th>
<th><span data-ttu-id="cddb0-173">ネットワークサイト2</span><span class="sxs-lookup"><span data-stu-id="cddb0-173">Network site 2</span></span></th>
<th><span data-ttu-id="cddb0-174">不明のネットワークサイト、または Location-Based ルーティングでは有効ではありません</span><span class="sxs-lookup"><span data-stu-id="cddb0-174">Unknown network site or not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cddb0-175">発信の承認</span><span class="sxs-lookup"><span data-stu-id="cddb0-175">Authorization of outbound calls</span></span></p></td>
<td><p><span data-ttu-id="cddb0-176">Lync ユーザー1のボイスポリシー</span><span class="sxs-lookup"><span data-stu-id="cddb0-176">Lync user 1 voice policy</span></span></p></td>
<td><p><span data-ttu-id="cddb0-177">Lync ユーザー1のボイスポリシー</span><span class="sxs-lookup"><span data-stu-id="cddb0-177">Lync user 1 voice policy</span></span></p></td>
<td><p><span data-ttu-id="cddb0-178">Lync ユーザー1のボイスポリシー</span><span class="sxs-lookup"><span data-stu-id="cddb0-178">Lync user 1 voice policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cddb0-179">発信通話のルーティング</span><span class="sxs-lookup"><span data-stu-id="cddb0-179">Routing of outbound calls</span></span></p></td>
<td><p><span data-ttu-id="cddb0-180">サイト1ボイスルーティングポリシー</span><span class="sxs-lookup"><span data-stu-id="cddb0-180">Site 1 voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="cddb0-181">サイト2ボイスルーティングポリシー</span><span class="sxs-lookup"><span data-stu-id="cddb0-181">Site 2 voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="cddb0-182">ユーザのボイスポリシーおよび Location-Based ルーティング用に有効になっていないシステムのみ</span><span class="sxs-lookup"><span data-stu-id="cddb0-182">User’s voice policy and only to systems not enabled for Location-Based Routing</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="call-transfers-and-forwards"></a><span data-ttu-id="cddb0-183">着信の転送と転送</span><span class="sxs-lookup"><span data-stu-id="cddb0-183">Call transfers and forwards</span></span>

<span data-ttu-id="cddb0-184">通話が転送または転送される場合、通話のルーティングは Location-Based ルーティングの影響を受けます。</span><span class="sxs-lookup"><span data-stu-id="cddb0-184">When calls are transferred or forwarded, the routing of calls is affected by Location-Based Routing.</span></span>

<span data-ttu-id="cddb0-185">次の表は、Lync ユーザー1が、別の Lync ユーザーに PSTN 通話を転送または転送する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="cddb0-185">The following table depicts Lync user 1 transferring or forwarding a PSTN call to another Lync user.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cddb0-186">着信転送または転送を開始するユーザー</span><span class="sxs-lookup"><span data-stu-id="cddb0-186">User initiating call transfer or forward</span></span></th>
<th><span data-ttu-id="cddb0-187">Lync ユーザー2</span><span class="sxs-lookup"><span data-stu-id="cddb0-187">Lync user 2</span></span></th>
<th><span data-ttu-id="cddb0-188">Lync ユーザー4</span><span class="sxs-lookup"><span data-stu-id="cddb0-188">Lync user 4</span></span></th>
<th><span data-ttu-id="cddb0-189">ネットワークサイトの Lync ユーザーが Location-Based ルーティングを有効にしていない</span><span class="sxs-lookup"><span data-stu-id="cddb0-189">Lync user in network site not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cddb0-190">Lync ユーザー1</span><span class="sxs-lookup"><span data-stu-id="cddb0-190">Lync user 1</span></span></p></td>
<td><p><span data-ttu-id="cddb0-191">通話または着信を転送できます。</span><span class="sxs-lookup"><span data-stu-id="cddb0-191">Call forward or transfer is allowed</span></span></p></td>
<td><p><span data-ttu-id="cddb0-192">通話または着信を転送できません。</span><span class="sxs-lookup"><span data-stu-id="cddb0-192">Call forward or transfer is not allowed</span></span></p></td>
<td><p><span data-ttu-id="cddb0-193">通話または着信を転送できません。</span><span class="sxs-lookup"><span data-stu-id="cddb0-193">Call forward or transfer is not allowed</span></span></p></td>
</tr>
</tbody>
</table>

  
<span data-ttu-id="cddb0-194">次の表は、転送される Lync ユーザーの場所 (Lync ユーザー2、Lync ユーザー4など) と PSTN エンドポイントとの間の通話のルーティング方法にどのように影響するかを Location-Based する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="cddb0-194">The following table illustrates how Location-Based Routing affects how the call is routed based on the location of the Lync user being transferred (Lync user 2, Lync user 4, etc) to a PSTN endpoint</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cddb0-195">通話が転送または転送されるエンドポイント</span><span class="sxs-lookup"><span data-stu-id="cddb0-195">Endpoint where call is transferred or forwarded to</span></span></th>
<th><span data-ttu-id="cddb0-196">Lync ユーザー2</span><span class="sxs-lookup"><span data-stu-id="cddb0-196">Lync user 2</span></span></th>
<th><span data-ttu-id="cddb0-197">Lync ユーザー4</span><span class="sxs-lookup"><span data-stu-id="cddb0-197">Lync user 4</span></span></th>
<th><span data-ttu-id="cddb0-198">ネットワークサイトの Lync ユーザーが Location-Based ルーティングを有効にしていない</span><span class="sxs-lookup"><span data-stu-id="cddb0-198">Lync user in network site not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cddb0-199">PSTN エンドポイント</span><span class="sxs-lookup"><span data-stu-id="cddb0-199">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="cddb0-200">着信の転送または転送は、サイト1のゲートウェイ経由でサイト1のボイスルーティングポリシーと出口を経由してルーティングされます</span><span class="sxs-lookup"><span data-stu-id="cddb0-200">Call forward or transfer is routed through site 1 voice routing policy and egress via Site 1 Gateway</span></span></p></td>
<td><p><span data-ttu-id="cddb0-201">着信の転送または転送は、サイト2ゲートウェイ経由でサイト2のボイスルーティングポリシーと出口を経由してルーティングされる</span><span class="sxs-lookup"><span data-stu-id="cddb0-201">Call forward or transfer is routed through site 2 voice routing policy and egress via Site 2 Gateway</span></span></p></td>
<td><p><span data-ttu-id="cddb0-202">着信の転送または転送は、Lync ユーザーの音声ポリシーを通じてルーティングされ、位置情報に基づくルーティングのためにゲートウェイ経由で送信が有効になっていない (使用可能な場合)</span><span class="sxs-lookup"><span data-stu-id="cddb0-202">Call forward or transfer is routed through the Lync user voice policy and egress via a gateway not enabled for location-based routing (if available)</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="simultaneous-ringing"></a><span data-ttu-id="cddb0-203">同時呼び出し</span><span class="sxs-lookup"><span data-stu-id="cddb0-203">Simultaneous ringing</span></span>

<span data-ttu-id="cddb0-204">サンプルトポロジで位置情報に基づくルーティングを構成すると、次の操作が強制されます。</span><span class="sxs-lookup"><span data-stu-id="cddb0-204">Once location-based routing is configured in the sample topology, the following interactions are enforced.</span></span>

<span data-ttu-id="cddb0-205">次の表では、Location-Based ルーティングで、さまざまな Lync ユーザー (Lync ユーザー2、Lync ユーザー4など) の同時呼び出しを許可するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="cddb0-205">The following table illustrates whether Location-Based Routing allows simultaneous ringing for different Lync users (i.e. Lync user 2, Lync user 4, etc).</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cddb0-206">着信 PSTN 通話ターゲット</span><span class="sxs-lookup"><span data-stu-id="cddb0-206">Incoming PSTN call target</span></span></th>
<th><span data-ttu-id="cddb0-207">Lync ユーザー2</span><span class="sxs-lookup"><span data-stu-id="cddb0-207">Lync user 2</span></span></th>
<th><span data-ttu-id="cddb0-208">Lync ユーザー4</span><span class="sxs-lookup"><span data-stu-id="cddb0-208">Lync user 4</span></span></th>
<th><span data-ttu-id="cddb0-209">ネットワークサイトの Lync ユーザーが Location-Based ルーティングを有効にしていない</span><span class="sxs-lookup"><span data-stu-id="cddb0-209">Lync user in network site not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cddb0-210">Lync ユーザー1</span><span class="sxs-lookup"><span data-stu-id="cddb0-210">Lync user 1</span></span></p></td>
<td><p><span data-ttu-id="cddb0-211">同時呼び出しが許可されている</span><span class="sxs-lookup"><span data-stu-id="cddb0-211">Simultaneous ring is allowed</span></span></p></td>
<td><p><span data-ttu-id="cddb0-212">同時呼び出しが許可されていない</span><span class="sxs-lookup"><span data-stu-id="cddb0-212">Simultaneous ring is not allowed</span></span></p></td>
<td><p><span data-ttu-id="cddb0-213">同時呼び出しが許可されていない</span><span class="sxs-lookup"><span data-stu-id="cddb0-213">Simultaneous ring is not allowed</span></span></p></td>
</tr>
</tbody>
</table>

  
<span data-ttu-id="cddb0-214">次の表では、Location-Based ルーティングで、さまざまな Lync ユーザーから PSTN エンドポイントへの同時呼び出しを許可するかどうか (Lync ユーザー2、Lync ユーザー4など) を示します。</span><span class="sxs-lookup"><span data-stu-id="cddb0-214">The following table illustrates whether Location-Based Routing allows simultaneous ringing to a PSTN endpoint from different Lync users (i.e. Lync user 2, Lync user 4, etc).</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cddb0-215">同時呼び出しのターゲット ユーザー</span><span class="sxs-lookup"><span data-stu-id="cddb0-215">Simultaneous ring target</span></span></th>
<th><span data-ttu-id="cddb0-216">Lync ユーザー2</span><span class="sxs-lookup"><span data-stu-id="cddb0-216">Lync user 2</span></span></th>
<th><span data-ttu-id="cddb0-217">Lync ユーザー4</span><span class="sxs-lookup"><span data-stu-id="cddb0-217">Lync user 4</span></span></th>
<th><span data-ttu-id="cddb0-218">ネットワークサイトの Lync ユーザーが Location-Based ルーティングを有効にしていない</span><span class="sxs-lookup"><span data-stu-id="cddb0-218">Lync user in network site not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cddb0-219">Lync ユーザー1携帯電話 (PSTN エンドポイント)</span><span class="sxs-lookup"><span data-stu-id="cddb0-219">Lync user 1 mobile phone (PSTN endpoint)</span></span></p></td>
<td><p><span data-ttu-id="cddb0-220">ネットワークサイト1のボイスルーティングポリシーと出口によるルーティング (サイト1ゲートウェイ経由)</span><span class="sxs-lookup"><span data-stu-id="cddb0-220">Call routed through network site 1’s voice routing policy and egress via site 1 gateway</span></span></p></td>
<td><p><span data-ttu-id="cddb0-221">サイト2ゲートウェイ経由でのネットワークサイト2のボイスルーティングポリシーと出口による通話</span><span class="sxs-lookup"><span data-stu-id="cddb0-221">Call routed through network site 2’s voice routing policy and egress via site 2 gateway</span></span></p></td>
<td><p><span data-ttu-id="cddb0-222">発信者の音声ポリシーを通してルーティングし、Location-Based ルーティング用に PSTN ゲートウェイ経由で着信する</span><span class="sxs-lookup"><span data-stu-id="cddb0-222">Call routed through the caller voice policy and will egress via a PSTN gateway not enabled for Location-Based Routing</span></span></p></td>
</tr>
</tbody>
</table>


</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="cddb0-223">関連項目</span><span class="sxs-lookup"><span data-stu-id="cddb0-223">See Also</span></span>


[<span data-ttu-id="cddb0-224">Lync Server 2013 での場所に基づくルーティングの計画</span><span class="sxs-lookup"><span data-stu-id="cddb0-224">Planning for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-planning-for-location-based-routing.md)  
  

<span data-ttu-id="cddb0-225"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cddb0-225"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

