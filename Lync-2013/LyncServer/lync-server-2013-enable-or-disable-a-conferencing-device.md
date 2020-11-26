---
title: 'Lync Server 2013: 会議デバイスを有効または無効にする'
description: 'Lync Server 2013: 会議デバイスを有効または無効にします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable or disable a conferencing device
ms:assetid: d5140e38-d015-4706-9bde-cf2fa748c36b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994070(v=OCS.15)
ms:contentKeyID: 51803981
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 761bc19536c889cced68ff586753f6800df0da59
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437575"
---
# <a name="enable-or-disable-a-conferencing-device-in-lync-server-2013"></a>Lync Server 2013 で会議デバイスを有効または無効にする

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**トピックの最終更新日:** 2013-02-20_

お使いの会議デバイスを有効または無効にするには、 **Csroom room** コマンドレットと **csroom room** コマンドレットを使用します。 これらのコマンドレットは、Lync Server 2013 管理シェルまたは Windows PowerShell のリモート セッションから実行できます。

<div>


> [!NOTE]  
> リモートの Windows PowerShell を使用して Lync Server に接続する方法について詳しくは、Lync Server Windows PowerShell のブログ記事「Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell (クイックスタート: リモート PowerShell を使用した Microsoft Lync Server 2010 の管理)」を<A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A>で参照してください。



</div>

<div>


<div>

## <a name="enabling-a-conferencing-device"></a>会議デバイスを有効にする

  - 会議デバイスを有効にするには、 **Csroom room** コマンドレットを使用します。 会議デバイスを有効にする場合は、会議デバイス id、b) 会議室のアカウントが所属するレジストラープール、およびそのアカウントに割り当てられる SIP アドレスを含める必要があります。
    
        Enable-CsMeetingRoom -Identity "Redmond Conferencing device" -RegistrarPool "atl-cs-001.litwareinc.com" -SipAddress "sip:RedmondMeetingRoom@litwareinc.com"

</div>

<div>

## <a name="disabling-a-conferencing-device"></a>会議デバイスの無効化

  - 会議デバイスを無効にするには、 **Csroom room** コマンドレットを使用します。 無効にする会議デバイスの id を指定していることを確認してください。
    
        Disable-CsMeetingRoom -Identity "sip:RedmondMeetingRoom@litwareinc.com"

</div>

詳細については、「 [Csroom room room](https://docs.microsoft.com/powershell/module/skype/Enable-CsMeetingRoom) !」コマンドレットと「 [csroom room room](https://docs.microsoft.com/powershell/module/skype/Disable-CsMeetingRoom) コマンドレットを無効にする」のヘルプトピックを参照してください。

</div>

</div>

<span> </span>

</div>

</div>

</div>

