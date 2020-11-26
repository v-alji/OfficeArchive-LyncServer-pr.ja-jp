---
title: 'Lync Server 2013: tblComplianceData'
description: 'Lync Server 2013: tblComplianceData'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblComplianceData
ms:assetid: 05b28f9b-4aba-4b69-ba8d-2ceeb6cbfaac
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558606(v=OCS.15)
ms:contentKeyID: 48183308
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3c597d67054303de2753182b37419f68051d3af8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444477"
---
# <a name="tblcompliancedata-in-lync-server-2013"></a><span data-ttu-id="f2c1a-103">Lync Server 2013 の tblComplianceData</span><span class="sxs-lookup"><span data-stu-id="f2c1a-103">tblComplianceData in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f2c1a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f2c1a-104">

<span> </span></span></span>

<span data-ttu-id="f2c1a-105">_**最終更新日:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="f2c1a-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="f2c1a-106">tblComplianceData には、コンプライアンスアダプターでまだ処理されていないコンプライアンスイベントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="f2c1a-106">tblComplianceData contains the compliance events that have not been processed by the compliance adapter yet.</span></span>

### <a name="columns"></a><span data-ttu-id="f2c1a-107">行</span><span class="sxs-lookup"><span data-stu-id="f2c1a-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f2c1a-108">列</span><span class="sxs-lookup"><span data-stu-id="f2c1a-108">Column</span></span></th>
<th><span data-ttu-id="f2c1a-109">型</span><span class="sxs-lookup"><span data-stu-id="f2c1a-109">Type</span></span></th>
<th><span data-ttu-id="f2c1a-110">説明</span><span class="sxs-lookup"><span data-stu-id="f2c1a-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2c1a-111">cmplEventID</span><span class="sxs-lookup"><span data-stu-id="f2c1a-111">cmplEventID</span></span></p></td>
<td><p><span data-ttu-id="f2c1a-112">bigint (null ではない)</span><span class="sxs-lookup"><span data-stu-id="f2c1a-112">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="f2c1a-113">イベント ID。</span><span class="sxs-lookup"><span data-stu-id="f2c1a-113">Event ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2c1a-114">entryDate</span><span class="sxs-lookup"><span data-stu-id="f2c1a-114">entryDate</span></span></p></td>
<td><p><span data-ttu-id="f2c1a-115">smalldatetime、null ではない</span><span class="sxs-lookup"><span data-stu-id="f2c1a-115">smalldatetime, not null</span></span></p></td>
<td><p><span data-ttu-id="f2c1a-116">挿入の時刻 (その場合は、cmplType = 9 の場合は、その場合はプレースホルダーのみのエントリであるため)。</span><span class="sxs-lookup"><span data-stu-id="f2c1a-116">Time of insertion (may be far in the future for cmplType=9 because the entry is just a placeholder in that case).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2c1a-117">cmplType 種類</span><span class="sxs-lookup"><span data-stu-id="f2c1a-117">cmplType</span></span></p></td>
<td><p><span data-ttu-id="f2c1a-118">int (null ではない)</span><span class="sxs-lookup"><span data-stu-id="f2c1a-118">int, not null</span></span></p></td>
<td><p><span data-ttu-id="f2c1a-119">コンプライアンスイベントの種類:</span><span class="sxs-lookup"><span data-stu-id="f2c1a-119">Type of compliance event:</span></span></p>
<ul>
<li><p><span data-ttu-id="f2c1a-120">1: チャット</span><span class="sxs-lookup"><span data-stu-id="f2c1a-120">1: Chat</span></span></p></li>
<li><p><span data-ttu-id="f2c1a-121">2: backchat</span><span class="sxs-lookup"><span data-stu-id="f2c1a-121">2: Backchat</span></span></p></li>
<li><p><span data-ttu-id="f2c1a-122">3: ファイルのダウンロード</span><span class="sxs-lookup"><span data-stu-id="f2c1a-122">3: File download</span></span></p></li>
<li><p><span data-ttu-id="f2c1a-123">4: ファイルのアップロード</span><span class="sxs-lookup"><span data-stu-id="f2c1a-123">4: File upload</span></span></p></li>
<li><p><span data-ttu-id="f2c1a-124">9: 暫定ファイル送信</span><span class="sxs-lookup"><span data-stu-id="f2c1a-124">9: Provisional file transfer</span></span></p></li>
<li><p><span data-ttu-id="f2c1a-125">10: チャットの削除 (置換あり)</span><span class="sxs-lookup"><span data-stu-id="f2c1a-125">10: Chat deletion (with replace)</span></span></p></li>
<li><p><span data-ttu-id="f2c1a-126">11: チャットの削除</span><span class="sxs-lookup"><span data-stu-id="f2c1a-126">11: Chat purging</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2c1a-127">cmplTime</span><span class="sxs-lookup"><span data-stu-id="f2c1a-127">cmplTime</span></span></p></td>
<td><p><span data-ttu-id="f2c1a-128">bigint (null ではない)</span><span class="sxs-lookup"><span data-stu-id="f2c1a-128">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="f2c1a-129">イベントのタイムスタンプ。</span><span class="sxs-lookup"><span data-stu-id="f2c1a-129">Time stamp for the event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2c1a-130">cmplChannelUri</span><span class="sxs-lookup"><span data-stu-id="f2c1a-130">cmplChannelUri</span></span></p></td>
<td><p><span data-ttu-id="f2c1a-131">nvarchar (255)、null ではない</span><span class="sxs-lookup"><span data-stu-id="f2c1a-131">nvarchar (255), not null</span></span></p></td>
<td><p><span data-ttu-id="f2c1a-132">チャネルの Uniform Resource Identifier (URI)。</span><span class="sxs-lookup"><span data-stu-id="f2c1a-132">Channel Uniform Resource Identifier (URI).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2c1a-133">cmplChatID</span><span class="sxs-lookup"><span data-stu-id="f2c1a-133">cmplChatID</span></span></p></td>
<td><p><span data-ttu-id="f2c1a-134">bigint</span><span class="sxs-lookup"><span data-stu-id="f2c1a-134">bigint</span></span></p></td>
<td><p><span data-ttu-id="f2c1a-135">チャット ID (chatId テーブルに対応する tblChat)。</span><span class="sxs-lookup"><span data-stu-id="f2c1a-135">Chat ID (corresponding to tblChat.chatId table).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2c1a-136">cmplUserID</span><span class="sxs-lookup"><span data-stu-id="f2c1a-136">cmplUserID</span></span></p></td>
<td><p><span data-ttu-id="f2c1a-137">int (null ではない)</span><span class="sxs-lookup"><span data-stu-id="f2c1a-137">int, not null</span></span></p></td>
<td><p><span data-ttu-id="f2c1a-138">ポスターのプリンシパル ID (tblPrincipal ID テーブルに対応)</span><span class="sxs-lookup"><span data-stu-id="f2c1a-138">Principal ID of the poster (corresponding to tblPrincipal.prinID table).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2c1a-139">cmplUserUri</span><span class="sxs-lookup"><span data-stu-id="f2c1a-139">cmplUserUri</span></span></p></td>
<td><p><span data-ttu-id="f2c1a-140">nvarchar (255)、null ではない</span><span class="sxs-lookup"><span data-stu-id="f2c1a-140">nvarchar (255), not null</span></span></p></td>
<td><p><span data-ttu-id="f2c1a-141">ユーザー URI。</span><span class="sxs-lookup"><span data-stu-id="f2c1a-141">User URI.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2c1a-142">cmplMessage</span><span class="sxs-lookup"><span data-stu-id="f2c1a-142">cmplMessage</span></span></p></td>
<td><p><span data-ttu-id="f2c1a-143">nvarchar (max)</span><span class="sxs-lookup"><span data-stu-id="f2c1a-143">nvarchar (max)</span></span></p></td>
<td><p><span data-ttu-id="f2c1a-144">メッセージ (エンコードは、cmplType 型によって異なります)。</span><span class="sxs-lookup"><span data-stu-id="f2c1a-144">Message (encoding depends on cmplType).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="f2c1a-145">キー</span><span class="sxs-lookup"><span data-stu-id="f2c1a-145">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f2c1a-146">列</span><span class="sxs-lookup"><span data-stu-id="f2c1a-146">Column</span></span></th>
<th><span data-ttu-id="f2c1a-147">説明</span><span class="sxs-lookup"><span data-stu-id="f2c1a-147">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2c1a-148">cmplEventID</span><span class="sxs-lookup"><span data-stu-id="f2c1a-148">cmplEventID</span></span></p></td>
<td><p><span data-ttu-id="f2c1a-149">主キー。</span><span class="sxs-lookup"><span data-stu-id="f2c1a-149">Primary key.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="f2c1a-150">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f2c1a-150">


</div>

<span> </span>

</div>

</div>

</span></span></div>

