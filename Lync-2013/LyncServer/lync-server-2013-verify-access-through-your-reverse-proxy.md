---
title: 'Lync Server 2013: リバース プロキシ経由のアクセスを確認する'
description: 'Lync Server 2013: リバースプロキシ経由でアクセスを確認します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verify access through your reverse proxy
ms:assetid: 3076a786-e022-4d41-91ec-1bf252b2a468
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429697(v=OCS.15)
ms:contentKeyID: 48183753
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 593aac5574f0dcf683351f12a6392f6116480ac5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443476"
---
# <a name="verify-access-through-your-reverse-proxy-in-lync-server-2013"></a>Lync Server 2013 でリバース プロキシ経由のアクセスを確認する

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2013-03-29_

リバースプロキシ上の情報にユーザーがアクセスできることを確認するには、次の手順に従います。 Access が正常に動作するためには、ファイアウォールの構成とドメインネームシステム (DNS) の構成を完了する必要がある場合があります。

<div>

## <a name="to-verify-that-you-can-access-the-website-through-the-internet"></a>インターネット経由で web サイトにアクセスできることを確認するには

  - Web ブラウザーを開き、クライアントがアドレス帳ファイルと会議の web サイトにアクセスするために使用する **アドレス** バーに、次のように url を入力します。
    
      - アドレス帳サーバーの場合、次のような URL を入力します。ここで、 **https://externalwebfarmFQDN/abs** externalwebfarmFQDN は、アドレス帳サービスをホストする外部 web サービスの外部 FQDN です。 アドレス帳サーバーフォルダーのディレクトリセキュリティが既定で Windows 認証に構成されているため、ユーザーは HTTP チャレンジを受け取る必要があります。
    
      - [会議] には、次のような URL を入力します。ここで、 **https://externalwebfarmFQDN/meet** externalwebfarmFQDN は会議コンテンツをホストする web ファームの外部 FQDN です。 この URL には、会議のトラブルシューティングページが表示されます。 または、会議の簡単な URL が正しく機能することを確認します。 会議参加の単純な URL の例を次に示します。 https://meet.contoso.com
    
      - 配布グループの展開については、次のような URL を入力 **https://externalwebfarmFQDN/GroupExpansion/service.svc** してください。 配布グループ展開サービスのディレクトリセキュリティが既定で Windows 認証に構成されているため、ユーザーは HTTP チャレンジを受け取る必要があります。
    
      - [ダイヤルイン] には、次のような単純な URL を入力し **https://externalwebfarmFQDN/dialin** ます。ここで、externalwebfarmFQDN は、ダイヤルイン会議のダイヤルインページをホストする web ファームの外部 FQDN です。 ユーザーは、ダイヤルインページに転送される必要があります。 または、Simple URL のダイヤルイン機能が正しく動作することを確認します。 ダイヤルインの単純な URL の例を次に示します。 https://dialin.contoso.com
    
      - 自動検出 URL が機能していることを確認するには、「」と入力 https://lyncdiscover します。 Externaldomaqdn。 ブラウザーでファイルを開くように求められます。 [メモ帳] を選択して開きます。 一般的な応答は、次のようになります。
        
            {"AccessLocation":"External","Root":{"Links":[{"href":"https:\/\/extweb.contoso.com\/Autodiscover\/AutodiscoverService.svc\/root\/domain","token":"Domain"},
            {"href":"https:\/\/extweb.contoso.com\/Autodiscover\/AutodiscoverService.svc\/root\/user","token":"User"},
            {"href":"https:\/\/lyncweb.contoso.com\/Autodiscover\/AutodiscoverService.svc\/root\/oauth\/user","token":"OAuth"}]}}

</div>

</div>

<span> </span>

</div>

</div>

</div>

