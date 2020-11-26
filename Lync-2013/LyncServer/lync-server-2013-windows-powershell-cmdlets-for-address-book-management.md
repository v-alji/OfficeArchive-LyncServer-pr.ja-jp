---
title: 'Lync Server 2013: アドレス帳管理のための Windows PowerShell コマンドレット'
description: 'Lync Server 2013: アドレス帳管理のための Windows PowerShell コマンドレット。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Windows PowerShell cmdlets for Address Book management
ms:assetid: 73bfa949-5628-4156-ad20-fe07a0dc6216
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429708(v=OCS.15)
ms:contentKeyID: 48184512
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b598d91a4d1a29a67d8f8ceb2477f2d9b96f1319
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446178"
---
# <a name="windows-powershell-cmdlets-for-address-book-services-in-lync-server-2013"></a><span data-ttu-id="37eb3-103">Lync Server 2013 のアドレス帳サービス用の Windows PowerShell コマンドレット</span><span class="sxs-lookup"><span data-stu-id="37eb3-103">Windows PowerShell cmdlets for Address Book Services in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="37eb3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="37eb3-104">

<span> </span></span></span>

<span data-ttu-id="37eb3-105">_**最終更新日:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="37eb3-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="37eb3-106">Lync Server には、アドレス帳サービスを管理して構成するための Windows PowerShell コマンドラインインターフェイスコマンドレットが数多く用意されています。</span><span class="sxs-lookup"><span data-stu-id="37eb3-106">Lync Server provides a number of Windows PowerShell command-line interface cmdlets to manage and configure the Address Book service.</span></span> <span data-ttu-id="37eb3-107">これらのコマンドレットの一部は、以前のバージョンの Office Communications Server で使用されていた ABServer.exe コマンドの代わりとなります。</span><span class="sxs-lookup"><span data-stu-id="37eb3-107">Some of these cmdlets are replacements for the ABServer.exe commands used in previous versions of Office Communications Server.</span></span> <span data-ttu-id="37eb3-108">次のトピックでは、アドレス帳サービスに関する情報の設定、作成、取得、アドレス帳サービスがアドレス帳サービスのファイルと設定を取得するときに使用する Web サービスに関する情報の設定、作成、取得に使用するコマンドレットについて説明します。</span><span class="sxs-lookup"><span data-stu-id="37eb3-108">In the following topics are the cmdlets that are used to set, create, and retrieve information about the Address Book service, its configuration and information about the Web services that the Address Book service uses when clients retrieve Address Book service files and settings.</span></span>

