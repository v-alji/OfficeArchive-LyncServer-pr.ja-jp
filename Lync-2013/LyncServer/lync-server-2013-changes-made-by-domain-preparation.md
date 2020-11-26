---
title: 'Lync Server 2013: ドメインの準備によって行われた変更'
description: 'Lync Server 2013: ドメインの準備によって行われた変更。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Changes made by domain preparation
ms:assetid: 9191221e-6166-4c2b-837e-fa73d90fdf80
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398742(v=OCS.15)
ms:contentKeyID: 48184845
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 26400bd1c72c6ae3b8dc1f2d2d8f6c6906b80595
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435118"
---
# <a name="changes-made-by-domain-preparation-in-lync-server-2013"></a><span data-ttu-id="35d74-103">Lync Server 2013 でのドメインの準備によって行われた変更</span><span class="sxs-lookup"><span data-stu-id="35d74-103">Changes made by domain preparation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="35d74-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="35d74-104">

<span> </span></span></span>

<span data-ttu-id="35d74-105">_**最終更新日:** 2010-10-18_</span><span class="sxs-lookup"><span data-stu-id="35d74-105">_**Topic Last Modified:** 2010-10-18_</span></span>

<span data-ttu-id="35d74-106">次の表に、ドメインの準備でドメインルート上に作成されるアクセス制御エントリ (Ace) を示します。</span><span class="sxs-lookup"><span data-stu-id="35d74-106">The following table lists the access control entries (ACEs) that domain preparation creates on the domain root.</span></span> <span data-ttu-id="35d74-107">特に注記がない限り、すべての Ace が継承されます。</span><span class="sxs-lookup"><span data-stu-id="35d74-107">All ACEs are inherited unless otherwise noted.</span></span>

<div id="sectionSection0" class="section">

