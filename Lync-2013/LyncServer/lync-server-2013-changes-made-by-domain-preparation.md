---
title: 'Lync Server 2013: ドメインの準備によって行われた変更'
description: 'Lync Server 2013: ドメインの準備によって行われた変更。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Changes made by domain preparation
ms:assetid: 9191221e-6166-4c2b-837e-fa73d90fdf80
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398742(v=OCS.15)
ms:contentKeyID: 48184845
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 26400bd1c72c6ae3b8dc1f2d2d8f6c6906b80595
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435118"
---
# <a name="changes-made-by-domain-preparation-in-lync-server-2013"></a>Lync Server 2013 でのドメインの準備によって行われた変更

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2010-10-18_

次の表に、ドメインの準備でドメインルート上に作成されるアクセス制御エントリ (Ace) を示します。 特に注記がない限り、すべての Ace が継承されます。

<div id="sectionSection0" class="section">

### <a name="aces-added-to-domain-root"></a>ドメインルートに追加された Ace

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th>AS</th>
<th>RTCUniversal-UserReadOnly-グループ</th>
<th>RTCUniversal-ServerReadOnly-グループ</th>
<th>RTCUniversal-UserAdmins</th>
<th>RTCHSUniversal-Services</th>
<th>Authenticated-Users</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>読み取りコンテナー (継承されません)</p></td>
<td><p><strong>はい</strong></p></td>
<td><p><strong>はい</strong></p></td>
<td><p>いいえ</p></td>
<td><p>いいえ</p></td>
<td><p>いいえ</p></td>
</tr>
<tr class="even">
<td><p>ユーザー PropertySet の読み取りユーザーアカウントの制限</p></td>
<td><p><strong>はい</strong></p></td>
<td><p>いいえ</p></td>
<td><p>いいえ</p></td>
<td><p>いいえ</p></td>
<td><p>いいえ</p></td>
</tr>
<tr class="odd">
<td><p>ユーザー PropertySet Personal-Information を読む</p></td>
<td><p><strong>はい</strong></p></td>
<td><p>いいえ</p></td>
<td><p>いいえ</p></td>
<td><p>いいえ</p></td>
<td><p>いいえ</p></td>
</tr>
<tr class="even">
<td><p>ユーザー PropertySet General-Information を読む</p></td>
<td><p><strong>はい</strong></p></td>
<td><p>いいえ</p></td>
<td><p>いいえ</p></td>
<td><p>いいえ</p></td>
<td><p>いいえ</p></td>
</tr>
<tr class="odd">
<td><p>ユーザー PropertySet Public-Information を読む</p></td>
<td><p><strong>はい</strong></p></td>
<td><p>いいえ</p></td>
<td><p>いいえ</p></td>
<td><p>いいえ</p></td>
<td><p>いいえ</p></td>
</tr>
<tr class="even">
<td><p>ユーザー PropertySet RTCUserSearchProperty-Set を読む</p></td>
<td><p><strong>はい</strong></p></td>
<td><p>いいえ</p></td>
<td><p>いいえ</p></td>
<td><p>いいえ</p></td>
<td><p><strong>はい</strong></p></td>
</tr>
<tr class="odd">
<td><p>ユーザー PropertySet RTCPropertySet を読む</p></td>
<td><p><strong>はい</strong></p></td>
<td><p>いいえ</p></td>
<td><p>いいえ</p></td>
<td><p>いいえ</p></td>
<td><p>いいえ</p></td>
</tr>
<tr class="even">
<td><p>ユーザープロパティ Proxy-Addresses の書き込み</p></td>
<td><p>いいえ</p></td>
<td><p>いいえ</p></td>
<td><p><strong>はい</strong></p></td>
<td><p>いいえ</p></td>
<td><p>いいえ</p></td>
</tr>
<tr class="odd">
<td><p>ユーザー PropertySet の書き込み RTCUserSearchProperty-Set</p></td>
<td><p>いいえ</p></td>
<td><p>いいえ</p></td>
<td><p><strong>はい</strong></p></td>
<td><p>いいえ</p></td>
<td><p>いいえ</p></td>
</tr>
<tr class="even">
<td><p>ユーザー PropertySet の書き込み RTCPropertySet</p></td>
<td><p>いいえ</p></td>
<td><p>いいえ</p></td>
<td><p><strong>はい</strong></p></td>
<td><p>いいえ</p></td>
<td><p>いいえ</p></td>
</tr>
<tr class="odd">
<td><p>PropertySet の DS-レプリケーション-すべての Active Directory オブジェクトの変更内容を確認する</p></td>
<td><p>いいえ</p></td>
<td><p>いいえ</p></td>
<td><p>いいえ</p></td>
<td><p><strong>はい</strong></p></td>
<td><p>いいえ</p></td>
</tr>
</tbody>
</table>


次の表は、3つの組み込みコンテナー (ユーザー、コンピューター、ドメインコントローラー) で、ドメインの準備によって作成される Ace を示しています。 特に注記がない限り、すべての Ace が継承されます。

### <a name="aces-added-to-built-in-containers"></a>組み込みのコンテナーに追加された Ace

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>AS</th>
<th>RTCUniversal-UserReadOnly-グループ</th>
<th>RTCUniversal-ServerReadOnly-グループ</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>読み取りコンテナー (継承されません)</p></td>
<td><p><strong>はい</strong></p></td>
<td><p><strong>はい</strong></p></td>
</tr>
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</div>

