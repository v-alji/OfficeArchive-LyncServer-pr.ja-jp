---
title: 存続可能ブランチ アプライアンスの接続
description: Survivable Branch Appliance に接続します。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Connect a Survivable Branch Appliance
ms:assetid: fe3167e2-d1b1-4cd4-bf30-262e0e7d14e8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721948(v=OCS.15)
ms:contentKeyID: 49733886
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f5bbf9e1a4189d3c80d6dec449adf68b82cd3691
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398348"
---
# <a name="connect-a-survivable-branch-appliance"></a>存続可能ブランチ アプライアンスの接続

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-10-19_

すべての Survivable Branch Appliance (SBA) は、SBA のバックアップレジストラーとして機能するフロントエンドプールと関連付けられています。 フロントエンドプールが Lync Server 2013 に移行された場合、SBA は Lync Server 2010 のフロントエンドプールから切り離されている必要があります。このプールが Lync server 2013 に移行されると、SBA はアップグレードされたフロントエンドプールに再関連付けされます。 これには、トポロジビルダーで従来の Lync Server 2010 トポロジから SBA を削除してから、SBA を Lync Server 2013 トポロジに追加する作業が含まれます。 従来の Lync Server 2010 SBA のホームユーザーは、SBA をトポロジから削除する前に、別のフロントエンドプールに移動する必要があります。 SBA が Lync Server 2013 トポロジに追加されると、それらのユーザーを SBA に戻すことができます。 以下に、これらの手順の概要を示します。

1.  従来の SBA Lync Server 2010 上に置かれたブランチユーザーを別のフロントエンドプールに移動します。

2.  従来の Lync Server 2010 トポロジから SBA を削除して、既存のフロントエンドプールをバックアップレジストラーとして切断します。

3.  Lync Server 2013 トポロジに SBA を追加し、この新しいフロントエンドプールをバックアップレジストラーとして構成します。

4.  ブランチユーザーを新しい Lync Server 2013 SBA に移動します。

**Lync Server 2010 SBA ブランチサイトをトポロジに追加する**

1.  **トポロジビルダー** を開きます。

2.  左側のウィンドウで、[ **ブランチサイト**] を右クリックし、[ **新しいブランチサイト**] をクリックします。

3.  [ **新しい分岐サイトの定義** ] ダイアログボックスで、[ **名前**] をクリックし、ブランチサイトの名前を入力します。

4.  省略[ **説明**] をクリックし、ブランチサイトにわかりやすい説明を入力します。

5.  **[次へ]** をクリックします。

6.  省略[次の **新しいブランチサイトの定義** ] ダイアログボックスで、次のいずれかの操作を行います。
    
    1.  [ **市区町村**] をクリックし、ブランチサイトが配置されている都市の名前を入力します。
    
    2.  [ **状態/地域**] をクリックして、ブランチサイトが配置されている状態または地域の名前を入力します。
    
    3.  [ **国コード**] をクリックし、ブランチサイトが配置されている国/地域の2桁の通話コードを入力します。

7.  [ **次へ**] をクリックし、次のいずれかの操作を行います。
    
    1.  このサイトで Lync 2010 Survivable Branch Appliance または Server を使用している場合は、[ **このウィザードを終了するときに、新しい Survivable ウィザードを開く** ] チェックボックスをオフにしてください。 [**完了**] をクリックします。

8.  従来の Lync Server 2010 SBA を Lync Server 2013 フロントエンドプールに関連付けるには、次の操作を行います。
    
    1.  作成されたブランチサイトを展開します。
    
    2.  **Lync Server 2010** を右クリックし、[**新規作成**] をクリックします。
    
    3.  [ **Survivable Branch Appliance] を** クリックします。

9.  表示されるウィザードの指示に従います。 ウィザード項目の詳細について [は、「Lync Server 2013 で Survivable Branch Appliance または Server を定義する](lync-server-2013-define-a-survivable-branch-appliance-or-server.md)」を参照してください。
    
    <div>
    

    > [!NOTE]  
    > Lync Server 2010 Survivable Branch Appliance は、Lync Server 2010 Monitoring Store にのみ関連付けることができます。

    
    </div>

10. このサイトで Survivable Branch アプライアンスまたはサーバーを使っていない場合は、[ **このウィザードを終了するときに、新しい Survivable ウィザードを開く** ] チェックボックスをオフにして、[ **完了**] をクリックします。

11. トポロジに追加する各ブランチサイトについて、前の手順を繰り返します。

</div>

<span> </span>

</div>

</div>

</div>

