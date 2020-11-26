---
title: Hosted Exchange UM との統合のための DNS SRV レコードを作成する
description: ホストされた Exchange UM と統合するための DNS SRV レコードを作成します。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create a DNS SRV record for integration with hosted Exchange UM
ms:assetid: 8ea590ae-58ea-4ca5-9853-e0708b3ea760
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh500728(v=OCS.15)
ms:contentKeyID: 48184770
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 694a595977abe33bebbb5fbcf2a508c9bb4e35a4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432234"
---
# <a name="create-a-dns-srv-record-for-integration-with-hosted-exchange-um"></a><span data-ttu-id="fdb49-103">Hosted Exchange UM との統合のための DNS SRV レコードを作成する</span><span class="sxs-lookup"><span data-stu-id="fdb49-103">Create a DNS SRV record for integration with hosted Exchange UM</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fdb49-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fdb49-104">

<span> </span></span></span>

<span data-ttu-id="fdb49-105">_**トピックの最終更新日:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="fdb49-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="fdb49-106">このトピックでは、Lync Server 2013 エッジサーバーが Microsoft Exchange Online などのホストされた Exchange サービスにルーティングするために必要なドメインネームシステム (DNS) SRV レコードを構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="fdb49-106">This topic describes how to configure the Domain Name System (DNS) SRV record that is required for a Lync Server 2013 Edge Server to route to a hosted Exchange service such as Microsoft Exchange Online.</span></span>

<div>

## <a name="to-create-an-external-dns-srv-record-for-the-hosted-exchange-service"></a><span data-ttu-id="fdb49-107">ホストされている Exchange サービスの外部 DNS SRV レコードを作成するには</span><span class="sxs-lookup"><span data-stu-id="fdb49-107">To create an external DNS SRV record for the hosted Exchange service</span></span>

1.  <span data-ttu-id="fdb49-108">DnsAdmins グループのメンバーとして外部 DNS サーバーにログオンします。</span><span class="sxs-lookup"><span data-stu-id="fdb49-108">Log on to the external DNS server as a member of the DnsAdmins group.</span></span>

