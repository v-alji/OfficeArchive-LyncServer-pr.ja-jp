---
title: ユーザー id を使用する Skype for Business Online のコマンドレット
description: ユーザー id を使用する Skype for Business Online のコマンドレット。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Cmdlets that use a user identity
ms:assetid: be87409f-6372-4c70-91ac-6ef13dfbe65a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362842(v=OCS.15)
ms:contentKeyID: 56558859
ms.date: 05/04/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 29f838317f8b2779de862eb2df82ae1b348871e4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398564"
---
# <a name="cmdlets-in-skype-for-business-online-that-use-a-user-identity"></a><span data-ttu-id="3b659-103">ユーザー id を使用する Skype for Business Online のコマンドレット</span><span class="sxs-lookup"><span data-stu-id="3b659-103">Cmdlets in Skype for Business Online that use a user identity</span></span>

 


<span data-ttu-id="3b659-104">Skype for Business Online には、個々のユーザー Id を参照するさまざまな方法があります。</span><span class="sxs-lookup"><span data-stu-id="3b659-104">In Skype for Business Online, there are a number of different ways to reference an individual user Identity:</span></span>

  - <span data-ttu-id="3b659-105">ユーザーの Active Directory ドメインサービスの表示名を使用します。</span><span class="sxs-lookup"><span data-stu-id="3b659-105">Use the user’s Active Directory Domain Services display name.</span></span> <span data-ttu-id="3b659-106">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="3b659-106">For example:</span></span>
    
        -Identity "Ken Myer"

  - <span data-ttu-id="3b659-107">ユーザーの SIP アドレスを使用します。</span><span class="sxs-lookup"><span data-stu-id="3b659-107">Use the user’s SIP address.</span></span> <span data-ttu-id="3b659-108">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="3b659-108">For example:</span></span>
    
        -Identity "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="3b659-109">ユーザーの UPN を使用します。</span><span class="sxs-lookup"><span data-stu-id="3b659-109">Use the user’s UPN.</span></span> <span data-ttu-id="3b659-110">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="3b659-110">For example:</span></span>
    
        -Identity " kenmyer@litwareinc.com"

  - <span data-ttu-id="3b659-111">ユーザーの Active Directory ドメインサービスの識別名を使用します。</span><span class="sxs-lookup"><span data-stu-id="3b659-111">Use the user’s Active Directory Domain Services distinguished name.</span></span> <span data-ttu-id="3b659-112">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="3b659-112">For example:</span></span>
    
        -Identity "CN=48ebd1ba-95d4-460c-b751-811ebf0c4611,OU=fa8226f5-14fa-46da-8 236-039b25bc7a27,OU=Lync Online Tenants,DC=litwareinc,DC=com"