### <a name="aces-added-to-domain-root"></a><span data-ttu-id="35d74-108">ドメインルートに追加された Ace</span><span class="sxs-lookup"><span data-stu-id="35d74-108">ACEs Added to Domain Root</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="35d74-109">AS</span><span class="sxs-lookup"><span data-stu-id="35d74-109">ACE</span></span></th>
<th><span data-ttu-id="35d74-110">RTCUniversal-UserReadOnly-グループ</span><span class="sxs-lookup"><span data-stu-id="35d74-110">RTCUniversal-UserReadOnly-Group</span></span></th>
<th><span data-ttu-id="35d74-111">RTCUniversal-ServerReadOnly-グループ</span><span class="sxs-lookup"><span data-stu-id="35d74-111">RTCUniversal-ServerReadOnly-Group</span></span></th>
<th><span data-ttu-id="35d74-112">RTCUniversal-UserAdmins</span><span class="sxs-lookup"><span data-stu-id="35d74-112">RTCUniversal-UserAdmins</span></span></th>
<th><span data-ttu-id="35d74-113">RTCHSUniversal-Services</span><span class="sxs-lookup"><span data-stu-id="35d74-113">RTCHSUniversal-Services</span></span></th>
<th><span data-ttu-id="35d74-114">Authenticated-Users</span><span class="sxs-lookup"><span data-stu-id="35d74-114">Authenticated-Users</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="35d74-115">読み取りコンテナー (継承されません)</span><span class="sxs-lookup"><span data-stu-id="35d74-115">Read Container (not inherited)</span></span></p></td>
<td><p><span data-ttu-id="35d74-116"><strong>はい</strong></span><span class="sxs-lookup"><span data-stu-id="35d74-116"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="35d74-117"><strong>はい</strong></span><span class="sxs-lookup"><span data-stu-id="35d74-117"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="35d74-118">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-118">No</span></span></p></td>
<td><p><span data-ttu-id="35d74-119">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-119">No</span></span></p></td>
<td><p><span data-ttu-id="35d74-120">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-120">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35d74-121">ユーザー PropertySet の読み取りユーザーアカウントの制限</span><span class="sxs-lookup"><span data-stu-id="35d74-121">Read User PropertySet User-Account-Restrictions</span></span></p></td>
<td><p><span data-ttu-id="35d74-122"><strong>はい</strong></span><span class="sxs-lookup"><span data-stu-id="35d74-122"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="35d74-123">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-123">No</span></span></p></td>
<td><p><span data-ttu-id="35d74-124">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-124">No</span></span></p></td>
<td><p><span data-ttu-id="35d74-125">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-125">No</span></span></p></td>
<td><p><span data-ttu-id="35d74-126">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35d74-127">ユーザー PropertySet Personal-Information を読む</span><span class="sxs-lookup"><span data-stu-id="35d74-127">Read User PropertySet Personal-Information</span></span></p></td>
<td><p><span data-ttu-id="35d74-128"><strong>はい</strong></span><span class="sxs-lookup"><span data-stu-id="35d74-128"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="35d74-129">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-129">No</span></span></p></td>
<td><p><span data-ttu-id="35d74-130">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-130">No</span></span></p></td>
<td><p><span data-ttu-id="35d74-131">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-131">No</span></span></p></td>
<td><p><span data-ttu-id="35d74-132">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-132">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35d74-133">ユーザー PropertySet General-Information を読む</span><span class="sxs-lookup"><span data-stu-id="35d74-133">Read User PropertySet General-Information</span></span></p></td>
<td><p><span data-ttu-id="35d74-134"><strong>はい</strong></span><span class="sxs-lookup"><span data-stu-id="35d74-134"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="35d74-135">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-135">No</span></span></p></td>
<td><p><span data-ttu-id="35d74-136">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-136">No</span></span></p></td>
<td><p><span data-ttu-id="35d74-137">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-137">No</span></span></p></td>
<td><p><span data-ttu-id="35d74-138">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-138">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35d74-139">ユーザー PropertySet Public-Information を読む</span><span class="sxs-lookup"><span data-stu-id="35d74-139">Read User PropertySet Public-Information</span></span></p></td>
<td><p><span data-ttu-id="35d74-140"><strong>はい</strong></span><span class="sxs-lookup"><span data-stu-id="35d74-140"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="35d74-141">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-141">No</span></span></p></td>
<td><p><span data-ttu-id="35d74-142">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-142">No</span></span></p></td>
<td><p><span data-ttu-id="35d74-143">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-143">No</span></span></p></td>
<td><p><span data-ttu-id="35d74-144">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-144">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35d74-145">ユーザー PropertySet RTCUserSearchProperty-Set を読む</span><span class="sxs-lookup"><span data-stu-id="35d74-145">Read User PropertySet RTCUserSearchProperty-Set</span></span></p></td>
<td><p><span data-ttu-id="35d74-146"><strong>はい</strong></span><span class="sxs-lookup"><span data-stu-id="35d74-146"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="35d74-147">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-147">No</span></span></p></td>
<td><p><span data-ttu-id="35d74-148">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-148">No</span></span></p></td>
<td><p><span data-ttu-id="35d74-149">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-149">No</span></span></p></td>
<td><p><span data-ttu-id="35d74-150"><strong>はい</strong></span><span class="sxs-lookup"><span data-stu-id="35d74-150"><strong>Yes</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35d74-151">ユーザー PropertySet RTCPropertySet を読む</span><span class="sxs-lookup"><span data-stu-id="35d74-151">Read User PropertySet RTCPropertySet</span></span></p></td>
<td><p><span data-ttu-id="35d74-152"><strong>はい</strong></span><span class="sxs-lookup"><span data-stu-id="35d74-152"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="35d74-153">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-153">No</span></span></p></td>
<td><p><span data-ttu-id="35d74-154">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-154">No</span></span></p></td>
<td><p><span data-ttu-id="35d74-155">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-155">No</span></span></p></td>
<td><p><span data-ttu-id="35d74-156">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-156">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35d74-157">ユーザープロパティ Proxy-Addresses の書き込み</span><span class="sxs-lookup"><span data-stu-id="35d74-157">Write User Property Proxy-Addresses</span></span></p></td>
<td><p><span data-ttu-id="35d74-158">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-158">No</span></span></p></td>
<td><p><span data-ttu-id="35d74-159">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-159">No</span></span></p></td>
<td><p><span data-ttu-id="35d74-160"><strong>はい</strong></span><span class="sxs-lookup"><span data-stu-id="35d74-160"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="35d74-161">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-161">No</span></span></p></td>
<td><p><span data-ttu-id="35d74-162">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-162">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35d74-163">ユーザー PropertySet の書き込み RTCUserSearchProperty-Set</span><span class="sxs-lookup"><span data-stu-id="35d74-163">Write User PropertySet RTCUserSearchProperty-Set</span></span></p></td>
<td><p><span data-ttu-id="35d74-164">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-164">No</span></span></p></td>
<td><p><span data-ttu-id="35d74-165">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-165">No</span></span></p></td>
<td><p><span data-ttu-id="35d74-166"><strong>はい</strong></span><span class="sxs-lookup"><span data-stu-id="35d74-166"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="35d74-167">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-167">No</span></span></p></td>
<td><p><span data-ttu-id="35d74-168">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-168">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35d74-169">ユーザー PropertySet の書き込み RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="35d74-169">Write User PropertySet RTCPropertySet</span></span></p></td>
<td><p><span data-ttu-id="35d74-170">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-170">No</span></span></p></td>
<td><p><span data-ttu-id="35d74-171">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-171">No</span></span></p></td>
<td><p><span data-ttu-id="35d74-172"><strong>はい</strong></span><span class="sxs-lookup"><span data-stu-id="35d74-172"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="35d74-173">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-173">No</span></span></p></td>
<td><p><span data-ttu-id="35d74-174">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-174">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35d74-175">PropertySet の DS-レプリケーション-すべての Active Directory オブジェクトの変更内容を確認する</span><span class="sxs-lookup"><span data-stu-id="35d74-175">Read PropertySet DS-Replication-Get-Changes of all Active Directory objects</span></span></p></td>
<td><p><span data-ttu-id="35d74-176">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-176">No</span></span></p></td>
<td><p><span data-ttu-id="35d74-177">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-177">No</span></span></p></td>
<td><p><span data-ttu-id="35d74-178">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-178">No</span></span></p></td>
<td><p><span data-ttu-id="35d74-179"><strong>はい</strong></span><span class="sxs-lookup"><span data-stu-id="35d74-179"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="35d74-180">いいえ</span><span class="sxs-lookup"><span data-stu-id="35d74-180">No</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="35d74-181">次の表は、3つの組み込みコンテナー (ユーザー、コンピューター、ドメインコントローラー) で、ドメインの準備によって作成される Ace を示しています。</span><span class="sxs-lookup"><span data-stu-id="35d74-181">The following table lists the ACEs that domain preparation creates in the three built-in containers: Users, Computers, and Domain Controllers.</span></span> <span data-ttu-id="35d74-182">特に注記がない限り、すべての Ace が継承されます。</span><span class="sxs-lookup"><span data-stu-id="35d74-182">All ACEs are inherited unless otherwise noted.</span></span>

