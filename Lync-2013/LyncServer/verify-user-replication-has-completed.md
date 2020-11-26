---
title: ユーザー レプリケーションの完了の確認
description: ユーザーの複製が完了したことを確認します。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Verify user replication has completed
ms:assetid: 119e9896-45e5-4f8b-af43-7b09360ada0b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204680(v=OCS.15)
ms:contentKeyID: 48183441
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 60bca44fcce811c29b1633bd4d3a39f832851885
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446073"
---
# <a name="verify-user-replication-has-completed"></a>ユーザー レプリケーションの完了の確認

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-09-17_

**移動-csuser** コマンドレットを実行しているときに、最初のレプリケーションが完了していないため、Active Directory ドメインサービス (AD DS) と Lync Server 2013 データベース間のユーザー情報が同期されていないため、エラーが発生する可能性があります。 Lync Server 2013 ユーザーレプリケーターサービスの初回の同期が正常に完了するまでにかかる時間は、Lync Server 2013 プールをホストしている Active Directory フォレストでホストされているドメインコントローラーの数によって異なります。 Lync server 2013 ユーザーレプリケーターサービスの初期同期処理は、Lync Server 2013 フロントエンドサーバーが初めて起動されたときに発生します。 その後、同期はユーザーレプリケーターの間隔に基づいています。 次の手順を実行して、ユーザーの複製が完了したことを確認してから、 **移動-csuser** コマンドレットを実行します。

<div>

## <a name="to-verify-user-replication-has-completed"></a>ユーザーの複製が完了したことを確認するには

1.  トポロジ ビルダーがインストールされているコンピューターに、Domain Admins グループおよび RTCUniversalServerAdmins グループのメンバーとしてログオンします。

2.  [ **スタート** ] メニューをクリックし、[ **実行**] をクリックします。

3.  **eventvwr.exe** を入力し、[ **OK]** をクリックします。

4.  イベントビューアーで [ **アプリケーションとサービスログ** ] をクリックして展開し、[Lync Server] を選択します。

5.  **操作** ウィンドウで、[**現在のログをフィルター**] をクリックします。

6.  [ **イベントソース** ] ボックスの一覧の [ **LS ユーザーレプリケーター**] をクリックします。

7.  **\<All Event IDs\>**「 **30024** 」と入力して、[ **OK]** をクリックします。

8.  [フィルター処理されたイベント] ボックスの一覧の **[全般** ] タブで、ユーザーの複製が正常に完了したことを示すエントリを探します。

</div>

</div>

<span> </span>

</div>

</div>

</div>

