---
title: 'Lync Server 2013: AudioClientEvent テーブル'
description: 'Lync Server 2013: AudioClientEvent テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AudioClientEvent table
ms:assetid: fef73d8f-7261-4e5b-9769-82435b007979
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413086(v=OCS.15)
ms:contentKeyID: 48185967
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2200cd9567bdd10ac4ad8f5c269062c2f5614dcb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438211"
---
# <a name="audioclientevent-table-in-lync-server-2013"></a><span data-ttu-id="ff3da-103">Lync Server 2013 の AudioClientEvent テーブル</span><span class="sxs-lookup"><span data-stu-id="ff3da-103">AudioClientEvent table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ff3da-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ff3da-104">

<span> </span></span></span>

<span data-ttu-id="ff3da-105">_**最終更新日:** 2012-10-17_</span><span class="sxs-lookup"><span data-stu-id="ff3da-105">_**Topic Last Modified:** 2012-10-17_</span></span>

<span data-ttu-id="ff3da-106">各レコードには、音声通話中の1つのエンドポイントのクライアントイベントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ff3da-106">Each record contains a client event for one endpoint in an audio call.</span></span> <span data-ttu-id="ff3da-107">通常、1つの通話には2つのレコードがあります。1つは呼び出し元用、もう1つは呼び出し先用です。</span><span class="sxs-lookup"><span data-stu-id="ff3da-107">Usually, one call has two records, one for caller and one for callee.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ff3da-108"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="ff3da-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="ff3da-109"><strong>データ型</strong></span><span class="sxs-lookup"><span data-stu-id="ff3da-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="ff3da-110"><strong>キー/インデックス</strong></span><span class="sxs-lookup"><span data-stu-id="ff3da-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="ff3da-111"><strong>詳細</strong></span><span class="sxs-lookup"><span data-stu-id="ff3da-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ff3da-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="ff3da-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="ff3da-113">datetime</span><span class="sxs-lookup"><span data-stu-id="ff3da-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="ff3da-114">Primary</span><span class="sxs-lookup"><span data-stu-id="ff3da-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="ff3da-115"><a href="lync-server-2013-medialine-table.md">Lync Server 2013 の MediaLine テーブル</a>から参照されている。</span><span class="sxs-lookup"><span data-stu-id="ff3da-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff3da-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="ff3da-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="ff3da-117">int</span><span class="sxs-lookup"><span data-stu-id="ff3da-117">int</span></span></p></td>
<td><p><span data-ttu-id="ff3da-118">Primary</span><span class="sxs-lookup"><span data-stu-id="ff3da-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="ff3da-119"><a href="lync-server-2013-medialine-table.md">Lync Server 2013 の MediaLine テーブル</a>から参照されている。</span><span class="sxs-lookup"><span data-stu-id="ff3da-119">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff3da-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="ff3da-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="ff3da-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="ff3da-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="ff3da-122">Primary</span><span class="sxs-lookup"><span data-stu-id="ff3da-122">Primary</span></span></p></td>
<td><p><span data-ttu-id="ff3da-123"><a href="lync-server-2013-medialine-table.md">Lync Server 2013 の MediaLine テーブル</a>から参照されている。</span><span class="sxs-lookup"><span data-stu-id="ff3da-123">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff3da-124"><strong>FromCaller</strong></span><span class="sxs-lookup"><span data-stu-id="ff3da-124"><strong>FromCaller</strong></span></span></p></td>
<td><p><span data-ttu-id="ff3da-125">bit</span><span class="sxs-lookup"><span data-stu-id="ff3da-125">bit</span></span></p></td>
<td><p><span data-ttu-id="ff3da-126">Primary</span><span class="sxs-lookup"><span data-stu-id="ff3da-126">Primary</span></span></p></td>
<td><p><span data-ttu-id="ff3da-127">0: 呼び出し先のデータ</span><span class="sxs-lookup"><span data-stu-id="ff3da-127">0: Callee’s data</span></span></p>
<p><span data-ttu-id="ff3da-128">1: 発信者のデータ</span><span class="sxs-lookup"><span data-stu-id="ff3da-128">1: Caller’s data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff3da-129"><strong>NetworkSendQualityEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="ff3da-129"><strong>NetworkSendQualityEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="ff3da-130">10進数 (5, 2)</span><span class="sxs-lookup"><span data-stu-id="ff3da-130">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ff3da-131">セッションのパーセンテージ NetworkSendQuality イベントが ' Bad ' 状態に対して発生しました。</span><span class="sxs-lookup"><span data-stu-id="ff3da-131">Percentage of session the NetworkSendQuality event was fired for ‘Bad’ state.</span></span></p>
<p><span data-ttu-id="ff3da-132">ネットワーク品質は、ジッタまたはパケット損失の観点から、送信された音声の品質に重大な影響を与えることがあります。</span><span class="sxs-lookup"><span data-stu-id="ff3da-132">Network quality in terms of jitter or packet loss is severe and impacting the quality of audio being sent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff3da-133"><strong>NetworkReceiveQualityEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="ff3da-133"><strong>NetworkReceiveQualityEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="ff3da-134">10進数 (5, 2)</span><span class="sxs-lookup"><span data-stu-id="ff3da-134">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ff3da-135">セッションのパーセンテージ ReceiveSendQuality イベントが ' Bad ' 状態で発生しました。</span><span class="sxs-lookup"><span data-stu-id="ff3da-135">Percentage of session the ReceiveSendQuality event was fired for ‘Bad’ state.</span></span></p>
<p><span data-ttu-id="ff3da-136">ネットワーク品質は、ジッタまたはパケット損失の観点から、受信中のオーディオの品質に深刻な影響を与えることができます。</span><span class="sxs-lookup"><span data-stu-id="ff3da-136">Network quality in terms of jitter or packet loss is severe and impacting the quality of audio being received.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff3da-137"><strong>NetworkDelayEventRatio スペック</strong></span><span class="sxs-lookup"><span data-stu-id="ff3da-137"><strong>NetworkDelayEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="ff3da-138">10進数 (5, 2)</span><span class="sxs-lookup"><span data-stu-id="ff3da-138">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ff3da-139">セッションのパーセンテージ "Bad" 状態に対して Delay イベントが発生しました。</span><span class="sxs-lookup"><span data-stu-id="ff3da-139">Percentage of session the Delay event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="ff3da-140">ネットワーク待ち時間が重大であり、対話的なコミュニケーションを防ぐことで、エクスペリエンスに影響を与える</span><span class="sxs-lookup"><span data-stu-id="ff3da-140">Network latency is severe and impacting the experience by preventing interactive communication</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff3da-141"><strong>NetworkBandwidthLowEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="ff3da-141"><strong>NetworkBandwidthLowEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="ff3da-142">10進数 (5, 2)</span><span class="sxs-lookup"><span data-stu-id="ff3da-142">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ff3da-143">セッションのパーセンテージ低帯域幅イベントが ' Bad ' 状態に対して発生しました。</span><span class="sxs-lookup"><span data-stu-id="ff3da-143">Percentage of session the LowBandwidth event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="ff3da-144">利用可能な音声エクスペリエンスを実現するには、利用可能な帯域幅が不足しています。</span><span class="sxs-lookup"><span data-stu-id="ff3da-144">The available bandwidth is insufficient for an acceptable voice experience.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff3da-145"><strong>CPUInsufficientEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="ff3da-145"><strong>CPUInsufficientEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="ff3da-146">10進数 (5, 2)</span><span class="sxs-lookup"><span data-stu-id="ff3da-146">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ff3da-147">セッションの割合。不適切な CPU イベントが ' Bad ' 状態に対して発生しました。</span><span class="sxs-lookup"><span data-stu-id="ff3da-147">Percentage of session the insufficient CPU event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="ff3da-148">現在使用中のモダリティとアプリケーションで処理するための CPU サイクルが十分にありません。</span><span class="sxs-lookup"><span data-stu-id="ff3da-148">There are insufficient CPU cycles for processing with the current modalities and applications in use.</span></span> <span data-ttu-id="ff3da-149">これにより、オーディオチャンネルでひずみが発生します。</span><span class="sxs-lookup"><span data-stu-id="ff3da-149">This causes distortions with the audio channel.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff3da-150"><strong>DeviceHalfDuplexAECEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="ff3da-150"><strong>DeviceHalfDuplexAECEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="ff3da-151">10進数 (5, 2)</span><span class="sxs-lookup"><span data-stu-id="ff3da-151">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ff3da-152">セッションのパーセンテージ DeviceHalfDuplexAEC イベントが ' Bad ' 状態で発生しました。</span><span class="sxs-lookup"><span data-stu-id="ff3da-152">Percentage of session the DeviceHalfDuplexAEC event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="ff3da-153">エコーを防ぐために、システムは半二重モードに設定されています。</span><span class="sxs-lookup"><span data-stu-id="ff3da-153">In order to prevent echo, the system has enter half duplex.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff3da-154"><strong>DeviceRenderNotFunctioningEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="ff3da-154"><strong>DeviceRenderNotFunctioningEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="ff3da-155">10進数 (5, 2)</span><span class="sxs-lookup"><span data-stu-id="ff3da-155">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ff3da-156">セッションの割合 DeviceRenderNotFunctioning イベントが ' Bad ' 状態に対して発生しました。</span><span class="sxs-lookup"><span data-stu-id="ff3da-156">Percentage of session the DeviceRenderNotFunctioning event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="ff3da-157">現在セッションで使用されているレンダーデバイスが正常に機能していません。</span><span class="sxs-lookup"><span data-stu-id="ff3da-157">The render device currently being used for the session is not functioning correctly.</span></span> <span data-ttu-id="ff3da-158">これにより、1方向の音声の問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ff3da-158">This can cause one-way audio issues.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff3da-159"><strong>DeviceCaptureNotFunctioningEventRatio 使い方</strong></span><span class="sxs-lookup"><span data-stu-id="ff3da-159"><strong>DeviceCaptureNotFunctioningEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="ff3da-160">10進数 (5, 2)</span><span class="sxs-lookup"><span data-stu-id="ff3da-160">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ff3da-161">セッションのパーセンテージ DeviceCaptureNotFunctioning イベントが ' Bad ' 状態に対して発生しました。</span><span class="sxs-lookup"><span data-stu-id="ff3da-161">Percentage of session the DeviceCaptureNotFunctioning event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="ff3da-162">現在セッションで使用されているキャプチャデバイスが正常に機能していません。</span><span class="sxs-lookup"><span data-stu-id="ff3da-162">The capture device currently being used for the session is not functioning correctly.</span></span> <span data-ttu-id="ff3da-163">これにより、1方向の音声の問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ff3da-163">This can cause one-way audio issues.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff3da-164"><strong>DeviceGlitchesEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="ff3da-164"><strong>DeviceGlitchesEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="ff3da-165">10進数 (5, 2)</span><span class="sxs-lookup"><span data-stu-id="ff3da-165">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ff3da-166">セッションの割合 DeviceGlitches イベントが ' Bad ' 状態で発生しました。</span><span class="sxs-lookup"><span data-stu-id="ff3da-166">Percentage of session the DeviceGlitches event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="ff3da-167">オーディオのレンダリングで、ひずみの原因となる重大な問題が発生します。</span><span class="sxs-lookup"><span data-stu-id="ff3da-167">There are severe glitches in the rendering of audio which is causing distortions.</span></span> <span data-ttu-id="ff3da-168">これらのエラーは、ドライバーの問題、遅延プロシージャ呼び出し (DPC) ストーム (ドライバー)、および CPU 使用率が高くなることが原因で発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ff3da-168">These glitches can be caused by driver issues, deferred procedure calls (DPC) storm (drivers), and high CPU usage.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff3da-169"><strong>DeviceLowSNREventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="ff3da-169"><strong>DeviceLowSNREventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="ff3da-170">10進数 (5, 2)</span><span class="sxs-lookup"><span data-stu-id="ff3da-170">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ff3da-171">セッションのパーセンテージ DeviceLowSNR イベントが ' Bad ' 状態に対して発生しました。</span><span class="sxs-lookup"><span data-stu-id="ff3da-171">Percentage of session the DeviceLowSNR event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="ff3da-172">キャプチャ品質は非常に低い。雑音が多いか、ユーザがマイクから離れすぎている。</span><span class="sxs-lookup"><span data-stu-id="ff3da-172">The capture quality is very poor, either very noisy or user is talking too far away from the microphone.</span></span> <span data-ttu-id="ff3da-173">これにより、ひずみが発生します。</span><span class="sxs-lookup"><span data-stu-id="ff3da-173">This will cause distortions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff3da-174"><strong>DeviceLowSpeechLevelEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="ff3da-174"><strong>DeviceLowSpeechLevelEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="ff3da-175">10進数 (5, 2)</span><span class="sxs-lookup"><span data-stu-id="ff3da-175">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ff3da-176">セッションのパーセンテージ DeviceLowSpeechLevel イベントが ' Bad ' 状態で発生しました。</span><span class="sxs-lookup"><span data-stu-id="ff3da-176">Percentage of session the DeviceLowSpeechLevel event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="ff3da-177">ユーザーの音声レベルが低すぎて、システムがそれ以上の機能を向上させることができない。</span><span class="sxs-lookup"><span data-stu-id="ff3da-177">User‘s speech level is too low and the system cannot increase it any further.</span></span> <span data-ttu-id="ff3da-178">これにより、ひずみが発生したり、一方向のオーディオとして認識されるようになります。</span><span class="sxs-lookup"><span data-stu-id="ff3da-178">This can either cause distortions or perceived as one-way audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff3da-179"><strong>DeviceClippingEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="ff3da-179"><strong>DeviceClippingEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="ff3da-180">10進数 (5, 2)</span><span class="sxs-lookup"><span data-stu-id="ff3da-180">Decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ff3da-181">セッションのパーセンテージ DeviceClipping イベントが ' Bad ' 状態で発生しました。</span><span class="sxs-lookup"><span data-stu-id="ff3da-181">Percentage of session the DeviceClipping event was fired for ‘Bad’ state.</span></span></p>
<p><span data-ttu-id="ff3da-182">ニアエンドの音声によってマイクがクリップされる場合は、クリッピングによるひずみが発生します。</span><span class="sxs-lookup"><span data-stu-id="ff3da-182">When near-end speech clips the microphone, far-end hears distortion due to clipping.</span></span> <span data-ttu-id="ff3da-183">ニアエンドマイクのクリッピングを回避することが重要です。</span><span class="sxs-lookup"><span data-stu-id="ff3da-183">It is important to avoid near-end microphone clipping.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff3da-184"><strong>DeviceEchoEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="ff3da-184"><strong>DeviceEchoEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="ff3da-185">10進数 (5, 2)</span><span class="sxs-lookup"><span data-stu-id="ff3da-185">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ff3da-186">セッションのパーセンテージ DeviceEchoEvent イベントが ' Bad ' 状態で発生しました。</span><span class="sxs-lookup"><span data-stu-id="ff3da-186">Percentage of session the DeviceEchoEvent event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="ff3da-187">デバイスまたはセットアップが原因で、システムの補正機能を超えたエコーが発生しています。</span><span class="sxs-lookup"><span data-stu-id="ff3da-187">Device or setup is causing echo beyond the ability of the system to compensate.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff3da-188"><strong>デバイスの Devicorています。</strong></span><span class="sxs-lookup"><span data-stu-id="ff3da-188"><strong>DeviceNearEndToEchoRatioEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="ff3da-189">10進数 (5, 2)</span><span class="sxs-lookup"><span data-stu-id="ff3da-189">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ff3da-190">セッションのパーセンテージ Devicenなイベントが ' Bad ' 状態で発生しました。</span><span class="sxs-lookup"><span data-stu-id="ff3da-190">Percentage of session the DeviceNearEndToEchoRatio event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="ff3da-191">ユーザーの音声が、ユーザーの中断を簡単にすることができるようになるため、キャプチャされたエコーと比較して、ユーザーエクスペリエンスに影響を与えることができます。</span><span class="sxs-lookup"><span data-stu-id="ff3da-191">The user’s speech is too low compared to the echo being captured which impacts the users experience because it limits how easy it is to interrupt a user.</span></span> <span data-ttu-id="ff3da-192">スピーカーの音量を下げて、マイクをトーカーに近づける。</span><span class="sxs-lookup"><span data-stu-id="ff3da-192">Reduce speaker volume, move the microphone closer to the talker.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff3da-193"><strong>DeviceMultipleEndpointsEventCount</strong></span><span class="sxs-lookup"><span data-stu-id="ff3da-193"><strong>DeviceMultipleEndpointsEventCount</strong></span></span></p></td>
<td><p><span data-ttu-id="ff3da-194">int</span><span class="sxs-lookup"><span data-stu-id="ff3da-194">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ff3da-195">セッション中に ' Bad ' 状態に対して DeviceMultipleEndpoints イベントが発生した回数。</span><span class="sxs-lookup"><span data-stu-id="ff3da-195">Number of times during session the DeviceMultipleEndpoints event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="ff3da-196">同じセッション内の複数のオーディオエンドポイントが検出され、レンダーボリュームが減ることで、システムが補正しています。</span><span class="sxs-lookup"><span data-stu-id="ff3da-196">Multiple audio endpoints in the same session detected and the system has compensated by reducing render volume.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff3da-197"><strong>Deviceskのイベントカウント</strong></span><span class="sxs-lookup"><span data-stu-id="ff3da-197"><strong>DeviceHowlingEventCount</strong></span></span></p></td>
<td><p><span data-ttu-id="ff3da-198">int</span><span class="sxs-lookup"><span data-stu-id="ff3da-198">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ff3da-199">セッション中に、' Bad ' 状態に対して Deviceなイベントイベントが発生した回数。</span><span class="sxs-lookup"><span data-stu-id="ff3da-199">Number of times during session the DeviceHowlingEvent event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="ff3da-200">音声フィードバックループが検出されました (複数のエンドポイントでのオーディオパスの共有によって発生)。</span><span class="sxs-lookup"><span data-stu-id="ff3da-200">Audio feedback loop detected (caused by multiple endpoints sharing audio path).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff3da-201"><strong>Devicerendervolumevolumeeventr</strong></span><span class="sxs-lookup"><span data-stu-id="ff3da-201"><strong>DeviceRenderZeroVolumeEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="ff3da-202">10進数 (5, 2)</span><span class="sxs-lookup"><span data-stu-id="ff3da-202">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ff3da-203">セッションのパーセンテージ Devicerenderゼロボリュームイベントが "Bad" 状態になったときに発生しました。</span><span class="sxs-lookup"><span data-stu-id="ff3da-203">Percentage of session the DeviceRenderZeroVolume event was fired for being in the “Bad’ state.</span></span> <span data-ttu-id="ff3da-204">レンダーデバイスがボリューム0に設定されています。</span><span class="sxs-lookup"><span data-stu-id="ff3da-204">The render device was set to zero volume.</span></span></p>
<p><span data-ttu-id="ff3da-205">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ff3da-205">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff3da-206"><strong>Devicerendermuteeventr</strong></span><span class="sxs-lookup"><span data-stu-id="ff3da-206"><strong>DeviceRenderMuteEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="ff3da-207">10進数 (5, 2)</span><span class="sxs-lookup"><span data-stu-id="ff3da-207">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ff3da-208">セッションのパーセンテージ DeviceRenderMute イベントが "Bad" 状態になったときに発生しました。</span><span class="sxs-lookup"><span data-stu-id="ff3da-208">Percentage of session the DeviceRenderMute event was fired for being in the “Bad’ state.</span></span> <span data-ttu-id="ff3da-209">レンダーデバイスがミュートにされました。</span><span class="sxs-lookup"><span data-stu-id="ff3da-209">The render device was muted.</span></span></p>
<p><span data-ttu-id="ff3da-210">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ff3da-210">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="ff3da-211">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ff3da-211">


</div>

<span> </span>

</div>

</div>

</span></span></div>

