---
title: 'Lync Server 2013: Microsoft Lync 展開方法の決定'
description: 'Lync Server 2013: Microsoft Lync の展開方法を決定する。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deciding how to deploy Microsoft Lync
ms:assetid: 6ca677d3-745d-4935-8f05-19274a8bccf2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204979(v=OCS.15)
ms:contentKeyID: 48184423
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a800b51dfddc6f2c99e42c8f117056ed4091b6a5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431233"
---
# <a name="deciding-how-to-deploy-lync-server-2013"></a><span data-ttu-id="4dc80-103">Lync Server 2013 展開方法の決定</span><span class="sxs-lookup"><span data-stu-id="4dc80-103">Deciding how to deploy Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4dc80-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4dc80-104">

<span> </span></span></span>

<span data-ttu-id="4dc80-105">_**最終更新日:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="4dc80-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="4dc80-106">Lync を計画する場合、最初の主な決定として、Microsoft Lync: Lync Server 2013 をオンプレミスに展開する方法、またはクラウドで Microsoft 365 または Office 365 を使用して Lync Online を展開する方法が挙げられます。</span><span class="sxs-lookup"><span data-stu-id="4dc80-106">When planning for Lync, the first major decision is how to deploy Microsoft Lync: as Lync Server 2013 on premises, or Lync Online with Microsoft 365 or Office 365 in the cloud.</span></span>

  - <span data-ttu-id="4dc80-107">**Lync Server 2013 オンプレミス** : lync のすべての機能セットが提供され、展開の構成、カスタマイズ、および操作に最適な柔軟性が提供されます。</span><span class="sxs-lookup"><span data-stu-id="4dc80-107">**Lync Server 2013 on-premises** : This choice provides the complete Lync feature set and provides ultimate flexibility in configuring, customizing, and operating your deployment.</span></span> <span data-ttu-id="4dc80-108">すべてのサーバーがオンサイトにインストールされ、組織によって管理されます。</span><span class="sxs-lookup"><span data-stu-id="4dc80-108">All servers are installed onsite and maintained by your organization.</span></span> <span data-ttu-id="4dc80-109">オンプレミスの展開では、Lync Server のさまざまな機能が提供されます。</span><span class="sxs-lookup"><span data-stu-id="4dc80-109">An on-premises deployment provides the full range of Lync Server features.</span></span>

  - <span data-ttu-id="4dc80-110">**クラウドでの Lync Online** Lync Online は、Lync Server のビジネスクラス機能を犠牲にすることなく、クラウドベースのインスタントメッセージング、プレゼンス、会議のコストとアジリティの向上を希望する組織向けに設計されています。</span><span class="sxs-lookup"><span data-stu-id="4dc80-110">**Lync Online in the cloud** Lync Online is designed for organizations that want the cost and agility benefits of cloud-based instant messaging, presence, and meetings without sacrificing the business-class capabilities of Lync Server.</span></span> <span data-ttu-id="4dc80-111">Lync Online を使用すると、Microsoft は必要なサーバーインフラストラクチャを展開して管理し、継続的なメンテナンス、パッチ、アップグレードを処理します。</span><span class="sxs-lookup"><span data-stu-id="4dc80-111">With Lync Online, Microsoft deploys and maintains the required server infrastructure, and handles ongoing maintenance, patches, and upgrades.</span></span> <span data-ttu-id="4dc80-112">オンプレミスの展開で利用できる機能の一部は、Lync Online では利用できません。</span><span class="sxs-lookup"><span data-stu-id="4dc80-112">Some features available in an on-premises deployment are not available in Lync Online.</span></span>

<span data-ttu-id="4dc80-113">どのような種類の展開を使用するかは、展開するワークロードと組織の地理的状態とビジネス状態によって異なります。</span><span class="sxs-lookup"><span data-stu-id="4dc80-113">Which type of deployment would be best for you depends on the workloads you want to deploy, and your organization’s geographical and business status.</span></span>

<div>

## <a name="lync-server"></a><span data-ttu-id="4dc80-114">Lync Server</span><span class="sxs-lookup"><span data-stu-id="4dc80-114">Lync Server</span></span>

