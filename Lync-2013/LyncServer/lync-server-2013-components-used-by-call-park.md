---
title: 'Lync Server 2013: コール パークで使用されるコンポーネント'
description: 'Lync Server 2013: コールパークで使用されるコンポーネント。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components used by Call Park
ms:assetid: c7ffbee3-0ce1-48c0-bb56-af098b41d6d6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398824(v=OCS.15)
ms:contentKeyID: 48185374
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 285af316fa2d49e8bebf68e11de6d9526e12ae29
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398528"
---
# <a name="components-used-by-call-park-in-lync-server-2013"></a><span data-ttu-id="74594-103">Lync Server 2013 のコール パークで使用されるコンポーネント</span><span class="sxs-lookup"><span data-stu-id="74594-103">Components used by Call Park in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="74594-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="74594-104">

<span> </span></span></span>

<span data-ttu-id="74594-105">_**最終更新日:** 2012-09-13_</span><span class="sxs-lookup"><span data-stu-id="74594-105">_**Topic Last Modified:** 2012-09-13_</span></span>

<span data-ttu-id="74594-106">エンタープライズ Voip を展開すると、コールパークアプリケーションが自動的にインストールされます。</span><span class="sxs-lookup"><span data-stu-id="74594-106">The Call Park application is automatically installed when you deploy Enterprise Voice.</span></span> <span data-ttu-id="74594-107">音声ポリシーを構成して、コールパークを有効にします。</span><span class="sxs-lookup"><span data-stu-id="74594-107">You enable Call Park by configuring voice policy.</span></span> <span data-ttu-id="74594-108">次の Lync Server 2013 コンポーネントは、コールパークアプリケーションをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="74594-108">The following Lync Server 2013 components support the Call Park application:</span></span>

  - <span data-ttu-id="74594-109">**アプリケーションサービス**   アプリケーションサービスは、コールパークアプリケーションなどのユニファイドコミュニケーションアプリケーションを展開、ホスティング、および管理するためのプラットフォームを提供します。</span><span class="sxs-lookup"><span data-stu-id="74594-109">**Application service**   Application service provides a platform for deploying, hosting, and managing unified communications applications, such as the Call Park application.</span></span> <span data-ttu-id="74594-110">アプリケーションサービスは、フロントエンドプールのすべてのフロントエンドサーバーと、すべての Standard Edition サーバーに自動的にインストールされます。</span><span class="sxs-lookup"><span data-stu-id="74594-110">Application service is automatically installed on every Front End Server in a Front End pool and on every Standard Edition server.</span></span>

  - <span data-ttu-id="74594-111">**コールパークアプリケーション**   コールパークアプリケーションは、アプリケーションサービスによってホストされるユニファイドコミュニケーションアプリケーションの1つです。</span><span class="sxs-lookup"><span data-stu-id="74594-111">**Call Park application**   The Call Park application is one of the unified communications applications that are hosted by Application service.</span></span> <span data-ttu-id="74594-112">エンタープライズボイスの展開時に自動的に含まれます。</span><span class="sxs-lookup"><span data-stu-id="74594-112">It is included automatically when you deploy Enterprise Voice.</span></span> <span data-ttu-id="74594-113">[パークパーク] を選び、通話を取得して、通話パークの orbits を管理します。</span><span class="sxs-lookup"><span data-stu-id="74594-113">Call Park parks and retrieves calls and manages call park orbits.</span></span>

  - <span data-ttu-id="74594-114">**音楽-保留中-ファイル**   音楽が有効になっている場合は、通話の保留中に音楽ファイルが再生されます。</span><span class="sxs-lookup"><span data-stu-id="74594-114">**Music-on hold-file**   If music in enabled, the music file is played while a call is parked.</span></span> <span data-ttu-id="74594-115">既定の音楽ファイルは、コールパークアプリケーションがインストールされているときに含まれます。</span><span class="sxs-lookup"><span data-stu-id="74594-115">A default music file is included when the Call Park application is installed.</span></span>

  - <span data-ttu-id="74594-116">**ファイルストア**   コールパークアプリケーションは、カスタムオーディオファイルを保持するためにファイルストアを使用します。</span><span class="sxs-lookup"><span data-stu-id="74594-116">**File Store**   The Call Park application uses File Store to hold custom audio files.</span></span>

  - <span data-ttu-id="74594-117">**Lync Server コントロールパネル**   Lync Server コントロールパネルを使用して、コールパークの軌道の表を構成し、ユーザーに対してコールパークを有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="74594-117">**Lync Server Control Panel**   You can use Lync Server Control Panel to configure the call park orbit table and to enable Call Park for users.</span></span>

  - <span data-ttu-id="74594-118">**Lync Server 管理シェル**   すべてのコールパークアプリケーション構成は、Lync Server 管理シェルコマンドレットを使用して実行できます。</span><span class="sxs-lookup"><span data-stu-id="74594-118">**Lync Server Management Shell**   All Call Park application configuration can be performed by using Lync Server Management Shell cmdlets.</span></span>

<span data-ttu-id="74594-119"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="74594-119"></div>

<span> </span>

</div>

</div>

</span></span></div>

