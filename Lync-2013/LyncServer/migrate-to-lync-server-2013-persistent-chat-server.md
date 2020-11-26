---
title: Lync Server 2010、グループ チャットまたは Office Communicatins Server 2007 R2 グループ チャットから Lync Server 2013、常設チャット サーバーへの移行
description: Lync Server 2010、グループチャット、または Office Communications Server 2007 R2 グループチャットから Lync Server 2013、常設チャットサーバーへの移行。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migration from Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server
ms:assetid: 5b4d3db1-6eba-4932-b49c-f60bcf9488f9
ms:mtpsurl: https://technet.microsoft.com/library/Gg615442(v=OCS.15)
ms:contentKeyID: 48184240
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6090d5924a203a960444d9a10700fd178d038887
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446858"
---
# <a name="migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server"></a>Lync Server 2010、グループ チャットまたは Office Communicatins Server 2007 R2 グループ チャットから Lync Server 2013、常設チャット サーバーへの移行

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-10-06_

このセクションのトピックでは、Lync Server 2010、グループチャット、または Office Communications Server 2007 R2 グループチャットを Lync Server 2013、常設チャットサーバーに移行するプロセスについて説明します。 Lync server 2013 の常設チャットサーバーの展開と Lync Server 2010、グループチャット、または Office Communications Server 2007 R2 グループチャットの展開については、この混合環境での操作に関する重要な情報も含まれています。 このガイドは主に、常設チャットサーバーのデータ移行に焦点を当てています。 以前のバージョンの Lync Server から Lync Server 2013 に移行しているユーザーの場合は、「 [lync server 2010 から Lync server 2013 に移行](migration-from-lync-server-2010-to-lync-server-2013.md) する」と「 [Office Communications server 2007 R2 から lync server 2013 に](migration-from-office-communications-server-2007-r2-to-lync-server-2013.md)移行する」を参照してください。

<div>


> [!IMPORTANT]  
> このトピックでは、lync server 2010 または Office Communications Server 2007 R2 との共存に、既に Lync Server 2013 をインストールしていることを前提としています。



</div>

<div>


> [!IMPORTANT]  
> このガイドでは、移行の各フェーズを実行するために必要な手順について説明します。 これは、すべてのレガシ展開トポロジまたは可能な移行シナリオには対応していません。 そのため、説明されているすべての手順を実行する必要がない場合や、展開によっては追加の手順を実行する必要がある場合があります。 このガイドには、確認手順の例も用意されています。 これらの検証手順は、移行の進行に応じて各フェーズが正常に完了するために必要な情報を確認するために用意されています。 この確認手順は、特定の移行プロセスに合わせて変更できます。



</div>

このガイドには、既存の展開のアップグレードに固有の情報が記載されています。 既存のトポロジを変更する方法については説明しません。 このガイドでは、新機能の実装については説明しません。 詳細な手順については、別のドキュメントまたはドキュメントの説明を参照してください。

このドキュメントでは、次の一覧で指定された用語を定義しています。

  - *用*  
    以前のバージョンの常設チャットサーバー (旧称グループチャットサーバー) から、Lync Server 2013 の常設チャットサーバーへの展開を移行します。

<!-- end list -->

  - *アップグレード*  
    新しいバージョンのソフトウェアをサーバーまたはクライアントコンピューターにインストールします。

<!-- end list -->

  - *共存*  
    移行時に存在する一時的な環境では、一部の機能が Lync Server 2013 に移行されている場合、常設チャットサーバー、その他の機能が以前のバージョンのグループチャットサーバーに残っている場合に、その他の機能は引き続き維持されます。

常設チャットサーバーは、Lync Server 2013 インフラストラクチャの拡張機能です。 使用しているトポロジに応じて、Lync Server 2010、グループチャット、または Office Communications Server 2007 R2 グループチャットを Lync Server 2013 常設チャットサーバーに移行することができます。 使用可能なトポロジと、グループチャットサーバーを移行するための技術およびソフトウェアの要件の詳細については、計画ドキュメントの「 [Lync server 2013 での常設チャットサーバーの計画](lync-server-2013-planning-for-persistent-chat-server.md) 」を参照してください。

組織でコンプライアンスのサポートが必要な場合は、各常設チャットサーバーと共に自動的にインストールされます。 別のサーバーは、コンプライアンスのために必要とされなくなりました。

<div>


> [!IMPORTANT]  
> ファイルシステムのセキュリティを適用するには、常設チャットサーバーが NTFS ファイルシステムにインストールされている必要があります。 FAT32 は、常設チャットサーバーでサポートされているファイルシステムではありません。<BR>組織でコンプライアンスのサポートが必要な場合は、各常設チャットサーバーと共に自動的にインストールされます。 別のサーバーは、コンプライアンスのために必要とされなくなりました。 Lync Server 2013 常設チャットサーバーでの変更の詳細については、「はじめに」の &nbsp; ドキュメントで「 <A href="lync-server-2013-new-persistent-chat-server-features.md">lync server 2013 の新しい常設チャットサーバー機能</A> 」を参照してください。



</div>

<div>

## <a name="in-this-section"></a>このセクション中

  - [標準移行シナリオ - 概要](standard-migration-scenario-high-level.md)

  - [移行のプロセス - 詳細](migration-process-details.md)

  - [共存の考慮事項](coexistence-considerations.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

