---
title: 仲介サーバーを構成する
description: 仲介サーバーを構成します。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Configure Mediation Server
ms:assetid: 583236fd-33cd-4045-81df-baa58ed07779
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204913(v=OCS.15)
ms:contentKeyID: 48184207
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5723d9446122b85f7bd1812f7c6f411c5c1c9dbe
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398865"
---
# <a name="configure-mediation-server"></a><span data-ttu-id="763a9-103">仲介サーバーを構成する</span><span class="sxs-lookup"><span data-stu-id="763a9-103">Configure Mediation Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="763a9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="763a9-104">

<span> </span></span></span>

<span data-ttu-id="763a9-105">_**最終更新日:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="763a9-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="763a9-106">この手順では、従来の Office Communications Server 2007 R2 仲介サーバーではなく、lync server 2013 仲介サーバーを使用するように Lync Server 2013 プールを構成する手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="763a9-106">This procedure details the steps to configure the Lync Server 2013 pool to use the Lync Server 2013 Mediation Server, instead of the legacy Office Communications Server 2007 R2 Mediation Server.</span></span>

<span data-ttu-id="763a9-107">トポロジを正常に発行、有効化、または無効にするには、RTCUniversalServerAdmins および Domain Admins グループのメンバーであるユーザーとしてログインしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="763a9-107">To successfully publish, enable, or disable a topology when adding or removing a server role, you should be logged in as a user who is a member of the RTCUniversalServerAdmins and Domain Admins groups.</span></span> <span data-ttu-id="763a9-108">また、サーバーの役割を追加するための適切な管理者権限と権限を委任することもできます。</span><span class="sxs-lookup"><span data-stu-id="763a9-108">It is also possible to delegate the proper administrator rights and permissions for adding server roles.</span></span> <span data-ttu-id="763a9-109">詳細については、「Standard Edition server または Enterprise Edition server 展開ドキュメントの委任セットアップの権限」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="763a9-109">For details, see Delegate Setup Permissions in the Standard Edition server or Enterprise Edition server Deployment documentation.</span></span> <span data-ttu-id="763a9-110">その他の構成変更については、RTCUniversalServerAdmins グループのメンバーシップのみが必要です。</span><span class="sxs-lookup"><span data-stu-id="763a9-110">For other configuration changes, only membership in the RTCUniversalServerAdmins group is required.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="763a9-111">Lync Server 2013 で動作する、限定 PSTN ゲートウェイ、IP Pbx、SIP トランクサービスの検索に関する最新情報については、「Microsoft ユニファイド通信での相互運用プログラムのオープン」を参照してください <A href="https://go.microsoft.com/fwlink/p/?linkid=206015">https://go.microsoft.com/fwlink/p/?linkId=206015</A> 。</span><span class="sxs-lookup"><span data-stu-id="763a9-111">For the latest information on finding qualified PSTN gateways, IP-PBXs, and SIP trunking services that work with Lync Server 2013, see "Microsoft Unified Communications Open Interoperability Program" at <A href="https://go.microsoft.com/fwlink/p/?linkid=206015">https://go.microsoft.com/fwlink/p/?linkId=206015</A>.</span></span>



</div>

<div>

## <a name="to-configure-mediation-server-using-topology-builder"></a><span data-ttu-id="763a9-112">トポロジビルダーを使用して仲介サーバーを構成するには</span><span class="sxs-lookup"><span data-stu-id="763a9-112">To configure Mediation Server Using Topology Builder</span></span>

1.  <span data-ttu-id="763a9-113">トポロジビルダーから既存のトポロジを開きます。</span><span class="sxs-lookup"><span data-stu-id="763a9-113">Open an existing topology from Topology Builder.</span></span>

2.  <span data-ttu-id="763a9-114">左側のウィンドウで、[ **PSTN ゲートウェイ**] に移動します。</span><span class="sxs-lookup"><span data-stu-id="763a9-114">In the left pane, navigate to **PSTN gateways**.</span></span>

