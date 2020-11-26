---
title: 'Lync Server 2013: 匿名 Web アプリアクセスのテスト'
description: 'Lync Server 2013: 匿名 Web アプリのアクセスをテストします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test anonymous Web App access
ms:assetid: 92f691cd-e05e-4bab-beb5-251d4b837a19
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn767949(v=OCS.15)
ms:contentKeyID: 63969630
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 11c33840912fefcaeef069e14773cfefd0834a8b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441271"
---
# <a name="test-anonymous-web-app-access-in-lync-server-2013"></a>Lync Server 2013 での匿名 Web アプリアクセスのテスト

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
<p>Windows PowerShell のリモートインスタンスを使って実行する場合は、Test-CsWebAppAnonymous コマンドレットを実行するためのアクセス許可を持つ RBAC の役割をユーザーに割り当てる必要があります。 このコマンドレットを使うことができるすべての RBAC ロールの一覧を表示するには、Windows PowerShell プロンプトから次のコマンドを実行します。</p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsWebAppAnonymous&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a>説明

Test-CsWebAppAnonymous コマンドレットは、匿名ユーザーが Lync Web App を使って Lync Server 会議に参加できることを確認します。 コマンドレットを実行すると、Test-CsWebAppAnonymous Web チケットサービスに接続して、匿名ユーザーの web チケットを取得します。 コマンドレットがこのチケットの取得に成功した場合、Test-CsWebAppAnonymous は Lync Server に連絡し、インスタントメッセージ、アプリケーション共有、データコラボレーションのための個別の会議を確立しようとします。

Test-CsWebAppAnonymous は、これらの会議を作成するために使用された Api と接続のみを検証することに注意してください。 このコマンドレットは、実際には会議を作成して実施するわけではありません。

</div>

<div>

## <a name="running-the-test"></a>テストの実行

Test-CsWebAppAnonymous コマンドレットを実行するには、構成済みのテストアカウントのペア、または Lync Server を有効にしている2人のユーザーのアカウントのいずれかを使用します。 テストアカウントを使用してこのチェックを実行するには、テスト対象の Lync サーバープールの完全修飾ドメイン名を指定する必要があります。 次に例を示します。

    Test-CsWebAppAnonymous -TargetFqdn atl-cs-001.litwareinc.com

実際のユーザーアカウントを使用してこのチェックを実行するには、Lync Server 管理シェルの資格情報オブジェクト (アカウント名とパスワードを含むオブジェクト) を各アカウントに作成する必要があります。 次に、CsWebAppAnonymous を呼び出したときに、これらの資格情報オブジェクトと、2つのアカウントの SIP アドレスを含める必要があります。

    $cred1 = Get-Credential "litwareinc\kenmyer"
    
    Test-CsWebApp -TargetFqdn atl-cs-001.litwareinc.com -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $cred1

詳細については、Test-CsWebAppAnonymous コマンドレットのヘルプトピックを参照してください。 Lync Server 2013 で使用する場合は、Test-CsWebAppAnonymous が廃止されることに注意してください。

</div>

<div>

## <a name="determining-success-or-failure"></a>成功または失敗を確認する

Test-CsWebAppAnonymous が匿名ユーザーを会議に参加できる場合、コマンドレットによってテスト結果の成功が返されます。

ターゲット Fqdn:

結果: 成功

待ち時間: 00:00:00

エラーメッセージ:

診断

匿名ユーザーが必要な会議に参加できない場合、テスト結果は [エラー] とマークされます。 通常 Test-CsWebAppAnonymous は、詳細なエラーメッセージと診断にも報告されます。

ターゲット Fqdn: atl-cs-001.litwareinc.com

結果: エラー

待ち時間:00:00: 05.9746266

エラーメッセージ: Web-Ticket サービスの応答が受信されませんでした

診断: HTTP 要求はクライアントで承認されていません

認証スキーム ' Ntlm '。 認証

サーバーから受信したヘッダーは、"Negotiate、NTLM" でした。

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a>テストに失敗した可能性がある理由

通常、Test-CsWebAppAnonymous のエラーはユーザー認証エラーの発生時に発生します。コマンドレットが、Lync Server に接続する匿名ユーザーの機能を確認している場合でも、有効なユーザーアカウントを使用してテストを実行する必要があります。 Test-CsWebAppAnonymous に失敗した場合は、指定したユーザーが有効な Lync Server ユーザーアカウントを持っていることを確認する必要があります。 Lync Server アカウント情報を取得するには、次のようなコマンドを使用します。

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object Enabled

Enabled プロパティが True と等しくない場合、またはコマンドが失敗した場合は、ユーザーが有効な Lync Server アカウントを持っていないことを意味します。

また、コマンドレットの実行時に入力したパスワードが有効なパスワードであることも確認する必要があります。

Office Web Apps サーバーの構成の問題も Test-CsWebAppAnonymous の失敗の原因となることがあります。次のような診断が表示されることがよくあります。

HTTP 要求は、クライアント認証スキーム ' Ntlm ' で承認されていません。 サーバーから受信した認証ヘッダーは、"Negotiate、NTLM" となりました。

Office Web Apps サーバーの問題の診断と解決の詳細については、「Office Web Apps のブログを参照する」を参照してください。 [サーバー 2013-コンピューターは、常に異常と報告され](http://www.wictorwilen.se/office-web-apps-server-2013---machines-are-always-reported-as-unhealthy)ます。

</div>

</div>

<span> </span>

</div>

</div>

</div>

