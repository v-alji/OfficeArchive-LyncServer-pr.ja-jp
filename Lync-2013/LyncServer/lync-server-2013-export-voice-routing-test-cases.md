---
title: 'Lync Server 2013: 音声ルーティング テスト ケースのエクスポート'
description: 'Lync Server 2013: ボイスルーティングテストケースをエクスポートします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Export voice routing test cases
ms:assetid: 489ac472-1a35-4755-b390-48f7cdf31e94
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425957(v=OCS.15)
ms:contentKeyID: 48184050
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 934bd183a17c46cf82fe5bc04faaa55a9bbe4731
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428350"
---
# <a name="export-voice-routing-test-cases-in-lync-server-2013"></a><span data-ttu-id="41499-103">Lync Server 2013 での音声ルーティング テスト ケースのエクスポート</span><span class="sxs-lookup"><span data-stu-id="41499-103">Export voice routing test cases in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="41499-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="41499-104">

<span> </span></span></span>

<span data-ttu-id="41499-105">_**最終更新日:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="41499-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="41499-106">テストケースは、組織内のボイスルートをテストするための手段を提供します。ダイヤルする番号や、使用するダイヤルプランや音声ポリシーなどを定義します。これらの条件が満たされた場合は、指定した電話番号が PSTN ネットワークに正常にルーティングされることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="41499-106">Test cases provide a way for you to test voice routes in your organization: you define such things as the number to be dialed and the dial plan and voice policy to be employed, and Lync Server can then verify that, given those conditions, the supplied number can successfully be routed to the PSTN network.</span></span>

<span data-ttu-id="41499-107">Lync Server コントロールパネルを使用して作成できるテストケースは、通常、ケースが最初に作成されて実行されたサーバーにのみ保存されます。</span><span class="sxs-lookup"><span data-stu-id="41499-107">Test cases, which can be created by using Lync Server Control Panel, are typically saved only on the server where the case was originally created and run.</span></span> <span data-ttu-id="41499-108">ただし、これらのテストケースは XML ファイルとしてエクスポートし、他のサーバーにインポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="41499-108">However, these test cases can be exported as XML files (with the .vtest extension) and then imported on other servers.</span></span> <span data-ttu-id="41499-109">これにより、トポロジ内のさまざまな場所にあるさまざまなコンピューターで同じテストを実行できます。</span><span class="sxs-lookup"><span data-stu-id="41499-109">This enables you to run the same tests on different computers located at different points in your topology.</span></span>

<div>

## <a name="to-export-a-voice-routing-test-case"></a><span data-ttu-id="41499-110">ボイスルーティングテストケースをエクスポートするには</span><span class="sxs-lookup"><span data-stu-id="41499-110">To export a voice routing test case</span></span>

1.  <span data-ttu-id="41499-111">Lync Server コントロールパネルで、[ **音声ルーティング** ] をクリックし、[ **音声ルーティングのテスト**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="41499-111">In Lync Server Control Panel, click **Voice Routing** and then click **Test Voice Routing**.</span></span>

2.  <span data-ttu-id="41499-112">[ **テスト用のボイスルーティング** ] タブで、エクスポートするテストケース (またはテストケース) を選択します。</span><span class="sxs-lookup"><span data-stu-id="41499-112">On the **Test Voice Routing** tab, select the test case (or test cases) to be exported.</span></span> <span data-ttu-id="41499-113">複数のテストケースを選択するには、エクスポートする最初のケースをクリックして、Ctrl キーを押しながら、エクスポートする追加のケースを選択します。</span><span class="sxs-lookup"><span data-stu-id="41499-113">To select multiple test cases, click the first case to be exported, then hold down the Ctrl key and select the additional cases to be exported.</span></span>

3.  <span data-ttu-id="41499-114">[ **アクション**] をクリックし、[ **テストケースのエクスポート**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="41499-114">Click **Action**, then click **Export test cases**.</span></span>

4.  <span data-ttu-id="41499-115">[名前 **を付けて保存** ] ダイアログボックスで、エクスポートされたテストケースを保存するフォルダーを選択し、結果の XML ファイルの名前を [ **ファイル名** ] ボックスに入力します。</span><span class="sxs-lookup"><span data-stu-id="41499-115">In the **Save As** dialog box, select a folder to store the exported test cases and type a name for the resulting XML file in the **File name** box.</span></span> <span data-ttu-id="41499-116">複数のテストケースをエクスポートする場合、これらのすべてのテストケースは1つの XML ファイルに保存されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="41499-116">Note that if you are exporting multiple tests cases all of these test cases will be saved to a single XML file.</span></span>

5.  <span data-ttu-id="41499-117">テストケースを保存するには、[ **保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="41499-117">To save the test cases, click **Save**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="41499-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="41499-118">See Also</span></span>


[<span data-ttu-id="41499-119">Lync Server 2013 音声ルーティング テスト ケースのインポート</span><span class="sxs-lookup"><span data-stu-id="41499-119">Import voice routing test cases in Lync Server 2013</span></span>](lync-server-2013-import-voice-routing-test-cases.md)  
  

<span data-ttu-id="41499-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="41499-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

