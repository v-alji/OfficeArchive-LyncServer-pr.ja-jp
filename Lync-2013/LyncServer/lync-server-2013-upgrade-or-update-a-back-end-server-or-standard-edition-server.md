---
title: バックエンドサーバーまたは Standard Edition server をアップグレードまたは更新する
description: バックエンドサーバーまたは Standard Edition サーバーをアップグレードまたは更新します。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Upgrade or update a Back End Server or Standard Edition server
ms:assetid: f95f8d3a-e039-484e-97bd-d727db21a12b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721942(v=OCS.15)
ms:contentKeyID: 49733879
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c529546bdcf88ada6fd82399d3b65b46b4312db0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440823"
---
# <a name="upgrade-or-update-a-back-end-server-or-standard-edition-server-in-lync-server-2013"></a><span data-ttu-id="eb8f9-103">Lync Server 2013 でバックエンドサーバーまたは Standard Edition サーバーをアップグレードまたは更新する</span><span class="sxs-lookup"><span data-stu-id="eb8f9-103">Upgrade or update a Back End Server or Standard Edition server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="eb8f9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="eb8f9-104">

<span> </span></span></span>

<span data-ttu-id="eb8f9-105">_**最終更新日:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="eb8f9-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="eb8f9-106">このトピックでは、Enterprise Edition バックエンドサーバーまたは Standard Edition サーバーに更新プログラムをインストールする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="eb8f9-106">This topic explains how to install an update on an Enterprise Edition Back End Server or a Standard Edition server.</span></span>

<span data-ttu-id="eb8f9-107">アップグレード中に少なくとも30分間バックエンドサーバーが停止している場合、ユーザーは回復性モードに移行することがあります。</span><span class="sxs-lookup"><span data-stu-id="eb8f9-107">If a Back End Server is down for at least 30 minutes while you are upgrading it, users may then go into resiliency mode.</span></span> <span data-ttu-id="eb8f9-108">アップグレードが完了し、バックエンドサーバーがプール内のフロントエンドサーバーに再度接続されると、ユーザーは完全な機能に戻ります。</span><span class="sxs-lookup"><span data-stu-id="eb8f9-108">When the upgrade is finished and the Back End Servers has again connected with the Front End Servers in the pool, users are returned to full functionality.</span></span> <span data-ttu-id="eb8f9-109">アップグレードが 30 分未満の場合、ユーザーには影響ありません。</span><span class="sxs-lookup"><span data-stu-id="eb8f9-109">If the upgrade takes less than 30 minutes, users will not be affected.</span></span>

<div>

## <a name="to-update-a-back-end-server-or-standard-edition-server"></a><span data-ttu-id="eb8f9-110">バックエンド サーバーまたは Standard Edition サーバーを更新するには</span><span class="sxs-lookup"><span data-stu-id="eb8f9-110">To update a back end server or Standard Edition server</span></span>

1.  <span data-ttu-id="eb8f9-111">アップグレードするサーバーに CsAdministrator の役割のメンバーとしてログオンします。</span><span class="sxs-lookup"><span data-stu-id="eb8f9-111">Log on to the server you are upgrading as a member of the CsAdministrator role.</span></span>

2.  <span data-ttu-id="eb8f9-112">更新をダウンロードして、ローカル ハードディスクに抽出します。</span><span class="sxs-lookup"><span data-stu-id="eb8f9-112">Download the update and extract it to the local hard disk.</span></span>

3.  <span data-ttu-id="eb8f9-113">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="eb8f9-113">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

4.  <span data-ttu-id="eb8f9-114">Lync Server サービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="eb8f9-114">Stop Lync Server services.</span></span> <span data-ttu-id="eb8f9-115">コマンド ラインで次を入力します。</span><span class="sxs-lookup"><span data-stu-id="eb8f9-115">At the command line, type:</span></span>
    
        Stop-CsWindowsService

5.  <span data-ttu-id="eb8f9-116">World Wide Web サービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="eb8f9-116">Stop the World Wide Web service.</span></span> <span data-ttu-id="eb8f9-117">コマンド ラインで次を入力します。</span><span class="sxs-lookup"><span data-stu-id="eb8f9-117">At the command line, type:</span></span>
    
        net stop w3svc

6.  <span data-ttu-id="eb8f9-118">すべての Lync Server 管理シェルウィンドウを閉じます。</span><span class="sxs-lookup"><span data-stu-id="eb8f9-118">Close all Lync Server Management Shell windows.</span></span>

7.  <span data-ttu-id="eb8f9-119">更新をインストールします。</span><span class="sxs-lookup"><span data-stu-id="eb8f9-119">Install the update.</span></span>

8.  <span data-ttu-id="eb8f9-120">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="eb8f9-120">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

9.  <span data-ttu-id="eb8f9-121">もう一度 Lync Server サービスを停止して、グローバルアセンブリキャッシュ (GAC) – d アセンブリをキャッチします。</span><span class="sxs-lookup"><span data-stu-id="eb8f9-121">Stop Lync Server services again to catch Global Assembly Cache (GAC) –d assemblies.</span></span> <span data-ttu-id="eb8f9-122">コマンド ラインで次を入力します。</span><span class="sxs-lookup"><span data-stu-id="eb8f9-122">At the command line, type:</span></span>
    
        Stop-CsWindowsService

10. <span data-ttu-id="eb8f9-123">World Wide Web サービスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="eb8f9-123">Restart the World Wide Web service.</span></span> <span data-ttu-id="eb8f9-124">コマンド ラインで次を入力します。</span><span class="sxs-lookup"><span data-stu-id="eb8f9-124">At the command line, type:</span></span>
    
        net start w3svc

11. <span data-ttu-id="eb8f9-125">次のいずれかの方法で、LyncServerUpdateInstaller.exe によって行われた変更を SQL Server データベースに適用します。</span><span class="sxs-lookup"><span data-stu-id="eb8f9-125">Apply the changes made by LyncServerUpdateInstaller.exe to the SQL Server databases by doing one of the following:</span></span>
    
      - <span data-ttu-id="eb8f9-126">Enterprise Edition バックエンドサーバーで、データベースのアーカイブや監視など、このサーバー上に併置されたデータベースがない場合は、コマンドラインで次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="eb8f9-126">If this is an Enterprise Edition Back End Server and there are no collocated databases on this server, such as Archiving or Monitoring databases, then type the following at a command line:</span></span>
        
            Install-CsDatabase -Update -ConfiguredDatabases -SqlServerFqdn <SQL Server FQDN>
    
      - <span data-ttu-id="eb8f9-127">Enterprise Edition バックエンドサーバーで、このサーバーに併置されたデータベースがある場合は、コマンドラインで次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="eb8f9-127">If this is an Enterprise Edition Back End Server and there are collocated databases on this server, then type the following at a command line:</span></span>
        
            Install-CsDatabase -Update -ConfiguredDatabases -SqlServerFqdn <SQL Server FQDN>  -ExcludeCollocatedStores
    
      - <span data-ttu-id="eb8f9-128">Standard Edition サーバーの場合は、コマンドラインで次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="eb8f9-128">If this is an Standard Edition server, type the following at a command line:</span></span>
        
            Install-CsDatabase -Update -LocalDatabases

<span data-ttu-id="eb8f9-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="eb8f9-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

