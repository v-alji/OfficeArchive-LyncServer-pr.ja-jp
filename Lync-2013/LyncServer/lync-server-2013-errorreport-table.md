---
title: 'Lync Server 2013: ErrorReport テーブル'
description: 'Lync Server 2013: ErrorReport テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ErrorReport table
ms:assetid: ae0287b4-e8ca-4f8c-84ef-502897dcaa2a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412826(v=OCS.15)
ms:contentKeyID: 48185129
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9c1cc65c396c16dc137255438f7ef7c32b2d0b78
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428518"
---
# <a name="errorreport-table-in-lync-server-2013"></a><span data-ttu-id="2042b-103">Lync Server 2013 の ErrorReport テーブル</span><span class="sxs-lookup"><span data-stu-id="2042b-103">ErrorReport table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2042b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2042b-104">

<span> </span></span></span>

<span data-ttu-id="2042b-105">_**最終更新日:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="2042b-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="2042b-106">ErrorReport テーブルには、発生したエラーに関する情報が格納されます。</span><span class="sxs-lookup"><span data-stu-id="2042b-106">The ErrorReport table stores information about errors that have occurred.</span></span> <span data-ttu-id="2042b-107">各レコードはエラー発生の1つです。</span><span class="sxs-lookup"><span data-stu-id="2042b-107">Each record is one error occurrence.</span></span> <span data-ttu-id="2042b-108">このエラーは、フロントエンドサーバーで実行されている CDR エージェントまたはクライアントから送信された cd-r エージェントによってキャプチャされます。</span><span class="sxs-lookup"><span data-stu-id="2042b-108">The errors are captured either by the CDR agent running on the front-end server or sent from the client.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2042b-109">列</span><span class="sxs-lookup"><span data-stu-id="2042b-109">Column</span></span></th>
<th><span data-ttu-id="2042b-110">データ型</span><span class="sxs-lookup"><span data-stu-id="2042b-110">Data Type</span></span></th>
<th><span data-ttu-id="2042b-111">キー/インデックス</span><span class="sxs-lookup"><span data-stu-id="2042b-111">Key/Index</span></span></th>
<th><span data-ttu-id="2042b-112">詳細</span><span class="sxs-lookup"><span data-stu-id="2042b-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2042b-113"><strong>ErrorTime</strong></span><span class="sxs-lookup"><span data-stu-id="2042b-113"><strong>ErrorTime</strong></span></span></p></td>
<td><p><span data-ttu-id="2042b-114">datetime</span><span class="sxs-lookup"><span data-stu-id="2042b-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="2042b-115">Primary</span><span class="sxs-lookup"><span data-stu-id="2042b-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="2042b-116">エラーが発生した日付と時刻。</span><span class="sxs-lookup"><span data-stu-id="2042b-116">Date and time the error occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2042b-117"><strong>ErrorReportSeq</strong></span><span class="sxs-lookup"><span data-stu-id="2042b-117"><strong>ErrorReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="2042b-118">int</span><span class="sxs-lookup"><span data-stu-id="2042b-118">int</span></span></p></td>
<td><p><span data-ttu-id="2042b-119">Primary</span><span class="sxs-lookup"><span data-stu-id="2042b-119">Primary</span></span></p></td>
<td><p><span data-ttu-id="2042b-120">エラーレポートを識別する ID 番号。</span><span class="sxs-lookup"><span data-stu-id="2042b-120">ID number to identify the error report.</span></span> <span data-ttu-id="2042b-121">エラーレポートを一意に識別するための <strong>Errortime</strong> と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="2042b-121">Used in conjunction with <strong>ErrorTime</strong> to uniquely identify an error report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2042b-122"><strong>ErrorId</strong></span><span class="sxs-lookup"><span data-stu-id="2042b-122"><strong>ErrorId</strong></span></span></p></td>
<td><p><span data-ttu-id="2042b-123">int</span><span class="sxs-lookup"><span data-stu-id="2042b-123">int</span></span></p></td>
<td><p><span data-ttu-id="2042b-124">外部</span><span class="sxs-lookup"><span data-stu-id="2042b-124">Foreign</span></span></p></td>
<td><p><span data-ttu-id="2042b-125">エラーの種類の一意の ID です。</span><span class="sxs-lookup"><span data-stu-id="2042b-125">Unique ID of the error type.</span></span> <span data-ttu-id="2042b-126">詳細については、「 <a href="lync-server-2013-errordef-table.md">Lync Server 2013 の Errordef テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2042b-126">See the <a href="lync-server-2013-errordef-table.md">ErrorDef table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2042b-127"><strong>FromUserId</strong></span><span class="sxs-lookup"><span data-stu-id="2042b-127"><strong>FromUserId</strong></span></span></p></td>
<td><p><span data-ttu-id="2042b-128">int</span><span class="sxs-lookup"><span data-stu-id="2042b-128">int</span></span></p></td>
<td><p><span data-ttu-id="2042b-129">外部</span><span class="sxs-lookup"><span data-stu-id="2042b-129">Foreign</span></span></p></td>
<td><p><span data-ttu-id="2042b-130">エラーの原因となった要求を生成したユーザー。</span><span class="sxs-lookup"><span data-stu-id="2042b-130">User who originated the request that caused the error.</span></span> <span data-ttu-id="2042b-131">詳細については、「 <a href="lync-server-2013-users-table.md">Lync Server 2013 のユーザーテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2042b-131">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2042b-132"><strong>ToUserId</strong></span><span class="sxs-lookup"><span data-stu-id="2042b-132"><strong>ToUserId</strong></span></span></p></td>
<td><p><span data-ttu-id="2042b-133">int</span><span class="sxs-lookup"><span data-stu-id="2042b-133">int</span></span></p></td>
<td><p><span data-ttu-id="2042b-134">外部</span><span class="sxs-lookup"><span data-stu-id="2042b-134">Foreign</span></span></p></td>
<td><p><span data-ttu-id="2042b-135">エラーの原因となった要求の送信先ユーザー。</span><span class="sxs-lookup"><span data-stu-id="2042b-135">Destination user for the request that caused the error.</span></span> <span data-ttu-id="2042b-136">詳細については、「 <a href="lync-server-2013-users-table.md">Lync Server 2013 のユーザーテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2042b-136">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2042b-137"><strong>ConferenceUriId</strong></span><span class="sxs-lookup"><span data-stu-id="2042b-137"><strong>ConferenceUriId</strong></span></span></p></td>
<td><p><span data-ttu-id="2042b-138">int</span><span class="sxs-lookup"><span data-stu-id="2042b-138">int</span></span></p></td>
<td><p><span data-ttu-id="2042b-139">外部</span><span class="sxs-lookup"><span data-stu-id="2042b-139">Foreign</span></span></p></td>
<td><p><span data-ttu-id="2042b-140">エラーに関連する会議の URI。</span><span class="sxs-lookup"><span data-stu-id="2042b-140">Conference URI related to the error.</span></span> <span data-ttu-id="2042b-141">詳細については、「 <a href="lync-server-2013-conferenceuris-table.md">Lync Server 2013 の ConferenceUris テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2042b-141">See the <a href="lync-server-2013-conferenceuris-table.md">ConferenceUris table in Lync Server 2013</a> for more information.</span></span> <span data-ttu-id="2042b-142">通常、ConferenceUriId が null でない場合は、FromUserId または ToUserId は null になります。</span><span class="sxs-lookup"><span data-stu-id="2042b-142">Typically, if ConferenceUriId is not null, then either FromUserId or ToUserId will be null.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2042b-143"><strong>セッション Id</strong></span><span class="sxs-lookup"><span data-stu-id="2042b-143"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="2042b-144">datetime</span><span class="sxs-lookup"><span data-stu-id="2042b-144">datetime</span></span></p></td>
<td><p><span data-ttu-id="2042b-145">外部</span><span class="sxs-lookup"><span data-stu-id="2042b-145">Foreign</span></span></p></td>
<td><p><span data-ttu-id="2042b-146">セッションを一意に識別するために <strong>Sessionidseq</strong> と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="2042b-146">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="2042b-147">詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2042b-147">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2042b-148"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="2042b-148"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="2042b-149">int</span><span class="sxs-lookup"><span data-stu-id="2042b-149">int</span></span></p></td>
<td><p><span data-ttu-id="2042b-150">外部</span><span class="sxs-lookup"><span data-stu-id="2042b-150">Foreign</span></span></p></td>
<td><p><span data-ttu-id="2042b-151">セッションを識別する ID 番号。</span><span class="sxs-lookup"><span data-stu-id="2042b-151">ID number to identify the session.</span></span> <span data-ttu-id="2042b-152">セッションを一意に識別するために <strong>Sessionidtime</strong> と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="2042b-152">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="2042b-153">詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2042b-153">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2042b-154"><strong>SourceId</strong></span><span class="sxs-lookup"><span data-stu-id="2042b-154"><strong>SourceId</strong></span></span></p></td>
<td><p><span data-ttu-id="2042b-155">int</span><span class="sxs-lookup"><span data-stu-id="2042b-155">int</span></span></p></td>
<td><p><span data-ttu-id="2042b-156">外部</span><span class="sxs-lookup"><span data-stu-id="2042b-156">Foreign</span></span></p></td>
<td><p><span data-ttu-id="2042b-157">エラーレポートを送信したサーバー (レポートがサーバーコンポーネントから送信されている場合)。</span><span class="sxs-lookup"><span data-stu-id="2042b-157">Server that sent the error report (if the report is being sent from a server component).</span></span> <span data-ttu-id="2042b-158">詳細については、「 <a href="lync-server-2013-servers-table.md">Lync Server 2013 のサーバーの表</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2042b-158">See the <a href="lync-server-2013-servers-table.md">Servers table in Lync Server 2013</a> for more information.</span></span></p>
<p><span data-ttu-id="2042b-159">このフィールドは、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="2042b-159">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2042b-160"><strong>ApplicationId</strong></span><span class="sxs-lookup"><span data-stu-id="2042b-160"><strong>ApplicationId</strong></span></span></p></td>
<td><p><span data-ttu-id="2042b-161">int</span><span class="sxs-lookup"><span data-stu-id="2042b-161">int</span></span></p></td>
<td><p><span data-ttu-id="2042b-162">外部</span><span class="sxs-lookup"><span data-stu-id="2042b-162">Foreign</span></span></p></td>
<td><p><span data-ttu-id="2042b-163">エラーレポートを送信したサーバー (レポートがサーバーコンポーネントから送信されている場合)。</span><span class="sxs-lookup"><span data-stu-id="2042b-163">Server that sent the error report (if the report is being sent from a server component).</span></span> <span data-ttu-id="2042b-164">詳細については、「 <a href="lync-server-2013-application-table.md">Lync Server 2013 のアプリケーションテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2042b-164">See the <a href="lync-server-2013-application-table.md">Application table in Lync Server 2013</a> for more information.</span></span></p>
<p><span data-ttu-id="2042b-165">このフィールドは、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="2042b-165">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2042b-166"><strong>MsDiagHeader</strong></span><span class="sxs-lookup"><span data-stu-id="2042b-166"><strong>MsDiagHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="2042b-167">画像</span><span class="sxs-lookup"><span data-stu-id="2042b-167">image</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="2042b-168">エラーに関する詳細情報。</span><span class="sxs-lookup"><span data-stu-id="2042b-168">More information about the error.</span></span></p>
<p><span data-ttu-id="2042b-169">このデータは、次の構文を使用してテキスト形式に変換できます。</span><span class="sxs-lookup"><span data-stu-id="2042b-169">This data can be converted to text format by using this syntax:</span></span></p>
<p><code>cast(cast(Detail as varbinary(max)) as varchar(max)) </code></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2042b-170"><strong>ClientVersionId</strong></span><span class="sxs-lookup"><span data-stu-id="2042b-170"><strong>ClientVersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="2042b-171">int</span><span class="sxs-lookup"><span data-stu-id="2042b-171">int</span></span></p></td>
<td><p><span data-ttu-id="2042b-172">外部</span><span class="sxs-lookup"><span data-stu-id="2042b-172">Foreign</span></span></p></td>
<td><p><span data-ttu-id="2042b-173">エラーレポートを送信するエンドポイントのクライアントバージョン。</span><span class="sxs-lookup"><span data-stu-id="2042b-173">The client version of endpoint that sends the error report.</span></span> <span data-ttu-id="2042b-174">詳細については、「 <a href="lync-server-2013-clientversions-table.md">Lync Server 2013 の Clientversions の表</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2042b-174">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2042b-175"><strong>IsCapturedByServer</strong></span><span class="sxs-lookup"><span data-stu-id="2042b-175"><strong>IsCapturedByServer</strong></span></span></p></td>
<td><p><span data-ttu-id="2042b-176">bit</span><span class="sxs-lookup"><span data-stu-id="2042b-176">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="2042b-177">エラーレポートは、フロントエンドサーバーで実行されている CDR エージェントまたはクライアントによってキャプチャされます。</span><span class="sxs-lookup"><span data-stu-id="2042b-177">Is the error report captured by the CDR agent running on the front-end server, or sent by the client.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2042b-178"><strong>フラッグ</strong></span><span class="sxs-lookup"><span data-stu-id="2042b-178"><strong>Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="2042b-179">smallint</span><span class="sxs-lookup"><span data-stu-id="2042b-179">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="2042b-180">今後の使用のために予約されています。</span><span class="sxs-lookup"><span data-stu-id="2042b-180">Reserved for future use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2042b-181"><strong>TelemetryId</strong></span><span class="sxs-lookup"><span data-stu-id="2042b-181"><strong>TelemetryId</strong></span></span></p></td>
<td><p><span data-ttu-id="2042b-182">長さ</span><span class="sxs-lookup"><span data-stu-id="2042b-182">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="2042b-183">電話会議に参加しているさまざまなコンポーネントについての、固有の識別子による結合時間情報の関連付け。</span><span class="sxs-lookup"><span data-stu-id="2042b-183">Unique identifier correlating join time information for the different components involved in a conference.</span></span></p>
<p><span data-ttu-id="2042b-184">このフィールドは、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="2042b-184">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2042b-185"><strong>SessionSetupTime 時間</strong></span><span class="sxs-lookup"><span data-stu-id="2042b-185"><strong>SessionSetupTime</strong></span></span></p></td>
<td><p><span data-ttu-id="2042b-186">int</span><span class="sxs-lookup"><span data-stu-id="2042b-186">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="2042b-187">特定のコンポーネントが会議に参加するために必要な時間 (ミリ秒単位) です。</span><span class="sxs-lookup"><span data-stu-id="2042b-187">Time (in milliseconds) required for a specific component to join a conference.</span></span></p>
<p><span data-ttu-id="2042b-188">このフィールドは、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="2042b-188">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2042b-189"><strong>ServerId</strong></span><span class="sxs-lookup"><span data-stu-id="2042b-189"><strong>ServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="2042b-190">int</span><span class="sxs-lookup"><span data-stu-id="2042b-190">int</span></span></p></td>
<td><p><span data-ttu-id="2042b-191">外部</span><span class="sxs-lookup"><span data-stu-id="2042b-191">Foreign</span></span></p></td>
<td><p><span data-ttu-id="2042b-192">エラーレポートを生成したサーバーの完全修飾ドメイン名を表します。</span><span class="sxs-lookup"><span data-stu-id="2042b-192">Represents the fully qualified domain name of the server that generated the error report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2042b-193"><strong>PoolId</strong></span><span class="sxs-lookup"><span data-stu-id="2042b-193"><strong>PoolId</strong></span></span></p></td>
<td><p><span data-ttu-id="2042b-194">int</span><span class="sxs-lookup"><span data-stu-id="2042b-194">int</span></span></p></td>
<td><p><span data-ttu-id="2042b-195">外部</span><span class="sxs-lookup"><span data-stu-id="2042b-195">Foreign</span></span></p></td>
<td><p><span data-ttu-id="2042b-196">エラーレポートが生成されたプールの完全修飾ドメイン名を表します。</span><span class="sxs-lookup"><span data-stu-id="2042b-196">Represents the fully qualified domain name of the pool where the error report was generated.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="2042b-197">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2042b-197">


</div>

<span> </span>

</div>

</div>

</span></span></div>

