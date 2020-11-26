---
title: 'Lync Server 2013: McuJoinsAndLeaves テーブル'
description: 'Lync Server 2013: McuJoinsAndLeaves テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: McuJoinsAndLeaves table
ms:assetid: 4e073366-0b5d-45b4-a3f6-d63dd5fd9f25
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398316(v=OCS.15)
ms:contentKeyID: 48184115
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ee7d9473892ac357dcefd80b0d52382c5dd7d930
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425753"
---
# <a name="mcujoinsandleaves-table-in-lync-server-2013"></a><span data-ttu-id="830c5-103">Lync Server 2013 の McuJoinsAndLeaves テーブル</span><span class="sxs-lookup"><span data-stu-id="830c5-103">McuJoinsAndLeaves table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="830c5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="830c5-104">

<span> </span></span></span>

<span data-ttu-id="830c5-105">_**最終更新日:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="830c5-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="830c5-106">この表の各レコードには、ユーザーの参加または退出と会議サーバーの1つの組み合わせについての通話の詳細が含まれています。</span><span class="sxs-lookup"><span data-stu-id="830c5-106">Each record in this table contains call details about one combination of a user join or leave and conferencing server.</span></span> <span data-ttu-id="830c5-107">たとえば、web 会議や音声/ビデオの要素を含む会議にユーザーが参加した場合、そのユーザーの web 会議参加用に1つのレコードが作成され、ユーザーの音声/ビデオ会議の参加用に別のレコードが作成されます。</span><span class="sxs-lookup"><span data-stu-id="830c5-107">For example, if a user joins a conference that includes web conferencing and audio/video elements, one record would be created for that user’s web conferencing join, and another record would be created for the user’s audio/video conferencing join.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="830c5-108">列</span><span class="sxs-lookup"><span data-stu-id="830c5-108">Column</span></span></th>
<th><span data-ttu-id="830c5-109">データ型</span><span class="sxs-lookup"><span data-stu-id="830c5-109">Data Type</span></span></th>
<th><span data-ttu-id="830c5-110">キー/インデックス</span><span class="sxs-lookup"><span data-stu-id="830c5-110">Key/Index</span></span></th>
<th><span data-ttu-id="830c5-111">詳細</span><span class="sxs-lookup"><span data-stu-id="830c5-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="830c5-112"><strong>セッション Id</strong></span><span class="sxs-lookup"><span data-stu-id="830c5-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="830c5-113">datetime</span><span class="sxs-lookup"><span data-stu-id="830c5-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="830c5-114">プライマリ、外部</span><span class="sxs-lookup"><span data-stu-id="830c5-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="830c5-115">会議インスタンスの時刻。</span><span class="sxs-lookup"><span data-stu-id="830c5-115">Time of conference instance.</span></span> <span data-ttu-id="830c5-116">電話会議インスタンスを一意に識別するために <strong>Sessionidseq</strong> と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="830c5-116">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a conference instance.</span></span> <span data-ttu-id="830c5-117">詳細については、「 <a href="lync-server-2013-conferences-table.md">Lync Server 2013 での会議の表</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="830c5-117">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="830c5-118"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="830c5-118"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="830c5-119">int</span><span class="sxs-lookup"><span data-stu-id="830c5-119">int</span></span></p></td>
<td><p><span data-ttu-id="830c5-120">プライマリ、外部</span><span class="sxs-lookup"><span data-stu-id="830c5-120">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="830c5-121">会議インスタンスを識別する ID 番号。</span><span class="sxs-lookup"><span data-stu-id="830c5-121">ID number to identify the conference instance.</span></span> <span data-ttu-id="830c5-122">電話会議インスタンスを一意に識別するために <strong>Sessionidtime</strong> と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="830c5-122">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a conference instance.</span></span> <span data-ttu-id="830c5-123">詳細については、「 <a href="lync-server-2013-conferences-table.md">Lync Server 2013 での会議の表</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="830c5-123">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="830c5-124"><strong>UserId</strong></span><span class="sxs-lookup"><span data-stu-id="830c5-124"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="830c5-125">int</span><span class="sxs-lookup"><span data-stu-id="830c5-125">int</span></span></p></td>
<td><p><span data-ttu-id="830c5-126">プライマリ、外部</span><span class="sxs-lookup"><span data-stu-id="830c5-126">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="830c5-127">このユーザーを識別する一意の番号です。</span><span class="sxs-lookup"><span data-stu-id="830c5-127">Unique number identifying this user.</span></span> <span data-ttu-id="830c5-128">詳細については、「 <a href="lync-server-2013-users-table.md">Lync Server 2013 のユーザーテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="830c5-128">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="830c5-129"><strong>McuUserInstance</strong></span><span class="sxs-lookup"><span data-stu-id="830c5-129"><strong>McuUserInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="830c5-130">int</span><span class="sxs-lookup"><span data-stu-id="830c5-130">int</span></span></p></td>
<td><p><span data-ttu-id="830c5-131">Primary</span><span class="sxs-lookup"><span data-stu-id="830c5-131">Primary</span></span></p></td>
<td><p><span data-ttu-id="830c5-132">ユーザーが複数のコンピューターまたはデバイスに一度にログオンしている場合、McuUserInstance はユーザーとデバイスの組み合わせを一意に識別します。</span><span class="sxs-lookup"><span data-stu-id="830c5-132">If a user is logged on at multiple computers or devices at once, McuUserInstance uniquely identifies the user/device combination.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="830c5-133"><strong>IsFromPstn</strong></span><span class="sxs-lookup"><span data-stu-id="830c5-133"><strong>IsFromPstn</strong></span></span></p></td>
<td><p><span data-ttu-id="830c5-134">bit</span><span class="sxs-lookup"><span data-stu-id="830c5-134">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="830c5-135">ユーザーが PSTN から参加しているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="830c5-135">Whether the user is joining from a PSTN or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="830c5-136"><strong>McuId</strong></span><span class="sxs-lookup"><span data-stu-id="830c5-136"><strong>McuId</strong></span></span></p></td>
<td><p><span data-ttu-id="830c5-137">int</span><span class="sxs-lookup"><span data-stu-id="830c5-137">int</span></span></p></td>
<td><p><span data-ttu-id="830c5-138">プライマリ、外部</span><span class="sxs-lookup"><span data-stu-id="830c5-138">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="830c5-139">この会議サーバーを識別する一意の番号です。</span><span class="sxs-lookup"><span data-stu-id="830c5-139">Unique number identifying this conferencing server.</span></span> <span data-ttu-id="830c5-140">詳細については、「 <a href="lync-server-2013-mcus-table.md">Lync Server 2013 での mcu の表</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="830c5-140">See the <a href="lync-server-2013-mcus-table.md">Mcus table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="830c5-141"><strong>/セッション Id</strong></span><span class="sxs-lookup"><span data-stu-id="830c5-141"><strong>DialogSessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="830c5-142">datetime</span><span class="sxs-lookup"><span data-stu-id="830c5-142">datetime</span></span></p></td>
<td><p><span data-ttu-id="830c5-143">外部</span><span class="sxs-lookup"><span data-stu-id="830c5-143">Foreign</span></span></p></td>
<td><p><span data-ttu-id="830c5-144">セッション要求の時刻。</span><span class="sxs-lookup"><span data-stu-id="830c5-144">Time of session request.</span></span> <span data-ttu-id="830c5-145">セッションを一意に識別するために <strong>Sessionidseq</strong> と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="830c5-145">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="830c5-146">詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="830c5-146">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="830c5-147"><strong>"/セッション Id"</strong></span><span class="sxs-lookup"><span data-stu-id="830c5-147"><strong>DialogSessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="830c5-148">int</span><span class="sxs-lookup"><span data-stu-id="830c5-148">int</span></span></p></td>
<td><p><span data-ttu-id="830c5-149">外部</span><span class="sxs-lookup"><span data-stu-id="830c5-149">Foreign</span></span></p></td>
<td><p><span data-ttu-id="830c5-150">セッションを識別する ID 番号。</span><span class="sxs-lookup"><span data-stu-id="830c5-150">ID number to identify the session.</span></span> <span data-ttu-id="830c5-151">セッションを一意に識別するために <strong>Sessionidtime</strong> と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="830c5-151">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="830c5-152">詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="830c5-152">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="830c5-153"><strong>UserJoinTime</strong></span><span class="sxs-lookup"><span data-stu-id="830c5-153"><strong>UserJoinTime</strong></span></span></p></td>
<td><p><span data-ttu-id="830c5-154">datetime</span><span class="sxs-lookup"><span data-stu-id="830c5-154">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="830c5-155">このユーザーがこの会議サーバーに参加する時刻です。</span><span class="sxs-lookup"><span data-stu-id="830c5-155">The time this user joins this conferencing server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="830c5-156"><strong>UserLeaveTime</strong></span><span class="sxs-lookup"><span data-stu-id="830c5-156"><strong>UserLeaveTime</strong></span></span></p></td>
<td><p><span data-ttu-id="830c5-157">datetime</span><span class="sxs-lookup"><span data-stu-id="830c5-157">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="830c5-158">このユーザーがこの会議サーバーから退席した時刻。</span><span class="sxs-lookup"><span data-stu-id="830c5-158">The time this user leaves this conferencing server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="830c5-159"><strong>ClientVerId</strong></span><span class="sxs-lookup"><span data-stu-id="830c5-159"><strong>ClientVerId</strong></span></span></p></td>
<td><p><span data-ttu-id="830c5-160">int</span><span class="sxs-lookup"><span data-stu-id="830c5-160">int</span></span></p></td>
<td><p><span data-ttu-id="830c5-161">外部</span><span class="sxs-lookup"><span data-stu-id="830c5-161">Foreign</span></span></p></td>
<td><p><span data-ttu-id="830c5-162">電話会議で使用するクライアントソフトウェアのバージョン番号を指定する識別子。</span><span class="sxs-lookup"><span data-stu-id="830c5-162">Identifier that specifies the version number of the client software use in the conference.</span></span> <span data-ttu-id="830c5-163">詳細については、「 <a href="lync-server-2013-clientversions-table.md">Lync Server 2013 の Clientversions の表</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="830c5-163">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p>
<p><span data-ttu-id="830c5-164">このフィールドは、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="830c5-164">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="830c5-165">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="830c5-165">


</div>

<span> </span>

</div>

</div>

</span></span></div>

