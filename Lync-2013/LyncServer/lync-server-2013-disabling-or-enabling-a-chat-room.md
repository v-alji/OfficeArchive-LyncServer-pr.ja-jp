---
title: 'Lync Server 2013: チャット ルームの無効化または有効化'
description: 'Lync Server 2013: チャットルームの無効化または有効化。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Disabling or enabling a chat room
ms:assetid: db0908fc-aae3-46e8-bc0b-245e9adfa1e2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ215883(v=OCS.15)
ms:contentKeyID: 48706011
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9b81ce2614cebcf554c0390369068d8fd8b8f932
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437848"
---
# <a name="disabling-or-enabling-a-chat-room-in-lync-server-2013"></a><span data-ttu-id="8787a-103">Lync Server 2013 でのチャット ルームの無効化または有効化</span><span class="sxs-lookup"><span data-stu-id="8787a-103">Disabling or enabling a chat room in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8787a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8787a-104">

<span> </span></span></span>

<span data-ttu-id="8787a-105">_**最終更新日:** 2014-02-05_</span><span class="sxs-lookup"><span data-stu-id="8787a-105">_**Topic Last Modified:** 2014-02-05_</span></span>

<span data-ttu-id="8787a-106">常設チャットルームのトピックが不要になった場合は、そのチャットルームを無効にしてユーザーが利用できないようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="8787a-106">If the topic of a Persistent Chat room is no longer relevant, you can make the chat room unavailable to users by disabling it.</span></span> <span data-ttu-id="8787a-107">チャット ルームを無効にすると、すべてのメンバーがチャット ルームから即座に切断されます。</span><span class="sxs-lookup"><span data-stu-id="8787a-107">When a chat room is disabled, all members are immediately disconnected from the room.</span></span> <span data-ttu-id="8787a-108">チャット ルームを無効にした後、ユーザーは、そのチャット ルームに再び参加することも、チャット ルームを検索することもできません。</span><span class="sxs-lookup"><span data-stu-id="8787a-108">After a chat room is disabled, users cannot rejoin it or find it in chat room searches.</span></span>

<span data-ttu-id="8787a-109">無効になったチャットルームは、常設チャット管理者が後で有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="8787a-109">A disabled chat room can be enabled later by a Persistent Chat administrator.</span></span> <span data-ttu-id="8787a-110">チャットルームを無効にすると、そのメンバーのメンバーシップリストとその他の設定が保持されます。</span><span class="sxs-lookup"><span data-stu-id="8787a-110">If a chat room is disabled, its membership list and other settings are preserved.</span></span> <span data-ttu-id="8787a-111">もう一度会議室を有効にした場合は、手動で設定を再作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="8787a-111">If you enable the room again, you do not need to manually re-create the settings.</span></span>

<span data-ttu-id="8787a-112">チャットルームの履歴が残っている場合 (チャットルームの履歴の保存は、カテゴリ内のすべての会議室に適用されるカテゴリのオプションの設定です。既定では、固定されていますが、カテゴリの [ **チャット履歴** を無効にする] に設定することでオフにすることができます)。</span><span class="sxs-lookup"><span data-stu-id="8787a-112">If the chat room’s history persists (chat room history persistence is an optional setting on a category that applies to all rooms within the category; the default is that it is persisted, but can be turned off by setting the category’s **Enable Chat History** to false), the content is preserved when the chat room is disabled.</span></span> <span data-ttu-id="8787a-113">ただし、チャット ルームが無効になっている間、コンテンツは検索に表示されません。</span><span class="sxs-lookup"><span data-stu-id="8787a-113">However, that content will not appear in searches during the time that the chat room remains in a disabled state.</span></span> <span data-ttu-id="8787a-114">チャット ルームを後で有効にすると、ユーザーは、チャット ルームが無効になる前に投稿されたメッセージを検索できます。</span><span class="sxs-lookup"><span data-stu-id="8787a-114">If you later enable the chat room, users can search for messages that were posted before the chat room was disabled.</span></span>

<span data-ttu-id="8787a-115">Windows PowerShell コマンドラインインターフェイスを使用してチャットルームを無効にして有効にする方法について詳しくは、「 [Windows powershell コマンドレットを使用して常設チャットサーバーを構成](configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md)する」の「会議室の管理」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="8787a-115">For details about disabling and enabling chat rooms by using the Windows PowerShell command-line interface, see "Room Management" in [Configuring Persistent Chat Server by using Windows PowerShell cmdlets](configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md).</span></span> <span data-ttu-id="8787a-116">チャットルームを無効にするには、次のようなコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="8787a-116">To disable a chat room, use a command similar to this:</span></span>

    Set-CsPersistentChatRoom -Identity "atl-cs-001.litwareinc.com\ITChatRoom" -Disabled $True

<span data-ttu-id="8787a-117">チャットルームを有効にするには、Disabled プロパティを False に設定します。</span><span class="sxs-lookup"><span data-stu-id="8787a-117">To enabled a chat room, set the Disabled property to False:</span></span>

    Set-CsPersistentChatRoom -Identity "atl-cs-001.litwareinc.com\ITChatRoom" -Disabled $False

<span data-ttu-id="8787a-118">Lync Server コントロールパネルを使用して、チャットルームを有効または無効にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="8787a-118">Note that chat rooms cannot be enabled or disabled by using the Lync Server Control Panel.</span></span>

<span data-ttu-id="8787a-119">チャットルームの設定の詳細については、展開ドキュメントの「 [Lync Server 2013 で会議室を構成](lync-server-2013-configure-rooms.md) する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8787a-119">For details about configuring chat rooms, see [Configure rooms in Lync Server 2013](lync-server-2013-configure-rooms.md) in the Deployment documentation.</span></span>

<span data-ttu-id="8787a-120"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8787a-120"></div>

<span> </span>

</div>

</div>

</span></span></div>

