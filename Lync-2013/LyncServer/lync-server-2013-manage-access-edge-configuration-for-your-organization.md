---
title: 'Lync Server 2013: 組織のアクセス エッジ構成の管理'
description: 'Lync Server 2013: 組織のアクセスエッジ構成を管理します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Manage Access Edge Configuration for your organization
ms:assetid: 0145eb08-984f-4ecd-bf9c-364817619c2a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ552443(v=OCS.15)
ms:contentKeyID: 48679555
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2161385f9c03f025bcf6f5e599b7e0276f6d592c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426138"
---
# <a name="manage-access-edge-configuration-for-your-organization-in-lync-server-2013"></a>Lync Server 2013 での組織のアクセス エッジ構成の管理

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-11-01_

このドキュメントは暫定版であり、変更される可能性があります。 空白のトピックがプレースホルダーとして含まれています。

1つ以上のエッジサーバーを展開した後、組織でサポートされているエッジサーバー経由での会議への外部ドメインまたはプロバイダーアクセス、リモートユーザーアクセス、匿名ユーザーアクセスの種類を有効にする必要があります。

これらのオプションには、[ **アクセスエッジ構成** ] ページから構成できる次の種類のアクセスがあります。

  - **フェデレーションとパブリック IM 接続を有効にする**   フェデレーションパートナードメインへのユーザーアクセスをサポートする場合は、この機能を有効にします。 この設定は、[ **外部アクセスポリシー** ] ページのグローバル、サイト、またはユーザーのスコープに対して構成される SIP フェデレーションと xmpp フェデレーションの両方に適用されます。 フェデレーション設定を適用するには、両方のページでフェデレーションのサポートを構成する必要があります。
    
    フェデレーションパートナーの検出方法に関するオプションの設定である2つのオプション、およびアーカイブの免責事項 (展開によって通信しているフェデレーション連絡先に通知を送信し、通信の詳細がアーカイブされていることを示す) が連絡先に送信されるかどうかを確認します。
    
      - **パートナードメインの検出を有効にする**   このオプションを選択すると、フェデレーションできるドメインの自動検出が有効になります。 Lync Server 2013 は、ドメインネームシステム (DNS) レコードを使用して、[許可したドメイン] 一覧にないドメインを検出し、検出されたフェデレーションパートナーから受信トラフィックを自動的に評価し、信頼レベル、トラフィック量、および管理者設定に基づいてトラフィックを制限またはブロックします。 このオプションが選択されていない場合、フェデレーションされたユーザーのアクセス許可は、[許可したドメイン] リストに含めるドメイン内のユーザーに対してのみ有効になります。 このオプションが選択されているかどうかにかかわらず、フェデレーションドメインでアクセスエッジサービスを実行している特定のサーバーへのアクセスを制限するなど、個々のドメインをブロックまたは許可するように指定することができます。 詳細については、「 [Lync Server 2013 で許可されている外部ドメインのサポートを構成する](lync-server-2013-configure-support-for-allowed-external-domains.md)」を参照してください。
    
      - **フェデレーションパートナーにアーカイブの免責事項を送信する**   このオプションをオンにすると、フェデレーションパートナーにアーカイブの免責事項のメッセージを送信することができます。これにより、コミュニケーションの詳細が記録されます。 フェデレーションパートナードメインとの外部通信をアーカイブする場合は、アーカイブの免責事項の通知を有効にして、展開によってメッセージと通信の詳細がアーカイブされていることをパートナーに警告する必要があります。 アーカイブの詳細については、「 [Lync Server 2013 でアーカイブするための要件を定義](lync-server-2013-defining-your-requirements-for-archiving.md)する」を参照してください。

  - **リモートユーザーアクセスを有効にする**   出張中の在宅勤務者やユーザーなど、組織内のユーザーが Lync Server に接続できるようにする場合は、このオプションを有効にします。 詳細については、「 [Lync Server 2013 でリモートユーザーアクセスを有効または無効](lync-server-2013-enable-or-disable-remote-user-access.md)にする」を参照してください。

  - **匿名ユーザーによる会議へのアクセスを有効にする**   内部ユーザーが、自分が開催する会議に外部匿名ユーザーを招待する場合は、このオプションを有効にします。 この設定を有効にすると、会議の匿名ユーザーのみを許可します。 会議のエクスペリエンスと、ユーザーが会議で何を行うことができるかを定義するオプションと、匿名ユーザーを含めるためのオプションについては、「 [サイトまたはユーザーの会議ユーザーエクスペリエンスを作成または変更](https://technet.microsoft.com/library/gg429715\(v=ocs.15\)) する」および「 [Lync Server 2013 用の会議ポリシー設定リファレンス](lync-server-2013-conferencing-policy-settings-reference.md)」を参照してください。

<div>


> [!NOTE]  
> 外部ユーザーアクセスのサポートを有効にするだけでなく、組織でのリモートユーザーアクセスの使用を制御するポリシーも構成して、ユーザーが外部ユーザーアクセスの種類を利用できるようにする必要があります。 外部ユーザーアクセスのポリシーの作成、構成、適用の詳細については、「 <A href="lync-server-2013-manage-external-access-policy-for-your-organization.md">Lync Server 2013 で外部アクセスポリシーを管理</A>する」を参照してください。



</div>

**Windows PowerShell コマンドレットを使用してアクセスエッジ構成情報を表示する**

  - Access Edge の構成情報は、Windows PowerShell と **CsAccessEdgeConfiguration** コマンドレットを使用して表示できます。 このコマンドレットは、Lync Server 2013 管理シェルまたは Windows PowerShell のリモート セッションから実行できます。 リモートの Windows PowerShell を使用して Lync Server に接続する方法について詳しくは、Lync Server Windows PowerShell のブログ記事「Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell (クイックスタート: リモート PowerShell を使用した Microsoft Lync Server 2010 の管理)」を[https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876)で参照してください。
    
    すべてのアクセスエッジの構成設定に関する情報を表示するには、Lync Server 管理シェルで次のコマンドを入力し、enter キーを押します。
    
        Get-CsAccessEdgeConfiguration
    
    次のような情報が表示されます。
    
        Identity                               : Global
        AllowAnonymousUsers                    : False
        AllowFederatedUsers                    : False
        AllowOutsideUsers                      : True
        BeClearingHouse                        : False
        EnablePartnerDiscovery                 : False
        EnableArchivingDisclaimer              : False
        EnableUserReplicator                   : True
        KeepCrlsUpToDateForPeers               : True
        MarkSourceVerifiableOnOutgoingMessages : True
        OutgoingTlsCountForFederatedPartners   : 4
        DiscoveredPartnerStandardRate          : 20
        EnableDiscoveredPartnerContactsLimit   : True
        MaxContactsPerDiscoveredPartner        : 1000
        DiscoveredPartnerReportPeriodMinutes   : 60
        MaxAcceptedCertificatesStored          : 1000
        MaxRejectedCertificatesStored          : 500
        CertificatesDeletedPercentage          : 20
        RoutingMethod                          : UseDnsSrvRouting

<div>

## <a name="in-this-section"></a>このセクション中

  - [Lync Server 2013 でのフェデレーションおよびパブリック IM 接続の有効化または無効化](lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md)

  - [Lync Server 2013 でのフェデレーション パートナーの検出の有効化または無効化](lync-server-2013-enable-or-disable-discovery-of-federation-partners.md)

  - [Lync Server 2013 でのフェデレーション パートナーに対するアーカイブ免責事項の送信の有効化または無効化](lync-server-2013-enable-or-disable-sending-an-archiving-disclaimer-to-federated-partners.md)

  - [Lync Server 2013 でのリモート ユーザー アクセスの有効化または無効化](lync-server-2013-enable-or-disable-remote-user-access.md)

  - [Lync Server 2013 匿名ユーザー アクセスの有効化または無効化](lync-server-2013-enable-or-disable-anonymous-user-access.md)

  - [Lync Server 2013 での匿名ユーザー サポートのための会議ポリシーの割り当て](lync-server-2013-assign-conferencing-policies-to-support-anonymous-users.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

