---
title: 'Lync Server 2013: アドレス帳管理の New-CsClientPolicy'
description: 'Lync Server 2013: アドレス帳の管理に New-CsClientPolicy します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New-CsClientPolicy for Address Book management
ms:assetid: ef4415fc-82c4-4dc8-97d1-37a084553343
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429726(v=OCS.15)
ms:contentKeyID: 48185771
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 12c14534c7af447f30a01b1bbbd1679a8375c705
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425111"
---
# <a name="new-csclientpolicy-for-address-book-management-in-lync-server-2013"></a>Lync Server 2013 でのアドレス帳管理の New-CsClientPolicy

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-11-01_

このコマンドレットを実行できるのはどのユーザーですか。既定では、次のグループのメンバーは New-CsClientPolicy コマンドレット: RTCUniversalServerAdmins を実行することを許可されています。 このコマンドレットが割り当てられているすべての役割ベースのアクセス制御 (RBAC) ロールのリストを返すには (自分自身で作成したカスタム RBAC ロールを含む)、Windows PowerShell プロンプトから次のコマンドを実行します。

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "New-CsClientPolicy"}

このコマンドレットを使用して、Lync Server 2013 で利用できる機能をクライアントに提供するための多数の設定を定義 New-CsClientPolicy ます。 アドレス帳サービスの場合は、パラメーター住所録の可用性が重要です。 このパラメーターは、クライアントで利用できるオプションに直接影響を与えます。次の3つのオプションがあります。

  - WebSearchAndFileDownload

  - WebSearchOnly

  - FileDownloadOnly

定義すると、クライアントがアドレス帳にどのようにアクセスするかを決定します。 このパラメーターを定義する場合は、いずれかのオプションを定義する必要があります。 この設定を変更しない場合、既定の WebSearchAndFileDownload は有効なままになります。

次に例を示します。

    New-CsClientPolicy -Identity RedmondClientPolicy -DisableCalendarPresence $True -DisablePhonePresence $True -DisplayPhoto "PhotosFromADOnly" -AddressBookAvailability "WebSearchOnly"

<div>

## <a name="see-also"></a>関連項目


[New-CsClientPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsClientPolicy)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

