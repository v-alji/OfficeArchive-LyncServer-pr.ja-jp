---
title: スコープまたは id を使用しない Skype for Business Online のコマンドレット
description: スコープまたは id を使用しない Skype for Business Online のコマンドレット。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Cmdlets that do not use a scope or an identity
ms:assetid: 9c50c732-3c64-4b6a-96fd-8f528eb739ce
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362824(v=OCS.15)
ms:contentKeyID: 56558839
ms.date: 05/04/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e7d893c4cf9203c8657dfbdfd7fb2bf46dbdfe4e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398577"
---
# <a name="cmdlets-in-skype-for-business-online-that-do-not-use-a-scope-or-an-identity"></a><span data-ttu-id="e496e-103">スコープまたは id を使用しない Skype for Business Online のコマンドレット</span><span class="sxs-lookup"><span data-stu-id="e496e-103">Cmdlets in Skype for Business Online that do not use a scope or an identity</span></span>

 


<span data-ttu-id="e496e-104">許可リストとブロックリスト (ユーザーが通信できる外部組織を決定するリスト) を変更するときに使用するコマンドレットは、スコープまたは Id のどちらも使用しません。</span><span class="sxs-lookup"><span data-stu-id="e496e-104">The cmdlets used when modifying the allowed lists and blocked lists (lists that determine which outside organizations your users are allowed to communicate with) do not use either a scope or an Identity.</span></span> <span data-ttu-id="e496e-105">実際、 **CsEdgeAllowAllKnownDomains** コマンドレットには何のパラメーターもありません。</span><span class="sxs-lookup"><span data-stu-id="e496e-105">In fact, the **New-CsEdgeAllowAllKnownDomains** cmdlet does not have any parameters whatsoever.</span></span> <span data-ttu-id="e496e-106">スコープまたは Id を使用しないコマンドレットは、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="e496e-106">The cmdlets that do not use either a scope or an Identity are:</span></span>

  - <span data-ttu-id="e496e-107">[New-CsEdgeAllowAllKnownDomains](https://technet.microsoft.com/library/jj994088\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="e496e-107">[New-CsEdgeAllowAllKnownDomains](https://technet.microsoft.com/library/jj994088\(v=ocs.15\))</span></span>

  - <span data-ttu-id="e496e-108">[New-CsEdgeAllowList](https://technet.microsoft.com/library/jj994023\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="e496e-108">[New-CsEdgeAllowList](https://technet.microsoft.com/library/jj994023\(v=ocs.15\))</span></span>

  - <span data-ttu-id="e496e-109">[New-CsEdgeDomainPattern](https://technet.microsoft.com/library/jj994040\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="e496e-109">[New-CsEdgeDomainPattern](https://technet.microsoft.com/library/jj994040\(v=ocs.15\))</span></span>

<span data-ttu-id="e496e-110">**CsEdgeAllowList** コマンドレットと **CsEdgeDomainPattern** コマンドレットの両方を使用して、ドメインパラメーターを含める必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="e496e-110">Note that, with both the **New-CsEdgeAllowList** cmdlet and the **New-CsEdgeDomainPattern** cmdlet, you must include the Domain parameter.</span></span> <span data-ttu-id="e496e-111">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="e496e-111">For example:</span></span>

    $x = New-CsEdgeDomainPattern -Domain "fabrikam.com"

## <a name="see-also"></a><span data-ttu-id="e496e-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="e496e-112">See Also</span></span>


[<span data-ttu-id="e496e-113">Skype for Business Online の id、スコープ、テナント</span><span class="sxs-lookup"><span data-stu-id="e496e-113">Identities, scopes, and tenants in Skype for Business Online</span></span>](identities-scopes-and-tenants-in-skype-for-business-online.md)  
<span data-ttu-id="e496e-114">[Lync Online のコマンドレット](https://technet.microsoft.com/library/dn362817\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="e496e-114">[The Skype for Business Online cmdlets](https://technet.microsoft.com/library/dn362817\(v=ocs.15\))</span></span>

