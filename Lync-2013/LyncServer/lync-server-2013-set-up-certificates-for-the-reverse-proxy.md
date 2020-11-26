---
title: 'Lync Server 2013: リバース プロキシの証明書の設定'
description: 'Lync Server 2013: リバースプロキシ用の証明書をセットアップします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Set up certificates for the reverse proxy
ms:assetid: c03a08ec-a67b-4f11-b0d7-6677461beaaa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412938(v=OCS.15)
ms:contentKeyID: 48185291
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f4b84241775bb3594840b68551048c01ff5faba2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441747"
---
# <a name="set-up-certificates-for-the-reverse-proxy-in-lync-server-2013"></a><span data-ttu-id="20bd8-103">Lync Server 2013 でのリバース プロキシの証明書の設定</span><span class="sxs-lookup"><span data-stu-id="20bd8-103">Set up certificates for the reverse proxy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="20bd8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="20bd8-104">

<span> </span></span></span>

<span data-ttu-id="20bd8-105">_**最終更新日:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="20bd8-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="20bd8-106">各リバースプロキシサーバーでは、リスニングサービスで使用するために web サーバー証明書が必要です。</span><span class="sxs-lookup"><span data-stu-id="20bd8-106">Each reverse proxy server requires a web server certificate for use by the listening service.</span></span> <span data-ttu-id="20bd8-107">Web サーバー証明書は、公開証明機関 (CA) によって発行されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="20bd8-107">The web server certificate must be issued by a public certification authority (CA).</span></span>

<span data-ttu-id="20bd8-108">このような証明書の要件の詳細については、「 [Lync Server 2013 の外部ユーザーアクセスの証明書の要件](lync-server-2013-certificate-requirements-for-external-user-access.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20bd8-108">For details about this and other certificate requirements, see [Certificate requirements for external user access in Lync Server 2013](lync-server-2013-certificate-requirements-for-external-user-access.md).</span></span>

<div>

## <a name="to-set-up-a-web-services-certificate-for-the-reverse-proxy"></a><span data-ttu-id="20bd8-109">リバースプロキシの Web サービス証明書を設定するには</span><span class="sxs-lookup"><span data-stu-id="20bd8-109">To set up a Web Services certificate for the reverse proxy</span></span>

  - <span data-ttu-id="20bd8-110">Web サービス証明書のセットアップなど、リバースプロキシを既にセットアップしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="20bd8-110">You should have already set up your reverse proxy, including setting up the Web Services certificate.</span></span> <span data-ttu-id="20bd8-111">エッジサーバーの展開を開始する前に、この操作を行っていない場合は、「 [Lync Server 2013 用のリバースプロキシサーバー](lync-server-2013-setting-up-reverse-proxy-servers.md) をセットアップして web サービスの証明書をインストールする」の手順を実行して、各 web 発行ルールを作成して、証明書を使用するように構成します。</span><span class="sxs-lookup"><span data-stu-id="20bd8-111">If you did not do so before starting your deployment of your Edge Servers, use the procedures in [Setting up reverse proxy servers for Lync Server 2013](lync-server-2013-setting-up-reverse-proxy-servers.md) to create request and install the Web Services certificate, and then create each web publishing rule and configure it to use the certificate.</span></span>

<span data-ttu-id="20bd8-112"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="20bd8-112"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

