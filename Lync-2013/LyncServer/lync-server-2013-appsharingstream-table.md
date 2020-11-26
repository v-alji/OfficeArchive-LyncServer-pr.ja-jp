---
title: 'Lync Server 2013: AppSharingStream テーブル'
description: 'Lync Server 2013: AppSharingStream テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AppSharingStream table
ms:assetid: 391490cb-d7b8-44ca-b4d1-429600da909c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204808(v=OCS.15)
ms:contentKeyID: 48183852
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b530af5b489e090e5d0d00fbb01b2b950bafbe5a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440557"
---
# <a name="appsharingstream-table-in-lync-server-2013"></a><span data-ttu-id="fc4e1-103">Lync Server 2013 の AppSharingStream テーブル</span><span class="sxs-lookup"><span data-stu-id="fc4e1-103">AppSharingStream table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fc4e1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fc4e1-104">

<span> </span></span></span>

<span data-ttu-id="fc4e1-105">_**最終更新日:** 2014-02-21_</span><span class="sxs-lookup"><span data-stu-id="fc4e1-105">_**Topic Last Modified:** 2014-02-21_</span></span>

<span data-ttu-id="fc4e1-106">AppSharingStream テーブルには、アプリケーション共有に使用されるネットワークストリームのエクスペリエンスのメトリックの質が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-106">The AppSharingStream table contains Quality of Experience metrics for the network streams used for application sharing.</span></span> <span data-ttu-id="fc4e1-107">この表は、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-107">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fc4e1-108"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="fc4e1-109"><strong>データ型</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="fc4e1-110"><strong>キー/インデックス</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="fc4e1-111"><strong>詳細</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-113">dateTime</span><span class="sxs-lookup"><span data-stu-id="fc4e1-113">dateTime</span></span></p></td>
<td><p><span data-ttu-id="fc4e1-114">プライマリ、外部</span><span class="sxs-lookup"><span data-stu-id="fc4e1-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="fc4e1-115">セッションが開始された日付と時刻。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-115">Date and time that the session started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-117">int</span><span class="sxs-lookup"><span data-stu-id="fc4e1-117">int</span></span></p></td>
<td><p><span data-ttu-id="fc4e1-118">プライマリ、外部</span><span class="sxs-lookup"><span data-stu-id="fc4e1-118">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="fc4e1-119">同じ日付と同時に開始したセッションを区別するために使用されるシーケンシャル識別子。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-119">Sequential identifier used to distinguish between sessions that started on the same date and at the same time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="fc4e1-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="fc4e1-122">プライマリ、外部</span><span class="sxs-lookup"><span data-stu-id="fc4e1-122">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="fc4e1-123">通話で使用されるビデオラインの種類を表します。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-123">Represents the type of video line used in the call.</span></span> <span data-ttu-id="fc4e1-124">有効な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-124">Allowed values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="fc4e1-125">0–音声</span><span class="sxs-lookup"><span data-stu-id="fc4e1-125">0 – Audio</span></span></p></li>
<li><p><span data-ttu-id="fc4e1-126">1-ビデオ</span><span class="sxs-lookup"><span data-stu-id="fc4e1-126">1 – Video</span></span></p></li>
<li><p><span data-ttu-id="fc4e1-127">2-パノラマビデオ</span><span class="sxs-lookup"><span data-stu-id="fc4e1-127">2 – Panoramic video</span></span></p></li>
<li><p><span data-ttu-id="fc4e1-128">3-アプリケーション/デスクトップ共有</span><span class="sxs-lookup"><span data-stu-id="fc4e1-128">3 –Application/Desktop Sharing</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-129"><strong>StreamID</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-129"><strong>StreamID</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-130">int</span><span class="sxs-lookup"><span data-stu-id="fc4e1-130">int</span></span></p></td>
<td><p><span data-ttu-id="fc4e1-131">Primary</span><span class="sxs-lookup"><span data-stu-id="fc4e1-131">Primary</span></span></p></td>
<td><p><span data-ttu-id="fc4e1-132">アプリケーション共有ストリームの一意の識別子。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-132">Unique identifier of the application sharing stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-133"><strong>JitterInterArrival</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-133"><strong>JitterInterArrival</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-134">int</span><span class="sxs-lookup"><span data-stu-id="fc4e1-134">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-135">RTP パケットの着信間に検出された平均ジッター (ジッターとは、通話の "揺れ" の測定値です)。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-135">Average jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="fc4e1-136">(ジッタは、 &quot; 通話の shakiness の尺度です &quot; )。通常、高ジッターの値は、輻輳または過負荷のメディアサーバーによって発生し、音声が歪むか、失われる原因となります。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-136">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-137"><strong>JitterInterArrivalMax</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-137"><strong>JitterInterArrivalMax</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-138">int</span><span class="sxs-lookup"><span data-stu-id="fc4e1-138">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-139">RTP パケット着信の間の最大ジッターが検出されました。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-139">Maximum jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="fc4e1-140">(ジッタは、 &quot; 通話の shakiness の尺度です &quot; )。通常、高ジッターの値は、輻輳または過負荷のメディアサーバーによって発生し、音声が歪むか、失われる原因となります。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-140">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-141"><strong>RoundTrip</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-141"><strong>RoundTrip</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-142">int</span><span class="sxs-lookup"><span data-stu-id="fc4e1-142">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-p105">リアルタイム転送プロトコル (RTP) パケットが別のエンドポイントとの間を往復するのに要する平均時間 (ミリ秒単位)。200 ミリ秒以下の往復時間が許容できる品質と見なされます。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-p105">Average amount of (in milliseconds) required for a Real-Time Transport Protocol packet to travel to another endpoint and then back. Round-trip times of 200 milliseconds or less are considered of acceptable quality.</span></span></p>
<p><span data-ttu-id="fc4e1-p106">この値が高い場合は、国際通話ルーティング、ルーティングの構成ミス、メディア サーバーの過負荷などの原因が考えられます。その結果、双方向のリアルタイムの音声会話が難しくなります。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-p106">High round-trip values can be caused by international call routing; a routing misconfiguration; or an overloaded media server. High round-trip times result in difficulties with two-way, real-time audio conversations.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-147"><strong>RoundTripMax</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-147"><strong>RoundTripMax</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-148">int</span><span class="sxs-lookup"><span data-stu-id="fc4e1-148">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-149">Real-Time トランスポートプロトコルパケットが別のエンドポイントに移動してから戻るために必要な最長 (ミリ秒単位)。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-149">Maximum amount of (in milliseconds) required for a Real-Time Transport Protocol packet to travel to another endpoint and then back.</span></span> <span data-ttu-id="fc4e1-150">200 ミリ秒以下の往復時間が許容できる品質と見なされます。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-150">Round-trip times of 200 milliseconds or less are considered of acceptable quality.</span></span></p>
<p><span data-ttu-id="fc4e1-p108">この値が高い場合は、国際通話ルーティング、ルーティングの構成ミス、メディア サーバーの過負荷などの原因が考えられます。その結果、双方向のリアルタイムの音声会話が難しくなります。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-p108">High round-trip values can be caused by international call routing; a routing misconfiguration; or an overloaded media server. High round-trip times result in difficulties with two-way, real-time audio conversations.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-153"><strong>PacketLossRate</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-153"><strong>PacketLossRate</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-154">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-154">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-p109">リアルタイム転送プロトコル (RTP) パケット損失の平均レート。(パケット損失は、RTP パケット、つまりインターネット経由で音声とビデオを転送するために使われるプロトコルの一種で、パケットが宛先に到達できなかったときに発生します)。この値が高い場合は、輻輳、帯域幅の不足、ワイヤレスの輻輳または干渉、メディア サーバーの過負荷などの原因が考えられます。パケット損失が発生すると、通常、音声のひずみや欠落が生じます。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-p109">Average rate of Real-Time Transport Protocol (RTP) packet loss. (Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion; lack of bandwidth; wireless congestion or interference; or an overloaded media server. Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-158"><strong>PacketLossRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-158"><strong>PacketLossRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-159">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-159">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-160">Real-Time トランスポートプロトコル (RTP) パケットロスの最大速度。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-160">Maximum rate of Real-Time Transport Protocol (RTP) packet loss.</span></span> <span data-ttu-id="fc4e1-161">(パケットの損失は、RTP パケット、インターネット上でのオーディオとビデオの伝送に使用されるプロトコル)、宛先への到達に失敗した場合に発生します。)通常、高損失率は輻輳が原因で発生します。帯域幅の不足。ワイヤレスの輻輳または妨害または、オーバーロードされたメディアサーバー。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-161">(Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion; lack of bandwidth; wireless congestion or interference; or an overloaded media server.</span></span> <span data-ttu-id="fc4e1-162">パケット損失が発生すると、通常、音声のひずみや欠落が生じます。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-162">Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-163"><strong>PacketUtilization</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-163"><strong>PacketUtilization</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-164">int</span><span class="sxs-lookup"><span data-stu-id="fc4e1-164">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-165">送信されたパケットの数です。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-165">Number of packets sent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-166"><strong>BandwidthEst</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-166"><strong>BandwidthEst</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-167">int</span><span class="sxs-lookup"><span data-stu-id="fc4e1-167">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-168">セッションの終了時に提供される推定される一方向の帯域幅。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-168">Estimated one-way bandwidth available at the end of the session.</span></span> <span data-ttu-id="fc4e1-169">1秒あたりのビット数で報告されます。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-169">Reported in bits per second.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-170"><strong>AppSharingPayloadDescription</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-170"><strong>AppSharingPayloadDescription</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-171">int</span><span class="sxs-lookup"><span data-stu-id="fc4e1-171">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-172">アプリケーション共有ペイロードの説明。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-172">Description of the application sharing payload.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-173"><strong>RelativeOneWayTotal</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-173"><strong>RelativeOneWayTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-174">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-174">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-175">一方向の待機時間の合計。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-175">Total amount of one-way latency.</span></span> <span data-ttu-id="fc4e1-176">相対的な一方向の待ち時間は、クライアントとサーバーの間の遅延を測定します。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-176">Relative one-way latency measures the delay between the client and the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-177"><strong>RelativeOneWayAverage</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-177"><strong>RelativeOneWayAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-178">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-178">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-179">一方向の待ち時間の平均値。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-179">Average amount of one-way latency.</span></span> <span data-ttu-id="fc4e1-180">相対的な一方向の待ち時間は、クライアントとサーバーの間の遅延を測定します。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-180">Relative one-way latency measures the delay between the client and the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-181"><strong>RelativeOneWayMax</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-181"><strong>RelativeOneWayMax</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-182">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-182">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-183">一方向の待機時間の上限。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-183">Maximum amount of one-way latency.</span></span> <span data-ttu-id="fc4e1-184">相対的な一方向の待ち時間は、クライアントとサーバーの間の遅延を測定します。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-184">Relative one-way latency measures the delay between the client and the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-185"><strong>RelativeOneWayBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-185"><strong>RelativeOneWayBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-186">int</span><span class="sxs-lookup"><span data-stu-id="fc4e1-186">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-187">1方向のバースト発生の合計。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-187">Total one-way burst occurrences.</span></span> <span data-ttu-id="fc4e1-188">"Bursty" 伝送とは、安定したストリームと比べて予期しないバーストでデータが流れる伝送です。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-188">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="fc4e1-189">このメトリックは、クライアントとサーバー間のデータフローを計測します。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-189">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-190"><strong>RelativeOneWayBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-190"><strong>RelativeOneWayBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-191">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-191">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-192">全体的な1方向バースト密度。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-192">Total one-way burst density.</span></span> <span data-ttu-id="fc4e1-193">"Bursty" 伝送とは、安定したストリームと比べて予期しないバーストでデータが流れる伝送です。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-193">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="fc4e1-194">このメトリックは、クライアントとサーバー間のデータフローを計測します。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-194">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-195"><strong>RelativeOneWayBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-195"><strong>RelativeOneWayBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-196">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-196">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-197">一方向のバースト期間の合計。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-197">Total one-way burst duration.</span></span> <span data-ttu-id="fc4e1-198">"Bursty" 伝送とは、安定したストリームと比べて予期しないバーストでデータが流れる伝送です。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-198">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="fc4e1-199">このメトリックは、クライアントとサーバー間のデータフローを計測します。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-199">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-200"><strong>RelativeOneWayGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-200"><strong>RelativeOneWayGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-201">int</span><span class="sxs-lookup"><span data-stu-id="fc4e1-201">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-202">一方向のギャップ出現の合計。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-202">Total one-way gap occurrences.</span></span> <span data-ttu-id="fc4e1-203">"Bursty" 伝送とは、安定したストリームではなく、予期しないバーストでデータが流れる伝送です。ギャップは、このようなバーストの間の遅延を示します。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-203">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="fc4e1-204">このメトリックは、クライアントとサーバー間のデータフローを計測します。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-204">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-205"><strong>RelativeOneWayGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-205"><strong>RelativeOneWayGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-206">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-206">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-207">一方向のギャップの密度の合計。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-207">Total one-way gap density.</span></span> <span data-ttu-id="fc4e1-208">"Bursty" 伝送とは、安定したストリームではなく、予期しないバーストでデータが流れる伝送です。ギャップは、このようなバーストの間の遅延を示します。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-208">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="fc4e1-209">このメトリックは、クライアントとサーバー間のデータフローを計測します。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-209">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-210"><strong>RelativeOneWayGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-210"><strong>RelativeOneWayGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-211">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-211">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-212">一方向のギャップ期間の合計。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-212">Total one-way gap duration.</span></span> <span data-ttu-id="fc4e1-213">"Bursty" 伝送とは、安定したストリームではなく、予期しないバーストでデータが流れる伝送です。ギャップは、このようなバーストの間の遅延を示します。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-213">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="fc4e1-214">このメトリックは、クライアントとサーバー間のデータフローを計測します。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-214">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-215"><strong>ApplicationSharingType</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-215"><strong>ApplicationSharingType</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-216">varChar (256)</span><span class="sxs-lookup"><span data-stu-id="fc4e1-216">varChar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-217">アプリケーションロール (共有先またはビューアー) とコンテンツタイプ。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-217">Application role (Sharer or Viewer) and content type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-218"><strong>RDPTileProcessingLatencyTotal</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-218"><strong>RDPTileProcessingLatencyTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-219">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-219">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-220">リモートデスクトッププロトコル (RDP) タイルの合計処理時間。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-220">Total processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="fc4e1-221">表示環境では、合計の遅延が長くなります。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-221">A higher total equates to a longer delay in the viewing experience.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-222"><strong>Rdp タイル処理</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-222"><strong>RDPTileProcessingLatencyAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-223">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-223">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-224">リモートデスクトッププロトコル (RDP) タイルの平均処理時間。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-224">Average processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="fc4e1-225">表示環境では、合計の遅延が長くなります。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-225">A higher total equates to a longer delay in the viewing experience.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-226"><strong>RDPTileProcessingLatencyMax</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-226"><strong>RDPTileProcessingLatencyMax</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-227">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-227">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-228">リモートデスクトッププロトコル (RDP) タイルの最大処理時間。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-228">Maximum processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="fc4e1-229">表示環境では、合計の遅延が長くなります。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-229">A higher total equates to a longer delay in the viewing experience.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-230"><strong>RDPTileProcessingLatencyBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-230"><strong>RDPTileProcessingLatencyBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-231">int</span><span class="sxs-lookup"><span data-stu-id="fc4e1-231">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-232">リモートデスクトッププロトコル (RDP) タイルの処理時間でのバースト発生。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-232">Burst occurrences in the processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="fc4e1-233">"Bursty" 伝送とは、安定したストリームと比べて予期しないバーストでデータが流れる伝送です。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-233">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-234"><strong>RDPTileProcessingLatencyBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-234"><strong>RDPTileProcessingLatencyBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-235">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-235">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-236">リモートデスクトッププロトコル (RDP) タイルの処理時間のバースト密度。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-236">Burst density in the processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="fc4e1-237">"Bursty" 伝送とは、安定したストリームと比べて予期しないバーストでデータが流れる伝送です。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-237">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-238"><strong>RDPTileProcessingLatencyBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-238"><strong>RDPTileProcessingLatencyBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-239">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-239">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-240">リモートデスクトッププロトコル (RDP) タイルの処理時間のバースト時間。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-240">Burst duration in the processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="fc4e1-241">"Bursty" 伝送とは、安定したストリームと比べて予期しないバーストでデータが流れる伝送です。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-241">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-242"><strong>RDPTileProcessingLatencyGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-242"><strong>RDPTileProcessingLatencyGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-243">int</span><span class="sxs-lookup"><span data-stu-id="fc4e1-243">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-244">リモートデスクトッププロトコル (RDP) タイルの処理時間のギャップの出現回数。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-244">Gap occurrences in the processing time for remote desktop protocol (RDP) tiles.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-245"><strong>RDPTileProcessingLatencyGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-245"><strong>RDPTileProcessingLatencyGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-246">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-246">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-247">リモートデスクトッププロトコル (RDP) タイルの処理時間のギャップの密度。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-247">Gap density in the processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="fc4e1-248">隙間が小さいほど、表示エクスペリエンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-248">Low gap density equates to a better viewing experience.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-249"><strong>RDPTileProcessingLatencyGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-249"><strong>RDPTileProcessingLatencyGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-250">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-250">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-251">リモートデスクトッププロトコル (RDP) タイルの処理時間の間隔。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-251">Gap duration in the processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="fc4e1-252">短い間隔の期間は、表示感が向上するようになります。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-252">Short gap durations equate to a better viewing experience.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-253"><strong>CaptureTileRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-253"><strong>CaptureTileRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-254">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-254">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-255">キャプチャされたタイルの合計レート (1 秒あたりのタイル数)</span><span class="sxs-lookup"><span data-stu-id="fc4e1-255">Total rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-256"><strong>CaptureTileRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-256"><strong>CaptureTileRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-257">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-257">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-258">キャプチャされたタイルの平均速度 (1 秒あたりのタイル数)。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-258">Average rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-259"><strong>CaptureTileRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-259"><strong>CaptureTileRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-260">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-260">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-261">キャプチャされたタイルの最大速度 (1 秒あたりのタイル数)</span><span class="sxs-lookup"><span data-stu-id="fc4e1-261">Maximum rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-262"><strong>CaptureTileRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-262"><strong>CaptureTileRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-263">t</span><span class="sxs-lookup"><span data-stu-id="fc4e1-263">in t</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-264">キャプチャされたタイルの速度 (1 秒あたりのタイル) でバーストが発生します。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-264">Burst occurrences in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-265"><strong>CaptureTileRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-265"><strong>CaptureTileRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-266">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-266">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-267">キャプチャされたタイルの速度 (1 秒あたりのタイル数) のバースト密度。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-267">Burst density in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-268"><strong>CaptureTileRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-268"><strong>CaptureTileRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-269">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-269">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-270">キャプチャされたタイルの割合でのバースト時間 (1 秒あたりのタイル数)。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-270">Burst duration in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-271"><strong>CaptureTileRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-271"><strong>CaptureTileRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-272">int</span><span class="sxs-lookup"><span data-stu-id="fc4e1-272">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-273">キャプチャされたタイルの比率 (1 秒あたりのタイル数) でのギャップ出現回数。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-273">Gap occurrences in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-274"><strong>CaptureTileRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-274"><strong>CaptureTileRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-275">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-275">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-276">キャプチャされたタイル (1 秒あたりのタイル数) の間隔の間隔。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-276">Gap density in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-277"><strong>CaptureTileRateGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-277"><strong>CaptureTileRateGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-278">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-278">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-279">キャプチャされたタイルの割合の間隔 (1 秒あたりのタイル数)</span><span class="sxs-lookup"><span data-stu-id="fc4e1-279">Gap duration in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-280"><strong>損失タイル</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-280"><strong>SpoiledTilePercentTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-281">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-281">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-282">閲覧者に届かなかったが、破棄され、最新のコンテンツによって上書きされたコンテンツの割合の合計。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-282">Total percentage of the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-283"><strong>SpoiledTilePercentAverage</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-283"><strong>SpoiledTilePercentAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-284">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-284">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-285">閲覧者に届かなかったが、新しいコンテンツによって破棄されて上書きされたコンテンツの平均割合。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-285">Average percentage of the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-286"><strong>SpoiledTilePercentMax</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-286"><strong>SpoiledTilePercentMax</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-287">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-287">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-288">閲覧者に届かなかったが、新しいコンテンツによって破棄されて上書きされたコンテンツの最大パーセンテージ。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-288">Maximum percentage of the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-289"><strong>SpoiledTilePercentBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-289"><strong>SpoiledTilePercentBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-290">int</span><span class="sxs-lookup"><span data-stu-id="fc4e1-290">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-291">閲覧者に届かなかったが、新しいコンテンツによって破棄されて上書きされたコンテンツのバースト発生。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-291">Burst occurrences for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-292"><strong>SpoiledTilePercentBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-292"><strong>SpoiledTilePercentBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-293">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-293">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-294">ビューアーに届かなかったが、新しいコンテンツによって破棄されて上書きされたコンテンツのバースト密度。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-294">Burst density for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-295"><strong>SpoiledTilePercentBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-295"><strong>SpoiledTilePercentBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-296">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-296">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-297">ビューアーに届かなかったが、新しいコンテンツによって破棄されて上書きされたコンテンツのバースト時間。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-297">Burst duration for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-298"><strong>SpoiledTilePercentGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-298"><strong>SpoiledTilePercentGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-299">int</span><span class="sxs-lookup"><span data-stu-id="fc4e1-299">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-300">閲覧者に届かなかったが、新しいコンテンツによって破棄されて上書きされたコンテンツの Gap オカレンス。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-300">Gap occurrences for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-301"><strong>SpoiledTilePercentGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-301"><strong>SpoiledTilePercentGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-302">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-302">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-303">ビューアーに届かなかったが、新しいコンテンツで破棄されて上書きされたコンテンツの Gap 濃度。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-303">Gap density for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-304"><strong>SpoiledTilePercentGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-304"><strong>SpoiledTilePercentGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-305">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-305">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-306">ビューアーに届かなかったが、新しいコンテンツによって破棄されて上書きされたコンテンツの間隔の期間。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-306">Gap duration for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-307"><strong>ScrapingFrameRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-307"><strong>ScrapingFrameRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-308">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-308">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-309">グラフィックスソースから scraped フレームの合計数です。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-309">Total number of frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-310"><strong>ScrapingFrameRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-310"><strong>ScrapingFrameRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-311">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-311">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-312">グラフィックスソースから scraped フレームの平均数。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-312">Average number of frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-313"><strong>ScrapingFrameRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-313"><strong>ScrapingFrameRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-314">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-314">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-315">グラフィックスソースから scraped フレームの最大数。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-315">Maximum number of frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-316"><strong>ScrapingFrameRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-316"><strong>ScrapingFrameRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-317">int</span><span class="sxs-lookup"><span data-stu-id="fc4e1-317">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-318">グラフィックソースからフレームの scraped が発生します。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-318">Burst occurrences in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-319"><strong>ScrapingFrameRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-319"><strong>ScrapingFrameRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-320">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-320">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-321">グラフィックスソースからのフレーム scraped のバースト密度。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-321">Burst density in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-322"><strong>ScrapingFrameRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-322"><strong>ScrapingFrameRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-323">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-323">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-324">グラフィックスソースからのフレーム scraped のバースト時間。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-324">Burst duration in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-325"><strong>ScrapingFrameRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-325"><strong>ScrapingFrameRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-326">int</span><span class="sxs-lookup"><span data-stu-id="fc4e1-326">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-327">グラフィックソースから、フレーム内の Gap オカレンスが scraped ます。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-327">Gap occurrences in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-328"><strong>ScrapingFrameRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-328"><strong>ScrapingFrameRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-329">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-329">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-330">グラフィックスソースから scraped フレームの間隔の濃度。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-330">Gap density in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-331"><strong>ScrapingFrameRateGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-331"><strong>ScrapingFrameRateGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-332">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-332">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-333">グラフィックスソースから scraped フレームの間隔を指定します。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-333">Gap duration in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-334"><strong>IncomingTileRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-334"><strong>IncomingTileRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-335">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-335">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-336">視聴者が受信したフレームの合計料金。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-336">Total incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-337"><strong>IncomingTileRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-337"><strong>IncomingTileRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-338">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-338">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-339">視聴者が受信したフレームの平均速度。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-339">Average incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-340"><strong>IncomingTileRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-340"><strong>IncomingTileRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-341">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-341">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-342">視聴者が受信した最大受信タイルレート。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-342">Maximum incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-343"><strong>IncomingTileRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-343"><strong>IncomingTileRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-344">int</span><span class="sxs-lookup"><span data-stu-id="fc4e1-344">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-345">視聴者が受信したタイルレートでのバースト発生</span><span class="sxs-lookup"><span data-stu-id="fc4e1-345">Burst occurrences in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-346"><strong>IncomingTileRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-346"><strong>IncomingTileRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-347">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-347">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-348">視聴者が受信したタイルレートのバースト密度。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-348">Burst density in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-349"><strong>IncomingTileRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-349"><strong>IncomingTileRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-350">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-350">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-351">閲覧者が受信した受信タイルレートのバースト時間。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-351">Burst duration in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-352"><strong>IncomingTileRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-352"><strong>IncomingTileRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-353">int</span><span class="sxs-lookup"><span data-stu-id="fc4e1-353">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-354">閲覧者が受信したタイルレートのギャップが表示されます。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-354">Gap occurrences in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-355"><strong>IncomingTileRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-355"><strong>IncomingTileRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-356">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-356">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-357">閲覧者によって受信された、受信タイルレートのギャップの密度。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-357">Gap density in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-358"><strong>IncomingTileRateGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-358"><strong>IncomingTileRateGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-359">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-359">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-360">視聴者が受信したタイルレートの間隔。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-360">Gap duration in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-361"><strong>IncomingFrameRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-361"><strong>IncomingFrameRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-362">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-362">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-363">視聴者が受信したフレームの合計料金。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-363">Total incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-364"><strong>IncomingFrameRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-364"><strong>IncomingFrameRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-365">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-365">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-366">視聴者が受信したフレームの平均速度。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-366">Average incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-367"><strong>IncomingFrameRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-367"><strong>IncomingFrameRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-368">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-368">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-369">視聴者が受信した受信フレームレートの上限。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-369">Maximum incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-370"><strong>IncomingFrameRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-370"><strong>IncomingFrameRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-371">int</span><span class="sxs-lookup"><span data-stu-id="fc4e1-371">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-372">視聴者が受信したフレームレートのバーストが発生します。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-372">Burst occurrences in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-373"><strong>IncomingFrameRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-373"><strong>IncomingFrameRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-374">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-374">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-375">視聴者が受信したフレームレートのバースト密度。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-375">Burst density in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-376"><strong>IncomingFrameRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-376"><strong>IncomingFrameRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-377">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-377">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-378">ビューアーで受信した受信フレームレートのバースト時間。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-378">Burst duration in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-379"><strong>IncomingFrameRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-379"><strong>IncomingFrameRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-380">int</span><span class="sxs-lookup"><span data-stu-id="fc4e1-380">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-381">閲覧者が受信したフレームレートのギャップが表示されます。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-381">Gap occurrences in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-382"><strong>IncomingFrameRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-382"><strong>IncomingFrameRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-383">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-383">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-384">視聴者が受信したフレームレートの間隔。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-384">Gap density in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-385"><strong>IncomingFrameRateDuration</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-385"><strong>IncomingFrameRateDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-386">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-386">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-387">視聴者が受信したフレームレートの間隔。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-387">Gap duration in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-388"><strong>OutgoingTileRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-388"><strong>OutgoingTileRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-389">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-389">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-390">送信者の合計送信タイルレート。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-390">Total outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-391"><strong>OutgoingTileRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-391"><strong>OutgoingTileRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-392">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-392">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-393">送信者の平均送信タイルレート。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-393">Average outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-394"><strong>OutgoingTileRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-394"><strong>OutgoingTileRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-395">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-395">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-396">送信者の最大送信タイルレート。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-396">Maximum outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-397"><strong>OutgoingTileRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-397"><strong>OutgoingTileRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-398">int</span><span class="sxs-lookup"><span data-stu-id="fc4e1-398">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-399">送信者の送信タイルレートのバーストが発生します。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-399">Burst occurrences in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-400"><strong>OutgoingTileRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-400"><strong>OutgoingTileRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-401">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-401">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-402">送信者の送信タイルレートのバースト密度。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-402">Burst density in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-403"><strong>OutgoingTileRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-403"><strong>OutgoingTileRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-404">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-404">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-405">送信者の送信タイルレートのバースト時間。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-405">Burst duration in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-406"><strong>OutgoingTileRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-406"><strong>OutgoingTileRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-407">int</span><span class="sxs-lookup"><span data-stu-id="fc4e1-407">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-408">送信者に対して、送信タイルレートのギャップが発生します。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-408">Gap occurrences in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-409"><strong>OutgoingTileRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-409"><strong>OutgoingTileRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-410">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-410">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-411">送信者の送信タイルレートの間隔。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-411">Gap density in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-412"><strong>OutgoingTileRateGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-412"><strong>OutgoingTileRateGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-413">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-413">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-414">送信者の送信タイルレートの間隔。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-414">Gap duration in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-415"><strong>OutgoingFrameRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-415"><strong>OutgoingFrameRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-416">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-416">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-417">送信者の総送信フレームレート。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-417">Total outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-418"><strong>OutgoingFrameRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-418"><strong>OutgoingFrameRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-419">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-419">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-420">送信者の平均送信フレームレート。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-420">average outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-421"><strong>OutgoingFrameRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-421"><strong>OutgoingFrameRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-422">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-422">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-423">送信者の最大送信フレームレート。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-423">Maximum outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-424"><strong>OutgoingFrameRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-424"><strong>OutgoingFrameRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-425">int</span><span class="sxs-lookup"><span data-stu-id="fc4e1-425">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-426">送信者の送信フレームレートでのバースト発生。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-426">Burst occurrences in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-427"><strong>OutgoingFrameRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-427"><strong>OutgoingFrameRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-428">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-428">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-429">送信者の送信フレームレートのバースト密度。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-429">Burst density in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-430"><strong>OutgoingFrameRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-430"><strong>OutgoingFrameRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-431">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-431">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-432">送信者の送信フレームレートのバースト時間。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-432">Burst duration in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-433"><strong>OutgoingFrameRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-433"><strong>OutgoingFrameRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-434">int</span><span class="sxs-lookup"><span data-stu-id="fc4e1-434">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-435">送信者に対して送信されるフレームレートのギャップ。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-435">Gap occurrences in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-436"><strong>OutgoingFrameRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-436"><strong>OutgoingFrameRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-437">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-437">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-438">送信者の発信フレームレートのギャップの密度。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-438">Gap density in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-439"><strong>OutgoingFrameRateGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-439"><strong>OutgoingFrameRateGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-440">float</span><span class="sxs-lookup"><span data-stu-id="fc4e1-440">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-441">送信者の発信フレームレートの間隔。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-441">Gap duration in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-442"><strong>AverageRectangleHeight</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-442"><strong>AverageRectangleHeight</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-443">int</span><span class="sxs-lookup"><span data-stu-id="fc4e1-443">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-444">平均ビデオ解像度の高さ (ピクセル単位)。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-444">Average video resolution height, in pixels.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-445"><strong>AverageRectangleWidth</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-445"><strong>AverageRectangleWidth</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-446">int</span><span class="sxs-lookup"><span data-stu-id="fc4e1-446">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-447">平均ビデオ解像度の幅 (ピクセル単位)。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-447">Average video resolution width, in pixels.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-448"><strong>トラフィック</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-448"><strong>Inbound</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-449">bit</span><span class="sxs-lookup"><span data-stu-id="fc4e1-449">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-450">受信伝送の平均フレームレート (1 秒あたりのフレーム数)。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-450">Average frame rate (in frames per second) for inbound transmissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc4e1-451"><strong>発信</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-451"><strong>Outbound</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-452">bit</span><span class="sxs-lookup"><span data-stu-id="fc4e1-452">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-453">送信時の平均フレームレート (1 秒あたりのフレーム数)。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-453">Average frame rate (in frames per second) for outbound transmissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc4e1-454"><strong>SenderIsCallerPAI</strong></span><span class="sxs-lookup"><span data-stu-id="fc4e1-454"><strong>SenderIsCallerPAI</strong></span></span></p></td>
<td><p><span data-ttu-id="fc4e1-455">bit</span><span class="sxs-lookup"><span data-stu-id="fc4e1-455">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc4e1-456">1ストリームの方向は、呼び出し元から呼び出し先へとなります。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-456">1 means the stream direction is from the caller to callee.</span></span></p>
<p><span data-ttu-id="fc4e1-457">0は、ストリームの方向を呼び出し元から呼び出し元に転送します。</span><span class="sxs-lookup"><span data-stu-id="fc4e1-457">0 means the stream direction is from the callee to the caller.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="fc4e1-458">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fc4e1-458">


</div>

<span> </span>

</div>

</div>

</span></span></div>

