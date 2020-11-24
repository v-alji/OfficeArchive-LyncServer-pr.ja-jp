---
title: 'Lync Server 2013: ディレクターのサービスの開始'
description: 'Lync Server 2013: ディレクターでサービスを開始します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Start services on the Director
ms:assetid: 095b13e1-e788-4b80-93fa-5c5e7498678b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398146(v=OCS.15)
ms:contentKeyID: 48183351
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 51c134099fb328b8647ed7a9176987c06eeb8070
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400011"
---
# <a name="start-services-on-the-director-in-lync-server-2013"></a><span data-ttu-id="d5e2d-103">Lync Server 2013 でのディレクターのサービスの開始</span><span class="sxs-lookup"><span data-stu-id="d5e2d-103">Start services on the Director in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d5e2d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d5e2d-104">

<span> </span></span></span>

<span data-ttu-id="d5e2d-105">_**最終更新日:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="d5e2d-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="d5e2d-106">ローカル構成ストアをインストールし、Lync Server コンポーネントをインストールして、ディレクターで証明書を構成したら、サーバーで Lync Server サービスを開始する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5e2d-106">After you install the Local Configuration Store, install the Lync Server Components, and configure certificates on a Director, you must start the Lync Server services on the server.</span></span> <span data-ttu-id="d5e2d-107">次の手順を使用して、展開の各ディレクターでサービスを開始できます。</span><span class="sxs-lookup"><span data-stu-id="d5e2d-107">You can use the following procedure to start services on each Director in your deployment.</span></span>

<div>

## <a name="to-start-services-on-a-director"></a><span data-ttu-id="d5e2d-108">ディレクターでサービスを開始するには</span><span class="sxs-lookup"><span data-stu-id="d5e2d-108">To start services on a Director</span></span>

1.  <span data-ttu-id="d5e2d-109">Lync Server の展開ウィザードの [ **Lync server 2013** ] ページで、[**手順 4: サービスを開始** する] の横にある [**実行**] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5e2d-109">In the Lync Server Deployment Wizard, on the **Lync Server 2013** page, click the **Run** button next to **Step 4: Start Services**.</span></span>

2.  <span data-ttu-id="d5e2d-110">[ **サービスの開始** ] ページで、[ **次** へ] をクリックして、サーバー上の Lync Server サービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="d5e2d-110">On the **Start Services** page, click **Next** to start the Lync Server services on the server.</span></span>

3.  <span data-ttu-id="d5e2d-111">すべてのサービスが正常に開始されたら、[**コマンドの実行**] ページで [**終了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5e2d-111">On the **Executing Commands** page, after all services have started successfully, click **Finish**.</span></span>

4.  <span data-ttu-id="d5e2d-112">**手順 4: サービスを開始** するには、[**サービスの状態] (オプション)** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d5e2d-112">Below **Step 4: Start Services**, click **Services Status (Optional)**.</span></span>

5.  <span data-ttu-id="d5e2d-113">サーバー上の **サービス** Microsoft 管理コンソール (MMC) で、すべての Lync server 2013 サービスが実行されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d5e2d-113">In the **Services** Microsoft Management Console (MMC) on the server, verify that all of the Lync Server 2013 services are running.</span></span>

<span data-ttu-id="d5e2d-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d5e2d-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