<span data-ttu-id="3b659-113">次のコマンドレットは、ユーザー Id を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="3b659-113">The following cmdlets accept a user Identity:</span></span>

  - <span data-ttu-id="3b659-114">[Disable-CsMeetingRoom](https://technet.microsoft.com/library/jj204723\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="3b659-114">[Disable-CsMeetingRoom](https://technet.microsoft.com/library/jj204723\(v=ocs.15\))</span></span>

  - <span data-ttu-id="3b659-115">[Enable-CsMeetingRoom](https://technet.microsoft.com/library/jj205062\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="3b659-115">[Enable-CsMeetingRoom](https://technet.microsoft.com/library/jj205062\(v=ocs.15\))</span></span>

  - <span data-ttu-id="3b659-116">[Get-CsExUmContact](https://technet.microsoft.com/library/gg412725\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="3b659-116">[Get-CsExUmContact](https://technet.microsoft.com/library/gg412725\(v=ocs.15\))</span></span>

  - <span data-ttu-id="3b659-117">[Get-CsMeetingRoom](https://technet.microsoft.com/library/jj205277\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="3b659-117">[Get-CsMeetingRoom](https://technet.microsoft.com/library/jj205277\(v=ocs.15\))</span></span>

  - <span data-ttu-id="3b659-118">[Get-CsOnlineUser](https://technet.microsoft.com/library/jj994026\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="3b659-118">[Get-CsOnlineUser](https://technet.microsoft.com/library/jj994026\(v=ocs.15\))</span></span>

  - <span data-ttu-id="3b659-119">[Get-CsUserAcp](https://technet.microsoft.com/library/gg398978\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="3b659-119">[Get-CsUserAcp](https://technet.microsoft.com/library/gg398978\(v=ocs.15\))</span></span>

  - <span data-ttu-id="3b659-120">[New-CsExUmContact](https://technet.microsoft.com/library/gg398139\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="3b659-120">[New-CsExUmContact](https://technet.microsoft.com/library/gg398139\(v=ocs.15\))</span></span>

  - <span data-ttu-id="3b659-121">[Remove-CsExUmContact](https://technet.microsoft.com/library/gg398946\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="3b659-121">[Remove-CsExUmContact](https://technet.microsoft.com/library/gg398946\(v=ocs.15\))</span></span>

  - <span data-ttu-id="3b659-122">[CsUserAcp の削除](https://technet.microsoft.com/library/gg398982\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="3b659-122">[Remove-CsUserAcp](https://technet.microsoft.com/library/gg398982\(v=ocs.15\))</span></span>

  - <span data-ttu-id="3b659-123">[Set-CsExUmContact](https://technet.microsoft.com/library/gg412944\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="3b659-123">[Set-CsExUmContact](https://technet.microsoft.com/library/gg412944\(v=ocs.15\))</span></span>

  - <span data-ttu-id="3b659-124">[Set-CsMeetingRoom](https://technet.microsoft.com/library/jj204831\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="3b659-124">[Set-CsMeetingRoom](https://technet.microsoft.com/library/jj204831\(v=ocs.15\))</span></span>

  - <span data-ttu-id="3b659-125">[Set-CsUserAcp](https://technet.microsoft.com/library/gg413018\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="3b659-125">[Set-CsUserAcp](https://technet.microsoft.com/library/gg413018\(v=ocs.15\))</span></span>

<span data-ttu-id="3b659-126">**Get Cs** コマンドレットのいずれかを呼び出す場合は、ユーザー id を指定する必要はないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="3b659-126">Note that you do not need to specify a user Identity when calling one of the **Get-Cs** cmdlets.</span></span> <span data-ttu-id="3b659-127">この場合、コマンドレットは指定された項目のすべてのインスタンスを返します。</span><span class="sxs-lookup"><span data-stu-id="3b659-127">In this case, the cmdlets return all the instances of the specified item.</span></span> <span data-ttu-id="3b659-128">たとえば、次のコマンドは、Skype for Business Online が有効になっているすべてのユーザーに関する情報を返します。</span><span class="sxs-lookup"><span data-stu-id="3b659-128">For example, this command returns information about all the users who have been enabled for Skype for Business Online:</span></span>

    Get-CsOnlineUser

<span data-ttu-id="3b659-129">Identity パラメーターが必要になるのは、特定のユーザーに関する情報を返す場合のみです。</span><span class="sxs-lookup"><span data-stu-id="3b659-129">The Identity parameter is required only if you want to return information for a specific user:</span></span>

    Get-CsOnlineUser -Identity "Ken Myer"

## <a name="see-also"></a><span data-ttu-id="3b659-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="3b659-130">See Also</span></span>


[<span data-ttu-id="3b659-131">Skype for Business Online の id、スコープ、テナント</span><span class="sxs-lookup"><span data-stu-id="3b659-131">Identities, scopes, and tenants in Skype for Business Online</span></span>](identities-scopes-and-tenants-in-skype-for-business-online.md)  
<span data-ttu-id="3b659-132">[Lync Online のコマンドレット](https://technet.microsoft.com/library/dn362817\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="3b659-132">[The Skype for Business Online cmdlets](https://technet.microsoft.com/library/dn362817\(v=ocs.15\))</span></span>

