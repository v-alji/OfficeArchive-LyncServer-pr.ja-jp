---
title: 'Lync Server 2013: 外部ユーザー アクセスの展開'
description: 'Lync Server 2013: 外部ユーザーアクセスの展開。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying external user access
ms:assetid: d40c9574-c16b-4fe6-b848-21ae0b7e4f0e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398918(v=OCS.15)
ms:contentKeyID: 48185495
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: af41a169fe3a72e440e95cfa370a16117fb828a6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430008"
---
# <a name="deploying-external-user-access-in-lync-server-2013"></a>Lync Server 2013 での外部ユーザー アクセスの展開

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2013-09-23_

Microsoft Lync Server 2013 の edge コンポーネントを展開することで、組織の内部ネットワークにログインしていない外部ユーザー (認証済みのリモートユーザー、一般向けインスタントメッセージング (IM) サービスのモバイルクライアントとユーザー)、Lync Server を使って組織内の他のユーザーと通信することが可能になります。 Lync Server 2013 の展開と構成のプロセスは、Lync Server 2010 とは大きく異なります。 インストールと管理のためのツールは、Lync Server 2010 とほぼ同じです。

<div>


> [!IMPORTANT]  
> Microsoft Lync Server 2013 &nbsp; Edge server のインストールと構成は、社内のチームとの計画と調整を大量に行う必要があります。これには、セキュリティ、ネットワーク、ファイアウォール、ドメインネームシステム (DNS)、ロードバランサー、および公開キー基盤 (PKI) に関する考慮事項が含まれます。 外部アクセスコンポーネントを展開する前に、記載されている計画プロセスとドキュメントを確認して使用することを強くお勧めします。 これにより、展開プロセスを実行するときに、不要な変更や問題の数と頻度を制限することができます。 外部ユーザーアクセスの計画については、「 <A href="lync-server-2013-planning-for-external-user-access.md">Lync Server 2013 での外部ユーザーアクセスの計画</A>」を参照してください。



</div>

<div>

## <a name="in-this-section"></a>このセクション中

  - [Lync Server 2013 の外部ユーザー アクセスの展開チェックリスト](lync-server-2013-deployment-checklist-for-external-user-access.md)

  - [Lync Server 2013 の外部ユーザー アクセス コンポーネントのシステム要件](lync-server-2013-system-requirements-for-external-user-access-components.md)

  - [Lync Server 2013 の境界ネットワークへのサーバーのインストールの準備](lync-server-2013-preparing-for-installation-of-servers-in-the-perimeter-network.md)

  - [Lync Server 2013 でのエッジおよびディレクターのトポロジの作成](lync-server-2013-building-an-edge-and-director-topology.md)

  - [Lync Server 2013 でのディレクターの](lync-server-2013-setting-up-the-director.md) セットアップ (オプション)

  - [Lync Server 2013 でのエッジ サーバーの設定](lync-server-2013-setting-up-edge-servers.md)

  - [Lync Server 2013 のリバース プロキシ サーバーの設定](lync-server-2013-setting-up-reverse-proxy-servers.md)

  - [Lync Server 2013 での外部ユーザー アクセスのサポートの構成](lync-server-2013-configuring-support-for-external-user-access.md)

  - [Lync Server 2013 での Lync と Skype の接続のプロビジョニング ガイド](lync-server-2013-provisioning-guide-for-lync-skype-connectivity.md)

  - [Lync Server 2013 での SIP フェデレーション、XMPP フェデレーションおよびパブリック インスタント メッセージングの構成](lync-server-2013-configuring-sip-federation-xmpp-federation-and-public-instant-messaging.md)

  - [Lync Server 2013 でのモビリティの展開](lync-server-2013-deploying-mobility.md)

  - [Lync Server 2013 でのエッジの展開の検証](lync-server-2013-verifying-your-edge-deployment.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

