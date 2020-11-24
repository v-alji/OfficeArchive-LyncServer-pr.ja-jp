---
title: パイロット プール展開の DNS レコードの構成
description: パイロットプール展開用の DNS レコードを構成します。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Configure DNS records for pilot pool deployment
ms:assetid: eb421bad-4bf1-4837-a077-7795094692d9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721921(v=OCS.15)
ms:contentKeyID: 49733855
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1e41e163432ba910f6d083cc508e8ad8c9f2006d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398871"
---
# <a name="configure-dns-records-for-pilot-pool-deployment"></a>パイロット プール展開の DNS レコードの構成

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-09-29_

Lync Server 2013 パイロットプールを展開する前に、パイロットプールの DNS ホストのエントリを更新する必要があります。 この手順を完了するには、サーバーまたはドメインに、Domain Admins グループのメンバーまたは DnsAdmins グループのメンバーとしてログオンしている必要があります。

**DNS ホスト A レコードを構成するには**

1.  ドメインネームシステム (DNS) サーバーで、[ **スタート**] をクリックし、[ **管理ツール**]、[ **DNS**] の順にクリックします。

2.  ドメインのコンソールツリーで [ **前方参照ゾーン**] を展開し、Lync Server 2013 がインストールされているドメインを右クリックします。

3.  [ **新しいホスト (A または AAAA)**] をクリックします。

4.  [ **名前**] をクリックして、Lync Server 2013 プールのホスト名を入力します (ドメイン名は、レコードが定義されていて、A レコードの一部として入力する必要はありません)。

5.  [ **Ip アドレス**] をクリックして、フロントエンドプールの ip アドレスを入力します。

6.  [ **ホストの追加**] をクリックし、[ **OK**] をクリックします。

7.  完了したら、[ **完了**] をクリックします。

</div>

<span> </span>

</div>

</div>

</div>

