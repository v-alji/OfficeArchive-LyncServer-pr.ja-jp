---
title: Lync Server 2013 の証明書インフラストラクチャの要件
description: Lync Server 2013 証明書インフラストラクチャの要件。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate infrastructure requirements
ms:assetid: 0051aa23-0bbe-4e72-9f29-e01c6bcc6190
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398066(v=OCS.15)
ms:contentKeyID: 48183219
ms.date: 06/23/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 02c7e69f272c29f0ba9386f403db326b4d39bbff
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435412"
---
# <a name="certificate-infrastructure-requirements-for-lync-server-2013"></a><span data-ttu-id="ab791-103">Lync Server 2013 の証明書インフラストラクチャの要件</span><span class="sxs-lookup"><span data-stu-id="ab791-103">Certificate infrastructure requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ab791-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ab791-104">

<span> </span></span></span>

<span data-ttu-id="ab791-105">_**最終更新日:** 2016-06-23_</span><span class="sxs-lookup"><span data-stu-id="ab791-105">_**Topic Last Modified:** 2016-06-23_</span></span>

<span data-ttu-id="ab791-106">Lync Server 2013 では、TLS と相互 TLS (MTLS) 接続をサポートするために公開キー基盤 (PKI) が必要です。</span><span class="sxs-lookup"><span data-stu-id="ab791-106">Lync Server 2013 requires a public key infrastructure (PKI) to support TLS and mutual TLS (MTLS) connections.</span></span>

<span data-ttu-id="ab791-107">Lync Server では、次の目的で証明書が使用されます。</span><span class="sxs-lookup"><span data-stu-id="ab791-107">Lync Server uses certificates for the following purposes:</span></span>

  - <span data-ttu-id="ab791-108">クライアントとサーバーの間の TLS 接続</span><span class="sxs-lookup"><span data-stu-id="ab791-108">TLS connections between client and server</span></span>

  - <span data-ttu-id="ab791-109">サーバー間の MTLS 接続</span><span class="sxs-lookup"><span data-stu-id="ab791-109">MTLS connections between servers</span></span>

  - <span data-ttu-id="ab791-110">パートナーの自動 DNS 検出を使ったフェデレーション</span><span class="sxs-lookup"><span data-stu-id="ab791-110">Federation using automatic DNS discovery of partners</span></span>

  - <span data-ttu-id="ab791-111">インスタント メッセージング (IM) 用のリモート ユーザー アクセス</span><span class="sxs-lookup"><span data-stu-id="ab791-111">Remote user access for instant messaging (IM)</span></span>

  - <span data-ttu-id="ab791-112">オーディオ/ビデオ (A/V) セッション、アプリケーション共有、および会議への外部ユーザーアクセス</span><span class="sxs-lookup"><span data-stu-id="ab791-112">External user access to audio/video (A/V) sessions, application sharing, and conferencing</span></span>

  - <span data-ttu-id="ab791-113">Web サービスの自動検出を使用したモバイル要求</span><span class="sxs-lookup"><span data-stu-id="ab791-113">Mobile requests using automatic discovery of Web Services</span></span>

