---
title: 'Lync Server 2013: 常設チャットデータベースのバックアップ'
description: 'Lync Server 2013: 常設チャットデータベースのバックアップ。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Backing up Persistent Chat databases
ms:assetid: b99ebdc0-a025-44d7-9d74-37a7365f330d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945646(v=OCS.15)
ms:contentKeyID: 51541507
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9885eaf0065f5b558922c056fb1f669a5b821460
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438023"
---
# <a name="backing-up-persistent-chat-databases-in-lync-server-2013"></a><span data-ttu-id="30d5b-103">Lync Server 2013 での常設チャットデータベースのバックアップ</span><span class="sxs-lookup"><span data-stu-id="30d5b-103">Backing up Persistent Chat databases in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="30d5b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="30d5b-104">

<span> </span></span></span>

<span data-ttu-id="30d5b-105">_**最終更新日:** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="30d5b-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<span data-ttu-id="30d5b-106">常設チャットルームのコンテンツは、常設チャットデータベース (行う) に保存されます。</span><span class="sxs-lookup"><span data-stu-id="30d5b-106">Persistent Chat room content is stored in the Persistent Chat database (Mgc.mdf).</span></span> <span data-ttu-id="30d5b-107">コンプライアンス データは非常に重要なビジネス データであり、定期的なバックアップが必要です。</span><span class="sxs-lookup"><span data-stu-id="30d5b-107">This is business-critical data that should be backed up regularly.</span></span> <span data-ttu-id="30d5b-108">常設チャットデータベースには、チャットルームのコンテンツに加えて、プリンシパルに関する情報 (ユーザー、ユーザーグループなど) と、チャットルームやチャットルームに必要なロールとアクセスも保存されます。</span><span class="sxs-lookup"><span data-stu-id="30d5b-108">In addition to the chat room content, the Persistent Chat database also stores information about the principals (such as users and user groups), and the roles and access that they have to chat rooms and chat room.</span></span>

<span data-ttu-id="30d5b-109">常設チャットデータをバックアップするには、2つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="30d5b-109">There are two ways of backing up Persistent Chat data.</span></span>

  - <span data-ttu-id="30d5b-110">SQL Server バックアップ</span><span class="sxs-lookup"><span data-stu-id="30d5b-110">SQL Server Backup</span></span>

  - <span data-ttu-id="30d5b-111">この `Export-CsPersistentChatData` コマンドレットは永続的なチャットデータをファイルとしてエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="30d5b-111">The `Export-CsPersistentChatData` cmdlet, which exports Persistent Chat data as a file</span></span>

<span data-ttu-id="30d5b-112">SQL Server のバックアップを使用して作成されたデータには、より多くのディスク領域が必要です。これは、によって作成された場合よりも20倍です `Export-CsPersistentChatData` が、Sql Server バックアップは管理者が理解している手順である可能性が高くなります。</span><span class="sxs-lookup"><span data-stu-id="30d5b-112">Data that is created by using SQL Server backup requires significantly more disk space—possibly 20 times more—than that created by `Export-CsPersistentChatData`, but SQL Server backup is more likely to be a procedure that administrators are familiar with.</span></span>

<span data-ttu-id="30d5b-113"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="30d5b-113"></div>

<span> </span>

</div>

</div>

</span></span></div>

