---
title: 'Lync Server 2013: IIS 要求のトレースログファイルを監視する'
description: 'Lync Server 2013: IIS 要求トレースログファイルを監視します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Monitoring IIS request tracing log files
ms:assetid: b6730e92-6d74-4fa7-a83f-50b7bdadbffa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690034(v=OCS.15)
ms:contentKeyID: 48185215
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 09692b79b1cc59ad18ad520885c0a795736b53cd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425417"
---
# <a name="monitoring-iis-request-tracing-log-files-in-lync-server-2013"></a>Lync Server 2013 で IIS 要求トレースのログファイルを監視する

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2013-02-14_

    This topic applies to deployments supporting Lync 2010 Lync Mobile clients only, and is intended for the Mobility Service (Mcx).

Lync Server Mobility Service (Mcx) のインターネットインフォメーションサービス (IIS) 要求のトレースを有効にすると、生成されたログファイルは1日に最大 3 gb のディスク領域を消費する可能性があります。 IIS トレースログは既定で有効になっています。 フロントエンドサーバーを監視して、ディスク領域が不足していないことを確認する必要があります。

既定では、IIS は、ログファイルを% SystemDrive% inetpub logs ログログに保存し \\ \\ \\ ます。

サーバー全体で IIS 要求トレースをオフにするには、コマンド ラインで次のように入力します。

    %SystemDrive%\Windows\System32\inetsrv\appcmd set config /section:httpLogging /dontLog:True

**HttpLogging** コマンドの詳細については、を参照してください [https://go.microsoft.com/fwlink/p/?linkId=234927](https://go.microsoft.com/fwlink/p/?linkid=234927) 。

</div>

<span> </span>

</div>

</div>

</div>

