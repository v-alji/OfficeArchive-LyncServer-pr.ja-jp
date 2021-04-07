---
title: 'Lync Server 2013: Lync フェデレーションのセットアップ'
description: 'Lync Server 2013: Lync フェデレーションのセットアップ。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up Lync federation
ms:assetid: 374ddc43-26f9-499d-be68-a5158adfa49c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204800(v=OCS.15)
ms:contentKeyID: 48183822
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 382def41635f05525e5b047e97febffdb069da2a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399812"
---
# <a name="setting-up-lync-federation-in-lync-server-2013"></a>Lync Server 2013 での Lync フェデレーションのセットアップ

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**トピック最終更新日:** 2014-03-27_

エッジ サーバーまたはエッジ サーバーを既に展開している場合は、フェデレーション シナリオ機能の追加は簡単です。 エッジ サーバーをセットアップしていない場合は、最初にセットアップする必要があります。 詳細については、「計画」の [「Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) での外部ユーザー アクセスの計画」および「展開ドキュメントの [Lync Server 2013](lync-server-2013-deploying-external-user-access.md) での外部ユーザー アクセスの展開」を参照してください。

<div>


> [!NOTE]  
> XMPP フェデレーション、Lync フェデレーション、またはパブリック インスタント メッセージング接続の任意の組み合わせをセットアップする場合は、それらを同時に、または一度に 1 つ展開できます。 トポロジ ビルダーと Lync Server 管理シェルを使用してオプションを構成し、1 つ、2 つ、または 3 つのフェデレーション の種類のオプションを構成した後、エッジ サーバーで展開ウィザードを実行すると、必要な手順の数を減らできます。



</div>

<div>

## <a name="setting-up-lync-federation-in-topology-builder-and-the-deployment-wizard"></a>トポロジ ビルダーと展開ウィザードでの Lync フェデレーションのセットアップ

1.  フロント エンド サーバーでトポロジ ビルダーを開きます。 エッジ プールを展開し、Edge サーバーまたはエッジ サーバー プールを右クリックします。 [プロパティの編集] を選択します。

2.  [全般] の [プロパティの編集] で、このエッジ プールのフェデレーションを有効にする (ポート 5061) を選択します。 [OK] をクリックします。

3.  [アクション] をクリックし、[トポロジ] を選択し、[発行] を選択します。 [トポロジの公開] のメッセージが表示されたら、[次へ] をクリックします。 発行が完了したら、[完了] をクリックします。

4.  エッジ サーバーで、Lync Server 展開ウィザードを開きます。 [Lync Server System のインストールまたは更新] をクリックし、[Lync Server コンポーネントのセットアップまたは削除] をクリックします。 [もう一度実行] をクリックします。

5.  Lync Server コンポーネントのセットアップで、[次へ] をクリックします。 実行されると、概要画面にアクションが表示されます。 展開が完了したら、[ログの表示] をクリックして、利用可能なログ ファイルを表示します。 [完了] をクリックして展開を完了します。
    
    <div>
    

    > [!IMPORTANT]  
    > このオプションは選択できますが、フェデレーションのために外部に公開できるのは組織内のエッジ プールまたはエッジ サーバーの 1 つのみです。 パブリック インスタント メッセージング (IM) ユーザーを含むフェデレーション ユーザーによるすべてのアクセスは、同じエッジ プールまたは単一のエッジ サーバーを経由します。 たとえば、展開にニューヨークに展開されたエッジ プールまたは 1 つのエッジ サーバーが含まれる場合、またロンドンに展開されたエッジ サーバーが含まれる場合、ニューヨーク エッジ プールまたは単一エッジ サーバーでフェデレーション サポートを有効にした場合、フェデレーション ユーザーのシグナル トラフィックは、ニューヨーク エッジ プールまたは単一エッジ サーバーを経由します。 これは、ロンドンのユーザーとの通信でも当てはめますが、ロンドンのフェデレーション ユーザーを呼び出すロンドンの内部ユーザーは、A/V トラフィックにロンドン プールまたはエッジ サーバーを使用します。

    
    </div>

</div>

<div>

## <a name="configuring-federation-with-partners"></a>パートナーとのフェデレーションの構成

