---
title: 'Lync Server 2013: QoE データベース クエリのサンプル'
description: 'Lync Server 2013: QoE データベースクエリの例'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Sample QoE database queries
ms:assetid: 04e6bdd3-bbd1-47ca-8114-94a3db6beeeb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398100(v=OCS.15)
ms:contentKeyID: 48183280
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d9bd789cabc4773e96351fa653170bef474060a1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442132"
---
# <a name="sample-qoe-database-queries-in-lync-server-2013"></a><span data-ttu-id="83c23-103">Lync Server 2013 の QoE データベース クエリのサンプル</span><span class="sxs-lookup"><span data-stu-id="83c23-103">Sample QoE database queries in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="83c23-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="83c23-104">

<span> </span></span></span>

<span data-ttu-id="83c23-105">_**最終更新日:** 2012-10-17_</span><span class="sxs-lookup"><span data-stu-id="83c23-105">_**Topic Last Modified:** 2012-10-17_</span></span>

<span data-ttu-id="83c23-106">このセクションには、Quality of Experience (QoE) データベースのサンプルクエリが含まれています。</span><span class="sxs-lookup"><span data-stu-id="83c23-106">This section contains sample queries for the Quality of Experience (QoE) database.</span></span>

<span data-ttu-id="83c23-107">すべてのオーディオストリームについて、ジッタとパケット損失の平均を取得するには、次の例を使用します。</span><span class="sxs-lookup"><span data-stu-id="83c23-107">Use the following example to get the jitter and packet loss average for all audio streams.</span></span>

    select avg(cast(JitterInterArrival as bigint)) as JitterAvg, avg(PacketLossRate) as PacketLossRateAvg from AudioStream

<span data-ttu-id="83c23-108">次の例を使用して、会議コンソールを使用した会議の合計数を確認します。</span><span class="sxs-lookup"><span data-stu-id="83c23-108">Use the following example to find the total numbers of conferences that used Meeting Console.</span></span>

    select avg(ConversationalMOS)
    from SessionView s
    inner join MediaLineView m
    on s.ConferenceDateTime = m.ConferenceDateTime
       and s.SessionSeq = m.SessionSeq
       and m.MediaLineLabel = 0 -- audio media line
       and s.CallerUserAgentType = 4 -- Lync
       and s.CalleeUserAgentType = 4 -- Lync

<span data-ttu-id="83c23-109">次の例を使用して、ConversstionalMOS、SendingMOS、ListendingMOS をキャプチャデバイスごとに取得します。</span><span class="sxs-lookup"><span data-stu-id="83c23-109">Use the following example to get ConversstionalMOS, SendingMOS and ListendingMOS per capture device.</span></span>

    select t.DeviceName as Device, count(*) as SampleNum, avg(ConversationalMOS) as ConversationalMOS, avg(SendListenMOS) SendingMOS, avg(RecvListenMOS) as ListendingMOS
    from
    (
       select m.CallerCaptureDev as DeviceName, m.ConferenceDateTime, m.SessionSeq, a.StreamID, m.ConversationalMOS,a.SendListenMOS, a.RecvListenMOS
       from MediaLineView m
       inner join AudioStream a
       on m.ConferenceDateTime = a.ConferenceDateTime
          and m.SessionSeq = a.SessionSeq
          and m.MediaLineLabel = 0
    
       union
    
       select m.CalleeCaptureDev as DeviceName, m.ConferenceDateTime, m.SessionSeq, a.StreamID, m.ConversationalMOS,a.SendListenMOS, a.RecvListenMOS
       from MediaLineView m
       inner join AudioStream a
       on m.ConferenceDateTime = a.ConferenceDateTime
          and m.SessionSeq = a.SessionSeq
          and m.MediaLineLabel = 0
    
    )as t
    group by t.DeviceName
    order by SampleNum desc

<span data-ttu-id="83c23-110"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="83c23-110"></div>

<span> </span>

</div>

</div>

</span></span></div>

