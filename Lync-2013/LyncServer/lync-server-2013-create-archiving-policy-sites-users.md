---
title: 'Lync Server 2013: 特定のサイトまたはユーザーに対して、内部または外部の通信のアーカイブを有効または無効にするアーカイブポリシーを作成する'
description: 'Lync Server 2013: 特定のサイトまたはユーザーに対して、内部または外部の通信のアーカイブを有効または無効にするアーカイブポリシーを作成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Creating an Archiving policy to enable or disable Archiving of internal or external communications for specific sites or users
ms:assetid: 5864793a-ba72-470c-bb5b-9fb41e968896
ms:mtpsurl: https://technet.microsoft.com/library/Gg398385(v=OCS.15)
ms:contentKeyID: 48184193
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a23f952229df9fe950f2666914263a7cf46595f4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431989"
---
# <a name="creating-an-archiving-policy-in-lync-server-2013-to-enable-or-disable-archiving-of-internal-or-external-communications-for-specific-sites-or-users"></a>Lync Server 2013 でアーカイブポリシーを作成して、特定のサイトまたはユーザーの内部または外部の通信のアーカイブを有効または無効にする

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**トピックの最終更新日:** 2013-02-23_

Lync Server 2013 では、ポリシーを使って、内部通信のアーカイブを有効または無効にしたり、Lync Server 2013 を使用しているユーザーの外部通信を有効にしたりすることができます。 これには、次のアーカイブポリシーが含まれます。

  - Lync Server 2013 を展開するときに既定で作成されるグローバルポリシー。

  - 特定のサイトまたはユーザーに対するアーカイブの実装方法を指定するために作成および使用できる、オプションのサイトレベルとユーザーレベルのポリシー。

アーカイブの展開時にアーカイブポリシーを最初に設定しましたが、展開後にポリシーの変更、追加、削除を行うことができます。 Lync Server 2013 コントロールパネルで、[**アーカイブと監視**] グループの [**アーカイブポリシー** ] ページを使用して、グローバルレベル、サイトレベル、ユーザーレベルでポリシーを管理できます。 Lync Server ストレージと Exchange 2013 ストレージを統合すると、Exchange ユーザーポリシーは Lync Server 2013 アーカイブポリシーよりも優先されます。

ポリシーの実装方法 (ポリシーの階層を含む) について詳しくは、「計画ドキュメント、展開ドキュメント、または運用ドキュメント」の「 [Lync Server 2013 でのアーカイブの動作](lync-server-2013-how-archiving-works.md) 」をご覧ください。

<div>


> [!NOTE]
> アーカイブの実装を制御するには、IM または会議のアーカイブ、重要モードの使用、削除オプションなど、アーカイブ構成のオプションを指定する必要があります。 既定では、グローバルアーカイブ構成またはサイトまたはプールのアーカイブ構成では、どのオプションも有効になっていません。 アーカイブポリシーで、内部または外部通信のアーカイブを有効にする前に、アーカイブ構成ですべての適切なオプションを指定する必要があります。 詳細については、「 <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">Lync Server 2013 でアーカイブ構成オプションを管理</A> する」を参照してください。この操作のドキュメントでは、組織、サイト、プールについて説明します。<BR>展開に対して Microsoft Exchange の統合を有効にしている場合は、exchange 2013 を使用しているユーザーに対してアーカイブが有効になっているかどうかが Exchange ポリシーによって制御され、メールボックス In-Place 保留になります。 詳細については、展開ドキュメントで <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Exchange Server との統合を使用する場合の「Lync server 2013 でアーカイブするためのポリシーを設定する</A> 」を参照してください。



</div>

<div>

## <a name="to-create-an-archiving-policy-for-a-site-or-users"></a>サイトまたはユーザーのアーカイブポリシーを作成するには

1.  CsArchivingAdministrator または CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。

2.  ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。 Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。

3.  左側のナビゲーション バーで、[**監視とアーカイブ**] をクリックし、[**アーカイブ ポリシー**] をクリックします。

4.  [**新規**] をクリックし、次のいずれかの操作を実行します。
    
      - サイトレベルのアーカイブポリシーを作成するには、[ **サイトポリシー** ] をクリックし、[ **サイトの選択**] でポリシーを適用するサイトをクリックします。
    
      - ユーザーレベルのアーカイブ ポリシーを作成するには、[**ユーザー ポリシー**] をクリックします。

