---
title: 'Lync Server 2013: 新しいチャット ルームの作成または編集'
description: 'Lync Server 2013: 新しい会議室の作成または編集。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Creating or editing a new room
ms:assetid: aa8f4349-cfd9-4036-9c4d-de8fb2c4c8a4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ215880(v=OCS.15)
ms:contentKeyID: 48706008
ms.date: 03/19/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d822eb05993f77c57200e29364f0a6a68509450b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431464"
---
# <a name="creating-or-editing-a-new-room-in-lync-server-2013"></a>Lync Server 2013 での新しいチャット ルームの作成または編集

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2015-03-19_

常設チャットルームの構成は、通常、ユーザーによって処理されます。通常、常設チャット管理者は、チャットルームの構成や管理は行いません。 会議室を管理するための Windows PowerShell コマンドレットは、 **CsPersistentChatAdministrator** 管理者のみが利用できます。

特定のカテゴリの作成 **者である** ユーザーは、Lync クライアントを使用して、会議室の作成と管理を行うことができます。 特定のチャットルームの管理者として指定されているユーザーは、会議室のプロパティやメンバーシップの編集など、会議室の継続的な管理を実行することもできます。

<div>


> [!TIP]  
> 常設チャット管理者も作成者になることができます。また、作成者に課される制限の対象にはなりません。



</div>

必要に応じて、常設チャットの管理者である場合は、Windows PowerShell コマンドレットを使う代わりに、ユーザーインターフェイスを使ってチャットルームを作成し、管理することができます。 これを行うには、常設チャットサーバーの管理者を SIP に有効にしてから、Lync クライアントを使ってチャットルームを作成し、管理します。

ユーザー用のカスタムの会議室管理ワークフローを作成する場合は、常設チャットサーバー構成の **RoomManagementUrl** プロパティを設定して、Lync クライアントからユーザー設定のソリューションにユーザーをリダイレクトすることができます。

Windows PowerShell コマンドラインインターフェイスを使用してチャットルームを構成する方法について詳しくは、「 [Windows powershell コマンドレットを使用して常設チャットサーバーを構成](configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md)する」の「会議室の管理」をご覧ください。

チャットルームの設定の詳細については、展開ドキュメントの「 [Lync Server 2013 で会議室を構成](lync-server-2013-configure-rooms.md) する」を参照してください。

<div>


> [!NOTE]  
> 常設チャットサーバーを使用すると、ユーザーは特定のサイトのチャットルームを作成して管理することができます。 ただし、ユーザーは同じトポロジ内の他のサイトのチャットルームを作成または管理することはできません。 組織内のすべてのサイトについて、必ずチャットルームの作成者と管理者を指定してください。



</div>

<div>


> [!NOTE]  
> Lync Server Survivable Branch Appliance をホームとして使用しているユーザーは、新しいチャットルームを作成したり、既存のルームの会議室カードを表示したりすることはできません。



</div>

</div>

<span> </span>

</div>

</div>

</div>

