---
title: Lync Server 2010、グループ チャットまたは Office Communicatins Server 2007 R2 グループ チャットから Lync Server 2013、常設チャット サーバーへの移行
description: Lync Server 2010、グループチャット、または Office Communications Server 2007 R2 グループチャットから Lync Server 2013、常設チャットサーバーへの移行。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migration from Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server
ms:assetid: 5b4d3db1-6eba-4932-b49c-f60bcf9488f9
ms:mtpsurl: https://technet.microsoft.com/library/Gg615442(v=OCS.15)
ms:contentKeyID: 48184240
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6090d5924a203a960444d9a10700fd178d038887
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446858"
---
# <a name="migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server"></a><span data-ttu-id="55993-103">Lync Server 2010、グループ チャットまたは Office Communicatins Server 2007 R2 グループ チャットから Lync Server 2013、常設チャット サーバーへの移行</span><span class="sxs-lookup"><span data-stu-id="55993-103">Migration from Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="55993-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="55993-104">

<span> </span></span></span>

<span data-ttu-id="55993-105">_**最終更新日:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="55993-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="55993-106">このセクションのトピックでは、Lync Server 2010、グループチャット、または Office Communications Server 2007 R2 グループチャットを Lync Server 2013、常設チャットサーバーに移行するプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="55993-106">The topics in this section guide you through the process of migrating either Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server.</span></span> <span data-ttu-id="55993-107">Lync server 2013 の常設チャットサーバーの展開と Lync Server 2010、グループチャット、または Office Communications Server 2007 R2 グループチャットの展開については、この混合環境での操作に関する重要な情報も含まれています。</span><span class="sxs-lookup"><span data-stu-id="55993-107">If you intend for your Lync Server 2013, Persistent Chat Server deployment to coexist with a Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat deployment, this guide also includes some essential information for operating in this mixed environment.</span></span> <span data-ttu-id="55993-108">このガイドは主に、常設チャットサーバーのデータ移行に焦点を当てています。</span><span class="sxs-lookup"><span data-stu-id="55993-108">This guide primarily focuses on data migration for Persistent Chat Server.</span></span> <span data-ttu-id="55993-109">以前のバージョンの Lync Server から Lync Server 2013 に移行しているユーザーの場合は、「 [lync server 2010 から Lync server 2013 に移行](migration-from-lync-server-2010-to-lync-server-2013.md) する」と「 [Office Communications server 2007 R2 から lync server 2013 に](migration-from-office-communications-server-2007-r2-to-lync-server-2013.md)移行する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="55993-109">For users who are migrating from legacy versions of Lync Server to Lync Server 2013, see [Migration from Lync Server 2010 to Lync Server 2013](migration-from-lync-server-2010-to-lync-server-2013.md) and [Migration from Office Communications Server 2007 R2 to Lync Server 2013](migration-from-office-communications-server-2007-r2-to-lync-server-2013.md).</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="55993-110">このトピックでは、lync server 2010 または Office Communications Server 2007 R2 との共存に、既に Lync Server 2013 をインストールしていることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="55993-110">This topic assumes that you have already installed Lync Server 2013 in coexistence with Lync Server 2010 or Office Communications Server 2007 R2.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="55993-111">このガイドでは、移行の各フェーズを実行するために必要な手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="55993-111">This guide describes the steps generally required to accomplish each phase of migration.</span></span> <span data-ttu-id="55993-112">これは、すべてのレガシ展開トポロジまたは可能な移行シナリオには対応していません。</span><span class="sxs-lookup"><span data-stu-id="55993-112">It does not address every possible legacy deployment topology or every possible migration scenario.</span></span> <span data-ttu-id="55993-113">そのため、説明されているすべての手順を実行する必要がない場合や、展開によっては追加の手順を実行する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="55993-113">Therefore, you may not need to perform every step that is described, or you may need to perform additional steps, depending on your deployment.</span></span> <span data-ttu-id="55993-114">このガイドには、確認手順の例も用意されています。</span><span class="sxs-lookup"><span data-stu-id="55993-114">The guide also provides examples of verification steps.</span></span> <span data-ttu-id="55993-115">これらの検証手順は、移行の進行に応じて各フェーズが正常に完了するために必要な情報を確認するために用意されています。</span><span class="sxs-lookup"><span data-stu-id="55993-115">These verification steps are provided to help you understand what you need to look for to be sure that each phase completes successfully as you progress through your migration.</span></span> <span data-ttu-id="55993-116">この確認手順は、特定の移行プロセスに合わせて変更できます。</span><span class="sxs-lookup"><span data-stu-id="55993-116">You can modify these verification steps to your specific migration process.</span></span>



