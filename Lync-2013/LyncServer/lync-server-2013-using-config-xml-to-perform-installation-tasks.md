---
title: 'Lync Server 2013: Config.xml を使ってインストールタスクを実行する'
description: 'Lync Server 2013: Config.xml を使ってインストールタスクを実行します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using Config.xml to perform installation tasks
ms:assetid: 0813184a-ab40-417c-b3a3-c2090766b831
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204651(v=OCS.15)
ms:contentKeyID: 48183332
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 22fff14e21a120c3a0ee2cd6432fd1eba2bbee5f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438954"
---
# <a name="using-configxml-to-perform-installation-tasks-in-lync-server-2013"></a>Lync Server 2013 で Config.xml を使ってインストールタスクを実行する

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-10-02_

Office カスタマイズ ツール (OCT) はカスタマイズ インストール向けの主要ツールですが、管理者は OCT では使用できない追加のインストール手順を Config.xml ファイルによって指定できます。以下のカスタマイズは、Config.xml ファイルを使用しないと実行できません。

  - ネットワーク インストール ポイントのパスを指定する。

  - インストールする製品を選択する。

  - ログ記録や、セットアップ カスタマイズ ファイルおよびソフトウェア更新プログラムの場所を構成する。

  - インストール オプション (ユーザー名など) を指定する。

  - Office をインストールせずにローカル インストール ソース (LIS) をユーザーのコンピューターにコピーする。

  - インストールに対する言語の追加または削除を行う。

Config.xml ファイルを使用して、Lync 2013 サイレントインストールを構成することをお勧めします。

既定では、コア製品フォルダーに保存されている Config.xml ファイル (product など) が含まれ \\ ます。WW) その製品をインストールするようにセットアップに指示します。 たとえば、次のフォルダーの Config.xml ファイルには、Lync 2013 がインストールされます。

  - \\\\サーバー \\ 共有 \\ Lync15 \\ Lync \\Config.xml

Lync 2013 をインストールするためによく使用される Config.xml の要素を次の表に示します。

### <a name="configxml-elements"></a>Config.xml の要素

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>要素</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Configuration</p></td>
<td><p>トップレベルの要素 (必須)。 Product 属性 (製品 = Lync など) が含まれています。</p></td>
</tr>
<tr class="even">
<td><p>OptionState</p></td>
<td><p>インストール中、特定の製品の機能が処理される方法を指定します。 次の属性を使用して、Business Connectivity Services のインストールを防止します。これには、Outlook 2010 を妨害する共有コンポーネントが含まれます。</p>
<ul>
<li><p>Id = &quot; lobimain&quot;</p></li>
<li><p>都道府県 = &quot; 不在&quot;</p></li>
<li><p>子供 = &quot; 強制&quot;</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>Display</p></td>
<td><p>セットアップがユーザーに表示する UI のレベル。一般的には次の属性があります。</p>
<ul>
<li><p>&quot;"はい" の通知 = [ &quot;  |  &quot; いいえ] &quot; (既定)</p></li>
<li><p>AcceptEula = &quot; Yes &quot;  |  &quot; no &quot; (既定値)</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>Logging</p></td>
<td><p>セットアップが実行するログ記録の種類のオプション。一般的には次の属性があります。</p>
<ul>
<li><p>Type = &quot; Off &quot;  |  &quot; Standard &quot; (既定) | &quot;詳細な&quot;</p></li>
<li><p>Template=”filename.txt” (ログファイルの名前)</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>Setting</p></td>
<td><p>Windows インストーラーのプロパティの値を指定します。一般的には次の属性があります。</p>
<ul>
<li><p>設定 Id = &quot; name &quot; (Windows Installer プロパティの名前)</p></li>
<li><p>Value = &quot; value &quot; (プロパティに割り当てる値)</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>DistributionPoint</p></td>
<td><p>インストールを実行するネットワーク インストール ポイントの完全修飾パス</p>
<ul>
<li><p>Location=” path”</p></li>
</ul></td>
</tr>
</tbody>
</table>


次の例は、Lync 2013 の一般的なサイレントインストールの Config.xml ファイルを示しています。

    <Configuration Product="Lync">
      <OptionState Id="LOBiMain" State="Absent" Children="Force" />
      <Display Level="None" CompletionNotice="No" AcceptEula="Yes" />
      <Logging Type="verbose" Path="%temp%" Template="LyncSetupVerbose(*).log" />
      <Setting Id="SETUP_REBOOT" Value="Never" />
      <DistributionPoint Location="\\server\share\Lync15" />
    </Configuration>

Config.xml ファイルを使用して Office のインストールとメンテナンスタスクを実行する方法の詳細については、を参照して <https://go.microsoft.com/fwlink/p/?linkid=267514> ください。

<div>

## <a name="to-customize-the-configxml-file"></a>Config.xml ファイルをカスタマイズするには

1.  Notepad などのテキスト エディター ツールで Config.xml ファイルを開きます。

2.  変更する要素を含む行に移動します。

3.  使用するサイレント オプションで要素のエントリを変更します。 コメントの区切り文字 "" を削除していることを確認してください \<\!--" and "--\> 。 たとえば、次の構文を使用します。
    
        < DistributionPoint Location="\\server\share\Lync15" />

4.  Config.xml ファイルを保存します。

</div>

</div>

<span> </span>

</div>

</div>

</div>

