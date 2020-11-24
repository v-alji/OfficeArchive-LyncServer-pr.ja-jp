---
title: 'Lync Server 2013: IPv6 の移行および共存の検討事項'
description: 'Lync Server 2013: IPv6 の移行と共存の考慮事項。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migration and coexistence considerations for IPv6
ms:assetid: 8c769c4f-c8a9-4cbf-9080-beee3be9848a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205068(v=OCS.15)
ms:contentKeyID: 48184751
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e8618cc14ff3c2467ea41df34e39f5094d1206dc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399687"
---
# <a name="migration-and-coexistence-considerations-for-ipv6-in-lync-server-2013"></a><span data-ttu-id="17f51-103">Lync Server 2013 における IPv6 の移行および共存の検討事項</span><span class="sxs-lookup"><span data-stu-id="17f51-103">Migration and coexistence considerations for IPv6 in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="17f51-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="17f51-104">

<span> </span></span></span>

<span data-ttu-id="17f51-105">_**最終更新日:** 2012-06-14_</span><span class="sxs-lookup"><span data-stu-id="17f51-105">_**Topic Last Modified:** 2012-06-14_</span></span>

<span data-ttu-id="17f51-106">IP version 6 (IPv6) は、Lync Server 2010 または Office Communications Server ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="17f51-106">IP version 6 (IPv6) is not supported on Lync Server 2010 or Office Communications Server.</span></span> <span data-ttu-id="17f51-107">パイロットのために、Lync Server 2010 および Lync Server 2013 の2つのスタックを共存させることができます。</span><span class="sxs-lookup"><span data-stu-id="17f51-107">For piloting purposes, you can test Lync Server 2010 and Lync Server 2013 dual-stack coexistence.</span></span> <span data-ttu-id="17f51-108">いずれかのプールで IPv6 (デュアルスタックネットワーク) を有効にする前に、特定のセントラルサイトのすべてのプールを Lync Server 2013 にアップグレードすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="17f51-108">We recommend that all pools for a given central site are upgraded to Lync Server 2013 before you enable IPv6 (dual-stack network) for any of the pools.</span></span> <span data-ttu-id="17f51-109">IPv6 に対応したプールのみを構成する必要がある場合は、テスト用のラボ環境に IPv6 専用のプールを設定することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="17f51-109">If you need to configure a pool for IPv6 only, we recommend that you set up an IPv6-only pool in your lab environment for testing.</span></span>

<span data-ttu-id="17f51-110">次のシナリオは、移行と共存でサポートされます。</span><span class="sxs-lookup"><span data-stu-id="17f51-110">The following scenarios are supported during migration and coexistence:</span></span>

  - <span data-ttu-id="17f51-111">Lync server 2013、Lync Server 2010、Office Communications Server 2007 R2 プール (IPv4 モード) では、Lync Server 2013 とデュアルスタックモードを共存させることができます。</span><span class="sxs-lookup"><span data-stu-id="17f51-111">Lync Server 2013, Lync Server 2010, and Office Communications Server 2007 R2 pools in IPv4 mode, coexisting with Lync Server 2013 in dual-stack mode.</span></span>

  - <span data-ttu-id="17f51-112">Ipv6 専用プールが孤立している場合は、IPv6 専用モードの Lync Server 2013 プール。</span><span class="sxs-lookup"><span data-stu-id="17f51-112">Lync Server 2013 pool in IPv6-only mode, if the IPv6-only pool is siloed.</span></span>

<span data-ttu-id="17f51-113"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="17f51-113"></div>

<span> </span>

</div>

</div>

</span></span></div>

