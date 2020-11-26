---
title: オペレーティング システムと必要なソフトウェアのサーバーへのインストール
description: サーバーにオペレーティングシステムと必須ソフトウェアをインストールします。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Install operating systems and prerequisite software on servers
ms:assetid: 055991e0-5aeb-43fc-a7ba-d4b02316d73b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398103(v=OCS.15)
ms:contentKeyID: 48183288
ms.date: 07/24/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2bae9e57db9c2f1d3f3bde7ce9cc7071b73aa01d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427174"
---
# <a name="install-operating-systems-and-prerequisite-software-on-servers-for-lync-server-2013"></a>Lync Server 2013 のオペレーティング システムと必要なソフトウェアのサーバーへのインストール

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2014-07-24_

ハードウェアとシステムインフラストラクチャをセットアップした後は、展開する各サーバー上の他のすべての必須ソフトウェアに加えて、適切な Windows オペレーティングシステムと更新プログラムをインストールする必要があります。 これには、各 Lync Server 2013 サーバーの役割と、展開に必要な SQL Server が実行されているその他のインフラストラクチャサーバーまたはサーバーが含まれます。

<div>


> [!NOTE]
> このセクションでは、内部サーバーのオペレーティングシステムと必須ソフトウェアのインストールについて説明します。 エッジサーバーを展開して外部ユーザーのアクセスをサポートする場合は、エッジサーバーやリバースプロキシサーバーなど、それらのサーバーのオペレーティングシステムと必須ソフトウェアをインストールする必要があります。 外部ユーザーアクセスをサポートするようにサーバーを準備する方法について詳しくは、「展開ドキュメントの「 <A href="lync-server-2013-preparing-for-installation-of-servers-in-the-perimeter-network.md">境界ネットワークでの Lync Server 2013 の境界ネットワークでのサーバーインストールの準備</A> 」をご覧ください。



</div>

<div>

## <a name="install-windows-operating-systems-on-servers"></a>Windows オペレーティングシステムをサーバーにインストールする

