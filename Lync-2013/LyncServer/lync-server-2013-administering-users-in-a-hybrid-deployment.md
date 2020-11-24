---
title: 'Lync Server 2013: ハイブリッド展開でユーザーを管理する'
description: 'Lync Server 2013: ハイブリッド展開でユーザーを管理します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Administering users in a hybrid deployment
ms:assetid: 6924ed7b-30a9-4be7-b952-90655625f2c8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204967(v=OCS.15)
ms:contentKeyID: 48184381
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7f1d7684a9f56eb013574a985ded0313378621c2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398007"
---
# <a name="administering-users-in-a-hybrid-lync-server-2013-deployment"></a>ハイブリッド Lync Server 2013 展開でユーザーを管理する

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2014-05-29_

Microsoft 365 管理センターで使用可能なユーザー管理機能を使って、Lync Online に移行したユーザーのユーザー設定とポリシーを管理できます。 管理タスクを実行するには、テナント管理者アカウントを使用してサインインする必要があります。

<div>

## <a name="moving-users-back-to-on-premises"></a>ユーザーをオンプレミスに戻す

<div class="">


> [!IMPORTANT]  
> このセクションは、Lync をオンプレミスで作成して有効にし、オンプレミスの展開から Lync Online に移行したユーザーにのみ適用されます。 Lync Online で作成されたユーザーを移動する場合 (オンプレミスの展開で Lync に対して有効にしていない場合) は、「lync <A href="lync-server-2013-moving-users-from-lync-online-to-lync-on-premises.md">Online のユーザーを Lync Server 2013 で社内の lync に移動</A>する」を参照してください。



</div>

  - Lync Online からオンプレミスの Lync にユーザーを戻すには、次のコマンドレットを実行します。
    
       ```PowerShell
        $cred=Get-Credential
       ```
    
       ```PowerShell
        Move-CsUser -Identity username@contoso.com -Target localpool.contoso.com -Credential $cred -HostedMigrationOverrideUrl <URL>
       ```

**HostedMigrationOverrideUrl** パラメーターの URL には、ホスティング型移行サービスが実行されているプールへの URL を次の形式で指定する必要があります。

Https:// \<Pool FQDN\> /HostedMigration/hostedmigrationService.svc. ホスティング型移行サービスの URL は、Microsoft 365 または Office 365 の組織アカウントの Lync Online コントロールパネルの URL を表示することで確認できます。

**Microsoft 365 または Office 365 組織のホスティング型移行サービスの URL を確認するには**

1.  組織に管理者としてログインします。

2.  **Lync 管理センター** を開きます。

3.  **Lync 管理センター** が表示されたら、アドレスバーの URL を選択して **lync.com** にコピーします。 URL は、次のような書式です。
    
    `https://webdir0a.online.lync.com/lscp/?language=en-US&tenantID=`

4.  URL の **webdir** を **admin** に置き換えると、次のようになります。
    
    `https://admin0a.online.lync.com`

5.  URL に以下の文字列を付加します。**/HostedMigration/hostedmigrationservice.svc**
    
    以上の手順によって、**HostedMigrationOverrideUrl** の値を持った URL は次のようになります。
    
    `https://admin0a.online.lync.com/HostedMigration/hostedmigrationservice.svc`

</div>

</div>

<span> </span>

</div>

</div>

</div>

