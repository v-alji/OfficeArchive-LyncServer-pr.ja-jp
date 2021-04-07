---
title: 'Lync Server 2013: Standard Edition サーバーの DNS 要件'
description: 'Lync Server 2013: Standard Edition サーバーの DNS 要件。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for a Standard Edition server
ms:assetid: 5d1daf54-6e60-4ce0-9254-7d57a0835fa4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204936(v=OCS.15)
ms:contentKeyID: 48184259
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8ea0c7219563d62a9d99bd85655b3d3fcb0c551f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399752"
---
# <a name="dns-requirements-for-a-standard-edition-server-in-lync-server-2013"></a>Lync Server 2013 の Standard Edition サーバーの DNS 要件

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**トピック最終更新日:** 2013-02-22_

ここでは、Standard Edition サーバーの展開に必要なドメイン ネーム システム (DNS) レコードについて説明します。

<div>

## <a name="dns-records-for-standard-edition-servers"></a>Standard Edition Servers の DNS レコード

次の表は、Lync Server 2013 Standard Edition サーバー展開の DNS 要件を示しています。


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
<td><p>Standard Edition サーバー</p></td>
<td><p>サーバーの完全修飾ドメイン名 (FQDN) を IP アドレスに解決する内部 A レコード。</p></td>
</tr>
<tr class="even">
<td><p>クライアントの自動サインイン</p></td>
<td><p>サポートされている SIP ドメインごとに、_sipinternaltls._tcp の SRV レコード。 &lt;サインインのクライアント要求を認証およびリダイレクトする Standard Edition サーバーの FQDN にマップされるポート &gt; 5061 を超えるドメイン。 詳細については <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">、Lync Server 2013</a>での自動クライアント サインインの DNS 要件を参照してください。</p></td>
</tr>
<tr class="odd">
<td><p>ユニファイド コミュニケーション (UC) デバイスによるデバイス更新 Web サービス検出</p></td>
<td><p>ucupdates-r2 という名前の内部 A レコード。 &lt;Device &gt; Update Web サービスをホストする Standard Edition サーバーの IP アドレスに解決される SIP ドメイン。 UC デバイスがオンになっているが、ユーザーがデバイスにログインしたことがない場合、A レコードにより、デバイスは Device Update Web サービスをホストしているサーバーを検出して更新プログラムを取得できます。 それ以外の場合、ユーザーが初めてログインすると、デバイスはインバンド プロビジョニングを行ってサーバー情報を取得します。 詳細については、操作に関するドキュメントの <a href="lync-server-2013-device-update-web-service.md">「Lync Server 2013</a> のデバイス更新 Web サービス」を参照してください。</p></td>
</tr>
<tr class="even">
<td><p>HTTP トラフィックをサポートするリバース プロキシ</p></td>
<td><p>外部 Web ファームの FQDN をリバース プロキシの外部 IP アドレスに解決する外部 A レコード。 クライアントと UC デバイスは、このレコードを使用してリバース プロキシに接続します。 詳細については、計画に <a href="lync-server-2013-determine-dns-requirements.md">関するドキュメントの「Lync Server 2013</a> の DNS 要件を決定する」を参照してください。</p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a>関連項目


[Lync Server 2013 でのクライアントの自動サインインの DNS 要件](lync-server-2013-dns-requirements-for-automatic-client-sign-in.md)  
[Lync Server 2013 の DNS の要件を確認する](lync-server-2013-determine-dns-requirements.md)  


[Lync Server 2013 のデバイス更新 Web サービス](lync-server-2013-device-update-web-service.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

