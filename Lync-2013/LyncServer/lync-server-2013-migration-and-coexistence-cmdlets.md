---
title: 'Lync Server 2013: 移行と共存のコマンドレット'
description: 'Lync Server 2013: 移行と共存のコマンドレット。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migration and coexistence cmdlets
ms:assetid: ff1a56e0-e883-473d-92fe-ca77ea4eb63b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415682(v=OCS.15)
ms:contentKeyID: 48185968
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: eecd1adad53d8f917d7db7ca201b25442a7d5e85
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399692"
---
# <a name="migration-and-coexistence-cmdlets-in-lync-server-2013"></a><span data-ttu-id="be601-103">Lync Server 2013 での移行と共存のコマンドレット</span><span class="sxs-lookup"><span data-stu-id="be601-103">Migration and coexistence cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="be601-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="be601-104">

<span> </span></span></span>

<span data-ttu-id="be601-105">_**トピックの最終更新日:** 2012-06-26_</span><span class="sxs-lookup"><span data-stu-id="be601-105">_**Topic Last Modified:** 2012-06-26_</span></span>

<span data-ttu-id="be601-106">[CsLegacyUser](https://technet.microsoft.com/library/Gg413025(v=OCS.15))コマンドレットを使用すると、Office Communications server 2007 または Microsoft lync server 2010 から Microsoft lync server 2013 にユーザーアカウントを移動することができます。</span><span class="sxs-lookup"><span data-stu-id="be601-106">The [Move-CsLegacyUser](https://technet.microsoft.com/library/Gg413025(v=OCS.15)) cmdlet provides a way for you to move user accounts from Office Communications Server 2007 or Microsoft Lync Server 2010 to Microsoft Lync Server 2013.</span></span> <span data-ttu-id="be601-107">"戻る" (たとえば、Microsoft Lync Server 2013 から Microsoft Lync Server 2010 に) ユーザーアカウントを移動する必要がある場合は、 [move-CsUser](https://technet.microsoft.com/library/Gg398528(v=OCS.15)) コマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="be601-107">If you need to move a user account "backward" (for example, from Microsoft Lync Server 2013 to Microsoft Lync Server 2010) use the [Move-CsUser](https://technet.microsoft.com/library/Gg398528(v=OCS.15)) cmdlet.</span></span>

  - <span></span>  
    <span data-ttu-id="be601-108">[Import-CsLegacyConferenceDirectory](https://technet.microsoft.com/library/Gg398418(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="be601-108">[Import-CsLegacyConferenceDirectory](https://technet.microsoft.com/library/Gg398418(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="be601-109">[インポート-CsLegacyConfiguration](https://technet.microsoft.com/library/Gg412923(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="be601-109">[Import-CsLegacyConfiguration](https://technet.microsoft.com/library/Gg412923(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="be601-110">[マージ-CsLegacyTopology](https://technet.microsoft.com/library/Gg425870(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="be601-110">[Merge-CsLegacyTopology](https://technet.microsoft.com/library/Gg425870(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="be601-111">[Move-CsApplicationEndpoint](https://technet.microsoft.com/library/Gg398188(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="be601-111">[Move-CsApplicationEndpoint](https://technet.microsoft.com/library/Gg398188(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="be601-112">[CsLegacyUser の移動](https://technet.microsoft.com/library/Gg413025(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="be601-112">[Move-CsLegacyUser](https://technet.microsoft.com/library/Gg413025(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="be601-113">[Convert-CsUserData](https://technet.microsoft.com/library/JJ205337(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="be601-113">[Convert-CsUserData](https://technet.microsoft.com/library/JJ205337(v=OCS.15))</span></span>

  - <span data-ttu-id="be601-114">[Export-CsUserData](https://technet.microsoft.com/library/JJ204897(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="be601-114">[Export-CsUserData](https://technet.microsoft.com/library/JJ204897(v=OCS.15))</span></span>

  - <span data-ttu-id="be601-115">[インポート-CsUserData](https://technet.microsoft.com/library/JJ205373(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="be601-115">[Import-CsUserData](https://technet.microsoft.com/library/JJ205373(v=OCS.15))</span></span>

  - <span data-ttu-id="be601-116">[Update-CsUserData](https://technet.microsoft.com/library/JJ205358(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="be601-116">[Update-CsUserData](https://technet.microsoft.com/library/JJ205358(v=OCS.15))</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="be601-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="be601-117">See Also</span></span>


[<span data-ttu-id="be601-118">Lync Server PowerShell ブログ</span><span class="sxs-lookup"><span data-stu-id="be601-118">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="be601-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="be601-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

