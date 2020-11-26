---
title: 'Lync Server 2013: アドレス帳管理の New-CsAddressBookConfiguration'
description: 'Lync Server 2013: アドレス帳の管理に New-CsAddressBookConfiguration します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New-CsAddressBookConfiguration for Address Book management
ms:assetid: a58ddc8c-ae04-4141-b69e-e45374a67d72
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429718(v=OCS.15)
ms:contentKeyID: 48184985
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c85d85fefe701456ad253f1afc69b73093b30996
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445450"
---
# <a name="new-csaddressbookconfiguration-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="335d1-103">Lync Server 2013 でのアドレス帳管理の New-CsAddressBookConfiguration</span><span class="sxs-lookup"><span data-stu-id="335d1-103">New-CsAddressBookConfiguration for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="335d1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="335d1-104">

<span> </span></span></span>

<span data-ttu-id="335d1-105">_**最終更新日:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="335d1-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="335d1-106">このコマンドレットを実行できるユーザー: 既定では、次のグループのメンバーは、RTCUniversalServerAdmins コマンドレットをローカルで New-CsAddressBookConfiguration 実行することを許可されています。</span><span class="sxs-lookup"><span data-stu-id="335d1-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the New-CsAddressBookConfiguration cmdlet locally: RTCUniversalServerAdmins.</span></span> <span data-ttu-id="335d1-107">このコマンドレットが割り当てられているすべての役割ベースのアクセス制御 (RBAC) ロールのリストを返すには (自分自身で作成したカスタム RBAC ロールを含む)、Windows PowerShell プロンプトから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="335d1-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "New-CsAddressBookConfiguration"}

<span data-ttu-id="335d1-108">New-CsAddressBookConfiguration コマンドレットは、アドレス帳の動作を管理するための新しい構成を作成します。</span><span class="sxs-lookup"><span data-stu-id="335d1-108">The New-CsAddressBookConfiguration cmdlet creates a new configuration to manage the behavior of the Address book.</span></span> <span data-ttu-id="335d1-109">このコマンドレットに固有の機能は、アドレス帳サービスがクライアントのダウンロードファイルを作成するかどうか、正規化ルールを使用するかどうか、差分ファイルの作成と圧縮された差分ファイルの保持期間、完全なファイルアドレス帳の作成日、ユーザーデータベース内の情報の同期のために内部で使用するものを定義することです。</span><span class="sxs-lookup"><span data-stu-id="335d1-109">Specific to this cmdlet is the ability to define if the Address Book Service creates the client download files, how and if normalization rules are used, how long to retain delta and compact delta files, delta file size before incorporating a new full file creation, what time of day the full file Address Book is created, and what the internal should be for synchronization of information in the User database.</span></span>

<span data-ttu-id="335d1-110">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="335d1-110">For example:</span></span>

    New-CsAddressBookConfiguration -Identity site:Redmond -KeepDuration 15 -SynchronizePollingInterval 00:10:00

<div>

## <a name="see-also"></a><span data-ttu-id="335d1-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="335d1-111">See Also</span></span>


[<span data-ttu-id="335d1-112">New-CsAddressBookConfiguration</span><span class="sxs-lookup"><span data-stu-id="335d1-112">New-CsAddressBookConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsAddressBookConfiguration)  
  

<span data-ttu-id="335d1-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="335d1-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

