---
title: 'Lync Server 2013: ユーザーおよびユーザー グループのドメインをルーム カテゴリへ追加する'
description: 'Lync Server 2013: ユーザーとユーザーグループのドメインを会議室カテゴリに追加します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Adding domains of users and user groups to the room category
ms:assetid: ee03f2cf-1c84-41c4-b524-d0729be33b8c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ215884(v=OCS.15)
ms:contentKeyID: 48706013
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 196a795547d5caa6dfd1732c3d6b4630ef79438a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439213"
---
# <a name="adding-domains-of-users-and-user-groups-to-the-room-category-in-lync-server-2013"></a><span data-ttu-id="bc692-103">Lync Server 2013 でユーザーおよびユーザー グループのドメインをルーム カテゴリへ追加する</span><span class="sxs-lookup"><span data-stu-id="bc692-103">Adding domains of users and user groups to the room category in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bc692-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bc692-104">

<span> </span></span></span>

<span data-ttu-id="bc692-105">_**最終更新日:** 2014-02-07_</span><span class="sxs-lookup"><span data-stu-id="bc692-105">_**Topic Last Modified:** 2014-02-07_</span></span>

<span data-ttu-id="bc692-106">より大きなユーザーグループをチャットルームに追加する方法については、「 [Lync Server 2013 でカテゴリを構成](lync-server-2013-configure-categories.md) する」および「展開ドキュメントの [カテゴリを管理](manage-categories.md) する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bc692-106">To add larger groups of users to a chat room, see [Configure categories in Lync Server 2013](lync-server-2013-configure-categories.md) and [Manage categories](manage-categories.md) in the Deployment documentation.</span></span> <span data-ttu-id="bc692-107">たとえば、次のコマンドは、active Directory の NorthAmericaUsers OU のすべてのユーザーを NorthAmerica チャットルームに追加します。</span><span class="sxs-lookup"><span data-stu-id="bc692-107">For example, this command adds all the users from the NorthAmericaUsers OU in active Directory to the NorthAmerica chat room:</span></span>

    Set-CsPersistentChatRoom -PersistentChatPoolFqdn "atl-cs-001.litwareinc.com\NorthAmerica" -Members @{Add="OU=NorthAmericaUsers,DC=litwareinc,DC=com"}

<span data-ttu-id="bc692-108">このコマンドを実行すると、すべてのメンバーが財務配布グループから同じチャットルームに追加されます。</span><span class="sxs-lookup"><span data-stu-id="bc692-108">His command adds all the members from the Finance distribution group to the same chat room:</span></span>

    Set-CsPersistentChatRoom -PersistentChatPoolFqdn "atl-cs-001.litwareinc.com\NorthAmerica" -Members @{Add="CN=Finance,OU=ExternalUsers,DC=litwareinc,DC=com"}

<span data-ttu-id="bc692-109"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bc692-109"></div>

<span> </span>

</div>

</div>

</span></span></div>

