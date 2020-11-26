---
title: 'Lync Server 2013: MediaList テーブル'
description: 'Lync Server 2013: MediaList テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: MediaList table
ms:assetid: 1f440590-c1bc-483e-b7bc-6cc763847768
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398279(v=OCS.15)
ms:contentKeyID: 48183579
ms.date: 07/12/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4e54535cd4a081657e7dcd59446cf65aaa3af7cd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445926"
---
# <a name="medialist-table-in-lync-server-2013"></a><span data-ttu-id="71fe4-103">Lync Server 2013 の MediaList テーブル</span><span class="sxs-lookup"><span data-stu-id="71fe4-103">MediaList table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="71fe4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="71fe4-104">

<span> </span></span></span>

<span data-ttu-id="71fe4-105">_**最終更新日:** 2016-07-12_</span><span class="sxs-lookup"><span data-stu-id="71fe4-105">_**Topic Last Modified:** 2016-07-12_</span></span>

<span data-ttu-id="71fe4-106">MediaList テーブルは、さまざまなメディアの種類の一覧を格納する静的なテーブルです。</span><span class="sxs-lookup"><span data-stu-id="71fe4-106">The MediaList table is a static table that stores the list of various media types.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="71fe4-107">列</span><span class="sxs-lookup"><span data-stu-id="71fe4-107">Column</span></span></th>
<th><span data-ttu-id="71fe4-108">データ型</span><span class="sxs-lookup"><span data-stu-id="71fe4-108">Data Type</span></span></th>
<th><span data-ttu-id="71fe4-109">キー/インデックス</span><span class="sxs-lookup"><span data-stu-id="71fe4-109">Key/Index</span></span></th>
<th><span data-ttu-id="71fe4-110">詳細</span><span class="sxs-lookup"><span data-stu-id="71fe4-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71fe4-111"><strong>MediaId</strong></span><span class="sxs-lookup"><span data-stu-id="71fe4-111"><strong>MediaId</strong></span></span></p></td>
<td><p><span data-ttu-id="71fe4-112">tinyint</span><span class="sxs-lookup"><span data-stu-id="71fe4-112">tinyint</span></span></p></td>
<td><p><span data-ttu-id="71fe4-113">Primary</span><span class="sxs-lookup"><span data-stu-id="71fe4-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="71fe4-114">値: 1 -7</span><span class="sxs-lookup"><span data-stu-id="71fe4-114">Values: 1-7</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71fe4-115"><strong>メディア</strong></span><span class="sxs-lookup"><span data-stu-id="71fe4-115"><strong>Media</strong></span></span></p></td>
<td><p><span data-ttu-id="71fe4-116">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="71fe4-116">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="71fe4-117">MediaID 値と Media 値の固定マッピング:</span><span class="sxs-lookup"><span data-stu-id="71fe4-117">Static mapping of MediaID and Media values:</span></span></p>
<ul>
<li><p><span data-ttu-id="71fe4-118">1– IM</span><span class="sxs-lookup"><span data-stu-id="71fe4-118">1 – IM</span></span></p></li>
<li><p><span data-ttu-id="71fe4-119">2 – ファイル転送</span><span class="sxs-lookup"><span data-stu-id="71fe4-119">2 – File Transfer</span></span></p></li>
<li><p><span data-ttu-id="71fe4-120">3 – リモート アシスタンス</span><span class="sxs-lookup"><span data-stu-id="71fe4-120">3 – Remote Assistance</span></span></p></li>
<li><p><span data-ttu-id="71fe4-121">4 – アプリケーション共有</span><span class="sxs-lookup"><span data-stu-id="71fe4-121">4 – Application Sharing</span></span></p></li>
<li><p><span data-ttu-id="71fe4-122">5-オーディオ</span><span class="sxs-lookup"><span data-stu-id="71fe4-122">5 – Audio</span></span></p></li>
<li><p><span data-ttu-id="71fe4-123">6-ビデオ</span><span class="sxs-lookup"><span data-stu-id="71fe4-123">6 – Video</span></span></p></li>
<li><p><span data-ttu-id="71fe4-124">7 – アプリケーション招待</span><span class="sxs-lookup"><span data-stu-id="71fe4-124">7 – App Invite</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


<span data-ttu-id="71fe4-125">LcsCDR.SessionDetailsView.MediaTypes の値でモダリティの種類を特定しようとしている場合は、次の Join スニペットを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="71fe4-125">If you are trying to determine the modality type for the values in LcsCDR.SessionDetailsView.MediaTypes, then you need to use the following Join snippet:</span></span>

    LEFT JOIN on Media.MediaId = MediaList.MediaId

<span data-ttu-id="71fe4-126"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="71fe4-126"></div>

<span> </span>

</div>

</div>

</span></span></div>

