---
title: 'Lync Server 2013: DNS SRV レコードの作成と確認'
description: 'Lync Server 2013: DNS SRV レコードを作成して確認します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create and verify DNS SRV records
ms:assetid: 86888c7e-1401-458f-9a7b-08ac726deeec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398680(v=OCS.15)
ms:contentKeyID: 48184714
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a71c876d0b26b9305feed7146fa6321a3983588d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432017"
---
# <a name="create-and-verify-dns-srv-records-in-lync-server-2013"></a>Lync Server 2013 での DNS SRV レコードの作成と確認

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2013-02-21_

この手順を完了するには、ドメイン管理者グループのメンバー、または DnsAdmins グループのメンバーとして、サーバーまたはドメインに最低でもログオンしている必要があります。

このトピックでは、Lync Server 2013 の展開で作成する必要があるドメインネームシステム (DNS) レコードを構成する方法と、自動クライアントサインインに必要なものを構成する方法について説明します。 フロントエンドプールを作成すると、セットアップによってプールの Active Directory オブジェクトと設定が作成されます。これには、プールの完全修飾ドメイン名 (FQDN) が含まれます。 同様のオブジェクトと設定が、Standard Edition サーバー用に作成されます。 クライアントがプールまたは Standard Edition サーバーに接続できるようにするには、プールまたは Standard Edition サーバーの FQDN が DNS に登録されている必要があります。 SIP ドメインごとに、内部 DNS で DNS SRV レコードを作成する必要があります。 この手順では、内部 DNS に SIP ユーザードメイン用のゾーンが含まれていることを前提としています。

<div>

## <a name="to-configure-a-dns-srv-record"></a>DNS SRV レコードを構成するには

1.  DNS サーバーで [ **スタート**] をクリックし、[ **管理ツール**]、[ **dns**] の順にクリックします。

2.  SIP ドメインのコンソールツリーで [ **前方参照ゾーン**] を展開し、Lync Server 2013 がインストールされる SIP ドメインを右クリックします。

3.  [ **その他の新しいレコード**] をクリックします。

4.  [**リソース レコードの種類を選択**] の [**サービス ロケーション (SRV)**] をクリックし、[**レコードの作成**] をクリックします。

5.  [**サービス**] をクリックして、「 **\_ sipinternaltls**」と入力します。

6.  [**プロトコル**] をクリックして、「 **\_ tcp**」と入力します。

7.  [**ポート番号**] をクリックし、「**5061**」と入力します。

8.  [**このサービスを提供しているホスト**] をクリックして、プールまたは Standard Edition サーバーの FQDN を入力します。

9.  [**OK**] をクリックしてから、[**完了**] をクリックします。

</div>

<div>

## <a name="to-verify-the-creation-of-a-dns-srv-record"></a>DNS SRV レコードの作成を確認するには

1.  Authenticated Users グループのメンバーであるアカウントまたは同等のアクセス許可を持つアカウントを使用して、ドメインのクライアント コンピューターにログオンします。

2.  [**スタート**] ボタンをクリックし、[**ファイル名を指定して実行**] をクリックします。

3.  [ **開く** ] ボックスに **cmd** と入力し、[ **OK**] をクリックします。

4.  コマンドプロンプトで「 **nslookup**」と入力し、enter キーを押します。

5.  「 **Set type = srv**」と入力して、enter キーを押します。

6.  「Sipinternaltls」と入力 **\_ します。 \_tcp.contoso.com** を選び、enter キーを押します。 トランスポート層セキュリティ (TLS) レコードに対して表示される出力は、次のようになります。
    
    サーバー: \<dns server\> contoso.com
    
    アドレス \<IP address of DNS server\>
    
    権限のない回答:
    
    \_sipinternaltls。 \_tcp.contoso.com SRV サービスの場所:
    
    priority = 0
    
    weight = 0
    
    ポート = 5061
    
    svr hostname = poolname.contoso.com (または Standard Edition server A レコード)
    
    poolname.contoso.com インターネットアドレス = \<virtual IP Address of the load balancer\> また \<IP address of a single Enterprise Edition server for pools with only one Enterprise Edition server\> は \<IP address of the Standard Edition server\>

7.  完了したら、コマンドプロンプトで「 **exit**」と入力し、enter キーを押します。

</div>

<div>

## <a name="to-verify-that-the-fqdn-of-the-front-end-pool-or-standard-edition-server-can-be-resolved"></a>フロントエンドプールまたは Standard Edition サーバーの FQDN が解決できることを確認するには

1.  ドメイン内のクライアントコンピューターにログオンします。

2.  [**スタート**] ボタンをクリックし、[**ファイル名を指定して実行**] をクリックします。

3.  [ **開く** ] ボックスに **cmd** と入力し、[ **OK**] をクリックします。

4.  コマンドプロンプトで、「 **nslookup** 」 \<FQDN of the Front End pool\> または「」と入力し、 \<FQDN of the Standard Edition server\> enter キーを押します。

5.  FQDN の適切な IP アドレスに解決される返信を受信したことを確認します。

</div>

</div>

<span> </span>

</div>

</div>

</div>

