---
title: 'Lync Server 2013: 常設チャット サーバーの計画'
description: 'Lync Server 2013: 常設チャットサーバーを計画しています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for Persistent Chat Server
ms:assetid: 57b2f574-234e-4a5a-bb78-8823369ba79e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398381(v=OCS.15)
ms:contentKeyID: 48184190
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6944437492a1eee718a614369201c3548c95864a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424453"
---
# <a name="planning-for-persistent-chat-server-in-lync-server-2013"></a><span data-ttu-id="dbd99-103">Lync Server 2013 での常設チャット サーバーの計画</span><span class="sxs-lookup"><span data-stu-id="dbd99-103">Planning for Persistent Chat Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dbd99-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dbd99-104">

<span> </span></span></span>

<span data-ttu-id="dbd99-105">_**最終更新日:** 2012-10-11_</span><span class="sxs-lookup"><span data-stu-id="dbd99-105">_**Topic Last Modified:** 2012-10-11_</span></span>

<span data-ttu-id="dbd99-106">Lync Server 2013 の常設チャットサーバーを使用して、複数のユーザーが、テキスト、リンク、ファイルなどの特定のトピックに関するコンテンツを投稿してアクセスできるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="dbd99-106">You can use Lync Server 2013, Persistent Chat Server to enable multiple users to participate in conversations in which they post and access content about specific topics, including text, links, and files.</span></span> <span data-ttu-id="dbd99-107">ユーザーはセッション中にリアルタイムで通信することができますが、各セッションのコンテンツは永続的なものであるため、セッションの終了後も引き続き利用できます。</span><span class="sxs-lookup"><span data-stu-id="dbd99-107">Although users can communicate in real time during a session, the content of each session is persistent, which means it continues to be available after a session ends.</span></span>

<span data-ttu-id="dbd99-108">このセクションでは、Lync Server 2013、常設チャットサーバーの展開 (要件の定義、コンポーネントとサポートされているトポロジの特定、展開に関する推奨事項など) の計画に関する考慮事項について説明します。</span><span class="sxs-lookup"><span data-stu-id="dbd99-108">This section describes planning considerations in a Lync Server 2013, Persistent Chat Server deployment, including defining requirements, identifying components and supported topologies, and deployment recommendations.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="dbd99-109">このセクション中</span><span class="sxs-lookup"><span data-stu-id="dbd99-109">In This Section</span></span>

  - [<span data-ttu-id="dbd99-110">Lync Server 2013 の常設チャット サーバーの概要</span><span class="sxs-lookup"><span data-stu-id="dbd99-110">Overview of Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-overview-of-persistent-chat-server.md)

  - [<span data-ttu-id="dbd99-111">Lync Server 2013 での常設チャットサーバーの動作方法</span><span class="sxs-lookup"><span data-stu-id="dbd99-111">How Persistent Chat Server works in Lync Server 2013</span></span>](lync-server-2013-how-persistent-chat-server-works.md)

  - [<span data-ttu-id="dbd99-112">Lync Server 2013 での、組織における常設チャット サーバーに対する要件の定義</span><span class="sxs-lookup"><span data-stu-id="dbd99-112">Defining your organization's requirements for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-defining-your-requirements-for-persistent-chat-server.md)

  - [<span data-ttu-id="dbd99-113">Lync Server 2013 の常設チャットサーバーのコンポーネントとトポロジ</span><span class="sxs-lookup"><span data-stu-id="dbd99-113">Components and topologies for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-components-and-topologies-for-persistent-chat-server.md)

  - [<span data-ttu-id="dbd99-114">Lync Server 2013 の常設チャットサーバーの技術要件</span><span class="sxs-lookup"><span data-stu-id="dbd99-114">Technical requirements for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-technical-requirements-for-persistent-chat-server.md)

  - [<span data-ttu-id="dbd99-115">Lync Server 2013 での常設チャット サーバーのシステムおよびインフラストラクチャのセットアップ</span><span class="sxs-lookup"><span data-stu-id="dbd99-115">Setting up systems and infrastructure for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-setting-up-systems-and-infrastructure-for-persistent-chat-server.md)

  - [<span data-ttu-id="dbd99-116">Lync Server 2013 の常設チャット サーバーの展開チェックリスト</span><span class="sxs-lookup"><span data-stu-id="dbd99-116">Deployment checklist for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-deployment-checklist-for-persistent-chat-server.md)

<span data-ttu-id="dbd99-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dbd99-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

