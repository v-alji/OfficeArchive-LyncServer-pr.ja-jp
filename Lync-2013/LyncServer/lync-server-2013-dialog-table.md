---
title: 'Lync Server 2013: Dialog テーブル'
description: 'Lync Server 2013: ダイアログテーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Dialog table
ms:assetid: 4d93424f-9072-43f5-83c2-3d539e3e9ca6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398313(v=OCS.15)
ms:contentKeyID: 48184068
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7ae93b8ca9f1146b7dc164803f27cbeeadc66777
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429204"
---
# <a name="dialog-table-in-lync-server-2013"></a>Lync Server 2013 の Dialog テーブル

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-10-02_

ダイアログテーブルはサポートテーブルです。各レコードは、1つのセッション開始プロトコル (SIP) ダイアログを表します。


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>列</strong></th>
<th><strong>データ型</strong></th>
<th><strong>キー/インデックス</strong></th>
<th><strong>詳細</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>ConferenceDateTime</strong></p></td>
<td><p>datetime</p></td>
<td><p>Primary</p></td>
<td><p>卓越した品質 (QoE) エージェントが、呼び出し元または呼び出し元から最初のレポートを受け取る時刻。 セッションを一意に識別するために SessionSeq と組み合わせて使用されます。</p></td>
</tr>
<tr class="even">
<td><p><strong>SessionSeq</strong></p></td>
<td><p>int</p></td>
<td><p>Primary</p></td>
<td><p>セッションを区別するための順序番号 (同じ ConferenceDateTime がある場合)。</p></td>
</tr>
<tr class="odd">
<td><p><strong>この Id</strong></p></td>
<td><p>varchar (256)</p></td>
<td></td>
<td><p>グローバルに一意のダイアログ ID。</p></td>
</tr>
<tr class="even">
<td><p><strong>このチェックサム</strong></p></td>
<td><p>int</p></td>
<td><p>位置</p></td>
<td><p>ダイアログ ID のチェックサム。</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

