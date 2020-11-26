---
title: 'Lync Server 2013: 割り当てられていない番号コマンドレット'
description: 'Lync Server 2013: 割り当てられていない番号コマンドレット。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Unassigned number cmdlets
ms:assetid: 4956dddb-199b-47f4-813f-ef3c461aaf2e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415649(v=OCS.15)
ms:contentKeyID: 48184065
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 046b5f2d7551a3fc3c62fb03c302939c9fad7f91
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436161"
---
# <a name="unassigned-number-cmdlets-in-lync-server-2013"></a><span data-ttu-id="0d71b-103">Lync Server 2013 の割り当てられていない番号コマンドレット</span><span class="sxs-lookup"><span data-stu-id="0d71b-103">Unassigned number cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0d71b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0d71b-104">

<span> </span></span></span>

<span data-ttu-id="0d71b-105">_**最終更新日:** 2012-03-21_</span><span class="sxs-lookup"><span data-stu-id="0d71b-105">_**Topic Last Modified:** 2012-03-21_</span></span>

<span data-ttu-id="0d71b-106">未割り当ての番号は、組織に属しているが、ユーザーまたは電話に割り当てられていない電話番号です。</span><span class="sxs-lookup"><span data-stu-id="0d71b-106">Unassigned numbers are phone numbers that belong to an organization but have not been assigned to a user or phone.</span></span> <span data-ttu-id="0d71b-107">割り当てられていない番号は、その番号に通話を発信したときに、さまざまな種類のお知らせを再生するように構成できます。</span><span class="sxs-lookup"><span data-stu-id="0d71b-107">Unassigned numbers can be configured to play various types of announcements when a call is made to those numbers.</span></span>

<div>

## <a name="unassigned-number-cmdlets"></a><span data-ttu-id="0d71b-108">割り当てられていない番号コマンドレット</span><span class="sxs-lookup"><span data-stu-id="0d71b-108">Unassigned Number Cmdlets</span></span>

<span data-ttu-id="0d71b-109">次のコマンドレットを使用して、割り当てられていない数値を管理できます。</span><span class="sxs-lookup"><span data-stu-id="0d71b-109">The following cmdlets can be used to manage unassigned numbers.</span></span>

<span data-ttu-id="0d71b-110">**未割り当て番号**</span><span class="sxs-lookup"><span data-stu-id="0d71b-110">**Unassigned Number**</span></span>

  - <span></span>  
    <span data-ttu-id="0d71b-111">[Get-CsUnassignedNumber](https://technet.microsoft.com/library/Gg412792(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0d71b-111">[Get-CsUnassignedNumber](https://technet.microsoft.com/library/Gg412792(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="0d71b-112">[New-CsUnassignedNumber](https://technet.microsoft.com/library/Gg398651(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0d71b-112">[New-CsUnassignedNumber](https://technet.microsoft.com/library/Gg398651(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="0d71b-113">[Remove-CsUnassignedNumber](https://technet.microsoft.com/library/Gg398209(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0d71b-113">[Remove-CsUnassignedNumber](https://technet.microsoft.com/library/Gg398209(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="0d71b-114">[Set-CsUnassignedNumber](https://technet.microsoft.com/library/Gg399033(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0d71b-114">[Set-CsUnassignedNumber](https://technet.microsoft.com/library/Gg399033(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="0d71b-115">[CsAnnouncement](https://technet.microsoft.com/library/Gg398937(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0d71b-115">[Get-CsAnnouncement](https://technet.microsoft.com/library/Gg398937(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="0d71b-116">[新しい CsAnnouncement](https://technet.microsoft.com/library/Gg398522(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0d71b-116">[New-CsAnnouncement](https://technet.microsoft.com/library/Gg398522(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="0d71b-117">[CsAnnouncement の削除](https://technet.microsoft.com/library/Gg412766(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0d71b-117">[Remove-CsAnnouncement](https://technet.microsoft.com/library/Gg412766(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="0d71b-118">[Set-CsAnnouncement](https://technet.microsoft.com/library/Gg425752(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0d71b-118">[Set-CsAnnouncement](https://technet.microsoft.com/library/Gg425752(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="0d71b-119">[Import-CsAnnouncementFile](https://technet.microsoft.com/library/Gg398472(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="0d71b-119">[Import-CsAnnouncementFile](https://technet.microsoft.com/library/Gg398472(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="0d71b-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="0d71b-120">See Also</span></span>


[<span data-ttu-id="0d71b-121">Lync Server PowerShell ブログ</span><span class="sxs-lookup"><span data-stu-id="0d71b-121">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="0d71b-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0d71b-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

