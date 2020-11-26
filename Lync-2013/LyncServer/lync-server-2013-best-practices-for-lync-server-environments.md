---
title: 'Lync Server 2013: Lync Server 環境のベストプラクティス'
description: 'Lync Server 2013: Lync Server 環境のベストプラクティス'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Best practices for Lync Server environments
ms:assetid: b0e45d84-09c8-4d3e-aad0-bc6f34ce233b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720348(v=OCS.15)
ms:contentKeyID: 63969642
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ae6c02621bd6506d2a1d379aeaf92b20ce3f7ae1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436063"
---
# <a name="best-practices-for-lync-server-2013-environments"></a>Lync Server 2013 環境のベストプラクティス

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2014-08-04_

システムの実行中の操作には、次の一般的な原則を適用する必要があります。

  - **MOF を理解して使用**   する  MOF は、日常の Lync Server 2013 の運用など、IT 資産の管理に関する組織の技術ガイダンスを提供するベストプラクティス、原則、およびモデルの集まりです。 MOF ガイドラインは、次のように、Microsoft 製品のミッションクリティカルな生産システムの信頼性、可用性、サポート性、および管理性を実現するのに役立ちます。 詳細については、「 [Microsoft Operations Framework 4.0](https://go.microsoft.com/fwlink/p/?linkid=40939)」を参照してください。

  - **Lync Server 2013 のベストプラクティスについて**   Lync Server 2013 を管理するための実用的で実証された手順を実装することをお勧めします。 試用、テスト、文書化された操作を管理する方法は、独自のメソッドを開発する場合よりも効率的に行うことができます。

  - **個別の操作を日単位、週単位、月単位のプロセスに分ける**   定期的に実行する必要のある運用タスクを文書化します。 タスクの実行方法を文書化することで、新しいテクノロジが展開された、またはスタッフが変更されたときなど、運用環境に変更があった場合に、情報が確実に保持されるようにすることができます。 タスクが毎日、毎週、毎月実行される管理可能なワークロードに、運用タスクを分けることをお勧めします。 日常的な作業では、システムの機能に重点を置いています。また、毎月のタスクでは、システムの長期の正常性を確保することに重点を置いています。
    
    このドキュメントは、エンタープライズ Voip でインスタントメッセージ/プレゼンス (IM/P) コンポーネントまたは IM/P を展開する環境で使用できます。 タスクまたはチェックリスト項目がエンタープライズ Voip に固有の場合、これが説明されています。また、環境にエンタープライズ Voip が含まれていない場合は、その部分がスキップされる可能性があります。

  - **Lync Server のオペレーティングシステムに必要なツールを展開する 2013**   問題のトラブルシューティング、タスクの自動化、Lync Server 2013 環境の監視と維持に役立つツールが数多くあります。 運営チームによって実行されるタスクを正確かつ効率的に実行し、管理された方法で実行するために、組織用に標準のツールセットを定義します。 また、インシデントおよび主要構成の変更を追跡するプロセスも実装する必要があります。

<div>

## <a name="reference"></a>Reference

一般的にサーバー管理の基本について理解していない読者のために、ここではサーバー管理のプラクティスの概要について説明します。 既にサーバー管理に慣れている読者は、このセクションをスキップすることができます。

ベストプラクティスとは、IT プロフェッショナルが多くの環境で得た知識と経験に基づいた推奨事項です。 Lync Server の管理者が日常的に実行する必要のある一般的なタスクの標準的な手順と、Lync Server 環境を管理するために使う必要のあるツールについて説明します。

Lync 管理者向けの一般的なタスクには、次のものがあります。

  - **容量と可用性の管理**   今後の容量要件を予測し、システムの容量、信頼性、および可用性に関するレポートを作成する方法と測定内容を定義します。 Lync Server を実行しているサーバーがシステムの負荷を処理するように設定されていること、および予期しないダウンタイムがサービスレベル契約 (SLA) で定義されているレベルの下にあることを確認する必要があります。 さらに、定義された要件を引き続き満たすためには、ハードウェアをアップグレードする必要があります。

  - **管理と構成の管理を変更**   する  IT システムに対する変更を制御します。 これには、テスト、アプリケーションのフィードバックと不測事態対応の計画、すべての変更の文書化、問題が発生した場合の管理からの承認などが含まれます。 ソフトウェアとハードウェアの資産とその構成を記録しておきます。

  - **システム管理**   データベース管理やサイト管理などの管理タスクを実行するための標準的な方法について説明します。

  - **セキュリティ管理**   IT インフラストラクチャのデータの機密性、データの整合性、データの可用性を保護するための詳細なポリシーと計画を立てます。 これには、IT セキュリティインフラストラクチャの維持と調整に関連する日常的なアクティビティとタスクが含まれます。

  - **システムのトラブルシューティング**   将来の問題を回避するための手順など、予期しない問題を処理するためのアウトライン方法。

  - **サービスレベル契約**   IT システムのパフォーマンスに関する一連の目標を維持し、これらの目標に対するパフォーマンスを定期的に測定します。

  - **ドキュメント**   構成情報や教訓などの標準的な手順を文書化し、それを必要とするスタッフメンバーが利用できるようにします。 構成の変更が行われると、それに合わせてドキュメントが更新されます。

</div>

<div>

## <a name="related-sections"></a>関連項目

続行する前に、次のシステム操作に関するトピックを確認してください。

  - [Lync Server 2013 での容量と可用性の管理](lync-server-2013-capacity-and-availability-management.md)

  - [Lync Server 2013 で管理を変更する](lync-server-2013-change-management.md)

  - [Lync Server 2013 での構成管理](lync-server-2013-configuration-management.md)

  - [Lync Server 2013 でのシステム管理](lync-server-2013-system-administration.md)

  - [Lync Server 2013 のサービスレベル契約](lync-server-2013-service-level-agreements.md)

  - [Lync Server 2013 のドキュメント](lync-server-2013-documentation.md)

  - [Lync Server 2013 の標準手順](lync-server-2013-standard-procedures.md)

  - [Lync Server 2013 の緊急対応手順](lync-server-2013-emergency-procedures.md)

</div>

<div>

## <a name="see-also"></a>関連項目


[Microsoft 運用フレームワーク4.0](https://go.microsoft.com/fwlink/p/?linkid=40939)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

