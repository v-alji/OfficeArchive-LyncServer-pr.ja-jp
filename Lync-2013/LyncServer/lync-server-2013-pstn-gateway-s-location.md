---
title: 'Lync Server 2013: PSTN ゲートウェイの場所'
description: 'Lync Server 2013: PSTN ゲートウェイの場所。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: PSTN gateway's location
ms:assetid: 49693a35-fad3-49ee-a71e-c7e4537b79aa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994031(v=OCS.15)
ms:contentKeyID: 51803940
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4f793249908bd1f064f9038ddd90c7f5b01a61d5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399093"
---
# <a name="pstn-gateways-location-in-lync-server-2013"></a>Lync Server 2013 の PSTN ゲートウェイの場所

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2013-03-09_

PSTN ゲートウェイおよび Pbx 経由でルーティングする場合は、そのシステムの場所に応じて、Location-Based ルーティング制限が必要になることがあります。 Location-Based ルーティングは、1回のトランク単位で有効にすることができます。

Location-Based ルーティングでは、トランクで有効になったときに、次のルールのセットが導入されます。

  - 1回のトランクで Location-Based ルーティングが有効になっている場合、そのトランクで定義されたルールは、そのトランク経由でルーティングされる通話に対してのみ適用されます。

  - Pstn tolls が、PSTN ゲートウェイが配置されているネットワークサイトとは異なるネットワークサイトから発信される場合は、Location-Based ルーティングによって、ネットワークサイトと特定のトランクとの関連付けが行われます。 これにより、特定のトランクへの通話のルーティングを許可するネットワーク サイトが定義されます。

Trunks Location-Based のルーティングを有効にするには、次の2つの方法があります。

  - トランクは、通話を PSTN に退出させる PSTN ゲートウェイに対して定義されています。この種のトランクによってルーティングされた着信通話は、トランクと同じネットワーク サイト内にあるエンドポイントにのみルーティングされます。

  - トランクは、PSTN に着信を転送しない仲介サーバーピアに対して定義されます。これは、固定の場所 (PBX 電話) で従来の電話を使用しているユーザーを対象としています。 このような特定の構成の場合、この種のトランクによってルーティングされたすべての着信通話は、トランクと同じネットワーク サイトから発信されていると見なされます。 PBX ユーザーからの通話では、トランクと同じネットワークサイトに配置されている Lync ユーザーと同じ Location-Based ルーティングが適用されます。 別々のネットワークサイトに配置されている2つの PBX システムが Lync Server 経由で接続されている場合、Location-Based ルーティングでは、1つのネットワークサイトの1つの PBX エンドポイントから他のネットワークサイトの別の PBX エンドポイントへのルーティングが許可されます。 このシナリオは Location-Based ルーティングによってブロックされることはありません。 このシナリオに加えて、同じ場所にある Lync ユーザーと同じように、仲介サーバーピアが関連付けられているネットワークサイトに関係なく、PSTN (つまり、別の PBX に接続されているエンドポイント) に電話をルーティングしない他の仲介サーバーピアとの通話を発信または受信することができます。 PSTN エンドポイントを含むすべての着信通話、発信通話、通話転送、通話転送には、位置に基づくルーティングが適用されます。この仲介サーバーピアのローカルとして定義されている PSTN ゲートウェイのみを使用します。

<div>

## <a name="see-also"></a>関連項目


[Lync Server 2013 の場所に基づくルーティングのガイダンス](lync-server-2013-guidance-for-location-based-routing.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

