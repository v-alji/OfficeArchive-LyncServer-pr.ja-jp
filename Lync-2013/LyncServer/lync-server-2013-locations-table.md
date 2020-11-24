---
title: 'Lync Server 2013: Locations テーブル'
description: 'Lync Server 2013: 場所テーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Locations table
ms:assetid: 78dc1b14-5394-4f8e-89d3-4ba593272a04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398596(v=OCS.15)
ms:contentKeyID: 48184579
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9d07b6d3d3820f4efb3310adf0734a7e10c53e6d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399831"
---
# <a name="locations-table-in-lync-server-2013"></a>Lync Server 2013 の Locations テーブル

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-05-25_

各レコードは、E9 通話のような緊急通話での1つの場所参照を表します。


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
<td><p><strong>セッション Id</strong></p></td>
<td><p>datetime</p></td>
<td><p>プライマリ、外部</p></td>
<td><p>セッション要求の時刻。 セッションを一意に識別するために <strong>Sessionidseq</strong> と組み合わせて使用されます。 詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</p></td>
</tr>
<tr class="even">
<td><p><strong>SessionIdSeq</strong></p></td>
<td><p>int</p></td>
<td><p>プライマリ、外部</p></td>
<td><p>セッションを識別する ID 番号。 セッションを一意に識別するために <strong>Sessionidtime</strong> と組み合わせて使用されます。 詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</p></td>
</tr>
<tr class="odd">
<td><p><strong>場所</strong></p></td>
<td><p>nvarchar (max)</p></td>
<td></td>
<td><p>緊急通話の場所。</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

