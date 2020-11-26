---
title: 'Lync Server 2013: クライアントのインストールのカスタマイズ'
description: 'Lync Server 2013: クライアントのインストールをカスタマイズします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Customizing client installation
ms:assetid: 5c1a85f1-5ebb-48fb-acb7-3bf46decbf80
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204934(v=OCS.15)
ms:contentKeyID: 48184254
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8dd1942c298ccbc8b6a2950baf4f24cc2f797a92
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431373"
---
# <a name="customizing-client-installation-in-lync-server-2013"></a><span data-ttu-id="fc158-103">Lync Server 2013 でのクライアントインストールのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="fc158-103">Customizing client installation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fc158-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fc158-104">

<span> </span></span></span>

<span data-ttu-id="fc158-105">_**最終更新日:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="fc158-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="fc158-106">エンタープライズ管理者は、このセクションで説明する方法を使用して、Office 2013 Windows Installer ベースの (.msi) インストールをカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="fc158-106">Enterprise administrators can customize the Office 2013 Windows Installer-based (.msi) installation by using the methods discussed in this section.</span></span> <span data-ttu-id="fc158-107">1つのツールによってすべてのカスタマイズオプションが提供されるわけではないため、Lync 2013 の展開では、これらの方法を組み合わせて使用する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fc158-107">Because no single tool provides all customization options, you’ll likely use a combination of these methods in your Lync 2013 deployment.</span></span> <span data-ttu-id="fc158-108">少なくとも、次のセクションで説明するツールを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="fc158-108">At a minimum, you might use the tools described in the following sections:</span></span>

  - <span data-ttu-id="fc158-109">[Lync Server 2013 で Office カスタマイズツール (OCT) を使用して](lync-server-2013-using-the-office-customization-tool-oct.md) 、lync や他の office プログラムのセットアップオプションと機能をカスタマイズします。</span><span class="sxs-lookup"><span data-stu-id="fc158-109">[Using the Office Customization Tool (OCT) in Lync Server 2013](lync-server-2013-using-the-office-customization-tool-oct.md) to customize setup options and features for Lync and other Office programs.</span></span>

  - <span data-ttu-id="fc158-110">[Config.xml を使って Lync Server 2013 でインストールタスクを実行](lync-server-2013-using-config-xml-to-perform-installation-tasks.md) し、ネットワークインストールポイントのパスを指定し、サイレントインストールを実行します。</span><span class="sxs-lookup"><span data-stu-id="fc158-110">[Using Config.xml to perform installation tasks in Lync Server 2013](lync-server-2013-using-config-xml-to-perform-installation-tasks.md) to specify the path of the network installation point and perform silent installation.</span></span>

  - <span data-ttu-id="fc158-111">[Lync Server 2013 のセットアップコマンドラインオプションを使用して](lync-server-2013-using-setup-command-line-options.md) 、インストール時に使用する Config.xml ファイルを指定します。</span><span class="sxs-lookup"><span data-stu-id="fc158-111">[Using Setup command-line options in Lync Server 2013](lync-server-2013-using-setup-command-line-options.md) to specify the Config.xml file to use during installation.</span></span>

  - <span data-ttu-id="fc158-112">グループポリシーオブジェクトエディター MMC スナップインを使用して、 [Lync Server 2013 でクライアントブートストラップポリシーを構成](lync-server-2013-configuring-client-bootstrapping-policies.md)します。</span><span class="sxs-lookup"><span data-stu-id="fc158-112">[Configuring client bootstrapping policies in Lync Server 2013](lync-server-2013-configuring-client-bootstrapping-policies.md) by using the Group Policy Object Editor MMC snap-in.</span></span>

<span data-ttu-id="fc158-113">製品の Office スイートを展開するときに構成するオプションが他にある場合もあります。</span><span class="sxs-lookup"><span data-stu-id="fc158-113">There will probably be other options you’ll want to configure as you deploy the Office suite of products.</span></span> <span data-ttu-id="fc158-114">このセクションのトピックでは、これらのカスタマイズツールの概要と、Lync 固有の考慮事項について説明します。</span><span class="sxs-lookup"><span data-stu-id="fc158-114">The topics in this section give an overview of these customization tools and discuss Lync-specific considerations.</span></span> <span data-ttu-id="fc158-115">各ツールの詳細な Office ヘルプへのリンクもあります。</span><span class="sxs-lookup"><span data-stu-id="fc158-115">Included are links to detailed Office help for each tool.</span></span>

<span data-ttu-id="fc158-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fc158-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

