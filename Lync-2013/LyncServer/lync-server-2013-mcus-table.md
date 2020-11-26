---
title: 'Lync Server 2013: Mcus テーブル'
description: 'Lync Server 2013: Mcu テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Mcus table
ms:assetid: 271b7963-8fd8-4d92-a701-1a62aaf895ee
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425742(v=OCS.15)
ms:contentKeyID: 48183674
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b0b5d0bcbebb5efc1d767776b4581b18d9f2ed18
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425746"
---
# <a name="mcus-table-in-lync-server-2013"></a><span data-ttu-id="7359b-103">Lync Server 2013 の Mcus テーブル</span><span class="sxs-lookup"><span data-stu-id="7359b-103">Mcus table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7359b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7359b-104">

<span> </span></span></span>

<span data-ttu-id="7359b-105">_**最終更新日:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="7359b-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="7359b-106">Mcu テーブルは、サポートテーブルです。</span><span class="sxs-lookup"><span data-stu-id="7359b-106">The Mcus table is a supporting table.</span></span> <span data-ttu-id="7359b-107">各レコードには、1つの会議サービスに関する情報が格納されます。</span><span class="sxs-lookup"><span data-stu-id="7359b-107">Each record stores information about one conferencing service.</span></span> <span data-ttu-id="7359b-108">これには、IM 会議サービスと、(フロントエンドサーバーでプロセスとして実行される) テレフォニー会議サービス、および Web 会議サービスと A/V 会議サービスを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="7359b-108">These can include the IM Conferencing service and the Telephony Conferencing service (which run as processes on front-end servers), and the Web Conferencing service and A/V Conferencing service.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7359b-109">列</span><span class="sxs-lookup"><span data-stu-id="7359b-109">Column</span></span></th>
<th><span data-ttu-id="7359b-110">データ型</span><span class="sxs-lookup"><span data-stu-id="7359b-110">Data Type</span></span></th>
<th><span data-ttu-id="7359b-111">キー/インデックス</span><span class="sxs-lookup"><span data-stu-id="7359b-111">Key/Index</span></span></th>
<th><span data-ttu-id="7359b-112">詳細</span><span class="sxs-lookup"><span data-stu-id="7359b-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7359b-113"><strong>McuId</strong></span><span class="sxs-lookup"><span data-stu-id="7359b-113"><strong>McuId</strong></span></span></p></td>
<td><p><span data-ttu-id="7359b-114">int</span><span class="sxs-lookup"><span data-stu-id="7359b-114">int</span></span></p></td>
<td><p><span data-ttu-id="7359b-115">Primary</span><span class="sxs-lookup"><span data-stu-id="7359b-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="7359b-116">この会議サーバーを識別する一意の番号です。</span><span class="sxs-lookup"><span data-stu-id="7359b-116">Unique number identifying this conferencing server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7359b-117"><strong>McuUri</strong></span><span class="sxs-lookup"><span data-stu-id="7359b-117"><strong>McuUri</strong></span></span></p></td>
<td><p><span data-ttu-id="7359b-118">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="7359b-118">nvarchar(450)</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7359b-119"><strong>McuTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="7359b-119"><strong>McuTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="7359b-120">inyint</span><span class="sxs-lookup"><span data-stu-id="7359b-120">inyint</span></span></p></td>
<td><p> <span data-ttu-id="7359b-121">外部</span><span class="sxs-lookup"><span data-stu-id="7359b-121">Foreign</span></span></p></td>
<td><p><span data-ttu-id="7359b-122">会議サーバーの種類 (例: チャット (Im の場合) または conf: オーディオビデオ)。</span><span class="sxs-lookup"><span data-stu-id="7359b-122">Conferencing server type, such as conf:chat (for IMs) or conf:audio-video.</span></span> <span data-ttu-id="7359b-123">詳細については、「 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 の UriTypes テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7359b-123">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="7359b-124">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7359b-124">


</div>

<span> </span>

</div>

</div>

</span></span></div>

