---
title: 'Lync Server 2013: ClientVersions テーブル'
description: 'Lync Server 2013: ClientVersions テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ClientVersions table
ms:assetid: 542316cf-a6db-4d52-ab28-8bf6d27a3b48
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398356(v=OCS.15)
ms:contentKeyID: 48184176
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 81cf7147b7e36148901580983cf66176b574f815
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434761"
---
# <a name="clientversions-table-in-lync-server-2013"></a><span data-ttu-id="6fc53-103">Lync Server 2013 の ClientVersions テーブル</span><span class="sxs-lookup"><span data-stu-id="6fc53-103">ClientVersions table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6fc53-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6fc53-104">

<span> </span></span></span>

<span data-ttu-id="6fc53-105">_**最終更新日:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="6fc53-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="6fc53-106">ClientVersions テーブルは、データベースに記録されているセッションに参加しているさまざまなクライアントの種類とバージョンの一覧を格納するサポートテーブルです。</span><span class="sxs-lookup"><span data-stu-id="6fc53-106">The ClientVersions table is a supporting table that stores a list of the various client types and versions that have participated in sessions recorded in the database.</span></span> <span data-ttu-id="6fc53-107">テーブル内の各レコードは、1つのクライアントバージョンを表します。</span><span class="sxs-lookup"><span data-stu-id="6fc53-107">Each record in the table represents one client version.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6fc53-108">列</span><span class="sxs-lookup"><span data-stu-id="6fc53-108">Column</span></span></th>
<th><span data-ttu-id="6fc53-109">データ型</span><span class="sxs-lookup"><span data-stu-id="6fc53-109">Data Type</span></span></th>
<th><span data-ttu-id="6fc53-110">キー/インデックス</span><span class="sxs-lookup"><span data-stu-id="6fc53-110">Key/Index</span></span></th>
<th><span data-ttu-id="6fc53-111">詳細</span><span class="sxs-lookup"><span data-stu-id="6fc53-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6fc53-112"><strong>VersionId</strong></span><span class="sxs-lookup"><span data-stu-id="6fc53-112"><strong>VersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="6fc53-113"><strong>int</strong></span><span class="sxs-lookup"><span data-stu-id="6fc53-113"><strong>int</strong></span></span></p></td>
<td><p><span data-ttu-id="6fc53-114">Primary</span><span class="sxs-lookup"><span data-stu-id="6fc53-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="6fc53-115">このクライアントの種類とバージョンを識別する一意の番号。</span><span class="sxs-lookup"><span data-stu-id="6fc53-115">Unique number identifying this client type and version.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fc53-116"><strong>バージョン</strong></span><span class="sxs-lookup"><span data-stu-id="6fc53-116"><strong>Version</strong></span></span></p></td>
<td><p><span data-ttu-id="6fc53-117"><strong>nvarchar(256)</strong></span><span class="sxs-lookup"><span data-stu-id="6fc53-117"><strong>nvarchar(256)</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6fc53-118">バージョン名。</span><span class="sxs-lookup"><span data-stu-id="6fc53-118">Version name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6fc53-119"><strong>ClientType</strong></span><span class="sxs-lookup"><span data-stu-id="6fc53-119"><strong>ClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="6fc53-120">int</span><span class="sxs-lookup"><span data-stu-id="6fc53-120">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6fc53-121">セッションで使用するクライアントの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="6fc53-121">Specifies the type of client used in the session.</span></span> <span data-ttu-id="6fc53-122">詳細については、「 <a href="lync-server-2013-useragentdef-table.md">Lync Server 2013 の Useragentdef テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6fc53-122">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more information.</span></span></p>
<p><span data-ttu-id="6fc53-123">このフィールドは、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="6fc53-123">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="6fc53-124">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6fc53-124">


</div>

<span> </span>

</div>

</div>

</span></span></div>

