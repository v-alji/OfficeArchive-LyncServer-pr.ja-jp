---
title: 'Lync Server 2013: アーカイブのためのサイトポリシーを設定する'
description: 'Lync Server 2013: アーカイブ用のサイトポリシーを設定します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up site policies for Archiving
ms:assetid: dc2ea206-8b9c-44dd-a479-efb217593c89
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205325(v=OCS.15)
ms:contentKeyID: 48185613
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 27e5b80b7f62ddc18d418415307457c7f2c4010d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441691"
---
# <a name="setting-up-site-policies-for-archiving-in-lync-server-2013"></a><span data-ttu-id="a8c0d-103">Lync Server 2013 でアーカイブ用のサイトポリシーを設定する</span><span class="sxs-lookup"><span data-stu-id="a8c0d-103">Setting up site policies for Archiving in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a8c0d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a8c0d-104">

<span> </span></span></span>

<span data-ttu-id="a8c0d-105">_**最終更新日:** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="a8c0d-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="a8c0d-106">各サイトのアーカイブポリシーを作成して構成することで、特定のサイトのアーカイブを有効または無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="a8c0d-106">You can enable or disable Archiving for specific sites by creating and configuring an Archiving policy for each of those sites.</span></span> <span data-ttu-id="a8c0d-107">サイト ポリシーはグローバル ポリシーより優先されますが、サイト ポリシーよりもユーザー ポリシーが優先されます。</span><span class="sxs-lookup"><span data-stu-id="a8c0d-107">A site policy overrides the global policy, but user policies override site policies.</span></span> <span data-ttu-id="a8c0d-108">アーカイブポリシーが適用されるのは、Microsoft Exchange 統合を使用していない場合、または Microsoft Exchange 統合を使用していないが、Exchange 2013 を使っていないユーザーがいて、メールボックスが In-Place 保留になっている場合のみです。</span><span class="sxs-lookup"><span data-stu-id="a8c0d-108">Archiving policies only apply if you do not use Microsoft Exchange integration or, if you do use Microsoft Exchange integration, but have some users who are not homed on Exchange 2013 and have their mailboxes put on In-Place Hold.</span></span>

<span data-ttu-id="a8c0d-109">グローバル、サイト、ユーザーのポリシーの階層など、アーカイブポリシーの動作について詳しくは、「 [Lync Server 2013 でのアーカイブのしくみ](lync-server-2013-how-archiving-works.md) 」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="a8c0d-109">For details about how Archiving policies work, including the hierarchy for global, site, and user policies, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a8c0d-110">展開時に Microsoft Exchange の統合を有効にすると、exchange 2013 を使用しているユーザーに対してアーカイブが有効になっているかどうかを制御するための Exchange In-Place ホールドポリシーが適用され、メールボックスは In-Place 保留になります。</span><span class="sxs-lookup"><span data-stu-id="a8c0d-110">If you enable Microsoft Exchange integration for your deployment, Exchange In-Place Hold policies control whether archiving is enabled for the users who are homed on Exchange 2013 and have their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="a8c0d-111">詳細については、展開ドキュメントで <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Exchange Server との統合を使用する場合の「Lync server 2013 でアーカイブするためのポリシーを設定する</A> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a8c0d-111">For details, see <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</A> in the Deployment documentation.</span></span><BR><span data-ttu-id="a8c0d-112">アーカイブ ポリシーで内部または外部の通信のアーカイブを有効にする前に、アーカイブ構成のすべてのオプションを適切に指定してください。</span><span class="sxs-lookup"><span data-stu-id="a8c0d-112">You should specify all appropriate options in the Archiving configurations before enabling Archiving of internal or external communications in the Archiving policies.</span></span> <span data-ttu-id="a8c0d-113">詳細については、展開ドキュメントの「 <A href="lync-server-2013-configuring-archiving-options.md">Lync Server 2013 でアーカイブオプションを構成する</A> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a8c0d-113">For details, see <A href="lync-server-2013-configuring-archiving-options.md">Configuring Archiving options in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="to-create-an-archiving-policy-for-a-site"></a><span data-ttu-id="a8c0d-114">サイトのアーカイブポリシーを作成するには</span><span class="sxs-lookup"><span data-stu-id="a8c0d-114">To create an archiving policy for a site</span></span>

1.  <span data-ttu-id="a8c0d-115">CsArchivingAdministrator または CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="a8c0d-115">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="a8c0d-116">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server 2013 コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="a8c0d-116">Open a browser window, and then enter the Admin URL to open the Lync Server 2013 Control Panel.</span></span>

3.  <span data-ttu-id="a8c0d-117">左側のナビゲーション バーで、[**監視とアーカイブ**] をクリックし、[**アーカイブ ポリシー**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a8c0d-117">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Policy**.</span></span>
    
    <span data-ttu-id="a8c0d-118">グローバル、サイト、ユーザーのポリシーの階層など、アーカイブポリシーの動作について詳しくは、「 [Lync Server 2013 でのアーカイブのしくみ](lync-server-2013-how-archiving-works.md) 」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="a8c0d-118">For details about how Archiving policies work, including the hierarchy for global, site, and user policies, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) Planning documentation, Deployment documentation, or Operations documentation.</span></span>

4.  <span data-ttu-id="a8c0d-119">[**新規作成**] をクリックし、[**サイト ポリシー**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a8c0d-119">Click **New**, and then click **Site policy**.</span></span>

5.  <span data-ttu-id="a8c0d-120">[**サイトの選択**] でポリシーを適用するサイトをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a8c0d-120">In **Select a site**, click the site to which the policy is to be applied.</span></span>

6.  <span data-ttu-id="a8c0d-121">[**新しいアーカイブ ポリシー**] で、次の操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="a8c0d-121">In **New Archiving Policy**, do the following:</span></span>
    
      - <span data-ttu-id="a8c0d-122">[**名前**] で、サイト ポリシーの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="a8c0d-122">In **Name**, specify the name for the site policy.</span></span>
    
      - <span data-ttu-id="a8c0d-123">[**説明**] にサイト ポリシーに関する情報を入力します (「Redmond のサイト ポリシー」など)。</span><span class="sxs-lookup"><span data-stu-id="a8c0d-123">In **Description**, provide information about what the site policy is (for example, site policy for Redmond).</span></span>
    
      - <span data-ttu-id="a8c0d-124">指定したサイトの内部通信のアーカイブを制御するには、[**内部通信をアーカイブする**] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="a8c0d-124">To control archiving of internal communications for the specified site, select or clear the **Archive internal communications** check box.</span></span>
    
      - <span data-ttu-id="a8c0d-125">指定したサイトの外部通信のアーカイブを制御するには、[**外部通信をアーカイブする**] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="a8c0d-125">To control archiving of external communications for the specified site, select or clear the **Archive external communications** check box.</span></span>

7.  <span data-ttu-id="a8c0d-126">[**確定**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a8c0d-126">Click **Commit**.</span></span>

<span data-ttu-id="a8c0d-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a8c0d-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

