---
title: 'Lync Server 2013: tblPrincipalType'
description: 'Lync Server 2013: tblPrincipalType'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalType
ms:assetid: 32e1c1d6-80f4-4624-bf4e-b4c77d3982fa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558633(v=OCS.15)
ms:contentKeyID: 48183787
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ba0f607d4499b54b16d7ecf8a4e7de603e874788
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398073"
---
# <a name="tblprincipaltype-in-lync-server-2013"></a><span data-ttu-id="8c171-103">Lync Server 2013 の tblPrincipalType</span><span class="sxs-lookup"><span data-stu-id="8c171-103">tblPrincipalType in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8c171-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8c171-104">

<span> </span></span></span>

<span data-ttu-id="8c171-105">_**最終更新日:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="8c171-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="8c171-106">tblPrincipalType には、tblPrincipal テーブルの内容を分類するためのプリンシパルの種類が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8c171-106">tblPrincipalType contains principal types to categorize what is in the tblPrincipal table.</span></span>

### <a name="columns"></a><span data-ttu-id="8c171-107">行</span><span class="sxs-lookup"><span data-stu-id="8c171-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8c171-108">列</span><span class="sxs-lookup"><span data-stu-id="8c171-108">Column</span></span></th>
<th><span data-ttu-id="8c171-109">型</span><span class="sxs-lookup"><span data-stu-id="8c171-109">Type</span></span></th>
<th><span data-ttu-id="8c171-110">説明</span><span class="sxs-lookup"><span data-stu-id="8c171-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8c171-111">ptypeID</span><span class="sxs-lookup"><span data-stu-id="8c171-111">ptypeID</span></span></p></td>
<td><p><span data-ttu-id="8c171-112">smallint (null ではない)</span><span class="sxs-lookup"><span data-stu-id="8c171-112">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="8c171-113">プリンシパルの種類 ID。</span><span class="sxs-lookup"><span data-stu-id="8c171-113">Principal type ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c171-114">ptypeDesc</span><span class="sxs-lookup"><span data-stu-id="8c171-114">ptypeDesc</span></span></p></td>
<td><p><span data-ttu-id="8c171-115">nvarchar (256)、null ではない</span><span class="sxs-lookup"><span data-stu-id="8c171-115">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="8c171-116">型の説明。</span><span class="sxs-lookup"><span data-stu-id="8c171-116">Description of the type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c171-117">ptypeIsSystemUser 場合</span><span class="sxs-lookup"><span data-stu-id="8c171-117">ptypeIsSystemUser</span></span></p></td>
<td><p><span data-ttu-id="8c171-118">ビット、null ではない</span><span class="sxs-lookup"><span data-stu-id="8c171-118">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="8c171-119">内部目的で使用されるプリンシパルに対応する型の場合は True です。</span><span class="sxs-lookup"><span data-stu-id="8c171-119">True if the type corresponds to the principals that are used for internal purposes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c171-120">ptypeIsUser</span><span class="sxs-lookup"><span data-stu-id="8c171-120">ptypeIsUser</span></span></p></td>
<td><p><span data-ttu-id="8c171-121">ビット、null ではない</span><span class="sxs-lookup"><span data-stu-id="8c171-121">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="8c171-122">型がユーザーの型である場合は True です。</span><span class="sxs-lookup"><span data-stu-id="8c171-122">True if the type is a user type.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="8c171-123">キー</span><span class="sxs-lookup"><span data-stu-id="8c171-123">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8c171-124">列</span><span class="sxs-lookup"><span data-stu-id="8c171-124">Column</span></span></th>
<th><span data-ttu-id="8c171-125">説明</span><span class="sxs-lookup"><span data-stu-id="8c171-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8c171-126">ptypeID</span><span class="sxs-lookup"><span data-stu-id="8c171-126">ptypeID</span></span></p></td>
<td><p><span data-ttu-id="8c171-127">主キー。</span><span class="sxs-lookup"><span data-stu-id="8c171-127">Primary key.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="principal-values"></a><span data-ttu-id="8c171-128">プリンシパルの値</span><span class="sxs-lookup"><span data-stu-id="8c171-128">Principal Values</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8c171-129">ID</span><span class="sxs-lookup"><span data-stu-id="8c171-129">ID</span></span></th>
<th><span data-ttu-id="8c171-130">役割</span><span class="sxs-lookup"><span data-stu-id="8c171-130">Role</span></span></th>
<th><span data-ttu-id="8c171-131">説明</span><span class="sxs-lookup"><span data-stu-id="8c171-131">Description</span></span></th>
<th><span data-ttu-id="8c171-132">[ユーザー]</span><span class="sxs-lookup"><span data-stu-id="8c171-132">User</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8c171-133">1</span><span class="sxs-lookup"><span data-stu-id="8c171-133">1</span></span></p></td>
<td><p><span data-ttu-id="8c171-134">任意</span><span class="sxs-lookup"><span data-stu-id="8c171-134">Any</span></span></p></td>
<td><p><span data-ttu-id="8c171-135">既知の型のない汎用プリンシパル。</span><span class="sxs-lookup"><span data-stu-id="8c171-135">Generic principal with no known type.</span></span> <span data-ttu-id="8c171-136">TblPrincipal テーブルでは使用されません。</span><span class="sxs-lookup"><span data-stu-id="8c171-136">Not used in tblPrincipal table.</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c171-137">2</span><span class="sxs-lookup"><span data-stu-id="8c171-137">2</span></span></p></td>
<td><p><span data-ttu-id="8c171-138">任意のユーザー</span><span class="sxs-lookup"><span data-stu-id="8c171-138">AnyUser</span></span></p></td>
<td><p><span data-ttu-id="8c171-139">ユーザーの種類の汎用プリンシパル。</span><span class="sxs-lookup"><span data-stu-id="8c171-139">Generic principal of user type.</span></span> <span data-ttu-id="8c171-140">TblPrincipal テーブルでは使用されません。</span><span class="sxs-lookup"><span data-stu-id="8c171-140">Not used in tblPrincipal table.</span></span></p></td>
<td><p><span data-ttu-id="8c171-141">はい</span><span class="sxs-lookup"><span data-stu-id="8c171-141">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c171-142">3</span><span class="sxs-lookup"><span data-stu-id="8c171-142">3</span></span></p></td>
<td><p><span data-ttu-id="8c171-143">AnyGroup</span><span class="sxs-lookup"><span data-stu-id="8c171-143">AnyGroup</span></span></p></td>
<td><p><span data-ttu-id="8c171-144">グループの意味を持つ汎用プリンシパル。</span><span class="sxs-lookup"><span data-stu-id="8c171-144">Generic principal with group semantic.</span></span> <span data-ttu-id="8c171-145">TblPrincipal テーブルでは使用されません。</span><span class="sxs-lookup"><span data-stu-id="8c171-145">Not used in tblPrincipal table.</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c171-146">4</span><span class="sxs-lookup"><span data-stu-id="8c171-146">4</span></span></p></td>
<td><p><span data-ttu-id="8c171-147">他のお互い</span><span class="sxs-lookup"><span data-stu-id="8c171-147">SystemUser</span></span></p></td>
<td><p><span data-ttu-id="8c171-148">常設チャットサーバーで内部的に使用されているプリンシパル。</span><span class="sxs-lookup"><span data-stu-id="8c171-148">Principal used internally by Persistent Chat Server.</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c171-149">5</span><span class="sxs-lookup"><span data-stu-id="8c171-149">5</span></span></p></td>
<td><p><span data-ttu-id="8c171-150">ユーザー</span><span class="sxs-lookup"><span data-stu-id="8c171-150">User</span></span></p></td>
<td><p><span data-ttu-id="8c171-151">標準ユーザー。</span><span class="sxs-lookup"><span data-stu-id="8c171-151">Regular user.</span></span></p></td>
<td><p><span data-ttu-id="8c171-152">はい</span><span class="sxs-lookup"><span data-stu-id="8c171-152">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c171-153">個</span><span class="sxs-lookup"><span data-stu-id="8c171-153">8</span></span></p></td>
<td><p><span data-ttu-id="8c171-154">修飾</span><span class="sxs-lookup"><span data-stu-id="8c171-154">DC</span></span></p></td>
<td><p><span data-ttu-id="8c171-155">Active Directory ドメインサービスのドメインコントローラー。</span><span class="sxs-lookup"><span data-stu-id="8c171-155">Active Directory Domain Services domain controller.</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c171-156">ファイブ</span><span class="sxs-lookup"><span data-stu-id="8c171-156">9</span></span></p></td>
<td><p><span data-ttu-id="8c171-157">グループ</span><span class="sxs-lookup"><span data-stu-id="8c171-157">Group</span></span></p></td>
<td><p><span data-ttu-id="8c171-158">Active Directory セキュリティグループ。</span><span class="sxs-lookup"><span data-stu-id="8c171-158">Active Directory security group.</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c171-159">常用</span><span class="sxs-lookup"><span data-stu-id="8c171-159">10</span></span></p></td>
<td><p><span data-ttu-id="8c171-160">フォルダー</span><span class="sxs-lookup"><span data-stu-id="8c171-160">Folder</span></span></p></td>
<td><p><span data-ttu-id="8c171-161">Active Directory コンテナーまたは組織単位。</span><span class="sxs-lookup"><span data-stu-id="8c171-161">Active Directory container or organizational unit.</span></span></p></td>
<td></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="8c171-162">関連項目</span><span class="sxs-lookup"><span data-stu-id="8c171-162">See Also</span></span>


[<span data-ttu-id="8c171-163">Lync Server 2013 の tblPrincipal</span><span class="sxs-lookup"><span data-stu-id="8c171-163">tblPrincipal in Lync Server 2013</span></span>](lync-server-2013-tblprincipal.md)  
  

<span data-ttu-id="8c171-164"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8c171-164"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

