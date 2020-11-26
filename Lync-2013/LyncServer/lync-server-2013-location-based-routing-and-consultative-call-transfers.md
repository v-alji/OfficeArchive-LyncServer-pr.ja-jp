---
title: 'Lync Server 2013: ルーティングと提案型通話の転送を Location-Based'
description: 'Lync Server 2013: ルーティングと提案型通話の転送 Location-Based。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Location-Based Routing and consultative call transfers
ms:assetid: b12460c2-36c8-481f-b867-fe10dc1c0bdf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362836(v=OCS.15)
ms:contentKeyID: 56335089
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0d07cf6a33ff4d6ad57f8913a798fac3bc393a00
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426559"
---
# <a name="location-based-routing-and-consultative-call-transfers-in-lync-server-2013"></a>Lync Server 2013 での Location-Based ルーティングとコンサルティングによる通話転送

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2013-07-31_

Location-Based ルーティング会議アプリケーションは、Lync 会議への Location-Based ルーティングを適用することに加えて、PSTN エンドポイントに送信されるコンサルティング呼び出しの転送に対して Location-Based ルーティングの制限を適用します。 お客様による発信は、2つの当事者間で確立された通話であり、一方の当事者が新しいユーザーに通話を転送します。 たとえば、PSTN エンドポイントはユーザー A (Lync 呼び出し元) を呼び出します。 ユーザー A は、PSTN ユーザーをユーザー B (Lync ユーザー) に転送する必要があることを決定します。 ユーザー A は、PSTN ユーザーとの通話を保留にし、ユーザー B を呼び出します。ユーザー B は PSTN ユーザーとの通信に同意します。 ユーザー A は、着信をユーザー B に転送します。

**取次通話転送の通話フロー**

![会議の位置情報に基づくルーティングの図](images/Dn362836.e4d43d6f-23d2-49c9-b12b-15248a743f92(OCS.15).jpg "会議の位置情報に基づくルーティングの図")

Location-Based ルーティングが有効になっている場合、PSTN エンドポイントのコンサルティング通話転送 (上の図を参照) が開始されます。これに Location-Based より、2つのアクティブな通話、PSTN ユーザーと Lync ユーザー A の間の通話、および Lync ユーザー A と Lync ユーザー B 間でのその他の操作が実行されます。

  - PSTN 通話をルーティングする SIP トランクが、Lync ユーザー B (つまり転送先) があるネットワークサイトへの PSTN 通話を再ルーティングすることを許可されている場合は、通話転送が許可されます。それ以外の場合は、コンサルティング着信の転送がブロックされます。 この承認は、転送された当事者が、PSTN エンドポイントへのアクティブな通話をルーティングしている SIP トランクと同じネットワークサイトに配置されている場所に基づいて行われます。

  - 受信した PSTN 通話の SIP トランクルーティングが、転送されたパーティ (Lync ユーザー B) が存在するか、または転送されたパーティが不明なネットワークサイトにある場合は、PSTN エンドポイントへの提案型コール転送 (つまり、着信転送ターゲット) はブロックされます。

次の表では、提案型の通話転送について、Location-Based ルーティング会議アプリケーションで Location-Based ルーティングの制限を適用する方法について説明します。 PBX エンドポイントはネットワーク サイトに直接関連付けられませんが、PBX の接続先の SIP トランクにネットワーク サイトが割り当てられる場合があります。 したがって、PBX エンドポイントがネットワーク サイトに間接的に関連付けられる場合があります。


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>通話転送を受ける側のネットワーク サイト</p></td>
<td><p>通話転送ターゲットのネットワーク サイト</p></td>
<td><p>動作</p></td>
</tr>
<tr class="even">
<td><p>PSTN エンドポイント</p></td>
<td><p>同じネットワークサイト内の Lync ユーザー (例: サイト 1)</p></td>
<td><p>取次転送が許可される</p></td>
</tr>
<tr class="odd">
<td><p>PSTN エンドポイント</p></td>
<td><p>異なるネットワークサイトの Lync ユーザー (例: サイト 2)</p></td>
<td><p>取次転送が許可されない</p></td>
</tr>
<tr class="even">
<td><p>PSTN エンドポイント</p></td>
<td><p>不明なネットワークサイトの Lync ユーザー</p></td>
<td><p>取次転送が許可されない</p></td>
</tr>
<tr class="odd">
<td><p>PSTN エンドポイント</p></td>
<td><p>フェデレーションされた Lync ユーザー</p></td>
<td><p>取次転送が許可されない</p></td>
</tr>
<tr class="even">
<td><p>PSTN エンドポイント</p></td>
<td><p>同じサイト (サイト 1) 内の PBX エンドポイント</p></td>
<td><p>取次転送が許可される</p></td>
</tr>
<tr class="odd">
<td><p>PSTN エンドポイント</p></td>
<td><p>別のサイト (サイト 2) 内の PBX エンドポイント</p></td>
<td><p>取次転送が許可されない</p></td>
</tr>
<tr class="even">
<td><p>同じサイト (サイト 1) 内の PBX エンドポイント</p></td>
<td><p>PSTN エンドポイント</p></td>
<td><p>取次転送が許可される</p></td>
</tr>
<tr class="odd">
<td><p>別のサイト (サイト 2) 内の PBX エンドポイント</p></td>
<td><p>PSTN エンドポイント</p></td>
<td><p>取次転送が許可されない</p></td>
</tr>
<tr class="even">
<td><p>任意のサイト内の PBX エンドポイント</p></td>
<td><p>同じネットワークサイト内の Lync ユーザー (例: サイト 1)</p></td>
<td><p>取次転送が許可される</p></td>
</tr>
<tr class="odd">
<td><p>任意のサイト内の PBX エンドポイント</p></td>
<td><p>異なるネットワークサイトの Lync ユーザー (例: サイト 2)</p></td>
<td><p>取次転送が許可される</p></td>
</tr>
<tr class="even">
<td><p>任意のサイト内の PBX エンドポイント</p></td>
<td><p>不明なネットワークサイトの Lync ユーザー</p></td>
<td><p>取次転送が許可される</p></td>
</tr>
<tr class="odd">
<td><p>任意のサイト内の PBX エンドポイント</p></td>
<td><p>フェデレーションされた Lync ユーザー</p></td>
<td><p>取次転送が許可される</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

