---
title: 'Lync Server 2013: Standard Edition サーバー データベースのインストール'
description: 'Lync Server 2013: Standard Edition Server データベースをインストールします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Install Standard Edition server database
ms:assetid: 0bd3a804-aad6-48cb-981b-54725af032db
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398167(v=OCS.15)
ms:contentKeyID: 48183385
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0a20d2c01de94ad88960555db78c57c6b79d92f7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427153"
---
# <a name="install-standard-edition-server-database-for-lync-server-2013"></a><span data-ttu-id="33d06-103">Lync Server 2013 の Standard Edition サーバー データベースのインストール</span><span class="sxs-lookup"><span data-stu-id="33d06-103">Install Standard Edition server database for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="33d06-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="33d06-104">

<span> </span></span></span>

<span data-ttu-id="33d06-105">_**最終更新日:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="33d06-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="33d06-106">インフラストラクチャ内で、標準エディションのサーバーをインフラストラクチャ内の唯一のサーバーとして設定します。これは、 **展開ウィザード** で最初のサーバーを設定することを目的としています。</span><span class="sxs-lookup"><span data-stu-id="33d06-106">Setting up a Standard Edition server as the only server in your infrastructure that homes users differs from other server installations in that there is a selection in the **Deployment Wizard** specifically for setting up the initial server.</span></span>

<div>

## <a name="to-install-a-standard-edition-server"></a><span data-ttu-id="33d06-107">Standard Edition サーバーをインストールするには</span><span class="sxs-lookup"><span data-stu-id="33d06-107">To install a Standard Edition server</span></span>

1.  <span data-ttu-id="33d06-108">Standard Edition server をインストールしようとしているサーバーに、ローカル管理者または同等のドメインとしてログオンします。</span><span class="sxs-lookup"><span data-stu-id="33d06-108">Log on to the server where you are going to install Standard Edition server as a local administrator or a domain equivalent.</span></span>

2.  <span data-ttu-id="33d06-109">Active Directory ドメインサービスの準備ができていない場合は、最初にこれらの手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="33d06-109">If you have not prepared Active Directory Domain Services, then first perform those procedures.</span></span> <span data-ttu-id="33d06-110">詳細については、「 [Lync Server 2013 用の Active Directory ドメインサービスの準備](lync-server-2013-preparing-active-directory-domain-services.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="33d06-110">For details, see [Preparing Active Directory Domain Services for Lync Server 2013](lync-server-2013-preparing-active-directory-domain-services.md).</span></span>

3.  <span data-ttu-id="33d06-111">Lync Server 展開ウィザードで、[ **最初の Standard Edition サーバーの準備**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33d06-111">In the Lync Server Deployment Wizard, click **Prepare first Standard Edition server**.</span></span>

4.  <span data-ttu-id="33d06-112">[ **単一標準エディションサーバーの準備** ] ページで、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33d06-112">On the **Prepare single Standard Edition Server** page, click **Next**.</span></span>

5.  <span data-ttu-id="33d06-113">[ **コマンドの実行** ] ページで、SQL Server 2012 Express が中央管理ストアとしてインストールされています。</span><span class="sxs-lookup"><span data-stu-id="33d06-113">On the **Executing Commands** page, the SQL Server 2012 Express is installed as the Central Management store.</span></span> <span data-ttu-id="33d06-114">必要なファイアウォールルールが作成されます。</span><span class="sxs-lookup"><span data-stu-id="33d06-114">Necessary firewall rules are created.</span></span> <span data-ttu-id="33d06-115">データベースと必須ソフトウェアのインストールが完了したら、[ **完了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33d06-115">When the installation of the database and prerequisite software is completed, click **Finish**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="33d06-116">最初のインストールでは、コマンド出力の概要画面に表示される更新プログラムがないと、時間がかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="33d06-116">The initial installation may take some time with no visible updates to the command output summary screen.</span></span> <span data-ttu-id="33d06-117">これは、SQL Server Express がインストールされているためです。</span><span class="sxs-lookup"><span data-stu-id="33d06-117">This is due to the installation of the SQL Server Express.</span></span> <span data-ttu-id="33d06-118">データベースのインストールを監視する必要がある場合は、タスクマネージャーを使用してセットアップを監視します。</span><span class="sxs-lookup"><span data-stu-id="33d06-118">If you need to monitor the installation of the database, use Task Manager to monitor the setup.</span></span>

    
    </div>

6.  <span data-ttu-id="33d06-119">[Lync Server 展開ウィザード] ページで、[管理ツール] をまだインストールしていない場合は、[ **トポロジビルダーのインストール** ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33d06-119">On the Lync Server Deployment Wizard page, click **Install Topology Builder** if you have not previously installed the administrative tools.</span></span> <span data-ttu-id="33d06-120">詳細については、「 [Lync Server 2013 管理ツールをインストール](lync-server-2013-install-lync-server-administrative-tools.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="33d06-120">For details, see [Install Lync Server 2013 administrative tools](lync-server-2013-install-lync-server-administrative-tools.md).</span></span>

7.  <span data-ttu-id="33d06-121">[Active Directory の準備] の横に緑色のチェックマークが表示されていることを確認します。 "最初の Standard Edition サーバーの準備" と "トポロジビルダーのインストール" を確認してください。</span><span class="sxs-lookup"><span data-stu-id="33d06-121">Confirm that there are green check marks next to “Prepare Active Directory,” “Prepare first Standard Edition server,” and “Install Topology Builder.”</span></span>

<span data-ttu-id="33d06-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="33d06-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

