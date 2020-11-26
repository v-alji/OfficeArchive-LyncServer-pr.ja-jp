---
title: 'Lync Server 2013: モビリティサービスと UCWA の使用状況を監視する'
description: 'Lync Server 2013: モビリティサービスと UCWA の使用状況を監視します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Monitoring Mobility Service and UCWA usage
ms:assetid: 8389b37a-ca3e-4047-8b51-85bc07da87e8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690025(v=OCS.15)
ms:contentKeyID: 48184683
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6575941faf904e46cd1f66d7226a16c88e8cbaa3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425396"
---
# <a name="monitoring-mobility-service-and-ucwa-usage-in-lync-server-2013"></a>Lync Server 2013 でのモビリティサービスと UCWA の使用状況の監視

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2013-02-14_

継続的に、Lync Server Mobility Service (Mcx) とユニファイドコミュニケーション Web API (UCWA) で使用されている CPU とメモリを監視する必要があります。 使用状況を監視するには、次の操作を行います。

**Unified Communications Web API (UCWA):**

  - インターネットインフォメーションサービス (IIS) マネージャーでの **LyncUcwa** worker プロセス。 [**ワーカー プロセス**] ウィンドウで、[**CPU %**] および [**プライベート バイト (KB)**] (メモリ) の列を確認します。

  - [**CPU**] および [**プロセッサ**] パフォーマンス カウンター。

ほとんどの展開で、UCWA の CPU 使用率は平均で 15% を下回っている必要があります。 メモリ使用量は、「 [Lync server 2013 でのサーバーメモリ容量の上限を監視](lync-server-2013-monitoring-for-server-memory-capacity-limits.md)する」で説明されている制限内に収まる必要があります。

CPU とメモリの使用状況カウンターに加えて、以下のパフォーマンス カウンターを使用すると、サーバーが要求で過負荷になっていないかどうかを確認するのに役立つ場合があります。

  - **LS: WEB –調整と認証 \\WEB –要求の合計が処理中で** あることを示します。これは、サーバー上の保留中の web 要求の数を示します。 このカウンターが1万に達すると、その後の要求は失敗し、"503-サービスを利用できません" というエラーメッセージが表示されます。

  - **ASP.NET \\要求はキューに入れら** れます (常に0である必要があります)。

<div>


> [!NOTE]  
> これらの値を満たしているか、それ以上の場合は、Web サービスをホストしているコンピューターの CPU、コア数、メモリのサイズが適切に調整されるように、キャパシティ計画を再検討して再計算する必要があります。



</div>

**Mobility Service (Mcx):**

  - **Csintmcxapppool** と **csextmcxapppool** ワーカープロセス (インターネットインフォメーションサービス (IIS) マネージャー)。 [**ワーカー プロセス**] ウィンドウで、[**CPU %**] および [**プライベート バイト (KB)**] (メモリ) の列を確認します。

  - [**CPU**] および [**プロセッサ**] パフォーマンス カウンター。

ほとんどの展開で、Mobility Service の CPU 使用率は平均で 15% を下回っている必要があります。 メモリ使用量は、「 [Lync server 2013 でのサーバーメモリ容量の上限を監視](lync-server-2013-monitoring-for-server-memory-capacity-limits.md)する」で説明されている制限内に収まる必要があります。

CPU とメモリの使用状況カウンターに加えて、以下の ASP.NET パフォーマンス カウンターを使用すると、サーバーが要求で過負荷になっていないかどうかを確認するのに役立つ場合があります。

  - **ASP.NET v 2.0.50727 \\現在の要求**: サーバー上の保留中の web 要求の数を示します。 このカウンターが5000に達すると、その後の要求は失敗し、"503-サービスを利用できません" というエラーメッセージが表示されます。

  - **ASP.NET \\要求はキューに入れら** れます (常に0である必要があります)。

<div>


> [!NOTE]  
> これらの値を満たしている、または超える場合は、Web サービスをホストしているコンピューターの CPU、コア数、メモリの適切なサイズ変更のために、キャパシティ計画を再検討して再計算する必要があります。



</div>

<div>

## <a name="see-also"></a>関連項目


[Lync Server 2013 でのサーバーメモリ容量の上限を監視する](lync-server-2013-monitoring-for-server-memory-capacity-limits.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

