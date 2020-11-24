---
title: 'Lync Server 2013: アドレス帳管理の Update-CsAddressBook'
description: 'Lync Server 2013: アドレス帳の管理に Update-CsAddressBook します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Update-CsAddressBook for Address Book management
ms:assetid: 0ffd2ef8-201c-44aa-8c64-1c7b0eaa7d48
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429695(v=OCS.15)
ms:contentKeyID: 48183428
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4adc7f94e2f31f64f6517b8cdf9bbcb0649f6c8b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399477"
---
# <a name="update-csaddressbook-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="a955b-103">Lync Server 2013 でのアドレス帳管理の Update-CsAddressBook</span><span class="sxs-lookup"><span data-stu-id="a955b-103">Update-CsAddressBook for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a955b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a955b-104">

<span> </span></span></span>

<span data-ttu-id="a955b-105">_**最終更新日:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="a955b-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="a955b-106">このコマンドレットを実行できるユーザー: 既定では、次のグループのメンバーは、Update-CsAddressBook コマンドレットをローカルで実行することを許可されています: RTCUniversalUserAdmins、RTCUniversalServerAdmins。</span><span class="sxs-lookup"><span data-stu-id="a955b-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the Update-CsAddressBook cmdlet locally: RTCUniversalUserAdmins, RTCUniversalServerAdmins.</span></span> <span data-ttu-id="a955b-107">このコマンドレットが割り当てられているすべての役割ベースのアクセス制御 (RBAC) ロールのリストを返すには (自分自身で作成したカスタム RBAC ロールを含む)、Windows PowerShell プロンプトから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="a955b-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Update-CsAddressBook"}

<span data-ttu-id="a955b-108">Update-CsAddressBook コマンドレットによって、Office Communications Server から **abserver.exe – Syncnow** コマンドが置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="a955b-108">The Update-CsAddressBook cmdlet replaces the **abserver.exe –syncNow** command from Office Communications Server.</span></span> <span data-ttu-id="a955b-109">このコマンドレットの目的は、スケジュールされた時間を待つのではなく、直ちに同期を開始することです。</span><span class="sxs-lookup"><span data-stu-id="a955b-109">The cmdlet’s purpose is to initiate a synchronization immediately rather than waiting for the scheduled time.</span></span> <span data-ttu-id="a955b-110">最初の例のコマンドは、組織内のすべてのアドレス帳を更新します。</span><span class="sxs-lookup"><span data-stu-id="a955b-110">The first example command updates all Address Books in the organization.</span></span> <span data-ttu-id="a955b-111">もう1つは、定義されたサーバーに関連付けられているアドレス帳のみを更新します。</span><span class="sxs-lookup"><span data-stu-id="a955b-111">The second updates only the Address Book associated with the defined server.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a955b-112">Lync server 2013 では、Lync Server ユーザーレプリケーターは Active Directory から変更を受け取り、構成された間隔に基づいて Lync Server ユーザーデータベースを更新します。</span><span class="sxs-lookup"><span data-stu-id="a955b-112">In Lync Server 2013, Lync Server User Replicator will pick up the changes from Active Directory and update the Lync Server user database based on a configured interval.</span></span> <span data-ttu-id="a955b-113">Lync Server ユーザーレプリケーターでは、管理者が更新プログラムを実行しなくても、変更内容が RTCab データベースにすばやく反映されます CSAddressBook。</span><span class="sxs-lookup"><span data-stu-id="a955b-113">Lync Server User Replicator will also propagate the changes to the RTCab database quickly without the administrator having to run Update-CSAddressBook.</span></span> <span data-ttu-id="a955b-114">CSAddressBook を実行するには、アドレス帳ファイルのダウンロードが有効になっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="a955b-114">Administrators will only need to run Update -CSAddressBook if the Address Book file download is enabled.</span></span>



</div>

<span data-ttu-id="a955b-115">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="a955b-115">For example:</span></span>

   ```PowerShell
    Update-CsAddressBook
   ```

   ```PowerShell
    Update-CsAddressBook -Fqdn atl-abs-001.contoso.com
   ```

<div>

## <a name="see-also"></a><span data-ttu-id="a955b-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="a955b-116">See Also</span></span>


[<span data-ttu-id="a955b-117">更新-CsAddressBook</span><span class="sxs-lookup"><span data-stu-id="a955b-117">Update-CsAddressBook</span></span>](https://docs.microsoft.com/powershell/module/skype/Update-CsAddressBook)  
  

<span data-ttu-id="a955b-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a955b-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

