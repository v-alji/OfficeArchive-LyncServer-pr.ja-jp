---
title: 'Lync Server 2013: アーカイブのグローバルポリシーを構成する'
description: 'Lync Server 2013: アーカイブのグローバルポリシーを構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring the global policy for Archiving
ms:assetid: 58341d6b-c3ff-4dd9-b1c7-0048f33861ca
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204906(v=OCS.15)
ms:contentKeyID: 48184192
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a8f8125f458c4269626e0b1c929f2acb1a8de0b9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432570"
---
# <a name="configuring-the-global-policy-for-archiving-in-lync-server-2013"></a><span data-ttu-id="f7b77-103">Lync Server 2013 でアーカイブ用のグローバルポリシーを構成する</span><span class="sxs-lookup"><span data-stu-id="f7b77-103">Configuring the global policy for Archiving in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f7b77-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f7b77-104">

<span> </span></span></span>

<span data-ttu-id="f7b77-105">_**最終更新日:** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="f7b77-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="f7b77-106">フロントエンドサーバーを展開すると、Lync Server によってアーカイブ用のグローバルポリシーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="f7b77-106">When you deploy your Front End Servers, Lync Server creates a global policy for Archiving.</span></span> <span data-ttu-id="f7b77-107">既定では、アーカイブはグローバルポリシーで無効になっています。</span><span class="sxs-lookup"><span data-stu-id="f7b77-107">By default, Archiving is disabled in the global policy.</span></span> <span data-ttu-id="f7b77-108">グローバルポリシーは、サイトまたはユーザーのポリシーをセットアップしてグローバルポリシーを上書きするか、一部またはすべてのユーザーに対して Microsoft Exchange の統合を使用している場合を除き、展開全体の内部および外部通信でアーカイブを有効にするかどうかを制御します。</span><span class="sxs-lookup"><span data-stu-id="f7b77-108">The global policy controls whether archiving is enabled for internal and external communications for your entire deployment, unless you set up site or user policies, which override the global policy, or if you use Microsoft Exchange integration for some or all of your users.</span></span> <span data-ttu-id="f7b77-109">Microsoft Exchange 統合を使用している場合、グローバルポリシーは、Exchange 2013 を使っているユーザーには適用されず、メールボックス In-Place 保持されます。</span><span class="sxs-lookup"><span data-stu-id="f7b77-109">If you use Microsoft Exchange integration, the global policy does not apply to any users who are homed on Exchange 2013 and have the mailboxes put on In-Place Hold.</span></span>

<span data-ttu-id="f7b77-110">グローバル、サイト、ユーザーのポリシーの階層など、アーカイブポリシーの動作について詳しくは、「 [Lync Server 2013 でのアーカイブのしくみ](lync-server-2013-how-archiving-works.md) 」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="f7b77-110">For details about how Archiving policies work, including the hierarchy for global, site, and user policies, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f7b77-111">展開時に Microsoft Exchange の統合を有効にすると、exchange 2013 を使用しているユーザーに対してアーカイブが有効になっているかどうかを制御するための Exchange In-Place ホールドポリシーが適用され、メールボックスは In-Place 保留になります。</span><span class="sxs-lookup"><span data-stu-id="f7b77-111">If you enable Microsoft Exchange integration for your deployment, Exchange In-Place Hold policies control whether archiving is enabled for the users who are homed on Exchange 2013 and have their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="f7b77-112">詳細については、展開ドキュメントで <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Exchange Server との統合を使用する場合の「Lync server 2013 でアーカイブするためのポリシーを設定する</A> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f7b77-112">For details, see <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</A> in the Deployment documentation.</span></span><BR><span data-ttu-id="f7b77-113">アーカイブを有効にする前に、アーカイブ構成ですべての適切なオプションを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7b77-113">You should specify all appropriate options in the Archiving configurations before enabling Archiving.</span></span> <span data-ttu-id="f7b77-114">詳細については、展開ドキュメントの「 <A href="lync-server-2013-configuring-archiving-options.md">Lync Server 2013 でアーカイブオプションを構成する</A> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f7b77-114">For details, see <A href="lync-server-2013-configuring-archiving-options.md">Configuring Archiving options in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="to-configure-the-global-policy-for-archiving-when-using-lync-server-archiving-databases"></a><span data-ttu-id="f7b77-115">Lync Server アーカイブデータベースを使用するときに、アーカイブ用のグローバルポリシーを構成するには</span><span class="sxs-lookup"><span data-stu-id="f7b77-115">To configure the global policy for archiving when using Lync Server Archiving databases</span></span>

1.  <span data-ttu-id="f7b77-116">CsArchivingAdministrator または CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="f7b77-116">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="f7b77-117">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server 2013 コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="f7b77-117">Open a browser window, and then enter the Admin URL to open the Lync Server 2013 Control Panel.</span></span> <span data-ttu-id="f7b77-118">Lync Server 2013 コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="f7b77-118">For details about the different methods you can use to start Lync Server 2013 Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="f7b77-119">左側のナビゲーション バーで、[**監視とアーカイブ**] をクリックし、[**アーカイブ ポリシー**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f7b77-119">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Policy**.</span></span>

4.  <span data-ttu-id="f7b77-120">[**アーカイブ ポリシー**] ページで、[**グローバル**]、[**編集**]、[**詳細の表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f7b77-120">On the **Archiving Policy** page, click **Global**, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="f7b77-121">[**アーカイブ ポリシーの編集 - グローバル**] で、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="f7b77-121">In **Edit Archiving Policy - Global**, do the following:</span></span>
    
      - <span data-ttu-id="f7b77-122">"グローバル" という既定の名前を使用しない場合は、[**名前**] にグローバル ポリシーの新しい名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="f7b77-122">In **Name**, if you do not want to use the default name of Global, specify a new name for the global policy.</span></span>
    
      - <span data-ttu-id="f7b77-123">[**説明**] に、そのポリシーの内容に関する情報を入力します (たとえば、「<部署名> のグローバル ポリシー」など)。</span><span class="sxs-lookup"><span data-stu-id="f7b77-123">In **Description**, provide information about what the policy is (for example, Global policy for *divisionName*).</span></span>
    
      - <span data-ttu-id="f7b77-124">サイト ポリシーまたはユーザー ポリシーによって特に制御されていないすべてのサイトとユーザーの内部通信のアーカイブを制御するには、[**内部通信のアーカイブ**] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="f7b77-124">To control archiving of internal communications for all sites and users not specifically controlled through a site policy or user policy, select or clear the **Archive internal communications** check box.</span></span>
    
      - <span data-ttu-id="f7b77-125">サイト ポリシーまたはユーザー ポリシーによって特に制御されていないすべてのサイトとユーザーの外部通信のアーカイブを制御するには、[**外部通信をアーカイブする**] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="f7b77-125">To control archiving of external communications for all sites and users not specifically controlled through a site policy or user policy, select or clear the **Archive external communications** check box.</span></span>

6.  <span data-ttu-id="f7b77-126">[**確定**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f7b77-126">Click **Commit**.</span></span>

<span data-ttu-id="f7b77-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f7b77-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

