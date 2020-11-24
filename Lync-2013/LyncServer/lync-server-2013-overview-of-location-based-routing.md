---
title: 'Lync Server 2013: Location-Based ルーティングの概要'
description: 'Lync Server 2013: Location-Based ルーティングの概要'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of Location-Based Routing
ms:assetid: 4aa494bd-0d66-4335-b9e8-f758d44a7202
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994032(v=OCS.15)
ms:contentKeyID: 51803941
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0b1e026791a8562629231b91b58d7e7eff569ffa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399680"
---
# <a name="overview-of-location-based-routing-in-lync-server-2013"></a>Lync Server 2013 での Location-Based ルーティングの概要

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2013-02-21_

場所に基づいたルーティングでは、国内および国際 PSTN 通話のルーティングを変更する新しいルール セットを導入して、課金回避を防止します。場所に基づいたルーティングによって、これらのルールを特定の地域、ゲートウェイ、ユーザー群のみに柔軟に適用できます。

次のシナリオでは、ルーティングで適用 Location-Based 主な種類の制限について説明します。

  - 出口通話– Location-Based ルーティングでは、発信者が PSTN の電話と同じ地域に配置されている PSTN ゲートウェイからの出口を強制することができます。これにより、発信者は、別の地域にある PSTN ゲートウェイからの着信を拒否します。

  - 受信した通話– Location-Based ルーティングは、着信通話を転送する PSTN ゲートウェイが、相手の Lync ユーザーと同じ地域に配置されていない場合に、着信する PSTN 通話が Lync エンドポイントを呼び出すことを防止できます。

  - 不明な地域– Location-Based ルーティングは、不明な場所 (インターネット経由で接続されているか、不明な地域にいるリモートユーザー) との間で、着信と発信の PSTN 通話を制限します。

  - 国際地域– Location-Based ルーティングでは、ユーザーの位置情報に対してローカルゲートウェイが見つからない場合は、国際 PSTN ゲートウェイを介した発信通話のルーティングが適用されます。

<div>

## <a name="see-also"></a>関連項目


[Lync Server 2013 での場所に基づくルーティングの計画](lync-server-2013-planning-for-location-based-routing.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

