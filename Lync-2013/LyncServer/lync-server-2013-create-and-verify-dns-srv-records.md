---
title: 'Lync Server 2013: DNS SRV レコードの作成と確認'
description: 'Lync Server 2013: DNS SRV レコードを作成して確認します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create and verify DNS SRV records
ms:assetid: 86888c7e-1401-458f-9a7b-08ac726deeec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398680(v=OCS.15)
ms:contentKeyID: 48184714
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a71c876d0b26b9305feed7146fa6321a3983588d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432017"
---
# <a name="create-and-verify-dns-srv-records-in-lync-server-2013"></a><span data-ttu-id="5f1b5-103">Lync Server 2013 での DNS SRV レコードの作成と確認</span><span class="sxs-lookup"><span data-stu-id="5f1b5-103">Create and verify DNS SRV records in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5f1b5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5f1b5-104">

<span> </span></span></span>

<span data-ttu-id="5f1b5-105">_**最終更新日:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="5f1b5-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="5f1b5-106">この手順を完了するには、ドメイン管理者グループのメンバー、または DnsAdmins グループのメンバーとして、サーバーまたはドメインに最低でもログオンしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f1b5-106">To successfully complete this procedure, you should be logged on to the server or domain minimally as a member of the Domain Admins group or a member of the DnsAdmins group.</span></span>

<span data-ttu-id="5f1b5-107">このトピックでは、Lync Server 2013 の展開で作成する必要があるドメインネームシステム (DNS) レコードを構成する方法と、自動クライアントサインインに必要なものを構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5f1b5-107">This topic describes how to configure the Domain Name System (DNS) records that you are required to create in Lync Server 2013 deployments and those required for automatic client sign in.</span></span> <span data-ttu-id="5f1b5-108">フロントエンドプールを作成すると、セットアップによってプールの Active Directory オブジェクトと設定が作成されます。これには、プールの完全修飾ドメイン名 (FQDN) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="5f1b5-108">When you create a Front End pool, Setup creates Active Directory objects and settings for the pool, including the pool fully qualified domain name (FQDN).</span></span> <span data-ttu-id="5f1b5-109">同様のオブジェクトと設定が、Standard Edition サーバー用に作成されます。</span><span class="sxs-lookup"><span data-stu-id="5f1b5-109">Similar objects and settings are created for a Standard Edition server.</span></span> <span data-ttu-id="5f1b5-110">クライアントがプールまたは Standard Edition サーバーに接続できるようにするには、プールまたは Standard Edition サーバーの FQDN が DNS に登録されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f1b5-110">For clients to be able to connect to the pool or Standard Edition server, the FQDN of the pool or Standard Edition server must be registered in DNS.</span></span> <span data-ttu-id="5f1b5-111">SIP ドメインごとに、内部 DNS で DNS SRV レコードを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f1b5-111">You must create DNS SRV records in your internal DNS for every SIP domain.</span></span> <span data-ttu-id="5f1b5-112">この手順では、内部 DNS に SIP ユーザードメイン用のゾーンが含まれていることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="5f1b5-112">This procedure assumes that your internal DNS has zones for your SIP user domains.</span></span>

<div>

## <a name="to-configure-a-dns-srv-record"></a><span data-ttu-id="5f1b5-113">DNS SRV レコードを構成するには</span><span class="sxs-lookup"><span data-stu-id="5f1b5-113">To configure a DNS SRV record</span></span>

