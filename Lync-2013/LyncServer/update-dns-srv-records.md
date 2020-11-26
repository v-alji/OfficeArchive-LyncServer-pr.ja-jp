---
title: DNS SRV レコードの更新
description: DNS SRV レコードを更新します。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Update DNS SRV records
ms:assetid: 9542b91a-108c-4980-89ec-634905cbbf26
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688139(v=OCS.15)
ms:contentKeyID: 49733739
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 24161074e8f3bcf7e296a957588eeb59d5f2ad1b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446550"
---
# <a name="update-dns-srv-records"></a>DNS SRV レコードの更新

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-09-29_

この手順を完了するには、サーバーまたはドメインに、Domain Admins グループのメンバーまたは DnsAdmins グループのメンバーとしてログオンしている必要があります。

このトピックでは、Lync Server 2013 に移行した後に、ドメインネームシステム (DNS) レコードを更新する方法について説明します。 すべてのユーザーが Lync Server 2013 に移動された後、従来の Lync Server 2010 プールまたはディレクターが廃止される前に、各 SIP ドメインの内部 DNS の DNS SRV レコードを更新する必要があります。 この手順では、内部 DNS に SIP ユーザードメイン用のゾーンが含まれていることを前提としています。

**DNS SRV レコードを構成するには**

1.  DNS サーバーで [ **スタート**] をクリックし、[ **管理ツール**]、[ **dns**] の順にクリックします。

2.  SIP ドメインのコンソールツリーで [**前方参照ゾーン**] を展開し、Lync Server 2013 がインストールされている SIP ドメインを展開して、[ **\_ tcp** ] 設定に移動します。

3.  右側のウィンドウで、[ **\_ sipinternaltls** ] を右クリックし、[**プロパティ**] を選択します。

4.  [ **このサービスを提供** しているホスト] で、Lync Server 2013 プールを指すようにホストの FQDN を更新します。

5.  **[OK]** をクリックします。

**フロントエンドプールまたは Standard Edition サーバーの FQDN が解決できることを確認するには**

1.  ドメイン内のクライアントコンピューターにログオンします。

2.  [**スタート**] ボタンをクリックし、[**ファイル名を指定して実行**] をクリックします。

3.  [ **開く** ] ボックスに **cmd** と入力し、[ **OK**] をクリックします。

4.  コマンドプロンプトで、「 **nslookup** 」 \<FQDN of the Front End pool\> または「」と入力し、 \<FQDN of the Standard Edition server\> enter キーを押します。

5.  FQDN の適切な IP アドレスに解決される返信を受信したことを確認します。

</div>

<span> </span>

</div>

</div>

</div>

