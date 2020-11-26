---
title: 'Lync Server 2013: グループチャットを監視する'
description: 'Lync Server 2013: グループチャットを監視します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Monitoring group chat
ms:assetid: bddcf0be-ebf3-46bc-90c7-2576877734fb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720924(v=OCS.15)
ms:contentKeyID: 63969648
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 625e45f455e8dba50a5fa64240b62cb010623d16
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425424"
---
# <a name="monitoring-group-chat-in-lync-server-2013"></a>Lync Server 2013 でグループチャットを監視する

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2014-08-04_

パフォーマンスを向上させるには、Microsoft ダウンロードセンターで入手できる最新の [累積サーバー更新プログラムインストーラー](https://support.microsoft.com/kb/968802) を実行することを強くお勧めします。

最新の累積更新プログラムを実行していることを前提として、グループチャットサーバーが最適な状態で実行されているかどうかを判断するために、メトリックについて次のストレステストテーブルを使用します。

### <a name="test-environment-and-user-model"></a>環境とユーザーモデルのテスト

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>グループチャットプール内の3つのグループチャットサーバ、それぞれに 8 GB のメモリと8個のプロセッサが搭載されています。</p></td>
</tr>
<tr class="even">
<td><p>Enterprise Edition での2台の Lync Server 2013 フロントエンド。</p></td>
</tr>
<tr class="odd">
<td><p>6万で3つのグループチャットサーバに同時に接続できます。</p></td>
</tr>
<tr class="even">
<td><p>グループチャットプールによってホストされている25000チャネル。</p></td>
</tr>
<tr class="odd">
<td><p>チャンネルサイズ:</p>
<ul>
<li><p>小さいチャンネルサイズ:30</p></li>
<li><p>ミディアムチャネルサイズ: 150</p></li>
<li><p>大きいチャンネルサイズ: 2500</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>チャネル数:</p>
<ul>
<li><p>小さいチャンネル数: 24000</p></li>
<li><p>数値媒体チャネル800</p></li>
<li><p>大きいチャンネルの番号24</p></li>
<li><p>チャネルの合計24824</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>チャネルの招待:</p>
<ul>
<li><p>チャンネルがチャンネルを招待した残りのチャネル</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>ユーザーが参加するチャネルの数:</p>
<ul>
<li><p>小:12</p></li>
<li><p>中: 2</p></li>
<li><p>大: 1</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>参加率:</p>
<ul>
<li><p>サーバーあたり10合計/秒、3.33/秒</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>ログアウト率:</p>
<ul>
<li><p>サーバーあたり10合計/秒、3.33/秒</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>チャット料金:</p>
<ul>
<li><p>1サーバーあたり20合計/秒、6.66/秒</p></li>
</ul></td>
</tr>
</tbody>
</table>


<div>


> [!IMPORTANT]  
> ハードウェア仕様またはユーザープロファイルが異なる場合、次のパフォーマンスカウンターの数値が異なる可能性があります。



</div>

### <a name="performance-counter-to-be-monitored"></a>監視対象のパフォーマンスカウンター

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>パフォーマンス カウンター</th>
<th>しきい値</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>プロセス (ChannelService)- &gt; プロセッサ時間の割合</p></td>
<td><p>Min: 0</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

