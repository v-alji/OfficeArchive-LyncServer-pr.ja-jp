---
title: 'Lync Server 2013: 組織内のデバイスのソフトウェア更新プログラムを表示する'
description: 'Lync Server 2013: 組織内のデバイスのソフトウェア更新プログラムを表示します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View software updates for devices in your organization
ms:assetid: d2cca12b-ed43-4e1f-90ab-d14bca8b482c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182592(v=OCS.15)
ms:contentKeyID: 48185418
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 833ab25315847b760271c63bbfca3ba8357e41c1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399212"
---
# <a name="view-software-updates-for-devices-in-lync-server-2013"></a>Lync Server 2013 でのデバイスのソフトウェア更新プログラムの表示

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-11-01_

Lync Server 2013 では、デバイス更新 Web サービスを使って、組織のデバイスのソフトウェア更新プログラムを表示して管理します。 これらの更新プログラムは、の Microsoft サポート web サイトから .cab (キャビネット) ファイルで入手でき [https://go.microsoft.com/fwlink/p/?linkId=204091](https://go.microsoft.com/fwlink/p/?linkid=204091) ます。 .Cab ファイルをダウンロードした後、 **インポート-CSDeviceUpdate** コマンドレットを実行して、.cab ファイルからデバイス更新ルールをインポートします。 **Csdeviceupdate** コマンドレットの詳細については、「Lync Server 管理シェルドキュメントの [インポート-csdeviceupdate](https://docs.microsoft.com/powershell/module/skype/Import-CsDeviceUpdate) 」を参照してください。

<div>


> [!TIP]  
> 新しい更新プログラムを組織に展開する前に、テストデバイスで正しく機能することを確認します。



</div>

<div>

## <a name="to-view-software-updates-for-uc-devices"></a>UC デバイスのソフトウェア更新プログラムを表示するには

1.  CsUserAdministrator または CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。

2.  Microsoft サポート web サイトで [https://go.microsoft.com/fwlink/p/?linkId=204091](https://go.microsoft.com/fwlink/p/?linkid=204091) 、.cab ファイルを Lync Server 2013 コンピューター上の場所にダウンロードします (たとえば、C: \\ Updates \\UCUpdates.cab)。

3.  \\ \\ 次のコマンドレットのいずれかを実行して、C: updateUCUpdates.cab ファイルからデバイス更新ルールをインポートします。
    
      - .Cab ファイルが、更新されるサービスを実行しているコンピューターと同じコンピューター上にある場合 (サービス: レドモンド-websvc-2)、次のコマンドレットを実行します。
        
            Import-CsDeviceUpdate -Identity service:Redmond-websvc-2 -FileName C:\Updates\UCUpdates.cab
    
      - .Cab ファイルが、更新されるサービスを実行しているコンピューターとは異なるコンピューター上にある場合 (サービス: Redmond-websvc-3)、次のコマンドレットを実行します。
        
            Import-CsDeviceUpdate -Identity service:Redmond-websvc-3 -ByteInput C:\Updates\UCUpdates.cab

4.  ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。 Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。

5.  左側のナビゲーションバーで、[ **クライアント**] をクリックし、[ **デバイスの更新**] をクリックします。

6.  [ **デバイス更新** ] ページで、一覧から更新プログラムをクリックし、次のいずれかの操作を行います。
    
      - **保留中の更新をキャンセルします。** 選択した更新プログラムが組織のデバイスに展開されないようにするには、[ **操作** ] メニューをクリックし、[ **保留中の更新をキャンセル**] をクリックします。
    
      - **更新を承認します。** 選択した更新を組織のデバイスに展開できるようにするには、[ **操作** ] メニューをクリックし、[ **承認**] をクリックします。
    
      - **更新プログラムを復元します。** 以前に承認された更新を組織のデバイスに展開できるようにするには、[ **操作** ] メニューをクリックし、[ **復元**] をクリックします。

</div>

<div>

## <a name="see-also"></a>関連項目


[Lync Server 2013 でのデバイス、電話、クライアント アプリケーションの管理](lync-server-2013-managing-devices-phones-and-client-applications.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

