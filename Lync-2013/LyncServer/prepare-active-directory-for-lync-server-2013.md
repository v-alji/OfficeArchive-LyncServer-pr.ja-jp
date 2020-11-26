---
title: Lync Server 2013 用に Active Directory を準備する
description: Lync Server 2013 用に Active Directory を準備します。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Prepare Active Directory for Lync Server 2013
ms:assetid: d0978eb6-d842-40e9-b475-73197cc34e08
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205265(v=OCS.15)
ms:contentKeyID: 48185413
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 75ca6476d82f755528f7d1c4341523d50722f796
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446844"
---
# <a name="prepare-active-directory-for-lync-server-2013"></a><span data-ttu-id="d8887-103">Lync Server 2013 用に Active Directory を準備する</span><span class="sxs-lookup"><span data-stu-id="d8887-103">Prepare Active Directory for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d8887-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d8887-104">

<span> </span></span></span>

<span data-ttu-id="d8887-105">_**最終更新日:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="d8887-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="d8887-106">Office Communications Server 2007 R2 を使用して、共存状態で Lync Server 2013 を展開する前に、Lync Server 2013 のスキーマ、フォレスト、ドメインを構成するために、追加の Active Directory タスクを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8887-106">Prior to deploying Lync Server 2013 in a coexistence state with Office Communications Server 2007 R2, you must perform some additional Active Directory tasks to configure the schema, forest, and domain for Lync Server 2013.</span></span> <span data-ttu-id="d8887-107">スキーマの拡張機能によって、Lync Server で必要な Active Directory のクラスと属性が追加されます。</span><span class="sxs-lookup"><span data-stu-id="d8887-107">The schema extensions add the Active Directory classes and attributes that are required by Lync Server.</span></span> <span data-ttu-id="d8887-108">詳細については、「 [Lync Server 2013 用の Active Directory ドメインサービスの準備](lync-server-2013-preparing-active-directory-domain-services.md)」のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d8887-108">For additional information, see the topic [Preparing Active Directory Domain Services for Lync Server 2013](lync-server-2013-preparing-active-directory-domain-services.md).</span></span>

<span data-ttu-id="d8887-109">**Lync Server 2013 用に Active Directory を準備する**</span><span class="sxs-lookup"><span data-stu-id="d8887-109">**Prepare Active Directory for Lync Server 2013**</span></span>

1.  <span data-ttu-id="d8887-110">Lync Server 2013 フロントエンドサーバーで、Lync Server 2013 のセットアップを実行します。</span><span class="sxs-lookup"><span data-stu-id="d8887-110">On the Lync Server 2013 Front End Server, run Lync Server 2013 Setup.</span></span>

2.  <span data-ttu-id="d8887-111">[ **Active Directory の準備**] を選ぶ</span><span class="sxs-lookup"><span data-stu-id="d8887-111">Select **Prepare Active Directory**</span></span>
    
    <span data-ttu-id="d8887-112">![Lync Server 2013 展開ウィザードの [ようこそ] ページ](images/JJ205265.5f88ae18-9c3c-42ea-a91a-836ecf5d515f(OCS.15).jpg "Lync Server 2013 展開ウィザードの [ようこそ] ページ")</span><span class="sxs-lookup"><span data-stu-id="d8887-112">![Lync Server 2013 Deployment Wizard, Welcome page](images/JJ205265.5f88ae18-9c3c-42ea-a91a-836ecf5d515f(OCS.15).jpg "Lync Server 2013 Deployment Wizard, Welcome page")</span></span>

3.  <span data-ttu-id="d8887-113">手順1から5を実行します。</span><span class="sxs-lookup"><span data-stu-id="d8887-113">Complete steps 1 through 5.</span></span>
    
    <span data-ttu-id="d8887-114">![展開ウィザードの [Active Directory]](images/JJ205265.eddd9e94-fa70-453f-8810-b99a2bf0844a(OCS.15).jpg "展開ウィザードの [Active Directory]")</span><span class="sxs-lookup"><span data-stu-id="d8887-114">![Deployment Wizard, Active Directory Prearation](images/JJ205265.eddd9e94-fa70-453f-8810-b99a2bf0844a(OCS.15).jpg "Deployment Wizard, Active Directory Prearation")</span></span>

<span data-ttu-id="d8887-115"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d8887-115"></div>

<span> </span>

</div>

</div>

</span></span></div>