1.  別の Microsoft Lync Server 2013、Lync Server 2010、Office Communications Server 2007 R2、または Office Communicator 2007 とのフェデレーションを正常にセットアップするには、次の表からフェデレーションの種類を選択し、DNS SRV レコード、DNS ホスト (A または AAAA for IPv6) を定義し、フェデレーションの種類に適用されるポリシーを構成します。
    
    
    <table>
    <colgroup>
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>フェデレーションの種類</th>
    <th>DNS レコード</th>
    <th>ポリシー定義</th>
    <th>備考</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p>検出されたパートナー ドメイン</p></td>
    <td><p>_sipfederationtls._tcp の形式の SRV レコードを構成します。 &lt;外部ドメイン名 SRV レコードのポート値が TCP 5061 で、このサービスを提供する &gt; <strong>ホスト</strong> が sip として定義されている場合。 &lt;外部ドメイン &gt; 名 – Access Edge サービスの FQDN。 SRV <a href="lync-server-2013-configure-dns-for-edge-support.md">レコードの作成の詳細については、「Lync Server 2013</a> でエッジ サポートの DNS を構成する」を参照してください。</p></td>
    <td><ul>
    <li><p><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Lync Server 2013 でのフェデレーションおよびパブリック IM 接続の有効化または無効化</a></p></li>
    <li><p><a href="lync-server-2013-enable-or-disable-discovery-of-federation-partners.md">Lync Server 2013 でのフェデレーション パートナーの検出の有効化または無効化</a></p></li>
    </ul></td>
    <td><p>以前のバージョンでは、この種類のフェデレーションを Open <strong>Enhanced Federation と呼ばていました</strong>。 SRV レコードの作成は、この種類のフェデレーションに必要であり、他のパートナーがフェデレーションを検出するために必要です。</p></td>
    </tr>
    <tr class="even">
    <td><p>許可されたパートナー ドメイン</p></td>
    <td><p>_sipfederationtls._tcp の形式の SRV レコードを構成します。 &lt;外部ドメイン名 SRV レコードのポート値が TCP 5061 で、このサービスを提供する &gt; <strong>ホスト</strong> が sip として定義されている場合。 &lt;外部ドメイン &gt; 名 – Access Edge サービスの FQDN。 SRV <a href="lync-server-2013-configure-dns-for-edge-support.md">レコードの作成の詳細については、「Lync Server 2013</a> でエッジ サポートの DNS を構成する」を参照してください。</p></td>
    <td><ul>
    <li><p><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Lync Server 2013 でのフェデレーションおよびパブリック IM 接続の有効化または無効化</a></p></li>
    </ul></td>
    <td><p>以前のバージョンでは、この種類のフェデレーションを拡張フェデレーション <strong>と呼ば呼ばされました</strong>。 SRV レコードの作成は、この種類のフェデレーションでは省略可能であり、他のパートナーがフェデレーションを検出できます。 当然ながら、これはオープン <strong>拡張フェデレーション、</strong>または検出されたパートナー <strong>ドメインです</strong></p></td>
    </tr>
    <tr class="odd">
    <td><p>許可されたパートナー サーバー</p></td>
    <td><p>ポリシーでフェデレーション パートナーとして SIP ドメイン名とパートナー エッジ サーバー FQDN を構成する</p></td>
    <td><ul>
    <li><p><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Lync Server 2013 でのフェデレーションおよびパブリック IM 接続の有効化または無効化</a></p></li>
    <li><p><a href="lync-server-2013-configure-support-for-allowed-external-domains.md">Lync Server 2013 での、許可された外部ドメイン向けサポートの構成</a></p></li>
    <li><p><a href="lync-server-2013-configure-support-for-blocked-external-domains.md">Lync Server 2013 での禁止された外部ドメイン向けサポートの構成</a></p></li>
    </ul></td>
    <td><p>このフェデレーションの種類は、1 対 1 のリレーションシップの定義であり、他のフェデレーション パートナーの検出を許可します。 各フェデレーション パートナーは明示的に構成されます。 以前のバージョンでは、これは直接フェデレーションと <strong>呼ばれる機能でした。</strong></p></td>
    </tr>
    <tr class="even">
    <td><p>ホスティング プロバイダーとパブリック IM プロバイダー</p></td>
    <td><p>この種のフェデレーションに特定の DNS 要件が定義されていない</p></td>
    <td><ul>
    <li><p><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Lync Server 2013 でのフェデレーションおよびパブリック IM 接続の有効化または無効化</a></p></li>
    <li><p><a href="lync-server-2013-create-or-edit-public-sip-federated-providers.md">Lync Server 2013 での公開 SIP フェデレーション プロバイダーの作成または編集</a></p></li>
    <li><p><a href="lync-server-2013-create-or-edit-hosted-sip-federated-providers.md">Lync Server 2013 でのホスト SIP フェデレーション プロバイダーの作成または編集</a></p></li>
    </ul></td>
    <td><p>このフェデレーションの種類は、ユーザー用に構成するサービスとホスティング プロバイダーを定義します。 一般的な用途には Windows Live Messenger、Yahoo! および AOL、および Lync Online や Microsoft 365 などのホスティング プロバイダー</p>
    <div>

    > [!IMPORTANT]  
    > <UL>
    > <LI>
    > <P>2012 年 9 月 1 日の現在、Microsoft Lync Public IM Connectivity User Subscription License ("PIC USL") は新規または更新契約の購入で利用できなくなりました。 アクティブなライセンスをお持ちのお客様は、引き続き Yahoo! サービスが日付をシャットダウンするまで Messenger。 AOL および Yahoo! が発表されました。 詳細については <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">、Lync Server 2013</A>のパブリック インスタント メッセンジャー接続のサポートを参照してください。</P>
    > <LI>
    > <P>PIC USL は、Lync Server または Office Communications Server が Yahoo! Messenger。 このサービスを提供する Microsoft の機能は、基になる契約である Yahoo! からのサポートを受け始め、曲がりくねっています。</P>
    > <LI>
    > <P>Lync はこれまで以上に、組織全体や世界中の個人とつながる強力なツールです。 Lync Standard CAL Windows Live Messengerユーザー/デバイス ライセンスを追加する必要はありません。 この一覧には Skype フェデレーションが追加され、Lync ユーザーは IM と音声で数億人のユーザーに連絡できます。</P></LI></UL>


    </div></td>
    </tr>
    </tbody>
    </table>


