---
title: 既存の会議および会議コンテンツの移行
description: 既存の会議と会議のコンテンツを移行します。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrate existing meetings and meeting content
ms:assetid: 30516731-2ae1-4a6d-a7e1-d3f05778c954
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688011(v=OCS.15)
ms:contentKeyID: 49733599
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d94dd35063a121a057a218c27fdb36e42a155b77
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443805"
---
# <a name="migrate-existing-meetings-and-meeting-content"></a>既存の会議および会議コンテンツの移行

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2013-02-22_

ユーザーアカウントを Lync Server 2010 から Lync Server 2013 サーバーに移動すると、次の情報がそのユーザーアカウントに移動されます。

  - **ユーザーが既にスケジュールした会議**。 これには、会議ディレクトリと会議データの移動が含まれます。

  - **ユーザーの暗証番号 (PIN)**。 ユーザーの現在の PIN は、有効期限が切れるか、ユーザーが新しい PIN を要求するまで、引き続き動作します。

次のユーザーアカウント情報は、新しいサーバーに移動されません。

  - **会議コンテンツ**。 会議中に共有されたコンテンツ (PowerPoint、ホワイトボード、添付ファイル、投票データなど) を移動するには、 **move-CsUser** コマンドレットの一部として、 **-moveconの [data** ] パラメーターを使用します。

</div>

<span> </span>

</div>

</div>

</div>

