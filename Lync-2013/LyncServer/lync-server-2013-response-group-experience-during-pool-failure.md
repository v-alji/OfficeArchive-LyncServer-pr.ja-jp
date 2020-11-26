---
title: Lync Server 2013 のプール障害時の応答グループのエクスペリエンス
description: プールの障害時の Lync Server 2013 応答グループのエクスペリエンス。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Response group experience during pool failure
ms:assetid: 4e00fb38-64b1-4fd9-903d-7639177bc303
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204886(v=OCS.15)
ms:contentKeyID: 48184116
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7d8d5904bc6934d4c330202bafa66d6dd8a16ff5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436245"
---
# <a name="response-group-experience-in-lync-server-2013-during-pool-failure"></a><span data-ttu-id="12b48-103">Lync Server 2013 でのプール障害時の応答グループのエクスペリエンス</span><span class="sxs-lookup"><span data-stu-id="12b48-103">Response group experience in Lync Server 2013 during pool failure</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="12b48-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="12b48-104">

<span> </span></span></span>

<span data-ttu-id="12b48-105">_**最終更新日:** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="12b48-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="12b48-106">このセクションでは、次のステージでの応答グループのアクティビティへの影響について詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="12b48-106">This section describes in detail how response group activity is affected in the following stages:</span></span>

  - <span data-ttu-id="12b48-107">プライマリプールで障害が発生しましたが、フェイルオーバーはまだ開始されていません。</span><span class="sxs-lookup"><span data-stu-id="12b48-107">An outage occurs in the primary pool, but failover is not yet initiated.</span></span>

  - <span data-ttu-id="12b48-108">サービスはバックアッププールにフェールオーバーされました。</span><span class="sxs-lookup"><span data-stu-id="12b48-108">Service is failed over to the backup pool.</span></span>

  - <span data-ttu-id="12b48-109">サービスがプライマリプールに戻されました。</span><span class="sxs-lookup"><span data-stu-id="12b48-109">Service is failed back to the primary pool.</span></span>

<div>

## <a name="user-experience-when-outage-occurs"></a><span data-ttu-id="12b48-110">障害が発生したときのユーザーエクスペリエンス</span><span class="sxs-lookup"><span data-stu-id="12b48-110">User Experience When Outage Occurs</span></span>

<span data-ttu-id="12b48-111">プールまたはサイトの障害が発生したときに、管理者がフェールオーバーを開始していない場合は、次の表で説明するように、応答グループのアクティビティが処理されます。</span><span class="sxs-lookup"><span data-stu-id="12b48-111">When a pool or site outage occurs, but the administrator has not yet initiated failover, response group activity is handled as described in the following table.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="12b48-112">障害回復中は、プライマリプール応答グループが回復中にバックアッププールにインポートされたかどうかによって、通話の動作が異なります。</span><span class="sxs-lookup"><span data-stu-id="12b48-112">During disaster recovery, calls behave differently depending on whether the primary pool response groups were imported to the backup pool during recovery.</span></span> <span data-ttu-id="12b48-113">次の表では、インポートされた応答グループを参照することで、障害回復モード中にプライマリプール応答グループがバックアッププールにインポートされたことを意味します。</span><span class="sxs-lookup"><span data-stu-id="12b48-113">In the following table, references to imported response groups mean that primary pool response groups were imported to the backup pool during disaster recovery mode.</span></span>



</div>

