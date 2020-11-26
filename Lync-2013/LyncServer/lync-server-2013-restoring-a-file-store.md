---
title: 'Lync Server 2013: ファイルストアを復元する'
description: 'Lync Server 2013: ファイルストアを復元しています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring a file store
ms:assetid: 89916fc6-31d3-4c7f-9eaf-c02584761ef4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202180(v=OCS.15)
ms:contentKeyID: 51541491
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 201c4b20f224fa3a25e931689e564410c60143e6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436252"
---
# <a name="restoring-a-file-store-in-lync-server-2013"></a>Lync Server 2013 でのファイルストアの復元

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2013-02-18_

標準エディション用のファイルストアは、通常 Standard Edition サーバーにあります。 Enterprise Edition のファイルストアは、通常はファイルサーバーまたはクラスターにあります。 次の手順では、ファイルストアを復元する方法について説明します。

<div>

## <a name="to-restore-a-file-store"></a>ファイルストアを復元するには

1.  ファイルストアに障害が発生した場合は、該当するファイルストアを $Backup から \\ ファイルサーバーまたは Standard Edition サーバー上のファイルストアの場所にコピーして、フォルダーを共有します。
    
    <div>
    

    > [!IMPORTANT]  
    > 復元されたファイルストアのパスとファイル名は、バックアップされたファイルストアとまったく同じである必要があります。これにより、ファイルを使用するコンポーネントがアクセスできるようになります。

    
    </div>

2.  必要に応じて、ファイルストアのアクセス制御リスト (Acl) を設定します。 コマンド ラインで次を入力します。
    
        Enable-CsTopology
    
    <div>
    

    > [!NOTE]  
    > この手順を実行する必要があるのは、復元プロセスでトポロジビルダーを実行していない場合のみです。

    
    </div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

