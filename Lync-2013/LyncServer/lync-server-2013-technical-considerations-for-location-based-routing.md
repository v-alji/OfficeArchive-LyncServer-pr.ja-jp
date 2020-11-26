---
title: 'Lync Server 2013: 場所に基づくルーティングに関する技術的考慮事項'
description: 'Lync Server 2013: Location-Based ルーティングの技術的な考慮事項'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Technical considerations for Location-Based Routing
ms:assetid: 2e2a9199-7c6f-48d3-9adb-3873fc4f8c4e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994027(v=OCS.15)
ms:contentKeyID: 51803936
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 54a025af81ab148ad41f95d0a8cf4f900beb7e00
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423429"
---
# <a name="technical-considerations-for-location-based-routing-in-lync-server-2013"></a>場所に基づくルーティングに関する Lync Server 2013 の技術的考慮事項

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2013-03-09_

ルーティング Location-Based 計画を立てるときは、次のシナリオへの影響を考慮する必要があります。

<div>

## <a name="disaster-recovery"></a>障害復旧

プライマリプールからバックアッププールへのフェールオーバー、および通常の操作をプライマリプールに復元したときに、Location-Based ルーティングは、障害発生時と回復時に常に適用されたままになります。

</div>

<div>

## <a name="survivable-branch-appliance"></a>存続可能ブランチ アプライアンス

Location-Based ルーティングを構成すると、Survivable Branch アプライアンスに関連付けられているゲートウェイの展開先が計画されます。 SBA に関連付けられているゲートウェイは、Survivable Branch Appliance と同じネットワークサイトにある必要があります。そうしないと、Location-Based ルーティングが構成されている場合に、Survivable Branch アプライアンスをホームとしているユーザーは、発信通話を行うことができなくなります。 Survivable Branch Appliance とセントラルサイト間の WAN 接続がダウンしている場合、Location-Based ルーティング制限は適用されません。

</div>

<div>

## <a name="see-also"></a>関連項目


[Lync Server 2013 での場所に基づくルーティングの計画](lync-server-2013-planning-for-location-based-routing.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

