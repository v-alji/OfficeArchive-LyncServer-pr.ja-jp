---
title: 'Lync Server 2013: tblPreference'
description: 'Lync Server 2013: tblPreference'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPreference
ms:assetid: f94eb128-f782-42ff-a568-ed3529573bc8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615052(v=OCS.15)
ms:contentKeyID: 48185913
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 86e8b81a6af93e9bf1d7673e54492579a1bed08e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441376"
---
# <a name="tblpreference-in-lync-server-2013"></a><span data-ttu-id="d0603-103">Lync Server 2013 の tblPreference</span><span class="sxs-lookup"><span data-stu-id="d0603-103">tblPreference in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d0603-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d0603-104">

<span> </span></span></span>

<span data-ttu-id="d0603-105">_**最終更新日:** 2012-09-24_</span><span class="sxs-lookup"><span data-stu-id="d0603-105">_**Topic Last Modified:** 2012-09-24_</span></span>

<span data-ttu-id="d0603-106">tblPreference には、ユーザーのクライアントの設定が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d0603-106">tblPreference contains the users’ client preferences.</span></span> <span data-ttu-id="d0603-107">通常、これは Lync 2013 より前のクライアントで使用されます。</span><span class="sxs-lookup"><span data-stu-id="d0603-107">This is generally used by clients previous to Lync 2013.</span></span>

### <a name="columns"></a><span data-ttu-id="d0603-108">行</span><span class="sxs-lookup"><span data-stu-id="d0603-108">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d0603-109">列</span><span class="sxs-lookup"><span data-stu-id="d0603-109">Column</span></span></th>
<th><span data-ttu-id="d0603-110">型</span><span class="sxs-lookup"><span data-stu-id="d0603-110">Type</span></span></th>
<th><span data-ttu-id="d0603-111">説明</span><span class="sxs-lookup"><span data-stu-id="d0603-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d0603-112">prefLabel</span><span class="sxs-lookup"><span data-stu-id="d0603-112">prefLabel</span></span></p></td>
<td><p><span data-ttu-id="d0603-113">nvarchar (255)、null ではない</span><span class="sxs-lookup"><span data-stu-id="d0603-113">nvarchar (255), not null</span></span></p></td>
<td><p><span data-ttu-id="d0603-114">" &lt; ユーザー sip uri &gt; | ユーザー名 &lt; " のような形式のラベル。設定 &gt; 。</span><span class="sxs-lookup"><span data-stu-id="d0603-114">Label with a format such as: &lt;user sip uri&gt;|username.&lt;preference set&gt;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0603-115">prefSeqID</span><span class="sxs-lookup"><span data-stu-id="d0603-115">prefSeqID</span></span></p></td>
<td><p><span data-ttu-id="d0603-116">int (null ではない)</span><span class="sxs-lookup"><span data-stu-id="d0603-116">int, not null</span></span></p></td>
<td><p><span data-ttu-id="d0603-117">バージョン管理のための連続番号 (ラベルあたり)。</span><span class="sxs-lookup"><span data-stu-id="d0603-117">A sequential number (per label) for versioning purposes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0603-118">prefContent</span><span class="sxs-lookup"><span data-stu-id="d0603-118">prefContent</span></span></p></td>
<td><p><span data-ttu-id="d0603-119">nvarchar (max)</span><span class="sxs-lookup"><span data-stu-id="d0603-119">nvarchar (max)</span></span></p></td>
<td><p><span data-ttu-id="d0603-120">エンコードされたコンテンツ。</span><span class="sxs-lookup"><span data-stu-id="d0603-120">Encoded content.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0603-121">最終方法</span><span class="sxs-lookup"><span data-stu-id="d0603-121">lastModifiedBy</span></span></p></td>
<td><p><span data-ttu-id="d0603-122">int (null ではない)</span><span class="sxs-lookup"><span data-stu-id="d0603-122">int, not null</span></span></p></td>
<td><p><span data-ttu-id="d0603-123">設定を更新したプリンシパルの ID です。</span><span class="sxs-lookup"><span data-stu-id="d0603-123">ID of the principal that updated the preference.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="d0603-124">キー</span><span class="sxs-lookup"><span data-stu-id="d0603-124">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d0603-125">列</span><span class="sxs-lookup"><span data-stu-id="d0603-125">Column</span></span></th>
<th><span data-ttu-id="d0603-126">説明</span><span class="sxs-lookup"><span data-stu-id="d0603-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d0603-127">&lt;prefLabel, prefSeqID&gt;</span><span class="sxs-lookup"><span data-stu-id="d0603-127">&lt;prefLabel, prefSeqID&gt;</span></span></p></td>
<td><p><span data-ttu-id="d0603-128">主キー。</span><span class="sxs-lookup"><span data-stu-id="d0603-128">Primary key.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="d0603-129">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d0603-129">


</div>

<span> </span>

</div>

</div>

</span></span></div>

