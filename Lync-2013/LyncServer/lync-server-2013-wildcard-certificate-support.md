---
title: Lync Server 2013 のワイルドカード証明書のサポート
description: Lync Server 2013 ワイルドカード証明書のサポート。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Wildcard certificate support
ms:assetid: 0bae2aa8-b6dc-46f5-a3be-3fe7581809d4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202161(v=OCS.15)
ms:contentKeyID: 48183382
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 46cc362eb925a86b5e90d51569db6d425ba88fa6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398913"
---
# <a name="wildcard-certificate-support-in-lync-server-2013"></a><span data-ttu-id="b5e1e-103">Lync Server 2013 のワイルドカード証明書のサポート</span><span class="sxs-lookup"><span data-stu-id="b5e1e-103">Wildcard certificate support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b5e1e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b5e1e-104">

<span> </span></span></span>

<span data-ttu-id="b5e1e-105">_**最終更新日:** 2013-03-21_</span><span class="sxs-lookup"><span data-stu-id="b5e1e-105">_**Topic Last Modified:** 2013-03-21_</span></span>

<span data-ttu-id="b5e1e-106">Lync Server 2013 は、証明書を使って通信の暗号化とサーバー id 認証を提供します。</span><span class="sxs-lookup"><span data-stu-id="b5e1e-106">Lync Server 2013 uses certificates to provide communications encryption and server identity authentication.</span></span> <span data-ttu-id="b5e1e-107">リバースプロキシ経由の web 公開など、サービスを提供するサーバーの完全修飾ドメイン名 (FQDN) に一致する厳密なサブジェクト代替名 (SAN) エントリは必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="b5e1e-107">In some cases, such as web publishing through the reverse proxy, strong subject alternative name (SAN) entry matching to the fully qualified domain name (FQDN) of the server presenting the service is not required.</span></span> <span data-ttu-id="b5e1e-108">このような場合は、ワイルドカード SAN エントリ (一般的には "ワイルドカード証明書" と呼ばれます) の証明書を使用して、公共の証明機関から要求された証明書のコストを削減し、証明書の計画プロセスの複雑さを軽減することができます。</span><span class="sxs-lookup"><span data-stu-id="b5e1e-108">In these cases, you can use certificates with wildcard SAN entries (commonly known as “wildcard certificates”) to reduce the cost of a certificate requested from a public certification authority and to reduce the complexity of the planning process for certificates.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="b5e1e-109">統合通信 (UC) デバイス (卓上電話など) の機能を維持するには、展開された証明書を慎重にテストして、ワイルドカード証明書の実装後にデバイスが正常に機能することを確認します。</span><span class="sxs-lookup"><span data-stu-id="b5e1e-109">To retain the functionality of unified communications (UC) devices (for example, desk phones), you should test the deployed certificate carefully to ensure that devices function properly after you implement a wildcard certificate.</span></span>



</div>

