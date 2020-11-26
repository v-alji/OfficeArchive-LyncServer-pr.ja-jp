---
title: 'Lync Server 2013: コール パーク構成の前提条件とユーザー権限'
description: 'Lync Server 2013: Call パーク構成の前提条件とユーザー権利'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call Park configuration prerequisites and user rights
ms:assetid: 25b8cfe0-e4e7-487c-9e78-8c040f629059
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425730(v=OCS.15)
ms:contentKeyID: 48183648
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b01187ad32fa7338765c0fa5b409b4e185e8ad35
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435713"
---
# <a name="call-park-configuration-prerequisites-and-user-rights-in-lync-server-2013"></a><span data-ttu-id="773b0-103">Lync Server 2013 のコール パーク構成の前提条件とユーザー権限</span><span class="sxs-lookup"><span data-stu-id="773b0-103">Call Park configuration prerequisites and user rights in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="773b0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="773b0-104">

<span> </span></span></span>

<span data-ttu-id="773b0-105">_**最終更新日:** 2012-09-10_</span><span class="sxs-lookup"><span data-stu-id="773b0-105">_**Topic Last Modified:** 2012-09-10_</span></span>

<span data-ttu-id="773b0-106">コールパークは、エンタープライズボイスの展開時に既定でインストールされる通話管理機能です。</span><span class="sxs-lookup"><span data-stu-id="773b0-106">Call Park is a call management feature that is installed by default when you deploy Enterprise Voice.</span></span> <span data-ttu-id="773b0-107">このトピックでは、コールパークと構成タスクを実行するために必要なユーザー権利を設定する前に、準備しておく必要があることについて説明します。</span><span class="sxs-lookup"><span data-stu-id="773b0-107">This topic describes what you need to have in place before you can configure Call Park and the user rights that you need to perform configuration tasks.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="773b0-108">会議のカスタマイズされた保留中のファイルは Lync Server 2013 の障害回復プロセスの一部としてはバックアップされません。プールにアップロードされたファイルが破損、破損、または消去された場合、ファイルは失われます。</span><span class="sxs-lookup"><span data-stu-id="773b0-108">Customized music-on-hold files for the Call Park application are not backed up as part of the Lync Server 2013 disaster recovery process, and the files will be lost if the files uploaded to the pool are damaged, corrupted, or erased.</span></span> <span data-ttu-id="773b0-109">コール パーク用にアップロードされているカスタマイズした保留音ファイルについては、常に個別のバックアップ コピーを保持してください。</span><span class="sxs-lookup"><span data-stu-id="773b0-109">Always keep a separate backup copy of the customized music-on-hold files that you have uploaded for Call Park.</span></span>



</div>