3.  <span data-ttu-id="763a9-115">[ **PSTN ゲートウェイ**] を右クリックし、[ **新しい IP/PSTN ゲートウェイ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="763a9-115">Right-click **PSTN gateways**, and then click **New IP/PSTN Gateway**.</span></span>

4.  <span data-ttu-id="763a9-116">[ **新しい IP/PSTN ゲートウェイの定義** ] ページに次の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="763a9-116">Complete the **Define New IP/PSTN Gateway** page with the following information:</span></span>
    
      - <span data-ttu-id="763a9-117">ゲートウェイの FQDN または IP アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="763a9-117">Enter the gateway FQDN or IP address.</span></span> <span data-ttu-id="763a9-118">ゲートウェイで TLS プロトコルを使用している場合は、ゲートウェイの FQDN が必要です。</span><span class="sxs-lookup"><span data-stu-id="763a9-118">The FQDN of the gateway is required if the gateway uses the TLS protocol.</span></span>
    
      - <span data-ttu-id="763a9-119">**IP/PSTN ゲートウェイのリスニングポート** の既定値をそのまま使うか、変更された場合は新しいリッスンポートを入力します。</span><span class="sxs-lookup"><span data-stu-id="763a9-119">Accept the default value of the **Listening port for IP/PSTN gateway** or enter the new listening port if it was modified.</span></span>
    
      - <span data-ttu-id="763a9-120">**Sip トランスポートプロトコル** を設定します。</span><span class="sxs-lookup"><span data-stu-id="763a9-120">Set the **Sip Transport Protocol**.</span></span>

5.  <span data-ttu-id="763a9-121">左側のウィンドウで、 **Enterprise Edition のフロントエンドプール** または **Standard Edition サーバー** に移動します。</span><span class="sxs-lookup"><span data-stu-id="763a9-121">In the left pane, navigate to the **Enterprise Edition Front End pool** or the **Standard Edition Server**.</span></span>

6.  <span data-ttu-id="763a9-122">プールを右クリックし、[プロパティの **編集**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="763a9-122">Right-click the pool, and then click **Edit Properties**.</span></span>

7.  <span data-ttu-id="763a9-123">[ **仲介サーバー**] で、 **リッスンポート** を設定します。</span><span class="sxs-lookup"><span data-stu-id="763a9-123">Under **Mediation Server**, set the **Listening ports**.</span></span>

8.  <span data-ttu-id="763a9-124">次に、新しく作成した PSTN ゲートウェイを選択して [ **追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="763a9-124">Next, associate the newly created PSTN gateway by selecting it and clicking **Add**.</span></span>

9.  <span data-ttu-id="763a9-125">[ **トポロジビルダー**] で、トップノードの **Lync Server** を選択します。</span><span class="sxs-lookup"><span data-stu-id="763a9-125">In **Topology Builder**, select the top-most node **Lync Server**.</span></span>

10. <span data-ttu-id="763a9-126">[ **アクション** ] メニューで、[ **発行トポロジ** ] を選択し、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="763a9-126">From the **Action** menu, select **Publish Topology** and then click **Next**.</span></span>

11. <span data-ttu-id="763a9-127">**発行ウィザード** が完了したら、[**完了**] をクリックしてウィザードを閉じます。</span><span class="sxs-lookup"><span data-stu-id="763a9-127">When the **Publishing wizard** completes, click **Finish** to close the wizard.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="763a9-128">次のトピック「ボイスルートを変更して、 <A href="change-voice-routes-to-use-the-new-lync-server-2013-mediation-server.md">新しい Lync server 2013 仲介サーバーを使用する</A> 」を実行し、ボイスルーティングが正しい仲介サーバーをポイントするようにすることが重要です。</span><span class="sxs-lookup"><span data-stu-id="763a9-128">It is important that you complete the next topic, <A href="change-voice-routes-to-use-the-new-lync-server-2013-mediation-server.md">Change voice routes to use the new Lync Server 2013 Mediation Server</A> to ensure that the voice routes are pointing to the correct Mediation Server.</span></span>



<span data-ttu-id="763a9-129"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="763a9-129"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

