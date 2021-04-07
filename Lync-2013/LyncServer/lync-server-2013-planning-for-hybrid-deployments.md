---
title: 'Lync Server 2013: ハイブリッド展開の計画'
description: 'Lync Server 2013: ハイブリッド展開の計画。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for hybrid deployments
ms:assetid: f8b3d240-bc2e-42c9-acf8-d532d641a14c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205403(v=OCS.15)
ms:contentKeyID: 48185910
ms.date: 05/25/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 919f6058059fc9bfcb6bcb4f4c38140e53be6274
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424549"
---
# <a name="planning-for-lync-server-2013-hybrid-deployments"></a><span data-ttu-id="ed84f-103">Lync Server 2013 のハイブリッド展開の計画</span><span class="sxs-lookup"><span data-stu-id="ed84f-103">Planning for Lync Server 2013 hybrid deployments</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ed84f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ed84f-104">

<span> </span></span></span>

<span data-ttu-id="ed84f-105">_**トピック最終更新日:** 2016-05-25_</span><span class="sxs-lookup"><span data-stu-id="ed84f-105">_**Topic Last Modified:** 2016-05-25_</span></span>

<span data-ttu-id="ed84f-106">ハイブリッド展開を計画する際には、ユーザーとネットワーク インフラストラクチャに対して次の要件を考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed84f-106">You should consider the following requirements for users and your network infrastructure while planning for a hybrid deployment.</span></span>

<div>

## <a name="infrastructure-requirements"></a><span data-ttu-id="ed84f-107">インフラストラクチャ要件</span><span class="sxs-lookup"><span data-stu-id="ed84f-107">Infrastructure Requirements</span></span>

