---
title: 'Lync Server 2013: MediaLine view'
description: 'Lync Server 2013: MediaLine ビュー。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: MediaLine view
ms:assetid: 132eca13-8913-4218-9eff-4960ced8c3dc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687972(v=OCS.15)
ms:contentKeyID: 49733560
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4c61fcc15b46958622e6cddd66427255a6def154
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445947"
---
# <a name="medialine-view-in-lync-server-2013"></a><span data-ttu-id="4d0be-103">Lync Server 2013 での MediaLine の表示</span><span class="sxs-lookup"><span data-stu-id="4d0be-103">MediaLine view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4d0be-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4d0be-104">

<span> </span></span></span>

<span data-ttu-id="4d0be-105">_**最終更新日:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="4d0be-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="4d0be-106">MediaLine ビューには、データベース内の各メディアラインに関する情報が格納されます。</span><span class="sxs-lookup"><span data-stu-id="4d0be-106">The MediaLine View stores information about each media line in the database.</span></span> <span data-ttu-id="4d0be-107">1つのオーディオセッションには通常、1つのオーディオメディアラインが含まれています。</span><span class="sxs-lookup"><span data-stu-id="4d0be-107">One audio session typically contains one audio media line.</span></span> <span data-ttu-id="4d0be-108">通常、1つのオーディオとビデオ (A/V) セッションには、1つのオーディオメディアラインと1つのビデオメディアラインが含まれます。ただし、会議デバイスが使用されている場合、または [ギャラリー] ビューを使用している場合は、2つのビデオメディアがセッションに含まれている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4d0be-108">One audio and video (A/V) session typically contains one audio media line and one video media line; however, the session might contain two video media lines if a conferencing device is used or if Gallery View is used.</span></span> <span data-ttu-id="4d0be-109">このビューは、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="4d0be-109">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4d0be-110">列</span><span class="sxs-lookup"><span data-stu-id="4d0be-110">Column</span></span></th>
<th><span data-ttu-id="4d0be-111">データ型</span><span class="sxs-lookup"><span data-stu-id="4d0be-111">Data Type</span></span></th>
<th><span data-ttu-id="4d0be-112">説明</span><span class="sxs-lookup"><span data-stu-id="4d0be-112">details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4d0be-113">ConferenceDateTime</span><span class="sxs-lookup"><span data-stu-id="4d0be-113">ConferenceDateTime</span></span></p></td>
<td><p><span data-ttu-id="4d0be-114">datetime</span><span class="sxs-lookup"><span data-stu-id="4d0be-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="4d0be-115"><a href="lync-server-2013-medialine-table.md">Lync Server 2013 の MediaLine テーブル</a>から参照されている。</span><span class="sxs-lookup"><span data-stu-id="4d0be-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d0be-116">SessionSeq</span><span class="sxs-lookup"><span data-stu-id="4d0be-116">SessionSeq</span></span></p></td>
<td><p><span data-ttu-id="4d0be-117">int</span><span class="sxs-lookup"><span data-stu-id="4d0be-117">int</span></span></p></td>
<td><p><span data-ttu-id="4d0be-118"><a href="lync-server-2013-medialine-table.md">Lync Server 2013 の MediaLine テーブル</a>から参照されている。</span><span class="sxs-lookup"><span data-stu-id="4d0be-118">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d0be-119">MediaLineLabel</span><span class="sxs-lookup"><span data-stu-id="4d0be-119">MediaLineLabel</span></span></p></td>
<td><p><span data-ttu-id="4d0be-120">tinyint</span><span class="sxs-lookup"><span data-stu-id="4d0be-120">tinyint</span></span></p></td>
<td><p><span data-ttu-id="4d0be-121"><a href="lync-server-2013-medialine-table.md">Lync Server 2013 の MediaLine テーブル</a>から参照されている。</span><span class="sxs-lookup"><span data-stu-id="4d0be-121">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d0be-122">CallerIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="4d0be-122">CallerIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="4d0be-123">int</span><span class="sxs-lookup"><span data-stu-id="4d0be-123">int</span></span></p></td>
<td><p><span data-ttu-id="4d0be-124">発信者の bits フラグで説明されている対話型接続確立 (ICE) プロセスに関する情報。</span><span class="sxs-lookup"><span data-stu-id="4d0be-124">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the caller.</span></span> <span data-ttu-id="4d0be-125">詳細については、「エクスペリエンスの品質監視サーバープロトコルの仕様」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4d0be-125">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d0be-126">CalleeIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="4d0be-126">CalleeIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="4d0be-127">int</span><span class="sxs-lookup"><span data-stu-id="4d0be-127">int</span></span></p></td>
<td><p><span data-ttu-id="4d0be-128">対話式接続確立 (ICE) プロセスについて詳しくは、「呼び出し先のビットフラグ」で説明します。</span><span class="sxs-lookup"><span data-stu-id="4d0be-128">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the callee.</span></span> <span data-ttu-id="4d0be-129">詳細については、「エクスペリエンスの品質監視サーバープロトコルの仕様」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4d0be-129">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d0be-130">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="4d0be-130">Security</span></span></p></td>
<td><p><span data-ttu-id="4d0be-131">tinyint</span><span class="sxs-lookup"><span data-stu-id="4d0be-131">tinyint</span></span></p></td>
<td><p><span data-ttu-id="4d0be-132">セキュリティプロファイルが使用されています。</span><span class="sxs-lookup"><span data-stu-id="4d0be-132">Security profile in use.</span></span> <span data-ttu-id="4d0be-133">0は NONE、1は SRTP、2は V1 です。</span><span class="sxs-lookup"><span data-stu-id="4d0be-133">0 is NONE, 1 is SRTP, 2 is V1.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d0be-134">Transport</span><span class="sxs-lookup"><span data-stu-id="4d0be-134">Transport</span></span></p></td>
<td><p><span data-ttu-id="4d0be-135">tinyint</span><span class="sxs-lookup"><span data-stu-id="4d0be-135">tinyint</span></span></p></td>
<td><p><span data-ttu-id="4d0be-136">トランスポートの種類。</span><span class="sxs-lookup"><span data-stu-id="4d0be-136">Transport type.</span></span> <span data-ttu-id="4d0be-137">0は UDP、1は TCP です。</span><span class="sxs-lookup"><span data-stu-id="4d0be-137">0 is UDP, 1 is TCP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d0be-138">CallerIPAddr</span><span class="sxs-lookup"><span data-stu-id="4d0be-138">CallerIPAddr</span></span></p></td>
<td><p><span data-ttu-id="4d0be-139">var (50)</span><span class="sxs-lookup"><span data-stu-id="4d0be-139">var(50)</span></span></p></td>
<td><p><span data-ttu-id="4d0be-140">発信者の IP アドレス。</span><span class="sxs-lookup"><span data-stu-id="4d0be-140">IP address of the caller.</span></span> <span data-ttu-id="4d0be-141">これは IPv4 または IPv6 のアドレスにすることができます。</span><span class="sxs-lookup"><span data-stu-id="4d0be-141">This can be either an IPv4 or IPv6 address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d0be-142">CallerPort</span><span class="sxs-lookup"><span data-stu-id="4d0be-142">CallerPort</span></span></p></td>
<td><p><span data-ttu-id="4d0be-143">int</span><span class="sxs-lookup"><span data-stu-id="4d0be-143">int</span></span></p></td>
<td><p><span data-ttu-id="4d0be-144">発信者によって使用されるポート。</span><span class="sxs-lookup"><span data-stu-id="4d0be-144">Port used by the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d0be-145">CallerInside</span><span class="sxs-lookup"><span data-stu-id="4d0be-145">CallerInside</span></span></p></td>
<td><p><span data-ttu-id="4d0be-146">bit</span><span class="sxs-lookup"><span data-stu-id="4d0be-146">bit</span></span></p></td>
<td><p><span data-ttu-id="4d0be-147">発信者が組織のネットワーク内にあるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="4d0be-147">Indicates whether or not the caller is inside the organization network.</span></span> <span data-ttu-id="4d0be-148">1発信者がエンタープライズネットワーク内にあることを意味します。</span><span class="sxs-lookup"><span data-stu-id="4d0be-148">1 means that the caller is inside the enterprise network.</span></span> <span data-ttu-id="4d0be-149">0は、発信者がネットワーク外であることを意味します。</span><span class="sxs-lookup"><span data-stu-id="4d0be-149">0 means that the caller is outside the network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d0be-150">CallerMacAddress</span><span class="sxs-lookup"><span data-stu-id="4d0be-150">CallerMacAddress</span></span></p></td>
<td><p><span data-ttu-id="4d0be-151">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="4d0be-151">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="4d0be-152">発信者によって使用されるネットワークインターフェイスの MAC アドレスです。</span><span class="sxs-lookup"><span data-stu-id="4d0be-152">MAC address of network interface used by caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d0be-153">CallerRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="4d0be-153">CallerRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="4d0be-154">var (50)</span><span class="sxs-lookup"><span data-stu-id="4d0be-154">var(50)</span></span></p></td>
<td><p><span data-ttu-id="4d0be-155">発信者によって使用される A/V Edge サービスの IP アドレス。</span><span class="sxs-lookup"><span data-stu-id="4d0be-155">IP Address of the A/V Edge service used by the caller.</span></span> <span data-ttu-id="4d0be-156">詳細については、「 <a href="lync-server-2013-ipaddress-table.md">Lync Server 2013 の IPAddress テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4d0be-156">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d0be-157">CalleeRelayPort</span><span class="sxs-lookup"><span data-stu-id="4d0be-157">CalleeRelayPort</span></span></p></td>
<td><p><span data-ttu-id="4d0be-158">int</span><span class="sxs-lookup"><span data-stu-id="4d0be-158">int</span></span></p></td>
<td><p><span data-ttu-id="4d0be-159">発信者が使用する A/V Edge サービスで使用されるポート。</span><span class="sxs-lookup"><span data-stu-id="4d0be-159">Port used on the A/V Edge service used by the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d0be-160">CallerReflexiveIPAddr</span><span class="sxs-lookup"><span data-stu-id="4d0be-160">CallerReflexiveIPAddr</span></span></p></td>
<td><p><span data-ttu-id="4d0be-161">var (50)</span><span class="sxs-lookup"><span data-stu-id="4d0be-161">var(50)</span></span></p></td>
<td><p><span data-ttu-id="4d0be-162">A/V Edge サービスによって報告された発信者の IP アドレス。</span><span class="sxs-lookup"><span data-stu-id="4d0be-162">Caller’s IP address as reported by the A/V Edge service.</span></span> <span data-ttu-id="4d0be-163">このアドレスは、クライアントが NAT の背後にある場合など、CallerIPAddr と異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="4d0be-163">This address may be different that the CallerIPAddr if the client is located behind a NAT for example.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d0be-164">CallerCaptureDev</span><span class="sxs-lookup"><span data-stu-id="4d0be-164">CallerCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="4d0be-165">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="4d0be-165">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="4d0be-166">発信者のキャプチャデバイス名。</span><span class="sxs-lookup"><span data-stu-id="4d0be-166">Caller’s capture device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d0be-167">CallerRenderDev</span><span class="sxs-lookup"><span data-stu-id="4d0be-167">CallerRenderDev</span></span></p></td>
<td><p><span data-ttu-id="4d0be-168">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="4d0be-168">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="4d0be-169">発信者のレンダーデバイス名。</span><span class="sxs-lookup"><span data-stu-id="4d0be-169">Caller’s render device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d0be-170">CallerCaptureDevDriver</span><span class="sxs-lookup"><span data-stu-id="4d0be-170">CallerCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="4d0be-171">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="4d0be-171">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="4d0be-172">発信者のキャプチャデバイスドライバー名。</span><span class="sxs-lookup"><span data-stu-id="4d0be-172">Caller’s capture device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d0be-173">CallerRenderDevDriver</span><span class="sxs-lookup"><span data-stu-id="4d0be-173">CallerRenderDevDriver</span></span></p></td>
<td><p><span data-ttu-id="4d0be-174">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="4d0be-174">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="4d0be-175">発信者のレンダーデバイスドライバー名。</span><span class="sxs-lookup"><span data-stu-id="4d0be-175">Caller’s render device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d0be-176">CallerWifiDriverDeviceDesc</span><span class="sxs-lookup"><span data-stu-id="4d0be-176">CallerWifiDriverDeviceDesc</span></span></p></td>
<td><p><span data-ttu-id="4d0be-177">varchar (256</span><span class="sxs-lookup"><span data-stu-id="4d0be-177">varchar(256</span></span></p></td>
<td><p><span data-ttu-id="4d0be-178">発信者の Wifi ドライバーの説明。</span><span class="sxs-lookup"><span data-stu-id="4d0be-178">Caller’s Wifi driver description.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d0be-179">CallerWifiDriverVersion</span><span class="sxs-lookup"><span data-stu-id="4d0be-179">CallerWifiDriverVersion</span></span></p></td>
<td><p><span data-ttu-id="4d0be-180">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="4d0be-180">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="4d0be-181">発信者の Wifi ドライババージョン。</span><span class="sxs-lookup"><span data-stu-id="4d0be-181">Caller’s Wifi driver version.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d0be-182">CalleeNetworkConnectionDetail</span><span class="sxs-lookup"><span data-stu-id="4d0be-182">CalleeNetworkConnectionDetail</span></span></p></td>
<td><p><span data-ttu-id="4d0be-183">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="4d0be-183">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="4d0be-184">発信者のネットワーク接続の詳細。</span><span class="sxs-lookup"><span data-stu-id="4d0be-184">Details of caller’s network connection.</span></span> <span data-ttu-id="4d0be-185">詳細については、「 <a href="lync-server-2013-networkconnectiondetail-table.md">Lync Server 2013 での Networkconnectiondetail の表</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4d0be-185">See the <a href="lync-server-2013-networkconnectiondetail-table.md">NetworkConnectionDetail table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d0be-186">CallerBssid</span><span class="sxs-lookup"><span data-stu-id="4d0be-186">CallerBssid</span></span></p></td>
<td><p><span data-ttu-id="4d0be-187">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="4d0be-187">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="4d0be-188">発信者の WiFi 接続で使用される基本サービスセット識別子。</span><span class="sxs-lookup"><span data-stu-id="4d0be-188">Basic Service Set Identifier used by callers WiFi connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d0be-189">CallerVPN</span><span class="sxs-lookup"><span data-stu-id="4d0be-189">CallerVPN</span></span></p></td>
<td><p><span data-ttu-id="4d0be-190">bit</span><span class="sxs-lookup"><span data-stu-id="4d0be-190">bit</span></span></p></td>
<td><p><span data-ttu-id="4d0be-191">発信者が仮想プライベートネットワーク経由で接続しているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="4d0be-191">Indicates whether the caller connected over a virtual private network.</span></span> <span data-ttu-id="4d0be-192">1は仮想プライベートネットワーク (VPN)、0は非 VPN です。</span><span class="sxs-lookup"><span data-stu-id="4d0be-192">1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d0be-193">CalleeIPAddr</span><span class="sxs-lookup"><span data-stu-id="4d0be-193">CalleeIPAddr</span></span></p></td>
<td><p><span data-ttu-id="4d0be-194">var (50)</span><span class="sxs-lookup"><span data-stu-id="4d0be-194">var(50)</span></span></p></td>
<td><p><span data-ttu-id="4d0be-195">呼び出し先の IP アドレス。</span><span class="sxs-lookup"><span data-stu-id="4d0be-195">IP address of the callee.</span></span> <span data-ttu-id="4d0be-196">これは IPv4 または IPv6 のアドレスにすることができます。</span><span class="sxs-lookup"><span data-stu-id="4d0be-196">This can be either an IPv4 or IPv6 address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d0be-197">CalleePort</span><span class="sxs-lookup"><span data-stu-id="4d0be-197">CalleePort</span></span></p></td>
<td><p><span data-ttu-id="4d0be-198">int</span><span class="sxs-lookup"><span data-stu-id="4d0be-198">int</span></span></p></td>
<td><p><span data-ttu-id="4d0be-199">呼び出し先によって使用されるポート。</span><span class="sxs-lookup"><span data-stu-id="4d0be-199">Port used by the callee.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d0be-200">CalleeInside</span><span class="sxs-lookup"><span data-stu-id="4d0be-200">CalleeInside</span></span></p></td>
<td><p><span data-ttu-id="4d0be-201">bit</span><span class="sxs-lookup"><span data-stu-id="4d0be-201">bit</span></span></p></td>
<td><p><span data-ttu-id="4d0be-202">呼び出し先がエンタープライズネットワーク内にあるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="4d0be-202">Indicates whether the callee is inside the enterprise network.</span></span> <span data-ttu-id="4d0be-203">1は、呼び出し先がエンタープライズネットワーク内にあることを意味します。0は、呼び出し先がネットワークの外部にあることを意味します。</span><span class="sxs-lookup"><span data-stu-id="4d0be-203">1 means callee is inside the enterprise network, 0 means the callee is outside the network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d0be-204">CalleeMacAddress</span><span class="sxs-lookup"><span data-stu-id="4d0be-204">CalleeMacAddress</span></span></p></td>
<td><p><span data-ttu-id="4d0be-205">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="4d0be-205">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="4d0be-206">呼び出し先によって使用されるネットワークインターフェイスの MAC アドレスです。</span><span class="sxs-lookup"><span data-stu-id="4d0be-206">MAC address of network interface used by callee.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d0be-207">CalleeRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="4d0be-207">CalleeRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="4d0be-208">var (50)</span><span class="sxs-lookup"><span data-stu-id="4d0be-208">var(50)</span></span></p></td>
<td><p><span data-ttu-id="4d0be-209">呼び出し先によって使用される A/V エッジサービスの IP アドレス。</span><span class="sxs-lookup"><span data-stu-id="4d0be-209">IP Address of the A/V Edge service used by the callee.</span></span> <span data-ttu-id="4d0be-210">詳細については、「 <a href="lync-server-2013-ipaddress-table.md">Lync Server 2013 の IPAddress テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4d0be-210">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d0be-211">CalleeRelayPort</span><span class="sxs-lookup"><span data-stu-id="4d0be-211">CalleeRelayPort</span></span></p></td>
<td><p><span data-ttu-id="4d0be-212">int</span><span class="sxs-lookup"><span data-stu-id="4d0be-212">int</span></span></p></td>
<td><p><span data-ttu-id="4d0be-213">呼び出し先によって使用される A/V Edge サービスで使用されるポート。</span><span class="sxs-lookup"><span data-stu-id="4d0be-213">Port used on the A/V Edge service used by the callee.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d0be-214">CalleeReflexiveIPAddr</span><span class="sxs-lookup"><span data-stu-id="4d0be-214">CalleeReflexiveIPAddr</span></span></p></td>
<td><p><span data-ttu-id="4d0be-215">var (50)</span><span class="sxs-lookup"><span data-stu-id="4d0be-215">var(50)</span></span></p></td>
<td><p><span data-ttu-id="4d0be-216">A/V Edge サービスによって報告された呼び出し先の IP アドレス。</span><span class="sxs-lookup"><span data-stu-id="4d0be-216">Callee’s IP address as reported by the A/V Edge service.</span></span> <span data-ttu-id="4d0be-217">このアドレスは、クライアントが NAT の背後にある場合など、CalleeIPAddr と異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="4d0be-217">This address may be different that the CalleeIPAddr if the client is located behind a NAT for example.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d0be-218">Calleecapdev</span><span class="sxs-lookup"><span data-stu-id="4d0be-218">CalleeCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="4d0be-219">var (50)</span><span class="sxs-lookup"><span data-stu-id="4d0be-219">var(50)</span></span></p></td>
<td><p><span data-ttu-id="4d0be-220">呼び出し先のキャプチャデバイス名。</span><span class="sxs-lookup"><span data-stu-id="4d0be-220">Callee’s capture device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d0be-221">Calle・ Enderdev</span><span class="sxs-lookup"><span data-stu-id="4d0be-221">CalleeRenderDev</span></span></p></td>
<td><p><span data-ttu-id="4d0be-222">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="4d0be-222">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="4d0be-223">呼び出し先のレンダリングデバイス名。</span><span class="sxs-lookup"><span data-stu-id="4d0be-223">Callee’s render device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d0be-224">Calleecapdevdriver</span><span class="sxs-lookup"><span data-stu-id="4d0be-224">CalleeCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="4d0be-225">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="4d0be-225">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="4d0be-226">呼び出し先のキャプチャデバイスドライバー名。</span><span class="sxs-lookup"><span data-stu-id="4d0be-226">Callee’s capture device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d0be-227">CalleeRenderDevDriver</span><span class="sxs-lookup"><span data-stu-id="4d0be-227">CalleeRenderDevDriver</span></span></p></td>
<td><p><span data-ttu-id="4d0be-228">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="4d0be-228">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="4d0be-229">呼び出し先のレンダリングデバイスドライバー名。</span><span class="sxs-lookup"><span data-stu-id="4d0be-229">Callee’s render device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d0be-230">CalleeWifiDriverDeviceDesc</span><span class="sxs-lookup"><span data-stu-id="4d0be-230">CalleeWifiDriverDeviceDesc</span></span></p></td>
<td><p><span data-ttu-id="4d0be-231">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="4d0be-231">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="4d0be-232">呼び出し先の Wifi ドライバーの説明。</span><span class="sxs-lookup"><span data-stu-id="4d0be-232">Callee’s Wifi driver description.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d0be-233">CalleeWifiDriverVersion</span><span class="sxs-lookup"><span data-stu-id="4d0be-233">CalleeWifiDriverVersion</span></span></p></td>
<td><p><span data-ttu-id="4d0be-234">varchar (256</span><span class="sxs-lookup"><span data-stu-id="4d0be-234">varchar(256</span></span></p></td>
<td><p><span data-ttu-id="4d0be-235">呼び出し先の Wifi ドライバーバージョン。</span><span class="sxs-lookup"><span data-stu-id="4d0be-235">Callee’s Wifi driver version.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d0be-236">CalleeNetworkConnectionDetail</span><span class="sxs-lookup"><span data-stu-id="4d0be-236">CalleeNetworkConnectionDetail</span></span></p></td>
<td><p><span data-ttu-id="4d0be-237">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="4d0be-237">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="4d0be-238">呼び出し先のネットワーク接続の詳細。</span><span class="sxs-lookup"><span data-stu-id="4d0be-238">Details of callee’s network connection.</span></span> <span data-ttu-id="4d0be-239">詳細については、「 <a href="lync-server-2013-networkconnectiondetail-table.md">Lync Server 2013 での Networkconnectiondetail の表</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4d0be-239">See the <a href="lync-server-2013-networkconnectiondetail-table.md">NetworkConnectionDetail table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d0be-240">CalleeBssid</span><span class="sxs-lookup"><span data-stu-id="4d0be-240">CalleeBssid</span></span></p></td>
<td><p><span data-ttu-id="4d0be-241">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="4d0be-241">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="4d0be-242">呼び出し先の WiFi 接続で使用される基本サービスセット識別子。</span><span class="sxs-lookup"><span data-stu-id="4d0be-242">Basic Service Set Identifier used by callee’s WiFi connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d0be-243">CalleeVPN</span><span class="sxs-lookup"><span data-stu-id="4d0be-243">CalleeVPN</span></span></p></td>
<td><p><span data-ttu-id="4d0be-244">bit</span><span class="sxs-lookup"><span data-stu-id="4d0be-244">bit</span></span></p></td>
<td><p><span data-ttu-id="4d0be-245">呼び出し先が仮想プライベートネットワーク経由で接続されているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="4d0be-245">Indicates whether the callee connected over a virtual private network.</span></span> <span data-ttu-id="4d0be-246">1は仮想プライベートネットワーク (VPN)、0は非 VPN です。</span><span class="sxs-lookup"><span data-stu-id="4d0be-246">1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d0be-247">ConversationalMOS</span><span class="sxs-lookup"><span data-stu-id="4d0be-247">ConversationalMOS</span></span></p></td>
<td><p><span data-ttu-id="4d0be-248">10進数 (3, 2)</span><span class="sxs-lookup"><span data-stu-id="4d0be-248">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="4d0be-249">オーディオセッションの会話 MOS を Narrowband します (両方のオーディオストリームに基づく)。</span><span class="sxs-lookup"><span data-stu-id="4d0be-249">Narrowband Conversational MOS of the audio sessions (based on both audio streams).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d0be-250">AppliedBandwidthLimit</span><span class="sxs-lookup"><span data-stu-id="4d0be-250">AppliedBandwidthLimit</span></span></p></td>
<td><p><span data-ttu-id="4d0be-251">int</span><span class="sxs-lookup"><span data-stu-id="4d0be-251">int</span></span></p></td>
<td><p><span data-ttu-id="4d0be-252">これは、さまざまなポリシー設定 (TURN、API、SDP、ポリシーサーバーなど) によって指定された send side stream に適用される実際の帯域幅です。</span><span class="sxs-lookup"><span data-stu-id="4d0be-252">This is the actual bandwidth applied to the given send side stream given various policy settings (TURN, API, SDP, Policy Server, etc.).</span></span> <span data-ttu-id="4d0be-253">これは、帯域幅の推定値に基づいて低帯域幅を使用できるため、有効帯域幅と混同しないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="4d0be-253">This should not to be confused with the effective bandwidth because there can be a lower effective bandwidth based on the bandwidth estimate.</span></span> <span data-ttu-id="4d0be-254">これは基本的に最大帯域幅であり、送信ストリームは、帯域幅の推定値によって課された制限を受けません。</span><span class="sxs-lookup"><span data-stu-id="4d0be-254">This is basically the maximum bandwidth the send stream can take barring limits imposed by the bandwidth estimate.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d0be-255">AppliedBandwidthSource</span><span class="sxs-lookup"><span data-stu-id="4d0be-255">AppliedBandwidthSource</span></span></p></td>
<td><p><span data-ttu-id="4d0be-256">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="4d0be-256">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="4d0be-257">適用される帯域幅キャップのソース。</span><span class="sxs-lookup"><span data-stu-id="4d0be-257">Source of the bandwidth cap being imposed.</span></span> <span data-ttu-id="4d0be-258">帯域幅の制限の対象となる場所 (たとえば、"Policy Server"、"TURN Server"、"モダリティ" など) について説明します。</span><span class="sxs-lookup"><span data-stu-id="4d0be-258">It describes where the bandwidth limit is coming from (for example, “Policy Server”, “TURN Server”, or “Modality”).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d0be-259">[発信者]</span><span class="sxs-lookup"><span data-stu-id="4d0be-259">Caller</span></span></p></td>
<td><p><span data-ttu-id="4d0be-260">bit</span><span class="sxs-lookup"><span data-stu-id="4d0be-260">bit</span></span></p></td>
<td><p><span data-ttu-id="4d0be-261">呼び出し元からのメトリックが受信されたかどうかを示します。1は yes、0はいいえ。</span><span class="sxs-lookup"><span data-stu-id="4d0be-261">Indicates whether metrics from the caller were received; 1 is yes, 0 is no.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d0be-262">[呼び出し先]</span><span class="sxs-lookup"><span data-stu-id="4d0be-262">Callee</span></span></p></td>
<td><p><span data-ttu-id="4d0be-263">bit</span><span class="sxs-lookup"><span data-stu-id="4d0be-263">bit</span></span></p></td>
<td><p><span data-ttu-id="4d0be-264">通話レシーバーからのメトリックが受信されたかどうかを示します。1は yes、0はいいえ。</span><span class="sxs-lookup"><span data-stu-id="4d0be-264">Indicates whether metrics from the call receiver were received; 1 is yes, 0 is no.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d0be-265">MidCallReport</span><span class="sxs-lookup"><span data-stu-id="4d0be-265">MidCallReport</span></span></p></td>
<td><p><span data-ttu-id="4d0be-266">bit</span><span class="sxs-lookup"><span data-stu-id="4d0be-266">bit</span></span></p></td>
<td><p><span data-ttu-id="4d0be-267">レポートが通話の一部であるか、または完了しているかを示します。</span><span class="sxs-lookup"><span data-stu-id="4d0be-267">Indicates whether the report is for a portion of the call or for the complete call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d0be-268">ClassifiedPoorCall</span><span class="sxs-lookup"><span data-stu-id="4d0be-268">ClassifiedPoorCall</span></span></p></td>
<td><p><span data-ttu-id="4d0be-269">bit</span><span class="sxs-lookup"><span data-stu-id="4d0be-269">bit</span></span></p></td>
<td><p><span data-ttu-id="4d0be-270">通話が低品質通話 (1) として分類されたか、または良好な通話 (0) であるかを示します。</span><span class="sxs-lookup"><span data-stu-id="4d0be-270">Indicates whether a call was classified as a poor call (1) or as a good call (0).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d0be-271">CallerConnectivityICE</span><span class="sxs-lookup"><span data-stu-id="4d0be-271">CallerConnectivityICE</span></span></p></td>
<td><p><span data-ttu-id="4d0be-272">tinyint</span><span class="sxs-lookup"><span data-stu-id="4d0be-272">tinyint</span></span></p></td>
<td><p><span data-ttu-id="4d0be-273">発信者が ICE プロトコル (インターネット接続の確立) を使ってネットワークに接続しているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="4d0be-273">Indicates whether the caller connected to the network using the ICE protocol (Internet Connectivity Establishment).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d0be-274">CalleeConnectivityICE</span><span class="sxs-lookup"><span data-stu-id="4d0be-274">CalleeConnectivityICE</span></span></p></td>
<td><p><span data-ttu-id="4d0be-275">tinyint</span><span class="sxs-lookup"><span data-stu-id="4d0be-275">tinyint</span></span></p></td>
<td><p><span data-ttu-id="4d0be-276">ユーザーが ICE プロトコル (インターネット接続の確立) を使ってネットワークに接続しているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="4d0be-276">Indicates whether the user called connected to the network using the ICE protocol (Internet Connectivity Establishment).</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="4d0be-277">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4d0be-277">


</div>

<span> </span>

</div>

</div>

</span></span></div>

