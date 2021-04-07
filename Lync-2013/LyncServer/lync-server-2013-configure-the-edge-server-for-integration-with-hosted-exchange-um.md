---
title: Hosted Exchange UM との統合のためのエッジ サーバーの構成
description: ホストされている Exchange UM と統合するエッジ サーバーを構成します。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure the Edge Server for integration with hosted Exchange UM
ms:assetid: ede3f2f9-f412-418e-a705-8d8ec98176c5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399075(v=OCS.15)
ms:contentKeyID: 48185745
ms.date: 01/24/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d1a2eb55df172e6df0bacef0c468a235cb00c3f3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433648"
---
# <a name="configure-the-edge-server-for-integration-with-hosted-exchange-um"></a><span data-ttu-id="7f3a4-103">Hosted Exchange UM との統合のためのエッジ サーバーの構成</span><span class="sxs-lookup"><span data-stu-id="7f3a4-103">Configure the Edge Server for integration with hosted Exchange UM</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7f3a4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7f3a4-104">

<span> </span></span></span>

<span data-ttu-id="7f3a4-105">_**トピック最終更新日:** 2015-01-23_</span><span class="sxs-lookup"><span data-stu-id="7f3a4-105">_**Topic Last Modified:** 2015-01-23_</span></span>

<span data-ttu-id="7f3a4-106">Lync Server 2013 ユーザーに、ホスト型 Exchange ユニファイド メッセージング (UM) のボイス メール機能を提供するには、Edge Server で次の構成タスクを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f3a4-106">To provide your Lync Server 2013 users with voice mail capabilities on hosted Exchange Unified Messaging (UM), you must perform the following configuration tasks on the Edge Server:</span></span>

  - <span data-ttu-id="7f3a4-107">フェデレーションのためにエッジ サーバーを構成します。</span><span class="sxs-lookup"><span data-stu-id="7f3a4-107">Configure the Edge Server for federation.</span></span>

  - <span data-ttu-id="7f3a4-108">サーバーの全体管理ストアのデータをエッジ サーバーに複製し、レプリケーションを確認します。</span><span class="sxs-lookup"><span data-stu-id="7f3a4-108">Replicate Central Management store data to the Edge Server and verify the replication.</span></span>

  - <span data-ttu-id="7f3a4-109">エッジ サーバーのホスティング プロバイダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="7f3a4-109">Create a hosting provider on the Edge Server.</span></span>

