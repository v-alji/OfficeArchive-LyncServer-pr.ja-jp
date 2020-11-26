---
title: ポートの概要-拡張可能なメッセージングとプレゼンスプロトコル (XMPP) フェデレーション
description: ポート概要-拡張可能なメッセージングとプレゼンスプロトコル (XMPP) フェデレーション。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary -  Extensible messaging and presence protocol (XMPP) federation
ms:assetid: 62e98fab-7add-4983-a3fa-dbe74e1c3849
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ618371(v=OCS.15)
ms:contentKeyID: 49105658
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9508bc8b9fbcca6fb6a37478def258a9fa52c373
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442804"
---
# <a name="port-summary---extensible-messaging-and-presence-protocol-xmpp-federation-in-lync-server-2013"></a><span data-ttu-id="2a8b6-103">ポート概要-Lync Server 2013 での拡張可能なメッセージングとプレゼンスプロトコル (XMPP) フェデレーション</span><span class="sxs-lookup"><span data-stu-id="2a8b6-103">Port summary - Extensible messaging and presence protocol (XMPP) federation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2a8b6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2a8b6-104">

<span> </span></span></span>

<span data-ttu-id="2a8b6-105">_**最終更新日:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="2a8b6-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="2a8b6-106">エッジサーバーに展開された拡張メッセージングとプレゼンスプロトコル (XMPP) プロキシ用に定義されたポートとプロトコルを使うと、XMPP フェデレーションパートナーからエッジサーバーへの通信が可能になり、エッジサーバーから XMPP フェデレーションパートナーへの通信も可能になります。</span><span class="sxs-lookup"><span data-stu-id="2a8b6-106">The ports and protocols defined for the extensible messaging and presence protocol (XMPP) proxy deployed on the Edge Server allow communications from the XMPP federated partner to the Edge Server, and also allows communication from your Edge Server to the XMPP federated partner.</span></span> <span data-ttu-id="2a8b6-107">フロントエンドサーバーまたはフロントエンドプールからエッジサーバーまたはエッジプールへのルールも定義されています。</span><span class="sxs-lookup"><span data-stu-id="2a8b6-107">A rule is also defined on the internal-facing firewall from the Front End Server or Front End pool to the Edge Server or Edge pool.</span></span>

<div>

## <a name="firewall-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="2a8b6-108">拡張メッセージングとプレゼンスプロトコルのファイアウォールの概要</span><span class="sxs-lookup"><span data-stu-id="2a8b6-108">Firewall Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2a8b6-109">Protocol/TCP または UDP/ポート</span><span class="sxs-lookup"><span data-stu-id="2a8b6-109">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="2a8b6-110">ソース (IP アドレス)</span><span class="sxs-lookup"><span data-stu-id="2a8b6-110">Source (IP address)</span></span></th>
<th><span data-ttu-id="2a8b6-111">宛先 (IP アドレス)</span><span class="sxs-lookup"><span data-stu-id="2a8b6-111">Destination (IP address)</span></span></th>
<th><span data-ttu-id="2a8b6-112">注釈</span><span class="sxs-lookup"><span data-stu-id="2a8b6-112">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2a8b6-113">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="2a8b6-113">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="2a8b6-114">任意</span><span class="sxs-lookup"><span data-stu-id="2a8b6-114">Any</span></span></p></td>
<td><p><span data-ttu-id="2a8b6-115">Access Edge サービスインターフェイスの IP アドレス</span><span class="sxs-lookup"><span data-stu-id="2a8b6-115">Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="2a8b6-116">XMPP 向けの標準的なサーバー間通信ポート。</span><span class="sxs-lookup"><span data-stu-id="2a8b6-116">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="2a8b6-117">フェデレーションされた XMPP パートナーからエッジサーバーの XMPP プロキシへの通信を許可します。</span><span class="sxs-lookup"><span data-stu-id="2a8b6-117">Allows communication to the Edge Server XMPP proxy from federated XMPP partners</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a8b6-118">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="2a8b6-118">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="2a8b6-119">Access Edge サービスインターフェイスの IP アドレス</span><span class="sxs-lookup"><span data-stu-id="2a8b6-119">Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="2a8b6-120">任意</span><span class="sxs-lookup"><span data-stu-id="2a8b6-120">Any</span></span></p></td>
<td><p><span data-ttu-id="2a8b6-121">XMPP 向けの標準的なサーバー間通信ポート。</span><span class="sxs-lookup"><span data-stu-id="2a8b6-121">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="2a8b6-122">エッジサーバーの XMPP プロキシからフェデレーションされた XMPP パートナーへの通信を許可します。</span><span class="sxs-lookup"><span data-stu-id="2a8b6-122">Allows communication from the Edge Server XMPP proxy to federated XMPP partners</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a8b6-123">XMPP/MTLS/23456</span><span class="sxs-lookup"><span data-stu-id="2a8b6-123">XMPP/MTLS/23456</span></span></p></td>
<td><p><span data-ttu-id="2a8b6-124">任意</span><span class="sxs-lookup"><span data-stu-id="2a8b6-124">Any</span></span></p></td>
<td><p><span data-ttu-id="2a8b6-125">内部エッジサーバーインターフェイス IP</span><span class="sxs-lookup"><span data-stu-id="2a8b6-125">Internal Edge Server Interface IP</span></span></p></td>
<td><p><span data-ttu-id="2a8b6-126">フロントエンドサーバーまたはフロントエンドプールの XMPP ゲートウェイからエッジサーバーへの内部の XMPP トラフィック</span><span class="sxs-lookup"><span data-stu-id="2a8b6-126">Internal XMPP traffic from the XMPP Gateway on the Front End Server or Front End pool to the Edge Server</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="2a8b6-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="2a8b6-127">See Also</span></span>


[<span data-ttu-id="2a8b6-128">Lync Server 2013 での XMPP 構成の例  - Google Talk との XMPP フェデレーション</span><span class="sxs-lookup"><span data-stu-id="2a8b6-128">Example XMPP configuration in Lync Server 2013 – XMPP federation with Google Talk</span></span>](lync-server-2013-example-xmpp-configuration-–-xmpp-federation-with-google-talk.md)  


[<span data-ttu-id="2a8b6-129">Lync Server 2013 での組織の XMPP フェデレーション パートナーの管理</span><span class="sxs-lookup"><span data-stu-id="2a8b6-129">Manage XMPP federated partners in Lync Server 2013</span></span>](lync-server-2013-manage-xmpp-federated-partners-for-your-organization.md)  
  

<span data-ttu-id="2a8b6-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2a8b6-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

