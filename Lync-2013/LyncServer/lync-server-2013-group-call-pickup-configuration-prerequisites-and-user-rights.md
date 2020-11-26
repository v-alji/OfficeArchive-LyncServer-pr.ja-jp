---
title: グループ通話のピックアップ構成の前提条件とユーザー権利
description: グループ通話のピックアップ構成の前提条件とユーザー権利。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Group Call Pickup configuration prerequisites and user rights
ms:assetid: 8757b1d3-751d-49c3-b1b8-b678f663f18e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945641(v=OCS.15)
ms:contentKeyID: 51541495
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 74d2a758b7199634e14ee387d2554b30bf2ae8d3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427874"
---
# <a name="group-call-pickup-configuration-prerequisites-and-user-rights-in-lync-server-2013"></a><span data-ttu-id="9095a-103">グループ通話の集配構成の前提条件とユーザー権限 Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9095a-103">Group Call Pickup configuration prerequisites and user rights in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9095a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9095a-104">

<span> </span></span></span>

<span data-ttu-id="9095a-105">_**最終更新日:** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="9095a-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="9095a-106">グループ通話のピックアップは、エンタープライズボイスの展開時に既定でインストールされる通話管理機能です。</span><span class="sxs-lookup"><span data-stu-id="9095a-106">Group Call Pickup is a call management feature that is installed by default when you deploy Enterprise Voice.</span></span> <span data-ttu-id="9095a-107">このトピックでは、グループ通話のピックアップと構成タスクを実行するために必要なユーザー権限を構成する前に必要な準備について説明します。</span><span class="sxs-lookup"><span data-stu-id="9095a-107">This topic describes what you need to have in place before you can configure Group Call Pickup and the user rights that you need to perform configuration tasks.</span></span>

