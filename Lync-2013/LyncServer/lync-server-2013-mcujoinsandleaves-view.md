---
title: 'Lync Server 2013: McuJoinsAndLeaves view'
description: 'Lync Server 2013: McuJoinsAndLeaves ビュー。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: McuJoinsAndLeaves view
ms:assetid: 6f00b8e7-b8b6-4657-ac5e-d8a571806ae2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688088(v=OCS.15)
ms:contentKeyID: 49733687
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f7f2f51c340d5bd4824a6e8eff1a0da172a758c9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425732"
---
# <a name="mcujoinsandleaves-view-in-lync-server-2013"></a><span data-ttu-id="39d81-103">Lync Server 2013 での McuJoinsAndLeaves の表示</span><span class="sxs-lookup"><span data-stu-id="39d81-103">McuJoinsAndLeaves view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="39d81-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="39d81-104">

<span> </span></span></span>

<span data-ttu-id="39d81-105">_**最終更新日:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="39d81-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="39d81-106">McuJoinsAndLeaves ビューには、1台の会議サーバーの情報の参加と脱退に関する情報が格納されます。</span><span class="sxs-lookup"><span data-stu-id="39d81-106">The McuJoinsAndLeaves view stores information about users join and leave information for one conference server.</span></span> <span data-ttu-id="39d81-107">このビューの各レコードには、ユーザーの参加または退出と会議サーバーの1つの組み合わせについての通話の詳細が含まれています。</span><span class="sxs-lookup"><span data-stu-id="39d81-107">Each record in this view contains call details about one combination of a user join or leave and conferencing server.</span></span> <span data-ttu-id="39d81-108">このビューは、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="39d81-108">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="39d81-109">列</span><span class="sxs-lookup"><span data-stu-id="39d81-109">Column</span></span></th>
<th><span data-ttu-id="39d81-110">データ型</span><span class="sxs-lookup"><span data-stu-id="39d81-110">Data Type</span></span></th>
<th><span data-ttu-id="39d81-111">詳細</span><span class="sxs-lookup"><span data-stu-id="39d81-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39d81-112"><strong>セッション Id</strong></span><span class="sxs-lookup"><span data-stu-id="39d81-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="39d81-113">datetime</span><span class="sxs-lookup"><span data-stu-id="39d81-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="39d81-114">会議インスタンスの時刻。</span><span class="sxs-lookup"><span data-stu-id="39d81-114">Time of conference instance.</span></span> <span data-ttu-id="39d81-115">電話会議インスタンスを一意に識別するために SessionIdSeq と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="39d81-115">Used in conjunction with SessionIdSeq to uniquely identify a conference instance.</span></span> <span data-ttu-id="39d81-116">詳細については、「 <a href="lync-server-2013-conferences-table.md">Lync Server 2013 での会議の表</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39d81-116">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39d81-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="39d81-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="39d81-118">int</span><span class="sxs-lookup"><span data-stu-id="39d81-118">int</span></span></p></td>
<td><p><span data-ttu-id="39d81-119">会議インスタンスを識別する ID 番号。</span><span class="sxs-lookup"><span data-stu-id="39d81-119">ID number to identify the conference instance.</span></span> <span data-ttu-id="39d81-120">電話会議インスタンスを一意に識別するために SessionIdTime と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="39d81-120">Used in conjunction with SessionIdTime to uniquely identify a conference instance.</span></span> <span data-ttu-id="39d81-121">詳細については、「 <a href="lync-server-2013-conferences-table.md">Lync Server 2013 での会議の表</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39d81-121">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39d81-122"><strong>McuUri</strong></span><span class="sxs-lookup"><span data-stu-id="39d81-122"><strong>McuUri</strong></span></span></p></td>
<td><p><span data-ttu-id="39d81-123">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="39d81-123">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="39d81-124">ユーザーが接続した会議サーバーの URI。</span><span class="sxs-lookup"><span data-stu-id="39d81-124">The URI of the conferencing server that the user connected to.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39d81-125"><strong>McuUriType</strong></span><span class="sxs-lookup"><span data-stu-id="39d81-125"><strong>McuUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="39d81-126">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="39d81-126">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="39d81-127">ユーザーが接続した会議サーバーの URI。</span><span class="sxs-lookup"><span data-stu-id="39d81-127">The URI of the conferencing server that the user connected to.</span></span> <span data-ttu-id="39d81-128">詳細については、「 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 の UriTypes テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39d81-128">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39d81-129"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="39d81-129"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="39d81-130">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="39d81-130">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="39d81-131">会議サーバーの参加/脱退情報がキャプチャされたユーザーの URI です。</span><span class="sxs-lookup"><span data-stu-id="39d81-131">The URI of the user whose conferencing server join/leave information was captured.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39d81-132"><strong>UserUriType</strong></span><span class="sxs-lookup"><span data-stu-id="39d81-132"><strong>UserUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="39d81-133">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="39d81-133">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="39d81-134">会議サーバーの参加/脱退情報がキャプチャされたユーザーの URI の種類です。</span><span class="sxs-lookup"><span data-stu-id="39d81-134">The type of URI of the user whose conferencing server join/leave information was captured.</span></span> <span data-ttu-id="39d81-135">詳細については、「 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 の UriTypes テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39d81-135">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39d81-136"><strong>UserTenant</strong></span><span class="sxs-lookup"><span data-stu-id="39d81-136"><strong>UserTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="39d81-137">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="39d81-137">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="39d81-138">会議サーバーの参加/脱退情報がキャプチャされたユーザーのテナント。</span><span class="sxs-lookup"><span data-stu-id="39d81-138">The tenant of the user whose conferencing server join/leave information was captured.</span></span> <span data-ttu-id="39d81-139">詳細については、「 <a href="lync-server-2013-tenants-table.md">Lync Server 2013 のテナントの一覧</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39d81-139">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39d81-140"><strong>UserClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="39d81-140"><strong>UserClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="39d81-141">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="39d81-141">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="39d81-142">会議サーバーの参加/退席中の情報がキャプチャされたユーザーによって使用されたクライアントのバージョン。</span><span class="sxs-lookup"><span data-stu-id="39d81-142">The version of client used by the user whose conferencing server join/leave information was captured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39d81-143"><strong>UserClientType</strong></span><span class="sxs-lookup"><span data-stu-id="39d81-143"><strong>UserClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="39d81-144">int</span><span class="sxs-lookup"><span data-stu-id="39d81-144">int</span></span></p></td>
<td><p><span data-ttu-id="39d81-145">会議サーバーの参加/脱退情報がキャプチャされたユーザーによって使用されたクライアント。</span><span class="sxs-lookup"><span data-stu-id="39d81-145">The client used by the user whose conferencing server join/leave information was captured.</span></span> <span data-ttu-id="39d81-146">詳細については、「 <a href="lync-server-2013-useragentdef-table.md">Lync Server 2013 の Useragentdef テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39d81-146">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39d81-147"><strong>UserClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="39d81-147"><strong>UserClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="39d81-148">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="39d81-148">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="39d81-149">会議サーバーの参加/脱退情報がキャプチャされたユーザーによって使用されたクライアントのカテゴリの名前です。</span><span class="sxs-lookup"><span data-stu-id="39d81-149">The name of the category of the client used by the user whose conferencing server join/leave information was captured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39d81-150"><strong>McuUserInstance</strong></span><span class="sxs-lookup"><span data-stu-id="39d81-150"><strong>McuUserInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="39d81-151">int</span><span class="sxs-lookup"><span data-stu-id="39d81-151">int</span></span></p></td>
<td><p><span data-ttu-id="39d81-152">複数のデバイスに同時にログオンしているユーザーのために、ユーザーとデバイスの組み合わせを一意に識別します。</span><span class="sxs-lookup"><span data-stu-id="39d81-152">Uniquely identifies the user/device combination for users simultaneously logged on to multiple devices.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39d81-153"><strong>IsUserFromPstn</strong></span><span class="sxs-lookup"><span data-stu-id="39d81-153"><strong>IsUserFromPstn</strong></span></span></p></td>
<td><p><span data-ttu-id="39d81-154">bit</span><span class="sxs-lookup"><span data-stu-id="39d81-154">bit</span></span></p></td>
<td><p><span data-ttu-id="39d81-155">ユーザーが内部ユーザーかどうかを表すビット。</span><span class="sxs-lookup"><span data-stu-id="39d81-155">Bit that represents whether the user is an internal user or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39d81-156"><strong>/セッション Id</strong></span><span class="sxs-lookup"><span data-stu-id="39d81-156"><strong>DialogSessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="39d81-157">datetime</span><span class="sxs-lookup"><span data-stu-id="39d81-157">datetime</span></span></p></td>
<td><p><span data-ttu-id="39d81-158">セッション要求の時刻。</span><span class="sxs-lookup"><span data-stu-id="39d81-158">Time of session request.</span></span> <span data-ttu-id="39d81-159">セッションを一意に識別するために SessionIdSeq と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="39d81-159">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="39d81-160">詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39d81-160">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39d81-161"><strong>"/セッション Id"</strong></span><span class="sxs-lookup"><span data-stu-id="39d81-161"><strong>DialogSessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="39d81-162">int</span><span class="sxs-lookup"><span data-stu-id="39d81-162">int</span></span></p></td>
<td><p><span data-ttu-id="39d81-163">セッションを識別する ID 番号。</span><span class="sxs-lookup"><span data-stu-id="39d81-163">ID number to identify the session.</span></span> <span data-ttu-id="39d81-164">セッションを一意に識別するために SessionIdTime と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="39d81-164">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="39d81-165">詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39d81-165">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39d81-166"><strong>この Id</strong></span><span class="sxs-lookup"><span data-stu-id="39d81-166"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="39d81-167">varchar (775)</span><span class="sxs-lookup"><span data-stu-id="39d81-167">varchar(775)</span></span></p></td>
<td><p><span data-ttu-id="39d81-168">セッションの SIP ダイアログ ID。</span><span class="sxs-lookup"><span data-stu-id="39d81-168">SIP dialog ID of the session.</span></span> <span data-ttu-id="39d81-169">形式は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="39d81-169">The format is: dialog;from-tag;to-tag.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39d81-170"><strong>UserJoinTime</strong></span><span class="sxs-lookup"><span data-stu-id="39d81-170"><strong>UserJoinTime</strong></span></span></p></td>
<td><p><span data-ttu-id="39d81-171">datetime</span><span class="sxs-lookup"><span data-stu-id="39d81-171">datetime</span></span></p></td>
<td><p><span data-ttu-id="39d81-172">ユーザーが会議サーバーに参加した時刻。</span><span class="sxs-lookup"><span data-stu-id="39d81-172">Time the user joined the conferencing server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39d81-173"><strong>UserLeaveTime</strong></span><span class="sxs-lookup"><span data-stu-id="39d81-173"><strong>UserLeaveTime</strong></span></span></p></td>
<td><p><span data-ttu-id="39d81-174">datetime</span><span class="sxs-lookup"><span data-stu-id="39d81-174">datetime</span></span></p></td>
<td><p><span data-ttu-id="39d81-175">ユーザーが会議サーバーを脱退した時刻。</span><span class="sxs-lookup"><span data-stu-id="39d81-175">Time the user left the conferencing server.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="39d81-176">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="39d81-176">


</div>

<span> </span>

</div>

</div>

</span></span></div>

