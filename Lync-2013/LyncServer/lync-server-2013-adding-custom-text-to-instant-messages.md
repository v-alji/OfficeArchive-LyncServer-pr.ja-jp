---
title: 'Lync Server 2013: インスタント メッセージへのユーザー設定テキストの追加'
description: 'Lync Server 2013: インスタントメッセージにカスタムテキストを追加します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Adding custom text to instant messages
ms:assetid: cabcc3ec-9d35-42ac-a403-e21b7d538c2c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398847(v=OCS.15)
ms:contentKeyID: 48185458
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 54f5cf031da0ba4d5bd0b6dbaa7f5ebc9d0b3a6c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439234"
---
# <a name="adding-custom-text-to-instant-messages-in-lync-server-2013"></a>Lync Server 2013 でのインスタント メッセージへのユーザー設定テキストの追加

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**トピックの最終更新日:** 2013-02-20_

**新しい CSClientPolicy** を使用するか、または imwarning パラメーターを使用し **て、すべて** の lync 2013 インスタントメッセージング (IM) 会話の先頭に免責事項または警告を追加します。

次の例のコマンドは、新しい IM の会話が開始されるたびに、会話ウィンドウの上部にセキュリティリマインダーを追加します。

    New-CsClientPolicy -Identity IMSecurityNotice -IMWarning 
    "Remember, security is everyone's responsibility. Keep it confidential."

ユーザーにこの新しいポリシーを割り当てるには **、グラント Clientpolicy** を使用します。 詳細については、「 **新しい-CSClientPolicy** 」と「Lync Server 管理シェルドキュメントの **権限を付与** する」を参照してください。

</div>

<span> </span>

</div>

</div>

</div>

