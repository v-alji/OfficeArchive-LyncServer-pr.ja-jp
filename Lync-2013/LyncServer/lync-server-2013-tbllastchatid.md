---
title: 'Lync Server 2013: tblLastChatId'
description: 'Lync Server 2013: tblLastChatId'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblLastChatId
ms:assetid: 17a4ffbe-cca9-4ec5-ae46-38a15274889a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558616(v=OCS.15)
ms:contentKeyID: 48183513
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 69e80a735e70c8a03441038f5e58eb93e0af1f82
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444428"
---
# <a name="tbllastchatid-in-lync-server-2013"></a><span data-ttu-id="50df5-103">Lync Server 2013 の tblLastChatId</span><span class="sxs-lookup"><span data-stu-id="50df5-103">tblLastChatId in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="50df5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="50df5-104">

<span> </span></span></span>

<span data-ttu-id="50df5-105">_**最終更新日:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="50df5-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="50df5-106">tblLastChatId には、各ユーザーに対して生成された (tblChat テーブルで使用された) 最後のチャット ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="50df5-106">tblLastChatId contains the last chat ID that was generated (and used in the tblChat table) for each user.</span></span>

### <a name="columns"></a><span data-ttu-id="50df5-107">行</span><span class="sxs-lookup"><span data-stu-id="50df5-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="50df5-108">列</span><span class="sxs-lookup"><span data-stu-id="50df5-108">Column</span></span></th>
<th><span data-ttu-id="50df5-109">型</span><span class="sxs-lookup"><span data-stu-id="50df5-109">Type</span></span></th>
<th><span data-ttu-id="50df5-110">説明</span><span class="sxs-lookup"><span data-stu-id="50df5-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="50df5-111">nodeID</span><span class="sxs-lookup"><span data-stu-id="50df5-111">nodeID</span></span></p></td>
<td><p><span data-ttu-id="50df5-112">int (null ではない)</span><span class="sxs-lookup"><span data-stu-id="50df5-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="50df5-113">ノード ID (チャットルームの種類のみ)。</span><span class="sxs-lookup"><span data-stu-id="50df5-113">Node ID (chat room-type only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50df5-114">lastChatID</span><span class="sxs-lookup"><span data-stu-id="50df5-114">lastChatID</span></span></p></td>
<td><p><span data-ttu-id="50df5-115">bigint (null ではない)</span><span class="sxs-lookup"><span data-stu-id="50df5-115">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="50df5-116">最後に使用されたチャット ID。</span><span class="sxs-lookup"><span data-stu-id="50df5-116">Last used chat ID.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="50df5-117">機能</span><span class="sxs-lookup"><span data-stu-id="50df5-117">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="50df5-118">列</span><span class="sxs-lookup"><span data-stu-id="50df5-118">Column</span></span></th>
<th><span data-ttu-id="50df5-119">説明</span><span class="sxs-lookup"><span data-stu-id="50df5-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="50df5-120">&lt;nodeID、lastChatID&gt;</span><span class="sxs-lookup"><span data-stu-id="50df5-120">&lt;nodeID, lastChatID&gt;</span></span></p></td>
<td><p><span data-ttu-id="50df5-121">主キー (nodeID だけが処理に十分な場合)。</span><span class="sxs-lookup"><span data-stu-id="50df5-121">Primary key (just nodeID is sufficient for processing).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50df5-122">nodeID</span><span class="sxs-lookup"><span data-stu-id="50df5-122">nodeID</span></span></p></td>
<td><p><span data-ttu-id="50df5-123">TblNode テーブルで参照される外部キー。</span><span class="sxs-lookup"><span data-stu-id="50df5-123">Foreign key with lookup in tblNode.nodeID table.</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="50df5-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="50df5-124">See Also</span></span>


[<span data-ttu-id="50df5-125">Lync Server 2013 の tblChat</span><span class="sxs-lookup"><span data-stu-id="50df5-125">tblChat in Lync Server 2013</span></span>](lync-server-2013-tblchat.md)  
  

<span data-ttu-id="50df5-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="50df5-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

