---
title: 'Lync Server 2013: 集中化されたログサービスのプロバイダーの構成'
description: 'Lync Server 2013: 一元ログサービスのプロバイダーを構成する。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring providers for Centralized Logging Service
ms:assetid: 6a197ecf-b56b-45e0-8e7c-f532ec5164ff
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688082(v=OCS.15)
ms:contentKeyID: 49733678
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9146865b3856f7956c6ae393ef38614b0fea168e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432717"
---
# <a name="configuring-providers-for-centralized-logging-service-in-lync-server-2013"></a>Lync Server 2013 での中央集中ログサービスのプロバイダーの構成

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2014-03-19_

一元管理サービスの *プロバイダー* の概念と構成は、理解するうえで最も重要なものの1つです。 *プロバイダー* は、lync server のトレースモデルの lync server server ロールコンポーネントに直接マッピングされます。 プロバイダーは、トレース対象の Lync Server 2013 のコンポーネント、収集するメッセージの種類 (fatal、エラー、警告など)、フラグ (TF Connection、TF Diag など) を定義し \_ ます。これは、 \_ プロバイダーは、各 Lync Server サーバーの役割で追跡可能なコンポーネントです。 プロバイダーを使用して、コンポーネントに対するトレースのレベルと種類 (S4、SIPStack、IM、プレゼンスなど) を定義します。 定義済みのプロバイダーは、シナリオの中で特定の問題状況に対応する特定の論理コレクション用のすべてのプロバイダーをグループ化するために使用されます。

Lync Server 管理シェルを使用して集中ログサービス機能を実行するには、CsAdministrator または CsServerAdministrator の役割ベースのアクセス制御 (RBAC) セキュリティグループのメンバーであるか、またはこれら2つのグループのいずれかを含むカスタム RBAC の役割である必要があります。 このコマンドレットが割り当てられているすべての役割ベースのアクセス制御 (RBAC) ロールのリストを返すには (自分自身で作成したカスタム RBAC ロールを含む)、Lync Server 管理シェルまたは Windows PowerShell プロンプトから次のコマンドを実行します。

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Lync Server 2013 cmdlet"}

次に例を示します。

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Set-CsClsConfiguration"}

このトピックの残りの部分では、トラブルシューティングを最適化するために、プロバイダーの定義方法、プロバイダーの変更方法、プロバイダー定義に含まれる内容について説明します。 一元化されたログサービスのコマンドを発行するには、2つの方法があります。 既定では、[ディレクトリ C: \\ Program files \\ Common Files \\ Microsoft Lync Server 2013 clsagent] の下にある CLSController.exe を使うことができ \\ ます。 または、Lync Server 管理シェルを使用して、Windows PowerShell コマンドを発行することもできます。 重要な点は、コマンドラインで CLSController.exe を使用する場合に、プロバイダーが既に定義されていて変更できないシナリオがいくつかありますが、ログレベルを定義できます。 Windows PowerShell を使用すると、ログセッションで使用するために新しいプロバイダーを定義することができます。また、それらの作成、収集内容、データ収集のレベルなども完全に制御できます。

<div class="">


> [!IMPORTANT]  
> 前述したように、プロバイダーは非常に強力です。ただし、シナリオは、プロバイダーが表すコンポーネントに対するトレースの設定と実行を行うために必要な具体的な情報をすべて含んでいるため、プロバイダーよりも強力です。シナリオとプロバイダーのコレクションは、大まかに言うと、大量の情報を収集する多数のコマンドを含むバッチ ファイルを実行することと、多数のコマンドをコマンド ラインから一度に 1 つずつ発行することに相当します。<BR>プロバイダーの詳細を深く把握する必要はありませんが、一元管理サービスには、既に定義されている多数のシナリオが用意されています。 用意されているシナリオを使用して、遭遇する可能性がある問題の大部分に対応できます。 まれに、プロバイダーを作成して定義し、シナリオに割り当てなければならない場合があります。 新しいプロバイダーとシナリオを作成する必要があるかどうかを考慮する前に、用意されている各シナリオを十分に調べることを強くお勧めします。 ここでは、シナリオでのプロバイダー要素の使用によるトレース情報の収集方法を理解するために、プロバイダーの作成に関する情報が提示されていますが、プロバイダーそのものの詳細については説明しません。



</div>

