---
title: 構成の設定の確認
description: 構成設定を確認します。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Verify configuration settings
ms:assetid: 51c2d1d9-63f7-43ab-88ca-b8913da7cede
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204885(v=OCS.15)
ms:contentKeyID: 48184111
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d7bb1135e95dafe51e906768fe0f4f0d57bf2d6c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423345"
---
# <a name="verify-configuration-settings"></a>構成の設定の確認

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-09-06_

中央管理ストアが配置されている内部コンピューターで、または Lync Server 2013 コアコンポーネント (OcsCore.msi) がインストールされているドメインに参加しているコンピューターで、Lync Server 2013 **Get-CsManagementStoreReplicationStatus** コマンドレットを実行して、構成情報のレプリケーションを検証できます。

初期結果では、レプリケーションに "True" ではなく "False" と表示されることがあります。 その場合は、 **CsManagementStoreReplication** コマンドレットを実行して、 **CsManagementStoreReplicationStatus** をもう一度実行する前に複製処理が完了するまで待ちます。

</div>

<span> </span>

</div>

</div>

</div>

