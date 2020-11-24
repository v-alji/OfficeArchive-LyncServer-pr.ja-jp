---
title: 'Lync Server 2013: トポロジの公開'
description: 'Lync Server 2013: トポロジを公開します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Publish your topology
ms:assetid: bfed3829-7a54-4b5c-a7cb-28871acd35e7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412935(v=OCS.15)
ms:contentKeyID: 48185287
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f4d27d2d3644eb1f174e2f3fab47197f2c122a97
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399038"
---
# <a name="publish-your-topology-in-lync-server-2013"></a>Lync Server 2013 でのトポロジの公開

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-09-08_

トポロジビルダーを使用してトポロジを構築するたびに、データを使用して Lync Server 2013 を展開できるように、トポロジを中央管理ストアのデータベースに発行する必要があります。 トポロジを公開するには、次の手順を使用します。

<div>

## <a name="to-publish-the-topology"></a>トポロジを公開するには

1.  トポロジビルダーを開始します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server Topology Builder**] の順にクリックします。

2.  [トポロジビルダー] のコンソールツリーで、[ **Lync 2013**] を右クリックし、[ **トポロジの公開**] をクリックします。

3.  ウィザードの [**ようこそ**] ページで、[**次へ**] をクリックします。

4.  **トポロジビルダーで CMS ストア** のページが見つかったら、[**次へ**] をクリックします。

5.  [**他のデータベースの作成**] ページで、[**次へ**] をクリックします。

6.  状態がデータベースの作成に成功したことを示す場合は、次の操作を行います。
    
      - ログを表示するには、[**ログの表示**] をクリックします。
    
      - ウィザードを閉じるには、[**完了**] をクリックします。
        
        <div>
        

        > [!IMPORTANT]  
        > エッジサーバーまたはエッジプールの新規インストールの場合は、既存のフロントエンドサーバー、フロントエンドプール、または Standard Edition サーバーから Edge Server 構成をエクスポートする必要があります。 構成をエクスポートするには、「 <A href="lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md">Lync Server 2013 トポロジをエクスポートして、edge インストール用の外部メディアにコピーする</A>」を参照してください。 Lync Server 展開ウィザードを通じて、エッジサーバーのセットアップおよび展開フェーズ中に、外部メディアまたはネットワーク共有から構成ファイルをインポートします。<BR>エッジサーバーが動作していて、ローカル構成管理ストアデータベースが内部展開によってレプリケートされると、それ以降の Lync Server 2013 構成の更新は公開され、エッジサーバーにレプリケートされます。

        
        </div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

