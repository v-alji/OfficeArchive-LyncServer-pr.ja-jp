---
title: Office Communications Server 2007 R2 から Lync Server 2013 への移行
description: Office Communications Server 2007 R2 から Lync Server 2013 に移行します。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migration from Office Communications Server 2007 R2 to Lync Server 2013
ms:assetid: f3fa4f5f-e9a2-4fb7-a12d-20f04173e697
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205375(v=OCS.15)
ms:contentKeyID: 48185802
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d0afdc754ae691bc674c200addb9fb97c1eb4199
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446150"
---
# <a name="migration-from-office-communications-server-2007-r2-to-lync-server-2013"></a><span data-ttu-id="96f52-103">Office Communications Server 2007 R2 から Lync Server 2013 への移行</span><span class="sxs-lookup"><span data-stu-id="96f52-103">Migration from Office Communications Server 2007 R2 to Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="96f52-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="96f52-104">

<span> </span></span></span>

<span data-ttu-id="96f52-105">_**最終更新日:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="96f52-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="96f52-106">このセクションのトピックでは、Office Communications Server 2007 R2 から Lync Server 2013 への移行プロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="96f52-106">The topics in this section guide you through the process of migrating from Office Communications Server 2007 R2 to Lync Server 2013</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="96f52-107">このドキュメントでは、移行の各フェーズを実行するために必要な手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="96f52-107">This document describes the steps generally required to accomplish each phase of migration.</span></span> <span data-ttu-id="96f52-108">これは、すべてのレガシ展開トポロジまたは可能な移行シナリオには対応していません。</span><span class="sxs-lookup"><span data-stu-id="96f52-108">It does not address every possible legacy deployment topology or every possible migration scenario.</span></span> <span data-ttu-id="96f52-109">このため、説明されている手順をすべて実行する必要がない場合や、展開によっては追加の手順を実行する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="96f52-109">Therefore, you may not need to perform every step described, or you may need to perform additional steps, depending on your deployment.</span></span> <span data-ttu-id="96f52-110">このドキュメントでは、確認手順の例についても説明します。</span><span class="sxs-lookup"><span data-stu-id="96f52-110">This document also provides examples of verification steps.</span></span> <span data-ttu-id="96f52-111">この確認手順は、移行の進行に合わせて各フェーズが正常に完了するために必要な情報を確認するために用意されています。</span><span class="sxs-lookup"><span data-stu-id="96f52-111">These verification steps are provided to help you understand what you need to look for to ensure that each phase completes successfully as you progress through your migration.</span></span> <span data-ttu-id="96f52-112">この確認手順は、特定の移行プロセスに合わせて調整してください。</span><span class="sxs-lookup"><span data-stu-id="96f52-112">Tailor these verification steps to your specific migration process.</span></span>



</div>

<span data-ttu-id="96f52-113">このガイドには、既存の展開のアップグレードに固有の情報が記載されています。</span><span class="sxs-lookup"><span data-stu-id="96f52-113">This guide provides information specific to upgrading your existing deployment.</span></span> <span data-ttu-id="96f52-114">既存のトポロジを変更する方法については説明しません。</span><span class="sxs-lookup"><span data-stu-id="96f52-114">It does not explain how to change your existing topology.</span></span> <span data-ttu-id="96f52-115">このガイドでは、新機能の実装については説明しません。</span><span class="sxs-lookup"><span data-stu-id="96f52-115">This guide does not cover the implementation of new features.</span></span> <span data-ttu-id="96f52-116">詳細な手順については、別のドキュメントまたはドキュメントの説明を参照してください。</span><span class="sxs-lookup"><span data-stu-id="96f52-116">When a detailed procedure is documented elsewhere, this guide directs you to the appropriate document or document section.</span></span>

<span data-ttu-id="96f52-117">このドキュメントでは、次の一覧で指定された用語を定義しています。</span><span class="sxs-lookup"><span data-stu-id="96f52-117">This document defines terms as specified in the following list.</span></span>

  - <span data-ttu-id="96f52-118">*用*</span><span class="sxs-lookup"><span data-stu-id="96f52-118">*migration*</span></span>  
    <span data-ttu-id="96f52-119">以前のバージョンの Office Communications Server 2007 R2 から Lync Server 2013 に運用環境の展開を移行します。</span><span class="sxs-lookup"><span data-stu-id="96f52-119">Moving your production deployment from a previous version of Office Communications Server 2007 R2 to Lync Server 2013.</span></span>

<!-- end list -->

  - <span data-ttu-id="96f52-120">*アップグレード*</span><span class="sxs-lookup"><span data-stu-id="96f52-120">*upgrade*</span></span>  
    <span data-ttu-id="96f52-121">新しいバージョンのソフトウェアをサーバーまたはクライアントコンピューターにインストールします。</span><span class="sxs-lookup"><span data-stu-id="96f52-121">Installing a newer version of software on a server or client computer.</span></span>

