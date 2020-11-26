---
title: 'Lync Server 2013: 音声ルーティング構成のエクスポートとインポート'
description: 'Lync Server 2013: ボイスルーティング構成のエクスポートとインポート'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Exporting and importing voice routing configuration
ms:assetid: c9b78622-5725-43b0-9ee1-5b82b1e1c8eb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398836(v=OCS.15)
ms:contentKeyID: 48185398
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a94a9c02672debae9f5b30e3a1a96856050d6ab1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428357"
---
# <a name="exporting-and-importing-voice-routing-configuration-in-lync-server-2013"></a>Lync Server 2013 での音声ルーティング構成のエクスポートとインポート

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-11-01_

音声ルーティング構成を公開せずに保存する場合は、次の手順に従って、Lync Server コントロールパネルの構成のエクスポートとインポートのコマンドを使用して、ボイスルーティング構成のスナップショットを保存して取得します。 ボイスルーティング構成ファイル (vcfg) をインポートする場合は、その間もサーバー上の音声ルーティング構成に変更が加えられたため、Lync Server コントロールパネルの [ **ボイスルーティング** ] グループのページには、音声ルーティングに対する変更がコミットされていないことが示されます。 こうした未確定の変更は、調整が必要な 2 つの構成間の相違です。

<div>


> [!IMPORTANT]  
> [ <STRONG>ボイスルーティング</STRONG> ] グループ内の任意のページの設定に対してコミットされていない変更を加えた場合、変更はエクスポートされた音声構成ファイル (vcfg) に保存されます。 これにより、複数の Lync Server コントロールパネルセッション中に、変更を公開する前に、ボイスルーティング構成の変更を行うことができます。



</div>

<div>

## <a name="in-this-section"></a>このセクション中

  - [ボイスルート構成ファイルを Lync Server 2013 でエクスポートする](lync-server-2013-export-a-voice-route-configuration-file.md)

  - [Lync Server 2013 でのボイス ルート構成ファイルのインポート](lync-server-2013-import-a-voice-route-configuration-file.md)

</div>

<div>

## <a name="related-sections"></a>関連項目

</div>

</div>

<span> </span>

</div>

</div>

</div>

