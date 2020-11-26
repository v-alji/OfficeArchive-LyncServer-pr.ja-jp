---
title: オペレーティング システムと必要なソフトウェアのサーバーへのインストール
description: サーバーにオペレーティングシステムと必須ソフトウェアをインストールします。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Install operating systems and prerequisite software on servers
ms:assetid: 055991e0-5aeb-43fc-a7ba-d4b02316d73b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398103(v=OCS.15)
ms:contentKeyID: 48183288
ms.date: 07/24/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2bae9e57db9c2f1d3f3bde7ce9cc7071b73aa01d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427174"
---
# <a name="install-operating-systems-and-prerequisite-software-on-servers-for-lync-server-2013"></a><span data-ttu-id="904db-103">Lync Server 2013 のオペレーティング システムと必要なソフトウェアのサーバーへのインストール</span><span class="sxs-lookup"><span data-stu-id="904db-103">Install operating systems and prerequisite software on servers for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="904db-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="904db-104">

<span> </span></span></span>

<span data-ttu-id="904db-105">_**最終更新日:** 2014-07-24_</span><span class="sxs-lookup"><span data-stu-id="904db-105">_**Topic Last Modified:** 2014-07-24_</span></span>

<span data-ttu-id="904db-106">ハードウェアとシステムインフラストラクチャをセットアップした後は、展開する各サーバー上の他のすべての必須ソフトウェアに加えて、適切な Windows オペレーティングシステムと更新プログラムをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="904db-106">After you have set up the hardware and system infrastructure, you need to install the appropriate Windows operating systems and updates, in addition to all other prerequisite software on each server that you are deploying.</span></span> <span data-ttu-id="904db-107">これには、各 Lync Server 2013 サーバーの役割と、展開に必要な SQL Server が実行されているその他のインフラストラクチャサーバーまたはサーバーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="904db-107">This includes each Lync Server 2013 server role and any additional infrastructure servers or servers running SQL Server that are required for your deployment.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="904db-108">このセクションでは、内部サーバーのオペレーティングシステムと必須ソフトウェアのインストールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="904db-108">This section describes installation of operating systems and prerequisite software for internal servers.</span></span> <span data-ttu-id="904db-109">エッジサーバーを展開して外部ユーザーのアクセスをサポートする場合は、エッジサーバーやリバースプロキシサーバーなど、それらのサーバーのオペレーティングシステムと必須ソフトウェアをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="904db-109">If you are deploying Edge Servers to support external user access, you also need to install operating systems and prerequisite software for those servers, including Edge Servers and reverse proxy servers.</span></span> <span data-ttu-id="904db-110">外部ユーザーアクセスをサポートするようにサーバーを準備する方法について詳しくは、「展開ドキュメントの「 <A href="lync-server-2013-preparing-for-installation-of-servers-in-the-perimeter-network.md">境界ネットワークでの Lync Server 2013 の境界ネットワークでのサーバーインストールの準備</A> 」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="904db-110">For details about preparing servers to support external user access, see <A href="lync-server-2013-preparing-for-installation-of-servers-in-the-perimeter-network.md">Preparing for installation of servers in the perimeter network for Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="install-windows-operating-systems-on-servers"></a><span data-ttu-id="904db-111">Windows オペレーティングシステムをサーバーにインストールする</span><span class="sxs-lookup"><span data-stu-id="904db-111">Install Windows Operating Systems on Servers</span></span>

