---
title: 'Lync Server 2013: tblComplianceState'
description: 'Lync Server 2013: tblComplianceState'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblComplianceState
ms:assetid: ea82e56c-3cca-4d89-b4e6-6bcaeb1f2830
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615045(v=OCS.15)
ms:contentKeyID: 48185937
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6eaf35eee8b4e24ec4d04e607fa77fd91b91e4e8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423513"
---
# <a name="tblcompliancestate-in-lync-server-2013"></a><span data-ttu-id="b7232-103">Lync Server 2013 の tblComplianceState</span><span class="sxs-lookup"><span data-stu-id="b7232-103">tblComplianceState in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b7232-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b7232-104">

<span> </span></span></span>

<span data-ttu-id="b7232-105">_**最終更新日:** 2012-06-28_</span><span class="sxs-lookup"><span data-stu-id="b7232-105">_**Topic Last Modified:** 2012-06-28_</span></span>

<span data-ttu-id="b7232-106">tblComplianceState には、プール全体のコンプライアンスの状態に関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b7232-106">tblComplianceState contains pool-wide compliance state information.</span></span>

### <a name="columns"></a><span data-ttu-id="b7232-107">行</span><span class="sxs-lookup"><span data-stu-id="b7232-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b7232-108">列</span><span class="sxs-lookup"><span data-stu-id="b7232-108">Column</span></span></th>
<th><span data-ttu-id="b7232-109">型</span><span class="sxs-lookup"><span data-stu-id="b7232-109">Type</span></span></th>
<th><span data-ttu-id="b7232-110">説明</span><span class="sxs-lookup"><span data-stu-id="b7232-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b7232-111">lastProcessedEntryID</span><span class="sxs-lookup"><span data-stu-id="b7232-111">lastProcessedEntryID</span></span></p></td>
<td><p><span data-ttu-id="b7232-112">bigint (null ではない)</span><span class="sxs-lookup"><span data-stu-id="b7232-112">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="b7232-113">最新の処理済みのコンプライアンスイベントの ID です。</span><span class="sxs-lookup"><span data-stu-id="b7232-113">ID of the latest processed compliance event.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7232-114">activeServerID</span><span class="sxs-lookup"><span data-stu-id="b7232-114">activeServerID</span></span></p></td>
<td><p><span data-ttu-id="b7232-115">int (null ではない)</span><span class="sxs-lookup"><span data-stu-id="b7232-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="b7232-116">データベースの排他ロックを保持しているコンプライアンスサーバーの ID。または、なしの場合は-1。</span><span class="sxs-lookup"><span data-stu-id="b7232-116">ID of the Compliance server holding the exclusive lock on the database, or -1 if none.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7232-117">lockExpirationTime</span><span class="sxs-lookup"><span data-stu-id="b7232-117">lockExpirationTime</span></span></p></td>
<td><p><span data-ttu-id="b7232-118">datetime2、null ではない</span><span class="sxs-lookup"><span data-stu-id="b7232-118">datetime2, not null</span></span></p></td>
<td><p><span data-ttu-id="b7232-119">有効期限をロックします (activeServerID が-1 でない場合)。</span><span class="sxs-lookup"><span data-stu-id="b7232-119">Lock expiration time (if activeServerID is not -1).</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b7232-120">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b7232-120">


</div>

<span> </span>

</div>

</div>

</span></span></div>

