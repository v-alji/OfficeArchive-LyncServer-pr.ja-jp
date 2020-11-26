---
title: 'Lync Server 2013: Lync クライアントを展開する'
description: 'Lync Server 2013: Lync クライアントを展開しています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying Lync clients
ms:assetid: 3d10abf2-d484-4fa0-8f10-4a5f9dfba4f5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204827(v=OCS.15)
ms:contentKeyID: 48183925
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 09b501fc721ac880c5cf7da0293e3aa9c6443722
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429987"
---
# <a name="deploying-lync-clients-in-lync-server-2013"></a>Lync Server 2013 での Lync クライアントの展開

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-10-03_

Lync 2013 では、クライアントの展開にさまざまなアプローチが導入されています。 以前のリリースから出発した Lync 2013 には、独自のインストーラーがありません。 代わりに Lync は、Office 2013 セットアッププログラムに含まれています。 Lync 2013 をユーザーに展開するには、Office 2013 のインストール方法とカスタマイズツールを使用できます。

  - **Office 2013 Windows installer** は、複数の MSI ファイルで構成される windows installer ベースのインストールパッケージです。 言語に依存しないコア MSI パッケージと 1 つ以上の言語固有のパッケージが組み合わされ 1 つの完全な製品になっています。 セットアップによって個々のパッケージがアセンブルされ、ユーザーのコンピューターへの Office のインストール中およびインストール後に、カスタマイズ タスクとメンテナンス タスクが実行されます。 このセクションのトピックでは、Lync 2013 を展開するために Office 2013 Windows インストーラーを使用およびカスタマイズする方法について説明します。

  - **Office 2013 クイック実行** は、Microsoft 365 管理センターからユーザーに office セットアップファイルを転送するインストールプログラムです。 管理者は、Office 展開ツールを使用してクイック実行用にインストールをカスタマイズできます。 Office 2013 クイック実行は主に Microsoft 365 環境で使用されるため、このインストール方法については、このセクションで詳しく説明されていません。 クイック実行インストールの使用とカスタマイズの詳細については、「Office 2013 リソースキット」を参照してください。 管理者は、Office 2013 クイック実行プログラムと言語ソースファイルをオンプレミスの場所にダウンロードすることもできます。これは、企業のセキュリティ要件により、ネットワーク上の需要を最小限にしたり、ユーザーがインターネットからソフトウェアをインストールしたりできないようにする場合に便利です。

このセクションのトピックでは、Office 2013 MSI ベースのインストーラーを使用してクライアントを展開する方法について説明します。 主な参照は、Office 2013 リソースキットドキュメントです。ここでは、インフラストラクチャの準備、セットアップのカスタマイズ、Office 2013 の展開の方法について詳しく説明します。 ただし、Office ドキュメントをこのセクションのトピックと組み合わせて使用する必要があります。このセクションでは、Lync 2013 に固有の展開に関する考慮事項について説明します。

<div>


> [!NOTE]  
> <UL>
> <LI>
> <P>Lync 2013 用のオンライン会議アドインは、Outlook メッセージングおよびコラボレーションクライアント内からの会議管理をサポートしており、Lync 2013 と共に自動的にインストールされます。</P>
> <LI>
> <P>Office 2013 セットアッププログラムでは、以前のバージョンの Lync や Office Communicator はアンインストールされません。 Lync 2013 クライアントは、他の Lync または Office Communicator クライアントと並行してインストールされます。</P></LI></UL>



</div>

<div>

## <a name="in-this-section"></a>このセクション中

  - [Lync Server 2013 でのクライアントインストールのカスタマイズ](lync-server-2013-customizing-client-installation.md)

  - [Lync Server 2013 での Lync の動作とユーザーインターフェイスのカスタマイズ](lync-server-2013-customizing-lync-behavior-and-the-user-interface.md)

  - [Lync Server 2013 でのオンライン会議アドインのカスタマイズ](lync-server-2013-customizing-the-online-meeting-add-in.md)

  - [Lync Server 2013 での会議参加ページの構成](lync-server-2013-configuring-the-meeting-join-page.md)

  - [Lync Server 2013 でサポートされているクライアントバージョンを構成する](lync-server-2013-configuring-supported-client-versions.md)

  - [Lync Server 2013 で拡張プレゼンスプライバシーモードを構成する](lync-server-2013-configuring-enhanced-presence-privacy-mode.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

