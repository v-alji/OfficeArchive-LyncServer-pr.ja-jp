---
title: Windows PowerShell コマンドレットを使用した常設チャット サーバーの構成
description: Windows PowerShell コマンドレットを使用して、常設チャットサーバーを構成します。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Configuring Persistent Chat Server by using Windows PowerShell cmdlets
ms:assetid: 4c1d1ad7-b6bd-476f-9c5b-f0c1756d5aa8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204877(v=OCS.15)
ms:contentKeyID: 48184089
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 39d97657684227ef3c36f6ac39389220a6805f82
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398846"
---
# <a name="configuring-persistent-chat-server-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="2e1d4-103">Windows PowerShell コマンドレットを使用した常設チャット サーバーの構成</span><span class="sxs-lookup"><span data-stu-id="2e1d4-103">Configuring Persistent Chat Server by using Windows PowerShell cmdlets</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2e1d4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2e1d4-104">

<span> </span></span></span>

<span data-ttu-id="2e1d4-105">_**最終更新日:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="2e1d4-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="2e1d4-106">次の Windows PowerShell コマンドレットを使用して、Lync Server 2013 の常設チャットサーバー内で管理を構成します。</span><span class="sxs-lookup"><span data-stu-id="2e1d4-106">Use the following Windows PowerShell cmdlets to configure management within Lync Server 2013, Persistent Chat Server.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="2e1d4-107">このセクション中</span><span class="sxs-lookup"><span data-stu-id="2e1d4-107">In This Section</span></span>

  - [<span data-ttu-id="2e1d4-108">Manage categories</span><span class="sxs-lookup"><span data-stu-id="2e1d4-108">Manage categories</span></span>](manage-categories.md)

  - [<span data-ttu-id="2e1d4-109">ルームの管理</span><span class="sxs-lookup"><span data-stu-id="2e1d4-109">Manage rooms</span></span>](manage-rooms.md)

  - [<span data-ttu-id="2e1d4-110">アドインの管理</span><span class="sxs-lookup"><span data-stu-id="2e1d4-110">Manage add-ins</span></span>](manage-add-ins.md)

  - [<span data-ttu-id="2e1d4-111">メッセージを削除する</span><span class="sxs-lookup"><span data-stu-id="2e1d4-111">Remove a message</span></span>](remove-a-message.md)

  - [<span data-ttu-id="2e1d4-112">代理トランザクションを使用した常設チャット サーバー のテスト</span><span class="sxs-lookup"><span data-stu-id="2e1d4-112">Test Persistent Chat Server with a synthetic transaction</span></span>](test-persistent-chat-server-with-a-synthetic-transaction.md)

  - [<span data-ttu-id="2e1d4-113">常設チャット サーバーに対する下位互換性の実行</span><span class="sxs-lookup"><span data-stu-id="2e1d4-113">Run backward compatibility for Persistent Chat Server</span></span>](run-backward-compatibility-for-persistent-chat-server.md)

  - [<span data-ttu-id="2e1d4-114">Lync Server 2013 で常設チャット ポリシーを実行、付与、削除、または設定する</span><span class="sxs-lookup"><span data-stu-id="2e1d4-114">Run, grant, get, remove, or set Persistent Chat Policy in Lync Server 2013</span></span>](lync-server-2013-run-grant-get-remove-or-set-persistent-chat-policy.md)

  - [<span data-ttu-id="2e1d4-115">Lync Server 2013 での常設チャット サーバーの構成</span><span class="sxs-lookup"><span data-stu-id="2e1d4-115">Configure Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-configure-persistent-chat-server.md)

  - [<span data-ttu-id="2e1d4-116">Lync Server 2013 で常設チャット サーバー プールの状態を取得する</span><span class="sxs-lookup"><span data-stu-id="2e1d4-116">Get Persistent Chat Server pool availability in Lync Server 2013</span></span>](lync-server-2013-get-persistent-chat-server-pool-availability.md)

  - [<span data-ttu-id="2e1d4-117">Lync Server 2013 の常設チャット コンプライアンス</span><span class="sxs-lookup"><span data-stu-id="2e1d4-117">Persistent Chat compliance in Lync Server 2013</span></span>](lync-server-2013-persistent-chat-compliance.md)

<span data-ttu-id="2e1d4-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2e1d4-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

