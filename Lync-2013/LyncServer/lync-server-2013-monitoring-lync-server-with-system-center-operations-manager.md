---
title: 'Lync Server 2013: System Center Operations Manager を使用して Lync Server を監視する'
description: 'Lync Server 2013: System Center Operations Manager を使用して Lync Server を監視します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Monitoring Lync 2013 with SCOM
ms:assetid: a74bde92-97ff-4d90-acb9-7a70272f0f31
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720343(v=OCS.15)
ms:contentKeyID: 63969636
ms.date: 05/06/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2ad93c47ab8d157b1e18b4bccc5094408f3d68ee
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425410"
---
# <a name="monitoring-lync-server-2013-with-system-center-operations-manager"></a><span data-ttu-id="ee38b-103">System Center Operations Manager での Lync Server 2013 の監視</span><span class="sxs-lookup"><span data-stu-id="ee38b-103">Monitoring Lync Server 2013 with System Center Operations Manager</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ee38b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ee38b-104">

<span> </span></span></span>

<span data-ttu-id="ee38b-105">_**最終更新日:** 2015-05-06_</span><span class="sxs-lookup"><span data-stu-id="ee38b-105">_**Topic Last Modified:** 2015-05-06_</span></span>

<span data-ttu-id="ee38b-106">Lync Server 管理パック (MP) は、Lync Server の展開を監視するために選択できる監視ソリューションです。</span><span class="sxs-lookup"><span data-stu-id="ee38b-106">The Lync Server Management Pack (MP) is your monitoring solution of choice for monitoring any Lync Server deployment.</span></span>

<span data-ttu-id="ee38b-107">MP は、従来のイベントログとパフォーマンスカウンターベースのインストルメンテーションを実装し、いくつかの主要な正常性インジケーターのペアイベント (失敗/成功) など、Lync Server で新しく利用可能なインストルメンテーションを有効にします。また、新しい代理トランザクション (テスト-Cs \* Windows PowerShell コマンドレット) も完全に実装します。</span><span class="sxs-lookup"><span data-stu-id="ee38b-107">The MP implements traditional Event Log and Performance counter-based instrumentation and enables newly available instrumentation in Lync Server, such as pair events (failure/success) for several Key Health Indicators, and also fully implements the new Synthetic Transactions (Test-Cs\* Windows PowerShell cmdlets).</span></span>

<span data-ttu-id="ee38b-108">Lync Server 2013 管理パックと関連ドキュメントは、で確認でき [https://go.microsoft.com/fwlink/p/?LinkId=400468](https://go.microsoft.com/fwlink/p/?linkid=400468) ます。</span><span class="sxs-lookup"><span data-stu-id="ee38b-108">You can find the Lync Server 2013 Management Pack and its related documentation at [https://go.microsoft.com/fwlink/p/?LinkId=400468](https://go.microsoft.com/fwlink/p/?linkid=400468).</span></span> <span data-ttu-id="ee38b-109">System Center Operations Manager 2012 を実行している場合は、この方法をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ee38b-109">This is recommended if you are running System Center Operations Manager 2012.</span></span>

<span data-ttu-id="ee38b-110"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ee38b-110"></div>

<span> </span>

</div>

</div>

</span></span></div>

