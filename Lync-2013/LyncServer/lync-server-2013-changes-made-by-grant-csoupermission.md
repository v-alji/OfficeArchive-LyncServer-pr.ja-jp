---
title: 'Lync Server 2013: Grant-CsOUPermission によって行われた変更'
description: 'Lync Server 2013: 許可によって行われた変更。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Changes made by Grant-CsOUPermission
ms:assetid: d744d352-1ad9-4447-8e2b-28e768d2ed1b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205310(v=OCS.15)
ms:contentKeyID: 48185564
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 10d3db0e9dde380628690bc016e2b4bd2ec85b54
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435055"
---
# <a name="changes-made-by-grant-csoupermission-in-lync-server-2013"></a><span data-ttu-id="01e94-103">Lync Server 2013 での Grant-CsOUPermission による変更</span><span class="sxs-lookup"><span data-stu-id="01e94-103">Changes made by Grant-CsOUPermission in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="01e94-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="01e94-104">

<span> </span></span></span>

<span data-ttu-id="01e94-105">_**最終更新日:** 2012-06-20_</span><span class="sxs-lookup"><span data-stu-id="01e94-105">_**Topic Last Modified:** 2012-06-20_</span></span>

<span data-ttu-id="01e94-106">Lync Server 2013 管理を委任するために、フォレストの準備によって作成された RTC ユニバーサルグループのメンバーが、Domain Admins グループのメンバーにならずに Ou にアクセスできるように、指定された組織単位 (Ou) にアクセス許可を追加できます。</span><span class="sxs-lookup"><span data-stu-id="01e94-106">To delegate Lync Server 2013 administration, you can add permissions to specified organizational units (OUs) so that members of the RTC universal groups created by forest preparation can access the OUs without being members of the Domain Admins group.</span></span>

<span data-ttu-id="01e94-107">**Grant-CsOuPermission** コマンドレットは、次の表に示すように、指定した OU 内のオブジェクトへのアクセス許可を付与します。</span><span class="sxs-lookup"><span data-stu-id="01e94-107">The **Grant-CsOuPermission** cmdlet grants permissions to objects in the specified OU as specified in the following tables.</span></span>

<div>

## <a name="granting-permission-for-user-objects"></a><span data-ttu-id="01e94-108">ユーザーオブジェクトのアクセス許可の付与</span><span class="sxs-lookup"><span data-stu-id="01e94-108">Granting Permission for User Objects</span></span>

<span data-ttu-id="01e94-109">OU 上のユーザーオブジェクトに対して **Grant-CsOuPermission** コマンドレットを実行すると、次の表に示すように、グループにアクセス許可が付与されます。</span><span class="sxs-lookup"><span data-stu-id="01e94-109">When you run the **Grant-CsOuPermission** cmdlet for User objects on an OU, groups are granted permissions as shown in the following table.</span></span>

