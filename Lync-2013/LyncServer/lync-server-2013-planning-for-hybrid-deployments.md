---
title: 'Lync Server 2013: ハイブリッド展開の計画'
description: 'Lync Server 2013: ハイブリッド展開の計画。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for hybrid deployments
ms:assetid: f8b3d240-bc2e-42c9-acf8-d532d641a14c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205403(v=OCS.15)
ms:contentKeyID: 48185910
ms.date: 05/25/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 919f6058059fc9bfcb6bcb4f4c38140e53be6274
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424549"
---
# <a name="planning-for-lync-server-2013-hybrid-deployments"></a>Lync Server 2013 のハイブリッド展開の計画

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**トピック最終更新日:** 2016-05-25_

ハイブリッド展開を計画する際には、ユーザーとネットワーク インフラストラクチャに対して次の要件を考慮する必要があります。

<div>

## <a name="infrastructure-requirements"></a>インフラストラクチャ要件

ハイブリッド展開を実装して展開するには、環境で次を構成する必要があります。

  - Skype for Business Online が有効になっている microsoft 365 または Office 365 組織。 オンプレミス展開では、ハイブリッド構成に 1 つのテナントのみを使用できます。

  - サポートされているトポロジに展開される、Skype for Business Server または Lync Server の 1 つのオンプレミス展開 (インフラストラクチャ)。 トポロジ要件を参照してください。
    
    ハイブリッド用に Lync Server 2013 または Lync Server 2010 展開を構成する方法については [、「Lync Server 2013](lync-server-2013-configuring-hybrid-deployments.md)ハイブリッド展開の構成」を参照してください。

  - Skype for Business Server 2015 管理ツール。 Lync Server 2013 または Lync Server 2010 を使用している場合は、Lync Server 2013 管理ツールを使用できます。

  - Microsoft 365 または Office 365 でシングル サインオンをサポートし、ユーザーがオンプレミスと同じログイン資格情報を使用して Office にサインインするには、Azure Active Directory (AAD) Connect のパスワード同期機能を使用できます。 また、Microsoft 365 または AD 365 でのシングル サインオンに Active Directory フェデレーション サービス (Office FS) を使用できます。
    
    詳細については、「オンプレミス ID と Azure Active Directory の統合」 [を参照してください](https://go.microsoft.com/fwlink/p/?linkid=619754)。

  - オンプレミスとオンラインの Active Directory オブジェクトの同期を維持する単一のディレクトリ同期ソリューション。 ディレクトリ同期の詳細については、「ディレクトリ統合ツール [」を参照してください](https://go.microsoft.com/fwlink/p/?linkid=530320)。

</div>

<div>

## <a name="lync-client-support"></a>Lync クライアント サポート

Lync クライアントでサポートされる機能と、オンプレミスとオンライン環境で使用できる機能にはいくつかの違いがあります。 組織のユーザーをホームする場所を決定する前に、Lync Server のさまざまな構成に対するクライアント サポートを表示できます。 Lync ハイブリッド展開では、次のクライアントが Skype for Business Online でサポートされています。

  - Lync 2010

  - Lync 2013

  - Lync Windows ストア アプリ

  - Lync Web App

  - Lync Mobile

  - Lync for Mac 2011

  - Lync Room System

  - Lync Basic 2013

クライアント サポートの詳細については、次のトピックを参照してください。

  - [Lync Online のクライアント](https://go.microsoft.com/fwlink/?linkid=281902)

  - [Lync Server 2013 のクライアントの比較表](lync-server-2013-desktop-client-comparison-tables.md)

  - [Lync Server 2013 のモバイル クライアントの比較表](lync-server-2013-mobile-client-comparison-tables.md)

</div>

<span id="BKMK_Topology"></span>

<div>

## <a name="topology-requirements"></a>トポロジ要件

Skype for Business Online とのハイブリッド展開を構成するには、次のいずれかのトポロジがサポートされている必要があります。

  - Skype for Business Server 2015 を実行しているすべてのサーバーを含む Skype for Business Server 2015 展開。

  - Lync Server 2013 を実行しているすべてのサーバーを含む Lync Server 2013 展開。

  - Lync Server 2010 の展開では、Lync Server 2010 を実行しているすべてのサーバーに最新の累積的な更新プログラムが適用されます。
    
      - フェデレーション エッジ サーバーとフェデレーション エッジ サーバーからの次のホップ サーバーは、最新の累積的な更新プログラムを使用して Lync Server 2010 を実行している必要があります。
    
      - Skype for Business Server 2015 または Lync Server 2013 管理ツールは、少なくとも 1 つのサーバーまたは管理ワークステーションにインストールする必要があります。

  - Skype for Business Server 2015 を実行している少なくとも 1 つのサイトで、次のサーバーの役割を持つ Lync Server 2013 と Skype for Business Server 2015 の複合展開。
    
      - 少なくとも 1 台のエンタープライズ プールまたは Standard Edition サーバー 
    
      - SIP フェデレーションに関連づけられたディレクター プール (もしあれば)
    
      - SIP フェデレーションに関連づけられたエッジ プール (もしあれば)

  - Lync Server 2010 と Skype for Business Server 2015 の混在展開。次のサーバーは、Skype for Business Server 2015 を実行している少なくとも 1 つのサイトで役割を果たします。
    
      - 少なくとも 1 台のエンタープライズ プールまたは Standard Edition サーバー 
    
      - SIP フェデレーションに関連づけられたディレクター プール (もしあれば)
    
      - サイトの SIP フェデレーションに関連づけられたエッジ プール

  - Lync Server 2013 を実行している少なくとも 1 つのサイトで、次のサーバーの役割を持つ Lync Server 2010 と Lync Server 2013 の複合展開。
    
      - サイトの少なくとも 1 台のエンタープライズ プールまたは Standard Edition サーバー
    
      - SIP フェデレーションに関連づけられたディレクター プール (もしサイトにあれば)
    
      - サイトの SIP フェデレーションに関連づけられたエッジ プール

<div>


> [!IMPORTANT]  
> オンプレミスと UNRESOLVED_TOKEN_VAL (skypeforbusiness) Online の間のユーザー移動を含むすべてのユーザー管理は、インストールされている最新バージョンの管理ツールを使用して行う必要があります。 管理ツールは、既存のオンプレミス展開とインターネットに接続できる別のサーバーにインストールする必要があります。 オンプレミス展開から UNRESOLVED_TOKEN_VAL(skype16_online) にユーザーを移動する <A href="https://docs.microsoft.com/powershell/module/skype/Move-CsUser">Move-CsUser</A> コマンドレットは、オンプレミス展開に接続されている管理ツールから実行する必要があります。



</div>

サポートされるトポロジの詳細については [、「Lync Server 2013](lync-server-2013-supported-topologies.md)でサポートされるトポロジ」および [「Lync Server 2013](https://go.microsoft.com/fwlink/p/?linkid=398709)リファレンス: エンタープライズ ハイブリッド展開用トポロジ」を参照してください。

ハイブリッド展開に関するトラブルシューティング情報と、PowerShell を Lync Online に接続する方法については [、「Lync Online: Lync PowerShell](https://go.microsoft.com/fwlink/p/?linkid=306718)およびハイブリッド トラブルシューティング」を参照してください。

</div>

<div>

## <a name="requirements-for-federation-allowedblocked-lists"></a>フェデレーション許可/ブロックリストの要件

許可ドメインの一覧には、パートナー エッジの完全修飾ドメイン名 (FQDN) が構成されているドメインが含まれます。これらは *許可パートナー サーバー* または *ダイレクト フェデレーション パートナー* と呼ばれることもあります。オープン フェデレーションとクローズド フェデレーションの違いをよく理解しておくことが必要です。オンプレミス展開ではこれらはそれぞれ *パートナーの検出* および *許可パートナー ドメインの一覧* と呼ばれます。

ハイブリッド展開を正しく構成するには、次の必要条件を満たす必要があります。

  - ドメイン マッチングは、オンプレミス展開と Microsoft 365 または Office 365 組織で同じように構成する必要があります。 オンプレミス展開でパートナーの検出が有効になっている場合、オンライン テナントではオープン フェデレーションを有効にする必要があります。 パートナーの検出が無効になっている場合、オンライン テナントではクローズド フェデレーションを構成する必要があります。

  - オンプレミス展開における禁止ドメインの一覧はオンライン テナントの禁止ドメインの一覧と正確に一致する必要があります。

  - オンプレミス展開における許可ドメインの一覧はオンライン テナントの許可ドメインの一覧と正確に一致する必要があります。

  - Lync Online コントロール パネルを使用して構成される、オンライン テナントの外部通信に対してフェデレーションを有効にする必要があります。

</div>

<div>

## <a name="dns-settings"></a>DNS の設定

ハイブリッド展開用の DNS レコードを作成する場合、すべての Lync 外部 DNS レコードがオンプレミス インフラストラクチャをポイントしている必要があります。 必要な DNS レコードの詳細については [、Lync Server 2013](lync-server-2013-domain-name-system-dns-requirements.md)のドメイン ネーム システム (DNS) の要件を参照してください。

さらに、次の表で説明している DNS 解決が使用しているオンプレミス展開で機能することを確認する必要があります。


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>DNS レコード</p></td>
<td><p>解決方法</p></td>
<td><p>DNS 要件</p></td>
</tr>
<tr class="even">
<td><p>_sipfederationtls._tcp の DNS SRV レコード。 &lt;sipdomain.com エッジの外部 IP に対して解決するサポートされている SIP ドメインすべてについて &gt;</p></td>
<td><p>エッジ サーバー</p></td>
<td><p>ハイブリッド展開でフェデレーション通信を有効にする。オンプレミスとオンラインで分割される SIP ドメイン用のフェデレーション トラフィックのルートをエッジ サーバーで認識している必要があります。</p></td>
</tr>
<tr class="odd">
<td><p>エッジ Web 会議サービス FQDN の DNS A レコード、たとえば、webcon.contoso.com は Web 会議のエッジ外部 IP に解決される</p></td>
<td><p>ユーザーのコンピューターが接続している会社内ネットワーク</p></td>
<td><p>オンライン ユーザーを有効にして、オンプレミスのホストされた会議でのコンテンツを提供または表示する。コンテンツには、PowerPoint ファイル、ホワイトボード、投票、および共有メモがあります。</p></td>
</tr>
</tbody>
</table>


所属する組織での DNS の構成方法によっては、内部 DNS 解決をこれらのレコードに適用するために、対応する SIP ドメインに対して組織内でホストする DNS ゾーンにこれらのレコードを追加する必要があります。

</div>

<div>

## <a name="firewall-considerations"></a>ファイアウォールに関する考慮事項

ネットワーク上のコンピューターは、標準のインターネット DNS 参照を実行できる必要があります。これらのコンピューターが標準のインターネット サイトに接続できれば、ネットワークはこの要件を満たしています。

Microsoft Online Services データ センターの場所によっては、ワイルドカード ドメイン名 (.outlook.com からのトラフィックなど) に基づいて接続を受け入れるネットワーク ファイアウォール デバイスも構成する \* 必要があります。 組織のファイアウォールがワイルドカードを使用した名前の構成方法をサポートしない場合は、許可する IP アドレスの範囲および特定のポートを手動で決める必要があります。

365 の URL [と IP Officeのヘルプ トピックを参照してください](https://go.microsoft.com/fwlink/p/?linkid=252942)。

</div>

<span id="b"></span>

<div>

## <a name="port-and-protocol-requirements"></a>ポートとプロトコルの要件

Lync Server 2013 内部通信のポート要件に加えて、次のポートも構成する必要があります。


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>プロトコル/ポート</th>
<th>アプリケーション</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>TCP 443</p></td>
<td><p>受信を開く</p>
<ul>
<li><p>Active Directory フェデレーション サービス (フェデレーション サーバーの役割)</p>
<p>詳細については、「FS 役割サービス <a href="https://go.microsoft.com/fwlink/p/?linkid=281899">のADを参照してください</a>。</p></li>
<li><p>Active Directory フェデレーション サービス (プロキシ サーバーの役割)</p></li>
<li><p>Microsoft Online Services ポータル</p></li>
<li><p>自分のポータル サイト</p></li>
<li><p>Outlook Web App</p></li>
<li><p>Lync クライアント (オンプレミスの Lync Server から Lync Online への通信)</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>TCP 80 と 443</p></td>
<td><p>受信を開く</p>
<ul>
<li><p>Microsoft Online Services ディレクトリ同期ツール</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>TCP 5061</p></td>
<td><p>エッジ サーバーで受信/送信を開く</p></td>
</tr>
<tr class="even">
<td><p>PSOM/TLS 443</p></td>
<td><p>データ共有セッションの受信/送信を開く</p></td>
</tr>
<tr class="odd">
<td><p>STUN/TCP 443</p></td>
<td><p>音声、ビデオ、アプリケーション共有セッションの受信/送信を開く</p></td>
</tr>
<tr class="even">
<td><p>STUN/UDP 3478</p></td>
<td><p>音声とビデオ セッションの受信/送信を開く</p></td>
</tr>
<tr class="odd">
<td><p>RTP/TCP 50000-59999</p></td>
<td><p>音声セッションとビデオ セッションの送信を開く</p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="user-accounts-and-data"></a>ユーザー アカウントとデータ

Lync Server 2013 のハイブリッド展開では、ユーザー アカウントが Active Directory ドメイン サービスで作成されるので、Lync Online にホームするユーザーは、まずオンプレミス展開で作成する必要があります。 その後、ユーザーを Skype for Business Online に移動すると、ユーザーの連絡先リストが移動されます。

Lync オンプレミスと Lync Online 展開の間でユーザー アカウントを AD FS および Dirsync と同期する場合、ユーザーが Lync Online に移動されていない場合でも、組織内のすべての Lync ユーザーの AD アカウントをオンプレミスとオンラインの Lync 展開の間で同期する必要があります。 すべてのユーザーを同期しない場合、組織のオンプレミス展開のユーザーとオンライン ユーザーとの間の通信が正常に動作しない可能性があります。

<div>


> [!IMPORTANT]  
> ユーザーが Microsoft 365 管理センターのオンライン ポータルを使用して作成された場合、ユーザー アカウントはオンプレミスの Active Directory と同期されません。また、ユーザーはオンプレミスの Active Directory に存在しません。 Lync Online でユーザーを既に作成済みで、オンプレミスの Lync Server とのハイブリッドを構成する場合は、「Lync Online から Lync <A href="lync-server-2013-moving-users-from-lync-online-to-lync-on-premises.md">Server 2013</A>のオンプレミスへのユーザーの移動」を参照してください。



</div>

また、ハイブリッド展開を計画する場合は、次のユーザー関連の問題も考慮する必要があります。

  - **ユーザーの連絡先**   Lync Online ユーザーの連絡先の制限は 250 です。 その数を超えた連絡先は、アカウントが Lync Online に移動されるときにユーザーの連絡先リストから削除されます。

  - **インスタント メッセージングとプレゼンス**   ユーザーの連絡先リスト、グループ、およびアクセス制御リスト (ACL) はユーザー アカウントと一緒に移行されます。

  - **会議データ、会議コンテンツ、スケジュールされた会議**   このコンテンツは、ユーザー アカウントでは移行されません。 ユーザーは、アカウントが Lync Online に移行された後で会議を予約し直す必要があります。

</div>

<div>

## <a name="user-policies-and-features"></a>ユーザー ポリシーと機能

  - Lync Server 2013 ハイブリッド環境では、ユーザーはインスタント メッセージング、音声、会議をオンプレミスまたはオンラインで有効にできますが、両方を同時に有効にすることはできません。

  - **Lync クライアント**    一部のユーザーは、Lync Online に移動するときに新しいクライアント バージョンが必要な場合があります。 Office Communications Server 2007 R2 の場合、Lync Online に移行する前に、ユーザーを Lync Server 2013 プールに移動する必要があります。
    
    クライアント サポートの詳細については [、「Lync Online](https://go.microsoft.com/fwlink/p/?linkid=281902) のクライアントとサポートされる Lync クライアントとネットワーク ポート構成 [」を参照してください](https://go.microsoft.com/fwlink/p/?linkid=281901)。

  - **オンプレミスのポリシーと構成 (ユーザー以外)**   オンライン ポリシーとオンプレミス ポリシーには、個別の構成が必要です。 両方に適用されるグローバル ポリシーを設定することはできません。

</div>

</div>

<span> </span>

</div>

</div>

</div>
