---
title: 'Lync Server 2013: アーカイブのアクセス許可を設定する'
description: 'Lync Server 2013: アーカイブのアクセス許可を設定します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up permissions for Archiving
ms:assetid: 67f97c94-52f5-4a83-a35c-8c307d5de9a4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204961(v=OCS.15)
ms:contentKeyID: 48184364
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1f06c4fb48772a41621ece765dcc90555f0cd2d5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399807"
---
# <a name="setting-up-permissions-for-archiving-in-lync-server-2013"></a><span data-ttu-id="fa4f3-103">Lync Server 2013 でアーカイブするためのアクセス許可を設定する</span><span class="sxs-lookup"><span data-stu-id="fa4f3-103">Setting up permissions for Archiving in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fa4f3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fa4f3-104">

<span> </span></span></span>

<span data-ttu-id="fa4f3-105">_**最終更新日:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="fa4f3-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="fa4f3-106">Lync Server 2013 では、特定のタスクを実行するユーザーが、1つ以上の特定のグループのメンバーになる必要があります。</span><span class="sxs-lookup"><span data-stu-id="fa4f3-106">In Lync Server 2013, specific tasks still require that users who perform those tasks be members of one or more specific groups.</span></span> <span data-ttu-id="fa4f3-107">ただし、ロールベースのアクセス制御 (RBAC) を使用して、定義済みの Lync Server 管理者ロールにユーザーを割り当てることによって権限を付与することもできます。アーカイブを展開する前に、適切なユーザー権限と権限が設定されていること、および特定の RBAC ロールに割り当てるユーザーがそのロールに割り当てられていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fa4f3-107">However, you can also use role-based access control (RBAC) to grant privileges by assigning users to predefined Lync Server administrative roles.Before you deploy Archiving, be sure that the appropriate user rights and permissions are in place, and that any users who you want to assign to a specific RBAC role have been assigned to that role.</span></span> <span data-ttu-id="fa4f3-108">アーカイブのサポートを展開するためのユーザー権利、権限、およびロールの詳細については、「計画ドキュメントと展開ドキュメントで利用可能な [Lync Server 2013 のアーカイブ用の展開チェックリスト](lync-server-2013-deployment-checklist-for-archiving.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fa4f3-108">For details about the user rights, permissions, and roles for deploying support for Archiving, see [Deployment checklist for Archiving in Lync Server 2013](lync-server-2013-deployment-checklist-for-archiving.md), which is available in the Planning documentation and the Deployment documentation.</span></span> <span data-ttu-id="fa4f3-109">RBAC の詳細については、計画ドキュメントの「 [Lync Server 2013 での役割ベースのアクセス制御の計画](lync-server-2013-planning-for-role-based-access-control.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fa4f3-109">For details about RBAC, see [Planning for role-based access control in Lync Server 2013](lync-server-2013-planning-for-role-based-access-control.md) in the Planning documentation.</span></span>

<span data-ttu-id="fa4f3-110"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fa4f3-110"></div>

<span> </span>

</div>

</div>

</span></span></div>

