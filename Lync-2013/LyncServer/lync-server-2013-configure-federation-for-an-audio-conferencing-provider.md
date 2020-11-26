---
title: 'Lync Server 2013: 電話会議プロバイダー用にフェデレーションを構成する'
description: 'Lync Server 2013: 電話会議プロバイダー用のフェデレーションを構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure federation for an audio conferencing provider
ms:assetid: 08dedcce-0d3f-45da-8282-cf2634a41665
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn510996(v=OCS.15)
ms:contentKeyID: 60595883
ms.date: 07/24/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c74654224c42618768d881a95031d58be4d55df5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434054"
---
# <a name="configure-federation-for-an-audio-conferencing-provider-in-lync-server-2013"></a>Lync Server 2013 で電話会議プロバイダーのフェデレーションを構成する

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2014-07-24_

ハイブリッド展開で電話会議プロバイダー (ACP) を使用する場合 (lync Online でオンプレミスの lync Server を使用する場合)、オンプレミスの Lync 展開と ACP パートナーとの間のフェデレーションを許可パートナーサーバーとして構成する必要があります。 フェデレーションは、ACP パートナー ドメインとエッジ サーバー (アクセス プロキシとも呼ばれます) をオンプレミス展開のフェデレーション ドメイン リストに追加すると設定できます。 その後、APC パートナーは、オンプレミスのエッジ サーバー プールの FQDN を、許可されるフェデレーション ドメイン リストに追加する必要があります。 ACP プロバイダーにお問い合わせください。詳細については、ACP パートナーが、許可されているフェデレーションドメインリストにオンプレミスエッジサーバープールの FQDN を追加する必要があります。

  - **許可されるフェデレーション ドメインとしての ACP ドメインおよびエッジ サーバーの追加**
    
    許可されたパートナーサーバー (許可されたフェデレーションドメイン) として ACP ドメインを追加するには、「 [Lync server 2013 で許可されている外部ドメインのサポートを構成](lync-server-2013-configure-support-for-allowed-external-domains.md)する」の手順に従います。 エッジ サーバーには、ACP パートナーのエッジ サーバーの FQDN を追加します。 ACP からもアクセス プロキシとして参照される可能性があるエッジ サーバーの FQDN を取得するには ACP パートナーへの問い合わせが必要になる場合があります。

  - **ACP パートナーへのエッジ サーバー プールの FQDN の指定**
    
    ACP パートナーは、フェデレーションを構成してオンプレミスのドメインを許可されるパートナー サーバーとして追加する必要があります。そのためには、エッジ サーバー プールの FQDN を許可されるフェデレーション ドメインとして追加します。

</div>

<span> </span>

</div>

</div>

</div>

