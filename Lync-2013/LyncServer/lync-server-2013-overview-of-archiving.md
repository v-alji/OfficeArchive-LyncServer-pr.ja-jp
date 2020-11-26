---
title: 'Lync Server 2013: アーカイブの概要'
description: 'Lync Server 2013: アーカイブの概要。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of Archiving
ms:assetid: 1e3c2ef1-f561-4f57-8b6a-7d78addc1ed1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204729(v=OCS.15)
ms:contentKeyID: 48183570
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 548d82d6731fd28fafbde5816a7a0dc77a1fcc02
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424829"
---
# <a name="overview-of-archiving-in-lync-server-2013"></a>Lync Server 2013 のアーカイブの概要

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2013-09-30_

Lync server 2013 でのアーカイブは、Lync Server 2013 経由で送信された通信をアーカイブするための手段を提供します。

最初の Lync Server 2013 の展開の一部としてアーカイブを実装することも、既存の展開に追加することもできます。 Lync Server 2013 アーカイブデータベース (SQL Server データベース) を使用してアーカイブデータを保存するには、トポロジビルダーを使用してデータベースをトポロジに追加してから、もう一度トポロジを公開します。 すべてのユーザーが Exchange 2013 を使用していて、メールボックス In-Place 保持されている場合は、トポロジを更新する必要はありませんが、Exchange 2013 でアーカイブデータを保存するために Microsoft Exchange の統合を有効にする必要があります。

アーカイブを実装するときに、アーカイブの内容を指定するように構成します。 既定では、何もアーカイブされません。 アーカイブの構成と管理は、Lync Server 2013 コントロールパネルを使用して行います。 内部通信、外部通信、またはその両方のアーカイブを実装することができます。 組織全体のアーカイブ設定を構成することができます。また、必要に応じて、特定のサイト、特定のプール、特定のユーザーとユーザーグループのアーカイブ設定を構成することもできます。 組織で適切なオプションを決定する方法の詳細については、計画ドキュメントの「 [Lync Server 2013 でアーカイブするための要件を定義](lync-server-2013-defining-your-requirements-for-archiving.md) する」を参照してください。 アーカイブポリシーと構成の実装方法、およびアーカイブできない情報の詳細については、計画ドキュメント、展開ドキュメント、または運用マニュアルの「 [Lync Server 2013 でのアーカイブの動作](lync-server-2013-how-archiving-works.md) 」を参照してください。

</div>

<span> </span>

</div>

</div>

</div>

