---
title: 'Lync Server 2013: Lync フェデレーションのセットアップ'
description: 'Lync Server 2013: Lync フェデレーションのセットアップ。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up Lync federation
ms:assetid: 374ddc43-26f9-499d-be68-a5158adfa49c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204800(v=OCS.15)
ms:contentKeyID: 48183822
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 382def41635f05525e5b047e97febffdb069da2a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399812"
---
# <a name="setting-up-lync-federation-in-lync-server-2013"></a><span data-ttu-id="cab16-103">Lync Server 2013 での Lync フェデレーションのセットアップ</span><span class="sxs-lookup"><span data-stu-id="cab16-103">Setting up Lync federation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cab16-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cab16-104">

<span> </span></span></span>

<span data-ttu-id="cab16-105">_**トピック最終更新日:** 2014-03-27_</span><span class="sxs-lookup"><span data-stu-id="cab16-105">_**Topic Last Modified:** 2014-03-27_</span></span>

<span data-ttu-id="cab16-106">エッジ サーバーまたはエッジ サーバーを既に展開している場合は、フェデレーション シナリオ機能の追加は簡単です。</span><span class="sxs-lookup"><span data-stu-id="cab16-106">If you have already deployed you Edge server or servers, adding the federated scenarios features is straight forward.</span></span> <span data-ttu-id="cab16-107">エッジ サーバーをセットアップしていない場合は、最初にセットアップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cab16-107">If you have not set up Edge Servers, you must do that first.</span></span> <span data-ttu-id="cab16-108">詳細については、「計画」の [「Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) での外部ユーザー アクセスの計画」および「展開ドキュメントの [Lync Server 2013](lync-server-2013-deploying-external-user-access.md) での外部ユーザー アクセスの展開」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cab16-108">For details, see: [Planning for external user access in Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) in the Planning documentation and [Deploying external user access in Lync Server 2013](lync-server-2013-deploying-external-user-access.md) in the Deployment documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="cab16-109">XMPP フェデレーション、Lync フェデレーション、またはパブリック インスタント メッセージング接続の任意の組み合わせをセットアップする場合は、それらを同時に、または一度に 1 つ展開できます。</span><span class="sxs-lookup"><span data-stu-id="cab16-109">If you intend to setup any combination of XMPP federation, Lync Federation, or public instant messaging connectivity, you can deploy them concurrently or one at a time.</span></span> <span data-ttu-id="cab16-110">トポロジ ビルダーと Lync Server 管理シェルを使用してオプションを構成し、1 つ、2 つ、または 3 つのフェデレーション の種類のオプションを構成した後、エッジ サーバーで展開ウィザードを実行すると、必要な手順の数を減らできます。</span><span class="sxs-lookup"><span data-stu-id="cab16-110">If you configure the options through the Topology Builder and the Lync Server Management shell, then run the Deployment Wizard at the Edge server after configuring the options for one, two or all three federation types, you can reduce the number of steps required.</span></span>



</div>

<div>

## <a name="setting-up-lync-federation-in-topology-builder-and-the-deployment-wizard"></a><span data-ttu-id="cab16-111">トポロジ ビルダーと展開ウィザードでの Lync フェデレーションのセットアップ</span><span class="sxs-lookup"><span data-stu-id="cab16-111">Setting Up Lync Federation in Topology Builder and the Deployment Wizard</span></span>

1.  <span data-ttu-id="cab16-112">フロント エンド サーバーでトポロジ ビルダーを開きます。</span><span class="sxs-lookup"><span data-stu-id="cab16-112">On a Front End server, open Topology Builder.</span></span> <span data-ttu-id="cab16-113">エッジ プールを展開し、Edge サーバーまたはエッジ サーバー プールを右クリックします。</span><span class="sxs-lookup"><span data-stu-id="cab16-113">Expand Edge pools, then right click your Edge server or Edge server pool.</span></span> <span data-ttu-id="cab16-114">[プロパティの編集] を選択します。</span><span class="sxs-lookup"><span data-stu-id="cab16-114">Select Edit properties.</span></span>

2.  <span data-ttu-id="cab16-115">[全般] の [プロパティの編集] で、このエッジ プールのフェデレーションを有効にする (ポート 5061) を選択します。</span><span class="sxs-lookup"><span data-stu-id="cab16-115">In Edit Properties under General, select Enable federation for this Edge pool (Port 5061).</span></span> <span data-ttu-id="cab16-116">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cab16-116">Click OK.</span></span>

