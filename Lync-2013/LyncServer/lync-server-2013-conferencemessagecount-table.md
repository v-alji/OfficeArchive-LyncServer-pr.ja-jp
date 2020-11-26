---
title: 'Lync Server 2013: ConferenceMessageCount テーブル'
description: 'Lync Server 2013: ConferenceMessageCount テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ConferenceMessageCount table
ms:assetid: 78569dbf-5217-42fa-ba1a-4380f56e2a3d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398590(v=OCS.15)
ms:contentKeyID: 48184570
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 271b654c09ab1aef194eb613e660de208aea1534
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434453"
---
# <a name="conferencemessagecount-table-in-lync-server-2013"></a><span data-ttu-id="09cf5-103">Lync Server 2013 の ConferenceMessageCount テーブル</span><span class="sxs-lookup"><span data-stu-id="09cf5-103">ConferenceMessageCount table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="09cf5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="09cf5-104">

<span> </span></span></span>

<span data-ttu-id="09cf5-105">_**最終更新日:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="09cf5-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="09cf5-106">このテーブル内の各レコードは、1人の IM 会議で1人のユーザーを表し、そのユーザーから送信されたメッセージの数が含まれます。</span><span class="sxs-lookup"><span data-stu-id="09cf5-106">Each record in this table represents one user in one IM conference and includes the number of messages sent by that user.</span></span> <span data-ttu-id="09cf5-107">各会議は、この表の複数のレコードで表されます。ユーザーごとに1つのレコード。</span><span class="sxs-lookup"><span data-stu-id="09cf5-107">Each conference is represented by multiple records in this table; one record for each user.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="09cf5-108">列</span><span class="sxs-lookup"><span data-stu-id="09cf5-108">Column</span></span></th>
<th><span data-ttu-id="09cf5-109">データ型</span><span class="sxs-lookup"><span data-stu-id="09cf5-109">Data Type</span></span></th>
<th><span data-ttu-id="09cf5-110">キー/インデックス</span><span class="sxs-lookup"><span data-stu-id="09cf5-110">Key/Index</span></span></th>
<th><span data-ttu-id="09cf5-111">詳細</span><span class="sxs-lookup"><span data-stu-id="09cf5-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09cf5-112"><strong>セッション Id</strong></span><span class="sxs-lookup"><span data-stu-id="09cf5-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="09cf5-113">datetime</span><span class="sxs-lookup"><span data-stu-id="09cf5-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="09cf5-114">プライマリ、外部</span><span class="sxs-lookup"><span data-stu-id="09cf5-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="09cf5-115">会議インスタンスの時刻。</span><span class="sxs-lookup"><span data-stu-id="09cf5-115">Time of conference instance.</span></span> <span data-ttu-id="09cf5-116">電話会議インスタンスを一意に識別するために <strong>Sessionidseq</strong> と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="09cf5-116">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a conference instance.</span></span> <span data-ttu-id="09cf5-117">詳細については、「 <a href="lync-server-2013-conferences-table.md">Lync Server 2013 での会議の表</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="09cf5-117">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09cf5-118"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="09cf5-118"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="09cf5-119">int</span><span class="sxs-lookup"><span data-stu-id="09cf5-119">int</span></span></p></td>
<td><p><span data-ttu-id="09cf5-120">プライマリ、外部</span><span class="sxs-lookup"><span data-stu-id="09cf5-120">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="09cf5-121">会議インスタンスを識別する ID 番号。</span><span class="sxs-lookup"><span data-stu-id="09cf5-121">ID number to identify the conference instance.</span></span> <span data-ttu-id="09cf5-122">電話会議インスタンスを一意に識別するために <strong>Sessionidtime</strong> と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="09cf5-122">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a conference instance.</span></span> <span data-ttu-id="09cf5-123">詳細については、「 <a href="lync-server-2013-conferences-table.md">Lync Server 2013 での会議の表</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="09cf5-123">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09cf5-124"><strong>UserId</strong></span><span class="sxs-lookup"><span data-stu-id="09cf5-124"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="09cf5-125">int</span><span class="sxs-lookup"><span data-stu-id="09cf5-125">int</span></span></p></td>
<td><p><span data-ttu-id="09cf5-126">外部</span><span class="sxs-lookup"><span data-stu-id="09cf5-126">Foreign</span></span></p></td>
<td><p><span data-ttu-id="09cf5-127">このユーザーを識別する一意の番号です。 <a href="lync-server-2013-users-table.md">Lync Server 2013 の [ユーザー] テーブル</a>から参照されます。</span><span class="sxs-lookup"><span data-stu-id="09cf5-127">Unique number identifying this user, referenced from the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09cf5-128"><strong>MessageCount</strong></span><span class="sxs-lookup"><span data-stu-id="09cf5-128"><strong>MessageCount</strong></span></span></p></td>
<td><p><span data-ttu-id="09cf5-129">smallint</span><span class="sxs-lookup"><span data-stu-id="09cf5-129">smallint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="09cf5-130">この会議中にこのユーザーによって送信されたメッセージの数です。</span><span class="sxs-lookup"><span data-stu-id="09cf5-130">The number of messages sent by this user during this conference.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="09cf5-131">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="09cf5-131">


</div>

<span> </span>

</div>

</div>

</span></span></div>

