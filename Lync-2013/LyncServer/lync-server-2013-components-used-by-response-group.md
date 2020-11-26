---
title: 'Lync Server 2013: 応答グループで使用されるコンポーネント'
description: 'Lync Server 2013: 応答グループで使用されるコンポーネント。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components used by Response Group
ms:assetid: 2b058785-47ca-43b7-b3de-6928a60dc685
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425768(v=OCS.15)
ms:contentKeyID: 48183693
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2a1e916d9e4bf986bf0337a6f1f1dd918ff2772e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434558"
---
# <a name="components-used-by-response-group-in-lync-server-2013"></a>Lync Server 2013 の応答グループで使用されるコンポーネント

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-09-11_

応答グループアプリケーションは、エンタープライズボイスの展開時に自動的に有効になります。 このセクションでは、応答グループアプリケーションをサポートするコンポーネントについて説明します。

<div>

## <a name="response-group-components"></a>応答グループのコンポーネント

次の Microsoft Lync Server 2013 コンポーネントは、応答グループアプリケーションをサポートしています。

  - **アプリケーションサービス**   アプリケーションサービスは、応答グループなど、統合された通信アプリケーションを展開、ホスティング、および管理するためのプラットフォームを提供します。 アプリケーションサービスは、フロントエンドプールとすべての Standard Edition サーバーの各フロントエンドサーバーに自動的にインストールされます。

  - **応答グループのアプリケーション**   応答グループアプリケーションは、アプリケーションサービスによってホストされるユニファイドコミュニケーションアプリケーションの1つです。 応答グループを展開すると、自動的に含まれます。 応答グループアプリケーションは、複数のエージェントに着信通話をルーティングしてキューに発信します。

  - **言語パック**   音声合成と音声認識をサポートするには、言語パックが必要です。 これらの音声テクノロジは、メッセージの構成 (開始メッセージおよびその他のプロンプト、対話型音声応答 (IVR) による質問と回答など) に使用します。 既定では、Lync Server 2013 を展開すると、サポートされている26言語パックがインストールされます。

  - **オーディオファイル**   オーディオファイルは、メッセージおよび保留中の音楽に使用されます。

  - **ファイルストア**   応答グループは、ファイルストアを使ってオーディオファイルを保存します。 複数の応答グループプールでは、同じファイルストアのインスタンスを使うことができます。

  - **応答グループ構成ツール**   応答グループ構成ツールは、応答グループの作成と構成に使用される web ベースのツールです。 応答グループの構成ツールは、Web サービスをインストールするときに含まれています。

  - **Microsoft Lync Server 2013 コントロールパネル**   Lync Server コントロールパネルを使用して、応答グループのエージェントグループとキューをセットアップして構成することができます。

  - **Lync Server 管理シェル**   応答グループの設定はすべて、Lync Server 管理シェルコマンドレットを使用して構成できます。

  - **Microsoft Lync 2013**   正式なエージェント (グループへの通話を許可するには、グループへのサインインが必要なエージェント) Lync 2013 を使って、グループにサインインしてサインアウトします。 エージェントグループが正式なエージェント用に構成されている場合、エージェントは Lync 2013 のメニュー項目をクリックして Internet Explorer を開き、グループへのサインインとグループからのサインアウト用の web ページ本体を表示します。

  - **Web サービス**   Web サービスは、応答グループ構成ツール、エージェントのサインインとサインアウトコンソール、Lync Server コントロールパネル、応答グループクライアント web サービスに必要です。

  - **応答グループクライアント Web サービス**   応答グループアプリケーションは、サードパーティのアプリケーションによって提供されるクライアント web サービスであり、エージェント、エージェントグループメンバーシップ、エージェントのサインイン状態、グループの通話状態、匿名の通話をサポートするグループの情報を取得するために使用できます。 Lync 2013 および Lync 2010 アテンダント応答グループクライアント Web サービスを使用して、エージェントが匿名呼び出しを行うときに使用できる応答グループの一覧を取得します。 Web サービスをインストールするときに、クライアント web サービスが含まれています。

</div>

</div>

<span> </span>

</div>

</div>

</div>

