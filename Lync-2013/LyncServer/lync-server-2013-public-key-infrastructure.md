---
title: 'Lync Server 2013: 公開キー基盤'
description: 'Lync Server 2013: 公開キー基盤。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Public Key Infrastructure for Lync Server 2013
ms:assetid: 737c8a25-23e9-4494-ab76-5a7b729b44ca
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn481131(v=OCS.15)
ms:contentKeyID: 59893870
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0b8f2ee8c6b1524cec461ad90a4d4cb1a1003b51
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399081"
---
# <a name="public-key-infrastructure-for-lync-server-2013"></a><span data-ttu-id="ba467-103">Lync Server 2013 用の公開キー基盤</span><span class="sxs-lookup"><span data-stu-id="ba467-103">Public Key Infrastructure for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ba467-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ba467-104">

<span> </span></span></span>

<span data-ttu-id="ba467-105">_**最終更新日:** 2013-11-13_</span><span class="sxs-lookup"><span data-stu-id="ba467-105">_**Topic Last Modified:** 2013-11-13_</span></span>

<span data-ttu-id="ba467-106">Microsoft Lync Server 2013 は、サーバー認証には証明書を使用し、クライアントとサーバー間、およびサーバーのさまざまな役割間で信頼のチェーンを確立します。</span><span class="sxs-lookup"><span data-stu-id="ba467-106">Microsoft Lync Server 2013 relies on certificates for server authentication and to establish a chain of trust between clients and servers and among the different server roles.</span></span> <span data-ttu-id="ba467-107">Windows Server 2012 R2、Windows Server 2012、windows Server 2008 R2、windows server 2008、および Windows Server 2003 公開キー基盤 (PKI) は、この信頼チェーンを確立して検証するためのインフラストラクチャを提供します。</span><span class="sxs-lookup"><span data-stu-id="ba467-107">The Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, Windows Server 2008, and Windows Server 2003 Public Key Infrastructure (PKI) provides the infrastructure for establishing and validating this chain of trust.</span></span>

<span data-ttu-id="ba467-p102">証明書とはデジタル ID です。証明書は、名前によってサーバーを識別し、そのプロパティを指定します。証明書の情報が有効であるためには、サーバーに接続するクライアントやその他のサーバーが信頼する CA から証明書が発行されている必要があります。サーバーがプライベート ネットワーク上の他のクライアントおよびサーバーとのみ接続する場合は、CA はエンタープライズ CA で問題ありません。サーバーがプライベート ネットワーク外のエンティティと対話する場合は、パブリック CA が必要な可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ba467-p102">Certificates are digital IDs. They identify a server by name and specify its properties. To ensure that the information on a certificate is valid, the certificate must be issued by a CA that is trusted by clients or other servers that connect to the server. If the server connects only with other clients and servers on a private network, the CA can be an enterprise CA. If the server interacts with entities outside the private network, a public CA might be required.</span></span>

<span data-ttu-id="ba467-p103">証明書の情報が有効であっても、証明書を提示しているサーバーが、実際に証明書によって提示されているサーバーであることを確認する手段が必要です。ここで Windows PKI が役立ちます。</span><span class="sxs-lookup"><span data-stu-id="ba467-p103">Even if the information on the certificate is valid, there must be some way to verify that the server presenting the certificate is actually the one represented by the certificate. This is where the Windows PKI comes in.</span></span>

<span data-ttu-id="ba467-p104">各証明書は、公開キーにリンクされています。証明書で名前が指定されているサーバーには、そのサーバーのみが知る、対応する秘密キーがあります。接続しようとしているクライアントまたはサーバーは、公開キーを使用して無作為な情報の断片を暗号化し、それをサーバーに送信します。サーバーがその情報を復号化し、プレーン テキストに戻すと、接続しようとしているエンティティは、証明書の秘密キーをサーバーが保持していること、つまり、そのサーバーが証明書で指定されていることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="ba467-p104">Each certificate is linked to a public key. The server named on the certificate holds a corresponding private key that only it knows. A connecting client or server uses the public key to encrypt a random piece of information and sends it to the server. If the server decrypts the information and returns it as plain text, the connecting entity can be sure that the server holds the private key to the certificate and therefore is the server named on the certificate.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="ba467-119">すべてのパブリック Ca が Lync Server 2013 証明書の要件を満たしているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="ba467-119">Not all public CAs comply with the requirements of Lync Server 2013 certificates.</span></span> <span data-ttu-id="ba467-120">認定されているパブリック CA ベンダーの一覧を参照して、パブリック証明書のニーズに合ったベンダーを探すことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ba467-120">We recommend that you refer to the listing of certified Public CA vendors for your public certificate needs.</span></span> <span data-ttu-id="ba467-121">詳細については、「ユニファイドコミュニケーションの証明書パートナー」を参照してください <A href="https://go.microsoft.com/fwlink/p/?linkid=140898">https://go.microsoft.com/fwlink/p/?LinkId=140898</A> 。</span><span class="sxs-lookup"><span data-stu-id="ba467-121">For details, see Unified Communications Certificate Partners at <A href="https://go.microsoft.com/fwlink/p/?linkid=140898">https://go.microsoft.com/fwlink/p/?LinkId=140898</A>.</span></span>



