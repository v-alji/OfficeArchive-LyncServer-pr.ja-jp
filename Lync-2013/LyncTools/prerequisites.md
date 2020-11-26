---
title: 前提条件
description: 受講.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Prerequisites
ms:assetid: 48016bea-be3b-4ba5-8df8-d8ad4d9243d9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945592(v=OCS.15)
ms:contentKeyID: 51541417
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 936e52961539ed57fe1b610d42fb1c9cf35589b0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446412"
---
# <a name="prerequisites"></a>前提条件

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2013-02-19_

Lync Server 2013 のストレスとパフォーマンスのツールを実行するためには、さまざまなハードウェア、ソフトウェア、システム構成の要件があります。

<div>

## <a name="client-hardware-requirements"></a>クライアントハードウェア要件

Lync server 2013 の展開で Lync Server 2013 ストレスおよびパフォーマンスツールを実行するには、ロードをシミュレートするすべての4500ユーザーに対して、次の最小ハードウェア要件を満たす少なくとも1つの専用コンピューターが必要です。

  - 1 ギガビットのネットワーク アダプター

  - 8 GB ram

  - 2デュアルコアセントラルプロセッシングユニット (Cpu)

</div>

<div>

## <a name="client-software-requirements"></a>クライアントソフトウェア要件

Lync server 2013 のストレスとパフォーマンスツールを Lync Server 2013 の展開で実行するために、サポートされているオペレーティングシステムは次のとおりです。

  - Windows Server 2012 オペレーティングシステム

  - Windows Server 2008 オペレーティングシステム (64 ビット版)

クライアントコンピューターは、次のソフトウェア要件を満たしている必要があります。

  - [Microsoft .Net Framework 4.5](https://go.microsoft.com/fwlink/?linkid=143212)ランタイムがインストールされている必要があります。

  - Windows Server 2008/Windows Server 2012 では、デスクトップエクスペリエンス機能を有効にする必要があります。

  - [Microsoft Visual C++ 2012 再頒布可能パッケージ](https://go.microsoft.com/fwlink/?linkid=143216)(x64) がインストールされている必要があります。

  - 完全に構成された Lync Server 2013 の展開。

<div>


> [!IMPORTANT]  
> Microsoft ユニファイドコミュニケーションマネージ API (UCMA) 4.0 ライブラリはインストールパッケージに含まれているため、UCMA は不要であり、クライアントコンピューターにインストールされていない必要があります。



</div>

</div>

<div>

## <a name="configuration-requirements"></a>構成要件

Lync Server 2013 のストレスとパフォーマンスツールを実行するコンピューターは、次の要件に従って構成する必要があります。

1.  ドメインまたはローカル管理者グループのメンバーとしてログオンしている必要があります。

2.  Lync server 2013 のストレスとパフォーマンスツール (LyncPerfTool.exe) は、Lync Server 2013 コンポーネントも実行しているコンピューターでは実行できません。

3.  フロントエンドサーバーまたはユーザーアカウントが保存されている Standard Edition サーバーで Lync Server 2013 ユーザー作成ツール (UserProvisioningTool.exe) を実行する必要があります。 ツールが複数回実行される場合、Microsoft ユニファイドコミュニケーションを有効にしている各ユーザーは、一意の電話番号を持っている必要があります。

4.  ページファイルのサイズは、システムで管理されているか、システムの RAM の量の1.5 倍以上である必要があります。

</div>

</div>

<span> </span>

</div>

</div>

</div>

