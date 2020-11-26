---
title: 'Lync Server 2013: ネットワーク パフォーマンスの監視'
description: 'Lync Server 2013: ネットワークのパフォーマンスを監視します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Monitoring network performance
ms:assetid: bc3a01da-91eb-4c0c-9598-35e5e46b00f6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720923(v=OCS.15)
ms:contentKeyID: 63969647
ms.date: 04/27/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0ead7e3f9001b06c783c9b22327581e795a20322
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425347"
---
# <a name="monitoring-network-performance-in-lync-server-2013"></a>Lync Server 2013 でのネットワーク パフォーマンスの監視

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2016-04-27_

Lync Server 2013 は、ネットワークに大きく依存して、インスタントメッセージング (IM)、音声通話、またはビデオ通信を通じて、ユーザー間の通信を可能にする、リアルタイムの通信技術です。 そのため、ユーザーが選択したコミュニケーションのモダリティが最適なエクスペリエンスを実現することを保証するために、ネットワークパフォーマンスを継続的に監視することが重要です。

ネットワークパフォーマンスは、次の2つのレベルで測定できます。

  - **全体的なネットワークパフォーマンス**   このレベルのパフォーマンス測定では、組織は、ネットワークの "大きな画像" ビューを作成することができ、通常はサードパーティのネットワーク監視システムを使用して実装されます。 これらのシステムでは、管理者が特定のネットワークコンポーネントの正常性をいつでも判断できるように、ルーターなどのリモートネットワークデバイスからパフォーマンスと容量のデータを受け取ります。

  - **個々のサーバーのパフォーマンス**   このレベルのパフォーマンス測定は、特定のサーバーに制限されています。また、管理者は、特定のパフォーマンスの問題のトラブルシューティングや、特定の期間における個々のサーバーのパフォーマンスを測定するために、キャパシティ計画プロセスの一環として、特定のサーバーのネットワークパフォーマンスを距離するのに役立ちます。

次のセクションで説明されているツールを使用して、ネットワークを監視することができます。

<div>

## <a name="tools-for-overall-network-performance-monitoring"></a>ネットワークパフォーマンスの全体的な監視用のツール

<div>

## <a name="system-center-operations-manager-2012"></a>System Center Operations Manager 2012

System Center Operations Manager は、IT 環境全体のサービスレベルを向上させるためのカスタマイズと拡張が容易なエンドツーエンドのサービス管理を提供します。 これにより、運用および IT 管理チームは、配布された IT サービスの正常性に影響する問題を特定して解決することができます。 エンドツーエンドのサービス管理は、Microsoft ベースの環境に限定されません。 管理用の Web サービス (WS-MANAGEMENT)、簡易ネットワーク管理プロトコル (SNMP)、パートナーソリューションをサポートしているため、Microsoft オペレーティングシステムとハードウェアを実行していないシステムは、System Center Operations Manager 2012 内のサービス監視に含めることができます。

</div>

<div>

## <a name="system-center-operations-manager-2012-and-third-party-network-management-solutions"></a>System Center Operations Manager 2012 とサードパーティのネットワーク管理ソリューション

**EMC Smarts**   Operations Manager 向けの EMC ソリューションを使用すると、サービスレベルに影響する問題をすばやく解決できます。 Operations Manager 用の EMC ソリューションを使用することで、1つの統合された自動ソリューションで IT サービスチェーン全体を管理および監視することができます。 パフォーマンスと可用性の問題の根本原因を簡単に特定し、それらをより迅速に解決して効果とコストを削減します。 主な利点は次のとおりです。

  - 高度で使いやすい管理によって、手作業での並べ替えやフィルター処理が困難なアラートの代わりに戦略的ビジネス価値を実現することができます。

  - **より高速な解像度**   IT の問題を解決し、ビジネスニーズにすばやく対応し、効果とコストを削減します。

  - **操作の合理化**   複数の管理ツール、アプリケーション、およびターミナルを組み合わせることで、IT の複雑さを回避します。

詳細については、次のページを参照してください。

