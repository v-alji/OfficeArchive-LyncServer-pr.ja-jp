---
title: 'Lync Server 2013: Grant-CsSetupPermission によって行われた変更'
description: 'Lync Server 2013: Grant-CsSetupPermission によって行われた変更。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Changes made by Grant-CsSetupPermission
ms:assetid: c5801f48-14e3-4fdd-8f14-d52e7af07a57
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205250(v=OCS.15)
ms:contentKeyID: 48185360
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d2a9156c977c993dd32e38fc6816bd08d3f65c1f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435069"
---
# <a name="changes-made-by-grant-cssetuppermission-in-lync-server-2013"></a><span data-ttu-id="3c18e-103">Lync Server 2013 での Grant-CsSetupPermission による変更</span><span class="sxs-lookup"><span data-stu-id="3c18e-103">Changes made by Grant-CsSetupPermission in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3c18e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3c18e-104">

<span> </span></span></span>

<span data-ttu-id="3c18e-105">_**最終更新日:** 2012-06-20_</span><span class="sxs-lookup"><span data-stu-id="3c18e-105">_**Topic Last Modified:** 2012-06-20_</span></span>

<span data-ttu-id="3c18e-106">セットアップを委任するには、特定の Active Directory 組織単位 (OU) の RTCUniversalServerAdmins ユニバーサルグループにアクセス許可を付与します。この OU の RTCUniversalServerAdmins グループのメンバーが、Domain Admins グループのメンバーにならずに、指定したドメインに Lync Server 2013 をインストールできるようにします。</span><span class="sxs-lookup"><span data-stu-id="3c18e-106">To delegate setup, you can grant permissions to the RTCUniversalServerAdmins universal group for a specific Active Directory organizational unit (OU), enabling members of the RTCUniversalServerAdmins group in that OU to install Lync Server 2013 in the specified domain without being members of the Domain Admins group.</span></span>

<span data-ttu-id="3c18e-107">**グラント setuppermissions** コマンドレットは、次の表で指定されているように、OU に対して RTCUniversalServerAdmins group アクセス許可を付与します。</span><span class="sxs-lookup"><span data-stu-id="3c18e-107">The **Grant-CsSetupPermission** cmdlet grants the RTCUniversalServerAdmins group permissions on an OU, as specified in the following table:</span></span>

