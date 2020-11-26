---
title: 'Lync Server 2013: Lync Server のバックアップ'
description: 'Lync Server 2013: Lync Server をバックアップしています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Backing up Lync Server
ms:assetid: 9ae8ac63-7893-4524-9ebe-c44f8ba9ce41
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202182(v=OCS.15)
ms:contentKeyID: 51541498
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 747501a2d3f2ab28f71ee06c4296494ea15a836b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438037"
---
# <a name="backing-up-lync-server-2013"></a><span data-ttu-id="2c6aa-103">Lync Server 2013 のバックアップ</span><span class="sxs-lookup"><span data-stu-id="2c6aa-103">Backing up Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2c6aa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2c6aa-104">

<span> </span></span></span>

<span data-ttu-id="2c6aa-105">_**最終更新日:** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="2c6aa-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<span data-ttu-id="2c6aa-106">このセクションの手順では、停止や障害が発生した場合にサービスを回復できるように、Lync Server をバックアップする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2c6aa-106">The procedures in this section describe how to back up Lync Server so that you can recover service in the event of an outage or failure.</span></span>

<span data-ttu-id="2c6aa-107">「 [バックアップと復元の戦略と Lync Server 2013 の計画を作成](lync-server-2013-developing-a-backup-and-restoration-strategy-and-plan.md)する」で説明されているように、組織のバックアップと回復の戦略と計画を策定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c6aa-107">You should develop a backup and recovery strategy and plan for your organization, as described in [Developing a backup and restoration strategy and plan for Lync Server 2013](lync-server-2013-developing-a-backup-and-restoration-strategy-and-plan.md).</span></span> <span data-ttu-id="2c6aa-108">この戦略と計画には、使用する予定の特定の手順を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c6aa-108">This strategy and plan should include the specific procedures that you plan to use.</span></span> <span data-ttu-id="2c6aa-109">このセクションのトピックに記載されている手順と、 [Lync server 2013 のバックアップおよび復元ワークシート](lync-server-2013-backup-and-restoration-worksheets.md)のワークシートを使用して、特定の lync server 展開をバックアップする計画を文書化します。</span><span class="sxs-lookup"><span data-stu-id="2c6aa-109">Use the procedures included in the topics in this section, along with the worksheets in [Backup and restoration worksheets for Lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md), to document how you plan to back up your specific Lync Server deployment.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="2c6aa-110">このセクション中</span><span class="sxs-lookup"><span data-stu-id="2c6aa-110">In This Section</span></span>

  - [<span data-ttu-id="2c6aa-111">Lync Server 2013 でバックアップの前提条件を確認する</span><span class="sxs-lookup"><span data-stu-id="2c6aa-111">Verifying backup prerequisites in Lync Server 2013</span></span>](lync-server-2013-verifying-backup-prerequisites.md)

  - [<span data-ttu-id="2c6aa-112">Lync Server 2013 でのデータと設定のバックアップ</span><span class="sxs-lookup"><span data-stu-id="2c6aa-112">Backing up data and settings in Lync Server 2013</span></span>](lync-server-2013-backing-up-data-and-settings.md)

<span data-ttu-id="2c6aa-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2c6aa-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