### <a name="permissions-granted-for-user-objects"></a><span data-ttu-id="01e94-110">ユーザーオブジェクトに付与される権限</span><span class="sxs-lookup"><span data-stu-id="01e94-110">Permissions Granted for User Objects</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="01e94-111">グループ</span><span class="sxs-lookup"><span data-stu-id="01e94-111">Group</span></span></th>
<th><span data-ttu-id="01e94-112">権限</span><span class="sxs-lookup"><span data-stu-id="01e94-112">Permission</span></span></th>
<th><span data-ttu-id="01e94-113">適用対象</span><span class="sxs-lookup"><span data-stu-id="01e94-113">Applies to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="01e94-114">RTCHSUniversalServices</span><span class="sxs-lookup"><span data-stu-id="01e94-114">RTCHSUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="01e94-115">ディレクトリの変更の複製</span><span class="sxs-lookup"><span data-stu-id="01e94-115">Replicating directory changes</span></span></p></td>
<td><p><span data-ttu-id="01e94-116">このオブジェクトのみ</span><span class="sxs-lookup"><span data-stu-id="01e94-116">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01e94-117">RTCUniversalServerReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="01e94-117">RTCUniversalServerReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="01e94-118">リストの内容</span><span class="sxs-lookup"><span data-stu-id="01e94-118">List contents</span></span></p>
<p><span data-ttu-id="01e94-119">すべてのプロパティを読み上げる</span><span class="sxs-lookup"><span data-stu-id="01e94-119">Read all properties</span></span></p>
<p><span data-ttu-id="01e94-120">読み取りアクセス許可</span><span class="sxs-lookup"><span data-stu-id="01e94-120">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="01e94-121">このオブジェクトのみ</span><span class="sxs-lookup"><span data-stu-id="01e94-121">This object only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01e94-122">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="01e94-122">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="01e94-123">リストの内容</span><span class="sxs-lookup"><span data-stu-id="01e94-123">List contents</span></span></p>
<p><span data-ttu-id="01e94-124">すべてのプロパティを読み上げる</span><span class="sxs-lookup"><span data-stu-id="01e94-124">Read all properties</span></span></p>
<p><span data-ttu-id="01e94-125">読み取りアクセス許可</span><span class="sxs-lookup"><span data-stu-id="01e94-125">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="01e94-126">このオブジェクトのみ</span><span class="sxs-lookup"><span data-stu-id="01e94-126">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01e94-127">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="01e94-127">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="01e94-128">RTCUserSearchPropertySet を読む</span><span class="sxs-lookup"><span data-stu-id="01e94-128">Read RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="01e94-129">RTCUserProvisioningPropertySet を読む</span><span class="sxs-lookup"><span data-stu-id="01e94-129">Read RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="01e94-130">RTCPropertySet を読む</span><span class="sxs-lookup"><span data-stu-id="01e94-130">Read RTCPropertySet</span></span></p>
<p><span data-ttu-id="01e94-131">Public-Information を読む</span><span class="sxs-lookup"><span data-stu-id="01e94-131">Read Public-Information</span></span></p>
<p><span data-ttu-id="01e94-132">General-Information を読む</span><span class="sxs-lookup"><span data-stu-id="01e94-132">Read General-Information</span></span></p>
<p><span data-ttu-id="01e94-133">ユーザーアカウントの制限を読む</span><span class="sxs-lookup"><span data-stu-id="01e94-133">Read User-Account-Restrictions</span></span></p></td>
<td><p><span data-ttu-id="01e94-134">子孫のユーザーオブジェクト</span><span class="sxs-lookup"><span data-stu-id="01e94-134">Descendant User objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01e94-135">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="01e94-135">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="01e94-136">RTCUserSearchPropertySet の書き込み</span><span class="sxs-lookup"><span data-stu-id="01e94-136">Write RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="01e94-137">MsExchUCVoiceMailSettings の書き込み</span><span class="sxs-lookup"><span data-stu-id="01e94-137">Write msExchUCVoiceMailSettings</span></span></p>
<p><span data-ttu-id="01e94-138">RTCUserProvisioningPropertySet の書き込み</span><span class="sxs-lookup"><span data-stu-id="01e94-138">Write RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="01e94-139">RTCPropertySet の書き込み</span><span class="sxs-lookup"><span data-stu-id="01e94-139">Write RTCPropertySet</span></span></p>
<p><span data-ttu-id="01e94-140">ProxyAddresses の書き込み</span><span class="sxs-lookup"><span data-stu-id="01e94-140">Write proxyAddresses</span></span></p></td>
<td><p><span data-ttu-id="01e94-141">子孫のユーザーオブジェクト</span><span class="sxs-lookup"><span data-stu-id="01e94-141">Descendant User objects</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="granting-permission-for-computer-objects"></a><span data-ttu-id="01e94-142">コンピューターオブジェクトへのアクセス許可の付与</span><span class="sxs-lookup"><span data-stu-id="01e94-142">Granting Permission for Computer Objects</span></span>

