---
title: 常設チャットのメンバーシップについて
description: 常設チャットのメンバーシップについて。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Understanding Persistent Chat membership
ms:assetid: 900392d6-6e9f-4dae-93d6-39d7474409ef
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398730(v=OCS.15)
ms:contentKeyID: 48184781
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 63e0d26ea56552d8906ab9a5cf216a7026868017
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398889"
---
# <a name="understanding-persistent-chat-membership"></a><span data-ttu-id="206f9-103">常設チャットのメンバーシップについて</span><span class="sxs-lookup"><span data-stu-id="206f9-103">Understanding Persistent Chat membership</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="206f9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="206f9-104">

<span> </span></span></span>

<span data-ttu-id="206f9-105">_**最終更新日:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="206f9-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="206f9-106">常設チャットルームへのユーザーアクセスは、メンバーシップによって管理されます。ユーザーは、メッセージを投稿して読むことができるように、チャットルームのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="206f9-106">User access to Persistent Chat rooms is managed by membership; users must be members of a chat room to be able to post and read messages.</span></span> <span data-ttu-id="206f9-107">チャットルームに指定された所属を持っている **発表** 者のみが、 **会議室への投稿** を使用できます。</span><span class="sxs-lookup"><span data-stu-id="206f9-107">Only **Presenters** who have a designated affiliation with chat rooms are allowed to use **Posting to Auditorium rooms**.</span></span> <span data-ttu-id="206f9-108">聴衆はチャットルームの一種 (もう1つは [ **通常**]) であり、発表者のみが投稿でき、全員が読むことができます。</span><span class="sxs-lookup"><span data-stu-id="206f9-108">An auditorium is a type of chat room (the other is **Normal**), where only Presenters can post and everyone can read.</span></span>

<span data-ttu-id="206f9-109">さらに、固定チャットルームは、カテゴリのルールの下でも動作します。</span><span class="sxs-lookup"><span data-stu-id="206f9-109">In addition, Persistent Chat rooms operate under the rules of a category.</span></span> <span data-ttu-id="206f9-110">カテゴリの詳細については、このトピックで後述する「 [Lync Server 2013 でカテゴリ、会議室、アドインを管理](lync-server-2013-managing-categories-rooms-and-add-ins.md)する」と「カテゴリのスコーピングのしくみ」と「会議室のカテゴリの戦略」のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="206f9-110">For details about categories, see [Managing categories, rooms, and add-ins in Lync Server 2013](lync-server-2013-managing-categories-rooms-and-add-ins.md), and also the sections "How Category Scoping Works" and "Room Category Strategies" later in this topic.</span></span>

<span data-ttu-id="206f9-111">常設チャット管理者は、チャットルームのカテゴリを作成して管理することができます。</span><span class="sxs-lookup"><span data-stu-id="206f9-111">A Persistent Chat administrator can create and manage chat room categories.</span></span> <span data-ttu-id="206f9-112">チャットルームのカテゴリの作成と管理の一環として、常設チャット管理者は、特定のカテゴリのチャットルームのメンバーまたは作成者としてアクセスできるプリンシパル (Active Directory ドメインサービスのグループ、コンテナー、ユーザー) を構成することができます。</span><span class="sxs-lookup"><span data-stu-id="206f9-112">As part of creating and managing chat room categories, the Persistent Chat administrator can configure principals (Active Directory Domain Services groups, containers, and users) that have access to be members or creators of chat rooms of a particular category.</span></span>

<div>

## <a name="active-directory-domain-services-and-persistent-chat"></a><span data-ttu-id="206f9-113">Active Directory ドメインサービスと常設チャット</span><span class="sxs-lookup"><span data-stu-id="206f9-113">Active Directory Domain Services and Persistent Chat</span></span>

<span data-ttu-id="206f9-114">常設チャットサーバーは、内部の常設チャットユーザーのプールに Active Directory を使用します。</span><span class="sxs-lookup"><span data-stu-id="206f9-114">Persistent Chat Server relies on Active Directory for the pool of internal Persistent Chat users.</span></span> <span data-ttu-id="206f9-115">常設チャット (クライアント) をインストールすると、ユーザーとユーザーグループのドメインを会議室カテゴリに追加することができます。</span><span class="sxs-lookup"><span data-stu-id="206f9-115">After you install Persistent Chat (client), you can add domains of users and user groups to the room category.</span></span> <span data-ttu-id="206f9-116">次に、これらのユーザーやグループを会議室のカテゴリのメンバーシップに追加することができます。</span><span class="sxs-lookup"><span data-stu-id="206f9-116">You can then add these users and groups to the membership of your room categories.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="206f9-117">常設チャットルームを変更するユーザーには、重複した名前がないことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="206f9-117">You must ensure that there are no duplicate names for users who want to make changes to their Persistent Chat room(s).</span></span> <span data-ttu-id="206f9-118">重複したユーザー名が存在する場合は、別の名前に変更して、ユーザーがこれらの変更を行うのをブロックします。</span><span class="sxs-lookup"><span data-stu-id="206f9-118">If duplicate user names exist, change them to different names to unblock users from making those changes.</span></span> <span data-ttu-id="206f9-119">Active Directory で名前が重複していて、そのユーザーの会議室での変更を試みると、エラーメッセージが表示され、ユーザーに管理者に連絡して解決を求めます。</span><span class="sxs-lookup"><span data-stu-id="206f9-119">If a user has duplicate names in Active Directory and tries to make changes in their room(s), an error message appears prompting the user to contact the administrator for resolution.</span></span>



