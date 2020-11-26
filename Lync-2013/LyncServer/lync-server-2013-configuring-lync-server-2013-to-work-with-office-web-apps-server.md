---
title: Office Web Apps サーバーで動作するように Lync Server 2013 を構成する
description: Office Web Apps サーバーと連携するように Lync Server 2013 を構成する。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Lync Server 2013 to work with Office Web Apps Server
ms:assetid: 6231e519-9010-4ff9-b5a6-b5859c2b3e11
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204944(v=OCS.15)
ms:contentKeyID: 48184288
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 07e53500e0ad272c81340c25946f5b7f8e72a121
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433014"
---
# <a name="configuring-lync-server-2013-to-work-with-office-web-apps-server"></a><span data-ttu-id="12e2f-103">Office Web Apps サーバーで動作するように Lync Server 2013 を構成する</span><span class="sxs-lookup"><span data-stu-id="12e2f-103">Configuring Lync Server 2013 to work with Office Web Apps Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="12e2f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="12e2f-104">

<span> </span></span></span>

<span data-ttu-id="12e2f-105">_**最終更新日:** 2013-04-22_</span><span class="sxs-lookup"><span data-stu-id="12e2f-105">_**Topic Last Modified:** 2013-04-22_</span></span>

<span data-ttu-id="12e2f-106">Lync Server 2013 で Office Web Apps サーバーを使用するように構成するには、Office Web Apps サーバーを展開して構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="12e2f-106">Before you can configure Lync Server 2013 to use Office Web Apps Server, Office Web Apps Server must be deployed and configured.</span></span> <span data-ttu-id="12e2f-107">1つの Office Web Apps サーバーをインストールして構成する方法について詳しくは、「office web apps サーバー **と office Web apps** をインストールして構成する」をご覧ください。または、Office Web Apps サーバーファームをインストールして、高可用性のために構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="12e2f-107">See the document **Guide to Deploying Office Web Apps Server and Office Web Apps** for detail information on how to install and configure a single Office Web Apps Server, or for information on how to install and configure an Office Web Apps Server Farm for high availability.</span></span>

<span data-ttu-id="12e2f-108">Office Web Apps サーバーが正常にインストールされ、Web ファームが正しく構成されたら、新しいサーバーと通信するために Lync Server を構成する必要があります。これは、Office Web Apps サーバー検出 URL を Lync Server トポロジに追加することによって行われます。</span><span class="sxs-lookup"><span data-stu-id="12e2f-108">After Office Web Apps Server has been successfully installed and your Web farm correctly configured, you must then configure Lync Server to communicate with the new server; this is done by adding the Office Web Apps Server discovery URL to your Lync Server topology.</span></span> <span data-ttu-id="12e2f-109">トポロジに Office Web Apps サーバーを追加するには、次の手順を行います。</span><span class="sxs-lookup"><span data-stu-id="12e2f-109">To add Office Web Apps Server to your topology, complete the following steps:</span></span>

