---
title: 'Lync Server 2013: 自動検出サービスの要件'
description: 'Lync Server 2013: 自動検出サービス要件。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Autodiscover service requirements
ms:assetid: 0ac5dbf7-9acd-4d25-b21a-932022b8b983
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690012(v=OCS.15)
ms:contentKeyID: 48183368
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 61e963bc9e921cc0a571f63d4be50f09d237c2dd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438128"
---
# <a name="autodiscover-service-requirements-for-lync-server-2013"></a>Lync Server 2013 の自動検出サービスの要件

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2013-02-25_

Microsoft Lync Server 2013 自動検出サービスは、監督およびフロントエンドプールサーバー上で実行され、DNS で公開されると、Lync Mobile を実行しているモバイルデバイスでモビリティサービスを見つけることができます。 Lync Mobile を実行しているモバイルデバイスでは自動検出機能を利用できますが、自動検出サービスを実行しているディレクターおよびフロントエンドサーバーで証明書のサブジェクトの代替名の一覧を変更する必要があります。 さらに、リバースプロキシの外部 web サービス公開ルールに使用されている証明書のサブジェクト代替名の一覧を変更することが必要になる場合もあります。

ディレクター、フロントエンドサーバー、リバースプロキシに必要なサブジェクト代替名のエントリの詳細については、「モビリティの計画」の「 [Lync Server 2013 でのモビリティの技術要件](lync-server-2013-technical-requirements-for-mobility.md) 」を参照してください。

リバースプロキシでのサブジェクト代替名の一覧の使用に関する決定は、自動検出サービスをポート80またはポート443のどちらに発行するかに基づきます。

  - **ポート80で公開**   自動検出サービスへの初期クエリがポート80経由で行われる場合、証明書の変更は必要ありません。 これは、Lync を実行しているモバイルデバイスは、ポート80の逆プロキシに外部からアクセスして、ポート8080の内部でディレクターまたはフロントエンドサーバーにリダイレクトされるためです。 詳細については、このトピックの後半の「ポート80を使った最初の自動検出プロセス」を参照してください。

  - **ポート443で公開**  外部 web サービス公開ルールによって使用される証明書のサブジェクト代替名リストには、lyncdiscover が含まれている必要があり *ます。 \<sipdomain\>* 組織内の各 SIP ドメインのエントリ。

内部証明機関を使用した再発行証明書は、通常、単純なプロセスですが、web サービス公開ルールで使用される公開証明書の場合、複数のサブジェクト代替名エントリを追加すると、負荷が高くなる可能性があります。 この問題を回避するには、ポート80経由の最初の自動検出接続をサポートします。その後、ディレクターまたはフロントエンドサーバー上のポート8080にリダイレクトされます。

たとえば、Lync Mobile を実行しているモバイルクライアントが、最初の要求に対して HTTP を使用して自動検出機能を使用して Lync Server 2013 にサインインするように構成されていることを前提とします。

<div>

## <a name="initial-autodiscover-process-for-mobile-devices-using-port-80"></a>ポート80を使ったモバイルデバイスの初期自動検出プロセス

1.  Lync Mobile を実行しているモバイルデバイスでは、DNS を使用して lyncdiscover.contoso.com を検索します。この場合、A レコードが存在します。

2.  外部 DNS は、外部 web サービスの IP アドレスをクライアントに返します。

3.  Lync Mobile を実行しているモバイルデバイス http://lyncdiscover.contoso.com?sipuri=lyncUser1@contoso.com は、リバースプロキシに要求を送信します。

4.  Web 発行ルールによって、ポート80からの外部への要求が内部でポート8080にブリッジされ、ディレクターまたはフロントエンドサーバーにルーティングされます。
    
    要求は HTTP であり、HTTPS ではないため、自動検出サービスをサポートするために、外部 web サービス公開ルールの証明書に変更を加える必要はありません。

5.  自動検出サービスは、外部 web サービスの Url (HTTPS 形式) を返します。

