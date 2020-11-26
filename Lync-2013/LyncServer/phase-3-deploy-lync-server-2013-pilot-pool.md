---
title: 'フェーズ 3: Lync Server 2013 パイロットプールの展開'
description: 'フェーズ 3: Lync Server 2013 パイロットプールを展開します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: 'Phase 3: Deploy Lync Server 2013 pilot pool'
ms:assetid: f12b1517-fb56-4ded-8323-57aa9fc9ea48
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205367(v=OCS.15)
ms:contentKeyID: 48185778
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f72f0cdd2e7d3b9e29891a4adc0ab0551539f465
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438457"
---
# <a name="phase-3-deploy-lync-server-2013-pilot-pool"></a><span data-ttu-id="3762d-103">フェーズ 3: Lync Server 2013 パイロットプールの展開</span><span class="sxs-lookup"><span data-stu-id="3762d-103">Phase 3: Deploy Lync Server 2013 pilot pool</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3762d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3762d-104">

<span> </span></span></span>

<span data-ttu-id="3762d-105">_**最終更新日:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="3762d-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="3762d-106">このセクションでは、Lync Server 2013 のパイロットプールを展開するために必要な手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="3762d-106">This section covers the steps required to deploy a pilot pool of Lync Server 2013.</span></span> <span data-ttu-id="3762d-107">Lync Server 2013 を展開するには、トポロジビルダーを使用して、展開するトポロジとコンポーネントを定義し、Lync Server 2013 コンポーネントの展開のための環境の準備、最初のフロントエンドサーバーでのトポロジの設計の公開、展開用のコンポーネントのための Lync Server 2013 ソフトウェアのインストールと構成を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="3762d-107">The deployment of Lync Server 2013 requires using Topology Builder to define your topology and the components you want to deploy, preparing your environment for deployment of the Lync Server 2013 components, publishing your topology design on the first Front End Server, and then installing and configuring Lync Server 2013 software for the components for your deployment.</span></span> <span data-ttu-id="3762d-108">完了すると、Lync Server 2013 パイロットプールの展開は既存の Lync Server 2010 プールと共存します。</span><span class="sxs-lookup"><span data-stu-id="3762d-108">When completed, your Lync Server 2013 pilot pool deployment will coexist with an existing Lync Server 2010 pool.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="3762d-109">このセクション中</span><span class="sxs-lookup"><span data-stu-id="3762d-109">In This Section</span></span>

  - [<span data-ttu-id="3762d-110">Lync Server の Active Directory の準備</span><span class="sxs-lookup"><span data-stu-id="3762d-110">Prepare Active Directory for Lync Server</span></span>](prepare-active-directory-for-lync-server.md)

  - [<span data-ttu-id="3762d-111">既存の展開環境からのトポロジのダウンロード</span><span class="sxs-lookup"><span data-stu-id="3762d-111">Download topology from existing deployment</span></span>](download-topology-from-existing-deployment.md)

  - [<span data-ttu-id="3762d-112">Lync Server 2013 パイロットプールの展開</span><span class="sxs-lookup"><span data-stu-id="3762d-112">Deploy Lync Server 2013 pilot pool</span></span>](deploy-lync-server-2013-pilot-pool.md)

  - [<span data-ttu-id="3762d-113">パイロット プールとレガシ プールの共存の確認</span><span class="sxs-lookup"><span data-stu-id="3762d-113">Verify pilot pool coexistence with legacy pool</span></span>](verify-pilot-pool-coexistence-with-legacy-pool.md)

  - [<span data-ttu-id="3762d-114">パイロット プールのレガシ エッジ サーバーへの接続</span><span class="sxs-lookup"><span data-stu-id="3762d-114">Connect pilot pool to legacy Edge Servers</span></span>](connect-pilot-pool-to-legacy-edge-servers.md)

  - [<span data-ttu-id="3762d-115">XMPP ゲートウェイ アクセス ポリシーおよび証明書の構成</span><span class="sxs-lookup"><span data-stu-id="3762d-115">Configure XMPP gateway access policies and certificates</span></span>](configure-xmpp-gateway-access-policies-and-certificates.md)

<span data-ttu-id="3762d-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3762d-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

