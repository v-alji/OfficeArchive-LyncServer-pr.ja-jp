---
title: 'Lync Server 2013: ブランチ サイトの展開'
description: 'Lync Server 2013: ブランチサイトの展開。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying branch sites
ms:assetid: 1475dee0-66ae-4ee5-b6f1-7409b4bbff45
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398217(v=OCS.15)
ms:contentKeyID: 48183483
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d653e3f06de832693d97bfb229f122a67c28640e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430092"
---
# <a name="deploying-branch-sites-in-lync-server-2013"></a><span data-ttu-id="0e5e0-103">Lync Server 2013 でのブランチ サイトの展開</span><span class="sxs-lookup"><span data-stu-id="0e5e0-103">Deploying branch sites in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0e5e0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0e5e0-104">

<span> </span></span></span>

<span data-ttu-id="0e5e0-105">_**最終更新日:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="0e5e0-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="0e5e0-106">ブランチサイトユーザーは、ブランチサイトが関連付けられているセントラルサイトのサーバーから、Lync Server 2013 のほとんどの機能を利用できます。</span><span class="sxs-lookup"><span data-stu-id="0e5e0-106">Branch site users get most of their Lync Server 2013 functionality from the server at the central site that the branch site is associated with.</span></span> <span data-ttu-id="0e5e0-107">各ブランチサイトは、1つのセントラルサイトと関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="0e5e0-107">Each branch site is associated with exactly one central site.</span></span> <span data-ttu-id="0e5e0-108">公衆交換電話網 (PSTN) との間で通話を発信するには、ブランチサイトに次のいずれかを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="0e5e0-108">To provide calls to and from the public switched telephone network (PSTN), a branch site might contain any of the following:</span></span>

  - <span data-ttu-id="0e5e0-109">PSTN ゲートウェイと、おそらく Meditation Server</span><span class="sxs-lookup"><span data-stu-id="0e5e0-109">A PSTN gateway and possibly a Meditation Server</span></span>

  - <span data-ttu-id="0e5e0-110">SIP トランク</span><span class="sxs-lookup"><span data-stu-id="0e5e0-110">A SIP trunk</span></span>

  - <span data-ttu-id="0e5e0-111">構内交換 (PBX) を使用する既存の音声インフラストラクチャ</span><span class="sxs-lookup"><span data-stu-id="0e5e0-111">An existing voice infrastructure with a private branch exchange (PBX)</span></span>

  - <span data-ttu-id="0e5e0-112">Survivable Branch アプライアンス</span><span class="sxs-lookup"><span data-stu-id="0e5e0-112">A Survivable Branch Appliance</span></span>

  - <span data-ttu-id="0e5e0-113">Survivable ブランチサーバー</span><span class="sxs-lookup"><span data-stu-id="0e5e0-113">A Survivable Branch Server</span></span>

<span data-ttu-id="0e5e0-114">Survivable Branch Appliance または Survivable ブランチサーバーを使用しているブランチサイトでは、このようなソリューションを使用することなく、広域ネットワークまたはセントラルサイトの障害が発生した場合よりも高い弾力性があります。</span><span class="sxs-lookup"><span data-stu-id="0e5e0-114">Branch sites with a Survivable Branch Appliance or a Survivable Branch Server are more resilient in times of wide-area network or central site failures than branch sites without one of these solutions.</span></span> <span data-ttu-id="0e5e0-115">たとえば、Survivable Branch Appliance または Survivable Branch Server が展開されているサイトでは、ブランチサイトをセントラルサイトに接続しているネットワークがダウンしている場合でも、ユーザーは PSTN 通話の発信と受信を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="0e5e0-115">For example, in a site with a Survivable Branch Appliance or a Survivable Branch Server deployed, users can still make and receive PSTN calls if the network connecting the branch site to the central site is down.</span></span> <span data-ttu-id="0e5e0-116">ブランチサイトの回復性を実現するもう1つの方法として、PSTN ゲートウェイまたは SIP トランクを使用して、ブランチサイトでのフルスケールの Lync Server 展開を利用することができます。</span><span class="sxs-lookup"><span data-stu-id="0e5e0-116">Another way to achieve branch-site resiliency is by using a PSTN gateway or a SIP trunk with a full-scale Lync Server deployment at the branch site.</span></span>

<span data-ttu-id="0e5e0-117">前提条件などの計画に関する考慮事項を含む、組織に適したブランチサイトの展開の詳細については、「 [Lync server 2013 での PSTN 接続の計画](lync-server-2013-planning-for-pstn-connectivity.md) 」および「計画ドキュメントの [lync server 2013 でのブランチサイトのボイスの回復性の計画](lync-server-2013-planning-for-branch-site-voice-resiliency.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0e5e0-117">For details about which branch site deployment is right for your organization, including prerequisites and other planning considerations, see [Planning for PSTN connectivity in Lync Server 2013](lync-server-2013-planning-for-pstn-connectivity.md) and [Planning for branch-site voice resiliency in Lync Server 2013](lync-server-2013-planning-for-branch-site-voice-resiliency.md) in the Planning documentation.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="0e5e0-118">このセクション中</span><span class="sxs-lookup"><span data-stu-id="0e5e0-118">In This Section</span></span>

  - [<span data-ttu-id="0e5e0-119">Lync Server 2013 におけるブランチ サイトでの PSTN 接続の提供</span><span class="sxs-lookup"><span data-stu-id="0e5e0-119">Providing PSTN connectivity at a branch site in Lync Server 2013</span></span>](lync-server-2013-providing-pstn-connectivity-at-a-branch-site.md)

  - [<span data-ttu-id="0e5e0-120">Lync Server 2013 を使用した存続可能ブランチ アプライアンスまたはサーバーの展開</span><span class="sxs-lookup"><span data-stu-id="0e5e0-120">Deploying a Survivable Branch Appliance or Server with Lync Server 2013</span></span>](lync-server-2013-deploying-a-survivable-branch-appliance-or-server.md)

<span data-ttu-id="0e5e0-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0e5e0-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

