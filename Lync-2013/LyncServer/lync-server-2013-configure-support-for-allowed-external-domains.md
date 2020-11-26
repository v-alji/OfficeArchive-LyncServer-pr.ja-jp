---
title: 'Lync Server 2013: 許可された外部ドメイン向けサポートの構成'
description: 'Lync Server 2013: 許可されている外部ドメインのサポートを構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure support for allowed external domains
ms:assetid: 3ee6e175-986d-4c33-b03a-b9f93083dca6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425908(v=OCS.15)
ms:contentKeyID: 48183943
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 13845638bca8791d43b8644c5dcb30ec73751a5b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433683"
---
# <a name="configure-support-for-allowed-external-domains-in-lync-server-2013"></a><span data-ttu-id="06d86-103">Lync Server 2013 での、許可された外部ドメイン向けサポートの構成</span><span class="sxs-lookup"><span data-stu-id="06d86-103">Configure support for allowed external domains in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="06d86-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="06d86-104">

<span> </span></span></span>

<span data-ttu-id="06d86-105">_**最終更新日:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="06d86-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="06d86-106">フェデレーションパートナーのサポートを構成している場合、組織とフェデレーションできる特定のドメインを管理することができます。</span><span class="sxs-lookup"><span data-stu-id="06d86-106">If you have configured support for federated partners, you can manage which specific domains can federate with your organization.</span></span> <span data-ttu-id="06d86-107">1つ以上の特定の外部ドメインを、許可されたフェデレーションドメインとして構成します。</span><span class="sxs-lookup"><span data-stu-id="06d86-107">You configure one or more specific external domains as allowed federated domains.</span></span> <span data-ttu-id="06d86-108">そのためには、許可ドメインの一覧に各ドメインを追加します。</span><span class="sxs-lookup"><span data-stu-id="06d86-108">To do this, add each domain to the list of allowed domains.</span></span> <span data-ttu-id="06d86-109">組織でパートナーの検出が有効になっている場合でも、ドメインが1000以上のユーザーと通信する必要がある、または1秒あたり20件を超えるメッセージを送信する必要があるフェデレーションパートナーである場合に、この操作を行います。</span><span class="sxs-lookup"><span data-stu-id="06d86-109">Even if partner discovery is enabled for your organization, do this if the domain is a federated partner that might need to communicate with more than 1,000 of your users or might need to send more than 20 messages per second.</span></span> <span data-ttu-id="06d86-110">組織でパートナー検出が有効になっていない場合、許可されたドメインリストに追加した外部ドメインのユーザーのみが、組織内のユーザーと IM および会議に参加できます。</span><span class="sxs-lookup"><span data-stu-id="06d86-110">If partner discovery is not enabled for your organization, only users of external domains that you add to the allowed domains list can participate in IM and conferencing with users in your organization.</span></span> <span data-ttu-id="06d86-111">フェデレーションドメインへのアクセスをフェデレーションパートナーのアクセスエッジサービスを実行している特定のサーバーに制限する場合は、許可ドメインの一覧で、各ドメインのアクセスエッジサービスを実行しているサーバーのドメイン名を指定できます。</span><span class="sxs-lookup"><span data-stu-id="06d86-111">If you want to restrict access for a federated domain to a specific server running the Access Edge service of the federated partner, you can specify the domain name of the server running the Access Edge service for each domain in the list of allowed domains.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="06d86-112">この手順では、特定のドメインのサポートを構成する方法について説明します。フェデレーションユーザーのサポートを実装するには、組織のフェデレーションユーザーのサポートを有効にする必要があります。また、フェデレーションユーザーと共同作業できるユーザーを管理するためのポリシーを構成して適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="06d86-112">This procedure describes how to configure support for specific domains, but implementing support for federated users also requires that you enable support for federated users for your organization, and configure and apply policies to control which users can collaborate with federated users.</span></span> <span data-ttu-id="06d86-113">フェデレーションユーザーのサポートを有効にする方法の詳細については、「 <A href="lync-server-2013-enable-or-disable-remote-user-access.md">Lync Server 2013 でリモートユーザーアクセスを有効または無効</A>にする」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="06d86-113">For details about enabling support for federated users, see <A href="lync-server-2013-enable-or-disable-remote-user-access.md">Enable or disable remote user access in Lync Server 2013</A>.</span></span> <span data-ttu-id="06d86-114">フェデレーションを制御するためのポリシーの構成の詳細については、「 <A href="lync-server-2013-configure-policies-to-control-federated-user-access.md">Lync Server 2013 でフェデレーションされたユーザーアクセスを制御するためのポリシーを構成する</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="06d86-114">For details about configuring policies to control federation, see <A href="lync-server-2013-configure-policies-to-control-federated-user-access.md">Configure policies to control federated user access in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-add-an-external-domain-to-the-list-of-allowed-domains"></a><span data-ttu-id="06d86-115">許可ドメインの一覧に外部ドメインを追加するには</span><span class="sxs-lookup"><span data-stu-id="06d86-115">To add an external domain to the list of allowed domains</span></span>