### <a name="outage-occurs"></a><span data-ttu-id="12b48-114">停止が発生する</span><span class="sxs-lookup"><span data-stu-id="12b48-114">Outage Occurs</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="12b48-115">通話の種類またはユーザーの操作</span><span class="sxs-lookup"><span data-stu-id="12b48-115">Type of call or user action</span></span></th>
<th><span data-ttu-id="12b48-116">停止中</span><span class="sxs-lookup"><span data-stu-id="12b48-116">During outage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="12b48-117">エージェントに接続された通話</span><span class="sxs-lookup"><span data-stu-id="12b48-117">Calls connected to an agent</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="12b48-118">通常の通話は接続されたままです。</span><span class="sxs-lookup"><span data-stu-id="12b48-118">Regular calls remain connected.</span></span></p></li>
<li><p><span data-ttu-id="12b48-119">匿名通話は切断されます。</span><span class="sxs-lookup"><span data-stu-id="12b48-119">Anonymous calls are disconnected.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12b48-120">進行中の通話はまだエージェントに接続されていません</span><span class="sxs-lookup"><span data-stu-id="12b48-120">In progress calls not yet connected to an agent</span></span></p></td>
<td><p><span data-ttu-id="12b48-121">通話は切断されます。</span><span class="sxs-lookup"><span data-stu-id="12b48-121">Calls are disconnected.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12b48-122">新規通話</span><span class="sxs-lookup"><span data-stu-id="12b48-122">New calls</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="12b48-123">通話は切断されます。</span><span class="sxs-lookup"><span data-stu-id="12b48-123">Calls are disconnected.</span></span></p></li>
<li><p><span data-ttu-id="12b48-124">応答グループがインポートされた場合、通話はバックアッププールに接続されますが、プライマリプールに所属しているエージェントにはアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="12b48-124">If response groups were imported, calls connect to backup pool, but agents homed in primary pool are unreachable.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12b48-125">応答グループの代理としてのエージェントの呼び出し</span><span class="sxs-lookup"><span data-stu-id="12b48-125">Agent calls on behalf of response group</span></span></p></td>
<td><p><span data-ttu-id="12b48-126">このステージでは、機能が無効になっています。</span><span class="sxs-lookup"><span data-stu-id="12b48-126">Feature is disabled during this stage.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12b48-127">エージェントのサインインとエージェントの情報</span><span class="sxs-lookup"><span data-stu-id="12b48-127">Agent sign-in and agent information</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="12b48-128">プライマリプールによって所有されているエージェントグループは、エージェントコンソールで確認できますが、エージェントはサインインできません。</span><span class="sxs-lookup"><span data-stu-id="12b48-128">Agent groups owned by the primary pool can be viewed on agent console but agents cannot sign in.</span></span></p></li>
<li><p><span data-ttu-id="12b48-129">バックアッププールによって所有されているエージェントグループは、エージェントコンソールで確認でき、エージェントはサインインできます。</span><span class="sxs-lookup"><span data-stu-id="12b48-129">Agent groups owned by the backup pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="12b48-130">インポートされたエージェントグループは、エージェントコンソールには表示されません。</span><span class="sxs-lookup"><span data-stu-id="12b48-130">Imported agent groups are not displayed on agent console.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12b48-131">応答グループの構成</span><span class="sxs-lookup"><span data-stu-id="12b48-131">Response group configuration</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="12b48-132">プライマリプールによって所有される応答グループは、プライマリプールのバックエンドデータベースの可用性に応じて表示できますが、変更はできません。</span><span class="sxs-lookup"><span data-stu-id="12b48-132">Response groups owned by the primary pool can be viewed, depending on the availability of the primary pool’s back-end database, but cannot be modified.</span></span></p></li>
<li><p><span data-ttu-id="12b48-133">バックアッププールによって所有されている応答グループを表示したり、変更したりできます。</span><span class="sxs-lookup"><span data-stu-id="12b48-133">Response groups owned by the backup pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="12b48-134">インポートされた応答グループは、Lync Server コントロールパネルまたは応答グループ構成ツールでは表示できませんが、Lync Server 管理シェルコマンドレットを使用して構成することができます。</span><span class="sxs-lookup"><span data-stu-id="12b48-134">Imported response groups cannot be viewed with Lync Server Control Panel or the Response Group Configuration Tool, but can be configured by using Lync Server Management Shell cmdlets.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="user-experience-during-failover"></a><span data-ttu-id="12b48-135">フェールオーバー中のユーザーエクスペリエンス</span><span class="sxs-lookup"><span data-stu-id="12b48-135">User Experience During Failover</span></span>

