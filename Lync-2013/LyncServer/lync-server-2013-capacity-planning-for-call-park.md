---
title: 'Lync Server 2013: コール パークの処理能力計画'
description: 'Lync Server 2013: コールパークのキャパシティ計画。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Capacity planning for Call Park
ms:assetid: 75520310-760a-4b1b-bcc1-4d724d13f87a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg416493(v=OCS.15)
ms:contentKeyID: 48184529
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 053a6dabad9d10540e84e9e4f43de09057c295f5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399951"
---
# <a name="capacity-planning-for-call-park-in-lync-server-2013"></a><span data-ttu-id="077ff-103">Lync Server 2013 のコール パークの処理能力計画</span><span class="sxs-lookup"><span data-stu-id="077ff-103">Capacity planning for Call Park in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="077ff-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="077ff-104">

<span> </span></span></span>

<span data-ttu-id="077ff-105">_**最終更新日:** 2012-09-13_</span><span class="sxs-lookup"><span data-stu-id="077ff-105">_**Topic Last Modified:** 2012-09-13_</span></span>

<div id="sectionSection0" class="section">

<span data-ttu-id="077ff-106">次の表では、キャパシティ計画の要件の基礎として使用できるコールパークユーザーモデルについて説明します。</span><span class="sxs-lookup"><span data-stu-id="077ff-106">The following table describes the Call Park user model that you can use as the basis for capacity planning requirements.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="077ff-107">障害復旧のキャパシティ計画として、ペアリングされたプールの各プールは、両方のプールのコールパークサービスのワークロードを処理できる必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="077ff-107">Keep in mind that, for disaster recovery capacity planning, each pool of a paired pool should be able to handle the workloads for Call Park services in both pools.</span></span>



</div>

### <a name="call-park-user-model"></a><span data-ttu-id="077ff-108">コール パークのユーザー モデル</span><span class="sxs-lookup"><span data-stu-id="077ff-108">Call Park User Model</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="077ff-109">指標</span><span class="sxs-lookup"><span data-stu-id="077ff-109">Metric</span></span></th>
<th><span data-ttu-id="077ff-110">フロントエンドプールあたり (8 個のフロントエンドサーバーを含む)</span><span class="sxs-lookup"><span data-stu-id="077ff-110">Per Front End pool (with 8 Front End Servers)</span></span></th>
<th><span data-ttu-id="077ff-111">Standard Edition サーバーごと</span><span class="sxs-lookup"><span data-stu-id="077ff-111">Per Standard Edition server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="077ff-112">保留率</span><span class="sxs-lookup"><span data-stu-id="077ff-112">Park rate</span></span></p></td>
<td><p><span data-ttu-id="077ff-113">8 分間に 1 回</span><span class="sxs-lookup"><span data-stu-id="077ff-113">8 per minute</span></span></p></td>
<td><p><span data-ttu-id="077ff-114">1 分間に 1 回</span><span class="sxs-lookup"><span data-stu-id="077ff-114">1 per minute</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="077ff-115">取得通話保留率</span><span class="sxs-lookup"><span data-stu-id="077ff-115">Retrieve parked call rate</span></span></p></td>
<td><p><span data-ttu-id="077ff-116">8 分間に 1 回</span><span class="sxs-lookup"><span data-stu-id="077ff-116">8 per minute</span></span></p></td>
<td><p><span data-ttu-id="077ff-117">1 分間に 1 回</span><span class="sxs-lookup"><span data-stu-id="077ff-117">1 per minute</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="077ff-118">平均保留時間</span><span class="sxs-lookup"><span data-stu-id="077ff-118">Average park duration</span></span></p></td>
<td><p><span data-ttu-id="077ff-119">60 秒</span><span class="sxs-lookup"><span data-stu-id="077ff-119">60 seconds</span></span></p></td>
<td><p><span data-ttu-id="077ff-120">60 秒</span><span class="sxs-lookup"><span data-stu-id="077ff-120">60 seconds</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="077ff-121">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="077ff-121">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

