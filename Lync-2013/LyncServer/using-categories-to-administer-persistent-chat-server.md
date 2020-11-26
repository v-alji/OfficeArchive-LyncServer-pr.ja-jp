---
title: カテゴリを使用して常設チャット サーバーを管理する
description: カテゴリを使って常設チャットサーバーを管理する。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Using categories to administer Persistent Chat Server
ms:assetid: dfcb3ad1-da90-467e-b08c-f4e68673b7b5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398988(v=OCS.15)
ms:contentKeyID: 48185628
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 181ecba944a042e3598b2964ad233590cf63349e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443168"
---
# <a name="using-categories-to-administer-persistent-chat-server"></a><span data-ttu-id="140b0-103">カテゴリを使用して常設チャット サーバーを管理する</span><span class="sxs-lookup"><span data-stu-id="140b0-103">Using categories to administer Persistent Chat Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="140b0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="140b0-104">

<span> </span></span></span>

<span data-ttu-id="140b0-105">_**最終更新日:** 2013-10-01_</span><span class="sxs-lookup"><span data-stu-id="140b0-105">_**Topic Last Modified:** 2013-10-01_</span></span>

<span data-ttu-id="140b0-106">常設チャットサーバーの展開では、多数の同時常設チャットルームをホストできます。</span><span class="sxs-lookup"><span data-stu-id="140b0-106">Your Persistent Chat Server deployment can host many concurrent Persistent Chat rooms.</span></span> <span data-ttu-id="140b0-107">チャット ルームは、サーバーで一連のカテゴリに編成できます。</span><span class="sxs-lookup"><span data-stu-id="140b0-107">Chat rooms can be organized into a set of categories on the server.</span></span> <span data-ttu-id="140b0-108">各チャット ルームは 1 つのカテゴリに属し、そのカテゴリからいくつかの設定を継承します。</span><span class="sxs-lookup"><span data-stu-id="140b0-108">Each chat room belongs to one category, and inherits some settings from that category.</span></span> <span data-ttu-id="140b0-109">この編成によって、業務目的に基づいて会話を識別するのに便利な構造が作成され、管理の委任および管理の簡素化が容易になります。</span><span class="sxs-lookup"><span data-stu-id="140b0-109">This organization creates a useful structure for identifying conversations, based on their business purpose, and facilitates delegated administration and simplified management.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="140b0-110">ユーザーに対して常設チャット (Lync client) を実行しているコンピューターでは、チャットルームの管理機能の多くは使用できますが、 <STRONG>cspersistentchatadministrator</STRONG> ロールの常設チャット管理者は、Lync Server コントロールパネルまたは Windows PowerShell コマンドレットを使用してカテゴリを作成または管理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="140b0-110">Although many of the management features of chat rooms are available in computers running Persistent Chat (Lync client) for the user, Persistent Chat Administrators (in the <STRONG>cspersistentchatadministrator</STRONG> role) must use the Lync Server Control Panel or Windows PowerShell cmdlets to create or manage categories.</span></span>



</div>

<span data-ttu-id="140b0-111">常設チャット管理者は、Lync Server コントロールパネルまたは Windows PowerShell コマンドレットを使ってカテゴリを作成および管理し、組織内のユーザーのチャットルームへのアクセスを設計します。</span><span class="sxs-lookup"><span data-stu-id="140b0-111">Persistent Chat administrators use Lync Server Control Panel or Windows PowerShell cmdlets to create and manage categories, and to design access for chat rooms for the users in their organization.</span></span>

<span data-ttu-id="140b0-112">チャットルーム管理者は、1人または複数のチャットルームを管理する機能を備えています。 Lync クライアントを使用して、会議室の作成と管理を行うことができます (または、ユーザーがカスタムソリューションとワークフローを作成して呼び出すことができます)。</span><span class="sxs-lookup"><span data-stu-id="140b0-112">Persistent Chat room managers, who have the ability to manage one or more chat rooms, can use the Lync client to launch a room management Web application to create and manage rooms (or customers can create custom solutions and workflows to be invoked).</span></span> <span data-ttu-id="140b0-113">常設チャット管理者は、Lync Server コントロールパネルまたは Windows PowerShell コマンドレットを使って、会議室の作成と管理を行うこともできます。</span><span class="sxs-lookup"><span data-stu-id="140b0-113">Persistent Chat administrators can also use Lync Server Control Panel or Windows PowerShell cmdlets to create and manage rooms.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="140b0-114">常設チャットルームには、常設チャットカテゴリと同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="140b0-114">A Persistent Chat room cannot have the same name as a Persistent Chat category.</span></span>



</div>

