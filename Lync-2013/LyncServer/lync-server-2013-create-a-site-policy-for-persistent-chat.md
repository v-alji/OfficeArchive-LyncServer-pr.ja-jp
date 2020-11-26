---
title: 'Lync Server 2013: 常設チャットのサイト ポリシーを作成する'
description: 'Lync Server 2013: 常設チャット用のサイトポリシーを作成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create a site policy for Persistent Chat
ms:assetid: 1327ff5c-b859-4010-a240-e0b2b084b5bd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204693(v=OCS.15)
ms:contentKeyID: 48183470
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0f1cfbcffd98e7bdb813a4113345abf17f5b37e5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432108"
---
# <a name="create-a-site-policy-for-persistent-chat-in-lync-server-2013"></a><span data-ttu-id="7e103-103">Lync Server 2013 で常設チャットのサイト ポリシーを作成する</span><span class="sxs-lookup"><span data-stu-id="7e103-103">Create a site policy for Persistent Chat in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7e103-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7e103-104">

<span> </span></span></span>

<span data-ttu-id="7e103-105">_**最終更新日:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="7e103-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="7e103-106">展開したサイトごとに、サイト固有の常設チャットポリシーを作成できます。</span><span class="sxs-lookup"><span data-stu-id="7e103-106">For each site you have deployed, you can create a site-specific Persistent Chat policy.</span></span>

<span data-ttu-id="7e103-107">サイト ポリシーの構成はグローバル ポリシーよりも優先されますが、サイト ポリシーで指定されたサイトだけが対象となります。</span><span class="sxs-lookup"><span data-stu-id="7e103-107">The configuration in the site policy overrides the global policy, but only for the specific site covered by the site policy.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="7e103-108">常設チャットサーバーを構成して使用するには、最初にトポロジビルダーを使用して、トポロジに常設チャットサーバーサポートを追加してから、トポロジを発行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e103-108">To configure and use Persistent Chat Server, you must first use Topology Builder to add Persistent Chat Server support to the topology, and then publish the topology.</span></span> <span data-ttu-id="7e103-109">詳細については、展開ドキュメントの「 <A href="lync-server-2013-adding-persistent-chat-server-to-your-deployment.md">Lync server 2013 での展開への常設チャットサーバーの追加</A> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7e103-109">For details, see <A href="lync-server-2013-adding-persistent-chat-server-to-your-deployment.md">Adding Persistent Chat Server to your deployment in Lync Server 2013</A> in the Deployment documentation.</span></span><BR><span data-ttu-id="7e103-110">常設チャットサーバーの構成設定を構成するには、展開ドキュメントの「 <A href="lync-server-2013-configure-persistent-chat-server-options-globally-or-for-persistent-chat-server-pool.md">Lync server 2013 で常設チャットサーバーのオプションをグローバルまたは常設チャットサーバープールに構成</A> する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7e103-110">To configure Persistent Chat Server configuration settings, see <A href="lync-server-2013-configure-persistent-chat-server-options-globally-or-for-persistent-chat-server-pool.md">Configure Persistent Chat Server options globally or for Persistent Chat Server pool in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="to-create-a-persistent-chat-policy-for-a-site"></a><span data-ttu-id="7e103-111">サイトの常設チャットポリシーを作成するには</span><span class="sxs-lookup"><span data-stu-id="7e103-111">To create a Persistent Chat policy for a site</span></span>

1.  <span data-ttu-id="7e103-112">CsPersistentChatAdministrator、CsAdministrator、または CsUserAdministrator の役割に割り当てられているユーザーから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="7e103-112">From a user account that is assigned to the CsPersistentChatAdministrator, CsAdministrator, or CsUserAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="7e103-113">[ **スタート** ] メニューから [Lync Server コントロールパネル] を選択するか、ブラウザーウィンドウを開き、管理 URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="7e103-113">From the **Start** menu, select the Lync Server Control Panel or open a browser window, and then enter the Admin URL.</span></span> <span data-ttu-id="7e103-114">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="7e103-114">For details about the different methods that you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="7e103-115">左側のナビゲーション バーで [**常設チャット**] をクリックし、[**常設チャットのポリシー**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7e103-115">In the left navigation bar, click **Persistent Chat**, and then click **Persistent Chat Policy**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="7e103-116">Windows PowerShell コマンドレットを使うこともできます。</span><span class="sxs-lookup"><span data-stu-id="7e103-116">You can also use Windows PowerShell cmdlets.</span></span> <span data-ttu-id="7e103-117">詳細については、展開ドキュメントの「 <A href="configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md">Windows PowerShell コマンドレットを使用して常設チャットサーバーを構成</A> する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7e103-117">For details, see <A href="configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md">Configuring Persistent Chat Server by using Windows PowerShell cmdlets</A> in the Deployment documentation.</span></span>

    
    </div>

4.  <span data-ttu-id="7e103-118">[**新規作成**] をクリックし、[**サイト ポリシー**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7e103-118">Click **New**, and then click **Site policy**.</span></span>

5.  <span data-ttu-id="7e103-119">[**サイトの選択**] でポリシーを適用するサイトをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7e103-119">In **Select a Site**, click the site to which the policy is to be applied.</span></span>

6.  <span data-ttu-id="7e103-120">[**新規 常設チャットのポリシー**] で、次の操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="7e103-120">In **New Persistent Chat Policy**, do the following:</span></span>
    
      - <span data-ttu-id="7e103-121">[**名前**] で、新しいサイト ポリシーの名前 (Redmond など) を指定します。</span><span class="sxs-lookup"><span data-stu-id="7e103-121">In **Name**, specify a name for the new site policy (for example, Redmond).</span></span>
    
      - <span data-ttu-id="7e103-122">[**説明**] にサイト ポリシーの内容の詳細 (「Redmond のチャット ルーム ポリシー」など) を入力します。</span><span class="sxs-lookup"><span data-stu-id="7e103-122">In **Description**, provide details about what the site policy is (for example, chat room policy for Redmond).</span></span>
    
      - <span data-ttu-id="7e103-123">サイト ポリシーによって特に制御されていないすべてのサイトの常設チャットを制御するには、[**常設チャットを有効にする**] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="7e103-123">To control Persistent Chat for all sites not specifically controlled through a site policy, select or clear the **Enable Persistent Chat** check box.</span></span>

7.  <span data-ttu-id="7e103-124">[**コミット**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7e103-124">Click **Commit**.</span></span>

<span data-ttu-id="7e103-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7e103-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

