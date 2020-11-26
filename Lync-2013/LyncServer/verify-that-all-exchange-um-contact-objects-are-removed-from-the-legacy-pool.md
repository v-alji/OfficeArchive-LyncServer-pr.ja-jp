---
title: すべての Exchange UM 連絡先オブジェクトが従来のプールから削除されていることを確認する
description: すべての Exchange UM 連絡先オブジェクトが、従来のプールから削除されていることを確認します。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Verify that all Exchange UM Contact objects are removed from the legacy pool
ms:assetid: 5a813169-0ed7-4f84-a242-ed2cd4ea5c43
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688068(v=OCS.15)
ms:contentKeyID: 49733664
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8af5dea6cf746c55d8fecf074e132f721c380de1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440137"
---
# <a name="verify-that-all-exchange-um-contact-objects-are-removed-from-the-legacy-pool"></a>すべての Exchange UM 連絡先オブジェクトが従来のプールから削除されていることを確認する

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-09-26_

**Ocsumutil** ツールまたは **Get-csexumcontact** コマンドレットを使用して、Exchange UM 連絡先オブジェクトが従来の Office Communications Server 2007 R2 プールから削除されていることを確認します。 **Ocsumutil** は、次のフォルダーにあります。

% Program Files% \\ Common Files \\ Lync Server 2013 \\ サポート \\OcsUMUtil.exe

**Ocsumutil** は、次のユーザーアカウントから実行されている必要があります。

  - RTCUniversalServerAdmins と RTCUniversalUserAdmins グループのメンバーシップ (Exchange Server ユニファイドメッセージングの設定を読むための権限が含まれています)

  - 指定された組織単位 (OU) コンテナーで連絡先オブジェクトを作成するためのドメイン権限

**Csexumcontact** コマンドレットの使い方の詳細については、「Lync Server 管理シェルのドキュメントの [入手](https://docs.microsoft.com/powershell/module/skype/Get-CsExUmContact)」を参照してください。

</div>

<span> </span>

</div>

</div>

</div>

