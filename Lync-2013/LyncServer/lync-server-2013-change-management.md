---
title: 'Lync Server 2013: 変更管理'
description: 'Lync Server 2013: 変更管理'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Change management
ms:assetid: 73c774f5-c12f-4c72-be73-e07dc745b994
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720336(v=OCS.15)
ms:contentKeyID: 63969618
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 69ea019f6366528c40b60a39ca8b646b49b336b0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435127"
---
# <a name="change-management-in-lync-server-2013"></a><span data-ttu-id="7d4e7-103">Lync Server 2013 で管理を変更する</span><span class="sxs-lookup"><span data-stu-id="7d4e7-103">Change management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7d4e7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7d4e7-104">

<span> </span></span></span>

<span data-ttu-id="7d4e7-105">_**最終更新日:** 2014-08-18_</span><span class="sxs-lookup"><span data-stu-id="7d4e7-105">_**Topic Last Modified:** 2014-08-18_</span></span>

<span data-ttu-id="7d4e7-106">IT 環境の変更は避けられません。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-106">Changes to the IT environment are unavoidable.</span></span> <span data-ttu-id="7d4e7-107">変更には、新しいテクノロジ、システム、アプリケーション、ハードウェア、ツール、プロセス、および役割と責任の変化が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-107">Changes include new technologies, systems, applications, hardware, tools, processes, and changes in roles and responsibilities.</span></span> <span data-ttu-id="7d4e7-108">効率的な変更管理システムでは、サービスの中断を最小限に抑えて、IT 環境への変更をすばやく導入することができます。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-108">An effective change management system lets you introduce changes to the IT environment quickly and with minimal service disruption.</span></span> <span data-ttu-id="7d4e7-109">変更管理システムでは、システムの変更に関係するチームが集まっています。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-109">A change management system brings together the teams involved in changing a system.</span></span> <span data-ttu-id="7d4e7-110">たとえば、Office Web Apps を活用することを決定します。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-110">For example, deciding to take advantage of the Office Web Apps.</span></span> <span data-ttu-id="7d4e7-111">これは、ユーザーがブラウザーでドキュメントの読み取りや編集を行うことができる統合 Lync サービスアプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-111">This is an integrated Lync Service application that enables users to read and edit documents in a browser.</span></span> <span data-ttu-id="7d4e7-112">運用を終了した後にこのサービスを実装するには、次のように複数のチームを関与させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-112">The implementation of this service, after you have gone into production, requires the involvement of several teams:</span></span>

  - <span data-ttu-id="7d4e7-113">**チームのテスト**   このチームは、テストサーバーで Office Web Apps をロードします。このプロセスでは、想定される使用パターンと運用サーバーの期待されるパフォーマンスに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-113">**Test Team**   This team load-tests the Office Web Apps on a test server, in the process providing information about the expected usage patterns and expected performance of the production servers.</span></span>

  - <span data-ttu-id="7d4e7-114">**Lync 管理者**   このチームは、展開戦略を決定し、可能な場所でインストールをスクリプトにします。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-114">**Lync Administrators**   This team determines the deployment strategy and scripts the installation where it was possible.</span></span> <span data-ttu-id="7d4e7-115">チームは、変更が運用環境に展開されていることを確認し、その後で管理を担当します。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-115">The team is responsible for making sure that the change is deployed on the production environment, and it is responsible for administration afterward.</span></span> <span data-ttu-id="7d4e7-116">変更が運用される前に、変更の影響を理解して手順に組み込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-116">The team must understand the effect of the changes and incorporate them in procedures before the changes are put into production</span></span>

  - <span data-ttu-id="7d4e7-117">**ネットワークチーム**   このチームは、インターネットから内部の Lync プールサーバーへのアクセスを許可するファイアウォールルールの変更を担当します。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-117">**Network Team**   This team is responsible for changes to firewall rules that allow access from the Internet to the internal Lync pool servers.</span></span> <span data-ttu-id="7d4e7-118">チームは、利用可能な帯域幅が追加の負荷をサポートしているかどうかを確認するために、Lync 管理者との共同作業を担当します。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-118">The team is also responsible in working with the Lync administrators for making sure that the available bandwidth can support the additional load.</span></span>

  - <span data-ttu-id="7d4e7-119">**セキュリティチーム**   このチームはセキュリティを評価し、リスクを最小限に抑えます。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-119">**Security Team**   This team assesses security and minimizes risks.</span></span> <span data-ttu-id="7d4e7-120">セキュリティチームは既知の脆弱性を確認し、セキュリティリスクが最小化されていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-120">The security team must review known vulnerabilities and help ensure that security risks are minimized.</span></span>

  - <span data-ttu-id="7d4e7-121">**ユーザー受け入れチーム**   このチームは、システムをテストし、改善のためのフィードバックを提供するユーザーで構成されています。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-121">**User Acceptance Team**   This team is composed of users who are willing to test the system and offer feedback for improvements.</span></span>

