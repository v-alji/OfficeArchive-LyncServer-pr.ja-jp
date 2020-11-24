---
title: 'Lync Server 2013: コールパークの正規化ルールを確認する'
description: 'Lync Server 2013: コールパークの正規化ルールを確認します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verify normalization rules for Call Park
ms:assetid: deaa170f-041e-45cb-8eab-f02931ab541e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398981(v=OCS.15)
ms:contentKeyID: 48185646
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2ac4c15091141e3069e7b77533d0e4148459f570
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399759"
---
# <a name="verify-normalization-rules-for-call-park-in-lync-server-2013"></a><span data-ttu-id="3c544-103">Lync Server 2013 でのコールパークの正規化ルールを確認する</span><span class="sxs-lookup"><span data-stu-id="3c544-103">Verify normalization rules for Call Park in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3c544-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3c544-104">

<span> </span></span></span>

<span data-ttu-id="3c544-105">_**最終更新日:** 2012-09-11_</span><span class="sxs-lookup"><span data-stu-id="3c544-105">_**Topic Last Modified:** 2012-09-11_</span></span>

<span data-ttu-id="3c544-106">コールパーク orbits は正規化されていない必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c544-106">Call Park orbits must not be normalized.</span></span> <span data-ttu-id="3c544-107">ダイヤル プランでオービット番号が正規化されていないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="3c544-107">Check your dial plans to be sure that your orbit numbers are not normalized.</span></span> <span data-ttu-id="3c544-108">追加の正規化ルールを作成して、orbits が正規化されないようにする必要がある場合は、「 [Lync Server 2013 でダイヤルプランを作成](lync-server-2013-create-a-dial-plan.md) する」の手順に従って、新しい正規化ルールを定義します。これにより、 **一致するパターン** は、オービット範囲と **翻訳パターン** の **$1** を識別します。</span><span class="sxs-lookup"><span data-stu-id="3c544-108">If you must create an additional normalization rule to prevent your orbits from being normalized, follow the procedure in [Create a dial plan in Lync Server 2013](lync-server-2013-create-a-dial-plan.md) to define a new normalization rule, so that **Pattern to match** identifies the orbit range and **Translation pattern** is **$1**.</span></span> <span data-ttu-id="3c544-109">たとえば、Call パークの軌道範囲が7000–7999の場合、 **照合するパターン** は **^ (7 \\ d {3} ) $** で、 **翻訳パターン** は **$1** です。</span><span class="sxs-lookup"><span data-stu-id="3c544-109">For example, if your Call Park orbit range is 7000 – 7999, the **Pattern to match** is **^(7\\d{3})$** and **Translation pattern** is **$1**.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="3c544-110">ダイヤル プランの既定の正規化ルールに <STRONG>^(\d\*)</STRONG> が含まれていないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="3c544-110">Be sure that the default normalization rule in your dial plans does not contain <STRONG>^(\d\*)</STRONG>.</span></span> <span data-ttu-id="3c544-111">そうしないと、Call パークの正規化ルールは実行されません。</span><span class="sxs-lookup"><span data-stu-id="3c544-111">Otherwise, your Call Park normalization rule will never run.</span></span>



</div>

<div>

## <a name="see-also"></a><span data-ttu-id="3c544-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="3c544-112">See Also</span></span>


[<span data-ttu-id="3c544-113">Lync Server 2013 でダイヤルプランを作成する</span><span class="sxs-lookup"><span data-stu-id="3c544-113">Create a dial plan in Lync Server 2013</span></span>](lync-server-2013-create-a-dial-plan.md)  
  

<span data-ttu-id="3c544-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3c544-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

