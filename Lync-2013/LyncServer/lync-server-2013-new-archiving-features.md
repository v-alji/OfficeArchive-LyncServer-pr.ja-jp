---
title: 'Lync Server 2013: アーカイブの新機能'
description: 'Lync Server 2013: 新しいアーカイブ機能。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New Archiving features
ms:assetid: c002e367-41ad-498d-9d23-8b117ac435b2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205225(v=OCS.15)
ms:contentKeyID: 48185288
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b5b69c90e62914284f178ae328375c6e350f5b3e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425164"
---
# <a name="new-archiving-features-in-lync-server-2013"></a>Lync Server 2013 のアーカイブの新機能

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-10-09_

Lync Server 2013 でアーカイブすると、次の種類のコンテンツをアーカイブできます。

  - ピアツーピアのインスタント メッセージ

  - マルチパーティのインスタントメッセージである会議 (会議)

  - アップロードされたコンテンツ (配付資料など) およびイベント関連のコンテンツ (参加、退席、アップロード、共有、表示設定の変更など) を含む会議コンテンツ

さらに、Lync Server 2013 でアーカイブすると、展開と運用の効率を向上させるための新機能が提供されます。 次の新機能が含まれています。

  - **フロントエンドサーバー上のアーカイブの collocation。**   Lync Server 2013 には、別のアーカイブサーバーの役割がありません。 アーカイブは、Enterprise Edition の展開におけるすべてのフロントエンドサーバーと、プールまたはサイト用に構成できる標準エディションのサーバーで利用できるオプションの機能です。

  - **Microsoft Exchange の統合。**   アーカイブを展開するときに、Exchange 2013 を使用しているすべてのユーザーに対して、既存の Exchange 2013 ストレージを使ってアーカイブ用のデータストレージを統合することができます。そのため、メールボックスは In-Place 保留にしておく必要があります。そのため、別の SQL Server データベースを展開して Lync データをアーカイブする必要はありませ Exchange 2013 を展開していない場合、または統合しない場合、または、Exchange 2013 を使用していない Lync 2013 ユーザーが In-Place 保留になっている場合は、SQL Server を使って、アーカイブデータを Lync コミュニケーションから保存することで、個別のアーカイブデータベースを展開できます。 Microsoft exchange 統合と Lync Server 2013 アーカイブデータベースの両方を使用できますが、展開内のすべてのユーザーに対して、Microsoft Exchange 統合を使用することができます。 In-Place ホールドの詳細については、「インプレースホールド」を参照してください [https://go.microsoft.com/fwlink/p/?LinkId=267500](https://go.microsoft.com/fwlink/p/?linkid=267500) 。

  - **SQL ストアのミラーリング。**   アーカイブを展開するときに、アーカイブデータベースに対して SQL Server データベースのミラーリングを有効にすることができます。

  - **ホワイトボードと投票のアーカイブ。**   アーカイブされた会議コンテンツには、会議中に共有されるホワイトボードと投票が含まれるようになりました。

次の種類のコンテンツはアーカイブされません。

  - ピアツーピアのファイル転送

  - ピアツーピアのインスタント メッセージおよび会議の音声ビデオ

  - ピアツーピアインスタントメッセージ (im) と会議のアプリケーション共有

<div>

## <a name="see-also"></a>関連項目


[Lync Server 2013 のアーカイブの計画](lync-server-2013-planning-for-archiving.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