<span data-ttu-id="140b0-p103">チャット ルームのマネージャーは、チャット ルームのカテゴリ変更を除いて、チャット ルームのすべてのプロパティに変更を加えることができます。チャット ルームのマネージャーが行う以下の操作は制限できません。</span><span class="sxs-lookup"><span data-stu-id="140b0-p103">Chat room managers can make changes to all chat room properties, except for changing the category of the room. They cannot be restricted from performing the following actions:</span></span>

  - <span data-ttu-id="140b0-117">チャット ルームを無効にする</span><span class="sxs-lookup"><span data-stu-id="140b0-117">Disabling a chat room</span></span>

  - <span data-ttu-id="140b0-118">チャット ルームの名前を変更する</span><span class="sxs-lookup"><span data-stu-id="140b0-118">Changing a chat room name</span></span>

  - <span data-ttu-id="140b0-119">チャット ルームの説明を変更する</span><span class="sxs-lookup"><span data-stu-id="140b0-119">Changing a chat room description</span></span>

  - <span data-ttu-id="140b0-120">チャット ルームの種類 (大会議室と標準) を変更する</span><span class="sxs-lookup"><span data-stu-id="140b0-120">Changing a chat room type (Auditorium versus Normal)</span></span>

  - <span data-ttu-id="140b0-121">チャット ルームのプライバシーを変更する (開く、閉じる、非公開にする)</span><span class="sxs-lookup"><span data-stu-id="140b0-121">Changing the privacy of a room (open versus closed versus secret)</span></span>

  - <span data-ttu-id="140b0-122">メンバーを追加または削除する</span><span class="sxs-lookup"><span data-stu-id="140b0-122">Adding or removing members</span></span>

  - <span data-ttu-id="140b0-123">チャット ルーム マネージャーを追加または削除する</span><span class="sxs-lookup"><span data-stu-id="140b0-123">Adding or removing chat room managers</span></span>

  - <span data-ttu-id="140b0-124">アドインを追加または削除する</span><span class="sxs-lookup"><span data-stu-id="140b0-124">Adding or removing an add-in</span></span>

  - <span data-ttu-id="140b0-125">招待状などの設定を変更する (カテゴリで許可されている設定に応じて)</span><span class="sxs-lookup"><span data-stu-id="140b0-125">Changing settings such as invitations (according to what’s permitted by the category)</span></span>

<div>

## <a name="delegated-administration"></a><span data-ttu-id="140b0-126">代理管理</span><span class="sxs-lookup"><span data-stu-id="140b0-126">Delegated Administration</span></span>

<span data-ttu-id="140b0-127">永続的なチャットルームの作成と管理は、カテゴリを適切に使用することで非常に簡単になります。</span><span class="sxs-lookup"><span data-stu-id="140b0-127">Creating and managing Persistent Chat rooms is much easier with the correct use of categories.</span></span> <span data-ttu-id="140b0-128">常設チャット管理者は、各カテゴリの **Allowedmembers** と **クリエーター** を定義できます。また、カテゴリで作成されたすべてのチャットルームに適用される既定のチャットルームの設定と動作も定義できます。</span><span class="sxs-lookup"><span data-stu-id="140b0-128">A Persistent Chat Administrator can define **AllowedMembers** and **Creators** for each category, and can also define the default chat room settings and behaviors that will be applied to all chat rooms created in the category.</span></span> <span data-ttu-id="140b0-129">常設チャット管理者は、Lync Server コントロールパネルまたは Windows PowerShell コマンドレットを使用して、カテゴリの作成と管理を行います。</span><span class="sxs-lookup"><span data-stu-id="140b0-129">Persistent Chat administrators create and manage categories by using Lync Server Control Panel or Windows PowerShell cmdlets.</span></span>

<span data-ttu-id="140b0-p105">カテゴリの Creators として特定されるユーザー、組織単位 (OU)、ユーザー グループは、そのカテゴリのチャット ルームの作成を許可されている個人およびグループです。カテゴリを作成した後、これらの個人およびグループは、**AllowedMembers** リストからユーザー、OU、ユーザー グループをチャット ルームの管理と参加が可能なマネージャーおよびメンバーとして選択できます。</span><span class="sxs-lookup"><span data-stu-id="140b0-p105">Users, Organizational Units (OUs), and user groups that are identified as Creators of the category are the only individuals and groups that are allowed to create rooms in the category. After the category is created, they can choose users, OUs, and user groups from the category’s **AllowedMembers** list as chat room managers and members to manage and participate in the room.</span></span>

<span data-ttu-id="140b0-132">カテゴリで作成されたチャットルームは、カテゴリによって適用されるポリシーと設定 (ルームのメンバーシップに含まれるユーザー、ルームを管理できるユーザー、ファイルのアップロードが許可されているかどうか、招待を送信するかどうかなど) に従っています。</span><span class="sxs-lookup"><span data-stu-id="140b0-132">Chat rooms that are created in a category adhere to the policies and settings enforced by the category (such as who can be in the room’s membership, who can manage the room, whether file uploads are allowed, whether invitations are sent, and so on).</span></span>

<span data-ttu-id="140b0-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="140b0-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