5.  [**新しいアーカイブ ポリシー**] で、次の操作を実行します。
    
      - [**名前**] で、新しいポリシーの名前を指定します (externalContoso など)。
    
      - [**説明**] に、そのポリシーの内容に関する詳細を入力します (「Contoso の外部ユーザー アーカイブ ポリシー」など)。
    
      - 内部ユーザーとの通信のアーカイブを制御するには、[**内部通信をアーカイブする**] チェック ボックスをオンまたはオフにします。
    
      - 外部ユーザーとの通信のアーカイブを制御するには、[**外部通信をアーカイブする**] チェック ボックスをオンまたはオフにします。

6.  [**確定**] をクリックします。
    
    <div>
    

    > [!IMPORTANT]
    > ユーザー ポリシーの設定は、そのポリシーを適用する特定のユーザーおよびユーザー グループにのみ適用されます。 詳細については、「 <A href="lync-server-2013-applying-an-archiving-policy-to-users.md">Lync Server 2013 のユーザーにアーカイブポリシーを適用する</A>」を参照してください。

    
    </div>

</div>

<div>

## <a name="creating-an-archiving-policy-by-using-windows-powershell-cmdlets"></a>Windows PowerShell コマンドレットを使用してアーカイブポリシーを作成する

アーカイブポリシーを作成するには、Windows PowerShell と **CsArchivingPolicy** コマンドレットを使用します。 このコマンドレットは、Lync Server 2013 管理シェルまたは Windows PowerShell のリモート セッションから実行できます。 リモートの Windows PowerShell を使用して Lync Server に接続する方法について詳しくは、Lync Server Windows PowerShell のブログ記事「Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell (クイックスタート: リモート PowerShell を使用した Microsoft Lync Server 2010 の管理)」を[https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876)で参照してください。

<div>

## <a name="to-create-a-new-archiving-policy-at-the-site-scope"></a>サイトの範囲に新しいアーカイブポリシーを作成するには

  - 次のコマンドは、Redmond サイトの新しいアーカイブ ポリシーを作成します。
    
        New-CsArchivingPolicy -Identity "site:Redmond"

</div>

<div>

## <a name="to-create-a-new-archiving-policy-at-the-per-user-scope"></a>ユーザーごとのスコープで新しいアーカイブポリシーを作成するには

  - ユーザーごとのスコープで新しいアーカイブポリシーを作成するには、ポリシーを作成するときに一意の Id を指定するだけです。
    
        New-CsArchivingPolicy -Identity "RedmondArchivingPolicy"

</div>

<div>

## <a name="to-create-a-new-archiving-policy-that-enables-archiving-of-internal-communication-sessions"></a>内部通信セッションのアーカイブを有効にする新しいアーカイブ ポリシーを作成するには

  - 前の各コマンドでは (必須の ID パラメーター以外に) パラメーターが指定されていないため、新しいポリシーではすべてのプロパティで既定値が使用されます。 別のプロパティ値を使用するポリシーを作成するには、該当するパラメーターとパラメーター値を含めます。 たとえば、内部のインスタントメッセージングセッションのアーカイブを許可するアーカイブポリシーを作成するには、次のようなコマンドを使用します。
    
        New-CsArchivingPolicy -Identity "site:Redmond" -ArchiveInternal $True

</div>

<div>

## <a name="to-create-a-new-archiving-policy-that-enables-archiving-of-both-internal-and-external-communication-sessions"></a>内部と外部の両通信セッションのアーカイブを有効にする新しいアーカイブ ポリシーを作成するには

  - 複数のパラメーターを含めることで、複数のプロパティ値を変更できます。 たとえば、次のコマンドは、内部と外部のインスタントメッセージングセッションの両方をアーカイブするための新しいポリシーを構成します。
    
        New-CsArchivingPolicy -Identity "site:Redmond" -ArchiveInternal $True -ArchiveExternal $True

</div>

詳細については、 [CsArchivingPolicy](https://technet.microsoft.com/library/Gg399032(v=OCS.15)) コマンドレットのヘルプトピックを参照してください。

</div>

<div>

## <a name="see-also"></a>関連項目


[Lync Server 2013 での内部および外部通信のアーカイブの管理](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