<span data-ttu-id="ab791-114">Lync Server の場合は、次の一般的な要件が適用されます。</span><span class="sxs-lookup"><span data-stu-id="ab791-114">For Lync Server, the following common requirements apply:</span></span>

  - <span data-ttu-id="ab791-115">すべてのサーバー証明書がサーバーの承認 (サーバー EKU) をサポートしている必要がある。</span><span class="sxs-lookup"><span data-stu-id="ab791-115">All server certificates must support server authorization (Server EKU).</span></span>

  - <span data-ttu-id="ab791-116">すべてのサーバー証明書に CRL 配布ポイント (CDP) を含める必要がある。</span><span class="sxs-lookup"><span data-stu-id="ab791-116">All server certificates must contain a CRL Distribution Point (CDP).</span></span>

  - <span data-ttu-id="ab791-117">すべての証明書が、オペレーティング システムでサポートされている署名アルゴリズムによって署名されている必要がある。</span><span class="sxs-lookup"><span data-stu-id="ab791-117">All certificates must be signed using a signing algorithm supported by the operating system.</span></span> <span data-ttu-id="ab791-118">Lync Server 2013 は、ダイジェストのサイズ (224、256、384、512ビット) の SHA-1 および SHA-1 スイートをサポートしており、オペレーティングシステムの要件を満たしているか、超えています。</span><span class="sxs-lookup"><span data-stu-id="ab791-118">Lync Server 2013 supports the SHA-1 and SHA-2 suite of digest sizes (224, 256, 384 and 512-bit), and meets or exceeds the operating system requirements.</span></span> <span data-ttu-id="ab791-119">オペレーティングシステムのサポートについては、を参照してください [https://go.microsoft.com/fwlink/?LinkId=287002](https://go.microsoft.com/fwlink/?linkid=287002) 。</span><span class="sxs-lookup"><span data-stu-id="ab791-119">For operating system support, see [https://go.microsoft.com/fwlink/?LinkId=287002](https://go.microsoft.com/fwlink/?linkid=287002).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ab791-120">RSASSA-PSS 署名アルゴリズムの使用はサポートされておらず、数ある問題の中でも、ログイン時のエラーや着信転送時の問題につながる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ab791-120">Using the RSASSA-PSS signature algorithm is unsupported, and may lead to errors on login and call forwarding issues, among other problems.</span></span>

    
    </div>

  - <span data-ttu-id="ab791-121">自動登録は、Lync Server を実行している内部サーバーでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="ab791-121">Auto-enrollment is supported for internal servers running Lync Server.</span></span>

  - <span data-ttu-id="ab791-122">自動登録は、Lync Server Edge サーバーではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="ab791-122">Auto-enrollment is not supported for Lync Server Edge Servers.</span></span>

  - <span data-ttu-id="ab791-123">Web ベースの証明書要求を Windows Server 2003 CA に送信する場合は、Windows Server 2003 と SP2 または Windows XP を実行しているコンピューターから送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ab791-123">When you submit a web-based certificate request to a Windows Server 2003 CA, you must submit it from a computer running either Windows Server 2003 with SP2 or Windows XP.</span></span>
    
    <span data-ttu-id="ab791-124">KB922706 では、Windows Server 2003 証明書サービスの web 登録に対して web 証明書を登録する際の問題を解決するためのサポートを提供していますが、windows server 2008、Windows Vista、または Windows 7 を使用して Windows Server 2003 CA から証明書を要求することはできません。</span><span class="sxs-lookup"><span data-stu-id="ab791-124">Note that although KB922706 provides support for resolving issues with enrolling web certificates against a Windows Server 2003 Certificate Services web enrollment, it does not make it possible to use Windows Server 2008, Windows Vista, or Windows 7 to request a certificate from a Windows Server 2003 CA.</span></span>

  - <span data-ttu-id="ab791-125">暗証キーの長さとして 1024、2048、4096 がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="ab791-125">Encryption key lengths of 1024, 2048, and 4096 are supported.</span></span> <span data-ttu-id="ab791-126">2048 以上のキーの長さはお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="ab791-126">Key lengths of 2048 and greater are recommended.</span></span>

  - <span data-ttu-id="ab791-127">既定のダイジェストまたはハッシュ アルゴリズムは RSA です。</span><span class="sxs-lookup"><span data-stu-id="ab791-127">The default digest, or hash signing, algorithm is RSA.</span></span> <span data-ttu-id="ab791-128">ECDH \_ P256、ecdh \_ P384、および ecdh \_ P521 アルゴリズムもサポートされています。</span><span class="sxs-lookup"><span data-stu-id="ab791-128">The ECDH\_P256, ECDH\_P384, and ECDH\_P521 algorithms are also supported.</span></span> 

<div>

## <a name="in-this-section"></a><span data-ttu-id="ab791-129">このセクション中</span><span class="sxs-lookup"><span data-stu-id="ab791-129">In This Section</span></span>

  - [<span data-ttu-id="ab791-130">Lync Server 2013 の内部サーバーに対する証明書要件</span><span class="sxs-lookup"><span data-stu-id="ab791-130">Certificate requirements for internal servers in Lync Server 2013</span></span>](lync-server-2013-certificate-requirements-for-internal-servers.md)

  - [<span data-ttu-id="ab791-131">Lync Server 2013 における外部ユーザー アクセスに対する証明書要件</span><span class="sxs-lookup"><span data-stu-id="ab791-131">Certificate requirements for external user access in Lync Server 2013</span></span>](lync-server-2013-certificate-requirements-for-external-user-access.md)

  - [<span data-ttu-id="ab791-132">Lync Server 2013 の常設チャット サーバーに対する証明書要件</span><span class="sxs-lookup"><span data-stu-id="ab791-132">Certificate requirements for Persistent Chat server in Lync Server 2013</span></span>](lync-server-2013-certificate-requirements-for-persistent-chat-server.md)

  - [<span data-ttu-id="ab791-133">Lync Server 2013 のモビリティの証明書の要件</span><span class="sxs-lookup"><span data-stu-id="ab791-133">Certificate requirements for mobility in Lync Server 2013</span></span>](lync-server-2013-certificate-requirements-for-mobility.md)

<span data-ttu-id="ab791-134"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ab791-134"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

