---
title: 'Lync Server 2013: フェデレーションドメインに接続する機能をテストする'
description: 'Lync Server 2013: フェデレーションドメインに接続する機能をテストしています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing ability to connect to a federated domain
ms:assetid: d8ccfade-ef54-47a4-9f87-36213a635ce5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743840(v=OCS.15)
ms:contentKeyID: 63969653
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bf1f5bdef66d34b9ca2e39797df0b4ad32d9afde
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441138"
---
# <a name="testing-ability-to-connect-to-a-federated-domain-from-lync-server-2013"></a>Lync Server 2013 からフェデレーションドメインに接続するためのテスト機能

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
<p>Windows PowerShell のリモートインスタンスを使って実行する場合は、Test-CsFederatedPartner コマンドレットを実行するためのアクセス許可を持つ RBAC の役割をユーザーに割り当てる必要があります。 このコマンドレットを使うことができるすべての RBAC ロールの一覧を表示するには、Windows PowerShell プロンプトから次のコマンドを実行します。</p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsFederatedPartner&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a>説明

Test-CsFederatedPartner は、フェデレーションパートナーのドメインに接続できるかどうかを確認します。 ドメインへの接続を確認するには、そのドメインが許可された (フェデレーションされた) ドメインのコレクションに表示されている必要があります。 次のコマンドを使用して、許可ドメインの一覧にあるドメインの一覧を取得できます。

    Get-CsAllowedDomain

詳細については、「 [CsFederatedPartner](https://docs.microsoft.com/powershell/module/skype/Test-CsFederatedPartner) コマンドレットのヘルプドキュメント」を参照してください。

</div>

<div>

## <a name="running-the-test"></a>テストの実行

Test-FederatedPartner コマンドレットには、エッジサーバーの FQDN とフェデレーションパートナーの FQDN という2つの情報が必要です。 たとえば、次のコマンドは、ドメイン contoso.com に接続する機能をテストします。

    Test-CsFederatedPartner -TargetFqdn "atl-edge-001.litwareinc.com" -Domain "contoso.com"

このコマンドを使用すると、許可ドメインリストに現在あるすべてのドメインへの接続をテストすることができます。

    Get-CsAllowedDomain | ForEach-Object {Test-CsFederatedPartner -TargetFqdn "atl-edge-001.litwareinc.com" -Domain $_.Identity}

詳細については、「 [CsFederatedPartner](https://docs.microsoft.com/powershell/module/skype/Test-CsFederatedPartner) コマンドレットのヘルプドキュメント」を参照してください。

</div>

<div>

## <a name="determining-success-or-failure"></a>成功または失敗を確認する

指定したドメインに接続できる場合は、次のような結果として、Success とマークされた Result プロパティが出力され **ます。**

TargetFqdn: atl-cs-001.litwareinc.com

結果: 成功

待ち時間: 00:00:00

誤差

診断

指定したドメインに接続できない場合、結果はエラーとして表示され、エラーと診断のプロパティに追加情報が記録されます。

TargetFqdn: atl-cs-001.litwareinc.com

結果: エラー

待ち時間: 00:00:00

エラー: 504、サーバーのタイムアウト

診断: ErrorCode = 2、Source = litwareinc、Reason = を参照してください。

応答コードと理由の語句。

DiagnosticHeader の場合

たとえば、前回の出力では、サーバーのタイムアウトエラーのためにテストが失敗したことが示されます。 これは通常、ネットワーク接続の問題、またはエッジサーバーへの接続の問題を示します。

Test-CsFederatedPartner が失敗した場合は、Verbose パラメーターも含めて、テストを再実行することをお勧めします。

    Test-CsFederatedPartner -TargetFqdn "atl-edge-001.litwareinc.com" -Domain "contoso.com" -Verbose

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a>テストに失敗した可能性がある理由

Test-CsFederatedPartner が失敗する可能性がある一般的な理由を次に示します。

  - エッジサーバーが利用できない可能性があります。 このコマンドを使用して、エッジサーバーの Fqdn を使用できます。
    
        Get-CsService -EdgeServer | Select-Object PoolFqdn
    
    次に、各エッジサーバーに対して ping を実行して、ネットワーク経由でアクセスできることを確認できます。 次に例を示します。
    
        ping atl-edge-001.litwareinc.com

  - 指定したドメインが [許可したドメイン] リストに表示されない場合があります。 許可ドメインリストに追加されたドメインを確認するには、次のコマンドを使用します。
    
        Get-CsAllowedDomain
    
    ユーザーが通信をブロックされたドメインの一覧を表示するには、次のコマンドを使用します。
    
        Get-CsBlockedDomain

</div>

</div>

<span> </span>

</div>

</div>

</div>

