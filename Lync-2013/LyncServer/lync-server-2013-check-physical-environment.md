---
title: 'Lync Server 2013: 物理環境を確認する'
description: 'Lync Server 2013: 物理環境を確認します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Performing physical environmental checks
ms:assetid: 153aee5e-3adf-4dbf-bf41-53e4fba51fb0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720558(v=OCS.15)
ms:contentKeyID: 63969582
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d963485b109e0afdf21b3a9085fa28884dfc3100
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434999"
---
# <a name="performing-physical-environmental-checks"></a><span data-ttu-id="248a3-103">物理的な環境のチェックを実行する</span><span class="sxs-lookup"><span data-stu-id="248a3-103">Performing physical environmental checks</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="248a3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="248a3-104">

<span> </span></span></span>

<span data-ttu-id="248a3-105">_**最終更新日:** 2014-04-30_</span><span class="sxs-lookup"><span data-stu-id="248a3-105">_**Topic Last Modified:** 2014-04-30_</span></span>

<span data-ttu-id="248a3-106">Lync Server 2013 展開のパフォーマンス、可用性、機能を確認する前に、物理環境を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="248a3-106">Before checking the performance, availability, and functionality of the Lync Server 2013 deployment, you should check the physical environment.</span></span> <span data-ttu-id="248a3-107">たとえば、サーバーの室温の温度が下げられているか、ネットワークケーブルを交換しなければならない場合があります。</span><span class="sxs-lookup"><span data-stu-id="248a3-107">For example, the server room temperature might have to be lowered, or a network cable might have to be replaced.</span></span> <span data-ttu-id="248a3-108">最善の結果を得るには、次の物理的な環境検査を実行します。</span><span class="sxs-lookup"><span data-stu-id="248a3-108">For best results, perform the following physical environmental inspections:</span></span>

  - <span data-ttu-id="248a3-109">**物理的なセキュリティ対策**   ロック、ドア、アクセス制限されたルームなどの物理的なセキュリティ保護は、セキュリティで保護されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="248a3-109">**Physical security measures**   Physical security protection such as locks, doors, and restricted-access rooms must be secured.</span></span> <span data-ttu-id="248a3-110">許可されていない強制された入力と機器の破損を確認します。</span><span class="sxs-lookup"><span data-stu-id="248a3-110">Check for any unauthorized and forced entries and signs of equipment damage.</span></span>

  - <span data-ttu-id="248a3-111">**気温と湿度**   高温度、低品質の気流、湿度は、ハードウェアコンポーネントのオーバーヒートを引き起こす可能性があります。</span><span class="sxs-lookup"><span data-stu-id="248a3-111">**Temperature and humidity**   High temperature, poor air flow, and humidity can cause hardware components to overheat.</span></span> <span data-ttu-id="248a3-112">温度と湿度をチェックして、加熱や空調などの環境システムがハードウェアの製造元の仕様に従って許容条件を満たしていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="248a3-112">Check temperature and humidity to help to make sure that the environmental systems such as heating and air conditioning can maintain acceptable conditions and function within the hardware manufacturer's specifications.</span></span> <span data-ttu-id="248a3-113">新しい機器が最近インストールされた場合は、両サーバー間の気流フローが unimpeded であり、製造元の仕様を満たしていることも確認してください。</span><span class="sxs-lookup"><span data-stu-id="248a3-113">When new equipment has recently been installed, also check that air flow both to and from the servers is unimpeded and meets manufacturer spec.</span></span>

  - <span data-ttu-id="248a3-114">**デバイスとコンポーネント**   Lync Server 2013 組織は、機能している物理ネットワークと関連ハードウェアに依存しています。</span><span class="sxs-lookup"><span data-stu-id="248a3-114">**Devices and components**   The Lync Server 2013 organization relies on a functioning physical network and related hardware.</span></span> <span data-ttu-id="248a3-115">ルーター、スイッチ、ハブ、物理ケーブル、コネクタが動作可能であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="248a3-115">Make sure that routers, switches, hubs, physical cables, and connectors are operational.</span></span>

<span data-ttu-id="248a3-116">これらのチェックを行う方法についての詳細は、インストールサイトと選択されたサーバーハードウェアによって大きく異なります。</span><span class="sxs-lookup"><span data-stu-id="248a3-116">The specifics on how to perform these checks will depend greatly on your installation site and the server hardware that was chosen.</span></span> <span data-ttu-id="248a3-117">このチェックを初めて実行するときは、ハードウェアのドキュメントを参照し、後で参照するために必要なパラメーターをメモしてください。</span><span class="sxs-lookup"><span data-stu-id="248a3-117">The first time that you perform this check, refer to the hardware documentation and note the desired parameters for future reference.</span></span>

### <a name="desired-server-space-environment"></a><span data-ttu-id="248a3-118">必要なサーバースペース環境</span><span class="sxs-lookup"><span data-stu-id="248a3-118">Desired server space environment</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="248a3-119">パラメーター</span><span class="sxs-lookup"><span data-stu-id="248a3-119">Parameter</span></span></th>
<th><span data-ttu-id="248a3-120">目的の値または範囲</span><span class="sxs-lookup"><span data-stu-id="248a3-120">Desired value or range</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="248a3-121">危険</span><span class="sxs-lookup"><span data-stu-id="248a3-121">Temperature</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="248a3-122">湿気</span><span class="sxs-lookup"><span data-stu-id="248a3-122">Humidity</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="248a3-123">サーバーの正面</span><span class="sxs-lookup"><span data-stu-id="248a3-123">Front of server faces</span></span></p></td>
<td><p><span data-ttu-id="248a3-124">ホット通路/低通路</span><span class="sxs-lookup"><span data-stu-id="248a3-124">Hot aisle / cold aisle</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="248a3-125">Unimpeded 排気クリアランス</span><span class="sxs-lookup"><span data-stu-id="248a3-125">Unimpeded exhaust clearance</span></span></p></td>
<td></td>
</tr>
</tbody>
</table><span data-ttu-id="248a3-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="248a3-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

