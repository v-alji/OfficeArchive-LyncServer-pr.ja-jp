---
title: 'Lync Server 2013: Lync Server でアーカイブ用のユーザーポリシーを設定する'
description: 'Lync Server 2013: Lync Server でアーカイブ用のユーザーポリシーを設定します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up user policies for Archiving in Lync Server
ms:assetid: 22d6cc76-6b5c-4a8c-bb8a-7996450ec085
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204742(v=OCS.15)
ms:contentKeyID: 48183626
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9e33abf6cf16c9c1367162aa8beee91874f4c725
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441628"
---
# <a name="setting-up-user-policies-for-archiving-in-lync-server-2013"></a><span data-ttu-id="c1e1a-103">Lync Server 2013 でアーカイブ用のユーザーポリシーを設定する</span><span class="sxs-lookup"><span data-stu-id="c1e1a-103">Setting up user policies for Archiving in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c1e1a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c1e1a-104">

<span> </span></span></span>

<span data-ttu-id="c1e1a-105">_**最終更新日:** 2012-10-10_</span><span class="sxs-lookup"><span data-stu-id="c1e1a-105">_**Topic Last Modified:** 2012-10-10_</span></span>

<span data-ttu-id="c1e1a-106">Lync Server 2013 上にある特定のユーザーに対してアーカイブを有効または無効にするには、1つ以上のユーザーポリシーを作成して構成し、適切なポリシーを特定のユーザーまたはユーザーグループに適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c1e1a-106">Enabling or disabling Archiving for specific users homed on Lync Server 2013 requires creating and configuring one or more user policies, and then applying the appropriate policy to specific users or user groups.</span></span> <span data-ttu-id="c1e1a-107">ユーザーポリシーは、サイトとグローバルポリシーを上書きします。ただし、Lync Server 2013 に所属しているユーザーのみです。</span><span class="sxs-lookup"><span data-stu-id="c1e1a-107">User policies override site and global policies, but only for users homed on Lync Server 2013.</span></span>

<span data-ttu-id="c1e1a-108">ユーザーは常に Lync Server に置かれています。</span><span class="sxs-lookup"><span data-stu-id="c1e1a-108">Users are always homed in Lync Server.</span></span> <span data-ttu-id="c1e1a-109">Microsoft Exchange の統合が有効になっている場合、メールボックスが Microsoft Exchange Server 2013 にあるユーザーは、Lync Server で管理されているアーカイブポリシーを持っている必要はありません。</span><span class="sxs-lookup"><span data-stu-id="c1e1a-109">If Microsoft Exchange integration is enabled, users whose mailboxes are in Microsoft Exchange Server 2013 don’t need to have their Archiving policies in Lync Server managed.</span></span> <span data-ttu-id="c1e1a-110">アーカイブを使用するユーザーは、Exchange In-Place ホールドによって管理されます。</span><span class="sxs-lookup"><span data-stu-id="c1e1a-110">These users with Archiving will be managed by Exchange In-Place Hold.</span></span>

<span data-ttu-id="c1e1a-111">グローバル、サイト、ユーザーのポリシーの階層など、アーカイブポリシーの動作について詳しくは、「計画ドキュメント、展開ドキュメント、または操作のドキュメント」の「 [Lync Server 2013 でのアーカイブの動作](lync-server-2013-how-archiving-works.md) 」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="c1e1a-111">For details about how Archiving policies work, including the hierarchy for global, site, and user policies, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="c1e1a-112">展開に対して Microsoft Exchange の統合を有効にしている場合、exchange 2013 を使っているユーザーに対してアーカイブが有効になっているかどうかが Exchange In-Place ホールドポリシーによって制御されます。</span><span class="sxs-lookup"><span data-stu-id="c1e1a-112">If you enabled Microsoft Exchange integration for your deployment, Exchange In-Place Hold policies control whether archiving is enabled for the users who are homed on Exchange 2013.</span></span> <span data-ttu-id="c1e1a-113">これらのユーザーのアーカイブを使用するには、メールボックスを In-Place 保持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c1e1a-113">Archiving for these users requires that they have their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="c1e1a-114">詳細については、展開ドキュメントで <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Exchange Server との統合を使用する場合の「Lync server 2013 でアーカイブするためのポリシーを設定する</A> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c1e1a-114">For details, see <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</A> in the Deployment documentation.</span></span><BR><span data-ttu-id="c1e1a-115">アーカイブを有効にする前に、アーカイブ構成ですべての適切なオプションを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c1e1a-115">You should specify all appropriate options in the Archiving configurations before enabling Archiving.</span></span> <span data-ttu-id="c1e1a-116">詳細については、展開ドキュメントの「 <A href="lync-server-2013-configuring-archiving-options.md">Lync Server 2013 でアーカイブオプションを構成する</A> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c1e1a-116">For details, see <A href="lync-server-2013-configuring-archiving-options.md">Configuring Archiving options in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="c1e1a-117">このセクション中</span><span class="sxs-lookup"><span data-stu-id="c1e1a-117">In This Section</span></span>

  - [<span data-ttu-id="c1e1a-118">Lync Server 2013 でアーカイブ用のユーザーポリシーを作成および構成する</span><span class="sxs-lookup"><span data-stu-id="c1e1a-118">Creating and configuring user policies for Archiving in Lync Server 2013</span></span>](lync-server-2013-creating-and-configuring-user-policies-for-archiving-in-lync-server.md)

  - [<span data-ttu-id="c1e1a-119">Lync server 2013 でユーザーに Lync Server のアーカイブポリシーを適用する</span><span class="sxs-lookup"><span data-stu-id="c1e1a-119">Applying a Lync Server Archiving policy to a user in Lync Server 2013</span></span>](lync-server-2013-applying-a-lync-server-archiving-policy-to-a-user.md)

<span data-ttu-id="c1e1a-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c1e1a-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