2.  必要な DNS ホスト (A または AAAA for IPv6) および DNS SRV レコードを定義および構成する

3.  Lync Server コントロール パネルを使用するか、Lync Server 管理シェルと適切なコマンドレットを使用して、ポリシーを定義および構成します。 Lync Server 管理シェルコマンドレットの詳細については[、Lync Server 2013](https://docs.microsoft.com/powershell/module/skype/)のフェデレーションと外部アクセスのコマンドレットを参照してください。
    
    <div>
    

    > [!NOTE]  
    > Lync Room System (LRS) には、フェデレーション Lync パートナーの開催者から送信された会議の参加ボタンは表示されません。 LRS に会議参加リンクを表示するには、次のコマンドレットを使用して送信組織が TNEF を有効にする必要があります。<BR><BR><CODE>New-RemoteDomain -DomainName Contoso.com -Name Contoso</CODE><BR><CODE>Set-RemoteDomain -Identity Contoso -TNEFEnabled $true</CODE><BR>これは LRS 固有ではありません。 また、MAPI プロパティが転送されないので、Outlook と Lync ではこの場合は [参加] リンクは表示されませんが、Outlook の場合、ユーザーは会議出席招待を開き、会議の URL をクリックできます。 TNEFEnabled が true Exchange 2013 に設定されている場合、OnlineMeetingExternalLink を含む MAPI プロパティは削除されません。アラームに [参加] ボタンが表示されます。

    
    </div>

</div>

<div>

## <a name="see-also"></a>関連項目


[Lync Server 2013 での SIP、XMPP フェデレーション、パブリック インスタント メッセージングの計画](lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md)  
[Lync Server 2013 へのフェデレーションおよび外部アクセスの管理](lync-server-2013-managing-federation-and-external-access-to-lync-server-2013.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

