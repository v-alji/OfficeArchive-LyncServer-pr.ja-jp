---
title: 'Lync Server 2013: Kerberos 認証アカウント パスワードの設定'
description: 'Lync Server 2013: Kerberos 認証アカウントパスワードを設定します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up Kerberos authentication account passwords
ms:assetid: b435f88e-4a77-4be7-b7e5-c17484303b74
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412870(v=OCS.15)
ms:contentKeyID: 48185167
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 614b1411f9454c39843f4e69cabbfc3b02986e51
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423973"
---
# <a name="setting-up-kerberos-authentication-account-passwords-in-lync-server-2013"></a>Lync Server 2013 での Kerberos 認証アカウント パスワードの設定

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2010-11-03_

Kerberos 認証アカウントのコンピューターオブジェクトを作成したら、アカウントのパスワードを設定できます。 1つのサーバーで Kerberos アカウントのパスワードを設定するための Windows PowerShell コマンドレットを実行します。 Kerberos 認証用に作成したオブジェクトに対してパスワードを設定することができます。 パスワードは既知の値に設定できますが、既定ではランダムなパスワードになります。 パスワードは、そのアカウントを使用するすべての Kerberos 認証ソースで利用できます。 Kerberos アカウントのパスワードをセットアップして管理するには、Windows PowerShell コマンドレットを使用します。

<div>


> [!NOTE]  
> Kerberos アカウントオブジェクトはコンピューターオブジェクトですが、参照されている Windows PowerShell コマンドレットの操作には UserAccount パラメーターを使います。 これは間違いではありませんが、Kerberos アカウントの作成とメンテナンスで使用する場合のコマンドレットの動作です。



</div>

<div>

## <a name="in-this-section"></a>このセクション中

  - [Lync Server 2013 でのサーバーへの Kerberos 認証アカウント パスワードの設定](lync-server-2013-set-a-kerberos-authentication-account-password-on-a-server.md)

  - [Lync Server 2013 での Kerberos 認証アカウント パスワードと IIS との同期](lync-server-2013-synchronize-a-kerberos-authentication-account-password-to-iis.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

