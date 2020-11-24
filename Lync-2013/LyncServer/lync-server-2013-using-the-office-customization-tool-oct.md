---
title: 'Lync Server 2013: Office カスタマイズツール (OCT) を使用する'
description: 'Lync Server 2013: Office カスタマイズツール (OCT) を使用します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using the Office Customization Tool (OCT)
ms:assetid: 26647cb6-ba84-4ba7-8b6f-2cf86818e530
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204748(v=OCS.15)
ms:contentKeyID: 48183654
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 602502ba4579ed6c640eee909d4c6b056ce247d7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400119"
---
# <a name="using-the-office-customization-tool-oct-in-lync-server-2013"></a><span data-ttu-id="db019-103">Lync Server 2013 で Office カスタマイズツール (OCT) を使用する</span><span class="sxs-lookup"><span data-stu-id="db019-103">Using the Office Customization Tool (OCT) in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="db019-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="db019-104">

<span> </span></span></span>

<span data-ttu-id="db019-105">_**最終更新日:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="db019-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="db019-106">Office カスタマイズ ツール (OCT) はセットアップ プログラムの一部であり、多くのカスタマイズにおける推奨ツールになっています。</span><span class="sxs-lookup"><span data-stu-id="db019-106">The Office Customization Tool (OCT) is part of the Setup program and is the recommended tool for many customizations.</span></span> <span data-ttu-id="db019-107">OCT を使用して Office をカスタマイズし、カスタマイズ内容をセットアップ カスタマイズ (.msp) ファイルに保存します。</span><span class="sxs-lookup"><span data-stu-id="db019-107">By using the OCT, you customize Office and save your customizations in a Setup customization .msp file.</span></span> <span data-ttu-id="db019-108">そのファイルをネットワーク インストール ポイントの Updates フォルダーに配置します。</span><span class="sxs-lookup"><span data-stu-id="db019-108">You place the file in the Updates folder on the network installation point.</span></span> <span data-ttu-id="db019-109">Office をインストールするときに、セットアップは Updates フォルダーのセットアップ カスタマイズ ファイルを検索し、カスタマイズ内容を適用します。</span><span class="sxs-lookup"><span data-stu-id="db019-109">When you install Office, Setup looks for a Setup customization file in the Updates folder and applies the customizations.</span></span> <span data-ttu-id="db019-110">Updates フォルダーは、Office 2013 の最初のインストール中にソフトウェアの更新プログラムを展開するためにのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="db019-110">The Updates folder can be used only to deploy software updates during an initial installation of Office 2013.</span></span>

<span data-ttu-id="db019-111">OCT はセットアップの一部で、ボリューム ライセンス版の製品に含まれています。</span><span class="sxs-lookup"><span data-stu-id="db019-111">The OCT is part of setup and it is included in volume license versions of the product.</span></span> <span data-ttu-id="db019-112">`setup.exe /admin`Office 2013 のソースファイルが含まれているネットワークインストールポイントのルートからコマンドラインを入力して、OCT を実行します。</span><span class="sxs-lookup"><span data-stu-id="db019-112">You run the OCT by typing `setup.exe /admin` at the command line from the root of the network installation point that contains the Office 2013 source files.</span></span> <span data-ttu-id="db019-113">たとえば、次のようなコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="db019-113">For example, use the following:</span></span>

`\\server\share\Office15\setup.exe /admin`

<span data-ttu-id="db019-114">管理者は OCT を使用してセットアップ カスタマイズ (.msp) ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="db019-114">Administrators use the OCT to create a setup customization .msp file.</span></span> <span data-ttu-id="db019-115">Microsoft Office 2010 10 月の場合、管理者は次の領域をカスタマイズすることができます。</span><span class="sxs-lookup"><span data-stu-id="db019-115">As in the Microsoft Office 2010 OCT, administrators can customize the following areas:</span></span>

  - <span data-ttu-id="db019-116">**セットアップ** クライアントと既定の組織名、追加のネットワークインストールソース、プロダクトキー、エンドユーザーライセンス契約、表示レベル、以前のバージョンの Office を削除するためのカスタムプログラム、インストール時、セキュリティ設定、セットアップのプロパティなど、既定のインストール場所を指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="db019-116">**Setup** Used to specify default installation location on the client and default organization name, additional network installation sources, product key, end-user license agreement, display level, earlier versions of Office to remove, custom programs to run during installation, security settings, and Setup properties.</span></span>

  - <span data-ttu-id="db019-117">**機能** ユーザー設定を構成し、Office 機能のインストール方法をカスタマイズするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="db019-117">**Features** Used to configure user settings and to customize how Office features are installed.</span></span> <span data-ttu-id="db019-118">管理者は、OCT を使用して、ユーザーの Office アプリケーション設定の初期既定値を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="db019-118">Administrators can use the OCT to specify initial default values of Office application settings for users.</span></span> <span data-ttu-id="db019-119">ユーザーはインストール後にほとんどの設定を変更できます。</span><span class="sxs-lookup"><span data-stu-id="db019-119">Users can modify most of the settings after the installation.</span></span>

  - <span data-ttu-id="db019-120">**追加コンテンツ** ファイルを追加または削除したり、レジストリエントリを追加または削除したり、ショートカットを構成したりするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="db019-120">**Additional content** Used to add or remove files, add or remove registry entries, and configure shortcuts.</span></span>

  - <span data-ttu-id="db019-121">**Outlook** ユーザーの既定の Outlook プロファイルのカスタマイズ、Exchange 設定の指定、アカウントの追加、アカウントの削除と設定のエクスポート、送信受信グループの指定を行うために使用され \\ ます。</span><span class="sxs-lookup"><span data-stu-id="db019-121">**Outlook** Used to customize a user's default Outlook profile, specify Exchange settings, add accounts, remove accounts and export settings, and specify Send\\Receive groups.</span></span>

<span data-ttu-id="db019-122">OCT の詳細については、を参照してください <https://go.microsoft.com/fwlink/p/?linkid=267516> 。</span><span class="sxs-lookup"><span data-stu-id="db019-122">For information about the OCT, see <https://go.microsoft.com/fwlink/p/?linkid=267516>.</span></span>

<span data-ttu-id="db019-123"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="db019-123"></div>

<span> </span>

</div>

</div>

</span></span></div>

