---
title: 'Lync Server 2013: 会議の Location-Based ルーティングの概要'
description: 'Lync Server 2013: 会議の Location-Based ルーティングの概要。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of Location-Based Routing for conferencing
ms:assetid: 8b86740e-db95-4304-bb83-64d0cbb91d47
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362815(v=OCS.15)
ms:contentKeyID: 56335084
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2a8fe9cdf4a797243c3ec04b3466011f374fb0d0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399681"
---
# <a name="overview-of-location-based-routing-for-conferencing-in-lync-server-2013"></a>Lync Server 2013 での会議の Location-Based ルーティングの概要

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2013-07-19_

Location-Based ルーティング会議アプリケーションは、PSTN の有料電話のバイパスを防止するメカニズムを Lync 会議に提供します。 アプリケーションは、参加している Lync ユーザーの場所に基づいて Location-Based ルーティングの制限を適用します。

次の条件が満たされている場合、Location-Based ルーティング会議アプリケーションによって、Lync 会議に Location-Based ルーティングが適用されるかどうかが決定されます。

  - 会議の開催者が Location-Based ルーティング用に有効になっている。 Location-Based ルーティングの制限は、Location-Based ルーティングが有効になっているユーザーによって開催された会議にのみ適用されます。

  - 少なくとも 1 人の会議参加者が PSTN エンドポイントである。 Location-Based ルーティングの制限は、PSTN エンドポイントを含む会議に対してのみ適用されます。

  - 会議と PSTN の橋渡しに使用される PSTN ゲートウェイがあるネットワーク サイトが、開催者と参加者の接続元のネットワーク サイトでもある。

Location-Based ルーティング会議アプリケーションは、異なるネットワークサイトから同じ電話会議への Lync ユーザーと PSTN エンドポイントの参加を防止します。 会議の開催者が Location-Based ルーティング用に有効になっている場合は、会議アプリケーションで次の制限が適用されます。

  - Lync 会議に参加できるエンドポイントは、既に会議に参加しているエンドポイントによって異なります。この制限は、参加したエンドポイントの退出と新しいエンドポイントが会議に参加すると調整されます。 開催者と参加者が同じネットワークサイトから Lync 会議に参加している場合、PSTN エンドポイント、同じネットワークサイトからの別の参加者、別のネットワークサイトからの別の参加者、または不明なネットワークサイトからの参加者の参加が許可されている場合。

  - 開催者と参加者が別のネットワーク サイトや不明なネットワーク サイトから会議に参加している場合、場所に基づくルーティングが有効な SIP トランクから PSTN 通話が入ると、PSTN エンドポイントは会議に参加できません。

  - 開催者と参加者が同じネットワークサイトから会議に参加していて、参加者が PSTN から同じ会議に参加している場合は、別のネットワークサイトの Lync エンドポイントで会議に参加することはできません。

これらの会議 Location-Based ルーティング制限は、次の表にまとめられています。


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>任意の時点の会議のユーザー</p></td>
<td><p>会議に参加できるユーザー</p></td>
<td><p>会議に参加できないユーザー</p></td>
</tr>
<tr class="even">
<td><p>1つのネットワークサイトからの Lync VoIP クライアントユーザー</p></td>
<td><p>同じネットワークサイトからの Lync VoIP クライアントユーザー</p>
<p>別のネットワークサイトからの Lync VoIP クライアントユーザー</p>
<p>不明のネットワークサイトからの Lync VoIP クライアントユーザー</p>
<p>フェデレーションされた Lync VoIP クライアントユーザー</p>
<p>PSTN エンドポイントから参加しているユーザー</p></td>
<td><p>なし</p></td>
</tr>
<tr class="odd">
<td><p>不明のネットワークサイトからの Lync VoIP クライアントユーザー</p></td>
<td><p>任意のサイトからの Lync VoIP クライアントユーザー</p>
<p>不明なサイトからの Lync VoIP クライアントユーザー</p>
<p>フェデレーションされた Lync VoIP クライアントユーザー</p></td>
<td><p>PSTN エンドポイント経由で参加しているユーザー</p></td>
</tr>
<tr class="even">
<td><p>異なるネットワークサイトの Lync VoIP クライアントユーザー</p></td>
<td><p>任意のネットワークサイトからの Lync VoIP クライアントユーザー</p>
<p>不明のネットワークサイトからの Lync VoIP クライアントユーザー</p>
<p>フェデレーションされた Lync VoIP クライアントユーザー</p></td>
<td><p>PSTN エンドポイント経由で参加しているユーザー</p></td>
</tr>
<tr class="odd">
<td><p>1つのネットワークサイトの Lync VoIP クライアントユーザーと PSTN エンドポイントからの参加ユーザー</p></td>
<td><p>同じネットワークサイトからの Lync VoIP クライアントユーザー</p></td>
<td><p>別のネットワークサイトからの Lync VoIP クライアントユーザー</p>
<p>不明のネットワークサイトからの Lync VoIP クライアントユーザー</p>
<p>フェデレーションされた Lync VoIP クライアントユーザー</p></td>
</tr>
</tbody>
</table>


Location-Based ルーティング会議アプリケーションのその他の特性を次に示します。

  - ユーザーが Location-Based ルーティングの制限を指定して会議に参加することを許可されていない場合、会議へのユーザー呼び出しは拒否され、その通話が完了していないか終了したことが Lync クライアントから報告されます。

  - Location-Based ルーティング enforcements を使って会議に参加している PSTN エンドポイントは、エンドポイントが Location-Based ルーティングが有効になっていないトランク経由で参加している場合、その状態に関係なく、会議への参加を制限されません。

  - PSTN への出口がない SIP トランク経由で Mediptserver に接続された PBX システムは、SIP トランクが定義されている同じネットワークサイトにある Lync ユーザーと同じ enforcements を持つことになります。 たとえば、PSTN エンドポイントは、PBX ユーザーと Lync ユーザーが同じネットワークサイトにある場合に、そのユーザーとの会議に参加することができます。そうしないと、PBX ユーザーが Lync ユーザーとは別のネットワークサイトにいる場合、PSTN エンドポイントは会議に参加できません。

</div>

<span> </span>

</div>

</div>

</div>

