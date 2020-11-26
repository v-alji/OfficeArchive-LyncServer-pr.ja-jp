---
title: 'Lync Server 2013: 大規模な会議のサポートについてよく寄せられる質問'
description: 'Lync Server 2013: 大規模な会議のサポートについてよく寄せられる質問。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync Server large meeting support FAQ
ms:assetid: 34b4fb6a-e35c-47e8-8ab1-f8331741fed2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204804(v=OCS.15)
ms:contentKeyID: 48183837
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c8d206400b46fc32a3af7b21ad7d50663e85d069
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426691"
---
# <a name="large-meeting-support-faq-for-lync-server-2013"></a><span data-ttu-id="ff716-103">Lync Server 2013 の大規模な会議のサポートについてよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="ff716-103">Large meeting support FAQ for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ff716-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ff716-104">

<span> </span></span></span>

<span data-ttu-id="ff716-105">_**最終更新日:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="ff716-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="ff716-106">以下のセクションでは、大規模な会議を作成して実行する場合の一般的な質問に対する回答を提供します。</span><span class="sxs-lookup"><span data-stu-id="ff716-106">The following sections provide answers to common questions for creating and running large meetings.</span></span>

<div>

## <a name="q-how-many-users-can-participate-in-a-large-meeting"></a><span data-ttu-id="ff716-107">Q: 大きな会議に参加できるユーザー数はいくつですか。</span><span class="sxs-lookup"><span data-stu-id="ff716-107">Q: How many users can participate in a large meeting?</span></span>

<span data-ttu-id="ff716-108">Lync Server のユーザーモデルでは、共有プール内の250ユーザー、または大規模な会議専用のプール内の1000ユーザーの制限が指定されていますが、これらの番号は、テストで使用した特定のハードウェアのセットに対してのみ、テストしたユーザーの数のみを表します。</span><span class="sxs-lookup"><span data-stu-id="ff716-108">The Lync Server user model specifies limits of 250 users in a shared pool or 1000 users in a pool dedicated to large meetings, but these numbers only represent the number of users we tested and only for the specific set of hardware that we used in our testing.</span></span> <span data-ttu-id="ff716-109">今回のテストに基づき、最大サイズの制限をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ff716-109">Based on our testing, we recommend those limits for maximum sizes.</span></span> <span data-ttu-id="ff716-110">ただし、(Lync Server 管理シェルで Windows PowerShell コマンドレットを使用して、または Lync Server コントロールパネルを使用して) 1 つ以上の会議ポリシーを構成することで、組織内の会議で許可される実際の参加者の数を制御できます。</span><span class="sxs-lookup"><span data-stu-id="ff716-110">However, you control the actual number of participants allowed in meetings in your organization by configuring one or more conferencing policies (which you configure using Windows PowerShell cmdlets in the Lync Server Management Shell or using the Lync Server Control Panel).</span></span> <span data-ttu-id="ff716-111">会議ポリシーで指定した数値は、1から4294967295までの任意の32ビットの整数にすることができますが、推奨されるサイズは 2 ~ 250 のどちらかです。既定値は250です。</span><span class="sxs-lookup"><span data-stu-id="ff716-111">The number that you specify in a conferencing policy can be any 32-bit whole number between 1 and 4,294,967,295, but the recommended size is between 2 and 250 participants, inclusive; and the default value is 250.</span></span>

</div>

<div>

## <a name="q-how-many-meetings-or-other-workloads-can-i-have-in-a-pool-that-is-dedicated-to-large-meetings"></a><span data-ttu-id="ff716-112">Q: 大規模な会議専用のプールでは、どのくらいの会議や他のワークロードを使用できますか?</span><span class="sxs-lookup"><span data-stu-id="ff716-112">Q: How many meetings or other workloads can I have in a pool that is dedicated to large meetings?</span></span>

<span data-ttu-id="ff716-113">最大で1000の参加者の大規模な会議で最高のユーザーエクスペリエンスを実現するには、大規模な会議専用のプールで一度に1つの大きな会議のみをホスティングすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ff716-113">To ensure the best user experience in large meetings of up to 1000 participants, we recommend hosting only a single large meeting at a time on a pool that is dedicated to large meetings.</span></span> <span data-ttu-id="ff716-114">また、大規模な会議の進行中に、そのプールで他のワークロードを実行できないようにすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ff716-114">We also recommend not allowing any other workloads to run on that pool when the large meeting is in progress.</span></span>

</div>

<div>

## <a name="q-should-the-organizers-of-large-meeting-be-homed-on-the-dedicated-pool"></a><span data-ttu-id="ff716-115">Q: 大規模な会議の開催者が専用のプールをホームにしているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="ff716-115">Q: Should the organizers of large meeting be homed on the dedicated pool?</span></span>

