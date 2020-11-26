---
title: 'Lync Server 2013: ゲートウェイ テーブル'
description: 'Lync Server 2013: ゲートウェイテーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Gateways table
ms:assetid: a909daad-d137-45e0-b149-1de9f8e1e029
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412795(v=OCS.15)
ms:contentKeyID: 48185034
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 869aee0227c64c17f7bdbbfd82acbd43ae029bac
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428032"
---
# <a name="gateways-table-in-lync-server-2013"></a><span data-ttu-id="22b65-103">Lync Server 2013 のゲートウェイ テーブル</span><span class="sxs-lookup"><span data-stu-id="22b65-103">Gateways table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="22b65-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="22b65-104">

<span> </span></span></span>

<span data-ttu-id="22b65-105">_**最終更新日:** 2010-11-05_</span><span class="sxs-lookup"><span data-stu-id="22b65-105">_**Topic Last Modified:** 2010-11-05_</span></span>

<span data-ttu-id="22b65-106">ゲートウェイテーブルは、サポートされているテーブルです。</span><span class="sxs-lookup"><span data-stu-id="22b65-106">The Gateways table is a supporting table.</span></span> <span data-ttu-id="22b65-107">各レコードには、データベース内にレコードがある公衆交換電話網 (PSTN) 通話に関連する1つのゲートウェイに関する情報が格納されます。</span><span class="sxs-lookup"><span data-stu-id="22b65-107">Each record stores information about one gateway that is involved in public switched telephone network (PSTN) calls that have records in the database.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="22b65-108">列</span><span class="sxs-lookup"><span data-stu-id="22b65-108">Column</span></span></th>
<th><span data-ttu-id="22b65-109">データ型</span><span class="sxs-lookup"><span data-stu-id="22b65-109">Data Type</span></span></th>
<th><span data-ttu-id="22b65-110">キー/インデックス</span><span class="sxs-lookup"><span data-stu-id="22b65-110">Key/Index</span></span></th>
<th><span data-ttu-id="22b65-111">詳細</span><span class="sxs-lookup"><span data-stu-id="22b65-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="22b65-112"><strong>GatewayId</strong></span><span class="sxs-lookup"><span data-stu-id="22b65-112"><strong>GatewayId</strong></span></span></p></td>
<td><p><span data-ttu-id="22b65-113">int</span><span class="sxs-lookup"><span data-stu-id="22b65-113">int</span></span></p></td>
<td><p><span data-ttu-id="22b65-114">Primary</span><span class="sxs-lookup"><span data-stu-id="22b65-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="22b65-115">このゲートウェイを識別する一意の番号。</span><span class="sxs-lookup"><span data-stu-id="22b65-115">Unique number identifying this gateway.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22b65-116"><strong>ゲートウェイ</strong></span><span class="sxs-lookup"><span data-stu-id="22b65-116"><strong>Gateway</strong></span></span></p></td>
<td><p><span data-ttu-id="22b65-117">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="22b65-117">nvarchar(256)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="22b65-118">ゲートウェイ名。</span><span class="sxs-lookup"><span data-stu-id="22b65-118">Gateway name.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="22b65-119">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="22b65-119">


</div>

<span> </span>

</div>

</div>

</span></span></div>

