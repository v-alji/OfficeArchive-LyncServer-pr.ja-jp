---
title: 'Lync Server 2013: エンタープライズボイスコマンドレット'
description: 'Lync Server 2013: エンタープライズボイスコマンドレット。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enterprise Voice cmdlets
ms:assetid: 7d7c6d94-3ead-4d99-95f7-c31b448ab9e2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415658(v=OCS.15)
ms:contentKeyID: 48184613
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 447876de74a63e1def03f41bca512d57c46daf91
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428609"
---
# <a name="enterprise-voice-cmdlets-in-lync-server-2013"></a>Lync Server 2013 のエンタープライズボイスコマンドレット

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2014-03-19_

[エンタープライズボイス] は、Microsoft Voice over IP (VoIP) 実装です。 Microsoft Lync Server 2013 でエンタープライズ Voip を管理するために使用できるコマンドレットを使うと、ダイヤルプラン (以前は位置情報プロファイル)、音声ポリシー、ルート、正規化ルールを作成および変更することができます。

<div>

## <a name="enterprise-voice-cmdlets"></a>エンタープライズ Voip コマンドレット

エンタープライズボイスに適用されるほとんどの管理タスクは、Lync Server コントロールパネルから実行できます。 このようなタスクは、Lync Server 管理シェルからコマンドレットを使用して実行することも、スクリプト内から実行することで、特定のタスクを自動化することもできます。 エンタープライズ Voip の管理に直接関連するコマンドレットの一覧を次に示します。

