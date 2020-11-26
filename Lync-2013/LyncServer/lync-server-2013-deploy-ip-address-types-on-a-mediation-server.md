---
title: 'Lync Server 2013: 仲介サーバーに IP アドレス タイプを展開する'
description: 'Lync Server 2013: 仲介サーバーに IP アドレスの種類を展開します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploy IP address types on a Mediation Server
ms:assetid: 689ebed5-96ee-4cd4-b7ae-ee2a86a1d9b3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204964(v=OCS.15)
ms:contentKeyID: 48184376
ms.date: 07/28/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: daa3be8d1ef12629dc185f98b95d2db0e565cf18
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430233"
---
# <a name="deploy-ip-address-types-on-a-mediation-server-for-lync-server-2013"></a><span data-ttu-id="1273f-103">Lync Server 2013 の仲介サーバーに IP アドレス タイプを展開する</span><span class="sxs-lookup"><span data-stu-id="1273f-103">Deploy IP address types on a Mediation Server for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1273f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1273f-104">

<span> </span></span></span>

<span data-ttu-id="1273f-105">_**最終更新日:** 2016-07-28_</span><span class="sxs-lookup"><span data-stu-id="1273f-105">_**Topic Last Modified:** 2016-07-28_</span></span>

<span data-ttu-id="1273f-106">トポロジビルダーを使用して、次の手順を実行して、仲介サーバーに IP アドレスの種類を展開します。</span><span class="sxs-lookup"><span data-stu-id="1273f-106">Using Topology Builder, perform the steps in the following procedure to deploy IP address types on a Mediation Server.</span></span>

<div>

## <a name="to-deploy-ip-address-types-on-a-mediation-server"></a><span data-ttu-id="1273f-107">仲介サーバーに IP アドレスの種類を展開するには</span><span class="sxs-lookup"><span data-stu-id="1273f-107">To deploy IP address types on a Mediation Server</span></span>

  - <span data-ttu-id="1273f-108">[トポロジビルダー] の [ **仲介プール**] で、プール内のサーバーを右クリックし、[ **プロパティの編集**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="1273f-108">In Topology Builder, under **Mediation pools**, right-click the server within a pool, and then select **Edit Properties**.</span></span> <span data-ttu-id="1273f-109">(または、サーバーを選択し、[**アクション**] メニューの [**プロパティの編集**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="1273f-109">(Alternatively, select the server, and then click **Edit Properties** from the **Action** menu.)</span></span>

  - <span data-ttu-id="1273f-p102">[**プロパティの編集**] ダイアログ ボックスで、構成する IP アドレスの種類を選択します。デュアル スタック構成の場合は、次の図のように、[**IPv4 を有効にする**] および [**IPv6 を有効にする**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="1273f-p102">In the **Edit Properties** dialog box, select the IP address type that you want to configure. For a dual-stack configuration, select **Enable IPv4** and **Enable IPv6**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="1273f-112">**仲介サーバー プールの [プロパティの編集] ダイアログ ボックス**</span><span class="sxs-lookup"><span data-stu-id="1273f-112">**Edit Properties dialog box for the Mediation Server pool**</span></span>
    
    <span data-ttu-id="1273f-113">![FQDN 付きの Lync Server の [全般] プロパティページ](images/JJ204964.4e650aca-dbff-4a86-b10d-f0162c032539(OCS.15).png "FQDN 付きの Lync Server の [全般] プロパティページ")</span><span class="sxs-lookup"><span data-stu-id="1273f-113">![Lync Server general properties page with FQDN](images/JJ204964.4e650aca-dbff-4a86-b10d-f0162c032539(OCS.15).png "Lync Server general properties page with FQDN")</span></span>
    
      - <span data-ttu-id="1273f-p103">[**すべての構成済み IP アドレスを使用する**]。コンピューター上で定義されているすべての IP アドレスの使用を許可する場合は、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="1273f-p103">**Use all configured IP addresses**. Select this option if you want to allow any IP address defined on the computer to be used.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="1273f-116">これは、IP version 6 (IPv6) 構成の推奨オプションです。</span><span class="sxs-lookup"><span data-stu-id="1273f-116">This is the recommended option for IP version 6 (IPv6) configurations.</span></span>

        
        </div>
    
      - <span data-ttu-id="1273f-p104">[**サービスの使用を、指定したアドレスに制限する**]。新しいサーバーで使用する特定のアドレスを指定する場合は、このオプションを選択します。このオプションを選択する場合は、プライマリ IP アドレスの値を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1273f-p104">**Limit service usage to selected IP addresses**. Select this option to specify a specific address to use on the new server. If you select this option, you must enter a value for Primary IP address.</span></span>
    
      - <span data-ttu-id="1273f-p105">[**プライマリ IP アドレス**]。公衆交換電話網 (PSTN) 以外のすべての通信でサーバーが使用する IP アドレスを入力します。入力する IP アドレスは、選択されているアドレスの種類の形式に一致している必要があります。</span><span class="sxs-lookup"><span data-stu-id="1273f-p105">**Primary IP address**. Enter an IP address that the server will use for all communications except public switched telephone network (PSTN). The IP address entered must match the format of the select address type.</span></span>
    
      - <span data-ttu-id="1273f-123">[**PSTN IP アドレス**]。</span><span class="sxs-lookup"><span data-stu-id="1273f-123">**PSTN IP address**.</span></span> <span data-ttu-id="1273f-124">仲介サーバーがスタンドアロンの場合は、PSTN IP アドレスを定義します。</span><span class="sxs-lookup"><span data-stu-id="1273f-124">Define a PSTN IP address when a Mediation Server is standalone.</span></span> <span data-ttu-id="1273f-125">このアドレスは、選択されているアドレスの種類の形式に一致している必要があります。</span><span class="sxs-lookup"><span data-stu-id="1273f-125">This address must match the format of the selected address type.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="1273f-126">Lync Server 2013 の PSTN IP アドレス構成をサポートするための追加のネットワークインターフェイスカード (NIC) のインストールは、併置された仲介サーバーの役割でサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="1273f-126">The installation of additional network interface cards (NIC)s to support the PSTN IP address configuration for Lync Server 2013 is not supported on collocated Mediation Server roles.</span></span> <span data-ttu-id="1273f-127">Lync Server 2013 でサポートされる NIC 構成の詳細については、「 <A href="lync-server-2013-server-hardware-platforms.md">Lync server 2013 のサーバーハードウェアプラットフォーム</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1273f-127">For more information about supported NIC configurations for Lync Server 2013, see <A href="lync-server-2013-server-hardware-platforms.md">Server hardware platforms for Lync Server 2013</A>.</span></span>

        
        <span data-ttu-id="1273f-128"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1273f-128"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

