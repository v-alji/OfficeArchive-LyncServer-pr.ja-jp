---
title: 'Lync Server 2013: ボイスポリシーコマンドレット'
description: 'Lync Server 2013: ボイスポリシーコマンドレット。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Voice policy cmdlets
ms:assetid: 92744ec6-754d-498b-b430-dcd5c985ce10
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415663(v=OCS.15)
ms:contentKeyID: 48184800
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 88f87f232ab9922a3e204f11e5231457a867426a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443343"
---
# <a name="voice-policy-cmdlets-in-lync-server-2013"></a><span data-ttu-id="95e0b-103">Lync Server 2013 の音声ポリシーコマンドレット</span><span class="sxs-lookup"><span data-stu-id="95e0b-103">Voice policy cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="95e0b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="95e0b-104">

<span> </span></span></span>

<span data-ttu-id="95e0b-105">_**最終更新日:** 2013-02-18_</span><span class="sxs-lookup"><span data-stu-id="95e0b-105">_**Topic Last Modified:** 2013-02-18_</span></span>

<span data-ttu-id="95e0b-106">エンタープライズボイスの管理には、ボイスポリシーやダイヤルプランなどの設定や、ボイスポリシーとボイスルートの関連付けなどが含まれます。</span><span class="sxs-lookup"><span data-stu-id="95e0b-106">Managing Enterprise Voice includes configuring such things as voice policies and dial plans, and associating voice policies with voice routes.</span></span> <span data-ttu-id="95e0b-107">音声ポリシーの管理に関連するコマンドレットを使用して、同時呼び出し (ユーザーが会社の電話に通話を発信するたびに2番目の電話をかける機能)、着信の転送、ダイヤルの要件などの機能を設定できます。</span><span class="sxs-lookup"><span data-stu-id="95e0b-107">Cmdlets related to managing voice policies can be used to set features such as simultaneous ringing (the ability to have a second phone ring each time someone calls your office phone), call forwarding, and dialing requirement.</span></span>

<div>

## <a name="voice-policy-cmdlets"></a><span data-ttu-id="95e0b-108">ボイスポリシーコマンドレット</span><span class="sxs-lookup"><span data-stu-id="95e0b-108">Voice Policy Cmdlets</span></span>

<span data-ttu-id="95e0b-109">次のコマンドレットを使用して、エンタープライズ Voip の音声ポリシーおよびダイヤルプランを管理できます。</span><span class="sxs-lookup"><span data-stu-id="95e0b-109">The following cmdlets can be used to manage voice policies and dial plans for Enterprise Voice.</span></span>

<span data-ttu-id="95e0b-110">**音声ポリシー**</span><span class="sxs-lookup"><span data-stu-id="95e0b-110">**Voice Policy**</span></span>

  - <span></span>  
    <span data-ttu-id="95e0b-111">[Get-CsDialPlan](https://technet.microsoft.com/library/Gg413043(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="95e0b-111">[Get-CsDialPlan](https://technet.microsoft.com/library/Gg413043(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="95e0b-112">[Grant-CsDialPlan](https://technet.microsoft.com/library/Gg398547(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="95e0b-112">[Grant-CsDialPlan](https://technet.microsoft.com/library/Gg398547(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="95e0b-113">[New-CsDialPlan](https://technet.microsoft.com/library/Gg425860(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="95e0b-113">[New-CsDialPlan](https://technet.microsoft.com/library/Gg425860(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="95e0b-114">[Remove-CsDialPlan](https://technet.microsoft.com/library/Gg398791(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="95e0b-114">[Remove-CsDialPlan](https://technet.microsoft.com/library/Gg398791(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="95e0b-115">[Set-CsDialPlan](https://technet.microsoft.com/library/Gg398644(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="95e0b-115">[Set-CsDialPlan](https://technet.microsoft.com/library/Gg398644(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="95e0b-116">[Test-CsDialPlan](https://technet.microsoft.com/library/Gg399024(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="95e0b-116">[Test-CsDialPlan](https://technet.microsoft.com/library/Gg399024(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="95e0b-117">[Get-CsPstnUsage](https://technet.microsoft.com/library/Gg412734(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="95e0b-117">[Get-CsPstnUsage](https://technet.microsoft.com/library/Gg412734(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="95e0b-118">[Set-CsPstnUsage](https://technet.microsoft.com/library/Gg399069(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="95e0b-118">[Set-CsPstnUsage](https://technet.microsoft.com/library/Gg399069(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="95e0b-119">[Get-CsVoicePolicy](https://technet.microsoft.com/library/Gg398101(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="95e0b-119">[Get-CsVoicePolicy](https://technet.microsoft.com/library/Gg398101(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="95e0b-120">[Grant-CsVoicePolicy](https://technet.microsoft.com/library/Gg398828(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="95e0b-120">[Grant-CsVoicePolicy](https://technet.microsoft.com/library/Gg398828(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="95e0b-121">[New-CsVoicePolicy](https://technet.microsoft.com/library/Gg425856(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="95e0b-121">[New-CsVoicePolicy](https://technet.microsoft.com/library/Gg425856(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="95e0b-122">[Remove-CsVoicePolicy](https://technet.microsoft.com/library/Gg398309(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="95e0b-122">[Remove-CsVoicePolicy](https://technet.microsoft.com/library/Gg398309(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="95e0b-123">[Set-CsVoicePolicy](https://technet.microsoft.com/library/Gg399021(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="95e0b-123">[Set-CsVoicePolicy](https://technet.microsoft.com/library/Gg399021(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="95e0b-124">[テスト-CsVoicePolicy](https://technet.microsoft.com/library/Gg398310(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="95e0b-124">[Test-CsVoicePolicy](https://technet.microsoft.com/library/Gg398310(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="95e0b-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="95e0b-125">See Also</span></span>


[<span data-ttu-id="95e0b-126">Lync Server 2013 のエンタープライズボイスコマンドレット</span><span class="sxs-lookup"><span data-stu-id="95e0b-126">Enterprise Voice cmdlets in Lync Server 2013</span></span>](lync-server-2013-enterprise-voice-cmdlets.md)  


[<span data-ttu-id="95e0b-127">Lync Server PowerShell ブログ</span><span class="sxs-lookup"><span data-stu-id="95e0b-127">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="95e0b-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="95e0b-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

