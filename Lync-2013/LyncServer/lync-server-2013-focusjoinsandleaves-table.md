---
title: 'Lync Server 2013: FocusJoinsAndLeaves テーブル'
description: 'Lync Server 2013: FocusJoinsAndLeaves テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: FocusJoinsAndLeaves table
ms:assetid: e6f0212c-67e9-4061-8720-d0296e855991
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399026(v=OCS.15)
ms:contentKeyID: 48185690
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5796de16ed204ce4f33935d937cbaa425d63a67f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428109"
---
# <a name="focusjoinsandleaves-table-in-lync-server-2013"></a><span data-ttu-id="77251-103">Lync Server 2013 の FocusJoinsAndLeaves テーブル</span><span class="sxs-lookup"><span data-stu-id="77251-103">FocusJoinsAndLeaves table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="77251-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="77251-104">

<span> </span></span></span>

<span data-ttu-id="77251-105">_**最終更新日:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="77251-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="77251-106">このテーブルの各レコードには、1人のユーザーの参加に関する CDR 情報と、1人の会議に関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="77251-106">Each record in this table contains the CDR information about one user’s join and leave information for one conference.</span></span> <span data-ttu-id="77251-107">各会議は、ユーザーが会議に参加して退席するたびに、1つのレコードでこのテーブルに表示されます。</span><span class="sxs-lookup"><span data-stu-id="77251-107">Each conference is represented in this table by one record for each time a user joins and leaves the conference.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="77251-108">列</span><span class="sxs-lookup"><span data-stu-id="77251-108">Column</span></span></th>
<th><span data-ttu-id="77251-109">データ型</span><span class="sxs-lookup"><span data-stu-id="77251-109">Data Type</span></span></th>
<th><span data-ttu-id="77251-110">キー/インデックス</span><span class="sxs-lookup"><span data-stu-id="77251-110">Key/Index</span></span></th>
<th><span data-ttu-id="77251-111">詳細</span><span class="sxs-lookup"><span data-stu-id="77251-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="77251-112"><strong>セッション Id</strong></span><span class="sxs-lookup"><span data-stu-id="77251-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="77251-113">datetime</span><span class="sxs-lookup"><span data-stu-id="77251-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="77251-114">プライマリ、外部</span><span class="sxs-lookup"><span data-stu-id="77251-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="77251-115">会議インスタンスの時刻。</span><span class="sxs-lookup"><span data-stu-id="77251-115">Time of conference instance.</span></span> <span data-ttu-id="77251-116">電話会議インスタンスを一意に識別するために <strong>Sessionidseq</strong> と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="77251-116">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a conference instance.</span></span> <span data-ttu-id="77251-117">詳細については、「 <a href="lync-server-2013-conferences-table.md">Lync Server 2013 での会議の表</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="77251-117">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77251-118"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="77251-118"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="77251-119">int</span><span class="sxs-lookup"><span data-stu-id="77251-119">int</span></span></p></td>
<td><p><span data-ttu-id="77251-120">プライマリ、外部</span><span class="sxs-lookup"><span data-stu-id="77251-120">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="77251-121">会議インスタンスを識別する ID 番号。</span><span class="sxs-lookup"><span data-stu-id="77251-121">ID number to identify the conference instance.</span></span> <span data-ttu-id="77251-122">電話会議インスタンスを一意に識別するために <strong>Sessionidtime</strong> と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="77251-122">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a conference instance.</span></span> <span data-ttu-id="77251-123">詳細については、「 <a href="lync-server-2013-conferences-table.md">Lync Server 2013 での会議の表</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="77251-123">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77251-124"><strong>/セッション Id</strong></span><span class="sxs-lookup"><span data-stu-id="77251-124"><strong>DialogSessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="77251-125">datetime</span><span class="sxs-lookup"><span data-stu-id="77251-125">datetime</span></span></p></td>
<td><p><span data-ttu-id="77251-126">プライマリ、外部</span><span class="sxs-lookup"><span data-stu-id="77251-126">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="77251-127">セッション要求の時刻。</span><span class="sxs-lookup"><span data-stu-id="77251-127">Time of session request.</span></span> <span data-ttu-id="77251-128">セッションを一意に識別するために <strong>Sessionidseq</strong> と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="77251-128">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="77251-129">詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="77251-129">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77251-130"><strong>"/セッション Id"</strong></span><span class="sxs-lookup"><span data-stu-id="77251-130"><strong>DialogSessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="77251-131">int</span><span class="sxs-lookup"><span data-stu-id="77251-131">int</span></span></p></td>
<td><p><span data-ttu-id="77251-132">プライマリ、外部</span><span class="sxs-lookup"><span data-stu-id="77251-132">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="77251-133">セッションを識別する ID 番号。</span><span class="sxs-lookup"><span data-stu-id="77251-133">ID number to identify the session.</span></span> <span data-ttu-id="77251-134">セッションを一意に識別するために <strong>Sessionidtime</strong> と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="77251-134">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="77251-135">詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="77251-135">see the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77251-136"><strong>UserId</strong></span><span class="sxs-lookup"><span data-stu-id="77251-136"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="77251-137">int</span><span class="sxs-lookup"><span data-stu-id="77251-137">int</span></span></p></td>
<td><p><span data-ttu-id="77251-138">外部</span><span class="sxs-lookup"><span data-stu-id="77251-138">Foreign</span></span></p></td>
<td><p><span data-ttu-id="77251-139">このユーザーを識別する一意の番号です。 <a href="lync-server-2013-users-table.md">Lync Server 2013 の [ユーザー] テーブル</a>から参照されます。</span><span class="sxs-lookup"><span data-stu-id="77251-139">Unique number identifying this user, referenced from the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77251-140"><strong>FocusUserInstance</strong></span><span class="sxs-lookup"><span data-stu-id="77251-140"><strong>FocusUserInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="77251-141">int</span><span class="sxs-lookup"><span data-stu-id="77251-141">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="77251-142">ユーザーが複数のコンピューターまたはデバイスに同時にログオンしている場合は、 <strong>UserInstance</strong> を使って、ユーザーとデバイスの組み合わせを一意に識別します。</span><span class="sxs-lookup"><span data-stu-id="77251-142">If a user is logged on at multiple computers or devices at the same time, <strong>UserInstance</strong> is used to uniquely identify the user/device combination.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77251-143"><strong>IsUserInternal</strong></span><span class="sxs-lookup"><span data-stu-id="77251-143"><strong>IsUserInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="77251-144">bit</span><span class="sxs-lookup"><span data-stu-id="77251-144">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="77251-145">ユーザーが内部からログオンしているかどうか。</span><span class="sxs-lookup"><span data-stu-id="77251-145">Whether the user logged on from internal or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77251-146"><strong>UserRole</strong></span><span class="sxs-lookup"><span data-stu-id="77251-146"><strong>UserRole</strong></span></span></p></td>
<td><p><span data-ttu-id="77251-147">int</span><span class="sxs-lookup"><span data-stu-id="77251-147">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="77251-148">会議でのこのユーザーの役割 (発表者や出席者など)</span><span class="sxs-lookup"><span data-stu-id="77251-148">This user’s role in the conference, such as Presenter or Attendee.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77251-149"><strong>UserJoinTime</strong></span><span class="sxs-lookup"><span data-stu-id="77251-149"><strong>UserJoinTime</strong></span></span></p></td>
<td><p><span data-ttu-id="77251-150">datetime</span><span class="sxs-lookup"><span data-stu-id="77251-150">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="77251-151">このユーザーが会議に参加した時刻。</span><span class="sxs-lookup"><span data-stu-id="77251-151">The time this user joins the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77251-152"><strong>UserLeaveTime</strong></span><span class="sxs-lookup"><span data-stu-id="77251-152"><strong>UserLeaveTime</strong></span></span></p></td>
<td><p><span data-ttu-id="77251-153">datetime</span><span class="sxs-lookup"><span data-stu-id="77251-153">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="77251-154">このユーザーが会議から退席した時刻。</span><span class="sxs-lookup"><span data-stu-id="77251-154">The time this user leaves the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77251-155"><strong>ClientVerId</strong></span><span class="sxs-lookup"><span data-stu-id="77251-155"><strong>ClientVerId</strong></span></span></p></td>
<td><p><span data-ttu-id="77251-156">int</span><span class="sxs-lookup"><span data-stu-id="77251-156">int</span></span></p></td>
<td><p><span data-ttu-id="77251-157">外部</span><span class="sxs-lookup"><span data-stu-id="77251-157">Foreign</span></span></p></td>
<td><p><span data-ttu-id="77251-158">ユーザーのクライアントソフトウェアのバージョン。 <a href="lync-server-2013-clientversions-table.md">Lync Server 2013 の Clientversions テーブル</a>に参照されます。</span><span class="sxs-lookup"><span data-stu-id="77251-158">Version of the user’s client software, referenced to the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77251-159"><strong>UserEndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="77251-159"><strong>UserEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="77251-160">長さ</span><span class="sxs-lookup"><span data-stu-id="77251-160">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="77251-161">電話会議で使用されるエンドポイントのグローバル一意識別子 (GUID)。</span><span class="sxs-lookup"><span data-stu-id="77251-161">Globally unique identifier (GUID) of the endpoint used in the conference.</span></span></p>
<p><span data-ttu-id="77251-162">このフィールドは、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="77251-162">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="77251-163">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="77251-163">


</div>

<span> </span>

</div>

</div>

</span></span></div>

