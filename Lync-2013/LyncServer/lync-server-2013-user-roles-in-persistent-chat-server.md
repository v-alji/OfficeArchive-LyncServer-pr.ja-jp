---
title: 'Lync Server 2013: 常設チャットサーバーのユーザーロール'
description: 'Lync Server 2013: 常設チャットサーバーのユーザーロール。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: User roles in Persistent Chat Server
ms:assetid: 343a0563-9ca5-4ad0-b4f3-a72f1d7f1a81
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ676774(v=OCS.15)
ms:contentKeyID: 49361095
ms.date: 03/19/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: aed64aaa9129e6667cd138bc4365acfb2a64d52c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439160"
---
# <a name="user-roles-in-persistent-chat-server-in-lync-server-2013"></a><span data-ttu-id="e3ec1-103">Lync Server 2013 の常設チャットサーバーのユーザーロール</span><span class="sxs-lookup"><span data-stu-id="e3ec1-103">User roles in Persistent Chat Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e3ec1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e3ec1-104">

<span> </span></span></span>

<span data-ttu-id="e3ec1-105">_**最終更新日:** 2015-03-19_</span><span class="sxs-lookup"><span data-stu-id="e3ec1-105">_**Topic Last Modified:** 2015-03-19_</span></span>

<span data-ttu-id="e3ec1-106">常設チャットサーバーでは、許可/拒否メンバーの概念が提供されます。これは、常設チャットカテゴリに適用され、特定のカテゴリのルームにアクセスできるユーザーを制御します。</span><span class="sxs-lookup"><span data-stu-id="e3ec1-106">Persistent Chat Server provides the concept of Allowed/Denied members, which applies to Persistent Chat categories and controls who can access rooms in a particular category.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="e3ec1-107">カテゴリ内の許可/拒否メンバーは、常設チャットルームに適用される <STRONG>メンバー</STRONG> の役割とは異なります。</span><span class="sxs-lookup"><span data-stu-id="e3ec1-107">Allowed/Denied members in a Category is not the same as a <STRONG>Member</STRONG> role, which applies to a Persistent Chat room.</span></span><BR><span data-ttu-id="e3ec1-108">検索では、検索を実行しているユーザーが許可/拒否メンバーリストに含まれている、開いているすべての閉じたチャットルームが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e3ec1-108">Searches display all open and closed chat rooms for which the user performing the search is in the Allowed/Denied member list.</span></span> <span data-ttu-id="e3ec1-109">検索を行うユーザーが非公開のルームのメンバーではない場合は、非公開のルームは表示されません。</span><span class="sxs-lookup"><span data-stu-id="e3ec1-109">Secret rooms are not displayed unless the user who performs the search is a member of the secret room.</span></span> <span data-ttu-id="e3ec1-110">ユーザーは、自分が既にメンバーであるルームか、メンバーシップを要求することができるルームのみを検索できます。</span><span class="sxs-lookup"><span data-stu-id="e3ec1-110">The user can search only for rooms that he or she is already a member of, or those for which they can request membership.</span></span>



</div>

<span data-ttu-id="e3ec1-111">許可/拒否メンバーの概念の主な根拠は、倫理的な壁です。</span><span class="sxs-lookup"><span data-stu-id="e3ec1-111">The primary rationale for the concept of Allowed/Denied Members is ethical walls.</span></span> <span data-ttu-id="e3ec1-112">たとえば、銀行および金融機関では、ポリシーおよび規則を導入しながら、会社とアナリストが通信を共有することを防止する倫理的境界を備えていることがよくあります。</span><span class="sxs-lookup"><span data-stu-id="e3ec1-112">For example, it is common in banking and financial institutions to have ethical boundaries that prevent traders and analysts from sharing communications while implementing policies and conventions.</span></span> <span data-ttu-id="e3ec1-113">この要件に対処するために、管理者はカテゴリを作成できます。このようにすると、1つのカテゴリによって、自分が会議室を作成して使用できるようになり、他のカテゴリではアナリストによるルームの作成や使用が許可されます。</span><span class="sxs-lookup"><span data-stu-id="e3ec1-113">To address this requirement, an administrator can create categories so that one category allows rooms to be created and used by traders, and another category allows rooms to be created and used by analysts.</span></span> <span data-ttu-id="e3ec1-114">この制約がシステムで設計されている場合、親カテゴリによって禁止されている場合は、ユーザーをルームのメンバーとして追加することは禁じられています。</span><span class="sxs-lookup"><span data-stu-id="e3ec1-114">With this constraint is designed into the system prohibits adding a user as a member of the room if the parent category prevents it.</span></span>

