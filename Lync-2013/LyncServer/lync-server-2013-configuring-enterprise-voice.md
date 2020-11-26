---
title: 'Lync Server 2013: エンタープライズ Voip の構成'
description: 'Lync Server 2013: エンタープライズ Voip を構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Enterprise Voice
ms:assetid: 7df179fa-d3a2-4b23-a433-b750aedf980b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994041(v=OCS.15)
ms:contentKeyID: 51803952
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 49a231b92bf7b04aa3466927a79258f0cbad4e3f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433123"
---
# <a name="configuring-enterprise-voice-in-lync-server-2013"></a><span data-ttu-id="86665-103">Lync Server 2013 でのエンタープライズ Voip の設定</span><span class="sxs-lookup"><span data-stu-id="86665-103">Configuring Enterprise Voice in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="86665-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="86665-104">

<span> </span></span></span>

<span data-ttu-id="86665-105">_**最終更新日:** 2013-03-12_</span><span class="sxs-lookup"><span data-stu-id="86665-105">_**Topic Last Modified:** 2013-03-12_</span></span>

<span data-ttu-id="86665-106">エンタープライズ Voip を展開するには、次の設定を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="86665-106">To deploy Enterprise Voice, you’ll need to configure the following:</span></span>

  - <span data-ttu-id="86665-107">トランクを作成する</span><span class="sxs-lookup"><span data-stu-id="86665-107">Create a Trunk</span></span>

  - <span data-ttu-id="86665-108">ボイスポリシーを定義する</span><span class="sxs-lookup"><span data-stu-id="86665-108">Define a Voice Policy</span></span>

  - <span data-ttu-id="86665-109">ボイスルートの定義</span><span class="sxs-lookup"><span data-stu-id="86665-109">Define a Voice Route</span></span>

  - <span data-ttu-id="86665-110">Enable Users for Enterprise Voice</span><span class="sxs-lookup"><span data-stu-id="86665-110">Enable Users for Enterprise Voice</span></span>

<div>

## <a name="create-a-trunk"></a><span data-ttu-id="86665-111">トランクを作成する</span><span class="sxs-lookup"><span data-stu-id="86665-111">Create a Trunk</span></span>

<span data-ttu-id="86665-112">エンタープライズ Voip 展開で trunks を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="86665-112">You must define trunks in your Enterprise Voice deployment.</span></span> <span data-ttu-id="86665-113">Location-Based ルーティングの場合は、トランクごとにトランク構成を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="86665-113">For Location-Based Routing, you must create a trunk configuration per trunk.</span></span> <span data-ttu-id="86665-114">Lync Server Topology Builder を使用して、trunks を定義し、Lync Server Windows PowerShell コマンド、新規 Set-cstrunkconfiguration、Lync Server コントロールパネルを使用して、対応するトランク構成を定義します。</span><span class="sxs-lookup"><span data-stu-id="86665-114">Use the Lync Server Topology Builder to define your trunks, and use the Lync Server Windows PowerShell command, New-CsTrunkConfiguration, or the Lync Server Control Panel to define the corresponding trunk configurations.</span></span> <span data-ttu-id="86665-115">トランク構成での Location-Based ルーティングを有効にする方法について詳しくは、「Trunks へのルーティング Location-Based を有効にする」を参照してください。「 [Lync Server 2013 で Location-Based ルーティング](lync-server-2013-enabling-location-based-routing.md)を有効にする」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="86665-115">More information on how to enable Location-Based Routing on trunk configurations can be found in the section, Enable Location-Based Routing to Trunks, in the topic, [Enabling Location-Based Routing in Lync Server 2013](lync-server-2013-enabling-location-based-routing.md).</span></span> <span data-ttu-id="86665-116">この例では、次の表はこのシナリオで使用される trunks を示しています。</span><span class="sxs-lookup"><span data-stu-id="86665-116">For this example, the following table illustrates the trunks used in this scenario.</span></span>

