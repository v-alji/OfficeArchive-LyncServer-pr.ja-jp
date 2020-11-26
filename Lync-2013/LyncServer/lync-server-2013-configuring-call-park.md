---
title: 'Lync Server 2013: コール パークの構成'
description: 'Lync Server 2013: コールパークの構成'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Call Park
ms:assetid: e4c5da53-7f6c-4535-bc9b-9da2026caec8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399014(v=OCS.15)
ms:contentKeyID: 48185732
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1d2708f26fae5706afc31aa195b9fdb82536247b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433249"
---
# <a name="configuring-call-park-in-lync-server-2013"></a><span data-ttu-id="6ac9b-103">Lync Server 2013 でのコール パークの構成</span><span class="sxs-lookup"><span data-stu-id="6ac9b-103">Configuring Call Park in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6ac9b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6ac9b-104">

<span> </span></span></span>

<span data-ttu-id="6ac9b-105">_**最終更新日:** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="6ac9b-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="6ac9b-106">コールパークエンタープライズボイスユーザーは、1つの電話から通話を保留にすることができます。通話を発信するには、任意の電話から内部番号 (通話パーク *軌道* と呼びます) をダイヤルする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6ac9b-106">Call Park enables an Enterprise Voice user to put a call on hold from one telephone and then retrieve the call later by dialing an internal number (known as a Call Park *orbit*) from any telephone.</span></span>

<span data-ttu-id="6ac9b-107">エンタープライズボイスの展開時に、コールパークで使用されるコンポーネントは、フロントエンドサーバーまたは Standard Edition サーバーに自動的にインストールされ、有効になります。</span><span class="sxs-lookup"><span data-stu-id="6ac9b-107">The components that Call Park uses are automatically installed and enabled on the Front End Server or Standard Edition server when you deploy Enterprise Voice.</span></span> <span data-ttu-id="6ac9b-108">ただし、ユーザーが使用できるようになる前に、コールパークを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6ac9b-108">However, you must configure Call Park before it is available to users.</span></span>

<span data-ttu-id="6ac9b-109">このセクションでは、コールパークの構成について説明します。</span><span class="sxs-lookup"><span data-stu-id="6ac9b-109">This section guides you through the configuration of Call Park.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="6ac9b-110">このセクション中</span><span class="sxs-lookup"><span data-stu-id="6ac9b-110">In This Section</span></span>

  - [<span data-ttu-id="6ac9b-111">Lync Server 2013 のコール パーク構成の前提条件とユーザー権限</span><span class="sxs-lookup"><span data-stu-id="6ac9b-111">Call Park configuration prerequisites and user rights in Lync Server 2013</span></span>](lync-server-2013-call-park-configuration-prerequisites-and-user-rights.md)

  - [<span data-ttu-id="6ac9b-112">Lync Server 2013 でのコールパークの展開プロセス</span><span class="sxs-lookup"><span data-stu-id="6ac9b-112">Deployment process for Call Park in Lync Server 2013</span></span>](lync-server-2013-deployment-process-for-call-park.md)

  - [<span data-ttu-id="6ac9b-113">Lync Server 2013 でのコール パーク オービット テーブルの構成</span><span class="sxs-lookup"><span data-stu-id="6ac9b-113">Configure the Call Park orbit table in Lync Server 2013</span></span>](lync-server-2013-configure-the-call-park-orbit-table.md)

  - [<span data-ttu-id="6ac9b-114">Lync Server 2013 でのコールパーク設定の構成</span><span class="sxs-lookup"><span data-stu-id="6ac9b-114">Configure Call Park settings in Lync Server 2013</span></span>](lync-server-2013-configure-call-park-settings.md)

  - [<span data-ttu-id="6ac9b-115">通話パークをカスタマイズする Lync Server 2013 の保留中の音楽</span><span class="sxs-lookup"><span data-stu-id="6ac9b-115">Customize Call Park music on hold in Lync Server 2013</span></span>](lync-server-2013-customize-call-park-music-on-hold.md)

  - [<span data-ttu-id="6ac9b-116">Lync Server 2013 のユーザーに対してコールパークを有効にする</span><span class="sxs-lookup"><span data-stu-id="6ac9b-116">Enable Call Park for users in Lync Server 2013</span></span>](lync-server-2013-enable-call-park-for-users.md)

  - [<span data-ttu-id="6ac9b-117">Lync Server 2013 でのコールパークの正規化ルールを確認する</span><span class="sxs-lookup"><span data-stu-id="6ac9b-117">Verify normalization rules for Call Park in Lync Server 2013</span></span>](lync-server-2013-verify-normalization-rules-for-call-park.md)

  - [<span data-ttu-id="6ac9b-118">省略Lync Server 2013 でのコールパークの展開を確認する</span><span class="sxs-lookup"><span data-stu-id="6ac9b-118">(Optional) Verify Call Park deployment in Lync Server 2013</span></span>](lync-server-2013-optional-verify-call-park-deployment.md)

<span data-ttu-id="6ac9b-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6ac9b-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

