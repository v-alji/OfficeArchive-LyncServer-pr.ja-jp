---
title: 'Lync Server 2013: フロント エンド プールの DNS 要件'
description: 'Lync Server 2013: フロント エンド プールの DNS 要件。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for Front End pools
ms:assetid: ba28919c-fbbe-4c54-8bf9-2b0cd3fa39c7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412910(v=OCS.15)
ms:contentKeyID: 48185228
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8c0369e82bd8ed2ea63e2156728b41f9942b0148
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429071"
---
# <a name="dns-requirements-for-front-end-pools-in-lync-server-2013"></a>Lync Server 2013 のフロント エンド プールの DNS 要件

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**トピック最終更新日:** 2012-11-07_

このセクションでは、フロント エンド プールの展開に必要なドメイン ネーム システム (DNS) レコードについて説明します。

<div>

## <a name="dns-records-for-front-end-pools"></a>フロント エンド プールの DNS レコード

次の表は、Lync Server 2013 フロント エンド プール展開の DNS 要件を示しています。

### <a name="dns-requirements-for-a-front-end-pool"></a>フロント エンド プールの DNS 要件

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>展開シナリオ</th>
<th>DNS 要件</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>複数のフロント エンド サーバーとハードウェア ロード バランサーを備えたフロント エンド プール (DNS ロード バランシングもそのプールに展開されるかどうか)</p></td>
<td><p>DNS ロード バランシングとハードウェア ロード バランサーの両方を使用する場合は、レコードをホスト (A) する必要があります。 DNS ロード バランシングのためにフロント エンド プールの完全修飾ドメイン名 (FQDN) を解決する内部 A レコードを作成します。 ロード バランサーの仮想 IP (VIP) アドレスに対する内部 Web サービスの内部ホスト (A) レコードを作成します。 トポロジ ビルダーで定義されている内部 Web サービス名を使用する必要があります。</p>
<p>たとえば、DNS ロード バランシングとハードウェア ロード バランシングの両方を使用する場合、DNS ロード バランシング用のプール内の各フロント エンド サーバーの A レコードと、ハードウェア ロード バランサーの仮想 IP をポイントする内部 Web サービスの A レコードがあります。</p>
<ul>
<li><p>DNS ロード バランシング: Pool01.contoso.net プール 10.10.10.5 の IP アドレス</p>
<div>

> [!WARNING]  
> 各フロント エンド サーバーには、次の異なる A レコードも含されます。


