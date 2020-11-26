---
title: 'Lync Server 2013: 組織の XMPP フェデレーション パートナーの管理'
description: 'Lync Server 2013: 組織の XMPP フェデレーションパートナーを管理します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Manage XMPP federated partners for your organization
ms:assetid: 48681433-725d-457f-926b-f91d95bcf082
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ552450(v=OCS.15)
ms:contentKeyID: 48679561
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 37d6fb4104c35ffc7db9649656f7786568a48b61
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426026"
---
# <a name="manage-xmpp-federated-partners-in-lync-server-2013"></a><span data-ttu-id="48e3a-103">Lync Server 2013 での組織の XMPP フェデレーション パートナーの管理</span><span class="sxs-lookup"><span data-stu-id="48e3a-103">Manage XMPP federated partners in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="48e3a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="48e3a-104">

<span> </span></span></span>

<span data-ttu-id="48e3a-105">_**最終更新日:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="48e3a-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="48e3a-106">このドキュメントは暫定版であり、変更される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="48e3a-106">This is preliminary documentation and is subject to change.</span></span> <span data-ttu-id="48e3a-107">空白のトピックがプレースホルダーとして含まれています。</span><span class="sxs-lookup"><span data-stu-id="48e3a-107">Blank topics are included as placeholders.</span></span>

<span data-ttu-id="48e3a-108">XMPP フェデレーションドメインのユーザーのサポートを管理するには、次の操作を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="48e3a-108">To manage support for users of XMPP federated domains, you need to do the following:</span></span>

  - <span data-ttu-id="48e3a-109">XMPP フェデレーションドメインのユーザーをサポートするために、1つ以上の外部アクセスポリシーを構成します。</span><span class="sxs-lookup"><span data-stu-id="48e3a-109">Configure one or more external access policies to support users of XMPP federated domains.</span></span>

  - <span data-ttu-id="48e3a-110">アクセスエッジ構成ポリシーを構成してフェデレーションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="48e3a-110">Configure Access Edge Configuration policy to support federation.</span></span>

  - <span data-ttu-id="48e3a-111">XMPP フェデレーションパートナーの定義を作成します。</span><span class="sxs-lookup"><span data-stu-id="48e3a-111">Create XMPP Federated Partners definitions.</span></span>

  - <span data-ttu-id="48e3a-112">XMPP フェデレーションで利用可能なネゴシエーション設定について説明します。</span><span class="sxs-lookup"><span data-stu-id="48e3a-112">Understand negotiation settings available for XMPP federation.</span></span>

<span data-ttu-id="48e3a-113">これらのタスクを実行するには、このセクションの手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="48e3a-113">To perform these tasks, use the procedures in this section.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="48e3a-114">このセクション中</span><span class="sxs-lookup"><span data-stu-id="48e3a-114">In This Section</span></span>

  - [<span data-ttu-id="48e3a-115">Lync Server 2013 での XMPP パートナー構成の作成または編集</span><span class="sxs-lookup"><span data-stu-id="48e3a-115">Create or edit XMPP partner configuration in Lync Server 2013</span></span>](lync-server-2013-create-or-edit-xmpp-partner-configuration.md)

  - [<span data-ttu-id="48e3a-116">Lync Server 2013 の XMPP フェデレーション パートナーのネゴシエーション設定</span><span class="sxs-lookup"><span data-stu-id="48e3a-116">Negotiation settings for XMPP federated partners in Lync Server 2013</span></span>](lync-server-2013-negotiation-settings-for-xmpp-federated-partners.md)

  - [<span data-ttu-id="48e3a-117">Lync Server 2013 での XMPP 構成の例  - Google Talk との XMPP フェデレーション</span><span class="sxs-lookup"><span data-stu-id="48e3a-117">Example XMPP configuration in Lync Server 2013 – XMPP federation with Google Talk</span></span>](lync-server-2013-example-xmpp-configuration-–-xmpp-federation-with-google-talk.md)

<span data-ttu-id="48e3a-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="48e3a-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

