---
title: 'Lync Server 2013: ホスト ボイス メール ポリシーの管理'
description: 'Lync Server 2013: ホストされているボイスメールポリシーを管理します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Manage hosted voice mail policies
ms:assetid: 50ff22e3-9c8b-4a33-a72f-d149892acf53
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398332(v=OCS.15)
ms:contentKeyID: 48184139
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fcb5e98884d37540d5e75cc8cb6b1b419e4e75e6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426096"
---
# <a name="manage-hosted-voice-mail-policies-in-lync-server-2013"></a><span data-ttu-id="13024-103">Lync Server 2013 でのホスト ボイス メール ポリシーの管理</span><span class="sxs-lookup"><span data-stu-id="13024-103">Manage hosted voice mail policies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="13024-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="13024-104">

<span> </span></span></span>

<span data-ttu-id="13024-105">_**最終更新日:** 2012-09-20_</span><span class="sxs-lookup"><span data-stu-id="13024-105">_**Topic Last Modified:** 2012-09-20_</span></span>

<span data-ttu-id="13024-106">ホストされた *ボイスメールポリシー* は、ホストされた Exchange サービス上にあるメールボックスを持つユーザーの呼び出しをルーティングする場所について、Lync Server 2013 Exum ルーティングアプリケーションに情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="13024-106">A *hosted voice mail policy* provides information to the Lync Server 2013 ExUM Routing application about where to route calls for users whose mailboxes are located on a hosted Exchange service.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="13024-107">通常は、1つのホストされたボイスメールポリシーのみが必要です。</span><span class="sxs-lookup"><span data-stu-id="13024-107">Typically, only one hosted voice mail policy is required.</span></span> <span data-ttu-id="13024-108">多くの場合、すべてのニーズに合わせてグローバルポリシーを変更できます。</span><span class="sxs-lookup"><span data-stu-id="13024-108">In many cases, you can modify the global policy to meet all your needs.</span></span> <span data-ttu-id="13024-109">サイトのスコープを使用してポリシーを作成すると、指定したサイトに所属するすべてのユーザーに自動的に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="13024-109">If you create a policy with site scope, it is assigned automatically to all users homed at the specified site.</span></span> <span data-ttu-id="13024-110">ユーザーごとのスコープを持つポリシーを作成する場合は、ユーザー、グループ、連絡先オブジェクトに明示的に割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="13024-110">If you create a policy with per-user scope, you must explicitly assign it to users, groups, and contact objects.</span></span> <span data-ttu-id="13024-111">複数のホストされたボイスメールポリシーを展開することもできますが、その場合は、ポリシーをユーザーごとに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="13024-111">It is possible to deploy multiple hosted voice mail policies, but in that case the policies must be assigned on a per-user basis.</span></span>



</div>

<span data-ttu-id="13024-112">ホストされたボイスメールポリシーの計画の詳細については、計画ドキュメントの「 [Lync Server 2013 のホスト型ボイスメールポリシー](lync-server-2013-hosted-voice-mail-policies.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="13024-112">For details about planning hosted voice mail policies, see [Hosted voice mail policies in Lync Server 2013](lync-server-2013-hosted-voice-mail-policies.md) in the Planning documentation.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="13024-113">このセクション中</span><span class="sxs-lookup"><span data-stu-id="13024-113">In This Section</span></span>

  - [<span data-ttu-id="13024-114">Lync Server 2013 でグローバルにホストされるボイスメールのポリシーを変更する</span><span class="sxs-lookup"><span data-stu-id="13024-114">Modify the global hosted voice mail policy in Lync Server 2013</span></span>](lync-server-2013-modify-the-global-hosted-voice-mail-policy.md)

  - [<span data-ttu-id="13024-115">Lync Server 2013 でサイトレベルでホストされるボイスメールのポリシーを作成する</span><span class="sxs-lookup"><span data-stu-id="13024-115">Create a site-level hosted voice mail policy in Lync Server 2013</span></span>](lync-server-2013-create-a-site-level-hosted-voice-mail-policy.md)

  - [<span data-ttu-id="13024-116">Lync Server 2013 でユーザーごとにホストされるボイスメールのポリシーを作成する</span><span class="sxs-lookup"><span data-stu-id="13024-116">Create a per-user hosted voice mail policy in Lync Server 2013</span></span>](lync-server-2013-create-a-per-user-hosted-voice-mail-policy.md)

  - [<span data-ttu-id="13024-117">Lync Server 2013 でユーザーごとにホストされるボイスメールのポリシーを割り当てる</span><span class="sxs-lookup"><span data-stu-id="13024-117">Assign a per-user hosted voice mail policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-hosted-voice-mail-policy.md)

<span data-ttu-id="13024-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="13024-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