<span data-ttu-id="86665-117">詳細については、「 [Lync Server 2013 のトポロジビルダーで追加の trunks を定義](lync-server-2013-define-additional-trunks-in-topology-builder.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="86665-117">For more information, see [Define additional trunks in Topology Builder in Lync Server 2013](lync-server-2013-define-additional-trunks-in-topology-builder.md).</span></span>


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
<th><span data-ttu-id="86665-118">トランク名</span><span class="sxs-lookup"><span data-stu-id="86665-118">Trunk name</span></span></th>
<th><span data-ttu-id="86665-119">システムの種類</span><span class="sxs-lookup"><span data-stu-id="86665-119">System type</span></span></th>
<th><span data-ttu-id="86665-120">名前</span><span class="sxs-lookup"><span data-stu-id="86665-120">Name</span></span></th>
<th><span data-ttu-id="86665-121">場所</span><span class="sxs-lookup"><span data-stu-id="86665-121">Location</span></span></th>
<th><span data-ttu-id="86665-122">仲介サーバー</span><span class="sxs-lookup"><span data-stu-id="86665-122">Mediation Server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="86665-123">トランク1の DEL-GW</span><span class="sxs-lookup"><span data-stu-id="86665-123">Trunk 1 DEL-GW</span></span></p></td>
<td><p><span data-ttu-id="86665-124">PSTN ゲートウェイ</span><span class="sxs-lookup"><span data-stu-id="86665-124">PSTN gateway</span></span></p></td>
<td><p><span data-ttu-id="86665-125">DEL-GW</span><span class="sxs-lookup"><span data-stu-id="86665-125">DEL-GW</span></span></p></td>
<td><p><span data-ttu-id="86665-126">Delhi</span><span class="sxs-lookup"><span data-stu-id="86665-126">Delhi</span></span></p></td>
<td><p><span data-ttu-id="86665-127">MS1</span><span class="sxs-lookup"><span data-stu-id="86665-127">MS1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86665-128">トランク 2 HYD</span><span class="sxs-lookup"><span data-stu-id="86665-128">Trunk 2 HYD-GW</span></span></p></td>
<td><p><span data-ttu-id="86665-129">PSTN ゲートウェイ</span><span class="sxs-lookup"><span data-stu-id="86665-129">PSTN gateway</span></span></p></td>
<td><p><span data-ttu-id="86665-130">HYD</span><span class="sxs-lookup"><span data-stu-id="86665-130">HYD-GW</span></span></p></td>
<td><p><span data-ttu-id="86665-131">Hyderabad</span><span class="sxs-lookup"><span data-stu-id="86665-131">Hyderabad</span></span></p></td>
<td><p><span data-ttu-id="86665-132">MS1</span><span class="sxs-lookup"><span data-stu-id="86665-132">MS1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="86665-133">トランク 3 DEL-PBX</span><span class="sxs-lookup"><span data-stu-id="86665-133">Trunk 3 DEL-PBX</span></span></p></td>
<td><p><span data-ttu-id="86665-134">PBX</span><span class="sxs-lookup"><span data-stu-id="86665-134">PBX</span></span></p></td>
<td><p><span data-ttu-id="86665-135">DEL-PBX</span><span class="sxs-lookup"><span data-stu-id="86665-135">DEL-PBX</span></span></p></td>
<td><p><span data-ttu-id="86665-136">Delhi</span><span class="sxs-lookup"><span data-stu-id="86665-136">Delhi</span></span></p></td>
<td><p><span data-ttu-id="86665-137">MS1</span><span class="sxs-lookup"><span data-stu-id="86665-137">MS1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86665-138">トランク 4 HYD</span><span class="sxs-lookup"><span data-stu-id="86665-138">Trunk 4 HYD-PBX</span></span></p></td>
<td><p><span data-ttu-id="86665-139">PBX</span><span class="sxs-lookup"><span data-stu-id="86665-139">PBX</span></span></p></td>
<td><p><span data-ttu-id="86665-140">HYD</span><span class="sxs-lookup"><span data-stu-id="86665-140">HYD-PBX</span></span></p></td>
<td><p><span data-ttu-id="86665-141">Hyderabad</span><span class="sxs-lookup"><span data-stu-id="86665-141">Hyderabad</span></span></p></td>
<td><p><span data-ttu-id="86665-142">MS1</span><span class="sxs-lookup"><span data-stu-id="86665-142">MS1</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="defines-voice-policies"></a><span data-ttu-id="86665-143">ボイスポリシーを定義します</span><span class="sxs-lookup"><span data-stu-id="86665-143">Defines Voice Policies</span></span>

<span data-ttu-id="86665-144">エンタープライズ Voip の展開には、音声ポリシーを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="86665-144">You must define voice policies for your Enterprise Voice deployment.</span></span> <span data-ttu-id="86665-145">ボイスポリシーを定義して、Location-Based ルーティングを使用するために必要なユーザーが一部しかない場合は、ユーザーのサブセットに対して Location-Based ルーティングの制限を適用します。</span><span class="sxs-lookup"><span data-stu-id="86665-145">Define a Voice Policy to enforce Location-Based Routing restrictions to a subset of users if only a subset of them is required to use Location-Based Routing.</span></span> <span data-ttu-id="86665-146">この例では、次の表はこのシナリオで使用される音声ポリシーを示しています。</span><span class="sxs-lookup"><span data-stu-id="86665-146">For this example, the following table illustrates the voice policies used in this scenario.</span></span> <span data-ttu-id="86665-147">この表には、Location-Based ルーティングに固有の設定のみが含まれています。</span><span class="sxs-lookup"><span data-stu-id="86665-147">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

<span data-ttu-id="86665-148">詳細については、「 [ボイスポリシーと PSTN 使用状況レコードを構成して、Lync Server 2013 での通話機能と特権を承認する](lync-server-2013-configuring-voice-policies-and-pstn-usage-records-to-authorize-calling-features-and-privileges.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="86665-148">For more information, see [Configuring voice policies and PSTN usage records to authorize calling features and privileges in Lync Server 2013](lync-server-2013-configuring-voice-policies-and-pstn-usage-records-to-authorize-calling-features-and-privileges.md).</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="86665-149">ボイスポリシー1</span><span class="sxs-lookup"><span data-stu-id="86665-149">Voice policy 1</span></span></th>
<th><span data-ttu-id="86665-150">ボイスポリシー2</span><span class="sxs-lookup"><span data-stu-id="86665-150">Voice policy 2</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="86665-151">ボイスポリシー ID</span><span class="sxs-lookup"><span data-stu-id="86665-151">Voice policy ID</span></span></p></td>
<td><p><span data-ttu-id="86665-152">ニューデリーのボイスポリシー</span><span class="sxs-lookup"><span data-stu-id="86665-152">Delhi voice policy</span></span></p></td>
<td><p><span data-ttu-id="86665-153">Hyderabad ボイスポリシー</span><span class="sxs-lookup"><span data-stu-id="86665-153">Hyderabad voice policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86665-154">PSTN の使用状況</span><span class="sxs-lookup"><span data-stu-id="86665-154">PSTN usages</span></span></p></td>
<td><p><span data-ttu-id="86665-155">ニューデリー使用量, PBX Del usage, PBX Hyd usage</span><span class="sxs-lookup"><span data-stu-id="86665-155">Delhi usage, PBX Del usage, PBX Hyd usage</span></span></p></td>
<td><p><span data-ttu-id="86665-156">Hyderabad usage、PBX Hyd usage、PBX Del usage</span><span class="sxs-lookup"><span data-stu-id="86665-156">Hyderabad usage, PBX Hyd usage, PBX Del usage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="86665-157">PreventPSTNTollBypass</span><span class="sxs-lookup"><span data-stu-id="86665-157">PreventPSTNTollBypass</span></span></p></td>
<td><p><span data-ttu-id="86665-158">False</span><span class="sxs-lookup"><span data-stu-id="86665-158">False</span></span></p></td>
<td><p><span data-ttu-id="86665-159">False</span><span class="sxs-lookup"><span data-stu-id="86665-159">False</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="define-voice-routes"></a><span data-ttu-id="86665-160">ボイスルートの定義</span><span class="sxs-lookup"><span data-stu-id="86665-160">Define Voice Routes</span></span>

<span data-ttu-id="86665-161">エンタープライズ Voip 展開には、ボイスルーティングを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="86665-161">You must define voice routes for your Enterprise Voice deployment.</span></span> <span data-ttu-id="86665-162">この例では、次の表はこのシナリオで使用されるボイスルートを示しています。</span><span class="sxs-lookup"><span data-stu-id="86665-162">For this example, the following table illustrates the voice routes used in this scenario.</span></span> <span data-ttu-id="86665-163">この表には、Location-Based ルーティングに固有の設定のみが含まれています。</span><span class="sxs-lookup"><span data-stu-id="86665-163">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

<span data-ttu-id="86665-164">詳細については、「 [Lync Server 2013 で送信通話の音声ルートを構成する](lync-server-2013-configuring-voice-routes-for-outbound-calls.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="86665-164">For more information, see [Configuring voice routes for outbound calls in Lync Server 2013](lync-server-2013-configuring-voice-routes-for-outbound-calls.md).</span></span>


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
<th></th>
<th><span data-ttu-id="86665-165">ボイスルート1</span><span class="sxs-lookup"><span data-stu-id="86665-165">Voice route 1</span></span></th>
<th><span data-ttu-id="86665-166">ボイスルート2</span><span class="sxs-lookup"><span data-stu-id="86665-166">Voice route 2</span></span></th>
<th><span data-ttu-id="86665-167">ボイスルート3</span><span class="sxs-lookup"><span data-stu-id="86665-167">Voice route 3</span></span></th>
<th><span data-ttu-id="86665-168">ボイスルーティング4</span><span class="sxs-lookup"><span data-stu-id="86665-168">Voice route 4</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="86665-169">名前</span><span class="sxs-lookup"><span data-stu-id="86665-169">Name</span></span></p></td>
<td><p><span data-ttu-id="86665-170">ニューデリールート</span><span class="sxs-lookup"><span data-stu-id="86665-170">Delhi route</span></span></p></td>
<td><p><span data-ttu-id="86665-171">Hyderabad ルート</span><span class="sxs-lookup"><span data-stu-id="86665-171">Hyderabad route</span></span></p></td>
<td><p><span data-ttu-id="86665-172">PBX の Del ルート</span><span class="sxs-lookup"><span data-stu-id="86665-172">PBX Del route</span></span></p></td>
<td><p><span data-ttu-id="86665-173">PBX Hyd ルート</span><span class="sxs-lookup"><span data-stu-id="86665-173">PBX Hyd route</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86665-174">PSTN の使用状況</span><span class="sxs-lookup"><span data-stu-id="86665-174">PSTN usages</span></span></p></td>
<td><p><span data-ttu-id="86665-175">ニューデリーの利用状況</span><span class="sxs-lookup"><span data-stu-id="86665-175">Delhi usage</span></span></p></td>
<td><p><span data-ttu-id="86665-176">Hyderabad の使用状況</span><span class="sxs-lookup"><span data-stu-id="86665-176">Hyderabad usage</span></span></p></td>
<td><p><span data-ttu-id="86665-177">PBX の Del の利用状況</span><span class="sxs-lookup"><span data-stu-id="86665-177">PBX Del usage</span></span></p></td>
<td><p><span data-ttu-id="86665-178">PBX Hyd の使用</span><span class="sxs-lookup"><span data-stu-id="86665-178">PBX Hyd usage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="86665-179">トランク</span><span class="sxs-lookup"><span data-stu-id="86665-179">Trunk</span></span></p></td>
<td><p><span data-ttu-id="86665-180">トランク1の DEL-GW</span><span class="sxs-lookup"><span data-stu-id="86665-180">Trunk 1 DEL-GW</span></span></p></td>
<td><p><span data-ttu-id="86665-181">トランク 2 HYD</span><span class="sxs-lookup"><span data-stu-id="86665-181">Trunk 2 HYD-GW</span></span></p></td>
<td><p><span data-ttu-id="86665-182">トランク 3 DEL-PBX</span><span class="sxs-lookup"><span data-stu-id="86665-182">Trunk 3 DEL-PBX</span></span></p></td>
<td><p><span data-ttu-id="86665-183">トランク 4 HYD</span><span class="sxs-lookup"><span data-stu-id="86665-183">Trunk 4 HYD-PBX</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="enable-users-for-enterprise-voice"></a><span data-ttu-id="86665-184">Enable Users for Enterprise Voice</span><span class="sxs-lookup"><span data-stu-id="86665-184">Enable Users for Enterprise Voice</span></span>

<span data-ttu-id="86665-185">エンタープライズ Voip のユーザーを有効にし、以前に定義した音声ポリシーを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="86665-185">Enable users for Enterprise Voice and assign them a voice policy you’ve previously defined.</span></span> <span data-ttu-id="86665-186">この例では、次の表はこのシナリオで使用される割り当てを示しています。</span><span class="sxs-lookup"><span data-stu-id="86665-186">For this example, the following table illustrates the assignment used in this scenario.</span></span> <span data-ttu-id="86665-187">この表には、Location-Based ルーティングに固有の設定のみが含まれています。</span><span class="sxs-lookup"><span data-stu-id="86665-187">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

<span data-ttu-id="86665-188">詳細については、「 [Lync Server 2013 でエンタープライズ voip のユーザーを有効にする](lync-server-2013-enable-users-for-enterprise-voice.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="86665-188">For more information, see [Enable users for Enterprise Voice in Lync Server 2013](lync-server-2013-enable-users-for-enterprise-voice.md).</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="86665-189">ニューデリーにあるユーザ</span><span class="sxs-lookup"><span data-stu-id="86665-189">Users located in Delhi</span></span></th>
<th><span data-ttu-id="86665-190">Hyderabad にあるユーザー</span><span class="sxs-lookup"><span data-stu-id="86665-190">Users located in Hyderabad</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="86665-191">関連付けられている音声ポリシー</span><span class="sxs-lookup"><span data-stu-id="86665-191">Associated voice policy</span></span></p></td>
<td><p><span data-ttu-id="86665-192">ニューデリーのボイスポリシー</span><span class="sxs-lookup"><span data-stu-id="86665-192">Delhi voice policy</span></span></p></td>
<td><p><span data-ttu-id="86665-193">Hyderabad ボイスポリシー</span><span class="sxs-lookup"><span data-stu-id="86665-193">Hyderabad voice policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86665-194">サンプルユーザー</span><span class="sxs-lookup"><span data-stu-id="86665-194">Sample users</span></span></p></td>
<td><p><span data-ttu-id="86665-195">DEL-LYNC-1、DEL-LYNC-2、DEL-LYNC-3</span><span class="sxs-lookup"><span data-stu-id="86665-195">DEL-LYNC-1,DEL-LYNC-2,DEL-LYNC-3</span></span></p></td>
<td><p><span data-ttu-id="86665-196">HYD-1、HYD、LYNC-2、HYD、LYNC-3</span><span class="sxs-lookup"><span data-stu-id="86665-196">HYD-LYNC-1, HYD-LYNC-2, HYD-LYNC-3</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="86665-197">関連項目</span><span class="sxs-lookup"><span data-stu-id="86665-197">See Also</span></span>


[<span data-ttu-id="86665-198">Lync Server 2013 の場所に基づくルーティングの構成</span><span class="sxs-lookup"><span data-stu-id="86665-198">Configuring Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-configuring-location-based-routing.md)  
  

<span data-ttu-id="86665-199"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="86665-199"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

