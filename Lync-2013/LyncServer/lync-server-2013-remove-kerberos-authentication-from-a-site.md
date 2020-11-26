---
title: 'Lync Server 2013: サイトからの Kerberos 認証の削除'
description: 'Lync Server 2013: サイトから Kerberos 認証を削除します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Remove Kerberos authentication from a site
ms:assetid: 93171b02-bb36-42dc-943d-86d9dde45b59
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398749(v=OCS.15)
ms:contentKeyID: 48184806
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2a3d9100d07d37e98800cfce106bc75fcfaeaa59
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436385"
---
# <a name="in-lync-server-2013-remove-kerberos-authentication-from-a-site"></a>Lync Server 2013 でのサイトからの Kerberos 認証の削除

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-01-16_

この手順を正常に完了するには、RTCUniversalServerAdmins グループのメンバーであるユーザーとしてログオンする必要があります。

サイトからの Kerberos 認証を削除する必要がある場合、またはサイトを削除する必要がある場合は、 **CsKerberosAccountAssignment** コマンドレットを使用して、サイトから kerberos 認証アカウントの割り当てを削除する必要があります。 次の手順を使用して、Kerberos 認証アカウントの割り当てを削除します。これにより、サイト内のすべてのコンピューターから課題が削除されます。

<div class=" ">


> [!WARNING]  
> Kerberos 対応のアカウントを完全に無効にする場合は、割り当てを削除した後で Active Directory ユーザーとコンピューターを使用して Active Directory ドメインサービスから削除する必要があります。 今後このオブジェクトを使う予定がある場合は、Active Directory オブジェクトを保持しておくことをお勧めします。



</div>

<div>

## <a name="to-remove-kerberos-authentication-from-a-site"></a>サイトから Kerberos 認証を削除するには

1.  RTCUniversalServerAdmins グループのメンバーとして、Lync Server 2013 を実行しているドメイン内のコンピューター、または管理ツールがインストールされているコンピューターにログオンします。

2.  Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。

3.  コマンドラインで、次の2つのコマンドを実行します。
    
       ```PowerShell
        Remove-CsKerberosAccountAssignment -Identity "site:SiteName"
       ```
    
       ```PowerShell
        Enable-CsTopology
       ```
    
    次に例を示します。
    
       ```PowerShell
        Remove-CsKerberosAccountAssignment -Identity "site:Redmond"
       ```
    
       ```PowerShell
        Enable-CsTopology
       ```
    
    <div class=" ">
    

    > [!IMPORTANT]  
    > アカウントの追加やアカウントの削除など、Kerberos 認証を変更した後は、Lync Server 管理シェルのコマンドプロンプトから、 <STRONG>Enable-CsTopology</STRONG> 方法を実行する必要があります。

    
    </div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