<span data-ttu-id="37eb3-109">これらのすべてのコマンドレットは、管理ツールがインストールされているサーバーまたはワークステーションの Lync Server ツールの lync server 管理シェルを通じて発行されます。</span><span class="sxs-lookup"><span data-stu-id="37eb3-109">All of these cmdlets are issued through the Lync Server Management Shell found in the Lync Server tools on a server or workstation where the administration tools have been installed.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="37eb3-110">このセクション中</span><span class="sxs-lookup"><span data-stu-id="37eb3-110">In This Section</span></span>

  - [<span data-ttu-id="37eb3-111">Lync Server 2013 でのアドレス帳管理用の新しい CsAddressBookConfiguration</span><span class="sxs-lookup"><span data-stu-id="37eb3-111">New-CsAddressBookConfiguration for Address Book management in Lync Server 2013</span></span>](lync-server-2013-New-CsAddressBookConfiguration-for-address-book-management.md)

  - [<span data-ttu-id="37eb3-112">Lync Server 2013 でのアドレス帳管理用の設定-CsAddressBookConfiguration</span><span class="sxs-lookup"><span data-stu-id="37eb3-112">Set-CsAddressBookConfiguration for Address Book management in Lync Server 2013</span></span>](lync-server-2013-set-csaddressbookconfiguration-for-address-book-management.md)

  - [<span data-ttu-id="37eb3-113">Lync Server 2013 でのアドレス帳管理のための設定を取得する</span><span class="sxs-lookup"><span data-stu-id="37eb3-113">Get-CsAddressBookConfiguration for Address Book management in Lync Server 2013</span></span>](lync-server-2013-get-csaddressbookconfiguration-for-address-book-management.md)

  - [<span data-ttu-id="37eb3-114">Lync Server 2013 でのアドレス帳管理用の削除-CsAddressBookConfiguration</span><span class="sxs-lookup"><span data-stu-id="37eb3-114">Remove-CsAddressBookConfiguration for Address Book management in Lync Server 2013</span></span>](lync-server-2013-remove-csaddressbookconfiguration-for-address-book-management.md)

  - [<span data-ttu-id="37eb3-115">Lync Server 2013 でのアドレス帳管理用のテスト-CsAddressBookService</span><span class="sxs-lookup"><span data-stu-id="37eb3-115">Test-CsAddressBookService for Address Book management in Lync Server 2013</span></span>](lync-server-2013-test-csaddressbookservice-for-address-book-management.md)

  - [<span data-ttu-id="37eb3-116">Lync Server 2013 でのアドレス帳の管理に関するテスト-CsAddressBookWebQuery</span><span class="sxs-lookup"><span data-stu-id="37eb3-116">Test-CsAddressBookWebQuery for Address Book management in Lync Server 2013</span></span>](lync-server-2013-test-csaddressbookwebquery-for-address-book-management.md)

  - [<span data-ttu-id="37eb3-117">Lync Server 2013 でのアドレス帳管理の更新プログラム-CsAddressBook</span><span class="sxs-lookup"><span data-stu-id="37eb3-117">Update-CsAddressBook for Address Book management in Lync Server 2013</span></span>](lync-server-2013-update-csaddressbook-for-address-book-management.md)

  - [<span data-ttu-id="37eb3-118">Lync Server 2013 でのアドレス帳管理用の新しい CsClientPolicy</span><span class="sxs-lookup"><span data-stu-id="37eb3-118">New-CsClientPolicy for Address Book management in Lync Server 2013</span></span>](lync-server-2013-new-csclientpolicy-for-address-book-management.md)

  - [<span data-ttu-id="37eb3-119">Lync Server 2013 でのアドレス帳管理のための CsClientPolicy の設定</span><span class="sxs-lookup"><span data-stu-id="37eb3-119">Set-CsClientPolicy for Address Book management in Lync Server 2013</span></span>](lync-server-2013-set-csclientpolicy-for-address-book-management.md)

  - [<span data-ttu-id="37eb3-120">Lync Server 2013 でのアドレス帳管理のための CsService</span><span class="sxs-lookup"><span data-stu-id="37eb3-120">Get-CsService for Address Book management in Lync Server 2013</span></span>](lync-server-2013-get-csservice-for-address-book-management.md)

  - [<span data-ttu-id="37eb3-121">Lync Server 2013 でのアドレス帳管理のための CsWebServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="37eb3-121">New-CsWebServiceConfiguration for Address Book management in Lync Server 2013</span></span>](lync-server-2013-New-CsWebServiceConfiguration-for-address-book-management.md)

  - [<span data-ttu-id="37eb3-122">Lync Server 2013 でのアドレス帳管理の CsWebServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="37eb3-122">Get-CsWebServiceConfiguration for Address Book management in Lync Server 2013</span></span>](lync-server-2013-get-cswebserviceconfiguration-for-address-book-management.md)

  - [<span data-ttu-id="37eb3-123">Lync Server 2013 でのアドレス帳管理用に CsWebServiceConfiguration を設定する</span><span class="sxs-lookup"><span data-stu-id="37eb3-123">Set-CsWebServiceConfiguration for Address Book management in Lync Server 2013</span></span>](lync-server-2013-set-cswebserviceconfiguration-for-address-book-management.md)

  - [<span data-ttu-id="37eb3-124">Lync Server 2013 でのアドレス帳管理用の CsWebServiceConfiguration の削除</span><span class="sxs-lookup"><span data-stu-id="37eb3-124">Remove-CsWebServiceConfiguration for Address Book management in Lync Server 2013</span></span>](lync-server-2013-remove-cswebserviceconfiguration-for-address-book-management.md)

</div>

<div>

## <a name="related-sections"></a><span data-ttu-id="37eb3-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="37eb3-125">Related Sections</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="37eb3-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="37eb3-126">See Also</span></span>


[https://go.microsoft.com/fwlink/p/?linkId=205826](https://go.microsoft.com/fwlink/p/?linkid=205826)  
  

<span data-ttu-id="37eb3-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="37eb3-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