</div>
<ol>
<li><p>FE01.contoso.net 10.10.10.1</p></li>
<li><p>FE02.contoso.net 10.10.10.2</p></li>
<li><p>FE03.contoso.net 10.10.10.3</p></li>
<li><p>FE04.contoso.net 10.10.10.4</p></li>
</ol></li>
<li><p>ハードウェア ロード バランシング: WebInternal.contoso.net HLB VIP 192.168.10.5 の IP アドレス</p></li>
</ul>
<p>HTTP/HTTPS トラフィックを除くすべてのトラフィックは、そのレコード Pool01.contoso.net します。 HTTP/HTTPS トラフィックでは、定義された内部 Web サービス アドレス 192.168.10.5 が使用されます。</p></td>
</tr>
<tr class="even">
<td><p>DNS ロード バランシングが展開されたフロント エンド プール</p></td>
<td><p>プールの FQDN をプール内の各サーバーの IP アドレスに解決する内部 A レコードのセット。 プール内のサーバーごとに 1 つの A レコードが必要です。</p></td>
</tr>
<tr class="odd">
<td><p>DNS ロード バランシングが展開されたフロント エンド プール</p></td>
<td><p>プール内の各サーバーの FQDN をそのサーバーの IP アドレスに解決する内部 A レコードのセット。 詳細については、計画に関するドキュメントの <a href="lync-server-2013-dns-load-balancing.md">「Lync Server 2013</a> の DNS ロード バランシング」を参照してください。</p></td>
</tr>
<tr class="even">
<td><p>1 つのフロント エンド サーバーと専用のバック エンド データベースを備え、ロード バランサーがないフロント エンド プール</p></td>
<td><p>フロント エンド プールの FQDN を単一の Enterprise Edition フロント エンド サーバーの IP アドレスに解決する内部 A レコード。</p></td>
</tr>
<tr class="odd">
<td><p>クライアントの自動サインイン</p></td>
<td><p>サポートされている SIP ドメインごとに、_sipinternaltls._tcp の SRV レコード。 &lt;サインイン要求を認証してリダイレクトするフロント エンド プールの FQDN にマップされるポート &gt; 5061 を超えるドメイン。 詳細については <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">、Lync Server 2013</a>での自動クライアント サインインの DNS 要件を参照してください。</p></td>
</tr>
<tr class="even">
<td><p>ユニファイド コミュニケーション (UC) デバイスによるデバイス更新 Web サービス検出</p></td>
<td><p>ucupdates-r2 という名前の内部 A レコード。 &lt;Device Update Web サービスをホストするフロント エンド プールの IP アドレスに解決 &gt; される SIP ドメイン。 UC デバイスがオンになっているが、ユーザーがデバイスにログインしたことがない場合、A レコードにより、デバイスは Device Update Web サービスをホストするフロント エンド プールを検出し、更新プログラムを取得できます。 それ以外の場合、ユーザーが初めてログインすると、デバイスはインバンド プロビジョニングを行ってこの情報を取得します。</p>
<div>

> [!IMPORTANT]  
> Lync Server 2010 で Device Update Web サービスを展開している場合は、ucupdates という名前の内部 A レコードを既に作成しています。 &lt;SIP ドメイン &gt; 。 Communications Server 2007 R2 Microsoft Office、ucupdates-r2 という名前の追加の DNS A レコードを作成する必要があります。 &lt;SIP ドメイン &gt; 。


</div></td>
</tr>
<tr class="odd">
<td><p>HTTP トラフィックをサポートするリバース プロキシ</p></td>
<td><p>外部 Web ファームの FQDN をリバース プロキシの外部 IP アドレスに解決する外部 A レコード。 クライアントと UC デバイスは、このレコードを使用してリバース プロキシに接続します。 詳細については、計画に <a href="lync-server-2013-determine-dns-requirements.md">関するドキュメントの「Lync Server 2013</a> の DNS 要件を決定する」を参照してください。</p></td>
</tr>
</tbody>
</table>


次の表は、内部 Web ファームの FQDN に必要な DNS レコードの例を示しています。

### <a name="example-dns-records-for-internal-web-farm-fqdn"></a>内部 Web ファーム FQDN の DNS レコードの例

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>内部 Web ファームの FQDN</th>
<th>プールの FQDN</th>
<th>DNS A レコード</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>webcon.contoso.com</p></td>
<td><p>ee-pool.contoso.com</p></td>
<td><p>フロントエンド サーバーによって使用 ee-pool.contoso.com ロード バランサーの VIP アドレスに解決される、サーバーの DNS A レコード。</p>
<p>フロントエンド サーバーによって webcon.contoso.com ロード バランサーの VIP アドレスに解決される、サーバーの DNS A レコード。</p></td>
</tr>
<tr class="even">
<td><p>ee-pool.contoso.com</p></td>
<td><p>ee-pool.contoso.com</p></td>
<td><p>フロント エンド プール ee-pool.contoso.com Enterprise Edition フロント エンド サーバーによって使用されるロード バランサーの仮想 IP (VIP) アドレスに解決する、ee-pool.contoso.com 用の DNS レコード。</p>
<p>このプールで DNS ロード バランシングを使用している場合は、フロント エンド プールと内部 Web ファームに同じ FQDN を設定できないことに注意してください。</p></td>
</tr>
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</div>

