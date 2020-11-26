---
title: 'Lync Server 2013: グループ通話のピックアップの構成'
description: 'Lync Server 2013: グループ通話のピックアップを構成しています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Group Call Pickup
ms:assetid: b4b0a9a0-91c6-43a5-9e2b-a086caeb3f94
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945645(v=OCS.15)
ms:contentKeyID: 51541505
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ff6be1ea20a98cfaf2addf32c7767940b420c5c8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433032"
---
# <a name="configuring-group-call-pickup-in-lync-server-2013"></a><span data-ttu-id="235af-103">Lync Server 2013 でグループ通話のピックアップを構成する</span><span class="sxs-lookup"><span data-stu-id="235af-103">Configuring Group Call Pickup in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="235af-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="235af-104">

<span> </span></span></span>

<span data-ttu-id="235af-105">_**最終更新日:** 2013-02-01_</span><span class="sxs-lookup"><span data-stu-id="235af-105">_**Topic Last Modified:** 2013-02-01_</span></span>

<span data-ttu-id="235af-106">Lync Server 2013 の累積更新プログラム: 2013 年2月に、グループ通話のピックアップが新しいエンタープライズ Voip 機能として導入されています。</span><span class="sxs-lookup"><span data-stu-id="235af-106">Cumulative update for Lync Server 2013: February 2013 introduces Group Call Pickup as a new Enterprise Voice feature.</span></span> <span data-ttu-id="235af-107">グループ通話のピックアップにより、ユーザーは、通話ピックアップグループ番号にダイヤルすることによって、他のユーザーが着信した通話を受け取れるようになります。</span><span class="sxs-lookup"><span data-stu-id="235af-107">Group Call Pickup lets users pick up calls that are ringing for another user by dialing a call pickup group number.</span></span>

<span data-ttu-id="235af-108">グループ通話のピックアップで使用されるコンポーネントは、エンタープライズボイスの展開時に、フロントエンドサーバーまたは Standard Edition サーバーに自動的にインストールされ、有効になります。</span><span class="sxs-lookup"><span data-stu-id="235af-108">The components that Group Call Pickup uses are automatically installed and enabled on the Front End Server or Standard Edition server when you deploy Enterprise Voice.</span></span> <span data-ttu-id="235af-109">ただし、グループ通話のピックアップは、ユーザーが利用できるようになる前に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="235af-109">However, you must configure Group Call Pickup before it is available to users.</span></span>

<span data-ttu-id="235af-110">このセクションでは、グループ通話のピックアップの構成について説明します。</span><span class="sxs-lookup"><span data-stu-id="235af-110">This section guides you through the configuration of Group Call Pickup.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="235af-111">このセクション中</span><span class="sxs-lookup"><span data-stu-id="235af-111">In This Section</span></span>

[<span data-ttu-id="235af-112">グループ通話の集配構成の前提条件とユーザー権限 Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="235af-112">Group Call Pickup configuration prerequisites and user rights in Lync Server 2013</span></span>](lync-server-2013-group-call-pickup-configuration-prerequisites-and-user-rights.md)

[<span data-ttu-id="235af-113">Lync Server 2013 でのグループ通話のピックアップの展開プロセス</span><span class="sxs-lookup"><span data-stu-id="235af-113">Deployment process for Group Call Pickup in Lync Server 2013</span></span>](lync-server-2013-deployment-process-for-group-call-pickup.md)

[<span data-ttu-id="235af-114">Deploy the SEFAUtil tool in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="235af-114">Deploy the SEFAUtil tool in Lync Server 2013</span></span>](lync-server-2013-deploy-the-sefautil-tool.md)

[<span data-ttu-id="235af-115">Lync Server 2013 での通話ピックアップグループ番号の設定</span><span class="sxs-lookup"><span data-stu-id="235af-115">Configure call pickup group numbers in Lync Server 2013</span></span>](lync-server-2013-configure-call-pickup-group-numbers.md)

[<span data-ttu-id="235af-116">Lync Server 2013 のユーザーに対してグループ通話のピックアップを有効にし、グループ番号を割り当てる</span><span class="sxs-lookup"><span data-stu-id="235af-116">Enable Group Call Pickup for users in Lync Server 2013 and assign a group number</span></span>](lync-server-2013-enable-group-call-pickup-for-users-and-assign-a-group-number.md)

[<span data-ttu-id="235af-117">グループ通話の集配の課題を Lync Server 2013 のユーザーに伝える</span><span class="sxs-lookup"><span data-stu-id="235af-117">Communicate Group Call Pickup assignments to users in Lync Server 2013</span></span>](lync-server-2013-communicate-group-call-pickup-assignment-to-users.md)

[<span data-ttu-id="235af-118">省略Lync Server 2013 でグループ通話のピックアップの展開を確認する</span><span class="sxs-lookup"><span data-stu-id="235af-118">(Optional) Verify the Group Call Pickup deployment in Lync Server 2013</span></span>](lync-server-2013-optional-verify-the-group-call-pickup-deployment.md)

<span data-ttu-id="235af-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="235af-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

