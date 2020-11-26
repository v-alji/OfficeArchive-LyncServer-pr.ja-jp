---
title: フロントエンド プールまたは Standard Edition サーバーの削除
description: フロントエンドプールまたは Standard Edition サーバーを削除します。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove Front End pool or Standard Edition server
ms:assetid: 83c39a36-49a1-4ac6-9cc5-b0e441b1fdec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688115(v=OCS.15)
ms:contentKeyID: 49733713
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c878d56b073558f4f4b50f31b6742fd581c80241
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440277"
---
# <a name="remove-front-end-pool-or-standard-edition-server"></a>フロントエンド プールまたは Standard Edition サーバーの削除

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-10-04_

このトピックでは、フロントエンドプールまたは標準エディションのフロントエンドサーバーを削除する手順について説明します。 フロントエンドプールを削除する場合は、プールに属している各フロントエンドサーバーをプール削除プロセスの一部として削除します。 Standard Edition のフロントエンドサーバーを削除する場合は、トポロジビルダーから SQL ストアの定義を削除する必要があります。

<div>

## <a name="to-remove-a-front-end-server-pool"></a>フロントエンドサーバープールを削除するには

1.  トポロジビルダーを開きます。

2.  Lync Server 2010 ノードに移動します。

3.  **Enterprise Edition のフロントエンド** プールを展開し、フロントエンドプールを展開して、削除するフロントエンドプールを右クリックし、[**削除**] をクリックします。

4.  トポロジを公開し、レプリケーションの状態を確認してから、必要に応じて Lync Server 展開ウィザードを実行します。

</div>

<div>

## <a name="to-remove-a-standard-edition-front-end-server"></a>Standard Edition フロントエンドサーバーを削除するには

1.  トポロジビルダーを開きます。

2.  Lync Server 2010 ノードに移動します。

3.  **Standard Edition のフロントエンド** サーバーを展開し、削除するフロントエンドサーバーを右クリックして、[**削除**] をクリックします。

4.  [ **Sql ストア**] を展開し、Standard Edition フロントエンドサーバーに関連付けられている sql Server データベースを右クリックし、[ **削除**] をクリックします。
    
    <div>
    

    > [!IMPORTANT]  
    > 併置された SQL Server データベースの定義は、Standard Edition のフロントエンドサーバーから削除する必要があります。

    
    </div>

5.  トポロジを公開し、レプリケーションの状態を確認してから、必要に応じて Lync Server 展開ウィザードを実行します。

</div>

</div>

<span> </span>

</div>

</div>

</div>

