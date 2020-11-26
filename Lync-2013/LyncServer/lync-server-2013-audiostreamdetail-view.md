---
title: 'Lync Server 2013: AudioStreamDetail ビュー'
description: 'Lync Server 2013: AudioStreamDetail ビュー。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AudioStreamDetail view
ms:assetid: b6a435b3-103c-41c4-96ed-33c3784534c0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721859(v=OCS.15)
ms:contentKeyID: 49733792
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 92c4c9bbb4f126e242e28d835222f6ba2af89d8b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438163"
---
# <a name="audiostreamdetail-view-in-lync-server-2013"></a><span data-ttu-id="8b0fb-103">Lync Server 2013 の AudioStreamDetail ビュー</span><span class="sxs-lookup"><span data-stu-id="8b0fb-103">AudioStreamDetail view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8b0fb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8b0fb-104">

<span> </span></span></span>

<span data-ttu-id="8b0fb-105">_**最終更新日:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="8b0fb-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="8b0fb-106">AudioStreamDetail ビューには、データベース内の各オーディオストリームに関する情報が格納されます。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-106">The AudioStreamDetail View stores information about each audio stream in the database.</span></span> <span data-ttu-id="8b0fb-107">このビューは、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8b0fb-108">列</span><span class="sxs-lookup"><span data-stu-id="8b0fb-108">Column</span></span></th>
<th><span data-ttu-id="8b0fb-109">データ型</span><span class="sxs-lookup"><span data-stu-id="8b0fb-109">Data Type</span></span></th>
<th><span data-ttu-id="8b0fb-110">詳細</span><span class="sxs-lookup"><span data-stu-id="8b0fb-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-111">セッション時間</span><span class="sxs-lookup"><span data-stu-id="8b0fb-111">SessionTime</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-112">datetime</span><span class="sxs-lookup"><span data-stu-id="8b0fb-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-113"><a href="lync-server-2013-medialine-table.md">Lync Server 2013 の MediaLine テーブル</a>から参照されている。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-113">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-114">SessionSeq</span><span class="sxs-lookup"><span data-stu-id="8b0fb-114">SessionSeq</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-115">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-115">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-116"><a href="lync-server-2013-medialine-table.md">Lync Server 2013 の MediaLine テーブル</a>から参照されている。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-116">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-117">StreamId</span><span class="sxs-lookup"><span data-stu-id="8b0fb-117">StreamId</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-118">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-118">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-119">メディアライン内の一意の ID。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-119">Unique ID within a media line.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-120">StartTime</span><span class="sxs-lookup"><span data-stu-id="8b0fb-120">StartTime</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-121">datetime</span><span class="sxs-lookup"><span data-stu-id="8b0fb-121">datetime</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-122">セッションの開始時刻。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-122">Start time of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-123">EndTime</span><span class="sxs-lookup"><span data-stu-id="8b0fb-123">EndTime</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-124">datetime</span><span class="sxs-lookup"><span data-stu-id="8b0fb-124">datetime</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-125">セッションの終了時刻。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-125">End time of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-126">このカテゴリ</span><span class="sxs-lookup"><span data-stu-id="8b0fb-126">DialogCategory</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-127">bit</span><span class="sxs-lookup"><span data-stu-id="8b0fb-127">bit</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-128">ダイアログカテゴリ: 0 は、仲介サーバー間の Lync サーバーです。1は PSTN ゲートウェイ区間の仲介サーバーです。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-128">Dialog category: 0 is the Lync Server to Mediation Server leg; 1 is the Mediation Server to PSTN gateway leg.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-129">MediationServerBypassFlag</span><span class="sxs-lookup"><span data-stu-id="8b0fb-129">MediationServerBypassFlag</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-130">bit</span><span class="sxs-lookup"><span data-stu-id="8b0fb-130">bit</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-131">通話がバイパスされたかどうかを示すフラグ。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-131">Flag indicating if the call was bypassed or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-132">Mediabypasswarnings フラグ</span><span class="sxs-lookup"><span data-stu-id="8b0fb-132">MediaBypassWarningFlag</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-133">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-133">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-134">存在する場合は、バイパス Id が一致した場合でも、通話がバイパスされなかった理由を示します。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-134">If present, indicates why a call was not bypassed even if the bypass IDs matched.</span></span> <span data-ttu-id="8b0fb-135">1つの値のみが定義されます。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-135">Only one value is defined:</span></span></p>
<p><span data-ttu-id="8b0fb-136">0x0001 –既定のネットワークアダプターの不明なバイパス ID。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-136">0x0001 – Unknown bypass ID for Default network adapter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-137">CallPriority</span><span class="sxs-lookup"><span data-stu-id="8b0fb-137">CallPriority</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-138">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-138">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-139">通話の優先度。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-139">Priority of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-140">CallerPool</span><span class="sxs-lookup"><span data-stu-id="8b0fb-140">CallerPool</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-141">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-141">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-142">発信者番号プールの FQDN。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-142">Caller pool FQDN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-143">CalleePool</span><span class="sxs-lookup"><span data-stu-id="8b0fb-143">CalleePool</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-144">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-144">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-145">呼び出し元プールの FQDN。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-145">Callee pool FQDN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-146">[発信者]</span><span class="sxs-lookup"><span data-stu-id="8b0fb-146">Caller</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-147">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-147">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-148">発信者の URI。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-148">Caller’s URI.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-149">[呼び出し先]</span><span class="sxs-lookup"><span data-stu-id="8b0fb-149">Callee</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-150">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-150">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-151">呼び出し先の URI。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-151">Callee’s URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-152">CallerUserAgent</span><span class="sxs-lookup"><span data-stu-id="8b0fb-152">CallerUserAgent</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-153">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-153">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-154">呼び出し元のユーザーエージェント文字列。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-154">Caller’s user agent string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-155">CallerUserAgentType</span><span class="sxs-lookup"><span data-stu-id="8b0fb-155">CallerUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-156">smallint</span><span class="sxs-lookup"><span data-stu-id="8b0fb-156">smallint</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-157">呼び出し元のユーザーエージェントの種類。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-157">Type of the caller’s user agent.</span></span> <span data-ttu-id="8b0fb-158">詳細については、「 <a href="lync-server-2013-useragent-table.md">Lync Server 2013 の UserAgent テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-158">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-159">CallerUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="8b0fb-159">CallerUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-160">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-160">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-161">発信者のユーザーエージェントのカテゴリ。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-161">Category of the caller’s user agent.</span></span> <span data-ttu-id="8b0fb-162">詳細については、「 <a href="lync-server-2013-useragentdef-table-qoe.md">Lync Server 2013 の Useragentdef テーブル (QoE)</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-162">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-163">CalleeUserAgent</span><span class="sxs-lookup"><span data-stu-id="8b0fb-163">CalleeUserAgent</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-164">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-164">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-165">呼び出し先のユーザーエージェント文字列。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-165">Callee’s user agent string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-166">CalleeUserAgentType</span><span class="sxs-lookup"><span data-stu-id="8b0fb-166">CalleeUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-167">smallint</span><span class="sxs-lookup"><span data-stu-id="8b0fb-167">smallint</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-168">呼び出し先のユーザーエージェントの種類。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-168">Type of callee’s user agent.</span></span> <span data-ttu-id="8b0fb-169">詳細については、「 <a href="lync-server-2013-useragent-table.md">Lync Server 2013 の UserAgent テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-169">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-170">CalleeUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="8b0fb-170">CalleeUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-171">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-171">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-172">呼び出し先のユーザーエージェントのカテゴリ。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-172">Category of callee’s user agent.</span></span> <span data-ttu-id="8b0fb-173">詳細については、「 <a href="lync-server-2013-useragentdef-table-qoe.md">Lync Server 2013 の Useragentdef テーブル (QoE)</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-173">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-174">CallerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8b0fb-174">CallerEndpoint</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-175">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-175">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-176">発信者のエンドポイント名。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-176">Caller’s endpoint name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-177">CalleeEndpoint</span><span class="sxs-lookup"><span data-stu-id="8b0fb-177">CalleeEndpoint</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-178">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-178">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-179">呼び出し先のエンドポイント名。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-179">Callee’s endpoint name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-180">CallerOS</span><span class="sxs-lookup"><span data-stu-id="8b0fb-180">CallerOS</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-181">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="8b0fb-181">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-182">発信者のエンドポイントのオペレーティングシステム (OS)。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-182">Operating system (OS) of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-183">CalleeOS</span><span class="sxs-lookup"><span data-stu-id="8b0fb-183">CalleeOS</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-184">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="8b0fb-184">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-185">呼び出し先のエンドポイントのオペレーティングシステム (OS)。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-185">Operating system (OS) of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-186">Caller</span><span class="sxs-lookup"><span data-stu-id="8b0fb-186">CallerCPUName</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-187">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="8b0fb-187">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-188">呼び出し元のエンドポイントの CPU 名。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-188">CPU name of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-189">CalleeCPUName</span><span class="sxs-lookup"><span data-stu-id="8b0fb-189">CalleeCPUName</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-190">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="8b0fb-190">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-191">呼び出し先のエンドポイントの CPU 名。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-191">CPU name of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-192">CallerCPUNumberOfCores</span><span class="sxs-lookup"><span data-stu-id="8b0fb-192">CallerCPUNumberOfCores</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-193">smallint</span><span class="sxs-lookup"><span data-stu-id="8b0fb-193">smallint</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-194">呼び出し元のエンドポイントの CPU コアの数。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-194">Number of CPU cores in the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-195">CalleeCPUNumberOfCores</span><span class="sxs-lookup"><span data-stu-id="8b0fb-195">CalleeCPUNumberOfCores</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-196">smallint</span><span class="sxs-lookup"><span data-stu-id="8b0fb-196">smallint</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-197">呼び出し先のエンドポイントの CPU コアの数です。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-197">Number of CPU cores in the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-198">Callerプロセッサーの速度</span><span class="sxs-lookup"><span data-stu-id="8b0fb-198">CallerCPUProcessorSpeed</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-199">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-199">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-200">発信者のエンドポイントの CPU プロセッサ速度。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-200">CPU processor speed of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-201">Calleecpuプロセッサー速度</span><span class="sxs-lookup"><span data-stu-id="8b0fb-201">CalleeCPUProcessorSpeed</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-202">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-202">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-203">呼び出し先のエンドポイントの CPU プロセッサ速度。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-203">CPU processor speed of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-204">CallerVirtualizationFlag</span><span class="sxs-lookup"><span data-stu-id="8b0fb-204">CallerVirtualizationFlag</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-205">tinyint</span><span class="sxs-lookup"><span data-stu-id="8b0fb-205">tinyint</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-206">呼び出し元のシステムが仮想環境で実行されているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-206">Indicates whether the caller’s system is running in a virtualized environment.</span></span> <span data-ttu-id="8b0fb-207">詳細については、「 <a href="lync-server-2013-endpoint-table.md">Lync Server 2013 のエンドポイントテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-207">See the <a href="lync-server-2013-endpoint-table.md">Endpoint table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-208">CalleeVirtualizationFlag</span><span class="sxs-lookup"><span data-stu-id="8b0fb-208">CalleeVirtualizationFlag</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-209">tinyint</span><span class="sxs-lookup"><span data-stu-id="8b0fb-209">tinyint</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-210">呼び出し先のシステムが仮想環境で実行されているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-210">Indicates whether the callee’s system is running in a virtualized environment.</span></span> <span data-ttu-id="8b0fb-211">詳細については、「 <a href="lync-server-2013-endpoint-table.md">Lync Server 2013 のエンドポイントテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-211">See the <a href="lync-server-2013-endpoint-table.md">Endpoint table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-212">CorrelationKey</span><span class="sxs-lookup"><span data-stu-id="8b0fb-212">CorrelationKey</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8b0fb-213">相関関係キー。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-213">Correlation key.</span></span> <span data-ttu-id="8b0fb-214"><a href="lync-server-2013-sessioncorrelation-table.md">Lync Server 2013 の Sessioncorrelation テーブル</a>から参照されます。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-214">Referenced from the <a href="lync-server-2013-sessioncorrelation-table.md">SessionCorrelation table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-215">ConnectivityIce</span><span class="sxs-lookup"><span data-stu-id="8b0fb-215">ConnectivityIce</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-216">tinyint</span><span class="sxs-lookup"><span data-stu-id="8b0fb-216">tinyint</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-217">メディアパスについての情報 (ダイレクトまたは中継など)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-217">Information about the media path, such as direct or relayed.</span></span> <span data-ttu-id="8b0fb-218">詳細については、「 <a href="lync-server-2013-medialine-table.md">Lync Server 2013 の MediaLine テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-218">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-219">CallerIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="8b0fb-219">CallerIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-220">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-220">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-221">発信者の bits フラグで説明されている対話型接続確立 (ICE) プロセスに関する情報。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-221">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the caller.</span></span> <span data-ttu-id="8b0fb-222">詳細については、「エクスペリエンスの品質監視サーバープロトコルの仕様」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-222">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-223">CalleeIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="8b0fb-223">CalleeIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-224">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-224">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-225">対話式接続確立 (ICE) プロセスについて詳しくは、「呼び出し先のビットフラグ」で説明します。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-225">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the callee.</span></span> <span data-ttu-id="8b0fb-226">詳細については、「エクスペリエンスの品質監視サーバープロトコルの仕様」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-226">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-227">Transport</span><span class="sxs-lookup"><span data-stu-id="8b0fb-227">Transport</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-228">tinyint</span><span class="sxs-lookup"><span data-stu-id="8b0fb-228">tinyint</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-229">トランスポートの種類: 0 は UDP、1は TCP です。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-229">Transport type: 0 is UDP, 1 is TCP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-230">CallerIPAddr</span><span class="sxs-lookup"><span data-stu-id="8b0fb-230">CallerIPAddr</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-231">var (50)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-231">var(50)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-232">発信者の IP アドレス。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-232">IP address of the caller.</span></span> <span data-ttu-id="8b0fb-233">これは IPv4 または IPv6 アドレスのいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-233">This may be either an IPv4 or an IPv6 address.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-234">CallerPort</span><span class="sxs-lookup"><span data-stu-id="8b0fb-234">CallerPort</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-235">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-235">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-236">発信者によって使用されるポート。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-236">Port used by the caller.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-237">CallerInside</span><span class="sxs-lookup"><span data-stu-id="8b0fb-237">CallerInside</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-238">bit</span><span class="sxs-lookup"><span data-stu-id="8b0fb-238">bit</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-239">発信者が間隔ネットワーク内にあるかどうかを示します。1は、発信者がエンタープライズネットワーク内にあることを意味します。0は、発信者がネットワークの外部にあることを意味します。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-239">Indicates whether the caller is inside the interval network: 1 means caller is inside the enterprise network, 0 means the caller is outside the network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-240">CalleeIPAddr</span><span class="sxs-lookup"><span data-stu-id="8b0fb-240">CalleeIPAddr</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-241">var (50)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-241">var(50)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-242">呼び出し先の IP アドレス。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-242">IP address of the callee.</span></span> <span data-ttu-id="8b0fb-243">これは IPv4 または IPv6 アドレスのいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-243">This may be either an IPv4 or an IPv6 address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-244">CalleePort</span><span class="sxs-lookup"><span data-stu-id="8b0fb-244">CalleePort</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-245">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-245">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-246">呼び出し先によって使用されるポート。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-246">Port used by the callee.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-247">CalleeInside</span><span class="sxs-lookup"><span data-stu-id="8b0fb-247">CalleeInside</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-248">bit</span><span class="sxs-lookup"><span data-stu-id="8b0fb-248">bit</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-249">呼び出し先が間隔ネットワーク内にあるかどうかを示します。1は、呼び出し先がエンタープライズネットワーク内にあることを意味します。0は、呼び出し先がネットワークの外部にあることを意味します。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-249">Indicates whether the callee is inside the interval network: 1 means callee is inside the enterprise network, 0 means the callee is outside the network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-250">CallerUserSite</span><span class="sxs-lookup"><span data-stu-id="8b0fb-250">CallerUserSite</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-251">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="8b0fb-251">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-252">発信者のサイトの名前。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-252">Name of the caller’s site.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-253">CallerRegion</span><span class="sxs-lookup"><span data-stu-id="8b0fb-253">CallerRegion</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-254">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="8b0fb-254">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-255">発信者のサイトの国/地域の名前です。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-255">Name of the country/region of the caller’s site.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-256">CalleeUserSite</span><span class="sxs-lookup"><span data-stu-id="8b0fb-256">CalleeUserSite</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-257">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="8b0fb-257">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-258">呼び出し先のサイトの名前。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-258">Name of the callee’s site.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-259">CalleeRegion</span><span class="sxs-lookup"><span data-stu-id="8b0fb-259">CalleeRegion</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-260">nvarchar(128</span><span class="sxs-lookup"><span data-stu-id="8b0fb-260">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-261">呼び出し先のサイトの国/地域の名前です。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-261">Name of the country/region of the callee’s site.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-262">CallerRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="8b0fb-262">CallerRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-263">var (50)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-263">var(50)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-264">発信者によって使用される A/V Edge サービスの IP アドレス。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-264">IP Address of the A/V Edge service used by the caller.</span></span> <span data-ttu-id="8b0fb-265">詳細については、「 <a href="lync-server-2013-ipaddress-table.md">Lync Server 2013 の IPAddress テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-265">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-266">CallerRelayPort</span><span class="sxs-lookup"><span data-stu-id="8b0fb-266">CallerRelayPort</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-267">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-267">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-268">発信者が使用する A/V Edge サービスで使用されるポート。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-268">Port used on the A/V Edge service used by the caller.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-269">CalleeRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="8b0fb-269">CalleeRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-270">var (50)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-270">var(50)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-271">呼び出し先によって使用される A/V エッジサービスの IP アドレスキー。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-271">IP Address key of the A/V Edge service used by the callee.</span></span> <span data-ttu-id="8b0fb-272">詳細については、「 <a href="lync-server-2013-ipaddress-table.md">Lync Server 2013 の IPAddress テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-272">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-273">CalleeRelayPort</span><span class="sxs-lookup"><span data-stu-id="8b0fb-273">CalleeRelayPort</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-274">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-274">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-275">呼び出し先によって使用される A/V Edge サービスで使用されるポート。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-275">Port used on the A/V Edge service used by the callee.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-276">CallerCaptureDev</span><span class="sxs-lookup"><span data-stu-id="8b0fb-276">CallerCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-277">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-277">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-278">発信者のキャプチャデバイス名。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-278">Caller’s capture device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-279">CallerRenderDev</span><span class="sxs-lookup"><span data-stu-id="8b0fb-279">CallerRenderDev</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-280">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-280">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-281">発信者のレンダーデバイス名。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-281">Caller’s render device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-282">CallerCaptureDevDriver</span><span class="sxs-lookup"><span data-stu-id="8b0fb-282">CallerCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-283">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-283">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-284">発信者のキャプチャデバイスドライバー名。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-284">Caller’s capture device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-285">CallerRenderDriver</span><span class="sxs-lookup"><span data-stu-id="8b0fb-285">CallerRenderDriver</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-286">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-286">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-287">発信者のレンダーデバイスドライバー名。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-287">Caller’s render device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-288">Calleecapdev</span><span class="sxs-lookup"><span data-stu-id="8b0fb-288">CalleeCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-289">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-289">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-290">呼び出し先のキャプチャデバイス名。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-290">Callee’s capture device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-291">Calle・ Enderdev</span><span class="sxs-lookup"><span data-stu-id="8b0fb-291">CalleeRenderDev</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-292">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-292">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-293">呼び出し先のレンダリングデバイス名。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-293">Callee’s render device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-294">Calleecapdevdriver</span><span class="sxs-lookup"><span data-stu-id="8b0fb-294">CalleeCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-295">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-295">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-296">呼び出し先のキャプチャデバイスドライバー名。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-296">Callee’s capture device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-297">CalleeRenderDevDriver</span><span class="sxs-lookup"><span data-stu-id="8b0fb-297">CalleeRenderDevDriver</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-298">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-298">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-299">呼び出し先のレンダリングデバイスドライバー名。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-299">Callee’s render device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-300">CallerNetworkConnectionType</span><span class="sxs-lookup"><span data-stu-id="8b0fb-300">CallerNetworkConnectionType</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-301">tinyint</span><span class="sxs-lookup"><span data-stu-id="8b0fb-301">tinyint</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-302">発信者のネットワーク接続の種類: 0 は有線、1はワイヤレス。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-302">Caller’s network connection type: 0 is wired, 1 is wireless.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-303">CallerVPN</span><span class="sxs-lookup"><span data-stu-id="8b0fb-303">CallerVPN</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-304">bit</span><span class="sxs-lookup"><span data-stu-id="8b0fb-304">bit</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-305">発信者が仮想プライベートネットワーク経由で接続しているかどうかを示します。1は仮想プライベートネットワーク (VPN)、0は VPN 以外。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-305">Indicates whether the caller connected over a virtual private network: 1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-306">CallerLinkSpeed</span><span class="sxs-lookup"><span data-stu-id="8b0fb-306">CallerLinkSpeed</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-307">10進数 (18, 0)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-307">decimal(18,0)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-308">発信者のエンドポイントのネットワークリンク速度 (bps)。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-308">Network link speed for the caller's endpoint in bps.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-309">CalleeNetworkConnectionType</span><span class="sxs-lookup"><span data-stu-id="8b0fb-309">CalleeNetworkConnectionType</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-310">tinyint</span><span class="sxs-lookup"><span data-stu-id="8b0fb-310">tinyint</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-311">呼び出し先のネットワーク接続の種類: 0 は有線、1はワイヤレス。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-311">Callee’s network connection type: 0 is wired, 1 is wireless.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-312">CalleeVPN</span><span class="sxs-lookup"><span data-stu-id="8b0fb-312">CalleeVPN</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-313">bit</span><span class="sxs-lookup"><span data-stu-id="8b0fb-313">bit</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-314">発信者が仮想プライベートネットワーク経由で接続しているかどうかを示します。1は仮想プライベートネットワーク (VPN)、0は VPN 以外。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-314">Indicates whether the caller connected over a virtual private network: 1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-315">CalleeLinkSpeed</span><span class="sxs-lookup"><span data-stu-id="8b0fb-315">CalleeLinkSpeed</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-316">10進数 (18, 0)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-316">decimal(18,0)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-317">転送先のエンドポイントのネットワークリンク速度 (bps)。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-317">Network link speed for the callee's endpoint in bps.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-318">ConversationalMOS</span><span class="sxs-lookup"><span data-stu-id="8b0fb-318">ConversationalMOS</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-319">10進数 (3, 2)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-319">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-320">オーディオセッションの会話 MOS を Narrowband します (両方のオーディオストリームに基づく)。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-320">Narrowband Conversational MOS of the audio sessions (based on both audio streams).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-321">AppliedBandwidthLimit</span><span class="sxs-lookup"><span data-stu-id="8b0fb-321">AppliedBandwidthLimit</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-322">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-322">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-323">さまざまなポリシー設定 (TURN、API、SDP、ポリシーサーバーなど) が指定された send side ストリームに適用される実際の帯域幅。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-323">Actual bandwidth applied to the given send side stream given various policy settings (TURN, API, SDP, Policy Server, and so on).</span></span> <span data-ttu-id="8b0fb-324">これは、帯域幅の推定値に基づいて低帯域幅を使用できるため、有効帯域幅と混同しないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-324">This is not to be confused with the effective bandwidth because there can be a lower effective bandwidth based on the bandwidth estimate.</span></span> <span data-ttu-id="8b0fb-325">これは基本的に最大帯域幅であり、送信ストリームは、帯域幅の推定によって課された制限を受けることができません。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-325">This is basically the maximum bandwidth the send stream can take barring limits imposed by the bandwidth estimate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-326">JitterInterArrival</span><span class="sxs-lookup"><span data-stu-id="8b0fb-326">JitterInterArrival</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-327">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-327">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-328">リアルタイム制御プロトコル (RTCP) の統計情報からの平均ネットワークジッター。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-328">Average network jitter from Real Time Control Protocol (RTCP) statistics.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-329">JitterInterArrivalMax</span><span class="sxs-lookup"><span data-stu-id="8b0fb-329">JitterInterArrivalMax</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-330">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-330">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-331">通話中の最大ネットワークジッター。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-331">Maximum network jitter during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-332">PacketLossRate</span><span class="sxs-lookup"><span data-stu-id="8b0fb-332">PacketLossRate</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-333">10進数 (5, 4)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-333">decimal(5,4)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-334">通話中の平均パケット損失率。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-334">Average packet loss rate during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-335">PacketLossRateMax</span><span class="sxs-lookup"><span data-stu-id="8b0fb-335">PacketLossRateMax</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-336">10進数 (5, 4)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-336">decimal(5,4)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-337">通話中に発生したパケット損失の上限。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-337">Maximum packet loss observed during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-338">BurstDensity</span><span class="sxs-lookup"><span data-stu-id="8b0fb-338">BurstDensity</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-339">10進数 (9, 4)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-339">decimal(9,4)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-340">通話中に損失が発生した場合のパケット損失の平均密度。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-340">Average density of packet loss during bursts of losses during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-341">BurstDuration</span><span class="sxs-lookup"><span data-stu-id="8b0fb-341">BurstDuration</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-342">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-342">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-343">通話中に損失が発生したときのパケット損失の平均時間。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-343">Average duration of packet loss during bursts of losses during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-344">BurstGapDensity</span><span class="sxs-lookup"><span data-stu-id="8b0fb-344">BurstGapDensity</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-345">10進数 (9, 4)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-345">decimal(9,4)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-346">パケット損失のバースト間のパケット損失の平均密度。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-346">Average density of packet loss during gaps between bursts of packet loss.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-347">BurstGapDuration</span><span class="sxs-lookup"><span data-stu-id="8b0fb-347">BurstGapDuration</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-348">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-348">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-349">パケット損失のバーストの間の平均時間差。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-349">Average duration of gaps between bursts of packet loss.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-350">PacketUtilization</span><span class="sxs-lookup"><span data-stu-id="8b0fb-350">PacketUtilization</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-351">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-351">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-352">オーディオストリームのパケット数。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-352">Packet count for the audio stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-353">BandwidthEst</span><span class="sxs-lookup"><span data-stu-id="8b0fb-353">BandwidthEst</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-354">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-354">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-355">オーディオストリームの帯域幅の推定。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-355">Bandwidth estimates for the audio stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-356">DegradationAvg</span><span class="sxs-lookup"><span data-stu-id="8b0fb-356">DegradationAvg</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-357">10進数 (3, 2)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-357">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-358">電話全体のネットワーク MOS が低下します。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-358">Network MOS Degradation for the whole call.</span></span> <span data-ttu-id="8b0fb-359">範囲は 0.0 ~ 5.0 です。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-359">Range is 0.0 to 5.0.</span></span> <span data-ttu-id="8b0fb-360">このメトリックは、ジッタとパケット損失によってネットワーク MOS が削減された量を示します。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-360">This metric shows the amount the Network MOS was reduced because of jitter and packet loss.</span></span> <span data-ttu-id="8b0fb-361">許容可能な品質には、0.5 未満の値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-361">For acceptable quality it should less than 0.5.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-362">DegradationMax</span><span class="sxs-lookup"><span data-stu-id="8b0fb-362">DegradationMax</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-363">10進数 (3, 2)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-363">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-364">通話中の最大ネットワーク MOS の品質低下。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-364">Maximum Network MOS degradation during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-365">DegradationJitterAvg</span><span class="sxs-lookup"><span data-stu-id="8b0fb-365">DegradationJitterAvg</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-366">10進数 (3, 2)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-366">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-367">ジッターによるネットワーク MOS の低下。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-367">Network MOS degradation caused by jitter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-368">DegradationPacketLossAvg</span><span class="sxs-lookup"><span data-stu-id="8b0fb-368">DegradationPacketLossAvg</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-369">10進数 (3, 2)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-369">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-370">パケット損失によるネットワーク MOS の低下。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-370">Network MOS degradation caused by packet loss.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-371">PayloadDescription</span><span class="sxs-lookup"><span data-stu-id="8b0fb-371">PayloadDescription</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-372">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-372">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-373">通話に使用するオーディオコーデック。 <a href="lync-server-2013-payloaddescription-table.md">Lync Server 2013 の PayloadDescription テーブル</a>から参照されています。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-373">The audio codec used for the call, referenced from the <a href="lync-server-2013-payloaddescription-table.md">PayloadDescription table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-374">AudioSampleRate</span><span class="sxs-lookup"><span data-stu-id="8b0fb-374">AudioSampleRate</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-375">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-375">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-376">オーディオストリームのサンプリングレート。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-376">Sampling rate for the audio stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-377">CallerSendSignalLevel</span><span class="sxs-lookup"><span data-stu-id="8b0fb-377">CallerSendSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-378">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-378">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-379">発信者が送信したオーディオのアナログゲインの制御オーディオ信号レベル。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-379">Post-Analog Gain Control audio signal level for the audio the caller sent.</span></span> <span data-ttu-id="8b0fb-380">このメトリックの単位は dBmo です。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-380">The unit for this metric is dBmo.</span></span> <span data-ttu-id="8b0fb-381">許容可能な品質を求めるには、少なくとも30個の dBmo を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-381">For acceptable quality, it should be at least 30 dBmo.</span></span> <span data-ttu-id="8b0fb-382">このメトリックは、A/V 会議サーバーまたは IP 携帯電話によって報告されることはありません。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-382">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-383">CallerRecvSignalLevel</span><span class="sxs-lookup"><span data-stu-id="8b0fb-383">CallerRecvSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-384">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-384">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-385">発信者が受信した音声の音声信号レベル。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-385">Audio signal level for the audio the caller received.</span></span> <span data-ttu-id="8b0fb-386">このメトリックの単位は dBmo です。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-386">The unit for this metric is dBmo.</span></span> <span data-ttu-id="8b0fb-387">許容可能な品質を求めるには、少なくとも30個の dBmo を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-387">For acceptable quality, it should be at least 30 dBmo.</span></span> <span data-ttu-id="8b0fb-388">このメトリックは、A/V 会議サーバーまたは IP 携帯電話によって報告されることはありません。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-388">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-389">CallerSendNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="8b0fb-389">CallerSendNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-390">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-390">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-391">発信者が送信したオーディオのアナログゲインのオーディオノイズレベルを制御します。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-391">Post-Analog Gain Control audio noise level for the audio the caller sent.</span></span> <span data-ttu-id="8b0fb-392">このメトリックの単位は dBmo です。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-392">The unit for this metric is dBmo.</span></span> <span data-ttu-id="8b0fb-393">許容される品質には、35 dBmo よりも小さい値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-393">For acceptable quality, it should be less than 35 dBmo.</span></span> <span data-ttu-id="8b0fb-394">このメトリックは、A/V 会議サーバーまたは IP 携帯電話によって報告されることはありません。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-394">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-395">CallerRecvNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="8b0fb-395">CallerRecvNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-396">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-396">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-397">送信者が受信したオーディオのアナログゲインのオーディオノイズレベルを制御します。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-397">Post-Analog Gain Control audio noise level for the audio the caller received.</span></span> <span data-ttu-id="8b0fb-398">このメトリックの単位は dBmo です。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-398">The unit for this metric is dBmo.</span></span> <span data-ttu-id="8b0fb-399">許容される品質には、35 dBmo よりも小さい値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-399">For acceptable quality, it should be less than 35 dBmo.</span></span> <span data-ttu-id="8b0fb-400">このメトリックは、A/V 会議サーバーまたは IP 携帯電話によって報告されることはありません。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-400">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-401">CallerEchoReturn</span><span class="sxs-lookup"><span data-stu-id="8b0fb-401">CallerEchoReturn</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-402">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-402">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-403">発信者に対する戻り値の損失の強調機能。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-403">Echo Return Loss Enhancement for the caller.</span></span> <span data-ttu-id="8b0fb-404">このメトリックの単位は dB です。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-404">The unit for this metric is dB.</span></span> <span data-ttu-id="8b0fb-405">小さい値は、エコーが少なくなります。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-405">Lower values represent less echo.</span></span> <span data-ttu-id="8b0fb-406">このメトリックは、A/V 会議サーバーまたは IP 携帯電話によって報告されることはありません。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-406">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-407">CallerSpeakerGlitchRate</span><span class="sxs-lookup"><span data-stu-id="8b0fb-407">CallerSpeakerGlitchRate</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-408">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-408">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-409">発信者のスピーカーレンダリングに対する5分あたりの平均エラー。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-409">Average glitches per five minutes for the caller’s loudspeaker rendering.</span></span> <span data-ttu-id="8b0fb-410">品質を向上させるには、5分未満でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-410">For good quality, this should be less than one per five minutes.</span></span> <span data-ttu-id="8b0fb-411">A/V 会議サーバー、仲介サーバー、または IP 電話によって報告されていません。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-411">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-412">CallerMicGlitchRate</span><span class="sxs-lookup"><span data-stu-id="8b0fb-412">CallerMicGlitchRate</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-413">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-413">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-414">発信者のマイクのキャプチャに対する5分あたりの平均エラー。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-414">Average glitches per five minutes for the caller’s microphone capture.</span></span> <span data-ttu-id="8b0fb-415">品質を向上させるには、5分未満の値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-415">For good quality this should be less than one per five minutes.</span></span> <span data-ttu-id="8b0fb-416">A/V 会議サーバー、仲介サーバー、または IP 電話によって報告されていません。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-416">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-417">CallerTimestampDriftRateMic</span><span class="sxs-lookup"><span data-stu-id="8b0fb-417">CallerTimestampDriftRateMic</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-418">10進数 (9, 2)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-418">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-419">発信者のマイクデバイスクロックドリフトレート。 CPU クロックを基準としています。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-419">Caller’s microphone device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-420">CallerTimestampDriftRateSpk</span><span class="sxs-lookup"><span data-stu-id="8b0fb-420">CallerTimestampDriftRateSpk</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-421">10進数 (9, 2)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-421">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-422">発信者のスピーカーデバイスクロックドリフトレート。 CPU クロックを基準としています。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-422">Caller’s speaker device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-423">CallerTimestampErrorMicMs</span><span class="sxs-lookup"><span data-stu-id="8b0fb-423">CallerTimestampErrorMicMs</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-424">10進数 (9, 2)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-424">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-425">平均マイクキャプチャストリームタイムスタンプエラー (ミリ秒単位)、通話の最後の20秒。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-425">Average microphone capture stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-426">CallerTimestampErrorSpkMs</span><span class="sxs-lookup"><span data-stu-id="8b0fb-426">CallerTimestampErrorSpkMs</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-427">10進数 (9, 2)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-427">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-428">発信者のスピーカーレンダーストリームのタイムスタンプエラーの平均値 (ミリ秒) です。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-428">Average of the caller’s speaker render stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-429">CallerVsEntryCauses 原因</span><span class="sxs-lookup"><span data-stu-id="8b0fb-429">CallerVsEntryCauses</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-430">smallint</span><span class="sxs-lookup"><span data-stu-id="8b0fb-430">smallint</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-431">音声スイッチは半二重モードで、中断機能が低減されます。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-431">Voice switch is a half-duplex mode with reduced interruption ability.</span></span> <span data-ttu-id="8b0fb-432">詳細については、「 <a href="lync-server-2013-medialine-table.md">Lync Server 2013 の MediaLine テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-432">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-433">CallerEchoEventCauses</span><span class="sxs-lookup"><span data-stu-id="8b0fb-433">CallerEchoEventCauses</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-434">tinyint</span><span class="sxs-lookup"><span data-stu-id="8b0fb-434">tinyint</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-435">呼び出し元のエコーイベントの原因。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-435">Causes of an echo event for the caller.</span></span> <span data-ttu-id="8b0fb-436">詳細については、「 <a href="lync-server-2013-medialine-table.md">Lync Server 2013 の MediaLine テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-436">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-437">CallerEchoPercentMicIn</span><span class="sxs-lookup"><span data-stu-id="8b0fb-437">CallerEchoPercentMicIn</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-438">10進数 (5, 2)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-438">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-439">呼び出し元のマイクキャプチャストリームでエコーが検出された時間のパーセンテージ。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-439">Percentage of time when echo is detected in the caller’s microphone capture stream.</span></span> <span data-ttu-id="8b0fb-440">ヘッドセットを使用する場合は、値を低くする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-440">If headset is used, the value should be low.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-441">CallerEchoPercentSend</span><span class="sxs-lookup"><span data-stu-id="8b0fb-441">CallerEchoPercentSend</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-442">10進数 (5, 2)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-442">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-443">呼び出し元の送信ストリームでエコーが検出された時間のパーセンテージ。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-443">Percentage of time when echo is detected in the caller’s sent stream.</span></span> <span data-ttu-id="8b0fb-444">送信ストリームでのエコー率が高いと、エコーが発生したことを示します。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-444">High echo percentage in send streams an indication of echo leak.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-445">CallerRxAGCSignalLevel</span><span class="sxs-lookup"><span data-stu-id="8b0fb-445">CallerRxAGCSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-446">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-446">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-447">発信者のオーディオのためのゲートウェイからの仲介サーバー上のシグナルレベルを受信しました。これは、仲介サーバーにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-447">Received signal level on the Mediation Server from the Gateway for the caller’s audio; this applies only to the Mediation Server.</span></span> <span data-ttu-id="8b0fb-448">このメトリックの単位は dBoV です。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-448">The unit of this metric is dBoV.</span></span> <span data-ttu-id="8b0fb-449">品質を向上させるには、許容範囲は-30 ~-18 dBoV にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-449">For good quality, the acceptable range should be -30 to -18 dBoV.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-450">CallerRxAGCNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="8b0fb-450">CallerRxAGCNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-451">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-451">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-452">発信者のオーディオのためのゲートウェイからの仲介サーバー上のシグナルレベルを受信しました。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-452">Received signal level on the Mediation Server from the Gateway for the caller’s audio.</span></span> <span data-ttu-id="8b0fb-453">これは、仲介サーバーにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-453">This applies only to the Mediation Server.</span></span> <span data-ttu-id="8b0fb-454">このメトリックの単位は dBoV です。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-454">The unit of this metric is dBoV.</span></span> <span data-ttu-id="8b0fb-455">品質を向上させるには、許容範囲として 50 dBoV 未満の値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-455">For good quality, the acceptable range should be less than -50 dBoV.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-456">CallerRxAGCGain</span><span class="sxs-lookup"><span data-stu-id="8b0fb-456">CallerRxAGCGain</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-457">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-457">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-458">発信者の音声に適用された仲介サーバー側の自動ゲイン制御 (AGC)。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-458">Automatic gain control (AGC) on the Mediation Server side applied to the caller’s audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-459">CallerInitialSignalLevelRMS</span><span class="sxs-lookup"><span data-stu-id="8b0fb-459">CallerInitialSignalLevelRMS</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-460">float</span><span class="sxs-lookup"><span data-stu-id="8b0fb-460">float</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-461">通話の最初の30秒間の着信シグナルの発信者への着信シグナルの平方根 (RMS)。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-461">Root mean square (RMS) of the incoming signal to the caller for up to the first 30 seconds of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-462">CalleeSendSignalLevel</span><span class="sxs-lookup"><span data-stu-id="8b0fb-462">CalleeSendSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-463">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-463">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-464">呼び出し元が送信したオーディオのアナログゲインコントロールオーディオ信号レベルを表します。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-464">Represents the Post-Analog Gain Control audio signal level for the audio the callee sent.</span></span> <span data-ttu-id="8b0fb-465">このメトリックの単位は dBmo です。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-465">The unit for this metric is dBmo.</span></span> <span data-ttu-id="8b0fb-466">許容可能な品質を求めるには、少なくとも30個の dBmo を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-466">For acceptable quality, it should be at least 30 dBmo.</span></span> <span data-ttu-id="8b0fb-467">このメトリックは、A/V 会議サーバーまたは IP 携帯電話によって報告されることはありません。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-467">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-468">CalleeRecvSignalLevel</span><span class="sxs-lookup"><span data-stu-id="8b0fb-468">CalleeRecvSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-469">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-469">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-470">呼び出し側が受信したオーディオの音声信号レベル。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-470">Audio signal level for the audio the callee received.</span></span> <span data-ttu-id="8b0fb-471">このメトリックの単位は dBmo です。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-471">The unit for this metric is dBmo.</span></span> <span data-ttu-id="8b0fb-472">許容可能な品質を求めるには、少なくとも30個の dBmo を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-472">For acceptable quality, it should be at least 30 dBmo.</span></span> <span data-ttu-id="8b0fb-473">このメトリックは、A/V 会議サーバーまたは IP 携帯電話によって報告されることはありません。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-473">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-474">CalleeSendNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="8b0fb-474">CalleeSendNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-475">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-475">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-476">以降のアナログゲインは、呼び出し元が送信したオーディオに対してオーディオノイズレベルを制御します。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-476">Post-Analog Gain Control audio noise level for the audio the callee sent.</span></span> <span data-ttu-id="8b0fb-477">このメトリックの単位は dBmo です。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-477">The unit for this metric is dBmo.</span></span> <span data-ttu-id="8b0fb-478">許容される品質には、35 dBmo よりも小さい値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-478">For acceptable quality, it should be less than 35 dBmo.</span></span> <span data-ttu-id="8b0fb-479">このメトリックは、A/V 会議サーバーまたは IP 携帯電話によって報告されることはありません。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-479">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-480">CalleeRecvNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="8b0fb-480">CalleeRecvNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-481">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-481">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-482">後からのアナログゲインコントロール呼び出し側が受信したオーディオのオーディオノイズレベルを制御します。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-482">Post-Analog Gain Control audio noise level for the audio the callee received.</span></span> <span data-ttu-id="8b0fb-483">このメトリックの単位は dBmo です。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-483">The unit for this metric is dBmo.</span></span> <span data-ttu-id="8b0fb-484">許容される品質には、35 dBmo よりも小さい値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-484">For acceptable quality, it should be less than 35 dBmo.</span></span> <span data-ttu-id="8b0fb-485">このメトリックは、A/V 会議サーバーまたは IP 携帯電話によって報告されることはありません。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-485">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-486">CalleeEchoReturn</span><span class="sxs-lookup"><span data-stu-id="8b0fb-486">CalleeEchoReturn</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-487">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-487">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-488">呼び出し先のエコーリターンロスの強化。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-488">Echo Return Loss Enhancement for the callee.</span></span> <span data-ttu-id="8b0fb-489">このメトリックの単位は dB です。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-489">The unit for this metric is dB.</span></span> <span data-ttu-id="8b0fb-490">小さい値は、エコーが少なくなります。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-490">Lower values represent less echo.</span></span> <span data-ttu-id="8b0fb-491">このメトリックは、A/V 会議サーバーまたは IP 携帯電話によって報告されることはありません。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-491">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-492">CalleeSpeakerGlitchRate</span><span class="sxs-lookup"><span data-stu-id="8b0fb-492">CalleeSpeakerGlitchRate</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-493">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-493">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-494">呼び出し先のスピーカーレンダリングに対する5分あたりの平均エラー。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-494">Average glitches per five minutes for the callee’s loudspeaker rendering.</span></span> <span data-ttu-id="8b0fb-495">品質を向上させるには、5分未満でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-495">For good quality, this should be less than one per five minutes.</span></span> <span data-ttu-id="8b0fb-496">A/V 会議サーバー、仲介サーバー、または IP 電話によって報告されていません。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-496">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-497">CalleeMicGlitchRate</span><span class="sxs-lookup"><span data-stu-id="8b0fb-497">CalleeMicGlitchRate</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-498">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-498">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-499">呼び出し先のマイクのキャプチャに対する5分あたりの平均エラー。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-499">Average glitches per five minutes for the callee’s microphone capture.</span></span> <span data-ttu-id="8b0fb-500">品質を向上させるには、5分未満の値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-500">For good quality this should be less than one per five minutes.</span></span> <span data-ttu-id="8b0fb-501">A/V 会議サーバー、仲介サーバー、または IP 電話によって報告されていません。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-501">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-502">CalleeTimestampDriftRateMic</span><span class="sxs-lookup"><span data-stu-id="8b0fb-502">CalleeTimestampDriftRateMic</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-503">10進数 (9, 2)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-503">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-504">呼び出し先のマイクデバイスクロックドリフトレート。 CPU クロックを基準としています。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-504">Callee’s microphone device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-505">CalleeTimestampDriftRateSpk</span><span class="sxs-lookup"><span data-stu-id="8b0fb-505">CalleeTimestampDriftRateSpk</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-506">10進数 (9, 2)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-506">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-507">呼び出し先のスピーカーデバイスクロックドリフト率。 CPU クロックを基準としています。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-507">Callee’s speaker device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-508">CalleeTimestampErrorMicMs</span><span class="sxs-lookup"><span data-stu-id="8b0fb-508">CalleeTimestampErrorMicMs</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-509">10進数 (9, 2)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-509">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-510">平均マイクキャプチャストリームタイムスタンプエラー (ミリ秒単位)、通話の最後の20秒。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-510">Average microphone capture stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-511">CalleeTimestampErrorSpkMs</span><span class="sxs-lookup"><span data-stu-id="8b0fb-511">CalleeTimestampErrorSpkMs</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-512">10進数 (9, 2)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-512">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-513">呼び出し側のスピーカーレンダーストリームのタイムスタンプエラーの平均 (ミリ秒) です。これは、通話の最後の20秒を示しています。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-513">Average of the callee’s speaker render stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-514">Calleevsenの原因</span><span class="sxs-lookup"><span data-stu-id="8b0fb-514">CalleeVsEntryCauses</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-515">smallint</span><span class="sxs-lookup"><span data-stu-id="8b0fb-515">smallint</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-516">音声スイッチは半二重モードで、中断機能が低減されます。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-516">Voice switch is a half-duplex mode with reduced interruption ability.</span></span> <span data-ttu-id="8b0fb-517">詳細については、「 <a href="lync-server-2013-medialine-table.md">Lync Server 2013 の MediaLine テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-517">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-518">CalleeEchoEventCauses</span><span class="sxs-lookup"><span data-stu-id="8b0fb-518">CalleeEchoEventCauses</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-519">tinyint</span><span class="sxs-lookup"><span data-stu-id="8b0fb-519">tinyint</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-520">呼び出し先のエコーイベントの原因。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-520">Causes of an echo event for the callee.</span></span> <span data-ttu-id="8b0fb-521">詳細については、「 <a href="lync-server-2013-medialine-table.md">Lync Server 2013 の MediaLine テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-521">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-522">CalleeEchoPercentMicIn</span><span class="sxs-lookup"><span data-stu-id="8b0fb-522">CalleeEchoPercentMicIn</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-523">10進数 (5, 2)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-523">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-524">呼び出し先のマイクキャプチャストリームでエコーが検出された時間のパーセンテージ。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-524">Percentage of time when echo is detected in the callee’s microphone capture stream.</span></span> <span data-ttu-id="8b0fb-525">ヘッドセットを使用する場合は、値を低くする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-525">If headset is used, the value should be low.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-526">CalleeEchoPercentSend</span><span class="sxs-lookup"><span data-stu-id="8b0fb-526">CalleeEchoPercentSend</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-527">10進数 (5, 2)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-527">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-528">呼び出し元の送信ストリームでエコーが検出された時間のパーセンテージ。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-528">Percentage of time when echo is detected in the callee’s sent stream.</span></span> <span data-ttu-id="8b0fb-529">送信ストリームでのエコー率が高いと、エコーが発生したことを示します。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-529">High echo percentage in send streams an indication of echo leak.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-530">CalleeRxAGCSignalLevel</span><span class="sxs-lookup"><span data-stu-id="8b0fb-530">CalleeRxAGCSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-531">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-531">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-532">呼び出し元のオーディオのゲートウェイからの、仲介サーバー上の受信したシグナルレベル。これは、仲介サーバーにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-532">Received signal level on the Mediation Server from the Gateway for the callee’s audio; this applies only to the Mediation Server.</span></span> <span data-ttu-id="8b0fb-533">このメトリックの単位は dBoV です。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-533">The unit of this metric is dBoV.</span></span> <span data-ttu-id="8b0fb-534">品質を向上させるには、許容範囲は [-30 ~-18] の dBoV にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-534">For good quality, the acceptable range should be [-30 to -18] dBoV.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-535">CalleeRxAGCNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="8b0fb-535">CalleeRxAGCNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-536">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-536">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-537">呼び出し元のオーディオのゲートウェイからの、仲介サーバー上の受信したシグナルレベル。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-537">Received signal level on the Mediation Server from the Gateway for the callee’s audio.</span></span> <span data-ttu-id="8b0fb-538">これは、仲介サーバーにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-538">This applies only to the Mediation Server.</span></span> <span data-ttu-id="8b0fb-539">このメトリックの単位は dBoV です。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-539">The unit of this metric is dBoV.</span></span> <span data-ttu-id="8b0fb-540">品質を向上させるには、許容範囲として 50 dBoV 未満の値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-540">For good quality, the acceptable range should be less than -50 dBoV.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-541">お金の獲得</span><span class="sxs-lookup"><span data-stu-id="8b0fb-541">CalleeRxAGCGain</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-542">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-542">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-543">呼び出し先のオーディオに適用された仲介サーバー側の自動ゲイン制御 (AGC)。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-543">Automatic gain control (AGC) on the Mediation Server side applied to the callee’s audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-544">CalleeInitialSignalLevelRMS</span><span class="sxs-lookup"><span data-stu-id="8b0fb-544">CalleeInitialSignalLevelRMS</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-545">float</span><span class="sxs-lookup"><span data-stu-id="8b0fb-545">float</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-546">呼び出しの最初の30秒間の呼び出し先への着信シグナルのルート平均平方根 (RMS)。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-546">Root mean square (RMS) of the incoming signal to the callee for up to the first 30 seconds of the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-547">RatioConcealedSamplesAvg</span><span class="sxs-lookup"><span data-stu-id="8b0fb-547">RatioConcealedSamplesAvg</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-548">10進数 (5, 2)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-548">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-549">オーディオの修復によって発生した、一般的なサンプルの平均比率。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-549">Average ratio of concealed samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-550">RatioStretchedSamplesAvg</span><span class="sxs-lookup"><span data-stu-id="8b0fb-550">RatioStretchedSamplesAvg</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-551">10進数 (5, 2)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-551">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-552">オーディオ修復によって生成された、一般的なサンプルの平均比率。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-552">Average ratio of stretched samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-553">RatioCompressedSamplesAvg</span><span class="sxs-lookup"><span data-stu-id="8b0fb-553">RatioCompressedSamplesAvg</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-554">10進数 (5, 2)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-554">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-555">オーディオの修復によって生成された、一般的なサンプルの圧縮サンプルの平均比率。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-555">Average ratio of compressed samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-556">RoundTrip</span><span class="sxs-lookup"><span data-stu-id="8b0fb-556">RoundTrip</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-557">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-557">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-558">RTCP の統計情報からのラウンドトリップ時間。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-558">Round trip time from RTCP statistics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-559">RoundTripMax</span><span class="sxs-lookup"><span data-stu-id="8b0fb-559">RoundTripMax</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-560">int</span><span class="sxs-lookup"><span data-stu-id="8b0fb-560">int</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-561">オーディオストリームの最大ラウンドトリップ時間。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-561">Maximum round trip time for the audio stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-562">OverallAvgNetworkMOS</span><span class="sxs-lookup"><span data-stu-id="8b0fb-562">OverallAvgNetworkMOS</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-563">10進数 (3, 2)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-563">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-564">通話の平均広帯域ネットワーク MOS。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-564">Average wideband Network MOS for the call.</span></span> <span data-ttu-id="8b0fb-565">このメトリックは、使用されているパケット損失、ジッタ、およびコーデックによって異なります。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-565">This metric depends on the packet loss, jitter, and codec used.</span></span> <span data-ttu-id="8b0fb-566">範囲は 1.0 ~ 5.0 です。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-566">Range is 1.0 to 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-567">OverallMinNetworkMOS</span><span class="sxs-lookup"><span data-stu-id="8b0fb-567">OverallMinNetworkMOS</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-568">10進数 (3, 2)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-568">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-569">通話の最小広帯域ネットワーク MOS。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-569">Minimum wideband Network MOS for the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-570">SendListenMOS</span><span class="sxs-lookup"><span data-stu-id="8b0fb-570">SendListenMOS</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-571">10進数 (3, 2)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-571">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-572">平均予測広帯域は、音声のレベル、ノイズレベル、キャプチャデバイスの特性など、送信された音声の MOS スコアを聞き取ります。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-572">Average predicted wideband Listening MOS score for audio sent, including speech level, noise level and capture device characteristics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-573">SendListenMOSMin</span><span class="sxs-lookup"><span data-stu-id="8b0fb-573">SendListenMOSMin</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-574">10進数 (3, 2)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-574">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-575">通話の最小 SendListenMOS。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-575">Minimum SendListenMOS for the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-576">RecvListenMOS</span><span class="sxs-lookup"><span data-stu-id="8b0fb-576">RecvListenMOS</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-577">10進数 (3, 2)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-577">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-578">予測される平均広帯域は、ネットワークから受信した音声 (音声のレベル、ノイズレベル、コーデック、ネットワーク条件、キャプチャデバイスの特性など) を対象としています。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-578">Average predicted wideband Listening MOS score for audio received from the network including speech level, noise level, codec, network conditions and capture device characteristics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-579">RecvListenMOSMin</span><span class="sxs-lookup"><span data-stu-id="8b0fb-579">RecvListenMOSMin</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-580">10進数 (3, 2)</span><span class="sxs-lookup"><span data-stu-id="8b0fb-580">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-581">通話の最小 RecvListenMOS。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-581">Minimum RecvListenMOS for the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0fb-582">AudioFECUsed</span><span class="sxs-lookup"><span data-stu-id="8b0fb-582">AudioFECUsed</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-583">bit</span><span class="sxs-lookup"><span data-stu-id="8b0fb-583">bit</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-584">通話にオーディオ FEC が使用されたかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-584">Indicates whether audio FEC was used for the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0fb-585">SenderIsCallerPAI</span><span class="sxs-lookup"><span data-stu-id="8b0fb-585">SenderIsCallerPAI</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-586">bit</span><span class="sxs-lookup"><span data-stu-id="8b0fb-586">bit</span></span></p></td>
<td><p><span data-ttu-id="8b0fb-587">P がアサートされた情報の方向を示します。1は、ストリームの方向を呼び出し元から呼び出し先に転送することを意味します。0は、ストリームの方向を呼び出し元から呼び出し元に転送します。</span><span class="sxs-lookup"><span data-stu-id="8b0fb-587">Indicates direction of the p-asserted identify information; 1 means the stream direction is from the caller to the callee; 0 means the stream direction is from the callee to the caller.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="8b0fb-588">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8b0fb-588">


</div>

<span> </span>

</div>

</div>

</span></span></div>

