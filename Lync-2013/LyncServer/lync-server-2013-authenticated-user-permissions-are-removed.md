---
title: 'Lync Server 2013: 認証済みユーザーのアクセス許可が削除されている'
description: 'Lync Server 2013: 認証されたユーザーのアクセス許可が削除されます。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Authenticated user permissions are removed
ms:assetid: 5fcd70a5-813a-4076-9bb6-5b0d47505038
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398425(v=OCS.15)
ms:contentKeyID: 48184304
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 59da0ec893395405010afdd0263bd6be5d646881
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438156"
---
# <a name="authenticated-user-permissions-are-removed-in-lync-server-2013"></a>Lync Server 2013 で認証済みユーザーのアクセス許可が削除されている

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2013-02-21_

ロックダウンされた Active Directory 環境では、認証済みユーザーアクセス制御エントリ (Ace) は、ユーザー、構成、システム、およびユーザーオブジェクトが保存されている組織単位 (Ou) を含む、既定の Active Directory コンテナーから削除されます。 認証済みユーザー Ace を削除すると、Active Directory 情報への読み取りアクセスができなくなります。 ただし、Ace を削除すると、ユーザーがドメインの準備を実行できるように、これらのコンテナーの読み取りアクセス許可に依存するため、Lync Server 2013 の問題が発生します。

この状況では、ドメインの準備、サーバーのアクティブ化、プールの作成を実行するために必要な Domain Admins グループのメンバーシップが、既定のコンテナーに格納されている Active Directory 情報への読み取りアクセス許可を付与することはなくなりました。 必要なフォレストの準備手順が完了していることを確認するには、フォレストルートドメイン内のさまざまなコンテナーの読み取りアクセス許可を手動で付与する必要があります。

フォレスト以外のルートドメインでドメインの準備、サーバーのアクティブ化、またはプールの作成を実行できるようにするには、次のオプションがあります。

  - エンタープライズ管理者グループのメンバーであるアカウントを使用して、ドメインの準備を実行します。

  - Domain Admins グループのメンバーであるアカウントを使用し、フォレストルートドメイン内の次の各コンテナーで、このアカウントに読み取りアクセス許可を付与します。
    
      - Domain
    
      - 構成またはシステム

エンタープライズ管理者グループのメンバーであるアカウントを使用して、ドメインの準備またはその他のセットアップタスクを実行しない場合は、フォレストルートの関連するコンテナーで読み取りアクセスを使用するアカウントを明示的に付与します。

<div>

## <a name="to-give-users-read-access-permissions-on-containers-in-the-forest-root-domain"></a>フォレストのルートドメインのコンテナーの読み取りアクセス許可をユーザーに付与するには

1.  フォレストルートドメインの Domain Admins グループのメンバーであるアカウントで、フォレストルートドメインに参加しているコンピューターにログオンします。

2.  フォレストルートドメインに対して adsiedit を実行します。
    
    認証済みユーザー Ace がドメイン、構成、またはシステムコンテナーから削除された場合は、次の手順で説明するように、コンテナーに読み取り専用のアクセス許可を付与する必要があります。

3.  コンテナーを右クリックし、[ **プロパティ**] をクリックします。

4.  [ **セキュリティ** ] タブをクリックします。

5.  [**詳細設定**] をクリックします。

6.  [ **権限** ] タブの [ **追加**] をクリックします。

7.  次の形式を使用して、アクセス許可を付与するユーザーまたはグループの名前を入力し `domain\account name` 、[ **OK]** をクリックします。

8.  [ **オブジェクト** ] タブの [ **適用** 対象] で、[ **このオブジェクトのみ**] をクリックします。

9.  [ **権限**] で、[ **許可する** 列: **リストコンテンツ**]、[すべての **プロパティの読み取り**]、[ **アクセス許可の読み取り**] の順にクリックして、次の許可 ace を選択します。

10. [ **OK]** を2回クリックします。

11. 手順2に示されている関連コンテナーについて、この手順を繰り返します。

</div>

</div>

<span> </span>

</div>

</div>

</div>