6.  Lync Mobile を実行しているモバイルデバイスは、ポート443のリバースプロキシに再接続し、ユーザーのホームプールで実行されているモビリティサービスに4443経由でリダイレクトされます。
    
    HTTPS クエリは、外部 web サービスの URL と自動検出サービスの URL の対比で行われるため、その証明書には、外部 web サービスの完全修飾ドメイン名 (Fqdn) に対するサブジェクト代替名のエントリが既に含まれているため、成功します。
    
    このシナリオでは、モバイル機能をサポートするために必要な証明書の変更はありません。
    
    <div>
    

    > [!NOTE]  
    > ターゲット web サーバーに、lyncdiscover.contoso.com の値が一致しない証明書がサブジェクトの代替名の一覧の値として含まれている場合:<BR>a. &nbsp; &nbsp; &nbsp;Web サーバーは、"Server Hello" と証明書を使って応答しません。<BR>b. &nbsp; &nbsp; &nbsp;Lync Mobile を実行しているモバイルデバイスは、直ちにセッションを終了します。<BR>ターゲット web サーバーに、サブジェクトの代替名の一覧の値として lyncdiscover.contoso.com を含む証明書がある場合:<BR>a. &nbsp; &nbsp; &nbsp;Web サーバーは、"Server hello" と証明書で応答します。<BR>b. &nbsp; &nbsp; &nbsp;Lync Mobile を実行しているモバイルデバイスは、証明書を検証し、ハンドシェイクを完了します。

    
    </div>

リバースプロキシサーバーでポート80を使って自動検出サービスへの最初の接続をサポートするには、次の例のような http 発行ルールを作成できます。これは、Forefront Threat Management Gateway 2010 リバースプロキシ web 発行ルール

1.  新しい web 公開ルールを作成します (たとえば、 **Lync Server の自動検出 (HTTP)**)。

2.  [ **パブリック名**] に「lyncdiscover.contoso.com」と入力します。

3.  [ **ブリッジ** ] タブで、ポート80からポート8080への要求をブリッジするオプションのみを選択します。

4.  [ **認証** ] タブで、[ **認証なし**] を選択し、 **クライアントは直接認証を行うことはできません**。

5.  変更をコミットし、Lync ルールの一覧の一番上 (最初の処理順序) にルールを移動します。

</div>

<div>

## <a name="mobility-for-the-split-domain-deployment"></a>分離ドメイン展開のモビリティ

共有 SIP アドレス空間 ( *分割ドメイン* とも呼ばれます) または *ハイブリッド展開* とは、ユーザーがオンプレミスの展開とオンライン環境の間で展開される構成です。 目的は、ホームサーバーが配置されている場所 (オンプレミスまたはオンライン) に関係なく、展開にログインし、ホームサーバーの場所にリダイレクトされるようにすることです。 これを実現するために、Microsoft Lync Server 2013 の自動検出機能を使用して、オンラインユーザーをオンライントポロジにリダイレクトします。 これを行うには、Lync Server 管理シェルを使用して、自動検出の uri (URL) を構成します。また、コマンドレットは、「 **CsHostingProvider** 」と「 **Set-CsHostingProvider**」を選びます。

次の展開された属性を収集して記録する必要があります。

  - Lync Server 管理シェルで、「
    
        Get-CsHostingProvider

  - 結果で、属性 **Proxyfqdn** を含むオンラインプロバイダーを見つけます。 たとえば、sipfed.online.lync.com

  - ProxyFQDN の値を記録する

  - オンプレミスの Lync Server コントロールパネルでフェデレーションを有効にして、オンラインプロバイダーとのフェデレーションを許可する

  - オンラインプロバイダーのフェデレーションを有効にします。 既定では、すべてのオンラインユーザーがドメインフェデレーションを有効にしており、すべてのドメインと通信できます。

  - ブロックドメインと許可ドメインを定義する場合は、明示的に許可するか、明示的にブロックするドメインを決定します。

  - オンラインフェデレーションの場合、ファイアウォールの例外、証明書と DNS ホスト (IPv6 を使用している場合は AAAA) を計画する必要があります。 さらに、フェデレーションポリシーを構成する必要があります。 詳細については、「 [Lync server 2013 と Office Communications server フェデレーションの計画](lync-server-2013-planning-for-lync-server-and-office-communications-server-federation.md)」を参照してください。

</div>

</div>

<span> </span>

</div>

</div>

</div>

