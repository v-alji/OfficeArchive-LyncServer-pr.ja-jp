---
title: 'Lync Server 2013: アナウンス アプリケーションの技術要件'
description: 'Lync Server 2013: お知らせアプリケーションの技術要件。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Technical requirements for the Announcement application
ms:assetid: fbd8c204-3765-4b22-a0c9-a781b5126366
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205413(v=OCS.15)
ms:contentKeyID: 48185944
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: adc5019408b79301bbcda3993ceb7d96ee4d9b7d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444309"
---
# <a name="technical-requirements-for-the-announcement-application-in-lync-server-2013"></a>Lync Server 2013 のアナウンス アプリケーションの技術要件

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2013-11-07_

このセクションでは、アナウンスメントアプリケーションの次の技術上の要件について説明します。

  - ハードウェアの要件

  - ソフトウェア要件

  - ポートの要件

  - オーディオファイルの要件

<div>

## <a name="hardware-requirements"></a>ハードウェア要件

アナウンスメントアプリケーションには、フロントエンドサーバーと同じハードウェア要件があります。 ハードウェア要件の詳細については、サポートドキュメントの「 [サーバーハードウェアプラットフォーム (Lync server 2013 の場合](lync-server-2013-server-hardware-platforms.md) )」を参照してください。

</div>

<div>

## <a name="software-requirements"></a>ソフトウェア要件

アナウンスメントアプリケーションには、フロントエンドサーバーと同じオペレーティングシステム要件とソフトウェアの前提条件があります。 ソフトウェア要件の詳細については、サポートドキュメントの「 [Lync server 2013 でのサーバーとツールのオペレーティングシステムのサポート](lync-server-2013-server-and-tools-operating-system-support.md) 」を参照してください。

アナウンスメントアプリケーションを実行するすべてのフロントエンドサーバーまたは標準エディションのサーバーには、windows server 2008 R2 を実行しているサーバー、または windows server 2012 R2 を実行して2012いるサーバー用の Microsoft メディアファンデーションがインストールされている必要があります。 Windows Server 2008 R2 の場合、windows Media 形式ランタイムは Windows デスクトップエクスペリエンスの一部としてインストールされます。 Windows media Format Runtime または Microsoft メディアファンデーションは、アナウンスメントアプリケーションがお知らせや音楽を再生するために Windows Media オーディオ (.wma) ファイルを使用する場合に必要です。

</div>

<div>

## <a name="port-requirements"></a>ポートの要件

アナウンスメントアプリケーションでは、次のポートが使用されます。

  - **ポート 5071**   SIP リッスン要求のために使用

<div>


> [!NOTE]  
> このポートは既定の設定であり、<STRONG>Set-CsApplicationServer</STRONG> コマンドレットを使用して変更することができます。 このコマンドレットの詳細については、「Lync Server 管理シェルのドキュメント」を参照してください。



</div>

</div>

<div>

## <a name="audio-file-requirements"></a>オーディオ ファイルの要件

アナウンスメントアプリケーションは、音楽とお知らせのウェーブ (.wav) ファイル形式と Windows Media オーディオ (.wma) ファイル形式をサポートしています。 アナウンスメントアプリケーションのオーディオファイルの要件は、応答グループアプリケーションの場合と同じです。 詳細については、「 [Lync Server 2013 の応答グループの技術要件](lync-server-2013-technical-requirements-for-response-group.md)」を参照してください。

</div>

</div>

<span> </span>

</div>

</div>

</div>

