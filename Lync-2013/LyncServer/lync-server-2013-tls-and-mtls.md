---
title: 'Lync Server 2013: TLS と MTLS'
description: 'Lync Server 2013: TLS と MTLS。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: TLS and MTLS for Lync Server 2013
ms:assetid: b32a5b85-fc82-42dc-a9b2-96400f8cd2b8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn481133(v=OCS.15)
ms:contentKeyID: 59893873
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a0ccee47e635435dd5f0d5eae03711c0cd5e517b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439704"
---
# <a name="tls-and-mtls-for-lync-server-2013"></a><span data-ttu-id="701dc-103">Lync Server 2013 の TLS と MTLS</span><span class="sxs-lookup"><span data-stu-id="701dc-103">TLS and MTLS for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="701dc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="701dc-104">

<span> </span></span></span>

<span data-ttu-id="701dc-105">_**最終更新日:** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="701dc-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="701dc-106">TLS プロトコルと MTLS プロトコルにより、インターネット上での通信の暗号化とエンドポイント認証機能が提供されます。</span><span class="sxs-lookup"><span data-stu-id="701dc-106">Transport Layer Security (TLS) and Mutual Transport Layer Security (MTLS) protocols provide encrypted communications and endpoint authentication on the Internet.</span></span> <span data-ttu-id="701dc-107">Microsoft Lync Server 2013 は、これら2つのプロトコルを使って、信頼されたサーバーのネットワークを作成し、そのネットワーク上のすべての通信を暗号化します。</span><span class="sxs-lookup"><span data-stu-id="701dc-107">Microsoft Lync Server 2013 uses these two protocols to create the network of trusted servers and to ensure that all communications over that network are encrypted.</span></span> <span data-ttu-id="701dc-108">サーバー間のすべての SIP 通信は MTLS により行われます。</span><span class="sxs-lookup"><span data-stu-id="701dc-108">All SIP communications between servers occur over MTLS.</span></span> <span data-ttu-id="701dc-109">クライアントからサーバーへの SIP 通信は TLS により行われます。</span><span class="sxs-lookup"><span data-stu-id="701dc-109">SIP communications from client to server occur over TLS.</span></span>

<span data-ttu-id="701dc-110">TLS は、ユーザーがクライアントソフトウェアを通じて、接続先の Lync Server 2013 サーバーを認証できるようにします。</span><span class="sxs-lookup"><span data-stu-id="701dc-110">TLS enables users, through their client software, to authenticate the Lync Server 2013 servers to which they connect.</span></span> <span data-ttu-id="701dc-111">TLS 接続では、クライアントはサーバーから有効な証明書を要求します。</span><span class="sxs-lookup"><span data-stu-id="701dc-111">On a TLS connection, the client requests a valid certificate from the server.</span></span> <span data-ttu-id="701dc-112">証明書が有効であると見なされるためには、証明書の発行元の CA がクライアントからも信頼されていること、およびサーバーの DNS 名が証明書の DNS 名に一致していることが必要です。</span><span class="sxs-lookup"><span data-stu-id="701dc-112">To be valid, the certificate must have been issued by a CA that is also trusted by the client and the DNS name of the server must match the DNS name on the certificate.</span></span> <span data-ttu-id="701dc-113">証明書が有効な場合、クライアントは証明書内の公開キーを使用して、通信に使う対称暗号化キーを暗号化し、証明書の最初の所有者だけが、その秘密キーを使用して通信の内容を暗号化することができます。</span><span class="sxs-lookup"><span data-stu-id="701dc-113">If the certificate is valid, the client uses the public key in the certificate to encrypt the symmetric encryption keys to be used for the communication, so only the original owner of the certificate can use its private key to decrypt the contents of the communication.</span></span> <span data-ttu-id="701dc-114">この接続は信頼済みと見なされ、それ以降は他の信頼されたサーバーやクライアントからチャレンジされません。</span><span class="sxs-lookup"><span data-stu-id="701dc-114">The resulting connection is trusted and from that point is not challenged by other trusted servers or clients.</span></span> <span data-ttu-id="701dc-115">このような意味合いで、Web サービスで使用される SSL (Secure Sockets Layer) は TLS ベースであるということができます。</span><span class="sxs-lookup"><span data-stu-id="701dc-115">Within this context, Secure Sockets Layer (SSL) as used with Web services can be associated as TLS-based.</span></span>

