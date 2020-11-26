---
title: 'Lync Server 2013: 必要に応じてタスク'
description: 'Lync Server 2013: 必要に応じてタスクを実行します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: As-needed tasks
ms:assetid: b66bc6fe-f138-4cf4-ba7f-aee9a3e0497e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn722431(v=OCS.15)
ms:contentKeyID: 63969643
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 91fe249d9615bb619426c58b22606c3ef182f9a7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440550"
---
# <a name="as-needed-tasks-in-lync-server-2013"></a>Lync Server 2013 での必要なタスク

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2014-08-18_

必要に応じて、次のタスクを実行します。 通常、標準の手順でもカバーされています。

  - * * 完全なセキュリティ監査 * * この監査は、メッセージングシステムのアップグレードまたは再設計、または試みた (または成功した) セキュリティ侵害に対応して、定期的に行うことができます。 この手順では、サーバーやファイアウォールでのポートスキャン、セキュリティ修正プログラムの監査、サードパーティのペネトレーションテストなどを行うことができます。

  - **証明書を期限切れに置き換える**   Lync Server の証明書を確認することは、通常の週間タスクの1つであり、管理者はすべての証明書の有効期限を記録する必要があります。 このレコードを使用すると、特定の証明書が期限切れになり、必要に応じて置き換えられるときに、管理者が通知を作成できます。

  - **パフォーマンスベースラインの更新**   アップグレードまたは構成を変更した後で、パフォーマンスのベースラインを更新します。 組織では、ベースラインを使用してパフォーマンスの変化を測定し、システムのパフォーマンスに影響する問題を検出することができます。

  - **エンタープライズプールの管理**   エンタープライズプール、標準エディションサーバー、および組織内の他のすべてのサーバーの初期構成は、個々のサーバーの展開中に実行されました。 Standard Edition server とエンタープライズプールの展開後のサーバーとプールの管理には、次のタスクが含まれます。
    
      - フロントエンドサーバーの管理
    
      - Web 会議を管理する
    
      - 会議を管理する
    
      - サービスアカウントの資格情報を変更する
    
      - データベースの管理
    
      - サービスを開始および停止し、サーバーの役割を非アクティブ化する
    
      - サーバーとサーバーの役割の削除、プールの削除、サーバーとプールの無効化

  - **利用状況の管理**   Lync Server 2013 を構成して、組織に最も適した機能を提供できます。 これには、次のポリシーが含まれます。
    
      - オンプレミスの Web 会議会議のサポートを管理する
    
      - インスタントメッセージを送信するための配布グループの使用を管理する
    
      - 連絡先、プレゼンス、およびクエリを管理する
    
      - クライアントのバージョンのフィルター処理を構成する
    
      - インテリジェント IM フィルターの設定
    
      - アーカイブ、通話の詳細の記録、会議のコンプライアンスを構成する

  - **エッジサーバーの接続の管理**   外部接続を提供するために必要なサーバーと設定の継続的な管理には、次のものが含まれます。
    
      - 内部サーバーとエッジサーバー間の接続の管理
    
      - エッジサーバーの内部および外部インターフェイスと証明書の構成
    
      - フェデレーションパートナーへのアクセスを管理する

  - **アドレス帳の管理**   アドレス帳サーバーの管理には次のものが含まれます。
    
      - アドレス帳のサーバー電話の正規化を構成する
    
      - コマンドラインからアドレス帳サーバーを管理する

  - **ユーザーアカウントを管理する**   ユーザーアカウントの管理には次のものが含まれます。
    
      - Lync Server のユーザーアカウントを有効にする
    
      - ウィザードを使用して Lync Server ユーザーを構成する
    
      - Lync Server の個々のユーザーアカウントのプロパティを構成する
    
      - Lync Server ユーザーを検索する
    
      - Lync Server ユーザーを移動する
    
      - Lync Server ユーザーを削除する

  - **Lync Server 2013 ログファイルを分析**   する  トラブルシューティングで一般的に使用される便利なツールの1つは、「lync server [2013 ログツールの使用](https://technet.microsoft.com/library/gg558599.aspx)について詳しく説明されている lync Server 2013 ログツール」です。

ログツールによって (サーバーごとに) ログファイルが生成されるため、Microsoft Office Server 12 リソースキットツールがコンピューターにインストールされている場合は、Snooper ツールを使用してこれらのログファイルを表示および分析することができます。 そうしないと、ログもテキストエディターを使って分析することができます。これは、Snooper ユーティリティを使用する場合よりも透明で、より複雑なものになります。

プロトコルメッセージの表示と分析を行うには

ログツールで、デバッグセッションを終了したら、[ログファイルの分析] をクリックし、Snooper ツールを使用してログファイルを表示します。 次のコンポーネントのプロトコルログを分析できます。

  - Lync Server SipStack (SIP)

  - Lync Server S4 (SIP)

  - MCU インフラストラクチャ C3P とフォーカス C3P を含む Lync Server 会議のシグナリングトラフィック (C3P)

  - Lync Server Web 会議トラフィック (PSOM)

  - Lync Server ユニファイドコミュニケーションクライアントプラットフォームクライアント (UCCP)

  - アーカイブデータベースからのエラーレポート

必要なタスクのパフォーマンスを整理するには、「As-Needed の操作チェックリスト」を参照してください。

<div>


> [!IMPORTANT]  
> 詳細な管理手順と管理手順については、「Microsoft Lync Server 2013 管理者ガイド」を参照してください。



</div>

<div>

## <a name="backup-and-restore-policies-or-configuration-settings"></a>バックアップ (および復元) ポリシーまたは構成設定

Lync Server 2013 を使用すると、システム全体のバックアップと復元を行うことができます。 1つのポリシーまたは構成設定の単一のコレクションをバックアップして、適切なポリシーを取得し、そのオブジェクトを Export-Clixml コマンドレットにパイプして、ポリシー情報を XML ファイルとして保存します。

`Get-CsClientPolicy -Identity "RedmondClientPolicy" | Export-Clixml -Path C:\Backup\RedmondClientPolicy.xml`

これで、RedmondClientPolicy を試して、設定を変更することができます。 以前のポリシーを復元する場合は、次のように入力します。

`$x = Import-Clixml -Path C:\Backup\RedmondClientPolicy.xml`

`Set-CsClientPolicy -Instance $x`

この方法はほとんどのポリシーと設定で動作しますが、より複雑な項目 (ルーティング構成設定など、複数の異なる音声ルートを含むアイテム) では動作しません。

</div>

</div>

<span> </span>

</div>

</div>

</div>

