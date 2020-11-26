---
title: 'Lync Server 2013: 構成管理'
description: 'Lync Server 2013: 構成管理。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuration management
ms:assetid: 00ea1196-cb40-427f-99a4-5e8037cbf367
ms:mtpsurl: https://technet.microsoft.com/library/Dn720316(v=OCS.15)
ms:contentKeyID: 63969570
ms.date: 05/16/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f5999708811cc4a34cf846a1ddd481ba38e07c62
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434250"
---
# <a name="configuration-management-in-lync-server-2013"></a><span data-ttu-id="9f7b0-103">Lync Server 2013 での構成管理</span><span class="sxs-lookup"><span data-stu-id="9f7b0-103">Configuration management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9f7b0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9f7b0-104">

<span> </span></span></span>

<span data-ttu-id="9f7b0-105">_**最終更新日:** 2015-05-15_</span><span class="sxs-lookup"><span data-stu-id="9f7b0-105">_**Topic Last Modified:** 2015-05-15_</span></span>

<span data-ttu-id="9f7b0-106">構成管理は、ハードウェアとソフトウェアの資産およびシステム構成情報を記録および追跡するプロセスです。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-106">Configuration management is the process of recording and tracking hardware and software assets and system configuration information.</span></span> <span data-ttu-id="9f7b0-107">通常、ソフトウェアライセンスの管理、クライアントコンピューターおよびサーバーの標準的なハードウェアとソフトウェアのビルドの維持、新しいコンピューターの名前付け標準の定義に使用されます。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-107">It is generally used to track software licenses, maintain a standard hardware and software build for client computers and servers, and define naming standards for new computers.</span></span> <span data-ttu-id="9f7b0-108">構成管理では、一般的に次のカテゴリについて説明します。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-108">Configuration management generally covers the following categories:</span></span>

  - <span data-ttu-id="9f7b0-109">**ハードウェア**   このカテゴリは、IT 組織が所有する機器、機材の所在地、および機器を使っている機器を追跡します。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-109">**Hardware**   This category tracks the pieces of equipment that the IT organization owns, where equipment is located, and who uses equipment.</span></span> <span data-ttu-id="9f7b0-110">この情報により、組織はアップグレードの計画と予算の作成、標準のハードウェア構築の維持、会計目的の IT 資産の価値の報告、および盗難防止の支援を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-110">This information enables an organization to plan and budget for upgrades, maintain standard hardware builds, report on the value of IT assets for accounting purposes, and help prevent theft.</span></span>

  - <span data-ttu-id="9f7b0-111">**ソフトウェア**   このカテゴリは、各コンピューターにインストールされているソフトウェア、バージョン番号、ライセンスが保持されている場所を追跡します。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-111">**Software**   This category tracks software that is installed on each computer, the version numbers, and where the licenses are held.</span></span> <span data-ttu-id="9f7b0-112">この情報は、アップグレードを計画し、ソフトウェアがライセンスされていることを確認し、許可されていない (およびライセンスのない) ソフトウェアの存在を検出するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-112">This information helps plan upgrades, to ensure that software is licensed, and detect the presence of unauthorized (and unlicensed) software.</span></span>

  - <span data-ttu-id="9f7b0-113">**標準ビルド**   このカテゴリは、クライアントコンピューターおよびサーバーの現在の標準ビルドを追跡し、クライアントコンピューターとサーバーがこの標準を満たしているかどうかを追跡します。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-113">**Standard Builds**   This category tracks the current standard build for the client computers and servers and whether the client computers and servers meet this standard.</span></span> <span data-ttu-id="9f7b0-114">標準ビルドを定義して適用すると、スタッフはソフトウェアの各部分の限られたバージョンのバージョンのみを保持する必要があるため、サポートスタッフに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-114">Defining and enforcing standard builds helps support staff because the staff is required to maintain only a limited number of versions of each piece of software.</span></span>

  - <span data-ttu-id="9f7b0-115">**累積的な更新プログラムと修正プログラム**   このカテゴリは、使用するためにテストおよび承認されているサービスパックと、どのコンピューターが最新であるかを追跡します。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-115">**Cumulative Updates and Hotfixes**   This category tracks which service packs are tested and approved for use and which computers are up to date.</span></span> <span data-ttu-id="9f7b0-116">この情報は、コンピューターが危険にさらされるリスクを軽減し、未承認の更新プログラムをインストールしたユーザーを検出するために重要です。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-116">This information is important to reduce the risk of computers being compromised and to detect users who have installed unapproved updates.</span></span>

  - <span data-ttu-id="9f7b0-117">**システム構成情報**   このカテゴリは、システムの機能、システム要素間の相互作用、円滑に動作しているシステムに依存するプロセスを追跡します。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-117">**System Configuration Information**   This category tracks the function of a system, the interaction between system elements, and the processes that depend on a system that is running smoothly.</span></span> <span data-ttu-id="9f7b0-118">たとえば、サードパーティのプロキシサーバーが1台のサーバーに対して構成されている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-118">For example, third-party proxy server may be configured on a single server.</span></span> <span data-ttu-id="9f7b0-119">このサーバーに対するプロキシサーバーの依存関係を理解し、障害が発生した場合は不測の計画が必要になることがあります。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-119">The proxy server’s dependence on this server should be understood and contingency plans may be required if there is a failure.</span></span> <span data-ttu-id="9f7b0-120">他のフロントエンドサーバーと通信するようにプロキシサーバーを構成できる場合は、依存関係と不測事態対応の計画が変わる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-120">If the proxy server can be configured to also communicate with another front-end server, dependencies and contingency plans will probably change.</span></span>

