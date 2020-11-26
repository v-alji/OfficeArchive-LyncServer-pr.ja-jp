---
title: 'Lync Server 2013: tblPrincipalInvites'
description: 'Lync Server 2013: tblPrincipalInvites'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalInvites
ms:assetid: 548ec156-4d1a-469d-a804-62cff226e5c2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558650(v=OCS.15)
ms:contentKeyID: 48184141
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d30d741864ed2a3cfbec8329215be33c21b3b262
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423506"
---
# <a name="tblprincipalinvites-in-lync-server-2013"></a>Lync Server 2013 の tblPrincipalInvites

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-06-25_

tblPrincipalInvites には、自動招待を含むすべてのノードのプロビジョニングされたすべてのユーザーの招待が含まれます。

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
<td><p>invID</p></td>
<td><p>int (null ではない)</p></td>
<td><p>TblLastInviteId テーブルから生成された一意の連続番号 (プリンシパル ID ごと)。</p></td>
</tr>
<tr class="odd">
<td><p>nodeID</p></td>
<td><p>int (null ではない)</p></td>
<td><p>ノード ID (チャットルームのみ)。</p></td>
</tr>
<tr class="even">
<td><p>createdOn</p></td>
<td><p>datetime。 null ではありません</p></td>
<td><p>作成時刻。</p></td>
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
<td><p>&lt;prinID、nodeID&gt;</p></td>
<td><p>主キー。</p></td>
</tr>
<tr class="even">
<td><p>prinID</p></td>
<td><p>TblPrincipal Id テーブルで参照される外部キー。</p></td>
</tr>
<tr class="odd">
<td><p>nodeID</p></td>
<td><p>TblNode テーブルで参照される外部キー。</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

