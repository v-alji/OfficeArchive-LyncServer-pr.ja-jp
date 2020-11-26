---
title: 'Lync Server 2013: 変換ルールの定義'
description: 'Lync Server 2013: 翻訳ルールを定義しています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Defining translation rules
ms:assetid: 4f6b975a-77e6-474c-9171-b139d84138c2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398322(v=OCS.15)
ms:contentKeyID: 48184093
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c0c59225c8dc74d7d97bf3536c7b7073bc977925
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430911"
---
# <a name="defining-translation-rules-in-lync-server-2013"></a><span data-ttu-id="a88a3-103">Lync Server 2013 での変換ルールの定義</span><span class="sxs-lookup"><span data-stu-id="a88a3-103">Defining translation rules in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a88a3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a88a3-104">

<span> </span></span></span>

<span data-ttu-id="a88a3-105">_**最終更新日:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="a88a3-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="a88a3-106">Lync Server 2013 エンタープライズボイスは、形式が164で正規化された電話番号に基づいて、通話をルーティングします。</span><span class="sxs-lookup"><span data-stu-id="a88a3-106">Lync Server 2013 Enterprise Voice routes calls based on phone numbers normalized to E.164 format.</span></span> <span data-ttu-id="a88a3-107">つまり、電話番号参照 (RNL) を実行する目的で、すべてのダイヤルされた文字列を E-164 形式に正規化して、一致する SIP URI に翻訳することができます。</span><span class="sxs-lookup"><span data-stu-id="a88a3-107">This means that all dialed strings must be normalized to E.164 format for the purpose of performing reverse number lookup (RNL) so they can be translated to their matching SIP URI.</span></span> <span data-ttu-id="a88a3-108">Lync Server 2013 には、呼び出された ID と発信者番号通知のプレゼンテーションを操作する機能が用意されています。</span><span class="sxs-lookup"><span data-stu-id="a88a3-108">Lync Server 2013 provides the ability to manipulate the called ID and the caller ID presentation.</span></span>

<span data-ttu-id="a88a3-109">このセクションでは、呼び出された ID と発信者番号を操作する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a88a3-109">This section discusses how to manipulate the called ID and caller ID.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="a88a3-110">このセクション中</span><span class="sxs-lookup"><span data-stu-id="a88a3-110">In This Section</span></span>

  - [<span data-ttu-id="a88a3-111">Lync Server 2013 での発信者番号通知のプレゼンテーション</span><span class="sxs-lookup"><span data-stu-id="a88a3-111">Caller ID presentation in Lync Server 2013</span></span>](lync-server-2013-caller-id-presentation.md)

  - [<span data-ttu-id="a88a3-112">Lync Server 2013 の ID プレゼンテーション</span><span class="sxs-lookup"><span data-stu-id="a88a3-112">Called ID presentation in Lync Server 2013</span></span>](lync-server-2013-called-id-presentation.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="a88a3-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="a88a3-113">See Also</span></span>


[<span data-ttu-id="a88a3-114">Lync Server 2013 の正規化ルールの定義</span><span class="sxs-lookup"><span data-stu-id="a88a3-114">Defining normalization rules in Lync Server 2013</span></span>](lync-server-2013-defining-normalization-rules.md)  
  

<span data-ttu-id="a88a3-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a88a3-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

