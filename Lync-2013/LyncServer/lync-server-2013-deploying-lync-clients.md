---
title: 'Lync Server 2013: Lync クライアントを展開する'
description: 'Lync Server 2013: Lync クライアントを展開しています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying Lync clients
ms:assetid: 3d10abf2-d484-4fa0-8f10-4a5f9dfba4f5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204827(v=OCS.15)
ms:contentKeyID: 48183925
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 09b501fc721ac880c5cf7da0293e3aa9c6443722
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429987"
---
# <a name="deploying-lync-clients-in-lync-server-2013"></a><span data-ttu-id="56804-103">Lync Server 2013 での Lync クライアントの展開</span><span class="sxs-lookup"><span data-stu-id="56804-103">Deploying Lync clients in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="56804-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="56804-104">

<span> </span></span></span>

<span data-ttu-id="56804-105">_**最終更新日:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="56804-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="56804-106">Lync 2013 では、クライアントの展開にさまざまなアプローチが導入されています。</span><span class="sxs-lookup"><span data-stu-id="56804-106">Lync 2013 introduces a different approach to client deployment.</span></span> <span data-ttu-id="56804-107">以前のリリースから出発した Lync 2013 には、独自のインストーラーがありません。</span><span class="sxs-lookup"><span data-stu-id="56804-107">In a departure from previous releases, Lync 2013 no longer has its own installer.</span></span> <span data-ttu-id="56804-108">代わりに Lync は、Office 2013 セットアッププログラムに含まれています。</span><span class="sxs-lookup"><span data-stu-id="56804-108">Instead, Lync is included with the Office 2013 setup program.</span></span> <span data-ttu-id="56804-109">Lync 2013 をユーザーに展開するには、Office 2013 のインストール方法とカスタマイズツールを使用できます。</span><span class="sxs-lookup"><span data-stu-id="56804-109">To deploy Lync 2013 to your users, you can use Office 2013 installation methods and customization tools.</span></span>

  - <span data-ttu-id="56804-110">**Office 2013 Windows installer** は、複数の MSI ファイルで構成される windows installer ベースのインストールパッケージです。</span><span class="sxs-lookup"><span data-stu-id="56804-110">**Office 2013 Windows Installer** is a Windows Installer-based installation package that consists of multiple MSI files.</span></span> <span data-ttu-id="56804-111">言語に依存しないコア MSI パッケージと 1 つ以上の言語固有のパッケージが組み合わされ 1 つの完全な製品になっています。</span><span class="sxs-lookup"><span data-stu-id="56804-111">A language-neutral core MSI package is combined with one or more language-specific packages to make a complete product.</span></span> <span data-ttu-id="56804-112">セットアップによって個々のパッケージがアセンブルされ、ユーザーのコンピューターへの Office のインストール中およびインストール後に、カスタマイズ タスクとメンテナンス タスクが実行されます。</span><span class="sxs-lookup"><span data-stu-id="56804-112">Setup assembles the individual packages and performs customization and maintenance tasks during and after installation of Office on users' computers.</span></span> <span data-ttu-id="56804-113">このセクションのトピックでは、Lync 2013 を展開するために Office 2013 Windows インストーラーを使用およびカスタマイズする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="56804-113">The topics in this section describe how to use and customize the Office 2013 Windows Installer to deploy Lync 2013.</span></span>

  - <span data-ttu-id="56804-114">**Office 2013 クイック実行** は、Microsoft 365 管理センターからユーザーに office セットアップファイルを転送するインストールプログラムです。</span><span class="sxs-lookup"><span data-stu-id="56804-114">**Office 2013 Click-to-Run** is an installation program that streams Office setup files to the user from the Microsoft 365 admin center.</span></span> <span data-ttu-id="56804-115">管理者は、Office 展開ツールを使用してクイック実行用にインストールをカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="56804-115">Administrators can customize installation by using the Office Deployment Tool for Click-to-Run.</span></span> <span data-ttu-id="56804-116">Office 2013 クイック実行は主に Microsoft 365 環境で使用されるため、このインストール方法については、このセクションで詳しく説明されていません。</span><span class="sxs-lookup"><span data-stu-id="56804-116">Because Office 2013 Click-to-Run is primarily used in the Microsoft 365 environment, this installation method is not described in detail in this section.</span></span> <span data-ttu-id="56804-117">クイック実行インストールの使用とカスタマイズの詳細については、「Office 2013 リソースキット」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="56804-117">Detailed information about using and customizing Click-to-Run installation is available in the Office 2013 Resource Kit documentation.</span></span> <span data-ttu-id="56804-118">管理者は、Office 2013 クイック実行プログラムと言語ソースファイルをオンプレミスの場所にダウンロードすることもできます。これは、企業のセキュリティ要件により、ネットワーク上の需要を最小限にしたり、ユーザーがインターネットからソフトウェアをインストールしたりできないようにする場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="56804-118">Administrators can also download the Office 2013 Click-to-Run program and language source files to an on-premises location, which is useful when you want to minimize the demand on the network or prevent users from installing software from the Internet because of corporate security requirements.</span></span>