<span data-ttu-id="7d4e7-122">変更管理プロセスでは、各チームの責任を定義し、実行される作業をスケジュールして、必要なチェックとテストを組み込むことができます。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-122">The change management process defines the responsibilities of each team and schedules the work to be performed, incorporating checks and tests where they are required.</span></span> <span data-ttu-id="7d4e7-123">コントロールを変更するかどうかは、変更の複雑さと期待される影響によって異なります。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-123">Change controls will vary depending on the complexity and expected effect of a change.</span></span> <span data-ttu-id="7d4e7-124">小規模な変更の自動承認、レビュー会議の変更、プロジェクトレベルの全レビューへの変更が可能です。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-124">They can vary from automatic approval of minor changes, to change review meetings, to full project-level reviews.</span></span> <span data-ttu-id="7d4e7-125">これについて詳しく説明するには、このセクションで変更のグループについて説明します。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-125">To explain this better, the groups of changes are discussed in this section.</span></span>

  - <span data-ttu-id="7d4e7-126">**主な変更点**   主要な変更は、システムに対してグローバル効果を持ち、さまざまなチームからの入力が必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-126">**Major Changes**   Major changes have a global effect on the system and may require input from various teams.</span></span> <span data-ttu-id="7d4e7-127">この例として、Lync Server 2013 へのアップグレードが挙げられます。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-127">An example of this is upgrading to Lync Server 2013.</span></span> <span data-ttu-id="7d4e7-128">大きな変更は、多くのチームやさまざまなシステムに影響します。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-128">Major changes affect many teams and perhaps different systems.</span></span> <span data-ttu-id="7d4e7-129">変更管理プロセスには、多くの場合、変更に関係する、または変更の影響を受けるチームに通知するために、1つ以上の変更レビュー会議が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-129">The change management process will probably include one or more change review meetings to inform the teams that will be involved in the change or be affected by the change.</span></span>

  - <span data-ttu-id="7d4e7-130">**大幅な変更**   大幅な変更を行うには、計画、構築、実装に多大なリソースが必要です。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-130">**Significant Changes**   Significant changes require significant resources to plan, build, and implement.</span></span> <span data-ttu-id="7d4e7-131">適切な変更管理が導入され、変更の効果が確実に認識されるようにし、展開手順がテストされ、ロールバックおよび不測事態対応計画が用意されていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-131">Appropriate change controls should be introduced to help make ensure that the effect of the change is understood, deployment procedures are tested, and the rollback and contingency plans are ready.</span></span> <span data-ttu-id="7d4e7-132">大幅な変更の例として、新しい累積的な更新プログラムが導入されています。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-132">An example of a significant change is deploying a new cumulative update.</span></span>

  - <span data-ttu-id="7d4e7-133">**軽微な変更**   一部の変更は、Microsoft Lync Server 2013 コントロールパネルでの特定の Lync ポリシーの変更など、IT 環境に大きな影響を与えることはありません。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-133">**Minor Changes**   Minor changes do not significantly affect the IT environment, for example, changing certain Lync policies via the Microsoft Lync Server 2013 Control Panel.</span></span>

  - <span data-ttu-id="7d4e7-134">**標準の変更点**   標準的な変更は定期的に行われ、よく理解され、文書化されています。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-134">**Standard Changes**   Standard changes are performed regularly and are well understood and documented.</span></span> <span data-ttu-id="7d4e7-135">変更管理プロセスでは、手順に対するすべての変更を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-135">The change management process should review all changes to the procedures.</span></span> <span data-ttu-id="7d4e7-136">コンテンツデータベースの作成やユーザーの追加などの定期的な変更には必要ありません。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-136">It should not be needed for routine changes like creating a content database or adding a user.</span></span>

