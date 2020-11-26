---
title: 'Lync Server 2013: 常設チャット サーバー ポリシーを有効にする'
description: 'Lync Server 2013: 常設チャットサーバーポリシーを有効にします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable Persistent Chat Server policy
ms:assetid: 87063d6c-2e38-4970-b76d-2aa15f0de29e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205056(v=OCS.15)
ms:contentKeyID: 48184718
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e58da577679795f00492af72b43ca72106d40f4f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428840"
---
# <a name="enable-persistent-chat-server-policy-in-lync-server-2013"></a><span data-ttu-id="ac62a-103">Lync Server 2013 で常設チャット サーバー ポリシーを有効にする</span><span class="sxs-lookup"><span data-stu-id="ac62a-103">Enable Persistent Chat Server policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ac62a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ac62a-104">

<span> </span></span></span>

<span data-ttu-id="ac62a-105">_**最終更新日:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="ac62a-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="ac62a-106">Lync Server 2013 コントロールパネルでは、**常設チャット** グループの **常設チャットのポリシー** ページを使用して、既定のグローバルポリシーを構成し、展開用に1つ以上の追加のユーザーとサイトポリシーを作成するなど、グローバル、プール、サイト、またはユーザーレベルでポリシーを管理できます。</span><span class="sxs-lookup"><span data-stu-id="ac62a-106">In the Lync Server 2013 Control Panel, you can use the **Persistent Chat Policy** page of the **Persistent Chat** group to manage policies at a global, pool, site, or user level, including configuring the default global policy and creating one or more additional user and site policies for your deployment.</span></span> <span data-ttu-id="ac62a-107">ユーザーが、ポリシーによって常設チャットサーバーを有効にしている場合は、常設チャットサーバー環境が Lync 2013 クライアントに表示されます。</span><span class="sxs-lookup"><span data-stu-id="ac62a-107">If a user is enabled for Persistent Chat Server by policy, then the Persistent Chat Server environment appears in their Lync 2013 client.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="ac62a-108">トポロジでは、常設チャットサーバーのサイトポリシーは、ユーザーのプールごと、またはユーザーごとのサイトに適用されます。</span><span class="sxs-lookup"><span data-stu-id="ac62a-108">In the topology, Persistent Chat Server site policies apply globally, per user’s pool, or per user’s site, or per user.</span></span>



</div>

<span data-ttu-id="ac62a-109">グローバルポリシーは、常設チャットサーバーの展開時に自動的に作成され、構成はできますが、削除はできません。</span><span class="sxs-lookup"><span data-stu-id="ac62a-109">The global policy is created automatically when you deploy Persistent Chat Server, and it can be configured, but not deleted.</span></span> <span data-ttu-id="ac62a-110">グローバル ポリシーはすべてのユーザーに適用されるため、ユーザーごとに設定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="ac62a-110">Because the global policy applies to all users, it doesn’t have to be set per user.</span></span>

<span data-ttu-id="ac62a-111">グローバルポリシーと共に、常設チャットサーバーのユーザーを有効にする、複数のサイトとユーザーのポリシーを作成して構成することができます。</span><span class="sxs-lookup"><span data-stu-id="ac62a-111">You can create and configure multiple site and user policies which, together with the global policy, enable users for Persistent Chat Server.</span></span> <span data-ttu-id="ac62a-112">プールとサイトの常設チャットサーバーポリシーは、そのサイトのユーザーに対してのみ、グローバル常設チャットサーバーポリシーを上書きします。</span><span class="sxs-lookup"><span data-stu-id="ac62a-112">Pool and site Persistent Chat Server policies override the global Persistent Chat Server policy, but only for users of that site.</span></span> <span data-ttu-id="ac62a-113">ユーザーポリシーは、ユーザーポリシーが割り当てられているユーザーのグローバル、プール、サイトの各ポリシーを上書きします。</span><span class="sxs-lookup"><span data-stu-id="ac62a-113">User policies override both global, pool, and site policies for the users to whom the user policy is assigned.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="ac62a-114">常設チャットサーバーを構成して使用するには、最初にトポロジビルダーを使用して、トポロジに常設チャットサーバーサポートを追加してから、トポロジを発行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ac62a-114">To configure and use Persistent Chat Server, you must first use Topology Builder to add Persistent Chat Server support to the topology, and then publish the topology.</span></span> <span data-ttu-id="ac62a-115">詳細については、展開ドキュメントの「 <A href="lync-server-2013-adding-persistent-chat-server-to-your-deployment.md">Lync server 2013 での展開への常設チャットサーバーの追加</A> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ac62a-115">For details, see <A href="lync-server-2013-adding-persistent-chat-server-to-your-deployment.md">Adding Persistent Chat Server to your deployment in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="ac62a-116">このセクション中</span><span class="sxs-lookup"><span data-stu-id="ac62a-116">In This Section</span></span>

  - [<span data-ttu-id="ac62a-117">Lync Server 2013 で常設チャットのグローバル ポリシーを構成する</span><span class="sxs-lookup"><span data-stu-id="ac62a-117">Configure the global policy for Persistent Chat in Lync Server 2013</span></span>](lync-server-2013-configure-the-global-policy-for-persistent-chat.md)

  - [<span data-ttu-id="ac62a-118">Lync Server 2013 で常設チャットのサイト ポリシーを作成する</span><span class="sxs-lookup"><span data-stu-id="ac62a-118">Create a site policy for Persistent Chat in Lync Server 2013</span></span>](lync-server-2013-create-a-site-policy-for-persistent-chat.md)

  - [<span data-ttu-id="ac62a-119">Lync Server 2013 で常設チャット用のユーザー ポリシーを作成する</span><span class="sxs-lookup"><span data-stu-id="ac62a-119">Create a user policy for Persistent Chat in Lync Server 2013</span></span>](lync-server-2013-create-a-user-policy-for-persistent-chat.md)

  - [<span data-ttu-id="ac62a-120">Lync Server 2013 で常設チャット ポリシーをユーザーまたはユーザー グループに適用する</span><span class="sxs-lookup"><span data-stu-id="ac62a-120">Apply a Persistent Chat policy to a user or user group in Lync Server 2013</span></span>](lync-server-2013-apply-a-persistent-chat-policy-to-a-user-or-user-group.md)

<span data-ttu-id="ac62a-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ac62a-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

