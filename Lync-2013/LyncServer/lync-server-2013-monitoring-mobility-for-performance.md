---
title: 'Lync Server 2013: パフォーマンスのためのモビリティの監視'
description: 'Lync Server 2013: パフォーマンスのためのモビリティの監視。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Monitoring mobility for performance
ms:assetid: 9c831c63-9a7d-48ec-9118-f8a7e80ddd04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690033(v=OCS.15)
ms:contentKeyID: 48184908
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d6c366542e88406df043ba1a782ee12cd64bd804
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425403"
---
# <a name="monitoring-mobility-for-performance-in-lync-server-2013"></a><span data-ttu-id="7cc6d-103">Lync Server 2013 でのモバイルパフォーマンスの監視</span><span class="sxs-lookup"><span data-stu-id="7cc6d-103">Monitoring mobility for performance in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7cc6d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7cc6d-104">

<span> </span></span></span>

<span data-ttu-id="7cc6d-105">_**最終更新日:** 2013-02-14_</span><span class="sxs-lookup"><span data-stu-id="7cc6d-105">_**Topic Last Modified:** 2013-02-14_</span></span>

<span data-ttu-id="7cc6d-106">Lync Server Mobility Service (Mcx) とユニファイドコミュニケーション Web API (UCWA) では、フロントエンドサーバーとフロントエンドプールの負荷が高くなります。</span><span class="sxs-lookup"><span data-stu-id="7cc6d-106">The Lync Server Mobility Service (Mcx) and the Unified Communications Web API (UCWA) increase the load on Front End Servers and Front End pools.</span></span> <span data-ttu-id="7cc6d-107">モバイルアプリケーションが最小化されている場合でもサーバーへの接続を維持するモバイルデバイス (lync 2010 Mobile を実行している Android や Nokia デバイス、Lync 2013 Mobile を実行している Android および Apple デバイスなど) は、モバイルアプリケーションが最小化されているときにサーバーへの接続を終了するデバイスよりも大きくロードされます。</span><span class="sxs-lookup"><span data-stu-id="7cc6d-107">Mobile devices that maintain a connection to the server even when the mobile application is minimized, such as Android and Nokia devices running Lync 2010 Mobile, as well as Android and Apple devices running Lync 2013 Mobile, impose a greater load than devices that terminate their connection to the server when the mobile application is minimized.</span></span> <span data-ttu-id="7cc6d-108">モバイル使用の増加に応じて、容量を増やす必要があるタイミングを判断するために、モビリティのパフォーマンスを監視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7cc6d-108">As your mobility usage increases, you must monitor mobility performance to determine when you need to increase your capacity.</span></span>

<span data-ttu-id="7cc6d-109">モビリティのパフォーマンスに影響を与えるいくつかの制限値があります。</span><span class="sxs-lookup"><span data-stu-id="7cc6d-109">Several limits influence mobility performance:</span></span>

  - <span data-ttu-id="7cc6d-110">使用可能なメモリ</span><span class="sxs-lookup"><span data-stu-id="7cc6d-110">Available memory</span></span>

  - <span data-ttu-id="7cc6d-111">要求キューの制限</span><span class="sxs-lookup"><span data-stu-id="7cc6d-111">Request queue limit</span></span>

  - <span data-ttu-id="7cc6d-112">同時接続数</span><span class="sxs-lookup"><span data-stu-id="7cc6d-112">Concurrent connections</span></span>

  - <span data-ttu-id="7cc6d-113">IIS キューの長さ</span><span class="sxs-lookup"><span data-stu-id="7cc6d-113">IIS queue length</span></span>

<span data-ttu-id="7cc6d-114">モビリティのパフォーマンスに影響を与える可能性のあるサーバーの制限は、最大12個の同時サインイン、認証、セッションの更新、終了です。</span><span class="sxs-lookup"><span data-stu-id="7cc6d-114">Other limits on servers that can influence mobility performance are a maximum of twelve concurrent sign-ins, authentications, session renewals, and terminations.</span></span> <span data-ttu-id="7cc6d-115">ただし、ほとんどの展開でこれらの最大値を変更する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="7cc6d-115">These maximums do not need to be modified for most deployments.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="7cc6d-116">このセクション中</span><span class="sxs-lookup"><span data-stu-id="7cc6d-116">In This Section</span></span>

  - [<span data-ttu-id="7cc6d-117">Lync Server 2013 でのサーバーメモリ容量の上限を監視する</span><span class="sxs-lookup"><span data-stu-id="7cc6d-117">Monitoring for server memory capacity limits in Lync Server 2013</span></span>](lync-server-2013-monitoring-for-server-memory-capacity-limits.md)

  - [<span data-ttu-id="7cc6d-118">Lync Server 2013 でのモビリティサービスと UCWA の使用状況の監視</span><span class="sxs-lookup"><span data-stu-id="7cc6d-118">Monitoring Mobility Service and UCWA usage in Lync Server 2013</span></span>](lync-server-2013-monitoring-mobility-service-and-ucwa-usage.md)

  - [<span data-ttu-id="7cc6d-119">Lync Server 2013 での高パフォーマンスのモビリティサービスの構成</span><span class="sxs-lookup"><span data-stu-id="7cc6d-119">Configuring Mobility Service for high performance in Lync Server 2013</span></span>](lync-server-2013-configuring-mobility-service-for-high-performance.md)

  - [<span data-ttu-id="7cc6d-120">Lync Server 2013 で IIS 要求トレースのログファイルを監視する</span><span class="sxs-lookup"><span data-stu-id="7cc6d-120">Monitoring IIS request tracing log files in Lync Server 2013</span></span>](lync-server-2013-monitoring-iis-request-tracing-log-files.md)

  - [<span data-ttu-id="7cc6d-121">Lync Server 2013 のモバイルパフォーマンスカウンター</span><span class="sxs-lookup"><span data-stu-id="7cc6d-121">Mobility performance counters in Lync Server 2013</span></span>](lync-server-2013-mobility-performance-counters.md)

<span data-ttu-id="7cc6d-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7cc6d-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

