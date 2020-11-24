---
title: 'Lync Server 2013: 音声ルーティング テスト ケースのインポート'
description: 'Lync Server 2013: ボイスルーティングテストケースをインポートします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Import voice routing test cases
ms:assetid: 6546e24c-9ad2-428b-92b2-63948ed0f884
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398460(v=OCS.15)
ms:contentKeyID: 48184325
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 06ce1b144de03406b7b78d6957371ed2bc303e95
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399555"
---
# <a name="import-voice-routing-test-cases-in-lync-server-2013"></a><span data-ttu-id="80b5e-103">Lync Server 2013 音声ルーティング テスト ケースのインポート</span><span class="sxs-lookup"><span data-stu-id="80b5e-103">Import voice routing test cases in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="80b5e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="80b5e-104">

<span> </span></span></span>

<span data-ttu-id="80b5e-105">_**最終更新日:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="80b5e-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="80b5e-106">テストケースは、組織内のボイスルートをテストするための手段を提供します。ダイヤルする番号や、使用するダイヤルプランや音声2013ポリシーなどを定義します。これらの条件が満たされた場合、指定された番号を PSTN ネットワークに正常にルーティングできることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="80b5e-106">Test cases provide a way for you to test voice routes in your organization: you define such things as the number to be dialed and the dial plan and voice policy to be employed, and Lync Server 2013 can then verify that, given those conditions, the supplied number can successfully be routed to the PSTN network.</span></span>

<span data-ttu-id="80b5e-107">Lync Server コントロールパネルを使用して作成できるテストケースは、通常、ケースが最初に作成されて実行されたサーバーにのみ保存されます。</span><span class="sxs-lookup"><span data-stu-id="80b5e-107">Test cases, which can be created by using Lync Server Control Panel, are typically saved only on the server where the case was originally created and run.</span></span> <span data-ttu-id="80b5e-108">ただし、これらのテストケースは XML ファイルとしてエクスポートし、他のサーバーにインポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="80b5e-108">However, these test cases can be exported as XML files (with the .vtest extension) and then imported on other servers.</span></span> <span data-ttu-id="80b5e-109">これにより、トポロジ内のさまざまな場所にあるさまざまなコンピューターで同じテストを実行できます。</span><span class="sxs-lookup"><span data-stu-id="80b5e-109">This enables you to run the same tests on different computers located at different points in your topology.</span></span>

<div>

## <a name="to-import-a-voice-routing-test-case"></a><span data-ttu-id="80b5e-110">ボイスルーティングテストケースをインポートするには</span><span class="sxs-lookup"><span data-stu-id="80b5e-110">To import a voice routing test case</span></span>

1.  <span data-ttu-id="80b5e-111">RTCUniversalServerAdmins グループのメンバーとして、あるいは CsVoiceAdministrator、CsServerAdministrator、または CsAdministrator の役割のメンバーとしてコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="80b5e-111">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="80b5e-112">詳細については、「 [Lync Server 2013 でセットアップのアクセス許可を委任](lync-server-2013-delegate-setup-permissions.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="80b5e-112">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="80b5e-113">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="80b5e-113">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="80b5e-114">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="80b5e-114">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="80b5e-115">左側のナビゲーション バーで [**音声ルーティング**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="80b5e-115">In the left navigation bar, click **Voice Routing**.</span></span>

4.  <span data-ttu-id="80b5e-116">[ **操作** ] メニューの [ **テストケースのインポート**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="80b5e-116">On the **Actions** menu, click **Import test cases**.</span></span>

5.  <span data-ttu-id="80b5e-117">インポートするテストケースファイル (vtest) を見つけて、[ **開く**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="80b5e-117">Find the test case file (.vtest) that you want to import, and then click **Open**.</span></span>

6.  <span data-ttu-id="80b5e-118">[**確定**] をクリックし、[**すべて確定**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="80b5e-118">Click **Commit**, and then click **Commit all**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="80b5e-119">Vtest ファイルをインポートするたびに、[ <STRONG>すべてコミット</STRONG> ] コマンドを実行してテストケースを発行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="80b5e-119">Whenever you import a .vtest file, you must run the <STRONG>Commit all</STRONG> command to publish the test case.</span></span> <span data-ttu-id="80b5e-120">詳細については、「操作のドキュメントで「 <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">Lync Server 2013 のボイスルーティング構成に保留中の変更を発行する</A> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="80b5e-120">For details, see <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">Publish pending changes to the voice routing configuration in Lync Server 2013</A> in the Operations documentation.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="80b5e-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="80b5e-121">See Also</span></span>


[<span data-ttu-id="80b5e-122">Lync Server 2013 での音声ルーティング テスト ケースのエクスポート</span><span class="sxs-lookup"><span data-stu-id="80b5e-122">Export voice routing test cases in Lync Server 2013</span></span>](lync-server-2013-export-voice-routing-test-cases.md)  
  

<span data-ttu-id="80b5e-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="80b5e-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

