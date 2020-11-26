---
title: 'Lync Server 2013: FileTransfers ビュー'
description: 'Lync Server 2013: FileTransfers ビュー。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: FileTransfers view
ms:assetid: e52c3ad0-152e-4a18-af1c-1aff0d205151
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721914(v=OCS.15)
ms:contentKeyID: 49733848
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dd2b084274a4d5daa093f2269617214f703ac03e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428154"
---
# <a name="filetransfers-view-in-lync-server-2013"></a>Lync Server 2013 の FileTransfers ビュー

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-10-01_

FileTransfer ビューには、ピアツーピアファイル転送セッションに関する情報が格納されます。 このビューは、Microsoft Lync Server 2013 で導入されました。

<div>


> [!NOTE]  
> FileTransfers ビューには、 <A href="lync-server-2013-sessiondetails-view.md">Lync Server 2013 の Sessiondetails ビュー</A> のすべての列に加えて、以下の列も含まれています。



</div>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>列</th>
<th>データ型</th>
<th>詳細</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>FileName</strong></p></td>
<td><p>nvarchar(256)</p></td>
<td><p>転送されたファイルの名前。</p></td>
</tr>
<tr class="even">
<td><p><strong>クッキー</strong></p></td>
<td><p>nvarchar(128</p></td>
<td><p>すべてのフォローアップメッセージをこのメールに関連付けられているものとして識別するために使用されます。</p></td>
</tr>
<tr class="odd">
<td><p><strong>FileIdentity</strong></p></td>
<td><p>長さ</p></td>
<td><p>同じファイル名を含むファイル転送を区別する一意の識別子。</p></td>
</tr>
<tr class="even">
<td><p><strong>受諾</strong></p></td>
<td><p>bit</p></td>
<td><p>TRUE または NULL を指定できます。 TRUE の場合は、拒否とキャンセルは NULL になります。</p></td>
</tr>
<tr class="odd">
<td><p><strong>拒否</strong></p></td>
<td><p>bit</p></td>
<td><p>TRUE または NULL を指定できます。 TRUE の場合は、Accept と Cancel は NULL になります。</p></td>
</tr>
<tr class="even">
<td><p><strong>キャンセル</strong></p></td>
<td><p>bit</p></td>
<td><p>TRUE または NULL を指定できます。 TRUE の場合は、Accept と Reject は NULL になります。</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