2.  <span data-ttu-id="fdb49-109">[ **スタート**] をクリックし、[ **管理ツール**]、[ **DNS**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="fdb49-109">Click **Start**, click **Administrative Tools**, and then click **DNS**.</span></span>

3.  <span data-ttu-id="fdb49-110">SIP ドメインのコンソールツリーで [ **前方参照ゾーン**] を展開し、Lync Server 2013 をインストールする SIP ドメインを選択します。</span><span class="sxs-lookup"><span data-stu-id="fdb49-110">In the console tree for your SIP domain, expand **Forward Lookup Zones**, and select the SIP domain in which Lync Server 2013 will be installed.</span></span>
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="fdb49-111">Lync Server がインストールされている、またはインストールされる SIP ドメインで DNS SRV レコードを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fdb49-111">You must create the DNS SRV record in the SIP domain in which Lync Server is or will be installed.</span></span> <span data-ttu-id="fdb49-112">SRV レコードを作成するときに、[このサービスを提供するホスト] フィールドを使う FQDN は、Edge プールの外部 FQDN である必要があります。</span><span class="sxs-lookup"><span data-stu-id="fdb49-112">When you create the SRV record, the FQDN used for the Host offering this service field must be the external FQDN of the Edge pool.</span></span> <span data-ttu-id="fdb49-113">たとえば、Edge プールの外部 FQDN が edge01.contoso.net の場合は、その値を入力します。</span><span class="sxs-lookup"><span data-stu-id="fdb49-113">For example, if the external FQDN of your Edge pool is edge01.contoso.net, enter that value.</span></span> <span data-ttu-id="fdb49-114">また、DNS Hosts (A) レコードと同じドメイン内に存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fdb49-114">This must also be in the same domain as the DNS Hosts (A) record.</span></span>

    
    </div>

4.  <span data-ttu-id="fdb49-115">選んだドメインを右クリックし、[ **その他の新しいレコード**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fdb49-115">Right-click the selected domain, and then click **Other New Records**.</span></span>

5.  <span data-ttu-id="fdb49-116">[ **リソースレコードの種類**] で [ **サービスの場所 (SRV)**] をクリックし、[ **レコードの作成**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fdb49-116">In **Resource Record Type**, click **Service Location (SRV)**, and then click **Create Record**.</span></span>

6.  <span data-ttu-id="fdb49-117">[**新しいリソースレコード**] で、[**サービス**] をクリックし、「 **\_ sipfederationtls**」と入力します。</span><span class="sxs-lookup"><span data-stu-id="fdb49-117">In **New Resource Record**, click **Service**, and then type **\_sipfederationtls**.</span></span>

7.  <span data-ttu-id="fdb49-118">[**プロトコル**] をクリックして、「 **\_ tcp**」と入力します。</span><span class="sxs-lookup"><span data-stu-id="fdb49-118">Click **Protocol**, and then type **\_tcp**.</span></span>

8.  <span data-ttu-id="fdb49-119">[**ポート番号**] をクリックし、「**5061**」と入力します。</span><span class="sxs-lookup"><span data-stu-id="fdb49-119">Click **Port Number**, and then type **5061**.</span></span>

9.  <span data-ttu-id="fdb49-120">[ **このサービスを提供するホスト**] をクリックして、lync Server 2013 Edge プールの完全修飾ドメイン名 (FQDN) を入力します。これにより、信頼できる外部クライアントの lync server 2013 システムへのアクセスが提供されます。</span><span class="sxs-lookup"><span data-stu-id="fdb49-120">Click **Host offering this service**, and then type the fully qualified domain name (FQDN) of the Lync Server 2013 Edge pool that provides access to your Lync Server 2013 system for trusted external clients.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="fdb49-121">また、ドメインは、Exchange Online の設定で、権限を持つ承認済みドメインとして設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fdb49-121">The domain must also be set up as an authoritative, accepted domain in your Exchange Online settings.</span></span> <span data-ttu-id="fdb49-122">詳しくは、「承認されたドメインをで作成する」をご覧ください <A href="https://go.microsoft.com/fwlink/p/?linkid=229762">https://go.microsoft.com/fwlink/p/?linkId=229762</A> 。</span><span class="sxs-lookup"><span data-stu-id="fdb49-122">For details, see Create Accepted Domains at <A href="https://go.microsoft.com/fwlink/p/?linkid=229762">https://go.microsoft.com/fwlink/p/?linkId=229762</A>.</span></span>

    
    </div>

10. <span data-ttu-id="fdb49-123">[**OK**] をクリックしてから、[**完了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fdb49-123">Click **OK**, and then click **Done**.</span></span>

</div>

<div>

## <a name="to-verify-that-the-dns-srv-record-was-created-successfully"></a><span data-ttu-id="fdb49-124">DNS SRV レコードが正常に作成されたことを確認するには</span><span class="sxs-lookup"><span data-stu-id="fdb49-124">To verify that the DNS SRV record was created successfully</span></span>

1.  <span data-ttu-id="fdb49-125">ドメイン内のクライアントコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="fdb49-125">Log on to a client computer in the domain.</span></span>

2.  <span data-ttu-id="fdb49-126">[**スタート**] ボタンをクリックし、[**ファイル名を指定して実行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fdb49-126">Click **Start**, and then click **Run**.</span></span>

3.  <span data-ttu-id="fdb49-127">コマンドプロンプトで、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="fdb49-127">At the command prompt, run the following command:</span></span>
    
        nslookup <FQDN Lync Edge Pool>

4.  <span data-ttu-id="fdb49-128">FQDN の適切な IP アドレスに解決される返信を受信したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="fdb49-128">Verify that you receive a reply that resolves to the appropriate IP address for the FQDN.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="fdb49-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="fdb49-129">See Also</span></span>


[<span data-ttu-id="fdb49-130">Lync Server 2013 でのリバース プロキシ サーバーの DNS レコードの作成</span><span class="sxs-lookup"><span data-stu-id="fdb49-130">Create DNS records for reverse proxy servers in Lync Server 2013</span></span>](lync-server-2013-create-dns-records-for-reverse-proxy-servers.md)  
  

<span data-ttu-id="fdb49-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fdb49-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

