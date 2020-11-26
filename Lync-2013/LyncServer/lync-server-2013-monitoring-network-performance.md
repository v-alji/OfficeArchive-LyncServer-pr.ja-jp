---
title: 'Lync Server 2013: ネットワーク パフォーマンスの監視'
description: 'Lync Server 2013: ネットワークのパフォーマンスを監視します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Monitoring network performance
ms:assetid: bc3a01da-91eb-4c0c-9598-35e5e46b00f6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720923(v=OCS.15)
ms:contentKeyID: 63969647
ms.date: 04/27/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0ead7e3f9001b06c783c9b22327581e795a20322
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425347"
---
# <a name="monitoring-network-performance-in-lync-server-2013"></a><span data-ttu-id="b46dd-103">Lync Server 2013 でのネットワーク パフォーマンスの監視</span><span class="sxs-lookup"><span data-stu-id="b46dd-103">Monitoring network performance in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b46dd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b46dd-104">

<span> </span></span></span>

<span data-ttu-id="b46dd-105">_**最終更新日:** 2016-04-27_</span><span class="sxs-lookup"><span data-stu-id="b46dd-105">_**Topic Last Modified:** 2016-04-27_</span></span>

<span data-ttu-id="b46dd-106">Lync Server 2013 は、ネットワークに大きく依存して、インスタントメッセージング (IM)、音声通話、またはビデオ通信を通じて、ユーザー間の通信を可能にする、リアルタイムの通信技術です。</span><span class="sxs-lookup"><span data-stu-id="b46dd-106">Lync Server 2013 is a real-time communications technology that relies heavily on the network to enable communication between users—either through instant messaging (IM), voice calls, or video communication.</span></span> <span data-ttu-id="b46dd-107">そのため、ユーザーが選択したコミュニケーションのモダリティが最適なエクスペリエンスを実現することを保証するために、ネットワークパフォーマンスを継続的に監視することが重要です。</span><span class="sxs-lookup"><span data-stu-id="b46dd-107">It is therefore important to monitor the network performance continuously to help guarantee that a user’s chosen communication modality provides the best possible experience.</span></span>

<span data-ttu-id="b46dd-108">ネットワークパフォーマンスは、次の2つのレベルで測定できます。</span><span class="sxs-lookup"><span data-stu-id="b46dd-108">Network performance can be measured at two levels:</span></span>

  - <span data-ttu-id="b46dd-109">**全体的なネットワークパフォーマンス**   このレベルのパフォーマンス測定では、組織は、ネットワークの "大きな画像" ビューを作成することができ、通常はサードパーティのネットワーク監視システムを使用して実装されます。</span><span class="sxs-lookup"><span data-stu-id="b46dd-109">**Overall network performance**   This level of performance measurement will allow an organization to create a "big-picture" view of their network and is usually implemented through third-party network monitoring systems.</span></span> <span data-ttu-id="b46dd-110">これらのシステムでは、管理者が特定のネットワークコンポーネントの正常性をいつでも判断できるように、ルーターなどのリモートネットワークデバイスからパフォーマンスと容量のデータを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="b46dd-110">These systems will receive performance and capacity data from remote network devices such as routers and switched throughout the network to allow administrators to determine the health of any given network component at any time of day.</span></span>

  - <span data-ttu-id="b46dd-111">**個々のサーバーのパフォーマンス**   このレベルのパフォーマンス測定は、特定のサーバーに制限されています。また、管理者は、特定のパフォーマンスの問題のトラブルシューティングや、特定の期間における個々のサーバーのパフォーマンスを測定するために、キャパシティ計画プロセスの一環として、特定のサーバーのネットワークパフォーマンスを距離するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="b46dd-111">**Individual server performance**   This level of performance measurement is limited to a specific server and will help administrators with gauging the network performance of a specific server to either help with troubleshooting a specific performance issue or to gauge the respective server’s performance over a given period as part of a capacity planning process.</span></span>

