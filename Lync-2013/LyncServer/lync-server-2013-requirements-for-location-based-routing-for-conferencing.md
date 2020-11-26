---
title: 'Lync Server 2013: 会議の Location-Based ルーティングの要件'
description: 'Lync Server 2013: 会議の Location-Based ルーティングの要件。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Requirements for Location-Based Routing for conferencing
ms:assetid: 766d9286-2c34-4faf-bb3e-f0ca478a70cf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362806(v=OCS.15)
ms:contentKeyID: 56335085
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fbaa1af2690c3148d2ecfb173b13be288a21d80f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442664"
---
# <a name="requirements-for-location-based-routing-for-conferencing-in-lync-server-2013"></a><span data-ttu-id="fec49-103">Lync Server 2013 での会議の Location-Based ルーティングの要件</span><span class="sxs-lookup"><span data-stu-id="fec49-103">Requirements for Location-Based Routing for conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fec49-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fec49-104">

<span> </span></span></span>

<span data-ttu-id="fec49-105">_**最終更新日:** 2013-07-19_</span><span class="sxs-lookup"><span data-stu-id="fec49-105">_**Topic Last Modified:** 2013-07-19_</span></span>

<span data-ttu-id="fec49-106">Location-Based ルーティング会議アプリケーションをインストールして構成するために必要な要件を次に示します。</span><span class="sxs-lookup"><span data-stu-id="fec49-106">The following are the requirements needed for the installation and configuration of the Location-Based Routing Conferencing application:</span></span>

  - <span data-ttu-id="fec49-107">Lync Server 2013 累積更新プログラム2は、トポロジ内のすべてのサーバーまたはプールに展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fec49-107">Lync Server 2013 Cumulative Update 2 must be deployed on all servers or pools in your topology.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="fec49-108">トポロジ内の Lync サーバーまたはプールに Lync Server 2013 累積更新プログラム2以降がインストールされていない場合、Lync 会議の Location-Based ルーティングを適用することはできません。</span><span class="sxs-lookup"><span data-stu-id="fec49-108">If a Lync server or pool in your topology does not have Lync Server 2013 Cumulative Update 2 or higher installed, then enforcement of Location-Based Routing of Lync meetings cannot be guaranteed.</span></span>



