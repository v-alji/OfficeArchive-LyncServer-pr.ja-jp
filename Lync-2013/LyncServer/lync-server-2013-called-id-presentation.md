---
title: 'Lync Server 2013: ID プレゼンテーションと呼ばれる'
description: 'Lync Server 2013: ID プレゼンテーションと呼ばれました。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Called ID presentation
ms:assetid: cf6c6af5-3418-411e-a50b-7a9cf8e100d4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721892(v=OCS.15)
ms:contentKeyID: 49733826
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6b438c7c19bc3c4ad641a8b9f8dac319c9fc2b1c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435650"
---
# <a name="called-id-presentation-in-lync-server-2013"></a><span data-ttu-id="b127f-103">Lync Server 2013 の ID プレゼンテーション</span><span class="sxs-lookup"><span data-stu-id="b127f-103">Called ID presentation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b127f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b127f-104">

<span> </span></span></span>

<span data-ttu-id="b127f-105">_**最終更新日:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="b127f-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="b127f-106">Lync Server 2010 を使用すると、通話先の国の電話番号 (電話番号) を、トランクのピアによって要求されるローカルのダイヤル形式 (関連付けられているゲートウェイ、構内交換機 (PBX)、SIP トランクなど) に変換することができます。</span><span class="sxs-lookup"><span data-stu-id="b127f-106">With Lync Server 2010, the called party’s phone number (that is, the phone number called) can be translated from E.164 format to the local dialing format that is required by the trunk peer (that is, the associated gateway, private branch exchange (PBX), or SIP trunk).</span></span> <span data-ttu-id="b127f-107">これを行うためには、トランク ピアへのルーティングの前に要求 URI を変換する変換ルールを 1 つ以上定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b127f-107">To do this, you must define one or more translation rules to translate the Request URI before routing it to the trunk peer.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="b127f-108">エンタープライズボイストランク構成に1つまたは複数の翻訳ルールを関連付ける機能は、トランクピアでの翻訳ルールの設定の <EM>代わり</EM> として使用することを目的としています。</span><span class="sxs-lookup"><span data-stu-id="b127f-108">The ability to associate one or more translation rules with an Enterprise Voice trunk configuration is intended to be used as an <EM>alternative</EM> to configuring translation rules on the trunk peer.</span></span> <span data-ttu-id="b127f-109">2つのルールが競合する可能性があるため、トランクピアで翻訳ルールを構成している場合、翻訳ルールをエンタープライズボイストランク構成に関連付けないでください。</span><span class="sxs-lookup"><span data-stu-id="b127f-109">Do not associate translation rules with an Enterprise Voice trunk configuration if you have configured translation rules on the trunk peer because the two rules might conflict.</span></span>



</div>

<span data-ttu-id="b127f-110">翻訳ルールを作成または変更するには、次のいずれかの方法を使用できます。</span><span class="sxs-lookup"><span data-stu-id="b127f-110">You can use either of the following methods to create or modify a translation rule:</span></span>

  - <span data-ttu-id="b127f-111">[ **翻訳ルールの作成** ] ツールを使用して、開始番号、長さ、削除する数字の値、追加する数字を指定します。次に、Lync Server コントロールパネルで、対応する一致パターンと翻訳ルールを生成できます。</span><span class="sxs-lookup"><span data-stu-id="b127f-111">Use the **Build a Translation Rule** tool to specify values for the starting digits, length, digits to remove and digits to add, and then let Lync Server Control Panel generate the corresponding matching pattern and translation rule for you.</span></span>

  - <span data-ttu-id="b127f-112">一致するパターンと翻訳ルールを定義するために、正規表現を手動で記述します。</span><span class="sxs-lookup"><span data-stu-id="b127f-112">Write regular expressions manually to define the matching pattern and translation rule.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b127f-113">正規表現の記述方法については、「.NET Framework の正規表現」を参照してください <A href="https://go.microsoft.com/fwlink/p/?linkid=140927">https://go.microsoft.com/fwlink/p/?linkId=140927</A> 。</span><span class="sxs-lookup"><span data-stu-id="b127f-113">For information about how to write regular expressions, see ".NET Framework Regular Expressions" at <A href="https://go.microsoft.com/fwlink/p/?linkid=140927">https://go.microsoft.com/fwlink/p/?linkId=140927</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="b127f-114">このセクション中</span><span class="sxs-lookup"><span data-stu-id="b127f-114">In This Section</span></span>

  - [<span data-ttu-id="b127f-115">Lync Server 2013 の翻訳ルールの作成ツールを使用して、翻訳ルールを作成または変更する</span><span class="sxs-lookup"><span data-stu-id="b127f-115">Create or modify a translation rule by using the Build a Translation Rule tool in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-translation-rule-by-using-the-build-a-translation-rule-tool.md)

  - [<span data-ttu-id="b127f-116">Lync Server 2013 で翻訳ルールを手動で作成または変更する</span><span class="sxs-lookup"><span data-stu-id="b127f-116">Create or modify a translation rule manually in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-translation-rule-manually.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="b127f-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="b127f-117">See Also</span></span>


[<span data-ttu-id="b127f-118">Lync Server 2013 での発信者番号通知のプレゼンテーション</span><span class="sxs-lookup"><span data-stu-id="b127f-118">Caller ID presentation in Lync Server 2013</span></span>](lync-server-2013-caller-id-presentation.md)  
  

<span data-ttu-id="b127f-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b127f-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

