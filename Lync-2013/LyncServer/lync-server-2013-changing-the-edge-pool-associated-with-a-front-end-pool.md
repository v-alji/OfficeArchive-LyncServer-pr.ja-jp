---
title: 'Lync Server 2013: フロント エンド プールに関連付けられたエッジ プールの変更'
description: 'Lync Server 2013: フロントエンドプールに関連付けられているエッジプールを変更します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Changing the Edge pool associated with a Front End pool
ms:assetid: 369468c7-2c0b-48cc-bbc3-825dad7b85aa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688023(v=OCS.15)
ms:contentKeyID: 49733613
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ab22ba35420341e291d51a1ff012459840e63a56
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435048"
---
# <a name="changing-the-edge-pool-associated-with-a-front-end-pool-in-lync-server-2013"></a><span data-ttu-id="67bd4-103">Lync Server 2013 でのフロント エンド プールに関連付けられたエッジ プールの変更</span><span class="sxs-lookup"><span data-stu-id="67bd4-103">Changing the Edge pool associated with a Front End pool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="67bd4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="67bd4-104">

<span> </span></span></span>

<span data-ttu-id="67bd4-105">_**最終更新日:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="67bd4-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="67bd4-106">エッジプールがダウンしていても、同じサイトのフロントエンドプールがまだ実行されている場合は、失敗したエッジプールが復元されるまで、別のサイトでエッジプールを使用するようにフロントエンドプールを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="67bd4-106">If an Edge pool goes down but the Front End pool at the same site is still running, you will need to set the Front End pool to use an Edge pool at a different site until the failed Edge pool is restored.</span></span>

<div>

## <a name="changing-the-edge-pool-associated-with-a-front-end-pool"></a><span data-ttu-id="67bd4-107">フロントエンドプールに関連付けられているエッジプールの変更</span><span class="sxs-lookup"><span data-stu-id="67bd4-107">Changing the Edge Pool Associated with a Front End Pool</span></span>

1.  <span data-ttu-id="67bd4-108">[Topology Builder] で、変更する必要があるフロントエンドプールの名前に移動します。</span><span class="sxs-lookup"><span data-stu-id="67bd4-108">In Topology Builder, navigate to the name of the Front End pool you need to change.</span></span>

2.  <span data-ttu-id="67bd4-109">プールを右クリックし、[プロパティの **編集**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="67bd4-109">Right-click the pool, and then click **Edit Properties**.</span></span>

3.  <span data-ttu-id="67bd4-110">[ **関連付け** ] セクションの [ **Edge プールの関連付け (メディアコンポーネントの場合)**] で、ドロップダウンボックスを使用して、このフロントエンドプールを関連付けるエッジプールを選択します。</span><span class="sxs-lookup"><span data-stu-id="67bd4-110">In the **Associations** section, under **Associate Edge Pool (for media components)**, use the drop down box to select the Edge pool you want to associate this Front End pool with.</span></span>

4.  <span data-ttu-id="67bd4-111">**[OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="67bd4-111">Click **OK**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="67bd4-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="67bd4-112">See Also</span></span>


[<span data-ttu-id="67bd4-113">Lync Server 2013 でのエッジ サーバーの障害復旧</span><span class="sxs-lookup"><span data-stu-id="67bd4-113">Edge Server disaster recovery in Lync Server 2013</span></span>](lync-server-2013-edge-server-disaster-recovery.md)  
  

<span data-ttu-id="67bd4-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="67bd4-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

