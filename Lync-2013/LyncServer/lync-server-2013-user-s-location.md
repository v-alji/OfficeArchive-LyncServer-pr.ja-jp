---
title: 'Lync Server 2013: ユーザーの場所'
description: 'Lync Server 2013: ユーザーの場所。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: User's location
ms:assetid: ce57941d-086b-448e-8ada-c7d636a2a1c9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994073(v=OCS.15)
ms:contentKeyID: 51803984
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a92ec780809cdb3e1ee582ce6c348c884bbb5890
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439171"
---
# <a name="users-location-in-lync-server-2013"></a>Lync Server 2013 のユーザーの場所

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2013-03-09_

Location-Based ルーティングでは、E9 によって使用されている Lync Server で定義されているものと同じネットワーク領域、サイト、サブネットを利用します。これは、PSTN の有料サービスを回避するために、通話ルーティングの制限を適用するために、着信ルーティングの制限を適用するために、 ユーザーの位置情報は、ユーザーの Lync エンドポイントの IP サブネットによって接続されます。 各 IP サブネットは、ネットワーク サイトに関連付けられ、管理者が定義したネットワーク地域に集約されます。 場所に基づくルーティングは、ユーザーのネットワーク サイトに基づいて適用されます。

ルーティングルールは、ネットワークサイト単位で適用されます。つまり、指定したルールセットは、同じネットワークサイト内に存在する Location-Based ルーティングで有効になっているすべてのエンドポイントに適用されます。 Location-Based 管理者は、必要なネットワークサイトにルーティング Location-Based を適用できます。

ボイスルーティングポリシーは、ネットワークサイトごとに定義できます。このような特定の PSTN ゲートウェイは、ネットワークサイト内のすべてのユーザーが PSTN 電話番号に発信するために使用する必要があります。 このような音声ルーティングポリシーは、ユーザーのボイスポリシーによって定義されたルーティングによって、Location-Based ルーティング用に有効になっているネットワークサイトに配置されている場合に、ルーティングが有効になっていると、そのルーティングが、Location-Based ルーティング用に有効になっている他の PSTN ゲートウェイ経由でルーティングできなくなります。 Lync ユーザーが PSTN 通話を発信すると、ユーザーの音声ポリシーによって、そのユーザーが通話を発信することを許可されているかどうかが決定されます。 ユーザーが通話を発信することをユーザーに許可している場合、Location-Based ルーティングによって、通話の発信元となる PSTN ゲートウェイが決定されます。 Location-Based ルーティングでは、ユーザーの位置に基づいてこの決定が行われます。

ユーザーの場所は、次の方法で分類できます。

  - ユーザーは、同じネットワークサイト (office など) に配置された PSTN ゲートウェイ上で、Location-Based ルーティングと彼の DID (直接の外線発信番号) で終了する既知のネットワークサイトにあります。 発信通話のルーティングは、ユーザーが配置されているネットワークサイトの音声ルーティングポリシーを通じて行われます。 ユーザーへの着信 PSTN 通話は、PSTN ゲートウェイと同じネットワークサイトに配置されているエンドポイントにルーティングされます。

  - ユーザーが、PSTN ゲートウェイがあるネットワーク サイトとは異なる既知のネットワーク サイトに位置する (ユーザーが企業内の別のオフィスに出張している場合など)。発信通話のルーティングでは、ユーザーが位置するネットワーク サイトの音声ルーティング ポリシーを使用します。PSTN 料が適切に課金されるようにするために、ユーザーへの着信した PSTN 通話は、PSTN ゲートウェイとは異なるサイトにあるエンドポイントにルーティングされません。

  - Lync Server の展開には未知のネットワークサイトにいるユーザーがいる場合、発信通話のルーティングは、ユーザーに割り当てられているボイスポリシーに基づいて、Location-Based ルーティング制限にバインドされていない PSTN ゲートウェイに適用されます。 PSTN 料が適切に課金されるようにするために、着信した PSTN 通話は、不明なネットワーク サイトにあるエンドポイントにルーティングされません。

<div>

## <a name="see-also"></a>関連項目


[Lync Server 2013 の場所に基づくルーティングのガイダンス](lync-server-2013-guidance-for-location-based-routing.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

