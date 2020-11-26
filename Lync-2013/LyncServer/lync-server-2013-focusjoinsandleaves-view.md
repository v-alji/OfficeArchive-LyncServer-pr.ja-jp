---
title: 'Lync Server 2013: FocusJoinsAndLeaves view'
description: 'Lync Server 2013: FocusJoinsAndLeaves ビュー。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: FocusJoinsAndLeaves view
ms:assetid: 226460ef-766f-4d61-80cb-f332b65a210d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687992(v=OCS.15)
ms:contentKeyID: 49733582
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c6f68c44461e378e9ebedce1305ee6b384a7a8a7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428110"
---
# <a name="focusjoinsandleaves-view-in-lync-server-2013"></a><span data-ttu-id="83b86-103">Lync Server 2013 での FocusJoinsAndLeaves の表示</span><span class="sxs-lookup"><span data-stu-id="83b86-103">FocusJoinsAndLeaves view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="83b86-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="83b86-104">

<span> </span></span></span>

<span data-ttu-id="83b86-105">_**最終更新日:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="83b86-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="83b86-106">FocusJoinsAndLeaves ビューには、1人の会議に参加するための情報が保存されます。</span><span class="sxs-lookup"><span data-stu-id="83b86-106">The FocusJoinsAndLeaves view stores information about join and leave information for one conference.</span></span> <span data-ttu-id="83b86-107">各会議は、ユーザーが会議に参加して退席するたびに書き込まれるレコードによって表示されます。</span><span class="sxs-lookup"><span data-stu-id="83b86-107">Each conference is represented in this view by a record written each time a user joins and leaves the conference.</span></span> <span data-ttu-id="83b86-108">このビューは、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="83b86-108">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="83b86-109">列</span><span class="sxs-lookup"><span data-stu-id="83b86-109">Column</span></span></th>
<th><span data-ttu-id="83b86-110">データ型</span><span class="sxs-lookup"><span data-stu-id="83b86-110">Data Type</span></span></th>
<th><span data-ttu-id="83b86-111">詳細</span><span class="sxs-lookup"><span data-stu-id="83b86-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="83b86-112"><strong>セッション Id</strong></span><span class="sxs-lookup"><span data-stu-id="83b86-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="83b86-113">datetime</span><span class="sxs-lookup"><span data-stu-id="83b86-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="83b86-114">会議インスタンスの時刻。</span><span class="sxs-lookup"><span data-stu-id="83b86-114">Time of conference instance.</span></span> <span data-ttu-id="83b86-115">電話会議インスタンスを一意に識別するために SessionIdSeq と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="83b86-115">Used in conjunction with SessionIdSeq to uniquely identify a conference instance.</span></span> <span data-ttu-id="83b86-116">詳細については、「 <a href="lync-server-2013-conferences-table.md">Lync Server 2013 での会議の表</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="83b86-116">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83b86-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="83b86-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="83b86-118">int</span><span class="sxs-lookup"><span data-stu-id="83b86-118">int</span></span></p></td>
<td><p><span data-ttu-id="83b86-119">会議インスタンスを識別する ID 番号。</span><span class="sxs-lookup"><span data-stu-id="83b86-119">ID number to identify the conference instance.</span></span> <span data-ttu-id="83b86-120">電話会議インスタンスを一意に識別するために SessionIdTime と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="83b86-120">Used in conjunction with SessionIdTime to uniquely identify a conference instance.</span></span> <span data-ttu-id="83b86-121">詳細については、「 <a href="lync-server-2013-conferences-table.md">Lync Server 2013 での会議の表</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="83b86-121">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83b86-122"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="83b86-122"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="83b86-123">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="83b86-123">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="83b86-124">会議の参加/退出情報がキャプチャされたユーザーの URI です。</span><span class="sxs-lookup"><span data-stu-id="83b86-124">URI of the user whose conference join/leave information was captured.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83b86-125"><strong>UserUriType</strong></span><span class="sxs-lookup"><span data-stu-id="83b86-125"><strong>UserUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="83b86-126">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="83b86-126">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="83b86-127">会議の参加/退出情報がキャプチャされたユーザーの URI の種類です。</span><span class="sxs-lookup"><span data-stu-id="83b86-127">Type of URI of the user whose conference join/leave information was captured.</span></span> <span data-ttu-id="83b86-128">詳細については、「 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 の UriTypes テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="83b86-128">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83b86-129"><strong>UserTenant</strong></span><span class="sxs-lookup"><span data-stu-id="83b86-129"><strong>UserTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="83b86-130">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="83b86-130">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="83b86-131">会議の参加/退出情報がキャプチャされたユーザーのテナントです。</span><span class="sxs-lookup"><span data-stu-id="83b86-131">Tenant of the user whose conference join/leave information was captured.</span></span> <span data-ttu-id="83b86-132">詳細については、「 <a href="lync-server-2013-tenants-table.md">Lync Server 2013 のテナントの一覧</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="83b86-132">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83b86-133"><strong>UserEndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="83b86-133"><strong>UserEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="83b86-134">長さ</span><span class="sxs-lookup"><span data-stu-id="83b86-134">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="83b86-135">会議の参加/退出情報がキャプチャされたユーザーを表す一意の識別子です。</span><span class="sxs-lookup"><span data-stu-id="83b86-135">Unique identifier of the user whose conference join/leave information was captured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83b86-136"><strong>UserClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="83b86-136"><strong>UserClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="83b86-137">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="83b86-137">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="83b86-138">会議の参加/退出情報がキャプチャされたユーザーが使用したクライアントのバージョン。</span><span class="sxs-lookup"><span data-stu-id="83b86-138">Version of client used by the user whose conference join/leave information was captured.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83b86-139"><strong>UserClientType</strong></span><span class="sxs-lookup"><span data-stu-id="83b86-139"><strong>UserClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="83b86-140">int</span><span class="sxs-lookup"><span data-stu-id="83b86-140">int</span></span></p></td>
<td><p><span data-ttu-id="83b86-141">電話会議の参加/退出情報がキャプチャされたユーザーによって使用されたクライアント。</span><span class="sxs-lookup"><span data-stu-id="83b86-141">Client used by the user whose conference join/leave information was captured.</span></span> <span data-ttu-id="83b86-142">詳細については、「 <a href="lync-server-2013-useragentdef-table.md">Lync Server 2013 の Useragentdef テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="83b86-142">See <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83b86-143"><strong>UserClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="83b86-143"><strong>UserClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="83b86-144">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="83b86-144">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="83b86-145">会議の参加/退出情報がキャプチャされたユーザーが使用したクライアントのカテゴリの名前です。</span><span class="sxs-lookup"><span data-stu-id="83b86-145">Name of the category of the client used by the user whose conference join/leave information was captured.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83b86-146"><strong>FocusUserInstance</strong></span><span class="sxs-lookup"><span data-stu-id="83b86-146"><strong>FocusUserInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="83b86-147">int</span><span class="sxs-lookup"><span data-stu-id="83b86-147">int</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83b86-148"><strong>IsuserInternal</strong></span><span class="sxs-lookup"><span data-stu-id="83b86-148"><strong>IsuserInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="83b86-149">bit</span><span class="sxs-lookup"><span data-stu-id="83b86-149">bit</span></span></p></td>
<td><p><span data-ttu-id="83b86-150">ユーザーが内部ユーザーかどうかを表すビット。</span><span class="sxs-lookup"><span data-stu-id="83b86-150">Bit that represents whether the user is an internal user or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83b86-151"><strong>/セッション Id</strong></span><span class="sxs-lookup"><span data-stu-id="83b86-151"><strong>DialogSessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="83b86-152">datetime</span><span class="sxs-lookup"><span data-stu-id="83b86-152">datetime</span></span></p></td>
<td><p><span data-ttu-id="83b86-153">セッション要求の時刻。</span><span class="sxs-lookup"><span data-stu-id="83b86-153">Time of session request.</span></span> <span data-ttu-id="83b86-154">セッションを一意に識別するために SessionIdSeq と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="83b86-154">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="83b86-155">詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="83b86-155">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83b86-156"><strong>"/セッション Id"</strong></span><span class="sxs-lookup"><span data-stu-id="83b86-156"><strong>DialogSessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="83b86-157">int</span><span class="sxs-lookup"><span data-stu-id="83b86-157">int</span></span></p></td>
<td><p><span data-ttu-id="83b86-158">ユーザーが複数のコンピューターまたはデバイスに同時にログオンしている場合は、UserInstance を使って、ユーザーとデバイスの組み合わせを一意に識別します。</span><span class="sxs-lookup"><span data-stu-id="83b86-158">If a user is logged on at multiple computers or devices at the same time, UserInstance is used to uniquely identify the user/device combination.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83b86-159"><strong>この Id</strong></span><span class="sxs-lookup"><span data-stu-id="83b86-159"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="83b86-160">varchar (775)</span><span class="sxs-lookup"><span data-stu-id="83b86-160">varchar(775)</span></span></p></td>
<td><p><span data-ttu-id="83b86-161">セッションの SIP ダイアログ ID。</span><span class="sxs-lookup"><span data-stu-id="83b86-161">SIP dialog ID of the session.</span></span> <span data-ttu-id="83b86-162">形式は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="83b86-162">The format is: dialog;from-tag;to-tag.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83b86-163"><strong>UserJoinTime</strong></span><span class="sxs-lookup"><span data-stu-id="83b86-163"><strong>UserJoinTime</strong></span></span></p></td>
<td><p><span data-ttu-id="83b86-164">datetime</span><span class="sxs-lookup"><span data-stu-id="83b86-164">datetime</span></span></p></td>
<td><p><span data-ttu-id="83b86-165">ユーザーが会議に参加した時刻。</span><span class="sxs-lookup"><span data-stu-id="83b86-165">Time that the user joined the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83b86-166"><strong>UserLeaveTime</strong></span><span class="sxs-lookup"><span data-stu-id="83b86-166"><strong>UserLeaveTime</strong></span></span></p></td>
<td><p><span data-ttu-id="83b86-167">datetime</span><span class="sxs-lookup"><span data-stu-id="83b86-167">datetime</span></span></p></td>
<td><p><span data-ttu-id="83b86-168">ユーザーが会議から退出した時刻。</span><span class="sxs-lookup"><span data-stu-id="83b86-168">Time that the user left the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83b86-169"><strong>UserRole</strong></span><span class="sxs-lookup"><span data-stu-id="83b86-169"><strong>UserRole</strong></span></span></p></td>
<td><p><span data-ttu-id="83b86-170">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="83b86-170">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="83b86-171">会議でのユーザーの役割 (発表者や出席者など)</span><span class="sxs-lookup"><span data-stu-id="83b86-171">User’s role in the conference, such as Presenter or Attendee.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="83b86-172">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="83b86-172">


</div>

<span> </span>

</div>

</div>

</span></span></div>