[Microsoft System Center Operations Manager](https://go.microsoft.com/fwlink/p/?linkid=243651)

[Microsoft System Center Operations Manager のソリューション](http://www.emc.com/collateral/software/data-sheet/h6135-server-manager-ds.pdf)

</div>

<div>

## <a name="third-party-solutions"></a>サードパーティのソリューション

Hp ネットワーク **管理センター (以前は Hp OpenView と呼ばれています)**[Hp ネットワーク管理センター](http://www8.hp.com/us/en/software-solutions/network-management/index.html?%26zn=bto%26cp=1-11-15-119_4000_100__)では、ネットワークの可用性とパフォーマンスを向上させるために、統合されたフォールトおよびパフォーマンス管理を実現しています。    ネットワーク管理センターは、障害、パフォーマンス、構成、および変更管理を統合する HP 自動ネットワーク管理ソリューションの一部です。

**Cisco のネットワーク管理とオートメーション製品**   企業向けには、Cisco には、CiscoWorks LAN 管理ソリューションや Cisco ネットワーク分析モジュールなど、さまざまな管理製品が用意されており、運用効率の向上とネットワークのダウンタイムの削減に役立ちます。 これらの製品に関するその他の情報については、の Cisco web サイトを参照してください [https://www.cisco.com/en/US/products/sw/netmgtsw/index.html](https://www.cisco.com/en/us/products/sw/netmgtsw/index.html) 。

簡易ネットワーク管理プロトコル (SNMP) 簡易ネットワーク管理プロトコル (SNMP) は、TCP/IP ネットワークを管理するための戦略を定義するネットワーク管理標準です。 SNMP では、ネットワークに関する構成と状態の情報を取得し、その情報を指定のコンピューターに送信してイベントを監視することができます。 この規格に基づくネットワーク管理プロトコルは、次のような分散アーキテクチャを使用しています。

  - 複数の管理ノード。各ノードには、管理インストルメンテーションへのリモートアクセスを提供するエージェントと呼ばれる SNMP エンティティが含まれています。

  - 管理要素を監視および制御するために管理アプリケーションを実行する、マネージャーと呼ばれる少なくとも1つの SNMP エンティティ。 管理要素は、ホストやルーターなどのデバイスです。 これらのユーザーは、管理情報にアクセスすることで監視および制御されます。

  - 管理プロトコル SNMP は、管理ステーションとエージェントの間で管理情報を伝えるために使用されます。 管理情報とは、管理情報ベース (MIB) と呼ばれる仮想情報ストア内に存在する管理対象オブジェクトのコレクションを指します。

<div>


> [!NOTE]  
> サードパーティのネットワーク監視ソリューションの例は、上記に記載されています。 このリストは確定的なものではありません。また、Microsoft は特定のベンダーソリューションに対応していません。 組織に最適なネットワーク監視ソリューションを決定するには、ネットワークサービスプロバイダーまたは各テクノロジプロバイダーに問い合わせてください。



</div>

</div>

</div>

<div>

## <a name="tools-for-monitoring-individual-server-network-performance"></a>個々のサーバーのネットワークパフォーマンスを監視するためのツール

<div>

## <a name="system-center-operations-manager-2012"></a>System Center Operations Manager 2012

System Center Operations Manager 2012 を使用すると、管理者は Windows Server 2012 管理パックを通じて個々のサーバーのネットワークパフォーマンスを表示することができます。 Windows Server オペレーティングシステム管理パックには、管理者がネットワークアダプターのパフォーマンスとアダプターの正常性を監視できる "パフォーマンス" 管理パックが含まれています。

</div>

<div>

## <a name="windows-network-monitor"></a>Windows ネットワークモニター

サーバー上のリソース使用状況の収集、表示、分析、ネットワークトラフィックの測定を行います。 ネットワークモニターは、ネットワークアクティビティを排他的に監視します。 ネットワークデータをキャプチャして分析し、そのデータをパフォーマンスログと共に使用することにより、ネットワークの使用状況の確認、ネットワークの問題の特定、将来のネットワークニーズの予測を行うことができます。

ネットワークモニター3.4 の詳細と、ネットワークモニターのインストールと構成、データのキャプチャと分析の方法については、次のセッションを参照してください。ネットワークモニター3.3 の概要。 また、 [ネットワークモニターのブログ](https://blogs.technet.com/b/netmon/)も確認してください。

</div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

