---
title: 'Lync Server 2013: ダイヤルイン会議のコマンドレット'
description: 'Lync Server 2013: ダイヤルイン会議のコマンドレット。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Dial-in conferencing cmdlets
ms:assetid: 0718f82a-91c4-466f-8443-a85002deaa48
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415630(v=OCS.15)
ms:contentKeyID: 48183320
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b19cc8a022f8d86e0b3bdd22a93f8df692404171
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429277"
---
# <a name="dial-in-conferencing-cmdlets-in-lync-server-2013"></a><span data-ttu-id="64c46-103">Lync Server 2013 でのダイヤルイン会議のコマンドレット</span><span class="sxs-lookup"><span data-stu-id="64c46-103">Dial-in conferencing cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="64c46-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="64c46-104">

<span> </span></span></span>

<span data-ttu-id="64c46-105">_**最終更新日:** 2012-03-21_</span><span class="sxs-lookup"><span data-stu-id="64c46-105">_**Topic Last Modified:** 2012-03-21_</span></span>

<span data-ttu-id="64c46-106">ダイヤルイン会議を使うと、ユーザーは "標準" 電話 (公衆交換電話網のデバイス) を使って、会議のオーディオ部分に参加することができます。</span><span class="sxs-lookup"><span data-stu-id="64c46-106">Dial-in conferencing provides a way for users to use a "regular" telephone (that is, a device on the public switched telephone network) to join the audio portion of a conference.</span></span>

<div>

## <a name="dial-in-conferencing-cmdlets"></a><span data-ttu-id="64c46-107">ダイヤルイン会議のコマンドレット</span><span class="sxs-lookup"><span data-stu-id="64c46-107">Dial-In Conferencing Cmdlets</span></span>

<span data-ttu-id="64c46-108">ダイヤルイン会議を許可したくない場合は、Set-CsConferencingPolicy コマンドレットを使用して、Enabledial In会議プロパティを False に設定することで、この機能を無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="64c46-108">If you do not want to allow dial-in conferencing you can disable this capability by using the Set-CsConferencingPolicy cmdlet and setting the EnableDialInConferencing property to False.</span></span> <span data-ttu-id="64c46-109">既定では、すべてのユーザーは、ダイヤルイン会議を含む会議を主催することができます。</span><span class="sxs-lookup"><span data-stu-id="64c46-109">By default, all users are allowed to host meetings that include dial-in conferencing.</span></span>

<span data-ttu-id="64c46-110">**ダイヤルイン会議**</span><span class="sxs-lookup"><span data-stu-id="64c46-110">**Dial-In Conferencing**</span></span>

  - <span></span>  
    <span data-ttu-id="64c46-111">[Get-CsConferenceDirectory](https://technet.microsoft.com/library/Gg425771(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="64c46-111">[Get-CsConferenceDirectory](https://technet.microsoft.com/library/Gg425771(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="64c46-112">[Move-CsConferenceDirectory](https://technet.microsoft.com/library/Gg412968(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="64c46-112">[Move-CsConferenceDirectory](https://technet.microsoft.com/library/Gg412968(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="64c46-113">[New-CsConferenceDirectory](https://technet.microsoft.com/library/Gg413080(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="64c46-113">[New-CsConferenceDirectory](https://technet.microsoft.com/library/Gg413080(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="64c46-114">[Remove-CsConferenceDirectory](rehttps://technet.microsoft.com/library/Gg412968(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="64c46-114">[Remove-CsConferenceDirectory](rehttps://technet.microsoft.com/library/Gg412968(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="64c46-115">[Test-CsDialInConferencing](https://technet.microsoft.com/library/Gg399013(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="64c46-115">[Test-CsDialInConferencing](https://technet.microsoft.com/library/Gg399013(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="64c46-116">[Get-CsDialInConferencingAccessNumber](https://technet.microsoft.com/library/Gg413015(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="64c46-116">[Get-CsDialInConferencingAccessNumber](https://technet.microsoft.com/library/Gg413015(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="64c46-117">[New-CsDialInConferencingAccessNumber](https://technet.microsoft.com/library/Gg398818(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="64c46-117">[New-CsDialInConferencingAccessNumber](https://technet.microsoft.com/library/Gg398818(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="64c46-118">[Remove-CsDialInConferencingAccessNumber](https://technet.microsoft.com/library/Gg412782(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="64c46-118">[Remove-CsDialInConferencingAccessNumber](https://technet.microsoft.com/library/Gg412782(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="64c46-119">[Set-CsDialInConferencingAccessNumber](https://technet.microsoft.com/library/Gg425770(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="64c46-119">[Set-CsDialInConferencingAccessNumber](https://technet.microsoft.com/library/Gg425770(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="64c46-120">[Get-CsDialInConferencingConfiguration](https://technet.microsoft.com/library/Gg398575(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="64c46-120">[Get-CsDialInConferencingConfiguration](https://technet.microsoft.com/library/Gg398575(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="64c46-121">[New-CsDialInConferencingConfiguration](https://technet.microsoft.com/library/Gg412816(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="64c46-121">[New-CsDialInConferencingConfiguration](https://technet.microsoft.com/library/Gg412816(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="64c46-122">[Remove-CsDialInConferencingConfiguration](https://technet.microsoft.com/library/Gg398174(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="64c46-122">[Remove-CsDialInConferencingConfiguration](https://technet.microsoft.com/library/Gg398174(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="64c46-123">[Set-CsDialInConferencingConfiguration](https://technet.microsoft.com/library/Gg425825(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="64c46-123">[Set-CsDialInConferencingConfiguration](https://technet.microsoft.com/library/Gg425825(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="64c46-124">[Get-CsDialInConferencingDtmfConfiguration](https://technet.microsoft.com/library/Gg398578(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="64c46-124">[Get-CsDialInConferencingDtmfConfiguration](https://technet.microsoft.com/library/Gg398578(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="64c46-125">[New-CsDialInConferencingDtmfConfiguration](https://technet.microsoft.com/library/Gg425792(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="64c46-125">[New-CsDialInConferencingDtmfConfiguration](https://technet.microsoft.com/library/Gg425792(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="64c46-126">[Remove-CsDialInConferencingDtmfConfiguration](https://technet.microsoft.com/library/Gg425894(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="64c46-126">[Remove-CsDialInConferencingDtmfConfiguration](https://technet.microsoft.com/library/Gg425894(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="64c46-127">[Set-CsDialInConferencingDtmfConfiguration](https://technet.microsoft.com/library/Gg398860(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="64c46-127">[Set-CsDialInConferencingDtmfConfiguration](https://technet.microsoft.com/library/Gg398860(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="64c46-128">[Get-CsDialInConferencingLanguageList](https://technet.microsoft.com/library/Gg425869(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="64c46-128">[Get-CsDialInConferencingLanguageList](https://technet.microsoft.com/library/Gg425869(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="64c46-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="64c46-129">See Also</span></span>


[<span data-ttu-id="64c46-130">Lync Server PowerShell ブログ</span><span class="sxs-lookup"><span data-stu-id="64c46-130">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="64c46-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="64c46-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

