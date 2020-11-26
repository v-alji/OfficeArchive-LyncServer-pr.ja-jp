---
title: 'Lync Server 2013: モバイルユーザーアクセスのテスト'
description: 'Lync Server 2013: モバイルユーザーアクセスをテストします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test mobile user access
ms:assetid: 81d97420-428b-41b7-91ef-185d572d3456
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn767947(v=OCS.15)
ms:contentKeyID: 63969624
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e99a05e6ef9fe925126026452823e5edcc100ede
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441243"
---
# <a name="test-mobile-user-access-in-lync-server-2013"></a>Lync Server 2013 でのモバイルユーザーアクセスのテスト

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2014-06-07_


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>確認のスケジュール</p></td>
<td><p>毎月</p></td>
</tr>
<tr class="even">
<td><p>テストツール</p></td>
<td><p>Windows PowerShell</p></td>
</tr>
<tr class="odd">
<td><p>必要なアクセス許可</p></td>
<td><p>Lync Server 管理シェルを使用してローカルで実行する場合、ユーザーは RTCUniversalServerAdmins セキュリティグループのメンバーである必要があります。</p>
<p>Windows PowerShell のリモートインスタンスを使って実行する場合は、Test-CsMcxConference コマンドレットを実行するためのアクセス許可を持つ RBAC の役割をユーザーに割り当てる必要があります。 このコマンドレットを使うことができるすべての RBAC ロールの一覧を表示するには、Windows PowerShell プロンプトから次のコマンドを実行します。</p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsMcxConference&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a>説明

モバイルデバイスユーザーは、次のような操作を行うことができます。

1.  インスタントメッセージとプレゼンス情報を交換します。

2.  ワイヤレスプロバイダーではなく、内部でボイスメールを保存して取得します。

3.  職場やダイヤルアウト会議などの Lync Server 機能を利用できます。 Test-CsMcxConference コマンドレットを使うと、ユーザーがモバイルデバイスを使って Lync Server 会議に参加して参加できることを簡単に確認することができます。

</div>

<div>

## <a name="running-the-test"></a>テストの実行

このチェックを実行するには、3つの Windows PowerShell credentials オブジェクト (アカウント名とパスワードを含むオブジェクト) を各アカウントに作成する必要があります。 次の例に示すように Test-CsMcxConference を呼び出す場合は、これらの資格情報オブジェクトと、2つのアカウントの SIP アドレスを含める必要があります。

    $organizerCred = Get-Credential "litwareinc\kenmyer"
    $user1Cred = Get-Credential "litwareinc\packerman"
    $user2Cred = Get-Credential "litwareinc\adelaney"
    
    Test-CsMcxConference -TargetFqdn "atl-cs-001.litwareinc.com" -Authentication Negotiate -OrganizerSipAddress "sip:kenmyer@litwareinc.com" -OrganizerCredential $organizerCred -UserSipAddress "sip:pilar@litwareinc.com" -UserCredential $user1Cred -User2SipAddress "sip:adelaney@litwareinc.com" -User2Credential $user2Cred

詳細については、「 [テスト-CsMcxConference](https://docs.microsoft.com/powershell/module/skype/Test-CsMcxConference) コマンドレット」のヘルプトピックを参照してください。

</div>

<div>

## <a name="determining-success-or-failure"></a>成功または失敗を確認する

チェックが成功すると、Test-CsMcxConference は成功のテスト結果を報告します。

ターゲット Fqdn: atl-cs-001.litwareinc.com

ターゲット Uri: http://atl-cs-001.litwareinc.com:443/mcx

結果: 成功

待ち時間: 00:00:00

エラーメッセージ:

診断

チェックインが失敗した場合 Test-CsMcxConference は、失敗のテスト結果を報告します。 通常、このテスト結果には、詳細なエラーメッセージと診断が付随します。 次に例を示します。

ターゲット Fqdn: atl-cs-001.litwareinc.com

ターゲット Uri: https://atl-cs-001.litwareinc.com:443/mcx

結果: エラー

待ち時間: 00:00:00

エラーメッセージ: Web-Ticket サービスの応答が受信されませんでした。

内部例外: HHTP 要求はクライアントで許可されていません

ネゴシエーションスキーム ' Ntlm '。 認証ヘッダーが受信されました

が、サーバーから ' Negotiate ' されました。

内部例外: リモートサーバーからエラーが返されました: (401)

第三者.

診断

内部診断: atl-cs-001.litwareinc.com------------------------

Cache-Control: private

Content-type: text/html;charset = utf-8。

サーバー: Microsoft-IIS/8.5

WWW-Authenticate: Negotiate、NTLM

X-電力: ASP.NET

X-コンテンツタイプ-オプション: nosniff

日付: 水曜日、28年5月 19:22:19 2014 日

Content-length: 6305

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a>テストに失敗した可能性がある理由

Test-CsMcxConference が失敗した場合は、モビリティサービスが実行されていてアクセスできることを確認することから開始する必要があります。 この操作を行うには、web ブラウザーを使用して、Lync Server プールのモビリティサービスの URL にアクセスできることを確認します。 たとえば、次のコマンドは、プール atl-cs-001.litwareinc.com の URL を確認します。

`https://atl-cs-001.litwareinc.com/mcx/mcxservice.svc`

モビリティサービスにアクセスできる場合は、テストユーザーが有効な Lync Server アカウントを持っていることを確認する必要があります。 次のようなコマンドを使用して、アカウント情報を取得できます。

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object Enabled

Enabled プロパティが True と等しくない場合、またはコマンドが失敗した場合は、ユーザーが有効な Lync Server アカウントを持っていないことを意味します。各ユーザーアカウントのモビリティが有効になっていることも確認する必要があります。 そのためには、まず、アカウントに割り当てられているモビリティポリシーを特定します。

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object MobilityPolicy

ポリシー名がわかったら、Get-CsMobilityPolicy コマンドレットを使用して、問題のポリシー (たとえば、RedmondMobilityPolicy) に EnableMobility プロパティが True に設定されていることを確認します。

    Get-CsMobilityPolicy -Identity "RedmondMobilityPolicy"

"認証ヘッダー" というエラーメッセージが表示された場合、Test-CsMcxConference の実行時に、有効なユーザーアカウントを指定していないことを意味する場合は、ユーザー名とパスワードを確認して、もう一度テストしてみてください。 ユーザーアカウントが有効であると確信できる場合は、Get-CsWebServiceConfiguration コマンドレットを使用して、UseWindowsAuth プロパティの値を確認します。 これにより、どの認証方法が組織で有効になっているかがわかります。

モバイルサービスのトラブルシューティングのヒントについては、「ブログの投稿の [トラブルシューティング外部の Lync モバイル接続の問題のトラブルシューティング](https://blogs.technet.com/b/nexthop/archive/2012/02/21/troubleshooting-external-lync-mobility-connectivity-issues-step-by-step.aspx)」を参照してください。

</div>

</div>

<span> </span>

</div>

</div>

</div>

