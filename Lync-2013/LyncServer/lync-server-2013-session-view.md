---
title: 'Lync Server 2013: セッションビュー'
description: 'Lync Server 2013: セッションビュー。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Session view
ms:assetid: 49e33f5b-45d0-4146-a5a4-76954d895a98
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688048(v=OCS.15)
ms:contentKeyID: 49733641
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ff4bc4abbd55e073006693d28f092f077698ef75
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444792"
---
# <a name="session-view-in-lync-server-2013"></a><span data-ttu-id="f285b-103">Lync Server 2013 のセッションビュー</span><span class="sxs-lookup"><span data-stu-id="f285b-103">Session view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f285b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f285b-104">

<span> </span></span></span>

<span data-ttu-id="f285b-105">_**最終更新日:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="f285b-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="f285b-106">セッションビューには、データベース内にレコードがあるセッションに関する情報が格納されます。</span><span class="sxs-lookup"><span data-stu-id="f285b-106">The Session View stores information about sessions that have records in the database.</span></span> <span data-ttu-id="f285b-107">このビューは、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="f285b-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f285b-108">列</span><span class="sxs-lookup"><span data-stu-id="f285b-108">Column</span></span></th>
<th><span data-ttu-id="f285b-109">データ型</span><span class="sxs-lookup"><span data-stu-id="f285b-109">Data Type</span></span></th>
<th><span data-ttu-id="f285b-110">詳細</span><span class="sxs-lookup"><span data-stu-id="f285b-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f285b-111">ConferenceDateTime</span><span class="sxs-lookup"><span data-stu-id="f285b-111">ConferenceDateTime</span></span></p></td>
<td><p><span data-ttu-id="f285b-112">datetime</span><span class="sxs-lookup"><span data-stu-id="f285b-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="f285b-113">MediaLine テーブルから参照されます。</span><span class="sxs-lookup"><span data-stu-id="f285b-113">Referenced from the MediaLine Table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f285b-114">ConferenceURI</span><span class="sxs-lookup"><span data-stu-id="f285b-114">ConferenceURI</span></span></p></td>
<td><p><span data-ttu-id="f285b-115">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="f285b-115">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="f285b-116">会議の URI (会議の場合) または [この Id がピアツーピアセッションの場合] です。</span><span class="sxs-lookup"><span data-stu-id="f285b-116">Conference URI if this is a conference, or DialogID if this is a peer-to-peer session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f285b-117">関連性</span><span class="sxs-lookup"><span data-stu-id="f285b-117">Correlation</span></span></p></td>
<td><p><span data-ttu-id="f285b-118">varchar (max)</span><span class="sxs-lookup"><span data-stu-id="f285b-118">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="f285b-119">セッションの関連付け ID。</span><span class="sxs-lookup"><span data-stu-id="f285b-119">Correlation ID of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f285b-120">このカテゴリ</span><span class="sxs-lookup"><span data-stu-id="f285b-120">DialogCategory</span></span></p></td>
<td><p><span data-ttu-id="f285b-121">bit</span><span class="sxs-lookup"><span data-stu-id="f285b-121">bit</span></span></p></td>
<td><p><span data-ttu-id="f285b-122">ダイアログカテゴリ0は Lync Server、仲介サーバーの区間、1は、PSTN ゲートウェイ区間への仲介サーバーです。</span><span class="sxs-lookup"><span data-stu-id="f285b-122">Dialog category; 0 is Lync Server to Mediation Server leg; 1 is Mediation Server to PSTN gateway leg.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f285b-123">MediationServerBypassFlag</span><span class="sxs-lookup"><span data-stu-id="f285b-123">MediationServerBypassFlag</span></span></p></td>
<td><p><span data-ttu-id="f285b-124">bit</span><span class="sxs-lookup"><span data-stu-id="f285b-124">bit</span></span></p></td>
<td><p><span data-ttu-id="f285b-125">通話がバイパスされたかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="f285b-125">Indicates whether or not the call was bypassed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f285b-126">Mediabypasswarnings フラグ</span><span class="sxs-lookup"><span data-stu-id="f285b-126">MediaBypassWarningFlag</span></span></p></td>
<td><p><span data-ttu-id="f285b-127">int</span><span class="sxs-lookup"><span data-stu-id="f285b-127">int</span></span></p></td>
<td><p><span data-ttu-id="f285b-128">このフィールドは、バイパス Id が一致した場合でも、着信がバイパスされなかった理由を示します (存在する場合)。</span><span class="sxs-lookup"><span data-stu-id="f285b-128">This field, if present, indicates why a call was not bypassed even if the bypass IDs matched.</span></span> <span data-ttu-id="f285b-129">Lync Server の場合は、1つの値のみが定義されます。</span><span class="sxs-lookup"><span data-stu-id="f285b-129">For Lync Server, only one value is defined:</span></span></p>
<p><span data-ttu-id="f285b-130">0x0001 –既定のネットワークアダプターの不明なバイパス ID</span><span class="sxs-lookup"><span data-stu-id="f285b-130">0x0001 – Unknown bypass ID for Default network adapter</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f285b-131">StartTime</span><span class="sxs-lookup"><span data-stu-id="f285b-131">StartTime</span></span></p></td>
<td><p><span data-ttu-id="f285b-132">datetime</span><span class="sxs-lookup"><span data-stu-id="f285b-132">datetime</span></span></p></td>
<td><p><span data-ttu-id="f285b-133">通話開始時刻。</span><span class="sxs-lookup"><span data-stu-id="f285b-133">Call start time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f285b-134">EndTime</span><span class="sxs-lookup"><span data-stu-id="f285b-134">EndTime</span></span></p></td>
<td><p><span data-ttu-id="f285b-135">datetime</span><span class="sxs-lookup"><span data-stu-id="f285b-135">datetime</span></span></p></td>
<td><p><span data-ttu-id="f285b-136">通話終了時刻。</span><span class="sxs-lookup"><span data-stu-id="f285b-136">Call end time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f285b-137">CallerPool</span><span class="sxs-lookup"><span data-stu-id="f285b-137">CallerPool</span></span></p></td>
<td><p><span data-ttu-id="f285b-138">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="f285b-138">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="f285b-139">発信者番号プールの FQDN。</span><span class="sxs-lookup"><span data-stu-id="f285b-139">Caller pool FQDN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f285b-140">CalleePool</span><span class="sxs-lookup"><span data-stu-id="f285b-140">CalleePool</span></span></p></td>
<td><p><span data-ttu-id="f285b-141">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="f285b-141">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="f285b-142">呼び出し元プールの FQDN。</span><span class="sxs-lookup"><span data-stu-id="f285b-142">Callee pool FQDN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f285b-143">CallerPAI</span><span class="sxs-lookup"><span data-stu-id="f285b-143">CallerPAI</span></span></p></td>
<td><p><span data-ttu-id="f285b-144">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="f285b-144">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="f285b-145">呼び出し元の p がアサートされた id URI。</span><span class="sxs-lookup"><span data-stu-id="f285b-145">Caller’s p-asserted identity URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f285b-146">CalleePAI</span><span class="sxs-lookup"><span data-stu-id="f285b-146">CalleePAI</span></span></p></td>
<td><p><span data-ttu-id="f285b-147">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="f285b-147">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="f285b-148">呼び出し先の p-アサートされた id URI。</span><span class="sxs-lookup"><span data-stu-id="f285b-148">Callee’s p-asserted identity URI.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f285b-149">CallerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f285b-149">CallerEndpoint</span></span></p></td>
<td><p><span data-ttu-id="f285b-150">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="f285b-150">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="f285b-151">発信者のエンドポイント名。</span><span class="sxs-lookup"><span data-stu-id="f285b-151">Caller’s endpoint name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f285b-152">CalleeEndpoint</span><span class="sxs-lookup"><span data-stu-id="f285b-152">CalleeEndpoint</span></span></p></td>
<td><p><span data-ttu-id="f285b-153">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="f285b-153">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="f285b-154">発信者のエンドポイント名。</span><span class="sxs-lookup"><span data-stu-id="f285b-154">Caller’s endpoint name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f285b-155">CallerUserAgent</span><span class="sxs-lookup"><span data-stu-id="f285b-155">CallerUserAgent</span></span></p></td>
<td><p><span data-ttu-id="f285b-156">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="f285b-156">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="f285b-157">呼び出し元のユーザーエージェント文字列。</span><span class="sxs-lookup"><span data-stu-id="f285b-157">Caller’s user agent string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f285b-158">CallerUserAgentType</span><span class="sxs-lookup"><span data-stu-id="f285b-158">CallerUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="f285b-159">smallint</span><span class="sxs-lookup"><span data-stu-id="f285b-159">smallint</span></span></p></td>
<td><p><span data-ttu-id="f285b-160">呼び出し元のユーザーエージェントの種類。</span><span class="sxs-lookup"><span data-stu-id="f285b-160">Type of caller’s user agent.</span></span> <span data-ttu-id="f285b-161">詳細については、「 <a href="lync-server-2013-useragent-table.md">Lync Server 2013 の UserAgent テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f285b-161">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f285b-162">CallerUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="f285b-162">CallerUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="f285b-163">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="f285b-163">nvarchar (64)</span></span></p></td>
<td><p><span data-ttu-id="f285b-164">呼び出し元のユーザーエージェントのカテゴリ。</span><span class="sxs-lookup"><span data-stu-id="f285b-164">Category of caller’s user agent.</span></span> <span data-ttu-id="f285b-165">詳細については、「 <a href="lync-server-2013-useragentdef-table-qoe.md">Lync Server 2013 の Useragentdef テーブル (QoE)</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f285b-165">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f285b-166">CalleeUserAgent</span><span class="sxs-lookup"><span data-stu-id="f285b-166">CalleeUserAgent</span></span></p></td>
<td><p><span data-ttu-id="f285b-167">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="f285b-167">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="f285b-168">呼び出し先のユーザーエージェント文字列。</span><span class="sxs-lookup"><span data-stu-id="f285b-168">Callee’s user agent string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f285b-169">CalleeUserAgentType</span><span class="sxs-lookup"><span data-stu-id="f285b-169">CalleeUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="f285b-170">smallint</span><span class="sxs-lookup"><span data-stu-id="f285b-170">smallint</span></span></p></td>
<td><p><span data-ttu-id="f285b-171">呼び出し先のユーザーエージェントの種類。</span><span class="sxs-lookup"><span data-stu-id="f285b-171">Type of user agent for the callee.</span></span> <span data-ttu-id="f285b-172">詳細については、「 <a href="lync-server-2013-useragent-table.md">Lync Server 2013 の UserAgent テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f285b-172">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f285b-173">CalleeUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="f285b-173">CalleeUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="f285b-174">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="f285b-174">nvarchar (64)</span></span></p></td>
<td><p><span data-ttu-id="f285b-175">呼び出し先のユーザーエージェントカテゴリ。</span><span class="sxs-lookup"><span data-stu-id="f285b-175">User agent category for the callee.</span></span> <span data-ttu-id="f285b-176">詳細については、「 <a href="lync-server-2013-useragentdef-table-qoe.md">Lync Server 2013 の Useragentdef テーブル (QoE)</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f285b-176">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f285b-177">CallerURI</span><span class="sxs-lookup"><span data-stu-id="f285b-177">CallerURI</span></span></p></td>
<td><p><span data-ttu-id="f285b-178">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="f285b-178">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="f285b-179">発信者の URI。</span><span class="sxs-lookup"><span data-stu-id="f285b-179">Caller’s URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f285b-180">CalleeURI</span><span class="sxs-lookup"><span data-stu-id="f285b-180">CalleeURI</span></span></p></td>
<td><p><span data-ttu-id="f285b-181">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="f285b-181">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="f285b-182">呼び出し先の URI。</span><span class="sxs-lookup"><span data-stu-id="f285b-182">Callee’s URI.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f285b-183">通話</span><span class="sxs-lookup"><span data-stu-id="f285b-183">CallPrioirty</span></span></p></td>
<td><p><span data-ttu-id="f285b-184">int</span><span class="sxs-lookup"><span data-stu-id="f285b-184">int</span></span></p></td>
<td><p><span data-ttu-id="f285b-185">通話の優先度。</span><span class="sxs-lookup"><span data-stu-id="f285b-185">Priority of the call.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="f285b-186">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f285b-186">


</div>

<span> </span>

</div>

</div>

</span></span></div>