<span data-ttu-id="12b48-136">管理者がバックアッププールへのフェールオーバーを呼び出すと、次の表で説明するように、フェールオーバーの際に応答グループのアクティビティが処理されます。</span><span class="sxs-lookup"><span data-stu-id="12b48-136">When an administrator invokes failover to a backup pool, response group activity is handled during and after the failover as described in the following table.</span></span> <span data-ttu-id="12b48-137">最初の列は、実行される可能性があるアクティビティの種類を示します。</span><span class="sxs-lookup"><span data-stu-id="12b48-137">The first column describes the type of activity that might be taking place.</span></span> <span data-ttu-id="12b48-138">中央の列は、バックアッププールへのフェールオーバーにかかる時間の短い間に各アクティビティが処理される方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="12b48-138">The middle column describes how each activity is handled during the brief time that it takes to fail over to the backup pool.</span></span> <span data-ttu-id="12b48-139">最後の列は、フェールオーバープロセスが完了し、バックアッププールがプライマリプールに対して有効になった後の、アクティビティが継続して処理される方法を示します。</span><span class="sxs-lookup"><span data-stu-id="12b48-139">The last column describes how the activity is handled for the duration, after the failover process is complete and the backup pool is standing in for the primary pool.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="12b48-140">障害回復中は、プライマリプール応答グループが回復中にバックアッププールにインポートされたかどうかによって、通話の動作が異なります。</span><span class="sxs-lookup"><span data-stu-id="12b48-140">During disaster recovery, calls behave differently depending on whether the primary pool response groups were imported to the backup pool during recovery.</span></span> <span data-ttu-id="12b48-141">次の表では、インポートされた応答グループを参照することで、障害回復モード中にプライマリプール応答グループがバックアッププールにインポートされたことを意味します。</span><span class="sxs-lookup"><span data-stu-id="12b48-141">In the following table, references to imported response groups mean that primary pool response groups were imported to the backup pool during disaster recovery mode.</span></span>



</div>

