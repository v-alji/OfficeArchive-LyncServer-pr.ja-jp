---
title: 'Lync Server 2013: 高パフォーマンスのモビリティサービスを構成する'
description: 'Lync Server 2013: 高パフォーマンスのモビリティサービスを構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Mobility Service for high performance
ms:assetid: c2b8aadb-cffb-49f0-ba7a-e8541a1ff475
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690042(v=OCS.15)
ms:contentKeyID: 48185332
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4732d9f6a92c383a105a6f0d7162c9b6c798de24
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432885"
---
# <a name="configuring-mobility-service-for-high-performance-in-lync-server-2013"></a><span data-ttu-id="ae5db-103">Lync Server 2013 での高パフォーマンスのモビリティサービスの構成</span><span class="sxs-lookup"><span data-stu-id="ae5db-103">Configuring Mobility Service for high performance in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ae5db-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ae5db-104">

<span> </span></span></span>

<span data-ttu-id="ae5db-105">_**最終更新日:** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="ae5db-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="ae5db-106">このトピックは、lync server 2013 モビリティサービス (Mcx) にのみ適用され、Lync Server 2013 2013 の累積更新プログラムで提供されるように、統合コミュニケーション Web API (UCWA) には適用されません。</span><span class="sxs-lookup"><span data-stu-id="ae5db-106">This topic applies only to the Lync Server 2013 Mobility Service (Mcx), and does not apply to Unified Communications Web API (UCWA), as delivered in the Cumulative Updates for Lync Server 2013: February 2013.</span></span>



</div>

<span data-ttu-id="ae5db-107">インターネットインフォメーションサービス (IIS) 7.5 にモバイルサービス (Mcx) をインストールすると、Mobility Service installer によって、フロントエンドサーバーの一部のパフォーマンス設定が構成されます。</span><span class="sxs-lookup"><span data-stu-id="ae5db-107">When you install the Mobility Service (Mcx) on Internet Information Services (IIS) 7.5, the Mobility Service installer configures some performance settings on the Front End Server.</span></span> <span data-ttu-id="ae5db-108">モビリティでは IIS 7.5 を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ae5db-108">We recommend that you use IIS 7.5 for mobility.</span></span> <span data-ttu-id="ae5db-109">これらの設定は、同時ユーザー要求の最大数と、Mobility Service で利用できるスレッドの最大数に影響します。</span><span class="sxs-lookup"><span data-stu-id="ae5db-109">The settings affect the maximum number of concurrent user requests and the maximum number of threads that are allowed for the Mobility Service.</span></span>

<span data-ttu-id="ae5db-110">以下にパフォーマンス設定を示します。</span><span class="sxs-lookup"><span data-stu-id="ae5db-110">Here are the performance settings:</span></span>

<div>

## <a name="settings-for-mcx-on-iis-75"></a><span data-ttu-id="ae5db-111">IIS 7.5 での Mcx の設定</span><span class="sxs-lookup"><span data-stu-id="ae5db-111">Settings for Mcx on IIS 7.5</span></span>

1.  <span data-ttu-id="ae5db-112">**maxConcurrentThreadsPerCPU** は、ゼロ (0) に設定されます。</span><span class="sxs-lookup"><span data-stu-id="ae5db-112">**maxConcurrentThreadsPerCPU** is set to zero (0).</span></span>

2.  <span data-ttu-id="ae5db-113">**maxConcurrentRequestsPerCPU** は、ゼロ (0) に設定されます。</span><span class="sxs-lookup"><span data-stu-id="ae5db-113">**maxConcurrentRequestsPerCPU** is set to zero (0).</span></span>

3.  <span data-ttu-id="ae5db-114">ASP.NET プロセス モデルは、AutoConfig に設定されます (IIS 7.5 のみ)。</span><span class="sxs-lookup"><span data-stu-id="ae5db-114">ASP.NET process model is set to AutoConfig (for IIS 7.5 only).</span></span>

4.  <span data-ttu-id="ae5db-115">HTTP.sys のキューの制限は 1,000 に設定されます (既定)。</span><span class="sxs-lookup"><span data-stu-id="ae5db-115">HTTP.sys queue limit is set to 1,000 (by default).</span></span>

<span data-ttu-id="ae5db-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ae5db-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