<span data-ttu-id="01e94-143">OU 上のコンピューターオブジェクトに対して **Grant-CsOuPermission** コマンドレットを実行すると、次の表に示すように、グループにアクセス許可が付与されます。</span><span class="sxs-lookup"><span data-stu-id="01e94-143">When you run the **Grant-CsOuPermission** cmdlet for Computer objects on an OU, groups are granted permissions as shown in the following table.</span></span>

### <a name="permissions-granted-for-computer-objects"></a><span data-ttu-id="01e94-144">コンピューターオブジェクトに付与される権限</span><span class="sxs-lookup"><span data-stu-id="01e94-144">Permissions Granted for Computer Objects</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="01e94-145">グループ</span><span class="sxs-lookup"><span data-stu-id="01e94-145">Group</span></span></th>
<th><span data-ttu-id="01e94-146">権限</span><span class="sxs-lookup"><span data-stu-id="01e94-146">Permission</span></span></th>
<th><span data-ttu-id="01e94-147">適用対象</span><span class="sxs-lookup"><span data-stu-id="01e94-147">Applies to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="01e94-148">RTCHSUniversalServices</span><span class="sxs-lookup"><span data-stu-id="01e94-148">RTCHSUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="01e94-149">ディレクトリの変更の複製</span><span class="sxs-lookup"><span data-stu-id="01e94-149">Replicating directory changes</span></span></p></td>
<td><p><span data-ttu-id="01e94-150">このオブジェクトのみ</span><span class="sxs-lookup"><span data-stu-id="01e94-150">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01e94-151">RTCUniversalServerReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="01e94-151">RTCUniversalServerReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="01e94-152">リストの内容</span><span class="sxs-lookup"><span data-stu-id="01e94-152">List contents</span></span></p>
<p><span data-ttu-id="01e94-153">すべてのプロパティを読み上げる</span><span class="sxs-lookup"><span data-stu-id="01e94-153">Read all properties</span></span></p>
<p><span data-ttu-id="01e94-154">読み取りアクセス許可</span><span class="sxs-lookup"><span data-stu-id="01e94-154">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="01e94-155">このオブジェクトのみ</span><span class="sxs-lookup"><span data-stu-id="01e94-155">This object only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01e94-156">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="01e94-156">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="01e94-157">リストの内容</span><span class="sxs-lookup"><span data-stu-id="01e94-157">List contents</span></span></p>
<p><span data-ttu-id="01e94-158">すべてのプロパティを読み上げる</span><span class="sxs-lookup"><span data-stu-id="01e94-158">Read all properties</span></span></p>
<p><span data-ttu-id="01e94-159">読み取りアクセス許可</span><span class="sxs-lookup"><span data-stu-id="01e94-159">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="01e94-160">このオブジェクトのみ</span><span class="sxs-lookup"><span data-stu-id="01e94-160">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01e94-161">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="01e94-161">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="01e94-162">Public-Information を読む</span><span class="sxs-lookup"><span data-stu-id="01e94-162">Read Public-Information</span></span></p>
<p><span data-ttu-id="01e94-163">読み取り済みの DNS ホスト名</span><span class="sxs-lookup"><span data-stu-id="01e94-163">Read Validated-DNS-Host-Name</span></span></p></td>
<td><p><span data-ttu-id="01e94-164">子コンピューターオブジェクト</span><span class="sxs-lookup"><span data-stu-id="01e94-164">Descendant Computer objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01e94-165">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="01e94-165">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="01e94-166">Public-Information を読む</span><span class="sxs-lookup"><span data-stu-id="01e94-166">Read Public-Information</span></span></p>
<p><span data-ttu-id="01e94-167">読み取り済みの DNS ホスト名</span><span class="sxs-lookup"><span data-stu-id="01e94-167">Read Validated-DNS-Host-Name</span></span></p></td>
<td><p><span data-ttu-id="01e94-168">子コンピューターオブジェクト</span><span class="sxs-lookup"><span data-stu-id="01e94-168">Descendant Computer objects</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="granting-permission-for-contact-or-appcontact-objects"></a><span data-ttu-id="01e94-169">Contact オブジェクトまたは AppContact オブジェクトのアクセス許可を付与する</span><span class="sxs-lookup"><span data-stu-id="01e94-169">Granting Permission for Contact or AppContact Objects</span></span>