**[Lync Server 2013 でのエンタープライズボイスコマンドレットのトラブルシューティング](lync-server-2013-troubleshooting-enterprise-voice-cmdlets.md)**

  - <span></span>  
    [Get-CsVoiceConfiguration](https://technet.microsoft.com/library/Gg398815(v=OCS.15))

  - <span></span>  
    [Remove-CsVoiceConfiguration](https://technet.microsoft.com/library/Gg398804(v=OCS.15))

  - <span></span>  
    [Set-CsVoiceConfiguration](https://technet.microsoft.com/library/Gg398967(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [Get-CsVoiceTestConfiguration](https://technet.microsoft.com/library/Gg412957(v=OCS.15))

  - <span></span>  
    [新規-CsVoiceTestConfiguration](https://technet.microsoft.com/library/Gg398961(v=OCS.15))

  - <span></span>  
    [Remove-CsVoiceTestConfiguration](https://technet.microsoft.com/library/Gg412813(v=OCS.15))

  - <span></span>  
    [Set-CsVoiceTestConfiguration](https://technet.microsoft.com/library/Gg398614(v=OCS.15))

  - <span></span>  
    [テスト-CsVoiceTestConfiguration](https://technet.microsoft.com/library/Gg398260(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [Test-CsDialPlan](https://technet.microsoft.com/library/Gg399024(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [テスト-CsVoiceNormalizationRule](https://technet.microsoft.com/library/Gg399003(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [テスト-CsVoicePolicy](https://technet.microsoft.com/library/Gg398310(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [テスト-CsVoiceRoute](https://technet.microsoft.com/library/Gg425873(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [テスト-Get-csvoiceuser](https://technet.microsoft.com/library/Gg413013(v=OCS.15))

**[Lync Server 2013 の音声正規化ルールコマンドレット](lync-server-2013-voice-normalization-rules-cmdlets.md)**

  - <span></span>  
    [Get-CsVoiceNormalizationRule](https://technet.microsoft.com/library/Gg398393(v=OCS.15))

  - <span></span>  
    [新規-CsVoiceNormalizationRule](https://technet.microsoft.com/library/Gg398240(v=OCS.15))

  - <span></span>  
    [Remove-CsVoiceNormalizationRule](https://technet.microsoft.com/library/Gg398501(v=OCS.15))

  - <span></span>  
    [Set-CsVoiceNormalizationRule](https://technet.microsoft.com/library/Gg398491(v=OCS.15))

  - <span></span>  
    [テスト-CsVoiceNormalizationRule](https://technet.microsoft.com/library/Gg399003(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [新規-CsVoiceRegex](https://technet.microsoft.com/library/Gg412751(v=OCS.15))

**[Lync Server 2013 の音声ポリシーコマンドレット](lync-server-2013-voice-policy-cmdlets.md)**

  - <span></span>  
    [Get-CsDialPlan](https://technet.microsoft.com/library/Gg413043(v=OCS.15))

  - <span></span>  
    [Grant-CsDialPlan](https://technet.microsoft.com/library/Gg398547(v=OCS.15))

  - <span></span>  
    [New-CsDialPlan](https://technet.microsoft.com/library/Gg425860(v=OCS.15))

  - <span></span>  
    [Remove-CsDialPlan](https://technet.microsoft.com/library/Gg398791(v=OCS.15))

  - <span></span>  
    [Set-CsDialPlan](https://technet.microsoft.com/library/Gg398644(v=OCS.15))

  - <span></span>  
    [Test-CsDialPlan](https://technet.microsoft.com/library/Gg399024(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [Get-CsPstnUsage](https://technet.microsoft.com/library/Gg412734(v=OCS.15))

  - <span></span>  
    [Set-CsPstnUsage](https://technet.microsoft.com/library/Gg399069(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [Get-CsVoicePolicy](https://technet.microsoft.com/library/Gg398101(v=OCS.15))

  - <span></span>  
    [Grant-CsVoicePolicy](https://technet.microsoft.com/library/Gg398828(v=OCS.15))

  - <span></span>  
    [New-CsVoicePolicy](https://technet.microsoft.com/library/Gg425856(v=OCS.15))

  - <span></span>  
    [Remove-CsVoicePolicy](https://technet.microsoft.com/library/Gg398309(v=OCS.15))

  - <span></span>  
    [Set-CsVoicePolicy](https://technet.microsoft.com/library/Gg399021(v=OCS.15))

  - <span></span>  
    [テスト-CsVoicePolicy](https://technet.microsoft.com/library/Gg398310(v=OCS.15))

**[Lync Server 2013 の音声ルーティングコマンドレット](lync-server-2013-voice-routing-cmdlets.md)**

  - <span></span>  
    [CsRoutingConfiguration を取得する](https://technet.microsoft.com/library/Gg425851(v=OCS.15))

  - <span></span>  
    [新しい-CsRoutingConfiguration](https://technet.microsoft.com/library/Gg399056(v=OCS.15))

  - <span></span>  
    [CsRoutingConfiguration の削除](https://technet.microsoft.com/library/Gg398643(v=OCS.15))

  - <span></span>  
    [設定-CsRoutingConfiguration](https://technet.microsoft.com/library/Gg412811(v=OCS.15))

<!-- end list -->

  - <span></span>  
    [Get-CsVoiceRoute](https://technet.microsoft.com/library/Gg425926(v=OCS.15))

  - <span></span>  
    [新規-CsVoiceRoute](https://technet.microsoft.com/library/Gg398197(v=OCS.15))

  - <span></span>  
    [Remove-CsVoiceRoute](https://technet.microsoft.com/library/Gg398468(v=OCS.15))

  - <span></span>  
    [Set-CsVoiceRoute](https://technet.microsoft.com/library/Gg412893(v=OCS.15))

  - <span></span>  
    [テスト-CsVoiceRoute](https://technet.microsoft.com/library/Gg425873(v=OCS.15))

</div>

<div>

## <a name="see-also"></a>関連項目


[Lync Server 2013 の高度なエンタープライズボイスコマンドレット](lync-server-2013-advanced-enterprise-voice-cmdlets.md)  
[Lync Server 2013 の音声アプリケーションコマンドレット](lync-server-2013-voice-application-cmdlets.md)  


[Lync Server PowerShell ブログ](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

