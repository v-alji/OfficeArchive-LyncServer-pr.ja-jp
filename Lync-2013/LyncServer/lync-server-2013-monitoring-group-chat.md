---
title: 'Lync Server 2013: グループチャットを監視する'
description: 'Lync Server 2013: グループチャットを監視します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Monitoring group chat
ms:assetid: bddcf0be-ebf3-46bc-90c7-2576877734fb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720924(v=OCS.15)
ms:contentKeyID: 63969648
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 625e45f455e8dba50a5fa64240b62cb010623d16
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425424"
---
# <a name="monitoring-group-chat-in-lync-server-2013"></a><span data-ttu-id="adcdd-103">Lync Server 2013 でグループチャットを監視する</span><span class="sxs-lookup"><span data-stu-id="adcdd-103">Monitoring group chat in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="adcdd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="adcdd-104">

<span> </span></span></span>

<span data-ttu-id="adcdd-105">_**最終更新日:** 2014-08-04_</span><span class="sxs-lookup"><span data-stu-id="adcdd-105">_**Topic Last Modified:** 2014-08-04_</span></span>

<span data-ttu-id="adcdd-106">パフォーマンスを向上させるには、Microsoft ダウンロードセンターで入手できる最新の [累積サーバー更新プログラムインストーラー](https://support.microsoft.com/kb/968802) を実行することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="adcdd-106">We highly recommend running the most recent [Cumulative Server Update Installer](https://support.microsoft.com/kb/968802) available on the Microsoft Download Center for performance improvements.</span></span>

<span data-ttu-id="adcdd-107">最新の累積更新プログラムを実行していることを前提として、グループチャットサーバーが最適な状態で実行されているかどうかを判断するために、メトリックについて次のストレステストテーブルを使用します。</span><span class="sxs-lookup"><span data-stu-id="adcdd-107">Assuming you are running latest cumulative update, use the following stress test table for metrics to understand if your Group Chat Servers are running at optimal health.</span></span>

### <a name="test-environment-and-user-model"></a><span data-ttu-id="adcdd-108">環境とユーザーモデルのテスト</span><span class="sxs-lookup"><span data-stu-id="adcdd-108">Test environment and user model</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="adcdd-109">グループチャットプール内の3つのグループチャットサーバ、それぞれに 8 GB のメモリと8個のプロセッサが搭載されています。</span><span class="sxs-lookup"><span data-stu-id="adcdd-109">Three Group Chat Servers in a Group Chat pool, each with 8 GB memory and 8 processors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adcdd-110">Enterprise Edition での2台の Lync Server 2013 フロントエンド。</span><span class="sxs-lookup"><span data-stu-id="adcdd-110">Two Lync Server 2013 Front Ends in Enterprise Edition.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adcdd-111">6万で3つのグループチャットサーバに同時に接続できます。</span><span class="sxs-lookup"><span data-stu-id="adcdd-111">60,000 concurrent users across three Group Chat Servers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adcdd-112">グループチャットプールによってホストされている25000チャネル。</span><span class="sxs-lookup"><span data-stu-id="adcdd-112">25,000 channels hosted by Group Chat Pool.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adcdd-113">チャンネルサイズ:</span><span class="sxs-lookup"><span data-stu-id="adcdd-113">Channel Size:</span></span></p>
<ul>
<li><p><span data-ttu-id="adcdd-114">小さいチャンネルサイズ:30</span><span class="sxs-lookup"><span data-stu-id="adcdd-114">Small Channel Size: 30</span></span></p></li>
<li><p><span data-ttu-id="adcdd-115">ミディアムチャネルサイズ: 150</span><span class="sxs-lookup"><span data-stu-id="adcdd-115">Medium Channel Size: 150</span></span></p></li>
<li><p><span data-ttu-id="adcdd-116">大きいチャンネルサイズ: 2500</span><span class="sxs-lookup"><span data-stu-id="adcdd-116">Large Channel Size: 2500</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adcdd-117">チャネル数:</span><span class="sxs-lookup"><span data-stu-id="adcdd-117">Channel Count:</span></span></p>
<ul>
<li><p><span data-ttu-id="adcdd-118">小さいチャンネル数: 24000</span><span class="sxs-lookup"><span data-stu-id="adcdd-118">Number small channels: 24,000</span></span></p></li>
<li><p><span data-ttu-id="adcdd-119">数値媒体チャネル800</span><span class="sxs-lookup"><span data-stu-id="adcdd-119">Number medium channels 800</span></span></p></li>
<li><p><span data-ttu-id="adcdd-120">大きいチャンネルの番号24</span><span class="sxs-lookup"><span data-stu-id="adcdd-120">Number large channels 24</span></span></p></li>
<li><p><span data-ttu-id="adcdd-121">チャネルの合計24824</span><span class="sxs-lookup"><span data-stu-id="adcdd-121">Total Channels 24,824</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adcdd-122">チャネルの招待:</span><span class="sxs-lookup"><span data-stu-id="adcdd-122">Invite channels:</span></span></p>
<ul>
<li><p><span data-ttu-id="adcdd-123">チャンネルがチャンネルを招待した残りのチャネル</span><span class="sxs-lookup"><span data-stu-id="adcdd-123">Half the channels were invite channels</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adcdd-124">ユーザーが参加するチャネルの数:</span><span class="sxs-lookup"><span data-stu-id="adcdd-124">Number of channels a user joins:</span></span></p>
<ul>
<li><p><span data-ttu-id="adcdd-125">小:12</span><span class="sxs-lookup"><span data-stu-id="adcdd-125">Small: 12</span></span></p></li>
<li><p><span data-ttu-id="adcdd-126">中: 2</span><span class="sxs-lookup"><span data-stu-id="adcdd-126">Medium: 2</span></span></p></li>
<li><p><span data-ttu-id="adcdd-127">大: 1</span><span class="sxs-lookup"><span data-stu-id="adcdd-127">Large: 1</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adcdd-128">参加率:</span><span class="sxs-lookup"><span data-stu-id="adcdd-128">Join rate:</span></span></p>
<ul>
<li><p><span data-ttu-id="adcdd-129">サーバーあたり10合計/秒、3.33/秒</span><span class="sxs-lookup"><span data-stu-id="adcdd-129">10 total/second, 3.33/second per server</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adcdd-130">ログアウト率:</span><span class="sxs-lookup"><span data-stu-id="adcdd-130">Logout rate:</span></span></p>
<ul>
<li><p><span data-ttu-id="adcdd-131">サーバーあたり10合計/秒、3.33/秒</span><span class="sxs-lookup"><span data-stu-id="adcdd-131">10 total/second, 3.33/second per server</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adcdd-132">チャット料金:</span><span class="sxs-lookup"><span data-stu-id="adcdd-132">Chat rate:</span></span></p>
<ul>
<li><p><span data-ttu-id="adcdd-133">1サーバーあたり20合計/秒、6.66/秒</span><span class="sxs-lookup"><span data-stu-id="adcdd-133">20 total/second, 6.66/second per server</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


<div>


> [!IMPORTANT]  
> <span data-ttu-id="adcdd-134">ハードウェア仕様またはユーザープロファイルが異なる場合、次のパフォーマンスカウンターの数値が異なる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="adcdd-134">The following performance counter numbers will likely vary when different hardware specifications or user profiles are used.</span></span>



</div>

### <a name="performance-counter-to-be-monitored"></a><span data-ttu-id="adcdd-135">監視対象のパフォーマンスカウンター</span><span class="sxs-lookup"><span data-stu-id="adcdd-135">Performance counter to be monitored</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="adcdd-136">パフォーマンス カウンター</span><span class="sxs-lookup"><span data-stu-id="adcdd-136">Performance Counter</span></span></th>
<th><span data-ttu-id="adcdd-137">しきい値</span><span class="sxs-lookup"><span data-stu-id="adcdd-137">Thresholds</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="adcdd-138">プロセス (ChannelService)- &gt; プロセッサ時間の割合</span><span class="sxs-lookup"><span data-stu-id="adcdd-138">Process(ChannelService)-&gt;%Processor Time</span></span></p></td>
<td><p><span data-ttu-id="adcdd-139">Min: 0</span><span class="sxs-lookup"><span data-stu-id="adcdd-139">Min: 0</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="adcdd-140">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="adcdd-140">


</div>

<span> </span>

</div>

</div>

</span></span></div>

