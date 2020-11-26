---
title: 'Lync Server 2013: 音声ルーティング テストの実行'
description: 'Lync Server 2013: ボイスルーティングテストを実行しています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Running voice routing tests
ms:assetid: 577cdc57-930e-4e12-a515-fdcf61b93153
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398377(v=OCS.15)
ms:contentKeyID: 48184185
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7add9b3e555229b478556a0aa1244bf76fa3c759
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442172"
---
# <a name="running-voice-routing-tests-in-lync-server-2013"></a><span data-ttu-id="07b24-103">Lync Server 2013 での音声ルーティング テストの実行</span><span class="sxs-lookup"><span data-stu-id="07b24-103">Running voice routing tests in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="07b24-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="07b24-104">

<span> </span></span></span>

<span data-ttu-id="07b24-105">_**最終更新日:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="07b24-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="07b24-106">Lync Server 2013 には、音声ルートをテストするための2つの異なる方法が用意されています。任意の電話番号やボイスルートに対して臨時のアドホックテストを行うことができます。または、ボイスルーティングテストケースを使用して、さらに正式なテストを行うこともできます。</span><span class="sxs-lookup"><span data-stu-id="07b24-106">Lync Server 2013 provides two different methods for testing voice routes: you can do informal, ad hoc testing against any phone number and any voice route; or you can do more formal testing using voice route test cases.</span></span> <span data-ttu-id="07b24-107">正式なテストでは、ダイヤルする番号やダイヤルプランと音声ポリシーなどを定義して、それらの条件が満たされた場合に、指定された番号を PSTN ネットワークに正常にルーティングできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="07b24-107">With formal testing, you define such things as the number to be dialed and the dial plan and voice policy to be employed, and Lync Server can then verify that, given those conditions, the supplied number can successfully be routed to the PSTN network.</span></span> <span data-ttu-id="07b24-108">この2つの方法については、このドキュメントの以降のセクションで説明します。</span><span class="sxs-lookup"><span data-stu-id="07b24-108">Both of these methods are described in subsequent sections of this documentation.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="07b24-109">このセクション中</span><span class="sxs-lookup"><span data-stu-id="07b24-109">In This Section</span></span>

  - [<span data-ttu-id="07b24-110">Lync Server 2013 で非公式の音声ルーティングテストを実行する</span><span class="sxs-lookup"><span data-stu-id="07b24-110">Run informal voice routing tests in Lync Server 2013</span></span>](lync-server-2013-run-informal-voice-routing-tests.md)

  - [<span data-ttu-id="07b24-111">Lync Server 2013 でボイスルーティングテストケースを実行する</span><span class="sxs-lookup"><span data-stu-id="07b24-111">Run voice routing test cases in Lync Server 2013</span></span>](lync-server-2013-run-voice-routing-test-cases.md)

<span data-ttu-id="07b24-112"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="07b24-112"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

