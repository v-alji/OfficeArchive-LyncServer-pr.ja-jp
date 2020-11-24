---
title: 'Lync Server 2013: tblAdminLock'
description: 'Lync Server 2013: tblAdminLock'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblAdminLock
ms:assetid: 785a43c0-6892-474c-821c-fa9cdbeb99d8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558665(v=OCS.15)
ms:contentKeyID: 48184560
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c3313826b2c0d578c515fb25f83e713b8978ae63
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398721"
---
# <a name="tbladminlock-in-lync-server-2013"></a><span data-ttu-id="b6885-103">Lync Server 2013 の tblAdminLock</span><span class="sxs-lookup"><span data-stu-id="b6885-103">tblAdminLock in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b6885-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b6885-104">

<span> </span></span></span>

<span data-ttu-id="b6885-105">_**最終更新日:** 2012-06-25_</span><span class="sxs-lookup"><span data-stu-id="b6885-105">_**Topic Last Modified:** 2012-06-25_</span></span>

<span data-ttu-id="b6885-106">tblAdminLock には、一部の管理者コマンドの実行に必要な管理者ロックが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b6885-106">tblAdminLock contains the administrator lock that is needed to run some administrator commands.</span></span>

### <a name="columns"></a><span data-ttu-id="b6885-107">行</span><span class="sxs-lookup"><span data-stu-id="b6885-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b6885-108">列</span><span class="sxs-lookup"><span data-stu-id="b6885-108">Column</span></span></th>
<th><span data-ttu-id="b6885-109">型</span><span class="sxs-lookup"><span data-stu-id="b6885-109">Type</span></span></th>
<th><span data-ttu-id="b6885-110">説明</span><span class="sxs-lookup"><span data-stu-id="b6885-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b6885-111">lockExpiresTime</span><span class="sxs-lookup"><span data-stu-id="b6885-111">lockExpiresTime</span></span></p></td>
<td><p><span data-ttu-id="b6885-112">datetime。 null ではありません</span><span class="sxs-lookup"><span data-stu-id="b6885-112">datetime, not null</span></span></p></td>
<td><p><span data-ttu-id="b6885-113">有効期限の日付と時刻をロックします。</span><span class="sxs-lookup"><span data-stu-id="b6885-113">Lock expiration date and time.</span></span> <span data-ttu-id="b6885-114">この値は、所有者が定期的に延長できます。</span><span class="sxs-lookup"><span data-stu-id="b6885-114">The owner can extend this value periodically.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6885-115">lockServerID</span><span class="sxs-lookup"><span data-stu-id="b6885-115">lockServerID</span></span></p></td>
<td><p><span data-ttu-id="b6885-116">int (null ではない)</span><span class="sxs-lookup"><span data-stu-id="b6885-116">int, not null</span></span></p></td>
<td><p><span data-ttu-id="b6885-117">ロックを所有しているサーバーの ID です。</span><span class="sxs-lookup"><span data-stu-id="b6885-117">ID of the server that owns the lock.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6885-118">lockActorID</span><span class="sxs-lookup"><span data-stu-id="b6885-118">lockActorID</span></span></p></td>
<td><p><span data-ttu-id="b6885-119">int (null ではない)</span><span class="sxs-lookup"><span data-stu-id="b6885-119">int, not null</span></span></p></td>
<td><p><span data-ttu-id="b6885-120">ロックを所有しているプリンシパルの ID です。</span><span class="sxs-lookup"><span data-stu-id="b6885-120">ID of the principal that owns the lock.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b6885-121">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b6885-121">


</div>

<span> </span>

</div>

</div>

</span></span></div>

