---
title: 'Lync Server 2013: セットアップのアクセス許可の委任'
description: 'Lync Server 2013: セットアップのアクセス許可を委任します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delegate setup permissions
ms:assetid: 9dca1683-4c69-4534-8ebe-6bd635cbae49
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412735(v=OCS.15)
ms:contentKeyID: 48184997
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a7038cf729bad459dbcd2a84a308b14aa56b68dd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398234"
---
# <a name="delegate-setup-permissions-in-lync-server-2013"></a>Lync Server 2013 でのセットアップのアクセス許可の委任

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2014-02-05_

Lync Server 2013 を展開しているユーザーまたはグループに Domain Admins グループのメンバーシップを許可しない場合は、RTCUniversalServerAdmins グループのメンバーを有効にして、Lync Server 2013 を実行しているサーバーで、 **CsTopology** Windows PowerShell コマンドレットを実行します。 既定では、RTCUniversalServerAdmins グループのメンバーはこのコマンドレットを実行することはできません。 Lync Server を実行しているサーバーで **Enable-CsTopology** 機能を実行するに **は、管理** 者の権限とアクセス許可を付与することができます。これには、lync server 2013 を実行しているサーバーのコンピューターオブジェクトがある組織単位 (OU) を指定します。

Lync Server をインストールするときに実行されるドメインの準備により、RTCUniversalServerAdmins グループのメンバーが Enable-CsTopology コマンドレットを実行するためのアクセス許可が自動的に追加されることはありません。 つまり、トポロジを有効にするには、既定でドメイン管理者である必要があることを意味します。 RTCUniversalServerAdmins グループのメンバーにトポロジを有効にする権利を付与するには、Grant-CsSetupPermissions コマンドレットを実行する必要があります。 さらに、Lync Server を実行しているコンピューターを格納する各 Active Directory コンテナーに対して、このコマンドレットを実行する必要があります。

このコマンドレットは、RTCUniversalServerAdmins グループに対してのみアクセス許可を付与することに注意してください。コマンドレットを使用して、他のセキュリティグループまたは個々のユーザーに権限を付与することはできません。

<div>


> [!NOTE]  
> <STRONG>Enable-CsTopology</STRONG> は、RTCUniversalServerAdmins group メンバーが Lync Server 2013 をセットアップして展開できるようにするためのキーコマンドレットです。



</div>

<div>

## <a name="to-add-the-ability-to-run-enable-cstopology-to-the-rtcuniversalserveradmins-group"></a>Enable-CsTopology を実行する機能を RTCUniversalServerAdmins グループに追加するには

1.  委任されたユーザーが実行 **可能な** ドメインの domain Admins グループのメンバーとしてサーバーにログオンします。

2.  Lync Server 2013 管理シェルを開きます。 Lync Server 2013 管理シェルは、各フロントエンドサーバーまたは Lync Server 2013 管理ツールがインストールされているすべてのコンピューターに自動的にインストールされます。 Lync Server 2013 管理シェルの詳細については、「運用ドキュメントの [Lync server 2013 管理シェル](lync-server-2013-lync-server-management-shell.md) 」を参照してください。

3.  Lync Server 2013 管理シェルから次のコマンドレットを実行します。
    
        Grant-CsSetupPermission -ComputerOU <DN of the OU> -Domain <Domain FQDN>
    
    <div>
    

    > [!NOTE]  
    > OU が最上位レベルではない場合は、完全なドメイン名を指定する必要があります。

    
    </div>
    
    次の例では、OU は contoso.com ドメイン内の "Lync Servers" です。
    
        Grant-CsSetupPermission -ComputerOU "OU=Lync Servers" -Domain contoso.com

</div>

</div>

<span> </span>

</div>

</div>

</div>

