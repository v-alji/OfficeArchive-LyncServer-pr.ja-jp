---
title: 'Lync Server 2013: (オプション) ダイヤルイン会議の設定の検証'
description: 'Lync Server 2013: (オプション) ダイヤルイン会議の設定を確認します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: (Optional) Verify dial-in conferencing settings
ms:assetid: a85efdda-97b0-4f3b-bd26-04416bee8ef5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412789(v=OCS.15)
ms:contentKeyID: 48185027
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ec002cfbd7cdd67498768a360143f88ab4f8e1b7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445205"
---
# <a name="optional-verify-dial-in-conferencing-settings-in-lync-server-2013"></a>(オプション) Lync Server 2013 でのダイヤルイン会議の設定の検証

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2010-11-02_

ダイヤルイン会議構成の最後の確認作業として、どのアクセス番号も使用しないダイヤルイン会議の地域があるダイヤル プランやダイヤルイン会議の地域が指定されていないアクセス番号を検索します。 この手順は省略可能です。

<div>

## <a name="to-find-dial-plans-with-a-dial-in-conferencing-region-that-is-not-used-by-an-access-number"></a>アクセス番号で使用されていないダイヤルイン会議領域でダイヤルプランを検索するには

1.  RTCUniversalServerAdmins グループのメンバーとして、または **Cs-serveradministrator** または **csadministrator** の役割のメンバーとしてコンピューターにログオンします。

2.  Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。

3.  コマンド プロンプトで次のコマンドを実行します。
    
        Get-CsDialinConferencingAccessNumber -EmptyRegion
    
    このコマンドレットは、どのアクセス番号も使用していないダイヤルイン会議の地域がある、すべてのダイヤル プランを返します。

</div>

<div>

## <a name="to-find-access-numbers-without-assigned-regions"></a>割り当てられている地域のないアクセス番号を検索するには

1.  RTCUniversalServerAdmins グループのメンバーとして、または **Cs-serveradministrator** または **csadministrator** の役割のメンバーとしてコンピューターにログオンします。

2.  Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。

3.  コマンド プロンプトで次のコマンドを実行します。
    
        Get-CsDialinConferencingAccessNumber -Region NULL
    
    このコマンドレットは、地域に関連付けられていないダイヤルイン会議アクセス番号をすべて返します。

</div>

</div>

<span> </span>

</div>

</div>

</div>

