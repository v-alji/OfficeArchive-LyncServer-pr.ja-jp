---
title: 'Lync Server 2013: FileTransfers ビュー'
description: 'Lync Server 2013: FileTransfers ビュー。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: FileTransfers view
ms:assetid: e52c3ad0-152e-4a18-af1c-1aff0d205151
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721914(v=OCS.15)
ms:contentKeyID: 49733848
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dd2b084274a4d5daa093f2269617214f703ac03e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428154"
---
# <a name="filetransfers-view-in-lync-server-2013"></a><span data-ttu-id="ee1d5-103">Lync Server 2013 の FileTransfers ビュー</span><span class="sxs-lookup"><span data-stu-id="ee1d5-103">FileTransfers view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ee1d5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ee1d5-104">

<span> </span></span></span>

<span data-ttu-id="ee1d5-105">_**最終更新日:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="ee1d5-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="ee1d5-106">FileTransfer ビューには、ピアツーピアファイル転送セッションに関する情報が格納されます。</span><span class="sxs-lookup"><span data-stu-id="ee1d5-106">The FileTransfer view stores information about peer-to-peer file transfer sessions.</span></span> <span data-ttu-id="ee1d5-107">このビューは、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ee1d5-107">This view was introduced in Microsoft Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="ee1d5-108">FileTransfers ビューには、 <A href="lync-server-2013-sessiondetails-view.md">Lync Server 2013 の Sessiondetails ビュー</A> のすべての列に加えて、以下の列も含まれています。</span><span class="sxs-lookup"><span data-stu-id="ee1d5-108">The FileTransfers view contains all of the columns in the <A href="lync-server-2013-sessiondetails-view.md">SessionDetails view in Lync Server 2013</A> in addition the columns listed below.</span></span>



</div>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ee1d5-109">列</span><span class="sxs-lookup"><span data-stu-id="ee1d5-109">Column</span></span></th>
<th><span data-ttu-id="ee1d5-110">データ型</span><span class="sxs-lookup"><span data-stu-id="ee1d5-110">Data Type</span></span></th>
<th><span data-ttu-id="ee1d5-111">詳細</span><span class="sxs-lookup"><span data-stu-id="ee1d5-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee1d5-112"><strong>FileName</strong></span><span class="sxs-lookup"><span data-stu-id="ee1d5-112"><strong>FileName</strong></span></span></p></td>
<td><p><span data-ttu-id="ee1d5-113">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="ee1d5-113">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="ee1d5-114">転送されたファイルの名前。</span><span class="sxs-lookup"><span data-stu-id="ee1d5-114">Name of the file transferred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee1d5-115"><strong>クッキー</strong></span><span class="sxs-lookup"><span data-stu-id="ee1d5-115"><strong>Cookie</strong></span></span></p></td>
<td><p><span data-ttu-id="ee1d5-116">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="ee1d5-116">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="ee1d5-117">すべてのフォローアップメッセージをこのメールに関連付けられているものとして識別するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ee1d5-117">Used to identify every follow-up message as being associated with this one.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee1d5-118"><strong>FileIdentity</strong></span><span class="sxs-lookup"><span data-stu-id="ee1d5-118"><strong>FileIdentity</strong></span></span></p></td>
<td><p><span data-ttu-id="ee1d5-119">長さ</span><span class="sxs-lookup"><span data-stu-id="ee1d5-119">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="ee1d5-120">同じファイル名を含むファイル転送を区別する一意の識別子。</span><span class="sxs-lookup"><span data-stu-id="ee1d5-120">Unique identifier to distinguish between file transfers involving the same file name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee1d5-121"><strong>受諾</strong></span><span class="sxs-lookup"><span data-stu-id="ee1d5-121"><strong>Accept</strong></span></span></p></td>
<td><p><span data-ttu-id="ee1d5-122">bit</span><span class="sxs-lookup"><span data-stu-id="ee1d5-122">bit</span></span></p></td>
<td><p><span data-ttu-id="ee1d5-123">TRUE または NULL を指定できます。</span><span class="sxs-lookup"><span data-stu-id="ee1d5-123">Can be TRUE or NULL.</span></span> <span data-ttu-id="ee1d5-124">TRUE の場合は、拒否とキャンセルは NULL になります。</span><span class="sxs-lookup"><span data-stu-id="ee1d5-124">If TRUE, then Reject and Cancel will be NULL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee1d5-125"><strong>拒否</strong></span><span class="sxs-lookup"><span data-stu-id="ee1d5-125"><strong>Reject</strong></span></span></p></td>
<td><p><span data-ttu-id="ee1d5-126">bit</span><span class="sxs-lookup"><span data-stu-id="ee1d5-126">bit</span></span></p></td>
<td><p><span data-ttu-id="ee1d5-127">TRUE または NULL を指定できます。</span><span class="sxs-lookup"><span data-stu-id="ee1d5-127">Can be TRUE or NULL.</span></span> <span data-ttu-id="ee1d5-128">TRUE の場合は、Accept と Cancel は NULL になります。</span><span class="sxs-lookup"><span data-stu-id="ee1d5-128">If TRUE, then Accept and Cancel will be NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee1d5-129"><strong>キャンセル</strong></span><span class="sxs-lookup"><span data-stu-id="ee1d5-129"><strong>Cancel</strong></span></span></p></td>
<td><p><span data-ttu-id="ee1d5-130">bit</span><span class="sxs-lookup"><span data-stu-id="ee1d5-130">bit</span></span></p></td>
<td><p><span data-ttu-id="ee1d5-131">TRUE または NULL を指定できます。</span><span class="sxs-lookup"><span data-stu-id="ee1d5-131">Can be TRUE or NULL.</span></span> <span data-ttu-id="ee1d5-132">TRUE の場合は、Accept と Reject は NULL になります。</span><span class="sxs-lookup"><span data-stu-id="ee1d5-132">If TRUE, then Accept and Reject will be NULL.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="ee1d5-133">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ee1d5-133">


</div>

<span> </span>

</div>

</div>

</span></span></div>

