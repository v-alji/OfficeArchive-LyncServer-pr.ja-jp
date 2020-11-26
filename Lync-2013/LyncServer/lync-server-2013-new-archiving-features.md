---
title: 'Lync Server 2013: アーカイブの新機能'
description: 'Lync Server 2013: 新しいアーカイブ機能。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New Archiving features
ms:assetid: c002e367-41ad-498d-9d23-8b117ac435b2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205225(v=OCS.15)
ms:contentKeyID: 48185288
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b5b69c90e62914284f178ae328375c6e350f5b3e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425164"
---
# <a name="new-archiving-features-in-lync-server-2013"></a><span data-ttu-id="f6636-103">Lync Server 2013 のアーカイブの新機能</span><span class="sxs-lookup"><span data-stu-id="f6636-103">New Archiving features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f6636-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f6636-104">

<span> </span></span></span>

<span data-ttu-id="f6636-105">_**最終更新日:** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="f6636-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="f6636-106">Lync Server 2013 でアーカイブすると、次の種類のコンテンツをアーカイブできます。</span><span class="sxs-lookup"><span data-stu-id="f6636-106">Archiving in Lync Server 2013 can archive the following types of content:</span></span>

  - <span data-ttu-id="f6636-107">ピアツーピアのインスタント メッセージ</span><span class="sxs-lookup"><span data-stu-id="f6636-107">Peer-to-peer instant messages</span></span>

  - <span data-ttu-id="f6636-108">マルチパーティのインスタントメッセージである会議 (会議)</span><span class="sxs-lookup"><span data-stu-id="f6636-108">Conferences (meetings) that are multi-party instant messages</span></span>

  - <span data-ttu-id="f6636-109">アップロードされたコンテンツ (配付資料など) およびイベント関連のコンテンツ (参加、退席、アップロード、共有、表示設定の変更など) を含む会議コンテンツ</span><span class="sxs-lookup"><span data-stu-id="f6636-109">Conference content, including uploaded content (for example, handouts) and event-related content (for example, joining, leaving, uploading sharing, and changes in visibility)</span></span>

