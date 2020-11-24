---
title: 'Lync Server 2013: 会議のための場所に基づくルーティングの構成'
description: 'Lync Server 2013: 会議の Location-Based ルーティングの構成。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuration of Location-Based Routing for conferencing
ms:assetid: d8c708cc-a1b1-48b1-808c-a64df15f7701
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362846(v=OCS.15)
ms:contentKeyID: 56335088
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6a87f9c799e565f64b0dd30ce025a4e7a3174625
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399950"
---
# <a name="configuration-of-location-based-routing-for-conferencing-in-lync-server-2013"></a><span data-ttu-id="1e034-103">Lync Server 2013 での会議のための場所に基づくルーティングの構成</span><span class="sxs-lookup"><span data-stu-id="1e034-103">Configuration of Location-Based Routing for conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1e034-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1e034-104">

<span> </span></span></span>

<span data-ttu-id="1e034-105">_**最終更新日:** 2013-09-11_</span><span class="sxs-lookup"><span data-stu-id="1e034-105">_**Topic Last Modified:** 2013-09-11_</span></span>

<span data-ttu-id="1e034-106">Location-Based ルーティング会議アプリケーションは、Lync Server 2013 Location-Based ルーティングの構成に依存しています。</span><span class="sxs-lookup"><span data-stu-id="1e034-106">The Location-Based Routing Conferencing application relies on the configuration of Lync Server 2013 Location-Based Routing.</span></span> <span data-ttu-id="1e034-107">主な構成は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="1e034-107">The main configurations are the following:</span></span>

  - <span data-ttu-id="1e034-108">会議の参加者の場所は、ネットワーク サイトに基づいて決定されます。</span><span class="sxs-lookup"><span data-stu-id="1e034-108">The location of participants joining a meeting is determined based on their network site.</span></span> <span data-ttu-id="1e034-109">Location-Based ルーティングを適用するには、ネットワークサイトとそれに関連付けられたネットワークサブネットが Lync Server で定義されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="1e034-109">A network site and its associated network subnets must be defined in Lync Server in order to enforce Location-Based Routing.</span></span>

  - <span data-ttu-id="1e034-110">会議の Location-Based ルーティングを適用するには、Location-Based ルーティング用に Lync 参加者を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1e034-110">To enforce Location-Based Routing of meetings, Lync participants must be enabled for Location-Based Routing.</span></span>

  - <span data-ttu-id="1e034-111">会議に参加する PSTN エンドポイントの Location-Based ルーティングを適用するには、PSTN エンドポイントを接続するために使用される SIP トランクを Location-Based ルーティング用に構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1e034-111">To enforce Location-Based Routing of PSTN endpoints joining meetings, the SIP trunk used to connect the PSTN endpoints must be configured for Location-Based Routing.</span></span>

<span data-ttu-id="1e034-112">Lync Server 2013 Location-Based ルーティングの展開と構成の詳細については、「 [場所ベースのルーティング](lync-server-2013-configuring-location-based-routing.md)を構成する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1e034-112">For additional information on deploying and configuring Lync Server 2013 Location-Based Routing, please refer Configuring [Location-Based Routing](lync-server-2013-configuring-location-based-routing.md).</span></span>

<div>

## <a name="enabling-the-location-based-routing-conferencing-application"></a><span data-ttu-id="1e034-113">Location-Based ルーティング会議アプリケーションを有効にする</span><span class="sxs-lookup"><span data-stu-id="1e034-113">Enabling the Location-Based Routing Conferencing Application</span></span>

<span data-ttu-id="1e034-114">Location-Based ルーティング会議アプリケーションは、既定では無効になっています。</span><span class="sxs-lookup"><span data-stu-id="1e034-114">The Location-Based Routing Conferencing application is disabled by default.</span></span> <span data-ttu-id="1e034-115">このアプリケーションを有効にする前に、このアプリケーションに割り当てるのに適した優先順位を決める必要があります。</span><span class="sxs-lookup"><span data-stu-id="1e034-115">Before enabling this application, you need to determine the right priority to assign for the application.</span></span> <span data-ttu-id="1e034-116">この優先度を決定するには、Lync Server 管理シェルで次のコマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="1e034-116">To determine this priority, run the following cmdlet in Lync Server Management Shell:</span></span>

```powershell
Get-CsServerApplication -Identity Service:Registrar:<Pool FQDN>
```

<span data-ttu-id="1e034-117">このコマンドレットで \<Pool FQDN\> は、Location-Based ルーティング会議アプリケーションを有効にするプールを指定します。</span><span class="sxs-lookup"><span data-stu-id="1e034-117">In this cmdlet, \<Pool FQDN\> is the pool in which the Location-Based Routing Conferencing application is to be enabled.</span></span>

