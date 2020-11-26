---
title: 'Lync Server 2013: tblComplianceParticipant'
description: 'Lync Server 2013: tblComplianceParticipant'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblComplianceParticipant
ms:assetid: 5d7e0dea-74f7-46d1-badf-b94abc8f066d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558655(v=OCS.15)
ms:contentKeyID: 48184262
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c1385b0a635f003a72de93f10f72642314ad7ebd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444456"
---
# <a name="tblcomplianceparticipant-in-lync-server-2013"></a><span data-ttu-id="40f10-103">Lync Server 2013 内の tblComplianceParticipant</span><span class="sxs-lookup"><span data-stu-id="40f10-103">tblComplianceParticipant in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="40f10-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="40f10-104">

<span> </span></span></span>

<span data-ttu-id="40f10-105">_**最終更新日:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="40f10-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="40f10-106">tblComplianceParticipant には、チャネルあたり、サーバーごとに現在の参加者が含まれています。</span><span class="sxs-lookup"><span data-stu-id="40f10-106">tblComplianceParticipant contains the current participants per channel and per server.</span></span>

### <a name="columns"></a><span data-ttu-id="40f10-107">行</span><span class="sxs-lookup"><span data-stu-id="40f10-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="40f10-108">列</span><span class="sxs-lookup"><span data-stu-id="40f10-108">Column</span></span></th>
<th><span data-ttu-id="40f10-109">型</span><span class="sxs-lookup"><span data-stu-id="40f10-109">Type</span></span></th>
<th><span data-ttu-id="40f10-110">説明</span><span class="sxs-lookup"><span data-stu-id="40f10-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="40f10-111">channelUri</span><span class="sxs-lookup"><span data-stu-id="40f10-111">channelUri</span></span></p></td>
<td><p><span data-ttu-id="40f10-112">nvarchar (255)、null ではない</span><span class="sxs-lookup"><span data-stu-id="40f10-112">nvarchar (255), not null</span></span></p></td>
<td><p><span data-ttu-id="40f10-113">チャネルの Uniform Resource Identifier (URI)。</span><span class="sxs-lookup"><span data-stu-id="40f10-113">Channel Uniform Resource Identifier (URI).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f10-114">userId</span><span class="sxs-lookup"><span data-stu-id="40f10-114">userId</span></span></p></td>
<td><p><span data-ttu-id="40f10-115">int (null ではない)</span><span class="sxs-lookup"><span data-stu-id="40f10-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="40f10-116">参加者のプリンシパル ID (tblPrincipal ID テーブルに対応)</span><span class="sxs-lookup"><span data-stu-id="40f10-116">Principal ID of the participant (corresponding to tblPrincipal.prinID table).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f10-117">joinedAt</span><span class="sxs-lookup"><span data-stu-id="40f10-117">joinedAt</span></span></p></td>
<td><p><span data-ttu-id="40f10-118">bigint (null ではない)</span><span class="sxs-lookup"><span data-stu-id="40f10-118">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="40f10-119">参加イベントのタイムスタンプ。</span><span class="sxs-lookup"><span data-stu-id="40f10-119">Time stamp of the joining event.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f10-120">partedAt</span><span class="sxs-lookup"><span data-stu-id="40f10-120">partedAt</span></span></p></td>
<td><p><span data-ttu-id="40f10-121">bigint</span><span class="sxs-lookup"><span data-stu-id="40f10-121">bigint</span></span></p></td>
<td><p><span data-ttu-id="40f10-122">参加者がまだ参加している場合は Null です。</span><span class="sxs-lookup"><span data-stu-id="40f10-122">Null if participant is still joined.</span></span> <span data-ttu-id="40f10-123">チャネルが null でない場合は、チャネルのタイムスタンプがイベントから出ます。</span><span class="sxs-lookup"><span data-stu-id="40f10-123">The time stamp of the channel leaving event if not null.</span></span></p>
<p><span data-ttu-id="40f10-124">これらのエントリは、すべての翻訳者がイベントを処理すると、最終的に削除されます。</span><span class="sxs-lookup"><span data-stu-id="40f10-124">These entries are eventually removed when all translators process the event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f10-125">userUri</span><span class="sxs-lookup"><span data-stu-id="40f10-125">userUri</span></span></p></td>
<td><p><span data-ttu-id="40f10-126">nvarchar (255)、null ではない</span><span class="sxs-lookup"><span data-stu-id="40f10-126">nvarchar(255), not null</span></span></p></td>
<td><p><span data-ttu-id="40f10-127">ユーザー URI。</span><span class="sxs-lookup"><span data-stu-id="40f10-127">User URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f10-128">serverID</span><span class="sxs-lookup"><span data-stu-id="40f10-128">serverID</span></span></p></td>
<td><p><span data-ttu-id="40f10-129">int</span><span class="sxs-lookup"><span data-stu-id="40f10-129">int</span></span></p></td>
<td><p><span data-ttu-id="40f10-130">サーバー id (serverID テーブルの場合)。</span><span class="sxs-lookup"><span data-stu-id="40f10-130">Server identity (as in tblServerIdentity.serverID table).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f10-131">sessionId</span><span class="sxs-lookup"><span data-stu-id="40f10-131">sessionId</span></span></p></td>
<td><p><span data-ttu-id="40f10-132">bigint</span><span class="sxs-lookup"><span data-stu-id="40f10-132">bigint</span></span></p></td>
<td><p><span data-ttu-id="40f10-133">サーバーセッション。</span><span class="sxs-lookup"><span data-stu-id="40f10-133">Server session.</span></span> <span data-ttu-id="40f10-134">これは、チャットサービスが開始されるたびに生成されるランダムな番号です。</span><span class="sxs-lookup"><span data-stu-id="40f10-134">This is a random number generated each time a Chat service starts.</span></span> <span data-ttu-id="40f10-135">これは、孤立した参加者を識別する目的でセッションを区別するために使われます。</span><span class="sxs-lookup"><span data-stu-id="40f10-135">It is used to differentiate sessions for the purpose of identifying orphaned participants.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="40f10-136">キー</span><span class="sxs-lookup"><span data-stu-id="40f10-136">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="40f10-137">列</span><span class="sxs-lookup"><span data-stu-id="40f10-137">Column</span></span></th>
<th><span data-ttu-id="40f10-138">説明</span><span class="sxs-lookup"><span data-stu-id="40f10-138">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="40f10-139">&lt;channelUri、userId、joinedAt&gt;</span><span class="sxs-lookup"><span data-stu-id="40f10-139">&lt;channelUri, userId, joinedAt&gt;</span></span></p></td>
<td><p><span data-ttu-id="40f10-140">主キー。</span><span class="sxs-lookup"><span data-stu-id="40f10-140">Primary key.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="40f10-141">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="40f10-141">


</div>

<span> </span>

</div>

</div>

</span></span></div>