1.  <span data-ttu-id="12e2f-110">[ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server Topology Builder**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="12e2f-110">Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="12e2f-111">[**トポロジ ビルダー**] ダイアログ ボックスで、[**既存の展開からトポロジをダウンロードする**] を選択して [**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="12e2f-111">In the **Topology Builder** dialog box, select **Download Topology from existing deployment** and then click **OK**.</span></span>

3.  <span data-ttu-id="12e2f-p103">[**トポロジに名前を付けて保存**] ダイアログ ボックスで、トポロジ ドキュメントの名前 (例: **PreWebAppsServerTopology**) を [**ファイル名**] ボックスに入力し、[**保存**] をクリックします。新しいトポロジで問題が発生した場合、後でこのトポロジを取得して再発行できます。</span><span class="sxs-lookup"><span data-stu-id="12e2f-p103">In the **Save Topology As** dialog box, type a name for your topology document (for example, **PreWebAppsServerTopology**) in the **File name** box and then click **Save**. This topology can later be retrieved and republished if you encounter problems with your new topology.</span></span>

4.  <span data-ttu-id="12e2f-114">[トポロジビルダー] で、[ **Lync Server 2013**] を展開し、サイトの名前を展開し、[ **Enterprise Edition のフロントエンドプール**] を展開して、いずれかのプールの名前を右クリックし、[ **プロパティの編集**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="12e2f-114">In Topology Builder, expand **Lync Server 2013**, expand the name of your site, expand **Enterprise Edition Front End pools**, right-click the name of one of your pools, and then click **Edit Properties**.</span></span>

5.  <span data-ttu-id="12e2f-115">[**プロパティの編集**] ダイアログ ボックスの [**全般**] タブで、[**Office Web Apps サーバーの関連付け**] という見出しを探し、[**新規作成**] をクリックします (または、ドロップダウン リストから既存の Office Web Apps サーバーを選択します)。</span><span class="sxs-lookup"><span data-stu-id="12e2f-115">In the **Edit Properties** dialog box, on the **General** tab, find the heading **Associate Office Web Apps Server** and then click **New** (or select an existing Office Web Apps Server from the drop-down list).</span></span>

6.  <span data-ttu-id="12e2f-116">[**新しい Office Web Apps サーバーの定義**] ダイアログ ボックスで、Office Web Apps サーバー コンピューターの完全修飾ドメイン名 (FQDN) を [**Office Web Apps サーバーの FQDN**] ボックスに入力します。これを行うと、Office Web Apps サーバー検出の URL が [**Office Web Apps サーバー検出の URL**] ボックスに自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="12e2f-116">In the **Define New Office Web Apps Server** dialog box, type the fully qualified domain name (FQDN) of your Office Web Apps Server computer in the **Office Web Apps Server FQDN** box; when you do this, your Office Web Apps Server discovery URL should automatically be entered into the **Office Web Apps Server discovery URL** box.</span></span>
    
    <span data-ttu-id="12e2f-117">Office Web Apps サーバーがオンプレミスで、Lync Server 2013 と同じネットワークゾーンにインストールされている場合は、[ **Office Web Apps サーバーを外部ネットワーク (つまり、境界/インターネット) に展開** する] オプションを選択しないでください。</span><span class="sxs-lookup"><span data-stu-id="12e2f-117">If the Office Web Apps Server is installed on-premises and in the same network zone as Lync Server 2013 then the option **Office Web Apps Server is deployed in an external network (that is, perimeter/Internet)** should not be selected.</span></span>
    
    <span data-ttu-id="12e2f-118">Office Web Apps サーバーを内部ファイアウォールの外側に展開する場合は、[**Office Web Apps サーバーは外部ネットワークで展開 (境界ネットワークまたはインターネット)**] オプションをオンにします。</span><span class="sxs-lookup"><span data-stu-id="12e2f-118">If the Office Web Apps Server is deployed outside your internal firewall, then select the option **Office Web Apps Server is deployed in an external network (that is, perimeter/Internet)**.</span></span>

7.  <span data-ttu-id="12e2f-119">[**新しい Office Web Apps サーバーの定義**] ダイアログ ボックスで、[**OK**] をクリックし、[**プロパティの編集**] ダイアログ ボックスで [**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="12e2f-119">In the **Define New Office Web Apps Server** dialog box, click **OK**, and then click **OK** in the **Edit Properties** dialog box.</span></span> <span data-ttu-id="12e2f-120">Office Web Apps の検出 URL がプールの関連付けの1つとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="12e2f-120">The Office Web Apps discovery URL will then be listed as one of the pool's Associations.</span></span>

<span data-ttu-id="12e2f-121">Office Web Apps サーバーに関連付ける必要がある各プールに対してこのプロセスを繰り返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="12e2f-121">You will have to repeat this process for each pool that needs to be associated with your Office Web Apps Server.</span></span>

<span data-ttu-id="12e2f-122">トポロジに探索 URL を追加した後、この更新されたトポロジを公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="12e2f-122">After you have added the discovery URL to the topology you must then publish this updated topology.</span></span> <span data-ttu-id="12e2f-123">これを行うには、トポロジ ビルダーで次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="12e2f-123">To do that in Topology Builder:</span></span>

1.  <span data-ttu-id="12e2f-124">[**操作**] をクリックし、[**トポロジの公開**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="12e2f-124">Click **Action** and then click **Publish Topology**.</span></span>

2.  <span data-ttu-id="12e2f-125">トポロジの公開ウィザードの [**トポロジの公開**] ページで、[**次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="12e2f-125">In the Publish Topology wizard, on the **Publish the Topology** page, click **Next**.</span></span>

3.  <span data-ttu-id="12e2f-126">[**公開ウィザードの完了**] ページで、[**完了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="12e2f-126">On the **Publishing wizard complete** page, click **Finish**.</span></span>

4.  <span data-ttu-id="12e2f-127">トポロジ ビルダーを閉じます。</span><span class="sxs-lookup"><span data-stu-id="12e2f-127">Close Topology Builder.</span></span>

<span data-ttu-id="12e2f-128"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="12e2f-128"></div>

<span> </span>

</div>

</div>

</span></span></div>

