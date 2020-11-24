---
title: 'Lync Server 2013: Exchange ユニファイド メッセージング (UM) のサポート'
description: 'Lync Server 2013: Exchange ユニファイドメッセージング (UM) がサポートされています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Exchange Unified Messaging (UM) support
ms:assetid: 0da62b8d-7416-4fb8-a405-381ca805c53a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398179(v=OCS.15)
ms:contentKeyID: 48183405
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 563517bb72167bbab0b08eba3b1359ae3ab52836
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399735"
---
# <a name="exchange-unified-messaging-um-support-in-lync-server-2013"></a><span data-ttu-id="0dbd0-103">Lync Server 2013 での Exchange ユニファイド メッセージング (UM) のサポート</span><span class="sxs-lookup"><span data-stu-id="0dbd0-103">Exchange Unified Messaging (UM) support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0dbd0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0dbd0-104">

<span> </span></span></span>

<span data-ttu-id="0dbd0-105">_**最終更新日:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="0dbd0-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="0dbd0-106">Lync Server 2013 は、音声メッセージとメールメッセージを1つのメッセージングインフラストラクチャに統合するための Exchange ユニファイドメッセージング (UM) との統合をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="0dbd0-106">Lync Server 2013 supports integration with Exchange Unified Messaging (UM) for combining voice messaging and email messaging into a single messaging infrastructure.</span></span> <span data-ttu-id="0dbd0-107">Exchange 2013 では、exchange UM は、メールボックスサーバーにインストールされて実行される Exchange UM サービスで構成され、クライアントアクセスサーバー上にインストールされて実行される UM 呼び出しルーターです。</span><span class="sxs-lookup"><span data-stu-id="0dbd0-107">In Exchange 2013, Exchange UM consists of the Exchange UM service, which is installed and runs on the Mailbox server, and the UM Call Router, which is installed and runs on the Client Access server.</span></span> <span data-ttu-id="0dbd0-108">Lync Server 2013 エンタープライズ Voip 展開の場合、Exchange UM では、音声メッセージとメールメッセージが、電話からアクセスできる単一のストア (つまり、Outlook Voice Access) またはコンピューターに統合されています。</span><span class="sxs-lookup"><span data-stu-id="0dbd0-108">For Lync Server 2013 Enterprise Voice deployments, Exchange UM combines voice messaging and email messaging into a single store that is accessible from a telephone (that is, Outlook Voice Access) or a computer.</span></span> <span data-ttu-id="0dbd0-109">Exchange UM および Lync Server 2013 は、エンタープライズボイスのユーザーに対して、通話の応答、Outlook Voice Access、自動応答サービスを提供するために連携します。</span><span class="sxs-lookup"><span data-stu-id="0dbd0-109">Exchange UM and Lync Server 2013 work together to provide call answering, Outlook Voice Access, and auto attendant services to users of Enterprise Voice.</span></span>

<span data-ttu-id="0dbd0-110">Lync Server 2013 は、Exchange UM のオンプレミス展開との統合に加えて、ホストされた Exchange UM との統合をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="0dbd0-110">In addition to the support for integration with on-premises deployments of Exchange UM, Lync Server 2013 supports integration with hosted Exchange UM.</span></span> <span data-ttu-id="0dbd0-111">これにより、一部またはすべてのユーザーを、Microsoft Exchange Online などのホストされた Exchange サービスプロバイダーに移行した場合に、ユーザーに音声メッセージを提供できます。</span><span class="sxs-lookup"><span data-stu-id="0dbd0-111">This enables you to provide voice messaging to your users if you migrate some or all of them to a hosted Exchange service provider such as Microsoft Exchange Online.</span></span>

<span data-ttu-id="0dbd0-112">Lync Server 2013 では、次のバージョンがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="0dbd0-112">Lync Server 2013 supports the following versions:</span></span>

  - <span data-ttu-id="0dbd0-113">Microsoft Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="0dbd0-113">Microsoft Exchange 2013</span></span>

  - <span data-ttu-id="0dbd0-114">Microsoft Exchange Server 2010 (必須) または最新の service pack (推奨)</span><span class="sxs-lookup"><span data-stu-id="0dbd0-114">Microsoft Exchange Server 2010 (required) or with latest service pack (recommended)</span></span>

  - <span data-ttu-id="0dbd0-115">Microsoft Exchange Server 2007 Service Pack 1 (SP1) (必須) または最新の Service pack (推奨)</span><span class="sxs-lookup"><span data-stu-id="0dbd0-115">Microsoft Exchange Server 2007 with Service Pack 1 (SP1) (required) or latest service pack (recommended)</span></span>

<span data-ttu-id="0dbd0-116">Lync Server 2013 または Lync Server 2013 データベースで Exchange UM を検索することはできません。</span><span class="sxs-lookup"><span data-stu-id="0dbd0-116">You cannot collocate Exchange UM with Lync Server 2013 or a Lync Server 2013 database.</span></span> <span data-ttu-id="0dbd0-117">Exchange UM と Lync Server 2013 は、別々のフォレストにインストールできます。</span><span class="sxs-lookup"><span data-stu-id="0dbd0-117">You can install Exchange UM and Lync Server 2013 in separate forests.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="0dbd0-118">Pbx が展開されているエンタープライズ Voip 展開では、すべてのユーザーにボイスメールと関連サービスを提供することができるため、Exchange UM が不要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="0dbd0-118">Exchange UM may not be required for Enterprise Voice deployments that have a PBX deployed, because the PBX can continue to provide voice mail and related services to all users.</span></span> <span data-ttu-id="0dbd0-119">最終的に PBX を廃止する場合 (たとえば、公衆交換電話網 (PSTN) 接続用に SIP トランクを展開した場合など) は、PBX ボイスメールシステムを使用していたユーザーにボイスメールを提供するように Exchange UM を再設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0dbd0-119">If you eventually retire the PBX (for example, if you deploy SIP trunking for public switched telephone network (PSTN) connectivity), you must reconfigure Exchange UM to provide voice mail to users who previously used the PBX voice mail system.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="0dbd0-120">このセクション中</span><span class="sxs-lookup"><span data-stu-id="0dbd0-120">In This Section</span></span>

  - [<span data-ttu-id="0dbd0-121">Lync Server 2013 の社内ユニファイド メッセージングのコンポーネントとトポロジ</span><span class="sxs-lookup"><span data-stu-id="0dbd0-121">Components and topologies for on-premises Unified Messaging in Lync Server 2013</span></span>](lync-server-2013-components-and-topologies-for-on-premises-unified-messaging.md)

  - [<span data-ttu-id="0dbd0-122">Lync Server 2013 でのホスト型 Exchange UM 統合のサポート</span><span class="sxs-lookup"><span data-stu-id="0dbd0-122">Support for hosted Exchange UM integration in Lync Server 2013</span></span>](lync-server-2013-support-for-hosted-exchange-um-integration.md)

<span data-ttu-id="0dbd0-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0dbd0-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