</div>

  - <span data-ttu-id="fec49-109">Lync Server 2013 Location-Based ルーティングは、Location-Based ルーティング会議アプリケーションの事前の前提条件です。</span><span class="sxs-lookup"><span data-stu-id="fec49-109">Lync Server 2013 Location-Based Routing is a pre-requisite for Location-Based Routing Conferencing application.</span></span> <span data-ttu-id="fec49-110">Lync Server 2013 Location-Based ルーティングの構成の詳細については、「 [Location-Based ルーティングを構成](lync-server-2013-configuring-location-based-routing.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fec49-110">For further information on configuring Lync Server 2013 Location-Based Routing, please refer to [Configuring Location-Based Routing](lync-server-2013-configuring-location-based-routing.md).</span></span>

  - <span data-ttu-id="fec49-111">Location-Based ルーティング会議アプリケーションの要件は、Lync Server 2013 Location-Based ルーティングの要件と同じです。</span><span class="sxs-lookup"><span data-stu-id="fec49-111">Requirements of Location-Based Routing Conferencing application are the same as the requirements for Lync Server 2013 Location-Based Routing.</span></span> <span data-ttu-id="fec49-112">詳細については、「 [Location-Based ルーティングの計画](lync-server-2013-planning-for-location-based-routing.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fec49-112">For more information, please refer to [Planning for Location-Based Routing](lync-server-2013-planning-for-location-based-routing.md).</span></span>

<div>

## <a name="supported-servers"></a><span data-ttu-id="fec49-113">サポートされているサーバー</span><span class="sxs-lookup"><span data-stu-id="fec49-113">Supported Servers</span></span>

<span data-ttu-id="fec49-114">Location-Based ルーティング会議アプリケーションでは、Lync Server 2013 累積更新プログラム2が、トポロジ内のすべての Front-End プールおよび標準エディションサーバーに展開されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="fec49-114">The Location-Based Routing Conferencing application requires that Lync Server 2013 Cumulative Update 2 is deployed on all Front-End pools and Standard Edition Servers in your topology.</span></span> <span data-ttu-id="fec49-115">使用しているトポロジの一部の Lync サーバーに Lync Server 2013 累積更新プログラム2がインストールされていない場合、Location-Based ルーティングの制限は、Lync 会議とコンサルティングによる通話転送に完全に適用することはできません。</span><span class="sxs-lookup"><span data-stu-id="fec49-115">If Lync Server 2013 Cumulative Update 2 is not installed on some Lync Servers in your topology, Location-Based Routing restrictions cannot be fully enforced on Lync meetings and consultative call transfers.</span></span>

<span data-ttu-id="fec49-116">次の表では、Location-Based ルーティングをサポートするサーバーの役割とバージョンの組み合わせを示します。</span><span class="sxs-lookup"><span data-stu-id="fec49-116">The following table identifies the combination of server roles and versions that support Location-Based Routing.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fec49-117">フロント エンド プールのバージョン</span><span class="sxs-lookup"><span data-stu-id="fec49-117">Front-End Pool version</span></span></p></td>
<td><p><span data-ttu-id="fec49-118">仲介サーバーのバージョン</span><span class="sxs-lookup"><span data-stu-id="fec49-118">Mediation Server version</span></span></p></td>
<td><p><span data-ttu-id="fec49-119">サポート対象</span><span class="sxs-lookup"><span data-stu-id="fec49-119">Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fec49-120">Lync Server 2013 累積更新プログラム 2</span><span class="sxs-lookup"><span data-stu-id="fec49-120">Lync Server 2013 Cumulative Update 2</span></span></p></td>
<td><p><span data-ttu-id="fec49-121">Lync Server 2013 累積更新プログラム 2</span><span class="sxs-lookup"><span data-stu-id="fec49-121">Lync Server 2013 Cumulative Update 2</span></span></p></td>
<td><p><span data-ttu-id="fec49-122">はい</span><span class="sxs-lookup"><span data-stu-id="fec49-122">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fec49-123">Lync Server 2013 累積更新プログラム 2</span><span class="sxs-lookup"><span data-stu-id="fec49-123">Lync Server 2013 Cumulative Update 2</span></span></p></td>
<td><p><span data-ttu-id="fec49-124">Lync Server 2013 累積更新プログラム 1</span><span class="sxs-lookup"><span data-stu-id="fec49-124">Lync Server 2013 Cumulative Update 1</span></span></p></td>
<td><p><span data-ttu-id="fec49-125">不可</span><span class="sxs-lookup"><span data-stu-id="fec49-125">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fec49-126">Lync Server 2013 累積更新プログラム 2</span><span class="sxs-lookup"><span data-stu-id="fec49-126">Lync Server 2013 Cumulative Update 2</span></span></p></td>
<td><p><span data-ttu-id="fec49-127">Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="fec49-127">Lync Server 2010</span></span></p></td>
<td><p><span data-ttu-id="fec49-128">不可</span><span class="sxs-lookup"><span data-stu-id="fec49-128">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fec49-129">Lync Server 2013 累積更新プログラム 2</span><span class="sxs-lookup"><span data-stu-id="fec49-129">Lync Server 2013 Cumulative Update 2</span></span></p></td>
<td><p><span data-ttu-id="fec49-130">Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="fec49-130">Office Communications Server 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="fec49-131">不可</span><span class="sxs-lookup"><span data-stu-id="fec49-131">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fec49-132">Lync Server 2013 累積更新プログラム 1</span><span class="sxs-lookup"><span data-stu-id="fec49-132">Lync Server 2013 Cumulative Update 1</span></span></p></td>
<td><p><span data-ttu-id="fec49-133">任意</span><span class="sxs-lookup"><span data-stu-id="fec49-133">Any</span></span></p></td>
<td><p><span data-ttu-id="fec49-134">不可</span><span class="sxs-lookup"><span data-stu-id="fec49-134">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fec49-135">Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="fec49-135">Lync Server 2010</span></span></p></td>
<td><p><span data-ttu-id="fec49-136">任意</span><span class="sxs-lookup"><span data-stu-id="fec49-136">Any</span></span></p></td>
<td><p><span data-ttu-id="fec49-137">不可</span><span class="sxs-lookup"><span data-stu-id="fec49-137">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fec49-138">Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="fec49-138">Office Communications Server 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="fec49-139">任意</span><span class="sxs-lookup"><span data-stu-id="fec49-139">Any</span></span></p></td>
<td><p><span data-ttu-id="fec49-140">不可</span><span class="sxs-lookup"><span data-stu-id="fec49-140">No</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="supported-clients"></a><span data-ttu-id="fec49-141">サポートされているクライアント</span><span class="sxs-lookup"><span data-stu-id="fec49-141">Supported Clients</span></span>

<span data-ttu-id="fec49-142">Lync 会議の Location-Based ルーティングをサポートする Lync クライアントは、Lync Server 2013 Location-Based ルーティングをサポートしているクライアントと同じです。</span><span class="sxs-lookup"><span data-stu-id="fec49-142">The Lync clients that support Location-Based Routing of Lync meetings are the same clients that support Lync Server 2013 Location-Based Routing.</span></span> <span data-ttu-id="fec49-143">詳細については、「 [クライアントとサーバーの Location-Based ルーティングのサポート](lync-server-2013-client-and-server-support-for-location-based-routing.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fec49-143">For more information, please refer to [Client and Server Support for Location-Based Routing](lync-server-2013-client-and-server-support-for-location-based-routing.md).</span></span>

</div>

<div>

## <a name="mediation-server-requirements-for-consultative-call-transfers"></a><span data-ttu-id="fec49-144">提案型通話転送の仲介サーバー要件</span><span class="sxs-lookup"><span data-stu-id="fec49-144">Mediation Server Requirements for Consultative Call Transfers</span></span>

<span data-ttu-id="fec49-145">Location-Based ルーティング会議アプリケーションでは、提案された通話転送に Location-Based ルーティングの制限を適用するために、スタンドアロンの仲介サーバーを展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fec49-145">The Location-Based Routing Conferencing application requires deploying stand-alone Mediation Servers in order to enforce Location-Based Routing restrictions on consultative call transfers.</span></span>

<span data-ttu-id="fec49-146">提案型の通話転送の Location-Based ルーティングを適用するには、Location-Based ルーティングが必要なネットワーク領域に、仲介サーバーが1つの仲介サーバーピア (PBX、SIP ゲートウェイなど) と関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="fec49-146">To enforce Location-Based Routing of consultative call transfers, the Mediation Server must be associated with only one Mediation Server peer (i.e. PBX, SIP gateway, etc) in network regions where Location-Based Routing is required.</span></span> <span data-ttu-id="fec49-147">追加の仲介サーバーピアが同じネットワーク領域に展開されている場合、仲介サーバーピアは、別の仲介サーバーと関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="fec49-147">If additional Mediation Server peers are deployed in the same network region, the Mediation Server peer must be associated with a different Mediation Server .</span></span> <span data-ttu-id="fec49-148">この要件は、次のように詳細に説明します。</span><span class="sxs-lookup"><span data-stu-id="fec49-148">This Requirement is detailed as follows:</span></span>

  - <span data-ttu-id="fec49-149">複数の仲介サーバーピアに対して1つの仲介サーバーを使用して、複数の SIP trunks で構成されている仲介サーバー経由で、複数のピア (Pbx とゲートウェイ) に対して、コンサルタントによる通話転送が仲介サーバーピアにルーティングされる場合、特定の SIP trunks での提案型通話転送が許可されているが、他の</span><span class="sxs-lookup"><span data-stu-id="fec49-149">Single Mediation Server per multiple Mediation Server peers When a consultative call transfer is routed to a Mediation Server peer through a Mediation Server that’s configured with multiple SIP trunks to multiple peers (i.e. PBXs and gateways), the consultative call transfer is blocked to prevent PSTN toll bypass if the consultative call transfer is permitted through some SIP trunks but disallowed through other SIP trunks.</span></span>
    
    <span data-ttu-id="fec49-150">たとえば、PSTN ゲートウェイ仲介サーバーピアと PBX 仲介サーバーピアをサービスしている単一の仲介サーバーの場合、次の動作が監視されます。</span><span class="sxs-lookup"><span data-stu-id="fec49-150">For example, in the case of a single Mediation Server servicing a PSTN Gateway Mediation Server Peer and a PBX Mediation Server Peer, the following behavior will be observed:</span></span>
    
      - <span data-ttu-id="fec49-151">特定のサイトの Lync ユーザー (つまり、サイト 1) から別のサイト (つまり、サイト 2) の Lync ユーザーに対して、提案型転送を使用して通話を転送しようとすると、PSTN の有料通話を防ぐことはできません。</span><span class="sxs-lookup"><span data-stu-id="fec49-151">When a Lync user from a given site (i.e. site 1) attempts to transfer a call with a PSTN endpoint to a Lync user from a different site (i.e. site 2) via consultative transfer, the call will be disallowed to prevent PSTN toll bypass.</span></span>
    
      - <span data-ttu-id="fec49-152">特定のサイトの Lync ユーザー (サイト 1) と、別のサイト (サイト 1) の PBX エンドポイントを使用して、別のサイト (サイト 2) との通話を発信しようとすると、PSTN 通話の可能性がある場合でも、通話は許可されません。</span><span class="sxs-lookup"><span data-stu-id="fec49-152">When a Lync user from a given site (i.e. site 1) attempts to transfer a call with a PBX endpoint in the same site (site 1) to a Lync user from a different site (i.e. site 2) via consultative transfer, the call will be disallowed even if it doesn’t incur in potential PSTN toll bypassing.</span></span>

  - <span data-ttu-id="fec49-153">仲介サーバーピアごとに個別の仲介サーバー</span><span class="sxs-lookup"><span data-stu-id="fec49-153">Separate Mediation Servers per Mediation Server peer</span></span>
    
    <span data-ttu-id="fec49-154">提案型転送が仲介サーバーピアを対象としている場合は、仲介サーバーによって処理される単一の仲介サーバーピアに対して、コンサルティング転送が評価されます。</span><span class="sxs-lookup"><span data-stu-id="fec49-154">When a consultative transfer is targeted at a Mediation Server Peer, the consultative transfer will be evaluated against the single Mediation Server Peer serviced by the Mediation Server.</span></span> <span data-ttu-id="fec49-155">この通話は、サイト内の他のすべての Mediations サーバーピアが、個別の仲介サーバーによってサービスされている場合でも、PSTN の有料電話による通話は許可されません。</span><span class="sxs-lookup"><span data-stu-id="fec49-155">The call will be disallowed or allowed based in its potential to incur in PSTN toll bypass regardless of all other Mediations Server Peers in the site as they’re serviced by separate Mediation Servers.</span></span>
    
    <span data-ttu-id="fec49-156">たとえば、PSTN ゲートウェイ仲介サーバーピアと PBX 仲介サーバーピアをサービスしている別個の仲介サーバーがある場合は、次の動作が監視されます。</span><span class="sxs-lookup"><span data-stu-id="fec49-156">For example, in the case of a separate Mediation Servers servicing a PSTN Gateway Mediation Server Peer and a PBX Mediation Server Peer, the following behavior will be observed:</span></span>
    
      - <span data-ttu-id="fec49-157">特定のサイトの Lync ユーザー (つまり、サイト 1) から別のサイト (つまり、サイト 2) の Lync ユーザーに対して、提案型転送を使用して通話を転送しようとすると、PSTN の有料通話を防ぐことはできません。</span><span class="sxs-lookup"><span data-stu-id="fec49-157">When a Lync user from a given site (i.e. site 1) attempts to transfer a call with a PSTN endpoint to a Lync user from a different site (i.e. site 2) via consultative transfer, the call will be disallowed to prevent PSTN toll bypass.</span></span>
    
      - <span data-ttu-id="fec49-158">特定のサイトの Lync ユーザー (サイト 1) と、別のサイト (サイト 1) の PBX エンドポイントを使用して、別のサイト (サイト 2) との通話を発信しようとすると、PSTN 通話の可能性があるため、通話は許可されません。</span><span class="sxs-lookup"><span data-stu-id="fec49-158">When a Lync user from a given site (i.e. site 1) attempts to transfer a call with a PBX endpoint in the same site (site 1) to a Lync user from a different site (i.e. site 2) via consultative transfer, the call will be allowed as it doesn’t incur in potential PSTN toll bypassing.</span></span>

</div>

<div>

## <a name="capabilities-not-supported-by-the-location-based-routing-conferencing-application"></a><span data-ttu-id="fec49-159">Location-Based ルーティング会議アプリケーションでサポートされていない機能</span><span class="sxs-lookup"><span data-stu-id="fec49-159">Capabilities Not Supported by the Location-Based Routing Conferencing Application</span></span>

<span data-ttu-id="fec49-160">Location-Based ルーティング会議アプリケーションでは、次の機能はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="fec49-160">The following capabilities are not supported by the Location-Based Routing Conferencing application:</span></span>

  - <span data-ttu-id="fec49-161">ダイヤルイン会議。</span><span class="sxs-lookup"><span data-stu-id="fec49-161">Dial-in conferencing.</span></span> <span data-ttu-id="fec49-162">Location-Based ルーティングは、ダイヤルイン会議には適用できません。</span><span class="sxs-lookup"><span data-stu-id="fec49-162">Location-Based Routing cannot be enforced for Dial-in conferencing.</span></span> <span data-ttu-id="fec49-163">会議開催者が、Location-Based のルーティングが有効になっている Lync ユーザーであっても、特定の会議へのダイヤルイン要求は Location-Based ルーティングによって制限されません。</span><span class="sxs-lookup"><span data-stu-id="fec49-163">Any dial-in request to a given conference will not be restricted by Location-Based Routing even if the conference organizer is a Lync user enabled for Location-Based Routing.</span></span>

  - <span data-ttu-id="fec49-164">Location-Based ルーティング制限を適用する必要がある地域では、会議アクセス番号をプロビジョニングしないことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="fec49-164">It’s recommended not to provision conferencing access numbers in regions where Location-Based Routing restrictions need to be enforced.</span></span>

<span data-ttu-id="fec49-165"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fec49-165"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

