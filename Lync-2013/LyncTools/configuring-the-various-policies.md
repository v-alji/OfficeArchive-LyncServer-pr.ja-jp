---
title: 各種ポリシーの構成
description: さまざまなポリシーを構成します。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Configuring the Various Policies
ms:assetid: e3b3cbda-7c17-470b-acb0-82fdcc473184
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945610(v=OCS.15)
ms:contentKeyID: 51541436
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 746d299ac605c7dfe89a957246d47309dfbc0a5d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440062"
---
# <a name="configuring-the-various-policies"></a>各種ポリシーの構成

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2013-02-24_

<div>

Lync Server 2013 のストレスとパフォーマンスツールを実行する前に、Lync Server 2013 トポロジで構成できる各種のポリシーを次に示します。

<div>

## <a name="configuring-the-archiving-policy"></a>アーカイブポリシーを構成する

「スクリプトの例 ArchivingPolicy.ps1 を参照してください。 このスクリプトは、アーカイブサーバーがトポロジに展開されている場合にのみ使用する必要があります。 詳細については、「lync Server 2013 のドキュメントとコマンドレットのヘルプ」を参照してください。 [lync server 2013 のコマンドレットのアーカイブと監視](https://technet.microsoft.com/library/gg415629\(v=ocs.15\))を行います。

</div>

<div>

## <a name="configuring-the-conferencing-policy"></a>会議ポリシーを構成する

「スクリプトの例 MeetingPolicy.ps1 を参照してください。 詳細については、「lync Server 2013 ドキュメント」および「 [Lync server 2013 の Web 会議コマンド](https://technet.microsoft.com/library/gg415675\(v=ocs.15\))レットのヘルプ」を参照してください。

</div>

<div>

## <a name="configuring-the-contacts-policy"></a>連絡先ポリシーを構成する

ContactsPolicy.ps1 の例を参照してください。 詳細については、「lync Server 2013 ドキュメント」および「 [Lync server 2013 の IM とプレゼンスのコマンド](https://technet.microsoft.com/library/gg398611\(v=ocs.15\))レットのヘルプ」を参照してください。

</div>

<div>

## <a name="configuring-the-federation-policy"></a>フェデレーションポリシーを構成する

FederationPolicy.ps1 の例を参照してください。 詳細については、「lync server 2013 ドキュメント」および「lync server 2013 での microsoft Lync Server 2013 および[フェデレーションと外部アクセスコマンド](https://technet.microsoft.com/library/gg415651\(v=ocs.15\))レットの[Edge server コマンド](https://technet.microsoft.com/library/gg415635\(v=ocs.15\))レットのヘルプ」を参照してください。

</div>

<div>

## <a name="configuring-the-call-admission-control-policy"></a>通話受付制御ポリシーを構成する

BandwidthPolicy.ps1 の例を参照してください。 詳細については、lync server 2013 の「 [通話受付制御](https://technet.microsoft.com/library/gg398529\(v=ocs.15\)) 」と「lync server [2013 での通話受付制御コマンド](https://technet.microsoft.com/library/gg415676\(v=ocs.15\))レットのヘルプ」を参照し2013てください。

</div>

<div>

## <a name="configuring-the-voice-routing-rules"></a>ボイスルーティングルールを構成する

RoutingRules.ps1 の例を参照してください。 ボイスルーティングルールを構成するときは、電話のコンテキスト (¥ Location Profile または/simplename) と内部/外部の市外局番 (特に PSTN-UC および UC-PSTN 用) を指定して、ユーザーを作成するときに指定できるようにします。 たとえば、RoutingRules.ps1 の例の **CsDialPlan** コマンドレットへの呼び出しの simplename パラメーターは、次の UserProfileGenerator.exe の図の locationprofile 値として使用する必要があります。

![サンプルの音声のルーティング ルール](images/JJ945610.9f34d971-4ed0-4a4c-b101-086a91c4578c(OCS.15).jpg "サンプルの音声のルーティング ルール")

詳細については、「lync Server 2013 ドキュメント」および「 [Lync server 2013 のエンタープライズボイスコマンド](https://technet.microsoft.com/library/gg415658\(v=ocs.15\))レットのヘルプ」を参照してください。

</div>

<div>

## <a name="configuring-conferencing-attendant-application"></a>会議アテンダントアプリケーションの構成

ConferenceAutoAttendantConfiguration.ps1 の例を参照してください。 ConferencingAutoAttendant 電話番号 (既定では 1121111111) をメモし、それを構成の生成用の LyncPerf ツール構成ツールに入力できるようにします。

![会議アテンダント アプリケーションを構成する](images/JJ945610.0618a22f-27a9-423a-9085-d2bf71e82db6(OCS.15).jpg "会議アテンダント アプリケーションを構成する")

詳細については、「lync server 2013 ドキュメント」および「lync server 2013 での [Web 会議コマンド](https://technet.microsoft.com/library/gg415675\(v=ocs.15\)) レットのヘルプ (lync server 2013 および [ダイヤルイン会議コマンド](https://technet.microsoft.com/library/gg415630\(v=ocs.15\))レットのヘルプ)」を参照してください。

</div>

<div>

## <a name="configuring-lync-server-call-park-service"></a>Lync Server コールパークサービスの構成

コールパークは既定では無効になっています。 CallParkConfiguration.ps1 の例を参照してください。 詳細については、「lync Server 2013 ドキュメント」および「 [Lync server 2013 のコールパークアプリケーションコマンドレット](https://technet.microsoft.com/library/gg415639\(v=ocs.15\))のヘルプ」を参照してください。

</div>

<div>

## <a name="configuring-emergency-calls"></a>緊急通話の設定

緊急通話のストレスとパフォーマンスのテストを構成するには、次の手順を実行します。

1.  緊急通話のためのボイスルートを設定します。 このボイスルートを設定する例については、「E911 にルーティングする」の説明を参照し RoutingRules.ps1 てください。
    
    <div>
    

    > [!WARNING]  
    > RoutingRules.ps1 のコマンドの例では、911ではなく数値119を含む数値パターンを使用しています。 ロードテスト中に、ローカルの緊急電話会社に誤って通話を発信しないようにするには、911 (または実際のローカル緊急電話番号) の使用を避ける必要があります。 この構成は、シミュレーション目的でのみ使用されます。

    
    </div>

2.  次の図に示すように、Userプロビジョニングツールの [ **LIS** ] タブの値を入力して、アドレスを構成します。
    
    ![場所情報サービスの構成](images/JJ945610.8ac1faa1-e9f9-40d0-b8b7-b159f4f459f7(OCS.15).jpg "場所情報サービスの構成")  

3.  [ **LIS 構成ファイルの生成**] をクリックします。

4.  ポート、サブネット、スイッチ、ワイヤレスアクセスポイント (Wap) の CSV ファイル、および Lync Server 2013 ストレスおよびパフォーマンスツール用の XML ファイルが生成されます。 CSV ファイルは、LisConfiguration.ps1 スクリプトで場所情報サービス (LIS) を構成するときに、(同じフォルダー内の) 入力として使用されます。 生成された Locations0.xml ファイルを、Lync Server 2013 のストレスとパフォーマンスツールの実行可能ファイル (LyncPerfTool.exe) と同じフォルダーに移動すると、位置情報プロファイル (ダイヤルプラン) のシナリオが実行されます。

</div>

<div>

## <a name="creating-enabling-configuring-and-disabling-users"></a>ユーザーの作成、有効化、構成、無効化

次のスクリプトを実行する前に、すべてのユーザーを作成する必要があります。 「ユーザー [と連絡先を作成して](create-users-and-contacts.md) ユーザーを作成する」の手順に従います。 詳細については、「 [ユーザー](https://technet.microsoft.com/library/gg398125\(v=ocs.15\))用の Lync Server 2013 コマンドレット」を参照してください。また、「ユーザーの [設定](https://technet.microsoft.com/library/gg398510\(v=ocs.15\))」を [参照して](https://technet.microsoft.com/library/gg398747\(v=ocs.15\)) ください。

</div>

<div>

## <a name="configuring-response-group-application"></a>応答グループアプリケーションを構成する

ResponseGroupConfiguration.ps1 の例を参照してください。 詳細については、「Lync Server 2013 ドキュメント」および「 [lync server 2013 のグループアプリケーションコマンドレットに応答](https://technet.microsoft.com/library/gg415654\(v=ocs.15\))するためのコマンドレットのヘルプ」を参照してください。応答グループのアプリケーション構成を確認するには、次の図のように「」を参照し `https://<poolfqdn>/RgsConfig/` てください。

![応答グループ構成ツール](images/JJ945610.480a9440-2283-4533-98f8-86daaab4781c(OCS.15).jpg "応答グループ構成ツール")

</div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

