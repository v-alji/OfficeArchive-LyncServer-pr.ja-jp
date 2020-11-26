---
title: 'Lync Server 2013: ConferenceSessionDetails テーブル'
description: 'Lync Server 2013: ConferenceSessionDetails テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ConferenceSessionDetails table
ms:assetid: 9eae6a54-69fd-4966-aa17-7ecee1297ad8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412741(v=OCS.15)
ms:contentKeyID: 48184925
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0d101eb1607e366ab814e60acaeee80820fe87c5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434418"
---
# <a name="conferencesessiondetails-table-in-lync-server-2013"></a><span data-ttu-id="ee9cb-103">Lync Server 2013 の ConferenceSessionDetails テーブル</span><span class="sxs-lookup"><span data-stu-id="ee9cb-103">ConferenceSessionDetails table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ee9cb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ee9cb-104">

<span> </span></span></span>

<span data-ttu-id="ee9cb-105">_**最終更新日:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="ee9cb-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="ee9cb-106">各レコードは1つの会議セッションを表します。これは、フォーカスのあるセッションまたは特定の会議サーバーのセッションのいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-106">Each record represents one conference session, which could be either the session with Focus or the session with a specific conferencing server.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ee9cb-107">列</span><span class="sxs-lookup"><span data-stu-id="ee9cb-107">Column</span></span></th>
<th><span data-ttu-id="ee9cb-108">データ型</span><span class="sxs-lookup"><span data-stu-id="ee9cb-108">Data Type</span></span></th>
<th><span data-ttu-id="ee9cb-109">キー/インデックス</span><span class="sxs-lookup"><span data-stu-id="ee9cb-109">Key/Index</span></span></th>
<th><span data-ttu-id="ee9cb-110">詳細</span><span class="sxs-lookup"><span data-stu-id="ee9cb-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee9cb-111"><strong>セッション Id</strong></span><span class="sxs-lookup"><span data-stu-id="ee9cb-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="ee9cb-112">Datetime</span><span class="sxs-lookup"><span data-stu-id="ee9cb-112">Datetime</span></span></p></td>
<td><p><span data-ttu-id="ee9cb-113">プライマリ、外部</span><span class="sxs-lookup"><span data-stu-id="ee9cb-113">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="ee9cb-114">セッション要求の時刻。電話会議セッションを一意に識別するために <strong>Sessionidseq</strong> と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-114">Time of session request; used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a conference session.</span></span> <span data-ttu-id="ee9cb-115">詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-115">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee9cb-116"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="ee9cb-116"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="ee9cb-117">int</span><span class="sxs-lookup"><span data-stu-id="ee9cb-117">int</span></span></p></td>
<td><p><span data-ttu-id="ee9cb-118">プライマリ、外部</span><span class="sxs-lookup"><span data-stu-id="ee9cb-118">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="ee9cb-119">セッションを識別する ID 番号。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-119">ID number to identify the session.</span></span> <span data-ttu-id="ee9cb-120">電話会議セッションを一意に識別するために <strong>Sessionidtime</strong> と組み合わせて使われます。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-120">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a conference session.</span></span> <span data-ttu-id="ee9cb-121">詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-121">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span> *</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee9cb-122"><strong>ConferenceUriId</strong></span><span class="sxs-lookup"><span data-stu-id="ee9cb-122"><strong>ConferenceUriId</strong></span></span></p></td>
<td><p><span data-ttu-id="ee9cb-123">int</span><span class="sxs-lookup"><span data-stu-id="ee9cb-123">int</span></span></p></td>
<td><p><span data-ttu-id="ee9cb-124">外部</span><span class="sxs-lookup"><span data-stu-id="ee9cb-124">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ee9cb-125">このセッションに関連する会議の URI にフォーカスを移動します。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-125">Focus conference URI related to this session.</span></span> <span data-ttu-id="ee9cb-126">詳細については、「 <a href="lync-server-2013-conferenceuris-table.md">Lync Server 2013 の ConferenceUris テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-126">See the <a href="lync-server-2013-conferenceuris-table.md">ConferenceUris table in Lync Server 2013</a> for more information.</span></span> <span data-ttu-id="ee9cb-127">この URI は、フォーカスベースの会議 URI です。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-127">This URI is a Focus-based conference URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee9cb-128"><strong>ConfInstance</strong></span><span class="sxs-lookup"><span data-stu-id="ee9cb-128"><strong>ConfInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="ee9cb-129">長さ</span><span class="sxs-lookup"><span data-stu-id="ee9cb-129">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee9cb-130">定期的な会議のインスタンスを区別する識別子。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-130">Identifier that differentiates between instances of recurring conferences.</span></span> <span data-ttu-id="ee9cb-131">各定期的な会議インスタンスの ConferenceURI は同じですが、異なる ConfInstance 値があります。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-131">Each recurring conference instance has the same ConferenceURI but a different ConfInstance value.</span></span></p>
<p><span data-ttu-id="ee9cb-132">このフィールドは、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-132">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee9cb-133"><strong>McuConferenceUriId</strong></span><span class="sxs-lookup"><span data-stu-id="ee9cb-133"><strong>McuConferenceUriId</strong></span></span></p></td>
<td><p><span data-ttu-id="ee9cb-134">int</span><span class="sxs-lookup"><span data-stu-id="ee9cb-134">int</span></span></p></td>
<td><p><span data-ttu-id="ee9cb-135">外部</span><span class="sxs-lookup"><span data-stu-id="ee9cb-135">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ee9cb-136">このセッションに関連する会議サーバーの会議 URI。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-136">Conferencing server conference URI related to this session.</span></span> <span data-ttu-id="ee9cb-137">詳細については、「 <a href="lync-server-2013-conferenceuris-table.md">Lync Server 2013 の ConferenceUris テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-137">See the <a href="lync-server-2013-conferenceuris-table.md">ConferenceUris table in Lync Server 2013</a> for more information.</span></span> <span data-ttu-id="ee9cb-138">この URI は、会議サーバーベースの会議 URI です。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-138">This URI is the conferencing server-based conference URI.</span></span> <span data-ttu-id="ee9cb-139">フォーカス会議セッションの場合、この列は null になります。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-139">For Focus conference sessions, this column will be null.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee9cb-140"><strong>UserId</strong></span><span class="sxs-lookup"><span data-stu-id="ee9cb-140"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="ee9cb-141">int</span><span class="sxs-lookup"><span data-stu-id="ee9cb-141">int</span></span></p></td>
<td><p><span data-ttu-id="ee9cb-142">外部</span><span class="sxs-lookup"><span data-stu-id="ee9cb-142">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ee9cb-143">会議セッションの1人のユーザーの ID です。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-143">ID of one user in the conference session.</span></span> <span data-ttu-id="ee9cb-144">詳細については、「 <a href="lync-server-2013-users-table.md">Lync Server 2013 のユーザーテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-144">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee9cb-145"><strong>UserEndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="ee9cb-145"><strong>UserEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="ee9cb-146">長さ</span><span class="sxs-lookup"><span data-stu-id="ee9cb-146">uniqueidentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee9cb-147">エンドポイントのインスタンスを識別するための GUID。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-147">A GUID to identify the instance of endpoint.</span></span> <span data-ttu-id="ee9cb-148">たとえば、あるユーザーが同じアカウントで異なるコンピューターにログオンしている場合、各コンピューターには別のエンドポイント ID があります。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-148">For example, if one user logs on to different machines with the same account, then each machine will have a different endpoint ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee9cb-149"><strong>OnBehalfOfId</strong></span><span class="sxs-lookup"><span data-stu-id="ee9cb-149"><strong>OnBehalfOfId</strong></span></span></p></td>
<td><p><span data-ttu-id="ee9cb-150">int</span><span class="sxs-lookup"><span data-stu-id="ee9cb-150">int</span></span></p></td>
<td><p><span data-ttu-id="ee9cb-151">外部</span><span class="sxs-lookup"><span data-stu-id="ee9cb-151">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ee9cb-152">発信者が代理としているユーザーの ID を示します。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-152">Indicates the ID of the user of who the caller is on behalf.</span></span> <span data-ttu-id="ee9cb-153">詳細については、「 <a href="lync-server-2013-users-table.md">Lync Server 2013 のユーザーテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-153">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee9cb-154"><strong>ReferredById</strong></span><span class="sxs-lookup"><span data-stu-id="ee9cb-154"><strong>ReferredById</strong></span></span></p></td>
<td><p><span data-ttu-id="ee9cb-155">int</span><span class="sxs-lookup"><span data-stu-id="ee9cb-155">int</span></span></p></td>
<td><p><span data-ttu-id="ee9cb-156">外部</span><span class="sxs-lookup"><span data-stu-id="ee9cb-156">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ee9cb-157">通話を参照するユーザーの ID です。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-157">ID of the user by who the call is referred.</span></span> <span data-ttu-id="ee9cb-158">詳細については、「 <a href="lync-server-2013-users-table.md">Lync Server 2013 のユーザーテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-158">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee9cb-159"><strong>UserClientVersionId</strong></span><span class="sxs-lookup"><span data-stu-id="ee9cb-159"><strong>UserClientVersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="ee9cb-160">int</span><span class="sxs-lookup"><span data-stu-id="ee9cb-160">int</span></span></p></td>
<td><p><span data-ttu-id="ee9cb-161">外部</span><span class="sxs-lookup"><span data-stu-id="ee9cb-161">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ee9cb-162">電話会議ユーザーが使用したクライアントバージョン。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-162">Client version used by the conference user.</span></span> <span data-ttu-id="ee9cb-163">詳細については、「 <a href="lync-server-2013-clientversions-table.md">Lync Server 2013 の Clientversions の表</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-163">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee9cb-164"><strong>ConfClientVersionId</strong></span><span class="sxs-lookup"><span data-stu-id="ee9cb-164"><strong>ConfClientVersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="ee9cb-165">int</span><span class="sxs-lookup"><span data-stu-id="ee9cb-165">int</span></span></p></td>
<td><p><span data-ttu-id="ee9cb-166">外部</span><span class="sxs-lookup"><span data-stu-id="ee9cb-166">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ee9cb-167">会議サーバーで使用されるクライアントのバージョンです。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-167">Client version used by the conference server.</span></span> <span data-ttu-id="ee9cb-168">詳細については、「 <a href="lync-server-2013-clientversions-table.md">Lync Server 2013 の Clientversions の表</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-168">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee9cb-169"><strong>Edialogidtime の置き換え</strong></span><span class="sxs-lookup"><span data-stu-id="ee9cb-169"><strong>ReplaceDialogIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="ee9cb-170">datetime</span><span class="sxs-lookup"><span data-stu-id="ee9cb-170">datetime</span></span></p></td>
<td><p><span data-ttu-id="ee9cb-171">外部</span><span class="sxs-lookup"><span data-stu-id="ee9cb-171">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ee9cb-172">現在のセッションによって置き換えられたダイアログを識別する ID 番号。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-172">ID number to identify the dialog which was replaced by current session.</span></span> <span data-ttu-id="ee9cb-173">詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-173">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee9cb-174"><strong>Edialogidseq の置き換え</strong></span><span class="sxs-lookup"><span data-stu-id="ee9cb-174"><strong>ReplaceDialogIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="ee9cb-175">int</span><span class="sxs-lookup"><span data-stu-id="ee9cb-175">int</span></span></p></td>
<td><p><span data-ttu-id="ee9cb-176">外部</span><span class="sxs-lookup"><span data-stu-id="ee9cb-176">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ee9cb-177">セッションを識別する ID 番号。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-177">ID number to identify the session.</span></span> <span data-ttu-id="ee9cb-178">このセッションによって置き換えられるセッションを一意に識別するために、 <strong>代替の操作と組み合わせ</strong> て使います。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-178">Used in conjunction with <strong>ReplacesDialogIdTime</strong> to uniquely identify a session that is replaced by this session.</span></span> <span data-ttu-id="ee9cb-179">詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-179">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee9cb-180"><strong>IsStartedByConfServer</strong></span><span class="sxs-lookup"><span data-stu-id="ee9cb-180"><strong>IsStartedByConfServer</strong></span></span></p></td>
<td><p><span data-ttu-id="ee9cb-181">bit</span><span class="sxs-lookup"><span data-stu-id="ee9cb-181">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee9cb-182">セッションが会議サーバーによって開始されたかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-182">Indicates if the session started by the conferencing Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee9cb-183"><strong>IsEndedByConfServer</strong></span><span class="sxs-lookup"><span data-stu-id="ee9cb-183"><strong>IsEndedByConfServer</strong></span></span></p></td>
<td><p><span data-ttu-id="ee9cb-184">bit</span><span class="sxs-lookup"><span data-stu-id="ee9cb-184">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee9cb-185">会議サーバーによってセッションが終了したかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-185">Indicates if the session ended by the conferencing server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee9cb-186"><strong>IsUserInternal</strong></span><span class="sxs-lookup"><span data-stu-id="ee9cb-186"><strong>IsUserInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="ee9cb-187">bit</span><span class="sxs-lookup"><span data-stu-id="ee9cb-187">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee9cb-188">ユーザーが内部からログオンしているかどうか。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-188">Whether user is logged on from internal or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee9cb-189"><strong>返信</strong></span><span class="sxs-lookup"><span data-stu-id="ee9cb-189"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="ee9cb-190">int</span><span class="sxs-lookup"><span data-stu-id="ee9cb-190">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee9cb-191">セッションの招待状へのセッション開始プロトコル (SIP) 応答コード。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-191">Session Initiation Protocol (SIP) response code to the session invitation.</span></span> <span data-ttu-id="ee9cb-192">通常、このフィールドは、セッションの最初の INVITE メッセージから生成されたデータによって設定されます。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-192">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="ee9cb-193">招待メッセージがない場合は、最初に関連する SIP メッセージ (BYE、キャンセル、メッセージ、または情報) の日付と時刻がフィールドに設定されています。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-193">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee9cb-194"><strong>DiagnosticId</strong></span><span class="sxs-lookup"><span data-stu-id="ee9cb-194"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="ee9cb-195">int</span><span class="sxs-lookup"><span data-stu-id="ee9cb-195">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee9cb-196">SIP ヘッダーからキャプチャされた診断 ID。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-196">Diagnostic ID captured from SIP header.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee9cb-197"><strong>ServerId</strong></span><span class="sxs-lookup"><span data-stu-id="ee9cb-197"><strong>ServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="ee9cb-198">int</span><span class="sxs-lookup"><span data-stu-id="ee9cb-198">int</span></span></p></td>
<td><p><span data-ttu-id="ee9cb-199">外部</span><span class="sxs-lookup"><span data-stu-id="ee9cb-199">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ee9cb-200">このセッションで使用するフロントエンドサーバーの ID です。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-200">ID of the front-end server used for this session.</span></span> <span data-ttu-id="ee9cb-201">詳細については、「 <a href="lync-server-2013-servers-table.md">Lync Server 2013 のサーバーの表</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-201">See the <a href="lync-server-2013-servers-table.md">Servers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee9cb-202"><strong>PoolId</strong></span><span class="sxs-lookup"><span data-stu-id="ee9cb-202"><strong>PoolId</strong></span></span></p></td>
<td><p><span data-ttu-id="ee9cb-203">int</span><span class="sxs-lookup"><span data-stu-id="ee9cb-203">int</span></span></p></td>
<td><p><span data-ttu-id="ee9cb-204">外部</span><span class="sxs-lookup"><span data-stu-id="ee9cb-204">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ee9cb-205">セッションがキャプチャされたプールの ID です。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-205">ID of the pool in which the session was captured.</span></span> <span data-ttu-id="ee9cb-206">詳細については、「 <a href="lync-server-2013-pools-table.md">Lync Server 2013 のプールテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-206">See the <a href="lync-server-2013-pools-table.md">Pools table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee9cb-207"><strong>MediationServerId</strong></span><span class="sxs-lookup"><span data-stu-id="ee9cb-207"><strong>MediationServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="ee9cb-208">int</span><span class="sxs-lookup"><span data-stu-id="ee9cb-208">int</span></span></p></td>
<td><p><span data-ttu-id="ee9cb-209">外部</span><span class="sxs-lookup"><span data-stu-id="ee9cb-209">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ee9cb-210">通話が使用している仲介サーバー。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-210">The Mediation Server the call is using.</span></span> <span data-ttu-id="ee9cb-211">詳細については、「 <a href="lync-server-2013-mediationservers-table.md">Lync Server 2013 の Mediationservers の表</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-211">See the <a href="lync-server-2013-mediationservers-table.md">MediationServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee9cb-212"><strong>GatewayId</strong></span><span class="sxs-lookup"><span data-stu-id="ee9cb-212"><strong>GatewayId</strong></span></span></p></td>
<td><p><span data-ttu-id="ee9cb-213">int</span><span class="sxs-lookup"><span data-stu-id="ee9cb-213">int</span></span></p></td>
<td><p><span data-ttu-id="ee9cb-214">外部</span><span class="sxs-lookup"><span data-stu-id="ee9cb-214">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ee9cb-215">通話が使用しているゲートウェイ。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-215">The gateway the call is using.</span></span> <span data-ttu-id="ee9cb-216">詳細については、「 <a href="lync-server-2013-gateways-table.md">Lync Server 2013 のゲートウェイテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-216">See the <a href="lync-server-2013-gateways-table.md">Gateways table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee9cb-217"><strong>EdgeServerId</strong></span><span class="sxs-lookup"><span data-stu-id="ee9cb-217"><strong>EdgeServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="ee9cb-218">int</span><span class="sxs-lookup"><span data-stu-id="ee9cb-218">int</span></span></p></td>
<td><p><span data-ttu-id="ee9cb-219">外部</span><span class="sxs-lookup"><span data-stu-id="ee9cb-219">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ee9cb-220">通話が使用しているエッジサーバー。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-220">The Edge Server the call is using.</span></span> <span data-ttu-id="ee9cb-221">詳細については、「 <a href="lync-server-2013-edgeservers-table.md">Lync Server 2013 の EdgeServers テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-221">See the <a href="lync-server-2013-edgeservers-table.md">EdgeServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee9cb-222"><strong>ContentTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="ee9cb-222"><strong>ContentTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="ee9cb-223">int</span><span class="sxs-lookup"><span data-stu-id="ee9cb-223">int</span></span></p></td>
<td><p><span data-ttu-id="ee9cb-224">外部</span><span class="sxs-lookup"><span data-stu-id="ee9cb-224">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ee9cb-225">セッションで使用されるコンテンツタイプ。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-225">Content type used in the session.</span></span> <span data-ttu-id="ee9cb-226">詳細については、「 <a href="lync-server-2013-contenttypes-table.md">Lync Server 2013 の ContentTypes テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-226">See the <a href="lync-server-2013-contenttypes-table.md">ContentTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee9cb-227"><strong>InviteTime</strong></span><span class="sxs-lookup"><span data-stu-id="ee9cb-227"><strong>InviteTime</strong></span></span></p></td>
<td><p><span data-ttu-id="ee9cb-228">datetime</span><span class="sxs-lookup"><span data-stu-id="ee9cb-228">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee9cb-229">最初の招待要求の時刻。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-229">The time of the first INVITE request.</span></span> <span data-ttu-id="ee9cb-230">通常、このフィールドは、セッションの最初の INVITE メッセージから生成されたデータによって設定されます。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-230">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="ee9cb-231">招待メッセージがない場合は、最初に関連する SIP メッセージ (BYE、キャンセル、メッセージ、または情報) の日付と時刻がフィールドに設定されています。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-231">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee9cb-232"><strong>ResponseTime</strong></span><span class="sxs-lookup"><span data-stu-id="ee9cb-232"><strong>ResponseTime</strong></span></span></p></td>
<td><p><span data-ttu-id="ee9cb-233">datetime</span><span class="sxs-lookup"><span data-stu-id="ee9cb-233">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee9cb-234">最初の SIP 応答の時刻。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-234">Time of the first SIP RESPONSE.</span></span> <span data-ttu-id="ee9cb-235">通常、このフィールドは、セッションの最初の INVITE メッセージから生成されたデータによって設定されます。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-235">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="ee9cb-236">招待メッセージがない場合は、最初に関連する SIP メッセージ (BYE、キャンセル、メッセージ、または情報) の日付と時刻がフィールドに設定されています。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-236">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee9cb-237"><strong>セッション終了時刻</strong></span><span class="sxs-lookup"><span data-stu-id="ee9cb-237"><strong>SessionEndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="ee9cb-238">datetime</span><span class="sxs-lookup"><span data-stu-id="ee9cb-238">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee9cb-239">セッションが終了した時刻。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-239">The time when the session is ended.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee9cb-240"><strong>UriTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="ee9cb-240"><strong>UriTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="ee9cb-241">tinyint</span><span class="sxs-lookup"><span data-stu-id="ee9cb-241">tinyint</span></span></p></td>
<td><p><span data-ttu-id="ee9cb-242">外部</span><span class="sxs-lookup"><span data-stu-id="ee9cb-242">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ee9cb-243"><a href="lync-server-2013-uritypes-table.md">Lync Server 2013 の UriTypes テーブル</a>の MCU URI の種類の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-243">Contains the MCU URI type value from the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a>.</span></span> <span data-ttu-id="ee9cb-244">このフィールドは、クエリのパフォーマンスを向上させるために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-244">This field is used for improving query performance.</span></span></p>
<p><span data-ttu-id="ee9cb-245">このフィールドは、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-245">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee9cb-246"><strong>UserFlag</strong></span><span class="sxs-lookup"><span data-stu-id="ee9cb-246"><strong>UserFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="ee9cb-247">smallint</span><span class="sxs-lookup"><span data-stu-id="ee9cb-247">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee9cb-248">ユーザー属性を示すビットセット。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-248">A bit set that indicates the user attributes.</span></span> <span data-ttu-id="ee9cb-249">次の属性定義が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-249">The following attribute definitions are listed:</span></span></p>
<ul>
<li><p><span data-ttu-id="ee9cb-250">デスクトップ電話と統合-1</span><span class="sxs-lookup"><span data-stu-id="ee9cb-250">Integrated with desktop phone - 1</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee9cb-251"><strong>CallFlag</strong></span><span class="sxs-lookup"><span data-stu-id="ee9cb-251"><strong>CallFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="ee9cb-252">smallint</span><span class="sxs-lookup"><span data-stu-id="ee9cb-252">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ee9cb-253">呼び出し属性を示すビットセット。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-253">A bit set that indicates the call attributes.</span></span> <span data-ttu-id="ee9cb-254">次の属性定義が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-254">The following attribute definitions are listed:</span></span></p>
<ul>
<li><p><span data-ttu-id="ee9cb-255">セッションを再試行しました-1</span><span class="sxs-lookup"><span data-stu-id="ee9cb-255">Retried Session - 1</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ee9cb-256">\* ほとんどのセッションでは、SessionIdSeq の値は1になります。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-256">\* For most sessions, SessionIdSeq will have the value of 1.</span></span> <span data-ttu-id="ee9cb-257">複数のセッションが同時に開始された場合は、1つのセッションの SessionIdSeq は1、それ以外の場合は2となります。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-257">If multiple sessions start at exactly the same time, the SessionIdSeq for one will be 1, for another will be 2, and so on.</span></span>

<span data-ttu-id="ee9cb-258"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ee9cb-258"></div>

<span> </span>

</div>

</div>

</span></span></div>

