---
title: 'Lync Server 2013: 一般的な市外局番の情報を表示する'
description: 'Lync Server 2013: 一般的な市外局番の情報を表示します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View common area phone information
ms:assetid: e652240c-6a3f-4be7-a083-32f24c08e655
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994081(v=OCS.15)
ms:contentKeyID: 51803992
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e4debe9a76118ac0bf1ca711426ce5487009a053
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443378"
---
# <a name="view-common-area-phone-information-in-lync-server-2013"></a>Lync Server 2013 で一般的な市外局番情報を表示する

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**トピックの最終更新日:** 2013-02-20_

組織で使用できるように構成されている一般的なエリア電話に関する情報を表示するには、 **CsCommonAreaPhone** コマンドレットを使用します。 パラメーターを指定せずにこのコマンドレットを使うと、すべての共通エリア電話に関する情報が返されます。 オプションのパラメーターを使うと、情報をフィルター処理する方法が異なります。 たとえば、指定した組織単位 (OU) 内の連絡先オブジェクト、または指定した建物内のすべての連絡先オブジェクトを持つ共通の市外電話をすべて取得できます。 **CsCommonAreaPhone** パラメーターの詳細については、「 [get-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/Get-CsCommonAreaPhone)」を参照してください。

**CsCommonAreaPhone** は、Lync Server 2013 管理シェルから、または Windows PowerShell のリモートセッションから実行します。

<div>


<div>

## <a name="viewing-information-about-all-your-common-area-phones"></a>共通のエリア電話に関する情報を表示する

  - 一般的なすべての地域電話に関する情報を表示するには、Lync Server 管理シェルで次のコマンドを入力し、enter キーを押します。
    
        Get-CsCommonAreaPhone
    
    次のような情報が表示できます。
    
        Identity           : CN=Building 14 Lobby,OU=Redmond,
                             DC=litwareinc,DC=com
        RegistrarPool      : atl-cs-001.litwareinc.com
        Enabled            : True
        SipAddress         : sip:4714e34b-9781-421d-b07a-
                             52056b5b4a56@litwareinc.com
        ClientPolicy       :
        PinPolicy          :
        VoicePolicy        :
        MobilityPolicy     :
        GroupChatPolicy    :
        ConferencingPolicy :
        LineURI            : tel:+14255550712
        DisplayNumber      : 1-425-555-0712
        DisplayName        : Building 14 Lobby
        Description        :
        ExUmEnabled        : False

</div>

詳細については、 [CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/Get-CsCommonAreaPhone) コマンドレットのヘルプトピックを参照してください。

</div>

</div>

<span> </span>

</div>

</div>

</div>

