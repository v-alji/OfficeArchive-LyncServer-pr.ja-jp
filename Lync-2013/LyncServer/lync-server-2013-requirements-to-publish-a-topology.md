---
title: 'Lync Server 2013: トポロジを公開する場合の要件'
description: 'Lync Server 2013: トポロジを公開するための要件。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Requirements to publish a topology
ms:assetid: 841cdf5d-d884-414d-ab50-3bb681b622ed
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg195733(v=OCS.15)
ms:contentKeyID: 48184688
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5699657e680b78587b8ba354e9dc538f2e280c56
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436357"
---
# <a name="requirements-to-publish-a-topology-in-lync-server-2013"></a><span data-ttu-id="2ed1a-103">Lync Server 2013 でトポロジを公開する場合の要件</span><span class="sxs-lookup"><span data-stu-id="2ed1a-103">Requirements to publish a topology in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2ed1a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2ed1a-104">

<span> </span></span></span>

<span data-ttu-id="2ed1a-105">_**最終更新日:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="2ed1a-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="2ed1a-106">このトピックでは、トポロジビルダーを使用するか、または Lync Server 2013 Management Shell コマンドラインインターフェイスを使用しているかにかかわらず、トポロジの発行に固有のインフラストラクチャとソフトウェアの要件について説明します。</span><span class="sxs-lookup"><span data-stu-id="2ed1a-106">This topic describes the infrastructure and software requirements that are specific to publishing a topology, whether by using Topology Builder or the Lync Server 2013 Management Shell command-line interface.</span></span> <span data-ttu-id="2ed1a-107">これらの要件は、すべての Lync Server 2013 管理ツールに適用されるオペレーティングシステム、ソフトウェア、アクセス許可の一般的な要件に加えています。</span><span class="sxs-lookup"><span data-stu-id="2ed1a-107">These requirements are in addition to the general operating system, software, and permissions requirements applicable to all Lync Server 2013 administrative tools.</span></span> <span data-ttu-id="2ed1a-108">トポロジを公開する前に、管理ツールの要件をすべて満たしていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="2ed1a-108">Make sure that you satisfy all administrative tools requirements before you publish a topology.</span></span>

  - <span data-ttu-id="2ed1a-109">作成している Lync Server 2013 展開の同じドメインまたはフォレストに参加しているコンピューターでトポロジビルダーを実行して、Active Directory ドメインサービスの準備手順が完了していることを確認します。そのコンピューターの管理ツールを使用して、トポロジを正常に公開することができます。</span><span class="sxs-lookup"><span data-stu-id="2ed1a-109">You must run Topology Builder on a computer that is joined to the same domain or forest of the Lync Server 2013 deployment you are creating so that Active Directory Domain Services preparation steps are already completed, enabling you to use the administrative tools on that computer to successfully publish your topology.</span></span>

  - <span data-ttu-id="2ed1a-110">トポロジで定義されたコンピューターは、エッジサーバーと AD DS を除き、ドメインに参加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2ed1a-110">The computers defined in the topology must be joined to the domain, except for Edge Servers, and in AD DS.</span></span> <span data-ttu-id="2ed1a-111">ただし、トポロジを公開するときに、コンピューターはオンラインである必要はありません。</span><span class="sxs-lookup"><span data-stu-id="2ed1a-111">However, the computers do not need to be online when you publish the topology.</span></span>

  - <span data-ttu-id="2ed1a-112">プールのファイル共有を作成し、リモートユーザーが使用できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2ed1a-112">The file share for the pool must be created and available to remote users.</span></span>

  - <span data-ttu-id="2ed1a-113">Enterprise Edition のフロントエンドプールを公開するには、SQL Server ベースのバックエンドサーバーを、リモートユーザーが利用できるようにするために、適切なファイアウォールルールを使用してサーバーを展開しているドメインに参加している必要があります。</span><span class="sxs-lookup"><span data-stu-id="2ed1a-113">In order to publish an Enterprise Edition Front End pool, the SQL Server-based Back End Server must be joined to the domain in which you are deploying the servers, online, and configured with the appropriate firewall rules to make it available to remote users.</span></span> <span data-ttu-id="2ed1a-114">ファイアウォールの例外の指定の詳細については、「 [Lync server 2013 での SQL Server のファイアウォール要件につい](lync-server-2013-understanding-firewall-requirements-for-sql-server.md)て」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2ed1a-114">For details about specifying firewall exceptions, see [Understanding firewall requirements for SQL Server with Lync Server 2013](lync-server-2013-understanding-firewall-requirements-for-sql-server.md).</span></span> <span data-ttu-id="2ed1a-115">SQL Server の構成の詳細については、「 [Lync server 2013 用に Sql server を構成する](lync-server-2013-configure-sql-server-for-lync-server.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2ed1a-115">For other details about configuring SQL Server, see [Configure SQL Server for Lync Server 2013](lync-server-2013-configure-sql-server-for-lync-server.md).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="2ed1a-116">Standard Edition サーバーには、公開された構成を受け入れる、併置されたデータベースがあります。</span><span class="sxs-lookup"><span data-stu-id="2ed1a-116">Standard Edition server has a collocated database that will accept the published configuration.</span></span> <span data-ttu-id="2ed1a-117">まず、Lync Server 展開ウィザードで [ <STRONG>最初の Standard Edition server</STRONG> セットアップ] タスクを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2ed1a-117">You must first run the <STRONG>Prepare first Standard Edition server</STRONG> setup task in the Lync Server Deployment Wizard.</span></span>

    
    </div>

<div>

## <a name="see-also"></a><span data-ttu-id="2ed1a-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="2ed1a-118">See Also</span></span>


[<span data-ttu-id="2ed1a-119">Lync Server 2013 でトポロジを公開する</span><span class="sxs-lookup"><span data-stu-id="2ed1a-119">Publish the topology in Lync Server 2013</span></span>](lync-server-2013-publish-the-topology.md)  
[<span data-ttu-id="2ed1a-120">Lync Server 2013 でのセットアップのアクセス許可の委任</span><span class="sxs-lookup"><span data-stu-id="2ed1a-120">Delegate setup permissions in Lync Server 2013</span></span>](lync-server-2013-delegate-setup-permissions.md)  


[<span data-ttu-id="2ed1a-121">Lync Server 2013 の管理ツールのソフトウェア要件</span><span class="sxs-lookup"><span data-stu-id="2ed1a-121">Administrative tools software requirements in Lync Server 2013</span></span>](lync-server-2013-administrative-tools-software-requirements.md)  
[<span data-ttu-id="2ed1a-122">Lync Server 2013 でのサーバーおよびツールのオペレーティング システムのサポート</span><span class="sxs-lookup"><span data-stu-id="2ed1a-122">Server and tools operating system support in Lync Server 2013</span></span>](lync-server-2013-server-and-tools-operating-system-support.md)  


[<span data-ttu-id="2ed1a-123">Lync Server 2013 のセットアップと管理に必要な管理者権限およびアクセス許可</span><span class="sxs-lookup"><span data-stu-id="2ed1a-123">Administrator rights and permissions required for setup and administration of Lync Server 2013</span></span>](lync-server-2013-administrator-rights-and-permissions-required-for-setup-and-administration.md)  
  

<span data-ttu-id="2ed1a-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2ed1a-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

