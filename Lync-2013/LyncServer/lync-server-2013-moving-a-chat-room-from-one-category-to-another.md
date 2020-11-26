---
title: 'Lync Server 2013: 1 つのカテゴリから他のカテゴリへのチャット ルームの移動'
description: 'Lync Server 2013: チャットルームを別のカテゴリに移動する。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Moving a chat room from one category to another
ms:assetid: 7e93b8f6-5a18-4476-a432-3918e01bcfa6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ215877(v=OCS.15)
ms:contentKeyID: 48706004
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4066732a90a94414b55d6a567fde0d496e4faf13
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425270"
---
# <a name="moving-a-chat-room-from-one-category-to-another-in-lync-server-2013"></a><span data-ttu-id="5d1db-103">Lync Server 2013 での 1 つのカテゴリから他のカテゴリへのチャット ルームの移動</span><span class="sxs-lookup"><span data-stu-id="5d1db-103">Moving a chat room from one category to another in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5d1db-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5d1db-104">

<span> </span></span></span>

<span data-ttu-id="5d1db-105">_**最終更新日:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="5d1db-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="5d1db-106">チャットルームの作成後は、常設チャットルームのカテゴリを変更しないことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="5d1db-106">We recommend that you do not change the category of a Persistent Chat room after the chat room is created.</span></span> <span data-ttu-id="5d1db-107">ただし、チャットルームマネージャーが別のカテゴリで **Creator** 権限を持っている場合は、そのカテゴリから別のカテゴリにルームを移動することができます。</span><span class="sxs-lookup"><span data-stu-id="5d1db-107">However, if the chat room manager has **Creator** privileges in another category, he or she can move the room from one category to another.</span></span> <span data-ttu-id="5d1db-108">会議室は削除されず、再び作成されることはありません。</span><span class="sxs-lookup"><span data-stu-id="5d1db-108">The room is not deleted and recreated.</span></span> <span data-ttu-id="5d1db-109">データベース内の関連付けの変更です。</span><span class="sxs-lookup"><span data-stu-id="5d1db-109">It is a change of association within the database.</span></span>

<span data-ttu-id="5d1db-110">チャットルームのカテゴリを変更することはめったにありません。</span><span class="sxs-lookup"><span data-stu-id="5d1db-110">Changing a chat room category should be done rarely.</span></span> <span data-ttu-id="5d1db-111">カテゴリはチャット ルームの許可されるメンバーシップを決定するので、チャット ルームを別のカテゴリに移動すると、新しいカテゴリでサポートされなくなったシステム アクセス制御リスト (SACL) は削除されます。</span><span class="sxs-lookup"><span data-stu-id="5d1db-111">A category determines the allowed membership for the chat room, so when a chat room is moved to another category, all the system access control lists (SACLs) that are no longer supported by the new category are purged.</span></span> <span data-ttu-id="5d1db-112">たとえば、ユーザーが会議室のメンバーであり、新しいカテゴリの **Allowedmember** ではなくなった場合、会議室のメンバーシップが変更され、ユーザーはルームから削除されます。</span><span class="sxs-lookup"><span data-stu-id="5d1db-112">For example, if a user was a member of the room and is no longer an **AllowedMember** in the new category, the room membership will be modified and the user will be removed from the room.</span></span>

<span data-ttu-id="5d1db-113">Windows PowerShell コマンドラインインターフェイスを使用してチャットルームを移動する方法について詳しくは、「 [Windows powershell コマンドレットを使用して常設チャットサーバーを構成](configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md)する」の「会議室の管理」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="5d1db-113">For details about moving a chat room by using the Windows PowerShell command-line interface, see "Room Management" in [Configuring Persistent Chat Server by using Windows PowerShell cmdlets](configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md).</span></span>

<span data-ttu-id="5d1db-114">チャットルームの設定の詳細については、展開ドキュメントの「 [Lync Server 2013 で会議室を構成](lync-server-2013-configure-rooms.md) する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5d1db-114">For details about configuring chat rooms, see [Configure rooms in Lync Server 2013](lync-server-2013-configure-rooms.md) in the Deployment documentation.</span></span>

<span data-ttu-id="5d1db-115"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5d1db-115"></div>

<span> </span>

</div>

</div>

</span></span></div>

