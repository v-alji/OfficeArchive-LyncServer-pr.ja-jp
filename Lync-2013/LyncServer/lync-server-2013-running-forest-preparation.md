---
title: 'Lync Server 2013: フォレストの準備の実行'
description: 'Lync Server 2013: フォレストの準備を実行しています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Running forest preparation
ms:assetid: 9d62f7be-bcfe-421d-8d8a-225567102a35
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412732(v=OCS.15)
ms:contentKeyID: 48184991
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ad3ef2d7583d541701d6606946ca1df1bbd8cf23
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442216"
---
# <a name="running-forest-preparation-for-lync-server-2013"></a>Lync Server 2013 でのフォレストの準備の実行

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-10-29_

セットアップまたは Lync Server 管理シェルコマンドレットを使用して、フォレストを準備することができます。 フォレストを準備するコマンドレットでは、 **CsAdForest を有効** にします。

フォレストを準備したら、ドメインの準備を実行する前に、グローバル設定がレプリケートされていることを確認する必要があります。

<div>

## <a name="to-use-setup-to-prepare-the-forest"></a>セットアップを使用してフォレストを準備するには

1.  フォレストルートドメインの Enterprise Admins グループのメンバーとしてドメインに参加しているコンピューターにログオンします。

2.  Lync Server 2013 のインストールフォルダーまたはメディアから、Setup.exe を実行して展開ウィザードを開始します。

3.  [**Active Directory の準備**] をクリックして、展開状態が判別されるまで待ちます。

4.  **手順 3: 現在のフォレストを準備** するには、[**実行**] をクリックします。

5.  [ **フォレストの準備** ] ページで、[ **次へ**] をクリックします。
    
    <div>
    

    > [!NOTE]  
    > フォレストの準備 Lync Server 2013 のユニバーサルグループを配置する場所を選ぶことができます。 組織の要件と一致する配置先を選択してください。

    
    </div>

6.  [**コマンドを実行しています**] ページで [**タスク状態: 完了**] を見つけて、[**ログの表示**] をクリックします。

7.  [ **アクション** ] 列の [ **forest Prep**] を展開し、 **\<Success\>** 各タスクの最後の実行結果を確認して、フォレストの準備が正常に完了したことを確認します。次に、[ **完了**] をクリックします。

8.  Active Directory のレプリケーションが完了するまで待機するか、フォレストルートドメインコントローラーの **Active Directory サイトとサービス** スナップインに記載されているすべてのドメインコントローラーに対して強制的にレプリケーションを実行してから、ドメインの準備を実行します。 すべての Active Directory サイトのドメインコントローラー間で強制的にレプリケーションを実行して、サイト内での複製が分単位で行われるようにします。

</div>

<div>

## <a name="to-use-cmdlets-to-prepare-the-forest"></a>コマンドレットを使用してフォレストを準備するには

1.  フォレストルートドメインの Domain Admins グループのメンバーとしてドメインに参加しているコンピューターにログオンします。

2.  Lync Server のコアコンポーネントは、次のようにインストールします。
    
    1.  Lync Server 2013 のインストールフォルダーまたはメディアで Setup.exe を実行して、Lync Server 展開ウィザードを開始します。
    
    2.  Microsoft Visual C++ 再頒布可能パッケージをインストールするかどうかを確認するメッセージが表示されたら、[ **はい**] をクリックします。
    
    3.  [Lync Server 2013 セットアップ] ダイアログボックスで、Lync Server ファイルをインストールする場所を入力するように求められます。 既定の場所を選ぶか、目的の場所を **参照** し、[ **インストール**] をクリックします。
    
    4.  [使用許諾契約] ページで、[ **使用許諾契約書に同意** します] をオンにし、[ **OK]** をクリックします。 インストーラーは、Lync Server 2013 コアコンポーネントをインストールします。

3.  Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。

4.  次のコマンドレットを実行します。
    
        Enable-CsAdForest [-GroupDomain <FQDN of the domain in which to create the universal groups>]
    
    次に例を示します。
    
        Enable-CsAdForest -GroupDomain domain1.contoso.com 
    
    GroupDomain パラメーターを指定しない場合、既定値はローカルドメインです。 ユニバーサルグループが、既定のドメインではないドメインで以前に作成された場合は、GroupDomain パラメーターを明示的に指定する必要があります。

5.  Active Directory のレプリケーションが完了するまで待機するか、フォレストルートドメインコントローラーの **Active Directory サイトとサービス** スナップインに記載されているすべてのドメインコントローラーに対して強制的にレプリケーションを実行してから、ドメインの準備を実行します。

6.  フォレストの準備が正常に完了したことを確認します。 次のコマンドレットを実行します。
    
        Get-CsAdForest 
    
    フォレストの準備が正常に完了した場合、このコマンドレットは **LC \_ FORESTSETTINGS \_ STATE \_** の値を返します。

</div>

<div>

## <a name="see-also"></a>関連項目


[コマンドレットの使用による Lync Server 2013 のフォレストの準備のリバース](lync-server-2013-using-cmdlets-to-reverse-forest-preparation.md)  


[Lync Server 2013 でのフォレストの準備](lync-server-2013-preparing-the-forest.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

