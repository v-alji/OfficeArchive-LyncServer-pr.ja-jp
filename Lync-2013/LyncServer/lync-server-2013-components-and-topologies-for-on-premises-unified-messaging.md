---
title: 'Lync Server 2013: 社内ユニファイド メッセージングのコンポーネントとトポロジ'
description: 'Lync Server 2013: オンプレミスのユニファイドメッセージングのコンポーネントとトポロジ。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components and topologies for on-premises Unified Messaging
ms:assetid: 22fc87cf-a7e5-4c8c-bb9b-101e5380cdcf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425711(v=OCS.15)
ms:contentKeyID: 48183619
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8fe2ca16ec9fbd39e9245fd366e1f7046dd16d42
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398546"
---
# <a name="components-and-topologies-for-on-premises-unified-messaging-in-lync-server-2013"></a><span data-ttu-id="d3019-103">Lync Server 2013 の社内ユニファイド メッセージングのコンポーネントとトポロジ</span><span class="sxs-lookup"><span data-stu-id="d3019-103">Components and topologies for on-premises Unified Messaging in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d3019-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d3019-104">

<span> </span></span></span>

<span data-ttu-id="d3019-105">_**最終更新日:** 2012-09-25_</span><span class="sxs-lookup"><span data-stu-id="d3019-105">_**Topic Last Modified:** 2012-09-25_</span></span>

<span data-ttu-id="d3019-106">このトピックでは、Lync Server 2013 の展開に Exchange ユニファイドメッセージング (UM) 機能を提供するために必要な Microsoft Exchange Server 2013 コンポーネントについて説明します。</span><span class="sxs-lookup"><span data-stu-id="d3019-106">This topic describes the Microsoft Exchange Server 2013 components required to provide Exchange Unified Messaging (UM) features to Lync Server 2013 deployment.</span></span> <span data-ttu-id="d3019-107">また、オンプレミスの Exchange UM との統合でサポートされているトポロジについても説明します。</span><span class="sxs-lookup"><span data-stu-id="d3019-107">It also describes the supported topologies for on-premises Exchange UM integration.</span></span>

<div>

## <a name="exchange-server-components"></a><span data-ttu-id="d3019-108">Exchange Server コンポーネント</span><span class="sxs-lookup"><span data-stu-id="d3019-108">Exchange Server Components</span></span>

<span data-ttu-id="d3019-109">統合された [ユニファイドメッセージングおよび Lync Server 2013 の機能](lync-server-2013-features-of-integrated-unified-messaging.md) について説明した exchange UM の機能とサービスを組織内のエンタープライズボイスユーザーに提供するには、Microsoft Exchange メールボックスサーバーとクライアントアクセスサーバーを展開して、ユーザーのメールボックスをホストし、メールやボイスメール用の1つの保存場所を提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3019-109">To provide the Exchange UM features and services described in [Features of integrated Unified Messaging and Lync Server 2013](lync-server-2013-features-of-integrated-unified-messaging.md) to Enterprise Voice users in your organization, you must deploy an Microsoft Exchange Mailbox server and Client Access server, which hosts user mailboxes and provides a single storage location for email and voice mail.</span></span> <span data-ttu-id="d3019-110">Exchange UM は、Exchange メールボックスとクライアントアクセスサーバーでサービスとして実行されます。</span><span class="sxs-lookup"><span data-stu-id="d3019-110">Exchange UM runs as a service on Exchange Mailbox and Client Access servers.</span></span>

<span data-ttu-id="d3019-111">Microsoft Exchange Server 2007 および Microsoft Exchange Server 2010 の Exchange UM コンポーネントの詳細については、「展開ドキュメントで [Lync Server 2013 ボイスメールを提供するためのオンプレミスの EXCHANGE UM の展開」を](lync-server-2013-deploying-on-premises-exchange-um-to-provide-lync-server-2013-voice-mail.md) 参照してください。</span><span class="sxs-lookup"><span data-stu-id="d3019-111">For details about Exchange UM components in Microsoft Exchange Server 2007 and Microsoft Exchange Server 2010, see [Deploying on-premises Exchange UM to provide Lync Server 2013 voice mail](lync-server-2013-deploying-on-premises-exchange-um-to-provide-lync-server-2013-voice-mail.md) in the Deployment documentation.</span></span>

</div>

<div>

## <a name="supported-topologies"></a><span data-ttu-id="d3019-112">サポートされるトポロジ</span><span class="sxs-lookup"><span data-stu-id="d3019-112">Supported Topologies</span></span>

