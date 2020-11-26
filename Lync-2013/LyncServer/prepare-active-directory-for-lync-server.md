---
title: Lync Server の Active Directory の準備
description: Lync Server 用に Active Directory を準備します。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Prepare Active Directory for Lync Server
ms:assetid: 54cd597d-0c2d-479c-8c52-1babc53f71dc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688059(v=OCS.15)
ms:contentKeyID: 49733653
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ff9ff2de825d68f2c7ca9d90cbecdf71e5d00d55
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423374"
---
# <a name="prepare-active-directory-for-lync-server"></a><span data-ttu-id="3131c-103">Lync Server の Active Directory の準備</span><span class="sxs-lookup"><span data-stu-id="3131c-103">Prepare Active Directory for Lync Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3131c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3131c-104">

<span> </span></span></span>

<span data-ttu-id="3131c-105">_**最終更新日:** 2012-09-17_</span><span class="sxs-lookup"><span data-stu-id="3131c-105">_**Topic Last Modified:** 2012-09-17_</span></span>

<span data-ttu-id="3131c-106">Lync server 2013 を共存2010状態で展開する前に、lync Server 2013 のスキーマ、フォレスト、ドメインを構成するために、追加の Active Directory タスクを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3131c-106">Prior to deploying Lync Server 2013 in a coexistence state with Lync Server 2010, you must perform some additional Active Directory tasks to configure the schema, forest, and domain for Lync Server 2013.</span></span> <span data-ttu-id="3131c-107">スキーマの拡張機能によって、Lync Server 2013 で必要な Active Directory のクラスと属性が追加されます。</span><span class="sxs-lookup"><span data-stu-id="3131c-107">The schema extensions add the Active Directory classes and attributes that are required by Lync Server 2013.</span></span> <span data-ttu-id="3131c-108">詳細については、「 [Lync Server 2013 用の Active Directory ドメインサービスの準備](lync-server-2013-preparing-active-directory-domain-services.md)」のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3131c-108">For additional information, see the topic [Preparing Active Directory Domain Services for Lync Server 2013](lync-server-2013-preparing-active-directory-domain-services.md).</span></span>

<span data-ttu-id="3131c-109">**Lync Server 2013 用に Active Directory を準備するには**</span><span class="sxs-lookup"><span data-stu-id="3131c-109">**To prepare Active Directory for Lync Server 2013**</span></span>

1.  <span data-ttu-id="3131c-110">Lync Server 2013 フロントエンドサーバーで、Lync Server 2013 のセットアップを実行します。</span><span class="sxs-lookup"><span data-stu-id="3131c-110">On the Lync Server 2013 Front End Server, run Lync Server 2013 Setup.</span></span>

2.  <span data-ttu-id="3131c-111">[ **Active Directory の準備**] を選びます。</span><span class="sxs-lookup"><span data-stu-id="3131c-111">Select **Prepare Active Directory**.</span></span>
    
    <span data-ttu-id="3131c-112">![Lync Server 2013 展開ウィザードの [ようこそ] ページ](images/JJ205265.5f88ae18-9c3c-42ea-a91a-836ecf5d515f(OCS.15).jpg "Lync Server 2013 展開ウィザードの [ようこそ] ページ")</span><span class="sxs-lookup"><span data-stu-id="3131c-112">![Lync Server 2013 Deployment Wizard, Welcome page](images/JJ205265.5f88ae18-9c3c-42ea-a91a-836ecf5d515f(OCS.15).jpg "Lync Server 2013 Deployment Wizard, Welcome page")</span></span>

3.  <span data-ttu-id="3131c-113">手順1から5を実行します。</span><span class="sxs-lookup"><span data-stu-id="3131c-113">Complete steps 1 through 5.</span></span>
    
    <span data-ttu-id="3131c-114">![展開ウィザードの [Active Directory]](images/JJ205265.eddd9e94-fa70-453f-8810-b99a2bf0844a(OCS.15).jpg "展開ウィザードの [Active Directory]")</span><span class="sxs-lookup"><span data-stu-id="3131c-114">![Deployment Wizard, Active Directory Prearation](images/JJ205265.eddd9e94-fa70-453f-8810-b99a2bf0844a(OCS.15).jpg "Deployment Wizard, Active Directory Prearation")</span></span>

<span data-ttu-id="3131c-115"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3131c-115"></div>

<span> </span>

</div>

</div>

</span></span></div>