[Lync Server 2013 の中央集中ログサービスの概要](lync-server-2013-overview-of-the-centralized-logging-service.md)については、次のようなシナリオで使用するためにプロバイダーを定義する主な要素を紹介します。

  - **Providers**   OCSLogger に精通している場合、プロバイダーは、トレースエンジンがログを収集する必要があることを OCSLogger に伝えるために選ぶコンポーネントです。 プロバイダーは同じコンポーネントであり、多くの場合、OCSLogger のコンポーネントと同じ名前が付いています。 OCSLogger に精通していない場合は、一元管理サービスでログを収集できるのは、サーバーの役割固有のコンポーネントです。 一元管理サービスの場合、CLSAgent は、プロバイダー構成で定義したコンポーネントのトレースを実行している一元ログサービスのアーキテクチャ部分です。

  - **ログレベル**   OCSLogger では、収集されたデータの詳細レベルの数を選択するオプションを提供しました。 この機能は、一元ログサービスとシナリオの一部であり、 **Type** パラメーターによって定義されます。 次のいずれかを選ぶことができます。
    
      - **すべて**   致命的、エラー、警告、および情報の種類のトレースメッセージを、定義されたプロバイダーのログに収集します。
    
      - **Fatal**   定義されたプロバイダーのエラーを示すトレースメッセージのみを収集します。
    
      - **エラー**   定義されたプロバイダーに関するエラー、および致命的なメッセージを示すトレースメッセージのみを収集します。
    
      - **警告**   定義されたプロバイダーに対して警告を示すトレースメッセージと、致命的エラーおよびエラーメッセージだけを収集します。
    
      - **Info**: 定義済みのプロバイダーについて、情報メッセージに加え、種類が重大、エラー、警告メッセージのトレース メッセージのみを収集します。
    
      - **Verbose**   定義されたプロバイダーの致命的、エラー、警告、情報の種類のすべてのトレースメッセージを収集します。

  - **フラグ**   OCSLogger では、トレースファイルから取得できる情報の種類を定義したプロバイダーごとに、フラグを選択するオプションが提供されました。 プロバイダーに基づいて、次のフラグを選ぶことができます。
    
      - **TF \_接続:**   接続に関連するログエントリを提供します。 これらのログには、特定のコンポーネントとの間で確立された接続に関する情報が含まれます。 これには、重要なネットワークレベルの情報が含まれることもあります (つまり、接続の概念なし)。
    
      - **TF \_セキュリティ**   には、セキュリティに関連するすべてのイベントとログエントリが用意されています。 たとえば、SipStack の場合、これは、ドメイン検証エラー、クライアント認証、承認エラーなどのセキュリティイベントです。
    
      - **TF \_Diag**   は、コンポーネントの診断またはトラブルシューティングに使用できる診断イベントを提供します。 たとえば、SipStack の場合は、証明書のエラー、DNS の警告/エラーがあります。
    
      - **TF \_Protocol**   SIP、統合されたコミュニティコーデックパックメッセージなどのプロトコルメッセージを提供します。
    
      - **TF \_コンポーネント**   は、プロバイダーの一部として指定されたコンポーネントのログを有効にします。
    
      - **All**: プロバイダーで使用できるすべてのフラグを設定します。

<div>

## <a name="to-review-information-about-existing-centralized-logging-service-scenario-providers"></a>既存の集中ログサービスシナリオプロバイダーに関する情報を確認するには

1.  Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。

2.  既存のプロバイダーの構成をレビューするには、次を入力します。
    
        Get-CsClsScenario -Identity <scope and scenario name> 
    
    たとえば、グローバル会議アテンダントに関する情報をレビューするには、次のように入力します。
    
        Get-CsClsScenario -Identity "global/CAA"
    
    このコマンドは、関連するフラグ、設定、およびコンポーネントと共にプロバイダーの一覧を表示します。 表示された情報が不足している場合、または既定の Windows PowerShell リスト形式でリストが長すぎる場合は、別の出力メソッドを定義して追加の情報を表示できます。 これを行うには、次のように入力します。
    
        Get-CsClsScenario -Identity "global/CAA" | Select-Object -ExpandProperty Provider
    
    このコマンドの出力では、各プロバイダーを行分割形式で表示します。プロバイダー名、ログの種類、ログ レベル、フラグ、GUID、および役割が行ごとに表示されます。

</div>

<div>

## <a name="to-define-a-new-centralized-logging-service-scenario-provider"></a>新しい集中ログサービスシナリオプロバイダーを定義するには

1.  Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。

2.  シナリオ プロバイダーは、トレースするコンポーネント、使用するフラグ、および収集する詳細レベルで構成されます。これを実行するには次のように入力します。
    
        $<variableName> = New-CsClsProvider -Name <provider component> -Type <log type> -Level <log level detail type> -Flags <provider trace log flags>
    
    たとえば、Lyss プロバイダーから収集する内容および詳細レベルを定義するトレース プロバイダー定義は、次のようになります。
    
        $LyssProvider = New-CsClsProvider -Name "Lyss" -Type "WPP" -Level "Info" -Flags "All"

-Level では、重大、エラー、警告、および情報メッセージが収集されます。 使用されるフラグは、明示 Ss プロバイダーに対して定義されているすべてのフラグであり、TF \_ Connection、tf \_ DIAG、tf プロトコルを含み \_ ます。

