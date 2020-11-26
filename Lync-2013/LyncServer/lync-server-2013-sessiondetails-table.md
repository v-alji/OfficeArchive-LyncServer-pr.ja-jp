---
title: 'Lync Server 2013: SessionDetails テーブル'
description: 'Lync Server 2013: SessionDetails の表。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: SessionDetails table
ms:assetid: 783d2508-e31f-4b54-be0c-63aa5ec21c04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398589(v=OCS.15)
ms:contentKeyID: 48184559
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fd927f784fb0f2a835c896824105fe8bb112c7a1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444778"
---
# <a name="sessiondetails-table-in-lync-server-2013"></a><span data-ttu-id="02ddc-103">Lync Server 2013 の SessionDetails テーブル</span><span class="sxs-lookup"><span data-stu-id="02ddc-103">SessionDetails table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="02ddc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="02ddc-104">

<span> </span></span></span>

<span data-ttu-id="02ddc-105">_**最終更新日:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="02ddc-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="02ddc-106">各レコードは、1つのピアツーピアセッションを表します。これは、VoIP-VoIP の電話、2パーティの IM セッション、または他の種類のセッションである可能性があります。</span><span class="sxs-lookup"><span data-stu-id="02ddc-106">Each record represents one peer-to-peer session, which could be a VoIP-VoIP phone call, two-party IM session, or other type of session.</span></span> <span data-ttu-id="02ddc-107">[Lync Server 2013 でメディアテーブル](lync-server-2013-media-table.md)を使用してテーブルを結合して、このセッションに関連する各メディアの詳細を見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="02ddc-107">You can perform a table join with the [Media table in Lync Server 2013](lync-server-2013-media-table.md) to find the details of each media involved in this session.</span></span>