<div>

## <a name="implementing-configuration-management"></a><span data-ttu-id="9f7b0-121">構成管理の実装</span><span class="sxs-lookup"><span data-stu-id="9f7b0-121">Implementing configuration management</span></span>

<span data-ttu-id="9f7b0-122">管理が必要な項目を特定したら、データとレポートデータを収集して構成管理を実装します。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-122">After you determine what items need managing, implement configuration management by collecting data and reporting data.</span></span> <span data-ttu-id="9f7b0-123">小規模の組織にとって最も簡単な方法は、データを手動で収集することです (クライアントコンピューター、オペレーティングシステム、インストールされているソフトウェアの数とモデル)。また、Office Word または Office Excel ドキュメントに保存します。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-123">The simplest approach for small organizations is to collect data manually (number and model of client computers, operating system, installed software) and save it in an Office Word or Office Excel document.</span></span> <span data-ttu-id="9f7b0-124">大規模で複雑で、絶えず変化するシステムでは、資産の検出と詳細情報の収集を自動化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-124">For larger, more complex, and constantly changing systems, the discovery of assets and collection of detailed information must be automated.</span></span> <span data-ttu-id="9f7b0-125">組織に関連する情報を判断し、データベースに記録します。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-125">Decide what information is relevant to your organization and record it in a database.</span></span>

<span data-ttu-id="9f7b0-126">構成管理データベースは、次の領域でのサポートスタッフと管理のための便利なツールです。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-126">The configuration management database is a useful tool for support staff and management in the following areas:</span></span>

  - <span data-ttu-id="9f7b0-127">**セキュリティ監査**   データベースでは、Lync Server を実行しているサーバーと、ホットフィックスが適用されているか、service pack または最新のウイルス対策更新プログラムがインストールされていないことを示すクライアントコンピューターシステムを特定できます。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-127">**Security Audits**   The database enables you to identify servers that are running Lync Server and client computer systems that must have hotfixes applied or that have missed the installation of a service pack or the latest antivirus updates.</span></span>

  - <span data-ttu-id="9f7b0-128">**ソフトウェアのインストール**   クライアントソフトウェアのバージョンを特定して追跡することで、管理者はバージョンの更新プログラムと新規インストールの計画を支援し、ライセンスドキュメントやコンプライアンスのサポートを受けることができます。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-128">**Software Installation**   Identifying client software versions and tracking them will aid administrators in planning version updates and new installs and also by helping with licensing documentation and compliance.</span></span>

  - <span data-ttu-id="9f7b0-129">**構成情報**   既定値から変更されたすべての設定の最新の一覧を保持している場合は、問題のトラブルシューティングをすばやく効率的に行うことができます。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-129">**Configuration Information**   If you maintain an up-to-date list of all settings that were changed from their default, then you'll be able to troubleshoot issues quickly and more effectively.</span></span>

  - <span data-ttu-id="9f7b0-130">**アップグレードを計画**   する  キャパシティレビューによって、Lync データベースサーバーで追加の記憶域が必要であることがわかった場合は、各サーバーに内部の RAID コントローラーがあるかどうかを確認することが重要です。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-130">**Planning Upgrades**   If a capacity review reveals that additional storage space is required on your Lync database servers, it’s important to know whether each server has an internal RAID controller.</span></span> <span data-ttu-id="9f7b0-131">その場合は、同じモデルですか?</span><span class="sxs-lookup"><span data-stu-id="9f7b0-131">If they do, then are they the same model?</span></span> <span data-ttu-id="9f7b0-132">同じ数のディスクがインストールされているかどうかを確認する</span><span class="sxs-lookup"><span data-stu-id="9f7b0-132">Do they have the same number of disks installed?</span></span> <span data-ttu-id="9f7b0-133">構成管理データベースには、インストールできるディスクの種類、番号、および各ケースのアップグレードパスが示されます。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-133">The configuration management database will indicate the type of disk that can be installed, the number, and the upgrade path in each case.</span></span>

