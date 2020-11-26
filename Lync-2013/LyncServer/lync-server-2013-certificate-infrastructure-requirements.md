---
title: Lync Server 2013 の証明書インフラストラクチャの要件
description: Lync Server 2013 証明書インフラストラクチャの要件。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate infrastructure requirements
ms:assetid: 0051aa23-0bbe-4e72-9f29-e01c6bcc6190
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398066(v=OCS.15)
ms:contentKeyID: 48183219
ms.date: 06/23/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 02c7e69f272c29f0ba9386f403db326b4d39bbff
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435412"
---
# <a name="certificate-infrastructure-requirements-for-lync-server-2013"></a>Lync Server 2013 の証明書インフラストラクチャの要件

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2016-06-23_

Lync Server 2013 では、TLS と相互 TLS (MTLS) 接続をサポートするために公開キー基盤 (PKI) が必要です。

Lync Server では、次の目的で証明書が使用されます。

  - クライアントとサーバーの間の TLS 接続

  - サーバー間の MTLS 接続

  - パートナーの自動 DNS 検出を使ったフェデレーション

  - インスタント メッセージング (IM) 用のリモート ユーザー アクセス

  - オーディオ/ビデオ (A/V) セッション、アプリケーション共有、および会議への外部ユーザーアクセス

  - Web サービスの自動検出を使用したモバイル要求

Lync Server の場合は、次の一般的な要件が適用されます。

  - すべてのサーバー証明書がサーバーの承認 (サーバー EKU) をサポートしている必要がある。

  - すべてのサーバー証明書に CRL 配布ポイント (CDP) を含める必要がある。

  - すべての証明書が、オペレーティング システムでサポートされている署名アルゴリズムによって署名されている必要がある。 Lync Server 2013 は、ダイジェストのサイズ (224、256、384、512ビット) の SHA-1 および SHA-1 スイートをサポートしており、オペレーティングシステムの要件を満たしているか、超えています。 オペレーティングシステムのサポートについては、を参照してください [https://go.microsoft.com/fwlink/?LinkId=287002](https://go.microsoft.com/fwlink/?linkid=287002) 。
    
    <div>
    

    > [!NOTE]  
    > RSASSA-PSS 署名アルゴリズムの使用はサポートされておらず、数ある問題の中でも、ログイン時のエラーや着信転送時の問題につながる可能性があります。

    
    </div>

  - 自動登録は、Lync Server を実行している内部サーバーでサポートされています。

  - 自動登録は、Lync Server Edge サーバーではサポートされていません。

  - Web ベースの証明書要求を Windows Server 2003 CA に送信する場合は、Windows Server 2003 と SP2 または Windows XP を実行しているコンピューターから送信する必要があります。
    
    KB922706 では、Windows Server 2003 証明書サービスの web 登録に対して web 証明書を登録する際の問題を解決するためのサポートを提供していますが、windows server 2008、Windows Vista、または Windows 7 を使用して Windows Server 2003 CA から証明書を要求することはできません。

  - 暗証キーの長さとして 1024、2048、4096 がサポートされます。 2048 以上のキーの長さはお勧めしません。

  - 既定のダイジェストまたはハッシュ アルゴリズムは RSA です。 ECDH \_ P256、ecdh \_ P384、および ecdh \_ P521 アルゴリズムもサポートされています。 

<div>

## <a name="in-this-section"></a>このセクション中

  - [Lync Server 2013 の内部サーバーに対する証明書要件](lync-server-2013-certificate-requirements-for-internal-servers.md)

  - [Lync Server 2013 における外部ユーザー アクセスに対する証明書要件](lync-server-2013-certificate-requirements-for-external-user-access.md)

  - [Lync Server 2013 の常設チャット サーバーに対する証明書要件](lync-server-2013-certificate-requirements-for-persistent-chat-server.md)

  - [Lync Server 2013 のモビリティの証明書の要件](lync-server-2013-certificate-requirements-for-mobility.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

