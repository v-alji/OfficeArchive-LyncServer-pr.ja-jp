---
title: 'Lync Server 2013: フロントエンド サーバー、インスタント メッセージングおよびプレゼンスの特徴と機能'
description: 'Lync Server 2013: フロントエンドサーバー、インスタントメッセージング、プレゼンスの機能と機能。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Features and functionality of Front End Servers, instant messaging, and presence
ms:assetid: 05b29536-dcd7-49b5-934a-2ebf20ddc45c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398109(v=OCS.15)
ms:contentKeyID: 48183294
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b5c8bc3db255228da3366eb5aa142cd5adc233d1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398175"
---
# <a name="features-and-functionality-of-front-end-servers-instant-messaging-and-presence-in-lync-server-2013"></a><span data-ttu-id="d704d-103">Lync Server 2013 のフロントエンド サーバー、インスタント メッセージングおよびプレゼンスの特徴と機能</span><span class="sxs-lookup"><span data-stu-id="d704d-103">Features and functionality of Front End Servers, instant messaging, and presence in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d704d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d704d-104">

<span> </span></span></span>

<span data-ttu-id="d704d-105">_**最終更新日:** 2013-03-17_</span><span class="sxs-lookup"><span data-stu-id="d704d-105">_**Topic Last Modified:** 2013-03-17_</span></span>

<span data-ttu-id="d704d-106">フロントエンドサーバーは、ほとんどの Lync Server 機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="d704d-106">Front End Servers provide most Lync Server functionality.</span></span> <span data-ttu-id="d704d-107">次の2つのエディションがあります。 Lync Server Enterprise Edition は、主に大規模な組織向けに設計されています。また、主に小規模の組織向けに設計されています。これは、ハードウェアの investement を減らし、高可用性を必要としないようにします。</span><span class="sxs-lookup"><span data-stu-id="d704d-107">There are two editions available: Lync Server Enterprise Edition, which is designed primarily for larger organizations, and Lync Server Standard Edition, which is designed primarily for smaller organizations which want a smaller hardware investement and do not require high availability.</span></span> <span data-ttu-id="d704d-108">どちらのエディションも、IM、プレゼンス、会議、エンタープライズ Voip などのすべての Lync Server ワークロードをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="d704d-108">Both editions support all Lync Server workloads including IM, presence, conferencing, and Enterprise Voice.</span></span>

<span data-ttu-id="d704d-109">インスタント メッセージング (IM) を使用すると、ユーザーは各自のコンピューターでテキスト ベースのメッセージを使用して、リアルタイムで相互通信を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="d704d-109">Instant messaging (IM) enables your users to communicate with each other in real time on their computers using text-based messages.</span></span> <span data-ttu-id="d704d-110">2 パーティとマルチパーティの両方の IM セッションがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="d704d-110">Both two-party and multiparty IM sessions are supported.</span></span> <span data-ttu-id="d704d-111">2 パーティの IM 会話の参加者は、3 番目の参加者をいつでも会話に追加できます。</span><span class="sxs-lookup"><span data-stu-id="d704d-111">A participant in a two-party IM conversation can add a third participant to the conversation at any time.</span></span> <span data-ttu-id="d704d-112">この際には、会議機能をサポートするように会話ウィンドウが変更されます。</span><span class="sxs-lookup"><span data-stu-id="d704d-112">When this happens, the Conversation window changes to support conferencing features.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="d704d-113">Lync と Communicator クライアントが1対1の通信に関わる場合、ピアツーピアと呼ばれることがよくあります。</span><span class="sxs-lookup"><span data-stu-id="d704d-113">Lync and Communicator clients when involved in a one to one communication, is often referred to as peer-to-peer.</span></span> <span data-ttu-id="d704d-114">技術的には、2つのクライアントは1つの会話と1つの会話の間でやり取りされ、中央にはインスタントメッセージング multipoint コントロールユニット (IMMCU) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d704d-114">Technically, the two clients are communicating in a one to one conversation, with the Instant Messaging multipoint control unit (IMMCU) in the middle.</span></span> <span data-ttu-id="d704d-115">IMMCU は、フロントエンドサーバーのコンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="d704d-115">The IMMCU is a component of Front End Server.</span></span> <span data-ttu-id="d704d-116">必要な通信ワークフローに IMMCU を配置すると、フロントエンドサーバーが有効になっている通話の詳細の記録とその他の機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="d704d-116">Placing the IMMCU in the required communication workflow allows call detail recording and other features that the Front End Server enables.</span></span> <span data-ttu-id="d704d-117">通信は、クライアント上の動的ソースポートからフロントエンドサーバーポート TLS/TCP/5061 に送信されます (推奨トランスポート層セキュリティを使用していることを前提としています)。</span><span class="sxs-lookup"><span data-stu-id="d704d-117">Communication is from a dynamic source port on the client to the Front End Server port TLS/TCP/5061 (assuming the use of the recommended transport layer security).</span></span> <span data-ttu-id="d704d-118">設計上、ピアツーピア通信 (およびマルチパーティの IM) は、Lync Server と IMMCU がアクティブで利用可能な場合にのみ可能です。</span><span class="sxs-lookup"><span data-stu-id="d704d-118">By design, peer-to-peer communication (as well as multi-party IM) is possible only when Lync Server and the IMMCU is active and available.</span></span>



</div>

<span data-ttu-id="d704d-119">*プレゼンス* は、ネットワーク上の他の状態に関する情報をユーザーに提供します。</span><span class="sxs-lookup"><span data-stu-id="d704d-119">*Presence* provides information to users about the status of other on the network.</span></span> <span data-ttu-id="d704d-120">ユーザーのプレゼンス状態からは、他のユーザーがそのユーザーに連絡してもよいかどうかや、連絡する場合にインスタント メッセージング、電話、メールのどれを使用するかを判断するのに役立つ情報が得られます。</span><span class="sxs-lookup"><span data-stu-id="d704d-120">A user’s presence status provides information to help others decide whether they should try to contact the user and whether to use instant messaging, phone, or email.</span></span> <span data-ttu-id="d704d-121">プレゼンスにより、可能な場合にはすぐにやりとりできますが、他にも、ユーザーが会議中であるかどうかや、外出のために応答できない状況なのかに関する情報も提供されます。</span><span class="sxs-lookup"><span data-stu-id="d704d-121">Presence encourages instant communication when possible, but it also provides information about whether a user is in a meeting or out of the office, indicating that instant communication is not possible.</span></span> <span data-ttu-id="d704d-122">このプレゼンス状態は、Microsoft Outlook メッセージングおよびコラボレーションクライアント、Microsoft SharePoint テクノロジ、Microsoft Word、Microsoft Excel スプレッドシートソフトウェアなど、Lync およびその他のプレゼンスに対応しているアプリケーションのプレゼンスアイコンとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="d704d-122">This presence status is displayed as a presence icon in Lync and other presence-aware applications, including the Microsoft Outlook messaging and collaboration client, Microsoft SharePoint technologies, Microsoft Word, and Microsoft Excel spreadsheet software.</span></span> <span data-ttu-id="d704d-123">プレゼンス アイコンからは、そのユーザーの現在の状態と、連絡してもよいかどうかを判別できます。</span><span class="sxs-lookup"><span data-stu-id="d704d-123">The presence icon represents the user’s current availability and willingness to communicate.</span></span>

<span data-ttu-id="d704d-124"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d704d-124"></div>

<span> </span>

</div>

</div>

</span></span></div>

