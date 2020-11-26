---
title: 'Lync Server 2013: UserStatistics テーブル'
description: 'Lync Server 2013: UserStatistics テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: UserStatistics table
ms:assetid: cfaf803b-1679-4169-92d3-533fad3e56ed
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721893(v=OCS.15)
ms:contentKeyID: 49733827
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 75b34fa3c34af4cc9cf2cacc6ae7feb4d217114c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436098"
---
# <a name="userstatistics-table-in-lync-server-2013"></a><span data-ttu-id="680ff-103">Lync Server 2013 の UserStatistics テーブル</span><span class="sxs-lookup"><span data-stu-id="680ff-103">UserStatistics table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="680ff-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="680ff-104">

<span> </span></span></span>

<span data-ttu-id="680ff-105">_**最終更新日:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="680ff-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="680ff-106">UserStatistics テーブルは、サポートテーブルです。</span><span class="sxs-lookup"><span data-stu-id="680ff-106">The UserStatistics table is a supporting table.</span></span> <span data-ttu-id="680ff-107">テーブルの各レコードには、個々のユーザーによるシステムの使用状況に関する情報が格納されます。</span><span class="sxs-lookup"><span data-stu-id="680ff-107">Each record in the table stores information about an individual user’s usage of the system.</span></span> <span data-ttu-id="680ff-108">この表は、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="680ff-108">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="680ff-109">列</span><span class="sxs-lookup"><span data-stu-id="680ff-109">Column</span></span></th>
<th><span data-ttu-id="680ff-110">データ型</span><span class="sxs-lookup"><span data-stu-id="680ff-110">Data Type</span></span></th>
<th><span data-ttu-id="680ff-111">キー/インデックス</span><span class="sxs-lookup"><span data-stu-id="680ff-111">Key/Index</span></span></th>
<th><span data-ttu-id="680ff-112">詳細</span><span class="sxs-lookup"><span data-stu-id="680ff-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="680ff-113"><strong>UserId</strong></span><span class="sxs-lookup"><span data-stu-id="680ff-113"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="680ff-114">int</span><span class="sxs-lookup"><span data-stu-id="680ff-114">int</span></span></p></td>
<td><p><span data-ttu-id="680ff-115">Primary</span><span class="sxs-lookup"><span data-stu-id="680ff-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="680ff-116">このユーザーを識別する一意の番号です。</span><span class="sxs-lookup"><span data-stu-id="680ff-116">Unique number identifying this user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="680ff-117"><strong>最終ログイン時間</strong></span><span class="sxs-lookup"><span data-stu-id="680ff-117"><strong>LastLogInTime</strong></span></span></p></td>
<td><p><span data-ttu-id="680ff-118">datetime</span><span class="sxs-lookup"><span data-stu-id="680ff-118">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="680ff-119">前回ユーザーがログインした日時。</span><span class="sxs-lookup"><span data-stu-id="680ff-119">Last time the user logged in.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="680ff-120"><strong>Lastconforizedtime</strong></span><span class="sxs-lookup"><span data-stu-id="680ff-120"><strong>LastConfOrganizedTime</strong></span></span></p></td>
<td><p><span data-ttu-id="680ff-121">datetime</span><span class="sxs-lookup"><span data-stu-id="680ff-121">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="680ff-122">ユーザーが最後に会議を開催した日時。</span><span class="sxs-lookup"><span data-stu-id="680ff-122">Last time the user organized a conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="680ff-123"><strong>Lastcallオーガナイザー Ercallfailuretime</strong></span><span class="sxs-lookup"><span data-stu-id="680ff-123"><strong>LastCallOrganizerCallFailureTime</strong></span></span></p></td>
<td><p><span data-ttu-id="680ff-124">datetime</span><span class="sxs-lookup"><span data-stu-id="680ff-124">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="680ff-125">前回ユーザーが通話の失敗を経験した日時。</span><span class="sxs-lookup"><span data-stu-id="680ff-125">Last time the user experienced a call failure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="680ff-126"><strong>Lastconforガント Izercallfailuretime</strong></span><span class="sxs-lookup"><span data-stu-id="680ff-126"><strong>LastConfOrganizerCallFailureTime</strong></span></span></p></td>
<td><p><span data-ttu-id="680ff-127">datetime</span><span class="sxs-lookup"><span data-stu-id="680ff-127">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="680ff-128">前回ユーザーが会議開催者として通話の失敗を経験した時刻。</span><span class="sxs-lookup"><span data-stu-id="680ff-128">Last time the user experienced a call failure as a conference organizer.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="680ff-129">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="680ff-129">


</div>

<span> </span>

</div>

</div>

</span></span></div>

