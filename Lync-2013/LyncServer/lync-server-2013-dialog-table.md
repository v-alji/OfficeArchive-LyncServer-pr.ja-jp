---
title: 'Lync Server 2013: Dialog テーブル'
description: 'Lync Server 2013: ダイアログテーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Dialog table
ms:assetid: 4d93424f-9072-43f5-83c2-3d539e3e9ca6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398313(v=OCS.15)
ms:contentKeyID: 48184068
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7ae93b8ca9f1146b7dc164803f27cbeeadc66777
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429204"
---
# <a name="dialog-table-in-lync-server-2013"></a><span data-ttu-id="90348-103">Lync Server 2013 の Dialog テーブル</span><span class="sxs-lookup"><span data-stu-id="90348-103">Dialog table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="90348-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="90348-104">

<span> </span></span></span>

<span data-ttu-id="90348-105">_**最終更新日:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="90348-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="90348-106">ダイアログテーブルはサポートテーブルです。各レコードは、1つのセッション開始プロトコル (SIP) ダイアログを表します。</span><span class="sxs-lookup"><span data-stu-id="90348-106">The Dialog table is a supporting table; each record represents one Session Initiation Protocol (SIP) dialog.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="90348-107"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="90348-107"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="90348-108"><strong>データ型</strong></span><span class="sxs-lookup"><span data-stu-id="90348-108"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="90348-109"><strong>キー/インデックス</strong></span><span class="sxs-lookup"><span data-stu-id="90348-109"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="90348-110"><strong>詳細</strong></span><span class="sxs-lookup"><span data-stu-id="90348-110"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="90348-111"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="90348-111"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="90348-112">datetime</span><span class="sxs-lookup"><span data-stu-id="90348-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="90348-113">Primary</span><span class="sxs-lookup"><span data-stu-id="90348-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="90348-114">卓越した品質 (QoE) エージェントが、呼び出し元または呼び出し元から最初のレポートを受け取る時刻。</span><span class="sxs-lookup"><span data-stu-id="90348-114">Time when the Quality of Excellence (QoE) agent receives the first report from either caller or callee.</span></span> <span data-ttu-id="90348-115">セッションを一意に識別するために SessionSeq と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="90348-115">Used in conjunction with SessionSeq to uniquely identify a session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90348-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="90348-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="90348-117">int</span><span class="sxs-lookup"><span data-stu-id="90348-117">int</span></span></p></td>
<td><p><span data-ttu-id="90348-118">Primary</span><span class="sxs-lookup"><span data-stu-id="90348-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="90348-119">セッションを区別するための順序番号 (同じ ConferenceDateTime がある場合)。</span><span class="sxs-lookup"><span data-stu-id="90348-119">Sequence number to differentiate sessions when they have the same ConferenceDateTime.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90348-120"><strong>この Id</strong></span><span class="sxs-lookup"><span data-stu-id="90348-120"><strong>DialogID</strong></span></span></p></td>
<td><p><span data-ttu-id="90348-121">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="90348-121">varchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="90348-122">グローバルに一意のダイアログ ID。</span><span class="sxs-lookup"><span data-stu-id="90348-122">Dialog ID which is globally unique.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90348-123"><strong>このチェックサム</strong></span><span class="sxs-lookup"><span data-stu-id="90348-123"><strong>DialogIDChecksum</strong></span></span></p></td>
<td><p><span data-ttu-id="90348-124">int</span><span class="sxs-lookup"><span data-stu-id="90348-124">int</span></span></p></td>
<td><p><span data-ttu-id="90348-125">位置</span><span class="sxs-lookup"><span data-stu-id="90348-125">index</span></span></p></td>
<td><p><span data-ttu-id="90348-126">ダイアログ ID のチェックサム。</span><span class="sxs-lookup"><span data-stu-id="90348-126">Checksum of the Dialog ID.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="90348-127">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="90348-127">


</div>

<span> </span>

</div>

</div>

</span></span></div>

