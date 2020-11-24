---
title: 'Lync Server 2013: tblServerIdentity'
description: 'Lync Server 2013: tblServerIdentity'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblServerIdentity
ms:assetid: 5411c9bc-b0b3-41fc-8b7e-fa71cccd770b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558648(v=OCS.15)
ms:contentKeyID: 48184125
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e954618cb373f2cf4f1b7ed929c3aaf6d8875e92
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398066"
---
# <a name="tblserveridentity-in-lync-server-2013"></a><span data-ttu-id="64fc8-103">Lync Server 2013 の tblServerIdentity</span><span class="sxs-lookup"><span data-stu-id="64fc8-103">tblServerIdentity in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="64fc8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="64fc8-104">

<span> </span></span></span>

<span data-ttu-id="64fc8-105">_**最終更新日:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="64fc8-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="64fc8-106">tblServerIdentity には、常設チャットサーバープール内のアクティブなチャットサーバーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="64fc8-106">tblServerIdentity contains the active chat servers in the Persistent Chat Server pool.</span></span>

### <a name="columns"></a><span data-ttu-id="64fc8-107">行</span><span class="sxs-lookup"><span data-stu-id="64fc8-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="64fc8-108">列</span><span class="sxs-lookup"><span data-stu-id="64fc8-108">Column</span></span></th>
<th><span data-ttu-id="64fc8-109">型</span><span class="sxs-lookup"><span data-stu-id="64fc8-109">Type</span></span></th>
<th><span data-ttu-id="64fc8-110">説明</span><span class="sxs-lookup"><span data-stu-id="64fc8-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="64fc8-111">serverID</span><span class="sxs-lookup"><span data-stu-id="64fc8-111">serverID</span></span></p></td>
<td><p><span data-ttu-id="64fc8-112">int (null ではない)</span><span class="sxs-lookup"><span data-stu-id="64fc8-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="64fc8-113">サーバー ID。</span><span class="sxs-lookup"><span data-stu-id="64fc8-113">Server ID.</span></span> <span data-ttu-id="64fc8-114">中央管理ストアのインスタンス ID に対応しています。</span><span class="sxs-lookup"><span data-stu-id="64fc8-114">Corresponds to the instance ID from Central Management store.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fc8-115">serverAddress</span><span class="sxs-lookup"><span data-stu-id="64fc8-115">serverAddress</span></span></p></td>
<td><p><span data-ttu-id="64fc8-116">nvarchar (256)、null ではない</span><span class="sxs-lookup"><span data-stu-id="64fc8-116">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="64fc8-117">Windows Communication Foundation アドレスを使用したサーバーアドレス。</span><span class="sxs-lookup"><span data-stu-id="64fc8-117">Server address using the Windows Communication Foundation address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fc8-118">Serverlastping 時間</span><span class="sxs-lookup"><span data-stu-id="64fc8-118">serverLastPingTime</span></span></p></td>
<td><p><span data-ttu-id="64fc8-119">datetime</span><span class="sxs-lookup"><span data-stu-id="64fc8-119">datetime</span></span></p></td>
<td><p><span data-ttu-id="64fc8-120">チャネルサーバーがこの行を更新して、実行中の証拠を与える最新の時刻。</span><span class="sxs-lookup"><span data-stu-id="64fc8-120">The latest time that the Channel Server updated this row to give evidence that it is running.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="64fc8-121">キー</span><span class="sxs-lookup"><span data-stu-id="64fc8-121">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="64fc8-122">列</span><span class="sxs-lookup"><span data-stu-id="64fc8-122">Column</span></span></th>
<th><span data-ttu-id="64fc8-123">説明</span><span class="sxs-lookup"><span data-stu-id="64fc8-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="64fc8-124">serverID</span><span class="sxs-lookup"><span data-stu-id="64fc8-124">serverID</span></span></p></td>
<td><p><span data-ttu-id="64fc8-125">主キー。</span><span class="sxs-lookup"><span data-stu-id="64fc8-125">Primary key.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="64fc8-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="64fc8-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

