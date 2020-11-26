---
title: 'Lync Server 2013: ユーザーごとのポリシーの割り当て'
description: 'Lync Server 2013: ユーザーごとのポリシーを割り当てます。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assigning per-user policies
ms:assetid: a4ed0120-d9e5-4eb2-acfd-8de2cb503652
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182561(v=OCS.15)
ms:contentKeyID: 48184971
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6a99156f9413926251c27dfee40677976b80b7ea
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438296"
---
# <a name="assigning-per-user-policies-in-lync-server-2013"></a><span data-ttu-id="270bd-103">Lync Server 2013 でのユーザーごとのポリシーの割り当て</span><span class="sxs-lookup"><span data-stu-id="270bd-103">Assigning per-user policies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="270bd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="270bd-104">

<span> </span></span></span>

<span data-ttu-id="270bd-105">_**最終更新日:** 2012-10-14_</span><span class="sxs-lookup"><span data-stu-id="270bd-105">_**Topic Last Modified:** 2012-10-14_</span></span>

<span data-ttu-id="270bd-106">グローバルポリシーなど、他のユーザーに割り当てられているポリシーで定義されている設定から逸脱する特定の設定を指定するために、特定のポリシーをユーザーまたはユーザーのグループに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="270bd-106">You can assign certain policies to a user or a group of users in order to specify particular settings that deviate from the settings defined in policies assigned to other users, such as global policies.</span></span> <span data-ttu-id="270bd-107">これらのポリシーは、ユーザーごとのポリシーと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="270bd-107">These policies are called per-user policies.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="270bd-108">このセクション中</span><span class="sxs-lookup"><span data-stu-id="270bd-108">In This Section</span></span>

  - [<span data-ttu-id="270bd-109">Lync Server 2013 でユーザーごとの会議ポリシーを割り当てる</span><span class="sxs-lookup"><span data-stu-id="270bd-109">Assign a per-user conferencing policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-conferencing-policy.md)

  - [<span data-ttu-id="270bd-110">Lync Server 2013 でユーザーごとのクライアントバージョンポリシーを割り当てる</span><span class="sxs-lookup"><span data-stu-id="270bd-110">Assign a per-user client version policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-client-version-policy.md)

  - [<span data-ttu-id="270bd-111">Lync Server 2013 でユーザーごとの PIN ポリシーを割り当てる</span><span class="sxs-lookup"><span data-stu-id="270bd-111">Assign a per-user PIN policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-pin-policy.md)

  - [<span data-ttu-id="270bd-112">Lync Server 2013 での Lync が有効なユーザーに対する外部ユーザー アクセス ポリシーの割り当て</span><span class="sxs-lookup"><span data-stu-id="270bd-112">Assign an external user access policy to a Lync enabled user in Lync Server 2013</span></span>](lync-server-2013-assign-an-external-user-access-policy-to-a-lync-enabled-user.md)

  - [<span data-ttu-id="270bd-113">Lync Server 2013 でユーザーごとのアーカイブポリシーを割り当てる</span><span class="sxs-lookup"><span data-stu-id="270bd-113">Assign a per-user archiving policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-archiving-policy.md)

  - [<span data-ttu-id="270bd-114">Lync Server 2013 でユーザーごとの場所ポリシーを割り当てる</span><span class="sxs-lookup"><span data-stu-id="270bd-114">Assign a per-user location policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-location-policy.md)

  - [<span data-ttu-id="270bd-115">Lync Server 2013 でユーザーごとのモバイルポリシーを割り当てる</span><span class="sxs-lookup"><span data-stu-id="270bd-115">Assign a per-user mobility policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-mobility-policy.md)

  - [<span data-ttu-id="270bd-116">Lync Server 2013 でユーザーごとの常設チャットポリシーを割り当てる</span><span class="sxs-lookup"><span data-stu-id="270bd-116">Assign a per-user Persistent Chat policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-persistent-chat-policy.md)

  - [<span data-ttu-id="270bd-117">Lync Server 2013 でユーザーごとのダイヤルプランポリシーを割り当てる</span><span class="sxs-lookup"><span data-stu-id="270bd-117">Assign a per-user dial plan policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-dial-plan-policy.md)

  - [<span data-ttu-id="270bd-118">Lync Server 2013 でユーザーごとの音声ポリシーを割り当てる</span><span class="sxs-lookup"><span data-stu-id="270bd-118">Assign a per-user voice policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-voice-policy.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="270bd-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="270bd-119">See Also</span></span>


[<span data-ttu-id="270bd-120">Lync Server 2013 のユーザー管理</span><span class="sxs-lookup"><span data-stu-id="270bd-120">Managing users in Lync Server 2013</span></span>](lync-server-2013-managing-users-in-lync-server.md)  
  

<span data-ttu-id="270bd-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="270bd-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