### <a name="failover-is-initiated"></a><span data-ttu-id="12b48-142">フェールオーバーが開始される</span><span class="sxs-lookup"><span data-stu-id="12b48-142">Failover Is Initiated</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="12b48-143">通話の種類またはユーザーの操作</span><span class="sxs-lookup"><span data-stu-id="12b48-143">Type of call or user action</span></span></th>
<th><span data-ttu-id="12b48-144">フェールオーバー中</span><span class="sxs-lookup"><span data-stu-id="12b48-144">During Failover</span></span></th>
<th><span data-ttu-id="12b48-145">フェールオーバーの完了後</span><span class="sxs-lookup"><span data-stu-id="12b48-145">After Failover Completes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="12b48-146">エージェントに接続された通話</span><span class="sxs-lookup"><span data-stu-id="12b48-146">Calls connected to an agent</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="12b48-147">通常の通話は接続されたままです。</span><span class="sxs-lookup"><span data-stu-id="12b48-147">Regular calls remain connected.</span></span></p></li>
<li><p><span data-ttu-id="12b48-148">匿名通話は切断されます。</span><span class="sxs-lookup"><span data-stu-id="12b48-148">Anonymous calls are disconnected.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="12b48-149">通常の通話は接続されたままです。</span><span class="sxs-lookup"><span data-stu-id="12b48-149">Regular calls remain connected.</span></span></p></li>
<li><p><span data-ttu-id="12b48-150">インポートした応答グループについては、バックアッププールに到達した匿名の通話が接続されたままになります。</span><span class="sxs-lookup"><span data-stu-id="12b48-150">For imported response groups, anonymous calls that have reached the backup pool remain connected.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12b48-151">進行中の通話はまだエージェントに接続されていません</span><span class="sxs-lookup"><span data-stu-id="12b48-151">In progress calls not yet connected to an agent</span></span></p></td>
<td><p><span data-ttu-id="12b48-152">通話は切断されます。</span><span class="sxs-lookup"><span data-stu-id="12b48-152">Calls are disconnected.</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="12b48-153">応答グループがインポートされなかった場合、この状態の通話はありません。</span><span class="sxs-lookup"><span data-stu-id="12b48-153">If response groups were not imported, no calls are in this status.</span></span></p></li>
<li><p><span data-ttu-id="12b48-154">インポートした応答グループの場合、バックアッププールに到達した通話は接続されたままになります。</span><span class="sxs-lookup"><span data-stu-id="12b48-154">For imported response groups, calls that have reached the backup pool remain connected.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12b48-155">新規通話</span><span class="sxs-lookup"><span data-stu-id="12b48-155">New calls</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="12b48-156">通話は切断されます。</span><span class="sxs-lookup"><span data-stu-id="12b48-156">Calls are disconnected.</span></span></p></li>
<li><p><span data-ttu-id="12b48-157">インポートされた応答グループの場合、通話はバックアッププールに接続しますが、プライマリプールに所属するエージェントにはアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="12b48-157">For imported response groups, calls connect to the backup pool, but agents homed in the primary pool are unreachable.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="12b48-158">応答グループがインポートされなかった場合、通話は切断されます。</span><span class="sxs-lookup"><span data-stu-id="12b48-158">If response groups were not imported, calls are disconnected.</span></span></p></li>
<li><p><span data-ttu-id="12b48-159">インポートされた応答グループの場合、通話はバックアッププールに接続します。</span><span class="sxs-lookup"><span data-stu-id="12b48-159">For imported response groups, calls connect to the backup pool.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12b48-160">応答グループの代理としてのエージェントの呼び出し</span><span class="sxs-lookup"><span data-stu-id="12b48-160">Agent calls on behalf of response group</span></span></p></td>
<td><p><span data-ttu-id="12b48-161">このステージでは機能が無効になっています</span><span class="sxs-lookup"><span data-stu-id="12b48-161">Feature is disabled during this stage</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="12b48-162">応答グループがインポートされなかった場合、通話は失敗します。</span><span class="sxs-lookup"><span data-stu-id="12b48-162">If response groups were not imported, calls fail.</span></span></p></li>
<li><p><span data-ttu-id="12b48-163">インポートされた応答グループの場合、通話は成功します。</span><span class="sxs-lookup"><span data-stu-id="12b48-163">For imported response groups, calls succeed.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12b48-164">エージェントのサインインとエージェントの情報</span><span class="sxs-lookup"><span data-stu-id="12b48-164">Agent sign-in and agent information</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="12b48-165">プライマリプールによって所有されているエージェントグループは、エージェントコンソールで確認できますが、エージェントはサインインできません。</span><span class="sxs-lookup"><span data-stu-id="12b48-165">Agent groups owned by the primary pool can be viewed on agent console but agents cannot sign in.</span></span></p></li>
<li><p><span data-ttu-id="12b48-166">バックアッププールによって所有されているエージェントグループは、エージェントコンソールで確認でき、エージェントはサインインできます。</span><span class="sxs-lookup"><span data-stu-id="12b48-166">Agent groups owned by the backup pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="12b48-167">インポートされたエージェントグループはエージェントコンソールに表示され、エージェントはサインインできます。</span><span class="sxs-lookup"><span data-stu-id="12b48-167">Imported agent groups are displayed on agent console and agents can sign in.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="12b48-168">プライマリプールによって所有されているエージェントグループは、エージェントコンソールで確認できますが、エージェントはサインインできません。</span><span class="sxs-lookup"><span data-stu-id="12b48-168">Agent groups owned by the primary pool can be viewed on agent console but agents cannot sign in.</span></span></p></li>
<li><p><span data-ttu-id="12b48-169">バックアッププールによって所有されているエージェントグループは、エージェントコンソールで確認でき、エージェントはサインインできます。</span><span class="sxs-lookup"><span data-stu-id="12b48-169">Agent groups owned by the backup pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="12b48-170">インポートされたエージェントグループはエージェントコンソールに表示され、エージェントはサインインできます。</span><span class="sxs-lookup"><span data-stu-id="12b48-170">Imported agent groups are displayed on agent console and agents can sign in.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12b48-171">応答グループの構成</span><span class="sxs-lookup"><span data-stu-id="12b48-171">Response group configuration</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="12b48-172">プライマリプールによって所有される応答グループは、プライマリプールのバックエンドデータベースの可用性に応じて表示できますが、変更はできません。</span><span class="sxs-lookup"><span data-stu-id="12b48-172">Response groups owned by the primary pool can be viewed, depending on the availability of the primary pool’s back-end database, but cannot be modified.</span></span></p></li>
<li><p><span data-ttu-id="12b48-173">バックアッププールによって所有されている応答グループを表示したり、変更したりできます。</span><span class="sxs-lookup"><span data-stu-id="12b48-173">Response groups owned by the backup pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="12b48-174">インポートされた応答グループは、Lync Server コントロールパネルまたは応答グループ構成ツールでは表示できませんが、Lync Server 管理シェルコマンドレットを使用して構成することができます。</span><span class="sxs-lookup"><span data-stu-id="12b48-174">Imported response groups cannot be viewed with Lync Server Control Panel or the Response Group Configuration Tool, but can be configured by using Lync Server Management Shell cmdlets.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="12b48-175">プライマリプールによって所有されている応答グループは、バックエンドデータベースの可用性によっては表示できますが、変更はできません。</span><span class="sxs-lookup"><span data-stu-id="12b48-175">Response groups owned by the primary pool can be viewed, depending on the availability of the back end database, but cannot be modified.</span></span></p></li>
<li><p><span data-ttu-id="12b48-176">バックアッププールによって所有されている応答グループを表示したり、変更したりできます。</span><span class="sxs-lookup"><span data-stu-id="12b48-176">Response groups owned by the backup pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="12b48-177">インポートされた応答グループは、Lync Server コントロールパネルまたは応答グループ構成ツールでは表示できませんが、Lync Server 管理シェルコマンドレットを使用して構成することができます。</span><span class="sxs-lookup"><span data-stu-id="12b48-177">Imported response groups cannot be viewed with Lync Server Control Panel or the Response Group Configuration Tool, but can be configured by using Lync Server Management Shell cmdlets.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="user-experience-during-failback"></a><span data-ttu-id="12b48-178">フェールバック中のユーザーエクスペリエンス</span><span class="sxs-lookup"><span data-stu-id="12b48-178">User Experience During Failback</span></span>

