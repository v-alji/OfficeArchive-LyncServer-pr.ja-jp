---
title: 'Lync Server 2013: 更新されたトポロジを発行してアーカイブデータベースを追加する'
description: 'Lync Server 2013: 更新されたトポロジを発行して、アーカイブデータベースを追加します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Publishing the updated topology to add Archiving databases
ms:assetid: 454c68df-2ef5-4b5f-a44c-4eee02635d45
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204860(v=OCS.15)
ms:contentKeyID: 48184034
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 90d1c53fb2a2dde5dde079f09b13ff4f06a659b3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399032"
---
# <a name="publishing-the-updated-topology-to-add-archiving-databases-in-lync-server-2013"></a><span data-ttu-id="84d37-103">更新されたトポロジを発行して、Lync Server 2013 でアーカイブデータベースを追加する</span><span class="sxs-lookup"><span data-stu-id="84d37-103">Publishing the updated topology to add Archiving databases in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="84d37-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="84d37-104">

<span> </span></span></span>

<span data-ttu-id="84d37-105">_**最終更新日:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="84d37-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="84d37-106">トポロジビルダーでトポロジを更新した後は、アーカイブを構成して使用する前に、トポロジを中央管理ストアに発行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="84d37-106">After updating your topology in Topology Builder, you must publish the topology to the Central Management store before you can configure and use Archiving.</span></span> <span data-ttu-id="84d37-107">このデータの読み取り専用コピーはトポロジ内のすべてのサーバーにレプリケートされ、すべてのサーバーは、トポロジおよび他の構成の変更と同期された状態で維持されます。</span><span class="sxs-lookup"><span data-stu-id="84d37-107">Read-only copies of the data are replicated to all servers in the topology to keep all servers in sync with topology and other configuration changes.</span></span>

<div>

## <a name="to-publish-your-updated-topology"></a><span data-ttu-id="84d37-108">更新されたトポロジを公開するには</span><span class="sxs-lookup"><span data-stu-id="84d37-108">To publish your updated topology</span></span>

1.  <span data-ttu-id="84d37-109">Lync Server 2013 を実行しているコンピューター、または Lync Server 管理ツールがインストールされているコンピューターで、ローカルユーザーグループのメンバーであるアカウント (または同等のユーザー権限を持つアカウント) を使用してログオンします。</span><span class="sxs-lookup"><span data-stu-id="84d37-109">On a computer that is running Lync Server 2013, or on which the Lync Server administrative tools are installed, log on using an account that is a member of the local Users group (or an account with equivalent user rights).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="84d37-110">トポロジを定義するには、ローカルユーザーグループのメンバーであるアカウントを使用します。ただし、トポロジにサーバーを追加するために必要なトポロジを公開するには、 <STRONG>ドメイン管理者</STRONG> グループと <STRONG>RTCUniversalServerAdmins</STRONG> グループのメンバーであるアカウントを使用する必要があります。さらに、Lync server 2013 ファイルストアで使用しているファイル共有に対してフルコントロールのアクセス許可 (つまり読み取り、書き込み、変更) を持つことができます (つまり、トポロジビルダーは、必要な随意アクセス制御リスト (dacl)、または同等の権限を持つアカウントを構成できます。</span><span class="sxs-lookup"><span data-stu-id="84d37-110">You can define a topology by using an account that is a member of the local Users group, but to publish a topology, which is required to add a server to the topology, you must use an account that is a member of the <STRONG>Domain Admins</STRONG> group and the <STRONG>RTCUniversalServerAdmins</STRONG> group, and that has full control permissions (that is, read, write, and modify) on the file share that you are using for the Lync Server 2013 file store (that is, so that Topology Builder can configure the required discretionary access control list (DACLs), or an account with equivalent rights.</span></span>

    
    </div>

2.  <span data-ttu-id="84d37-111">トポロジービルダーを使用して、前のセクションで作成したトポロジを開きます。</span><span class="sxs-lookup"><span data-stu-id="84d37-111">Open the topology you created in the previous section using Topology Builder.</span></span>

3.  <span data-ttu-id="84d37-112">コンソールツリーで、[ **Lync Server 2013**] を右クリックし、[ **トポロジの公開**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84d37-112">In the console tree, right-click **Lync Server 2013**, and then click **Publish Topology**.</span></span>

4.  <span data-ttu-id="84d37-113">[**トポロジの公開**] ページで、[**次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84d37-113">On the **Publish the topology** page, click **Next**.</span></span>

5.  <span data-ttu-id="84d37-114">[**データベースの作成**] ページで、データベースが選択されていることを確認し、[**次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84d37-114">On the **Create databases** page, verify that the database is selected, and then click **Next**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="84d37-115">データベースを作成するための適切なアクセス許可を持っていない場合、ここでのデータベースの選択を取り消して、適切なアクセス許可を持つ別のユーザーがデータベースを作成できます。</span><span class="sxs-lookup"><span data-stu-id="84d37-115">If you do not have the appropriate permissions to create databases, you can cancel the selection of the database and someone with appropriate permissions can create the database.</span></span> <span data-ttu-id="84d37-116">必要な管理者権限と権限の詳細については、展開ドキュメントの「 <A href="lync-server-2013-deployment-permissions-for-sql-server.md">Lync server 2013 の SQL server の展開権限</A> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="84d37-116">For details about the required administrator rights and permissions, see <A href="lync-server-2013-deployment-permissions-for-sql-server.md">Deployment permissions for SQL Server in Lync Server 2013</A> in the Deployment documentation.</span></span><BR><span data-ttu-id="84d37-117">トポロジビルダーを使用すると、専用の SQL Server サーバー上のデータベースのみをインストールできます。</span><span class="sxs-lookup"><span data-stu-id="84d37-117">Only databases on dedicated SQL Server servers can be installed by using Topology Builder.</span></span> <span data-ttu-id="84d37-118">他のサーバーコンポーネントと連携している SQL Server サーバー上のデータベースは、そのコンピューターのローカルセットアップを実行してインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="84d37-118">Databases on SQL Server servers that are collocated with other server components must be installed by running local setup on that computer.</span></span>

    
    </div>

6.  <span data-ttu-id="84d37-119">[**公開ウィザードの完了**] ページで、トポロジが正常に公開されたことを確認し、[**完了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84d37-119">On the **Publishing wizard complete** page, verify that the topology was successfully published, and then click **Finish**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="84d37-120">トポロジを公開した後、コンテンツをアーカイブする前に、アーカイブのオプションおよびポリシーを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="84d37-120">After publishing the topology, you must configure options and policies for Archiving before any content can be archived.</span></span> <span data-ttu-id="84d37-121">詳細については、「展開ドキュメントの「 <A href="lync-server-2013-configuring-support-for-archiving.md">Lync Server 2013 でアーカイブのサポートを構成する</A> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="84d37-121">For details, see <A href="lync-server-2013-configuring-support-for-archiving.md">Configuring support for Archiving in Lync Server 2013</A> in the Deployment documentation.</span></span>

    
    <span data-ttu-id="84d37-122"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="84d37-122"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

