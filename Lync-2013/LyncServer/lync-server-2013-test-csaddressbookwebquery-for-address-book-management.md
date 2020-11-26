---
title: 'Lync Server 2013: アドレス帳管理の Test-CsAddressBookWebQuery'
description: 'Lync Server 2013: アドレス帳の管理に Test-CsAddressBookWebQuery します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test-CsAddressBookWebQuery for Address Book management
ms:assetid: 977a9c1f-5f4e-4539-9a26-8748b61a57d8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429716(v=OCS.15)
ms:contentKeyID: 48184865
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c7448733ed1477d36b887648154d66c96f9e6d0b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441257"
---
# <a name="test-csaddressbookwebquery-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="f7a8e-103">Lync Server 2013 でのアドレス帳管理の Test-CsAddressBookWebQuery</span><span class="sxs-lookup"><span data-stu-id="f7a8e-103">Test-CsAddressBookWebQuery for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f7a8e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f7a8e-104">

<span> </span></span></span>

<span data-ttu-id="f7a8e-105">_**最終更新日:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="f7a8e-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="f7a8e-106">このコマンドレットを実行できるのはどのユーザーですか。既定では、次のグループのメンバーは Test-CsAddressBookWebQuery コマンドレット: RTCUniversalServerAdmins を実行することを許可されています。</span><span class="sxs-lookup"><span data-stu-id="f7a8e-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the Test-CsAddressBookWebQuery cmdlet: RTCUniversalServerAdmins.</span></span> <span data-ttu-id="f7a8e-107">このコマンドレットが割り当てられているすべての役割ベースのアクセス制御 (RBAC) ロールのリストを返すには (自分自身で作成したカスタム RBAC ロールを含む)、Windows PowerShell プロンプトから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="f7a8e-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Test-CsAddressBookService"}

<span data-ttu-id="f7a8e-108">Test-CsAddressBookService の代理トランザクションと同様に、Test-CsAddressBookWebQuery は、アドレス帳の Web クエリに対してクエリを実行して、正常に動作していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f7a8e-108">Similar to the Test-CsAddressBookService synthetic transaction, Test-CsAddressBookWebQuery performs a query against the Address Book Web Query to ensure that it is operating properly.</span></span> <span data-ttu-id="f7a8e-109">このコマンドレットは、Web チケット認証に接続し、– UserCredential で指定された資格情報を提示します。</span><span class="sxs-lookup"><span data-stu-id="f7a8e-109">The cmdlet will connect to the Web Ticket authentication and present the credentials specified in –UserCredential.</span></span> <span data-ttu-id="f7a8e-110">認証された場合、コマンドレットは、– TargetSipAddress 情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="f7a8e-110">If authenticated, the cmdlet then present the –TargetSipAddress information.</span></span> <span data-ttu-id="f7a8e-111">このコマンドレットは、連絡先に関する情報を取得できなかった場合に、成功を報告する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7a8e-111">The cmdlet should report success if it was able to retrieve the information about the contact.</span></span>

<span data-ttu-id="f7a8e-112">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="f7a8e-112">For example:</span></span>

    Test-CsAddressBookWebQuery -TargetFqdn atl-cs-001.contoso.com -UserCredential contoso\bob -UserSipAddress "sip:bob@contoso.com" -TargetSipAddress "sip:bob@contoso.com"

<div>

## <a name="see-also"></a><span data-ttu-id="f7a8e-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="f7a8e-113">See Also</span></span>


[<span data-ttu-id="f7a8e-114">Test-CsAddressBookWebQuery</span><span class="sxs-lookup"><span data-stu-id="f7a8e-114">Test-CsAddressBookWebQuery</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsAddressBookWebQuery)  
  

<span data-ttu-id="f7a8e-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f7a8e-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

