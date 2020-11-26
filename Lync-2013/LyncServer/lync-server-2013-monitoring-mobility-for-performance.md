---
title: 'Lync Server 2013: パフォーマンスのためのモビリティの監視'
description: 'Lync Server 2013: パフォーマンスのためのモビリティの監視。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Monitoring mobility for performance
ms:assetid: 9c831c63-9a7d-48ec-9118-f8a7e80ddd04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690033(v=OCS.15)
ms:contentKeyID: 48184908
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d6c366542e88406df043ba1a782ee12cd64bd804
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425403"
---
# <a name="monitoring-mobility-for-performance-in-lync-server-2013"></a>Lync Server 2013 でのモバイルパフォーマンスの監視

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2013-02-14_

Lync Server Mobility Service (Mcx) とユニファイドコミュニケーション Web API (UCWA) では、フロントエンドサーバーとフロントエンドプールの負荷が高くなります。 モバイルアプリケーションが最小化されている場合でもサーバーへの接続を維持するモバイルデバイス (lync 2010 Mobile を実行している Android や Nokia デバイス、Lync 2013 Mobile を実行している Android および Apple デバイスなど) は、モバイルアプリケーションが最小化されているときにサーバーへの接続を終了するデバイスよりも大きくロードされます。 モバイル使用の増加に応じて、容量を増やす必要があるタイミングを判断するために、モビリティのパフォーマンスを監視する必要があります。

モビリティのパフォーマンスに影響を与えるいくつかの制限値があります。

  - 使用可能なメモリ

  - 要求キューの制限

  - 同時接続数

  - IIS キューの長さ

モビリティのパフォーマンスに影響を与える可能性のあるサーバーの制限は、最大12個の同時サインイン、認証、セッションの更新、終了です。 ただし、ほとんどの展開でこれらの最大値を変更する必要はありません。

<div>

## <a name="in-this-section"></a>このセクション中

  - [Lync Server 2013 でのサーバーメモリ容量の上限を監視する](lync-server-2013-monitoring-for-server-memory-capacity-limits.md)

  - [Lync Server 2013 でのモビリティサービスと UCWA の使用状況の監視](lync-server-2013-monitoring-mobility-service-and-ucwa-usage.md)

  - [Lync Server 2013 での高パフォーマンスのモビリティサービスの構成](lync-server-2013-configuring-mobility-service-for-high-performance.md)

  - [Lync Server 2013 で IIS 要求トレースのログファイルを監視する](lync-server-2013-monitoring-iis-request-tracing-log-files.md)

  - [Lync Server 2013 のモバイルパフォーマンスカウンター](lync-server-2013-mobility-performance-counters.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