</div>

<span data-ttu-id="55993-117">このガイドには、既存の展開のアップグレードに固有の情報が記載されています。</span><span class="sxs-lookup"><span data-stu-id="55993-117">This guide provides information specific to upgrading your existing deployment.</span></span> <span data-ttu-id="55993-118">既存のトポロジを変更する方法については説明しません。</span><span class="sxs-lookup"><span data-stu-id="55993-118">It does not explain how to change your existing topology.</span></span> <span data-ttu-id="55993-119">このガイドでは、新機能の実装については説明しません。</span><span class="sxs-lookup"><span data-stu-id="55993-119">This guide does not cover the implementation of new features.</span></span> <span data-ttu-id="55993-120">詳細な手順については、別のドキュメントまたはドキュメントの説明を参照してください。</span><span class="sxs-lookup"><span data-stu-id="55993-120">When a detailed procedure is documented elsewhere, this guide directs you to the appropriate document or document section.</span></span>

<span data-ttu-id="55993-121">このドキュメントでは、次の一覧で指定された用語を定義しています。</span><span class="sxs-lookup"><span data-stu-id="55993-121">This document defines terms as specified in the following list.</span></span>

  - <span data-ttu-id="55993-122">*用*</span><span class="sxs-lookup"><span data-stu-id="55993-122">*migration*</span></span>  
    <span data-ttu-id="55993-123">以前のバージョンの常設チャットサーバー (旧称グループチャットサーバー) から、Lync Server 2013 の常設チャットサーバーへの展開を移行します。</span><span class="sxs-lookup"><span data-stu-id="55993-123">Moving your deployment from a previous version of Persistent Chat Server, formerly known as Group Chat Server, to Lync Server 2013, Persistent Chat Server.</span></span>

<!-- end list -->

  - <span data-ttu-id="55993-124">*アップグレード*</span><span class="sxs-lookup"><span data-stu-id="55993-124">*upgrade*</span></span>  
    <span data-ttu-id="55993-125">新しいバージョンのソフトウェアをサーバーまたはクライアントコンピューターにインストールします。</span><span class="sxs-lookup"><span data-stu-id="55993-125">Installing a newer version of software on a server or client computer.</span></span>

<!-- end list -->

  - <span data-ttu-id="55993-126">*共存*</span><span class="sxs-lookup"><span data-stu-id="55993-126">*coexistence*</span></span>  
    <span data-ttu-id="55993-127">移行時に存在する一時的な環境では、一部の機能が Lync Server 2013 に移行されている場合、常設チャットサーバー、その他の機能が以前のバージョンのグループチャットサーバーに残っている場合に、その他の機能は引き続き維持されます。</span><span class="sxs-lookup"><span data-stu-id="55993-127">The temporary environment that exists during migration, when some functionality has been migrated to Lync Server 2013, Persistent Chat Server, and other functionality still remains on a prior version of Group Chat Server.</span></span>

