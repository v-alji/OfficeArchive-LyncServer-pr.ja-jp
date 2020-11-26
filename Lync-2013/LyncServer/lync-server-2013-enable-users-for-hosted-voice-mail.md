---
title: 'Lync Server 2013: ホスト型ボイス メールに対するユーザーの有効化'
description: 'Lync Server 2013: ホストされているボイスメールのユーザーを有効にします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable users for hosted voice mail
ms:assetid: fa559f8f-ef99-43a1-b580-9e998b95efb8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413062(v=OCS.15)
ms:contentKeyID: 48185919
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3853a70d433c09029a02f2ca6256b5988defdcb2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437470"
---
# <a name="enable-users-for-hosted-voice-mail-in-lync-server-2013"></a>Lync Server 2013 でのホスト型ボイス メールに対するユーザーの有効化

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-09-24_

手順に従って、ホストされている Exchange ユニファイドメッセージング (UM) サービスで Lync Server 2013 ユーザーのボイスメールを有効にします。

詳細については、計画ドキュメントの「 [Lync Server 2013 でのホスト型 Exchange ユーザーの管理](lync-server-2013-hosted-exchange-user-management.md) 」を参照してください。

[Set-CsUser](https://docs.microsoft.com/powershell/module/skype/Set-CsUser)コマンドレットの詳細については、「Lync Server 管理シェルのドキュメント」を参照してください。

<div>


> [!IMPORTANT]  
> ホストされたボイスメールに対して Lync Server 2013 ユーザーを有効にする前に、ユーザーアカウントに適用されるホスト型ボイスメールのポリシーを展開する必要があります。 詳細については、「 <A href="lync-server-2013-hosted-voice-mail-policies.md">Lync Server 2013 のホスト型ボイスメールポリシー</A>」を参照してください。



</div>

<div>

## <a name="to-enable-users-for-hosted-voice-mail"></a>ユーザーがホストされたボイスメールを有効にするには

1.  Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。

2.  Set-CsUser コマンドレットを実行して、ホストされたボイスメールのユーザーアカウントを構成します。 たとえば、以下を実行します。
    
        Set-CsUser -HostedVoiceMail $True -Identity "contoso\kenmyer"
    
    上述の例では、次のパラメーターが設定されます。
    
      - **HostedVoiceMail** を使用すると、ユーザーのボイスメール通話を、ホスティングされている Exchange UM にルーティングすることができます。 また、Microsoft Lync 2013 には、"ボイスメールの呼び出し" インジケーターが表示されるように通知されます。
    
      - **Id** は、変更するユーザーアカウントを指定します。 Id 値は、次の形式のいずれかを使用して指定できます。
        
          - ユーザーの SIP アドレス
        
          - ユーザーの Active Directory ユーザープリンシパル名
        
          - ユーザーのドメイン \\ ログオン名 (たとえば、contoso \\ kenmyer)
        
          - ユーザーの Active Directory ドメインサービス Display-Name (Ken Myer など)。 Display-Name を Id 値として使用する場合は、アスタリスク ( \* ) ワイルドカード文字を使用できます。 たとえば、"smith" という Id を指定すると、" \* smith" という文字列で終わる Display-Name を持つすべてのユーザーが返されます。
        
        <div>
        

        > [!NOTE]  
        > SAM アカウント名はフォレスト内で必ずしも一意ではないため、ユーザーの Active Directory SAM アカウント名を Id 値として使用することはできません。

        
        </div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

