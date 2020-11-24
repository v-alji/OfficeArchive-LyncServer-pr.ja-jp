---
title: 'Lync Server 2013: QoE レポート'
description: 'Lync Server 2013: QoE レポート。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: QoE reports
ms:assetid: 49c827af-b8dd-4c6e-b0dc-b4bc6d60e9a3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720913(v=OCS.15)
ms:contentKeyID: 63969601
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 55965d246b7f0ddd71eaeeec99d218eaf8819c2e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398997"
---
# <a name="qoe-reports-in-lync-server-2013"></a>Lync Server 2013 の QoE レポート

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2014-05-01_

<div>

## <a name="qoe-summarytrend-reports"></a>QoE サマリー/トレンドレポート

QoE サマリー/トレンドレポートは、組織のネットワークリソースが十分であることを確認するために、1日のピーク使用時間を見つけてメディアの品質を確認するのに役立ちます。 組織では、レポートで利用可能な多くのフィルターを使用して、特定の場所、クライアントとデバイスの種類、サーバーのパフォーマンスの数値を特定することもできます。

QoE サマリー/トレンドレポートは次の要素で構成されます。

  - UC 対多集計のサマリー/トレンドレポート

  - PSTN サマリー/トレンドレポート

  - 会議の概要/傾向レポート

</div>

<div>

## <a name="qoe-performance-reports"></a>QoE のパフォーマンスレポート

QoE パフォーマンスレポートには、仲介サーバー、A/V 会議サーバー、エンドポイントの場所の QoE パフォーマンスに焦点を当てた3つのレポートに関する詳細が用意されています。

</div>

<div>

## <a name="mediation-server-performance-report"></a>仲介サーバーパフォーマンスレポート

仲介サーバーのパフォーマンスレポートには、指定した期間中に、1つ以上の仲介によって得られたメトリックが一覧表示されます。 ユニファイドコミュニケーション (UC) 対仲介サーバーの区間と、各通話の仲介サーバー間の区間のメトリックは、別々に報告されます。 このレポートを使用して、組織のさまざまな仲介サーバーのボリュームとパフォーマンスを比較します。

各仲介サーバー (および各通話区間用) には、次のようなレポートが表示されます。

  - 通話の数

  - パケット損失

  - ラウンドトリップ時間

  - ジッター

  - 話し言葉平均の意見 (MOS)

  - MOS を送信中

  - 聞き取り MOS

  - Network MOS

  - ネットワーク MOS の低下

  - エコーリターン

  - シグナルレベル

</div>

<div>

## <a name="av-conferencing-server-performance-report"></a>A/V 会議サーバーパフォーマンスレポート

A/V 会議サーバーパフォーマンスレポートでは、指定された期間中に1つ以上の A/V 会議サーバーによって達成された指標の一覧が表示されます。 このレポートは、組織のさまざまな A/V 会議サーバーのボリュームとパフォーマンスを比較するために使用できます。 組織でレポートを分離して、Lync クライアントや PSTN クライアントなど、特定のクライアントの種類のエクスペリエンスのみを表示することもできます。

各 A/V 会議サーバーでは、レポートに次の内容が表示されます。

  - 会議の数

  - パケット損失

  - ラウンドトリップ時間

  - ジッター

  - 話し言葉平均の意見 (MOS)

  - MOS を送信中

  - 聞き取り MOS

  - Network MOS

  - ネットワーク MOS の低下

  - エコーリターン

  - シグナルレベル

</div>

<div>

## <a name="location-based-performance-report"></a>位置ベースのパフォーマンスレポート

Location-Based のパフォーマンスレポートでは、ネットワーク上の場所の一覧が表示され、それぞれの場所には、事前に決定された各品質の範囲の通話数が示されます。 このレポートの目標は、さまざまな場所についての組織の電話の大半の通話品質を把握して、組織のさまざまな場所でのさまざまなメディア品質の評価を確認することです。

レポートを表示すると、さまざまなメトリックのテーブルが表示されます。組織がレポートを決定する各指標ごとに1つのテーブルが表示されます。 このレポートには、次のメトリックから選ぶことができます。

  - 話し言葉平均の意見 (MOS)

  - Network MOS

  - ネットワーク MOS の低下

  - MOS を送信中

  - 聞き取り MOS

  - パケット損失

  - ジッター

  - 間隔

</div>

</div>

<span> </span>

</div>

</div>

</div>

