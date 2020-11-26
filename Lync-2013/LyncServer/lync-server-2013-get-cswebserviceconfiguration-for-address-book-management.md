---
title: 'Lync Server 2013: アドレス帳管理の Get-CsWebServiceConfiguration'
description: 'Lync Server 2013: アドレス帳の管理に Get-CsWebServiceConfiguration します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Get-CsWebServiceConfiguration for Address Book management
ms:assetid: 0b223733-5224-47d1-9b47-2109e6f135c9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429692(v=OCS.15)
ms:contentKeyID: 48183372
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bb22d7607f9ac18cda9c8653374ae86839b033e0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427944"
---
# <a name="get-cswebserviceconfiguration-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="33a68-103">Lync Server 2013 でのアドレス帳管理の Get-CsWebServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="33a68-103">Get-CsWebServiceConfiguration for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="33a68-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="33a68-104">

<span> </span></span></span>

<span data-ttu-id="33a68-105">_**最終更新日:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="33a68-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="33a68-106">このコマンドレットを実行できるユーザー: 既定では、次のグループのメンバーは、Get-CsWebServiceConfiguration コマンドレットをローカルで実行することを許可されています: RTCUniversalUserAdmins、RTCUniversalServerAdmins。</span><span class="sxs-lookup"><span data-stu-id="33a68-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the Get-CsWebServiceConfiguration cmdlet locally: RTCUniversalUserAdmins, RTCUniversalServerAdmins.</span></span> <span data-ttu-id="33a68-107">このコマンドレットが割り当てられているすべての役割ベースのアクセス制御 (RBAC) ロールのリストを返すには (自分自身で作成したカスタム RBAC ロールを含む)、Windows PowerShell プロンプトから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="33a68-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Get-CsWebServiceConfiguration"}

<span data-ttu-id="33a68-108">Get-CsWebServiceConfiguration は、組織で現在使用されている Web サービス構成の情報を返します。</span><span class="sxs-lookup"><span data-stu-id="33a68-108">Get-CsWebServiceConfiguration returns information of the Web Services configuration currently in use in your organization.</span></span> <span data-ttu-id="33a68-109">アドレス帳サービスの対象となるのは、配布リスト展開関数の状態です。</span><span class="sxs-lookup"><span data-stu-id="33a68-109">Of interest to the Address Book Services is the status of Distribution List Expansion function.</span></span> <span data-ttu-id="33a68-110">属性 EnableGroupExpansion が True の場合は、現在、組織でグループの展開が許可されています。</span><span class="sxs-lookup"><span data-stu-id="33a68-110">If the attribute EnableGroupExpansion is True, your organization currently allows group expansion.</span></span>

<span data-ttu-id="33a68-111">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="33a68-111">For example:</span></span>

    Get-CsWebServiceConfiguration -Identity site:Redmond

<div>

## <a name="see-also"></a><span data-ttu-id="33a68-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="33a68-112">See Also</span></span>


[<span data-ttu-id="33a68-113">Get-CsWebServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="33a68-113">Get-CsWebServiceConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsWebServiceConfiguration)  
  

<span data-ttu-id="33a68-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="33a68-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

