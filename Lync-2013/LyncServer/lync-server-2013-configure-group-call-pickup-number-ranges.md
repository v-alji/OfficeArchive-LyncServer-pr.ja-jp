---
title: 'Lync Server 2013: グループ通話の集配番号の範囲を構成する'
description: 'Lync Server 2013: グループ通話の集配番号の範囲を構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure Group Call Pickup number ranges
ms:assetid: f15f75f6-f965-4558-b612-f40cecdd5d8c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945657(v=OCS.15)
ms:contentKeyID: 51541529
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4f0594bd681a157b8ff479846b2f6f1964a09cad
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399386"
---
# <a name="configure-group-call-pickup-number-ranges-in-lync-server-2013"></a><span data-ttu-id="d41fe-103">Lync Server 2013 でグループ通話の集配番号の範囲を構成する</span><span class="sxs-lookup"><span data-stu-id="d41fe-103">Configure Group Call Pickup number ranges in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d41fe-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d41fe-104">

<span> </span></span></span>

<span data-ttu-id="d41fe-105">_**最終更新日:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="d41fe-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="d41fe-106">グループ通話のピックアップは、コールパークアプリケーションに基づいています。</span><span class="sxs-lookup"><span data-stu-id="d41fe-106">Group Call Pickup is based on the Call Park application.</span></span> <span data-ttu-id="d41fe-107">グループ通話のピックアップを展開するときは、通話集配グループ番号として指定されている電話番号の範囲を使って、コールパークの軌道テーブルを構成します。</span><span class="sxs-lookup"><span data-stu-id="d41fe-107">When you deploy Group Call Pickup, you configure the call park orbit table with ranges of phone numbers that are designated as call pickup group numbers.</span></span> <span data-ttu-id="d41fe-108">ユーザーはこのグループ番号にダイヤルし、他のユーザーに着信している通話をピックアップします。</span><span class="sxs-lookup"><span data-stu-id="d41fe-108">These group numbers are the numbers that users dial to pick up calls that are ringing for another user.</span></span>

<span data-ttu-id="d41fe-109">コール パーク オービットの番号と同様に、通話ピックアップのグループ番号には、ユーザーや電話が割り当てられていない仮想の内線番号を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d41fe-109">Like call park orbit numbers, call pickup group numbers need to be virtual extensions that have no user or phone assigned to them.</span></span> <span data-ttu-id="d41fe-110">グループ通話のピックアップを展開する各フロントエンドプールには、1つ以上の通話ピックアップグループ番号が含まれていることがあります。</span><span class="sxs-lookup"><span data-stu-id="d41fe-110">Each Front End pool where you deploy Group Call Pickup can have one or more ranges of call pickup group numbers.</span></span> <span data-ttu-id="d41fe-111">グループ番号の範囲は、Lync Server 展開でグローバルに一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="d41fe-111">The group number ranges must be globally unique across the Lync Server deployment.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="d41fe-112">このセクション中</span><span class="sxs-lookup"><span data-stu-id="d41fe-112">In This Section</span></span>

  - [<span data-ttu-id="d41fe-113">Create or modify a Group Call Pickup number range in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d41fe-113">Create or modify a Group Call Pickup number range in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-group-call-pickup-number-range.md)

  - [<span data-ttu-id="d41fe-114">Lync Server 2013 でグループ通話の集配番号の範囲を削除する</span><span class="sxs-lookup"><span data-stu-id="d41fe-114">Delete a Group Call Pickup number range in Lync Server 2013</span></span>](lync-server-2013-delete-a-group-call-pickup-number-range.md)

<span data-ttu-id="d41fe-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d41fe-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

