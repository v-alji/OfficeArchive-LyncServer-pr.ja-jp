---
title: 'Lync Server 2013: 会議の Location-Based ルーティングの要件'
description: 'Lync Server 2013: 会議の Location-Based ルーティングの要件。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Requirements for Location-Based Routing for conferencing
ms:assetid: 766d9286-2c34-4faf-bb3e-f0ca478a70cf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362806(v=OCS.15)
ms:contentKeyID: 56335085
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fbaa1af2690c3148d2ecfb173b13be288a21d80f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442664"
---
# <a name="requirements-for-location-based-routing-for-conferencing-in-lync-server-2013"></a>Lync Server 2013 での会議の Location-Based ルーティングの要件

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2013-07-19_

Location-Based ルーティング会議アプリケーションをインストールして構成するために必要な要件を次に示します。

  - Lync Server 2013 累積更新プログラム2は、トポロジ内のすべてのサーバーまたはプールに展開する必要があります。

<div>


> [!NOTE]  
> トポロジ内の Lync サーバーまたはプールに Lync Server 2013 累積更新プログラム2以降がインストールされていない場合、Lync 会議の Location-Based ルーティングを適用することはできません。



</div>

  - Lync Server 2013 Location-Based ルーティングは、Location-Based ルーティング会議アプリケーションの事前の前提条件です。 Lync Server 2013 Location-Based ルーティングの構成の詳細については、「 [Location-Based ルーティングを構成](lync-server-2013-configuring-location-based-routing.md)する」を参照してください。

  - Location-Based ルーティング会議アプリケーションの要件は、Lync Server 2013 Location-Based ルーティングの要件と同じです。 詳細については、「 [Location-Based ルーティングの計画](lync-server-2013-planning-for-location-based-routing.md)」を参照してください。

<div>

## <a name="supported-servers"></a>サポートされているサーバー

Location-Based ルーティング会議アプリケーションでは、Lync Server 2013 累積更新プログラム2が、トポロジ内のすべての Front-End プールおよび標準エディションサーバーに展開されている必要があります。 使用しているトポロジの一部の Lync サーバーに Lync Server 2013 累積更新プログラム2がインストールされていない場合、Location-Based ルーティングの制限は、Lync 会議とコンサルティングによる通話転送に完全に適用することはできません。

次の表では、Location-Based ルーティングをサポートするサーバーの役割とバージョンの組み合わせを示します。


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>フロント エンド プールのバージョン</p></td>
<td><p>仲介サーバーのバージョン</p></td>
<td><p>サポート対象</p></td>
</tr>
<tr class="even">
<td><p>Lync Server 2013 累積更新プログラム 2</p></td>
<td><p>Lync Server 2013 累積更新プログラム 2</p></td>
<td><p>はい</p></td>
</tr>
<tr class="odd">
<td><p>Lync Server 2013 累積更新プログラム 2</p></td>
<td><p>Lync Server 2013 累積更新プログラム 1</p></td>
<td><p>不可</p></td>
</tr>
<tr class="even">
<td><p>Lync Server 2013 累積更新プログラム 2</p></td>
<td><p>Lync Server 2010</p></td>
<td><p>不可</p></td>
</tr>
<tr class="odd">
<td><p>Lync Server 2013 累積更新プログラム 2</p></td>
<td><p>Office Communications Server 2007 R2</p></td>
<td><p>不可</p></td>
</tr>
<tr class="even">
<td><p>Lync Server 2013 累積更新プログラム 1</p></td>
<td><p>任意</p></td>
<td><p>不可</p></td>
</tr>
<tr class="odd">
<td><p>Lync Server 2010</p></td>
<td><p>任意</p></td>
<td><p>不可</p></td>
</tr>
<tr class="even">
<td><p>Office Communications Server 2007 R2</p></td>
<td><p>任意</p></td>
<td><p>不可</p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="supported-clients"></a>サポートされているクライアント

