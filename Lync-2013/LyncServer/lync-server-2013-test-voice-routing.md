---
title: 'Lync Server 2013: 音声ルーティングのテスト'
description: 'Lync Server 2013: ボイスルーティングをテストします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test voice routing
ms:assetid: d3aae909-fef6-440f-b144-0b62dc82bf5d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398915(v=OCS.15)
ms:contentKeyID: 48185444
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e641e68ccecfe7d1d0e64dc9eb1b1f5016e68e22
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441152"
---
# <a name="test-voice-routing-in-lync-server-2013"></a><span data-ttu-id="e0195-103">Lync Server 2013 での音声ルーティングのテスト</span><span class="sxs-lookup"><span data-stu-id="e0195-103">Test voice routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e0195-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e0195-104">

<span> </span></span></span>

<span data-ttu-id="e0195-105">_**最終更新日:** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="e0195-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<span data-ttu-id="e0195-106">Lync Server コントロールパネルの [ **ボイスルーティングのテスト** ] タブを使用して、テストケースのシナリオを構成することができます。</span><span class="sxs-lookup"><span data-stu-id="e0195-106">You can use the Lync Server Control Panel **Test Voice Routing** tab to configure test case scenarios.</span></span> <span data-ttu-id="e0195-107">テストケースを定義するには、指定した電話番号をテストするためのダイヤルプラン、音声ポリシー、PSTN 使用量、および音声ルートを指定します。</span><span class="sxs-lookup"><span data-stu-id="e0195-107">To define a test case, you specify the dial plan, voice policy, PSTN usage, and voice route against which to test a specified phone number.</span></span>

<span data-ttu-id="e0195-108">実際にボイスルーティング構成を展開する前に、さまざまな電話番号でテストして、期待どおりの結果が得られていることを確認することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e0195-108">Before you actually deploy your voice routing configuration, we recommend that you test it on various phone numbers to make sure that the results are what you're expecting.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="e0195-109">[ <STRONG>テストケースのエクスポート</STRONG> ] と [ <STRONG>テストケースのインポート</STRONG> ] コマンドを使用して、ボイスルーティングテストケースを保存し、別のコンピューターで使用するためにインポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="e0195-109">You can use the <STRONG>Export test cases</STRONG> and <STRONG>Import test cases</STRONG> commands to save voice routing test cases and import them for use on another computer.</span></span>



</div>

<div>


> [!WARNING]  
> <span data-ttu-id="e0195-110">ダイヤルプラン、ボイスポリシー、ボイスルート、または電話の使用状況など、音声ルーティング構成の一部を削除する場合は、ボイスルーティングテストケースを確認して更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0195-110">If you delete any part of your voice routing configuration, such as a dial plan, voice policy, voice route, or phone usage, you should review and update your voice routing test cases.</span></span> <span data-ttu-id="e0195-111">Lync Server コントロールパネルでは、設定が変更されたために無効になったケースをテストすることはできません。</span><span class="sxs-lookup"><span data-stu-id="e0195-111">The Lync Server Control Panel will not alert you to test cases that are no longer valid due to changed configurations.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="e0195-112">このセクション中</span><span class="sxs-lookup"><span data-stu-id="e0195-112">In This Section</span></span>

  - [<span data-ttu-id="e0195-113">Lync Server 2013 での音声ルーティング テスト ケースの作成</span><span class="sxs-lookup"><span data-stu-id="e0195-113">Create a voice routing test case in Lync Server 2013</span></span>](lync-server-2013-create-a-voice-routing-test-case.md)

  - [<span data-ttu-id="e0195-114">Lync Server 2013 での音声ルーティング テスト ケースのエクスポート</span><span class="sxs-lookup"><span data-stu-id="e0195-114">Export voice routing test cases in Lync Server 2013</span></span>](lync-server-2013-export-voice-routing-test-cases.md)

  - [<span data-ttu-id="e0195-115">Lync Server 2013 音声ルーティング テスト ケースのインポート</span><span class="sxs-lookup"><span data-stu-id="e0195-115">Import voice routing test cases in Lync Server 2013</span></span>](lync-server-2013-import-voice-routing-test-cases.md)

  - [<span data-ttu-id="e0195-116">Lync Server 2013 での音声ルーティング テストの実行</span><span class="sxs-lookup"><span data-stu-id="e0195-116">Running voice routing tests in Lync Server 2013</span></span>](lync-server-2013-running-voice-routing-tests.md)

<span data-ttu-id="e0195-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e0195-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

