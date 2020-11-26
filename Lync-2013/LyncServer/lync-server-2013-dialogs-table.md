---
title: 'Lync Server 2013: Dialogs テーブル'
description: 'Lync Server 2013: Dialogs テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Dialogs table
ms:assetid: 487a430b-af66-4ea6-b28e-4e33cfdb7f9e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425954(v=OCS.15)
ms:contentKeyID: 48184001
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8c2c9cf9ec59fc48f7f5ffc6232980e3f8aa68c1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429183"
---
# <a name="dialogs-table-in-lync-server-2013"></a><span data-ttu-id="47213-103">Lync Server 2013 の Dialogs テーブル</span><span class="sxs-lookup"><span data-stu-id="47213-103">Dialogs table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="47213-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="47213-104">

<span> </span></span></span>

<span data-ttu-id="47213-105">_**最終更新日:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="47213-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="47213-106">Dialogs テーブルは、ピアツーピアセッションの DialogIDs に関する情報を格納するサポートテーブルです。</span><span class="sxs-lookup"><span data-stu-id="47213-106">The Dialogs table is a supporting table that stores the information about DialogIDs for peer-to-peer sessions.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="47213-107">列</span><span class="sxs-lookup"><span data-stu-id="47213-107">Column</span></span></th>
<th><span data-ttu-id="47213-108">データ型</span><span class="sxs-lookup"><span data-stu-id="47213-108">Data Type</span></span></th>
<th><span data-ttu-id="47213-109">キー/インデックス</span><span class="sxs-lookup"><span data-stu-id="47213-109">Key/Index</span></span></th>
<th><span data-ttu-id="47213-110">詳細</span><span class="sxs-lookup"><span data-stu-id="47213-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="47213-111"><strong>セッション Id</strong></span><span class="sxs-lookup"><span data-stu-id="47213-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="47213-112">datetime</span><span class="sxs-lookup"><span data-stu-id="47213-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="47213-113">Primary</span><span class="sxs-lookup"><span data-stu-id="47213-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="47213-114">セッション要求の時刻。セッションを一意に識別するために SessionIDSeq と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="47213-114">Time of session request; used in conjunction with SessionIDSeq to uniquely identify a session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47213-115"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="47213-115"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="47213-116">int</span><span class="sxs-lookup"><span data-stu-id="47213-116">int</span></span></p></td>
<td><p><span data-ttu-id="47213-117">Primary</span><span class="sxs-lookup"><span data-stu-id="47213-117">Primary</span></span></p></td>
<td><p><span data-ttu-id="47213-118">セッションを識別する ID 番号。</span><span class="sxs-lookup"><span data-stu-id="47213-118">ID number to identify the session.</span></span> <span data-ttu-id="47213-119">セッションを一意に識別するために SessionIDTime と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="47213-119">Used in conjunction with SessionIDTime to uniquely identify a session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47213-120"><strong>ExternalChecksum</strong></span><span class="sxs-lookup"><span data-stu-id="47213-120"><strong>ExternalChecksum</strong></span></span></p></td>
<td><p><span data-ttu-id="47213-121">int</span><span class="sxs-lookup"><span data-stu-id="47213-121">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="47213-122">ExternalID のチェックサム。</span><span class="sxs-lookup"><span data-stu-id="47213-122">Checksum of the ExternalID.</span></span> <span data-ttu-id="47213-123">このフィールドは、データベースの検索速度を上げるために使用されます。</span><span class="sxs-lookup"><span data-stu-id="47213-123">This field is used to increase the speed of database searches.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47213-124"><strong>ExternalId</strong></span><span class="sxs-lookup"><span data-stu-id="47213-124"><strong>ExternalId</strong></span></span></p></td>
<td><p><span data-ttu-id="47213-125">varbinary (775)</span><span class="sxs-lookup"><span data-stu-id="47213-125">varbinary(775)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="47213-126">SIP ダイアログ ID。バイナリとして保存されます。</span><span class="sxs-lookup"><span data-stu-id="47213-126">SIP dialog ID, stored as a binary.</span></span> <span data-ttu-id="47213-127">バイナリの形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="47213-127">The format of the binary is:</span></span></p>
<p><span data-ttu-id="47213-128">ダイアログ; 開始タグからタグへ</span><span class="sxs-lookup"><span data-stu-id="47213-128">dialog;from-tag;to-tag</span></span></p>
<p><span data-ttu-id="47213-129">このデータは、次の構文を使用してテキスト形式に変換できます。</span><span class="sxs-lookup"><span data-stu-id="47213-129">This data can be converted to text format by using this syntax:</span></span></p>
<p><code>cast(cast(ExternalId as varbinary(max)) as varchar(max))</code></p></td>
</tr>
</tbody>
</table><span data-ttu-id="47213-130">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="47213-130">


</div>

<span> </span>

</div>

</div>

</span></span></div>