<span data-ttu-id="904db-112">展開する各サーバーで、次のように適切な Windows オペレーティングシステムをインストールします。</span><span class="sxs-lookup"><span data-stu-id="904db-112">On each server that you are deploying, install the appropriate Windows operating system as follows:</span></span>

  - <span data-ttu-id="904db-113">**Lync Server 2013 を実行しているサーバー**   Lync Server 2013 を実行しているサーバーのオペレーティングシステム要件の詳細については、サポートドキュメントの「 [Lync server 2013 でのサーバーとツールのオペレーティングシステムのサポート](lync-server-2013-server-and-tools-operating-system-support.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="904db-113">**Servers running Lync Server 2013**   For details about the operating system requirements for servers running Lync Server 2013, see [Server and tools operating system support in Lync Server 2013](lync-server-2013-server-and-tools-operating-system-support.md) in the Supportability documentation.</span></span>

  - <span data-ttu-id="904db-114">**データベースサーバー**   バックエンドデータベース、アーカイブデータベース、監視データベースなど、データベースサーバーのオペレーティングシステム要件の詳細については、SQL Server のマニュアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="904db-114">**Database servers**   For details about operating system requirements for database servers, including the back-end database, Archiving database, and Monitoring database, see the SQL Server documentation.</span></span> <span data-ttu-id="904db-115">SQL Server 2012 の場合は、SQL Server 2012 Books Online を参照してください [https://go.microsoft.com/fwlink/p/?linkId=218015](https://go.microsoft.com/fwlink/p/?linkid=218015) 。</span><span class="sxs-lookup"><span data-stu-id="904db-115">For SQL Server 2012, see the SQL Server 2012 Books Online at [https://go.microsoft.com/fwlink/p/?linkId=218015](https://go.microsoft.com/fwlink/p/?linkid=218015).</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="904db-116">Windows Server 2008 R2 SP1 で Lync Server 2013 をインストールする場合は、 &nbsp; &nbsp; まず Microsoft サポート技術情報の記事2646886、「修正: モジュールが IIS 7.5 で InsertEntityBody メソッドを呼び出すときにヒープの破損が発生する」、at、 <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=2646886"> https://go.microsoft.com/fwlink/p/?linkid=3052&amp kbid = 2646886</A>に記載されている更新プログラムをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="904db-116">If you are installing Lync Server 2013 on Windows Server&nbsp;2008&nbsp;R2 with SP1, you must first install the update described in the Microsoft Knowledge Based article 2646886, “FIX: Heap corruption occurs when a module calls the InsertEntityBody method in IIS 7.5”, at <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=2646886">https://go.microsoft.com/fwlink/p/?linkid=3052&amp;kbid=2646886</A>.</span></span><BR><span data-ttu-id="904db-117">また、「サポート技術情報」の記事に記載されているようにレジストリを変更する必要があります。これには、 <A href="https://go.microsoft.com/fwlink/p/?linkid=506893">Windows Server 2012 R2 にインストールされている Lync Server 2013 フロントエンドサーバーに</A>保存されている、「イベント id 32402, 61045 の記録」の</span><span class="sxs-lookup"><span data-stu-id="904db-117">You must also modify the registry as described in the KB article, <A href="https://go.microsoft.com/fwlink/p/?linkid=506893">Event IDs 32402, 61045 are logged in Lync Server 2013 Front End servers that are installed in Windows Server 2012 R2</A>.</span></span>



</div>

</div>

<div>

## <a name="install-windows-update-on-servers"></a><span data-ttu-id="904db-118">サーバーに Windows Update をインストールする</span><span class="sxs-lookup"><span data-stu-id="904db-118">Install Windows Update on Servers</span></span>

<span data-ttu-id="904db-119">各サーバー上の Windows Update から以下の更新プログラムをインストールします。</span><span class="sxs-lookup"><span data-stu-id="904db-119">Install the following updates from Windows Update on each server:</span></span>

  - <span data-ttu-id="904db-120">**Lync Server 2013 を実行しているサーバーの Windows Update**   Lync Server 2013 を実行しているサーバーに必要な Windows Update からの更新プログラムの詳細については、「計画ドキュメントの「 [Lync server 2013 のその他のソフトウェア要件](lync-server-2013-additional-software-requirements.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="904db-120">**Windows Update for servers running Lync Server 2013**   For details about the updates from Windows Update that are required for servers running Lync Server 2013, see [Additional software requirements for Lync Server 2013](lync-server-2013-additional-software-requirements.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="904db-121">**データベースサーバー**   バックエンドデータベース、アーカイブデータベース、監視データベースなど、データベースサーバーに必要な更新プログラムの詳細については、SQL Server 2012 に関するドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="904db-121">**Database servers**   For details about the updates from Windows Update that are required for database servers, including the back-end database, Archiving database, and Monitoring database, see the SQL Server 2012 documentation.</span></span> <span data-ttu-id="904db-122">SQL Server 2012 の場合は、SQL Server 2012 Books Online を参照してください [https://go.microsoft.com/fwlink/p/?linkId=218015](https://go.microsoft.com/fwlink/p/?linkid=218015) 。</span><span class="sxs-lookup"><span data-stu-id="904db-122">For SQL Server 2012, see the SQL Server 2012 Books Online at [https://go.microsoft.com/fwlink/p/?linkId=218015](https://go.microsoft.com/fwlink/p/?linkid=218015).</span></span>

</div>

<div>

## <a name="install-other-prerequisite-software-on-servers"></a><span data-ttu-id="904db-123">サーバーにその他の必須ソフトウェアをインストールする</span><span class="sxs-lookup"><span data-stu-id="904db-123">Install Other Prerequisite Software on Servers</span></span>

<span data-ttu-id="904db-124">Lync Server 2013 では、サーバーに次の追加ソフトウェアがインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="904db-124">Lync Server 2013 requires the installation of the following additional software on servers:</span></span>

  - <span data-ttu-id="904db-125">**Lync Server 2013 を実行しているサーバーの必須ソフトウェア**   Lync Server 2013 を実行しているサーバーのその他のソフトウェアの前提条件は、展開されているサーバーの役割によって異なります。</span><span class="sxs-lookup"><span data-stu-id="904db-125">**Prerequisite software for servers running Lync Server 2013**   The additional software prerequisites for servers running Lync Server 2013 depend on the server role being deployed.</span></span> <span data-ttu-id="904db-126">各サーバー固有のソフトウェア要件の詳細については、「計画ドキュメントの「 [Lync server 2013 のその他のソフトウェア要件](lync-server-2013-additional-software-requirements.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="904db-126">For details about the specific software requirements for each server, see [Additional software requirements for Lync Server 2013](lync-server-2013-additional-software-requirements.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="904db-127">**Windows Id ファンデーション**   Lync Server 2013 では、サーバー間認証のシナリオをサポートするために、Windows Id ファンデーションをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="904db-127">**Windows Identity Foundation**   Lync Server 2013 requires the installation of Windows Identity Foundation in order to support server-to-server authentication scenarios.</span></span> <span data-ttu-id="904db-128">コンピューターにインストールされていることを確認するには、[コントロールパネル]、[ **プログラムと機能**]、[ **インストールされている更新** プログラムの表示]、[ **Microsoft Windows**] の下の [確認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="904db-128">To verify that it has already been installed on your computer, go to Control Panel, click **Programs and Features**, **View installed updates**, and look under **Microsoft Windows**.</span></span> <span data-ttu-id="904db-129">Windows Id Foundation のインストールの詳細については、を参照してください [https://go.microsoft.com/fwlink/p/?linkId=204657](https://go.microsoft.com/fwlink/p/?linkid=204657) 。</span><span class="sxs-lookup"><span data-stu-id="904db-129">For details about installing Windows Identity Foundation, see [https://go.microsoft.com/fwlink/p/?linkId=204657](https://go.microsoft.com/fwlink/p/?linkid=204657).</span></span>

  - <span data-ttu-id="904db-130">**Microsoft .Net Framework 4.5**   Lync Server 2013 では、64ビット版の Microsoft .NET Framework 4.5 が必要です。</span><span class="sxs-lookup"><span data-stu-id="904db-130">**Microsoft .NET Framework 4.5**   The 64-bit edition of Microsoft .NET Framework 4.5 is required for Lync Server 2013.</span></span>

  - <span data-ttu-id="904db-131">**データベースサーバー向けの必須ソフトウェア**   バックエンドデータベース、アーカイブデータベース、監視データベースなど、データベースサーバーに必要な Windows Update の詳細については、SQL Server 2012 に関するドキュメントを参照してください [https://go.microsoft.com/fwlink/p/?linkId=218015](https://go.microsoft.com/fwlink/p/?linkid=218015) 。</span><span class="sxs-lookup"><span data-stu-id="904db-131">**Prerequisite software for database servers**   For details about the Windows Update required for database servers, including the back-end database, Archiving database, and Monitoring database, see the SQL Server 2012 documentation at [https://go.microsoft.com/fwlink/p/?linkId=218015](https://go.microsoft.com/fwlink/p/?linkid=218015).</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="904db-132">Lync Server 2013 は、各標準エディションサーバーと、ローカル構成ストアが配置されている Lync Server 2013 を実行している各サーバーに、Microsoft SQL Server 2012 Express を自動的にインストールします。</span><span class="sxs-lookup"><span data-stu-id="904db-132">Lync Server 2013 automatically installs Microsoft SQL Server 2012 Express on each Standard Edition server and each server running Lync Server 2013 on which the local configuration store is located.</span></span>

    
    </div>

  - <span data-ttu-id="904db-133">**Windows Media Format Runtime**   会議を展開するすべてのフロントエンドサーバーおよび標準エディションサーバーには、Windows Media Format ランタイムがインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="904db-133">**Windows Media Format Runtime**   All Front End Servers and Standard Edition servers where conferencing will be deployed must have the Windows Media Format Runtime installed.</span></span> <span data-ttu-id="904db-134">Windows Media 形式ランタイムは、コールパーク、アナウンスメント、および応答グループアプリケーションがお知らせや音楽を再生するために、Windows Media オーディオ (.wma) ファイルを実行するために必要です。</span><span class="sxs-lookup"><span data-stu-id="904db-134">The Windows Media Format Runtime is required to run the Windows Media Audio (.wma) files that the Call Park, Announcement, and Response Group applications play for announcements and music.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="904db-135">Windows Server 2012 および Windows Server 2012 R2 の場合、Windows Media Format Runtime は Microsoft メディアファンデーションと共にインストールされます。</span><span class="sxs-lookup"><span data-stu-id="904db-135">For Windows Server 2012 and Windows Server 2012 R2 the Windows Media Format Runtime installs with Microsoft Media Foundation.</span></span>

    
    </div>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="904db-136">Windows Server &nbsp; 2008 および Windows server &nbsp; 2008 R2 の場合、Windows &nbsp; デスクトップエクスペリエンスの一部として Windows Media 形式ランタイムがインストールされます。</span><span class="sxs-lookup"><span data-stu-id="904db-136">For Windows Server&nbsp;2008 and Windows Server&nbsp;2008&nbsp;R2 the Windows Media Format Runtime installs as part of the Windows Desktop Experience.</span></span> <span data-ttu-id="904db-137">Lync Server 2013 をインストールする前に、Windows デスクトップエクスペリエンスをインストールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="904db-137">It is recommended that you install Windows Desktop Experience before you install Lync Server 2013.</span></span> <span data-ttu-id="904db-138">Lync Server 2013 でサーバー上にこのソフトウェアが見つからない場合は、インストールするように求められます。その後、インストールを完了するには、サーバーを再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="904db-138">If Lync Server 2013 does not find this software on the server, it will prompt you to install it, and then you must restart the server to complete installation.</span></span>

    
    <span data-ttu-id="904db-139"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="904db-139"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

