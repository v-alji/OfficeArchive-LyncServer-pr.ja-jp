---
title: 'Lync Server 2013: Lync と Skype の接続のプロビジョニング ガイド'
description: 'Lync Server 2013: Lync-Skype 接続のプロビジョニングガイド。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Provisioning guide for Lync-Skype connectivity
ms:assetid: 69adda9b-5b72-4538-9be6-079b2f462e09
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn440173(v=OCS.15)
ms:contentKeyID: 57793363
ms.date: 11/26/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9859a7a621ba4329fe0436fe50a0d9de1d0ae1ef
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436742"
---
# <a name="provisioning-guide-for-lync-skype-connectivity-in-lync-server-2013"></a>Lync Server 2013 での Lync と Skype の接続のプロビジョニング ガイド

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2014-11-26_

Lync Server 2013 は、Skype との接続をサポートしています。 この接続を使用すると、Lync 2013 ユーザーは、Skype ユーザーの Microsoft Account (MSA) を使用して Skype の連絡先を追加できます。 Skype クライアントも、Lync ユーザーを連絡先リストに追加できます。 Lync Server で管理上設定されたポリシーに基づいて、Lync ユーザーと Skype ユーザーは、インスタント メッセージを使用して通信し、お互いのプレゼンスを確認し、音声およびビデオ通話を開始できるようになります。 Lync-Skype 接続は、Lync Online の機能でもあり、Microsoft 365 管理センター内の Lync 管理センターから Lync Online ユーザーに対して有効にすることができます。

<div>

> [!IMPORTANT]  
> Lync Server がパブリック インスタント メッセージング接続 (PIC) を使用して Windows Messenger と接続するように既に構成されている場合、展開は、既に Lync と Skype の接続用に構成されています。検討する対象となりうる唯一の変更は、既存の Messenger PIC エントリの名前を Skype などに変更することだけです。詳細については、このガイドで後述する Lync の「Lync 用の Skype PIC プロバイダー設定を構成する」を参照してください。

</div>

<div>

## <a name="in-this-section"></a>このセクション中

  - [Lync Online ユーザー向けの Lync Server 2013 での Lync-Skype 接続についての注意](lync-server-2013-note-about-lync-skype-connectivity-for-lync-on.md)

  - [Lync Server 2013 から Lync Server パブリック IM 接続プロビジョニング サイトへのアクセス](lync-server-2013-accessing-the-lync-server-public-im-connectivity-provisioning-site.md)

  - [Lync Server 2013 での Lync と Skype の接続の有効化](lync-server-2013-enabling-lync-skype-connectivity.md)

  - [エンド ユーザーとしての Lync Server 2013 での Lync と Skype の接続の使用](lync-server-2013-using-lync-skype-connectivity-as-an-end-user.md)

  - [FAQ: Skype 接続用の Lync Server 2013 のプロビジョニング](lync-server-2013-frequently-asked-questions-provisioning-lync-server-for-skype-connectivity.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

