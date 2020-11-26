---
title: 'Lync Server 2013: アドレス帳管理の Remove-CsWebServiceConfiguration'
description: 'Lync Server 2013: アドレス帳の管理に Remove-CsWebServiceConfiguration します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Remove-CsWebServiceConfiguration for Address Book management
ms:assetid: 91947cad-5cdd-41b9-83e1-650703c55879
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429713(v=OCS.15)
ms:contentKeyID: 48184848
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 145cb1cb98bcb4c988a8fdaea74a4eae86d5fc4f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436427"
---
# <a name="remove-cswebserviceconfiguration-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="e4d87-103">Lync Server 2013 でのアドレス帳管理の Remove-CsWebServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4d87-103">Remove-CsWebServiceConfiguration for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e4d87-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e4d87-104">

<span> </span></span></span>

<span data-ttu-id="e4d87-105">_**最終更新日:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="e4d87-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="e4d87-106">このコマンドレットを実行できるユーザー: 既定では、次のグループのメンバーは、RTCUniversalServerAdmins コマンドレットをローカルで Remove-CsWebServiceConfiguration 実行することを許可されています。</span><span class="sxs-lookup"><span data-stu-id="e4d87-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the Remove-CsWebServiceConfiguration cmdlet locally: RTCUniversalServerAdmins.</span></span> <span data-ttu-id="e4d87-107">このコマンドレットが割り当てられているすべての役割ベースのアクセス制御 (RBAC) ロールのリストを返すには (自分自身で作成したカスタム RBAC ロールを含む)、Windows PowerShell プロンプトから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="e4d87-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Remove-CsWebServiceConfiguration"}

<span data-ttu-id="e4d87-108">Remove-CsWebServiceConfiguration コマンドレットを使用すると、管理者は以前に作成した Web サービス構成を削除できます。</span><span class="sxs-lookup"><span data-stu-id="e4d87-108">The Remove-CsWebServiceConfiguration cmdlet allows an administrator to remove a previously created Web Services configuration.</span></span> <span data-ttu-id="e4d87-109">グローバル Web サービス構成を削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="e4d87-109">The cmdlet cannot remove the global Web Services configuration.</span></span>

<span data-ttu-id="e4d87-110">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="e4d87-110">For example:</span></span>

    Remove-CsWebServiceConfiguration -Identity site:Redmond

<div>

## <a name="see-also"></a><span data-ttu-id="e4d87-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="e4d87-111">See Also</span></span>


[<span data-ttu-id="e4d87-112">Remove-CsWebServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4d87-112">Remove-CsWebServiceConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsWebServiceConfiguration)  
  

<span data-ttu-id="e4d87-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e4d87-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

