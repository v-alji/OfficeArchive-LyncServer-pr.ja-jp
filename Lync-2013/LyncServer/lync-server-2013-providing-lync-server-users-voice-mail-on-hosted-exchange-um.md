---
title: 'Lync Server 2013: Lync Server ユーザーに Hosted Exchange UM のボイス メールを提供する'
description: 'Lync Server 2013: Lync Server ユーザーがホスティングされている Exchange UM でボイスメールを提供している。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Providing Lync Server 2013 users voice mail on hosted Exchange UM
ms:assetid: 306d3fb5-231b-4f0b-b8d8-0d9083b5ed77
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425807(v=OCS.15)
ms:contentKeyID: 48183752
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: be4048e7fc2bd30a4ab670259a1871bd1b59483a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436833"
---
# <a name="providing-lync-server-2013-users-voice-mail-on-hosted-exchange-um"></a><span data-ttu-id="cda6b-103">Lync Server 2013 ユーザーに Hosted Exchange UM のボイス メールを提供する</span><span class="sxs-lookup"><span data-stu-id="cda6b-103">Providing Lync Server 2013 users voice mail on hosted Exchange UM</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cda6b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cda6b-104">

<span> </span></span></span>

<span data-ttu-id="cda6b-105">_**最終更新日:** 2012-09-24_</span><span class="sxs-lookup"><span data-stu-id="cda6b-105">_**Topic Last Modified:** 2012-09-24_</span></span>

<span data-ttu-id="cda6b-106">このセクションでは、ホストされた Exchange ユニファイドメッセージング (UM) サービスでボイスメールを使用して、オンプレミスの Lync Server 2013 展開にユーザーを提供するプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="cda6b-106">This section guides you through the process of providing users in an on-premises Lync Server 2013 deployment with voice mail on a hosted Exchange Unified Messaging (UM) service.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="cda6b-107">このセクション中</span><span class="sxs-lookup"><span data-stu-id="cda6b-107">In This Section</span></span>

  - [<span data-ttu-id="cda6b-108">Hosted Exchange UM との統合のための DNS SRV レコードを作成する</span><span class="sxs-lookup"><span data-stu-id="cda6b-108">Create a DNS SRV record for integration with hosted Exchange UM</span></span>](lync-server-2013-create-a-dns-srv-record-for-integration-with-hosted-exchange-um.md)

  - [<span data-ttu-id="cda6b-109">Hosted Exchange UM との統合のためのエッジ サーバーの構成</span><span class="sxs-lookup"><span data-stu-id="cda6b-109">Configure the Edge Server for integration with hosted Exchange UM</span></span>](lync-server-2013-configure-the-edge-server-for-integration-with-hosted-exchange-um.md)

  - [<span data-ttu-id="cda6b-110">Lync Server 2013 でのホスト ボイス メール ポリシーの管理</span><span class="sxs-lookup"><span data-stu-id="cda6b-110">Manage hosted voice mail policies in Lync Server 2013</span></span>](lync-server-2013-manage-hosted-voice-mail-policies.md)

  - [<span data-ttu-id="cda6b-111">Lync Server 2013 でのホスト型ボイス メールに対するユーザーの有効化</span><span class="sxs-lookup"><span data-stu-id="cda6b-111">Enable users for hosted voice mail in Lync Server 2013</span></span>](lync-server-2013-enable-users-for-hosted-voice-mail.md)

  - [<span data-ttu-id="cda6b-112">Lync Server 2013 での Hosted Exchange UM の連絡先オブジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="cda6b-112">Create contact objects for hosted Exchange UM in Lync Server 2013</span></span>](lync-server-2013-create-contact-objects-for-hosted-exchange-um.md)

<span data-ttu-id="cda6b-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cda6b-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