<span data-ttu-id="12b48-179">管理者がプライマリプールへのフェールバックを起動すると、次の表で説明するように、フェールバックの際に応答グループのアクティビティが処理されます。</span><span class="sxs-lookup"><span data-stu-id="12b48-179">When an administrator invokes failback to the primary pool, response group activity is handled during and after the failback as described in the following table.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="12b48-180">障害回復中は、プライマリプール応答グループが回復中にバックアッププールにインポートされたかどうかによって、通話の動作が異なります。</span><span class="sxs-lookup"><span data-stu-id="12b48-180">During disaster recovery, calls behave differently depending on whether the primary pool response groups were imported to the backup pool during recovery.</span></span> <span data-ttu-id="12b48-181">次の表では、インポートされた応答グループを参照することで、障害回復モード中にプライマリプール応答グループがバックアッププールにインポートされたことを意味します。</span><span class="sxs-lookup"><span data-stu-id="12b48-181">In the following table, references to imported response groups mean that primary pool response groups were imported to the backup pool during disaster recovery mode.</span></span>



</div>

### <a name="call-handling-in-failback"></a><span data-ttu-id="12b48-182">フェールバックでの通話の処理</span><span class="sxs-lookup"><span data-stu-id="12b48-182">Call Handling in Failback</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="12b48-183">通話の種類またはユーザーの操作</span><span class="sxs-lookup"><span data-stu-id="12b48-183">Type of call or user action</span></span></th>
<th><span data-ttu-id="12b48-184">フェールバック中</span><span class="sxs-lookup"><span data-stu-id="12b48-184">During Failback</span></span></th>
<th><span data-ttu-id="12b48-185">フェールバックの完了後</span><span class="sxs-lookup"><span data-stu-id="12b48-185">After Failback Completes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="12b48-186">エージェントに接続された通話</span><span class="sxs-lookup"><span data-stu-id="12b48-186">Calls connected to an agent</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="12b48-187">通常の通話は接続されたままです。</span><span class="sxs-lookup"><span data-stu-id="12b48-187">Regular calls remain connected.</span></span></p></li>
<li><p><span data-ttu-id="12b48-188">応答グループがインポートされなかった場合、この状態の匿名通話はありません。</span><span class="sxs-lookup"><span data-stu-id="12b48-188">If response groups were not imported, no anonymous calls are in this status.</span></span></p></li>
<li><p><span data-ttu-id="12b48-189">インポートした応答グループでは、匿名の通話は接続されたままになります。</span><span class="sxs-lookup"><span data-stu-id="12b48-189">For imported response groups, anonymous calls remain connected.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="12b48-190">通常の通話は接続されたままです。</span><span class="sxs-lookup"><span data-stu-id="12b48-190">Regular calls remain connected.</span></span></p></li>
<li><p><span data-ttu-id="12b48-191">応答グループがインポートされなかった場合、この状態の匿名通話はありません。</span><span class="sxs-lookup"><span data-stu-id="12b48-191">If response groups were not imported, no anonymous calls are in this status.</span></span></p></li>
<li><p><span data-ttu-id="12b48-192">インポートした応答グループでは、匿名の通話は接続されたままになります。</span><span class="sxs-lookup"><span data-stu-id="12b48-192">For imported response groups, anonymous calls remain connected.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12b48-193">進行中の通話はまだエージェントに接続されていません</span><span class="sxs-lookup"><span data-stu-id="12b48-193">In progress calls not yet connected to an agent</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="12b48-194">応答グループがインポートされなかった場合、この状態の通話はありません。</span><span class="sxs-lookup"><span data-stu-id="12b48-194">If response groups were not imported, no calls are in this status.</span></span></p></li>
<li><p><span data-ttu-id="12b48-195">インポートされた応答グループの場合、通話は切断されます。</span><span class="sxs-lookup"><span data-stu-id="12b48-195">For imported response groups, calls will be disconnected.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="12b48-196">応答グループがインポートされなかった場合、この状態の通話はありません。</span><span class="sxs-lookup"><span data-stu-id="12b48-196">If response groups were not imported, no calls are in this status.</span></span></p></li>
<li><p><span data-ttu-id="12b48-197">インポートされた応答グループの場合、通話は切断されます。</span><span class="sxs-lookup"><span data-stu-id="12b48-197">For imported response groups, calls will be disconnected.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12b48-198">新規通話</span><span class="sxs-lookup"><span data-stu-id="12b48-198">New calls</span></span></p></td>
<td><p><span data-ttu-id="12b48-199">通話はプライマリプールに接続しますが、プライマリプールに所属しているエージェントにはアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="12b48-199">Calls connect to the primary pool, but agents homed in the primary pool are unreachable.</span></span></p></td>
<td><p><span data-ttu-id="12b48-200">通話はプライマリプールに接続します。</span><span class="sxs-lookup"><span data-stu-id="12b48-200">Calls connect to the primary pool.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12b48-201">応答グループの代理としてのエージェントの呼び出し</span><span class="sxs-lookup"><span data-stu-id="12b48-201">Agent calls on behalf of response group</span></span></p></td>
<td><p><span data-ttu-id="12b48-202">このステージでは、機能が無効になっています。</span><span class="sxs-lookup"><span data-stu-id="12b48-202">Feature is disabled during this stage.</span></span></p></td>
<td><p><span data-ttu-id="12b48-203">通話が成功します。</span><span class="sxs-lookup"><span data-stu-id="12b48-203">Calls succeed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12b48-204">エージェントのサインインとエージェントの情報</span><span class="sxs-lookup"><span data-stu-id="12b48-204">Agent sign-in and agent information</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="12b48-205">プライマリプールによって所有されているエージェントグループは、エージェントコンソールで確認できますが、エージェントはサインインできません。</span><span class="sxs-lookup"><span data-stu-id="12b48-205">Agent groups owned by the primary pool can be viewed on agent console but agents cannot sign in.</span></span></p></li>
<li><p><span data-ttu-id="12b48-206">バックアッププールによって所有されているエージェントグループは、エージェントコンソールで確認でき、エージェントはサインインできます。</span><span class="sxs-lookup"><span data-stu-id="12b48-206">Agent groups owned by the backup pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="12b48-207">インポートされたエージェントグループはエージェントコンソールに表示され、エージェントはサインインできます。</span><span class="sxs-lookup"><span data-stu-id="12b48-207">Imported agent groups are displayed on agent console and agents can sign in.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="12b48-208">プライマリプールによって所有されているエージェントグループは、エージェントコンソールで確認でき、エージェントはサインインできます。</span><span class="sxs-lookup"><span data-stu-id="12b48-208">Agent groups owned by the primary pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="12b48-209">バックアッププールによって所有されているエージェントグループは、エージェントコンソールで確認でき、エージェントはサインインできます。</span><span class="sxs-lookup"><span data-stu-id="12b48-209">Agent groups owned by the backup pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="12b48-210">インポートされたエージェントグループは、エージェントコンソールには表示されません。</span><span class="sxs-lookup"><span data-stu-id="12b48-210">Imported agent groups are not displayed on agent console.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12b48-211">応答グループの構成</span><span class="sxs-lookup"><span data-stu-id="12b48-211">Response group configuration</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="12b48-212">プライマリプールによって所有される応答グループは、プライマリプールのバックエンドデータベースの可用性に応じて表示できますが、変更はできません。</span><span class="sxs-lookup"><span data-stu-id="12b48-212">Response groups owned by the primary pool can be viewed, depending on the availability of the primary pool’s back-end database, but cannot be modified.</span></span></p></li>
<li><p><span data-ttu-id="12b48-213">バックアッププールによって所有されている応答グループを表示したり、変更したりできます。</span><span class="sxs-lookup"><span data-stu-id="12b48-213">Response groups owned by the backup pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="12b48-214">インポートされた応答グループは、Lync Server コントロールパネルまたは応答グループ構成ツールでは表示できませんが、Lync Server 管理シェルコマンドレットを使用して構成することができます。</span><span class="sxs-lookup"><span data-stu-id="12b48-214">Imported response groups cannot be viewed with Lync Server Control Panel or the Response Group Configuration Tool, but can be configured by using Lync Server Management Shell cmdlets.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="12b48-215">プライマリプールによって所有されている応答グループを表示したり、変更したりできます。</span><span class="sxs-lookup"><span data-stu-id="12b48-215">Response groups owned by the primary pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="12b48-216">バックアッププールによって所有されている応答グループを表示したり、変更したりできます。</span><span class="sxs-lookup"><span data-stu-id="12b48-216">Response groups owned by the backup pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="12b48-217">インポートされた応答グループは、Lync Server コントロールパネルまたは応答グループ構成ツールでは表示できませんが、Lync Server 管理シェルコマンドレットを使用して構成することができます。</span><span class="sxs-lookup"><span data-stu-id="12b48-217">Imported response groups cannot be viewed with Lync Server Control Panel or the Response Group Configuration Tool, but can be configured by using Lync Server Management Shell cmdlets.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="12b48-218">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="12b48-218">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