<span data-ttu-id="773b0-110">このセクションでは、通話パークに関連する計画ドキュメントを読み取っていることを前提としています (「 [Lync Server 2013 での通話管理機能の計画](lync-server-2013-planning-for-call-management-features.md)」を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="773b0-110">This section assumes that you have read the planning documentation related to Call Park (see [Planning for call management features in Lync Server 2013](lync-server-2013-planning-for-call-management-features.md)).</span></span>

<div>

## <a name="call-park-configuration-prerequisites"></a><span data-ttu-id="773b0-111">コールパーク構成の前提条件</span><span class="sxs-lookup"><span data-stu-id="773b0-111">Call Park Configuration Prerequisites</span></span>

<span data-ttu-id="773b0-112">コールパークには、次のコンポーネントが必要です。</span><span class="sxs-lookup"><span data-stu-id="773b0-112">Call Park requires the following components:</span></span>

  - <span data-ttu-id="773b0-113">アプリケーション サービス</span><span class="sxs-lookup"><span data-stu-id="773b0-113">Application service</span></span>

  - <span data-ttu-id="773b0-114">コール パーク アプリケーション</span><span class="sxs-lookup"><span data-stu-id="773b0-114">Call Park application</span></span>

<span data-ttu-id="773b0-115">これらのコンポーネントは、エンタープライズボイスの展開時に自動的にインストールされます。</span><span class="sxs-lookup"><span data-stu-id="773b0-115">These components are installed automatically when you deploy Enterprise Voice.</span></span>

<span data-ttu-id="773b0-116">通話の保留中に発信者に音楽が聞こえるようにする場合は、音楽の保留ファイルも必要です。</span><span class="sxs-lookup"><span data-stu-id="773b0-116">If you want callers to hear music while the call is parked, a music-on-hold file is also required.</span></span> <span data-ttu-id="773b0-117">既定の音楽の保留ファイルは、エンタープライズボイスの展開時に自動的にインストールされます。</span><span class="sxs-lookup"><span data-stu-id="773b0-117">A default music-on-hold file is installed automatically when you deploy Enterprise Voice.</span></span> <span data-ttu-id="773b0-118">既定のファイルは、独自の音楽の保留ファイルに置き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="773b0-118">You can substitute the default file with your own music-on-hold file.</span></span> <span data-ttu-id="773b0-119">[コールパークファイルストアでは、オーディオファイルを保持します。</span><span class="sxs-lookup"><span data-stu-id="773b0-119">Call Park uses File Store to hold the audio file.</span></span>

</div>

<div>

## <a name="call-park-configuration-user-rights"></a><span data-ttu-id="773b0-120">コールパーク構成のユーザー権利</span><span class="sxs-lookup"><span data-stu-id="773b0-120">Call Park Configuration User Rights</span></span>

<span data-ttu-id="773b0-121">以下の管理ツールを使って、コールパークを構成することができます。</span><span class="sxs-lookup"><span data-stu-id="773b0-121">You can use the following administrative tools to configure Call Park:</span></span>

  - <span data-ttu-id="773b0-122">Lync Server コントロール パネル</span><span class="sxs-lookup"><span data-stu-id="773b0-122">Lync Server Control Panel</span></span>

  - <span data-ttu-id="773b0-123">Lync Server 管理シェル</span><span class="sxs-lookup"><span data-stu-id="773b0-123">Lync Server Management Shell</span></span>

<span data-ttu-id="773b0-124">これらのツールを使って、コールパークの軌道を設定したり、コールパークで使用される他の設定を構成したりします。</span><span class="sxs-lookup"><span data-stu-id="773b0-124">You use these tools to set up the Call Park orbit table and to configure other settings used by Call Park.</span></span>

<span data-ttu-id="773b0-125">コールパークを構成するには、タスクに応じて次の管理者ロールが必要です。</span><span class="sxs-lookup"><span data-stu-id="773b0-125">Configuring Call Park requires any of the following administrative roles, depending on the task:</span></span>

  - <span data-ttu-id="773b0-126">**CsVoiceAdministrator:** この管理者ロールは、音声関連のすべての設定とポリシーを作成、構成、管理できます。</span><span class="sxs-lookup"><span data-stu-id="773b0-126">**CsVoiceAdministrator:** This administrator role can create, configure, and manage all voice-related settings and policies.</span></span>

  - <span data-ttu-id="773b0-127">**Csuseradministrator:** この管理者の役割は、音声ポリシーでのコールパークを有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="773b0-127">**CsUserAdministrator:** This administrator role can enable Call Park in voice policy.</span></span> <span data-ttu-id="773b0-128">この管理者ロールは、すべての音声構成に対して読み取り専用ビューでアクセスすることもできます。</span><span class="sxs-lookup"><span data-stu-id="773b0-128">This administrator role also has read-only view access to all voice configurations.</span></span>

  - <span data-ttu-id="773b0-129">**Csserveradministrator:** この管理者の役割は、サーバーとサービスの管理、監視、トラブルシューティングを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="773b0-129">**CsServerAdministrator:** This administrator role can manage, monitor, and troubleshoot servers and services.</span></span>

  - <span data-ttu-id="773b0-130">**Csadministrator:** この管理者ロールは、CsVoiceAdministrator、CsServerAdministrator、Csserveradministrator のすべてのタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="773b0-130">**CsAdministrator:** This administrator role can perform all of the tasks of CsVoiceAdministrator, CsServerAdministrator, and CsUserAdministrator.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="773b0-131">管理権限の詳細については、計画ドキュメントの「 <A href="lync-server-2013-planning-for-role-based-access-control.md">Lync Server 2013 での役割ベースのアクセス制御の計画</A> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="773b0-131">For details about administrative rights, see <A href="lync-server-2013-planning-for-role-based-access-control.md">Planning for role-based access control in Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="773b0-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="773b0-132">See Also</span></span>


[<span data-ttu-id="773b0-133">Lync Server 2013 でのエンタープライズボイスの展開</span><span class="sxs-lookup"><span data-stu-id="773b0-133">Deploying Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-deploying-enterprise-voice.md)  


[<span data-ttu-id="773b0-134">Lync Server 2013 の通話管理機能の計画</span><span class="sxs-lookup"><span data-stu-id="773b0-134">Planning for call management features in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-management-features.md)  
  

<span data-ttu-id="773b0-135"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="773b0-135"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

