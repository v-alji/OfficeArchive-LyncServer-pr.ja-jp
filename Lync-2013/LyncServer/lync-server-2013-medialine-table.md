---
title: 'Lync Server 2013: MediaLine テーブル'
description: 'Lync Server 2013: MediaLine テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: MediaLine table
ms:assetid: 414b1d63-ae97-4c27-bac0-c9ad0f808ff0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425920(v=OCS.15)
ms:contentKeyID: 48183956
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2acea8e14ba0608d9ebf72a48f888bfc4501fae3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425620"
---
# <a name="medialine-table-in-lync-server-2013"></a><span data-ttu-id="e4117-103">Lync Server 2013 の MediaLine テーブル</span><span class="sxs-lookup"><span data-stu-id="e4117-103">MediaLine table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e4117-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e4117-104">

<span> </span></span></span>

<span data-ttu-id="e4117-105">_**最終更新日:** 2014-02-21_</span><span class="sxs-lookup"><span data-stu-id="e4117-105">_**Topic Last Modified:** 2014-02-21_</span></span>

<span data-ttu-id="e4117-106">各レコードは1つのメディアラインを表します。</span><span class="sxs-lookup"><span data-stu-id="e4117-106">Each record represents one media line.</span></span> <span data-ttu-id="e4117-107">(1 つのオーディオセッションには通常、1つのオーディオメディアラインが含まれています。</span><span class="sxs-lookup"><span data-stu-id="e4117-107">(One audio session usually contains one audio media line.</span></span> <span data-ttu-id="e4117-108">1つのオーディオとビデオ (A/V) セッションには通常、1つのオーディオメディアラインと1つのビデオメディアラインが含まれていますが、会議デバイスが使用されている場合や、[ギャラリー] ビューを使用している場合は、2つのビデオメディア線が表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="e4117-108">One audio and video (A/V) session usually contains one audio media line and one video media line, although the session might contain two video media lines if a conferencing device is used or if Gallery View is used.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e4117-109"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-109"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="e4117-110"><strong>データ型</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-110"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="e4117-111"><strong>キー/インデックス</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-111"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="e4117-112"><strong>詳細</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-112"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e4117-113"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-113"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-114">datetime</span><span class="sxs-lookup"><span data-stu-id="e4117-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="e4117-115">Primary</span><span class="sxs-lookup"><span data-stu-id="e4117-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="e4117-116"><a href="lync-server-2013-session-table.md">Lync Server 2013 のセッションテーブル</a>から参照されます。</span><span class="sxs-lookup"><span data-stu-id="e4117-116">Referenced from the <a href="lync-server-2013-session-table.md">Session table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4117-117"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-117"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-118">int</span><span class="sxs-lookup"><span data-stu-id="e4117-118">int</span></span></p></td>
<td><p><span data-ttu-id="e4117-119">Primary</span><span class="sxs-lookup"><span data-stu-id="e4117-119">Primary</span></span></p></td>
<td><p><span data-ttu-id="e4117-120"><a href="lync-server-2013-session-table.md">Lync Server 2013 のセッションテーブル</a>から参照されます。</span><span class="sxs-lookup"><span data-stu-id="e4117-120">Referenced from the <a href="lync-server-2013-session-table.md">Session table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4117-121"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-121"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-122">tinyint</span><span class="sxs-lookup"><span data-stu-id="e4117-122">tinyint</span></span></p></td>
<td><p><span data-ttu-id="e4117-123">Primary</span><span class="sxs-lookup"><span data-stu-id="e4117-123">Primary</span></span></p></td>
<td><p><span data-ttu-id="e4117-124">0はメインオーディオ、1はメインビデオ、2はパノラマビデオ、3はアプリケーション/デスクトップ共有です。</span><span class="sxs-lookup"><span data-stu-id="e4117-124">0 is main audio, 1 is main video, and 2 is panoramic video, 3 is Application/Desktop Sharing.</span></span> <span data-ttu-id="e4117-125">このラベルは、1つのセッション内で一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="e4117-125">This label must be unique within a single session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4117-126"><strong>ConnectivityIce</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-126"><strong>ConnectivityIce</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-127">tinyint</span><span class="sxs-lookup"><span data-stu-id="e4117-127">tinyint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4117-128">この列は存在しますが、Microsoft Lync Server 2013 では使用されません。</span><span class="sxs-lookup"><span data-stu-id="e4117-128">This column is present but not used in Microsoft Lync Server 2013.</span></span> <span data-ttu-id="e4117-129">メディアラインに使用される接続に関する情報は、CallerConnectivityICE 列と CalleeConnectivityICE 列に記録されます。</span><span class="sxs-lookup"><span data-stu-id="e4117-129">Information about the connectivity used for a media line is captured in the CallerConnectivityICE and CalleeConnectivityICE columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4117-130"><strong>CallerIceWarningFlags</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-130"><strong>CallerIceWarningFlags</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-131">int</span><span class="sxs-lookup"><span data-stu-id="e4117-131">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4117-132">「Bits フラグ」で説明されている対話型接続確立 (ICE) プロセスに関する情報。</span><span class="sxs-lookup"><span data-stu-id="e4117-132">Information about Interactive Connectivity Establishment (ICE) process described in bits flags.</span></span> <span data-ttu-id="e4117-133">詳細については、「ダウンロード可能な <em>エクスペリエンス監視サーバープロトコルの仕様</em>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e4117-133">For details, refer to the <em>Quality of Experience Monitoring Server Protocol Specification</em>, available for download.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4117-134"><strong>CalleeIceWarningFlags</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-134"><strong>CalleeIceWarningFlags</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-135">int</span><span class="sxs-lookup"><span data-stu-id="e4117-135">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4117-136">CallerIceWarningFlags と同じですが、呼び出し先側でも同じです。</span><span class="sxs-lookup"><span data-stu-id="e4117-136">Same as CallerIceWarningFlags, but on the callee side.</span></span> <span data-ttu-id="e4117-137">詳細については、「ダウンロード可能な <em>エクスペリエンス監視サーバープロトコルの仕様</em>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e4117-137">For details, refer to the <em>Quality of Experience Monitoring Server Protocol Specification</em>, available for download.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4117-138"><strong>セキュリティ</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-138"><strong>Security</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-139">tinyint</span><span class="sxs-lookup"><span data-stu-id="e4117-139">tinyint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4117-140">使用されているセキュリティプロファイル。</span><span class="sxs-lookup"><span data-stu-id="e4117-140">The security profile in use.</span></span> <span data-ttu-id="e4117-141">0は NONE、1は SRTP、2は V1 です。</span><span class="sxs-lookup"><span data-stu-id="e4117-141">0 is NONE, 1 is SRTP, 2 is V1.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4117-142"><strong>Transport</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-142"><strong>Transport</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-143">tinyint</span><span class="sxs-lookup"><span data-stu-id="e4117-143">tinyint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4117-144">0は UDP、1は TCP です。</span><span class="sxs-lookup"><span data-stu-id="e4117-144">0 is UDP, 1 is TCP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4117-145"><strong>CallerIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-145"><strong>CallerIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-146">int</span><span class="sxs-lookup"><span data-stu-id="e4117-146">int</span></span></p></td>
<td><p><span data-ttu-id="e4117-147">外部</span><span class="sxs-lookup"><span data-stu-id="e4117-147">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e4117-148">発信者の IP アドレス。</span><span class="sxs-lookup"><span data-stu-id="e4117-148">IP Address of the caller.</span></span> <span data-ttu-id="e4117-149">詳細については、「 <a href="lync-server-2013-ipaddress-table.md">Lync Server 2013 の IPAddress テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e4117-149">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4117-150"><strong>CallerPort</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-150"><strong>CallerPort</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-151">int</span><span class="sxs-lookup"><span data-stu-id="e4117-151">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4117-152">発信者によって使用されるポート。</span><span class="sxs-lookup"><span data-stu-id="e4117-152">Port used by the caller.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4117-153"><strong>CallerSubnet</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-153"><strong>CallerSubnet</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-154">int</span><span class="sxs-lookup"><span data-stu-id="e4117-154">int</span></span></p></td>
<td><p> <span data-ttu-id="e4117-155">外部</span><span class="sxs-lookup"><span data-stu-id="e4117-155">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e4117-156">発信者のサブネット。</span><span class="sxs-lookup"><span data-stu-id="e4117-156">The subnet of the caller.</span></span> <span data-ttu-id="e4117-157">詳細については、「 <a href="lync-server-2013-ipaddress-table.md">Lync Server 2013 の IPAddress テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e4117-157">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4117-158"><strong>CallerInside</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-158"><strong>CallerInside</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-159">bit</span><span class="sxs-lookup"><span data-stu-id="e4117-159">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4117-160">1: 発信者がエンタープライズネットワーク内にあることを示します。0は、呼び出し元がネットワークの外部にあることを意味します。</span><span class="sxs-lookup"><span data-stu-id="e4117-160">1 means caller is inside the enterprise network, 0 means the caller is outside the network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4117-161"><strong>CallerMacAddress</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-161"><strong>CallerMacAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-162">int</span><span class="sxs-lookup"><span data-stu-id="e4117-162">int</span></span></p></td>
<td><p><span data-ttu-id="e4117-163">外部</span><span class="sxs-lookup"><span data-stu-id="e4117-163">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e4117-164">発信者の mac アドレス。 <a href="lync-server-2013-macaddress-table.md">Lync Server 2013 の MacAddress テーブル</a>から参照されています。</span><span class="sxs-lookup"><span data-stu-id="e4117-164">Caller’s mac address, referenced from <a href="lync-server-2013-macaddress-table.md">MacAddress table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4117-165"><strong>CallerRelayIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-165"><strong>CallerRelayIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-166">int</span><span class="sxs-lookup"><span data-stu-id="e4117-166">int</span></span></p></td>
<td><p><span data-ttu-id="e4117-167">外部</span><span class="sxs-lookup"><span data-stu-id="e4117-167">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e4117-168">発信者が使用した Lync Server A/V Edge サービスの IP アドレス。</span><span class="sxs-lookup"><span data-stu-id="e4117-168">IP Address of the Lync Server A/V Edge service used by the caller.</span></span> <span data-ttu-id="e4117-169">詳細については、「 <a href="lync-server-2013-ipaddress-table.md">Lync Server 2013 の IPAddress テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e4117-169">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4117-170"><strong>CallerRelayPort</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-170"><strong>CallerRelayPort</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-171">int</span><span class="sxs-lookup"><span data-stu-id="e4117-171">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4117-172">発信者によって、A/V Edge サービスで使用されるポート。</span><span class="sxs-lookup"><span data-stu-id="e4117-172">Port used on the A/V Edge service by the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4117-173"><strong>CallerCaptureDev</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-173"><strong>CallerCaptureDev</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-174">int</span><span class="sxs-lookup"><span data-stu-id="e4117-174">int</span></span></p></td>
<td><p><span data-ttu-id="e4117-175">外部</span><span class="sxs-lookup"><span data-stu-id="e4117-175">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e4117-176">発信者によって使用されるデバイスをキャプチャします。</span><span class="sxs-lookup"><span data-stu-id="e4117-176">Capture device used by the caller.</span></span> <span data-ttu-id="e4117-177"><a href="lync-server-2013-device-table.md">Lync Server 2013 のデバイステーブル</a>から参照されている。</span><span class="sxs-lookup"><span data-stu-id="e4117-177">Referenced from the <a href="lync-server-2013-device-table.md">Device table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4117-178"><strong>CallerRenderDev</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-178"><strong>CallerRenderDev</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-179">int</span><span class="sxs-lookup"><span data-stu-id="e4117-179">int</span></span></p></td>
<td><p><span data-ttu-id="e4117-180">外部</span><span class="sxs-lookup"><span data-stu-id="e4117-180">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e4117-181">発信者によって使われるレンダリングデバイス。</span><span class="sxs-lookup"><span data-stu-id="e4117-181">Render device used by caller.</span></span> <span data-ttu-id="e4117-182"><a href="lync-server-2013-device-table.md">Lync Server 2013 のデバイステーブル</a>から参照されている。</span><span class="sxs-lookup"><span data-stu-id="e4117-182">Referenced from the <a href="lync-server-2013-device-table.md">Device table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4117-183"><strong>CallerCaptureDevDriver</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-183"><strong>CallerCaptureDevDriver</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-184">int</span><span class="sxs-lookup"><span data-stu-id="e4117-184">int</span></span></p></td>
<td><p><span data-ttu-id="e4117-185">外部</span><span class="sxs-lookup"><span data-stu-id="e4117-185">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e4117-186">発信者のキャプチャデバイスのドライバー。 <a href="lync-server-2013-devicedriver-table.md">Lync Server 2013 の Devicedriver テーブル</a>から参照されます。</span><span class="sxs-lookup"><span data-stu-id="e4117-186">Driver for the caller’s capture device, referenced from the <a href="lync-server-2013-devicedriver-table.md">DeviceDriver table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4117-187"><strong>CallerRenderDevDriver</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-187"><strong>CallerRenderDevDriver</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-188">int</span><span class="sxs-lookup"><span data-stu-id="e4117-188">int</span></span></p></td>
<td><p><span data-ttu-id="e4117-189">外部</span><span class="sxs-lookup"><span data-stu-id="e4117-189">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e4117-190">発信者のレンダリングデバイスのドライバー。 <a href="lync-server-2013-devicedriver-table.md">Lync Server 2013 の devicedriver テーブル</a>から参照されます。</span><span class="sxs-lookup"><span data-stu-id="e4117-190">Driver for the caller’s render device, referenced from the <a href="lync-server-2013-devicedriver-table.md">DeviceDriver table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4117-191"><strong>CallerNetworkConnectionType</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-191"><strong>CallerNetworkConnectionType</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-192">tinyint</span><span class="sxs-lookup"><span data-stu-id="e4117-192">tinyint</span></span></p></td>
<td><p><span data-ttu-id="e4117-193">外部</span><span class="sxs-lookup"><span data-stu-id="e4117-193">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e4117-194">発信者がネットワークに接続した方法を示します。</span><span class="sxs-lookup"><span data-stu-id="e4117-194">Indicates how the caller connected to the network.</span></span> <span data-ttu-id="e4117-195">値は、 <a href="lync-server-2013-networkconnectiondetail-table.md">Lync Server 2013 の Networkconnectiondetail テーブル</a>から取得されます。</span><span class="sxs-lookup"><span data-stu-id="e4117-195">Values are obtained from the <a href="lync-server-2013-networkconnectiondetail-table.md">NetworkConnectionDetail table in Lync Server 2013</a>.</span></span> <span data-ttu-id="e4117-196">一般的な値は、有線接続の場合は0、WiFi 接続の場合は0です。イーサネット接続の場合は3。</span><span class="sxs-lookup"><span data-stu-id="e4117-196">Typical values are 0 for a wired connection’ 1 for a WiFi connection; and 3 for an Ethernet connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4117-197"><strong>CallerBssid</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-197"><strong>CallerBssid</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-198">int</span><span class="sxs-lookup"><span data-stu-id="e4117-198">int</span></span></p></td>
<td><p><span data-ttu-id="e4117-199">外部</span><span class="sxs-lookup"><span data-stu-id="e4117-199">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e4117-200">ワイヤレスが使用されている場合は、発信者の BSSID。</span><span class="sxs-lookup"><span data-stu-id="e4117-200">Caller’s BSSID if wireless is used.</span></span> <span data-ttu-id="e4117-201"><a href="lync-server-2013-macaddress-table.md">Lync Server 2013 の MacAddress テーブル</a>から参照されています。</span><span class="sxs-lookup"><span data-stu-id="e4117-201">Referenced from <a href="lync-server-2013-macaddress-table.md">MacAddress table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4117-202"><strong>CallerVPN</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-202"><strong>CallerVPN</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-203">bit</span><span class="sxs-lookup"><span data-stu-id="e4117-203">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e4117-204">発信者のリンク。</span><span class="sxs-lookup"><span data-stu-id="e4117-204">The caller's link.</span></span> <span data-ttu-id="e4117-205">1は仮想プライベートネットワーク (VPN)、0は非 VPN です。</span><span class="sxs-lookup"><span data-stu-id="e4117-205">1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4117-206"><strong>CallerLinkSpeed</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-206"><strong>CallerLinkSpeed</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-207">10進数 (18, 0)</span><span class="sxs-lookup"><span data-stu-id="e4117-207">decimal(18,0)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e4117-208">発信者のエンドポイントのネットワークリンク速度 (bps)。</span><span class="sxs-lookup"><span data-stu-id="e4117-208">The network link speed, in bps, for the caller's endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4117-209"><strong>CalleeIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-209"><strong>CalleeIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-210">int</span><span class="sxs-lookup"><span data-stu-id="e4117-210">int</span></span></p></td>
<td><p><span data-ttu-id="e4117-211">外部</span><span class="sxs-lookup"><span data-stu-id="e4117-211">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e4117-212">通話受信者の IP アドレス。</span><span class="sxs-lookup"><span data-stu-id="e4117-212">IP Address of the call receiver.</span></span> <span data-ttu-id="e4117-213">詳細については、「 <a href="lync-server-2013-ipaddress-table.md">Lync Server 2013 の IPAddress テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e4117-213">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4117-214"><strong>CalleePort</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-214"><strong>CalleePort</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-215">bit</span><span class="sxs-lookup"><span data-stu-id="e4117-215">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e4117-216">通話レシーバーで使用されているポート。</span><span class="sxs-lookup"><span data-stu-id="e4117-216">Port used by the call receiver.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4117-217"><strong>CalleeSubnet</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-217"><strong>CalleeSubnet</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-218">int</span><span class="sxs-lookup"><span data-stu-id="e4117-218">int</span></span></p></td>
<td><p><span data-ttu-id="e4117-219">外部</span><span class="sxs-lookup"><span data-stu-id="e4117-219">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e4117-220">呼び出し先のサブネット。</span><span class="sxs-lookup"><span data-stu-id="e4117-220">Subnet of callee.</span></span> <span data-ttu-id="e4117-221">詳細については、「 <a href="lync-server-2013-ipaddress-table.md">Lync Server 2013 の IPAddress テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e4117-221">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4117-222"><strong>CalleeInside</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-222"><strong>CalleeInside</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-223">bit</span><span class="sxs-lookup"><span data-stu-id="e4117-223">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4117-224">1: 通話受信者が企業ネットワーク内にあることを意味する0は、通話レシーバーがネットワークの外側にあることを意味します。</span><span class="sxs-lookup"><span data-stu-id="e4117-224">1 means call receiver is inside the enterprise network, 0 means the call receiver is outside the network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4117-225"><strong>CalleeMacAddress</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-225"><strong>CalleeMacAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-226">int</span><span class="sxs-lookup"><span data-stu-id="e4117-226">int</span></span></p></td>
<td><p><span data-ttu-id="e4117-227">外部</span><span class="sxs-lookup"><span data-stu-id="e4117-227">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e4117-228">呼び出し先 Mac アドレス。</span><span class="sxs-lookup"><span data-stu-id="e4117-228">Callee Mac address.</span></span> <span data-ttu-id="e4117-229"><a href="lync-server-2013-macaddress-table.md">Lync Server 2013 の MacAddress テーブル</a>から参照されている。</span><span class="sxs-lookup"><span data-stu-id="e4117-229">Referenced from the <a href="lync-server-2013-macaddress-table.md">MacAddress table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4117-230"><strong>CalleeRelayIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-230"><strong>CalleeRelayIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-231">int</span><span class="sxs-lookup"><span data-stu-id="e4117-231">int</span></span></p></td>
<td><p><span data-ttu-id="e4117-232">外部</span><span class="sxs-lookup"><span data-stu-id="e4117-232">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e4117-233">通話レシーバーによって使用される A/V エッジサービスの IP アドレス。</span><span class="sxs-lookup"><span data-stu-id="e4117-233">IP Address of the A/V Edge service used by the call receiver.</span></span> <span data-ttu-id="e4117-234">詳細については、「 <a href="lync-server-2013-ipaddress-table.md">Lync Server 2013 の IPAddress テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e4117-234">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4117-235"><strong>CalleeRelayPort</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-235"><strong>CalleeRelayPort</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-236">int</span><span class="sxs-lookup"><span data-stu-id="e4117-236">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4117-237">通話レシーバーによって、A/V Edge サービスで使用されるポート。</span><span class="sxs-lookup"><span data-stu-id="e4117-237">Port used on the A/V Edge Service by the call receiver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4117-238"><strong>Calleecapdev</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-238"><strong>CalleeCaptureDev</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-239">int</span><span class="sxs-lookup"><span data-stu-id="e4117-239">int</span></span></p></td>
<td><p><span data-ttu-id="e4117-240">外部</span><span class="sxs-lookup"><span data-stu-id="e4117-240">foreign</span></span></p></td>
<td><p><span data-ttu-id="e4117-241">通話レシーバーによって使用されるデバイスをキャプチャします。</span><span class="sxs-lookup"><span data-stu-id="e4117-241">Capture device used by the call receiver.</span></span> <span data-ttu-id="e4117-242"><a href="lync-server-2013-device-table.md">Lync Server 2013 のデバイステーブル</a>から参照されている。</span><span class="sxs-lookup"><span data-stu-id="e4117-242">Referenced from the <a href="lync-server-2013-device-table.md">Device table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4117-243"><strong>Calle・ Enderdev</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-243"><strong>CalleeRenderDev</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-244">int</span><span class="sxs-lookup"><span data-stu-id="e4117-244">int</span></span></p></td>
<td><p><span data-ttu-id="e4117-245">外部</span><span class="sxs-lookup"><span data-stu-id="e4117-245">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e4117-246">通話レシーバーによって使用されるレンダリングデバイス。</span><span class="sxs-lookup"><span data-stu-id="e4117-246">Render device used by the call receiver.</span></span> <span data-ttu-id="e4117-247"><a href="lync-server-2013-device-table.md">Lync Server 2013 のデバイステーブル</a>から参照されている。</span><span class="sxs-lookup"><span data-stu-id="e4117-247">Referenced from the <a href="lync-server-2013-device-table.md">Device table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4117-248"><strong>Calleecapdevdriver</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-248"><strong>CalleeCaptureDevDriver</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-249">int</span><span class="sxs-lookup"><span data-stu-id="e4117-249">int</span></span></p></td>
<td><p><span data-ttu-id="e4117-250">外部</span><span class="sxs-lookup"><span data-stu-id="e4117-250">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e4117-251">通話レシーバーのキャプチャデバイスのドライバー。</span><span class="sxs-lookup"><span data-stu-id="e4117-251">Driver for the call receiver’s capture device.</span></span> <span data-ttu-id="e4117-252"><a href="lync-server-2013-devicedriver-table.md">Lync Server 2013 の Devicedriver テーブル</a>から参照されています。</span><span class="sxs-lookup"><span data-stu-id="e4117-252">Referenced from <a href="lync-server-2013-devicedriver-table.md">DeviceDriver table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4117-253"><strong>CalleeRenderDevDriver</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-253"><strong>CalleeRenderDevDriver</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-254">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="e4117-254">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="e4117-255">外部</span><span class="sxs-lookup"><span data-stu-id="e4117-255">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e4117-256">通話レシーバーのレンダリングデバイスのドライバー。</span><span class="sxs-lookup"><span data-stu-id="e4117-256">Driver for the call receiver’s render device.</span></span> <span data-ttu-id="e4117-257"><a href="lync-server-2013-devicedriver-table.md">Lync Server 2013 の Devicedriver テーブル</a>から参照されています。</span><span class="sxs-lookup"><span data-stu-id="e4117-257">Referenced from <a href="lync-server-2013-devicedriver-table.md">DeviceDriver table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4117-258"><strong>CalleeNetworkConnectionType</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-258"><strong>CalleeNetworkConnectionType</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-259">tinyint</span><span class="sxs-lookup"><span data-stu-id="e4117-259">tinyint</span></span></p></td>
<td><p><span data-ttu-id="e4117-260">外部</span><span class="sxs-lookup"><span data-stu-id="e4117-260">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e4117-261">呼び出し先がネットワークに接続された方法を示します。</span><span class="sxs-lookup"><span data-stu-id="e4117-261">Indicates how the callee connected to the network.</span></span> <span data-ttu-id="e4117-262">値は、 <a href="lync-server-2013-networkconnectiondetail-table.md">Lync Server 2013 の Networkconnectiondetail テーブル</a>から取得されます。</span><span class="sxs-lookup"><span data-stu-id="e4117-262">Values are obtained from the <a href="lync-server-2013-networkconnectiondetail-table.md">NetworkConnectionDetail table in Lync Server 2013</a>.</span></span> <span data-ttu-id="e4117-263">一般的な値は、有線接続の場合は0、WiFi 接続の場合は0です。イーサネット接続の場合は3。</span><span class="sxs-lookup"><span data-stu-id="e4117-263">Typical values are 0 for a wired connection’ 1 for a WiFi connection; and 3 for an Ethernet connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4117-264"><strong>CalleeBssid</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-264"><strong>CalleeBssid</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-265">int</span><span class="sxs-lookup"><span data-stu-id="e4117-265">int</span></span></p></td>
<td><p><span data-ttu-id="e4117-266">外部</span><span class="sxs-lookup"><span data-stu-id="e4117-266">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e4117-267">ワイヤレスが使用されている場合は、呼び出し先の BSSID。</span><span class="sxs-lookup"><span data-stu-id="e4117-267">Callee’s BSSID if wireless is used.</span></span> <span data-ttu-id="e4117-268"><a href="lync-server-2013-macaddress-table.md">Lync Server 2013 の MacAddress テーブル</a>から参照されています。</span><span class="sxs-lookup"><span data-stu-id="e4117-268">Referenced from <a href="lync-server-2013-macaddress-table.md">MacAddress table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4117-269"><strong>CalleeVPN</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-269"><strong>CalleeVPN</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-270">bit</span><span class="sxs-lookup"><span data-stu-id="e4117-270">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4117-271">通話レシーバーのリンク。1は仮想プライベートネットワーク (VPN)、0は非 VPN です。</span><span class="sxs-lookup"><span data-stu-id="e4117-271">The call receiver’s link; 1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4117-272"><strong>CalleeLinkSpeed</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-272"><strong>CalleeLinkSpeed</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-273">10進数 (18, 0)</span><span class="sxs-lookup"><span data-stu-id="e4117-273">decimal(18,0)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4117-274">通話受信側エンドポイントのネットワークリンク速度 (bps)。</span><span class="sxs-lookup"><span data-stu-id="e4117-274">The network link speed, in bps, for the call receiver’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4117-275"><strong>ConversationalMOS</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-275"><strong>ConversationalMOS</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-276">10進数 (3, 2)</span><span class="sxs-lookup"><span data-stu-id="e4117-276">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4117-277">オーディオセッションの会話 MOS を Narrowband します (両方のオーディオストリームに基づく)。</span><span class="sxs-lookup"><span data-stu-id="e4117-277">Narrowband Conversational MOS of the audio sessions (based on both audio streams).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4117-278"><strong>AppliedBandwidthLimit</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-278"><strong>AppliedBandwidthLimit</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-279">int</span><span class="sxs-lookup"><span data-stu-id="e4117-279">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e4117-280">これは、さまざまなポリシー設定 (TURN、API、SDP、ポリシーサーバーなど) が指定された send side stream に適用される実際の帯域幅です。</span><span class="sxs-lookup"><span data-stu-id="e4117-280">This is the actual bandwidth applied to the given send side stream given various policy settings (TURN, API, SDP, Policy Server, and so on).</span></span> <span data-ttu-id="e4117-281">これは、帯域幅の推定値に基づいて低帯域幅を使用できるため、有効帯域幅と混同しないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e4117-281">This is not to be confused with the effective bandwidth because there can be a lower effective bandwidth based on the bandwidth estimate.</span></span> <span data-ttu-id="e4117-282">これは基本的に最大帯域幅であり、送信ストリームは、帯域幅の推定値によって課された制限を受けません。</span><span class="sxs-lookup"><span data-stu-id="e4117-282">This is basically the maximum bandwidth the send stream can take barring limits imposed by the bandwidth estimate.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4117-283"><strong>AppliedBandwidthSourceKey</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-283"><strong>AppliedBandwidthSourceKey</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-284">smallint</span><span class="sxs-lookup"><span data-stu-id="e4117-284">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e4117-285">これは、適用される帯域幅の上限のソースです。</span><span class="sxs-lookup"><span data-stu-id="e4117-285">This is the source of the bandwidth cap being imposed.</span></span> <span data-ttu-id="e4117-286">帯域幅の制限の対象となる場所について説明します ("Policy Server"、"TURN Server"、"モダリティ" など)。</span><span class="sxs-lookup"><span data-stu-id="e4117-286">It describes where the bandwidth limit is coming from (“Policy Server”, “TURN Server”, “Modality”, and so on).</span></span> <span data-ttu-id="e4117-287"><a href="lync-server-2013-appliedbandwidthsource-table.md">Lync Server 2013 の AppliedBandwidthSource テーブル</a>から参照されている。</span><span class="sxs-lookup"><span data-stu-id="e4117-287">Referenced from the <a href="lync-server-2013-appliedbandwidthsource-table.md">AppliedBandwidthSource table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4117-288"><strong>[発信者]</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-288"><strong>Caller</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-289">bit</span><span class="sxs-lookup"><span data-stu-id="e4117-289">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4117-290">呼び出し元からのメトリックが受信されたかどうかを示します。1は yes で、null 値は no です。</span><span class="sxs-lookup"><span data-stu-id="e4117-290">Indicates whether metrics from the caller were received; 1 is yes, a null value is no.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4117-291"><strong>[呼び出し先]</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-291"><strong>Callee</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-292">bit</span><span class="sxs-lookup"><span data-stu-id="e4117-292">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e4117-293">通話レシーバーからのメトリックが受信されたかどうかを示します。1は yes で、null 値は no です。</span><span class="sxs-lookup"><span data-stu-id="e4117-293">Indicates whether metrics from the call receiver were received; 1 is yes, a null value is no.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4117-294"><strong>MidCallReport</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-294"><strong>MidCallReport</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-295">bit</span><span class="sxs-lookup"><span data-stu-id="e4117-295">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e4117-296">レポートがセッションの一部であるか、セッション全体であるかを示します。</span><span class="sxs-lookup"><span data-stu-id="e4117-296">Indicates whether the report is for a portion of the session or for the complete session.</span></span></p>
<p><span data-ttu-id="e4117-297">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="e4117-297">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4117-298"><strong>ClassifiedPoorCall</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-298"><strong>ClassifiedPoorCall</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-299">bit</span><span class="sxs-lookup"><span data-stu-id="e4117-299">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e4117-300">通話が低品質通話 (1) または良好コール (0) として分類されているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="e4117-300">Indicates whether a call was classified as a poor call (value of 1) or as a good call (0).</span></span></p>
<p><span data-ttu-id="e4117-301">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="e4117-301">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4117-302"><strong>CallerConnectivityICE</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-302"><strong>CallerConnectivityICE</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-303">tinyInt</span><span class="sxs-lookup"><span data-stu-id="e4117-303">tinyInt</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e4117-304">発信者が ICE プロトコル (インターネット接続の確立) を使ってネットワークに接続しているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="e4117-304">Indicates whether the caller connected to the network using the ICE protocol (Internet Connectivity Establishment).</span></span></p>
<p><span data-ttu-id="e4117-305">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="e4117-305">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4117-306"><strong>CalleeConnectivityICE</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-306"><strong>CalleeConnectivityICE</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-307">tinyint</span><span class="sxs-lookup"><span data-stu-id="e4117-307">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e4117-308">発信者が ICE プロトコル (インターネット接続の確立) を使ってネットワークに接続しているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="e4117-308">Indicates whether the caller connected to the network using the ICE protocol (Internet Connectivity Establishment).</span></span></p>
<p><span data-ttu-id="e4117-309">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="e4117-309">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4117-310"><strong>CallerReflexiveLocalIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-310"><strong>CallerReflexiveLocalIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-311">int</span><span class="sxs-lookup"><span data-stu-id="e4117-311">int</span></span></p></td>
<td><p><span data-ttu-id="e4117-312">外部</span><span class="sxs-lookup"><span data-stu-id="e4117-312">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e4117-313">通話を発信したユーザーの再帰 IP アドレス。</span><span class="sxs-lookup"><span data-stu-id="e4117-313">Reflexive IP address of the user who placed the call.</span></span> <span data-ttu-id="e4117-314">NAT (ネットワークアドレス変換) を使用している組織では、再帰 IP アドレスはプロキシサーバーの IP アドレスです。</span><span class="sxs-lookup"><span data-stu-id="e4117-314">In organizations that use NAT (network address translation), the reflexive IP address is the IP address of the proxy server.</span></span></p>
<p><span data-ttu-id="e4117-315">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="e4117-315">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4117-316"><strong>CallerWiFiDriverDevicesDesc</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-316"><strong>CallerWiFiDriverDevicesDesc</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-317">int</span><span class="sxs-lookup"><span data-stu-id="e4117-317">int</span></span></p></td>
<td><p><span data-ttu-id="e4117-318">外部</span><span class="sxs-lookup"><span data-stu-id="e4117-318">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e4117-319">通話を発信したユーザーによって採用された WiFi ドライバーのデバイスの説明。</span><span class="sxs-lookup"><span data-stu-id="e4117-319">Device description for the WiFi driver employed by the user who placed the call.</span></span></p>
<p><span data-ttu-id="e4117-320">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="e4117-320">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4117-321"><strong>CallerWiFiDriverVersion</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-321"><strong>CallerWiFiDriverVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-322">int</span><span class="sxs-lookup"><span data-stu-id="e4117-322">int</span></span></p></td>
<td><p><span data-ttu-id="e4117-323">外部</span><span class="sxs-lookup"><span data-stu-id="e4117-323">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e4117-324">通話を発信したユーザーによって採用された WiFi ドライバーのバージョン番号。</span><span class="sxs-lookup"><span data-stu-id="e4117-324">Version number for the WiFi driver employed by the user who placed the call.</span></span></p>
<p><span data-ttu-id="e4117-325">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="e4117-325">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4117-326"><strong>CalleReflexiveLocalIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-326"><strong>CalleReflexiveLocalIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-327">int</span><span class="sxs-lookup"><span data-stu-id="e4117-327">int</span></span></p></td>
<td><p><span data-ttu-id="e4117-328">外部</span><span class="sxs-lookup"><span data-stu-id="e4117-328">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e4117-329">通話を受信したユーザーの再帰 IP アドレス。</span><span class="sxs-lookup"><span data-stu-id="e4117-329">Reflexive IP address of the user who received the call.</span></span> <span data-ttu-id="e4117-330">NAT (ネットワークアドレス変換) を使用している組織では、再帰 IP アドレスはプロキシサーバーの IP アドレスです。</span><span class="sxs-lookup"><span data-stu-id="e4117-330">In organizations that use NAT (network address translation), the reflexive IP address is the IP address of the proxy server.</span></span></p>
<p><span data-ttu-id="e4117-331">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="e4117-331">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4117-332"><strong>CalleeWiFiDriverDevicesDesc</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-332"><strong>CalleeWiFiDriverDevicesDesc</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-333">int</span><span class="sxs-lookup"><span data-stu-id="e4117-333">int</span></span></p></td>
<td><p><span data-ttu-id="e4117-334">外部</span><span class="sxs-lookup"><span data-stu-id="e4117-334">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e4117-335">通話を受信したユーザーによって採用された WiFi ドライバーのデバイスの説明。</span><span class="sxs-lookup"><span data-stu-id="e4117-335">Device description for the WiFi driver employed by the user who received the call.</span></span></p>
<p><span data-ttu-id="e4117-336">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="e4117-336">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4117-337"><strong>CalleeWiFiDriverVersion</strong></span><span class="sxs-lookup"><span data-stu-id="e4117-337"><strong>CalleeWiFiDriverVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="e4117-338">int</span><span class="sxs-lookup"><span data-stu-id="e4117-338">int</span></span></p></td>
<td><p><span data-ttu-id="e4117-339">外部</span><span class="sxs-lookup"><span data-stu-id="e4117-339">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e4117-340">通話を受信したユーザーが使用する WiFi ドライバーのバージョン番号。</span><span class="sxs-lookup"><span data-stu-id="e4117-340">Version number for the WiFi driver employed by the user who received the call.</span></span></p>
<p><span data-ttu-id="e4117-341">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="e4117-341">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="e4117-342">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e4117-342">


</div>

<span> </span>

</div>

</div>

</span></span></div>

