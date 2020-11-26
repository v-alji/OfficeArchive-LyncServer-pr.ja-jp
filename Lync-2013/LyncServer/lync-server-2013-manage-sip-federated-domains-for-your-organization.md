---
title: 'Lync Server 2013: 組織の SIP フェデレーション ドメインの管理'
description: 'Lync Server 2013: 組織の SIP フェデレーションドメインを管理します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Manage SIP federated domains for your organization
ms:assetid: abc48829-e5cf-4651-bc38-899192f5c3bc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ552454(v=OCS.15)
ms:contentKeyID: 48679565
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6fcb8851af7e623251e5c0b635e67e524355fd4c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426033"
---
# <a name="manage-sip-federated-domains-for-your-organization-in-lync-server-2013"></a><span data-ttu-id="0213d-103">Lync Server 2013 での組織の SIP フェデレーション ドメインの管理</span><span class="sxs-lookup"><span data-stu-id="0213d-103">Manage SIP federated domains for your organization in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0213d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0213d-104">

<span> </span></span></span>

<span data-ttu-id="0213d-105">_**最終更新日:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="0213d-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="0213d-106">このドキュメントは暫定版であり、変更される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0213d-106">This is preliminary documentation and is subject to change.</span></span> <span data-ttu-id="0213d-107">空白のトピックがプレースホルダーとして含まれています。</span><span class="sxs-lookup"><span data-stu-id="0213d-107">Blank topics are included as placeholders.</span></span>

<span data-ttu-id="0213d-108">フェデレーションできる SIP ドメインを管理して構成するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="0213d-108">To manage and configure SIP domains that you can federate with, you can do the following:</span></span>

  - <span data-ttu-id="0213d-109">SIP フェデレーションパートナードメインの許可ドメインリストを作成または編集します。</span><span class="sxs-lookup"><span data-stu-id="0213d-109">Create or edit an allowed domain list of SIP federated partner domains.</span></span>

  - <span data-ttu-id="0213d-110">SIP フェデレーションドメインのブロックドメインリストを作成または編集します。</span><span class="sxs-lookup"><span data-stu-id="0213d-110">Create or edit a blocked domain list of SIP federated domains.</span></span>

<span data-ttu-id="0213d-111">これらのタスクを実行するには、このセクションの手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="0213d-111">To perform these tasks, use the procedures in this section.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="0213d-112">このセクション中</span><span class="sxs-lookup"><span data-stu-id="0213d-112">In This Section</span></span>

  - [<span data-ttu-id="0213d-113">Lync Server 2013 での、許可された外部ドメイン向けサポートの構成</span><span class="sxs-lookup"><span data-stu-id="0213d-113">Configure support for allowed external domains in Lync Server 2013</span></span>](lync-server-2013-configure-support-for-allowed-external-domains.md)

  - [<span data-ttu-id="0213d-114">Lync Server 2013 での禁止された外部ドメイン向けサポートの構成</span><span class="sxs-lookup"><span data-stu-id="0213d-114">Configure support for blocked external domains in Lync Server 2013</span></span>](lync-server-2013-configure-support-for-blocked-external-domains.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="0213d-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="0213d-115">See Also</span></span>


[<span data-ttu-id="0213d-116">Lync Server 2013 でのフェデレーション ユーザー アクセスを制御するポリシーの構成</span><span class="sxs-lookup"><span data-stu-id="0213d-116">Configure policies to control federated user access in Lync Server 2013</span></span>](lync-server-2013-configure-policies-to-control-federated-user-access.md)  
[<span data-ttu-id="0213d-117">Lync Server 2013 でのフェデレーションおよびパブリック IM 接続の有効化または無効化</span><span class="sxs-lookup"><span data-stu-id="0213d-117">Enable or disable federation and public IM connectivity in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md)  
[<span data-ttu-id="0213d-118">Lync Server 2013 でのフェデレーション パートナーの検出の有効化または無効化</span><span class="sxs-lookup"><span data-stu-id="0213d-118">Enable or disable discovery of federation partners in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-discovery-of-federation-partners.md)  
  

<span data-ttu-id="0213d-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0213d-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

