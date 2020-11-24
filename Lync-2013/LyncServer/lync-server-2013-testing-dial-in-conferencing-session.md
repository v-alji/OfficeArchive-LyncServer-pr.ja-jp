---
title: 'Lync Server 2013: ダイヤルイン会議セッションのテスト'
description: 'Lync Server 2013: ダイヤルイン会議セッションをテストしています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing dial-in conferencing session
ms:assetid: 6c505be5-5af7-450c-b3ca-10d9122bee5c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743834(v=OCS.15)
ms:contentKeyID: 63969613
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4d0c51b16df674dbf8bf7f0a2c6c4c93c2606d95
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398973"
---
# <a name="testing-dial-in-conferencing-session-in-lync-server-2013"></a>Lync Server 2013 でのダイヤルイン会議セッションのテスト

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2014-06-05_


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
<p>Windows PowerShell のリモートインスタンスを使って実行する場合は、Test-CsDialInConferencing コマンドレットを実行するためのアクセス許可を持つ RBAC の役割をユーザーに割り当てる必要があります。 このコマンドレットを使うことができるすべての RBAC ロールの一覧を表示するには、Windows PowerShell プロンプトから次のコマンドを実行します。</p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsDialInConferencing&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a>説明

Test-CsDialInConferencing コマンドレットは、ユーザーがダイヤルイン会議に参加できるかどうかを確認します。 Test-CsDialInConferencing は、テストユーザーをシステムにログインしようとします。 ログオンが成功すると、コマンドレットはユーザーの資格情報とアクセス許可を使って、利用可能なダイヤルイン会議アクセス番号をすべて試します。 各ダイヤルイン試行の成功または失敗が通知されます。次に、テストユーザーは、Lync Server からログオフされます。テスト-Csdial Inコンファレンスは、適切な接続を確立できることのみを確認します。 このコマンドレットは、実際には電話をかけたり、他のユーザーが参加できるダイヤルイン会議を作成したりすることはありません。

</div>

<div>

## <a name="running-the-test"></a>テストの実行

Test-CsDialInConferencing コマンドレットを実行するには、事前に定義されたテストアカウント (「Lync Server のテストを実行するためのテストアカウントをセットアップする」を参照) を使用するか、Lync Server を有効にしているユーザーのアカウントを使用します。 テストアカウントを使用してこのチェックを実行するには、テスト対象の Lync Server プールの FQDN を指定する必要があります。 次に例を示します。

    Test-CsDialInConferencing -TargetFqdn "atl-cs-001.litwareinc.com" 

実際のユーザーアカウントを使用してこのチェックを実行するには、アカウント名とパスワードを含む Windows PowerShell 資格情報オブジェクトを作成する必要があります。 次に、その資格情報オブジェクトと、通話テスト用のアカウント SIP アドレスを指定する必要があります。

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsDialInConferencing -TargetFqdn atl-cs-001.litwareinc.com" -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

詳細については、「 [テスト](https://docs.microsoft.com/powershell/module/skype/Test-CsDialInConferencing) 用のヘルプ」コマンドレットのヘルプドキュメントを参照してください。

</div>

<div>

## <a name="determining-success-or-failure"></a>成功または失敗を確認する

指定したユーザーが Lync サーバーにログオンして、利用可能なダイヤルイン会議アクセス番号のいずれかを使用して接続すると、次のような出力が表示され、Result プロパティは Success とマークされ **ます。**

TargetFqdn: atl-cs-001.litwareinc.com

結果: 成功

待ち時間:00:00: 06.8630376

誤差

診断

指定したユーザーがこの接続を確立できない場合、結果はエラーとして表示され、エラーと診断のプロパティに追加情報が記録されます。

TargetFqdn: atl-cs-001.litwareinc.com

結果: エラー

待ち時間: 00:00:00

エラー: ログオンは拒否されました。 適切な資格情報があることを確認する

使用されていて、アカウントが有効になっています。

内部例外: NegotiateSecurityAssociation に失敗しました。エラー:-

2146893044

診断

前回の出力では、テストユーザーが Lync Server 自体へのアクセスを拒否されたことを示しています。 これは通常、Test-CsDialInConferencing に渡されたユーザー資格情報が無効であったことを意味します。 さらに、Windows PowerShell 資格情報オブジェクトを再作成する必要があります。 ユーザーアカウントのパスワードを取得することはできますが、次のようなコマンドを使用して SIP アドレスを確認できます。

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object SipAddress

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a>テストに失敗した可能性がある理由

Test-CsDialInConferencing が失敗する可能性がある一般的な理由を次に示します。

  - 無効なユーザーアカウントが指定されました。 次のようなコマンドを実行すると、ユーザーアカウントが存在するかどうかを確認できます。
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - ユーザーアカウントは有効ですが、アカウントは現在 Lync Server に対して有効になっていません。 Lync Server でユーザーアカウントが有効になっていることを確認するには、次のようなコマンドを実行します。
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    Enabled プロパティが False に設定されている場合は、ユーザーが現在 Lync Server を有効にしていないことを意味します。

  - ダイヤルイン会議のアクセス番号が間違っている可能性があります。 次のコマンドを使用して、現在構成されているダイヤルイン会議アクセス番号のリストを返すことができます。
    
        Get-CsDialConferencingAccessNumber

</div>

</div>

<span> </span>

</div>

</div>

</div>

