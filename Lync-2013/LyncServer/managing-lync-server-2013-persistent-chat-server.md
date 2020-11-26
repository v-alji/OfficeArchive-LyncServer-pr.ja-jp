---
title: Lync Server 2013、常設チャット サーバーの管理
description: Lync Server 2013 の常設チャットサーバーを管理します。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing Lync Server 2013, Persistent Chat Server
ms:assetid: 82befdc6-5d32-45f1-bfd7-aaedffed1ab8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398657(v=OCS.15)
ms:contentKeyID: 48184672
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fe5306c79c738d61b70c3dd079fb55650e6fdae9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446907"
---
# <a name="managing-lync-server-2013-persistent-chat-server"></a><span data-ttu-id="f3a50-103">Lync Server 2013、常設チャット サーバーの管理</span><span class="sxs-lookup"><span data-stu-id="f3a50-103">Managing Lync Server 2013, Persistent Chat Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f3a50-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f3a50-104">

<span> </span></span></span>

<span data-ttu-id="f3a50-105">_**最終更新日:** 2012-10-11_</span><span class="sxs-lookup"><span data-stu-id="f3a50-105">_**Topic Last Modified:** 2012-10-11_</span></span>

<span data-ttu-id="f3a50-106">Lync Server 2013 の常設チャットサーバーを使用して、複数のユーザーが、テキスト、リンク、ファイルなどの特定のトピックに関するコンテンツを投稿してアクセスできるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="f3a50-106">You can use Lync Server 2013, Persistent Chat Server to enable multiple users to participate in conversations in which they post and access content about specific topics, including text, links, and files.</span></span> <span data-ttu-id="f3a50-107">ユーザーはセッション中にリアルタイムで通信することができますが、各セッションのコンテンツは永続的であり、セッションが終了した後も引き続き利用可能であることを意味します。</span><span class="sxs-lookup"><span data-stu-id="f3a50-107">Although users can communicate in real time during a session, the content of each session is persistent, which means that it continues to be available after a session ends.</span></span>

<span data-ttu-id="f3a50-108">常設チャットルームの内容は、主に短いテキストメッセージで構成されていますが、 *ストーリー* と呼ばれる長いメッセージと、ハイパーリンク、絵文字、アップロードされたドキュメントにも含めることができます。</span><span class="sxs-lookup"><span data-stu-id="f3a50-108">The content of Persistent Chat rooms consists primarily of short text messages, although it can include longer messages, referred to as *stories*, and also hyperlinks, emoticons, and uploaded documents.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f3a50-109">ファイルのアップロードとダウンロードは Lync 2013 クライアントでサポートされていません。ただし、引き続き Lync Server 2013 の常設チャットサーバーでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="f3a50-109">File upload and download is not supported by the Lync 2013 client; however, it is still supported by Lync Server 2013, Persistent Chat Server.</span></span> <span data-ttu-id="f3a50-110">従来のグループチャットクライアントでは、ファイルの投稿と表示はできますが、Lync 2013 クライアント経由で同じチャットルームにアクセスした場合、ファイルにアクセスすることはできません。</span><span class="sxs-lookup"><span data-stu-id="f3a50-110">The legacy Group Chat client can post and view files, but if the same chat room is accessed via the Lync 2013 client, it will not be able to access the files.</span></span>



</div>

<span data-ttu-id="f3a50-111">チャットルームへのアクセスは、メンバーシップリストによって制御されます。</span><span class="sxs-lookup"><span data-stu-id="f3a50-111">Access to a chat room is controlled by a membership list.</span></span> <span data-ttu-id="f3a50-112">チャットルームの履歴全体は、時系列レビューまたはフルテキスト検索のいずれかのメンバーが利用できます。</span><span class="sxs-lookup"><span data-stu-id="f3a50-112">The entire chat room history is available to any member for chronological review or full-text search.</span></span> <span data-ttu-id="f3a50-113">常設チャットクライアントの使用について詳しくは、「計画ドキュメントの [Lync server 2013 でのクライアントの計画](lync-server-2013-planning-for-clients.md) 」をご覧ください。展開ドキュメントの [lync server 2013 でクライアントとデバイスを展開](lync-server-2013-deploying-clients-and-devices.md) してください。</span><span class="sxs-lookup"><span data-stu-id="f3a50-113">For details about using the Persistent Chat client, see [Planning for clients in Lync Server 2013](lync-server-2013-planning-for-clients.md) in the Planning documentation, and [Deploying clients and devices in Lync Server 2013](lync-server-2013-deploying-clients-and-devices.md) in the Deployment documentation.</span></span>

