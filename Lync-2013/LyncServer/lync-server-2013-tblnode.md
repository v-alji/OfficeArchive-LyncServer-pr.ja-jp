---
title: 'Lync Server 2013: tblNode'
description: 'Lync Server 2013: tblNode'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblNode
ms:assetid: a31d2961-aa83-4286-a12e-15d279c95f19
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615024(v=OCS.15)
ms:contentKeyID: 48184960
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d0a5d630621c32cbc54501249c7a679bf4023c60
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423520"
---
# <a name="tblnode-in-lync-server-2013"></a><span data-ttu-id="743d4-103">Lync Server 2013 の tblNode</span><span class="sxs-lookup"><span data-stu-id="743d4-103">tblNode in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="743d4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="743d4-104">

<span> </span></span></span>

<span data-ttu-id="743d4-105">_**最終更新日:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="743d4-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="743d4-106">tblNode には、Lync Server 2013 コントロールパネルと管理コマンドレットで管理されるオブジェクトツリー (カテゴリまたはチャットルームノードを含む) が含まれています。</span><span class="sxs-lookup"><span data-stu-id="743d4-106">tblNode contains the object tree (with category or chat room nodes) as managed in the Lync Server 2013 Control Panel and administrative cmdlets.</span></span>

### <a name="columns"></a><span data-ttu-id="743d4-107">行</span><span class="sxs-lookup"><span data-stu-id="743d4-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="743d4-108">列</span><span class="sxs-lookup"><span data-stu-id="743d4-108">Column</span></span></th>
<th><span data-ttu-id="743d4-109">型</span><span class="sxs-lookup"><span data-stu-id="743d4-109">Type</span></span></th>
<th><span data-ttu-id="743d4-110">説明</span><span class="sxs-lookup"><span data-stu-id="743d4-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="743d4-111">nodeID</span><span class="sxs-lookup"><span data-stu-id="743d4-111">nodeID</span></span></p></td>
<td><p><span data-ttu-id="743d4-112">int (null ではない)</span><span class="sxs-lookup"><span data-stu-id="743d4-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="743d4-113">ノード ID (一意の番号)。</span><span class="sxs-lookup"><span data-stu-id="743d4-113">Node ID (unique number).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="743d4-114">nodeGuid</span><span class="sxs-lookup"><span data-stu-id="743d4-114">nodeGuid</span></span></p></td>
<td><p><span data-ttu-id="743d4-115">GUID、null ではない</span><span class="sxs-lookup"><span data-stu-id="743d4-115">GUID, not null</span></span></p></td>
<td><p><span data-ttu-id="743d4-116">ノード GUID。</span><span class="sxs-lookup"><span data-stu-id="743d4-116">Node GUID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="743d4-117">parentID</span><span class="sxs-lookup"><span data-stu-id="743d4-117">parentID</span></span></p></td>
<td><p><span data-ttu-id="743d4-118">int</span><span class="sxs-lookup"><span data-stu-id="743d4-118">int</span></span></p></td>
<td><p><span data-ttu-id="743d4-119">親のノード ID。</span><span class="sxs-lookup"><span data-stu-id="743d4-119">Node ID of parent.</span></span> <span data-ttu-id="743d4-120">ルートノード (ID 1 の) には、それ自体も親として含まれています。</span><span class="sxs-lookup"><span data-stu-id="743d4-120">The root node (with ID 1) includes itself as parent as well.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="743d4-121">nodeType</span><span class="sxs-lookup"><span data-stu-id="743d4-121">nodeType</span></span></p></td>
<td><p><span data-ttu-id="743d4-122">ビット、null ではない</span><span class="sxs-lookup"><span data-stu-id="743d4-122">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="743d4-123">ノードがカテゴリの場合は True です。</span><span class="sxs-lookup"><span data-stu-id="743d4-123">True if the node is a category.</span></span></p>
<p><span data-ttu-id="743d4-124">ノードがチャットルームの場合は False です。</span><span class="sxs-lookup"><span data-stu-id="743d4-124">False if the node is a chat room.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="743d4-125">nodeName</span><span class="sxs-lookup"><span data-stu-id="743d4-125">nodeName</span></span></p></td>
<td><p><span data-ttu-id="743d4-126">nvarchar (256)、null ではない</span><span class="sxs-lookup"><span data-stu-id="743d4-126">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="743d4-127">ノード名。</span><span class="sxs-lookup"><span data-stu-id="743d4-127">Node name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="743d4-128">nodeDesc</span><span class="sxs-lookup"><span data-stu-id="743d4-128">nodeDesc</span></span></p></td>
<td><p><span data-ttu-id="743d4-129">nvarchar (256)、null ではない</span><span class="sxs-lookup"><span data-stu-id="743d4-129">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="743d4-130">ノードの説明。</span><span class="sxs-lookup"><span data-stu-id="743d4-130">Node description.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="743d4-131">召集</span><span class="sxs-lookup"><span data-stu-id="743d4-131">invite</span></span></p></td>
<td><p><span data-ttu-id="743d4-132">bit</span><span class="sxs-lookup"><span data-stu-id="743d4-132">bit</span></span></p></td>
<td><p><span data-ttu-id="743d4-133">カテゴリの場合:</span><span class="sxs-lookup"><span data-stu-id="743d4-133">For categories:</span></span></p>
<ul>
<li><p><span data-ttu-id="743d4-134">招待がオンの場合は True です。</span><span class="sxs-lookup"><span data-stu-id="743d4-134">True if invites are on.</span></span></p></li>
<li><p><span data-ttu-id="743d4-135">招待がオフの場合は False です。</span><span class="sxs-lookup"><span data-stu-id="743d4-135">False if invites are off.</span></span></p></li>
</ul>
<p><span data-ttu-id="743d4-136">会議室の場合:</span><span class="sxs-lookup"><span data-stu-id="743d4-136">For rooms:</span></span></p>
<ul>
<li><p><span data-ttu-id="743d4-137">[招待] がオフの場合は False です (親カテゴリを上書きします)。</span><span class="sxs-lookup"><span data-stu-id="743d4-137">False if invites are off (overrides the parent category).</span></span></p></li>
<li><p><span data-ttu-id="743d4-138">招待設定が親カテゴリから継承されている場合は Null です。</span><span class="sxs-lookup"><span data-stu-id="743d4-138">Null if the invites setting is inherited from the parent category.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="743d4-139">ログ</span><span class="sxs-lookup"><span data-stu-id="743d4-139">logged</span></span></p></td>
<td><p><span data-ttu-id="743d4-140">bit</span><span class="sxs-lookup"><span data-stu-id="743d4-140">bit</span></span></p></td>
<td><p><span data-ttu-id="743d4-141">カテゴリの場合:</span><span class="sxs-lookup"><span data-stu-id="743d4-141">For categories:</span></span></p>
<ul>
<li><p><span data-ttu-id="743d4-142">チャット履歴がオンの場合は True です。</span><span class="sxs-lookup"><span data-stu-id="743d4-142">True if chat history is on.</span></span></p></li>
<li><p><span data-ttu-id="743d4-143">チャット履歴がオフの場合は False です。</span><span class="sxs-lookup"><span data-stu-id="743d4-143">False if chat history is off.</span></span></p></li>
</ul>
<p><span data-ttu-id="743d4-144">会議室の場合:</span><span class="sxs-lookup"><span data-stu-id="743d4-144">For rooms:</span></span></p>
<ul>
<li><p><span data-ttu-id="743d4-145">空.</span><span class="sxs-lookup"><span data-stu-id="743d4-145">Null.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="743d4-146">filePost</span><span class="sxs-lookup"><span data-stu-id="743d4-146">filePost</span></span></p></td>
<td><p><span data-ttu-id="743d4-147">bit</span><span class="sxs-lookup"><span data-stu-id="743d4-147">bit</span></span></p></td>
<td><p><span data-ttu-id="743d4-148">カテゴリの場合:</span><span class="sxs-lookup"><span data-stu-id="743d4-148">For categories:</span></span></p>
<ul>
<li><p><span data-ttu-id="743d4-149">ファイルのアップロードが許可されている場合は True です。</span><span class="sxs-lookup"><span data-stu-id="743d4-149">True if file uploads are allowed.</span></span></p></li>
<li><p><span data-ttu-id="743d4-150">ファイルのアップロードが許可されていない場合は False です。</span><span class="sxs-lookup"><span data-stu-id="743d4-150">False if file uploads are disallowed.</span></span></p></li>
</ul>
<p><span data-ttu-id="743d4-151">会議室の場合:</span><span class="sxs-lookup"><span data-stu-id="743d4-151">For rooms:</span></span></p>
<ul>
<li><p><span data-ttu-id="743d4-152">空.</span><span class="sxs-lookup"><span data-stu-id="743d4-152">Null.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="743d4-153">無効に</span><span class="sxs-lookup"><span data-stu-id="743d4-153">disabled</span></span></p></td>
<td><p><span data-ttu-id="743d4-154">ビット、null ではない</span><span class="sxs-lookup"><span data-stu-id="743d4-154">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="743d4-155">チャットルームが無効になっている場合は True です。</span><span class="sxs-lookup"><span data-stu-id="743d4-155">True if the chat room is disabled.</span></span> <span data-ttu-id="743d4-156">チャットルームにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="743d4-156">Applies only to chat rooms.</span></span> <span data-ttu-id="743d4-157">(カテゴリの場合は False)。</span><span class="sxs-lookup"><span data-stu-id="743d4-157">(False for categories.)</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="743d4-158">状況</span><span class="sxs-lookup"><span data-stu-id="743d4-158">behavior</span></span></p></td>
<td><p><span data-ttu-id="743d4-159">smallint (null ではない)</span><span class="sxs-lookup"><span data-stu-id="743d4-159">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="743d4-160">動作 (EnumValue テーブルでの検索):</span><span class="sxs-lookup"><span data-stu-id="743d4-160">Behavior (looked up in EnumValue table):</span></span></p>
<ul>
<li><p><span data-ttu-id="743d4-161">4: 標準 (通常のチャットルーム)。</span><span class="sxs-lookup"><span data-stu-id="743d4-161">4: Normal (normal chat rooms).</span></span></p></li>
<li><p><span data-ttu-id="743d4-162">5: 聴衆 (聴衆チャットルーム、発表者のみが投稿できます)。</span><span class="sxs-lookup"><span data-stu-id="743d4-162">5: Auditorium (auditorium chat rooms, only presenters can contribute).</span></span></p></li>
</ul>
<p><span data-ttu-id="743d4-163">チャットルームにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="743d4-163">Applies only to chat rooms.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="743d4-164">明確化</span><span class="sxs-lookup"><span data-stu-id="743d4-164">visibility</span></span></p></td>
<td><p><span data-ttu-id="743d4-165">smallint (null ではない)</span><span class="sxs-lookup"><span data-stu-id="743d4-165">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="743d4-166">Visibility (EnumValue テーブル上で検索される):</span><span class="sxs-lookup"><span data-stu-id="743d4-166">Visibility (looked up on EnumValue table):</span></span></p>
<ul>
<li><p><span data-ttu-id="743d4-167">2: プライベート</span><span class="sxs-lookup"><span data-stu-id="743d4-167">2: Private</span></span></p></li>
<li><p><span data-ttu-id="743d4-168">3: 範囲</span><span class="sxs-lookup"><span data-stu-id="743d4-168">3: Scoped</span></span></p></li>
<li><p><span data-ttu-id="743d4-169">6: 開く</span><span class="sxs-lookup"><span data-stu-id="743d4-169">6: Open</span></span></p></li>
</ul>
<p><span data-ttu-id="743d4-170">チャットルームにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="743d4-170">Applies only to chat rooms.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="743d4-171">siopID</span><span class="sxs-lookup"><span data-stu-id="743d4-171">siopID</span></span></p></td>
<td><p><span data-ttu-id="743d4-172">GUID</span><span class="sxs-lookup"><span data-stu-id="743d4-172">GUID</span></span></p></td>
<td><p><span data-ttu-id="743d4-173">アドインがこのチャットルームに関連付けられている場合は Add-In GUID。</span><span class="sxs-lookup"><span data-stu-id="743d4-173">Add-In GUID if an add-in is associated with this chat room.</span></span> <span data-ttu-id="743d4-174">(カテゴリにはアドインがありません。)</span><span class="sxs-lookup"><span data-stu-id="743d4-174">(Categories do not have add-ins.)</span></span></p>
<p><span data-ttu-id="743d4-175">アドイン情報は、SiopWhiteList リスト表で検索されます。</span><span class="sxs-lookup"><span data-stu-id="743d4-175">The add-in information is looked up in SiopWhiteList table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="743d4-176">nodeAddedBy</span><span class="sxs-lookup"><span data-stu-id="743d4-176">nodeAddedBy</span></span></p></td>
<td><p><span data-ttu-id="743d4-177">int (null ではない)</span><span class="sxs-lookup"><span data-stu-id="743d4-177">int, not null</span></span></p></td>
<td><p><span data-ttu-id="743d4-178">このノードを作成したプリンシパルの ID です。</span><span class="sxs-lookup"><span data-stu-id="743d4-178">ID of the principal that created this node.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="743d4-179">nodeAddedOn</span><span class="sxs-lookup"><span data-stu-id="743d4-179">nodeAddedOn</span></span></p></td>
<td><p><span data-ttu-id="743d4-180">bigint (null ではない)</span><span class="sxs-lookup"><span data-stu-id="743d4-180">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="743d4-181">ノードの作成のタイムスタンプ。</span><span class="sxs-lookup"><span data-stu-id="743d4-181">Time stamp of the node creation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="743d4-182">nodeUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="743d4-182">nodeUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="743d4-183">int (null ではない)</span><span class="sxs-lookup"><span data-stu-id="743d4-183">int, not null</span></span></p></td>
<td><p><span data-ttu-id="743d4-184">このノードの最新の更新を実行したプリンシパルの ID です。</span><span class="sxs-lookup"><span data-stu-id="743d4-184">ID of the principal that did the latest update of this node.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="743d4-185">nodeUpdatedOn</span><span class="sxs-lookup"><span data-stu-id="743d4-185">nodeUpdatedOn</span></span></p></td>
<td><p><span data-ttu-id="743d4-186">bigint (null ではない)</span><span class="sxs-lookup"><span data-stu-id="743d4-186">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="743d4-187">このノードの最新の更新プログラムのタイムスタンプです。</span><span class="sxs-lookup"><span data-stu-id="743d4-187">Time stamp of the latest update of this node.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="743d4-188">purgedOn</span><span class="sxs-lookup"><span data-stu-id="743d4-188">purgedOn</span></span></p></td>
<td><p><span data-ttu-id="743d4-189">datetime</span><span class="sxs-lookup"><span data-stu-id="743d4-189">datetime</span></span></p></td>
<td><p><span data-ttu-id="743d4-190">このノードに影響を与える最新の消去操作 (tblScopedPrincipal テーブルと tblPrincipalRole テーブルからのスコープの削除) の時間。</span><span class="sxs-lookup"><span data-stu-id="743d4-190">Time of the latest purge operation (removal of scopes from tblScopedPrincipal table and roles from tblPrincipalRole table) that affected this node.</span></span> <span data-ttu-id="743d4-191">これは、チャットサービスの内部キャッシュ更新メカニズムによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="743d4-191">This is used by the Chat service’s internal cache update mechanism.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="743d4-192">機能</span><span class="sxs-lookup"><span data-stu-id="743d4-192">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="743d4-193">列</span><span class="sxs-lookup"><span data-stu-id="743d4-193">Column</span></span></th>
<th><span data-ttu-id="743d4-194">説明</span><span class="sxs-lookup"><span data-stu-id="743d4-194">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="743d4-195">nodeID</span><span class="sxs-lookup"><span data-stu-id="743d4-195">nodeID</span></span></p></td>
<td><p><span data-ttu-id="743d4-196">主キー。</span><span class="sxs-lookup"><span data-stu-id="743d4-196">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="743d4-197">状況</span><span class="sxs-lookup"><span data-stu-id="743d4-197">behavior</span></span></p></td>
<td><p><span data-ttu-id="743d4-198">TblEnumValue Id テーブルで参照される外部キー。</span><span class="sxs-lookup"><span data-stu-id="743d4-198">Foreign key with lookup in tblEnumValue.valueID table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="743d4-199">明確化</span><span class="sxs-lookup"><span data-stu-id="743d4-199">visibility</span></span></p></td>
<td><p><span data-ttu-id="743d4-200">TblEnumValue Id テーブルで参照される外部キー。</span><span class="sxs-lookup"><span data-stu-id="743d4-200">Foreign key with lookup in tblEnumValue.valueID table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="743d4-201">parentID</span><span class="sxs-lookup"><span data-stu-id="743d4-201">parentID</span></span></p></td>
<td><p><span data-ttu-id="743d4-202">TblNode テーブルで参照される外部キー。</span><span class="sxs-lookup"><span data-stu-id="743d4-202">Foreign key with lookup in tblNode.nodeID table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="743d4-203">siopID</span><span class="sxs-lookup"><span data-stu-id="743d4-203">siopID</span></span></p></td>
<td><p><span data-ttu-id="743d4-204">TblSiopWhiteList テーブルで参照する外部キー。</span><span class="sxs-lookup"><span data-stu-id="743d4-204">Foreign key with lookup in tblSiopWhiteList.siopId table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="743d4-205">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="743d4-205">


</div>

<span> </span>

</div>

</div>

</span></span></div>

