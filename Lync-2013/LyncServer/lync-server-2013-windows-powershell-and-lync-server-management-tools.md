---
title: 'Lync Server 2013: Windows PowerShell と Lync Server の管理ツール'
description: 'Lync Server 2013: Windows PowerShell および Lync Server 管理ツール。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Windows PowerShell and Lync Server 2013 management tools
ms:assetid: 6a285f7c-0ef5-4cab-9976-d03be276e35d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn481130(v=OCS.15)
ms:contentKeyID: 59893869
ms.date: 07/20/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 11c8d63974ad05a041eb446182cbc7f9336044b9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398901"
---
# <a name="windows-powershell-and-lync-server-2013-management-tools"></a><span data-ttu-id="aae14-103">Windows PowerShell と Lync Server 2013 の管理ツール</span><span class="sxs-lookup"><span data-stu-id="aae14-103">Windows PowerShell and Lync Server 2013 management tools</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="aae14-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="aae14-104">

<span> </span></span></span>

<span data-ttu-id="aae14-105">_**最終更新日:** 2016-07-20_</span><span class="sxs-lookup"><span data-stu-id="aae14-105">_**Topic Last Modified:** 2016-07-20_</span></span>

<span data-ttu-id="aae14-106">Microsoft Lync Server 2013 では、管理ツールは Windows PowerShell を使って実装されています。</span><span class="sxs-lookup"><span data-stu-id="aae14-106">In Microsoft Lync Server 2013, management tools are implemented using Windows PowerShell.</span></span> <span data-ttu-id="aae14-107">Windows PowerShell には、コマンドライン環境、製品固有のコマンド、完全なスクリプト言語が含まれています。</span><span class="sxs-lookup"><span data-stu-id="aae14-107">Windows PowerShell includes a command-line environment, product-specific commands, and a full scripting language.</span></span> <span data-ttu-id="aae14-108">Windows PowerShell を使用して実装されている Lync Server 2013 ツールには、次のようなものがあります。</span><span class="sxs-lookup"><span data-stu-id="aae14-108">Lync Server 2013 tools that are implemented using Windows PowerShell include the following:</span></span>

  - <span data-ttu-id="aae14-109">**トポロジビルダー**。</span><span class="sxs-lookup"><span data-stu-id="aae14-109">**Topology Builder**.</span></span> <span data-ttu-id="aae14-110">トポロジビルダーを使用して、計画されたトポロジを作成、調整、および公開し、サーバーのインストールを開始する前にトポロジを検証します。</span><span class="sxs-lookup"><span data-stu-id="aae14-110">You use Topology Builder to create, adjust, and publish your planned topology, and it validates your topology before you begin server installations.</span></span> <span data-ttu-id="aae14-111">個々のサーバーに Lync Server 2013 をインストールすると、サーバーはインストールプロセスの一環として公開されたトポロジを読み取り、インストールプログラムはトポロジで指示されたとおりにサーバーを展開します。</span><span class="sxs-lookup"><span data-stu-id="aae14-111">When you install Lync Server 2013 on individual servers, the servers read the published topology as part of the installation process, and the installation program deploys the server as directed in the topology.</span></span> <span data-ttu-id="aae14-112">After setup, configuration information is automatically replicated to all servers.</span><span class="sxs-lookup"><span data-stu-id="aae14-112">After setup, configuration information is automatically replicated to all servers.</span></span> <span data-ttu-id="aae14-113">Components can be added to your deployment only by using Topology Builder.</span><span class="sxs-lookup"><span data-stu-id="aae14-113">Components can be added to your deployment only by using Topology Builder.</span></span>

  - <span data-ttu-id="aae14-114">**Lync Server 管理シェル**。</span><span class="sxs-lookup"><span data-stu-id="aae14-114">**Lync Server Management Shell**.</span></span> <span data-ttu-id="aae14-115">Lync Server 管理シェルを使用すると、展開の完全なコマンドライン管理を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="aae14-115">You can use Lync Server Management Shell for full command-line management of your deployment.</span></span>

  - <span data-ttu-id="aae14-116">**Lync Server コントロールパネル**。</span><span class="sxs-lookup"><span data-stu-id="aae14-116">**Lync Server Control Panel**.</span></span> <span data-ttu-id="aae14-117">Microsoft Lync Server 2013 コントロールパネルのユーザーインターフェイスを使用して、展開で最も一般的なタスクを管理することができます。</span><span class="sxs-lookup"><span data-stu-id="aae14-117">You can use the Microsoft Lync Server 2013 Control Panel user interface to manage the most common tasks in your deployment.</span></span>

