---
title: 'Lync Server 2013: VideoStreamDetail ビュー'
description: 'Lync Server 2013: VideoStreamDetail ビュー。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VideoStreamDetail view
ms:assetid: ec8c45e1-307d-40ec-a75e-6083306105f2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721928(v=OCS.15)
ms:contentKeyID: 49733863
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a3f420c292627d15fd0d54f2eba01c565a49a72d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443427"
---
# <a name="videostreamdetail-view-in-lync-server-2013"></a><span data-ttu-id="be370-103">Lync Server 2013 の VideoStreamDetail ビュー</span><span class="sxs-lookup"><span data-stu-id="be370-103">VideoStreamDetail view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="be370-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="be370-104">

<span> </span></span></span>

<span data-ttu-id="be370-105">_**最終更新日:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="be370-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="be370-106">VideoStreamDetail ビューには、データベース内の各ビデオストリームに関する情報が格納されます。</span><span class="sxs-lookup"><span data-stu-id="be370-106">The VideoStreamDetail View stores information about each video stream in the database.</span></span> <span data-ttu-id="be370-107">このビューは、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="be370-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="be370-108">列</span><span class="sxs-lookup"><span data-stu-id="be370-108">Column</span></span></th>
<th><span data-ttu-id="be370-109">データ型</span><span class="sxs-lookup"><span data-stu-id="be370-109">Data Type</span></span></th>
<th><span data-ttu-id="be370-110">説明</span><span class="sxs-lookup"><span data-stu-id="be370-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be370-111">セッション時間</span><span class="sxs-lookup"><span data-stu-id="be370-111">SessionTime</span></span></p></td>
<td><p><span data-ttu-id="be370-112">datetime</span><span class="sxs-lookup"><span data-stu-id="be370-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="be370-113"><a href="lync-server-2013-medialine-table.md">Lync Server 2013 の MediaLine テーブル</a>から参照されている。</span><span class="sxs-lookup"><span data-stu-id="be370-113">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-114">SessionSeq</span><span class="sxs-lookup"><span data-stu-id="be370-114">SessionSeq</span></span></p></td>
<td><p><span data-ttu-id="be370-115">int</span><span class="sxs-lookup"><span data-stu-id="be370-115">int</span></span></p></td>
<td><p><span data-ttu-id="be370-116"><a href="lync-server-2013-medialine-table.md">Lync Server 2013 の MediaLine テーブル</a>から参照されている。</span><span class="sxs-lookup"><span data-stu-id="be370-116">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-117">MediaLineLabel</span><span class="sxs-lookup"><span data-stu-id="be370-117">MediaLineLabel</span></span></p></td>
<td><p><span data-ttu-id="be370-118">tinyint</span><span class="sxs-lookup"><span data-stu-id="be370-118">tinyint</span></span></p></td>
<td><p><span data-ttu-id="be370-119"><a href="lync-server-2013-medialine-table.md">Lync Server 2013 の MediaLine テーブル</a>から参照されている。</span><span class="sxs-lookup"><span data-stu-id="be370-119">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-120">StreamId</span><span class="sxs-lookup"><span data-stu-id="be370-120">StreamId</span></span></p></td>
<td><p><span data-ttu-id="be370-121">int</span><span class="sxs-lookup"><span data-stu-id="be370-121">int</span></span></p></td>
<td><p><span data-ttu-id="be370-122">メディアライン内の一意の ID。</span><span class="sxs-lookup"><span data-stu-id="be370-122">Unique ID within a media line.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-123">StartTime</span><span class="sxs-lookup"><span data-stu-id="be370-123">StartTime</span></span></p></td>
<td><p><span data-ttu-id="be370-124">datetime</span><span class="sxs-lookup"><span data-stu-id="be370-124">datetime</span></span></p></td>
<td><p><span data-ttu-id="be370-125">セッションの開始時刻。</span><span class="sxs-lookup"><span data-stu-id="be370-125">Start time of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-126">EndTime</span><span class="sxs-lookup"><span data-stu-id="be370-126">EndTime</span></span></p></td>
<td><p><span data-ttu-id="be370-127">datetime</span><span class="sxs-lookup"><span data-stu-id="be370-127">datetime</span></span></p></td>
<td><p><span data-ttu-id="be370-128">セッションの終了時刻。</span><span class="sxs-lookup"><span data-stu-id="be370-128">End time of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-129">CallPriority</span><span class="sxs-lookup"><span data-stu-id="be370-129">CallPriority</span></span></p></td>
<td><p><span data-ttu-id="be370-130">int</span><span class="sxs-lookup"><span data-stu-id="be370-130">int</span></span></p></td>
<td><p><span data-ttu-id="be370-131">通話の優先度。</span><span class="sxs-lookup"><span data-stu-id="be370-131">Priority of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-132">CallerPool</span><span class="sxs-lookup"><span data-stu-id="be370-132">CallerPool</span></span></p></td>
<td><p><span data-ttu-id="be370-133">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="be370-133">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="be370-134">発信者番号プールの FQDN。</span><span class="sxs-lookup"><span data-stu-id="be370-134">Caller pool FQDN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-135">CalleePool</span><span class="sxs-lookup"><span data-stu-id="be370-135">CalleePool</span></span></p></td>
<td><p><span data-ttu-id="be370-136">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="be370-136">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="be370-137">呼び出し元プールの FQDN。</span><span class="sxs-lookup"><span data-stu-id="be370-137">Callee pool FQDN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-138">[発信者]</span><span class="sxs-lookup"><span data-stu-id="be370-138">Caller</span></span></p></td>
<td><p><span data-ttu-id="be370-139">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="be370-139">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="be370-140">発信者の URI。</span><span class="sxs-lookup"><span data-stu-id="be370-140">Caller’s URI.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-141">[呼び出し先]</span><span class="sxs-lookup"><span data-stu-id="be370-141">Callee</span></span></p></td>
<td><p><span data-ttu-id="be370-142">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="be370-142">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="be370-143">呼び出し先の URI。</span><span class="sxs-lookup"><span data-stu-id="be370-143">Callee’s URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-144">CallerUserAgent</span><span class="sxs-lookup"><span data-stu-id="be370-144">CallerUserAgent</span></span></p></td>
<td><p><span data-ttu-id="be370-145">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="be370-145">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="be370-146">呼び出し元のユーザーエージェント文字列。</span><span class="sxs-lookup"><span data-stu-id="be370-146">Caller’s user agent string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-147">CallerUserAgentType</span><span class="sxs-lookup"><span data-stu-id="be370-147">CallerUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="be370-148">smallint</span><span class="sxs-lookup"><span data-stu-id="be370-148">smallint</span></span></p></td>
<td><p><span data-ttu-id="be370-149">呼び出し元のユーザーエージェントの種類。</span><span class="sxs-lookup"><span data-stu-id="be370-149">Type of caller’s user agent.</span></span> <span data-ttu-id="be370-150">詳細については、「 <a href="lync-server-2013-useragent-table.md">Lync Server 2013 の UserAgent テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="be370-150">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-151">CallerUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="be370-151">CallerUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="be370-152">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="be370-152">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="be370-153">呼び出し元のユーザーエージェントのカテゴリ。</span><span class="sxs-lookup"><span data-stu-id="be370-153">Category of caller’s user agent.</span></span> <span data-ttu-id="be370-154">詳細については、「 <a href="lync-server-2013-useragentdef-table-qoe.md">Lync Server 2013 の Useragentdef テーブル (QoE)</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="be370-154">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-155">CalleeUserAgent</span><span class="sxs-lookup"><span data-stu-id="be370-155">CalleeUserAgent</span></span></p></td>
<td><p><span data-ttu-id="be370-156">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="be370-156">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="be370-157">呼び出し先のユーザーエージェント文字列。</span><span class="sxs-lookup"><span data-stu-id="be370-157">Callee’s user agent string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-158">CalleeUserAgentType</span><span class="sxs-lookup"><span data-stu-id="be370-158">CalleeUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="be370-159">smallint</span><span class="sxs-lookup"><span data-stu-id="be370-159">smallint</span></span></p></td>
<td><p><span data-ttu-id="be370-160">呼び出し先のユーザーエージェントの種類。</span><span class="sxs-lookup"><span data-stu-id="be370-160">Type of callee’s user agent.</span></span> <span data-ttu-id="be370-161">詳細については、「 <a href="lync-server-2013-useragent-table.md">Lync Server 2013 の UserAgent テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="be370-161">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-162">CalleeUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="be370-162">CalleeUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="be370-163">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="be370-163">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="be370-164">呼び出し先のユーザーエージェントのカテゴリ。</span><span class="sxs-lookup"><span data-stu-id="be370-164">Category of callee’s user agent.</span></span> <span data-ttu-id="be370-165">詳細については、「 <a href="lync-server-2013-useragentdef-table-qoe.md">Lync Server 2013 の Useragentdef テーブル (QoE)</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="be370-165">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-166">CallerEndpoint</span><span class="sxs-lookup"><span data-stu-id="be370-166">CallerEndpoint</span></span></p></td>
<td><p><span data-ttu-id="be370-167">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="be370-167">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="be370-168">発信者のエンドポイント名。</span><span class="sxs-lookup"><span data-stu-id="be370-168">Caller’s endpoint name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-169">CalleeEndpoint</span><span class="sxs-lookup"><span data-stu-id="be370-169">CalleeEndpoint</span></span></p></td>
<td><p><span data-ttu-id="be370-170">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="be370-170">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="be370-171">呼び出し先のエンドポイント名。</span><span class="sxs-lookup"><span data-stu-id="be370-171">Callee’s endpoint name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-172">CallerOS</span><span class="sxs-lookup"><span data-stu-id="be370-172">CallerOS</span></span></p></td>
<td><p><span data-ttu-id="be370-173">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="be370-173">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="be370-174">発信者のエンドポイントのオペレーティングシステム (OS)。</span><span class="sxs-lookup"><span data-stu-id="be370-174">Operating system (OS) of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-175">CalleeOS</span><span class="sxs-lookup"><span data-stu-id="be370-175">CalleeOS</span></span></p></td>
<td><p><span data-ttu-id="be370-176">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="be370-176">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="be370-177">呼び出し先のエンドポイントのオペレーティングシステム (OS)。</span><span class="sxs-lookup"><span data-stu-id="be370-177">Operating system (OS) of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-178">Caller</span><span class="sxs-lookup"><span data-stu-id="be370-178">CallerCPUName</span></span></p></td>
<td><p><span data-ttu-id="be370-179">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="be370-179">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="be370-180">呼び出し元のエンドポイントの CPU 名。</span><span class="sxs-lookup"><span data-stu-id="be370-180">CPU name of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-181">CalleeCPUName</span><span class="sxs-lookup"><span data-stu-id="be370-181">CalleeCPUName</span></span></p></td>
<td><p><span data-ttu-id="be370-182">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="be370-182">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="be370-183">呼び出し先のエンドポイントの CPU 名。</span><span class="sxs-lookup"><span data-stu-id="be370-183">CPU name of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-184">CallerCPUNumberOfCores</span><span class="sxs-lookup"><span data-stu-id="be370-184">CallerCPUNumberOfCores</span></span></p></td>
<td><p><span data-ttu-id="be370-185">smallint</span><span class="sxs-lookup"><span data-stu-id="be370-185">smallint</span></span></p></td>
<td><p><span data-ttu-id="be370-186">呼び出し元のエンドポイントの CPU コアの数。</span><span class="sxs-lookup"><span data-stu-id="be370-186">Number of CPU cores of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-187">CalleeCPUNumberOfCores</span><span class="sxs-lookup"><span data-stu-id="be370-187">CalleeCPUNumberOfCores</span></span></p></td>
<td><p><span data-ttu-id="be370-188">smallint</span><span class="sxs-lookup"><span data-stu-id="be370-188">smallint</span></span></p></td>
<td><p><span data-ttu-id="be370-189">呼び出し先のエンドポイントの CPU コアの数。</span><span class="sxs-lookup"><span data-stu-id="be370-189">Number of CPU cores of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-190">Callerプロセッサーの速度</span><span class="sxs-lookup"><span data-stu-id="be370-190">CallerCPUProcessorSpeed</span></span></p></td>
<td><p><span data-ttu-id="be370-191">int</span><span class="sxs-lookup"><span data-stu-id="be370-191">int</span></span></p></td>
<td><p><span data-ttu-id="be370-192">発信者のエンドポイントの CPU プロセッサ速度。</span><span class="sxs-lookup"><span data-stu-id="be370-192">CPU processor speed of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-193">Calleecpuプロセッサー速度</span><span class="sxs-lookup"><span data-stu-id="be370-193">CalleeCPUProcessorSpeed</span></span></p></td>
<td><p><span data-ttu-id="be370-194">int</span><span class="sxs-lookup"><span data-stu-id="be370-194">int</span></span></p></td>
<td><p><span data-ttu-id="be370-195">呼び出し先のエンドポイントの CPU プロセッサ速度。</span><span class="sxs-lookup"><span data-stu-id="be370-195">CPU processor speed of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-196">CallerVirtualizationFlag</span><span class="sxs-lookup"><span data-stu-id="be370-196">CallerVirtualizationFlag</span></span></p></td>
<td><p><span data-ttu-id="be370-197">tinyint</span><span class="sxs-lookup"><span data-stu-id="be370-197">tinyint</span></span></p></td>
<td><p><span data-ttu-id="be370-198">呼び出し元のシステムが仮想環境で実行されているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="be370-198">Indicates whether the caller’s system is running in a virtualized environment.</span></span> <span data-ttu-id="be370-199">詳細については、「 <a href="lync-server-2013-endpoint-table.md">Lync Server 2013 のエンドポイントテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="be370-199">See the <a href="lync-server-2013-endpoint-table.md">Endpoint table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-200">CalleeVirtualizationFlag</span><span class="sxs-lookup"><span data-stu-id="be370-200">CalleeVirtualizationFlag</span></span></p></td>
<td><p><span data-ttu-id="be370-201">tinyint</span><span class="sxs-lookup"><span data-stu-id="be370-201">tinyint</span></span></p></td>
<td><p><span data-ttu-id="be370-202">呼び出し先のシステムが仮想環境で実行されているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="be370-202">Indicates whether the callee’s system is running in a virtualized environment.</span></span> <span data-ttu-id="be370-203">詳細については、「 <a href="lync-server-2013-endpoint-table.md">Lync Server 2013 のエンドポイントテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="be370-203">See the <a href="lync-server-2013-endpoint-table.md">Endpoint table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-204">ConnectivityIce</span><span class="sxs-lookup"><span data-stu-id="be370-204">ConnectivityIce</span></span></p></td>
<td><p><span data-ttu-id="be370-205">tinyint</span><span class="sxs-lookup"><span data-stu-id="be370-205">tinyint</span></span></p></td>
<td><p><span data-ttu-id="be370-206">メディアパスについての情報 (ダイレクトまたは中継など)</span><span class="sxs-lookup"><span data-stu-id="be370-206">Information about media path, such as direct or relayed.</span></span> <span data-ttu-id="be370-207">詳細については、「 <a href="lync-server-2013-medialine-table.md">Lync Server 2013 の MediaLine テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="be370-207">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-208">CallerIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="be370-208">CallerIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="be370-209">int</span><span class="sxs-lookup"><span data-stu-id="be370-209">int</span></span></p></td>
<td><p><span data-ttu-id="be370-210">発信者の bits フラグで説明されている対話型接続確立 (ICE) プロセスに関する情報。</span><span class="sxs-lookup"><span data-stu-id="be370-210">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the caller.</span></span> <span data-ttu-id="be370-211">詳細については、「エクスペリエンスの品質監視サーバープロトコルの仕様」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="be370-211">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-212">CalleeIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="be370-212">CalleeIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="be370-213">int</span><span class="sxs-lookup"><span data-stu-id="be370-213">int</span></span></p></td>
<td><p><span data-ttu-id="be370-214">対話式接続確立 (ICE) プロセスについて詳しくは、「呼び出し先のビットフラグ」で説明します。</span><span class="sxs-lookup"><span data-stu-id="be370-214">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the callee.</span></span> <span data-ttu-id="be370-215">詳細については、「エクスペリエンスの品質監視サーバープロトコルの仕様」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="be370-215">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-216">Transport</span><span class="sxs-lookup"><span data-stu-id="be370-216">Transport</span></span></p></td>
<td><p><span data-ttu-id="be370-217">int</span><span class="sxs-lookup"><span data-stu-id="be370-217">int</span></span></p></td>
<td><p><span data-ttu-id="be370-218">トランスポートの種類: 0 は UDP、1は TCP です。</span><span class="sxs-lookup"><span data-stu-id="be370-218">Transport type: 0 is UDP, 1 is TCP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-219">CallerIPAddr</span><span class="sxs-lookup"><span data-stu-id="be370-219">CallerIPAddr</span></span></p></td>
<td><p><span data-ttu-id="be370-220">var (50)</span><span class="sxs-lookup"><span data-stu-id="be370-220">var(50)</span></span></p></td>
<td><p><span data-ttu-id="be370-221">発信者の IP アドレス。</span><span class="sxs-lookup"><span data-stu-id="be370-221">IP address of the caller.</span></span> <span data-ttu-id="be370-222">これは IPv4 または IPv6 アドレスのいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="be370-222">This may be either an IPv4 or an IPv6 address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-223">CallerPort</span><span class="sxs-lookup"><span data-stu-id="be370-223">CallerPort</span></span></p></td>
<td><p><span data-ttu-id="be370-224">int</span><span class="sxs-lookup"><span data-stu-id="be370-224">int</span></span></p></td>
<td><p><span data-ttu-id="be370-225">発信者によって使用されるポート。</span><span class="sxs-lookup"><span data-stu-id="be370-225">Port used by the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-226">CallerInside</span><span class="sxs-lookup"><span data-stu-id="be370-226">CallerInside</span></span></p></td>
<td><p><span data-ttu-id="be370-227">bit</span><span class="sxs-lookup"><span data-stu-id="be370-227">bit</span></span></p></td>
<td><p><span data-ttu-id="be370-228">発信者が組織のネットワーク内にあるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="be370-228">Indicates whether the caller is inside the organization network.</span></span> <span data-ttu-id="be370-229">1: 発信者がエンタープライズネットワーク内にあることを示します。0は、呼び出し元がネットワークの外部にあることを意味します。</span><span class="sxs-lookup"><span data-stu-id="be370-229">1 means caller is inside the enterprise network, 0 means the caller is outside the network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-230">CalleeIPAddr</span><span class="sxs-lookup"><span data-stu-id="be370-230">CalleeIPAddr</span></span></p></td>
<td><p><span data-ttu-id="be370-231">var (50)</span><span class="sxs-lookup"><span data-stu-id="be370-231">var(50)</span></span></p></td>
<td><p><span data-ttu-id="be370-232">呼び出し先の IP アドレス。</span><span class="sxs-lookup"><span data-stu-id="be370-232">IP address of the callee.</span></span> <span data-ttu-id="be370-233">これは IPv4 または IPv6 アドレスのいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="be370-233">This may be either an IPv4 or an IPv6 address.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-234">CalleePort</span><span class="sxs-lookup"><span data-stu-id="be370-234">CalleePort</span></span></p></td>
<td><p><span data-ttu-id="be370-235">int</span><span class="sxs-lookup"><span data-stu-id="be370-235">int</span></span></p></td>
<td><p><span data-ttu-id="be370-236">呼び出し先によって使用されるポート。</span><span class="sxs-lookup"><span data-stu-id="be370-236">Port used by the callee.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-237">CalleeInside</span><span class="sxs-lookup"><span data-stu-id="be370-237">CalleeInside</span></span></p></td>
<td><p><span data-ttu-id="be370-238">bit</span><span class="sxs-lookup"><span data-stu-id="be370-238">bit</span></span></p></td>
<td><p><span data-ttu-id="be370-239">発信者が組織のネットワーク内にあるかどうかを示します。1は、呼び出し元がエンタープライズネットワーク内にあることを意味します。0は、呼び出し先がネットワークの外部にあることを意味します。</span><span class="sxs-lookup"><span data-stu-id="be370-239">Indicates whether the caller is inside the organization network.1 means callee is inside the enterprise network, 0 means the callee is outside the network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-240">CallerUserSite</span><span class="sxs-lookup"><span data-stu-id="be370-240">CallerUserSite</span></span></p></td>
<td><p><span data-ttu-id="be370-241">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="be370-241">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="be370-242">発信者のサイトの名前。</span><span class="sxs-lookup"><span data-stu-id="be370-242">Name of the caller’s site.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-243">CallerRegion</span><span class="sxs-lookup"><span data-stu-id="be370-243">CallerRegion</span></span></p></td>
<td><p><span data-ttu-id="be370-244">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="be370-244">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="be370-245">発信者のサイトの国/地域の名前です。</span><span class="sxs-lookup"><span data-stu-id="be370-245">Name of the country/region of the caller’s site.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-246">CalleeUserSite</span><span class="sxs-lookup"><span data-stu-id="be370-246">CalleeUserSite</span></span></p></td>
<td><p><span data-ttu-id="be370-247">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="be370-247">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="be370-248">呼び出し先のサイトの名前。</span><span class="sxs-lookup"><span data-stu-id="be370-248">Name of the callee’s site.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-249">CalleeRegion</span><span class="sxs-lookup"><span data-stu-id="be370-249">CalleeRegion</span></span></p></td>
<td><p><span data-ttu-id="be370-250">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="be370-250">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="be370-251">呼び出し先のサイトの国/地域の名前です。</span><span class="sxs-lookup"><span data-stu-id="be370-251">Name of the country/region of the callee’s site.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-252">CallerRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="be370-252">CallerRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="be370-253">var (50)</span><span class="sxs-lookup"><span data-stu-id="be370-253">var(50)</span></span></p></td>
<td><p><span data-ttu-id="be370-254">発信者によって使用される A/V Edge サービスの IP アドレス。</span><span class="sxs-lookup"><span data-stu-id="be370-254">IP Address of the A/V Edge service used by the caller.</span></span> <span data-ttu-id="be370-255">詳細については、「 <a href="lync-server-2013-ipaddress-table.md">Lync Server 2013 の IPAddress テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="be370-255">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-256">CallerRelayPort</span><span class="sxs-lookup"><span data-stu-id="be370-256">CallerRelayPort</span></span></p></td>
<td><p><span data-ttu-id="be370-257">int</span><span class="sxs-lookup"><span data-stu-id="be370-257">int</span></span></p></td>
<td><p><span data-ttu-id="be370-258">発信者によって使用される A/V Edge サービス上のポート。</span><span class="sxs-lookup"><span data-stu-id="be370-258">Port on the A/V Edge service used by the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-259">CalleeRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="be370-259">CalleeRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="be370-260">var (50)</span><span class="sxs-lookup"><span data-stu-id="be370-260">var(50)</span></span></p></td>
<td><p><span data-ttu-id="be370-261">呼び出し先によって使用される A/V エッジサービスの IP アドレスキー。</span><span class="sxs-lookup"><span data-stu-id="be370-261">IP Address key of the A/V Edge service used by the callee.</span></span> <span data-ttu-id="be370-262">詳細については、「 <a href="lync-server-2013-ipaddress-table.md">Lync Server 2013 の IPAddress テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="be370-262">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-263">CalleeRelayPort</span><span class="sxs-lookup"><span data-stu-id="be370-263">CalleeRelayPort</span></span></p></td>
<td><p><span data-ttu-id="be370-264">int</span><span class="sxs-lookup"><span data-stu-id="be370-264">int</span></span></p></td>
<td><p><span data-ttu-id="be370-265">呼び出し先によって使用される A/V エッジサービスのポート。</span><span class="sxs-lookup"><span data-stu-id="be370-265">Port on the A/V Edge service used by the callee.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-266">CallerCaptureDev</span><span class="sxs-lookup"><span data-stu-id="be370-266">CallerCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="be370-267">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="be370-267">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="be370-268">発信者のキャプチャデバイス名。</span><span class="sxs-lookup"><span data-stu-id="be370-268">Caller’s capture device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-269">CallerRenderDev</span><span class="sxs-lookup"><span data-stu-id="be370-269">CallerRenderDev</span></span></p></td>
<td><p><span data-ttu-id="be370-270">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="be370-270">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="be370-271">発信者のレンダーデバイス名。</span><span class="sxs-lookup"><span data-stu-id="be370-271">Caller’s render device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-272">CallerCaptureDevDriver</span><span class="sxs-lookup"><span data-stu-id="be370-272">CallerCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="be370-273">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="be370-273">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="be370-274">発信者のキャプチャデバイスドライバー名。</span><span class="sxs-lookup"><span data-stu-id="be370-274">Caller’s capture device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-275">CallerRenderDevDriver</span><span class="sxs-lookup"><span data-stu-id="be370-275">CallerRenderDevDriver</span></span></p></td>
<td><p><span data-ttu-id="be370-276">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="be370-276">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="be370-277">発信者のレンダーデバイスドライバー名。</span><span class="sxs-lookup"><span data-stu-id="be370-277">Caller’s render device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-278">Calleecapdev</span><span class="sxs-lookup"><span data-stu-id="be370-278">CalleeCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="be370-279">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="be370-279">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="be370-280">呼び出し先のキャプチャデバイス名。</span><span class="sxs-lookup"><span data-stu-id="be370-280">Callee’s capture device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-281">Calle・ Enderdev</span><span class="sxs-lookup"><span data-stu-id="be370-281">CalleeRenderDev</span></span></p></td>
<td><p><span data-ttu-id="be370-282">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="be370-282">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="be370-283">呼び出し先のレンダリングデバイス名。</span><span class="sxs-lookup"><span data-stu-id="be370-283">Callee’s render device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-284">Callecap・ Devdriver</span><span class="sxs-lookup"><span data-stu-id="be370-284">CalleCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="be370-285">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="be370-285">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="be370-286">呼び出し先のキャプチャデバイスドライバー名。</span><span class="sxs-lookup"><span data-stu-id="be370-286">Callee’s capture device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-287">CalleeRenderDevDriver</span><span class="sxs-lookup"><span data-stu-id="be370-287">CalleeRenderDevDriver</span></span></p></td>
<td><p><span data-ttu-id="be370-288">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="be370-288">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="be370-289">呼び出し先のレンダリングデバイスドライバー名。</span><span class="sxs-lookup"><span data-stu-id="be370-289">Callee’s render device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-290">CallerNetworkConnectionType</span><span class="sxs-lookup"><span data-stu-id="be370-290">CallerNetworkConnectionType</span></span></p></td>
<td><p><span data-ttu-id="be370-291">tinyint</span><span class="sxs-lookup"><span data-stu-id="be370-291">tinyint</span></span></p></td>
<td><p><span data-ttu-id="be370-292">発信者のネットワーク接続の種類: 0 は有線、1はワイヤレス。</span><span class="sxs-lookup"><span data-stu-id="be370-292">Caller’s network connection type: 0 is wired, 1 is wireless.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-293">CallerVPN</span><span class="sxs-lookup"><span data-stu-id="be370-293">CallerVPN</span></span></p></td>
<td><p><span data-ttu-id="be370-294">bit</span><span class="sxs-lookup"><span data-stu-id="be370-294">bit</span></span></p></td>
<td><p><span data-ttu-id="be370-295">発信者が仮想プライベートネットワーク経由で接続しているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="be370-295">Indicates whether or not the caller connected over a virtual private network.</span></span> <span data-ttu-id="be370-296">1は仮想プライベートネットワーク (VPN)、0は非 VPN です。</span><span class="sxs-lookup"><span data-stu-id="be370-296">1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-297">CallerLinkSpeed</span><span class="sxs-lookup"><span data-stu-id="be370-297">CallerLinkSpeed</span></span></p></td>
<td><p><span data-ttu-id="be370-298">10進数 (18,)</span><span class="sxs-lookup"><span data-stu-id="be370-298">decimal(18,)</span></span></p></td>
<td><p><span data-ttu-id="be370-299">発信者のエンドポイントのネットワークリンク速度 (bps)。</span><span class="sxs-lookup"><span data-stu-id="be370-299">Network link speed for the caller's endpoint in bps.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-300">CalleeNetworkConnectionType</span><span class="sxs-lookup"><span data-stu-id="be370-300">CalleeNetworkConnectionType</span></span></p></td>
<td><p><span data-ttu-id="be370-301">tinyint</span><span class="sxs-lookup"><span data-stu-id="be370-301">tinyint</span></span></p></td>
<td><p><span data-ttu-id="be370-302">呼び出し先のネットワーク接続の種類: 0 は有線、1はワイヤレス。</span><span class="sxs-lookup"><span data-stu-id="be370-302">Callee’s network connection type: 0 is wired, 1 is wireless.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-303">CalleeVPN</span><span class="sxs-lookup"><span data-stu-id="be370-303">CalleeVPN</span></span></p></td>
<td><p><span data-ttu-id="be370-304">bit</span><span class="sxs-lookup"><span data-stu-id="be370-304">bit</span></span></p></td>
<td><p><span data-ttu-id="be370-305">呼び出し先が仮想プライベートネットワーク経由で接続されているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="be370-305">Indicates whether or not the callee connected over a virtual private network.</span></span> <span data-ttu-id="be370-306">1は仮想プライベートネットワーク (VPN)、0は非 VPN です。</span><span class="sxs-lookup"><span data-stu-id="be370-306">1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-307">CalleeLinkSpeed</span><span class="sxs-lookup"><span data-stu-id="be370-307">CalleeLinkSpeed</span></span></p></td>
<td><p><span data-ttu-id="be370-308">10進数 (18, 0)</span><span class="sxs-lookup"><span data-stu-id="be370-308">decimal(18,0)</span></span></p></td>
<td><p><span data-ttu-id="be370-309">転送先のエンドポイントのネットワークリンク速度 (bps)。</span><span class="sxs-lookup"><span data-stu-id="be370-309">Network link speed for the callee’s endpoint (in bps).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-310">ConversationalMOS</span><span class="sxs-lookup"><span data-stu-id="be370-310">ConversationalMOS</span></span></p></td>
<td><p><span data-ttu-id="be370-311">10進数 (3, 2)</span><span class="sxs-lookup"><span data-stu-id="be370-311">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="be370-312">オーディオセッションの会話 MOS を Narrowband します (両方のオーディオストリームに基づく)。</span><span class="sxs-lookup"><span data-stu-id="be370-312">Narrowband Conversational MOS of the audio sessions (based on both audio streams).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-313">AppliedBandwidthLimit</span><span class="sxs-lookup"><span data-stu-id="be370-313">AppliedBandwidthLimit</span></span></p></td>
<td><p><span data-ttu-id="be370-314">int</span><span class="sxs-lookup"><span data-stu-id="be370-314">int</span></span></p></td>
<td><p><span data-ttu-id="be370-315">さまざまなポリシー設定 (TURN、API、SDP、ポリシーサーバーなど) が指定された send side ストリームに適用される実際の帯域幅。</span><span class="sxs-lookup"><span data-stu-id="be370-315">Actual bandwidth applied to the given send side stream given various policy settings (TURN, API, SDP, Policy Server, and so on).</span></span> <span data-ttu-id="be370-316">これは、帯域幅の推定値に基づいて低帯域幅を使用できるため、有効帯域幅と混同しないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="be370-316">This is not to be confused with the effective bandwidth because there can be a lower effective bandwidth based on the bandwidth estimate.</span></span> <span data-ttu-id="be370-317">これは基本的に最大帯域幅であり、送信ストリームは、帯域幅の推定値によって課された制限を受けません。</span><span class="sxs-lookup"><span data-stu-id="be370-317">This is basically the maximum bandwidth the send stream can take barring limits imposed by the bandwidth estimate.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-318">JitterInterArrival</span><span class="sxs-lookup"><span data-stu-id="be370-318">JitterInterArrival</span></span></p></td>
<td><p><span data-ttu-id="be370-319">int</span><span class="sxs-lookup"><span data-stu-id="be370-319">int</span></span></p></td>
<td><p><span data-ttu-id="be370-320">リアルタイム制御プロトコル (RTCP) の統計情報からの平均ネットワークジッター。</span><span class="sxs-lookup"><span data-stu-id="be370-320">Average network jitter from Real Time Control Protocol (RTCP) statistics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-321">JitterInterArrivalMax</span><span class="sxs-lookup"><span data-stu-id="be370-321">JitterInterArrivalMax</span></span></p></td>
<td><p><span data-ttu-id="be370-322">int</span><span class="sxs-lookup"><span data-stu-id="be370-322">int</span></span></p></td>
<td><p><span data-ttu-id="be370-323">通話中の最大ネットワークジッター。</span><span class="sxs-lookup"><span data-stu-id="be370-323">Maximum network jitter during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-324">RoundTrip</span><span class="sxs-lookup"><span data-stu-id="be370-324">RoundTrip</span></span></p></td>
<td><p><span data-ttu-id="be370-325">int</span><span class="sxs-lookup"><span data-stu-id="be370-325">int</span></span></p></td>
<td><p><span data-ttu-id="be370-326">RTCP の統計情報からのラウンドトリップ時間。</span><span class="sxs-lookup"><span data-stu-id="be370-326">Round trip time from RTCP statistics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-327">RoundTripMax</span><span class="sxs-lookup"><span data-stu-id="be370-327">RoundTripMax</span></span></p></td>
<td><p><span data-ttu-id="be370-328">int</span><span class="sxs-lookup"><span data-stu-id="be370-328">int</span></span></p></td>
<td><p><span data-ttu-id="be370-329">オーディオストリームの最大ラウンドトリップ時間。</span><span class="sxs-lookup"><span data-stu-id="be370-329">Maximum round trip time for the audio stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-330">PacketLossRate</span><span class="sxs-lookup"><span data-stu-id="be370-330">PacketLossRate</span></span></p></td>
<td><p><span data-ttu-id="be370-331">10進数 (5, 4)</span><span class="sxs-lookup"><span data-stu-id="be370-331">decimal(5,4)</span></span></p></td>
<td><p><span data-ttu-id="be370-332">通話中の平均パケット損失率。</span><span class="sxs-lookup"><span data-stu-id="be370-332">Average packet loss rate during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-333">PacketLossRateMax</span><span class="sxs-lookup"><span data-stu-id="be370-333">PacketLossRateMax</span></span></p></td>
<td><p><span data-ttu-id="be370-334">10進数 (5, 4)</span><span class="sxs-lookup"><span data-stu-id="be370-334">decimal(5,4)</span></span></p></td>
<td><p><span data-ttu-id="be370-335">通話中に発生したパケット損失の上限。</span><span class="sxs-lookup"><span data-stu-id="be370-335">Maximum packet loss observed during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-336">PacketUtilization</span><span class="sxs-lookup"><span data-stu-id="be370-336">PacketUtilization</span></span></p></td>
<td><p><span data-ttu-id="be370-337">int</span><span class="sxs-lookup"><span data-stu-id="be370-337">int</span></span></p></td>
<td><p><span data-ttu-id="be370-338">ビデオストリームのパケット数 (リアルタイムトランスポートプロトコル、RTP)。</span><span class="sxs-lookup"><span data-stu-id="be370-338">Packet count for the video stream (Real Time Transport Protocol, RTP).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-339">BandwidthEst</span><span class="sxs-lookup"><span data-stu-id="be370-339">BandwidthEst</span></span></p></td>
<td><p><span data-ttu-id="be370-340">int</span><span class="sxs-lookup"><span data-stu-id="be370-340">int</span></span></p></td>
<td><p><span data-ttu-id="be370-341">オーディオストリームの帯域幅の推定。</span><span class="sxs-lookup"><span data-stu-id="be370-341">Bandwidth estimates for the audio stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-342">PayloadDescription</span><span class="sxs-lookup"><span data-stu-id="be370-342">PayloadDescription</span></span></p></td>
<td><p><span data-ttu-id="be370-343">int</span><span class="sxs-lookup"><span data-stu-id="be370-343">int</span></span></p></td>
<td><p><span data-ttu-id="be370-344">通話に使用されるオーディオコーデック。 <a href="lync-server-2013-payloaddescription-table.md">Lync Server 2013 の PayloadDescription テーブル</a>から参照されています。</span><span class="sxs-lookup"><span data-stu-id="be370-344">Audio codec used for the call, referenced from the <a href="lync-server-2013-payloaddescription-table.md">PayloadDescription table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-345">VideoResolution</span><span class="sxs-lookup"><span data-stu-id="be370-345">VideoResolution</span></span></p></td>
<td><p><span data-ttu-id="be370-346">char (9)</span><span class="sxs-lookup"><span data-stu-id="be370-346">char(9)</span></span></p></td>
<td><p><span data-ttu-id="be370-347">ピクセル幅にピクセルの高さを掛けたビデオの解像度。</span><span class="sxs-lookup"><span data-stu-id="be370-347">Resolution of the video in pixels width multiplied by pixels height.</span></span> <span data-ttu-id="be370-348">文字列として報告されます。</span><span class="sxs-lookup"><span data-stu-id="be370-348">Reported as a string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-349">VideoBitRateAvg</span><span class="sxs-lookup"><span data-stu-id="be370-349">VideoBitRateAvg</span></span></p></td>
<td><p><span data-ttu-id="be370-350">int</span><span class="sxs-lookup"><span data-stu-id="be370-350">int</span></span></p></td>
<td><p><span data-ttu-id="be370-351">ビデオストリームの平均ビットレート。</span><span class="sxs-lookup"><span data-stu-id="be370-351">Average bit rate of the video stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-352">InboundVideoFrameRateAvg</span><span class="sxs-lookup"><span data-stu-id="be370-352">InboundVideoFrameRateAvg</span></span></p></td>
<td><p><span data-ttu-id="be370-353">10進数 (9, 4)</span><span class="sxs-lookup"><span data-stu-id="be370-353">decimal(9,4)</span></span></p></td>
<td><p><span data-ttu-id="be370-354">受信したビデオのフレームレート。</span><span class="sxs-lookup"><span data-stu-id="be370-354">Frame rate of video received.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-355">OutboundVideoFrameRateAvg</span><span class="sxs-lookup"><span data-stu-id="be370-355">OutboundVideoFrameRateAvg</span></span></p></td>
<td><p><span data-ttu-id="be370-356">10進数 (9, 4)</span><span class="sxs-lookup"><span data-stu-id="be370-356">decimal(9,4)</span></span></p></td>
<td><p><span data-ttu-id="be370-357">送信されたビデオのフレームレート。</span><span class="sxs-lookup"><span data-stu-id="be370-357">Frame rate of video sent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-358">ViideoBitRateMax</span><span class="sxs-lookup"><span data-stu-id="be370-358">ViideoBitRateMax</span></span></p></td>
<td><p><span data-ttu-id="be370-359">int</span><span class="sxs-lookup"><span data-stu-id="be370-359">int</span></span></p></td>
<td><p><span data-ttu-id="be370-360">ビデオセッション中の最大ビデオビットレート。</span><span class="sxs-lookup"><span data-stu-id="be370-360">Maximum video bit rate during the video session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-361">パケット損失率</span><span class="sxs-lookup"><span data-stu-id="be370-361">VideoPacketLossRate</span></span></p></td>
<td><p><span data-ttu-id="be370-362">10進数 (9, 4)</span><span class="sxs-lookup"><span data-stu-id="be370-362">decimal(9,4)</span></span></p></td>
<td><p><span data-ttu-id="be370-363">ビデオパケットが失われた速度。</span><span class="sxs-lookup"><span data-stu-id="be370-363">Rate at which video packets were lost.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-364">VideoFrameLossRate</span><span class="sxs-lookup"><span data-stu-id="be370-364">VideoFrameLossRate</span></span></p></td>
<td><p><span data-ttu-id="be370-365">10進数 (9.4)</span><span class="sxs-lookup"><span data-stu-id="be370-365">decimal(9.4)</span></span></p></td>
<td><p><span data-ttu-id="be370-366">失われたビデオフレームの合計のパーセンテージ。</span><span class="sxs-lookup"><span data-stu-id="be370-366">Percentage of total video frames that are lost.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-367">VideoFEC</span><span class="sxs-lookup"><span data-stu-id="be370-367">VideoFEC</span></span></p></td>
<td><p><span data-ttu-id="be370-368">bit</span><span class="sxs-lookup"><span data-stu-id="be370-368">bit</span></span></p></td>
<td><p><span data-ttu-id="be370-369">使用されません。</span><span class="sxs-lookup"><span data-stu-id="be370-369">Not used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-370">VideoAllocateBWAvg</span><span class="sxs-lookup"><span data-stu-id="be370-370">VideoAllocateBWAvg</span></span></p></td>
<td><p><span data-ttu-id="be370-371">int</span><span class="sxs-lookup"><span data-stu-id="be370-371">int</span></span></p></td>
<td><p><span data-ttu-id="be370-372">ビデオに割り当てられている平均帯域幅。</span><span class="sxs-lookup"><span data-stu-id="be370-372">Average amount of bandwidth allocated for video.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be370-373">ビデオ</span><span class="sxs-lookup"><span data-stu-id="be370-373">VideoLocalFrameLossPercentageAvg</span></span></p></td>
<td><p><span data-ttu-id="be370-374">10進数 (9.4)</span><span class="sxs-lookup"><span data-stu-id="be370-374">decimal(9.4)</span></span></p></td>
<td><p><span data-ttu-id="be370-375">紛失したビデオフレームの合計の割合。</span><span class="sxs-lookup"><span data-stu-id="be370-375">Percentage of total video frames that were lost.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be370-376">SenderIsCallerPAI</span><span class="sxs-lookup"><span data-stu-id="be370-376">SenderIsCallerPAI</span></span></p></td>
<td><p><span data-ttu-id="be370-377">bit</span><span class="sxs-lookup"><span data-stu-id="be370-377">bit</span></span></p></td>
<td><p><span data-ttu-id="be370-378">P がアサートした id 情報のストリームの方向。</span><span class="sxs-lookup"><span data-stu-id="be370-378">Stream direction for p-asserted identity information.</span></span> <span data-ttu-id="be370-379">1は、ストリームの方向を呼び出し元から呼び出し先に転送することを意味します。0は、ストリームの方向を呼び出し元から呼び出し元に転送します。</span><span class="sxs-lookup"><span data-stu-id="be370-379">1 means the stream direction is from the caller to the callee; 0 means the stream direction is from the callee to the caller.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="be370-380">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="be370-380">


</div>

<span> </span>

</div>

</div>

</span></span></div>

