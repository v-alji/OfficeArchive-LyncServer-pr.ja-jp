---
title: 'Lync Server 2013: アドレス帳サーバーコマンドレット'
description: 'Lync Server 2013: アドレス帳サーバーコマンドレット。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Address Book Server cmdlets
ms:assetid: 33da45da-3c57-4d04-9679-f0e5a0cfd37e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415643(v=OCS.15)
ms:contentKeyID: 48183793
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e4fef903d25f0d2707410e017f4eb280282bbdab
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439997"
---
# <a name="address-book-server-cmdlets-in-lync-server-2013"></a><span data-ttu-id="71e88-103">Lync Server 2013 のアドレス帳サーバーコマンドレット</span><span class="sxs-lookup"><span data-stu-id="71e88-103">Address Book Server cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="71e88-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="71e88-104">

<span> </span></span></span>

<span data-ttu-id="71e88-105">_**トピックの最終更新日:** 2012-06-26_</span><span class="sxs-lookup"><span data-stu-id="71e88-105">_**Topic Last Modified:** 2012-06-26_</span></span>

<span data-ttu-id="71e88-106">アドレス帳サーバーは、Active Directory ドメインサービスと Microsoft Lync Server 2013 との間で中継されています。</span><span class="sxs-lookup"><span data-stu-id="71e88-106">Address Book servers are intermediaries between Active Directory Domain Services and Microsoft Lync Server 2013.</span></span> <span data-ttu-id="71e88-107">アドレス帳サーバーによって、Lync Server 2013 に保存されているユーザー情報が Active Directory に保存されているユーザー情報と同期していることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="71e88-107">The Address Book server ensures that the user information stored in Lync Server 2013 is in synch with the user information stored in Active Directory.</span></span> <span data-ttu-id="71e88-108">これは、ユーザーデータベースに保存されている情報を使用して、定期的にアドレス帳ファイルを同期することによって行われます。</span><span class="sxs-lookup"><span data-stu-id="71e88-108">This is done by periodically synching Address Book files with information stored in the User database.</span></span> <span data-ttu-id="71e88-109">さらに、Lync Server には、アドレス帳サーバーを管理するための多数のコマンドレットが用意されています。</span><span class="sxs-lookup"><span data-stu-id="71e88-109">In turn, Lync Server includes a number of cmdlets for managing Address Book servers.</span></span>

<div>

## <a name="address-book-server-cmdlets"></a><span data-ttu-id="71e88-110">アドレス帳サーバーのコマンドレット</span><span class="sxs-lookup"><span data-stu-id="71e88-110">Address Book Server Cmdlets</span></span>

<span data-ttu-id="71e88-111">Lync Server コントロールパネルで、アドレス帳のサーバー設定を構成することはできません。</span><span class="sxs-lookup"><span data-stu-id="71e88-111">You cannot configure the Address Book Server settings in Lync Server Control Panel.</span></span> <span data-ttu-id="71e88-112">Windows PowerShell は、これらの設定を管理するための主要なツールです。</span><span class="sxs-lookup"><span data-stu-id="71e88-112">Windows PowerShell is the primary tool for managing these settings.</span></span> <span data-ttu-id="71e88-113">アドレス帳サーバーの管理に直接関連するコマンドレットの一覧を次に示します。</span><span class="sxs-lookup"><span data-stu-id="71e88-113">The following is a list of cmdlets that relate directly to managing the Address Book Server:</span></span>

<span data-ttu-id="71e88-114">**アドレス帳サーバー**</span><span class="sxs-lookup"><span data-stu-id="71e88-114">**Address Book Server**</span></span>

  - <span></span>  
    <span data-ttu-id="71e88-115">[CsAddressBookConfiguration の入手](https://technet.microsoft.com/library/Gg398132(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="71e88-115">[Get-CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg398132(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="71e88-116">[New-CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg398395(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="71e88-116">[New-CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg398395(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="71e88-117">[CsAddressBookConfiguration の削除](https://technet.microsoft.com/library/Gg398934(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="71e88-117">[Remove-CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg398934(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="71e88-118">[Set-CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg412784(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="71e88-118">[Set-CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg412784(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="71e88-119">[更新-CsAddressBook](https://technet.microsoft.com/library/Gg398194(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="71e88-119">[Update-CsAddressBook](https://technet.microsoft.com/library/Gg398194(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="71e88-120">[Debug-CsAddressBookReplication](https://technet.microsoft.com/library/JJ205232(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="71e88-120">[Debug-CsAddressBookReplication](https://technet.microsoft.com/library/JJ205232(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="71e88-121">[Test-CsAddressBookService](https://technet.microsoft.com/library/Gg398661(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="71e88-121">[Test-CsAddressBookService](https://technet.microsoft.com/library/Gg398661(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="71e88-122">[Test-CsAddressBookWebQuery](https://technet.microsoft.com/library/Gg398773(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="71e88-122">[Test-CsAddressBookWebQuery](https://technet.microsoft.com/library/Gg398773(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="71e88-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="71e88-123">See Also</span></span>


[<span data-ttu-id="71e88-124">Lync Server PowerShell ブログ</span><span class="sxs-lookup"><span data-stu-id="71e88-124">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="71e88-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="71e88-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

