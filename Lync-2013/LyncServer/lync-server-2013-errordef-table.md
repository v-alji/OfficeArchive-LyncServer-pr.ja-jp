---
title: 'Lync Server 2013: ErrorDef テーブル'
description: 'Lync Server 2013: ErrorDef テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ErrorDef table
ms:assetid: 6acf3b86-da61-4923-9812-300db6f66dec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398503(v=OCS.15)
ms:contentKeyID: 48184403
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e58980a671b54007012bbbf6780e24c162aebe00
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428539"
---
# <a name="errordef-table-in-lync-server-2013"></a>Lync Server 2013 ErrorDef テーブル

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-05-25_

ErrorDef テーブルには、発生する可能性がある各エラーの種類に関する情報が格納されます。 各レコードは1種類のエラーです。


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>列</th>
<th>データ型</th>
<th>キー/インデックス</th>
<th>詳細</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>ErrorId</strong></p></td>
<td><p>int</p></td>
<td><p>Primary</p></td>
<td><p>この種類のエラーを識別する固有の ID 番号。</p></td>
</tr>
<tr class="even">
<td><p><strong>返信</strong></p></td>
<td><p>int</p></td>
<td><p> </p></td>
<td><p>このエラーに関連付けられた標準 SIP 応答コード。</p></td>
</tr>
<tr class="odd">
<td><p><strong>MsDiagId</strong></p></td>
<td><p>int</p></td>
<td><p> </p></td>
<td><p>Microsoft 診断 ID。</p></td>
</tr>
<tr class="even">
<td><p><strong>発信者の Typeid</strong></p></td>
<td><p>Int</p></td>
<td><p>外部</p></td>
<td><p>通話の種類。 詳細については、「 <a href="lync-server-2013-calltype-table.md">Lync Server 2013 の CallType テーブル</a> 」を参照してください。</p></td>
</tr>
<tr class="odd">
<td><p><strong>RequestType</strong></p></td>
<td><p>varbinary (33)</p></td>
<td><p> </p></td>
<td><p>失敗した要求の種類。</p>
<p>このデータは、次の構文を使用してテキスト形式に変換できます。</p>
<p><code>cast(cast(RequestType as varbinary(max)) as varchar(max))</code></p></td>
</tr>
<tr class="even">
<td><p><strong>ContentType</strong></p></td>
<td><p>varbinary (257)</p></td>
<td><p> </p></td>
<td><p>失敗した要求のコンテンツタイプ。</p>
<p>このデータは、次の syntaxt を使用してテキスト形式に変換できます。</p>
<p><code>cast(cast(ContentType as varbinary(max)) as varchar(max))</code></p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

