---
title: 'Lync Server 2013: ProgressReport テーブル'
description: 'Lync Server 2013: 進捗レポートのテーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ProgressReport table
ms:assetid: 38e5f060-5e9b-4185-87b2-7ef61c4bb75f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425864(v=OCS.15)
ms:contentKeyID: 48183847
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d36ee2ab75410ea2462da4b647ef5b45afefb1bb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436868"
---
# <a name="progressreport-table-in-lync-server-2013"></a><span data-ttu-id="a311d-103">Lync Server 2013 の ProgressReport テーブル</span><span class="sxs-lookup"><span data-stu-id="a311d-103">ProgressReport table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a311d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a311d-104">

<span> </span></span></span>

<span data-ttu-id="a311d-105">_**最終更新日:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="a311d-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="a311d-106">進行状況レポートは、呼び出しまたはセッションが完了した後に、クライアントからデータベースにアップロードされたデータに基づいています。</span><span class="sxs-lookup"><span data-stu-id="a311d-106">Progress reports are based on data uploaded by the client to the database after a call or session is completed.</span></span> <span data-ttu-id="a311d-107">進行状況レポートは、Lync Server 2013 で判別目的で役立つ可能性がある通話とセッションに対してのみ記録されます。</span><span class="sxs-lookup"><span data-stu-id="a311d-107">Progress reports will be written only for calls and sessions that Lync Server 2013 determines might be useful for diagnostic purposes.</span></span>

