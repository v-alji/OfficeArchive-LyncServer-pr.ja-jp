---
title: 'Lync Server 2013: LIS サーバー構成のテスト'
description: 'Lync Server 2013: LIS サーバーの構成をテストしています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing LIS server configuration
ms:assetid: 6b06e7ab-522f-41a2-878b-e89cd4e3c6da
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn690129(v=OCS.15)
ms:contentKeyID: 63969614
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ba4d16d2ce48e3e5bb89e863f02902d05ce77bd7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398961"
---
# <a name="testing-lis-server-configuration-in-lync-server-2013"></a>Lync Server 2013 での LIS サーバーの構成のテスト

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
<p>Windows PowerShell のリモートインスタンスを使って実行する場合は、Test-CsLisConfiguration コマンドレットを実行するためのアクセス許可を持つ RBAC の役割をユーザーに割り当てる必要があります。 このコマンドレットを使うことができるすべての RBAC ロールの一覧を表示するには、Windows PowerShell プロンプトから次のコマンドを実行します。</p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsLisConfiguration&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a>説明

Test-CsLisConfiguration コマンドレットによって、LIS web サービスに連絡できるかどうかが確認されます。 Web サービスに連絡できる場合は、特定の場所が見つかるかどうかに関係なく、テストが成功したと見なされます。

</div>

<div>

## <a name="running-the-test"></a>テストの実行

Test-CsLisConfguration コマンドレットを実行するには、事前に定義されたテストアカウント (「Lync Server のテストを実行するためのテストアカウントをセットアップする」を参照) を使用するか、Lync Server を有効にしているユーザーのアカウントを使用します。 テストアカウントを使用してこのチェックを実行するには、テスト対象の Lync Server プールの FQDN を指定する必要があります。 次に例を示します。

    Test-CsLisConfiguration -TargetFqdn "atl-cs-001.litwareinc.com"

実際のユーザーアカウントを使用してこのチェックを実行するには、最初に、アカウント名とパスワードを含む Windows PowerShell 資格情報オブジェクトを作成する必要があります。 次に、CsLisConfiguration を呼び出したときに、アカウントに割り当てられている資格情報オブジェクトと SIP アドレスを指定する必要があります。

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsLisConfiguration -TargetFqdn "atl-cs-001.litwareinc.com"-UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

詳細については、「 [CsLisConfiguration](https://docs.microsoft.com/powershell/module/skype/Test-CsLisConfiguration) コマンドレットのヘルプドキュメント」を参照してください。

</div>

<div>

## <a name="determining-success-or-failure"></a>成功または失敗を確認する

LIS が適切に構成されている場合は、次のような結果が返され、Result プロパティは Success とマークされ **ます。**

TargetUri : https://atl-cs-001.litwareinc.com:443/locationinformation/

liservice .svc

TargetFqdn: atl-cs-001.litwareinc.com

結果: 成功

待ち時間:00:00: 06.1616913

誤差

診断

指定したユーザーがログオンまたはログオフできない場合は、結果がエラーとして表示され、エラーと診断のプロパティに追加情報が記録されます。

TargetUri :

TargetFqdn: atl-cs-001.litwareinc.com

結果: エラー

待ち時間: 00:00:00

エラー: 11004、要求された名前は有効ですが、要求されたデータがありません

種類が見つかりました

診断

Test-CsLisConfiguration: トポロジで一致するクラスターが見つかりませんでした。

たとえば、前の出力には "一致するクラスターがトポロジで見つかりませんでした" というメモが含まれています。 これは通常、エッジサーバーに問題があることを示します。これは、サービスプロバイダに接続してアドレスを検証するためにエッジサーバーを使用している LIS。

Test-CsLisConfiguration が失敗した場合は、Verbose パラメーターも含めて、テストを再実行することをお勧めします。

    Test-CsLisConfiguration -TargetFqdn "atl-cs-001.litwareinc.com" -Verbose

Verbose パラメーターが含まれている場合、Test-CsLisConfiguration は、指定されたユーザーが Lync Server にログオンする機能を確認したときに実行された各操作のステップバイステップのアカウントを返します。 次に例を示します。

位置情報サービスを呼び出しています。

サービスパス = https://atl-cs-001.litwareinc.com:443/locationinformation/liservice.svc

Subnet =

BssId = 5

Chいい Sid =

PortId =

PortIdSubType = 未定義の型

Mac

"位置情報の Web サービス要求" の例外は、応答コード Item400 で失敗しました。 ' STLisConfigurationWorkflow の実行中に発生したワークフローのことです。.

前の出力をよく確認すると、位置情報サービスを呼び出した後にコマンドレットが失敗したことがわかります。 この呼び出しで使用されたパラメーターの1つは、次のようになりました。

BssId = 5

これは、基本サービスセット識別子 (BssID) の有効な値ではありません。 代わりに、BssID は次のようになります。

12-34-56-78-90-ab

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a>テストに失敗した可能性がある理由

Test-CsLisConfiguration が失敗する可能性がある一般的な理由を次に示します。

  - 指定されたパラメーター値が正しくありません。 上の例で示したように、オプションのパラメーターは正しく構成されている必要があります。また、テストは失敗します。 省略可能なパラメーターを指定せずにコマンドを再実行し、それが成功するかどうかを確認します。

</div>

</div>

<span> </span>

</div>

</div>

</div>

