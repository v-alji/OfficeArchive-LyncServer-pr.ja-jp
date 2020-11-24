---
title: トポロジ ビルダーを使用して高可用性と障害回復を構成する
description: トポロジビルダーを使用して、高可用性と障害回復を構成します。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using Topology Builder to configure high availability and disaster recovery
ms:assetid: abc1a25d-1f5e-46ef-91d2-0144fc847206
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205172(v=OCS.15)
ms:contentKeyID: 48185113
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 04764a58ac3ae1bbe0df97aadeabb03158ce8100
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400118"
---
# <a name="using-topology-builder-to-configure-high-availability-and-disaster-recovery-in-lync-server-2013"></a>Lync Server 2013 でトポロジ ビルダーを使用して高可用性と障害回復を構成する

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-10-06_

[トポロジビルダー] で次の手順を実行して、常設チャットサーバーの高可用性と障害回復を構成します。

1.  ミラーデータベースとログ配布のセカンダリデータベース SQL Server ストアを追加します。

2.  常設チャットサーバーサービスのプロパティを編集するには、次の操作を行います。
    
    1.  プライマリ データベースのミラーリングを有効にします。
    
    2.  プライマリミラー SQL Server ストアを追加します。
    
    3.  SQL Server のログ配布データベースを有効にします。
    
    4.  SQL Server ログ配布のセカンダリ SQL Server ストアを追加します。
    
    5.  セカンダリデータベースの SQL Server ストアミラーを追加します。
    
    6.  トポロジを公開します。

</div>

<span> </span>

</div>

</div>

</div>

