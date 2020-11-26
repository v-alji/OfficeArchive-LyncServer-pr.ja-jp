---
title: 'Lync Server 2013: 複数のトランクのサポート'
description: 'Lync Server 2013: 複数のトランクのサポート。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Multiple trunk support
ms:assetid: a1309c09-ad9a-4c54-9650-4e3f5b2a4a00
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205127(v=OCS.15)
ms:contentKeyID: 48184948
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3bbabb90405b3fdae47a59ba8a0798743943216d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425208"
---
# <a name="multiple-trunk-support-in-lync-server-2013"></a><span data-ttu-id="31475-103">Lync Server 2013 での複数のトランクのサポート</span><span class="sxs-lookup"><span data-stu-id="31475-103">Multiple trunk support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="31475-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="31475-104">

<span> </span></span></span>

<span data-ttu-id="31475-105">_**最終更新日:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="31475-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="31475-106">Lync Server 2013 機能は、ゲートウェイと仲介サーバー間の複数の関連付けをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="31475-106">Lync Server 2013 functionality supports multiple associations between gateways and Mediation Servers.</span></span> <span data-ttu-id="31475-107">これらの関連付けは、仲介サーバープールと公衆交換電話網 (PSTN) ゲートウェイ、セッション境界コントローラー (SBC)、または ip-pbx との間の論理的な関連付けであるトランクを定義することによって行われます。</span><span class="sxs-lookup"><span data-stu-id="31475-107">These associations are made by defining a trunk, which is a logical association between a Mediation Server pool and a public switched telephone network (PSTN) gateway, Session Border Controller (SBC), or IP-PBX.</span></span> <span data-ttu-id="31475-108">トポロジビルダーを使用して、ゲートウェイを仲介サーバーに関連付けます (つまり、trunks)。</span><span class="sxs-lookup"><span data-stu-id="31475-108">Use the Topology Builder to associate gateways with Mediation Servers (that is, trunks).</span></span>

  - <span data-ttu-id="31475-109">Lync Server 2013 でトランクを割り当てまたは削除するには、まず、トポロジビルダーで樹幹を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="31475-109">To assign or remove a trunk in Lync Server 2013, you must first define a trunk in Topology Builder.</span></span> <span data-ttu-id="31475-110">トランクは、仲介サーバーの完全修飾ドメイン名 (FQDN)、仲介サーバーのリッスンポート、ゲートウェイの FQDN、ゲートウェイのリスニングポートで構成されます。</span><span class="sxs-lookup"><span data-stu-id="31475-110">A trunk consists of the following association: Mediation Server fully qualified domain name (FQDN), the Mediation Server listening port, the gateway FQDN, and the gateway listening port.</span></span>

  - <span data-ttu-id="31475-111">複数の trunks を構成するために、同じゲートウェイと仲介サーバー間に複数の関連付けを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="31475-111">To configure multiple trunks, you can create multiple associations between the same gateway and the Mediation Server.</span></span> <span data-ttu-id="31475-112">これにより、エンタープライズ Voip インフラストラクチャのさらなる弾力性が提供されます。これは、プライベート支店交換 (PBX) 間の運用シナリオで特に便利です。</span><span class="sxs-lookup"><span data-stu-id="31475-112">This provides additional resiliency to the Enterprise Voice infrastructure, which is especially useful in private branch exchange (PBX) interoperational scenarios.</span></span>

<span data-ttu-id="31475-113">トランクが定義されている場合は、ルートに関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="31475-113">When a trunk is defined, it must be associated to a route.</span></span> <span data-ttu-id="31475-114">トランクをルートに関連付けるには、トポロジビルダーでトランクの単純な名前を定義します。</span><span class="sxs-lookup"><span data-stu-id="31475-114">To associate a trunk to a route, you define a simple name for the trunk in Topology Builder.</span></span> <span data-ttu-id="31475-115">この簡易名は、Lync Server コントロールパネルでトランク名として使用されます。ここでは、trunks をルートに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="31475-115">This simple name is used as the trunk name in the Lync Server Control Panel, where trunks can be associated with routes.</span></span> <span data-ttu-id="31475-116">簡単なトランク名は、Lync Server 管理シェルからのゲートウェイ名として使用されます。</span><span class="sxs-lookup"><span data-stu-id="31475-116">The simple trunk name is used as the gateway name from the Lync Server Management Shell.</span></span>

    New-CsVoiceRoute -Identity <RouteId> -NumberPattern <String> -PstnUsages @{add="<UsageString>"} -PstnGatewayList @{add="<TrunkSimpleName>"}

<span data-ttu-id="31475-117">管理者は、仲介サーバーに関連付けられている既定のトランクを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="31475-117">The administrator must select a default trunk associated with a Mediation Server.</span></span> <span data-ttu-id="31475-118">トポロジビルダーで、関連する仲介サーバーを右クリックし、[ **プロパティ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31475-118">From the Topology Builder, right-click the associated Mediation Server, and then click **Properties**.</span></span> <span data-ttu-id="31475-119">仲介サーバーの既定のゲートウェイを指定します。</span><span class="sxs-lookup"><span data-stu-id="31475-119">Specify the default gateway for the Mediation Server.</span></span>

<span data-ttu-id="31475-120">次の図は、各仲介サーバーとゲートウェイに対して定義されている複数の trunks を示しています。</span><span class="sxs-lookup"><span data-stu-id="31475-120">The following diagram illustrates the multiple trunks that are defined for each Mediation Server and gateway.</span></span>

<span data-ttu-id="31475-121">**M-N トランクルーティング**</span><span class="sxs-lookup"><span data-stu-id="31475-121">**M-N Trunk Routing**</span></span>

<span data-ttu-id="31475-122">![複数のトランクの割り当て](images/JJ205127.c61cd9a7-d8d9-4e02-83b9-ab62519a48c4(OCS.15).jpg "複数のトランクの割り当て")</span><span class="sxs-lookup"><span data-stu-id="31475-122">![Multiple trunk assignments.](images/JJ205127.c61cd9a7-d8d9-4e02-83b9-ab62519a48c4(OCS.15).jpg "Multiple trunk assignments.")</span></span>

<span data-ttu-id="31475-123"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="31475-123"></div>

<span> </span>

</div>

</div>

</span></span></div>

