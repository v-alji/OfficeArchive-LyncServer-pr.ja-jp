---
title: 'Lync Server 2013: tblFileToken'
description: 'Lync Server 2013: tblFileToken'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblFileToken
ms:assetid: 49e7dd79-1607-443c-818a-88c160e4ed06
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558646(v=OCS.15)
ms:contentKeyID: 48184073
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9c0a0465bd769cff5c23c00a98f79e2346232175
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423534"
---
# <a name="tblfiletoken-in-lync-server-2013"></a><span data-ttu-id="e47ef-103">Lync Server 2013 の tblFileToken</span><span class="sxs-lookup"><span data-stu-id="e47ef-103">tblFileToken in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e47ef-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e47ef-104">

<span> </span></span></span>

<span data-ttu-id="e47ef-105">_**最終更新日:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="e47ef-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="e47ef-106">tblFileToken には、ファイル転送のための一時トークンが含まれています。</span><span class="sxs-lookup"><span data-stu-id="e47ef-106">tblFileToken contains temporary tokens for file transfer purposes.</span></span>

### <a name="columns"></a><span data-ttu-id="e47ef-107">行</span><span class="sxs-lookup"><span data-stu-id="e47ef-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e47ef-108">列</span><span class="sxs-lookup"><span data-stu-id="e47ef-108">Column</span></span></th>
<th><span data-ttu-id="e47ef-109">型</span><span class="sxs-lookup"><span data-stu-id="e47ef-109">Type</span></span></th>
<th><span data-ttu-id="e47ef-110">説明</span><span class="sxs-lookup"><span data-stu-id="e47ef-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e47ef-111">fileToken</span><span class="sxs-lookup"><span data-stu-id="e47ef-111">fileToken</span></span></p></td>
<td><p><span data-ttu-id="e47ef-112">nvarchar (50)、null ではない</span><span class="sxs-lookup"><span data-stu-id="e47ef-112">nvarchar (50), not null</span></span></p></td>
<td><p><span data-ttu-id="e47ef-113">一意のトークン (GUID)。</span><span class="sxs-lookup"><span data-stu-id="e47ef-113">Unique token (a GUID).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e47ef-114">fileTokenUserID</span><span class="sxs-lookup"><span data-stu-id="e47ef-114">fileTokenUserID</span></span></p></td>
<td><p><span data-ttu-id="e47ef-115">int (null ではない)</span><span class="sxs-lookup"><span data-stu-id="e47ef-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="e47ef-116">ファイルを転送するプリンシパルの ID です。</span><span class="sxs-lookup"><span data-stu-id="e47ef-116">ID of the principal that is transferring the file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e47ef-117">fileTokenChannelID</span><span class="sxs-lookup"><span data-stu-id="e47ef-117">fileTokenChannelID</span></span></p></td>
<td><p><span data-ttu-id="e47ef-118">GUID、null ではない</span><span class="sxs-lookup"><span data-stu-id="e47ef-118">GUID, not null</span></span></p></td>
<td><p><span data-ttu-id="e47ef-119">チャットルームノードの GUID です。</span><span class="sxs-lookup"><span data-stu-id="e47ef-119">GUID of the chat room node.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e47ef-120">fileTokenExpireDate</span><span class="sxs-lookup"><span data-stu-id="e47ef-120">fileTokenExpireDate</span></span></p></td>
<td><p><span data-ttu-id="e47ef-121">datetime。 null ではありません</span><span class="sxs-lookup"><span data-stu-id="e47ef-121">datetime, not null</span></span></p></td>
<td><p><span data-ttu-id="e47ef-122">有効期限。</span><span class="sxs-lookup"><span data-stu-id="e47ef-122">Expiration time.</span></span> <span data-ttu-id="e47ef-123">(固定されていない限り、トークンは30分後に期限切れになります (このコラムの次の説明を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="e47ef-123">(Tokens expire after 30 minutes, unless pinned (see the following descriptions in this column).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e47ef-124">fileTokenComplianceFileUrl</span><span class="sxs-lookup"><span data-stu-id="e47ef-124">fileTokenComplianceFileUrl</span></span></p></td>
<td><p><span data-ttu-id="e47ef-125">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="e47ef-125">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e47ef-126">転送されたファイルの URL (コンプライアンスサービスの使用の場合)。</span><span class="sxs-lookup"><span data-stu-id="e47ef-126">URL of the transferred file (for Compliance service use).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e47ef-127">fileTokenComplianceThumbnailUrl</span><span class="sxs-lookup"><span data-stu-id="e47ef-127">fileTokenComplianceThumbnailUrl</span></span></p></td>
<td><p><span data-ttu-id="e47ef-128">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="e47ef-128">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e47ef-129">転送されたファイル (コンプライアンスサービスの使用の場合) のサムネイルの URL。</span><span class="sxs-lookup"><span data-stu-id="e47ef-129">URL of the thumbnail for the transferred file (for Compliance service use).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e47ef-130">fileTokenComplianceTime</span><span class="sxs-lookup"><span data-stu-id="e47ef-130">fileTokenComplianceTime</span></span></p></td>
<td><p><span data-ttu-id="e47ef-131">datetime2</span><span class="sxs-lookup"><span data-stu-id="e47ef-131">datetime2</span></span></p></td>
<td><p><span data-ttu-id="e47ef-132">実際のファイル転送操作のタイムスタンプ (コンプライアンスサービスの使用の場合)。</span><span class="sxs-lookup"><span data-stu-id="e47ef-132">Timestamp for the actual file transfer operation (for Compliance service use).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e47ef-133">fileTokenComplianceIsUpload</span><span class="sxs-lookup"><span data-stu-id="e47ef-133">fileTokenComplianceIsUpload</span></span></p></td>
<td><p><span data-ttu-id="e47ef-134">bit</span><span class="sxs-lookup"><span data-stu-id="e47ef-134">bit</span></span></p></td>
<td><p><span data-ttu-id="e47ef-135">アップロードの場合は True(コンプライアンスサービスの使用のために) False を返します。</span><span class="sxs-lookup"><span data-stu-id="e47ef-135">True if upload; False if download (for Compliance service use).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e47ef-136">fileTokenCompliancePinned</span><span class="sxs-lookup"><span data-stu-id="e47ef-136">fileTokenCompliancePinned</span></span></p></td>
<td><p><span data-ttu-id="e47ef-137">ビット、null ではない</span><span class="sxs-lookup"><span data-stu-id="e47ef-137">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="e47ef-138">トークンがピン留めされている場合は True です。</span><span class="sxs-lookup"><span data-stu-id="e47ef-138">True if token is pinned.</span></span> <span data-ttu-id="e47ef-139">これは、コンプライアンスサービスが関連するフィールドを取得できるようになるまで、トークンをテーブルに保持するために使われます。</span><span class="sxs-lookup"><span data-stu-id="e47ef-139">It’s used to keep the token in the table until Compliance service has a chance to retrieve the relevant fields from it.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="e47ef-140">機能</span><span class="sxs-lookup"><span data-stu-id="e47ef-140">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e47ef-141">列</span><span class="sxs-lookup"><span data-stu-id="e47ef-141">Column</span></span></th>
<th><span data-ttu-id="e47ef-142">説明</span><span class="sxs-lookup"><span data-stu-id="e47ef-142">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e47ef-143">fileToken</span><span class="sxs-lookup"><span data-stu-id="e47ef-143">fileToken</span></span></p></td>
<td><p><span data-ttu-id="e47ef-144">主キー。</span><span class="sxs-lookup"><span data-stu-id="e47ef-144">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e47ef-145">fileTokenChannelID</span><span class="sxs-lookup"><span data-stu-id="e47ef-145">fileTokenChannelID</span></span></p></td>
<td><p><span data-ttu-id="e47ef-146">TblNode Guid テーブルで参照されている外部キー。</span><span class="sxs-lookup"><span data-stu-id="e47ef-146">Foreign key with lookup in tblNode.nodeGuid table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="e47ef-147">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e47ef-147">


</div>

<span> </span>

</div>

</div>

</span></span></div>

