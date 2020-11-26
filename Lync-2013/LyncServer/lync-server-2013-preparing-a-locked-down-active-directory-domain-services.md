---
title: 'Lync Server 2013: ロックダウンされた Active Directory ドメイン サービスの準備'
description: 'Lync Server 2013: ロックダウンされた Active Directory ドメインサービスを準備しています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing a locked-down Active Directory Domain Services
ms:assetid: 68bde963-3fa3-4102-88d6-ac931c1dd2d7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398492(v=OCS.15)
ms:contentKeyID: 48184377
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4aea04b138de2630935713eda7cbef9e4d21572a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424227"
---
# <a name="preparing-a-locked-down-active-directory-domain-services-in-lync-server-2013"></a>Lync Server 2013 でのロックダウンされた Active Directory ドメイン サービスの準備

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-05-14_

組織は、セキュリティリスクを軽減するために Active Directory ドメインサービスをロックダウンすることがよくあります。 ただし、ロックダウンされた Active Directory 環境では、Lync Server 2013 で必要なアクセス許可を制限できます。 Lync Server 2013 用のロックダウン Active Directory 環境を適切に準備するには、いくつかの追加の考慮事項と手順が必要です。

ロックダウンされた Active Directory 環境でアクセス許可が制限される一般的な方法には、次の2つがあります。

  - 認証済みユーザーアクセス制御エントリ (Ace) がコンテナーから削除されます。

  - ユーザー、連絡先、InetOrgPerson、またはコンピューターのオブジェクトのコンテナーでは、アクセス許可の継承が無効になっています。

<div>

## <a name="in-this-section"></a>このセクション中

  - [Lync Server 2013 で認証済みユーザーのアクセス許可が削除されている](lync-server-2013-authenticated-user-permissions-are-removed.md)

  - [Lync Server 2013 のコンピューター、ユーザー、または InetOrgPerson のコンテナーでアクセス許可の継承が無効になっている](lync-server-2013-permissions-inheritance-is-disabled-on-computers-users-or-inetorgperson-containers.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

