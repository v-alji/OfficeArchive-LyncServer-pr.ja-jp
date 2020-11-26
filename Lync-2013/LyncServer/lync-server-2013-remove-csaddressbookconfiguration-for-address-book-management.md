---
title: アドレス帳管理の Remove-CsAddressBookConfiguration
description: アドレス帳管理の Remove-CsAddressBookConfiguration。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Remove-CsAddressBookConfiguration for Address Book management
ms:assetid: 5d173ebe-ec4d-4640-8432-a25071ea9cc5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429705(v=OCS.15)
ms:contentKeyID: 48184258
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d513c128dfe87c5a6e92b66a6ba4e1dbdfbfb651
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436441"
---
# <a name="remove-csaddressbookconfiguration-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="be20f-103">Lync Server 2013 でのアドレス帳管理の Remove-CsAddressBookConfiguration</span><span class="sxs-lookup"><span data-stu-id="be20f-103">Remove-CsAddressBookConfiguration for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="be20f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="be20f-104">

<span> </span></span></span>

<span data-ttu-id="be20f-105">_**最終更新日:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="be20f-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="be20f-106">このコマンドレットを実行できるユーザー: 既定では、次のグループのメンバーは、RTCUniversalServerAdmins コマンドレットをローカルで Remove-CsAddressBookConfiguration 実行することを許可されています。</span><span class="sxs-lookup"><span data-stu-id="be20f-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the Remove-CsAddressBookConfiguration cmdlet locally: RTCUniversalServerAdmins.</span></span> <span data-ttu-id="be20f-107">このコマンドレットが割り当てられているすべての役割ベースのアクセス制御 (RBAC) ロールのリストを返すには (自分自身で作成したカスタム RBAC ロールを含む)、Windows PowerShell プロンプトから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="be20f-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Remove-CsAddressBookConfiguration"}

<span data-ttu-id="be20f-108">名前が示すように、Remove-CsAddressBookConfiguration は定義されたサイト Id に基づいて構成を削除します。</span><span class="sxs-lookup"><span data-stu-id="be20f-108">As the name implies, Remove-CsAddressBookConfiguration will remove the configuration based on the defined Site Identity.</span></span>

<span data-ttu-id="be20f-109">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="be20f-109">For example:</span></span>

    Remove-CsAddressBookConfiguration -Identity site:Redmond

<div>

## <a name="see-also"></a><span data-ttu-id="be20f-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="be20f-110">See Also</span></span>


<span data-ttu-id="be20f-111">[CsAddressBookConfiguration の削除](https://technet.microsoft.com/library/Gg398934(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="be20f-111">[Remove-CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg398934(v=OCS.15))</span></span>  
  

<span data-ttu-id="be20f-112"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="be20f-112"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

