---
title: 'Lync Server 2013: Lync Phone Edition のログインをテストする'
description: 'Lync Server 2013: Lync Phone Edition のログインをテストしています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing Lync Phone Edition login
ms:assetid: 1ccde6bf-9a2d-4fcf-b81f-1bc9fee2cfbb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn690128(v=OCS.15)
ms:contentKeyID: 63969583
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d21d65676c4f5e0f867c7d9556cdea50419be69b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398937"
---
# <a name="testing-lync-phone-edition-login-in-lync-server-2013"></a>Lync Server 2013 での Lync Phone Edition のログインのテスト

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
<p>Windows PowerShell のリモートインスタンスを使って実行する場合は、Test-CsPhoneBootstrap コマンドレットを実行するためのアクセス許可を持つ RBAC の役割をユーザーに割り当てる必要があります。 このコマンドレットを使うことができるすべての RBAC ロールの一覧を表示するには、Windows PowerShell プロンプトから次のコマンドを実行します。</p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsPhoneBootstrap&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a>説明

Test-CsPhoneBootstrap コマンドレットを使用すると、管理者は、ユーザーが割り当てられた電話番号と PIN を使って、Lync 2013 Phone Edition 対応のデバイスからシステムにログオンできることを確認できます。 (実際にテストを実行するために必要なデバイスはありません)。

Test-CsPhoneBootstrap のチェックを行うために、テスト対象のユーザーアカウントをホストするレジストラープールは、DHCP を使って検出できる必要があります。 この方法でレジストラーが検出可能かどうかを判断するには、コマンドレット Get-CsRegistrarConfiguration を使用して、EnableDHCPServer プロパティの値を確認します。 このプロパティが False に設定されている場合は、Set-CsRegistrarConfiguration を使用してプロパティ値を True に設定し、DHCP を使ってレジストラーを検出できるようにする必要があります。 また、エンタープライズ DHCP サーバーを使用して、Lync Server 固有のオプションを構成することでも実行できます。

</div>

<div>

## <a name="running-the-test"></a>テストの実行

Test-CsPhoneBootstrap コマンドレットを実行するには、少なくとも Lync Server の有効なユーザーの電話番号とクライアントの暗証番号 (PIN) を指定する必要があります。 たとえば、次のコマンドは、電話番号12065551219と PIN 0712 を持っているユーザーのログオン機能をテストします。

    Test-CsPhoneBootstrap -PhoneOrExt "+12065551219" -Pin "0712"

さらに包括的なチェックを行うには、ユーザーの SIP アドレスを含めることもできます。 その場合、テストが成功するには、電話番号、クライアント PIN、および SIP アドレスがすべて有効である必要があります。

    Test-CsPhoneBootstrap -PhoneOrExt "+12065551219" -Pin "0712" -UserSipAddress "sip:kenmyer@litwareinc.com"

詳細については、「 [テスト-CsPhoneBootstrap](https://docs.microsoft.com/powershell/module/skype/Test-CsPhoneBootstrap) コマンドレット」のヘルプドキュメントを参照してください。

</div>

<div>

## <a name="determining-success-or-failure"></a>成功または失敗を確認する

指定したユーザーが Lync Server に接続できた場合は、次のような出力が表示され、Result プロパティは Success とマークされ **ます。**

TargetUri : https://atl-cs-001.litwareinc.com:443/CertProv/

Certservices .svc

TargetFqdn: atl-cs-001.litwareinc.com

結果: 成功

待ち時間:00:00: 06.3981276

誤差

診断

指定したユーザーが接続できなかった場合は、結果がエラーとして表示され、エラーと診断のプロパティに追加情報が記録されます。

TargetFqdn: atl-cs-001.litwareinc.com

結果: エラー

待ち時間:00:00: 04.1993845

エラー: エラー-Web-Ticket サービスの応答が受信されませんでした。

診断

前回の出力では、Web チケットサービスが応答しなかったため、テストが失敗したことが示されます。 これは、サービス自体で問題が発生したか、または SIP アドレス、電話番号、またはクライアント PIN がテスト用の CsPhoneBootstrap に渡されたことが原因である可能性があります。 次のようなコマンドを使用して、ユーザーの SIP アドレスと電話番号を確認できます。

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object SipAddress, LineUri

また、次のようにコマンドを使用して、ユーザーが有効な PIN を持っていることを確認できます。

    Get-CsClientPinInfo -Identity "sip:kenmyer@litwareinc.com" 

Test-CsPhoneBootstrap が失敗した場合は、Verbose パラメーターも含めて、テストを再実行することをお勧めします。

    Test-CsPhoneBootstrap -PhoneOrExt "+12065551219" -Pin "0712" -Verbose

Verbose パラメーターが含まれている場合、Test-CsPhoneBootstrap は、指定されたユーザーが Lync Server にログオンする機能を確認したときに実行された各操作のステップバイステップのアカウントを返します。 たとえば、次の例は、正常に行われなかったログオンの出力を示しています。このセッションでは、不正な PIN が含まれています。

内線番号での PIN 認証の使用 \\ : 12065551219 ピン: 0712

Web チケットを取得できませんでした

調べ

\- Web サービスの url が有効であり、web サービスが機能している

\- 認証に PhoneNo PIN を使用している場合は、 \\ ユーザーの uri と一致することを確認します。

\- NTLM Kerberos 認証を使用している場合は \\ 、有効な資格情報を指定していることを確認します。

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a>テストに失敗した可能性がある理由

Test-CsPhoneBootstrap が失敗する可能性がある一般的な理由を次に示します。

  - 有効でない SIP アドレスが指定された可能性があります。 次のようなコマンドを使用して、SIP アドレスが正しいことを確認できます。
    
        Get-CsUser -Identity "sip:kenmyer@litwareinc.com"

  - 無効な PIN を指定した可能性があります。 ユーザーの PIN 番号を取得することはできませんが、次のようなコマンドを使用して、ユーザーの PIN 番号が少なくなっていることを確認できます。
    
        Get-CsClientPinInfo -Identity "sip:kenmyer@litwareinc.com"

  - 無効な電話番号を指定した可能性があります。 次のようなコマンドを使用して、ユーザーの電話を確認できます。
    
        Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object LineUri

  - レジストラープールは DHCP 対応ではありません。 レジストラープールが DHCP に対して有効になっているかどうかを確認するには、Get-CsRegistrarConfiguration コマンドレットを実行して、EnableDHCPServer プロパティの値を確認します。 次に例を示します。
    
        Get-CsRegistrarConfiguration -Identity "global"

</div>

</div>

<span> </span>

</div>

</div>

</div>

