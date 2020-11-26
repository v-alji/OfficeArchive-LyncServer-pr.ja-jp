---
title: 'Lync Server 2013: ClientVersions ビュー'
description: 'Lync Server 2013: ClientVersions ビュー。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ClientVersions view
ms:assetid: caf7678f-83a0-46c8-83cc-fee4c3991f52
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721891(v=OCS.15)
ms:contentKeyID: 49733825
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 42ede7107a59db3162ac7f5344e47e81a80d57df
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434733"
---
# <a name="clientversions-view-in-lync-server-2013"></a><span data-ttu-id="f9373-103">Lync Server 2013 の ClientVersions ビュー</span><span class="sxs-lookup"><span data-stu-id="f9373-103">ClientVersions view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f9373-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f9373-104">

<span> </span></span></span>

<span data-ttu-id="f9373-105">_**最終更新日:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="f9373-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="f9373-106">[ClientVersions] ビューには、データベースに記録されているセッションに参加しているさまざまなクライアントの種類とバージョンに関する情報が格納されます。</span><span class="sxs-lookup"><span data-stu-id="f9373-106">The ClientVersions view stores information about the various client types and versions that have participated in sessions recorded in the database.</span></span> <span data-ttu-id="f9373-107">ビューの各レコードは、1つのクライアントバージョンを表します。</span><span class="sxs-lookup"><span data-stu-id="f9373-107">Each record in the view represents one client version.</span></span> <span data-ttu-id="f9373-108">このビューは、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="f9373-108">This view was introduced in Microsoft Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f9373-109">特定の列に対して複数のレコードが存在する場合があります。</span><span class="sxs-lookup"><span data-stu-id="f9373-109">There may be multiple records for certain columns.</span></span>



</div>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f9373-110">列</span><span class="sxs-lookup"><span data-stu-id="f9373-110">Column</span></span></th>
<th><span data-ttu-id="f9373-111">データ型</span><span class="sxs-lookup"><span data-stu-id="f9373-111">Data Type</span></span></th>
<th><span data-ttu-id="f9373-112">詳細</span><span class="sxs-lookup"><span data-stu-id="f9373-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f9373-113"><strong>VersionId</strong></span><span class="sxs-lookup"><span data-stu-id="f9373-113"><strong>VersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="f9373-114">int</span><span class="sxs-lookup"><span data-stu-id="f9373-114">int</span></span></p></td>
<td><p><span data-ttu-id="f9373-115">このクライアントの種類とバージョンを識別する一意の番号。</span><span class="sxs-lookup"><span data-stu-id="f9373-115">Unique number identifying this client type and version.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9373-116"><strong>バージョン</strong></span><span class="sxs-lookup"><span data-stu-id="f9373-116"><strong>Version</strong></span></span></p></td>
<td><p><span data-ttu-id="f9373-117">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="f9373-117">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="f9373-118">ユーザーエージェントを表します。</span><span class="sxs-lookup"><span data-stu-id="f9373-118">Represents the user agent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9373-119"><strong>ClientType</strong></span><span class="sxs-lookup"><span data-stu-id="f9373-119"><strong>ClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="f9373-120">int</span><span class="sxs-lookup"><span data-stu-id="f9373-120">int</span></span></p></td>
<td><p><span data-ttu-id="f9373-121">クライアントの種類。</span><span class="sxs-lookup"><span data-stu-id="f9373-121">Type of client.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9373-122"><strong>ClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="f9373-122"><strong>ClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="f9373-123">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="f9373-123">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="f9373-124">クライアントが所属するカテゴリ。</span><span class="sxs-lookup"><span data-stu-id="f9373-124">Category that the client belongs to.</span></span> <span data-ttu-id="f9373-125">たとえば、.0 というクライアント Conferencing_Attendant_1 は ClientCategory CAA をに属しています。</span><span class="sxs-lookup"><span data-stu-id="f9373-125">For example, the client Conferencing_Attendant_1.0 belongs to the ClientCategory CAA.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="f9373-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f9373-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

