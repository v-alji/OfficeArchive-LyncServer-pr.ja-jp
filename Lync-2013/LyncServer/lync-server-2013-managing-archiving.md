---
title: 'Lync Server 2013: アーカイブの管理'
description: 'Lync Server 2013: アーカイブを管理します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing Lync Server 2013 Archiving
ms:assetid: 48c6cc8c-c2c1-4534-9a8a-fd5eb738076a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520990(v=OCS.15)
ms:contentKeyID: 48184003
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9c7010645f36a7144ea508447d2c628bc8feacb0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425977"
---
# <a name="managing-lync-server-2013-archiving"></a><span data-ttu-id="3b088-103">Lync Server 2013 アーカイブの管理</span><span class="sxs-lookup"><span data-stu-id="3b088-103">Managing Lync Server 2013 Archiving</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3b088-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3b088-104">

<span> </span></span></span>

<span data-ttu-id="3b088-105">_**最終更新日:** 2012-10-10_</span><span class="sxs-lookup"><span data-stu-id="3b088-105">_**Topic Last Modified:** 2012-10-10_</span></span>

<span data-ttu-id="3b088-106">組織のアーカイブを展開するときは、展開時に初期構成を指定します。</span><span class="sxs-lookup"><span data-stu-id="3b088-106">When you deploy Archiving for your organization, you specify the initial configuration during deployment.</span></span> <span data-ttu-id="3b088-107">ただし、日常的な管理のためのアーカイブサポートの実装方法を変更したり、組織の新しい要件を満たすことが必要になる場合もあります。</span><span class="sxs-lookup"><span data-stu-id="3b088-107">However, there may be times when you want to change how you implement archiving support for day-to-day management or to meet new requirements in your organization.</span></span> <span data-ttu-id="3b088-108">たとえば、組織内の特定のサイト、プール、またはユーザーについて、アーカイブのサポートを設定する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="3b088-108">For example, you may need to set up archiving support differently for a specific site, pool, or users within your organization.</span></span> <span data-ttu-id="3b088-109">Lync Server 2013 を使用しているユーザーは、アーカイブポリシーと構成の作成とカスタマイズを行います。</span><span class="sxs-lookup"><span data-stu-id="3b088-109">For users homed on Lync Server 2013, you do this be creating and customizing archiving policies and configurations.</span></span> <span data-ttu-id="3b088-110">Microsoft Exchange 統合を使用している場合は、Exchange 2013 の設定も構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3b088-110">If you use Microsoft Exchange integration, you must also configure Exchange 2013 settings.</span></span> <span data-ttu-id="3b088-111">このセクションでは、アーカイブの展開を変更できるようにするための情報と手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="3b088-111">This section provides information and procedures to enable you to make changes to your Archiving deployment.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="3b088-112">このセクション中</span><span class="sxs-lookup"><span data-stu-id="3b088-112">In This Section</span></span>

  - [<span data-ttu-id="3b088-113">Lync Server 2013 でのアーカイブのしくみ</span><span class="sxs-lookup"><span data-stu-id="3b088-113">How Archiving works in Lync Server 2013</span></span>](lync-server-2013-how-archiving-works.md)

  - [<span data-ttu-id="3b088-114">Lync Server 2013 での内部および外部通信のアーカイブの管理</span><span class="sxs-lookup"><span data-stu-id="3b088-114">Managing the Archiving of internal and external communications in Lync Server 2013</span></span>](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md)

  - [<span data-ttu-id="3b088-115">組織、サイト、およびプールの Lync Server 2013 でアーカイブ構成オプションを管理する</span><span class="sxs-lookup"><span data-stu-id="3b088-115">Managing Archiving configuration options in Lync Server 2013 for your organization, sites, and pools</span></span>](lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md)

  - [<span data-ttu-id="3b088-116">Lync Server 2013 でアーカイブデータベースのオプションを変更する</span><span class="sxs-lookup"><span data-stu-id="3b088-116">Changing Archiving database options in Lync Server 2013</span></span>](lync-server-2013-changing-archiving-database-options.md)

  - [<span data-ttu-id="3b088-117">Lync Server 2013 からアーカイブデータをエクスポートする</span><span class="sxs-lookup"><span data-stu-id="3b088-117">Exporting archived data from Lync Server 2013</span></span>](lync-server-2013-exporting-archived-data.md)

<span data-ttu-id="3b088-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3b088-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