<span data-ttu-id="aae14-118">これらのツールは、550製品固有のコマンドレットを閉じるなど、展開を管理するための Windows PowerShell コマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="aae14-118">These tools use Windows PowerShell cmdlets for management of your deployment, including close to 550 product-specific cmdlets.</span></span> <span data-ttu-id="aae14-119">Lync Server 2013 に含まれているセキュリティコマンドレットは、主に認証、ユーザー権利、アクセス許可を管理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="aae14-119">The security cmdlets included in Lync Server 2013 are primarily used to manage authentication, and user rights and permissions.</span></span> <span data-ttu-id="aae14-120">認証の管理には、さまざまなコマンドレット (証明書と暗証番号 (PIN) の認証用のコマンドレットなど) を使用できます。</span><span class="sxs-lookup"><span data-stu-id="aae14-120">A wide variety of cmdlets are available for managing authentication, including cmdlets for certificate and personal identification number (PIN) authentication.</span></span> <span data-ttu-id="aae14-121">さらに、いくつかのコマンドレットを使用して、新しい Role-Based アクセス制御 (RBAC) 機能を使用して、Lync Server 2013 の管理制御を委任することができます。</span><span class="sxs-lookup"><span data-stu-id="aae14-121">In addition, a number of cmdlets enable you to use the new Role-Based Access Control (RBAC) feature to delegate administrative control of Lync Server 2013.</span></span> <span data-ttu-id="aae14-122">Lync Server のコマンドレットの詳細については、「 [Lync server 2013 管理シェル](lync-server-2013-lync-server-management-shell.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aae14-122">For details about the Lync Server cmdlets, see [Lync Server 2013 Management Shell](lync-server-2013-lync-server-management-shell.md).</span></span>

<span data-ttu-id="aae14-123">Windows PowerShell のスクリプト セキュリティ機能は、Microsoft Visual Basic Scripting Edition (VBScript) など、古いテクノロジにおけるスクリプト関連のいくつかのセキュリティ問題を回避するように特別に設計されています。</span><span class="sxs-lookup"><span data-stu-id="aae14-123">The script security features for Windows PowerShell are specifically designed to help prevent some of the scripting-related security problems of older technologies, including Microsoft Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="aae14-124">Windows PowerShell のセキュリティ機能は、ユーザーが簡単にスクリプトを実行することができない環境を作成することを目的としています。</span><span class="sxs-lookup"><span data-stu-id="aae14-124">The Windows PowerShell security features are intended to create an environment in which users cannot easily or unknowingly run scripts.</span></span> <span data-ttu-id="aae14-125">既定では、Windows PowerShell のセキュリティ機能は有効になっています。</span><span class="sxs-lookup"><span data-stu-id="aae14-125">By default, Windows PowerShell security features are enabled.</span></span> <span data-ttu-id="aae14-126">これらの機能の状態は、スクリプトに関するニーズと多様なセキュリティの目標に応じて変更できます。</span><span class="sxs-lookup"><span data-stu-id="aae14-126">You can modify the state of those features to accommodate your scripting needs and a variety of security goals.</span></span> <span data-ttu-id="aae14-127">シェルによってユーザーがスクリプトを実行できないようにするというわけではありません。</span><span class="sxs-lookup"><span data-stu-id="aae14-127">This is not to say that the shell makes it impossible for users to run scripts.</span></span> <span data-ttu-id="aae14-128">あくまでも、ユーザー自身がスクリプトを実行しているという認識を持たずにスクリプトを実行することを、既定で困難にするということです。</span><span class="sxs-lookup"><span data-stu-id="aae14-128">Rather, the shell makes it difficult—by default—for users to run scripts without realizing they are doing so.</span></span> <span data-ttu-id="aae14-129">詳細については、「Windows PowerShell スクリプトのセキュリティ」を参照してください [https://go.microsoft.com/fwlink/p/?LinkId=213145](https://go.microsoft.com/fwlink/p/?linkid=213145) 。</span><span class="sxs-lookup"><span data-stu-id="aae14-129">For details, see Windows PowerShell Script Security at [https://go.microsoft.com/fwlink/p/?LinkId=213145](https://go.microsoft.com/fwlink/p/?linkid=213145).</span></span>

<span data-ttu-id="aae14-130"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="aae14-130"></div>

<span> </span>

</div>

</div>

</span></span></div>

