---
title: 'Lync Server 2013: メディアビュー'
description: 'Lync Server 2013: メディアビュー。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Media view
ms:assetid: 1a7b2e59-082e-4188-98ae-48ae9bd3494a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687981(v=OCS.15)
ms:contentKeyID: 49733570
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 74643986b12a30b1055a46a37febf90eeb70c514
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446038"
---
# <a name="media-view-in-lync-server-2013"></a>Lync Server 2013 でのメディアの表示

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-10-01_

メディアビューには、ピアツーピアセッションで使用される1つのメディアの種類に関する情報が格納されます。 複数のメディアの種類を使用している場合は、1つのセッションがテーブル内の複数のレコードで表されます。 このビューは、Microsoft Lync Server 2013 で導入されました。

<div>


> [!NOTE]  
> メディア表示は、セッションのメディア再生時間の計算に使用しないようにします。 このビューには、セッションでのメディア交換の通知の詳細が含まれています。 メディア交換は INVITE 要求によって実行され、StartTime は招待が送信された時間を示します。この招待時刻は、メディアの開始時刻を意味するわけではありません。これは、セッションが受け入れられた後にのみメディアが開始されるためです。



</div>

メディアビューには、 [Lync Server 2013 の Sessiondetails ビュー](lync-server-2013-sessiondetails-view.md) のすべての列に加えて、以下に示すものが含まれています。


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
<td><p><strong>メディア</strong></p></td>
<td><p>nvarchar(256)</p></td>
<td><p>メディアの種類。 詳細については、「 <a href="lync-server-2013-medialist-table.md">Lync Server 2013 の Medialist の表</a> 」を参照してください。</p></td>
</tr>
<tr class="even">
<td><p><strong>MediaStartTime</strong></p></td>
<td><p>datetime</p></td>
<td><p>メディア要求が送信された時刻。</p></td>
</tr>
<tr class="odd">
<td><p><strong>MediaEndTime</strong></p></td>
<td><p>datetime</p></td>
<td><p>セッションの終了時刻。</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

