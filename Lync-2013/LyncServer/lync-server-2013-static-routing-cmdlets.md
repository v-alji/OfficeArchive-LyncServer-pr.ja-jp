---
title: 'Lync Server 2013: 静的ルーティングコマンドレット'
description: 'Lync Server 2013: 静的ルーティングコマンドレット。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Static routing cmdlets
ms:assetid: 71d5e0cd-8412-4383-818a-95b851a4da4b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg416492(v=OCS.15)
ms:contentKeyID: 48184496
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 33fd251f63111cebb9297287252e666a7e10f0e1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423688"
---
# <a name="static-routing-cmdlets-in-lync-server-2013"></a><span data-ttu-id="ec3b2-103">Lync Server 2013 の静的ルーティングコマンドレット</span><span class="sxs-lookup"><span data-stu-id="ec3b2-103">Static routing cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ec3b2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ec3b2-104">

<span> </span></span></span>

<span data-ttu-id="ec3b2-105">_**最終更新日:** 2012-06-20_</span><span class="sxs-lookup"><span data-stu-id="ec3b2-105">_**Topic Last Modified:** 2012-06-20_</span></span>

<span data-ttu-id="ec3b2-106">静的ルートの場合、管理者は SIP メッセージによって取得されたネットワークルートを事前に決めることができます。</span><span class="sxs-lookup"><span data-stu-id="ec3b2-106">With static routes, administrators can predetermine the network routes taken by SIP messages.</span></span> <span data-ttu-id="ec3b2-107">サーバーによってメッセージが受信されると、サーバーはメッセージアドレスを確認し、管理者によって構成されている次ホップサーバーにメッセージを転送します。</span><span class="sxs-lookup"><span data-stu-id="ec3b2-107">When a message is received by a server, the server checks the message address and then forwards the message to the next hop server preconfigured by an administrator.</span></span> <span data-ttu-id="ec3b2-108">適切に構成されていれば、静的なルートは、迅速かつ正確にメッセージを配信し、サーバーに最小限の overheard を配置することに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="ec3b2-108">If configured correctly, static routes help ensure timely, and accurate, delivery of messages, and with minimal overheard placed on servers.</span></span>

<div>

## <a name="static-routing-cmdlets"></a><span data-ttu-id="ec3b2-109">静的なルーティングコマンドレット</span><span class="sxs-lookup"><span data-stu-id="ec3b2-109">Static Routing Cmdlets</span></span>