</div>

<div>

## <a name="tools-used-for-configuration-management"></a><span data-ttu-id="9f7b0-134">構成管理に使用されるツール</span><span class="sxs-lookup"><span data-stu-id="9f7b0-134">Tools used for configuration management</span></span>

<span data-ttu-id="9f7b0-135">アセットを検出、監査、および報告するための多くのツールがあります。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-135">There are many tools to discover, audit, and report assets.</span></span> <span data-ttu-id="9f7b0-136">このセクションでは、これらのツールの一部について説明します。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-136">Some of these tools are discussed in this section.</span></span>

  - <span data-ttu-id="9f7b0-137">**自動スクリプト**   簡単なスクリプトを作成して、オペレーティングシステム、service pack レベル、ソフトウェアが特定のコンピューターに存在するかどうかなどの項目をレポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-137">**Automated Scripts**   You can write simple scripts to report items such as the operating system, service pack level, and whether software exists on a specific set of computers.</span></span> <span data-ttu-id="9f7b0-138">これらのスクリプトは、組織の正確な要件に書くことができます。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-138">You can write these scripts to an organization’s exact requirements.</span></span> <span data-ttu-id="9f7b0-139">ただし、必要なスクリプトの数とその複雑さは、スクリプトを作成して維持するのにコストがかかる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-139">However, the required number of scripts and their complexity can make scripts expensive to create and maintain.</span></span>

  - <span data-ttu-id="9f7b0-140">**自動ツール**   会社の規模と組織のニーズによっては、自動化ツールの使用を検討することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-140">**Automated Tools**   Depending on the size of your business and your organizational needs, you may want to consider using automated tools.</span></span> <span data-ttu-id="9f7b0-141">Microsoft Endpoint Configuration Manager などのツールによって標準のレポートテンプレート (service pack level など) が組み込まれているほか、カスタムアプリケーションの場合など、カスタマイズされたレポートを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-141">Tools such as Microsoft Endpoint Configuration Manager incorporate standard report templates (such as service pack level) and also enable you to create customized reports, for example, for a custom application.</span></span> <span data-ttu-id="9f7b0-142">Microsoft Endpoint Configuration Manager は、ハードウェアとソフトウェアの構成を報告するために使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-142">The Microsoft Endpoint Configuration Manager can also be used to report on hardware and software configurations.</span></span>

</div>

<div>

## <a name="relationship-with-change-management"></a><span data-ttu-id="9f7b0-143">変更管理との関係</span><span class="sxs-lookup"><span data-stu-id="9f7b0-143">Relationship with change management</span></span>

<span data-ttu-id="9f7b0-144">構成管理は、変更管理に密接に関係しています。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-144">Configuration management is closely related to change management.</span></span> <span data-ttu-id="9f7b0-145">構成管理は、変更の必要性と、変更が発生したことを特定して記録することを示します。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-145">Configuration management identifies the need for change and identifies and records that a change has occurred.</span></span> <span data-ttu-id="9f7b0-146">たとえば、構成管理データベースを使って、修正プログラムが必要なサーバーを特定することができます。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-146">For example, the configuration management database can be used to identify servers that require a hotfix.</span></span> <span data-ttu-id="9f7b0-147">次に、変更管理によって修正プログラムを適用するプロセスが定義されます。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-147">Change management then defines the process for applying the hotfix.</span></span>

<span data-ttu-id="9f7b0-148">逆に、新しい累積更新プログラムがロールアウトされた場合、変更管理プロセスでは、構成管理システムにこの情報を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-148">Conversely, if a new cumulative update is rolled out, the change management process should supply this information to the configuration management system.</span></span> <span data-ttu-id="9f7b0-149">ソフトウェアが展開されている場所とタイミングを検出して追跡するために、構成管理ツールは、おそらく、新しいソフトウェアを特定するように構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f7b0-149">The configuration management tools will probably need to be configured to identify the new software so that they can discover and track where and when the software is deployed.</span></span>

<span data-ttu-id="9f7b0-150"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9f7b0-150"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

