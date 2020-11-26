---
title: 'Lync Server 2013: 大会議室のチャット ルームでメッセージを投稿できるユーザーの設定'
description: 'Lync Server 2013: 聴衆チャットルームにメッセージを投稿できるユーザーを設定します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting who can post messages in an auditorium chat room
ms:assetid: 26168d3e-362c-4c34-9693-21301f151166
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ215873(v=OCS.15)
ms:contentKeyID: 48705999
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0fba9e31a0cb5be9de66a9fc7185b5dea6c507cb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441614"
---
# <a name="setting-who-can-post-messages-in-an-auditorium-chat-room-in-lync-server-2013"></a><span data-ttu-id="bfa1f-103">Lync Server 2013 での大会議室のチャット ルームでメッセージを投稿できるユーザーの設定</span><span class="sxs-lookup"><span data-stu-id="bfa1f-103">Setting who can post messages in an auditorium chat room in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bfa1f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bfa1f-104">

<span> </span></span></span>

<span data-ttu-id="bfa1f-105">_**最終更新日:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="bfa1f-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="bfa1f-106">聴衆チャットルームでは、発表者の役割を与えられたユーザーのみがメッセージを投稿できます。</span><span class="sxs-lookup"><span data-stu-id="bfa1f-106">In an auditorium chat room, only users who have been granted the role of Presenter can post messages.</span></span> <span data-ttu-id="bfa1f-107">他のすべてのメンバーはメッセージのみを読むことができます。</span><span class="sxs-lookup"><span data-stu-id="bfa1f-107">All other members can only read messages.</span></span> <span data-ttu-id="bfa1f-108">聴衆チャットルームの発表者は、チャットルームのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="bfa1f-108">Presenters in an auditorium chat room must be members of the chat room.</span></span>

<span data-ttu-id="bfa1f-109">聴衆チャットルームを管理するために Windows PowerShell コマンドラインインターフェイスを使用する方法について詳しくは、「展開ドキュメントの [会議室を管理](manage-rooms.md) する」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="bfa1f-109">For details about using the Windows PowerShell command-line interface to manage auditorium chat rooms, see [Manage rooms](manage-rooms.md) in the Deployment documentation.</span></span>

<span data-ttu-id="bfa1f-110">常設チャットルームの管理者やチャットルームの管理者は、チャットルームの設定を管理できますが、 **発表** 者でなければ聴衆チャットルームに投稿することはできません。</span><span class="sxs-lookup"><span data-stu-id="bfa1f-110">Although Persistent Chat room administrators and chat room managers can manage chat room settings, they cannot post in an auditorium chat room unless they are **Presenters**.</span></span>

<span data-ttu-id="bfa1f-111"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bfa1f-111"></div>

<span> </span>

</div>

</div>

</span></span></div>

