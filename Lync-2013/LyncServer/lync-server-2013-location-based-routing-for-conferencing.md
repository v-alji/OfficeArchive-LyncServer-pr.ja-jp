---
title: 'Lync Server 2013: 会議の Location-Based ルーティング'
description: 'Lync Server 2013: 会議用に Location-Based ルーティングします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Location-Based Routing for conferencing
ms:assetid: e1acb1ba-0ed2-4abf-8a7b-1ca3049e95e3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362849(v=OCS.15)
ms:contentKeyID: 56335087
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 979c835e03bbf87c9a9bf86b030cb9a8f4e138e0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426544"
---
# <a name="location-based-routing-for-conferencing-in-lync-server-2013"></a><span data-ttu-id="b7943-103">Lync Server 2013 での会議の Location-Based ルーティング</span><span class="sxs-lookup"><span data-stu-id="b7943-103">Location-Based Routing for conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b7943-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b7943-104">

<span> </span></span></span>

<span data-ttu-id="b7943-105">_**最終更新日:** 2013-07-31_</span><span class="sxs-lookup"><span data-stu-id="b7943-105">_**Topic Last Modified:** 2013-07-31_</span></span>

<span data-ttu-id="b7943-106">ルーティングを Location-Based すると、通話中の当事者の位置に基づいて、VoIP エンドポイントと PSTN エンドポイント間の通話のルーティングを制限できるようになります。</span><span class="sxs-lookup"><span data-stu-id="b7943-106">Location-Based Routing makes it possible to restrict the routing of calls between VoIP endpoints and PSTN endpoints based on the location of the parties in the call.</span></span> <span data-ttu-id="b7943-107">Lync Server 2013 の累積的な更新プログラム2では、PSTN の電話会議 (会議など) に Location-Based ルーティングルールを適用して、PSTN の有料サービスを回避することができます。</span><span class="sxs-lookup"><span data-stu-id="b7943-107">With Cumulative Update 2 of Lync Server 2013, Location-Based Routing rules can be enforced on Lync meetings (i.e. conferences) to prevent PSTN toll bypass.</span></span> <span data-ttu-id="b7943-108">アプリケーションは、参加しているユーザーの場所に基づいて Location-Based ルーティング制限を適用して、アクティブな会議を監視します。</span><span class="sxs-lookup"><span data-stu-id="b7943-108">The application monitors an active conference and enforces Location-Based Routing restrictions based on the location of users participating.</span></span> <span data-ttu-id="b7943-109">また、Location-Based ルーティング会議アプリケーションでは、PSTN エンドポイントを含む提案型転送への Location-Based ルーティングの制限の適用を有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="b7943-109">The Location-Based Routing Conferencing application additionally enables the enforcement of Location-Based Routing restrictions to consultative transfers involving PSTN endpoints.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="b7943-110">このセクション中</span><span class="sxs-lookup"><span data-stu-id="b7943-110">In This Section</span></span>

  - [<span data-ttu-id="b7943-111">Lync Server 2013 での会議の Location-Based ルーティングの概要</span><span class="sxs-lookup"><span data-stu-id="b7943-111">Overview of Location-Based Routing for conferencing in Lync Server 2013</span></span>](lync-server-2013-overview-of-location-based-routing-for-conferencing.md)

  - [<span data-ttu-id="b7943-112">Lync Server 2013 での位置情報に基づくルーティングとコンサルティングによる通話転送</span><span class="sxs-lookup"><span data-stu-id="b7943-112">Location-Based Routing and consultative call transfers in Lync Server 2013</span></span>](lync-server-2013-location-based-routing-and-consultative-call-transfers.md)

  - [<span data-ttu-id="b7943-113">Lync Server 2013 での会議の Location-Based ルーティングの要件</span><span class="sxs-lookup"><span data-stu-id="b7943-113">Requirements for Location-Based Routing for conferencing in Lync Server 2013</span></span>](lync-server-2013-requirements-for-location-based-routing-for-conferencing.md)

  - [<span data-ttu-id="b7943-114">Lync Server 2013 での会議のための場所に基づくルーティングの構成</span><span class="sxs-lookup"><span data-stu-id="b7943-114">Configuration of Location-Based Routing for conferencing in Lync Server 2013</span></span>](lync-server-2013-configuration-of-location-based-routing-for-conferencing.md)

<span data-ttu-id="b7943-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b7943-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

