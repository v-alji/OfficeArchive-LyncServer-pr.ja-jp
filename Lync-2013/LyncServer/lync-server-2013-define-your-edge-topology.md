---
title: 'Lync Server 2013: エッジ トポロジを定義する'
description: 'Lync Server 2013: エッジトポロジを定義します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Define your edge topology
ms:assetid: 787b23f1-8fa0-4c37-abf2-c516c5dd66f0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398591(v=OCS.15)
ms:contentKeyID: 48184562
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bd4aa16ca23d24f0edd92189216030ef926fc841
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431037"
---
# <a name="define-your-edge-topology-in-lync-server-2013"></a><span data-ttu-id="a06fc-103">Lync Server 2013 でエッジ トポロジを定義する</span><span class="sxs-lookup"><span data-stu-id="a06fc-103">Define your edge topology in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a06fc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a06fc-104">

<span> </span></span></span>

<span data-ttu-id="a06fc-105">_**最終更新日:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="a06fc-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="a06fc-106">トポロジを作成するには、トポロジビルダーを使用する必要があります。また、エッジサーバーを展開する前に、少なくとも1つの内部フロントエンドプールまたは Standard Edition サーバーを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a06fc-106">You must use Topology Builder to build your topology and you must set up at least one internal Front End pool or Standard Edition server before you can deploy your Edge Server.</span></span> <span data-ttu-id="a06fc-107">次の手順を使用して、1つのエッジサーバーのエッジトポロジを定義した後、「 [Lync server 2013 2013 でトポロジを公開](lync-server-2013-publish-your-topology.md) する」の手順を実行して、「microsoft [edge のインストール用の外部メディアにコピー](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md) する」を使用して、トポロジを公開し、エッジサーバーで利用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-107">Use the following procedure to define the edge topology for a single Edge Server, and then use the procedures in [Publish your topology in Lync Server 2013](lync-server-2013-publish-your-topology.md) and [Export your Lync Server 2013 topology and copy it to external media for edge installation](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md) to publish the topology and make it available to your Edge Server.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a06fc-108">内部エッジ インターフェイスと外部エッジ インターフェイスでは、同じ種類のロード バランシングを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a06fc-108">The internal Edge interface and external Edge interface must use the same type of load balancing.</span></span> <span data-ttu-id="a06fc-109">1 つのエッジ インターフェイスで DNS ロード バランシングを使用し、もう 1 つのエッジ インターフェイスでロード バランサー機器を使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="a06fc-109">You cannot use DNS load balancing on one Edge interface and hardware load balancing on the other Edge interface.</span></span>



</div>

