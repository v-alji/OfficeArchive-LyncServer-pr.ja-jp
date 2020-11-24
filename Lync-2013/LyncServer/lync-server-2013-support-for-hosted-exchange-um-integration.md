---
title: 'Lync Server 2013: ホスト型 Exchange UM 統合のサポート'
description: Lync Server 2013 では、ホストされた Exchange UM との統合がサポートされています。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Support for hosted Exchange UM integration
ms:assetid: c7573ec3-013c-48d9-b59b-2a5427e6da35
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398821(v=OCS.15)
ms:contentKeyID: 48185376
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 88920667d703bc634921903e8e3995cb65db6873
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398120"
---
# <a name="support-for-hosted-exchange-um-integration-in-lync-server-2013"></a><span data-ttu-id="8a21f-103">Lync Server 2013 でのホスト型 Exchange UM 統合のサポート</span><span class="sxs-lookup"><span data-stu-id="8a21f-103">Support for hosted Exchange UM integration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8a21f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8a21f-104">

<span> </span></span></span>

<span data-ttu-id="8a21f-105">_**最終更新日:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="8a21f-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="8a21f-106">Lync server 2013 ExUM ルーティングアプリケーションでは、次の図に示すように、オンプレミス環境での Exchange ユニファイドメッセージング (UM) との統合をサポートしています。この場合、Lync Server 2013 と Exchange UM は両方とも企業内でローカルにインストールされているか、またはサービスプロバイダーによってホストされている Exchange UM</span><span class="sxs-lookup"><span data-stu-id="8a21f-106">The Lync Server 2013 ExUM Routing application supports integration with Exchange Unified Messaging (UM) in an on-premises environment, where Lync Server 2013 and Exchange UM are both installed locally within your enterprise, or in with Exchange UM hosted by a service provider, as shown in the following diagram.</span></span>

<span data-ttu-id="8a21f-107">![オンプレミスの Lync Server Exchange UM の展開](images/Gg398821.d6498eb9-87ee-40f3-8ecd-852f91546590(OCS.15).jpg "オンプレミスの Lync Server Exchange UM の展開")</span><span class="sxs-lookup"><span data-stu-id="8a21f-107">![On-premises Lync Server Exchange UM Deployment](images/Gg398821.d6498eb9-87ee-40f3-8ecd-852f91546590(OCS.15).jpg "On-premises Lync Server Exchange UM Deployment")</span></span>

<span data-ttu-id="8a21f-108">次のモードがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="8a21f-108">The following modes are supported:</span></span>

  - <span data-ttu-id="8a21f-109">**オンプレミスモード**   Lync Server 2013 と Exchange UM は両方とも、エンタープライズ内のローカルサーバーに展開されます。</span><span class="sxs-lookup"><span data-stu-id="8a21f-109">**On-premises Mode**   Lync Server 2013 and Exchange UM are both deployed on local servers within your enterprise.</span></span>

  - <span data-ttu-id="8a21f-110">**クロスプレミスモード**   Lync Server 2013 は企業内のローカルサーバーに展開され、Exchange UM は Microsoft Exchange Online のデータセンターなどのオンラインサービスプロバイダーの機能でホストされます。</span><span class="sxs-lookup"><span data-stu-id="8a21f-110">**Cross-premises Mode**   Lync Server 2013 is deployed on local servers within your enterprise and Exchange UM is hosted in an online service provider’s facility, such as a Microsoft Exchange Online data center.</span></span>

  - <span data-ttu-id="8a21f-111">**混在モード**   Lync Server 2013 の展開では、組織内の Microsoft Exchange Server を実行しているローカルサーバー上の一部のユーザーメールボックス、およびホストされている Exchange service データセンターにある一部のメールボックスを使用しています。</span><span class="sxs-lookup"><span data-stu-id="8a21f-111">**Mixed Mode**   Your Lync Server 2013 deployment has some user mailboxes homed on local servers running Microsoft Exchange Server within your enterprise and some mailboxes homed in a hosted Exchange service data center.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="8a21f-112">混在モードは、評価中にユーザーをホストされた Exchange UM に移行するときに、移行ソリューションとして使用することができます。また、他のユーザーを移行した後で、一部のユーザーの Exchange UM サービスをオンプレミスのままにしておくと、永続的な解決策として使用できます。</span><span class="sxs-lookup"><span data-stu-id="8a21f-112">Mixed mode can be used as a transitional solution during evaluation and stepwise migration of users to hosted Exchange UM, or as a permanent solution if you opt to keep some users’ Exchange UM services on-premises after migrating others.</span></span>

    
    </div>

<span data-ttu-id="8a21f-113">Lync Server 2013 をホストされた Exchange UM と統合するには、 *共有 SIP アドレス空間* ( *分割ドメイン* とも呼ばれます) を構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a21f-113">To integrate Lync Server 2013 with hosted Exchange UM, you must configure a *shared SIP address space* (also called a *split domain*).</span></span> <span data-ttu-id="8a21f-114">この構成では、Lync Server 2013 とサードパーティがホストする Exchange UM サービスプロバイダーは両方とも、同じ SIP ドメインアドレス空間にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="8a21f-114">In this configuration, both Lync Server 2013 and the third-party hosted Exchange UM service provider can access the same SIP domain address space.</span></span> <span data-ttu-id="8a21f-115">詳細については、計画ドキュメントの「 [Lync Server 2013 の Hosted EXCHANGE UM 統合アーキテクチャ](lync-server-2013-hosted-exchange-um-integration-architecture.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8a21f-115">For details, see [Hosted Exchange UM integration architecture in Lync Server 2013](lync-server-2013-hosted-exchange-um-integration-architecture.md) in the Planning documentation.</span></span>

<span data-ttu-id="8a21f-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8a21f-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

