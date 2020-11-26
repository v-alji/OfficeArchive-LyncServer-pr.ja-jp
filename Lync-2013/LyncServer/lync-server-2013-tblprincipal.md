---
title: 'Lync Server 2013: tblPrincipal'
description: 'Lync Server 2013: tblPrincipal'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipal
ms:assetid: 79a24502-b4ce-41f0-8979-8caddf535338
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558667(v=OCS.15)
ms:contentKeyID: 48184571
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0f07b37ac4c8ceed5c044b5c263eeee6370adfdc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444414"
---
# <a name="tblprincipal-in-lync-server-2013"></a><span data-ttu-id="341be-103">Lync Server 2013 の tblPrincipal</span><span class="sxs-lookup"><span data-stu-id="341be-103">tblPrincipal in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="341be-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="341be-104">

<span> </span></span></span>

<span data-ttu-id="341be-105">_**最終更新日:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="341be-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="341be-106">tblPrincipal には、ユーザー、フォルダー、グループを含むすべてのプリンシパルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="341be-106">tblPrincipal contains all principals, including users, folders, and groups.</span></span>

### <a name="columns"></a><span data-ttu-id="341be-107">行</span><span class="sxs-lookup"><span data-stu-id="341be-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="341be-108">列</span><span class="sxs-lookup"><span data-stu-id="341be-108">Column</span></span></th>
<th><span data-ttu-id="341be-109">型</span><span class="sxs-lookup"><span data-stu-id="341be-109">Type</span></span></th>
<th><span data-ttu-id="341be-110">説明</span><span class="sxs-lookup"><span data-stu-id="341be-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="341be-111">prinID</span><span class="sxs-lookup"><span data-stu-id="341be-111">prinID</span></span></p></td>
<td><p><span data-ttu-id="341be-112">int (null ではない)</span><span class="sxs-lookup"><span data-stu-id="341be-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="341be-113">プリンシパル ID。</span><span class="sxs-lookup"><span data-stu-id="341be-113">Principal ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="341be-114">prinGuid</span><span class="sxs-lookup"><span data-stu-id="341be-114">prinGuid</span></span></p></td>
<td><p><span data-ttu-id="341be-115">GUID、null ではない</span><span class="sxs-lookup"><span data-stu-id="341be-115">GUID, not null</span></span></p></td>
<td><p><span data-ttu-id="341be-116">プリンシパル GUID。</span><span class="sxs-lookup"><span data-stu-id="341be-116">Principal GUID.</span></span> <span data-ttu-id="341be-117">これは、プライマリキーとして広く使用されており、その意味は Active Directory ドメインサービスの領域にあります。</span><span class="sxs-lookup"><span data-stu-id="341be-117">This is broadly used as an alternate primary key because its meaning crosses over into the Active Directory Domain Services space.</span></span> <span data-ttu-id="341be-118">(キャッシュされるプリンシパルの GUID は、対応する Active Directory オブジェクト GUID と同じです)。</span><span class="sxs-lookup"><span data-stu-id="341be-118">(The GUID for a cached principal is equal to the corresponding Active Directory object GUID.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="341be-119">prinUri</span><span class="sxs-lookup"><span data-stu-id="341be-119">prinUri</span></span></p></td>
<td><p><span data-ttu-id="341be-120">nvarchar (256)、null ではない</span><span class="sxs-lookup"><span data-stu-id="341be-120">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="341be-121">プリンシパル URI。</span><span class="sxs-lookup"><span data-stu-id="341be-121">Principal URI.</span></span> <span data-ttu-id="341be-122">SIP スキームはユーザのために使用され、ma はその他ほとんどすべてに使用されます。</span><span class="sxs-lookup"><span data-stu-id="341be-122">The SIP scheme is used for users, and ma-grp is used for almost everything else.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="341be-123">prinName</span><span class="sxs-lookup"><span data-stu-id="341be-123">prinName</span></span></p></td>
<td><p><span data-ttu-id="341be-124">nvarchar (256)</span><span class="sxs-lookup"><span data-stu-id="341be-124">nvarchar (256)</span></span></p></td>
<td><p><span data-ttu-id="341be-125">共通名。</span><span class="sxs-lookup"><span data-stu-id="341be-125">Common name.</span></span> <span data-ttu-id="341be-126">ユーザーの種類によってのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="341be-126">Used only by user types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="341be-127">prinDisplayName</span><span class="sxs-lookup"><span data-stu-id="341be-127">prinDisplayName</span></span></p></td>
<td><p><span data-ttu-id="341be-128">Nvarchar (256)</span><span class="sxs-lookup"><span data-stu-id="341be-128">Nvarchar (256)</span></span></p></td>
<td><p><span data-ttu-id="341be-129">表示名。</span><span class="sxs-lookup"><span data-stu-id="341be-129">Display name.</span></span> <span data-ttu-id="341be-130">ユーザーの種類によってのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="341be-130">Used only by user types.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="341be-131">prinCompanyName</span><span class="sxs-lookup"><span data-stu-id="341be-131">prinCompanyName</span></span></p></td>
<td><p><span data-ttu-id="341be-132">nvarchar (256)</span><span class="sxs-lookup"><span data-stu-id="341be-132">nvarchar (256)</span></span></p></td>
<td><p><span data-ttu-id="341be-133">会社名。</span><span class="sxs-lookup"><span data-stu-id="341be-133">Company name.</span></span> <span data-ttu-id="341be-134">ユーザーの種類によってのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="341be-134">Used only by user types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="341be-135">メールをプリントする</span><span class="sxs-lookup"><span data-stu-id="341be-135">prinEmail</span></span></p></td>
<td><p><span data-ttu-id="341be-136">nvarchar (256)</span><span class="sxs-lookup"><span data-stu-id="341be-136">nvarchar (256)</span></span></p></td>
<td><p><span data-ttu-id="341be-137">電子メール。</span><span class="sxs-lookup"><span data-stu-id="341be-137">Email.</span></span> <span data-ttu-id="341be-138">ユーザーの種類によってのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="341be-138">Used only by user types.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="341be-139">prinADPath</span><span class="sxs-lookup"><span data-stu-id="341be-139">prinADPath</span></span></p></td>
<td><p><span data-ttu-id="341be-140">nvarchar (384)</span><span class="sxs-lookup"><span data-stu-id="341be-140">nvarchar (384)</span></span></p></td>
<td><p><span data-ttu-id="341be-141">プリンシパルがキャッシュされたバージョンである Active Directory オブジェクトのドメイン名。</span><span class="sxs-lookup"><span data-stu-id="341be-141">Domain name of the Active Directory object that the principal is a cached version of.</span></span> <span data-ttu-id="341be-142">Active Directory オブジェクト (システムユーザーなど) ではない型の場合は Null にすることができます。</span><span class="sxs-lookup"><span data-stu-id="341be-142">Can be Null for types that are not Active Directory objects (such as system users).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="341be-143">プリント</span><span class="sxs-lookup"><span data-stu-id="341be-143">prinADUserPrincipalName</span></span></p></td>
<td><p><span data-ttu-id="341be-144">nvarchar (256)</span><span class="sxs-lookup"><span data-stu-id="341be-144">nvarchar (256)</span></span></p></td>
<td><p><span data-ttu-id="341be-145">ユーザーのユーザープリンシパル名 (UPN)。</span><span class="sxs-lookup"><span data-stu-id="341be-145">User’s user principal name (UPN).</span></span> <span data-ttu-id="341be-146">通常のユーザーの種類でのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="341be-146">Used only by regular user types.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="341be-147">prinDisabled</span><span class="sxs-lookup"><span data-stu-id="341be-147">prinDisabled</span></span></p></td>
<td><p><span data-ttu-id="341be-148">smallint (null ではない)</span><span class="sxs-lookup"><span data-stu-id="341be-148">smallint, not null</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="341be-149">0: プリンシパルは有効です。</span><span class="sxs-lookup"><span data-stu-id="341be-149">0: Principal is active.</span></span></p></li>
<li><p><span data-ttu-id="341be-150">1: ユーザーの SIP 機能が無効になっているため、プリンシパルが無効になっています。</span><span class="sxs-lookup"><span data-stu-id="341be-150">1: Principal is disabled because user’s SIP capabilities are disabled.</span></span></p></li>
<li><p><span data-ttu-id="341be-151">2: 関連付けられている広告オブジェクトが削除されたため、プリンシパルが削除されました。</span><span class="sxs-lookup"><span data-stu-id="341be-151">2: Principal is deleted because associated AD object has been deleted.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="341be-152">prinTypeID</span><span class="sxs-lookup"><span data-stu-id="341be-152">prinTypeID</span></span></p></td>
<td><p><span data-ttu-id="341be-153">smallint (null ではない)</span><span class="sxs-lookup"><span data-stu-id="341be-153">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="341be-154">プリンシパルの種類 (tblPrincipalType テーブルから)。</span><span class="sxs-lookup"><span data-stu-id="341be-154">Principal type (from tblPrincipalType table).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="341be-155">prinPoolID</span><span class="sxs-lookup"><span data-stu-id="341be-155">prinPoolID</span></span></p></td>
<td><p><span data-ttu-id="341be-156">Int</span><span class="sxs-lookup"><span data-stu-id="341be-156">Int</span></span></p></td>
<td><p><span data-ttu-id="341be-157">プリンシパルの Lync プールの割り当て。</span><span class="sxs-lookup"><span data-stu-id="341be-157">Lync pool assignment for the principal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="341be-158">prinPolicyID</span><span class="sxs-lookup"><span data-stu-id="341be-158">prinPolicyID</span></span></p></td>
<td><p><span data-ttu-id="341be-159">Int</span><span class="sxs-lookup"><span data-stu-id="341be-159">Int</span></span></p></td>
<td><p><span data-ttu-id="341be-160">タグの種類のポリシーが存在する場合は、ユーザーの常設チャットサーバーポリシーの値。</span><span class="sxs-lookup"><span data-stu-id="341be-160">Persistent Chat Server policy value for user, if tag type policy is present.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="341be-161">プリント</span><span class="sxs-lookup"><span data-stu-id="341be-161">prinAddedBy</span></span></p></td>
<td><p><span data-ttu-id="341be-162">int</span><span class="sxs-lookup"><span data-stu-id="341be-162">int</span></span></p></td>
<td><p><span data-ttu-id="341be-163">作成者のプリンシパル ID。</span><span class="sxs-lookup"><span data-stu-id="341be-163">Principal ID of the creator.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="341be-164">prinAddedOn</span><span class="sxs-lookup"><span data-stu-id="341be-164">prinAddedOn</span></span></p></td>
<td><p><span data-ttu-id="341be-165">bigint (null ではない)</span><span class="sxs-lookup"><span data-stu-id="341be-165">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="341be-166">作成時刻のタイムスタンプ。</span><span class="sxs-lookup"><span data-stu-id="341be-166">Time stamp for the creation time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="341be-167">プリント</span><span class="sxs-lookup"><span data-stu-id="341be-167">prinUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="341be-168">int</span><span class="sxs-lookup"><span data-stu-id="341be-168">int</span></span></p></td>
<td><p><span data-ttu-id="341be-169">最後に更新したプリンシパルの ID です。</span><span class="sxs-lookup"><span data-stu-id="341be-169">ID of the principal that last updated this.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="341be-170">prinUpdatedOn</span><span class="sxs-lookup"><span data-stu-id="341be-170">prinUpdatedOn</span></span></p></td>
<td><p><span data-ttu-id="341be-171">bigint (null ではない)</span><span class="sxs-lookup"><span data-stu-id="341be-171">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="341be-172">最終更新のタイムスタンプ。</span><span class="sxs-lookup"><span data-stu-id="341be-172">Time stamp for the last update.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="341be-173">prinVerifiedOn</span><span class="sxs-lookup"><span data-stu-id="341be-173">prinVerifiedOn</span></span></p></td>
<td><p><span data-ttu-id="341be-174">datetime。 null ではありません</span><span class="sxs-lookup"><span data-stu-id="341be-174">datetime, not null</span></span></p></td>
<td><p><span data-ttu-id="341be-175">プリンシパルの前回の Active Directory 同期更新の日付と時刻。</span><span class="sxs-lookup"><span data-stu-id="341be-175">Date and time of the last Active Directory Sync refresh for the principal.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="341be-176">機能</span><span class="sxs-lookup"><span data-stu-id="341be-176">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="341be-177">列</span><span class="sxs-lookup"><span data-stu-id="341be-177">Column</span></span></th>
<th><span data-ttu-id="341be-178">説明</span><span class="sxs-lookup"><span data-stu-id="341be-178">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="341be-179">prinID</span><span class="sxs-lookup"><span data-stu-id="341be-179">prinID</span></span></p></td>
<td><p><span data-ttu-id="341be-180">主キー。</span><span class="sxs-lookup"><span data-stu-id="341be-180">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="341be-181">prinTypeID</span><span class="sxs-lookup"><span data-stu-id="341be-181">prinTypeID</span></span></p></td>
<td><p><span data-ttu-id="341be-182">TblPrincipalType テーブルで参照する外部キー。</span><span class="sxs-lookup"><span data-stu-id="341be-182">Foreign key with lookup in tblPrincipalType.ptypeID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="341be-183">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="341be-183">


</div>

<span> </span>

</div>

</div>

</span></span></div>