<span data-ttu-id="7f3a4-110">詳細については、次のコマンドレットの Lync Server 管理シェルのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7f3a4-110">For details, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - <span data-ttu-id="7f3a4-111">[Set-CsAccessEdgeConfiguration](https://technet.microsoft.com/library/Gg413017(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="7f3a4-111">[Set-CsAccessEdgeConfiguration](https://technet.microsoft.com/library/Gg413017(v=OCS.15))</span></span>

  - <span data-ttu-id="7f3a4-112">[New-CsHostingProvider](https://technet.microsoft.com/library/Gg398490(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="7f3a4-112">[New-CsHostingProvider](https://technet.microsoft.com/library/Gg398490(v=OCS.15))</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="7f3a4-113">これらの手順を実行する前に、Hosted Exchange サービス用の外部 DNS SRV レコードを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f3a4-113">You must create an external DNS SRV record for the hosting Exchange service before you perform these steps.</span></span> <span data-ttu-id="7f3a4-114">詳細については、「ホストされた <A href="lync-server-2013-create-a-dns-srv-record-for-integration-with-hosted-exchange-um.md">Exchange UM と統合するために DNS SRV レコードを作成する」を参照してください</A>。</span><span class="sxs-lookup"><span data-stu-id="7f3a4-114">For details, see <A href="lync-server-2013-create-a-dns-srv-record-for-integration-with-hosted-exchange-um.md">Create a DNS SRV record for integration with hosted Exchange UM</A>.</span></span>



</div>

<div>

## <a name="to-configure-the-edge-server-for-federation"></a><span data-ttu-id="7f3a4-115">フェデレーションのためにエッジ サーバーを構成するには</span><span class="sxs-lookup"><span data-stu-id="7f3a4-115">To configure the Edge Server for federation</span></span>

1.  <span data-ttu-id="7f3a4-116">Lync Server 管理シェルを開始する: [スタート] をクリックし、[すべてのプログラム] をクリックし **、[Microsoft Lync Server 2013]** をクリックして、[Lync Server 管理シェル]**をクリックします**。</span><span class="sxs-lookup"><span data-stu-id="7f3a4-116">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="7f3a4-p102">Set-CsAccessEdgeConfiguration コマンドレットを実行して、フェデレーションのためにサーバーを構成します。たとえば、以下を実行します。</span><span class="sxs-lookup"><span data-stu-id="7f3a4-p102">Run the Set-CsAccessEdgeConfiguration cmdlet to configure the server for federation. For example, run:</span></span>
    
        Set-CsAccessEdgeConfiguration -UseDnsSrvRouting -AllowFederatedUsers 1 -EnablePartnerDiscovery 0
    
    <span data-ttu-id="7f3a4-119">上述の例では、次のパラメーターが設定されます。</span><span class="sxs-lookup"><span data-stu-id="7f3a4-119">The preceding example sets the following parameters:</span></span>
    
      - <span data-ttu-id="7f3a4-120">**UseDnsSrvRouting** は、エッジ サーバーがフェデレーション要求を送信および受信するときに、DNS SRV レコードを使用するように指定します。</span><span class="sxs-lookup"><span data-stu-id="7f3a4-120">**UseDnsSrvRouting** specifies that Edge Servers will rely on DNS SRV records when sending and receiving federation requests.</span></span>
    
      - <span data-ttu-id="7f3a4-p103">**AllowFederatedUsers** は、内部ユーザーとフェデレーション ドメインからのユーザーとの通信を許可するかどうかを指定します。このプロパティは、さらに内部ユーザーが分割ドメインのシナリオでユーザーと通信できるかどうかも決定します。</span><span class="sxs-lookup"><span data-stu-id="7f3a4-p103">**AllowFederatedUsers** specifies whether internal users are allowed to communicate with users from federated domains. This property also determines whether internal users can communicate with users in a split domain scenario.</span></span>
    
      - <span data-ttu-id="7f3a4-123">**EnablePartnerDiscovery** では、Lync Server が DNS レコードを使用して、Active Directory の許可ドメイン リストに一覧されていないパートナー ドメインを検出するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="7f3a4-123">**EnablePartnerDiscovery** specifies whether Lync Server will use DNS records to try to discover partner domains not listed in the Active Directory allowed domains list.</span></span> <span data-ttu-id="7f3a4-124">False の場合、Lync Server 2013 は許可されているドメインリストにあるドメインとのみフェデレーションします。</span><span class="sxs-lookup"><span data-stu-id="7f3a4-124">If False, Lync Server 2013 will only federate with domains found on the allowed domains list.</span></span> <span data-ttu-id="7f3a4-125">DNS のサービス ルーティングを使用する場合、このパラメーターは必須です。</span><span class="sxs-lookup"><span data-stu-id="7f3a4-125">This parameter is required if you use DNS service routing.</span></span> <span data-ttu-id="7f3a4-126">ほとんどの展開環境では、すべてのパートナーに対してフェデレーションが開かれることのないように、この値を False に設定します。</span><span class="sxs-lookup"><span data-stu-id="7f3a4-126">In most deployments, the value is set to false to avoid opening up federation to all partners.</span></span>

</div>

<div>

## <a name="to-replicate-data-to-the-edge-server-and-verify-the-replication"></a><span data-ttu-id="7f3a4-127">データをエッジ サーバーにレプリケートし、レプリケーションを確認するには</span><span class="sxs-lookup"><span data-stu-id="7f3a4-127">To replicate data to the Edge Server and verify the replication</span></span>

  - <span data-ttu-id="7f3a4-128">エッジ サーバーへのレプリケーションが完了したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="7f3a4-128">Verify that the replication to the Edge Server is complete.</span></span> <span data-ttu-id="7f3a4-129">手順については [、「Lync Server 2013](lync-server-2013-verify-connectivity-between-internal-servers-and-edge-servers.md)で内部サーバーとエッジ サーバー間の接続を確認する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7f3a4-129">For the procedure, see [Verify connectivity between internal servers and Edge Servers in Lync Server 2013](lync-server-2013-verify-connectivity-between-internal-servers-and-edge-servers.md).</span></span>

</div>

<div>

## <a name="to-create-a-hosting-provider-on-the-edge-server"></a><span data-ttu-id="7f3a4-130">エッジ サーバーのホスティング プロバイダーを作成するには</span><span class="sxs-lookup"><span data-stu-id="7f3a4-130">To create a hosting provider on the Edge Server</span></span>

1.  <span data-ttu-id="7f3a4-131">Lync Server 管理シェルを開始する: [スタート] をクリックし、[すべてのプログラム] をクリックし **、[Microsoft Lync Server 2013]** をクリックして、[Lync Server 管理シェル]**をクリックします**。</span><span class="sxs-lookup"><span data-stu-id="7f3a4-131">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="7f3a4-132">**New-CsHostingProvider** コマンドレットを実行して、ホスティング プロバイダーを構成します。</span><span class="sxs-lookup"><span data-stu-id="7f3a4-132">Run the **New-CsHostingProvider** cmdlet to configure the hosting provider.</span></span> <span data-ttu-id="7f3a4-133">たとえば、以下を実行します。</span><span class="sxs-lookup"><span data-stu-id="7f3a4-133">For example, run:</span></span>
    
        New-CsHostingProvider -Identity Fabrikam.com -Enabled $True -EnabledSharedAddressSpace $True -HostsOCSUsers $False -ProxyFQDN "proxyserver.fabrikam.com" -IsLocal $False -VerificationLevel UseSourceVerification
    
    <span data-ttu-id="7f3a4-134">上述の例では、次のパラメーターが設定されます。</span><span class="sxs-lookup"><span data-stu-id="7f3a4-134">The preceding example sets the following parameters:</span></span>
    
      - <span data-ttu-id="7f3a4-p107">**Identity** では、作成するホスティング プロバイダーの文字列値から成る一意識別子を指定します。この例では **Fabrikam.com** です。既存のプロバイダーがその ID で既に構成されている場合には、このコマンドは失敗することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="7f3a4-p107">**Identity** specifies a unique string value identifier for the hosting provider you are creating, in this example, **Fabrikam.com**. Note that the command will fail if an existing provider has already been configured with that Identity.</span></span>
    
      - <span data-ttu-id="7f3a4-p108">**Enabled** は、ドメインとホスティング プロバイダー間のネットワーク接続が有効になっているかどうかを示します。この値を **True** に設定しないと、2 つの組織間でメッセージを交換することはできません。</span><span class="sxs-lookup"><span data-stu-id="7f3a4-p108">**Enabled** indicates whether the network connection between your domain and the hosting provider is enabled. Messages cannot be exchanged between the two organizations until this value is set to **True**.</span></span>
    
      - <span data-ttu-id="7f3a4-139">**EnabledSharedAddressSpace** では、共有 SIP アドレス スペース (分割ドメイン) シナリオで、ホスティング プロバイダーが使用されているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="7f3a4-139">**EnabledSharedAddressSpace** indicates whether the hosting provider is being used in a shared SIP address space (split domain) scenario.</span></span>
        
        <div>
        

        > [!NOTE]
        > <span data-ttu-id="7f3a4-140">True に設定 <CODE>EnableSharedAddressSpace</CODE> する前に、フェデレーション SRV レコードを内部的に解決してみてください。</span><span class="sxs-lookup"><span data-stu-id="7f3a4-140">Before you set <CODE>EnableSharedAddressSpace</CODE> to True, try to resolve the Federation SRV record internally.</span></span> <span data-ttu-id="7f3a4-141">このレコードを内部で解決できない場合は、レコード _sipfederationtls._tcp を作成する必要があります。 &lt;ドメイン &gt; と _sip._tls。 &lt;内部 &gt; DNS のドメインにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="7f3a4-141">If this record cannot be resolved internally, then you need to create the records, _sipfederationtls._tcp.&lt;domain&gt; and _sip._tls.&lt;domain&gt; in the internal DNS.</span></span> <span data-ttu-id="7f3a4-142">これらのレコードは Edge Server のアクセス インターフェイスの外部 IP アドレスをポイントする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f3a4-142">These records should point to the external IP address of the Access Interface of the Edge Server.</span></span>

        
        </div>
    
      - <span data-ttu-id="7f3a4-143">**HostsOCSUsers は** 、ホスティング プロバイダーが Lync Server 2013 アカウントのホストに使用されているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="7f3a4-143">**HostsOCSUsers** indicates whether the hosting provider is used to host Lync Server 2013 accounts.</span></span> <span data-ttu-id="7f3a4-144">**False** は、プロバイダーが Microsoft Exchange アカウントなど、別の種類のアカウントをホストしていることを示します。</span><span class="sxs-lookup"><span data-stu-id="7f3a4-144">If **False**, the provider hosts other account types, such as Microsoft Exchange accounts.</span></span>
    
      - <span data-ttu-id="7f3a4-p111">**ProxyFQDN** では、ホスティング プロバイダーで使用されているプロキシ サーバーの完全修飾ドメイン名 (FQDN) を指定します。この例では **proxyserver.fabrikam.com** です。この値は変更できません。ホスティング プロバイダーがプロキシ サーバーを変更すると、そのプロバイダーのエントリを削除して再作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f3a4-p111">**ProxyFQDN** specifies the fully qualified domain name (FQDN) for the proxy server used by the hosting provider, in this example, **proxyserver.fabrikam.com**. This value cannot be modified. If the hosting provider changes its proxy server you will need to delete and then recreate the entry for that provider.</span></span>
    
      - <span data-ttu-id="7f3a4-148">**IsLocal** は、ホスティング プロバイダーによって使用されるプロキシ サーバーが Lync Server 2013 トポロジ内に含まれているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="7f3a4-148">**IsLocal** indicates whether the proxy server used by the hosting provider is contained within your Lync Server 2013 topology.</span></span>
    
      - <span data-ttu-id="7f3a4-149">**VerficationLevel** は、ホスティング プロバイダーとのメッセージ送受信に対して許可された確認レベルを示します。</span><span class="sxs-lookup"><span data-stu-id="7f3a4-149">**VerficationLevel** indicates the allowed verification level for messages sent to and from the hosted provider.</span></span> <span data-ttu-id="7f3a4-150">ホスティング プロバイダーから送信されたメッセージに含まれる確認レベルを信頼する **UseSourceVerification** を指定します。</span><span class="sxs-lookup"><span data-stu-id="7f3a4-150">Specify **UseSourceVerification**, which relies on the verification level included in messages sent from the hosting provider.</span></span> <span data-ttu-id="7f3a4-151">このレベルが指定されない場合は、メッセージは確認できないため拒否されます。</span><span class="sxs-lookup"><span data-stu-id="7f3a4-151">If this level is not specified, then the message will be rejected as being unverifiable.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="7f3a4-152">関連項目</span><span class="sxs-lookup"><span data-stu-id="7f3a4-152">See Also</span></span>


[<span data-ttu-id="7f3a4-153">エッジ インストール用の Lync Server 2013 のトポロジをエクスポートして外部メディアにコピーする</span><span class="sxs-lookup"><span data-stu-id="7f3a4-153">Export your Lync Server 2013 topology and copy it to external media for edge installation</span></span>](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md)  


[<span data-ttu-id="7f3a4-154">Lync Server 2013 での内部サーバーとエッジ サーバーの間の接続の検証</span><span class="sxs-lookup"><span data-stu-id="7f3a4-154">Verify connectivity between internal servers and Edge Servers in Lync Server 2013</span></span>](lync-server-2013-verify-connectivity-between-internal-servers-and-edge-servers.md)  


<span data-ttu-id="7f3a4-155">[New-CsHostingProvider](https://technet.microsoft.com/library/Gg398490(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="7f3a4-155">[New-CsHostingProvider](https://technet.microsoft.com/library/Gg398490(v=OCS.15))</span></span>  
  

<span data-ttu-id="7f3a4-156"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7f3a4-156"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