3.  <span data-ttu-id="cab16-117">[アクション] をクリックし、[トポロジ] を選択し、[発行] を選択します。</span><span class="sxs-lookup"><span data-stu-id="cab16-117">Click Action, select Topology, select Publish.</span></span> <span data-ttu-id="cab16-118">[トポロジの公開] のメッセージが表示されたら、[次へ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cab16-118">When prompted on Publish the topology, click Next.</span></span> <span data-ttu-id="cab16-119">発行が完了したら、[完了] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cab16-119">When the Publish is finished, click Finish.</span></span>

4.  <span data-ttu-id="cab16-120">エッジ サーバーで、Lync Server 展開ウィザードを開きます。</span><span class="sxs-lookup"><span data-stu-id="cab16-120">On the Edge server, open the Lync Server Deployment wizard.</span></span> <span data-ttu-id="cab16-121">[Lync Server System のインストールまたは更新] をクリックし、[Lync Server コンポーネントのセットアップまたは削除] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cab16-121">Click Install or Update Lync Server System, then click Setup or Remove Lync Server Components.</span></span> <span data-ttu-id="cab16-122">[もう一度実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cab16-122">Click Run Again.</span></span>

5.  <span data-ttu-id="cab16-123">Lync Server コンポーネントのセットアップで、[次へ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cab16-123">At Setup Lync Server components, click Next.</span></span> <span data-ttu-id="cab16-124">実行されると、概要画面にアクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="cab16-124">The summary screen will show actions as they are executed.</span></span> <span data-ttu-id="cab16-125">展開が完了したら、[ログの表示] をクリックして、利用可能なログ ファイルを表示します。</span><span class="sxs-lookup"><span data-stu-id="cab16-125">Once the deployment is done, click View Log to view available log files.</span></span> <span data-ttu-id="cab16-126">[完了] をクリックして展開を完了します。</span><span class="sxs-lookup"><span data-stu-id="cab16-126">Click Finish to complete the deployment.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="cab16-127">このオプションは選択できますが、フェデレーションのために外部に公開できるのは組織内のエッジ プールまたはエッジ サーバーの 1 つのみです。</span><span class="sxs-lookup"><span data-stu-id="cab16-127">You can select this option, but only one Edge pool or Edge Server in your organization can be published externally for federation.</span></span> <span data-ttu-id="cab16-128">パブリック インスタント メッセージング (IM) ユーザーを含むフェデレーション ユーザーによるすべてのアクセスは、同じエッジ プールまたは単一のエッジ サーバーを経由します。</span><span class="sxs-lookup"><span data-stu-id="cab16-128">All access by federated users, including public instant messaging (IM) users, go through the same Edge pool or single Edge Server.</span></span> <span data-ttu-id="cab16-129">たとえば、展開にニューヨークに展開されたエッジ プールまたは 1 つのエッジ サーバーが含まれる場合、またロンドンに展開されたエッジ サーバーが含まれる場合、ニューヨーク エッジ プールまたは単一エッジ サーバーでフェデレーション サポートを有効にした場合、フェデレーション ユーザーのシグナル トラフィックは、ニューヨーク エッジ プールまたは単一エッジ サーバーを経由します。</span><span class="sxs-lookup"><span data-stu-id="cab16-129">For example, if your deployment includes an Edge pool or single Edge Server deployed in New York and one deployed in London and you enable federation support on the New York Edge pool or single Edge Server, signal traffic for federated users will go through the New York Edge pool or single Edge Server.</span></span> <span data-ttu-id="cab16-130">これは、ロンドンのユーザーとの通信でも当てはめますが、ロンドンのフェデレーション ユーザーを呼び出すロンドンの内部ユーザーは、A/V トラフィックにロンドン プールまたはエッジ サーバーを使用します。</span><span class="sxs-lookup"><span data-stu-id="cab16-130">This is true even for communications with London users, although a London internal user calling a London federated user uses the London pool or Edge Server for A/V traffic.</span></span>

    
    </div>

</div>

<div>

## <a name="configuring-federation-with-partners"></a><span data-ttu-id="cab16-131">パートナーとのフェデレーションの構成</span><span class="sxs-lookup"><span data-stu-id="cab16-131">Configuring Federation with Partners</span></span>

1.  <span data-ttu-id="cab16-132">別の Microsoft Lync Server 2013、Lync Server 2010、Office Communications Server 2007 R2、または Office Communicator 2007 とのフェデレーションを正常にセットアップするには、次の表からフェデレーションの種類を選択し、DNS SRV レコード、DNS ホスト (A または AAAA for IPv6) を定義し、フェデレーションの種類に適用されるポリシーを構成します。</span><span class="sxs-lookup"><span data-stu-id="cab16-132">To setup a successful federation with another Microsoft Lync Server 2013, Lync Server 2010, Office Communications Server 2007 R2, or Office Communicator 2007, select the type of federation from the following table and define DNS SRV records, DNS host (A or AAAA for IPv6) and configure policies applicable to the type of federation:</span></span>
    
    
    <table>
    <colgroup>
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="cab16-133">フェデレーションの種類</span><span class="sxs-lookup"><span data-stu-id="cab16-133">Federation type</span></span></th>
    <th><span data-ttu-id="cab16-134">DNS レコード</span><span class="sxs-lookup"><span data-stu-id="cab16-134">DNS Records</span></span></th>
    <th><span data-ttu-id="cab16-135">ポリシー定義</span><span class="sxs-lookup"><span data-stu-id="cab16-135">Policy Definition</span></span></th>
    <th><span data-ttu-id="cab16-136">備考</span><span class="sxs-lookup"><span data-stu-id="cab16-136">Notes</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="cab16-137">検出されたパートナー ドメイン</span><span class="sxs-lookup"><span data-stu-id="cab16-137">Discovered Partner Domain</span></span></p></td>
    <td><p><span data-ttu-id="cab16-138">_sipfederationtls._tcp の形式の SRV レコードを構成します。 &lt;外部ドメイン名 SRV レコードのポート値が TCP 5061 で、このサービスを提供する &gt; <strong>ホスト</strong> が sip として定義されている場合。</span><span class="sxs-lookup"><span data-stu-id="cab16-138">Configure SRV record of the format _sipfederationtls._tcp.&lt;external domain name&gt;Where the port value for the SRV record is TCP 5061 and the <strong>Host offering this service</strong> is defined as sip.</span></span> <span data-ttu-id="cab16-139">&lt;外部ドメイン &gt; 名 – Access Edge サービスの FQDN。</span><span class="sxs-lookup"><span data-stu-id="cab16-139">&lt;external domain name&gt; – the FQDN of your Access Edge service.</span></span> <span data-ttu-id="cab16-140">SRV <a href="lync-server-2013-configure-dns-for-edge-support.md">レコードの作成の詳細については、「Lync Server 2013</a> でエッジ サポートの DNS を構成する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cab16-140">See <a href="lync-server-2013-configure-dns-for-edge-support.md">Configure DNS for edge support in Lync Server 2013</a> for details on creating the SRV record</span></span></p></td>
    <td><ul>
    <li><p><span data-ttu-id="cab16-141"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Lync Server 2013 でのフェデレーションおよびパブリック IM 接続の有効化または無効化</a></span><span class="sxs-lookup"><span data-stu-id="cab16-141"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="cab16-142"><a href="lync-server-2013-enable-or-disable-discovery-of-federation-partners.md">Lync Server 2013 でのフェデレーション パートナーの検出の有効化または無効化</a></span><span class="sxs-lookup"><span data-stu-id="cab16-142"><a href="lync-server-2013-enable-or-disable-discovery-of-federation-partners.md">Enable or disable discovery of federation partners in Lync Server 2013</a></span></span></p></li>
    </ul></td>
    <td><p><span data-ttu-id="cab16-143">以前のバージョンでは、この種類のフェデレーションを Open <strong>Enhanced Federation と呼ばていました</strong>。</span><span class="sxs-lookup"><span data-stu-id="cab16-143">Previous versions referred to this type of federation as <strong>Open Enhanced Federation</strong>.</span></span> <span data-ttu-id="cab16-144">SRV レコードの作成は、この種類のフェデレーションに必要であり、他のパートナーがフェデレーションを検出するために必要です。</span><span class="sxs-lookup"><span data-stu-id="cab16-144">The creation of the SRV record is required for this type of federation and is to allow other partners to discover your federation.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="cab16-145">許可されたパートナー ドメイン</span><span class="sxs-lookup"><span data-stu-id="cab16-145">Allowed Partner Domain</span></span></p></td>
    <td><p><span data-ttu-id="cab16-146">_sipfederationtls._tcp の形式の SRV レコードを構成します。 &lt;外部ドメイン名 SRV レコードのポート値が TCP 5061 で、このサービスを提供する &gt; <strong>ホスト</strong> が sip として定義されている場合。</span><span class="sxs-lookup"><span data-stu-id="cab16-146">Configure SRV record of the format _sipfederationtls._tcp.&lt;external domain name&gt;Where the port value for the SRV record is TCP 5061 and the <strong>Host offering this service</strong> is defined as sip.</span></span> <span data-ttu-id="cab16-147">&lt;外部ドメイン &gt; 名 – Access Edge サービスの FQDN。</span><span class="sxs-lookup"><span data-stu-id="cab16-147">&lt;external domain name&gt; – the FQDN of your Access Edge service.</span></span> <span data-ttu-id="cab16-148">SRV <a href="lync-server-2013-configure-dns-for-edge-support.md">レコードの作成の詳細については、「Lync Server 2013</a> でエッジ サポートの DNS を構成する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cab16-148">See <a href="lync-server-2013-configure-dns-for-edge-support.md">Configure DNS for edge support in Lync Server 2013</a> for details on creating the SRV record</span></span></p></td>
    <td><ul>
    <li><p><span data-ttu-id="cab16-149"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Lync Server 2013 でのフェデレーションおよびパブリック IM 接続の有効化または無効化</a></span><span class="sxs-lookup"><span data-stu-id="cab16-149"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</a></span></span></p></li>
    </ul></td>
    <td><p><span data-ttu-id="cab16-150">以前のバージョンでは、この種類のフェデレーションを拡張フェデレーション <strong>と呼ば呼ばされました</strong>。</span><span class="sxs-lookup"><span data-stu-id="cab16-150">Previous versions referred to this type of federation as <strong>Enhanced Federation</strong>.</span></span> <span data-ttu-id="cab16-151">SRV レコードの作成は、この種類のフェデレーションでは省略可能であり、他のパートナーがフェデレーションを検出できます。</span><span class="sxs-lookup"><span data-stu-id="cab16-151">The creation of the SRV record is optional for this type of federation and is to allow other partners to discover your federation.</span></span> <span data-ttu-id="cab16-152">当然ながら、これはオープン <strong>拡張フェデレーション、</strong>または検出されたパートナー <strong>ドメインです</strong></span><span class="sxs-lookup"><span data-stu-id="cab16-152">Of course, this is then an <strong>Open Enhanced Federation</strong>, or <strong>Discovered Partner Domain</strong></span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="cab16-153">許可されたパートナー サーバー</span><span class="sxs-lookup"><span data-stu-id="cab16-153">Allowed Partner Server</span></span></p></td>
    <td><p><span data-ttu-id="cab16-154">ポリシーでフェデレーション パートナーとして SIP ドメイン名とパートナー エッジ サーバー FQDN を構成する</span><span class="sxs-lookup"><span data-stu-id="cab16-154">Configure the SIP domain name and the partner Edge Server FQDN as a federation partner in Policies</span></span></p></td>
    <td><ul>
    <li><p><span data-ttu-id="cab16-155"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Lync Server 2013 でのフェデレーションおよびパブリック IM 接続の有効化または無効化</a></span><span class="sxs-lookup"><span data-stu-id="cab16-155"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="cab16-156"><a href="lync-server-2013-configure-support-for-allowed-external-domains.md">Lync Server 2013 での、許可された外部ドメイン向けサポートの構成</a></span><span class="sxs-lookup"><span data-stu-id="cab16-156"><a href="lync-server-2013-configure-support-for-allowed-external-domains.md">Configure support for allowed external domains in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="cab16-157"><a href="lync-server-2013-configure-support-for-blocked-external-domains.md">Lync Server 2013 での禁止された外部ドメイン向けサポートの構成</a></span><span class="sxs-lookup"><span data-stu-id="cab16-157"><a href="lync-server-2013-configure-support-for-blocked-external-domains.md">Configure support for blocked external domains in Lync Server 2013</a></span></span></p></li>
    </ul></td>
    <td><p><span data-ttu-id="cab16-158">このフェデレーションの種類は、1 対 1 のリレーションシップの定義であり、他のフェデレーション パートナーの検出を許可します。</span><span class="sxs-lookup"><span data-stu-id="cab16-158">This federation type is the definition of a one to one relationship and does not allow for discovery of other federation partners.</span></span> <span data-ttu-id="cab16-159">各フェデレーション パートナーは明示的に構成されます。</span><span class="sxs-lookup"><span data-stu-id="cab16-159">Each federation partner is configured explicitly.</span></span> <span data-ttu-id="cab16-160">以前のバージョンでは、これは直接フェデレーションと <strong>呼ばれる機能でした。</strong></span><span class="sxs-lookup"><span data-stu-id="cab16-160">In previous versions, this was known as <strong>Direct Federation</strong></span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="cab16-161">ホスティング プロバイダーとパブリック IM プロバイダー</span><span class="sxs-lookup"><span data-stu-id="cab16-161">Hosting Provider and Public IM Provider</span></span></p></td>
    <td><p><span data-ttu-id="cab16-162">この種のフェデレーションに特定の DNS 要件が定義されていない</span><span class="sxs-lookup"><span data-stu-id="cab16-162">No specific DNS requirements are defined for this type of federation</span></span></p></td>
    <td><ul>
    <li><p><span data-ttu-id="cab16-163"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Lync Server 2013 でのフェデレーションおよびパブリック IM 接続の有効化または無効化</a></span><span class="sxs-lookup"><span data-stu-id="cab16-163"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="cab16-164"><a href="lync-server-2013-create-or-edit-public-sip-federated-providers.md">Lync Server 2013 での公開 SIP フェデレーション プロバイダーの作成または編集</a></span><span class="sxs-lookup"><span data-stu-id="cab16-164"><a href="lync-server-2013-create-or-edit-public-sip-federated-providers.md">Create or edit public SIP federated providers in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="cab16-165"><a href="lync-server-2013-create-or-edit-hosted-sip-federated-providers.md">Lync Server 2013 でのホスト SIP フェデレーション プロバイダーの作成または編集</a></span><span class="sxs-lookup"><span data-stu-id="cab16-165"><a href="lync-server-2013-create-or-edit-hosted-sip-federated-providers.md">Create or edit hosted SIP federated providers Lync Server 2013</a></span></span></p></li>
    </ul></td>
    <td><p><span data-ttu-id="cab16-166">このフェデレーションの種類は、ユーザー用に構成するサービスとホスティング プロバイダーを定義します。</span><span class="sxs-lookup"><span data-stu-id="cab16-166">This federation type defines services and hosting providers that you want to configure for your users.</span></span> <span data-ttu-id="cab16-167">一般的な用途には Windows Live Messenger、Yahoo!</span><span class="sxs-lookup"><span data-stu-id="cab16-167">Typical uses include configuration for public IM providers like Windows Live Messenger, Yahoo!</span></span> <span data-ttu-id="cab16-168">および AOL、および Lync Online や Microsoft 365 などのホスティング プロバイダー</span><span class="sxs-lookup"><span data-stu-id="cab16-168">and AOL, as well as hosting providers such as Lync Online and Microsoft 365</span></span></p>
    <div>

    > [!IMPORTANT]  
    > <UL>
    > <LI>
    > <P><span data-ttu-id="cab16-169">2012 年 9 月 1 日の現在、Microsoft Lync Public IM Connectivity User Subscription License ("PIC USL") は新規または更新契約の購入で利用できなくなりました。</span><span class="sxs-lookup"><span data-stu-id="cab16-169">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) is no longer available for purchase for new or renewing agreements.</span></span> <span data-ttu-id="cab16-170">アクティブなライセンスをお持ちのお客様は、引き続き Yahoo!</span><span class="sxs-lookup"><span data-stu-id="cab16-170">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="cab16-171">サービスが日付をシャットダウンするまで Messenger。</span><span class="sxs-lookup"><span data-stu-id="cab16-171">Messenger until the service shut down date.</span></span> <span data-ttu-id="cab16-172">AOL および Yahoo!</span><span class="sxs-lookup"><span data-stu-id="cab16-172">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="cab16-173">が発表されました。</span><span class="sxs-lookup"><span data-stu-id="cab16-173">has been announced.</span></span> <span data-ttu-id="cab16-174">詳細については <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">、Lync Server 2013</A>のパブリック インスタント メッセンジャー接続のサポートを参照してください。</span><span class="sxs-lookup"><span data-stu-id="cab16-174">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="cab16-175">PIC USL は、Lync Server または Office Communications Server が Yahoo!</span><span class="sxs-lookup"><span data-stu-id="cab16-175">The PIC USL is a per-user per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="cab16-176">Messenger。</span><span class="sxs-lookup"><span data-stu-id="cab16-176">Messenger.</span></span> <span data-ttu-id="cab16-177">このサービスを提供する Microsoft の機能は、基になる契約である Yahoo! からのサポートを受け始め、曲がりくねっています。</span><span class="sxs-lookup"><span data-stu-id="cab16-177">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which is winding down.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="cab16-178">Lync はこれまで以上に、組織全体や世界中の個人とつながる強力なツールです。</span><span class="sxs-lookup"><span data-stu-id="cab16-178">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="cab16-179">Lync Standard CAL Windows Live Messengerユーザー/デバイス ライセンスを追加する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="cab16-179">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="cab16-180">この一覧には Skype フェデレーションが追加され、Lync ユーザーは IM と音声で数億人のユーザーに連絡できます。</span><span class="sxs-lookup"><span data-stu-id="cab16-180">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span></P></LI></UL>


    </div></td>
    </tr>
    </tbody>
    </table>


2.  <span data-ttu-id="cab16-181">必要な DNS ホスト (A または AAAA for IPv6) および DNS SRV レコードを定義および構成する</span><span class="sxs-lookup"><span data-stu-id="cab16-181">Define and configure any required DNS host (A or AAAA for IPv6) and DNS SRV records</span></span>

3.  <span data-ttu-id="cab16-182">Lync Server コントロール パネルを使用するか、Lync Server 管理シェルと適切なコマンドレットを使用して、ポリシーを定義および構成します。</span><span class="sxs-lookup"><span data-stu-id="cab16-182">Define and configure any policies using the Lync Server Control Panel or by using the Lync Server Management Shell and the appropriate cmdlets.</span></span> <span data-ttu-id="cab16-183">Lync Server 管理シェルコマンドレットの詳細については[、Lync Server 2013](https://docs.microsoft.com/powershell/module/skype/)のフェデレーションと外部アクセスのコマンドレットを参照してください。</span><span class="sxs-lookup"><span data-stu-id="cab16-183">For details on the Lync Server Management Shell cmdlets, see [Federation and external access cmdlets in Lync Server 2013](https://docs.microsoft.com/powershell/module/skype/)</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="cab16-184">Lync Room System (LRS) には、フェデレーション Lync パートナーの開催者から送信された会議の参加ボタンは表示されません。</span><span class="sxs-lookup"><span data-stu-id="cab16-184">Lync Room System (LRS) does not show join button for meetings sent by organizers in federated Lync partners.</span></span> <span data-ttu-id="cab16-185">LRS に会議参加リンクを表示するには、次のコマンドレットを使用して送信組織が TNEF を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cab16-185">For a meeting join link to appear on LRS, the sending organization must enable TNEF by using the following cmdlet:</span></span><BR><BR><CODE>New-RemoteDomain -DomainName Contoso.com -Name Contoso</CODE><BR><CODE>Set-RemoteDomain -Identity Contoso -TNEFEnabled $true</CODE><BR><span data-ttu-id="cab16-186">これは LRS 固有ではありません。</span><span class="sxs-lookup"><span data-stu-id="cab16-186">Note that this is not LRS specific.</span></span> <span data-ttu-id="cab16-187">また、MAPI プロパティが転送されないので、Outlook と Lync ではこの場合は [参加] リンクは表示されませんが、Outlook の場合、ユーザーは会議出席招待を開き、会議の URL をクリックできます。</span><span class="sxs-lookup"><span data-stu-id="cab16-187">Outlook and Lync would also not show Join links in this case as MAPI properties are not transported, but in the Outlook case, the user can open up the meeting invite and click on the meeting URL.</span></span> <span data-ttu-id="cab16-188">TNEFEnabled が true Exchange 2013 に設定されている場合、OnlineMeetingExternalLink を含む MAPI プロパティは削除されません。アラームに [参加] ボタンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="cab16-188">When TNEFEnabled is set to true Exchange 2013 does not strip MAPI properties including OnlineMeetingExternalLink and the Join button will be shown on the reminder.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="cab16-189">関連項目</span><span class="sxs-lookup"><span data-stu-id="cab16-189">See Also</span></span>


[<span data-ttu-id="cab16-190">Lync Server 2013 での SIP、XMPP フェデレーション、パブリック インスタント メッセージングの計画</span><span class="sxs-lookup"><span data-stu-id="cab16-190">Planning for SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>](lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md)  
[<span data-ttu-id="cab16-191">Lync Server 2013 へのフェデレーションおよび外部アクセスの管理</span><span class="sxs-lookup"><span data-stu-id="cab16-191">Managing federation and external access to Lync Server 2013</span></span>](lync-server-2013-managing-federation-and-external-access-to-lync-server-2013.md)  
  

<span data-ttu-id="cab16-192"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cab16-192"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

