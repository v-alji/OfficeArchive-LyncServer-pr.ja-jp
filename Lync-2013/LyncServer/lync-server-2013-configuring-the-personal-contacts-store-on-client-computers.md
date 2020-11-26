---
title: 'Lync Server 2013: クライアントコンピューターで個人用連絡先ストアを構成する'
description: 'Lync Server 2013: クライアントコンピューターで個人用の連絡先ストアを構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring the personal contacts store on client computers
ms:assetid: ec69a6cb-07f2-4057-9544-55035f83eeae
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721922(v=OCS.15)
ms:contentKeyID: 49733857
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c1040b3eb9aa38e3e0c537d690b9292ab8f1ead2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432521"
---
# <a name="configuring-the-personal-contacts-store-on-client-computers-for-lync-server-2013"></a>Lync Server 2013 のクライアントコンピューターで個人用連絡先ストアを構成する

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2014-02-05_

Microsoft Lync Server 2013 と Microsoft Exchange Server 2013 を統合する場合は、Microsoft Lync 2010 を実行しているすべてのクライアントコンピューターで個人用連絡先ストアを構成することをお勧めします。 特に、Exchange を個人用連絡先ストアとして使用するように Lync を構成し、同時にユーザーがその決定を上書きできないようにする必要があります。 そのためには、各クライアント コンピューターでレジストリ値を作成して構成します。

これは、Lync 2013 を実行しているコンピューターでは必要ありません。

1 台のコンピューターでこの値を構成するには、次の手順を実行します。

1.  クライアント コンピューターで [**スタート**] ボタンをクリックし、[**ファイル名を指定して実行**] をクリックします。

2.  [**ファイル名を指定して実行**] ダイアログ ボックスで「regedit」と入力して、Enter キーを押します。

3.  レジストリエディターで、[ **HKEY \_ ローカル \_ コンピューター**]、[ **ソフトウェア**]、[ **ポリシー**] の順に展開し、[ **Microsoft**]、[ **Communicator**] の順に展開します。

4.  [**Communicator**] を右クリックし、[**新規**] をポイントし、[**DWORD (32 ビット) 値**] をクリックします。

5.  新しい値を作成した後に「**PersonalContactStoreOverride**」と入力し、Enter キーを押して値の名前を変更します。

6.  PersonalContactStoreOverride の値が 0 に設定されていることを確認し、レジストリ エディターを閉じます。

複数のコンピューターでこれと同じ変更をする必要がある場合は、カスタム グループ ポリシー オブジェクトを作成します。 詳細については、のグループポリシードキュメントを参照してください [https://go.microsoft.com/fwlink/p/?LinkId=268543](https://go.microsoft.com/fwlink/p/?linkid=268543) 。

</div>

<span> </span>

</div>

</div>

</div>

