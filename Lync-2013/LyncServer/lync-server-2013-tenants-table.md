---
title: 'Lync Server 2013: Tenants テーブル'
description: 'Lync Server 2013: テナントのテーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Tenants table
ms:assetid: c1b070c1-2c59-4ca9-910b-43f673f97fda
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412950(v=OCS.15)
ms:contentKeyID: 48185309
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 96025dfd9fb42a6083f7f3daca98e243f01a8516
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441285"
---
# <a name="tenants-table-in-lync-server-2013"></a><span data-ttu-id="077d4-103">Lync Server 2013 の Tenants テーブル</span><span class="sxs-lookup"><span data-stu-id="077d4-103">Tenants table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="077d4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="077d4-104">

<span> </span></span></span>

<span data-ttu-id="077d4-105">_**最終更新日:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="077d4-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="077d4-106">テナントの表は、さまざまなテナントの一覧を格納するサポートテーブルです。</span><span class="sxs-lookup"><span data-stu-id="077d4-106">The Tenants table is a supporting table that stores a list of the various tenants.</span></span> <span data-ttu-id="077d4-107">テーブル内の各レコードは、1つのテナントを表します。</span><span class="sxs-lookup"><span data-stu-id="077d4-107">Each record in the table represents one tenant.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="077d4-108">オンプレミスの展開では、CDR はビルトインのテナント ID を使用して、パブリック IM 接続、フェデレーション、匿名など、さまざまな認証の種類を示します。</span><span class="sxs-lookup"><span data-stu-id="077d4-108">In on-premises deployment, CDR uses the build-in Tenant ID to indicate different authentication type, such as public IM connectivity, Federated and Anonymous.</span></span>



</div>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="077d4-109">列</span><span class="sxs-lookup"><span data-stu-id="077d4-109">Column</span></span></th>
<th><span data-ttu-id="077d4-110">データ型</span><span class="sxs-lookup"><span data-stu-id="077d4-110">Data Type</span></span></th>
<th><span data-ttu-id="077d4-111">キー/インデックス</span><span class="sxs-lookup"><span data-stu-id="077d4-111">Key/Index</span></span></th>
<th><span data-ttu-id="077d4-112">詳細</span><span class="sxs-lookup"><span data-stu-id="077d4-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="077d4-113"><strong>テナント</strong></span><span class="sxs-lookup"><span data-stu-id="077d4-113"><strong>TenantId</strong></span></span></p></td>
<td><p><span data-ttu-id="077d4-114">int</span><span class="sxs-lookup"><span data-stu-id="077d4-114">int</span></span></p></td>
<td><p><span data-ttu-id="077d4-115">Primary</span><span class="sxs-lookup"><span data-stu-id="077d4-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="077d4-116">このテナント ID を識別する一意の番号です。</span><span class="sxs-lookup"><span data-stu-id="077d4-116">Unique number identifying this Tenant ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="077d4-117"><strong>TenantKey</strong></span><span class="sxs-lookup"><span data-stu-id="077d4-117"><strong>TenantKey</strong></span></span></p></td>
<td><p><span data-ttu-id="077d4-118">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="077d4-118">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="077d4-119">許可される値:</span><span class="sxs-lookup"><span data-stu-id="077d4-119">Allowed values:</span></span></p>
<ul>
<li><p><span data-ttu-id="077d4-120">00000000-0000-0000-0000-000000000000 – Enterprise</span><span class="sxs-lookup"><span data-stu-id="077d4-120">00000000-0000-0000-0000-000000000000 – Enterprise</span></span></p></li>
<li><p><span data-ttu-id="077d4-121">00000000-0000-0000-0000-000000000001 –フェデレーション</span><span class="sxs-lookup"><span data-stu-id="077d4-121">00000000-0000-0000-0000-000000000001 – Federated</span></span></p></li>
<li><p><span data-ttu-id="077d4-122">00000000-0000-0000-0000-000000000002 –匿名</span><span class="sxs-lookup"><span data-stu-id="077d4-122">00000000-0000-0000-0000-000000000002 – Anonymous</span></span></p></li>
<li><p><span data-ttu-id="077d4-123">00000000-0000-0000-0000-000000000003 –パブリック IM 接続</span><span class="sxs-lookup"><span data-stu-id="077d4-123">00000000-0000-0000-0000-000000000003 – Public IM connectivity</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="077d4-124">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="077d4-124">


</div>

<span> </span>

</div>

</div>

</span></span></div>

