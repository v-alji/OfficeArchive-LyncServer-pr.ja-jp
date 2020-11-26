---
title: 'Lync Server 2013: Active Directory ドメイン サービスの準備'
description: 'Lync Server 2013: Active Directory ドメインサービスの準備をしています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing Active Directory Domain Services for Lync Server 2013
ms:assetid: 7e126464-5d29-4013-9c44-0ccc2fbdea0f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398630(v=OCS.15)
ms:contentKeyID: 48184620
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d6ecfcffd55739bc6d1bf1b83a701a0fd515ec56
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424220"
---
# <a name="preparing-active-directory-domain-services-for-lync-server-2013"></a><span data-ttu-id="9212c-103">Lync Server 2013 用の Active Directory ドメイン サービスの準備</span><span class="sxs-lookup"><span data-stu-id="9212c-103">Preparing Active Directory Domain Services for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9212c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9212c-104">

<span> </span></span></span>

<span data-ttu-id="9212c-105">_**最終更新日:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="9212c-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="9212c-106">Lync Server 2013 を展開して運用する前に、スキーマを拡張し、オブジェクトを作成して構成することによって、Active Directory ドメインサービスを準備する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9212c-106">Before you deploy and operate Lync Server 2013, you must prepare Active Directory Domain Services by extending the schema and then creating and configuring objects.</span></span> <span data-ttu-id="9212c-107">スキーマの拡張機能によって、Lync Server で必要な Active Directory のクラスと属性が追加されます。</span><span class="sxs-lookup"><span data-stu-id="9212c-107">The schema extensions add the Active Directory classes and attributes that are required by Lync Server.</span></span>

<span data-ttu-id="9212c-108">このセクションのトピックでは、Lync Server を展開するために AD DS を準備する方法と、セットアップおよび組織単位 (OU) の権限を割り当てる方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9212c-108">The topics in this section describe how to prepare AD DS for deploying Lync Server and how to assign setup and organizational unit (OU) permissions.</span></span> <span data-ttu-id="9212c-109">Lync Server に必要なスキーマ変更の詳細については、「 [Active Directory スキーマの拡張機能、クラス、および Lync server 2013 で使用される属性](lync-server-2013-active-directory-schema-extensions-classes-and-attributes-used-by-lync-server.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9212c-109">For details about the schema changes required for Lync Server, see [Active Directory schema extensions, classes, and attributes used by Lync Server 2013](lync-server-2013-active-directory-schema-extensions-classes-and-attributes-used-by-lync-server.md).</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="9212c-110">このセクション中</span><span class="sxs-lookup"><span data-stu-id="9212c-110">In This Section</span></span>

  - [<span data-ttu-id="9212c-111">Lync Server 2013 に関する Active Directory インフラストラクチャの要件</span><span class="sxs-lookup"><span data-stu-id="9212c-111">Active Directory infrastructure requirements for Lync Server 2013</span></span>](lync-server-2013-active-directory-infrastructure-requirements.md)

  - [<span data-ttu-id="9212c-112">Lync Server 2013 の Active Directory ドメイン サービスの準備の概要</span><span class="sxs-lookup"><span data-stu-id="9212c-112">Overview of Active Directory Domain Services preparation in Lync Server 2013</span></span>](lync-server-2013-overview-of-active-directory-domain-services-preparation.md)

  - [<span data-ttu-id="9212c-113">Lync Server 2013 での Active Directory ドメイン サービスの準備</span><span class="sxs-lookup"><span data-stu-id="9212c-113">Preparing Active Directory Domain Services in Lync Server 2013</span></span>](lync-server-2013-preparing-active-directory-domain-services.md)

  - [<span data-ttu-id="9212c-114">Lync Server 2013 でのロックダウンされた Active Directory ドメイン サービスの準備</span><span class="sxs-lookup"><span data-stu-id="9212c-114">Preparing a locked-down Active Directory Domain Services in Lync Server 2013</span></span>](lync-server-2013-preparing-a-locked-down-active-directory-domain-services.md)

  - [<span data-ttu-id="9212c-115">Lync Server 2013 でのアクセス許可の付与</span><span class="sxs-lookup"><span data-stu-id="9212c-115">Granting permissions in Lync Server 2013</span></span>](lync-server-2013-granting-permissions.md)

<span data-ttu-id="9212c-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9212c-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