### <a name="permissions-granted-to-objects-in-the-ou"></a><span data-ttu-id="3c18e-108">OU 内のオブジェクトに付与されているアクセス許可</span><span class="sxs-lookup"><span data-stu-id="3c18e-108">Permissions granted to Objects in the OU</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3c18e-109">権限の対象:</span><span class="sxs-lookup"><span data-stu-id="3c18e-109">Permissions apply to:</span></span></th>
<th><span data-ttu-id="3c18e-110">付与されるアクセス許可:</span><span class="sxs-lookup"><span data-stu-id="3c18e-110">Permissions granted are:</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3c18e-111">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="3c18e-111">RTCUniversalServerAdmins</span></span></p></td>
<td><p><span data-ttu-id="3c18e-112">特殊なアクセス:</span><span class="sxs-lookup"><span data-stu-id="3c18e-112">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="3c18e-113">ServicePrincipalName を読み上げる</span><span class="sxs-lookup"><span data-stu-id="3c18e-113">Read servicePrincipalName</span></span></p></li>
<li><p><span data-ttu-id="3c18e-114">ServicePrincipalName の書き込み</span><span class="sxs-lookup"><span data-stu-id="3c18e-114">Write servicePrincipalName</span></span></p></li>
<li><p><span data-ttu-id="3c18e-115">ツリーの削除</span><span class="sxs-lookup"><span data-stu-id="3c18e-115">Delete tree</span></span></p></li>
<li><p><span data-ttu-id="3c18e-116">ディレクトリの変更の複製</span><span class="sxs-lookup"><span data-stu-id="3c18e-116">Replicating directory changes</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c18e-117">子孫の serviceConnectionPoint オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3c18e-117">Descendant serviceConnectionPoint objects</span></span></p></td>
<td><p><span data-ttu-id="3c18e-118">特殊なアクセス:</span><span class="sxs-lookup"><span data-stu-id="3c18e-118">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="3c18e-119">読み取りアクセス許可</span><span class="sxs-lookup"><span data-stu-id="3c18e-119">Read permissions</span></span></p></li>
<li><p><span data-ttu-id="3c18e-120">書き込み権限</span><span class="sxs-lookup"><span data-stu-id="3c18e-120">Write permissions</span></span></p></li>
<li><p><span data-ttu-id="3c18e-121">子の作成</span><span class="sxs-lookup"><span data-stu-id="3c18e-121">Create child</span></span></p></li>
<li><p><span data-ttu-id="3c18e-122">子の削除</span><span class="sxs-lookup"><span data-stu-id="3c18e-122">Delete child</span></span></p></li>
<li><p><span data-ttu-id="3c18e-123">リストの内容</span><span class="sxs-lookup"><span data-stu-id="3c18e-123">List contents</span></span></p></li>
<li><p><span data-ttu-id="3c18e-124">プロパティの書き込み</span><span class="sxs-lookup"><span data-stu-id="3c18e-124">Write property</span></span></p></li>
<li><p><span data-ttu-id="3c18e-125">プロパティの読み取り</span><span class="sxs-lookup"><span data-stu-id="3c18e-125">Read property</span></span></p></li>
<li><p><span data-ttu-id="3c18e-126">ツリーの削除</span><span class="sxs-lookup"><span data-stu-id="3c18e-126">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c18e-127">下位の Msrtcsip-userenabled true オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3c18e-127">Descendant msRTCSIP-Server objects</span></span></p></td>
<td><p><span data-ttu-id="3c18e-128">特殊なアクセス:</span><span class="sxs-lookup"><span data-stu-id="3c18e-128">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="3c18e-129">プロパティの書き込み</span><span class="sxs-lookup"><span data-stu-id="3c18e-129">Write property</span></span></p></li>
<li><p><span data-ttu-id="3c18e-130">プロパティの読み取り</span><span class="sxs-lookup"><span data-stu-id="3c18e-130">Read property</span></span></p></li>
<li><p><span data-ttu-id="3c18e-131">ツリーの削除</span><span class="sxs-lookup"><span data-stu-id="3c18e-131">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c18e-132">下位の Msrtcsip-userenabled true-WebComponents オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3c18e-132">Descendant msRTCSIP-WebComponents objects</span></span></p></td>
<td><p><span data-ttu-id="3c18e-133">特殊なアクセス:</span><span class="sxs-lookup"><span data-stu-id="3c18e-133">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="3c18e-134">プロパティの書き込み</span><span class="sxs-lookup"><span data-stu-id="3c18e-134">Write property</span></span></p></li>
<li><p><span data-ttu-id="3c18e-135">プロパティの読み取り</span><span class="sxs-lookup"><span data-stu-id="3c18e-135">Read property</span></span></p></li>
<li><p><span data-ttu-id="3c18e-136">ツリーの削除</span><span class="sxs-lookup"><span data-stu-id="3c18e-136">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c18e-137">子孫の Msrtcsip-userenabled true-MCU オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3c18e-137">Descendant msRTCSIP-MCU objects</span></span></p></td>
<td><p><span data-ttu-id="3c18e-138">特殊なアクセス:</span><span class="sxs-lookup"><span data-stu-id="3c18e-138">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="3c18e-139">プロパティの書き込み</span><span class="sxs-lookup"><span data-stu-id="3c18e-139">Write property</span></span></p></li>
<li><p><span data-ttu-id="3c18e-140">プロパティの読み取り</span><span class="sxs-lookup"><span data-stu-id="3c18e-140">Read property</span></span></p></li>
<li><p><span data-ttu-id="3c18e-141">ツリーの削除</span><span class="sxs-lookup"><span data-stu-id="3c18e-141">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c18e-142">子孫の Msrtcsip-userenabled true-MediationServer オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3c18e-142">Descendant msRTCSIP-MediationServer objects</span></span></p></td>
<td><p><span data-ttu-id="3c18e-143">特殊なアクセス:</span><span class="sxs-lookup"><span data-stu-id="3c18e-143">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="3c18e-144">プロパティの書き込み</span><span class="sxs-lookup"><span data-stu-id="3c18e-144">Write property</span></span></p></li>
<li><p><span data-ttu-id="3c18e-145">プロパティの読み取り</span><span class="sxs-lookup"><span data-stu-id="3c18e-145">Read property</span></span></p></li>
<li><p><span data-ttu-id="3c18e-146">ツリーの削除</span><span class="sxs-lookup"><span data-stu-id="3c18e-146">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c18e-147">子 Msrtcsip-userenabled true ApplicationServer オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3c18e-147">Descendant msRTCSIP-ApplicationServer objects</span></span></p></td>
<td><p><span data-ttu-id="3c18e-148">特殊なアクセス:</span><span class="sxs-lookup"><span data-stu-id="3c18e-148">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="3c18e-149">プロパティの書き込み</span><span class="sxs-lookup"><span data-stu-id="3c18e-149">Write property</span></span></p></li>
<li><p><span data-ttu-id="3c18e-150">プロパティの読み取り</span><span class="sxs-lookup"><span data-stu-id="3c18e-150">Read property</span></span></p></li>
<li><p><span data-ttu-id="3c18e-151">ツリーの削除</span><span class="sxs-lookup"><span data-stu-id="3c18e-151">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c18e-152">子 Msrtcsip-userenabled true ConnectionPoint オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3c18e-152">Descendant msRTCSIP-ConnectionPoint objects</span></span></p></td>
<td><p><span data-ttu-id="3c18e-153">特殊なアクセス:</span><span class="sxs-lookup"><span data-stu-id="3c18e-153">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="3c18e-154">プロパティの書き込み</span><span class="sxs-lookup"><span data-stu-id="3c18e-154">Write property</span></span></p></li>
<li><p><span data-ttu-id="3c18e-155">プロパティの読み取り</span><span class="sxs-lookup"><span data-stu-id="3c18e-155">Read property</span></span></p></li>
<li><p><span data-ttu-id="3c18e-156">ツリーの削除</span><span class="sxs-lookup"><span data-stu-id="3c18e-156">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c18e-157">子コンピューターオブジェクト</span><span class="sxs-lookup"><span data-stu-id="3c18e-157">Descendant Computer objects</span></span></p></td>
<td><p><span data-ttu-id="3c18e-158">ServiceConnectionPoint の特殊なアクセス:</span><span class="sxs-lookup"><span data-stu-id="3c18e-158">Special access for serviceConnectionPoint:</span></span></p>
<ul>
<li><p><span data-ttu-id="3c18e-159">子オブジェクトを作成する</span><span class="sxs-lookup"><span data-stu-id="3c18e-159">Create child objects</span></span></p></li>
<li><p><span data-ttu-id="3c18e-160">子オブジェクトを削除する</span><span class="sxs-lookup"><span data-stu-id="3c18e-160">Delete child objects</span></span></p></li>
<li><p><span data-ttu-id="3c18e-161">ツリーの削除</span><span class="sxs-lookup"><span data-stu-id="3c18e-161">Delete tree</span></span></p></li>
</ul>
<p><span data-ttu-id="3c18e-162">パブリック情報への特別なアクセス:</span><span class="sxs-lookup"><span data-stu-id="3c18e-162">Special access for public information:</span></span></p>
<ul>
<li><p><span data-ttu-id="3c18e-163">プロパティの読み取り</span><span class="sxs-lookup"><span data-stu-id="3c18e-163">Read property</span></span></p></li>
</ul>
<p><span data-ttu-id="3c18e-164">DNS ホスト名の特殊なアクセス:</span><span class="sxs-lookup"><span data-stu-id="3c18e-164">Special access for DNS host name:</span></span></p>
<ul>
<li><p><span data-ttu-id="3c18e-165">プロパティの読み取り</span><span class="sxs-lookup"><span data-stu-id="3c18e-165">Read property</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="3c18e-166">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3c18e-166">


</div>

<span> </span>

</div>

</div>

</span></span></div>

