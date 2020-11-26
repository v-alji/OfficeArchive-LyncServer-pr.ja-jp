---
title: 'Lync Server 2013: Pools テーブル'
description: 'Lync Server 2013: プールテーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Pools table
ms:assetid: e0632b8d-e23a-4365-8a7a-6ca0957a46a9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398991(v=OCS.15)
ms:contentKeyID: 48185680
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a587eba6798121f39fe64ff8bd720b62e9311ec0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424409"
---
# <a name="pools-table-in-lync-server-2013"></a>Lync Server 2013 の Pools テーブル

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2010-11-09_

プールテーブルは、さまざまなプールに関する情報を格納するサポートテーブルです。 テーブル内の各レコードは、1つのプールを表します。


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
<td><p><strong>PoolId</strong></p></td>
<td><p>int</p></td>
<td><p>Primary</p></td>
<td><p>このプールを識別する一意の番号。</p></td>
</tr>
<tr class="even">
<td><p><strong>PoolFQDN</strong></p></td>
<td><p>nvarchar(256)</p></td>
<td><p> </p></td>
<td><p>プールの FQDN。</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

