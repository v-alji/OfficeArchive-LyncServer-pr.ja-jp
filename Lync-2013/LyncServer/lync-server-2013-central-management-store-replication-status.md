---
title: 'Lync Server 2013: 中央管理ストアのレプリケーションの状態'
description: 'Lync Server 2013: サーバーの全体管理ストアのレプリケーションの状態。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Central management store replication status
ms:assetid: f514f88d-986b-4e45-b79b-e04a7616c1fe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720926(v=OCS.15)
ms:contentKeyID: 63969663
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5f1f9008a966040cf34ac0499c023f9dbe53a541
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435461"
---
# <a name="central-management-store-replication-status-in-lync-server-2013"></a>Lync Server 2013 での中央管理ストアのレプリケーションの状態

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2015-01-26_

管理者が Lync Server に何らかの変更を加えた場合 (たとえば、管理者が新しい音声ポリシーを作成した場合や、アドレス帳サーバー構成設定を変更した場合など)、その変更は中央管理ストアに記録されます。 次に、Lync Server サービスまたはサーバーの役割を実行しているすべてのコンピューターに変更を複製する必要があります。

データをレプリケートするために、(中央管理サーバー上で動作している) マスター レプリケーターは、変更後の構成データのスナップショットを作成します。 次に、このスナップショットのコピーが、Lync Server サービスまたはサーバーの役割を実行している各コンピューターに送信されます。 それらのコンピューター上では、レプリケーション エージェントがスナップショットを受信し、変更後のデータをアップロードします。 次に、エージェントは、マスター レプリケーターに、レプリケーションの最新の状態を報告するメッセージを送信します。

Get-CsManagementStoreReplicationStatus コマンドレットを使用すると、組織内のすべての Lync Server コンピューターのレプリケーションの状態を確認できます。

このコマンドレットを実行できるユーザー: 既定では、次のグループのメンバーが、Get-CsManagementStoreReplicationStatus  コマンドレットのローカル実行を承認されています。 RTCUniversalUserAdmins、RTCUniversalServerAdmins。

このコマンドレットが割り当てられたすべての RBAC ロール (自分自身で作成したカスタム RBAC ロールを含む) の一覧を返すには、Windows PowerShell プロンプトから次のコマンドを実行します。

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Get-CsManagementStoreReplicationStatus"}

<div>

## <a name="see-also"></a>関連項目


[Get-CsManagementStoreReplicationStatus](https://docs.microsoft.com/powershell/module/skype/Get-CsManagementStoreReplicationStatus)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

