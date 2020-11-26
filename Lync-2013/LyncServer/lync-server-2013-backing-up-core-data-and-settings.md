---
title: 'Lync Server 2013: コアデータと設定のバックアップ'
description: 'Lync Server 2013: コアデータと設定をバックアップします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Backing up core data and settings
ms:assetid: 278bc95a-7b8d-4e01-a872-a844830459de
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202170(v=OCS.15)
ms:contentKeyID: 51541452
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 637eeb950a3b8380f6e756f46a5083f51b5d7e1f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438100"
---
# <a name="backing-up-core-data-and-settings-in-lync-server-2013"></a><span data-ttu-id="470c4-103">Lync Server 2013 でのコアデータと設定のバックアップ</span><span class="sxs-lookup"><span data-stu-id="470c4-103">Backing up core data and settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="470c4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="470c4-104">

<span> </span></span></span>

<span data-ttu-id="470c4-105">_**最終更新日:** 2014-04-23_</span><span class="sxs-lookup"><span data-stu-id="470c4-105">_**Topic Last Modified:** 2014-04-23_</span></span>

<span data-ttu-id="470c4-106">次の手順では、Lync Server Management Shell コマンドレットを使用して、コアサービスの設定とデータのバックアップファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="470c4-106">The following procedures use Lync Server Management Shell cmdlets to create backup files for settings and data for core services.</span></span> <span data-ttu-id="470c4-107">このセクションで使用されるツールの詳細については、「 [Lync Server 2013 のバックアップと復元の要件](lync-server-2013-backup-and-restoration-requirements-tools-and-permissions.md)」を参照してください。ツールと権限。</span><span class="sxs-lookup"><span data-stu-id="470c4-107">For details about the tools used in this section, including where they are located, see [Backup and restoration requirements in Lync Server 2013: tools and permissions](lync-server-2013-backup-and-restoration-requirements-tools-and-permissions.md).</span></span> <span data-ttu-id="470c4-108">アーカイブと監視データのバックアップの詳細については、「 [Lync Server 2013 でのアーカイブと監視データベースのバックアップ](lync-server-2013-backing-up-archiving-and-monitoring-databases.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="470c4-108">For details about backing up Archiving and Monitoring data, see [Backing up Archiving and Monitoring databases in Lync Server 2013](lync-server-2013-backing-up-archiving-and-monitoring-databases.md).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="470c4-109">このセクションの中央管理ストアをバックアップする手順には、アーカイブと監視の設定と構成が含まれます。</span><span class="sxs-lookup"><span data-stu-id="470c4-109">The step in this section to back up the Central Management store includes the settings and configuration for Archiving and Monitoring.</span></span>



</div>

<span data-ttu-id="470c4-110">このセクションで説明されているコマンドレットは、ローカルまたはリモートで実行できます。</span><span class="sxs-lookup"><span data-stu-id="470c4-110">You can run the cmdlets described in this section locally or remotely.</span></span>

<div>

## <a name="to-back-up-core-data-and-settings"></a><span data-ttu-id="470c4-111">コアデータと設定をバックアップするには</span><span class="sxs-lookup"><span data-stu-id="470c4-111">To back up core data and settings</span></span>

1.  <span data-ttu-id="470c4-112">RTCUniversalServerAdmins グループのメンバーであるユーザーアカウントから、社内展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="470c4-112">From a user account that is a member of the RTCUniversalServerAdmins group, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="470c4-113">次の手順で作成したバックアップを保存するには、新しい共有フォルダーを作成し、 **$Backup** によって参照されるパスを新しい共有フォルダーに更新します。</span><span class="sxs-lookup"><span data-stu-id="470c4-113">To store the backups you create in the following steps, create a new shared folder and update the path referenced by **$Backup** to the new shared folder.</span></span>

3.  <span data-ttu-id="470c4-114">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="470c4-114">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

4.  <span data-ttu-id="470c4-115">一元管理ストア構成ファイルをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="470c4-115">Back up the Central Management store configuration file.</span></span> <span data-ttu-id="470c4-116">コマンドラインで、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="470c4-116">At the command line, type the following:</span></span>
    
        Export-CsConfiguration -FileName <path and file name for backup>
    
    <span data-ttu-id="470c4-117">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="470c4-117">For example:</span></span>
    
        Export-CsConfiguration -FileName "C:\Config.zip"
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="470c4-118">この手順では、Lync サーバーのトポロジ、ポリシー、構成の設定をファイルにエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="470c4-118">This step exports your Lync Server topology, policies, and configuration settings to a file.</span></span> <span data-ttu-id="470c4-119">トポロジデータをバックアップするために、他の手順は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="470c4-119">No other step is required to backup topology data.</span></span>

    
    </div>

5.  <span data-ttu-id="470c4-120">バックアップされた全体管理ストア構成ファイルを $Backup にコピーし \\ ます。</span><span class="sxs-lookup"><span data-stu-id="470c4-120">Copy the backed-up Central Management store configuration file to $Backup\\.</span></span>

6.  <span data-ttu-id="470c4-121">位置情報サービスのデータをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="470c4-121">Back up Location Information service data.</span></span> <span data-ttu-id="470c4-122">コマンドラインで、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="470c4-122">At the command line, type the following:</span></span>
    
        Export-CsLisConfiguration -FileName <path and file name for backup>
    
    <span data-ttu-id="470c4-123">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="470c4-123">For example:</span></span>
    
        Export-CsLisConfiguration -FileName "C:\E911Config.zip"

7.  <span data-ttu-id="470c4-124">バックアップされた場所情報サービス構成ファイルを $Backup にコピーし \\ ます。</span><span class="sxs-lookup"><span data-stu-id="470c4-124">Copy the backed-up Location Information service configuration file to $Backup\\.</span></span>

8.  <span data-ttu-id="470c4-125">フロントエンドプールおよびすべての Standard Edition サーバーの各バックエンドデータベースで、ユーザーデータをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="470c4-125">Back up user data on every back-end database of a Front End pool and every Standard Edition server.</span></span> <span data-ttu-id="470c4-126">コマンドラインで、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="470c4-126">At the command line, type the following:</span></span>
    
        Export-CsUserData -PoolFQDN <Fqdn> -FileName <String>
    
    <span data-ttu-id="470c4-127">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="470c4-127">For example:</span></span>
    
        Export-CsUserData -PoolFQDN "atl-cs-001.litwareinc.com" -FileName "C:\Logs\ExportedUserData.zip"

9.  <span data-ttu-id="470c4-128">バックアップされたユーザーファイルを $Backup にコピーし \\ ます。</span><span class="sxs-lookup"><span data-stu-id="470c4-128">Copy the backed up user file to $Backup\\.</span></span>

10. <span data-ttu-id="470c4-129">応答グループアプリケーションを実行するすべてのプールで、応答グループの構成をバックアップします。</span><span class="sxs-lookup"><span data-stu-id="470c4-129">On every pool that runs the Response Group application, back up the Response Group configuration.</span></span> <span data-ttu-id="470c4-130">以下の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="470c4-130">Do the following:</span></span>
    
    1.  <span data-ttu-id="470c4-131">コマンドラインで、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="470c4-131">At the command line, type:</span></span>
        
            Export-CsRgsConfiguration -Source "service:ApplicationServer:<pool FQDN>" -FileName <path and file name for backup>
        
        <span data-ttu-id="470c4-132">例:</span><span class="sxs-lookup"><span data-stu-id="470c4-132">For example:</span></span>
        
            Export-CsRgsConfiguration -Source ApplicationServer:pool01.contoso.com -FileName C:\RgsConfiguration.zip

11. <span data-ttu-id="470c4-133">バックアップされた応答グループ構成ファイルを $Backup にコピーし \\ ます。</span><span class="sxs-lookup"><span data-stu-id="470c4-133">Copy the backed up Response Group configuration file to $Backup\\.</span></span>

<span data-ttu-id="470c4-134"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="470c4-134"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

