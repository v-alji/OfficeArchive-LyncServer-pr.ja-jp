---
title: 'Lync Server 2013: 禁止された外部ドメイン向けサポートの構成'
description: 'Lync Server 2013: ブロックされた外部ドメインのサポートを構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure support for blocked external domains
ms:assetid: 49103138-e1ab-42bf-91aa-57cf23bbf260
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ619176(v=OCS.15)
ms:contentKeyID: 49733638
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 81c2c76dc32dd5e8d458dad4e91ff375d2ab005c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433676"
---
# <a name="configure-support-for-blocked-external-domains-in-lync-server-2013"></a><span data-ttu-id="375c0-103">Lync Server 2013 での禁止された外部ドメイン向けサポートの構成</span><span class="sxs-lookup"><span data-stu-id="375c0-103">Configure support for blocked external domains in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="375c0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="375c0-104">

<span> </span></span></span>

<span data-ttu-id="375c0-105">_**最終更新日:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="375c0-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="375c0-106">フェデレーションパートナーのサポートを構成している場合は、どのドメインを組織とのフェデレーションからブロックするかを管理できます。</span><span class="sxs-lookup"><span data-stu-id="375c0-106">If you have configured support for federated partners, you can manage which domains will be blocked from federating with your organization.</span></span> <span data-ttu-id="375c0-107">ブロックされたドメインの一覧はブロックリスト (許可されていない明示的なエントリの一覧) として機能し、このオプションを有効にしている場合はフェデレーションドメインの検出に適用されます。</span><span class="sxs-lookup"><span data-stu-id="375c0-107">The list of blocked domains will act as a block list (listing of explicit entries that are not to be allowed) and will apply in federated domain discovery, if you have this option enabled.</span></span> <span data-ttu-id="375c0-108">詳細については、「 [Lync Server 2013 でフェデレーションパートナーの検出を有効または無効](lync-server-2013-enable-or-disable-discovery-of-federation-partners.md)にする」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="375c0-108">For details, see [Enable or disable discovery of federation partners in Lync Server 2013](lync-server-2013-enable-or-disable-discovery-of-federation-partners.md).</span></span>

<span data-ttu-id="375c0-109">1つ以上の外部ドメインをブロックして組織に接続します。</span><span class="sxs-lookup"><span data-stu-id="375c0-109">Block one or more external domains from connecting to your organization.</span></span> <span data-ttu-id="375c0-110">そのためには、ブロックされたドメインの一覧にドメインを追加します。</span><span class="sxs-lookup"><span data-stu-id="375c0-110">To do this, add the domain to the list of blocked domains.</span></span>

<div>

## <a name="to-add-an-external-domain-to-the-list-of-blocked-domains"></a><span data-ttu-id="375c0-111">ブロックされたドメインの一覧に外部ドメインを追加するには</span><span class="sxs-lookup"><span data-stu-id="375c0-111">To add an external domain to the list of blocked domains</span></span>

1.  <span data-ttu-id="375c0-112">RTCUniversalServerAdmins グループ (または同等のユーザー権限を持つグループ) のメンバーであるユーザー アカウントまたは CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="375c0-112">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="375c0-113">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="375c0-113">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="375c0-114">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="375c0-114">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="375c0-115">左側のナビゲーションバーで、[ **外部ユーザーアクセス**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="375c0-115">In the left navigation bar, click **External User Access**.</span></span>

4.  <span data-ttu-id="375c0-116">[ **フェデレーションドメイン**] をクリックし、[ **新規作成**] をクリックして、[ **禁止ドメイン**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="375c0-116">Click **Federated Domains**, click **New**, and then click **Blocked domain**.</span></span>

5.  <span data-ttu-id="375c0-117">**新しいフェデレーションドメイン** で、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="375c0-117">In **New Federated Domains**, do the following:</span></span>
    
      - <span data-ttu-id="375c0-118">[ **Domain name (または FQDN)**] に、ブロックするフェデレーションパートナードメインの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="375c0-118">In **Domain name (or FQDN)**, type the name of the federated partner domain that you want to block.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="375c0-119">名前の長さは、256文字以下にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="375c0-119">The name cannot exceed 256 characters in length.</span></span><BR><span data-ttu-id="375c0-120">フェデレーションパートナーのドメイン名での検索では、サフィックス一致が実行されます。</span><span class="sxs-lookup"><span data-stu-id="375c0-120">The search on the federated partner domain name performs a suffix match.</span></span> <span data-ttu-id="375c0-121">たとえば、 <STRONG>contoso.com</STRONG>と入力すると、検索によってドメイン <STRONG>it.contoso.com</STRONG>も返されます。</span><span class="sxs-lookup"><span data-stu-id="375c0-121">For example, if you type <STRONG>contoso.com</STRONG>, the search will also return the domain <STRONG>it.contoso.com</STRONG>.</span></span><BR><span data-ttu-id="375c0-122">フェデレーションパートナードメインは、同時にブロックおよび許可することはできません。</span><span class="sxs-lookup"><span data-stu-id="375c0-122">A federated partner domain cannot simultaneously be blocked and allowed.</span></span> <span data-ttu-id="375c0-123">Lync Server 2013 では、リストを同期する必要がないように、この問題を回避することができます。</span><span class="sxs-lookup"><span data-stu-id="375c0-123">Lync Server 2013 prevents this from happening so that you do not have to synch up your lists.</span></span>

        
        </div>
    
      - <span data-ttu-id="375c0-124">省略[ **コメント**] に、この構成について他のシステム管理者と共有する情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="375c0-124">(Optional) In **Comment**, type information that you want to share with other system administrators about this configuration.</span></span>

6.  <span data-ttu-id="375c0-125">[**コミット**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="375c0-125">Click **Commit**.</span></span>

7.  <span data-ttu-id="375c0-126">ブロックするフェデレーションパートナーごとに、手順 4 ~ 6 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="375c0-126">Repeat steps 4 through 6 for each federated partner that you want to block.</span></span>

<span data-ttu-id="375c0-127">フェデレーションされたユーザーアクセスを有効にするには、組織でフェデレーションされたユーザーアクセスのサポートを有効にする必要もあります。</span><span class="sxs-lookup"><span data-stu-id="375c0-127">To enable federated user access, you must also enable support for federated user access in your organization.</span></span> <span data-ttu-id="375c0-128">詳細については、「 [Lync Server 2013 でリモートユーザーアクセスを有効または無効](lync-server-2013-enable-or-disable-remote-user-access.md)にする」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="375c0-128">For details, see [Enable or disable remote user access in Lync Server 2013](lync-server-2013-enable-or-disable-remote-user-access.md).</span></span>

<span data-ttu-id="375c0-129">さらに、フェデレーションされたユーザーと共同作業できるようにするユーザーにポリシーを構成して適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="375c0-129">Additionally, you must configure and apply the policy to users that you want to be able to collaborate with federated users.</span></span> <span data-ttu-id="375c0-130">詳細については、「 [Lync Server 2013 でフェデレーションされたユーザーアクセスを制御するためのポリシーを構成する](lync-server-2013-configure-policies-to-control-federated-user-access.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="375c0-130">For details, see [Configure policies to control federated user access in Lync Server 2013](lync-server-2013-configure-policies-to-control-federated-user-access.md).</span></span>

<span data-ttu-id="375c0-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="375c0-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

