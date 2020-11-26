---
title: 'Lync Server 2013: tblLastInviteId'
description: 'Lync Server 2013: tblLastInviteId'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblLastInviteId
ms:assetid: 222b3508-5963-4ddc-b4f3-e8412767e61b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558625(v=OCS.15)
ms:contentKeyID: 48183608
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e5a13cfc7edc29ea20c95f7f4d587b0cfb84eb73
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444421"
---
# <a name="tbllastinviteid-in-lync-server-2013"></a><span data-ttu-id="7c64f-103">Lync Server 2013 の tblLastInviteId</span><span class="sxs-lookup"><span data-stu-id="7c64f-103">tblLastInviteId in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7c64f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7c64f-104">

<span> </span></span></span>

<span data-ttu-id="7c64f-105">_**最終更新日:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="7c64f-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="7c64f-106">tblLastInviteId には、各ユーザーに対して生成された (tblPrincipalInvites テーブルで使用された) 最後の招待 ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7c64f-106">tblLastInviteId contains the last invite ID that was generated (and used in the tblPrincipalInvites table) for each user.</span></span>

### <a name="columns"></a><span data-ttu-id="7c64f-107">行</span><span class="sxs-lookup"><span data-stu-id="7c64f-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7c64f-108">列</span><span class="sxs-lookup"><span data-stu-id="7c64f-108">Column</span></span></th>
<th><span data-ttu-id="7c64f-109">型</span><span class="sxs-lookup"><span data-stu-id="7c64f-109">Type</span></span></th>
<th><span data-ttu-id="7c64f-110">説明</span><span class="sxs-lookup"><span data-stu-id="7c64f-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7c64f-111">prinID</span><span class="sxs-lookup"><span data-stu-id="7c64f-111">prinID</span></span></p></td>
<td><p><span data-ttu-id="7c64f-112">int (null ではない)</span><span class="sxs-lookup"><span data-stu-id="7c64f-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="7c64f-113">プリンシパル ID。</span><span class="sxs-lookup"><span data-stu-id="7c64f-113">Principal ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c64f-114">lastInviteID</span><span class="sxs-lookup"><span data-stu-id="7c64f-114">lastInviteID</span></span></p></td>
<td><p><span data-ttu-id="7c64f-115">int (null ではない)</span><span class="sxs-lookup"><span data-stu-id="7c64f-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="7c64f-116">最後に使用した招待の ID。</span><span class="sxs-lookup"><span data-stu-id="7c64f-116">Last used invite ID.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="7c64f-117">機能</span><span class="sxs-lookup"><span data-stu-id="7c64f-117">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7c64f-118">列</span><span class="sxs-lookup"><span data-stu-id="7c64f-118">Column</span></span></th>
<th><span data-ttu-id="7c64f-119">説明</span><span class="sxs-lookup"><span data-stu-id="7c64f-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7c64f-120">prinID</span><span class="sxs-lookup"><span data-stu-id="7c64f-120">prinID</span></span></p></td>
<td><p><span data-ttu-id="7c64f-121">主キー。</span><span class="sxs-lookup"><span data-stu-id="7c64f-121">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c64f-122">prinID</span><span class="sxs-lookup"><span data-stu-id="7c64f-122">prinID</span></span></p></td>
<td><p><span data-ttu-id="7c64f-123">TblPrincipal Id テーブルで参照される外部キー。</span><span class="sxs-lookup"><span data-stu-id="7c64f-123">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="7c64f-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="7c64f-124">See Also</span></span>


[<span data-ttu-id="7c64f-125">Lync Server 2013 の tblPrincipalInvites</span><span class="sxs-lookup"><span data-stu-id="7c64f-125">tblPrincipalInvites in Lync Server 2013</span></span>](lync-server-2013-tblprincipalinvites.md)  
  

<span data-ttu-id="7c64f-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7c64f-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

