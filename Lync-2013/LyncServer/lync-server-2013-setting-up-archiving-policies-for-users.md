---
title: 'Lync Server 2013: ユーザーのアーカイブポリシーを設定する'
description: 'Lync Server 2013: ユーザーのアーカイブポリシーを設定します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up Archiving policies for users
ms:assetid: 1bbb45df-0590-4c66-9d65-d25526f57790
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204722(v=OCS.15)
ms:contentKeyID: 48183549
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9c18a15c1a0611f49a6fd9a4983f3ce87104332e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444764"
---
# <a name="setting-up-archiving-policies-for-users-in-lync-server-2013"></a><span data-ttu-id="d4f40-103">Lync Server 2013 でユーザーのアーカイブポリシーを設定する</span><span class="sxs-lookup"><span data-stu-id="d4f40-103">Setting up Archiving policies for users in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d4f40-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d4f40-104">

<span> </span></span></span>

<span data-ttu-id="d4f40-105">_**最終更新日:** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="d4f40-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="d4f40-106">特定のユーザーのアーカイブを有効または無効にするには、ユーザーのアーカイブポリシーを作成して構成し、そのポリシーを特定のユーザーまたはユーザーグループに適用します。</span><span class="sxs-lookup"><span data-stu-id="d4f40-106">You can enable or disable Archiving for specific users by creating and configuring an Archiving policy for users, and then applying the policy to specific users or user groups.</span></span> <span data-ttu-id="d4f40-107">ユーザー ポリシーは、グローバル ポリシーやサイト ポリシーより優先されます。</span><span class="sxs-lookup"><span data-stu-id="d4f40-107">User policies override any global policy or site policies.</span></span> <span data-ttu-id="d4f40-108">アーカイブポリシーが適用されるのは、Microsoft Exchange 統合を使用していない場合、または Microsoft Exchange 統合を使用していないが、Exchange 2013 を使っていないユーザーがいて、メールボックスが In-Place 保留になっている場合のみです。</span><span class="sxs-lookup"><span data-stu-id="d4f40-108">Archiving policies only apply if you do not use Microsoft Exchange integration or, if you do use Microsoft Exchange integration, but have some users who are not homed on Exchange 2013 and have their mailboxes put on In-Place Hold.</span></span>

<span data-ttu-id="d4f40-109">グローバル、サイト、ユーザーのポリシーの階層など、アーカイブポリシーの動作について詳しくは、「 [Lync Server 2013 でのアーカイブのしくみ](lync-server-2013-how-archiving-works.md) 」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="d4f40-109">For details about how Archiving policies work, including the hierarchy for global, site, and user policies, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="d4f40-110">展開時に Microsoft Exchange の統合を有効にすると、exchange 2013 を使用しているユーザーに対してアーカイブが有効になっているかどうかを制御するための Exchange In-Place ホールドポリシーが適用され、メールボックスは In-Place 保留になります。</span><span class="sxs-lookup"><span data-stu-id="d4f40-110">If you enable Microsoft Exchange integration for your deployment, Exchange In-Place Hold policies control whether archiving is enabled for the users who are homed on Exchange 2013 and have their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="d4f40-111">詳細については、展開ドキュメントで <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Exchange Server との統合を使用する場合の「Lync server 2013 でアーカイブするためのポリシーを設定する</A> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d4f40-111">For details, see <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</A> in the Deployment documentation.</span></span><BR><span data-ttu-id="d4f40-112">アーカイブ ポリシーで内部または外部の通信のアーカイブを有効にする前に、アーカイブ構成のすべてのオプションを適切に指定してください。</span><span class="sxs-lookup"><span data-stu-id="d4f40-112">You should specify all appropriate options in the Archiving configurations before enabling Archiving of internal or external communications in the Archiving policies.</span></span> <span data-ttu-id="d4f40-113">詳細については、展開ドキュメントの「 <A href="lync-server-2013-configuring-archiving-options.md">Lync Server 2013 でアーカイブオプションを構成する</A> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d4f40-113">For details, see <A href="lync-server-2013-configuring-archiving-options.md">Configuring Archiving options in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="d4f40-114">このセクション中</span><span class="sxs-lookup"><span data-stu-id="d4f40-114">In This Section</span></span>

  - [<span data-ttu-id="d4f40-115">Lync Server 2013 でアーカイブ用のユーザーポリシーを設定する</span><span class="sxs-lookup"><span data-stu-id="d4f40-115">Setting up user policies for Archiving in Lync Server 2013</span></span>](lync-server-2013-setting-up-user-policies-for-archiving-in-lync-server.md)

  - [<span data-ttu-id="d4f40-116">Exchange Server との統合を使用するときに、Lync Server 2013 でアーカイブするためのポリシーを設定する</span><span class="sxs-lookup"><span data-stu-id="d4f40-116">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</span></span>](lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md)

<span data-ttu-id="d4f40-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d4f40-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