Lync 会議の Location-Based ルーティングをサポートする Lync クライアントは、Lync Server 2013 Location-Based ルーティングをサポートしているクライアントと同じです。 詳細については、「 [クライアントとサーバーの Location-Based ルーティングのサポート](lync-server-2013-client-and-server-support-for-location-based-routing.md)」を参照してください。

</div>

<div>

## <a name="mediation-server-requirements-for-consultative-call-transfers"></a>提案型通話転送の仲介サーバー要件

Location-Based ルーティング会議アプリケーションでは、提案された通話転送に Location-Based ルーティングの制限を適用するために、スタンドアロンの仲介サーバーを展開する必要があります。

提案型の通話転送の Location-Based ルーティングを適用するには、Location-Based ルーティングが必要なネットワーク領域に、仲介サーバーが1つの仲介サーバーピア (PBX、SIP ゲートウェイなど) と関連付けられている必要があります。 追加の仲介サーバーピアが同じネットワーク領域に展開されている場合、仲介サーバーピアは、別の仲介サーバーと関連付けられている必要があります。 この要件は、次のように詳細に説明します。

  - 複数の仲介サーバーピアに対して1つの仲介サーバーを使用して、複数の SIP trunks で構成されている仲介サーバー経由で、複数のピア (Pbx とゲートウェイ) に対して、コンサルタントによる通話転送が仲介サーバーピアにルーティングされる場合、特定の SIP trunks での提案型通話転送が許可されているが、他の
    
    たとえば、PSTN ゲートウェイ仲介サーバーピアと PBX 仲介サーバーピアをサービスしている単一の仲介サーバーの場合、次の動作が監視されます。
    
      - 特定のサイトの Lync ユーザー (つまり、サイト 1) から別のサイト (つまり、サイト 2) の Lync ユーザーに対して、提案型転送を使用して通話を転送しようとすると、PSTN の有料通話を防ぐことはできません。
    
      - 特定のサイトの Lync ユーザー (サイト 1) と、別のサイト (サイト 1) の PBX エンドポイントを使用して、別のサイト (サイト 2) との通話を発信しようとすると、PSTN 通話の可能性がある場合でも、通話は許可されません。

  - 仲介サーバーピアごとに個別の仲介サーバー
    
    提案型転送が仲介サーバーピアを対象としている場合は、仲介サーバーによって処理される単一の仲介サーバーピアに対して、コンサルティング転送が評価されます。 この通話は、サイト内の他のすべての Mediations サーバーピアが、個別の仲介サーバーによってサービスされている場合でも、PSTN の有料電話による通話は許可されません。
    
    たとえば、PSTN ゲートウェイ仲介サーバーピアと PBX 仲介サーバーピアをサービスしている別個の仲介サーバーがある場合は、次の動作が監視されます。
    
      - 特定のサイトの Lync ユーザー (つまり、サイト 1) から別のサイト (つまり、サイト 2) の Lync ユーザーに対して、提案型転送を使用して通話を転送しようとすると、PSTN の有料通話を防ぐことはできません。
    
      - 特定のサイトの Lync ユーザー (サイト 1) と、別のサイト (サイト 1) の PBX エンドポイントを使用して、別のサイト (サイト 2) との通話を発信しようとすると、PSTN 通話の可能性があるため、通話は許可されません。

</div>

<div>

## <a name="capabilities-not-supported-by-the-location-based-routing-conferencing-application"></a>Location-Based ルーティング会議アプリケーションでサポートされていない機能

Location-Based ルーティング会議アプリケーションでは、次の機能はサポートされていません。

  - ダイヤルイン会議。 Location-Based ルーティングは、ダイヤルイン会議には適用できません。 会議開催者が、Location-Based のルーティングが有効になっている Lync ユーザーであっても、特定の会議へのダイヤルイン要求は Location-Based ルーティングによって制限されません。

  - Location-Based ルーティング制限を適用する必要がある地域では、会議アクセス番号をプロビジョニングしないことをお勧めします。

</div>

</div>

<span> </span>

</div>

</div>

</div>

