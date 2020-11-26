---
title: 'Lync Server 2013: アナウンスの構成の前提条件と役割'
description: 'Lync Server 2013: お知らせの構成の前提条件と役割。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Announcement configuration prerequisites and roles
ms:assetid: 82f2dfe9-4c5e-4d65-96a1-96495d506ea4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398658(v=OCS.15)
ms:contentKeyID: 48184674
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a8e6e7009adc6826c255e28ddda925b0e9be5fd6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439969"
---
# <a name="announcement-configuration-prerequisites-and-roles-in-lync-server-2013"></a><span data-ttu-id="bb043-103">Lync Server 2013 のアナウンスの構成の前提条件と役割</span><span class="sxs-lookup"><span data-stu-id="bb043-103">Announcement configuration prerequisites and roles in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bb043-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bb043-104">

<span> </span></span></span>

<span data-ttu-id="bb043-105">_**最終更新日:** 2013-02-25_</span><span class="sxs-lookup"><span data-stu-id="bb043-105">_**Topic Last Modified:** 2013-02-25_</span></span>

<span data-ttu-id="bb043-106">"お知らせ" は、エンタープライズの音声通話管理機能です。</span><span class="sxs-lookup"><span data-stu-id="bb043-106">Announcement is an Enterprise Voice call management feature.</span></span> <span data-ttu-id="bb043-107">このトピックでは、アナウンスメントを構成するために必要な準備と、構成タスクを実行するために必要な役割の割り当てについて説明します。</span><span class="sxs-lookup"><span data-stu-id="bb043-107">This topic describes what you need to have in place before you can configure Announcement and the role assignments that you need to perform configuration tasks.</span></span>

<span data-ttu-id="bb043-108">このセクションでは、お知らせに関連する計画ドキュメントを読み取っていることを前提としています (「 [Lync Server 2013 の通話管理機能の計画](lync-server-2013-planning-for-call-management-features.md)」を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="bb043-108">This section assumes that you have read the planning documentation related to Announcement (see [Planning for call management features in Lync Server 2013](lync-server-2013-planning-for-call-management-features.md)).</span></span>

<div>

## <a name="announcement-configuration-prerequisites"></a><span data-ttu-id="bb043-109">アナウンスメント構成の前提条件</span><span class="sxs-lookup"><span data-stu-id="bb043-109">Announcement Configuration Prerequisites</span></span>

<span data-ttu-id="bb043-110">アナウンスメントアプリケーションには、次のコンポーネントが必要です。</span><span class="sxs-lookup"><span data-stu-id="bb043-110">The Announcement application requires the following components:</span></span>

  - <span data-ttu-id="bb043-111">アプリケーション サービス</span><span class="sxs-lookup"><span data-stu-id="bb043-111">Application service</span></span>

  - <span data-ttu-id="bb043-112">応答グループ アプリケーション</span><span class="sxs-lookup"><span data-stu-id="bb043-112">Response Group application</span></span>

  - <span data-ttu-id="bb043-113">ファイルストア、オーディオファイルを保持する場合</span><span class="sxs-lookup"><span data-stu-id="bb043-113">File Store, to hold audio files</span></span>

<span data-ttu-id="bb043-114">エンタープライズボイスを展開すると、これらのすべてのコンポーネントが既定でインストールされます。</span><span class="sxs-lookup"><span data-stu-id="bb043-114">All of these components are installed by default when you deploy Enterprise Voice.</span></span>

</div>

<div>

## <a name="announcement-configuration-roles"></a><span data-ttu-id="bb043-115">アナウンスメント構成ロール</span><span class="sxs-lookup"><span data-stu-id="bb043-115">Announcement Configuration Roles</span></span>

<span data-ttu-id="bb043-116">以下の管理ツールを使用して、お知らせを構成することができます。</span><span class="sxs-lookup"><span data-stu-id="bb043-116">You can use the following administrative tools to configure announcements:</span></span>

  - <span data-ttu-id="bb043-117">Lync Server コントロール パネル</span><span class="sxs-lookup"><span data-stu-id="bb043-117">Lync Server Control Panel</span></span>

  - <span data-ttu-id="bb043-118">Lync Server 管理シェル</span><span class="sxs-lookup"><span data-stu-id="bb043-118">Lync Server Management Shell</span></span>

<span data-ttu-id="bb043-119">アナウンスメントアプリケーションを構成するには、次の管理者ロールのいずれかが必要です。</span><span class="sxs-lookup"><span data-stu-id="bb043-119">Configuring Announcement application requires one of the following administrative roles:</span></span>

  - <span data-ttu-id="bb043-120">**CsVoiceAdministrator**   この管理者の役割は、お知らせの設定など、音声に関連したすべての設定とポリシーの作成、構成、管理を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="bb043-120">**CsVoiceAdministrator**   This administrator role can create, configure, and manage all voice-related settings and policies, including Announcement settings.</span></span>

  - <span data-ttu-id="bb043-121">**Csserveradministrator**   この管理者の役割は、サーバーとサービスの管理、監視、トラブルシューティングを行い、すべてのアナウンスメント設定を構成することができます。</span><span class="sxs-lookup"><span data-stu-id="bb043-121">**CsServerAdministrator**   This administrator role can manage, monitor, and troubleshoot servers and services, and configure all Announcement settings.</span></span>

  - <span data-ttu-id="bb043-122">**Csadministrator**   この管理者の役割は、すべての管理タスクを実行し、すべての設定を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="bb043-122">**CsAdministrator**   This administrator role can perform all administrative tasks and modify all settings.</span></span>

  - <span data-ttu-id="bb043-123">**Csviewonlyadministrator**   この管理者の役割は、展開の正常性を監視するために展開を表示できます。</span><span class="sxs-lookup"><span data-stu-id="bb043-123">**CsViewOnlyAdministrator**   This administrator role can view the deployment to monitor deployment health.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="bb043-124">管理ユーザー権限の詳細については、計画ドキュメントの「 <A href="lync-server-2013-planning-for-role-based-access-control.md">Lync Server 2013 での役割ベースのアクセス制御の計画</A> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bb043-124">For details about administrative user rights, see <A href="lync-server-2013-planning-for-role-based-access-control.md">Planning for role-based access control in Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="bb043-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="bb043-125">See Also</span></span>


[<span data-ttu-id="bb043-126">Lync Server 2013 でのエンタープライズボイスの展開</span><span class="sxs-lookup"><span data-stu-id="bb043-126">Deploying Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-deploying-enterprise-voice.md)  


[<span data-ttu-id="bb043-127">Lync Server 2013 の通話管理機能の計画</span><span class="sxs-lookup"><span data-stu-id="bb043-127">Planning for call management features in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-management-features.md)  
  

<span data-ttu-id="bb043-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bb043-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

