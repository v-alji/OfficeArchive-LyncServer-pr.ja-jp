---
title: プールからのフロントエンド サーバーの削除
description: プールからフロントエンドサーバーを削除します。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove a Front End Server from a pool
ms:assetid: 767225c9-7c0b-4d54-a407-d77134ba2abe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688095(v=OCS.15)
ms:contentKeyID: 49733694
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 45560a6f43288b47c0f85f880a190e31f2c8c04d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440326"
---
# <a name="remove-a-front-end-server-from-a-pool"></a><span data-ttu-id="a3f47-103">プールからのフロントエンド サーバーの削除</span><span class="sxs-lookup"><span data-stu-id="a3f47-103">Remove a Front End Server from a pool</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a3f47-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a3f47-104">

<span> </span></span></span>

<span data-ttu-id="a3f47-105">_**最終更新日:** 2012-10-04_</span><span class="sxs-lookup"><span data-stu-id="a3f47-105">_**Topic Last Modified:** 2012-10-04_</span></span>

<span data-ttu-id="a3f47-106">Microsoft Lync Server 2010 Enterprise Edition のフロントエンドサーバーは、スタンドアロンコンピューターとして存在することはできません。</span><span class="sxs-lookup"><span data-stu-id="a3f47-106">The Microsoft Lync Server 2010 Enterprise Edition Front End Server cannot exist as a stand-alone computer.</span></span> <span data-ttu-id="a3f47-107">プールに1台のコンピュータしかない場合でも、フロントエンドプールとして定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a3f47-107">It must be defined as a Front End pool, even if there is only a single computer in the pool.</span></span>

<span data-ttu-id="a3f47-108">このトピックでは、既存のフロントエンドプールから個々のフロントエンドサーバーを削除する手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="a3f47-108">This topic guides you through the process of removing an individual Front End Server from an existing Front End pool.</span></span> <span data-ttu-id="a3f47-109">フロントエンドサーバーがプール内の最後のサーバーである場合、またはプールを完全に削除する場合は、「 [フロントエンドプールまたは Standard Edition サーバーを削除](remove-front-end-pool-or-standard-edition-server.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a3f47-109">If the Front End Server is the last server in the pool or if you are removing the pool completely, see [Remove Front End pool or Standard Edition server](remove-front-end-pool-or-standard-edition-server.md).</span></span> <span data-ttu-id="a3f47-110">フロントエンドプールを削除する前に、個々のフロントエンドサーバーを削除する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="a3f47-110">There is no need to remove the individual Front End Servers before you remove the Front End pool.</span></span> <span data-ttu-id="a3f47-111">プールを削除すると、各フロントエンドサーバーが削除されます。</span><span class="sxs-lookup"><span data-stu-id="a3f47-111">When you remove the pool, you remove each Front End Server.</span></span>

<div>

## <a name="to-remove-a-front-end-server-from-a-pool"></a><span data-ttu-id="a3f47-112">プールからフロントエンドサーバーを削除するには</span><span class="sxs-lookup"><span data-stu-id="a3f47-112">To remove a Front End Server from a pool</span></span>

1.  <span data-ttu-id="a3f47-113">Lync Server 2013 フロントエンドサーバーを開き、[トポロジビルダー] を開きます。</span><span class="sxs-lookup"><span data-stu-id="a3f47-113">Open the Lync Server 2013 Front End Server, open Topology Builder.</span></span>

2.  <span data-ttu-id="a3f47-114">Lync Server 2010 ノードに移動します。</span><span class="sxs-lookup"><span data-stu-id="a3f47-114">Navigate to the Lync Server 2010 node.</span></span>

3.  <span data-ttu-id="a3f47-115">[ **Enterprise Edition のフロントエンドプール**] を展開し、削除するフロントエンドサーバーでフロントエンドプールを展開して、削除するフロントエンドサーバーを右クリックし、[ **削除**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a3f47-115">Expand **Enterprise Edition Front End pools**, expand the Front End pool with the Front End Server that you want to remove, right-click the Front End Server that you want to remove, and then click **Delete**.</span></span>

<span data-ttu-id="a3f47-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a3f47-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