展開する各サーバーで、次のように適切な Windows オペレーティングシステムをインストールします。

  - **Lync Server 2013 を実行しているサーバー**   Lync Server 2013 を実行しているサーバーのオペレーティングシステム要件の詳細については、サポートドキュメントの「 [Lync server 2013 でのサーバーとツールのオペレーティングシステムのサポート](lync-server-2013-server-and-tools-operating-system-support.md) 」を参照してください。

  - **データベースサーバー**   バックエンドデータベース、アーカイブデータベース、監視データベースなど、データベースサーバーのオペレーティングシステム要件の詳細については、SQL Server のマニュアルを参照してください。 SQL Server 2012 の場合は、SQL Server 2012 Books Online を参照してください [https://go.microsoft.com/fwlink/p/?linkId=218015](https://go.microsoft.com/fwlink/p/?linkid=218015) 。

<div>


> [!NOTE]
> Windows Server 2008 R2 SP1 で Lync Server 2013 をインストールする場合は、 &nbsp; &nbsp; まず Microsoft サポート技術情報の記事2646886、「修正: モジュールが IIS 7.5 で InsertEntityBody メソッドを呼び出すときにヒープの破損が発生する」、at、 <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=2646886"> https://go.microsoft.com/fwlink/p/?linkid=3052&amp kbid = 2646886</A>に記載されている更新プログラムをインストールする必要があります。<BR>また、「サポート技術情報」の記事に記載されているようにレジストリを変更する必要があります。これには、 <A href="https://go.microsoft.com/fwlink/p/?linkid=506893">Windows Server 2012 R2 にインストールされている Lync Server 2013 フロントエンドサーバーに</A>保存されている、「イベント id 32402, 61045 の記録」の



</div>

</div>

<div>

## <a name="install-windows-update-on-servers"></a>サーバーに Windows Update をインストールする

各サーバー上の Windows Update から以下の更新プログラムをインストールします。

  - **Lync Server 2013 を実行しているサーバーの Windows Update**   Lync Server 2013 を実行しているサーバーに必要な Windows Update からの更新プログラムの詳細については、「計画ドキュメントの「 [Lync server 2013 のその他のソフトウェア要件](lync-server-2013-additional-software-requirements.md) 」を参照してください。

  - **データベースサーバー**   バックエンドデータベース、アーカイブデータベース、監視データベースなど、データベースサーバーに必要な更新プログラムの詳細については、SQL Server 2012 に関するドキュメントを参照してください。 SQL Server 2012 の場合は、SQL Server 2012 Books Online を参照してください [https://go.microsoft.com/fwlink/p/?linkId=218015](https://go.microsoft.com/fwlink/p/?linkid=218015) 。

</div>

<div>

## <a name="install-other-prerequisite-software-on-servers"></a>サーバーにその他の必須ソフトウェアをインストールする

Lync Server 2013 では、サーバーに次の追加ソフトウェアがインストールされている必要があります。

  - **Lync Server 2013 を実行しているサーバーの必須ソフトウェア**   Lync Server 2013 を実行しているサーバーのその他のソフトウェアの前提条件は、展開されているサーバーの役割によって異なります。 各サーバー固有のソフトウェア要件の詳細については、「計画ドキュメントの「 [Lync server 2013 のその他のソフトウェア要件](lync-server-2013-additional-software-requirements.md) 」を参照してください。

  - **Windows Id ファンデーション**   Lync Server 2013 では、サーバー間認証のシナリオをサポートするために、Windows Id ファンデーションをインストールする必要があります。 コンピューターにインストールされていることを確認するには、[コントロールパネル]、[ **プログラムと機能**]、[ **インストールされている更新** プログラムの表示]、[ **Microsoft Windows**] の下の [確認] をクリックします。 Windows Id Foundation のインストールの詳細については、を参照してください [https://go.microsoft.com/fwlink/p/?linkId=204657](https://go.microsoft.com/fwlink/p/?linkid=204657) 。

  - **Microsoft .Net Framework 4.5**   Lync Server 2013 では、64ビット版の Microsoft .NET Framework 4.5 が必要です。

  - **データベースサーバー向けの必須ソフトウェア**   バックエンドデータベース、アーカイブデータベース、監視データベースなど、データベースサーバーに必要な Windows Update の詳細については、SQL Server 2012 に関するドキュメントを参照してください [https://go.microsoft.com/fwlink/p/?linkId=218015](https://go.microsoft.com/fwlink/p/?linkid=218015) 。
    
    <div>
    

    > [!NOTE]
    > Lync Server 2013 は、各標準エディションサーバーと、ローカル構成ストアが配置されている Lync Server 2013 を実行している各サーバーに、Microsoft SQL Server 2012 Express を自動的にインストールします。

    
    </div>

  - **Windows Media Format Runtime**   会議を展開するすべてのフロントエンドサーバーおよび標準エディションサーバーには、Windows Media Format ランタイムがインストールされている必要があります。 Windows Media 形式ランタイムは、コールパーク、アナウンスメント、および応答グループアプリケーションがお知らせや音楽を再生するために、Windows Media オーディオ (.wma) ファイルを実行するために必要です。
    
    <div>
    

    > [!NOTE]
    > Windows Server 2012 および Windows Server 2012 R2 の場合、Windows Media Format Runtime は Microsoft メディアファンデーションと共にインストールされます。

    
    </div>
    
    <div>
    

    > [!NOTE]
    > Windows Server &nbsp; 2008 および Windows server &nbsp; 2008 R2 の場合、Windows &nbsp; デスクトップエクスペリエンスの一部として Windows Media 形式ランタイムがインストールされます。 Lync Server 2013 をインストールする前に、Windows デスクトップエクスペリエンスをインストールすることをお勧めします。 Lync Server 2013 でサーバー上にこのソフトウェアが見つからない場合は、インストールするように求められます。その後、インストールを完了するには、サーバーを再起動する必要があります。

    
    </div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

