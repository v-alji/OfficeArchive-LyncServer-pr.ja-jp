---
title: 'Lync Server 2013: 進捗状況レポートビュー'
description: 'Lync Server 2013: 進捗状況レポートビュー。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ProgressReport view
ms:assetid: b49f3fc7-0e2f-498f-8505-aaaf54e435f9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721857(v=OCS.15)
ms:contentKeyID: 49733790
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b95086012f254499644e778e43cafdf70ffc8f9c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436854"
---
# <a name="progressreport-view-in-lync-server-2013"></a><span data-ttu-id="7a866-103">Lync Server 2013 の進捗状況レポートビュー</span><span class="sxs-lookup"><span data-stu-id="7a866-103">ProgressReport view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7a866-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7a866-104">

<span> </span></span></span>

<span data-ttu-id="7a866-105">_**最終更新日:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="7a866-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="7a866-106">進捗レポートビューには、完了したセッションに関する情報が格納されます。</span><span class="sxs-lookup"><span data-stu-id="7a866-106">The ProgressReport view stores information about completed sessions.</span></span> <span data-ttu-id="7a866-107">進行状況レポートは、Lync Server 2013 で判別目的で役立つ可能性がある通話とセッションに対してのみ記録されます。</span><span class="sxs-lookup"><span data-stu-id="7a866-107">Progress reports will be written only for calls and sessions that Lync Server 2013 determines might be useful for diagnostic purposes.</span></span> <span data-ttu-id="7a866-108">このビューは、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="7a866-108">This view was introduced in Microsoft Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="7a866-109">ErrorTime、ErrorReportSeq、進捗レポート Seq フィールドは、必ずしもエラーも参照しません。通話またはメッセージの状態を示すメッセージが表示されるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="7a866-109">The ErrorTime, ErrorReportSeq and ProgressReportSeq fields don’t necessarily refer to errors but to messages that indicate the status of calls or messages.</span></span>



</div>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7a866-110">列</span><span class="sxs-lookup"><span data-stu-id="7a866-110">Column</span></span></th>
<th><span data-ttu-id="7a866-111">データ型</span><span class="sxs-lookup"><span data-stu-id="7a866-111">Data Type</span></span></th>
<th><span data-ttu-id="7a866-112">詳細</span><span class="sxs-lookup"><span data-stu-id="7a866-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7a866-113"><strong>ErrorTime</strong></span><span class="sxs-lookup"><span data-stu-id="7a866-113"><strong>ErrorTime</strong></span></span></p></td>
<td><p><span data-ttu-id="7a866-114">datetime</span><span class="sxs-lookup"><span data-stu-id="7a866-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="7a866-115">エラーが発生した時刻。</span><span class="sxs-lookup"><span data-stu-id="7a866-115">Time of error occurred.</span></span> <span data-ttu-id="7a866-116">エラーを一意に識別するには、ErrorReportSeq と組み合わせて使います。</span><span class="sxs-lookup"><span data-stu-id="7a866-116">Used in conjunction with ErrorReportSeq to uniquely identify an error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a866-117"><strong>ErrorReportSeq</strong></span><span class="sxs-lookup"><span data-stu-id="7a866-117"><strong>ErrorReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="7a866-118">int</span><span class="sxs-lookup"><span data-stu-id="7a866-118">int</span></span></p></td>
<td><p><span data-ttu-id="7a866-119">エラーを識別する ID 番号。</span><span class="sxs-lookup"><span data-stu-id="7a866-119">ID number to identify the error.</span></span> <span data-ttu-id="7a866-120">エラーを一意に識別するための ErrorTime と共に使用されます。</span><span class="sxs-lookup"><span data-stu-id="7a866-120">Used in conjunction with ErrorTime to uniquely identify an error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a866-121"><strong>進捗状況レポート Seq</strong></span><span class="sxs-lookup"><span data-stu-id="7a866-121"><strong>ProgressReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="7a866-122">int</span><span class="sxs-lookup"><span data-stu-id="7a866-122">int</span></span></p></td>
<td><p><span data-ttu-id="7a866-123">進行状況レポートを識別する ID。</span><span class="sxs-lookup"><span data-stu-id="7a866-123">ID to identify the progress report.</span></span> <span data-ttu-id="7a866-124">同じエラーレポートの進行状況レポートを区別するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7a866-124">Used to distinguish progress reports of the same error report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a866-125"><strong>MsDiagId</strong></span><span class="sxs-lookup"><span data-stu-id="7a866-125"><strong>MsDiagId</strong></span></span></p></td>
<td><p><span data-ttu-id="7a866-126">int</span><span class="sxs-lookup"><span data-stu-id="7a866-126">int</span></span></p></td>
<td><p><span data-ttu-id="7a866-127">エラーレポートの診断 ID。</span><span class="sxs-lookup"><span data-stu-id="7a866-127">Diagnostic ID for the error report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a866-128"><strong>ソース</strong></span><span class="sxs-lookup"><span data-stu-id="7a866-128"><strong>Source</strong></span></span></p></td>
<td><p><span data-ttu-id="7a866-129">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="7a866-129">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7a866-130">エラーが発生したサーバーの名前 (サーバーコンポーネントからレポートが送信された場合)。</span><span class="sxs-lookup"><span data-stu-id="7a866-130">Name of server that originated the error (if report was sent from a server component).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a866-131"><strong>Application</strong></span><span class="sxs-lookup"><span data-stu-id="7a866-131"><strong>Application</strong></span></span></p></td>
<td><p><span data-ttu-id="7a866-132">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="7a866-132">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7a866-133">エラーの発生元のアプリケーションの名前 (サーバーコンポーネントからレポートが送信された場合)。</span><span class="sxs-lookup"><span data-stu-id="7a866-133">Name of application that originated the error (if report was sent from a server component).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a866-134"><strong>TelemetryId</strong></span><span class="sxs-lookup"><span data-stu-id="7a866-134"><strong>TelemetryId</strong></span></span></p></td>
<td><p><span data-ttu-id="7a866-135">長さ</span><span class="sxs-lookup"><span data-stu-id="7a866-135">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="7a866-136">電話会議に参加しているさまざまなコンポーネントについての、固有の識別子による結合時間情報の関連付け。</span><span class="sxs-lookup"><span data-stu-id="7a866-136">Unique identifier correlating join time information for the different components involved in a conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a866-137"><strong>SessionSetupTime 時間</strong></span><span class="sxs-lookup"><span data-stu-id="7a866-137"><strong>SessionSetupTime</strong></span></span></p></td>
<td><p><span data-ttu-id="7a866-138">int</span><span class="sxs-lookup"><span data-stu-id="7a866-138">int</span></span></p></td>
<td><p><span data-ttu-id="7a866-139">特定のコンポーネントが会議に参加するために必要な時間 (ミリ秒単位) です。</span><span class="sxs-lookup"><span data-stu-id="7a866-139">Time (in milliseconds) required for a specific component to join a conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a866-140"><strong>MsDiagHeader</strong></span><span class="sxs-lookup"><span data-stu-id="7a866-140"><strong>MsDiagHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="7a866-141">varchar (max)</span><span class="sxs-lookup"><span data-stu-id="7a866-141">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="7a866-142">追加のエラー情報。</span><span class="sxs-lookup"><span data-stu-id="7a866-142">Additional error information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="7a866-143">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7a866-143">


</div>

<span> </span>

</div>

</div>

</span></span></div>