<span data-ttu-id="01e94-170">組織内の連絡先オブジェクトまたは AppContact オブジェクトに対して **Grant-CsOuPermission** コマンドレットを実行すると、次の表に示すように、グループにアクセス許可が付与されます。</span><span class="sxs-lookup"><span data-stu-id="01e94-170">When you run the **Grant-CsOuPermission** cmdlet for Contact objects or AppContact objects on an OU, groups are granted permissions as shown in the following table.</span></span>

### <a name="permissions-granted-for-contact-or-appcontact-objects"></a><span data-ttu-id="01e94-171">Contact オブジェクトまたは AppContact オブジェクトに付与されているアクセス許可</span><span class="sxs-lookup"><span data-stu-id="01e94-171">Permissions Granted for Contact or AppContact Objects</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="01e94-172">グループ</span><span class="sxs-lookup"><span data-stu-id="01e94-172">Group</span></span></th>
<th><span data-ttu-id="01e94-173">権限</span><span class="sxs-lookup"><span data-stu-id="01e94-173">Permission</span></span></th>
<th><span data-ttu-id="01e94-174">適用対象</span><span class="sxs-lookup"><span data-stu-id="01e94-174">Applies to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="01e94-175">RTCHSUniversalServices</span><span class="sxs-lookup"><span data-stu-id="01e94-175">RTCHSUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="01e94-176">ディレクトリの変更の複製</span><span class="sxs-lookup"><span data-stu-id="01e94-176">Replicating directory changes</span></span></p></td>
<td><p><span data-ttu-id="01e94-177">このオブジェクトのみ</span><span class="sxs-lookup"><span data-stu-id="01e94-177">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01e94-178">RTCUniversalServerReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="01e94-178">RTCUniversalServerReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="01e94-179">リストの内容</span><span class="sxs-lookup"><span data-stu-id="01e94-179">List contents</span></span></p>
<p><span data-ttu-id="01e94-180">すべてのプロパティを読み上げる</span><span class="sxs-lookup"><span data-stu-id="01e94-180">Read all properties</span></span></p>
<p><span data-ttu-id="01e94-181">読み取りアクセス許可</span><span class="sxs-lookup"><span data-stu-id="01e94-181">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="01e94-182">このオブジェクトのみ</span><span class="sxs-lookup"><span data-stu-id="01e94-182">This object only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01e94-183">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="01e94-183">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="01e94-184">リストの内容</span><span class="sxs-lookup"><span data-stu-id="01e94-184">List contents</span></span></p>
<p><span data-ttu-id="01e94-185">すべてのプロパティを読み上げる</span><span class="sxs-lookup"><span data-stu-id="01e94-185">Read all properties</span></span></p>
<p><span data-ttu-id="01e94-186">読み取りアクセス許可</span><span class="sxs-lookup"><span data-stu-id="01e94-186">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="01e94-187">このオブジェクトのみ</span><span class="sxs-lookup"><span data-stu-id="01e94-187">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01e94-188">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="01e94-188">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="01e94-189">RTCUserSearchPropertySet を読む</span><span class="sxs-lookup"><span data-stu-id="01e94-189">Read RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="01e94-190">RTCUserProvisioningPropertySet を読む</span><span class="sxs-lookup"><span data-stu-id="01e94-190">Read RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="01e94-191">RTCPropertySet を読む</span><span class="sxs-lookup"><span data-stu-id="01e94-191">Read RTCPropertySet</span></span></p>
<p><span data-ttu-id="01e94-192">Public-Information を読む</span><span class="sxs-lookup"><span data-stu-id="01e94-192">Read Public-Information</span></span></p>
<p><span data-ttu-id="01e94-193">General-Information を読む</span><span class="sxs-lookup"><span data-stu-id="01e94-193">Read General-Information</span></span></p>
<p><span data-ttu-id="01e94-194">Personal-Information を読む</span><span class="sxs-lookup"><span data-stu-id="01e94-194">Read Personal-Information</span></span></p>
<p><span data-ttu-id="01e94-195">ユーザーアカウントの制限を読む</span><span class="sxs-lookup"><span data-stu-id="01e94-195">Read User-Account-Restrictions</span></span></p></td>
<td><p><span data-ttu-id="01e94-196">子孫の連絡先オブジェクト</span><span class="sxs-lookup"><span data-stu-id="01e94-196">Descendant Contact objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01e94-197">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="01e94-197">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="01e94-198">RTCUserSearchPropertySet の書き込み</span><span class="sxs-lookup"><span data-stu-id="01e94-198">Write RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="01e94-199">他の Ip電話を書く</span><span class="sxs-lookup"><span data-stu-id="01e94-199">Write otherIpPhone</span></span></p>
<p><span data-ttu-id="01e94-200">DisplayName を書く</span><span class="sxs-lookup"><span data-stu-id="01e94-200">Write displayName</span></span></p>
<p><span data-ttu-id="01e94-201">説明の書き込み</span><span class="sxs-lookup"><span data-stu-id="01e94-201">Write description</span></span></p>
<p><span data-ttu-id="01e94-202">TelephoneNumber の書き込み</span><span class="sxs-lookup"><span data-stu-id="01e94-202">Write telephoneNumber</span></span></p>
<p><span data-ttu-id="01e94-203">MsExchUCVoiceMailSettings の書き込み</span><span class="sxs-lookup"><span data-stu-id="01e94-203">Write msExchUCVoiceMailSettings</span></span></p>
<p><span data-ttu-id="01e94-204">RTCUserProvisioningPropertySet の書き込み</span><span class="sxs-lookup"><span data-stu-id="01e94-204">Write RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="01e94-205">RTCPropertySet の書き込み</span><span class="sxs-lookup"><span data-stu-id="01e94-205">Write RTCPropertySet</span></span></p>
<p><span data-ttu-id="01e94-206">ProxyAddresses の書き込み</span><span class="sxs-lookup"><span data-stu-id="01e94-206">Write proxyAddresses</span></span></p></td>
<td><p><span data-ttu-id="01e94-207">子孫の連絡先オブジェクト</span><span class="sxs-lookup"><span data-stu-id="01e94-207">Descendant Contact objects</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="granting-permission-for-device-objects"></a><span data-ttu-id="01e94-208">デバイスオブジェクトのアクセス許可の付与</span><span class="sxs-lookup"><span data-stu-id="01e94-208">Granting Permission for Device Objects</span></span>

