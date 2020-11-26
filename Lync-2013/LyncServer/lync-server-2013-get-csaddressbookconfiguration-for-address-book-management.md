---
title: 'Lync Server 2013: アドレス帳管理の Get-CsAddressBookConfiguration'
description: 'Lync Server 2013: アドレス帳の管理に Get-CsAddressBookConfiguration します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Get-CsAddressBookConfiguration for Address Book management
ms:assetid: bd62f916-caf3-4e10-ada4-631bbb331ef1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429721(v=OCS.15)
ms:contentKeyID: 48185264
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 91b96aead7b7038464f3166691a5952b9ff850dc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427979"
---
# <a name="get-csaddressbookconfiguration-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="36d2f-103">Lync Server 2013 でのアドレス帳管理の Get-CsAddressBookConfiguration</span><span class="sxs-lookup"><span data-stu-id="36d2f-103">Get-CsAddressBookConfiguration for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="36d2f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="36d2f-104">

<span> </span></span></span>

<span data-ttu-id="36d2f-105">_**最終更新日:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="36d2f-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="36d2f-106">このコマンドレットを実行できるユーザー: 既定では、次のグループのメンバーは、RTCUniversalServerAdmins コマンドレットをローカルで Get-CsAddressBookConfiguration 実行することを許可されています。</span><span class="sxs-lookup"><span data-stu-id="36d2f-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the Get-CsAddressBookConfiguration cmdlet locally: RTCUniversalServerAdmins.</span></span> <span data-ttu-id="36d2f-107">このコマンドレットが割り当てられているすべての役割ベースのアクセス制御 (RBAC) ロールのリストを返すには (自分自身で作成したカスタム RBAC ロールを含む)、Windows PowerShell プロンプトから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="36d2f-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Get-CsAddressBookConfiguration"}

<span data-ttu-id="36d2f-108">コマンドレット Get-CsAddressBookConfiguration は、既に存在する構成に関する情報を返します。</span><span class="sxs-lookup"><span data-stu-id="36d2f-108">The cmdlet Get-CsAddressBookConfiguration returns information about a configuration that already exists.</span></span>

<span data-ttu-id="36d2f-109">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="36d2f-109">For example:</span></span>

    Get-CsAddressBookConfiguration -Identity site:Redmond

<span data-ttu-id="36d2f-110">Get-CsAddressBookConfiguration と Set-CsAddressBookConfiguration の機能を組み合わせると、管理者は、変更する構成を定義して、変更を適用することができます。</span><span class="sxs-lookup"><span data-stu-id="36d2f-110">Combining the functionality of Get-CsAddressBookConfiguration and Set-CsAddressBookConfiguration allows the administrator to define which configurations to modify and then apply the modifications.</span></span> <span data-ttu-id="36d2f-111">たとえば、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="36d2f-111">For example, this combined:</span></span>

    Get-CsAddressBookConfiguration -Filter site:* | Set-CsAddressBookConfiguration -RunTimeOfDay 23:00

<span data-ttu-id="36d2f-112">すべてのサイト内のすべての構成を返し、23:00 時間の RunTimeOfDay を構成に適用します。</span><span class="sxs-lookup"><span data-stu-id="36d2f-112">Returns all configurations in all sites and applies the RunTimeOfDay of 23:00 hours to the configurations.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="36d2f-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="36d2f-113">See Also</span></span>


[<span data-ttu-id="36d2f-114">CsAddressBookConfiguration の入手</span><span class="sxs-lookup"><span data-stu-id="36d2f-114">Get-CsAddressBookConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsAddressBookConfiguration)  
  

<span data-ttu-id="36d2f-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="36d2f-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

