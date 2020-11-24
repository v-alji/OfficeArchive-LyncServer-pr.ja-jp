---
title: 'Lync Server 2013: グループ通話のピックアップで使用されるコンポーネント'
description: 'Lync Server 2013: グループ通話のピックアップで使用されるコンポーネント。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components used by Group Call Pickup
ms:assetid: 45db2f23-d486-4b20-a8cf-7b48a1f9fd3a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945625(v=OCS.15)
ms:contentKeyID: 51541470
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 517f75dcbac8bfed0e749c061a9696b7667e10ed
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398523"
---
# <a name="components-used-by-group-call-pickup-in-lync-server-2013"></a>Lync Server 2013 でグループ通話のピックアップによって使用されるコンポーネント

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2013-01-30_

グループ通話のピックアップは、エンタープライズボイスと Call パークアプリケーションを展開したときに自動的に展開されます。 グループ通話のピックアップを有効にするには、通話ピックアップグループ番号として指定された別の範囲の番号を使用して、ユーザーをピックアップグループに発信し、グループ通話のピックアップを許可するようにユーザーを割り当てることで、グループ通話のピックアップを有効にします。 グループ通話のピックアップは、次の Lync Server コンポーネントでサポートされています。

  - **アプリケーションサービス**   アプリケーションサービスは、コールパークアプリケーションなどのユニファイドコミュニケーションアプリケーションを展開、ホスティング、および管理するためのプラットフォームを提供します。 アプリケーションサービスは、フロントエンドプールのすべてのフロントエンドサーバーと、すべての Standard Edition サーバーに自動的にインストールされます。

  - **コールパークアプリケーション**   コールパークアプリケーションは、アプリケーションサービスによってホストされるユニファイドコミュニケーションアプリケーションの1つです。 グループ通話のピックアップは、コールパークアプリケーションに基づいています。

  - **Lync Server 管理シェル**   グループ通話のピックアップグループを管理するには、Lync Server 管理シェルを使用します。

  - **SEFAUtil リソースキットツール**   セカンダリ拡張機能のアクティブ化ユーティリティ (SEFAUtil) を使用して、ユーザーを通話ピックアップグループに割り当て、ユーザーに対して通話集配を有効または無効にします。

</div>

<span> </span>

</div>

</div>

</div>

