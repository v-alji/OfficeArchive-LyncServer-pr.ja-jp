---
title: 'Lync Server 2013: 新しい障害復旧および高可用性機能'
description: 'Lync Server 2013: 新しい障害回復と高可用性機能。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New disaster recovery and high availability features
ms:assetid: 4fa7cd0f-784b-4d3f-b839-432c2ecaf7c1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204892(v=OCS.15)
ms:contentKeyID: 48184130
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 92816f61b66d9eed76c16286aaa6c7392dca7708
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425115"
---
# <a name="new-disaster-recovery-and-high-availability-features-in-lync-server-2013"></a>Lync Server 2013 の新しい障害復旧および高可用性機能

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-09-20_

Lync Server 2010 の場合と同様に、Lync Server 2013 の主な高可用性 (HA) スキームは、プールによるサーバーの冗長性に基づいています。 特定のサーバーの役割を実行するサーバーで障害が発生した場合は、プール内の同じ役割を実行する他のサーバーがそのサーバーの負荷を引き受けます。 同じことが、フロントエンド サーバー、エッジ サーバー、仲介サーバー、およびディレクターでも実行されます。

Lync Server 2013 は、2つのデータセンターにあるフロントエンドプールを組み合わせることによって、新しい障害回復手段を追加します。 ペアリングされたプールのいずれかがダウンした場合、管理者はそのプールのユーザーをペアの他のプールにフェールオーバーして、サービスの継続を提供できます。 この機能には、記憶域ネットワークや共有ディスクなどの高価なネットワークやハードウェアソリューションは必要ありません。

また、Lync Server 2013 により、バックエンドサーバーの高可用性が追加されます。 これは、フロントエンドプール用に2つのバックエンドサーバーを展開し、バックエンドサーバーで実行されているすべての Lync データベースの同期 SQL ミラーリングをセットアップする、オプションのトポロジです。 ミラーのミラーリングを行うかどうかを選ぶことができます。

<div>

## <a name="see-also"></a>関連項目


[Lync Server 2013 での高可用性および障害復旧の計画](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

