---
title: 'Lync Server 2013: グループ通話の集配番号をユーザーに割り当てる'
description: 'Lync Server 2013: グループ通話の集配番号をユーザーに割り当てます。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assign Group Call Pickup numbers to users
ms:assetid: b8e79275-8e7e-4799-b908-f34f61df22f0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945647(v=OCS.15)
ms:contentKeyID: 51541508
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d550b4556af427e11e99ffb26fb2a6c34d019490
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438345"
---
# <a name="assign-group-call-pickup-numbers-to-users-in-lync-server-2013"></a>グループ通話の集配番号を Lync Server 2013 のユーザーに割り当てる

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2013-01-30_

グループ通話のピックアップグループ番号をコールパークの軌道テーブルに追加したら、グループをユーザーに割り当てることができます。 セカンダリ拡張機能のアクティブ化 (SEFAUtil) リソースキットツールを使用して、ユーザーに通話ピックアップグループを割り当てます。

<div>


> [!NOTE]  
> ハイブリッド展開では、オンラインのユーザーにグループの通話ピックアップグループを割り当てないでください。 自宅のユーザーはグループ通話のピックアップに参加できません。 つまり、オンラインに所属するユーザーへの呼び出しを他のユーザーが応答することや、他のユーザーへの呼び出しをオンラインに所属するユーザーが応答することはできません。



</div>

<div>

## <a name="to-assign-a-group-call-pickup-group-to-a-user"></a>グループ通話のピックアップグループをユーザーに割り当てるには

1.  SEFAUtil ツールをインストールしたコンピューターに管理者権限でログオンします。

2.  コマンド ラインで、次のコマンドを実行します。
    
        SEFAUtil.exe sip:<sip address of user> /server:<pool FQDN> /enablegrouppickup:<group number>
    
    例:
    
        SEFAUtil.exe katarina@contoso.com /server:pool01.contoso.com /enablegrouppickup:199

</div>

<div>

## <a name="see-also"></a>関連項目


[Lync Server 2013 のユーザーに対してグループ通話のピックアップを有効にする](lync-server-2013-enable-group-call-pickup-for-users.md)  
[Lync Server 2013 のユーザーに対してグループ通話のピックアップを無効にする](lync-server-2013-disable-group-call-pickup-for-users.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

