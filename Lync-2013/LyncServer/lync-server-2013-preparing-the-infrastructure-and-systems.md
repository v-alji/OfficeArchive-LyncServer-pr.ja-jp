---
title: 'Lync Server 2013: インフラストラクチャとシステムの準備'
description: 'Lync Server 2013: インフラストラクチャとシステムの準備を行います。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing the infrastructure and systems
ms:assetid: 1254ee38-0679-4714-b293-1050f107c158
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398205(v=OCS.15)
ms:contentKeyID: 48183458
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bfabdda9d117af1534578c8543f9ce72808d5a53
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424101"
---
# <a name="preparing-the-infrastructure-and-systems-for-lync-server-2013"></a>Lync Server 2013 のインフラストラクチャとシステムの準備

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2013-02-21_

Lync Server 2013 を展開するには、トポロジの設計を定義して公開するために、トポロジビルダーを使用する必要があります。 トポロジに必要なコンポーネントを特定するには、トポロジビルダーを使用してトポロジの設計を作成し、保存します。 トポロジビルダーでトポロジを公開する前に、次の操作を行います。

  - 必要なすべてのコンピューター (必要に応じて、Lync Server 2013、データベースサーバー、インターネットインフォメーションサービス (IIS) を実行しているサーバー)、ネットワークアダプター、ハードウェアロードバランサー、ストレージデバイス (ファイルサーバーなど) など、トポロジ設計の各コンポーネントのハードウェアを入手してインストールします。 展開に必要なコンポーネントを指定するトポロジの定義方法について詳しくは、「 [Lync Server 2013 でトポロジを定義して構成](lync-server-2013-defining-and-configuring-the-topology.md)する」をご覧ください。 サーバーのハードウェア要件の詳細については、サポートされているドキュメントで「 [Lync Server 2013 に](lync-server-2013-supported-hardware.md) 対応したハードウェア」を参照してください。

  - ネットワークインフラストラクチャが要件を満たしていることを確認します。 詳細については、計画ドキュメントの「 [Lync Server 2013 のネットワークインフラストラクチャ要件](lync-server-2013-network-infrastructure-requirements.md) 」を参照してください。

  - Active Directory ドメインサービスをセットアップします。 トポロジを公開して有効にするには、内部サーバーを AD DS のコンピューターアカウントで表す必要があります。 これは、コンピューターを AD DS に結合することで実現されます。 AD DS の準備の詳細については、「 [Lync Server 2013 用の Active Directory ドメインサービスの準備](lync-server-2013-preparing-active-directory-domain-services.md)」を参照してください。

  - ファイル共有を作成します。 Standard Edition サーバーは、必要なファイルのファイル共有をホストできますが、エンタープライズ展開では、ファイル共有をフロントエンドサーバーでホストすることはできません。 フォルダーおよび共有に対してアクセス制御リスト (ACL) を展開して設定するために必要なアクセス許可とグループメンバーシップは、トポロジビルダーが正常に完了するために適切に設定されている必要があります。 Topology Builder を実行しているユーザーには、次の権限とグループメンバーシップがあることを確認する必要があります。
    
      - ローカル管理者のメンバー
    
      - ドメインユーザーのメンバー
    
      - ファイルストアの共有とフォルダーのフルコントロール

  - Enterprise Edition の場合、SQL Server をインストールして構成します。 SQL Server のセットアップを完了するには、SQL Server ベースのサーバーがオンラインであり、トポロジを発行したユーザーが sql Server のローカル管理者であり、sql server インスタンスの SQL Server sysadmin グループのメンバーである必要があります。

このトピックで説明したすべての準備作業を完了した後で、トポロジを公開する前に、Windows オペレーティングシステムやその他の必須ソフトウェアのインストール、IIS のセットアップ、DNS の構成など、その他の準備作業も実行する必要があります。 これらのタスクの詳細については、「 [Lync server 2013 を実行しているサーバーのシステム要件](lync-server-2013-system-requirements-for-servers-running-lync-server-2013.md)」を参照してください。「lync [server 2013 用に IIS を構成する](lync-server-2013-configure-iis.md)」および「 [lync server 2013 用のインフラストラクチャとシステムの準備](lync-server-2013-preparing-the-infrastructure-and-systems.md)」を参照してください。 さらに、クライアントとクライアントの要件について理解しておく必要があります。 詳細については、「 [Lync Server 2013 でのクライアントとデバイスの展開](lync-server-2013-deploying-clients-and-devices.md)」を参照してください。

<div>

## <a name="in-this-section"></a>このセクション中

  - [Lync Server 2013 のハードウェアのセットアップ](lync-server-2013-hardware-setup.md)

  - [Lync Server 2013 のソフトウェアのセットアップ](lync-server-2013-software-setup.md)

  - [Lync Server 2013 用の Active Directory ドメイン サービスの準備](lync-server-2013-preparing-active-directory-domain-services.md)

  - [Lync Server 2013 用 SQL Server の構成](lync-server-2013-configure-sql-server-for-lync-server.md)

  - [Lync Server 2013 でのフロント エンド プールまたは Standard Edition サーバー用の DNS レコードの構成](lync-server-2013-configure-dns-records-for-a-front-end-pool-or-standard-edition-server.md)

  - [Lync Server 2013 管理ツールをインストールする](lync-server-2013-install-lync-server-administrative-tools.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