<span data-ttu-id="56804-119">このセクションのトピックでは、Office 2013 MSI ベースのインストーラーを使用してクライアントを展開する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="56804-119">The topics in this section focus on how to deploy clients by using the Office 2013 MSI-based installer.</span></span> <span data-ttu-id="56804-120">主な参照は、Office 2013 リソースキットドキュメントです。ここでは、インフラストラクチャの準備、セットアップのカスタマイズ、Office 2013 の展開の方法について詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="56804-120">Your primary reference should be the Office 2013 Resource Kit documentation, which describes in detail how to prepare your infrastructure, customize setup, and deploy Office 2013.</span></span> <span data-ttu-id="56804-121">ただし、Office ドキュメントをこのセクションのトピックと組み合わせて使用する必要があります。このセクションでは、Lync 2013 に固有の展開に関する考慮事項について説明します。</span><span class="sxs-lookup"><span data-stu-id="56804-121">However, you should use the Office documentation in conjunction with topics in this section, which point out deployment considerations that are specific to Lync 2013.</span></span>

<div>


> [!NOTE]  
> <UL>
> <LI>
> <P><span data-ttu-id="56804-122">Lync 2013 用のオンライン会議アドインは、Outlook メッセージングおよびコラボレーションクライアント内からの会議管理をサポートしており、Lync 2013 と共に自動的にインストールされます。</span><span class="sxs-lookup"><span data-stu-id="56804-122">The Online Meeting Add-in for Lync 2013, which supports meeting management from within the Outlook messaging and collaboration client, installs automatically with Lync 2013.</span></span></P>
> <LI>
> <P><span data-ttu-id="56804-123">Office 2013 セットアッププログラムでは、以前のバージョンの Lync や Office Communicator はアンインストールされません。</span><span class="sxs-lookup"><span data-stu-id="56804-123">The Office 2013 setup program does not uninstall previous versions of Lync or Office Communicator.</span></span> <span data-ttu-id="56804-124">Lync 2013 クライアントは、他の Lync または Office Communicator クライアントと並行してインストールされます。</span><span class="sxs-lookup"><span data-stu-id="56804-124">The Lync 2013 client installs side-by-side with other Lync or Office Communicator clients</span></span></P></LI></UL>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="56804-125">このセクション中</span><span class="sxs-lookup"><span data-stu-id="56804-125">In This Section</span></span>

  - [<span data-ttu-id="56804-126">Lync Server 2013 でのクライアントインストールのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="56804-126">Customizing client installation in Lync Server 2013</span></span>](lync-server-2013-customizing-client-installation.md)

  - [<span data-ttu-id="56804-127">Lync Server 2013 での Lync の動作とユーザーインターフェイスのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="56804-127">Customizing Lync behavior and the user interface in Lync Server 2013</span></span>](lync-server-2013-customizing-lync-behavior-and-the-user-interface.md)

  - [<span data-ttu-id="56804-128">Lync Server 2013 でのオンライン会議アドインのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="56804-128">Customizing the Online Meeting Add-in in Lync Server 2013</span></span>](lync-server-2013-customizing-the-online-meeting-add-in.md)

  - [<span data-ttu-id="56804-129">Lync Server 2013 での会議参加ページの構成</span><span class="sxs-lookup"><span data-stu-id="56804-129">Configuring the meeting join page in Lync Server 2013</span></span>](lync-server-2013-configuring-the-meeting-join-page.md)

  - [<span data-ttu-id="56804-130">Lync Server 2013 でサポートされているクライアントバージョンを構成する</span><span class="sxs-lookup"><span data-stu-id="56804-130">Configuring supported client versions in Lync Server 2013</span></span>](lync-server-2013-configuring-supported-client-versions.md)

  - [<span data-ttu-id="56804-131">Lync Server 2013 で拡張プレゼンスプライバシーモードを構成する</span><span class="sxs-lookup"><span data-stu-id="56804-131">Configuring enhanced presence privacy mode in Lync Server 2013</span></span>](lync-server-2013-configuring-enhanced-presence-privacy-mode.md)

<span data-ttu-id="56804-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="56804-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