<span data-ttu-id="01e94-209">OU 上のデバイスオブジェクトに対して **Grant-CsOuPermission** コマンドレットを実行すると、次の表に示すように、グループにアクセス許可が付与されます。</span><span class="sxs-lookup"><span data-stu-id="01e94-209">When you run the **Grant-CsOuPermission** cmdlet for Device objects on an OU, groups are granted permissions as shown in the following table.</span></span>

### <a name="permissions-granted-for-device-objects"></a><span data-ttu-id="01e94-210">デバイスオブジェクトに付与されるアクセス許可</span><span class="sxs-lookup"><span data-stu-id="01e94-210">Permissions Granted for Device Objects</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="01e94-211">グループ</span><span class="sxs-lookup"><span data-stu-id="01e94-211">Group</span></span></th>
<th><span data-ttu-id="01e94-212">権限</span><span class="sxs-lookup"><span data-stu-id="01e94-212">Permission</span></span></th>
<th><span data-ttu-id="01e94-213">適用対象</span><span class="sxs-lookup"><span data-stu-id="01e94-213">Applies to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="01e94-214">RTCHSUniversalServices</span><span class="sxs-lookup"><span data-stu-id="01e94-214">RTCHSUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="01e94-215">ディレクトリの変更の複製</span><span class="sxs-lookup"><span data-stu-id="01e94-215">Replicating directory changes</span></span></p></td>
<td><p><span data-ttu-id="01e94-216">このオブジェクトのみ</span><span class="sxs-lookup"><span data-stu-id="01e94-216">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01e94-217">RTCUniversalServerReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="01e94-217">RTCUniversalServerReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="01e94-218">リストの内容</span><span class="sxs-lookup"><span data-stu-id="01e94-218">List contents</span></span></p>
<p><span data-ttu-id="01e94-219">すべてのプロパティを読み上げる</span><span class="sxs-lookup"><span data-stu-id="01e94-219">Read all properties</span></span></p>
<p><span data-ttu-id="01e94-220">読み取りアクセス許可</span><span class="sxs-lookup"><span data-stu-id="01e94-220">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="01e94-221">このオブジェクトのみ</span><span class="sxs-lookup"><span data-stu-id="01e94-221">This object only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01e94-222">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="01e94-222">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="01e94-223">リストの内容</span><span class="sxs-lookup"><span data-stu-id="01e94-223">List contents</span></span></p>
<p><span data-ttu-id="01e94-224">すべてのプロパティを読み上げる</span><span class="sxs-lookup"><span data-stu-id="01e94-224">Read all properties</span></span></p>
<p><span data-ttu-id="01e94-225">読み取りアクセス許可</span><span class="sxs-lookup"><span data-stu-id="01e94-225">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="01e94-226">このオブジェクトのみ</span><span class="sxs-lookup"><span data-stu-id="01e94-226">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01e94-227">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="01e94-227">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="01e94-228">RTCUserSearchPropertySet を読む</span><span class="sxs-lookup"><span data-stu-id="01e94-228">Read RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="01e94-229">RTCUserProvisioningPropertySet を読む</span><span class="sxs-lookup"><span data-stu-id="01e94-229">Read RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="01e94-230">RTCPropertySet を読む</span><span class="sxs-lookup"><span data-stu-id="01e94-230">Read RTCPropertySet</span></span></p>
<p><span data-ttu-id="01e94-231">Public-Information を読む</span><span class="sxs-lookup"><span data-stu-id="01e94-231">Read Public-Information</span></span></p>
<p><span data-ttu-id="01e94-232">Personal-Information を読む</span><span class="sxs-lookup"><span data-stu-id="01e94-232">Read Personal-Information</span></span></p>
<p><span data-ttu-id="01e94-233">General-Information を読む</span><span class="sxs-lookup"><span data-stu-id="01e94-233">Read General-Information</span></span></p>
<p><span data-ttu-id="01e94-234">ユーザーアカウントの制限を読む</span><span class="sxs-lookup"><span data-stu-id="01e94-234">Read User-Account-Restrictions</span></span></p></td>
<td><p><span data-ttu-id="01e94-235">子孫の連絡先オブジェクト</span><span class="sxs-lookup"><span data-stu-id="01e94-235">Descendant Contact objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01e94-236">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="01e94-236">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="01e94-237">子の作成</span><span class="sxs-lookup"><span data-stu-id="01e94-237">Create child</span></span></p>
<p><span data-ttu-id="01e94-238">子の削除</span><span class="sxs-lookup"><span data-stu-id="01e94-238">Delete child</span></span></p>
<p><span data-ttu-id="01e94-239">ツリーの削除</span><span class="sxs-lookup"><span data-stu-id="01e94-239">Delete tree</span></span></p></td>
<td><p><span data-ttu-id="01e94-240">問い合わせ</span><span class="sxs-lookup"><span data-stu-id="01e94-240">Contact</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01e94-241">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="01e94-241">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="01e94-242">DisplayName を書く</span><span class="sxs-lookup"><span data-stu-id="01e94-242">Write displayName</span></span></p>
<p><span data-ttu-id="01e94-243">説明の書き込み</span><span class="sxs-lookup"><span data-stu-id="01e94-243">Write description</span></span></p>
<p><span data-ttu-id="01e94-244">TelephoneNumber の書き込み</span><span class="sxs-lookup"><span data-stu-id="01e94-244">Write telephoneNumber</span></span></p></td>
<td><p><span data-ttu-id="01e94-245">子孫のユーザーオブジェクト</span><span class="sxs-lookup"><span data-stu-id="01e94-245">Descendant User objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01e94-246">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="01e94-246">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="01e94-247">RTCUserSearchPropertySet の書き込み</span><span class="sxs-lookup"><span data-stu-id="01e94-247">Write RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="01e94-248">他の Ip電話を書く</span><span class="sxs-lookup"><span data-stu-id="01e94-248">Write otherIpPhone</span></span></p>
<p><span data-ttu-id="01e94-249">DisplayName を書く</span><span class="sxs-lookup"><span data-stu-id="01e94-249">Write displayName</span></span></p>
<p><span data-ttu-id="01e94-250">説明の書き込み</span><span class="sxs-lookup"><span data-stu-id="01e94-250">Write description</span></span></p>
<p><span data-ttu-id="01e94-251">TelephoneNumber の書き込み</span><span class="sxs-lookup"><span data-stu-id="01e94-251">Write telephoneNumber</span></span></p>
<p><span data-ttu-id="01e94-252">MsExchUCVoiceMailSettings の書き込み</span><span class="sxs-lookup"><span data-stu-id="01e94-252">Write msExchUCVoiceMailSettings</span></span></p>
<p><span data-ttu-id="01e94-253">RTCUserProvisioningPropertySet の書き込み</span><span class="sxs-lookup"><span data-stu-id="01e94-253">Write RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="01e94-254">RTCPropertySet の書き込み</span><span class="sxs-lookup"><span data-stu-id="01e94-254">Write RTCPropertySet</span></span></p>
<p><span data-ttu-id="01e94-255">ProxyAddresses の書き込み</span><span class="sxs-lookup"><span data-stu-id="01e94-255">Write proxyAddresses</span></span></p></td>
<td><p><span data-ttu-id="01e94-256">子孫の連絡先オブジェクト</span><span class="sxs-lookup"><span data-stu-id="01e94-256">Descendant Contact objects</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="granting-permission-for-inetorgperson-objects"></a><span data-ttu-id="01e94-257">InetOrgPerson オブジェクトのアクセス許可を付与する</span><span class="sxs-lookup"><span data-stu-id="01e94-257">Granting Permission for InetOrgPerson Objects</span></span>

