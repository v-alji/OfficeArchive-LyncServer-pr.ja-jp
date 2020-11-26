---
title: Lync Server 2013 の Active Directory のサポート
description: Lync Server 2013 Active Directory のサポート。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Active Directory support
ms:assetid: 28ed9ac4-586d-4803-ad45-99c4fa793f54
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425756(v=OCS.15)
ms:contentKeyID: 48183679
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 349862b2f541ef3033c9a725a6ff04c6a4e219f7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439409"
---
# <a name="active-directory-support-in-lync-server-2013"></a>Lync Server 2013 での Active Directory のサポート

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-12-04_

Lync Server 2013 でサポートされている Active Directory ドメインサービスオンプレミストポロジは、次のようになります。

  - 単一のドメインを含む単一のフォレスト

  - 単一のツリーと複数のドメインを含む単一のフォレスト

  - 複数のツリーと不整合の名前空間を含む単一のフォレスト

  - 中央フォレスト トポロジの複数のフォレスト

  - リソース フォレスト トポロジの複数のフォレスト

<div>


> [!NOTE]  
> Lync Server 2013 では、単一ラベルドメインはサポートされていません。 たとえば、 <STRONG>local</STRONG> という名前のルートドメインを持つフォレストはサポートされていますが、 <STRONG>local</STRONG> という名前の単一ラベルルートドメインはサポートされていません。 詳細については、「Microsoft サポート技術情報の記事300684」を参照してください。 "単一ラベルの DNS 名でドメイン用に Windows を構成する" について説明し <A href="https://go.microsoft.com/fwlink/p/?linkid=143752">https://go.microsoft.com/fwlink/p/?linkId=143752</A> ます。



</div>

<div>


> [!NOTE]  
> Lync Server 2013 では、ドメイン名の変更はサポートされていません。 Lync Server が展開されているドメインの名前を変更する必要がある場合は、まず Lync Server をアンインストールしてから、ドメインの名前を変更してから、Lync Server を再インストールする必要があります。



</div>

オンプレミス展開のサポートされるトポロジと要件の詳細については、計画ドキュメントの「 [Lync Server 2013 での Active Directory ドメインサービスの要件、サポート、およびトポロジ](lync-server-2013-active-directory-domain-services-requirements-support-and-topologies.md) 」を参照してください。

</div>

<span> </span>

</div>

</div>

</div>

