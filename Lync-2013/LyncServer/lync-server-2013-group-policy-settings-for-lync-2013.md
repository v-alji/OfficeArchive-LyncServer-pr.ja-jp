---
title: 'Lync Server 2013: Lync 2013 のグループポリシー設定'
description: 'Lync Server 2013: Lync 2013 のグループポリシー設定。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Group Policy settings for Lync 2013
ms:assetid: 5917a52b-dae0-4ec0-8548-a68dc20ab71c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204924(v=OCS.15)
ms:contentKeyID: 48184235
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5c6f2b26fc19653b0098ed4775df1f9c8146986c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427783"
---
# <a name="group-policy-settings-for-lync-2013"></a>Lync 2013 のグループポリシー設定

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-10-03_

以前のバージョンの Lync と Office Communicator では、スタンドアロンの Communicator 管理用テンプレートを使用してクライアントグループポリシー設定を構成できました。 Lync 2013 では、新しい管理用テンプレートファイル (admx および adml ファイル) が、Office グループポリシー管理用テンプレートと共に含まれています。 Lync 2013 の admx ファイルと adml ファイルを使用できるかどうかによって、テンプレートをダウンロードし、すべての Office プログラムと言語パックのグループポリシー設定を一元管理できます。 詳細については、Office 2013 ドキュメントの「Office 2013 管理用テンプレートファイル (ADMX、ADML)」を参照してください <https://go.microsoft.com/fwlink/p/?linkid=267516> 。

<div>

## <a name="client-bootstrapping-policies"></a>クライアントブートストラップポリシー

ユーザーが初めてサーバーにサインインする前に構成する必要があるクライアントブートストラップポリシーはいくつかあります。 これらのポリシーは、クライアントがサインインしてサーバーからインバンドのプロビジョニング設定を受信する前に有効になるため、グループポリシーを使って構成することができます。 詳細については、展開ドキュメントの「 [Lync Server 2013 でのクライアントブートストラップポリシーの構成](lync-server-2013-configuring-client-bootstrapping-policies.md) 」を参照してください。

</div>

</div>

<span> </span>

</div>

</div>

</div>

