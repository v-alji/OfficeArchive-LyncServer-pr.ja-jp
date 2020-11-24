---
title: 'Lync Server 2013: ダイヤルインの会議ポリシーを構成する'
description: 'Lync Server 2013: ダイヤルインの会議ポリシーを構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure conferencing policy for dial-in
ms:assetid: 9bf926d6-0248-4352-98c3-9c5a333debbc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398810(v=OCS.15)
ms:contentKeyID: 48184979
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dd8dee1d9e7e6391c6420b15a895199dfc7a8791
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399938"
---
# <a name="configure-conferencing-policy-for-dial-in-in-lync-server-2013"></a>Lync Server 2013 でダイヤルインの会議ポリシーを構成する

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2014-03-21_

会議ポリシーは、参加者向けの会議機能を指定するユーザー アカウント設定です。会議ポリシーは、サイト スコープまたはユーザー スコープで作成できます。会議ポリシー設定には、会議の予約と参加の多くの側面が含まれます。複数の会議ポリシー設定で、参加者向けのダイヤルイン会議をサポートしています。ダイヤルイン会議を構成する際に、これらのフィールドが組織に適切に設定されていることを確認し、必要に応じて変更する必要があります。

会議ポリシーの次のフィールドを確認します。

  - **参加者に匿名ユーザーの招待を許可する**   この設定により、会議の開催者は、会議に匿名の参加者 (つまり、認証されていない人) を招待することができます。 ダイヤルイン会議では、この設定は省略可能です。 既定では、既定で [グローバル会議] ポリシーに設定されています。

  - **PSTN ダイヤルイン会議を有効にする**   この設定により、ユーザーは PSTN からダイヤルインして、会議のオーディオ部分に参加することができます。 この設定は、ダイヤルイン会議では必須です。 既定では、既定で [グローバル会議] ポリシーに設定されています。

  - **匿名の参加者にダイヤルアウトを許可する**   この設定では、既に会議に参加している匿名ユーザーが電話番号にダイヤルアウトして、会議のオーディオ部分に参加することを許可します。 ダイヤルイン会議では、この設定は省略可能です。 既定では、既定では、既定では [グローバル会議] ポリシーが選択されていません。

  - **参加者がエンタープライズ voip に対して有効になっていないダイヤルアウトを許可する**   この設定では、エンタープライズボイスに対して有効になっていない会議の参加者と開催者が、電話会議のオーディオ部分に参加するための電話番号にダイヤルアウトすることを許可します。 ダイヤルアウト通話は、開催者に割り当てられた音声ポリシーに基づいて承認されます。 既定では、既定では、既定では [グローバル会議] ポリシーが選択されていません。 設定の既定値が無効になっています。
    
    <div>
    

    > [!NOTE]  
    > この機能を有効にするには、エンタープライズボイスに対して有効になっていない会議開催者には、そのユーザーが開催した会議からのダイヤルアウトを承認する適切な音声ポリシーが割り当てられている必要があります。 ボイスポリシーは、Lync Server 管理シェルからエンタープライズ Voip が有効になっていないユーザーに割り当てることができます。 ユーザーに対して明示的に音声ポリシーが割り当てられていない場合は、サイトのボイスポリシーがダイヤルアウト要求を承認するために使用されます。 サイトのボイスポリシーがない場合は、グローバルボイスポリシーが使用されます。&nbsp;

    
    </div>

このセクションの手順では、会議ポリシーを変更する方法について説明します。 既定の会議ポリシーで参加者エクスペリエンスを定義するすべての設定を構成する方法の詳細については、「 [Lync Server 2013 で会議の構成設定のコレクションを作成または変更](lync-server-2013-create-or-modify-a-collection-of-meeting-configuration-settings.md)する」を参照してください。 特定のユーザーまたはユーザーのグループに対して会議ポリシーを作成する方法の詳細については、「 [Lync Server 2013 で会議ポリシーを作成または変更](lync-server-2013-create-or-modify-a-conferencing-policy.md)する」を参照してください。 利用可能なすべての会議ポリシー設定の一覧については、「 [Lync Server 2013 の会議ポリシー設定リファレンス](lync-server-2013-conferencing-policy-settings-reference.md)」を参照してください。

<div>

## <a name="to-modify-the-conferencing-policy-for-dial-in"></a>ダイヤルインの会議ポリシーを変更するには

1.  RTCUniversalServerAdmins グループのメンバーとして、または **Cs-serveradministrator** または **csadministrator** の役割のメンバーとしてコンピューターにログオンします。

2.  ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。 Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。

3.  左側のナビゲーション バーで [**会議**] をクリックします。

4.  [ **会議ポリシー** ] タブで、会議ポリシー名をダブルクリックして、[ **会議ポリシーの編集** ] ダイアログボックスを開きます。

5.  ダイヤルイン会議のフィールドが組織に適していることを確認し、必要に応じて設定を変更します。

6.  [**コミット**] をクリックします。

</div>

</div>

<span> </span>

</div>

</div>

</div>