<span data-ttu-id="01e94-258">OU 上の InetOrgPerson オブジェクトに対して **Grant-CsOuPermission** コマンドレットを実行すると、次の表に示すように、グループにアクセス許可が付与されます。</span><span class="sxs-lookup"><span data-stu-id="01e94-258">When you run the **Grant-CsOuPermission** cmdlet for InetOrgPerson objects on an OU, groups are granted permissions as shown in the following table.</span></span>

### <a name="permissions-granted-for-inetorgperson-objects"></a><span data-ttu-id="01e94-259">InetOrgPerson オブジェクトに対して付与されるアクセス許可</span><span class="sxs-lookup"><span data-stu-id="01e94-259">Permissions Granted for InetOrgPerson Objects</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="01e94-260">グループ</span><span class="sxs-lookup"><span data-stu-id="01e94-260">Group</span></span></th>
<th><span data-ttu-id="01e94-261">権限</span><span class="sxs-lookup"><span data-stu-id="01e94-261">Permission</span></span></th>
<th><span data-ttu-id="01e94-262">適用対象</span><span class="sxs-lookup"><span data-stu-id="01e94-262">Applies to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="01e94-263">RTCHSUniversalServices</span><span class="sxs-lookup"><span data-stu-id="01e94-263">RTCHSUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="01e94-264">ディレクトリの変更の複製</span><span class="sxs-lookup"><span data-stu-id="01e94-264">Replicating directory changes</span></span></p></td>
<td><p><span data-ttu-id="01e94-265">このオブジェクトのみ</span><span class="sxs-lookup"><span data-stu-id="01e94-265">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01e94-266">RTCUniversalServerReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="01e94-266">RTCUniversalServerReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="01e94-267">リストの内容</span><span class="sxs-lookup"><span data-stu-id="01e94-267">List contents</span></span></p>
<p><span data-ttu-id="01e94-268">すべてのプロパティを読み上げる</span><span class="sxs-lookup"><span data-stu-id="01e94-268">Read all properties</span></span></p>
<p><span data-ttu-id="01e94-269">読み取りアクセス許可</span><span class="sxs-lookup"><span data-stu-id="01e94-269">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="01e94-270">このオブジェクトのみ</span><span class="sxs-lookup"><span data-stu-id="01e94-270">This object only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01e94-271">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="01e94-271">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="01e94-272">リストの内容</span><span class="sxs-lookup"><span data-stu-id="01e94-272">List contents</span></span></p>
<p><span data-ttu-id="01e94-273">すべてのプロパティを読み上げる</span><span class="sxs-lookup"><span data-stu-id="01e94-273">Read all properties</span></span></p>
<p><span data-ttu-id="01e94-274">読み取りアクセス許可</span><span class="sxs-lookup"><span data-stu-id="01e94-274">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="01e94-275">このオブジェクトのみ</span><span class="sxs-lookup"><span data-stu-id="01e94-275">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01e94-276">RTCUniversalUserReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="01e94-276">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="01e94-277">RTCUserSearchPropertySet を読む</span><span class="sxs-lookup"><span data-stu-id="01e94-277">Read RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="01e94-278">RTCUserProvisioningPropertySet を読む</span><span class="sxs-lookup"><span data-stu-id="01e94-278">Read RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="01e94-279">RTCPropertySet を読む</span><span class="sxs-lookup"><span data-stu-id="01e94-279">Read RTCPropertySet</span></span></p>
<p><span data-ttu-id="01e94-280">Personal-Information を読む</span><span class="sxs-lookup"><span data-stu-id="01e94-280">Read Personal-Information</span></span></p>
<p><span data-ttu-id="01e94-281">Public-Information を読む</span><span class="sxs-lookup"><span data-stu-id="01e94-281">Read Public-Information</span></span></p>
<p><span data-ttu-id="01e94-282">General-Information を読む</span><span class="sxs-lookup"><span data-stu-id="01e94-282">Read General-Information</span></span></p>
<p><span data-ttu-id="01e94-283">ユーザーアカウントの制限を読む</span><span class="sxs-lookup"><span data-stu-id="01e94-283">Read User-Account-Restrictions</span></span></p></td>
<td><p><span data-ttu-id="01e94-284">子の inetOrgPerson オブジェクト</span><span class="sxs-lookup"><span data-stu-id="01e94-284">Descendant inetOrgPerson objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01e94-285">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="01e94-285">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="01e94-286">RTCUserSearchPropertySet の書き込み</span><span class="sxs-lookup"><span data-stu-id="01e94-286">Write RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="01e94-287">RTCUserProvisioningPropertySet の書き込み</span><span class="sxs-lookup"><span data-stu-id="01e94-287">Write RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="01e94-288">RTCPropertySet の書き込み</span><span class="sxs-lookup"><span data-stu-id="01e94-288">Write RTCPropertySet</span></span></p>
<p><span data-ttu-id="01e94-289">ProxyAddresses の書き込み</span><span class="sxs-lookup"><span data-stu-id="01e94-289">Write proxyAddresses</span></span></p></td>
<td><p><span data-ttu-id="01e94-290">子の inetOrgPerson オブジェクト</span><span class="sxs-lookup"><span data-stu-id="01e94-290">Descendant inetOrgPerson objects</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="01e94-291">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="01e94-291">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

