---
title: Lync Server 2013 会議のユーザーモデル
description: Lync Server 2013 会議のユーザーモデル。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: The conferencing user model
ms:assetid: ba4bbba9-f2e3-4cab-8eba-b51f12133cab
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205199(v=OCS.15)
ms:contentKeyID: 48185229
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 699f41303b82f4d8fd2864cbf1b29a1c601b826e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434280"
---
# <a name="the-conferencing-user-model-in-lync-server-2013"></a><span data-ttu-id="6bc83-103">Lync Server 2013 の会議ユーザーモデル</span><span class="sxs-lookup"><span data-stu-id="6bc83-103">The conferencing user model in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6bc83-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6bc83-104">

<span> </span></span></span>

<span data-ttu-id="6bc83-105">_**最終更新日:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="6bc83-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="6bc83-106">Lync Server 会議のユーザーモデルの重要な部分は、会議のサイズです。</span><span class="sxs-lookup"><span data-stu-id="6bc83-106">A critical part of the Lync Server conferencing user model is meeting size.</span></span> <span data-ttu-id="6bc83-107">(前のセクションで説明したように) 複数のデータポイントからデータを収集した後、次のことを決定しました。</span><span class="sxs-lookup"><span data-stu-id="6bc83-107">After collecting data from the multiple data points (as described in the previous section), we determined the following:</span></span>

  - <span data-ttu-id="6bc83-108">ほとんどの会議は、実際にはわずか 4 ~ 6 人の参加者が開催する、共同作業の小さな会議です。</span><span class="sxs-lookup"><span data-stu-id="6bc83-108">Most meetings are actually small collaborative meetings with an average of four to six participants</span></span>

  - <span data-ttu-id="6bc83-109">会議の約80% は、参加者が20人を超えています。</span><span class="sxs-lookup"><span data-stu-id="6bc83-109">Approximately 80 percent of meetings have fewer than 20 participants.</span></span>

  - <span data-ttu-id="6bc83-110">会議の99.98% は、参加者数が100を超えています。</span><span class="sxs-lookup"><span data-stu-id="6bc83-110">99.98 percent of meetings have fewer than 100 participants.</span></span>

<span data-ttu-id="6bc83-111">会議のサイズに加えて、会議のユーザーモデルでは、次のようなさまざまな要因も考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6bc83-111">In addition to meeting size, the conferencing user model also takes into account a variety of factors, such as:</span></span>

  - <span data-ttu-id="6bc83-112">**同時会議**   同時に会議には何人のユーザーがいますか?</span><span class="sxs-lookup"><span data-stu-id="6bc83-112">**Concurrent meetings**   How many users are expected to be in meetings at the same time?</span></span>

  - <span data-ttu-id="6bc83-113">**メディアミックス**   会議でユーザーによって使用されるメディアの種類は何ですか。</span><span class="sxs-lookup"><span data-stu-id="6bc83-113">**Media mix**   What types of media are available and expected to be used by users in meetings?</span></span>

  - <span data-ttu-id="6bc83-114">**ユーザーの種類**   ユーザーは、内部ユーザー、リモートユーザー、フェデレーションユーザー、匿名ユーザーのいずれですか。</span><span class="sxs-lookup"><span data-stu-id="6bc83-114">**User types**   Are users internal users, remote users, federated users, or anonymous users?</span></span>

  - <span data-ttu-id="6bc83-115">**会議のランプアップ時間**   会議のすべてのユーザーが会議に参加するには、どのくらいの時間がかかりますか?</span><span class="sxs-lookup"><span data-stu-id="6bc83-115">**Meeting ramp up time**   How long does it take for all users of a meeting to join a meeting?</span></span>

<span data-ttu-id="6bc83-116">ユーザーモデルの詳細については、「 [Lync Server 2013 のユーザーモデル](lync-server-2013-user-models.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6bc83-116">For details about the user model, see [User models in Lync Server 2013](lync-server-2013-user-models.md).</span></span>

<span data-ttu-id="6bc83-117">テストに使用する会議とユーザーの数を決定するには、次の操作を行いました。</span><span class="sxs-lookup"><span data-stu-id="6bc83-117">To determine the number of meetings and users to use for testing, we did the following:</span></span>

  - <span data-ttu-id="6bc83-118">組織内のユーザーの合計数を取得しました (たとえば、8万ユーザー)。会議の同時実行率 (たとえば、すべてのユーザーの 5%) によって、同時に会議に予定されているユーザーの合計数 (この例では、4000ユーザー) を求めています。</span><span class="sxs-lookup"><span data-stu-id="6bc83-118">Took the total number of users in an organization (for example, 80,000 users) and multiplied it by the meeting concurrency rate (for example, 5% of all users) to determine the total number of users expected to be in meetings at the same time (in this example, 4000 users).</span></span>

  - <span data-ttu-id="6bc83-119">フロントエンドサーバーあたりの会議出席者の推定数 (この例では、フロントエンドサーバーあたり500ユーザー) を決定するために、ユーザーの合計数を、展開の Lync Server 2013、フロントエンドサーバー (たとえば、8台) で割ります。</span><span class="sxs-lookup"><span data-stu-id="6bc83-119">Divided the total number of users by the number of Lync Server 2013, Front End Servers in the deployment (for example, 8 servers) to determine the estimated number of meeting participants per Front End Server (in this example, 500 users per Front End Server).</span></span>

  - <span data-ttu-id="6bc83-120">フロントエンドサーバーあたりのユーザー数を平均会議のサイズ (たとえば、4人のユーザー) で割って、フロントエンドサーバーあたりの会議の推定平均数 (この例では、フロントエンドサーバーあたり125会議) を決定します。</span><span class="sxs-lookup"><span data-stu-id="6bc83-120">Divided the number of users per Front End Server by the average meeting size (for example, 4 users) to determine the estimated average number of meetings per Front End Server (in this example, 125 meetings per Front End Server).</span></span>

  - <span data-ttu-id="6bc83-121">各フロントエンドサーバーでメディアのロードを1つずつ取得するために、メディアミックスを見積もりました。</span><span class="sxs-lookup"><span data-stu-id="6bc83-121">To get the per media load on each Front End Server, we estimated the media mix.</span></span> <span data-ttu-id="6bc83-122">たとえば、会議の75% が必要なのは、音声サポートだけでなく、会議の50% ではアプリケーション共有が必要であると想定した場合、47会議と188ユーザーは、各フロントエンドサーバーに同時に接続して、アプリケーション共有を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="6bc83-122">For example, assuming that 75% of the meetings require more than just audio support and 50% of those meetings require application sharing, an average of 47 meetings and 188 users connect concurrently to each Front End Server for application sharing.</span></span>

  - <span data-ttu-id="6bc83-123">サーバーのスケーラビリティを確保するために、さまざまな会議サイズ (共有プールの最大250ユーザーのユーザーモデルに基づく) をテストしました。</span><span class="sxs-lookup"><span data-stu-id="6bc83-123">Tested a variety of meeting sizes (based our user model of up to 250 users in a shared pool) to ensure server scalability.</span></span>

<span data-ttu-id="6bc83-124"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6bc83-124"></div>

<span> </span>

</div>

</div>

</span></span></div>

