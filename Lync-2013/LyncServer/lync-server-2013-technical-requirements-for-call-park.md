---
title: 'Lync Server 2013: コール パークの技術要件'
description: 'Lync Server 2013: コールパークの技術要件。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Technical requirements for Call Park
ms:assetid: 38bcf302-2b72-4492-9266-f6dc31b566e1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204818(v=OCS.15)
ms:contentKeyID: 48183897
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6ddc17b40f78c42c090d1a87b4580ebdad0a07f6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399231"
---
# <a name="technical-requirements-for-call-park-in-lync-server-2013"></a>Lync Server 2013 のコール パークの技術要件

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2013-11-07_

このセクションでは、次のようなコールパークの技術要件について説明します。

  - ハードウェアの要件

  - ソフトウェア要件

  - ポートの要件

  - オーディオファイルの要件

<div>

## <a name="hardware-requirements"></a>ハードウェア要件

コールパークアプリケーションには、フロントエンドサーバーと同じハードウェア要件があります。 ハードウェア要件の詳細については、サポートドキュメントの「 [サーバーハードウェアプラットフォーム (Lync server 2013 の場合](lync-server-2013-server-hardware-platforms.md) )」を参照してください。

</div>

<div>

## <a name="software-requirements"></a>ソフトウェア要件

コールパークアプリケーションには、フロントエンドサーバーと同じオペレーティングシステム要件とソフトウェアの前提条件があります。 ソフトウェア要件の詳細については、サポートドキュメントの「 [Lync server 2013 でのサーバーとツールのオペレーティングシステムのサポート](lync-server-2013-server-and-tools-operating-system-support.md) 」を参照してください。

コールパークアプリケーションが展開されているすべてのフロントエンドサーバーおよび標準エディションのサーバーでは、windows server 2008 R2 を実行しているサーバー、または windows server 2012 R2 を実行して2012いるサーバーに対して Microsoft メディアファンデーションがインストールされている必要があります。 Windows Server 2008 R2 の場合、windows Media Format Runtime は Windows デスクトップエクスペリエンスの一部としてインストールされます。 Windows media 形式のランタイムまたは Microsoft メディアファンデーションが必要なのは、Windows Media オーディオ (.wma) ファイルで、保留中の音楽の再生が再生されます。

</div>

<div>

## <a name="port-requirements"></a>ポートの要件

コールパークアプリケーションでは、次のポートを使用します。

  - **ポート 5075**   SIP リッスン要求に使用します。

<div>


> [!NOTE]  
> このポートは既定の設定であり、<STRONG>Set-CsApplicationServer</STRONG> コマンドレットを使用して変更できます。 このコマンドレットの詳細については、「Lync Server 管理シェルのドキュメント」を参照してください。



</div>

</div>

<div>

## <a name="audio-file-requirements"></a>オーディオ ファイルの要件

コールパークアプリケーションは、保留中の音楽に対して Windows Media オーディオ (.wma) ファイルのみをサポートします。 保留音のファイルをカスタマイズするには、Microsoft Expression Encoder 4 を使用できます。 式エンコーダー4をダウンロードするには、の「Expression Encoder 4」を参照してください [https://go.microsoft.com/fwlink/p/?linkId=202843](https://go.microsoft.com/fwlink/p/?linkid=202843) 。 このツールを使用すると、ファイルを WMA 形式に変換できます。 通話パーク音楽の保存に推奨される形式は、メディアオーディオ9、44 kHz、16ビット、モノラル、CBR、32 kbps です。

<div>


> [!NOTE]  
> 変換されたファイルは、44 kHz で録音された場合でも、電話では 16 kHz でのみ再生されます。



</div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

