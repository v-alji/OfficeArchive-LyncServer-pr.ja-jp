---
title: ベストプラクティスアナライザーのグループメンバーシップとユーザー権限の要件
description: ベストプラクティスアナライザーのグループメンバーシップとユーザー権限の要件。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Group memberships and user rights requirements for Best Practices Analyzer
ms:assetid: f812e343-8f75-454e-b7a8-1b404e32071a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg591354(v=OCS.15)
ms:contentKeyID: 48185869
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 64a7d785a77701c6796488178a7cce10caf54f42
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427825"
---
# <a name="group-memberships-and-user-rights-requirements-for-best-practices-analyzer-in-lync-server-2013"></a>Lync Server 2013 でのベストプラクティスアナライザーのグループメンバーシップとユーザー権限の要件

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-10-21_

ベストプラクティスアナライザーを正常に実行するには、ログオンに使用するユーザーアカウントが、ローカルコンピューターの管理者グループのメンバーである必要があります。 さらに、環境をスキャンするには、ユーザーアカウントが次のグループのメンバーである必要があります。

  - **ドメイン管理者**   Active Directory ドメインサービスの情報を列挙し、ドメインコントローラーとグローバルカタログサーバー上の Windows Management Instrumentation (WMI) プロバイダーを呼び出すには、こちらを参照してください。

  - **管理者**   各 Lync Server 2013 内部コンピューターと各エッジサーバーで、Windows Management Instrumentation (WMI) プロバイダーを呼び出してレジストリにアクセスするために必要です。

  - **RTCUniversalReadOnlyAdmins**   フルまたは委任された読み取り専用の Lync Server 2013 管理者権限。

  - **Exchange の表示のみ管理者**   Microsoft Exchange 組織のフルまたは委任された Exchange の表示のみの管理者。

ユーザーアカウントに十分なユーザー権限がない場合は、次の2つのオプションがあります。

  - コマンドプロンプトで、 **runas** コマンドを使用して、十分なユーザー権限があるアカウントでツールを実行します。 構文は次のとおりです。
    
        runas /netonly /user:<domain>\<userName> rtcbpa.exe

  - [ **Active Directory に接続する** ] ページで、ベストプラクティスアナライザーを実行するために使用する予定のアカウントの資格情報を設定します。 [ **詳細ログインオプションの表示] を** クリックします。 Active Directory ドメインサービスへの接続用に1つ、Lync Server 2013 エッジサーバーへの接続用、および Exchange サーバーへの接続用の3つのアカウントを入力できます。 これらのいずれかのアカウントを指定しない場合、ログオンに使用したユーザーアカウントとベストプラクティスアナライザーを実行するために使用されます。

</div>

<span> </span>

</div>

</div>

</div>