<span data-ttu-id="ed84f-108">ハイブリッド展開を実装して展開するには、環境で次を構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed84f-108">You must have the following configured in your environment in order to implement and deploy a hybrid deployment.</span></span>

  - <span data-ttu-id="ed84f-109">Skype for Business Online が有効になっている microsoft 365 または Office 365 組織。</span><span class="sxs-lookup"><span data-stu-id="ed84f-109">A Microsoft 365 or Office 365 organization with Skype for Business Online enabled.</span></span> <span data-ttu-id="ed84f-110">オンプレミス展開では、ハイブリッド構成に 1 つのテナントのみを使用できます。</span><span class="sxs-lookup"><span data-stu-id="ed84f-110">Note that you can use only a single tenant for a hybrid configuration with your on-premises deployment.</span></span>

  - <span data-ttu-id="ed84f-111">サポートされているトポロジに展開される、Skype for Business Server または Lync Server の 1 つのオンプレミス展開 (インフラストラクチャ)。</span><span class="sxs-lookup"><span data-stu-id="ed84f-111">A single on-premises deployment (infrastructure) of Skype for Business Server or Lync Server that is deployed in a supported topology.</span></span> <span data-ttu-id="ed84f-112">トポロジ要件を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ed84f-112">See Topology Requirements.</span></span>
    
    <span data-ttu-id="ed84f-113">ハイブリッド用に Lync Server 2013 または Lync Server 2010 展開を構成する方法については [、「Lync Server 2013](lync-server-2013-configuring-hybrid-deployments.md)ハイブリッド展開の構成」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ed84f-113">For information about configuring your Lync Server 2013 or Lync Server 2010 deployment for hybrid, see [Configuring Lync Server 2013 hybrid deployments](lync-server-2013-configuring-hybrid-deployments.md).</span></span>

  - <span data-ttu-id="ed84f-114">Skype for Business Server 2015 管理ツール。</span><span class="sxs-lookup"><span data-stu-id="ed84f-114">Skype for Business Server 2015 administrative tools.</span></span> <span data-ttu-id="ed84f-115">Lync Server 2013 または Lync Server 2010 を使用している場合は、Lync Server 2013 管理ツールを使用できます。</span><span class="sxs-lookup"><span data-stu-id="ed84f-115">If you are using Lync Server 2013 or Lync Server 2010, you can use the Lync Server 2013 administrative tools.</span></span>

  - <span data-ttu-id="ed84f-116">Microsoft 365 または Office 365 でシングル サインオンをサポートし、ユーザーがオンプレミスと同じログイン資格情報を使用して Office にサインインするには、Azure Active Directory (AAD) Connect のパスワード同期機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="ed84f-116">To support Single Sign-on with Microsoft 365 or Office 365 so that users can use the same login credentials for signing in to Office as they do on-premises, you can use the password sync features of Azure Active Directory (AAD) Connect.</span></span> <span data-ttu-id="ed84f-117">また、Microsoft 365 または AD 365 でのシングル サインオンに Active Directory フェデレーション サービス (Office FS) を使用できます。</span><span class="sxs-lookup"><span data-stu-id="ed84f-117">You can also use Active Directory Federation Services (AD FS) for single sign-on with Microsoft 365 or Office 365.</span></span>
    
    <span data-ttu-id="ed84f-118">詳細については、「オンプレミス ID と Azure Active Directory の統合」 [を参照してください](https://go.microsoft.com/fwlink/p/?linkid=619754)。</span><span class="sxs-lookup"><span data-stu-id="ed84f-118">For more information, see [Integrating your on-premises identities with Azure Active Directory](https://go.microsoft.com/fwlink/p/?linkid=619754).</span></span>

  - <span data-ttu-id="ed84f-119">オンプレミスとオンラインの Active Directory オブジェクトの同期を維持する単一のディレクトリ同期ソリューション。</span><span class="sxs-lookup"><span data-stu-id="ed84f-119">A single directory synchronization solution to keep your on-premises and online Active Directory objects synchronized.</span></span> <span data-ttu-id="ed84f-120">ディレクトリ同期の詳細については、「ディレクトリ統合ツール [」を参照してください](https://go.microsoft.com/fwlink/p/?linkid=530320)。</span><span class="sxs-lookup"><span data-stu-id="ed84f-120">For details about Directory Synchronization, see [Directory Integration Tools](https://go.microsoft.com/fwlink/p/?linkid=530320).</span></span>

</div>

<div>

## <a name="lync-client-support"></a><span data-ttu-id="ed84f-121">Lync クライアント サポート</span><span class="sxs-lookup"><span data-stu-id="ed84f-121">Lync Client Support</span></span>

<span data-ttu-id="ed84f-122">Lync クライアントでサポートされる機能と、オンプレミスとオンライン環境で使用できる機能にはいくつかの違いがあります。</span><span class="sxs-lookup"><span data-stu-id="ed84f-122">There are some differences in the features supported in Lync clients, as well as the features available in on-premises and online environments.</span></span> <span data-ttu-id="ed84f-123">組織のユーザーをホームする場所を決定する前に、Lync Server のさまざまな構成に対するクライアント サポートを表示できます。</span><span class="sxs-lookup"><span data-stu-id="ed84f-123">Before you decide where you want to home users in your organization, you can view the client support for the various configurations of Lync Server.</span></span> <span data-ttu-id="ed84f-124">Lync ハイブリッド展開では、次のクライアントが Skype for Business Online でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="ed84f-124">The following clients are supported with Skype for Business Online in a Lync hybrid deployment:</span></span>

  - <span data-ttu-id="ed84f-125">Lync 2010</span><span class="sxs-lookup"><span data-stu-id="ed84f-125">Lync 2010</span></span>

  - <span data-ttu-id="ed84f-126">Lync 2013</span><span class="sxs-lookup"><span data-stu-id="ed84f-126">Lync 2013</span></span>

  - <span data-ttu-id="ed84f-127">Lync Windows ストア アプリ</span><span class="sxs-lookup"><span data-stu-id="ed84f-127">Lync Windows Store app</span></span>

  - <span data-ttu-id="ed84f-128">Lync Web App</span><span class="sxs-lookup"><span data-stu-id="ed84f-128">Lync Web App</span></span>

  - <span data-ttu-id="ed84f-129">Lync Mobile</span><span class="sxs-lookup"><span data-stu-id="ed84f-129">Lync Mobile</span></span>

  - <span data-ttu-id="ed84f-130">Lync for Mac 2011</span><span class="sxs-lookup"><span data-stu-id="ed84f-130">Lync for Mac 2011</span></span>

  - <span data-ttu-id="ed84f-131">Lync Room System</span><span class="sxs-lookup"><span data-stu-id="ed84f-131">Lync Room System</span></span>

  - <span data-ttu-id="ed84f-132">Lync Basic 2013</span><span class="sxs-lookup"><span data-stu-id="ed84f-132">Lync Basic 2013</span></span>

<span data-ttu-id="ed84f-133">クライアント サポートの詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ed84f-133">For details about client support, see the following topics:</span></span>

  - [<span data-ttu-id="ed84f-134">Lync Online のクライアント</span><span class="sxs-lookup"><span data-stu-id="ed84f-134">Clients for Lync Online</span></span>](https://go.microsoft.com/fwlink/?linkid=281902)

  - [<span data-ttu-id="ed84f-135">Lync Server 2013 のクライアントの比較表</span><span class="sxs-lookup"><span data-stu-id="ed84f-135">Client comparison tables for Lync Server 2013</span></span>](lync-server-2013-desktop-client-comparison-tables.md)

  - [<span data-ttu-id="ed84f-136">Lync Server 2013 のモバイル クライアントの比較表</span><span class="sxs-lookup"><span data-stu-id="ed84f-136">Mobile client comparison tables for Lync Server 2013</span></span>](lync-server-2013-mobile-client-comparison-tables.md)

</div>

<span id="BKMK_Topology"></span>

<div>

## <a name="topology-requirements"></a><span data-ttu-id="ed84f-137">トポロジ要件</span><span class="sxs-lookup"><span data-stu-id="ed84f-137">Topology Requirements</span></span>

<span data-ttu-id="ed84f-138">Skype for Business Online とのハイブリッド展開を構成するには、次のいずれかのトポロジがサポートされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed84f-138">To configure your deployment for hybrid with Skype for Business Online, you need to have one of the following supported topologies:</span></span>

  - <span data-ttu-id="ed84f-139">Skype for Business Server 2015 を実行しているすべてのサーバーを含む Skype for Business Server 2015 展開。</span><span class="sxs-lookup"><span data-stu-id="ed84f-139">A Skype for Business Server 2015 deployment with all servers running Skype for Business Server 2015.</span></span>

  - <span data-ttu-id="ed84f-140">Lync Server 2013 を実行しているすべてのサーバーを含む Lync Server 2013 展開。</span><span class="sxs-lookup"><span data-stu-id="ed84f-140">A Lync Server 2013 deployment with all servers running Lync Server 2013.</span></span>

  - <span data-ttu-id="ed84f-141">Lync Server 2010 の展開では、Lync Server 2010 を実行しているすべてのサーバーに最新の累積的な更新プログラムが適用されます。</span><span class="sxs-lookup"><span data-stu-id="ed84f-141">A Lync Server 2010 deployment with all servers running Lync Server 2010 with the latest cumulative updates.</span></span>
    
      - <span data-ttu-id="ed84f-142">フェデレーション エッジ サーバーとフェデレーション エッジ サーバーからの次のホップ サーバーは、最新の累積的な更新プログラムを使用して Lync Server 2010 を実行している必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed84f-142">The federation Edge Server and next hop server from the federation Edge Server must be running Lync Server 2010 with the latest cumulative updates.</span></span>
    
      - <span data-ttu-id="ed84f-143">Skype for Business Server 2015 または Lync Server 2013 管理ツールは、少なくとも 1 つのサーバーまたは管理ワークステーションにインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed84f-143">The Skype for Business Server 2015 or Lync Server 2013 Administrative Tools must be installed on at least one server or management workstation.</span></span>

  - <span data-ttu-id="ed84f-144">Skype for Business Server 2015 を実行している少なくとも 1 つのサイトで、次のサーバーの役割を持つ Lync Server 2013 と Skype for Business Server 2015 の複合展開。</span><span class="sxs-lookup"><span data-stu-id="ed84f-144">A mixed Lync Server 2013 and Skype for Business Server 2015 deployment with the following server roles in at least one site running Skype for Business Server 2015:</span></span>
    
      - <span data-ttu-id="ed84f-145">少なくとも 1 台のエンタープライズ プールまたは Standard Edition サーバー </span><span class="sxs-lookup"><span data-stu-id="ed84f-145">At least one Enterprise Pool or Standard Edition server</span></span>
    
      - <span data-ttu-id="ed84f-146">SIP フェデレーションに関連づけられたディレクター プール (もしあれば)</span><span class="sxs-lookup"><span data-stu-id="ed84f-146">The Director Pool associated with SIP federation, if it exists</span></span>
    
      - <span data-ttu-id="ed84f-147">SIP フェデレーションに関連づけられたエッジ プール (もしあれば)</span><span class="sxs-lookup"><span data-stu-id="ed84f-147">The Edge Pool associated with SIP federation</span></span>

  - <span data-ttu-id="ed84f-148">Lync Server 2010 と Skype for Business Server 2015 の混在展開。次のサーバーは、Skype for Business Server 2015 を実行している少なくとも 1 つのサイトで役割を果たします。</span><span class="sxs-lookup"><span data-stu-id="ed84f-148">A mixed Lync Server 2010 and Skype for Business Server 2015 deployment with the following servers roles in at least one site running Skype for Business Server 2015:</span></span>
    
      - <span data-ttu-id="ed84f-149">少なくとも 1 台のエンタープライズ プールまたは Standard Edition サーバー </span><span class="sxs-lookup"><span data-stu-id="ed84f-149">At least one Enterprise Pool or Standard Edition server</span></span>
    
      - <span data-ttu-id="ed84f-150">SIP フェデレーションに関連づけられたディレクター プール (もしあれば)</span><span class="sxs-lookup"><span data-stu-id="ed84f-150">The Director Pool associated with SIP federation, if it exists</span></span>
    
      - <span data-ttu-id="ed84f-151">サイトの SIP フェデレーションに関連づけられたエッジ プール</span><span class="sxs-lookup"><span data-stu-id="ed84f-151">The Edge Pool associated with SIP federation for the Site</span></span>

  - <span data-ttu-id="ed84f-152">Lync Server 2013 を実行している少なくとも 1 つのサイトで、次のサーバーの役割を持つ Lync Server 2010 と Lync Server 2013 の複合展開。</span><span class="sxs-lookup"><span data-stu-id="ed84f-152">A mixed Lync Server 2010 and Lync Server 2013 deployment with the following server roles in at least one site running Lync Server 2013:</span></span>
    
      - <span data-ttu-id="ed84f-153">サイトの少なくとも 1 台のエンタープライズ プールまたは Standard Edition サーバー</span><span class="sxs-lookup"><span data-stu-id="ed84f-153">At least one Enterprise Pool or Standard Edition server in the site</span></span>
    
      - <span data-ttu-id="ed84f-154">SIP フェデレーションに関連づけられたディレクター プール (もしサイトにあれば)</span><span class="sxs-lookup"><span data-stu-id="ed84f-154">The Director Pool associated with SIP federation, if it exists in the site</span></span>
    
      - <span data-ttu-id="ed84f-155">サイトの SIP フェデレーションに関連づけられたエッジ プール</span><span class="sxs-lookup"><span data-stu-id="ed84f-155">The Edge Pool associated with SIP federation for the site</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="ed84f-156">オンプレミスと UNRESOLVED_TOKEN_VAL (skypeforbusiness) Online の間のユーザー移動を含むすべてのユーザー管理は、インストールされている最新バージョンの管理ツールを使用して行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed84f-156">All user management, including user moves between on-premises and UNRESOLVED_TOKEN_VAL(skypeforbusiness) Online, needs to be done using the latest installed version of the administrative tools.</span></span> <span data-ttu-id="ed84f-157">管理ツールは、既存のオンプレミス展開とインターネットに接続できる別のサーバーにインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed84f-157">The administrative tools must be installed on a separate server that has connect access to the existing on-premises deployment and to the Internet.</span></span> <span data-ttu-id="ed84f-158">オンプレミス展開から UNRESOLVED_TOKEN_VAL(skype16_online) にユーザーを移動する <A href="https://docs.microsoft.com/powershell/module/skype/Move-CsUser">Move-CsUser</A> コマンドレットは、オンプレミス展開に接続されている管理ツールから実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed84f-158">The <A href="https://docs.microsoft.com/powershell/module/skype/Move-CsUser">Move-CsUser</A> cmdlet to move users from your on-premises deployment to UNRESOLVED_TOKEN_VAL(skype16_online) must be run from the administrative tools connected to your on-premises deployment.</span></span>



</div>

<span data-ttu-id="ed84f-159">サポートされるトポロジの詳細については [、「Lync Server 2013](lync-server-2013-supported-topologies.md)でサポートされるトポロジ」および [「Lync Server 2013](https://go.microsoft.com/fwlink/p/?linkid=398709)リファレンス: エンタープライズ ハイブリッド展開用トポロジ」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ed84f-159">For more information about supported topologies, see [Supported topologies in Lync Server 2013](lync-server-2013-supported-topologies.md), and [Lync Server 2013 Reference Topologies for Enterprise Hybrid Deployments](https://go.microsoft.com/fwlink/p/?linkid=398709).</span></span>

<span data-ttu-id="ed84f-160">ハイブリッド展開に関するトラブルシューティング情報と、PowerShell を Lync Online に接続する方法については [、「Lync Online: Lync PowerShell](https://go.microsoft.com/fwlink/p/?linkid=306718)およびハイブリッド トラブルシューティング」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ed84f-160">For troubleshooting information about hybrid deployments and connecting PowerShell to Lync Online, see [Lync Online: Lync PowerShell and Hybrid Troubleshooting](https://go.microsoft.com/fwlink/p/?linkid=306718).</span></span>

</div>

<div>

## <a name="requirements-for-federation-allowedblocked-lists"></a><span data-ttu-id="ed84f-161">フェデレーション許可/ブロックリストの要件</span><span class="sxs-lookup"><span data-stu-id="ed84f-161">Requirements for Federation Allowed/Blocked Lists</span></span>

<span data-ttu-id="ed84f-p108">許可ドメインの一覧には、パートナー エッジの完全修飾ドメイン名 (FQDN) が構成されているドメインが含まれます。これらは *許可パートナー サーバー* または *ダイレクト フェデレーション パートナー* と呼ばれることもあります。オープン フェデレーションとクローズド フェデレーションの違いをよく理解しておくことが必要です。オンプレミス展開ではこれらはそれぞれ *パートナーの検出* および *許可パートナー ドメインの一覧* と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="ed84f-p108">The Allowed domains list includes domains that have a partner Edge fully qualified domain name (FQDN) configured. These are sometimes referred to as *allowed partner servers* or *direct federation partners*. You should be familiar with the difference between Open Federation and Closed Federation, referred to as *partner discovery* and *allowed partner domain list*, respectively, in on-premises deployments.</span></span>

<span data-ttu-id="ed84f-165">ハイブリッド展開を正しく構成するには、次の必要条件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed84f-165">The following requirements must be met to successfully configure a hybrid deployment:</span></span>

  - <span data-ttu-id="ed84f-166">ドメイン マッチングは、オンプレミス展開と Microsoft 365 または Office 365 組織で同じように構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed84f-166">Domain matching must be configured the same for your on-premises deployment and your Microsoft 365 or Office 365 organization.</span></span> <span data-ttu-id="ed84f-167">オンプレミス展開でパートナーの検出が有効になっている場合、オンライン テナントではオープン フェデレーションを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed84f-167">If partner discovery is enabled on the on-premises deployment, then open federation must be configured for your online tenant.</span></span> <span data-ttu-id="ed84f-168">パートナーの検出が無効になっている場合、オンライン テナントではクローズド フェデレーションを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed84f-168">If partner discovery is not enabled, then closed federation must be configured for your online tenant.</span></span>

  - <span data-ttu-id="ed84f-169">オンプレミス展開における禁止ドメインの一覧はオンライン テナントの禁止ドメインの一覧と正確に一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed84f-169">The Blocked domains list in the on-premises deployment must exactly match the Blocked domains list for your online tenant.</span></span>

  - <span data-ttu-id="ed84f-170">オンプレミス展開における許可ドメインの一覧はオンライン テナントの許可ドメインの一覧と正確に一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed84f-170">The Allowed domains list in the on-premises deployment must exactly match the Allowed domains list for your online tenant.</span></span>

  - <span data-ttu-id="ed84f-171">Lync Online コントロール パネルを使用して構成される、オンライン テナントの外部通信に対してフェデレーションを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed84f-171">Federation must be enabled for the external communications for the online tenant, which is configured by using the Lync Online Control Panel.</span></span>

</div>

<div>

## <a name="dns-settings"></a><span data-ttu-id="ed84f-172">DNS の設定</span><span class="sxs-lookup"><span data-stu-id="ed84f-172">DNS Settings</span></span>

<span data-ttu-id="ed84f-173">ハイブリッド展開用の DNS レコードを作成する場合、すべての Lync 外部 DNS レコードがオンプレミス インフラストラクチャをポイントしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed84f-173">When creating DNS records for hybrid deployments, all Lync external DNS records should point to the on-premises infrastructure.</span></span> <span data-ttu-id="ed84f-174">必要な DNS レコードの詳細については [、Lync Server 2013](lync-server-2013-domain-name-system-dns-requirements.md)のドメイン ネーム システム (DNS) の要件を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ed84f-174">For details on required DNS records, please refer to [Domain Name System (DNS) requirements for Lync Server 2013](lync-server-2013-domain-name-system-dns-requirements.md).</span></span>

<span data-ttu-id="ed84f-175">さらに、次の表で説明している DNS 解決が使用しているオンプレミス展開で機能することを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed84f-175">Additionally you need to ensure that the DNS resolution described in the following table works in your on-premises deployment:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ed84f-176">DNS レコード</span><span class="sxs-lookup"><span data-stu-id="ed84f-176">DNS record</span></span></p></td>
<td><p><span data-ttu-id="ed84f-177">解決方法</span><span class="sxs-lookup"><span data-stu-id="ed84f-177">Resolvable by</span></span></p></td>
<td><p><span data-ttu-id="ed84f-178">DNS 要件</span><span class="sxs-lookup"><span data-stu-id="ed84f-178">DNS requirement</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed84f-179">_sipfederationtls._tcp の DNS SRV レコード。 &lt;sipdomain.com エッジの外部 IP に対して解決するサポートされている SIP ドメインすべてについて &gt;</span><span class="sxs-lookup"><span data-stu-id="ed84f-179">DNS SRV record for _sipfederationtls._tcp.&lt;sipdomain.com&gt; for all supported SIP domains resolving to Access Edge external IP(s)</span></span></p></td>
<td><p><span data-ttu-id="ed84f-180">エッジ サーバー</span><span class="sxs-lookup"><span data-stu-id="ed84f-180">Edge server(s)</span></span></p></td>
<td><p><span data-ttu-id="ed84f-p111">ハイブリッド展開でフェデレーション通信を有効にする。オンプレミスとオンラインで分割される SIP ドメイン用のフェデレーション トラフィックのルートをエッジ サーバーで認識している必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed84f-p111">Enable federated communication in a hybrid configuration. The Edge Server needs to know where to route federated traffic for the SIP domain that is split between on premises and online.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed84f-183">エッジ Web 会議サービス FQDN の DNS A レコード、たとえば、webcon.contoso.com は Web 会議のエッジ外部 IP に解決される</span><span class="sxs-lookup"><span data-stu-id="ed84f-183">DNS A record(s) for Edge Web Conferencing Service FQDN, e.g. webcon.contoso.com resolving to Web Conferencing Edge external IP(s)</span></span></p></td>
<td><p><span data-ttu-id="ed84f-184">ユーザーのコンピューターが接続している会社内ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ed84f-184">Internal corporate network connected users’ computers</span></span></p></td>
<td><p><span data-ttu-id="ed84f-p112">オンライン ユーザーを有効にして、オンプレミスのホストされた会議でのコンテンツを提供または表示する。コンテンツには、PowerPoint ファイル、ホワイトボード、投票、および共有メモがあります。</span><span class="sxs-lookup"><span data-stu-id="ed84f-p112">Enable online users to present or view content in on-premises hosted meetings. Content includes PowerPoint files, whiteboards, polls, and shared notes.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ed84f-187">所属する組織での DNS の構成方法によっては、内部 DNS 解決をこれらのレコードに適用するために、対応する SIP ドメインに対して組織内でホストする DNS ゾーンにこれらのレコードを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed84f-187">Depending on how DNS is configured in your organization, you may need to add these records to the internal hosted DNS zone for the corresponding SIP domain(s) to provide internal DNS resolution to these records.</span></span>

</div>

<div>

## <a name="firewall-considerations"></a><span data-ttu-id="ed84f-188">ファイアウォールに関する考慮事項</span><span class="sxs-lookup"><span data-stu-id="ed84f-188">Firewall Considerations</span></span>

<span data-ttu-id="ed84f-p113">ネットワーク上のコンピューターは、標準のインターネット DNS 参照を実行できる必要があります。これらのコンピューターが標準のインターネット サイトに接続できれば、ネットワークはこの要件を満たしています。</span><span class="sxs-lookup"><span data-stu-id="ed84f-p113">Computers on your network must be able to perform standard Internet DNS lookups. If these computers can reach standard Internet sites, your network meets this requirement.</span></span>

<span data-ttu-id="ed84f-191">Microsoft Online Services データ センターの場所によっては、ワイルドカード ドメイン名 (.outlook.com からのトラフィックなど) に基づいて接続を受け入れるネットワーク ファイアウォール デバイスも構成する \* 必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed84f-191">Depending on the location of your Microsoft Online Services data center, you must also configure your network firewall devices to accept connections based on wildcard domain names (for example, all traffic from \*.outlook.com).</span></span> <span data-ttu-id="ed84f-192">組織のファイアウォールがワイルドカードを使用した名前の構成方法をサポートしない場合は、許可する IP アドレスの範囲および特定のポートを手動で決める必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed84f-192">If your organization’s firewalls do not support wildcard name configurations, you will have to manually determine the IP address ranges that you would like to allow and the specified ports.</span></span>

<span data-ttu-id="ed84f-193">365 の URL [と IP Officeのヘルプ トピックを参照してください](https://go.microsoft.com/fwlink/p/?linkid=252942)。</span><span class="sxs-lookup"><span data-stu-id="ed84f-193">Refer to the Help topic [Office 365 URLs and IP address ranges](https://go.microsoft.com/fwlink/p/?linkid=252942).</span></span>

</div>

<span id="b"></span>

<div>

## <a name="port-and-protocol-requirements"></a><span data-ttu-id="ed84f-194">ポートとプロトコルの要件</span><span class="sxs-lookup"><span data-stu-id="ed84f-194">Port and Protocol Requirements</span></span>

<span data-ttu-id="ed84f-195">Lync Server 2013 内部通信のポート要件に加えて、次のポートも構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed84f-195">In addition to the port requirements for internal Lync Server 2013 communication, you must also configure the following ports.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ed84f-196">プロトコル/ポート</span><span class="sxs-lookup"><span data-stu-id="ed84f-196">Protocol / Port</span></span></th>
<th><span data-ttu-id="ed84f-197">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="ed84f-197">Applications</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ed84f-198">TCP 443</span><span class="sxs-lookup"><span data-stu-id="ed84f-198">TCP 443</span></span></p></td>
<td><p><span data-ttu-id="ed84f-199">受信を開く</span><span class="sxs-lookup"><span data-stu-id="ed84f-199">Open inbound</span></span></p>
<ul>
<li><p><span data-ttu-id="ed84f-200">Active Directory フェデレーション サービス (フェデレーション サーバーの役割)</span><span class="sxs-lookup"><span data-stu-id="ed84f-200">Active Directory Federation Services (federation server role)</span></span></p>
<p><span data-ttu-id="ed84f-201">詳細については、「FS 役割サービス <a href="https://go.microsoft.com/fwlink/p/?linkid=281899">のADを参照してください</a>。</span><span class="sxs-lookup"><span data-stu-id="ed84f-201">For more information, see <a href="https://go.microsoft.com/fwlink/p/?linkid=281899">Understanding AD FS Role Services</a>.</span></span></p></li>
<li><p><span data-ttu-id="ed84f-202">Active Directory フェデレーション サービス (プロキシ サーバーの役割)</span><span class="sxs-lookup"><span data-stu-id="ed84f-202">Active Directory Federation Services (proxy server role)</span></span></p></li>
<li><p><span data-ttu-id="ed84f-203">Microsoft Online Services ポータル</span><span class="sxs-lookup"><span data-stu-id="ed84f-203">Microsoft Online Services Portal</span></span></p></li>
<li><p><span data-ttu-id="ed84f-204">自分のポータル サイト</span><span class="sxs-lookup"><span data-stu-id="ed84f-204">My Company Portal</span></span></p></li>
<li><p><span data-ttu-id="ed84f-205">Outlook Web App</span><span class="sxs-lookup"><span data-stu-id="ed84f-205">Outlook Web App</span></span></p></li>
<li><p><span data-ttu-id="ed84f-206">Lync クライアント (オンプレミスの Lync Server から Lync Online への通信)</span><span class="sxs-lookup"><span data-stu-id="ed84f-206">Lync client (communication to Lync Online from on-premises Lync Server)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed84f-207">TCP 80 と 443</span><span class="sxs-lookup"><span data-stu-id="ed84f-207">TCP 80 and 443</span></span></p></td>
<td><p><span data-ttu-id="ed84f-208">受信を開く</span><span class="sxs-lookup"><span data-stu-id="ed84f-208">Open inbound</span></span></p>
<ul>
<li><p><span data-ttu-id="ed84f-209">Microsoft Online Services ディレクトリ同期ツール</span><span class="sxs-lookup"><span data-stu-id="ed84f-209">Microsoft Online Services Directory Synchronization Tool</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed84f-210">TCP 5061</span><span class="sxs-lookup"><span data-stu-id="ed84f-210">TCP 5061</span></span></p></td>
<td><p><span data-ttu-id="ed84f-211">エッジ サーバーで受信/送信を開く</span><span class="sxs-lookup"><span data-stu-id="ed84f-211">Open inbound/outbound on the Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed84f-212">PSOM/TLS 443</span><span class="sxs-lookup"><span data-stu-id="ed84f-212">PSOM/TLS 443</span></span></p></td>
<td><p><span data-ttu-id="ed84f-213">データ共有セッションの受信/送信を開く</span><span class="sxs-lookup"><span data-stu-id="ed84f-213">Open inbound/outbound for data sharing sessions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed84f-214">STUN/TCP 443</span><span class="sxs-lookup"><span data-stu-id="ed84f-214">STUN/TCP 443</span></span></p></td>
<td><p><span data-ttu-id="ed84f-215">音声、ビデオ、アプリケーション共有セッションの受信/送信を開く</span><span class="sxs-lookup"><span data-stu-id="ed84f-215">Open inbound/outbound for audio, video, application sharing sessions</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed84f-216">STUN/UDP 3478</span><span class="sxs-lookup"><span data-stu-id="ed84f-216">STUN/UDP 3478</span></span></p></td>
<td><p><span data-ttu-id="ed84f-217">音声とビデオ セッションの受信/送信を開く</span><span class="sxs-lookup"><span data-stu-id="ed84f-217">Open inbound/outbound for audio and video sessions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed84f-218">RTP/TCP 50000-59999</span><span class="sxs-lookup"><span data-stu-id="ed84f-218">RTP/TCP 50000-59999</span></span></p></td>
<td><p><span data-ttu-id="ed84f-219">音声セッションとビデオ セッションの送信を開く</span><span class="sxs-lookup"><span data-stu-id="ed84f-219">Open outbound for audio and video sessions</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="user-accounts-and-data"></a><span data-ttu-id="ed84f-220">ユーザー アカウントとデータ</span><span class="sxs-lookup"><span data-stu-id="ed84f-220">User Accounts and Data</span></span>

<span data-ttu-id="ed84f-221">Lync Server 2013 のハイブリッド展開では、ユーザー アカウントが Active Directory ドメイン サービスで作成されるので、Lync Online にホームするユーザーは、まずオンプレミス展開で作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed84f-221">In a Lync Server 2013 hybrid deployment, any user that you want to home in Lync Online must first be created in the on-premises deployment, so that the user account is created in Active Directory Domain Services.</span></span> <span data-ttu-id="ed84f-222">その後、ユーザーを Skype for Business Online に移動すると、ユーザーの連絡先リストが移動されます。</span><span class="sxs-lookup"><span data-stu-id="ed84f-222">You can then move the user to Skype for Business Online, which will move the user’s contact list.</span></span>

<span data-ttu-id="ed84f-223">Lync オンプレミスと Lync Online 展開の間でユーザー アカウントを AD FS および Dirsync と同期する場合、ユーザーが Lync Online に移動されていない場合でも、組織内のすべての Lync ユーザーの AD アカウントをオンプレミスとオンラインの Lync 展開の間で同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed84f-223">When you synchronize user accounts between your Lync on-premises and Lync Online deployments with AD FS and Dirsync, you need to synchronize the AD accounts for all Lync users in your organization between your on-premises and online Lync deployments, even if users are not moved to Lync Online.</span></span> <span data-ttu-id="ed84f-224">すべてのユーザーを同期しない場合、組織のオンプレミス展開のユーザーとオンライン ユーザーとの間の通信が正常に動作しない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ed84f-224">If you do not synchronize all users, communication between on-premises and online users in your organization may not work as expected.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="ed84f-225">ユーザーが Microsoft 365 管理センターのオンライン ポータルを使用して作成された場合、ユーザー アカウントはオンプレミスの Active Directory と同期されません。また、ユーザーはオンプレミスの Active Directory に存在しません。</span><span class="sxs-lookup"><span data-stu-id="ed84f-225">If the user is created by using the online portal for Microsoft 365 admin center, the user account will not be synchronized with on-premises Active Directory, and the user will not exist in the on-premises Active Directory.</span></span> <span data-ttu-id="ed84f-226">Lync Online でユーザーを既に作成済みで、オンプレミスの Lync Server とのハイブリッドを構成する場合は、「Lync Online から Lync <A href="lync-server-2013-moving-users-from-lync-online-to-lync-on-premises.md">Server 2013</A>のオンプレミスへのユーザーの移動」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ed84f-226">If you have already created users in Lync Online, and want to configure hybrid with an on-premises Lync Server, see <A href="lync-server-2013-moving-users-from-lync-online-to-lync-on-premises.md">Moving users from Lync Online to Lync on-premises in Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="ed84f-227">また、ハイブリッド展開を計画する場合は、次のユーザー関連の問題も考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed84f-227">You should also consider the following user-related issues when planning for a hybrid deployment.</span></span>

  - <span data-ttu-id="ed84f-228">**ユーザーの連絡先**   Lync Online ユーザーの連絡先の制限は 250 です。</span><span class="sxs-lookup"><span data-stu-id="ed84f-228">**User contacts**   The limit for contacts for Lync Online users is 250.</span></span> <span data-ttu-id="ed84f-229">その数を超えた連絡先は、アカウントが Lync Online に移動されるときにユーザーの連絡先リストから削除されます。</span><span class="sxs-lookup"><span data-stu-id="ed84f-229">Any contacts beyond that number will be removed from the user’s contact list when the account is moved to Lync Online.</span></span>

  - <span data-ttu-id="ed84f-230">**インスタント メッセージングとプレゼンス**   ユーザーの連絡先リスト、グループ、およびアクセス制御リスト (ACL) はユーザー アカウントと一緒に移行されます。</span><span class="sxs-lookup"><span data-stu-id="ed84f-230">**Instant Messaging and Presence**   User contact lists, groups, and access control lists (ACLs) are migrated with the user account.</span></span>

  - <span data-ttu-id="ed84f-231">**会議データ、会議コンテンツ、スケジュールされた会議**   このコンテンツは、ユーザー アカウントでは移行されません。</span><span class="sxs-lookup"><span data-stu-id="ed84f-231">**Conferencing data, meeting content, and scheduled meetings**   This content is not migrated with the user account.</span></span> <span data-ttu-id="ed84f-232">ユーザーは、アカウントが Lync Online に移行された後で会議を予約し直す必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed84f-232">Users must reschedule meetings after their accounts are migrated to Lync Online.</span></span>

</div>

<div>

## <a name="user-policies-and-features"></a><span data-ttu-id="ed84f-233">ユーザー ポリシーと機能</span><span class="sxs-lookup"><span data-stu-id="ed84f-233">User Policies and Features</span></span>

  - <span data-ttu-id="ed84f-234">Lync Server 2013 ハイブリッド環境では、ユーザーはインスタント メッセージング、音声、会議をオンプレミスまたはオンラインで有効にできますが、両方を同時に有効にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="ed84f-234">In a Lync Server 2013 hybrid environment, users can be enabled for Instant Messaging, voice, and meetings either on-premises or online, but not both simultaneously.</span></span>

  - <span data-ttu-id="ed84f-235">**Lync クライアント**    一部のユーザーは、Lync Online に移動するときに新しいクライアント バージョンが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="ed84f-235">**Lync Client**    Some users may require a new client version when they are moved to Lync Online.</span></span> <span data-ttu-id="ed84f-236">Office Communications Server 2007 R2 の場合、Lync Online に移行する前に、ユーザーを Lync Server 2013 プールに移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed84f-236">For Office Communications Server 2007 R2, users must be moved to a Lync Server 2013 pool prior to migration to Lync Online.</span></span>
    
    <span data-ttu-id="ed84f-237">クライアント サポートの詳細については [、「Lync Online](https://go.microsoft.com/fwlink/p/?linkid=281902) のクライアントとサポートされる Lync クライアントとネットワーク ポート構成 [」を参照してください](https://go.microsoft.com/fwlink/p/?linkid=281901)。</span><span class="sxs-lookup"><span data-stu-id="ed84f-237">For more information about client support, see [Clients for Lync Online](https://go.microsoft.com/fwlink/p/?linkid=281902) and [Supported Lync clients and network port configurations](https://go.microsoft.com/fwlink/p/?linkid=281901).</span></span>

  - <span data-ttu-id="ed84f-238">**オンプレミスのポリシーと構成 (ユーザー以外)**   オンライン ポリシーとオンプレミス ポリシーには、個別の構成が必要です。</span><span class="sxs-lookup"><span data-stu-id="ed84f-238">**On-premises policies and configuration (non-user)**   Online and on-premises policies require separate configuration.</span></span> <span data-ttu-id="ed84f-239">両方に適用されるグローバル ポリシーを設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="ed84f-239">You cannot set global policies that apply to both.</span></span>

<span data-ttu-id="ed84f-240"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ed84f-240"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>
