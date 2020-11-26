---
title: 'Lync Server 2013: Hosted Exchange ユニファイド メッセージング統合'
description: 'Lync Server 2013: ホストされている Exchange ユニファイドメッセージングの統合。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hosted Exchange Unified Messaging integration
ms:assetid: f4de0165-da3b-499e-98fc-28ddd0db02d5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413027(v=OCS.15)
ms:contentKeyID: 48185829
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 980c0bc47258e9fae94ff623559342ca36eea145
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427531"
---
# <a name="hosted-exchange-unified-messaging-integration-in-lync-server-2013"></a><span data-ttu-id="032e0-103">Lync Server 2013 の Hosted Exchange ユニファイド メッセージング統合</span><span class="sxs-lookup"><span data-stu-id="032e0-103">Hosted Exchange Unified Messaging integration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="032e0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="032e0-104">

<span> </span></span></span>

<span data-ttu-id="032e0-105">_**最終更新日:** 2012-09-20_</span><span class="sxs-lookup"><span data-stu-id="032e0-105">_**Topic Last Modified:** 2012-09-20_</span></span>

<span data-ttu-id="032e0-106">以前の Lync Server 2013 リリースでは、Exchange ユニファイドメッセージング (UM) の *オンプレミス* 展開との統合に加えて、lync server 2013 では、 *ホスティング* された exchange UM との統合のサポートが提供されています。</span><span class="sxs-lookup"><span data-stu-id="032e0-106">In addition to the support that previous Lync Server 2013 releases have provided for integration with *on-premises* deployments of Exchange Unified Messaging (UM), Lync Server 2013 introduces support for integration with *hosted* Exchange UM.</span></span> <span data-ttu-id="032e0-107">ホストされた Exchange UM を使用すると、Microsoft Exchange Online などのホストされている Exchange サービスプロバイダーに一部またはすべてのユーザーを転送する場合に、Lync Server 2013 でユーザーに音声メッセージを提供できます。</span><span class="sxs-lookup"><span data-stu-id="032e0-107">Hosted Exchange UM enables Lync Server 2013 to provide voice messaging to your users if you transfer some or all of them to a hosted Exchange service provider such as Microsoft Exchange Online.</span></span>

<span data-ttu-id="032e0-108">Lync Server 2013 エンタープライズ Voip は、Exchange UM インフラストラクチャを使って、通話応答、通話通知、音声アクセス (ボイスメールを含む)、自動応答サービスを提供します。</span><span class="sxs-lookup"><span data-stu-id="032e0-108">Lync Server 2013 Enterprise Voice uses the Exchange UM infrastructure to provide call answering, call notification, voice access (including voice mail), and auto attendant services.</span></span> <span data-ttu-id="032e0-109">詳細については、「 [統合ユニファイドメッセージングと Lync Server 2013 の機能](lync-server-2013-features-of-integrated-unified-messaging.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="032e0-109">For details, see [Features of integrated Unified Messaging and Lync Server 2013](lync-server-2013-features-of-integrated-unified-messaging.md).</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="032e0-110">このセクション中</span><span class="sxs-lookup"><span data-stu-id="032e0-110">In This Section</span></span>

  - [<span data-ttu-id="032e0-111">Lync Server 2013 の Hosted Exchange UM アーキテクチャとルーティング</span><span class="sxs-lookup"><span data-stu-id="032e0-111">Hosted Exchange UM architecture and routing in Lync Server 2013</span></span>](lync-server-2013-hosted-exchange-um-architecture-and-routing.md)

  - [<span data-ttu-id="032e0-112">Lync Server 2013 のホスト型ボイス メール ポリシー</span><span class="sxs-lookup"><span data-stu-id="032e0-112">Hosted voice mail policies in Lync Server 2013</span></span>](lync-server-2013-hosted-voice-mail-policies.md)

  - [<span data-ttu-id="032e0-113">Lync Server 2013 の Hosted Exchange ユーザー管理</span><span class="sxs-lookup"><span data-stu-id="032e0-113">Hosted Exchange user management in Lync Server 2013</span></span>](lync-server-2013-hosted-exchange-user-management.md)

  - [<span data-ttu-id="032e0-114">Lync Server 2013 の Hosted Exchange 連絡先オブジェクト管理</span><span class="sxs-lookup"><span data-stu-id="032e0-114">Hosted Exchange Contact object management in Lync Server 2013</span></span>](lync-server-2013-hosted-exchange-contact-object-management.md)

  - [<span data-ttu-id="032e0-115">Hosted Exchange UM と Lync Server 2013 の統合のための展開プロセス</span><span class="sxs-lookup"><span data-stu-id="032e0-115">Deployment process for integrating hosted Exchange UM with Lync Server 2013</span></span>](lync-server-2013-deployment-process-for-integrating-hosted-exchange-um.md)

<span data-ttu-id="032e0-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="032e0-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

