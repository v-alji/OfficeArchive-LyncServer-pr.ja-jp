---
title: バックエンド サーバー上の SQL Server インスタンスとデータベースの削除
description: バックエンドサーバー上の SQL Server インスタンスとデータベースを削除します。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove SQL Server instances and databases on the Back End Server
ms:assetid: 32457df9-7dd9-4fca-9362-ea4de26b0296
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688016(v=OCS.15)
ms:contentKeyID: 49733606
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c87426a3496e6def2ad65775f5dadb1a0141ae3f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400095"
---
# <a name="remove-sql-server-instances-and-databases-on-the-back-end-server"></a>バックエンド サーバー上の SQL Server インスタンスとデータベースの削除

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-10-19_

自分に依存している Lync Server 2010 を実行しているサーバーを削除した後、または Lync Server 2010 を実行しているサーバーを別のデータベースを使用するように再構成した後に、Microsoft SQL Server データベースとインスタンスを削除します。 このトピックでは、現在の SQL Server を廃止する場合、またはデータベースが使用されていないように表示されるように、Lync Server 2010 を実行している現在のサーバーを再構成する場合に、この手順を実行する必要があります。

アーカイブサーバーまたは監視サーバーのデータベースまたはインスタンスを削除するには、まずサーバーの役割を削除する必要があります。 同様に、フロントエンドプールのインスタンスまたはデータベースを削除するには、まず依存サーバーの役割を削除または再構成する必要があります。 これらの手順では、サーバーの併置されたデータベースと個別のインスタンスが区別されません。 プロシージャはデータベースの collocation の影響を受けません。

<div>

## <a name="in-this-section"></a>このセクション中

  - [フロントエンド プール用の SQL Server データベースの削除](remove-the-sql-server-database-for-a-front-end-pool.md)

  - [監視サーバー用の SQL Server データベースの削除](remove-the-sql-server-database-for-a-monitoring-server.md)

  - [アーカイブ サーバー用の SQL Server データベースの削除](remove-the-sql-server-database-for-an-archiving-server.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