<span data-ttu-id="4dc80-115">オンプレミスの Lync Server 展開は、次のシナリオに適しています。</span><span class="sxs-lookup"><span data-stu-id="4dc80-115">An on-premises Lync Server deployment is best for the following scenarios:</span></span>

  - <span data-ttu-id="4dc80-116">**完全なエンタープライズ Voip 機能**   PBX の代わりとして、または高度な通話機能を使用する完全なエンタープライズボイスソリューションの展開を計画している場合は、オンプレミスの Lync Server の展開が必要です。</span><span class="sxs-lookup"><span data-stu-id="4dc80-116">**Full Enterprise Voice Capabilities**   If you plan to deploy a full Enterprise Voice solution to replace your PBX or which uses advanced calling features, an on-premises Lync Server deployment is required.</span></span> <span data-ttu-id="4dc80-117">オンプレミスは、PBX システムと trunks との直接接続、および応答グループやコールパークなどの高度な電話機能をサポートします。</span><span class="sxs-lookup"><span data-stu-id="4dc80-117">On-premises supports direct connectivity with PBX systems and trunks, and advanced phone features such as response groups and call park.</span></span> <span data-ttu-id="4dc80-118">現時点では、Lync Online はこれらの機能をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="4dc80-118">Lync Online does not currently support these features.</span></span>

  - <span data-ttu-id="4dc80-119">**メディア品質コントロール**   通話受付制御 (CAC) 機能や QoS (Quality of Service) 機能など、さまざまな種類のメディア品質保証機能が必要な場合は、オンプレミスの展開が必要になります。</span><span class="sxs-lookup"><span data-stu-id="4dc80-119">**Media Quality Controls**   If you want the full range of media quality assurance features, such as Call Admission Control (CAC) and Quality of Service (QoS) features, you will want an on-premises deployment .</span></span>

  - <span data-ttu-id="4dc80-120">**常設チャット**   組織に常設チャットを展開する必要がある場合は、オンプレミスの展開を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4dc80-120">**Persistent Chat**   If you need to deploy Persistent chat for your organization, you must choose an on-premises deployment.</span></span>

  - <span data-ttu-id="4dc80-121">**サードパーティのサーバーアプリケーション**   オンプレミスの展開のみが、Microsoft ユニファイドコミュニケーションマネージ API (UCMA) を使用する信頼されたサードパーティアプリケーションと連携できます。</span><span class="sxs-lookup"><span data-stu-id="4dc80-121">**3rd-Party Server Applications**   Only on-premises deployments can work with trusted 3rd-party applications that use the Microsoft Unified Communications Managed API (UCMA).</span></span>

  - <span data-ttu-id="4dc80-122">**地域のサポートが必要な多国籍/地方企業**   複数の国または地域にデータセンターがあり、各地域にサーバーを展開して管理する必要がある場合は、この種類の地域管理機能を提供できるように、オンプレミス展開をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="4dc80-122">**Multi-National/Multi-Regional Companies Needing Regional Support**   If you have datacenters in multiple countries or regions and need servers to be deployed and managed on a regional basis, an on-premises deployment is best, as it provides this type of regional management capabilities.</span></span>

  - <span data-ttu-id="4dc80-123">**ポリシー、レポート、アップグレードを完全に制御**   する  オンプレミスの Lync Server 展開機能を使用すると、サーバーとクライアントのすべてのポリシー、監視およびその他のレポート、アップグレードのタイミングなどへのアクセスが可能になります。</span><span class="sxs-lookup"><span data-stu-id="4dc80-123">**Complete control over policies, reports, and upgrades**   With an on premises Lync Server deployment, you have access to the full set of server and client policies, Monitoring and other reports, and timing of upgrades.</span></span> <span data-ttu-id="4dc80-124">Lync Online には、ポリシー設定とレポートのサブセットが用意されています。このウィンドウには、アップグレードを承認するための重要なウィンドウが含まれています。</span><span class="sxs-lookup"><span data-stu-id="4dc80-124">Lync Online provides a subset of policy setting and reports, and provides a limited, though significant, window for accepting upgrades.</span></span>

</div>

<div>

## <a name="lync-online"></a><span data-ttu-id="4dc80-125">Lync Online</span><span class="sxs-lookup"><span data-stu-id="4dc80-125">Lync Online</span></span>

<span data-ttu-id="4dc80-126">上に挙げた要因が自分にとって重要ではない場合は、[Lync Online] を選んで、展開と管理性をさらに向上させることができます。</span><span class="sxs-lookup"><span data-stu-id="4dc80-126">If none of the factors in the preceding list are critical for you, you may want to choose Lync Online, for simpler deployment and manageability.</span></span> <span data-ttu-id="4dc80-127">Lync Online は、強力な IM、プレゼンス、会議機能のセットを提供します。また、組織内のユーザー間での音声通話とビデオ通話も可能になります。</span><span class="sxs-lookup"><span data-stu-id="4dc80-127">Lync Online provides a robust IM, presence and conferencing feature set, and also enables voice and video calls over IP between users in your organization.</span></span>

<span data-ttu-id="4dc80-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4dc80-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>
