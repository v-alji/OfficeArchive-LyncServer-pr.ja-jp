---
title: 'Lync Server 2013: ユーザー アカウント設定の構成'
description: 'Lync Server 2013: ユーザーアカウント設定を構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure user account settings
ms:assetid: b7c74ecc-b924-4efc-8a56-3a5f94a9ef13
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412896(v=OCS.15)
ms:contentKeyID: 48185200
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e6ab4c57ba3d3e8c084314e1093736334312d0c1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400059"
---
# <a name="configure-user-account-settings-in-lync-server-2013"></a>Lync Server 2013 でのユーザー アカウント設定の構成

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-10-05_

ダイヤルイン ユーザーは各自の電話番号または内線番号、それに PIN を入力し、認証されたユーザーとして会議に参加します。 認証には、Lync Server のユーザーアカウントで指定されたテレフォニー **回線 URI** が必要です。

このトピックの手順は、[**回線 URI**] を 1 つのユーザー アカウントに対して割り当てる方法について説明します。 [**回線 URI**] を複数のユーザー アカウントに対して割り当てる必要がある場合は、**Set-CsUser** コマンドレットを使用するスクリプトを作成できます。 サンプルスクリプトを使用して複数のユーザーアカウントに **行の uri** を割り当てる方法の詳細については、の「複数のユーザーに行の Uri を割り当てる」を参照してください [https://go.microsoft.com/fwlink/p/?linkId=196945](https://go.microsoft.com/fwlink/p/?linkid=196945) 。

<div>

## <a name="to-configure-user-account-settings"></a>ユーザーアカウント設定を構成するには

1.  RTCUniversalServerAdmins グループのメンバーとしてコンピューターにログオンするか、**Cs-UserAdministrator** または **CsAdministrator** の役割のメンバーとしてコンピューターにログオンします。

2.  ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。 Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。

3.  左側のナビゲーション バーで [**ユーザー**] をクリックします。

4.  検索フィールドで、ダイヤルイン会議の構成を行うユーザーの名前を入力するか、[**フィルターの追加**] をクリックして検索フィールドを指定し、次に [**検索**] をクリックします。

5.  ユーザー名をダブルクリックして、[ **Lync Server ユーザーの編集** ] ダイアログボックスを開きます。

6.  [**テレフォニー**] の下の [**回線 URI**] フィールドで、正規化された一意の電話番号 (たとえば、tel:+14255550200) を入力します。
    
    <div>
    

    > [!NOTE]  
    > [<STRONG>回線 URI</STRONG>] を指定できるのは、[<STRONG>テレフォニー</STRONG>] が [<STRONG>PC 間のみ</STRONG>]、[<STRONG>エンタープライズ VoIP</STRONG>]、[<STRONG>リモート通話コントロール</STRONG>]、または [<STRONG>リモート通話コントロールのみ</STRONG>] に設定されている場合のみです。

    
    </div>

7.  [**確定**] をクリックします。

</div>

</div>

<span> </span>

</div>

</div>

</div>

