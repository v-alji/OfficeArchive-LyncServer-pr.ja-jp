---
title: 'Lync Server 2013: グループ通話のピックアップをユーザーに対して有効にし、グループ番号を割り当てる'
description: 'Lync Server 2013: グループ通話のピックアップを有効にして、グループ番号を割り当てることができます。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable Group Call Pickup for users and assign a group number
ms:assetid: c33bb6c2-d43b-4fb6-a0fa-6d82a7b09abe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945650(v=OCS.15)
ms:contentKeyID: 51541517
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a03fcb20bfd88842dc8b29100b9ece595bf76254
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428924"
---
# <a name="enable-group-call-pickup-for-users-in-lync-server-2013-and-assign-a-group-number"></a>Lync Server 2013 のユーザーに対してグループ通話のピックアップを有効にし、グループ番号を割り当てる

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2013-01-30_

コールパークの軌道の表に通話集配グループ番号を追加した後、グループ番号をユーザーに割り当て、グループ通話のピックアップを有効にします。 セカンダリ拡張機能のアクティブ化 (SEFAUtil) リソースキットツールを使用して、グループ番号を割り当て、グループ通話のピックアップを有効にします。

<div>


> [!NOTE]  
> ハイブリッド展開では、オンラインのユーザーにグループの通話ピックアップグループを割り当てないでください。 自宅のユーザーはグループ通話のピックアップに参加できません。 つまり、オンラインに所属するユーザーへの呼び出しを他のユーザーが応答することや、他のユーザーへの呼び出しをオンラインに所属するユーザーが応答することはできません。



</div>

<div>

## <a name="to-assign-a-group-number-and-enable-group-call-pickup-for-a-user"></a>グループ番号を割り当てて、ユーザーに対してグループ通話のピックアップを有効にするには

1.  SEFAUtil ツールをインストールしたコンピューターに管理者権限でログオンします。

2.  コマンド ラインで、次のコマンドを実行します。
    
        SEFAUtil.exe sip:<sip address of user> /server:<pool FQDN> /enablegrouppickup:<group number>
    
    たとえば、グループ番号 199 をユーザーに割り当てるには
    
        SEFAUtil.exe katarina@contoso.com /server:pool01.contoso.com /enablegrouppickup:199 

</div>

<div>

## <a name="see-also"></a>関連項目


[Lync Server 2013 のユーザーに対してグループ通話のピックアップを無効にする](lync-server-2013-disable-group-call-pickup-for-users.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

