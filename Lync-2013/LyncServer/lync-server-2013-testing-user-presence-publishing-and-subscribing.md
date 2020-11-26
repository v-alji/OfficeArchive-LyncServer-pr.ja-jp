---
title: 'Lync Server 2013: ユーザープレゼンスの発行と購読のテスト'
description: 'Lync Server 2013: ユーザープレゼンスの発行と購読をテストしています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing user presence publishing and subscribing
ms:assetid: 27694c71-8e63-4aa4-b49f-fa06ccb81949
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743832(v=OCS.15)
ms:contentKeyID: 63969587
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 90913f270fbd034ca4d2ea7cf3b93c255fc95c66
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439714"
---
# <a name="testing-user-presence-publishing-and-subscribing-in-lync-server-2013"></a>Lync Server 2013 でユーザーのプレゼンスの発行と購読をテストする

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
<p>Windows PowerShell のリモートインスタンスを使って実行する場合は、Test-CsPresence コマンドレットを実行するためのアクセス許可を持つ RBAC の役割をユーザーに割り当てる必要があります。 このコマンドレットを使うことができるすべての RBAC ロールの一覧を表示するには、Windows PowerShell プロンプトから次のコマンドを実行します。</p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsPresence&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a>説明

Test-CsPresence は、テストユーザーのペアが Lync Server にログオンして、プレゼンス情報を交換できるかどうかを判断するために使用されます。 これを行うために、コマンドレットでは、最初に2人のユーザーがシステムに記録されます。 両方のログオンが成功した場合、最初のテストユーザーは、2番目のユーザーからプレゼンス情報を受け取るように要求します。 2番目のユーザーがこの情報を公開すると、Test-CsPresence 情報が最初のユーザーに正常に送信されたことを確認できます。 プレゼンス情報を交換した後、2つのテストユーザーが Lync Server からログオフします。

</div>

<div>

## <a name="running-the-test"></a>テストの実行

Test-CsPresence コマンドレットを実行するには、定義済みのテストアカウントのペア (「Lync Server テストを実行するためのテストアカウントをセットアップする」を参照) を使用するか、Lync Server を有効にしている2人のユーザーのアカウントを使用します。 テストアカウントを使用してこの確認を実行するには、テストする Lync Server プールの FQDN を指定する必要があります。 次に例を示します。

    Test-CsPresence -TargetFqdn "atl-cs-001.litwareinc.com"

実際のユーザーアカウントを使用してこのチェックを実行するには、2つの Windows PowerShell credentials オブジェクト (アカウント名とパスワードを含むオブジェクト) を各アカウントに作成する必要があります。 次に、テストに登録するときに、これらの資格情報オブジェクトと、2つのアカウントの SIP アドレスを含める必要があります。

    $credential1 = Get-Credential "litwareinc\kenmyer"
    $credential2 = Get-Credential "litwareinc\davidlongmire"
    Test-CsPresence -TargetFqdn "atl-cs-001.litwareinc.com" -PublisherSipAddress "sip:kenmyer@litwareinc.com" -PublisherCredential $credential1 -SubscriberSipAddress "sip:davidlongmire@litwareinc.com" -SubscriberCredential $credential2

詳細については、「 [テスト-CsPresence テスト](https://docs.microsoft.com/powershell/module/skype/Test-CsPresence) 」コマンドレットのヘルプドキュメントを参照してください。

</div>

<div>

## <a name="determining-success-or-failure"></a>成功または失敗を確認する

指定したユーザーがプレゼンス情報を交換できる場合は、次のような出力が表示され、Result プロパティは Success とマークされ **ます。**

TargetFqdn: atl-cs-001.litwareinc.com

結果: 成功

待ち時間:00:00: 06.3280315

誤差

診断

2人のユーザーがプレゼンス情報を交換できない場合、結果はエラーとして表示され、エラーと診断のプロパティに追加情報が記録されます。

TargetFqdn: atl-cs-001.litwareinc.com

結果: エラー

待ち時間: 00:00:00

エラー: 404、見つかりません

診断: ErrorCode = 4005、Source = atl-cs-001.litwareinc.com、

理由 = ターゲット URI が SIP で有効になっていないか、

残っ.

DiagnosticHeader の場合

たとえば、前の出力では、2つのユーザーアカウントの少なくとも1つが無効であるためにテストが失敗したことが示されています。アカウントが存在しないか、Lync Server に対して有効になっていません。 次のようなコマンドを実行すると、アカウントが存在するかどうかを確認し、Lync Server で有効になっているかどうかを確認できます。

    "sip:kenmyer@litwareinc.com", "sip:davidlongmire@litwareinc.com" | Get-CsUser | Select-Object SipAddress, Enabled

Test-CsPresence が失敗した場合は、Verbose パラメーターも含めて、テストを再実行することをお勧めします。

    Test-CsPresence -TargetFqdn "atl-cs-001.litwareinc.com" -Verbose

Verbose パラメーターが含まれている場合、Test-CsPresence は、指定されたユーザーが Lync Server にログオンする機能を確認したときに実行された各操作のステップバイステップのアカウントを返します。 次に例を示します。

不明に対する登録要求のヒット

"Register" アクティビティは "0.0345791" 秒で完了しました。

' SelfSubscribeActivity ' アクティビティが開始されました。

' SelfSubscribeActivity ' アクティビティは "0.0041174" 秒で完了しました。

' SubscribePresence ' アクティビティが開始されました。

' SubscribePresence ' アクティビティは "0.0038764" 秒で完了しました。

"PublishPresence" アクティビティが開始されました。

例外の "プレゼンス通知は25秒以内に受信されません。" ワークフローの同期ワークフローの実行についてのワークフローを実行しました。

25秒以内にプレゼンス通知が受信されなかったということは、ネットワークの問題によって情報の交換が妨げられていることを示している可能性があります。

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a>テストに失敗した可能性がある理由

Test-CsPresence が失敗する可能性がある一般的な理由を次に示します。

  - 指定したユーザーアカウントが間違っています。 次のようなコマンドを実行すると、ユーザーアカウントが存在するかどうかを確認できます。
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - ユーザーアカウントは有効ですが、アカウントは現在 Lync Server に対して有効になっていません。 Lync Server でユーザーアカウントが有効になっていることを確認するには、次のようなコマンドを実行します。
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    Enabled プロパティが False に設定されている場合は、ユーザーが現在 Lync Server を有効にしていないことを意味します。

</div>

</div>

<span> </span>

</div>

</div>

</div>