</div>

<div>

## <a name="crl-distribution-points"></a><span data-ttu-id="ba467-122">CRL 配布ポイント</span><span class="sxs-lookup"><span data-stu-id="ba467-122">CRL Distribution Points</span></span>

<span data-ttu-id="ba467-123">Lync Server 2013 では、すべてのサーバー証明書に1つ以上の証明書失効リスト (CRL) 配布ポイントが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="ba467-123">Lync Server 2013 requires all server certificates to contain one or more Certificate Revocation List (CRL) distribution points.</span></span> <span data-ttu-id="ba467-124">CRL 配布ポイント (CDP) とは、証明書の発行後にそれが失効していないこと、および証明書が有効期限内にあることを確認するために、CRL をダウンロードできる場所です。</span><span class="sxs-lookup"><span data-stu-id="ba467-124">CRL distribution points (CDPs) are locations from which CRLs can be downloaded for purposes of verifying that the certificate has not been revoked since the time it was issued and the certificate is still within the validity period.</span></span> <span data-ttu-id="ba467-125">CRL 配布ポイントは、URL として証明書のプロパティに記述され、通常、セキュア HTTP です。</span><span class="sxs-lookup"><span data-stu-id="ba467-125">A CRL distribution point is noted in the properties of the certificate as a URL, and is typically secure HTTP.</span></span>

</div>

<div>

## <a name="enhanced-key-usage"></a><span data-ttu-id="ba467-126">拡張キー使用法</span><span class="sxs-lookup"><span data-stu-id="ba467-126">Enhanced Key Usage</span></span>

<span data-ttu-id="ba467-127">Lync Server 2013 では、サーバー認証のために、すべてのサーバー証明書で拡張キー使用法 (EKU) がサポートされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="ba467-127">Lync Server 2013 requires all server certificates to support Enhanced Key Usage (EKU) for the purpose of server authentication.</span></span> <span data-ttu-id="ba467-128">サーバー認証用に EKU フィールドを構成することは、サーバーの認証に対して、その証明書が有効であることを意味します。</span><span class="sxs-lookup"><span data-stu-id="ba467-128">Configuring the EKU field for server authentication means that the certificate is valid for the purpose of authenticating servers.</span></span> <span data-ttu-id="ba467-129">この EKU は、MTLS には不可欠です。</span><span class="sxs-lookup"><span data-stu-id="ba467-129">This EKU is essential for MTLS.</span></span> <span data-ttu-id="ba467-130">EKU には、複数のエントリを指定し、複数の目的に対して証明書を有効にできます。</span><span class="sxs-lookup"><span data-stu-id="ba467-130">It is possible to have more than one entry in the EKU, enabling the certificate for more than one purpose.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="ba467-131">Live Communications Server 2003 および Live Communications Server 2005 からの送信 MTLS 接続には、クライアント認証 EKU が必要ですが、これは不要になりました。</span><span class="sxs-lookup"><span data-stu-id="ba467-131">The Client Authentication EKU is required for outbound MTLS connections from Live Communications Server 2003 and Live Communications Server 2005, but it is no longer required.</span></span> <span data-ttu-id="ba467-132">ただし、パブリック IM 接続を使って AOL に接続するエッジサーバーには、この EKU が存在している必要があります。</span><span class="sxs-lookup"><span data-stu-id="ba467-132">However, this EKU must be present on Edge Servers that connect to AOL by means of public IM connectivity.</span></span>



<span data-ttu-id="ba467-133"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ba467-133"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

