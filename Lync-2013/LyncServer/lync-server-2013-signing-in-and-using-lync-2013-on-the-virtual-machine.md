---
title: 'Lync Server 2013: 仮想マシン上の Lync 2013 へのサインインと使用'
description: 'Lync Server 2013: 仮想マシンにサインインして Lync 2013 を使用します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Signing in and using Lync 2013 on the virtual machine
ms:assetid: 6140fc19-5bef-4b58-9b0f-19112b5ecd00
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204948(v=OCS.15)
ms:contentKeyID: 48184318
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ad9a92d450fb9d60aed70617089d95280528892f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444702"
---
# <a name="signing-in-and-using-lync-2013-on-the-virtual-machine"></a>仮想マシン上の Lync 2013 へのサインインと使用

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-10-03_

VDI プラグインが有効になった後、ユーザーが Lync 2013 にサインインすると、次の手順が発生します。

1.  ユーザーは、仮想マシンで実行されている Lync 2013 クライアントに自分の資格情報を入力します。

2.  Lync は、VDI プラグインの可用性を検出した後、ユーザーに資格情報を再入力するように求めます。 このダイアログボックスでは、ユーザーが [ **パスワードを保存** する] チェックボックスをオンにして、以降のサインインで資格情報を入力する必要がないようにすることをお勧めします。

3.  Lync は、VDI プラグインとのペアリングを開始します。 ペアリングが完了する前に、クライアントは Lync ステータスバーに2つのアイコンを表示します。 左下のアイコンは、オーディオデバイスが利用できないことを示し、右下の [点滅] アイコンは、次のように、VDI ペアリングが進行中であることを示します。
    
    ![成功したペアリングを示す Lync VDI アイコン](images/JJ204948.303d618c-4bc8-41c4-8553-2475de0d395e(OCS.15).png "成功したペアリングを示す Lync VDI アイコン")  

4.  VDI ペアリングが成功すると、通話に使用されるオーディオ デバイスおよび VDI ペアリングが成功したことを示すアイコンに変わります。
    
    ![成功を示す Lync VDI ペアリングアイコン](images/JJ204948.57be3387-a3e5-4949-831e-f5ff9fcc5598(OCS.15).png "成功を示す Lync VDI ペアリングアイコン")  

5.  Lync と VDI プラグインをペアリングした後、ユーザーはローカルコンピューターに接続されている Lync 互換デバイスで自分のプレゼンスを見ることができます。 これで、ユーザーは通常の方法で通話を発信して応答することができます。

</div>

<span> </span>

</div>

</div>

</div>