<span data-ttu-id="9095a-108">このセクションでは、グループ通話のピックアップに関連する計画ドキュメントを読み取っていることを前提としています (「 [Lync Server 2013 でのグループ通話のピックアップの計画](lync-server-2013-planning-for-group-call-pickup.md)」を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="9095a-108">This section assumes that you have read the planning documentation related to Group Call Pickup (see [Planning for Group Call Pickup in Lync Server 2013](lync-server-2013-planning-for-group-call-pickup.md)).</span></span>

<div>

## <a name="group-call-pickup-configuration-prerequisites"></a><span data-ttu-id="9095a-109">グループ通話のピックアップ構成の前提条件</span><span class="sxs-lookup"><span data-stu-id="9095a-109">Group Call Pickup Configuration Prerequisites</span></span>

<span data-ttu-id="9095a-110">グループ通話のピックアップには次のコンポーネントが必要です。</span><span class="sxs-lookup"><span data-stu-id="9095a-110">Group Call Pickup requires the following components:</span></span>

  - <span data-ttu-id="9095a-111">アプリケーション サービス</span><span class="sxs-lookup"><span data-stu-id="9095a-111">Application service</span></span>

  - <span data-ttu-id="9095a-112">コール パーク アプリケーション</span><span class="sxs-lookup"><span data-stu-id="9095a-112">Call Park application</span></span>

<span data-ttu-id="9095a-113">これらのコンポーネントは、エンタープライズボイスの展開時に自動的にインストールされます。</span><span class="sxs-lookup"><span data-stu-id="9095a-113">These components are installed automatically when you deploy Enterprise Voice.</span></span>

</div>

<div>

## <a name="group-call-pickup-configuration-user-rights"></a><span data-ttu-id="9095a-114">グループ通話のピックアップ構成のユーザー権利</span><span class="sxs-lookup"><span data-stu-id="9095a-114">Group Call Pickup Configuration User Rights</span></span>

<span data-ttu-id="9095a-115">グループ通話のピックアップを構成するには、次の管理ツールを使用します。</span><span class="sxs-lookup"><span data-stu-id="9095a-115">You use the following administrative tools to configure Group Call Pickup:</span></span>

  - <span data-ttu-id="9095a-116">Lync Server 管理シェル</span><span class="sxs-lookup"><span data-stu-id="9095a-116">Lync Server Management Shell</span></span>

  - <span data-ttu-id="9095a-117">SEFAUtil リソースキットツール</span><span class="sxs-lookup"><span data-stu-id="9095a-117">SEFAUtil resource kit tool</span></span>

<span data-ttu-id="9095a-118">Lync Server 管理シェルを使用して、通話パークの軌道テーブルにある通話ピックアップグループの作成と管理を行います。</span><span class="sxs-lookup"><span data-stu-id="9095a-118">Use Lync Server Management Shell to create and manage call pickup groups in the Call Park orbit table.</span></span> <span data-ttu-id="9095a-119">SEFAUtil リソースキットツールを使用して、通話ピックアップグループを割り当て、ユーザーに対してグループ通話のピックアップを有効にするか、ユーザーのグループ通話のピックアップを無効にします。</span><span class="sxs-lookup"><span data-stu-id="9095a-119">Use the SEFAUtil resource kit tool to assign a call pickup group and enable Group Call Pickup for users or to disable Group Call Pickup for users.</span></span>

<span data-ttu-id="9095a-120">グループ通話のピックアップを構成するには、タスクに応じて次の管理者ロールが必要です。</span><span class="sxs-lookup"><span data-stu-id="9095a-120">Configuring Group Call Pickup requires any of the following administrative roles, depending on the task:</span></span>

  - <span data-ttu-id="9095a-121">**CsVoiceAdministrator:** この管理者ロールは、音声関連のすべての設定とポリシーを作成、構成、管理できます。</span><span class="sxs-lookup"><span data-stu-id="9095a-121">**CsVoiceAdministrator:** This administrator role can create, configure, and manage all voice-related settings and policies.</span></span>

  - <span data-ttu-id="9095a-122">**Csuseradministrator:** この管理者の役割は、ユーザーに対してグループ通話のピックアップを有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="9095a-122">**CsUserAdministrator:** This administrator role can enable Group Call Pickup for users.</span></span> <span data-ttu-id="9095a-123">この管理者ロールは、すべての音声構成に対して読み取り専用ビューでアクセスすることもできます。</span><span class="sxs-lookup"><span data-stu-id="9095a-123">This administrator role also has read-only view access to all voice configurations.</span></span>

  - <span data-ttu-id="9095a-124">**Csserveradministrator:** この管理者の役割は、サーバーとサービスの管理、監視、トラブルシューティングを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="9095a-124">**CsServerAdministrator:** This administrator role can manage, monitor, and troubleshoot servers and services.</span></span>

  - <span data-ttu-id="9095a-125">**Csadministrator:** この管理者ロールは、CsVoiceAdministrator、CsServerAdministrator、Csserveradministrator のすべてのタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="9095a-125">**CsAdministrator:** This administrator role can perform all of the tasks of CsVoiceAdministrator, CsServerAdministrator, and CsUserAdministrator.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="9095a-126">管理権限の詳細については、計画ドキュメントの「 <A href="lync-server-2013-planning-for-role-based-access-control.md">Lync Server 2013 での役割ベースのアクセス制御の計画</A> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9095a-126">For details about administrative rights, see <A href="lync-server-2013-planning-for-role-based-access-control.md">Planning for role-based access control in Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="9095a-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="9095a-127">See Also</span></span>


[<span data-ttu-id="9095a-128">Lync Server 2013 でのエンタープライズボイスの展開</span><span class="sxs-lookup"><span data-stu-id="9095a-128">Deploying Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-deploying-enterprise-voice.md)  


[<span data-ttu-id="9095a-129">Lync Server 2013 の通話管理機能の計画</span><span class="sxs-lookup"><span data-stu-id="9095a-129">Planning for call management features in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-management-features.md)  
  

<span data-ttu-id="9095a-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9095a-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

