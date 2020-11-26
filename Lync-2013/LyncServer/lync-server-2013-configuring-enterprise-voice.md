---
title: 'Lync Server 2013: エンタープライズ Voip の構成'
description: 'Lync Server 2013: エンタープライズ Voip を構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Enterprise Voice
ms:assetid: 7df179fa-d3a2-4b23-a433-b750aedf980b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994041(v=OCS.15)
ms:contentKeyID: 51803952
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 49a231b92bf7b04aa3466927a79258f0cbad4e3f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433123"
---
# <a name="configuring-enterprise-voice-in-lync-server-2013"></a>Lync Server 2013 でのエンタープライズ Voip の設定

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2013-03-12_

エンタープライズ Voip を展開するには、次の設定を行う必要があります。

  - トランクを作成する

  - ボイスポリシーを定義する

  - ボイスルートの定義

  - Enable Users for Enterprise Voice

<div>

## <a name="create-a-trunk"></a>トランクを作成する

エンタープライズ Voip 展開で trunks を定義する必要があります。 Location-Based ルーティングの場合は、トランクごとにトランク構成を作成する必要があります。 Lync Server Topology Builder を使用して、trunks を定義し、Lync Server Windows PowerShell コマンド、新規 Set-cstrunkconfiguration、Lync Server コントロールパネルを使用して、対応するトランク構成を定義します。 トランク構成での Location-Based ルーティングを有効にする方法について詳しくは、「Trunks へのルーティング Location-Based を有効にする」を参照してください。「 [Lync Server 2013 で Location-Based ルーティング](lync-server-2013-enabling-location-based-routing.md)を有効にする」を参照してください。 この例では、次の表はこのシナリオで使用される trunks を示しています。

詳細については、「 [Lync Server 2013 のトポロジビルダーで追加の trunks を定義](lync-server-2013-define-additional-trunks-in-topology-builder.md)する」を参照してください。


<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th>トランク名</th>
<th>システムの種類</th>
<th>名前</th>
<th>場所</th>
<th>仲介サーバー</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>トランク1の DEL-GW</p></td>
<td><p>PSTN ゲートウェイ</p></td>
<td><p>DEL-GW</p></td>
<td><p>Delhi</p></td>
<td><p>MS1</p></td>
</tr>
<tr class="even">
<td><p>トランク 2 HYD</p></td>
<td><p>PSTN ゲートウェイ</p></td>
<td><p>HYD</p></td>
<td><p>Hyderabad</p></td>
<td><p>MS1</p></td>
</tr>
<tr class="odd">
<td><p>トランク 3 DEL-PBX</p></td>
<td><p>PBX</p></td>
<td><p>DEL-PBX</p></td>
<td><p>Delhi</p></td>
<td><p>MS1</p></td>
</tr>
<tr class="even">
<td><p>トランク 4 HYD</p></td>
<td><p>PBX</p></td>
<td><p>HYD</p></td>
<td><p>Hyderabad</p></td>
<td><p>MS1</p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="defines-voice-policies"></a>ボイスポリシーを定義します

エンタープライズ Voip の展開には、音声ポリシーを定義する必要があります。 ボイスポリシーを定義して、Location-Based ルーティングを使用するために必要なユーザーが一部しかない場合は、ユーザーのサブセットに対して Location-Based ルーティングの制限を適用します。 この例では、次の表はこのシナリオで使用される音声ポリシーを示しています。 この表には、Location-Based ルーティングに固有の設定のみが含まれています。

詳細については、「 [ボイスポリシーと PSTN 使用状況レコードを構成して、Lync Server 2013 での通話機能と特権を承認する](lync-server-2013-configuring-voice-policies-and-pstn-usage-records-to-authorize-calling-features-and-privileges.md)」を参照してください。


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th>ボイスポリシー1</th>
<th>ボイスポリシー2</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ボイスポリシー ID</p></td>
<td><p>ニューデリーのボイスポリシー</p></td>
<td><p>Hyderabad ボイスポリシー</p></td>
</tr>
<tr class="even">
<td><p>PSTN の使用状況</p></td>
<td><p>ニューデリー使用量, PBX Del usage, PBX Hyd usage</p></td>
<td><p>Hyderabad usage、PBX Hyd usage、PBX Del usage</p></td>
</tr>
<tr class="odd">
<td><p>PreventPSTNTollBypass</p></td>
<td><p>False</p></td>
<td><p>False</p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="define-voice-routes"></a>ボイスルートの定義

エンタープライズ Voip 展開には、ボイスルーティングを定義する必要があります。 この例では、次の表はこのシナリオで使用されるボイスルートを示しています。 この表には、Location-Based ルーティングに固有の設定のみが含まれています。

詳細については、「 [Lync Server 2013 で送信通話の音声ルートを構成する](lync-server-2013-configuring-voice-routes-for-outbound-calls.md)」を参照してください。


<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th>ボイスルート1</th>
<th>ボイスルート2</th>
<th>ボイスルート3</th>
<th>ボイスルーティング4</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>名前</p></td>
<td><p>ニューデリールート</p></td>
<td><p>Hyderabad ルート</p></td>
<td><p>PBX の Del ルート</p></td>
<td><p>PBX Hyd ルート</p></td>
</tr>
<tr class="even">
<td><p>PSTN の使用状況</p></td>
<td><p>ニューデリーの利用状況</p></td>
<td><p>Hyderabad の使用状況</p></td>
<td><p>PBX の Del の利用状況</p></td>
<td><p>PBX Hyd の使用</p></td>
</tr>
<tr class="odd">
<td><p>トランク</p></td>
<td><p>トランク1の DEL-GW</p></td>
<td><p>トランク 2 HYD</p></td>
<td><p>トランク 3 DEL-PBX</p></td>
<td><p>トランク 4 HYD</p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="enable-users-for-enterprise-voice"></a>Enable Users for Enterprise Voice

エンタープライズ Voip のユーザーを有効にし、以前に定義した音声ポリシーを割り当てます。 この例では、次の表はこのシナリオで使用される割り当てを示しています。 この表には、Location-Based ルーティングに固有の設定のみが含まれています。

詳細については、「 [Lync Server 2013 でエンタープライズ voip のユーザーを有効にする](lync-server-2013-enable-users-for-enterprise-voice.md)」を参照してください。


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th>ニューデリーにあるユーザ</th>
<th>Hyderabad にあるユーザー</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>関連付けられている音声ポリシー</p></td>
<td><p>ニューデリーのボイスポリシー</p></td>
<td><p>Hyderabad ボイスポリシー</p></td>
</tr>
<tr class="even">
<td><p>サンプルユーザー</p></td>
<td><p>DEL-LYNC-1、DEL-LYNC-2、DEL-LYNC-3</p></td>
<td><p>HYD-1、HYD、LYNC-2、HYD、LYNC-3</p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="see-also"></a>関連項目


[Lync Server 2013 の場所に基づくルーティングの構成](lync-server-2013-configuring-location-based-routing.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

