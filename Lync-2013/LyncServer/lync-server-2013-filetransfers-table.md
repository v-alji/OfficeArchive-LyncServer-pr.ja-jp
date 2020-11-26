---
title: 'Lync Server 2013: FileTransfers テーブル'
description: 'Lync Server 2013: FileTransfers テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: FileTransfers table
ms:assetid: 5368e67c-d8a9-43a1-9472-a839950dedb3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398353(v=OCS.15)
ms:contentKeyID: 48184118
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ccde45fa3743a809499273676d567846ef292ecc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428168"
---
# <a name="filetransfers-table-in-lync-server-2013"></a><span data-ttu-id="a6c47-103">Lync Server 2013 の FileTransfers テーブル</span><span class="sxs-lookup"><span data-stu-id="a6c47-103">FileTransfers table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a6c47-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a6c47-104">

<span> </span></span></span>

<span data-ttu-id="a6c47-105">_**最終更新日:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="a6c47-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="a6c47-106">各レコードは、1つのファイル転送セッションを表します。</span><span class="sxs-lookup"><span data-stu-id="a6c47-106">Each record represents one file transfer session.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a6c47-107">列</span><span class="sxs-lookup"><span data-stu-id="a6c47-107">Column</span></span></th>
<th><span data-ttu-id="a6c47-108">データ型</span><span class="sxs-lookup"><span data-stu-id="a6c47-108">Data Type</span></span></th>
<th><span data-ttu-id="a6c47-109">キー/インデックス</span><span class="sxs-lookup"><span data-stu-id="a6c47-109">Key/Index</span></span></th>
<th><span data-ttu-id="a6c47-110">詳細</span><span class="sxs-lookup"><span data-stu-id="a6c47-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a6c47-111"><strong>セッション Id</strong></span><span class="sxs-lookup"><span data-stu-id="a6c47-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="a6c47-112">datetime</span><span class="sxs-lookup"><span data-stu-id="a6c47-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="a6c47-113">プライマリ、外部</span><span class="sxs-lookup"><span data-stu-id="a6c47-113">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="a6c47-114">セッション要求の時刻。</span><span class="sxs-lookup"><span data-stu-id="a6c47-114">Time of session request.</span></span> <span data-ttu-id="a6c47-115">セッションを一意に識別するために <strong>Sessionidseq</strong> と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="a6c47-115">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="a6c47-116">詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a6c47-116">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6c47-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="a6c47-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="a6c47-118">int</span><span class="sxs-lookup"><span data-stu-id="a6c47-118">int</span></span></p></td>
<td><p><span data-ttu-id="a6c47-119">プライマリ、外部</span><span class="sxs-lookup"><span data-stu-id="a6c47-119">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="a6c47-120">セッションを識別する ID 番号。</span><span class="sxs-lookup"><span data-stu-id="a6c47-120">ID number to identify the session.</span></span> <span data-ttu-id="a6c47-121">セッションを一意に識別するために <strong>Sessionidtime</strong> と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="a6c47-121">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="a6c47-122">詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a6c47-122">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6c47-123"><strong>ファイル名</strong></span><span class="sxs-lookup"><span data-stu-id="a6c47-123"><strong>File Name</strong></span></span></p></td>
<td><p><span data-ttu-id="a6c47-124">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="a6c47-124">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a6c47-125">ファイルの名前。</span><span class="sxs-lookup"><span data-stu-id="a6c47-125">Name of the file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6c47-126"><strong>FileIdentity</strong></span><span class="sxs-lookup"><span data-stu-id="a6c47-126"><strong>FileIdentity</strong></span></span></p></td>
<td><p><span data-ttu-id="a6c47-127">長さ</span><span class="sxs-lookup"><span data-stu-id="a6c47-127">uniqueidentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a6c47-128">同じファイル名を含むファイル転送を区別する一意の識別子。</span><span class="sxs-lookup"><span data-stu-id="a6c47-128">Unique identifier to distinguish between file transfers involving the same file name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6c47-129"><strong>クッキー</strong></span><span class="sxs-lookup"><span data-stu-id="a6c47-129"><strong>Cookie</strong></span></span></p></td>
<td><p><span data-ttu-id="a6c47-130">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="a6c47-130">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="a6c47-131">Primary</span><span class="sxs-lookup"><span data-stu-id="a6c47-131">Primary</span></span></p></td>
<td><p><span data-ttu-id="a6c47-132">すべてのフォローアップメッセージをこのメールに関連付けられているものとして識別するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="a6c47-132">Used to identify every follow-up message as being associated with this one.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6c47-133"><strong>受諾</strong></span><span class="sxs-lookup"><span data-stu-id="a6c47-133"><strong>Accept</strong></span></span></p></td>
<td><p><span data-ttu-id="a6c47-134">bit</span><span class="sxs-lookup"><span data-stu-id="a6c47-134">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a6c47-135">TRUE または NULL を指定できます。</span><span class="sxs-lookup"><span data-stu-id="a6c47-135">Can be TRUE or NULL.</span></span> <span data-ttu-id="a6c47-136">TRUE の場合は、拒否とキャンセルは NULL になります。</span><span class="sxs-lookup"><span data-stu-id="a6c47-136">If TRUE, then Reject and Cancel will be NULL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6c47-137"><strong>拒否</strong></span><span class="sxs-lookup"><span data-stu-id="a6c47-137"><strong>Reject</strong></span></span></p></td>
<td><p><span data-ttu-id="a6c47-138">bit</span><span class="sxs-lookup"><span data-stu-id="a6c47-138">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a6c47-139">TRUE または NULL を指定できます。</span><span class="sxs-lookup"><span data-stu-id="a6c47-139">Can be TRUE or NULL.</span></span> <span data-ttu-id="a6c47-140">TRUE の場合は、Accept と Cancel は NULL になります。</span><span class="sxs-lookup"><span data-stu-id="a6c47-140">If TRUE, then Accept and Cancel will be NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6c47-141"><strong>キャンセル</strong></span><span class="sxs-lookup"><span data-stu-id="a6c47-141"><strong>Cancel</strong></span></span></p></td>
<td><p><span data-ttu-id="a6c47-142">bit</span><span class="sxs-lookup"><span data-stu-id="a6c47-142">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a6c47-143">TRUE または NULL を指定できます。</span><span class="sxs-lookup"><span data-stu-id="a6c47-143">Can be TRUE or NULL.</span></span> <span data-ttu-id="a6c47-144">TRUE の場合は、Accept と Reject は NULL になります。</span><span class="sxs-lookup"><span data-stu-id="a6c47-144">If TRUE, then Accept and Reject will be NULL.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="a6c47-145">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a6c47-145">


</div>

<span> </span>

</div>

</div>

</span></span></div>