1.  <span data-ttu-id="06d86-116">RTCUniversalServerAdmins グループ (または同等のユーザー権限を持つグループ) のメンバーであるユーザー アカウントまたは CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="06d86-116">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="06d86-117">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="06d86-117">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="06d86-118">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="06d86-118">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="06d86-119">左側のナビゲーションバーで、[ **外部ユーザーアクセス**] をクリックし、[ **フェデレーションドメイン**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="06d86-119">In the left navigation bar, click **External User Access**, and then click **Federated Domains**.</span></span>

4.  <span data-ttu-id="06d86-120">[ **フェデレーションドメイン** ] ページで、[ **新規作成**] をクリックし、[許可した **ドメイン**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="06d86-120">On the **Federated Domains** page, click **New**, and then click **Allowed domain**.</span></span>

5.  <span data-ttu-id="06d86-121">**新しいフェデレーションドメイン** で、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="06d86-121">In **New Federated Domains**, do the following:</span></span>
    
      - <span data-ttu-id="06d86-122">[ **Domain name (または FQDN)**] に、フェデレーションパートナードメインの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="06d86-122">In **Domain name (or FQDN)**, type the name of the federated partner domain.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="06d86-123">この名前は一意であり、アクセスエッジサービスを実行しているこのサーバーで許可されているドメインとして既に存在することはできません。</span><span class="sxs-lookup"><span data-stu-id="06d86-123">This name must be unique and cannot already exist as an allowed domain for this server running the Access Edge service.</span></span> <span data-ttu-id="06d86-124">名前の長さは、256文字以下にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="06d86-124">The name cannot exceed 256 characters in length.</span></span><BR><span data-ttu-id="06d86-125">フェデレーションパートナーのドメイン名での検索では、サフィックス一致が実行されます。</span><span class="sxs-lookup"><span data-stu-id="06d86-125">The search on the federated partner domain name performs a suffix match.</span></span> <span data-ttu-id="06d86-126">たとえば、 <STRONG>contoso.com</STRONG>と入力すると、検索によってドメイン <STRONG>it.contoso.com</STRONG>も返されます。</span><span class="sxs-lookup"><span data-stu-id="06d86-126">For example, if you type <STRONG>contoso.com</STRONG>, the search will also return the domain <STRONG>it.contoso.com</STRONG>.</span></span><BR><span data-ttu-id="06d86-127">フェデレーションパートナードメインは、同時にブロックおよび許可することはできません。</span><span class="sxs-lookup"><span data-stu-id="06d86-127">A federated partner domain cannot simultaneously be blocked and allowed.</span></span> <span data-ttu-id="06d86-128">Lync Server 2013 では、リストを同期する必要がないように、この問題を回避することができます。</span><span class="sxs-lookup"><span data-stu-id="06d86-128">Lync Server 2013 prevents this from happening so that you do not have to synch up your lists.</span></span>

        
        </div>
    
      - <span data-ttu-id="06d86-129">このフェデレーションドメインへのアクセスを、アクセスエッジサービス **(FQDN)** で実行されている特定のサーバーのユーザーに制限する場合は、アクセスエッジサービスを実行しているフェデレーションドメインのサーバーの FQDN を入力します。</span><span class="sxs-lookup"><span data-stu-id="06d86-129">If you want to restrict access for this federated domain to users of a specific server running the Access Edge service, in **Access Edge service (FQDN)**, type the FQDN of the federated domain’s server running the Access Edge service.</span></span>
    
      - <span data-ttu-id="06d86-130">追加情報を提供する場合は、[ **コメント**] に、この構成について他のシステム管理者と共有する情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="06d86-130">If you want to provide additional information, in **Comment**, type information that you want to share with other system administrators about this configuration.</span></span>

6.  <span data-ttu-id="06d86-131">[**コミット**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="06d86-131">Click **Commit**.</span></span>

7.  <span data-ttu-id="06d86-132">許可するフェデレーションパートナードメインごとに、手順 4 ~ 6 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="06d86-132">Repeat steps 4 through 6 for each federated partner domain that you want to allow.</span></span>

<span data-ttu-id="06d86-133">フェデレーションされたユーザーアクセスを有効にするには、組織でフェデレーションされたユーザーアクセスのサポートを有効にする必要もあります。</span><span class="sxs-lookup"><span data-stu-id="06d86-133">To enable federated user access, you must also enable support for federated user access in your organization.</span></span> <span data-ttu-id="06d86-134">詳細については、「 [Lync Server 2013 でリモートユーザーアクセスを有効または無効](lync-server-2013-enable-or-disable-remote-user-access.md)にする」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="06d86-134">For details, see [Enable or disable remote user access in Lync Server 2013](lync-server-2013-enable-or-disable-remote-user-access.md).</span></span>

<span data-ttu-id="06d86-135">さらに、フェデレーションされたユーザーと共同作業できるようにするユーザーにポリシーを構成して適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="06d86-135">Additionally, you must configure and apply the policy to users that you want to be able to collaborate with federated users.</span></span> <span data-ttu-id="06d86-136">詳細については、「 [Lync Server 2013 でフェデレーションされたユーザーアクセスを制御するためのポリシーを構成する](lync-server-2013-configure-policies-to-control-federated-user-access.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="06d86-136">For details, see [Configure policies to control federated user access in Lync Server 2013](lync-server-2013-configure-policies-to-control-federated-user-access.md).</span></span>

<span data-ttu-id="06d86-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="06d86-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

