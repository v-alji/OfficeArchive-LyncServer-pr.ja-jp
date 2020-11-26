---
title: 'Lync Server 2013: プールのフェールオーバーおよびフェールバックの復旧時間'
description: プールフェールオーバーとプールのフェールバックの Lync Server 2013 の回復時間。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Recovery time for pool failover and pool failback
ms:assetid: 902c658f-8442-4d0d-b3ad-bf795ecd550d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205079(v=OCS.15)
ms:contentKeyID: 48184786
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1bb09c32ac4d062358a511464dc21aa7346ee034
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436679"
---
# <a name="recovery-time-for-pool-failover-and-pool-failback-in-lync-server-2013"></a>Lync Server 2013 のプールのフェールオーバーおよびフェールバックの復旧時間

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-09-10_

プールのフェールオーバーとプールのフェールバックの場合、復旧時間の目標 (RTO) のエンジニアリングターゲットは30分です。 これは、管理者が障害が発生し、フェールオーバー手順が開始された後に、フェールオーバーが発生するために必要な時間です。 管理者が状況を評価して意思決定を行う時間は含まれません。また、フェールオーバーの完了後にユーザーがもう一度サインインする時間も含まれません。

プールのフェールオーバーとプールのフェールバックの場合、RPO (目標復旧時点) のエンジニアリングターゲットは30分です。 これは、障害が発生したときに、バックアップ サービスのレプリケーション待機時間に起因してデータが消失する可能性がある時間を表すものです。 たとえば、プールが午前10:00 時に停止し、RPO が30分の場合は、9:30 A.M. までにプールに書き込まれたデータ また、10:00 はバックアッププールにレプリケートされておらず、失われる可能性があります。

このドキュメントに示す RTO と RPO の数値はすべて、待ち時間の少ない高速接続で 2 つのサイトが結ばれている同じ地域内に 2 つのデータ センターが設置されていることを前提としています。 どちらの数値も、データ レプリケーションにバックログがない事前定義済みのユーザー モデルに対して、同時アクティブ ユーザーが 40,000 人と Lync に対して有効になっているユーザーが 200,000 人存在するプールを対象として測定を行った結果です。 これらの数値は、パフォーマンス テストおよび検証に基づいて変更される可能性があります。

</div>

<span> </span>

</div>

</div>

</div>

