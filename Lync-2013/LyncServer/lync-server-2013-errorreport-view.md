---
title: 'Lync Server 2013: ErrorReport view'
description: 'Lync Server 2013: ErrorReport ビュー。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ErrorReport view
ms:assetid: ca873f7e-b18b-4eaf-8db0-5f9d5a9b60a1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721887(v=OCS.15)
ms:contentKeyID: 49733821
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 50fb0a362c71d8dfb5873157e7b1ed3d3eb680ae
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428525"
---
# <a name="errorreport-view-in-lync-server-2013"></a><span data-ttu-id="6a956-103">Lync Server 2013 での ErrorReport の表示</span><span class="sxs-lookup"><span data-stu-id="6a956-103">ErrorReport view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6a956-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6a956-104">

<span> </span></span></span>

<span data-ttu-id="6a956-105">_**最終更新日:** 2013-01-22_</span><span class="sxs-lookup"><span data-stu-id="6a956-105">_**Topic Last Modified:** 2013-01-22_</span></span>

<span data-ttu-id="6a956-106">ErrorReport ビューには、報告されたエラーに関する情報が格納されます。</span><span class="sxs-lookup"><span data-stu-id="6a956-106">The ErrorReport view stores information about errors reported.</span></span> <span data-ttu-id="6a956-107">各レコードはエラー発生の1つです。</span><span class="sxs-lookup"><span data-stu-id="6a956-107">Each record is one error occurrence.</span></span> <span data-ttu-id="6a956-108">このエラーは、フロントエンドサーバーで実行されている CDR エージェントまたはクライアントから送信された cd-r エージェントによってキャプチャされます。</span><span class="sxs-lookup"><span data-stu-id="6a956-108">The errors are captured either by the CDR agent running on the front-end server or sent from the client.</span></span> <span data-ttu-id="6a956-109">このビューは、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="6a956-109">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6a956-110">列</span><span class="sxs-lookup"><span data-stu-id="6a956-110">Column</span></span></th>
<th><span data-ttu-id="6a956-111">データ型</span><span class="sxs-lookup"><span data-stu-id="6a956-111">Data Type</span></span></th>
<th><span data-ttu-id="6a956-112">詳細</span><span class="sxs-lookup"><span data-stu-id="6a956-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6a956-113"><strong>ErrorTime</strong></span><span class="sxs-lookup"><span data-stu-id="6a956-113"><strong>ErrorTime</strong></span></span></p></td>
<td><p><span data-ttu-id="6a956-114">datetime</span><span class="sxs-lookup"><span data-stu-id="6a956-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="6a956-115">エラーが発生した時刻。</span><span class="sxs-lookup"><span data-stu-id="6a956-115">Time of error occurred.</span></span> <span data-ttu-id="6a956-116">エラーを一意に識別するには、ErrorReportSeq と組み合わせて使います。</span><span class="sxs-lookup"><span data-stu-id="6a956-116">Used in conjunction with ErrorReportSeq to uniquely identify an error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a956-117"><strong>ErrorReportSeq</strong></span><span class="sxs-lookup"><span data-stu-id="6a956-117"><strong>ErrorReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="6a956-118">int</span><span class="sxs-lookup"><span data-stu-id="6a956-118">int</span></span></p></td>
<td><p><span data-ttu-id="6a956-119">エラーを識別する ID 番号。</span><span class="sxs-lookup"><span data-stu-id="6a956-119">ID number to identify the error.</span></span> <span data-ttu-id="6a956-120">エラーを一意に識別するための ErrorTime と共に使用されます。</span><span class="sxs-lookup"><span data-stu-id="6a956-120">Used in conjunction with ErrorTime to uniquely identify an error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a956-121"><strong>MsDiagId</strong></span><span class="sxs-lookup"><span data-stu-id="6a956-121"><strong>MsDiagId</strong></span></span></p></td>
<td><p><span data-ttu-id="6a956-122">int</span><span class="sxs-lookup"><span data-stu-id="6a956-122">int</span></span></p></td>
<td><p><span data-ttu-id="6a956-123">エラーレポートの診断 ID。</span><span class="sxs-lookup"><span data-stu-id="6a956-123">Diagnostic ID for the error report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a956-124"><strong>FromUri</strong></span><span class="sxs-lookup"><span data-stu-id="6a956-124"><strong>FromUri</strong></span></span></p></td>
<td><p><span data-ttu-id="6a956-125">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="6a956-125">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="6a956-126">エラーを発生させたユーザーの URI。</span><span class="sxs-lookup"><span data-stu-id="6a956-126">URI of the user who originated the error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a956-127"><strong>FromUriType</strong></span><span class="sxs-lookup"><span data-stu-id="6a956-127"><strong>FromUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="6a956-128">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="6a956-128">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="6a956-129">エラーを発生させたユーザーの URI の種類。</span><span class="sxs-lookup"><span data-stu-id="6a956-129">Type of URI of the user who originated the error.</span></span> <span data-ttu-id="6a956-130">詳細については、「 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 の UriTypes テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6a956-130">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a956-131"><strong>FromTenant</strong></span><span class="sxs-lookup"><span data-stu-id="6a956-131"><strong>FromTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="6a956-132">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="6a956-132">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="6a956-133">エラーを発生させたユーザーのテナント。</span><span class="sxs-lookup"><span data-stu-id="6a956-133">Tenant of the user who originated the error.</span></span> <span data-ttu-id="6a956-134">詳細については、「 <a href="lync-server-2013-tenants-table.md">Lync Server 2013 のテナントの一覧</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6a956-134">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a956-135"><strong>ToUri</strong></span><span class="sxs-lookup"><span data-stu-id="6a956-135"><strong>ToUri</strong></span></span></p></td>
<td><p><span data-ttu-id="6a956-136">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="6a956-136">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="6a956-137">エラーレポートのターゲットであるユーザーの URI。</span><span class="sxs-lookup"><span data-stu-id="6a956-137">URI of the user who was the target of the error report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a956-138"><strong>ToUriType</strong></span><span class="sxs-lookup"><span data-stu-id="6a956-138"><strong>ToUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="6a956-139">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="6a956-139">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="6a956-140">エラーレポートの対象となるユーザーの URI の種類。</span><span class="sxs-lookup"><span data-stu-id="6a956-140">Type of URI of the user who target of the error report.</span></span> <span data-ttu-id="6a956-141">詳細については、UriTypes の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6a956-141">See the UriTypes Table for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a956-142"><strong>すべての Ant</strong></span><span class="sxs-lookup"><span data-stu-id="6a956-142"><strong>ToTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="6a956-143">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="6a956-143">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="6a956-144">エラーレポートの対象ユーザーのテナント。</span><span class="sxs-lookup"><span data-stu-id="6a956-144">Tenant of the user who target of the error report.</span></span> <span data-ttu-id="6a956-145">詳細については、「 <a href="lync-server-2013-tenants-table.md">Lync Server 2013 のテナントの一覧</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6a956-145">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a956-146"><strong>ConferenceUri</strong></span><span class="sxs-lookup"><span data-stu-id="6a956-146"><strong>ConferenceUri</strong></span></span></p></td>
<td><p><span data-ttu-id="6a956-147">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="6a956-147">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="6a956-148">エラーレポートのターゲットとなった会議の URI。</span><span class="sxs-lookup"><span data-stu-id="6a956-148">URI of the conference that was the target of the error report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a956-149"><strong>ConferenceUriType</strong></span><span class="sxs-lookup"><span data-stu-id="6a956-149"><strong>ConferenceUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="6a956-150">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="6a956-150">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="6a956-151">エラーレポートのターゲットとなった会議の URI の種類。</span><span class="sxs-lookup"><span data-stu-id="6a956-151">URI type of the conference that was the target of the error report.</span></span> <span data-ttu-id="6a956-152">詳細については、「 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 の UriTypes テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6a956-152">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a956-153"><strong>セッション Id</strong></span><span class="sxs-lookup"><span data-stu-id="6a956-153"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="6a956-154">datetime</span><span class="sxs-lookup"><span data-stu-id="6a956-154">datetime</span></span></p></td>
<td><p><span data-ttu-id="6a956-155">エラーレポートを生成したセッション要求の時刻。</span><span class="sxs-lookup"><span data-stu-id="6a956-155">Time of session request that originated the error report.</span></span> <span data-ttu-id="6a956-156">セッションを一意に識別するために SessionIdSeq と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="6a956-156">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="6a956-157">詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6a956-157">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a956-158"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="6a956-158"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="6a956-159">int</span><span class="sxs-lookup"><span data-stu-id="6a956-159">int</span></span></p></td>
<td><p><span data-ttu-id="6a956-160">エラーレポートを生成したセッション要求を識別する ID 番号。</span><span class="sxs-lookup"><span data-stu-id="6a956-160">ID number to identify the session request that originated the error report.</span></span> <span data-ttu-id="6a956-161">セッションを一意に識別するために SessionIdTime と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="6a956-161">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="6a956-162">詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6a956-162">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a956-163"><strong>この Id</strong></span><span class="sxs-lookup"><span data-stu-id="6a956-163"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="6a956-164">varstring (775)</span><span class="sxs-lookup"><span data-stu-id="6a956-164">varstring(775)</span></span></p></td>
<td><p><span data-ttu-id="6a956-165">エラーを発生させたセッションの SIP ダイアログ ID。</span><span class="sxs-lookup"><span data-stu-id="6a956-165">SIP dialog ID of session that originated the error.</span></span> <span data-ttu-id="6a956-166">形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="6a956-166">The format is:</span></span></p>
<p><span data-ttu-id="6a956-167">ダイアログ; 開始タグからタグへ</span><span class="sxs-lookup"><span data-stu-id="6a956-167">dialog;from-tag;to-tag</span></span></p>
<p><span data-ttu-id="6a956-168">このデータは、次の構文を使用してテキスト形式に変換できます。</span><span class="sxs-lookup"><span data-stu-id="6a956-168">This data can be converted to text format by using this syntax:</span></span></p>
<p><span data-ttu-id="6a956-169">キャスト (cast (ExternalId as varbinary (max)) (varchar (max)))</span><span class="sxs-lookup"><span data-stu-id="6a956-169">cast(cast(ExternalId as varbinary(max)) as varchar(max))</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a956-170"><strong>ClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="6a956-170"><strong>ClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="6a956-171">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="6a956-171">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="6a956-172">エラーの発生元のユーザーによって使用されたクライアントのバージョン。</span><span class="sxs-lookup"><span data-stu-id="6a956-172">Version of client used by the user who originated the error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a956-173"><strong>ClientType</strong></span><span class="sxs-lookup"><span data-stu-id="6a956-173"><strong>ClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="6a956-174">int</span><span class="sxs-lookup"><span data-stu-id="6a956-174">int</span></span></p></td>
<td><p><span data-ttu-id="6a956-175">エラーの発生元のユーザーによって使用されたクライアント。</span><span class="sxs-lookup"><span data-stu-id="6a956-175">Client used by the user who originated the error.</span></span> <span data-ttu-id="6a956-176">詳細については、「 <a href="lync-server-2013-useragentdef-table.md">Lync Server 2013 の Useragentdef テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6a956-176">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a956-177"><strong>ClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="6a956-177"><strong>ClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="6a956-178">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="6a956-178">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="6a956-179">エラーの発生元のユーザーによって使用されたクライアントのカテゴリの名前です。</span><span class="sxs-lookup"><span data-stu-id="6a956-179">Name of the category of the client used by the user who originated the error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a956-180"><strong>ソース</strong></span><span class="sxs-lookup"><span data-stu-id="6a956-180"><strong>Source</strong></span></span></p></td>
<td><p><span data-ttu-id="6a956-181">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="6a956-181">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="6a956-182">エラーが発生したサーバーの名前 (サーバーコンポーネントからレポートが送信された場合)。</span><span class="sxs-lookup"><span data-stu-id="6a956-182">Name of server that originated the error (if report was sent from a server component).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a956-183"><strong>Application</strong></span><span class="sxs-lookup"><span data-stu-id="6a956-183"><strong>Application</strong></span></span></p></td>
<td><p><span data-ttu-id="6a956-184">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="6a956-184">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="6a956-185">エラーの発生元のアプリケーションの名前 (サーバーコンポーネントからレポートが送信された場合)。</span><span class="sxs-lookup"><span data-stu-id="6a956-185">Name of application that originated the error (if report was sent from a server component).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a956-186"><strong>返信</strong></span><span class="sxs-lookup"><span data-stu-id="6a956-186"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="6a956-187">int</span><span class="sxs-lookup"><span data-stu-id="6a956-187">int</span></span></p></td>
<td><p><span data-ttu-id="6a956-188">エラーレポートが含まれる SIP メッセージのセッションへの SIP 応答コード。</span><span class="sxs-lookup"><span data-stu-id="6a956-188">SIP response code to the session of the SIP message containing the error report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a956-189"><strong>RequestType</strong></span><span class="sxs-lookup"><span data-stu-id="6a956-189"><strong>RequestType</strong></span></span></p></td>
<td><p><span data-ttu-id="6a956-190">varchar (max)</span><span class="sxs-lookup"><span data-stu-id="6a956-190">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="6a956-191">失敗した要求の種類。</span><span class="sxs-lookup"><span data-stu-id="6a956-191">Type of request that failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a956-192"><strong>ContentType</strong></span><span class="sxs-lookup"><span data-stu-id="6a956-192"><strong>ContentType</strong></span></span></p></td>
<td><p><span data-ttu-id="6a956-193">varchar (max)</span><span class="sxs-lookup"><span data-stu-id="6a956-193">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="6a956-194">失敗した要求のコンテンツタイプ。</span><span class="sxs-lookup"><span data-stu-id="6a956-194">Content type of the request that failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a956-195"><strong>CallType</strong></span><span class="sxs-lookup"><span data-stu-id="6a956-195"><strong>CallType</strong></span></span></p></td>
<td><p><span data-ttu-id="6a956-196">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="6a956-196">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="6a956-197">セッションの種類。</span><span class="sxs-lookup"><span data-stu-id="6a956-197">Type of session.</span></span> <span data-ttu-id="6a956-198">詳細については、「 <a href="lync-server-2013-calltype-table.md">Lync Server 2013 の CallType テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6a956-198">See the <a href="lync-server-2013-calltype-table.md">CallType table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a956-199"><strong>TelemetryId</strong></span><span class="sxs-lookup"><span data-stu-id="6a956-199"><strong>TelemetryId</strong></span></span></p></td>
<td><p><span data-ttu-id="6a956-200">長さ</span><span class="sxs-lookup"><span data-stu-id="6a956-200">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="6a956-201">電話会議に参加しているさまざまなコンポーネントについての、固有の識別子による結合時間情報の関連付け。</span><span class="sxs-lookup"><span data-stu-id="6a956-201">Unique identifier correlating join time information for the different components involved in a conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a956-202"><strong>SetupTime 時間</strong></span><span class="sxs-lookup"><span data-stu-id="6a956-202"><strong>SetupTime</strong></span></span></p></td>
<td><p><span data-ttu-id="6a956-203">int</span><span class="sxs-lookup"><span data-stu-id="6a956-203">int</span></span></p></td>
<td><p><span data-ttu-id="6a956-204">特定のコンポーネントが会議に参加するために必要な時間 (ミリ秒単位) です。</span><span class="sxs-lookup"><span data-stu-id="6a956-204">Time (in milliseconds) required for a specific component to join a conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a956-205"><strong>IsCapturedByServer</strong></span><span class="sxs-lookup"><span data-stu-id="6a956-205"><strong>IsCapturedByServer</strong></span></span></p></td>
<td><p><span data-ttu-id="6a956-206">bit</span><span class="sxs-lookup"><span data-stu-id="6a956-206">bit</span></span></p></td>
<td><p><span data-ttu-id="6a956-207">エラーレポートが、フロントエンドサーバーで実行されている CDR エージェントまたはクライアントによってキャプチャされたかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="6a956-207">Indicates whether the error report was captured by the CDR agent running on the Front End server, or sent by the client.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a956-208"><strong>フラッグ</strong></span><span class="sxs-lookup"><span data-stu-id="6a956-208"><strong>Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="6a956-209">smallint</span><span class="sxs-lookup"><span data-stu-id="6a956-209">smallint</span></span></p></td>
<td><p><span data-ttu-id="6a956-210">今後の使用のために予約されています。</span><span class="sxs-lookup"><span data-stu-id="6a956-210">Reserved for future use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a956-211"><strong>MsDiagHeader</strong></span><span class="sxs-lookup"><span data-stu-id="6a956-211"><strong>MsDiagHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="6a956-212">varchar (max)</span><span class="sxs-lookup"><span data-stu-id="6a956-212">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="6a956-213">エラーに関する追加情報。</span><span class="sxs-lookup"><span data-stu-id="6a956-213">Additional information about the error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a956-214"><strong>FrontEnd</strong></span><span class="sxs-lookup"><span data-stu-id="6a956-214"><strong>FrontEnd</strong></span></span></p></td>
<td><p><span data-ttu-id="6a956-215">nvarchar</span><span class="sxs-lookup"><span data-stu-id="6a956-215">nvarchar</span></span></p></td>
<td><p><span data-ttu-id="6a956-216">レポートを提出したフロントエンドサーバーの完全修飾ドメイン名。</span><span class="sxs-lookup"><span data-stu-id="6a956-216">Fully qualified domain name of the Front End server that submitted the report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a956-217"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="6a956-217"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="6a956-218">nvarchar</span><span class="sxs-lookup"><span data-stu-id="6a956-218">nvarchar</span></span></p></td>
<td><p><span data-ttu-id="6a956-219">レポートを提出したフロントエンドサーバーを含むプールの完全修飾ドメイン名。</span><span class="sxs-lookup"><span data-stu-id="6a956-219">Fully qualified domain name of the pool containing the Front End server that submitted the report.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="6a956-220">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6a956-220">


</div>

<span> </span>

</div>

</div>

</span></span></div>

