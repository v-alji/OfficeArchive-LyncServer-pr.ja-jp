---
title: 'Lync Server 2013: SIP/CSTA ゲートウェイの IP アドレスの定義'
description: 'Lync Server 2013: SIP/CSTA ゲートウェイの IP アドレスを定義します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Define a SIP/CSTA gateway IP address
ms:assetid: ae944057-3ad6-4474-a09b-81a3d27bd50f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg602125(v=OCS.15)
ms:contentKeyID: 48185073
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 23286b2748df3af06f905a791bf0ee80c6f0a919
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431142"
---
# <a name="define-a-sipcsta-gateway-ip-address-in-lync-server-2013"></a><span data-ttu-id="97fd9-103">Lync Server 2013 での SIP/CSTA ゲートウェイの IP アドレスの定義</span><span class="sxs-lookup"><span data-stu-id="97fd9-103">Define a SIP/CSTA gateway IP address in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="97fd9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="97fd9-104">

<span> </span></span></span>

<span data-ttu-id="97fd9-105">_**最終更新日:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="97fd9-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="97fd9-106">Lync Server が伝送制御プロトコル (TCP) 接続を使ってリモート通話コントロール用に展開した SIP/CSTA ゲートウェイに接続する場合は、トポロジビルダーでゲートウェイの IP アドレスを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="97fd9-106">If Lync Server will connect to the SIP/CSTA gateway that you deployed for remote call control by using a Transmission Control Protocol (TCP) connection, then you must define the IP address of the gateway in Topology Builder.</span></span> <span data-ttu-id="97fd9-107">トランスポート層セキュリティ (TLS) 接続をサポートするゲートウェイの場合、この手順は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="97fd9-107">This step is not necessary for gateways that support Transport Layer Security (TLS) connections.</span></span> <span data-ttu-id="97fd9-108">TLS 接続をサポートしているすべてのゲートウェイについては、この手順をスキップして、「lync [ユーザーが Lync Server 2013 のリモート通話制御を有効にする](lync-server-2013-enable-lync-users-for-remote-call-control.md)」の手順に従って、リモート通話コントロールの展開を継続できます。</span><span class="sxs-lookup"><span data-stu-id="97fd9-108">For any gateway that supports TLS connections, you can skip this procedure and continue deployment of remote call control by following the steps in [Enable Lync users for remote call control in Lync Server 2013](lync-server-2013-enable-lync-users-for-remote-call-control.md).</span></span>

<div>

## <a name="to-define-the-sipcsta-gateway-ip-address-by-using-topology-builder"></a><span data-ttu-id="97fd9-109">Topology Builder を使用して SIP/CSTA ゲートウェイの IP アドレスを定義するには</span><span class="sxs-lookup"><span data-stu-id="97fd9-109">To define the SIP/CSTA gateway IP address by using Topology Builder</span></span>

1.  <span data-ttu-id="97fd9-110">トポロジ ビルダーがインストールされているコンピューターに、Domain Admins グループおよび RTCUniversalServerAdmins グループのメンバーとしてログオンします。</span><span class="sxs-lookup"><span data-stu-id="97fd9-110">Log on to the computer where Topology Builder is installed as a member of the Domain Admins group and the RTCUniversalServerAdmins group.</span></span>

2.  <span data-ttu-id="97fd9-111">トポロジビルダーを開始します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server Topology Builder**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="97fd9-111">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

3.  <span data-ttu-id="97fd9-112">既存のトポロジをダウンロードするためのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="97fd9-112">Choose the option to download an existing topology.</span></span>

4.  <span data-ttu-id="97fd9-113">[信頼されている **アプリケーションサーバー** ] ノードを展開します。</span><span class="sxs-lookup"><span data-stu-id="97fd9-113">Expand the **Trusted application servers** node.</span></span>

5.  <span data-ttu-id="97fd9-114">「 [Lync Server 2013 のリモート通話コントロールに対して信頼されているアプリケーションエントリを構成](lync-server-2013-configure-a-trusted-application-entry-for-remote-call-control.md)する」の説明に従って、作成した信頼できるアプリケーションプールを右クリックし、[ **プロパティの編集**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="97fd9-114">Right-click the trusted application pool that you created, as described in [Configure a trusted application entry for remote call control in Lync Server 2013](lync-server-2013-configure-a-trusted-application-entry-for-remote-call-control.md), and then click **Edit Properties**.</span></span>

6.  <span data-ttu-id="97fd9-115">[ **このプールへの構成データのレプリケーションを有効に** する] チェックボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="97fd9-115">Clear the **Enable replication of configuration data to this pool** check box.</span></span>

7.  <span data-ttu-id="97fd9-116">[ **サービスの利用制限を選択した IP アドレスに制限] を** クリックします。</span><span class="sxs-lookup"><span data-stu-id="97fd9-116">Click **Limit service usage to selected IP addresses**.</span></span> <span data-ttu-id="97fd9-117">既定の設定では、[構成され **た IP アドレスをすべて使用する**] を選びます。</span><span class="sxs-lookup"><span data-stu-id="97fd9-117">The default setting is **Use all configured IP addresses**.</span></span>

8.  <span data-ttu-id="97fd9-118">[ **プライマリ IP アドレス** ] テキストボックスに、SIP/csta ゲートウェイの IP アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="97fd9-118">In the **Primary IP address** text box, enter the IP address of the SIP/CSTA gateway.</span></span>

9.  <span data-ttu-id="97fd9-119">サーバーの全体管理ストアでトポロジを更新するには、コンソールツリーで [ **Lync Server**] をクリックし、[ **操作** ] ウィンドウで [ **発行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="97fd9-119">To update the topology in the Central Management store, in the console tree, click **Lync Server**, and then, from the **Actions** pane, click **Publish**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="97fd9-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="97fd9-120">See Also</span></span>


[<span data-ttu-id="97fd9-121">Lync Server 2013 でのリモート通話コントロールの静的ルートの構成</span><span class="sxs-lookup"><span data-stu-id="97fd9-121">Configure a static route for remote call control in Lync Server 2013</span></span>](lync-server-2013-configure-a-static-route-for-remote-call-control.md)  
[<span data-ttu-id="97fd9-122">Lync Server 2013 でリモート通話コントロールの信頼済みアプリケーション エントリを構成する</span><span class="sxs-lookup"><span data-stu-id="97fd9-122">Configure a trusted application entry for remote call control in Lync Server 2013</span></span>](lync-server-2013-configure-a-trusted-application-entry-for-remote-call-control.md)  
  

<span data-ttu-id="97fd9-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="97fd9-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

