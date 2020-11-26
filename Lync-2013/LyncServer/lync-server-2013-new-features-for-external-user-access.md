---
title: 'Lync Server 2013: 外部ユーザー アクセスの新機能'
description: 'Lync Server 2013: 外部ユーザーアクセスの新機能。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New features for external user access
ms:assetid: 99da6bd5-ec14-4ad9-8f7d-37fbddf567dd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398794(v=OCS.15)
ms:contentKeyID: 48184884
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d9d960a469334a836c453e8ae3bbf51f1b66bb93
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445401"
---
# <a name="new-features-for-external-user-access-in-lync-server-2013"></a>Lync Server 2013 の外部ユーザー アクセスの新機能

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-10-17_

Lync Server 2013 には、ユーザーの機能と通信方法を拡張する新機能が導入されています。 また、Lync Server 2013 では、組織で利用できるサービスをより適切に統合および拡張するために、既存のサービスへの変更が導入されています。 以下は、Lync Server 2013 Edge Server サービスの計画と展開に影響を与える可能性のある変更内容をまとめたものです。

  - **IPv6 アドレス指定のサポート**   Lync Server 2013 は、すべての Edge Server サービスの IPv6 アドレス指定をサポートしています。 Windows Server の構成を通じてインターフェイスの IPv6 アドレスを指定している場合は、トポロジビルダーの IP アドレス構成を使用して、エッジサーバー構成の IPv6 アドレスを使うことができます。
    
    <div>
    

    > [!IMPORTANT]  
    > Lync Server 2013 での IPv6 アドレスの使用は、組織が展開するルーターやファイアウォールでの IPv6 のサポート、およびインターネットサービスプロバイダーによるサポートによって異なります。

    
    </div>

  - **拡張可能なメッセージングとプレゼンスプロトコル (XMPP)**   Lync Server 2013 は、完全に統合された XMPP プロキシ (エッジサーバーに展開) と、フロントエンドサーバーに XMPP ゲートウェイを展開したものです。 XMPP フェデレーションは、オプションのコンポーネントとして展開できます。 XMPP プロキシと XMPP ゲートウェイを追加して構成することにより、Microsoft Lync 2013 ユーザーは、インスタントメッセージング (IM) とプレゼンスのために、XMPP ベースのパートナーから連絡先を追加できます。
    
    <div>
    

    > [!NOTE]  
    > 現時点では、Lync Server 2013 の XMPP サービスは、Lync クライアントと XMPP ベースの連絡先の間でインスタントメッセージ (im) とプレゼンスを提供します。

    
    </div>

  - **モバイルクライアント用のモバイルサービス**   Lync Server 2010 のモバイルサービスで導入された lync Server 2013 のモバイルサービスでは、サポートされている Apple iOS、Android、Windows Phone、または Nokia モバイルデバイスを使用して、Microsoft Lync モバイルクライアントが、インスタントメッセージの送受信、連絡先の表示、プレゼンスの表示などの操作を実行できます。 さらに、モバイルデバイスでは、クリックして会議に参加したり、勤務先の電話、1回の通話、ボイスメール、不在着信通知など、一部のエンタープライズ音声機能をサポートしたりします。
    
    <div>
    

    > [!NOTE]  
    > モビリティサービスは、フロントエンドサーバーに展開されているリバースプロキシと公開されたサービスを使用します。 エッジサーバーへの変更は必要ありません。

    
    </div>

  - **ディレクターはオプションの役割**   Lync Server 2013 トポロジでのディレクターサーバーの役割が変更されていません。 さらに、web サービスのホスト、着信ユーザー要求の事前認証、外部ユーザーのホームプールへの送信を行うことができます。 推奨された役割からのディレクターをオプションの役割に変更しても、ディレクターの値を減らすことはできませんが、機能が損なわれることなく、サーバー数やその他のハードウェア要件 (ディレクターのハードウェアロードバランサーなど) が必要になります。 フロントエンドサーバーは、提供されたサービスに影響を与えずにディレクターと同じジョブを行うことができるため、必要に応じて、[ディレクター] を展開することもできます。 フロントエンドサーバーによって同じサービスが提供されるという確信を持って、ディレクターを安全に除外することができます。

<div>

## <a name="see-also"></a>関連項目


[Lync Server 2013 での IPv6 の計画と構成](lync-server-2013-planning-for-and-configuring-ipv6.md)  


[Lync Server 2013 の外部ユーザー アクセスの計画](lync-server-2013-planning-for-external-user-access.md)  
[Lync Server 2013 での拡張メッセージングとプレゼンスプロトコル (XMPP) フェデレーションの計画](lync-server-2013-planning-for-extensible-messaging-and-presence-protocol-xmpp-federation.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