<span data-ttu-id="701dc-116">サーバー間接続は、相互認証に MTLS を利用します。</span><span class="sxs-lookup"><span data-stu-id="701dc-116">Server-to-server connections rely on MTLS for mutual authentication.</span></span> <span data-ttu-id="701dc-117">MTLS 接続では、サーバーが発信したメッセージをサーバーが受信すると、相互に信頼できる CA からの証明書を交換します。</span><span class="sxs-lookup"><span data-stu-id="701dc-117">On an MTLS connection, the server originating a message and the server receiving it exchange certificates from a mutually trusted CA.</span></span> <span data-ttu-id="701dc-118">証明書は、各サーバーの ID を他のサーバーに証明します。</span><span class="sxs-lookup"><span data-stu-id="701dc-118">The certificates prove the identity of each server to the other.</span></span> <span data-ttu-id="701dc-119">Lync Server 2013 の展開では、有効期間中にエンタープライズ CA によって発行された証明書は、そのドメイン内のエンタープライズ CA を信頼する Active Directory ドメインのすべてのメンバーによって自動的に有効と見なされます。</span><span class="sxs-lookup"><span data-stu-id="701dc-119">In Lync Server 2013 deployments, certificates issued by the enterprise CA that are during their validity period and not revoked by the issuing CA are automatically considered valid by all internal clients and servers because all members of an Active Directory domain trust the Enterprise CA in that domain.</span></span> <span data-ttu-id="701dc-120">フェデレーションシナリオでは、発行 CA は両方のフェデレーションパートナーによって信頼されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="701dc-120">In federated scenarios, the issuing CA must be trusted by both federated partners.</span></span> <span data-ttu-id="701dc-121">各パートナーは、必要に応じて異なる CA を使用できます。その CA は、他のパートナーによっても信頼されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="701dc-121">Each partner can use a different CA, if desired, so long as that CA is also trusted by the other partner.</span></span> <span data-ttu-id="701dc-122">この信頼は、エッジサーバーが信頼されたルート ca でパートナーのルート CA 証明書を持っているか、または両方の当事者が信頼しているサードパーティ CA を使用して、最も簡単に実現できます。</span><span class="sxs-lookup"><span data-stu-id="701dc-122">This trust is most easily accomplished by the Edge Servers having the partner’s root CA certificate in their trusted root CAs, or by use of a third-party CA that is trusted by both parties.</span></span>

<span data-ttu-id="701dc-123">TLS と MTLS は、盗聴および中間者 (man-in-the-middle) 攻撃の両方を防ぐのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="701dc-123">TLS and MTLS help prevent both eavesdropping and man-in-the middle attacks.</span></span> <span data-ttu-id="701dc-124">中間者 (man-in-the-middle) 攻撃では、攻撃者は 2 つのネットワーク エンティティ間の通信を、双方に気付かれることなく、攻撃者のコンピューターを経由して再ルーティングします。</span><span class="sxs-lookup"><span data-stu-id="701dc-124">In a man-in-the-middle attack, the attacker reroutes communications between two network entities through the attacker’s computer without the knowledge of either party.</span></span> <span data-ttu-id="701dc-125">TLS および Lync Server 2013 の信頼されたサーバー (Topology Builder で指定されたもののみ) の仕様は、2つのエンドポイント間の公開キー暗号化を使用して調整されたエンドツーエンドの暗号化を使用することによって、アプリケーションレイヤーの一部である中間攻撃のリスクを軽減します。また、攻撃者は、対応する秘密キーを持つ有効な信頼できる証明書を持ち、クライアントが通信して通信を解読するサービスの名前に発行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="701dc-125">TLS and Lync Server 2013 specification of trusted servers (only those specified in Topology Builder) mitigate the risk of a man-in-the middle attack partially on the application layer by using end-to-end encryption coordinated using the Public Key cryptography between the two endpoints, and an attacker would have to have a valid and trusted certificate with the corresponding private key and issued to the name of the service to which the client is communicating to decrypt the communication.</span></span> <span data-ttu-id="701dc-126">とはいえ、結局は、現在のネットワーク インフラストラクチャ (このケースでは社内 DNS) でのセキュリティのベスト プラクティスに従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="701dc-126">Ultimately, however, you must follow best security practices with your networking infrastructure (in this case corporate DNS).</span></span> <span data-ttu-id="701dc-127">Lync Server 2013 は、ドメインコントローラーとグローバルカタログが信頼されているのと同じ方法で DNS サーバーが信頼されていることを前提としていますが、DNS は、攻撃者のサーバーが不正な名前への要求に正常に応答できないようにすることによって、dns ハイジャック攻撃に対する保護レベルを提供します。</span><span class="sxs-lookup"><span data-stu-id="701dc-127">Lync Server 2013 assumes that the DNS server is trusted in the same way that domain controllers and global catalogs are trusted, but DNS does provide a level of safeguard against DNS hijack attacks by preventing an attacker’s server from responding successfully to a request to the spoofed name.</span></span>

<span data-ttu-id="701dc-128">次の図は、Lync Server 2013 で MTLS を使用して信頼されたサーバーのネットワークを作成する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="701dc-128">The following figure shows at a high level how Lync Server 2013 uses MTLS to create a network of trusted servers.</span></span>

<span data-ttu-id="701dc-129">**Lync Server ネットワークの信頼された接続**</span><span class="sxs-lookup"><span data-stu-id="701dc-129">**Trusted connections in a Lync Server network**</span></span>

<span data-ttu-id="701dc-130">![437749da-c372-4f・・・・・・・・・・・・・・・・ナイン](images/Dn481133.437749da-c372-4f0d-ac72-ccfd5191696b(OCS.15).jpg "437749da-c372-4f・・・・・・・・・・・・・・・・ナイン")</span><span class="sxs-lookup"><span data-stu-id="701dc-130">![437749da-c372-4f0d-ac72-ccfd5191696b](images/Dn481133.437749da-c372-4f0d-ac72-ccfd5191696b(OCS.15).jpg "437749da-c372-4f0d-ac72-ccfd5191696b")</span></span>

<span data-ttu-id="701dc-131"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="701dc-131"></div>

<span> </span>

</div>

</div>

</span></span></div>

