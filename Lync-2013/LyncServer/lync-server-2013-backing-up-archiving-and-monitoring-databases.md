---
title: 'Lync Server 2013: アーカイブと監視データベースのバックアップを作成する'
description: 'Lync Server 2013: アーカイブと監視データベースのバックアップを作成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Backing up Archiving and Monitoring databases
ms:assetid: c120db81-b02c-4a4c-90cd-8aca6cff64f9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202188(v=OCS.15)
ms:contentKeyID: 51541515
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 49b4fa194bffa27a52f32d61a729eeaa31cc0ad3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438121"
---
# <a name="backing-up-archiving-and-monitoring-databases-in-lync-server-2013"></a><span data-ttu-id="1ae94-103">Lync Server 2013 でのアーカイブと監視データベースのバックアップ</span><span class="sxs-lookup"><span data-stu-id="1ae94-103">Backing up Archiving and Monitoring databases in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1ae94-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1ae94-104">

<span> </span></span></span>

<span data-ttu-id="1ae94-105">_**最終更新日:** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="1ae94-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<span data-ttu-id="1ae94-106">アーカイブまたは監視を展開した場合は、組織の SQL Server バックアップポリシーに従ってこれらのデータベースをバックアップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1ae94-106">If you deployed Archiving or Monitoring, you need to back up these databases according to your organization's SQL Server backup policy.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="1ae94-107">一元管理ストアをバックアップすると、アーカイブと監視の設定がバックアップされます。</span><span class="sxs-lookup"><span data-stu-id="1ae94-107">The settings for Archiving and Monitoring are backed up when you back up the Central Management store.</span></span> <span data-ttu-id="1ae94-108">詳細については、「 <A href="lync-server-2013-backing-up-core-data-and-settings.md">Lync Server 2013 でのコアデータと設定のバックアップ</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1ae94-108">For details, see <A href="lync-server-2013-backing-up-core-data-and-settings.md">Backing up core data and settings in Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="1ae94-109">アーカイブと監視の場合、sql server Management Studio などの SQL Server ツールを使用して手動バックアップを実行するか、SQL Server 管理ツールを使用して定期的な自動バックアップをスケジュールすることができます。</span><span class="sxs-lookup"><span data-stu-id="1ae94-109">For Archiving and Monitoring, you can use a SQL Server tool such as SQL Server Management Studio to perform a manual backup, or you can use SQL Server management tools to schedule regular, automatic backups.</span></span>

<span data-ttu-id="1ae94-110"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1ae94-110"></div>

<span> </span>

</div>

</div>

</span></span></div>