</div>

</div>

<div>

## <a name="how-category-scoping-works"></a><span data-ttu-id="206f9-120">カテゴリのスコーピングのしくみ</span><span class="sxs-lookup"><span data-stu-id="206f9-120">How Category Scoping Works</span></span>

<span data-ttu-id="206f9-121">カテゴリは、 **Allowedmembers** プロパティに基づいて、そのカテゴリの常設チャットルームのメンバーシップリストのメンバーになることができるすべてのユーザーとグループを指定します。</span><span class="sxs-lookup"><span data-stu-id="206f9-121">A category specifies all the users and groups that can be members in a membership list of a Persistent Chat room in that category, based on its **AllowedMembers** property.</span></span> <span data-ttu-id="206f9-122">たとえば、カテゴリの **allowedmembers** を contoso.com に設定した場合、 *contoso* の任意のグループまたはユーザーをメンバーとしてそのカテゴリのチャットルームに追加することができます。</span><span class="sxs-lookup"><span data-stu-id="206f9-122">For example, if you set the category’s **AllowedMembers** to contoso.com, you can add any group or user at *Contoso* as a member to chat rooms in that category.</span></span> <span data-ttu-id="206f9-123">カテゴリの **Allowedmembers** を [ *Sales*] に設定した場合、この配布リストのグループとユーザーのみがそのカテゴリのチャットルームにメンバーとして追加できます。</span><span class="sxs-lookup"><span data-stu-id="206f9-123">If you set the **AllowedMembers** on a category to *Sales*, only groups and users in this distribution list can be added as members to chat rooms in that category.</span></span> <span data-ttu-id="206f9-124">同様に、作成 **者プロパティによって、** そのカテゴリでチャットルームを作成できるユーザーを制御することができます。</span><span class="sxs-lookup"><span data-stu-id="206f9-124">Similarly, the **Creators** property enables you to control who can create chat rooms in that category.</span></span> <span data-ttu-id="206f9-125">チャットルームが作成されると、 **Allowedmembers** グループのメンバーを管理 **者** として指定して、ルームでの継続的な管理操作 (メンバーシップの変更や承認など) を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="206f9-125">After the chat room is created, anyone from the **AllowedMembers** group can be designated as a **Manager** for ongoing management operations on the rooms (for example, membership changes and approvals).</span></span>

<span data-ttu-id="206f9-126">**Allowedmembers** と category の作成者の **定義には**、次の利点があります。</span><span class="sxs-lookup"><span data-stu-id="206f9-126">Defining **AllowedMembers** and **Creators** for a category has the following benefits:</span></span>

  - <span data-ttu-id="206f9-127">カテゴリ内のすべてのチャット ルームがカテゴリ レベルの制限のセットにバインドされます。</span><span class="sxs-lookup"><span data-stu-id="206f9-127">All chat rooms in this category are bound by the restrictions set at the category level.</span></span> <span data-ttu-id="206f9-128">これにより、業務ニーズとアクセス ポリシーに基づいてチャット ルームを分離できます。</span><span class="sxs-lookup"><span data-stu-id="206f9-128">You can use this to segregate chat rooms based on business need and access policies.</span></span>

  - <span data-ttu-id="206f9-129">作成 **者リストに含まれている** ユーザーは、そのカテゴリで新しいチャットルームを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="206f9-129">A user who is in the **Creators** list can create new chat rooms in that category.</span></span> <span data-ttu-id="206f9-130">組織内のユーザーの制限された人数でチャットルームを作成できるシステムを実装する場合は、このコントロールを使用してその要件を満たすことができます。</span><span class="sxs-lookup"><span data-stu-id="206f9-130">If you want to implement a system where a restricted number of personnel in the organization can create chat rooms, this control can be used to meet that requirement.</span></span>