<span data-ttu-id="a311d-108">ErrorTime、ErrorReportSeq、進捗レポート Seq フィールドは、必ずしもエラーも参照しません。通話またはメッセージの状態を示すメッセージが表示されるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="a311d-108">The ErrorTime, ErrorReportSeq and ProgressReportSeq fields don’t necessarily refer to errors but to messages that indicate the status of calls or messages.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a311d-109">列</span><span class="sxs-lookup"><span data-stu-id="a311d-109">Column</span></span></th>
<th><span data-ttu-id="a311d-110">データ型</span><span class="sxs-lookup"><span data-stu-id="a311d-110">Data Type</span></span></th>
<th><span data-ttu-id="a311d-111">キー/インデックス</span><span class="sxs-lookup"><span data-stu-id="a311d-111">Key/Index</span></span></th>
<th><span data-ttu-id="a311d-112">詳細</span><span class="sxs-lookup"><span data-stu-id="a311d-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a311d-113"><strong>ErrorTime</strong></span><span class="sxs-lookup"><span data-stu-id="a311d-113"><strong>ErrorTime</strong></span></span></p></td>
<td><p><span data-ttu-id="a311d-114">datetime</span><span class="sxs-lookup"><span data-stu-id="a311d-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="a311d-115">プライマリ、外部</span><span class="sxs-lookup"><span data-stu-id="a311d-115">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="a311d-116">この進捗状況レポートが含まれる進捗状況エラーレポートの日付と時刻。</span><span class="sxs-lookup"><span data-stu-id="a311d-116">Date and time of the progress error report that contains this progress report.</span></span> <span data-ttu-id="a311d-117">詳細については、「 <a href="lync-server-2013-errorreport-table.md">Lync Server 2013 の ErrorReport テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a311d-117">See the <a href="lync-server-2013-errorreport-table.md">ErrorReport table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a311d-118"><strong>ErrorId</strong></span><span class="sxs-lookup"><span data-stu-id="a311d-118"><strong>ErrorId</strong></span></span></p></td>
<td><p><span data-ttu-id="a311d-119">int</span><span class="sxs-lookup"><span data-stu-id="a311d-119">int</span></span></p></td>
<td><p><span data-ttu-id="a311d-120">プライマリ、外部</span><span class="sxs-lookup"><span data-stu-id="a311d-120">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="a311d-121">ID 番号は、ErrorTime と共に使用されます。進捗レポートは、進行状況レポートを一意に識別するために使われます。</span><span class="sxs-lookup"><span data-stu-id="a311d-121">ID number used in conjunction with ErrorTime, ProgressReportSeq to uniquely identify a progress report.</span></span> <span data-ttu-id="a311d-122">詳細については、「 <a href="lync-server-2013-errorreport-table.md">Lync Server 2013 の ErrorReport テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a311d-122">See the <a href="lync-server-2013-errorreport-table.md">ErrorReport table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a311d-123"><strong>ErrorReportSeq</strong></span><span class="sxs-lookup"><span data-stu-id="a311d-123"><strong>ErrorReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="a311d-124">int</span><span class="sxs-lookup"><span data-stu-id="a311d-124">int</span></span></p></td>
<td><p><span data-ttu-id="a311d-125">プライマリ、外部</span><span class="sxs-lookup"><span data-stu-id="a311d-125">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="a311d-126">エラーレポートを識別する ID 番号。</span><span class="sxs-lookup"><span data-stu-id="a311d-126">ID number that identifies the error report.</span></span> <span data-ttu-id="a311d-127">エラーレポートを一意に識別するには、ErrorReporSeq と ErrorTime との組み合わせで使用されます。</span><span class="sxs-lookup"><span data-stu-id="a311d-127">ErrorReporSeq is used in conjunction with ErrorTime to uniquely identify an error report.</span></span> <span data-ttu-id="a311d-128">詳細については、「 <a href="lync-server-2013-errorreport-table.md">Lync Server 2013 の ErrorReport テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a311d-128">See the <a href="lync-server-2013-errorreport-table.md">ErrorReport table in Lync Server 2013</a> for more information</span></span></p>
<p><span data-ttu-id="a311d-129">このフィールドは、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="a311d-129">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a311d-130"><strong>進捗状況レポート Seq</strong></span><span class="sxs-lookup"><span data-stu-id="a311d-130"><strong>ProgressReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="a311d-131">int</span><span class="sxs-lookup"><span data-stu-id="a311d-131">int</span></span></p></td>
<td><p><span data-ttu-id="a311d-132">Primary</span><span class="sxs-lookup"><span data-stu-id="a311d-132">Primary</span></span></p></td>
<td><p><span data-ttu-id="a311d-133">進捗状況レポートを識別する ID 番号。</span><span class="sxs-lookup"><span data-stu-id="a311d-133">ID number to identify the progress report.</span></span> <span data-ttu-id="a311d-134">ErrorTime と ErrorReportSeq と組み合わせて、進行状況レポートを一意に識別するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="a311d-134">Used in conjunction with ErrorTime and ErrorReportSeq to uniquely identify a progress report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a311d-135"><strong>MsDiagId</strong></span><span class="sxs-lookup"><span data-stu-id="a311d-135"><strong>MsDiagId</strong></span></span></p></td>
<td><p><span data-ttu-id="a311d-136">int</span><span class="sxs-lookup"><span data-stu-id="a311d-136">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a311d-137">進行状況レポートの診断 ID。</span><span class="sxs-lookup"><span data-stu-id="a311d-137">Diagnostic ID of the progress report.</span></span></p>
<p><span data-ttu-id="a311d-138">このフィールドは、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="a311d-138">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a311d-139"><strong>SourceId</strong></span><span class="sxs-lookup"><span data-stu-id="a311d-139"><strong>SourceId</strong></span></span></p></td>
<td><p><span data-ttu-id="a311d-140">int</span><span class="sxs-lookup"><span data-stu-id="a311d-140">int</span></span></p></td>
<td><p><span data-ttu-id="a311d-141">外部</span><span class="sxs-lookup"><span data-stu-id="a311d-141">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a311d-142">エラーレポートを送信したサーバー (レポートがサーバーコンポーネントから送信された場合)。</span><span class="sxs-lookup"><span data-stu-id="a311d-142">Server that sent the error report (if the report was sent from a server component).</span></span> <span data-ttu-id="a311d-143">詳細については、「 <a href="lync-server-2013-servers-table.md">Lync Server 2013 のサーバーの表</a> 」を参照してください。このフィールドは、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="a311d-143">See the <a href="lync-server-2013-servers-table.md">Servers table in Lync Server 2013</a> for more information.This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a311d-144"><strong>ApplicationId</strong></span><span class="sxs-lookup"><span data-stu-id="a311d-144"><strong>ApplicationId</strong></span></span></p></td>
<td><p><span data-ttu-id="a311d-145">int</span><span class="sxs-lookup"><span data-stu-id="a311d-145">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a311d-146">レポートの作成に関する Lync Server プロセス。</span><span class="sxs-lookup"><span data-stu-id="a311d-146">The Lync Server process that the report is about.</span></span> <span data-ttu-id="a311d-147">詳しくは、アプリケーションの表をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="a311d-147">See the Application Table for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a311d-148"><strong>[詳細]</strong></span><span class="sxs-lookup"><span data-stu-id="a311d-148"><strong>Detail</strong></span></span></p></td>
<td><p><span data-ttu-id="a311d-149">画像</span><span class="sxs-lookup"><span data-stu-id="a311d-149">image</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a311d-150">サイズを節約するためのバイナリ形式で保存された進行状況レポートの詳細。このデータは、次の構文を使用してテキスト形式に変換できます。</span><span class="sxs-lookup"><span data-stu-id="a311d-150">Progress report details, stored in binary format to save space.This data can be converted to text format using this syntax:</span></span></p>
<p><span data-ttu-id="a311d-151">cast (cast (varbinary (max) としての Detail (max))</span><span class="sxs-lookup"><span data-stu-id="a311d-151">cast(cast(Detail as varbinary(max)) as varchar(max))</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a311d-152"><strong>TelemetryId</strong></span><span class="sxs-lookup"><span data-stu-id="a311d-152"><strong>TelemetryId</strong></span></span></p></td>
<td><p><span data-ttu-id="a311d-153">長さ</span><span class="sxs-lookup"><span data-stu-id="a311d-153">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a311d-154">会議に参加しているさまざまなコンポーネントの参加時間情報を関連付ける一意の識別子です。</span><span class="sxs-lookup"><span data-stu-id="a311d-154">Unique identifier that correlates join time information for the different components involved in a conference.</span></span></p>
<p><span data-ttu-id="a311d-155">このフィールドは、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="a311d-155">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a311d-156"><strong>SessionSetupTime 時間</strong></span><span class="sxs-lookup"><span data-stu-id="a311d-156"><strong>SessionSetupTime</strong></span></span></p></td>
<td><p><span data-ttu-id="a311d-157">int</span><span class="sxs-lookup"><span data-stu-id="a311d-157">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a311d-158">特定のコンポーネントが会議に参加するまでの時間 (ミリ秒単位) です。</span><span class="sxs-lookup"><span data-stu-id="a311d-158">Time (in milliseconds) for a specific component to join a conference.</span></span></p>
<p><span data-ttu-id="a311d-159">このフィールドは、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="a311d-159">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="a311d-160">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a311d-160">


</div>

<span> </span>

</div>

</div>

</span></span></div>

