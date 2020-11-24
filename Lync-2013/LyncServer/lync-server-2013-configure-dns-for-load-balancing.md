---
title: 'Lync Server 2013: 負荷分散の DNS 構成'
description: 'Lync Server 2013: 負荷分散用の DNS を構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure DNS for load balancing
ms:assetid: 1b2e8414-8676-4872-8ecf-ea07196f74de
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398251(v=OCS.15)
ms:contentKeyID: 48183540
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4b13db22d65ee67723ebc0a31544137d467d5c6b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399896"
---
# <a name="configure-dns-for-load-balancing-in-lync-server-2013"></a><span data-ttu-id="5474c-103">Lync Server 2013 での負荷分散の DNS 構成</span><span class="sxs-lookup"><span data-stu-id="5474c-103">Configure DNS for load balancing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5474c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5474c-104">

<span> </span></span></span>

<span data-ttu-id="5474c-105">_**最終更新日:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="5474c-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="5474c-106">この手順を完了するには、ドメイン管理者グループのメンバー、または DnsAdmins グループのメンバーとして、サーバーまたはドメインに最低でもログオンしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="5474c-106">To successfully complete this procedure, you should be logged on to the server or domain minimally as a member of the Domain Admins group or a member of the DnsAdmins group.</span></span>

<span data-ttu-id="5474c-107">ドメインネームシステム (DNS) の負荷分散は、Lync Server 2013 に固有のネットワークトラフィック (SIP トラフィックやメディアトラフィックなど) のバランスを行います。</span><span class="sxs-lookup"><span data-stu-id="5474c-107">Domain Name System (DNS) Load Balancing balances the network traffic that is unique to Lync Server 2013, such as SIP traffic and media traffic.</span></span> <span data-ttu-id="5474c-108">DNS の負荷分散は、フロントエンドプール、エッジプール、ディレクタープール、スタンドアロンの仲介プールでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="5474c-108">DNS load balancing is supported for Front End pools, Edge pools, Director pools, and stand-alone Mediation pools.</span></span> <span data-ttu-id="5474c-109">DNS 負荷分散を使うように構成されているプールには、次の2つの完全修飾ドメイン名 (Fqdn) が定義されている必要があります。 DNS の負荷分散 (たとえば、pool1.contoso.com) によって使用され、プール内のサーバーの物理 Ip アドレスに解決されるレギュラープール FQDN と、プールの Web サービス (web1.contoso.net など) の別の FQDN がプールの仮想 IP アドレスに解決されます。</span><span class="sxs-lookup"><span data-stu-id="5474c-109">A pool that is configured to use DNS load balancing must have two fully qualified domain names (FQDNs) defined: the regular pool FQDN that is used by DNS load balancing (for example, pool1.contoso.com) and that resolves to the physical IPs of the servers in the pool, and another FQDN for the pool’s Web Services (for example, web1.contoso.net), which resolves to the virtual IP address of the pool.</span></span> <span data-ttu-id="5474c-110">DNS の負荷分散の詳細については、計画ドキュメントの「 [Lync Server 2013 での dns の負荷分散](lync-server-2013-dns-load-balancing.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5474c-110">For details about DNS Load Balancing, see [DNS load balancing in Lync Server 2013](lync-server-2013-dns-load-balancing.md) in the Planning documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="5474c-111">クライアント間の HTTPS トラフィックには、依然としてハードウェア負荷分散が必要です。</span><span class="sxs-lookup"><span data-stu-id="5474c-111">Hardware load balancing is still required for client to server HTTPS traffic.</span></span>



</div>

<span data-ttu-id="5474c-112">DNS の負荷分散を使用するには、次の手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5474c-112">Before you can use DNS load balancing, you must do the following:</span></span>

1.  <span data-ttu-id="5474c-113">内部 Web サービスプールの FQDN を上書きします。</span><span class="sxs-lookup"><span data-stu-id="5474c-113">Override the internal Web Services pool FQDN.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="5474c-114">自己定義の FQDN を使用して内部 web サービスを上書きする場合、各 FQDN は、他のフロントエンドプール、ディレクター、またはディレクタープールから一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="5474c-114">If decide to override the Internal web services with a self-defined FQDN, each FQDN must be unique from any other Front End pool, Director or a Director pool.</span></span>

    
    </div>

2.  <span data-ttu-id="5474c-115">DNS A host レコードを作成して、プールの FQDN を解決し、プール内のすべてのサーバーの IP アドレスを解決します。</span><span class="sxs-lookup"><span data-stu-id="5474c-115">Create DNS A host records to resolve the pool FQDN to the IP addresses of all the servers in the pool.</span></span>

3.  <span data-ttu-id="5474c-116">IP アドレスをランダムに有効にするか、Windows Server DNS の場合は、ラウンドロビンを有効にします。</span><span class="sxs-lookup"><span data-stu-id="5474c-116">Enable IP Address randomization or, for Windows Server DNS, enable round robin.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="5474c-117">ラウンドロビンは既定で有効になっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="5474c-117">Round robin should be enabled by default.</span></span>

    
    </div>

<div>

## <a name="to-override-internal-web-services-fqdn"></a><span data-ttu-id="5474c-118">内部 Web サービスの FQDN を上書きするには</span><span class="sxs-lookup"><span data-stu-id="5474c-118">To override internal Web services FQDN</span></span>

1.  <span data-ttu-id="5474c-119">トポロジビルダーを開始します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server Topology Builder**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="5474c-119">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="5474c-120">コンソールツリーで、Enterprise Edition の [フロントエンドプール] ノードを展開します。</span><span class="sxs-lookup"><span data-stu-id="5474c-120">From the console tree, expand the Enterprise Edition Front End pools node.</span></span>

3.  <span data-ttu-id="5474c-121">プールを右クリックし、[ **プロパティの編集**] をクリックして、[ **Web サービス**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5474c-121">Right-click the pool, click **Edit Properties**, and then click **Web Services**.</span></span>

4.  <span data-ttu-id="5474c-122">[ **内部 web サービス**] の下で、[ **FQDN の上書き** ] チェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="5474c-122">Below **Internal web services**, select the **Override FQDN** check box.</span></span>

5.  <span data-ttu-id="5474c-123">プール内のサーバーの物理 IP アドレスに解決されるプールの FQDN を入力します。</span><span class="sxs-lookup"><span data-stu-id="5474c-123">Type the pool FQDN that resolves to the physical IP addresses of the servers in the pool.</span></span>

6.  <span data-ttu-id="5474c-124">[ **外部 web サービス**] の下に、プールの仮想 IP アドレスに解決される外部プールの FQDN を入力して、[ **OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5474c-124">Below **External web services**, type the external pool FQDN that resolves to the virtual IP addresses of the pool, and then click **OK**.</span></span>

7.  <span data-ttu-id="5474c-125">コンソールツリーで [ **Lync Server 2013**] をクリックし、[ **操作** ] ウィンドウで [ **トポロジの公開**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5474c-125">From the console tree, click **Lync Server 2013**, and then in the **Actions** pane, click **Publish Topology**.</span></span>

</div>

<div>

## <a name="to-create-dns-host-a-records-for-all-internal-pool-servers"></a><span data-ttu-id="5474c-126">すべての内部プールサーバー用の DNS ホスト (A) レコードを作成するには</span><span class="sxs-lookup"><span data-stu-id="5474c-126">To create DNS Host (A) Records for all internal pool servers</span></span>

1.  <span data-ttu-id="5474c-127">[ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **管理ツール**]、[ **DNS**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="5474c-127">Click **Start**, click **All Programs**, click **Administrative Tools**, and then click **DNS**.</span></span>

2.  <span data-ttu-id="5474c-128">**Dns マネージャー** で、レコードを管理する dns サーバーをクリックして展開します。</span><span class="sxs-lookup"><span data-stu-id="5474c-128">In **DNS Manager**, click the DNS Server that manages your records to expand it.</span></span>

3.  <span data-ttu-id="5474c-129">[ **前方参照ゾーン** ] をクリックして展開します。</span><span class="sxs-lookup"><span data-stu-id="5474c-129">Click **Forward Lookup Zones** to expand it.</span></span>

4.  <span data-ttu-id="5474c-130">レコードを追加する必要がある DNS ドメインを右クリックし、[ **新しいホスト (A または AAAA)**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5474c-130">Right-click the DNS domain that you need to add records to, and then click **New Host (A or AAAA)**.</span></span>

5.  <span data-ttu-id="5474c-131">[**名前**] ボックスにホスト レコード名を入力します (ドメイン名は自動的に追加されます)。</span><span class="sxs-lookup"><span data-stu-id="5474c-131">In the **Name** box, type the name of the host record (the domain name will be automatically appended).</span></span>

6.  <span data-ttu-id="5474c-132">[IP アドレス] ボックスに、個々のフロントエンドサーバーの IP アドレスを入力し、[ **関連付けられたポインター (PTR) レコードを作成** する] を選択するか、または該当する場合は、認証された **すべてのユーザーが同じ所有者名で DNS レコードを更新できるように** します。</span><span class="sxs-lookup"><span data-stu-id="5474c-132">In the IP Address box, type the IP address of the individual Front End Server and then select **Create associated pointer (PTR) record** or **Allow any authenticated user to update DNS records with the same owner name**, if applicable.</span></span>

7.  <span data-ttu-id="5474c-133">DNS の負荷分散に参加するすべてのメンバーのフロントエンドサーバーのレコードの作成を続けます。</span><span class="sxs-lookup"><span data-stu-id="5474c-133">Continue creating records for all member Front End Servers that will participate in DNS Load Balancing.</span></span>
    
    <span data-ttu-id="5474c-134">たとえば、pool1.contoso.com と3つのフロントエンドサーバーという名前のプールがある場合は、次の DNS エントリを作成します。</span><span class="sxs-lookup"><span data-stu-id="5474c-134">For example, if you had a pool named pool1.contoso.com and three Front End Servers, you would create the following DNS entries:</span></span>
    
    
    <table>
    <colgroup>
    <col style="width: 33%" />
    <col style="width: 33%" />
    <col style="width: 33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="5474c-135">FQDN</span><span class="sxs-lookup"><span data-stu-id="5474c-135">FQDN</span></span></th>
    <th><span data-ttu-id="5474c-136">型</span><span class="sxs-lookup"><span data-stu-id="5474c-136">Type</span></span></th>
    <th><span data-ttu-id="5474c-137">データ</span><span class="sxs-lookup"><span data-stu-id="5474c-137">Data</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="5474c-138">Pool1.contoso.com</span><span class="sxs-lookup"><span data-stu-id="5474c-138">Pool1.contoso.com</span></span></p></td>
    <td><p><span data-ttu-id="5474c-139">ホスト (A)</span><span class="sxs-lookup"><span data-stu-id="5474c-139">Host (A)</span></span></p></td>
    <td><p><span data-ttu-id="5474c-140">192.168.1.1</span><span class="sxs-lookup"><span data-stu-id="5474c-140">192.168.1.1</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="5474c-141">Pool1.contoso.com</span><span class="sxs-lookup"><span data-stu-id="5474c-141">Pool1.contoso.com</span></span></p></td>
    <td><p><span data-ttu-id="5474c-142">ホスト (A)</span><span class="sxs-lookup"><span data-stu-id="5474c-142">Host (A)</span></span></p></td>
    <td><p><span data-ttu-id="5474c-143">192.168.1.2</span><span class="sxs-lookup"><span data-stu-id="5474c-143">192.168.1.2</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="5474c-144">Pool1.contoso.com</span><span class="sxs-lookup"><span data-stu-id="5474c-144">Pool1.contoso.com</span></span></p></td>
    <td><p><span data-ttu-id="5474c-145">ホスト (A)</span><span class="sxs-lookup"><span data-stu-id="5474c-145">Host (A)</span></span></p></td>
    <td><p><span data-ttu-id="5474c-146">192.168.1.3</span><span class="sxs-lookup"><span data-stu-id="5474c-146">192.168.1.3</span></span></p></td>
    </tr>
    </tbody>
    </table>
    
    <span data-ttu-id="5474c-147">DNS Host (A) レコードの作成の詳細については、「 [Lync Server 2013 の Dns ホストレコードを構成](lync-server-2013-configure-dns-host-records.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5474c-147">For details about creating DNS Host (A) records, see [Configure DNS Host records for Lync Server 2013](lync-server-2013-configure-dns-host-records.md).</span></span>

</div>

<div>

## <a name="to-enable-round-robin-for-windows-server"></a><span data-ttu-id="5474c-148">Windows Server のラウンドロビンを有効にするには</span><span class="sxs-lookup"><span data-stu-id="5474c-148">To enable round robin for Windows Server</span></span>

1.  <span data-ttu-id="5474c-149">[ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **管理ツール**]、[ **DNS**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="5474c-149">Click **Start**, click **All Programs**, click **Administrative Tools**, and then click **DNS**.</span></span>

2.  <span data-ttu-id="5474c-150">[ **Dns**] を展開し、構成する dns サーバーを右クリックして、[ **プロパティ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5474c-150">Expand **DNS**, right-click the DNS server you want to configure, and then click **Properties**.</span></span>

3.  <span data-ttu-id="5474c-151">[ **詳細設定** ] タブをクリックし、[ **ラウンドロビンを有効に** して **ネットマスクの順序を有効** にする] を選び、[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5474c-151">Click the **Advanced** tab, select **Enable round robin** and **Enable netmask ordering**, and then click **OK**.</span></span>
    
    <span data-ttu-id="5474c-152">![[DNS ラウンドロビン] ダイアログボックス](images/Gg398251.e7bf6125-8d78-4460-8401-0a8e7e21d305(OCS.15).jpg "[DNS ラウンドロビン] ダイアログボックス")</span><span class="sxs-lookup"><span data-stu-id="5474c-152">![DNS Round Robin dialog box](images/Gg398251.e7bf6125-8d78-4460-8401-0a8e7e21d305(OCS.15).jpg "DNS Round Robin dialog box")</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="5474c-153">この機能は既定で有効になっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="5474c-153">This feature should be enabled by default.</span></span>



</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="5474c-154">関連項目</span><span class="sxs-lookup"><span data-stu-id="5474c-154">See Also</span></span>


[<span data-ttu-id="5474c-155">Lync Server 2013 での DNS の負荷分散</span><span class="sxs-lookup"><span data-stu-id="5474c-155">DNS load balancing in Lync Server 2013</span></span>](lync-server-2013-dns-load-balancing.md)  
  

<span data-ttu-id="5474c-156"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5474c-156"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

