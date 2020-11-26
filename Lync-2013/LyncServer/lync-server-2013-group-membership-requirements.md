---
title: 'Lync Server 2013: グループ メンバーシップの要件'
description: 'Lync Server 2013: グループメンバーシップの要件。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Group membership requirements
ms:assetid: 01876843-8717-4e72-baf5-866ac8cceee6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204623(v=OCS.15)
ms:contentKeyID: 48183239
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3f18fb6fbc782ecd41b7a782965f2cd6a82f6fd5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427839"
---
# <a name="group-membership-requirements-for-lync-server-2013"></a>Lync Server 2013 のグループ メンバーシップの要件

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-10-05_

次の表は、Lync Server 2013 を正常にインストール、管理、トラブルシューティングするために、ユーザーが所属する必要があるグループをまとめたものです。


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Lync Server 2013 実行可能ファイル</th>
<th>グループメンバーシップが必要です</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Setup.exe</strong> – Lync Server 2013 管理ツールのインストールを開始する実行可能ファイル。</p></td>
<td><p>実行可能ファイルを実行しているコンピューターのローカル管理者グループのメンバー。 Active Directory ドメインサービスの情報を読み取るためのドメインユーザーグループのメンバー。 ローカルコンピューターで必須の MSI パッケージを自動的にインストールするためには、プログラムファイルディレクトリなどの保護されたローカルコンピューターリソースの読み取りと書き込みを許可する特権が必要です。また、ローカルコンピューターハイブなどの保護されたレジストリについても、このレベルのアクセス許可が必要です。</p>
<div>

> [!TIP]  
> また、ドメイン管理者グループのメンバーシップを付与しないユーザーまたはグループに、セットアップのアクセス許可を委任することもできます。 詳細については、展開ドキュメントの「 <A href="lync-server-2013-granting-setup-permissions.md">Lync Server 2013 でのセットアップ権限の付与</A> 」を参照してください。


</div></td>
</tr>
<tr class="even">
<td><p><strong>Deploy.exe</strong> – setup.exe によって呼び出される deploy.exe は、サーバーの役割のソフトウェアコンポーネントの展開を担当します。</p></td>
<td><p>実行可能ファイルを実行しているコンピューターのローカル管理者グループのメンバー。 ドメインユーザーグループのメンバーで、AD DS の情報を読み取ります。 ローカルコンピューターで必須の MSI パッケージを自動的にインストールするためには、プログラムファイルディレクトリなどの保護されたローカルコンピューターリソースの読み取りと書き込みを許可する特権が必要です。また、ローカルコンピューターハイブなどの保護されたレジストリについても、このレベルのアクセス許可が必要です。 中央管理ストアを読むには、RtcUniversalReadOnlyAdmins group のメンバーシップが必要です。</p>
<div>

> [!NOTE]  
> Windows Vista オペレーティングシステムまたは Windows 7 オペレーティングシステムを実行している場合は、ユーザーアカウント制御 (UAC) によってインストールを続行するかどうかを確認するメッセージが表示されます。 標準ユーザーアカウントでログオンしている場合は、ソフトウェアをインストールする権限を持つアカウントの入力を求められたときに、資格情報を提供するために、ローカル管理者グループのメンバーであるユーザーが必要になります。


</div></td>
</tr>
<tr class="odd">
<td><p><strong>Bootstrapper.exe</strong> – setup.exe によって呼び出される bootstrapper.exe は、サーバーの役割の展開と構成を担当します。</p></td>
<td><p>実行可能ファイルを実行しているコンピューターのローカル管理者グループのメンバー。 Bootstrapper.exe を実行する RTCUniversalServerAdmins グループのメンバー。 ドメインユーザーグループのメンバーで、AD DS の情報を読み取ります。 ローカルコンピューターで必須の MSI パッケージを自動的にインストールするためには、プログラムファイルディレクトリなどの保護されたローカルコンピューターリソースの読み取りと書き込みを許可する特権が必要です。また、ローカルコンピューターハイブなどの保護されたレジストリについても、このレベルのアクセス許可が必要です。</p></td>
</tr>
<tr class="even">
<td><p><strong>TopologyBuilder</strong> – Lync Server 2013 トポロジの作成、表示、調整、検証を行うためのウィザードベースのユーザーインターフェイス。</p></td>
<td><p>トポロジを表示するために、実行可能ファイルを実行しているコンピューターのローカル管理者グループのメンバー。 構成の設定を変更する RTCUniversalServerAdmins グループのメンバー。 トポロジを公開するには、RTCUniversalServerAdmins group と Domain Admins グループのメンバー、または RTCUniversalServerAdmins グループのメンバー (グループに委任の設定権限が付与されている場合のみ)。 RTCUniversalServerAdmins グループのメンバーが、ドメイン管理者グループのメンバーにならずにトポロジを公開できるようにするための委任セットアップのアクセス許可の詳細については、「展開ドキュメントの「 <a href="lync-server-2013-granting-setup-permissions.md">Lync Server 2013 でのセットアップアクセス許可の付与</a> 」を参照してください。</p></td>
</tr>
<tr class="odd">
<td><p><strong>AdminUIHost</strong> – Lync Server 2013 を管理するための Web ベースのグラフィカルユーザーインターフェイスです。</p></td>
<td><p>特定の管理タスクが割り当てられている、他の役割ベースのアクセス制御 (RBAC) 役割のメンバー。 CsAdministrator グループまたはメンバー。 Lync Server 2013 コントロールパネルでは、Lync Server 2013 Management Shell コマンドレットを実行することで、構成の変更を実装します。 定義済みの役割と、コマンドレットのメンバーの実行を許可する方法については、計画ドキュメントの「 <a href="lync-server-2013-planning-for-role-based-access-control.md">Lync Server 2013 でのロールベースのアクセス制御の計画</a> 」を参照してください。</p></td>
</tr>
<tr class="even">
<td><p>Lync server <strong>2013 モジュールを読み込み</strong>ました。 lync server 2013 の管理に固有のコマンドレットを使用して、コマンドライン管理ツールをPowerShell.exe します。</p></td>
<td><p>特定のコマンドレットが割り当てられている CsAdministrator グループまたは別の RBAC 役割のメンバー。 定義済みの役割と、コマンドレットのメンバーの実行を許可する方法については、計画ドキュメントの「 <a href="lync-server-2013-planning-for-role-based-access-control.md">Lync Server 2013 でのロールベースのアクセス制御の計画</a> 」を参照してください。</p>
<p>または、コマンドレットに応じて、次の1つまたは複数のグループのメンバーになります。</p>
<ul>
<li><p>RTCUniversalServerAdmins</p></li>
<li><p>RTCUniversalUserAdmins</p></li>
<li><p>RTCUniversalReadOnlyAdmins</p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

