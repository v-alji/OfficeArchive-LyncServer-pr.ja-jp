---
title: 'Lync Server 2013: ConferenceSessionDetails view'
description: 'Lync Server 2013: ConferenceSessionDetails ビュー。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ConferenceSessionDetails view
ms:assetid: 5858c84d-baed-421d-ad1d-3726e150e256
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688066(v=OCS.15)
ms:contentKeyID: 49733660
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d1c62f020413efecdbc0f909618256ccc7308d4f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434397"
---
# <a name="conferencesessiondetails-view-in-lync-server-2013"></a><span data-ttu-id="11fca-103">Lync Server 2013 での ConferenceSessionDetails の表示</span><span class="sxs-lookup"><span data-stu-id="11fca-103">ConferenceSessionDetails view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="11fca-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="11fca-104">

<span> </span></span></span>

<span data-ttu-id="11fca-105">_**最終更新日:** 2012-11-12_</span><span class="sxs-lookup"><span data-stu-id="11fca-105">_**Topic Last Modified:** 2012-11-12_</span></span>

<span data-ttu-id="11fca-106">ConferenceSessionDetails ビューには、マルチパーティセッションに関する情報が格納されます。</span><span class="sxs-lookup"><span data-stu-id="11fca-106">The ConferenceSessionDetails view stores information about multiparty sessions.</span></span> <span data-ttu-id="11fca-107">各レコードは1つの会議セッションを表します。これは、フォーカスのあるセッションまたは特定の会議サーバーのセッションのいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="11fca-107">Each record represents one conference session, which could be either the session with Focus or the session with a specific conferencing server.</span></span> <span data-ttu-id="11fca-108">このビューは、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="11fca-108">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11fca-109">列</span><span class="sxs-lookup"><span data-stu-id="11fca-109">Column</span></span></th>
<th><span data-ttu-id="11fca-110">データ型</span><span class="sxs-lookup"><span data-stu-id="11fca-110">Data Type</span></span></th>
<th><span data-ttu-id="11fca-111">詳細</span><span class="sxs-lookup"><span data-stu-id="11fca-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="11fca-112"><strong>セッション Id</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-113">datetime</span><span class="sxs-lookup"><span data-stu-id="11fca-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="11fca-114">セッション要求の時刻。</span><span class="sxs-lookup"><span data-stu-id="11fca-114">Time of session request.</span></span> <span data-ttu-id="11fca-115">セッションを一意に識別するために SessionIdSeq と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="11fca-115">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="11fca-116">詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="11fca-116">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11fca-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-118">int</span><span class="sxs-lookup"><span data-stu-id="11fca-118">int</span></span></p></td>
<td><p><span data-ttu-id="11fca-119">セッションを識別する ID 番号。</span><span class="sxs-lookup"><span data-stu-id="11fca-119">ID number to identify the session.</span></span> <span data-ttu-id="11fca-120">セッションを一意に識別するために SessionIdTime と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="11fca-120">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="11fca-121">詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="11fca-121">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11fca-122"><strong>InviteTime</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-122"><strong>InviteTime</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-123">datetime</span><span class="sxs-lookup"><span data-stu-id="11fca-123">datetime</span></span></p></td>
<td><p><span data-ttu-id="11fca-124">最初の招待要求の時刻。</span><span class="sxs-lookup"><span data-stu-id="11fca-124">Time of the first INVITE request.</span></span> <span data-ttu-id="11fca-125">通常、このフィールドは、セッションの最初の INVITE メッセージから生成されたデータによって設定されます。</span><span class="sxs-lookup"><span data-stu-id="11fca-125">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="11fca-126">招待メッセージがない場合は、最初に関連する SIP メッセージ (BYE、キャンセル、メッセージ、または情報) の日付と時刻がフィールドに設定されています。</span><span class="sxs-lookup"><span data-stu-id="11fca-126">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11fca-127"><strong>ConferenceUri</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-127"><strong>ConferenceUri</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-128">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="11fca-128">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="11fca-129">会議の URI。</span><span class="sxs-lookup"><span data-stu-id="11fca-129">URI of the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11fca-130"><strong>ConferenceUriType</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-130"><strong>ConferenceUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-131">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="11fca-131">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="11fca-132">電話会議 URI の種類。</span><span class="sxs-lookup"><span data-stu-id="11fca-132">Type of conference URI.</span></span> <span data-ttu-id="11fca-133">詳細については、「 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 の UriTypes テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="11fca-133">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11fca-134"><strong>ConfInstance</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-134"><strong>ConfInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-135">長さ</span><span class="sxs-lookup"><span data-stu-id="11fca-135">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="11fca-136">定期的な会議のインスタンスを区別する識別子。</span><span class="sxs-lookup"><span data-stu-id="11fca-136">Identifier that differentiates between instances of recurring conferences.</span></span> <span data-ttu-id="11fca-137">各定期的な会議インスタンスの ConferenceURI は同じですが、異なる ConfInstance 値があります。</span><span class="sxs-lookup"><span data-stu-id="11fca-137">Each recurring conference instance has the same ConferenceURI but a different ConfInstance value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11fca-138"><strong>McuConferenceUri</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-138"><strong>McuConferenceUri</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-139">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="11fca-139">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="11fca-140">会議サーバーの URI。</span><span class="sxs-lookup"><span data-stu-id="11fca-140">URI of the conferencing server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11fca-141"><strong>McuConferenceUriType</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-141"><strong>McuConferenceUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-142">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="11fca-142">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="11fca-143">会議サーバーの URI の種類。</span><span class="sxs-lookup"><span data-stu-id="11fca-143">Type of conferencing server URI.</span></span> <span data-ttu-id="11fca-144">詳細については、「 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 の UriTypes テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="11fca-144">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11fca-145"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-145"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-146">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="11fca-146">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="11fca-147">セッションに関連するユーザーの URI。</span><span class="sxs-lookup"><span data-stu-id="11fca-147">URI of the user involved in the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11fca-148"><strong>UserUriType</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-148"><strong>UserUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-149">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="11fca-149">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="11fca-150">セッションの一部だったユーザーの URI の種類。</span><span class="sxs-lookup"><span data-stu-id="11fca-150">Type of URI of the user whose was part of the session.</span></span> <span data-ttu-id="11fca-151">詳細については、「 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 の UriTypes テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="11fca-151">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11fca-152"><strong>UserTenant</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-152"><strong>UserTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-153">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="11fca-153">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="11fca-154">セッションの一部だったユーザーのテナント。</span><span class="sxs-lookup"><span data-stu-id="11fca-154">Tenant of the user whose was part of the session.</span></span> <span data-ttu-id="11fca-155">詳細については、「 <a href="lync-server-2013-tenants-table.md">Lync Server 2013 のテナントの一覧</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="11fca-155">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11fca-156"><strong>UserEndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-156"><strong>UserEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-157">長さ</span><span class="sxs-lookup"><span data-stu-id="11fca-157">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="11fca-158">セッションの一部だったユーザーの一意の識別子。</span><span class="sxs-lookup"><span data-stu-id="11fca-158">Unique identifier of the user whose was part of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11fca-159"><strong>EndTime</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-159"><strong>EndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-160">datetime</span><span class="sxs-lookup"><span data-stu-id="11fca-160">datetime</span></span></p></td>
<td><p><span data-ttu-id="11fca-161">セッションの終了時刻。</span><span class="sxs-lookup"><span data-stu-id="11fca-161">End time of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11fca-162"><strong>ConferenceClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-162"><strong>ConferenceClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-163">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="11fca-163">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="11fca-164">会議サーバーのバージョン。</span><span class="sxs-lookup"><span data-stu-id="11fca-164">Version of conference server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11fca-165"><strong>ConferenceClientType</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-165"><strong>ConferenceClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-166">int</span><span class="sxs-lookup"><span data-stu-id="11fca-166">int</span></span></p></td>
<td><p><span data-ttu-id="11fca-167">会議サーバーの種類。</span><span class="sxs-lookup"><span data-stu-id="11fca-167">Type of conference server.</span></span> <span data-ttu-id="11fca-168">詳細については、「 <a href="lync-server-2013-useragentdef-table.md">Lync Server 2013 の Useragentdef テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="11fca-168">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11fca-169"><strong>ConferenceCategory</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-169"><strong>ConferenceCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-170">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="11fca-170">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="11fca-171">会議サーバーのカテゴリ。</span><span class="sxs-lookup"><span data-stu-id="11fca-171">Conference server category.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11fca-172"><strong>UserClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-172"><strong>UserClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-173">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="11fca-173">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="11fca-174">セッションに参加したユーザーによって使用されたクライアントのバージョン。</span><span class="sxs-lookup"><span data-stu-id="11fca-174">Version of client used by the user who participated in the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11fca-175"><strong>UserClientType</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-175"><strong>UserClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-176">int</span><span class="sxs-lookup"><span data-stu-id="11fca-176">int</span></span></p></td>
<td><p><span data-ttu-id="11fca-177">セッションに参加したユーザーによって使用されたクライアント。</span><span class="sxs-lookup"><span data-stu-id="11fca-177">Client used by the user who participated in the session.</span></span> <span data-ttu-id="11fca-178">詳細については、「 <a href="lync-server-2013-useragentdef-table.md">Lync Server 2013 の Useragentdef テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="11fca-178">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11fca-179"><strong>UserClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-179"><strong>UserClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-180">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="11fca-180">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="11fca-181">セッションの一部だったユーザーによって使用されたクライアントのカテゴリの名前です。</span><span class="sxs-lookup"><span data-stu-id="11fca-181">Name of the category of the client used by the user who was part of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11fca-182"><strong>OnBehalfOfUri</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-182"><strong>OnBehalfOfUri</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-183">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="11fca-183">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="11fca-184">セッションが開始されたユーザーの URI。</span><span class="sxs-lookup"><span data-stu-id="11fca-184">URI of the user on whose behalf the session was started.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11fca-185"><strong>OnBehalfOfUriType</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-185"><strong>OnBehalfOfUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-186">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="11fca-186">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="11fca-187">セッションが開始されたユーザーの URI の種類。</span><span class="sxs-lookup"><span data-stu-id="11fca-187">Type of URI of the user on whose behalf the session was started.</span></span> <span data-ttu-id="11fca-188">詳細については、「 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 の UriTypes テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="11fca-188">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11fca-189"><strong>OnBehalfOfTenant</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-189"><strong>OnBehalfOfTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-190">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="11fca-190">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="11fca-191">セッションを開始したユーザーのテナント。</span><span class="sxs-lookup"><span data-stu-id="11fca-191">Tenant of the user whose on behalf the session was started.</span></span> <span data-ttu-id="11fca-192">詳細については、「 <a href="lync-server-2013-tenants-table.md">Lync Server 2013 のテナントの一覧</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="11fca-192">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11fca-193"><strong>△この Uri</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-193"><strong>ReferredByUri</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-194">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="11fca-194">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="11fca-195">セッションを参照したユーザーの URI。</span><span class="sxs-lookup"><span data-stu-id="11fca-195">URI of the user who referred the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11fca-196"><strong>ベンチャー Redbyuritん</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-196"><strong>ReferredByUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-197">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="11fca-197">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="11fca-198">セッションを参照したユーザーの URI の種類。</span><span class="sxs-lookup"><span data-stu-id="11fca-198">Type of URI of the user who referred the session.</span></span> <span data-ttu-id="11fca-199">詳細については、「 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 の UriTypes テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="11fca-199">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11fca-200"><strong>、Uritbyuritenant</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-200"><strong>ReferredByUriTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-201">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="11fca-201">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="11fca-202">セッションを参照したユーザーのテナント。</span><span class="sxs-lookup"><span data-stu-id="11fca-202">Tenant of the user who referred the session.</span></span> <span data-ttu-id="11fca-203">詳細については、「 <a href="lync-server-2013-tenants-table.md">Lync Server 2013 のテナントの一覧</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="11fca-203">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11fca-204"><strong>この Id</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-204"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-205">varstring (775)</span><span class="sxs-lookup"><span data-stu-id="11fca-205">varstring(775)</span></span></p></td>
<td><p><span data-ttu-id="11fca-206">SIP ダイアログ ID。</span><span class="sxs-lookup"><span data-stu-id="11fca-206">SIP dialog ID.</span></span> <span data-ttu-id="11fca-207">書式は</span><span class="sxs-lookup"><span data-stu-id="11fca-207">The format is</span></span></p>
<p><span data-ttu-id="11fca-208">:d ialog; from タグ; to タグ</span><span class="sxs-lookup"><span data-stu-id="11fca-208">:dialog;from-tag;to-tag</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11fca-209"><strong>Edialogidtime の置き換え</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-209"><strong>ReplaceDialogIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-210">datetime</span><span class="sxs-lookup"><span data-stu-id="11fca-210">datetime</span></span></p></td>
<td><p><span data-ttu-id="11fca-211">現在のセッションによって置き換えられたダイアログを識別する ID 番号。</span><span class="sxs-lookup"><span data-stu-id="11fca-211">ID number to identify the dialog which was replaced by current session.</span></span> <span data-ttu-id="11fca-212">詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="11fca-212">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11fca-213"><strong>Edialogidseq の置き換え</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-213"><strong>ReplaceDialogIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-214">int</span><span class="sxs-lookup"><span data-stu-id="11fca-214">int</span></span></p></td>
<td><p><span data-ttu-id="11fca-215">セッションを識別する ID 番号。</span><span class="sxs-lookup"><span data-stu-id="11fca-215">ID number to identify the session.</span></span> <span data-ttu-id="11fca-216">このセッションによって置き換えられるセッションを一意に識別するには、置換 Edialogidtime と組み合わせて使います。</span><span class="sxs-lookup"><span data-stu-id="11fca-216">Used in conjunction with ReplaceDialogIdTime to uniquely identify a session that is replaced by this session.</span></span> <span data-ttu-id="11fca-217">詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="11fca-217">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11fca-218"><strong>置換の方法 Id</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-218"><strong>ReplacesDialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-219">varchar (775)</span><span class="sxs-lookup"><span data-stu-id="11fca-219">varchar(775)</span></span></p></td>
<td><p><span data-ttu-id="11fca-220">SIP ダイアログ ID によってセッションが置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="11fca-220">SIP dialog ID the session replaces.</span></span> <span data-ttu-id="11fca-221">の形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="11fca-221">The format of the is:</span></span></p>
<p><span data-ttu-id="11fca-222">ダイアログ; 開始タグからタグへ</span><span class="sxs-lookup"><span data-stu-id="11fca-222">dialog;from-tag;to-tag</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11fca-223"><strong>IsStartedByConfServer</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-223"><strong>IsStartedByConfServer</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-224">bit</span><span class="sxs-lookup"><span data-stu-id="11fca-224">bit</span></span></p></td>
<td><p><span data-ttu-id="11fca-225">セッションが会議サーバーによって開始されたかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="11fca-225">Indicates whether the session was started by the conferencing server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11fca-226"><strong>IsEndedByConfServer</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-226"><strong>IsEndedByConfServer</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-227">bit</span><span class="sxs-lookup"><span data-stu-id="11fca-227">bit</span></span></p></td>
<td><p><span data-ttu-id="11fca-228">会議サーバーによってセッションが終了したかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="11fca-228">Indicates whether the session was ended by the conferencing server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11fca-229"><strong>IsUserInternal</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-229"><strong>IsUserInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-230">bit</span><span class="sxs-lookup"><span data-stu-id="11fca-230">bit</span></span></p></td>
<td><p><span data-ttu-id="11fca-231">ユーザーが内部ネットワークからログオンしているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="11fca-231">Indicates whether the user logged on from the internal network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11fca-232"><strong>ResponseTime</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-232"><strong>ResponseTime</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-233">datetime</span><span class="sxs-lookup"><span data-stu-id="11fca-233">datetime</span></span></p></td>
<td><p><span data-ttu-id="11fca-234">最初の招待メッセージに対する返信の時刻。</span><span class="sxs-lookup"><span data-stu-id="11fca-234">Time of the response to the first INVITE message.</span></span> <span data-ttu-id="11fca-235">通常、このフィールドは、セッションの最初の INVITE メッセージから生成されたデータによって設定されます。</span><span class="sxs-lookup"><span data-stu-id="11fca-235">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="11fca-236">招待メッセージがない場合は、最初に関連する SIP メッセージ (BYE、キャンセル、メッセージ、または情報) の日付と時刻がフィールドに設定されています。</span><span class="sxs-lookup"><span data-stu-id="11fca-236">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11fca-237"><strong>返信</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-237"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-238">int</span><span class="sxs-lookup"><span data-stu-id="11fca-238">int</span></span></p></td>
<td><p><span data-ttu-id="11fca-239">セッション招待状への SIP 応答コード。</span><span class="sxs-lookup"><span data-stu-id="11fca-239">SIP response code to the session invitation.</span></span> <span data-ttu-id="11fca-240">通常、このフィールドは、セッションの最初の INVITE メッセージから生成されたデータによって設定されます。</span><span class="sxs-lookup"><span data-stu-id="11fca-240">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="11fca-241">招待メッセージがない場合は、最初に関連する SIP メッセージ (BYE、キャンセル、メッセージ、または情報) の日付と時刻がフィールドに設定されています。</span><span class="sxs-lookup"><span data-stu-id="11fca-241">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11fca-242"><strong>DiagnosticId</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-242"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-243">int</span><span class="sxs-lookup"><span data-stu-id="11fca-243">int</span></span></p></td>
<td><p><span data-ttu-id="11fca-244">セッション SIP ヘッダーからキャプチャされた診断 ID。</span><span class="sxs-lookup"><span data-stu-id="11fca-244">Diagnostic ID captured from session SIP headers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11fca-245"><strong>ContentType</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-245"><strong>ContentType</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-246">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="11fca-246">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="11fca-247">セッションのコンテンツタイプ。</span><span class="sxs-lookup"><span data-stu-id="11fca-247">Content type for the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11fca-248"><strong>FrontEnd</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-248"><strong>FrontEnd</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-249">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="11fca-249">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="11fca-250">セッションのデータをキャプチャしたフロントエンドサーバーの FQDN。</span><span class="sxs-lookup"><span data-stu-id="11fca-250">FQDN of the Front End server that captured the data for the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11fca-251"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-251"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-252">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="11fca-252">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="11fca-253">セッションのデータをキャプチャしたプールの FQDN。</span><span class="sxs-lookup"><span data-stu-id="11fca-253">FQDN of the pool that captured the data for the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11fca-254"><strong>MediationServer</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-254"><strong>MediationServer</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-255">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="11fca-255">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="11fca-256">セッションに参加したユーザーによって使用される仲介サーバー。</span><span class="sxs-lookup"><span data-stu-id="11fca-256">Mediation Server used by the user who participated in the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11fca-257"><strong>ゲートウェイ</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-257"><strong>Gateway</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-258">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="11fca-258">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="11fca-259">セッションに参加したユーザーが使用したゲートウェイ。</span><span class="sxs-lookup"><span data-stu-id="11fca-259">Gateway used by the user who participated the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11fca-260"><strong>EdgeServer</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-260"><strong>EdgeServer</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-261">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="11fca-261">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="11fca-262">セッションに参加したユーザーによって使用されたエッジサーバーの FQDN。</span><span class="sxs-lookup"><span data-stu-id="11fca-262">FQDN of the Edge server used by the user who participated in the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11fca-263"><strong>UserFlag</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-263"><strong>UserFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-264">smallint</span><span class="sxs-lookup"><span data-stu-id="11fca-264">smallint</span></span></p></td>
<td><p><span data-ttu-id="11fca-265">セッションに参加したユーザーの属性を示します。</span><span class="sxs-lookup"><span data-stu-id="11fca-265">Indicates the attributes of the user who participated in the session.</span></span> <span data-ttu-id="11fca-266">次の属性定義を使用できます。</span><span class="sxs-lookup"><span data-stu-id="11fca-266">The following attribute definitions allowed:</span></span></p>
<p><span data-ttu-id="11fca-267">0x01-デスクトップ電話と統合</span><span class="sxs-lookup"><span data-stu-id="11fca-267">0x01 - Integrated with desktop phone</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11fca-268"><strong>CallFlag</strong></span><span class="sxs-lookup"><span data-stu-id="11fca-268"><strong>CallFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="11fca-269">smallint</span><span class="sxs-lookup"><span data-stu-id="11fca-269">smallint</span></span></p></td>
<td><p><span data-ttu-id="11fca-270">呼び出しの属性を示します。</span><span class="sxs-lookup"><span data-stu-id="11fca-270">Indicates the call attributes.</span></span> <span data-ttu-id="11fca-271">次の属性定義を使用できます。</span><span class="sxs-lookup"><span data-stu-id="11fca-271">The following attribute definitions are allowed:</span></span></p>
<p><span data-ttu-id="11fca-272">0x01-再試行 Session0</span><span class="sxs-lookup"><span data-stu-id="11fca-272">0x01 - Retried Session0</span></span></p>
<p><span data-ttu-id="11fca-273">x02-応答グループの代理としてエージェントによって発信された通話</span><span class="sxs-lookup"><span data-stu-id="11fca-273">x02 - A call made by agent on behalf of a Response Group</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="11fca-274">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="11fca-274">


</div>

<span> </span>

</div>

</div>

</span></span></div>

