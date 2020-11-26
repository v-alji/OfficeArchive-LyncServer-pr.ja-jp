---
title: 'Lync Server 2013: 既定の写真オプションを構成する'
description: 'Lync Server 2013: 既定の写真オプションを構成しています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring default picture options
ms:assetid: b1c986f0-6400-447a-9e36-78c1c3a4f793
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn205074(v=OCS.15)
ms:contentKeyID: 56280893
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6261aca82b4c71eb8e0573e8d2adbfc008e743fc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433214"
---
# <a name="configuring-default-picture-options-in-lync-server-2013"></a>Lync Server 2013 で既定のピクチャオプションを構成する

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2013-03-22_

既定では、ユーザーの写真が自動的に表示されます。 ユーザーが画像を非表示にする場合は、Lync クライアントで [ **自分の写真を表示** しない] オプションを選択できます。 ただし、この設定は、他の一部の Office アプリケーションでは無視されます。

ユーザーによって無効にされている場合でも画像を表示する可能性がある場合は、ユーザーの写真が既定で表示されないように、世界中の Lync 画像の表示設定をグローバルに変更したり、サイトまたはサービス用に変更したりすることができます。 以下の Lync Server Management Shell コマンドレットを使用して、クライアントで [ **自分の写真を表示** する] オプションを明示的に選択しない限り、ユーザーの写真が表示されないようにします。

    Set-CsPrivacyConfiguration -DisplayPublishedPhotoDefault $False

このコマンドレットの詳細については、「Lync Server Management Shell ドキュメントの [CsPrivacyConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsPrivacyConfiguration) 」を参照してください。

</div>

<span> </span>

</div>

</div>

</div>

