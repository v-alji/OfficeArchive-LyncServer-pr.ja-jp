---
title: 'Lync Server 2013: Kerberos 認証の設定'
description: 'Lync Server 2013: Kerberos 認証を設定する。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up Kerberos authentication
ms:assetid: dd8009ef-6265-4cc0-b2c7-e474cd1f4b09
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398976(v=OCS.15)
ms:contentKeyID: 48185601
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bb461968bc073edbfe640f609257f3e84c192461
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441719"
---
# <a name="setting-up-kerberos-authentication-in-lync-server-2013"></a>Lync Server 2013 での Kerberos 認証の設定

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2013-02-21_

Lync Server 2013 は、Web サービスの NTLM 認証と Kerberos 認証をサポートしています。 Office Communications Server 2007 および Office Communications Server 2007 R2 では、サービスプリンシパル名 (SPN) をユーザーアカウントに割り当てて、認証プリンシパルとして機能させることができるようにするために、既定の RTCComponentService と RTCService をユーザーアカウントとして使用しました。 Lync Server は NetworkService を使って Web サービスを実行します。 NetworkService には、Spn を割り当てることはできません。

Active Directory オブジェクトに Spn を保持する必要がないという問題を解決するために、Lync Server コントロールパネルでは、この目的でコンピューターアカウントオブジェクトを使うことができます。 コンピューターアカウントオブジェクトは、Spn を保持することができ、パスワードの有効期限は適用されません。これは、以前のバージョンでのユーザーアカウントの使用に関する問題です。

Kerberos 認証を提供するようにコンピューターオブジェクトを構成するには、Windows PowerShell コマンドレットを使用します。

<div>

## <a name="in-this-section"></a>このセクション中

  - [Lync Server 2013 で Kerberos 認証を有効にするための前提条件](lync-server-2013-prerequisites-for-enabling-kerberos-authentication.md)

  - [Lync Server 2013 での Kerberos 認証アカウントの作成](lync-server-2013-create-a-kerberos-authentication-account.md)

  - [Lync Server 2013 での、サイトへの Kerberos 認証アカウントの割り当て](lync-server-2013-assign-a-kerberos-authentication-account-to-a-site.md)

  - [Lync Server 2013 での Kerberos 認証アカウント パスワードの設定](lync-server-2013-setting-up-kerberos-authentication-account-passwords.md)

  - [Lync Server 2013 での他のサイトへの Kerberos 認証の追加](lync-server-2013-add-kerberos-authentication-to-other-sites.md)

  - [Lync Server 2013 でのサイトからの Kerberos 認証の削除](lync-server-2013-remove-kerberos-authentication-from-a-site.md)

  - [Lync Server 2013 での Kerberos 認証の状態と割り当てについてのテストおよびレポート](lync-server-2013-testing-and-reporting-the-status-and-assignment-of-kerberos-authentication.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

