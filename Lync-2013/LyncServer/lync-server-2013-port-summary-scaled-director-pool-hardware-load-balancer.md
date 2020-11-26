---
title: 'Lync Server 2013: ポートの概要 - 拡張ディレクター プール、ハードウェア ロード バランサー'
description: 'Lync Server 2013: ポート概要-スケーリングされたディレクタープール、ハードウェアロードバランサー。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Scaled Director pool, hardware load balancer
ms:assetid: 6ae2f4ac-5b64-4e45-8253-133308f5812d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204983(v=OCS.15)
ms:contentKeyID: 48184434
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 10bfb3a3ad3a38b6cb0e46414bf22deecc71d7b5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442797"
---
# <a name="port-summary---scaled-director-pool-hardware-load-balancer-in-lync-server-2013"></a>ポートの概要 - Lync Server 2013 の拡張ディレクター プール、ハードウェア ロード バランサー

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-10-21_

ディレクタープールのファイアウォールポート要件は、エッジサーバーまたはリバースプロキシの内部インターフェイスからディレクターとの通信を確立するために使用されるポートで構成されています。 Microsoft Lync Server 2013 は、既定では、ポート HTTP/TCP 8080 と HTTPS/TCP 4443 が、リバースプロキシからディレクターまで、およびフロントエンドプールとフロントエンドサーバーによって開かれることを想定しています。 さらに、エッジサーバーの内部インターフェイスからディレクターへのセッション開始プロトコル (SIP) 通信と、フロントエンドプールとフロントエンドサーバーへの通信が必要です。 SIP プロトコルは、SIP/MTLS/TCP 5061 をエッジサーバーからフロントエンドプールとフロントエンドサーバーに使用します。 SIP/MTLS/TCP 5061 によるディレクター、フロントエンドプール、フロントエンドサーバーからエッジサーバーの内部インターフェイスへの通信を可能にするルールも作成する必要があります。

### <a name="director-ports-and-protocols-for-firewall-definitions"></a>ファイアウォールの定義用のディレクターポートとプロトコル

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Role/Protocol/TCP または UDP/ポート</th>
<th>送信元 IP アドレス</th>
<th>宛先 IP アドレス</th>
<th>メモ</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>HTTP/TCP 8080</p></td>
<td><p>リバースプロキシ内部インターフェイス</p></td>
<td><p>ディレクターハードウェアロードバランサー VIP</p></td>
<td><p>リバースプロキシの外部で最初に受信した通信は、ディレクター HLB VIP とフロントエンドサーバー web サービスに送信されます。</p></td>
</tr>
<tr class="even">
<td><p>HTTPS/TCP 4443</p></td>
<td><p>リバースプロキシ内部インターフェイス</p></td>
<td><p>ディレクターハードウェアロードバランサー VIP</p></td>
<td><p>リバースプロキシの外部で最初に受信した通信は、ディレクター HLB VIP とフロントエンドサーバー web サービスに送信されます。</p></td>
</tr>
<tr class="odd">
<td><p>HTTPS/TCP 444</p></td>
<td><p>ディレクター</p></td>
<td><p>フロントエンドサーバーまたはフロントエンドプール</p></td>
<td><p>ディレクター HLB VIP とフロントエンドサーバー間のサーバー間通信</p></td>
</tr>
<tr class="even">
<td><p>HTTP/TCP 80</p></td>
<td><p>内部クライアント</p></td>
<td><p>ディレクターハードウェアロードバランサー VIP</p></td>
<td><p>ディレクターは、内部および外部クライアントに web サービスを提供します。</p></td>
</tr>
<tr class="odd">
<td><p>HTTPS/TCP 443</p></td>
<td><p>内部クライアント</p></td>
<td><p>ディレクターハードウェアロードバランサー VIP</p></td>
<td><p>ディレクターは、内部および外部クライアントに web サービスを提供します。</p></td>
</tr>
<tr class="even">
<td><p>SIP/MTLS/TCP 5061</p></td>
<td><p>エッジサーバーの内部インターフェイス</p></td>
<td><p>ディレクターハードウェアロードバランサー VIP</p></td>
<td><p>エッジサーバーからディレクターへの SIP 通信と、フロントエンドサーバー。</p></td>
</tr>
<tr class="odd">
<td><p>MTLS/TCP/50001</p></td>
<td><p>任意</p></td>
<td><p>ディレクター</p></td>
<td><p>一元管理サービスコントローラー (ClsController.exe) またはエージェント (ClsAgent.exe) コマンドとログ収集</p></td>
</tr>
<tr class="even">
<td><p>MTLS/TCP/50002</p></td>
<td><p>任意</p></td>
<td><p>ディレクター</p></td>
<td><p>一元管理サービスコントローラー (ClsController.exe) またはエージェント (ClsAgent.exe) コマンドとログ収集</p></td>
</tr>
<tr class="odd">
<td><p>MTLS/TCP/50003</p></td>
<td><p>任意</p></td>
<td><p>ディレクター</p></td>
<td><p>一元管理サービスコントローラー (ClsController.exe) またはエージェント (ClsAgent.exe) コマンドとログ収集</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

