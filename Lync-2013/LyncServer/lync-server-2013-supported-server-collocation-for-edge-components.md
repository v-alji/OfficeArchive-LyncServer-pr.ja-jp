---
title: 'Lync Server 2013: エッジ コンポーネントのサポートされるサーバーの併置'
description: 'Lync Server 2013: edge コンポーネント用にサポートされているサーバーの collocation。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Supported server collocation for edge components
ms:assetid: 435c4dd8-36af-4b71-9b88-3ffcf0fc5c65
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425934(v=OCS.15)
ms:contentKeyID: 48183978
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7bf253e5210e077ca62b3d00f7f130d54d8392a5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423639"
---
# <a name="supported-server-collocation-for-edge-components-in-lync-server-2013"></a>Lync Server 2013 での、エッジ コンポーネントのサポートされるサーバーの併置

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-09-08_

アクセスエッジサービス、Web 会議エッジサービス、A/V Edge サービス、および XMPP プロキシサービスは、エッジサーバーに併置されています。 次のサーバーは、外部ユーザーアクセスに必要な機能を提供し、専用サーバーとして展開する必要があります。

  - エッジ サーバー

  - 監督 (オプション)

  - リバース プロキシ

<div>


> [!IMPORTANT]  
> リバースプロキシは、Lync Server 2013 のみを提供するための専用である必要はありません。 たとえば、Lync Server Web サービスを公開するためのサービスを提供し、Lync Server にまったく関係のない別の Web サイトに公開された Web サイトを同時に提供することができます。 他のサービスをサポートするために既に境界ネットワーク内に逆プロキシサーバーがある場合は、Lync Server 2013 で使うことができます。



</div>

</div>

<span> </span>

</div>

</div>

</div>

