---
title: 'Lync Server 2013: Registration テーブル'
description: 'Lync Server 2013: 登録テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Registration table
ms:assetid: 05ff9dd3-1aaa-4af0-bd69-8789fb8eaeb3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398114(v=OCS.15)
ms:contentKeyID: 48183298
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 806e1a4e944c9bc04ebdd167c41c80a57fde3f29
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436567"
---
# <a name="registration-table-in-lync-server-2013"></a><span data-ttu-id="65dc9-103">Lync Server 2013 の Registration テーブル</span><span class="sxs-lookup"><span data-stu-id="65dc9-103">Registration table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="65dc9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="65dc9-104">

<span> </span></span></span>

<span data-ttu-id="65dc9-105">_**最終更新日:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="65dc9-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="65dc9-106">各レコードは、1つのユーザー登録イベントを表します。</span><span class="sxs-lookup"><span data-stu-id="65dc9-106">Each record represents one user registration event.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="65dc9-107">列</span><span class="sxs-lookup"><span data-stu-id="65dc9-107">Column</span></span></th>
<th><span data-ttu-id="65dc9-108">データ型</span><span class="sxs-lookup"><span data-stu-id="65dc9-108">Data Type</span></span></th>
<th><span data-ttu-id="65dc9-109">キー/インデックス</span><span class="sxs-lookup"><span data-stu-id="65dc9-109">Key/Index</span></span></th>
<th><span data-ttu-id="65dc9-110">詳細</span><span class="sxs-lookup"><span data-stu-id="65dc9-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="65dc9-111"><strong>セッション Id</strong></span><span class="sxs-lookup"><span data-stu-id="65dc9-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="65dc9-112">datetime</span><span class="sxs-lookup"><span data-stu-id="65dc9-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="65dc9-113">プライマリ、外部</span><span class="sxs-lookup"><span data-stu-id="65dc9-113">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="65dc9-114">セッション要求の時刻。</span><span class="sxs-lookup"><span data-stu-id="65dc9-114">Time of session request.</span></span> <span data-ttu-id="65dc9-115">セッションを一意に識別するために <strong>Sessionidseq</strong> と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="65dc9-115">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="65dc9-116">詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="65dc9-116">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65dc9-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="65dc9-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="65dc9-118">int</span><span class="sxs-lookup"><span data-stu-id="65dc9-118">int</span></span></p></td>
<td><p><span data-ttu-id="65dc9-119">プライマリ、外部</span><span class="sxs-lookup"><span data-stu-id="65dc9-119">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="65dc9-120">セッションを識別する ID 番号。</span><span class="sxs-lookup"><span data-stu-id="65dc9-120">ID number to identify the session.</span></span> <span data-ttu-id="65dc9-121">セッションを一意に識別するために <strong>Sessionidtime</strong> と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="65dc9-121">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="65dc9-122">詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="65dc9-122">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65dc9-123"><strong>UserId</strong></span><span class="sxs-lookup"><span data-stu-id="65dc9-123"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="65dc9-124">int</span><span class="sxs-lookup"><span data-stu-id="65dc9-124">int</span></span></p></td>
<td><p><span data-ttu-id="65dc9-125">外部</span><span class="sxs-lookup"><span data-stu-id="65dc9-125">Foreign</span></span></p></td>
<td><p><span data-ttu-id="65dc9-126">ユーザー ID。</span><span class="sxs-lookup"><span data-stu-id="65dc9-126">The user ID.</span></span> <span data-ttu-id="65dc9-127">詳細については、「 <a href="lync-server-2013-users-table.md">Lync Server 2013 のユーザーテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="65dc9-127">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65dc9-128"><strong>EndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="65dc9-128"><strong>EndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="65dc9-129">長さ</span><span class="sxs-lookup"><span data-stu-id="65dc9-129">uniqueidentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65dc9-130">登録エンドポイントを識別する GUID。</span><span class="sxs-lookup"><span data-stu-id="65dc9-130">A GUID to identify a registration endpoint.</span></span> <span data-ttu-id="65dc9-131">通常、同じユーザーの同じコンピューターの register イベントには、同じエンドポイント ID があります。</span><span class="sxs-lookup"><span data-stu-id="65dc9-131">Usually the register event from the same computer of the same user will have the same endpoint ID.</span></span> <span data-ttu-id="65dc9-132">各コンピューターには、別のエンドポイント ID があります。</span><span class="sxs-lookup"><span data-stu-id="65dc9-132">Different machines have a different endpoint ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65dc9-133"><strong>Endポインタ a</strong></span><span class="sxs-lookup"><span data-stu-id="65dc9-133"><strong>EndpointEra</strong></span></span></p></td>
<td><p><span data-ttu-id="65dc9-134">長さ</span><span class="sxs-lookup"><span data-stu-id="65dc9-134">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65dc9-135">同じユーザーと同じエンドポイントを含む登録を区別するために使用される ID です。</span><span class="sxs-lookup"><span data-stu-id="65dc9-135">ID used to differentiate registrations that involve the same user and the same endpoint.</span></span></p>
<p><span data-ttu-id="65dc9-136">このフィールドは、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="65dc9-136">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65dc9-137"><strong>ClientVersionId</strong></span><span class="sxs-lookup"><span data-stu-id="65dc9-137"><strong>ClientVersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="65dc9-138">int</span><span class="sxs-lookup"><span data-stu-id="65dc9-138">int</span></span></p></td>
<td><p><span data-ttu-id="65dc9-139">外部</span><span class="sxs-lookup"><span data-stu-id="65dc9-139">Foreign</span></span></p></td>
<td><p><span data-ttu-id="65dc9-140">現在のユーザーのクライアントバージョン。</span><span class="sxs-lookup"><span data-stu-id="65dc9-140">Client version of current user.</span></span> <span data-ttu-id="65dc9-141">詳細については、「 <a href="lync-server-2013-clientversions-table.md">Lync Server 2013 の Clientversions の表</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="65dc9-141">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65dc9-142"><strong>RegistrarId</strong></span><span class="sxs-lookup"><span data-stu-id="65dc9-142"><strong>RegistrarId</strong></span></span></p></td>
<td><p><span data-ttu-id="65dc9-143">int</span><span class="sxs-lookup"><span data-stu-id="65dc9-143">int</span></span></p></td>
<td><p><span data-ttu-id="65dc9-144">外部</span><span class="sxs-lookup"><span data-stu-id="65dc9-144">Foreign</span></span></p></td>
<td><p><span data-ttu-id="65dc9-145">登録に使用されるレジストラーサーバーの ID です。</span><span class="sxs-lookup"><span data-stu-id="65dc9-145">ID of the Registrar Server used for registration.</span></span> <span data-ttu-id="65dc9-146">詳細については、「 <a href="lync-server-2013-servers-table.md">Lync Server 2013 のサーバーの表</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="65dc9-146">See the <a href="lync-server-2013-servers-table.md">Servers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65dc9-147"><strong>PoolId</strong></span><span class="sxs-lookup"><span data-stu-id="65dc9-147"><strong>PoolId</strong></span></span></p></td>
<td><p><span data-ttu-id="65dc9-148">int</span><span class="sxs-lookup"><span data-stu-id="65dc9-148">int</span></span></p></td>
<td><p><span data-ttu-id="65dc9-149">外部</span><span class="sxs-lookup"><span data-stu-id="65dc9-149">Foreign</span></span></p></td>
<td><p><span data-ttu-id="65dc9-150">セッションがキャプチャされたプールの ID です。</span><span class="sxs-lookup"><span data-stu-id="65dc9-150">ID of the pool in which the session was captured.</span></span> <span data-ttu-id="65dc9-151">詳細については、「 <a href="lync-server-2013-pools-table.md">Lync Server 2013 のプールテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="65dc9-151">See the <a href="lync-server-2013-pools-table.md">Pools table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65dc9-152"><strong>EdgeServerId</strong></span><span class="sxs-lookup"><span data-stu-id="65dc9-152"><strong>EdgeServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="65dc9-153">int</span><span class="sxs-lookup"><span data-stu-id="65dc9-153">int</span></span></p></td>
<td><p><span data-ttu-id="65dc9-154">外部</span><span class="sxs-lookup"><span data-stu-id="65dc9-154">Foreign</span></span></p></td>
<td><p><span data-ttu-id="65dc9-155">エッジサーバーの登録が進行中です。</span><span class="sxs-lookup"><span data-stu-id="65dc9-155">Edge Server the registration is going through.</span></span> <span data-ttu-id="65dc9-156">詳細については、「 <a href="lync-server-2013-edgeservers-table.md">Lync Server 2013 の EdgeServers テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="65dc9-156">See the <a href="lync-server-2013-edgeservers-table.md">EdgeServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65dc9-157"><strong>IsInternal</strong></span><span class="sxs-lookup"><span data-stu-id="65dc9-157"><strong>IsInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="65dc9-158">わずか</span><span class="sxs-lookup"><span data-stu-id="65dc9-158">Bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65dc9-159">ユーザーが内部からログオンしているかどうか。</span><span class="sxs-lookup"><span data-stu-id="65dc9-159">Whether the user is logged on from internal or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65dc9-160"><strong>IsUserServiceAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="65dc9-160"><strong>IsUserServiceAvailable</strong></span></span></p></td>
<td><p><span data-ttu-id="65dc9-161">bit</span><span class="sxs-lookup"><span data-stu-id="65dc9-161">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65dc9-162">UserService が利用できるかどうか。</span><span class="sxs-lookup"><span data-stu-id="65dc9-162">Whether the UserService is available or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65dc9-163"><strong>IsPrimaryRegistrar</strong></span><span class="sxs-lookup"><span data-stu-id="65dc9-163"><strong>IsPrimaryRegistrar</strong></span></span></p></td>
<td><p><span data-ttu-id="65dc9-164">bit</span><span class="sxs-lookup"><span data-stu-id="65dc9-164">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65dc9-165">プライマリレジストラーに登録するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="65dc9-165">Whether register to the primary Registrar or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65dc9-166"><strong>IsPrimaryRegistrarCentral</strong></span><span class="sxs-lookup"><span data-stu-id="65dc9-166"><strong>IsPrimaryRegistrarCentral</strong></span></span></p></td>
<td><p><span data-ttu-id="65dc9-167">bit</span><span class="sxs-lookup"><span data-stu-id="65dc9-167">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65dc9-168">ユーザーが survivable branch アプライアンスに登録されているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="65dc9-168">Indicates whether or not the user is registered with a survivable branch appliance.</span></span></p>
<p><span data-ttu-id="65dc9-169">このフィールドは、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="65dc9-169">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65dc9-170"><strong>RegisterTime</strong></span><span class="sxs-lookup"><span data-stu-id="65dc9-170"><strong>RegisterTime</strong></span></span></p></td>
<td><p><span data-ttu-id="65dc9-171">datetime</span><span class="sxs-lookup"><span data-stu-id="65dc9-171">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65dc9-172">登録時間。</span><span class="sxs-lookup"><span data-stu-id="65dc9-172">Registration time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65dc9-173"><strong>DeRegisterTime</strong></span><span class="sxs-lookup"><span data-stu-id="65dc9-173"><strong>DeRegisterTime</strong></span></span></p></td>
<td><p><span data-ttu-id="65dc9-174">datetime</span><span class="sxs-lookup"><span data-stu-id="65dc9-174">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65dc9-175">De-Registration 時間。</span><span class="sxs-lookup"><span data-stu-id="65dc9-175">De-Registration time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65dc9-176"><strong>返信</strong></span><span class="sxs-lookup"><span data-stu-id="65dc9-176"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="65dc9-177">int</span><span class="sxs-lookup"><span data-stu-id="65dc9-177">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65dc9-178">Register 要求の応答コード。</span><span class="sxs-lookup"><span data-stu-id="65dc9-178">Response code of the register request.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65dc9-179"><strong>DiagnosticId</strong></span><span class="sxs-lookup"><span data-stu-id="65dc9-179"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="65dc9-180">int</span><span class="sxs-lookup"><span data-stu-id="65dc9-180">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65dc9-181">Register 要求の診断 ID。</span><span class="sxs-lookup"><span data-stu-id="65dc9-181">Diagnostic ID of the register request.</span></span> <span data-ttu-id="65dc9-182">これにより、診断情報の種類が示されます。</span><span class="sxs-lookup"><span data-stu-id="65dc9-182">This indicates that diagnostic information type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65dc9-183"><strong>DeviceId</strong></span><span class="sxs-lookup"><span data-stu-id="65dc9-183"><strong>DeviceId</strong></span></span></p></td>
<td><p><span data-ttu-id="65dc9-184">int</span><span class="sxs-lookup"><span data-stu-id="65dc9-184">int</span></span></p></td>
<td><p><span data-ttu-id="65dc9-185">外部</span><span class="sxs-lookup"><span data-stu-id="65dc9-185">Foreign</span></span></p></td>
<td><p><span data-ttu-id="65dc9-186">Register 要求の取得元のデバイス。</span><span class="sxs-lookup"><span data-stu-id="65dc9-186">The device that the register request is coming from.</span></span> <span data-ttu-id="65dc9-187">詳細については、「 <a href="lync-server-2013-devices-table.md">Lync Server 2013 のデバイスの表</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="65dc9-187">See the <a href="lync-server-2013-devices-table.md">Devices table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65dc9-188"><strong>DeRegisterTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="65dc9-188"><strong>DeRegisterTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="65dc9-189">tinyint</span><span class="sxs-lookup"><span data-stu-id="65dc9-189">tinyint</span></span></p></td>
<td><p><span data-ttu-id="65dc9-190">外部</span><span class="sxs-lookup"><span data-stu-id="65dc9-190">Foreign</span></span></p></td>
<td><p><span data-ttu-id="65dc9-191">"ユーザーが開始しました"、"登録の期限切れ"、"クライアントが失敗しました" などの de レジスタの理由。</span><span class="sxs-lookup"><span data-stu-id="65dc9-191">The reason of de-register, such as ‘user initiated’, ‘registration expired’, ‘client fail’, and more.</span></span> <span data-ttu-id="65dc9-192">詳細については、「 <a href="lync-server-2013-deregistertype-table.md">Lync Server 2013 の DeRegisterType テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="65dc9-192">See the <a href="lync-server-2013-deregistertype-table.md">DeRegisterType table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65dc9-193"><strong>IPAddress</strong></span><span class="sxs-lookup"><span data-stu-id="65dc9-193"><strong>IPAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="65dc9-194">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="65dc9-194">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="65dc9-195">ユーザーが登録したエンドポイントの IP アドレス。</span><span class="sxs-lookup"><span data-stu-id="65dc9-195">IP address of the endpoint the user registered with.</span></span> <span data-ttu-id="65dc9-196">これは IPv4 アドレスまたは IPv6 アドレスにすることができます。</span><span class="sxs-lookup"><span data-stu-id="65dc9-196">This can be an IPv4 address or an IPv6 address.</span></span></p>
<p><span data-ttu-id="65dc9-197">このフィールドは、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="65dc9-197">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="65dc9-198">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="65dc9-198">


</div>

<span> </span>

</div>

</div>

</span></span></div>