1.  <span data-ttu-id="5f1b5-114">DNS サーバーで [ **スタート**] をクリックし、[ **管理ツール**]、[ **dns**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="5f1b5-114">On the DNS server, click **Start**, click **Administrative Tools**, and then click **DNS**.</span></span>

2.  <span data-ttu-id="5f1b5-115">SIP ドメインのコンソールツリーで [ **前方参照ゾーン**] を展開し、Lync Server 2013 がインストールされる SIP ドメインを右クリックします。</span><span class="sxs-lookup"><span data-stu-id="5f1b5-115">In the console tree for your SIP domain, expand **Forward Lookup Zones**, and then right-click the SIP domain in which Lync Server 2013 will be installed.</span></span>

3.  <span data-ttu-id="5f1b5-116">[ **その他の新しいレコード**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5f1b5-116">Click **Other New Records**.</span></span>

4.  <span data-ttu-id="5f1b5-117">[**リソース レコードの種類を選択**] の [**サービス ロケーション (SRV)**] をクリックし、[**レコードの作成**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5f1b5-117">In **Select a resource record type**, click **Service Location (SRV)**, and then click **Create Record**.</span></span>

5.  <span data-ttu-id="5f1b5-118">[**サービス**] をクリックして、「 **\_ sipinternaltls**」と入力します。</span><span class="sxs-lookup"><span data-stu-id="5f1b5-118">Click **Service**, and then type **\_sipinternaltls**.</span></span>

6.  <span data-ttu-id="5f1b5-119">[**プロトコル**] をクリックして、「 **\_ tcp**」と入力します。</span><span class="sxs-lookup"><span data-stu-id="5f1b5-119">Click **Protocol**, and then type **\_tcp**.</span></span>

7.  <span data-ttu-id="5f1b5-120">[**ポート番号**] をクリックし、「**5061**」と入力します。</span><span class="sxs-lookup"><span data-stu-id="5f1b5-120">Click **Port Number**, and then type **5061**.</span></span>

8.  <span data-ttu-id="5f1b5-121">[**このサービスを提供しているホスト**] をクリックして、プールまたは Standard Edition サーバーの FQDN を入力します。</span><span class="sxs-lookup"><span data-stu-id="5f1b5-121">Click **Host offering this service**, and then type the FQDN of the pool or Standard Edition server.</span></span>

9.  <span data-ttu-id="5f1b5-122">[**OK**] をクリックしてから、[**完了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5f1b5-122">Click **OK**, and then click **Done**.</span></span>

</div>

<div>

## <a name="to-verify-the-creation-of-a-dns-srv-record"></a><span data-ttu-id="5f1b5-123">DNS SRV レコードの作成を確認するには</span><span class="sxs-lookup"><span data-stu-id="5f1b5-123">To verify the creation of a DNS SRV record</span></span>

1.  <span data-ttu-id="5f1b5-124">Authenticated Users グループのメンバーであるアカウントまたは同等のアクセス許可を持つアカウントを使用して、ドメインのクライアント コンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="5f1b5-124">Log on to a client computer in the domain with an account that is a member of the Authenticated Users group or has equivalent permissions.</span></span>

2.  <span data-ttu-id="5f1b5-125">[**スタート**] ボタンをクリックし、[**ファイル名を指定して実行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5f1b5-125">Click **Start**, and then click **Run**.</span></span>

3.  <span data-ttu-id="5f1b5-126">[ **開く** ] ボックスに **cmd** と入力し、[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5f1b5-126">In the **Open** box, type **cmd**, and then click **OK**.</span></span>

4.  <span data-ttu-id="5f1b5-127">コマンドプロンプトで「 **nslookup**」と入力し、enter キーを押します。</span><span class="sxs-lookup"><span data-stu-id="5f1b5-127">At the command prompt, type **nslookup**, and then press ENTER.</span></span>

5.  <span data-ttu-id="5f1b5-128">「 **Set type = srv**」と入力して、enter キーを押します。</span><span class="sxs-lookup"><span data-stu-id="5f1b5-128">Type **set type=srv**, and then press ENTER.</span></span>

6.  <span data-ttu-id="5f1b5-129">「Sipinternaltls」と入力 **\_ します。 \_tcp.contoso.com** を選び、enter キーを押します。</span><span class="sxs-lookup"><span data-stu-id="5f1b5-129">Type **\_sipinternaltls.\_tcp.contoso.com**, and then press ENTER.</span></span> <span data-ttu-id="5f1b5-130">トランスポート層セキュリティ (TLS) レコードに対して表示される出力は、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="5f1b5-130">The output displayed for the Transport Layer Security (TLS) record is as follows:</span></span>
    
    <span data-ttu-id="5f1b5-131">サーバー: \<dns server\> contoso.com</span><span class="sxs-lookup"><span data-stu-id="5f1b5-131">Server: \<dns server\>.contoso.com</span></span>
    
    <span data-ttu-id="5f1b5-132">アドレス \<IP address of DNS server\></span><span class="sxs-lookup"><span data-stu-id="5f1b5-132">Address: \<IP address of DNS server\></span></span>
    
    <span data-ttu-id="5f1b5-133">権限のない回答:</span><span class="sxs-lookup"><span data-stu-id="5f1b5-133">Non-authoritative answer:</span></span>
    
    <span data-ttu-id="5f1b5-134">\_sipinternaltls。 \_tcp.contoso.com SRV サービスの場所:</span><span class="sxs-lookup"><span data-stu-id="5f1b5-134">\_sipinternaltls.\_tcp.contoso.com SRV service location:</span></span>
    
    <span data-ttu-id="5f1b5-135">priority = 0</span><span class="sxs-lookup"><span data-stu-id="5f1b5-135">priority = 0</span></span>
    
    <span data-ttu-id="5f1b5-136">weight = 0</span><span class="sxs-lookup"><span data-stu-id="5f1b5-136">weight = 0</span></span>
    
    <span data-ttu-id="5f1b5-137">ポート = 5061</span><span class="sxs-lookup"><span data-stu-id="5f1b5-137">port = 5061</span></span>
    
    <span data-ttu-id="5f1b5-138">svr hostname = poolname.contoso.com (または Standard Edition server A レコード)</span><span class="sxs-lookup"><span data-stu-id="5f1b5-138">svr hostname = poolname.contoso.com (or Standard Edition server A record)</span></span>
    
    <span data-ttu-id="5f1b5-139">poolname.contoso.com インターネットアドレス = \<virtual IP Address of the load balancer\> また \<IP address of a single Enterprise Edition server for pools with only one Enterprise Edition server\> は \<IP address of the Standard Edition server\></span><span class="sxs-lookup"><span data-stu-id="5f1b5-139">poolname.contoso.com internet address = \<virtual IP Address of the load balancer\> or \<IP address of a single Enterprise Edition server for pools with only one Enterprise Edition server\> or \<IP address of the Standard Edition server\></span></span>

7.  <span data-ttu-id="5f1b5-140">完了したら、コマンドプロンプトで「 **exit**」と入力し、enter キーを押します。</span><span class="sxs-lookup"><span data-stu-id="5f1b5-140">When you are finished, at the command prompt, type **exit**, and then press ENTER.</span></span>

</div>

<div>

## <a name="to-verify-that-the-fqdn-of-the-front-end-pool-or-standard-edition-server-can-be-resolved"></a><span data-ttu-id="5f1b5-141">フロントエンドプールまたは Standard Edition サーバーの FQDN が解決できることを確認するには</span><span class="sxs-lookup"><span data-stu-id="5f1b5-141">To verify that the FQDN of the Front End pool or Standard Edition server can be resolved</span></span>

1.  <span data-ttu-id="5f1b5-142">ドメイン内のクライアントコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="5f1b5-142">Log on to a client computer in the domain.</span></span>

2.  <span data-ttu-id="5f1b5-143">[**スタート**] ボタンをクリックし、[**ファイル名を指定して実行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5f1b5-143">Click **Start**, and then click **Run**.</span></span>

3.  <span data-ttu-id="5f1b5-144">[ **開く** ] ボックスに **cmd** と入力し、[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5f1b5-144">In the **Open** box, type **cmd**, and then click **OK**.</span></span>

4.  <span data-ttu-id="5f1b5-145">コマンドプロンプトで、「 **nslookup** 」 \<FQDN of the Front End pool\> または「」と入力し、 \<FQDN of the Standard Edition server\> enter キーを押します。</span><span class="sxs-lookup"><span data-stu-id="5f1b5-145">At the command prompt, type **nslookup** \<FQDN of the Front End pool\> or \<FQDN of the Standard Edition server\>, and then press ENTER.</span></span>

5.  <span data-ttu-id="5f1b5-146">FQDN の適切な IP アドレスに解決される返信を受信したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="5f1b5-146">Verify that you receive a reply that resolves to the appropriate IP address for the FQDN.</span></span>

<span data-ttu-id="5f1b5-147"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5f1b5-147"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

