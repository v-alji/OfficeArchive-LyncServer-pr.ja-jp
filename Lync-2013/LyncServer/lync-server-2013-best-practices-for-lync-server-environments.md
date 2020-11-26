---
title: 'Lync Server 2013: Lync Server 環境のベストプラクティス'
description: 'Lync Server 2013: Lync Server 環境のベストプラクティス'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Best practices for Lync Server environments
ms:assetid: b0e45d84-09c8-4d3e-aad0-bc6f34ce233b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720348(v=OCS.15)
ms:contentKeyID: 63969642
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ae6c02621bd6506d2a1d379aeaf92b20ce3f7ae1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436063"
---
# <a name="best-practices-for-lync-server-2013-environments"></a><span data-ttu-id="8682b-103">Lync Server 2013 環境のベストプラクティス</span><span class="sxs-lookup"><span data-stu-id="8682b-103">Best practices for Lync Server 2013 environments</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8682b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8682b-104">

<span> </span></span></span>

<span data-ttu-id="8682b-105">_**最終更新日:** 2014-08-04_</span><span class="sxs-lookup"><span data-stu-id="8682b-105">_**Topic Last Modified:** 2014-08-04_</span></span>

<span data-ttu-id="8682b-106">システムの実行中の操作には、次の一般的な原則を適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8682b-106">The following general principles should be applied to ongoing operations of your system:</span></span>

  - <span data-ttu-id="8682b-107">**MOF を理解して使用**   する  MOF は、日常の Lync Server 2013 の運用など、IT 資産の管理に関する組織の技術ガイダンスを提供するベストプラクティス、原則、およびモデルの集まりです。</span><span class="sxs-lookup"><span data-stu-id="8682b-107">**Understand and utilize MOF**   MOF is a collection of best practices, principles, and models that provide organizations technical guidance about the management of IT assets, such as daily Lync Server 2013 operations.</span></span> <span data-ttu-id="8682b-108">MOF ガイドラインは、次のように、Microsoft 製品のミッションクリティカルな生産システムの信頼性、可用性、サポート性、および管理性を実現するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="8682b-108">Following MOF guidelines can help you achieve mission-critical production system reliability, availability, supportability, and manageability for Microsoft products.</span></span> <span data-ttu-id="8682b-109">詳細については、「 [Microsoft Operations Framework 4.0](https://go.microsoft.com/fwlink/p/?linkid=40939)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8682b-109">For more information, see [Microsoft Operations Framework 4.0](https://go.microsoft.com/fwlink/p/?linkid=40939).</span></span>

  - <span data-ttu-id="8682b-110">**Lync Server 2013 のベストプラクティスについて**   Lync Server 2013 を管理するための実用的で実証された手順を実装することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="8682b-110">**Learn about best practices for Lync Server 2013**   We recommend that you implement practical and proven procedures to manage Lync Server 2013.</span></span> <span data-ttu-id="8682b-111">試用、テスト、文書化された操作を管理する方法は、独自のメソッドを開発する場合よりも効率的に行うことができます。</span><span class="sxs-lookup"><span data-stu-id="8682b-111">By using tried, tested, and documented methods of managing operations may be more efficient than developing your own methods.</span></span>

  - <span data-ttu-id="8682b-112">**個別の操作を日単位、週単位、月単位のプロセスに分ける**   定期的に実行する必要のある運用タスクを文書化します。</span><span class="sxs-lookup"><span data-stu-id="8682b-112">**Separate operations into daily, weekly, and monthly processes**   Document the required operational tasks that you'll regularly perform.</span></span> <span data-ttu-id="8682b-113">タスクの実行方法を文書化することで、新しいテクノロジが展開された、またはスタッフが変更されたときなど、運用環境に変更があった場合に、情報が確実に保持されるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="8682b-113">Documenting how you perform tasks helps make sure that your information is preserved when there is a change in your operational environment such as when new technologies are deployed or staff changes occur.</span></span> <span data-ttu-id="8682b-114">タスクが毎日、毎週、毎月実行される管理可能なワークロードに、運用タスクを分けることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="8682b-114">We recommend that operational tasks be separated into manageable workloads where tasks are performed daily, weekly, and monthly.</span></span> <span data-ttu-id="8682b-115">日常的な作業では、システムの機能に重点を置いています。また、毎月のタスクでは、システムの長期の正常性を確保することに重点を置いています。</span><span class="sxs-lookup"><span data-stu-id="8682b-115">Daily tasks would focus efforts on the functioning of a system, and monthly tasks would focus more on ensuring the long-term health of a system.</span></span>
    
    <span data-ttu-id="8682b-116">このドキュメントは、エンタープライズ Voip でインスタントメッセージ/プレゼンス (IM/P) コンポーネントまたは IM/P を展開する環境で使用できます。</span><span class="sxs-lookup"><span data-stu-id="8682b-116">This document can be used in environments deploying only instant messaging/presence (IM/P) components or IM/P with Enterprise Voice.</span></span> <span data-ttu-id="8682b-117">タスクまたはチェックリスト項目がエンタープライズ Voip に固有の場合、これが説明されています。また、環境にエンタープライズ Voip が含まれていない場合は、その部分がスキップされる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8682b-117">When tasks or checklist items are specific to Enterprise Voice, this is mentioned and if your environment does not include Enterprise Voice the portion may be skipped.</span></span>

  - <span data-ttu-id="8682b-118">**Lync Server のオペレーティングシステムに必要なツールを展開する 2013**   問題のトラブルシューティング、タスクの自動化、Lync Server 2013 環境の監視と維持に役立つツールが数多くあります。</span><span class="sxs-lookup"><span data-stu-id="8682b-118">**Deploy the tools that are required for operating Lync Server 2013**   Many tools are available to help troubleshoot issues, automate tasks, and help monitor and maintain the Lync Server 2013 environment.</span></span> <span data-ttu-id="8682b-119">運営チームによって実行されるタスクを正確かつ効率的に実行し、管理された方法で実行するために、組織用に標準のツールセットを定義します。</span><span class="sxs-lookup"><span data-stu-id="8682b-119">Define a standard set of tools for your organization so the tasks that are performed by the operations team are performed accurately, efficiently, consistently, and in a controlled manner.</span></span> <span data-ttu-id="8682b-120">また、インシデントおよび主要構成の変更を追跡するプロセスも実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8682b-120">You should also implement processes to track incidents and major configuration changes.</span></span>

<div>

## <a name="reference"></a><span data-ttu-id="8682b-121">Reference</span><span class="sxs-lookup"><span data-stu-id="8682b-121">Reference</span></span>

<span data-ttu-id="8682b-122">一般的にサーバー管理の基本について理解していない読者のために、ここではサーバー管理のプラクティスの概要について説明します。</span><span class="sxs-lookup"><span data-stu-id="8682b-122">For the benefit of readers not already familiar with the basics of server management in general, we provide an overview of server management practices.</span></span> <span data-ttu-id="8682b-123">既にサーバー管理に慣れている読者は、このセクションをスキップすることができます。</span><span class="sxs-lookup"><span data-stu-id="8682b-123">Readers already familiar with server management may choose to skip this section.</span></span>

<span data-ttu-id="8682b-124">ベストプラクティスとは、IT プロフェッショナルが多くの環境で得た知識と経験に基づいた推奨事項です。</span><span class="sxs-lookup"><span data-stu-id="8682b-124">Best practices are recommendations that are based on the knowledge and experience that IT professionals have gained across many environments.</span></span> <span data-ttu-id="8682b-125">Lync Server の管理者が日常的に実行する必要のある一般的なタスクの標準的な手順と、Lync Server 環境を管理するために使う必要のあるツールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="8682b-125">They provide standard procedures for typical tasks that your Lync Server administrators must perform daily, and list the tools that they should use to manage a Lync Server environment.</span></span>

<span data-ttu-id="8682b-126">Lync 管理者向けの一般的なタスクには、次のものがあります。</span><span class="sxs-lookup"><span data-stu-id="8682b-126">Typical tasks for Lync administrators include the following:</span></span>

  - <span data-ttu-id="8682b-127">**容量と可用性の管理**   今後の容量要件を予測し、システムの容量、信頼性、および可用性に関するレポートを作成する方法と測定内容を定義します。</span><span class="sxs-lookup"><span data-stu-id="8682b-127">**Capacity and Availability Management**   Define how and what to measure to predict future capacity requirements and to report about the capacity, reliability, and availability of your systems.</span></span> <span data-ttu-id="8682b-128">Lync Server を実行しているサーバーがシステムの負荷を処理するように設定されていること、および予期しないダウンタイムがサービスレベル契約 (SLA) で定義されているレベルの下にあることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8682b-128">You must verify that servers that are running Lync Server are sized to handle the load on the system, and that unplanned downtime is kept under the levels defined in the service level agreement (SLA).</span></span> <span data-ttu-id="8682b-129">さらに、定義された要件を引き続き満たすためには、ハードウェアをアップグレードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8682b-129">Additionally, you'll have to upgrade hardware to continue to meet the defined requirements.</span></span>

  - <span data-ttu-id="8682b-130">**管理と構成の管理を変更**   する  IT システムに対する変更を制御します。</span><span class="sxs-lookup"><span data-stu-id="8682b-130">**Change Management and Configuration Management**   Control how changes are made to IT systems.</span></span> <span data-ttu-id="8682b-131">これには、テスト、アプリケーションのフィードバックと不測事態対応の計画、すべての変更の文書化、問題が発生した場合の管理からの承認などが含まれます。</span><span class="sxs-lookup"><span data-stu-id="8682b-131">This should include testing, application feedback and contingency plans, documentation of all changes, and approval from management if issues occur.</span></span> <span data-ttu-id="8682b-132">ソフトウェアとハードウェアの資産とその構成を記録しておきます。</span><span class="sxs-lookup"><span data-stu-id="8682b-132">Keep a record of your software and hardware assets and their configurations.</span></span>

  - <span data-ttu-id="8682b-133">**システム管理**   データベース管理やサイト管理などの管理タスクを実行するための標準的な方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8682b-133">**System Administration**   Outline standard methods for doing administrative tasks such as database administration and site administration.</span></span>

  - <span data-ttu-id="8682b-134">**セキュリティ管理**   IT インフラストラクチャのデータの機密性、データの整合性、データの可用性を保護するための詳細なポリシーと計画を立てます。</span><span class="sxs-lookup"><span data-stu-id="8682b-134">**Security Administration**   Have a detailed policy and plan that protects data confidentiality, data integrity, and data availability of the IT infrastructure.</span></span> <span data-ttu-id="8682b-135">これには、IT セキュリティインフラストラクチャの維持と調整に関連する日常的なアクティビティとタスクが含まれます。</span><span class="sxs-lookup"><span data-stu-id="8682b-135">This includes day-to-day activities and tasks that are related to maintaining and adjusting the IT security infrastructure.</span></span>

  - <span data-ttu-id="8682b-136">**システムのトラブルシューティング**   将来の問題を回避するための手順など、予期しない問題を処理するためのアウトライン方法。</span><span class="sxs-lookup"><span data-stu-id="8682b-136">**System Troubleshooting**   Outline methods for dealing with unexpected issues, including steps to prevent similar issues in the future.</span></span>

  - <span data-ttu-id="8682b-137">**サービスレベル契約**   IT システムのパフォーマンスに関する一連の目標を維持し、これらの目標に対するパフォーマンスを定期的に測定します。</span><span class="sxs-lookup"><span data-stu-id="8682b-137">**Service Level Agreements**   Maintain a set of goals for the performance of the IT systems and regularly measure performance against these goals.</span></span>

  - <span data-ttu-id="8682b-138">**ドキュメント**   構成情報や教訓などの標準的な手順を文書化し、それを必要とするスタッフメンバーが利用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="8682b-138">**Documentation**   Document standard procedures, such as configuration information and lessons learned, and make them available to the staff members that need them.</span></span> <span data-ttu-id="8682b-139">構成の変更が行われると、それに合わせてドキュメントが更新されます。</span><span class="sxs-lookup"><span data-stu-id="8682b-139">As changes to the configuration are made, update the documentation accordingly.</span></span>

</div>

<div>

## <a name="related-sections"></a><span data-ttu-id="8682b-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="8682b-140">Related Sections</span></span>

<span data-ttu-id="8682b-141">続行する前に、次のシステム操作に関するトピックを確認してください。</span><span class="sxs-lookup"><span data-stu-id="8682b-141">Review the following topics concerning system operations before proceeding:</span></span>

  - [<span data-ttu-id="8682b-142">Lync Server 2013 での容量と可用性の管理</span><span class="sxs-lookup"><span data-stu-id="8682b-142">Capacity and availability management in Lync Server 2013</span></span>](lync-server-2013-capacity-and-availability-management.md)

  - [<span data-ttu-id="8682b-143">Lync Server 2013 で管理を変更する</span><span class="sxs-lookup"><span data-stu-id="8682b-143">Change management in Lync Server 2013</span></span>](lync-server-2013-change-management.md)

  - [<span data-ttu-id="8682b-144">Lync Server 2013 での構成管理</span><span class="sxs-lookup"><span data-stu-id="8682b-144">Configuration management in Lync Server 2013</span></span>](lync-server-2013-configuration-management.md)

  - [<span data-ttu-id="8682b-145">Lync Server 2013 でのシステム管理</span><span class="sxs-lookup"><span data-stu-id="8682b-145">System administration in Lync Server 2013</span></span>](lync-server-2013-system-administration.md)

  - [<span data-ttu-id="8682b-146">Lync Server 2013 のサービスレベル契約</span><span class="sxs-lookup"><span data-stu-id="8682b-146">Service level agreements in Lync Server 2013</span></span>](lync-server-2013-service-level-agreements.md)

  - [<span data-ttu-id="8682b-147">Lync Server 2013 のドキュメント</span><span class="sxs-lookup"><span data-stu-id="8682b-147">Documentation in Lync Server 2013</span></span>](lync-server-2013-documentation.md)

  - [<span data-ttu-id="8682b-148">Lync Server 2013 の標準手順</span><span class="sxs-lookup"><span data-stu-id="8682b-148">Standard procedures in Lync Server 2013</span></span>](lync-server-2013-standard-procedures.md)

  - [<span data-ttu-id="8682b-149">Lync Server 2013 の緊急対応手順</span><span class="sxs-lookup"><span data-stu-id="8682b-149">Emergency procedures in Lync Server 2013</span></span>](lync-server-2013-emergency-procedures.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="8682b-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="8682b-150">See Also</span></span>


[<span data-ttu-id="8682b-151">Microsoft 運用フレームワーク4.0</span><span class="sxs-lookup"><span data-stu-id="8682b-151">Microsoft Operations Framework 4.0</span></span>](https://go.microsoft.com/fwlink/p/?linkid=40939)  
  

<span data-ttu-id="8682b-152"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8682b-152"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

