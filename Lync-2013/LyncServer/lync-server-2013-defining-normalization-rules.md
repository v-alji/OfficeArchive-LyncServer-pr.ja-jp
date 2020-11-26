---
title: 'Lync Server 2013: 正規化ルールの定義'
description: 'Lync Server 2013: 正規化ルールの定義'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Defining normalization rules
ms:assetid: ed31d56c-00b5-4f72-bd9f-beb4100d441f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399071(v=OCS.15)
ms:contentKeyID: 48185741
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3a123e17b1d3256781ff34e4cade2b344ba8fe14
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430995"
---
# <a name="defining-normalization-rules-in-lync-server-2013"></a><span data-ttu-id="b46af-103">Lync Server 2013 の正規化ルールの定義</span><span class="sxs-lookup"><span data-stu-id="b46af-103">Defining normalization rules in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b46af-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b46af-104">

<span> </span></span></span>

<span data-ttu-id="b46af-105">_**最終更新日:** 2014-04-22_</span><span class="sxs-lookup"><span data-stu-id="b46af-105">_**Topic Last Modified:** 2014-04-22_</span></span>

<span data-ttu-id="b46af-106">Lync Server 2013 正規化ルールは、ダイヤルした電話番号を E-164 形式に変換するために .NET Framework の正規表現を使用します。つまり、正規化ルールは、ユーザーがダイヤルした電話番号を取得し、その番号を Lync Server が内部的に使用する形式に変換します。</span><span class="sxs-lookup"><span data-stu-id="b46af-106">Lync Server 2013 normalization rules use .NET Framework regular expressions to translate dialed phone numbers to E.164 format; in other words, normalization rules take the phone number dialed by a user and convert that number to the format used internally by Lync Server.</span></span> <span data-ttu-id="b46af-107">各ダイヤル プランには、正規化ルールを 1 つ以上割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="b46af-107">Each dial plan must be assigned one or more normalization rules.</span></span>

<span data-ttu-id="b46af-108">正規化ルールの詳細については、計画ドキュメントの「 [Lync Server 2013 でのダイヤルプランと正規化ルール](lync-server-2013-dial-plans-and-normalization-rules.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b46af-108">For details about normalization rules, see [Dial plans and normalization rules in Lync Server 2013](lync-server-2013-dial-plans-and-normalization-rules.md) in the Planning documentation.</span></span>

<span data-ttu-id="b46af-109">正規表現の記述方法の詳細については、「」の「.NET Framework の正規表現」を参照してください [https://go.microsoft.com/fwlink/p/?linkId=140927](https://go.microsoft.com/fwlink/p/?linkid=140927) 。</span><span class="sxs-lookup"><span data-stu-id="b46af-109">For details about how to write regular expressions, see ".NET Framework Regular Expressions" at [https://go.microsoft.com/fwlink/p/?linkId=140927](https://go.microsoft.com/fwlink/p/?linkid=140927).</span></span>

<span data-ttu-id="b46af-110">正規化ルールを定義または編集するには、次のいずれかの方法を使用できます。</span><span class="sxs-lookup"><span data-stu-id="b46af-110">You can use either of the following methods to define or edit a normalization rule:</span></span>

  - <span data-ttu-id="b46af-111">[ **正規化ルールのビルド** ] ツールを使用して、先頭の数字、長さ、削除する数字、追加する数字の値を指定します。これにより、Lync Server コントロールパネルで、対応する一致パターンと翻訳ルールを生成できます。</span><span class="sxs-lookup"><span data-stu-id="b46af-111">Use the **Build a Normalization Rule** tool to specify values for the starting digits, length, digits to remove and digits to add, and then let Lync Server Control Panel generate the corresponding matching pattern and translation rule for you.</span></span>

  - <span data-ttu-id="b46af-112">一致するパターンと翻訳ルールを定義するために、正規表現を手動で記述します。</span><span class="sxs-lookup"><span data-stu-id="b46af-112">Write regular expressions manually to define the matching pattern and translation rule.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="b46af-113">このセクション中</span><span class="sxs-lookup"><span data-stu-id="b46af-113">In This Section</span></span>

  - [<span data-ttu-id="b46af-114">「Lync Server 2013 で正規化ルールを作成する」を使用して正規化ルールを作成または変更する</span><span class="sxs-lookup"><span data-stu-id="b46af-114">Create or modify a normalization rule by using Build a Normalization Rule in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-normalization-rule-by-using-build-a-normalization-rule.md)

  - [<span data-ttu-id="b46af-115">Lync Server 2013 での手動による正規化ルールの作成または変更</span><span class="sxs-lookup"><span data-stu-id="b46af-115">Create or modify a normalization rule manually in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-normalization-rule-manually.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="b46af-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="b46af-116">See Also</span></span>


[<span data-ttu-id="b46af-117">Lync Server 2013 でダイヤルプランを作成する</span><span class="sxs-lookup"><span data-stu-id="b46af-117">Create a dial plan in Lync Server 2013</span></span>](lync-server-2013-create-a-dial-plan.md)  
[<span data-ttu-id="b46af-118">Lync Server 2013 でのダイヤル プランの変更</span><span class="sxs-lookup"><span data-stu-id="b46af-118">Modify a dial plan in Lync Server 2013</span></span>](lync-server-2013-modify-a-dial-plan.md)  
  

<span data-ttu-id="b46af-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b46af-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

