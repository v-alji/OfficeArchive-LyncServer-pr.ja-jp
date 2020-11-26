---
title: 'Lync Server 2013: Mcu ビュー'
description: 'Lync Server 2013: Mcu ビュー。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Mcus view
ms:assetid: 8e8bbb1b-993b-4b66-862b-7e7654777203
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688127(v=OCS.15)
ms:contentKeyID: 49733725
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c2f72b4584696162496dcd91990edb086d558204
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425711"
---
# <a name="mcus-view-in-lync-server-2013"></a><span data-ttu-id="cb47c-103">Lync Server 2013 の mcu ビュー</span><span class="sxs-lookup"><span data-stu-id="cb47c-103">Mcus view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cb47c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cb47c-104">

<span> </span></span></span>

<span data-ttu-id="cb47c-105">_**最終更新日:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="cb47c-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="cb47c-106">Mcu ビューには、会議セッションに参加した Mcu に関する情報が格納されます。</span><span class="sxs-lookup"><span data-stu-id="cb47c-106">The Mcus view stores information about the MCUs that have participated in conference sessions.</span></span> <span data-ttu-id="cb47c-107">このビューは、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="cb47c-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cb47c-108">列</span><span class="sxs-lookup"><span data-stu-id="cb47c-108">Column</span></span></th>
<th><span data-ttu-id="cb47c-109">データ型</span><span class="sxs-lookup"><span data-stu-id="cb47c-109">Data Type</span></span></th>
<th><span data-ttu-id="cb47c-110">詳細</span><span class="sxs-lookup"><span data-stu-id="cb47c-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cb47c-111"><strong>McuId</strong></span><span class="sxs-lookup"><span data-stu-id="cb47c-111"><strong>McuId</strong></span></span></p></td>
<td><p><span data-ttu-id="cb47c-112">int</span><span class="sxs-lookup"><span data-stu-id="cb47c-112">int</span></span></p></td>
<td><p><span data-ttu-id="cb47c-113">MCU を識別する一意の番号。</span><span class="sxs-lookup"><span data-stu-id="cb47c-113">Unique number identifying the MCU.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb47c-114"><strong>McuUri</strong></span><span class="sxs-lookup"><span data-stu-id="cb47c-114"><strong>McuUri</strong></span></span></p></td>
<td><p><span data-ttu-id="cb47c-115">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="cb47c-115">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="cb47c-116">MCU の URI。</span><span class="sxs-lookup"><span data-stu-id="cb47c-116">URI of the MCU.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb47c-117"><strong>McuUriType</strong></span><span class="sxs-lookup"><span data-stu-id="cb47c-117"><strong>McuUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="cb47c-118">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="cb47c-118">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="cb47c-119">MCU URI の種類。</span><span class="sxs-lookup"><span data-stu-id="cb47c-119">Type of MCU URI.</span></span> <span data-ttu-id="cb47c-120">詳細については、「 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 の UriTypes テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cb47c-120">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="cb47c-121">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cb47c-121">


</div>

<span> </span>

</div>

</div>

</span></span></div>

