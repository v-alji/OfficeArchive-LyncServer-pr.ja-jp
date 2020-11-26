---
title: 'Lync Server 2013: IP とネットワーク プロトコルのサポート'
description: 'Lync Server 2013: IP およびネットワークプロトコルのサポート。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: IP and networking protocol support
ms:assetid: b0cffb10-3478-445c-89c7-8cb8b5027424
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412848(v=OCS.15)
ms:contentKeyID: 48185128
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dbd8022dd7197524334e0c70ea0ad875a30446de
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426747"
---
# <a name="ip-and-networking-protocol-support-in-lync-server-2013"></a>Lync Server 2013 での IP とネットワーク プロトコルのサポート

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-09-21_

Lync Server 2013 は、次の IP およびネットワークプロトコルをサポートしています。

  - **IP プロトコル。**   Lync Server 2013 では、サーバーネットワークの IP バージョン 4 (IPv4) または IP version 6 (IPv6) がサポートされています。
    
    <div>
    

    > [!NOTE]  
    > Lync Server 2013 は、デュアル IP スタックが有効になっているネットワークで機能することができます。

    
    </div>

  - **SIP トランスポートプロトコル。**   一般的に、SIP では、ユーザーデータグラムプロトコル (UDP)、伝送制御プロトコル (TCP)、トランスポート層セキュリティ (TLS) の3つ以上のトランスポートタイプを使うことができます。 既定の SIP トランスポート構成では、TLS は TCP 経由で実行されます。 TLS は Lync Server 2013 ネットワーク内で使用されます。 ネットワークの端では、Lync Server 2013 は TCP 経由で相互運用できます。 Lync Server 2013 では、エンタープライズ通信のセキュリティ、信頼性、スケーラビリティに関する最小標準を満たしていないため、SIP トランスポートの UDP はサポートされていません。 詳細については、「NextHop のブログ記事「udp について」または「UDP ではなく」を参照してください [https://go.microsoft.com/fwlink/p/?linkId=185369](https://go.microsoft.com/fwlink/p/?linkid=185369) 。
    
    <div>
    

    > [!NOTE]  
    > 各ブログの内容と URL は、将来予告なしに変更されることがあります。

    
    </div>

</div>

<span> </span>

</div>

</div>

</div>

