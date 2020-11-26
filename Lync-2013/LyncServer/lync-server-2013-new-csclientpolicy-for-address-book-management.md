---
title: 'Lync Server 2013: アドレス帳管理の New-CsClientPolicy'
description: 'Lync Server 2013: アドレス帳の管理に New-CsClientPolicy します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New-CsClientPolicy for Address Book management
ms:assetid: ef4415fc-82c4-4dc8-97d1-37a084553343
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429726(v=OCS.15)
ms:contentKeyID: 48185771
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 12c14534c7af447f30a01b1bbbd1679a8375c705
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425111"
---
# <a name="new-csclientpolicy-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="bebd0-103">Lync Server 2013 でのアドレス帳管理の New-CsClientPolicy</span><span class="sxs-lookup"><span data-stu-id="bebd0-103">New-CsClientPolicy for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bebd0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bebd0-104">

<span> </span></span></span>

<span data-ttu-id="bebd0-105">_**最終更新日:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="bebd0-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="bebd0-106">このコマンドレットを実行できるのはどのユーザーですか。既定では、次のグループのメンバーは New-CsClientPolicy コマンドレット: RTCUniversalServerAdmins を実行することを許可されています。</span><span class="sxs-lookup"><span data-stu-id="bebd0-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the New-CsClientPolicy cmdlet: RTCUniversalServerAdmins.</span></span> <span data-ttu-id="bebd0-107">このコマンドレットが割り当てられているすべての役割ベースのアクセス制御 (RBAC) ロールのリストを返すには (自分自身で作成したカスタム RBAC ロールを含む)、Windows PowerShell プロンプトから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="bebd0-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "New-CsClientPolicy"}

<span data-ttu-id="bebd0-108">このコマンドレットを使用して、Lync Server 2013 で利用できる機能をクライアントに提供するための多数の設定を定義 New-CsClientPolicy ます。</span><span class="sxs-lookup"><span data-stu-id="bebd0-108">The cmdlet New-CsClientPolicy defines a large number of settings for provisioning clients for features that are available in Lync Server 2013.</span></span> <span data-ttu-id="bebd0-109">アドレス帳サービスの場合は、パラメーター住所録の可用性が重要です。</span><span class="sxs-lookup"><span data-stu-id="bebd0-109">For the Address Book Service, the parameter AddressBookAvailability is of interest.</span></span> <span data-ttu-id="bebd0-110">このパラメーターは、クライアントで利用できるオプションに直接影響を与えます。次の3つのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="bebd0-110">This parameter, which directly impacts the options available to clients, has three possible options:</span></span>

  - <span data-ttu-id="bebd0-111">WebSearchAndFileDownload</span><span class="sxs-lookup"><span data-stu-id="bebd0-111">WebSearchAndFileDownload</span></span>

  - <span data-ttu-id="bebd0-112">WebSearchOnly</span><span class="sxs-lookup"><span data-stu-id="bebd0-112">WebSearchOnly</span></span>

  - <span data-ttu-id="bebd0-113">FileDownloadOnly</span><span class="sxs-lookup"><span data-stu-id="bebd0-113">FileDownloadOnly</span></span>

<span data-ttu-id="bebd0-114">定義すると、クライアントがアドレス帳にどのようにアクセスするかを決定します。</span><span class="sxs-lookup"><span data-stu-id="bebd0-114">When defined, it determines how the Address Book is accessed by clients.</span></span> <span data-ttu-id="bebd0-115">このパラメーターを定義する場合は、いずれかのオプションを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bebd0-115">If you define this parameter, you must define one of the options.</span></span> <span data-ttu-id="bebd0-116">この設定を変更しない場合、既定の WebSearchAndFileDownload は有効なままになります。</span><span class="sxs-lookup"><span data-stu-id="bebd0-116">If you do not modify this setting, the default WebSearchAndFileDownload remains in effect.</span></span>

<span data-ttu-id="bebd0-117">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="bebd0-117">For example:</span></span>

    New-CsClientPolicy -Identity RedmondClientPolicy -DisableCalendarPresence $True -DisablePhonePresence $True -DisplayPhoto "PhotosFromADOnly" -AddressBookAvailability "WebSearchOnly"

<div>

## <a name="see-also"></a><span data-ttu-id="bebd0-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="bebd0-118">See Also</span></span>


[<span data-ttu-id="bebd0-119">New-CsClientPolicy</span><span class="sxs-lookup"><span data-stu-id="bebd0-119">New-CsClientPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsClientPolicy)  
  

<span data-ttu-id="bebd0-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bebd0-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

