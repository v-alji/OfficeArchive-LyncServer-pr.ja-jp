---
title: 'Lync Server 2013: Lync Room System 管理 Web ポータルをインストールする'
description: 'Lync Server 2013: Lync Room System 管理 Web ポータルをインストールします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Installing the Lync Room System Administrative Web Portal
ms:assetid: dd19e368-c338-4e21-a40d-6439d46a9748
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn436326(v=OCS.15)
ms:contentKeyID: 56737622
ms.date: 04/09/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0fba239346d75142bb4009c58e0ac67e8e1f3bcb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427006"
---
# <a name="installing-the-lync-room-system-administrative-web-portal-in-lync-server-2013"></a>Installing the Lync Room System Administrative Web Portal in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2015-04-09_

Microsoft Lync Room System 管理 Web ポータルは、Microsoft ダウンロードセンターからダウンロードでき [https://go.microsoft.com/fwlink/p/?LinkId=324044](https://go.microsoft.com/fwlink/p/?linkid=324044) ます。

Lync Room System 管理 Web ポータルをインストールするには、次の手順を使用します。

1.  Lync Server 管理シェルで次のコマンドレットを実行して、信頼されているアプリケーションポートを構成します。
    
        Set-CsWebServer -Identity POOLFQDN -MeetingRoomAdminPortalInternalListeningPort 4456 -MeetingRoomAdminPortalExternalListeningPort 4457

2.  会議室ポータルをインストールするには、 **LyncRoomAdminPortal.exe** をダウンロードしてから、管理者として実行します。

3.  Web.config ファイルを次の場所から開きます。
    
    % Program Files% \\ Microsoft Lync Server 2013 \\ Web コンポーネント \\ 会議室ポータルの \\ Int \\ ハンドラー\\

4.  Web.Config ファイルで、「Lync Room System 管理ポータルの前提条件を設定する」セクションの「手順2で作成したユーザー名に PortalUserName を変更します (手順は LRSApp の推奨名)。
    
        <add key="PortalUserName" value="sip:LRSApp@domain.com" />

5.  LRS 管理ポータルは信頼できるアプリケーションであるため、ポータル構成でパスワードを入力する必要はありません。 このユーザーがローカル レジストラーとは別のレジストラーを使用している場合、Web.Config ファイルで次の行を追加してレジストラを指定する必要があります。
    
        <add key="PortalUserRegistrarFQDN" value="pool-xxxx.domain.com" />

6.  5061 以外のポートが使用されている場合は、Web.Config ファイルに次の行を追加します。
    
        <add key="PortalUserRegistrarPort" value="5061" />

<div>

## <a name="verifying-installation-of-the-lync-room-system-administrative-web-portal"></a>Lync Room System 管理 Web ポータルのインストールを確認する

Lync Room System 管理 Web ポータルのインストールを確認するには、次の操作を行います。


1.  フロントエンド サーバーで、次の URL を参照します。
    
    https:// \<fe-server\> /lrs
    
    下記の画像のように、エラーが表示されないようにします。
    
    ![Lync Room System、管理用ポータル サインイン画面](images/Dn436326.050bcf70-2f3b-46b2-9b96-ebd12679b713(OCS.15).png "Lync Room System、管理用ポータル サインイン画面")

2.  エラーが表示されない場合は、トポロジ内の他のいずれかのコンピューターから次の URL へのアクセスを試行します。
    
    https:// \<fe-server\> /lrs
    
    このページにアクセスするには、「」の「自動クライアントサインイン用の DNS レコード」の説明に従って DNS レコードを追加する必要があり [https://go.microsoft.com/fwlink/p/?LinkId=318056](https://go.microsoft.com/fwlink/p/?linkid=318056) ます。

</div>

</div>

<span> </span>

</div>

</div>

</div>

