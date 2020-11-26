---
title: 'Lync Server 2013: 監視データにアクセスする'
description: 'Lync Server 2013: 監視データにアクセスしています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Accessing monitoring data
ms:assetid: 845385ca-5532-4fa2-91b9-51c6de6fec91
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688116(v=OCS.15)
ms:contentKeyID: 49733714
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c183a66c98072f2ab30bb49e561f9f95c753142f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439500"
---
# <a name="accessing-monitoring-data-in-lync-server-2013"></a><span data-ttu-id="c2154-103">Lync Server 2013 での監視データへのアクセス</span><span class="sxs-lookup"><span data-stu-id="c2154-103">Accessing monitoring data in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c2154-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c2154-104">

<span> </span></span></span>

<span data-ttu-id="c2154-105">_**最終更新日:** 2012-09-05_</span><span class="sxs-lookup"><span data-stu-id="c2154-105">_**Topic Last Modified:** 2012-09-05_</span></span>

<span data-ttu-id="c2154-p101">監視データは、2 つの SQL Server データベースに格納されます。LcsCdr には通話詳細記録データが格納され、QoEMetrics には QoE (Quality of Experience) データが格納されます。これら 2 つのデータベースについて特別なことは何もありません。つまり、これらのデータベースに格納されているデータには、SQL Server データのアクセスと分析に使用する一般的なツールでアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="c2154-p101">Monitoring data is stored in a pair of SQL Server databases: LcsCdr for call detail recording data, and QoEMetrics for Quality of Experience data. There is nothing special about these two databases; that means that the data stored in those databases can be accessed using any of the tools you typically use for accessing and analyzing SQL Server data.</span></span>

<span data-ttu-id="c2154-108">監視データへのアクセスと分析について考慮すべきツールの1つは、Lync Server Monitoring レポートです。</span><span class="sxs-lookup"><span data-stu-id="c2154-108">One tool you should consider for accessing and analyzing monitoring data is the Lync Server Monitoring Reports.</span></span> <span data-ttu-id="c2154-109">レポートの監視は、Microsoft SQL Server Reporting Service によって公開された標準レポートのセットです。</span><span class="sxs-lookup"><span data-stu-id="c2154-109">Monitoring Reports are a set of standard reports that are published by Microsoft SQL Server Reporting Service.</span></span> <span data-ttu-id="c2154-110">これらのレポートは、web ブラウザーを使用してアクセスできます。これらのレポートは、CDR と QoE データベースに保存されている通話の詳細記録 (CDR) と Quality of Experience (QoE) レコードに基づいて提供されます。</span><span class="sxs-lookup"><span data-stu-id="c2154-110">These reports, which are accessible by using a web browser, provide usage, call diagnostic information, and media quality information, all based on call detail recording (CDR) and Quality of Experience (QoE) records stored in the CDR and QoE databases.</span></span> <span data-ttu-id="c2154-111">Lync server 2013 に付属している監視レポートと lync server をインストールして、監視が構成された後に Lync Server 展開ウィザードからインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="c2154-111">Monitoring Reports ship with Lync Server 2013 and can be installed from the Lync Server Deployment Wizard after Lync Server has been installed and monitoring has been configured.</span></span>

<span data-ttu-id="c2154-p103">説明したように、監視レポートには SQL Server Reporting Service を使用する必要があります。SQL Server Reporting Service は、SQL Server のインストールと同時に、または SQL Server 自体をインストールした後でいつでも、インストールできます。</span><span class="sxs-lookup"><span data-stu-id="c2154-p103">As noted, Monitoring Reports requires the use of SQL Server Reporting Service. SQL Server Reporting Service can be installed at the same time you install SQL Server or can be installed any time after SQL Server itself has been installed.</span></span>

<span data-ttu-id="c2154-114">詳細については、「Lync Server 2013 展開ガイド」で「 [Lync server 2013 監視レポートをインストールする](lync-server-2013-installing-lync-server-2013-monitoring-reports.md) 」のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c2154-114">For more information, see the topic [Installing Lync Server 2013 Monitoring Reports](lync-server-2013-installing-lync-server-2013-monitoring-reports.md) in the Lync Server 2013 deployment guide.</span></span>

<span data-ttu-id="c2154-115"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c2154-115"></div>

<span> </span>

</div>

</div>

</span></span></div>