<span data-ttu-id="55993-128">常設チャットサーバーは、Lync Server 2013 インフラストラクチャの拡張機能です。</span><span class="sxs-lookup"><span data-stu-id="55993-128">Persistent Chat Server is an extension of the Lync Server 2013 infrastructure.</span></span> <span data-ttu-id="55993-129">使用しているトポロジに応じて、Lync Server 2010、グループチャット、または Office Communications Server 2007 R2 グループチャットを Lync Server 2013 常設チャットサーバーに移行することができます。</span><span class="sxs-lookup"><span data-stu-id="55993-129">Depending on your topology, you can migrate Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013 Persistent Chat Server.</span></span> <span data-ttu-id="55993-130">使用可能なトポロジと、グループチャットサーバーを移行するための技術およびソフトウェアの要件の詳細については、計画ドキュメントの「 [Lync server 2013 での常設チャットサーバーの計画](lync-server-2013-planning-for-persistent-chat-server.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="55993-130">For details about available topologies and the technical and software requirements for migrating Group Chat Server, see [Planning for Persistent Chat Server in Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md) in the Planning documentation.</span></span>

<span data-ttu-id="55993-131">組織でコンプライアンスのサポートが必要な場合は、各常設チャットサーバーと共に自動的にインストールされます。</span><span class="sxs-lookup"><span data-stu-id="55993-131">If your organization requires compliance support, it is now automatically installed with each Persistent Chat Server.</span></span> <span data-ttu-id="55993-132">別のサーバーは、コンプライアンスのために必要とされなくなりました。</span><span class="sxs-lookup"><span data-stu-id="55993-132">A separate server is no longer needed for compliance.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="55993-133">ファイルシステムのセキュリティを適用するには、常設チャットサーバーが NTFS ファイルシステムにインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="55993-133">Persistent Chat Server must be installed on an NTFS file system to help enforce file system security.</span></span> <span data-ttu-id="55993-134">FAT32 は、常設チャットサーバーでサポートされているファイルシステムではありません。</span><span class="sxs-lookup"><span data-stu-id="55993-134">FAT32 is not a supported file system for Persistent Chat Server.</span></span><BR><span data-ttu-id="55993-135">組織でコンプライアンスのサポートが必要な場合は、各常設チャットサーバーと共に自動的にインストールされます。</span><span class="sxs-lookup"><span data-stu-id="55993-135">If your organization requires compliance support, it is now automatically installed with each Persistent Chat Server.</span></span> <span data-ttu-id="55993-136">別のサーバーは、コンプライアンスのために必要とされなくなりました。</span><span class="sxs-lookup"><span data-stu-id="55993-136">A separate server is no longer needed for compliance.</span></span> <span data-ttu-id="55993-137">Lync Server 2013 常設チャットサーバーでの変更の詳細については、「はじめに」の &nbsp; ドキュメントで「 <A href="lync-server-2013-new-persistent-chat-server-features.md">lync server 2013 の新しい常設チャットサーバー機能</A> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="55993-137">For more details about changes in Lync Server 2013&nbsp;Persistent Chat Server, see <A href="lync-server-2013-new-persistent-chat-server-features.md">New Persistent Chat Server features in Lync Server 2013</A> in the Getting Started documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="55993-138">このセクション中</span><span class="sxs-lookup"><span data-stu-id="55993-138">In This Section</span></span>

  - [<span data-ttu-id="55993-139">標準移行シナリオ - 概要</span><span class="sxs-lookup"><span data-stu-id="55993-139">Standard migration scenario - high-level</span></span>](standard-migration-scenario-high-level.md)

  - [<span data-ttu-id="55993-140">移行のプロセス - 詳細</span><span class="sxs-lookup"><span data-stu-id="55993-140">Migration process - details</span></span>](migration-process-details.md)

  - [<span data-ttu-id="55993-141">共存の考慮事項</span><span class="sxs-lookup"><span data-stu-id="55993-141">Coexistence considerations</span></span>](coexistence-considerations.md)

<span data-ttu-id="55993-142"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="55993-142"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

