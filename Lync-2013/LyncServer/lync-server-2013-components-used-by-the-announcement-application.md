---
title: 'Lync Server 2013: アナウンス アプリケーションで使用されるコンポーネント'
description: 'Lync Server 2013: アナウンスメントアプリケーションで使用されるコンポーネント。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components used by the Announcement application
ms:assetid: 7b1a0281-cf31-459d-a734-5f10a129089c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398608(v=OCS.15)
ms:contentKeyID: 48184595
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e5338ad097c814d5c6435bd89dbf7cfa8680feb8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398522"
---
# <a name="components-used-by-the-announcement-application-in-lync-server-2013"></a>Lync Server 2013 のアナウンス アプリケーションで使用されるコンポーネント

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-09-13_

Lync Server 2013 では、アナウンスメントアプリケーションは応答グループアプリケーションのコンポーネントです。 エンタープライズ Voip を展開すると、応答グループアプリケーションと共に、アナウンスメントアプリケーションが自動的にインストールされ、アクティブ化されます。 このセクションでは、アナウンスメントアプリケーションをサポートするコンポーネントについて説明します。

<div>

## <a name="announcement-application-components"></a>アナウンスメントアプリケーションのコンポーネント

以下の Lync Server コンポーネントは、アナウンスメントアプリケーションをサポートしています。

  - **アプリケーションサービス**   アプリケーションサービスは、ユニファイドコミュニケーションアプリケーションを展開、ホスティング、および管理するためのプラットフォームを提供します。 アプリケーションサービスは、フロントエンドプールのすべてのフロントエンドサーバーと、すべての Standard Edition サーバーに自動的にインストールされます。

  - **応答グループのアプリケーション**   応答グループアプリケーションは、アプリケーションサービスによってホストされるユニファイドコミュニケーションアプリケーションの1つです。 [割り当てられていない電話番号] の範囲がお知らせにルーティングするように構成されている場合は、電話番号への通話をルーティングするために応答グループアプリケーションが必要です。 (応答グループアプリケーションは、すべての範囲が Exchange ユニファイドメッセージング (UM) にルーティングするように構成されている場合は必須ではありません)。

  - **オーディオファイル**   アナウンスメントにはオーディオファイルが使用されます。

  - **ファイルストア**   アナウンスメントアプリケーションは、ファイルストアを使ってオーディオファイルを保存します。

  - **Lync Server コントロールパネル**   Lync Server コントロールパネルを使用して、割り当てられていない番号テーブルを構成することができます。

  - **Lync Server 管理シェル**   Lync Server 管理シェルコマンドレットを使用して、アナウンスメントの設定と割り当てられていない番号テーブルを構成することができます。

</div>

</div>

<span> </span>

</div>

</div>

</div>