</div>

<div>

## <a name="room-category-strategies"></a><span data-ttu-id="206f9-131">会議室のカテゴリ戦略</span><span class="sxs-lookup"><span data-stu-id="206f9-131">Room Category Strategies</span></span>

<span data-ttu-id="206f9-132">カテゴリの **Allowedmembers** には、このカテゴリの常設チャットルームを使用するすべてのユーザーが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="206f9-132">A category’s **AllowedMembers** must include all users who will use any Persistent Chat room in this category.</span></span> <span data-ttu-id="206f9-133">ビジネスデータを保護し、適切なレベルのアクセスを確保するための要件に応じて、1つ以上のカテゴリを定義して、ルームに検索して参加できるユーザーを指定することができます。</span><span class="sxs-lookup"><span data-stu-id="206f9-133">Depending on your requirements to protect business data and ensure the appropriate level of access, you may want to define one or more categories to specify who can search and participate in rooms.</span></span> <span data-ttu-id="206f9-134">特定のユーザーのセット (中央のヘルプデスクまたはフルタイムの従業員のみ) に対して会議室の作成を許可する場合は、その要件を満たすように、 **カテゴリの作成** 者のスコープを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="206f9-134">If you want to allow only a particular set of users (a central helpdesk, or only full-time employees) to create rooms, you can scope the **Creators** of a category to satisfy that requirement.</span></span>

<span data-ttu-id="206f9-135">分類項目を使用して、倫理的でない壁を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="206f9-135">Categories can also be used to create ethical walls.</span></span> <span data-ttu-id="206f9-136">倫理的な壁によって、組織内での利益の競合を防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="206f9-136">Ethical walls prevent any conflict of interest in an organization.</span></span> <span data-ttu-id="206f9-137">たとえば、管理者は、自分専用のカテゴリでチャットルームを作成できますが、他のカテゴリのチャットルームはアナリストのみが使用できます。</span><span class="sxs-lookup"><span data-stu-id="206f9-137">For example, an administrator can create chat rooms in a category for traders only, whereas chat rooms in another category can be used by analysts only.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="206f9-138">Lync Server 2013 の常設チャットサーバーでは、フェデレーションユーザーへのアクセスはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="206f9-138">In Lync Server 2013, Persistent Chat Server, we do not support access to federated users.</span></span> <span data-ttu-id="206f9-139">以前のバージョンの常設チャットサーバーでフェデレーションされたユーザーからチャットがある場合は、チャットが移行されます。</span><span class="sxs-lookup"><span data-stu-id="206f9-139">If there are chats from federated users in previous versions of Persistent Chat Server, they will be migrated.</span></span> <span data-ttu-id="206f9-140">フェデレーションされたユーザーは、無効なプリンシパルとして追加されます。</span><span class="sxs-lookup"><span data-stu-id="206f9-140">The federated users are added as disabled principals.</span></span>



</div>

</div>

<div>

## <a name="narrowing-the-members-to-user-groups"></a><span data-ttu-id="206f9-141">メンバーをユーザーグループに絞り込む</span><span class="sxs-lookup"><span data-stu-id="206f9-141">Narrowing the Members to User Groups</span></span>

<span data-ttu-id="206f9-142">カテゴリにドメインを追加すると、そのドメインにグループオブジェクトが含まれているユーザーグループが利用できるようになり、そのカテゴリの会議室のメンバーとして指定することができます。</span><span class="sxs-lookup"><span data-stu-id="206f9-142">When you add a domain to a category, the user groups whose group objects are contained in that domain are available to you so that you can specify them as members of rooms in that category.</span></span>

<span data-ttu-id="206f9-143">カテゴリの **Allowedmembers** と **クリエーター** の定義には、ドメインや組織単位などの Active Directory コンテナーの使用をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="206f9-143">We recommend, as a general rule, that you use Active Directory containers, such as domains and organizational units, for defining a category’s **AllowedMembers** and **Creators**.</span></span> <span data-ttu-id="206f9-144">任意のドメインから、 **Allowedmembers** または **クリエーター** リストにオブジェクトを追加できます。</span><span class="sxs-lookup"><span data-stu-id="206f9-144">You can add objects from any domain to an **AllowedMembers** or **Creators** list.</span></span> <span data-ttu-id="206f9-145">このカテゴリの下にあるルームに追加できる **のは、** **allowedmembers** または作成者リスト内のオブジェクトのみです。</span><span class="sxs-lookup"><span data-stu-id="206f9-145">Only objects within the **AllowedMembers** or **Creators** list can be added to rooms under that category.</span></span>

<span data-ttu-id="206f9-146"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="206f9-146"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

