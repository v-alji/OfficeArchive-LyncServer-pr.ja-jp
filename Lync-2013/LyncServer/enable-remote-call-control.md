---
title: リモート通話コントロールを有効にする
description: リモート通話コントロールを有効にします。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Enable remote call control
ms:assetid: 0b91d418-e6ed-4556-97af-e8523e01f249
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204664(v=OCS.15)
ms:contentKeyID: 48183380
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8009ffc927ad3f7a4f83ad3505100f3a9d4e82d6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398781"
---
# <a name="enable-remote-call-control"></a>リモート通話コントロールを有効にする

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-10-02_

リモート通話コントロールを使用すると、ユーザーは Lync Server 2013 を使用して、デスクトップのプライベートブランチ exchange (PBX) 電話を制御できます。 従来の環境でリモート通話コントロールを展開して、Lync Server 2013 を移行する必要がある場合は、次のタスクを実行する必要があります。

1.  SIP/CSTA ゲートウェイをインストールして、PBX と通信できるように設定します。 Lync Server 2013 パイロットプールを展開する場合は、この手順を実行する必要があります。

2.  トポロジを結合してポリシーと設定を移行した後で、Lync Server 2013 を構成して、CSTA 要求が SIP/CSTA ゲートウェイにルーティングされるようにします。 この手順は、自動移行の後に続く手動の手順です。 CSTA 要求のルーティングを構成するには、次の操作を行います。
    
      - 従来の承認済みホストエントリを削除します (Lync Server 2013 では、 *信頼されたサーバーエントリ* と呼ばれます)。 従来の展開からユーザーを移行する場合は、Lync Server 2013 パイロットプールで新しい信頼されたアプリケーションのエントリを構成する前に、SIP/CSTA ゲートウェイ用に作成した既存の認証済みホストエントリをすべて削除してください。 従来の承認済みホストのエントリを削除する方法について詳しくは、「承認され [たホストエントリを削除](remove-an-authorized-host-entry.md)する」をご覧ください。
    
      - リモート通話コントロールの静的ルートを構成します。 リモート通話コントロールをサポートする個々のプールに対して静的ルートを構成できます。また、プールレベルの静的ルートで構成されていない各プールがグローバル静的ルートを使うように、グローバル静的ルートを構成することもできます。 静的ルートを構成する方法の詳細については、展開ドキュメントの「 [Lync Server 2013 でリモート通話コントロールの静的ルートを構成](lync-server-2013-configure-a-static-route-for-remote-call-control.md) する」を参照してください。
    
      - リモート通話コントロールをサポートする各プールで、リモート通話コントロール用の信頼されたアプリケーションエントリを構成します。 信頼されたアプリケーションのエントリを構成する方法の詳細については、展開ドキュメントの「 [Lync Server 2013 でのリモート通話コントロール用に信頼されているアプリケーションエントリを構成](lync-server-2013-configure-a-trusted-application-entry-for-remote-call-control.md) する」を参照してください。

3.  伝送制御プロトコル (TCP) を使って Lync Server 2013 に接続している SIP/CSTA ゲートウェイを展開した場合は、トポロジビルダーでゲートウェイの IP アドレスを定義してください。 IP アドレスの定義の詳細については、展開ドキュメントの「 [Lync Server 2013 で SIP/CSTA ゲートウェイの IP アドレスを定義する](lync-server-2013-define-a-sip-csta-gateway-ip-address.md) 」を参照してください。

4.  リモートの通話コントロールを有効にし、line server の Uniform Resource Identifier (URI) と行の URI を割り当てることで、リモート通話コントロール用に Lync 2013 ユーザーを構成します。 従来の展開から Lync Server 2013 にユーザーを移行すると、リモートの通話コントロールの設定が他のユーザーの設定とともに移行されます。

5.  従来の展開で、アドレス帳の電話番号の正規化ルールをカスタマイズした場合、カスタマイズされた正規化ルールを移行するには、ポリシーの自動移行と設定が完了した後に、いくつかの手動タスクを実行する必要があります。 正規化ルールをカスタマイズしていない場合は、アドレス帳が他のトポロジと共に移行されます。 カスタマイズされた正規化ルールを手動で移行する方法について詳しくは、「 [アドレス帳を移行](migrate-address-book.md)する」をご覧ください。

</div>

<span> </span>

</div>

</div>

</div>

