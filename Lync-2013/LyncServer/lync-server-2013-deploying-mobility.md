---
title: 'Lync Server 2013: モビリティの展開'
description: 'Lync Server 2013: モビリティの展開。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying mobility
ms:assetid: f41e6b25-d2cd-43fd-a17b-22cfda8bcd4f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690055(v=OCS.15)
ms:contentKeyID: 48185805
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cf927b950f8b94884fb91224a87e196fc815fca1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429875"
---
# <a name="deploying-mobility-in-lync-server-2013"></a><span data-ttu-id="45b94-103">Lync Server 2013 でのモビリティの展開</span><span class="sxs-lookup"><span data-stu-id="45b94-103">Deploying mobility in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="45b94-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="45b94-104">

<span> </span></span></span>

<span data-ttu-id="45b94-105">_**最終更新日:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="45b94-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="45b94-106">Lync Server 2013 モビリティ機能を展開するときに、モバイルユーザーは、インスタントメッセージング (IM)、プレゼンス、連絡先などの Lync 機能に対応するモバイルデバイスを使用できます。</span><span class="sxs-lookup"><span data-stu-id="45b94-106">When you deploy the Lync Server 2013 mobility feature, mobile users can use supported mobile devices for Lync functionality such as instant messaging (IM), presence, and contacts.</span></span>

<span data-ttu-id="45b94-107">モバイル機能を展開するための要件の詳細については、「 [Lync Server 2013 でのモビリティの計画](lync-server-2013-planning-for-mobility.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="45b94-107">For details about requirements for deploying the mobility feature, see [Planning for mobility in Lync Server 2013](lync-server-2013-planning-for-mobility.md).</span></span>

<span data-ttu-id="45b94-108">このセクションでは、モバイル機能と自動検出機能を展開して確認するための手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="45b94-108">This section guides you through the steps for deploying and verifying the mobility and automatic discovery features.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="45b94-109">このセクション中</span><span class="sxs-lookup"><span data-stu-id="45b94-109">In This Section</span></span>

  - [<span data-ttu-id="45b94-110">Lync Server 2013 での自動検出サービスの DNS レコードの作成</span><span class="sxs-lookup"><span data-stu-id="45b94-110">Creating DNS records for the Autodiscover Service in Lync Server 2013</span></span>](lync-server-2013-creating-dns-records-for-the-autodiscover-service.md)

  - [<span data-ttu-id="45b94-111">Lync Server 2013 でのモビリティに合わせた証明書の変更</span><span class="sxs-lookup"><span data-stu-id="45b94-111">Modifying certificates for mobility in Lync Server 2013</span></span>](lync-server-2013-modifying-certificates-for-mobility.md)

  - [<span data-ttu-id="45b94-112">Lync Server 2013 での、モビリティに合わせたリバース プロキシの構成</span><span class="sxs-lookup"><span data-stu-id="45b94-112">Configuring the reverse proxy for mobility in Lync Server 2013</span></span>](lync-server-2013-configuring-the-reverse-proxy-for-mobility.md)

  - [<span data-ttu-id="45b94-113">Lync Server 2013 のハイブリッド展開での自動検出の構成によるモビリティ</span><span class="sxs-lookup"><span data-stu-id="45b94-113">Configuring Autodiscover in Lync Server 2013 for mobility with hybrid deployments</span></span>](lync-server-2013-configuring-autodiscover-for-mobility-with-hybrid-deployments.md)

  - [<span data-ttu-id="45b94-114">Lync Server 2013 でのモビリティ展開の確認</span><span class="sxs-lookup"><span data-stu-id="45b94-114">Verifying your mobility deployment in Lync Server 2013</span></span>](lync-server-2013-verifying-your-mobility-deployment.md)

  - [<span data-ttu-id="45b94-115">Lync Server 2013 でプッシュ通知を構成する</span><span class="sxs-lookup"><span data-stu-id="45b94-115">Configuring for push notifications in Lync Server 2013</span></span>](lync-server-2013-configuring-for-push-notifications.md)

  - [<span data-ttu-id="45b94-116">Lync Server 2013 でのモビリティ ポリシーの構成</span><span class="sxs-lookup"><span data-stu-id="45b94-116">Configuring mobility policy in Lync Server 2013</span></span>](lync-server-2013-configuring-mobility-policy.md)

<span data-ttu-id="45b94-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="45b94-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

