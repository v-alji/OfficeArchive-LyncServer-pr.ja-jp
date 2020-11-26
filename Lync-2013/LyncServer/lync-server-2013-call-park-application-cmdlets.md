---
title: 'Lync Server 2013: コールパークアプリケーションコマンドレット'
description: 'Lync Server 2013: コールパークアプリケーションコマンドレット。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call Park application cmdlets
ms:assetid: 30cc001f-b29e-4d44-bad7-65e1133e67b1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415639(v=OCS.15)
ms:contentKeyID: 48183764
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 25d37e8cfad022e9e8478e68f158e1838bdcca5b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435720"
---
# <a name="call-park-application-cmdlets-in-lync-server-2013"></a><span data-ttu-id="5415d-103">Lync Server 2013 のコールパークアプリケーションコマンドレット</span><span class="sxs-lookup"><span data-stu-id="5415d-103">Call Park application cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5415d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5415d-104">

<span> </span></span></span>

<span data-ttu-id="5415d-105">_**最終更新日:** 2012-03-21_</span><span class="sxs-lookup"><span data-stu-id="5415d-105">_**Topic Last Modified:** 2012-03-21_</span></span>

<span data-ttu-id="5415d-106">[コールパーク] アプリケーションを使うと、通話を保留にして別の電話からその通話を取得することができます。</span><span class="sxs-lookup"><span data-stu-id="5415d-106">Call Park application allows a user to place a call on hold, then retrieve that call from a different phone.</span></span> <span data-ttu-id="5415d-107">以下のコマンドレットを使用して、コールパーク orbits と Call パークアプリケーションの設定を構成します。</span><span class="sxs-lookup"><span data-stu-id="5415d-107">Use these cmdlets to configure settings for call park orbits and the Call Park application.</span></span>

<div>

## <a name="call-park-application-cmdlets"></a><span data-ttu-id="5415d-108">コールパークアプリケーションコマンドレット</span><span class="sxs-lookup"><span data-stu-id="5415d-108">Call Park Application Cmdlets</span></span>

<span data-ttu-id="5415d-109">次のコマンドレットを使用して、コールパークアプリケーションを管理できます。</span><span class="sxs-lookup"><span data-stu-id="5415d-109">The following cmdlets can be used to manage Call Park application.</span></span>

<span data-ttu-id="5415d-110">**コールパークアプリケーション**</span><span class="sxs-lookup"><span data-stu-id="5415d-110">**Call Park Application**</span></span>

  - <span></span>  
    <span data-ttu-id="5415d-111">[Get-CsCallParkOrbit](https://technet.microsoft.com/library/Gg398554(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="5415d-111">[Get-CsCallParkOrbit](https://technet.microsoft.com/library/Gg398554(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="5415d-112">[新規-CsCallParkOrbit](https://technet.microsoft.com/library/Gg398936(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="5415d-112">[New-CsCallParkOrbit](https://technet.microsoft.com/library/Gg398936(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="5415d-113">[Remove-CsCallParkOrbit](https://technet.microsoft.com/library/Gg412901(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="5415d-113">[Remove-CsCallParkOrbit](https://technet.microsoft.com/library/Gg412901(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="5415d-114">[Set-CsCallParkOrbit](https://technet.microsoft.com/library/Gg398796(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="5415d-114">[Set-CsCallParkOrbit](https://technet.microsoft.com/library/Gg398796(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="5415d-115">[Set-CsCallParkServiceMusicOnHoldFile](https://technet.microsoft.com/library/Gg412836(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="5415d-115">[Set-CsCallParkServiceMusicOnHoldFile](https://technet.microsoft.com/library/Gg412836(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="5415d-116">[Get-CsCpsConfiguration](https://technet.microsoft.com/library/Gg398948(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="5415d-116">[Get-CsCpsConfiguration](https://technet.microsoft.com/library/Gg398948(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="5415d-117">[新規-CsCpsConfiguration](https://technet.microsoft.com/library/Gg412919(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="5415d-117">[New-CsCpsConfiguration](https://technet.microsoft.com/library/Gg412919(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="5415d-118">[Remove-CsCpsConfiguration](https://technet.microsoft.com/library/Gg398358(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="5415d-118">[Remove-CsCpsConfiguration](https://technet.microsoft.com/library/Gg398358(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="5415d-119">[Set-CsCpsConfiguration](https://technet.microsoft.com/library/Gg412721(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="5415d-119">[Set-CsCpsConfiguration](https://technet.microsoft.com/library/Gg412721(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="5415d-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="5415d-120">See Also</span></span>


[<span data-ttu-id="5415d-121">Lync Server PowerShell ブログ</span><span class="sxs-lookup"><span data-stu-id="5415d-121">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="5415d-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5415d-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