変数 $LyssProvider を定義した後、**New-CsClsScenario** コマンドレットでその変数を使用して Lyss プロバイダーからトレースを収集できます。 このプロバイダーの作成と新しいシナリオへの割り当てを完了するには、次のように入力します。

    New-CsClsScenario -Identity "site:Redmond/RedmondLyssInfo" -Provider $LyssProvider

$LyssProvider は、**New-CsClsProvider** で作成された定義済みのシナリオを含む変数です。

</div>

<div>

## <a name="to-change-an-existing-centralized-logging-service-scenario-provider"></a>既存の集中ログサービスシナリオプロバイダーを変更するには

1.  Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。

2.  既存のプロバイダーの構成を更新または変更するには、次のように入力します。
    
        $LyssProvider = New-CsClsProvider -Name "Lyss" -Type "WPP" -Level "Debug" -Flags "TF_Connection, TF_Diag"
    
    次のように入力することで、プロバイダーを割り当てるシナリオを更新します。
    
        Set-CsClsScenario -Identity "site:Redmond/RedmondLyssInfo" -Provider $LyssProvider

コマンドを実行すると、最終的にシナリオ site:Redmond/RedmondLyssInfo のフラグと割り当てられるプロバイダーのレベルが更新されます。Get-CsClsScenario を使用して、新しいシナリオを表示できます。詳細については、「[Get-CsClsScenario](https://docs.microsoft.com/powershell/module/skype/Get-CsClsScenario)」を参照してください。

<div class="">


> [!WARNING]  
> <STRONG>New-ClsCsProvider</STRONG> は、フラグが有効かどうかを確認しません。 フラグのスペル (TF_DIAG、TF_CONNECTION など) が正しいことを確認してください。 フラグのスペルが正しくない場合、プロバイダーは期待されるログ情報を返すことができません。



</div>

このシナリオに対してプロバイダーを追加するには、次のように入力します。

    Set-CsClsScenario -Identity "site:Redmond/RedmondLyssInfo" -Provider @{Add=$ABSProvider, $CASProvider, S4Provider}

Add ディレクティブで定義される各プロバイダーは、**New-CsClsProvider** プロセスで既に定義されています。

</div>

<div>

## <a name="to-remove-a-scenario-provider"></a>シナリオ プロバイダーを削除するには

1.  Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。

2.  用意されているコマンドレットを使用して、既存のプロバイダーの更新と新しいプロバイダーの作成を実行できます。 プロバイダーを削除するには、**Set-CsClsScenario** に対して Provider パラメーター用の Replace ディレクティブを使用する必要があります。 プロバイダーを完全に削除する唯一の方法は、Update ディレクティブを使用して、削除するプロバイダーを、再定義した同じ名前のプロバイダーに置き換えることです。 たとえば、プロバイダー LyssProvider は、ログの種類、Debug に設定されたレベル、フラグセットは TF CONNECTION と TF DIAG として、WPP で定義され \_ \_ ます。 このフラグを "All" に変更する必要があるとします。 このプロバイダーを変更するには、次のように入力します。
    
        $LyssProvider = New-CsClsProvider -Name "Lyss" -Type "WPP" -Level "Debug" -Flags "All"

     &nbsp;
    
        Set-CsClsScenario -Identity "site:Redmond/RedmondLyssInfo" -Provider @{Replace=$LyssProvider}

3.  シナリオとそれに関連付けられているプロバイダーを完全に削除するには、次のように入力します。
    
        Remove-CsClsScenario -Identity <scope and name of scenario>
    
    次に例を示します。
    
        Remove-CsClsScenario -Identity "site:Redmond/RedmondLyssInfo"
    
    <div class="">
    

    > [!WARNING]  
    > <STRONG>Remove-CsClsScenario</STRONG> コマンドレットは、確認のプロンプトを表示しません。 シナリオは、それに関連付けられているプロバイダーと共に削除されます。 シナリオを初めて作成したときに使用したコマンドを再実行することで、シナリオを再作成できます。 削除したシナリオまたはプロバイダーを回復するための手順はありません。

    
    </div>

**Remove-CsClsScenario** コマンドレットを使用してシナリオを削除すると、シナリオはスコープから完全に削除されます。 作成したシナリオとシナリオの一部であったプロバイダーを使用するには、新しいプロバイダーを作成し、それらを新しいシナリオに割り当てます。

</div>

<div>

## <a name="see-also"></a>関連項目


[Get-CsClsScenario](https://docs.microsoft.com/powershell/module/skype/Get-CsClsScenario)  
[新しい CsClsScenario シナリオ](https://docs.microsoft.com/powershell/module/skype/New-CsClsScenario)  
[削除-CsClsScenario](https://docs.microsoft.com/powershell/module/skype/Remove-CsClsScenario)  
[Set-CsClsScenario](https://docs.microsoft.com/powershell/module/skype/Set-CsClsScenario)  
[新規の CsClsProvider](https://docs.microsoft.com/powershell/module/skype/New-CsClsProvider)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