<span data-ttu-id="f3a50-114">組織に常設チャットサーバーを設定する場合は、展開時に初期構成を指定します。</span><span class="sxs-lookup"><span data-stu-id="f3a50-114">When you set up Persistent Chat Server for your organization, you specify the initial configuration during deployment.</span></span> <span data-ttu-id="f3a50-115">ただし、常設チャットサーバーサポートの実装方法を変更する必要がある場合もあります。</span><span class="sxs-lookup"><span data-stu-id="f3a50-115">However, there may be times when you want to change how you implement Persistent Chat Server support.</span></span> <span data-ttu-id="f3a50-116">たとえば、組織内の特定のチームまたはグループに対して、常設チャットサーバーのサポートとコントロールを設定する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="f3a50-116">For example, you may need to set up Persistent Chat Server support and controls differently for a specific team or group within your organization.</span></span> <span data-ttu-id="f3a50-117">このセクションには、常設チャットサーバーの展開をカスタマイズするための情報と手順が記載されています。</span><span class="sxs-lookup"><span data-stu-id="f3a50-117">This section provides information and procedures to help you customize your Persistent Chat Server deployment.</span></span> <span data-ttu-id="f3a50-118">常設チャットサーバー用に構成できる機能の詳細については、計画ドキュメントの「 [Lync server 2013 での常設チャットサーバーに関する組織の要件の定義](lync-server-2013-defining-your-requirements-for-persistent-chat-server.md) 」と「計画ドキュメント、展開ドキュメント、または運用ドキュメント」の「 [lync server 2013 での常設チャットサーバーの動作](lync-server-2013-how-persistent-chat-server-works.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f3a50-118">For details about the features and functionality that you can configure for Persistent Chat Server, see [Defining your organization's requirements for Persistent Chat Server in Lync Server 2013](lync-server-2013-defining-your-requirements-for-persistent-chat-server.md) in the Planning documentation, and [How Persistent Chat Server works in Lync Server 2013](lync-server-2013-how-persistent-chat-server-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span> <span data-ttu-id="f3a50-119">Lync Server 2013 用の常設チャットサーバーの展開について詳しくは、展開ドキュメントの「 [Lync server 2013 での常設チャットサーバーの展開](lync-server-2013-deploying-persistent-chat-server.md) 」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="f3a50-119">For details about deploying Persistent Chat Server for Lync Server 2013, see [Deploying Persistent Chat Server in Lync Server 2013](lync-server-2013-deploying-persistent-chat-server.md) in the Deployment documentation.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="f3a50-120">このセクション中</span><span class="sxs-lookup"><span data-stu-id="f3a50-120">In This Section</span></span>

  - [<span data-ttu-id="f3a50-121">Lync Server 2013 での常設チャットサーバーの動作方法</span><span class="sxs-lookup"><span data-stu-id="f3a50-121">How Persistent Chat Server works in Lync Server 2013</span></span>](lync-server-2013-how-persistent-chat-server-works.md)

  - [<span data-ttu-id="f3a50-122">カテゴリを使用して常設チャット サーバーを管理する</span><span class="sxs-lookup"><span data-stu-id="f3a50-122">Using categories to administer Persistent Chat Server</span></span>](using-categories-to-administer-persistent-chat-server.md)

  - [<span data-ttu-id="f3a50-123">常設チャットのメンバーシップについて</span><span class="sxs-lookup"><span data-stu-id="f3a50-123">Understanding Persistent Chat membership</span></span>](understanding-persistent-chat-membership.md)

  - [<span data-ttu-id="f3a50-124">常設チャット サーバーのベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="f3a50-124">Persistent Chat Server best practices</span></span>](persistent-chat-server-best-practices.md)

  - [<span data-ttu-id="f3a50-125">Lync Server 2013 でのカテゴリ、ルーム、およびアドインの管理</span><span class="sxs-lookup"><span data-stu-id="f3a50-125">Managing categories, rooms, and add-ins in Lync Server 2013</span></span>](lync-server-2013-managing-categories-rooms-and-add-ins.md)

  - [<span data-ttu-id="f3a50-126">Lync Server 2013 での常設チャットのユーザー アクセスの管理</span><span class="sxs-lookup"><span data-stu-id="f3a50-126">Managing Persistent Chat user access in Lync Server 2013</span></span>](lync-server-2013-managing-persistent-chat-user-access.md)

  - [<span data-ttu-id="f3a50-127">Lync Server 2013 での常設チャット システムの運用および保守</span><span class="sxs-lookup"><span data-stu-id="f3a50-127">Operating and maintaining the Persistent Chat system in Lync Server 2013</span></span>](lync-server-2013-operating-and-maintaining-the-persistent-chat-system.md)

<span data-ttu-id="f3a50-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f3a50-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