### <a name="aces-added-to-built-in-containers"></a><span data-ttu-id="35d74-183">組み込みのコンテナーに追加された Ace</span><span class="sxs-lookup"><span data-stu-id="35d74-183">ACEs Added to Built-in Containers</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="35d74-184">AS</span><span class="sxs-lookup"><span data-stu-id="35d74-184">ACE</span></span></th>
<th><span data-ttu-id="35d74-185">RTCUniversal-UserReadOnly-グループ</span><span class="sxs-lookup"><span data-stu-id="35d74-185">RTCUniversal-UserReadOnly-Group</span></span></th>
<th><span data-ttu-id="35d74-186">RTCUniversal-ServerReadOnly-グループ</span><span class="sxs-lookup"><span data-stu-id="35d74-186">RTCUniversal-ServerReadOnly-Group</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="35d74-187">読み取りコンテナー (継承されません)</span><span class="sxs-lookup"><span data-stu-id="35d74-187">Read Container (not inherited)</span></span></p></td>
<td><p><span data-ttu-id="35d74-188"><strong>はい</strong></span><span class="sxs-lookup"><span data-stu-id="35d74-188"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="35d74-189"><strong>はい</strong></span><span class="sxs-lookup"><span data-stu-id="35d74-189"><strong>Yes</strong></span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="35d74-190">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="35d74-190">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

