---
title: マスター番地の住所ガイドに照らして都市の住所をテストする
description: マスター番地の住所ガイドに照らして、都市の住所をテストします。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing civic addresses against the master street address guide
ms:assetid: dc680de9-2a0f-4fd3-a99e-9bab0bc30ae5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn690132(v=OCS.15)
ms:contentKeyID: 63969657
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 16e0d721b70e3db175b2d23ddee6f59d13a13c4e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439829"
---
# <a name="testing-civic-addresses-against-the-master-street-address-guide-in-lync-server-2013"></a>Lync Server 2013 の主要住所ガイドに照らして、都市の住所をテストする

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
<p>Windows PowerShell のリモートインスタンスを使って実行する場合は、Test-CsRegistration コマンドレットを実行するためのアクセス許可を持つ RBAC の役割をユーザーに割り当てる必要があります。 このコマンドレットを使うことができるすべての RBAC ロールの一覧を表示するには、Windows PowerShell プロンプトから次のコマンドを実行します。</p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsLisCivicAddress &quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a>説明

Test-CsLisCivicAddress コマンドレットを使用して、位置情報サービス (LIS) データベースに追加された場所を確認します。 このコマンドレットを実行するには、E9 のネットワークルーティングプロバイダーに属している主要な住所ガイド (MSAG) で見つかった場所を比較します。 ネットワークルーティングプロバイダーを持っていない場合、またはプロバイダーに接続できない場合、テストは失敗します。

コマンドにオプションのスイッチパラメーター UpdateValidationStatus を追加した場合、テストを渡す各アドレスについて、対応する MSAGValid な database プロパティが True に設定されます。

</div>

<div>

## <a name="running-the-test"></a>テストの実行

Test-CsLisCivicAddress コマンドレットを使用して、個々のアドレスのテストや複数のアドレスのテストを行うことができます。 たとえば、このコマンドは、Redmond、WA にある1つのアドレスをテストします。

    Test-CsLisCivicAddress -HouseNumber 1234 -HouseNumberSuffix "" -PreDirectional "" -StreetName Main -StreetSuffix St -PostDirectional "" -City Redmond -State WA -PostalCode 98052 -Country US -UpdateValidationStatus

このコマンドでは、現在の LIS データベースにあるすべてのアドレスがテストされます。

    Get-CsLisCivicAddress | Test-CsLisCivicAddress -UpdateValidationStatus

詳細については、「 [CsRegistration のテスト](https://technet.microsoft.com/library/Gg412737(v=OCS.15)) 」コマンドレットのヘルプドキュメントを参照してください。

</div>

<div>

## <a name="determining-success-or-failure"></a>成功または失敗を確認する

Test-CsLisCivicAddress は、指定されたアドレスのバックが成功したか失敗したかを報告します。 アドレスが見つからない場合、またはサービスプロバイダに接続できない場合、住所テストは失敗します。

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a>テストに失敗した可能性がある理由

Test-CsLisCivicAddress が失敗する可能性がある一般的な理由を次に示します。

  - LIS サービスプロバイダーが利用できない可能性があります。 Get-CsLisConfiguration コマンドレットを実行して、LIS サービスプロバイダーの URL を取得できます。
    
        Get-CsLisConfiguration 
    
    その URL に ping して、サービスプロバイダが利用可能であることを確認できます。

</div>

</div>

<span> </span>

</div>

</div>

</div>

