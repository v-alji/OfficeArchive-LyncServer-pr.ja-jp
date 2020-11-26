---
title: Lync Server 2013 会議のロード配布
description: Lync Server 2013 会議ロード配布。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conferencing load distribution
ms:assetid: 5901a076-1b6f-4720-8837-95fc7f3c37f3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204922(v=OCS.15)
ms:contentKeyID: 48184233
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 28897b26d7351bf0ea577e2678d916aec6d15647
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434327"
---
# <a name="conferencing-load-distribution-in-lync-server-2013"></a><span data-ttu-id="af211-103">Lync Server 2013 での会議のロード配布</span><span class="sxs-lookup"><span data-stu-id="af211-103">Conferencing load distribution in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="af211-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="af211-104">

<span> </span></span></span>

<span data-ttu-id="af211-105">_**最終更新日:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="af211-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="af211-106">他のいくつかの専用会議ソリューションとは異なり、Lync Server アーキテクチャは共有ハードウェアモデルです。</span><span class="sxs-lookup"><span data-stu-id="af211-106">Unlike some other dedicated conferencing solutions, Lync Server architecture is a shared-hardware model.</span></span> <span data-ttu-id="af211-107">これは、同じハードウェアが多くのソフトウェアコンポーネントによって共有されていることを意味します。各デバイスでは、リアルタイムのさまざまな通信がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="af211-107">This means that the same hardware is shared by many software components, each of which supports different real-time communications.</span></span> <span data-ttu-id="af211-108">各種類のリアルタイム通信は、サーバーに特定の負荷をかけます。</span><span class="sxs-lookup"><span data-stu-id="af211-108">Each type of real-time communications places specific loads on the servers.</span></span> <span data-ttu-id="af211-109">たとえば、フロントエンドサーバーでは、セッション開始プロトコル (SIP) ルーティングコンポーネント、web アプリケーション (アドレス帳検索など)、Web 会議サービス、A/V 会議サービス、エンタープライズボイスアプリケーション (たとえば、会議アテンダントアプリケーションと応答グループアプリケーション)、仲介サーバーを実行できます。</span><span class="sxs-lookup"><span data-stu-id="af211-109">For example, the Front End Server can run the Session Initiation Protocol (SIP) routing components, web applications (such as Address Book search), Web Conferencing service, A/V Conferencing service, Enterprise Voice applications (for example, Conferencing Attendant application and Response Group application), and Mediation Server.</span></span> <span data-ttu-id="af211-110">フロントエンドサーバー上の一連のデータベースでは、ユーザー、連絡先、プレゼンス、会議、音声ルーティングデータに対するストレージと処理も提供されます。</span><span class="sxs-lookup"><span data-stu-id="af211-110">A set of databases on the Front End Server also provide storage and processing for user, contact, presence, conferencing, and voice routing data.</span></span> <span data-ttu-id="af211-111">このハードウェア共有、コンポーネント、サービス、プロセスが CPU とメモリリソースに競合するため、会議以外のワークロードはサーバーのスケーリングに直接影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="af211-111">With this hardware sharing, components, services, and processes compete for CPU and memory resources, so non-conferencing workloads have a direct impact on server scaling.</span></span>

<span data-ttu-id="af211-112">他のハードウェアポートベースの会議ソリューションと比べて、Lync Server 会議アーキテクチャは、非予約モデルです。</span><span class="sxs-lookup"><span data-stu-id="af211-112">Compared to other hardware port-based conferencing solutions, Lync Server conferencing architecture is a no-reservation model.</span></span> <span data-ttu-id="af211-113">ユーザーが会議をスケジュールすると、Lync Server によって会議データベース内にレコードが作成されます。会議のデータは保存されますが、スケジュールされた会議のハードウェアリソースは事前に予約されません。</span><span class="sxs-lookup"><span data-stu-id="af211-113">When a user schedules a meeting, Lync Server creates a record in the conferencing database, which stores conferencing data, but does not reserve any hardware resources for the scheduled meeting ahead of time.</span></span> <span data-ttu-id="af211-114">代わりに、Lync Server には負荷分散ロジックが組み込まれており、プール内のすべてのフロントエンドサーバー間で均等に負荷を分散するような方法で、フロントエンドサーバー上に会議リソースを動的に割り当てています。</span><span class="sxs-lookup"><span data-stu-id="af211-114">Instead, Lync Server has built-in load balancing logic to dynamically allocate conferencing resources on Front End Servers in a way that distributes loads equally across all Front End Servers in the pool.</span></span> <span data-ttu-id="af211-115">これにより、ハードウェアリソースのプロビジョニングや使用が効果的に行われますが、大規模な会議 (特に適切な計画を必要としない) のサポートが困難になります。</span><span class="sxs-lookup"><span data-stu-id="af211-115">This effectively provisions and utilizes hardware resources, but makes it challenging to support very large meetings (especially without appropriate planning).</span></span> <span data-ttu-id="af211-116">たとえば、Lync Server 2013 プールが最上位の容量に近い状態で実行されている場合、各フロントエンドサーバーは約125の平均サイズの会議をホストしている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="af211-116">For example, when a Lync Server 2013 pool is running close to its top capacity, each Front End Server might host approximately 125 average-size meetings.</span></span> <span data-ttu-id="af211-117">別の小規模な会議を追加しても問題はありませんが、1,000 ユーザーの会議を追加した場合、フロントエンド サーバーは他の 125 件の会議と同時にこのような大規模な会議をサポートできない可能性が高いため、問題が発生します。</span><span class="sxs-lookup"><span data-stu-id="af211-117">Adding another small meeting would not be a problem, but adding a meeting for 1000 users would be a problem because the Front End Servers would probably not be able to support such a large meeting at the same time as the other 125 meetings.</span></span>

<span data-ttu-id="af211-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="af211-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

