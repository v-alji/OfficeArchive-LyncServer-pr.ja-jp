---
title: 'Lync Server 2013: Lync フェデレーションのセットアップ'
description: 'Lync Server 2013: Lync フェデレーションをセットアップします。'
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
# <a name="setting-up-lync-federation-in-lync-server-2013"></a><span data-ttu-id="7df26-103">Lync Server 2013 での Lync フェデレーションのセットアップ</span><span class="sxs-lookup"><span data-stu-id="7df26-103">Setting up Lync federation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7df26-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7df26-104">

<span> </span></span></span>

<span data-ttu-id="7df26-105">_**最終更新日:** 2014-03-27_</span><span class="sxs-lookup"><span data-stu-id="7df26-105">_**Topic Last Modified:** 2014-03-27_</span></span>

<span data-ttu-id="7df26-106">エッジサーバーまたはサーバーを既に展開している場合は、フェデレーションシナリオ機能を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="7df26-106">If you have already deployed you Edge server or servers, adding the federated scenarios features is straight forward.</span></span> <span data-ttu-id="7df26-107">エッジサーバーをセットアップしていない場合は、最初にこの操作を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="7df26-107">If you have not set up Edge Servers, you must do that first.</span></span> <span data-ttu-id="7df26-108">詳細については、「 [Lync server 2013 での外部ユーザーアクセスの計画](lync-server-2013-planning-for-external-user-access.md) 」を参照してください。これには、展開ドキュメントの「 [lync server 2013 での外部ユーザーアクセスの展開](lync-server-2013-deploying-external-user-access.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7df26-108">For details, see: [Planning for external user access in Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) in the Planning documentation and [Deploying external user access in Lync Server 2013](lync-server-2013-deploying-external-user-access.md) in the Deployment documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="7df26-109">XMPP フェデレーション、Lync フェデレーション、またはパブリックインスタントメッセージング接続の任意の組み合わせを設定する場合は、それらを同時に、または一度に1つずつ展開することができます。</span><span class="sxs-lookup"><span data-stu-id="7df26-109">If you intend to setup any combination of XMPP federation, Lync Federation, or public instant messaging connectivity, you can deploy them concurrently or one at a time.</span></span> <span data-ttu-id="7df26-110">トポロジビルダーと Lync Server 管理シェルを使用してオプションを構成する場合は、1つ、2つ、または3つのフェデレーションの種類のオプションを構成した後で、エッジサーバーで展開ウィザードを実行すると、必要な手順の数を減らすことができます。</span><span class="sxs-lookup"><span data-stu-id="7df26-110">If you configure the options through the Topology Builder and the Lync Server Management shell, then run the Deployment Wizard at the Edge server after configuring the options for one, two or all three federation types, you can reduce the number of steps required.</span></span>



</div>

<div>

## <a name="setting-up-lync-federation-in-topology-builder-and-the-deployment-wizard"></a><span data-ttu-id="7df26-111">トポロジビルダーと展開ウィザードでの Lync フェデレーションのセットアップ</span><span class="sxs-lookup"><span data-stu-id="7df26-111">Setting Up Lync Federation in Topology Builder and the Deployment Wizard</span></span>

1.  <span data-ttu-id="7df26-112">フロントエンドサーバーで、[トポロジビルダー] を開きます。</span><span class="sxs-lookup"><span data-stu-id="7df26-112">On a Front End server, open Topology Builder.</span></span> <span data-ttu-id="7df26-113">[Edge プール] を展開し、エッジサーバーまたはエッジサーバープールを右クリックします。</span><span class="sxs-lookup"><span data-stu-id="7df26-113">Expand Edge pools, then right click your Edge server or Edge server pool.</span></span> <span data-ttu-id="7df26-114">[プロパティの編集] を選びます。</span><span class="sxs-lookup"><span data-stu-id="7df26-114">Select Edit properties.</span></span>

2.  <span data-ttu-id="7df26-115">[プロパティの編集] の [全般] で、[このエッジプールに対してフェデレーションを有効にする (ポート 5061)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="7df26-115">In Edit Properties under General, select Enable federation for this Edge pool (Port 5061).</span></span> <span data-ttu-id="7df26-116">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7df26-116">Click OK.</span></span>

3.  <span data-ttu-id="7df26-117">[アクション] をクリックし、[トポロジ] を選択し、[発行] を選択します。</span><span class="sxs-lookup"><span data-stu-id="7df26-117">Click Action, select Topology, select Publish.</span></span> <span data-ttu-id="7df26-118">トポロジの発行を求められたら、[次へ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7df26-118">When prompted on Publish the topology, click Next.</span></span> <span data-ttu-id="7df26-119">発行が完了したら、[完了] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7df26-119">When the Publish is finished, click Finish.</span></span>

4.  <span data-ttu-id="7df26-120">エッジサーバーで、Lync Server 展開ウィザードを開きます。</span><span class="sxs-lookup"><span data-stu-id="7df26-120">On the Edge server, open the Lync Server Deployment wizard.</span></span> <span data-ttu-id="7df26-121">[Lync Server System のインストールまたは更新] をクリックし、[Lync Server コンポーネントのセットアップまたは削除] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7df26-121">Click Install or Update Lync Server System, then click Setup or Remove Lync Server Components.</span></span> <span data-ttu-id="7df26-122">[実行] をもう一度クリックします。</span><span class="sxs-lookup"><span data-stu-id="7df26-122">Click Run Again.</span></span>

5.  <span data-ttu-id="7df26-123">Lync Server コンポーネントのセットアップで、[次へ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7df26-123">At Setup Lync Server components, click Next.</span></span> <span data-ttu-id="7df26-124">概要画面には、実行中の操作が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7df26-124">The summary screen will show actions as they are executed.</span></span> <span data-ttu-id="7df26-125">展開が完了したら、[ログの表示] をクリックして、利用可能なログファイルを表示します。</span><span class="sxs-lookup"><span data-stu-id="7df26-125">Once the deployment is done, click View Log to view available log files.</span></span> <span data-ttu-id="7df26-126">[完了] をクリックして展開を完了します。</span><span class="sxs-lookup"><span data-stu-id="7df26-126">Click Finish to complete the deployment.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="7df26-127">このオプションは選択できますが、フェデレーション用に組織内のエッジプールまたはエッジサーバーを1つだけにすることができます。</span><span class="sxs-lookup"><span data-stu-id="7df26-127">You can select this option, but only one Edge pool or Edge Server in your organization can be published externally for federation.</span></span> <span data-ttu-id="7df26-128">パブリックインスタントメッセージング (IM) ユーザーを含むフェデレーションユーザーによるすべてのアクセスは、同じエッジプールまたは単一エッジサーバーを通過します。</span><span class="sxs-lookup"><span data-stu-id="7df26-128">All access by federated users, including public instant messaging (IM) users, go through the same Edge pool or single Edge Server.</span></span> <span data-ttu-id="7df26-129">たとえば、展開に、ニューヨークに展開されている Edge プールまたは1つのエッジサーバーと、ロンドンに展開されているものがある場合、フェデレーションされたユーザーのためのシグナルトラフィックは、ニューヨークエッジプールまたは単一エッジサーバーを通過します。</span><span class="sxs-lookup"><span data-stu-id="7df26-129">For example, if your deployment includes an Edge pool or single Edge Server deployed in New York and one deployed in London and you enable federation support on the New York Edge pool or single Edge Server, signal traffic for federated users will go through the New York Edge pool or single Edge Server.</span></span> <span data-ttu-id="7df26-130">これは、london ユーザーとの通信でも同じですが、london フェデレーションユーザーを呼び出す London の内部ユーザーは、A/V トラフィック用に London プールまたはエッジサーバーを使用します。</span><span class="sxs-lookup"><span data-stu-id="7df26-130">This is true even for communications with London users, although a London internal user calling a London federated user uses the London pool or Edge Server for A/V traffic.</span></span>

    
    </div>

</div>

<div>

## <a name="configuring-federation-with-partners"></a><span data-ttu-id="7df26-131">パートナーとのフェデレーションを構成する</span><span class="sxs-lookup"><span data-stu-id="7df26-131">Configuring Federation with Partners</span></span>

1.  <span data-ttu-id="7df26-132">別の Microsoft Lync Server 2013、Lync Server 2010、Office Communications Server 2007 R2、または Office Communicator 2007 とのフェデレーションを正常に実行するには、次の表からフェデレーションの種類を選択して、DNS SRV レコード、DNS ホスト (A または AAAA 用の AAAA)、およびフェデレーションの種類に適用されるポリシーを構成します。</span><span class="sxs-lookup"><span data-stu-id="7df26-132">To setup a successful federation with another Microsoft Lync Server 2013, Lync Server 2010, Office Communications Server 2007 R2, or Office Communicator 2007, select the type of federation from the following table and define DNS SRV records, DNS host (A or AAAA for IPv6) and configure policies applicable to the type of federation:</span></span>
    
    
    <table>
    <colgroup>
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="7df26-133">フェデレーションの種類</span><span class="sxs-lookup"><span data-stu-id="7df26-133">Federation type</span></span></th>
    <th><span data-ttu-id="7df26-134">DNS レコード</span><span class="sxs-lookup"><span data-stu-id="7df26-134">DNS Records</span></span></th>
    <th><span data-ttu-id="7df26-135">ポリシー定義</span><span class="sxs-lookup"><span data-stu-id="7df26-135">Policy Definition</span></span></th>
    <th><span data-ttu-id="7df26-136">メモ</span><span class="sxs-lookup"><span data-stu-id="7df26-136">Notes</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="7df26-137">検出されたパートナードメイン</span><span class="sxs-lookup"><span data-stu-id="7df26-137">Discovered Partner Domain</span></span></p></td>
    <td><p><span data-ttu-id="7df26-138">_Tcp _sipfederationtls の形式の SRV レコードを構成します。&gt;SRV レコードのポート値が TCP 5061 であり、<strong>このサービスを提供</strong>しているホストが sip として定義されている外部ドメイン名。</span><span class="sxs-lookup"><span data-stu-id="7df26-138">Configure SRV record of the format _sipfederationtls._tcp.&lt;external domain name&gt;Where the port value for the SRV record is TCP 5061 and the <strong>Host offering this service</strong> is defined as sip.</span></span> <span data-ttu-id="7df26-139">&lt;外部ドメイン名 &gt; –アクセスエッジサービスの FQDN。</span><span class="sxs-lookup"><span data-stu-id="7df26-139">&lt;external domain name&gt; – the FQDN of your Access Edge service.</span></span> <span data-ttu-id="7df26-140">SRV レコードの作成の詳細については、「 <a href="lync-server-2013-configure-dns-for-edge-support.md">Lync Server 2013 での microsoft edge サポートの DNS の構成</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7df26-140">See <a href="lync-server-2013-configure-dns-for-edge-support.md">Configure DNS for edge support in Lync Server 2013</a> for details on creating the SRV record</span></span></p></td>
    <td><ul>
    <li><p><span data-ttu-id="7df26-141"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Lync Server 2013 でのフェデレーションおよびパブリック IM 接続の有効化または無効化</a></span><span class="sxs-lookup"><span data-stu-id="7df26-141"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="7df26-142"><a href="lync-server-2013-enable-or-disable-discovery-of-federation-partners.md">Lync Server 2013 でのフェデレーション パートナーの検出の有効化または無効化</a></span><span class="sxs-lookup"><span data-stu-id="7df26-142"><a href="lync-server-2013-enable-or-disable-discovery-of-federation-partners.md">Enable or disable discovery of federation partners in Lync Server 2013</a></span></span></p></li>
    </ul></td>
    <td><p><span data-ttu-id="7df26-143">以前のバージョンでは、この種類のフェデレーションを <strong>オープン拡張フェデレーション</strong>として参照しました。</span><span class="sxs-lookup"><span data-stu-id="7df26-143">Previous versions referred to this type of federation as <strong>Open Enhanced Federation</strong>.</span></span> <span data-ttu-id="7df26-144">SRV レコードの作成は、この種類のフェデレーションに必要であり、他のパートナーがフェデレーションを検出できるようにするために必要です。</span><span class="sxs-lookup"><span data-stu-id="7df26-144">The creation of the SRV record is required for this type of federation and is to allow other partners to discover your federation.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="7df26-145">許可されたパートナードメイン</span><span class="sxs-lookup"><span data-stu-id="7df26-145">Allowed Partner Domain</span></span></p></td>
    <td><p><span data-ttu-id="7df26-146">_Tcp _sipfederationtls の形式の SRV レコードを構成します。&gt;SRV レコードのポート値が TCP 5061 であり、<strong>このサービスを提供</strong>しているホストが sip として定義されている外部ドメイン名。</span><span class="sxs-lookup"><span data-stu-id="7df26-146">Configure SRV record of the format _sipfederationtls._tcp.&lt;external domain name&gt;Where the port value for the SRV record is TCP 5061 and the <strong>Host offering this service</strong> is defined as sip.</span></span> <span data-ttu-id="7df26-147">&lt;外部ドメイン名 &gt; –アクセスエッジサービスの FQDN。</span><span class="sxs-lookup"><span data-stu-id="7df26-147">&lt;external domain name&gt; – the FQDN of your Access Edge service.</span></span> <span data-ttu-id="7df26-148">SRV レコードの作成の詳細については、「 <a href="lync-server-2013-configure-dns-for-edge-support.md">Lync Server 2013 での microsoft edge サポートの DNS の構成</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7df26-148">See <a href="lync-server-2013-configure-dns-for-edge-support.md">Configure DNS for edge support in Lync Server 2013</a> for details on creating the SRV record</span></span></p></td>
    <td><ul>
    <li><p><span data-ttu-id="7df26-149"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Lync Server 2013 でのフェデレーションおよびパブリック IM 接続の有効化または無効化</a></span><span class="sxs-lookup"><span data-stu-id="7df26-149"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</a></span></span></p></li>
    </ul></td>
    <td><p><span data-ttu-id="7df26-150">以前のバージョンでは、この種類のフェデレーションを <strong>拡張フェデレーション</strong>として参照しました。</span><span class="sxs-lookup"><span data-stu-id="7df26-150">Previous versions referred to this type of federation as <strong>Enhanced Federation</strong>.</span></span> <span data-ttu-id="7df26-151">SRV レコードの作成は、この種類のフェデレーションではオプションであり、他のパートナーがフェデレーションを検出できるようにするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7df26-151">The creation of the SRV record is optional for this type of federation and is to allow other partners to discover your federation.</span></span> <span data-ttu-id="7df26-152">これは、<strong>オープン拡張フェデレーション</strong>、または検出された<strong>パートナードメイン</strong>の場合です。</span><span class="sxs-lookup"><span data-stu-id="7df26-152">Of course, this is then an <strong>Open Enhanced Federation</strong>, or <strong>Discovered Partner Domain</strong></span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="7df26-153">許可されたパートナーサーバー</span><span class="sxs-lookup"><span data-stu-id="7df26-153">Allowed Partner Server</span></span></p></td>
    <td><p><span data-ttu-id="7df26-154">ポリシーでフェデレーションパートナーとして SIP ドメイン名とパートナーエッジサーバーの FQDN を構成する</span><span class="sxs-lookup"><span data-stu-id="7df26-154">Configure the SIP domain name and the partner Edge Server FQDN as a federation partner in Policies</span></span></p></td>
    <td><ul>
    <li><p><span data-ttu-id="7df26-155"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Lync Server 2013 でのフェデレーションおよびパブリック IM 接続の有効化または無効化</a></span><span class="sxs-lookup"><span data-stu-id="7df26-155"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="7df26-156"><a href="lync-server-2013-configure-support-for-allowed-external-domains.md">Lync Server 2013 での、許可された外部ドメイン向けサポートの構成</a></span><span class="sxs-lookup"><span data-stu-id="7df26-156"><a href="lync-server-2013-configure-support-for-allowed-external-domains.md">Configure support for allowed external domains in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="7df26-157"><a href="lync-server-2013-configure-support-for-blocked-external-domains.md">Lync Server 2013 での禁止された外部ドメイン向けサポートの構成</a></span><span class="sxs-lookup"><span data-stu-id="7df26-157"><a href="lync-server-2013-configure-support-for-blocked-external-domains.md">Configure support for blocked external domains in Lync Server 2013</a></span></span></p></li>
    </ul></td>
    <td><p><span data-ttu-id="7df26-158">このフェデレーションタイプは、1対1の関係であり、他のフェデレーションパートナーを検出することはできません。</span><span class="sxs-lookup"><span data-stu-id="7df26-158">This federation type is the definition of a one to one relationship and does not allow for discovery of other federation partners.</span></span> <span data-ttu-id="7df26-159">各フェデレーションパートナーは、個別に構成されます。</span><span class="sxs-lookup"><span data-stu-id="7df26-159">Each federation partner is configured explicitly.</span></span> <span data-ttu-id="7df26-160">以前のバージョンでは、これは<strong>直接フェデレーション</strong>と呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="7df26-160">In previous versions, this was known as <strong>Direct Federation</strong></span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="7df26-161">ホスティングプロバイダーとパブリック IM プロバイダー</span><span class="sxs-lookup"><span data-stu-id="7df26-161">Hosting Provider and Public IM Provider</span></span></p></td>
    <td><p><span data-ttu-id="7df26-162">この種類のフェデレーションには特定の DNS 要件が定義されていません</span><span class="sxs-lookup"><span data-stu-id="7df26-162">No specific DNS requirements are defined for this type of federation</span></span></p></td>
    <td><ul>
    <li><p><span data-ttu-id="7df26-163"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Lync Server 2013 でのフェデレーションおよびパブリック IM 接続の有効化または無効化</a></span><span class="sxs-lookup"><span data-stu-id="7df26-163"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="7df26-164"><a href="lync-server-2013-create-or-edit-public-sip-federated-providers.md">Lync Server 2013 での公開 SIP フェデレーション プロバイダーの作成または編集</a></span><span class="sxs-lookup"><span data-stu-id="7df26-164"><a href="lync-server-2013-create-or-edit-public-sip-federated-providers.md">Create or edit public SIP federated providers in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="7df26-165"><a href="lync-server-2013-create-or-edit-hosted-sip-federated-providers.md">Lync Server 2013 でのホスト SIP フェデレーション プロバイダーの作成または編集</a></span><span class="sxs-lookup"><span data-stu-id="7df26-165"><a href="lync-server-2013-create-or-edit-hosted-sip-federated-providers.md">Create or edit hosted SIP federated providers Lync Server 2013</a></span></span></p></li>
    </ul></td>
    <td><p><span data-ttu-id="7df26-166">このフェデレーションタイプでは、ユーザーに対して構成するサービスとホスティングプロバイダーを定義します。</span><span class="sxs-lookup"><span data-stu-id="7df26-166">This federation type defines services and hosting providers that you want to configure for your users.</span></span> <span data-ttu-id="7df26-167">一般的な使用方法 Windows Live Messenger、Yahoo! などのパブリック IM プロバイダーの構成が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7df26-167">Typical uses include configuration for public IM providers like Windows Live Messenger, Yahoo!</span></span> <span data-ttu-id="7df26-168">および AOL、Lync Online、Microsoft 365 などのホスティングプロバイダー</span><span class="sxs-lookup"><span data-stu-id="7df26-168">and AOL, as well as hosting providers such as Lync Online and Microsoft 365</span></span></p>
    <div>

    > [!IMPORTANT]  
    > <UL>
    > <LI>
    > <P><span data-ttu-id="7df26-169">2012年9月1日以降、Microsoft Lync パブリック IM 接続ユーザーサブスクリプションライセンス ("PIC USL") は、新規または更新契約の購入に使用できなくなりました。</span><span class="sxs-lookup"><span data-stu-id="7df26-169">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) is no longer available for purchase for new or renewing agreements.</span></span> <span data-ttu-id="7df26-170">アクティブなライセンスを持っているお客様は、Yahoo! とのフェデレーションを継続できます。</span><span class="sxs-lookup"><span data-stu-id="7df26-170">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="7df26-171">サービスが終了するまでの Messenger。</span><span class="sxs-lookup"><span data-stu-id="7df26-171">Messenger until the service shut down date.</span></span> <span data-ttu-id="7df26-172">AOL および Yahoo! の2014年6月の終了日</span><span class="sxs-lookup"><span data-stu-id="7df26-172">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="7df26-173">が発表されました。</span><span class="sxs-lookup"><span data-stu-id="7df26-173">has been announced.</span></span> <span data-ttu-id="7df26-174">詳細については、「 <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Lync Server 2013 でのパブリックインスタントメッセンジャー接続のサポート</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7df26-174">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="7df26-175">PIC USL は、Lync Server または Office Communications Server が Yahoo! とのフェデレーションを行うために必要な1か月あたりのユーザーごとのサブスクリプションライセンスです。</span><span class="sxs-lookup"><span data-stu-id="7df26-175">The PIC USL is a per-user per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="7df26-176">Messenger.</span><span class="sxs-lookup"><span data-stu-id="7df26-176">Messenger.</span></span> <span data-ttu-id="7df26-177">このサービスを提供するための Microsoft の機能は、Yahoo! からのサポートによって決定されたものであり、その基となる契約は "巻停止" となります。</span><span class="sxs-lookup"><span data-stu-id="7df26-177">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which is winding down.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="7df26-178">Lync は、組織間、および世界各地の個人と接続するための強力なツールです。</span><span class="sxs-lookup"><span data-stu-id="7df26-178">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="7df26-179">Windows Live Messenger とのフェデレーションには、Lync 標準 CAL 以外の追加のユーザー/デバイスライセンスは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="7df26-179">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="7df26-180">Skype federation はこのリストに追加されます。 Lync ユーザーは、IM と音声を使用して、数百人の何百万ものユーザーに連絡できます。</span><span class="sxs-lookup"><span data-stu-id="7df26-180">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span></P></LI></UL>


    </div></td>
    </tr>
    </tbody>
    </table>


2.  <span data-ttu-id="7df26-181">必要な DNS ホスト (A または AAAA の場合は AAAA) と DNS SRV レコードを定義して構成する</span><span class="sxs-lookup"><span data-stu-id="7df26-181">Define and configure any required DNS host (A or AAAA for IPv6) and DNS SRV records</span></span>

3.  <span data-ttu-id="7df26-182">Lync Server コントロールパネルを使用するか、Lync Server 管理シェルと適切なコマンドレットを使用して、ポリシーを定義して構成します。</span><span class="sxs-lookup"><span data-stu-id="7df26-182">Define and configure any policies using the Lync Server Control Panel or by using the Lync Server Management Shell and the appropriate cmdlets.</span></span> <span data-ttu-id="7df26-183">Lync Server 管理シェルコマンドレットの詳細については、「 [Lync server 2013 のフェデレーションと外部アクセスコマンドレット](https://docs.microsoft.com/powershell/module/skype/)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7df26-183">For details on the Lync Server Management Shell cmdlets, see [Federation and external access cmdlets in Lync Server 2013](https://docs.microsoft.com/powershell/module/skype/)</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="7df26-184">Lync Room System (LRS) では、フェデレーションされた Lync パートナーの開催者によって送信された会議の [参加] ボタンは表示されません。</span><span class="sxs-lookup"><span data-stu-id="7df26-184">Lync Room System (LRS) does not show join button for meetings sent by organizers in federated Lync partners.</span></span> <span data-ttu-id="7df26-185">LRS に表示される会議の参加リンクの場合、送信側の組織は、次のコマンドレットを使用して TNEF を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7df26-185">For a meeting join link to appear on LRS, the sending organization must enable TNEF by using the following cmdlet:</span></span><BR><BR><CODE>New-RemoteDomain -DomainName Contoso.com -Name Contoso</CODE><BR><CODE>Set-RemoteDomain -Identity Contoso -TNEFEnabled $true</CODE><BR><span data-ttu-id="7df26-186">これは LRS 固有のものではないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="7df26-186">Note that this is not LRS specific.</span></span> <span data-ttu-id="7df26-187">また、MAPI プロパティは転送されませんが、Outlook の場合は、outlook と Lync では、会議の出席依頼を開き、会議の URL をクリックすることができます。</span><span class="sxs-lookup"><span data-stu-id="7df26-187">Outlook and Lync would also not show Join links in this case as MAPI properties are not transported, but in the Outlook case, the user can open up the meeting invite and click on the meeting URL.</span></span> <span data-ttu-id="7df26-188">TNEFEnabled が true に設定されている場合、Exchange 2013 は、OnlineMeetingExternalLink を含む MAPI プロパティを削除しません。また、アラームに [参加] ボタンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7df26-188">When TNEFEnabled is set to true Exchange 2013 does not strip MAPI properties including OnlineMeetingExternalLink and the Join button will be shown on the reminder.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="7df26-189">関連項目</span><span class="sxs-lookup"><span data-stu-id="7df26-189">See Also</span></span>


[<span data-ttu-id="7df26-190">Lync Server 2013 での SIP、XMPP フェデレーション、およびパブリックインスタントメッセージングの計画</span><span class="sxs-lookup"><span data-stu-id="7df26-190">Planning for SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>](lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md)  
[<span data-ttu-id="7df26-191">Lync Server 2013 へのフェデレーションおよび外部アクセスの管理</span><span class="sxs-lookup"><span data-stu-id="7df26-191">Managing federation and external access to Lync Server 2013</span></span>](lync-server-2013-managing-federation-and-external-access-to-lync-server-2013.md)  
  

<span data-ttu-id="7df26-192"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7df26-192"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

