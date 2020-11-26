---
title: 'Lync Server 2013: データベースのセキュリティ強化および保護'
description: 'Lync Server 2013: データベースのセキュリティを強化し、保護します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hardening and protecting the databases of Lync Server 2013
ms:assetid: 6953e721-3511-4235-b848-51bab093dc89
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn518330(v=OCS.15)
ms:contentKeyID: 62625490
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: af1ed8f54384e8ecac3b1e4ce6a4253a10bcc2c6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427762"
---
# <a name="hardening-and-protecting-the-databases-of-lync-server-2013"></a>Lync Server 2013 のデータベースのセキュリティ強化および保護

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2013-12-05_

Microsoft Lync Server 2013 は、ユーザー情報、会議の状態、アーカイブデータ、および通話詳細レコード (CDRs) を保存するための SQL Server データベースにも依存しています。 Lync server 2013 データを Lync Server のバックエンドデータベースで最大限に活用するには、フォールトトレランスを向上させてトラブルシューティングを簡素化する方法でアプリケーションデータを区分することができます。 これらの目標を達成するには、次の方法でアプリケーションデータをパーティションに分割します。

  - **サーバーのパーティション分割のベストプラクティスを使用する**   オペレーティングシステムファイル、アプリケーションファイル、プログラムファイルをデータファイルから分離します。

  - **トランザクションログファイルとデータベースファイルを保存**   する  フォールトトレランスを強化して回復を最適化し、暗号化されたディスクまたはボリュームに保存するには、これらのファイルを個別に保存します。

  - **サーバークラスタリングの使用**   バックエンドサーバーをクラスター化して、Lync Server 2013 システムの可用性を最適化します。

  - **すべてのデータバックアップが暗号化され、適切に処理されるようにする**   紛失、廃棄、または紛失したバックアップメディアが、Lync Server 2013 展開のデータセキュリティに大きな脅威をもたらす可能性がある

Standard Edition server 以外の Lync Server 2013 サーバーでは、SQL Server Express インスタンス (RTCLOCAL インスタンス) にリモートからアクセスすることはできません。また、Standard Edition サーバー上の SQL Server Express を除き、ローカルのファイアウォール例外は作成されません。 Standard Edition サーバーでは、バックエンドデータベースと中央管理ストア (CMS) の両方が、リモートでアクセスできるように設定されています。 SQL Server データベースを強化するには、次の操作を行います。

  - Standard Edition サーバーの SQL Server Express ファイアウォールをカスタマイズして、データベースにリモートアクセスできるサーバーの範囲を制限します。 既定では、すべての IP アドレスでデータベースにリモートアクセスできます。

  - Sql server 構成マネージャーを使用して、SQL Server リモートアクセスのプロトコル、IP アドレス、ポートを指定します。
    
      - Lync Server 2013 は、TCP/IP プロトコルを使います。 IP バージョン 4 (IPv4) をサポートしますが、IP バージョン 6 (IPv6) ではサポートされません。
        
        <div>
        

        > [!NOTE]  
        > Lync Server 2013 は、デュアル IP スタックが有効になっているネットワークで機能することができます。

        
        </div>
    
      - Lync Server 2013 は複数の IP アドレス (マルチホームネットワークのアドレスカード) をサポートしています。 SQL Server が特定の IP アドレス (個別のアドレスまたはサブネット) のみをリッスンするように指定し、特定のプロトコルのみを使用するように指定することができます。
    
      - Lync Server 2013 は、静的および動的な SQL Server のポートをサポートしています。

  - 静的な (既定以外の) ポートで SQL Server を実行します。 SQL Server Browser は実行しないでください (クライアントにリスニングポートを報告することはできません)。 これには、フロントエンドサーバー、監視サーバー、アーカイブサーバー、管理コンソール (Lync Server 管理シェル、Lync Server コントロールパネル、またはトポロジビルダーを実行する)、および Lync Server データベースを実行している他のすべてのサーバーを含む、各 SQL Server クライアントのカスタム構成が必要です。

<div>


> [!NOTE]  
> データベースへのアクセスは、信頼できるデータベース管理者に制限されている必要があります。 悪意のあるデータベース管理者が、Lync server 2013 サーバーに対する直接のアクセスや管理を許可されていない場合でも、データベースにデータを挿入または変更して、Lync Server 2013 サーバー経由の権限を取得したり、サービスから機密情報を取得したりすることができます。



</div>

カスタム構成と SQL Server データベースの強化の詳細については、「NextHop ブログの記事「カスタム SQL Server ネットワーク構成での Lync Server 2010 の使用」を参照してください [https://go.microsoft.com/fwlink/p/?LinkId=214008](https://go.microsoft.com/fwlink/p/?linkid=214008) 。

<div>


> [!NOTE]  
> オペレーティングシステムやアプリケーションサーバーを強化することもできます。また、グループポリシーを使用して、Lync Server の展開にセキュリティ lockdowns を実装することもできます。 詳細については、「 <A href="lync-server-2013-hardening-and-protecting-servers-and-applications.md">Lync Server 2013 用のサーバーとアプリケーションの強化と保護</A>」を参照してください。



</div>

</div>

<span> </span>

</div>

</div>

</div>

