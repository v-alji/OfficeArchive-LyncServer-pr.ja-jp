---
title: 'Lync Server 2013: エッジ サーバーのインストール'
description: 'Lync Server 2013: エッジサーバーをインストールします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Install Edge Servers
ms:assetid: 1655ab69-3899-4ee4-a1cc-8243bc1bfa0f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398230(v=OCS.15)
ms:contentKeyID: 48183503
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e699a7f41b0ee554bc85fb2d9a72a2d9a42870cb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427209"
---
# <a name="install-edge-servers-for-lync-server-2013"></a>Lync Server 2013 のエッジ サーバーのインストール

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-09-08_

Lync Server 2013 は、Lync Server 展開ウィザードを使って、エッジサーバーにインストールします。 各エッジサーバーで展開ウィザードを実行することで、エッジサーバーのセットアップに必要なほとんどのタスクを実行できます。 エッジサーバーに Lync Server 2013 を展開するには、既にトポロジビルダーを実行して、エッジサーバートポロジを定義および公開し、エッジサーバーから入手できるメディアにエクスポートする必要があります。 詳細については、「 [Lync server 2013 の外部ユーザーアクセスのシナリオ](lync-server-2013-scenarios-for-external-user-access.md) 」および「 [lync server 2013 トポロジをエクスポートして、edge インストール用の外部メディアにコピーする](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md)」を参照してください。

展開ウィザードを使用して各エッジサーバーをインストールし、必要な証明書をインストールして割り当て、必要なサービスを開始するには、「 [Lync server 2013 で外部ユーザーアクセスのサポートを構成](lync-server-2013-configuring-support-for-external-user-access.md) する」の情報を使用して、外部ユーザーのアクセスを有効にして構成すると共に、 [lync server 2013 で](lync-server-2013-verifying-your-edge-deployment.md) の microsoft Edge の展開を確認し

<div>

## <a name="to-install-an-edge-server"></a>エッジサーバーをインストールするには

1.  エッジサーバーをローカルの管理者グループのメンバーまたは同等のユーザー権限とアクセス許可を持つアカウントとしてインストールするコンピューターにログオンします。

2.  トポロジビルダーを使用して作成したトポロジ構成ファイルを、外部メディアにエクスポートしてコピーすることができるようにするには、Edge サーバーで利用できます (たとえば、トポロジ構成ファイルをコピーした USB ドライブへのアクセス、またはファイルをコピーしたネットワーク共有へのアクセスを確認します)。

3.  展開ウィザードを開始します。
    
    <div>
    

    > [!NOTE]  
    > Microsoft Visual C++ 再頒布可能パッケージをインストールする必要があるというメッセージが表示されたら、[ <STRONG>はい</STRONG>] をクリックします。 次のダイアログボックスでは、既定の <STRONG>インストール場所</STRONG> をそのまま使用するか、[ <STRONG>参照</STRONG> ] をクリックして別の場所を選択し、[ <STRONG>インストール</STRONG>] をクリックします。 次のダイアログボックスで、[ <STRONG>使用許諾契約書の条項に同意</STRONG> します] チェックボックスをオンにし、[ <STRONG>OK</STRONG>] をクリックします。

    
    </div>

4.  展開ウィザードで、[ **Lync Server System のインストールまたは更新**] をクリックします。

5.  ウィザードによって、手順1の展開状態が決定された後 **。ローカル構成ストアをインストール** し、[ **実行** ] をクリックして、次の操作を行います。
    
      - [ **全体管理ストアのローカルレプリカの構成** ] ダイアログボックスで、[ **ファイルからのインポート (Edge サーバーに推奨)**] をクリックし、エクスポートされたトポロジ構成ファイルの場所に移動して、.zip ファイルを選択し、[ **開く**] をクリックして、[ **次へ**] をクリックします。
    
      - 展開ウィザードは、構成ファイルから構成情報を読み取り、その XML 構成ファイルをローカルコンピューターに書き込みます。
    
      - [**コマンドの実行**] プロセスが完了した後、[**終了**] をクリックします。

6.  展開ウィザードで、[ **手順 2: Lync サーバーコンポーネントをセットアップまたは削除** する] をクリックして、ローカルコンピューターに保存されている XML 構成ファイルで指定されている lync server 2013 edge コンポーネントをインストールします。

7.  インストールが完了したら、サービスを開始する前に、 [Lync Server 2013 の Edge 証明書のセットアップ](lync-server-2013-set-up-edge-certificates.md) に関する情報を使用して、必要な証明書をインストールして割り当てます。

</div>

</div>

<span> </span>

</div>

</div>

</div>

