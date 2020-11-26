---
title: 'Lync Server 2013: 設計の編集'
description: 'Lync Server 2013: デザインを編集します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Editing the design
ms:assetid: 08f639ba-0e5f-4ae7-9191-c3d96c25b169
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558608(v=OCS.15)
ms:contentKeyID: 51541445
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 20462c1c1813551159e8eeb3b255bd9069e3cce1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428968"
---
# <a name="editing-the-design-in-lync-server-2013"></a><span data-ttu-id="36a36-103">Lync Server 2013 での設計の編集</span><span class="sxs-lookup"><span data-stu-id="36a36-103">Editing the design in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="36a36-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="36a36-104">

<span> </span></span></span>

<span data-ttu-id="36a36-105">_**最終更新日:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="36a36-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="36a36-p101">最初のインタビューによる質問を完了すると、サイトの完全修飾ドメイン名 (FQDN) と IP アドレスを編集できます。これを行うには、[**グローバル トポロジ**] ページで、編集するサイトをダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="36a36-p101">After completing the initial interview questions, you can edit the fully qualified domain name (FQDN) and IP addresses for the site. To do this, on the **Global Topology** page, double-click the site that you want to edit.</span></span>

<span data-ttu-id="36a36-108">計画ツールには、選択したサイトのサイトトポロジが表示されます。</span><span class="sxs-lookup"><span data-stu-id="36a36-108">The Planning Tool displays the site topology for the selected site.</span></span> <span data-ttu-id="36a36-109">サイト ページの下部には、次の 4 つのタブがあります。</span><span class="sxs-lookup"><span data-stu-id="36a36-109">At the bottom of the site page are four tabs:</span></span>

<span data-ttu-id="36a36-110">![計画ツール、サイト トポロジ](images/Gg558608.e6189c20-360a-42bd-ba90-11bdb5b7551b(OCS.15).jpg "計画ツール、サイト トポロジ")</span><span class="sxs-lookup"><span data-stu-id="36a36-110">![Planning Tool Site Topology](images/Gg558608.e6189c20-360a-42bd-ba90-11bdb5b7551b(OCS.15).jpg "Planning Tool Site Topology")</span></span>

  - <span data-ttu-id="36a36-111">サイト トポロジ - 現在表示されているページで、推奨されるビジュアルなトポロジの概要が含まれます。</span><span class="sxs-lookup"><span data-stu-id="36a36-111">Site Topology – The currently displayed page with a visual overview of the topology as recommended.</span></span>

  - <span data-ttu-id="36a36-112">エッジネットワーク図– [Edge ネットワークダイアグラム] ページでは、計画ツールのほとんどの作業をデザイナーが行います。</span><span class="sxs-lookup"><span data-stu-id="36a36-112">Edge Network Diagram – The Edge Network Diagram page is where the designer does most of the work in the Planning Tool.</span></span> <span data-ttu-id="36a36-113">この図は、推奨される Lync Server 2013 トポロジのネットワーク構成を示しています。これには、サーバーの IP アドレスと Fqdn 用の編集可能なエントリ、およびハードウェアとドメインネームシステム (DNS) ロードバランサーの両方が含まれています。</span><span class="sxs-lookup"><span data-stu-id="36a36-113">The diagram displays the network configuration for a recommended Lync Server 2013 topology, with editable entries for IP addresses and FQDNs for servers, pool, and both hardware and Domain Name System (DNS) load balancers.</span></span>

  - <span data-ttu-id="36a36-114">エッジ管理レポート - 次の合計 4 つのレポートが含まれます。</span><span class="sxs-lookup"><span data-stu-id="36a36-114">Edge Admin Report – The Edge Admin Report contains a total of four reports:</span></span>
    
    <span data-ttu-id="36a36-115">![[エッジ管理レポート] ページ](images/Gg558608.0019cc5e-af39-4cb9-82ce-58f6388242ff(OCS.15).jpg "[エッジ管理レポート] ページ")</span><span class="sxs-lookup"><span data-stu-id="36a36-115">![Edge Admin Report page](images/Gg558608.0019cc5e-af39-4cb9-82ce-58f6388242ff(OCS.15).jpg "Edge Admin Report page")</span></span>  
    
      - <span data-ttu-id="36a36-p104">概要レポート - エッジ ネットワーク構成の設定に関する一般的なレポート。[  **エッジ ネットワーク図**] ページの値を、実際の展開で使用する、トポロジの TCP/IP および FQDN の値に編集する場合、それらのアドレスと名前がここに表示されます。それ以外の場合、既定のテキストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="36a36-p104">Summary Report – A general report of settings for the Edge network configuration. If you edit the values on the **Edge Network Diagram** page to the topology TCP/IP and FQDN values of that will be used in the actual deployment, those addresses and names will be represented here. Otherwise, the default text will appear.</span></span>
    
      - <span data-ttu-id="36a36-119">証明書レポート - トポロジで必要な証明書のサブジェクト名とサブジェクトの別名が表示されます。</span><span class="sxs-lookup"><span data-stu-id="36a36-119">Certificate Report – The certificate report will list the subject name and subject alternative names for the certificates that are required for the topology.</span></span>
    
      - <span data-ttu-id="36a36-p105">ファイアウォール レポート - インフラストラクチャに周辺ファイアウォールを構成するために必要な情報が表示されます。IP アドレス (既定値または編集された値)、サーバーの役割、送信元 IP と送信元ポート、宛先 IP と宛先ポート、トランスポート プロトコル、アプリケーション プロトコル、および関連する注記が表示されます。</span><span class="sxs-lookup"><span data-stu-id="36a36-p105">Firewall Report – The firewall report lists information necessary to configure perimeter firewalls in the infrastructure. This includes the IP addresses (either the default or edited values), server role, source IP and port, destination IP and port, transport protocol, application protocol, and relevant notes.</span></span>
    
      - <span data-ttu-id="36a36-p106">DNS レポート - 作成する必要がある DNS エントリの関連情報が表示されます。正しい動作に必要なレコードの種類、FQDN、IP アドレス、およびコメントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="36a36-p106">DNS Report – The DNS Report lists relevant information for the DNS entries that you must create. The record type, FQDN, IP address, and comments necessary for the proper operation are included.</span></span>

  - <span data-ttu-id="36a36-p107">サイトの概要 - 最初のインタビューの質問への回答または [  **サイトの設計**] での値の入力による選択肢の概要が表示されます。処理能力に関する情報も表示されます。</span><span class="sxs-lookup"><span data-stu-id="36a36-p107">Site Summary – The site summary presents an overview of the selections that you made by either answering the initial interview questions or filling in the values in **Design Sites**. Capacity information is also presented.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="36a36-126">サイトの概要ページの情報は、設計ごとにカスタマイズされるため、ここで説明しているすべてのセクションや情報が含まれない場合があります。</span><span class="sxs-lookup"><span data-stu-id="36a36-126">The information on the Site Summary page is customized for each design and may not contain all sections or information detailed here.</span></span>

    
    </div>

<div>

## <a name="see-also"></a><span data-ttu-id="36a36-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="36a36-127">See Also</span></span>


[<span data-ttu-id="36a36-128">Lync Server 2013 でのネットワーク構成図の編集</span><span class="sxs-lookup"><span data-stu-id="36a36-128">Editing the network configuration diagram in Lync Server 2013</span></span>](lync-server-2013-editing-the-network-configuration-diagram.md)  
  

<span data-ttu-id="36a36-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="36a36-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