<span data-ttu-id="e3ec1-115">次に、4つのユーザーロール常設チャットサーバーを示します。</span><span class="sxs-lookup"><span data-stu-id="e3ec1-115">Following are the four user roles Persistent Chat Server:</span></span>

  - <span data-ttu-id="e3ec1-116">**作成者:** チャットルームを作成する権限を持つユーザー。</span><span class="sxs-lookup"><span data-stu-id="e3ec1-116">**Creator:** Users who have permissions to create chat rooms.</span></span> <span data-ttu-id="e3ec1-117">これらのユーザーは、特定のカテゴリの作成者リストに含まれています。そのカテゴリでチャットルームを作成したり、カテゴリに従ってメンバーシップを割り当てたり、チャットルームを管理するために管理者を割り当てることもできます。</span><span class="sxs-lookup"><span data-stu-id="e3ec1-117">These users are in the Creators list of certain categories: they can create chat rooms in that category, and they can also assign membership according to the category, and assign managers to manage the chat room.</span></span> <span data-ttu-id="e3ec1-118">チャットルームを作成したユーザーは、ルームの管理者として自動的に追加されます。</span><span class="sxs-lookup"><span data-stu-id="e3ec1-118">The user who creates a chat room is automatically added as a manager of the room.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="e3ec1-p104">作成者は、チャット ルームを作成する権限があります。作成者は自動的に管理者に昇格し、作成したチャット サービスでメンバーシップ、管理者などを調整することもできます。</span><span class="sxs-lookup"><span data-stu-id="e3ec1-p104">Being a Creator simply provides rights for creating chat rooms. It is the automatic promotion to Manager that enables the Creator to further refine memberships, managers, and so on, on the created chat services.</span></span>

    
    </div>
    
    <span data-ttu-id="e3ec1-121">この役割は、組織内でチャット ルームの作成者を制御するためのものです。特に、ポリシーと指針を施行するためにチャット ルームの作成を集約的に管理する必要があり、その後、組織内のその他のユーザーにチャット ルーム管理を委任する場合です。</span><span class="sxs-lookup"><span data-stu-id="e3ec1-121">This role exists to give you the option of controlling who creates chat rooms in your organization, particularly if you want to centrally manage creating chat rooms to enforce policies and conventions, and subsequently delegate the chat room management to other users in the organization.</span></span>

  - <span data-ttu-id="e3ec1-122">**上司:** チャットルームのプロパティを管理するユーザー。</span><span class="sxs-lookup"><span data-stu-id="e3ec1-122">**Manager:** Users who manage properties of a chat room.</span></span> <span data-ttu-id="e3ec1-123">チャット ルームの管理者は、メンバー リストの変更 (メンバーの追加と削除) やチャット ルーム管理者リストの変更 (管理者の追加と削除) を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="e3ec1-123">Chat room managers can modify the member list (add and remove members), and modify the chat room managers list (add and remove managers).</span></span> <span data-ttu-id="e3ec1-124">チャット ルーム管理者は、自分がチャット ルームに参加できるように、(大会議室の) 発表者リストまたはメンバーに自分自身を追加できます。</span><span class="sxs-lookup"><span data-stu-id="e3ec1-124">Chat room managers can add themselves to the members or presenters list (for auditorium rooms) so they can participate in the chat room.</span></span> <span data-ttu-id="e3ec1-125">また、チャット ルーム管理者はチャット ルームを無効にできます (システム管理者は、無効にされたチャット ルームを検索して、それらを完全に削除できます)。</span><span class="sxs-lookup"><span data-stu-id="e3ec1-125">Chat room managers can also disable chat rooms (administrators can query for disabled chat rooms and can permanently delete them).</span></span> <span data-ttu-id="e3ec1-126">システム管理者は、チャット ルームのカテゴリ以外、チャット ルームのすべてのプロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="e3ec1-126">Managers can change all the properties of a chat room, except the category of the chat room.</span></span> <span data-ttu-id="e3ec1-127">チャットルームを作成した後は、常設チャット管理者のみがカテゴリを変更できます。</span><span class="sxs-lookup"><span data-stu-id="e3ec1-127">Only the Persistent Chat Administrator can change the category after the chat room has been created.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="e3ec1-128">ルーム管理者が、別のカテゴリの作成者でもある場合、カテゴリを、自分がルームを作成する権限があるカテゴリに変更できます。</span><span class="sxs-lookup"><span data-stu-id="e3ec1-128">If the manager is also a Creator in another category, he or she can change the category to one where they are authorized to create rooms.</span></span>

    
    </div>

  - <span data-ttu-id="e3ec1-129">**メンバー:** チャットルームのメンバーであるユーザー。</span><span class="sxs-lookup"><span data-stu-id="e3ec1-129">**Member:** Users who are members of a chat room.</span></span> <span data-ttu-id="e3ec1-130">メンバーは、ディレクトリ内のチャット ルームを見たり (非公開のチャット ルームでも可能)、チャット ルームを購読したり (未読メッセージ、エゴ フィルター、キーワード フィルターなどのメタデータ オプションを含む)、チャット ルームに参加したりできます (発表者のみがメッセージを投稿できるオーディオリアム チャット ルームでなければ、投稿もできます)。</span><span class="sxs-lookup"><span data-stu-id="e3ec1-130">These users can see the chat rooms in the directory (even if the chat room is secret), as well as subscribe to the chat room (including metadata options such as unread messages, ego filters, and keyword filters), and participate in the chat room (can post, unless the room is an auditorium room where only presenters can post, get content, and search).</span></span> <span data-ttu-id="e3ec1-131">チャット ルームのメンバーではないユーザーは、カテゴリの許可されたメンバー リストに入っていれば、チャット ルームを検索することはできますが、コンテンツにアクセスするにはチャット ルームへの参加を要求する必要があります (システムにはアクセスの要求または承認の機能はありません。</span><span class="sxs-lookup"><span data-stu-id="e3ec1-131">Users who aren’t members of the chat room can search for the chat room if they are in the Allowed Members list of the category, but need to request access to join these chat rooms to access content.</span></span> <span data-ttu-id="e3ec1-132">電子メール、電話、他の手段で外部的に行う必要があります)。</span><span class="sxs-lookup"><span data-stu-id="e3ec1-132">(There is no request access or approvals built into the system; these are done externally by email, phone, or other forms of contact.)</span></span>

  - <span data-ttu-id="e3ec1-133">**プレゼンター:** 聴衆会議室に投稿できるユーザー。</span><span class="sxs-lookup"><span data-stu-id="e3ec1-133">**Presenter:** Users who can post to an auditorium room.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="e3ec1-134">常設チャットサーバーを使用すると、ユーザーは特定のサイトのチャットルームを作成して管理することができます。</span><span class="sxs-lookup"><span data-stu-id="e3ec1-134">Persistent Chat Server lets users create and manage chat room for a specific site.</span></span> <span data-ttu-id="e3ec1-135">ただし、ユーザーは同じトポロジ内の他のサイトのチャットルームを作成または管理することはできません。</span><span class="sxs-lookup"><span data-stu-id="e3ec1-135">Users cannot, however, create or manage chat rooms on other sites within the same topology.</span></span> <span data-ttu-id="e3ec1-136">組織内のすべてのサイトについて、必ずチャットルームの作成者と管理者を指定してください。</span><span class="sxs-lookup"><span data-stu-id="e3ec1-136">Be sure to specify chat room Creators and Managers for all the sites in your organization.</span></span>



