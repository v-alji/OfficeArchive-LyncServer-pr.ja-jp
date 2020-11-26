---
title: 'Lync Server 2013: バックアップ レジストラー関係'
description: Lync Server 2013 のバックアップレジストラーのリレーションシップ。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Backup Registrar relationships
ms:assetid: 7e078271-84b9-4666-989c-c4507a0cdf4a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205033(v=OCS.15)
ms:contentKeyID: 48184631
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7b0bfce6444ae78c2fb792a6d63dba4bf36b1791
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437918"
---
# <a name="backup-registrar-relationships-in-lync-server-2013"></a>Lync Server 2013 のバックアップ レジストラー関係

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-06-28_

障害復旧の機能を提供するほか、ペアになった 2 つのプールは互いにバックアップ レジストラーの役割も果たします。 Lync Server 2013 では、フロントエンドプール間のバックアップレジストラーの関係は、常に1:1 と逆数になります。 つまり、P1 が P2 のバックアップである場合、P2 は P1 のバックアップである必要があります。また、その他のフロントエンドプールのバックアップを行うことはできません。 これは、Lync Server 2010 からの変更であり、フロントエンドプールのバックアップ関係は何度でもかまいません。

2つのフロントエンドプール間のバックアップリレーションシップは1:1 と対称である必要がありますが、Lync Server 2010 の場合と同様に、各フロントエンドプールも、任意の数の Survivable Branch アプライアンスのバックアップレジストラーにすることができます。

Lync Server 2013 は、Survivable Branch アプライアンスをホームにしているユーザーに対して、障害回復のサポートを拡張しないことに注意してください。 Survivable Branch アプライアンスのバックアップとして機能するフロントエンドプールがダウンしている場合は、フロントエンドプールに所属しているユーザーが、バックアップフロントエンドプールにフェールオーバーした後でも、Survivable Branch アプライアンスにサインインしたユーザーは復元性モードになります。

</div>

<span> </span>

</div>

</div>

</div>

