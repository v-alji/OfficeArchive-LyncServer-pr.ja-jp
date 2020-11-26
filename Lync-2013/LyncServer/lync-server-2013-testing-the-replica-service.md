---
title: 'Lync Server 2013: レプリカサービスをテストする'
description: 'Lync Server 2013: レプリカサービスをテストしています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing the replica service
ms:assetid: 4ff2cc91-0036-4c5a-9792-7bf43d8ce18d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727303(v=OCS.15)
ms:contentKeyID: 63969600
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a61751b95115da3d6519f20f52262b7159ffcbfe
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440977"
---
# <a name="testing-the-replica-service-in-lync-server-2013"></a>Lync Server 2013 でのレプリカサービスのテスト

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2014-11-03_


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>確認のスケジュール</p></td>
<td><p>[毎日]</p></td>
</tr>
<tr class="even">
<td><p>テストツール</p></td>
<td><p>Windows PowerShell</p></td>
</tr>
<tr class="odd">
<td><p>必要なアクセス許可</p></td>
<td><p>Lync Server 管理シェルを使用してローカルで実行する場合、ユーザーは RTCUniversalServerAdmins セキュリティグループのメンバーである必要があります。</p>
<p>Windows PowerShell のリモートインスタンスを使用して実行する場合、ユーザーには、 <strong>CsReplica</strong> コマンドレットを実行するためのアクセス許可が与えられた RBAC の役割を割り当てる必要があります。 このコマンドレットを使うことができるすべての RBAC ロールの一覧を表示するには、Windows PowerShell プロンプトから次のコマンドを実行します。</p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsReplica&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a>説明

**Test CsReplica** コマンドレットは、Lync Server 2013 レプリカサービスがローカルコンピューターで実行されていることを確認します。 **Test CsReplica** コマンドレットは、次のようなタスクを実行します。

  - レプリケーターエージェントと集中ログエージェントサービスの状態を確認する

  - 必要なポートが Windows ファイアウォールで開かれていることを確認する

  - 必要な Active Directory とローカルコンピューターのセキュリティグループが存在することを確認します。

このコマンドレットはローカルで実行する必要があることに注意してください。 つまり、レプリカサービスが実行されているコンピューターで実行されている必要があります。 リモートサーバーに対してテスト用の **CsReplica** コマンドレットを実行するためのオプションはありません。

</div>

<div>

## <a name="running-the-test"></a>テストの実行

例1に示すコマンドは、ローカルコンピューターの Lync Server 2013 レプリカサービスをテストします。 この例では、Verbose パラメーターを使用して、テストの最終的なエラー、テストの成否、テストによって生成されたレポートの場所など、テストに関する情報が画面に表示されることを保証します。

    Test-CsReplica -Verbose

例2は、例1で示したコマンドの変形です。 この場合、レポートパラメーターは、テストによって生成されたレポートのフォルダーパスと名前を指定するために含まれています。 レポートパスを指定しない場合、次のような自動生成名がレポートに表示されます。

C: \\ \\ Litwareinc \\ AppData \\ ローカル \\ Temp \\ 1 \\Test-Cs-Replica-3db40ee0-4b5d-4f58-8d3d-b1e61253129e.html

    Test-CsReplica -Verbose -Report C:\Logs\ReplicaTest.html

</div>

<div>

## <a name="determining-success-or-failure"></a>成功または失敗を確認する

セクションの本文をここに挿入します。

冗長: 新しいログファイルの作成 "C: \\ ユーザーが \\ \\ AppData \\ ローカル \\ Temp \\Test-CsReplica-3cb066b3-dd23-411a-8932-99f01c0f940c.xml をテストしています。

冗長: 新しいログファイルの作成 "C: \\ ユーザーが \\ \\ AppData \\ ローカル \\ Temp \\Test-CsReplica-3cb066b3-dd23-411a-8932-99f01c0f940c.xml をテストしています。

VERBOSE: "Test-CsReplica" 処理は正常に完了しました。

詳細: 詳細な結果は、"C: \\ ユーザーが \\ \\ AppData \\ ローカル \\ 一時 \\Test-CsReplica-3cb066b3-dd23-411a-8932-99f01c0f940c.xml をテストしている" という説明を参照してください。

VERBOSE: 新しいログファイルを作成しています

"C: \\ \\ \\ AppData \\ ローカル \\ Temp \\ 2 \\ テスト-csreplica-29fddb35-f56e-4e3c-8f4c-e

d3bd0e4a083.xml] を選びます。

VERBOSE: 新しいログファイルを作成しています

"C: \\ \\ \\ AppData \\ ローカル \\ Temp \\ 2 \\ テスト-csreplica-29fddb35-f56e-4e3c-8f4c-e

d3bd0e4a083.html "。

警告: Test-CsReplica に失敗しました。

警告: 詳細な結果は次のページでご覧いただけます。

"C: \\ \\ \\ AppData \\ ローカル \\ Temp \\ 2 \\ テスト-csreplica-29fddb35-f56e-4e3c-8f4c-e

d3bd0e4a083.html "。

Test-CsReplica: コマンドの実行に失敗しました。要求されたレジストリアクセスがありません

禁止.

行: 1 char: 1

\+ Test-CsReplica-Verbose

\+ ~~~~~~~~~~~~~~~~~~~~~~~

\+ カテゴリ情報: InvalidOperation: (:) \[テスト-CsReplica \] 、セキュリティ

エラー

\+ FullyQualifiedErrorId: ProcessingFailed、Microsoft Rtc. .Deploy

予約.TestReplicaCmdlet

PS C: \\ ユーザーの \\ テスト\>

PS C: \\ \\ \> Test-CsUcwaConference-Targetfqdn "LyncTest" をテストする

icrosoft.com "

警告: 指定した完全修飾のレジストラーポート番号の読み取りに失敗しました

ドメイン名 (FQDN)。 既定のレジストラーポート番号を使用します。 エラー

InvalidOperationException: トポロジで一致するクラスターが見つかりませんでした。

自宅

SipSyntheticTransaction-TryRetri の同期を行います。

eveRegistrarPortFromTopology (Int32& registrarPortNumber)

Test-CsUcwaConference: 割り当てられているテストユーザーはありません

\[LyncTest.SelfHost.Corp.Microsoft.com \] 。 テストユーザー構成を確認します。

行: 1 char: 1

\+ Test-CsUcwaConference-TargetFqdn "LyncTest.SelfHost.Corp.Microsoft.com"

\+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

\+ カテゴリ情報: ResourceUnavailable 使用できません: (:) \[テスト-CsUcwaConference\]

、InvalidOperationException

\+ FullyQualifiedErrorId: Notん Testusers、Microsoft Rtc。

TestUcwaConferenceCmdlet

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a>テストに失敗した可能性がある理由

次に **、テスト用のレプリカ** が機能しない場合の一般的な理由を示します。

  - レプリケーターエージェントと集中ログエージェントサービスで、大きな問題が発生する場合があります。

  - 必要なポートが Windows ファイアウォールで開かれていない可能性がある

  - 必要な Active Directory とローカルコンピューターのセキュリティグループが存在しない可能性があります

</div>

</div>

<span> </span>

</div>

</div>

</div>