</div>

<span data-ttu-id="e3ec1-137">次の役割は、常設チャットサーバーの管理者ロールです。</span><span class="sxs-lookup"><span data-stu-id="e3ec1-137">The following roles are administrator roles for Persistent Chat Server:</span></span>

  - <span data-ttu-id="e3ec1-138">**常設チャット管理者 (CsPersistentChatAdministrator):** これは、常設チャットサーバーの管理と管理のための新しい Role-Based アクセス制御 (RBAC) 役割です。</span><span class="sxs-lookup"><span data-stu-id="e3ec1-138">**Persistent Chat Administrator (CsPersistentChatAdministrator):** This is a new Role-Based Access Control (RBAC) role to administer and manage Persistent Chat Server.</span></span> <span data-ttu-id="e3ec1-139">CsPersistentChatAdministrator として指定されたユーザーまたはセキュリティグループは、Windows PowerShell コマンドレットをリモートで (つまり、常設チャットサーバー以外のコンピューターから) 使用して、常設チャットサーバーを管理することができます。</span><span class="sxs-lookup"><span data-stu-id="e3ec1-139">Users or security groups designated as CsPersistentChatAdministrator are able administer Persistent Chat Server by using Windows PowerShell cmdlets remotely (that is, from a computer other than the Persistent Chat Server).</span></span> <span data-ttu-id="e3ec1-140">常設チャットサーバーは、常設チャットの管理者が常設チャットサーバーのフロントエンドサーバーの RTC ローカル管理者ローカルグループのメンバーであることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e3ec1-140">Persistent Chat Server checks that the Persistent Chat Administrator is member of the RTC Local administrator local group on the Persistent Chat Server Front End Server.</span></span>
    
    <span data-ttu-id="e3ec1-141">CsPersistentChatAdministrator role では、チャットルームの管理 (メンバーシップ、マネージャー、カテゴリを含むすべてのプロパティの変更、ルームを無効としてマークするなど)、チャットルームの作成とアクセスを許可するユーザーを定義するチャットルームカテゴリの作成と管理を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="e3ec1-141">The CsPersistentChatAdministrator role can manage chat rooms (modify all properties including membership, managers, categories, mark rooms as disabled), as well as create and manage chat room categories that define who can create and access chat rooms.</span></span> <span data-ttu-id="e3ec1-142">Administrators can also mark chat rooms as disabled and clean up chat rooms that are no longer active.</span><span class="sxs-lookup"><span data-stu-id="e3ec1-142">Administrators can also mark chat rooms as disabled and clean up chat rooms that are no longer active.</span></span> <span data-ttu-id="e3ec1-143">Administrators are not subject to the Creators or Allowed Members restrictions.</span><span class="sxs-lookup"><span data-stu-id="e3ec1-143">Administrators are not subject to the Creators or Allowed Members restrictions.</span></span> <span data-ttu-id="e3ec1-144">Administrators can create any kind of chat room and add themselves as a member to any chat room.</span><span class="sxs-lookup"><span data-stu-id="e3ec1-144">Administrators can create any kind of chat room and add themselves as a member to any chat room.</span></span> <span data-ttu-id="e3ec1-145">管理者は、常設チャットの構成を変更して管理することもできます (プールのプロパティ、グローバル設定、コンプライアンス構成)。また、古いグループチャットサーバーの展開から Lync Server 2013 常設チャットサーバーへの移行を計画して実装することもできます。</span><span class="sxs-lookup"><span data-stu-id="e3ec1-145">Administrators can also modify and manage Persistent Chat configuration (pool properties, global settings, and compliance configuration) and can also plan and implement migration from an older Group Chat Server deployment to Lync Server 2013 Persistent Chat Server.</span></span>

  - <span data-ttu-id="e3ec1-146">**Lync 管理者:** 展開担当の Lync Server 2013 の全体的なエンタープライズ管理者。</span><span class="sxs-lookup"><span data-stu-id="e3ec1-146">**Lync Administrator:** Overall enterprise administrator for Lync Server 2013 responsible for deployment.</span></span>

  - <span data-ttu-id="e3ec1-147">**Operations Manager:** 日常的な操作の管理を担当するユーザー。</span><span class="sxs-lookup"><span data-stu-id="e3ec1-147">**Operations Manager:** User responsible for managing day-to-day operations.</span></span>

  - <span data-ttu-id="e3ec1-148">**サードパーティの開発者とパートナー:** サードパーティの開発者は、システムを拡張します。特に、グループ会話、コンプライアンスサポートとツール、web/モバイルクライアント、ボット開発のフレームワークには、倫理的な壁ソリューションが用意されています。</span><span class="sxs-lookup"><span data-stu-id="e3ec1-148">**Third-party developers and partners:** Third-party developers extend the system, in particular providing an ethical wall solution for group conversations, compliance support and tools, web/mobile clients, and a framework for Bot development.</span></span>

<span data-ttu-id="e3ec1-149"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e3ec1-149"></div>

<span> </span>

</div>

</div>

</span></span></div>

