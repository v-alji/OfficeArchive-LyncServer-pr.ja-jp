---
title: 'Lync Server 2013: ドメインネームシステム (DNS) の要件'
description: 'Lync Server 2013: ドメインネームシステム (DNS) の要件。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Domain Name System (DNS) requirements
ms:assetid: 586cf18e-0080-4eb1-aee5-56843277fdfc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398386(v=OCS.15)
ms:contentKeyID: 48184194
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f84868d4929cc410cddbb6c9ad2019a12841e80f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49397929"
---
# <a name="domain-name-system-dns-requirements-for-lync-server-2013"></a><span data-ttu-id="1992e-103">Lync Server 2013 のドメインネームシステム (DNS) 要件</span><span class="sxs-lookup"><span data-stu-id="1992e-103">Domain Name System (DNS) requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1992e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1992e-104">

<span> </span></span></span>

<span data-ttu-id="1992e-105">_**最終更新日:** 2012-06-18_</span><span class="sxs-lookup"><span data-stu-id="1992e-105">_**Topic Last Modified:** 2012-06-18_</span></span>

<span data-ttu-id="1992e-106">Lync Server を展開するには、クライアントとサーバーの検出を有効にするドメインネームシステム (DNS) レコードを作成し、必要に応じて、組織でサポートが必要な場合は、自動クライアントサインインをサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1992e-106">To deploy Lync Server, you must create Domain Name System (DNS) records that enable the discovery of clients and servers, and, optionally, support for automatic client sign-in if your organization wants to support it.</span></span>

<span data-ttu-id="1992e-107">Lync Server では、次のような方法で DNS を使用します。</span><span class="sxs-lookup"><span data-stu-id="1992e-107">Lync Server uses DNS in the following ways:</span></span>

  - <span data-ttu-id="1992e-108">内部サーバーまたはサーバー間通信のプールを検出します。</span><span class="sxs-lookup"><span data-stu-id="1992e-108">To discover internal servers or pools for server-to-server communications.</span></span>

  - <span data-ttu-id="1992e-109">クライアントが、さまざまな SIP トランザクションに使用されるフロントエンドプールまたは Standard Edition サーバーを検出できるようにするには、</span><span class="sxs-lookup"><span data-stu-id="1992e-109">To allow clients to discover the Front End pool or Standard Edition server used for various SIP transactions.</span></span>

  - <span data-ttu-id="1992e-110">ログオンしていないユニファイドコミュニケーション (UC) デバイスで、デバイス更新 Web サービスが実行されているフロントエンドプールまたは Standard Edition サーバーを検出し、更新プログラムを入手してログを送信できるようにするには、</span><span class="sxs-lookup"><span data-stu-id="1992e-110">To allow unified communications (UC) devices that are not logged on to discover the Front End pool or Standard Edition server running Device Update Web Service, obtain updates, and send logs.</span></span>

  - <span data-ttu-id="1992e-111">外部サーバーとクライアントが、エッジサーバーまたはインスタントメッセージング (IM) または会議の HTTP リバースプロキシに接続できるようにするには、こちらを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1992e-111">To allow external servers and clients to connect to Edge Servers or the HTTP reverse proxy for instant messaging (IM) or conferencing.</span></span>

  - <span data-ttu-id="1992e-112">外部 UC デバイスがエッジサーバーまたは HTTP リバースプロキシ経由でデバイス更新 Web サービスに接続できるようにするには、[更新プログラムの取得] を選びます。</span><span class="sxs-lookup"><span data-stu-id="1992e-112">To allow external UC devices to connect to Device Update Web service through Edge Servers or the HTTP reverse proxy and obtain updates.</span></span>

  - <span data-ttu-id="1992e-113">モバイルクライアントが、デバイス設定で Url を手動で入力する必要なく、Web サービスのリソースを自動的に検出できるようにする。</span><span class="sxs-lookup"><span data-stu-id="1992e-113">To allow mobile clients to automatically discover Web Services resources without requiring users to manually enter URLs in device settings.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="1992e-114">このセクション中</span><span class="sxs-lookup"><span data-stu-id="1992e-114">In This Section</span></span>

  - [<span data-ttu-id="1992e-115">Lync Server 2013 の DNS の要件を確認する</span><span class="sxs-lookup"><span data-stu-id="1992e-115">Determine DNS requirements for Lync Server 2013</span></span>](lync-server-2013-determine-dns-requirements.md)

  - [<span data-ttu-id="1992e-116">Lync Server 2013 のフロントエンドプールの DNS 要件</span><span class="sxs-lookup"><span data-stu-id="1992e-116">DNS requirements for Front End pools in Lync Server 2013</span></span>](lync-server-2013-dns-requirements-for-front-end-pools.md)

  - [<span data-ttu-id="1992e-117">Lync Server 2013 での Standard Edition サーバーの DNS 要件</span><span class="sxs-lookup"><span data-stu-id="1992e-117">DNS requirements for Standard Edition servers in Lync Server 2013</span></span>](lync-server-2013-dns-requirements-for-standard-edition-servers.md)

  - [<span data-ttu-id="1992e-118">Lync Server 2013 の簡易 URL の DNS 要件</span><span class="sxs-lookup"><span data-stu-id="1992e-118">DNS requirements for simple URLs in Lync Server 2013</span></span>](lync-server-2013-dns-requirements-for-simple-urls.md)

  - [<span data-ttu-id="1992e-119">Lync Server 2013 での自動クライアントサインインの DNS 要件</span><span class="sxs-lookup"><span data-stu-id="1992e-119">DNS requirements for automatic client sign-in in Lync Server 2013</span></span>](lync-server-2013-dns-requirements-for-automatic-client-sign-in.md)

  - [<span data-ttu-id="1992e-120">Lync Server 2013 を使ったモビリティの DNS 要件</span><span class="sxs-lookup"><span data-stu-id="1992e-120">DNS requirements for mobility with Lync Server 2013</span></span>](lync-server-2013-dns-requirements-for-mobility.md)

  - [<span data-ttu-id="1992e-121">Lync Server 2013 での DNS の負荷分散</span><span class="sxs-lookup"><span data-stu-id="1992e-121">DNS load balancing in Lync Server 2013</span></span>](lync-server-2013-dns-load-balancing.md)

<span data-ttu-id="1992e-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1992e-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

