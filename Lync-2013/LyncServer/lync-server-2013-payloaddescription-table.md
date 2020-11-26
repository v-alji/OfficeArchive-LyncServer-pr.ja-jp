---
title: 'Lync Server 2013: PayloadDescription テーブル'
description: 'Lync Server 2013: PayloadDescription テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: PayloadDescription table
ms:assetid: c49d61c0-305a-4770-a5d2-5d9f05decc6d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412971(v=OCS.15)
ms:contentKeyID: 48185353
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 90ba6b3b85060601487b5b6d0d8747c5fbfa2a9a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445051"
---
# <a name="payloaddescription-table-in-lync-server-2013"></a><span data-ttu-id="d614d-103">Lync Server 2013 の PayloadDescription テーブル</span><span class="sxs-lookup"><span data-stu-id="d614d-103">PayloadDescription table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d614d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d614d-104">

<span> </span></span></span>

<span data-ttu-id="d614d-105">_**最終更新日:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="d614d-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="d614d-106">PayloadDescription テーブルは、サポートテーブルです。</span><span class="sxs-lookup"><span data-stu-id="d614d-106">The PayloadDescription table is a supporting table.</span></span> <span data-ttu-id="d614d-107">各レコードは、オーディオセッションまたはビデオセッションで使用される1つのコーデックを表します。</span><span class="sxs-lookup"><span data-stu-id="d614d-107">Each record represents one Codec, which is used in an audio or video session.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d614d-108"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="d614d-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="d614d-109"><strong>データ型</strong></span><span class="sxs-lookup"><span data-stu-id="d614d-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="d614d-110"><strong>キー/インデックス</strong></span><span class="sxs-lookup"><span data-stu-id="d614d-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="d614d-111"><strong>詳細</strong></span><span class="sxs-lookup"><span data-stu-id="d614d-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d614d-112"><strong>PayloadDescriptionKey</strong></span><span class="sxs-lookup"><span data-stu-id="d614d-112"><strong>PayloadDescriptionKey</strong></span></span></p></td>
<td><p><span data-ttu-id="d614d-113">int</span><span class="sxs-lookup"><span data-stu-id="d614d-113">int</span></span></p></td>
<td><p><span data-ttu-id="d614d-114">Primary</span><span class="sxs-lookup"><span data-stu-id="d614d-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="d614d-115">コーデックを識別する一意の番号。</span><span class="sxs-lookup"><span data-stu-id="d614d-115">Unique number identifying the Codec.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d614d-116"><strong>PayloadDescription</strong></span><span class="sxs-lookup"><span data-stu-id="d614d-116"><strong>PayloadDescription</strong></span></span></p></td>
<td><p><span data-ttu-id="d614d-117">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d614d-117">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d614d-118">一意</span><span class="sxs-lookup"><span data-stu-id="d614d-118">Unique</span></span></p></td>
<td><p><span data-ttu-id="d614d-119">コーデック名。</span><span class="sxs-lookup"><span data-stu-id="d614d-119">Codec name.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="d614d-120">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d614d-120">


</div>

<span> </span>

</div>

</div>

</span></span></div>

