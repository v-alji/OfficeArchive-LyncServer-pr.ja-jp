---
title: 'Lync Server 2013: バックアップと復元の計画を立てる'
description: 'Lync Server 2013: バックアップと復元の戦略を確立します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Establishing a backup and restoration strategy
ms:assetid: f545a75f-bbc4-4968-b510-8f6f3920112b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202195(v=OCS.15)
ms:contentKeyID: 51541532
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f4fdefed873d1fd69d82f8ecebceeb92f06f65f7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428469"
---
# <a name="establishing-a-backup-and-restoration-strategy-for-lync-server-2013"></a>Lync Server 2013 のバックアップと復元の戦略を確立する

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2013-03-26_

Lync Server のバックアップと復元の計画を作成するには、組織の目標に合った戦略を開発する必要があります。 効果的なバックアップと復元計画を作成するには、次のことを行う必要があります。

  - 業務上の優先度を設定します。

  - バックアップと復元の要件を特定します。

<div>

## <a name="establishing-business-priorities"></a>業務上の優先度を設定する

組織のビジネス優先順位を評価する。 通常、バックアップと復元の戦略に影響を与える主な業務上の優先順位は、次のとおりです。

  - ビジネス継続性の要件

  - データの完全性

  - データの重要度

  - 移植性の要件

  - コストの制約

顧客によって開発されたサービスレベルアグリーメント (Sla) を決定するために、このようなヘルプなどのビジネスニーズについて説明します。 サービスレベル契約は、バックアップと復元戦略に大きく影響します。

</div>

<div>

## <a name="identifying-backup-and-restoration-requirements"></a>バックアップと復元の要件を特定する

ビジネス優先度とサービスレベル契約によって、Lync Server のバックアップと復元に関する組織の要件を決定することができます。 次の要件を特定して、文書化します。

  - **バックアップの頻度**   バックアップの頻度に関するベストプラクティスの詳細については、「 [Lync Server 2013 のバックアップと復元のベストプラクティス](lync-server-2013-best-practices-for-backup-and-restoration.md)」を参照してください。

  - **バックアップと復元ツール**   だれがツールを使用するか、どのコンピューターを使用するかを指定します。 このトピックで説明しているツールと必要なアクセス許可について詳しくは、「 [Lync Server 2013 のバックアップと復元の要件](lync-server-2013-backup-and-restoration-requirements-tools-and-permissions.md)」をご覧ください。ツールと権限。

  - **バックアップの場所**   バックアップがローカルまたはリモートで保持されるかどうかを確認し、セキュリティとアクセシビリティを考慮します。 バックアップに使用するメディアを指定します。

  - **ハードウェアとソフトウェアの要件**   バックアップと復元をサポートするために必要なソフトウェアとネットワーク接続のバックアップや復元のハードウェアなど、特定のハードウェアとソフトウェアの要件を特定して文書化します。 ハードウェアとソフトウェアの要件を開発する際には、次のようなさまざまな復元シナリオを念頭に置いてください。

  - **復元シナリオ**   次のシナリオの復元プロセスを以下に示します。
    
      - Lync サーバープールは失敗します。 このシナリオでは、プール内の各サーバーを再構築する必要があります。
    
      - Standard Edition サーバーで障害が発生します。 このシナリオでは、新規またはクリーンなコンピューターにサーバーを再構築し、データベースを復元する必要があります。
    
      - 中央管理ストアが失われます。 少なくとも、このシナリオでは、一元管理ストアを復元して発行する必要があります。
    
      - 中央管理ストアが正常に機能している場合、バックエンドサーバーが失われます。 このシナリオでは、新規またはクリーンなコンピューターにサーバーを再構築し、データベースを復元する必要があります。
    
      - Lync Server プールのメンバーであるサーバーが失敗します。 このシナリオでは、新しいコンピューターまたはクリーンコンピューターにサーバーを再構築する必要があります。
    
      - ファイルストアが失敗します。 このシナリオでは、ファイルサーバーまたはファイルクラスターを復元する必要があります。
    
      - アーカイブ、監視、または永続的なチャットデータベースは失敗します。 このシナリオでは、データベースを再作成する必要があります。データが組織にとって重要である場合は、データを復元する必要があります。 Lync Server のバックアップと実行を取得するには、アーカイブ、監視、常設チャットデータは必要ありません。

</div>

</div>

<span> </span>

</div>

</div>

</div>

