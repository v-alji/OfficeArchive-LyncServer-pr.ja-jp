---
title: 'Lync Server 2013: エッジ コンポーネントのサポートされるサーバーの併置'
description: 'Lync Server 2013: edge コンポーネント用にサポートされているサーバーの collocation。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Supported server collocation for edge components
ms:assetid: 435c4dd8-36af-4b71-9b88-3ffcf0fc5c65
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425934(v=OCS.15)
ms:contentKeyID: 48183978
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7bf253e5210e077ca62b3d00f7f130d54d8392a5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423639"
---
# <a name="supported-server-collocation-for-edge-components-in-lync-server-2013"></a><span data-ttu-id="c40c0-103">Lync Server 2013 での、エッジ コンポーネントのサポートされるサーバーの併置</span><span class="sxs-lookup"><span data-stu-id="c40c0-103">Supported server collocation for edge components in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c40c0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c40c0-104">

<span> </span></span></span>

<span data-ttu-id="c40c0-105">_**最終更新日:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="c40c0-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="c40c0-106">アクセスエッジサービス、Web 会議エッジサービス、A/V Edge サービス、および XMPP プロキシサービスは、エッジサーバーに併置されています。</span><span class="sxs-lookup"><span data-stu-id="c40c0-106">The Access Edge service, Web Conferencing Edge service, A/V Edge service and XMPP Proxy service are collocated on the Edge Servers.</span></span> <span data-ttu-id="c40c0-107">次のサーバーは、外部ユーザーアクセスに必要な機能を提供し、専用サーバーとして展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c40c0-107">The following servers provide functions needed for external user access and must be deployed as dedicated servers:</span></span>

  - <span data-ttu-id="c40c0-108">エッジ サーバー</span><span class="sxs-lookup"><span data-stu-id="c40c0-108">Edge Server</span></span>

  - <span data-ttu-id="c40c0-109">監督 (オプション)</span><span class="sxs-lookup"><span data-stu-id="c40c0-109">Director (Optional)</span></span>

  - <span data-ttu-id="c40c0-110">リバース プロキシ</span><span class="sxs-lookup"><span data-stu-id="c40c0-110">Reverse proxy</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="c40c0-111">リバースプロキシは、Lync Server 2013 のみを提供するための専用である必要はありません。</span><span class="sxs-lookup"><span data-stu-id="c40c0-111">The reverse proxy does not need to be dedicated to serving only Lync Server 2013.</span></span> <span data-ttu-id="c40c0-112">たとえば、Lync Server Web サービスを公開するためのサービスを提供し、Lync Server にまったく関係のない別の Web サイトに公開された Web サイトを同時に提供することができます。</span><span class="sxs-lookup"><span data-stu-id="c40c0-112">For example, you can provide services to publish the Lync Server Web services, and concurrently provide a published Web site for another Web site that has no bearing on Lync Server at all.</span></span> <span data-ttu-id="c40c0-113">他のサービスをサポートするために既に境界ネットワーク内に逆プロキシサーバーがある場合は、Lync Server 2013 で使うことができます。</span><span class="sxs-lookup"><span data-stu-id="c40c0-113">If you already have a reverse proxy server in the perimeter network to support other services, you can use it for Lync Server 2013.</span></span>



<span data-ttu-id="c40c0-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c40c0-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

