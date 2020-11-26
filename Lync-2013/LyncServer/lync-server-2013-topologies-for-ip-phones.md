---
title: 'Lync Server 2013: IP 電話のトポロジ'
description: 'Lync Server 2013: IP 電話のトポロジ。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Topologies for IP phones
ms:assetid: 26ebffcf-43ff-4e70-847d-0fbc90e94e57
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425740(v=OCS.15)
ms:contentKeyID: 48183662
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7a151a83a69e1f7e14dcbed8d8ab1038157fa839
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439670"
---
# <a name="topologies-for-ip-phones-in-lync-server-2013"></a><span data-ttu-id="c9fa3-103">Lync Server 2013 の IP 電話のトポロジ</span><span class="sxs-lookup"><span data-stu-id="c9fa3-103">Topologies for IP phones in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c9fa3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c9fa3-104">

<span> </span></span></span>

<span data-ttu-id="c9fa3-105">_**最終更新日:** 2012-06-21_</span><span class="sxs-lookup"><span data-stu-id="c9fa3-105">_**Topic Last Modified:** 2012-06-21_</span></span>

<span data-ttu-id="c9fa3-106">このセクションでは、接続プロセスの概要について説明し、IP 電話が内部と外部のネットワークで接続する方法の違いについて説明します。</span><span class="sxs-lookup"><span data-stu-id="c9fa3-106">This section provides an overview of the connectivity process and explains the differences between how an IP phone connects in an internal and external network.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="c9fa3-107">Lync Server では、次の IP 電話がサポートされています。 Aastra 6721ip の共通エリアフォン、Aastra 6721ip 卓上電話、HP 4110 IP 電話 (卓上電話)、HP 4120 IP 電話 (卓上電話)、Polycom CX600 ip 卓上電話、Polycom CX700 ip 卓上電話、Polycom POLYCOM IP 会議電話。</span><span class="sxs-lookup"><span data-stu-id="c9fa3-107">Lync Server provides support for the following IP phones: the Aastra 6721ip common area phone, Aastra 6725ip desk phone, HP 4110 IP Phone (common area phone), HP 4120 IP Phone (desk phone), Polycom CX600 IP desk phone, Polycom CX700 IP desk phone, Polycom CX500 IP common area phone, and Polycom CX3000 IP conference phone.</span></span> <span data-ttu-id="c9fa3-108">これらの携帯電話では、Polycom CX700 以外はすべて Lync Phone Edition を実行できます。</span><span class="sxs-lookup"><span data-stu-id="c9fa3-108">Of those phones, all but the Polycom CX700 can run Lync Phone Edition.</span></span>



</div>

<span data-ttu-id="c9fa3-109">次の図は、企業環境内のデバイス接続に関連するすべてのコンポーネントについて説明しています。</span><span class="sxs-lookup"><span data-stu-id="c9fa3-109">The following diagram describes all the components involved in device connectivity within the corporate environment.</span></span>

<span data-ttu-id="c9fa3-110">**内部トポロジ**</span><span class="sxs-lookup"><span data-stu-id="c9fa3-110">**Internal Topology**</span></span>

<span data-ttu-id="c9fa3-111">![3d88893e-df57-46e3-855a-a1d24589030a](images/Gg425740.3d88893e-df57-46e3-855a-a1d24589030a(OCS.15).jpg "3d88893e-df57-46e3-855a-a1d24589030a")</span><span class="sxs-lookup"><span data-stu-id="c9fa3-111">![3d88893e-df57-46e3-855a-a1d24589030a](images/Gg425740.3d88893e-df57-46e3-855a-a1d24589030a(OCS.15).jpg "3d88893e-df57-46e3-855a-a1d24589030a")</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="c9fa3-112">上の図は論理的な表現であり、物理的な概要ではありません。</span><span class="sxs-lookup"><span data-stu-id="c9fa3-112">The previous figure is a logical representation, not a physical overview.</span></span> <span data-ttu-id="c9fa3-113">たとえば、Active Directory ドメインサービス (AD DS) は、Lync Server コンポーネントと同じコンピューター上に存在することはほとんどありません。</span><span class="sxs-lookup"><span data-stu-id="c9fa3-113">For example, Active Directory Domain Services (AD DS) is rarely located on the same machine as any Lync Server components.</span></span> <span data-ttu-id="c9fa3-114">ユーザーストアはバックエンドサーバーまたはアーカイブおよび監視サーバー上に配置できます。</span><span class="sxs-lookup"><span data-stu-id="c9fa3-114">The user store can be located on the Back End Server or on the Archiving and Monitoring Servers.</span></span> <span data-ttu-id="c9fa3-115">Lync Server 管理シェル、web サーバー、更新サービスはすべて、フロントエンドサーバーの役割の一部です。</span><span class="sxs-lookup"><span data-stu-id="c9fa3-115">The Lync Server Management Shell, web server, and update services are all part of the Front End Server role.</span></span>



</div>

<span data-ttu-id="c9fa3-116">次の図は、デバイスが企業ネットワークの外部にある場合に関連するコンポーネントの概要を示しています。</span><span class="sxs-lookup"><span data-stu-id="c9fa3-116">The following diagram provides an overview of the components involved when the device is located outside the corporate network.</span></span>

<span data-ttu-id="c9fa3-117">**外部トポロジ**</span><span class="sxs-lookup"><span data-stu-id="c9fa3-117">**External Topology**</span></span>

<span data-ttu-id="c9fa3-118">![8ce6bb8e-b89c-4c4e-ac6d-41ac6c68f6f3](images/Gg425740.8ce6bb8e-b89c-4c4e-ac6d-41ac6c68f6f3(OCS.15).jpg "8ce6bb8e-b89c-4c4e-ac6d-41ac6c68f6f3")</span><span class="sxs-lookup"><span data-stu-id="c9fa3-118">![8ce6bb8e-b89c-4c4e-ac6d-41ac6c68f6f3](images/Gg425740.8ce6bb8e-b89c-4c4e-ac6d-41ac6c68f6f3(OCS.15).jpg "8ce6bb8e-b89c-4c4e-ac6d-41ac6c68f6f3")</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="c9fa3-119">デバイス更新 Web サービスでは、外部と内部の web サイトが提供されますが、外部の web サイトのみがここに表示されます。</span><span class="sxs-lookup"><span data-stu-id="c9fa3-119">The Device Update Web service provides an external and internal website, but only the external one is shown here.</span></span><BR><span data-ttu-id="c9fa3-120">外部アクセスを有効にするには、レジストラーの場所と、組織のデバイス更新 Web サービスの URL が DNS に公開されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="c9fa3-120">The location of the Registrar and the URL of the Device Update Web service for the organization must be published in DNS if external access is to be enabled.</span></span> <span data-ttu-id="c9fa3-121">さらに、エッジサーバーを展開し、デバイスから企業環境への外部通信を許可するように適切に構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c9fa3-121">Additionally, the Edge Server must be deployed and correctly configured to allow external communications from the device to the corporate environment and back.</span></span> <span data-ttu-id="c9fa3-122">Edge の展開はデバイス接続に固有ではないため、前の図では省略します。</span><span class="sxs-lookup"><span data-stu-id="c9fa3-122">This is omitted from the previous diagram because Edge deployment is not specific to device connectivity.</span></span>



<span data-ttu-id="c9fa3-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c9fa3-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