<span data-ttu-id="1e034-118">このコマンドレットは、Lync Server によってホストされているアプリケーションの一覧とそれぞれの priority の値を返します。</span><span class="sxs-lookup"><span data-stu-id="1e034-118">This cmdlet will return the list of the applications hosted by Lync Server and the priority value for each of them.</span></span> <span data-ttu-id="1e034-119">Location-Based ルーティング会議アプリケーションには、"UdcAgent" アプリケーションよりも大きく、"DefaultRouting"、"ExumRouting"、"OutboundRouting" アプリケーションよりも小さい優先度の値を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="1e034-119">The Location-Based Routing Conferencing application needs to be assigned a priority value larger than the “UdcAgent” application and smaller than the “DefaultRouting”, “ExumRouting” and “OutboundRouting” applications.</span></span> <span data-ttu-id="1e034-120">Location-Based ルーティング会議アプリケーションには、"UdcAgent" アプリケーションの優先度値より1ポイント高い優先度の値を割り当てることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="1e034-120">We recommend that you assign the Location-Based Routing Conferencing application a priority value that is one point higher than the priority value of the “UdcAgent” application.</span></span>

<span data-ttu-id="1e034-121">たとえば、"UdcAgent" アプリケーションの優先度値が "2" の場合 "DefaultRouting" アプリケーションの優先度値は "8" で、"ExumRouting" アプリケーションの優先度値は "9" で、"OutboundRouting" アプリケーションには "10" という優先度の値が設定されています。その場合は、Location-Based ルーティング会議アプリケーションに優先度値 "3" を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="1e034-121">For example, if the “UdcAgent” application has a priority value of “2”, the “DefaultRouting” application has a priority value of “8”, the “ExumRouting” application has a priority value of “9” and the “OutboundRouting” application has a priority value of “10” then you should assign the Location-Based Routing Conferencing application a priority value of “3”.</span></span> <span data-ttu-id="1e034-122">こうすると、アプリケーションの優先度が次の順序で設定されます。その他のアプリケーション (優先度: 0 から 1)、"UdcAgent" (優先度: 2)、Location-Based ルーティング会議アプリケーション (優先度: 3)、その他のアプリケーション (優先度: 4)、その他のアプリケーション (優先度:10)、"ExumRouting" (priority:10)、"OutboundRouting" (Priority:11)。</span><span class="sxs-lookup"><span data-stu-id="1e034-122">Doing so would place the priority of the applications in the following order: Other applications (Priorities: 0 to 1), “UdcAgent” (Priority: 2), Location-Based Routing Conferencing application (Priority: 3), other applications (Priorities: 4 to 8), “DefaultRouting” (Priority: 9), “ExumRouting” (Priority: 10) and “OutboundRouting” (Priority: 11).</span></span>

<span data-ttu-id="1e034-123">Location-Based ルーティング会議アプリケーションの正しい優先度の値を見つけたら、次のコマンドレットを使用して、ユーザーが Location-Based ルーティング用に有効になっている各 Front-End プールまたは Standard Edition Server に対して、次のコマンドレットを入力します。</span><span class="sxs-lookup"><span data-stu-id="1e034-123">After you find the correct priority value for the Location-Based Routing Conferencing application, type the following cmdlet for each Front-End pool or Standard Edition Server that homes users enabled for Location-Based Routing:</span></span>

```powershell
New-CsServerApplication -Identity Service:Registrar:<Pool FQDN>/LBRouting -Priority <Application Priority> -Enabled $true -Critical $true -Uri http://www.microsoft.com/LCS/LBRouting
```

<span data-ttu-id="1e034-124">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="1e034-124">For example:</span></span>

```powershell
New-CsServerApplication -Identity Service:Registrar:LS2013CU2LBRPool.contoso.com/LBRouting -Priority 3 -Enabled $true -Critical $true -Uri http://www.microsoft.com/LCS/LBRouting
```

<span data-ttu-id="1e034-125">このコマンドレットを使用した後、Location-Based ルーティング会議アプリケーションが有効になっているプールまたは Standard Edition サーバーで、すべてのフロントエンドサーバーを再起動します。</span><span class="sxs-lookup"><span data-stu-id="1e034-125">After using this cmdlet, restart all Front End servers in the pool or the Standard Edition Servers where the Location-Based Routing Conferencing application has been enabled.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="1e034-126">Enforcements での会議または提案転送へのルーティングは、該当するプールまたは Standard Edition サーバーのすべてのフロントエンドサーバーが再起動されるまでは適用されません。 Location-Based</span><span class="sxs-lookup"><span data-stu-id="1e034-126">Location-Based Routing enforcements to conferences or consultative transfers won’t be enforced until all the Front End Servers in the applicable pools or the Standard Edition Servers are restarted.</span></span>



</div>

<span data-ttu-id="1e034-127">Location-Based ルーティング会議アプリケーションが正常に有効になり、適用可能なすべての Lync サーバーが再起動されると、Location-Based ルーティングが有効になっている Lync ユーザーによって開催されたすべての会議が監視され、PSTN の有料電話のバイパスを防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="1e034-127">Once the Location-Based Routing Conferencing application has been successfully enabled and all applicable Lync servers have been restarted, all conferences organized by Lync users enabled for Location-Based Routing will be monitored to prevent PSTN toll bypass</span></span>

<span data-ttu-id="1e034-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1e034-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

