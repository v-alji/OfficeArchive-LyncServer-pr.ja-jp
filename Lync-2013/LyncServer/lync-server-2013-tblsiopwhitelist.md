---
title: 'Lync Server 2013: tblSiopWhiteList'
description: 'Lync Server 2013: tblSiopWhiteList'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblSiopWhiteList
ms:assetid: 05fc1df4-32eb-4d46-9d1c-e0b607091142
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558607(v=OCS.15)
ms:contentKeyID: 48183310
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fbb58c0818a6f36959732f210b8eb53bbfe223d0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398060"
---
# <a name="tblsiopwhitelist-in-lync-server-2013"></a><span data-ttu-id="6e55f-103">Lync Server 2013 の tblSiopWhiteList</span><span class="sxs-lookup"><span data-stu-id="6e55f-103">tblSiopWhiteList in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6e55f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6e55f-104">

<span> </span></span></span>

<span data-ttu-id="6e55f-105">_**最終更新日:** 2012-06-28_</span><span class="sxs-lookup"><span data-stu-id="6e55f-105">_**Topic Last Modified:** 2012-06-28_</span></span>

<span data-ttu-id="6e55f-106">tblSiopWhiteList は、ノードに関連付けることができる登録済みアドインの一覧です。</span><span class="sxs-lookup"><span data-stu-id="6e55f-106">tblSiopWhiteList is the list of registered add-ins that can be associated with nodes.</span></span>

### <a name="columns"></a><span data-ttu-id="6e55f-107">行</span><span class="sxs-lookup"><span data-stu-id="6e55f-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6e55f-108">列</span><span class="sxs-lookup"><span data-stu-id="6e55f-108">Column</span></span></th>
<th><span data-ttu-id="6e55f-109">型</span><span class="sxs-lookup"><span data-stu-id="6e55f-109">Type</span></span></th>
<th><span data-ttu-id="6e55f-110">説明</span><span class="sxs-lookup"><span data-stu-id="6e55f-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6e55f-111">siopID</span><span class="sxs-lookup"><span data-stu-id="6e55f-111">siopID</span></span></p></td>
<td><p><span data-ttu-id="6e55f-112">GUID、null ではない</span><span class="sxs-lookup"><span data-stu-id="6e55f-112">GUID, not null</span></span></p></td>
<td><p><span data-ttu-id="6e55f-113">アドインの GUID です。</span><span class="sxs-lookup"><span data-stu-id="6e55f-113">GUID of the add-in.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e55f-114">siopName</span><span class="sxs-lookup"><span data-stu-id="6e55f-114">siopName</span></span></p></td>
<td><p><span data-ttu-id="6e55f-115">nvarchar (50)、null ではない</span><span class="sxs-lookup"><span data-stu-id="6e55f-115">nvarchar (50), not null</span></span></p></td>
<td><p><span data-ttu-id="6e55f-116">アドインの名前を表示します。</span><span class="sxs-lookup"><span data-stu-id="6e55f-116">Display-name of the add-in.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e55f-117">siopUrl</span><span class="sxs-lookup"><span data-stu-id="6e55f-117">siopUrl</span></span></p></td>
<td><p><span data-ttu-id="6e55f-118">nvarchar (255)、null ではない</span><span class="sxs-lookup"><span data-stu-id="6e55f-118">nvarchar (255), not null</span></span></p></td>
<td><p><span data-ttu-id="6e55f-119">アドインの URL。</span><span class="sxs-lookup"><span data-stu-id="6e55f-119">URL of the add-in.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="6e55f-120">キー</span><span class="sxs-lookup"><span data-stu-id="6e55f-120">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6e55f-121">列</span><span class="sxs-lookup"><span data-stu-id="6e55f-121">Column</span></span></th>
<th><span data-ttu-id="6e55f-122">説明</span><span class="sxs-lookup"><span data-stu-id="6e55f-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6e55f-123">siopID</span><span class="sxs-lookup"><span data-stu-id="6e55f-123">siopID</span></span></p></td>
<td><p><span data-ttu-id="6e55f-124">主キー。</span><span class="sxs-lookup"><span data-stu-id="6e55f-124">Primary key.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="6e55f-125">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6e55f-125">


</div>

<span> </span>

</div>

</div>

</span></span></div>

