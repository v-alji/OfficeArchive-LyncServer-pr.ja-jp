---
title: 'Lync Server 2013: アクセス許可の付与'
description: 'Lync Server 2013: アクセス許可を付与します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Granting permissions
ms:assetid: d1c9ea66-bd07-480e-99a0-011108f97e42
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398901(v=OCS.15)
ms:contentKeyID: 48185446
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4bdb2b1ef39b85caa89c7597f455e6e4fc08e44e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399734"
---
# <a name="granting-permissions-in-lync-server-2013"></a><span data-ttu-id="67437-103">Lync Server 2013 でのアクセス許可の付与</span><span class="sxs-lookup"><span data-stu-id="67437-103">Granting permissions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="67437-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="67437-104">

<span> </span></span></span>

<span data-ttu-id="67437-105">_**最終更新日:** 2012-10-15_</span><span class="sxs-lookup"><span data-stu-id="67437-105">_**Topic Last Modified:** 2012-10-15_</span></span>

<span data-ttu-id="67437-106">セットアップの場合、特定の Active Directory 組織単位 (OU) の RTCUniversalServerAdmins ユニバーサルグループにアクセス許可を付与し、その OU の RTCUniversalServerAdmins グループのメンバーが、指定したドメインに Lync Server 2013 をインストールできるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="67437-106">For setup, you can grant permissions to the RTCUniversalServerAdmins universal group for a specific Active Directory organizational unit (OU), enabling members of the RTCUniversalServerAdmins group in that OU to install Lync Server 2013 in the specified domain.</span></span> <span data-ttu-id="67437-107">OU にアクセス許可を付与すると、次のアクセス許可が付与されます。</span><span class="sxs-lookup"><span data-stu-id="67437-107">When you grant permissions for an OU, the following permissions are granted:</span></span>

  - <span data-ttu-id="67437-108">モード</span><span class="sxs-lookup"><span data-stu-id="67437-108">Read</span></span>

  - <span data-ttu-id="67437-109">書き込み</span><span class="sxs-lookup"><span data-stu-id="67437-109">Write</span></span>

  - <span data-ttu-id="67437-110">ReadSPN</span><span class="sxs-lookup"><span data-stu-id="67437-110">ReadSPN</span></span>

  - <span data-ttu-id="67437-111">WriteSPN</span><span class="sxs-lookup"><span data-stu-id="67437-111">WriteSPN</span></span>

<span data-ttu-id="67437-112">管理者は、特定の Ou にアクセス許可を追加して、フォレストの準備によって作成された RTC ユニバーサルグループのメンバーが、Domain Admins グループのメンバーではなくても Ou にアクセスできるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="67437-112">For administration, you can add permissions to specified OUs so that members of the RTC universal groups created by forest preparation can access the OUs without needing to be members of the Domain Admins group.</span></span> <span data-ttu-id="67437-113">指定した OU に追加されたアクセス許可は、[ユーザーの **有効化** ] と同じアクセス許可であり、[コンピューター] と [ユーザー] のコンテナーに追加します。</span><span class="sxs-lookup"><span data-stu-id="67437-113">The permissions added to the specified OU are the same permissions that the **Enable-CsAdDomain** cmdlet adds to the computers and users OU containers.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="67437-114">このセクション中</span><span class="sxs-lookup"><span data-stu-id="67437-114">In This Section</span></span>

  - [<span data-ttu-id="67437-115">Lync Server 2013 でのセットアップ アクセス許可の付与</span><span class="sxs-lookup"><span data-stu-id="67437-115">Granting setup permissions in Lync Server 2013</span></span>](lync-server-2013-granting-setup-permissions.md)

  - [<span data-ttu-id="67437-116">Lync Server 2013 での組織単位アクセス許可の付与</span><span class="sxs-lookup"><span data-stu-id="67437-116">Granting organizational unit permissions in Lync Server 2013</span></span>](lync-server-2013-granting-organizational-unit-permissions.md)

<span data-ttu-id="67437-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="67437-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

