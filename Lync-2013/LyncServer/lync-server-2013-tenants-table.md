---
title: 'Lync Server 2013: Tenants テーブル'
description: 'Lync Server 2013: テナントのテーブル。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Tenants table
ms:assetid: c1b070c1-2c59-4ca9-910b-43f673f97fda
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412950(v=OCS.15)
ms:contentKeyID: 48185309
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 96025dfd9fb42a6083f7f3daca98e243f01a8516
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441285"
---
# <a name="tenants-table-in-lync-server-2013"></a>Lync Server 2013 の Tenants テーブル

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-09-28_

テナントの表は、さまざまなテナントの一覧を格納するサポートテーブルです。 テーブル内の各レコードは、1つのテナントを表します。

<div>


> [!NOTE]  
> オンプレミスの展開では、CDR はビルトインのテナント ID を使用して、パブリック IM 接続、フェデレーション、匿名など、さまざまな認証の種類を示します。



</div>


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
<td><p><strong>テナント</strong></p></td>
<td><p>int</p></td>
<td><p>Primary</p></td>
<td><p>このテナント ID を識別する一意の番号です。</p></td>
</tr>
<tr class="even">
<td><p><strong>TenantKey</strong></p></td>
<td><p>nvarchar(256)</p></td>
<td></td>
<td><p>許可される値:</p>
<ul>
<li><p>00000000-0000-0000-0000-000000000000 – Enterprise</p></li>
<li><p>00000000-0000-0000-0000-000000000001 –フェデレーション</p></li>
<li><p>00000000-0000-0000-0000-000000000002 –匿名</p></li>
<li><p>00000000-0000-0000-0000-000000000003 –パブリック IM 接続</p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

