---
title: XMPP 構成の例  - Google Talk との XMPP フェデレーション
description: XMPP の構成の例– Google Talk との XMPP フェデレーション。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
manager: serdars
audience: admin
f1.keywords:
- NOCSH
TOCTitle: Example XMPP configuration – XMPP federation with Google Talk
ms:assetid: 360a2f7b-015b-4e93-ac67-0f609c21f1a2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204807(v=OCS.15)
ms:contentKeyID: 48183848
ms.date: 07/23/2014
mtps_version: v=OCS.15
ms.openlocfilehash: e6ea920fad0344e784aac104ab5528d89b90f47b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428452"
---
# <a name="example-xmpp-configuration-in-lync-server-2013--xmpp-federation-with-google-talk"></a>Lync Server 2013 での XMPP 構成の例  - Google Talk との XMPP フェデレーション

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2014-04-22_

XMPP プロキシを展開するための構成例では、Google Talk とのフェデレーションを定義しています。

<div>

## <a name="example-xmpp-configuration--xmpp-federation-with-google-talk"></a>XMPP 構成の例  - Google Talk との XMPP フェデレーション

1.  フロントエンドサーバーで、Lync Server 展開ウィザードを開きます。 [ **Lync Server System** の **インストール** または更新] をクリックし、[ **lync server コンポーネント** の **セットアップ** または削除] をクリックします。 [ **実行] をもう一度** クリックします。

2.  **Lync Server コンポーネントのセットアップ** で、[**次へ**] をクリックします。 概要画面には、実行中の操作が表示されます。 展開が完了したら、[ **ログの表示** ] をクリックして、利用可能なログファイルを表示します。 [ **完了** ] をクリックして展開を完了します。

3.  エッジサーバーで、Lync Server 展開ウィザードを開きます。 [ **Lync Server System** の **インストール** または更新] をクリックし、[ **lync server コンポーネント** の **セットアップ** または削除] をクリックします。 [ **実行] をもう一度** クリックします。

4.  Google の会話を XMPP で許可されているパートナーとして追加します。 Google Talk では、現時点では、サーバー間の XMPP フェデレーション向けの暗号化されていない TCP 接続のみをサポートしており、身元確認のためのサーバーコールバックのみをサポートしています。 ( <http://xmpp.org/extensions/xep-0220.html> を参照)。
    
        New-CsXmppAllowedPartner gmail.com -TlsNegotiation NotSupported -SaslNegotiation NotSupported -EnableKeepAlive $false -SupportDialbackNegotiation $true

5.  エッジフェデレーションを有効にするには、次のように入力します。
    
        Set-CsAccessEdgeConfiguration -AllowFederatedUsers $true

6.  **Lync Server コンポーネントのセットアップ** で、[**次へ**] をクリックします。 概要画面には、実行中の操作が表示されます。 展開が完了したら、[ **ログの表示** ] をクリックして、利用可能なログファイルを表示します。 [ **完了** ] をクリックして展開を完了します。

7.  エッジサーバーの Lync Server 展開ウィザードで、[ **手順 3: 証明書の要求、インストール、または割り当て**] の横にある [実行] を **もう一度** クリックします。
    
    <div>
    

    > [!TIP]
    > 初めてエッジサーバーを展開する場合は、[実行] ではなく、[実行] と表示されます。

    
    </div>

8.  [**利用可能な証明書タスク**] ページで、[**新しい証明書要求を作成する**] をクリックします。

9.  [ **証明書の要求** ] ページで、[ **外部境界の証明書**] をクリックします。

10. [ **遅延または即時要求** ] ページで、[ **今すぐ要求を準備するが、後で送信** する] チェックボックスをオンにします。

11. [ **証明書要求ファイル** ] ページで、要求を保存するファイルの完全パスとファイル名を入力します (たとえば、c: \\ cert \_ 外部 \_ edge)。

12. [ **代替証明書テンプレートの指定** ] ページで、既定の web サーバテンプレート以外のテンプレートを使用するには、[ **選択された証明機関に別の証明書テンプレートを使用** する] チェックボックスをオンにします。

13. [ **名前とセキュリティの設定** ] ページで、次の操作を行います。
    
    1.  [ **フレンドリ名**] に、証明書の表示名を入力します。
    
    2.  **ビット長** では、ビット長 (通常は **2048** の既定値) を指定します。
    
    3.  [ **証明書の秘密キーをエクスポート可能としてマーク** する] チェックボックスがオンになっていることを確認する

14. [ **組織の情報** ] ページで、組織の名前と組織単位 (たとえば、部門や部署) を入力します。

15. [ **地理情報** ] ページで、場所情報を指定します。

16. [ **Subject Name/Subject name** ] ページには、ウィザードによって自動的に入力される情報が表示されます。 追加の件名の代替名が必要な場合は、次の2つの手順で指定します。

17. [ **サブジェクト代替名 (san)] ページの Sip ドメイン設定** で、[Domain] チェックボックスをオンにして sip を追加します。 \<sipdomain\> [サブジェクトの別名] リストに入力します。

18. [ **追加のサブジェクト代替名の構成** ] ページで、必要なその他のサブジェクトの代替名を指定します。
    
    <div>
    

    > [!TIP]
    > XMPP プロキシがインストールされている場合、既定では、ドメイン名 (contoso.com など) が SAN エントリに設定されます。 他のエントリが必要な場合は、この手順で追加します。

    
    </div>

19. [ **要求の概要** ] ページで、要求の生成に使用する証明書情報を確認します。

20. コマンドの実行が完了したら、 **ログを表示** するか、[ **次へ** ] をクリックして続行します。

21. [**証明書要求ファイル**] ページで、[**完了**] をクリックして、証明書ウィザードの [**表示**] または [終了] をクリックし、生成された証明書署名要求 (CSR) ファイルを表示できます。

22. 要求ファイルをコピーして、公開証明機関に提出します。

23. 公開証明書の受信、インポート、割り当てが完了したら、Edge Server サービスを停止して再起動する必要があります。 Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。 Lync Server 管理シェルで、次のように入力します。
    ```
        Stop-CsWindowsService
    ```
    
    ```
        Start-CsWindowsService
    ```
    
24. XMPP フェデレーション用の DNS を構成するには、次の SRV レコードを外部 DNS に追加します。 \_ xmpp-サーバー。 \_tcp.\<domain name\> SRV レコードは、エッジサーバーのアクセスエッジ FQDN に解決され、ポート値は5269になります。

25. フロントエンドサーバーで Lync Server 管理シェルを開き、次のように入力して、すべてのユーザーを有効にするように新しい外部アクセスポリシーを構成します。
    
        New-CsExternalAccessPolicy -Identity FedPic -EnableFederationAccess $true -EnablePublicCloudAccess $true
        Get-CsUser | Grant-CsExternalAccessPolicy -PolicyName FedPic

</div>

</div>

<span> </span>

</div>

</div>

</div>

