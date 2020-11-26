---
title: BackCompatSite を削除する
description: BackCompatSite を削除します。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove BackCompatSite
ms:assetid: 039650e3-541b-45c2-a682-c4fa08423118
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204637(v=OCS.15)
ms:contentKeyID: 48183265
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 809324320ec1869ac0c9d324b8fc270a3cf8f174
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440306"
---
# <a name="remove-backcompatsite"></a>BackCompatSite を削除する

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-09-28_

すべてのプールが非アクティブ化され、すべてのエッジサーバーがアンインストールされたら、トポロジビルダーの結合ウィザードを実行して、 **BackCompatSite** を削除します。

<div>

## <a name="to-remove-backcompat-site-from-topology-builder"></a>Topology Builder から BackCompat サイトを削除するには

1.  トポロジビルダーから既存の展開を開きます。

2.  [ **操作** ] メニューで、[ **2007 R2 トポロジのマージ**] をクリックします。

3.  [**次へ**] をクリックして続行します。

4.  [ **レガシ edge の指定** ] ページで、エッジサーバーの一覧が空であることを確認します。 リストが空でない場合は、[ **削除** ] ボタンを使用して、すべてのレガシーエッジサーバーを削除してから、[ **次へ**] をクリックします。
    
    ![トポロジの結合ウィザード、[Edge セットアップ] ページを指定する](images/JJ204637.fb35a59a-711e-4259-b177-7311df1fed3c(OCS.15).jpg "トポロジの結合ウィザード、[Edge セットアップ] ページを指定する")  

5.  [ **内部 SIP ポート設定の指定** ] ページで、[ **次へ**] をクリックします。

6.  [ **概要** ] ページで、[ **次** へ] をクリックして、トポロジの結合を開始して、従来のサイトを削除します。

7.  [ **状態** ] 列で、値が **成功** していることを確認し、[ **完了** ] をクリックしてウィザードを閉じます。

8.  [Topology Builder] の左側のウィンドウで、[BackCompatSite] を展開して、サーバーが一覧に表示されていないことを確認します。

9.  **BackCompatSite** を右クリックし、[**削除**] をクリックします。

10. [ **トポロジビルダー**] で、トップノードの **Lync Server** を選択します。

11. [ **アクション** ] メニューで、[ **発行トポロジ** ] を選択し、[ **次へ**] をクリックします。

12. **発行ウィザード** が完了したら、[**完了**] をクリックしてウィザードを閉じます。

</div>

</div>

<span> </span>

</div>

</div>

</div>

