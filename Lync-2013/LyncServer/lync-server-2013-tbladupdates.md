---
title: 'Lync Server 2013: tblADUpdates'
description: 'Lync Server 2013: tblADUpdates'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblADUpdates
ms:assetid: ba19fa16-4d2d-4635-ac32-f93e09469546
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615033(v=OCS.15)
ms:contentKeyID: 48185227
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7ab4418a10eac283d0f39d09b1c1fe15a32b2e68
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444484"
---
# <a name="tbladupdates-in-lync-server-2013"></a>Lync Server 2013 の tblADUpdates

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-09-12_

tblADUpdates には、以降の Active Directory 同期手順でまだ処理されていない Active Directory ドメインサービスの変更が含まれています。

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
<td><p>prinGuid</p></td>
<td><p>GUID、null ではない</p></td>
<td><p>変更されたオブジェクトのプリンシパル GUID。</p></td>
</tr>
<tr class="even">
<td><p>prinADPath</p></td>
<td><p>nvarchar (384)、null ではない</p></td>
<td><p>オブジェクトの識別名。</p></td>
</tr>
<tr class="odd">
<td><p>Prin属性が変更されました</p></td>
<td><p>ビット、null ではない</p></td>
<td><p>オブジェクトの少なくとも1つの属性が変更された場合は True です。</p></td>
</tr>
<tr class="even">
<td><p>prinMembersChanged</p></td>
<td><p>ビット、null ではない</p></td>
<td><p>メンバーシップが変更された場合は True です。</p></td>
</tr>
<tr class="odd">
<td><p>prinAffiliationsChanged</p></td>
<td><p>ビット、null ではない</p></td>
<td><p>使用されません。</p></td>
</tr>
<tr class="even">
<td><p>プリントが削除されました</p></td>
<td><p>ビット、null ではない</p></td>
<td><p>オブジェクトが削除された場合は True。</p></td>
</tr>
<tr class="odd">
<td><p>最終更新日</p></td>
<td><p>datetime。 null ではありません</p></td>
<td><p>行が挿入された時刻のタイムスタンプ。</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

