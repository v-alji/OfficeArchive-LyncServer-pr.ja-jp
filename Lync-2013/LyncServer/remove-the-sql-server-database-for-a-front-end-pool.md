---
title: フロントエンド プール用の SQL Server データベースの削除
description: フロントエンドプールの SQL Server データベースを削除します。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove the SQL Server database for a Front End pool
ms:assetid: 6bb932df-3ed7-49b6-ae17-61e4c6a5fe82
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688084(v=OCS.15)
ms:contentKeyID: 49733681
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 01c5d47e4c52197c5792fa3b7770da7bbd1b26cb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400076"
---
# <a name="remove-the-sql-server-database-for-a-front-end-pool"></a><span data-ttu-id="36bc5-103">フロントエンド プール用の SQL Server データベースの削除</span><span class="sxs-lookup"><span data-stu-id="36bc5-103">Remove the SQL Server database for a Front End pool</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="36bc5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="36bc5-104">

<span> </span></span></span>

<span data-ttu-id="36bc5-105">_**最終更新日:** 2012-10-04_</span><span class="sxs-lookup"><span data-stu-id="36bc5-105">_**Topic Last Modified:** 2012-10-04_</span></span>

<span data-ttu-id="36bc5-106">Microsoft Lync Server 2010 フロントエンドプールを削除するか、プールを再構成して別のデータベースを使用する場合は、プールデータをホストしている SQL Server データベースを削除できます。</span><span class="sxs-lookup"><span data-stu-id="36bc5-106">After you remove a Microsoft Lync Server 2010 Front End pool or reconfigure the pool to use a different database, you can remove the SQL Server databases that hosted the pool data.</span></span> <span data-ttu-id="36bc5-107">次の手順を使用して、Topology Builder から定義を削除し、データベースサーバーからデータベースとログファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="36bc5-107">Use the following procedures to remove the definitions from Topology Builder, and then remove the database and log files from the database server.</span></span>

<div>

## <a name="to-remove-the-sql-server-database-using-topology-builder"></a><span data-ttu-id="36bc5-108">トポロジビルダーを使用して SQL Server データベースを削除するには</span><span class="sxs-lookup"><span data-stu-id="36bc5-108">To remove the SQL Server database using Topology Builder</span></span>

1.  <span data-ttu-id="36bc5-109">Lync Server 2013 フロントエンドサーバーから、[トポロジビルダー] を開き、既存のトポロジをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="36bc5-109">From the Lync Server 2013 Front End Server, open Topology Builder and download the existing topology.</span></span>

2.  <span data-ttu-id="36bc5-110">[トポロジビルダー] で、[ **共有コンポーネント** ] に移動し、[ **sql Server ストア**] で、削除または再構成されたフロントエンドプールに関連付けられている sql server インスタンスを右クリックし、[ **削除**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="36bc5-110">In Topology Builder, navigate to **Shared Components** and then **SQL Server Stores**, right-click the SQL Server instance associated with the removed or reconfigured Front End pool, and then click **Delete**.</span></span>

3.  <span data-ttu-id="36bc5-111">トポロジを公開し、レプリケーションの状態を確認します。</span><span class="sxs-lookup"><span data-stu-id="36bc5-111">Publish the topology, and then check the replication status.</span></span>

</div>

<div>

## <a name="to-remove-user-and-application-databases-from-the-sql-server"></a><span data-ttu-id="36bc5-112">SQL Server からユーザーデータベースとアプリケーションデータベースを削除するには</span><span class="sxs-lookup"><span data-stu-id="36bc5-112">To remove user and application databases from the SQL Server</span></span>

1.  <span data-ttu-id="36bc5-113">SQL Server 上のデータベースを削除するには、データベースファイルを削除する SQL Server の [SQL Server のオプション] グループのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="36bc5-113">To remove the databases on the SQL Server, you must be a member of the SQL Server sysadmins group for the SQL Server where you are removing the database files.</span></span>

2.  <span data-ttu-id="36bc5-114">Lync Server 管理シェルを開く</span><span class="sxs-lookup"><span data-stu-id="36bc5-114">Open Lync Server Management Shell</span></span>

3.  <span data-ttu-id="36bc5-115">プールユーザーストアのデータベースを削除するには、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="36bc5-115">To remove the database for the pool user store, type:</span></span>
    
        Uninstall-CsDataBase -DatabaseType User -SqlServerFqdn <FQDN> [-SqlInstanceName <instance>]
    
    <span data-ttu-id="36bc5-116">\<FQDN\>は、データベースサーバーの完全修飾ドメイン名 (FQDN) であり、 \<instance\> 名前付きデータベースインスタンス (定義されている場合) です。</span><span class="sxs-lookup"><span data-stu-id="36bc5-116">Where \<FQDN\> is the fully qualified domain name (FQDN) of the database server, and \<instance\> is the named database instance (that is, if one was defined).</span></span>

4.  <span data-ttu-id="36bc5-117">プールアプリケーションストアのデータベースを削除するには、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="36bc5-117">To remove the database for the pool application store, type:</span></span>
    
        Uninstall-CsDataBase -DatabaseType Application -SqlServerFqdn <FQDN> [-SqlInstanceName <instance>]
    
    <span data-ttu-id="36bc5-118">\<FQDN\>は、データベースサーバーの FQDN であり、 \<instance\> 名前付きデータベースインスタンス (定義されている場合) です。</span><span class="sxs-lookup"><span data-stu-id="36bc5-118">Where \<FQDN\> is the FQDN of the database server, and \<instance\> is the named database instance (that is, if one was defined).</span></span>

5.  <span data-ttu-id="36bc5-119">**CsDataBase** コマンドレットで操作の確認を求めるメッセージが表示されたら、情報を読み、 **Y** キーを押します (または、enter キーを押すか、enter キーを押して続行します)。または、コマンドレットを停止するか (エラーがある場合)、enter キー **を押します**。</span><span class="sxs-lookup"><span data-stu-id="36bc5-119">When the **Uninstall-CsDataBase** cmdlet prompts you to confirm actions, read the information, and then press **Y** (or press Enter) to proceed, or press **N** and then Enter if you want to stop the cmdlet (that is, in case there errors).</span></span>

<span data-ttu-id="36bc5-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="36bc5-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