<!-- end list -->

  - <span data-ttu-id="96f52-122">*共存*</span><span class="sxs-lookup"><span data-stu-id="96f52-122">*coexistence*</span></span>  
    <span data-ttu-id="96f52-123">一部の機能が Lync Server 2013 に移行されていて、その他の機能が以前のバージョンの Office Communications Server 2007 R2 上に残っている場合に、移行中に存在する一時的な環境。</span><span class="sxs-lookup"><span data-stu-id="96f52-123">The temporary environment that exists during migration when some functionality has been migrated to Lync Server 2013 and other functionality still remains on a prior version of Office Communications Server 2007 R2.</span></span>

<!-- end list -->

  - <span data-ttu-id="96f52-124">*運用性*</span><span class="sxs-lookup"><span data-stu-id="96f52-124">*interoperability*</span></span>  
    <span data-ttu-id="96f52-125">共存期間中に展開が正常に動作する能力。</span><span class="sxs-lookup"><span data-stu-id="96f52-125">The ability of your deployment to operate successfully during the period of coexistence.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="96f52-126">このセクション中</span><span class="sxs-lookup"><span data-stu-id="96f52-126">In This Section</span></span>

  - [<span data-ttu-id="96f52-127">移行を始める前に</span><span class="sxs-lookup"><span data-stu-id="96f52-127">Before you begin the migration</span></span>](before-you-begin-the-migration.md)

  - [<span data-ttu-id="96f52-128">移行のフェーズ</span><span class="sxs-lookup"><span data-stu-id="96f52-128">Migration phases</span></span>](migration-phases.md)

  - [<span data-ttu-id="96f52-129">フェーズ 1: Office Communications Server 2007 R2 からの移行を計画する</span><span class="sxs-lookup"><span data-stu-id="96f52-129">Phase 1: Plan your migration from Office Communications Server 2007 R2</span></span>](phase-1-plan-your-migration-from-office-communications-server-2007-r2.md)

  - [<span data-ttu-id="96f52-130">フェーズ 2: 移行の準備</span><span class="sxs-lookup"><span data-stu-id="96f52-130">Phase 2: Prepare for migration</span></span>](phase-2-prepare-for-migration.md)

  - [<span data-ttu-id="96f52-131">フェーズ 3: Lync Server 2013 パイロットプールの展開</span><span class="sxs-lookup"><span data-stu-id="96f52-131">Phase 3: Deploy Lync Server 2013 pilot pool</span></span>](phase-3-deploy-lync-server-2013-pilot-pool.md)

  - [<span data-ttu-id="96f52-132">フェーズ 4: トポロジの結合</span><span class="sxs-lookup"><span data-stu-id="96f52-132">Phase 4: Merge topologies</span></span>](phase-4-merge-topologies.md)

  - [<span data-ttu-id="96f52-133">フェーズ 5: パイロットプールを構成する</span><span class="sxs-lookup"><span data-stu-id="96f52-133">Phase 5: Configure the pilot pool</span></span>](phase-5-configure-the-pilot-pool.md)

  - [<span data-ttu-id="96f52-134">フェーズ 6: ユーザーをパイロットプールに移動する</span><span class="sxs-lookup"><span data-stu-id="96f52-134">Phase 6: Move users to the pilot pool</span></span>](phase-6-move-users-to-the-pilot-pool.md)

  - [<span data-ttu-id="96f52-135">フェーズ 7: Lync Server 2013 エッジサーバーをパイロットプールに追加する</span><span class="sxs-lookup"><span data-stu-id="96f52-135">Phase 7: Add Lync Server 2013 Edge Server to pilot pool</span></span>](phase-7-add-lync-server-2013-edge-server-to-pilot-pool.md)

  - [<span data-ttu-id="96f52-136">フェーズ 8: パイロット展開から実稼働への移行</span><span class="sxs-lookup"><span data-stu-id="96f52-136">Phase 8: Move from pilot deployment into production</span></span>](phase-8-move-from-pilot-deployment-into-production.md)

  - [<span data-ttu-id="96f52-137">フェーズ 9: 移行後のタスクを完了する</span><span class="sxs-lookup"><span data-stu-id="96f52-137">Phase 9: Complete post-migration tasks</span></span>](phase-9-complete-post-migration-tasks.md)

  - [<span data-ttu-id="96f52-138">フェーズ 10: レガシサイトの廃止</span><span class="sxs-lookup"><span data-stu-id="96f52-138">Phase 10: Decommission legacy site</span></span>](phase-10-decommission-legacy-site.md)

<span data-ttu-id="96f52-139"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="96f52-139"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