<span data-ttu-id="d3019-113">Lync Server 2013 と Exchange ユニファイドメッセージング (UM) は、同じフォレストまたは複数のフォレストに展開できます。</span><span class="sxs-lookup"><span data-stu-id="d3019-113">You can deploy Lync Server 2013 and Exchange Unified Messaging (UM) in the same forest or multiple forests.</span></span> <span data-ttu-id="d3019-114">展開が複数のフォレストにまたがる場合は、各 Exchange UM フォレストの Exchange 統合手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3019-114">If the deployment spans multiple forests, you must perform the Exchange integration steps for each Exchange UM forest.</span></span> <span data-ttu-id="d3019-115">さらに、Lync Server 2013 フォレストと Lync Server 2013 フォレストを信頼するように Microsoft Exchange フォレストを構成し、各 Exchange UM フォレストを信頼するようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3019-115">Furthermore, you must configure each Microsoft Exchange forest to trust the Lync Server 2013 forest and the Lync Server 2013 forest to trust each Exchange UM forest.</span></span> <span data-ttu-id="d3019-116">このフォレストの信頼に加えて、Lync Server 2013 フォレストのユーザーオブジェクトに対して、すべてのユーザーの Exchange UM 設定を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3019-116">In addition to this forest trust, the Exchange UM settings for all users must be set on the user objects in the Lync Server 2013 forest.</span></span>

<span data-ttu-id="d3019-117">Lync Server 2013 は、Exchange UM との統合のために次のトポロジをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="d3019-117">Lync Server 2013 supports the following topologies for Exchange UM integration:</span></span>

  - <span data-ttu-id="d3019-118">1つのフォレスト</span><span class="sxs-lookup"><span data-stu-id="d3019-118">Single forest</span></span>

  - <span data-ttu-id="d3019-119">単一ドメイン (つまり、単一のドメインを持つ単一フォレスト)。</span><span class="sxs-lookup"><span data-stu-id="d3019-119">Single domain (that is, a single forest with a single domain).</span></span> <span data-ttu-id="d3019-120">Lync Server 2013、Microsoft Exchange、およびユーザーはすべて同じドメインに存在します。</span><span class="sxs-lookup"><span data-stu-id="d3019-120">Lync Server 2013, Microsoft Exchange, and users all reside in the same domain.</span></span>

  - <span data-ttu-id="d3019-121">複数のドメイン (つまり、1つ以上の子ドメインを持つルートドメイン)。</span><span class="sxs-lookup"><span data-stu-id="d3019-121">Multiple domain (that is, a root domain with one or more child domains).</span></span> <span data-ttu-id="d3019-122">Lync Server 2013、および Microsoft Exchange サーバーは、ユーザーを作成するドメインとは異なるドメインに展開されます。</span><span class="sxs-lookup"><span data-stu-id="d3019-122">Lync Server 2013, and Microsoft Exchange servers are deployed in different domains from the domain where you create users.</span></span> <span data-ttu-id="d3019-123">Exchange UM サーバーは、サポートされている Lync Server 2013 プールとは異なるドメインに展開できます。</span><span class="sxs-lookup"><span data-stu-id="d3019-123">Exchange UM servers can be deployed in different domains from the Lync Server 2013 pool they support.</span></span>

  - <span data-ttu-id="d3019-124">複数のフォレスト (リソースフォレスト)。</span><span class="sxs-lookup"><span data-stu-id="d3019-124">Multiple forest (that is, resource forest).</span></span> <span data-ttu-id="d3019-125">Lync Server 2013 は1つのフォレストに展開され、ユーザーは複数のフォレストに分散されます。</span><span class="sxs-lookup"><span data-stu-id="d3019-125">Lync Server 2013 is deployed in a single forest, and then users are distributed across multiple forests.</span></span> <span data-ttu-id="d3019-126">ユーザーの Exchange UM 属性は、Lync Server 2013 フォレストにレプリケートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3019-126">The users’ Exchange UM attributes must be replicated over to the Lync Server 2013 forest.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="d3019-127">Exchange は複数のフォレストに展開できます。</span><span class="sxs-lookup"><span data-stu-id="d3019-127">Exchange can be deployed in multiple forests.</span></span> <span data-ttu-id="d3019-128">各 Exchange 組織は、Exchange UM をそのユーザーに提供することができます。また、Exchange UM を Lync Server 2013 と同じフォレストに展開することもできます。</span><span class="sxs-lookup"><span data-stu-id="d3019-128">Each Exchange organization can provide Exchange UM to its users, or Exchange UM can be deployed in the same forest as Lync Server 2013.</span></span>

    
    <span data-ttu-id="d3019-129"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d3019-129"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