<span data-ttu-id="f6636-110">さらに、Lync Server 2013 でアーカイブすると、展開と運用の効率を向上させるための新機能が提供されます。</span><span class="sxs-lookup"><span data-stu-id="f6636-110">Additionally, Archiving in Lync Server 2013 provides new features that improve deployment and operations efficiency.</span></span> <span data-ttu-id="f6636-111">次の新機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f6636-111">These new features consist of:</span></span>

  - <span data-ttu-id="f6636-112">**フロントエンドサーバー上のアーカイブの collocation。**</span><span class="sxs-lookup"><span data-stu-id="f6636-112">**Collocation of Archiving on Front End Servers.**</span></span>   <span data-ttu-id="f6636-113">Lync Server 2013 には、別のアーカイブサーバーの役割がありません。</span><span class="sxs-lookup"><span data-stu-id="f6636-113">Lync Server 2013 does not have a separate Archiving Server role.</span></span> <span data-ttu-id="f6636-114">アーカイブは、Enterprise Edition の展開におけるすべてのフロントエンドサーバーと、プールまたはサイト用に構成できる標準エディションのサーバーで利用できるオプションの機能です。</span><span class="sxs-lookup"><span data-stu-id="f6636-114">Archiving is an optional feature available on all Front End Servers in an Enterprise Edition deployment, and on Standard Edition servers, that can be implemented configured for a pool or a site.</span></span>

  - <span data-ttu-id="f6636-115">**Microsoft Exchange の統合。**</span><span class="sxs-lookup"><span data-stu-id="f6636-115">**Microsoft Exchange integration.**</span></span>   <span data-ttu-id="f6636-116">アーカイブを展開するときに、Exchange 2013 を使用しているすべてのユーザーに対して、既存の Exchange 2013 ストレージを使ってアーカイブ用のデータストレージを統合することができます。そのため、メールボックスは In-Place 保留にしておく必要があります。そのため、別の SQL Server データベースを展開して Lync データをアーカイブする必要はありませ</span><span class="sxs-lookup"><span data-stu-id="f6636-116">When you deploy Archiving, you can integrate data storage for Archiving with your existing Exchange 2013 storage for all users who are homed on Exchange 2013 and have their mailboxes put on In-Place Hold, so you don’t need to deploy separate SQL Server databases to archive Lync data.</span></span> <span data-ttu-id="f6636-117">Exchange 2013 を展開していない場合、または統合しない場合、または、Exchange 2013 を使用していない Lync 2013 ユーザーが In-Place 保留になっている場合は、SQL Server を使って、アーカイブデータを Lync コミュニケーションから保存することで、個別のアーカイブデータベースを展開できます。</span><span class="sxs-lookup"><span data-stu-id="f6636-117">If you do not have an Exchange 2013 deployment, or if you prefer not to integrate with it, or if you have any Lync 2013 users who are not homed on Exchange 2013 with their mailboxes put on In-Place Hold, you can deploy separate Archiving databases by using SQL Server to store archived data from Lync communications.</span></span> <span data-ttu-id="f6636-118">Microsoft exchange 統合と Lync Server 2013 アーカイブデータベースの両方を使用できますが、展開内のすべてのユーザーに対して、Microsoft Exchange 統合を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="f6636-118">You can use both Microsoft Exchange integration and Lync Server 2013 Archiving databases if you want to use Microsoft Exchange integration for some but not all users in your deployment.</span></span> <span data-ttu-id="f6636-119">In-Place ホールドの詳細については、「インプレースホールド」を参照してください [https://go.microsoft.com/fwlink/p/?LinkId=267500](https://go.microsoft.com/fwlink/p/?linkid=267500) 。</span><span class="sxs-lookup"><span data-stu-id="f6636-119">For details about In-Place Hold, see “In-Place Hold” at [https://go.microsoft.com/fwlink/p/?LinkId=267500](https://go.microsoft.com/fwlink/p/?linkid=267500).</span></span>

  - <span data-ttu-id="f6636-120">**SQL ストアのミラーリング。**</span><span class="sxs-lookup"><span data-stu-id="f6636-120">**SQL Store Mirroring.**</span></span>   <span data-ttu-id="f6636-121">アーカイブを展開するときに、アーカイブデータベースに対して SQL Server データベースのミラーリングを有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="f6636-121">When you deploy Archiving, you can enable SQL Server database mirroring for your Archiving database.</span></span>

  - <span data-ttu-id="f6636-122">**ホワイトボードと投票のアーカイブ。**</span><span class="sxs-lookup"><span data-stu-id="f6636-122">**Archiving of Whiteboards and Polls.**</span></span>   <span data-ttu-id="f6636-123">アーカイブされた会議コンテンツには、会議中に共有されるホワイトボードと投票が含まれるようになりました。</span><span class="sxs-lookup"><span data-stu-id="f6636-123">Archived conference content now includes whiteboards and polls that are shared during the meeting.</span></span>

<span data-ttu-id="f6636-124">次の種類のコンテンツはアーカイブされません。</span><span class="sxs-lookup"><span data-stu-id="f6636-124">The following types of content are not archived:</span></span>

  - <span data-ttu-id="f6636-125">ピアツーピアのファイル転送</span><span class="sxs-lookup"><span data-stu-id="f6636-125">Peer-to-peer file transfers</span></span>

  - <span data-ttu-id="f6636-126">ピアツーピアのインスタント メッセージおよび会議の音声ビデオ</span><span class="sxs-lookup"><span data-stu-id="f6636-126">Audio/video for peer-to-peer instant messages and conferences</span></span>

  - <span data-ttu-id="f6636-127">ピアツーピアインスタントメッセージ (im) と会議のアプリケーション共有</span><span class="sxs-lookup"><span data-stu-id="f6636-127">Application sharing for peer-to-peer instant messages and conferences</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="f6636-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="f6636-128">See Also</span></span>


[<span data-ttu-id="f6636-129">Lync Server 2013 のアーカイブの計画</span><span class="sxs-lookup"><span data-stu-id="f6636-129">Planning for Archiving in Lync Server 2013</span></span>](lync-server-2013-planning-for-archiving.md)  
  

<span data-ttu-id="f6636-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f6636-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