<span data-ttu-id="7d4e7-137">次の例では、変更管理の例として、さまざまなチームがどのように連携し、新しいサービスパックが展開されたときに実行されるアクションが検査されます。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-137">The following example of change management examines how different teams interact and the actions that are performed when a new service pack is deployed.</span></span> <span data-ttu-id="7d4e7-138">これらのアクションは、変更管理プロセスによって整理および管理されます。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-138">These actions are organized and managed by the change management process.</span></span>

  - <span data-ttu-id="7d4e7-139">**変更依頼を生成する**   セキュリティチームは、最新の service pack を評価し、実働システムで発生する可能性のある脆弱性を解決することを確認しました。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-139">**Raise a change request**   The security team has assessed the latest service pack and confirmed that it resolves a possible vulnerability in the production system.</span></span> <span data-ttu-id="7d4e7-140">チームは、Lync Server を実行しているすべてのサーバーに新しい累積更新プログラムを適用するための変更要求を発生させます。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-140">The team raises a change request to have the new cumulative update applied to all servers that are running Lync Server.</span></span>

  - <span data-ttu-id="7d4e7-141">**Service pack のリリースノートのレビュー**   Lync 管理チームは、サービスパックのリリースノートを確認して、システムに対する影響を特定します。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-141">**Service pack release notes review**   The Lync administrator team reviews the service pack release notes to identify the effect on the system.</span></span>

  - <span data-ttu-id="7d4e7-142">**一連のラボテストを実施**   Lync 管理チームは、インストールされているアプリケーションやサーバーシステムに影響を与えずに、サービスパックを正常に適用できるかどうかを判断するために、テスト環境でサーバーのテスト更新を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-142">**A series of lab tests is performed**   The Lync administrator team must perform test updates on a server in a test environment to decide whether the service pack can be applied successfully without affecting any of the installed applications and server systems.</span></span> <span data-ttu-id="7d4e7-143">運用環境で Lync Server とインターフェイスするサードパーティ製または内部で作成されたアプリケーションがある場合は、それらもテストする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-143">If there are third-party or internally created applications that interface with Lync Server in a production environment, these should be also tested.</span></span> <span data-ttu-id="7d4e7-144">また、これらのテストを使って、アップグレードを実行するために必要な時間を見積もることができます。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-144">These tests can also be used to estimate the time that is required to perform the upgrades.</span></span>

  - <span data-ttu-id="7d4e7-145">**ユーザーには停止が通知される**   Lync 管理者チーム、コミュニケーションチーム、またはユーザーヘルプデスクは、計画されているメンテナンスサイクルと、サービスを利用できない期間について、影響を受けるすべてのユーザーに通知します。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-145">**Users are informed of the outage**   The Lync administrator team, communications team, or user help desk informs all affected users about the planned maintenance cycle and how long the service will be unavailable.</span></span>

  - <span data-ttu-id="7d4e7-146">**Lync の完全バックアップがアップグレード前に実行さ**   れる  サービスパックのインストールに失敗した場合、Lync 管理者チームは、元のシステム状態に戻すために使用できる有効なバックアップがあることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-146">**A full backup of Lync is performed before the upgrade**   The Lync administrator team must verify that there is a valid backup that can be used to revert to the original system state if the service pack installation fails.</span></span> <span data-ttu-id="7d4e7-147">このシステムで問題が発生した場合に、このシステムがすぐに使用できるようにするには、バックアップをスタンバイサーバーに復元することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-147">We recommend that the backup be restored to a standby server to have this system readily available if there are issues.</span></span>

  - <span data-ttu-id="7d4e7-148">**累積的な更新プログラムが展開されます**   Lync 管理チームが、計画されたメンテナンスサイクル中にインストールを実行します。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-148">**The cumulative update is deployed**   The Lync administrator team does the installation during the planned maintenance cycle.</span></span>

<div>

## <a name="managing-the-timing-of-changes"></a><span data-ttu-id="7d4e7-149">変更のタイミングを管理する</span><span class="sxs-lookup"><span data-stu-id="7d4e7-149">Managing the timing of changes</span></span>

<span data-ttu-id="7d4e7-150">変更をスケジュールするための手順を実装して、作業のセクションが重複して中断しないようにすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-150">We recommend that you implement a procedure for scheduling changes to avoid disruptions in overlapping sections of your work.</span></span> <span data-ttu-id="7d4e7-151">たとえば、2つのチームが両方ともシステムのわずかな変更を計画している可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-151">For example, two teams may both be planning a minor change to a system.</span></span> <span data-ttu-id="7d4e7-152">1つのチームが、プールに累積更新プログラムを適用している場合、別のチームがそのプールに従来のユーザーを移行している可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-152">One team may be applying a cumulative update on a pool while another team is migrating legacy users into that pool.</span></span> <span data-ttu-id="7d4e7-153">他のチームが計画している変更によって影響を受けることはありません。また、チームが計画している変更については、各チームが把握しているとは限りません。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-153">Neither team is affected by the changes that the other team is planning, and each team may not necessarily know about changes that the other team is planning.</span></span> <span data-ttu-id="7d4e7-154">両方の変更が同時に発生した場合は、変更を実装するときに問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-154">If both changes occurred at the same time, there might be issues implementing the changes.</span></span> <span data-ttu-id="7d4e7-155">また、変更が適用された後に問題が発生した場合、たとえば、ユーザーの移行が失敗した場合は、どの変更をロールバックするかを決定するのが難しい場合があります。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-155">Also, if there are issues after the changes were applied, for example, if the user migration fails, it may be difficult to decide which change should be rolled back.</span></span> <span data-ttu-id="7d4e7-156">変更をテストして承認するために、定期的なメンテナンス期間を IT と管理の間に設定しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d4e7-156">There should be regular maintenance periods set up between IT and management to test the changes and accept them.</span></span>

<span data-ttu-id="7d4e7-157"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7d4e7-157"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

