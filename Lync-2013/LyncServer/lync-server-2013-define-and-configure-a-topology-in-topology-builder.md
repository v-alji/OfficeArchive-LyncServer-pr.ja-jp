---
title: 'Lync Server 2013: トポロジ ビルダーでのトポロジの定義と構成'
description: 'Lync Server 2013: トポロジビルダーでトポロジを定義して構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Define and configure a topology in Topology Builder
ms:assetid: 99231ff5-1c21-432b-ad65-8675fcd484f9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398788(v=OCS.15)
ms:contentKeyID: 48184953
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 83a1f29ec78cf7cfd3856d3f1aa87a22dc0bbe00
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431058"
---
# <a name="define-and-configure-a-topology-in-topology-builder-for-lync-server-2013"></a><span data-ttu-id="83a7a-103">Lync Server 2013 のトポロジ ビルダーでのトポロジの定義と構成</span><span class="sxs-lookup"><span data-stu-id="83a7a-103">Define and configure a topology in Topology Builder for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="83a7a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="83a7a-104">

<span> </span></span></span>

<span data-ttu-id="83a7a-105">_**最終更新日:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="83a7a-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="83a7a-106">トポロジビルダーを実行して新しいトポロジを定義したり、既存のトポロジを変更したりするには、ローカル管理者または特権ドメイングループのメンバーシップは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="83a7a-106">Running Topology Builder to define a new topology or to modify an existing topology does not require membership in a local administrator or privileged domain group.</span></span> <span data-ttu-id="83a7a-107">トポロジビルダーは、構成要件に基づいて、Enterprise Edition フロントエンドプールまたは標準エディションのトポロジを定義するために必要な手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="83a7a-107">Topology Builder guides you through the steps necessary to define your topology for an Enterprise Edition Front End pool or a Standard Edition, based on your configuration requirements.</span></span>

<span data-ttu-id="83a7a-108">サーバーに Lync Server 2013 をインストールするには、トポロジビルダーを使用してトポロジを完了して公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="83a7a-108">You must use Topology Builder to complete and publish the topology before you can install Lync Server 2013 on servers.</span></span> <span data-ttu-id="83a7a-109">次の手順では、新しいトポロジを定義するために必要な手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="83a7a-109">The following procedure includes the steps required to define a new topology.</span></span>

<div>

## <a name="to-define-a-topology"></a><span data-ttu-id="83a7a-110">トポロジを定義するには</span><span class="sxs-lookup"><span data-stu-id="83a7a-110">To define a topology</span></span>

1.  <span data-ttu-id="83a7a-111">トポロジビルダーを開始します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server Topology Builder**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="83a7a-111">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="83a7a-112">[トポロジビルダー] で [ **新しいトポロジ**] を選びます。</span><span class="sxs-lookup"><span data-stu-id="83a7a-112">In Topology Builder, select **New Topology**.</span></span> <span data-ttu-id="83a7a-113">トポロジを保存する場所とファイル名を入力するように求められます。</span><span class="sxs-lookup"><span data-stu-id="83a7a-113">You are prompted for a location and file name for saving the topology.</span></span> <span data-ttu-id="83a7a-114">トポロジファイルにわかりやすい名前を付け、tbxml の既定の拡張子をそのまま使用します。</span><span class="sxs-lookup"><span data-stu-id="83a7a-114">Give the topology file a meaningful name and accept the default extension of .tbxml.</span></span> <span data-ttu-id="83a7a-115">**[OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="83a7a-115">Click **OK**.</span></span>

3.  <span data-ttu-id="83a7a-116">新しいトポロジ XML ファイルを保存する場所に移動し、ファイルの名前を入力して、[ **保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="83a7a-116">Navigate to the location where you want to save the new topology XML file, enter a name for the file, and then click **Save**.</span></span>

4.  <span data-ttu-id="83a7a-117">[ **プライマリドメインの定義** ] ページで、組織のプライマリ SIP ドメインの名前を入力し、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="83a7a-117">On the **Define the primary domain** page, enter the name of the primary SIP domain for your organization, and then click **Next**.</span></span>

5.  <span data-ttu-id="83a7a-118">[ **追加でサポートされるドメインの指定** ] ページで、必要に応じて追加ドメインの名前を入力し、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="83a7a-118">On the **Specify additional supported domains** page, enter the names of additional domains, if any, and then click **Next**.</span></span>

6.  <span data-ttu-id="83a7a-119">[ **最初のサイトの定義** ] ページで、最初のサイトの名前と説明を入力し、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="83a7a-119">On the **Define the first site** page, enter a name and a description for the first site, and then click **Next**.</span></span>

7.  <span data-ttu-id="83a7a-120">[ **サイトの詳細の指定** ] ページで、サイトの場所情報を入力し、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="83a7a-120">On the **Specify site details** page, enter the location information for the site, and then click **Next**.</span></span>

8.  <span data-ttu-id="83a7a-121">[ **新しいトポロジの定義が完了しました** ] ページで、[ **このウィザードを閉じるときに新しいフロントエンドウィザードを開く** ] チェックボックスがオンになっていることを確認し、[ **完了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="83a7a-121">On the **New topology was successfully defined** page, make sure the **Open the New Front End Wizard when this wizard closes** check box is selected, and then click **Finish**.</span></span>

<span data-ttu-id="83a7a-122">トポロジを定義して保存したら、新しいフロントエンドウィザードを使って、サイトのフロントエンドプールまたは Standard Edition サーバーを定義します。</span><span class="sxs-lookup"><span data-stu-id="83a7a-122">After you’ve defined and saved the topology, use the New Front End Wizard to define a Front End pool or Standard Edition server for your site.</span></span> <span data-ttu-id="83a7a-123">詳細について [は、「Lync server 2013 でフロントエンドプールまたは Standard Edition サーバーを定義して構成](lync-server-2013-define-and-configure-a-front-end-pool-or-standard-edition-server.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="83a7a-123">For details, see [Define and configure a Front End pool or Standard Edition server in Lync Server 2013](lync-server-2013-define-and-configure-a-front-end-pool-or-standard-edition-server.md).</span></span>

<span data-ttu-id="83a7a-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="83a7a-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