<span data-ttu-id="b5e1e-110">ワイルドカードエントリは、どのロールのサブジェクト名 (共通名または CN とも呼ばれます) としてはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="b5e1e-110">There is no support for a wildcard entry as the subject name (also referred to as the common name or CN) for any role.</span></span> <span data-ttu-id="b5e1e-111">SAN でワイルドカードエントリを使用する場合、次のサーバーの役割がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="b5e1e-111">The following server roles are supported when using wildcard entries in the SAN:</span></span>

  - <span></span>  
    <span data-ttu-id="b5e1e-112">**リバースプロキシ。**</span><span class="sxs-lookup"><span data-stu-id="b5e1e-112">**Reverse proxy.**</span></span>   <span data-ttu-id="b5e1e-113">簡単な URL (会議とダイヤルイン) の発行証明書については、ワイルドカード SAN エントリがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="b5e1e-113">Wildcard SAN entry is supported for Simple URL (meet and dialin) publishing certificate.</span></span>

  - <span></span>  
    <span data-ttu-id="b5e1e-114">**リバースプロキシ。**</span><span class="sxs-lookup"><span data-stu-id="b5e1e-114">**Reverse proxy.**</span></span>   <span data-ttu-id="b5e1e-115">発行証明書の LyncDiscover の SAN エントリで、ワイルドカード SAN エントリがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="b5e1e-115">Wildcard SAN entry is supported for the SAN entries for LyncDiscover on the publishing certificate.</span></span>

  - <span></span>  
    <span data-ttu-id="b5e1e-116">**重役.**</span><span class="sxs-lookup"><span data-stu-id="b5e1e-116">**Director.**</span></span>   <span data-ttu-id="b5e1e-117">簡単な Url (会議とダイヤルイン) でのワイルドカードによる SAN エントリ、およびディレクター web コンポーネントの LyncDiscover と LyncDiscoverInternal の SAN エントリがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="b5e1e-117">Wildcard SAN entry is supported for Simple URLs (meet and dialin) and for SAN entries for LyncDiscover and LyncDiscoverInternal in Director web components.</span></span>

  - <span></span>  
    <span data-ttu-id="b5e1e-118">**フロントエンドサーバー (Standard Edition) とフロントエンドプール (Enterprise Edition)。**</span><span class="sxs-lookup"><span data-stu-id="b5e1e-118">**Front End Server (Standard Edition) and Front End pool (Enterprise Edition).**</span></span> <span data-ttu-id="b5e1e-119">ワイルドカード SAN エントリは、単純な Url (会議とダイヤルイン) でサポートされています。また、フロントエンド web コンポーネントの LyncDiscover と LyncDiscoverInternal の SAN エントリに対応しています。</span><span class="sxs-lookup"><span data-stu-id="b5e1e-119">Wildcard SAN entry is supported for Simple URLs (meet and dialin) and for SAN entries for LyncDiscover and LyncDiscoverInternal in Front End web components.</span></span>

  - <span></span>  
    <span data-ttu-id="b5e1e-120">**Exchange ユニファイドメッセージング (UM)。**</span><span class="sxs-lookup"><span data-stu-id="b5e1e-120">**Exchange Unified Messaging (UM).**</span></span>   <span data-ttu-id="b5e1e-121">サーバーでは、スタンドアロンサーバーとして展開する場合、SAN エントリは使用されません。</span><span class="sxs-lookup"><span data-stu-id="b5e1e-121">The server does not use SAN entries when deployed as a stand-alone server.</span></span>

  - <span></span>  
    <span data-ttu-id="b5e1e-122">**Microsoft Exchange Server クライアントアクセスサーバー。**</span><span class="sxs-lookup"><span data-stu-id="b5e1e-122">**Microsoft Exchange Server Client Access server.**</span></span>   <span data-ttu-id="b5e1e-123">SAN のワイルドカードエントリは、内部と外部のクライアントでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="b5e1e-123">Wildcard entries in the SAN are supported for internal and external clients.</span></span>

  - <span></span>  
    <span data-ttu-id="b5e1e-124">**同じサーバー上の exchange ユニファイドメッセージング (UM) と Microsoft Exchange Server クライアントアクセスサーバー。**</span><span class="sxs-lookup"><span data-stu-id="b5e1e-124">**Exchange Unified Messaging (UM) and Microsoft Exchange Server Client Access server on same server.**</span></span>   <span data-ttu-id="b5e1e-125">ワイルドカード SAN エントリがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="b5e1e-125">Wildcard SAN entries are supported.</span></span>

