---
title: 'Lync Server 2013: ディレクターを使った自動クライアント サインインの構成'
description: 'Lync Server 2013: ディレクターを使用するように自動クライアント Sign-In を構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure Automatic Client Sign-In to use the Director
ms:assetid: 85369ffc-53ae-43be-8a23-84a094faecff
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398678(v=OCS.15)
ms:contentKeyID: 48184703
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b9c45a1a677d3a30704d8dca1771ef865cef29ec
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399620"
---
# <a name="configure-automatic-client-sign-in-to-use-the-director-in-lync-server-2013"></a><span data-ttu-id="ba03a-103">Lync Server 2013 でのディレクターを使った自動クライアント サインインの構成</span><span class="sxs-lookup"><span data-stu-id="ba03a-103">Configure Automatic Client Sign-In to use the Director in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ba03a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ba03a-104">

<span> </span></span></span>

<span data-ttu-id="ba03a-105">_**最終更新日:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="ba03a-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="ba03a-106">Lync Server 2013、ディレクター、またはディレクタープールを展開する場合は、ベストプラクティスとして、自動クライアント Sign-In を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ba03a-106">When you deploy a Lync Server 2013, Director or a pool of Directors, we recommend that you use Automatic Client Sign-In as a best practice.</span></span> <span data-ttu-id="ba03a-107">自動クライアントサインイン用に DNS サーバーを構成する方法について詳しくは、「計画ドキュメントの「 [Lync Server 2013 での自動クライアントサインインの dns 要件](lync-server-2013-dns-requirements-for-automatic-client-sign-in.md) 」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="ba03a-107">For details about how to configure DNS servers for automatic client sign-in, see [DNS requirements for automatic client sign-in in Lync Server 2013](lync-server-2013-dns-requirements-for-automatic-client-sign-in.md) in the Planning documentation.</span></span>

<span data-ttu-id="ba03a-108">既に自動クライアントサインインを展開している場合は、次のセクションを参照してディレクターで構成してください。</span><span class="sxs-lookup"><span data-stu-id="ba03a-108">If you have already deployed Automatic Client Sign-In, see the following sections to configure it on your Director(s).</span></span>

<div>

## <a name="single-director-instance"></a><span data-ttu-id="ba03a-109">単一のディレクターインスタンス</span><span class="sxs-lookup"><span data-stu-id="ba03a-109">Single Director Instance</span></span>

<span data-ttu-id="ba03a-110">既に自動クライアント Sign-In 展開されていて、フロントエンドサーバーまたはフロントエンドプールをポイントしている場合は、そのディレクターをポイントするように DNS SRV レコードを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ba03a-110">If you already have Automatic Client Sign-In deployed and it is pointing to a Front End Server or a Front End pool, you need to change the DNS SRV record to point to the Director.</span></span>

</div>

<div>

## <a name="director-pool"></a><span data-ttu-id="ba03a-111">ディレクタープール</span><span class="sxs-lookup"><span data-stu-id="ba03a-111">Director Pool</span></span>

<span data-ttu-id="ba03a-112">既に自動クライアント Sign-In 展開されていて、フロントエンドサーバーまたはフロントエンドプールを指している場合は、そのディレクタープールをポイントするように DNS SRV レコードを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ba03a-112">If you already have Automatic Client Sign-In deployed and it is pointing to a Front End Server or a Front End pool, you need to change the DNS SRV record to point to the Director pool.</span></span>

<span data-ttu-id="ba03a-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ba03a-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