<span data-ttu-id="b46dd-112">次のセクションで説明されているツールを使用して、ネットワークを監視することができます。</span><span class="sxs-lookup"><span data-stu-id="b46dd-112">You can monitor the network by using the tools described in the following sections.</span></span>

<div>

## <a name="tools-for-overall-network-performance-monitoring"></a><span data-ttu-id="b46dd-113">ネットワークパフォーマンスの全体的な監視用のツール</span><span class="sxs-lookup"><span data-stu-id="b46dd-113">Tools for Overall Network Performance Monitoring</span></span>

<div>

## <a name="system-center-operations-manager-2012"></a><span data-ttu-id="b46dd-114">System Center Operations Manager 2012</span><span class="sxs-lookup"><span data-stu-id="b46dd-114">System Center Operations Manager 2012</span></span>

<span data-ttu-id="b46dd-115">System Center Operations Manager は、IT 環境全体のサービスレベルを向上させるためのカスタマイズと拡張が容易なエンドツーエンドのサービス管理を提供します。</span><span class="sxs-lookup"><span data-stu-id="b46dd-115">System Center Operations Manager provides end-to-end service management that is easy to customize and extend for improved service levels across an IT environment.</span></span> <span data-ttu-id="b46dd-116">これにより、運用および IT 管理チームは、配布された IT サービスの正常性に影響する問題を特定して解決することができます。</span><span class="sxs-lookup"><span data-stu-id="b46dd-116">This enables Operations and IT Management teams to identify, and resolve issues affecting the health of distributed IT services.</span></span> <span data-ttu-id="b46dd-117">エンドツーエンドのサービス管理は、Microsoft ベースの環境に限定されません。</span><span class="sxs-lookup"><span data-stu-id="b46dd-117">End-to-end service management is not restricted to Microsoft-based environments.</span></span> <span data-ttu-id="b46dd-118">管理用の Web サービス (WS-MANAGEMENT)、簡易ネットワーク管理プロトコル (SNMP)、パートナーソリューションをサポートしているため、Microsoft オペレーティングシステムとハードウェアを実行していないシステムは、System Center Operations Manager 2012 内のサービス監視に含めることができます。</span><span class="sxs-lookup"><span data-stu-id="b46dd-118">Support for Web Services for Management (WS-Management), Simple Network Management Protocol (SNMP), and partner solutions allow for systems that do not run Microsoft operating systems and hardware to be included in service monitoring within System Center Operations Manager 2012.</span></span>

</div>

<div>

## <a name="system-center-operations-manager-2012-and-third-party-network-management-solutions"></a><span data-ttu-id="b46dd-119">System Center Operations Manager 2012 とサードパーティのネットワーク管理ソリューション</span><span class="sxs-lookup"><span data-stu-id="b46dd-119">System Center Operations Manager 2012 and Third-Party Network Management Solutions</span></span>

