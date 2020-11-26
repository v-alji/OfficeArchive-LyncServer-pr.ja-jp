---
title: 'Lync Server 2013: Exchange UM コマンドレット'
description: 'Lync Server 2013: Exchange UM コマンドレット。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Exchange UM cmdlets
ms:assetid: 32922b9f-590d-41cc-ba57-9ed5f1caa814
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415642(v=OCS.15)
ms:contentKeyID: 48183786
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 272e791969508b488efb0aaa2db10fb645ddd81c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428399"
---
# <a name="exchange-um-cmdlets-in-lync-server-2013"></a><span data-ttu-id="ecbb8-103">Lync Server 2013 の Exchange UM コマンドレット</span><span class="sxs-lookup"><span data-stu-id="ecbb8-103">Exchange UM cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ecbb8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ecbb8-104">

<span> </span></span></span>

<span data-ttu-id="ecbb8-105">_**トピックの最終更新日:** 2012-06-26_</span><span class="sxs-lookup"><span data-stu-id="ecbb8-105">_**Topic Last Modified:** 2012-06-26_</span></span>

<span data-ttu-id="ecbb8-106">Microsoft Lync Server 2013 は、Exchange ユニファイド メッセージング (UM) と連携して、ホストされたボイス メールの自動応答およびサブスクライバー アクセスを実装します。</span><span class="sxs-lookup"><span data-stu-id="ecbb8-106">Microsoft Lync Server 2013 works together with Exchange Unified Messaging (UM) to implement Auto Attendant and Subscriber Access for hosted voice mail.</span></span> <span data-ttu-id="ecbb8-107">これらの機能は、Lync Server 管理シェルのコマンドレットを使用して管理できます。</span><span class="sxs-lookup"><span data-stu-id="ecbb8-107">These features can be managed through cmdlets in the Lync Server Management Shell.</span></span>

<div>

## <a name="exchange-um-cmdlets"></a><span data-ttu-id="ecbb8-108">Exchange UM コマンドレット</span><span class="sxs-lookup"><span data-stu-id="ecbb8-108">Exchange UM Cmdlets</span></span>

<span data-ttu-id="ecbb8-109">次のコマンドレットを使用して、Exchange UM を管理できます。</span><span class="sxs-lookup"><span data-stu-id="ecbb8-109">The following cmdlets can be used to manage Exchange UM</span></span>

<span data-ttu-id="ecbb8-110">**Exchange UM**</span><span class="sxs-lookup"><span data-stu-id="ecbb8-110">**Exchange UM**</span></span>

  - <span></span>  
    <span data-ttu-id="ecbb8-111">[Get-CsExUmContact](https://technet.microsoft.com/library/Gg412725(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ecbb8-111">[Get-CsExUmContact](https://technet.microsoft.com/library/Gg412725(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="ecbb8-112">[Move-CsExUmContact](https://technet.microsoft.com/library/Gg425842(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ecbb8-112">[Move-CsExUmContact](https://technet.microsoft.com/library/Gg425842(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="ecbb8-113">[New-CsExUmContact](https://technet.microsoft.com/library/Gg398139(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ecbb8-113">[New-CsExUmContact](https://technet.microsoft.com/library/Gg398139(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="ecbb8-114">[Remove-CsExUmContact](rehttps://technet.microsoft.com/library/Gg425842(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ecbb8-114">[Remove-CsExUmContact](rehttps://technet.microsoft.com/library/Gg425842(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="ecbb8-115">[Set-CsExUmContact](https://technet.microsoft.com/library/Gg412944(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ecbb8-115">[Set-CsExUmContact](https://technet.microsoft.com/library/Gg412944(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="ecbb8-116">[Test-CsExStorageConnectivity](https://technet.microsoft.com/library/JJ204740(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ecbb8-116">[Test-CsExStorageConnectivity](https://technet.microsoft.com/library/JJ204740(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="ecbb8-117">[Test-CsExStorageNotification](https://technet.microsoft.com/library/JJ205331(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ecbb8-117">[Test-CsExStorageNotification](https://technet.microsoft.com/library/JJ205331(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="ecbb8-118">[Test-CsExUMConnectivity](https://technet.microsoft.com/library/JJ204784(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ecbb8-118">[Test-CsExUMConnectivity](https://technet.microsoft.com/library/JJ204784(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="ecbb8-119">[Test-CsExUMVoiceMail](https://technet.microsoft.com/library/JJ205058(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ecbb8-119">[Test-CsExUMVoiceMail](https://technet.microsoft.com/library/JJ205058(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="ecbb8-120">[Get-CsHostedVoicemailPolicy](https://technet.microsoft.com/library/Gg398348(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ecbb8-120">[Get-CsHostedVoicemailPolicy](https://technet.microsoft.com/library/Gg398348(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="ecbb8-121">[Grant-CsHostedVoicemailPolicy](https://technet.microsoft.com/library/Gg412829(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ecbb8-121">[Grant-CsHostedVoicemailPolicy](https://technet.microsoft.com/library/Gg412829(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="ecbb8-122">[New-CsHostedVoicemailPolicy](https://technet.microsoft.com/library/Gg398653(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ecbb8-122">[New-CsHostedVoicemailPolicy](https://technet.microsoft.com/library/Gg398653(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="ecbb8-123">[Remove-CsHostedVoicemailPolicy](https://technet.microsoft.com/library/Gg398211(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ecbb8-123">[Remove-CsHostedVoicemailPolicy](https://technet.microsoft.com/library/Gg398211(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="ecbb8-124">[Set-CsHostedVoicemailPolicy](https://technet.microsoft.com/library/Gg412722(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ecbb8-124">[Set-CsHostedVoicemailPolicy](https://technet.microsoft.com/library/Gg412722(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="ecbb8-125">[Get-CsVoicemailReroutingConfiguration](https://technet.microsoft.com/library/Gg425732(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ecbb8-125">[Get-CsVoicemailReroutingConfiguration](https://technet.microsoft.com/library/Gg425732(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="ecbb8-126">[New-CsVoicemailReroutingConfiguration](https://technet.microsoft.com/library/Gg425849(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ecbb8-126">[New-CsVoicemailReroutingConfiguration](https://technet.microsoft.com/library/Gg425849(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="ecbb8-127">[Remove-CsVoicemailReroutingConfiguration](https://technet.microsoft.com/library/Gg398573(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ecbb8-127">[Remove-CsVoicemailReroutingConfiguration](https://technet.microsoft.com/library/Gg398573(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="ecbb8-128">[Set-CsVoicemailReroutingConfiguration](https://technet.microsoft.com/library/Gg412948(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="ecbb8-128">[Set-CsVoicemailReroutingConfiguration](https://technet.microsoft.com/library/Gg412948(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ecbb8-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="ecbb8-129">See Also</span></span>


[<span data-ttu-id="ecbb8-130">Lync Server PowerShell ブログ</span><span class="sxs-lookup"><span data-stu-id="ecbb8-130">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="ecbb8-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ecbb8-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

