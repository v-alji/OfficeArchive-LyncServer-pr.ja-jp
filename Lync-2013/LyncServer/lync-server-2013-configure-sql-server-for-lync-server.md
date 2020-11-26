---
title: 'Lync Server 2013: Lync Server 用 SQL Server の構成'
description: 'Lync Server 2013: Lync Server 用の SQL Server を構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure SQL Server for Lync Server 2013
ms:assetid: 375e5cc4-e436-46dc-9b02-5063f35cdcc1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425848(v=OCS.15)
ms:contentKeyID: 48183869
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d9ac7d8f14c64f3b7935df3f48602a6df1791c7a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433711"
---
# <a name="configure-sql-server-for-lync-server-2013"></a><span data-ttu-id="c284f-103">Lync Server 2013 用 SQL Server の構成</span><span class="sxs-lookup"><span data-stu-id="c284f-103">Configure SQL Server for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c284f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c284f-104">

<span> </span></span></span>

<span data-ttu-id="c284f-105">_**最終更新日:** 2013-08-12_</span><span class="sxs-lookup"><span data-stu-id="c284f-105">_**Topic Last Modified:** 2013-08-12_</span></span>

<span data-ttu-id="c284f-106">このセクションのトピックでは、Lync Server のエンタープライズ展開で使用するように SQL Server を展開して構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c284f-106">The topics in this section discuss how to deploy and configure SQL Server to use in an Enterprise deployment of Lync Server.</span></span> <span data-ttu-id="c284f-107">Standard Edition サーバーでは、標準エディションサーバーのワークロードに合わせて適切にサイズ調整された sql Server Express バージョンの SQL Server を使用します。</span><span class="sxs-lookup"><span data-stu-id="c284f-107">Standard Edition servers use a collocated SQL Server Express version of SQL Server that is right sized for the workloads of a Standard Edition server.</span></span>

<span data-ttu-id="c284f-108">Lync Server 2013 の中央管理ストアは、プール内のすべての Enterprise Edition サーバーのユーザーデータを保持し、SQL Server ベースのバックエンドサーバーに配置されるように設計されています。</span><span class="sxs-lookup"><span data-stu-id="c284f-108">The Lync Server 2013 Central Management store holds user data for all Enterprise Edition servers within a pool, and is designed to be located on a SQL Server -based Back End Server.</span></span> <span data-ttu-id="c284f-109">一元的なリポジトリとして、中央管理ストアは、他の Lync Server 2013 の役割と同じコンピューターにインストールすることはできません。</span><span class="sxs-lookup"><span data-stu-id="c284f-109">As a centralized repository, the Central Management store cannot be installed on the same computer as any other Lync Server 2013 role.</span></span> <span data-ttu-id="c284f-110">中央管理ストアは、プール内の Enterprise Edition サーバー上に配置できません。</span><span class="sxs-lookup"><span data-stu-id="c284f-110">The Central Management store cannot reside on an Enterprise Edition server in the pool.</span></span> <span data-ttu-id="c284f-111">最初にトポロジを公開し、選択してデータベースを作成すると、中央管理ストアが自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="c284f-111">The Central Management store is created automatically when you publish the topology for the first time and select to create the databases.</span></span> <span data-ttu-id="c284f-112">インストールを正常に実行するためには、バックエンドサーバーとして指定したコンピューターで SQL Server データベースソフトウェアが実行されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="c284f-112">The computer that you designate as the Back End Server must already be running SQL Server database software in order for the installation to succeed.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="c284f-113">このセクション中</span><span class="sxs-lookup"><span data-stu-id="c284f-113">In This Section</span></span>

  - [<span data-ttu-id="c284f-114">Lync Server 2013 の SQL Server データとログ ファイルの配置</span><span class="sxs-lookup"><span data-stu-id="c284f-114">SQL Server data and log file placement for Lync Server 2013</span></span>](lync-server-2013-sql-server-data-and-log-file-placement.md)

  - [<span data-ttu-id="c284f-115">Lync Server 2013 での SQL Server の構成</span><span class="sxs-lookup"><span data-stu-id="c284f-115">Configure SQL Server in Lync Server 2013</span></span>](lync-server-2013-configure-sql-server.md)

  - [<span data-ttu-id="c284f-116">Lync Server 2013 の SQL Server の展開のアクセス許可</span><span class="sxs-lookup"><span data-stu-id="c284f-116">Deployment permissions for SQL Server in Lync Server 2013</span></span>](lync-server-2013-deployment-permissions-for-sql-server.md)

  - [<span data-ttu-id="c284f-117">Lync Server 2013 での Lync Server 管理シェルを使用したデータベースのインストール</span><span class="sxs-lookup"><span data-stu-id="c284f-117">Database installation using Lync Server Management Shell in Lync Server 2013</span></span>](lync-server-2013-database-installation-using-lync-server-management-shell.md)

  - [<span data-ttu-id="c284f-118">Lync Server 2013 での SQL Server のファイアウォール要件について</span><span class="sxs-lookup"><span data-stu-id="c284f-118">Understanding firewall requirements for SQL Server with Lync Server 2013</span></span>](lync-server-2013-understanding-firewall-requirements-for-sql-server.md)

  - [<span data-ttu-id="c284f-119">Lync Server 2013 用の SQL Server クラスタリングを構成する</span><span class="sxs-lookup"><span data-stu-id="c284f-119">Configure SQL Server clustering for Lync Server 2013</span></span>](lync-server-2013-configure-sql-server-clustering.md)

<span data-ttu-id="c284f-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c284f-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