<span data-ttu-id="b46dd-120">**EMC Smarts**   Operations Manager 向けの EMC ソリューションを使用すると、サービスレベルに影響する問題をすばやく解決できます。</span><span class="sxs-lookup"><span data-stu-id="b46dd-120">**EMC Smarts**   EMC Solutions for Operations Manager help you quickly resolve issues affecting service levels throughout.</span></span> <span data-ttu-id="b46dd-121">Operations Manager 用の EMC ソリューションを使用することで、1つの統合された自動ソリューションで IT サービスチェーン全体を管理および監視することができます。</span><span class="sxs-lookup"><span data-stu-id="b46dd-121">By using EMC Solutions for Operations Manager, you can manage and monitor your whole IT service chain with one integrated, automated solution.</span></span> <span data-ttu-id="b46dd-122">パフォーマンスと可用性の問題の根本原因を簡単に特定し、それらをより迅速に解決して効果とコストを削減します。</span><span class="sxs-lookup"><span data-stu-id="b46dd-122">You'll easily identify the root causes of performance and availability issues, and resolve them faster which reduces effects and costs.</span></span> <span data-ttu-id="b46dd-123">主な利点は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="b46dd-123">Key benefits include the following:</span></span>

  - <span data-ttu-id="b46dd-124">高度で使いやすい管理によって、手作業での並べ替えやフィルター処理が困難なアラートの代わりに戦略的ビジネス価値を実現することができます。</span><span class="sxs-lookup"><span data-stu-id="b46dd-124">Advanced, easy-to-use management   Focus on delivering strategic business value instead of manually sorting and filtering confusing alerts.</span></span>

  - <span data-ttu-id="b46dd-125">**より高速な解像度**   IT の問題を解決し、ビジネスニーズにすばやく対応し、効果とコストを削減します。</span><span class="sxs-lookup"><span data-stu-id="b46dd-125">**Faster resolution**   Solve IT issues and respond to business needs faster, reducing effect and cost.</span></span>

  - <span data-ttu-id="b46dd-126">**操作の合理化**   複数の管理ツール、アプリケーション、およびターミナルを組み合わせることで、IT の複雑さを回避します。</span><span class="sxs-lookup"><span data-stu-id="b46dd-126">**Streamlined operations**   Avoid IT complexity by combining multiple management tools, applications, and terminals.</span></span>

<span data-ttu-id="b46dd-127">詳細については、次のページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b46dd-127">More information can be found here:</span></span>

