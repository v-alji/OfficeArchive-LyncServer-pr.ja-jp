---
title: 'Lync Server 2013: tblSkippedAffiliations'
description: 'Lync Server 2013: tblSkippedAffiliations'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblSkippedAffiliations
ms:assetid: 0b129b54-a7a8-42a6-9279-0e08410c06ec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558611(v=OCS.15)
ms:contentKeyID: 48183373
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 31746cee7302d34a1d19b3059ca1da6beab9345d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399806"
---
# <a name="tblskippedaffiliations-in-lync-server-2013"></a>Lync Server 2013 の tblSkippedAffiliations

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-09-12_

tblSkippedAffiliations には、読み取ることができなかった所属先が含まれています (通常は Active Directory ドメインサービスアクセスエラーが原因です)。

### <a name="columns"></a>行

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>列</th>
<th>型</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>prinID</p></td>
<td><p>int (null ではない)</p></td>
<td><p>プリンシパル ID。</p></td>
</tr>
<tr class="even">
<td><p>影響の説明</p></td>
<td><p>nvarchar (256)、null ではない</p></td>
<td><p>所属を識別する文字列。</p>
<p>形式は次のとおりです: guid: {0} uri: {1} &gt; id:{2}</p></td>
</tr>
<tr class="odd">
<td><p>updatedBy</p></td>
<td><p>int (null ではない)</p></td>
<td><p>この行を更新したプリンシパルの ID です。 Active Directory 同期がこれらのエントリの唯一のソースであるため、常に 1 (システムユーザー) になります。</p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a>機能

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>列</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>&lt;prinID、の影響の説明&gt;</p></td>
<td><p>主キー。</p></td>
</tr>
<tr class="even">
<td><p>prinID</p></td>
<td><p>TblPrincipal Id テーブルで参照される外部キー。</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

