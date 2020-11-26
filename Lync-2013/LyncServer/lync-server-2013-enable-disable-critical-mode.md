---
title: 'Lync Server 2013: アーカイブに失敗した場合に、IM および web 会議セッションをブロックまたは許可するために、クリティカルモードを有効または無効にする'
description: 'Lync Server 2013: アーカイブに失敗した場合に、IM および web 会議セッションをブロックまたは許可するために、クリティカルモードを有効または無効にします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enabling or disabling critical mode to block or allow IM and web conferencing sessions if Archiving fails
ms:assetid: fafdcd2e-b778-4ed5-a25f-09208aa3b699
ms:mtpsurl: https://technet.microsoft.com/library/Gg182609(v=OCS.15)
ms:contentKeyID: 48185927
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ac318a04d8ed3b952e45bf5b8718a78432391d29
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437589"
---
# <a name="enabling-or-disabling-critical-mode-in-lync-server-2013-to-block-or-allow-im-and-web-conferencing-sessions-if-archiving-fails"></a>アーカイブに失敗した場合に IM および web 会議セッションをブロックまたは許可するための、Lync Server 2013 でのクリティカルモードの有効化または無効化

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**トピックの最終更新日:** 2013-02-23_

Lync Server 2013 コントロールパネルで、[アーカイブ構成] を使って、重要なモードを有効または無効にします。 これには、次のアーカイブ構成が含まれます。

  - Lync Server 2013 を展開するときに既定で作成されるグローバル構成。

  - 作成および使用して、特定のサイトまたはプールに対するアーカイブの実装方法を指定することができる、オプションのサイトレベルとプールレベルの構成。

アーカイブの展開時にアーカイブ構成を最初に設定しましたが、展開後に構成の変更、追加、削除を行うことができます。 アーカイブ構成の実装方法について詳しくは、「指定できるオプションやアーカイブ構成の階層」をご覧ください。「計画ドキュメント、展開ドキュメント、または操作のドキュメントでの [Lync Server 2013 でのアーカイブの動作](lync-server-2013-how-archiving-works.md) 」を参照してください。

<div>


> [!NOTE]  
> アーカイブを使用するには、内部通信のアーカイブを有効にするか、外部通信を有効にするか、または Lync Server 2013 を使用しているユーザーに対してアーカイブを有効にするかを指定するようにアーカイブポリシーを構成する必要があります。 既定では、内部または外部の通信でアーカイブは有効になっていません。 すべてのポリシーでアーカイブを有効にする前に、このセクションで説明するように、展開用に適切なアーカイブ構成を指定し、必要に応じて特定のサイトとプールを指定する必要があります。 アーカイブを有効にする方法の詳細については、展開ドキュメントの「 <A href="lync-server-2013-configuring-and-assigning-archiving-policies.md">Lync Server 2013 でアーカイブポリシーを構成して割り当てる</A> 」を参照してください。<BR>Exchange Server の統合機能を使用して exchange 2013 サーバー上のアーカイブデータとファイルを保存し、すべてのユーザーが Exchange 2013 サーバー上にある場合は、アーカイブを展開した後で、SQL Server データベースの構成をトポロジから削除する必要があります。 この操作を行うには、トポロジビルダーを使用する必要があります。 詳細については、「運用ドキュメントの「 <A href="lync-server-2013-changing-archiving-database-options.md">Lync Server 2013 でアーカイブデータベースのオプションを変更する</A> 」を参照してください。



</div>

<div>

## <a name="to-enable-or-disable-blocking-of-im-and-web-conferencing-sessions-if-archiving-fails"></a>アーカイブに失敗した場合に、IM および web 会議セッションのブロックを有効または無効にするには

1.  CsArchivingAdministrator または CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。

2.  ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。 Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。

3.  左側のナビゲーション バーで、[**監視とアーカイブ**] をクリックし、[**アーカイブ構成**] をクリックします。

4.  アーカイブ構成の一覧から、適切なグローバル構成、サイト構成、またはプール構成の名前をクリックし、[**編集**]、[**詳細の表示**] の順にクリックし、次の操作を実行します。

5.  障害が発生したときのアーカイブの動作を設定するには、[**アーカイブ失敗時はインスタント メッセージング (IM) または Web 会議セッションを禁止する**] チェック ボックスをオンまたはオフにします。

6.  [**確定**] をクリックします。

</div>

<div>

## <a name="enabling-and-disabling-critical-mode-by-using-windows-powershell-cmdlets"></a>Windows PowerShell コマンドレットを使用して重要モードを有効または無効にする

**CsArchivingConfiguration** コマンドレットを使用して、重要なモードを有効または無効にすることができます。 このコマンドレットは、Lync Server 2013 管理シェルから、または Windows PowerShell のリモートセッションから実行できます。 リモートの Windows PowerShell を使用して Lync Server に接続する方法について詳しくは、Lync Server Windows PowerShell のブログ記事「Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell (クイックスタート: リモート PowerShell を使用した Microsoft Lync Server 2010 の管理)」を[https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876)で参照してください。

<div>

## <a name="to-enable-critical-mode"></a>クリティカルモードを有効にするには

  - クリティカルモードを有効にするには、Blockonアーカイブエラープロパティの値を True ($True) に設定します。 次に例を示します。
    
        Set-CsArchivingConfiguration -Identity "site:Redmond" -BlockOnArchiveFailure $True

</div>

<div>

## <a name="to-disable-critical-mode"></a>重要モードを無効にするには

  - 重要モードを無効にするには、Blockonアーカイブエラープロパティの値を False ($False) に設定します。 次に例を示します。
    
        Set-CsArchivingConfiguration -Identity "site:Redmond" -BlockOnArchiveFailure $False

</div>

詳細については、 [CsArchivingConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsArchivingConfiguration) コマンドレットのヘルプトピックを参照してください。

</div>

<div>

## <a name="see-also"></a>関連項目


[Lync Server 2013 でアーカイブデータベースのオプションを変更する](lync-server-2013-changing-archiving-database-options.md)  


[Lync Server 2013 でのアーカイブのしくみ](lync-server-2013-how-archiving-works.md)  


[組織、サイト、およびプールの Lync Server 2013 でアーカイブ構成オプションを管理する](lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

