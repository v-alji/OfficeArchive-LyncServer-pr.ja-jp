---
title: 'Lync Server 2013: AudioSignal テーブル'
description: 'Lync Server 2013: AudioSignal テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AudioSignal table
ms:assetid: 0013c8c6-cdf9-4d70-bc2a-cddd1560f66b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398064(v=OCS.15)
ms:contentKeyID: 48183217
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 82f3b3119eaccfe56c4706cff07469bc3434461f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438207"
---
# <a name="audiosignal-table-in-lync-server-2013"></a><span data-ttu-id="31731-103">Lync Server 2013 の AudioSignal テーブル</span><span class="sxs-lookup"><span data-stu-id="31731-103">AudioSignal table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="31731-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="31731-104">

<span> </span></span></span>

<span data-ttu-id="31731-105">_**最終更新日:** 2013-11-12_</span><span class="sxs-lookup"><span data-stu-id="31731-105">_**Topic Last Modified:** 2013-11-12_</span></span>

<span data-ttu-id="31731-106">各レコードは、1つのエンドポイントの音声シグナルメトリックを表します。</span><span class="sxs-lookup"><span data-stu-id="31731-106">Each record represents audio signal metrics for one endpoint.</span></span> <span data-ttu-id="31731-107">通常、各通話には2つのレコードがあります。1つは呼び出し元用、もう1つは呼び出し先用です。</span><span class="sxs-lookup"><span data-stu-id="31731-107">Usually, each call has two records, one is for caller, and one is for callee.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="31731-108"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="31731-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="31731-109"><strong>データ型</strong></span><span class="sxs-lookup"><span data-stu-id="31731-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="31731-110"><strong>キー/インデックス</strong></span><span class="sxs-lookup"><span data-stu-id="31731-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="31731-111"><strong>詳細</strong></span><span class="sxs-lookup"><span data-stu-id="31731-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="31731-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="31731-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="31731-113">datetime</span><span class="sxs-lookup"><span data-stu-id="31731-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="31731-114">Primary</span><span class="sxs-lookup"><span data-stu-id="31731-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="31731-115"><a href="lync-server-2013-medialine-table.md">Lync Server 2013 の MediaLine テーブル</a>から参照されている。</span><span class="sxs-lookup"><span data-stu-id="31731-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31731-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="31731-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="31731-117">int</span><span class="sxs-lookup"><span data-stu-id="31731-117">int</span></span></p></td>
<td><p><span data-ttu-id="31731-118">Primary</span><span class="sxs-lookup"><span data-stu-id="31731-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="31731-119"><a href="lync-server-2013-medialine-table.md">Lync Server 2013 の MediaLine テーブル</a>から参照されている。</span><span class="sxs-lookup"><span data-stu-id="31731-119">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31731-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="31731-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="31731-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="31731-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="31731-122">Primary</span><span class="sxs-lookup"><span data-stu-id="31731-122">Primary</span></span></p></td>
<td><p><span data-ttu-id="31731-123"><a href="lync-server-2013-medialine-table.md">Lync Server 2013 の MediaLine テーブル</a>から参照されている。</span><span class="sxs-lookup"><span data-stu-id="31731-123">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31731-124"><strong>FromCaller</strong></span><span class="sxs-lookup"><span data-stu-id="31731-124"><strong>FromCaller</strong></span></span></p></td>
<td><p><span data-ttu-id="31731-125">bit</span><span class="sxs-lookup"><span data-stu-id="31731-125">bit</span></span></p></td>
<td><p><span data-ttu-id="31731-126">Primary</span><span class="sxs-lookup"><span data-stu-id="31731-126">Primary</span></span></p></td>
<td><p><span data-ttu-id="31731-127">0: 呼び出し先のデータ</span><span class="sxs-lookup"><span data-stu-id="31731-127">0: Callee’s data</span></span></p>
<p><span data-ttu-id="31731-128">1: 発信者のデータ</span><span class="sxs-lookup"><span data-stu-id="31731-128">1: Caller’s data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31731-129"><strong>SendSignalLevel</strong></span><span class="sxs-lookup"><span data-stu-id="31731-129"><strong>SendSignalLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="31731-130">int</span><span class="sxs-lookup"><span data-stu-id="31731-130">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="31731-131">アナログ高のゲイン制御オーディオ信号レベルを表します。</span><span class="sxs-lookup"><span data-stu-id="31731-131">Represents the Post-Analog Gain Control audio signal level.</span></span> <span data-ttu-id="31731-132">このメトリックの単位は dBmo です。</span><span class="sxs-lookup"><span data-stu-id="31731-132">The unit for this metric is dBmo.</span></span> <span data-ttu-id="31731-133">許容可能な品質を求めるには、少なくとも30個の dBmo を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="31731-133">For acceptable quality, it should be at least 30 dBmo.</span></span> <span data-ttu-id="31731-134">このメトリックは、A/V 会議サーバーまたは IP 携帯電話によって報告されることはありません。</span><span class="sxs-lookup"><span data-stu-id="31731-134">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31731-135"><strong>RecvSignalLevel</strong></span><span class="sxs-lookup"><span data-stu-id="31731-135"><strong>RecvSignalLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="31731-136">int</span><span class="sxs-lookup"><span data-stu-id="31731-136">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="31731-137">「SendSignalLevel」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="31731-137">See SendSignalLevel.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31731-138"><strong>SendNoiseLevel</strong></span><span class="sxs-lookup"><span data-stu-id="31731-138"><strong>SendNoiseLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="31731-139">int</span><span class="sxs-lookup"><span data-stu-id="31731-139">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="31731-140">アナログのゲイン制御オーディオノイズレベルを表します。</span><span class="sxs-lookup"><span data-stu-id="31731-140">Represents the Post-Analog Gain Control audio noise level.</span></span> <span data-ttu-id="31731-141">このメトリックの単位は dBmo です。</span><span class="sxs-lookup"><span data-stu-id="31731-141">The unit for this metric is dBmo.</span></span> <span data-ttu-id="31731-142">許容される品質には、35 dBmo よりも小さい値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="31731-142">For acceptable quality, it should be less than 35 dBmo.</span></span> <span data-ttu-id="31731-143">このメトリックは、A/V 会議サーバーまたは IP 携帯電話によって報告されることはありません。</span><span class="sxs-lookup"><span data-stu-id="31731-143">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31731-144"><strong>RecvNoiseLevel</strong></span><span class="sxs-lookup"><span data-stu-id="31731-144"><strong>RecvNoiseLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="31731-145">int</span><span class="sxs-lookup"><span data-stu-id="31731-145">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="31731-146">「SendNoiseLevel」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="31731-146">See SendNoiseLevel.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31731-147"><strong>EchoReturn</strong></span><span class="sxs-lookup"><span data-stu-id="31731-147"><strong>EchoReturn</strong></span></span></p></td>
<td><p><span data-ttu-id="31731-148">int</span><span class="sxs-lookup"><span data-stu-id="31731-148">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="31731-149">エコーリターンロスの拡張メトリック。</span><span class="sxs-lookup"><span data-stu-id="31731-149">Echo Return Loss Enhancement metric.</span></span> <span data-ttu-id="31731-150">このメトリックの単位は dB です。</span><span class="sxs-lookup"><span data-stu-id="31731-150">The unit for this metric is dB.</span></span> <span data-ttu-id="31731-151">小さい値は、エコーが少なくなります。</span><span class="sxs-lookup"><span data-stu-id="31731-151">Lower values represent less echo.</span></span> <span data-ttu-id="31731-152">このメトリックは、A/V 会議サーバーまたは IP 携帯電話によって報告されることはありません。</span><span class="sxs-lookup"><span data-stu-id="31731-152">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31731-153"><strong>AudioSpeakerGlitchRate</strong></span><span class="sxs-lookup"><span data-stu-id="31731-153"><strong>AudioSpeakerGlitchRate</strong></span></span></p></td>
<td><p><span data-ttu-id="31731-154">int</span><span class="sxs-lookup"><span data-stu-id="31731-154">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="31731-155">スピーカーレンダリングに対する5分あたりの平均エラー。</span><span class="sxs-lookup"><span data-stu-id="31731-155">Average glitches per five minutes for the loudspeaker rendering.</span></span> <span data-ttu-id="31731-156">品質を向上させるには、5分未満でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="31731-156">For good quality, this should be less than one per five minutes.</span></span> <span data-ttu-id="31731-157">A/V 会議サーバー、仲介サーバー、または IP 電話によって報告されていません。</span><span class="sxs-lookup"><span data-stu-id="31731-157">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31731-158"><strong>AudioMicGlitchRate</strong></span><span class="sxs-lookup"><span data-stu-id="31731-158"><strong>AudioMicGlitchRate</strong></span></span></p></td>
<td><p><span data-ttu-id="31731-159">int</span><span class="sxs-lookup"><span data-stu-id="31731-159">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="31731-160">マイクをキャプチャするための5分あたりの平均エラー。</span><span class="sxs-lookup"><span data-stu-id="31731-160">Average glitches per five minutes for the microphone capture.</span></span> <span data-ttu-id="31731-161">品質を向上させるには、5分未満の値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="31731-161">For good quality this should be less than one per five minutes.</span></span> <span data-ttu-id="31731-162">A/V 会議サーバー、仲介サーバー、または IP 電話によって報告されていません。</span><span class="sxs-lookup"><span data-stu-id="31731-162">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31731-163"><strong>AudioTimestampDriftRateMic</strong></span><span class="sxs-lookup"><span data-stu-id="31731-163"><strong>AudioTimestampDriftRateMic</strong></span></span></p></td>
<td><p><span data-ttu-id="31731-164">10進数 (9, 2)</span><span class="sxs-lookup"><span data-stu-id="31731-164">decimal(9,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="31731-165">CPU クロックを基準としたマイクデバイスクロックドリフトレート。</span><span class="sxs-lookup"><span data-stu-id="31731-165">Microphone device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31731-166"><strong>AudioTimestampDriftRateSpk</strong></span><span class="sxs-lookup"><span data-stu-id="31731-166"><strong>AudioTimestampDriftRateSpk</strong></span></span></p></td>
<td><p><span data-ttu-id="31731-167">10進数 (9, 2)</span><span class="sxs-lookup"><span data-stu-id="31731-167">decimal(9,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="31731-168">CPU クロックを基準としたスピーカーデバイスクロックドリフトレート。</span><span class="sxs-lookup"><span data-stu-id="31731-168">Speaker device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31731-169"><strong>AudioTimestampErrorMicMs</strong></span><span class="sxs-lookup"><span data-stu-id="31731-169"><strong>AudioTimestampErrorMicMs</strong></span></span></p></td>
<td><p><span data-ttu-id="31731-170">10進数 (9, 2)</span><span class="sxs-lookup"><span data-stu-id="31731-170">decimal(9,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="31731-171">CPU クロックを基準としたスピーカーデバイスクロックドリフトレート。</span><span class="sxs-lookup"><span data-stu-id="31731-171">Speaker device clock drift rate, relative to CPU clock.</span></span></p>
<p><span data-ttu-id="31731-172">平均マイクキャプチャストリームタイムスタンプエラー (ミリ秒単位)、通話の最後の20秒。</span><span class="sxs-lookup"><span data-stu-id="31731-172">Average microphone capture stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31731-173"><strong>AudioTimestampErrorSpkMs</strong></span><span class="sxs-lookup"><span data-stu-id="31731-173"><strong>AudioTimestampErrorSpkMs</strong></span></span></p></td>
<td><p><span data-ttu-id="31731-174">10進数 (9, 2)</span><span class="sxs-lookup"><span data-stu-id="31731-174">decimal(9,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="31731-175">通話の最後の20秒間の平均スピーカーレンダーストリームタイムスタンプエラー (ミリ秒単位)。</span><span class="sxs-lookup"><span data-stu-id="31731-175">Average speaker render stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31731-176"><strong>VsEntryCauses 原因</strong></span><span class="sxs-lookup"><span data-stu-id="31731-176"><strong>VsEntryCauses</strong></span></span></p></td>
<td><p><span data-ttu-id="31731-177">smallint</span><span class="sxs-lookup"><span data-stu-id="31731-177">smallint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="31731-178">音声スイッチは半二重モードで、中断機能が低減されます。</span><span class="sxs-lookup"><span data-stu-id="31731-178">Voice switch is a half-duplex mode with reduced interruption ability.</span></span> <span data-ttu-id="31731-179">音声スイッチの入力の原因:</span><span class="sxs-lookup"><span data-stu-id="31731-179">Causes of voice switch entry:</span></span></p>
<p><span data-ttu-id="31731-180">ENTER_VS_BADTS 0x01</span><span class="sxs-lookup"><span data-stu-id="31731-180">ENTER_VS_BADTS 0x01</span></span></p>
<p><span data-ttu-id="31731-181">ENTER_VS_ECHO 0x02</span><span class="sxs-lookup"><span data-stu-id="31731-181">ENTER_VS_ECHO 0x02</span></span></p>
<p><span data-ttu-id="31731-182">ENTER_VS_FORCEORCONVERGENCE 0x04</span><span class="sxs-lookup"><span data-stu-id="31731-182">ENTER_VS_FORCEORCONVERGENCE 0x04</span></span></p>
<p><span data-ttu-id="31731-183">ENTER_VS_DNLP 0x08</span><span class="sxs-lookup"><span data-stu-id="31731-183">ENTER_VS_DNLP 0x08</span></span></p>
<p><span data-ttu-id="31731-184">原因として、このような個々の原因が考えられます。</span><span class="sxs-lookup"><span data-stu-id="31731-184">The cause can be a combination of those individual causes.</span></span> <span data-ttu-id="31731-185">ENTER_VS_FORCEORCONVERGENCE を有効にするには、regkey をテスト目的として使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="31731-185">ENTER_VS_FORCEORCONVERGENCE can only be enabled by regkey for test purpose.</span></span></p>
<p><span data-ttu-id="31731-186">この列のデータ型は、Microsoft Lync Server 2013 で変更されました。</span><span class="sxs-lookup"><span data-stu-id="31731-186">The data type for this column was changed in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31731-187"><strong>EchoEventCauses</strong></span><span class="sxs-lookup"><span data-stu-id="31731-187"><strong>EchoEventCauses</strong></span></span></p></td>
<td><p><span data-ttu-id="31731-188">tinyint</span><span class="sxs-lookup"><span data-stu-id="31731-188">tinyint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="31731-189">エコーイベントの原因:</span><span class="sxs-lookup"><span data-stu-id="31731-189">Causes of an echo event:</span></span></p>
<p><span data-ttu-id="31731-190">ECHO_EVENT_BAD_TIMESTAMP 0x01</span><span class="sxs-lookup"><span data-stu-id="31731-190">ECHO_EVENT_BAD_TIMESTAMP 0x01</span></span></p>
<p><span data-ttu-id="31731-191">ECHO_EVENT_POSTAEC_ECHO 0x02</span><span class="sxs-lookup"><span data-stu-id="31731-191">ECHO_EVENT_POSTAEC_ECHO 0x02</span></span></p>
<p><span data-ttu-id="31731-192">ECHO_EVENT_ANLP 0x04</span><span class="sxs-lookup"><span data-stu-id="31731-192">ECHO_EVENT_ANLP 0x04</span></span></p>
<p><span data-ttu-id="31731-193">ECHO_EVENT_DNLP 0x08</span><span class="sxs-lookup"><span data-stu-id="31731-193">ECHO_EVENT_DNLP 0x08</span></span></p>
<p><span data-ttu-id="31731-194">ECHO_EVENT_MIC_CLIPPING 0x10</span><span class="sxs-lookup"><span data-stu-id="31731-194">ECHO_EVENT_MIC_CLIPPING 0x10</span></span></p>
<p><span data-ttu-id="31731-195">ECHO_EVENT_BAD_STATE 0x20</span><span class="sxs-lookup"><span data-stu-id="31731-195">ECHO_EVENT_BAD_STATE 0x20</span></span></p>
<p><span data-ttu-id="31731-196">原因として、このような個々の原因が考えられます。</span><span class="sxs-lookup"><span data-stu-id="31731-196">The cause can be a combination of those individual causes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31731-197"><strong>EchoPercentMicIn</strong></span><span class="sxs-lookup"><span data-stu-id="31731-197"><strong>EchoPercentMicIn</strong></span></span></p></td>
<td><p><span data-ttu-id="31731-198">10進数 (5, 2)</span><span class="sxs-lookup"><span data-stu-id="31731-198">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="31731-199">マイクのキャプチャストリームでエコーが検出された時間の割合。</span><span class="sxs-lookup"><span data-stu-id="31731-199">Percentage of time when echo was detected in the microphone capture stream.</span></span> <span data-ttu-id="31731-200">一般的に、ヘッドセットまたはハンドセットの値は低く、スピーカーフォンやスタンドアロンスピーカーでは高くなります。</span><span class="sxs-lookup"><span data-stu-id="31731-200">Typically, values are low for headsets or handsets, and higher for speaker phones or stand-alone speakers.</span></span> <span data-ttu-id="31731-201">オンボード音響エコーキャンセルをサポートしているデバイスでは、高値を指定するとエコーリークが発生します。</span><span class="sxs-lookup"><span data-stu-id="31731-201">For devices that support on-board acoustic echo cancellation, high values indicate echo leak.</span></span> <span data-ttu-id="31731-202">その他のデバイスでは、デバイスの品質を評価するためにこのメトリックを使用しないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="31731-202">For other devices, this metric should not be used to evaluate device quality.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31731-203"><strong>EchoPercentSend</strong></span><span class="sxs-lookup"><span data-stu-id="31731-203"><strong>EchoPercentSend</strong></span></span></p></td>
<td><p><span data-ttu-id="31731-204">10進数 (5, 2)</span><span class="sxs-lookup"><span data-stu-id="31731-204">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="31731-205">送信ストリームでエコーが検出された時間のパーセンテージ。</span><span class="sxs-lookup"><span data-stu-id="31731-205">Percentage of time when echo is detected in sent stream.</span></span> <span data-ttu-id="31731-206">送信ストリームでのエコー率が高いと、エコーが発生したことを示します。</span><span class="sxs-lookup"><span data-stu-id="31731-206">High echo percentage in send streams an indication of echo leak.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31731-207"><strong>RxAGCSignalLevel</strong></span><span class="sxs-lookup"><span data-stu-id="31731-207"><strong>RxAGCSignalLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="31731-208">int</span><span class="sxs-lookup"><span data-stu-id="31731-208">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="31731-209">ゲートウェイからの仲介サーバー上の受信したシグナルレベル。これは、仲介サーバーにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="31731-209">Received signal level on the Mediation Server from the Gateway; this applies only to the Mediation Server.</span></span> <span data-ttu-id="31731-210">このメトリックの単位は dBoV です。</span><span class="sxs-lookup"><span data-stu-id="31731-210">The unit of this metric is dBoV.</span></span> <span data-ttu-id="31731-211">品質を向上させるには、許容範囲は [-30 ~-18] の dBoV にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="31731-211">For good quality, the acceptable range should be [-30 to -18] dBoV.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31731-212"><strong>RxAGCNoiseLevel</strong></span><span class="sxs-lookup"><span data-stu-id="31731-212"><strong>RxAGCNoiseLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="31731-213">int</span><span class="sxs-lookup"><span data-stu-id="31731-213">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="31731-214">ゲートウェイからの仲介サーバーで受信したシグナルレベル。</span><span class="sxs-lookup"><span data-stu-id="31731-214">Received signal level on the Mediation Server from the Gateway.</span></span> <span data-ttu-id="31731-215">これは、仲介サーバーにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="31731-215">This applies only to the Mediation Server.</span></span> <span data-ttu-id="31731-216">このメトリックの単位は dBoV です。</span><span class="sxs-lookup"><span data-stu-id="31731-216">The unit of this metric is dBoV.</span></span> <span data-ttu-id="31731-217">品質を向上させるには、許容範囲として 50 dBoV 未満の値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="31731-217">For good quality, the acceptable range should be less than -50 dBoV.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31731-218"><strong>RxAvgAGCGain</strong></span><span class="sxs-lookup"><span data-stu-id="31731-218"><strong>RxAvgAGCGain</strong></span></span></p></td>
<td><p><span data-ttu-id="31731-219">int</span><span class="sxs-lookup"><span data-stu-id="31731-219">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="31731-220">仲介サーバー側の自動ゲイン制御 (AGC)。</span><span class="sxs-lookup"><span data-stu-id="31731-220">Automatic gain control (AGC) on the Mediation Server side.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31731-221"><strong>InitialSignalLevelRMS</strong></span><span class="sxs-lookup"><span data-stu-id="31731-221"><strong>InitialSignalLevelRMS</strong></span></span></p></td>
<td><p><span data-ttu-id="31731-222">float</span><span class="sxs-lookup"><span data-stu-id="31731-222">float</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="31731-223">通話の最初の30秒以内の着信シグナルのルート平均平方根 (RMS)。</span><span class="sxs-lookup"><span data-stu-id="31731-223">The root mean square (RMS) of the incoming signal of up to the first 30 seconds of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31731-224"><strong>RecvSignalLevelCh1</strong></span><span class="sxs-lookup"><span data-stu-id="31731-224"><strong>RecvSignalLevelCh1</strong></span></span></p></td>
<td><p><span data-ttu-id="31731-225">int</span><span class="sxs-lookup"><span data-stu-id="31731-225">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="31731-226">チャネル1で受信したシグナルレベル。</span><span class="sxs-lookup"><span data-stu-id="31731-226">Signal level as received on channel 1.</span></span></p>
<p><span data-ttu-id="31731-227">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="31731-227">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31731-228"><strong>RecvSignalLevelCh2</strong></span><span class="sxs-lookup"><span data-stu-id="31731-228"><strong>RecvSignalLevelCh2</strong></span></span></p></td>
<td><p><span data-ttu-id="31731-229">int</span><span class="sxs-lookup"><span data-stu-id="31731-229">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="31731-230">チャネル2で受信したシグナルレベル。</span><span class="sxs-lookup"><span data-stu-id="31731-230">Signal level as received on channel 2.</span></span></p>
<p><span data-ttu-id="31731-231">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="31731-231">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31731-232"><strong>RecvNoiseLevelCh1</strong></span><span class="sxs-lookup"><span data-stu-id="31731-232"><strong>RecvNoiseLevelCh1</strong></span></span></p></td>
<td><p><span data-ttu-id="31731-233">int</span><span class="sxs-lookup"><span data-stu-id="31731-233">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="31731-234">チャネル1で受信したノイズレベル。</span><span class="sxs-lookup"><span data-stu-id="31731-234">Noise level as received on channel 1.</span></span></p>
<p><span data-ttu-id="31731-235">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="31731-235">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31731-236"><strong>RecvNoiseLevelCh2</strong></span><span class="sxs-lookup"><span data-stu-id="31731-236"><strong>RecvNoiseLevelCh2</strong></span></span></p></td>
<td><p><span data-ttu-id="31731-237">int</span><span class="sxs-lookup"><span data-stu-id="31731-237">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="31731-238">チャネル2で受信したノイズレベル。</span><span class="sxs-lookup"><span data-stu-id="31731-238">Noise level as received on channel 2.</span></span></p>
<p><span data-ttu-id="31731-239">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="31731-239">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31731-240"><strong>SendSignalLevelCh1</strong></span><span class="sxs-lookup"><span data-stu-id="31731-240"><strong>SendSignalLevelCh1</strong></span></span></p></td>
<td><p><span data-ttu-id="31731-241">int</span><span class="sxs-lookup"><span data-stu-id="31731-241">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="31731-242">チャネル1で送信されたシグナルレベル。</span><span class="sxs-lookup"><span data-stu-id="31731-242">Signal level as sent on channel 1.</span></span></p>
<p><span data-ttu-id="31731-243">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="31731-243">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31731-244"><strong>SendSignalLevelCh2</strong></span><span class="sxs-lookup"><span data-stu-id="31731-244"><strong>SendSignalLevelCh2</strong></span></span></p></td>
<td><p><span data-ttu-id="31731-245">int</span><span class="sxs-lookup"><span data-stu-id="31731-245">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="31731-246">チャネル2で送信されたシグナルレベル。</span><span class="sxs-lookup"><span data-stu-id="31731-246">Signal level as sent on channel 2.</span></span></p>
<p><span data-ttu-id="31731-247">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="31731-247">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31731-248"><strong>SendNoiseLevelCh1</strong></span><span class="sxs-lookup"><span data-stu-id="31731-248"><strong>SendNoiseLevelCh1</strong></span></span></p></td>
<td><p><span data-ttu-id="31731-249">int</span><span class="sxs-lookup"><span data-stu-id="31731-249">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="31731-250">チャネル1で送信されたノイズレベル。</span><span class="sxs-lookup"><span data-stu-id="31731-250">Noise level as sent on channel 1.</span></span></p>
<p><span data-ttu-id="31731-251">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="31731-251">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31731-252"><strong>SendNoiseLevelCh2</strong></span><span class="sxs-lookup"><span data-stu-id="31731-252"><strong>SendNoiseLevelCh2</strong></span></span></p></td>
<td><p><span data-ttu-id="31731-253">int</span><span class="sxs-lookup"><span data-stu-id="31731-253">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="31731-254">チャンネル2に送信されたノイズレベル。</span><span class="sxs-lookup"><span data-stu-id="31731-254">Noise level as sent on channel 2.</span></span></p>
<p><span data-ttu-id="31731-255">この列は Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="31731-255">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="31731-256">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="31731-256">


</div>

<span> </span>

</div>

</div>

</span></span></div>