<span data-ttu-id="ff716-116">いいえ。</span><span class="sxs-lookup"><span data-stu-id="ff716-116">No.</span></span> <span data-ttu-id="ff716-117">専用プールで大規模な会議のスケジュールを管理する専用スタッフ以外のユーザーは、すべてのユーザーを割り当てることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ff716-117">We recommend not homing any users other than the dedicated staff that manages scheduling of large meetings on the dedicated pool.</span></span> <span data-ttu-id="ff716-118">これにより、その他のリアルタイム通信トラフィックが、プールでホストされている大規模な会議で問題が発生するのを防ぎます。</span><span class="sxs-lookup"><span data-stu-id="ff716-118">This prevents other real-time communications traffic from causing problems with large meetings that are hosted in the pool.</span></span> <span data-ttu-id="ff716-119">大規模な会議スケジュールのスタッフのユーザーアカウントを使用して、専用プールで大規模な会議をスケジュールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff716-119">You should schedule large meetings on the dedicated pool using a user account of the large meeting scheduling staff.</span></span> <span data-ttu-id="ff716-120">会議の開催者 (大きな会議を要求するユーザー) のユーザーアカウントを大きな会議の発表者として追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff716-120">You should add the user account of the meeting organizer (the user who requests a large meeting) as a presenter for the large meeting.</span></span>

</div>

<div>

## <a name="q-what-media-modalities-can-i-use-in-a-large-meeting"></a><span data-ttu-id="ff716-121">Q: 大規模な会議では、どのようなメディアモダリティを使用できますか?</span><span class="sxs-lookup"><span data-stu-id="ff716-121">Q: What media modalities can I use in a large meeting?</span></span>

<span data-ttu-id="ff716-122">最大1000人のユーザーとの大規模な会議には、オーディオ、ビデオ、PowerPoint 共有、ホワイトボード、プレゼンスのポーリングなどが含まれます。</span><span class="sxs-lookup"><span data-stu-id="ff716-122">Large meetings with up to 1000 users can include audio, video, PowerPoint sharing, whiteboards, and presence polling.</span></span>

</div>

<div>

## <a name="q-can-i-use-group-instant-messaging-im-in-large-meetings"></a><span data-ttu-id="ff716-123">Q: 大規模な会議でグループインスタントメッセージング (IM) を使用できますか。</span><span class="sxs-lookup"><span data-stu-id="ff716-123">Q: Can I use group instant messaging (IM) in large meetings?</span></span>

<span data-ttu-id="ff716-124">はい。</span><span class="sxs-lookup"><span data-stu-id="ff716-124">Yes.</span></span> <span data-ttu-id="ff716-125">ただし、特に多くの会議参加者によって送信されるインスタントメッセージは大量であるため、IM ウィンドウでのテキストのスクロール速度の問題により、ユーザーエクスペリエンスに影響する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ff716-125">However, large numbers of instant messages, especially when sent by a large number of meeting participants, can affect the user experience due to problems with fast text scrolling in the IM window.</span></span> <span data-ttu-id="ff716-126">最大で1000のユーザーに大量のインスタントメッセージを配信すると、サーバーの負荷が大きくなり、パフォーマンスに悪影響を及ぼす可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ff716-126">Delivering a large amount of instant messages to up to 1000 users can also introduce significant server loads, which can affect performance.</span></span> <span data-ttu-id="ff716-127">通常、IM は質問と回答にのみ必要です (Q&a \& )。</span><span class="sxs-lookup"><span data-stu-id="ff716-127">Generally, IM is only required for questions and answers (Q\&As).</span></span>

</div>

<div>

## <a name="can-users-join-large-meetings-by-dialing-in-from-a-phone"></a><span data-ttu-id="ff716-128">電話からダイヤルインすることで、ユーザーは大きな会議に参加できますか?</span><span class="sxs-lookup"><span data-stu-id="ff716-128">Can users join large meetings by dialing in from a phone?</span></span>

<span data-ttu-id="ff716-129">はい。</span><span class="sxs-lookup"><span data-stu-id="ff716-129">Yes.</span></span> <span data-ttu-id="ff716-130">Lync Server 2013 プールが正しく展開され、ダイヤルイン会議が有効になっている場合、ユーザーはダイヤルインして大人数の会議に参加することができます。</span><span class="sxs-lookup"><span data-stu-id="ff716-130">If the Lync Server 2013 pool is properly deployed and enabled for dial-in conferencing, users will be able to join the large meetings by dialing in.</span></span> <span data-ttu-id="ff716-131">このテストでは、最大15% の1000ユーザーが、10分間に大きな会議に参加できることが示されています。</span><span class="sxs-lookup"><span data-stu-id="ff716-131">Our testing has shown that up to 15% of the 1000 users can join the large meeting over a 10 minute period.</span></span>

</div>

<div>

## <a name="q-can-i-host-large-meetings-in-a-virtual-topology"></a><span data-ttu-id="ff716-132">Q: 大規模な会議を仮想トポロジでホストすることはできますか?</span><span class="sxs-lookup"><span data-stu-id="ff716-132">Q: Can I host large meetings in a virtual topology?</span></span>

<span data-ttu-id="ff716-133">仮想トポロジで大規模な会議をテストしていないため、仮想マシンを使用して大規模な会議専用のプールをホストすることはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="ff716-133">We have not tested large meetings in a virtual topology, so we do not support the use of virtual machines to host a dedicated pool for large meetings.</span></span>

<span data-ttu-id="ff716-134"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ff716-134"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

