---
title: 'Lync Server 2013: 音声番号の正規化とルーティングを検証する'
description: 'Lync Server 2013: 音声番号の正規化とルーティングを検証しています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Validating voice number normalization and routing
ms:assetid: a6a825c7-6928-4e80-b7e9-803b7f7ebd13
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720922(v=OCS.15)
ms:contentKeyID: 63969633
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5f28f679cbb991bdb90362eb61c9c7b68879791e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438625"
---
# <a name="validating-voice-number-normalization-and-routing-in-lync-server-2013"></a><span data-ttu-id="2a896-103">Lync Server 2013 での音声番号の正規化とルーティングの検証</span><span class="sxs-lookup"><span data-stu-id="2a896-103">Validating voice number normalization and routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2a896-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2a896-104">

<span> </span></span></span>

<span data-ttu-id="2a896-105">_**最終更新日:** 2014-05-19_</span><span class="sxs-lookup"><span data-stu-id="2a896-105">_**Topic Last Modified:** 2014-05-19_</span></span>

<span data-ttu-id="2a896-106">正しい番号の正規化とルーティングは、機能的なエンタープライズ Voip 環境で非常に重要です。</span><span class="sxs-lookup"><span data-stu-id="2a896-106">Correct number normalization and routing is very important for functional Enterprise Voice environment.</span></span> <span data-ttu-id="2a896-107">特に、プライベートブランチ exchange (PBX) から単体の Lync Server 環境に移行する場合、移行を成功させるためのキーの1つとして、既存のすべてのダイヤルルールを表示して文書化し、適切な正規化ルール、音声ポリシー、電話の使用状況、ルートを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="2a896-107">Especially during migrations from private branch exchange (PBX) to stand-alone Lync Server environment, one of the keys to successful migration is to reveal and document all existing dialing rules, and create appropriate normalization rules, voice policies, phone usages and routes.</span></span>

<span data-ttu-id="2a896-108">番号の正規化とルーティングは、移行時だけでなく、通常どおりにシステムの安定した操作を実行する場合にも重要です。</span><span class="sxs-lookup"><span data-stu-id="2a896-108">Validating number normalization and routing is important not only during migrations but also during normal, stable operation of the system.</span></span>

<span data-ttu-id="2a896-109">この検証は、lync server コントロールパネルを使用して、Lync Server のグローバル設定で公開された現在の正規化ルールのセットとの堅固なテストケースの開発を開始することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="2a896-109">We recommend conducting this validation daily by using the Lync Server Control Panel, starting with developing a robust set of test cases against the current set of normalization rules that were published in the Lync Server global settings.</span></span> <span data-ttu-id="2a896-110">これらのテストケースは、ダイヤルプランに加えられた不要な変更を強調表示するために、毎日実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a896-110">These test cases should be run daily to highlight any unwanted changes that were made and committed to the dial plan.</span></span>

<span data-ttu-id="2a896-111">Lync Server コントロールパネルは、音声ルーティングに関する構成情報の視覚化、テスト、変更、アーカイブ、共有にも役立ちます。また、エンタープライズのボイス番号正規化規則、ダイヤルプラン、音声ポリシー、ルートを変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="2a896-111">Lync Server Control Panel also helps you visualize, test, change, archive, and share configuration information about voice routing and in changing Enterprise Voice number normalization rules, dial plans, voice policy, and routes.</span></span> <span data-ttu-id="2a896-112">次の操作を実行するための追加機能が用意されています。</span><span class="sxs-lookup"><span data-stu-id="2a896-112">It has additional features for doing the following:</span></span>

  - <span data-ttu-id="2a896-113">システム間でのボイスルーティングデータのエクスポートとインポートまたはバックアップ。</span><span class="sxs-lookup"><span data-stu-id="2a896-113">Exporting and importing or backing up voice routing data between systems.</span></span>

  - <span data-ttu-id="2a896-114">ライブシステムにアップロードする前に構成の変更をテストする。</span><span class="sxs-lookup"><span data-stu-id="2a896-114">Testing configuration changes before uploading them to a live system.</span></span>

  - <span data-ttu-id="2a896-115">構成テストケースを作成し、実行して、そのデータを変更した後、展開されたシステムへの変更をコミットする前に、ルーティングの操作性を向上させることができます。</span><span class="sxs-lookup"><span data-stu-id="2a896-115">Creating and running configuration test cases to help ensure the usability of routing data after you make changes to it, but before committing them the changes to a deployed system.</span></span>

  - <span data-ttu-id="2a896-116">数値正規化ルール、位置情報プロファイル、音声ポリシー、および必要な正規表現を記述せずにデータをルーティングする。</span><span class="sxs-lookup"><span data-stu-id="2a896-116">Creating and changing number normalization rules, location profiles, voice policy, and routing data without writing the necessary regular expressions.</span></span>

  - <span data-ttu-id="2a896-117">Lync Server Phone Edition との互換性を保つために、位置情報プロファイルを分析します。</span><span class="sxs-lookup"><span data-stu-id="2a896-117">Analyzing a location profile for compatibility with the Lync Server Phone Edition.</span></span>

  - <span data-ttu-id="2a896-118">音声ルーティングテストの詳細については[、「Lync Server 2013 でのボイスルーティングのテスト」](lync-server-2013-test-voice-routing.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2a896-118">More information about voice routing tests can be found at [Test voice routing in Lync Server 2013](lync-server-2013-test-voice-routing.md)</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="2a896-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="2a896-119">See Also</span></span>


[<span data-ttu-id="2a896-120">Lync Server 2013 での音声ルーティングのテスト</span><span class="sxs-lookup"><span data-stu-id="2a896-120">Test voice routing in Lync Server 2013</span></span>](lync-server-2013-test-voice-routing.md)  
  

<span data-ttu-id="2a896-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2a896-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

