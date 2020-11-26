---
title: 'Lync Server 2013: サポートされる仮想化テクノロジと既知の制限'
description: 'Lync Server 2013: サポートされている仮想化テクノロジと既知の制限。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Supported virtualization technologies and known limitations
ms:assetid: 6d3d749d-e840-4c05-afae-d6e69e7616aa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204982(v=OCS.15)
ms:contentKeyID: 48184428
ms.date: 02/07/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 745fa535462d29342f4c0a58674ee6487db42a6f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423562"
---
# <a name="supported-virtualization-technologies-and-known-limitations-in-lync-server-2013"></a><span data-ttu-id="9b016-103">Lync Server 2013 でサポートされる仮想化テクノロジと既知の制限</span><span class="sxs-lookup"><span data-stu-id="9b016-103">Supported virtualization technologies and known limitations in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9b016-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9b016-104">

<span> </span></span></span>

<span data-ttu-id="9b016-105">_**最終更新日:** 2017-02-06_</span><span class="sxs-lookup"><span data-stu-id="9b016-105">_**Topic Last Modified:** 2017-02-06_</span></span>

<span data-ttu-id="9b016-106">Lync VDI プラグインを使うと、サポートされている仮想化テクノロジで音声とビデオ通話を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="9b016-106">The Lync VDI plug-in allows audio and video calling for supported virtualization technologies.</span></span> <span data-ttu-id="9b016-107">これにより、microsoft Lync 2010 ホワイトペーパーの [クライアント仮想化](https://go.microsoft.com/fwlink/?linkid=330447) での Microsoft lync Server 2010 について説明されている機能が拡張されます。</span><span class="sxs-lookup"><span data-stu-id="9b016-107">This extends the functionality outlined for Microsoft Lync Server 2010 in the [Client Virtualization in Microsoft Lync 2010](https://go.microsoft.com/fwlink/?linkid=330447) white paper.</span></span> <span data-ttu-id="9b016-108">標準的な電話の規制に準拠するため、E911 のサポートも含まれています。</span><span class="sxs-lookup"><span data-stu-id="9b016-108">In compliance with standard telephone regulations, support for E911 is also included.</span></span> <span data-ttu-id="9b016-109">以下のセクションでは、Lync VDI プラグインでサポートされている仮想化テクノロジと既知の機能の制限について説明します。</span><span class="sxs-lookup"><span data-stu-id="9b016-109">The following sections describe the virtualization technologies that are supported by the Lync VDI plug-in and the known feature limitations.</span></span>

<div>

## <a name="support-for-virtualization-technologies"></a><span data-ttu-id="9b016-110">サポートされている仮想化テクノロジ</span><span class="sxs-lookup"><span data-stu-id="9b016-110">Support for Virtualization Technologies</span></span>

<span data-ttu-id="9b016-111">Lync VDI プラグインは、個人用仮想デスクトップシナリオでは完全なデスクトップリモート処理をサポートしていますが、リモートデスクトップセッションのシナリオではサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="9b016-111">The Lync VDI plug-in supports full desktop remoting in the personal virtual desktop scenario, but not in the remote desktop session scenario.</span></span> <span data-ttu-id="9b016-112">これらのシナリオは、次のように記述できます。</span><span class="sxs-lookup"><span data-stu-id="9b016-112">These scenarios can be described as follows:</span></span>

  - <span data-ttu-id="9b016-113">**サポート: カスタマイズされた仮想デスクトップまたは仮想デスクトップインフラストラクチャ (VDI)。**</span><span class="sxs-lookup"><span data-stu-id="9b016-113">**Supported: Personalized Virtual Desktops or Virtual Desktop Infrastructure (VDI).**</span></span>   <span data-ttu-id="9b016-114">このシナリオでは、各ユーザーがカスタマイズ可能な仮想デスクトップにログオンし、セッション間で保持されるファイルをデスクトップに保存することができます。</span><span class="sxs-lookup"><span data-stu-id="9b016-114">In this scenario, each user logs on to a customizable virtual desktop and is able to save files on the desktop that persist across sessions.</span></span> <span data-ttu-id="9b016-115">Microsoft リモートデスクトップサービス、VMware ホライズンビュー、Citrix XenDesktop は、Lync での使用がテストされている実装です。</span><span class="sxs-lookup"><span data-stu-id="9b016-115">Microsoft Remote Desktop Services, VMware Horizon View, and Citrix XenDesktop are implementations that have been tested for use with Lync.</span></span> <span data-ttu-id="9b016-116">Microsoft によってテストされたベンダー固有の VDI 環境とクライアントハードウェアの詳細については、「 [Microsoft Lync のインフラストラクチャ認定](https://go.microsoft.com/fwlink/?linkid=313435)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9b016-116">For information about vendor-specific VDI environments and client hardware that have been tested by Microsoft, see [Infrastructure qualified for Microsoft Lync](https://go.microsoft.com/fwlink/?linkid=313435).</span></span>

  - <span data-ttu-id="9b016-117">**サポートされないシナリオ: リモート デスクトップ セッション。**</span><span class="sxs-lookup"><span data-stu-id="9b016-117">**Not supported: Remote Desktop Sessions.**</span></span>   <span data-ttu-id="9b016-118">このシナリオでは、各ユーザーはカスタマイズできない汎用の仮想デスクトップ セッションにログオンします。</span><span class="sxs-lookup"><span data-stu-id="9b016-118">In this scenario, each user logs on to a generic virtual desktop session that cannot be customized.</span></span> <span data-ttu-id="9b016-119">このような実装の例には、マイクロソフト リモート デスクトップ セッション (RDSH) や Citrix XenApp と Citrix Receiver の組み合わせがあります。</span><span class="sxs-lookup"><span data-stu-id="9b016-119">Example implementations include Microsoft Remote Desktop Sessions (RDSH) and Citrix XenApp combined with Citrix Receiver.</span></span>

<span data-ttu-id="9b016-120">Lync VDI プラグインは、アプリケーションの仮想化などの他の仮想化テクノロジをサポートしていません。これにより、完全なアプリケーションをローカルでインストールする必要なく、アプリケーションを使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="9b016-120">The Lync VDI plug-in does not support other virtualization technologies, such as application virtualization, which allows the use of an application without requiring installation of the full application locally.</span></span> <span data-ttu-id="9b016-121">実装の例には、Citrix XenApp と Microsoft Application Virtualization (App-v) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9b016-121">Example implementations include Citrix XenApp and Microsoft Application Virtualization (App-V).</span></span> <span data-ttu-id="9b016-122">アプリケーションのストリーミング、アプリケーションのリモート処理、および混合型の仮想化モード (たとえば、完全なデスクトップリモート処理におけるアプリケーションのリモート処理) はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="9b016-122">Application streaming, application remoting, and mixed virtualization modes (for example, application remoting in full desktop remoting) are not supported.</span></span>

<span data-ttu-id="9b016-123">拡張性を許可するために、Lync VDI プラグインは動的仮想チャネル (DVCs) と呼ばれるプラットフォームに依存しない Api を使うように設計されています。</span><span class="sxs-lookup"><span data-stu-id="9b016-123">To allow extensibility, the Lync VDI plug-in was designed to use platform-independent APIs called Dynamic Virtual Channels (DVCs).</span></span> <span data-ttu-id="9b016-124">Lync で明示的にサポートされていないシナリオについては、「VDI ソリューションプロバイダーのサポートステートメント」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9b016-124">For scenarios that are not explicitly supported by Lync, refer to support statements from the VDI solution provider.</span></span>

</div>

<div>

## <a name="known-feature-limitations"></a><span data-ttu-id="9b016-125">既知の機能制限</span><span class="sxs-lookup"><span data-stu-id="9b016-125">Known Feature Limitations</span></span>

<span data-ttu-id="9b016-126">VDI 環境で Lync 2013 を使用する場合は、次のような制限があります。</span><span class="sxs-lookup"><span data-stu-id="9b016-126">The following are known limitations when you use Lync 2013 in a VDI environment:</span></span>

  - <span data-ttu-id="9b016-127">通話の委任と応答グループのエージェント匿名化) 機能は、制限されています。</span><span class="sxs-lookup"><span data-stu-id="9b016-127">There is limited support for Call Delegation and Response Group Agent Anonymization features.</span></span>

  - <span data-ttu-id="9b016-128">以下の機能はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="9b016-128">There is no support for the following features:</span></span>
    
      - <span data-ttu-id="9b016-129">統合オーディオ デバイスとビデオ デバイスのチューニング ページ</span><span class="sxs-lookup"><span data-stu-id="9b016-129">Integrated Audio Device and Video Device tuning pages.</span></span>
    
      - <span data-ttu-id="9b016-130">マルチビュー ビデオ</span><span class="sxs-lookup"><span data-stu-id="9b016-130">Multiple-view video.</span></span>
    
      - <span data-ttu-id="9b016-131">会話の録音</span><span class="sxs-lookup"><span data-stu-id="9b016-131">Recording of conversations.</span></span>
    
      - <span data-ttu-id="9b016-132">リモートデスクトップサービス (RDS)。</span><span class="sxs-lookup"><span data-stu-id="9b016-132">Remote Desktop Services (RDS).</span></span>
    
      - <span data-ttu-id="9b016-133">会議への匿名参加 (つまり、組織とフェデレーションされていない組織によってホストされている Lync 会議への参加)。</span><span class="sxs-lookup"><span data-stu-id="9b016-133">Joining meetings anonymously (that is, joining Lync meetings hosted by an organization that does not federate with your organization).</span></span>
    
      - <span data-ttu-id="9b016-134">Lync VDI プラグインと Lync Phone Edition デバイスの併用。</span><span class="sxs-lookup"><span data-stu-id="9b016-134">Using the Lync VDI plug-in along with a Lync Phone Edition device.</span></span>
    
      - <span data-ttu-id="9b016-135">ネットワーク停止時の通話の継続</span><span class="sxs-lookup"><span data-stu-id="9b016-135">Call continuity in case of a network outage.</span></span>
    
      - <span data-ttu-id="9b016-136">保留機能の着信音と音楽のカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="9b016-136">Customized ringtones and music-on-hold features.</span></span>

  - <span data-ttu-id="9b016-137">Lync VDI プラグインは、Microsoft 365 または Office 365 環境ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="9b016-137">The Lync VDI plug-in is not supported in a Microsoft 365 or Office 365 environment.</span></span>

<span data-ttu-id="9b016-138"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9b016-138"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

