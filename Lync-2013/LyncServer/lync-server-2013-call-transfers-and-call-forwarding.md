---
title: 'Lync Server 2013: 通話転送と着信転送'
description: 'Lync Server 2013: 着信の転送と着信の転送。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call transfers and call forwarding
ms:assetid: 978610ec-63c7-4cf6-ad7a-9ef91559bf12
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994051(v=OCS.15)
ms:contentKeyID: 51803962
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d9359cb64b386d022eab33e4523dfaccf784075b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435685"
---
# <a name="call-transfers-and-call-forwarding-in-lync-server-2013"></a>Lync Server 2013 の通話転送と着信転送

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2013-03-09_

PSTN エンドポイントが含まれている場合、Location-Based ルーティングは、calle のエンドポイントの場所と、通話が転送または転送されるエンドポイント (転送/転送ターゲット) を分析します。 Location-Based ルーティングは、両方のエンドポイントの場所に応じて、通話を転送するか転送するかを決定します。

次の表は、PSTN エンドポイントを使用した通話での Lync ユーザーのシナリオと、Lync ユーザーが別の Lync ユーザーに通話を転送するシナリオを示しています。 Transferee のエンドポイントのネットワークサイトの場所に応じて、Location-Based ルーティングは、通話転送または転送のルーティングに影響します。

### <a name="initiating-call-transfer-or-forward"></a>通話転送または着信転送の開始

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>通話転送または着信転送を開始するユーザー</th>
<th>ターゲット エンドポイントが、通話転送または着信転送を開始するユーザーと同じネットワーク サイトにある</th>
<th>ターゲット エンドポイントが、通話転送または着信転送を開始するユーザーとは別のネットワーク サイトにある</th>
<th>ターゲットエンドポイントが不明なネットワークサイトにあるか、Location-Based ルーティング用に有効になっていないネットワークサイトにある</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Lync ユーザー</p></td>
<td><p>通話または着信を転送できます。</p></td>
<td><p>通話または着信を転送できません。</p></td>
<td><p>通話または着信を転送できません。</p></td>
</tr>
</tbody>
</table>

  

たとえば、PSTN エンドポイントでの Lync ユーザーは、同じネットワークサイト内の別の Lync ユーザーに通話を転送します。 この場合、通話の転送が許可されます。

次の表は、別の Lync ユーザーとの通話での Lync ユーザーのシナリオと、いずれかのユーザーが通話を PSTN エンドポイントに転送するシナリオを示しています。 一方のユーザーが通話を PSTN エンドポイントに転送した場合に、通話の転送先ユーザーの場所によって、場所に基づくルーティングが通話にどのように影響するかを表しています。

### <a name="call-transfer-or-forward-to-pstn-endpoint"></a>PSTN エンドポイントへの通話転送または着信転送

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>通話/着信転送エンドポイント ターゲット</th>
<th>同じネットワークサイト内の Lync ユーザー</th>
<th>異なるネットワークサイトの Lync ユーザー</th>
<th>不明のネットワークサイトまたはネットワークサイト内の一方または両方の Lync ユーザーが Location-Based ルーティング用に有効になっていない</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>PSTN エンドポイント</p></td>
<td><p>転送先ユーザーのサイトの音声ルーティング ポリシーによって、通話または着信の転送が許可される</p></td>
<td><p>転送先ユーザーのサイトの音声ルーティング ポリシーによって、通話または着信の転送が許可される</p></td>
<td><p>通話または着信の転送は、転送先ユーザーの音声ポリシーによって、場所に基づくルーティングが有効になっていないトランクのみを経由して許可される</p></td>
</tr>
</tbody>
</table>

  
たとえば、同じネットワークサイト内の別の Lync ユーザーとの通話で Lync ユーザーが通話を PSTN エンドポイントに転送し、通話転送が許可されているとします。

<div>

## <a name="see-also"></a>関連項目


[Lync Server 2013 の場所に基づくルーティングのシナリオ](lync-server-2013-scenarios-for-location-based-routing.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

