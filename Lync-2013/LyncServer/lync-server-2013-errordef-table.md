---
title: 'Lync Server 2013: ErrorDef テーブル'
description: 'Lync Server 2013: ErrorDef テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ErrorDef table
ms:assetid: 6acf3b86-da61-4923-9812-300db6f66dec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398503(v=OCS.15)
ms:contentKeyID: 48184403
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e58980a671b54007012bbbf6780e24c162aebe00
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428539"
---
# <a name="errordef-table-in-lync-server-2013"></a><span data-ttu-id="29f25-103">Lync Server 2013 ErrorDef テーブル</span><span class="sxs-lookup"><span data-stu-id="29f25-103">ErrorDef table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="29f25-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="29f25-104">

<span> </span></span></span>

<span data-ttu-id="29f25-105">_**最終更新日:** 2012-05-25_</span><span class="sxs-lookup"><span data-stu-id="29f25-105">_**Topic Last Modified:** 2012-05-25_</span></span>

<span data-ttu-id="29f25-106">ErrorDef テーブルには、発生する可能性がある各エラーの種類に関する情報が格納されます。</span><span class="sxs-lookup"><span data-stu-id="29f25-106">The ErrorDef table stores information about each type of error that may occur.</span></span> <span data-ttu-id="29f25-107">各レコードは1種類のエラーです。</span><span class="sxs-lookup"><span data-stu-id="29f25-107">Each record is one type of error.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="29f25-108">列</span><span class="sxs-lookup"><span data-stu-id="29f25-108">Column</span></span></th>
<th><span data-ttu-id="29f25-109">データ型</span><span class="sxs-lookup"><span data-stu-id="29f25-109">Data Type</span></span></th>
<th><span data-ttu-id="29f25-110">キー/インデックス</span><span class="sxs-lookup"><span data-stu-id="29f25-110">Key/Index</span></span></th>
<th><span data-ttu-id="29f25-111">詳細</span><span class="sxs-lookup"><span data-stu-id="29f25-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="29f25-112"><strong>ErrorId</strong></span><span class="sxs-lookup"><span data-stu-id="29f25-112"><strong>ErrorId</strong></span></span></p></td>
<td><p><span data-ttu-id="29f25-113">int</span><span class="sxs-lookup"><span data-stu-id="29f25-113">int</span></span></p></td>
<td><p><span data-ttu-id="29f25-114">Primary</span><span class="sxs-lookup"><span data-stu-id="29f25-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="29f25-115">この種類のエラーを識別する固有の ID 番号。</span><span class="sxs-lookup"><span data-stu-id="29f25-115">Unique ID number identifying this type of error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29f25-116"><strong>返信</strong></span><span class="sxs-lookup"><span data-stu-id="29f25-116"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="29f25-117">int</span><span class="sxs-lookup"><span data-stu-id="29f25-117">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="29f25-118">このエラーに関連付けられた標準 SIP 応答コード。</span><span class="sxs-lookup"><span data-stu-id="29f25-118">Standard SIP response code associated with this error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29f25-119"><strong>MsDiagId</strong></span><span class="sxs-lookup"><span data-stu-id="29f25-119"><strong>MsDiagId</strong></span></span></p></td>
<td><p><span data-ttu-id="29f25-120">int</span><span class="sxs-lookup"><span data-stu-id="29f25-120">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="29f25-121">Microsoft 診断 ID。</span><span class="sxs-lookup"><span data-stu-id="29f25-121">Microsoft Diagnostic ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29f25-122"><strong>発信者の Typeid</strong></span><span class="sxs-lookup"><span data-stu-id="29f25-122"><strong>CallTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="29f25-123">Int</span><span class="sxs-lookup"><span data-stu-id="29f25-123">Int</span></span></p></td>
<td><p><span data-ttu-id="29f25-124">外部</span><span class="sxs-lookup"><span data-stu-id="29f25-124">Foreign</span></span></p></td>
<td><p><span data-ttu-id="29f25-125">通話の種類。</span><span class="sxs-lookup"><span data-stu-id="29f25-125">Type of the call.</span></span> <span data-ttu-id="29f25-126">詳細については、「 <a href="lync-server-2013-calltype-table.md">Lync Server 2013 の CallType テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="29f25-126">See the <a href="lync-server-2013-calltype-table.md">CallType table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29f25-127"><strong>RequestType</strong></span><span class="sxs-lookup"><span data-stu-id="29f25-127"><strong>RequestType</strong></span></span></p></td>
<td><p><span data-ttu-id="29f25-128">varbinary (33)</span><span class="sxs-lookup"><span data-stu-id="29f25-128">varbinary(33)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="29f25-129">失敗した要求の種類。</span><span class="sxs-lookup"><span data-stu-id="29f25-129">Type of request that failed.</span></span></p>
<p><span data-ttu-id="29f25-130">このデータは、次の構文を使用してテキスト形式に変換できます。</span><span class="sxs-lookup"><span data-stu-id="29f25-130">This data can be converted to text format by using this syntax:</span></span></p>
<p><code>cast(cast(RequestType as varbinary(max)) as varchar(max))</code></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29f25-131"><strong>ContentType</strong></span><span class="sxs-lookup"><span data-stu-id="29f25-131"><strong>ContentType</strong></span></span></p></td>
<td><p><span data-ttu-id="29f25-132">varbinary (257)</span><span class="sxs-lookup"><span data-stu-id="29f25-132">varbinary(257)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="29f25-133">失敗した要求のコンテンツタイプ。</span><span class="sxs-lookup"><span data-stu-id="29f25-133">Content type of the request that failed.</span></span></p>
<p><span data-ttu-id="29f25-134">このデータは、次の syntaxt を使用してテキスト形式に変換できます。</span><span class="sxs-lookup"><span data-stu-id="29f25-134">This data can be converted to text format by using this syntaxt:</span></span></p>
<p><code>cast(cast(ContentType as varbinary(max)) as varchar(max))</code></p></td>
</tr>
</tbody>
</table><span data-ttu-id="29f25-135">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="29f25-135">


</div>

<span> </span>

</div>

</div>

</span></span></div>