<span data-ttu-id="02ddc-108">IsUser1IntegratedWithDeskPhone と IsUser2IntegratedWithDeskPhone フィールドが、Microsoft Lync Server 2013 で使用されている SessionDetails テーブルから削除されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="02ddc-108">Note that the IsUser1IntegratedWithDeskPhone and the IsUser2IntegratedWithDeskPhone fields have been dropped from the SessionDetails table used in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="02ddc-109">列</span><span class="sxs-lookup"><span data-stu-id="02ddc-109">Column</span></span></th>
<th><span data-ttu-id="02ddc-110">データ型</span><span class="sxs-lookup"><span data-stu-id="02ddc-110">Data Type</span></span></th>
<th><span data-ttu-id="02ddc-111">キー/インデックス</span><span class="sxs-lookup"><span data-stu-id="02ddc-111">Key/Index</span></span></th>
<th><span data-ttu-id="02ddc-112">詳細</span><span class="sxs-lookup"><span data-stu-id="02ddc-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="02ddc-113"><strong>セッション Id</strong></span><span class="sxs-lookup"><span data-stu-id="02ddc-113"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="02ddc-114">datetime</span><span class="sxs-lookup"><span data-stu-id="02ddc-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="02ddc-115">プライマリ、外部</span><span class="sxs-lookup"><span data-stu-id="02ddc-115">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="02ddc-116">セッション要求の時刻。</span><span class="sxs-lookup"><span data-stu-id="02ddc-116">Time of session request.</span></span> <span data-ttu-id="02ddc-117">セッションを一意に識別するために <strong>Sessionidseq</strong> と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="02ddc-117">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="02ddc-118">詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02ddc-118">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02ddc-119"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="02ddc-119"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="02ddc-120">int</span><span class="sxs-lookup"><span data-stu-id="02ddc-120">int</span></span></p></td>
<td><p><span data-ttu-id="02ddc-121">プライマリ、外部</span><span class="sxs-lookup"><span data-stu-id="02ddc-121">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="02ddc-122">セッションを識別する ID 番号。</span><span class="sxs-lookup"><span data-stu-id="02ddc-122">ID number to identify the session.</span></span> <span data-ttu-id="02ddc-123">セッションを一意に識別するために <strong>Sessionidtime</strong> と組み合わせて使用されます。 \* 詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02ddc-123">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.\* See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02ddc-124"><strong>CorrelationId</strong></span><span class="sxs-lookup"><span data-stu-id="02ddc-124"><strong>CorrelationId</strong></span></span></p></td>
<td><p><span data-ttu-id="02ddc-125">長さ</span><span class="sxs-lookup"><span data-stu-id="02ddc-125">uniqueidentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="02ddc-126">複数のセッションを関連付けるための GUID。</span><span class="sxs-lookup"><span data-stu-id="02ddc-126">A GUID to correlate multiple sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02ddc-127"><strong>Edialogidtime の置き換え</strong></span><span class="sxs-lookup"><span data-stu-id="02ddc-127"><strong>ReplaceDialogIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="02ddc-128">datetime</span><span class="sxs-lookup"><span data-stu-id="02ddc-128">datetime</span></span></p></td>
<td><p><span data-ttu-id="02ddc-129">外部</span><span class="sxs-lookup"><span data-stu-id="02ddc-129">Foreign</span></span></p></td>
<td><p><span data-ttu-id="02ddc-130">現在のセッションによって置き換えられたダイアログを識別する ID 番号。</span><span class="sxs-lookup"><span data-stu-id="02ddc-130">ID number to identify the dialog which was replaced by current session.</span></span> <span data-ttu-id="02ddc-131">詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02ddc-131">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02ddc-132"><strong>Edialogidseq の置き換え</strong></span><span class="sxs-lookup"><span data-stu-id="02ddc-132"><strong>ReplaceDialogIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="02ddc-133">int</span><span class="sxs-lookup"><span data-stu-id="02ddc-133">int</span></span></p></td>
<td><p><span data-ttu-id="02ddc-134">外部</span><span class="sxs-lookup"><span data-stu-id="02ddc-134">Foreign</span></span></p></td>
<td><p><span data-ttu-id="02ddc-135">セッションを識別する ID 番号。</span><span class="sxs-lookup"><span data-stu-id="02ddc-135">ID number to identify the session.</span></span> <span data-ttu-id="02ddc-136">このセッションによって置き換えられるセッションを一意に識別するために、 <strong>代替の操作と組み合わせ</strong> て使います。</span><span class="sxs-lookup"><span data-stu-id="02ddc-136">Used in conjunction with <strong>ReplacesDialogIdTime</strong> to uniquely identify a session that is replaced by this session.</span></span> <span data-ttu-id="02ddc-137">詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02ddc-137">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02ddc-138"><strong>User1Id</strong></span><span class="sxs-lookup"><span data-stu-id="02ddc-138"><strong>User1Id</strong></span></span></p></td>
<td><p><span data-ttu-id="02ddc-139">int</span><span class="sxs-lookup"><span data-stu-id="02ddc-139">int</span></span></p></td>
<td><p><span data-ttu-id="02ddc-140">外部</span><span class="sxs-lookup"><span data-stu-id="02ddc-140">Foreign</span></span></p></td>
<td><p><span data-ttu-id="02ddc-141">セッションの1人のユーザーの ID です。</span><span class="sxs-lookup"><span data-stu-id="02ddc-141">ID of one user in the session.</span></span> <span data-ttu-id="02ddc-142">詳細については、「 <a href="lync-server-2013-users-table.md">Lync Server 2013 のユーザーテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02ddc-142">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02ddc-143"><strong>User2Id</strong></span><span class="sxs-lookup"><span data-stu-id="02ddc-143"><strong>User2Id</strong></span></span></p></td>
<td><p><span data-ttu-id="02ddc-144">int</span><span class="sxs-lookup"><span data-stu-id="02ddc-144">int</span></span></p></td>
<td><p><span data-ttu-id="02ddc-145">外部</span><span class="sxs-lookup"><span data-stu-id="02ddc-145">Foreign</span></span></p></td>
<td><p><span data-ttu-id="02ddc-146">セッション内の他のユーザーの ID です。</span><span class="sxs-lookup"><span data-stu-id="02ddc-146">ID of the other user in the session.</span></span> <span data-ttu-id="02ddc-147">詳細については、「 <a href="lync-server-2013-users-table.md">Lync Server 2013 のユーザーテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02ddc-147">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02ddc-148"><strong>User1EndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="02ddc-148"><strong>User1EndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="02ddc-149">長さ</span><span class="sxs-lookup"><span data-stu-id="02ddc-149">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="02ddc-150">セッションの最初のユーザーによって使用されるエンドポイントを示す GUID。</span><span class="sxs-lookup"><span data-stu-id="02ddc-150">GUID that identifies the endpoint used by the first user in the session.</span></span></p>
<p><span data-ttu-id="02ddc-151">このフィールドは、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="02ddc-151">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02ddc-152"><strong>User2EndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="02ddc-152"><strong>User2EndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="02ddc-153">長さ</span><span class="sxs-lookup"><span data-stu-id="02ddc-153">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="02ddc-154">セッション内の2番目のユーザーによって使用されるエンドポイントを識別する GUID。</span><span class="sxs-lookup"><span data-stu-id="02ddc-154">GUID that identifies the endpoint used by the second user in the session.</span></span></p>
<p><span data-ttu-id="02ddc-155">このフィールドは、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="02ddc-155">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02ddc-156"><strong>TargetUserId</strong></span><span class="sxs-lookup"><span data-stu-id="02ddc-156"><strong>TargetUserId</strong></span></span></p></td>
<td><p><span data-ttu-id="02ddc-157">int</span><span class="sxs-lookup"><span data-stu-id="02ddc-157">int</span></span></p></td>
<td><p><span data-ttu-id="02ddc-158">外部</span><span class="sxs-lookup"><span data-stu-id="02ddc-158">Foreign</span></span></p></td>
<td><p><span data-ttu-id="02ddc-159">SIP 要求の元の To ユーザーの URI。</span><span class="sxs-lookup"><span data-stu-id="02ddc-159">The original To user URI in the SIP request.</span></span> <span data-ttu-id="02ddc-160">詳細については、「 <a href="lync-server-2013-users-table.md">Lync Server 2013 のユーザーテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02ddc-160">see the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02ddc-161"><strong>SessionStartedById</strong></span><span class="sxs-lookup"><span data-stu-id="02ddc-161"><strong>SessionStartedById</strong></span></span></p></td>
<td><p><span data-ttu-id="02ddc-162">int</span><span class="sxs-lookup"><span data-stu-id="02ddc-162">int</span></span></p></td>
<td><p><span data-ttu-id="02ddc-163">外部</span><span class="sxs-lookup"><span data-stu-id="02ddc-163">Foreign</span></span></p></td>
<td><p><span data-ttu-id="02ddc-164">セッションを開始したユーザーの ID です。</span><span class="sxs-lookup"><span data-stu-id="02ddc-164">ID of the user who started the session.</span></span> <span data-ttu-id="02ddc-165">詳細については、「 <a href="lync-server-2013-users-table.md">Lync Server 2013 のユーザーテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02ddc-165">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02ddc-166"><strong>OnBehalfOfId</strong></span><span class="sxs-lookup"><span data-stu-id="02ddc-166"><strong>OnBehalfOfId</strong></span></span></p></td>
<td><p><span data-ttu-id="02ddc-167">int</span><span class="sxs-lookup"><span data-stu-id="02ddc-167">int</span></span></p></td>
<td><p><span data-ttu-id="02ddc-168">外部</span><span class="sxs-lookup"><span data-stu-id="02ddc-168">Foreign</span></span></p></td>
<td><p><span data-ttu-id="02ddc-169">発信者が代理としているユーザーの ID を示します。</span><span class="sxs-lookup"><span data-stu-id="02ddc-169">Indicates the ID of the user of who the caller is on behalf.</span></span> <span data-ttu-id="02ddc-170">詳細については、「 <a href="lync-server-2013-users-table.md">Lync Server 2013 のユーザーテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02ddc-170">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02ddc-171"><strong>ReferredById</strong></span><span class="sxs-lookup"><span data-stu-id="02ddc-171"><strong>ReferredById</strong></span></span></p></td>
<td><p><span data-ttu-id="02ddc-172">int</span><span class="sxs-lookup"><span data-stu-id="02ddc-172">int</span></span></p></td>
<td><p><span data-ttu-id="02ddc-173">外部</span><span class="sxs-lookup"><span data-stu-id="02ddc-173">Foreign</span></span></p></td>
<td><p><span data-ttu-id="02ddc-174">通話を参照するユーザーの ID です。</span><span class="sxs-lookup"><span data-stu-id="02ddc-174">ID of the user by who the call is referred.</span></span> <span data-ttu-id="02ddc-175">詳細については、「 <a href="lync-server-2013-users-table.md">Lync Server 2013 のユーザーテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02ddc-175">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02ddc-176"><strong>ServerId</strong></span><span class="sxs-lookup"><span data-stu-id="02ddc-176"><strong>ServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="02ddc-177">int</span><span class="sxs-lookup"><span data-stu-id="02ddc-177">int</span></span></p></td>
<td><p><span data-ttu-id="02ddc-178">外部</span><span class="sxs-lookup"><span data-stu-id="02ddc-178">Foreign</span></span></p></td>
<td><p><span data-ttu-id="02ddc-179">このセッションで使用するフロントエンドサーバーの ID です。</span><span class="sxs-lookup"><span data-stu-id="02ddc-179">ID of the front-end server used for this session.</span></span> <span data-ttu-id="02ddc-180">詳細については、「 <a href="lync-server-2013-servers-table.md">Lync Server 2013 のサーバーの表</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02ddc-180">See the <a href="lync-server-2013-servers-table.md">Servers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02ddc-181"><strong>PoolId</strong></span><span class="sxs-lookup"><span data-stu-id="02ddc-181"><strong>PoolId</strong></span></span></p></td>
<td><p><span data-ttu-id="02ddc-182">int</span><span class="sxs-lookup"><span data-stu-id="02ddc-182">int</span></span></p></td>
<td><p><span data-ttu-id="02ddc-183">外部</span><span class="sxs-lookup"><span data-stu-id="02ddc-183">Foreign</span></span></p></td>
<td><p><span data-ttu-id="02ddc-184">セッションがキャプチャされたプールの ID です。</span><span class="sxs-lookup"><span data-stu-id="02ddc-184">ID of the pool in which the session was captured.</span></span> <span data-ttu-id="02ddc-185">詳細については、「 <a href="lync-server-2013-pools-table.md">Lync Server 2013 のプールテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02ddc-185">See the <a href="lync-server-2013-pools-table.md">Pools table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02ddc-186"><strong>ContentTypeID</strong></span><span class="sxs-lookup"><span data-stu-id="02ddc-186"><strong>ContentTypeID</strong></span></span></p></td>
<td><p><span data-ttu-id="02ddc-187">int</span><span class="sxs-lookup"><span data-stu-id="02ddc-187">int</span></span></p></td>
<td><p><span data-ttu-id="02ddc-188">外部</span><span class="sxs-lookup"><span data-stu-id="02ddc-188">Foreign</span></span></p></td>
<td><p><span data-ttu-id="02ddc-189">セッションで使用されるコンテンツタイプ。</span><span class="sxs-lookup"><span data-stu-id="02ddc-189">Content type used in the session.</span></span> <span data-ttu-id="02ddc-190">詳細については、「 <a href="lync-server-2013-contenttypes-table.md">Lync Server 2013 の ContentTypes テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02ddc-190">See the <a href="lync-server-2013-contenttypes-table.md">ContentTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02ddc-191"><strong>User1ClientVerId</strong></span><span class="sxs-lookup"><span data-stu-id="02ddc-191"><strong>User1ClientVerId</strong></span></span></p></td>
<td><p><span data-ttu-id="02ddc-192">int</span><span class="sxs-lookup"><span data-stu-id="02ddc-192">int</span></span></p></td>
<td><p><span data-ttu-id="02ddc-193">外部</span><span class="sxs-lookup"><span data-stu-id="02ddc-193">Foreign</span></span></p></td>
<td><p><span data-ttu-id="02ddc-194">User1 が使用するクライアントのバージョン。</span><span class="sxs-lookup"><span data-stu-id="02ddc-194">Client version used by User1.</span></span> <span data-ttu-id="02ddc-195">詳細については、「 <a href="lync-server-2013-clientversions-table.md">Lync Server 2013 の Clientversions の表</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02ddc-195">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02ddc-196"><strong>User2ClientVerId</strong></span><span class="sxs-lookup"><span data-stu-id="02ddc-196"><strong>User2ClientVerId</strong></span></span></p></td>
<td><p><span data-ttu-id="02ddc-197">int</span><span class="sxs-lookup"><span data-stu-id="02ddc-197">int</span></span></p></td>
<td><p><span data-ttu-id="02ddc-198">外部</span><span class="sxs-lookup"><span data-stu-id="02ddc-198">Foreign</span></span></p></td>
<td><p><span data-ttu-id="02ddc-199">User2 が使用するクライアントのバージョン。</span><span class="sxs-lookup"><span data-stu-id="02ddc-199">Client version used by User2.</span></span> <span data-ttu-id="02ddc-200">詳細については、「 <a href="lync-server-2013-clientversions-table.md">Lync Server 2013 の Clientversions の表</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02ddc-200">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02ddc-201"><strong>User1EdgeServerid</strong></span><span class="sxs-lookup"><span data-stu-id="02ddc-201"><strong>User1EdgeServerid</strong></span></span></p></td>
<td><p><span data-ttu-id="02ddc-202">int</span><span class="sxs-lookup"><span data-stu-id="02ddc-202">int</span></span></p></td>
<td><p><span data-ttu-id="02ddc-203">外部</span><span class="sxs-lookup"><span data-stu-id="02ddc-203">Foreign</span></span></p></td>
<td><p><span data-ttu-id="02ddc-204">User1 で使用されるエッジサーバー。</span><span class="sxs-lookup"><span data-stu-id="02ddc-204">Edge Server used by User1.</span></span> <span data-ttu-id="02ddc-205">詳細については、「 <a href="lync-server-2013-edgeservers-table.md">Lync Server 2013 の EdgeServers テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02ddc-205">See the <a href="lync-server-2013-edgeservers-table.md">EdgeServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02ddc-206"><strong>User2EdgeServerid</strong></span><span class="sxs-lookup"><span data-stu-id="02ddc-206"><strong>User2EdgeServerid</strong></span></span></p></td>
<td><p><span data-ttu-id="02ddc-207">int</span><span class="sxs-lookup"><span data-stu-id="02ddc-207">int</span></span></p></td>
<td><p><span data-ttu-id="02ddc-208">外部</span><span class="sxs-lookup"><span data-stu-id="02ddc-208">Foreign</span></span></p></td>
<td><p><span data-ttu-id="02ddc-209">User2 によって使用されるエッジサーバー。</span><span class="sxs-lookup"><span data-stu-id="02ddc-209">Edge Server used by User2.</span></span> <span data-ttu-id="02ddc-210">詳細については、「 <a href="lync-server-2013-edgeservers-table.md">Lync Server 2013 の EdgeServers テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02ddc-210">See the <a href="lync-server-2013-edgeservers-table.md">EdgeServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02ddc-211"><strong>IsUser1Internal</strong></span><span class="sxs-lookup"><span data-stu-id="02ddc-211"><strong>IsUser1Internal</strong></span></span></p></td>
<td><p><span data-ttu-id="02ddc-212">bit</span><span class="sxs-lookup"><span data-stu-id="02ddc-212">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="02ddc-213">User1 が内部からログオンしているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="02ddc-213">Whether User1 is logged on from internal or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02ddc-214"><strong>IsUser2Internal</strong></span><span class="sxs-lookup"><span data-stu-id="02ddc-214"><strong>IsUser2Internal</strong></span></span></p></td>
<td><p><span data-ttu-id="02ddc-215">bit</span><span class="sxs-lookup"><span data-stu-id="02ddc-215">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="02ddc-216">User2 が内部からログオンしているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="02ddc-216">Whether User2 is logged on from internal or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02ddc-217"><strong>InviteTime</strong></span><span class="sxs-lookup"><span data-stu-id="02ddc-217"><strong>InviteTime</strong></span></span></p></td>
<td><p><span data-ttu-id="02ddc-218">datetime</span><span class="sxs-lookup"><span data-stu-id="02ddc-218">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="02ddc-219">最初の招待要求の時刻。</span><span class="sxs-lookup"><span data-stu-id="02ddc-219">The time of the first INVITE request.</span></span> <span data-ttu-id="02ddc-220">通常、このフィールドは、セッションの最初の INVITE メッセージから生成されたデータによって設定されます。</span><span class="sxs-lookup"><span data-stu-id="02ddc-220">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="02ddc-221">招待メッセージがない場合は、最初に関連する SIP メッセージ (BYE、キャンセル、メッセージ、または情報) の日付と時刻がフィールドに設定されています。</span><span class="sxs-lookup"><span data-stu-id="02ddc-221">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span> <span data-ttu-id="02ddc-222">通常、このフィールドは、セッションの最初の INVITE メッセージから生成されたデータによって設定されます。</span><span class="sxs-lookup"><span data-stu-id="02ddc-222">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="02ddc-223">招待メッセージがない場合は、最初に関連する SIP メッセージ (BYE、キャンセル、メッセージ、または情報) の日付と時刻がフィールドに設定されています。</span><span class="sxs-lookup"><span data-stu-id="02ddc-223">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02ddc-224"><strong>ResponseTime</strong></span><span class="sxs-lookup"><span data-stu-id="02ddc-224"><strong>ResponseTime</strong></span></span></p></td>
<td><p><span data-ttu-id="02ddc-225">datetime</span><span class="sxs-lookup"><span data-stu-id="02ddc-225">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="02ddc-226">最初の招待メッセージに対する応答の時刻。</span><span class="sxs-lookup"><span data-stu-id="02ddc-226">The time of the response to the first INVITE message.</span></span> <span data-ttu-id="02ddc-227">通常、このフィールドは、セッションの最初の INVITE メッセージから生成されたデータによって設定されます。</span><span class="sxs-lookup"><span data-stu-id="02ddc-227">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="02ddc-228">招待メッセージがない場合は、最初に関連する SIP メッセージ (BYE、キャンセル、メッセージ、または情報) の日付と時刻がフィールドに設定されています。</span><span class="sxs-lookup"><span data-stu-id="02ddc-228">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02ddc-229"><strong>返信</strong></span><span class="sxs-lookup"><span data-stu-id="02ddc-229"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="02ddc-230">int</span><span class="sxs-lookup"><span data-stu-id="02ddc-230">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="02ddc-231">セッション招待状への SIP 応答コード。</span><span class="sxs-lookup"><span data-stu-id="02ddc-231">SIP response code to the session invitation.</span></span> <span data-ttu-id="02ddc-232">通常、このフィールドは、セッションの最初の INVITE メッセージから生成されたデータによって設定されます。</span><span class="sxs-lookup"><span data-stu-id="02ddc-232">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="02ddc-233">招待メッセージがない場合は、最初に関連する SIP メッセージ (BYE、キャンセル、メッセージ、または情報) の日付と時刻がフィールドに設定されています。</span><span class="sxs-lookup"><span data-stu-id="02ddc-233">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02ddc-234"><strong>DiagnosticId</strong></span><span class="sxs-lookup"><span data-stu-id="02ddc-234"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="02ddc-235">int</span><span class="sxs-lookup"><span data-stu-id="02ddc-235">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="02ddc-236">SIP ヘッダーからキャプチャされた診断 ID。</span><span class="sxs-lookup"><span data-stu-id="02ddc-236">Diagnostic ID captured from SIP header.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02ddc-237"><strong>CallPriority</strong></span><span class="sxs-lookup"><span data-stu-id="02ddc-237"><strong>CallPriority</strong></span></span></p></td>
<td><p><span data-ttu-id="02ddc-238">int</span><span class="sxs-lookup"><span data-stu-id="02ddc-238">int</span></span></p></td>
<td><p><span data-ttu-id="02ddc-239">外部</span><span class="sxs-lookup"><span data-stu-id="02ddc-239">Foreign</span></span></p></td>
<td><p><span data-ttu-id="02ddc-240">通話の優先度。</span><span class="sxs-lookup"><span data-stu-id="02ddc-240">Call priority.</span></span> <span data-ttu-id="02ddc-241">詳細については、「 <a href="lync-server-2013-callpriorities-table.md">Lync Server 2013 の Callpriorities テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02ddc-241">See the <a href="lync-server-2013-callpriorities-table.md">CallPriorities table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02ddc-242"><strong>User1MessageCount</strong></span><span class="sxs-lookup"><span data-stu-id="02ddc-242"><strong>User1MessageCount</strong></span></span></p></td>
<td><p><span data-ttu-id="02ddc-243">int</span><span class="sxs-lookup"><span data-stu-id="02ddc-243">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="02ddc-244">セッション中に User1 から送信されたメッセージの数です。</span><span class="sxs-lookup"><span data-stu-id="02ddc-244">Number of messages sent by User1 during the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02ddc-245"><strong>User2MessageCount</strong></span><span class="sxs-lookup"><span data-stu-id="02ddc-245"><strong>User2MessageCount</strong></span></span></p></td>
<td><p><span data-ttu-id="02ddc-246">int</span><span class="sxs-lookup"><span data-stu-id="02ddc-246">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="02ddc-247">セッション中に User2 から送信されたメッセージの数です。</span><span class="sxs-lookup"><span data-stu-id="02ddc-247">Number of messages sent by User2 during the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02ddc-248"><strong>セッション終了時刻</strong></span><span class="sxs-lookup"><span data-stu-id="02ddc-248"><strong>SessionEndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="02ddc-249">datetime</span><span class="sxs-lookup"><span data-stu-id="02ddc-249">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="02ddc-250">セッションの終了時。</span><span class="sxs-lookup"><span data-stu-id="02ddc-250">Time at the end of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02ddc-251"><strong>MediaTypes</strong></span><span class="sxs-lookup"><span data-stu-id="02ddc-251"><strong>MediaTypes</strong></span></span></p></td>
<td><p><span data-ttu-id="02ddc-252">int</span><span class="sxs-lookup"><span data-stu-id="02ddc-252">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="02ddc-253">このセッションのメディアの種類を示すビットセット。</span><span class="sxs-lookup"><span data-stu-id="02ddc-253">A bit set that indicates the media type of this session.</span></span> <span data-ttu-id="02ddc-254">表示される型の定義を次に示します。</span><span class="sxs-lookup"><span data-stu-id="02ddc-254">Listed are the definitions of the types:</span></span></p>
<h3 id="section-1"> </h3>
<div>
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="02ddc-255">インスタント メッセージ</span><span class="sxs-lookup"><span data-stu-id="02ddc-255">IM</span></span></p></td>
<td><p><span data-ttu-id="02ddc-256">1</span><span class="sxs-lookup"><span data-stu-id="02ddc-256">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02ddc-257">FILE_TRANSFER</span><span class="sxs-lookup"><span data-stu-id="02ddc-257">FILE_TRANSFER</span></span></p></td>
<td><p><span data-ttu-id="02ddc-258">2</span><span class="sxs-lookup"><span data-stu-id="02ddc-258">2</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02ddc-259">REMOTE_ASSISTANCE</span><span class="sxs-lookup"><span data-stu-id="02ddc-259">REMOTE_ASSISTANCE</span></span></p></td>
<td><p><span data-ttu-id="02ddc-260">4</span><span class="sxs-lookup"><span data-stu-id="02ddc-260">4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02ddc-261">APP_SHARING</span><span class="sxs-lookup"><span data-stu-id="02ddc-261">APP_SHARING</span></span></p></td>
<td><p><span data-ttu-id="02ddc-262">個</span><span class="sxs-lookup"><span data-stu-id="02ddc-262">8</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02ddc-263">オーディオトランジション</span><span class="sxs-lookup"><span data-stu-id="02ddc-263">AUDIO</span></span></p></td>
<td><p><span data-ttu-id="02ddc-264">16</span><span class="sxs-lookup"><span data-stu-id="02ddc-264">16</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02ddc-265">ビデオ</span><span class="sxs-lookup"><span data-stu-id="02ddc-265">VIDEO</span></span></p></td>
<td><p><span data-ttu-id="02ddc-266">32</span><span class="sxs-lookup"><span data-stu-id="02ddc-266">32</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02ddc-267">APP_INVITE</span><span class="sxs-lookup"><span data-stu-id="02ddc-267">APP_INVITE</span></span></p></td>
<td><p><span data-ttu-id="02ddc-268">64</span><span class="sxs-lookup"><span data-stu-id="02ddc-268">64</span></span></p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02ddc-269"><strong>User1Flag</strong></span><span class="sxs-lookup"><span data-stu-id="02ddc-269"><strong>User1Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="02ddc-270">smallint</span><span class="sxs-lookup"><span data-stu-id="02ddc-270">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="02ddc-271">User1 属性を示すビットセット。</span><span class="sxs-lookup"><span data-stu-id="02ddc-271">A bit set that indicates the User1 attributes.</span></span> <span data-ttu-id="02ddc-272">次の属性定義が表示されます。</span><span class="sxs-lookup"><span data-stu-id="02ddc-272">The following attribute definitions are listed:</span></span></p>
<ul>
<li><p><span data-ttu-id="02ddc-273">0x01-デスクトップ電話と統合</span><span class="sxs-lookup"><span data-stu-id="02ddc-273">0x01 - Integrated with desktop phone</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02ddc-274"><strong>User2Flag</strong></span><span class="sxs-lookup"><span data-stu-id="02ddc-274"><strong>User2Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="02ddc-275">smallint</span><span class="sxs-lookup"><span data-stu-id="02ddc-275">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="02ddc-276">User2 の属性を示すビットセット。</span><span class="sxs-lookup"><span data-stu-id="02ddc-276">A bit set that indicates the User2 attributes.</span></span> <span data-ttu-id="02ddc-277">次の属性定義が表示されます。</span><span class="sxs-lookup"><span data-stu-id="02ddc-277">The following attribute definitions are listed:</span></span></p>
<ul>
<li><p><span data-ttu-id="02ddc-278">0x01-デスクトップ電話と統合</span><span class="sxs-lookup"><span data-stu-id="02ddc-278">0x01 - Integrated with desktop phone</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02ddc-279"><strong>CallFlag</strong></span><span class="sxs-lookup"><span data-stu-id="02ddc-279"><strong>CallFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="02ddc-280">smallint</span><span class="sxs-lookup"><span data-stu-id="02ddc-280">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="02ddc-281">呼び出し属性を示すビットセット。</span><span class="sxs-lookup"><span data-stu-id="02ddc-281">A bit set that indicates the call attributes.</span></span> <span data-ttu-id="02ddc-282">次の属性定義が表示されます。</span><span class="sxs-lookup"><span data-stu-id="02ddc-282">The following attribute definitions are listed:</span></span></p>
<ul>
<li><p><span data-ttu-id="02ddc-283">0x01-再試行セッション</span><span class="sxs-lookup"><span data-stu-id="02ddc-283">0x01 - Retried Session</span></span></p></li>
<li><p><span data-ttu-id="02ddc-284">0x02-応答グループの代理としてエージェントによって発信された通話</span><span class="sxs-lookup"><span data-stu-id="02ddc-284">0x02 - A call made by agent on behalf of a response group</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02ddc-285"><strong>処理</strong></span><span class="sxs-lookup"><span data-stu-id="02ddc-285"><strong>Processed</strong></span></span></p></td>
<td><p><span data-ttu-id="02ddc-286">bit</span><span class="sxs-lookup"><span data-stu-id="02ddc-286">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="02ddc-287">監視サービスで内部的に使用されます。</span><span class="sxs-lookup"><span data-stu-id="02ddc-287">For internal use by the Monitoring service.</span></span></p>
<p><span data-ttu-id="02ddc-288">このフィールドは、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="02ddc-288">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="02ddc-289">\* ほとんどのセッションでは、SessionIdSeq の値は1になります。</span><span class="sxs-lookup"><span data-stu-id="02ddc-289">\* For most sessions, SessionIdSeq will have the value of 1.</span></span> <span data-ttu-id="02ddc-290">複数のセッションが同時に開始された場合は、1つのセッションの SessionIdSeq は1、それ以外の場合は2となります。</span><span class="sxs-lookup"><span data-stu-id="02ddc-290">If multiple sessions start at exactly the same time, the SessionIdSeq for one will be 1, for another will be 2, and so on.</span></span>

<span data-ttu-id="02ddc-291"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="02ddc-291"></div>

<span> </span>

</div>

</div>

</span></span></div>