[<span data-ttu-id="b46dd-128">Microsoft System Center Operations Manager</span><span class="sxs-lookup"><span data-stu-id="b46dd-128">Microsoft System Center Operations Manager</span></span>](https://go.microsoft.com/fwlink/p/?linkid=243651)

[<span data-ttu-id="b46dd-129">Microsoft System Center Operations Manager のソリューション</span><span class="sxs-lookup"><span data-stu-id="b46dd-129">Solutions for Microsoft System Center Operations Manager</span></span>](http://www.emc.com/collateral/software/data-sheet/h6135-server-manager-ds.pdf)

</div>

<div>

## <a name="third-party-solutions"></a><span data-ttu-id="b46dd-130">サードパーティのソリューション</span><span class="sxs-lookup"><span data-stu-id="b46dd-130">Third-Party Solutions</span></span>

<span data-ttu-id="b46dd-131">Hp ネットワーク **管理センター (以前は Hp OpenView と呼ばれています)**[Hp ネットワーク管理センター](http://www8.hp.com/us/en/software-solutions/network-management/index.html?%26zn=bto%26cp=1-11-15-119_4000_100__)では、ネットワークの可用性とパフォーマンスを向上させるために、統合されたフォールトおよびパフォーマンス管理を実現しています。   </span><span class="sxs-lookup"><span data-stu-id="b46dd-131">**HP Network Management Center (previously known as HP OpenView)**   [HP Network Management Center](http://www8.hp.com/us/en/software-solutions/network-management/index.html?%26zn=bto%26cp=1-11-15-119_4000_100__) provides integrated fault and performance management to improve network availability and performance.</span></span> <span data-ttu-id="b46dd-132">ネットワーク管理センターは、障害、パフォーマンス、構成、および変更管理を統合する HP 自動ネットワーク管理ソリューションの一部です。</span><span class="sxs-lookup"><span data-stu-id="b46dd-132">Network Management Center is part of the HP automated network management solution that unifies fault, performance, configuration, and change management.</span></span>

<span data-ttu-id="b46dd-133">**Cisco のネットワーク管理とオートメーション製品**   企業向けには、Cisco には、CiscoWorks LAN 管理ソリューションや Cisco ネットワーク分析モジュールなど、さまざまな管理製品が用意されており、運用効率の向上とネットワークのダウンタイムの削減に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="b46dd-133">**Cisco Network Management and Automation products**   For the Enterprise, Cisco has several management products available including CiscoWorks LAN Management Solution and Cisco Network Analysis Module, to help improve operational efficiency and reduce network downtime.</span></span> <span data-ttu-id="b46dd-134">これらの製品に関するその他の情報については、の Cisco web サイトを参照してください [https://www.cisco.com/en/US/products/sw/netmgtsw/index.html](https://www.cisco.com/en/us/products/sw/netmgtsw/index.html) 。</span><span class="sxs-lookup"><span data-stu-id="b46dd-134">For additional data on these products, refer to the Cisco website at [https://www.cisco.com/en/US/products/sw/netmgtsw/index.html](https://www.cisco.com/en/us/products/sw/netmgtsw/index.html).</span></span>

<span data-ttu-id="b46dd-135">簡易ネットワーク管理プロトコル (SNMP) 簡易ネットワーク管理プロトコル (SNMP) は、TCP/IP ネットワークを管理するための戦略を定義するネットワーク管理標準です。</span><span class="sxs-lookup"><span data-stu-id="b46dd-135">Simple Network Management Protocol (SNMP)   Simple Network Management Protocol (SNMP) is a network management standard that defines a strategy for managing TCP/IP networks.</span></span> <span data-ttu-id="b46dd-136">SNMP では、ネットワークに関する構成と状態の情報を取得し、その情報を指定のコンピューターに送信してイベントを監視することができます。</span><span class="sxs-lookup"><span data-stu-id="b46dd-136">SNMP enables you to capture configuration and status information about the network, and send the information to a designated computer for event monitoring.</span></span> <span data-ttu-id="b46dd-137">この規格に基づくネットワーク管理プロトコルは、次のような分散アーキテクチャを使用しています。</span><span class="sxs-lookup"><span data-stu-id="b46dd-137">This standards based network management protocol uses a distributed architecture that includes the following:</span></span>

  - <span data-ttu-id="b46dd-138">複数の管理ノード。各ノードには、管理インストルメンテーションへのリモートアクセスを提供するエージェントと呼ばれる SNMP エンティティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b46dd-138">Multiple managed nodes, each with an SNMP entity called an agent which provides remote access to management instrumentation.</span></span>

  - <span data-ttu-id="b46dd-139">管理要素を監視および制御するために管理アプリケーションを実行する、マネージャーと呼ばれる少なくとも1つの SNMP エンティティ。</span><span class="sxs-lookup"><span data-stu-id="b46dd-139">At least one SNMP entity known as a manager which runs management applications to monitor and control managed elements.</span></span> <span data-ttu-id="b46dd-140">管理要素は、ホストやルーターなどのデバイスです。</span><span class="sxs-lookup"><span data-stu-id="b46dd-140">Managed elements are devices such as hosts, routers, and so on.</span></span> <span data-ttu-id="b46dd-141">これらのユーザーは、管理情報にアクセスすることで監視および制御されます。</span><span class="sxs-lookup"><span data-stu-id="b46dd-141">They are monitored and controlled by accessing their management information.</span></span>

  - <span data-ttu-id="b46dd-142">管理プロトコル SNMP は、管理ステーションとエージェントの間で管理情報を伝えるために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b46dd-142">A management protocol, SNMP, is used to communicate management information between the management stations and agents.</span></span> <span data-ttu-id="b46dd-143">管理情報とは、管理情報ベース (MIB) と呼ばれる仮想情報ストア内に存在する管理対象オブジェクトのコレクションを指します。</span><span class="sxs-lookup"><span data-stu-id="b46dd-143">Management information refers to a collection of managed objects that live in a virtual information store called a Management Information Base (MIB).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b46dd-144">サードパーティのネットワーク監視ソリューションの例は、上記に記載されています。</span><span class="sxs-lookup"><span data-stu-id="b46dd-144">Examples of third-party network monitoring solutions are provided above.</span></span> <span data-ttu-id="b46dd-145">このリストは確定的なものではありません。また、Microsoft は特定のベンダーソリューションに対応していません。</span><span class="sxs-lookup"><span data-stu-id="b46dd-145">This list is not definitive and Microsoft does not favor any specific vendor solution.</span></span> <span data-ttu-id="b46dd-146">組織に最適なネットワーク監視ソリューションを決定するには、ネットワークサービスプロバイダーまたは各テクノロジプロバイダーに問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="b46dd-146">Consult with a network service provider and or your respective technology provider to determine the best network monitoring solution for your organization.</span></span>



</div>

</div>

</div>

<div>

## <a name="tools-for-monitoring-individual-server-network-performance"></a><span data-ttu-id="b46dd-147">個々のサーバーのネットワークパフォーマンスを監視するためのツール</span><span class="sxs-lookup"><span data-stu-id="b46dd-147">Tools for Monitoring Individual Server Network Performance</span></span>

<div>

## <a name="system-center-operations-manager-2012"></a><span data-ttu-id="b46dd-148">System Center Operations Manager 2012</span><span class="sxs-lookup"><span data-stu-id="b46dd-148">System Center Operations Manager 2012</span></span>

<span data-ttu-id="b46dd-149">System Center Operations Manager 2012 を使用すると、管理者は Windows Server 2012 管理パックを通じて個々のサーバーのネットワークパフォーマンスを表示することができます。 Windows Server オペレーティングシステム管理パックには、管理者がネットワークアダプターのパフォーマンスとアダプターの正常性を監視できる "パフォーマンス" 管理パックが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b46dd-149">System Center Operations Manager 2012 would allow administrators to view network performance of individual servers through the Windows Server 2012 Management Pack: The Windows Server operating system management pack includes a "Performance" management pack that would allow administrators to monitor Network Adapter performance and adapter health.</span></span>

</div>

<div>

## <a name="windows-network-monitor"></a><span data-ttu-id="b46dd-150">Windows ネットワークモニター</span><span class="sxs-lookup"><span data-stu-id="b46dd-150">Windows Network Monitor</span></span>

<span data-ttu-id="b46dd-151">サーバー上のリソース使用状況の収集、表示、分析、ネットワークトラフィックの測定を行います。</span><span class="sxs-lookup"><span data-stu-id="b46dd-151">Collects, displays, analyzes resource usage on a server, and measures network traffic.</span></span> <span data-ttu-id="b46dd-152">ネットワークモニターは、ネットワークアクティビティを排他的に監視します。</span><span class="sxs-lookup"><span data-stu-id="b46dd-152">Network Monitor exclusively monitors network activity.</span></span> <span data-ttu-id="b46dd-153">ネットワークデータをキャプチャして分析し、そのデータをパフォーマンスログと共に使用することにより、ネットワークの使用状況の確認、ネットワークの問題の特定、将来のネットワークニーズの予測を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="b46dd-153">By capturing and analyzing network data, and using this data with performance logs, you can determine the network usage, identify network issues, and forecast future network needs.</span></span>

<span data-ttu-id="b46dd-154">ネットワークモニター3.4 の詳細と、ネットワークモニターのインストールと構成、データのキャプチャと分析の方法については、次のセッションを参照してください。ネットワークモニター3.3 の概要。</span><span class="sxs-lookup"><span data-stu-id="b46dd-154">For more information about Network Monitor 3.4, and to learn how to install and configure Network Monitor and capture and analyze data, review this session: Network Monitor 3.3 Overview.</span></span> <span data-ttu-id="b46dd-155">また、 [ネットワークモニターのブログ](https://blogs.technet.com/b/netmon/)も確認してください。</span><span class="sxs-lookup"><span data-stu-id="b46dd-155">Also, review the [Network Monitor blog](https://blogs.technet.com/b/netmon/).</span></span>

<span data-ttu-id="b46dd-156"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b46dd-156"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