<span data-ttu-id="ec3b2-110">Microsoft サポート担当者から指示があった場合を除き、Microsoft Lync Server 2013 に対して構成されている静的ルートは、 [新しい-CsStaticRoute](https://technet.microsoft.com/library/Gg398265(v=OCS.15)) コマンドレットを使って作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec3b2-110">Unless otherwise instructed by Microsoft support personnel, static routes configured for Microsoft Lync Server 2013 should be created using the [New-CsStaticRoute](https://technet.microsoft.com/library/Gg398265(v=OCS.15)) cmdlet.</span></span> <span data-ttu-id="ec3b2-111">ルートを作成した後は、CsStaticRoutingConfiguration コマンドレットを使って、そのルートを静的ルーティングコレクションに追加することができます。</span><span class="sxs-lookup"><span data-stu-id="ec3b2-111">After a route has been created, you can then use the CsStaticRoutingConfiguration cmdlets to add that route to a static routing collection.</span></span>

<span data-ttu-id="ec3b2-112">**静的なルーティング**</span><span class="sxs-lookup"><span data-stu-id="ec3b2-112">**Static Routing**</span></span>

  - <span></span>  
    <span data-ttu-id="ec3b2-113">[Get-CsSipResponseCodeTranslationRule](https://technet.microsoft.com/library/Gg398130(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ec3b2-113">[Get-CsSipResponseCodeTranslationRule](https://technet.microsoft.com/library/Gg398130(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="ec3b2-114">[New-CsSipResponseCodeTranslationRule](https://technet.microsoft.com/library/Gg413041(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ec3b2-114">[New-CsSipResponseCodeTranslationRule](https://technet.microsoft.com/library/Gg413041(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="ec3b2-115">[Remove-CsSipResponseCodeTranslationRule](https://technet.microsoft.com/library/Gg412932(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ec3b2-115">[Remove-CsSipResponseCodeTranslationRule](https://technet.microsoft.com/library/Gg412932(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="ec3b2-116">[Set-CsSipResponseCodeTranslationRule](https://technet.microsoft.com/library/Gg425895(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ec3b2-116">[Set-CsSipResponseCodeTranslationRule](https://technet.microsoft.com/library/Gg425895(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="ec3b2-117">[新しい-CsStaticRoute](https://technet.microsoft.com/library/Gg398265(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ec3b2-117">[New-CsStaticRoute](https://technet.microsoft.com/library/Gg398265(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="ec3b2-118">[CsStaticRoutingConfiguration の取得](https://technet.microsoft.com/library/Gg398754(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ec3b2-118">[Get-CsStaticRoutingConfiguration](https://technet.microsoft.com/library/Gg398754(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="ec3b2-119">[新しい-CsStaticRoutingConfiguration](https://technet.microsoft.com/library/Gg425811(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ec3b2-119">[New-CsStaticRoutingConfiguration](https://technet.microsoft.com/library/Gg425811(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="ec3b2-120">[Remove-CsStaticRoutingConfiguration](https://technet.microsoft.com/library/Gg398668(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ec3b2-120">[Remove-CsStaticRoutingConfiguration](https://technet.microsoft.com/library/Gg398668(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="ec3b2-121">[設定-CsStaticRoutingConfiguration](https://technet.microsoft.com/library/Gg398724(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ec3b2-121">[Set-CsStaticRoutingConfiguration](https://technet.microsoft.com/library/Gg398724(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="ec3b2-122">[New-CsSipProxyCustom](https://technet.microsoft.com/library/Gg425904(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ec3b2-122">[New-CsSipProxyCustom](https://technet.microsoft.com/library/Gg425904(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="ec3b2-123">[新規-CsSipProxyRealm](https://technet.microsoft.com/library/Gg413084(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ec3b2-123">[New-CsSipProxyRealm](https://technet.microsoft.com/library/Gg413084(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="ec3b2-124">[新規-CsSipProxyTCP](https://technet.microsoft.com/library/Gg425745(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ec3b2-124">[New-CsSipProxyTCP](https://technet.microsoft.com/library/Gg425745(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="ec3b2-125">[新規-CsSipProxyTLS](https://technet.microsoft.com/library/Gg398629(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ec3b2-125">[New-CsSipProxyTLS](https://technet.microsoft.com/library/Gg398629(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="ec3b2-126">[New-CsSipProxyTransport](https://technet.microsoft.com/library/Gg398489(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ec3b2-126">[New-CsSipProxyTransport](https://technet.microsoft.com/library/Gg398489(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="ec3b2-127">[新規-CsSipProxyUseDefault](https://technet.microsoft.com/library/Gg398274(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ec3b2-127">[New-CsSipProxyUseDefault](https://technet.microsoft.com/library/Gg398274(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="ec3b2-128">[新規-CsSipProxyUseDefaultCert](https://technet.microsoft.com/library/Gg425858(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ec3b2-128">[New-CsSipProxyUseDefaultCert](https://technet.microsoft.com/library/Gg425858(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="ec3b2-129">[新規-CsIssuedCertId](https://technet.microsoft.com/library/Gg425814(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ec3b2-129">[New-CsIssuedCertId](https://technet.microsoft.com/library/Gg425814(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ec3b2-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="ec3b2-130">See Also</span></span>


[<span data-ttu-id="ec3b2-131">Lync Server PowerShell ブログ</span><span class="sxs-lookup"><span data-stu-id="ec3b2-131">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="ec3b2-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ec3b2-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

