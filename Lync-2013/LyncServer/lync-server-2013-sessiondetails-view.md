---
title: 'Lync Server 2013: セッションの詳細ビュー'
description: 'Lync Server 2013: SessionDetails ビュー。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: SessionDetails view
ms:assetid: ea328c6f-cf22-48dd-8f7f-f1666c9148c8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721924(v=OCS.15)
ms:contentKeyID: 49733859
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4c9f657257e54389defb805919be61adbdecad74
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424031"
---
# <a name="sessiondetails-view-in-lync-server-2013"></a><span data-ttu-id="d412d-103">Lync Server 2013 のセッション詳細表示</span><span class="sxs-lookup"><span data-stu-id="d412d-103">SessionDetails view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d412d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d412d-104">

<span> </span></span></span>

<span data-ttu-id="d412d-105">_**最終更新日:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="d412d-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="d412d-106">セッションの詳細ビューには、ピアツーピアセッションに関する情報が格納されます。これは、VoIP-VoIP 電話、2パーティの IM セッション、または他の種類のセッションである可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d412d-106">The SessionDetails view stores information about peer-to-peer sessions, which could be a VoIP-VoIP phone call, two-party IM session, or other type of session.</span></span> <span data-ttu-id="d412d-107">このビューは、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="d412d-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d412d-108">列</span><span class="sxs-lookup"><span data-stu-id="d412d-108">Column</span></span></th>
<th><span data-ttu-id="d412d-109">データ型</span><span class="sxs-lookup"><span data-stu-id="d412d-109">Data Type</span></span></th>
<th><span data-ttu-id="d412d-110">詳細</span><span class="sxs-lookup"><span data-stu-id="d412d-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d412d-111"><strong>セッション Id</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-112">datetime</span><span class="sxs-lookup"><span data-stu-id="d412d-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="d412d-113">セッション要求の時刻。</span><span class="sxs-lookup"><span data-stu-id="d412d-113">Time of session request.</span></span> <span data-ttu-id="d412d-114">セッションを一意に識別するために SessionIdSeq と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="d412d-114">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="d412d-115">詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 テーブルのダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d412d-115">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> Table for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d412d-116"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-116"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-117">int</span><span class="sxs-lookup"><span data-stu-id="d412d-117">int</span></span></p></td>
<td><p><span data-ttu-id="d412d-118">セッションを識別する ID 番号。</span><span class="sxs-lookup"><span data-stu-id="d412d-118">ID number to identify the session.</span></span> <span data-ttu-id="d412d-119">セッションを一意に識別するために SessionIdTime と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="d412d-119">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="d412d-120">詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d412d-120">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d412d-121"><strong>InviteTime</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-121"><strong>InviteTime</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-122">datetime</span><span class="sxs-lookup"><span data-stu-id="d412d-122">datetime</span></span></p></td>
<td><p><span data-ttu-id="d412d-123">最初の招待要求の時刻。</span><span class="sxs-lookup"><span data-stu-id="d412d-123">Time of the first INVITE request.</span></span> <span data-ttu-id="d412d-124">通常、このフィールドは、セッションの最初の INVITE メッセージから生成されたデータによって設定されます。</span><span class="sxs-lookup"><span data-stu-id="d412d-124">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="d412d-125">招待メッセージがない場合は、最初に関連する SIP メッセージ (BYE、キャンセル、メッセージ、または情報) の日付と時刻がフィールドに設定されています。</span><span class="sxs-lookup"><span data-stu-id="d412d-125">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span> <span data-ttu-id="d412d-126">通常、このフィールドは、セッションの最初の INVITE メッセージから生成されたデータによって設定されます。</span><span class="sxs-lookup"><span data-stu-id="d412d-126">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="d412d-127">招待メッセージがない場合は、最初に関連する SIP メッセージ (BYE、キャンセル、メッセージ、または情報) の日付と時刻がフィールドに設定されています。</span><span class="sxs-lookup"><span data-stu-id="d412d-127">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d412d-128"><strong>FromUri</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-128"><strong>FromUri</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-129">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="d412d-129">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="d412d-130">セッションを開始したユーザーの URI。</span><span class="sxs-lookup"><span data-stu-id="d412d-130">URI of the user who started the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d412d-131"><strong>ToUri</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-131"><strong>ToUri</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-132">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="d412d-132">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="d412d-133">セッションに参加したユーザーの URI。</span><span class="sxs-lookup"><span data-stu-id="d412d-133">URI of the user who joined the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d412d-134"><strong>FromUriType</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-134"><strong>FromUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-135">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d412d-135">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d412d-136">セッションを開始したユーザーの URI の種類。</span><span class="sxs-lookup"><span data-stu-id="d412d-136">Type of URI of the user who started the session.</span></span> <span data-ttu-id="d412d-137">詳細については、「 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 の UriTypes テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d412d-137">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d412d-138"><strong>ToUriType</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-138"><strong>ToUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-139">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d412d-139">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d412d-140">セッションに参加したユーザーの URI の種類。</span><span class="sxs-lookup"><span data-stu-id="d412d-140">Type of URI of the user who joined the session.</span></span> <span data-ttu-id="d412d-141">詳細については、「 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 の UriTypes テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d412d-141">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d412d-142"><strong>FromTenant</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-142"><strong>FromTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-143">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="d412d-143">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="d412d-144">セッションを開始したユーザーのテナント。</span><span class="sxs-lookup"><span data-stu-id="d412d-144">Tenant of the user who started the session.</span></span> <span data-ttu-id="d412d-145">詳細については、「 <a href="lync-server-2013-tenants-table.md">Lync Server 2013 のテナントの一覧</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d412d-145">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d412d-146"><strong>すべての Ant</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-146"><strong>ToTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-147">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d412d-147">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d412d-148">セッションに参加したユーザーのテナント。</span><span class="sxs-lookup"><span data-stu-id="d412d-148">The tenant of the user who joined the session.</span></span> <span data-ttu-id="d412d-149">詳細については、「 <a href="lync-server-2013-tenants-table.md">Lync Server 2013 のテナントの一覧</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d412d-149">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d412d-150"><strong>FromEndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-150"><strong>FromEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-151">長さ</span><span class="sxs-lookup"><span data-stu-id="d412d-151">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="d412d-152">セッションを開始したユーザーのエンドポイントを表す一意の識別子です。</span><span class="sxs-lookup"><span data-stu-id="d412d-152">Unique identifier of the endpoint of the user who started the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d412d-153"><strong>ToEndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-153"><strong>ToEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-154">長さ</span><span class="sxs-lookup"><span data-stu-id="d412d-154">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="d412d-155">セッションに参加したユーザーのエンドポイントを表す一意の識別子です。</span><span class="sxs-lookup"><span data-stu-id="d412d-155">Unique identifier of the endpoint of the user who joined the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d412d-156"><strong>EndTime</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-156"><strong>EndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-157">datetime</span><span class="sxs-lookup"><span data-stu-id="d412d-157">datetime</span></span></p></td>
<td><p><span data-ttu-id="d412d-158">セッションの終了時刻。</span><span class="sxs-lookup"><span data-stu-id="d412d-158">End time of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d412d-159"><strong>FromMessageCount</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-159"><strong>FromMessageCount</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-160">int</span><span class="sxs-lookup"><span data-stu-id="d412d-160">int</span></span></p></td>
<td><p><span data-ttu-id="d412d-161">セッションを開始したユーザーによって送信されたメッセージの数です。</span><span class="sxs-lookup"><span data-stu-id="d412d-161">Number of messages sent by the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d412d-162"><strong>ToMessageCount</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-162"><strong>ToMessageCount</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-163">int</span><span class="sxs-lookup"><span data-stu-id="d412d-163">int</span></span></p></td>
<td><p><span data-ttu-id="d412d-164">セッションに参加したユーザーによって送信されたメッセージの数です。</span><span class="sxs-lookup"><span data-stu-id="d412d-164">Number of messages sent by the user who joined the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d412d-165"><strong>FromClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-165"><strong>FromClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-166">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d412d-166">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d412d-167">セッションを開始したユーザーによって使用されたクライアントのバージョン。</span><span class="sxs-lookup"><span data-stu-id="d412d-167">Version of client used by the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d412d-168"><strong>FromClientType</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-168"><strong>FromClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-169">int</span><span class="sxs-lookup"><span data-stu-id="d412d-169">int</span></span></p></td>
<td><p><span data-ttu-id="d412d-170">セッションを開始したユーザーによって使用されたクライアント。</span><span class="sxs-lookup"><span data-stu-id="d412d-170">Client used by the user who started the session.</span></span> <span data-ttu-id="d412d-171">詳細については、「 <a href="lync-server-2013-useragentdef-table.md">Lync Server 2013 の Useragentdef テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d412d-171">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d412d-172"><strong>FromClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-172"><strong>FromClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-173">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="d412d-173">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="d412d-174">セッションを開始したユーザーによって使用されたクライアントのカテゴリの名前です。</span><span class="sxs-lookup"><span data-stu-id="d412d-174">Name of the category of the client used by the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d412d-175"><strong>ToClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-175"><strong>ToClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-176">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d412d-176">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d412d-177">セッションに参加したユーザーによって使用されたクライアントのバージョン</span><span class="sxs-lookup"><span data-stu-id="d412d-177">Version of client used by the user who joined the session</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d412d-178"><strong>ToClientType</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-178"><strong>ToClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-179">int</span><span class="sxs-lookup"><span data-stu-id="d412d-179">int</span></span></p></td>
<td><p><span data-ttu-id="d412d-180">セッションに参加したユーザーによって使用されたクライアント。</span><span class="sxs-lookup"><span data-stu-id="d412d-180">Client used by the user who joined the session.</span></span> <span data-ttu-id="d412d-181">詳細については、「 <a href="lync-server-2013-useragentdef-table.md">Lync Server 2013 の Useragentdef テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d412d-181">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d412d-182"><strong>ToClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-182"><strong>ToClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-183">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="d412d-183">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="d412d-184">セッションに参加したユーザーによって使用されたクライアントのカテゴリの名前です。</span><span class="sxs-lookup"><span data-stu-id="d412d-184">Name of the category of the client used by the user who joined the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d412d-185"><strong>TargetUri</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-185"><strong>TargetUri</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-186">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="d412d-186">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="d412d-187">セッションのターゲットユーザーの URI。</span><span class="sxs-lookup"><span data-stu-id="d412d-187">URI of the target user of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d412d-188"><strong>TargetUriType</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-188"><strong>TargetUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-189">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="d412d-189">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="d412d-190">セッションのターゲットユーザーの URI の種類です。</span><span class="sxs-lookup"><span data-stu-id="d412d-190">Type of URI of the target user for the session.</span></span> <span data-ttu-id="d412d-191">詳細については、「 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 の UriTypes テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d412d-191">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d412d-192"><strong>OnBehalfOfUri</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-192"><strong>OnBehalfOfUri</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-193">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="d412d-193">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="d412d-194">セッションが開始されたユーザーの URI。</span><span class="sxs-lookup"><span data-stu-id="d412d-194">URI of the user on whose behalf the session was started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d412d-195"><strong>OnnnBehalfOfUriType</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-195"><strong>OnnnBehalfOfUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-196">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d412d-196">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d412d-197">セッションが開始されたユーザーの URI の種類。</span><span class="sxs-lookup"><span data-stu-id="d412d-197">Type of URI of the user on whose behalf the session was started.</span></span> <span data-ttu-id="d412d-198">詳細については、「 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 の UriTypes テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d412d-198">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d412d-199"><strong>OnBehalfOfTenant</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-199"><strong>OnBehalfOfTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-200">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d412d-200">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d412d-201">セッションを開始したユーザーのテナント。</span><span class="sxs-lookup"><span data-stu-id="d412d-201">Tenant of the user whose on behalf the session was started.</span></span> <span data-ttu-id="d412d-202">詳細については、「 <a href="lync-server-2013-tenants-table.md">Lync Server 2013 のテナントの一覧</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d412d-202">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d412d-203"><strong>△この Uri</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-203"><strong>ReferredByUri</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-204">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="d412d-204">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="d412d-205">セッションを参照したユーザーの URI。</span><span class="sxs-lookup"><span data-stu-id="d412d-205">URI of the user who referred the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d412d-206"><strong>ベンチャー Redbyuritん</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-206"><strong>ReferredByUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-207">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d412d-207">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d412d-208">セッションを参照したユーザーの URI の種類。</span><span class="sxs-lookup"><span data-stu-id="d412d-208">Type of URI of the user who referred the session.</span></span> <span data-ttu-id="d412d-209">詳細については、「 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 の UriTypes テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d412d-209">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d412d-210"><strong>このテナント</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-210"><strong>ReferredByTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-211">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d412d-211">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d412d-212">セッションを参照したユーザーのテナント。</span><span class="sxs-lookup"><span data-stu-id="d412d-212">Tenant of the user who referred the session.</span></span> <span data-ttu-id="d412d-213">詳細については、「 <a href="lync-server-2013-tenants-table.md">Lync Server 2013 のテナントの一覧</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d412d-213">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d412d-214"><strong>この Id</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-214"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-215">varchar (775)</span><span class="sxs-lookup"><span data-stu-id="d412d-215">varchar(775)</span></span></p></td>
<td><p><span data-ttu-id="d412d-216">SIP ダイアログ ID。</span><span class="sxs-lookup"><span data-stu-id="d412d-216">SIP dialog ID.</span></span> <span data-ttu-id="d412d-217">形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="d412d-217">The format is:</span></span></p>
<p><span data-ttu-id="d412d-218">ダイアログ; 開始タグからタグへ</span><span class="sxs-lookup"><span data-stu-id="d412d-218">dialog;from-tag;to-tag</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d412d-219"><strong>CorrelationId</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-219"><strong>CorrelationId</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-220">長さ</span><span class="sxs-lookup"><span data-stu-id="d412d-220">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="d412d-221">複数のセッションの関連付けに使用する GUID。</span><span class="sxs-lookup"><span data-stu-id="d412d-221">GUID used to correlate multiple sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d412d-222"><strong>Edialogidtime の置き換え</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-222"><strong>ReplaceDialogIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-223">datetime</span><span class="sxs-lookup"><span data-stu-id="d412d-223">datetime</span></span></p></td>
<td><p><span data-ttu-id="d412d-224">セッションによって置き換えられたダイアログの時間です。</span><span class="sxs-lookup"><span data-stu-id="d412d-224">Time of the dialog which was replaced by the session.</span></span> <span data-ttu-id="d412d-225">セッションによって置き換えられるダイアログを一意に識別するには、置換 Edialogidseq と組み合わせて使います。</span><span class="sxs-lookup"><span data-stu-id="d412d-225">Used in conjunction with ReplaceDialogIdSeq to uniquely identify a dialog that is replaced by the session.</span></span> <span data-ttu-id="d412d-226">詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d412d-226">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d412d-227"><strong>Edialogidseq の置き換え</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-227"><strong>ReplaceDialogIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-228">int</span><span class="sxs-lookup"><span data-stu-id="d412d-228">int</span></span></p></td>
<td><p><span data-ttu-id="d412d-229">セッションを識別する ID 番号。</span><span class="sxs-lookup"><span data-stu-id="d412d-229">ID number to identify the session.</span></span> <span data-ttu-id="d412d-230">セッションによって置き換えられるダイアログを一意に識別するために、交換 Edialogidtime と組み合わせて使います。</span><span class="sxs-lookup"><span data-stu-id="d412d-230">Used in conjunction with ReplaceDialogIdTime to uniquely identify a dialog that is replaced by the session.</span></span> <span data-ttu-id="d412d-231">詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d412d-231">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d412d-232"><strong>置換の方法 Id</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-232"><strong>ReplacesDialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-233">varchar (775)</span><span class="sxs-lookup"><span data-stu-id="d412d-233">varchar(775)</span></span></p></td>
<td><p><span data-ttu-id="d412d-234">SIP ダイアログ ID によってセッションが置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="d412d-234">SIP dialog ID the session replaces.</span></span> <span data-ttu-id="d412d-235">形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="d412d-235">The format is:</span></span></p>
<p><span data-ttu-id="d412d-236">ダイアログ; 開始タグからタグへ</span><span class="sxs-lookup"><span data-stu-id="d412d-236">dialog;from-tag;to-tag</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d412d-237"><strong>ResponseTime</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-237"><strong>ResponseTime</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-238">datetime</span><span class="sxs-lookup"><span data-stu-id="d412d-238">datetime</span></span></p></td>
<td><p><span data-ttu-id="d412d-239">最初の招待メッセージに対する返信の時刻。</span><span class="sxs-lookup"><span data-stu-id="d412d-239">Time of the response to the first INVITE message.</span></span> <span data-ttu-id="d412d-240">通常、このフィールドは、セッションの最初の INVITE メッセージから生成されたデータによって設定されます。</span><span class="sxs-lookup"><span data-stu-id="d412d-240">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="d412d-241">招待メッセージがない場合は、最初に関連する SIP メッセージ (BYE、キャンセル、メッセージ、または情報) の日付と時刻がフィールドに設定されています。</span><span class="sxs-lookup"><span data-stu-id="d412d-241">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d412d-242"><strong>返信</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-242"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-243">int</span><span class="sxs-lookup"><span data-stu-id="d412d-243">int</span></span></p></td>
<td><p><span data-ttu-id="d412d-244">セッション招待状への SIP 応答コード。</span><span class="sxs-lookup"><span data-stu-id="d412d-244">SIP response code to the session invitation.</span></span> <span data-ttu-id="d412d-245">通常、このフィールドは、セッションの最初の INVITE メッセージから生成されたデータによって設定されます。</span><span class="sxs-lookup"><span data-stu-id="d412d-245">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="d412d-246">招待メッセージがない場合は、最初に関連する SIP メッセージ (BYE、キャンセル、メッセージ、または情報) の日付と時刻がフィールドに設定されています。</span><span class="sxs-lookup"><span data-stu-id="d412d-246">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d412d-247"><strong>DiagnosticId</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-247"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-248">int</span><span class="sxs-lookup"><span data-stu-id="d412d-248">int</span></span></p></td>
<td><p><span data-ttu-id="d412d-249">SIP ヘッダーからキャプチャされた診断 ID。</span><span class="sxs-lookup"><span data-stu-id="d412d-249">Diagnostic ID captured from SIP headers.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d412d-250"><strong>ContentType</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-250"><strong>ContentType</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-251">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d412d-251">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d412d-252">セッションのコンテンツの種類です。</span><span class="sxs-lookup"><span data-stu-id="d412d-252">Type of content for the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d412d-253"><strong>FrontEnd</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-253"><strong>FrontEnd</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-254">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d412d-254">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d412d-255">セッションのデータをキャプチャしたフロントエンドサーバーの FQDN。</span><span class="sxs-lookup"><span data-stu-id="d412d-255">FQDN of the Front End server that captured the data for the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d412d-256"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-256"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-257">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d412d-257">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d412d-258">セッションのデータをキャプチャしたプールの FQDN。</span><span class="sxs-lookup"><span data-stu-id="d412d-258">FQDN of the pool that captured the data for the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d412d-259"><strong>FromEdgeServer</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-259"><strong>FromEdgeServer</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-260">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d412d-260">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d412d-261">セッションを開始したユーザーによって使用されたエッジサーバーの FQDN。</span><span class="sxs-lookup"><span data-stu-id="d412d-261">FQDN of the Edge server used by the user who started the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d412d-262"><strong>ToEdgeServer</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-262"><strong>ToEdgeServer</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-263">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d412d-263">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d412d-264">セッションを開始したユーザーによって使用されたエッジサーバーの FQDN</span><span class="sxs-lookup"><span data-stu-id="d412d-264">FQDN of the Edge server used by the user who started the session</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d412d-265"><strong>IsFromInternal</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-265"><strong>IsFromInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-266">bit</span><span class="sxs-lookup"><span data-stu-id="d412d-266">bit</span></span></p></td>
<td><p><span data-ttu-id="d412d-267">セッションを開始したユーザーが内部ネットワークからログオンしているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="d412d-267">Indicates whether the user who started the session logged on from the internal network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d412d-268"><strong>IsToInternal</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-268"><strong>IsToInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-269">bit</span><span class="sxs-lookup"><span data-stu-id="d412d-269">bit</span></span></p></td>
<td><p><span data-ttu-id="d412d-270">セッションに参加したユーザーが内部ネットワークからログオンしているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="d412d-270">Indicates whether the user who joined the session logged on from the internal network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d412d-271"><strong>CallPriority</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-271"><strong>CallPriority</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-272">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d412d-272">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d412d-273">セッションの通話優先度。</span><span class="sxs-lookup"><span data-stu-id="d412d-273">Call priority of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d412d-274"><strong>FromUserFlag</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-274"><strong>FromUserFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-275">smallint</span><span class="sxs-lookup"><span data-stu-id="d412d-275">smallint</span></span></p></td>
<td><p><span data-ttu-id="d412d-276">セッションを開始したユーザーの属性を示します。</span><span class="sxs-lookup"><span data-stu-id="d412d-276">Indicates the attributes of the user who started the session.</span></span> <span data-ttu-id="d412d-277">次の属性定義を使用できます。</span><span class="sxs-lookup"><span data-stu-id="d412d-277">The following attribute definitions are allowed:</span></span></p>
<p><span data-ttu-id="d412d-278">0x01-デスクトップ電話と統合</span><span class="sxs-lookup"><span data-stu-id="d412d-278">0x01 - Integrated with desktop phone</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d412d-279"><strong>ToUserFlag</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-279"><strong>ToUserFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-280">smallint</span><span class="sxs-lookup"><span data-stu-id="d412d-280">smallint</span></span></p></td>
<td><p><span data-ttu-id="d412d-281">セッションを開始したユーザーの属性を示します。</span><span class="sxs-lookup"><span data-stu-id="d412d-281">Indicates the attributes of the user who started the session.</span></span> <span data-ttu-id="d412d-282">次の属性定義を使用できます。</span><span class="sxs-lookup"><span data-stu-id="d412d-282">The following attribute definitions are allowed:</span></span></p>
<p><span data-ttu-id="d412d-283">0x01-デスクトップ電話と統合</span><span class="sxs-lookup"><span data-stu-id="d412d-283">0x01 - Integrated with desktop phone</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d412d-284"><strong>CallFlag</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-284"><strong>CallFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-285">smallint</span><span class="sxs-lookup"><span data-stu-id="d412d-285">smallint</span></span></p></td>
<td><p><span data-ttu-id="d412d-286">呼び出しの属性を示します。</span><span class="sxs-lookup"><span data-stu-id="d412d-286">Indicates the call attributes.</span></span> <span data-ttu-id="d412d-287">次の属性定義を使用できます。</span><span class="sxs-lookup"><span data-stu-id="d412d-287">The following attribute definitions are allowed:</span></span></p>
<p><span data-ttu-id="d412d-288">0x01-再試行セッション</span><span class="sxs-lookup"><span data-stu-id="d412d-288">0x01 - Retried Session</span></span></p>
<p><span data-ttu-id="d412d-289">0x02-応答グループの代理としてエージェントによって発信された通話</span><span class="sxs-lookup"><span data-stu-id="d412d-289">0x02 - A call made by agent on behalf of a Response Group</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d412d-290"><strong>場所</strong></span><span class="sxs-lookup"><span data-stu-id="d412d-290"><strong>Location</strong></span></span></p></td>
<td><p><span data-ttu-id="d412d-291">varchar (max)</span><span class="sxs-lookup"><span data-stu-id="d412d-291">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="d412d-292">緊急通話の場所。</span><span class="sxs-lookup"><span data-stu-id="d412d-292">Location of emergency call.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="d412d-293">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d412d-293">


</div>

<span> </span>

</div>

</div>

</span></span></div>

