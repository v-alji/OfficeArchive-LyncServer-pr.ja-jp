---
title: 常設チャット サーバーのベスト プラクティス
description: 常設チャットサーバーのベストプラクティス。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Persistent Chat Server best practices
ms:assetid: dc18e7f7-599b-4d32-abf7-cd9e691426a2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398970(v=OCS.15)
ms:contentKeyID: 48185612
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5c575c0afa0366e88748eadfcf4c04fccb20b375
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438786"
---
# <a name="persistent-chat-server-best-practices"></a><span data-ttu-id="b1872-103">常設チャット サーバーのベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="b1872-103">Persistent Chat Server best practices</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b1872-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b1872-104">

<span> </span></span></span>

<span data-ttu-id="b1872-105">_**最終更新日:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="b1872-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="b1872-106">カテゴリと常設チャットルームを作成して、スコープとメンバーシップを設計する際には、次のヒントを参考にしてください。</span><span class="sxs-lookup"><span data-stu-id="b1872-106">As you create your categories and Persistent Chat rooms and design your scoping and membership, the following tips can help your planning:</span></span>

  - <span data-ttu-id="b1872-107">会社が倫理的な壁を必要としない場合は、カテゴリツリーの範囲を狭くしないでください。</span><span class="sxs-lookup"><span data-stu-id="b1872-107">If your company does not require an ethical wall, do not narrow the scope in your category tree.</span></span> <span data-ttu-id="b1872-108">すべてのユーザーを1つのカテゴリの範囲に入れ、そのカテゴリのすべてのチャットルームを作成します。</span><span class="sxs-lookup"><span data-stu-id="b1872-108">Put all your users in the scope of one category, and create all chat rooms in that category.</span></span> <span data-ttu-id="b1872-109">その後、メンバーシップリストを使用して、各チャットルームへのアクセスを許可または制限します。</span><span class="sxs-lookup"><span data-stu-id="b1872-109">Subsequently, use only membership lists to grant or restrict access to each chat room.</span></span>

  - <span data-ttu-id="b1872-110">ほとんどの場合、新しいトピックに関するディスカッションをいつでも開始できるように、ユーザーが新しいチャットルームを作成できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1872-110">In most cases, you should enable users to create new chat rooms so that discussions about new topics can be started any time.</span></span> <span data-ttu-id="b1872-111">これを行うには **、作成者リストを** **allowedmembers** リストと同じにします。</span><span class="sxs-lookup"><span data-stu-id="b1872-111">Do this by making the **Creators** list the same as the **AllowedMembers** list.</span></span> <span data-ttu-id="b1872-112">ただし、中央のサポートチームまたは特定のユーザーにのみ会議室の作成を許可する場合は、適切なサブセットとして作成者 **の一覧を** 作成します。</span><span class="sxs-lookup"><span data-stu-id="b1872-112">However, if you want to allow only a central support team or designated users to create rooms, then make the **Creators** list as the appropriate subset.</span></span>

  - <span data-ttu-id="b1872-113">各チャットルームには、組織に適した場所を示す完全な名前と説明の概要を指定します。</span><span class="sxs-lookup"><span data-stu-id="b1872-113">Give each chat room a complete name and description summary that describes where it fits in with your organization.</span></span> <span data-ttu-id="b1872-114">ユーザーは、チャットルームを使用するときにカテゴリ名を見ることができないため、ユーザーがチャットルームの目的のディスカッションフォーラムを特定するのに役立つように、カテゴリ名を利用することはできません。</span><span class="sxs-lookup"><span data-stu-id="b1872-114">Because users cannot see the category name when they use the chat room, you cannot rely on the category name to help users determine the intended discussion forum for the chat room.</span></span>

  - <span data-ttu-id="b1872-115">特定の命名規則やその他のアクセス制御や検証を実装する場合は、カスタムの会議室の作成ワークフローが必要になることがあります。</span><span class="sxs-lookup"><span data-stu-id="b1872-115">You may want to have a custom room creation workflow if you have certain naming conventions or other access controls or validations to implement.</span></span> <span data-ttu-id="b1872-116">常設チャットの構成では、ホストしているものに **RoomManagementUrl** をカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="b1872-116">The Persistent Chat configuration enables you to customize the **RoomManagementUrl** to something that you host.</span></span> <span data-ttu-id="b1872-117">たとえば、ユーザーが Lync クライアントで [ **会議室の作成** ] をクリックすると、ユーザーはカスタムソリューションにリダイレクトすることができます。</span><span class="sxs-lookup"><span data-stu-id="b1872-117">For example, when users click **Create a room** in their Lync client, they can be redirected to your custom solution.</span></span>

  - <span data-ttu-id="b1872-118">他のビジネスデータをチャットルームに表示して、チャットルームの操作性を向上させるためのさまざまなアドインを作成します。</span><span class="sxs-lookup"><span data-stu-id="b1872-118">Create a variety of add-ins that help to enhance the experience of chat rooms by bringing in other business data into chat rooms.</span></span> <span data-ttu-id="b1872-119">管理者は、システムに許可するアドインを登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1872-119">Administrators must register the add-ins that they want to allow in the system.</span></span> <span data-ttu-id="b1872-120">チャットルームマネージャーと作成者は、それぞれの会議室に最も関連性の高いアドインの一覧から選ぶことができます。</span><span class="sxs-lookup"><span data-stu-id="b1872-120">Chat room managers and creators can choose from the list of allowed add-ins for the ones most relevant to their respective rooms.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="b1872-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="b1872-121">See Also</span></span>


[<span data-ttu-id="b1872-122">Lync Server 2013 でのカテゴリ、ルーム、およびアドインの管理</span><span class="sxs-lookup"><span data-stu-id="b1872-122">Managing categories, rooms, and add-ins in Lync Server 2013</span></span>](lync-server-2013-managing-categories-rooms-and-add-ins.md)  
  

<span data-ttu-id="b1872-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b1872-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