<span data-ttu-id="a06fc-110">トポロジの公開、有効化、または無効化を行うには、サーバーの役割を追加または削除するときに、RTCUniversalServerAdmins および Domain Admins グループのメンバーであるユーザーとしてログインしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="a06fc-110">To successfully publish, enable, or disable a topology when adding or removing a server role, you must be logged in as a user who is a member of the RTCUniversalServerAdmins and Domain Admins groups.</span></span> <span data-ttu-id="a06fc-111">また、ユーザーアカウントにサーバーの役割を追加するために必要な管理者権限とアクセス許可を付与することもできます。</span><span class="sxs-lookup"><span data-stu-id="a06fc-111">You can also grant the administrator rights and permissions required for adding server roles to a user account.</span></span> <span data-ttu-id="a06fc-112">詳細については、Standard Edition server または Enterprise Edition server 展開ドキュメントの「 [Lync server 2013 でのセットアップ権限の委任](lync-server-2013-delegate-setup-permissions.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a06fc-112">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md) in the Standard Edition server or Enterprise Edition server Deployment documentation.</span></span> <span data-ttu-id="a06fc-113">その他の構成変更については、RTCUniversalServerAdmins グループのメンバーシップのみが必要です。</span><span class="sxs-lookup"><span data-stu-id="a06fc-113">For other configuration changes, only membership in the RTCUniversalServerAdmins group is required.</span></span>

<span data-ttu-id="a06fc-114">内部トポロジを定義して公開したときに、エッジトポロジを定義したときに、以前に定義したエッジトポロジに対する変更が必要ない場合、それを定義して再公開する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="a06fc-114">If you defined your edge topology when you defined and published your internal topology, and no changes are required to the edge topology that you previously defined, you do not need to do define it and publish it again.</span></span> <span data-ttu-id="a06fc-115">エッジトポロジを変更する必要がある場合にのみ、次の手順を使用してください。</span><span class="sxs-lookup"><span data-stu-id="a06fc-115">Use the following procedure only if you need to make changes to your edge topology.</span></span> <span data-ttu-id="a06fc-116">以前に定義して公開されたトポロジをエッジサーバーで利用できるようにする必要があります。これは、「Lync Server 2013 トポロジをエクスポートする」の手順を使用して、 [edge インストール用の外部メディアにコピー](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md)する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a06fc-116">You must make the previously defined and published topology available to your Edge Servers, which you do by using the procedure in [Export your Lync Server 2013 topology and copy it to external media for edge installation](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md).</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="a06fc-117">エッジサーバーからトポロジビルダーを実行することはできません。</span><span class="sxs-lookup"><span data-stu-id="a06fc-117">You cannot run Topology Builder from an Edge Server.</span></span> <span data-ttu-id="a06fc-118">フロントエンドサーバーまたは Standard Edition サーバーから実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a06fc-118">You must run it from your Front End Server or Standard Edition servers.</span></span>



</div>

<span data-ttu-id="a06fc-119">エッジサーバートポロジを定義するプロセスは、トポロジビルダーで行います。</span><span class="sxs-lookup"><span data-stu-id="a06fc-119">The process to define your Edge Server topology is done in Topology Builder.</span></span> <span data-ttu-id="a06fc-120">計画および構成する3種類の主なエッジサーバートポロジは、以下のとおりです。</span><span class="sxs-lookup"><span data-stu-id="a06fc-120">The three primary types of Edge Server topologies that you plan and configure are listed below:</span></span>

  - <span data-ttu-id="a06fc-121">単一エッジサーバーのトポロジを定義するには</span><span class="sxs-lookup"><span data-stu-id="a06fc-121">To define the Topology for a Single Edge Server</span></span>

  - <span data-ttu-id="a06fc-122">負荷分散エッジサーバープールのトポロジを定義するには</span><span class="sxs-lookup"><span data-stu-id="a06fc-122">To define the Topology for a Load Balanced Edge Server Pool</span></span>

  - <span data-ttu-id="a06fc-123">ハードウェアの負荷分散エッジプールのトポロジを定義するには</span><span class="sxs-lookup"><span data-stu-id="a06fc-123">To define the Topology for a Hardware Load Balanced Edge Pool</span></span>

<div>

## <a name="to-define-the-topology-for-a-single-edge-server"></a><span data-ttu-id="a06fc-124">単一エッジサーバーのトポロジを定義するには</span><span class="sxs-lookup"><span data-stu-id="a06fc-124">To define the topology for a single Edge Server</span></span>

1.  <span data-ttu-id="a06fc-125">トポロジビルダーを開始します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server Topology Builder**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-125">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="a06fc-126">コンソールツリーで、エッジサーバーを展開するサイトを展開します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-126">In the console tree, expand the site in which you want to deploy an Edge Server.</span></span>

3.  <span data-ttu-id="a06fc-127">[ **エッジプール**] を右クリックし、[ **新しいエッジプール**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-127">Right-click **Edge pools**, and then click **New Edge Pool**.</span></span>

4.  <span data-ttu-id="a06fc-128">[ **新しいエッジプールの定義**] で、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-128">In **Define the New Edge Pool**, click **Next**.</span></span>

5.  <span data-ttu-id="a06fc-129">[ **Edge プールの FQDN の定義**] で、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="a06fc-129">In **Define the Edge pool FQDN**, do the following:</span></span>
    
      - <span data-ttu-id="a06fc-130">[ **プールの FQDN**] に、エッジサーバーの内部インターフェイスの完全修飾ドメイン名 (FQDN) を入力します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-130">In **Pool FQDN**, type the fully qualified domain name (FQDN) of the internal interface for the Edge Server.</span></span>
        
        <div>
        

        > [!IMPORTANT]  
        > <span data-ttu-id="a06fc-131">指定する名前が、サーバーで構成されているコンピューター名と同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="a06fc-131">The name you specify must be identical to the computer name configured on the server.</span></span> <span data-ttu-id="a06fc-132">既定では、ドメインに参加していないコンピューターのコンピューター名は、FQDN ではなく、短い名前です。</span><span class="sxs-lookup"><span data-stu-id="a06fc-132">By default the computer name of a computer that is not joined to a domain is a short name, not an FQDN.</span></span> <span data-ttu-id="a06fc-133">トポロジ ビルダーでは、短い名前ではなく FQDN を使用します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-133">Topology Builder uses FQDNs, not short names.</span></span> <span data-ttu-id="a06fc-134">そのため、エッジ サーバーとして展開する、ドメインに参加していないコンピューターの名前で DNS サフィックスを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a06fc-134">So, you must configure a DNS suffix on the name of the computer to be deployed as an Edge Server that is not joined to a domain.</span></span> <span data-ttu-id="a06fc-135">Lync Server、エッジ サーバー、およびプールの FQDN を割り当てる場合に使用できる文字は、標準文字のみ (A ～ Z、a ～ z、0 ～ 9、およびハイフン) です。</span><span class="sxs-lookup"><span data-stu-id="a06fc-135">Use only standard characters (including A–Z, a–z, 0–9, and hyphens) when assigning FQDNs of your Lync Servers, Edge Servers, and pools.</span></span> <span data-ttu-id="a06fc-136">Unicode 文字およびアンダースコアは使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="a06fc-136">Do not use Unicode characters or underscores.</span></span> <span data-ttu-id="a06fc-137">通常、FQDN 内の非標準文字は、外部 DNS とパブリック Ca でサポートされていません (証明書の SN に FQDN を割り当てる必要がある場合)。</span><span class="sxs-lookup"><span data-stu-id="a06fc-137">Nonstandard characters in an FQDN are often not supported by external DNS and public CAs (when the FQDN must be assigned to the SN in the certificate).</span></span> <span data-ttu-id="a06fc-138">DNS サフィックスをコンピューター名に追加する方法の詳細については、「 <A href="lync-server-2013-configure-dns-for-edge-support.md">Lync Server 2013 で microsoft edge のサポートを構成</A>する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a06fc-138">For details about adding a DNS suffix to a computer name, see <A href="lync-server-2013-configure-dns-for-edge-support.md">Configure DNS for edge support in Lync Server 2013</A>.</span></span>

        
        </div>
    
      - <span data-ttu-id="a06fc-139">[ **単一コンピュータープール**] をクリックし、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-139">Click **Single computer pool**, and then click **Next**.</span></span>

6.  <span data-ttu-id="a06fc-140">**[機能の選択**] で、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="a06fc-140">In **Select features**, do the following:</span></span>
    
      - <span data-ttu-id="a06fc-141">SIP アクセスサービス、Lync Server 2013 Web 会議サービス、および A/V Edge サービス用に1つの FQDN と IP アドレスを使用する予定がある場合は、[ **単一の fqdn と Ip アドレスを使用** する] チェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-141">If you plan to use a single FQDN and IP address for the SIP Access service, Lync Server 2013 Web Conferencing service, and A/V Edge services, select the **Use a single FQDN and IP Address** check box.</span></span>
    
      - <span data-ttu-id="a06fc-142">フェデレーションを有効にする予定がある場合は、[ **このエッジプールのフェデレーションを有効にする (Port 5061)** ] チェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-142">If you plan to enable federation select the **Enable federation for this Edge pool (Port 5061)** check box.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="a06fc-143">このオプションは選択できますが、フェデレーション用に組織内のエッジプールまたはエッジサーバーを1つだけにすることができます。</span><span class="sxs-lookup"><span data-stu-id="a06fc-143">You can select this option, but only one Edge pool or Edge Server in your organization can be published externally for federation.</span></span> <span data-ttu-id="a06fc-144">パブリックインスタントメッセージング (IM) ユーザーを含むフェデレーションユーザーによるすべてのアクセスは、同じエッジプールまたは単一エッジサーバーを通過します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-144">All access by federated users, including public instant messaging (IM) users, go through the same Edge pool or single Edge Server.</span></span> <span data-ttu-id="a06fc-145">たとえば、展開に、ニューヨークに展開されている Edge プールまたは1つのエッジサーバーと、ロンドンに展開されているものがある場合、フェデレーションされたユーザーのためのシグナルトラフィックは、ニューヨークエッジプールまたは単一エッジサーバーを通過します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-145">For example, if your deployment includes an Edge pool or single Edge Server deployed in New York and one deployed in London and you enable federation support on the New York Edge pool or single Edge Server, signal traffic for federated users will go through the New York Edge pool or single Edge Server.</span></span> <span data-ttu-id="a06fc-146">これは、london ユーザーとの通信でも同じですが、london フェデレーションユーザーを呼び出す London の内部ユーザーは、A/V トラフィック用に London プールまたはエッジサーバーを使用します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-146">This is true even for communications with London users, although a London internal user calling a London federated user uses the London pool or Edge Server for A/V traffic.</span></span>

        
        </div>
    
      - <span data-ttu-id="a06fc-147">展開用の拡張メッセージングとプレゼンスプロトコル (XMPP) をサポートする予定の場合は、[ **xmpp フェデレーションを有効にする (ポート 5269)** ] チェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-147">If you plan to support the extensible messaging and presence protocol (XMPP) for your deployment, select the **Enable XMPP federation (port 5269)** check box</span></span>

7.  <span data-ttu-id="a06fc-148">**[IP オプションの選択**] で、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="a06fc-148">In **Select IP Options**, do the following:</span></span>
    
      - <span data-ttu-id="a06fc-149">**[内部インターフェイスで Ipv4 を有効** にする]: エッジサーバーまたはエッジプールの内部インターフェイスに ipv4 アドレスを適用する場合は、このチェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-149">**Enable IPv4 on internal interface**: Select the check box if you want to apply an IPv4 address to the Edge Server or Edge pool internal interface</span></span>
    
      - <span data-ttu-id="a06fc-150">**[内部インターフェイスで Ipv6 を有効** にする]: ipv6 アドレスをエッジサーバーまたはエッジプールの内部インターフェイスに適用する場合は、このチェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-150">**Enable IPv6 on internal interface**: Select the check box if you want to apply an IPv6 address to the Edge Server or Edge pool internal interface</span></span>
    
      - <span data-ttu-id="a06fc-151">**[外部インターフェイスで Ipv4 を有効** にする]: エッジサーバーまたはエッジプールの外部インターフェイスに ipv4 アドレスを適用する場合は、このチェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-151">**Enable IPv4 on external interface**: Select the check box if you want to apply an IPv4 address to the Edge Server or Edge pool external interface</span></span>
    
      - <span data-ttu-id="a06fc-152">**[外部インターフェイスで Ipv6 を有効** にする]: ipv6 アドレスをエッジサーバーまたはエッジプールの外部インターフェイスに適用する場合は、このチェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-152">**Enable IPv6 on external interface**: Select the check box if you want to apply an IPv6 address to the Edge Server or Edge pool external interface</span></span>
    
    <span data-ttu-id="a06fc-153">また、外部 IP アドレスにネットワークアドレス変換アドレスを使用するようにエッジサーバーまたはエッジプールを構成することもできます。</span><span class="sxs-lookup"><span data-stu-id="a06fc-153">You can also configure the Edge Server or Edge pool to use a network address translation address for the external IP addresses.</span></span> <span data-ttu-id="a06fc-154">この操作を行うには、チェックボックスをオンにします。 **このエッジプールの外部 IP アドレスは NAT によって変換され** ます。</span><span class="sxs-lookup"><span data-stu-id="a06fc-154">You do this by selecting the check box **The external IP address of this Edge pool is translated by NAT**.</span></span>

8.  <span data-ttu-id="a06fc-155">**外部の fqdn** で、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="a06fc-155">In **External FQDNs**, do the following:</span></span>
    
      - <span data-ttu-id="a06fc-156">SIP アクセス、Web 会議サービス、および A/V Edge サービス用に1つの FQDN と IP アドレスを使用することを選んだ **[機能の選択]** で、外部 FQDN を **sip アクセス** に入力します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-156">If in **Select features** you chose to use a single FQDN and IP address for the SIP access, Web Conferencing service, and A/V Edge service, type the external FQDN in **SIP Access**.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="a06fc-157">このオプションを選択する場合は、各エッジサービス (アクセスエッジサービスの場合は5061、Web 会議エッジサービスの場合は444、A/V Edge サービスの場合は 443) に異なるポート番号を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a06fc-157">If you choose this option, you must specify a different port number for each of the edge services (recommended port settings: 5061 for Access Edge service, 444 for Web Conferencing Edge service, and 443 for A/V Edge service).</span></span> <span data-ttu-id="a06fc-158">このオプションをオンにすると、接続の問題が発生するのを防ぎ、構成を簡素化することができます。その場合、3つのサービスで同じポート番号 (443 など) を使うことができます。</span><span class="sxs-lookup"><span data-stu-id="a06fc-158">Selecting this option can help prevent potential connectivity issues, and simplify the configuration because you can then use the same port number (for example, 443) for all three services.</span></span>

        
        </div>
    
      - <span data-ttu-id="a06fc-159">1つの FQDN と IP アドレスを使用することを **選択し** なかった場合は、 **SIP アクセス**、 **Web 会議** 、 **オーディオビデオ** の外部 fqdn を入力して、既定のポートを維持します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-159">If in **Select features** you did not chose to use a single FQDN and IP Address, type the External FQDNs for **SIP Access**, **Web Conferencing** and **Audio Video**, keeping the default ports.</span></span>

9.  <span data-ttu-id="a06fc-160">**[次へ]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-160">Click **Next**.</span></span>

10. <span data-ttu-id="a06fc-161">[ **内部 ip アドレスの定義**] で、お客様の要件に合わせて、 **内部 IPv4 アドレス** と **内部 IPv6 アドレス** にエッジサーバーの IP アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-161">In **Define the Internal IP address**, type the IP address of your Edge Server in **Internal IPv4 address** and **Internal IPv6 address** as is appropriate for your requirements.</span></span> <span data-ttu-id="a06fc-162">**[次へ]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-162">Click **Next**.</span></span>

11. <span data-ttu-id="a06fc-163">[ **外部 IP アドレスの定義**] で、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="a06fc-163">In **Define the External IP address**, do the following:</span></span>
    
      - <span data-ttu-id="a06fc-164">SIP アクセス、Web 会議サービス、および A/V Edge サービス用に1つの FQDN と IP アドレスを使用する場合は、 **Sip アクセス** でエッジサーバーの外部 IPv4 アドレスを入力して、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-164">If you chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Edge service, type the external IPv4 address of the Edge Server in **SIP Access**, and then, click **Next**.</span></span>
    
      - <span data-ttu-id="a06fc-165">IPv6 アドレスを使用する場合は、 **SIP アクセス** でエッジサーバーの外部 IPv6 アドレスを入力して、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-165">If you chose to use IPv6 addresses, type the external IPv6 address of the Edge Server in **SIP Access**, and then, click **Next**.</span></span>
    
      - <span data-ttu-id="a06fc-166">SIP アクセス、Web 会議サービス、および A/V Edge サービス用に1つの FQDN と IP アドレスを使わない場合は、 **Sip アクセス**、 **Web 会議**、 **a/v 会議** でエッジサーバーの外部 IPv4 アドレスを入力し、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-166">If you did not chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Edge service, type the external IPv4 addresses of the Edge Server in **SIP Access**, **Web Conferencing**, and **A/V Conferencing**, and then click **Next**.</span></span>
    
      - <span data-ttu-id="a06fc-167">IPv6 アドレスの使用を選択したが、SIP アクセス、Web 会議サービス、および A/V Edge サービス用に1つの FQDN と IP アドレスを使用しなかった場合、 **Sip アクセス**、 **Web 会議**、 **a/v 会議** でエッジサーバーの外部 IPv6 アドレスを入力し、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-167">If you chose to use IPv6 addresses and did not chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Edge service, type the external IPv6 addresses of the Edge Server in **SIP Access**, **Web Conferencing**, and **A/V Conferencing**, and then click **Next**.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="a06fc-168">IPv6 アドレス指定を有効にして割り当てなかった場合、このダイアログボックスは表示されません。</span><span class="sxs-lookup"><span data-stu-id="a06fc-168">If you did not choose to enable and assign IPv6 addressing, you will not see this dialog box.</span></span>

        
        </div>

12. <span data-ttu-id="a06fc-169">NAT の使用を選択した場合は、ダイアログボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a06fc-169">If you chose to use NAT, a dialog box appears.</span></span> <span data-ttu-id="a06fc-170">**A/V Edge サービスのパブリック ipv4 アドレス** で、NAT で翻訳するパブリック ipv4 アドレスを入力し、[**次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-170">In **Public IPv4 address for the A/V Edge service**, type the public IPv4 address to be translated by NAT, and then click **Next**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a06fc-171">これは、A/V Edge サービスの外部 IP アドレスである必要があります。</span><span class="sxs-lookup"><span data-stu-id="a06fc-171">This should be the external IP address of the A/V Edge service.</span></span>

    
    </div>

13. <span data-ttu-id="a06fc-172">NAT アドレスと IPv6 アドレスの使用を選択した場合は、ダイアログボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a06fc-172">If you chose to use NAT and IPv6 addresses, a dialog box appears.</span></span> <span data-ttu-id="a06fc-173">**A/V Edge サービスのパブリック ipv6 アドレス** で、NAT で変換するパブリック ipv6 アドレスを入力し、[**次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-173">In **Public IPv6 address for the A/V Edge service**, type the public IPv6 address to be translated by NAT, and then click **Next**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a06fc-174">これは、A/V Edge サービスの外部 IP アドレスである必要があります。</span><span class="sxs-lookup"><span data-stu-id="a06fc-174">This should be the external IP address of the A/V Edge service.</span></span>

    
    </div>

14. <span data-ttu-id="a06fc-175">[ **次ホップの定義**] の [ **次ホッププール**] で、フロントエンドプールまたは標準エディションプールのいずれかの内部プールの名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-175">In **Define the next hop**, in **Next hop pool**, select the name of the internal pool, which can be either a Front End pool or a Standard Edition pool.</span></span> <span data-ttu-id="a06fc-176">または、展開にディレクターが含まれている場合は、ディレクターを選択します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-176">Or, if your deployment includes a Director, select the Director.</span></span> <span data-ttu-id="a06fc-177">[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-177">Then, click **Next**.</span></span>

15. <span data-ttu-id="a06fc-178">[ **フロントエンドプールの関連付け**] で、サポートされている外部ユーザーとの通信にこのエッジサーバーを使用する内部プールの名前を選ぶことで、1つ以上の内部プールを指定します。これには、このエッジサーバーを使用するための内部プールの名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-178">In **Associate Front End pools**, specify one or more internal pools, which can include Front End pools and Standard Edition servers, to be associated with this Edge Server, by selecting the names of the internal pools that are to use this Edge Server for communication with supported external users.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a06fc-179">1つの負荷分散エッジプールまたは単一エッジサーバーのみを、A/V トラフィック用の内部プールに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="a06fc-179">Only one load-balanced Edge pool or single Edge Server can be associated with each internal pool for A/V traffic.</span></span> <span data-ttu-id="a06fc-180">エッジプールまたはエッジサーバーに既に関連付けられている内部プールがある場合は、内部プールが既にエッジプールまたはエッジサーバーに関連付けられていることを示す警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a06fc-180">If you already have an internal pool associated with an Edge pool or Edge Server, a warning appears indicating that the internal pool is already associated an Edge pool or Edge Server.</span></span> <span data-ttu-id="a06fc-181">既に別のエッジサーバーと関連付けられているプールを選択すると、その関連付けが変更されます。</span><span class="sxs-lookup"><span data-stu-id="a06fc-181">If you select a pool that is already associated with another Edge Server, it will change the association.</span></span>

    
    </div>

16. <span data-ttu-id="a06fc-182">[**完了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-182">Click **Finish**.</span></span>

17. <span data-ttu-id="a06fc-183">トポロジを公開します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-183">Publish your topology.</span></span>

</div>

<div>

## <a name="to-define-the-topology-for-a-dns-load-balanced-edge-server-pool"></a><span data-ttu-id="a06fc-184">DNS 負荷分散エッジサーバープールのトポロジを定義するには</span><span class="sxs-lookup"><span data-stu-id="a06fc-184">To define the topology for a DNS load balanced Edge Server pool</span></span>

1.  <span data-ttu-id="a06fc-185">トポロジビルダーを開始します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server Topology Builder**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-185">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="a06fc-186">コンソールツリーで、エッジサーバーを展開するサイトを展開します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-186">In the console tree, expand the site in which you want to deploy Edge Servers.</span></span>

3.  <span data-ttu-id="a06fc-187">[ **エッジプール**] を右クリックし、[ **新しいエッジプール**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-187">Right-click **Edge Pools**, and then click **New Edge Pool**.</span></span>

4.  <span data-ttu-id="a06fc-188">[ **新しいエッジプールの定義**] で、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-188">In **Define the New Edge Pool**, click **Next**.</span></span>

5.  <span data-ttu-id="a06fc-189">[ **Edge プールの FQDN の定義**] で、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="a06fc-189">In **Define the Edge pool FQDN**, do the following:</span></span>
    
      - <span data-ttu-id="a06fc-190">[ **プールの FQDN**] に、エッジプールの内部接続の完全修飾ドメイン名 (FQDN) を入力します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-190">In **Pool FQDN**, type the fully qualified domain name (FQDN) for the internal connection of the Edge pool.</span></span>
        
        <div>
        

        > [!IMPORTANT]  
        > <span data-ttu-id="a06fc-191">プールに指定した名前は、内部のエッジプール名である必要があります。</span><span class="sxs-lookup"><span data-stu-id="a06fc-191">The name you specify for the pool must be the internal edge pool name.</span></span> <span data-ttu-id="a06fc-192">これは FQDN として定義されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="a06fc-192">This must be defined as a FQDN.</span></span> <span data-ttu-id="a06fc-193">トポロジ ビルダーでは、短い名前ではなく FQDN を使用します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-193">Topology Builder uses FQDNs, not short names.</span></span> <span data-ttu-id="a06fc-194">Lync Server、エッジ サーバー、およびプールの FQDN を割り当てる場合に使用できる文字は、標準文字のみ (A ～ Z、a ～ z、0 ～ 9、およびハイフン) です。</span><span class="sxs-lookup"><span data-stu-id="a06fc-194">Use only standard characters (including A–Z, a–z, 0–9, and hyphens) when assigning FQDNs of your Lync Servers, Edge Servers, and pools.</span></span> <span data-ttu-id="a06fc-195">Unicode 文字およびアンダースコアは使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="a06fc-195">Do not use Unicode characters or underscores.</span></span> <span data-ttu-id="a06fc-196">通常、FQDN 内の非標準文字は、外部 DNS とパブリック Ca でサポートされていません (証明書の SN に FQDN を割り当てる必要がある場合)。</span><span class="sxs-lookup"><span data-stu-id="a06fc-196">Nonstandard characters in an FQDN are often not supported by external DNS and public CAs (when the FQDN must be assigned to the SN in the certificate).</span></span>

        
        </div>
    
      - <span data-ttu-id="a06fc-197">[ **複数のコンピュータープール**] をクリックし、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-197">Click **Multiple computer pool**, and then click **Next**.</span></span>

6.  <span data-ttu-id="a06fc-198">**[機能の選択**] で、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="a06fc-198">In **Select features**, do the following:</span></span>
    
      - <span data-ttu-id="a06fc-199">SIP アクセス、Lync Server 2013 Web 会議サービス、および A/V Edge サービス用に1つの FQDN と IP アドレスを使用する予定がある場合は、[ **単一の fqdn と Ip アドレスを使用** する] チェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-199">If you plan to use a single FQDN and IP address for the SIP access, Lync Server 2013 Web Conferencing service and A/V Edge services, select the **Use a single FQDN and IP Address** check box.</span></span>
    
      - <span data-ttu-id="a06fc-200">フェデレーションを有効にする予定がある場合は、[ **このエッジプールに対してフェデレーションを有効にする (ポート 5061)** ] チェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-200">If you plan to enable federation, select the **Enable federation for this Edge pool (Port 5061)** check box.</span></span> <span data-ttu-id="a06fc-201">[**次へ**] をクリック</span><span class="sxs-lookup"><span data-stu-id="a06fc-201">Click **Next**</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="a06fc-202">このオプションは選択できますが、フェデレーション用に組織内のエッジプールまたはエッジサーバーを1つだけにすることができます。</span><span class="sxs-lookup"><span data-stu-id="a06fc-202">You can select this option, but only one Edge pool or Edge Server in your organization can be published externally for federation.</span></span> <span data-ttu-id="a06fc-203">パブリックインスタントメッセージング (IM) ユーザーを含むフェデレーションユーザーによるすべてのアクセスは、同じエッジプールまたは単一エッジサーバーを通過します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-203">All access by federated users, including public instant messaging (IM) users, go through the same Edge pool or single Edge Server.</span></span> <span data-ttu-id="a06fc-204">たとえば、展開に、ニューヨークに展開されたエッジプールまたは1つのエッジサーバーと、ロンドンに展開されているものがあり、新しいニューヨークエッジプールまたは単一エッジサーバーでフェデレーションサポートを有効にしている場合、フェデレーションユーザーのシグナルトラフィックは、ニューヨークエッジプールまたは単一エッジサーバーに送られます。</span><span class="sxs-lookup"><span data-stu-id="a06fc-204">For instance, if your deployment includes an Edge pool or single Edge Server deployed in New York and one deployed in London and you enable federation support on the New York Edge pool or single Edge Server, signal traffic for federated users will go through the New York Edge pool or single Edge Server.</span></span> <span data-ttu-id="a06fc-205">これは、london ユーザーとの通信でも同じですが、london フェデレーションユーザーを呼び出す London の内部ユーザーは、A/V トラフィック用に London プールまたはエッジサーバーを使用します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-205">This is true even for communications with London users, although a London internal user calling a London federated user uses the London pool or Edge Server for A/V traffic.</span></span>

        
        </div>
    
      - <span data-ttu-id="a06fc-206">展開用の拡張メッセージングとプレゼンスプロトコル (XMPP) をサポートする予定の場合は、[ **xmpp フェデレーションを有効にする (ポート 5269)** ] チェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-206">If you plan to support the extensible messaging and presence protocol (XMPP) for your deployment, select the **Enable XMPP federation (port 5269)** check box</span></span>

7.  <span data-ttu-id="a06fc-207">**[次へ]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-207">Click **Next**.</span></span>

8.  <span data-ttu-id="a06fc-208">**[IP オプションの選択**] で、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="a06fc-208">In **Select IP Options**, do the following:</span></span>
    
      - <span data-ttu-id="a06fc-209">**[内部インターフェイスで Ipv4 を有効** にする]: エッジサーバーまたはエッジプールの内部インターフェイスに ipv4 アドレスを適用する場合は、このチェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-209">**Enable IPv4 on internal interface**: Select the check box if you want to apply an IPv4 address to the Edge Server or Edge pool internal interface</span></span>
    
      - <span data-ttu-id="a06fc-210">**[内部インターフェイスで Ipv6 を有効** にする]: ipv6 アドレスをエッジサーバーまたはエッジプールの内部インターフェイスに適用する場合は、このチェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-210">**Enable IPv6 on internal interface**: Select the check box if you want to apply an IPv6 address to the Edge Server or Edge pool internal interface</span></span>
    
      - <span data-ttu-id="a06fc-211">**[外部インターフェイスで Ipv4 を有効** にする]: エッジサーバーまたはエッジプールの外部インターフェイスに ipv4 アドレスを適用する場合は、このチェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-211">**Enable IPv4 on external interface**: Select the check box if you want to apply an IPv4 address to the Edge Server or Edge pool external interface</span></span>
    
      - <span data-ttu-id="a06fc-212">**[外部インターフェイスで Ipv6 を有効** にする]: ipv6 アドレスをエッジサーバーまたはエッジプールの外部インターフェイスに適用する場合は、このチェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-212">**Enable IPv6 on external interface**: Select the check box if you want to apply an IPv6 address to the Edge Server or Edge pool external interface</span></span>
    
    <span data-ttu-id="a06fc-213">また、外部 IP アドレスにネットワークアドレス変換アドレスを使用するようにエッジサーバーまたはエッジプールを構成することもできます。</span><span class="sxs-lookup"><span data-stu-id="a06fc-213">You can also configure the Edge Server or Edge pool to use a network address translation address for the external IP addresses.</span></span> <span data-ttu-id="a06fc-214">この操作を行うには、チェックボックスをオンにします。 **このエッジプールの外部 IP アドレスは NAT によって変換され** ます。</span><span class="sxs-lookup"><span data-stu-id="a06fc-214">You do this by selecting the check box **The external IP address of this Edge pool is translated by NAT**.</span></span>

9.  <span data-ttu-id="a06fc-215">**外部の fqdn** で、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="a06fc-215">In **External FQDNs**, do the following:</span></span>
    
      - <span data-ttu-id="a06fc-216">SIP アクセス、Web 会議サービス、および A/V Edge サービス用に1つの FQDN と IP アドレスを使用することを選んだ **[機能の選択]** で、外部 FQDN を **sip アクセス** に入力します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-216">If in **Select features** you chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Edge service, type the external FQDN in **SIP Access**.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="a06fc-217">このオプションを選択する場合は、各エッジサービス (アクセスエッジサービスの場合は5061、Web 会議エッジサービスの場合は444、A/V Edge サービスの場合は 443) に異なるポート番号を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a06fc-217">If you choose this option, you must specify a different port number for each of the Edge services (recommended port settings: 5061 for Access Edge service, 444 for Web Conferencing Edge service, and 443 for A/V Edge service).</span></span> <span data-ttu-id="a06fc-218">このオプションをオンにすると、接続の問題が発生するのを防ぎ、構成を簡素化することができます。その場合、3つのサービスで同じポート番号 (443 など) を使うことができます。</span><span class="sxs-lookup"><span data-stu-id="a06fc-218">By selecting this option, you can help prevent potential connectivity issues and simplify the configuration because you can then use the same port number (for example, 443) for all three services.</span></span>

        
        </div>
    
      - <span data-ttu-id="a06fc-219">1つの FQDN と IP アドレスを使用するように **選択し** なかった場合は、 **SIP アクセス** のために、エッジプールの一般向け側に選択した fqdn を入力します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-219">If in **Select features** you did not chose to use a single FQDN and IP Address, type the FQDN that you have chosen for your public facing side of the edge pool for in **SIP Access**.</span></span> <span data-ttu-id="a06fc-220">[ **Web 会議**] で、エッジプールの一般向けのサイドに選択した FQDN を入力します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-220">In **Web Conferencing**, type the FQDN you have chosen for your public facing side of the Edge pool.</span></span> <span data-ttu-id="a06fc-221">[ **オーディオ/ビデオ**] で、エッジプールの一般向けのサイドに選択した FQDN を入力します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-221">In **Audio/Video**, type the FQDN you have chosen for your public facing side of the Edge pool.</span></span> <span data-ttu-id="a06fc-222">既定のポートを使用します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-222">Use the default ports.</span></span>

10. <span data-ttu-id="a06fc-223">**[次へ]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-223">Click **Next**.</span></span>

11. <span data-ttu-id="a06fc-224">[ **このプールのコンピューターを定義する**] で、[ **追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-224">In **Define the computers in this pool**, click **Add**.</span></span>

12. <span data-ttu-id="a06fc-225">[ **内部 FQDN] と [IP アドレス**] で、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="a06fc-225">In **Internal FQDN and IP address**, do the following:</span></span>
    
      - <span data-ttu-id="a06fc-226">[ **内部 ipv4 アドレス**] に、このプールで作成する最初のエッジサーバーの要件に合わせて ipv4 アドレスと **内部 IPv6 アドレス** を入力します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-226">In **Internal IPv4 address**, type the IPv4 address and **Internal IPv6 address** as is appropriate for your requirements for the first Edge Server that you want to create in this pool.</span></span>
    
      - <span data-ttu-id="a06fc-227">[ **INTERNAL fqdn**] に、このプールで作成する最初のエッジサーバーの FQDN を入力します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-227">In **Internal FQDN**, type the FQDN of the first Edge Server that you want to create in this pool.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="a06fc-228">指定する名前が、サーバーに構成されているコンピューター名と同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="a06fc-228">The name you specify must be identical to the computer name configured on the server.</span></span> <span data-ttu-id="a06fc-229">既定では、ドメインに参加していないコンピューターのコンピューター名は、FQDN ではなく短い名前です。</span><span class="sxs-lookup"><span data-stu-id="a06fc-229">By default, the computer name of a computer that is not joined to a domain is a short name, not an FQDN.</span></span> <span data-ttu-id="a06fc-230">トポロジ ビルダーでは、短い名前ではなく FQDN を使用します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-230">Topology Builder uses FQDNs, not short names.</span></span> <span data-ttu-id="a06fc-231">そのため、エッジ サーバーとして展開する、ドメインに参加していないコンピューターの名前で DNS サフィックスを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a06fc-231">So, you must configure a DNS suffix on the name of the computer to be deployed as an Edge Server that is not joined to a domain.</span></span> <span data-ttu-id="a06fc-232">Lync サーバー、エッジサーバー、プール、およびアレイの Fqdn を割り当てるときは、標準文字 (A ~ Z、a ~ z、0 ~ 9、ハイフンを含む) のみを使用します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-232">Use only standard characters (including A–Z, a–z, 0–9, and hyphens) when assigning FQDNs of your Lync Servers, Edge Servers, pools, and arrays.</span></span> <span data-ttu-id="a06fc-233">Unicode 文字およびアンダースコアは使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="a06fc-233">Do not use Unicode characters or underscores.</span></span> <span data-ttu-id="a06fc-234">通常、FQDN 内の非標準文字は、外部 DNS とパブリック Ca でサポートされていません (証明書の SN に FQDN を割り当てる必要がある場合)。</span><span class="sxs-lookup"><span data-stu-id="a06fc-234">Nonstandard characters in an FQDN are often not supported by external DNS and public CAs (when the FQDN must be assigned to the SN in the certificate).</span></span> <span data-ttu-id="a06fc-235">DNS サフィックスをコンピューター名に追加する方法の詳細については、「 <A href="lync-server-2013-configure-dns-for-edge-support.md">Lync Server 2013 で microsoft edge のサポートを構成</A>する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a06fc-235">For details about adding a DNS suffix to a computer name, see <A href="lync-server-2013-configure-dns-for-edge-support.md">Configure DNS for edge support in Lync Server 2013</A>.</span></span>

        
        </div>

13. <span data-ttu-id="a06fc-236">**[次へ]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-236">Click **Next**.</span></span>

14. <span data-ttu-id="a06fc-237">[ **外部 IP アドレスの定義**] で、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="a06fc-237">In **Define the external IP addresses**, do the following:</span></span>
    
      - <span data-ttu-id="a06fc-238">SIP アクセス、Web 会議サービス、および A/V Edge サービス用に1つの FQDN と IP アドレスを使用する場合は、 **Sip アクセス** でエッジサーバーの外部 IP アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-238">If you chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Edge service, type the external IP address of the Edge Server in **SIP Access**.</span></span>
    
      - <span data-ttu-id="a06fc-239">SIP アクセス、Web 会議サービス、および A/V 会議サービスに1つの FQDN と IP アドレスを使用することを選んでいなかった場合は、 **Sip アクセス** 用にこのエッジプールサーバーの一般向けのサイドに選択した ip アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-239">If you did not chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Conferencing service, type the IP address that you have chosen for your public facing side of this Edge pool server for **SIP Access**.</span></span> <span data-ttu-id="a06fc-240">[ **Web 会議**] で、この Edge プールサーバーのパブリック向けのサイドに選択した IP アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-240">In **Web Conferencing**, type the IP address that you have chosen for your public facing side of this Edge pool server.</span></span> <span data-ttu-id="a06fc-241">[ **A/V 会議**] に、この Edge プールサーバーのパブリック向けサイドに選択した IP アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-241">In **A/V Conferencing**, type the IP address you have chosen for your public facing side of this Edge pool server.</span></span>

15. <span data-ttu-id="a06fc-242">**[次へ]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-242">Click **Next**.</span></span>

16. <span data-ttu-id="a06fc-243">IPv6 アドレスを有効にする場合は、[ **外部 IP アドレスの定義**] で、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="a06fc-243">If you chose to enable IPv6 addresses, In **Define the external IP addresses**, do the following:</span></span>
    
      - <span data-ttu-id="a06fc-244">SIP アクセス、Web 会議サービス、および A/V Edge サービス用に1つの FQDN と IP アドレスを使用する場合は、 **Sip アクセス** でエッジサーバーの外部 IPv6 アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-244">If you chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Edge service, type the external IPv6 address of the Edge Server in **SIP Access**.</span></span>
    
      - <span data-ttu-id="a06fc-245">SIP アクセス、Web 会議サービス、および A/V 会議サービスに1つの FQDN と IP アドレスを使用することを選んでいない場合は、 **Sip アクセス** のために、このエッジプールサーバーのパブリックフェーシング側に選択した IPv6 アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-245">If you did not chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Conferencing service, type the IPv6 address that you have chosen for your public facing side of this Edge pool server for **SIP Access**.</span></span> <span data-ttu-id="a06fc-246">[ **Web 会議**] で、この Edge プールサーバーのパブリック向け側に選択した IPv6 アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-246">In **Web Conferencing**, type the IPv6 address that you have chosen for your public facing side of this Edge pool server.</span></span> <span data-ttu-id="a06fc-247">[ **A/V 会議**] に、この Edge プールサーバーのパブリック向け側に選択した IPv6 アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-247">In **A/V Conferencing**, type the IPv6 address you have chosen for your public facing side of this Edge pool server.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a06fc-248">IPv6 アドレス指定を有効にして割り当てなかった場合、このダイアログボックスは表示されません。</span><span class="sxs-lookup"><span data-stu-id="a06fc-248">If you did not choose to enable and assign IPv6 addressing, you will not see this dialog box.</span></span>

    
    </div>

17. <span data-ttu-id="a06fc-249">[**完了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-249">Click **Finish**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a06fc-250">プールに作成した最初のエッジサーバーが、[ <STRONG>このプール内のコンピューターの定義</STRONG> ] ダイアログボックスに表示されます。</span><span class="sxs-lookup"><span data-stu-id="a06fc-250">You will now see the first Edge Server you created in your pool in the <STRONG>Define the computers in this pool</STRONG> dialog box.</span></span>

    
    </div>

18. <span data-ttu-id="a06fc-251">[ **このプールのコンピューターの定義**] で、[ **追加**] をクリックし、edge プールに追加する2台目のエッジサーバーについて、手順 11 ~ 14 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-251">In **Define the computers in this pool**, click **Add**, and then repeat steps 11 through 14 for the second Edge Server that you want to add to you Edge pool.</span></span>

19. <span data-ttu-id="a06fc-252">手順 11 ~ 14 を繰り返したら、[次の **プール内のコンピューターを定義** する] の [**次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-252">After you repeat steps 11 through 14, click **Next** in **Define the computers in this pool**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a06fc-253">この時点で、プールに両方のエッジサーバーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a06fc-253">At this point, you can see both of the Edge Servers in your pool.</span></span>

    
    </div>

20. <span data-ttu-id="a06fc-254">NAT の使用を選択した場合は、ダイアログボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a06fc-254">If you chose to use NAT, a dialog box appears.</span></span> <span data-ttu-id="a06fc-255">[ **パブリック IP アドレス**] に、NAT で変換するパブリック IPv4 と IPv6 (該当する場合) のアドレスを入力し、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-255">In **Public IP address**, type the public IPv4 and IPv6 (as appropriate) addresses to be translated by NAT, and then click **Next**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a06fc-256">これは、A/V Edge の外部 IP アドレスである必要があります。</span><span class="sxs-lookup"><span data-stu-id="a06fc-256">This should be the external IP Address of the A/V Edge.</span></span>

    
    </div>

21. <span data-ttu-id="a06fc-257">[ **次ホップの定義**] の [ **次ホッププール** ] ボックスの一覧で、内部プールの名前を選びます。これは、フロントエンドプールまたは標準エディションプールのいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="a06fc-257">In **Define the next hop**, in the **Next hop pool** list, select the name of the internal pool, which can be either a Front End pool or a Standard Edition pool.</span></span> <span data-ttu-id="a06fc-258">または、展開にディレクターが含まれている場合は、ディレクターの名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-258">Or, if your deployment includes a Director, select the name of the Director.</span></span> <span data-ttu-id="a06fc-259">[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-259">Then, click **Next**.</span></span>

22. <span data-ttu-id="a06fc-260">[ **フロントエンドプールの関連付け**] で、サポートされている外部ユーザーとの通信にこのエッジサーバーを使用する内部プールの名前を選ぶことによって、このエッジサーバーに関連付ける1つ以上の内部プールを指定します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-260">In **Associate Front End pools**, specify one or more internal pools, which can include Front End pools and Standard Edition servers, to be associated with this Edge Server, by selecting the names of the internal pool(s) that is to use this Edge Server for communication with supported external users.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a06fc-261">1つの負荷分散エッジプールまたは単一エッジサーバーのみを、A/V トラフィック用の内部プールに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="a06fc-261">Only one load-balanced Edge pool or single Edge Server can be associated with each internal pool for A/V traffic.</span></span> <span data-ttu-id="a06fc-262">エッジプールまたはエッジサーバーに既に関連付けられている内部プールがある場合は、内部プールが既にエッジプールまたはエッジサーバーに関連付けられていることを示す警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a06fc-262">If you already have an internal pool associated with an Edge pool or Edge Server, a warning appears indicating that the internal pool is already associated an Edge pool or Edge Server.</span></span> <span data-ttu-id="a06fc-263">既に別のエッジサーバーと関連付けられているプールを選択すると、その関連付けが変更されます。</span><span class="sxs-lookup"><span data-stu-id="a06fc-263">If you select a pool that is already associated with another Edge Server, it will change the association.</span></span>

    
    </div>

23. <span data-ttu-id="a06fc-264">[**完了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-264">Click **Finish**.</span></span>

24. <span data-ttu-id="a06fc-265">トポロジを公開します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-265">Publish your topology.</span></span>

</div>

<div>

## <a name="to-define-the-topology-for-a-hardware-load-balanced-edge-server-pool"></a><span data-ttu-id="a06fc-266">ハードウェア負荷分散エッジサーバープールのトポロジを定義するには</span><span class="sxs-lookup"><span data-stu-id="a06fc-266">To define the topology for a hardware load balanced Edge Server pool</span></span>

1.  <span data-ttu-id="a06fc-267">トポロジビルダーを開始します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server Topology Builder**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-267">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="a06fc-268">コンソールツリーで、エッジサーバーを展開するサイトを展開します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-268">In the console tree, expand the site in which you want to deploy Edge Servers.</span></span>

3.  <span data-ttu-id="a06fc-269">[ **エッジプール**] を右クリックし、[ **新しいエッジプール**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-269">Right-click **Edge Pools**, and then select **New Edge Pool**.</span></span>

4.  <span data-ttu-id="a06fc-270">[ **新しいエッジプールの定義**] で、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-270">In **Define the New Edge Pool**, click **Next**.</span></span>

5.  <span data-ttu-id="a06fc-271">[ **Edge プールの FQDN の定義**] で、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="a06fc-271">In **Define the Edge pool FQDN**, do the following:</span></span>
    
      - <span data-ttu-id="a06fc-272">[ **Fqdn**] に、エッジプールの内部側で選択した完全修飾ドメイン名 (FQDN) を入力します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-272">In **FQDN**, type the fully qualified domain name (FQDN) you have chosen for the internal side of the Edge pool.</span></span>
        
        <div>
        

        > [!IMPORTANT]  
        > <span data-ttu-id="a06fc-273">プールに指定した名前は、内部のエッジプール名である必要があります。</span><span class="sxs-lookup"><span data-stu-id="a06fc-273">The name you specify for the pool must be the internal edge pool name.</span></span> <span data-ttu-id="a06fc-274">これは FQDN として定義されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="a06fc-274">This must be defined as a FQDN.</span></span> <span data-ttu-id="a06fc-275">トポロジ ビルダーでは、短い名前ではなく FQDN を使用します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-275">Topology Builder uses FQDNs, not short names.</span></span> <span data-ttu-id="a06fc-276">Lync Server、エッジ サーバー、およびプールの FQDN を割り当てる場合に使用できる文字は、標準文字のみ (A ～ Z、a ～ z、0 ～ 9、およびハイフン) です。</span><span class="sxs-lookup"><span data-stu-id="a06fc-276">Use only standard characters (including A–Z, a–z, 0–9, and hyphens) when assigning FQDNs of your Lync Servers, Edge Servers, and pools.</span></span> <span data-ttu-id="a06fc-277">Unicode 文字およびアンダースコアは使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="a06fc-277">Do not use Unicode characters or underscores.</span></span> <span data-ttu-id="a06fc-278">通常、FQDN 内の非標準文字は、外部 DNS とパブリック Ca でサポートされていません (証明書の SN に FQDN を割り当てる必要がある場合)。</span><span class="sxs-lookup"><span data-stu-id="a06fc-278">Nonstandard characters in an FQDN are often not supported by external DNS and public CAs (when the FQDN must be assigned to the SN in the certificate).</span></span>

        
        </div>
    
    <!-- end list -->
    
      - <span data-ttu-id="a06fc-279">[ **複数のコンピュータープール**] をクリックし、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-279">Click **Multiple computer pool**, and then **Next**.</span></span>

6.  <span data-ttu-id="a06fc-280">**[機能の選択]** で、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="a06fc-280">In **Select features** do the following:</span></span>
    
      - <span data-ttu-id="a06fc-281">SIP アクセスサービス、Lync Server Web 会議サービス、および A/V Edge サービス用に1つの FQDN と IP アドレスを使用する予定がある場合は、[ **単一の fqdn & Ip アドレスを使用** する] チェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-281">If you plan to use a single FQDN and IP address for the SIP access service, Lync Server Web Conferencing service, and A/V Edge service, select the **Use a single FQDN & IP Address** check box.</span></span>
    
      - <span data-ttu-id="a06fc-282">フェデレーションを有効にする予定がある場合は、[ **このエッジプールに対してフェデレーションを有効にする (ポート 5061)** ] チェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-282">If you plan to enable federation, select the **Enable federation for this Edge pool (Port 5061)** check box.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="a06fc-283">このオプションは選択できますが、フェデレーション用に組織内のエッジプールまたはエッジサーバーを1つだけにすることができます。</span><span class="sxs-lookup"><span data-stu-id="a06fc-283">You can select this option, but only one Edge pool or Edge Server in your organization may be published externally for federation.</span></span> <span data-ttu-id="a06fc-284">パブリックインスタントメッセージング (IM) ユーザーを含むフェデレーションユーザーによるすべてのアクセスは、同じエッジプールまたは単一エッジサーバーを通過します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-284">All access by federated users, including public instant messaging (IM) users, go through the same Edge pool or single Edge Server.</span></span> <span data-ttu-id="a06fc-285">たとえば、展開に、ニューヨークに展開されたエッジプールまたは1つのエッジサーバーと、ロンドンに展開されているものがあり、新しいニューヨークエッジプールまたは単一エッジサーバーでフェデレーションサポートを有効にしている場合、フェデレーションユーザーのシグナルトラフィックは、ニューヨークエッジプールまたは単一エッジサーバーに送られます。</span><span class="sxs-lookup"><span data-stu-id="a06fc-285">For instance, if your deployment includes an Edge pool or single Edge Server deployed in New York and one deployed in London and you enable federation support on the New York Edge pool or single Edge Server, signal traffic for federated users will go through the New York Edge pool or single Edge Server.</span></span> <span data-ttu-id="a06fc-286">これは、london ユーザーとの通信でも同じですが、london フェデレーションユーザーを呼び出す London の内部ユーザーは、A/V トラフィック用に London プールまたはエッジサーバーを使用します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-286">This is true even for communications with London users, although a London internal user calling a London federated user uses the London pool or Edge Server for A/V traffic.</span></span>

        
        </div>
    
      - <span data-ttu-id="a06fc-287">展開用の拡張メッセージングとプレゼンスプロトコル (XMPP) をサポートする予定の場合は、[ **xmpp フェデレーションを有効にする (ポート 5269)** ] チェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-287">If you plan to support the extensible messaging and presence protocol (XMPP) for your deployment, select the **Enable XMPP federation (port 5269)** check box</span></span>

7.  <span data-ttu-id="a06fc-288">**[次へ]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-288">Click **Next**.</span></span>

8.  <span data-ttu-id="a06fc-289">**[IP オプションの選択**] で、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="a06fc-289">In **Select IP Options**, do the following:</span></span>
    
      - <span data-ttu-id="a06fc-290">**[内部インターフェイスで Ipv4 を有効** にする]: エッジサーバーまたはエッジプールの内部インターフェイスに ipv4 アドレスを適用する場合は、このチェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-290">**Enable IPv4 on internal interface**: Select the check box if you want to apply an IPv4 address to the Edge Server or Edge pool internal interface</span></span>
    
      - <span data-ttu-id="a06fc-291">**[内部インターフェイスで Ipv6 を有効** にする]: ipv6 アドレスをエッジサーバーまたはエッジプールの内部インターフェイスに適用する場合は、このチェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-291">**Enable IPv6 on internal interface**: Select the check box if you want to apply an IPv6 address to the Edge Server or Edge pool internal interface</span></span>
    
      - <span data-ttu-id="a06fc-292">**[外部インターフェイスで Ipv4 を有効** にする]: エッジサーバーまたはエッジプールの外部インターフェイスに ipv4 アドレスを適用する場合は、このチェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-292">**Enable IPv4 on external interface**: Select the check box if you want to apply an IPv4 address to the Edge Server or Edge pool external interface</span></span>
    
      - <span data-ttu-id="a06fc-293">**[外部インターフェイスで Ipv6 を有効** にする]: ipv6 アドレスをエッジサーバーまたはエッジプールの外部インターフェイスに適用する場合は、このチェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-293">**Enable IPv6 on external interface**: Select the check box if you want to apply an IPv6 address to the Edge Server or Edge pool external interface</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="a06fc-294">[<STRONG>エッジプールの外部 IP アドレスは NAT で変換され</STRONG>ます] チェックボックスをオンにしない<STRONG>で</STRONG>ください。</span><span class="sxs-lookup"><span data-stu-id="a06fc-294"><STRONG>Do Not</STRONG> select the <STRONG>The external IP address of the Edge pool is translated by NAT</STRONG> check box.</span></span> <span data-ttu-id="a06fc-295">ハードウェア負荷分散を使用している場合、ネットワークアドレス変換 (NAT) はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="a06fc-295">Network address translation (NAT) is not supported when you are using hardware load balancing.</span></span>

    
    </div>

9.  <span data-ttu-id="a06fc-296">**外部の fqdn** で、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="a06fc-296">In **External FQDNs**, do the following:</span></span>
    
      - <span data-ttu-id="a06fc-297">SIP アクセス、Web 会議サービス、および A/V Edge サービス用に1つの FQDN と IP アドレスを使用することを選んだ **[機能の選択]** で、外部 FQDN を **sip アクセス** に入力します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-297">If in **Select features** you chose to use a single FQDN and IP address for the SIP access, Web Conferencing service, and A/V Edge service, type the external FQDN in **SIP Access**.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="a06fc-298">このオプションを選択する場合は、各エッジサービス 5061 (アクセスエッジサービスの場合は444、Web 会議エッジサービスの場合は、A/V Edge サービスの場合は 443) に異なるポート番号を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a06fc-298">If you choose to select this option, you must specify a different port number for each of the Edge services (recommended port settings: 5061 for Access Edge service, 444 for Web Conferencing Edge service, and 443 for A/V Edge service).</span></span> <span data-ttu-id="a06fc-299">このオプションをオンにすると、接続の問題が発生するのを防ぎ、構成を簡素化することができます。その場合、3つのサービスで同じポート番号 (443 など) を使うことができます。</span><span class="sxs-lookup"><span data-stu-id="a06fc-299">By selecting this option, you can help prevent potential connectivity issues and simplify the configuration because you can then use the same port number (for example, 443) for all three services.</span></span>

        
        </div>
    
      - <span data-ttu-id="a06fc-300">1つの FQDN と IP アドレスを使用するように **選択し** なかった場合は、 **SIP アクセス** のために、エッジプールの一般向け側に選択した fqdn を入力します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-300">If in **Select features** you did not chose to use a single FQDN and IP address, type the FQDN that you have chosen for your public facing side of the edge pool for in **SIP Access**.</span></span> <span data-ttu-id="a06fc-301">[ **Web 会議**] で、エッジプールの一般向けのサイドに選択した FQDN を入力します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-301">In **Web Conferencing**, type the FQDN you have chosen for your public facing side of the Edge pool.</span></span> <span data-ttu-id="a06fc-302">[ **オーディオ/ビデオ**] で、エッジプールの一般向けのサイドに選択した FQDN を入力します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-302">In **Audio/Video**, type the FQDN you have chosen for your public facing side of the Edge pool.</span></span> <span data-ttu-id="a06fc-303">既定のポートを使用します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-303">Use the default ports.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="a06fc-304">これらは、プールの一般向け仮想 IP (VIP) Fqdn になります。</span><span class="sxs-lookup"><span data-stu-id="a06fc-304">These will be the publicly facing virtual IP (VIP) FQDNs for the pool.</span></span>

        
        </div>

10. <span data-ttu-id="a06fc-305">**[次へ]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-305">Click **Next**.</span></span>

11. <span data-ttu-id="a06fc-306">[ **このプールのコンピューターを定義する**] で、[ **追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-306">In **Define the computers in this pool**, click **Add**.</span></span>

12. <span data-ttu-id="a06fc-307">[ **外部 IP アドレスの定義**] で、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="a06fc-307">In **Define the external IP addresses**, do the following:</span></span>
    
      - <span data-ttu-id="a06fc-308">SIP アクセス、Web 会議サービス、および A/V Edge サービス用に1つの FQDN と IP アドレスを使用する場合は、sip アクセスのエッジサーバーの外部 IPv4 アドレスを **入力します。** **Sip アクセス** のエッジサーバーの外部 IP アドレス。</span><span class="sxs-lookup"><span data-stu-id="a06fc-308">If you chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Edge service, type the external IPv4 address of the Edge Server in **SIP Access**.external IP address of the Edge Server in **SIP Access**.</span></span>
    
      - <span data-ttu-id="a06fc-309">SIP アクセス、Web 会議サービス、および A/V 会議サービスに1つの FQDN と IP アドレスを使用することを選んでいなかった場合は、 **Sip アクセス** 用にこのエッジプールサーバーの一般向けのサイドに選択した ip アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-309">If you did not chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Conferencing service, type the IP address that you have chosen for your public facing side of this Edge pool server for **SIP Access**.</span></span> <span data-ttu-id="a06fc-310">[ **Web 会議**] で、この Edge プールサーバーのパブリック向けのサイドに選択した IP アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-310">In **Web Conferencing**, type the IP address that you have chosen for your public facing side of this Edge pool server.</span></span> <span data-ttu-id="a06fc-311">[ **A/V 会議**] に、この Edge プールサーバーのパブリック向けサイドに選択した IP アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-311">In **A/V Conferencing**, type the IP address you have chosen for your public facing side of this Edge pool server.</span></span>

13. <span data-ttu-id="a06fc-312">**[次へ]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-312">Click **Next**.</span></span>

14. <span data-ttu-id="a06fc-313">IPv6 アドレスを有効にする場合は、[ **外部 IP アドレスの定義**] で、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="a06fc-313">If you chose to enable IPv6 addresses, In **Define the external IP addresses**, do the following:</span></span>
    
      - <span data-ttu-id="a06fc-314">SIP アクセス、Web 会議サービス、および A/V Edge サービス用に1つの FQDN と IP アドレスを使用する場合は、 **Sip アクセス** でエッジサーバーの外部 IPv6 アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-314">If you chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Edge service, type the external IPv6 address of the Edge Server in **SIP Access**.</span></span>
    
      - <span data-ttu-id="a06fc-315">SIP アクセス、Web 会議サービス、および A/V 会議サービスに1つの FQDN と IP アドレスを使用することを選んでいない場合は、 **Sip アクセス** のために、このエッジプールサーバーのパブリックフェーシング側に選択した IPv6 アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-315">If you did not chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Conferencing service, type the IPv6 address that you have chosen for your public facing side of this Edge pool server for **SIP Access**.</span></span> <span data-ttu-id="a06fc-316">[ **Web 会議**] で、この Edge プールサーバーのパブリック向け側に選択した IPv6 アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-316">In **Web Conferencing**, type the IPv6 address that you have chosen for your public facing side of this Edge pool server.</span></span> <span data-ttu-id="a06fc-317">[ **A/V 会議**] に、この Edge プールサーバーのパブリック向け側に選択した IPv6 アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-317">In **A/V Conferencing**, type the IPv6 address you have chosen for your public facing side of this Edge pool server.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a06fc-318">IPv6 アドレス指定を有効にして割り当てなかった場合、このダイアログボックスは表示されません。</span><span class="sxs-lookup"><span data-stu-id="a06fc-318">If you did not choose to enable and assign IPv6 addressing, you will not see this dialog box.</span></span>

    
    </div>

15. <span data-ttu-id="a06fc-319">[**完了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-319">Click **Finish**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a06fc-320">プールに作成した最初のエッジサーバーが、[ <STRONG>このプール内のコンピューターの定義</STRONG> ] ダイアログボックスに表示されます。</span><span class="sxs-lookup"><span data-stu-id="a06fc-320">You will now see the first Edge Server you created in your pool in the <STRONG>Define the computers in this pool</STRONG> dialog box.</span></span>

    
    </div>

16. <span data-ttu-id="a06fc-321">[ **このプールのコンピューターの定義**] で、[ **追加**] をクリックし、エッジプールに追加する2台目のエッジサーバーについて、手順 11 ~ 14 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-321">In **Define the computers in this pool**, click **Add**, and then repeat steps 11 through 14 for the second Edge Server that you want to add to your Edge pool.</span></span>

17. <span data-ttu-id="a06fc-322">手順 11 ~ 14 を繰り返したら、[次の **プール内のコンピューターを定義** する] の [**次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-322">After you repeat steps 11 through 14, click **Next** in **Define the computers in this pool**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a06fc-323">この時点で、プールに両方のエッジサーバーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a06fc-323">At this point, you can see both of the Edge Servers in your pool.</span></span>

    
    </div>

18. <span data-ttu-id="a06fc-324">[ **次ホップの定義**] の [ **次ホッププール** ] ボックスの一覧で、内部プールの名前を選びます。これは、フロントエンドプールまたは標準エディションプールのいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="a06fc-324">In **Define the next hop**, in the **Next hop pool** list, select the name of the internal pool, which can be either a Front End pool or a Standard Edition pool.</span></span> <span data-ttu-id="a06fc-325">または、展開にディレクターが含まれている場合は、ディレクターの名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-325">Or, if your deployment includes a Director, select the name of the Director.</span></span> <span data-ttu-id="a06fc-326">[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-326">Then, click **Next**.</span></span>

19. <span data-ttu-id="a06fc-327">[ **フロントエンドプールの関連付け**] で、サポートされている外部ユーザーとの通信にこのエッジサーバーを使用する内部プールの名前を選ぶことによって、このエッジサーバーに関連付ける1つ以上の内部プールを指定します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-327">In **Associate Front End pools**, specify one or more internal pools, which can include Front End pools and Standard Edition servers, to be associated with this Edge Server, by selecting the names of the internal pool(s) that is to use this Edge Server for communication with supported external users.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a06fc-328">1つの負荷分散エッジプールまたは単一エッジサーバーのみを、A/V トラフィック用の内部プールに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="a06fc-328">Only one load-balanced Edge pool or single Edge Server can be associated with each internal pool for A/V traffic.</span></span> <span data-ttu-id="a06fc-329">エッジプールまたはエッジサーバーに既に関連付けられている内部プールがある場合は、内部プールが既にエッジプールまたはエッジサーバーに関連付けられていることを示す警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a06fc-329">If you already have an internal pool associated with an Edge pool or Edge Server, a warning appears indicating that the internal pool is already associated an Edge pool or Edge Server.</span></span> <span data-ttu-id="a06fc-330">既に別のエッジサーバーと関連付けられているプールを選択すると、その関連付けが変更されます。</span><span class="sxs-lookup"><span data-stu-id="a06fc-330">If you select a pool that is already associated with another Edge Server, it will change the association.</span></span>

    
    </div>

20. <span data-ttu-id="a06fc-331">[**完了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a06fc-331">Click **Finish**.</span></span>

21. <span data-ttu-id="a06fc-332">トポロジを公開します。</span><span class="sxs-lookup"><span data-stu-id="a06fc-332">Publish your topology.</span></span>

<span data-ttu-id="a06fc-333"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a06fc-333"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