<span data-ttu-id="b5e1e-126">このトピックでは対処できないサーバーの役割:</span><span class="sxs-lookup"><span data-stu-id="b5e1e-126">Server roles that are not addressed in this topic:</span></span>

  - <span data-ttu-id="b5e1e-127">内部サーバーの役割 (仲介サーバー、アーカイブおよび監視サーバー、Survivable Branch Appliance、または Survivable ブランチサーバーなどに限定されない)</span><span class="sxs-lookup"><span data-stu-id="b5e1e-127">Internal server roles (including, but not limited to the Mediation Server, Archiving and Monitoring Server, Survivable Branch Appliance, or Survivable Branch Server)</span></span>

  - <span data-ttu-id="b5e1e-128">外部エッジサーバーインターフェイス</span><span class="sxs-lookup"><span data-stu-id="b5e1e-128">External Edge Server interfaces</span></span>

  - <span data-ttu-id="b5e1e-129">内部エッジサーバー</span><span class="sxs-lookup"><span data-stu-id="b5e1e-129">Internal Edge Server</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="b5e1e-130">内部エッジサーバーインターフェイスの場合、ワイルドカードエントリは SAN に割り当てることができ、サポートされています。</span><span class="sxs-lookup"><span data-stu-id="b5e1e-130">For the internal Edge Server interface, a wildcard entry can be assigned to the SAN, and is supported.</span></span> <span data-ttu-id="b5e1e-131">内部エッジサーバー上の SAN は照会されず、ワイルドカード SAN エントリの値が制限されます。</span><span class="sxs-lookup"><span data-stu-id="b5e1e-131">The SAN on the internal Edge Server is not queried, and a wildcard SAN entry is of limited value.</span></span>

    
    </div>

<span data-ttu-id="b5e1e-132">証明書でのワイルドカードの使用など、証明書の構成の詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5e1e-132">For details about certificate configurations, including the use of wildcards in certificates, see the following topics:</span></span>

  - [<span data-ttu-id="b5e1e-133">Lync Server 2013 の内部サーバーに対する証明書要件</span><span class="sxs-lookup"><span data-stu-id="b5e1e-133">Certificate requirements for internal servers in Lync Server 2013</span></span>](lync-server-2013-certificate-requirements-for-internal-servers.md)

  - [<span data-ttu-id="b5e1e-134">Lync Server 2013 における外部ユーザー アクセスに対する証明書要件</span><span class="sxs-lookup"><span data-stu-id="b5e1e-134">Certificate requirements for external user access in Lync Server 2013</span></span>](lync-server-2013-certificate-requirements-for-external-user-access.md)

  - [<span data-ttu-id="b5e1e-135">証明書の概要 - Lync Server 2013 の DNS および HLB による負荷分散</span><span class="sxs-lookup"><span data-stu-id="b5e1e-135">Certificate summary - DNS and HLB load balanced in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-dns-and-hlb-load-balanced.md)

  - [<span data-ttu-id="b5e1e-136">証明書の概要 - Lync Server 2013 の単一ディレクター</span><span class="sxs-lookup"><span data-stu-id="b5e1e-136">Certificate summary - Single Director in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-single-director.md)

  - [<span data-ttu-id="b5e1e-137">証明書の概要 - Lync Server 2013 の拡張ディレクター プール、ハードウェア ロード バランサー</span><span class="sxs-lookup"><span data-stu-id="b5e1e-137">Certificate summary - Scaled Director pool, hardware load balancer in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-scaled-director-pool-hardware-load-balancer.md)

  - [<span data-ttu-id="b5e1e-138">証明書の概要 - Lync Server 2013 リバース プロキシ</span><span class="sxs-lookup"><span data-stu-id="b5e1e-138">Certificate summary - Reverse proxy in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-reverse-proxy.md)

  - [<span data-ttu-id="b5e1e-139">内部設置型ユニファイド メッセージングおよび Lync Server 2013 を統合するためのガイドライン</span><span class="sxs-lookup"><span data-stu-id="b5e1e-139">Guidelines for integrating on-premises Unified Messaging and Lync Server 2013</span></span>](lync-server-2013-guidelines-for-integrating-on-premises-unified-messaging.md)

<span data-ttu-id="b5e1e-140">ワイルドカードの使用など、Exchange 用の証明書の構成の詳細については、「Exchange 2013 の製品ドキュメント」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5e1e-140">For details about configuring certificates for Exchange, including the use of wildcards, see the Exchange 2013 product documentation.</span></span>

<span data-ttu-id="b5e1e-141"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b5e1e-141"></div>

<span> </span>

</div>

</div>

</span></span></div>

